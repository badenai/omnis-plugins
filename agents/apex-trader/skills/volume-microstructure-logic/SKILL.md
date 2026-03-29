---
name: volume-microstructure-logic
description: Use when formalizing Order Flow Imbalance (OFI), tick-level microstructure, volume profile mechanics, and deterministic liquidity execution.
---

## The Iron Law

```text
Never use subjective price action descriptions or basic retail indicators. You must define all volume and microstructure events using explicit array index inequalities, absolute price differentials, Standard Deviation bounds, or ATR volatility thresholds to enforce strict programmable execution.
```

## Behavioral Rules

*   Compute tick-level Order Flow Imbalance (OFI) and Level-2 depth regression arrays natively using `finmlkit` and Numba JIT compilation to guarantee sub-millisecond calculation speeds.
*   Replace static temporal or standard volume bars with dynamic Quantile bars triggered strictly by EWMA volatility thresholding.
*   Define Highest Volume Node (HVN) absorption deterministically: require extreme negative Cumulative Volume Delta (CVD) at a strict spatial boundary (±0.5% of the HVN) combined with zero downward absolute price translation.
*   Calculate the degree of a Fair Value Gap (FVG) by extracting the absolute slope (|β1|) from a Tick-Level RANSAC Regression fitted to the execution data.
*   Enforce a programmatic formation time threshold of ≥120 seconds before logging an FVG into the memory array.
*   Generate dynamic upper and lower containment arrays for structural gap memory using exact ATR multipliers to filter out low-volatility structural noise.
*   Filter non-representative volume spikes by enforcing strict temporal session awareness bounds when mapping ES Futures Point of Control (POC) gaps.
*   Manage trade validation and position states using deterministic boolean gates and continuous out-of-sample R-multiple breakeven mathematical matrices.
*   Use `HftBacktest` to model sub-millisecond execution, strictly accounting for queue position, feed latency, and GLFT market-making deterministic states.
*   Define momentum and structural baseline states exclusively via Volatility-of-Volatility (VoV) Z-Scoring and Gamma Exposure (GEX) programmatic thresholds.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "Implement a Stop-Loss (SL) and Take-Profit (TP) capping risk at 1%." | Uses brittle retail jargon and arbitrary heuristics instead of deterministic R-multiple matrices, array-bounded invalidation, and programmatic structural limits. |
| "Detect kinematic price exhaustion at the resistance boundary." | Contaminates code with meaningless physics jargon; replace with exact programmatic standard deviation bounds and explicit array indexing. |
| "Initiate stateful object-oriented array sanitization for the block." | Employs superficial OOP filler; use explicit mathematical computations, absolute price differentials, and boolean gates. |
| "Execute entry on the N-bar moving average swing crossover." | Substitutes quantifiable microstructure mechanics with lagging retail math; mandate Order Flow Imbalance (OFI) or Level-2 depth regression instead. |
| "Apply bidirectional Zero-Phase Filters for live trade execution." | Introduces mathematical lookahead bias and violates the rigid latency/causality boundaries required for real-time live event loops. |

## Quick Reference

| Concept | Deterministic Implementation |
| :--- | :--- |
| **High-Frequency Simulation** | `HftBacktest` with strict queue position and latency accounting |
| **Microstructure Pipeline** | Numba JIT + `finmlkit` for sub-millisecond OFI array generation |
| **Dynamic Data Aggregation** | EWMA-thresholded Quantile bars (discarding static OHLCV) |
| **HVN Absorption Trigger** | Extreme CVD + ±0.5% HVN spatial boundary + zero price translation |
| **FVG Structural Validation** | Tick-Level RANSAC Regression slope (\|β1\|) + ≥120s formation time |
| **Regime State Classifier** | VoV Z-Score bounds paired with GEX mean-reversion gating |
| **Dynamic Array Containment** | ATR-multiplied bounds applied directly to limit order mapping |