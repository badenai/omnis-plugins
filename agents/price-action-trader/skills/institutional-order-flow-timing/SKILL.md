---
name: institutional-order-flow-timing
description: Use when analyzing algorithmic market timing, session killzones, AMD (Accumulation, Manipulation, Distribution) cycles, or footprint order flow dynamics.
---

## The Iron Law

```text
Never execute a trade based solely on price levels without first aligning with institutional session timing (Killzones) and verifying algorithmic involvement via order flow absorption or initiation. Time dictates price delivery.
```

## Behavioral Rules

*   **AMD Validation:** Require a clear Accumulation phase (typically Asian session), wait for Manipulation (London Judas Swing) to sweep resting liquidity, and trade only the subsequent Distribution phase (New York expansion).
*   **Macro Window Execution:** Restrict active charting and trade execution to specific 60-minute high-volatility "Macro" windows (e.g., London Open, NY AM) to capture pure algorithmic displacement.
*   **Footprint Confirmation:** Validate Order Blocks and Balanced Price Ranges (BPR) using Level 2 footprint data by confirming Absorption (heavy bid/ask volume failing to advance price) immediately followed by Initiation (Delta divergence in the reversal direction).
*   **Judas CHOCH Application:** If a perfect, time-aligned liquidity sweep and 1-minute displacement setup occurs strictly within a Killzone macro window, execute the setup mechanically even if it conflicts with higher-timeframe structural bias.
*   **Wyckoff Volume Verification:** Utilize tick volume as a Volume Spread Analysis (VSA) proxy to confirm institutional effort and validate Spring (SSL sweep) or Upthrust (BSL sweep) mechanics during session transitions.
*   **Avoid Blind Limits:** Abandon predictive standard limit orders at standard Order Blocks; transition entirely to reactive entries triggered by real-time order flow shifts at the Point of Interest (POI).

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "This Order Block is perfectly formed, I am placing a blind limit order here." | Blind limits ignore real-time order flow; elite execution requires footprint absorption validation to prevent being run over by algorithmic drawdowns. |
| "I am taking the Asian session breakout because momentum is building." | The Asian session is algorithmically programmed for order accumulation; breakouts are engineered traps designed to build liquidity for the London manipulation sweep. |
| "The structural FVG is clean, so the time of day does not matter." | Price patterns devoid of session Killzone alignment lack the algorithmic volume injections required for sustained structural distribution. |
| "The footprint shows massive buy volume at the highs, I must go long." | Heavy volume at a high that fails to push price forward is Absorption (retail limit orders trapped by institutional sellers), signaling a short reversal. |

## Quick Reference

| Institutional Concept | Timing / Condition | Required Action |
| :--- | :--- | :--- |
| **Accumulation (A)** | Asian Session | Map resting liquidity boundaries; do not trade breakouts. |
| **Manipulation (M)** | London Open Killzone | Wait for the "Judas Swing" to sweep Asian liquidity pools. |
| **Distribution (D)** | New York Session | Execute in the direction of post-sweep displacement toward unmitigated external liquidity. |
| **Footprint Reversal** | Price hits structural POI | Wait for Absorption (trapped volume) + Initiation (Delta divergence) before entry. |
| **Macro Execution** | 60-min High-Vol Windows | Scan exclusively for mechanical "Judas CHOCH" setups and execute without hesitation. |