# Predicción de Churn de Clientes – Interconnect

## Descripción del proyecto
Este proyecto tiene como objetivo predecir la cancelación de clientes (churn) para la empresa de telecomunicaciones Interconnect. El modelo permite identificar clientes con alto riesgo de abandono para apoyar campañas de retención mediante promociones y planes personalizados.

## Objetivo del negocio
El objetivo principal es anticipar qué clientes tienen mayor probabilidad de cancelar el servicio, permitiendo al equipo de marketing priorizar acciones preventivas y reducir la tasa de churn.

## Datos utilizados
Se utilizaron datos históricos de clientes provenientes de múltiples fuentes:

- contract.csv: información contractual
- personal.csv: datos demográficos
- internet.csv: servicios de internet contratados
- phone.csv: servicios telefónicos

Los datos fueron integrados mediante el identificador único `customerID`.
La variable objetivo se definió como `churn`, derivada de la columna `EndDate`.

## Metodología
El análisis incluyó limpieza de datos, ingeniería de variables, codificación de variables categóricas y separación de datos mediante un esquema estratificado.

Se aplicó un enfoque de validación realista, priorizando la métrica AUC-ROC debido al desbalance de clases. Adicionalmente, se calibraron las probabilidades para mejorar la interpretabilidad del modelo en escenarios de negocio.

## Modelos evaluados
Se evaluaron distintos modelos de clasificación, incluyendo:

- Regresión Logística
- Random Forest
- Gradient Boosting
- HistGradientBoosting

El modelo final fue seleccionado en función de su desempeño y estabilidad en validación.

## Resultados
El mejor modelo fue HistGradientBoosting con calibración isotónica de probabilidades.

- AUC-ROC: 0.885
- Accuracy: 0.837
- Brier Score: 0.1128

La calibración permitió obtener probabilidades más confiables, facilitando la priorización de clientes según su nivel de riesgo.

## Conclusiones
El modelo desarrollado permite identificar clientes con alta probabilidad de churn de forma precisa y accionable. 

Los resultados pueden utilizarse para diseñar campañas de retención basadas en umbrales de riesgo y priorización por probabilidad, aportando valor directo al negocio y reduciendo costos asociados a la pérdida de clientes.

## Tecnologías utilizadas
- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Joblib

