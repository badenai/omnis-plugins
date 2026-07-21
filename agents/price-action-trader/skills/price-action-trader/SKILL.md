---
name: price-action-trader
description: Use when mapping market structure (BOS, CHOCH, MSS), identifying liquidity pools or sweeps, evaluating PD arrays (Premium/Discount, OBs, FVGs), or executing institutional entry protocols (Unicorn, Reaper IFVG, IOFED) within session Kill Zones.
---

## The Iron Law

```the-iron-law
A structural transition (BOS, CHOCH, or MSS) is strictly validated ONLY by a candle body close beyond the structural swing extreme on the analysis timeframe. Any breach by a wick must be classified as a liquidity sweep, not a structural break.
```

## Behavioral Rules

### 1. Market Structure & Liquidity Mapping
*   If a swing high or low is breached only by a candlestick wick, classify it as a liquidity sweep and prepare for a potential counter-move; do not map it as a trend continuation (BOS).
*   Map structural progression strictly via Higher Highs/Higher Lows in uptrends and Lower Highs/Lower Lows in downtrends using candle body closes to confirm validity.
*   Distinguish between Change of Character (CHOCH) and Market Structure Shift (MSS) by requiring strong displacement (aggressive momentum candles) to confirm an MSS.
*   Treat equal highs (EQH) and equal lows (EQL) as high-priority draw-on-liquidity targets; expect these retail clusters to be swept before any sustained reversal.
*   Identify failure swings (where the market fails to make a higher high/lower low) as low-resistance liquidity pools that the market algorithm will target.
*   Drop to lower execution timeframes (1m/5m) to wait for an explicit MSS candle close following an HTF liquidity sweep; never execute blind single-sweep entries.

### 2. Premium/Discount & PD Array Selection
*   Divide every active dealing range into Premium (top 50%), Equilibrium (50%), and Discount (bottom 50%).
*   Execute long setups strictly within Discount arrays and short setups strictly within Premium arrays.
*   Map the Optimal Trade Entry (OTE) zone using a Fibonacci retracement from the true structural anchor of the impulse leg, targeting the 0.618 to 0.79 range with 0.705 as the sweet spot midpoint.
*   Verify order blocks (OB) on structured retests; prioritize Breaker Blocks (failed OBs after a liquidity sweep and MSS) over Mitigation Blocks (failed OBs from failure swings).
*   Track the exact 50% midpoint of Fair Value Gaps (FVG) or long wick shadows as Consequent Encroachment (CE), and treat it as a critical algorithmic reaction level.
*   Classify an FVG as an Inversion FVG (IFVG) only when price decisively closes with a full candle body past its outer boundary.

### 3. Entry Protocols & Timing
*   Execute the Unicorn Model strictly at the horizontal overlap of an ICT Breaker Block and an ICT FVG.
*   Execute the Reaper IFVG model only if an Inversion FVG sits entirely within the impulsive price leg of a breaker block.
*   Utilize the Institutional Order Flow Entry Drill (IOFED) for high-momentum trends only when a retracement fills less than 50% of an FVG (respecting CE) before reversing aggressively.
*   Restrict execution strictly to session Kill Zones: London Open (2:00 – 5:00 AM ET), New York Open (8:30 – 11:00 AM ET), and New York PM (1:30 – 4:00 PM ET).
*   Enforce the strict Silver Bullet windows (10:00 – 11:00 AM ET and 2:00 – 3:00 PM ET) for high-probability setups.
*   Stand down and discard the setup entirely if a single parameter of the 7-Rule Silver Bullet Entry Protocol is missing.

### 4. Risk & Operational Mechanics
*   Scale contract sizing dynamically and inversely to the structural stop-loss width so that cash risk remains absolute (e.g., exactly 1% per trade).
*   Place stop-losses strictly beyond the absolute extreme of the liquidity sweep wick to survive algorithmic re-testing.
*   Cease trading and close the platform immediately for the day upon committing three operational errors (Three-Mistake Rule).
*   Synchronize contract sizing with the firm's dynamic risk engine if operating under a proprietary trading firm's Floating Risk Rule.

## Red Flags

| Retail Rationalization | Why It Is Wrong (Institutional Reality) |
| :--- | :--- |
| "A wick broke the previous swing high, so the uptrend is continuing. I will buy the breakout." | Wicks represent liquidity sweeps or stop hunts. Buying a wick breakout traps you at the exact turning point before a reversal. |
| "This 5-minute FVG printed, so I will place a limit order to buy the immediate retest." | Statistically, up to 84% of LTF FVGs fail or break structure if they are not aligned with HTF order blocks or discount arrays. |
| "A liquidity sweep occurred; I must enter on market immediately so I do not miss the move." | Over 30% of first sweeps are inducement traps. You must wait for an LTF MSS candle close and position stops past the sweep wick. |
| "The pattern looks clean, so I will trade it at 12:30 PM ET during lunch hour." | Trading outside session Kill Zones lacks institutional algorithm delivery, exposing you to low-volume chop and manipulation. |
| "I will widen my stop past the structure to give this order block room to breathe." | Moving stops invalidates risk-to-reward ratios and signals emotional trading. Stops must remain fixed at structural extremes. |

## Quick Reference

| Concept | Trigger/Execution Condition | Stop-Loss / Target Placement |
| :--- | :--- | :--- |
| **BOS (Break of Structure)** | Candle body close past prior structural swing extreme on HTF. | Stop-loss at the invalidation swing low/high; target opposing external liquidity. |
| **Liquidity Sweep** | Wick breaches swing high/low or EQH/EQL and closes back inside. | Stop-loss strictly beyond the absolute sweep wick extreme; target internal liquidity/FVG. |
| **Unicorn Model** | Price retraces to the horizontal overlap of an ICT Breaker Block and an FVG. | Stop-loss past the extreme of the Breaker Block; target OTE extremes or major external liquidity. |
| **Silver Bullet** | Time of day is 10:00–11:00 AM ET or 2:00–3:00 PM ET; 7-rule checklist is fully met. | Stop-loss past the local swing structural anchor; target minimum 2R or next HTF liquidity pool. |
| **Reaper IFVG** | Inversion FVG resides strictly within the impulsive leg of a breaker block. | Stop-loss past the breaker block boundary; target opposing pool or discount/premium extreme. |