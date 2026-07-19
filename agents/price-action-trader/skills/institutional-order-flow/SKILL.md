---
name: institutional-order-flow
description: Use when analyzing market structure shifts, identifying institutional imbalances (Fair Value Gaps, Balanced Price Ranges), mapping order blocks, identifying liquidity pools, or evaluating premium/discount arrays for trade execution.
---

## The Iron Law

```text
NEVER execute a long position in a Premium pricing zone (top 50% of the dealing range) or a short position in a Discount pricing zone (bottom 50% of the dealing range), and ALWAYS require a higher-timeframe Point of Interest (POI) to overlap with your execution array.
```

## Behavioral Rules

*   **Validate Breaks of Structure (BOS):** Require a candle body close beyond the previous swing high or low on the dominant execution timeframe; classify any wick-only breaks strictly as liquidity sweeps.
*   **Identify Market Structure Shifts (MSS):** Confirm an MSS or Change of Character (CHOCH) only when energetic displacement (high-volume expansion candles) breaks a local swing high or low.
*   **Execute Premium/Discount Protocols:** Divide the current trading range using a Fibonacci framework to isolate Premium (top 50%), Equilibrium (50%), and Discount (bottom 50%) before identifying setups.
*   **Optimize Entry Location (OTE):** Align Optimal Trade Entry (OTE) zones (61.8% to 79% retracements of the most recent impulsive structural leg) directly with a higher-timeframe POI before taking execution.
*   **Leverage Consequent Encroachment (CE):** Use the 50% midpoint of a Fair Value Gap (FVG) or a long candlestick wick shadow as your sensitive dynamic level for entry validation or stop placement.
*   **Apply Polarity to Inverse FVGs (IFVG):** Flip the structural role of an FVG to an Inverse FVG immediately when a candle closes decisively past its boundaries.
*   **Map Balanced Price Ranges (BPR):** Treat overlapping bullish and bearish FVGs as highly reactive horizontal magnets representing immediate algorithmic rebalancing.
*   **Differentiate Mitigation vs. Breaker Blocks:** Prioritize Breaker Blocks over Mitigation Blocks by ensuring that the block successfully swept liquidity before the market structure shift.
*   **Target Unicorn Entry Models:** Locate the horizontal overlap of an ICT Breaker Block and an FVG to execute high-precision, low-drawdown entries.
*   **Identify Hidden Order Blocks (HOB):** Look for overlapping wicks of consecutive same-color candles on a higher timeframe, then drop to a lower timeframe within that zone to find the precise execution block.
*   **Filter Lower-Timeframe FVGs:** Reject lower-timeframe (e.g., M15) FVGs unless they directly overlap with a Higher Timeframe (HTF) Order Block or premium/discount array.
*   **Enforce Silver Bullet Time Filters:** Restrict ICT Silver Bullet trade execution strictly to three one-hour windows: London Open (3:00–4:00 AM EST), New York AM (10:00–11:00 AM EST), and New York PM (2:00–3:00 PM EST).
*   **Enforce Silver Bullet Sweep Conditions:** Invalidate any Silver Bullet setup if a liquidity sweep does not precede or mark the initial segment of the 60-minute execution window.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "Entering a long position inside the premium zone because there is a strong bullish momentum breakout." | Entering longs in premium ignores institutional pricing; price will routinely retrace to discount zones or HTF POIs before expanding. |
| "Validating a Break of Structure (BOS) using a wick rejection or wick pierce of the swing high/low." | Wicks represent liquidity sweeps/stop-hunts; treating them as continuation leads to entering false breakouts at extreme structural prices. |
| "Taking an FVG setup on a lower timeframe without checking if it aligns with an HTF order block." | Up to 84% of lower-timeframe FVGs fail and reverse immediately if they are not backed by higher-timeframe structural confluence. |
| "Trading the Silver Bullet setup without a preceding liquidity sweep during the session window." | Displacement without a preceding stop-hunt lacks institutional backing and results in high-drawdown failure. |
| "Treating every unmitigated order block as a valid support/resistance level." | Unmitigated order blocks inside retail ranges or without liquidity inducement act as traps rather than reactive points of interest. |

## Quick Reference

| Concept | Primary Condition | Operational Action |
| :--- | :--- | :--- |
| **BOS** | Candle body close beyond swing high/low | Confirm structural trend continuation. |
| **MSS / CHOCH** | Energetic displacement breaking swing high/low | Identify early structural reversal. |
| **OTE** | 61.8% to 79% retracement of impulsive leg | Execute entries aligned with HTF POIs. |
| **Unicorn Model** | Horizontal overlap of Breaker Block and FVG | Execute high-precision, low-drawdown entries. |
| **Silver Bullet** | Specific 1-hour window with preceding sweep | Enter at FVG Consequent Encroachment (50%). |
| **BPR** | Bullish and Bearish FVGs directly overlapping | Target or enter at this highly reactive magnet. |