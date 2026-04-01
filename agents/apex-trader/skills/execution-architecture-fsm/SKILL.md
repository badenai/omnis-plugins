---
name: execution-architecture-fsm
description: Use when designing or debugging high-performance algorithmic execution pipelines, NautilusTrader finite state machines, HftBacktest tick-level simulations, or QuestDB time-series data architectures to guarantee backtest-to-live parity.
---

## The Iron Law

```text
Every state transition within the execution architecture must be strictly gated by computable array index inequalities, absolute price differentials, and ATR-derived volatility thresholds. Programmatic trade lifecycles must execute as Finite State Machines (FSM) driven by deterministic market microstructure metrics (e.g., standard deviation bounds of Order Flow Imbalance), strictly prohibiting subjective heuristics, retail acronyms (SL/TP), or physics-adjacent abstraction.
```

## Behavioral Rules

- When synchronizing asynchronous multi-timeframe tick data, enforce QuestDB `ASOF JOIN` queries to align multi-dimensional Level 2 arrays and eliminate lookahead bias.
- If assessing strategy viability, execute tick-level validation via HftBacktest utilizing Numba JIT arrays and Guéant–Lehalle–Fernandez-Tapia (GLFT) models to mathematically enforce simulated latency, partial fills, and queue position dynamics.
- When architecting the NautilusTrader execution pipeline, define every trade lifecycle event—including entries, programmatic scale-outs, and strict invalidations—as a closed Finite State Machine (FSM) transition triggered by exact Boolean gates.
- If calculating structural invalidation parameters, derive risk boundaries exclusively from ATR array values and absolute mathematical price differentials, actively discarding arbitrary percentage-based heuristics or retail risk terminology.
- When gating FSM breakouts, require deterministic validation through Multi-Level Order Flow Imbalance (MLOFI) standard deviation bound crossings and computable VPIN thresholds, completely bypassing simplified N-bar swing logic.
- If designing adaptive tempo state machines, utilize binary-temporal representations indexed to the immediately preceding tick event rather than relying on fixed-time loop thresholding.
- When managing high-throughput order flow matrices, process limit order book depletion metrics using explicit Numba-accelerated array math to trigger programmatic Liquidation Risk Exposure (LCE) state pullbacks.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "Implement a Stop-Loss (SL) and Take-Profit (TP) at 1.5%." | Replaces exact FSM state transitions, programmatic scale-out logic, and array-based risk boundaries with brittle retail jargon and arbitrary heuristics. |
| "Validate the kinematic momentum of the sequence." | Contaminates executable programmatic logic with meaningless physics-adjacent buzzwords instead of concrete computational array index inequalities. |
| "Assume fill at the bar midpoint for simplicity." | Violates the absolute requirement for backtest-to-live parity and destroys structural edge by bypassing GLFT queue position physics. |
| "Use an N-bar swing moving average to define the baseline." | Dilutes quantitative precision by substituting rigorous Multi-Level Order Flow Imbalance (OFI) processing with lagging retail simplifications. |
| "Apply stateful object-oriented sanitization protocols." | Abstracts away the concrete Boolean gates, explicit thresholding, and n-dimensional array math required for deterministic execution. |

## Quick Reference

| Architecture Component | Implementation Mandate | Mathematical / Data Anchor |
| :--- | :--- | :--- |
| **Data Synchronization** | `ASOF JOIN` strictly | Zero lookahead bias temporal array matching |
| **Microstructure Simulation** | `HftBacktest` + GLFT | Numba-accelerated latency & queue positioning |
| **Lifecycle Management** | `NautilusTrader` FSM | Boolean gates & absolute price differentials |
| **State Validation** | MLOFI & VPIN | Multi-level order flow standard deviations |
| **Risk / Invalidation** | Programmatic boundary math | Exact volatility-scaled (ATR) array indexes |
| **Event Timing** | Adaptive Tempo arrays | Binary-temporal tick-event indexing |