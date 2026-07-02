---
name: market-structure-liquidity
description: Use when analyzing market trends, validating structural shifts (BOS, CHOCH, IDM), identifying institutional price delivery arrays (Order Blocks, FVGs, BPRs, Breaker Blocks), and tracking liquidity sweeps, session Killzones (AMD), or footprint absorption dynamics.
---

## The Iron Law
```text
Never validate a market structure shift (MSS/CHOCH) or institutional order block (OB) unless it is preceded by a clear liquidity sweep of a major high/low and accompanied by aggressive, displaced candle bodies (body-to-wick ratio > 70%) that leave behind a valid Fair Value Gap (FVG).
```

## Behavioral Rules

1. **Verify Structural Shifts (CHOCH vs. IDM):**
   * Do not classify a high/low break as a Change of Character (CHOCH) unless the candle delivers a clean body close past an external swing level with aggressive displacement.
   * Classify any minor internal high/low breaks or simple wick rejections past a level as Inducement (IDM) rather than a structural shift.

2. **Differentiate Breakers from Mitigation Blocks:**
   * Treat a failed Order Block as a high-probability Breaker Block *only* if the block was preceded by a clear liquidity sweep (stop hunt) before reversing.
   * Treat a failed Order Block as a lower-probability Mitigation Block if it was formed via a failure swing (failing to sweep the previous extreme); enforce tighter risk limits or require HTF POI confirmation for these setups.

3. **Validate Balanced Price Ranges (BPR):**
   * Filter out BPR/FVG entries where the displacement candles exhibit a body-to-wick ratio below 70%. Only execute when the ratio exceeds 70% to maintain a higher mathematical expectancy.

4. **Execute IOFED Entries with Precision:**
   * Execute Limit Orders directly at the proximal edge of the Fair Value Gap (FVG) when utilizing the Institutional Order Flow Entry Drill (IOFED). 
   * Stop out immediately if the price violates the 50% consequent encroachment level of the FVG, as the algorithm must respect this level to confirm high-momentum delivery.

5. **Execute Multi-Timeframe Footprint Convergence:**
   * Always follow the strict three-step execution workspace sequence:
     1. Locate High Volume Nodes (HVNs) or key liquidity pools on a **30-minute chart**.
     2. Zoom to a **5-minute footprint** to monitor real-time absorption (e.g., massive aggressive delta spikes failing to move price) and diagonal bid/ask imbalances.
     3. Confirm entry via **1-minute Cumulative Volume Delta (CVD)** divergences.

6. **Align with Session Killzones & AMD/AMDX:**
   * Only execute trades during designated session Killzones.
   * Map the Daily Cycle strictly according to the Power of Three (AMD):
     * **Accumulation (A):** Map the tight trading range formed during the low-volume Asian session.
     * **Manipulation (M):** Look for false breakouts sweeping the Asian range extremes during the London session (Judas Swing).
     * **Distribution (D):** Execute the true trend expansion and reversal off the London manipulation leg during the New York session.

## Red Flags

| Red Flag | Rationalization | Why Wrong |
| :--- | :--- | :--- |
| **Trading "BOS" on Wick Breaks** | "The price swept past the old high, so the trend must be continuing upward." | **Structure Trap.** Wicks represent rejection and liquidity sweeps, not structural continuation. True BOS requires a displacement body close. |
| **Buying Every Unmitigated OB** | "Every Order Block represents institutional buying or selling that must be mitigated." | **Liquidity Inducement.** Without a preceding liquidity sweep and aggressive displacement (leaving an FVG), retail order blocks act as target liquidity. |
| **Trading Outside Killzones** | "The setup looks perfect on a 15m chart, even if it is during the mid-day lull." | **Low Probability.** Volume and institutional participation drop outside Killzones, resulting in high-slippage, range-bound traps and false breakouts. |
| **Chasing IOFED with Deep Stops** | "I will place my stop below the swing low just in case the FVG gets fully filled." | **Risk Invalidation.** The entire edge of the IOFED model relies on high-momentum algorithmic preservation of the FVG's proximal edge. Deep retracements invalidate the setup. |

## Quick Reference

| Concept | Key Metric / Trigger | Target / Stop Rules | Risk Weight |
| :--- | :--- | :--- | :--- |
| **Unicorn Entry** | Breaker Block overlapping a high-displacement FVG | Stop behind Breaker; Target external liquidity | High |
| **High-Quality BPR** | Body-to-wick ratio > 70% on displacement candles | Stop behind the BPR boundary; Target next key level | High |
| **IOFED Drill** | Immediate execution at FVG proximal edge | Tight stop at 50% Consequent Encroachment | Moderate (Asymmetric) |
| **True CHOCH** | External swing level broken by solid body close | Stop below the displacement leg origin | High |
| **Inducement (IDM)** | Internal liquidity sweep (wicks past structural levels) | Avoid trading; wait for sweep of IDM before entering | Low (Filter) |
| **Power of Three (AMD)** | London sweep of Asian range extreme | Entry on manipulation rejection; target NY distribution | High |