---
name: volume-microstructure-logic
description: Use when generating deterministic, rule-based quantitative algorithms for order flow imbalance (OFI), algorithmic volume profiling, Limit Order Book (LOB) array reconstruction, and Point of Control (POC) or Highest Volume Node (HVN) absorption mechanics.
---

## The Iron Law

```text
You must formalize all volume and microstructure concepts as computable multi-dimensional arrays, boolean gates, absolute price differentials, and N-bar window logic. Never output subjective visual interpretations, retail acronyms (SL/TP), or abstract machine-learning buzzwords; if a volume profile or order book dynamic cannot be expressed via strict array index inequalities, standard deviation bounds, and programmatic risk constraints, it must be discarded.
```

## Behavioral Rules

*   Calculate Order Flow Imbalance (OFI) across specific Limit Order Book depths (e.g., Depth 5-10) using Numba-accelerated arrays to compute bid/ask delta metrics.
*   Define Highest Volume Node (HVN) absorption programmatically using discrete price-volume arrays and standard deviation bounds to trigger state transitions when volume accumulation exceeds +1.5σ.
*   Reconstruct Limit Order Book (LOB) dynamics utilizing rolling N-bar window logic and array index inequalities to separate genuine resting liquidity from cancellation velocity programmatically.
*   Validate all structural breakouts conditionally by demanding an absolute price differential (`|Close - Open| > ATR(10) * BodyMultiplier`) coupled strictly with an absolute volume threshold (`Current Volume > Volume_SMA(50)`).
*   Enforce mean-reversion Point of Control (POC) gap determinism using boolean gates that trigger execution strictly when a price array migrates outside the Value Area and closes back within the boundary constraint.
*   Manage high-frequency execution lifecycles using event-driven Finite State Machines (FSM) that close stale states strictly via predefined temporal durations or explicit R-multiple breakeven constraints.
*   Filter volume anomalies using bidirectional Zero-Phase Filters (ZPF) applied to tick-data arrays to isolate structural baseline states without introducing moving-average lag.
*   Compute programmatic Open Interest (OI) divergence alongside extreme exchange liquidation arrays to identify actionable squeeze cascades over strict temporal windows (e.g., 60-second execution gates).
*   Constrain risk programmatically by explicitly defining trade lifecycle closures using multi-dimensional position sizing arrays rather than hardcoded percentage heuristics.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "Wait for the heatmap to show strong absorption." | Relies on visual LOB GUI interpretation instead of explicit multi-level OFI array computations. |
| "Set a tight SL and TP based on the 15-minute chart." | Contaminates quant architecture with retail SL/TP jargon and subjective fixed-timeframes instead of using exact R-multiple constraints and FSM closures. |
| "Filter the signals using a RANSAC regression or ML classification." | Replaces concrete deterministic logic, Boolean gates, and array index inequalities with opaque, non-computable machine-learning buzzwords. |
| "Confirm the kinematic variance of the volume node." | Uses hallucinated physics terminology instead of standard programmatic metrics like standard deviation bounds or absolute volume differentials. |
| "Scale position size to 1% of account equity." | Utilizes arbitrary retail percentage heuristics rather than dynamic programmatic position sizing formulas constrained by ATR volatility thresholds. |
| "Wait for price to $\rightarrow$ the order block threshold $\le$ 0.5." | Uses abstracted LaTeX-style formatting instead of explicit code-level programmatic operators for absolute price differentials. |

## Quick Reference

| Concept | Deterministic Implementation Standard |
| :--- | :--- |
| **LOB Reconstruction** | Multi-dimensional arrays tracking liquidity addition and cancellation velocity via strict array index inequalities. |
| **Volume Validation** | Breakout displacement mandated by `\|Close - Open\| > ATR * Multiplier` paired with concurrent volume velocity arrays. |
| **Order Flow Imbalance** | Numba-accelerated processing calculating aggregate bid/ask delta at specific Level 2 depths (MLOFI). |
| **POC Determinism** | Boolean mean-reversion triggers executing exclusively when price drops outside VA boundaries and returns. |
| **Risk Execution** | Strict FSM state transitions governed by exact R-multiple calculations and ATR-scaled position arrays. |