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


El conjunto de datos contiene 301 registros y 9 columnas, relacionadas con vehículos en venta. Las variables incluyen información como el nombre del auto, año, precio original, precio de venta, kilómetros recorridos, tipo de combustible, tipo de vendedor, tipo de transmisión y número de dueños anteriores.

El precio de venta promedio de los autos es 4.66, con un máximo de 35, lo que sugiere la presencia de vehículos de mucho valor en relacion al de menor valor.
El kilometraje promedio es de 36,947 km, pero existen vehículos con hasta 500,000 km, lo cual es un valor muy alto y puede influir negativamente en el precio de venta.

La mayoría de los autos han tenido un solo dueño (0), aunque hay algunos con hasta 3 dueños anteriores.
La mayoría de los autos tienen un precio de venta inferior a 10.
Hay una distribución sesgada (asimetría positiva)

La mayor densidad de precios se encuentra entre 0 y 5.
Segun el diagrama de caja (boxplot) hay varios valores atípicos (outliers) por encima de los 15.

Existe una alta correlación (0.88) entre el Present_Price y el Selling_Price, cuanto mayor es el precio original del auto, mayor será su precio de venta.
Year también tiene una correlación positiva (0.24) con el precio de venta autos más nuevos tienden a venderse a mayor precio.
Kms_Driven tiene una ligera correlación negativa (-0.05) con el precio de venta, cuanto más usado está un auto, menor suele ser su precio.

La variable Owner tiene baja correlación con el precio de venta, lo que sugiere que el número de dueños anteriores no influye significativamente en el precio.

No hay valores faltantes
la variables año de fabricación también tienen relación con el precio de venta
 
utilicé el método SelectKBest con la función f_regression, que evalúa la relación estadística entre cada característica y la variable objetivo, que en este caso es el precio de venta del carro (Selling_Price), realice la codificación de las variables categóricas (Fuel_Type, Seller_Type y Transmission) usando LabelEncoder, ya que los algoritmos de regresión lineal solo funcionan con datos numéricos,calculé la edad del carro restando el año del vehículo al año actual (2025) y eliminé la columna Year, ya que Car_Age es más útil para el modelo.

utilice el SelectKBest, que asigna un puntaje de relevancia a cada una de las variables independientes, ordené los resultados de mayor a menor relevancia.
Esto indica que las características más influyentes para predecir el precio de venta

Present_Price (precio actual del carro)
Seller_Type (tipo de vendedor)
Fuel_Type (tipo de combustible)
Transmission (tipo de transmisión)
Tamaño de datos de entrenamiento: (240, 8) 
Tamaño de datos de prueba: (61, 8)

Separé el 80% para entrenamiento y el 20% para prueba, use train_test_split de sklearn y además fijé el proceso aleatorio (random_state=42) para que siempre que corra el código me dé la misma división.

R² Score: 0.22822489808575297 
RMSE: 4.967028000903721
 
En esta gráfica estoy comparando el precio real de los vehículos con el precio que predice el modelo de regresión lineal que entrené.

Cada punto azul representa un carro del conjunto de prueba:
El eje X muestra el precio real del carro.
El eje Y muestra el precio que predijo el modelo.

La línea roja discontinua representa el lugar donde el precio predicho sería igual al precio real.

Entre más cerca estén los puntos de esa línea, mejor la predicción.
al evaluar qué tan bien está funcionando mi modelo de regresión lineal, utilicé varias métricas que son adecuadas para este tipo de modelos:

R² (Coeficiente de Determinación): indica qué tan bien se ajusta el modelo a los datos reales. 
se obtuvo un R² de 0.228, el modelo explica aproximadamente el 22.8% de la variabilidad del precio.

RMSE (Root Mean Squared Error): me dio un valor de 4.96, error promedio entre el precio real y el predicho es de 4.96 unidades

Estas métricas me permiten entender si el modelo está haciendo buenas predicciones
 
En la gráfica comparo directamente los precios reales con los que predijo el modelo. Cada punto azul representa un vehículo: su precio real y su precio estimado.

La línea roja es la línea perfecta, donde el precio predicho sería exactamente igual al real, muchos puntos están cerca de esa línea, lo cual indica que el modelo tiene buen desempeño
 
se evidencia cómo se comportan los errores en relación con el precio que predice el modelo. En el eje X están los precios que predice, y en el eje Y está el error (precio real menos predicho).

La línea roja representa el cero, o sea, cuando no hay error. Si los puntos están dispersos uniformemente alrededor de esa línea, como se ve en mi gráfica, el modelo no tiene un patrón de error y se comporta de forma bastante estable en diferentes rangos de precios.
 
la mayoría de los errores están cerca de 0, lo cual es bueno porque significa que el modelo generalmente predice con precisión
 
Desempeño del modelo
R² Score en entrenamiento: 0.8821220886752527
RMSE (Error cuadrático medio): 4.092088226121881

el modelo explica aproximadamente el 88% de la variación en los precios de venta de los carros
es un buen nivel de ajuste para tratarse de un modelo lineal simple.

La variable más influyente fue "Present_Price", seguida por "Seller_Type" y "Fuel_Type", ya que el precio actual de venta es el principal factor que afecta cuánto se puede vender un carro usado.

El modelo de regresión lineal proporciona una aproximación para predecir el precio de venta de los vehículos, basado en las variables disponibles. 

