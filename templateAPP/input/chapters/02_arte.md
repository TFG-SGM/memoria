# Estado del Arte
En el contexto del desarrollo de una aplicación Web, es esencial considerar diversos factores, incluyendo la metodología de desarrollo, las herramientas y tecnologías disponibles y la usabilidad de la aplicación. A continuación, es realizado un análisis que abarca todas estas áreas con el propósito de determinar las mejoras prácticas y enfoques para implementar durante el proyecto. 

## Metodologías de Desarrollo Software
Para que un software, como es una aplicación Web, llegue a producción debe pasar por un proceso de desarrollo de software, conocido también como “ciclo de vida del desarrollo del software”. A su vez, para organizar este ciclo es necesario utilizar cierta metodología de desarrollo. En este apartado es realizado un análisis de las distintas fases de dicho proceso, además de las metodologías más destacadas.

### Ciclo de Vida del Desarrollo del Software
El ciclo de vida del desarrollo de software es un proceso estructurado que abarca desde la concepción de un proyecto hasta su despliegue y mantenimiento. A lo largo de este ciclo, se llevan a cabo una serie de fases y actividades. Cada fase del ciclo de vida del desarrollo de software tiene sus propios objetivos y entregables específicos. Este normalmente está dividido en las siguientes fases @ciclo-vida-desarrollo-software: 

- **Planificación y análisis:** se elabora un plan que describe en detalle cómo se dará vida al proyecto desde la idea hasta la realización.
- **Definición de requisitos:** se recopilan los diferentes requisitos para la aplicación final.
- **Diseño:** se elabora un documento de diseño de software que incluye el diseño del sistema, los lenguajes de programación, las plantillas, la plataforma a utilizar y las medidas de seguridad de la aplicación.
- **Desarrollo:** se transforman los requisitos en código para desarrollar la propia aplicación.
- **Pruebas:** se realizan pruebas de validación para asegurar que esté funcionando correctamente y haga lo que debe hacer.
- **Despliegue:** se entrega al usuario final.
- **Mantenimiento:** se arreglan los diferentes errores que encuentren los usuarios, teniendo que volver a la primera fase del ciclo si fuera necesario.

Una vez se conoce el ciclo de desarrollo, es esencial saber cómo organizar el mismo. Para ello, en el siguiente punto se analizan las diferentes metodologías de desarrollo.

### Metodologías de Desarrollo
Para organizar cada una de las fases, como se ha mencionado previamente, es necesario implementar una metodología de desarrollo, con el fin de aumentar la productividad y la calidad del software. A continuación, se detallan algunas de las metodologías más destacadas @metodologias-desarrollo.

- **Cascada:** se trata de una de las metodologías más antiguas. En este caso, las fases de desarrollo se realizan de una manera secuencial, es decir, una fase comienza solo cuando termina la fase anterior. Aunque esto hace que la estructura sea más clara y fácil de entender, tiene la desventaja de ser poco flexible y adaptable a los cambios de los requisitos, que tan a menudo se ve en un desarrollo de software. 
- **Iterativa:** esta metodología divide el proyecto en pequeñas partes, y cada parte es desarrollada, probada e implementada de manera iterativa. Cada una de estas iteraciones agrega funcionalidad al software.
- **En V:** en esta metodología se relaciona cada fase de desarrollo con su fase de pruebas correspondiente. De esta manera, pone un gran énfasis en la validación temprana de requisitos y la calidad del software. No obstante, similar a la metodología en cascada, su enfoque lineal puede resultar inflexible frente a cambios en los requisitos.
- **Espiral:** se trata de una metodología que mezcla los elementos de la planificación en cascada con la flexibilidad de las metodologías ágiles. Utiliza ciclos repetitivos incluyendo planificación, evaluación de riesgos, ingeniería y evaluación del cliente. Aunque es bastante efectivo en la gestión de riesgos, puede acabar resultando muy complejo de gestionar, además de requerir más tiempo y recursos que otras metodologías. 
- **Big bang:** esta metodología tiene un enfoque único en el que los desarrolladores se lanzan directamente a la codificación sin mucha planificación. Esto significa que los requisitos se implementan a medida que aparecen, es decir, sin ningún tipo de hoja de ruta clara. Sin embargo, a la hora de necesitar realizar algún cambio, puede llegar a requerir una renovación completa del software.
- **Ágil:** esta metodología organiza las fases del ciclo de vida en varios ciclos de desarrollo, de forma que el equipo realiza pequeños cambios de software incrementales en cada uno de estos ciclos. Esto lo hace ideal para proyectos de desarrollo de software que requieran flexibilidad y capacidad de adaptarse a los cambios con el tiempo.

