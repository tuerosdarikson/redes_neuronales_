Proyecto de Predicción de Montos de Préstamos Digitales en Perú
Objetivo del Trabajo
El presente proyecto tiene como finalidad aplicar técnicas de aprendizaje supervisado —específicamente regresión lineal simple y redes neuronales artificiales— para predecir el monto promedio de préstamos digitales otorgados a clientes peruanos. El desarrollo se realizó utilizando Python, con el apoyo de bibliotecas especializadas como Pandas, NumPy, Scikit-learn y TensorFlow/Keras. Asimismo, se utilizó GitHub como sistema de control de versiones y plataforma de documentación del proyecto.

Breve Descripción del Dataset
El dataset utilizado proviene de Kaggle y se titula "Préstamos Digitales - Perú". Está conformado por registros anonimizados de clientes que han interactuado con plataformas financieras digitales. Cada fila representa un cliente, y las columnas incluyen información relevante sobre comportamiento digital y datos financieros.

Las variables empleadas en este estudio son:

trxDigitalUm: número de transacciones digitales realizadas en el último mes.

promSaldoPrest3Um: promedio del saldo de préstamo en los últimos tres meses.

genero: sexo del cliente (Masculino/Femenino).

procedencia: región o ciudad de residencia del cliente.

Para garantizar la calidad del entrenamiento de los modelos, se filtraron los registros eliminando los que presentaban valores nulos o promSaldoPrest3Um igual a cero.

Librerías Utilizadas
Las siguientes bibliotecas fueron esenciales para el desarrollo del análisis:

Pandas y NumPy: para la manipulación y transformación del conjunto de datos.

Matplotlib: para la visualización de los resultados.

Scikit-learn: para el entrenamiento del modelo de regresión lineal, escalado de variables y cálculo de métricas.

TensorFlow / Keras: para el diseño, entrenamiento y evaluación de la red neuronal artificial.

Explicación de los Modelos
1. Regresión Lineal Simple
Objetivo: modelar la relación entre la frecuencia de transacciones digitales (trxDigitalUm) y el monto promedio del préstamo (promSaldoPrest3Um).

Implementación: se usó el modelo LinearRegression de sklearn, dividiendo el dataset en conjuntos de entrenamiento (80%) y prueba (20%).

Visualización: se construyó un gráfico de dispersión con la línea de regresión superpuesta para evaluar la relación entre las variables.

2. Red Neuronal Artificial
Entradas: trxDigitalUm, genero_cod (codificación del sexo), procedencia_cod (codificación de la ubicación).

Variable objetivo: promSaldoPrest3Um

Arquitectura del modelo:

Una capa de entrada con 3 neuronas.

Tres capas ocultas con 64, 32 y 16 neuronas respectivamente, todas con activación ReLU.

Una capa de salida con activación lineal.

Compilación y entrenamiento: el modelo se entrenó usando el optimizador Adam, función de pérdida MSE (error cuadrático medio) y métrica MAE (error absoluto medio). Se utilizaron 100 épocas con validación cruzada interna del 20%.

Capturas de Gráficas
Las siguientes gráficas fueron generadas durante el proyecto:

Gráfico de regresión lineal: muestra la relación entre trxDigitalUm y promSaldoPrest3Um.

Gráfico de evolución del error: visualiza la disminución del error (loss) durante las 100 épocas de entrenamiento de la red neuronal.

Gráfico de valores reales vs predichos: evalúa visualmente la calidad de las predicciones de la red neuronal en el conjunto de prueba.

Todas las gráficas se encuentran integradas en el notebook principal (.ipynb).

Conclusiones Personales
La regresión lineal permite entender relaciones simples entre variables, sin embargo, su capacidad predictiva es limitada cuando intervienen múltiples factores.

La red neuronal artificial demostró ser un modelo más potente para predecir montos de préstamo, capturando relaciones no lineales y dependencias múltiples.

La limpieza del dataset fue determinante para asegurar la calidad de los resultados.

El uso de herramientas modernas como Keras y Scikit-learn facilita la experimentación rápida y efectiva en entornos de ciencia de datos.

Este proyecto refuerza la importancia del aprendizaje automático para la toma de decisiones financieras basadas en datos reales.
