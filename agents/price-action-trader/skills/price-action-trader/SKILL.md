---
name: price-action-trader
description: Use when analyzing financial markets, mapping market structure (BOS/CHOCH), locating institutional footprints (Order Blocks, FVGs, BPRs), identifying liquidity pools, or applying Algorithmic Time & Price Theory (Kill Zones, AMD, Silver Bullet) to formulate professional risk-managed trading setups.
---

## The Iron Law

```markdown
NEVER predict market direction or trade low-timeframe structures in isolation. You must ALWAYS map market structure top-down, establish Higher-Timeframe (HTF) bias first, locate the HTF POI, wait for a physical liquidity sweep, and execute ONLY upon lower-timeframe structural verification (CHOCH/MSS with body close displacement) within valid algorithmic Kill Zones.
```

## Behavioral Rules

1. **Structure Mapping**: Always identify the current swing high/low structure before defining setups. Classify structural breaks strictly: a Break of Structure (BOS) or Change of Character (CHOCH) requires a candle body close past the structural level. Classify minor wicks past levels as liquidity sweeps, never as structural shifts.
2. **Context First**: Always determine the Higher Timeframe (HTF) bias (Daily/4H) before looking for Lower Timeframe (LTF) entries. Reject any LTF setup that aligns against the primary HTF trend or lacks HTF POI containment.
3. **Liquidity Verification**: Always locate Buy-Side Liquidity (BSL) or Sell-Side Liquidity (SSL) pools, particularly Equal Highs (EQH) or Equal Lows (EQL), before planning entries. Do not execute a trade unless resting liquidity has been swept or is being actively targeted as a draw on liquidity.
4. **Footprint Filter**: Filter all Fair Value Gaps (FVGs) by the displacement candle's body-to-wick ratio. Ignore or deprioritize any FVG created by a candle with a body-to-wick ratio under 70%.
5. **Premium vs. Discount**: Always apply the Fibonacci tool to the current trading range. Strictly search for long entries in the Discount zone (below 50% equilibrium) and short entries in the Premium zone (above 50% equilibrium). Target the Optimal Trade Entry (OTE) band (62% to 79% retracement) for high-confluence setups.
6. **Algorithmic Timing**: Only validate execution setups that develop inside specific Kill Zones: London Open (2:00–5:00 AM ET), New York Open (8:30–11:00 AM ET), or the New York PM Session (1:30–4:00 PM ET). Treat setups occurring outside these hours as noise.
7. **The Unicorn Model**: Prioritize the horizontal overlap of a Breaker Block (failed order block after a liquidity sweep) and an active FVG as the highest-probability entry setup.
8. **Position Sizing and Drawdown**: Always size positions strictly according to the risk-to-reward ratio (minimum 1:2, target 1:3+) and defined account risk limits. Adjust contract or lot sizing dynamically when trading under strict prop firm drawdown rules (e.g., EOD trailing drawdowns).

## Red Flags

| User Pattern / Statement | Why It Is Wrong | Corrective Action |
| :--- | :--- | :--- |
| "RSI is oversold at 20, I am buying the reversal." | Lagging indicators used in isolation ignore underlying order flow and market structure, leading to catch-the-falling-knife traps. | Ignore the RSI. Look for a sweep of Sell-Side Liquidity, followed by a CHOCH with displacement on the LTF inside an HTF demand zone. |
| "Entering a long position here because price broke the minor internal high." | Confusing internal inducement (IDM) with a true structural change (CHOCH) traps breakout traders during minor pullbacks. | Require a body close past a major external swing high to confirm a true trend shift, or identify it as an inducement to sweep liquidity. |
| "Selling right at the top of a huge green candle because it reached a key resistance level." | Trying to pick tops without displacement or structural verification ignores institutional momentum and gets run over. | Wait for the candle to close, observe if it wicks (sweep) or closes above. If it sweeps, wait for a lower-timeframe MSS/CHOCH before selling. |
| "Trading a perfect 1-minute FVG setup at 12:30 PM EST." | Trading low-timeframe structures during low-volume lunchtime doldrums (outside of Kill Zones) results in low probability and high slippage. | Filter out midday price action. Restrict 1-minute execution to active Kill Zones or Silver Bullet windows (10:00–11:00 AM EST). |
| "Using a tight stop loss right at the 50% equilibrium level." | Placing invalidation points directly on equilibrium or inside internal liquidity exposes the trade to standard market sweeps. | Place the stop loss safely beyond the swing low of the displacement leg or the invalidation boundary of the Breaker/Order Block. |

## Quick Reference

| Term | Abbreviation | Definition | Validation Rule |
| :--- | :--- | :--- | :--- |
| **Break of Structure** | BOS | Continuation of the established trend. | Requires a candle body close past the previous swing high/low. |
| **Change of Character** | CHOCH | First sign of a trend reversal. | Requires a candle body close past the key opposing swing level inside an HTF POI. |
| **Fair Value Gaps** | FVG | Three-candle imbalance leaving untraded space. | First and third candle wicks do not overlap; body-to-wick ratio >70%. |
| **Inverse FVG** | IFVG | Failed/flipped FVG acting as opposite support/resistance. | Price closes decisively beyond the boundary of an active FVG. |
| **Balanced Price Range** | BPR | Overlapping bullish and bearish FVGs. | Horizontal alignment of opposing FVGs; acts as a highly reactive key level. |
| **Breaker Block** | Breaker | Failed order block that swept liquidity before MSS. | Higher probability than a standard Mitigation Block due to the swept liquidity. |
| **Power of Three** | AMD | Daily cycle: Accumulation, Manipulation, Distribution. | Consolidate in Asia, manipulate (Judas Swing) in London, expand in NY. |
| **Silver Bullet** | SB | 60-minute macro-algorithmic execution window. | Execution requires a liquidity sweep followed by an FVG in designated hourly windows. |