---
name: quantitative-regime-filtering
description: Use when architecting logic for algorithmically dictating trading system activation, parameter switching, and trade lifecycle constraints using explicit metrics like GEX, VoV Z-Scoring, and TSMOM.
---

## The Iron Law

```text
Never hardcode static strategy parameters; you must explicitly define regime-filtering Boolean gates, Average True Range (ATR) thresholds, and array index inequalities driven by Gamma Exposure (GEX), Vol-of-Vol (VoV) Z-Scoring, and Time-Series Momentum (TSMOM) to algorithmically dictate system activation, parameter switching, and exposure compression.
```

## Behavioral Rules

*   If Gamma Exposure (GEX) is mathematically positive, set Boolean gates to route execution arrays to mean-reversion logic.
*   If Gamma Exposure (GEX) is low or negative, toggle execution states to activate breakout logic algorithms.
*   Program a hard-coded circuit breaker to instantly halt all trade lifecycle Finite State Machines (FSMs) if the Vol-of-Vol (VoV) Z-Score strictly exceeds a +1.5 threshold.
*   Update Time-Series Momentum (TSMOM) parameters exclusively at the end-of-day temporal boundary to prevent tick-level execution loop latency from API calls or intensive recalibrations.
*   If asset correlation elasticity breaches its pre-calculated historical baseline array, proportionally compress risk-per-trade limits across the entire portfolio exposure matrix.
*   Implement Automated Pause Gates (The Kitchen Loop) using explicit structural boundary arrays to detect Out-of-Distribution (OOD) regime drift prior to hitting lagging equity curve drawdowns.
*   Define specific absolute price differentials and Average True Range (ATR) volatility thresholds when calculating deterministic regime boundaries.
*   Extract quantitative regime baseline states using specific programmatic math (e.g., standard deviation bounds, array index inequalities) rather than utilizing generic machine learning classifiers or visual heuristics.
*   Reserve Finite State Machines (FSM) strictly for asynchronous trade lifecycle management and execution state handling; use basic computational arithmetic and array indexing for simple indicator or Z-score calculations.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "I will use a standard Take-Profit (TP) and Stop-Loss (SL) to handle regime shifts." | Violates deterministic state closure mandates; relies on retail jargon instead of programmatic risk encoding, state transitions, and volatility-scaled structural invalidation. |
| "The strategy reduces position size to 0.5% during high volatility." | Hardcodes arbitrary retail percentage heuristics instead of enforcing dynamic, mathematically defined exposure compression based on Correlation Elasticity and VoV Z-scores. |
| "I will apply a generic Deep Learning LSTM to predict the market regime." | Obscures deterministic market structure and lacks strict programmatic invalidation constraints; regime filters must use explicit computable logic like GEX thresholds and array index inequalities. |
| "I added an FSM to calculate the Vol-of-Vol Z-score." | Over-engineers simple arithmetic; Finite State Machines must govern complex, multi-stage trade lifecycles and asynchronous order routing, not basic variable calculation. |
| "I will calculate kinematic variance to validate the breakout regime." | Contaminates the codebase with irrelevant physics jargon instead of using concrete microstructure metrics like Order Flow Imbalance (OFI), ATR boundaries, and Absolute Price Differentials. |
| "Calculate the regime $\ge$ $1.5\sigma$ utilizing object-oriented stateful arrays." | Utilizes forbidden LaTeX formatting and abstract generic programming buzzwords instead of explicit code-level directives and simple exact mathematical operators. |

## Quick Reference

| Regime Metric | Deterministic Condition | Programmatic Action |
| :--- | :--- | :--- |
| **Gamma Exposure (GEX)** | Positive | Activate mean-reversion logic arrays |
| **Gamma Exposure (GEX)** | Low / Negative | Toggle Boolean gates for breakout logic |
| **Vol-of-Vol (VoV) Z-Score** | > +1.5 | Halt FSM execution (Circuit Breaker) |
| **TSMOM** | End-of-Day Boundary | Recalculate and update system parameters |
| **Correlation Elasticity** | > Historical Baseline | Compress portfolio risk arrays proportionally |
| **OOD Drift Control** | Structural Boundary Breach | Trigger Automated Pause Gates |