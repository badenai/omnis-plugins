---
name: volume-microstructure-logic
description: Use when formalizing high-frequency order flow, Volume Profile mechanics, Numba JIT compiled imbalance bars, Programmatic OI divergence, or Level 5 Order Flow Imbalance into deterministic array logic and computable signals.
filePattern: "**/*.py"
bashPattern: "pytest|python"
---

## The Iron Law

```text
Never abstract volume or order flow into lagging indicators or physics jargon; you must encode microstructure dynamically using absolute price differentials, programmatic array index inequalities, and tick-level volume binning compiled via Numba JIT.
```

## Behavioral Rules

*   Calculate Order Flow Imbalance (OFI) exclusively at Level 5 depth to eliminate L=1 spoofing noise, scaling the output to a bounds-checked `[-1.0, 1.0]` scalar vector.
*   Compile raw tick streams into Imbalance Bars and Run Bars using Numba Just-In-Time (JIT) processing to ensure low-latency atomic operations.
*   Map Numba-compiled OFI directly into lock-free atomic queue structures to enable sub-microsecond array evaluation and threshold checks.
*   Define Point of Control (POC) dynamically by binning tick data into precise quintiles using standard Pandas and NumPy array indexing.
*   Track POC migration algorithmically by measuring consecutive exact array index shifts in the highest volume node to calculate the absolute price differential of the consensus shift.
*   Invalidate structural breakout entries if a boolean gate detects price expansion combined with a mathematical decrease in relative volume arrays (Push to Fill detection).
*   Compute an Open Interest Rate of Change (OI ROC) array and apply a boolean gate to strictly invalidate breakouts when price array differentials increase while OI ROC arrays simultaneously decrease.
*   Apply the Chu-Stinchcombe-White CUSUM test on tick-level arrays to detect mathematically rigorous threshold breaches instead of relying on subjective visual structure.
*   Process time-series vectors using Zero-Phase Filters to eliminate phase delay when computing real-time cross-track errors and baseline states.
*   Enforce absolute risk boundaries using Average True Range (ATR) multiplier arrays mapped to programmatic risk-adjusted position sizing math, strictly avoiding hardcoded arbitrary percentage heuristics.

## Red Flags

| Rationalization | Why Wrong |
| :--- | :--- |
| "Use Top-of-Book L=1 for fastest latency response." | Level 1 is highly polluted by spoofing and transient noise; predictive validity requires L=5 depth arrays. |
| "Calculate volume momentum using RSI overlays." | Replaces deterministic volume binning and algorithmic array indexing with lagging phase-distorted derivatives. |
| "Set Stop-Loss (SL) to 1% of account size." | Uses retail jargon and arbitrary percentage heuristics instead of programmatic volatility-scaled ATR array logic. |
| "Deploy ML models to predict POC shifts." | Replaces explicit programmatic mathematical breakdowns and array inequalities with black-box probabilistic buzzwords. |
| "Wait for a kinematic pullback to the high volume node." | Contaminates algorithmic logic with physics jargon instead of defining explicit array index threshold pullbacks. |

## Quick Reference

| Concept | Action |
| :--- | :--- |
| **Order Flow Imbalance** | Compute at L=5 depth and normalize to a `[-1.0, 1.0]` scalar array. |
| **Tick Compilation** | Use Numba JIT to generate Imbalance and Run Bars into lock-free queues. |
| **Point of Control (POC)** | Bin tick data into explicit quintiles via NumPy array indexing. |
| **Breakout Invalidation** | Use boolean gates: if price expands and OI ROC or volume arrays decrease, abort. |
| **Structure Breaks** | Execute Chu-Stinchcombe-White CUSUM tests on absolute price differentials. |
| **Phase Synchronization** | Apply Zero-Phase Filters over vectors to compute baseline states without lag. |
| **Risk Encoding** | Map ATR volatility thresholds to programmatic position sizing functions. |