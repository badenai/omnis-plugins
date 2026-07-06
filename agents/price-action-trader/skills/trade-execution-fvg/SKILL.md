---
name: trade-execution-fvg
description: Use when executing trades based on Algorithmic Price Delivery, Fair Value Gaps (FVG), Inverse FVGs (IFVG), Balanced Price Ranges (BPR), and nesting strategies within HTF structures.
---

## The Iron Law

```
NEVER trade an FVG, IFVG, or BPR in isolation; you MUST validate execution through multi-timeframe alignment, ensuring the array nests within a Higher Timeframe (HTF) structure (Order Block, Breaker, or premium/discount boundary) and is swept during an active ICT Kill Zone.
```

## Behavioral Rules

*   **Rule of HTF Alignment:** If an FVG forms on a lower timeframe, you must only execute if it resides inside an unmitigated HTF (e.g., 1H, 4H, Daily) Order Block, Breaker Block, or at key premium/discount boundaries.
*   **Rule of Displacement:** You must verify that the displacement candle forming the FVG exhibits energetic body expansion. Reject any FVG formed by candles with a body-to-wick ratio of less than 60%.
*   **Rule of Balanced Price Ranges (BPR):** When executing on a BPR, you must prioritize entries where the displacement candle has a body-to-wick ratio exceeding 70% to ensure high-probability delivery (2.1R average target).
*   **Rule of Inverse FVGs (IFVG):** When a standard FVG fails to hold price, you must wait for a decisive candle body close past its boundary to validate the structural polarity flip before executing on the retest.
*   **Rule of the Unicorn Model:** You must execute the Unicorn setup only when an energetic, displacement-induced FVG overlaps horizontally and directly with an active ICT Breaker Block.
*   **Rule of the Reaper Inversion FVG:** You must place Reaper FVG limit orders exclusively in the discount portion of the impulsive leg for bullish setups, and in the premium portion of the leg for bearish setups, ensuring it lies within the leg executing the initial liquidity sweep and MSS.
*   **Rule of the Suspension Block:** If a candle's body is fully overlapped by the prior candle's wick to its left, preventing a standard FVG, you must use the body and its twin volume imbalances as a highly precise, low-drawdown support/resistance reload zone.
*   **Rule of Precision Entry (IOFED):** When executing via the Institutional Order Flow Entry Drill, you must place your limit order precisely at the proximal edge of the FVG, accepting higher potential drawdown in exchange for maximizing risk-to-reward.
*   **Rule of Consequent Encroachment:** If executing a conservative entry, you must place your entry limit order exactly at the 50% midpoint (Consequent Encroachment) of the FVG and set your stop-loss past the invalidation level of the first candle's wick.
*   **Rule of Execution Timing:** You must restrict all FVG, IFVG, and BPR execution entries to designated ICT Kill Zones: London Open (2:00 AM – 5:00 AM ET), New York Open / Silver Bullet (8:30 AM – 11:00 AM ET), or New York PM Session (1:30 PM – 4:00 PM ET).

## Red Flags

| Red Flag | Why it is Wrong |
| :--- | :--- |
| **Trading Low-Timeframe FVGs in Isolation** | Causes overtrading and high failure rates because the FVG lacks higher timeframe context and structural backing. |
| **Executing on Low-Displacement Candles** | Signals low institutional momentum; candles with body-to-wick ratios under 60% represent weak institutional interest and high probability of failure. |
| **Using Standard FVGs in Premium/Discount Mismatches** | Entering long in premium arrays or short in discount arrays ignores algorithmic pricing rules, leading to immediate drawdowns. |
| **Treating Wick Rejections as IFVGs** | A wick penetration through an FVG does not constitute a polarity flip; it requires a full candle body close to confirm institutional mitigation. |
| **Executing Outside of ICT Kill Zones** | Low-volume, off-session price action lacks the algorithmic delivery and liquidity required to sustain HTF target expansion. |

## Quick Reference

| Institutional Array | Validation Trigger | Entry Location | Stop-Loss Placement |
| :--- | :--- | :--- | :--- |
| **Standard FVG** | Body-to-wick ratio > 60% inside HTF Order Block | Proximal edge (IOFED) or 50% Consequent Encroachment | Beyond the wick of Candle 1 (origin) |
| **Inverse FVG (IFVG)** | Decisive candle body close past FVG boundary | Re-test of the flipped FVG boundary | Beyond the swing high/low of the breaking candle |
| **Balanced Price Range (BPR)** | Horizontally overlapping bullish and bearish FVGs with > 70% displacement | Retest of the overlapping boundary zone | Beyond the high/low of the displacement candle |
| **Unicorn Model** | FVG horizontally nested within a validated Breaker Block | Retest of the Breaker/FVG overlap zone | Beyond the invalidation level of the Breaker Block |
| **Reaper Inversion FVG** | Sweep + MSS leg; IFVG sits in premium (short) / discount (long) | Flipped boundary within the impulsive sweep leg | Past the high/low of the Breaker Block leg |
| **Suspension Block** | Candle body fully overlapped by prior wick; twin volume imbalances | Within the suspended candle body | Beyond the high/low of the prior candle's wick |