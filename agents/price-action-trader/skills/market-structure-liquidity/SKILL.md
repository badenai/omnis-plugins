---
name: market-structure-liquidity
description: Use when analyzing market structure (BOS, CHOCH, IDM), identifying institutional liquidity pools (BSL, SSL, sweeps), or evaluating price delivery models (FVG, OB, BPR, Breaker Blocks) to define trade setups.
---

## The Iron Law

```
A structural shift (BOS, CHOCH, or MSS) is strictly INVALID unless the candle body closes past the structural swing extreme. Wick rejections without body closes must be classified as liquidity sweeps (stop hunts), never as structure breaks.
```

## Behavioral Rules

*   **Determine Higher Timeframe (HTF) Bias First:** You must always map the HTF trend (Daily/4H) before looking for lower timeframe (LTF) entries. Never execute an LTF trade that goes directly against HTF structural alignment.
*   **Differentiate CHOCH from Inducement (IDM):** If the price breaks an internal minor structure point without confirming an external HTF swing point, you must label this as Internal Inducement (IDM), not a Change of Character (CHOCH).
*   **Validate Breakers vs. Mitigation Blocks:** You must only classify a failed order block as a Breaker Block if price swept a liquidity pool (manipulation/stop hunt) prior to the structural shift. If no sweep occurred, you must classify it as a lower-probability Mitigation Block.
*   **Apply the Unicorn Model Filter:** When evaluating a Unicorn setup, you must confirm that the Fair Value Gap (FVG) overlaps horizontally with the Breaker Block range. If the FVG sits entirely outside the Breaker Block, do not classify it as a Unicorn.
*   **Enforce Session Killzones:** You must reject any intraday entry pattern that occurs outside of the designated Killzone operating windows: London Open (2:00 AM – 5:00 AM ET), New York Open (8:30 AM – 11:00 AM ET), or New York PM Session (1:30 PM – 4:00 PM ET).
*   **Apply the Power of Three (AMD) Sequence:** You must look for the three-phase sequence: Accumulation (Asian consolidation), Manipulation (London Judas swing sweeping Asian highs/lows), and Distribution (New York expansion towards HTF targets).
*   **Filter Entries Using Body-to-Wick Ratios:** When using Balanced Price Ranges (BPR) or FVGs for execution, you must verify that the displacement candles driving the move have a body-to-wick ratio above 70%. If the ratio is under 60%, you must reduce target expectations (maximum 1.3R) or pass on the setup due to poor momentum.
*   **Locate Reaper Inversion FVGs in Premium/Discount:** In bullish setups, you must verify that the Reaper Inversion FVG resides in the discount portion of the impulsive leg. In bearish setups, you must verify that it resides in the premium portion.
*   **Require Volumetric Absorption for Sweep Confirmation:** When validating a liquidity sweep on an active chart, you must look for footprint absorption (large market order volume stalls and reverses) or delta-price divergence rather than assuming a sweep guarantees an immediate reversal.

## Red Flags

| Red Flag | Real-Time Reality / Why It's Wrong | Correct Market Action |
| :--- | :--- | :--- |
| **Wick CHOCH** | Classifying a wick past a swing point as a structural shift, leading to entering trades against the dominant trend. | Classify the wick as a liquidity sweep (stop hunt) and wait for a body close to confirm a true CHOCH/MSS. |
| **Chasing IDM Breakouts** | Treating internal structural breaks (Inducements) as major trend reversals. | Wait for the market to run the inducement level into an unmitigated HTF PD Array before looking for entries. |
| **Out-of-Session Execution** | Entering trades during the low-volume Asian session or mid-day lull. | Limit execution strictly to the London Open, New York Open, and New York PM Killzones. |
| **Improper Breaker Mapping** | Labeling a failed order block as a "Breaker" when the prior leg failed to sweep liquidity. | Downgrade the level to a Mitigation Block, demand higher timeframe alignment, and apply tighter risk parameters. |
| **Ignoring Displacement** | Entering on FVGs or BPRs formed by small, low-momentum candles with high wick-to-body ratios. | Filter for high-displacement candles (body-to-wick ratio > 70%) to ensure institutional presence. |

## Quick Reference

| Concept | Key Mechanics | Validation Rule |
| :--- | :--- | :--- |
| **BOS (Break of Structure)** | Continuation of dominant trend | Requires candle body close past prior swing high/low. |
| **CHOCH (Change of Character)** | First sign of trend reversal | Requires candle body close past major structural extreme. |
| **Inducement (IDM)** | Minor internal structural liquidity | Used as bait to trap retail before continuing HTF trend. |
| **Liquidity Sweep** | Price runs past swing high/low and rejects | Indicated by long wicks and footprint absorption. |
| **Unicorn Model** | Breaker Block $\cap$ Fair Value Gap | FVG must lie horizontally within the Breaker Block. |
| **BPR (Balanced Price Range)** | Overlapping bullish & bearish FVGs | Signals immediate algorithmic rebalancing & high-speed support/resistance. |
| **Consequent Encroachment** | 50% midpoint of FVG or shadow wick | Acts as an algorithmic gravity point for precise entry/defense. |
| **Power of Three (AMD)** | Accumulation $\rightarrow$ Manipulation $\rightarrow$ Distribution | Wait for manipulation (Judas swing) to sweep retail before entry. |