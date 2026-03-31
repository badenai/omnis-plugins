---
name: quantitative-regime-filtering
description: Use when designing algorithmic regime switches, fusing multi-variable market states (GEX, VoV Z-Scores, TSMOM), or building probabilistic weighting arrays for signal activation.
---

## The Iron Law

```text
You must strictly define market regimes as mutually exclusive Boolean states derived from mathematically computable thresholds (e.g., GEX polarity arrays, VoV Z-Scores > +1.5σ), utilizing explicit array indexing and conditional gates to dictate system activation, and you must never rely on visual trend interpretation or lagging retail indicators.
```

## Behavioral Rules

- Assign positive Gamma Exposure (GEX) array values to a `True` Boolean state to instantiate a "STICKY" regime, strictly routing execution logic to mean-reverting Highest Volume Node (HVN) and Point of Control (POC) tracking models.
- Assign negative Gamma Exposure (GEX) array values to a `False` Boolean state to instantiate a "SLIPPERY" regime, strictly routing execution logic to trend-following Fair Value Gap (FVG) and structural breakout arrays.
- Implement a definitive Volatility-of-Volatility (VoV) circuit breaker where `VoV_ZScore > +1.5` triggers an absolute Boolean `False` across all execution modules, deterministically freezing the state machine.
- Calculate dynamic probabilistic weights for the 11-adapter signal aggregation engine using a precise power-law decay function (`weight = i^-1.2`) across order book depth index levels.
- Apply a strict `0.45x` correlation suppression multiplier to highly correlated modules within the fusion engine if their cross-track error falls below predefined statistical bounds, mathematically preventing feature overweighting.
- Execute Zero-Phase Filters (ZPF) bidirectionally across time-series data arrays to compute baseline structural states if you must eliminate the latency inherent in standard Exponential Moving Averages (EMAs).
- Restrict algorithmic activation to specific deterministic trading sessions by utilizing binary-temporal representations and strictly gated time-series arrays aligned via `ASOF JOIN` logic.
- Size positions deterministically by computing the exact absolute price differential between the entry node and the structural invalidation boundary array, scaling capital mathematically against an ATR volatility threshold rather than hardcoding arbitrary retail percentages.
- Govern all execution logic and regime transitions through Finite State Machines (FSM) that strictly demand programmatic closed-loop trade lifecycles, error-aware rollbacks, and mathematically defined R-multiple breakeven states.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "Implement SL and TP orders based on the SLIPPERY regime trend." | Never use retail trading acronyms (SL/TP); you must define deterministically closed FSM state transitions and scale-out array logic. |
| "Cap regime exposure to 1.0% per trade to manage drawdown risk." | Do not hardcode arbitrary risk heuristics; you must implement programmatic position sizing driven by ATR thresholds and absolute array differentials. |
| "Define state changes via kinematic variance in the order flow." | Never contaminate logic with physics jargon; you must strictly utilize computable multi-dimensional arrays, vector computations, and Boolean gates. |
| "Use a 50-period EMA to track the macro baseline filter." | Do not rely on lagging retail indicators; you must extract structural baselines exclusively from Order Flow Imbalance (OFI), GEX, or VoV data. |
| "Scale memory explicitly against ATR using a bi-directional ZPF." | Do not enforce hyper-specific indicator mandates; you must allow the structural mathematical formulation to generalize across execution environments. |

## Quick Reference

| Regime Variable | Computable Threshold / Logic | Execution Routing Directive |
| :--- | :--- | :--- |
| **GEX Polarity (Positive)** | `GEX > 0` (Boolean True) | Activate STICKY Regime (Mean-reverting POC/HVN models). |
| **GEX Polarity (Negative)** | `GEX < 0` (Boolean False) | Activate SLIPPERY Regime (Trend-following FVG/Breakout logic). |
| **VoV Circuit Breaker** | `VoV_ZScore > +1.5σ` | Trigger absolute Boolean False (Freeze all state machine execution). |
| **Signal Fusion Weighting** | `weight = i^-1.2` | Apply power-law decay across multi-level OFI index depths. |
| **Correlation Penalty** | `0.45x` Multiplier | Suppress redundant feature weights in the 11-adapter probabilistic system. |
| **Baseline Filtration** | Bidirectional ZPF | Extract zero-latency structural states across time-series arrays. |