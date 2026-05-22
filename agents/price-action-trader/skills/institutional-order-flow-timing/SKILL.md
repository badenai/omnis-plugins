---
name: institutional-order-flow-timing
description: Use when validating institutional Order Blocks (OB), detecting algorithmic displacement/delivery, or verifying multi-timeframe structural alignment.
---

## The Iron Law

```text
An Order Block (OB) is strictly INVALID unless the subsequent displacement candle closes past the structural point, leaves a clear, unmitigated Fair Value Gap (FVG), and the OB's proximal edge remains completely untouched prior to the entry execution.
```

## Behavioral Rules

*   **If** identifying a potential Order Block (OB), **then** confirm it originated within a price leg that successfully swept internal liquidity and created a Break of Structure (BOS) or Change of Character (CHOCH).
*   **Never** classify an opposing candle as a valid OB if the subsequent displacement leg fails to leave a clean, unmitigated Fair Value Gap (FVG).
*   **If** analyzing market structure shifts, **then** require a complete candle body close past the key external swing level; treat wicks strictly as liquidity sweeps and never as structural trend shifts.
*   **If** executing the Breaker Block model, **then** ensure that price swept liquidity (e.g., a stop hunt forming a higher high or lower low) immediately prior to the displacement and structural breach.
*   **If** trading the Unicorn Model, **then** locate the direct geometric overlap between a valid Breaker Block and an FVG or Inverse FVG (iFVG) on the execution chart.
*   **If** deploying the Venom Model, **then** place execution limit orders exactly at the proximal boundary of the Balanced Price Range (BPR) immediately following a verified liquidity sweep.
*   **If** implementing the Institutional Order Flow Entry Drill (IOFED), **then** place the limit entry order precisely at the proximal edge of the FVG to minimize drawdowns, avoiding standard 50% equilibrium retracement entries on high-velocity moves.
*   **Strictly** restrict all entry execution triggers to the three daily Silver Bullet timing windows: 3:00 AM – 4:00 AM NY (London Open), 10:00 AM – 11:00 AM NY (NY AM), and 2:00 PM – 3:00 PM NY (NY PM).
*   **If** the planned institutional setup (sweep, displacement, and FVG/BPR formation) does not fully trigger within the active 60-minute window, **then** instantly cancel all pending limit orders, close open intraday targets, and exit the screen.

## Red Flags

| Domain-Specific Rationalizations | Why Wrong |
| :--- | :--- |
| "This down-candle is a valid Order Block because price moved up aggressively from it later." | **Wrong.** Without immediate displacement leaving an FVG on the initial move, it represents retail support/resistance, not institutional block validation. |
| "A high-timeframe wick went past the key swing point, confirming a market structure shift (CHOCH)." | **Wrong.** Wicks are liquidity sweeps (stop hunts) that signal manipulation; true structural shifts demand a full candle body close. |
| "Entering a Mitigation Block because it is cheaper than waiting for a Breaker Block." | **Wrong.** Mitigation Blocks lack a prior liquidity sweep to trap counter-trend traders, making them highly vulnerable to being swept as Inducement (IDM). |
| "Taking an FVG entry after price has already wicked into and mitigated the zone." | **Wrong.** Once price mitigates an FVG or touches the proximal edge of an OB, the resting institutional orders are already filled and the setup is dead. |
| "Executing an SMC entry at 11:30 AM NY because the pattern is too perfect to ignore." | **Wrong.** Algorithmic delivery patterns are strictly time-bound. Trading outside the designated execution windows leaves you vulnerable to low-volume retail noise. |

## Quick Reference

| Concept | High-Probability Trigger Conditions | Execution / Risk Rules |
| :--- | :--- | :--- |
| **Order Block (OB)** | Sweeps liquidity + breaks structure + leaves FVG. | Enter at proximal edge; stop loss strictly past block invalidation. |
| **Breaker Block** | Broken OB that was run through *after* a liquidity sweep. | Enter on retest of the broken block's boundary; high momentum expected. |
| **Balanced Price Range (BPR)** | Bidirectional violent displacement forming overlapping FVGs. | Place limit order at proximal boundary of BPR; highly compressed stop loss. |
| **Unicorn Model** | Coincidence of a valid Breaker Block and a fresh FVG / iFVG. | Enter on first retest of the overlapping confluence zone. |
| **IOFED Drill** | High-velocity displacement leaving a clear FVG. | Enter strictly at the proximal edge of the FVG; target next liquidity pool. |
| **Silver Bullet Execution** | Setups forming within 3-4 AM, 10-11 AM, or 2-3 PM NY time. | Cancel all orders if not filled within the exact 60-minute window. |