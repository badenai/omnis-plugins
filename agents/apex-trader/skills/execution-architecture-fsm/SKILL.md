---
name: execution-architecture-fsm
description: Use when designing event-driven trading systems, high-frequency execution architectures, finite state machines (FSM) for trade lifecycles, or translating quantitative signals into deterministic order management using HftBacktest, NautilusTrader, Numba, or explicit array logic.
filePattern: "**/*.py"
bashPattern: "pytest"
---

## The Iron Law

```text
You must encode every execution lifecycle as a strictly closed Finite State Machine (FSM) governed by explicit array index inequalities, absolute price differentials, and Boolean gates. Never decouple mathematical signal generation from execution state transitions; you must mathematically define both the deterministic structural arrays (e.g., ATR volatility bounds) and the programmable error-aware rollbacks that manage asynchronous order flow without look-ahead leakage.
```

## Behavioral Rules

1. **Design deterministic trade lifecycles.** Construct all order execution modules as closed-loop finite state machines with explicitly mapped transitions (e.g., PENDING, PARTIAL_FILL, FILLED) and programmed error-aware rollbacks to prevent asynchronous deadlocks.
2. **Compute explicit mathematical signals.** Drive FSM state transitions utilizing precise algorithmic thresholds, including array index inequalities, absolute price differentials, and Boolean gates, completely ignoring subjective charting or lagging technical indicators.
3. **Compile tick-level microstructure.** Process intra-bar order flow imbalances and dynamic liquidity vectors using Numba-compiled machine code over raw array structures to guarantee low-latency execution and eliminate non-deterministic Pandas overhead.
4. **Enforce programmable risk and position sizing.** Calculate risk parameters using dynamic R-multiple breakeven states, ATR-scaled volatility arrays, and explicit mathematical sizing formulas rather than relying on fixed percentage heuristics.
5. **Gate execution via array synchronization.** Trigger state transitions only when an N-period dynamic rolling min/max breakout matrix mathematically synchronizes with structural generation arrays, ensuring unambiguous market structure containment.
6. **Implement robust temporal execution.** Utilize high-performance, event-driven backtesting engines (e.g., NautilusTrader, HftBacktest) to enforce precise temporal alignment of asynchronous L2 snap/tick data streams without introducing look-ahead bias.
7. **Validate logic out-of-sample.** Subject every formulated FSM architecture to strict walk-forward validation and continuous out-of-sample testing to mathematically verify risk-adjusted statistical expectancy.

## Red Flags

| Discretionary / Flawed Concept | Why it violates strict Execution Architecture FSM principles |
| :--- | :--- |
| Implementing retail "SL" or "TP" parameters | Replaces explicitly programmed FSM state transitions and calculated scale-out arrays with brittle, non-computable retail abstractions. |
| Referencing "kinematic validation" or "structural decay" | Contaminates programmable execution vocabulary with unactionable, cross-domain physics jargon instead of using concrete boolean gates. |
| Capping risk using arbitrary heuristics (e.g., "0.5% per trade") | Abandons deterministic, algorithmically derived position sizing models based on exact statistical expectancy and dynamic programmatic constraints. |
| Designing "stateful object-oriented sanitization protocols" | Obfuscates precise mathematical operations and explicit array indexing behind bloated, superficial programming buzzwords. |
| Abstracting execution states away from quantitative signals | Fails to physically link the mathematical arrays (e.g., ATR standard deviation bounds) to the actionable triggers required for closed-loop FSM trade lifecycles. |

## Quick Reference

| Architecture Component | Implementation Directive | Enforcement Standard |
| :--- | :--- | :--- |
| **Trade Lifecycle** | Closed-Loop Finite State Machine | Program exact state transition arrays and error-aware rollbacks. |
| **Signal Generation** | Array Index Inequalities | Require absolute price differentials and synchronized Boolean gates. |
| **Microstructure Logic** | Numba-Compiled Machine Code | Process tick flows via explicit multidimensional data arrays. |
| **Risk Encoding** | Programmatic Sizing Matrices | Calculate absolute constraints via ATR boundaries and R-multiples. |
| **Execution Engine** | Asynchronous Event-Driven Parsers | Mandate deterministic temporal alignment via NautilusTrader/HftBacktest. |