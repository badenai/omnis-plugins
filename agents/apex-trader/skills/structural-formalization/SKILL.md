---
name: structural-formalization
description: Use when translating subjective price action (FVGs, order blocks, trend lines, liquidity sweeps) into deterministic algorithms, executable array logic, or programmatic market structure rules.
filePattern: "**/*.py"
---

## The Iron Law

```text
Never accept or generate subjective visual price action descriptions; you must strictly translate every structural concept (e.g., FVGs, sweeps, order blocks) into executable N-bar window logic, computable array index inequalities, absolute price differentials, ATR volatility thresholds, and rigid Boolean gates.
```

## Behavioral Rules

- If defining Fair Value Gaps (FVGs) or order blocks, mandate deterministic mathematical boundaries using absolute price differentials and maintain active zones in ATR-penalized Time-to-Live (TTL) memory arrays.
- When formalizing liquidity sweeps, mandate explicit localized structural breaks (e.g., Boolean CHoCH triggers via array index comparisons) and Volume Z-Score > +1.5σ validation to algorithmically falsify manufactured liquidity voids.
- If mapping multi-timeframe support or resistance, enforce recursive fractal trees by computing the exact 50% midpoint (`Consequent Encroachment = (High + Low) / 2`) of valid displacement nodes using N-bar window arrays.
- Dictate trend containment and structural invalidation exclusively as deterministic state transitions triggered when continuous closing prices violate a dynamically averaged, volatility-scaled containment band.
- Always couple signal generation logic directly with risk execution logic by providing both the deterministic array inequalities for the setup and the programmatic mathematical position sizing (e.g., R-multiple breakeven logic).
- Reject lagging retail indicator simplifications (like MACD or generic EMAs); enforce Zero-Phase Filter (ZPF) smoothing and real-time Order Flow Imbalance (OFI) extraction for institutional displacement tracking.
- If testing or validating structural logic, natively encode walk-forward validation parameters and continuous out-of-sample data partitioning directly into the quantitative architecture.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "Implement a 3-bar FVG entry with standard SL/TP targets and a 1% risk cap." | Reject retail jargon and static percentages; you must define risk via programmatic dynamic R-multiples derived from absolute price differentials and current ATR arrays. |
| "Measure the kinematic variance and momentum decay to find structural reversals." | Avoid cross-domain physics jargon; you must rely on strict computable variables like standard deviation boundaries, discrete array indices, and Boolean logic gates. |
| "Use an object-oriented stateful sanitization array to classify the market trend." | Eradicate generic programming buzzwords; you must provide explicit mathematical array manipulations and concrete logic for baseline structural state tracking. |
| "Feed the raw, unadjusted LOB sequence directly into a standard LSTM predictor." | Never use unstationary raw data in black-box models; you must enforce strict differencing, Z-scoring, or dimensional reduction (e.g., PCA) before model ingestion. |
| "Deploy a Finite State Machine (FSM) to calculate the fixed position size." | Never shoehorn complex architectural frameworks into simple arithmetic operations; you must reserve FSMs for asynchronous tick data parsing and strict state closures. |

## Quick Reference

| Subjective Concept | Programmatic Formalization Directive |
| :--- | :--- |
| **Trend / Bias** | Compute continuous CUSUM (Cumulative Sum) structural breaks with explicit Boolean array invalidation. |
| **Fair Value Gap (FVG)** | Track absolute price differentials stored in ATR-penalized arrays with specific N-bar containment window logic. |
| **Liquidity Sweep** | Code a price excursion beyond an N-bar local extremum followed by Volume Z-score > 1.5σ and a reverse Boolean CHoCH. |
| **Support / Resistance** | Map recursive fractal node displacements and trigger at the exact `(High + Low) / 2` Consequent Encroachment midpoint. |
| **Market Regime** | Evaluate Gamma Exposure (GEX) combined with Volatility-of-Volatility (VoV) Z-scoring to gate Boolean execution states. |
| **Risk / Stop Loss** | Define Mean Time To Violation (MTTV) constraints and R-multiple scale-out matrices based on deterministic tick velocity. |