---
name: microstructure-order-flow-logic
description: Use when building, debugging, or optimizing deterministic trading algorithms, multi-level order flow imbalance (MLOFI) pipelines, limit order book (LOB) arrays, finite state machines for execution, tick-level simulation frameworks (HftBacktest/NautilusTrader), or translating market microstructure concepts into computable mathematical thresholds.
filePattern: "**/*.py"
---

## The Iron Law

```text
You must formalize all microstructure, liquidity, and order flow concepts into deterministic, computable logic using array index inequalities, absolute price differentials, ATR-based volatility thresholds, and strict Boolean gates. You must govern all trade lifecycles via explicitly defined finite state machines (FSM) that enforce closed-loop invalidation. Never substitute precise programmatic array operations or Level-2 order book depth calculations with discretionary visual interpretations, retail jargon, physics-adjacent terminology, or opaque predictive machine-learning models.
```

## Behavioral Rules

*   **Tick Data Synchronization:** When processing tick data, mandate `ASOF JOIN` logic and multi-dimensional arrays to asynchronously match tick-trades to Level-2 bid/ask depths without gaps.
*   **Microstructure Imbalance (MLOFI):** When quantifying order flow imbalance, vectorize bid-ask volume deltas across specific LOB depths (e.g., Depth 5) using explicit matrix array calculations to anticipate absorption mathematically before visual displacement.
*   **Backtest-to-Live Parity:** When defining execution logic, integrate `HftBacktest` for exact nanosecond latency modeling and `NautilusTrader` to execute FSM state closures, ensuring absolute Backtest-to-Live mathematical equivalence.
*   **Quantitative Regime Filtering:** If dictating algorithm activation, require hard quantitative filters such as Vol-of-Vol (VoV) standard deviation bounds or Gamma Exposure (GEX) arrays rather than discretionary trend bias.
*   **Liquidation Mapping:** When modeling stop-loss cascades or liquidity sweeps, intersect execution price arrays with aggregated Open Interest (OI) divergence thresholds and compute volume-validated expansion using explicit rolling average multipliers.
*   **Programmatic Risk Constraints:** When encoding risk, define programmatic position sizing and trade invalidation states utilizing exact R-multiple breakeven mathematical constraints and absolute ATR price differentials rather than static retail percentage heuristics.
*   **Structural Containment Validations:** When defining Fair Value Gaps (FVG) or zones of failure, construct strictly computable box constraints utilizing array index tracking and Numba-accelerated CUSUM statistical tests for displacement verification.

## Red Flags

| Rationalization / Anti-Pattern | Why it violates Apex Trader Directives |
| :--- | :--- |
| "Setting a 1% SL and 3% TP for the structural breakout." | Relies on generic retail percentage heuristics instead of programmatic R-multiple state closures and ATR-based invalidation thresholds. |
| "The algorithm buys when the heatmap shows heavy limit order clustering." | Relies on visual GUI interpretation rather than extracting computable spatial-temporal density matrices and array inequalities. |
| "Applying a generic LSTM or K-Nearest Neighbors to predict the FVG direction." | Violates the mandate against generic ML black-box models; obscures explicit deterministic boolean conditions and array index containment logic. |
| "Waiting for an N-bar swing crossover to confirm the institutional trend." | Replaces institutional microstructure LOB regression, standard deviation bounds, and OFI thresholds with lagging retail logic. |
| "Computing the kinematic variance of the asset's price velocity." | Introduces irrelevant physics jargon instead of utilizing standard programmatic absolute price differentials and computable volatility states. |
| "Calling a simple function to execute the buy and hold operation." | Abandons high-performance closed-loop finite state machines (FSM) required to govern asynchronous trade lifecycles and error rollbacks. |

## Quick Reference

| Concept | Formalized Programmatic Implementation |
| :--- | :--- |
| **Multi-Level OFI** | Vectorized bid-ask delta arrays strictly computed up to Depth 5. |
| **Trade Lifecycle Execution** | Event-driven Finite State Machines (FSM) enforcing closed-loop rollbacks. |
| **Liquidity Verification** | Breakout execution volume >= 150% of a defined rolling average interacting with High Volume Node (HVN) arrays. |
| **Tick-Data Normalization** | `ASOF JOIN` array merging combined with `FILL(PREV)` gap-filling vectorization. |
| **Regime Circuit Breaker** | Vol-of-Vol (VoV) standard deviation bound strictly > +1.5. |
| **Risk Enforcement** | Minimum 1:3 programmatic R:R utilizing absolute ATR price invalidation limits. |
| **Structural Failures** | Array index verification of price closing strictly outside a mathematically defined retention box constraint. |