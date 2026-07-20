---
name: institutional-order-flow
description: Use when analyzing market structure transformations (BOS, MSS, CHoCH), mapping premium/discount pricing arrays (Order Blocks, Breaker Blocks, FVGs, Balanced Price Ranges), tracking liquidity sweeps (BSL, SSL, EQH/EQL, Inducement), and executing timezone-restricted institutional setups.
---

## The Iron Law

```
Never classify a structural level breach as a Break of Structure (BOS) or Market Structure Shift (MSS) unless the candle body closes decisively beyond the level; any wick-only penetration must be classified strictly as a liquidity sweep.
```

## Behavioral Rules

*   **Market Structure & Ranges**
    *   If a wick penetrates a structural swing high or low without a candle body close, classify it strictly as a liquidity sweep rather than a structural continuation (BOS).
    *   Confirm a Market Structure Shift (MSS) only when there is strong displacement (aggressive, large-bodied momentum candles) breaking a major swing level on the execution timeframe.
    *   Map every active dealing range between a verified swing high and swing low into Premium (top 50%), Equilibrium (50%), and Discount (bottom 50%).
    *   Enter long setups strictly within Discount arrays and short setups strictly within Premium arrays; filter out and ignore entries forming in middle-range consolidations.

*   **Liquidity & Inducement Dynamics**
    *   Identify external liquidity (BSL/SSL) at major swing highs/lows and internal liquidity at minor swing points or pullbacks before defining any target destination.
    *   Trace internal liquidity sweeps (Inducement) as the required algorithmic engineering of fuel before trading continuation setups in the primary higher-timeframe trend direction.
    *   Target Equal Highs (EQH) and Equal Lows (EQL) as primary draws on liquidity, treating them as massive retail stop-loss pools ripe for institutional harvesting.
    *   Enforce a Wait-and-Verify double-sweep protocol on highly manipulated assets: wait for a primary sweep, a secondary sweep (double-sweep), and a subsequent lower-timeframe MSS candle close before placing orders.
    *   Place hard protective stop-losses structurally beyond the absolute extreme wick of the sweep candle; never place stops inside the wick body as it is statistically prone to being run during structural re-tests.

*   **Premium & Discount Pricing Arrays (PD Arrays)**
    *   Validate an Order Block (OB) only if it is the last candle in the opposite direction before a high-volume, impulsive price expansion.
    *   Prioritize Breaker Blocks (BB) over Mitigation Blocks (MB); ensure the breaker setup successfully swept a liquidity pool before the market structure shifted.
    *   Mark the exact 50% midpoint of Fair Value Gaps (FVG) and long candlestick wicks as Consequent Encroachment (CE) to serve as key structural validation levels.
    *   Filter out isolated lower-timeframe (e.g., 15-minute) FVGs; do not execute trades on them unless they align directly with a higher-timeframe (e.g., 4-hour) Order Block or premium/discount array.
    *   Verify Balanced Price Ranges (BPR) where a bullish FVG and a bearish FVG horizontally overlap, using them as robust boundaries for trend invalidation.
    *   Flip standard FVGs to Inverse FVGs (IFVG) once a candle closes decisively past their boundaries, trading them as inverted support or resistance on subsequent retracements.

*   **Specialized Entry Models**
    *   Execute the ICT Unicorn Model by seeking the precise horizontal overlap of an ICT Breaker Block and an ICT Fair Value Gap (FVG) within the breaker's range.
    *   Execute the Reaper Inversion FVG (Reaper IFVG) only when the inversion FVG lies within the impulsive leg of a breaker block (discount zone for longs, premium zone for shorts).
    *   Utilize Optimal Trade Entry (OTE) by mapping Fibonacci retracements between 0.618 and 0.79, targeting the 0.705 level as the high-probability algorithmic entry point.

*   **Session Timing & Algorithmic Cycles**
    *   Restrict execution setups strictly to ICT Kill Zones (London: 2:00 AM – 5:00 AM ET; NY: 8:30 AM – 11:00 AM ET; NY PM: 1:30 PM – 4:00 PM ET).
    *   Prioritize trading execution during the Silver Bullet Windows (London AM: 3:00 AM – 4:00 AM EST; NY AM: 10:00 AM – 11:00 AM EST; NY PM: 2:00 PM – 3:00 PM EST).
    *   Apply the Accumulation, Manipulation, Distribution (AMD) template: identify Asian session accumulation, wait for London/NY manipulation (Judas Swing) to sweep range extremes, and trade the subsequent distribution.

*   **Microstructure & Volumetric Verification**
    *   Confirm footprint diagonal imbalances only when aggressive market orders on one side exceed passive orders on the other side by at least a 3:1 ratio.
    *   Verify passive limit walls on heatmaps with real-time footprint execution (absorption, delta flip, CVD divergence) before assuming institutional support or resistance to avoid spoofing traps.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "The price just swept the level and immediate displacement started; I should enter on the first lower-timeframe market order." | 30% to 40% of first-touch liquidity sweeps are traps (inducement) designed to engineer a secondary, deeper sweep before the real move occurs. |
| "There is a massive FVG here, so I will place a limit order at the gap boundary and set a tight stop right behind it." | 30% to 40% of FVGs remain unfilled, and up to 84% of lower-timeframe FVGs break structure when they are not backed by higher-timeframe arrays. |
| "This heatmap shows a huge buy limit order wall, so this level is guaranteed to hold as strong support." | Market makers deploy spoofing algorithms with massive limit order walls to induce retail positioning, only to cancel them milliseconds before price arrival. |
| "Price broke the swing high by 2 ticks. This is a clean Break of Structure (BOS) indicating trend continuation." | A valid structural break requires a candle body close. Wick-only violations are strictly liquidity sweeps and are highly prone to immediate reversals. |
| "I can trade these order flow setups at any hour because the market is fractal and structural patterns repeat constantly." | Volume and institutional algorithmic delivery peak inside specific Kill Zones and Silver Bullet windows. Trading outside these hours exposes capital to low-volume noise. |

## Quick Reference

| Concept | Technical Signature | Primary Action |
| :--- | :--- | :--- |
| **BOS vs. Sweep** | Body close past swing high/low vs. Wick-only penetration and immediate rejection. | Validate trend continuation on body close; prepare for reversal setup on wick sweep. |
| **MSS / CHoCH** | Energetic displacement close breaking a major swing level on execution timeframe. | Confirm trend shift and search for premium/discount PD arrays for entry. |
| **Double-Sweep Protocol** | Secondary sweep of the initial sweep candle's extreme wick. | Wait for secondary sweep, monitor for lower-timeframe MSS, then execute with stop at absolute low/high. |
| **ICT Unicorn Model** | Horizontal overlap of a Breaker Block and a Fair Value Gap (FVG). | Execute limit or market entry inside the overlapping zone with structural invalidation below/above breaker. |
| **Reaper IFVG** | Failed FVG (Inversion) located within the impulsive leg of a Breaker Block. | Execute on the mitigation of the IFVG, anticipating institutional defense of the breaker's premium/discount zone. |
| **Consequent Encroachment** | The exact 50% midpoint of a Fair Value Gap or a long candlestick wick. | Monitor for structural reactions; bodies holding past 50% indicate potential structural invalidation. |