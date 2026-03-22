---
name: volume-microstructure-logic
description: Use when designing, debugging, or formalizing algorithms related to Volume Profile mechanics, Point of Control (POC) migration, Open Interest (OI) liquidation cascades, or deterministic microstructure imbalances.
---

## The Iron Law

```text
Never accept subjective descriptions of volume or liquidity; every volume node, Point of Control (POC) migration, and liquidation cascade must be formalized via explicit mathematical bounds, precise array index inequalities, absolute price differentials, and computable aggregate Open Interest (OI) density formulas.
```

## Behavioral Rules

- When mapping a Volume Profile, formally encode it as a matrix of deterministic absorption nodes, exact price coordinates, and calculated migration velocities over a defined N-bar window.
- If tracking a Point of Control (POC) migration, enforce a strict bearish state filter if the POC array value settles >20% below the current absolute price differential.
- Define structural balance exclusively via mathematical conditions where the exact POC coordinate is centered within the Value Area and strictly bracketed by High Volume Node (HVN) limit arrays.
- If algorithmically exploiting a POC gap, mandate a deterministic mean-reversion entry trigger only when the closing price array crosses back inside the quantified Value Area.
- When validating price expansion past structural resistance limits, require an inverse volume array condition (`Volume[t] < Volume[t-1]`) to flag a "Push to Fill" liquidity hunt.
- If price expansion occurs concurrently with increasing volume metrics, strictly classify the event as a structural containment failure and trigger your breakout logic sequence.
- Compute aggregate Open Interest (OI) density against continuously skewed funding rates to map exact mathematical coordinates for "Liquidation Pools."
- If designing a fade strategy into a forced closure event, utilize the explicitly calculated liquidation pools as high-probability entry coordinates to capture the slippage gap, rather than placing standard stop orders at subjective structural boundaries.
- When evaluating structural retention at a previously established volume node, require a deterministic nth-touch verification matrix that measures absolute delta momentum degradation across a minimum of three array interactions.

## Red Flags

| Subjective Rationalization | Algorithmic Correction |
| :--- | :--- |
| "The level looks heavy based on volume exhaustion." | Reject visual intuition; require a codified nth-touch failure matrix with explicit delta momentum degradation measured across strict n-bar arrays. |
| "Enter the trade because price is hitting a strong volume node." | Reject assumption of bounce; entry demands exact threshold triggers based on order flow absorption or delta divergence measured directly at the node coordinate. |
| "The volume profile shifted lower, so the regime is bearish." | Reject unquantified shifts; enforce a strict programmatic filter requiring the POC migration drop to exceed a defined percentage (e.g., >20%) of the absolute price differential. |
| "Liquidation cascades will trigger just past obvious round numbers." | Reject stochastic assumptions; map liquidation pools mathematically via exact Open Interest (OI) density arrays and exchange leverage multipliers. |

## Quick Reference

| Volume / Microstructure Concept | Computable Implementation Metric |
| :--- | :--- |
| Liquidation Pool Mapping | Array coordinates of max OI density multiplied by calculated forced margin closure thresholds. |
| Negative POC Shift | `POC[t] < POC[t-1]` by >20% of the active ATR or absolute price differential. |
| Structural Balance Definition | POC mathematical coordinate exactly centered between Top HVN array and Bottom HVN array. |
| POC Gap Fill Trigger | `Price[close] > Value Area Low` AND Prior POC coordinate untested. |
| Push to Fill (Liquidity Hunt) | `Price[high] > Resistance Array` AND `Volume[t] < Volume[t-1]`. |
| Containment Failure | `Price[high] > Resistance Array` AND `Volume[t] >= Volume[t-1] * Volume_Multiplier`. |
| Zone of Failure (ZPF) Array | Minimum 3-touch loop (`touch_count == 3`) AND `Delta[t3] < Delta[t2]`. |