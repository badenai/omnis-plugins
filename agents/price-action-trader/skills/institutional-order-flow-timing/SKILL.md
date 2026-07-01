---
name: institutional-order-flow-timing
description: Use when analyzing market structure, identifying session-specific liquidity sweeps, mapping the Daily Algorithmic Script (Accumulation, Manipulation, Distribution), or planning execution entries during the Asian, London, and New York Killzones.
---

## The Iron Law

```
NEVER execute trades outside of designated session Killzones (Asian, London, or New York), and NEVER execute long setups in Premium pricing or short setups in Discount pricing arrays.
```

## Behavioral Rules

*   **Map Asian Accumulation:** Map the Asian session (8 PM - 12 AM EST) highs and lows as resting buy-side (BSL) and sell-side (SSL) liquidity pools, and do not execute entries within this consolidation range.
*   **Identify London Manipulation:** Anticipate the Judas Swing during the London session (2 AM - 5 AM EST) to sweep the Asian range extremes. If a sweep occurs, wait for a wick rejection or micro-order flow footprint absorption to confirm the false expansion before executing.
*   **Trade New York Distribution:** Align execution setups during the New York AM session (7 AM - 12 PM EST) with the true directional expansion, targeting unmitigated high-timeframe zones in the opposite direction of the London manipulation phase.
*   **Manage London Close Reversals:** Tighten stop losses or take full profits during the London Close session (10 AM - 12 PM EST), treating this window strictly as a profit-taking or minor reversal phase.
*   **Enforce Premium vs. Discount:** Plot a Fibonacci retracement tool over the active dealing range before executing. Restrict buy setups strictly to the Discount zone (below the 50% equilibrium level) and sell setups strictly to the Premium zone (above the 50% equilibrium level).
*   **Validate the Unicorn Entry:** Only execute the Unicorn model when a valid Breaker Block (which successfully swept liquidity prior to the shift) horizontally overlaps with a Fair Value Gap (FVG) within the appropriate premium or discount zone.
*   **Execute the Venom Entry:** Utilize the Venom model only during active session Killzones, executing immediately upon the formation of a Balanced Price Range (BPR) following a major high-timeframe liquidity sweep.
*   **Filter Structural Shifts:** Distinguish between true Market Structure Shifts (MSS) and Inducement (IDM). Require a full candle body close past an external swing level to validate a structural shift; treat minor internal breaks as retail traps.
*   **Apply the Three-Mistake Circuit Breaker:** Immediately shut down all trading platforms and cease execution if you commit three process-oriented errors in a single day (e.g., executing out-of-session, widening stop losses, or over-leveraging).

## Red Flags

| Retail Rationalization | Why It Is Algorithmic Poison |
| :--- | :--- |
| "The Asian range breakout is strong; I will buy the continuation." | **The London session is designed to manipulate.** Breakouts of the Asian range are highly probable stop hunts engineered to trap retail liquidity before reversing. |
| "The setup is perfect, so it does not matter that the New York session closed." | **Volume and liquidity are session-dependent.** Trading outside designated Killzones exposes orders to low-volume algorithmic drift and wide spreads. |
| "I am buying this Fair Value Gap in Premium because the momentum is high." | **Institutional pricing rules are absolute.** Buying in Premium or selling in Discount drastically reduces your probability of success and increases drawdown risk. |
| "Price broke the minor internal high, so the trend has officially reversed." | **This is structure inducement.** Internal breaks are engineered to trap breakout traders. True shifts require external swing high/low candle body validation. |

## Quick Reference

| Session / Killzone | Time (EST) | Algorithmic Phase | Core Tactical Execution Objective |
| :--- | :--- | :--- | :--- |
| **Asian Session** | 8:00 PM - 12:00 AM | Accumulation | Map BSL/SSL pools above and below the range; do not execute. |
| **London Open** | 2:00 AM - 5:00 AM | Manipulation (Judas Swing) | Look for sweeps of Asian range extremes; watch for rejection signals. |
| **New York AM** | 7:00 AM - 12:00 PM | Distribution | Trade the major expansion in alignment with HTF targets and order flow. |
| **London Close** | 10:00 AM - 12:00 PM | Reversal / Profit-Taking | Manage active positions, trail stops tightly, and do not open new setups. |