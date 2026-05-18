---
name: market-structure-liquidity
description: Use when analyzing market structure, identifying directional bias, tracking liquidity pools (PDH, PDL, session boundaries), evaluating liquidity sweeps, and confirming Market Structure Shifts (MSS) with displacement.
---

## The Iron Law

```text
Never execute a reversal or assume a shift in directional bias without first observing a liquidity sweep of a key level (PDH, PDL, session high/low) followed immediately by a Market Structure Shift (MSS) confirmed by energetic price displacement.
```

## Behavioral Rules

*   **Establish Higher-Timeframe Context:** Determine overarching directional bias and identify target liquidity pools on the Daily or 4-Hour charts before stepping down to lower timeframes (15m, 5m, 1m) to track structural shifts.
*   **Map the Liquidity Matrix:** Mark Previous Day Highs (PDH), Previous Day Lows (PDL), and session boundaries (Asian, London, NY) as mandatory zones of interest for impending liquidity purges.
*   **Demand Displacement:** Validate a Market Structure Shift (MSS) or Change of Character (CHOCH) only if price breaks a structural swing point with energetic, large-range candles that leave behind imbalances; discard slow, grinding, or wicky breaks as algorithmic noise.
*   **Frame the Delivery:** Structure all trade hypotheses around the delivery of price from Internal Range Liquidity out to External Range Liquidity, or vice versa.
*   **Wait Out Macro Volatility:** Require high-timeframe structural confirmation before acting during Tier-1 economic data releases, as algorithms frequently engineer double-sided sweeps of both buy-side and sell-side liquidity.
*   **Anchor Risk to Structure:** Place absolute invalidation levels (stop-loss orders) strictly above or below the extreme wick that engineered the structural liquidity sweep; never use arbitrary pip-count stops.

## Red Flags

| Rationalization | Why it is wrong |
| :--- | :--- |
| "Price just swept the PDL, so I am buying the exact low immediately." | A sweep without a subsequent structural shift and displacement is a falling knife; institutional sponsorship is unconfirmed. |
| "There is a Change of Character on the 1-minute chart, trend is reversing." | Low-timeframe structural breaks divorced from higher-timeframe Premium/Discount liquidity arrays are meaningless algorithmic noise. |
| "The candle barely edged past the swing high, but it's technically an MSS." | Sluggish breaks lack the displacement required to confirm true institutional order flow; true shifts leave energetic footprints. |
| "The market is in a tight summer range, but I'll trade every micro structural break." | Choppy, low-volume conditions frequently produce fake structural shifts; algorithmic ping-pong lacks true directional intent. |

## Quick Reference

| Concept | Structural Definition | Required Action |
| :--- | :--- | :--- |
| **External/Internal Liquidity** | PDH/PDL, Session extremes vs. inside range pools. | Map these as primary draw on price and entry targets. |
| **Liquidity Sweep (Purge)** | A wick that trades through a key liquidity pool and rejects. | Wait for the sweep to conclude, then monitor for structural reversal. |
| **Displacement** | Energetic expansion candles breaking structural levels. | Demand this to validate any Market Structure Shift (MSS). |
| **MSS / CHOCH** | The break of the last significant swing point after a sweep. | Use as the ultimate confirmation that institutional bias has shifted. |
| **Structural Invalidation** | The absolute extreme wick of the liquidity sweep. | Anchor hard risk management strictly to this price level. |