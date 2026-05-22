---
name: market-structure-liquidity
description: Use when you map market structure shifts (BOS, CHOCH), identify internal vs. external liquidity pools, validate high-probability order blocks, and execute precision entries at key institutional liquidity levels.
---

## The Iron Law

```
Never confirm a structural shift (BOS, MSS, or CHOCH) without a full candlestick body close past the key swing point; classify any break executed only by a candlestick wick strictly as a liquidity sweep.
```

## Behavioral Rules

1. Map high-timeframe (HTF) external liquidity pools, including Previous Day High/Low (PDH/PDL) and session extremes, before analyzing lower-timeframe (LTF) structures.
2. Identify the primary draw on liquidity (DOL) as either external range liquidity or internal range liquidity before initiating any execution sequence.
3. If a swing point is broken strictly by a candlestick wick, label it as a liquidity sweep and prepare for potential reversal entries.
4. Require a complete candlestick body close on your validation timeframe to confirm a true Break of Structure (BOS) or Change of Character (CHOCH).
5. Differentiate a true CHOCH from minor Inducement (IDM) by mapping external structural swing highs/lows and marking internal breaks as traps.
6. Validate an Order Block (OB) only if it originates within the leg that created a BOS/CHOCH, sweeps internal liquidity, and displays immediate displacement leaving a clean Fair Value Gap (FVG).
7. Disregard previously mitigated Order Blocks; place entries only at unmitigated proximal edges.
8. Classify a broken block as a Breaker Block only if it swept liquidity prior to the structural shift; classify it as a Mitigation Block if no liquidity sweep occurred.
9. If executing the Unicorn entry model, confirm that a valid Breaker Block directly overlaps with a Fair Value Gap (FVG) or Inverse FVG (iFVG).
10. If executing the Venom entry model, place limit orders strictly at the proximal boundary of a Balanced Price Range (BPR) formed directly after an external liquidity sweep.
11. If utilizing the Liquidity Sweep & MSS Strategy, place your protective stop-loss strictly beyond the swing wick that swept the high-timeframe liquidity.
12. Restrict your search for structural setups to the three precise 60-minute windows: 3:00 AM – 4:00 AM, 10:00 AM – 11:00 AM, and 2:00 PM – 3:00 PM NY time.
13. If a valid MSS and imbalance configuration does not trigger within the designated 60-minute execution window, cancel all resting limit orders and immediately close active intraday positions.

## Red Flags

| Red Flag (Action or Rationalization) | Why Wrong / Correct Rule |
| :--- | :--- |
| Labeling a wick break as a BOS because price moved past the previous swing high. | Classify wicks strictly as liquidity sweeps; do not assume trend continuation without a confirmed candle body close. |
| Entering on any opposing candle labeled as an order block without verifying preceding sweeps or displacement. | Avoid unvalidated blocks; require both a preceding liquidity sweep and a subsequent FVG to prove institutional sponsorship. |
| Treating minor internal structural breaks as trend reversals (CHOCH). | Ignore minor internal breaks; wait for a true body close on external structures to avoid entering during minor pullbacks. |
| Executing long positions in premium arrays or short positions in discount arrays. | Map your current dealing range; ensure long entries are placed strictly in discount zones and short entries strictly in premium zones. |
| Treating Mitigation Blocks with the same win probability as Breaker Blocks. | Prioritize Breaker Blocks over Mitigation Blocks; expect Mitigation Blocks to fail more frequently due to the absence of a liquidity sweep. |

## Quick Reference

| Concept | Mechanical Definition | Execution Trigger |
| :--- | :--- | :--- |
| **True CHOCH** | Confirm via a candle body close past a major external swing high or low. | Wait for the displacement leg to form a valid FVG before executing an entry. |
| **Liquidity Sweep** | Identify a wick-only penetration of PDH/PDL or session extremes. | Wait for a lower-timeframe Market Structure Shift (MSS) with aggressive displacement. |
| **Breaker Block** | Locate a broken Order Block that swept liquidity before the structural break. | Enter at the proximal edge where the block overlaps with an FVG (Unicorn setup). |
| **Balanced Price Range (BPR)** | Locate the exact horizontal overlap of aggressive bullish and bearish FVGs. | Set limit orders at the proximal boundary immediately after a liquidity sweep. |
| **Inducement (IDM)** | Identify minor internal structural breaks designed to trap early breakout traders. | Do not execute; wait for these internal highs/lows to be swept before hunting a setup. |