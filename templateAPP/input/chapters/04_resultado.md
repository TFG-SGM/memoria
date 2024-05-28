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
	usecase (Exportar datos de prueba)
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
Médico --> (Exportar datos de prueba)
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

```{.plantuml #capitulo4:diagrama-clases caption="Diagrama de clases ilustrando una arquitectura" frame=single}
@startuml

skinparam class {
    BorderColor black
}
skinparam ArrowColor black

Views ..> DataService
Views ..> TestService

DataService ..> AuthRouter
DataService ..> AdminRouter
DataService ..> DoctorRouter
DataService ..> PatientRouter
DataService ..> TestRouter
DataService ..> TestTypeRouter
DataService ..> FileRouter

AuthRouter ..> AuthController
AdminRouter ..> AdminController
DoctorRouter ..> DoctorController
PatientRouter ..> PatientController
TestRouter ..> TestController
TestTypeRouter ..> TestTypeController
FileRouter ..> FileController

AdminController ..> AdminModel
DoctorController ..> DoctorModel
PatientController ..> PatientModel
TestController ..> TestModel
TestTypeController ..> TestTypeModel

class Views #Plum {}

class TestService #Wheat {
    +number[] getRealMovements(parts: TestPartsData, axis: axisData, actualPart: string)
    +number[] getIdealMovements(parts: TestPartsData, axis: axisData, actualPart: string)
    +string[] getBodyParts(parts: TestPartsData)
    +object getBodyPartsForRadial(parts: TestPartsData)
    +number[] getBodyPartRestriction(parts: TestPartsData)
    +number[] getUniqueVariations(parts: TestPartsData, axis: axisData, actualPart: string)
    +number[] getVariationsCount(parts: TestPartsData, axis: axisData, actualPart: string, uniqueVariations: number[])
    +number[] getBoxPlotData(movements: number[])
    +any[][] getCorrelatedVariations(parts: TestPartsData, axis: axisData, parts1: string, parts2: string)
    +object getProcessDataForBarChart(data: TestSubData)
    +object getProcessDataForChartEvolution(tests: TestData[])
    -number findQuartile(sortedData: number[], quartile: number)
}

class DataService #Wheat {
    +string getToken()
	+data login(email: string, password: string)
	+void logout()
	+data getData(endpoint: string)
	+data createData(endpoint: string, newData: T) 
	+data createFormData(endpoint: string, newData: T) 
	+data deleteData(endpoint: string) 
	+data updateData(endpoint: string, newData: T) 
	+data updateFormData(endpoint: string, newData: T) 
	+data getUserData() 
	-FormData getFormDataFromObject(data: T) 
}

class AuthRouter #LightGrey {
	void get("/auth/login")
	void post("/auth/user-data")
}

class AdminRouter #LightGrey {
	void get("/admin/")
	void post("/admin/")
	void get("/admin/:id")
	void put("/admin/:id")
	void put("/admin/password/:id")
	void delete("/admin/:id")
}

class DoctorRouter #LightGrey {
	void get("/doctor/")
	void post("/doctor/")
	void get("/doctor/:id")
	void put("/doctor/:id")
	void put("/doctor/password/:id")
	void delete("/doctor/:id")
}

class PatientRouter #LightGrey {
	void get("/patient/")
	void post("/patient/")
	void get("/patient/:id")
	void put("/patient/:id")
	void delete("/patient/:id")
}

class TestRouter #LightGrey {
	void get("/test/")
	void post("/test/")
	void get("/test/:id")
	void put("/test/:id")
	void delete("/test/:id")
	void delete("/test/patient/:patientId")
	void get("/test/attribute")
}

class TestTypeRouter #LightGrey {
	void get("/testType/")
	void get("/testType/:id")
}

class FileRouter #LightGrey {
	void get("/file/:id")
	void delete("/file/:id")
}

class AuthController #LightSkyBlue {
	void validateEmail(email: string)
	void hasPassword(password: string)
	void getUserData(req: Request, res: Response)
	void login(req: Request, res: Response)
}

class AdminController #LightSkyBlue {
	void getAll(req: Request, res: Response)
	void getById(req: Request, res: Response)
	void create(req: Request, res: Response)
	void update(req: Request, res: Response)
	void updatePass(req: Request, res: Response)
	void delete(req: Request, res: Response)
}

class DoctorController #LightSkyBlue {
	void getAll(req: Request, res: Response)
	void getById(req: Request, res: Response)
	void create(req: Request, res: Response)
	void update(req: Request, res: Response)
	void updatePass(req: Request, res: Response)
	void delete(req: Request, res: Response)
}

class PatientController #LightSkyBlue {
	void getAll(req: Request, res: Response)
	void getById(req: Request, res: Response)
	void create(req: Request, res: Response)
	void update(req: Request, res: Response)
	void delete(req: Request, res: Response)
}

class TestController #LightSkyBlue {
	void getAll(req: Request, res: Response)
	void getById(req: Request, res: Response)
	void create(req: Request, res: Response)
	void update(req: Request, res: Response)
	void delete(req: Request, res: Response)
	void deleteByPatient(req: Request, res: Response)
	void getAttributes(req: Request, res: Response)
}

class TestTypeController #LightSkyBlue {
	void getAll(req: Request, res: Response)
	void getById(req: Request, res: Response)
}

class FileController #LightSkyBlue {
	void getById(req: Request, res: Response)
	void delete(req: Request, res: Response)
}

class AdminModel #LightGreen {
	admin[] getAll()
	admin getById({id: string})
	admin create({input: User})
	admin update({id: string, input: User})
	int delete({id: string})
}

class DoctorModel #LightGreen{
	doctor[] getAll()
	doctor getById({id: string})
	doctor create({input: User})
	doctor update({id: string , input: User})
	int delete({id})
}

class PatientModel #LightGreen{
	patient[] getAll()
	patient getById({id: string})
	patient create({input: Patient})
	patient update({id: string, input: Patient})
	int delete({id: string})
}

class TestModel #LightGreen {
	test[] getAll({patientId: string, doctorId: string, typeId: string, date: string, order: string})
	test getById({id: string})
	test create({id: string})
	tes update({id: string})
	int delete({id: string})
	string[] deleteByPatient({patientId: string})
	string[] getAttributes({attribute: string, patientId: string})
}

class TestTypeModel #LightGreen{
	testType[] getAll()
	testType getById({id: string})
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

Una vez presentada la arquitectura de la aplicación DynaViz, en este punto se detallará la guía de utilización de la misma, enfocandose en la instalación de la aplicación y el uso de la misma con el rol tanto del administrador como de médico.

### Instalación

En el caso de querer usar *DynaViz* de manera local, se deberan seguir los siguientes pasos:

1. Iniciar la aplicación Web con `pnpm install`, seguido de `pnpm run dev`.
2. Generar los datos aleatorios con `pnpm run generate`.
3. Iniciar sesión con el correo del administrador o médico (el cual se puede ver en la [BD](#BD) de *MongoDB Compass*) y usando la contraseña "admin" o "doctor" según el rol con el que se este iniciando sesión.

Es importante destacar, que para el adecuado despliegue local es necesario tener instalado el gestor de paquetes *pnpm* y el gestor de base de datos *MongoDB Compass*. 

En los siguientes puntos, se mostrarán los diferentes menús tanto para el rol de administrador como para el rol de médico.

### Rol de Administrador

Por un lado, como administrador se puede administrar los tres tipos de identidades: administradores, médicos y pacientes.

Antes de poder usar *DynaViz*, el administrador debe iniciar sesión desde la ventana mostrada en la Figura \ref{capitulo4:inicio-sesion}. Una vez completado el inicio de sesión, el usuario será dirigido a la ventana de la Figura \ref{capitulo4:inicio-admin}, donde podrá elegir entre consultar administradores, médicos o pacientes.

Dado que la administración de los tres tipos de identidades es similar, se explicará únicamente la administración de médicos. Por lo tanto, al seleccionar la opción de consultar médicos, el administrador será dirigido a la ventana de lista de médicos mostrada en la Figura \ref{capitulo4:lista-medicos}.

En esta ventana, el administrador puede añadir un nuevo médico o seleccionar un médico existente, lo que abrirá una ventana modal (Figura \ref{capitulo4:detalles-medico}) en la que se pueden consultar los detalles, editar o eliminar el médico seleccionado.

Las ventanas modales para crear y editar son similares. En la Figura \ref{capitulo4:nuevo-medico} se muestra la ventana modal de creación, donde se destaca que la imagen es el único campo no obligatorio. Además, el campo de contraseña no se solicita al editar un médico, permitiendo que solo el usuario pueda cambiar su propia contraseña.

Finalmente, el administrador puede consultar y administrar los datos de su cuenta seleccionando el icono en la cabecera de la aplicación Web, lo que abrirá la ventana modal mostrada en la Figura \ref{capitulo4:mi-cuenta}. En dicho menú, el usuario puede editar sus datos tal y como se observa en las Figuras \ref{capitulo4:editar-mi-cuenta} y \ref{capitulo4:editar-contraseña}.

![Ventana de inicio de sesión\label{capitulo4:inicio-sesion}](cap4_inicio-sesion.png)

![Ventana de inicio como administrador\label{capitulo4:inicio-admin}](cap4_inicio-admin.png)

![Ventana de lista de médicos\label{capitulo4:lista-medicos}](cap4_lista-medicos.png)

![Ventana modal de detallas de administrador\label{capitulo4:detalles-medico}](cap4_detalles-medico.png)

![Ventana modal de nuevo médico\label{capitulo4:nuevo-medico}](cap4_nuevo-medico.png)

![Ventana modal de "Mi cuenta"\label{capitulo4:mi-cuenta}](cap4_mi-cuenta.png)

![Ventana modal de edición de datos de cuenta\label{capitulo4:editar-mi-cuenta}](cap4_editar-mi-cuenta.png)

![Ventana modal de edición de contraseña\label{capitulo4:editar-contraseña}](cap4_editar-contraseña.png)

### Rol de Médico

Por otro lado, como médico se puede administrar únicamente pacientes, pero de una manera más avanzada que los administradores, teniendo la posibilidad de gestionar las pruebas de dichos pacientes.

Al igual que los administradores, el médico debe iniciar sesión para usar *DynaViz* desde la ventana de la Figura \ref{capitulo4:inicio-sesion}. Una vez iniciada la sesión, el médico será dirigido directamente a la ventana de lista de pacientes, donde solo se listan los pacientes asignados al médico que ha iniciado sesión.

En esta ventana, el médico puede añadir un nuevo paciente, desde la ventana modal mostrada en la Figura \ref{capitulo4:nuevo-paciente} o consultar los detalles de uno existente. Similar al rol de administrador, en la ventana modal de los detalles del paciente, se puede editar o eliminar al paciente. Sin embargo, al iniciar sesión como médico, habrá un tercer botón para consultar las pruebas del paciente, tal como se muestra en la Figura \ref{capitulo4:detalles-paciente}.

En la ventana de la lista de pruebas mostrada en la Figura \ref{capitulo4:lista-pruebas}, el médico puede elegir entre añadir una nueva prueba, consultar una prueba existente o consultar la evolución del paciente.

Por un lado, si el médico decide añadir una nueva prueba, aparecerá la ventana modal de la Figura \ref{capitulo4:nueva-prueba}, donde puede o bien usar un vídeo grabado previamente o bien grabar un vídeo desde *DynaViz*, tal como se muestra en la Figura \ref{capitulo4:grabando-video}.

Por otro lado, si el médico decide consultar una prueba existente, se dirigirá a una nueva ventana para analizar la prueba (Figura \ref{capitulo4:grafica-lineas}). En dicha ventana, el médico puede consultar los detalles de la prueba, donde, como se muestra en la Figura \ref{capitulo4:detalles-prueba}, se puede eliminar la prueba; exportar los datos a un documento PDF, como se muestra en las Figuras \ref{capitulo4:exportar-datos} y \ref{capitulo4:documento-prueba}; y elegir entre las diferentes gráficas para visualizar los datos. A continuación, se listan todas las gráficas que existen en *DynaViz*:

- Gráfico de líneas mostrado en la Figura \ref{capitulo4:grafica-lineas}
- Gráfico de barras mostrado en la Figura \ref{capitulo4:grafica-barras}
- Gráfico radial mostrado en la Figura \ref{capitulo4:grafica-radar}
- Gráfico de pastel mostrado en la Figura \ref{capitulo4:grafica-pastel}
- Mapa de árbol mostrado en la Figura \ref{capitulo4:grafica-arbol}
- Histograma mostrado en la Figura \ref{capitulo4:grafica-histograma}
- Diagrama de cajas y bigotes mostrado en las Figuras \ref{capitulo4:grafica-cajas1} y Figura \ref{capitulo4:grafica-cajas2}
- Gráfico de burbujas mostrado en la Figura \ref{capitulo4:grafica-burbujas}
- Mapa de calor mostrado en la Figura \ref{capitulo4:grafica-calor}

Por último, en el caso de consultar la evolución, el médico será dirigido a la ventana de la Figura \ref{capitulo4:grafica-evolucion}, donde, como se puede observar, el médico puede filtrar el análisis de la evolución tanto por el tipo de prueba como por la parte del cuerpo específica. A continuación, se listan los tres tipos de gráficas de evolución que existen en *DynaViz*:

- Gráfico de líneas mostrada en la Figura \ref{capitulo4:grafica-evolucion-lineas}
- Gráfico de barras mostrada en la Figura \ref{capitulo4:grafica-evolucion-barras}
- Gráfico radial mostrada en la Figura \ref{capitulo4:grafica-evolucion-radar}

Además, cabe destacar que cada una de las gráficas viene acompañada de un botón de ayuda, el cual hace aparecer una ventana modal similar a la Figura \ref{capitulo4:grafica-ayuda}.

Finalmente, al igual que el rol de administrador, el médico puede consultar y administrar los datos de su cuenta en las mismas ventanas modales mostradas en las Figuras \ref{capitulo4:mi-cuenta}, \ref{capitulo4:editar-mi-cuenta} y \ref{capitulo4:editar-contraseña}.

Una vez, presentada la guía de utilización, en los siguientes puntos se detallaran las pruebas unitarias realizadas durante el desarrollo así como la compatibilidad de *DynaViz*.

![Ventana de lista de pacientes como médico\label{capitulo4:lista-pacientes-medico}](cap4_lista-pacientes-medico.png)

![Ventana modal de nuevo paciente\label{capitulo4:nuevo-paciente}](cap4_nuevo-paciente.png)

![Ventana modal de detalles de paciente\label{capitulo4:detalles-paciente}](cap4_detalles-paciente.png)

![Ventana de lista de pruebas\label{capitulo4:lista-pruebas}](cap4_lista-pruebas.png)

![Ventana modal de nueva prueba\label{capitulo4:nueva-prueba}](cap4_nueva-prueba.png)

![Venatana modal grabando vídeo de prueba\label{capitulo4:grabando-video}](cap4_grabando-video.png)

![Ventana modal de detalles de prueba\label{capitulo4:detalles-prueba}](cap4_detalles-prueba.png)

![Venatana modal para exportar datos de prueba\label{capitulo4:exportar-datos}](cap4_exportar-datos.png)

![Documento PDF generado al exportar datos de prueba\label{capitulo4:documento-prueba}](cap4_documento-prueba.png)

![Gráfico de líneas\label{capitulo4:grafica-lineas}](cap4_grafica-lineas.png)

![Gráfico de barras\label{capitulo4:grafica-barras}](cap4_grafica-barras.png)

![Gráfico radial\label{capitulo4:grafica-radar}](cap4_grafica-radar.png)

![Gráfico de pastel\label{capitulo4:grafica-pastel}](cap4_grafica-pastel.png)

![Mapa de árbol\label{capitulo4:grafica-arbol}](cap4_grafica-arbol.png)

![Histograma\label{capitulo4:grafica-histograma}](cap4_grafica-histograma.png)

![Diagrama de cajas y bigotes de desplazamientos\label{capitulo4:grafica-cajas1}](cap4_grafica-cajas1.png)

![Diagrama de cajas y bigotes de variaciones\label{capitulo4:grafica-cajas2}](cap4_grafica-cajas2.png)

![Gráfico de burbujas\label{capitulo4:grafica-burbujas}](cap4_grafica-burbujas.png)

![Mapa de calor\label{capitulo4:grafica-calor}](cap4_grafica-calor.png)

![Ventana de análisis de evolución\label{capitulo4:grafica-evolucion}](cap4_grafica-evolucion.png)

![Gráfico de líneas de evolución\label{capitulo4:grafica-evolucion-lineas}](cap4_grafica-evolucion-lineas.png)

![Gráfico de barras de evolución\label{capitulo4:grafica-evolucion-barras}](cap4_grafica-evolucion-barras.png)

![Gráfico radial de evolución\label{capitulo4:grafica-evolucion-radar}](cap4_grafica-evolucion-radar.png)

![Ventana modal de ayuda\label{capitulo4:grafica-ayuda}](cap4_grafica-ayuda.png)

## Pruebas Unitarias

Durante el desarrollo de DynaViz, se realizaron varias pruebas unitarias con el objetivo de probar los diferentes componentes de *React*. Al final, de los 55 componentes implementados, se han conseguido probar 20 de ellos utilizando la herramienta *Cypress* @cypress, tal y como se observa en la Figura \ref{capitulo4:tests-cases}.

![Lista de componentes probados usando *Cypress*\label{capitulo4:tests-cases}](cap4_tests-cases.png){height=50%}

## Compatibilidad del Sistema

Finalmente, *DynaViz* ha sido probado en los navegadores *Google Chrome v125.0.6422.112*, *Firefox v126.0*, y *Brave v1.66.113*, obteniendo un funcionamiento correcto en todos ellos. Al tratarse de una aplicación Web, se espera que también sea compatible con otros navegadores modernos como *Edge* y *Safari*.

Además, la aplicación es *responsive*, lo que significa que se adapta a las pantallas de dispositivos móviles. Esto se puede apreciar en la Figura \ref{capitulo4:diseño-responsive}, que muestra la ventana de lista de pacientes, la ventana modal de detalles del paciente y la gráfica de líneas, respectivamente.

Una vez se ha presentado la aplicación Web implementada, en el siguiente capítulo se detallará la evaluación de dicho sistema.

![Diseño responsive\label{capitulo4:diseño-responsive}](cap4_diseño-responsive.png)

