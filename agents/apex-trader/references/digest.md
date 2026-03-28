*Knowledge last updated: 2026-03-28*

## Core Knowledge (by weight)

As a quantitative algorithm architect, my mandate is the absolute eradication of ambiguity. Subjective chart reading is a failure mode. Market structure, liquidity, and order flow must be distilled into deterministic, computable arrays, finite state machines (FSM), and rigid invalidation thresholds.

### I. High-Frequency Microstructure & Event-Driven Execution (Weight: 1.0)
The foundation of any quantitative system is its data pipeline and execution architecture. Without tick-level precision and latency-aware execution, theoretical alpha decays to zero.
*   **HFT Simulation & Accounting:** [HftBacktest](concepts/hftbacktest-microstructure-simulation.md) provides the core microstructure simulation framework. It utilizes Numba JIT and Rust to model Level-2/Level-3 order book reconstruction, deterministic queue position probabilities, and Guéant–Lehalle–Fernandez-Tapia (GLFT) market-making alphas. 
*   **Tick-Level Feature Engineering:** [finmlkit](concepts/numba-hft-microstructure-bars.md) replaces non-deterministic Pandas operations with explicit Numba-compiled machine code. It generates information-driven bars and intra-bar flow imbalance arrays directly from raw tick sequences, utilizing the Triple Barrier Method for programmatic label generation and risk encoding.
*   **Event-Driven Trade Lifecycles:** [NautilusTrader](concepts/event-driven-execution-engines.md) acts as the production-grade FSM. Every trade lifecycle must be constructed as a "closed" state space. Environmental inputs (partial fills, disconnects) must map to specific [error-aware rollbacks](concepts/trade-lifecycle-validation.md) to prevent deadlock.
*   **Temporal Data Alignment:** Utilizing [QuestDB's](concepts/infrastructure-data-pipeline.md) ASOF JOINs and multi-dimensional arrays guarantees deterministic alignment of asynchronous data streams (e.g., executing tick vs. L2 snapshot) without look-ahead leakage.

### II. Structural Formalization & FVG Mechanics (Weight: 1.0 - 0.96)
Discretionary Smart Money Concepts (SMC) are computationally meaningless without mathematical thresholds.
*   **Tick-Level RANSAC Regression:** The [FVG Degree](concepts/fvg-tick-level-ransac-degree.md) is quantified via linear regression ($|\beta_1|$) over tick data during the precise formation window. The **Inverse FVG Hypothesis** mathematically validates that low-degree FVGs (flatter slopes, $\le 0.00015$ units/sec) are high-probability structural support boundaries, whereas extreme high-degree gaps are algorithmic exhaustion/manipulation.
*   **Volatility-Scaled FVG Memory Arrays:** FVG structural arrays must be dynamic. Utilizing [ATR-scaled FVG tracking](concepts/volatility-scaled-fvg-memory.md), gaps formed in low-volatility regimes are filtered as algorithmic noise. Sustained arrays form continuous Support/Resistance bounds that govern FSM regime shifting.
*   **FSM Gated Breakouts:** Structural containment requires merging [FVG 3-candle imbalance arrays](concepts/market-structure-containment.md) with an N-period dynamic rolling min/max breakout matrix. Execution occurs *only* when the breakout vector and FVG generation precisely synchronize. 
*   **Recursive Fractal Mapping:** Multi-timeframe execution is an inherently concurrent system. Major arrays dictate global FSM state; minor arrays act as triggers. Entries target [Consequent Encroachment](concepts/recursive-fractal-structure-mapping.md)—the exact 50% midpoint of the validated institutional node.

### III. Order Flow, Volume Profile & Liquidity Mapping (Weight: 0.98 - 0.95)
Price is a lagging derivative of order flow imbalance.
*   **POC Gap Determinism & Session Mechanics:** Empirical validation across 1,572 ES Futures sessions establishes a [98.5% fill rate for POC gaps](concepts/algorithmic-volume-profile-validation.md), acting as a deterministic mean-reversion magnet. [Volume-validated expansion](concepts/volume-validated-market-structure.md) enforces that structural shifts must be accompanied by session-relative volume z-scores, successfully filtering ~21% of false breakouts. 
*   **POC Migration Divergence & Unfinished Auctions:** Breakouts are programmatically invalidated if the temporal POC vector descends while the price vector ascends ("hollow breakout"). [Unfinished Auctions](concepts/algorithmic-volume-profile-validation.md) are strictly defined mathematically as structural extremes with exactly 0 contracts traded on the respective bid/ask arrays.
*   **Multi-Level OFI (MLOFI):** Moving beyond top-of-book, [Stationarized Log-OFI](concepts/tick-level-order-imbalance-depth.md) utilizes the Lee-Ready algorithm to compute an $N$-depth dynamic vector of liquidity withdrawal and aggressive displacement, triggering microstructural execution prior to the actual price break.
*   **Programmatic OI Divergence:** [60-Second Liquidation Cascades](concepts/programmatic-oi-divergence-engine.md) are mathematical inevitabilities triggered by Auto-Deleveraging (ADL). Identifying divergence between OI destruction heatmaps and spot stability yields the precise mathematical exhaustion points for algorithmic sweeping targets.

### IV. Quantitative Regime Filtering & Risk Encoding (Weight: 1.0 - 0.95)
Regime filters gate execution logic. An algorithm executing mean-reversion in a trending volatility regime is fundamentally broken.
*   **GEX States & VoV Circuit Breakers:** Positive [Gamma Exposure (GEX)](concepts/gex-driven-intraday-momentum.md) activates "STICKY" FSM logic (range equilibrium retests). Negative GEX triggers "SLIPPERY" (breakout) logic. A **VoV Z-Score > +1.5σ** acts as a systemic fail-safe, programmatically halting all operations in unpredictable volatility surfaces.
*   **Signal Aggregation Consensus:** The [Profi Terminal architecture](concepts/signal-fusion-and-aggregation-logic.md) provides a template for signal fusion, combining multiple independent adapters while enforcing a 0.45x Correlation Suppression penalty for confluent logic families to avoid over-weighting bias.
*   **Deterministic Risk Architecture:** Algorithms must internally encode risk thresholds between [0.1% and 1.0% equity per execution](concepts/risk-engine-and-liquidity-mapping.md), enforcing a strict $1:3$ to $1:4$ fixed R:R baseline. Manual intervention during execution inherently destroys the statistical expectancy calculated in the out-of-sample data.
*   **Zero-Phase Filtering (ZPF):** Moving averages and conventional indicators introduce phase delay, misaligning signal triggers. [ZPF mechanisms](concepts/algorithmic-signal-smoothing-zpf.md) processing time-series bidirectionally eliminate phase lag, aligning deep network (DLSTM) state predictions perfectly with raw tick flows.

---

## Recent Developments (last 30 days)

*   **Agentic Algorithm Discovery:** The transition to LLM-driven algorithmic design is accelerating. Pipelines like the [Claudini autoresearch framework](concepts/agentic-algorithm-discovery.md) are systematically evolving complex, adversarial trading algorithms that outperform human baselines by up to 40%. White-box red-teaming allows AI to map FSM failure modes prior to Walk-Forward Analysis (WFA).
*   **Evolutionary Logic Generation:** [Genetic Programming (GP) via Symbolic Regression](concepts/genetic-programming-structural-logic.md) is now extracting novel order-book relationships directly from data matrices. Instead of human-designed triggers, GP evolves completely transparent expression trees optimizing exclusively for risk-adjusted parameters (Sharpe, MaxDD).
*   **DeFi AMM Invariant State Machines:** Extension of traditional order book algorithms into [DeFi AMM structures via DeFiPy](concepts/event-driven-execution-engines.md), utilizing Q64.96 machine precision to model Uniswap V3 ticks as an analog to limit order flow, enabling automated 'Liquidity Exit' agents.
*   **LLM Signal Architectures:** Rapid translation of structural multi-timeframe concepts into deployable, [60+ feature ES dashboards](concepts/es-volume-profile-optimization.md) via Claude/Cursor architectures demonstrates the operational capacity to reduce build times for highly dense execution systems from months to days.

---

## Open Questions / Counter-Evidence

*   **Phase Lag Tolerances vs. Real-Time Requirement:** While Zero-Phase Filters (ZPF) effectively smooth data with zero phase distortion, their inherent requirement to process time-series data *backwards* introduces look-ahead dependencies making real-time, tick-by-tick microsecond execution mathematically problematic without strict temporal windowing protocols.
*   **Discretionary SMC Transition to Code:** While Breaker Blocks and FVGs have been successfully translated into rule-based models (`np.where` arrays, rolling min/max matrices), the nuance of multi-timeframe "context" remains computationally expensive. Relying purely on structural cascades occasionally results in false-positive "zones of failure" when macro volume spikes contravene tick-level slope degradation.
*   **Indicator Stationarity:** Is the transformation of lagging indicators (RSI, MACD) into multi-dimensional vectors via [KNN classification models](concepts/ml-structural-classification-engine.md) statistically robust out-of-sample, or merely advanced curve-fitting? My mandate explicitly prioritizes flow imbalance (OFI) over derivative indicators unless standard scaling and strict Walk-Forward Analysis enforce regime-agnostic edge.