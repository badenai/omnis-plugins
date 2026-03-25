---
name: execution-architecture-fsm
description: Use when designing high-frequency trading execution logic, Finite State Machines for trade lifecycles, Numba JIT-compiled tick pipelines, Depth-5 Order Flow Imbalance matrices, Zero-Phase Filters, or absolute programmatic array index bounds.
filePattern: "**/*.py"
bashPattern: "pytest|unittest"
---

## The Iron Law

```text
Every high-frequency execution condition and structural trigger must be formalized as a strict, deterministic computational framework utilizing zero-ambiguity array index inequalities, discrete boolean logic gates, dynamic volatility limits (e.g., ATR multipliers), and exact mathematical formulas within a strictly closed Finite State Machine (FSM).
```

## Behavioral Rules

- Compile raw tick data pipelines natively using Numba JIT functions to bypass pandas-based event processing latency and permit sub-microsecond array queueing.
- Calculate Order Flow Imbalance (OFI) programmatically by aggregating volumetric data up to 5 limit book depths (L=5), scaled strictly from -1.0 to 1.0.
- Validate Fair Value Gaps (FVG) exclusively by quantifying the absolute slope of tick-level linear regression (`|beta_1|`), mandating a velocity array parameter of `<= 0.00015` units/sec for execution matrix inclusion.
- Reject structural gap velocity signals computing `> 0.0004` units/sec via absolute boolean exclusion filters to eliminate algorithmic limit order noise.
- Implement algorithmic signal smoothing bidirectionally utilizing Zero-Phase Filters (ZPF) to compute real-time cross-track errors without introducing time-series phase lag.
- Enforce rigid event-driven error handling within FSM lifecycles by programming a fail-fast arithmetic overflow policy that immediately forces execution matrices into a `FAULTED` state upon timestamp or volumetric array corruption.
- Define FSM gated breakouts by natively bounding a 3-node imbalance array directly against an N-period dynamic rolling min/max threshold.
- Lock structural execution failure boundaries deterministically to the extreme array index of the third reference node in the sequence to ensure mathematically sound risk truncation.
- Map structural Zones of Failure by indexing exactly three programmatic attempts to breach an array maximum before triggering a short algorithmic state inversion upon mathematical divergence of the third node.
- Regulate intrabar FSM velocity strictly via Binary-Temporal Representations (tempo bits) to replace fragile, time-based execution parameters.
- Bind institutional displacement matrices to Relative Volume (RVOL) array thresholds strictly computing `> 1.5x` before appending nodes to active execution sequences.
- Control active portfolio matrices using exposure compression protocols that scale down active algorithmic leverage proportionally when multi-asset correlation matrices breach predefined elasticity baselines.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "Implement an SL and TP at the 0.5% level for the execution logic." | Relies on brittle retail trading heuristics (SL/TP) and arbitrary percentages instead of programmatic R-multiple arrays and FSM state scale-out transitions. |
| "The execution matrix tracks kinematic variance of the price momentum." | Introduces cross-domain physics jargon ("kinematic variance") that abstract away executable array index inequalities and quantifiable volatility thresholds. |
| "Use an N-bar swing crossover to detect market displacement." | Diminishes complex market microstructure capabilities by substituting exact standard deviation bounds and Depth-5 OFI regression with basic retail lagging logic. |
| "Build a stateful object-oriented data class to manage price arrays." | Replaces precise mathematical operations, absolute price differentials, and Numba JIT constraints with generic, superficial software engineering jargon. |
| "If the FVG is triggered, enter the trade using the signal indicator." | Decouples signal generation from risk encoding; fails to encode strict internal failure modes, bounding arrays, or mathematical FSM containment states. |

## Quick Reference

| Architecture Component | Deterministic Formulation |
| :--- | :--- |
| **Data Processing** | Numba JIT compilation for sub-microsecond event queueing arrays. |
| **Order Flow Imbalance** | Depth-5 volumetric aggregation (L=5) scaled geometrically from -1.0 to 1.0. |
| **Tick-Level FVG Regression** | Absolute slope degree (`|beta_1|`) validation `<= 0.00015` units/sec velocity. |
| **FSM Error Handling** | Immediate fallback to `FAULTED` state on volumetric/timestamp arithmetic overflow. |
| **Signal Filtering** | Bidirectional Zero-Phase Filters (ZPF) for cross-track calculation devoid of lag. |
| **FSM Breakout Arrays** | 3-node bounds against N-period dynamic rolling min/max dynamic thresholds. |
| **Velocity Control** | Binary-Temporal Representations replacing time-based FSM hyperparameters. |