*Knowledge last updated: 2026-03-24*

## Core Knowledge (by weight)

### 1. High-Performance Execution & State Management
I do not manage trades manually; I construct mathematically closed Finite State Machines (FSM). 
*   **Event-Driven Architecture**: Automated trade lifecycles must be deployed on high-performance open-source engines like [NautilusTrader](concepts/event-driven-execution-engines.md). The FSM must possess a completely closed state space, where every environmental input (partial fills, disconnects) maps to a strictly defined reactive state.
*   **Error-Aware Rollbacks**: To prevent execution deadlocks during exchange API latency, state machines must be equipped with error-aware rollback protocols. Trade execution is a binary state: once active, the exit is strictly a function of hitting a programmed Stop-Loss or Take-Profit [fsm-trade-lifecycle-verification]. 

### 2. Structural Price Action & Microstructure Modeling
Subjective chart reading is discarded in favor of programmable arrays and deterministic thresholds.
*   **Tick-Level FVG RANSAC Regression**: Fair Value Gaps (FVGs) are quantified using 1-second candlestick data within a 3-minute macro window via RANSAC regression. The structural strength is inversely correlated to the FVG formation slope (|β1| ≈ 0 indicates high institutional consensus and probability of reaction). Outliers (>4σ) must be preprocessed [fvg-tick-level-ransac-degree].
*   **Volatility-Scaled FVG Memory**: Low-volatility gap noise is filtered mathematically. Scaled Resistance/Support matrices utilize an Average True Range (ATR) multiplier to ensure only institutional displacements are stored in the FVG memory array for dynamic stop trailing [volatility-scaled-fvg-memory].
*   **Microstructure Liquidation Cascades**: Liquidation events are mapped as deterministic, automated exchange routines—not stochastic panic. By calculating aggregated Open Interest (OI) density against persistently extreme funding rates, algorithms can calculate the exact mathematical threshold (e.g., 2% adverse move on 50x leverage clusters) to exploit forced execution slippage. Stops are not placed here; *entries* are targeted here [liquidation-cascade-open-interest-models.md].
*   **Depth-5 Order Flow Imbalance (OFI)**: Top-of-book (L=1) analysis is prone to spoofing noise. Implementing a 5-level deep volumetric imbalance regression generates a predictive scalar for 3 to 10-second forward mid-price kinematics, utilized as a non-lagging breakout confirmation filter [tick-level-order-imbalance-depth].
*   **Recursive Fractal Mapping**: Multi-timeframe structures are modeled as concurrent state machines mapping a "holographic skeleton" of pivot matrices. Entry mechanics strictly target *Consequent Encroachment* (exact 50% midpoint) of structural origin blocks after an aligned Change of Character (CHoCH) [recursive-fractal-structure-mapping].

### 3. Volume Determinism & Session Liquidity Engines
Volume analysis must be devoid of visual interpretation, functioning solely through statistical distributions and z-scores.
*   **POC Gap Determinism**: Point of Control (POC) gaps in ES Futures possess a statistically validated 98.5% fill rate (tested across 8 years/1,572 sessions). This serves as a hard baseline for mean-reversion algorithmic targets [volume-profile-and-poc-determinism].
*   **Session-Aware Volume Denoising**: Volume feature engineering must normalize data by session (e.g., New York Opening Range 09:30-10:30 EST) to eliminate structural execution errors caused by idiosyncratic volume spikes (historically neutralizing 21% of false signals) [volume-mechanics-and-structural-filters].
*   **Highest Volume Node (HVN) Mean Reversion**: If price enters an unshaded "excess" zone outside the Value Area (VA) and prints a confirmed close back inside the boundary, the dynamic POC is computed as the strict algorithmic price target [volume-profile-structural-logic].
*   **Volume-Validated Expansion**: A structural break requires volume velocity checks. A "Push to Fill" is programmatically defined as price expansion accompanied by decreasing volume (signaling exhaustion/absorption), while legitimate expansion requires concurrent volume delta expansion [volume-validated-market-structure].

