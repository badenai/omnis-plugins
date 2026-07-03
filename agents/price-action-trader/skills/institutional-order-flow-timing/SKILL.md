---
name: institutional-order-flow-timing
description: Use when analyzing market structure shifts, institutional order blocks, liquidity sweeps, fair value gaps, and execution timing within London, New York, or Asian session Killzones.
---

## The Iron Law

```
Never execute a trade position unless the setup resides within an active, session-specific Killzone (London, NY, Asia) and is triggered by a direct manipulation of liquidity (sweep or failure swing) at a high-timeframe Point of Interest.
```

## Behavioral Rules

*   **Enforce Time-of-Day Parameters:** If price action develops outside of designated Killzone windows (London: 02:00–05:00 EST, New York: 07:00–10:00 EST, Asia: 20:00–00:00 EST), you must treat the movement as low-probability consolidation or retail bait and decline execution.
*   **Evaluate Order Flow Over Refinement:** You must prioritize the broader Order Flow (the entire corrective leg preceding a BOS) over highly refined, single-candle Order Blocks to prevent missing institutional entry windows.
*   **Verify Unicorn Model Overlaps:** When executing a Unicorn setup, you must confirm that the Fair Value Gap (FVG) horizontally overlaps the exact price boundary of the newly formed Breaker Block.
*   **Analyze Breaker vs. Mitigation Context:** You must classify a structural block as a high-probability Breaker Block *only* if it is preceded by a completed liquidity sweep (stop hunt). If a block forms from a failure swing without sweeping liquidity, you must classify it as a Mitigation Block and enforce tighter risk parameters due to its lower structural reliability.
*   **Apply the Displacement Quality Filter:** You must measure the body-to-wick ratio of the displacement candle forming a FVG or Balanced Price Range (BPR). If the body-to-wick ratio is below 70%, you must reduce the setup's target projection to 1.3R (compared to 2.1R for ratios above 70%) or skip the entry.
*   **Confirm Sweeps with Volumetric Footprints:** When utilizing footprint charts to confirm a liquidity sweep, you must verify the presence of a diagonal bid/ask imbalance ratio exceeding 3:1 alongside a clear delta divergence (e.g., price closing bullish while net Delta is highly negative) to confirm institutional absorption.
*   **Execute the IOFED with Momentum Bias:** When applying the Institutional Order Flow Entry Drill (IOFED), you must place limit orders at the proximal boundary of the FVG (filling no more than 50% consequent encroachment) *only* during high-momentum trends where immediate continuation is statistically supported.
*   **Identify Hidden Order Blocks (HOB):** You must drill down to lower timeframes to locate fully formed, high-probability order blocks within the overlapping candle wicks of higher-timeframe charts.
*   **Integrate Wyckoff and Volume Profile:** You must align Wyckoff phases (Accumulation/Distribution) with Volume Profile Point of Control (POC) and High-Volume Nodes (HVNs) to establish structural targets.
*   **Apply the Process-Oriented Three-Mistake Rule:** You must immediately close execution platforms for the day if you commit three distinct operational errors (e.g., trading out-of-session, widening a stop-loss, or violating contract sizing).

## Red Flags

| Red Flag | Why it is Wrong |
| :--- | :--- |
| **Out-of-Session Execution** | Executing setups during low-volume mid-day doldrums, where algorithmic delivery targets are absent and spread widening occurs. |
| **Extreme OB Over-Refinement** | Demanding price tap a single lower-timeframe candle extreme, resulting in missing the broader, valid Order Flow mitigation. |
| **Blind Mitigation Block Entries** | Treating Mitigation Blocks as high-probability reversals without acknowledging that the absence of a liquidity sweep makes them prime targets for stop runs. |
| **Trading Low-Body Displacement** | Entering FVGs or BPRs formed by weak, wick-heavy candles (under 70% body ratio) that indicate lack of institutional displacement. |
| **Relying on "AI" Broker Alerts** | Substituting raw price and volume footprint analysis with lagging, retail-focused indicators rebranded as automated AI signals. |

## Quick Reference

| Session / Concept | Time Window (EST) / Metric | Core Structural Trigger | Target/Risk Action |
| :--- | :--- | :--- | :--- |
| **London Killzone** | 02:00 – 05:00 | Liquidity sweep of Asian session range extreme or PDH/PDL. | Target opposite liquidity pool. |
| **New York Killzone** | 07:00 – 10:00 | Reversal or continuation of London trend via Breaker/FVG overlap. | Target London session extreme or Daily bias. |
| **Asia Killzone** | 20:00 – 00:00 | Tactical range-bound sweeps; lower-volatility setups. | Enforce tight targets and trailing stops. |
| **The Unicorn Model** | Session-independent | Horizontal overlap of FVG and Breaker Block after a liquidity sweep. | Stop-loss placed past Breaker swing extreme. |
| **BPR Quality Filter** | Setup-dependent | Displacement candle body-to-wick ratio > 70%. | Target 2.1R minimum; reduce to 1.3R if ratio < 60%. |
| **IOFED Entry** | High-momentum trend | Immediate reversal upon tapping the proximal edge of an FVG (respects 50% CE). | Immediate entry at FVG boundary; tight stops. |