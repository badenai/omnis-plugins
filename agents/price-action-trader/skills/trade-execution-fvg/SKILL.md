---
name: trade-execution-fvg
description: Use when validating, filtering, and executing trade entries based on algorithmic market imbalances, Fair Value Gaps (FVG), Balanced Price Ranges (BPR), and specific execution models including the Unicorn, Venom, and IOFED setups.
---

## The Iron Law

```
Never validate, map, or execute trades on any FVG, BPR, or associated entry setup if the displacement candles forming the imbalance possess a body-to-wick ratio below 70%.
```

## Behavioral Rules

*   **Apply the 70% Candle Filter:** Measure the body-to-wick ratio of the displacement candle forming the FVG or BPR. If the ratio is below 70%, immediately discard the setup as it indicates poor institutional sponsorship and reduces expected value to 1.3R.
*   **Execute the Unicorn Setup:** Enter only when a high-volume FVG horizontally overlaps with a validated Breaker Block. You must confirm that this confluence occurs after a liquidity sweep of a major swing high/low and an aggressive Market Structure Shift (MSS).
*   **Filter Out Mitigation Overlaps:** Reject any "Unicorn" variation that uses a Mitigation Block. You must verify a clear liquidity sweep (stop hunt) prior to the structural shift to ensure the block is a true Breaker Block.
*   **Execute the Venom Setup:** Limit Venom model entries strictly to defined session Killzones. You must confirm an immediate liquidity sweep followed instantly by the formation of a Balanced Price Range (BPR).
*   **Validate the Balanced Price Range (BPR):** Map a BPR only when an aggressive displacement move is immediately neutralized by an aggressive opposing displacement move, creating a clean horizontal overlap of a bullish FVG and a bearish FVG.
*   **Execute the IOFED Setup:** Place limit orders precisely at the proximal edge of the FVG when trading the Institutional Order Flow Entry Drill (IOFED) to capture high-momentum expansions.
*   **Enforce IOFED Invalidation:** Cancel the IOFED limit order immediately if price closes beyond the 50% consequent encroachment level of the FVG before triggering your entry.
*   **Align with Premium/Discount Arrays:** Only execute long entries at FVGs/BPRs residing within a discount of the current structural range, and short entries at FVGs/BPRs residing within a premium of the current structural range.

## Red Flags

| Domain-Specific Rationalization | Why It Is Wrong |
| :--- | :--- |
| "This FVG is massive and highly visible, so it should act as strong magnetic support even though the candle is mostly wicks." | Candles with less than 70% body-to-wick ratios signify weak displacement and retail participation, dropping trade expectancy significantly. |
| "I am executing a Unicorn setup on a Mitigation Block overlap because the structural shift was clean." | Mitigation blocks represent trend fatigue and failure swings without a liquidity sweep. A true Unicorn setup strictly requires a Breaker Block to guarantee swept resting liquidity. |
| "I will leave my IOFED limit order open because a deeper pullback into the FVG gives me a better risk-to-reward ratio." | IOFED relies on extreme institutional momentum that must respect the proximal edge. Pulling deeper than 50% (consequent encroachment) invalidates the momentum thesis of the drill. |
| "Trading a Venom setup during the late-day quiet hours since the BPR is perfectly formed on the 5-minute chart." | Venom models are highly dependent on algorithmic volatility. Trading them outside of primary session Killzones exposes you to low-volume consolidation and market maker manipulation. |

## Quick Reference

| Setup / Concept | Core Validation Filter | Execution Trigger | Invalidation Level |
| :--- | :--- | :--- | :--- |
| **Unicorn Model** | FVG overlaps a Breaker Block + HTF liquidity sweep + MSS. | Touch of the horizontal FVG-Breaker overlap zone. | Close beyond the opposite boundary of the Breaker Block. |
| **Venom Model** | BPR formation + session Killzone + immediate counter-displacement. | Direct entry on the horizontal overlap of the bullish/bearish FVGs. | Close outside the outer boundary of the BPR. |
| **IOFED** | Displacement candle body-to-wick ratio > 70% + strong momentum trend. | Limit order resting at the proximal edge of the FVG. | Candle close past the 50% consequent encroachment level. |
| **Balanced Price Range (BPR)** | Successive, overlapping opposing FVGs neutralizing each other. | First return to the shared horizontal overlap area. | A body close outside the extreme wick of the overlapping candles. |