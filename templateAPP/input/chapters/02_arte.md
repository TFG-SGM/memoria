# Estado del Arte
En el contexto del desarrollo de una aplicación Web, consideramos esenciales diversos factores, incluyendo la metodología de desarrollo, las herramientas y tecnologías disponibles, y la usabilidad de la aplicación. En este capítulo se realiza un análisis que abarca todas estas áreas con el propósito de determinar las mejores prácticas y enfoques para implementar durante el proyecto. Sin embargo, antes de detallar estos aspectos es crucial comprender el trastorno de la fibromialgia, que es el foco de la aplicación web que se busca desarrollar.

## Fibromialgia

La fibromialgia, tal y como expone *MayoClinic* @fibromialgia, es un trastorno que se caracteriza por dolor generalizado en los músculos y huesos acompañado de fatiga y dificultades para dormir, recordar y mantener el estado de ánimo. Además, los expertos creen que este trastorno amplifica la sensación de dolor al afectar la manera en que el cerebro y la médula espinal procesan las señales de dolor y no dolor.

Los síntomas suelen iniciarse tras un evento como un trauma físico, cirugía, infección o estrés psicológico significativo. En otros casos, los síntomas se desarrollan gradualmente sin un desencadenante específico.

Las mujeres tienen más probabilidad que los hombres de padecer fibromialgia. Además del dolor, muchas personas con este trastorno experimentan dolores de cabeza tensionales, problemas en la articulación temporomandibular, síndrome de colon irritable, así como ansiedad y depresión.

Aunque no hay una cura definitiva para la fibromialgia, existen varios medicamentos que pueden ayudar a controlar los síntomas. Además, el ejercicio, técnicas de relajación y medidas para reducir el estrés pueden ser beneficiosas en el manejo de esta condición.

