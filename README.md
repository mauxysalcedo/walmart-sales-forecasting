# 🛒 Walmart Store Sales Forecasting

## 📝 Descripción del Proyecto
Este repositorio contiene un proyecto académico de análisis de datos y machine learning desarrollado para predecir las ventas semanales de las tiendas Walmart. El objetivo principal es aplicar modelos predictivos sobre datos históricos (Kaggle) para facilitar la toma de decisiones y la prospectiva de la demanda.

A través de un análisis exhaustivo de más de 420,000 registros, el proyecto se enfoca en la **Tienda 4**, seleccionada por su alto volumen de ventas (segundo lugar general con ~$299.5M) y la excelente calidad/limpieza de sus datos (cero registros con ventas nulas).

---

## 🛠️ Tecnologías y Herramientas Utilizadas
* **Lenguaje:** Python 🐍
* **Manipulación de Datos:** Pandas, NumPy
* **Machine Learning:** Scikit-learn (Random Forest, Histogram Gradient Boosting)
* **Visualización:** Matplotlib, Seaborn
* **Entorno:** Jupyter Notebook / Anaconda
* **Dashboards:** Excel (para reportes ejecutivos)

---

## 🧠 Metodología y Modelado
1. **Feature Engineering:** Se crearon variables temporales (semana del año, mes, año) y variables de rezago (`venta_semana_anterior`) para capturar la estacionalidad de las ventas.
2. **División de Datos:** Se utilizó la fecha `"2012-06-01"` como punto de corte cronológico para separar los conjuntos de entrenamiento (`train`) y prueba (`test`).
3. **Modelos Evaluados:**
   * *Random Forest Regressor*
   * *Histogram Gradient Boosting Regressor*

---

## 📊 Resultados Clave
El modelo **Histogram Gradient Boosting** demostró un rendimiento superior, logrando un mejor ajuste a los datos reales agregados por semana:

| Métrica Evaluada | Random Forest | Histogram Gradient Boosting |
| :--- | :--- | :--- |
| **RMSE** (Raíz del Error Cuadrático Medio) | $68,156.40 | **$60,343.19** |
| **MAPE** (Error Porcentual Absoluto Medio) | 2.64% | **2.45%** |

*Nota: Una tasa de error del 2.45% en forecasting de ventas al por menor representa un modelo altamente preciso y viable para aplicaciones del mundo real.*
