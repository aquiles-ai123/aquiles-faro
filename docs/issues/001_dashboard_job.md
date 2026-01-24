Labels sugeridas: good first issue, help wanted, jobs, P1

## Contexto
Hoy no hay un resumen único del estado de jobs; hay que revisar varios archivos para entender qué corrió y qué falló.

## Objetivo
Agregar un job "dashboard" que escriba un resumen en `runtime/dashboard.md` con el estado reciente de los jobs.

## Alcance
Incluye:
- Nuevo job que lee `runtime/hub/events.jsonl`
- Output en `runtime/dashboard.md`
- Documentación del job en `docs/spec/03_jobs.md`

No incluye:
- UI web o panel interactivo
- Persistencia en base de datos

## Criterios de aceptación
- [ ] Se genera `runtime/dashboard.md` con fecha y hora
- [ ] Incluye últimas ejecuciones de `daily_digest`, `nightly_backlog`, `community_draft`, `llm_bench`
- [ ] Muestra status (ok/warn/error) y duración cuando esté disponible
- [ ] El job no falla si `events.jsonl` está vacío

## Cómo verificar
1) Ejecutar el job
2) Confirmar que `runtime/dashboard.md` existe y tiene secciones por job
3) Forzar un error y verificar que se refleje el status

## Pistas de implementación
- Parsear las últimas N líneas de `events.jsonl` y agrupar por job
- Estructura simple en Markdown

## Archivos sugeridos
- `docs/spec/03_jobs.md`
- `docs/spec/02_architecture.md`
- (Implementación) `aquiles/jobs/dashboard.py` en el repo de runtime
