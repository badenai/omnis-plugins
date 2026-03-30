---
name: execution-architecture-fsm
description: Use when designing or debugging high-performance event-driven trading engines, Finite State Machines (FSM) for trade lifecycles, tick-level microstructure simulations (HftBacktest), or asynchronous time-series data pipelines (QuestDB).
filePattern: "**/*.py"
---

## The Iron Law

```text
Build every trade lifecycle exclusively as a strict Finite State Machine (FSM) governed by explicit boolean gates, exact array index inequalities, and ATR-derived absolute price differentials, guaranteeing zero-ambiguity state transitions, deterministic error-aware rollbacks, and mathematically constrained execution without reliance on retail heuristics or discretionary buffers.
```

## Behavioral Rules

*   Construct all trade lifecycles using strict Finite State Machines (e.g., via NautilusTrader) defining states such as `PENDING`, `PARTIAL_FILL`, `FILLED`, `R_MULTIPLE_BREAKEVEN`, and `CLOSED` through explicit boolean flags.
*   Enforce all state transitions via mathematically rigid boundaries utilizing array index inequalities and exact absolute price differentials (e.g., `current_price >= entry_price + (ATR(14) * 3.0)`).
*   Handle raw tick-level data ingestion asynchronously using QuestDB `ASOF JOIN` queries to deterministically bind trade execution events to the exact microsecond state of the limit order book.
*   Validate all execution logic through Numba-accelerated tick-level simulation frameworks (e.g., HftBacktest), explicitly modeling order feed latencies and probability-based queue positions.
*   Calculate Order Flow Imbalance (OFI) and limit order elasticity by transforming Level 2 depth arrays into continuous linear regression slopes over rolling micro-windows (e.g., 12 seconds) to threshold execution triggers.
*   Enforce position invalidation and scale-out logic programmatically via R-multiple breakeven state definitions and dynamic exposure compression, rejecting all retail acronyms.
*   Derive system deployment triggers strictly from mathematically bounded quantitative regime filters, requiring specific standard deviation limits (e.g., `VoV_Z_score <= 1.5`) and structural array alignments before enabling FSM execution.
*   Execute error-aware rollbacks immediately when a partial fill or connection drop violates the expected state boolean, automatically neutralizing active portfolio risk metrics.

## Red Flags

| Rationalization | Why Wrong |
| :--- | :--- |
| "We can manage the trade using SL and TP parameters." | Retail jargon replaces explicit, deterministically closed FSM state transitions and mathematically defined R-multiple scale-out logic. |
| "Let's track the kinematic variance of the price slope." | Hallucinates physics jargon; execution requires computable array indexing and strict absolute price differentials. |
| "Risk per trade is capped between 0.1% and 1.0%." | Relies on arbitrary heuristics instead of programmatic, mathematical position sizing and fraction-of-equity formulas. |
| "Trigger a stateful object-oriented sanitization protocol." | Empty superficial OOP jargon; state management requires explicit boolean gates and exact array manipulation. |
| "Calculate an N-bar moving average to filter the entry." | Ignores quantitative execution requirements; microstructure triggers must rely on Order Flow Imbalance (OFI) arrays and standard deviation bounds. |
| "The FSM will process $X \le Y$ using a kinematic event." | Contaminates the model with LaTeX math formatting and physics terms instead of explicit programmatic operators (`<=`) and concrete data structures. |

## Quick Reference

| FSM State / Process | Transition Trigger / Boundary | Data Structure | Validation / Engine |
| :--- | :--- | :--- | :--- |
| **Pending Entry** | `bid_price >= structural_threshold` AND `OFI_array[i] > std_dev_bound` | `numpy.ndarray` | HftBacktest (Queue Position) |
| **Active Position** | `fill_qty > 0` | Boolean FSM State | NautilusTrader |
| **Exposure Reduction** | `current_price >= entry_price + (ATR(14) * 3.0)` | Array Index Inequality | QuestDB ASOF JOIN |
| **Terminal / Invalid** | `current_price <= invalidation_coordinate` | Absolute Price Differential | Numba JIT Compilation |
| **Circuit Breaker** | `VoV_Z_score > 1.5` | Mathematical Threshold | System-wide State Override |