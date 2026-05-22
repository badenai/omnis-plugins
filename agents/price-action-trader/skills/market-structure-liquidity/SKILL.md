---
name: market-structure-liquidity
description: Use when mapping internal vs external market structure, evaluating Break of Structure (BOS) vs Change of Character (CHOCH), or identifying Buy-Side/Sell-Side liquidity sweeps (stop hunts) and inducement (IDM) traps.
---

## The Iron Law

```text
Never validate a structural Change of Character (CHOCH) without a preceding algorithmic sweep of a major liquidity pool (Buy-Side/Sell-Side) and subsequent aggressive displacement closing past a true external swing level. Treat all wicks or internal minor structure breaks as Inducement (IDM) traps.
```

## Behavioral Rules

*   **Prioritize Liquidity Sweeps:** Require algorithms to purge critical Buy-Side Liquidity (BSL) or Sell-Side Liquidity (SSL) pools (e.g., Previous Day Highs/Lows, Equal Highs/Lows) before validating any structural reversal bias.
*   **Validate True CHOCH:** Classify a structural shift as a Change of Character (CHOCH) if and only if price closes *with displacement* past a major external swing level.
*   **Identify Inducement (IDM):** Label any price action that merely wicks past a structural level or breaks an internal minor structure as Inducement (IDM); use this to map where algorithms are trapping early retail stop losses.
*   **Filter Internal vs. External Structure:** Differentiate explicitly between internal price legs (minor structure) and external macro swings (major structure) to avoid getting trapped by lower-timeframe noise.
*   **Demand a Catalyst:** Invalidate any trade setup that appears in a vacuum; ensure every high-probability structure shift is initiated by the algorithmic harvesting of external liquidity.
*   **Align Timeframes:** Reject low-timeframe structural shifts if they directly contradict the higher-timeframe external liquidity draw, unless executing purely within a hyper-specific intra-session liquidity sweep.

## Red Flags

| Rationalization | Why Wrong |
| :--- | :--- |
| "Price broke the nearest higher low, so the macro trend has changed." | Breaking an internal minor low is Inducement (IDM) designed to trap early direction traders before the macro trend continues. |
| "The wick crossed the previous day's high, confirming a Break of Structure." | A wick without candle body displacement constitutes a liquidity sweep (stop hunt), not a valid structural break. |
| "There is a clean structural CHOCH here without a prior liquidity sweep." | Institutional reversals do not occur in a vacuum; they strictly require the purging of BSL or SSL pools to acquire positional liquidity. |
| "I am executing a reversal solely based on this 1-minute structural shift." | Low-timeframe structural shifts act as algorithmic noise and traps when divorced from higher-timeframe external liquidity targets. |

## Quick Reference

| Concept | Mechanical Definition | Actionable Trigger |
| :--- | :--- | :--- |
| **CHOCH** | Displacement body close past a major external swing level. | Validate true state shift; look for institutional entry models. |
| **IDM** | Internal minor structure break or a simple wick past a level. | Ignore reversal signals; wait for algorithmic sweep of early trapped traders. |
| **BSL/SSL Sweep** | Wick piercing Previous Day High/Low (PDH/PDL) or Equal Highs/Lows. | Anticipate immediate reversal targeting opposing liquidity pools. |
| **External Structure** | Macro Higher High / Higher Low swing points. | Map as absolute higher-timeframe bias and ultimate take-profit targets. |
| **Internal Structure** | Minor price legs contained inside the current macro leg. | Monitor exclusively to identify Inducement (IDM) timing traps. |