Al final, la elección de la metodología de desarrollo de software es esencial para el éxito del proyecto y debe ajustarse a las particularidades del mismo. Cada enfoque tiene sus propias fortalezas y debilidades. Sin embargo, la metodología ágil puede ser la que más destaque para el desarrollo de software debido a su agilidad, ciclos cortos de desarrollo y capacidad para adaptarse a cambios en los requisitos. En el siguiente punto, se analizará algunas de las metodologías ágiles más utilizadas en la actualidad.

### Metodologías Ágiles
Como ya se ha mencionado las metodologías ágiles son las que más destacan en la actualidad debido a su flexibilidad para adaptarse a los cambios. A continuación, son analizadas tres de las más populares @metodologias-agiles:

- **Extreme programming:** consiste en una metodología ágil que se centra en la mejora continua y la respuesta rápida a los cambios en los requisitos. Para ello, pone énfasis en la retroalimentación constante y la comunicación abierta, destacando prácticas como la programación en parejas, pruebas unitarias continuas y entregas frecuentes. 
- **Kanban:** con origen en la manufactura, esta metodología ágil se ha conseguido aplicar con éxito al desarrollo de software. Se basa principalmente en la visualización del flujo de trabajo mediante el uso de tableros Kanban, representando cada tarea mediante tarjetas que se mueven a través de columnas que representan diferentes estados del proceso. A pesar de la mejora continua y flexibilidad que ofrece, se puede notar la ausencia de una estructura para roles y eventos, lo que dificulta la gestión de proyectos más grandes.
- **Scrum:** muy conocido y usado en la actualidad. En Scrum, los ciclos de desarrollo se llaman “sprints”, que generalmente duran entre dos y cuatro semanas. Además, utiliza roles definidos claramente como el Scrum Master, el Product Owner y el equipo de desarrollo. También, se enfoca en la entrega iterativa de incrementos de software y gracias a su énfasis en la comunicación constante y adaptabilidad al cambio se ha convertido en una elección popular en el desarrollo de proyectos software, como es el caso de la implementación de una aplicación Web. En la figura \ref{capitulo2:scrum} se puede observar el flujo de esta popular metodología.

![Flujo de la metodología Scrum\label{capitulo2:scrum}](scrum.png)

Nuevamente, la elección de la metodología dependerá de las características del proyecto. Siendo en este caso, Scrum la que más destaca entre todas ellas. Sin embargo, una vez se conoce el proceso y las diferentes metodologías del desarrollo de software, es esencial conocer la tecnología Web que se puede utilizar para el desarrollo de dicho software, la cual se detalla en el siguiente punto.

## Tecnología Web
En el proceso de implementación de una aplicación Web, resulta esencial no solo seguir una metodología específica, sino también utilizar las diversa tecnología Web disponible. Este campo de estudio abarca un extenso conjunto de herramientas, estándares y prácticas que han sido utilizados en el desarrollo, implementación y mantenimiento de aplicaciones y sitios Web. Desde los aspectos del lado del cliente hasta los del servidor, este panorama tecnológico tiene como objetivo primordial mejorar la experiencia del usuario y optimizar la eficiencia en el desarrollo. A continuación, se profundiza en todas estas áreas.

### BackEnd
En el ámbito del desarrollo BackEnd, se puede encontrar un ecosistema diverso de lenguajes de programación, cada uno acompañado de sus propios frameworks. Este panorama se enriquece aún más con la presencia crucial de bases de datos y la adopción generalizada de contenedores. En este análisis, se explora detenidamente cada una de estas áreas tecnológicas.

Por un lado, los lenguajes de programación, los cuales desempeñan un papel crucial, definiendo la estructura y el rendimiento de las aplicaciones. Se destacan principalmente cuatro lenguajes @tecnologia-backend: JavaScript, Python, Ruby y PHP.

- **JavaScript:** se trata de un lenguaje de programación versátil y ampliamente utilizado que funciona tanto en el lado del cliente como en el lado del servidor. En el contexto del desarrollo del lado del servidor, se emplea en el entorno de ejecución Node.js, que utiliza el motor V8 de Google Chrome. JavaScript es destacado por su capacidad para manejar operaciones de entrada/salida de manera eficiente y su naturaleza asíncrona, lo que lo hace ideal para aplicaciones escalables y basadas en eventos, como aplicaciones Web en tiempo real.
- **Python:** consiste en un lenguaje versátil y de alto nivel que enfatiza la legibilidad del código y la productividad del programador. Con una sintaxis clara y concisa, Python es utilizado en una amplia gama de aplicaciones, desde desarrollo Web hasta inteligencia artificial y análisis de datos. 
- **Ruby:** es conocido por su elegancia y simplicidad, priorizando la productividad del desarrollador. Aunque es menos ubicuo que otros lenguajes, ha ganado popularidad gracias a su enfoque en la facilidad de uso y la creación de código conciso y expresivo.
- **PHP:** se trata de un lenguaje de scripting especialmente diseñado para el desarrollo Web. Ampliamente utilizado para construir aplicaciones Web dinámicas, PHP se integra fácilmente con HTML y se ejecuta en el lado del servidor.

