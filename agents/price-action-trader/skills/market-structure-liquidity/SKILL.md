---
name: market-structure-liquidity
description: Use when analyzing market structure, identifying structural shifts (BOS, CHOCH, MSS), validating high-probability Order Blocks, Breakers, and BPRs, or evaluating liquidity sweeps (BSL/SSL) to define precise institutional trade setups.
---

## The Iron Law

```
Never validate an Order Block (OB) or execute a trade setup without a verified prior Liquidity Sweep (BSL/SSL) followed by immediate, aggressive displacement that creates a structural shift (BOS/CHOCH/MSS) leaving an unmitigated FVG or BPR. No sweep, no trade.
```

## Behavioral Rules

*   **Confirm Structural Transitions:** If identifying a Change of Character (CHOCH) or Market Structure Shift (MSS), distinguish it from a minor inducement trap by requiring a clear candle body close past key structural levels on the higher timeframe.
*   **Validate Order Blocks (OB):** Strictly enforce the three rules of OB validation before taking an entry: verify it originates a structural break (BOS/CHOCH), displays aggressive displacement leaving behind an FVG, and remains completely unmitigated.
*   **Map Premium and Discount Zones:** Execute buy entries strictly within discount zones (below the 50% equilibrium mark of the current trading range) and sell entries strictly within premium zones (above the 50% equilibrium mark).
*   **Differentiate Failures and Sweeps:** Prioritize Breaker Blocks (failed OBs broken after a successful liquidity sweep) over Mitigation Blocks (failed OBs broken after a failure swing without a sweep), as mitigation blocks carry a lower institutional probability.
*   **Apply the Power of Three (AMD):** Frame daily cycles around Accumulation (Asian session consolidation), Manipulation (London session Judas Swing sweeping extremes), and Distribution (New York session expansion).
*   **Identify Balanced Price Ranges (BPR):** Locate BPRs only when an explosive expansion is immediately countered by an aggressive contraction, creating overlapping bullish and bearish FVGs; use these boundaries as ultra-high-probability defense barriers.
*   **Execute Confluent Entry Models:**
    *   *Unicorn Model:* Enter at the exact intersection of a fresh Mitigation or Breaker Block with a Fair Value Gap (FVG) or Inverse FVG (iFVG).
    *   *Venom Model:* Place entries directly at BPR boundaries formed immediately after a major liquidity sweep within strict 60-minute macro windows.
    *   *IOFED Model:* Place the limit order directly at the proximal edge of the FVG instead of waiting for a 50% equilibrium fill when executing during high-displacement moves.

## Red Flags

| If you see/hear... | Why it is wrong / Corrective action |
| :--- | :--- |
| Labeling any random opposing candle as a valid institutional "Order Block." | **Do not label candles without displacement as OBs.** Require an immediate, explosive expansion that leaves behind a valid FVG and breaks structure. |
| Trading a Mitigation Block in isolation without identifying a prior liquidity sweep. | **Avoid trading failure swings without HTF narrative backing.** Prioritize Breaker Blocks that leverage the fuel of trapped retail stops. |
| Classifying a minor wick-only break of a key level as a confirmed CHOCH/MSS. | **Never accept wicks as structural shifts.** Treat wick-only breaks as liquidity sweeps; require a higher timeframe candle body close to confirm a change in trend. |
| Entering trades at the 50% equilibrium mark during low-volatility accumulation phases. | **Do not chase price within consolidation.** Wait for the algorithm to sweep resting session liquidity pools (BSL/SSL) before executing. |
| Placing orders outside of premium/discount parameters because of a strong momentum narrative. | **Never chase momentum.** If price is not in a discount zone for longs or a premium zone for shorts, wait for a deep retracement to an unmitigated FVG or BPR. |

## Quick Reference

| Structure / Concept | Primary Function | Validation Criteria | Target Execution Entry |
| :--- | :--- | :--- | :--- |
| **BOS (Break of Structure)** | Trend Continuation | Clear candle body close past a previous swing high or low in a trending market. | Retracement to an unmitigated FVG or OB within the discount/premium range. |
| **CHOCH / MSS** | Trend Reversal | First structural shift accompanied by aggressive counter-trend displacement. | Retracement to the newly created FVG, iFVG, or Breaker Block. |
| **Liquidity Sweep (BSL / SSL)** | Market Manipulation / Fuel | Rapid wick purge of PDH, PDL, or session extremes followed by immediate rejection. | Switch to lower timeframe; enter on the subsequent MSS. |
| **Breaker Block** | Retailing Trap | Failed order block broken through *after* a successful liquidity sweep. | Place limit order at the breaker zone boundary; expect minimal drawdown. |
| **Balanced Price Range (BPR)** | Algorithmic Equilibrium | Horizontal overlap of a bullish FVG and a bearish FVG from violent two-way delivery. | Direct entry at BPR boundaries during active macro windows. |
| **Unicorn Model** | Dual-Confirmation Entry | Convergence of a Mitigation/Breaker Block directly overlapping a fresh FVG or iFVG. | Place entry at the exact intersection of the block and the imbalance. |