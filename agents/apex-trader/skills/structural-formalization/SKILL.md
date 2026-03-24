---
name: structural-formalization
description: Use when building, reviewing, or defining quantitative trading algorithms, formalizing price action concepts into deterministic code, implementing array-based market structure logic, calculating ATR-scaled gap matrices, or encoding precise entry/exit/stop rules based on absolute price differentials.
filePattern: "**/*.py"
bashPattern: "pytest|unittest"
---

## The Iron Law

```text
You must translate all subjective price action into explicit array indices, absolute price differentials, N-bar window logic, and strict Boolean gates; never output a chart pattern or structural concept without its accompanying computable algorithmic definition, verifiable data input, and hardcoded risk constraint.
```

## Behavioral Rules

*   Define structural arrays using explicit indexing and strict mathematical inequalities (e.g., `close[i] > high[i-1]`) rather than generic object-oriented jargon or physics-adjacent terminology.
*   Filter low-volatility gap noise mathematically by scaling Resistance/Support memory arrays with Average True Range (ATR) multipliers to ensure only true institutional displacements persist in programmatic memory.
*   Quantify structural concepts like Fair Value Gaps (FVGs) using precise 1-second candlestick data arrays within bounded macro windows (e.g., 3 minutes), and systematically drop statistical outliers exceeding 4 standard deviations before saving to dynamic trailing matrices.
*   Target the exact 50% midpoint (Consequent Encroachment) of structural origin blocks using absolute price differentials immediately after validating a Change of Character (CHoCH) across aligned multi-timeframe arrays.
*   Enforce absolute mathematical risk parameters by constraining position sizing strictly between 0.1% and 1.0% of portfolio equity per trade calculation.
*   Encode strict stop-loss and take-profit invalidation logic into every algorithmic entry signal, ensuring a mathematically hardcoded minimum 1:3 Risk-to-Reward ratio aligned with the extreme bounds of the structural range.
*   Construct recursive fractal structures by mapping pivot logic across concurrent time-series arrays rather than relying on abstract, single-timeframe visual indicators.
*   Calculate absolute programmatic limits for both entry and exit variables instead of abstracting logic into complex machine-learning algorithms or superfluous architectural frameworks.

## Red Flags

| Detection | Rationalization | Why Wrong |
| :--- | :--- | :--- |
| "Kinematic validation" or "RANSAC flat slopes" | Attempting to sound sophisticated regarding price movement or regression analysis. | Contaminates execution logic with irrelevant physics-adjacent or ML buzzwords instead of relying on concrete array indices and Boolean gates. |
| LaTeX-style math operators (`$\le$`, `$\rightarrow$`) | Trying to formulate complex mathematical representations of trading rules. | Abstracts away explicit code-level directives like programmatic risk constraints, time-series array management, and basic arithmetic execution. |
| Object-oriented filler like "stateful array sanitization protocol" | Creating an artificial aura of deterministic or architectural rigor. | Replaces exact mathematical operations, variable definitions, and precise algorithmic logic with unactionable programming jargon. |
| Entry triggers lacking a defined stop limit | Assuming risk management is a separate module or manual process. | Violates the core mandate of risk encoding; algorithms without mathematically bound stop-losses placed at structural range extremes are incomplete. |
| Decoupling signal logic from execution mechanisms | Focusing purely on identifying patterns without defining how the machine trades them. | Robust algorithms require explicit instructions dictating both the mathematical structure breakdown and the computable lifecycle limits of the trade. |

## Quick Reference

| Concept | Computable Implementation |
| :--- | :--- |
| **Market Structure Break** | Array index inequality confirming `close[0] > max(high[1...N])` with corresponding volume delta array expansion. |
| **FVG / Gap Memory** | 1-second resolution candlestick bounds stored in matrices with $>4\sigma$ outlier exclusion and ATR-scaled noise filters. |
| **Target Acquisition** | Absolute price differential set exactly to the 50% mathematically calculated midpoint of an aligned structural origin array. |
| **Risk Encoding** | Hardcoded variables limiting equity exposure (0.1% - 1.0%) with strict stop thresholds at array range extremes (min 1:3 R:R). |
| **Fractal Mapping** | Concurrent logic arrays scanning for synchronized pivot conditions across multiple N-bar timeframes without visual indicator lag. |