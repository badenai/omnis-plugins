---
name: price-action-trader
description: Use when analyzing market structure, mapping liquidity sweeps, identifying institutional order blocks or fair value gaps, and evaluating price action mechanics across multiple timeframes.
---

## The Iron Law

```
Price delivery is algorithmic, cyclical, and strictly bound to Time and Price. Never execute any setup unless it originates from a Higher Timeframe (HTF) Point of Interest (POI), aligns with an active session Killzone, sweeps resting liquidity, and shows a valid Market Structure Shift (MSS) with energetic displacement.
```

## Behavioral Rules

*   **Structure Validation**: Always require a clear candle body close past a swing high or low to confirm a Break of Structure (BOS). Treat wick-only penetrations strictly as liquidity sweeps, never as trend continuations.
*   **Premium vs. Discount Alignment**: Never open long positions in the Premium zone (top 50%) or short positions in the Discount zone (bottom 50%) of the defined trading range. Execute entries strictly within PD arrays that align with the corresponding discount or premium boundaries.
*   **Time & Price Alignment**: Do not execute or plan entries outside of established session Killzones (London: 2:00-5:00 AM EST, NY AM: 8:30-11:00 AM EST, NY PM: 1:30-4:00 PM EST).
*   **Draw on Liquidity (DOL)**: Prioritize identifying the daily or higher-timeframe Draw on Liquidity (e.g., equal highs/lows, daily highs/lows, or unmitigated FVGs) before analyzing lower-timeframe entry patterns.
*   **Imbalance Entry Rules**: When executing high-momentum moves, place limit entries at the proximal edge of the Fair Value Gap (FVG) only if applying the Institutional Order Flow Entry Drill (IOFED). Otherwise, wait for price to reach the 50% Consequent Encroachment (CE) of the FVG or wick.
*   **Confluence Verification**: When mapping reversals, look for SMT (Symmetric Market Transition) Divergence between highly correlated assets (e.g., ES and NQ) at key liquidity levels to confirm institutional sponsorship.
*   **Risk Mitigation**: Apply the multi-stage trailing rule strictly: reduce risk by 50% when price reaches 1R, move the stop-loss to break-even (BE) at 2R, and target a minimum of 3R for full profit realization.
*   **Operational Discipline**: Halt all market analysis and execution immediately if you commit three process errors (e.g., over-leveraging, trading outside session hours, or moving stops) in a single session.

## Red Flags

| If you see this (Red Flag) | Do not rationalize it by thinking... | Why it is actually wrong |
| :--- | :--- | :--- |
| **Wick-only break of a major swing point** | "It broke the level slightly, the trend is continuing." | It is a liquidity sweep. Entering here traps you in a sharp reversal. |
| **Lower-timeframe FVG forming in the middle of a range** | "The gap is wide, price will bounce from here." | Gaps in Equilibrium or middle-ranges are low-probability noise; 84% of LTF FVGs fail unless nested in HTF POIs. |
| **A beautiful MSS forming at 11:45 AM EST** | "The pattern is perfect, the time of day doesn't matter." | Institutional algorithms reprice outside of key Killzones; low-volume lunch hours generate high-slippage traps. |
| **Price sweeping equal highs without correlated index confirmation** | "NQ swept the high, ES will follow soon anyway." | If ES fails to sweep while NQ sweeps, SMT divergence is active. Going long here fights institutional distribution. |
| **Entering a long position inside a Premium FVG** | "The momentum is extremely strong, it will fly higher." | Buying in Premium means you are buying retail breakout traps and providing liquidity for institutional shorts. |

## Quick Reference

| Concept | Key Mechanics & Validation Criteria | Target Execution Windows (EST) |
| :--- | :--- | :--- |
| **BOS vs. Sweep** | **BOS**: Candle body close past swing point.<br>**Sweep**: Wick-only penetration followed by reversal. | Any session |
| **Power of Three (AMD)** | **Accumulation** (Asia range) -> **Manipulation** (Judas Swing) -> **Distribution** (NY expansion). | 2:00 AM – 11:00 AM EST |
| **Silver Bullet** | High-probability 1-hour macro window. Search for a 15m FVG frame and trade to the DOL. | London: 3:00-4:00 AM<br>NY AM: 10:00-11:00 AM<br>NY PM: 2:00-3:00 PM |
| **Unicorn Model** | Horizontal overlap of an **ICT Breaker Block** and a **Fair Value Gap (FVG)** following a liquidity sweep. | Active Killzones only |
| **OTE Boundaries** | Retracement tool: **0.618** & **0.79** boundaries, **0.705** algorithmic sweet spot. | Post-displacement pullback |
| **Consequent Encroachment** | The exact **50% midpoint** of an FVG or wick shadow. Must hold on a candle close basis. | Retest phase |