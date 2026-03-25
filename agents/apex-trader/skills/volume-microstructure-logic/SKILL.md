---
name: volume-microstructure-logic
description: Use when designing, backtesting, or implementing deterministic algorithms that rely on order book depth, tick-level trade flows, volume profiles, High-Volume Nodes (HVN), Point of Control (POC) migrations, Order Flow Imbalance (OFI), and exchange liquidation mechanics.
filePattern: "**/*.py"
bashPattern: "pytest|unittest"
---

## The Iron Law

```text
You must formalize all microstructure and volume profile mechanics strictly through explicit programmatic computational structures: array index inequalities, absolute price differentials, N-bar window logic, standard deviation bounds, and boolean gates intrinsically tied to finite state machine (FSM) transitions. Never decouple signal generation arrays from event-driven execution architecture, and never substitute precise mathematical array bounds with retail jargon, arbitrary percentage heuristics, or abstracted physics/machine-learning buzzwords.
```

## Behavioral Rules

*   **Order Flow Imbalance (OFI):** Calculate OFI deterministically by aggregating Level-2 volumetric imbalances up to exactly 5 levels deep (Depth-5), scaling the numeric output strictly from `-1.0` to `1.0` using matrix array bounds.
*   **Tick-Level Event Parsing:** Process raw tick data arrays natively via Numba-compiled functions to eliminate latency, and evaluate sub-microsecond structural breaks strictly using mathematically rigorous Chu-Stinchcombe-White CUSUM tests.
*   **Volume Profile Determinism:** Bin volume distributions mathematically into NumPy array quintiles, categorizing High-Volume Nodes (HVN) exclusively at the 80th percentile threshold to eliminate subjective volume interpretation.
*   **POC Migration Tracking:** Track Point of Control (POC) migration by calculating absolute price differentials within `poc_distance_pct` arrays to compute value consensus rate of change.
*   **Liquidation Cascade Mapping:** Trigger a squeeze FSM execution exclusively upon the boolean convergence of three programmatic states: positive offshore Open Interest (OI) divergence arrays, negative funding rate integers, and positive spot premium differentials.
*   **Execution Architecture:** Manage trade lifecycle and order parsing exclusively through Finite State Machines (FSMs) utilizing "fail-fast" arithmetic overflow policies; cascade the state instantly to `FAULTED` if timestamp or volumetric arrays overflow.
*   **Mathematical Risk Encoding:** Validate structural matrices against absolute Average True Range (ATR) volatility thresholds and enforce position sizing programmatically; reject FSM state activation if programmatic R-multiple expectancy formulas (minimum 1:3 R:R) are not mathematically satisfied.
*   **Out-of-Sample Validation:** Require multi-asset vectorized walk-forward optimizations to measure out-of-sample survival rates, penalizing the algorithm's Sharpe and drawdowns strictly based on deterministic matrix performance rather than curve-fitted in-sample iterations.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "Setting a strict 1% Stop-Loss (SL) and 3% Take-Profit (TP) protects the algorithmic position." | Relies on retail trading jargon and arbitrary percentage heuristics instead of deterministically closed FSM state transitions and scale-out logic tied to programmatic array limits. |
| "The algorithm uses kinematic validation to detect institutional displacement based on flat slope momentum." | Injects physics-adjacent terminology and abstract phrasing instead of utilizing precise mathematical operations, standard deviation bounds, and concrete array index inequalities. |
| "We define the Fair Value Gap using a stateful object-oriented array class that tracks subjective zones of failure." | Replaces explicit programmatic bounds and absolute price differentials with superficial programming jargon, masking the lack of strict mathematical thresholds. |
| "Use K-Nearest Neighbors and ML-classified confidence to identify the volumetric structural breakout." | Substitutes exact programmatic signal definitions and clear boolean execution architecture with over-engineered, contradictory machine-learning buzzwords. |
| "Validate the breakout using a basic N-bar swing high/low technical logic check." | Replaces sophisticated market microstructure modeling (like OFI aggregation and Depth-5 Level 2 regression) with basic retail logic, diluting quantitative architecture. |

## Quick Reference

| Concept | Implementation Directive | Enforcement Matrix |
| :--- | :--- | :--- |
| **Depth-5 OFI** | Aggregate Level-2 volumetric imbalance up to L=5 (`-1.0` to `1.0`). | Multi-level arithmetic summation arrays |
| **Z-Scored Volume** | Bin volume distribution; HVN must meet $\ge$ 80th percentile. | NumPy array quintile thresholding |
| **Break Detection** | Apply Chu-Stinchcombe-White CUSUM tests on Numba tick arrays. | Mathematical sub-microsecond tests |
| **POC Migration** | Compute absolute rate of change via `poc_distance_pct` arrays. | Absolute price differential tracking |
| **Liquidation Event** | Activate FSM strictly on OI spike + negative funding + spot premium. | Concurrent boolean gate convergence |
| **State Management** | Utilize FSM components with fail-fast overflow cascading. | Native event-driven execution architecture |
| **Volatility Risk** | Measure arrays against absolute ATR bounds; enforce 1:3 R-multiples. | Array index limits & programmatic sizing |