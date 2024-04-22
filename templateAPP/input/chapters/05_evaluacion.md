# Evaluación del Sistema

En este capítulo se presentan las distintas evaluaciones llevadas a cabo durante el desarrollo del proyecto, detallando los participantes involucrados, el contexto de uso, las tareas realizadas, el diseño experimental empleado, las métricas de usabilidad aplicadas y los resultados obtenidos en cada una de ellas. Como referencia, se ha seguido el estándar internacional ISO/IEC 25062 @iso-usabilidad para evaluar la calidad en el uso del sistema, complementado con el uso del cuestionario [SUS](#SUS), tal y como expone Sauro @sauro. Este cuestionario consta de diez preguntas diseñadas para evaluar la experiencia del usuario con el sistema, las cuales deben responderse indicando el grado de acuerdo o desacuerdo en una escala de cinco puntos.

## Primera Evaluación

La primera evaluación se realizó el 15 de abril de 2024 con el objetivo de recopilar las impresiones iniciales de usuarios reales y evaluar su satisfacción al utilizar la aplicación web. A continuación, se detallan los participantes, el contexto de uso, las tareas asignadas, el diseño experimental empleado, las métricas de usabilidad aplicadas y los resultados obtenidos en esta prueba de evaluación.

### Participantes

La evaluación se llevó a cabo con la participación de dos fisioterapeutas especializados, específicamente Cristina Bravo y Manuel Trinidad. Aunque el número de participantes pueda parecer reducido, el objetivo principal era asegurar la aceptación del sistema por parte de expertos en el campo. Además, al finalizar la prueba de evaluación, los participantes pudieron proporcionar un feedback muy relevante gracias a su experiencia y conocimiento especializado.

Una vez presentados los participantes, en el siguiente punto se describe el contexto de uso de la prueba de evaluación.

### Contexto de Uso

La evaluación se llevó a cabo mediante videoconferencia con la aplicación *Microsoft Teams* @teams, lo que permitió que cada participante utilizara su propio hardware. Específicamente, Cristina utilizó el sistema operativo *Windows* y Manuel *MacOS*.

Es importante destacar que la aplicación web se desplegó en *Render* @render y la base de datos en *MongoDB Atlas* @mongodb-atlas. Dado que ambas plataformas fueron utilizadas en una versión gratuita, se presentaron algunas limitaciones, siendo la principal la imposibilidad de finalizar la creación de una prueba y desconexiones temporales del servidor en algunos casos.

Al finalizar la evaluación, los participantes completaron el cuestionario [SUS](#SUS) para proporcionar retroalimentación sobre su experiencia. Este cuestionario fue realizado utilizando un formulario de *Google Forms* @google-forms.

Una vez presentado el contexto de uso, en el siguiente punto se describen las diferentes tareas realizadas por los participantes.

### Tareas

Las tareas realizadas por los participantes durante la evaluación fueron las siguientes:

- **Tarea 1:** Añadir un nuevo paciente. Editar la edad de dicho nuevo paciente. Eliminar el paciente recién creado.
- **Tarea 2:** Consultar pruebas del primer paciente. Filtrar por fecha la lista de pruebas. Analizar la gráfica de línea, pastel y burbuja de una de las pruebas. De esa misma prueba consultar los detalles.
- **Tarea 3:** Consultar evolución del primer paciente. Filtrar gráfica de evolución por un tipo de prueba y observar la evolución de dos partes del cuerpo específicas.
- **Tarea 4:** Hacer uso del menú de añadir prueba (pero sin acabar de añadir la prueba).

Una vez presentadas las tareas, en el siguiente punto se describe el diseño experimental de la prueba de evaluación.

### Diseño Experimental

El proceso de evaluación siguió los siguientes pasos:

1. **Explicación previa:** Antes de comenzar la evaluación, se proporcionó a cada participante un documento que detallaba las tareas a realizar y el proceso para iniciar sesión en la aplicación web.
2. **Realización de tareas:** Se asignó a cada participante una lista de tareas específicas que debían completar. Durante este proceso, se implementó la técnica de *pensamiento en voz alta*, permitiendo a los participantes expresar sus opiniones mientras interactuaban con la aplicación. También se utilizó la técnica de *observación* para analizar cómo los participantes se desenvolvían durante la prueba.
3. **Test de evaluación:** Una vez completadas las tareas, cada participante completó el cuestionario [SUS](#SUS). El objetivo de este paso era recopilar más información y opiniones sobre la aplicación desde la perspectiva de los usuarios.

Una vez presentado el diseño experimental, en el siguiente punto se describen las métricas de evaluación.

### Métricas de Usabilidad

La principal métrica de usabilidad utilizada en esta evaluación fue la satisfacción del usuario. Esta métrica se midió mediante el cuestionario [SUS](#SUS), que todos los participantes completaron al finalizar las tareas asignadas. El cuestionario constaba de diez declaraciones diseñadas para evaluar varios aspectos relacionados con la usabilidad de la aplicación, brindando así una comprensión más completa de la experiencia del usuario.

Finalmente, en el siguiente punto se describen los resultados obtenidos tras la completar la prueba de evaluación. 

### Resultados

Tras la primera prueba de evaluación, se recibió un valioso feedback por parte de ambos fisioterapeutas.

Mediante las técnicas de *pensamiento en voz alta* y *observación* durante la realización de las tareas, se confirmó que la aplicación web es fácil de utilizar. Sin embargo, se observó que el entendimiento de las gráficas que muestran los datos de las pruebas puede resultar confuso para algunos usuarios, lo que podría requerir la asistencia de un profesional para su interpretación.

Por otro lado, en la Figura \ref{capitulo5:resultados-sus1} se presentan los resultados del cuestionario [SUS](#SUS) de cada participante, los cuales muestran una evaluación muy positiva de la aplicación. Después de todo, según Sauro @sauro la media de resultados [SUS](#SUS) de 500 estudios es de 68, por lo que un resultado mayor se considera mejor que la media.

Además, Sauro proporciona la gráfica que se muestra en la Figura \ref{capitulo5:grafica-sauro}, donde se asocian los rangos percentiles con las puntuaciones del [SUS](#SUS) y las calificaciones con letras. Esta gráfica revela que los resultados de ambos participantes se encuentran en el rango A, ya que superan los 80,3 puntos.

![Resultados [SUS](#SUS)\label{capitulo5:resultados-sus1}](cap5_resultados-sus1.png){width=75%}

![Asociación entre rangos percentiles con puntuaciones [SUS](#SUS)\label{capitulo5:grafica-sauro}](cap5_grafica-sauro.png){width=75%}

## Resumen de las Evaluaciones

