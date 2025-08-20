Informe de Análisis de Cancelación de Clientes – Telecom X
🎯 Objetivo

Identificar los factores que más influyen en la cancelación de clientes (Churn) y evaluar modelos predictivos que permitan anticipar qué usuarios tienen mayor riesgo de cancelar sus servicios.

🔎 Resultados de Modelado

Se entrenaron dos modelos con el dataset procesado:

1. Regresión Logística (con normalización)

Accuracy: 79.84%

Precision: 64.15%

Recall: 54.55%

F1-score: 58.96%

👉 Buen balance entre precisión y recall, especialmente útil para detectar clientes en riesgo (recall superior a Random Forest).

2. Random Forest (sin normalización)

Accuracy: 77.80%

Precision: 60.13%

Recall: 48.66%

F1-score: 53.79%

👉 Rendimiento competitivo, aunque ligeramente inferior en recall y F1. Puede beneficiarse de ajuste de hiperparámetros.

📌 Principales Factores que Influyen en la Cancelación
🔹 Variables destacadas en Regresión Logística (coeficientes)

Aumentan la probabilidad de cancelación:

CargosTotales (facturación acumulada alta)

TipoInternet_Fiber optic

FacturaDigital

MetodoPago_Electronic check

Disminuyen la probabilidad de cancelación:

MesesContrato (antigüedad)

TipoContrato_Two year y One year (compromisos largos)

TipoInternet_No (clientes sin internet)

Cuentas_Diarias

🔹 Variables más importantes en Random Forest (importancia)

CargosTotales

MesesContrato

Cuentas_Diarias

CargosMensuales

TipoInternet_Fiber optic

MetodoPago_Electronic check

Total_Servicios

TipoContrato_Two year

FacturaDigital

Genero_Male

👉 Coincidencia clara: facturación, antigüedad, tipo de internet, contrato y método de pago son las variables más influyentes.

⚖️ Diagnóstico de los Modelos

Overfitting: No se evidencia de forma grave, aunque Random Forest podría beneficiarse de regularización (limitando profundidad de árboles y ajustando muestras mínimas por división).

Underfitting: La Regresión Logística podría mejorar recall si se ajusta el parámetro de regularización (C) o si se aplican pesos balanceados para la clase minoritaria (clientes que cancelan).

💡 Estrategias de Retención Propuestas

Migración de contrato mensual a anual/bienal: Ofrecer descuentos o beneficios por permanencia.

Control de costos para clientes con facturación alta: Programas de optimización de plan y alertas por aumentos en la factura.

Atención temprana a clientes nuevos (0–90 días): campañas de onboarding, encuestas NPS iniciales, soporte prioritario.

Incentivar métodos de pago más seguros (tarjeta de crédito/autopago) para reducir riesgo asociado a pagos con Electronic check.

Mejorar experiencia en clientes de fibra óptica: garantizar SLA, soporte proactivo, upgrades de velocidad.

Paquetes de servicios adicionales (Bundles): integrar soporte técnico, respaldo en línea o TV para aumentar fidelidad.

✅ Conclusión

La cancelación en Telecom X está fuertemente relacionada con antigüedad, facturación, tipo de internet, tipo de contrato y método de pago.
El modelo más prometedor en esta etapa es la Regresión Logística, al equilibrar precisión y recall, aunque Random Forest puede mejorar con tuning.

La empresa puede reducir el churn mediante estrategias de permanencia, gestión de facturación y fortalecimiento de la experiencia digital y de soporte.
