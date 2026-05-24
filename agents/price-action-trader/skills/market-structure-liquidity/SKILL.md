---
name: market-structure-liquidity
description: Use when analyzing market structure, mapping liquidity pools, identifying trend shifts (BOS/CHOCH), verifying liquidity sweeps/grabs, or validating structural levels for entry/exit execution.
---

## The Iron Law

```
Do not classify any structural break (BOS or CHOCH) without a candle body close past the key external swing level; any break made via wick-only must be treated strictly as a liquidity sweep.
```

## Behavioral Rules

*   **Define Structural Transitions:** If identifying a trend transition, classify the first structural shift of a major swing level as a Change of Character (CHOCH) and subsequent trend-aligned breaks as a Break of Structure (BOS).
*   **Validate via Displacement:** Require a clean candlestick body close with high relative displacement to confirm structural transitions; treat wick-only breaks as sweeps or stop hunts.
*   **Enforce Pricing Arrays:** Only search for sell setups in the Premium Zone (above the 50% equilibrium of the dealing range) and buy setups in the Discount Zone (below the 50% equilibrium).
*   **Map Session Cycles:** Identify Consolidation (Accumulation) during the Asian session, expect an engineered false breakout (Manipulation/Judas Swing) during the London session to sweep extremes, and trade the heavy displacement (Distribution) during the New York session.
*   **Differentiate Structural Levels:** Do not confuse minor internal structure breaks (Inducement/IDM) with high-probability trend shifts; map the true CHOCH only at major external high/low boundaries.
*   **Filter Order Blocks (OB):** Validate an OB only if it initiated a structural break (BOS/CHOCH) that swept liquidity, generated immediate displacement leaving an unmitigated Fair Value Gap (FVG), and remains completely untouched (unmitigated).
*   **Prioritize Traps over Failure Swings:** Target Breaker Blocks (blocks that swept liquidity before breaking structure) rather than standard Mitigation Blocks (failure swings that did not sweep liquidity) to maximize entry confirmation.
*   **Assess Sweep Scale:** Classify broad, multi-price level manipulation beyond daily/weekly/session extremes as a Liquidity Sweep (signaling high-timeframe reversal), and identify rapid, single-candle wick rejections as localized Liquidity Grabs (signaling near-term continuation).
*   **Integrate Volume Signs:** Correlate tick or transaction volume with structural sweeps; validate reversals when high volume accompanies a wick rejection at key extremes (Springs and Upthrusts).

## Red Flags

| Retail Rationalization | Why Wrong |
| :--- | :--- |
| "The wick broke the level, so the trend has officially reversed." | Wick-only breaks indicate liquidity absorption, not structural change. Expect immediate price reversals instead of trend continuation. |
| "Executing a buy limit inside a Discount OB that has already been tapped once." | Treat mitigation as binary. Do not re-enter an OB that has already been tapped, as institutional orders have been filled. |
| "This internal break of structure means I should jump in immediately." | Recognize internal breaks as engineered inducements. Wait for major external sweeps before entering. |
| "Entering a buy in the Premium Zone because the momentum is extremely strong." | Never buy in Premium zones. Execute longs only in Discount zones where institutions accumulate positions. |
| "Trading a structural breakout without any prior liquidity sweep." | Avoid trading breaks lacking prior liquidity sweeps. Focus execution strictly on Breaker Blocks that trapped participants. |

## Quick Reference

| Concept | Primary Condition | Action/Execution |
| :--- | :--- | :--- |
| **Change of Character (CHOCH)** | Candle body closes past major external swing high/low | Identify primary trend shift; wait for mitigation of new POIs. |
| **Break of Structure (BOS)** | Candle body closes in the direction of dominant HTF trend | Align execution with trend; target next key liquidity pool. |
| **Liquidity Sweep** | Price wicks past HTF key extreme (PDH/PDL, PW/PL) with displacement | Execute counter-trend entries upon low-timeframe CHOCH confirmation. |
| **Liquidity Grab** | Rapid, localized single-candle wick rejection of short-term liquidity | Enter immediate continuation setups in the direction of the trend. |
| **Inducement (IDM)** | Minor internal structural breaks designed to build liquidity | Avoid trading internal breaks; wait for HTF POI mitigation. |
| **Unicorn Model** | Overlap of a validated Breaker Block and an active FVG | Place limit entry at the exact intersection of both zones. |