---
name: structural-formalization
description: Use when translating subjective price action patterns into deterministic mathematical algorithms, designing regime filters via GEX or Vol-of-Vol, mapping Zones of Failure arrays, or calculating structural tick-level regression bounds.
filePattern: "**/*.py"
---

## The Iron Law
```text
You must encode every structural market pattern, regime transition, and execution state as deterministic array index inequalities, absolute price differentials, standard deviation bounds, or computable rolling statistics, explicitly rejecting all discretionary technical analysis and rigid retail risk heuristics.
```

## Behavioral Rules

*   **Define Structural Bounds Mathematically**: Translate Fair Value Gaps (FVGs) and market structure breaks into programmable data structures by calculating the absolute slope of their tick-level linear regression line (`abs(beta1)`); only validate entries if the void degree is `<= 0.00015` units/sec, while strictly rejecting stop-hunts characterized by slopes `> 0.0004` units/sec.
*   **Enforce Quantitative Regime Parameters**: Dictate Finite State Machine (FSM) activation by mapping Gamma Exposure (GEX); trigger a "STICKY" mean-reversion FSM regime when GEX is positive, and a "SLIPPERY" breakout/trend-following matrix when GEX falls into low or negative thresholds.
*   **Program Volatility Circuit Breakers**: Halt all non-closing execution sequences programmatically if the Vol-of-Vol (VoV) Z-score strictly exceeds `+1.5` standard deviations, treating the volatility surface as hostile.
*   **Map Structural Failure Sequences**: Define Zones of Failure via an explicit 3-vector rolling array sequence (`[Array 1: High]`, `[Array 2: Retracement/Secondary Pump]`, `[Array 3: Failure to Gain]`); lock short execution strictly to Array 3 overlaps concurring with volume expansion bounds exceeding `1.5x` Relative Volume (RVOL).
*   **Encode Execution in Closed-Loop Architecture**: Decouple underlying signal generation mathematics (e.g., ATR volatility boundaries, absolute price differentials) from the FSM trade lifecycle execution; ensure all execution logic routes through explicit deterministic states (`PRE_INITIALIZED`, `READY`, `RUNNING`, `STOPPED`, `DEGRADED`, `FAULTED`).
*   **Extract Microstructure Displacements**: Compute Order Flow Imbalance (OFI) scaled rigidly between `-1.0` and `+1.0`; aggregate volumetric imbalances to a strict Limit Order Book depth of 5 (L=5) to strip spoofing noise and elevate predictive correlation without introducing lag.
*   **Utilize Dynamic Volatility Memory**: Filter out low-volatility structural gaps dynamically using explicit Average True Range (ATR) multipliers; encode valid volatility-scaled gaps as strict `[Lower_Bound, Upper_Bound]` state transitions for programmatic stop-trailing matrices.
*   **Implement Error-Aware Rollbacks**: Force the FSM into a `FAULTED` state immediately upon detecting arithmetic overflow, unhandled tick latency, or partial fills, executing a deterministic state rollback to avert compounding execution errors.

## Red Flags

| Pattern | Why it Fails (Domain-Specific Rationalization) |
| :--- | :--- |
| Injecting physics buzzwords (e.g., "kinematic validation", "kinematic variance") | **Vocabulary contamination.** Replaces concrete programmatic concepts like boolean gates and array index inequalities with unactionable, meaningless jargon. |
| Hardcoding "Stop-Loss (SL)", "Take-Profit (TP)", or arbitrary `1%` risk heuristics | **Retail jargon contamination.** Replaces programmable R-multiple matrices, ATR-bounded state transitions, and absolute mathematical position sizing with brittle discretionary retail logic. |
| Over-specializing strategy entirely into FSM architecture while omitting numerical thresholds | **Scope over-specialization / Instruction deletion.** Starves the algorithm of necessary mathematical rigor by stripping out the concrete quantitative metrics (e.g., ATR boundaries, standard deviation bounds) needed for signal validation. |
| Replacing L2 depth Order Flow Imbalance (OFI) with simple "N-bar swing logic" | **Quantitative logic dilution.** Severely weakens the system's ability to programmatically model complex market microstructure and institutional displacement dynamics. |
| Masking basic arithmetic with terms like "stateful object-oriented array sanitization" | **Superficial algorithmic over-engineering.** Artificially inflates standard calculations with verbose object-oriented terminology, resulting in imprecise and bloated code directives. |
| Defining structural shifts using formatting symbols (e.g., $\rightarrow$, $\le$) instead of operators | **Execution abstraction.** Abstracts explicit code-level directives and numerical boolean operations (`<=`, `>`, `==`) behind formatting syntax, diminishing direct machine interpretability. |

## Quick Reference

| Concept | Deterministic Translation | Computable Threshold / Implementation |
| :--- | :--- | :--- |
| **FVG Structural Validation** | Tick-Level Linear Regression Slope | `abs(beta1) <= 0.00015` units/sec (Valid); `> 0.0004` (False) |
| **Regime State Switch (GEX)** | Gamma Exposure Polarity Matrix | `GEX > 0` = STICKY (Range); `GEX <= 0` = SLIPPERY (Trend) |
| **System Circuit Breaker** | Vol-of-Vol (VoV) Z-Score Limit | Halt non-closing executions if `VoV_Z > +1.5` sigma |
| **Order Flow Imbalance (OFI)** | Aggregated LOB Volumetric Matrix | Compute strictly from `-1.0` to `+1.0` at Depth `L=5` |
| **Zones of Failure** | Rolling Array Sequence + RVOL | `[High, Retrace, Fail]` vector overlap + `Volume > 1.5x RVOL` |
| **Execution Architecture** | Decoupled Closed-Loop FSM | `READY`, `RUNNING`, `STOPPED`, `FAULTED` strict enforcements |
| **Programmatic Stop Bounds** | Volatility-Scaled FVG Dynamic Array| `[Lower_Bound, Upper_Bound]` state transitions mapped to ATR |