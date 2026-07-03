---
name: market-structure-liquidity
description: Use when analyzing market structure transitions (BOS, CHOCH, MSS), validating liquidity sweeps, mapping premium/discount arrays, or evaluating institutional setups (Unicorn, Breakers, BPRs) to react to price delivery at key liquidity pools.
---

## The Iron Law

```text
NEVER execute any trade entry on a structural shift (MSS/CHOCH) or order block unless a higher-timeframe liquidity sweep (stop hunt) has occurred immediately prior, and the shifting candle body-to-wick ratio is greater than 70%.
```

## Behavioral Rules

*   **Restrict Execution Windows:** Limit trade executions strictly to London, New York, and Asia Killzones. Disregard low-volume consolidation periods outside these hours.
*   **Validate Sweeps Volumetrically:** Confirm structural sweeps at Key Levels (PDH, PDL, session extremes) using footprint charts. Require a diagonal bid/ask imbalance greater than 3:1 and clear delta divergence before entering a reversal.
*   **Execute Unicorn Setup Rules:** Identify horizontal overlaps between an ICT Breaker Block and an ICT Fair Value Gap (FVG) after a liquidity sweep. Set limit orders directly at this overlap boundary, and position stops past the FVG-forming candle or Breaker extreme.
*   **Prioritize Order Flow Over Refined OBs:** Prioritize broader structural Order Flow (the entire corrective pullback leg) over over-refined lower-timeframe Order Blocks to avoid missed trades.
*   **Apply Invalidation to Mitigation Blocks:** Reject Mitigation Blocks (failure swings) unless you have high-timeframe structural alignment and a highly compressed stop-loss. Prioritize Breaker Blocks that established clear liquidity sweeps.
*   **Filter Displacement Candlesticks:** Only trade Balanced Price Ranges (BPRs) or FVGs formed by displacement candles with a body-to-wick ratio greater than 70%. Reject any structural shifts displaying a ratio below 60%.
*   **Enforce IOFED Entry Controls:** If executing an Institutional Order Flow Entry Drill (IOFED) at the proximal edge of an FVG (under 50% retracement), scale down risk parameters to account for a statistically lower win rate compared to equilibrium mitigation.
*   **Enforce the Psychological Circuit Breaker:** Terminate all trading sessions immediately upon committing three operational errors (such as executing outside Killzones, adjusting a stop-loss wider, or exceeding contract-size parameters).

## Red Flags

| If you think/rationalize... | Why it is wrong / What to do instead |
| :--- | :--- |
| "I should refine this Order Block to the 1-minute extreme to get a 1:20 Risk-to-Reward ratio." | This causes high missed-trade bias. Map the broader higher-timeframe Order Flow leg and execute on a lower-timeframe structural shift inside it. |
| "This breakout is moving fast; I can enter the structural shift even though liquidity wasn't swept." | You are trading into a retail trap. Wait for a clear stop-run (sweep) of a key level (PDH/PDL) and an aggressive displacement shift before entering. |
| "A mitigation block formed, so I can enter a high-confidence swing reversal without a sweep." | Mitigation blocks represent exhaustion and have lower structural strength. Lower your position size, tighten risk, and require high-timeframe POI confluence. |
| "The RSI is oversold at this key level, which confirms my liquidity sweep entry." | Do not overlay lagging retail indicators. Rely strictly on pure price delivery, wick rejections, and footprint volume absorption. |
| "The market shifted structure, even though the displacement candle has long wicks and a small body." | Weak candle bodies (under 60% body-to-wick ratio) indicate poor institutional commitment. Only trade displacement legs with a body-to-wick ratio over 70%. |

## Quick Reference

| Setup / Concept | Primary Conditions | Execution & Stop Placement |
| :--- | :--- | :--- |
| **Unicorn Setup** | Liquidity sweep + MSS/CHOCH + FVG overlapping a Breaker Block. | Limit at the overlap; stop beyond the FVG-forming candle or Breaker extreme. |
| **IOFED Entry** | Price retraces into FVG but holds under 50% (consequent encroachment). | Direct entry at proximal edge; use tighter stop-loss; scale size down. |
| **BPR & IFVG** | Dynamic overlap of bullish/bearish FVGs or flipped FVG; candle body-to-wick > 70%. | Entry on retest of the boundary; stop beyond the invalidation level. |
| **Sweep Confirmation** | Stop hunt of PDH/PDL or session extremes inside a Killzone. | Confirm via footprint delta divergence and >3:1 diagonal imbalance before entering. |
| **Breaker Block** | Failed Order Block after a confirmed liquidity sweep and structural shift. | Limit at the breaker boundary; stop beyond the sweep swing extreme. |