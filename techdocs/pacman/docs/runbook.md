# Runbook — pacman

## Checks rápidos
1. ¿Responde el endpoint de estado/health si existe?
2. ¿Está accesible MongoDB o `servidor-web` si depende de él?
3. ¿Los errores son de reglas de juego o de persistencia?

## Errores comunes
### Fallos al iniciar partida
**Acciones:**
- validar payload requerido
- confirmar que existen datos base (si depende de seeds)
- revisar logs

### Inconsistencias de estado
**Acciones:**
- comprobar si hay estado en memoria vs BD
- reiniciar servicio si es stateless y persiste en BD
- revisar colecciones/índices

## Mitigación / rollback
- volver a versión estable previa
- deshabilitar funcionalidades nuevas (si existe mecanismo)

## Contacto
- Owner: `team-arcade`
