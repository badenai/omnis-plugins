---
name: structural-formalization
description: Use when designing algorithms for price action, market structure breaks, fair value gaps, order blocks, liquidity sweeps, fractal mapping, and structural failures.
---

## The Iron Law

```text
You must formalize all subjective structural concepts (trends, patterns, gaps, blocks) into explicit array index inequalities, N-bar window lookbacks, and boolean gates. Never use physics terminology, ML buzzwords, or generic object-oriented filler to describe price action; rely exclusively on programmable arithmetic, tick-level loops, and absolute integer thresholds.
```

## Behavioral Rules

- Formulate Fair Value Gaps (FVGs) using precise array index inequalities (e.g., `High[i-2] < Low[i]`) and validate their significance by comparing gap width against an N-period Average True Range (ATR) threshold.
- Calculate structural velocity using simple linear regression slope operators over tick-level arrays; reject the use of complex terminology like "RANSAC flat slopes".
- Program multi-timeframe regime filters by maintaining distinct arrays where Higher Timeframe (HTF) pivot highs and lows act as absolute boolean gates for Lower Timeframe (LTF) execution.
- Target the exact 50% midpoint (`(High + Low) / 2`) of order block arrays for entry triggers to mathematically eliminate ambiguous "zone" trading.
- Define liquidity sweeps programmatically by requiring an N-bar window extreme breach followed immediately by a strict directional confirmation (e.g., `Close < Open`) in the subsequent bar.
- Map "Zones of Failure" and retention failures using rigid integer-touch counters; enforce execution only when `touch_count == N` (e.g., the 3rd rejection) returns a boolean true.
- Validate buyer-seller flips conditionally: require historical array pivot breach, logging of a new extreme index, and a subsequent retest bar that closes with a rejection wick.
- Manage structural "memory" by coding N-bar decay loops that dynamically invalidate older gap arrays based on localized volatility metrics.
- Write all arithmetic and logical constraints strictly using standard code operators (e.g., `<`, `>`, `==`, `<=`); never use LaTeX-style formatting for math.
- Reject any structural algorithm proposal that fails to encode a deterministic hard array boundary for its stop-loss condition.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "Kinematic validation of structural decay" | Contaminates the model with physics jargon instead of using basic boolean logic and array loops. |
| "ML-classified confidence on RANSAC flat slopes" | Replaces practical programmatic concepts (linear regression slopes) with overly complex ML buzzwords. |
| "Triggering a stateful object-oriented sanitization" | Employs artificial architectural phrasing to mask a lack of precise computable variables. |
| "Wait for the trend to look exhausted" | Relies on subjective visual evaluation rather than deterministic N-bar structural failure counting. |
| `if slope $\ge$ ATR_threshold:` | Utilizes banned LaTeX-style math formatting that abstracts away standard programmatic syntax. |

## Quick Reference

| Concept | Deterministic Implementation Standard |
| :--- | :--- |
| **Fair Value Gap** | `High[i-2] < Low[i]` validated against `> (ATR * multiplier)`. |
| **Liquidity Sweep** | Price breaches N-bar High array index + next bar `Close < Open`. |
| **Structural Failure** | Trigger executes when `touch_counter == 3` (integer threshold). |
| **Order Block Entry** | Limit order strictly derived via `(High + Low) / 2`. |
| **Fractal Mapping** | HTF pivot array dictates boolean regime filter for LTF arrays. |