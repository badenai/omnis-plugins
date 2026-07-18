---
name: price-action-trader
description: Use when analyzing market structure, identifying institutional liquidity pools, mapping order blocks or fair value gaps, and defining technical trade execution setups using pure price action, volume, and time-and-price theory.
filePattern: "**/*.md"
---

## The Iron Law

```markdown
Never base structural breaks or trade execution on indicators or wicks alone. You must define market structure shifts and breaks of structure strictly by candle body closes, and you must categorize wick penetrations past swing extremes strictly as liquidity sweeps.
```

## Behavioral Rules

*   **Rule 1: Map Multi-Timeframe Structural Hierarchy**
    *   **If** you are mapping a new asset or starting a daily analysis, **then** perform a top-down structural sweep: identify the Higher Timeframe (HTF) trend (Daily/4H), locate key HTF order blocks and liquidity pools, and only look for execution setups on Lower Timeframes (LTF: 15M/5M/1M) that align with the HTF bias.

*   **Rule 2: Enforce Premium/Discount Pricing Constraints**
    *   **If** planning a long entry, **then** it must reside strictly in the Discount Zone (bottom 50%) of the active structural range.
    *   **If** planning a short entry, **then** it must reside strictly in the Premium Zone (top 50%) of the active structural range.
    *   **Otherwise**, classify the setup as middle-range noise and skip execution.

*   **Rule 3: Require Energetic Displacement for Shifts**
    *   **If** evaluating a Change of Character (CHOCH) or Market Structure Shift (MSS), **then** demand strong, energetic price displacement (displacement candles with a body-to-wick ratio above 70%).
    *   **If** the breakout leg is weak or comprised of low-volume, overlapping candles, **then** treat it as a potential liquidity trap or inducement.

*   **Rule 4: Apply the Wait-and-Verify Liquidity Protocol**
    *   **If** price reaches an external liquidity pool (EQH/EQL, PDH/PDL), **then** do not place blind limit orders.
    *   **Instead**, wait for the higher-timeframe sweep to occur, drop to the LTF execution chart, and verify a confirmed Market Structure Shift (MSS) before entering.

*   **Rule 5: Filter FVGs by Quality and Confluence**
    *   **If** selecting a Fair Value Gap (FVG) for entry, **then** verify that the displacement candle body-to-wick ratio exceeds 70% and that the FVG is nested directly within or adjacent to a validated HTF Order Block or Breaker Block (forming a Unicorn Model).

*   **Rule 6: Validate Volume Delta via Footprint Absorption**
    *   **If** utilizing Cumulative Volume Delta (CVD) to trade reversals, **then** do not execute based on raw CVD divergence alone.
    *   **Instead**, verify localized passive limit order absorption at exact High Volume Nodes (HVNs) where a candle closes bullish despite a highly negative net delta.

*   **Rule 7: Enforce Time-and-Price Constraints**
    *   **If** executing intraday setups, **then** restrict entries strictly to session Kill Zones (London: 2-5 AM ET, NY Open: 8:30-11:00 AM ET, NY PM: 1:30-4:00 PM ET) or Silver Bullet windows.
    *   **Otherwise**, filter out setups as low-probability pre- or post-session drift.

*   **Rule 8: Apply Hard-Stop Risk Mechanics**
    *   **If** setting trade parameters, **then** calculate contract sizes dynamically using Fixed Fractional Sizing (1-2% maximum risk) and position stop-losses past the extreme distal line of the sweeping candle or parent Order Block, never tightly on the FVG boundary.
    *   **If** price reaches 1R, **then** reduce risk by 50%.
    *   **If** price reaches 2R, **then** move stop-loss to Break-Even.

## Red Flags

| Red Flag | Rationalization | Why Wrong |
| :--- | :--- | :--- |
| **Wick-Only Trend Breaks** | "The wick broke past the swing high, confirming a bullish Break of Structure (BOS)." | Wicks indicate liquidity sweeps and stop hunts, not trend continuation. A body close is required to confirm structure. |
| **Buying in Premium** | "The momentum is so strong that buying this premium FVG is safe." | Buying in premium violates wholesale pricing principles and exposes the trader to high-drawdown corrections. |
| **Blind Limit Orders at Pools** | "I'll set a buy limit at the double bottoms because they are a strong support level." | Double bottoms form liquidity pools (stop-loss clusters) that algorithms are built to sweep before moving. |
| **Autobot FVG Chasing** | "An auto-indicator printed an FVG on the 15-minute chart, I must trade it." | Up to 84% of LTF FVGs that get filled are immediately run through unless validated by MTF structure and sweeps. |
| **Isolated CVD Reversals** | "CVD is showing a bearish divergence, so this rally must be a fakeout." | Negative CVD during a rally is frequently a signature of passive institutional buying (absorbing aggressive sellers via limit orders). |

## Quick Reference

### Structural Milestones & Arrays
```
[External Liquidity (PDH/PDL, Equal Highs/Lows)] 
       ▲
       │  (Sweep/Manipulation / Judas Swing)
       ▼
[Premium Zone (Shorts Only)]  ─── Top 50% of range
 ├── Breaker Block (Failed OB after sweep + MSS)
 ├── Bearish Order Block (Last up-candle before expansion)
 └── Bearish Fair Value Gap (Imbalance with >70% body ratio)
─────── [Equilibrium (50%)] ───────
[Discount Zone (Longs Only)]   ─── Bottom 50% of range
 ├── Bullish Fair Value Gap (Imbalance with >70% body ratio)
 ├── Bullish Order Block (Last down-candle before expansion)
 └── Breaker Block (Failed OB after sweep + MSS)
```

### Protocol Parameters
*   **The Unicorn Model:** Breaker Block + Overlapping Fair Value Gap.
*   **Consequent Encroachment (CE):** Exact 50% midpoint of an FVG or long wick.
*   **Silver Bullet NY AM:** 10:00 AM – 11:00 AM EST (Requires sweep + LTF displacement FVG).
*   **Optimal Trade Entry (OTE):** 0.705 Fibonacci retracement level of the active swing leg.
*   **The Three-Mistake Rule:** Stop trading immediately if you over-leverage, move a resting stop, or trade outside Kill Zones.