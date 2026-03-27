---
name: quantitative-regime-filtering
description: Use when determining algorithm activation states, toggling execution logic between mean-reverting and trend-following environments, mapping Gamma Exposure (GEX) thresholds, calculating Vol-of-Vol (VoV) Z-Scores for circuit breakers, or implementing Zero-Phase Filter (ZPF) baseline tracking.
filePattern: "**/*.py"
---

## The Iron Law
```text
Always govern trade lifecycle Finite State Machines (FSM) through computable array matrices; require strict Boolean gates derived from Gamma Exposure (GEX) polarity and Volatility-of-Volatility (VoV) standard deviation bounds to deterministically route execution logic before any signal sequence initiates.
```

## Behavioral Rules

*   Route execution logic strictly to mean-reversion arrays and range-midpoint targeting formulas if Gamma Exposure is positive (`GEX > 0`), initializing a "STICKY" FSM state.
*   Route execution logic strictly to breakout and trend-following N-bar arrays if Gamma Exposure is negative (`GEX < 0`), initializing a "SLIPPERY" FSM state.
*   Halt all algorithmic entry signals and trigger closed-state rollback logic if the Vol-of-Vol (VoV) Z-Score exceeds a +1.5σ threshold (`vov_zscore > 1.5`).
*   Compute structural baseline states using Zero-Phase Filters (ZPF) running bidirectionally across time-series arrays to eliminate phase lag and supply synchronized, zero-distortion Boolean inputs.
*   Dictate position sizing and risk constraints exclusively via ATR volatility thresholds and strict R-multiple breakeven state definitions, never utilizing arbitrary fixed percentage heuristics.
*   Formulate Time-Series Momentum (TSMOM) inputs into rigid programmatic thresholds backed strictly by continuous out-of-sample walk-forward validation arrays.
*   Validate all structural baseline shifts by verifying Relative Volume (RVOL) exceeds 1.5x at the precise array index breakpoint.

## Red Flags

| Domain-Specific Rationalizations | Why Wrong |
| :--- | :--- |
| "Use RSI > 70 to detect the overbought regime." | Relies on lagging retail indicators instead of Order Flow Imbalance (OFI), VoV Z-Scoring, or empirical GEX metrics. |
| "Set the SL to 1% for trend regimes and TP to 2% for range regimes." | Uses brittle retail jargon (SL/TP) and arbitrary heuristics instead of explicit ATR volatility threshold bounds and programmatic R-multiple state transitions. |
| "The regime changed because of a kinematic variance event detected by the RANSAC ML slope." | Contaminates code with irrelevant physics jargon and over-engineered ML buzzwords instead of relying on explicit array index inequalities and Boolean gates. |
| "Trigger a structural decay phase change in the object-oriented state manager." | Replaces precise mathematical operations and N-bar array tracking with superficial object-oriented programming buzzwords. |
| "Execute the trade if the regime feels choppy or sentiment implies reversion." | Injects non-formalized, subjective human judgment and non-deterministic text inputs into an environment requiring zero ambiguity. |

## Quick Reference

| Regime Trigger / Condition | Programmatic Logic & Output State |
| :--- | :--- |
| **Positive GEX** (`GEX > 0`) | **STICKY State FSM**: Activate mean-reversion array matrices and compute range-midpoint retest logic. |
| **Negative GEX** (`GEX < 0`) | **SLIPPERY State FSM**: Activate breakout array matrices, trend-following logic, and trailing ATR stop limits. |
| **VoV Z-Score** (`vov_z > 1.5`) | **Circuit Breaker Gate**: Force True; halt all new execution states and lock current capital exposure. |
| **Relative Vol** (`RVOL > 1.5x`) | **Baseline Shift Gate**: Force True; validate structural breaks at the current array index breakpoint. |
| **Structural Baseline Sync** | **ZPF Computation**: Execute Zero-Phase Filter bidirectionally across N-bar windows to output zero-lag logic states. |