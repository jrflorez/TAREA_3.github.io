# TAREA_3.github.io

TAREA 3 ALGORITMOS DE APRENDIZAJE SUPERVISADO

TRABAJO PRESENTADO AL TUTOR
BREYNER ALEXANDER PARRA -
SANDRA MILENA PATINO AVELLA

ESTUDIANTE 
JOSE RICARDOFLOREZ CESPEDES
GRUPO 202016908_45

ANÁLISIS DE DATOS

UNIVERSIDAD NACIONAL ABIERTA Y A DISTANCIA

INGENIERIA DE SISTEMAS 

2025

CALI

Análisis e interpretación de los resultados obtenidos en el desarrollo de un modelo de Regresión Lineal para predecir el precio de venta de vehículos. Se exploraron diversas variables como el año del vehículo y su kilometraje para determinar su influencia en el precio de venta.


Descripción del Dataset

El dataset utilizado contiene información relevante sobre diversos vehículos, incluyendo:

Año del vehículo

Kilometraje recorrido

Precio de venta (variable objetivo)

Tendencia creciente:

Los autos más nuevos (años más recientes) tienden a tener precios más altos.

A medida que el año aumenta, la dispersión de los precios se incrementa, lo que indica que hay más variabilidad en los valores de los vehículos más recientes.

Precios bajos en autos antiguos:

Los autos de años anteriores a 2005 tienen precios mucho más bajos en comparación con los modelos más nuevos.

Esto sugiere que los autos más antiguos pierden valor con el tiempo (depreciación).

Mayor dispersión en modelos recientes:

Desde aproximadamente 2010 en adelante, los precios varían ampliamente. Algunos vehículos tienen precios extremadamente altos, mientras que otros tienen precios más accesibles.

Esto podría deberse a la presencia de autos de lujo o vehículos especiales que mantienen o aumentan su valor.
Antes del modelado, se realizó una limpieza de datos, eliminando valores nulos y atípicos para asegurar la calidad de la información.


Entrenamiento del Modelo de Regresión Lineal

Para la predicción del precio de los vehículos, se utilizó un modelo de Regresión Lineal con las siguientes variables predictoras:

X: Año del vehículo, Kilometraje recorrido

Y: Precio de venta


División de los Datos

Los datos se dividieron en:

80% para entrenamiento

20% para prueba


Evaluación del Modelo

Las métricas de desempeño fueron:

MAE (Error Absoluto Medio)

MSE (Error Cuadrático Medio)

R² (Coeficiente de determinación)

Estos valores reflejan el grado de precisión del modelo en la predicción del precio de los vehículos.

Análisis de las Gráficas Generadas

se analizan los gráficos generados para entender el comportamiento de los datos y la precisión del modelo:

Histograma del Precio de Venta

Este gráfico muestra la distribución de los precios de los vehículos en el dataset, observando si existen valores extremos que puedan afectar el modelo.

Relación Año del Vehículo vs Precio

Se observa que los vehículos más nuevos tienden a tener precios más altos, mientras que los modelos más antiguos tienen precios más bajos, lo que confirma una relación inversamente proporcional.


Matriz de Correlación

Se identificó una correlación negativa entre el kilometraje y el precio, lo cual indica que a mayor kilometraje, menor es el valor del vehículo. También se evidenció una correlación positiva entre el año del vehículo y su precio.
matriz de correlación entre variables. permite visualizar las relaciones entre diferentes características de un conjunto de datos, probablemente relacionado con vehículos.

observaciones :

La variable "Price" (Precio) tiene una correlación fuerte con "Length" (0.56), "Width" (0.56) y "Fuel Tank Capacity" (0.58).

"Length" y "Width" están fuertemente correlacionadas (0.81), lo cual es lógico, ya que ambas están relacionadas con el tamaño del vehículo.

"Height" y "Seating Capacity" tienen una correlación de 0.70, lo que podría indicar que vehículos más altos suelen tener más capacidad de asientos.

"Year" y "Kilometer" tienen una correlación negativa de -0.30, lo que sugiere que los autos más nuevos tienden a tener menos kilometraje recorrido.

Comparación de Valores Reales vs Predichos

El gráfico de dispersión muestra que la mayoría de los valores predichos están alineados con los valores reales, lo que indica que el modelo tiene un buen nivel de precisión.


El modelo de regresión lineal logró capturar de manera efectiva la relación entre las variables predictoras y el precio de venta de los vehículos.

La precisión del modelo puede mejorarse incluyendo otras variables relevantes como la marca, el tipo de combustible o el número de propietarios anteriores.

Se recomienda optimizar el modelo utilizando técnicas más avanzadas como Regresión Polinómica o modelos de aprendizaje automático, como árboles de decisión o redes neuronales.

Con estos análisis, se puede concluir que el modelo es útil para realizar predicciones de precios de vehículos con una precisión aceptable, aunque existen oportunidades para mejorarlo y refinarlo con técnicas más sofisticadas
