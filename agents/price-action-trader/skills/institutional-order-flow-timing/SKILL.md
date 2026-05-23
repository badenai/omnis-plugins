---
name: institutional-order-flow-timing
description: Use when analyzing market cycles, identifying institutional sweeps, determining premium/discount alignment, locating structural imbalances (FVGs, BPRs, Breakers), or validating executions within session timing macros.
---

## The Iron Law

```text
NEVER execute an entry outside of a strict session-timing macro window, nor outside of premium/discount alignment (buys only in discount, sells only in premium) relative to the active trading range.
```

## Behavioral Rules

*   **Session-Cycle Mapping (AMD):** Divide daily sessions strictly into Accumulation (Asian session consolidation), Manipulation (London session Judas Swing sweeping Asian extremes), and Distribution (New York AM/PM expansion driving the true trend leg).
*   **Premium/Discount Restraint:** Calculate the 50% equilibrium mark of the active structural leg before execution; restrict buys to discount zones (< 50%) and sells to premium zones (> 50%).
*   **Algorithmic Imbalance Management:** Utilize the consequent encroachment (CE / 50% midpoint) of a Fair Value Gap (FVG) as the primary institutional magnet, expecting price to react at or before this level.
*   **Order Block Validation:** Validate an Order Block (OB) only if it has swept local liquidity, originated a confirmed structural break (BOS/CHOCH), exhibited aggressive displacement leaving an invalidating FVG, and remains unmitigated (untouched).
*   **Breaker vs. Mitigation Prioritization:** Prioritize Breaker Blocks (failed OBs that swept liquidity before failure) over Mitigation Blocks (failed OBs originating from failure swings) due to their higher algorithmic probability.
*   **Balanced Price Range (BPR) Execution:** Identify BPRs where a bullish and bearish FVG overlap horizontally; treat the boundaries of this overlapping zone as a highly defended, minimal-drawdown barrier for immediate entry.
*   **Liquidity Sweeps & MSS Validation:** Wait for a clear higher-timeframe (HTF) candle body close to confirm a Market Structure Shift (MSS) following an external liquidity sweep (PDH/PDL/Session extremes) to avoid structure inducement traps.
*   **Correlation Splits (SMT):** Spot SMT divergence at key HTF Points of Interest (POIs) by identifying correlation cracks between correlated assets (e.g., EURUSD sweeping liquidity while GBPUSD fails to sweep) to confirm institutional footprint alignment.
*   **Timing Macro Restriction:** Restrict execution exclusively to the 60-minute algorithmic macro windows during London and New York sessions to minimize exposure to off-hours noise and daily drawdown traps.
*   **Unicorn & Venom Model Tactics:** Execute the Unicorn model when a fresh Mitigation or Breaker Block aligns with a valid FVG/iFVG; execute the Venom model directly at BPR boundaries strictly within defined macro windows.
*   **IOFED Precision:** If utilizing the Institutional Order Flow Entry Drill (IOFED), place limit orders directly at the proximal edge of the FVG instead of waiting for the 50% CE fill, adapting risk parameters to accommodate the tighter stop limits.
*   **Order Flow Volume Verification:** Confirm HTF POI mitigations using Footprint charts, looking for passive institutional limit absorption (high volume with static price) followed by delta divergence before executing counter-trend plays.

## Red Flags

| Red Flag / Retail Rationalization | Why It Is Algorithmically Wrong |
| :--- | :--- |
| **"Chasing immediate breakout candles."** | Violates premium/discount rules; buying in premium or selling in discount turns institutional algorithms against your position. |
| **"Labeling any random opposite-colored candle as an Order Block."** | True OBs require structure alignment (BOS/CHOCH), immediate aggressive displacement leaving an FVG, and freshness. |
| **"Trading session transitions or off-hours without regard to timing macros."** | Exposes positions to low-liquidity noise, consolidation, or sudden unhedged spreads without institutional volume backup. |
| **"Trading Mitigation Blocks in isolation during high-volatility events."** | Mitigation blocks stem from failure swings and lack the trapped liquidity "fuel" of Breaker Blocks, resulting in high failure rates. |
| **"Executing counter-trend positions on any minor lower-timeframe FVG touch."| Treats internal liquidity as structural reversals, leading to getting swept by the higher-timeframe expansion leg. |

## Quick Reference

| Concept | Target / Rule | Execution Metric |
| :--- | :--- | :--- |
| **AMD Session Cycle** | Asia (Accumulate), London (Manipulate), NY (Distribute) | Check session high/low sweeps for Manipulation. |
| **Premium vs. Discount** | Equilibrium (50%) of active trading range | Buy < 50% range, Sell > 50% range. |
| **FVG & BPR Alignment**| CE (50% of FVG) or overlapping FVG zones (BPR) | Treat BPR boundaries as immediate low-drawdown entry triggers. |
| **High-Probability OB** | Structure alignment + aggressive displacement + freshness | Only execute on the first test of the unmitigated zone. |
| **SMT Divergence** | Divergent highs/lows on highly correlated assets | Enter when one asset sweeps while the other fails. |
| **Algorithmic Macros** | Strict 60-minute session-specific execution windows | Restrict all entry orders to these volatility windows. |