# Challenge_Telecom_X_Vol_2
Alura LATAM's challenge telecom x part 2 
1. Modelo Seleccionado

El modelo seleccionado fue Regresión Logística con ajuste de clases (class_weight='balanced').

Aunque en el reporte de clasificación el desempeño puede parecer moderado, el análisis mediante la matriz de confusión demuestra un comportamiento equilibrado y consistente para la predicción de cancelación (churn).

Métricas principales

Accuracy: 0.80

Precision (Yes): 0.65

Recall (Yes): 0.52

F1-score (Yes): 0.58

El modelo logra identificar correctamente aproximadamente el 52% de los clientes que cancelan, manteniendo una precisión del 65% en las predicciones positivas.

En comparación con otros modelos evaluados:
KNN
Random Forest
Decision Tree

La regresión logística presentó el mejor equilibrio entre interpretación, estabilidad y desempeño general.

Además, al utilizar class_weight='balanced', el modelo evitó el sesgo hacia la clase mayoritaria, mejorando la detección de clientes que cancelan.

2. Variables Más Relevantes

El análisis de importancia de variables (Permutation Importance) identificó los siguientes factores como los principales determinantes de cancelación:

Tenure

InternetService_Fiber optic

ChargesMonthly

Contract_One year

Interpretación de Variables:
Tenure (Antigüedad del cliente)

Es la variable más influyente en el modelo.

Clientes con menor tiempo utilizando el servicio presentan mayor probabilidad de cancelar.
A medida que aumenta la antigüedad, la probabilidad de churn disminuye significativamente.

Esto sugiere que el abandono ocurre principalmente en las primeras etapas del ciclo de vida del cliente.

InternetService – Fiber Optic
El tipo de servicio influye directamente en la probabilidad de cancelación.
El servicio de fibra óptica suele estar asociado a mayores costos mensuales, lo que puede aumentar las expectativas del cliente y generar mayor sensibilidad ante problemas de precio o calidad.

ChargesMonthly (Cargo mensual)

Existe una relación directa entre mayor costo mensual y mayor probabilidad de cancelación.
Clientes con cargos mensuales elevados tienden a abandonar el servicio con mayor frecuencia, especialmente si perciben que el valor recibido no compensa el costo.
Este factor está relacionado con el tipo de servicio contratado (por ejemplo, fibra óptica).

Contract – One Year

Los contratos de mayor duración reducen significativamente la probabilidad de cancelación.
Los clientes con contratos anuales presentan mayor estabilidad y permanencia en comparación con los contratos mensuales.
Esto confirma que la estructura contractual influye directamente en la retención.

3. Propuestas Estratégicas

Con base en los resultados del modelo, se proponen las siguientes estrategias para reducir la tasa de cancelación:

1️⃣ Incentivos en los primeros meses

Dado que el churn es más alto en clientes nuevos:

Ofrecer beneficios durante los primeros 1–3 meses.

Descuentos temporales.

Programas de acompañamiento o soporte prioritario.

Objetivo: reducir el abandono temprano.

2️⃣ Optimización del valor percibido

Dado que el precio y la fibra óptica influyen en la cancelación:

Incluir beneficios adicionales (almacenamiento en la nube, mejoras de velocidad, mayor capacidad de datos).

Ofrecer planes escalonados según consumo real.

Ajustar paquetes para mejorar percepción costo–beneficio.

3️⃣ Rediseño de contratos

Considerando que los contratos largos reducen churn:

Incentivar migración de planes mensuales a contratos anuales.

Ofrecer descuentos por permanencia.

Evaluar la sustitución del contrato mensual por planes flexibles basados en consumo.

Conclusión

El modelo de regresión logística demuestra que la cancelación en Telecom X está principalmente determinada por:
Antigüedad del cliente
Tipo de servicio contratado
Costo mensual
Duración del contrato

Los resultados muestran que el churn es un fenómeno estructural asociado a permanencia y precio, más que a servicios complementarios.

El modelo es interpretable, consistente con la lógica de negocio y adecuado para la toma de decisiones estratégicas orientadas a la retención de clientes.
