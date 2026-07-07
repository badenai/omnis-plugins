---
name: market-structure-liquidity
description: Use when analyzing market structure, identifying structural transitions (BOS, CHOCH, IDM), mapping premium/discount arrays, locating institutional liquidity pools (BSL, SSL), or evaluating liquidity sweep and mechanical entry setups (Unicorn, Venom, OTE).
---

## The Iron Law

```
A structural transition (CHOCH/MSS) is valid ONLY if there is a decisive candle body close past the major external swing level. A simple wick through a level or a minor internal break is classified strictly as inducement (IDM) or a liquidity sweep, NEVER a structural break.
```

## Behavioral Rules

*   **Rule 1: Enforce Top-Down Multi-Timeframe Alignment**
    *   Do NOT map lower-timeframe (LTF) setups in isolation.
    *   First, identify the Higher Timeframe (HTF) Draw on Liquidity (DOL) and key Premium/Discount arrays.
    *   Second, wait for the HTF liquidity pool to be swept or mitigated before zooming down exactly two intervals (e.g., 4H to 15M) for LTF entry execution.

*   **Rule 2: Classify Structural Breaks with Precision**
    *   Label price continuation moves as Break of Structure (BOS) only after a clean candle body close in the direction of the dominant trend.
    *   Label trend reversals as Change of Character (CHOCH) or Market Structure Shift (MSS) only when displacement occurs past a major external swing point.
    *   Classify all sub-structural or non-displaced moves as Inducement (IDM) or liquidity sweeps.

*   **Rule 3: Qualify Liquidity Sweeps and Absorption**
    *   Confirm structural liquidity grabs (BSL/SSL) using footprint/volumetric delta data when available.
    *   A true sweep requires passive limit order absorption: look for a massive diagonal delta spike (aggressive market orders exceeding a 3x imbalance ratio) that fails to expand price, resulting in a candle close that opposes the aggressive flow.

*   **Rule 4: Execute Mechanical Entry Models strictly within Killzones**
    *   Only execute the ICT Unicorn Model (overlapping Breaker Block and FVG) or Venom Model (horizontal overlap of bullish and bearish FVGs establishing a Balanced Price Range) inside designated session windows: London Open (2:00 AM – 5:00 AM ET), NY Open (8:30 AM – 11:00 AM ET), or NY PM (1:30 PM – 4:00 PM ET).
    *   Set the immediate invalidation level at the outer swing extreme of the initial liquidity sweep.

*   **Rule 5: Grade Imbalances and BPRs by Candle Body Quality**
    *   Filter out low-momentum imbalances. Only grade Fair Value Gaps (FVGs) and Balanced Price Ranges (BPRs) as high-probability (A+ setups) if the forming displacement candles possess a body-to-wick ratio above 70%.

## Red Flags

| Red Flag | Rationalization | Why Wrong |
| :--- | :--- | :--- |
| Wicking past a swing level labeled as CHOCH/MSS | "It broke the level on the lower timeframe, so the trend has officially reversed." | Wicks only hunt liquidity. Labeling a wick-only sweep as a structural shift leads to trading directly into institutional manipulation. |
| Trading LTF structures without HTF context | "The 1-minute chart has a clean BOS and FVG, I can trade this trend continuation." | High-frequency noise yields a statistically negative expectancy when traded without parent Order Block or HTF liquidity alignment. |
| Entering trades mid-range without Premium/Discount mapping | "Price is moving fast, I need to buy now before it leaves without me." | Buying in Premium or selling in Discount zones destroys the risk-to-reward ratio and exposes the account to algorithmically engineered retracements. |
| Treating every minor break as a trend shift | "Price just took out the previous minor internal low, the trend is now bearish." | This is retail inducement (IDM) designed to trap early breakout traders before the real expansion occurs. |

## Quick Reference

| Concept | Structural Rule / Trigger | Target / Invalidation Zone | Execution Metric |
| :--- | :--- | :--- | :--- |
| **BOS (Break of Structure)** | Trend continuation; requires candle body close past swing high/low. | Opposite structural swing low/high is the invalidation point. | Body-to-wick ratio > 70% on breakout candle. |
| **CHOCH / MSS** | Trend reversal; requires displacement and body close past major external swing. | Invalidation is the swing extreme of the reversal leg. | Exactly two timeframes lower for entry. |
| **Unicorn Model** | Horizontal overlap of an ICT Breaker Block and an ICT FVG. | Invalidation: candle body close beyond the initial liquidity sweep extreme. | Session Killzones only; limit order at proximal edge. |
| **Venom Model / BPR** | Horizontal overlap of bullish and bearish FVGs forming equilibrium. | Invalidation: outer boundaries of the BPR. | immediate entry at BPR boundary post HTF sweep. |
| **Optimal Trade Entry (OTE)** | Retracement of impulse leg into the 0.618 to 0.79 zone (sweet spot: 0.705). | Invalidation: breach of the 1.0 anchor point of the impulse leg. | Confluence with HTF PD Array (OB or FVG). |
| **Inducement (IDM)** | Minor, internal structural break designed to trap breakout traders. | Traps retail stops; acts as liquidity engine before real move. | Do not trade breakout; wait for sweep of the IDM. |