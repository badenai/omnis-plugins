---
name: market-structure-liquidity
description: Use when analyzing market structure, identifying shifts (BOS/CHOCH), evaluating liquidity sweeps vs grabs, validating order blocks, and executing setups like the Unicorn, Venom, or Balanced Price Range (BPR) models.
---

## The Iron Law

```text
NEVER execute a trade entry without a confirmed prior sweep of high-timeframe liquidity (PDH/PDL, session extremes, or major swing points) followed by a lower-timeframe market structure shift (MSS/CHOCH) showing aggressive displacement (FVG creation).
```

## Behavioral Rules

*   **Anticipate the AMD Cycle:** If trading the London session (2 AM–5 AM EST), anticipate manipulation (Judas Swing) to sweep Asian range liquidity. If trading the New York AM session (7 AM–12 PM EST), seek true trend expansion (distribution) toward opposing liquidity targets.
*   **Enforce Strict Order Block Validation:** Only validate an Order Block (OB) if it originates from within the swing leg that created a BOS/CHOCH and left behind an unfilled Fair Value Gap (FVG). Invalidate any OB if price has already wicked deeply into it, as its resting institutional orders have been mitigated.
*   **Differentiate Breaker and Mitigation Blocks:** Prioritize Breaker Blocks over Mitigation Blocks. Only classify a zone as a high-probability Breaker Block if the market swept liquidity (creating a higher high/lower low) before violently breaking the last order block. 
*   **Utilize the Balanced Price Range (BPR):** Define a BPR when an aggressive impulse leg is immediately met by an equally aggressive counter-impulse leg, creating overlapping bullish (BISI) and bearish (SIBI) FVGs. Use the boundaries of this horizontal overlap as a low-slippage defense zone for execution.
*   **Isolate Sweeps from Grabs:** Distinguish macro Liquidity Sweeps (broad manipulation beyond major structural extremes like PDH/PDL) from micro Liquidity Grabs (localized, single-candle stop-hunts designed for trend continuation). Do not execute counter-trend reversals on minor localized grabs.
*   **Confirm with SMT Divergence:** Compare highly correlated assets (e.g., EUR/USD and GBP/USD, or S&P 500 and Nasdaq) at key structural levels. If one asset sweeps a key high/low while the other fails to do so, confirm SMT divergence and trade in the direction of the sweeping asset.
*   **Execute the Unicorn Model:** Place limit orders strictly at the horizontal overlap of a valid Breaker Block and an FVG, ensuring the setup resides within a premium/discount pricing array relative to the current swing leg.
*   **Execute the Venom Model:** Following a sweep of major external session liquidity, monitor the lower timeframes for an immediate BPR. Place limit orders directly on the boundary of that BPR for rapid, tight-risk execution.
*   **Adapt with IOFED in High Momentum:** If trading a strongly trending market where deep retracements to the 50% FVG midpoint (Consequent Encroachment) are unlikely, execute via the Institutional Order Flow Entry Drill (IOFED) at the proximal edge of the FVG. Automatically reduce position size to offset the risk of a deeper fill.
*   **Expose Hidden Order Blocks (HOB):** Look for overlapping wicks on higher-timeframe charts (Daily/4H) and drill down to lower timeframes (15M/5M) to locate clean, unmitigated order blocks hidden inside those wicks.
*   **Validate POIs with Footprint Fusion:** When price hits a key HTF structure, do not place blind limits. Wait for passive institutional absorption to show on a footprint chart, requiring a 3-bar Cumulative Delta Divergence and a dominant footprint delta candle before entry.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "This mitigation block doesn't need a prior liquidity sweep because the trend is extremely strong." | Mitigation blocks represent failure swings and lack the trapped institutional liquidity ("rocket fuel") needed to sustain high-probability reversals. |
| "I will place my limit order directly at the FVG Consequent Encroachment without waiting for lower-timeframe validation." | Standard single FVGs act as magnets and can drag price deep into or through their boundaries. Execution without LTF structural shifts leads to unnecessary stop-outs. |
| "I am executing a counter-trend reversal here because this single-candle 5-minute wick represents a major sweep." | Single-candle intraday grabs are localized stop-hunts meant to fuel trend continuation. Trading against the trend on these traps retail traders. |
| "This is a valid Order Block because it represents the last counter-trend candle before a move, even though there is no FVG." | Without displacement and a resulting FVG, there is no proof of institutional urgency or unfilled orders resting at that block. |
| "I will ignore SMT divergence because my individual asset chart looks perfect." | Ignoring SMT divergence means ignoring institutional accumulation/distribution footprints, significantly reducing the probability of a clean expansion. |

## Quick Reference

| Concept | Trigger | Validation Rules | Primary Target |
| :--- | :--- | :--- | :--- |
| **Breaker Block** | Liquidity sweep followed by violent displacement breaking the last OB. | Must have a prior liquidity sweep and leave behind an unfilled FVG. | Opposing external liquidity pool / major swing extreme. |
| **Balanced Price Range (BPR)** | Immediate, overlapping bullish and bearish impulse legs. | Horizontal intersection of a BISI and a SIBI. | Opposing session extremes or unmitigated FVGs. |
| **Unicorn Model** | Price retracing into a premium/discount pricing array. | Precise horizontal overlap of a Breaker Block and an FVG. | Next major structural liquidity pool. |
| **Venom Model** | Session-level external liquidity sweep during a Killzone. | Immediate formation of a lower-timeframe BPR. | Opposing session high/low with mathematically tight stop. |
| **SMT Divergence** | Correlated assets showing non-symmetrical highs or lows. | One asset sweeps a key level while the other fails to do so. | Align execution with the asset that completed the sweep. |
| **IOFED** | High-momentum market structure expansion. | Entry at the proximal edge (beginning) of the FVG. | Nearest structural target with reduced position size. |