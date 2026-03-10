# Descripción del Proyecto

Este proyecto implementa un sistema de **detección de fraude en transacciones con tarjeta de crédito utilizando técnicas de Machine Learning.**

La detección de fraude es un problema crítico en la industria **fintech**, donde los modelos deben ser capaces de identificar transacciones sospechosas en datasets altamente desbalanceados, minimizando al mismo tiempo los falsos positivos que podrían afectar la experiencia del usuario.

El objetivo principal del proyecto es **desarrollar y evaluar modelos de clasificación capaces de identificar transacciones fraudulentas**, manejando adecuadamente el desbalance de clases y optimizando métricas relevantes para este tipo de problema.

---

# Dataset

El dataset contiene transacciones realizadas con tarjetas de crédito por titulares europeos.

Características principales:

| Característica                | Valor   |
| ----------------------------- | ------- |
| Número total de transacciones | 284,807 |
| Transacciones fraudulentas    | 492     |
| Proporción de fraude          | ~0.17%  |

Debido a razones de confidencialidad, las variables han sido transformadas mediante **Análisis de Componentes Principales (PCA).**

Variables incluidas:

* V1 – V28: variables anonimizadas obtenidas mediante PCA
* Time: segundos transcurridos entre transacciones
* Amount: monto de la transacción
* Class: variable objetivo
    * 0: transacción legítima
    * 1: fraude

---

# Problema de Desbalance de Clases

El dataset presenta un **desbalance extremo entre clases**, donde las transacciones fraudulentas representan menos del **1% del total.**

Para abordar este problema se aplicaron las siguientes estrategias:

* Random Undersampling en el conjunto de entrenamiento
* Mantener el dataset de validación con la distribución original

Esto permite entrenar el modelo correctamente sin comprometer la evaluación realista del desempeño.

---

# Metodología

El flujo del proyecto se compone de las siguientes etapas:

1. Análisis Exploratorio de Datos (EDA)
2. Preprocesamiento del dataset
3. Manejo del desbalance de clases
4. Entrenamiento de modelos de clasificación
5. Ajuste del threshold de clasificación
6. Evaluación del desempeño del modelo

---

# Modelos Implementados

Se entrenaron dos modelos de Machine Learning:

**Regresión Logística**

Utilizada como modelo baseline para establecer una referencia inicial de desempeño.

Ventajas:

* Interpretabilidad
* Simplicidad
* Bajo costo computacional

**Random Forest**

Modelo de ensamblado basado en múltiples árboles de decisión.

Ventajas:

* Captura relaciones no lineales
* Maneja bien datasets complejos
* Reduce overfitting mediante agregación de árboles

**Ajuste del Threshold de Clasificación**

El threshold por defecto en modelos de clasificación suele ser 0.5.

En este proyecto se ajustó a **0.9**, con el objetivo de:

* Reducir falsos positivos
* Mantener una buena tasa de detección de fraude
* Lograr un mejor balance entre precision y recall

Este tipo de ajuste es común en sistemas de detección de fraude en producción.

--- 

# Resultados del Modelo

**Random Forest (Mejor Modelo)**

| Métrica   | Resultado |
| --------- | --------- |
| Accuracy  | 0.999     |
| Precision | 0.84      |
| Recall    | 0.85      |
| F1 Score  | 0.84      |
| ROC-AUC   | 0.983     |
| PR-AUC    | 0.774     |


**Matriz de Confusión**

|               | Predicho Legítimo | Predicho Fraude |
| ------------- | ----------------- | --------------- |
| Real Legítimo | 56,843            | 17              |
| Real Fraude   | 15                | 87              |


Interpretación:

1. 87 fraudes detectados correctamente
2. 15 fraudes no detectados
3. 17 falsos positivos
4. 56,843 transacciones legítimas clasificadas correctamente

El modelo logra detectar aproximadamente **85% de las transacciones fraudulentas.**

---
# Comparación de Modelos

| Modelo              | Precision | Recall   | F1 Score | ROC-AUC   |
| ------------------- | --------- | -------- | -------- | --------- |
| Logistic Regression | 0.79      | 0.80     | 0.80     | 0.956     |
| Random Forest       | **0.84**  | **0.85** | **0.84** | **0.983** |

El modelo **Random Forest superó al baseline en todas las métricas clave**, lo que indica una mejor capacidad para capturar patrones complejos de fraude.

---

# Métricas Utilizadas
Debido al desbalance del dataset, se priorizaron métricas más informativas que la accuracy:

1. Precision: proporción de fraudes predichos correctamente
2. Recall: capacidad del modelo para detectar fraudes reales
3. F1 Score: balance entre precision y recall
4. ROC-AUC: capacidad del modelo para separar ambas clases
5. PR-AUC: métrica más adecuada para datasets desbalanceados

---

# Tecnologías Utilizadas

- Python

- Pandas

- NumPy

- Scikit-learn

- Matplotlib

