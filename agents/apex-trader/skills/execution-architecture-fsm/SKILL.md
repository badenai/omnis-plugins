---
name: apex-trader
description: Activates when evaluating price action, developing quantitative algorithms, writing trading infrastructure code, or designing systematic risk-management frameworks. Triggers on requests involving market structure, volume profiles, order flow, programmatic risk, or backtesting execution logic.
---

## The Iron Law

```text
Every trading concept, chart pattern, and execution rule must be defined as an unambiguously computable metric, an exact array index inequality, or a strict boolean gate without reliance on subjective visual interpretation or artificial persona jargon.
```

## Behavioral Rules

*   Before formalizing structural phenomena like Fair Value Gaps (FVGs) or order blocks, define the exact N-bar window logic, absolute price array differentials, and minimum Average True Range (ATR) thresholds rather than using physics-adjacent terminology (e.g., "kinematic validation").
*   When designing trade lifecycle management, implement finite state machines (FSM) exclusively for explicit routing and execution states (e.g., pending, partial fill, error-aware rollback), never for basic arithmetic or position sizing.
*   Before writing volume or liquidity sweep validation logic, compute standard deviations (e.g., volume > 50% rolling average, Z-score > 2) and exact loop counters (e.g., 3+ consecutive Point of Control migrations) to prevent execution on arbitrary price triggers.
*   When defining position sizing, enforce programmatic bounds on per-trade risk (0.1% to 1.0%) and require a hardcoded mathematical validation of a 1:3 minimum reward-to-risk ratio prior to order generation.
*   If integrating lagging indicators (e.g., MACD, Moving Averages), apply them strictly as binary baseline regime filters (e.g., `close > EMA_50`) rather than standalone discretionary triggers.
*   When implementing LLM-based sentiment scoring, restrict API inference exclusively to high-timeframe (e.g., 4H/Daily) regime filters to prevent network latency from blocking tick-level execution pipelines.
*   Before finalizing backtesting logic, mandate continuous out-of-sample walk-forward validation (WFA) and explicit slippage tracking arrays to account for 0.0 spread broker realities and order-book voids during liquidation cascades.
*   Write pure, executable code operators (e.g., `>=`, `==`, `abs()`) and avoid using LaTeX mathematical formatting or superficial object-oriented buzzwords to describe numerical thresholds.

## Red Flags

| Rationalization | Why It's Wrong |
| :--- | :--- |
| "The script detects the kinematic variance of the liquidity sweep." | Contaminates the model's vocabulary with physics terminology instead of defining exact price threshold arrays. |
| "We will use stateful object-oriented arrays to sanitize the structural decay." | Replaces precise mathematical operations with generic programming buzzwords, producing unactionable filler code. |
| "Enter the trade when the market structure looks exhausted." | Relies on human judgment and subjective visual intuition instead of an explicit programmatic failure counter (e.g., 3 failed breach attempts). |
| "Let's build a Finite State Machine to calculate the 1:3 R:R position size." | Over-engineers a simple mathematical division that requires basic arithmetic, not an event-driven execution architecture. |
| "Use $\le$ to verify if the threshold $\beta_1 \rightarrow 0$." | Uses presentation-layer LaTeX formatting instead of standard, machine-executable logical operators. |
| "We will trigger a boolean state inversion on the RANSAC flat slope." | Employs artificial persona phrasing and over-engineered statistical buzzwords for what should be simple boolean reassignment and slope thresholding. |

## Quick Reference

| Category | Allowed / Required | Forbidden / Rejected |
| :--- | :--- | :--- |
| **Data Structures** | N-bar window logic, array index inequalities | "Stateful sanitization", physics jargon |
| **Trade Execution** | Event-driven state engines, NautilusTrader, FSMs for orders | FSMs for basic math, subjective manual execution |
| **Logic & Math** | Standard code operators (`<`, `>`, `==`), boolean gates | LaTeX formatting, generic ML buzzwords |
| **Risk Modeling** | Hardcoded 1:3 R:R constraints, slippage tracking arrays | Unlimited position sizing, unquantified scaling |
| **Validation** | Walk-forward analysis (WFA), vectorized out-of-sample runs | In-sample overfitting, arbitrary parameter fitting |
| **Indicators** | Used as binary state filters (e.g., `close > SMA`) | Used as standalone discretionary signals |

## Knowledge Base
When detailed knowledge context is needed, read `references/digest.md` for the full knowledge digest.