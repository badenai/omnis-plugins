---
name: volume-microstructure-logic
description: Use when designing deterministic algorithms for volume profile mechanics, POC migration, liquidation cascade mapping, session-specific liquidity sweeps, and mathematical validation of expansions using absolute price differentials and ATR volatility thresholds.
---

## The Iron Law

```text
You must formalize all volume and liquidity concepts using explicit programmatic logic—such as N-bar window loops, exact array index inequalities, absolute price differentials, and ATR volatility thresholds—strictly forbidding the use of subjective chart reading, cross-domain physics metaphors, or vague ML/math buzzwords.
```

## Behavioral Rules

- Define structural volume expansions using explicit array comparisons where N-bar breakout volume strictly exceeds the 50-bar Simple Moving Average volume by a defined programmatic multiplier (e.g., `RVOL > 1.5`).
- Categorize 'Push to Fill' volume traps programmatically by triggering a Boolean invalidation state if an N-bar price expansion corresponds with a negative volume array slope over the exact same time-series window.
- Compute Negative POC (Point of Control) Distributions using exact numerical threshold checks where the rolling 24-hour POC migrates a specific absolute price differential below the current array index price.
- Construct Microstructure Liquidation Cascades by mapping Open Interest (OI) density arrays against consecutive funding rate skews, utilizing Boolean gates to trigger margin exhaustion signals at explicit leverage thresholds.
- Format session liquidity boundaries using strict Unix timestamp arrays to fence NY and London macro windows, rejecting any structural sweep validation outside these explicit temporal brackets.
- Calculate institutional displacement proxies utilizing strictly computable mathematical statements: `Daily Return * (Current Bar Volume / 50-bar SMA Volume)`.
- Validate Fair Value Gap (FVG) and structural retention dynamically by binding the zone's active lifespan to an N-bar ATR (Average True Range) volatility threshold computed at the precise array index of formation.
- Demand specific mathematical operations (e.g., arithmetic comparisons, array index offsets) instead of LaTeX-style math formatting to represent actionable code-level directives.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| Validating entries using "kinematic momentum" or "velocity variance" | Contaminates vocabulary with cross-domain physics terminology instead of relying on executable array index logic. |
| Utilizing "Tick-Level RANSAC flat slopes" or "ML-classified confidence" | Replaces practical programming concepts (N-bar window logic, Boolean gates) with over-engineered, uncomputable ML buzzwords. |
| Formatting conditions with `$\ge$` or `$\rightarrow$` notations | Abstracts away explicit Python/MQL code-level directives required for algorithmic implementation. |
| Employing "stateful object-oriented sanitization protocols" for sizing | Masks simple position sizing arithmetic with superficial programming jargon and unactionable filler. |
| Mandating complex Finite State Machines (FSM) for volume calculation | Over-specializes execution architecture into contexts that only require basic arithmetic and array iteration. |

## Quick Reference

| Liquidity Concept | Programmatic Definition |
| :--- | :--- |
| **Negative POC Distribution** | `current_price > (POC_price + absolute_price_offset) AND POC_migrated_down == True` |
| **Volume-Validated Expansion** | `(close[i] - close[i-N]) > (ATR[i] * threshold) AND (volume[i] / SMA_volume) > 1.5` |
| **Liquidation Cascade Proxy** | `OI_density_array[i] > density_threshold AND consecutive_funding_skew >= N_bars` |
| **Volume Trap (Push to Fill)** | `price_slope_array > 0 AND volume_slope_array < 0` |
| **Session Boundary Fence** | `NY_start_timestamp <= current_tick_timestamp <= NY_end_timestamp` |
| **ATR-Scaled Zone Memory** | `max_zone_lifespan_bars = base_bars * (current_ATR / baseline_ATR)` |