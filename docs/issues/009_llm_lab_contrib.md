Labels sugeridas: good first issue, help wanted, docs, llm_lab, P1

## Contexto
No hay una guía para agregar nuevas suites de evaluación al LLM Lab.

## Objetivo
Documentar cómo agregar una suite nueva: prompts, métricas, y formato de salida.

## Alcance
Incluye:
- Estructura sugerida de prompts
- Cómo medir TTFT/tokens/s
- Cómo actualizar `leaderboard.md`

No incluye:
- Implementación de nuevos modelos
- CI automatizado

## Criterios de aceptación
- [ ] Guía con pasos claros
- [ ] Ejemplo mínimo de suite
- [ ] Referencias a archivos existentes

## Cómo verificar
1) Seguir la guía para agregar una suite ficticia
2) Verificar que la documentación es suficiente

## Pistas de implementación
- Incluir ejemplo con 2 prompts
- Definir campos obligatorios

## Archivos sugeridos
- `docs/spec/04_llm_lab.md`
- `CONTRIBUTING.md`
