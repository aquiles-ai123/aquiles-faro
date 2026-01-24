# 04 — LLM Lab

## Métricas
- **TTFT** (Time To First Token)
- **tokens/s**
- **total_s** (tiempo total)
- **prompts_ok** (cantidad de prompts exitosos)

## Cómo correr el benchmark
```bash
python -m aquiles.jobs.run llm_bench
```
Esto genera `runtime/leaderboard.md`.

## Agregar un modelo nuevo (Ollama)
1) Instalar modelo:
```bash
ollama pull <tag>
```
2) Configurar:
```bash
AQUILES_LLM_MODEL_FAST=<tag>
AQUILES_LLM_MODEL_BEST=<tag>
```

## Criterios “fast vs best”
- **fast**: tareas simples, clasificación, extracción, resumen corto.
- **best**: outputs finales, diagnósticos, drafts publicables.
