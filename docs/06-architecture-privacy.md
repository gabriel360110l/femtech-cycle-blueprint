# Architecture & Privacy

## Local-first by default
- Primary storage: encrypted SQLite (SQLCipher, WatermelonDB, Drift, etc.)
- AES-256 encryption at rest
- Biometric app lock
- No account required for core functionality

## Optional sync (Phase 2+)
- Zero-knowledge end-to-end encryption
- Key never leaves the device
- References: libsodium, Standard Notes / Ente-style sync protocols

## Recommended tech direction (open decision)
| Option | Pros | Cons |
|--------|------|------|
| React Native | Large ecosystem, Drip reference | Performance on complex charts |
| Flutter | Fast UI, single codebase, Menstrudel example | Smaller native health SDK integration |
| Kotlin + Swift | Best native performance & HealthKit/Health Connect | Double codebase |

**Suggestion for MVP:** Flutter or React Native + local encrypted SQLite. Decide early.

## Interoperability
- HealthKit / Health Connect for optional wearable BBT (sleeping wrist temperature)
- Future FHIR Observation export using LOINC codes
- Dutch clinical language (NHG / NVOG terminology) in exports

## Security notes
- Never log raw biometric data to analytics
- Clear data-deletion path
- Decoy PIN / panic mode (inspired by Euki) is valuable for safety
