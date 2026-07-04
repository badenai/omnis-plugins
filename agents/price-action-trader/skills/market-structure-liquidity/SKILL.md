---
name: market-structure-liquidity
description: Use when analyzing market structure, defining trend transitions, evaluating liquidity sweeps, determining order blocks, fair value gaps, or identifying precise price action entry models like the Unicorn or Venom.
---

## The Iron Law

```
Never map a Market Structure Shift (MSS), Change of Character (CHOCH), or Break of Structure (BOS) without verifying whether the price closed past the swing level with structural volume displacement, or merely swept liquidity. A wick-only breach of a key swing level is a liquidity sweep, not a structural breakout.
```

## Behavioral Rules

*   If the price sweeps a key liquidity extreme (stop hunt) and then completes a high-velocity structural shift, classify the resulting failed order block as a Breaker Block.
*   If the price fails to sweep the previous extreme (failure swing) before reversing through a previous order block, classify the zone as a Mitigation Block and enforce tighter risk parameters.
*   If analyzing Fair Value Gaps (FVG), verify if a candle has closed completely past its boundary; if so, immediately flip its role to an Inverse Fair Value Gaps (IFVG).
*   If mapping premium/discount arrays, label overlapping bullish and bearish FVGs as a Balanced Price Range (BPR) and treat it as a high-velocity, low-drawdown algorithmic equilibrium zone.
*   If a candlestick's body is completely overlapped by the wick of the prior candle on its left and sits suspended between an upper and lower volume imbalance, classify it as a Suspension Block and mark it as an algorithmic reload zone.
*   If looking for a Hidden Order Block (HOB) on a high-timeframe (HTF) wick-overlap zone, drill down to lower timeframes (LTF) to find the fully formed, unmitigated traditional order block.
*   If executing the ICT Unicorn Model, ensure the Fair Value Gap (FVG) forms horizontally overlapping with, or directly within, the price range of the validated Breaker Block.
*   If executing the ICT Reaper Inversion FVG Model, verify that the Inversion FVG resides precisely inside the impulsive price leg of the Breaker Block, ensuring it sits in the discount portion for long setups or the premium portion for short setups.
*   If executing the Venom Model, execute market entries strictly at the boundary of a newly formed Balanced Price Range (BPR) during session Killzones, targeting high-timeframe external liquidity pools.
*   If using the Institutional Order Flow Entry Drill (IOFED) on high-momentum trends, place the limit order directly at the proximal edge of the FVG rather than waiting for a 50% consequent encroachment fill.
*   If confirming a liquidity sweep via order flow/footprint data, require diagonal buy/sell imbalances exceeding a 3:1 ratio (absorption) accompanied by stalling price action.
*   If a breakout displays neutral or exhausted volume delta, classify it as Inducement (IDM) and treat it as a trap rather than a genuine Break of Structure (BOS).

## Red Flags

| Red Flag | Why It Is Wrong | Correct Action |
| :--- | :--- | :--- |
| Treating a wick-only breach of a swing high/low as a Break of Structure (BOS). | A wick breach without candle body confirmation represents a liquidity run/stop hunt, not structural expansion. | Classify it as a liquidity sweep and look for a reversal pattern. |
| Refinement to a single refined Order Block (OB) ignoring structural Order Flow (OF). | Price often mitigates the broader corrective pullback leg (Order Flow) rather than reaching a deep, highly refined OB, leading to missed trades. | Evaluate the entire corrective sequence of candles before the BOS as the mitigation zone. |
| Treating a Mitigation Block with the same probability as a Breaker Block. | Mitigation blocks do not clear liquidity prior to reversal (failure swing) and represent trend exhaustion, making them more prone to failure. | Enforce tighter risk parameters and wait for additional lower-timeframe structural validation. |
| Using "volume footprint" and Cumulative Volume Delta (CVD) metrics on retail Forex spot charts without acknowledging OTC limitations. | Forex is non-centralized; retail broker volume is a localized tick proxy and does not represent global institutional transactions. | Treat OTC footprint indicators as auxiliary data; prioritize raw price delivery, HTF structural levels, and centralized futures volume where available. |
| Automatically placing limit orders at 50% consequent encroachment on every FVG. | In high-momentum, aggressive institutional expansions, the market will often run from the proximal edge without filling deeper bids. | Use the IOFED technique to enter directly at the proximal boundary of the FVG in high-momentum states. |

## Quick Reference

| Concept | Structural Trigger | Execution / Target Rule |
| :--- | :--- | :--- |
| **Breaker Block** | Liquidity Sweep + MSS/CHOCH. | High-probability entry zone; highly resilient to deep drawdown. |
| **Mitigation Block** | Failure Swing + MSS/CHOCH. | Trend exhaustion entry; requires tighter stops and conservative targets. |
| **Balanced Price Range (BPR)** | Horizontally overlapping bullish & bearish FVGs. | Algorithmic equilibrium; tight target with immediate reaction expected. |
| **Suspension Block** | Candlestick body overlapped by prior wick between twin volume imbalances. | High-reliability institutional reload zone. |
| **Unicorn Model** | Horizontal overlap of a Breaker Block and an FVG. | Double-pressure entry model; place stop beyond the breaker swing extreme. |
| **Reaper Inversion FVG** | Inversion FVG inside the premium (short) / discount (long) of a Breaker's impulsive leg. | Hidden institutional reload zone targeting early breaker-block failures. |
| **Venom Model** | BPR formation immediately after a liquidity sweep during Killzones. | Rapid execution targeting HTF external liquidity pools. |
| **Inducement (IDM)** | Structural break with low or exhausted volume delta. | Avoid entry; prepare for a reversal sweep of the breakout participants. |