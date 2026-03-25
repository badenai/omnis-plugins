---
name: structural-formalization
description: Use when formalizing subjective price action into deterministic code, designing programmatic order flow or volume algorithms, mapping liquidity sweeps to arrays, or converting market structure rules into finite state machines and matrix bounds.
filePattern: "**/*.py"
bashPattern: "pytest|unittest"
---

## The Iron Law

```text
Every structural price action concept must be mathematically formalized using explicit array index inequalities, absolute price differentials, ATR volatility thresholds, and strict Boolean gates; if a market behavior cannot be defined as a measurable matrix boundary or closed-loop deterministic state transition, exclude it from the algorithmic architecture.
```

## Behavioral Rules

*   **Matrix Boundary Extraction:** Always translate subjective charting concepts (e.g., Fair Value Gaps, structural breaks, liquidity sweeps) strictly into computable matrix arrays and precise N-period dynamic rolling thresholds.
*   **FVG Formalization:** If defining a Fair Value Gap (FVG), validate institutional displacement strictly by measuring the absolute slope and applying a threshold velocity (e.g., <= 0.00015 units/sec) on its tick-level regression to filter algorithmic noise.
*   **ATR-Scaled Invalidation:** When building structural boundary arrays, scale memory buffers against dynamic Average True Range (ATR) vectors to manage dynamic invalidation trailing and trigger immediate state control flips upon breach.
*   **FSM Gated Breakouts:** Structure breakout algorithms to require a minimum 3-candle imbalance array natively bound to an N-period dynamic rolling min/max threshold, setting extreme node array sequence invalidation as the absolute risk cutoff.
*   **Order Flow Imbalance (OFI):** When calculating order flow dynamics, aggregate volumetric imbalance up to 5 levels deep (Depth-5 Level 2 regression) to accurately model institutional displacement and mitigate Level 1 (BBO) spoofing vulnerabilities.
*   **Programmatic Volume Profiling:** If tracking volume distributions, strictly bin tick volume into quintiles using NumPy, isolate the 80th percentile for High-Volume Nodes (HVN), and map Point of Control (POC) migration mathematically via percentage distance arrays.
*   **Regime State Switching:** Use quantitative baseline states—such as Gamma Exposure (GEX) polarity and Vol-of-Vol Z-Scores—to strictly toggle algorithmic execution logic (e.g., mandate range-equilibrium mean reversion during positive GEX; enable breakout finite state machines during negative GEX).
*   **Structural Failure Encoding:** Map zones of structural failure by indexing exactly three strict programmatic attempts to breach an array maximum, triggering counter-trend execution exclusively upon the mathematical divergence of the third node.
*   **Deterministic Risk Enforcement:** Always enforce a programmatic 1:3 R-multiple breakeven state constraint and multi-asset walk-forward validation prior to state activation; never initialize a sequence without deterministic closure logic.
*   **High-Frequency Execution Architecture:** If processing tick-level event arrays, implement Numba JIT compilation to bypass standard data frame execution latency and enable sub-microsecond structural break evaluation via Chu-Stinchcombe-White CUSUM tests.
*   **Event-Driven Error Handling:** Design closed-loop Finite State Machine (FSM) component lifecycles with strict fail-fast arithmetic overflow policies; cascade the execution framework immediately to a faulted state if timestamp or volumetric arrays overflow.

## Red Flags

| Rationalization / Concept | Why Wrong |
| :--- | :--- |
| Using "Kinematic validation" or "velocity vectors" without price differential definitions | Contaminates vocabulary with cross-domain physics jargon; abstracts away actionable array and matrix indexing logic. |
| Implementing "Stop-Loss (SL)" or "Take-Profit (TP)" retail heuristic variables | Relies on brittle retail jargon rather than deterministic R-multiple state scaling and programmatic extreme node sequence invalidations. |
| Restricting position sizing to "0.1% to 1.0%" hardcoded risk parameters | Replaces dynamic correlation elasticity matrices and exposure compression protocols with arbitrary, inflexible retail percentages. |
| Substituting array inequalities with generic "stateful object-oriented sanitization" | Employs superficial OOP buzzwords that starve the algorithm of the explicit mathematical operators needed for quantitative code. |
| Defining breakouts via "N-bar swing logic" or simple price action crossovers | Dilutes market microstructure modeling; ignores standard deviation bounds, Order Flow Imbalance arrays, and depth regression mechanics. |
| Executing standard lagging MACD/RSI calculations | Introduces structural phase distortions; deterministic systems require Zero-Phase Filters (ZPF) or bidirectional real-time cross-track computations. |

## Quick Reference

| Subjective Concept | Deterministic Algorithmic Formalization |
| :--- | :--- |
| **Fair Value Gaps (FVG)** | Absolute slope tick-level regression velocity bound within dynamic ATR-scaled upper/lower boundary arrays. |
| **Structural Breakouts** | 3-candle imbalance arrays bounded by N-period dynamic rolling min/max index thresholds. |
| **High-Volume Nodes (HVN)** | 80th percentile NumPy volume binning mapping deterministic POC percentage distance arrays. |
| **Institutional Displacement** | Depth-5 Order Flow Imbalance (OFI) scaling from -1.0 to +1.0 concurrent with standard deviation boundary expansion. |
| **Trend Exhaustion (ZPF)** | Indexed array sequences measuring 3 strict mathematical divergences against an N-period rolling array maximum. |
| **Liquidation Cascades** | Instantaneous programmed absolute price drops concurrent with isolated open interest (OI) metric collapse. |
| **Risk Encoding** | Closed-loop Finite State Machines enforcing strict 1:3 R-multiple matrix constraints and sequence bounds. |