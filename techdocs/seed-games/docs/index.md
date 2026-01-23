# seed-games

Job que inserta/actualiza datos iniciales de **juegos** en la base de datos.

## Qué hace
- Crea juegos iniciales en `mongo-db`.
- (Ideal) Es **idempotente**: si ya existen, no duplica; actualiza o ignora.

## Ownership
- Owner: `team-arcade`
- System: `arcade-platform`

## Dependencias
- Resource: `mongo-db`
- (Opcional) Component: `servidor-web` (si utiliza su API en vez de escribir directo a BD)

## Cuándo se ejecuta
- Manual en local (desarrollo)
- En despliegues iniciales / entornos nuevos
- (Opcional) en pipeline CI/CD o como init job

## Configuración (variables de entorno)
> Ajusta a lo real.
- `MONGO_URL`
- `NODE_ENV`
- (Opcional) `SEED_MODE=upsert|insert`
- (Opcional) `DRY_RUN=true|false`

## Cómo ejecutarlo
Ejemplo (orientativo):
- `npm install`
- `npm run seed:games` (o comando real)

## Qué datos crea/modifica
- Colección: `<games>` (pon el nombre real)
- Campos relevantes: `<name>`, `<genre>`, `<createdAt>`, etc.

## Verificación
- Revisar colección en Mongo
- Confirmar que `servidor-web` lista juegos correctamente (si aplica)

## Operación
- Ver [Runbook](runbook.md).
