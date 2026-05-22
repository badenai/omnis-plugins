---
name: trade-execution-fvg
description: Use when identifying high-precision entry mechanisms, executing orders at Fair Value Gaps (FVG) or Balanced Price Ranges (BPR), calculating Consequent Encroachment (CE), or applying mechanical entry models like IOFED, Unicorn, and Venom.
---

## The Iron Law

```
NEVER execute a long entry above the 50% equilibrium of the dealing range (premium) or a short entry below the 50% equilibrium (discount). All execution imbalances (FVGs, BPRs, iFVGs) must be completely unmitigated; a single previous wick touch invalidates the setup.
```

## Behavioral Rules

*   **Premium/Discount Constraints**: Restrict all long executions strictly to discount arrays (below the 50% Fibonacci equilibrium of the defined dealing range) and all short executions strictly to premium arrays (above the 50% equilibrium).
*   **Imbalance Execution Models**:
    *   If executing a standard FVG entry, place the limit order at either the proximal edge or the exact 50% Consequent Encroachment (CE) level of the gap.
    *   If executing the IOFED (Institutional Order Flow Entry Drill) model, place the entry limit order strictly at the proximal edge of the FVG and do not wait for deeper retracements to the 50% CE.
    *   If executing the Venom model, place limit orders precisely at the proximal boundary of the Balanced Price Range (BPR) immediately following a major liquidity sweep.
*   **Balanced Price Range (BPR) Validation**:
    *   Identify a BPR strictly by locating the exact horizontal overlap where a highly aggressive bullish displacement is immediately countered by a highly aggressive bearish displacement (or vice versa).
    *   Do not execute a BPR entry unless the pattern forms immediately after a clean sweep of external liquidity (Previous Day High/Low or session swing high/low).
    *   Place execution orders at the proximal boundary of the BPR; do not allow or wait for deep retracements to the 50% CE as valid BPRs are heavily defended and rarely deeply penetrated.
*   **Unicorn Model Confluence**: Trigger the Unicorn Model only at the direct confluence zone where a valid Breaker Block (a broken order block that swept liquidity prior to displacement) intersects directly with a standard FVG or an Inverse FVG (iFVG).
*   **Strict Time-Restricted Execution (Silver Bullet)**:
    *   Limit active hunting and execution of intraday imbalance setups strictly to the three 60-minute windows: 3:00 AM – 4:00 AM NY (London Open), 10:00 AM – 11:00 AM NY (NY AM), and 2:00 PM – 3:00 PM NY (NY PM).
    *   Cancel all pending limit orders and close active intraday positions immediately if the liquidity sweep, Market Structure Shift (MSS) with displacement, and imbalance formation do not fully trigger an entry within the designated 60-minute window.
*   **Order Flow & Footprint Verification**:
    *   Verify passive institutional absorption on the footprint chart before executing an entry at a Point of Interest (POI), ensuring heavy market volume hits the bid/ask while price fails to progress.
    *   Confirm the final entry trigger using footprint initiation, requiring a sharp Delta Divergence or aggressive buying/selling imbalances moving away from the POI.
*   **Candle Range Theory (CRT) Allocation**: During Candle 3 (Distribution) of the CRT cycle, execute on lower-timeframe charts (1m to 5m) using local FVGs to capture the rapid intraday expansion.
*   **Market Structure Shift (MSS) Confirmation**: Validate an MSS strictly by confirming a full body candle close past the swing high/low; do not treat wicks through structure as structural breaks.

## Red Flags

| Rationalization | Why it is wrong |
| :--- | :--- |
| "Entering an FVG that has already been wicked into because it is a strong HTF zone." | The first test of the proximal edge is the only valid high-probability touch; subsequent touches represent mitigation and capital risk. |
| "Executing a trade during high-impact news spikes because the displacement candle is huge." | Entering news-driven spikes directly violates execution rules; wait for the liquidity sweep and lower-timeframe MSS post-news. |
| "Using standard FVG entries with deep stop losses in a highly aggressive, instant-displacement market." | Slower entries miss the move or yield poor R:R; apply the IOFED model to capture high-velocity institutional delivery at the proximal edge. |
| "Executing a long in a premium array or a short in a discount array because of a strong LTF break." | Institutional orders are restricted by premium/discount equilibrium; trading against the HTF array leads to high-drawdown stopouts. |
| "Treating an FVG that does not produce displacement or a body close past swing points as a valid POI." | Without strong displacement and a body-close MSS/CHOCH, the imbalance is just retail noise or market inducement. |
| "Keeping limit orders active outside the Silver Bullet execution windows because 'the setup is still valid'." | Leaving orders open outside designated algorithmic windows invites low-volume chop, slippage, and manipulative stop hunts. |

## Quick Reference

| Execution Model | Entry Trigger Level | Stop Loss Placement | Target Profit / Exit |
| :--- | :--- | :--- | :--- |
| **Standard FVG** | Proximal edge of the gap or 50% Consequent Encroachment (CE) | Beyond the swing high/low that created the displacement | Opposing external range liquidity |
| **Balanced Price Range (BPR)** | Proximal boundary of the overlapping bullish/bearish FVGs | Directly beyond the boundary or the sweep wick | Opposing session or daily liquidity pool |
| **IOFED Model** | Strict proximal edge of the FVG (very beginning) | Tighter structural stop behind the immediate candle block | Quick expansion targets (1:3+ R:R minimum) |
| **Unicorn Model** | Confluence zone of Breaker Block + FVG / iFVG | Beyond the high/low of the Breaker Block | Next HTF liquidity pool or unmitigated FVG |
| **Venom Model** | Proximal boundary of the post-sweep BPR | Strictly behind the wick that swept external liquidity | HTF external liquidity (PDH/PDL) |
| **Silver Bullet Setup** | First retracement into FVG/BPR formed inside the 60m window | Protected structural swing high/low formed during the sweep | Opposing session high/low |