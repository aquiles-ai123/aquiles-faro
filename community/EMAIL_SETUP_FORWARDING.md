# Email Forwarding Setup (aquilesindustries.com)

**Objetivo:** configurar forwarding para reportes de conducta y seguridad sin crear nuevas cuentas Gmail.

## Opción A — ImprovMX (recomendada)

**DNS / MX**
- `mx1.improvmx.com` (prioridad 10)
- `mx2.improvmx.com` (prioridad 20)

**SPF (TXT en @)**
- `v=spf1 include:spf.improvmx.com ~all`

**Alias a crear**
- `conduct@aquilesindustries.com` → **tu Gmail** + **1–2 correos de confianza**
- `security@aquilesindustries.com` → **tu Gmail** + **1–2 correos de confianza**

**Notas**
- La propagación DNS puede demorar 24–48h.
- No publiques los destinos internos en repos públicos.

## Opción B — Cloudflare Email Routing

**Requisito:** el dominio debe usar nameservers/DNS de Cloudflare.

**Pasos (alto nivel)**
- Activar Email Routing en Cloudflare.
- Crear “custom addresses” para:
  - `conduct@aquilesindustries.com`
  - `security@aquilesindustries.com`
- Crear reglas de reenvío a **2–3 destinatarios internos**.

**Advertencia**
- Cloudflare Routing no permite responder “como” el dominio; la respuesta saldrá desde el correo interno.

## Checklist pilot‑ready
- [ ] El correo no depende de una sola persona (mínimo 2–3 destinatarios)
- [ ] SLA de acuse: < 48h
- [ ] Privacidad: no compartir identidad del reportante fuera del team
