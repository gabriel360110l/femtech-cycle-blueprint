# Anti-Patterns: What Other Apps Do Wrong

Use this as a checklist of things to **avoid** when building the app.

## 1. Algorithm & Medical Accuracy

| What other apps do | Why it fails | What to do instead |
|--------------------|--------------|--------------------|
| Ovulation = cycle length − 14 | Ignores variable follicular phase, PCOS, stress, post-partum | Use personal luteal length + BBT/mucus confirmation (Sensiplan) + probabilistic window |
| Treat long cycles or heavy pain as “normal variation” | Delays diagnosis of endo, adenomyosis, PCOS, thyroid issues | Surface red flags with clear “discuss with doctor” language + export |
| One-size-fits-all predictions | Poor accuracy on irregular cycles | Personal history + disturbance flags for BBT |
| Show fertile days after confirmed ovulation | Biologically wrong (egg only lives 12–24h) | Close fertile window once 3-over-6 + mucus peak are done |

## 2. Life-Stage Handling

| What other apps do | Why it fails | What to do instead |
|--------------------|--------------|--------------------|
| Separate apps for cycle / TTC / pregnancy / post-partum | Data loss, bad UX, emotional insensitivity | One app with clear modes + seamless switch (no data loss) |
| Keep showing baby content after miscarriage | Extremely painful | One-tap Loss Recovery mode that immediately stops all pregnancy-related UI |
| Ignore IVF/IUI specifics (e.g. Ovitrelle false positives) | Causes unnecessary anxiety | Explicit trigger-shot countdown and warnings |

## 3. Privacy & Trust

| What other apps do | Why it fails | What to do instead |
|--------------------|--------------|--------------------|
| Sell or share data via tracking SDKs | Users lose trust, legal risk | Local-first by default, no third-party analytics on health data |
| Require account + cloud for basic use | Creates barrier and data risk | Fully offline usable, optional encrypted backup later |
| No clear data deletion | Users feel trapped | Easy full export + permanent delete |

## 4. UX & Emotional Design

| What other apps do | Why it fails | What to do instead |
|--------------------|--------------|--------------------|
| Overly pink, infantilizing design | Alienates many users | Calm, professional, inclusive visual language |
| Celebratory confetti after loss or during anxiety | Tone-deaf | Soft, optional animations; respect Loss Recovery and Rainbow modes |
| Hide how predictions are calculated | Black-box feel | Explain the method (Sensiplan, personal averages) transparently |
| Ignore heavy bleeding / pain severity | Misses pathology signals | Structured pain location + severity + bleeding volume logging |

## 5. Technical & Product Mistakes

- Building every feature at once (cycle + pregnancy + IVF + AI risk scores) → never ships. Start with MVP.
- Claiming medical accuracy without validation on real data.
- No clinical export → doctors cannot use the data.
- Poor offline support or slow charts → frustrating daily use.
- No accessibility considerations (font size, contrast, screen reader).

## Quick “Do Not” Checklist

- [ ] Never use fixed 28-day calendar math as primary method
- [ ] Never present a diagnosis or risk score as medical fact
- [ ] Never keep baby-related content after a miscarriage
- [ ] Never send health data to third parties by default
- [ ] Never force an account for core tracking
- [ ] Never ignore pathology red flags
- [ ] Never ship without a useful doctor export
