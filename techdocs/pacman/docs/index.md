# pacman

Servicio relacionado con el juego Pacman (API REST).

## Qué hace
- Expone endpoints REST para iniciar partida / movimientos / estados (según tu implementación).
- Puede depender del backend principal para persistencia o reglas.

## Ownership
- Owner: `team-arcade`
- System: `arcade-platform`

## Repositorio
- Código: ver `backstage.io/source-location`

## API
- La documentación de endpoints está en la entidad **API**: `pacman-api` (OpenAPI).

## Dependencias
- Resource: `mongo-db`
- (Opcional) Component: `servidor-web` (si hace llamadas o comparte lógica/datos)

## Configuración (variables de entorno)
> Ajusta a lo real.
- `PORT`
- `MONGO_URL` (si guarda estado)
- `SERVIDOR_WEB_URL` (si llama al backend)
- `NODE_ENV`

## Cómo ejecutar en local
1. Levantar dependencias (Mongo, servidor-web si aplica)
2. Instalar dependencias
3. Ejecutar servicio

Ejemplo (orientativo):
- `npm install`
- `npm run dev`

## Observabilidad
- Logs: dónde se ven
- Métricas/trazas: (si aplica)

## Operación
- Ver [Runbook](runbook.md).
