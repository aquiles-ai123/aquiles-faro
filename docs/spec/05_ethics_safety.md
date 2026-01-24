# 05 — Ética y seguridad

## Reglas base
- **Trazabilidad**: todo se registra en JSONL.
- **Logs append-only**: no se editan retroactivamente.
- **Minimización de datos**: solo evidencia necesaria.
- **No PII**: evitar datos personales o sensibles.

## Guardrails anti prompt-injection
- Separar evidencia de instrucciones.
- Priorizar inputs controlados (inbox y ledger).
- Validaciones de salida (formato, límites de longitud).

## Política de claims con evidencia
- Cada afirmación debe estar respaldada por evidencia disponible.
- Si falta evidencia, se declara explícitamente.

## Seguridad operacional
- No exponer puertos innecesarios.
- Preferir redes privadas (Tailscale) y firewall (UFW).
- Mantener secrets fuera del repo.
