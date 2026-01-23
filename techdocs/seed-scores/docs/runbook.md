# Runbook — seed-scores

## Problemas típicos
### Rankings vacíos tras seed
**Acciones:**
- confirmar que el seed realmente inserta (logs)
- revisar colección objetivo
- comprobar filtros (ej. requiere games existentes → ejecutar antes `seed-games`)

### Datos inconsistentes
**Acciones:**
- asegurar orden de ejecución (games antes de scores)
- validar referencias (`gameId`, `playerId`)
- añadir validaciones y upserts

## Rollback
- Borrar registros “seed” por criterio (tag/seedVersion)
- Restaurar backup si aplica

## Contacto
- Owner: `team-arcade`
