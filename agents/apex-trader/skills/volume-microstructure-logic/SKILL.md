---
name: volume-microstructure-logic
description: Use when formalizing order flow imbalance, Z-Scored Volume Profiles, session liquidity mechanics, ES Futures POC Gap Determinism, microstructure liquidation cascades, and depth-specific OFI metrics into deterministic algorithms.
---

## The Iron Law

```text
You must encode all volume, order flow, and liquidity microstructure mechanics strictly as computable mathematical thresholds, deterministic boolean gates, and explicit array index inequalities, entirely rejecting subjective chart interpretations, lagging retail indicators, and generic risk heuristics.
```

## Behavioral Rules

- Define POC Gap Determinism using session-relative opening price differentials to compute exact mean-reversion pull probabilities based on empirical ES Futures structural mechanics.
- Formalize POC (Point of Control) Migration divergence by enforcing multidimensional array inequalities where a breakout boolean is invalidated if the temporal POC vector descends while the price vector ascends.
- Calculate Multi-Level Order Flow Imbalance (MLOFI) by applying absolute contract delta formulas to N-depth Level 2 bid/ask liquidity matrices to compute pre-breakout institutional displacement.
- Programmatically define unfinished auctions strictly as structural price extremes where exactly 0 contracts are mathematically recorded on the respective bid/ask array index.
- Require structural breakouts to trigger an FSM state transition only when accompanied by session-relative volume Z-scores exceeding a explicitly defined standard deviation bound.
- Map microstructure liquidation cascades by comparing Open Interest (OI) destruction arrays against absolute price stability vectors within strict 60-second rolling temporal boundaries.
- Compute explicit mathematical position sizing, volatility-adjusted scaling bounds, and programmatic R-multiple breakeven logic instead of relying on retail stop-loss frameworks.
- Execute Order Flow Imbalance evaluation using explicit asynchronous state management to ensure deterministic temporal alignment between executing tick flows and L2 snapshot data.

## Red Flags

| Rationalization / Concept | Why Wrong |
| :--- | :--- |
| "Setting SL and TP parameters..." | Relies on retail jargon instead of deterministic FSM state transitions and programmatic scale-out logic. |
| "Kinematic validation of order flow..." | Hallucinates physics-adjacent jargon instead of utilizing concrete array indexing and standard deviation bounds. |
| "Scaling structural memory using KNN models..." | Over-complicates deterministic logic with arbitrary ML buzzwords instead of relying on explicit computational structures and boolean gates. |
| "Limiting exposure to 1.0% per trade..." | Hardcodes arbitrary retail risk percentages instead of defining programmatic, volatility-scaled risk matrices. |
| "Volume looks exceptionally strong..." | Subjective and non-computable; volume must be rigidly normalized via Z-scores or standard deviation arrays. |
| "Implementing an object-oriented stateful array sanitization protocol..." | Replaces precise mathematical array operations and FSM execution architecture with generic, unactionable programming filler. |

## Quick Reference

| Concept | Formalization Metric | Execution Logic |
| :--- | :--- | :--- |
| **POC Divergence** | Temporal POC vector vs. Price vector array | Invalidate 'hollow' breakout boolean gates. |
| **Multi-Level OFI** | N-depth L2 bid/ask delta threshold | Trigger pre-breakout displacement states in the FSM. |
| **Unfinished Auctions** | Array index with `contracts_traded == 0` | Target mathematically deterministic structural extremes. |
| **Volume Expansion** | Session-relative Volume Z-Score > $X\sigma$ | Validate structural containment and expansion events. |
| **Liquidation Cascades** | OI destruction matrix vs. spot absolute differential | Execute mean-reversion logic upon ADL exhaustion detection. |
| **Microstructure Alignment** | ASOF JOIN temporal matrix indexing | Guarantee deterministic alignment of asynchronous L2 data. |