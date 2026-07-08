---
name: institutional-order-flow-timing
description: Use when analyzing institutional order flow, tracking algorithmic execution timing windows, executing structural setups (Unicorn, Inverse FVGs, Breakers), or evaluating Power of Three (AMD) delivery cycles.
---

## The Iron Law

```
Never execute a trade outside of the designated institutional timing windows (London Open, New York Open/Silver Bullet, or New York PM Killzones), and never validate structural shifts (MSS/CHoCH) based on candlestick wicks alone; structural shifts require a decisive candle body close past external swing levels.
```

## Behavioral Rules

*   **Enforce the Timing Hierarchy:** You must only seek trade entries during valid session killzones (London Open: 2:00 AM – 5:00 AM ET; NY Open/Silver Bullet: 8:30 AM – 11:00 AM ET; NY PM Session: 1:30 PM – 4:00 PM ET). If the current chart time falls outside these specific windows, you must advise the trader to sit on their hands.
*   **Verify Structural Shifts with Body Closes:** You must require a definitive candle body close past a major external swing high or low to confirm a Market Structure Shift (MSS) or Change of Character (CHoCH). Treat any wick-only breaks strictly as liquidity sweeps (stop hunts) and never as structural trend shifts.
*   **Validate the Power of Three (AMD) Sequence:** When analyzing intraday cycles, you must identify Asian range consolidation as Accumulation, look for London open expansions below/above the Asian range as Manipulation (Judas Swing), and wait for New York to deliver the true directional trend reversal as Distribution.
*   **Filter FVGs and BPRs by Candle Quality:** You must only recommend entry execution on Fair Value Gaps (FVG) or Balanced Price Ranges (BPR) if the underlying displacement candle has a body-to-wick ratio above 70%. You must reject low-momentum candles with massive wicks as invalid structural imbalances.
*   **Confirm Breaker Blocks with Liquidity Sweeps:** You must only classify a failed order block as a Breaker Block if price successfully swept a key liquidity extreme prior to delivering the violent, imbalance-leaving Market Structure Shift. If no sweep occurred, classify the level as a weaker Mitigation Block.
*   **Apply the Inverse FVG (IFVG) Polarity Shift:** When price closes decisively beyond a bullish FVG, you must immediately flip that zone into a bearish resistance level (IFVG) on any subsequent retest, rather than discarding the zone as invalidated.
*   **Cross-Reference with Consequent Encroachment:** You must identify and map the 50% midpoint (Consequent Encroachment) of every active HTF FVG as the ultimate algorithmic magnet and key structural support/resistance level.
*   **Apply the Three-Mistake Rule:** You must advise immediate platform shutdown if the trader commits three process violations (such as trading outside killzones, widening stops, or over-leveraging) within a single trading day.

## Red Flags

| Red Flag / Retail Trap | Why It Is Wrong | Institutional Price Action Correction |
| :--- | :--- | :--- |
| **Executing setups during lunch hour / dead zones** | Volatility and institutional order flow drop off, leading to directionless chop and retail stop hunts. | Restrict trade execution strictly to London, NY Open, and NY PM Killzones. |
| **Treating wick-only breaks as structural trend shifts** | Wicks indicate liquidity sweeps and immediate rejection, not sustainable market expansion. | Require a full candle body close on the execution timeframe to confirm MSS/CHoCH. |
| **Buying unmitigated order blocks without HTF alignment** | Low-timeframe order blocks are easily ran over if they align against the HTF order flow. | Only trade LTF order blocks that are nested directly within or adjacent to HTF PD arrays. |
| **Discarding violated FVGs as useless** | Algorithms defend failed levels; a breached FVG becomes a highly sensitive support/resistance zone. | Flip the breached zone into an Inverse FVG (IFVG) and monitor for polarity-shift retests. |
| **Trading "reversal patterns" (wedges, double bottoms) in isolation** | Geometric patterns are retail traps designed to build up dense liquidity pools above and below key levels. | Wait for the retail patterns to get swept, then execute in the opposite direction off an OB or FVG. |

## Quick Reference

| Institutional Setup | Key Structural Criteria | Primary Target | Invalidation Condition |
| :--- | :--- | :--- | :--- |
| **ICT Unicorn Model** | Direct horizontal overlap of a Breaker Block (BB) and a Fair Value Gap (FVG) following a liquidity sweep. | Opposing external liquidity pool (BSL/SSL). | Candle body close beyond the outer anchor point of the initial sweep wick. |
| **Inverse FVG (IFVG)** | Decisive candle body close past a pre-existing FVG zone, flipping its polarity. | Next unmitigated structural key level. | Retest body close back inside the original invalidation zone. |
| **Breaker Block** | Failed order block formed *after* a successful liquidity sweep and a violent displacement-driven MSS. | First unmitigated FVG or structural liquidity pool. | Candle body close past the origin of the displacement leg. |
| **Mitigation Block** | Failed order block formed by a failure swing (failed to sweep the previous structural extreme before reversing). | Near-term internal liquidity pools (lower probability). | Candle body close past the failure swing extreme. |
| **Balanced Price Range (BPR)** | Direct horizontal overlap of a bullish FVG and a bearish FVG, signaling immediate price equilibrium. | High-volume expansion targets. | Candle body close back inside the opposing extreme of the BPR. |