# Common Conditions That Affect Many Women

These conditions are frequent enough that the app should be able to help users recognise patterns and prepare for a doctor visit. **The app never diagnoses.** It only shows patterns and suggests discussing them with a healthcare professional.

## Prevalence (approximate, European/global figures)

| Condition | Rough prevalence | What it is |
|-----------|------------------|------------|
| **Endometriosis** | ~1 in 10 (10%) of reproductive-age women | Tissue similar to the uterine lining grows **outside** the uterus (peritoneum, ovaries, bowel, bladder, etc.). It bleeds and causes inflammation, scars and adhesions. |
| **Adenomyosis** | Common, especially after 30–35; often co-exists with endo | Endometrial tissue grows **into the muscle wall** of the uterus. Causes an enlarged, painful uterus and very heavy bleeding. |
| **PCOS** | 5–15% (Rotterdam criteria) | Hormonal condition with irregular/absent ovulation, high androgens (acne, excess hair, hair loss) and often polycystic ovaries on ultrasound. |
| **Uterine fibroids (myomas)** | Very common; up to 50%+ by age 50 have them on imaging; ~20–25% have symptoms | Benign muscle knots in or on the uterus. Can cause heavy bleeding, pressure and pain. |
| **Heavy menstrual bleeding (menorrhagia)** | Affects a large share of women at some point | Bleeding that interferes with daily life (soaking through pads/tampons in 1–2 hours, large clots, >7 days). Often linked to fibroids, adenomyosis or other causes. |
| **PMDD** | ~3–8% | Severe mood symptoms (depression, anxiety, anger, hopelessness) that start after ovulation and disappear within a few days of the period starting. Not a hormone excess — a brain sensitivity. |
| **Short luteal phase / LPD** | Common in fertility issues | Luteal phase <10 days. Can affect implantation. |
| **Anovulatory cycles** | Frequent in PCOS, stress, perimenopause, post-partum | Bleeding without a proper ovulation (no temperature shift). |

## Key symptoms the app must be able to log

### Pain & location
- Severity (0–10)
- Location: lower abdomen, lower back, one ovary side, rectum, bladder, legs, shoulder (rare but important for diaphragmatic endo)
- Timing: only during period, days before period, throughout the cycle, during sex, during bowel movements, during urination
- Impact: does it stop daily activities? Do normal painkillers fail?

### Bleeding
- Flow (spotting / light / medium / heavy)
- Clots (size)
- Duration of bleeding
- Soaking through protection in <1–2 hours
- Bleeding between periods or after sex

### Other highly relevant logs
- Deep pain during sex (dyspareunia)
- Painful bowel movements during period (dyschezia)
- Painful urination or blood in urine during period
- Extreme bloating (“endo belly”)
- Fatigue
- Mood symptoms that are clearly luteal-phase only (for PMDD pattern)

## How the app can later give warnings (non-diagnostic)

Examples of pattern rules (always phrased as “consider discussing with your doctor”):

```text
IF pain_severity >= 7 AND (pain_stops_daily_life OR painkillers_not_helping)
  AND (pain_with_bowel_movement_during_period OR deep_pain_during_sex OR endo_belly)
  → "Severe cyclical pain pattern. Many women with these symptoms later receive a diagnosis of endometriosis or adenomyosis. A doctor can help investigate."

IF average_cycle_length > 35 OR cycles_per_year < 8
  AND (acne OR excess_hair OR no_temperature_shift)
  → "Irregular cycles + androgen signs can fit PCOS. Rotterdam criteria require 2 of 3. Discuss with a doctor."

IF bleeding_days > 7 OR soaking_every_1-2h OR large_clots
  → "Heavy bleeding. Can be linked to fibroids, adenomyosis or other causes and may lead to iron deficiency. Worth checking."

IF confirmed_ovulation AND luteal_phase < 10 days for several cycles
  → "Short luteal phase. Can be relevant for fertility. Discuss if you are trying to conceive."

IF mood_symptoms_severe AND only_in_luteal_phase AND disappear_within_2_days_of_period
  → "Pattern consistent with PMDD. Validated questionnaires (e.g. DRSP) exist; a doctor or psychiatrist can confirm."
```

**Important rules for warnings**
- Never say “you have endometriosis” or any diagnosis.
- Always include a disclaimer.
- Prefer “pattern that many women with X experience” language.
- Make warnings optional / dismissible.
- Export the relevant logs so the user can show them to a doctor.

## Temperature measurement (BBT)

Basal Body Temperature is one of the most useful tools the app can support.

**What to track**
- Temperature (preferably to 0.01°C)
- Time of measurement
- Disturbed flag (fever, alcohol, <5 h sleep, late measurement, illness)

**How users can measure**
- Oral, vaginal or rectal thermometer (same method every day)
- Ideally right after waking, before getting up
- Wearables (Oura, Apple Watch sleeping wrist temperature) can be imported later via HealthKit / Health Connect, but classic BBT remains the gold standard for Sensiplan

**What the app does with it**
- Draw the chart
- Detect the 3-over-6 shift (Sensiplan)
- Ignore disturbed readings
- Use confirmed ovulation to improve future predictions and luteal-phase length

This combination of detailed symptom logging + temperature + pattern warnings gives users something most commercial apps lack: data they can actually take to a doctor.
