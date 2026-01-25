# Aquiles Faro — Módulo 01: Research Desk (Open)

Aquiles Faro es el módulo abierto de Aquiles OS para investigación aplicada: **local-first, auditable y ético**. Su foco es transformar evidencia en diagnóstico y acciones concretas, con trazabilidad completa y sin cambios a ciegas.

**Dominio canónico:** aquilesindustries.com  
**CoC:** conduct@aquilesindustries.com · **Security:** security@aquilesindustries.com  
**SLA acuse:** 48h  
**Forwarding setup:** `community/EMAIL_SETUP_FORWARDING.md`

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

## 🚨 Public Preview
Esta es una **preview ética y auditable** del Engine.  
Leé el release público: `PUBLIC_RELEASE.md`.

## Para devs
- Cómo contribuir: ver `CONTRIBUTING.md`
- Expectativas de conducta: ver `CODE_OF_CONDUCT.md`
- Labels sugeridas: `good first issue`, `help wanted`, `llm_lab`, `jobs`, `docs`, `security`

## Conducta y seguridad
- Código de Conducta: `CODE_OF_CONDUCT.md`
- Playbook de enforcement: `community/COC_ENFORCEMENT_PLAYBOOK.md`
- Política de seguridad: `SECURITY.md`

## Ética y seguridad
- Eje operativo: **evidencia → diagnóstico → acción**
- “No cambios a ciegas”: todo se justifica con evidencia y queda auditado

## CTA
Abrí un issue con tu caso de uso + hardware (CPU/GPU, RAM) para priorizar mejoras.
