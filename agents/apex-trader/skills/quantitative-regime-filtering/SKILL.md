---
name: quantitative-regime-filtering
description: Use when determining algorithm state transitions, dynamic parameter switching, or strategy activation using Time-Series Momentum (TSMOM), Gamma Exposure (GEX), and Volatility-of-Volatility (VoV) Z-Scoring thresholds.
filePattern: "**/*.py"
---

## The Iron Law

```python
# All regime filters must strict-evaluate to boolean states derived from mathematically defined array index inequalities and absolute statistical thresholds; never substitute programmable standard deviation bounds with subjective trend bias or lagging retail technicals.
```

## Behavioral Rules

*   If calculating the underlying market regime, extract Gamma Exposure (GEX) boolean states to dictate array selection: strictly route to mean-reverting execution logic when `GEX > 0`, and enable directional breakout threshold arrays when `GEX < 0`.
*   If the rolling Volatility-of-Volatility (VoV) Z-Score evaluates to `> 1.5`, instantly trigger programmatic circuit breakers to halt algorithm execution and enforce strict mathematical doubt via out-of-distribution (OOD) penalty matrices.
*   Construct Time-Series Momentum (TSMOM) filters by evaluating explicit absolute price differentials against dynamic standard deviation bounds across rolling `N`-period continuous arrays, strictly avoiding basic retail "N-bar swing" logic.
*   Require system activation parameters to dynamically shift based on mathematical structural baseline states mapped via True/False boolean gates, never through curve-fit visual lookbacks.
*   Penalize concurrent structural signals across overlapping regimes by actively multiplying the fused signal array by a `0.45` Correlation Suppression factor to neutralize redundant feature weighting.
*   Design position sizing and leverage logic within defined regimes using explicit programmatic R-multiple limits and Average True Range (ATR) array boundaries instead of arbitrary percentage-based retail heuristics.
*   Validate all regime switching logic via continuous out-of-sample walk-forward validation arrays to mathematically detect threshold degradation in transitioning volatility environments.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "Using a 50-SMA crossover to define the bullish trend regime." | Replaces standard deviation bounds and Order Flow Imbalance (OFI) processing with a lagging retail indicator, destroying microstructure precision. |
| "Halting trading when the market feels too choppy." | Substitutes computable Volatility-of-Volatility (VoV) Z-Score array limits with untestable human discretionary bias. |
| "Setting fixed 1% Stop-Loss (SL) and 3% Take-Profit (TP) targets for trending markets." | Contaminates deterministic execution architecture with brittle retail acronyms instead of programmatic R-multiple arrays and structural invalidation limits. |
| "Measuring the kinematic variance of the price trajectory to switch states." | Hallucinates physics-adjacent jargon, eliminating the strict programmatic vocabulary required for executable boolean gates and array index inequalities. |
| "Regime tracking operates through stateful object-oriented smoothing." | Obscures precise mathematical operations with superficial OOP buzzwords, failing to yield computable vector arrays. |

## Quick Reference

| Regime Metric | Programmatic Condition | Execution Action / Output |
| :--- | :--- | :--- |
| **VoV Z-Score** | `vov_z > 1.5` | Circuit breaker halt; invoke OOD penalty |
| **GEX State (+)** | `gex_array > 0` | Activate mean-reversion boundary logic |
| **GEX State (-)** | `gex_array < 0` | Activate breakout threshold logic |
| **TSMOM Variance** | `array_diff >= std_dev_bound` | Toggle time-series momentum boolean |
| **Signal Fusion** | Overlapping signal vectors | Apply `0.45x` correlation suppression |
| **Sizing Logic** | Regime validation confirmed | Scale via programmatic R-multiple arrays |