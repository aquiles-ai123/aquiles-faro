# Contributing to Aquiles Faro

¡Gracias por contribuir! Este repo prioriza **trazabilidad**, **evidencia** y **claridad**.

## Reglas de PR
- Cambios pequeños y focalizados (ideal: 1 tema por PR).
- Incluir evidencia: logs, benchmarks, capturas o pasos reproducibles.
- Evitar cambios irreversibles o sin justificación.
- Si el cambio afecta comportamiento, documentar el impacto.

## Cómo contribuir (docs primero)
1) Abrí un issue con el objetivo y el contexto.
2) Editá/creá archivos en `docs/` y actualizá `ROADMAP.md` si aplica.
3) Enlazá contenido relevante desde `docs/README.md`.

## Estándares de documentación
- Títulos claros y jerarquía consistente (H1 único, H2/H3 según sección).
- Lenguaje conciso y verificable.
- No incluir PII ni datos sensibles.
- Referenciar artefactos reales (ej: `runtime/reports/*.md`).

## Checklist para PR
- [ ] No incluye secretos ni datos sensibles
- [ ] Contenido reproducible o verificable
- [ ] Cambios documentados en `README.md` o `docs/`
- [ ] Sin tocar `index.html` / `evidence.html` (si no es necesario)

## Running local (si aplica)
Este repo publica documentación y artefactos de módulo. Si tu aporte requiere ejecución, indicá en el PR:
- hardware (CPU/GPU, RAM)
- comandos exactos
- outputs esperados