Como se ha mencionado previamente, la aplicación Web que se pretende desarrollar durante este proyecto tiene como objetivo analizar el movimiento de las personas para comprobar si presentan este trastorno, además de indicar visualmente la calidad de movimiento de las diferentes partes del cuerpo. Para lograr este objetivo se requiere que el paciente realice ciertas pruebas que involucran movimiento. Sin embargo, antes de realizar estas pruebas, el médico evalúa el nivel de dolor del paciente utilizando la escala  [EVA](#EVA).

La escala [EVA](#EVA), tal y como expone Basterrechea @escala-eva, se basa en una escala horizontal representada por una línea normalmente de 10 centímetros en la que el paciente debe marcar el lugar en el que considera que se encuentra su dolor.

Los resultados se evalúan normalmente en tres niveles de dolor según los valores marcados:

- (<4): Los valores inferiores a 4 indican que el dolor es leve o leve-moderado.
- (4-6): En el caso de que la medición sea entre 4 y 6 centímetros, el dolor se considera de moderado a moderado-grave.
- (>6): Si los valores son mayores de 6 se considera un dolor que pasa de grave a insoportable.

Una vez presentado el trastorno de la fibromialgia y la escala [EVA](#EVA), en el siguiente punto se explican las diferentes metodologías de desarrollo software que se pueden utilizar para implementar la aplicación Web.

## Metodologías de Desarrollo Software

El desarrollo de software es un proceso fundamental en la creación de aplicaciones Web y otros sistemas informáticos. Este proceso conocido como "ciclo de vida del desarrollo del software" implica una serie de etapas que van desde la concepción de la idea hasta la implementación y mantenimiento del producto final. Para gestionar eficientemente este ciclo es crucial adoptar una metodología de desarrollo adecuada. En este punto se realiza un análisis de las distintas fases de dicho proceso, además de las metodologías más destacadas.

### Ciclo de Vida del Desarrollo del Software
El ciclo de vida del desarrollo de software es un proceso estructurado que abarca desde la concepción de un proyecto hasta su despliegue y mantenimiento. A lo largo de este ciclo se llevan a cabo una serie de fases y actividades. Cada fase del ciclo de vida del desarrollo de software tiene sus propios objetivos y entregables específicos. Este normalmente está dividido en las siguientes fases, tal y como expone Clark @ciclo-vida-desarrollo-software.

- **Planificación y análisis:** Se elabora un plan que describe en detalle cómo se dará vida al proyecto desde la idea hasta la realización.
- **Definición de requisitos:** Se recopilan los diferentes requisitos para la aplicación final.
- **Diseño:** Se elabora un documento de diseño de software que incluye el diseño del sistema, los lenguajes de programación, las plantillas, la plataforma a utilizar y las medidas de seguridad de la aplicación.
- **Desarrollo:** Se transforman los requisitos en código para desarrollar la propia aplicación.
- **Pruebas:** Se realizan pruebas de validación para asegurar que esté funcionando correctamente y haga lo que debe hacer.
- **Despliegue:** Se entrega al usuario final.
- **Mantenimiento:** Se arreglan los diferentes errores que encuentren los usuarios, teniendo que volver a la primera fase del ciclo si fuera necesario.

Una vez presentado el ciclo de desarrollo, es esencial saber cómo organizar el mismo. Para ello, en el siguiente punto se analizan las diferentes metodologías de desarrollo.

### Metodologías de Desarrollo
Para organizar cada una de las fases, como se ha mencionado previamente, es necesario implementar una metodología de desarrollo con el fin de aumentar la productividad y la calidad del software. A continuación, se detallan algunas de las metodologías más destacadas, tal y como expone Alona @metodologias-desarrollo.

- **Cascada:** Se trata de una de las metodologías más antiguas. En este caso, las fases de desarrollo se realizan de una manera secuencial, es decir, una fase comienza solo cuando termina la fase anterior. Aunque esto hace que la estructura sea más clara y fácil de entender, tiene la desventaja de ser poco flexible y adaptable a los cambios de los requisitos que tan a menudo se ven en un desarrollo de software. 
- **Iterativa:** Esta metodología divide el proyecto en pequeñas partes y cada parte es desarrollada, probada e implementada de manera iterativa. Cada una de estas iteraciones agrega funcionalidad al software.
- **En V:** En esta metodología se relaciona cada fase de desarrollo con su fase de pruebas correspondiente. De esta manera, pone un gran énfasis en la validación temprana de requisitos y la calidad del software. No obstante, similar a la metodología en cascada, su enfoque lineal puede resultar inflexible frente a cambios en los requisitos.
- **Espiral:** Se trata de una metodología que mezcla los elementos de la planificación en cascada con la flexibilidad de las metodologías ágiles. Utiliza ciclos repetitivos, incluyendo planificación, evaluación de riesgos, ingeniería y evaluación del cliente. Aunque es bastante efectivo en la gestión de riesgos, puede acabar resultando muy complejo de gestionar, además de requerir más tiempo y recursos que otras metodologías. 
- **Big bang:** Esta metodología tiene un enfoque único en el que los desarrolladores se lanzan directamente a la codificación sin mucha planificación. Esto significa que los requisitos se implementan a medida que aparecen, es decir, sin ningún tipo de hoja de ruta clara. Sin embargo, a la hora de necesitar realizar algún cambio puede llegar a requerir una renovación completa del software.
- **Ágil:** Esta metodología organiza las fases del ciclo de vida en varios ciclos de desarrollo, de forma que el equipo realiza pequeños cambios de software incrementales en cada uno de estos ciclos. Esto lo hace ideal para proyectos de desarrollo de software que requieran flexibilidad y capacidad de adaptarse a los cambios con el tiempo.

Al final, la elección de la metodología de desarrollo de software es esencial para el éxito del proyecto y debe ajustarse a las particularidades del mismo. Cada enfoque tiene sus propias fortalezas y debilidades. Sin embargo, la metodología ágil puede ser la que más destaque para el desarrollo de software debido a su agilidad, ciclos cortos de desarrollo y capacidad para adaptarse a cambios en los requisitos. En el siguiente punto se analizan algunas de las metodologías ágiles más utilizadas en la actualidad.

### Metodologías Ágiles
Como ya se ha mencionado, las metodologías ágiles son las que más destacan en la actualidad debido a su flexibilidad para adaptarse a los cambios. A continuación, son analizadas tres de las más usadas hoy en día, tal y como expone Espírito @metodologias-agiles:

- **Extreme programming:** Consiste en una metodología ágil que se centra en la mejora continua y la respuesta rápida a los cambios en los requisitos. Para ello, pone énfasis en la retroalimentación constante y la comunicación abierta, destacando prácticas como la programación en parejas, pruebas unitarias continuas y entregas frecuentes. 
- **Kanban:** Con origen en la manufactura, esta metodología ágil se ha conseguido aplicar con éxito al desarrollo de software. Se basa principalmente en la visualización del flujo de trabajo mediante el uso de tableros Kanban, representando cada tarea mediante tarjetas que se mueven a través de columnas que representan diferentes estados del proceso. A pesar de la mejora continua y flexibilidad que ofrece, se puede notar la ausencia de una estructura para roles y eventos, lo que dificulta la gestión de proyectos más grandes.
- **Scrum:** Muy conocido y usado en la actualidad. En Scrum, los ciclos de desarrollo se llaman “Sprints” que generalmente duran entre dos y cuatro semanas. Además, utiliza roles definidos claramente como el Scrum Master, el Product Owner y el equipo de desarrollo. También, se enfoca en la entrega iterativa de incrementos de software y gracias a su énfasis en la comunicación constante y adaptabilidad al cambio se ha convertido en una elección popular en el desarrollo de proyectos software como es el caso de la implementación de una aplicación Web.

Al final, la elección de la metodología depende de las características del proyecto. Siendo en este caso Scrum la que más destaca entre todas ellas, debido a su enfoque iterativo e incremental que permite una mayor flexibilidad y adaptabilidad a los cambios en el proyecto. Sin embargo, una vez presentado el proceso y las diferentes metodologías del desarrollo de software, es esencial conocer la tecnología Web que se puede utilizar para el desarrollo de dicho software, la cual se detalla en el siguiente punto.

## Tecnología Web
En el proceso de implementación de una aplicación Web resulta esencial no solo seguir una metodología específica, sino también utilizar la diversa tecnología Web disponible. Este campo de estudio abarca un extenso conjunto de herramientas, estándares y prácticas que han sido utilizadas en el desarrollo, implementación y mantenimiento de aplicaciones y sitios Web. Desde los aspectos del lado del cliente hasta los del servidor, este panorama tecnológico tiene como objetivo primordial mejorar la experiencia del usuario y optimizar la eficiencia en el desarrollo. A continuación, se profundiza en todas estas tecnologías.

### Tecnología Fundamental en la Web

Dentro del desarrollo Web, los lenguajes de marcado y de programación fundamentales están compuestos por la tríada formada de [HTML](#HTML), [CSS](#CSS) y *JavaScript*, siendo este último extendido mediante *TypeScript*. A continuación, se realiza una breve explicación de cada uno de estos lenguajes, tal y como exponen *Mozilla* @html @css y Cherni @libro-typescript.

- **HTML:** Lenguaje de marcado estándar utilizado para estructurar el contenido de las páginas Web. Define la jerarquía y organización de los elementos en una página.
- **CSS:** Lenguaje de estilo que complementa a [HTML](#HTML). Permite definir el diseño, la presentación y la apariencia visual de los elementos [HTML](#HTML), proporcionando control sobre colores, tipografías y disposición.
- **JavaScript:** Se trata del lenguaje de programación del lado del cliente que permite la creación de interactividad en las páginas Web. Es esencial para manipular el [DOM](#DOM) y responder a eventos.
- **TypeScript @typescript:** Es un lenguaje de programación fuertemente tipado que extiende *JavaScript*. A diferencia de este último, *TypeScript* añade un sistema de tipos estático, proporcionando beneficios como la detección temprana de errores y una mejor mantenibilidad en proyectos a gran escala. Esta diferencia se puede ver ilustrada en la Figura \ref{capitulo2:circulo-typescript}.

![TypeScript vs JavaScript\label{capitulo2:circulo-typescript}](cap2_circulo-typescript.png){width=40%}

Una vez presentada la tecnología fundamental en la Web, en el siguiente punto se explica el concepto de las [SPA](#SPA), así como los diferentes *frameworks* más utilizados para desarrollar dichas aplicaciones. 

### Aplicaciones de una Sola Página

Una [SPA](#SPA), como expone Holmes en @spa, es una aplicación que opera dentro del navegador y no requiere recargar la página durante su uso, a diferencia de una aplicación de múltiples páginas.

Para desarrollar una [SPA](#SPA) se emplea la técnica de desarrollo conocida como [AJAX](#AJAX), como describe *Mozilla* [@ajax].

La técnica [AJAX](#AJAX) implica que la aplicación Web solicite contenido al servidor mediante peticiones [HTTP](#HTTP) asíncronas. Luego, utiliza este nuevo contenido para actualizar las secciones relevantes de la página sin necesidad de recargarla por completo, lo que significa que solo se necesita solicitar el [HTML](#HTML) y el [CSS](#CSS) en la petición inicial.

Inicialmente, [AJAX](#AJAX) se implementaba mediante la interfaz *XMLHttpRequest*, pero en la actualidad son más comunes el uso de la *API fetch* [@api-fetch] y la biblioteca *Axios* [@axios].

Por otro lado, como expone Rivera @spa-routers, es importante entender la diferencia entre el enrutado tradicional conocido como "enrutado en el lado del servidor" y el enrutado empleado en una [SPA](#SPA) conocido como "enrutado en el lado del cliente".

En el enrutado en el lado del servidor, cada vez que el usuario hace click en un nuevo enlace, el navegador pide al servidor una página completamente nueva, como se ilustra en la Figura \ref{capitulo2:enrutado-servidor}. 

```{.plantuml #capitulo2:enrutado-servidor caption="Enrutado en el lado del servidor" frame=single width=50%}
@startuml
actor Usuario

Usuario -> Interfaz: Escribe una URL
Interfaz -> Controlador: getURL(u)
Controlador -> Servidor: getURL(u)

Servidor -> Controlador: page
Controlador -> Interfaz: page
Interfaz -> Usuario: showPage()

Usuario -> Interfaz: Hace click en link
Interfaz -> Controlador: getURL(u)
Controlador -> Servidor: getURL(u)

Servidor -> Controlador: newPage
Controlador -> Interfaz: newPage
Interfaz -> Usuario: showPage()

@enduml
```

Por otro lado, en el enrutado en el lado del cliente, cuando el usuario hace click en un nuevo enlace, el navegador renderiza el nuevo contenido en la misma página, pero a la vez simula un cambio en la [URL](#URL) con el fin de otorgar feedback al usuario. La Figura \ref{capitulo2:enrutado-cliente} ilustra este tipo de enrutado.

```{.plantuml #capitulo2:enrutado-cliente caption="Enrutado en el lado del cliente" frame=single width=75%}
@startuml
actor Usuario

Usuario -> Interfaz: Escribe una URL
Interfaz -> Controlador: getURL(u)
Controlador -> Servidor: getURL(u)

Servidor -> Controlador: page
Controlador -> Interfaz: page
Interfaz -> Usuario: showPage()

Usuario -> Interfaz: Hace click en link
Interfaz -> Controlador: getURL(u)
Controlador -> Controlador: changeURL(u)
Controlador -> Interfaz: renderNewContent()

note right
Se renderiza un nuevo contenido en la 
misma página con distinta URL
end note

Interfaz -> Usuario: showPage()
@enduml
```

Finalmente, para desarrollar una [SPA](#SPA) se utilizan *frameworks* que complementan a la tecnología fundamental de la Web mencionada en el punto anterior. A continuación, se presentan cuatro de estos *frameworks*, tal y como expone Baryshevskiy @tendencias-tecnologias-web: *React*, *Angular*, *Vue* y *Svelte*.

- **React @react:** Desarrollado por *Facebook*, *React* es una biblioteca de *JavaScript* que se centra en la construcción de interfaces de usuario reactivas y eficientes. Su enfoque en la creación de componentes modulares y su capacidad para gestionar el estado de manera efectiva lo convierten en una elección popular para aplicaciones dinámicas y escalables.
- **Angular @angular:** Respaldado por *Google*, es un *framework* completo de desarrollo que abarca desde la creación de componentes hasta la gestión del estado y el enrutamiento. Su estructura robusta y su integración con *TypeScript* ofrecen un enfoque amplio para el desarrollo de [SPAs](#SPA), siendo especialmente adecuado para proyectos empresariales complejos.
- **Vue.js @vuejs:** Se trata de un *framework* progresivo de *JavaScript* que destaca por su simplicidad y flexibilidad. Su diseño modular facilita la integración gradual en proyectos existentes y su curva de aprendizaje suave lo convierte en una opción popular para desarrolladores que buscan una alternativa accesible y potente.
- **Svelte @svelte:** Adopta un enfoque diferente al trasladar gran parte del trabajo de construcción a tiempo de compilación. Esto resulta en aplicaciones más livianas y rápidas en tiempo de ejecución. Su sintaxis sencilla y su rendimiento eficiente lo hacen atractivo para desarrolladores que buscan una alternativa innovadora y eficaz en la construcción de [SPAs](#SPA).

Una vez presentadas las [SPA](#SPA) y los diferentes *frameworks*, en el siguiente punto se detallan las librerías más utilizadas hoy en día para visualizar datos en la Web.

### Librerías para Visualización de Datos

Diversas librerías han surgido para facilitar la creación de visualizaciones atractivas e interactivas, después de todo la visualización de datos desempeña un papel fundamental en la comprensión y comunicación efectiva de información en entornos Web. A continuación, son presentadas algunas de las librerías más destacadas, tal y como expone Majorek @librerias-visualizacion-datos:

- **D3.js @d3js:** Destaca como una herramienta poderosa para la manipulación basada en datos. Su capacidad para crear visualizaciones altamente personalizables e interactivas lo convierte en una opción popular para desarrolladores que buscan flexibilidad en la representación gráfica de datos complejos.
- **Three.js @threejs:** Aunque inicialmente diseñada para gráficos 3D, *Three.js* puede ser aprovechada para visualizaciones de datos tridimensionales impactantes. Su capacidad para crear experiencias visuales inmersivas lo convierte en una elección interesante para proyectos ambiciosos.
- **Chart.js @chartjs:** Aporta una solución simple y fácil de usar, ofreciendo una variedad de gráficos, como barras, líneas y radar. Esta librería en *JavaScript* permite a los desarrolladores incorporar rápidamente visualizaciones atractivas en sus aplicaciones Web.
- **ECharts @echarts:** Ofrece una amplia variedad de gráficos, incluyendo líneas, barras, dispersión y mapas, entre otros. La capacidad de *Echarts* para manejar grandes conjuntos de datos y su enfoque en la interactividad hacen que sea una elección sólida para proyectos que requieren visualizaciones dinámicas y atractivas. 
- **Highcharts @highcharts:** Con una amplia gama de opciones de personalización, *Highcharts* simplifica la creación de gráficos interactivos. Esta librería en *JavaScript* es adecuada para proyectos que buscan una solución robusta y fácil de implementar.
- **React-Vis @reactvis:** Diseñada específicamente para trabajar con *React*, *React-Vis* proporciona componentes listos para usar que facilitan la incorporación de visualizaciones de datos en aplicaciones *React*. Es una elección eficiente para proyectos que utilizan este marco de trabajo.

Una vez presentados los fundamentos de la Web, las [SPA](#SPA) y las diferentes librerías para visualizar datos, en el siguiente punto se expone la diversa tecnología que existe en el lado del servidor.

### Tecnología en el Lado del Servidor

En el lado del servidor se puede encontrar un ecosistema diverso de lenguajes de programación, cada uno acompañado de sus propios *frameworks*, además de la presencia crucial de las bases de datos. En este análisis se explora detenidamente cada una de estas áreas tecnológicas.

Por un lado, los lenguajes de programación, los cuales desempeñan un papel significativo, definiendo la estructura y el rendimiento de las aplicaciones. Se destacan principalmente cuatro lenguajes, tal y como expone Osadchuk @tecnologia-backend: *JavaScript*, *Python*, *Ruby* y *PHP*.

- **JavaScript:** Se trata de un lenguaje de programación versátil y ampliamente utilizado que funciona tanto en el lado del cliente como en el lado del servidor. En el contexto del desarrollo del lado del servidor, se emplea en el entorno de ejecución **Node.js @nodejs**, que utiliza el motor *V8* de *Google Chrome*. *JavaScript* es destacado por su capacidad para manejar operaciones de entrada/salida de manera eficiente y su naturaleza asíncrona, lo que lo hace ideal para aplicaciones escalables y basadas en eventos como aplicaciones Web en tiempo real.
- **Python @python:** Consiste en un lenguaje versátil y de alto nivel que enfatiza la legibilidad del código y la productividad del programador. Con una sintaxis clara y concisa, *Python* es utilizado en una amplia gama de aplicaciones, desde desarrollo Web hasta inteligencia artificial y análisis de datos. 
- **Ruby @ruby:** Es conocido por su elegancia y simplicidad, priorizando la productividad del desarrollador. Aunque es menos ubicuo que otros lenguajes, ha ganado popularidad gracias a su enfoque en la facilidad de uso y la creación de código conciso y expresivo.
- **PHP:** Se trata de un lenguaje de programación especialmente diseñado para el desarrollo Web. Ampliamente utilizado para construir aplicaciones Web dinámicas, *PHP* se integra fácilmente con [HTML](#HTML) y se ejecuta en el lado del servidor.

Estos lenguajes, aunque poderosos por sí mismos, se ven mejorados cuando se combinan con *frameworks* específicos. Cada uno de los mencionados tiene su conjunto de *frameworks* que agilizan y estructuran el proceso de desarrollo. A continuación, se explora un *framework* representativo para cada uno de estos lenguajes respectivamente, tal y como expone nuevamente Osadchuk @tecnologia-backend: *Express*, *Django*, *Ruby* on *Rails* y *Laravel*.

- **Express.js @expressjs:** Es un *framework* para Node.js que simplifica el desarrollo de aplicaciones Web y [API](#API)s. Con un enfoque minimalista, permite la creación rápida de servidores y rutas, facilitando la construcción de aplicaciones robustas con *JavaScript* del lado del servidor.
- **Django @django:** Es un *framework* de alto nivel para *Python*, diseñado para maximizar la eficiencia y la reutilización del código. Con un conjunto integrado de herramientas y una arquitectura basada en el patrón de diseño [MVC](#MVC), *Django* simplifica la creación de aplicaciones Web complejas al proporcionar una estructura organizativa y características como la administración automática de bases de datos.
- **Ruby on Rails @rubyonrails:** Es un *framework* que sigue el principio de convención sobre configuración para el desarrollo rápido de aplicaciones Web en *Ruby*. Facilita la creación de aplicaciones mediante la automatización de tareas repetitivas y la adopción de convenciones predefinidas. *Rails* proporciona un entorno coherente que acelera el proceso de desarrollo y favorece la escritura de código limpio y conciso.
- **Laravel @laravel:** Es un *framework* elegante y completo para *PHP* que aborda diversos aspectos del desarrollo Web. Ofrece una sintaxis expresiva, una gestión eficiente de bases de datos, y una amplia gama de herramientas para tareas comunes. *Laravel* fomenta la creación de aplicaciones seguras y modernas con un énfasis en la legibilidad y mantenimiento del código.

Por otro lado, en el contexto del desarrollo del lado del servidor consideramos esenciales no solo los lenguajes de programación y sus *frameworks* asociados, sino también las bases de datos, los cuales son elementos fundamentales para la persistencia y gestión de datos. Para una comprensión más detallada, se examinan tres bases de datos específicas, tal y como expone Ramotion @bases-de-datos: *MySQL*, *MongoDB* y *Neo4j*.

- **MySQL @mysql:** Se trata de una [BD](#BD) relacional reconocida por su fiabilidad y consistencia en la gestión de datos estructurados. Ha sido una opción de confianza en el desarrollo Web, proporcionando un entorno robusto para aplicaciones que dependen de una estructura de datos clara y relaciones definidas.
- **MongoDB @mongodb:** Destaca como una [BD](#BD) no relacional orientada a documentos ofreciendo flexibilidad en el esquema y una capacidad eficaz para manejar grandes volúmenes de datos no estructurados. Esta característica la convierte en una elección popular para aplicaciones que requieren escalabilidad y adaptabilidad a cambios en la estructura de datos.
- **Neo4j @neo4j:** Como una [BD](#BD) de grafos, está diseñada para almacenar y procesar datos en forma de nodos y relaciones. Esto la convierte en una opción adecuada para aplicaciones que necesiten modelar y analizar redes complejas como redes sociales, sistemas de recomendación y análisis de relaciones en datos interconectados.

Una vez presentada cada una de las tecnologías del lado del servidor, en el siguiente punto se exponen el concepto de *API REST*, el cual es fundamental en el desarrollo Web hoy en día.

### API REST

Una [API REST](#API REST), como expone *RedHat* @api-rest, es un conjunto de reglas y convenciones para comunicarse con servicios Web de manera eficiente y coherente. Para comprender mejor este concepto, es útil entender tanto qué es una [API](#API) en general como qué significa [REST](#REST).

Por un lado, una [API](#API) es esencialmente un conjunto de definiciones y protocolos que permiten que diferentes aplicaciones se comuniquen entre sí. Funciona como un contrato entre el proveedor de servicios y el usuario, donde se especifica qué puede hacer el usuario con los servicios proporcionados por el proveedor y cómo interactuar con ellos. En el contexto de software, una [API](#API) define las formas en que las distintas partes de un programa pueden interactuar entre sí. En resumen, una [API](#API) proporciona una manera estandarizada y segura para que diferentes aplicaciones se comuniquen y compartan datos.

Por otro lado, [REST](#REST) es un estilo arquitectónico que define una serie de principios para diseñar redes de comunicación, particularmente aplicaciones Web. Se basa en el concepto de recursos que son identificadores únicos para entidades específicas (como datos o funciones) en una aplicación Web. [REST](#REST) utiliza métodos estándar de [HTTP](#HTTP), como *GET*, *POST*, *PUT* y *DELETE*, para realizar operaciones en estos recursos. Los recursos son manipulados a través de representaciones, que pueden ser en formatos como [JSON](#JSON), [XML](#XML), [HTML](#HTML), etc. [REST](#REST) promueve una arquitectura basada en el cliente-servidor, donde el servidor proporciona recursos y el cliente los solicita y manipula.

Por lo tanto, una [API REST](#API REST) es una interfaz de programación que sigue los principios y limitaciones de la arquitectura [REST](#REST). Utiliza los métodos estándar de [HTTP](#HTTP) para realizar operaciones en recursos como leer, crear, actualizar y eliminar datos. Cuando un cliente envía una solicitud a través de una [API REST](#API REST), se le devuelve una representación del estado del recurso solicitado en un formato especificado como [JSON](#JSON) o [XML](#HML). Siendo [JSON](#JSON) particularmente popular debido a su legibilidad tanto para humanos como para máquinas y su independencia de cualquier lenguaje de programación específico. En resumen, una [API REST](#API REST) proporciona una forma estándar y eficiente de interactuar con servicios Web basados en [REST](#REST).

Una vez presentada tanto la tecnología del lado del cliente como del servidor, en el siguiente punto se expone la tecnología emergente en la Web.

### Tecnología Emergente

Por último, dentro del ámbito del desarrollo Web destacan innovaciones particulares: *Docker*, *Kubernetes*, *WebAssemby* y *Progressive Web Apps*. Todas ellas son analizadas más en detalle a continuación, tal y como expone Baryshevskiy @tendencias-tecnologias-web.

- **Docker @docker:** Se trata de plataforma de contenedores que posibilita el empaquetado, la distribución y la ejecución coherente de aplicaciones en diversos entornos. Su enfoque revolucionario ha transformado la consistencia y portabilidad en el despliegue de software, permitiendo una gestión eficaz de dependencias y configuraciones. En la Figura \ref{capitulo2:docker-vs-vm} se puede observar la diferencia entre un despliegue de contenedores que comparten el [SO](#SO) y un despliegue de máquinas virtuales que hacen una copia completa del [SO](#SO) cada una.
- **Kubernetes @kubernetes:** Consiste en un sistema de orquestación de contenedores que simplifica la administración, escalabilidad y despliegue de aplicaciones contenidas en entornos distribuidos. Su capacidad para coordinar eficientemente la ejecución de contenedores a lo largo de múltiples nodos ha consolidado su posición como una herramienta fundamental en el despliegue de infraestructuras escalables y resilientes. 
- **WebAssembly (Wasm):** Permite la ejecución de código de alto rendimiento, escrito en lenguajes como *C++* o *Rust*, directamente en el navegador. Esto amplía significativamente las posibilidades para construir aplicaciones Web más potentes y rápidas, acercando el rendimiento de las aplicaciones Web al de las aplicaciones nativas.
- **Progressive Web Apps (PWA):** Ofrecen experiencias avanzadas que combinan lo mejor de las aplicaciones Web y nativas. Su capacidad para funcionar offline permite a los usuarios acceder al contenido incluso en ausencia de conexión a Internet, mejorando la accesibilidad y la continuidad de la experiencia del usuario.

![Despliegue con docker vs con máquinas virtuales @imagen-docker-vs-vm\label{capitulo2:docker-vs-vm}](cap2_docker-vs-vm.png){width=75%}

Una vez presentada la diferente tecnología Web que rodea tanto el lado del *BackEnd* como el lado del *FrontEnd*, es de gran ayuda conocer los stacks tecnológicos más utilizados y analizarlos, lo cual se realiza en el siguiente punto.

### Stacks Tecnológicos
En el contexto de los stacks tecnológicos, es decir, la elección de un conjunto específico de tecnologías, se trata de un aspecto crítico dentro del desarrollo Web, ya que afecta directamente la eficiencia del desarrollo, la escalabilidad y el mantenimiento del sistema. A continuación son explicadas brevemente cuatro stacks, tal y como expone Campana @stacks-tecnologicos: *LAMP*, *Python Django*, *MEAN* y *MERN*.

- **LAMP (Linux, Apache, MySQL, PHP/Python/Perl):** Ha sido un pilar en el desarrollo Web durante muchos años y sigue siendo una opción confiable para una variedad de proyectos tradicionales. *Linux* proporciona el sistema operativo, Apache sirve como servidor Web, *MySQL* maneja la base de datos, y *PHP*, *Python* o *Perl* actúan como lenguajes de programación del lado del servidor. Este conjunto ofrece estabilidad, flexibilidad y una amplia base de conocimientos, siendo especialmente adecuado para aplicaciones Web convencionales.
- **Python Django (Python, Django, Apache, MySQL):** Stack tecnológico compuesto de Python como lenguaje principal de programación, Django como *framework* Web basado en el patrón [MVC](#MVC), Apache como servidor Web para la gestión de solicitudes [HTTP](#HTTP), y *MySQL* como sistema de gestión de bases de datos. Este conjunto es especialmente adecuado para proyectos Web que buscan la combinación de la versatilidad de *Python*, la solidez de *Django*, y la confiabilidad de *Apache* y *MySQL*.
- **MEAN (MongoDB, Express.js, Angular, Node.js):** Es un stack tecnológico basado completamente en *JavaScript*. *MongoDB* es la base de datos [NoSQL](#NoSQL), *Express.js* actúa como el *framework* del lado del servidor, *Angular* es el *framework* del lado del cliente y *Node.js* proporciona el entorno de ejecución del servidor. Este stack ha ganado popularidad por su coherencia en el uso de un solo lenguaje de programación (*JavaScript* / *TypeScript*) en todo el flujo de desarrollo, lo que simplifica la colaboración entre los equipos de desarrollo y permite una transición más fluida de los datos entre el servidor y el cliente.
- **MERN (MongoDB, Express.js, React, Node.js):** Similar a *MEAN*, pero reemplaza *Angular* con *React* en el lado del cliente. *React* ha ganado una enorme popularidad por su enfoque declarativo y su capacidad para construir interfaces de usuario altamente interactivas. *MERN* comparte las ventajas de *MEAN*, pero además permite a los desarrolladores aprovechar las características distintivas de *React* para crear experiencias de usuario más dinámicas y eficientes.

A raíz de esto, se puede concluir que la elección entre los diferentes stacks tecnológicos que existen depende de las necesidades específicas del proyecto y las preferencias del equipo de desarrollo. Teniendo cada stack sus propias ventajas y pudiendo ser la elección correcta según los requisitos particulares de la aplicación que se esté construyendo.

Finalmente, en la Tabla \ref{capitulo2:tabla-tecnologia} se puede observar una visualización detallada de la tecnología abordada en este capítulo. Siendo destacable como cada stack tecnológico está compuesto por diferentes tipos de tecnologías, demostrando así la diversidad y complejidad de las soluciones presentadas.

| **Stack**         | **SO** | **Servidor** | **BD** |  **Lenguaje**   | **BackEnd** | **FrontEnd** |
| ---------------------- | :---------: | :----------: | :-----------: | :---------------: | :---------: | :----------: |
| **LAMP**          |     Linux     |    Apache    |     MySQL     | PHP/Python/Perl |      -      |      -       |
| **Python Django** |       -       |    Apache    |     MySQL     |     Python      |   Django    |      -       |
| **MEAN**          |       -       |      -       |    MongoDB    |   JavaScript    | Express.js  |   Angular    |
| **MERN**          |       -       |      -       |    MongoDB    |   JavaScript    | Express.js  |    React     |

:Tecnología presentada en el capítulo 2.2\label{capitulo2:tabla-tecnologia}

Una vez presentada la tecnología para construir una aplicación Web, en el siguiente punto se detallan los proveedores de hosting para poder desplegar dicha aplicación. 

### Proveedores de Hosting

Como se ha mencionado anteriormente, es importante comprender cómo publicar una aplicación Web en Internet, para lo cual se recurre a proveedores de hosting.

Un proveedor de hosting, tal y como expone *Google* @hosting-providers, posee servidores y ofrece espacio a sus clientes, quienes utilizan ese espacio para almacenar sus páginas Web haciéndolas accesibles a cualquier persona en Internet. Para elegir un proveedor de hosting es crucial entender la diferencia entre sitios estáticos y dinámicos, como expone Spilotro @dynamic-vs-static.

Por un lado, un sitio estático permanece igual en todo momento, es decir, su contenido no cambia. Por otro lado, un sitio dinámico, como una aplicación Web, presenta un contenido variable según el usuario que lo visite. Para crear estos últimos se requiere un servidor y una base de datos utilizando la tecnología mencionada previamente.

Existen varios proveedores de hosting para sitios dinámicos, siendo uno de los más populares y fáciles de usar las [PaaS](#PaaS). Estas plataformas, como expone Chai @paas, gestionan muchos detalles a bajo nivel, permitiendo a los desarrolladores concentrarse más en la construcción de aplicaciones en lugar de configurar y administrar el servidor.

En el pasado, la elección de un proveedor [PaaS](#PaaS) era más sencilla debido a la existencia de *Heroku* @heroku, que ofrecía un plan gratuito muy favorable para el despliegue de aplicaciones Web. Sin embargo, a partir de 2022 esta versión gratuita dejó de existir, como expone Wise @heroku-price, provocando que hoy en día sea más difícil elegir un proveedor [PaaS](#PaaS) entre la multitud disponible, tal y como expone Batschinski @heroku-alternatives. En la Figura \ref{capitulo2:planes-gratuitos-paas} se detallan los planes gratuitos que ofrecen algunas de las plataformas más populares. Las características comparadas incluyen el número de aplicaciones que se pueden desplegar de forma gratuita, el número de horas de uso permitidas, si el servicio se desconecta tras un período de inactividad y si se requiere una tarjeta de crédito para su utilización.

| **Plataforma**          | **N.º Apps** | **Horas de Uso**      | **Desconexión**           | **Tarjeta** |
| -------------------- | ----------- | --------------------- | ----------------------------- | ------- |
| **Fly.io @flyio**       | Tres      | Ilimitado             | Nunca                     | Si      |
| **Railway app @railway** | Ilimitado | Subvención de 5€ | Nunca                     | No      |
| **Adaptable.io @adaptable** | Ilimitado | Ilimitado             | Nunca                     | Si      |
| **Render @render**      | Ilimitado | 750 al mes            | 15 minutos de inactividad | No      |

: Planes gratuitos de [PaaS](#PaaS)\label{capitulo2:planes-gratuitos-paas}

Una vez presentada toda la tecnología que se puede utilizar a la hora de construir una aplicación Web. Es fundamental tener en cuenta las diferentes técnicas de visualización que existen para asegurar que el usuario entienda los datos que se muestran con dicha aplicación. Estas técnicas son analizadas en el siguiente punto. 

## Técnicas de Visualización de Datos
Como se ha mencionado previamente, el desarrollo de la aplicación Web deseada requiere la presentación atractiva de datos para los usuarios, lo que implica el uso de técnicas de visualización de datos existentes. En esencia, esto implica la transformación de una gran cantidad de información en un formato visual comprensible mediante elementos gráficos. Esto permite comunicar relaciones complejas entre los datos para mejorar la comprensión por parte de los usuarios. A continuación, se realiza un análisis de las diversas técnicas según lo expuesto por Wilke @fundamentals-data-visualization, Yi y Restori @chartio, y Holtz @data-viz. Estas técnicas se agrupan en seis categorías principales: distribución, correlación, ranking, parte de un todo, evolución y otras técnicas. 

### Técnicas de Distribución

Las técnicas de distribución se utilizan para comprender cómo se distribuyen los datos en un conjunto. Esto es crucial para comprender la dispersión y la concentración de los valores. Las visualizaciones de distribución permiten identificar patrones, valores atípicos y la forma general de la distribución de los datos. Dentro de este grupo se encuentran las técnicas que se enumeran a continuación:

- El histograma
- El gráfico de densidad
- El diagrama de caja y bigotes
- El diagrama de violín

Por un lado, el histograma toma como entrada únicamente una variable numérica. Esta variable se divide en varios intervalos y el número de observaciones por intervalo se representa mediante la altura de las barras, como se ilustra en la Figura \ref{capitulo2:histograma}. Utilizando esta técnica es posible representar la distribución de varias variables en el mismo *eje Y* de esta forma compararlas.

![Histograma @data-viz\label{capitulo2:histograma}](cap2_histograma.png){width=75%}

Por otro lado, una versión más suave del histograma es el gráfico de densidad, el cual representa la distribución de una variable numérica utilizando una estimación de densidad del núcleo para mostrar la función de densidad de probabilidad de la variable. En la Figura  \ref{capitulo2:grafico-densidad} se ve el mismo ejemplo anterior, pero esta vez usando un gráfico de densidad. Nuevamente, al igual que el histograma, es posible representar varias variables en el mismo eje.

![Gráfico de densidad @data-viz\label{capitulo2:grafico-densidad}](cap2_grafico-densidad.png){width=75%}

El diagrama de cajas y bigotes proporciona un buen resumen de una o más variables numéricas. Este tipo de diagramas está compuesto por varios elementos, como muestra la Figura \ref{capitulo2:diagrama-caja-componentes}. La desventaja de estos diagramas es que resumir también significa perder información. Por ejemplo, en el diagrama de cajas y bigotes de la Figura \ref{capitulo2:diagrama-caja} es fácil concluir que el de color verde tiene un valor más alto que los demás. Sin embargo, no se puede ver la distribución subyacente de puntos en cada grupo ni su número de observaciones. Es por eso que, si la cantidad de datos no es muy grande, es una buena práctica añadir lo que se conoce como "*jitter*" al gráfico, como muestra la Figura \ref{capitulo2:diagrama-caja-jitter}.

![Componentes del diagrama de caja y bigotes @diagrama-caja-componentes\label{capitulo2:diagrama-caja-componentes}](cap2_diagrama-caja-componentes.png){width=75%}

![Diagrama de caja y bigotes @data-viz\label{capitulo2:diagrama-caja}](cap2_diagrama-caja.png){width=75%}

![Diagrama de caja y bigotes con "*jitter*" @data-viz\label{capitulo2:diagrama-caja-jitter}](cap2_diagrama-caja-jitter.png){width=75%}

Sin embargo, si se tiene un tamaño de muestra grande, usar "*jitter*" provocaría que los puntos se superpondrían entre ellos. Por lo que, una alternativa es usar el diagrama de violín que permite visualizar la distribución de una variable numérica para uno o varios grupos. Cada "violín" representa un grupo o una variable. La forma representa la estimación de densidad de la variable: cuanto más datos haya en un rango específico, más grande será el "violín" para ese rango. Es muy similar a un diagrama de caja y bigotes, pero permite una comprensión más profunda de la distribución. En la Figura \ref{capitulo2:diagrama-violin} se ve un ejemplo de este tipo de diagramas.

![Diagrama de violin @data-viz\label{capitulo2:diagrama-violin}](cap2_diagrama-violin.png){width=75%}

Una vez presentadas las técnicas utilizadas para comprender la distribución de los datos, en el siguiente punto se detallan las técnicas para conocer la relación entre ellos.

### Técnicas de Correlación

Las técnicas de correlación revelan la relación entre dos o más variables. Determinar esta relación entre variables es fundamental para comprender cómo cambian juntas y si existe alguna dependencia entre ellas. Las visualizaciones de correlación ayudan a identificar patrones, tendencias y posibles relaciones causales entre variables. Dentro de este grupo se encuentran las técnicas que se enumeran a continuación:

- El gráfico de dispersión
- El gráfico de burbujas
- El mapa de calor

El diagrama de dispersión muestra la relación entre 2 variables numéricas. Para cada punto de datos, el valor de su primera variable se representa en el *eje X* y el de la segunda en el *eje Y*, tal y como se ilustra en la Figura \ref{capitulo2:diagrama-dispersion}.

![Diagrama de dispersión @data-viz\label{capitulo2:diagrama-dispersion}](cap2_diagrama-dispersion.png){width=75%}

Por otro lado, como se observa en la Figura \ref{capitulo2:grafico-burbujas}, si al diagrama de dispersión se le agrega una tercera dimensión a través del tamaño de los puntos, se trataría de un gráfico de burbujas.

![Gráfico de burbujas @data-viz\label{capitulo2:grafico-burbujas}](cap2_grafico-burbujas.png){width=75%}

Finalmente, el mapa de calor consiste en una representación gráfica de datos donde los valores individuales contenidos en una matriz se representan como colores. Se puede observar un ejemplo en la Figura \ref{capitulo2:mapa-calor}.

![Mapa de calor @data-viz\label{capitulo2:mapa-calor}](cap2_mapa-calor.png){width=75%}

Una vez presentadas las técnicas utilizadas para conocer la relación entre los datos, en el siguiente punto se detallan las técnicas para clasificarlos.

### Técnicas de Ranking

Las técnicas de ranking se centran en comparar y ordenar valores para identificar los más altos, los más bajos o cualquier otro criterio de clasificación. Estas visualizaciones son útiles para comprender la posición relativa de los elementos dentro de un conjunto de datos y para identificar tendencias o patrones de comportamiento. Dentro de este grupo se encuentran las técnicas que se enumeran a continuación:

- La gráfica de barras
- El gráfico lollipop
- El gráfico de barras circular
- El gráfico radial

El gráfico de barras es una herramienta visual ampliamente empleada para la representación de datos, siendo su función principal la de mostrar la relación entre una variable numérica y una variable categórica. Siendo cada categoría representada mediante una barra, y el valor numérico mediante la longitud de dicha barra.

Es importante destacar que estos gráficos permiten comparar los valores entre distintos grupos. Esto se logra colocando las barras una al lado de la otra o apilándolas entre sí. Además, cuando las etiquetas de las categorías son muy largas, se recomienda invertir los ejes y crear un gráfico de barras horizontal para una mejor visualización, tal y como muestra la Figura \ref{capitulo2:grafico-barras}. Esto facilita la lectura de las etiquetas y la interpretación de los datos.

![Gráfico de barras @data-viz\label{capitulo2:grafico-barras}](cap2_grafico-barras.png){width=75%}

Al tratarse de un gráfico tan común, el diagrama de barras puede resultar aburrido. Es por este motivo que surgieron variaciones como el gráfico lollipop que sustituye las barras por una línea y un punto, como se ve en la Figura \ref{capitulo2:grafico-lollipop} y el gráfico de barras circular ilustrado en la Figura \ref{capitulo2:grafico-barras-circular}. Este último es más difícil de leer, por lo que es una buena práctica utilizarlos cuando la diferencia entre las barras es muy obvia o hay muchas que mostrar.

![Gráfico lollipop @data-viz\label{capitulo2:grafico-lollipop}](cap2_grafico-lollipop.png){width=75%}

![Gráfico de barras circular @data-viz\label{capitulo2:grafico-barras-circular}](cap2_grafico-barras-circular.png){width=75%}

Finalmente, dentro de este grupo se encuentra el gráfico radial, el cual consiste en un gráfico bidimensional diseñado para representar una o más series de valores sobre múltiples variables cuantitativas. Cada variable tiene su propio eje, y todos los ejes están unidos en el centro del gráfico. Una práctica común es comparar varios individuos en un mismo gráfico, como se muestra en la Figura \ref{capitulo2:grafico-radial}, o en caso de que sean muchos individuos, mostrarlos en gráficos separados.

![Gráfico radial @data-viz\label{capitulo2:grafico-radial}](cap2_grafico-radial.png){width=75%}

A pesar de su atractivo visual, los gráficos radar no suelen ser ampliamente utilizados debido a que al tener un formato circular, pueden resultar más difíciles de interpretar. Este formato tampoco permite ordenar los valores de manera efectiva. Además, el dibujo que se forma puede variar según el orden de las categorías, a pesar de que los datos sean los mismos.

Una vez presentadas las técnicas utilizadas para ordenar los diferentes valores, en el siguiente punto se detallan las técnicas para conocer como los datos se proporcionan según el todo.

### Técnicas de Parte de un Todo

Las técnicas de parte de un todo, como indica su nombre, muestran cómo se dividen los datos en partes proporcionales al todo. Son útiles para comprender la composición de un conjunto de datos y para visualizar la distribución de los valores en relación con el conjunto completo. Las visualizaciones de parte de un todo permiten identificar las contribuciones relativas de cada componente y compararlos entre sí. Dentro de este grupo se encuentran las técnicas que se enumeran a continuación:

- El gráfico de pastel
- El mapa de árbol
- El diagrama de sol

El gráfico de pastel, caracterizado por un círculo dividido en secciones que representan proporciones del total, se emplea comúnmente para visualizar porcentajes, donde la suma total alcanza el 100%. A pesar de su popularidad, este tipo de representación resulta difícil de interpretar debido a la baja capacidad humana para percibir con precisión ángulos. Esta dificultad se evidencia al intentar determinar cuál de las secciones es la más grande en diferentes gráficos, como el mostrado en la Figura \ref{capitulo2:grafico-tarta}, seguido de la comparación con la Figura \ref{capitulo2:grafico-barras-apiladas} que presenta los mismos datos pero en un formato de barras.

![Gráfico de tarta @data-viz\label{capitulo2:grafico-tarta}](cap2_grafico-tarta.png){width=75%}

![Gráfico de barras apiladas @data-viz\label{capitulo2:grafico-barras-apiladas}](cap2_grafico-barras-apiladas.png){width=75%}

De este ejemplo se deduce que las alternativas más efectivas son los gráficos de barras y los de lollipop explicados en el grupo anterior, los cuales pueden emplearse también en este contexto. Asimismo, los mapas de árbol constituyen otra alternativa viable.

Los mapas de árbol muestran datos jerárquicos como un conjunto de rectángulos anidados. Cada grupo se representa mediante un rectángulo, cuya área es proporcional a su valor. Mediante esquemas de color o interactividad, es posible representar varias dimensiones. En la Figura \ref{capitulo2:mapa-arbol} se puede observar un ejemplo de este tipo de diagramas.

![Mapa de árbol @data-viz\label{capitulo2:mapa-arbol}](cap2_mapa-arbol.png){width=75%}

Por último, una técnica muy similar al mapa de árbol, pero con un diseño radial, es el diagrama de sol, tal y como se ilustra en la Figura \ref{capitulo2:diagrama-sol}. Este tipo de diagramas muestran una estructura jerárquica, siendo el origen de la organización el centro del círculo, y cada nivel es representado con un anillo adicional. El último nivel (hojas) se encuentra en la parte exterior extrema del círculo. 

![Diagrama de sol @data-viz\label{capitulo2:diagrama-sol}](cap2_diagrama-sol.png){width=75%}

Una vez presentadas las técnicas utilizadas para conocer las proporciones de los datos, en el siguiente punto se detallan las técnicas que indican la evolución de los datos a lo largo del tiempo.

### Técnicas de Evolución

Las técnicas de evolución muestran cómo cambian los datos a lo largo del tiempo o en relación con otra variable. Son esenciales para identificar tendencias, patrones estacionales, ciclos y cambios a largo plazo en los datos. Las visualizaciones de evolución permiten comprender la dinámica temporal de los fenómenos y tomar decisiones informadas basadas en estos cambios. Dentro de este grupo se encuentran las técnicas que se enumeran a continuación:

- La gráfica de línea
- La gráfica de área
- La gráfica de área apilada

La gráfica de línea es una herramienta visual que representa la evolución de una o varias variables numéricas a lo largo del tiempo. En este tipo de gráfica los puntos de datos se disponen en orden según su valor en el *eje X* y se conectan mediante segmentos de línea recta, como se muestra en la Figura \ref{capitulo2:grafica-linea}. Además, de representar la evolución temporal de una única variable, las gráficas de línea también pueden utilizarse para comparar la evolución de varias variables simultáneamente. 

Es importante destacar que en este tipo de gráficas no se suelen señalar los datos. No obstante, es una buena práctica señalarlos con un punto cuando se trata de una muestra pequeña, lo que contribuye a mantener la claridad y la precisión en la representación visual de los datos, facilitando su interpretación por parte del lector.

![Gráfica de línea @data-viz\label{capitulo2:grafica-linea}](cap2_grafica-linea.png){width=75%}

En el caso que el área entre el *eje X* y la línea esté rellena de un color como se ilustra en la Figura \ref{capitulo2:grafica-area} se trataría de una gráfica de área. Por otro lado, una extensión de este tipo es la gráfica de área apilada, que consiste en un gráfico de área que muestra la evolución de varios grupos en la misma gráfica. Los valores de cada grupo se muestran encima de cada uno, lo que permite comprobar la evolución del total y la importancia de cada grupo. La Figura \ref{capitulo2:grafica-area-apilada} muestra un ejemplo de este tipo de gráficas.

![Gráfica de área @data-viz\label{capitulo2:grafica-area}](cap2_grafica-area.png){width=75%}

![Gráfica de área apilada @data-viz\label{capitulo2:grafica-area-apilada}](cap2_grafica-area-apilada.png){width=75%}

Finalmente, una vez presentadas las técnicas utilizadas para conocer la evolución de los datos, en el siguiente punto se detallan otras técnicas de visualización interesantes.

### Otras Técnicas

Este grupo abarca diversas técnicas que no se ajustan directamente a las categorías anteriores debido a la gran variedad de enfoques disponibles, un ejemplo son las visualizaciones especializadas para representar datos geoespaciales, como el mapa ilustrado en la Figura \ref{capitulo2:mapa}.

![Mapa @data-viz\label{capitulo2:mapa}](cap2_mapa.png){width=75%}

Otro tipo de visualizaciones que entraría dentro de esta categoría son las visualizaciones de flujo, como el diagrama de cuerdas, que representa conexiones entre nodos. Cada nodo se representa mediante un fragmento en la parte exterior del diseño circular, y se trazan arcos entre cada par de entidades. El tamaño de cada arco es proporcional a la importancia del flujo. La Figura \ref{capitulo2:diagrama-cuerdas} muestra un ejemplo de este tipo de diagramas.

![Diagrama de cuerdas @data-viz\label{capitulo2:diagrama-cuerdas}](cap2_diagrama-cuerdas.png){width=75%}

Por último, dentro de este grupo también se incluye la visualización de datos en su forma individual cuando solo se desea mostrar un único dato, así como en formato de tabla.

Una vez se han presentado las diferentes técnicas de visualización de datos que existen, es crucial conocer la disciplina de la [IPO](#IPO), concepto que se detalla mejor en el siguiente punto.

## Interacción Persona-Ordenador 
Por último, para el desarrollo de una aplicación Web enfocada en el lado del cliente es indispensable detenerse para hablar de la disciplina de la [IPO](#IPO), de la experiencia de usuario y de la usabilidad. A continuación, se detallan cada uno de estos conceptos. 

### Concepto de la IPO
La [IPO](#IPO) es definida por [SIGCHI](#SIGCHI) como “la disciplina relacionada con el diseño, evaluación e implementación de sistemas informáticos interactivos para el uso de seres humanos, y con el estudio de los fenómenos más importantes con los que está relacionado” @toni-ipo.

Dentro de esta disciplina se pueden encontrar distintos aspectos, los cuales se pueden ver reflejados en la Figura \ref{capitlo2:interaccion-persona-ordenador}. Por un lado, se observa una persona con sus características de procesamiento de la información, tanto las de comunicación como las físicas que interactúa con un ordenador. El cual también tiene sus propias características. Por otro lado, en medio se encuentran los dispositivos de entrada y salida que relacionan a la persona con el ordenador, comunicándose mediante diferentes elementos de diseño.

Además, la Figura \ref{capitlo2:interaccion-persona-ordenador} muestra que la persona no está sola, sino que realiza el trabajo dentro de una organización social, siendo posible gracias a un proceso de desarrollo en el que cada uno de estos componentes debe ser abordado con igual grado de implicación y no caer en el error de obviar la parte humana, centrándose solamente en la parte tecnológica.

![Flujo de la disciplina de la [IPO](#IPO) @toni-ipo\label{capitlo2:interaccion-persona-ordenador}](cap2_flujo-ipo.png){width=75%}

A raíz de todo esto, se puede decir que la disciplina de la [IPO](#IPO) es la encargada de estudiar la experiencia de usuario de la aplicación Web. Concepto que se detalla más en profundidad en el siguiente punto.

### Experiencia de Usuario

El término de experiencia de usuario no tiene una definición consensuada, sin embargo, una de las más destacadas es la que propone el estándar [ISO](#ISO) DIS 9241-210:2008 @iso-ux, definiendo este concepto como "las percepciones y respuestas de una persona que resultan del uso y/o uso anticipado de un producto, sistema o servicio".

Además, la experiencia de usuario presenta diferentes facetas a considerar para el diseño o evaluación de un sistema interactivo. Sin embargo, nuevamente al igual que ocurre con su definición, todavía no están consensuadas ni por la comunidad científica ni por ningún organismo de estandarización. A continuación, se mencionan diferentes facetas para diferentes autores:

- El autor Peter Morville @morville definió la colmena de la UX en la que se incluyen: usable, útil, deseable, valioso, creíble, encontrable y accesible como atributos a considerar para obtener una experiencia de usuario positiva.
- Autores como Hassenzahl y Tractinsky @hassenzahl proponen tres facetas: más allá de lo instrumental; experimental; y emociones y afectos.
- Otros referentes como Hassan Montero y Ortego Santamaría @hassan-montero señalan al usuario, contexto y contenido como los componentes más importantes dentro de la experiencia de usuario.

Para concluir, Granollers sugiere la siguiente definición @toni-ux cubriendo los diferentes aspectos: “la experiencia de usuario atiende a todos los factores, tanto internos como externos del usuario y del sistema interactivo que causen alguna sensación a quien esté utilizando un sistema interactivo concreto en un determinado contexto de uso”. Entre estos factores se encuentra la usabilidad, la cual es explicada en el siguiente punto.

### Usabilidad

El concepto de usabilidad fue introducido por J. Nielsen @libro-nielsen, quien concluyó que un sistema software tiene dos componentes: el aspecto funcional y la forma en que los usuarios pueden usar este aspecto, siendo este último el que es tratado para mejorar la usabilidad de una aplicación. Por consiguiente, los aspectos que se tienen en cuenta al hablar de usabilidad serían la facilidad de aprendizaje, la efectividad de uso y la satisfacción con las que las personas son capaces de realizar sus tareas.

Teniendo esto en cuenta, la usabilidad se puede definir coloquialmente como “fácil de usar o de utilizar y de aprender” @toni-usabilidad. Definición que se considera correcta, pero incompleta, ya que el concepto engloba muchos más aspectos. Es por ello que el organismo de estandarización [ISO](#ISO) propone dos definiciones:

- "La medida en la que un producto se puede usar por determinados usuarios para conseguir objetivos específicos con efectividad, eficiencia y satisfacción en un contexto de uso especificado" propuesta por la [ISO](#ISO) 9241-11  @iso92.
- "La capacidad que tiene un producto software para ser atractivo, entendido, aprendido, usado por el usuario cuando es utilizado bajo unas condiciones específicas" propuesta por la [ISO](#ISO)/IEC 9126 @iso91.

Una vez se ha definido el concepto de usabilidad se debe saber que este tiene un gran conjunto de atributos, los cuales Granollers @toni-usabilidad los resumen en: facilidad de aprendizaje, sintetizabilidad, familiaridad, consistencia, flexibilidad, robustez, recuperabilidad, tiempo de respuesta, adecuación de tareas y disminución de la carga cognitiva.

Al final, se puede concluir que para conseguir un buen grado de usabilidad en una aplicación se requiere pensar en el usuario, lo cual se consigue diseñando una interfaz centrada en el usuario. Esto implica conocer las particularidades de los usuarios para cada caso y reflejarlas en la interacción de la interfaz. Aunque un equipo de desarrollo pueda implementar sistemas similares, es crucial involucrar a los usuarios desde el inicio para lograr una familiaridad que proporcione seguridad y relajación durante la manipulación del sistema.

El objetivo es lograr una interfaz fácil de usar y aprender, lo cual requiere una estrecha colaboración con los usuarios a lo largo de todo el proceso de desarrollo. Implicar a los usuarios desde el principio es fundamental y no se debe confundir con simplemente diseñar pensando en el usuario sin su participación activa. Es crucial conocer la opinión de los usuarios de primera mano para garantizar la utilidad y la comodidad de la interfaz.

Además, los sistemas interactivos deben centrarse en todos los usuarios considerando las diferencias individuales, incluso teniendo en cuenta a aquellos con discapacidades. Ignorar a los usuarios o dejar su participación a la fase final del proyecto puede resultar en una interfaz que no cumple con sus necesidades y expectativas. En resumen, el diseño de sistemas interactivos implica hacer del usuario el foco principal desde el inicio del proceso hasta la implementación final, abarcando la diversidad de usuarios y sus características específicas.

A raíz de todo esto, se puede concluir que la usabilidad es un factor a tener muy en cuenta a la hora de desarrollar la aplicación Web deseada, tema que es abordado con mayor detalle en los próximos capítulos.
