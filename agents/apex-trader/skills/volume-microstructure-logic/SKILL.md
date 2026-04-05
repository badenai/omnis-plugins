---
name: microstructure-lob-analytics
description: Use when engineering Limit Order Book (LOB) features, Multi-Level Order-Flow Imbalance (MLOFI), Numba-accelerated footprint extraction, programmatic order flow heatmaps, or translating tick-level liquidity into deterministic mathematical arrays.
filePattern: "**/*.py"
bashPattern: "numba|finmlkit|hftbacktest"
---

## The Iron Law

```text
You must strictly translate all order flow and Limit Order Book (LOB) liquidity dynamics into deterministic, N-dimensional mathematical arrays and computable numerical thresholds. Never use subjective tape-reading logic, visual heatmap heuristics, lagging retail indicators, or physics-adjacent buzzwords; all microstructure features must be explicitly constructed using exact array index inequalities, standard deviation limits, Multi-Level Order-Flow Imbalance (MLOFI) formulas, and programmatic volumetric aggregations tightly bound to concrete execution logic.
```

## Behavioral Rules

*   Compute Limit Order Book depth by constructing Multi-Level Order-Flow Imbalance (MLOFI) across minimum 5-level arrays rather than relying on static top-of-book volume.
*   Accelerate footprint extraction and volumetric calculations (e.g., High/Low Volume Node absorption) strictly using Numba Just-In-Time (JIT) routines and continuous internal array reconstruction.
*   Define institutional displacement and flow toxicity mathematically by implementing precise thresholds for Volume-Synchronized Probability of Informed Trading (VPIN) and Kyle's Lambda (market impact per unit traded).
*   Process asynchronous tick-level execution data using high-throughput vectorized operations (e.g., explicit ASOF JOIN commands) to synchronize multi-dimensional L2/L3 order book snapshots without look-ahead bias.
*   Bind all microstructure signal arrays directly to deterministic execution logic using concrete arithmetic price differentials, boolean gates, and Average True Range (ATR) standard deviation boundaries.
*   Enforce structural trade lifecycle closures explicitly via dynamic R-multiple scale-out arrays and ATR-based invalidation logic, explicitly rejecting all arbitrary percentage-based heuristics or manual retail targets.
*   Filter spoofing and artificial order flow spikes by computing programmatic multi-exchange Open Interest (OI) divergence and measuring localized LOB array decay.
*   Identify structural baseline shifts mathematically by measuring Cumulative Volume Delta (CVD) divergence against Numba-accelerated order flow imbalance thresholds.
*   Determine market regime states by computing Gamma Exposure (GEX) binary state flags combined with Volatility-of-Volatility (VoV) Z-Score bounds (> +1.5σ) before instantiating algorithmic triggers.

## Red Flags

| Domain-Specific Rationalization | Why It Violates Algorithmic Parity |
| :--- | :--- |
| Using terms like "kinematic variance" or "RANSAC flat slopes" | Physics-adjacent jargon and ML buzzwords obscure the standard programmatic array indexing and boolean gates required for deterministic code. |
| Formatting instructions with LaTeX math (e.g., `\le`, `\rightarrow`) | Replaces exact code-level operator syntax (`<=`, `->`) needed for executable, compilable risk constraints and variable assignment. |
| Using "Stop-Loss (SL)" or "Take-Profit (TP)" concepts | Retail jargon replaces the required programmable mathematical breakeven states and strict R-multiple array invalidation metrics. |
| Substituting exact math with "stateful object-oriented wrappers" | Superficial programming buzzwords destroy the concrete mathematical linear algebra required for vectorizing L2/L3 order book depth snapshots. |
| Filtering momentum with MACD, RSI, or standard moving averages | Relies on fundamentally flawed, phase-delayed lagging logic instead of Zero-Phase Filtered (ZPF) raw tick/volume arrays. |
| Hardcoding fixed risk boundaries like "0.1% to 1.0% risk" | Brittle retail heuristics override the required dynamically computed, ATR-scaled position sizing and structural volatility thresholding. |
| Over-abstracting logic solely into Finite State Machine (FSM) states | Decouples signal generation from execution; algorithms must explicitly detail the raw arithmetic arrays and index inequalities driving the state change. |

## Quick Reference

| Microstructure Concept | Deterministic Implementation Array / Metric |
| :--- | :--- |
| **LOB Depth Analytics** | Multi-Level Order-Flow Imbalance (MLOFI) 5-level vectors |
| **Flow Toxicity Measurement** | Volume-Synchronized Probability of Informed Trading (VPIN) |
| **Market Resilience/Impact** | Deterministic formulas of Kyle's Lambda |
| **Volumetric Feature Processing** | Numba-Accelerated JIT footprint parsing and continuous state arrays |
| **Regime Outlier Suppression** | Volatility-of-Volatility (VoV) Z-Scoring bound rules |
| **Structural Breakdown Modeling** | Chu-Stinchcombe-White CUSUM tests |
| **Data Pipeline Synchronization** | ASOF JOIN vectorized operations for tick/book alignment |
| **Signal/Execution Smoothing** | Zero-Phase Filters (ZPF) applied across dual-directional raw arrays |
| **Risk Containment** | Volatility-Scaled Average True Range (ATR) limit indexing |