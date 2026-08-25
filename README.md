# 📈 Pronóstico de Ventas Semanales - Walmart
**Asignatura:** Prospectiva Tecnológica y Producción Inteligente  
**Dataset:** Walmart Recruiting - Store Sales Forecasting (Kaggle)

---

## 📋 Descripción General del Proyecto
Este repositorio contiene el desarrollo completo de un ejercicio analítico y predictivo orientado a la gestión de demanda minorista (`Weekly_Sales`). El proyecto está estructurado metodológicamente en **dos partes complementarias**: un análisis macro de negocio y una extensión técnica de Machine Learning aplicada a series temporales.

---

## 🗂️ Estructura y Desarrollo por Partes

### Parte 1: Análisis Macro y Visualización de Negocio
* **Objetivo:** Analizar el comportamiento macroeconómico y la estacionalidad de las tiendas con mayor volumen de facturación histórica.
* **Implementación:** 
  * Procesamiento y agregación de datos mediante un pipeline en Python (Pandas) para agrupar ventas semanales.
  * Estructuración de datos orientada a alimentar un **Dashboard en Excel** que facilita la visualización gerencial de las tendencias clave de las tiendas Top.

### Parte 2: Modelado Predictivo y Machine Learning (Foco en Tienda 4)
* **Objetivo:** Desplegar modelos de pronóstico de demanda a un nivel de granularidad mayor (**por departamento / `Dept`**).
* **Criterio de Selección:** Para esta fase de modelado, se seleccionó específicamente la **Tienda 4**. Esta decisión estratégica se tomó tras verificar que presenta una alta estabilidad operativa y una **mínima presencia de ruido, valores atípicos y registros negativos** por devoluciones masivas, lo cual evita distorsiones críticas en los algoritmos de predicción.
* **Metodología y Herramientas:** Implementación de modelos de series temporales (como *Holt-Winters*) en entornos de Jupyter Notebook para anticipar el comportamiento futuro de la demanda.

---

## 🔄 Arquitectura de Datos y Pipeline (ETL)
El flujo de la información sigue una arquitectura analítica estándar:
1. **Extracción (Extract):** Ingesta del archivo masivo `train.csv` (con más de 400,000 registros de ventas) utilizando Python.
2. **Transformación (Transform):** Limpieza de tipos de datos, parseo de fechas (`parse_dates`), control de anomalías/valores negativos y segmentación focalizada (como el aislamiento de la Tienda 4 para la fase predictiva).
3. **Carga y Consumo (Load / Consumption):** Despliegue de los resultados procesados hacia la capa de visualización de negocio (Excel) y la capa de experimentación algorítmica (Machine Learning).

---

## 🛠️ Stack Tecnológico
* **Lenguaje:** Python 3.x
* **Manipulación y Análisis:** Pandas, NumPy
* **Machine Learning / Series Temporales:** Statsmodels (`ExponentialSmoothing` / Holt-Winters), Scikit-learn
* **Visualización de Datos:** Matplotlib, Seaborn
* **Entorno de Desarrollo:** VS Code, Jupyter Notebooks
* **Herramientas Complementarias:** Microsoft Excel (Dashboards macro)

---
