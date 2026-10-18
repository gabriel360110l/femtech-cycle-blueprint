# Developer Notes — Practical Tips for Later Implementation

Short, concrete notes so future development is easier.

## Suggested tech starting points
- **Flutter** or **React Native** for one codebase (iOS + Android).
- Local encrypted SQLite (SQLCipher / Drift / WatermelonDB).
- Charts: `fl_chart` (Flutter) or Skia-based / Victory Native (React Native).
- Optional later: HealthKit + Health Connect for wearable temperature.

## File / folder ideas for the actual app later
```
lib/
  models/          # UserProfile, DailyLog, Cycle, etc.
  services/
    prediction/    # Gaussian + Sensiplan logic
    database/      # encrypted SQLite
    export/        # PDF generation
  screens/
    home/
    calendar/
    log/
    charts/
    export/
  widgets/
```

## Important implementation rules
1. Never calculate ovulation as cycle_length - 14 as the main method.
2. Always store whether a BBT reading was disturbed.
3. Keep a clear separation between raw logs and calculated events (confirmed ovulation, luteal length).
4. Make mode switching instant and reversible.
5. PDF export should work fully offline.
6. All warning texts must include a non-diagnostic disclaimer.

## Testing ideas
- Unit tests for the 3-over-6 temperature rule with known example charts.
- Tests for short luteal phase detection.
- Tests that anovulatory cycles are excluded from averages.
- UI tests for logging speed.

## Open decisions still to make
- Exact tech stack (Flutter vs React Native)
- Whether to support cloud backup in v1 or later
- Exact wording of warnings (legal review recommended)
- Which languages to support first (NL + EN recommended)
