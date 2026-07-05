---
name: trade-execution-fvg
description: Use when executing, validating, or managing trades based on institutional order flow, Fair Value Gaps (BISI/SIBI), Consequent Encroachment, Breaker Blocks, and advanced PD arrays.
---

## The Iron Law

```
[The Execution Constraint]
Every execution trigger MUST align with a designated session Killzone (London Open 2:00-5:00 AM ET, NY Open 8:30-11:00 AM ET, or NY PM 1:30-4:00 PM ET) and reside strictly within a Premium (for short entries) or Discount (for long entries) array relative to the dealing range; execution outside these windows or within equilibrium is strictly forbidden.
```

## Behavioral Rules

### 1. Market Structure & Displacement Validation
* If a Break of Structure (BOS) or Change of Character (CHOCH/MSS) occurs, you must verify that the candle closed past the structural swing extreme with a full body; do not classify wick-only breaks as structural shifts, but rather as liquidity sweeps.
* If evaluating a structural shift, you must analyze the body-to-wick ratio of the displacement candle: if the ratio is above 70%, prioritize immediate execution models; if the ratio is below 60%, demand deeper retracements or reject the setup due to insufficient institutional momentum.
* If a minor internal structural break occurs without higher timeframe external swing validation, you must classify it as internal inducement (IDM); do not execute trades on these traps.

### 2. Fair Value Gap (FVG) & Consequent Encroachment (CE) Execution
* If executing at a Fair Value Gap, you must classify the imbalance as either a Buy-side Imbalance Sell-side Inefficiency (BISI) for longs or a Sell-side Imbalance Buy-side Inefficiency (SIBI) for shorts.
* If trading high-momentum, trend-dominant conditions, you may deploy the Institutional Order Flow Entry Drill (IOFED) by placing limit orders at the proximal edge (outer boundary) of the FVG.
* If trading standard mean-reverting or structural setups, you must place your execution limits at the exact 50% midpoint of the FVG, representing the Consequent Encroachment (CE).
* If a bullish FVG and a bearish FVG horizontally overlap in the same price band, you must label this a Balanced Price Range (BPR) and treat it as an immediate high-probability rebalancing entry zone.

### 3. Advanced Entry Model Selection (Unicorn, Venom, and Reaper)
* If executing the Unicorn Model, you must verify the exact horizontal overlap where a Fair Value Gap (FVG) sits directly inside the price range of a validated Breaker Block following an MSS.
* If executing the Venom Model, you must restrict entries strictly to the Balanced Price Range (BPR) immediately following a major liquidity sweep during an active session Killzone.
* If executing the Reaper Inversion FVG model, you must locate an Inversion FVG (invalidated FVG) that resides precisely inside the impulsive leg of a Breaker Block, ensuring it lies in the discount portion for longs or the premium portion for shorts.
* If analyzing overlapping wicks of consecutive same-color candles on a higher timeframe, you must drill down to a lower timeframe to identify and mark the Hidden Order Block (HOB) hidden within the wick-overlap zone.
* If a candlestick body is completely overlapped by the wick of the prior candle on its left, preventing a standard FVG, you must map this as a Suspension Block sandwiched between volume imbalances and treat it as a valid support/resistance level.

### 4. Structural Reversal Block Classification
* If a structural block is broken, you must classify it as a Breaker Block only if price swept liquidity (accomplished a stop hunt) prior to the structural shift.
* If the broken block failed to sweep the previous extreme before reversing (exhaustion swing), you must classify it as a Mitigation Block and enforce tighter risk parameters due to its lower probability.

### 5. Order Flow & Volumetric Verification
* If executing at a key POI, you must confirm liquidity sweeps using footprint charts: look for high-volume passive limit order absorption (diagonal delta bids/asks stalling and reversing).
* If price sweeps a key level and prints a Delta-Price Divergence (e.g., a bullish candle close on highly negative net Delta), you must interpret this as passive institutional absorption and execute the reversal.

## Red Flags

| Red Flag | Rationalization | Why Wrong |
| :--- | :--- | :--- |
| Wick-Only Break of Structure | "The price swept past the old high, so the trend must be continuing upward." | Wick-only breaks without candle body closes indicate liquidity sweeps, not structural continuation. |
| Executing at Equilibrium | "The price is cheap enough and is Reacting to a small 5m FVG." | Entering at equilibrium or within the wrong pricing array (buying premium/selling discount) destroys R:R. |
| Mitigation Block as Breaker Block | "This block reversed the price, so it's a high-probability entry." | Without a prior liquidity sweep, a mitigation block represents trend fatigue and has high failure rates. |
| Disregarding Killzones | "The pattern is perfect; it doesn't matter that it's 1:00 PM ET." | Institutional algorithms do not distribute price efficiently outside operating Killzones, leading to high slippage and noise. |
| Ignoring Inversion FVG Location | "The Inversion FVG is valid anywhere on the chart." | A valid Reaper Inversion FVG must sit strictly in discount for bullish setups and premium for bearish setups. |

## Quick Reference

| Term / Setup | Primary Location / Condition | Execution Trigger / Metric |
| :--- | :--- | :--- |
| **BISI** | Discount array during Killzone | Entry at proximal edge (IOFED) or 50% Consequent Encroachment (CE) |
| **SIBI** | Premium array during Killzone | Entry at proximal edge (IOFED) or 50% Consequent Encroachment (CE) |
| **Unicorn Model** | Overlap: Breaker Block $\cap$ FVG | High displacement MSS body close + FVG inside Breaker range |
| **Venom Model** | Balanced Price Range (BPR) | Post-liquidity sweep horizontal FVG overlap; >70% body-to-wick |
| **Reaper Inversion** | Impulsive leg of Breaker Block | Failed FVG (Inversion) aligned in Premium (short) / Discount (long) |
| **Breaker Block** | Post-Liquidity Sweep + MSS | Reversal key level backed by executed retail stop-loss clusters |
| **Mitigation Block** | Failure Swing (No Sweep) + MSS | Exhaustion level; requires tighter risk and strict HTF alignment |
| **Suspension Block** | Sandwich between volume imbalances | Candlestick body completely overlapped by prior candle's wick |