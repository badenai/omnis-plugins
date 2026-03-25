---
name: volume-microstructure-logic
description: Use when building, debugging, or optimizing trading algorithms that analyze order flow imbalance (OFI), microstructure liquidation mechanics, volume profiles, open interest (OI) divergence, and high-frequency tick data.
filePattern: "**/*.py"
---

## The Iron Law

```text
Enforce all microstructure and liquidity events as exact programmatic variables utilizing strict array index inequalities, absolute price differentials, and explicitly calculated volumetric thresholds. Never substitute explicit mathematical definitions with generic object-oriented buzzwords, physics analogies, retail acronyms, or qualitative descriptions of price action.
```

## Behavioral Rules

*   Calculate Order Flow Imbalance (OFI) strictly as a bounded float between -1.0 and 1.0.
*   Aggregate volumetric imbalance across exactly 5 order book levels (Depth=5) to strip spoofing noise before extracting features.
*   Accelerate high-frequency tick data parsing and array operations exclusively via Numba JIT compilation to eliminate execution latency.
*   Map liquidation cascades programmatically by tracking simultaneous open interest (OI) drops and price vector changes within the exact same millisecond timestamp.
*   Detect forced-closure squeeze events using boolean gates: require offshore derivative OI to increase concurrently with negative funding rates and positive spot premiums.
*   Compute Fair Value Gap (FVG) velocity by extracting the absolute slope of its tick-level linear regression line (`abs(beta)`), avoiding lagging indicators entirely.
*   Define true structural displacement by enforcing a maximum absolute slope threshold (e.g., `<= 0.00015` units/sec) on tick-level voids.
*   Ignore high-degree price gaps (`abs(beta) > 0.0004` units/sec) algorithmically by tagging them as false stop-hunts.
*   Define High Volume Nodes (HVNs) strictly as the 80th percentile volume quantiles within an explicitly defined N-bar rolling array.
*   Validate breakout execution vectors only if the current price array traverses an HVN-bounded coordinate state concurrently with a strictly positive Cumulative Volume Delta (CVD).
*   Compute Point of Control (POC) gaps by assigning them explicit `[Lower_Bound, Upper_Bound]` array coordinates.
*   Determine structural failure (Retention Failure) by enforcing simultaneous volume expansion thresholds (`> 1.5 * RVOL`) alongside rolling N-period min/max array overlaps.
*   Enforce capital preservation by hardcoding programmatic minimum 1:3 R-multiple boundaries and deterministic execution closures over arbitrary retail percentage rules.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "Implementing SL/TP parameters to manage the liquidity sweep trade." | Introduces retail jargon; algorithm must rely on deterministic state transitions and explicitly computed R-multiple array evaluations. |
| "The algorithm detects kinematic momentum variance to validate the volume profile." | Contaminates vocabulary with physics terminology instead of utilizing standard deviation bounds or strict array indexing. |
| "Using an RSI overbought threshold to detect the liquidation cascade." | Relies on lagging indicators instead of mapping explicit microstructure order flow imbalance and derivative open interest divergences. |
| "Structuring the trade state via a generic object-oriented array matrix." | Replaces precise mathematical operations and boolean logic with unactionable, superficial programming buzzwords. |
| "Executing the order because the FVG looks like a high-probability displacement." | Discretionary and vague; requires explicit tick-level linear regression slope calculations and absolute threshold gating. |

## Quick Reference

| Microstructure Concept | Programmatic Implementation |
| :--- | :--- |
| **Order Flow Imbalance (OFI)** | `Float [-1.0, 1.0] calculated via L2 order book aggregated to Depth=5` |
| **Squeeze Divergence FSM** | `if OI[i] > OI[i-1] and FundingRate < 0 and SpotPremium > 0:` |
| **High Volume Node (HVN)** | `Volume >= 80th percentile of rolling N-bar volume array` |
| **Liquidation Vector Stop** | `Trigger immediately upon Total OI and Price declining in the same ms` |
| **Valid Structural Displacement** | `abs(linear_regression_slope) <= 0.00015` |
| **Volume Retention Failure** | `Current Volume > (1.5 * RVOL) AND Price intersects N-period overlap` |
| **High-Frequency Parsing** | `@njit` compilation over multi-dimensional tick data numpy arrays |