Estos lenguajes, aunque poderosos por sí mismos, se ven potenciados cuando se combinan con frameworks específicos. Cada uno de los mencionados tiene su conjunto de frameworks que agilizan y estructuran el proceso de desarrollo. A continuación, se explora un framework representativo para cada uno de estos lenguajes respectivamente @tecnologia-backend: Express, Django, Ruby on Rails y Laravel.

- **Express:** es un framework para Node.js que simplifica el desarrollo de aplicaciones Web y APIs. Con un enfoque minimalista, permite la creación rápida de servidores y rutas, facilitando la construcción de aplicaciones robustas con JavaScript del lado del servidor.
- **Django:** es un framework de alto nivel para Python, diseñado para maximizar la eficiencia y la reutilización del código. Con un conjunto integrado de herramientas y una arquitectura basada en el patrón de diseño Modelo-Vista-Controlador (MVC), Django simplifica la creación de aplicaciones Web complejas al proporcionar una estructura organizativa y características como la administración automática de bases de datos.
- **Ruby on Rails:** es un framework que sigue el principio de convención sobre configuración para el desarrollo rápido de aplicaciones Web en Ruby. Facilita la creación de aplicaciones mediante la automatización de tareas repetitivas y la adopción de convenciones predefinidas. Rails proporciona un entorno coherente que acelera el proceso de desarrollo y favorece la escritura de código limpio y conciso.
- **Laravel:** es un framework elegante y completo para PHP que aborda diversos aspectos del desarrollo Web. Ofrece una sintaxis expresiva, una gestión eficiente de bases de datos, y una amplia gama de herramientas para tareas comunes. Laravel fomenta la creación de aplicaciones seguras y modernas, con un énfasis en la legibilidad y mantenimiento del código.

Por otro lado, en el contexto del desarrollo del lado del servidor es esencial considerar no sólo los lenguajes de programación y sus frameworks asociados, sino también las bases de datos, los cuales son elementos fundamentales para la persistencia y gestión de datos. Para una comprensión más detallada, se examinan dos bases de datos específicas: MongoDB y MySQL.

- **MongoDB:** destaca como una base de datos NoSQL orientada a documentos, ofreciendo flexibilidad en el esquema y una capacidad eficaz para manejar grandes volúmenes de datos no estructurados. Esta característica la convierte en una elección popular para aplicaciones que requieren escalabilidad y adaptabilidad a cambios en la estructura de datos.
- **MySQL:** al contrario que MongoDB se trata de una base de datos relacional, reconocida por su fiabilidad y consistencia en la gestión de datos estructurados. Ha sido una opción de confianza en el desarrollo Web, proporcionando un entorno robusto para aplicaciones que dependen de una estructura de datos clara y relaciones definidas.

Finalmente, en el lado del servidor, no se debe pasar por alto la importancia de los contenedores. A continuación, se analizan dos tecnologías destacadas @tendencias-tecnologias-web: Docker y Kubernetes.

- **Docker:** se trata de plataforma de contenedores que posibilita el empaquetado, la distribución y la ejecución coherente de aplicaciones en diversos entornos. Su enfoque revolucionario ha transformado la consistencia y portabilidad en el despliegue de software, permitiendo una gestión eficaz de dependencias y configuraciones.
- **Kubernetes:** consiste en un sistema de orquestación de contenedores, simplificando la administración, escalabilidad y despliegue de aplicaciones contenidas en entornos distribuidos. Su capacidad para coordinar eficientemente la ejecución de contenedores a lo largo de múltiples nodos ha consolidado su posición como una herramienta fundamental en el despliegue de infraestructuras escalables y resilientes. En la figura \ref{capitulo2:docker-y-kubernetes} se puede observar el uso de Kubernetes junto con Docker.

![Flujo de Docker y Kubernetes\label{capitulo2:docker-y-kubernetes}](docker-y-kubernetes.png)

En resumen, la tecnología de BackEnd engloba un conjunto diverso de herramientas y tecnologías esenciales para el desarrollo y funcionamiento de aplicaciones Web y servicios. La elección de tecnologías específicas depende de factores como los requisitos del proyecto, la escala y complejidad de la aplicación, así como las preferencias del equipo de desarrollo. La combinación adecuada de estos elementos contribuye a la creación de sistemas BackEnd robustos, eficientes y escalables. Sin embargo, una vez se conoce el lado del servidor, es vital conocer el otro lado conocido como el FrontEnd, el cual se enfoca más en el cliente. En el siguiente punto, se detalla la diferente tecnología Web dentro de dicha área. 

