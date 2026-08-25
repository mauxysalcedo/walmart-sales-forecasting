# 📈 Pronóstico de Ventas Semanales - Walmart
**Curso:** Prospectiva Tecnológica y Producción Inteligente  
**Dataset:** Walmart Recruiting - Store Sales Forecasting (Kaggle)

---

## 📋 Descripción General
Este proyecto implementa un flujo completo de análisis de datos y pronóstico de demanda de ventas semanales (`Weekly_Sales`). El trabajo se divide en **dos partes fundamentales**: un análisis macroeconómico y de negocio, y una extensión técnica de Machine Learning para series temporales.

---

## 🗂️ Estructura del Proyecto: Dos Partes

### Parte 1: Análisis Macro y Selección de Tiendas (Dashboard en Excel / Python)
* **Objetivo:** Analizar el comportamiento macro de las tiendas con mayor volumen de ventas para identificar tendencias y estacionalidades.
* **Criterio de Selección:** Se evaluaron las tiendas con mayor historial y se seleccionó específicamente la **Tienda 4** debido a su alta estabilidad operativa y a la **menor presencia de ruido, valores atípicos y registros negativos** por devoluciones masivas.
* **Herramientas:** Procesamiento inicial en Python (Pandas) para estructurar los datos que alimentan un dashboard analítico.

### Parte 2: Modelado Predictivo y Machine Learning (Python / Series Temporales)
* **Objetivo:** Extender el análisis a nivel de departamento (`Dept`) para predecir la demanda futura.
* **Metodología:** Entrenamiento de modelos de series temporales (como Holt-Winters) para el pronóstico de ventas semanales.
* **Manejo de Datos:** Tratamiento preventivo de valores negativos y estacionalidades por departamento para evitar distorsiones en las proyecciones.

---

## 🛠️ Arquitectura de Datos y Pipeline (ETL)
El flujo de datos sigue una arquitectura estructurada en tres fases:
1. **Extracción (Extract):** Carga del dataset masivo (`train.csv`) usando Python y Pandas.
2. **Transformación (Transform):** Limpieza de fechas, agregaciones por tienda/fecha y filtrado de la Tienda 4.
3. **Carga y Consumo (Load / Consumption):** Exportación de datos procesados hacia el dashboard en Excel y los scripts de Machine Learning en Jupyter Notebooks.

---

## 🧰 Stack Tecnológico
* **Lenguaje:** Python 3.x
* **Manipulación y Análisis:** Pandas, NumPy
* **Visualización:** Matplotlib, Seaborn
* **Machine Learning / Series Temporales:** Statsmodels (Holt-Winters), Scikit-learn
* **Entorno:** VS Code, Jupyter Notebooks
* **Visualización de Negocio:** Excel

---
