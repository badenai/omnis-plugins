---
name: execution-architecture-fsm
description: Use when designing algorithmic trading execution architectures, finite state machines (FSM) for trade lifecycle management, backtest-to-live parity simulations, high-performance time-series data pipelines (QuestDB, ASOF JOINs), or event-driven microstructure engines (NautilusTrader, HftBacktest, finmlkit).
filePattern: "**/*.py"
---

## The Iron Law

```text
All trade lifecycle management must be mathematically encoded as a deterministic Finite State Machine (FSM) utilizing explicit boolean gates, computable n-dimensional array indexing, and dynamically calculated absolute price differentials (e.g., ATR-scaled threshold tracking). Never substitute strict programmatic state transitions with retail trading heuristics (e.g., static SL/TP logic) or abstract architectural jargon. Absolute backtest-to-live computational parity is mandatory.
```

## Behavioral Rules

- If encoding a trade lifecycle, implement finite state machines with explicitly defined closure logic, asynchronous rollback mechanisms, and mathematically defined structural containment boundaries.
- When mapping time-series data pipelines for execution, utilize high-throughput infrastructures (e.g., QuestDB) employing `SAMPLE BY` with `FILL PREV` interpolation and precise `ASOF JOIN` operations to chronologically align asynchronous LOB events with executed trades.
- If simulating order execution, mandate `HftBacktest` or an equivalent tick-level simulator to natively model network latency, dynamic limit order book (LOB) queue positioning, and partial fill mathematics; never assume instant or deterministic fills at OHLC prices.
- When transitioning algorithms to live execution, deploy event-driven frameworks (e.g., `NautilusTrader`) enforcing exact `Decimal` types for Level 2 depth analysis to prevent floating-point drift across trade states.
- If processing Order Flow Imbalance (OFI), microstructure footprints, or spatial-temporal density arrays, implement Numba JIT compilation over raw memory arrays to bypass object-oriented serialization and ensure ultra-low latency execution.
- When managing execution timing logic, govern FSM entry transitions via the Adaptive State Model in Binary-Temporal Representation (ASMBTR) to calculate tick-acceleration probability matrices, completely discarding static time-delay constraints.
- If encoding risk management states, restrict position sizing and invalidation via dynamically calculated R-multiple breakeven formulas and programmatic array tracking, explicitly rejecting static percentage-based or retail limit constraints.

## Red Flags

| Rationalization | Why Wrong |
| :--- | :--- |
| "We will use standard Stop-Loss (SL) and Take-Profit (TP) parameters to manage the trade." | Contaminates execution architecture with rigid retail heuristics; ignores FSM requirement for dynamically computed scale-out math and volatility-bounded state invalidation. |
| "Let's assume trades execute at the close price of the bar for backtesting speed." | Violates absolute backtest-to-live parity; strips out essential queue position logic, multi-tranche fill dynamics, and latency penalties native to HftBacktest. |
| "A generic pandas dataframe and `merge_asof` will handle the LOB and trade alignment." | Fails at required ingestion scales (8M+ rows/s); relies on high-overhead object serialization instead of performant tick synchronization via QuestDB and array processing. |
| "We can manage the order logic using simple boolean flags inside a standard loop." | Subverts the strict Finite State Machine mandate; leaves asynchronous order events unhandled and lacks formalized error-aware rollbacks for rejected or partial states. |
| "This execution logic uses kinematic validation to predict fill probabilities." | Injects meaningless cross-domain physics jargon into what must strictly be explicit boolean logic, queue array indexing, and empirical probability distribution tracking. |

## Quick Reference

| System Requirement | Deterministic Implementation Pattern | Primary Framework / Tool |
| :--- | :--- | :--- |
| **Microstructure Simulation** | Compute queue position and execution latency mathematically: `mid + (alpha*forecast) - (beta*risk_skew)` | HftBacktest |
| **Data Alignment & Ingestion** | Synchronize ticks via `ASOF JOIN` and aggregate via `SAMPLE BY` / `FILL PREV` | QuestDB |
| **State Management** | Implement strictly closed, event-driven deterministic transitions using explicit array conditionals | NautilusTrader |
| **Array Data Processing** | Numba JIT compilation on raw memory vectors to bypass Python serialization | finmlkit / project-x-py |
| **Temporal Execution Logic** | Map asynchronous tick sequences using Binary-Temporal Representation (ASMBTR) | Adaptive Tempo FSM |