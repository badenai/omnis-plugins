---
name: volume-microstructure-logic
description: Use when building deterministic volume profile matrices, order book microstructure logic, POC migration tracking, HVN absorption algorithms, and Depth 5 Order Flow Imbalance (OFI) processing.
filePattern: "**/*.py"
---
## The Iron Law

```text
You must formalize Volume Profile and Order Book Microstructure exclusively through strict programmatic data structures: exact array index inequalities, Boolean logic gates, absolute price differentials, and N-bar window logic. Never abstract volume or depth mechanics into visual charting concepts, physics-adjacent jargon, generic object-oriented buzzwords, or retail acronyms (e.g., SL/TP). Every volume node, point of control, and order flow imbalance must be evaluated as a mathematically computable array.
```

## Behavioral Rules

*   When identifying High-Volume Nodes (HVNs), strictly bin tick data into quintiles using NumPy and classify the 80th percentile as the executable HVN threshold array.
*   Compute Point of Control (POC) migration as a deterministic absolute velocity array (e.g., `df['poc_distance_pct']`) to trigger mathematically rigorous mean-reversion targets via POC Gap Determinism logic.
*   When calculating Order Flow Imbalance (OFI), strictly process the data at Depth 5 (L=5) of the order book to generate a non-lagging probabilistic scalar.
*   Discard Top-of-Book (L=1) order flow data unconditionally as spoofing noise; never utilize L1 for institutional displacement algorithms.
*   Confirm institutional displacement intent at breakout vectors by computing the deterministic proxy scalar: `Daily Return * (Current Volume / 50-day SMA Volume)`.
*   Utilize Numba Just-In-Time (JIT) compilation to bypass standard Python latency when structuring high-frequency tick data arrays and processing absolute volume matrices.
*   Govern risk on volume-validated signals by mapping explicit R-multiple matrices, ATR volatility thresholds, and strict array-driven scale-out logic instead of hardcoding arbitrary percentage heuristics or retail stop mechanisms.
*   Strip out all physics-adjacent terminology when describing volume dynamics; represent structural expansions explicitly through array indices and absolute numerical differentials.
*   Define intraday volume execution regimes exclusively via Gamma Exposure (GEX) binary state flags, ensuring state changes are governed by precise mathematical boundaries, not qualitative descriptions.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "Using Top-of-Book volume to measure order flow pressure." | Top-of-Book (L=1) is spoofing noise; OFI must be computed strictly at Depth 5 (L=5) to form a valid, non-lagging probabilistic scalar. |
| "The POC migrated rapidly, demonstrating high kinematic momentum." | Violates anti-patterns by using physics-adjacent jargon; POC migration must be defined strictly via a computable numeric array (e.g., `poc_distance_pct`). |
| "Setting a trade with a 1% SL and 3% TP for the HVN bounce." | Violates the Iron Law by injecting retail jargon and arbitrary heuristics instead of enforcing programmable mathematical R-matrices and array-based risk states. |
| "Finding the volume value area by abstracting a stateful object-oriented data array." | Utilizes empty programming buzzwords instead of defining the explicit NumPy quintile binning and 80th-percentile HVN logic required for deterministic code. |
| "Using K-Nearest Neighbors to predict POC target zones." | Violates quantitative constraints by substituting exact mathematical array structural processing with contradictory machine-learning classifiers lacking walk-forward logic. |

## Quick Reference

| Concept | Implementation Standard | Rejection Criteria |
| :--- | :--- | :--- |
| **HVN Classification** | NumPy quintile binning; exact 80th percentile boolean threshold. | Visual "value area" charting or subjective bounds. |
| **OFI Depth Execution** | Process strictly at Depth 5 (L=5) for probabilistic scalar generation. | Relying on Top-of-Book (L=1) or aggregate level limits. |
| **POC Migration** | Tracking via absolute computed arrays (`df['poc_distance_pct']`). | Visual tracking or "kinematic" buzzwords. |
| **Institutional Proxy** | Compute scalar: `Daily Rtn * (Cur Vol / 50-day SMA Vol)`. | Discretionary high-volume bar reading. |
| **Microstructure Speed** | Numba JIT compilation applied directly to raw tick data feeds. | Standard Pandas DataFrame operations for HFT. |
| **Risk Encoding** | ATR-based thresholds and exact array index scale-out matrices. | Hardcoded percentages, SL/TP retail acronyms. |