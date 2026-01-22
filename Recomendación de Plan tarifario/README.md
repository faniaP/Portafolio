# Recomendación de Plan Tarifario – Megaline

## Descripción del proyecto
La compañía de telecomunicaciones **Megaline** busca migrar a sus clientes de planes heredados hacia sus nuevos planes tarifarios: **Smart** y **Ultra**.  
Para lograrlo, es necesario analizar el comportamiento de consumo de los clientes y **recomendar el plan más adecuado** según su uso real.

Este proyecto desarrolla un **modelo de clasificación** que, a partir de datos históricos de consumo, recomienda el plan óptimo para cada cliente.

---

## Objetivo
Construir un **sistema de recomendación** que:
- Analice el comportamiento de consumo de los clientes
- Identifique patrones de uso
- Recomiende uno de los planes tarifarios disponibles (**Smart** o **Ultra**)
- Evalúe el desempeño de distintos modelos de machine learning

---

## Dataset
El conjunto de datos contiene información agregada por cliente, incluyendo:
- Número de llamadas realizadas
- Minutos totales de llamadas
- Cantidad de mensajes enviados
- Consumo de datos móviles (MB)
- Plan tarifario actual

Los datos fueron previamente anonimizados y preparados para análisis.

---

## Metodología

### 1. Análisis exploratorio de datos (EDA)
- Revisión de variables
- Distribuciones y correlaciones
- Identificación de patrones de consumo por tipo de plan

### 2. Limpieza y procesamiento
- Verificación de valores faltantes
- Transformación de variables
- Separación de variables predictoras y variable objetivo

### 3. Modelado
Se entrenaron y evaluaron los siguientes modelos:
- 🌳 Árbol de Decisión
- 🌲 Random Forest

### 4. Evaluación
- Comparación de métricas de desempeño
- Selección del modelo con mejor capacidad predictiva

---

## Modelos utilizados
- Decision Tree Classifier
- Random Forest Classifier

Ambos modelos permiten interpretar qué variables influyen más en la recomendación del plan tarifario.

---

## Métrica de evaluación
- **Accuracy**
- Comparación entre modelos para seleccionar el mejor desempeño

---

## Resultados
- El modelo de **Random Forest** presentó un mejor rendimiento general frente al Árbol de Decisión.
- Las variables más relevantes para la recomendación fueron:
  - Consumo de datos móviles
  - Minutos de llamadas
  - Número de mensajes enviados

Esto demuestra que el patrón de consumo es un buen predictor del plan tarifario ideal.

---

## Conclusiones
- Es posible automatizar la recomendación de planes tarifarios mediante machine learning.
- El modelo puede apoyar estrategias de **retención de clientes** y **optimización de ingresos**.
- Random Forest resulta más robusto para este tipo de problema de clasificación.

---

## Tecnologías utilizadas
- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib  
- Seaborn  
- Jupyter Notebook  

---

## Estructura del proyecto
```text
recomendacion-plan-tarifario/
│
├── recomendacion_pla_tarifario.ipynb
├── README.md
└── datasets/
    ├── users_behavior.csv
