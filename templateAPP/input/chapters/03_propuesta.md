# Propuesta de Solución

En este capítulo se proporciona la propuesta diseñada para abordar el problema presentado en el capítulo de introducción. Asimismo, se presenta una explicación detallada de la metodología de desarrollo seleccionada y las herramientas empleadas a lo largo del proyecto.

## Propuesta de Solución

Para llevar a cabo la solución al problema planteado en la introducción, se propone el desarrollo de una aplicación Web moderna y eficiente con el fin de brindar una buena experiencia de usuario. Para conseguir esto se plantea la creación de una [SPA](#SPA) con una arquitectura [MVC](#MVC) teniendo un foco en la usabilidad. A continuación, se detallarán mejor todos estos puntos.

### Tecnología SPA

Los [SPA](#SPA), como se detalla en el capítulo anterior y señala BasuMallick en @ventajas-spa, ofrecen la ventaja crucial de posibilitar la interacción del usuario sin tener que recargar la página. Esta característica contribuye de manera significativa a la reducción del tiempo de carga, lo que, a su vez, se traduce en una mejora sustancial en la velocidad de la aplicación. Al prescindir de la recarga de la página, como se ilustra en la Figura \ref{capitulo3:flujo-spa}, solo es necesario intercambiar datos, mientras que recursos fundamentales como [HTML](#HTML) y [CSS](#CSS) se cargan de manera única al inicio.

![Flujo de una [SPA](#SPA)\label{capitulo3:flujo-spa}](flujo-spa.png){width=50%}

Además, los [SPA](#SPA) pueden incorporar las funcionalidades de los [PWA](#PWA), permitiendo su uso incluso cuando no hay conexión a internet. Esto lo consiguen los [SPA](#SPA) enviando una única petición al servidor, para luego guardar y almacenar lo que recibe en el caché, permitiendo sincronizar los datos sel servidor cuando la conexión lo permita.

Asimismo, los [SPA](#SPA) permiten crear aplicaciones Web con una compatibilidad multiplataforma, teniendo la posibilidad de utilizar la aplicación en cualquier dispositivo, navegador y sistema operativo. 

Finalmente, con todas estas características se puede concluir que los [SPA](#SPA) mejoran significativamente la experiencia del usuario gracias a la velocidad, la posibilidad de utilizarla offline y en cualquier dispositivo. Para la creación de dicha aplicación, se propone también el uso de una arquitectura [MVC](#MVC), la cual será detallada en el siguiente punto.

### Arquitectura MVC

Con una arquitectura [MVC](#MVC), tal y como explica Hernández en @arquitectura-mvc, se conseguirá fortalecer la robustez y escalabilidad de la aplicación, al dividir el código en tres componentes principales, cada uno con responsabilidades específicas, lo que facilita la organización, el mantenimiento y la expansión esenciales en una aplicación moderna y eficiente. Estos tres componentes consisten en: Modelo, Vista y Controlador.

1. **Modelo:** Encargado de gestionar los datos y la lógica. En el contexto de la aplicación de diagnóstico de fibromialgia, el Modelo podría ser responsable de la manipulación de datos relacionados con los pacientes, resultados de diagnóstico y cualquier información relevante para el proceso de evaluación médica.
2. **Vista:** Representa la interfaz de usuario y se encarga de la presentación de datos. La Vista en este caso sería responsable de mostrar al usuario la información relevante de manera clara y comprensible, teniendo un gran enfoque en la usabilidad.
3. **Controlador:** Gestiona la interacción del usuario y actúa como intermediario entre el Modelo y la Vista. El Controlador sería responsable de procesar las acciones del usuario, actualizar el Modelo según sea necesario y coordinar la presentación actualizada a través de la Vista.

Esta división clara de responsabilidades, que se puede ver en la Figura \ref{capitulo3:arquitectura-mvc}, no solo facilita el desarrollo y la mantenibilidad del código, sino que también proporciona una base sólida para futuras expansiones y mejoras en la aplicación.

![Arquitectura [MVC](#MVC)\label{capitulo3:arquitectura-mvc}](arquitectura-mvc.png){width=75%}

En adicción al uso de esta arquitectura para la escalabilidad de la aplicación, se plantea la elección de una **base de datos no relacional**, ya que estas ofrecen ventajas significativas en términos de flexibilidad y capacidad para manejar grandes volúmenes de datos.

Por último, en el siguiente punto se detallará la propuesta de un enfoque en la usabilidad con el objetivo de dar una gran experiencia al usuario final.

### Usabilidad

Diseñar una interfaz intuitiva y usable que responda a las necesidades del usuario final, haciendo que sea tanto fácil de utilizar como de aprender, es esencial en una aplicación Web que quiera brindar una gran experiencia de usuario.

La creación de una interfaz intuitiva implica la adopción de elementos visuales y de diseño que reflejen la lógica y el flujo de trabajo esperado por el usuario. Se busca minimizar la curva de aprendizaje, permitiendo que tanto profesionales de la salud como pacientes puedan interactuar de manera natural con la aplicación desde el primer momento. La disposición lógica de los elementos, la claridad en las indicaciones y la consistencia en el diseño contribuirán a una experiencia de usuario sin complicaciones.

En paralelo, se plantea la implementación de un **diseño responsive** que se adapte fluidamente a diversos tamaños de pantalla. Después de todo, la gran variabilidad de dispositivos que existen, como ordenadores, tablets y teléfonos móviles, requiere que la interfaz sea flexible y se ajuste de manera óptima a cada contexto. Esta adaptabilidad no solo mejora la accesibilidad, sino que también proporciona una experiencia consistente y agradable independientemente del dispositivo utilizado.

En resumen, con una interfaz usable, tecnología [SPA](#SPA) y arquitectura [MVC](#MVC) se asegura que la aplicación sea moderna y eficiente, ofreciendo una buena experiencia al usuario. No obstante, para lograr la implementación exitosa de dicha aplicación Web, es esencial seguir una metodología de desarrollo adecuada, la cual se detallará en el próximo punto.

## Metodología de Desarrollo

En el contexto de la metodología de desarrollo a seguir, se ha optado por adoptar la metodología ágil, específicamente Scrum. En este apartado, se proporcionará una justificación exhaustiva de la elección de Scrum como marco de trabajo. Además, se explorará el flujo de trabajo característico de esta metodología, y se detallarán las adaptaciones específicas realizadas para asegurar la alineación con los objetivos y características particulares del proyecto.

### Justificación 

Para justificar la elección de la metodología de Scrum, es esencial conocer en primer lugar la decisión de adoptar una metodología ágil para el desarrollo de la aplicación Web. Esta elección se fundamenta principalmente en tres razones: flexibilidad ante cambios, entregas continuas y una colaboración activa con el cliente. A continuación, se detallan cada una de estas razones. 

1. **Flexibilidad ante cambios:** Los proyectos de desarrollo de aplicaciones Web a menudo enfrentan cambios en los requisitos del cliente. Las metodologías ágiles están diseñadas para adaptarse fácilmente a cambios, permitiendo una respuesta rápida y eficiente a las necesidades cambiantes a lo largo del ciclo de vida del proyecto.
2. **Entregas iterativas y continuas:** Las metodologías ágiles promueven entregas iterativas y continuas de incrementos de software funcional. En el contexto de una aplicación Web, esto significa que se pueden entregar funcionalidades tangibles en intervalos cortos, lo que facilita la obtención de retroalimentación temprana y la posibilidad de ajustar el enfoque según las necesidades cambiantes del usuario.
3. **Colaboración activa con el cliente:** La interacción continua con el cliente es un pilar fundamental de las metodologías ágiles. En el desarrollo de aplicaciones Web, donde la experiencia del usuario es crucial, la colaboración directa con el cliente asegura una comprensión precisa de sus expectativas y permite ajustes rápidos para garantizar la satisfacción del usuario final.

Sin embargo, como se ha mencionado previamente, dentro de las metodologías ágiles, la elección específica ha sido Scrum. A continuación, se detallan las razones principales para elegir dicha metodología. 

1. **Roles claros y definidos:** Scrum define roles específicos como el Scrum Master, Product Owner y Desarrolladores, proporcionando claridad en las responsabilidades y contribuyendo a una gestión eficaz del proyecto.
2. **Estructura de Sprints:** La división del proyecto en Sprints permite entregas incrementales regulares, lo cual es beneficioso en el desarrollo Web para mantener un ritmo constante de desarrollo y despliegue de funcionalidades.
3. **Foco en la colaboración:** Scrum promueve la colaboración continua entre los miembros del equipo y el cliente, facilitando la resolución rápida de problemas y la adaptación a los cambios de manera conjunta.
4. **Gestión efectiva de los requisitos:** La gestión del [PB](#PB) en Scrum permite la priorización y adaptación de los requisitos, especialmente importante en el desarrollo Web, donde la variedad de funcionalidades puede ser extensa.
5. **Mejora continua a través de la retroalimentación:** Los eventos de revisión y retrospectiva en Scrum proporcionan oportunidades cruciales para la mejora continua, permitiendo ajustar enfoques y procesos según la retroalimentación del equipo y del cliente.

En conclusión, la elección de Scrum como metodología ágil para el desarrollo de la aplicación Web se fundamenta en sus principios sólidos, su enfoque estructurado y su capacidad para adaptarse a las complejidades del desarrollo de software en el entorno dinámico de la Web. 

Una vez se conoce la justificación de la elección de Scrum, es esencial conocer exactamente cómo es el flujo de dicha metodología, lo cual se explicará en el siguiente punto.

### Scrum

Scrum se destaca como una metodología ágil que brinda apoyo a individuos y equipos en la creación de soluciones adaptables para desafíos complejos. Su implementación eficaz demanda la colaboración de un equipo compacto, típicamente compuesto por 10 personas o menos. Este equipo se distingue por su estructura no jerárquica, su versatilidad multifuncional y su capacidad de autogestión. En este contexto, Scrum define tres roles específicos, cada uno desempeñando una función crucial: Desarrolladores, Product Owner y Scrum Master.

1. **Desarrolladores:** Este grupo asume la responsabilidad de llevar a cabo el desarrollo del producto, transformando elementos de la lista de requisitos en incrementos funcionales del software. 
2. **Product Owner:** Representa a todas las partes interesadas del producto y se encarga de maximizar su valor para clientes, usuarios y demás involucrados. Su enfoque se centra en la toma de decisiones orientada a los objetivos.
3. **Scrum Master:** Juega un papel vital en garantizar el correcto funcionamiento de la metodología Scrum. Facilita la comprensión de la teoría y práctica de Scrum tanto dentro del equipo como en toda la organización. Además, se esfuerza por eliminar obstáculos y fomentar un entorno favorable para la colaboración y mejora continua.

Esta estructura de roles en Scrum establece un equilibrio que promueve la eficiencia, la flexibilidad y la adaptabilidad, elementos clave para abordar la complejidad de los proyectos de desarrollo de software. No obstante, Scrum no se limita únicamente a roles específicos, sino que también incorpora una serie de eventos que tienen lugar en cada iteración, la cual es comúnmente llamada Sprint.

El **Sprint** funciona como un contenedor que abarca los distintos eventos, con una duración preestablecida de un mes o menos. Tan pronto como concluye un Sprint, el siguiente comienza de inmediato. Dichos eventos están diseñados para fomentar la colaboración y la transparencia, y desempeñan un papel esencial en el éxito de la metodología Scrum. Los eventos clave en Scrum incluyen: Planificación del Sprint, Scrum Diario, Revisión del Sprint y Retrospectiva del Sprint.

1. **Planificación del Sprint:** En este evento, el equipo define el trabajo a realizar durante el próximo Sprint. Se seleccionan elementos del [PB](#PB) para abordar en el Sprint y se establece un objetivo claro.
2. **Scrum Diario:** Este evento diario brinda la oportunidad a los miembros del equipo para sincronizar sus actividades, compartir actualizaciones sobre su progreso, identificar posibles obstáculos y ajustar la planificación según sea necesario.
3. **Revisión del Sprint:** Al final de cada Sprint, el equipo presenta el trabajo completado al Product Owner y otros interesados. Se obtiene retroalimentación y se ajustan las prioridades para el próximo Sprint.
4. **Retrospectiva del Sprint:** Después de la revisión del Sprint, el equipo reflexiona sobre su desempeño, identifica áreas de mejora y establece acciones para implementar en el próximo Sprint con el fin de mejorar la calidad y la eficacia.

Estos eventos proporcionan un marco temporal y oportunidades para la colaboración, asegurando que el equipo se adapte continuamente y entregue valor de manera consistente. La interacción entre los miembros del equipo y la participación activa en estos eventos son esenciales para un correcto flujo de trabajo en Scrum.

Finalmente, el equipo también interactúa con diferentes artefactos en el contexto de Scrum. Estos artefactos proporcionan transparencia y visibilidad sobre el trabajo realizado, el trabajo por hacer y el estado general del proyecto. Los principales artefactos en Scrum son: Product Backlog, Sprint Backlog, Incremento.

1. **Product Backlog:** Esta lista priorizada de elementos describe las funcionalidades, mejoras y correcciones deseadas para el producto. Los desarrolladores junto con la ayuda del Product Owner son responsables de gestionar y priorizar este backlog, asegurándose de que siempre refleje las necesidades más importantes del cliente y del negocio.
2. **Sprint Backlog:** Durante la planificación del Sprint, el equipo selecciona elementos del [PB](#PB) para abordar en el Sprint. Estos elementos se trasladan al [SB](#SB), que sirve como una lista detallada de las tareas que el equipo planea completar durante el Sprint.
3. **Incremento:** Este es el resultado del trabajo del equipo al final de cada Sprint. Es un producto potencialmente entregable que incluye todas las funcionalidades completadas durante el Sprint.

Estos artefactos proporcionan una representación clara de las metas y el progreso del equipo. La interacción efectiva con estos elementos asegura una comprensión compartida de las prioridades y una adaptabilidad continua durante el desarrollo del producto en el marco de Scrum.

La información presentada anteriormente se ha obtenido de "La Guía de Scrum" @scrum-guide por Schwaber y Sutherland. En conclusión, la interacción de todos estos elementos en la metodología Scrum se ilustra en la figura \ref{capitulo3:scrum}. Comienza con la reunión de planificación, en la que participan todos los roles, marcando así el inicio del Sprint. Este Sprint tiene una duración máxima de 4 semanas y se acompaña de reuniones diarias realizadas por el equipo de desarrollo. Durante el Sprint, se llevan a cabo las tareas del [SB](#SB), seleccionadas previamente del [PB](#PB), y culminan en un incremento al final del Sprint. A continuación, se llevan a cabo la reunión de revisión y la retrospectiva, nuevamente con la participación de todo el equipo Scrum.

![Flujo de la metodología Scrum @imagen-scrum\label{capitulo3:scrum}](scrum.png)

No obstante, para la ejecución de este proyecto, ha sido esencial realizar adaptaciones específicas de la metodología, las cuales se detallan en el siguiente apartado.

### Adaptación

Como se ha expuesto anteriormente, Scrum proporciona una estructura bien definida con roles específicos, eventos y artefactos; no obstante, su flexibilidad permite adaptaciones según las particularidades de cada proyecto. En el caso de este proyecto, se enfrenta a limitaciones y condiciones específicas que han influido en la configuración tradicional de Scrum.

Por un lado, una consideración clave radica en la **reducida composición del equipo**, conformado exclusivamente por el autor del proyecto y los dos tutores. Ante esta restricción, se han realizado ajustes en la asignación de roles:

- El equipo de desarrollo estará compuesto únicamente por un desarrollador, en este caso, el propio autor del proyecto.
- Los roles de Scrum Master y Product Owner se han asignado a ambos tutores, quienes desempeñarán estas funciones de manera colaborativa.

Por otro lado, otra consideración del proyecto es la **limitación de disponibilidad diaria**, la cual impide la realización de las reuniones diarias. Sin embargo, a pesar de esta baja disponibilidad, las reuniones de planificación, revisión y retrospectiva sí serán realizadas, llevándose a cabo en el mismo día.

Estas adaptaciones han sido cuidadosamente diseñadas para mantener la integridad del marco de trabajo Scrum mientras se ajusta a las circunstancias particulares del proyecto. Aunque las modificaciones se han realizado por necesidad, se busca preservar los principios fundamentales de Scrum, como la transparencia, la inspección y la adaptación, para lograr un desarrollo efectivo y un producto final de alta calidad.

Una vez se conoce la metodología que guiará el desarrollo del proyecto, resulta esencial conocer las herramientas que serán utilizadas durante el mismo. Estas herramientas serán expuestas en la siguiente sección.

## Herramientas

Existe una amplia variedad de herramientas disponibles para facilitar el desarrollo de un proyecto. A continuación, se detallarán las distintas herramientas que se emplean en este proyecto, organizadas en tres categorías principales: gestión de proyectos, documentación y desarrollo.

### Gestión de Proyecto

En el ámbito de la gestión de proyectos, se han seleccionado las siguientes herramientas:

- **Planificación del proyecto:** GitHub Projects y Excel @excel
- **Comunicación y reuniones:** Outlook @outlook, Microsoft Teams @teams y OneDrive @onedrive
- **Control de versiones:** Git @git y GitHub @github

Para la planificación detallada del proyecto, se implementará GitHub Projects, una herramienta que simplifica la creación de tableros adaptados al flujo de trabajo de la metodología Scrum, detallada previamente. Esta plataforma será complementada con el uso de Excel, aplicación de hojas de cálculo proporcionada por *Microsoft*, la cual será utilizada para la creación de los diferentes [BC](#BC) destinados a evaluar el trabajo realizado en cada sprint. 

Específicamente, se utilizará la plantilla diseñada siguiendo los pasos expuestos por Swam en @plantilla-bc. La representación visual de esta plantilla se muestra en la Figura \ref{capitulo3:plantilla-bc}, la cual consiste en una tabla que incluye fechas, el peso planificado de las [HU](#HU) a realizar cada día, el peso real de las [HU](#HU) completadas diariamente y el peso "quemado" en relación con el peso total del Sprint.

![Plantilla para la creación del [BC](#BC)\label{capitulo3:plantilla-bc}](plantilla-bc.png){width=75%}

En términos de comunicación y reuniones entre los miembros del equipo, se aprovechará el entorno proporcionado por *Microsoft*. Esto incluye el uso de Outlook para el envío de correos electrónicos, Microsoft Teams para facilitar reuniones virtuales y OneDrive para la compartición de archivos.

Finalmente, para gestionar el control de versiones tanto de la documentación como de la aplicación Web, se empleará Git junto con GitHub. En esta última, se creará una organización, la cual estará configurada con los distintos miembros del equipo, permitiendo la gestión de repositorios, así como del proyecto a través de la herramienta GitHub Projects mencionada anteriormente.

En conjunto, todas estas herramientas permitirán tener una gestión del proyecto adecuada desde la fase de planificación hasta el despliegue. No obstante, el éxito en el desarrollo de un proyecto no solo depende del uso adecuado de herramientas para gestionarlo, sino también de la correcta documentación. A continuación, en la siguiente sección, se detallarán las herramientas específicas utilizadas para documentar de manera efectiva cada aspecto del proyecto.

### Documentación

En lo que respecta a las herramientas destinadas a la documentación del proyecto, se han seleccionado las siguientes:

- **Lenguaje de marcado:** Markdown
- **Editor de texto:** Typora @typora
- **Generación de memoria:** Plantilla de Félix Albertos @plantilla-felix
- **Diagramas:** Diagrams.net @diagramsnet 
- **Diseño de interfaces:** Excalidraw @excalidraw y Figma @figma

Por un lado, la documentación se redacta utilizando el lenguaje de marcado Markdown, que simplifica la aplicación de formato a un texto plano mediante caracteres especiales. Para esta tarea, se utiliza el editor Typora, elegido por su experiencia de escritura sin distracciones y su fácil manejo. En cuanto a la generación de la memoria final con el formato adecuado, se emplea la plantilla proporcionada por el tutor Félix Albertos. Esta plantilla, diseñada específicamente para la elaboración del [TFG](#TFG), elimina las posibles preocupaciones de formato al utilizar Markdown como entrada.

Por otro lado, en el caso de necesitar desarrollar diagramas, se recurrirá a Diagrams.net. Finalmente, para el diseño de las interfaces a implementar, se utilizará Excalidraw para bocetos con pocos detalles y Figma para diseños más elaborados.

Con la combinación de todas estas herramientas se conseguirá crear un flujo de trabajo documental eficiente y versátil, optimizando la redacción, formato, generación de memoria y diseño de interfaces en el proyecto. Sin embargo, una vez se han presentado las herramientas destinadas a la documentación, es esencial pasar a detallar las distintas herramientas específicas utilizadas en el desarrollo del proyecto.

### Desarrollo

Dentro de las herramientas de desarrollo, se contemplan las que se enumeran a continuación, agrupadas en tres categorías: FrontEnd, BackEnd y Otras.

- **FrontEnd**
  - **Lenguaje de marcado:** HTML
  - **Lenguaje de diseño gráfico:** CSS
  - **Lenguaje de programación:** TypeScript @typescript
  - **Framework:** React @react
  - **Herramienta:** Vite @vite
  - **Librería destacada:** D3.js @d3js
- **BackEnd**
  - **Lenguaje de programación:** TypeScript @typescript
  - **Entorno de desarrollo:** Node.js @nodejs
  - **Framework:** Express.js @expressjs
  - **Base de datos:** MongoDB @mongodb
  - **Librerías destacadas:** Mongoose @mongoose
- **Otras**
  - **Editor de código:** Visual Studio Code @vscode
  - **Gestor de paquetes:** pnpm @pnpm


Estas herramientas han sido seleccionadas cuidadosamente con el objetivo de implementar el stack MERN utilizando TypeScript como lenguaje central. El propósito es lograr el desarrollo de una aplicación web moderna y eficiente que abarque tanto el lado del cliente como el del servidor. A continuación, se detallan a fondo cada una de estas tecnologías.

En el FrontEnd, se ha optado por tecnologías líderes en la industria, como [HTML](#HTML), [CSS](#CSS), TypeScript y React. Estas elecciones proporcionan una estructura sólida para la creación de interfaces de usuario dinámicas y atractivas. Además, se ha incorporado Vite como herramienta de construcción, ofreciendo un entorno de desarrollo rápido y liviano que contribuye a la eficiencia del proceso de desarrollo. Finalmente, en el lado del cliente, se resalta la elección de la librería D3.js para la visualización de datos.

En el BackEnd, se repite la elección de TypeScript dentro del entorno de Node.js. Este último será respaldado por Express.js como framework, proporcionando un entorno ágil y escalable para la gestión eficiente de las operaciones del servidor. El stack MERN se solidifica al optar por MongoDB como base de datos, destacándose por su capacidad de almacenamiento flexible y escalable. La interfaz con esta base de datos se simplifica mediante el uso de la librería Mongoose, facilitando el acceso y la manipulación de los datos de manera eficaz.

Finalmente, se destaca la elección de Visual Studio Code como editor de código debido a su popularidad, extensibilidad y potentes características que mejoran la productividad del desarrollador. Además, se utilizará pnpm como gestor de paquetes, el cual añade eficiencia a la gestión de dependencias, facilitando la instalación y actualización de bibliotecas y herramientas de manera más rápida y consistente.

En conclusión, la selección de estas herramientas se alinea con el objetivo de desarrollar una aplicación Web moderna, eficiente y atractiva para el usuario. Todas estas tecnologías están interrelacionadas, como se ilustra en la Figura \ref{capitulo3:arquitectura-tecnologica}. Esta figura no solo presenta la implementación de la arquitectura [MVC](#MVC) previamente mencionada, sino que también muestra una clara división en tres secciones: Cliente, Servidor y Base de Datos.

- **Cliente:** En la sección del cliente, se incorpora toda la tecnología presentada anteriormente en el FrontEnd. Además, esta sección representa la Vista en la arquitectura [MVC](#MVC).
- **Servidor:** En esta sección, se observa la mayoría de la tecnología presentada en el BackEnd. Además, esta sección contiene tanto el Controlador, el cual sería la API utilizando el framework Express, como el Modelo utilizando la librería Mongoose.
- **Base de Datos:** Aquí se destaca el uso de la base de datos no relacional MongoDB, que sirve como el componente clave para el almacenamiento de datos.

![Arquitectura tecnológica\label{capitulo3:arquitectura-tecnologica}](arquitectura-tecnologica.png){width=40%}

Una vez que se ha presentado las diversas herramientas que se utilizarán en el proyecto, junto con la metodología y la propuesta de solución, en el próximo capítulo se explicará el resultado final de la aplicación Web.