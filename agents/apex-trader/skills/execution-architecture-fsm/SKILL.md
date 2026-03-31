---
name: execution-architecture-fsm
description: Use when designing event-driven trading pipelines, implementing Finite State Machines for trade lifecycles, structuring NautilusTrader/HftBacktest backtest-to-live parity, or managing high-frequency tick data arrays and asynchronous order flow logic.
---

## The Iron Law

```text
Every trade lifecycle must be governed by a mathematically closed Finite State Machine (FSM) utilizing explicit boolean gates, strictly indexed multi-dimensional data arrays, and absolute programmatic price/ATR differentials, guaranteeing zero-ambiguity state transitions and deterministic backtest-to-live execution parity.
```

## Behavioral Rules

- Use QuestDB `ASOF JOIN` operations and `SAMPLE BY` with gap-filling (`FILL PREV`) to deterministically align asynchronous tick streams and multi-level Order Flow Imbalance (OFI) arrays before passing them to the event-driven execution engine.
- Programmatically enforce closed-loop FSM trade lifecycles using NautilusTrader or HftBacktest by defining explicit state transitions (e.g., PENDING, PARTIAL, FILLED, ROLLBACK) governed entirely by boolean gates and strict array index inequalities.
- Enforce strict mathematical parity between backtest and live execution by directly modeling network latency, probability-based simulated queue positioning, and partial fill dynamics within the HftBacktest Guéant–Lehalle–Fernandez-Tapia (GLFT) framework.
- Construct invalidation parameters and state closures using absolute price differentials and Average True Range multipliers (e.g., `|Close - Open| > ATR(10) * BodyMultiplier`) rather than subjective concepts or arbitrary percentage heuristics.
- Encode minimum R-multiple breakeven state definitions and dynamically adjusting scale-out rules natively into the FSM exit logic to mathematically constrain risk per trade.
- Implement Numba-accelerated multi-dimensional array processing for raw trade data to compute depth-based Order Flow Imbalance (e.g., Depth 5-10) and evaluate limit order cancellation velocity over explicitly defined N-second rolling windows.
- Trigger deterministic error-aware rollback functions immediately upon detecting missing exchange data, unacknowledged order states, or asynchronous execution delays to prevent FSM deadlock and ensure structural integrity.
- Implement Adaptive State Models of a Binary-Temporal Representation (ASMBTR) where state transitions fire strictly based on predefined microstructural unit changes and precise temporal durations, completely eliminating the data loss inherent in static time-based charting bounds.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "Using SL/TP targets at 1% for risk management." | Employs retail acronyms and arbitrary percentage heuristics instead of explicit, deterministically closed FSM state transitions and mathematically calculated volatility thresholds (e.g., ATR multipliers). |
| "N-bar swing logic handles structural execution." | Replaces complex market microstructure concepts (Order Flow Imbalance, Level 2 depth arrays) and concrete computational tracking with basic, lagging retail simplifications. |
| "Applying FSM architecture to calculate position sizing parameters." | Shoehorns complex execution state architecture into basic arithmetic tasks; FSMs strictly govern asynchronous trade lifecycles and event-driven order states, not static formula derivations. |
| "Abstracting the trigger logic into a dynamic ML confidence variable." | Replaces concrete computational structures (array index inequalities, boolean gates) with generic machine-learning buzzwords, resulting in ambiguous, unactionable execution criteria. |
| "Using kinematic variance to measure order block momentum." | Contaminates execution architecture with cross-domain physics jargon, leading to meaningless code generation instead of strict programmatic array indexing and verifiable standard deviation bounds. |

## Quick Reference

| Action | Implementation Standard |
| :--- | :--- |
| **Tick-Data Synchronization** | `ASOF JOIN` via QuestDB with `SAMPLE BY ... FILL PREV` |
| **State Transition Triggers** | Explicit boolean gates and strict array index inequalities |
| **Volatility Breakout Bounds** | Absolute price differentials and ATR matrices (e.g., `ATR(10) * multiplier`) |
| **Backtest Parity Engine** | HftBacktest with GLFT modeling and probabilistic queue sizing |
| **High-Frequency Computation** | Numba-accelerated arrays for Level 2 multi-depth OFI parsing |
| **Lifecycle Exception Handling** | Deterministic error-aware rollbacks to prevent FSM deadlock |