# Predicción de Abandono de Clientes (Churn) - Telco

## 📋 Descripción del proyecto

Proyecto de clasificación binaria orientado a predecir el abandono de clientes (`Churn`) en una empresa de telecomunicaciones. El objetivo es identificar a los clientes con alta probabilidad de abandonar el servicio, permitiendo a la empresa diseñar estrategias de retención basadas en datos.

## 🎯 Objetivo de negocio

- Identificar las variables que más influyen en el churn.
- Construir un modelo con alta capacidad de detección de clientes en riesgo.
- Comparar modelos y seleccionar el más adecuado según métricas relevantes para el negocio.
- Traducir los hallazgos del modelo en recomendaciones de retención.

## 📊 Dataset

[Telco Customer Churn - Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

7,043 registros y 21 variables, incluyendo información demográfica, servicios contratados, tipo de contrato y facturación.

## 🔧 Flujo del proyecto

1. **EDA** — análisis exploratorio de variables numéricas y categóricas, identificación de patrones de churn.
2. **Limpieza de datos** — corrección de tipado en `TotalCharges`, tratamiento de valores nulos y de categorías redundantes.
3. **Encoding** — codificación binaria de la variable objetivo y One-Hot Encoding del resto de variables categóricas.
4. **Escalado** — estandarización de variables numéricas (StandardScaler), evitando data leakage.
5. **Modelado** — entrenamiento y comparación de Regresión Logística y Random Forest.
6. **Ajuste** — manejo del desbalance de clases mediante `class_weight='balanced'`.
7. **Conclusión ejecutiva** — análisis de coeficientes y recomendaciones de negocio.

## 🤖 Modelos y resultados

| Modelo | ROC-AUC | Recall (Churn) | Precisión (Churn) |
|---|---|---|---|
| Regresión Logística | 0.836 | 0.57 | 0.65 |
| Random Forest | 0.819 | 0.49 | 0.63 |
| Regresión Logística (balanceada) | 0.835 | 0.80 | 0.49 |

El modelo balanceado fue seleccionado como el más adecuado para el objetivo del negocio, priorizando la detección de clientes en riesgo (recall) sobre la exactitud global.

## 🔑 Principales factores identificados

**Aumentan el churn:**
- Servicio de internet por fibra óptica
- Cargos totales acumulados altos
- Pago mediante cheque electrónico
- Servicios de streaming

**Reducen el churn:**
- Contratos de uno y dos años
- Mayor antigüedad del cliente (tenure)
- Servicios de soporte técnico y seguridad en línea

## 💡 Recomendaciones de negocio

- Incentivar la migración a contratos de largo plazo.
- Investigar las causas de insatisfacción en clientes con fibra óptica.
- Fortalecer el onboarding y seguimiento en los primeros meses de servicio.
- Promover servicios de valor agregado (soporte técnico, seguridad, respaldo).
- Monitorear clientes que pagan con cheque electrónico como segmento de riesgo.

## 🛠️ Tecnologías utilizadas

- Python (Pandas, NumPy)
- Scikit-learn
- Matplotlib, Seaborn, Plotly
- Google Colab


##  Autor

Juan Pablo Holguín Mejía — Economista | Data Analyst
