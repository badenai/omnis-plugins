---
name: market-structure-liquidity
description: Use when analyzing market structure, identifying swing highs/lows, distinguishing CHOCH from Inducement, detecting liquidity sweeps, or evaluating institutional price delivery arrays.
---

## The Iron Law

```
A valid Change of Character (CHOCH) or Break of Structure (BOS) MUST execute a decisive candle body close past the key external swing high or low; any movement past these levels with only wicks or internal structure breaks must be treated as Inducement (IDM) or a Liquidity Sweep.
```

## Behavioral Rules

*   **Assess structure via body closes only:** You must require a clear candle body close on the active timeframe to confirm a structural break (BOS/CHOCH). Do not mark a trend change if only the wick penetrates the key swing level.
*   **Identify inducement before entering:** You must classify breaks of minor internal highs or lows as Inducement (IDM) traps engineered to sweep breakout traders, rather than true structural reversals.
*   **Validate liquidity sweeps with volume/footprint:** When price sweeps a major liquidity pool (equal highs/lows, session extremes), you must look for aggressive wick rejections or diagonal footprint volume imbalances (>3x ratio) confirming absorption before planning a reversal entry.
*   **Map Premium vs. Discount pricing arrays:** You must draw structural legs from swing low to swing high (or vice versa) and search for bullish setups strictly in the discount zone (<50% retracement) and bearish setups strictly in the premium zone (>50% retracement).
*   **Verify Breaker and FVG alignment:** When applying the Unicorn Model, you must confirm that a Fair Value Gap (FVG) forms directly overlapping or within the horizontal boundaries of the corresponding Breaker Block.
*   **Enforce time-of-day execution filters:** You must restrict active trade setups to official ICT Kill Zones (London Open 2:00-5:00 AM ET, NY Open/Silver Bullet 8:30-11:00 AM ET, or NY PM 1:30-4:00 PM ET). Ignore structural setups that form during low-volume mid-day doldrums.
*   **Examine volume profile displacement:** You must require a body-to-wick ratio of over 70% on the breakout candle to validate high-probability Balanced Price Ranges (BPR) and displacement legs.

## Red Flags

| Red Flag / Bad Practice | Why It Is Wrong | Corrective Action |
| :--- | :--- | :--- |
| **Marking CHOCH on wick breaks** | Wicks indicate price rejection and liquidity collection, not structural shifts. | Wait for a decisive candle body close past the external swing high/low to confirm the shift. |
| **Trading mid-range FVGs** | Buying premium FVGs or selling discount FVGs violates basic mathematical edge. | Filter setups so you only execute in discount zones for longs and premium zones for shorts. |
| **Treating internal sweeps as trend changes** | Minor internal structure breaks are retail traps (Inducement) designed to generate liquidity. | Wait for major external session or swing highs/lows to be swept before hunting a reversal. |
| **Using fixed indicator levels for oversold/overbought** | Lagging indicators like RSI ignore real-time liquidity pools and structural boundaries. | Focus exclusively on price delivery arrays, order blocks, volume, and swing mechanics. |
| **Ignoring the clock during execution** | Algorithmic setups fail or lack follow-through outside of designated institutional volume hours. | Only enter trades that trigger inside the specified London and New York Kill Zones. |

## Quick Reference

| Concept | Key Indicator | Confirmation Metric | Target Area |
| :--- | :--- | :--- | :--- |
| **BOS / CHOCH** | External Swing Break | Candle Body Close | Next key HTF structural level |
| **Inducement (IDM)** | Internal Wick Sweep | Wick Rejection / No Body Close | Opposing liquidity pools |
| **Unicorn Model** | Breaker Block + FVG | horizontal overlapping zones | Target premium/discount extremes |
| **Reaper Inversion** | IFVG inside Breaker Leg | Located in Premium (Short) / Discount (Long) | Sweep of opposing swing pool |
| **Power of Three** | AMD Sequence | Asian Accumulation -> London Manipulation -> NY Distribution | Daily range expansion target |
| **BPR Execution** | Horizontally overlapping FVGs | Breakout candle body-to-wick ratio > 70% | Next unmitigated structural array |