---
name: institutional-order-flow-timing
description: Use when analyzing market execution windows, identifying algorithmic price delivery arrays (FVGs, BPRs, Breakers), or evaluating institutional session setups (Kill Zones, Judas Swings, and liquidity sweeps).
---

## The Iron Law

```
Price delivery is subordinate to Time. Never execute structural setups, liquidity sweeps, or PD array mitigations outside of designated algorithmic Kill Zones (London, NY Open/Silver Bullet, NY PM). If the clock does not validate the level, the setup does not exist.
```

## Behavioral Rules

1. **Validate Setup Timing First**
   * If price reaches a high-probability PD Array (Order Block, FVG, or BPR) outside of active session Kill Zones, you must ignore the level and wait for the next algorithmic execution window.
   * Active execution windows must be strictly restricted to:
     * London Open: 2:00 AM – 5:00 AM ET
     * New York Open / Silver Bullet: 8:30 AM – 11:00 AM ET
     * New York PM Session: 1:30 PM – 4:00 PM ET

2. **Deconstruct the Judas Swing**
   * When an aggressive run occurs in the first 30–60 minutes of a session open, you must check for a sweep of key intraday liquidity pools (previous session highs/lows or daily highs/lows) before looking for reversal setups.
   * Never chase the initial, high-velocity move of a session; identify it as the Judas Swing and prepare to trade the subsequent Market Structure Shift (MSS) in the opposite direction.

3. **Differentiate Breakers from Mitigation Blocks**
   * You must classify a failed order block as a Breaker Block *only* if price has swept a major liquidity extreme (stop hunt) prior to the Market Structure Shift.
   * You must classify a failed order block as a Mitigation Block if price forms a failure swing (failing to take the previous high/low) before reversing. Apply tighter risk parameters and half-risk sizing to Mitigation Blocks due to lower institutional conviction.

4. **Execute Precise Entry Models**
   * **The ICT Unicorn Model:** You must execute entries strictly when a Fair Value Gap (FVG) overlaps horizontally within the physical boundaries of a Breaker Block.
   * **The ICT Reaper Inversion FVG:** If executing an Inversion FVG within a breaker's impulsive leg, you must verify the Inversion FVG lies in the *Discount* zone for long setups, or the *Premium* zone for short setups.
   * **The Venom Model:** Execute immediate market or limit orders at the boundary of a newly formed Balanced Price Range (BPR) following a confirmed liquidity sweep during a Kill Zone. Target external liquidity.
   * **IOFED:** In high-momentum trends, place limit orders directly at the proximal edge of the FVG rather than waiting for a 50% consequent encroachment fill.

5. **Confirm Structural Breaks via Volumetrics**
   * Do not classify a candle close past a swing level as a genuine Break of Structure (BOS) or Change of Character (CHOCH) without validating volume/delta.
   * If the break occurs on declining volume or negative/neutral Cumulative Volume Delta (CVD), treat it as an Inducement (IDM) trap and wait for a sweep.
   * If a liquidity sweep is accompanied by massive market order imbalances (exceeding 3:1 on a footprint chart) but price immediately stalls and fails to expand, confirm this as institutional absorption and execute the reversal.

6. **Enforce the Three-Mistake Rule**
   * You must recommend a complete trading halt and platform shutdown if a trader commits three operational errors in a single session, including:
     * Executing trades outside designated Kill Zones.
     * Manually moving a resting stop loss.
     * Over-leveraging beyond risk parameters.

## Red Flags

| Red Flag | Rationalization | Why It's Wrong | Correct Action |
| :--- | :--- | :--- | :--- |
| **Out-of-hours breakout** | "This breakout at 11:45 AM ET is highly impulsive and will run without me." | Midday price action is characterized by low institutional participation and high algorithmic manipulation. | Wait for the New York PM Kill Zone (1:30 PM ET) to establish a true directional bias. |
| **Trading unmitigated OBs** | "This single, refined 15m Order Block is perfect; price must bounce here." | Algorithms target broader structural Order Flow (the entire corrective leg) rather than a single refined candle. | Analyze the entire corrective swing leg and look for HTF structural alignment first. |
| **Treating local tick volume as global CVD** | "My MT4 tick volume show huge absorption at this Forex key level." | Spot Forex volume is decentralized; local tick volume is an unreliable proxy for global order flow. | Verify structural shifts using centralized futures market data (6E, ES, NQ) or focus purely on HTF price structures. |
| **Using static sizing under Floating Risk rules** | "I will keep using my standard 2-lot size despite this high-volatility news release." | Modern prop firm engines compress risk limits dynamically; static sizing leads to automated account liquidation. | Adjust position sizing using ATR or contract-based volatility scales to match dynamic drawdown limits. |

## Quick Reference

```
                             [ALGORITHMIC TIME WINDOWS]
 ┌───────────────────────────┬───────────────────────────┬───────────────────────────┐
 │        London Open        │     NY Open/Silver Bullet  │       NY PM Session       │
 │    2:00 AM - 5:00 AM ET   │   8:30 AM - 11:00 AM ET   │    1:30 PM - 4:00 PM ET   │
 └───────────────────────────┴───────────────────────────┴───────────────────────────┘
```

| Setup / Concept | Primary Execution Trigger | Risk Management Key | Target Objective |
| :--- | :--- | :--- | :--- |
| **Unicorn Model** | Horizontal overlap of Breaker Block and FVG during Kill Zone. | Stop placed past the invalidation level of the Breaker. | Next major liquidity pool (high/low). |
| **Reaper Inversion FVG** | Inversion FVG situated within Premium/Discount boundaries of a breaker leg. | Tight invalidation invalidating the Inversion FVG boundary. | Key HTF structural level. |
| **Venom Model** | Boundary test of a horizontal BPR after a confirmed liquidity sweep. | Stop-loss placed immediately behind the BPR structure. | External HTF liquidity pool. |
| **IOFED** | Limit order at the proximal edge of an FVG in high-momentum trends. | Stop-loss placed outside the FVG's originating candle wick. | Nearest liquidity draw or swing target. |
| **Judas Swing** | Aggressive session-start rally/drop sweeping major liquidity. | Wait for confirmation via MSS/CHOCH on lower timeframe. | Expansion to opposite end of daily range. |