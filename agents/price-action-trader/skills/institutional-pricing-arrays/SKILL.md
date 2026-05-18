---
name: institutional-pricing-arrays
description: Use when analyzing market entries, Fair Value Gaps (FVG), Order Blocks (OB), or executing trades within Premium/Discount pricing arrays after a structural shift.
filePattern: "**/*.md"
---

## The Iron Law

```text
Never execute a long position in a Premium or a short position in a Discount; you must strictly confine all entries to institutional footprints (Fair Value Gaps/Order Blocks) that reside within the correct half of the overarching structural dealing range.
```

## Behavioral Rules

*   **Premium/Discount (PD) Calibration:** Measure the structural leg from the absolute swing high to the absolute swing low to define the current dealing range. 
*   **Execution Matrix:** Only initiate long positions in the Discount matrix (<50% of the range) and only initiate short positions in the Premium matrix (>50% of the range).
*   **Displacement Requirement:** Validate a Fair Value Gap (FVG) or Order Block (OB) as tradeable only if it was forged by strong, impulsive energetic displacement that simultaneously breaks market structure (MSS).
*   **Invalidating Retail Noise:** Ignore all overlapping, slow, or low-volatility structural breaks; if price does not leave a clear imbalance (FVG) behind, discard the setup immediately.
*   **Internal to External Delivery:** Enter trades at Internal Range Liquidity (FVGs/OBs) and explicitly target External Range Liquidity (unmitigated swing highs/lows) for take-profit placement.
*   **High-Impact News Filter:** Never execute entries on FVGs formed during the immediate volatility shock of high-impact news (e.g., CPI, NFP); wait for the post-news structure to establish a clear PD array.
*   **Timeframe Alignment:** Require higher-timeframe (Daily/4H) directional bias confirmation before dialing down to the 15m, 5m, or 1m timeframes to pinpoint the FVG entry.

## Red Flags

| Retail Rationalization | Institutional Reality |
| :--- | :--- |
| "This FVG is massive, I will enter at the very beginning of the gap to guarantee a fill." | Entering a gap before it crosses into the correct Premium/Discount threshold traps you in mid-range chop with negative expectancy. |
| "Price is returning to a 1-minute order block, this is a perfect sniper entry." | Lower-timeframe arrays divorced from the higher-timeframe Daily/4H narrative are localized liquidity pools engineered to be swept. |
| "Price broke resistance, I am buying the immediate pullback." | A break of structure lacking energetic displacement and a resulting FVG is retail noise, not a true institutional market structure shift. |
| "I will trade this FVG even though it formed inside a tight consolidation range." | Low-volatility conditions lack the institutional sponsorship required to validate imbalances; these gaps have a high failure rate. |

## Quick Reference

| Pricing Array | Identification | Execution Condition |
| :--- | :--- | :--- |
| **Premium Array** | Upper 50% of the current structural dealing range. | Execute shorts at Premium OBs/FVGs; take profit on longs. |
| **Discount Array** | Lower 50% of the current structural dealing range. | Execute longs at Discount OBs/FVGs; take profit on shorts. |
| **Fair Value Gap (FVG)** | 3-candle sequence leaving a clear price imbalance. | Price retraces into the gap, aligning with HTF narrative and correct PD matrix. |
| **Order Block (OB)** | Last opposite-colored candle before energetic displacement. | Must reside at the origin of an FVG and definitively break market structure. |
| **Displacement** | Impulsive, large-range candles breaking levels. | Required confirmation step before marking any FVG or OB valid for entry. |