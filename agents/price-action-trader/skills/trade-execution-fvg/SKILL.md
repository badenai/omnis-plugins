---
name: trade-execution-fvg
description: Use when analyzing trade entry points, placing limit orders at Fair Value Gaps (FVG), Balanced Price Ranges (BPR), Order Blocks (OB), or determining execution mechanics within the Unicorn Model and IOFED frameworks.
---

## The Iron Law

```text
Never execute a trade without violent structural displacement that leaves a clear price vacuum (FVG); you must mechanically align your entry with an unmitigated institutional defense zone (OB, BPR, or Breaker) and place your stop loss strictly beyond the originating invalidation wick.
```

## Behavioral Rules

*   **Mechanical Order Block Validation:** If labeling an Order Block (OB), strictly require three conditions before executing: it must originate a structural break that sweeps internal liquidity, be followed immediately by displacement leaving an FVG, and remain 100% unmitigated. 
*   **Unicorn Model Execution:** When a Higher Timeframe Breaker Block or Order Block overlaps directly with a newly formed FVG, execute aggressively at this double-confirmation zone; do not wait for secondary lower-timeframe confirmation.
*   **BPR (Balanced Price Range) Exploitation:** If price forms overlapping bullish and bearish FVGs (an immediate aggressive reversal), treat the resulting BPR as a zero-drawdown defense zone; execute your limit order directly on the retest of the BPR edge.
*   **IOFED (Institutional Order Flow Entry Drill) Protocol:** If executing for maximum Risk-to-Reward, enter strictly at the proximal edge of the FVG rather than waiting for 50% Equilibrium (EQ); accept the higher rate of missed fills in exchange for highly asymmetric R:R.
*   **Strict Invalidation Placement:** When executing any FVG or OB setup, place your stop loss strictly beyond the absolute extreme wick of the originating liquidity sweep; never widen the stop if price draws deeper into the zone.
*   **Ignore Unaligned Vacuums:** If an FVG appears on a lower timeframe (e.g., 1-minute) but lacks Higher Timeframe directional alignment or does not originate from a major liquidity sweep, ignore it entirely; treat it as an algorithmic inducement trap.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "Any opposite-colored candle before a big move is a valid Order Block to trade from." | Retail trap; valid OBs must explicitly sweep internal liquidity, leave an FVG via displacement, and remain entirely unmitigated. |
| "I will wait for a lower-timeframe CHOCH inside this HTF Unicorn setup to be safe." | Unicorn setups (OB/Breaker + FVG) are inherently double-confirmed; waiting for low-timeframe noise causes missed entries and ruins R:R. |
| "Price broke the sweep wick, but I will scale into this FVG because the HTF trend is strong." | Once the structural invalidation wick is breached, the institutional premise is void; scaling in turns mechanical risk management into a gamble. |
| "I will wait for the FVG to hit 50% Equilibrium to ensure I get a better average price." | For aggressive displacement, price often only taps the proximal edge (IOFED); demanding the EQ fill guarantees missed high-momentum executions. |

## Quick Reference

| Execution Framework | Execution Criteria & Mechanical Action |
| :--- | :--- |
| **Mechanical Order Block** | Require liquidity sweep + displacement + FVG + 100% unmitigated state. Enter on first touch. |
| **Unicorn Model** | Identify HTF Breaker/OB overlapping with a fresh FVG. Execute aggressively at the overlap edge. |
| **Balanced Price Range** | Identify overlapping opposing FVGs. Execute limit order at the external edge of the neutralized zone. |
| **IOFED Approach** | Enter precisely at the proximal edge of the FVG to prioritize asymmetric Risk-to-Reward. |
| **Invalidation Rule** | Place hard stop strictly beyond the wick of the originating liquidity sweep. |