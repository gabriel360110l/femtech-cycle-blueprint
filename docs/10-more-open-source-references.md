# Additional Open-Source Period & Health References

Extra useful projects (filtered for relevance and quality). Focus on privacy-first and European-usable tools.

## More cycle / period trackers

| Project | Stack | Why useful | Link |
|---------|-------|------------|------|
| **Mooneva Cycle** | (Android/iOS) | Fully offline, encrypted, no internet permission, import from Drip/Flo/Clue, multi-language | https://github.com/aradar46/Mooneva-Cycle-Private-Period-Tracker |
| **Peri** | Ionic / React | Simple cycle tracker with good localisation (many languages) | https://github.com/IraSoro/peri |
| **Ovumcy** | Go / self-hosted | Self-hosted, privacy-first, Docker-ready cycle tracker | https://github.com/ovumcy/ovumcy-web |
| **Ephira** | React Native | Encrypted local-first, clean modern design | https://github.com/adulbrich/ephira |
| **POW!** | Gatsby | End-to-end encrypted menstrual journal | https://github.com/raae/pow-app |

## Prediction & algorithm notes

- Personal history is the strongest signal: average cycle length, variability, and confirmed ovulation days from previous cycles.
- Allow users to enter past cycle lengths even before they start daily logging (improves early predictions).
- Combine:
  1. Historical average + standard deviation (probabilistic)
  2. Confirmed BBT + mucus (Sensiplan)
  3. Optional LH tests
- Show confidence level (“based on 3 cycles” vs “based on 12 cycles”).

## European-friendly design points

- Support first day of week = Monday (default in most of Europe).
- Metric units.
- Clear language around fertility (avoid overly American marketing tone).
- Privacy copy that matches GDPR expectations.

## Already covered earlier (still the strongest references)

- Drip + sympto → best Sensiplan implementation
- Bluma → modern offline UX
- Menstrudel → clean Flutter example
- ROS Cycle → transparent Gaussian prediction
- Euki → privacy + medical content

These additions give more concrete examples of how other open-source projects handle prediction, import, offline storage and multi-language support.
