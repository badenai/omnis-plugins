---
name: trade-execution-fvg
description: Use when executing trades utilizing Fair Value Gaps (FVGs), Consequent Encroachment (CE), Inverse FVGs (iFVGs), and Balanced Price Ranges (BPR) to capitalize on algorithmic imbalances and institutional pricing equilibrium.
---

## The Iron Law

```text
Define a Balanced Price Range (BPR) strictly as the overlapping zone of consecutive bullish and bearish FVGs formed by violent, back-to-back displacement. If a candle body closes beyond the outer boundary of this BPR, immediately invalidate the setup and exit all active positions.
```

## Behavioral Rules

*   **Execute IOFED on High-Velocity Legs:** If price prints a hyper-displaced expansion leg, place limit orders directly at the proximal edge of the FVG instead of waiting for a 50% retracement.
*   **Target Consequent Encroachment on Normal Volatility:** If price approaches a standard FVG under normal volatility, set your entry trigger at the Consequent Encroachment (50% midpoint) level.
*   **Monitor Close Relative to CE:** Monitor the candle body close relative to the Consequent Encroachment (CE); if a candle body closes beyond the CE level, discard the FVG as a high-probability support or resistance zone.
*   **Execute BPRs Inside Macro Windows:** When executing the Venom Model, place your limit order directly at the boundary of the BPR during a designated 60-minute macro window.
*   **Pivot on iFVG Confirmations:** If a candle body closes entirely through an active FVG, immediately reclassify it as an Inverse FVG (iFVG) and trade it as a support/resistance level on the subsequent retest.
*   **Execute Unicorn Setup on Key Overlaps:** Execute the Unicorn Model only when a fresh Breaker or Mitigation Block directly overlaps with a newly formed FVG or iFVG.
*   **Enforce Premium/Discount Filters:** Filter all imbalance setups by premium/discount parameters; do not buy BISIs (Buyside Imbalance Sellside Inefficiencies) in premium zones, and do not sell SIBIs (Sellside Imbalance Buyside Inefficiencies) in discount zones.

## Red Flags

| Retail Rationalization | Why It Is Algorithmically Wrong |
| :--- | :--- |
| "Wait for the 50% CE level on this hyper-displaced leg to secure a perfect entry." | "Understand that rapid algorithmic expansion often leaves you behind if you do not enter at the proximal edge (IOFED)." |
| "Enter on this clean FVG despite price trading deep within premium/discount territory." | "Do not ignore HTF premium/discount arrays, as executing here forces you to chase late-stage retail momentum." |
| "Classify these overlapping consolidations as a high-probability BPR." | "Require violent, back-to-back opposite-direction displacement to form a true BPR; otherwise, you are trading noise." |
| "Hold the trade because price only closed slightly past the BPR boundary." | "Exit immediately if a body closes past the BPR boundary, as this signifies that the algorithmic equilibrium is completely compromised." |
| "Execute entries on 1-minute FVGs regardless of HTF structure." | "Ensure the lower-timeframe FVG aligns directly with a higher-timeframe POI or major liquidity sweep to avoid trading noise." |

## Quick Reference

| Setup Type | Algorithmic Trigger Condition | Execution Action | Absolute Invalidation |
| :--- | :--- | :--- | :--- |
| **Standard FVG (BISI/SIBI)** | If price retraces into a fresh, unmitigated FVG | Place the entry order at the proximal edge or CE | Exit if a candle body closes past the FVG boundary |
| **Consequent Encroachment (CE)** | If price seeks high-liquidity midpoint equilibrium | Set limit order precisely at the 50% midpoint | Exit if a candle body closes beyond the 50% level |
| **Balanced Price Range (BPR)** | If overlapping BISI and SIBI form via dual displacement | Place limit order at the outer boundary of the BPR | Exit if a candle body closes past the BPR boundary |
| **Unicorn Model** | If a fresh Breaker Block overlaps with an FVG or iFVG | Place entry order at the direct intersection of both arrays | Exit if a body closes past the Breaker's invalidation level |
| **IOFED Precision** | If extreme velocity creates a heavily displaced FVG | Set limit order at the absolute proximal edge immediately | Exit if price fails to reject instantly on the first touch |