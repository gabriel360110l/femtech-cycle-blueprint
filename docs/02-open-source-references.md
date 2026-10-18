# Open-Source References

Useful existing projects (as of late 2026). Always verify current status and license before forking or copying code.

| Project | Stack | Why relevant | Link |
|---------|-------|--------------|------|
| Drip | React Native + SQLite | Gold-standard open-source symptothermal implementation. Supported by Mozilla. | https://github.com/bloodyhealth/drip |
| sympto | JavaScript | Extracted Sensiplan engine from Drip. | https://github.com/bloodyhealth/sympto |
| Bluma | TypeScript / React Native | Modern offline, biometric, encrypted local-first design. | https://github.com/blumaHQ/bluma-app |
| Menstrudel | Flutter | Clean multi-platform UI and local storage example. | https://github.com/J-shw/Menstrudel |
| Euki | Swift + Kotlin | Strong privacy features (decoy PIN, zero-knowledge local storage) + medical content. | https://github.com/Euki-App |

## Datasets (for validation)
- FedCycle / Marquette University (Kaggle) — real clinical cycle data with LH and mucus
- PCOS clinical datasets (Rotterdam criteria)
- Citizen Endo / Phendo — endometriosis phenotyping

**Note:** Use these for testing algorithms. Do not ship models trained on them without proper validation and licensing checks.
