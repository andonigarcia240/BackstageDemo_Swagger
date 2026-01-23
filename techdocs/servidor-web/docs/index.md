# servidor-web

Backend principal de la plataforma arcade.

## Qué hace
- Expone endpoints REST para operaciones principales (juegos, puntuaciones, etc.).
- Persiste/consulta datos en MongoDB.

## Ownership
- Owner: `team-arcade`
- System: `arcade-platform`

## Repositorio
- Código: ver `backstage.io/source-location` (en el catálogo de Backstage)

## API
- La documentación de endpoints está en la entidad **API**: `servidor-web-api` (OpenAPI).
- Aquí se documentan guías, ejemplos y operación.

## Dependencias
- Resource: `mongo-db`

## Configuración (variables de entorno)
> Ajusta estos nombres a los reales de tu proyecto.
- `PORT` (ej. 3000)
- `MONGO_URL` (ej. mongodb://localhost:27017/arcade)
- `NODE_ENV` (development/production)
- (Opcional) `CORS_ORIGIN`, `JWT_SECRET`, etc.

## Cómo ejecutar en local
1. Levantar MongoDB
2. Instalar dependencias
3. Arrancar el servidor

Ejemplo (orientativo):
- `npm install`
- `npm run dev` o `npm start`

## Healthcheck
- Si tienes endpoint de salud, documenta:
  - `GET /health` → 200 OK

## Observabilidad
- Logs: dónde se ven (console, fichero, plataforma)
- Métricas: (si aplica)
- Trazas: (si aplica)

## Seguridad
- Autenticación/autorización (si aplica)
- CORS / rate limiting (si aplica)

## Operación
- Ver [Runbook](runbook.md) para incidencias típicas.