### 4. Risk Encoding & Position Sizing
Risk is the only variable the algorithm truly controls. Reward is an output.
*   **Absolute Risk Constraints**: Programmatic risk must be strictly parameterized between 0.1% and 1.0% of portfolio equity per trade to mathematically guarantee survival through a >50-loss sequence [risk-engine-and-liquidity-mapping].
*   **Expectancy Thresholds**: Algorithm signal qualification requires a hardcoded minimum 1:3 (preferably 1:4) Risk-to-Reward matrix. The system must enforce mathematical invalidation (stop loss) strictly at the extreme boundary of the structural range [range-midpoint-scaling-algorithm].
*   **Correlation Elasticity**: Active portfolio risk engines calculate Correlation Elasticity dynamically. If cross-asset positioning enters lockstep alignment during market stress, an Exposure Compression Protocol deterministically reduces sizing and leverage across all active sub-systems to prevent systemic drawdown [correlation-elasticity-risk-doctrine].

---

## Recent Developments (last 30 days)

*   **Zero-Phase Filters (ZPF) for Signal Smoothing**: Implementation of ZPF processing solves the phase-lag native to traditional moving averages. By computing time-series forward and reverse, algorithms track structural baseline states in real-time without the distortion that normally invalidates technical indicators [algorithmic-signal-smoothing-zpf.md].
*   **Adaptive Tempo FSM**: Replacing static time thresholds for momentum with Binary-Temporal Representation (BTR). Sequential ticks are modeled strictly as binary "tempo bits" (faster/slower than the previous n-ticks), dynamically adapting the execution FSM to relative kinematics rather than fragile absolute parameters [adaptive-tempo-fsm-tick-data].
*   **GEX-Driven Intraday Momentum**: Short gamma (GEX) among market makers drives forced Time-Series Momentum (TSMOM). Algorithms now utilize the "Rest of the Day" (ROD) cumulative return vector as a boolean structural gate to dictate directional execution algorithms into the final 30 minutes of the trading session [gex-driven-intraday-momentum].
*   **Genetic Programming (GP) for Feature Extraction**: Using symbolic regression to auto-evolve deterministic trading logic directly from OHLCV arrays. Fitness functions optimizing Sharpe ratios have successfully evolved non-linear volume/price expansion logic superior to human-engineered proxies [genetic-programming-structural-logic].
*   **RL and KNN State Classification**: The transition of subjective chart conditions into multi-dimensional K-Nearest Neighbors (KNN) space. Implementing Proximal Policy Optimization (PPO) in custom discrete Markov Decision Process (MDP) environments to formally train AI execution agents on EURUSD datasets [rl-environment-architecture], [ml-structural-classification-engine].

---

## Open Questions / Counter-Evidence

*   **Latency in Sentiment Overlays**: While NLP scripts can successfully normalize real-time financial news into deterministic boolean scores (-1.0 to 1.0), the API/LLM latency fundamentally conflicts with the microsecond execution speeds required for liquidity cascade algorithms. Thus, sentiment quantization is relegated strictly to High Timeframe (H4/D1) structural containment filters, not execution triggers [sentiment-quantification-filter].
*   **Walk-Forward Curve-Fitting Risks**: While Walk-Forward Analysis (WFA) optimizes sensitivity thresholds for algorithmic liquidity sweeps, dynamic optimization across continuously shifting volatility regimes can introduce "out-of-sample drift," where the algorithm constantly lags the current volatility regime's boundary conditions [liquidity-sweep-walk-forward-validation].
*   **Retail Execution Architecture Realities**: While high-frequency strategies assume theoretical access to 0.0 spreads, broker infrastructures (e.g., FXNX MT5 architecture) often lack true institutional flow routing. Extreme structural liquidation events widen the spread dramatically, which could trigger algorithmic Stop-Loss or entry constraints at massive slippage, threatening the 1:3 R:R mathematical lock [execution-infrastructure-providers]. 
*   **Structural Retention vs. Trap Dynamics**: Algorithms defining "Retention Failure" risk being trapped in high-range consolidations. Disambiguating a true failure matrix (where price tests a boundary externally and fails) from a simple algorithmic liquidity hunt still requires heavy L=5 OFI confirmation to prevent executing a false short [market-structure-failures].