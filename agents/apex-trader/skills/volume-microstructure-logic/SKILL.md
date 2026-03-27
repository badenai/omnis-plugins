---
name: volume-microstructure-logic
description: Use when designing tick-level order book algorithms, calculating Order Flow Imbalance (OFI) at specific book depths, formalizing volumetric imbalance mechanics, or vectorizing raw trade sequences for programmatic liquidity tracking and low-latency execution systems.
filePattern: "**/*.py"
---

## The Iron Law

```text
You must formalize all microstructure and order flow concepts into strictly computable multi-dimensional arrays, absolute price differentials, and threshold-gated Boolean logic. You must process top-of-book and depth-of-book events using exact array indexing and standard deviation bounds, never relying on lagging retail heuristics, subjective price action interpretations, or unquantifiable momentum approximations.
```

## Behavioral Rules

*   **Order Flow Imbalance Formulation**: When calculating Order Flow Imbalance (OFI), you must compute volumetric imbalance strictly at a depth of 5 levels (L=5) using explicit array subtraction and bid/ask queue size differentials to isolate predictive deterministic signals from top-of-book spoofing noise.
*   **Raw Trade Vectorization**: If processing raw asynchronous trade sequences, you must utilize Numba JIT compiled functions to vectorize tick-level data directly into information-driven volume bars, completely bypassing non-deterministic, time-based pandas aggregations.
*   **Liquidation Cascade Mapping**: When tracking exchange forced closures, you must cross-reference Open Interest (OI) destruction divergences against localized exchange reserves using explicit array inequalities to pinpoint the exact failure depths where order books mathematically break.
*   **Volume-Validated Expansion**: If defining structural breakout states, you must algorithmically verify volumetric proof-of-work by requiring a localized Volume Z-Score acceleration strictly greater than a predefined standard deviation threshold; otherwise, you must programmatically categorize the movement as a low-conviction liquidity hunt and trigger a reversion state.
*   **Execution Architecture Governance**: When mapping the trade lifecycle for microstructure events, you must implement a closed-loop Finite State Machine (FSM) that dictates deterministic state transitions, queue position probability modeling, and error-aware rollbacks without ever utilizing retail stop-loss abstractions.
*   **Dynamic Volatility Scaling**: You must scale all structural boundaries, imbalance memory arrays, and risk constraints using dynamic Average True Range (ATR) threshold multipliers and R-multiple breakeven definitions rather than hardcoded percentage risk heuristics.
*   **Point of Control (POC) Determinism**: If tracking volume profiles across multiple sessions, you must define POC migration and VWAP relative-positioning using exact coordinate arrays to construct high-probability mean-reversion anchors based on continuous out-of-sample data.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "We can use top-of-book (L=1) flow for faster signal generation." | Top-of-book order flow is highly susceptible to spoofing and introduces computational noise, corrupting the deterministic validity of the volumetric imbalance signal. |
| "Let's implement a standard SL/TP heuristic of 0.5% risk for this strategy." | Hardcoded percentage heuristics and retail risk acronyms replace the required programmatic position sizing, R-multiple math, and deterministic FSM rollback logic. |
| "The algorithm detects a kinematic volatility shift and flat slope consensus." | Physics-adjacent terminology contaminates the programmatic vocabulary; strict execution requires explicit mathematical bounds, array index inequalities, and Boolean gates. |
| "We will resample the tick data using Pandas time-based grouping for simplicity." | Non-deterministic and computationally slow Pandas aggregations introduce execution latency and destroy the pure asynchronous trade sequence needed for formalized microstructure modeling. |
| "Use an ML-classified confidence filter to determine structural context." | Over-specifying generic ML buzzwords abstracts away the explicit absolute price differentials and computable array structures required for precise algorithm qualification. |

## Quick Reference

| Microstructure Concept | Formalization Method | Algorithmic Constraint |
| :--- | :--- | :--- |
| **Order Flow Imbalance** | L=5 bid/ask volume differential array | Must filter out L=1 top-of-book spoofing noise. |
| **Raw Trade Processing** | Numba JIT compiled vectorized arrays | Must bypass slow time-based DataFrame aggregations. |
| **Execution Governance** | Closed-loop Finite State Machine (FSM) | Must define strict transition logic for queue modeling and rollbacks. |
| **Structural Expansion** | Localized Volume Z-Score > σ threshold | Must explicitly enforce volumetric proof-of-work via statistical bounds. |
| **Liquidation Sweeps** | OI destruction divergence vs exchange reserves | Must use precise array index inequalities to trigger entry states. |
| **Volatility Scaling** | ATR threshold multipliers applied to boundaries | Must dynamically compute boundaries instead of using fixed price ticks. |