---
name: trade-execution-imbalances
description: Use when validating mechanical Order Blocks (OB), trading Fair Value Gaps (FVG), executing the Unicorn Model, or defining exact entry triggers and stop placements in price action setups.
---

## The Iron Law

```text
Never execute a trade without observing violent institutional displacement that leaves behind a Fair Value Gap (FVG); if price action does not create a clear imbalance, the move lacks institutional sponsorship and the setup is invalid.
```

## Behavioral Rules

*   Execute entries exclusively within 15m, 5m, or 1m Premium/Discount arrays that strictly align with the Daily/4H narrative bias.
*   Validate an Order Block (OB) using three mechanical criteria: it must form within a liquidity-sweeping BOS/CHOCH leg, it must immediately precede aggressive displacement that leaves an FVG, and it must remain 100% unmitigated.
*   Discard any Order Block that has been previously wicked into; treat the first touch as the only valid institutional entry.
*   If a Fair Value Gap (FVG) directly overlays a Higher Timeframe OB or Breaker Block (Unicorn Model), execute mechanically upon return to this stacked zone without waiting for secondary lower-timeframe confirmations.
*   Place stop-loss orders rigidly beyond the original liquidity sweep wick to protect capital against algorithmic deep mitigations.
*   Target a minimum 1:2 or 1:3 Risk-to-Reward (RR) ratio on all mechanical executions.
*   Employ the Institutional Order Flow Entry Drill (IOFED) by placing limit orders at the proximal edge of an FVG only when higher-timeframe alignment is flawless.
*   Wait for price to retrace to the 50% Equilibrium (EQ) of the FVG if the algorithmic environment suggests a deeper mitigation is required before continuation.

## Red Flags

| Rationalization | Why it's a Trap |
| :--- | :--- |
| "This Order Block was already tested, but it looks strong." | Institutional orders are exhausted on the first touch; mitigated zones are high-risk. |
| "The candle is green, so it serves as a valid bullish OB." | An OB is entirely invalid unless it sweeps internal liquidity and directly causes FVG displacement. |
| "I will wait for a 1-minute CHOCH inside this Unicorn setup." | Unicorn setups represent high-conviction overlapping arrays; waiting for LTF confirmation causes missed entries. |
| "Price didn't leave an FVG, but the breakout looks aggressive." | No FVG means no proven institutional order imbalance; you are buying into a retail breakout trap. |
| "I'll trail my stop tightly inside the FVG to reduce risk." | Premature trailing ignores algorithmic repricing; stops must remain safely beyond the originating sweep wick. |

## Quick Reference

| Execution Concept | Validation Criteria | Mechanical Rule |
| :--- | :--- | :--- |
| **Mechanical OB** | Unmitigated, swept internal liquidity, caused FVG | Enter strictly on the first touch; invalidate if wicked. |
| **Unicorn Model** | FVG perfectly overlapping a HTF OB / Breaker | Execute immediately upon price return into the stacked zone. |
| **IOFED Entry** | Flawless HTF alignment, aggressive momentum | Enter at the proximal edge of the FVG. |
| **EQ Entry** | Standard FVG mitigation phase | Enter at the 50% Equilibrium of the FVG. |
| **Invalidation (Stop)** | Valid MSS and FVG creation identified | Place stop rigidly beyond the initiating liquidity sweep wick. |