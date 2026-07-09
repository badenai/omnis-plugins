---
name: market-structure-liquidity
description: "Use when analyzing market structure, mapping trend transitions (BOS/CHOCH), verifying liquidity sweeps vs. body closes, and locating institutional liquidity pools."
---

## The Iron Law

```
A wick through a structural level is strictly a liquidity sweep (stop hunt) and must never be mapped as a structural break. A valid Change of Character (CHOCH) or Break of Structure (BOS) requires a full candle body close past the swing level on the timeframe being analyzed.
```

## Behavioral Rules

*   If analyzing structural trends, map the structural extremes objectively: Higher Highs (HH) and Higher Lows (HL) for bullish regimes; Lower Highs (LH) and Lower Lows (LL) for bearish regimes.
*   If a major external swing level is breached, classify it as a Change of Character (CHOCH) only if the candle body closes past that level; otherwise, classify it as a liquidity sweep.
*   If a minor internal high or low is broken, treat it as an Internal Inducement (IDM) trap designed to catch breakout traders, not a structural trend shift.
*   If confirming a liquidity sweep, verify the reaction via lower-timeframe footprint absorption (bid/ask imbalances exceeding 3x) or CVD divergence before entering.
*   If analyzing structural transitions, always perform top-down multi-timeframe alignment; never execute based on low-timeframe structure divorced from the higher-timeframe trend.

## Red Flags

| Invalid Action | Why It Is Wrong | Corrective Action |
| :--- | :--- | :--- |
| **Mapping a wick rejection as a BOS/CHOCH** | Wicks indicate price rejection and a sweep of liquidity, not structural acceptance. | Wait for a full candle body to close past the swing level to confirm structure. |
| **Treating internal breaks (IDM) as major trend shifts** | Minor internal breaks trap early retail traders before sweeping the actual extreme. | Identify external swing highs/lows and ignore internal noise. |
| **Trading low-timeframe structure in isolation** | Low-timeframe structures are highly noisy and frequently fail without higher-timeframe context. | Align the lower-timeframe entry structure with HTF premium/discount zones and key liquidity pools. |
| **Assuming every FVG or OB will hold** | Up to 84% of lower-timeframe FVGs reverse and fail if they do not align with HTF structural arrays. | Only trade FVGs and OBs that overlap with HTF levels or form part of a liquidity sweep setup (e.g., Unicorn Model). |

## Quick Reference

| Structure / Concept | Definition | Validation Metric |
| :--- | :--- | :--- |
| **Break of Structure (BOS)** | Continuation of the dominant structural trend. | Full candle body close past the previous swing high/low. |
| **Change of Character (CHOCH)** | First signal of a potential structural trend reversal. | Full candle body close past the major counter-trend swing level. |
| **Liquidity Sweep (Stop Hunt)** | Price temporarily breaches a level to collect resting stops before reversing. | Wick rejection through the level, accompanied by absorption volume. |
| **Internal Inducement (IDM)** | Minor internal structural break trapping retail breakout traders. | Internal minor high/low break followed by immediate reversal to actual key level. |
| **SMC Unicorn Model** | Horizontal overlap of an ICT Breaker Block and an ICT Fair Value Gap (FVG). | High-probability entry zone formed during a displacement leg post-sweep. |