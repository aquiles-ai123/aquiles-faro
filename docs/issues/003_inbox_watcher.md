Labels sugeridas: good first issue, help wanted, jobs, P1

## Contexto
Hoy el inbox depende de cargas manuales; falta un watcher simple que incorpore archivos automáticamente.

## Objetivo
Agregar un watcher de inbox con polling simple que detecte nuevos archivos y los registre en eventos.

## Alcance
Incluye:
- Polling de carpeta `runtime/inbox/`
- Registro de eventos `inbox_added`
- Documentación del watcher

No incluye:
- Watcher avanzado por inotify
- OCR o parsing de PDFs

## Criterios de aceptación
- [ ] Detecta archivos nuevos sin intervención
- [ ] Escribe evento en `events.jsonl`
- [ ] No duplica registros en reinicios
- [ ] Documentado en `docs/spec/02_architecture.md`

## Cómo verificar
1) Iniciar watcher
2) Copiar un archivo al inbox
3) Verificar evento en `events.jsonl`

## Pistas de implementación
- Mantener un registro simple de hashes recientes
- Intervalo configurable por env

## Archivos sugeridos
- `docs/spec/02_architecture.md`
- (Implementación) `aquiles/watchers/inbox.py` en el repo de runtime
