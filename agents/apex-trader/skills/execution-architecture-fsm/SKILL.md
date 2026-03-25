---
name: execution-architecture-fsm
description: Use when designing or debugging high-performance event-driven trading execution systems, Finite State Machine (FSM) lifecycles, state rollbacks, or adaptive tempo tick parsing frameworks.
filePattern: "**/*.py"
---

## The Iron Law

```text
All execution architecture must be strictly governed by closed-loop Finite State Machines (FSM) that couple deterministic signal generation with trade lifecycle management, utilizing explicit array index inequalities, boolean gates, absolute price differentials, and ATR volatility thresholds instead of retail heuristics or abstract object-oriented terminology.
```

## Behavioral Rules

*   Construct event-driven execution architectures (e.g., NautilusTrader) by strictly decoupling raw message handlers from the FSM lifecycle.
*   Restrict FSM node definitions to explicit binary states: `PRE_INITIALIZED`, `READY`, `RUNNING`, `STOPPED`, `DEGRADED`, and `FAULTED`.
*   Force the FSM into a `FAULTED` condition and execute a deterministic state rollback immediately upon encountering unhandled tick latency, partial fills, or array index arithmetic overflows.
*   Implement adaptive tempo processing via Binary-Temporal Representation (BTR) to shift execution state matrices only when tick tempo probabilities cross predefined, computable thresholds.
*   Govern system activation states algorithmically using baseline quantitative regime filters, such as Gamma Exposure (GEX) thresholds or Vol-of-Vol Z-scores exceeding explicit standard deviation bounds (e.g., > +1.5σ).
*   Encode dynamic position management using ATR-scaled market structure metrics, translating volatility into explicit `[Lower_Bound, Upper_Bound]` state transitions.
*   Dictate position sizing and trade lifecycle closures via mathematical risk formulations and programmatic R-multiple breakeven states, strictly avoiding retail trading acronyms (e.g., SL/TP) or arbitrary hardcoded percentage heuristics.
*   Integrate microstructure data directly into FSM transition logic by standardizing Order Flow Imbalance (OFI) scores strictly from -1.0 to +1.0 at defined L2 book depths.
*   Ensure every entry signal logic is strictly coupled to its programmatic execution function; an FSM cannot dispatch an order unless the corresponding invalidation array condition is mathematically closed.

## Red Flags

| Rationalization | Why Wrong |
| :--- | :--- |
| "Implement an SL/TP order constraint for this execution block." | Retail acronyms and static constraints break deterministic FSM state transitions, R-multiple programmatic tracking, and scale-out logic. |
| "Verify the breakout using kinematic validation." | Physics-adjacent terminology contaminates the programmatic vocabulary; strictly use array index inequalities, absolute price differentials, and boolean gates. |
| "Manage the trade state via a stateful object-oriented sanitization protocol." | Superficial OOP buzzwords abstract away the explicit mathematical operations and numeric variable checks required for determinism. |
| "A finite state machine is overkill here; just use a while loop for the script." | Bypassing closed-loop FSMs destroys the ability to handle asynchronous tick data, partial fills, and error-aware rollbacks, leading to data corruption. |
| "Cap the risk exposure to exactly 0.5% per trade." | Hardcoded percentage heuristics bypass programmatic risk encoding, correlation tracking, and dynamic sizing formulas based on account balance delta. |

## Quick Reference

| Concept | Implementation Requirement |
| :--- | :--- |
| **Strict FSM States** | `PRE_INITIALIZED`, `READY`, `RUNNING`, `STOPPED`, `DEGRADED`, `FAULTED` |
| **Error Handling** | Unhandled latency or partial fills trigger immediate `FAULTED` + rollback |
| **Pacing / Tick Parsing** | Binary-Temporal Representation (BTR) matrix shifts via tempo probabilities |
| **Dynamic Trailing** | Computed ATR-scaled boundaries encoded as `[Lower_Bound, Upper_Bound]` |
| **Order Imbalance** | Strict OFI standardization from -1.0 to +1.0 at specific depth limits |
| **Regime Circuit Breakers** | Z-Scored Vol-of-Vol (+1.5σ bounds) and quantitative GEX baselines |