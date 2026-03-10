# Predicción de Ventas de Videojuegos

## Descripción del proyecto
La industria de los videojuegos es altamente competitiva y depende en gran medida de la toma de decisiones basada en datos.  
En este proyecto se analizan datos históricos de ventas de videojuegos con el objetivo de **identificar patrones de éxito** y **predecir el desempeño comercial** de los juegos según diferentes características.

El análisis permite comprender cómo factores como la plataforma, el género, la región y las reseñas influyen en las ventas globales.

---

## Objetivo
Desarrollar un análisis predictivo que:
- Identifique las características asociadas a videojuegos exitosos
- Analice tendencias de ventas por región y plataforma
- Apoye la toma de decisiones estratégicas en lanzamientos y marketing
- Explore modelos para la predicción de ventas

---

## Dataset
El conjunto de datos incluye información sobre:
- Nombre del videojuego
- Plataforma
- Género
- Año de lanzamiento
- Ventas por región (NA, EU, JP, Global)
- Calificaciones de críticos y usuarios

Los datos corresponden a ventas históricas y fueron utilizados con fines analíticos.

---

## Metodología

### 1. Análisis exploratorio de datos (EDA)
- Análisis de ventas globales y regionales
- Identificación de plataformas y géneros más rentables
- Evaluación de tendencias a lo largo del tiempo
- Análisis del impacto de reseñas en las ventas

### 2. Preparación de datos
- Limpieza de valores faltantes
- Conversión de tipos de datos
- Filtrado de periodos relevantes para el análisis
- Creación de variables auxiliares

### 3. Análisis y modelado
- Análisis estadístico de variables clave
- Evaluación de relaciones entre calificaciones y ventas
- Exploración de modelos predictivos para estimar ventas

---

## Métricas y criterios de análisis
- Análisis descriptivo
- Correlaciones
- Métricas de error para modelos predictivos (cuando aplica)

---

## Resultados
- Se identificaron **plataformas y géneros con mayor volumen de ventas**.
- Las ventas varían significativamente por región.
- Existe una relación entre las reseñas de críticos y el desempeño comercial de los videojuegos.
- Los datos históricos permiten generar estimaciones útiles para la planeación de lanzamientos.

---

## Conclusiones
- El análisis de datos es clave para reducir el riesgo en el lanzamiento de videojuegos.
- Las tendencias históricas ayudan a anticipar el comportamiento del mercado.
- Este enfoque puede apoyar decisiones en desarrollo, distribución y marketing.

---

## Tecnologías utilizadas
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  
- Jupyter Notebook  

---

## Estructura del proyecto
```text
prediccion-ventas-videojuegos/
│
├── prediccion_ventas_videojuegos.ipynb
├── README.md
└── data/
