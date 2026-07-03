---
name: trade-execution-fvg
description: Use when validating, refining, and executing trade setups using advanced price action entry models including the ICT Unicorn Model, Balanced Price Ranges (BPR), Inverse Fair Value Gaps (IFVG), and Institutional Order Flow Entry Drills (IOFED).
---

## The Iron Law

```
NEVER execute an FVG, BPR, or Unicorn setup if the displacement candle body-to-wick ratio is below 70%, or if the setup forms without a confirmed higher-timeframe liquidity sweep.
```

## Behavioral Rules

*   **Enforce Body-to-Wick Ratios:** Only execute setups where the displacement candle body-to-wick ratio is 70% or greater. If the ratio is under 60%, reject the setup immediately due to statistically degraded reward outcomes (1.3R vs. 2.1R average).
*   **Execute the ICT Unicorn Model:** 
    *   Verify a liquidity sweep has occurred, followed by an aggressive displacement leg causing a Market Structure Shift (MSS).
    *   Isolate the exact horizontal overlap where the newly formed FVG sits within the boundaries of the Breaker Block.
    *   Place limit orders directly at this overlapping dual-pressure boundary.
    *   Set the stop-loss strictly beyond the FVG-forming candle body or the Breaker swing extreme.
*   **Map Balanced Price Ranges (BPR):** 
    *   Locate where a bullish FVG and a bearish FVG overlap horizontally.
    *   Treat this zone as an immediate algorithmic rebalance. 
    *   Place limit entries on the first retest of this overlap zone, anticipating instant price rejection.
*   **Validate Inverse FVGs (IFVGs):** 
    *   Wait for a candle body to close completely past the boundary of a traditional FVG to confirm its inversion.
    *   Once confirmed, flip the bias of the zone (support turns to resistance, or vice versa).
    *   Set invalidation levels strictly behind the candle body that closed past and invalidated the original FVG.
*   **Execute Institutional Order Flow Entry Drills (IOFED):**
    *   Enter trades directly at the proximal edge of the FVG in high-momentum conditions.
    *   Invalidate the trade immediately if price prints a candle body close past 50% consequent encroachment (CE) of the FVG.
*   **Identify Hidden Order Blocks (HOB):**
    *   Scan higher-timeframe (HTF) charts for overlapping candle wicks.
    *   Refine down to lower-timeframe (LTF) charts to identify the fully-formed order block hidden within those wicks.
    *   Use the LTF OB boundaries for surgical entry placement.
*   **Differentiate Breakers vs. Mitigation Blocks:**
    *   Prioritize Breaker Blocks because they are anchored by a high-velocity liquidity sweep.
    *   If trading a Mitigation Block, reduce position sizing by 50% and apply tighter stop-losses to protect capital against trend fatigue and subsequent stop-runs.

## Red Flags

| Red Flag | Why It Is Wrong |
| :--- | :--- |
| **Trading low-displacement FVGs** | Candles with wicks exceeding 30% of their total range represent low institutional interest and drop average returns to 1.3R. |
| **Placing limit orders outside Breaker/FVG overlaps** | Entering outside the Unicorn overlap zone forfeits the dual-pressure structural cushion, increasing execution drawdown. |
| **Allowing IOFED to violate Consequent Encroachment** | If price closes past 50% of the FVG, the trend lack urgency; holding the trade violates the core assumption of strong institutional order flow. |
| **Trading Mitigation Blocks with standard risk** | Mitigation blocks lack a prior liquidity sweep (failure swing), making them highly vulnerable to being run over during subsequent liquidity grabs. |
| **Entering IFVGs on wick-only breaches** | Wicks past an FVG are liquidity grabs, not structural invalidations; only a full candle body close confirms an Inverse FVG flip. |

## Quick Reference

| Model | Key Trigger Criteria | Stop-Loss / Invalidation |
| :--- | :--- | :--- |
| **Unicorn Model** | Liquidity sweep + MSS + FVG overlapping a Breaker Block. | Beyond the FVG-forming candle or the Breaker extreme. |
| **Balanced Price Range (BPR)** | Horizontally overlapping bullish & bearish FVGs (body-to-wick > 70%). | Beyond the boundary of the opposing FVG candle. |
| **Inverse FVG (IFVG)** | HTF/LTF candle body closes completely past an existing FVG zone. | Beyond the high/low of the invalidating candle. |
| **IOFED** | Entry at the proximal FVG edge during high-momentum trends. | Any candle body close past 50% Consequent Encroachment (CE). |
| **Hidden Order Block (HOB)** | Overlapping wicks on HTF that resolve to clean OBs on LTF. | Beyond the HTF wick extreme. |