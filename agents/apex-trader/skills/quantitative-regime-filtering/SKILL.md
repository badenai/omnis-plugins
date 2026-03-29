---
name: quantitative-regime-filtering
description: Use when determining system activation states, filtering execution logic based on Gamma Exposure (GEX), VoV Z-Scores, or aggregating multi-adapter quantitative signals into unified execution thresholds.
---

## The Iron Law

```text
You must govern system activation exclusively through deterministic Boolean gates and array index inequalities driven by Gamma Exposure (GEX), VoV Z-Scores, and standard deviation bounds. Never substitute precise programmatic execution thresholds (e.g., `vov_zscore > 1.5`, `gex < 0`) with ambiguous retail heuristics, subjective momentum descriptions, or arbitrary hardcoded percentage caps.
```

## Behavioral Rules

*   **VoV Circuit Breakers**: You must implement strict volatility circuit breakers using Volatility of Volatility (VoV) Z-Scoring, explicitly returning a Boolean `False` to block all entry functions if the VoV Z-Score exceeds `1.5` due to unstable volatility surfaces.
*   **GEX Routing Logic**: If Gamma Exposure (GEX) is positive, you must route execution logic exclusively to mean-reversion array structures; if GEX is negative, you must route execution to momentum breakout arrays.
*   **Signal Fusion Penalties**: If aggregating multi-adapter signals, enforce probabilistic consensus by mathematically applying a correlation suppression penalty (e.g., `0.45x` weight reduction) when independent adapters from the same analytical family align.
*   **Array Management**: Define structural baseline states and institutional displacement strictly using computable array index inequalities, absolute price differentials, and standard deviation bounds on Level 2 Order Flow Imbalance (OFI).
*   **Risk Scaling**: If transitioning between quantitative regimes, dynamically scale algorithmic position sizing based on real-time ATR volatility multipliers and strictly defined R-multiple breakeven states.
*   **Temporal Sequestering**: You must sequester high-latency external data inputs (e.g., LLM API sentiment coordinates) into high-timeframe (H4/D1) regime filters to prevent blocking sub-millisecond execution loops.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "Setting SL and TP at 1% and 3% to limit risk." | Uses retail acronyms and arbitrary heuristics instead of programmatic R-multiple breakeven states and dynamic ATR-scaled invalidation. |
| "Using kinematic validation to detect structural decay." | Contaminates execution code with physics jargon and artificial persona phrasing instead of utilizing absolute price differentials and boolean gates. |
| "Applying finite state machines to calculate position sizing parameters." | Shoehorns complex asynchronous state management into contexts requiring only straightforward array math and basic algorithmic arithmetic. |
| "Implementing a bi-directional Zero-Phase Filter for real-time signal smoothing." | Introduces mathematical lookahead bias, violating strict real-time determinism required for live event loop execution. |
| "Evaluating market momentum using MACD crossovers." | Relies on lagging retail indicators rather than deriving structural baselines from Order Flow Imbalance arrays and empirical microstructure execution data. |

## Quick Reference

| Regime Component | Programmatic Threshold | Deterministic Action |
| :--- | :--- | :--- |
| **GEX State > 0** | `gex_array[i] > 0` | Activate STICKY mean-reversion arrays |
| **GEX State < 0** | `gex_array[i] < 0` | Activate SLIPPERY breakout/expansion structures |
| **VoV Z-Score** | `vov_zscore > 1.5` | Trigger Boolean lock on all execution functions |
| **Signal Fusion** | `entropy_confidence >= threshold` | Apply correlation suppression to redundant adapters |
| **Displacement** | `ofi_array[i] > std_dev_bound` | Confirm institutional structural breaks |
| **Position Sizing** | `atr_multiplier * risk_unit` | Programmatically constrain risk via R-multiple limits |