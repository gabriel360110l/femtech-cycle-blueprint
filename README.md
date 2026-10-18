# FemTech Cycle Blueprint

Next-generation open-source blueprint for a **privacy-first**, medically grounded app for menstrual cycle, fertility, pregnancy, pathology and post-partum recovery.

This repository contains research, algorithms, data models, clinical decision rules and an AI system prompt. It is **not** production code yet.

## Why this exists

Most commercial cycle apps:
- Use a naive "cycle length − 14" ovulation calculation
- Ignore or downplay pathology (endometriosis, PCOS, adenomyosis, PMDD)
- Force users to switch apps between life stages (cycle → TTC → pregnancy → post-partum)
- Sell or leak intimate health data

This blueprint aims to do better: local-first, symptothermal + probabilistic prediction, pathology-aware, and sensitive to pregnancy loss and fertility treatment.

## Recommended reading order

1. [MVP Scope](./docs/MVP-SCOPE.md) — start here
2. [Problem Analysis](./docs/01-problem-analysis.md)
3. [Anti-Patterns (What Not To Do)](./docs/07-anti-patterns.md)
4. [Algorithms & Clinical Rules](./docs/03-algorithms.md)
5. [Data Model](./docs/04-data-model.md)
6. [Architecture & Privacy](./docs/06-architecture-privacy.md)
7. [UI / UX & Smooth App References](./docs/08-ui-ux-references.md)
8. [Open-Source References](./docs/02-open-source-references.md)
9. [AI System Prompt](./prompts/system-prompt.md)

## Important disclaimers

- This is **not** a medical device and must not present diagnoses.
- All risk flags and pattern recognition must be framed as "information to discuss with a healthcare professional".
- In the EU, certain features may fall under the Medical Device Regulation (MDR). Legal review is required before shipping diagnostic-style functionality.
- Algorithms (especially probabilistic and ML-based) need validation on real clinical datasets before accuracy claims are made.

## Status

- Research dossier: improved and structured
- System prompt: strengthened
- Data model: expanded
- Anti-patterns and UI references added
- Implementation: not started

## License

Research and documentation: open for reuse with attribution.  
Any future code will need an explicit license (recommended: AGPL-3.0 or MIT for libraries).
