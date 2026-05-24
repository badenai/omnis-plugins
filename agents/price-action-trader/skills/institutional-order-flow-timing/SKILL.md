---
name: institutional-order-flow-timing
description: Use when analyzing market structure shifts, identifying session liquidity sweeps (Asian, London, NY), executing during macro timing windows (Silver Bullet, London/NY Open), or mapping AMD/AMDX price delivery cycles.
---

## The Iron Law

```text
NEVER execute any trade entry unless price is inside a designated session macro timing window (London Open 2-5 AM EST, NY Open 7-10 AM EST, or Silver Bullet windows) AND has swept liquidity from a major session range extreme (Asian Range, London High/Low, or Previous Day High/Low).
```

## Behavioral Rules

*   If analyzing the Asian session (8 PM - 12 AM EST), map the high and low boundaries as accumulation ranges; do not trade breakout patterns within this zone.
*   If price approaches the London Open (2 AM - 5 AM EST), anticipate the Judas Swing to sweep Asian range extremes before seeking structural reversals.
*   If executing during the New York AM Session (7 AM - 12 PM EST), trade strictly in the direction of the daily bias targeting unmitigated high-timeframe liquidity pools.
*   If utilizing the AMDX framework, identify the 'X' phase to govern late-session execution and prevent trading into exhausted daily trends.
*   If trading modern prop firm evaluations, restrict all active executions to 60-minute macro windows (e.g., London Open, NY Open, Silver Bullet) to minimize exposure and preserve drawdown.
*   If a liquidity sweep occurs outside of key session timing windows, classify it as a low-probability manipulation and refuse execution until a valid session window opens.
*   If price wicks through a structural level during high-volatility news releases, classify the movement as a liquidity sweep rather than a Market Structure Shift until a session-based candle body closes past the boundary.

## Red Flags

| Retail/Incorrect Practice (Why wrong) | Rationalization used to justify it |
| :--- | :--- |
| Trading breakouts of the Asian range immediately without waiting for a manipulation sweep. | "The volume is expanding, and this momentum breakout is a clear trend continuation." |
| Executing trades during the lunch hour doldrums (12 PM - 1 PM EST). | "Price is retracing to a key FVG, so this is a cheap entry for the PM session." |
| Treating a late-session, low-volume sweep as a valid reversal setup. | "A key daily high was swept at 3:30 PM EST, so a massive reversal must be starting." |
| Taking counter-trend setups during the distribution phase of a strong NY session. | "The moves are overextended on the 5-minute chart and due for a pullback." |
| Relying on standard lagging indicators to determine momentum shifts during session transitions. | "RSI is oversold at the London Open, confirming the market has hit a structural bottom." |

## Quick Reference

| Session / Cycle Phase | Key Time Window (EST) | Algorithmic Function | Execution Action |
| :--- | :--- | :--- | :--- |
| **Asian Accumulation** | 8:00 PM - 12:00 AM | Engineers liquidity pools on both sides of a tight range. | Mark high/low extremes; do NOT trade breakouts. |
| **London Manipulation** | 2:00 AM - 5:00 AM | Executes the Judas Swing; sweeps Asian range/PDH/PDL. | Look for CHOCH/MSS after a confirmed liquidity sweep. |
| **NY AM Distribution** | 7:00 AM - 12:00 PM | Expands price aggressively toward high-timeframe targets. | Trade aligned with daily bias using FVGs and Order Blocks. |
| **PM Continuation/Reversal (X)** | 1:00 PM - 4:00 PM | Resolves the AMDX cycle; completes or reverses daily trend. | Restrict trade size; target local pools; avoid late-day chasers. |
| **Silver Bullet (AM)** | 10:00 AM - 11:00 AM | Rapidly delivers price to local liquidity pools via FVG. | Enter at first FVG validation with strict 10-15 pip targets. |