### FrontEnd
En el ámbito del Frontend, se pueden encontrar diferentes lenguajes tanto de marcado como de programación. Además, destacan los diferentes frameworks, así como de las diferentes librerías de visualización de datos que desempeñan un papel crucial en la construcción de interfaces de usuario atractivas. Tampoco se puede pasar por alto, la creciente popularidad del WebAssembly y las Progressive Web Apps, innovaciones que están transformando la experiencia del usuario dentro del ámbito del FrontEnd. A continuación, se realizará un análisis de estas tecnologías para comprender su impacto y aplicaciones específicas.

Por un lado, los lenguajes de marcado como de programación fundamentales que encontramos en el desarrollo del FrontEnd son la tríada formada de HTML, CSS y JavaScript, este último extendido mediante TypeScript. A continuación, se realiza una breve explicación de cada uno de estos lenguajes.

- **HTML:** lenguaje de marcado estándar utilizado para estructurar el contenido de las páginas Web. Define la jerarquía y organización de los elementos en una página.
- **CSS:** lenguaje de estilo que complementa a HTML. Permite definir el diseño, la presentación y la apariencia visual de los elementos HTML, proporcionando control sobre colores, tipografías y disposición.
- **JavaScript:** se trata del lenguaje de programación del lado del cliente que permite la creación de interactividad en las páginas Web. Es esencial para manipular el DOM (Modelo de Objeto de Documento) y responder a eventos del usuario.
- **TypeScript:** es una extensión de JavaScript que añade un sistema de tipos estático, proporcionando beneficios como la detección temprana de errores y una mejor mantenibilidad en proyectos a gran escala.

Además de estos lenguajes fundamentales, los frameworks de aplicaciones de una sola página (SPA) han revolucionado la forma en que se desarrollan las interfaces de usuario. Estos frameworks permiten la creación de experiencias más dinámicas al cargar solo los componentes necesarios en lugar de recargar toda la página (ver figura \ref{capitulo2:spa}). Aquí se presentan cuatro de dichos frameworks @tendencias-tecnologias-web: React, Angular, Vue y Svelte.

- **React:** desarrollado por Facebook, React es una biblioteca de JavaScript que se centra en la construcción de interfaces de usuario reactivas y eficientes. Su enfoque en la creación de componentes modulares y su capacidad para gestionar el estado de manera efectiva lo convierten en una elección popular para aplicaciones dinámicas y escalables.
- **Angular:** respaldado por Google, es un framework completo de desarrollo que abarca desde la creación de componentes hasta la gestión del estado y el enrutamiento. Su estructura robusta y su integración con TypeScript ofrecen un enfoque amplio para el desarrollo de SPAs, siendo especialmente adecuado para proyectos empresariales complejos.
- **Vue:** se trata de un framework progresivo de JavaScript que destaca por su simplicidad y flexibilidad. Su diseño modular facilita la integración gradual en proyectos existentes, y su curva de aprendizaje suave lo convierte en una opción popular para desarrolladores que buscan una alternativa accesible y potente.
- **Svelte:** adopta un enfoque diferente al trasladar gran parte del trabajo de construcción a tiempo de compilación. Esto resulta en aplicaciones más livianas y rápidas en tiempo de ejecución. Su sintaxis sencilla y su rendimiento eficiente lo hacen atractivo para desarrolladores que buscan una alternativa innovadora y eficaz en la construcción de SPAs.

![Aplicaciones de una sola página vs Aplicaciones Web tradicionales\label{capitulo2:spa}](web-tradicional-vs-spa.png)

Por otro lado, diversas librerías han surgido para facilitar la creación de visualizaciones atractivas e interactivas, después de todo la visualización de datos desempeña un papel fundamental en la comprensión y comunicación efectiva de información en entornos Web. A continuación, son presentadas algunas de las librerías más destacadas @librerias-visualizacion-datos:

- **D3.js:** destaca como una herramienta poderosa para la manipulación basada en datos en documentos . Su capacidad para crear visualizaciones altamente personalizables e interactivas lo convierte en una opción popular para desarrolladores que buscan flexibilidad en la representación gráfica de datos complejos.
- **Chart.js:** aporta una solución simple y fácil de usar, ofreciendo una variedad de gráficos, como barras, líneas y radar. Esta librería en JavaScript permite a los desarrolladores incorporar rápidamente visualizaciones atractivas en sus aplicaciones Web.
- **Highcharts:** con una amplia gama de opciones de personalización, Highcharts simplifica la creación de gráficos interactivos. Esta librería en JavaScript es adecuada para proyectos que buscan una solución robusta y fácil de implementar.
- **Three.js:** aunque inicialmente diseñada para gráficos 3D, Three.js puede ser aprovechada para visualizaciones de datos tridimensionales impactantes. Su capacidad para crear experiencias visuales inmersivas lo convierte en una elección interesante para proyectos ambiciosos.
- **React-Vis:** diseñada específicamente para trabajar con React, React-Vis proporciona componentes listos para usar que facilitan la incorporación de visualizaciones de datos en aplicaciones React. Es una elección eficiente para proyectos que utilizan este marco de trabajo.
- **Material-UI:** basada en el diseño visual de Material Design de Google. Ofrece una amplia variedad de componentes y estilos que facilitan el desarrollo de aplicaciones Web con una apariencia moderna y coherente. Entre estos componentes se pueden encontrar tablas y gráficos.

