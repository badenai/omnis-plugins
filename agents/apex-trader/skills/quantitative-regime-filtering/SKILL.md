---
name: quantitative-regime-filtering
description: Use when building algorithmic regime classifiers, integrating Gamma Exposure (GEX) filters, calculating Vol-of-Vol (VoV) Z-scores, evaluating signal entropy, or programmatic system activation state switching.
filePattern: "**/*.py"
---

## The Iron Law

```text
Every quantitative regime classification must be mathematically derived from absolute array index inequalities and standard deviation bounds (e.g., VoV Z-scores, GEX polarity, signal entropy); never activate an execution state machine without evaluating its strictly defined Boolean regime gate.
```

## Behavioral Rules

*   Evaluate Gamma Exposure (GEX) polarity to set the Boolean regime state: mandate `sticky_regime = True` (mean-reversion logic enabled) for positive GEX and `slippery_regime = True` (breakout/trend logic enabled) for negative GEX.
*   Calculate Volatility-of-Volatility (VoV) Z-scores using standard deviation bounds over an N-bar window array.
*   Implement a hard Boolean circuit breaker that overrides all signals and halts execution when the VoV Z-score exceeds +1.5.
*   Apply a 0.45 correlation suppression multiplier to mathematical weights when aggregating array signals from identical analytical families.
*   Calculate absolute system confidence using the arithmetic ratio `1 - (Signal Entropy / Max Entropy)`.
*   Output probability uncertainty metrics alongside every signal matrix to prevent mirage reasoning in Out-of-Distribution (OOD) environments.
*   Scale position sizing leverage arrays inversely to the calculated correlation elasticity threshold across asset classes.
*   Trigger parameter switching exclusively through verifiable mathematical thresholds and array index inequalities rather than relying on object-oriented abstractions.
*   Derive all momentum metrics strictly from Order Flow Imbalance (OFI), VoV arrays, or empirical execution data, completely ignoring lagging retail indicator crossovers.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "Pause the strategy if price action is choppy or moving sideways." | Relies on vague visual interpretation; regime halts must use strict VoV Z-Score thresholds and Boolean circuit breakers. |
| "Implement a stateful object-oriented sanitization protocol to filter out kinematic variance." | Over-engineered, cross-domain vocabulary contamination; use concrete array index inequalities and standard deviation bounds. |
| "Filter the market regime by confirming if the 50-period moving average crosses the 200-period." | Uses lagging retail indicators; momentum and regime states must derive from Gamma Exposure (GEX) and Order Flow Imbalance (OFI). |
| "Calculate a 1.0% stop-loss and take-profit heuristic to cap exposure during high volatility." | Contaminated by retail trading jargon; requires R-multiple risk encoding and deterministic matrix exposure scaling. |
| "Return the fusion signal simply as a 1 or 0 binary execution trigger." | Fails to account for epistemic uncertainty; the system must output probabilistic uncertainty alongside the structural signal array. |

## Quick Reference

| Action | Computable Implementation Rule |
| :--- | :--- |
| **GEX Matrix Logic** | Positive = Mean-Reversion array enabled; Negative = Breakout array enabled. |
| **VoV Circuit Breaker** | `if vov_zscore_array[i] > 1.5:` trigger systemic execution halt. |
| **Signal Entropy Check** | System Confidence = `1 - (Signal Entropy / Max Entropy)`. |
| **Correlation Penalty** | Multiply signal weights by 0.45x if sourced from identical analytical families. |
| **Risk Elasticity** | Scale down position sizing leverage arrays deterministically upon breaching the correlation elasticity limit. |
| **Execution Gating** | Enforce strict Boolean verification (`True`/`False`) of the active macro regime before passing parameters to the execution engine. |