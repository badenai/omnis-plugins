---
name: volume-microstructure-logic
description: Use when processing order book depth arrays, mapping open interest liquidation cascades, analyzing order flow imbalance (OFI), or building session-normalized volume profile and POC mean-reversion rules.
filePattern: "**/*.py"
bashPattern: "pytest|unittest"
---

## The Iron Law

```text
You must formalize all volume and market microstructure logic into strict, deterministic arrays, replacing visual profile concepts and subjective tape reading with explicitly defined array index inequalities, absolute price differentials, and N-bar mathematical windows.
```

## Behavioral Rules

- Extract Order Flow Imbalance (OFI) strictly from Depth-5 (L=5) limit order arrays to bypass L=1 spoofing noise using programmed boolean gates.
- Calculate forced-closure liquidation entry proxies by correlating Open Interest (OI) density arrays against funding rate extremes using strict arithmetic thresholds.
- Normalize all volume feature arrays by exact session time boundaries (e.g., 09:30-10:30 EST) to programmatically filter idiosyncratic execution volume spikes.
- Require boolean validation of positive volume delta expansion when coding structural breakouts; if an N-bar array shows price expansion paired with decreasing volume arrays, flag the event immediately as an exhaustion/absorption failure.
- Set mean-reversion algorithmic limits strictly to the dynamic Point of Control (POC) baseline if a price array registers a confirmed closing index inside the Value Area from a previously unshaded excess zone.
- Manage volume thresholds and microstructure invalidation levels dynamically using an ATR volatility multiplier to scale absolute price differentials, ensuring stops are mathematically tied to true market depth.
- Prevent structural array pollution by explicitly stripping all ML/AI classification buzzwords (like K-Nearest Neighbors or RANSAC) from your order flow algorithms, relying instead on unambiguous boolean states and strict array slicing.

## Red Flags

| Red Flag | Why Wrong |
| :--- | :--- |
| Writing "price exhibits upward kinematic velocity." | Contaminates code with physics jargon; strictly use absolute price differentials and N-bar array index inequalities. |
| Relying on top-of-book (L=1) tape reading logic. | L=1 is highly susceptible to spoofing; mandate Depth-5 volumetric arrays for OFI evaluation. |
| Utilizing "ML-based volume confidence clusters." | Replaces computable deterministic logic with opaque machine learning buzzwords; use standard deviation thresholds and boolean gates. |
| Building variables like `MarketPanic = True`. | Assumes subjective emotional states; use explicit Open Interest limits and absolute mathematical slippage constraints. |
| Hardcoding static volume limits globally. | Fails to account for session-specific variance; always apply Time-Indexed Volume Array Normalization. |

## Quick Reference

| Concept | Deterministic Implementation |
| :--- | :--- |
| **Liquidation Targets** | OI Density Array × Funding Rate Minimum Arithmetic Threshold |
| **Order Flow Imbalance** | Depth-5 Volumetric Delta Boolean Comparison |
| **HVN Mean Reversion** | Value Area Bounds Array Check (Strict `True`/`False` gate) |
| **POC Gap Target** | Session-Validated 98.5% Mean Reversion Price Constant |
| **Volume Exhaustion** | N-Bar Price Array Breakout + Decreasing Volume Array Index |
| **Volatility Scaling** | ATR Volatility Threshold × Absolute Price Differential |