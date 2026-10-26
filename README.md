# Showz: análisis de métricas de marketing (LTV, CAC, ROMI)

## Contexto
Showz, una plataforma de venta de entradas para eventos, necesitaba saber en qué fuentes de marketing invertir. Analicé 359,400 visitas, 50,415 pedidos y $329,131 en gastos de marketing.

## Preguntas
1. ¿Cómo usan los clientes el sitio y con qué frecuencia regresan?
2. ¿Cuándo compran, cuánto gastan y cuánto valor generan en el tiempo?
3. ¿Qué fuentes de marketing recuperan su inversión?

## Qué hice
- Limpié y preparé tres tablas (visitas, pedidos, costos): tipos de fecha, nombres de columnas, duplicados.
- Calculé métricas de producto (DAU, WAU, MAU, sticky factor, duración de sesión).
- Construí cohortes mensuales para calcular el LTV.
- Calculé CAC y ROMI por fuente de adquisición.

## Decisiones
- Usé la **mediana** en lugar de la media para la duración de sesión y el ticket, porque ambas distribuciones están fuertemente sesgadas a la derecha.
- Asigné cada cliente a la fuente de su **primera visita** para calcular el CAC.
- Excluí junio de 2018 del análisis de tendencias porque los datos de ese mes estaban incompletos.

## Resultados
- Solo **3 de 7 fuentes son rentables** (ROMI > 1): fuentes 1, 2 y 9.
- La **fuente 3** consume el 42.9% del presupuesto, con el CAC más alto ($15.47) y el ROMI más bajo (0.31).
- El **72% de los clientes compra el mismo día** de su primera visita: la ventana de remarketing más efectiva son los primeros 2 días.
- Ventas con estacionalidad marcada: pico en octubre–diciembre.

**Recomendación:** redirigir presupuesto de la fuente 3 hacia las fuentes 1, 2 y 9, y reforzar la inversión antes de la temporada alta.

## Herramientas
Python · pandas · NumPy · Matplotlib · análisis de cohortes

## Cómo verlo
Abre `showz_business_metrics_analysis.ipynb`. Los CSV de origen estaban en la plataforma de TripleTen y no se incluyen.
