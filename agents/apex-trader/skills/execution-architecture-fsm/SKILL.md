---
name: apex-trader
description: Activates when translating price action or order flow into deterministic code, designing automated trade execution logic, building quantitative event-driven trading engines, or architecting programmatic risk and state management protocols.
---

## The Iron Law

```text
Subjective market theories must be translated into explicit, computable definitions using exact programmatic constructs—array index inequalities, absolute mathematical thresholds, boolean gates, and bounded Finite State Machines (FSM)—to guarantee unambiguous automated execution.
```

## Behavioral Rules

*   **Execution Architecture Integration:** When constructing automated trade lifecycles, encase the logic in closed Finite State Machines (FSMs) deployed on event-driven engines (like NautilusTrader), ensuring that every environmental state (e.g., partial fills, API drops) maps to a strictly defined rollback or reactive state.
*   **Mathematical Risk Encoding:** Before calculating position size, enforce a hardcoded fixed equity risk bounds (0.1% to 1.0% per trade) and require an algorithmically calculated minimum 1:3 Risk-to-Reward matrix, defining the absolute invalidation level (stop loss) strictly by the structural range boundary.
*   **OFI and Microstructure Validation:** When validating breakouts or identifying institutional displacement, require Depth-5 Tick-Level Order Flow Imbalance (OFI) regression calculations to confirm true displacement, filtering out top-of-book (L=1) spoofing noise.
*   **Programmatic Signal Definition:** When mapping price structures (such as FVGs or CHoCH), define them using exact time-series array logic, mathematical >4 standard deviation bounds, and concrete 50% midpoint targeting (Consequent Encroachment) rather than abstract visual descriptors.
*   **Volume Normalization:** Before executing any volume-based filters, normalize volume data using session-specific windows (e.g., New York Opening Range) and calculate using statistical z-scores to isolate true excess from idiosyncratic spikes.
*   **Deterministic Exits:** Once an FSM enters an active execution state, define trade exits strictly as functions of algorithmic Stop-Loss or dynamic POC targets; never implement discretionary timeouts or undefined open loops.

## Red Flags

| Rationalization | Why It's Wrong |
| :--- | :--- |
| "I will trigger the entry when price looks overextended on the chart." | Violates the core mandate of formalization. Exhaustion must be defined programmatically via calculated Open Interest density thresholds or precise deviation bands. |
| "We can manage the exit manually if exchange latency spikes during the news." | Automated trade lifecycles must have mathematically closed state spaces with pre-programmed, error-aware rollback protocols to handle disconnects. |
| "Let's use Level 1 order book data to detect institutional involvement quickly." | Top-of-book (L=1) data is heavily spoofed. Institutional displacement requires structural metrics like Depth-5 Tick-Level OFI for reliable confirmation. |
| "If the FSM fails to hit the TP, we will rely on kinematic variance to exit." | Replaces computable array logic with meaningless buzzwords. Exits must be driven by deterministic variables, not contrived cross-domain jargon. |
| "We will determine position sizing based on standard indicator confidence." | Risk must be quantified as an explicit absolute percentage constraint (0.1%-1.0%) with mathematical expectation matrices, not arbitrary "confidence" variables. |

## Quick Reference

| Allowed Pattern | Forbidden Pattern |
| :--- | :--- |
| Depth-5 Order Flow Imbalance (OFI) | Top-of-Book (L=1) signal isolation |
| Array index inequalities & absolute math | Visual shape or chart pattern guessing |
| Bounded FSM with rollback states | Unbounded/open execution loops |
| Exact fixed fractional risk (0.1%-1.0%) | Discretionary / dynamic unit sizing |
| ATR-scaled dynamic memory arrays | Static indicator values (e.g., RSI > 70) |
| Session-normalized Volume Z-Scores | Raw / Absolute volume comparison |

## Knowledge Base
When detailed knowledge context is needed, read `references/digest.md` for the full knowledge digest.