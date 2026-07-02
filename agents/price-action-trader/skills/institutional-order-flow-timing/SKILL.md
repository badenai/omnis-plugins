---
name: institutional-order-flow-timing
description: Use when analyzing institutional order flow, tracking session killzones, mapping AMD cycles, and executing precise timeframe alignment entries (e.g., Unicorn Model, BPR, IOFED, HOB).
---

## The Iron Law

```
Never execute an entry unless there is direct alignment between a High-Timeframe (HTF) Point of Interest (POI) and a Lower-Timeframe (LTF) structural shift occurring strictly within a designated Session Killzone (London or New York). No Killzone, no trade.
```

## Behavioral Rules

*   **Validate BPR Quality:** You must reject any Balanced Price Range (BPR) or Fair Value Gap (FVG) where the displacement candles exhibit a body-to-wick ratio below 70%. Ratios below 60% must be ignored due to degraded expectancy.
*   **Differentiate Structural Blocks:** When evaluating structural flips, categorize a failed Order Block as a high-probability **Breaker Block** only if it swept a key extreme (stop hunt) prior to the Market Structure Shift (MSS). Categorize it as a lower-probability **Mitigation Block** if it formed during a failure swing.
*   **Enforce IOFED Parameters:** When executing the Institutional Order Flow Entry Drill (IOFED), place limit orders strictly at the proximal edge of the FVG. You must cancel the order if price penetrates past the 50% consequent encroachment level without filling you.
*   **Map HOB to LTF:** When identifying a Hidden Order Block (HOB) via overlapping wicks on a High Timeframe (HTF), you must drill down to the Lower Timeframe (LTF) to confirm and map the exact boundaries of the clean order block before setting execution limits.
*   **Execute AMD and AMDX Cycle Analysis:** 
    *   Map the **Asian Session** as Accumulation (A). Do not execute entries here; treat this range as a liquidity generator.
    *   Monitor the **London Session** for the Judas Swing/Manipulation (M) to sweep Asian extremes.
    *   Execute during the **New York Session** for Distribution (D) once London manipulation is confirmed and swept.
*   **Confirm Liquidity Sweeps via Volume and Footprint:**
    *   Do not treat an external swing break as a Change of Character (CHOCH) unless the candle delivers a clean body close past the level with aggressive displacement.
    *   Classify any wick-only break or minor internal break as **Inducement (IDM)** and wait for a deeper sweep.
    *   Verify structural absorption at key HTF levels using a 30m-to-5m-to-1m footprint sequence, confirming entry only when aggressive diagonal delta imbalances are absorbed and accompanied by a 1m Cumulative Volume Delta (CVD) divergence.
*   **Apply the Three-Mistake Circuit Breaker:** You must mandate the immediate closure of all execution platforms if three operational errors are committed in a single session (e.g., trading outside Killzones, manual stop-loss adjustments, size violations).

## Red Flags

| Red Flag | Why It Is Wrong | Correct Action |
| :--- | :--- | :--- |
| **Trading FVGs/BPRs with long wicks** | Displacement candles with < 70% body-to-wick ratios yield poor expectancy (1.3R vs 2.1R). | Only execute when displacement candles show strong body dominance (>70%). |
| **Treating failure swings as Breakers** | Mitigation Blocks lack the momentum of swept resting liquidity, resulting in a low win-rate. | Require a clear liquidity sweep (stop hunt) before classifying the zone as a high-probability Breaker. |
| **Trading outside Killzones** | Algorithmic delivery algorithms (AMD/AMDX) operate on time-of-day filters; out-of-session moves are low-probability. | Stand flat during the Asian session; execute strictly within London and New York session windows. |
| **Chasing IOFED beyond 50% encroachment** | If the algorithm penetrates past the 50% level of the FVG, the immediate momentum model is invalidated. | Cancel proximal limit orders immediately if consequent encroachment (50%) is breached before execution. |
| **Executing on automated SMC indicators blindly** | Static automated scripts curve-fit historical data and fail to map real-time institutional liquidity transitions. | Manually verify structural shifts, sweeps, and footprint delta absorption on live charts. |

## Quick Reference

| Model / Pattern | Key Trigger Conditions | Execution Zone / Method |
| :--- | :--- | :--- |
| **ICT Unicorn Model** | HTF Liquidity Sweep + MSS + Overlapping Breaker Block & FVG | Entry limit within the overlapping horizontal zone of the Breaker and FVG. |
| **Venom Model** | Session Killzone + Liquidity Sweep + Immediate Balanced Price Range (BPR) | Execution on BPR horizontal boundary with tight invalidation past the sweep high/low. |
| **IOFED Precision** | High-momentum trend + FVG formation | Limit order at the proximal edge of the FVG; invalidation past 50% consequent encroachment. |
| **Hidden Order Block (HOB)** | Overlapping HTF wicks | Refine to LTF standard Order Block; execute on first touch of the refined zone. |
| **AMDX Cycle** | Accumulation (Asia) -> Manipulation (London) -> Distribution (New York) | Enter New York reversal entries after London sweeps the Asian range extremes. |