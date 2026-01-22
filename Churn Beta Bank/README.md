# Predicción de Churn de Clientes

## Descripción del proyecto
La pérdida de clientes (**churn**) es uno de los principales problemas estratégicos en empresas de servicios.  
Este proyecto desarrolla un **modelo de machine learning supervisado** para predecir la probabilidad de que un cliente abandone el servicio, utilizando datos históricos de comportamiento y características del cliente.

El objetivo es anticipar la deserción y permitir que la empresa implemente **estrategias de retención proactivas** basadas en datos.

---

## Objetivo
Construir un modelo predictivo que permita:
- Identificar clientes con alta probabilidad de churn
- Analizar los factores que influyen en la deserción
- Evaluar distintos modelos de clasificación
- Apoyar decisiones estratégicas de retención

---

## Dataset
El dataset contiene información relacionada con:
- Datos demográficos de clientes
- Comportamiento de uso del servicio
- Variables contractuales
- Historial de permanencia
- Variable objetivo: **Churn** (abandono del cliente)

Los datos fueron procesados y preparados para modelado supervisado.

---

## Metodología

### 1. Análisis exploratorio de datos (EDA)
- Análisis de distribuciones
- Identificación de patrones de churn
- Relación entre variables y abandono
- Análisis de correlaciones

### 2. Preprocesamiento
- Limpieza de datos
- Codificación de variables categóricas
- Normalización / escalado
- División de datos en entrenamiento y prueba

### 3. Modelado supervisado
Se entrenaron y compararon distintos modelos de clasificación:
- Regresión logística
- Árbol de decisión
- Random Forest

### 4. Evaluación
- Comparación de métricas de desempeño
- Selección del modelo óptimo
- Análisis de capacidad predictiva

---

## Modelos utilizados
- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier

---

## Métricas de evaluación
- **Accuracy**
- **Precision**
- **Recall**
- **F1-score**
- Matriz de confusión

---

## Resultados
- El modelo de **Random Forest** presentó el mejor desempeño general.
- Se identificaron variables clave asociadas al churn, como:
  - Tipo de contrato
  - Tiempo de permanencia
  - Tipo de servicio contratado
  - Consumo y uso del servicio

El modelo permite clasificar clientes según su nivel de riesgo de abandono.

---

## Conclusiones
- El churn puede ser modelado de forma efectiva mediante aprendizaje supervisado.
- El modelo permite anticipar la pérdida de clientes antes de que ocurra.
- Puede utilizarse como base para:
  - Campañas de retención
  - Ofertas personalizadas
  - Estrategias comerciales inteligentes
  - Optimización de ingresos

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
prediccion-churn/
│
├── AprendizajeSupervisado_Churn.ipynb
├── README.md
└── datasets/
    └── Churn.csv
