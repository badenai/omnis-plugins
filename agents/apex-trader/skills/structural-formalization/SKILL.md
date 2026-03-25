---
name: structural-formalization
description: Use when formalizing subjective price action concepts into deterministic algorithmic logic, translating structural containment, array index inequalities, CUSUM-based market structure breaks, and absolute price differentials into executable code.
filePattern: "**/*.py"
bashPattern: "pytest|python"
---

## The Iron Law

```text
You must translate all subjective price action into explicit programmatic logic using concrete computational structures: exact array index inequalities, N-bar window arrays, absolute price differentials, and deterministic Boolean gates.
```

## Behavioral Rules

*   Translate structural imbalances and gaps into precise computational definitions utilizing explicit array index conditions (e.g., comparing `high` values at `t-1` directly to `low` values at `t+1`).
*   Define market structure breaks strictly through mathematical threshold breaches, utilizing logic such as Cumulative Sum (CUSUM) array functions or N-bar absolute price differentials.
*   Gate breakout and structural containment logic utilizing simultaneous N-period dynamic rolling min/max arrays mapped directly to Boolean states.
*   Calculate retention failures and previous failure zones by quantifying the exact temporal duration (bar counts) a price array sustains computational boundary logic before a programmed breach.
*   Require absolute price differentials and mathematically computed volatility limits (e.g., True Range array values) for dynamic position invalidation, preventing reliance on static risk assumptions.
*   Couple all structural signal generation directly with explicit programmed execution logic to ensure every mathematical entry threshold has a mathematically defined exit state.
*   Compute mean reversion targets strictly utilizing exact midpoint calculations of predefined impulse arrays, gating entries exclusively via Boolean validation of internal structure loss.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "Applying physics or kinematic terminology to describe market velocity." | Contaminates programmatic vocabulary and prevents the generation of exact, executable computational variables. |
| "Setting predefined, static percentage values to restrict positional risk." | Fails to enforce dynamic, computationally derived position sizing using true programmatic risk constraints. |
| "Abstracting price patterns into heavy machine-learning classifiers." | Replaces the explicit, unambiguous array inequalities and Boolean gates needed for transparent deterministic execution logic. |
| "Implementing heavy object-oriented state architectures for standard calculations." | Produces unactionable, over-engineered filler code when straightforward mathematical array functions are required. |
| "Using retail trading terminology to manage positional boundaries." | Abandons explicit, deterministically closed mathematical state transitions and programmatic scale-out arrays. |

## Quick Reference

| Structural Concept | Deterministic Translation |
| :--- | :--- |
| **Imbalance Logic** | Exact computational array inequalities (e.g., `high.shift(1) < low.shift(-1)`) |
| **Breakout Gating** | Simultaneous N-bar dynamic rolling min/max array bounds |
| **Structure Breakdown** | Computed threshold breaches via CUSUM data structures |
| **Retention Failure** | Explicit bar-count duration thresholds mapped prior to an array breach |
| **Dynamic Invalidation** | Volatility-scaled absolute price differentials mapped to state limits |
| **Mean Reversion Target** | Calculated midpoint of an impulse N-bar window logic sequence |