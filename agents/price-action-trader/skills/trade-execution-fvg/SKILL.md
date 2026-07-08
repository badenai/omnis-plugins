---
name: trade-execution-fvg
description: Use when validating market imbalances, executing Fair Value Gaps (FVG) or Inverse FVGs (IFVG), verifying structural entries (Unicorn model), and configuring risk parameters or position sizing on active trade setups.
---

## The Iron Law

```
Never execute a market entry on a Fair Value Gap (FVG) or Balanced Price Range (BPR) unless the displacement candle body-to-wick ratio is strictly above 70%, the setup occurs within a designated session Killzone, and the stop-loss is placed beyond the structural extreme of the displacement leg.
```

## Behavioral Rules

1. **Verify Displacement Intensity:**
   * **If** a Fair Value Gap (FVG) or Balanced Price Range (BPR) forms with a displacement candle body-to-wick ratio below 70%, **then** invalidate the setup immediately and do not execute an entry.
   * **If** the candle body-to-wick ratio is 70% or greater, **then** mark the zone as valid for execution on a structural retest.

2. **Execute Strictly Inside Session Killzones:**
   * **If** a setup triggers outside of the London Open (2:00 AM – 5:00 AM ET), New York Open / Silver Bullet (8:30 AM – 11:00 AM ET), or New York PM Session (1:30 PM – 4:00 PM ET), **then** deny execution. 
   * **If** the trade setup forms within these exact algorithmic timing windows, **then** proceed to structural confirmation.

3. **Validate the ICT Unicorn Model:**
   * **If** executing the Unicorn Model, **then** verify the direct horizontal overlap of a Breaker Block (BB) and a Fair Value Gap (FVG) following a session liquidity sweep.
   * **If** a subsequent candle body closes beyond the outer anchor point of the initial sweep wick, **then** immediately invalidate the entire setup.

4. **Apply Inverse Fair Value Gap (IFVG) Rules:**
   * **If** price closes decisively beyond a bullish FVG on a candle body close, **then** flip the zone into a bearish IFVG (resistance).
   * **If** price closes decisively beyond a bearish FVG on a candle body close, **then** flip the zone into a bullish IFVG (support).

5. **Locate Target Midpoints:**
   * **If** executing an entry at a Fair Value Gap, **then** plot the Consequent Encroachment (CE) at exactly the 50% midpoint of the FVG as a key institutional magnet and limit order placement area.

6. **Enforce the Three-Mistake Circuit Breaker:**
   * **If** three operational errors are committed in a single session (e.g., executing out of hours, manual stop widening, or over-leveraging), **then** enforce an immediate platform shutdown for the remainder of the day.

## Red Flags

| Red Flag | Rationalization | Why Wrong |
| :--- | :--- | :--- |
| **Trading Low-Body Candles** | "The FVG is wide, so it must represent strong institutional presence regardless of the wicks." | **Imbalance Failure:** Candles with large wicks and low body ratios (< 70%) indicate high intraday volatility and rejection/absorption, not aggressive single-sided price delivery. |
| **Executing Outside Killzones** | "The structure is too clean to ignore, even if it is during the lunch hour lull." | **Liquidity Traps:** Volume drops outside session killzones; algorithms hunt low-volume retail liquidity, resulting in high slippage and false structural shifts. |
| **Widening Stop Losses** | "I will give the trade some room to breathe past the sweep candle wick and move my stop." | **Account Destruction:** Widening stops violates fixed-risk parameters, invalidates the trade's mathematical probability, and fosters toxic emotional trading behavior. |
| **Treating Sweeps as CHoCH** | "A wick swept the high/low, so we have a structural change of character." | **Fakeout Bias:** A true CHoCH requires a definitive body close past structural levels. Wicks alone are stop hunts/sweeps, which deliver price in the opposite direction. |

## Quick Reference

| Setup Model | Required Confluences | Stop-Loss Placement | Profit Target |
| :--- | :--- | :--- | :--- |
| **ICT Unicorn** | Breaker Block + FVG overlap + Sweep | Beyond the outer anchor of the sweep wick | Key opposing HTF liquidity pool |
| **Inverse FVG (IFVG)** | Decisive body close past invalid FVG | Beyond the body close of the inversion candle | Unmitigated HTF Order Block / CE |
| **BPR Quality Entry** | Overlapping Bull/Bear FVGs + >70% body-to-wick | Beyond the swing high/low of the BPR leg | Nearest major external range liquidity |
| **Standard FVG (BISI/SIBI)**| HTF alignment + Killzone + Sweep of liquidity | Beyond the displacement candle origin | Consequent Encroachment (CE) or opposing range |