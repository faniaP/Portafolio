# Predicción de Demanda de Taxis – Sweet Lift Taxi

## Descripción del proyecto
La compañía **Sweet Lift Taxi** ha recopilado datos históricos sobre pedidos de taxis en los aeropuertos.  
Para atraer a más conductores durante las **horas pico**, es necesario **predecir la cantidad de pedidos de taxis para la próxima hora**.

En este proyecto se desarrolla un **modelo de series temporales** capaz de anticipar la demanda horaria de taxis, permitiendo una mejor planificación operativa y asignación de recursos.

---

## Objetivo
Construir un modelo predictivo que:
- Pronostique la cantidad de pedidos de taxis para la siguiente hora
- Capture patrones temporales como tendencia y estacionalidad
- Cumpla con el criterio de desempeño:
  - **RECM (RMSE) ≤ 48** en el conjunto de prueba

---

## Dataset
El conjunto de datos contiene:
- Fecha y hora de los pedidos
- Número de pedidos realizados por intervalo de tiempo

Los datos fueron agregados por hora para facilitar el análisis de series temporales.

---

## Enfoque de Series Temporales

El problema se aborda como una **serie temporal univariada**, donde:
- La variable objetivo es el número de pedidos por hora
- El tiempo es el eje principal de análisis

---

## 🔍 Metodología

### 1. Análisis exploratorio de la serie
- Visualización de la serie temporal
- Identificación de tendencia y estacionalidad
- Análisis de autocorrelación

### 2. Preparación de datos
- Re-muestreo por hora
- Creación de variables retardadas (*lags*)
- Variables de calendario (hora, día de la semana)
- División de datos en entrenamiento y prueba respetando el orden temporal

### 3. Modelado
Se entrenaron distintos modelos de regresión adaptados a series temporales, incluyendo:
- Regresión Lineal
- Modelos basados en árboles

### 4. Evaluación
- Predicción sobre el conjunto de prueba
- Evaluación del desempeño mediante **RECM (RMSE)**

---

## Métrica de evaluación
- **RECM (Raíz del Error Cuadrático Medio)**

📌 Criterio del proyecto:
RECM ≤ 48


---

## Resultados

El modelo final logró cumplir con el umbral establecido de RECM ≤ 48.

Se observó que las variables temporales y los valores históricos (lags) son clave para la predicción de la demanda.

El modelo captura correctamente los picos de demanda en horarios específicos.


---

## Conclusiones

La demanda de taxis presenta patrones temporales claros y predecibles.

Los modelos de series temporales permiten anticipar horas pico de forma efectiva.

Esta solución puede apoyar la toma de decisiones operativas, como la asignación de conductores en aeropuertos.

---
### Tecnologías utilizadas

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

### Estructura del proyecto
```text
series_temporales/
│
├── series_temporales.ipynb
├── README.md
└── datasets/
    └── taxi.csv
