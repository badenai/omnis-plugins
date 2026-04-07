---
name: volume-microstructure-logic
description: Use when building, reviewing, or optimizing quantitative algorithms that ingest tick-level data, compute Order Flow Imbalance (OFI), process Limit Order Book (LOB) arrays, model institutional displacement via volume-synchronized probability of informed trading (VPIN), or reconstruct multi-level liquidity utilizing Numba-accelerated Python wrappers.
filePattern: "**/*.py"
---

## The Iron Law

```text
You must strictly translate all order flow and limit order book dynamics into deterministic, computable array index inequalities, boolean gates, and standard deviation bounds; never default to basic N-bar swing logic or subjective LOB heatmap visualizations.
```

## Behavioral Rules

- Implement Multi-Level Order Flow Imbalance (MLOFI) vectorization by extracting tick-level order imbalance depth using n-dimensional arrays to mathematically capture liquidity addition and cancellation velocity.
- Compute institutional displacement by calculating Volume-Synchronized Probability of Informed Trading (VPIN) and use deterministic implementations of Kyle's Lambda to continuously measure market impact per traded volume.
- Bypass Python serialization bottlenecks by utilizing Numba JIT-compiled algorithms with strict `Decimal` types to construct deterministic spatial-temporal density arrays and Order Flow Imbalances (OFI) without floating-point errors.
- Govern all asynchronous trade lifecycles using rigid Finite State Machines (FSMs) that evaluate programmatic risk constraints, mathematical position sizing, and R-multiple breakeven states to ensure zero logic drift.
- Define market structure containment and imbalance using explicit absolute price differentials, exact array indexing, and Average True Range (ATR) thresholds rather than generic machine learning buzzwords or subjective visual patterns.
- Apply deterministic wash-volume filtration models against all Limit Order Book activity using statistical Z-scoring to mathematically separate genuine limit liquidity from manipulative spoofing.
- Reject raw, non-stationary LOB data inputs; always enforce strict differencing, Z-scoring, or Principal Component Analysis (PCA) dimensionality reduction before array processing.

## Red Flags

| Rationalization | Why Wrong |
| :--- | :--- |
| "The execution threshold requires a Stop-Loss (SL) of 0.5%." | Uses brittle retail jargon and arbitrary heuristics instead of programmatic R-multiple breakeven states and mathematical position sizing models. |
| "The kinematic momentum of the order flow validates the liquidity sweep." | Introduces meaningless physics-adjacent jargon instead of explicit programmatic logic like array index inequalities and standard deviation bounds. |
| "Feed the raw LOB data directly into a generic LSTM to predict price direction." | Violates the mandate against generic black-box predictive models and fails to apply strict differencing or Z-scoring to non-stationary raw LOB data. |
| "Manage the stateful object-oriented LOB arrays to dynamically track liquidity." | Replaces precise mathematical operations and algorithmic array management with generic object-oriented buzzwords, creating imprecise filler. |
| "Use a 3-bar engulfing pattern to confirm the order block displacement." | Relies solely on OHLC parameters without tick-level volume validation or standard deviation bounds for institutional displacement. |

## Quick Reference

| Microstructure Concept | Programmatic Implementation |
| :--- | :--- |
| **Institutional Displacement** | Volume-Synchronized Probability of Informed Trading (VPIN) arrays |
| **Market Friction & Impact** | Deterministic implementations of Kyle's Lambda |
| **Multi-Depth LOB Liquidity** | Vectorized Multi-Level Order Flow Imbalance (MLOFI) depth arrays |
| **Microstructure Processing** | Numba JIT-compiled functions utilizing strict `Decimal` operations |
| **Trade Lifecycle Execution** | Rigid Finite State Machines (FSMs) evaluating R-multiple states |
| **Volatility Context** | Average True Range (ATR) thresholds and VoV Z-scoring |