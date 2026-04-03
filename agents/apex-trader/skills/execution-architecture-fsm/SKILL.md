---
name: execution-architecture-fsm
description: Use when designing live trading engines, time-series data pipelines, event-driven execution systems, NautilusTrader components, tick data ingestion, Finite State Machine (FSM) trade lifecycle management, QuestDB ASOF JOIN temporal alignment, or Numba-accelerated microstructure processing.
filePattern: "**/*.py"
bashPattern: "pytest"
---

## The Iron Law

```text
Every execution pipeline must seamlessly bind programmable market structure mathematics (precise array index inequalities, absolute price differentials, ATR volatility thresholds) to rigid event-driven execution architecture, ensuring all trade lifecycles are governed strictly as closed-loop Finite State Machines (FSMs) with mathematically guaranteed Backtest-to-Live parity.
```

## Behavioral Rules

*   Implement trade lifecycles strictly as Finite State Machines (FSMs) using frameworks like `NautilusTrader`, guaranteeing closed loops, deterministic asynchronous event parsing, error-aware rollbacks, and explicit transition states.
*   Enforce Numba JIT compilation for generating tick-level footprints, CUSUM monitors, Order Flow Imbalance (OFI), and multi-dimensional L2/L3 array operations to eliminate `Pandas` DataFrame slicing latency bottlenecks.
*   Utilize `ASOF JOIN` logic within high-throughput time-series databases (e.g., QuestDB) for deterministic temporal alignment of disjointed multi-timeframe limit order book (LOB) ticks and asynchronous trade events.
*   Map structural price action boundaries explicitly into absolute numerical arrays, index inequalities, and boolean logic gates to trigger state transitions, completely avoiding abstract object-oriented wrappers that obfuscate mathematical operations.
*   Standardize execution topologies to ensure mathematical equivalence between `HftBacktest` queue simulation (explicitly modeling probabilistic queue positioning and network latency) and production NautilusTrader state machines.
*   Calculate position sizing and execution invalidation using dynamic array variables like ATR volatility scalars and R-multiple structural breakeven points rather than fixed-percentage retail logic.
*   Design continuous out-of-sample generation and walk-forward validation testing environments to autonomously handle drift attenuation and execution metric calculation natively within the pipeline.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "Implement simple Stop-Loss (SL) and Take-Profit (TP) parameters to limit exposure risk." | Contaminates execution architecture with retail concepts; fails to implement dynamically closed FSM state transitions and programmatic scale-out structures based on array bounds. |
| "A generic OOP stateful object protocol handles the execution abstraction." | Obscures necessary computational mechanisms; replaces precise mathematical constraints like array index inequalities and ATR bounds with unactionable buzzwords. |
| "Use standard Pandas DataFrame merges to align the tick data streams." | Introduces severe execution latency and temporal phase lag; mandates Numba-acceleration and asynchronous `ASOF JOINs` for rigorous multi-timeframe alignment. |
| "The FSM architecture handles lifecycle progression, so we can omit explicit price differentials in the trigger definition." | Over-specializes architectural design; starves the algorithm of the concrete, quantitative market structure logic required to drive those state transitions. |
| "Integrate an LSTM model to predict limit order book state changes in the pipeline." | Violates prohibitions against generic black-box predictive models; introduces Out-Of-Distribution (OOD) regime brittleness into a system requiring strict mathematical determinism. |

## Quick Reference

| System Component | Implementation Mandate | Output Target |
| :--- | :--- | :--- |
| **Pipeline Ingestion** | QuestDB `ASOF JOIN` asynchronous alignment | Deterministic multi-timeframe synchronization |
| **Microstructure Logic** | Numba JIT compilation for LOB arrays | Ultra-low latency footprint extraction & math |
| **Lifecycle Management** | `NautilusTrader` Event-Driven FSMs | Zero-ambiguity trade state closures |
| **Execution Simulation** | `HftBacktest` with GLFT queue positioning | Mathematical Backtest-to-Live Parity |
| **Condition Triggers** | Boolean gates, exact array index inequalities | Definitive state transition activation |
| **Risk & Scaling Rules** | Dynamic ATR scalars + absolute price deltas | Programmatic Mean Time To Violation (MTTV) |