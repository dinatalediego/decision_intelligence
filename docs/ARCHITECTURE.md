# Arquitectura de producto

## Principio

La unidad pedagógica no es el algoritmo, sino el contrato de decisión:

`contexto → objetivo → datos → baseline → modelo → incertidumbre → acción → outcome`

## Capítulos v0.1

| Capítulo | Familia | Pregunta | Métrica | Acción |
|---|---|---|---|---|
| Forecast | supervisado/temporal | ¿cuántas separaciones vendrán? | MAE + cobertura | capacidad y meta |
| Churn | supervisado | ¿qué separación podría caer? | calibración + utilidad | rescate priorizado |
| Clustering | no supervisado | ¿qué patrones de demanda existen? | silueta + estabilidad | oferta/mensaje |
| Pricing bandit | reinforcement | ¿qué incentivo probar? | recompensa + regret | política con guardrails |

## Capas

- `index.html`: narrativa, semántica y contenido.
- `styles.css`: sistema visual editorial/inmobiliario responsive.
- `app.js`: generador sintético, SVG, estado de simuladores y buzón.
- `setInsights()`: capa interpretativa determinística que traduce cada escenario a lectura, funcionamiento del modelo y criterio de decisión sin antropomorfizarlo ni inferir causalidad.
- `tests/`: criterios de aceptación estructurales, seguridad y completitud.

La v0.1 es estática para minimizar costo y superficie de riesgo. Supabase queda diferido hasta que exista una necesidad real de progreso multiusuario, comentarios persistentes o edición de contenidos.
