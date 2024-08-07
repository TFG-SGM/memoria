# Diagramas

En este anexo se recogen los diagramas diseñados para facilitar la implementación y comprensión del sistema desarrollado. A continuación, son explicados en detalle cada uno de ellos.

## Diagrama de Despliegue

El diagrama de la Figura \ref{anexo3:diagrama-despliegue} muestra la disposición física de los diferentes artefactos software de la aplicación Web en nodos. Se identifican principalmente tres nodos:

- El PC del cliente que contiene la cámara y el navegador. Este último con los archivos específicos del lado del cliente.
- El servidor Web que aloja la [API](#API) accedida por el cliente.
- La base de datos MongoDB Atlas donde se guardan los datos de la aplicación Web en las diferentes colecciones.

```{.plantuml #anexo3:diagrama-despliegue caption="Diagrama de despliegue" frame=single}
@startuml

node "Client PC" {
    node Camera
    node "Web Browser" {
        node CacheStorage
        artifact index.html
        artifact react_components.tsx
    }
}

node "Web Server (Node.js)" {  
    node API
    artifact app.ts
    artifact routers.ts
    artifact controllers.ts
    artifact models.ts
}

database "MongoDB Atlas" as mongodb {
    folder "Collections" {
        frame "admins"
        frame "doctors"
        frame "fs.chunks"
        frame "fs.files"
        frame "patients"
        frame "testTypes"
        frame "tests"
    }
}

index.html --> react_components.tsx 
react_components.tsx --> API : REST API Request
API --> react_components.tsx  : REST API Response
API --> app.ts 
app.ts --> routers.ts 
routers.ts --> controllers.ts 
controllers.ts --> models.ts 
models.ts --> mongodb : Database Operations

@enduml
```

## Diagrama de Base de Datos

El diagrama de la Figura \ref{anexo3:diagrama-bd} muestra las diferentes entidades de la base de datos.  Es importante recordar que esta base de datos es no relacional y utiliza *MongoDB*, lo que significa que no es necesario que cada documento tenga la misma estructura exacta. Sin embargo, se diseñó el diagrama para proporcionar una base de los diferentes atributos que puede tener cada entidad.

En el contexto de la aplicación Web se han identificado principalmente cinco entidades: administrador, médico, paciente, prueba y datos de prueba. 

```{.plantuml #anexo3:diagrama-bd caption="Diagrama de base de datos" frame=single}
@startuml

entity admins{
_id : ObjectId
name : string
surname : string
date : date
city : string 
email : string
phone : string
password : string
uId : string
}

entity doctors{
_id : ObjectId
name : string
surname : string
date : date
city : string 
email : string
phone : string
password : string
uId : string
}

entity patients{
_id : ObjectId
name : string
surname : string
date : date
city : string 
email : string
phone : string
weight : number
height : number
isFibro: boolean
diagnosisYears: number
activityLevel: number
ocupation: string
assignedDoctor : string
uId : string
}

entity tests {
_id : ObjectId
doctorId : string
date : date
typeId : string
patientId: string
videoFile : {name: string, id: string}
evaScale: number
data: {time: string, quality: number, parts: object}
}

entity testTypes {
_id : ObjectId
name : string
bodyParts: string[]
}


entity fs.files {
_id : ObjectId
lenght : number
chunkSize : number
uploadDate : date
filename : string
contentType : string
}

entity fs.chunks {
_id : ObjectId
files_id : ObjectId
n : number
data : BinData
}

patients "1" o-- "1" doctors
patients "1" o-- "0..*" tests
tests "1" o-- "1" doctors
tests "1" o-- "1" testTypes
tests "1" o-- "0..*" fs.files
fs.files "1" o-- "1..*" fs.chunks

@enduml
```

## Diagrama de Secuencia para Iniciar Sesión

El diagrama de la Figura \ref{anexo3:diagrama-secuencia-inicio-sesion} muestra los diferentes pasos que ocurren al iniciar sesión con exito en la aplicación Web. Se puede observar cómo la página de inicio de sesión a través de la clase *DataService* ejecuta la operación *PUT* a la [API](#API), la cual empleando el *AuthController* comprueba si existe el correo electrónico pedido, seguidamente de verificar si la contraseña es correcta. 

Una vez todo se realiza con éxito, el *DataService* añade el token obtenido al almacenamiento local, el cual es empleado para verificar la identidad en posteriores operaciones que realice el usuario.

```{.plantuml #anexo3:diagrama-secuencia-inicio-sesion caption="Diagrama de secuencia de inicio de sesión con exito" frame=single}
@startuml
actor Doctor

Doctor -> LoginPage: Introduce datos
Doctor -> LoginPage: Inicia sesión

LoginPage -> DataService: login()
DataService -> AuthRouter: post("auth/login", {email, password})

AuthRouter -> AuthController : login()
AuthController -> AdminModel : findByEmail({email})
AuthController -> DoctorModel : findByEmail({email})

AdminModel -> "MongoDB Atlas" : findOne({email})
DoctorModel -> "MongoDB Atlas" : findOne({email})

"MongoDB Atlas" -> AuthController : admin/doctor

AuthController -> AuthController : compare(passwords)

AuthController -> AuthController : sign()
AuthController -> AuthRouter : token
AuthRouter -> DataService : token

DataService -> localstorage : setItem("token",token)
DataService -> LoginPage : ok

LoginPage -> Doctor : navigate(/app)

@enduml
```

## Diagrama de Secuencia para Crear un Paciente 

El diagrama de la Figura \ref{anexo3:diagrama-secuencia-creacion-paciente} muestra los diferentes pasos que ocurren al crear un nuevo paciente con éxito en la aplicación Web, teniendo en cuenta que el médico ya está iniciado sesión. 

En el diagrama se puede observar cómo nuevamente a través del *DataService* se ejecuta la operación *POST* en la ruta de paciente. Dicha ruta, antes de continuar con las operaciones, comprueba si el usuario está autentificado y si tiene el rol correcto, en este caso si es un médico. Estas comprobaciones son realizadas por los middlewares *userAuth* y *checkRole*.

Una vez completadas las comprobaciones previas, se pasa a la segunda etapa donde se verifica la validez de los datos del nuevo paciente, así como la existencia previa del correo electrónico en la base de datos. Si todas las verificaciones son exitosas, el nuevo paciente se agrega y el usuario recibe la confirmación en la interfaz.

Es importante destacar que los diagramas de secuencia para la consulta, creación, edición y eliminación de las diferentes entidades de la base de datos siguen un patrón similar al mostrado en este diagrama.

```{.plantuml #anexo3:diagrama-secuencia-creacion-paciente caption="Diagrama de secuencia de creación de un paciente con exito" frame=single}
@startuml
actor Doctor

Doctor -> PatientsListPage: Pincha en botón de crear
PatientsListPage -> Doctor : Enseña menú de creación
Doctor -> PatientsListPage: Introduce los datos necesarios
Doctor -> PatientsListPage: Confirma creación

PatientsListPage -> DataService : createData("/patient", newData)
DataService -> PatientRouter : post("/patient", newData, header)

PatientRouter -> PatientRouter : userAuth()
PatientRouter -> PatientRouter : checkRole("doctor")

PatientRouter -> PatientController : create()

PatientController -> PatientSchema  : validatePatient()
PatientSchema -> PatientController : result
PatientController -> AuthController : validateEmail(email)
AuthController -> PatientController : true
PatientController -> PatientModel : create(result.data)
PatientModel -> "MongoDB Atlas" : insertOne(result.data)

"MongoDB Atlas" -> PatientModel : newPatient 
PatientModel -> PatientController : newPatient
PatientController -> PatientRouter : newPatient
PatientRouter -> DataService: newPatient
DataService -> PatientsListPage : newPatient

PatientsListPage -> Doctor : Muestra nuevo paciente
@enduml
```

## Diagrama de Actividad para Crear una Prueba

El diagrama de la Figura \ref{anexo3:diagrama-actividad-crear-prueba} muestra los diferentes pasos que debe seguir un médico para crear una nueva prueba. En el cual se puede observar que, si el paciente no existe, es necesario crearlo antes de agregar la nueva prueba deseada.

```{.plantuml #anexo3:diagrama-actividad-crear-prueba caption="Diagrama de actividad para crear una prueba" frame=single width=50%}
@startuml
start
:Iniciar sesión;

if (¿Médico registrado?) then (si)
  :Consultar pacientes;

  if (¿Paciente existe?) then (si)

  else (no)
    :Crear paciente;
  endif

    :Consultar pruebas de paciente;

  :Crear Prueba;

else (no)
  end
endif

stop
@enduml
```

