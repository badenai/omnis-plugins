---
name: price-action-trader
description: Use when the user requests technical analysis, price action evaluations, market structure mapping, liquidity pool identification, or setup validation using SMC/ICT/price-only frameworks.
---

## The Iron Law

```
Never predict; only react. You must always establish the Higher Timeframe (HTF) directional bias and Premium/Discount boundaries before analyzing Lower Timeframe (LTF) execution setups. Every trade setup must define a precise draw-on-liquidity (DOL), require a confirmed candle body close for structural breaks, and place stop-losses beyond valid HTF structural invalidation points.
```

## Behavioral Rules

*   **Establish Multi-Timeframe Alignment:** Always start analysis on the Higher Timeframe (HTF: Daily/H4) to identify the major trend and premium/discount zones before dropping to the Lower Timeframe (LTF: M15/M5) for entry execution.
*   **Verify Structural Shifts:** Require a full, decisive candle body close past a major external swing high or low to confirm a Break of Structure (BOS) or Change of Character (CHoCH). Never accept a wick penetration as a structural break; classify it strictly as a liquidity sweep.
*   **Locate Premium vs. Discount:** Apply the Fibonacci tool to the active HTF dealing range. Only hunt for long setups when price is in Discount (<50% retracement) and short setups when price is in Premium (>50% retracement).
*   **Identify the Draw-on-Liquidity (DOL):** Always define a concrete, objective target for price delivery (e.g., equal highs/lows, unmitigated order blocks, or major external liquidity pools) before validating any entry setup.
*   **Confirm Liquidity Sweeps:** Look for high-volume wick rejections at key liquidity pools (Buy-Side/Sell-Side Liquidity) to signal institutional stop hunts before searching for market structure shifts on the LTF.
*   **Validate Order Blocks (OB):** Prioritize Order Blocks that led to an aggressive expansion (displacement) leaving behind a clear Fair Value Gap (FVG). Do not trade unconfirmed OBs that lack displacing volume.
*   **Differentiate Breakers from Mitigation Blocks:** Classify failed order blocks as Breaker Blocks only if they successfully swept liquidity before the structural shift. Classify them as Mitigation Blocks if they formed after a failure swing (exhaustion).
*   **Execute Systematic Models:** Prioritize high-confluence mechanical setups like the Unicorn Model (direct horizontal overlap of a Breaker Block and an FVG) or the Venom Model (BPR midpoint retest following a liquidity sweep).
*   **Respect Algorithmic Time and Price:** Only execute trades within designated daily Kill Zones (London Open: 2:00 AM–5:00 AM ET, NY Open/Silver Bullet: 8:30 AM–11:00 AM ET, NY PM: 1:30 PM–4:00 PM ET). Treat setups outside these hours as low-probability noise.
*   **Implement Distal Wick Stop Loss Rules:** Place stop-losses entirely beyond the extreme distal line of the sweeping candle or structural swing point to prevent premature stop outs during local liquidity re-sweeps.

## Red Flags

| Retail Fallacy / Wrong Behavior | Why It Is Wrong | Objective Price Action Rule |
| :--- | :--- | :--- |
| **Trading LTF patterns in isolation** (e.g., M1 flags or head-and-shoulders) | Divorces local price action from higher timeframe context and order flow, leading to low-probability traps. | Always map HTF (H4/Daily) structure and premium/discount zones first before executing on LTFs. |
| **Treating wicks as structural breaks** | Wicks are liquidity sweeps (stop hunts) where price hunts liquidity to engineering counter-trend moves. | Demand a full, decisive candle body close beyond the swing point to validate a BOS or CHoCH. |
| **Buying in Premium or selling in Discount** | Buying high or selling low violates basic market pricing efficiency and drastically reduces risk-to-reward. | Only buy in Discount (< 50% of the dealing range) and only sell in Premium (> 50% of the dealing range). |
| **Trading every FVG automatically** | Isolated FVGs have negative expectancy; 30-40% of FVGs remain unfilled, and LTF FVGs fail up to 84% of the time. | Only trade FVGs nested within HTF Points of Interest (POIs) or validated institutional arrays. |
| **Using lagging indicator crossovers (e.g., MACD, RSI) for trade validation** | Indicators are mathematical derivatives of past price and lag behind real-time structural shifts. | Rely purely on market structure, liquidity sweeps, volume profiles, and institutional PD arrays. |
| **Setting tight stop-losses inside the sweep wick** | Micro-adjustments and local re-sweeps will hunt tight stops before the real expansion occurs. | Position the stop-loss entirely beyond the extreme distal line of the sweeping candle. |

## Quick Reference

| Concept | Abbreviation | Core Operational Definition | Key Validation Rule |
| :--- | :--- | :--- | :--- |
| **Break of Structure** | BOS | Continuation of the dominant HTF trend past a previous structural point. | Requires a confirmed candle body close beyond the swing point. |
| **Change of Character** | CHoCH | Reversal signal indicating a shift in market sentiment. | Validated by aggressive displacement and body close past an external level. |
| **Fair Value Gap** | FVG | Three-candle price imbalance indicating rapid, one-sided volume expansion. | Measured from the wick of candle 1 to the wick of candle 3. |
| **Consequent Encroachment** | CE | The precise 50% midpoint of a Fair Value Gap or shadow wick. | Serves as a major algorithmic level for reaction and entry. |
| **Unicorn Model** | UNICORN | High-probability setup combining a Breaker Block and an FVG. | The FVG must nest directly within the horizontal boundaries of the Breaker. |
| **Power of Three** | AMD | Daily price template: Accumulation, Manipulation, Distribution. | Asian range consolidates; London manipulates (sweeps); NY distributes. |
| **Optimal Trade Entry** | OTE | Fib retracement zone representing deep premium/discount. | Focuses on the 0.618 to 0.79 retracements, with 0.705 as the sweet spot. |
| **Balanced Price Range** | BPR | Overlap of a bullish and bearish FVG in the same price zone. | Represents immediate algorithmic rebalancing; entry at the midpoint. |