# Open-Source References

Useful existing projects (status checked late 2026). Always verify current activity, license and maintenance before forking or copying code.

## Core cycle & fertility trackers

| Project | Stack | Why relevant | Link |
|---------|-------|--------------|------|
| **Drip** (Bloody Health) | React Native + SQLite | Gold-standard open-source symptothermal (Sensiplan) implementation. Supported by Mozilla Tech Fund. Local-first. | https://github.com/bloodyhealth/drip<br>(primary development now on [GitLab](https://gitlab.com/bloodyhealth/drip)) |
| **sympto** | JavaScript / NPM | Extracted pure Sensiplan algorithm engine from Drip (temperature shift, mucus peak, outliers). | https://github.com/bloodyhealth/sympto |
| **Bluma** | TypeScript / React Native | Modern offline, biometric lock, encrypted local-first design. | https://github.com/blumaHQ/bluma-app |
| **Menstrudel** | Flutter / Dart | Clean multi-platform UI, local storage, notifications. Good Flutter reference. | https://github.com/J-shw/Menstrudel |
| **Euki** | Swift (iOS) + Kotlin (Android) | Strong privacy (decoy PIN / panic mode, zero-knowledge local storage) + medical knowledge content. Recommended by Mozilla & WIRED. | https://github.com/Euki-App |
| **ROS Cycle Project** | HTML5 / JS | Transparent probabilistic (Gaussian) ovulation model + PCOD/PCOS checklist + local PDF export. | https://github.com/alwin-m/ROS-Cycle-Project |

## Pregnancy & related modules

| Project | Stack | Why relevant | Link |
|---------|-------|--------------|------|
| **MMM-PregnancyTracker** | JavaScript | Ready-made `milestones.json` and `size_comparisons.json` (week 1–40) + due-date calculation from conception or LMP. | https://github.com/gowthamravichandran/MMM-PregnancyTracker |

## Research / datasets (for validation only)

| Project / Dataset | Link | Notes |
|-------------------|------|-------|
| Citizen Endo / Phendo (Columbia Univ.) | https://github.com/citizenendo | Endometriosis phenotyping, pain location maps, daily symptom questions. |
| FedCycle / Marquette University | Kaggle (search "fedcycle marquette") | Real clinical cycle data with LH peaks, mucus scores, follicular/luteal lengths. |
| PCOS clinical datasets | Kaggle | Rotterdam criteria based profiles. |

## Additional privacy-focused examples (optional reference)

| Project | Link | Notes |
|---------|------|-------|
| Ephira | https://github.com/adulbrich/ephira | Encrypted local-first React Native tracker. |
| Privates | https://github.com/Bingles2k8/Privates | Local-first, SQLCipher, zero network calls. |

---

**Important notes**
- Prefer studying the algorithm code (especially `bloodyhealth/sympto` and Drip) rather than copying entire apps.
- Check licenses (MIT, GPL, etc.) carefully.
- Use datasets only for offline validation of your own algorithms. Do not ship models trained on them without proper review.
- Drip’s main development has moved to GitLab; the GitHub repo is still useful as a mirror.
