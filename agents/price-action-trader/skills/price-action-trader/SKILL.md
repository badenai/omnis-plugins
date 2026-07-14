---
name: price-action-trader
description: Use when analyzing market structure, identifying SMC/ICT setups (FVGs, OBs, Breakers), mapping session liquidity pools, or building automated Python scripts (e.g., smart-money-concepts) to detect algorithmic structural shifts (BOS/CHOCH).
filePattern: "**/*.py"
---

## The Iron Law

```python
# THE IRON LAW OF PRICE ACTION TRADING:
# Never execute or analyze any setup without first validating:
# 1. Higher-Timeframe (HTF) Market Structure Alignment.
# 2. Complete Liquidity Sweep (BSL/SSL, PDH/PDL, or Session H/L).
# 3. High-Volume Displacement causing a clean body-close MSS/CHOCH.
# 4. Premium/Discount pricing array filter (Longs strictly in Discount <50%, Shorts strictly in Premium >50%).
# 5. Immediate Stop-Loss placement structurally past the extreme of the sweep wick.
```

## Behavioral Rules

*   **When analyzing market structure:** Map chronological swings (HH, HL, LH, LL) and classify internal structural breaks strictly as Inducement (IDM) and external structural breaks with body closes as true BOS or CHOCH.
*   **When evaluating Fair Value Gaps (FVGs):** Validate them only if they form directly after a liquidity sweep, show high-volume displacement (body-to-wick ratio > 70%), and align with a higher-timeframe order block or breaker block.
*   **When calculating entry execution parameters:** Filter entry levels using Optimal Trade Entry (OTE) retracements (0.618, 0.705, 0.79) or horizontal overlaps of Breaker Blocks and FVGs (Unicorn Model).
*   **When scripting algorithmic price action detectors in Python:** Implement mathematically defined rules that require a full candle body close past a swing level to signal a structural shift, preventing lookahead bias and subjective charting.
*   **When applying timing filters:** Limit trade executions strictly to session Killzones: London (2:00 AM – 5:00 AM EST), New York AM (8:30 AM – 11:00 AM EST), and New York PM (1:30 PM – 4:00 PM EST).
*   **When executing active trade management:** Enforce strict risk escalation rules: at 1R profit reduce initial risk by 50%, at 2R profit move stop-loss to absolute breakeven, and beyond 2R trail stop behind structural swing points toward a minimum 1:3 RR target.
*   **When analyzing multi-asset correlations:** Utilize Smart Money Technique (SMT) divergence at session highs/lows to select the strongest asset for buys and the weakest asset for shorts.

## Red Flags

| Vulnerability / Retail Trap | Why It Is Wrong | Institutional Action |
| :--- | :--- | :--- |
| **Trading Low-TF FVGs in isolation** | Up to 84% of lower-timeframe FVGs fail and act as liquidity traps when not aligned with HTF context. | Only trade FVGs that overlap HTF POIs or key liquidity sweep zones. |
| **Using lagging indicator crossovers (RSI/MACD)** | Indicators lag behind price action, causing late entries and ignoring the underlying liquidity pools. | Trade pure price delivery, structural shifts, and volume-based order flow. |
| **Entering trades at equilibrium (50%) or worse** | Buying in Premium or selling in Discount drastically reduces the trade's mathematical expectancy and R:R. | Apply Fib retracements and execute entries strictly in Discount for longs and Premium for shorts. |
| **Misidentifying minor internal breaks as CHOCH** | Retail traders get chopped out by entering on minor sub-structural traps designed as inducement. | Wait for clear, energetic displacement past major external swing points to confirm a reversal. |
| **Ignoring the daily Killzone timing filters** | Algorithmic order delivery is highly time-sensitive; trading outside Killzones results in low volume and choppy ranges. | Trade strictly within London, NY AM (Silver Bullet), and NY PM sessions. |

## Quick Reference

### 1. Market Structure & Execution Blueprint
*   **BOS (Break of Structure):** Trend continuation; requires a clean candle body close past a swing high/low in the direction of the dominant trend.
*   **CHOCH / MSS (Change of Character / Market Structure Shift):** Potential trend reversal; requires energetic displacement and a body close past a major external structural swing point.
*   **Premium / Discount:** The 50% midpoint of the current dealing range. Longs = Discount (<50%), Shorts = Premium (>50%).
*   **OTE (Optimal Trade Entry):** Algorithmic retracement zone between the 0.618 and 0.79 levels, with 0.705 as the sweet spot.

### 2. Primary PD Array Configurations
*   **Unicorn Model:** Horizonatal overlap of an ICT Breaker Block and an unmitigated Fair Value Gap (FVG).
*   **Balanced Price Range (BPR):** Horizontal overlap of a bullish FVG and a bearish FVG, creating an immediate algorithmic equilibrium zone.
*   **Inverse FVG (IFVG):** A standard FVG that has been broken by a decisive candle body close, flipping its support/resistance polarity.
*   **Breaker Block:** A failed order block that successfully swept liquidity (stop hunt of an extreme) before the market shifted structure.