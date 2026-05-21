---
name: market-structure-liquidity
description: Use when analyzing price action, identifying trend direction, mapping structural breaks, hunting liquidity pools, and distinguishing true reversals from inducement traps.
---

## The Iron Law

```text
Never validate a Change of Character (CHOCH) or Break of Structure (BOS) unless it directly originates from a sweep of external liquidity; structural breaks without prior liquidity absorption are algorithmic traps (Inducement).
```

## Behavioral Rules

*   Identify sweeps of external liquidity strictly at Previous Day Highs/Lows (PDH/PDL) or established session boundaries before mapping reversal structures.
*   Require a candle body to close with aggressive displacement past a major external swing level to validate a True CHOCH or BOS.
*   Treat wick penetrations of structural levels as liquidity sweeps (stop hunts/Wyckoff Springs/Upthrusts), never as true structural breaks.
*   Categorize internal, minor structural breaks as Inducement (IDM) engineered to wipe out early breakout traders.
*   Map the Manipulation phase (Judas Swing) to time-based sweeps of Asian session Accumulation boundaries during London or New York Killzones.
*   Validate liquidity sweeps by confirming that subsequent price action creates a Market Structure Shift (MSS) leaving a Fair Value Gap (FVG).
*   Always align low-timeframe structural shifts (e.g., 1-minute or 3-minute killzone sweeps) with the Higher-Timeframe (HTF) directional bias.
*   Place stop losses strictly beyond the extreme wick of the liquidity sweep to mechanically protect the structural level.

## Red Flags

| Rationalization | Why wrong |
| :--- | :--- |
| "Price broke this minor high, so the trend has changed." | Minor internal breaks are Inducement (IDM); true reversals require a sweep of major external liquidity first. |
| "The wick went past the previous high, that is a Break of Structure." | Wicks represent liquidity sweeps (stop hunts); valid BOS/CHOCH requires a solid body close with displacement. |
| "I am trading this 1-minute structural shift because the killzone just started." | Low-timeframe shifts divorced from higher-timeframe alignment degrade edge and lead to volatile stop-outs. |
| "There is a massive Order Block here, I will enter immediately." | An OB is invalid unless it originates a structural break that sweeps internal liquidity and leaves an FVG. |

## Quick Reference

| Concept | Mechanical Definition | Action |
| :--- | :--- | :--- |
| **True CHOCH / BOS** | Candle body closes past major external swing with violent displacement. | Validate reversal or continuation bias. |
| **Liquidity Sweep** | Wick penetrates PDH/PDL or Session extreme and immediately rejects. | Anticipate reversal; wait for MSS and FVG creation. |
| **Inducement (IDM)** | Minor, internal structural break before major liquidity is swept. | Do not enter; wait for the IDM pool itself to be swept. |
| **Judas Swing** | Time-based sweep of Asian session boundaries during London/NY open. | Execute in the opposite direction of the manipulation. |
| **Wyckoff Sweep** | BSL sweep (Upthrust) or SSL sweep (Spring) with tick volume expansion. | Use as a mechanical filter to confirm institutional intent. |