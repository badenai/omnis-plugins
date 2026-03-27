---
name: execution-architecture-fsm
description: Use when designing or debugging high-frequency algorithmic trade execution, event-driven backtesting, Finite State Machine (FSM) trade lifecycles, Numba/Rust-compiled microstructure queue simulations, and programmatic order flow state logic.
filePattern: "**/*.py"
---

## The Iron Law

```text
You must design all trade execution lifecycles as mathematically closed Finite State Machines (FSM) utilizing explicit computational structures—such as array index inequalities, absolute price differentials, and ATR-scaled volatility thresholds—to govern every state transition, entry, and scale-out event without relying on abstract machine learning buzzwords or subjective retail heuristics.
```

## Behavioral Rules

*   **State Machine Execution:** If designing an order execution system, implement a closed-loop Finite State Machine (e.g., utilizing NautilusTrader architectures) where every pending, filled, partial, dropped, or cascading event maps to an explicit transition with error-aware rollback logic.
*   **Computational Structure Gating:** Govern all FSM breakout and entry states using strict programmatic logic, incorporating explicit array index inequalities (e.g., `np.where`), absolute price differentials, and N-period rolling thresholds.
*   **Volatility-Scaled Boundaries:** Constrain system states by dynamically scaling validation boundaries using Average True Range (ATR) threshold multipliers, ensuring state transitions (e.g., bullish to bearish control) execute instantly upon absolute mathematical breach of the ATR-scaled array.
*   **Microstructure Imbalance:** Calculate Order Flow Imbalance (OFI) regression strictly at a book depth of 5 levels (L=5) to compute deterministic state-change triggers, aggressively discarding top-of-book (L=1) spoofing noise.
*   **High-Frequency Simulation:** If building backtest frameworks, mandate high-fidelity Level-3 (Market-By-Order) reconstruction and queue simulation frameworks (e.g., HftBacktest) to account for feed/order latencies mathematically.
*   **Vectorized Acceleration:** Accelerate raw asynchronous trade arrays and microstructure features strictly via Numba JIT compilation or Rust integrations, actively bypassing non-deterministic and high-latency Pandas aggregations.
*   **Programmatic Risk States:** Define all risk and trade closures using hardcoded R-multiple breakeven state definitions, absolute volatility scale-outs, and Correlation Elasticity tracking arrays.
*   **Microstructure Liquidation Logic:** Trigger liquidity sweep state transitions by computing Open Interest (OI) destruction divergences against localized standard deviation bounds of exchange reserves.
*   **Volume State Verification:** Require algorithmic verification of volume for displacement states, specifically demanding localized Volume Z-Score acceleration and programmatic highest-volume-node (HVN) absolute arrays before validating structural regime shifts.

## Red Flags

| Flag | Domain-Specific Rationalization | Why Wrong |
| :--- | :--- | :--- |
| SL/TP Acronyms | "The system sets an SL at 0.5% and a TP at 1.5% for risk management." | Relies on brittle retail jargon and arbitrary heuristics instead of programmatic R-multiple state definitions and ATR-scaled scale-out logic. |
| ML/Math Buzzwords | "The FSM utilizes RANSAC flat slopes and ML-classified confidence for structure." | Abstracts away the required concrete computational structures (array inequalities, boolean gates) needed for executable code. |
| Physics Jargon | "Execute upon kinematic validation of the price vector." | Contaminates execution code with meaningless cross-domain phrasing; logic must rely on numeric absolute price differentials. |
| Pure FSM without Signal Math | "The state machine moves from IDLE to ACTIVE based on a stateful object-oriented array." | Over-specializes architectural flow while starving the model of exact mathematical market structure parameters and array logic. |
| Latency Agnosticism | "Assume instant fills upon signal crossover." | Fails to incorporate queue probability modeling and L3 depth simulation, creating an invalid mathematical expectancy. |

## Quick Reference

| Execution Component | Programmatic Implementation | Target Architecture |
| :--- | :--- | :--- |
| **Trade Lifecycle** | Closed-loop FSM with rollback handlers | NautilusTrader / Event-Driven |
| **Signal Gating** | Array index inequalities & Boolean logic | `np.where` / Absolute Differentials |
| **Microstructure Speed** | Raw asynchronous array vectorization | Numba JIT / Rust |
| **Order Flow Imbalance** | Depth 5 (L=5) volumetric regression | Level 3 / Market-By-Order |
| **Queue Simulation** | Latency modeling & fill probability | HftBacktest Frameworks |
| **Boundary Logic** | Dynamic ATR-scaled absolute thresholding | Time-Series Arrays |
| **Risk/Position Sizing** | R-multiple scale-out state transitions | Exposure Compression Arrays |