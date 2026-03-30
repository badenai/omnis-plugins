---
name: volume-microstructure-logic
description: Use when converting volume profiles, limit order books, multi-level order-flow imbalance (MLOFI), or liquidation cascades into computable N-dimensional arrays and deterministic execution state logic.
filePattern: "**/*.py"
---

## The Iron Law

```text
Require exact translation of order flow heatmaps, highest volume nodes (HVN), and limit order book depth into N-dimensional Numpy arrays; mandate the use of explicit array index inequalities, Numba-accelerated multi-level order-flow imbalance (MLOFI) processing, absolute price differentials, and standard deviation bounds to trigger deterministic Boolean execution states.
```

## Behavioral Rules

- If scraping visual order flow heatmaps (e.g., Bookmap liquidity clustering), strictly convert the resting limit order "bubbles" into N-dimensional Numpy arrays rather than applying visual density heuristics.
- If defining Order Flow Imbalance (OFI) at specific limit book depths (e.g., Depth 5), utilize Numba-accelerated linear regression slopes calculated over rolling micro-windows (e.g., 12-second intervals) to mathematically separate spoofed liquidity from true institutional absorption.
- If evaluating volume distributions, enforce algorithmic Z-Scored Volume Profiles and strictly gate directional continuation triggers behind a Point of Control (POC) migration that mathematically exceeds predetermined bounds (e.g., > 1.5% distance from session open).
- If modeling forced-closure events, utilize Programmatic Open Interest (OI) Divergence to map multi-tranche liquidation cascades, and trigger a localized Finite State Machine (FSM) drawdown isolation protocol if the primary sequence falls underwater by a defined scalar limit.
- If trading ES Futures structural mechanics, mandate POC Gap Determinism as a scaled Boolean trigger validated strictly against session-aware volume feature engineering to filter idiosyncratic noise.
- If formalizing liquidity sweep phenomena, evaluate passive limit order elasticity, resting limit density decay arrays, and Cumulative Volume Delta (CVD) divergence instead of writing logic optimized for anthropomorphic "stop hunting" by composite operators.
- If generating volume-validated structural expansion signals, map the mathematical confirmation of price expansion explicitly to decreasing volume arrays bounded by absolute ATR volatility thresholds and VWAP standard deviation bands.
- If validating execution latencies or queue position probability, natively implement HftBacktest tick-level simulation frameworks within the walk-forward validation matrix to prove execution timing edge.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "Implementing Stop-Loss (SL) and Take-Profit (TP) levels for the microstructure entry." | Substitutes deterministic FSM state closures, dynamic array-based scale-out logic, and time-based invalidation with lagging, brittle retail concepts. |
| "Filtering the gap tick data through kinematic variance and ML-classified confidence intervals." | Contaminates the algorithm with hallucinated physics-adjacent jargon and over-engineered buzzwords instead of relying on explicit mathematical array index inequalities and Boolean gates. |
| "Waiting for a visual confirmation of the liquidity sweep before executing the order block." | Relies on subjective charting and discretionary interpretation rather than processing mathematical limit density decay and computed OI arrays. |
| "Setting the algorithm to risk a flat 1.0% per trade to ensure account safety." | Replaces programmatic, volatility-scaled position sizing matrices and continuous Risk-Multiple mathematical evaluations with arbitrary heuristics. |
| "Using an N-bar simple moving average crossover on volume to detect order flow shifts." | Dilutes quantitative rigor by abandoning Multi-Level Order-Flow Imbalance (MLOFI), Numba acceleration, and Z-scored standard deviation bounds in favor of a lagging indicator. |

## Quick Reference

| Microstructure Concept | Deterministic Array/Math Implementation |
| :--- | :--- |
| **Order Book Heatmaps** | N-dimensional Numpy arrays mapping local resting limit density |
| **Order Flow Imbalance** | Numba-accelerated linear regression slopes over rolling micro-windows |
| **POC Migration** | Z-Scored array distance tracking > 1.5% deviation from session open |
| **Liquidation Cascades** | Multi-tranche FSM state isolation via Open Interest (OI) divergence tracking |
| **Institutional Displacement** | Array index inequalities checking against absolute ATR and VWAP standard deviation bounds |
| **Liquidity Sweeps** | Computed resting limit order elasticity and Cumulative Volume Delta (CVD) decay formulas |