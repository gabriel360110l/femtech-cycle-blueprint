# Prediction Logic — Detailed Explanation

This document explains how the app should predict the next period, ovulation and fertile window so that a developer can implement it later without guessing.

## Core idea

Predictions improve the more personal data the user logs. Never rely only on a fixed 28-day model.

### 1. When the user has little data (0–2 cycles)
- Ask for average cycle length and average period length if they know it.
- Use a conservative default (e.g. 28 days cycle, 14-day luteal) but clearly show low confidence.
- Display a wider fertile window and say “based on limited data”.

### 2. When the user has 3+ cycles
- Calculate personal average cycle length and standard deviation.
- Estimate personal luteal phase length from confirmed ovulations (if BBT/mucus available).
- Use the Gaussian model from the algorithms document.
- Narrow the fertile window as confidence grows.

### 3. When the user logs BBT + cervical mucus
- Switch to (or overlay) Sensiplan confirmation.
- Once ovulation is confirmed (3-over-6 + mucus peak), the fertile window closes.
- The next period is predicted as ovulation day + personal luteal length.

## What to show the user
- Predicted period start (with range, e.g. “between 12–16 May”).
- Fertile window as a probability band, not a hard yes/no.
- Confidence indicator: “Based on 2 cycles” / “Based on 8 cycles + temperature”.
- Clear note when a reading was disturbed and therefore ignored.

## Edge cases to handle
- Very irregular cycles (>7–9 days variation) → widen the window and lower confidence.
- Anovulatory cycle detected → do not use that cycle for luteal-phase average.
- After miscarriage or post-partum → reset or heavily discount recent cycles until a new pattern appears.
- Hormonal contraception → hide fertile window and treat bleeding as withdrawal bleeding.

## Practical implementation notes
- Store every confirmed ovulation date.
- Recalculate averages after each new cycle ends.
- Allow the user to manually mark a cycle as “irregular / ignore for averages”.
- Always let the user override or correct a predicted ovulation if they have an LH test or ultrasound.
