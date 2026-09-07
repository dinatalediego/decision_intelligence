# Operación y verificación

## Gate previo a despliegue

1. Ejecutar `npm run check`.
2. Confirmar que `dist/index.html`, `dist/styles.css` y `dist/app.js` existen.
3. Confirmar 4 laboratorios × 5 gráficos y que cada slider actualiza su capítulo.
4. Revisar los enlaces académicos y el destino del buzón.
5. Comparar `git rev-parse HEAD` con el commit desplegado por Vercel.

## Comparación origen → destino

| Elemento | Origen esperado | Destino esperado |
|---|---|---|
| HTML | `dist/index.html` | `/index.html` |
| Estilos | `dist/styles.css` | `/styles.css` |
| Interacciones | `dist/app.js` | `/app.js` |
| Registros sintéticos | generados en navegador con semilla | idénticos para el mismo control |
| Secretos | ninguno | ninguno |

## Registros rechazados

No hay ingestión de registros en v0.1. Por diseño, se rechaza persistir sugerencias: el usuario elige enviarlas mediante su correo o GitHub. En una futura tabla Supabase, registrar rechazos explícitos por validación, rate-limit y contenido vacío.

## Riesgos pendientes

- Los simuladores enseñan comportamiento estadístico; no entrenan librerías Python reales en el navegador.
- El contenido académico necesita revisión editorial/versionado a medida que crezcan los capítulos.
- El buzón depende de una aplicación de correo o una sesión de GitHub.
- Antes de conectar Supabase: crear migración, RLS, políticas mínimas, anti-spam y prueba de inserción/rechazo en una rama.

## Rollback

Vercel puede volver al deployment anterior sin modificar el historial de Git. El repositorio conserva cada versión trazable por commit.
