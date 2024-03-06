# Entrevistas

En este anexo se recogen las entrevistas realizadas con los stakeholders durante el desarrollo del proyecto. Estas entrevistas se enmarcan dentro de un método de evaluación de usabilidad por indagación, tal y como explica Granollers @metodos-evaluacion-usabilidad. El proceso de indagación se basa en alcanzar el conocimiento a través de la reflexión. En este tipo de métodos, una parte crucial del trabajo implica interactuar con los usuarios y observar detenidamente su uso del sistema en situaciones reales, con el objetivo de obtener respuestas a preguntas planteadas verbalmente o por escrito. A continuación, se detallan cada una de las entrevistas realizadas.

## Primera Entrevista

La primera entrevista tuvo lugar el 16 de febrero de 2024, llevada a cabo en formato de videoconferencia Contó con la participación de los stakeholders, Cristina y Manuel. A lo largo de la reunión, se abordaron una serie de preguntas que condujeron a unas conclusiones.

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
