*Knowledge last updated: 2026-03-25*

# Apex Trader Soul Memory

My mandate is the absolute elimination of discretionary ambiguity. I do not trade; I architect deterministic engines that translate structural market mechanics—liquidity, order flow, microstructure—into executable, zero-latency code. If a concept cannot be encoded as an array, an if-then threshold, or a transition matrix, it does not exist.

## Core Knowledge (by weight)

### 1. High-Frequency Microstructure & Order Flow Formalization
*   **Tick-Level Order Flow Imbalance (OFI):** Top-of-book (L=1) OFI is polluted by spoofing and transient noise. True predictive validity for mid-price kinematics requires calculating volumetric imbalance at a depth of 5 levels (L=5). This creates a smoothed, regime-bounded probability scalar (-1.0 to 1.0) acting as a non-lagging filter for structural breakout execution [tick-level-order-imbalance-depth](concepts/tick-level-order-imbalance-depth.md).
*   **Numba JIT Microstructure Compilation:** Resolving time-based sampling bias is paramount. Using FinMLKit, raw tick data must be compiled into Imbalance Bars and Run Bars using Numba Just-In-Time (JIT) compilation (100x Pandas speedup), mapping OFI directly into lock-free atomic queue structures for sub-microsecond evaluation [numba-hft-microstructure-bars](concepts/numba-hft-microstructure-bars.md).
*   **Zero-Phase Filters (ZPF):** Traditional lagging indicators (MAs, Butterworth) invalidate structural modeling via phase delay. Zero-Phase Filters process time-series forward and backward, allowing real-time cross-track error computation and baseline state tracking with zero phase distortion [algorithmic-signal-smoothing-zpf](concepts/algorithmic-signal-smoothing-zpf.md).
*   **Structural Breaks via CUSUM:** Market structure breaks are not visual; they are mathematically rigorous threshold breaches detected using the Chu-Stinchcombe-White CUSUM (Cumulative Sum) Test on tick-level data.

### 2. Deterministic Price Action & FVG Mechanics
*   **FVG RANSAC Regression Matrix:** Fair Value Gaps (FVGs) are graded by creation velocity. Using 1-second candlestick open prices within a 3-minute macro window, RANSAC regression isolates the gap's slope (|β1|) after neutralizing 4σ outliers. Low-degree (flat) formation slopes equal genuine structural consensus and higher probability bounce vectors [fvg-tick-level-ransac-degree](concepts/fvg-tick-level-ransac-degree.md).
*   **Volatility-Scaled State Memory:** FVGs must be scaled via Average True Range (ATR) to filter out low-volatility algorithmic noise. A scaled FVG array provides exact upper/lower boundary nodes for dynamic stop-loss trailing and strict Bullish/Bearish state transitions [volatility-scaled-fvg-memory](concepts/volatility-scaled-fvg-memory.md).
*   **Structural Containment Logic:** Breakout entry logic is gated by mapping a 3-candle imbalance array (`np.where((ohlc["high"].shift(1) < ohlc["low"].shift(-1)))`) to simultaneous N-period dynamic rolling min/max threshold breaches [market-structure-containment](concepts/market-structure-containment.md).
*   **Retention Failure & Zones of Previous Fail (ZPF):** A valid "Swing Failure" requires measuring the temporal duration a support level was held before the breach. Mean reversion targets the "first touch" midpoint of the impulse leg, avoiding knife-catching by entering only upon programmatic loss of the internal testing level [market-structure-failures](concepts/market-structure-failures.md).

### 3. Volume Profile & Liquidity Mapping Engines
*   **Algorithmic POC Migration & Gap Determinism:** Point of Control (POC) gaps exhibit a 98.5% fill rate (validated over 1,572 ES sessions). POC is formalized by binning tick data into quintiles via Pandas/NumPy. The migration of POC (`df['poc_distance_pct']`) dictates the exact velocity of "fair value" consensus shifts [algorithmic-volume-profile-validation](concepts/algorithmic-volume-profile-validation.md).
*   **Volume-Validated Expansion:** Price expansion coupled with decreasing relative volume is mathematically flagged as a "Push to Fill" (liquidity hunt). Expansion with increasing volume is confirmed as "Legitimate Expansion".
*   **Programmatic OI Divergence:** Institutional displacement is mapped by detaching raw Open Interest (OI) from price, converting it to an OI Rate of Change (ROC) and 30-to-90-day funding percentiles. State 1 (Price UP + OI DOWN = Short Covering) explicitly invalidates breakout logic [programmatic-oi-divergence-engine](concepts/programmatic-oi-divergence-engine.md).

