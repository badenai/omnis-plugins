---
name: structural-formalization
description: Use when formalizing subjective price action, volume profiles, liquidations, and market structure into deterministic code, array logic, and execution state machines.
---

## The Iron Law

```text
You must translate subjective market structure into computable boolean gates, exact array index inequalities, absolute price differentials, and programmatic risk constraints; never output descriptive chart logic, over-engineered statistical buzzwords, or abstract architectural frameworks without their explicit, executable mathematical equations and execution functions.
```

## Behavioral Rules

- Define Fair Value Gaps (FVGs) and Order Blocks exclusively through array index inequalities, N-bar window logic, and absolute price differentials.
- Scale structural zone memory dynamically by computing the exact True Range (ATR) threshold at the specific time of the formation.
- Calculate structural boundaries and liquidity sweeps using explicit mathematical thresholds and multi-timeframe pivot arrays rather than subjective support/resistance zones.
- Formalize institutional orderflow proxies into computable features using strict mathematical operators (e.g., `Daily_Return * (Current_Volume / 50-day_SMA_Volume)`) and enforce a boolean gate of `RVOL > 1.5` for validation.
- Govern breakout signal generation by computing absolute volume disparities, requiring strictly increasing volume for breakouts and programmatically tagging decreasing volume expansions as traps.
- Detect Microstructure Liquidation Cascades by executing array multiplications of aggregated Open Interest (OI) density against persistently skewed funding rates.
- Trigger a bearish regime algorithmically when a Negative POC Distribution occurs, defined strictly as POC migration settling >20% below current price while price remains under the AVWAP.
- Format multi-timeframe structures recursively, enforcing a higher-timeframe condition as a rigid boolean filter for any lower-timeframe execution trigger.
- Encode trade lifecycles strictly as Finite State Machines (FSM) with mathematically closed state spaces, embedding error-aware rollback logic for asynchronous exchange API drops.
- Implement explicit programmatic risk constraints directly alongside execution logic, hardcoding risk between 0.1% and 1.0% per trade.
- Enforce a minimum mathematically defined 1:3 Risk-to-Reward ratio using internal liquidity markers (e.g., Consequent Encroachment calculations) as target constraints.
- Process time-series data both forward and backward using Zero-Phase Filters (ZPF) via basic array management to establish zero-lag structural baselines.
- Execute a midpoint scaling algorithm starting exactly at the 0.5 range retracement, proportionally increasing position sizing as absolute price approaches the hard-stop array boundary.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "Utilize K-Nearest Neighbors or Tick-Level RANSAC flat slopes to model structural equilibrium." | Replaces fundamental programming concepts (array indices, boolean gates, N-bar windows) with over-engineered ML buzzwords that reduce algorithmic determinism. |
| "The entry is validated by a structural push $\ge$ the previous swing." | Uses LaTeX-style math formatting (`$\ge$`) inside instructions, which abstracts away explicit code-level array management and variable logic. |
| "Observe the kinematic variance and volume velocity of the liquidity sweep." | Contaminates the model with physics-adjacent jargon, producing meaningless, unactionable filler instead of pure quantitative logic. |
| "The system utilizes stateful object-oriented proxy classes to manage execution gracefully." | Replaces precise mathematical operations and asynchronous lifecycle rollbacks with generic object-oriented buzzwords. |
| "Only use the FSM architecture to abstract the trade states." | Over-specializes into pure state management, deleting the critical absolute price differentials and ATR volatility thresholds required for signal generation. |

## Quick Reference

| Concept | Computable Formalization |
| :--- | :--- |
| **Fair Value Gap (FVG)** | 3-bar absolute price differential + ATR-scaled dynamic memory threshold |
| **Liquidation Cascade** | Aggregate OI density array `*` sustained funding rate skew coefficient |
| **Orderflow Displacement** | `[Daily_Return * (Current_Volume / SMA_Volume_50)] && RVOL > 1.5` |
| **Negative Distribution** | `(POC_Current < POC_Prev * 0.8) && (Price < AVWAP)` |
| **Risk Enforcement** | `0.001 <= risk_per_trade <= 0.01` && `target_dist >= (3 * stop_dist)` |
| **Fractal Alignment** | HTF Pivot Array State `== TRUE` strictly gates LTF CHoCH execution |
| **FSM Trade Lifecycle** | Rigid state closures (Entry -> Partial -> Trail) with API drop rollbacks |