---
name: institutional-order-flow-timing
description: Use when analyzing market session boundaries, AMD (Accumulation, Manipulation, Distribution) cycles, Killzone setups, DOM/Footprint order absorption, volume spread analysis (VSA), or executing IOFED/Judas CHOCH strategies based on time and algorithmic order flow.
---

## The Iron Law

```text
Never execute a structural setup without confirming session timing (AMD Killzones) and verifying institutional volume absorption or displacement at the swept liquidity boundaries.
```

## Behavioral Rules

* Map the algorithmic Power of 3 (AMD) cycle strictly by defining Asian session Accumulation, London session Manipulation (Judas Swing), and New York session Distribution.
* If trading a Judas CHOCH, wait for a specific Killzone to sweep established session boundaries before anticipating a reversal.
* Require violent lower-timeframe displacement immediately following a time-based sweep to validate institutional footprint.
* Confirm structural sweeps by checking DOM or Footprint data to identify heavy institutional limit orders (liquidity walls) absorbing aggressive retail market orders.
* Validate Wyckoff Springs (Sell-Side Liquidity sweeps) and Upthrusts (Buy-Side Liquidity sweeps) exclusively when accompanied by tick volume expansion.
* Execute Institutional Order Flow Entry Drill (IOFED) entries strictly at the proximal edge of an unmitigated Fair Value Gap (FVG) to enforce highly asymmetric Risk-to-Reward.
* Abandon pure price action setups if they occur outside of high-volume session Killzones.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "This structure looks perfect, even though we are in the middle of the Asian session." | Algorithms operate on specific time-based Killzones; out-of-session moves lack institutional backing and volume. |
| "I will wait for the FVG 50% Equilibrium (EQ) to enter safely." | IOFED mechanics dictate proximal edge execution; waiting for EQ sacrifices high R:R and often results in entirely missed entries. |
| "Price swept the Previous Day High, so I am shorting the immediate tick." | Entering without confirming DOM absorption or immediate displacement invites getting crushed by true structural breakouts. |
| "Volume data is just secondary lagging noise." | Classical VSA and order flow footprint validate true institutional intent during sweeps, filtering out fake CHOCHs (Inducements). |

## Quick Reference

| Concept | Required Action |
| :--- | :--- |
| **AMD Framework** | Bracket Asian Accumulation limits; target London Manipulation sweeps; ride New York Distribution. |
| **Judas CHOCH** | Fade the initial Killzone breakout that targets prior session external liquidity pools. |
| **DOM Absorption** | Inspect footprint charts for massive limit order walls trapping retail market orders at sweep levels. |
| **Wyckoff Confluence** | Demand tick volume expansion on all Spring (SSL) and Upthrust (BSL) events. |
| **IOFED Execution** | Set aggressive limit entries precisely at the proximal edge of the displacement FVG. |