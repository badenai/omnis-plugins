---
name: volume-microstructure-logic
description: Use when formalizing limit order book dynamics, order flow imbalance (OFI), volume profile metrics, tick-level execution arrays, or VPIN toxicity into computable mathematical thresholds.
---

## The Iron Law

```text
You must never process volume or order flow as subjective visual clusters, DOM heatmaps, or generic retail volume concepts. All microstructure data must be strictly formalized into Numba-accelerated dynamic arrays, explicit Multi-Level Order Flow Imbalance (MLOFI) computations, and precise statistical metrics (e.g., standard deviation bounds, VPIN) that deterministically control algorithm state machines.
```

## Behavioral Rules

- Define momentum ignition using rigorous tick-level mathematical tests (e.g., Chu-Stinchcombe-White CUSUM) directly on `finmlkit` arrays rather than relying on lagging N-bar swing logic.
- Process limit order book (LOB) depth using Multi-Level Order Flow Imbalance (MLOFI) across L2–L5+ matrices, applying Principal Component Analysis (PCA) to filter spoofing noise from true institutional displacement.
- Calculate anomalous absorption at High Volume Nodes (HVNs) using explicit computational divergences: require volume expansion $\ge 150\%$, flattening Cumulative Volume Delta (CVD), and strict ATR-based price range compression.
- Gate algorithm execution and Finite State Machine (FSM) transitions using computable toxicity metrics, combining Volume-synchronized Probability of Informed Trading (VPIN) and Kyle’s Lambda to quantify exact price impact.
- Implement falsification logic that mathematically compares tick execution velocity against actual LOB depletion arrays to distinguish genuine structural liquidity utilization from wash-trade spoofing.
- Retain concrete array indexing, exact absolute price differentials, and Average True Range (ATR) standard deviation bounds when encoding execution logic, avoiding purely abstract architectural jargon.
- Bind all volume profile tracking to deterministic programmatic arrays, processing historical High Volume Nodes (HVNs) and Point of Control (POC) gaps via strict quantitative mean-reversion anchors and falsification filters.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "Looking for a strong volume climax on the visual DOM heatmap..." | Fails to formalize liquidity; mandates mathematical LOB depletion arrays and exact CUSUM threshold triggers instead of visual heuristics. |
| "Setting a tight Stop-Loss (SL) and Take-Profit (TP) if volume drops..." | Injects forbidden retail trading jargon (SL/TP); requires programmatic Finite State Machine (FSM) risk enclosures and deterministic VPIN gating. |
| "Applying kinematic variance to measure order book pressure..." | Contaminates the model with hallucinated, physics-adjacent jargon instead of utilizing explicit array index inequalities and Boolean logic. |
| "Using a 20-period moving average to gauge volume trend..." | Replaces rigorous market microstructure concepts (like Multi-Level OFI and standard deviation bounds) with lagging, rudimentary retail indicators. |
| "Using an LSTM/KNN machine learning model to predict the next volume node..." | Relies on generic AI/ML black-box models that obscure deterministic market structure and lack strict programmatic invalidation constraints. |
| "Creating a stateful object-oriented liquidity sanitization protocol..." | Replaces precise mathematical operations and Numba-accelerated arrays with superficial programming buzzwords that produce unactionable filler. |

## Quick Reference

| Microstructure Concept | Formalization Strategy | Key Execution Framework |
| :--- | :--- | :--- |
| **Top-of-Book Noise Filtering** | Apply Multi-Level OFI across L2-L5+ arrays using PCA | `finmlkit` Numba-accelerated matrices |
| **Momentum Ignition Detection** | Tick-level Chu-Stinchcombe-White CUSUM testing | High-throughput async tick parsing |
| **Institutional Absorption** | Vol $\ge 150\%$ + CVD flattening + strict ATR containment | Deterministic array index inequalities |
| **Flow Toxicity / Price Impact** | Aggregate VPIN + Kyle's Lambda thresholds | FSM execution halt / scale-down logic |
| **Spoofing / Wash Trade Falsification** | Match tick execution velocity vs actual LOB depletion | Depth-Weighted Order Imbalance arrays |
| **POC Determinism Validation** | Validate historical POC gaps via session-aware filtering | Programmatic mean-reversion logic |