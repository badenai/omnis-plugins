---
name: trade-execution-fvg
description: Use when identifying market imbalances (FVGs, BISI, SIBI), determining Consequent Encroachment (CE), evaluating Balanced Price Ranges (BPR), or executing trades using precise price action entry techniques like IOFED, OTE, the ICT Unicorn, and Venom models.
---

## The Iron Law

```
Never execute a trade based on a Fair Value Gap (FVG) or Balanced Price Range (BPR) in isolation. Every execution must align with a Higher Timeframe (HTF) Draw on Liquidity, occur strictly within a designated Session Killzone, and be triggered by a confirmed Lower Timeframe (LTF) structural shift or liquidity sweep.
```

## Behavioral Rules

*   **Determine Imbalance Type:** Classify the market imbalance precisely. Label a buying imbalance as a Buyside Imbalance Sellside Inefficiency (BISI) and a selling imbalance as a Sellside Imbalance Buyside Inefficiency (SIBI).
*   **Locate Consequent Encroachment (CE):** Calculate and map the exact 50% midpoint of any FVG or BPR. Use this level as your primary reactive execution point for low-risk limit orders.
*   **Manage Failed FVGs (IFVGs):** If a candle body closes decisively through the boundary of a validated FVG, immediately reclassify the zone as an Inverse Fair Value Gap (IFVG) and flip its structural polarity (support becomes resistance, and vice versa).
*   **Identify Balanced Price Ranges (BPR):** Locate areas where a bullish FVG and a bearish FVG directly overlap horizontally. Treat this zone as an immediate algorithmic magnet and utilize its outer boundaries as robust invalidation levels.
*   **Apply the Institutional Order Flow Entry Drill (IOFED):** Under high-momentum conditions where deep retracements to CE are unlikely, execute limit orders directly at the proximal edge of the FVG to prevent missing the expansion leg.
*   **Filter by Candle Quality:** Only execute setups on FVGs, BPRs, or displacement legs where the candle body-to-wick ratio is at least 70%. Reject any setups formed by weak, high-wick candles (under 60% body ratio).
*   **Execute the ICT Unicorn Model:** Verify that a session-based liquidity sweep has occurred, confirm a displacement leg creating a Market Structure Shift (MSS), locate the direct horizontal overlap of an ICT Breaker Block and an FVG, and place the entry limit order strictly within a Session Killzone.
*   **Execute the Venom Model:** Locate a horizontal overlap of a bullish and bearish FVG (BPR) forming immediately after a major liquidity sweep during a predetermined session Killzone. Place entry orders precisely at the boundary of the BPR, targeting HTF external liquidity.
*   **Align with OTE (Optimal Trade Entry):** Use the Fibonacci tool to map the 0.618 to 0.79 retracement of the most recent impulsive swing leg. Only execute if the OTE zone overlaps directly with a pre-existing HTF PD Array (such as an unmitigated Order Block or FVG) after a clear liquidity sweep.
*   **Enforce Time Alignment:** Restrict all trade executions to active ICT Killzones (London Open: 2:00 AM – 5:00 AM ET; NY Open/Silver Bullet: 8:30 AM – 11:00 AM ET; NY PM Session: 1:30 PM – 4:00 PM ET). Do not execute new trades outside of these windows.

## Red Flags

| Deficient Action / Belief | Rationalization | Why It Is Wrong |
| :--- | :--- | :--- |
| Trading every FVG on the chart | "The price always fills gaps, so this is an easy reversal setup." | FVGs traded without HTF Draw on Liquidity and session alignment have a statistically negative expectancy and result in heavy losses. |
| Placing stops inside the FVG | "I want a super tight stop-loss to get a massive risk-to-reward ratio." | Algorithmic delivery frequently tests the 50% Consequent Encroachment (CE) or sweeps the outer FVG boundary before expanding. Stops must go beyond structural invalidation levels. |
| Ignoring candle body closes through FVGs | "It just swept the level and will reverse back in my direction." | A decisive candle body close straight through an FVG invalidates it, converting the zone into an Inverse FVG (IFVG). Ignoring this means trading against order flow. |
| Executing trades on low-body candles | "The gap is huge, so the displacement is strong." | If the candle body-to-wick ratio is under 60%, the move lacks institutional backing and represents exhaustion rather than true displacement. |
| Mid-day trading outside Killzones | "The setup looks perfect, I don't need to wait for NY or London Open." | Volume and volatility are thin outside of session Killzones; algorithms consolidate price, leading to stop hunts and failed executions. |

## Quick Reference

| Concept | Definition / Formula | Execution Trigger / Action |
| :--- | :--- | :--- |
| **BISI** | Buyside Imbalance Sellside Inefficiency | Look for bullish expansion; entry at proximal boundary or CE on retest. |
| **SIBI** | Sellside Imbalance Buyside Inefficiency | Look for bearish expansion; entry at proximal boundary or CE on retest. |
| **Consequent Encroachment (CE)** | 50% Midpoint of an FVG or BPR | Place low-risk limit orders at this exact mathematical equilibrium level. |
| **Inverse FVG (IFVG)** | FVG breached by a decisive candle body close | Flip bias; trade the retest of the boundary as flipped support/resistance. |
| **BPR** | Horizontally overlapping bullish and bearish FVGs | Immediate entry at the boundaries; highly robust invalidation zones. |
| **IOFED** | Limit order placed precisely at the proximal edge of FVG | Use during high-momentum runs to capture fast-moving expansion legs. |
| **ICT Unicorn Model** | Horizontal overlap of a Breaker Block + FVG | Execute in Killzone after a session liquidity sweep and MSS displacement. |
| **Venom Model** | Horizontally overlapping FVGs (BPR) after a sweep | Execute at the BPR boundary targeting HTF external liquidity pools. |
| **OTE** | 61.8% – 79.0% Retracement range (70.5% Sweet Spot) | Execute when OTE overlaps an unmitigated HTF FVG/OB after a sweep. |