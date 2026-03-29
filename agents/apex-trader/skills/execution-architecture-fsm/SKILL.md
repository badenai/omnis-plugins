---
name: execution-architecture-fsm
description: Use when designing or debugging high-performance event-driven trading execution systems, Finite State Machines (FSM) for trade lifecycles, and tick-level microstructure backtesting pipelines using NautilusTrader, HftBacktest, or QuestDB.
---

## The Iron Law

```text
Every execution architecture must encapsulate trade lifecycles strictly as Finite State Machines (FSM) driven by deterministic Boolean gates, exact array index inequalities, absolute price differentials, and asynchronous event callbacks, explicitly prohibiting ambiguous retail logic, hardcoded risk heuristics, or synchronous blocking calls.
```

## Behavioral Rules

- Implement trade lifecycles utilizing NautilusTrader as an event-driven state machine, guaranteeing strict state closures, dynamic scale-out logic, and error-aware rollbacks upon asynchronous tick events.
- Utilize HftBacktest to strictly enforce deterministic accounting for feed and order latencies, reconstructing Level-2/Level-3 Limit Order Books (LOB) utilizing Numba JIT for micro-second accuracy.
- Query and synchronize asynchronous multi-timeframe tick data utilizing QuestDB ASOF JOINs to ensure exact temporal alignment across multi-dimensional LOB arrays.
- Calculate programmatic position sizing, dynamic ATR volatility thresholds, and explicit R-multiple breakeven state definitions using exact mathematical logic and matrix operations.
- Enforce time-based trade invalidations utilizing explicit Mean Time To Violation (MTTV) programmatic thresholds to natively terminate stale execution states.
- Encode structural market state transitions utilizing explicit computational data structures, exact array index inequalities, and Boolean gates rather than superficial object-oriented abstractions or physics-adjacent terminology.
- Determine institutional displacement utilizing programmatic absolute price differentials, Order Flow Imbalance (OFI) arrays, and strict standard deviation bounds.
- Trigger automated exposure compression protocols systematically to reduce leverage when cross-asset structural correlation breaches mathematically defined coefficient limits.
- Process tick-level feature engineering utilizing finmlkit and Numba JIT compilation for >100x speedups, strictly avoiding standard Pandas dataframes in the latency-sensitive execution path.
- Sequester high-latency algorithmic inputs (e.g., LLM API responses) into higher-timeframe (H4/D1) regime filters to ensure they are fully decoupled from sub-millisecond execution loops and high-velocity liquidity sweep FSMs.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "Using SL and TP variables simplifies the exit logic for this algorithmic trade." | Contaminates execution architecture with retail trading simplifications; demands explicit R-multiple breakeven states and FSM-driven scale-out logic. |
| "Scale risk exposure arbitrarily between 0.1% and 1.0% based on signal strength." | Hardcodes arbitrary heuristics; requires pure programmatic mathematical position sizing constrained by dynamic ATR arrays. |
| "We use kinematic validation and RANSAC flat slopes for our entry triggers." | Introduces physics and machine learning buzzwords that reduce executable code clarity; execution triggers require strict array index inequalities and Boolean gates. |
| "We can manage the trade status with a stateful object-oriented boolean flag." | Submits superficial OOP jargon instead of rigorous architectural enforcement; trade lifecycles require a formalized Finite State Machine with closed loop transitions. |
| "We will use standard Pandas `merge_asof` for tick aggregation in the live loop." | Violates high-frequency latency mandates; execution systems must utilize Numba JIT arrays and Time-Series DB (QuestDB) ASOF JOINs for sub-millisecond sync. |

## Quick Reference

| Concept | Implementation Standard | Architecture Requirement |
| :--- | :--- | :--- |
| **Microstructure Backtesting** | HftBacktest (Rust / Numba JIT) | Enforce exact feed/order latencies & Level-2/3 queue position modeling. |
| **Trade Lifecycle Engine** | Event-Driven FSM (NautilusTrader) | Asynchronous tick parsing, strict state closures, and error rollbacks. |
| **Asynchronous Data Sync** | Time-Series Database (QuestDB) | Utilize ASOF JOINs for multi-dimensional LOB arrays and temporal alignment. |
| **Risk & Invalidation** | MTTV & Exposure Compression | Programmatic mathematical sizing, ATR bounds, and strict R-multiple breakeven states. |
| **Execution Logic Encoding** | Array inequalities & Boolean gates | Exclude subjective retail jargon, physics terminology, and superficial OOP abstractions. |