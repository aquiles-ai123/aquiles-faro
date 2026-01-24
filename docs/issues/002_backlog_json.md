Labels sugeridas: good first issue, help wanted, jobs, P1

## Contexto
El backlog actual es solo Markdown, lo que dificulta integraciones futuras y métricas automáticas.

## Objetivo
Generar un `backlog.json` junto al Markdown con una estructura estable y consumible.

## Alcance
Incluye:
- Export JSON con tareas pequeñas, épica, riesgos, métrica
- Mantener el Markdown existente
- Documentar el formato JSON en `docs/spec/03_jobs.md`

No incluye:
- API pública de lectura
- Cambios a la lógica de generación del backlog

## Criterios de aceptación
- [ ] Se crea `runtime/reports/backlog_YYYY-MM-DD.json`
- [ ] Contiene campos: `tasks`, `epic`, `risks`, `metric`, `generated_at`
- [ ] El job sigue produciendo el `.md` actual
- [ ] El formato está documentado

## Cómo verificar
1) Ejecutar `nightly_backlog`
2) Verificar existencia y validez de JSON
3) Validar que el `.md` continúa igual

## Pistas de implementación
- Parsear el texto o generar JSON directamente desde el prompt
- Versionar el esquema con un campo `schema_version`

## Archivos sugeridos
- `docs/spec/03_jobs.md`
- (Implementación) `aquiles/jobs/nightly_backlog.py` en el repo de runtime
