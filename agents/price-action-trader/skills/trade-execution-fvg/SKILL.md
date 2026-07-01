---
name: trade-execution-fvg
description: Use when analyzing market structure shifts, identifying Fair Value Gaps (BISI/SIBI), determining Premium/Discount pricing arrays, and executing orders via Unicorn, Venom, or Balanced Price Range (BPR) entry models.
---

## The Iron Law

```
Never execute a buy-side entry in Premium pricing or a sell-side entry in Discount pricing, and instantly invalidate any Fair Value Gap (FVG) entry if price closes a candle body past its Consequent Encroachment (50% midpoint).
```

## Behavioral Rules

*   **Determine Pricing Arrays First:** Always calculate the dealing range using a Fibonacci retracement from swing low to swing high before plotting entries. Limit buy executions strictly to the Discount zone (<50%) and sell executions strictly to the Premium zone (>50%).
*   **Validate the FVG Sequence:** Classify bullish imbalances as BISI (Buyside Imbalance Sellside Inefficiency) and bearish imbalances as SIBI (Sellside Imbalance Buyside Inefficiency) only when a three-candle sequence shows rapid displacement.
*   **Enforce Consequent Encroachment:** Plot the exact 50% midpoint (Consequent Encroachment) of every targeted FVG. Set alert notifications at this level and treat a candle body close past it as an automatic invalidation signal.
*   **Execute the Unicorn Model:** Trigger entries only at the horizontal overlap of a Breaker Block and an FVG. Place the entry at the proximal boundary of the FVG, position the stop loss behind the Breaker's structural swing extreme, and reject the setup if the block failed to sweep liquidity (Mitigation Block).
*   **Map Balanced Price Ranges (BPR):** Identify BPRs only where a displaced FVG in one direction is immediately overrun by an opposing FVG over the exact same price zone. Execute limit orders at the BPR equilibrium during session Killzones for near-zero-drawdown entries.
*   **Filter Order Blocks (OB):** Validate an OB for execution only if it originated the move creating a BOS/CHOCH, left an immediate FVG, and remains completely unmitigated. Instantly reject any second-touch mitigation setups.
*   **Align Execution with Killzones:** Restrict all execution triggers to the London session (2 AM - 5 AM EST) or New York AM session (7 AM - 12 PM EST). Invalidate any setups that form during low-volume Asian or off-session hours.

## Red Flags

| Red Flag (Retail Rationalization) | Why It Is Wrong |
| :--- | :--- |
| "Entering a long inside a BISI in the upper 30% of the dealing range because the trend is extremely strong." | Violates the premium/discount rule; buying in premium exposes the account to deep institutional stop hunts. |
| "Executing a Unicorn model entry using a Mitigation Block because no Breaker Block is available." | Mitigation blocks do not sweep liquidity and lack the cleared stop-loss "fuel," leading to high failure rates. |
| "Keeping an FVG entry active after a high-timeframe candle closes past its Consequent Encroachment." | A body close past the 50% midpoint of an FVG indicates structural invalidation and an institutional failure to defend the imbalance. |
| "Re-entering an Order Block on its second or third touch because it held beautifully the first time." | Mitigated blocks have already cleared their resting institutional orders; subsequent touches have a severely compromised edge. |
| "Executing FVG entries outside of defined London or New York session Killzones." | Low-volume hours lack institutional algorithmic delivery, turning FVGs into retail traps. |

## Quick Reference

| Setup / Array | Execution Trigger | Stop Loss Placement | Validation Key |
| :--- | :--- | :--- | :--- |
| **BISI (Bullish FVG)** | Entry at proximal boundary inside Discount zone (<50%) | Just below Candle 1 low of the FVG sequence | Must not close a candle body below Consequent Encroachment (50%) |
| **SIBI (Bearish FVG)** | Entry at proximal boundary inside Premium zone (>50%) | Just above Candle 1 high of the FVG sequence | Must not close a candle body above Consequent Encroachment (50%) |
| **Unicorn Model** | Entry at the horizontal overlap of Breaker Block and FVG | Tucked behind the Breaker's structural swing extreme | Breaker must have successfully swept liquidity |
| **Venom / BPR** | Entry at the horizontal overlap of the dual opposing FVGs | Just past the invalidation level of the BPR zone | Execution must occur within London/NY Killzones |