# Runbook — servidor-web

Guía rápida para operar y resolver incidencias.

## Arranque / parada
- Arranque local: `npm run dev` (o comando real)
- Arranque prod: (systemd/docker/k8s) — describe tu caso

## Checks rápidos
1. ¿Responde el healthcheck?
   - `GET /health`
2. ¿Mongo está accesible?
   - probar conexión / revisar `MONGO_URL`
3. ¿Logs muestran error de conexión o auth?

## Errores comunes
### No conecta a MongoDB
**Síntoma:** timeouts, `ECONNREFUSED`, errores de driver  
**Acciones:**
- Verifica que Mongo está levantado
- Revisa `MONGO_URL`
- Revisa red/puertos/credenciales

### 500 al llamar endpoints
**Acciones:**
- Revisa logs del request (payload, stacktrace)
- Comprueba si hay datos iniciales (ejecuta `seed-games` / `seed-scores` si procede)
- Verifica índices/colecciones esperadas

## Rollback / mitigación
- Si el despliegue falla:
  - vuelve a la imagen/commit anterior
  - desactiva feature flag si existe

## Contacto
- Owner: `team-arcade`
