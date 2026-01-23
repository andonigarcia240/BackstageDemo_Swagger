# seed-scores

Job que inserta/actualiza datos iniciales de **puntuaciones**.

## Qué hace
- Crea puntuaciones iniciales o estructura base para ranking.
- (Ideal) Idempotente: no duplica entradas.

## Ownership
- Owner: `team-arcade`
- System: `arcade-platform`

## Dependencias
- Resource: `mongo-db`
- (Opcional) Component: `servidor-web` (si opera vía API)

## Cuándo se ejecuta
- Inicialización de entornos
- Migraciones ligeras de datos (si lo usas así)
- Manual bajo demanda

## Configuración (variables de entorno)
> Ajusta a lo real.
- `MONGO_URL`
- (Opcional) `DEFAULT_SCORE=0`
- (Opcional) `DRY_RUN=true|false`

## Cómo ejecutarlo
Ejemplo (orientativo):
- `npm install`
- `npm run seed:scores` (o comando real)

## Qué datos crea/modifica
- Colección: `<scores>` (nombre real)
- Campos: `<playerId>`, `<gameId>`, `<score>`, etc.

## Verificación
- Consultar en Mongo
- Confirmar endpoints en `servidor-web` o `pacman` (si aplican) muestran rankings

## Operación
- Ver [Runbook](runbook.md).
