---
name: execution-architecture-fsm
description: Use when designing, debugging, or deploying high-frequency execution pipelines, event-driven trade lifecycle finite state machines (FSM), HftBacktest/NautilusTrader integrations, or handling tick-data streams and Numba-accelerated microstructure arrays.
filePattern: "**/*.py"
bashPattern: "pytest|nautilus"
---

## The Iron Law

```text
Every execution state and trade lifecycle must be governed by a mathematically closed, event-driven Finite State Machine (FSM) that guarantees absolute deterministic parity between HftBacktest tick-level simulations and NautilusTrader live environments. Execution logic must rely exclusively on computable array index inequalities, strict Boolean gates, Order Flow Imbalance (OFI) thresholds, and precise absolute price differentials. You shall never utilize retail trading simplifications, discretionary logic, generic OOP abstractions, or black-box predictive models to govern market state transitions.
```

## Behavioral Rules

*   Construct trade lifecycles strictly as Finite State Machines (FSM) utilizing `NautilusTrader`, enforcing explicit event-driven transitions, absolute state closures, and mathematically verifiable error-aware rollbacks.
*   Guarantee absolute Backtest-to-Live Parity by validating execution logic natively inside `HftBacktest` Level-2 and Level-3 order book simulations, accounting deterministically for network latency, queue position, and partial fills.
*   Define system activation and validation states explicitly via standard deviation bounds, Vol-of-Vol (VoV) Z-Scores, and Order Flow Imbalance arrays rather than generic technical crossover mechanics.
*   Enforce fixed position sizing and programmatic trade invalidation using strictly computable array index inequalities, absolute price differentials, and dynamically updating ATR volatility bounds instead of generic percentage-based limits.
*   Synchronize asynchronous tick-trades and multi-depth LOB snapshots utilizing `QuestDB` 2D Multi-Dimensional Arrays natively executing `ASOF JOIN` logic to eliminate sampling gaps and lookahead bias.
*   Accelerate all microstructural mathematical calculations—including Multi-Level Order-Flow Imbalance (MLOFI) processing and Chu-Stinchcombe-White CUSUM statistical tests—strictly via `Numba` JIT-compiled functions within the `finmlkit` framework.
*   Govern execution pacing via the Adaptive State Model in Binary-Temporal Representation (ASMBTR) framework to process relative tick velocity shifts, replacing arbitrary fixed-time limits with deterministic tick-event tempo encoding.
*   Compute cross-track validation natively within arrays using strict Boolean gates to process aggregated consensus signals, mathematically penalizing redundant order flow features via defined correlation suppression constraints.
*   Design every algorithmic component to output its own intrinsic failure mode parameter, mandating strict walk-forward validation schemas to benchmark out-of-sample systemic degradation continuously.

## Red Flags

| Rationalization / Anti-Pattern | Why it is Wrong (Execution Architecture Domain) |
| :--- | :--- |
| "Implementing Stop-Loss (SL) and Take-Profit (TP) parameters at 1% logic bounds." | Contaminates code with retail trading jargon; abandons exact programmatic R-multiple state definitions, ATR thresholds, and event-driven FSM scale-out logic. |
| "Replacing finite state structures with generic object-oriented flag updates." | Fails to close loops programmatically; introduces severe risk of execution state drift, ambiguous transitions, and orphaned limit orders during live exchange routing. |
| "Using kinematic variance or momentum acceleration terminology to describe fills." | Vocabulary contamination; introduces irrelevant physical science jargon that obfuscates the explicit time-series math, array indexing, and order book reconstruction requirements. |
| "Replacing LOB Order Flow Imbalance arrays with N-bar swing indicator logic." | Strips out critical microstructure dimensions; downgrades institutional standard deviation displacement detection into lagging, retail-level geometry abstraction. |
| "Synchronizing tick data streams using standard DataFrame merge algorithms." | Guaranteed to introduce lookahead bias and significant computational latency; deterministic ultra-high-frequency modeling mandates strict time-aware `ASOF JOIN` synchronization. |

## Quick Reference

| Component | Deterministic Implementation Standard |
| :--- | :--- |
| **Execution Framework** | Strict event-driven Finite State Machines (FSM) utilizing `NautilusTrader` for trade lifecycles. |
| **Simulation Parity** | `HftBacktest` arrays simulating Level-2/Level-3 queue execution latency with mathematical exactness. |
| **Pipelining / Storage** | `QuestDB` for 8M+ rows/s ingestion utilizing `SAMPLE BY ... FILL(PREV)` and `ASOF JOIN` for tick alignment. |
| **Computational Velocity** | `finmlkit` and `Numba` JIT compilation for real-time Order Flow Imbalance (OFI) processing and structural math. |
| **Programmatic Risk** | Absolute price differentials, computable array index inequalities, and dynamically scaled ATR logic. |
| **State Triggers** | Strict Boolean gates governed by Volume-of-Volume Z-scoring and multi-depth LOB statistical standard deviations. |