Por último, dentro del ámbito del FrontEnd destacan dos innovaciones particulares: el WebAssemby y las Progressive Web Apps. Ambas son analizadas más en detalle a continuación @tendencias-tecnologias-web.

- **WebAssembly (Wasm):** permite la ejecución de código de alto rendimiento, escrito en lenguajes como C++ o Rust, directamente en el navegador. Esto amplía significativamente las posibilidades para construir aplicaciones Web más potentes y rápidas, acercando el rendimiento de las aplicaciones Web al de las aplicaciones nativas.
- **Progressive Web Apps (PWA):** ofrecen experiencias avanzadas que combinan lo mejor de las aplicaciones Web y nativas. Su capacidad para funcionar offline permite a los usuarios acceder a contenido incluso en ausencia de conexión a Internet, mejorando la accesibilidad y la continuidad de la experiencia del usuario.

En conclusión, la tecnología del Frontend al igual que el BackEnd abarca un conjunto diverso de herramientas y tecnologías esenciales para la creación y operación de aplicaciones Web y servicios. La selección de tecnologías particulares está condicionada por diversos factores, incluyendo los requisitos específicos del proyecto y la complejidad de la aplicación, así como las preferencias del equipo de desarrollo.

Una vez se conoce la diferente tecnología Web que rodea tanto el lado del BackEnd como el lado del FrontEnd, es de gran ayuda conocer los stacks tecnológicos más utilizados y analizarlos. Lo cual se realizará en el siguiente punto.

### Stacks Tecnológicos
En el contexto de los stacks tecnológicos, es decir, la elección de un conjunto específico de tecnologías, se trata de un aspecto crítico dentro del desarrollo Web, ya que afecta directamente la eficiencia del desarrollo, la escalabilidad y el mantenimiento del sistema. A continuación son explicadas brevemente cuatro stacks @stacks-tecnologicos: LAMP, Python Django, MEAN y MERN.

- **LAMP (Linux, Apache, MySQL, PHP/Python/Perl):** ha sido un pilar en el desarrollo Web durante muchos años y sigue siendo una opción confiable para una variedad de proyectos tradicionales. Linux proporciona el sistema operativo, Apache sirve como servidor Web, MySQL maneja la base de datos, y PHP, Python o Perl actúan como lenguajes de programación del lado del servidor. Este conjunto ofrece estabilidad, flexibilidad y una amplia base de conocimientos, siendo especialmente adecuado para aplicaciones Web convencionales.
- **Python Django (Python, Django, Apache, MySQL):** stack tecnológico compuesto de Python como lenguaje principal de programación, Django como framework Web basado en el patrón MVC, Apache como servidor Web para la gestión de solicitudes HTTP, y MySQL como sistema de gestión de bases de datos. Este conjunto es especialmente adecuado para proyectos Web que buscan la combinación de la versatilidad de Python, la solidez de Django, y la confiabilidad de Apache y MySQL.
- **MEAN (MongoDB, Express.js, Angular, Node.js):** es un stack tecnológico basado completamente en JavaScript. MongoDB es la base de datos NoSQL, Express.js actúa como el framework del lado del servidor, Angular es el framework del lado del cliente y Node.js proporciona el entorno de ejecución del servidor. Este stack ha ganado popularidad por su coherencia en el uso de un solo lenguaje de programación (JavaScript/TypeScript) en todo el flujo de desarrollo, lo que simplifica la colaboración entre los equipos de desarrollo y permite una transición más fluida de los datos entre el servidor y el cliente.
- **MERN (MongoDB, Express.js, React, Node.js):** similar a MEAN, pero reemplaza Angular con React en el lado del cliente. React ha ganado una enorme popularidad por su enfoque declarativo y su capacidad para construir interfaces de usuario altamente interactivas. MERN comparte las ventajas de MEAN, pero además permite a los desarrolladores aprovechar las características distintivas de React para crear experiencias de usuario más dinámicas y eficientes.

| **Stack** | **SO** | **Servidor** | **BD** | **Lenguaje** | **BackEnd** | **FrontEnd** |
|---|:---:|:---:|:---:|:---:|:---:|:---:|
| **LAMP** | Linux | Apache | MySQL | PHP/Python/Perl | - | - |
| **PythonDjango** | - | Apache | MySQL | Python | Django | - |
| **MEAN** | - | - | MongoDB | JavaScript | Express.js | Angular |
| **MERN** | - | - | MongoDB | JavaScript | Express.js | React |

