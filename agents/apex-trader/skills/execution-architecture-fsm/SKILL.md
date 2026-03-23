---
name: execution-architecture-fsm
description: Use when designing high-performance event-driven algorithmic execution systems, building finite state machines (FSM) for trade lifecycles, or implementing error-aware state rollbacks in quantitative trading environments like NautilusTrader.
filePattern: "**/*.py"
bashPattern: "pytest|unittest|python"
---

## The Iron Law

```text
Trade lifecycles must be formalized as deterministically closed Finite State Machines (FSM) executing concrete programmatic logic—specifically array index inequalities, absolute price differentials, and boolean gates—mandating error-aware rollbacks for asynchronous failures while strictly rejecting subjective state management.
```

## Behavioral Rules

*   **Implement Event-Driven Execution:** Build automated trading pipelines using high-performance, event-driven architectures (e.g., NautilusTrader) to process microstructure-level ticks and enforce zero logic drift between backtesting and live production.
*   **Enforce FSM State Closures:** Formalize every discrete phase of a trade (entry routing, partial take-profits, trailing stop activation) as an explicit FSM state.
*   **Mandate Mathematical Transitions:** Trigger state transitions strictly using explicit, computable numeric thresholds, such as absolute price differentials, N-bar window logic, or Average True Range (ATR) volatility thresholds.
*   **Program Error-Aware Rollbacks:** Construct error-handling logic to immediately revert to mathematically safe FSM states when confronting asynchronous exchange API drops, partial fills, or disconnected websockets to prevent execution deadlocks.
*   **Align Multi-Timeframe Logic:** Utilize concurrent state machines to enforce fractal structural alignment, ensuring higher-timeframe states function as rigid boolean directional filters for lower-timeframe execution triggers.
*   **Synchronize Signals and Execution:** Couple your mathematical signal generation directly with your FSM architecture; never decouple the quantitative arrays that detect a setup from the specific execution state that routes the order.
*   **Filter Phase Lag Deterministically:** Process time-series data using structural baseline tracking that eliminates phase lag, but rely on generalized deterministic logic and boolean structures rather than over-constraining the model to hyper-specific mathematical indicator formulas.
*   **Encode Risk into Transitions:** Bind strict programmatic risk and position-sizing variables directly into the entry execution state logic, enforcing maximum risk ceilings via concrete numeric boundaries.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "Using kinematic validation to track the momentum state change." | Introduces physics-adjacent jargon that contaminates execution vocabulary; use explicit boolean gates and array indexing instead. |
| "Abstracting the execution via stateful object-oriented sanitization." | Replaces precise mathematical operations and quantitative execution arrays with unactionable, superficial programming buzzwords. |
| "Tracking trade progress using loosely updated global variables." | Fails to enforce mathematically closed FSM boundaries, leading to undefined system states during sudden market volatility or API disconnection. |
| "Focusing entirely on FSM states without defining signal logic." | Over-specializes the execution architecture while starving the algorithm of the absolute price logic and ATR boundaries required to generate real trades. |
| "Enforcing bi-directional Zero-Phase Filters for all momentum states." | Over-constrains the logic with hyper-specific mandates that conflict with broad, robust, programmatic trade lifecycle execution. |

## Quick Reference

| Architecture Component | Formalization Mandate |
| :--- | :--- |
| **Trade Lifecycle** | Model strictly as a Finite State Machine (FSM) with closed boundaries. |
| **Execution Infrastructure** | Utilize event-driven, low-latency queues (e.g., NautilusTrader). |
| **State Transitions** | Trigger via array index inequalities, absolute prices, and booleans. |
| **Error Handling** | Program deterministic rollbacks for all asynchronous API/network failures. |
| **Multi-Timeframe Structure** | Deploy concurrent FSMs where HTF booleans filter LTF order execution. |
| **Risk Encoding** | Hardcode exact dynamic sizing logic into the 'Active/Entry' state transition. |