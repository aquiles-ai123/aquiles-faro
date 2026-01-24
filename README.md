# Aquiles Faro — Módulo 01: Research Desk (Open)

Aquiles Faro es el módulo abierto de Aquiles OS para investigación aplicada: **local-first, auditable y ético**. Su foco es transformar evidencia en diagnóstico y acciones concretas, con trazabilidad completa y sin cambios a ciegas.

## Qué genera
- **Daily Digest**
- **Nightly Backlog**
- **Community Draft (CPU-friendly)**
- **LLM Bench / Leaderboard** (TTFT + tok/s)

## Cómo corre (alto nivel)
- Linux + systemd --user
- Ollama local o remoto (OpenAI-compat)
- Logs JSONL append-only (auditoría y reproducibilidad)

## Quickstart (usuarios)
**Requisitos mínimos**
- Linux
- Python 3.x
- Ollama (opcional)

**Si solo querés ver outputs:** mirá `docs/`.

## Para devs
- Cómo contribuir: ver `CONTRIBUTING.md`
- Labels sugeridas: `good first issue`, `help wanted`, `llm_lab`, `jobs`, `docs`, `security`

## Ética y seguridad
- Eje operativo: **evidencia → diagnóstico → acción**
- “No cambios a ciegas”: todo se justifica con evidencia y queda auditado

## CTA
Abrí un issue con tu caso de uso + hardware (CPU/GPU, RAM) para priorizar mejoras.
