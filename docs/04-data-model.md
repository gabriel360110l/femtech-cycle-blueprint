# Core Data Model

Recommended local-first schema (SQLite + SQLCipher or equivalent). All intimate data stays on device by default.

## 1. UserProfile
- `current_mode`: Cycle | Diagnostic | TTC | Pregnancy | LossRecovery | PostPartum | Perimenopause
- `known_conditions`: array (Endometriosis, Adenomyosis, PCOS, PMDD, Thyroid, etc.)
- `luteal_phase_avg_length`
- `privacy_flags`: hide_weight_triggers, rainbow_safe_mode, etc.
- `contraception_type`

## 2. ReproductiveEpisode
Overarching time periods (one cycle, one pregnancy, one IVF round, one post-partum period).
- `type`, `start_date`, `end_date`, `outcome`, `notes`

## 3. DailyBiometricLog
- `date`, `bbt_temperature`, `bbt_time`, `bbt_disturbed`
- `cervical_mucus` (Dry | Sticky | Creamy | Eggwhite | Watery)
- `cervical_position`, `lh_test`, `hcg_test`
- `resting_heart_rate`

## 4. DailySymptomAndPainLog
- `bleeding_flow`, `clots_size`
- `pain_locations` (array)
- `pain_severity` (0–10)
- `painkillers_taken`
- `gi_symptoms`, `mood_tags`, `energy_level`

## 5. NutritionAndSupplementLog
- folic acid, vitamin D, iron (+ vitamin C flag), DHA, water, caffeine, etc.

## Additional recommended fields
- Consent timestamps per data category
- Soft-delete + audit trail for medical exports
- LOINC/FHIR mapping fields for future interoperability (e.g. 8310-5 for BBT, 8665-2 for LMP)

## Export
One-click clinical PDF/CSV of the last 3–6 months containing:
- Cycle lengths and variability
- Confirmed vs predicted ovulation
- Luteal phase lengths
- Pain and bleeding patterns
- Relevant red-flag observations (with disclaimer)
