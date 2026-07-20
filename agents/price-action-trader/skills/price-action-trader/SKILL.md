---
name: price-action-trader
description: Use when analyzing financial market charts, mapping market structure (BOS, CHoCH, MSS), identifying Premium/Discount dealing ranges, locating institutional liquidity pools/sweeps, evaluating PD arrays (Order Blocks, FVGs, Breakers), or integrating footprint volume microstructure and session timing.
---

## The Iron Law

```
Never classify a wick penetration of a structural swing high or low as a Break of Structure (BOS)—treat it strictly as a liquidity sweep until a candle body closes beyond that level; never execute longs outside discount arrays or shorts outside premium arrays of the active dealing range.
```

## Behavioral Rules

### 1. Market Structure & Dealing Range Verification
* If a swing level is penetrated only by a candlestick wick, classify it as a liquidity sweep and wait for a full candle body close to confirm a valid Break of Structure (BOS).
* Confirm a Market Structure Shift (MSS) only when price prints strong displacement (aggressive momentum candles) breaking a major swing level, rather than a passive tap or low-volume reaction.
* Map the active dealing range from the verified swing high to the swing low, dividing it precisely into Premium (top 50%), Equilibrium (50%), and Discount (bottom 50%).
* Reject all long entries in Premium arrays and all short entries in Discount arrays; filter out all trades executing within middle-range consolidations.

### 2. Liquidity & Inducement Mechanics
* Identify Equal Highs (EQH) and Equal Lows (EQL) as high-probability targets (liquidity clusters) for institutional sweeps before mapping reversal zones.
* Wait for the complete sweep of internal liquidity (Inducement) to trap premature traders before aligning your execution with the primary higher-timeframe trend.
* Apply a strict "Wait-and-Verify" double-sweep protocol on lower timeframes (1m/5m) to filter out early single-sweep retail SMC traps.
* Place hard protective stop-losses structurally beyond the absolute extreme sweep wick; never place stops within the wick body as they are highly vulnerable to re-tests.

### 3. PD Array Calibration & Entry Models
* Validate an Order Block (OB) only if it represents the last candle in the opposite direction before a decisive, high-volume price expansion.
* Prioritize Breaker Blocks (BB) over Mitigation Blocks (MB) due to the completed liquidity sweep validating the breaker's institutional backing.
* Confirm an Inverse Fair Value Gap (IFVG) only when a candle body closes decisively past the original FVG boundaries, flipping its structural polarity.
* Execute the ICT Unicorn Model by locating the exact horizontal overlap of an ICT Breaker Block and an ICT Fair Value Gap (FVG) inside the breaker's price range.
* Use the Reaper Inversion FVG (Reaper IFVG) strictly within the impulsive price leg of a breaker block (discount for bullish, premium for bearish) to catch institutional defenses.

### 4. Session Timing & Algorithmic Cycles
* Restrict live execution to precise ICT Kill Zones: London Open (2:00 AM – 5:00 AM ET), New York Open (8:30 AM – 11:00 AM ET), and New York PM (1:30 PM – 4:00 PM ET).
* Prioritize the Silver Bullet Windows for rapid algorithmic delivery: London AM (3:00 AM – 4:00 AM EST), New York AM (10:00 AM – 11:00 AM EST), or New York PM (2:00 PM – 3:00 PM EST).
* Map the daily Accumulation, Manipulation, Distribution (AMD) template: expect the Asian range to accumulate, the London session to manipulate (Judas Swing), and the New York session to distribute.

### 5. Volumetric & Order Flow Confluence
* Verify heatmap passive limit orders using footprint chart execution; do not trade heatmap walls unless confirmed by diagonal bid-ask imbalances (3:1 ratio) or Point of Control (POC) cluster rejections.
* Identify institutional absorption when massive market order volume (visible on footprint delta) is met by passive limit orders, causing price to stall instead of expanding.
* Confirm market exhaustion by identifying a Cumulative Volume Delta (CVD) divergence (e.g., price printing lower lows while CVD prints a flat or rising slope).

### 6. Professional Mechanics & Risk Controls
* Position-size dynamically using Fixed Fractional (risking a constant 1% to 2% of capital per trade) or Volatility-Based models.
* Implement the "Three-Mistake Rule": immediately close all trading platforms upon committing three pre-defined operational errors (e.g., trading outside session windows, altering a resting stop-loss, violating contract sizes).
* Ensure any lower-timeframe FVG or OB entry is backed by a higher-timeframe (e.g., 4-hour) trend structure to avoid the statistical 84% failure rate of isolated lower-timeframe gaps.

---

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "A wick broke the swing high, so the structure has shifted bullish. Let's buy the breakout." | A wick is a liquidity sweep, not a structural break. Entering on a wick break traps you right before the market reverses. |
| "A 15-minute Fair Value Gap (FVG) has formed; I'll place a limit order directly at the proximal boundary." | 84% of lower-timeframe FVGs that get filled immediately reverse and break structure unless backed by a higher-timeframe HTF array. |
| "There is a massive buy wall on the heatmap, meaning this level is guaranteed to hold as strong support." | Limit walls are highly vulnerable to algorithmic spoofing and can be pulled milliseconds before price arrival. Must verify execution via footprint. |
| "Price swept the low once, so the manipulation phase is complete; let's enter immediately with a tight stop inside the sweep wick." | 30% to 40% of first-touch sweeps are inducement traps for a secondary deeper sweep (double-sweep). Stops inside the wick body will be run. |
| "This is a great setup; I'll trade it at 1:15 PM EST because the market looks highly active." | Trading outside designated Kill Zones or Silver Bullet windows exposes you to low-volume, manipulative retail shakeouts. |

---

## Quick Reference

### Structural & Session Coordinates

| Core Concepts | Tactical Checklist / Parameters | Rules of Engagement |
| :--- | :--- | :--- |
| **BOS vs. Sweep** | • BOS: Candle body close beyond key swing point.<br>• Sweep: Wick penetration only, followed by immediate rejection. | Wait for body close before marking trend continuation. |
| **Premium/Discount** | • Premium: Top 50% of the active dealing range.<br>• Discount: Bottom 50% of the active dealing range. | • Shorts: Premium only.<br>• Longs: Discount only. |
| **Double-Sweep Protocol** | • Step 1: Sweep of major HTF external liquidity.<br>• Step 2: Secondary sweep (inducement of early buyers/sellers).<br>• Step 3: Low-timeframe MSS close. | Place hard stop-loss strictly beyond the absolute extreme sweep wick. |
| **Kill Zones (ET)** | • London Open: 2:00 AM – 5:00 AM ET<br>• New York Open: 8:30 AM – 11:00 AM ET<br>• New York PM: 1:30 PM – 4:00 PM ET | No new positions executed outside these specific hours. |
| **Silver Bullet (ET)** | • London AM: 3:00 AM – 4:00 AM EST<br>• New York AM: 10:00 AM – 11:00 AM EST<br>• New York PM: 2:00 PM – 3:00 PM EST | Target these highly scheduled 60-minute algorithmic windows. |
| **Unicorn Model** | • Intersection: ICT Breaker Block + ICT FVG.<br>• Location: Directly inside the breaker's price range. | Wait for retest of the overlapping zone for low-drawdown entry. |