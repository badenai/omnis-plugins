---
name: institutional-order-flow-timing
description: Use when analyzing market structure, mapping daily AMD cycles, tracking session Killzones (London/New York), evaluating SMT Divergence, or identifying high-probability institutional entry models (Unicorn, Venom, IOFED).
---

## The Iron Law

```
NEVER execute any trade entry outside of designated session Killzones (London 2 AM–5 AM EST or New York 7 AM–12 PM EST), nor without a verified higher-timeframe liquidity sweep or SMT divergence confirmation.
```

## Behavioral Rules

*   **Asian Range Assessment:** If the Asian range (8 PM–12 AM EST) does not compress into a clear, tight consolidation, abort execution plans for the subsequent London session Judas Swing.
*   **London Judas Swing Verification:** Monitor the London open (2 AM–5 AM EST) for an engineered false expansion (manipulation) that sweeps the Asian range highs or lows before looking for reversal setups.
*   **New York Distribution Execution:** Trade the true distribution expansion trend during the New York AM session (7 AM–12 PM EST), targeting the opposing HTF liquidity pools.
*   **SMT Divergence Confirmation:** Compare highly correlated assets (e.g., EUR/USD vs. GBP/USD, or S&P 500 vs. Nasdaq) at key structural swings; if one asset sweeps a key high/low while the other fails to do so, execute strictly in the direction of the sweeping asset's displacement.
*   **Breaker Block Validation:** Never trade a mitigation block lacking a prior liquidity sweep; only select breaker blocks that actively cleared resting stop orders before breaking market structure with high displacement.
*   **Unicorn Model Execution:** Place limit orders only at the exact horizontal intersection of a validated Breaker Block and an unfilled Fair Value Gap (FVG) situated within a premium or discount pricing array.
*   **Venom Model Execution:** Upon a major external liquidity sweep (PDH/PDL or session extremes), immediately monitor the lower timeframes and execute a limit order directly at the boundary of the newly formed Balanced Price Range (BPR).
*   **IOFED Entry Protocols:** When trading high-momentum trends using the Institutional Order Flow Entry Drill (IOFED), enter limit orders directly at the proximal edge of the FVG, and adjust risk to account for potential drawdowns to the Consequent Encroachment (50% midpoint) level.
*   **Order Flow Absorption:** When price reaches a key HTF Point of Interest (POI), verify passive institutional absorption using a low-timeframe (1m/3m) footprint chart to confirm a cumulative delta divergence before executing.
*   **60-Minute Macro Windows:** Restrict active entry executions strictly to the designated high-volatility 60-minute algorithmic macro windows within the session Killzones.

## Red Flags

| Domain-Specific Rationalizations | Why Wrong |
| :--- | :--- |
| "I'll enter a reversal trade at this order block during the late afternoon session because the setup looks perfect." | Late afternoon (post-NY AM) is characterized by low institutional volume and algorithmic flatlining, leading to choppy stop-outs and spread expansions. |
| "This mitigation block will hold because it represents a clear change of character on the 15-minute chart." | Mitigation blocks lack a preceding liquidity sweep (stop hunt) to engineer the required fuel, resulting in a low-probability structure that is easily breached. |
| "I should buy this bullish breakout above the Asian high during the London open." | The initial move during the London open is typically the Judas Swing (manipulation) designed to sweep Asian range liquidity and trap breakout traders before reversing. |
| "Both EURUSD and GBPUSD broke their previous daily highs, so the uptrend is strongly confirmed." | Symmetrical sweeps indicate a standard trend move; look for non-symmetrical SMT divergence where one fails to sweep to confirm true institutional accumulation/distribution. |
| "This single FVG is deep, so I will set my limit order at the very bottom and wait." | Standard single FVGs act as magnets and can drag price deep into their voids; use Balanced Price Ranges (BPRs) for low-drawdown entries since orders there are already neutralized. |

## Quick Reference

| Phase / Setup | Session Window (EST) | Action / Execution Protocol |
| :--- | :--- | :--- |
| **Asian Accumulation** | 8 PM – 12 AM EST | Do not trade; define and map range high/low boundaries. |
| **London Manipulation** | 2 AM – 5 AM EST | Watch for the Judas Swing (Asian range sweep); target SMT divergence. |
| **NY Distribution** | 7 AM – 12 PM EST | Enter with the true expansion trend towards HTF liquidity targets. |
| **Unicorn Setup** | Killzone Specific | Execute at the horizontal overlap of a Breaker Block and an FVG. |
| **Venom Setup** | Post-HTF Sweep | Enter limit directly at the Balanced Price Range (BPR) boundary. |
| **IOFED Setup** | Strong HTF Trend | Enter at the proximal edge of the FVG; set stop loss beyond structural swing. |