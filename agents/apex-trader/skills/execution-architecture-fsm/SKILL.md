---
name: execution-architecture-fsm
description: Use when designing high-frequency execution infrastructure, backtest-to-live parity models, HftBacktest simulations, NautilusTrader state closures, or QuestDB time-series synchronization logic.
---

## The Iron Law

```text
Every execution architecture must govern trade lifecycles via deterministic Finite State Machines (FSM), natively utilizing concrete array index inequalities, precise absolute price differentials, and Order Flow Imbalance (OFI) calculations to guarantee absolute backtest-to-live mathematical equivalence.
```

## Behavioral Rules

*   Construct rigid NautilusTrader Finite State Machines (FSM) transitioning exclusively through explicitly defined states (`PRE_INITIALIZED`, `READY`, `RUNNING`, `STOPPED`, `DEGRADED`, `FAULTED`, `DISPOSED`) using strict boolean gates.
*   Require ASOF JOINs via QuestDB when synchronizing multi-timeframe tick data to enforce deterministic temporal alignment and mathematically eradicate look-ahead bias.
*   Design execution models to mandate mathematical equivalence between HftBacktest simulations and live production by explicitly calculating queue position simulation, GLFT reservation prices, and partial fill dynamics via precise array operations.
*   Implement programmatic risk constraints utilizing Average True Range (ATR) volatility thresholds, Order Flow Imbalance standard deviation bounds, and absolute price differentials instead of static retail percentages or arbitrary heuristic rules.
*   Route core Order Flow Imbalance (OFI) matrix processing and limit order book depth calculations through Numba-accelerated JIT arrays to enforce vectorized, low-latency execution.
*   Encode explicit time-based invalidation metrics (e.g., Mean Time To Violation) and continuous out-of-sample memory arrays into every FSM to deterministically close stale or degraded states without ambiguity.
*   Process all asynchronous execution reports as unidirectional state transitions featuring hard-coded rollback arrays to manage partial fills or degraded exchange connectivity.
*   Apply probabilistic state shifting (Adaptive State Model in Binary-Temporal Representation) to transition FSM execution states dynamically based on sequential tick acceleration rather than static time thresholds.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "We can manage the trade using SL and TP values to lock in profits." | Contaminates logic with retail jargon; fails to implement programmatic R-multiple breakeven states, ATR volatility thresholds, and FSM scale-out logic. |
| "I'll implement a kinematic validation filter to manage the state decay." | Utilizes physics jargon; obscures concrete computational structures like array index inequalities and standard deviation bounds. |
| "We can align the tick data using standard Pandas merge functions." | Introduces massive look-ahead bias and latency; strict deterministic synchronization mandates ASOF JOINs and SIMD-accelerated SQL. |
| "The execution module uses an ML-classified confidence interval to trigger orders." | Replaces explicit, computable variables and boolean FSM gates with vague, non-deterministic black-box probabilities. |
| "Our backtest assumes full limit order fills whenever price touches the level." | Destroys backtest-to-live parity; ignores mathematically required queue position simulation and structural market impact constraints. |

## Quick Reference

| Concept | Action | Core Mechanism |
| :--- | :--- | :--- |
| **State Management** | Transition trade lifecycles via strict boolean logic | NautilusTrader FSM |
| **Data Synchronization** | Align asynchronous ticks without look-ahead bias | QuestDB ASOF JOIN |
| **Microstructure Modeling** | Vectorize OFI and LOB depth calculations | Numba-Accelerated JIT Arrays |
| **Execution Parity** | Reconstruct Market-By-Order logic and queue positioning | HftBacktest & GLFT Modeling |
| **Risk Containment** | Bound structural market memory and invalidation logic | ATR Thresholds & Array Indexing |