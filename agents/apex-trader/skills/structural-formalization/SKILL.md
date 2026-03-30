---
name: structural-formalization
description: Use when formalizing subjective price action concepts (e.g., Fair Value Gaps, Market Structure Shifts, Order Blocks) into deterministic, executable Python code via array index inequalities, absolute price differentials, and Boolean triggers.
filePattern: "**/*.py"
---

## The Iron Law

```text
Every subjective price action concept must be strictly distilled into absolute mathematical boundaries, precise array index inequalities, and computable Boolean gates; never rely on visual discretion, retail heuristics, or unquantifiable chart reading.
```

## Behavioral Rules

- Require explicit array bounds and `abs(Close - Open) > ATR(10) * BodyMultiplier` formulations when formalizing Market Structure Shifts (MSS) or programmatic breakout containment.
- Define Order Blocks using deterministic Boolean variables (e.g., `close_mitigation = True`) that invalidate only upon a structural close beyond predefined algorithmic bounds, completely ignoring transient wick intrusions.
- Implement Zones of Failure as an exact 3-touch structural ceiling array where the trigger evaluates strictly if the third attempt fails mathematically to exceed the prior `N-period` local extrema.
- Formalize Fair Value Gaps using strict absolute price differentials and dynamic Volatility-Scaled ATR thresholds to dictate whether gaps qualify to enter the dynamic trailing memory array.
- Enforce structural containment and signal filtering using explicit `N-bar` window logic, `N-dimensional` NumPy arrays, and array indexing rather than generic state abstractions or unquantifiable ML buzzwords.
- Program entry, invalidation, and scale-out logic as exact absolute coordinate crossings or strictly defined programmatic risk multiples, and never use discretionary retail jargon.
- Extract Order Flow Heatmap characteristics and limit order representations exclusively into numerical `N-dimensional` NumPy arrays for downstream algorithmic evaluation and Order Flow Imbalance (OFI) linear regression.
- Compute dynamic structural baseline states by parsing chaotic tick streams into Imbalance bars and utilizing real-time cross-track error computations rather than phase-delayed moving averages.
- Anchor localized entry triggers exactly at the 50% coordinate (Consequent Encroachment) of the identified structural node derived from multi-timeframe structural mapping matrices.

## Red Flags

| Rationalization | Why Wrong |
| :--- | :--- |
| "Set SL to 1% and TP to 3% for the trade." | Uses retail trading acronyms; fails to implement programmable structural invalidation loops and mathematically closed scale-out logic. |
| "Check if price visually sweeps liquidity to trigger entry." | Relies on unquantifiable anthropomorphic definitions; must use deterministic limit order density decay arrays and OFI. |
| "Implement kinematic variance for structural decay." | Contaminates code with irrelevant physics jargon instead of relying on concrete array indexing and standard Boolean gates. |
| "Track the FVG with an object-oriented stateful wrapper." | Replaces absolute mathematical price differentials and standard deviation bounds with superficial object-oriented filler. |
| "The breakout is confirmed if the High crosses the prior High." | Lacks standard deviation or ATR volatility containment validation (e.g., `abs(Close - Open) > ATR`). |

## Quick Reference

| Concept | Deterministic Implementation |
| :--- | :--- |
| Market Structure Shift (MSS) | `abs(Close - Open) > ATR(10) * BodyMultiplier` |
| Order Block Invalidation | Boolean flag triggered strictly by `Close > Bounds`; ignore wick highs/lows. |
| Zones of Failure | Array evaluating a 3-touch structural ceiling against `N-period` local extrema. |
| Volatility-Scaled FVG | Absolute gap price differential dynamically filtered via ATR multiplier arrays. |
| Liquidity Validation | `N-dimensional` NumPy arrays parsing Order Flow Imbalance (OFI) limit density. |
| Consequent Encroachment | Exact 50% coordinate mapping of the quantified structural node. |