:Comparación de Stacks Tecnológicos\label{capitulo2:comparacion-stacks-tecnologicos}

Con todo esto en mente, se puede concluir que la elección entre los diferentes stacks tecnológicos que existen depende de las necesidades específicas del proyecto y las preferencias del equipo de desarrollo. Teniendo cada stack sus propias ventajas y pudiendo ser la elección correcta según los requisitos particulares de la aplicación que se esté construyendo.

Una vez se conoce toda la tecnología que se puede utilizar a la hora de construir una aplicación Web. Es fundamental, tener en mente las diferentes técnicas de visualización que existen para asegurar que el usuario entienda los datos que se muestran con dicha aplicación. Estas técnicas son analizadas en el siguiente punto. 

## Técnicas de Visualización en la Web
Como se ha mencionado previamente para desarrollar la aplicación Web deseada es necesario mostrar datos de una manera atractiva al usuario y para ello hay que hacer uso de las técnicas existentes de visualización de datos. Al fin y al cabo, esto vendría a ser la traducción de una gran cantidad de información en un contexto visual usando elementos gráficos. De forma que consiga comunicar relaciones de datos complejas para una mejor comprensión de los usuarios. A continuación es realizado un análisis de las diferentes técnicas.

### Tipos de Visualización de Datos
Para conseguir mostrar toda esta cantidad de datos existen diferentes tipos de visualización de datos, algunos de estos son los que se presentan a continuación @tipos-visualizacion-datos.

- **Gráficos de números:** representan inmediatamente un dato clave. 
- **Gráficos de líneas:**  muestran datos a lo largo de una línea continua, conectando puntos de datos. Se utilizan comúnmente para visualizar tendencias a lo largo del tiempo.
- **Mapas:** muestran los datos por una localización geográfica. Normalmente la información se muestra con un mapa de áreas coloreado.
- **Gráfico de cascada:** muestra los datos durante un periodo de tiempo determinado, ilustrando los valores positivos y negativos
- **Gráficos de barras:** representan datos utilizando barras rectangulares de longitudes proporcionales a los valores que representan. Pueden ser horizontales o verticales. Además, pueden mostrar las barras individualmente, acumuladas o agrupadas entre ellas.
- **Gráficos de pastel (pie charts):** dividen un círculo en sectores para representar proporciones. Son útiles para mostrar la distribución porcentual de un conjunto de datos.
- **Gráficos de calibre (gauge charts):** utiliza agujas y colores para mostrar datos similares a la lectura en un velocímetro.
- **Gráficos radiales (radar charts):** muestran datos en un formato circular, útiles para comparar múltiples categorías en función de varias variables.
- **Diagramas de dispersión:** representan puntos en un plano cartesiano para mostrar la relación entre dos variables. Cada punto representa una observación.
- **Tablas:** forma común de visualización de datos que organiza la información en filas y columnas. Cada fila representa un conjunto de datos y cada columna representa un atributo. 
- **Gráficos de burbujas:** similar a un diagrama de dispersión, pero con la adición de un tercer valor que se representa mediante el tamaño de las burbujas.
- **Diagramas de caja (boxplots):** representan la distribución estadística de un conjunto de datos a través de cuartiles. Muestran la mediana, los cuartiles y los valores atípicos.
- **Gráfico de embudo (funnel chart):** muestra como los datos se mueven a través de un proceso específico.
- **Mapas de calor:** utilizan colores para representar la intensidad de un valor en una matriz bidimensional. Son útiles para mostrar la concentración de datos en áreas específicas.

Sin embargo, no solo es necesario conocer qué técnicas existen sino también saber cuales son las mejores prácticas a la hora de utilizarlas. En el siguiente punto, se tratarán estas diferentes prácticas.

### Mejores Prácticas
Existen diferentes prácticas recomendadas que se emplean a la hora de mostrar los datos, entre las que encontramos el uso de la teoría de color, la importancia de la sencillez, el uso de comparaciones, entre otros muchas más. A continuación se analizan más en detalle todas estas prácticas y consejos @practicas-visualizacion-datos.

