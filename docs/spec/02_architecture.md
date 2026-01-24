# 02 — Arquitectura

## Componentes
- **Control plane**: API para inbox y tareas.
- **Worker**: ejecuta jobs y escribe artefactos.
- **Runtime**: directorio de trabajo (inbox, reports, community, chat, hub).
- **Ledger**: logs JSONL append-only (auditoría).
- **LLM router/cache**: selecciona modelos fast/best y cachea respuestas.

## Flujo
**inbox → jobs → reports → community**
1) Ingesta de evidencia en `runtime/inbox/`
2) Jobs procesan evidencia
3) Outputs en `runtime/reports/`
4) Drafts de comunidad en `runtime/community/`

## Artefactos
- `runtime/reports/*.md`
- `runtime/hub/events.jsonl`
- `runtime/chat/responses.jsonl`

## Configuración vía env
- `AQUILES_LLM_BASE_URL`
- `AQUILES_LLM_MODEL_FAST` / `AQUILES_LLM_MODEL_BEST`
- `AQUILES_LLM_TIMEOUT_CONNECT` / `AQUILES_LLM_TIMEOUT_READ`
- `AQUILES_LLM_MAX_TOKENS`
- `AQUILES_LLM_CACHE_TTL`
