---
name: trade-execution-fvg
description: Use when framing trade entries, placing stop-losses, identifying Fair Value Gaps (FVG) for execution, or applying the mechanical execution sequence of liquidity purge, market structure shift, and multi-timeframe entry alignment.
---

## The Iron Law

```text
Never execute a trade without first confirming a higher-timeframe liquidity sweep followed by a lower-timeframe Market Structure Shift (MSS) with displacement, and always mandate entry at the resulting Fair Value Gap (FVG) with the stop-loss strictly placed beyond the sweep wick.
```

## Behavioral Rules

*   Establish higher-timeframe (Daily/4H) directional bias and Premium/Discount (PD) arrays before evaluating lower-timeframe (15m/5m/1m) execution setups.
*   Execute entries using only the strict mechanical sequence: Identify Liquidity (PDH/PDL/Session pools) -> Wait for Purge -> Confirm MSS with Displacement -> Enter on FVG Retracement.
*   Demand energetic displacement candles that break structure to confirm an MSS; ignore structural breaks that lack strong volume or momentum footprints.
*   Place stop-loss orders objectively beyond the absolute wick that engineered the liquidity sweep, never relying on fixed or arbitrary pip counts.
*   Cancel entry limit orders or exit manually if the sweep wick is violated before or during the trade execution, as the institutional setup is objectively invalidated.
*   Frame trade setups exclusively to deliver price from Internal Range Liquidity out to External Range Liquidity.
*   If trading around heavy macroeconomic data (e.g., FOMC, CPI), wait for double-sided sweeps to clear and rely solely on a post-volatility higher-timeframe MSS for entry confirmation.

## Red Flags

| Rationalization | Why wrong |
| :--- | :--- |
| "I'm entering early on the sweep to get a better price." | A sweep without an MSS and displacement is merely a stop hunt; entering without institutional confirmation is gambling. |
| "I'll use a fixed 10-pip stop loss to keep my risk-reward high." | Risk must be defined by market structure (the specific sweep wick), not an arbitrary pip count. |
| "The 1-minute chart shows a bullish FVG, so I am buying immediately." | Lower timeframes are pure noise when divorced from a higher-timeframe (Daily/4H) directional bias and PD array context. |
| "Price is sweeping the high during FOMC, I'm shorting right now." | News volatility frequently engineers double-sided sweeps; entering before the post-news structure shifts exposes you to immediate stop-outs. |

## Quick Reference

| Phase | Action | Condition |
| :--- | :--- | :--- |
| **1. HTF Context** | Establish bias and Premium/Discount arrays | Must use Daily/4H charts |
| **2. Liquidity Purge** | Wait for price to sweep external liquidity | Target PDH, PDL, or Session Highs/Lows |
| **3. Institutional MSS**| Confirm Market Structure Shift | Requires energetic displacement candles |
| **4. Mechanical Entry**| Set limit order at FVG retracement | Must frame Internal to External Range delivery |
| **5. Risk Placement** | Place hard stop-loss | Strictly above/below the exact sweep wick |