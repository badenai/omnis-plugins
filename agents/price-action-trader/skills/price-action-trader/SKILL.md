---
name: price-action-trader
description: Use when analyzing market structure, identifying institutional footprints (such as Order Blocks or Fair Value Gaps), locating liquidity pools, and drafting risk-managed trade setups.
filePattern: "**/*.md"
---

## The Iron Law

```markdown
Every market analysis, structural mapping, or trade setup MUST begin with the Higher Timeframe (HTF) trend, proceed to identify liquidity pools, isolate institutional imbalances within premium/discount arrays, and execute ONLY upon explicit lower-timeframe structural shifts or volume validation. Under no circumstances will lagging indicator systems be used to justify a trade.
```

## Behavioral Rules

*   **Define Market Structure with Precision:** 
    *   Classify structural continuations (BOS) only when a candle body closes past the previous swing high/low. 
    *   Treat wick breaks strictly as liquidity sweeps or minor internal swings.
    *   Distinguish CHOCH as the first internal structural warning, and MSS as a confirmed institutional shift characterized by aggressive displacement on the execution timeframe.
*   **Locate Liquidity Pools:** 
    *   Map major external swing highs as Buy-Side Liquidity (BSL) and major swing lows as Sell-Side Liquidity (SSL).
    *   Identify double/triple tops and bottoms as Equal Highs (EQH) and Equal Lows (EQL) to isolate retail stop clusters.
    *   Treat minor internal structural breaks as Inducement (IDM) to avoid early breakout traps.
*   **Enforce Premium vs. Discount Arrays:** 
    *   Measure the current dealing range using Fibonacci frameworks.
    *   Restrict long entries to the Discount zone (bottom 50% of the range) and short entries to the Premium zone (top 50% of the range).
    *   Prioritize Optimal Trade Entry (OTE) levels between the 0.618 and 0.79 Fibonacci retracements.
*   **Evaluate Institutional Imbalances:** 
    *   Identify Fair Value Gaps (FVG) as three-candle price imbalances where the wicks of the first and third candles do not overlap.
    *   Validate the 50% midpoint of an FVG or candle shadow as Consequent Encroachment (CE).
    *   Reverse FVG polarity (IFVG) if a candle closes decisively past the imbalance zone.
    *   Locate Balanced Price Ranges (BPR) where bullish and bearish FVGs overlap horizontally.
*   **Identify Institutional footprints:** 
    *   Isolate the last candle before a decisive market expansion as an Order Block (OB).
    *   Map Breaker Blocks (BB) when price sweeps a structural extreme and completes an MSS.
    *   Map Mitigation Blocks (MB) when price fails to sweep the extreme (failure swing) before reversing.
    *   Look for Unicorn Model setups at the horizontal overlap of a Breaker Block and an FVG.
*   **Align Time and Price:** 
    *   Restrict executions to ICT Kill Zones: London Open (2:00 AM – 5:00 AM ET), New York Open (8:30 AM – 11:00 AM ET), and New York PM (1:30 PM – 4:00 PM ET).
    *   Verify Silver Bullet protocols during London Open (3:00–4:00 AM EST), New York AM (10:00–11:00 AM EST), or New York PM (2:00–3:00 PM EST).
    *   Apply the Power of Three (AMD): Accumulation (consolidation), Manipulation (Judas swing), and Distribution (expansion).
*   **Apply Volumetric and Structural Invalidation:** 
    *   Validate liquidity sweeps by verifying passive limit-order absorption (heavy volume spike with no expansion, combined with Cumulative Delta Divergence).
    *   Wait for lower-timeframe MSS with displacement following a HTF sweep; do not enter blindly on limit orders.
    *   Place stop-losses mechanically beyond the distal extreme of the sweep wick.

## Red Flags

| Retold Narrative (Wrong) | Objective Market Reality (Right) | Why It Is Wrong |
| :--- | :--- | :--- |
| "RSI is oversold, meaning the market is ready to reverse and we should buy." | "The market is in a structural downtrend; RSI is staying low because order flow is heavily bearish." | Lagging indicators do not drive price; price moves to sweep liquidity and resolve imbalances regardless of RSI boundaries. |
| "A wick broke above the previous swing high, confirming a bullish Break of Structure (BOS)." | "A wick break is a liquidity sweep (stop hunt) targeting buy-side liquidity before a reversal." | A valid BOS requires a body close. Entering on wick breaks traps traders at the exact moment institutions exit positions. |
| "This 15-minute FVG is a guaranteed reversal entry zone because the market always fills gaps." | "Up to 84% of lower-timeframe FVGs fail or act as traps unless aligned with HTF order flow and a sweep." | FVGs are highly random in isolation; treating every minor imbalance as a limit order trigger leads to heavy losses. |
| "Placing my stop-loss tightly inside the sweep wick to maximize my risk-to-reward ratio." | "Stop-losses must be placed mechanically beyond the distal extreme of the sweep wick." | Placing tight stops inside the sweep structure makes the position vulnerable to secondary sweeps and algorithmic noise. |
| "Entering a long position in the premium zone because the trend is very strong." | "Long positions must be executed strictly in the discount zone (below the 50% equilibrium level)." | Buying in the premium zone of a dealing range reduces the probability of success and increases the risk of drawdown. |

## Quick Reference

```
+-------------------------------------------------------------------------+
|                         STRUCTURAL HIERARCHY                            |
+=========================+===============================================+
| Break of Structure      | Candle body close past previous swing extreme.|
| CHOCH / MSS             | Displacement past local swing; change in flow.|
| Inducement (IDM)        | Minor internal break designed to trap breakout.|
+-------------------------+-----------------------------------------------+

+-------------------------------------------------------------------------+
|                       PRICING & IMBALANCE ARRAYS                        |
+=========================+===============================================+
| Premium / Discount      | Equilibrium at 50%; buy Discount, sell Premium|
| Optimal Trade Entry     | Fibonacci retracement levels 0.618 to 0.79    |
| Fair Value Gap (FVG)    | 3-candle imbalance; wicks do not overlap      |
| Consequent Encroachment | The exact 50% midpoint of an FVG or wick      |
| Balanced Price Range    | Overlap of a bullish FVG and a bearish FVG    |
| Unicorn Model           | Horizontal overlap of a Breaker Block and FVG |
+-------------------------+-----------------------------------------------+

+-------------------------------------------------------------------------+
|                           ALGORITHMIC SCHEDULE                          |
+=========================+===============================================+
| London Open Kill Zone   | 2:00 AM – 5:00 AM ET                          |
| NY Open / Silver Bullet | 8:30 AM – 11:00 AM ET                         |
| NY PM Kill Zone         | 1:30 PM – 4:00 PM ET                          |
| Silver Bullet Hour (AM) | 10:00 AM – 11:00 AM ET (Highest Probability)  |
+-------------------------+-----------------------------------------------+
```