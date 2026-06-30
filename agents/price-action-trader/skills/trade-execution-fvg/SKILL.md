---
name: trade-execution-fvg
description: Use when validating point-of-interest structures, executing market entries using Fair Value Gaps (BISI, SIBI, CE, BPR), mapping order block mitigations, or confirming micro-entries via footprint data.
---

## The Iron Law

```
Never enter a trade on an order block or Fair Value Gap (FVG) that lacks violent displacement (leaving a fresh, unmitigated imbalance) or has already been previously mitigated.
```

## Behavioral Rules

*   **Order Block Validation:** Only validate an Order Block if it originates from within the swing leg that created a Break of Structure (BOS) or Change of Character (CHOCH) and swept internal liquidity.
*   **Displacement Requirement:** Ensure the immediate subsequent price action shows violent displacement, leaving behind an unfilled Fair Value Gap (FVG) to prove institutional urgency.
*   **Mitigation State:** Execute entries exclusively on the first touch (unmitigated state) of an Order Block; do not trade subsequent retests.
*   **FVG & Consequent Encroachment:** If executing standard FVG entries, place limit orders at the Consequent Encroachment (50% midpoint) of the FVG.
*   **High-Momentum Execution (IOFED):** If executing in high-momentum trends where deep retracements are unlikely, apply the Institutional Order Flow Entry Drill (IOFED) by entering at the proximal edge of the FVG.
*   **Imbalance Invalidative Closes:** Do not trade an FVG if price has already closed past its Consequent Encroachment on the higher timeframe.
*   **Balanced Price Range (BPR) Construction:** Construct a Balanced Price Range (BPR) by identifying the exact horizontal overlap of a bullish FVG (BISI) and a bearish FVG (SIBI).
*   **BPR Boundary Execution:** Place limit orders at the outer boundaries of a BPR to secure low-slippage entries with minimal drawdown.
*   **Unicorn Model Verification:** When using the Unicorn Model, execute only if a Breaker Block and an FVG overlap horizontally within a premium or discount pricing array.
*   **Venom Model Execution:** When using the Venom Model, wait for an external liquidity sweep during a session Killzone, then execute immediately at the boundary of the newly formed lower-timeframe BPR.
*   **Order Flow & Footprint Confirmation:** Avoid placing blind limit orders at key Points of Interest (POIs); confirm absorption first via a 3-bar Cumulative Delta Divergence on the execution timeframe (1m/3m footprint charts).
*   **Delta Trigger Confirmation:** Trigger execution only when a dominant footprint delta candle emerges alongside confirmation from the Time & Sales (T&S) aggression ratio.
*   **Hidden Order Blocks (HOB):** If utilizing Hidden Order Blocks (HOB), drill down to the 15-minute or 5-minute timeframe to locate the exact body overlaps of HTF wicks before refining your entry.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "The market touched the Order Block, so I must enter on the second retest." | OB has already been mitigated; the first touch is the only high-probability entry. |
| "This FVG is huge, so it will definitely act as support." | Large single FVGs act as magnetic voids and can pull price deep into them, causing excessive drawdown. Use a BPR or CE instead. |
| "The price broke structure with tiny, overlapping candles, but there's a block there." | Lack of displacement proves institutional absence; a valid block requires a clean, aggressive break leaving an unfilled FVG. |
| "Entering on this Mitigation Block because it looks like a Breaker." | If no liquidity pool was swept before the structural break, the block lacks the "rocket fuel" necessary for reversal and has a high failure rate. |
| "Placing my stop-loss at the exact edge of the FVG." | Placing stops too close to the proximal edge of an FVG leads to premature stop-outs; stops must be placed beyond the invalidation level (the candle high/low that formed the FVG). |

## Quick Reference

| Setup Type | Key Identification Criteria | Execution Strategy |
| :--- | :--- | :--- |
| **Unicorn Model** | Overlapping Breaker Block + FVG inside premium/discount array | Limit order inside overlap zone; stop-loss placed beyond the Breaker Block. |
| **Venom Model** | BPR formation following HTF external liquidity sweep in a session Killzone | Limit at the BPR boundary; target opposing external liquidity with highly compressed risk. |
| **IOFED** | Strongly trending market with unfilled FVG | Place entry at the proximal edge of the FVG; target next structural liquidity pool. |
| **BPR Entry** | Horizontally overlapping BISI and SIBI | Execute limit at BPR boundary; defense of the boundary yields low-slippage support/resistance. |
| **Consequent Encroachment (CE)** | Deep FVG retracement setup | Limit order placed exactly at the 50% midpoint of the FVG; invalidates if price closes past CE on HTF. |