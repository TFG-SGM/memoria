# Diagramas

En este anexo se recogen los diferentes diagramas desarrollados para facilitar la implementación del sistema. Dichos diagramas son los siguientes:

- Figura \ref{anexo3:diagrama-casos-de-uso}: Diagrama de casos de uso.
- Figura \ref{anexo3:diagrama-despliegue}: Diagrama de despliegue.
- Figura \ref{anexo3:diagrama-clases}: Diagrama de clases de controladores y modelos.
- Figura \ref{anexo3:diagrama-bd}: Diagrama de base de datos.
- Figura \ref{anexo3:diagrama-secuencia-inicio-sesion}: Diagrama de secuencia de inicio de sesión.
- Figura \ref{anexo3:diagrama-secuencia-creacion-paciente}: Diagrama de secuencia de creación de paciente.
- Figura \ref{anexo3:diagrama-actividad-crear-prueba}: Diagrama de actividad para crear una prueba. 

```{.plantuml #anexo3:diagrama-casos-de-uso caption="Diagrama de casos de uso" frame=single}
@startuml
skinparam actorStyle awesome
left to right direction
rectangle Sistema {
	usecase (Iniciar sesión)
	usecase (Consultar pacientes)
	usecase (Añadir paciente)
	usecase (Editar paciente)
	usecase (Eliminar paciente)
	usecase (Consultar médicos)
	usecase (Añadir médico)
	usecase (Editar médico)
	usecase (Eliminar médico)
	usecase (Consultar pruebas de paciente)
	usecase (Añadir prueba para paciente)
	usecase (Eliminar prueba de paciente)
	usecase (Consultar datos de prueba)
	usecase (Consultar evolución de paciente)
}

Médico --> (Iniciar sesión)
Médico --> (Consultar pacientes)
Médico --> (Añadir paciente)
Médico --> (Editar paciente)
Médico --> (Eliminar paciente)
Médico --> (Consultar médicos)
Médico --> (Añadir médico)
Médico --> (Editar médico)
Médico --> (Eliminar médico)
Médico --> (Consultar pruebas de paciente)
Médico --> (Añadir prueba para paciente)
Médico --> (Eliminar prueba de paciente)
Médico --> (Consultar datos de prueba)
Médico --> (Consultar evolución de paciente)

(Iniciar sesión) <-- Administrador
(Consultar pacientes) <-- Administrador
(Añadir paciente) <-- Administrador
(Editar paciente) <-- Administrador
(Eliminar paciente) <-- Administrador
(Consultar médicos) <-- Administrador
(Añadir médico) <-- Administrador
(Editar médico) <-- Administrador
(Eliminar médico) <-- Administrador
@enduml
```

```{.plantuml #anexo3:diagrama-despliegue caption="Diagrama de despliegue" frame=single}
@startuml

node "PC Cliente" {
node Camara
node "Navegador Web" {
artifact index.html
artifact react_components.tsx
}
}
node "Servidor Web" {
node API

artifact app.ts
artifact routers.ts
artifact controllers.ts
artifact models.ts

}
database "MongoDB Atlas"

@enduml

```

```{.plantuml #anexo3:diagrama-clases caption="Diagrama de clases de controladores y modelos" frame=single}
@startuml
AdminController ..> AdminModel
DoctorController ..> DoctorModel
PatientController ..> PatientModel
TestController ..> TestModel

class AdminController {
	void getAll()
	void getById()
	void create()
	void update()
	void delete()
}

class AdminModel {
	admin[] getAll()
	admin getById()
	admin create()
	void update()
	void delete()
}

class DoctorController {
	void getAll()
	void getById()
	void create()
	void update()
	void delete()
}

class DoctorModel {
	doctor[] getAll()
	doctor getById()
	doctor create()
	void update()
	void delete()
}

class PatientController {
	void getAll()
	void getById()
	void create()
	void update()
	void delete()
}

class PatientModel {
	patient[] getAll()
	patient getById()
	patient create()
	void update()
	void delete()
}

class TestController {
	void getAll()
	void getById()
	void create()
	void update()
	void delete()
}

class TestModel {
	test[] getAll()
	test getById()
	patient create()
	void update()
	void delete()
}


@enduml
```

```{.plantuml #anexo3:diagrama-bd caption="Diagrama de base de datos" frame=single}
@startuml


entity Admin{
_id : string
name : string
surname : string
bornDate : date
address : string 
email : string
phone : number
password : string
}

entity Doctor{
_id : string
name : string
surname : string
bornDate : date
address : string 
email : string
phone : number
password : string
}

entity Patient{
_id : string
name : string
surname : string
bornDate : date
address : string 
email : string
phone : number
}

entity Test {
_id : string
doctor : Doctor
date : date
type : string
patientId: string
videoFile : file
}

entity TestData{
_id : string
testId: string
...data
}

Doctor --o Test
Patient o-- Test
Test *-- TestData
@enduml
```

```{.plantuml #anexo3:diagrama-secuencia-inicio-sesion caption="Diagrama de secuencia de inicio de sesión con exito" frame=single}
@startuml
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

```{.plantuml #anexo3:diagrama-secuencia-creacion-paciente caption="Diagrama de secuencia de creación de un paciente con exito" frame=single}
@startuml
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

```{.plantuml #anexo3:diagrama-actividad-crear-prueba caption="Diagrama de actividad para crear una prueba" frame=single}
@startuml
start
:Iniciar sesión;

if (¿Médico registrado?) then (si)
  :Consultar pacientes;

  if (¿Paciente existe?) then (si)
    :Consultar pruebas de paciente;

  else (no)
    :Crear paciente;
    :Consultar pruebas de paciente;
  endif

  :Crear Prueba;

else (no)
  end
endif

stop
@enduml
```

