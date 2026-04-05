---
name: structural-formalization
description: Use when requested to translate subjective price action concepts (like Fair Value Gaps, market structure breaks, liquidity sweeps, or order blocks) into executable algorithms, mathematical definitions, programmatic constraints, array inequalities, and objective programmatic trade execution rules.
filePattern: "**/*.py"
---

## The Iron Law

```text
Never generate discretionary visual price action logic, retail concepts, or physics-adjacent jargon. Every structural market concept (e.g., FVG, liquidity sweep, structural break) must be strictly formalized into deterministic, computable logic utilizing exact array index inequalities, absolute price differentials, ATR/Standard Deviation thresholds, Order Flow Imbalance (OFI), and strictly constrained Finite State Machine (FSM) execution cycles.
```

## Behavioral Rules

- Formalize Fair Value Gaps (FVG) deterministically using RANSAC linear regression on tick-level data, strictly requiring R-squared > 0.75, an outlier ratio < 0.15, and absolute slope measured in price-per-second.
- Model multi-timeframe structures using deterministic recursive fractal mapping, targeting exact programmatic coordinates (e.g., 50% Consequent Encroachment) utilizing volume-validated retest arrays.
- Instantiate dynamic structural levels into volatility-scaled memory arrays where the Time-To-Live (TTL) metric is inversely scaled to Average True Range (ATR).
- Define structural containment and breakout thresholds using strictly computable parameters like absolute price differentials, Boolean gates, and direct array index inequalities rather than generic object-oriented jargon.
- Design execution lifecycles exclusively via event-driven Finite State Machines (FSM) to enforce deterministic state closures, mathematically defined position sizing, and error-aware rollbacks.
- Quantify structural market displacement using deterministic statistics like Multi-Level Order-Flow Imbalance (MLOFI) vectors, HVN Volume Z-Scores > 2.0, and standard deviation bounds, bypassing subjective order flow heatmaps entirely.
- Validate structural shifts and liquidity sweeps utilizing mathematical counter-evidence logic (e.g., localized Limit Order Book decay and multi-exchange OI divergence) to distinguish organic institutional absorption from artificial wash-trading spoofing.
- Encode strict invalidation logic into every algorithmic sequence utilizing programmed scale-out logic and Mean Time To Violation (MTTV) metrics to close stale states.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "We can manage the FVG entry using standard SL/TP and 1% risk." | Violates execution mandates by replacing explicit FSM state transitions, mathematical position sizing, and programmatic scale-out logic with brittle retail acronyms and arbitrary heuristics. |
| "The algorithm tracks the kinematic variance of the liquidity sweep." | Contaminates execution logic with irrelevant physics-adjacent terminology; structural breaks must rely on computable array indexing, boolean gates, and strict absolute price differentials. |
| "We will capture the market structure break using an OOP sanitization protocol on an engulfing pattern." | Replaces precise mathematical operations and tick-level standard deviation thresholds with superficial programming jargon and traditional N-bar candlestick rules that lack continuous state reconstruction. |
| "Use an LSTM to forecast the structural baseline state based on the limit order book." | Obscures deterministic market microstructure behind black-box predictive models; AI/ML usage must be strictly constrained to interpretable linear algebra (e.g., PCA) or robust statistical fitting (e.g., RANSAC). |
| "A visual check confirms the footprint chart shows order flow absorption." | Fails to formalize input; visual/manual analysis must be converted into MLOFI matrices, Numba-accelerated footprint arrays, and deterministic Kyle's Lambda calculations. |

## Quick Reference

| Subjective Concept | Formalized Programmatic Implementation | Required Invalidation Metric |
| :--- | :--- | :--- |
| **Fair Value Gaps (FVG)** | Tick-Level RANSAC Linear Regression (R² > 0.75, outlier < 0.15) | ATR-Inversely Scaled Time-To-Live (TTL) memory arrays |
| **Market Structure Break** | Array Index Inequalities & Chu-Stinchcombe-White CUSUM tests | Absolute Price Differential failure / FSM state rollback |
| **Order Block Retest** | Recursive Fractal Mapping at exact 50% Consequent Encroachment | Volume-validated expansion failure / MTTV threshold |
| **Institutional Displacement**| MLOFI Vectors (Depth 5) & Standard Deviation Bounds | LOB array desynchronization / Multi-exchange OI Divergence |
| **Trade Lifecycle** | Event-Driven Finite State Machines (FSM) / Polars matrices | R-Multiple Breakeven state transition closure |