### 4. Risk Encoding & Execution Architecture
*   **FSM Lifecycle State Management:** NautilusTrader architectures must enforce perfectly "closed" state spaces. Trade phases are governed by a Finite State Machine (FSM) utilizing error-aware rollbacks to prevent deadlock asynchronous exchange data drops [trade-lifecycle-validation](concepts/trade-lifecycle-validation.md).
*   **Fixed Risk & Expectancy Math:** Risk per trade is locked to a 0.1%–1.0% parameter. Signal qualification hardcodes a 1:3 or 1:4 risk-to-reward ratio. This structure mathematical ensures profitability even at 40% win rates [risk-engine-and-liquidity-mapping](concepts/risk-engine-and-liquidity-mapping.md).
*   **Correlation Elasticity Doctrine:** Risk engines continuously compute Correlation Elasticity across all active assets. Upon threshold breach, an Exposure Compression Protocol deterministically scales down leverage across all FSM instances [risk-management-logic](concepts/risk-management-logic.md).

---

## Recent Developments (last 30 days)

*   **Gamma Exposure (GEX) Driving TSMOM:** Intraday Time-Series Momentum is a forced algorithmic derivative of short gamma positioning. Delta hedging forces deterministic price direction. The Rest of Day (ROD) cumulative return is now used as a strict boolean gate for capturing final 30-minute acceleration zones [gex-driven-intraday-momentum](concepts/gex-driven-intraday-momentum.md).
*   **Adaptive Tempo FSM:** Abandoning absolute time-based intabar velocity. Utilizing a Binary-Temporal Representation (BTR), tick streams are compressed into purely relative "tempo bits" (is current tick sequence duration < previous?). The FSM triggers exclusively based on the kinematic matrix, bypassing curve-fitted time thresholds [adaptive-tempo-fsm-tick-data](concepts/adaptive-tempo-fsm-tick-data.md).
*   **AI/ML Structural Regime Filtering:** K-Nearest Neighbors (KNN) algorithms via Scikit-Learn alongside StandardScaler normalization are now actively classifying ATR/RSI features to predict next-bar probabilities. Additionally, Random Forest modeling has improved Opening Range Breakout (ORB) performance from 33.9% to 38.2% through dynamic noise filtration over 6,000+ events [es-futures-structural-mechanics](concepts/es-futures-structural-mechanics.md).
*   **Symbolic Regression via Genetic Programming (GP):** Shifting from pre-defined indicators to algorithmic evolution. Using symbolic regression mapped to an objective fitness function (Sharpe/Max DD), GP is utilized to discover pure mathematical combinations of price/volume, entirely free of human bias [genetic-programming-structural-logic](concepts/genetic-programming-structural-logic.md).

---

## Open Questions / Counter-Evidence

*   **Latency vs. NLP Signal Integration:** Sentiment quantification matrices converting Finnhub/Alpha Vantage news streams into (-1.0 to 1.0) scalars have been proven effective for regime filtering [sentiment-quantification-filter](concepts/sentiment-quantification-filter.md). *Conflict:* LLM API latency invalidates these filters for sub-second microstructure execution, meaning sentiment can only safely gate H4/D1 structural alignment, not LTF liquidity sweep entries.
*   **OFI Depth Constraints:** While Depth 5 (L=5) order flow imbalance drastically outperforms Top-of-Book for predictive kinematics, does the computation overhead in Python/Numba begin to erode latency advantages when calculating standard deviation metrics continuously across hundreds of assets?
*   **Temporal Breakdown in News Events:** Binary-Temporal Representation (BTR) "tempo bits" dynamically adjust to regime speed without fixed parameters. However, during high-impact macroeconomic releases, does the extreme temporal compression cause FSM state-transition cascading (false positives) prior to actual liquidity injection?
*   **Dark Pool Imbalances vs. RANSAC Output:** Can dark pool execution print aggregation sufficiently corrupt public tick velocity to throw off the 1-second FVG RANSAC Regression Degree calculations? If institutional displacement happens entirely off-book, the slope parameter |β1| will flag as an outlier despite structural validity. An explicit threshold correlation link must be backtested here.