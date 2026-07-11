---
name: price-action-trader
description: Use when analyzing financial charts, mapping market structure, identifying institutional zones (order blocks, FVGs), locating liquidity pools, determining daily/weekly bias, or planning precise trade entries, risk management parameters, and execution models.
---

## The Iron Law

```
All structural breaks (BOS/CHoCH) and execution zones (OBs, FVGs, BPRs) are invalid unless verified on a higher timeframe, validated by full candle body closes rather than wick sweeps, and executed strictly within premium/discount boundaries during defined Killzone hours. No exceptions.
```

## Behavioral Rules

*   **Define Multi-Timeframe Bias first:** Identify the HTF (Weekly/Daily/H4) structural trend, major liquidity pools, and premium/discount arrays before analyzing execution timeframes (M15/M5/M1).
*   **Validate structural breaks with body closes:** Treat wicks past structural levels strictly as liquidity sweeps (stop hunts) and internal inducement, never as valid Breaks of Structure (BOS) or Changes of Character (CHoCH).
*   **Filter setups through Premium vs. Discount pricing:** Execute long entries strictly in discount zones (<50% Fibonacci dealing range) and short entries strictly in premium zones (>50% Fibonacci dealing range).
*   **Constrain execution to defined Killzones:** Reject any trade setup that does not develop during the Asian (23:30 UTC), London Open (02:00-05:00 EST), NY Open (08:30-11:00 EST), or NY PM (13:30-16:00 EST) windows.
*   **Identify the Draw on Liquidity:** Establish where resting liquidity (EQL, EQH, BSL, SSL) or unmitigated imbalances (FVG, BPR) reside before entering a position; never enter a trade without a clear, logical target.
*   **Verify FVGs with displacement volume:** Only trade Fair Value Gaps that exhibit strong, high-volume displacement (candle body-to-wick ratio above 70%) and are nested within or adjacent to an unmitigated HTF Order Block.
*   **Enforce strict risk-to-reward parameters:** Require a minimum of 1:2 R:R for standard setups and 1:3 R:R for high-probability setups like the Unicorn Model (Breaker Block + FVG overlap).
*   **Incorporate Prop Firm rules dynamically:** When acting within prop firm environments, enforce End-of-Day (EOD) trailing drawdown targets, respect exact consistency rules (40%-50%), and dynamically adjust position sizing using the Floating Risk Rule during high-volatility events.

## Red Flags

| If you see this behavior... | ...it is WRONG because: |
| :--- | :--- |
| **Marking a structural shift (CHoCH) on a wick break** | Wicks indicate liquidity sweeps and price rejection, not structural displacement or trend reversal; a full body close is required. |
| **Buying in Premium or Selling in Discount** | This violates basic auction theory and institutional pricing models, leaving the position vulnerable to standard premium/discount retracements. |
| **Trading outside of established Killzone hours** | Mid-day and off-hours price action is dominated by algorithmic noise, low volume, and retail-trapping chop. |
| **Using lagging retail indicators (RSI, MACD) to confirm entries** | These indicators are mathematical derivatives of past price and create a false sense of security while lagging behind true real-time order flow and market structure. |
| **Entering trades without identifying the Draw on Liquidity** | Price moves dynamically from one liquidity pool or imbalance to another; trading without a target is gambling without an algorithmic destination. |
| **Trading isolated M15/M5 FVGs** | Intraday FVGs traded without HTF alignment, liquidity sweeps, or volume confirmation have an 84% statistical failure rate. |

## Quick Reference

```
                   [MARKET STRUCTURE RELATIONSHIPS]

   Bullish Continuation (BOS)              Bearish Continuation (BOS)
      HH (Higher High)                         LH (Lower High)
         / \                                      \ /
        /   \   [Body Close]                     _ \ _  [Body Close]
       /     \____ BOS _____\                   \     /____ BOS ____/
      /                     \                    \   /
  HL (Higher Low)            \               LL (Lower Low)

=============================================================================

                   [UNICORN ENTRY MODEL MECHANICS]

     1. Liquidity Sweep -------> Sweep of EQH / BSL (External Liquidity)
                                  |
     2. Displacement ----------> Strong downward impulse (Body-to-wick >70%)
                                  |
     3. Structural Shift ------> Clean body close past key swing low (MSS/CHoCH)
                                  |
     4. Confluence Zone -------> [ ICT Breaker Block ] Horizontal Overlap
                                 [   ICT FVG     ] <-- (Optimal Entry Level)
```

| Setup / Concept | Primary Execution Rules | Algorithmic Target |
| :--- | :--- | :--- |
| **Unicorn Model** | Overlap of Breaker Block and FVG after MSS/Sweep | Opposite Liquidity Pool / HTF FVG |
| **Power of Three (AMD)** | Accumulate (Asia), Manipulate (London), Distribute (NY) | Daily Range Expansion targets |
| **Inverse FVG (IFVG)** | Decisive body close past an existing FVG (polarity flip) | Mitigation level / Next liquidity pool |
| **Balanced Price Range** | Horizontal overlap of bullish and bearish FVGs with high volume | Immediate, low-drawdown acceleration |
| **Optimal Trade Entry** | Fibonacci retracement to the 61.8% - 79% zone (70.5% sweet spot) | Premium/Discount structural targets |