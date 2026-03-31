---
name: structural-formalization
description: Use when translating subjective price action, market structure, liquidity sweeps, or chart patterns into deterministic programming logic, exact array computations, and boolean conditions.
---

## The Iron Law

```text
You must translate every subjective price action concept into strictly computable definitions using explicit array index inequalities, absolute price differentials, Order Flow Imbalance (OFI) processing, and ATR-qualified boolean gates, completely eliminating all visual chart interpretation and retail heuristics.
```

## Behavioral Rules

*   **Displacement Qualification:** Qualify Market Structure Shifts (MSS) programmatically by demanding the absolute difference between close and open exceeds an Average True Range multiplier threshold (`abs(Close[i] - Open[i]) > ATR(10) * BodyMultiplier`).
*   **Order Block Mitigation:** Construct order blocks as rigid boolean mitigation states bounded by exact price arrays, invalidating the active state only upon a terminal candle close beyond the defined array boundary constraint.
*   **Gap Validation:** Define Fair Value Gaps (FVG) and structural imbalances using absolute price differentials and linear regression slopes applied to high-frequency tick arrays, stripping out high-velocity exhaustion gaps unless explicitly validated by multi-level OFI computations.
*   **Order Flow Imbalance:** Process market microstructure strictly through Numba-accelerated arrays computing Order Flow Imbalance (OFI) across specific Limit Order Book depths (e.g., Depth 5-10) to map institutional displacement.
*   **Volume-Validated Breakouts:** Validate expanding price vectors programmatically by calculating Price-Volume Interaction metrics, strictly comparing current volume against a Simple Moving Average (SMA) baseline array.
*   **Position Sizing & Risk:** Enforce position sizing and risk management natively through computable R-multiple breakeven state definitions and deterministic scale-out arrays rather than static retail percentage heuristics.
*   **State Management:** Govern trade lifecycles using closed-loop Finite State Machines (FSM) linked directly to array-driven signal thresholds to prevent deadlock during partial fills or missing exchange data.
*   **Liquidity Profiling:** Programmatically distinguish resting liquidity from spoofing by calculating cancellation velocity and queue positioning over rolling time windows via array iteration, never relying on visual depth density.

## Red Flags

| Domain-Specific Rationalization | Why It Violates Structural Formalization |
| :--- | :--- |
| "Use an N-bar swing logic to detect the pivot points and market structure breaks." | Replaces robust Order Flow Imbalance (OFI) and standard deviation displacement metrics with lagging retail logic. |
| "Set the SL to the swing low and the TP at a fixed 1.5% profit." | Employs banned retail acronyms (SL/TP) and arbitrary percentage heuristics instead of dynamic R-multiple states and scale-out arrays. |
| "The kinematic variance of the RANSAC flat slope mathematically confirms the void." | Contaminates execution code with physics buzzwords instead of relying on explicit array indexing and clear boolean logic. |
| "Trigger a stateful object-oriented sanitization protocol for the LOB arrays." | Uses superficial programming jargon rather than detailing the precise mathematical operations required for multi-level depth processing. |
| "Check if the absolute value is $\ge$ the threshold to enter the state." | Utilizes LaTeX math formatting which abstracts away exact, copy-pasteable code-level directives like `>=`. |
| "Deploy a Finite State Machine to calculate the position size." | Shoehorns complex execution architecture into simple arithmetic calculations, diluting both the FSM's purpose and the math. |

## Quick Reference

| Concept | Computable Implementation | Execution Logic |
| :--- | :--- | :--- |
| **Displacement** | `abs(Close - Open) > ATR(10) * BodyMultiplier` | Trigger boolean state inversion |
| **Order Blocks** | Strict boundary array assignment (High/Low) | Terminal close invalidation gate |
| **Momentum** | Depth 5-10 MLOFI / Volume-Price Interaction | Standard deviation threshold breach |
| **Gap (FVG) Retest** | Absolute price differential + Slope threshold (`abs(slope) <= max_val`) | Asynchronous array intersection |
| **Risk Encoding** | Base risk amount * R-multiple scale-out tiers | FSM rollback on limit violation |
| **Baseline Filtering** | Zero-Phase Filter bidirectional arrays | Cross-track error computation |