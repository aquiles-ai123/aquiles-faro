Labels sugeridas: good first issue, help wanted, security, P1

## Contexto
El community_draft puede incluir PII si la evidencia lo trae; necesitamos un filtro básico.

## Objetivo
Agregar un anonimizador simple por regex (emails, teléfonos, IDs) y una nota al inicio del draft.

## Alcance
Incluye:
- Regex para email/teléfono/ID
- Reemplazo con `[REDACTED]`
- Nota al inicio si se aplicó anonimización

No incluye:
- Detección avanzada de PII
- Revisión humana automática

## Criterios de aceptación
- [ ] Detecta emails y teléfonos comunes
- [ ] Reemplaza por `[REDACTED]`
- [ ] Agrega nota “Anonimización aplicada” al inicio

## Cómo verificar
1) Ejecutar `community_draft` con evidencia que contenga emails
2) Verificar que el output redacta datos

## Pistas de implementación
- Aplicar regex antes de escribir el archivo final
- Loguear un evento con `redactions_count`

## Archivos sugeridos
- `docs/spec/05_ethics_safety.md`
- (Implementación) `aquiles/jobs/community_draft.py`
