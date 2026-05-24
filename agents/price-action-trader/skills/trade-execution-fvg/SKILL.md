---
name: trade-execution-fvg
description: Use when executing trades, validating Fair Value Gaps (FVG), analyzing Balanced Price Ranges (BPR), confirming high-probability institutional Order Blocks (OB), or optimizing entry mechanics like the Unicorn, Venom, or IOFED models within premium and discount zones.
---

## The Iron Law

```text
NEVER execute an entry on a mitigating touch of an execution array (OB, FVG, or BPR) unless it is the absolute FIRST touch of a completely unmitigated zone, aligned strictly within a Premium/Discount pricing boundary, and characterized by energetic body-close displacement.
```

## Behavioral Rules

*   **Validate Order Blocks (OB)** strictly by ensuring they initiated a structural break (BOS/CHOCH), left a clear unmitigated FVG, and represent the absolute first mitigation touch.
*   **Prioritize Breaker Blocks** over Mitigation Blocks for entries, verifying first that the Breaker successfully swept liquidity before the structural shift occurred.
*   **Map Balanced Price Ranges (BPR)** by identifying the exact horizontal overlap where a bullish FVG and a bearish FVG neutralize each other.
*   **Execute BPR entries** at the immediate horizontal edge to minimize drawdown, and set invalidation rules to trigger on a candle body close outside the BPR boundary.
*   **If executing via the Unicorn Model**, confirm the entry zone is the precise horizontal intersection of a Breaker Block (BB) and an overlapping FVG.
*   **Discard the Unicorn setup immediately** if price action exhibits grinding, overlapping, or wick-heavy consolidation instead of clear, rapid displacement.
*   **If trading the Venom Model**, execute entries strictly at the boundaries of a BPR that forms immediately following an external liquidity sweep, restricted to specific macro timing windows.
*   **When executing the Institutional Order Flow Entry Drill (IOFED)**, place limit orders precisely at the proximal (outer) edge of the FVG.
*   **Position the IOFED stop loss** strictly beyond the FVG boundary to protect capital against deep retracements.
*   **If trading high-volume sweeps at HTF POIs**, verify institutional absorption on the footprint chart using Cumulative Delta Divergence over 3+ consecutive bars before executing market entries.

## Red Flags

| Retail Rationalization | Why Wrong (Execution Rule) |
| :--- | :--- |
| "Entering at 50% Consequent Encroachment of an FVG guarantees a safer fill." | **Do not assume a deep fill.** Strong institutional displacement often leaves the trade behind; prioritize proximal execution (IOFED) when momentum is high. |
| "Execute entries on any visible Order Block to capture the reversal." | **Never execute on mitigated or weak OBs.** Only execute if the OB has left a clear FVG and represents the absolute first mitigation touch. |
| "Trade standard FVGs during low-volume grinding price action." | **Avoid grinding ranges.** Only execute on FVGs formed by high-displacement, wide-range candles, as low-volume gaps are highly prone to being swept. |
| "Treat any broken order block as a high-probability Breaker Block." | **Do not misclassify blocks.** A block is only a Breaker if it successfully swept liquidity before the structure shift; otherwise, classify it as a lower-probability Mitigation Block. |

## Quick Reference

| Execution Model | Entry Trigger Point | Stop-Loss Placement | Invalidation Metric |
| :--- | :--- | :--- | :--- |
| **Unicorn Model** | Intersection of Breaker Block & FVG | Just beyond the Breaker Block high/low | Presence of grinding or wick-heavy price action |
| **Venom Model** | Proximal boundary of the BPR | Body close past opposite BPR boundary | Execution outside of designated Macro windows |
| **IOFED** | Proximal (outer) edge of the FVG | Just beyond the FVG structural boundary | Deep retracement violating the FVG limit |
| **BPR Execution** | Immediate outer edge of overlapping FVGs | Body close outside the BPR boundary | Failure of immediate price rejection at the level |