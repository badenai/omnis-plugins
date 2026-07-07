---
name: institutional-order-flow-timing
description: Use when analyzing market structure transitions, locating order block variations (Breakers, Mitigation, Hidden, Suspension Blocks), validating imbalances (FVGs, IFVGs, BPRs), identifying liquidity pools, or timing trade executions within algorithmic session Killzones (London, NY, Silver Bullet, AMD/Quarterly Theory).
---

## The Iron Law

```
All institutional order blocks, fair value gaps, and structural transitions are completely invalid unless they are initiated by a Higher Timeframe (HTF) liquidity sweep and executed strictly within a designated session Killzone (London Open, New York Open/Silver Bullet, or New York PM).
```

## Behavioral Rules

1. **Verify HTF Liquidity Sweeps First**: Do not look for lower-timeframe entry setups unless the Higher Timeframe (HTF) Draw on Liquidity (BSL or SSL) has been swept or tapped. 
2. **Apply Two-Timeframe Hierarchy Strictly**: Always define the HTF key zone (e.g., 4-Hour) first, then zoom down exactly two intervals (e.g., 15-Minute) for execution setup identification. Do not jump arbitrarily between random timeframes.
3. **Validate Structural Breaks by Body Closes Only**: Define a Change of Character (CHOCH) or Market Structure Shift (MSS) strictly by a candle body closing past the major external swing level. If only the wick breaks the level, classify it as Inducement (IDM) or a Liquidity Sweep, and do not execute trend-reversal orders.
4. **Distinguish Breaker Blocks (BB) from Mitigation Blocks (MB)**: 
   * *Condition*: If the failed order block swept liquidity before the structural shift, classify it as a Breaker Block (BB) and trade it as a high-velocity, structurally robust level.
   * *Condition*: If the failed order block was created by a failure swing (exhaustion) without sweeping the extreme, classify it as a Mitigation Block (MB) and apply tighter risk management.
5. **Classify Order Block Exceptions (HOB & Suspension Blocks)**:
   * *Condition*: If identifying unmitigated zones on daily/weekly charts that look like standard wicks, drill down to lower timeframes to locate Hidden Order Blocks (HOB) for high-precision entries.
   * *Condition*: If price is suspended between two volume imbalances with zero wick-to-wick gap but the body is overlapped by the prior wick, trade it as a Suspension Block.
6. **Classify and Map Imbalances**:
   * *Condition*: If a standard FVG fails to hold and experiences a decisive candle body close through its boundaries, reclassify it immediately as an Inverse Fair Value Gaps (IFVG) and flip your directional bias.
   * *Condition*: If a bullish FVG and a bearish FVG overlap horizontally, label the zone as a Balanced Price Range (BPR) and use its outer boundaries as robust invalidation levels.
7. **Determine Entry Mechanics (IOFED vs. CE)**:
   * *Condition*: In high-momentum conditions (candle body-to-wick ratio > 70%), utilize the Institutional Order Flow Entry Drill (IOFED) by placing a limit order at the proximal edge of the FVG.
   * *Condition*: In standard retracements, place the limit entry at the Consequent Encroachment (CE) (the exact 50% midpoint) of the FVG.
8. **Enforce Temporal Killzones**: Reject any execution setup that occurs outside the algorithmic windows: London Open (2:00 AM – 5:00 AM ET), NY Open/Silver Bullet (8:30 AM – 11:00 AM ET), or NY PM Session (1:30 PM – 4:00 PM ET).
9. **Apply the Power of Three (AMD)**: Track the daily cycle as Accumulation (Asia range consolidation), Manipulation (London Judas Swing sweeping Asia extremes), and Distribution (NY trend expansion). Apply Quarterly Theory (AMDX) to avoid entering late-session trends during the "X" phase.
10. **Validate Sweeps via Footprint/DOM Absorption**: Confirm a liquidity sweep in real-time only when a high delta spike is met by passive limit order stacking, resulting in a candle stalling/reversing rather than expanding (e.g., candle closes bullish despite a highly negative net Delta).
11. **Abide by the Three-Mistake Rule**: Terminate trading and shut down the execution platform immediately upon committing three operational errors (such as trading outside Kill Zones, manually widening a stop, or violating sizing rules).

## Red Flags

| Red Flag | Why Wrong |
| :--- | :--- |
| **Trading LTF structure in isolation** | Statistically negative expectancy; the 1m/5m structural changes are noise without HTF parent POI alignment. |
| **Labeling a wick-only break as CHOCH** | Classic retail trap; wicks represent liquidity sweeps/inducement, not a true market structure shift (which requires body closes). |
| **Entering trades during the "X" Phase** | Entering late-session distributions during AMDX leads to trading exhausted trends right before reversal. |
| **Placing orders on low-quality FVGs** | Imbalances with candle body-to-wick ratios below 60% show weak institutional momentum, dropping average performance to 1.3R. |
| **Using fixed pip/percent risk in high volatility** | Fails to account for dynamic institutional delivery; must adapt leverage using contract-based exposure / floating risk rules. |

## Quick Reference

### PD Array & Timing Alignment Matrix

| Phase / Concept | Temporal Window (ET) | Primary Structural Focus | Validation Criteria |
| :--- | :--- | :--- | :--- |
| **London Open** | 2:00 AM – 5:00 AM | Judas Swing / Manipulation | Sweeps Asian session extremes, forms BB/MB |
| **New York Open** | 8:30 AM – 11:00 AM | Silver Bullet / Distribution | MSS + displacement FVG or Unicorn Model |
| **New York PM** | 1:30 PM – 4:00 PM | Late Session Reversal / Expansion | Sweeps NY AM session highs/lows, targets PM liquidity |
| **Power of Three (AMD)** | Daily Cycle | Accumulation $\rightarrow$ Manipulation $\rightarrow$ Distribution | Daily high/low formed during London; NY distributes |
| **Balanced Price Range** | Any (during Killzone) | Overlapping Bullish & Bearish FVGs | Immediate horizontal overlap, body-to-wick ratio > 70% |
| **Unicorn Model** | Session-specific | Breaker Block (BB) + FVG Overlap | MSS displacement leg; invalidation beyond sweep anchor |
| **Consequent Encroachment**| Any | 50% Midpoint of FVG | Precise mathematical midpoint reaction |