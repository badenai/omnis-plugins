---
name: price-action-trader
description: Use when analyzing financial charts, mapping market structure (HH/HL, BOS, CHOCH/MSS), identifying institutional liquidity pools and fair value gaps (FVG), executing top-down multi-timeframe setups, or applying strict price-and-time session rules (Kill Zones, Silver Bullet) without relying on lagging retail indicators.
---

## The Iron Law

```text
Never execute a trade without first mapping the higher-timeframe market structure, establishing premium/discount pricing, and waiting for an active liquidity sweep or structural displacement at a high-probability institutional array.
```

## Behavioral Rules

*   **Market Structure Mapping**
    *   Map structural progression using HH/HL (uptrend) and LH/LL (downtrend) across multiple timeframes.
    *   Require a candle body close beyond the previous swing high or low on the dominant execution timeframe to validate a Break of Structure (BOS).
    *   Treat wicks that pierce levels without a body close strictly as liquidity sweeps or stop-hunts.
    *   If expecting a structural reversal, wait for an energetic market structure shift (MSS/CHOCH) characterized by strong, high-volume expansion candles.

*   **Dealing Ranges & Premium/Discount Arrays**
    *   Divide every active trading range into premium (top 50%), equilibrium (midpoint), and discount (bottom 50%) zones.
    *   Never enter long positions in the Premium zone or short positions in the Discount zone.
    *   Target Optimal Trade Entry (OTE) retracements between the 61.8% and 79% levels, prioritizing the 70.5% algorithmic sweet spot.
    *   Only execute OTE setups when they directly overlap with a higher-timeframe Point of Interest (POI).

*   **Imbalance & Footprint Identification**
    *   Identify Fair Value Gaps (FVG) as three-candle structures where the first and third candle wicks do not overlap.
    *   Utilize the 50% Consequent Encroachment (CE) of FVGs or long wicks as dynamic validation levels.
    *   If price closes decisively past an existing FVG, immediately flip its structural role to an Inverse FVG (IFVG).
    *   Look for Balanced Price Ranges (BPR) where bullish and bearish FVGs overlap to locate immediate algorithmic rebalancing zones.
    *   Combine an ICT Breaker Block with an overlapping FVG to execute the high-probability Unicorn Entry Model.
    *   Locate Hidden Order Blocks (HOB) by dropping to lower timeframes when encountering overlapping wicks of consecutive same-color candles on the higher timeframe.

*   **Liquidity & Stop-Loss Pools**
    *   Map External Range Liquidity (ERL) at major swing highs/lows and Internal Range Liquidity (IRL) at minor swing points and FVGs.
    *   Anticipate that price will sweep internal range liquidity and inducement (IDM) before expanding toward major external targets.
    *   Treat Equal Highs (EQH) and Equal Lows (EQL) as major stop-loss clusters and high-probability magnets for institutional sweeps.

*   **Time & Price Integration**
    *   Restrict high-probability execution to daily session Kill Zones: London Open (2:00 AM – 5:00 AM ET), New York Open (8:30 AM – 11:00 AM ET), and New York PM (1:30 PM – 4:00 PM ET).
    *   Apply the Power of Three (AMD) model: Accumulation (Asian), Manipulation (London Judas Swing), and Distribution (New York expansion).
    *   For the ICT Silver Bullet model, execute strictly within the designated windows: 3:00–4:00 AM, 10:00–11:00 AM, or 2:00–3:00 PM EST.
    *   If implementing the Silver Bullet, require a liquidity sweep to occur before or during the start of the 60-minute window; invalidate the setup immediately if displacement occurs without a preceding stop hunt.

*   **Risk & Position Sizing Mechanics**
    *   Implement the Three-Mistake Rule to immediately halt all execution after three predefined operational errors.
    *   Scale position sizes inversely with market volatility using Average True Range (ATR) to keep absolute dollar risk constant.

## Red Flags

| Rationalization / Indicator Signal | Why It Is Flawed / Institutional Reality |
| :--- | :--- |
| "Entering a trade because RSI is oversold/overbought." | RSI is a lagging indicator; price sweeps liquidity and expands regardless of indicator states. |
| "Entering longs immediately upon price touching a major support level." | Support levels are retail stop-loss clusters (EQL/SSL) and act as high-probability magnets for institutional sweeps. |
| "Executing an FVG entry on a low timeframe (e.g., M15) without HTF context." | Statistically, 84% of LTF FVGs filled without HTF POI alignment fail and immediately reverse. |
| "Trading highly volatile breakouts in low-volume environments." | Low-volume price runs are liquidity vacuums, highly prone to immediate fakeouts and deep sweeps. |
| "Treating any wick piercing a swing level as a confirmed Break of Structure (BOS)." | A valid BOS mathematically requires a candle body close; wicks are sweeps and stop-hunts. |

## Quick Reference

| Concept/Setup | Key Conditions / Rules | Expected Target/Action |
| :--- | :--- | :--- |
| **Break of Structure (BOS)** | Candle body close beyond previous swing high/low. | Confirm trend continuation; map new dealing range. |
| **Market Structure Shift (MSS/CHOCH)** | High-volume displacement candle breaking local swing. | Identify potential reversal; look for FVG/OB entry. |
| **Optimal Trade Entry (OTE)** | 61.8% - 79% Fibonacci retracement of active leg. | Execute orders in deep discount (longs) or premium (shorts). |
| **Fair Value Gap (FVG)** | Three-candle gap; wicks of 1st and 3rd candles do not overlap. | Enter at FVG boundary or 50% Consequent Encroachment (CE). |
| **Unicorn Entry** | Horizontal overlap of an ICT Breaker Block and an FVG. | High-probability entry with low drawdown on retest. |
| **Silver Bullet** | 3-4 AM, 10-11 AM, 2-3 PM EST + preceding Liquidity Sweep. | Execute on FVG mitigation inside the 60-minute window. |
| **Power of Three (AMD)** | Accumulation (Asia) -> Manipulation (London Judas) -> Distribution (NY). | Sell above Asian high or buy below Asian low during London/NY open. |