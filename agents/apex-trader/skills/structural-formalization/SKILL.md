---
name: structural-formalization
description: Use when translating subjective price action patterns, Fair Value Gaps (FVGs), and market structure boundaries into deterministic computational arrays, Boolean execution gates, and volatility-scaled programmatic logic.
filePattern: "**/*.py"
---

## The Iron Law

```text
You must formalize all Fair Value Gaps (FVGs) and market structure bounds using explicit computational data structures—specifically array index inequalities, absolute price differentials, N-bar window logic, and ATR volatility thresholds—and never substitute these mathematical definitions with subjective charting concepts, retail trading mechanics, or abstract physics jargon.
```

## Behavioral Rules

- Define FVGs strictly as 3-candle computable imbalance logic arrays utilizing exact array index inequalities (e.g., `np.where((high.shift(1) < low.shift(-1)))`).
- Scale all structural containment arrays and FVG memory boundaries dynamically using ATR threshold multipliers.
- Trigger Boolean state inversions for structural shifts only when closing absolute price differentials strictly pierce programmatic standard deviation bounds.
- Validate FSM-gated breakouts by coupling FVG array generation directly to concurrent Support/Resistance N-period rolling threshold breaks.
- Manage position invalidation and dynamic trailing via explicit R-multiple mathematical boundaries and strict programmatic array bounds.
- Govern trade lifecycles through closed finite state machines that evaluate exact algorithmic arithmetic and absolute price differentials for execution.
- Discard FVG arrays programmatically if the absolute price movement fails to exceed localized order flow or N-bar window validation requirements.
- Calculate signal invalidation thresholds using empirical microstructure metrics rather than relying on abstract machine learning buzzwords or superficial object-oriented state sanitization.

## Red Flags

| Rationalization | Why Wrong |
| :--- | :--- |
| "I will implement a standard SL and TP parameter to govern the FVG risk engine." | Retail trading acronyms abstract away the explicit, deterministically closed FSM state transitions and programmatic R-multiple scale-out logic required for quantitative architecture. |
| "We should measure the structural kinematic variance using a stateful sanitization protocol." | Physics-adjacent jargon and generic object-oriented buzzwords replace the precise array index inequalities, Boolean gates, and absolute price differentials required for executable code. |
| "Risk per trade is capped between 0.1% and 1.0% based on account size." | Hardcoding arbitrary risk percentage heuristics replaces dynamic, mathematical position sizing and programmatic R-multiple breakeven arrays. |
| "I'll use ML-classified confidence scores and RANSAC flat slopes to validate the breakout." | Substituting practical programming concepts with complex ML/math buzzwords diminishes the model's ability to generate unambiguous, deterministic N-bar window execution code. |

## Quick Reference

| Concept | Deterministic Implementation |
| :--- | :--- |
| **FVG Array Detection** | Implement via 3-candle index arrays: `np.where((high.shift(1) < low.shift(-1)))`. |
| **Volatility Scaling** | Store valid FVG boundaries in dynamic arrays scaled by an ATR threshold multiplier. |
| **Market Structure Break** | Trigger Boolean state inversions strictly when price breaches N-bar rolling thresholds. |
| **Position Containment** | Execute programmable risk boundaries governed by R-multiple breakeven state arrays. |
| **Signal Validation** | Require absolute price differentials and standard deviation bounds to confirm displacement. |
| **Lifecycle Execution** | Map all signal generations and invalidations directly into closed-loop Finite State Machines. |