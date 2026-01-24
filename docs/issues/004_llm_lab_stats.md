Labels sugeridas: good first issue, help wanted, llm_lab, P1

## Contexto
El leaderboard actual es un snapshot simple. Para comparar modelos, necesitamos percentiles y un historial.

## Objetivo
Mejorar el leaderboard con p50/p95 de TTFT y tokens/s, y guardar histórico en JSONL.

## Alcance
Incluye:
- Cálculo de p50/p95 por modelo
- Archivo histórico `runtime/leaderboard_history.jsonl`
- Documentación en `docs/spec/04_llm_lab.md`

No incluye:
- Dashboard web
- Agregaciones multi-host

## Criterios de aceptación
- [ ] Leaderboard muestra p50/p95 TTFT y tokens/s
- [ ] Se agrega una línea por run en `leaderboard_history.jsonl`
- [ ] Se documenta el formato del historial

## Cómo verificar
1) Ejecutar `llm_bench` dos veces
2) Verificar actualización del leaderboard
3) Verificar historial JSONL con dos líneas

## Pistas de implementación
- Usar percentiles con ordenamiento simple (sin libs extra)
- Incluir `run_id`, `model`, `timestamp`, `metrics`

## Archivos sugeridos
- `docs/spec/04_llm_lab.md`
- (Implementación) `aquiles/jobs/llm_bench.py` en el repo de runtime
