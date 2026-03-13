# Aquiles Reasoning Demo

## Run date
- 2026-03-13

## Purpose
This public note links Faro to a real local reproducible demo run of Aquiles using golden claims.

The run was executed against the local Proyecto Aquiles web/API surface and stored as a structured
manifest plus per-case JSON outputs.

## Scope of the demo
Golden claim categories included:

- definitional
- historical quantitative negation
- temporal geopolitical
- comparative evaluative politics
- historical relational technology
- economics

## High-level result
The deterministic claim decomposition pipeline is already distinguishing claim types with useful
structure. The main gap remains traceable-source retrieval, which still returned zero valid sources
across the public demo set.

This is useful because it shows progress and limitation at the same time:

- claim understanding is improving
- evidence traceability still needs stronger domain connectors

## Manifest
- [aquiles_reasoning_demo_manifest_2026-03-13.json](aquiles_reasoning_demo_manifest_2026-03-13.json)

## Observed cases

### def_ia_01
- claim type: definitional
- context: IA
- relation: definición solicitada
- domains: tecnologia

### hist_termopilas_01
- claim type: negación cuantitativa
- context: La batalla de las termópilas
- object: 300 soldados
- domains: historia

### temp_ww3_01
- claim type: temporal
- context: La tercera guerra mundial
- relation: inicio temporal afirmado
- domains: tecnologia, historia

### comp_boric_01
- claim type: comparativo-evaluativo
- context: Gobierno de Gabriel Boric en Chile
- object: gobiernos anteriores en Chile
- domains: politica, economia

### hist_tech_ww2_01
- claim type: relacional
- context: La segunda guerra mundial
- object: la tecnología
- domains: tecnologia, historia

### econ_inflation_01
- claim type: relacional
- context: La inflación
- object: el poder adquisitivo en Chile
- domains: economia

## Interpretation
This demo should be read as a methodological checkpoint, not as a finished verification engine.

It demonstrates that Aquiles can already:

- normalize and classify diverse claims
- render methodology-oriented structure
- expose gaps honestly when evidence support is weak

It does not yet demonstrate strong traceable retrieval quality across all domains.
