Labels sugeridas: good first issue, help wanted, security, P1

## Contexto
El inbox puede contener instrucciones maliciosas que intentan romper el flujo (“prompt injection”).

## Objetivo
Implementar un gate básico anti prompt-injection con denylist y logging.

## Alcance
Incluye:
- Detección de patrones comunes (denylist)
- Registro en `events.jsonl` cuando se detecta
- Documentación de la política en `docs/spec/05_ethics_safety.md`

No incluye:
- Detección basada en ML
- Bloqueo global del sistema

## Criterios de aceptación
- [ ] Se detectan patrones obvios (ej: “ignore previous instructions”)
- [ ] Se registra un evento con el item afectado
- [ ] No se rompe el pipeline (fallback con warn)

## Cómo verificar
1) Agregar un archivo con texto malicioso al inbox
2) Ejecutar un job que consuma inbox
3) Verificar evento `prompt_injection_detected`

## Pistas de implementación
- Mantener denylist en config
- Registrar `sha1` y ruta del archivo

## Archivos sugeridos
- `docs/spec/05_ethics_safety.md`
- (Implementación) `aquiles/jobs/_util.py` o gate en pre-procesamiento
