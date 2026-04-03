---
name: microstructure-order-flow-logic
description: Use when formalizing high-frequency limit order book (LOB) dynamics, Multi-Level Order Flow Imbalance (MLOFI) vectorization, flow toxicity metrics (VPIN, Kyle's Lambda), spatial-temporal density matrices, or integrating HftBacktest and GLFT models.
filePattern: "**/*.py"
bashPattern: "pytest"
---

## The Iron Law

```text
Never substitute explicit computational data structures with discretionary analysis, retail jargon, physics analogies, or superficial architectural buzzwords; you must translate all order flow and microstructure dynamics into strictly computable, zero-ambiguity N-dimensional arrays using explicit programmatic logic (e.g., exact array index inequalities, absolute price differentials, ATR thresholds, and boolean FSM gates) to ensure backtest-to-live parity.
```

## Behavioral Rules

*   Transform Limit Order Book (LOB) visual clustering strictly into N-dimensional spatial-temporal density matrices.
*   Compute Multi-Level Order Flow Imbalance (MLOFI) as a mathematical vector across defined LOB depths (e.g., L=5) utilizing precise array slicing rather than single-level static depth.
*   Integrate Volume-Synchronized Probability of Informed Trading (VPIN) and map Kyle's Lambda into deterministic arrays to explicitly calculate price impact per unit of volume before permitting execution.
*   Enforce HftBacktest framework parameters to mathematically simulate order feed latencies, probabilistic queue positioning, and Guéant–Lehalle–Fernandez-Tapia (GLFT) market-making models for exact backtest-to-live parity.
*   Dictate trade lifecycle execution via Finite State Machines (FSM) utilizing explicit boolean gates and array index state transitions for deterministic entry, scale-out, and invalidation.
*   Apply Average True Range (ATR) scalar arrays and exact standard deviation bounds to filter out noise; explicitly reject static percentage risk heuristics.
*   Gate system activation using binary Gamma Exposure (GEX) states and apply Volatility-of-Volatility (VoV) Z-Score thresholds as strict circuit breakers (e.g., unconditionally halt arrays if VoV Z > 1.5).
*   Structure time-series pipelines using Numba JIT-compiled functions for tick-level generation and QuestDB ASOF JOINs to guarantee asynchronous alignment without phase lag.
*   Map 60-second liquidation cascade zones computationally and validate true absorption over simple sweeps by mandating flat Open Interest (OI) divergence arrays.
*   Restrict all machine learning integrations strictly to interpretable linear algebra (e.g., PCA for MLOFI dimensionality reduction) or robust statistical fitting (e.g., Tick-Level RANSAC Regression); categorically reject black-box predictive models.

## Red Flags

| Rationalization / Anti-Pattern | Why Wrong |
| :--- | :--- |
| "We will use an LSTM to predict the LOB imbalance shift." | Generic black-box prediction violates deterministic transparency; restrict AI/ML entirely to interpretable linear algebra (e.g., PCA, RANSAC). |
| "The kinematic variance of the LOB slope dictates entry." | Physics-adjacent jargon contaminates programmatic vocabulary; dictate boundaries using exact array index inequalities and absolute price math. |
| "Set a Stop-Loss (SL) at 1% and Take-Profit (TP) at 3%." | Retail jargon and arbitrary percentage heuristics destroy dynamic risk sizing; encode invalidations using programmatic FSM state closures and ATR bounds. |
| "Create stateful object-oriented array layers to sanitize the tape." | Superficial algorithmic over-engineering obscures the actual math; use concrete mathematical array slicing and boolean operations. |
| "Confirm momentum with MACD crossovers or RSI exhaustion." | Lagging retail indicators are mathematically inferior; momentum must be derived exclusively from vectorized MLOFI, VoV, or direct tick footprint execution data. |

## Quick Reference

| Concept | Programmatic Implementation | Core Constraint |
| :--- | :--- | :--- |
| **MLOFI Mapping** | Numba-accelerated N-dimensional L=5 array vectorization | Must compute net flow across deep levels prior to price displacement |
| **Microstructure Toxicity** | VPIN arrays and Kyle's Lambda | Require explicit mathematical price impact per volume thresholds |
| **Execution Validation** | HftBacktest + GLFT Models | Must simulate network latency and queue position arrays |
| **System Gates** | GEX binary gate + VoV Z-score | Strict halt if VoV exceeds computed standard deviation limits |
| **Liquidation Avoidance** | Rolling 60-second Open Interest (OI) divergence | Require flat OI metrics to mathematically validate absorption |
| **Data Synchronization** | QuestDB ASOF JOINs + Numba JIT | Dictate deterministic temporal alignment and sub-millisecond footprint parsing |
| **Trade Lifecycle** | NautilusTrader Finite State Machine (FSM) | Absolute mathematical containment utilizing explicit boolean transitions |