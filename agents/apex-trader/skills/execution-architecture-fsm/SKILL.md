---
name: execution-architecture-fsm
description: Use when architecting event-driven trading execution, designing Finite State Machines (FSM) for trade lifecycles, configuring NautilusTrader or HftBacktest, managing tick-level limit order book simulation, or ensuring mathematical backtest-to-live parity via QuestDB data pipelines.
filePattern: "**/*.py"
bashPattern: "pytest|nautilus|hftbacktest"
---

## The Iron Law

```text
Every trade lifecycle must be explicitly managed as a deterministic Finite State Machine (FSM) where simulated order execution strictly mirrors live production dynamics. You must define all entry, partial fill, cancellation, and exit states using absolute mathematical thresholds, precise array index inequalities, and ATR-derived standard deviation bounds, refusing any abstract state transition that lacks concrete programmatic price and order flow logic.
```

## Behavioral Rules

*   Construct every trade lifecycle using strict Finite State Machine (FSM) execution frameworks (e.g., NautilusTrader or project-x-py) to manage asynchronous external trade events and error-aware rollbacks.
*   Enforce absolute backtest-to-live parity by requiring historical simulations in HftBacktest to mathematically match production environments, explicitly accounting for Market-By-Price (MBP), Market-By-Order (MBO), network latency, and simulated queue position dynamics.
*   Define invalidation logic and state transitions using computable array index inequalities, concrete mathematical definitions, and absolute price differentials.
*   Calculate algorithmic position sizing and risk boundaries using strictly computed R-multiples and mathematical breakeven state definitions.
*   Execute time-series vectorization and limit order book (LOB) multi-dimensional arrays utilizing QuestDB `ASOF JOIN` and `SAMPLE BY` SQL extensions to mathematically eliminate look-ahead bias and lagless structural reconstruction.
*   Incorporate time-based invalidation metrics (e.g., Mean Time To Violation/MTTV) natively within FSM failure loops to close stale trade states.
*   Compute order queue positioning and reservation prices dynamically using the Guéant–Lehalle–Fernandez-Tapia (GLFT) model to adjust for inventory risk skewing during microstructure simulation.
*   Process multi-timeframe structural mapping deterministically, passing validated multi-level Order Flow Imbalance (OFI) and VoV limits as immutable boundary parameters into the execution engine.
*   Formalize DeFi AMM structural logic via DeFiPy down to the tick level, utilizing Q64.96 machine precision arithmetic to prevent floating-point desyncs during simulated concentrated liquidity execution.

## Red Flags

| Rationalization | Why it's wrong |
| :--- | :--- |
| "Setting SL and TP handles the trade logic." | Introduces retail trading acronyms; algorithmic architecture demands exact mathematical scaling logic, deterministic FSM state closures, and R-multiple breakeven programming. |
| "The state machine manages the logic, so we don't need exact price arrays." | Over-abstracts execution and deletes mathematical formulation; FSMs must bind directly to structural baseline states using computable array inequalities. |
| "We can use simple N-bar swings or moving averages to trigger the backtest execution." | Strips out quantitative architecture; execution must rely on full L2 depth reconstruction, tick-level Order Flow Imbalance (OFI), and ATR standard deviation bounds. |
| "Use 'kinematic momentum' to validate the breakout and transition trade states." | Contaminates execution code with irrelevant physics jargon; structural validation must exclusively utilize deterministic volumetric or programmatic price-per-second regression logic. |
| "We will use stateful object-oriented arrays to handle the sanitization protocol for signals." | Replaces precise computational directives with generic programming jargon; requires exact mathematical operations and vector management. |

## Quick Reference

| System / Component | Deterministic Implementation Mandate |
| :--- | :--- |
| **Execution Architecture** | Event-Driven FSM (`NautilusTrader`, `project-x-py`) with strict state transitions |
| **Simulation Parity** | `HftBacktest` (MBO/MBP, latency simulation, GLFT inventory modeling) |
| **Data Ingestion** | `QuestDB` utilizing `ASOF JOIN` for ultra-high throughput async tick parsing |
| **DeFi Parity** | `DeFiPy` Q64.96 precision bounds for Uniswap V3 concentrated liquidity execution |
| **State Triggers** | Array Index Inequalities, Absolute Price Differentials, ATR standard deviations |
| **Invalidation Rules** | Programmatic Risk Bounds, FSM Rollbacks, Mean Time To Violation (MTTV) |