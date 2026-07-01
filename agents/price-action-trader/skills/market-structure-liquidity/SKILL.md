---
name: market-structure-liquidity
description: Use when analyzing market structure, tracking BOS or CHOCH transitions, mapping liquidity sweeps, and detecting inducement traps.
---

## The Iron Law

```text
Never classify an internal or minor structure breach as a structural reversal (MSS/CHOCH) unless a candle body aggressively closes beyond a major external swing point; treat any sweep or wick-only breach strictly as a liquidity grab or inducement.
```

## Behavioral Rules

*   **Establish Higher-Timeframe Context:** Always conduct a top-down multi-timeframe analysis to identify the dominant market trend and primary key levels before mapping lower-timeframe structures.
*   **Validate Structural Shifts via Candle Closes:** If mapping structural reversals, require a full candle body close past a major external swing point before confirming a Change of Character (CHOCH) or Market Structure Shift (MSS).
*   **Treat Wicks as Liquidity Sweeps:** Treat any wick penetration that fails to close past an external level strictly as a liquidity sweep or stop hunt.
*   **Apply Strict Order Block Validation:** When identifying Order Blocks (OB), validate them only if they originate a BOS or CHOCH, create a Fair Value Gap (FVG), and remain entirely unmitigated.
*   **Filter Breakers from Mitigation Blocks:** Distinguish Breaker Blocks from Mitigation Blocks by verifying that the Breaker successfully swept liquidity (engineered a stop hunt) before the structural shift occurred.
*   **Restrict Execution to Premium/Discount Arrays:** Restrict all buy executions to the Discount zone (below the 50% Fibonacci equilibrium of the dealing range) and all sell executions to the Premium zone (above the 50% level).
*   **Identify and Avoid Inducement Traps:** Identify structural Inducement (IDM) as minor, internal breaks designed to trap early breakout traders; do not execute trades on these levels.
*   **Monitor the Session Cycle (AMD):** Anticipate consolidation during the Asian session (Accumulation), a fakeout or sweep during the London session (Manipulation), and true directional expansion during the New York session (Distribution).
*   **Confirm Sweeps with Order Flow Volume:** If validating a liquidity sweep with footprint charts, verify absorption via high passive volume limits holding price, followed by initiation confirmation via delta divergence.

## Red Flags

| Domain-specific rationalizations | Why wrong |
|---|---|
| "The price wicked past the previous session high, which means the market has broken structure and we must immediately enter a breakout trade." | Never mistake a wick rejection for a structural break; treat wick penetrations as liquidity sweeps and wait for a full candle body close to confirm structural shifts. |
| "We can trade this order block because it represents the last opposing candle before a minor price run." | Do not validate an order block unless it actively originates a BOS/CHOCH, generates a Fair Value Gap (FVG), and remains unmitigated. |
| "A Change of Character occurred on the 1-minute chart, so we should immediately execute a position against the 4-hour trend." | Never execute counter-trend trades based on low-timeframe structural shifts unless they align with higher-timeframe premium/discount arrays. |
| "The momentum is extremely bullish, so we can buy a breakout within the Premium zone of the current dealing range." | Never execute long positions inside the Premium zone; restrict buy orders to the Discount zone to avoid being trapped by institutional reversals. |

## Quick Reference

| Structural Element | Key Validation Criteria | Trading Action |
|---|---|---|
| **BOS (Break of Structure)** | Confirm a full candle body close past a swing point in the direction of the dominant HTF trend. | Search for continuation entries aligned with the trend. |
| **MSS / CHOCH** | Verify a strong candle body close past a key external swing high or low. | Prepare for a structural trend reversal and map new Premium/Discount arrays. |
| **Liquidity Sweep** | Identify a wick penetration of an external high or low followed by an immediate rejection. | Execute counter-sweep setups like the Unicorn or Venom models. |
| **Inducement (IDM)** | Identify minor internal structural breaks that fail to clear external swing liquidity. | Avoid entry and wait for the engineered liquidity to be swept. |
| **Breaker Block** | Locate a broken order block that successfully swept liquidity before the structural shift occurred. | Utilize as a high-probability mitigation or re-entry zone within the Unicorn model. |
| **BPR (Balanced Price Range)** | Locate a horizontal overlap of opposing FVGs created by rapid price delivery in both directions. | Target as a key equilibrium zone for high-precision, low-drawdown entries. |