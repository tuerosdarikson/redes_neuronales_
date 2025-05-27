# Proyecto de Predicción de Montos de Préstamos Digitales en Perú

## Objetivo del Trabajo

Este proyecto tiene como finalidad aplicar técnicas de aprendizaje supervisado específicamente regresión lineal simple y redes neuronales artificiales para predecir el monto promedio de préstamos digitales otorgados a clientes peruanos.

El desarrollo se realizó utilizando Python, con el apoyo de bibliotecas especializadas como Pandas, NumPy, Scikit-learn y TensorFlow/Keras. Además, se empleó GitHub como sistema de control de versiones y plataforma de documentación del proyecto.

---

## Breve Descripción del Dataset

El dataset utilizado proviene de Kaggle y se titula **"Préstamos Digitales - Perú"**. Está conformado por registros anonimizados de clientes que han interactuado con plataformas financieras digitales. Cada fila representa un cliente y las columnas incluyen información relevante sobre comportamiento digital y datos financieros.

### Variables empleadas:

- `trxDigitalUm`: número de transacciones digitales realizadas en el último mes.
- `promSaldoPrest3Um`: promedio del saldo de préstamo en los últimos tres meses.
- `genero`: sexo del cliente (Masculino/Femenino).
- `procedencia`: región o ciudad de residencia del cliente.


---

## Librerías Utilizadas

- `Pandas` y `NumPy`: para la manipulación y transformación del conjunto de datos.
- `Matplotlib`: para la visualización de los resultados.
- `Scikit-learn`: para el modelo de regresión lineal, escalado de variables y evaluación de métricas.
- `TensorFlow / Keras`: para el diseño, entrenamiento y evaluación de la red neuronal artificial.

---

## Explicación de los Modelos

### 1. Regresión Lineal Simple

- **Objetivo:** Modelar la relación entre `trxDigitalUm` y `promSaldoPrest3Um`.
- **Implementación:** Se utilizó `LinearRegression` de `sklearn`. El dataset se dividió en entrenamiento (80%) y prueba (20%).
- **Visualización:** Se construyó un gráfico de dispersión con la línea de regresión superpuesta para evaluar la relación.

### 2. Red Neuronal Artificial

- **Entradas:** 
  - `trxDigitalUm`
  - `genero_cod` (codificación del sexo)
  - `procedencia_cod` (codificación de la ubicación)
- **Variable objetivo:** `promSaldoPrest3Um`
- **Arquitectura del modelo:**
  - Capa de entrada con 3 neuronas
  - 3 capas ocultas con 64, 32 y 16 neuronas (activación ReLU)
  - Capa de salida con activación lineal
- **Compilación y entrenamiento:**
  - Optimizador: `Adam`
  - Función de pérdida: `MSE` (Error cuadrático medio)
  - Métrica: `MAE` (Error absoluto medio)
  - 100 épocas con validación del 20%

---

## Capturas de Gráficas

Las siguientes gráficas se encuentran integradas en el notebook principal (`.ipynb`):

- **Gráfico de regresión lineal:** Relación entre `trxDigitalUm` y `promSaldoPrest3Um`.
- **Gráfico de evolución del error:** Disminución del `loss` durante las 100 épocas de entrenamiento.
- **Gráfico de valores reales vs predichos:** Evalúa visualmente la calidad de las predicciones en el conjunto de prueba.

---

## Conclusiones Personales

- La regresión lineal permite entender relaciones simples entre variables, pero su capacidad predictiva es limitada frente a modelos más complejos.
- La red neuronal artificial mostró mejor capacidad predictiva al capturar relaciones no lineales y dependencias múltiples.
- La limpieza del dataset fue crucial para lograr resultados confiables.
- Herramientas modernas como `Keras` y `Scikit-learn` facilitan la experimentación eficiente en ciencia de datos.
- Este proyecto refuerza la importancia del aprendizaje automático en la toma de decisiones financieras basadas en datos reales.
