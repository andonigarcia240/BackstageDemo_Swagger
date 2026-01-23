# mongo-db

Recurso MongoDB usado por `arcade-platform`.

## Ownership
- Owner: `team-arcade`
- System: `arcade-platform`

## Uso
- Consumido por:
  - `servidor-web`
  - `pacman`
  - `seed-games`
  - `seed-scores`

## Conexión
- Variable típica: `MONGO_URL`
- Ejemplo: `mongodb://localhost:27017/arcade` (ajusta)

## Colecciones esperadas
> Ajusta nombres reales.
- `games`
- `scores`
- (otras)

## Backups / restauración
- Describe el método (si aplica): dump/restore, snapshots, etc.

## Operación
- Monitorizar espacio, índices, conexiones.
