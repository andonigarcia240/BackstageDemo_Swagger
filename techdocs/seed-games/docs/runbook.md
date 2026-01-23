# Runbook — seed-games

## Problemas típicos
### Se ejecuta y no inserta nada
**Causas:**
- ya existían registros y el seed es idempotente
- el filtro de “ya existe” está mal
- no conecta a Mongo

**Acciones:**
- revisa logs del job
- valida `MONGO_URL`
- comprueba si está en modo `upsert` o `insert`

### Duplicados en la colección
**Acciones:**
- revisar si falta índice único (por ejemplo por `gameId` o `name`)
- ajustar seed a `upsert`
- limpiar duplicados con script controlado

## Rollback
- Si el seed mete datos incorrectos:
  - borrar por criterio (tag, campo `seedVersion`, etc.)
  - o restaurar backup si aplica

## Contacto
- Owner: `team-arcade`
