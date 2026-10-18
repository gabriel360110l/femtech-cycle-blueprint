# Algorithms & Clinical Decision Rules

## Two-layer prediction model

### Layer 1 — Probabilistic (calendar + variation)
Gaussian probability of ovulation on cycle day `d`:

$$P_{ov}(d) = \exp\left( -\frac{(d - (\mu_C - L_{lut}))^2}{2(\sigma_C + \delta)^2} \right)$$

- $\mu_C$ = personal average cycle length  
- $\sigma_C$ = personal standard deviation  
- $L_{lut}$ = personal average luteal phase length (default 14, range 10–16)  
- $\delta$ = biological noise (1–2 days)

This produces a probability distribution, not a false binary "fertile/not fertile".

### Layer 2 — Symptothermal confirmation (Sensiplan)
Ovulation is confirmed when:
1. Three consecutive BBT readings are higher than the highest of the previous six low readings, **and**
2. The third high reading is at least +0.2°C above the coverline, **and**
3. Combined with the cervical mucus peak (egg-white / spinnbarkeit).

**Disturbance exclusion:** fever, alcohol, <5 hours sleep, or unusual measurement time → mark `exclude_from_algorithm = true`.

**Fertile window closure:** both the third high temperature day **and** the third day after mucus peak must have passed.

## Clinical red flags (examples)

```text
IF confirmed_ovulation AND days_to_next_period < 10 FOR 3 cycles
  → Flag: Possible short luteal phase / progesterone issue (discuss with doctor)

IF period_started AND no_thermal_shift_detected
  → Flag: Anovulatory cycle (breakthrough bleeding)

IF bleeding_days > 7 OR pad_change < 1-2h OR clots > 2.5cm
  → Flag: Heavy menstrual bleeding — consider iron status, fibroids, adenomyosis

IF medication == 'hCG trigger (Ovitrelle/Pregnyl)' AND days_since_trigger < 12
  → Warn: Positive pregnancy test may be false positive
```

**Important:** All flags must be presented as "patterns to discuss with a healthcare professional", never as a diagnosis.

## Validation requirement
- Sensiplan rules are established and can be unit-tested against known examples.
- Probabilistic models and any future ML must be validated on real datasets (e.g. FedCycle / Marquette) before accuracy claims.
