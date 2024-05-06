# DynaViz

En este capítulo, se proporcionará un detallado análisis de la aplicación Web DynaViz desarrollada durante el proyecto, acompañado de diversos diagramas y capturas de pantalla que ilustran su funcionamiento. Se explicará en detalle las funcionalidades y la arquitectura del sistema implementado. También, se ofrecerá una guía completa para su utilización. Además, se examinará las diversas técnicas de visualización de datos empleadas y se detallará la compatibilidad del sistema con los diferentes dispositivos.

## Funcionalidades del Sistema

Antes de pasar a explicar el resultado final de la aplicación Web es fundamental detallar las diferentes funcionalidades que se han implementado. Para ello, se debe comprender que la aplicación Web tenía como objetivo el diagnostico de la fibormialgía a través del movimiento. No obstante, este proyecto se concentra en la parte visual del lado del cliente, es decir, en la representación de los datos recopilados, los cuales se analizarán para comprender mejor el problema de la fibromialgia.

Para que este sistema pueda lograr dicho objetivo, es esencial que cumpla con los diferentes casos de uso que muestra la Figura \ref{capitulo4:diagrama-casos-uso}. Los cuales son repartidas en dos roles: administradores y médicos.

```{.plantuml #capitulo4:diagrama-casos-uso caption="Diagrama de casos de uso" frame=single}
@startuml
skinparam actorStyle awesome
left to right direction
rectangle Sistema {
	usecase (Iniciar sesión)
	usecase (Consultar administradores)
	usecase (Añadir administrador)
	usecase (Editar administrador)
	usecase (Eliminar administrador)
	usecase (Consultar médicos)
	usecase (Añadir médico)
	usecase (Editar médico)
	usecase (Eliminar médico)
	usecase (Consultar pacientes)
	usecase (Añadir paciente)
	usecase (Editar paciente)
	usecase (Eliminar paciente)
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
Médico --> (Consultar pruebas de paciente)
Médico --> (Añadir prueba para paciente)
Médico --> (Eliminar prueba de paciente)
Médico --> (Consultar datos de prueba)
Médico --> (Consultar evolución de paciente)

(Iniciar sesión) <-- Administrador
(Consultar administradores) <-- Administrador
(Añadir administrador) <-- Administrador
(Editar administrador) <-- Administrador
(Eliminar administrador) <-- Administrador
(Consultar médicos) <-- Administrador
(Añadir médico) <-- Administrador
(Editar médico) <-- Administrador
(Eliminar médico) <-- Administrador
(Consultar pacientes) <-- Administrador
(Añadir paciente) <-- Administrador
(Editar paciente) <-- Administrador
(Eliminar paciente) <-- Administrador
@enduml
```

Por un lado, los administradores deben poder iniciar sesión y tener la capacidad de consultar, añadir, editar y eliminar otros administradores y médicos.

Por otro lado, los médicos deben poder iniciar sesión en la aplicación y tener la capacidad de consultar, añadir, editar y eliminar tanto médicos como pacientes. También deben tener la capacidad de añadir, gestionar y consultar las pruebas realizadas a los pacientes, además de poder revisar la evolución del paciente según los resultados de estas pruebas. Finalmente, es importante destacar que la visualización de los datos será crucial en la consulta de las diferentes pruebas.

Una vez que se comprenden las diversas funcionalidades del sistema, es esencial pasar a conocer su arquitectura, la cual se detalla en el siguiente punto.

## Arquitectura del Sistema

