# Entrevistas

En este anexo se recogen las entrevistas realizadas con los stakeholders durante el desarrollo del proyecto. Estas entrevistas se enmarcan dentro de un método de evaluación de usabilidad por indagación, tal y como explica Granollers @metodos-evaluacion-usabilidad. El proceso de indagación se basa en alcanzar el conocimiento a través de la reflexión. En este tipo de métodos, una parte crucial del trabajo implica interactuar con los usuarios y observar detenidamente su uso del sistema en situaciones reales, con el objetivo de obtener respuestas a preguntas planteadas verbalmente o por escrito. A continuación, se detallan cada una de las entrevistas realizadas.

## Primera Entrevista

La primera entrevista tuvo lugar el 16 de febrero de 2024, llevada a cabo en formato de videoconferencia. Contó con la participación de los stakeholders, Cristina y Manuel. A lo largo de la reunión, se abordaron una serie de preguntas que condujeron a unas conclusiones.

### Guión de Preguntas

En este punto se presenta el guión de preguntas utilizado durante la entrevista. Es fundamental resaltar que, además de obtener información mediante preguntas directas a los interesados, también se sostuvo una conversación con ellos. A continuación, se enumeran las preguntas formuladas durante la entrevista.

**¿Cuál es el propósito principal de la aplicación Web?** 

El propósito fundamental es facilitar a los médicos la capacidad de proporcionar retroalimentación a los pacientes sobre su movilidad y postura. La idea es que esta herramienta sea utilizada conjuntamente por el médico y el paciente durante sesiones presenciales.

**¿Quién necesita acceder a la plataforma Web y qué roles desempeñan?** 

El acceso estará limitado a los médicos, ya que la aplicación está diseñada para ofrecer retroalimentación a los pacientes. Además, puede haber un rol de administrador encargado de gestionar los permisos de acceso de los médicos.

**¿Qué métodos pueden utilizar los médicos para realizar las pruebas de diagnóstico?** 

Los médicos pueden optar por grabar directamente desde la aplicación Web o adjuntar vídeos ya grabados. Sería útil que la aplicación Web ofrezca indicaciones, como alertas si una parte del cuerpo no se detecta correctamente o si hay problemas de iluminación. Además, es importante considerar que existen diferentes tipos de pruebas con requisitos específicos.

**¿Deberían incluirse los vídeos como parte de la visualización de las pruebas?**

No, ya que algunas personas pueden no sentirse cómodas viéndose en vídeo. Una alternativa sugerida es presentar un modelo tridimensional del cuerpo en su lugar.

**¿Cuál es el resultado final esperado de las pruebas? ¿Se presenta un porcentaje de probabilidad de tener fibromialgia, o se analiza porcentaje por cada área del cuerpo?**

El objetivo es comparar los datos del paciente con los de un movimiento ideal. Esta comparación puede presentarse mediante modelos 3D y gráficos de datos. Además, la aplicación debe permitir focalizar en áreas específicas del cuerpo y asignarles una puntuación o porcentaje.

**¿Se pueden ver pruebas realizadas en el pasado?**

Sí, sería útil que los pacientes pudieran ver pruebas anteriores y compararlas para observar su progreso a lo largo del tiempo, lo que podría motivarlos a mejorar.

### Conclusiones

Tras la primera entrevista, se logró obtener una comprensión inicial de la visión de la aplicación deseada por los stakeholders. Se destaca principalmente la decisión de no permitir el acceso de los pacientes al sistema, enfocando su uso en la interacción entre médico y paciente para proporcionar retroalimentación sobre el movimiento. Debido a esto, algunas preguntas preparadas sobre el rol del cliente no se pudieron realizar como las siguientes:

- ¿Tiene acceso a todas las pruebas realizadas o solo a algunas específicas?
- ¿Puede agregar videos como parte de las pruebas? ¿Y puede enviarlos a los médicos?
- ¿Es posible que un paciente esté asignado a varios médicos?
- ¿La visualización de las pruebas es similar a la de los médicos o se presenta de manera más simplificada para los pacientes?

Por otro lado, es relevante mencionar que los requerimientos relacionados con las señales durante la grabación por parte del médico no forman parte del proyecto, ya que se prioriza el desarrollo de técnicas para visualizar los datos.

A pesar de las nuevas preguntas que surgieron tras depurar los distintos requisitos de la entrevista, se logró obtener una visión general que sirvió como base para el desarrollo continuo de la aplicación Web.

## Segunda Entrevista

La segunda entrevista, realizada el 11 de marzo de 2024, se llevó a cabo mediante videoconferencia con la participación de los stakeholders, Cristina y Manuel. Durante la reunión, se abordaron una serie de preguntas que condujeron a conclusiones significativas. Además, se presentó el prototipo no interactivo detallado en el Anexo 4, así como el estudio de técnicas de visualización de datos que se detalla en el Anexo 5.

### Guión de Preguntas

A continuación se detallan las preguntas formuladas durante la entrevista, las cuales se presentaron junto con el prototipo no interactivo.

**¿El médico puede gestionar otros médicos o solo a los pacientes?**

La gestión de los médicos debe ser exclusiva de los administradores, permitiendo a los médicos concentrarse en la atención de los pacientes.

**¿El administrador puede gestionar a los pacientes o esta función está reservada solo para los médicos?**

Tanto los médicos como los administradores pueden gestionar a los pacientes en la aplicación Web.

**¿Qué información se debe recopilar al crear un nuevo perfil de paciente?**

Se requiere información básica como nombre, apellidos, edad, ubicación, número de teléfono, correo electrónico, además de datos relevantes como el diagnóstico y tiempo de padecimiento de la fibromialgia, nivel de actividad física y ocupación.

**¿Un paciente puede tener asignados varios médicos?**

No, cada paciente deberá tener asignado un único médico.

**¿Debería una prueba en la aplicación Web contener datos de diferentes pruebas o solo de una?**

Cada prueba debe ser específica y contener sus propios datos individuales.

**¿Es posible añadir nuevos tipos de pruebas?**

Inicialmente, no se considera necesario añadir más tipos de pruebas. Además, es importante considerar que los puntos de interés para cada tipo de prueba han sido seleccionados cualitativamente.

**¿Qué información se debe proporcionar al crear una prueba?**

Al crear una prueba, se solicitará la fecha, tipo de prueba, un vídeo y posiblemente escalas para evaluar el estado del paciente en el momento de la prueba, como por ejemplo la escala [EVA](#EVA) para evaluar el dolor del paciente en el momento de realizar la prueba.

También se sugiere la posibilidad de crear múltiples pruebas de diferentes tipos simultáneamente para mejorar la eficiencia del médico. Además, se menciona la necesidad de un filtro para la facilitar la búsqueda de las pruebas por fecha o tipo.

**¿Es viable mostrar un "grado de problema" basado en la variación entre el movimiento ideal y el real para cada parte del cuerpo?**

Sí, se propone mostrar un "porcentaje de calidad de movimiento", calculado comparando el movimiento ideal con el movimiento real de cada parte del cuerpo.

### Conclusiones

Tras la segunda entrevista, se obtuvo una comprensión más profunda de los requisitos de la aplicación Web a desarrollar, enfatizando la importancia de la usabilidad para garantizar que los médicos puedan utilizar las funciones de manera sencilla y efectiva.

Además, se identificaron las preferencias de los stakeholders en cuanto a técnicas de visualización de datos, destacando las gráficas de líneas y de barras. Se sugiere, además, representar el desplazamiento en lugar del ángulo de cada parte del cuerpo, ya que esto simplificará su visualización.

