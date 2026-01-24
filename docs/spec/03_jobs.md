# 03 — Jobs

## daily_digest
- **Inputs**: archivos recientes del inbox.
- **Output**: `runtime/reports/daily_digest_YYYY-MM-DD.md`.
- **Uso**: resumen diario basado en evidencia.

## nightly_backlog
- **Inputs**: `runtime/hub/events.jsonl` (eventos recientes).
- **Output**: `runtime/reports/backlog_YYYY-MM-DD.md`.
- **Uso**: backlog accionable con riesgos y métricas.

## community_draft
- **Inputs**: último digest y backlog.
- **Output**: `runtime/reports/community_draft_YYYY-MM-DD.md`.
- **Uso**: borrador publicable, CPU-friendly.

## llm_bench
- **Inputs**: suite de prompts.
- **Output**: `runtime/leaderboard.md`.
- **Uso**: medir TTFT, tokens/s y estabilidad.

## Programación (systemd timers)
- Jobs se pueden disparar con timers `systemd --user`.
- Alternativamente, se ejecutan manualmente con `python -m aquiles.jobs.run <job>`.

## Manejo de fallos
- Reintentos puntuales por job (cuando aplique).
- En errores, el sistema registra `status=warn` y continúa.
- No hay crash global del worker.