Como se explicó en el capítulo anterior, la aplicación Web ha sido implementada empleando una arquitectura [MVC](#MVC), la cual se ilustra en la Figura \ref{capitulo4:diagrama-clases} como un diagrama de clases. Es importante destacar que la aplicación ha sido desarrollada utilizando *TypeScript*, un lenguaje que permite el desarrollo orientado a objetos.

```{.plantuml #capitulo4:diagrama-clases caption="Diagrama de clases ilustrando una arquitectura MVC" frame=single}
@startuml

Views ..> DataService
Views ..> TestService

DataService ..> AuthRouter
DataService ..> AdminRouter
DataService ..> DoctorRouter
DataService ..> PatientRouter
DataService ..> TestRouter
DataService ..> TestTypeRouter
DataService ..> VideoRouter

AuthRouter ..> AuthController
AdminRouter ..> AdminController
DoctorRouter ..> DoctorController
PatientRouter ..> PatientController
TestRouter ..> TestController
TestTypeRouter ..> TestTypeController
VideoRouter ..> VideoController

AdminController ..> AdminModel
DoctorController ..> DoctorModel
PatientController ..> PatientModel
TestController ..> TestModel
TestTypeController ..> TestTypeModel

class TestService {
	+number[] getRealMovements(parts,axis,actualPart)
    +number[] getIdealMovements(parts,axis,actualPart)
    +string[] getBodyParts(parts)
    +object getBodyPartsForRadial(parts)
    +number[] getBodyPartRestriction(parts)
    +number[] getUniqueVariations(parts,axis,actualPart)
    +number[] getVariationsCount(parts,axis,actualPart,uniqueVariations)
    +number[] getBoxPlotData(movements)
    +any[][] getCorrelatedVariations(parts,axis,parts1,parts2)
    -number findQuartile(sortedData,quartile)
}

class DataService {
    +string getToken()
	+data login(enail,password)
	+void logout()
	+data getData(endpoint)
	+data createData(endpoint,newData) 
	+data createTestData(endpoin,newData)
	+data deleteData(endpoint) 
	+data updateData(endpoint,newData) 
	+data getUserData() 
	-FormData getFormDataFromObject(data) 
}

class AuthRouter {
	void get("/auth/login")
	void post("/auth/user-data")
}

class AdminRouter {
	void get("/admin/")
	void post("/admin/")
	void get("/admin/:id")
	void put("/admin/:id")
	void put("/admin/password/:id")
	void delete("/admin/:id")
}

class DoctorRouter {
	void get("/doctor/")
	void post("/doctor/")
	void get("/doctor/:id")
	void put("/doctor/:id")
	void put("/doctor/password/:id")
	void delete("/doctor/:id")
}

class PatientRouter {
	void get("/patient/")
	void post("/patient/")
	void get("/patient/:id")
	void put("/patient/:id")
	void delete("/patient/:id")
}

class TestRouter {
	void get("/test/")
	void post("/test/")
	void get("/test/:id")
	void put("/test/:id")
	void delete("/test/:id")
	void delete("/test/patient/:patientId")
	void get("/test/attribute")
}

class TestTypeRouter {
	void get("/testType/")
	void get("/testType/:id")
}

class VideoRouter {
	void get("/video/:id")
	void delete("/video/:id")
}

class AuthController {
	void validateEmail(email)
	void hasPassword(password)
	void getUserData(req,res)
	void login(req,res)
}

class AdminController {
	void getAll(req,res)
	void getById(req,res)
	void create(req,res)
	void update(req,res)
	void updatePass(req,res)
	void delete(req,res)
}

class DoctorController {
	void getAll(req,res)
	void getById(req,res)
	void create(req,res)
	void update(req,res)
	void updatePass(req,res)
	void delete(req,res)
}

class PatientController {
	void getAll(req,res)
	void getById(req,res)
	void create(req,res)
	void update(req,res)
	void delete(req,res)
}

class TestController {
	void getAll(req,res)
	void getById(req,res)
	void create(req,res)
	void update(req,res)
	void delete(req,res)
	void deleteByPatient(req,res)
	void getAttributes(req,res)
}

class TestTypeController {
	void getAll(req,res)
	void getById(req,res)
}

class VideoController {
	void getById(req,res)
	void delete(req,res)
}

class AdminModel {
	admin[] getAll()
	admin getById({id})
	admin create({input})
	admin update({id,input})
	int delete({id})
}

class DoctorModel {
	doctor[] getAll()
	doctor getById({id})
	doctor create({input})
	doctor update({id,input})
	int delete({id})
}

class PatientModel {
	patient[] getAll()
	patient getById({id})
	patient create({input})
	patient update({id,input})
	int delete({id})
}

class TestModel {
	test[] getAll({patientId,doctorId,typeId,date,order})
	test getById({id})
	test create({id})
	tes update({id})
	int delete({id})
	string[] deleteByPatient({patientId})
	string[] getAttributes({attribute, patientId})
}

class TestTypeModel {
	testType[] getAll()
	testType getById({id})
}

@enduml
```

En el diagrama, se pueden observar las diferentes clases distribuidas de abajo hacia arriba, principalmente en los siguientes grupos:

- **Modelos**: Estas clases acceden a la base de datos.
- **Controladores**: Utilizan los diferentes modelos para responder a las diversas solicitudes.
- **Rutas**: Son fundamentales para el desarrollo de la [API](#API) de la aplicación Web. Cuando se solicita un recurso asignado a ellas, invocan al controlador correspondiente.
- **DataService**: Esta clase del lado del cliente se encarga de solicitar los diferentes recursos a la [API](#API) a través de las rutas.
- **TestService**: Esta clase del lado del cliente es utilizada por las diferentes gráficas para obtener los datos.
- **Vistas**: Representan las distintas páginas y ventanas modales de la aplicación Web. Utilizan la clase *DataService* para acceder a los recursos de la base de datos.

Además de emplear la arquitectura [MVC](#MVP), la aplicación Web se trata de una [SPA](#SPA). Como se explicó en capítulos anteriores, esto implica un enrutado en el lado del cliente, lo que hace que la aplicación Web simule el movimiento entre páginas, a pesar de que en realidad sea una única página.

Por último, se anima a leer el Anexo C, donde se muestran los diferentes diagramas diseñados durante el desarrollo del sistema y se profundiza más en la arquitectura del sistema.

Ahora que se conoce la arquitectura de la aplicación Web desarrollada, en el siguiente punto se proporcionará una guía para su utilización.

## Guía de Utilización

### Instalación

(Recuerda: Hablar sobre el script de autogenerar datos)

### Rol de Administrador

### Rol de Médico

## Compatibilidad del Sistema

