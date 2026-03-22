---
name: volume-microstructure-logic
description: Use when generating code for volumetric validation, Z-Scored Volume Profiles, Open Interest divergence, POC migration, institutional displacement proxies, and deterministic liquidation cascades.
---

## The Iron Law

```text
Never execute a structural break or trend initiation without programmatic volume validation; if Relative Volume (RVOL) or Z-scored volume arrays do not explicitly meet predetermined numerical thresholds, flag the price movement as exhaustion noise and halt execution.
```

## Behavioral Rules

*   Compute institutional displacement via strict mathematical proxies, requiring Relative Volume (RVOL) > 1.5x on structural break bars before generating an entry signal.
*   Validate uptrend continuations by enforcing a Point of Control (POC) migration counter that must equal or exceed 3 consecutive positive period shifts concurrent with calculated Value Area (VA) expansion.
*   Calculate Volume Z-scores during price expansion arrays to detect divergence computationally.
*   Emit an automated structural exhaustion short signal if price array logic registers a higher high while High Volume Node (HVN) calculations contract and the Volume Z-score exceeds 2.0.
*   Map Open Interest (OI) Delta arrays against price vectors to yield a continuous mathematical divergence score.
*   Generate explicit limit-order exit nodes (liquidation flush targets) when high OI divergence aligns with boolean flips in extreme funding rate data.
*   Filter out Opening Range Breakouts (ORBs) immediately unless validated by session-aware volume de-noising filters.
*   Demand 0.0 spread execution environments (e.g., tick-level bid/ask arrays) when deploying microstructure liquidation mapping systems to prevent slippage contamination.
*   Use standard array index inequalities, N-bar lookback windows, and boolean gates to build logic; never substitute simple algorithmic operations with ML/math buzzwords.
*   Use explicit code-level directives (`>`, `<`, `>=`, `==`) for all constraints; strictly avoid LaTeX formatting or textual math representations.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "Check for a kinematic volume validation event." | Violates anti-patterns by using banned physics terminology instead of standard array indexing and boolean logic. |
| "The volume looks heavy enough to support the breakout." | Relies on subjective, non-computable intuition instead of a strict RVOL > 1.5x threshold. |
| "Initiate stateful object-oriented volume array sanitization." | Introduces superficial architectural buzzwords and fluff instead of writing direct matrix or array calculations. |
| "Trigger a Boolean state inversion when POC decays." | Uses artificial persona phrasing instead of defining explicit variable assignments and numeric thresholds. |
| "Long FVG formation detected, enter trade." | Fails to incorporate the mandatory volatility-scaled volume checks and flat slope requirements for structural zones. |

## Quick Reference

| Microstructure Concept | Deterministic Formalization Rule |
| :--- | :--- |
| **Institutional Displacement** | Breakout Bar RVOL > 1.5x |
| **POC Uptrend Validation** | POC positive shift count >= 3 AND Value Area expands |
| **Volume Exhaustion (Short)** | Price HH == True AND HVN contracts AND Volume Z-Score > 2.0 |
| **Liquidation Cascade Exits** | OI Delta divergence == True AND Funding Rate Extreme == True |
| **Price-Volume Proxy** | `Daily Return * (Current Volume / 50-day SMA Volume)` |
| **Internal Bar Position** | `(Close - Open) / (High - Low)` |