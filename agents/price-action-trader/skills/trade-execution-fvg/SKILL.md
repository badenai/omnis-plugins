---
name: trade-execution-fvg
description: Use when analyzing or executing trades based on Advanced PD Arrays, including Fair Value Gaps (FVG), Inverse FVGs (IFVG), Balanced Price Ranges (BPR), Suspension Blocks, the Institutional Order Flow Entry Drill (IOFED), and advanced entry models (Unicorn, Reaper Inversion).
---

## The Iron Law

```
NEVER EXECUTE AN ENTRY OUTSIDE OF A DESIGNATED KILL ZONE (LONDON OPEN: 2:00-5:00 AM ET, NY OPEN/SILVER BULLET: 8:30-11:00 AM ET, NY PM: 1:30-4:00 PM ET) OR WITHOUT AN ACTIVE HIGH-PROBABILITY PD ARRAY INTERACTION.
```

## Behavioral Rules

*   **Validate Fair Value Gaps (FVG):** Identify a three-candle price imbalance where the wicks of the first and third candles do not overlap.
*   **Flip Invalidated FVGs to Inverse FVGs (IFVG):** When a candle closes completely past an FVG boundary, immediately treat that level as a structural support/resistance flip.
*   **Map Balanced Price Ranges (BPR):** Mark overlapping bullish and bearish FVGs horizontally to establish algorithmic equilibrium. Treat BPRs as highly reactive, tight targets expecting minimal drawdown.
*   **Identify Suspension Blocks:** Look for a specialized candlestick suspended between an upper and lower volume imbalance, where the body is completely overlapped by the wick of the prior candle on its left. Treat the body-and-twin-imbalance zone as a high-probability institutional re-load area.
*   **Execute the Institutional Order Flow Entry Drill (IOFED):** Place limit orders directly at the proximal edge of an FVG rather than waiting for a 50% consequent encroachment fill when trading fast-moving, high-momentum trends.
*   **Classify Failed Order Blocks:**
    *   **Breaker Blocks:** Require a successful sweep of a key liquidity extreme (stop hunt) followed by a Market Structure Shift (MSS) before executing on the failed order block.
    *   **Mitigation Blocks:** Identify trend exhaustion via a failure swing (failing to sweep the previous extreme) before executing on the failed order block, applying tighter risk parameters.
*   **Uncover Hidden Order Blocks (HOB):** When analyzing overlapping wicks of consecutive same-color candles on a higher timeframe (HTF), drill down to a lower timeframe (LTF) inside that wick-overlap zone to locate the unmitigated traditional order block.
*   **Execute the ICT Unicorn Model:** Enter only when an ICT Breaker Block horizontally overlaps an energetic ICT Fair Value Gaps (FVG) where the FVG resides directly within the price range of the breaker block.
*   **Execute the ICT Reaper Inversion FVG:** Align the Inversion FVG precisely inside the impulsive price leg of a breaker block. Validate that the "Reaper" sits in the discount portion for bullish setups, or the premium portion for bearish setups.
*   **Execute the Venom Model:** Trigger immediate market or limit entries at the boundary of a newly formed Balanced Price Range (BPR) following a major liquidity sweep strictly within session Kill Zones.
*   **Confirm Liquidity Sweeps Volumetrically:** Verify true institutional sweeps on a footprint chart via diagonal bid/ask imbalances exceeding a 3:1 ratio (absorption) accompanied by passive limit orders and immediate price rejection.
*   **Validate Structural Shifts vs. Inducement:** Confirm Breaks of Structure (BOS) or Changes of Character (CHOCH) only when accompanied by aggressive, high-delta volume. Classify breakouts with neutral or exhausted volume delta as Inducement (IDM) traps and avoid early entries.

## Red Flags

| Red Flag | Why it is Wrong |
| :--- | :--- |
| **Entering trades mid-session outside Kill Zones** | Retail algorithms hunt liquidity and generate choppy, non-directional noise outside of institutional hours, leading to papercuts. |
| **Using lagging indicators to confirm FVG reactions** | RSI, MACD, or Bollinger Bands diverge from immediate transactional order flow and lag behind raw price-delivery algorithms. |
| **Treating an invalidated FVG as a loss of bias** | Failing to recognize an Inverse FVG (IFVG) role-reversal causes traders to miss immediate institutional support/resistance flips. |
| **Applying footprint volume profiles blindly to OTC Spot Forex** | Spot FX lacks a centralized exchange; localized broker tick-volume data acts as a proxy and can generate false absorption signals. |
| **Ignoring the discount/premium rule for the Reaper Inversion FVG** | Entering a bearish Reaper setup in a discount array (or bullish in premium) results in poor risk-to-reward ratios and high drawdown. |

## Quick Reference

| PD Array / Setup | Structural Core | Target / Entry Mechanic |
| :--- | :--- | :--- |
| **Fair Value Gaps (FVG)** | 3-candle price imbalance (no wick overlap) | Magnetic draw; Entry at proximal boundary or 50% CE |
| **Inverse FVG (IFVG)** | FVG invalidated by a complete candle close past its boundary | Role-reversed boundary acts as a support/resistance flip |
| **Balanced Price Range (BPR)** | Horizontally overlapping bullish and bearish FVGs | High-precision entry/target; absolute algorithmic equilibrium |
| **Suspension Block** | Body suspended between dual volume imbalances, overlapped by prior wick | High-probability institutional re-load zone |
| **IOFED Drill** | High-momentum directional trend | Immediate limit order at proximal edge of FVG (no CE wait) |
| **ICT Unicorn Model** | Horizontal overlap of a Breaker Block and an FVG | Dual-pressure confirmation zone for highly asymmetric R:R |
| **Reaper Inversion FVG** | Inversion FVG inside a breaker block's impulsive leg | Entry at the Inversion FVG (must align with Premium/Discount) |
| **Venom Model** | Session Kill Zone + Liquidity Sweep + BPR formation | Execution directly at the BPR boundary targeting HTF liquidity |