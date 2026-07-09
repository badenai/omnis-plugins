---
name: trade-execution-fvg
description: Use when identifying, validating, or executing trade setups based on Order Blocks (OB), Breaker Blocks, Mitigation Blocks, and Fair Value Gaps (FVG), including Consequent Encroachment (CE) and multi-timeframe PD array alignment.
---

## The Iron Law

```
Never execute a trade off a lower-timeframe FVG or Order Block unless it directly aligns with a higher-timeframe HTF discount/premium array, a major liquidity sweep, or a validated HTF Order Block.
```

## Behavioral Rules

*   **Validate the HTF Trend First:** Map the structural progression (HH/HL or LH/LL) on the higher timeframe (HTF) before looking for lower-timeframe (LTF) entries.
*   **Filter FVGs by Displacement Quality:** Only select FVGs created by displacement candles with a body-to-wick ratio above 70%. Discard or penalize FVGs created by weak, low-volume candle spreads (under 60% body-to-wick ratio).
*   **Calculate Consequent Encroachment (CE):** Identify the exact 50% midpoint of the FVG. Set your limit orders at this level for high-probability, algorithmic entries, or use it to validate a reaction (price must respect CE on a closing basis).
*   **Differentiate Breaker vs. Mitigation Blocks:**
    *   If the failed Order Block swept liquidity (stop hunt of a previous extreme) before the Market Structure Shift (MSS), categorize it as a **Breaker Block** (high priority).
    *   If the failed Order Block did not sweep liquidity (exhaustion/failure swing) before the MSS, categorize it as a **Mitigation Block** (lower priority).
*   **Enforce Golden Zone Entry (OTE):** Ensure the Order Block or FVG aligns with the Optimal Trade Entry (OTE) zone (61.8% to 79.0% Fibonacci retracement) of the structural dealing range. Do not buy in Premium or sell in Discount.
*   **Apply Polarity Flips (IFVG):** If price closes decisively beyond a bullish FVG, flip its polarity to a bearish Inverse FVG (IFVG) and treat it as resistance on subsequent retests. Apply the same logic inversely to bearish FVGs.
*   **Validate Liquidity Sweeps with Candle Closes:** Treat a wick through a key level strictly as a liquidity sweep (stop hunt). Require a candle body close past a major external swing level to confirm a true Change of Character (CHOCH) or Break of Structure (BOS).
*   **Utilize the Unicorn Model:** Search for the horizontal overlap of an ICT Breaker Block and an FVG formed during a high-displacement leg following a liquidity sweep for an A+ setup.

## Red Flags

| Red Flag | Rationalization | Why Wrong |
| :--- | :--- | :--- |
| Trading every LTF FVG | "An FVG is an algorithmic imbalance, so price must react to it immediately." | Up to 84% of LTF FVGs that get filled immediately reverse and break structure if they do not align with HTF context or liquidity sweeps. |
| Buying OBs in Premium / Selling OBs in Discount | "The Order Block looks clean and strong on the M15 chart." | Institutional order flow operates on premium/discount arrays. Trading against HTF premium/discount leads to high-probability stop outs. |
| Marking a wick-only break as a structural transition | "Price broke the previous high, so this is a bullish Change of Character." | A wick-only breach is a liquidity sweep (stop hunt) designed to engineer liquidity before a reversal. A true CHOCH requires a body close. |
| Treating Mitigation Blocks as equal to Breaker Blocks | "Both are failed order blocks, so they carry the same entry weight." | Breaker Blocks contain swept resting liquidity (stop losses) from the previous extreme, making them structurally superior and far more reactive. |

## Quick Reference

| PD Array Type | Definition / Key Characteristic | Best Execution / Invalidations |
| :--- | :--- | :--- |
| **Order Block (OB)** | Last candle before a decisive, aggressive expansion leg | Invalidation: Candle body close beyond the opening price of the OB. |
| **Fair Value Gaps (FVG)** | 3-candle imbalance; empty space between candle 1 and candle 3 wicks | Best entry: Consequent Encroachment (50% midpoint). |
| **Breaker Block** | Failed OB that swept liquidity before the structural shift (MSS) | High-priority entry zone when overlapped with an FVG (Unicorn Model). |
| **Mitigation Block** | Failed OB that failed to sweep liquidity before the structural shift | Lower-priority entry; requires clear volume confirmation. |
| **Inverse FVG (IFVG)** | An FVG that was decisively breached on a candle close basis | Retest entry: Flips polarity to act as support/resistance. |
| **Balanced Price Range (BPR)** | Horizontal overlap of a bullish FVG and a bearish FVG | Ultra-fast delivery zone; acts as a highly reactive, tight entry anchor. |