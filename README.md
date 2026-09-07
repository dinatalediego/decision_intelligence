# Decision Intelligence Academy

Portal educativo interactivo que enseña ciencia de datos como un ciclo de decisión: evidencia → modelo → acción → resultado → aprendizaje.

## Alcance v0.1

- 4 capítulos: forecasting, churn con XGBoost, clustering con K-means y pricing con contextual bandits.
- 5 gráficos por capítulo (20 en total), generados con SVG y datos sintéticos determinísticos.
- Controles interactivos para horizonte, estacionalidad, umbral, hiperparámetros, número de clusters, exploración y guardrails.
- Ruta de 8 semanas hacia un rol de Decision Intelligence.
- Biblioteca académica primaria y buzón que prepara correo/issue sin almacenar datos personales.

## Ejecutar

El sitio es estático. Sirve la carpeta `dist/` con cualquier servidor HTTP local o impórtalo en Vercel; `vercel.json` ya apunta a esa carpeta.

```bash
npm test
npm run check
```

## Datos y privacidad

Todos los registros son sintéticos y reproducibles. No existe conexión a Supabase, CRM o data warehouse en esta versión. El buzón usa `mailto:` o GitHub Issues y no persiste contenido en el portal.

## Despliegue

En Vercel: importar `dinatalediego/decision_intelligence`, mantener Framework Preset en `Other` y publicar. No requiere variables de entorno ni plan de pago.

Consulta [docs/OPERATIONS.md](docs/OPERATIONS.md) para verificación y riesgos.
