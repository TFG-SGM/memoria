# Estudio de Técnicas de Visualización de Datos

En este anexo se recopilan las diferentes técnicas de visualización propuestas para analizar los datos que se recopilen tras el uso del algoritmo de la inteligencia artificial. No obstante, antes de explorar las diversas técnicas es fundamental identificar los datos a visualizar.

## Identificación de Datos 

Los datos que se han identificado para visualizar en la aplicación Web son los que se enumeran a continuación:

- **Duración del vídeo en segundos**: Permite un análisis detallado.
- **Partes del cuerpo de interés para cada tipo de prueba**: Identifica las áreas relevantes para cada evaluación.
- **Desplazamiento ideal y real de cada parte del cuerpo**: Se registra el movimiento óptimo y el movimiento real en cada segundo del vídeo en los ejes *x* e *y*.
- **Variación entre desplazamiento ideal y real**: Se analiza la discrepancia entre el movimiento deseado y el observado en cada parte del cuerpo y en cada segundo del vídeo, en los ejes *x* e *y*.
- **Restricción de movimiento por parte del cuerpo**: Se asigna un valor del 0 al 100 que representa la limitación de movimiento para cada parte del cuerpo. Este cálculo se basa en las variaciones de movimiento observadas en los ejes *x* e *y* entre todos los pacientes, siendo el valor máximo (100) la media de las cinco peores situaciones.
- **Restricción de movimiento total después de la prueba**: Al igual que el dato anterior, se asigna un valor del 0 al 100 que indica la restricción de movimiento total tras la prueba. Este valor se calcula considerando la media de las restricciones individuales de movimiento para cada parte del cuerpo entre todos los pacientes, siendo el valor máximo (100) la media de las cinco peores situaciones.

Una vez identificados los diferentes datos a visualizar, en los siguientes puntos se detallarán las diferentes técnicas de visualización de datos para distintos casos.

## Visualización del Tiempo de Vídeo

La Figura \ref{anexo5:lineas} muestra una gráfica de línea que representa el desplazamiento de una parte específica del cuerpo en un eje concreto en cada fotograma del vídeo de la prueba. Esta visualización permite comparar el desplazamiento observado con el desplazamiento ideal.

![Gráfica de línea según tiempo de vídeo\label{anexo5:lineas}](anx5_lineas.png)

## Evaluación de Restricción de Movimiento

Para evaluar la restricción de movimiento de las distintas partes del cuerpo, se recurre a técnicas de visualización tipo ranking. Estas pueden ser representadas tanto mediante un diagrama radial, como se ilustra en la Figura \ref{anexo5:radar}, o mediante un gráfico de barras, como se muestra en la Figura \ref{anexo5:barras}. Sin embargo, se sugiere preferir el uso del gráfico de barras debido a su capacidad para diferenciar de manera más clara entre los datos.

![Diagrama radial para evaluar restricción de movimiento\label{anexo5:radar}](anx5_radar.png)

![Gráfica de barras para evaluar restricción de movimiento\label{anexo5:barras}](anx5_barras.png)

## Análisis Conjunto

Para abordar el análisis integral de la restricción del movimiento, se emplean técnicas de visualización que representan el todo y sus partes. Entre estas técnicas se incluyen el gráfico de pastel, ejemplificado en la Figura \ref{anexo5:pastel}, y el diagrama de árbol, representado en la Figura \ref{anexo5:arbol}. Aunque el gráfico de pastel podría considerarse como una opción, se prefieren los diagramas de barras o de árbol debido a que ofrecen una percepción visual más clara y efectiva.

![Gráfico de pastel según el conjunto de la restricción de movimiento\label{anexo5:pastel}](anx5_pastel.png)

![Diagrama de árbol según el conjunto de la restricción de movimiento\label{anexo5:arbol}](anx5_arbol.png)

## Distribución de Datos

Para analizar la distribución de los datos, específicamente la variación entre el desplazamiento real y el ideal de las distintas partes del cuerpo en un eje específico, se emplean técnicas de visualización como el histograma, representado en la Figura \ref{anexo5:histograma}, y el diagrama de cajas y bigotes, ejemplificado en la Figura \ref{anexo5:caja-2}. 

![Histogramas comparando la distribución de variaciones entre el desplazamiento real e ideal \label{anexo5:histograma}](anx5_histograma.png)

![Diagrama de cajas y bigotes comparando la distribución de variaciones de varias partes del cuerpo\label{anexo5:caja-2}](anx5_caja-2.png)

Además, el diagrama de cajas y bigotes puede ser usado para comparar la distribución del desplazamiento real e ideal de una parte del cuerpo específica. Aunque, en este caso será necesario un división de cuando empieza y acaba una repetición del movimiento pedido durante la prueba.

![Diagrama de cajas y bigotes comparando la distribución del desplazamiento real e ideal de una parte del cuerpo\label{anexo5:caja-1}](anx5_caja-1.png)

## Correlación entre Partes del Cuerpo

Para observar la correlación entre las diferentes partes del cuerpo, se propone utilizar las ténicas de visualización como el diagrama de burbujas mostrado en la Figura \ref{anexo5:burbujas} y el mapa de calor ilustrado en la FIgura \ref{anexo5:calor}. En dichos diagramas se relacionan las diferentes partes del cuerpo según si tienen la misma variación en un momento exacto del vídeo.

![Diagrama de burbujas según la variación de dos partes del cuerpo en un momento de la prueba\label{anexo5:burbujas}](anx5_burbujas.png)

![Mapa de calor según la variación de dos partes del cuerpo en un momento de la prueba\label{anexo5:calor}](anx5_calor.png)

## Evolución del Paciente

Finalmente, para analizar la evolución del paciente se emplean diversas técnicas de visualización que muestren como mejora o empeora la restricción de movimiento de las diferentes partes del cuerpo del paciente. Entre estas técnicas se pueden utilizar las gráficas de líneas, tal y como muestra la Figura \ref{anexo5:evolucion-lineas}, las de barras ilustradas en la Figura \ref{anexo5:evolucion-barras} y varios diagramas radiales como se observa en la Figura \ref{anexo5:evolucion-radar}.

Se sugiere además emplear técnicas de análisis de distribución para examinar la manera en que las restricciones de movimiento se distribuyen en distintas partes del cuerpo a lo largo del tiempo. Igualmente, se propone utilizar métodos de correlación para identificar momentos en los que dos regiones corporales presenten restricciones de movimiento similares.

![Gráficas de líneas para analizar evolución del paciente\label{anexo5:evolucion-lineas}](anx5_evolucion-lineas.png)

![Gráficas de barras para analizar evolución del paciente\label{anexo5:evolucion-barras}](anx5_evolucion-barras.png)

![Diagramas radiales para analizar evolución del paciente\label{anexo5:evolucion-radar}](anx5_evolucion-radar.png)
