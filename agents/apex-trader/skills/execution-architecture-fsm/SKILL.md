---
name: apex-trader
description: Activates when tasked with designing, implementing, or refactoring quantitative trading algorithms, automated risk-management constraints, or programmatic trade lifecycle execution architecture.
---

## The Iron Law

```text
Require explicit programmatic invalidation and fixed risk per trade constraints for every algorithmic entry signal; never allow undefined trade states or logic that relies on subjective intervention.
```

## Behavioral Rules

* Before writing trade entry code, enforce a fixed maximum risk limit (e.g., capping risk at exactly 1.0% of portfolio equity) and define a strictly computable exit condition.
* When implementing structural pattern detection, use explicit time-series array indexing, window lookbacks, and boolean comparisons (e.g., checking if `close[0] > high[1]`) instead of abstract mathematical notation or cross-domain physics jargon.
* Require volumetric validation for breakout or expansion signals by coding discrete quantitative thresholds, such as relative volume multipliers or moving average comparisons.
* When managing trade lifecycles, write explicit error-handling callbacks for asynchronous API events like partial fills and exchange disconnects to ensure exact deterministic execution.
* Avoid wrapping simple calculations, such as position sizing or basic arithmetic, in unnecessarily complex architectural frameworks; reserve state machines strictly for handling asynchronous external trade events.
* When utilizing sentiment scores or external signals, apply them strictly as quantitative regime filters or boolean circuit breakers rather than raw execution triggers.

## Red Flags

| Rationalization | Why It's Wrong |
| :--- | :--- |
| "Let's use a kinematic validation model to verify the price action slope." | Implement discrete boolean checks and array comparisons instead of contaminating the code with irrelevant physics terminology. |
| "The system will exit when the machine learning model predicts a reversal." | Code explicit, hardcoded stop-loss logic; do not substitute predictive classification for rigid deterministic risk boundaries. |
| "We should wrap the position sizing logic in a Finite State Machine." | Keep simple programmatic arithmetic direct; reserve complex state architecture for actual asynchronous trade lifecycle routing. |
| "We can just run a standard MACD crossover to define the market trend." | Base entry rules on computable market structure and liquidity events rather than generic, lagging indicators without volume validation. |

## Quick Reference

| Allowed | Forbidden |
| :--- | :--- |
| Explicit array index lookbacks & thresholds | Physics, ML, or abstract math jargon |
| Hardcoded maximum-risk percentage caps | Open-ended or undefined risk parameters |
| Volume-validated boolean execution rules | Raw signals based on subjective indicators |
| Discrete API callback error handling | Assuming perfect instantaneous order fills |

## Knowledge Base
When detailed knowledge context is needed, read `references/digest.md` for the full knowledge digest.