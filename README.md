# 📈 Pronóstico de Ventas Semanales - Walmart
**Asignatura:** Prospectiva Tecnológica y Producción Inteligente  
**Dataset:** Walmart Recruiting - Store Sales Forecasting (Kaggle)

---

## 📋 Descripción General del Proyecto
Este repositorio contiene el desarrollo completo de un ejercicio analítico y predictivo orientado a la gestión de la demanda minorista (`Weekly_Sales`). El proyecto está estructurado metodológicamente en **dos partes complementarias**: un análisis macro de negocio y una extensión técnica de Machine Learning aplicada a series temporales.

---

## 🗂️ Estructura y Desarrollo por Partes

### Parte 1: Análisis Macro, Agregación y Selección de las Top 5 Tiendas
* **Objetivo:** Analizar el comportamiento macroeconómico y la estacionalidad de las tiendas con mayor volumen de facturación histórica para comprender los patrones globales de venta.
* **Proceso y Alcance:**
  * **Carga y Exploración Masiva:** Ingesta inicial del dataset completo (`train.csv` con más de 421,000 registros) utilizando Python y Pandas para evaluar rangos de fechas, tipos de datos y consistencia general.
  * **Identificación del Top 5 de Tiendas:** Agrupamiento y ordenamiento de las ventas semanales por tienda (`Store` y `Date`) para aislar y perfilar **las 5 tiendas con mayor volumen total de ventas** en todo el historial.
  * **Integración con Dashboard (Excel):** Estructuración y exportación de los datos procesados de estas sucursales principales para alimentar un tablero de control gerencial en **Excel**, facilitando la visualización visual de tendencias macro y picos estacionales globales.

### Parte 2: Modelado Predictivo y Machine Learning (Foco en Tienda 4)
* **Objetivo:** Desplegar modelos de pronóstico de demanda a un nivel de granularidad mayor (**por departamento / `Dept`**).
* **Criterio de Selección (Tienda 4):** Dentro del análisis de sucursales, se seleccionó específicamente la **Tienda 4** para esta fase de modelado. Esta decisión estratégica se tomó tras verificar que presenta una alta estabilidad operativa y una **mínima presencia de ruido, valores atípicos y registros negativos** por devoluciones masivas, lo cual evita distorsiones críticas en los algoritmos de predicción.
* **Metodología y Herramientas:** Implementación de modelos de series temporales (como *Holt-Winters* / *Exponential Smoothing*) en entornos de Jupyter Notebook para anticipar el comportamiento futuro de la demanda por departamento.

---

## 🔄 Arquitectura de Datos y Pipeline (ETL)
El flujo de la información sigue una arquitectura analítica estándar:
1. **Extracción (Extract):** Ingesta del archivo masivo `train.csv` utilizando Python.
2. **Transformación (Transform):** Limpieza de tipos de datos, parseo de fechas (`parse_dates`), control de anomalías, agregación de las Top 5 tiendas y segmentación focalizada de la Tienda 4 para la fase predictiva.
3. **Carga y Consumo (Load / Consumption):** Despliegue de los resultados procesados hacia la capa de visualización de negocio (Excel) y la capa de experimentación algorítmica (Machine Learning).

---

## 🛠️ Stack Tecnológico
* **Lenguaje:** Python 3.x
* **Manipulación y Análisis:** Pandas, NumPy
* **Machine Learning / Series Temporales:** Statsmodels (`ExponentialSmoothing` / Holt-Winters), Scikit-learn
* **Visualización de Datos:** Matplotlib, Seaborn
* **Entorno de Desarrollo:** VS Code, Jupyter Notebooks
* **Herramientas Complementarias:** Microsoft Excel (Dashboards macro de negocio)

---
