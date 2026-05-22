---
name: trade-execution-fvg
description: Use when identifying and executing trades at Points of Interest (POIs) such as Order Blocks, Fair Value Gaps (FVGs), Balanced Price Ranges (BPRs), or applying the Unicorn/Venom models and footprint absorption analysis.
---

## The Iron Law

```text
Never execute blindly at a Point of Interest (POI) using static limit orders; you must strictly await localized algorithmic validation via displacement (FVG/BPR creation) or order flow absorption to confirm institutional defense.
```

## Behavioral Rules

*   Validate an Order Block ONLY if it meets three mechanical criteria: it initiates a structural break sweeping internal liquidity, creates aggressive displacement leaving a Fair Value Gap (FVG), and remains completely unmitigated.
*   Invalidate any Order Block immediately once price wicks into it; treat the institutional edge as permanently exhausted.
*   Execute the Venom Model strictly by waiting for a Killzone liquidity sweep followed immediately by the formation of a Balanced Price Range (BPR).
*   Execute the Unicorn Model only when price pulls back into a Mitigation/Breaker Block that perfectly aligns with an FVG.
*   Require footprint confirmation—specifically heavy order flow Absorption that fails to push price, followed by Delta Initiation in the reversal direction—before executing at any established POI.
*   Define your FVG entry mechanics prior to execution: use the IOFED model (executing exactly at the proximal edge) to maximize Risk-to-Reward, or wait for the standard 50% Equilibrium (EQ) fill to prioritize strike rate.
*   Treat an overlapping bullish and bearish FVG strictly as a Balanced Price Range (BPR); use this zone as a near-zero-drawdown defense level once price returns to it.

## Red Flags

| Rationalization | Why Wrong |
| :--- | :--- |
| "This large opposing candle looks like a perfect Order Block." | Without sweeping internal liquidity, causing displacement (FVG), and remaining unmitigated, it is merely retail noise, not an institutional footprint. |
| "I will leave a blind limit order at the 50% EQ of this FVG." | Blind limits ignore real-time footprint absorption and Delta initiation, exposing the execution to unchecked algorithmic continuation. |
| "Price returned to this previously tested OB, I will buy the double bottom." | An institutional Order Block is exhausted the exact moment it is wicked into; secondary touches lack algorithmic backing and act as inducement. |
| "I am executing this Venom Model setup because a BPR just formed." | The Venom model is invalid if the BPR formation was not immediately preceded by a Killzone liquidity sweep. |

## Quick Reference

| POI / Execution Model | Validation Criteria | Execution Trigger |
| :--- | :--- | :--- |
| **High-Probability OB** | Sweeps internal liquidity, creates displacement (FVG), completely unmitigated. | Footprint Absorption and Delta Initiation upon first touch. |
| **Balanced Price Range** | Overlapping bullish and bearish FVGs creating a neutralized price vacuum. | Price returns to the BPR zone after a Killzone sweep. |
| **Unicorn Model** | A Mitigation/Breaker Block physically overlaps/aligns with an FVG. | Price taps the aligned Breaker + FVG zone. |
| **FVG Entry (IOFED)** | Institutional displacement leaves an unmitigated gap in price delivery. | Execute at the proximal edge for maximum R:R. |
| **FVG Entry (EQ)** | Institutional displacement leaves an unmitigated gap in price delivery. | Execute at the 50% Equilibrium mark for higher strike rate. |