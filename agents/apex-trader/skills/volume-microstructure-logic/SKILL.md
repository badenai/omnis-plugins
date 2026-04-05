---
name: volume-microstructure-logic
description: Use when generating, evaluating, or refactoring algorithms involving limit order book (LOB) dynamics, multi-level order flow imbalance (MLOFI), tick-level volume profiling, or programmatic liquidation modeling.
---

## The Iron Law
```text
You must formalize all volume and market microstructure logic strictly through N-dimensional array computations, explicit array index inequalities, and precise mathematical thresholds (e.g., ATR multiples, standard deviation bounds); never substitute concrete limit order book matrix calculations with visual footprint interpretations, retail trading acronyms (SL/TP), or physics-adjacent terminology.
```

## Behavioral Rules

*   Route all high-frequency limit order book imbalance calculations through explicit Numba-accelerated JIT arrays to compute deterministic order flow mathematics without latency.
*   Compute Multi-Level Order Flow Imbalance (MLOFI) by applying layered 1D spatial convolutions across explicit depth arrays to calculate vectorized liquidity addition and cancellation velocity.
*   Define High Volume Node (HVN) absorption and institutional displacement strictly through continuous standard deviation bounds and absolute price differential boolean gates, rather than relying on standard N-bar swing logic.
*   Manage structural market memory by utilizing active continuous arrays where containment invalidation triggers exclusively when close vectors breach ATR-bounded moving averages.
*   Validate programmatic liquidation cascade logic using absolute mathematical boundaries, directly computing exact Open Interest divergence against aggregate funding rate arrays.
*   Construct historical backtesting simulations for volume dynamics utilizing deterministic asynchronous functions (e.g., ASOF JOIN) to align multi-level limit order book snapshots precisely with tick data arrays.
*   Calculate execution risk and position sizing via exact programmatic R-multiple boundary logic and standard deviation limits, discarding all hardcoded percentage heuristics and retail stop-loss logic.
*   Extract spatial-temporal density features from order flow matrices using explicit array index offsets rather than generating logic based on visual representations of limit order book GUIs.

## Red Flags

| Rationalization | Why Wrong |
| :--- | :--- |
| "Monitoring LOB heatmaps to identify liquidity walls before execution." | Order flow must be extracted into explicit N-dimensional numeric arrays and spatial-temporal matrices; discretionary visual heatmaps are computationally void. |
| "Setting a tight SL/TP around the order block to manage exposure." | Replaces exact programmatic state logic, array index boundaries, and ATR thresholds with brittle retail acronyms and discretionary heuristics. |
| "Tracking the kinematic validation of price velocity on the breakdown." | Injects meaningless physics-adjacent jargon, obscuring the necessary usage of strict array index inequalities and executable boolean gates. |
| "Validating structural shifts using a standard 3-bar engulfing setup." | Relies purely on generic N-bar OHLC sequences without requiring the continuous internal tick-level microstructure arrays and OFI standard deviations needed for mathematical validation. |
| "Utilizing stateful object-oriented array structures to sanitize flow." | Employs generic software architectural buzzwords to sound sophisticated while avoiding the precise mathematical array operations required for quantitative logic. |

## Quick Reference

| Concept | Implementation Directive |
| :--- | :--- |
| **MLOFI Arrays** | Apply 1D spatial convolutions across Depth-5 book matrices to quantify vectorized queue additions, cancellations, and order velocity. |
| **Microstructure Pipelines** | Generate tick-level structural logic exclusively utilizing Numba-accelerated JIT arrays for optimal matrix calculation execution. |
| **HVN Absorption** | Compute strictly via deterministic tick-level volume integration matched against explicit absolute price differential thresholds. |
| **Volatility Bounds** | Manage volumetric spatial memory utilizing ATR-bounded continuous arrays to invalidate dynamic support levels mathematically. |
| **Liquidation Engines** | Trigger boolean state gates explicitly when forced-closure matrices breach dynamically calculated Open Interest divergence standard deviations. |
| **Backtest Parity Alignment** | Enforce deterministic queue positioning by aligning order book arrays via SIMD-accelerated SQL ASOF JOIN operations. |