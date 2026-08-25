# 📈 Pronóstico de Ventas Semanales - Walmart
**Curso:** Prospectiva Tecnológica y Producción Inteligente  
**Dataset:** Walmart Recruiting - Store Sales Forecasting (Kaggle)

---

## 📋 Descripción del Proyecto
Este proyecto implementa un modelo de análisis de datos y pronóstico de demanda de ventas semanales (`Weekly_Sales`) utilizando Python y librerías de Machine Learning. El objetivo principal es analizar el comportamiento macro de las tiendas con mayor volumen comercial y proyectar la demanda futura a nivel de departamento para optimizar la planificación logística y de inventarios.

---

## 🛠️ Arquitectura de Datos y Pipeline (ETL)
El flujo de datos sigue una arquitectura analítica estructurada en tres fases principales:

1. **Extracción (Extract):** Carga y lectura del dataset masivo (`train.csv`) utilizando **Python** y **Pandas**.
2. **Transformación y Limpieza (Transform):** 
   * Limpieza y formato de fechas (`parse_dates`).
   * Agrupamiento de ventas por tienda y fecha (`groupby`).
   * **Criterio de Selección de Tiendas:** Se evaluaron las tiendas con mayor volumen histórico y se seleccionó específicamente la **Tienda 4** debido a su alta estabilidad operativa y a la **menor presencia de ruido, valores atípicos y registros negativos** por devoluciones masivas, lo que garantiza una mayor calidad en el entrenamiento de los modelos predictivos.
3. **Carga y Consumo (Load / Consumption):** Exportación de los datos procesados para alimentar un dashboard analítico en **Excel** y la capa de modelado predictivo en **Jupyter Notebooks**.

---

## 🧰 Stack Tecnológico
* **Lenguaje:** Python 3.x
* **Manipulación y Análisis de Datos:** Pandas, NumPy
* **Visualización:** Matplotlib, Seaborn
* **Machine Learning / Series Temporales:** Statsmodels (Holt-Winters), Scikit-learn
* **Entorno de Trabajo:** VS Code, Jupyter Notebooks
* **Herramientas de Apoyo:** Excel (para visualización macro de negocio)

---

## 🚀 Estructura del Notebook
* **Parte 1:** Análisis macroeconómico y de tendencia de las tiendas Top (con foco en la Tienda 4).
* **Parte 2:** Extensión de Machine Learning y pronóstico de series temporales a nivel de departamento (`Dept`).

---
