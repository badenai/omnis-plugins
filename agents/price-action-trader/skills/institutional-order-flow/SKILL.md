---
name: institutional-order-flow
description: Use when analyzing market liquidity pools (BSL/SSL), sweep events, Fair Value Gaps (FVGs), Premium/Discount arrays, Order Blocks, and executing precise institutional entries like the Unicorn or Reaper model during designated Kill Zones and ICT Macros.
---

## The Iron Law

```
NEVER execute an entry unless price has swept a validated liquidity pool, confirmed with an explicit lower-timeframe Market Structure Shift (MSS) candle body close, and aligned with Premium (for shorts) or Discount (for longs) arrays relative to the active dealing range.
```

## Behavioral Rules

*   **Map the Dealing Range**: Divide every active trading range into Premium (top 50%), Equilibrium (50%), and Discount (bottom 50%) before identifying execution arrays.
*   **Enforce Wholesale Pricing**: Execute long positions strictly within Discount arrays and short positions strictly within Premium arrays.
*   **Verify Structural Breaks**: Require a full candle body close beyond the structural swing point to confirm a valid Break of Structure (BOS) or Market Structure Shift (MSS).
*   **Classify Wick Penetrations**: Classify wicks filtering through a structural swing point strictly as liquidity sweeps, never as structural breaks.
*   **Execute Multi-Timeframe Sweeps**: Wait for a complete liquidity sweep on the higher timeframe (HTF), drop to the lower timeframe (LTF), and require an explicit MSS candle body close with strong displacement before entering.
*   **Protect Against Double-Sweeps**: Position stop-losses strictly beyond the absolute extreme of the liquidity sweep wick to survive algorithmic inducement re-tests.
*   **Deploy the Unicorn Model**: Prioritize entry setups where an ICT Breaker Block horizontally overlaps with an ICT Fair Value Gap (FVG) after a clean liquidity sweep.
*   **Deploy the Reaper IFVG Model**: Execute via the Reaper Inversion FVG when an Inversion FVG sits strictly within the impulsive price leg of a breaker block.
*   **Apply the IOFED Continuation Protocol**: Utilize the Institutional Order Flow Entry Drill (IOFED) in high-momentum trends only when a retracement into an FVG respects the 50% Consequent Encroachment (CE) and fails to fill.
*   **Filter Lower-Timeframe FVGs**: Discard lower-timeframe FVGs that are filled immediately unless they are directly backed by a Higher Timeframe (H4) Order Block or premium/discount array.
*   **Trade Strict Session Kill Zones**: Execute setups strictly within designated Kill Zones (London: 2:00–5:00 AM ET; NY Open: 8:30–11:00 AM ET; NY PM: 1:30–4:00 PM ET) and align with active 20-minute ICT Macros.
*   **Verify Volumetric Absorption**: Validate institutional reversal zones by confirming footprint diagonal imbalances (>= 3:1 ratio) or Cumulative Volume Delta (CVD) divergence at key HTF Order Blocks.
*   **Implement the Stand-Down Protocol**: Abort the trade entirely if a single checklist item of the 7-Rule Silver Bullet Entry Protocol is missing.
*   **Enforce Behavioral Circuit Breakers**: Shut down all execution platforms immediately upon committing three pre-defined operational errors to protect capital.

## Red Flags

| Domain-Specific Rationalization | Why It Is Wrong |
| :--- | :--- |
| "A high-momentum wick broke the swing high, so structure has officially broken to the upside." | Wicks indicate liquidity sweeps and stop hunts; a structural break requires a full candle body close to confirm institutional displacement. |
| "This FVG is printing on the 5-minute chart, so it is ready for an immediate limit order entry." | Up to 84% of lower-timeframe FVGs that get filled immediately reverse and break structure if they lack backing from an HTF Order Block or PD array. |
| "The market swept liquidity once, so I must enter immediately before I miss the move." | 30% to 40% of first sweeps are inducement traps designed to engineer liquidity for a secondary, deeper sweep; always wait for a secondary sweep or an LTF MSS. |
| "I can execute this Order Block setup at 11:45 AM ET because the price action is clean." | Order delivery algorithms operate on strict time-and-price schedules; setups outside Kill Zones or ICT Macros represent retail noise. |
| "I will place my stop-loss tight, halfway inside the sweep candle wick to get a higher risk-to-reward ratio." | Algorithmic market makers frequently hunt early retail stops with secondary re-tests of the sweep wick; stops must sit strictly beyond the absolute extreme. |

## Quick Reference

| Reference Point | Condition for Execution | Algorithmic Target / Level |
| :--- | :--- | :--- |
| **Unicorn Model** | Horizontal overlap of a Breaker Block and an FVG | Deep retest of the overlapping zone |
| **Reaper IFVG** | FVG polarity flip nested inside breaker's impulsive leg | Boundaries of the Inversion FVG |
| **Consequent Encroachment** | Midpoint of an FVG or long candlestick wick shadow | Exact 50% level of the imbalance |
| **Balanced Price Range** | Horizontal overlap of a bullish and a bearish FVG | Extreme support/resistance with minimal drawdown |
| **Silver Bullet Window** | Executed inside 10:00–11:00 AM ET or 2:00–3:00 PM ET | 1-minute FVG retest targeting opposing liquidity |
| **Optimal Trade Entry (OTE)** | retracement from true structural anchor of impulse leg | 0.618 to 0.79 Fibonacci levels (0.705 midpoint) |
| **Footprint Absorption** | High volume traded on both Bid/Ask with no price progress | Mitigation block or HTF Order Block boundary |