- **Conocer el caso de uso para cada tipo.** Es de vital importancia tener en mente que cada tipo de visualización de datos es mejor en diferentes situaciones.
- **Evitar mostrar datos que puedan engañar al usuario.** Para ello se aconseja principalmente que los ejes no empiecen por 0 y que tampoco se omitan datos. 
- **Tomar ventaja de la teoría de color.** Al fin y al cabo, los colores no solo ayudan a destacar datos importantes, sino también está demostrado que distintos colores causan distintas emociones a las personas. Además, se pueden aprovechar asociaciones de colores que los usuarios den por hecho, como colores de tonos más claros para valores bajos.
- **Priorizar la sencillez.** Se trata de otra buena práctica para conseguir que el usuario entienda mejor los datos. Evitando muchas etiquetas, imágenes, colores demasiado brillantes, entre otras cosas.
- **Usar los diferentes elementos textuales con cuidado.** Haciendo que los subtítulos sean cortos y contengan las unidades de medida; etiquetas cortas; ordenar la leyenda por orden de aparición; adición de tooltips interactivos para mostrar texto adicional. 
- **Incluir comparaciones.** Presentar dos gráficas juntas que muestren la misma información durante un periodo de tiempo particular proporcionará una guía del impacto de los diferentes datos.
- **Añadir interactividad a los datos.** De esta forma se consigue dar vida a la visualización de datos permitiendo a los usuarios navegar por ellos, a través de filtros y widgets.

Todas estas prácticas, ayudan en gran medida a que el usuario comprenda mejor los datos que se muestran. Sin embargo, otra buena práctica que se recomienda es el uso de los principios de Gestalt, los cuales se detallan mejor en el siguiente punto.

### Principios de Gestalt
Los principios de Gestalt describen cómo los humanos agrupan elementos similares, reconocen patrones y simplifican imágenes complejas cuando se perciben objetos. Los diseñadores utilizan estos principios para organizar el contenido en sitios Web y otras interfaces para que sea estéticamente agradable y fácil de entender. En este punto se tratan los principios @principios-gestalt de simplicidad, proximidad y cierre que pueden ser usados en la visualización de datos. A continuación se detallan cada uno de ellos.

- **Simplicidad:** indica que los elementos gráficos que tengan propiedades visuales compartidas se consideran como parte de un mismo grupo. En la figura \ref{capitlo2:principios-gestalt} se puede ver el uso de similitud de color para indicar dos clases de elementos: los rojos y los grises.
- **Proximidad:** sigue la misma lógica que el anterior, este principio indica que los elementos que estén próximos entre ellos se consideran como un mismo grupo. En la figura \ref{capitlo2:principios-gestalt} se puede ver el uso de este principio.
- **Cierre:** nuevamente sigue la misma lógica anterior, encerrando los elementos en un área. Como se puede ver en la figura \ref{capitlo2:principios-gestalt}, junto a los otros dos principios, este último es el más fuerte visualmente.

![Principios de Gestalt\label{capitlo2:principios-gestalt}](principios-gestalt.png){width=50%}

Los principios que se han presentado aquí solo son tres de los muchos que existen y son aplicados. Sin embargo, con los ejemplos anteriores uno se puede dar cuenta de la gran utilidad que tienen estos principios a la hora de mostrar datos a los usuarios, y poder dar una mejor experiencia de usuario. Concepto el cual se profundizará más en el siguiente punto junto con el concepto de usabilidad.

## Usabilidad 
Por último, para el desarrollo de una aplicación Web enfocada en el lado del cliente es indispensable detenerse para hablar de la disciplina de interacción Persona-Ordenador, de la usabilidad y de la experiencia de usuario. A continuación, se detallan cada uno de estos conceptos. 

### Interacción Persona-Ordenador
La interacción Persona-Ordenador (IPO) es definida como “la disciplina relacionada con el diseño, evaluación e implementación de sistemas informáticos interactivos para el uso de seres humanos, y con el estudio de los fenómenos más importantes con los que está relacionado” @toni-granollers

Dentro de esta disciplina, se pueden encontrar distintos aspectos, los cuales se pueden ver reflejados en la figura \ref{capitlo2:interaccion-persona-ordenador}. Por un lado, se observa una persona con sus características de procesamiento de la información , tanto las de comunicación como las físicas que interactúa con un ordenador. El cual también tiene sus propias características. Por otro lado, en medio se encuentran los dispositivos de entrada y salida que relacionan a la persona con el ordenador, comunicándose mediante diferentes elementos de diseño.

Además la figura, muestra que la persona no está sola sino que realiza el trabajo dentro de una organización social, siendo posible gracias a un proceso de desarrollo en el que cada uno de estos componentes debe ser abordado con igual grado de implicación y no caer en el error de obviar la parte humana, centrándose solamente en la parte tecnológica.

![Flujo de la disciplina de la Interacción Persona-Ordenador\label{capitlo2:interaccion-persona-ordenador}](interaccion-persona-ordenador.png){width=75%}

Con todo esto en mente, se puede decir que la disciplina de interacción Persona-Ordenador es la encargada de estudiar la usabilidad de la aplicación Web. Concepto que se detalla más en profundidad en el siguiente punto.

