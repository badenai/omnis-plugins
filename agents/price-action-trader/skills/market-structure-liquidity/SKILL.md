---
name: market-structure-liquidity
description: Use when analyzing market structure, identifying swing points (BOS, CHoCH, MSS), mapping internal vs. external liquidity, evaluating liquidity sweeps, or locating institutional footprints like Order Blocks, Breakers, and Fair Value Gaps.
---

## The Iron Law

```
All structural assessments must begin with a top-down HTF sweep-to-MSS alignment; do not execute on LTF structures unless an HTF liquidity sweep or key HTF PD array mitigation has occurred first.
```

## Behavioral Rules

*   **Rule on Structural Breaks:** Classify a structural break as a valid Break of Structure (BOS) or Change of Character (CHoCH/MSS) only if the candlestick body closes decisively past the external swing point. If only the wick pierces the level, classify it strictly as a liquidity sweep (stop hunt).
*   **Rule on Inducement vs. Shift:** Treat minor internal breaks within a swing range as Inducement (IDM) designed to trap retail breakout traders. Do not label internal structural breaks as a true CHoCH/MSS.
*   **Rule on Execution Timing:** Restrict trade setups and execution entries strictly to established algorithmic Killzones (London Open: 2:00 AM – 5:00 AM ET; New York Open/Silver Bullet: 8:30 AM – 11:00 AM ET; New York PM Session: 1:30 PM – 4:00 PM ET). Do not execute trades outside these daily macro time windows.
*   **Rule on FVG Validation:** Evaluate Fair Value Gaps (FVGs) using the body-to-wick ratio of the displacement candle. Discard any FVG or Balanced Price Range (BPR) setup if the displacement candle's body-to-wick ratio is under 70%.
*   **Rule on Reversal Entries (The Unicorn Model):** Validate the ICT Unicorn entry model only when there is a direct horizontal overlap of a Breaker Block (BB) and a Fair Value Gap (FVG) created by the same displacement leg following a liquidity sweep. Invalidate the setup immediately if a candle body closes beyond the outer anchor point of the initial sweep wick.
*   **Rule on Polarity Flipping (Inverse FVGs):** If price closes decisively beyond a bullish FVG, immediately flip the zone into a bearish Inverse FVG (IFVG) to act as resistance on subsequent retests, and vice versa.
*   **Rule on Structural Failure (Mitigation vs. Breaker):** Map a failed order block as a Breaker Block only if price swept a key liquidity extreme before breaking the block. If price failed to sweep the extreme before breaking the block (failure swing), map it as a Mitigation Block and enforce tighter risk filters.
*   **Rule on Risk Management and Errors:** Enforce the Three-Mistake Rule. Shut down the trading platform immediately if you commit three process errors (e.g., trading outside killzones, widening stops, or over-leveraging) before financial daily loss limits are hit.

## Red Flags

| Red Flag | Rationalization | Why Wrong |
| :--- | :--- | :--- |
| **Wick-only structural break** | "Price broke the level with a wick, confirming a trend continuation/reversal." | **No body close means no structural break.** Wicks represent price rejection and liquidity sweeps, not structural acceptance. |
| **Trading minor internal breaks** | "The 5m chart broke the nearest internal high, signaling a trend change." | **Inducement trap.** Internal breaks are retail inducement. True trend shifts require HTF external swing point body closes. |
| **Executing mid-day or off-hours** | "The setup looks perfect at 12:30 PM ET; I must enter now before it moves." | **Low probability manipulation.** Algorithmic order flow and institutional participation occur inside strict Killzones; mid-day price action is random, low-volume noise. |
| **Ignoring displacement quality** | "An FVG formed, so I am entering on the retest, even though the candle was mostly wicks." | **Low probability imbalance.** Candles with body-to-wick ratios under 70% represent exhaustion, not aggressive institutional displacement, drastically lowering setup win rates. |
| **Discretionary stop adjustments** | "I will widen my stop loss slightly below this next level to avoid getting wicked out." | **Emotional capital destruction.** Widening stops violates fixed-risk parameters and invalidates the trade's initial probabilistic edge. |

## Quick Reference

| Concept | Identifier | Core Rule / Validation |
| :--- | :--- | :--- |
| **BOS** | Break of Structure | Trend continuation; requires a decisive candle **body close** past a prior swing high/low. |
| **CHoCH / MSS** | Change of Character / Market Structure Shift | Trend reversal; requires a decisive candle **body close** past an external swing point. |
| **Liquidity Sweep** | Stop Hunt | Wick-only penetration of session highs/lows, equal highs (EQH), or equal lows (EQL) followed by rejection. |
| **Unicorn Model** | Premium Entry | Horizontal overlap of a **Breaker Block** and an **FVG** following a session liquidity sweep. |
| **Inverse FVG (IFVG)** | Polarity Flip | A failed FVG that has been closed past by a candle body; acts as support/resistance on retest. |
| **Consequent Encroachment (CE)** | 50% Midpoint | The exact midpoint of a Fair Value Gap; acts as a highly sensitive algorithmic magnetic level. |
| **BPR Quality Filter** | Balanced Price Range | Overlapping bullish/bearish FVGs; only valid if displacement candle has a **>70% body-to-wick ratio**. |