# arcade-platform

Sistema que agrupa las APIs y Jobs de la plataforma arcade.

## Componentes
- **APIs**
  - `servidor-web`: backend principal REST
  - `pacman`: servicio REST de Pacman
- **Jobs**
  - `seed-games`: inicializa/siembra juegos
  - `seed-scores`: inicializa/siembra puntuaciones
- **Recursos**
  - `mongo-db`: base de datos MongoDB

## Responsables
- Owner: `team-arcade`

## Flujos típicos
1. `servidor-web` expone endpoints de negocio y opera contra `mongo-db`.
2. `pacman` se apoya en `servidor-web` (si aplica) y/o en `mongo-db`.
3. Jobs (`seed-games`, `seed-scores`) cargan datos iniciales en `mongo-db` (idealmente idempotentes).

## Cómo empezar (dev)
- Levanta MongoDB
- Arranca `servidor-web`
- Arranca `pacman`
- Ejecuta seeds cuando sea necesario (`seed-games` / `seed-scores`)
