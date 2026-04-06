---
name: volume-microstructure-logic
description: Use when formalizing order flow, Limit Order Book (LOB) dynamics, Volume Profiles, and microstructure execution data into n-dimensional arrays and deterministic backtest-ready code.
filePattern: "**/*.py"
---

## The Iron Law

```text
You must strictly translate all discretionary Limit Order Book (LOB) visualizations, volume profiles, and order flow concepts into deterministic mathematical thresholds utilizing n-dimensional arrays, precise array index inequalities, and Boolean gates. Visual or intuition-based microstructure interpretation is strictly forbidden; you must rely exclusively on Numba-accelerated Order Flow Imbalance (OFI), explicit standard deviation bounds, and exact absolute price differentials for execution and signal generation.
```

## Behavioral Rules

*   If calculating market liquidity resilience, natively compute Kyle's Lambda to deterministically track the exact price impact per traded volume across LOB depth arrays.
*   When profiling volume distributions, apply session-aware volume filters and strictly calculate Z-scored Volume Profiles to penalize idiosyncratic spikes and identify Highest Volume Node (HVN) absorption.
*   If engineering features for institutional displacement, apply explicit standard deviation bounds to LOB depth regressions and calculate Volume-Synchronized Probability of Informed Trading (VPIN) rather than utilizing standard retail N-bar swing logic.
*   When extracting features from Limit Order Books, extract Multi-Level Order-Flow Imbalance (MLOFI) by applying 1D spatial convolutions across specific depth thresholds (e.g., Depth 5) to map n-dimensional liquidity density.
*   If constructing volume-validated execution pipelines, bypass Pandas entirely and utilize Numba JIT compilation (`@njit`) to process Order Flow Imbalance (OFI) and structural breaks directly from raw memory arrays.
*   When defining forced-closure liquidation sweeps, demand localized structural confirmation triggers (e.g., Volume Z-Score > +1.5σ and Boolean state inversions based on absolute price differentials) independent of the sweep to algorithmically bypass institutional spoofing layers.
*   If defining risk models and positional exposure within microstructure engines, enforce R-multiple breakeven state definitions, Average True Range (ATR) scaled array limits, and strict Finite State Machine (FSM) state transitions rather than utilizing standard stop-losses or arbitrary retail heuristics.
*   When measuring Point of Control (POC) mechanics, strictly map POC Gap Determinism against an array of session boundaries to trigger mean-reversion or structural retention state changes.
*   If smoothing high-frequency signal data, apply Zero-Phase Filter (ZPF) architectures across continuous time-series arrays to eliminate lagging phase delays inherent in standard moving averages.

## Red Flags

| Rationalization | Why it violates Apex Trader constraints |
| :--- | :--- |
| "Using a visual heatmap GUI to identify order block resistance." | Fails the Iron Law; visual heatmaps must be mathematically translated into spatial-temporal density matrices and Depth-Weighted Order Imbalance arrays. |
| "Setting risk at 1% with an SL/TP ratio of 1:3." | Contaminates the codebase with retail jargon and arbitrary heuristics; requires closed-loop FSM trade lifecycle management and programmatic scale-out math utilizing ATR and R-multiples. |
| "Applying an EMA crossover or RSI to confirm order flow momentum." | Utilizes lagging retail technical indicators; all momentum metrics must be derived exclusively from Order Flow Imbalance (OFI), VoV, or empirical microstructure execution data. |
| "Validating volume spikes utilizing kinematic momentum." | Employs forbidden physics-adjacent jargon; logic must rely on programmatic data structures like array indexing, Boolean gates, and Z-scored thresholds. |
| "Utilizing stateful object-oriented arrays to handle LOB updates." | Masks simple computational requirements with superficial programming buzzwords; LOB data demands strict vectorized Numba-accelerated raw memory management. |

## Quick Reference

| Action | Microstructure Component | Programmatic Formalization Method |
| :--- | :--- | :--- |
| **Quantify Flow Toxicity** | VPIN & Kyle's Lambda | Deterministic n-dimensional calculation of price impact per traded volume. |
| **Measure LOB Imbalance** | MLOFI Vectorization | 1D spatial convolutions and dynamic array processing across specific L2 depths. |
| **Track Equilibrium Shifts** | Z-Scored Volume Profile | Session-aware POC gap determinism relying on precise time-series array inequalities. |
| **Process High-Freq Ticks** | Numba-Accelerated Pipelines | JIT compiled raw memory arrays for Order Flow Imbalance (OFI) processing. |
| **Manage Microstructure Risk** | Finite State Machines (FSM) | Strict transition gates driven by ATR thresholds, R-multiples, and absolute price differentials. |