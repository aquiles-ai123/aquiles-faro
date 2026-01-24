Labels sugeridas: good first issue, help wanted, llm_lab, P1

## Contexto
Usuarios CPU-only no saben qué modelos y valores usar para estabilidad y latencia.

## Objetivo
Definir un “CPU preset” de configuración + guía de modelos recomendados (1B–3B).

## Alcance
Incluye:
- Preset de env recomendado (max_tokens, timeouts, modelos)
- Lista corta de modelos (1B–3B) y notas
- Documentación en `docs/spec/04_llm_lab.md`

No incluye:
- Benchmark exhaustivo en hardware variado
- Comparativas GPU

## Criterios de aceptación
- [ ] Se agrega sección “CPU preset” en docs
- [ ] Incluye valores recomendados y justificación breve
- [ ] Lista de 2–4 modelos con pros/cons

## Cómo verificar
1) Revisar la sección en `docs/spec/04_llm_lab.md`
2) Confirmar valores claros y copy/paste-ready

## Pistas de implementación
- Basarse en tiempos típicos de modelos 1B–3B
- Priorizar estabilidad sobre calidad

## Archivos sugeridos
- `docs/spec/04_llm_lab.md`
- `README.md`