### Concepto de Usabilidad
El concepto de usabilidad fue introducido por J. Nielsen, quien concluyó que un sistema software tiene dos componentes: el aspecto funcional y la forma en que los usuarios pueden usar este aspecto. Siendo este último, el que es tratado para mejorar la usabilidad de una aplicación. Por consiguiente, los aspectos que se tienen en mente al hablar de usabilidad serían la facilidad de aprendizaje, la efectividad de uso y la satisfacción con las que las personas son capaces de realizar sus tareas.

Teniendo esto en cuenta, la usabilidad se puede definir coloquialmente como “fácil de usar o de utilizar y de aprender” @toni-granollers. Definición que se considera correcta pero incompleta ya que el concepto engloba muchos más aspectos, es por ello que el organismo de estandarización ISO propone dos definiciones:

- La medida en la que un producto se puede usar por determinados usuarios para conseguir objetivos específicos con efectividad, eficiencia y satisfacción en un contexto de uso especificado @toni-granollers.
- La capacidad que tiene un producto software para ser atractivo, entendido, aprendido, usado por el usuario cuando es utilizado bajo unas condiciones específicas @toni-granollers.

Una vez se ha definido el concepto de usabilidad, se debe saber que este tiene un gran conjunto de atributos, entre los cuales encontramos @toni-granollers: facilidad de aprendizaje, sintetizabilidad, familiaridad, consistencia, flexibilidad, robustez, recuperabilidad, tiempo de respuesta, adecuación de tareas y disminución de la carga cognitiva.

Al final, se puede concluir que la usabilidad incita a diseñar una interfaz centrada en el usuario (ver figura \ref{capitlo2:diseño-centrado-usuario}). Lo que implica conocer las particularidades de los usuarios para cada caso y reflejarlas en la interacción de la interfaz. Aunque un equipo de desarrollo pueda implementar sistemas similares, es crucial involucrar a los usuarios desde el inicio para lograr una familiaridad que proporcione seguridad y relajación durante la manipulación del sistema.

El objetivo es lograr una interfaz fácil de usar y aprender, lo cual requiere una estrecha colaboración con los usuarios a lo largo de todo el proceso de desarrollo. Implicar a los usuarios desde el principio es fundamental, y no se debe confundir con simplemente diseñar pensando en el usuario sin su participación activa. Es crucial conocer la opinión de los usuarios de primera mano para garantizar la utilidad y la comodidad de la interfaz.

Además, los sistemas interactivos deben centrarse en todos los usuarios, considerando las diferencias individuales, incluso teniendo en cuenta a aquellos con discapacidades. Ignorar a los usuarios o dejar su participación a la fase final del proyecto puede resultar en una interfaz que no cumple con sus necesidades y expectativas. En resumen, el diseño de sistemas interactivos implica hacer del usuario el foco principal desde el inicio del proceso hasta la implementación final, abarcando la diversidad de usuarios y sus características específicas.

![Diseño centrado en el usuario\label{capitlo2:diseño-centrado-usuario}](diseño-centrado-usuario.png){width=50%}

Por otro lado, dentro de la disciplina de la IPO, también se puede encontrar el término experiencia de usuario, el cual no debe ser confundido con usabilidad, después de todo este último es una faceta del primero. En el siguiente punto, se explica mejor el concepto de experiencia de usuario.

### Experiencia de Usuario
El término de experiencia de usuario no tiene una definición consensuada, sin embargo, el estándar ISO lo define como "las percepciones y respuestas de una persona que resultan del uso y/o uso anticipado de un producto, sistema o servicio" @toni-granollers.

Además, la experiencia de usuario presenta diferentes facetas a considerar para el diseño o evaluación de un sistema interactivo. Sin embargo, nuevamente al igual que ocurre con su definición, todavía no están consensuadas ni por la comunidad científica ni por ningún organismo de estandarización. A continuación, se mencionan diferentes facetas para diferentes autores @toni-granollers:

- El autor Peter Morville definió la colmena de la UX en la que se incluyen: usable, útil, deseable, valioso, creíble, encontrable y accesible como atributos a considerar para obtener una UX positiva.
- Autores como Hassenzahl y Tractinsky proponen tres facetas: más allá de lo instrumental; experimental; y emociones y afectos.
- Otros referentes como Hassan Montero y Ortego Santamaría señalan a usuario, contexto y contenido como los componentes más importantes dentro de la experiencia de usuario.

En conclusión, “la experiencia de usuario atiende a todos los factores, tanto internos como externos del usuario y del sistema interactivo, que causen alguna sensación a quien esté utilizando un sistema interactivo concreto en un determinado contexto de uso” @toni-granollers. Entre estos factores, encontramos la usabilidad, la cual ya ha sido explicada en el punto anterior, y será un factor a tener muy en cuenta a la hora de desarrollar la aplicación Web deseada. De la cual se hablará más en detalle en los próximos capítulos.
