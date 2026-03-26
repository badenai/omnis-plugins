---
name: quantitative-regime-filtering
description: Use when engineering system activation flags, mapping Gamma Exposure (GEX) binary state toggles, computing Vol-of-Vol circuit breakers, calculating relative intrabar velocity via Binary-Temporal Representations, or smoothing mathematical signal arrays with zero-phase filters.
filePattern: "**/*.py"
---

## The Iron Law

```text
You must enforce programmatic regime states using strict Boolean gates, precise array index inequalities, and explicit volatility thresholds (e.g., GEX > 0, VoV Z-score > 1.5) rather than descriptive physics terminology; all execution logic must map to discrete mathematical arrays without relying on absolute time bounds or retail heuristics.
```

## Behavioral Rules

*   **Enforce GEX Binary States:** If calculating regime activation, map Gamma Exposure (GEX) into a boolean flag: set `is_sticky = True` (Positive GEX) to activate mean-reversion boundary arrays, and `is_slippery = True` (Negative GEX) to activate trend-following structural displacement rules.
*   **Trigger VoV Circuit Breakers:** If Vol-of-Vol (VoV) Z-Score exceeds +1.5σ, you must immediately set a programmatic override (`halt_execution = True`) to terminate signal generation and block FSM progression.
*   **Formalize Intrabar Velocity:** If calculating temporal structures, deploy Binary-Temporal Representation (BTR) arrays to model relative duration tempo bits instead of writing brittle logic dependent on absolute time thresholds.
*   **Implement Zero-Phase Filtering:** When designing signal smoothing architecture, apply bi-directional Zero-Phase Filters (ZPF) strictly to eliminate phase delay; explicitly forbid the use of traditional lagging moving averages.
*   **Define Executable Mathematics:** Design all state boundaries using exact N-bar window logic, computable array index inequalities, and absolute price differentials instead of abstract descriptive terms.
*   **Constrain Risk Programmatically:** Require dynamic structural failure arrays and R-multiple breakeven state definitions for invalidation logic; never utilize generic retail terminology (SL/TP) or arbitrary hardcoded percentage caps.
*   **Reject Physics Contamination:** Never substitute functional code concepts (like boolean matrices or programmatic thresholds) with cross-domain physics terminology (e.g., "kinematic validation" or "velocity kinematics") when describing price action events.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "Using 'kinematic event' accurately describes the sudden price action velocity." | Contaminates the model's programmatic vocabulary; replaces actionable Boolean gates and absolute price differentials with meaningless abstract physics jargon. |
| "We will implement a tight SL (Stop-Loss) to manage the breakout regime risk." | Submits to retail trading jargon instead of mathematically defining a strict FSM invalidation state transition or computable structural failure boundary. |
| "We'll smooth the momentum baseline using an EMA crossover." | Introduces unacceptable algorithmic phase delay; violates the mandate to utilize Zero-Phase Filtering (ZPF) arrays for signal smoothing. |
| "Limit exposure to a flat 1.0% per trade to control drawdown during regime switches." | Relies on arbitrary retail percentage heuristics rather than computing a rigorous volatility-scaled position sizing matrix and strict 1:3 R:R boundary. |
| "We must wrap the GEX threshold in stateful object-oriented arrays for sanitization." | Introduces superficial algorithmic over-engineering; obscures simple programmatic variable definitions behind vague, unactionable object-oriented buzzwords. |

## Quick Reference

| Concept | Deterministic Implementation Constraint |
| :--- | :--- |
| **GEX Regime Matrix** | Map Positive GEX to `STICKY` arrays; map Negative GEX to `SLIPPERY` arrays. |
| **Circuit Breaker** | `halt_execution = True` conditionally when VoV Z-Score > +1.5σ. |
| **Velocity Modeling** | Encode tempo bit states via Binary-Temporal Representation (BTR). |
| **Signal Smoothing** | Utilize only Zero-Phase Filters (ZPF); reject standard moving averages. |
| **Invalidation Rules** | Define structural boundary failure arrays; avoid "SL/TP" retail jargon. |
| **Architectural Syntax** | Use N-bar windows, array index inequalities, and Boolean gates. |