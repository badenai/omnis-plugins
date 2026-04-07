---
name: execution-architecture-fsm
description: Use when designing or debugging high-frequency trading architectures, finite state machine (FSM) trade lifecycle execution, backtest-to-live parity pipelines, HftBacktest LOB simulations, NautilusTrader integrations, QuestDB tick-data pipelines, or deterministic array-based execution constraints.
filePattern: "**/*.py"
bashPattern: "pytest|unittest"
---

## The Iron Law

```text
Every high-frequency execution architecture must guarantee absolute backtest-to-live parity through closed-loop Finite State Machines (FSM), deterministic order-book simulation natively modeling partial fills and queue positioning, and strictly programmable risk logic utilizing continuous array index inequalities, dynamic volatility thresholds (e.g., ATR multiples), and explicit boolean gates, completely eliminating arbitrary retail heuristics or unquantifiable discretionary states.
```

## Behavioral Rules

- When architecting trade lifecycles, construct rigid Finite State Machines (FSMs) via NautilusTrader that enforce explicit state closures, asynchronous external trade event handling, and error-aware rollbacks.
- When validating historical execution parity, simulate Level-3 Limit Order Book (LOB) dynamics utilizing HftBacktest to mathematically model deterministic queue priority and exact order-fill mechanics.
- If ingesting multi-timeframe tick data, pipeline the arrays through QuestDB utilizing deterministic `SAMPLE BY` time-bucketing and `ASOF JOINs` to guarantee precise asynchronous L2 synchronization.
- Structure all algorithmic condition triggers using strict array index inequalities, boolean gates, absolute price differentials, and Numba-accelerated multi-dimensional array operations.
- Enforce strict `Decimal` object utilization or integer-based tick parsing across all pricing models to structurally eliminate floating-point precision drift.
- If an algorithm manages prolonged active states, enforce deterministic halt gates utilizing Mean Time To Violation (MTTV) metrics and Vol-of-Vol (VoV) standard deviation bounds to systematically terminate stale executions.
- When defining exit conditions, programmatically encode risk using mathematical position sizing formulas and dynamic R-multiple breakeven state definitions rather than implementing static retail percentage constraints.
- Integrate Order Flow Imbalance (OFI) calculations natively into execution FSMs to mathematically quantify multi-level limit order book liquidity addition and cancellation velocity prior to fill routing.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "I added a 1% SL and 3% TP to manage trade risk." | Injects retail trading heuristics; execution must utilize dynamic, ATR-bounded mathematical position sizing and programmed R-multiple state transitions. |
| "Let's filter the kinematic variance to map the momentum shift." | Contaminates codebase with irrelevant physics terminology; price action must be mathematically expressed via Order Flow Imbalance and exact standard deviation bounds. |
| "Assumed the market executes the fill at the close price of the active bar." | Destroys backtest-to-live parity; must utilize HftBacktest and deterministic LOB simulation for partial fill and queue priority mechanics. |
| "Triggered a long position when the simple threshold crossed." | Lacks FSM state closures; all entries must strictly transition a defined Finite State Machine from one mathematically closed state to another. |
| "Abstracted the array indexing into a stateful object-oriented queue for readability." | Introduces superficial programming jargon while stripping required Numba JIT array structures and precise computable boolean inequalities necessary for deterministic logic. |

## Quick Reference

| Concept | Formal Implementation |
| :--- | :--- |
| **Trade Lifecycle Management** | `NautilusTrader` strict FSM state transitions and error-aware rollbacks |
| **LOB Simulation Engine** | `HftBacktest` Level-3 modeling, probabilistic queue priority mapping |
| **Time-Series Sync** | `QuestDB` deterministic `SAMPLE BY` bucketing and `ASOF JOIN` logic |
| **Execution Mathematics** | Array index inequalities, boolean gates, absolute price differentials |
| **Performance Processing** | `Numba` JIT, strictly vectorized `Decimal` array computations |
| **Execution Invalidation** | Mean Time To Violation (MTTV), Vol-of-Vol (VoV) Z-Score threshold limits |
| **Risk Architecture** | Dynamic R-multiple breakeven states, ATR-bounded sizing formulas |