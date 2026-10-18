# MVP Scope (Recommended Starting Point)

Building the full vision at once is a multi-year effort. Start with a focused MVP that already differentiates itself.

## Phase 1 — Core Cycle Tracker (MVP)

**Must-have:**
- Local-first encrypted storage (SQLite + SQLCipher or equivalent)
- Daily logging: bleeding (flow + clots), BBT, cervical mucus, symptoms, pain (location + severity), mood
- Symptothermal ovulation confirmation (Sensiplan 3-over-6 + mucus peak)
- Probabilistic fertile window (Gaussian based on personal cycle history)
- Cycle statistics and simple charts
- One-click PDF export for GP/gynaecologist (last 3–6 months: cycle lengths, luteal phase, pain patterns, bleeding volume estimate)
- Modes: Cycle & Health + Diagnostic/Pain mode
- Strong disclaimers and no diagnostic language

**Explicitly out of MVP:**
- Full pregnancy module
- IVF/IUI specific workflows
- Wearable automatic sync
- Cloud sync / partner mode
- Advanced ML risk scoring

## Phase 2 — Fertility & TTC
- TTC mode with DPO tracking
- LH test logging
- Better fertile window visualisation
- Optional wearable BBT import (Apple Health / Health Connect)

## Phase 3 — Pregnancy & Loss
- Pregnancy mode (week-by-week)
- Loss recovery mode (one-tap, stops baby-related content)
- Basic post-partum tracking

## Phase 4 — Pathology depth & Interoperability
- Structured red-flag rules
- FHIR/LOINC export
- More sophisticated pattern recognition (still non-diagnostic)

## Success criteria for MVP
- Fully offline usable
- Data never leaves the device by default
- Export is useful for a Dutch GP (uses NHG-relevant language)
- Ovulation detection matches Sensiplan rules on test data
