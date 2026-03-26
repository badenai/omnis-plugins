---
name: execution-architecture-fsm
description: Use when designing or debugging high-frequency execution architectures, Finite State Machines (FSM) for trade lifecycles, Numba-compiled tick data processing, or event-driven execution logic.
filePattern: "**/*.py"
---

## The Iron Law

```text
Construct every Finite State Machine (FSM) execution loop utilizing explicit array index inequalities, absolute price differentials, ATR volatility thresholds, and Boolean gates to dictate strictly closed state transitions. Never decouple structural signal generation logic from event-driven execution frameworks, and never substitute concrete programmatic execution arrays with uncomputable ML buzzwords, physics-adjacent jargon, or retail trading heuristics.
```

## Behavioral Rules

*   Compile raw tick data directly into Imbalance/Run bars and Chu-Stinchcombe-White CUSUM structural breaks using Numba JIT kernels to bypass standard Python latency.
*   Implement Finite State Machines (FSM) for all trade lifecycles, ensuring mathematically closed states and error-aware rollbacks to prevent deadlock during asynchronous API drops.
*   Govern signal activation using strict mathematical boolean gates derived from simultaneous N-period rolling min/max array breaches and structural memory bounds.
*   Compute Order Flow Imbalance (OFI) strictly at Depth 5 (L=5) of the order book as a probabilistic scalar, ignoring Top-of-Book (L=1) spoofing noise.
*   Enforce a programmatic minimum 1:3 risk-to-reward ratio mathematically using absolute price differentials before allowing an FSM to transition into an entry state.
*   Regulate intrabar execution tempo using a Binary-Temporal Representation (BTR) to model relative duration bits, entirely avoiding absolute time threshold calculations.
*   Halt execution programmatically if operational asset Correlation Elasticity breaches predefined arrays or if Vol-of-Vol (VoV) Z-Score exceeds a +1.5 standard deviation bound.
*   Calculate dynamic parameter thresholds explicitly utilizing Walk-Forward Analysis (WFA) loops to enforce continuous out-of-sample validation.
*   Scale structural containment boundary arrays dynamically utilizing specific ATR multipliers to define precise mathematical invalidation thresholds.

## Red Flags

| Rationalization | Why Wrong |
| :--- | :--- |
| "Implement a dynamic Stop-Loss (SL) and Take-Profit (TP) for the state." | Replaces deterministic FSM state transitions, ATR volatility thresholds, and R-multiple breakeven array logic with brittle retail terminology. |
| "Cap risk exposure at 1.0% to maintain a safe margin." | Replaces programmatic position sizing and strict mathematical R:R matrices with hardcoded, arbitrary retail heuristics. |
| "Wait for kinematic validation of the trend before transitioning states." | Contaminates the model with physics-adjacent jargon, abandoning required array index inequalities and boolean gates. |
| "Wrap the ticks in a stateful object-oriented array sanitization protocol." | Replaces precise mathematical operations, subscript notations, and Numba JIT arrays with superficial programming filler. |
| "Use ML-classified confidence or RANSAC flat slopes to determine the exit." | Replaces unambiguous mathematical boundaries and absolute price differentials with overly complex, uncomputable ML buzzwords. |

## Quick Reference

| Component | Implementation Constraint |
| :--- | :--- |
| **Tick Processing** | Execute via Numba JIT kernels to construct deterministic Imbalance/Run arrays and CUSUM breakpoints. |
| **State Lifecycle** | Build strictly closed Finite State Machines (FSM) utilizing event-driven engines with asynchronous API drop rollbacks. |
| **Microstructure** | Compute Order Flow Imbalance (OFI) scalar arrays exclusively at Depth 5 (L=5), discarding L=1 data. |
| **Intrabar Tempo** | Regulate relative execution duration via Binary-Temporal Representation (BTR) tempo bits. |
| **Risk Architecture** | Enforce a 1:3 R:R expectancy matrix programmatically using absolute price differentials prior to FSM trigger. |
| **Structural Logic** | Trigger state execution only when boolean gates confirm simultaneous N-period rolling min/max array breaches. |