---
name: institutional-order-flow-timing
description: Use when analyzing market structure shifts, identifying institutional entry arrays (Order Blocks, FVGs, Breaker Blocks), verifying order flow via volume profiles, and executing trades strictly within session-specific Killzones.
---

## The Iron Law

```
Never execute a trade or analyze a setup outside of designated session Killzones (London Open: 2:00-5:00 AM ET, NY Open: 8:30-11:00 AM ET, NY PM: 1:30-4:00 PM ET). If a structure shift or liquidity sweep occurs outside these windows, classify it as low-probability noise and ignore it.
```

## Behavioral Rules

*   **Validate Market Structure Shifts (MSS/CHOCH):** Only classify a shift as a valid MSS/CHOCH if the candle body closes past the structural swing extreme with strong institutional displacement. Treat wick-only breaks as liquidity sweeps (stop hunts), not structural shifts.
*   **Differentiate Structural Blocks:** Classify a support/resistance flip as a high-probability **Breaker Block** if and only if the block originated from a leg that successfully swept liquidity before the structure shift. If no liquidity sweep occurred prior to the reversal, classify it as a lower-probability **Mitigation Block** and enforce tighter risk parameters.
*   **Evaluate Fair Value Gaps (FVGs):** Prioritize FVGs and Balanced Price Ranges (BPRs) formed by high-displacement candles with a body-to-wick ratio of 70% or greater. Downgrade or ignore setups where the displacement candles have a body-to-wick ratio under 60%.
*   **Locate Advanced PD Arrays:** Look for **Reaper Inversion FVGs** strictly in the premium zone of the impulsive leg for bearish setups, and strictly in the discount zone of the impulsive leg for bullish setups.
*   **Confirm Sweeps with Volume/Delta:** Verify liquidity sweeps at key pools (PDH, PDL, Asian extremes) using delta-price divergences or volume footprint absorption. If a sweep occurs but net Delta shows no absorption (no passive institutional limit walls stacking on the DOM), do not execute the reversal.
*   **Apply the Power of Three (AMD):** Frame the daily session strictly using the Accumulation-Manipulation-Distribution (AMD) blueprint. Identify the low-volume Asian session as Accumulation, search for the London Open Judas Swing as Manipulation, and look for the New York session to deliver the true daily expansion (Distribution).
*   **Enforce the Three-Mistake Rule:** Terminate your trading terminal immediately for the day if you commit three process-oriented execution errors (such as trading outside of session Killzones, chasing internal inducement, or moving a resting stop-loss), regardless of whether your daily financial drawdown limit has been reached.

## Red Flags

| Red Flag | Why It Is Wrong | Corrective Action |
| :--- | :--- | :--- |
| **Executing on Wick-Only Breaks** | Mistaking a liquidity run (stop hunt) for a structural trend shift (BOS/MSS). | Require a full candlestick body close past the swing high/low to confirm structural displacement. |
| **Chasing Internal Inducement** | Treating minor internal structural breaks as high-probability CHOCH setups, trapping entries early. | Wait for HTF external swing point sweeps and clear, displacement-backed MSS. |
| **Trading Mitigation Blocks as Breakers** | Assuming a failed OB is strong support/resistance when it never swept liquidity before reversing. | Demote mitigation setups to low-probability; require additional HTF POI confluence. |
| **Executing Outside Killzones** | Trading low-volume, algorithmic manipulation phases during session transitions or Asian ranges. | Keep hands off the keyboard except during the London, NY AM, and NY PM Killzone windows. |
| **Ignoring Delta Divergence on Sweeps** | Entering a reversal sweep without verifying if passive institutional buyers/sellers absorbed the market orders. | Verify footprints for heavy passive limit stacking (icebergs) or strong delta-price divergence at the level. |

## Quick Reference

### Session Killzones & Algorithmic Timing (Eastern Time)

| Session / Killzone | Time Window (ET) | Algorithmic Behavior / Focus |
| :--- | :--- | :--- |
| **Asian Session** | 6:00 PM – 2:00 AM | **Accumulation Phase:** Low-volume range building liquidity on both extremes. |
| **London Open** | 2:00 AM – 5:00 AM | **Manipulation Phase (Judas Swing):** Sweep of Asian range extremes; trend initiation. |
| **New York Open** | 8:30 AM – 11:00 AM | **Distribution Phase:** High-volume execution, Silver Bullet setups, major expansion. |
| **New York PM** | 1:30 PM – 4:00 PM | **Resolution / Reversal Phase:** Late-day trend continuation or macro trend reversal. |

### Institutional Price Array Matrix

| PD Array Type | Definition / Identification | Precision Level / Gravity Point |
| :--- | :--- | :--- |
| **Order Block (OB)** | Last counter-trend candle before a high-displacement expansion leg. | Mean Threshold (50% midpoint of the OB candle body). |
| **Fair Value Gap (FVG)** | 3-candle price imbalance representing single-sided market delivery. | Consequent Encroachment (CE) (50% of the FVG gap). |
| **Breaker Block** | An invalidated Order Block that successfully swept liquidity before MSS. | Midpoint of the Breaker Block body. |
| **Balanced Price Range (BPR)** | The exact horizontal overlap of a bullish FVG and a bearish FVG. | Entire overlapping price band acting as immediate support/resistance. |
| **Suspension Block** | Candlestick body completely overlapped by the wick of the prior candle. | Sandwiched between upper and lower volume imbalances. |