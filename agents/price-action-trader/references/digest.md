*Knowledge last updated: 2026-07-15*

# Price Action Expert Soul: Comprehensive Memory Document

This document serves as the core repository of knowledge, mechanical trading principles, and advanced execution parameters for the **Price Action Expert Soul**. Grounded strictly in pure price data, volume, and market structure, this manual rejects lagging retail indicators in favor of algorithmic price delivery, institutional order flow, and rigorous risk management.

---

## Core Knowledge (by weight)

### 1. Market Structure and Structural Hierarchy
The foundation of price action trading is the objective categorization of trend continuations versus structural reversals. Distinguishing these states requires strict, non-discretionary rules to prevent trading in middle-range noise [ict-market-structure-and-liquidity](concepts/ict-market-structure-and-liquidity.md).
*   **Break of Structure (BOS):** Signifies trend continuation in the direction of the dominant higher-timeframe order flow. A valid BOS **requires a candle body close** past the previous swing high or swing low. Wicks filtering through a level do not constitute a BOS; they are classified strictly as liquidity sweeps [ict-market-structure-and-liquidity](concepts/ict-market-structure-and-liquidity.md).
*   **Change of Character (CHoCH) & Market Structure Shift (MSS):** Represent trend reversals. 
    *   *CHoCH* marks the first signal of a potential trend change, often occurring on the internal, lower-timeframe structure [ict-market-structure-and-liquidity](concepts/ict-market-structure-and-liquidity.md).
    *   *MSS* requires energetic, high-volume displacement to confirm systemic damage to prior order flow on the execution timeframe [ict-smc-price-action-concepts](recent/2026-07/ict-smc-price-action-concepts.md).
*   **Premium vs. Discount Arrays (PD Arrays):** Every trading range defined by a validated swing high and swing low must be split into three zones using Fibonacci frameworks [ict-market-structure-and-liquidity](concepts/ict-market-structure-and-liquidity.md):
    1.  **Premium Zone (Top 50%):** Area of expensive pricing; shorts are executed strictly within Premium PD arrays.
    2.  **Equilibrium (50% Midpoint):** Neutral zone; no new positions should be opened here.
    3.  **Discount Zone (Bottom 50%):** Area of wholesale pricing; longs are executed strictly within Discount PD arrays.

### 2. Algorithmic Liquidity Delivery and Pools
Markets are not random; they are driven by algorithms designed to deliver price from one liquidity pool to another, seeking to rebalance inefficiencies and clear resting stop-loss clusters [ict-killzones-and-fvgs](concepts/ict-killzones-and-fvgs.md).
*   **External Liquidity:** Resides outside the current trading range at highly obvious swing points, specifically previous daily highs (PDH), previous daily lows (PDL), highs of day (HOD), and lows of day (LOD) [market_liquidity_concepts](concepts/concepts/market_liquidity_concepts.md).
*   **Internal Liquidity / Inducement (IDM):** Resides inside the current trading range at minor swing points and short-term pullbacks. The algorithm engineered these levels as "inducements" to trap early retail breakout traders and generate stop-loss fuel before continuing the primary higher-timeframe trend [market_liquidity_concepts](concepts/concepts/market_liquidity_concepts.md), [structure-inducement-vs-choch](concepts/structure-inducement-vs-choch.md). Internal liquidity is typically swept first before the market seeks major external pools [market_liquidity_concepts](concepts/concepts/market_liquidity_concepts.md).
*   **High vs. Low Resistance Liquidity:**
    *   *Low Resistance Liquidity* forms after a failure swing (a failure to make a new structural high or low), presenting weaker defense and acting as easy draw-on-liquidity targets [high-low-resistance-liquidity](concepts/concepts/high-low-resistance-liquidity.md).
    *   *High Resistance Liquidity* forms after a clean structural break and immediate sharp reversal. Sweeping high-resistance liquidity provides the high-volume fuel needed to accelerate price rapidly toward low-resistance pools [high-low-resistance-liquidity](concepts/concepts/high-low-resistance-liquidity.md).
*   **Equal Highs (EQH) & Equal Lows (EQL):** Double or triple tops/bottoms form highly dense clusters of retail stop-losses, creating primary structural targets for institutional sweeps [liquidity-sweeps-and-pools](concepts/concepts/liquidity-sweeps-and-pools.md).

### 3. Institutional Footprints: Order Blocks, Imbalances, and Inversions
Institutional participants leave clear footprints of their execution, which can be programmatically verified or visually graded [algorithmic-price-action-smc](concepts/algorithmic-price-action-smc.md).
*   **Order Blocks (OB):** The last candle of opposite color prior to a decisive, high-volume market expansion or breakout [fvg-and-order-block-confluence](concepts/fvg-and-order-block-confluence.md).
*   **Breaker Blocks (BB) vs. Mitigation Blocks (MB):**
    *   *Breaker Blocks* are failed order blocks formed *after* price successfully sweeps a major liquidity pool (stop hunt of an extreme) and completes an MSS [high-probability-order-blocks.md](concepts/concepts/high-probability-order-blocks.md).
    *   *Mitigation Blocks* are failed order blocks formed by a failure swing, meaning the reversal occurs without sweeping the previous extreme. MBs represent trend exhaustion and require higher timeframe points of interest (POI) for validation [high-probability-order-blocks.md](concepts/concepts/high-probability-order-blocks.md).
*   **Hidden Order Blocks (HOB):** Zones formed by overlapping wicks of consecutive same-color candles on higher timeframes. Drilling down to lower timeframes reveals them as fully formed, unmitigated traditional order blocks [high-probability-order-blocks](concepts/concepts/concepts/high-probability-order-blocks.md).
*   **Fair Value Gaps (FVG):** A three-candle price imbalance where the wicks of the first and third candles do not overlap, leaving an untraded zone [ict-killzones-and-fvgs](concepts/ict-killzones-and-fvgs.md).
    *   **Consequent Encroachment (CE):** The exact 50% midpoint of an FVG or wick shadow, acting as a crucial support/resistance validation level [ict-smc-price-action-concepts](recent/2026-07/ict-smc-price-action-concepts.md).
    *   **Inverse Fair Value Gap (IFVG):** When price closes decisively beyond the boundary of a standard FVG, the zone flips structural polarity (expected support becomes resistance, and vice versa) [smc-fvg-ob-mechanics](concepts/concepts/recent/2026-07/smc-fvg-ob-mechanics.md).
    *   **Balanced Price Range (BPR):** Formed when a bullish FVG and a bearish FVG directly overlap horizontally, representing complete algorithmic equilibrium. Retests of BPR boundaries offer ultra-precise, low-drawdown entries [balanced-price-range-bpr](concepts/balanced-price-range-bpr.md).

### 4. Precise Time & Price Alignment
Algorithmic price delivery relies on precise scheduling. High-probability setups form exclusively when key structural levels align with intraday time windows [ict-institutional-liquidity-and-timing](concepts/concepts/ict-institutional-liquidity-and-timing.md).
*   **The Power of Three (AMD):** Models daily candle generation:
    1.  **Accumulation:** Typically occurs during the low-volume Asian session, building a horizontal range [ict-smc-framework](concepts/concepts/ict-smc-framework.md).
    2.  **Manipulation (Judas Swing):** Characterized by a false run during session opens (e.g., London Open) designed to sweep the Asian range extremes, hunt retail stops, and engineer institutional liquidity [ict-institutional-liquidity-and-timing](concepts/concepts/ict-institutional-liquidity-and-timing.md), [ict-smc-framework](concepts/concepts/ict-smc-framework.md).
    3.  **Distribution:** The real daily expansion leg, which usually manifests during the New York AM session [ict-smc-framework](concepts/concepts/ict-smc-framework.md).
*   **Session Killzones (EST):**
    *   *London Open:* 2:00 AM – 5:00 AM EST [ict-killzones-and-fvgs](concepts/ict-killzones-and-fvgs.md).
    *   *New York Open:* 8:30 AM – 11:00 AM EST [ict-killzones-and-fvgs](concepts/ict-killzones-and-fvgs.md).
    *   *New York PM Session:* 1:30 PM – 4:00 PM EST [ict-killzones-and-fvgs](concepts/ict-killzones-and-fvgs.md).
*   **Silver Bullet Windows (EST):** One-hour high-probability macro windows:
    *   *London:* 3:00 AM – 4:00 AM EST [ict-killzones-and-fvgs](concepts/concepts/ict-killzones-and-fvgs.md).
    *   *New York AM:* 10:00 AM – 11:00 AM EST (the single highest-probability macro hour) [ict-killzones-and-fvgs](concepts/concepts/ict-killzones-and-fvgs.md).
    *   *New York PM:* 2:00 PM – 3:00 PM EST [ict-killzones-and-fvgs](concepts/concepts/ict-killzones-and-fvgs.md).
*   **Optimal Trade Entry (OTE) Settings:** Location tool mapped via Fibonacci retracements of the most recent impulsive leg:
    *   **0.618 (61.8%) and 0.79 (79%)** define the OTE boundaries [advanced-pd-arrays](concepts/concepts/concepts/concepts/advanced-pd-arrays.md).
    *   **0.705 (70.5%)** acts as the algorithmic "sweet spot" midpoint [advanced-pd-arrays](concepts/concepts/concepts/concepts/advanced-pd-arrays.md).
    *   *Symmetrical Take-Profit Targets:* Placed at the **-0.27** and **-0.62** Fibonacci extensions [advanced-pd-arrays](concepts/concepts/concepts/concepts/advanced-pd-arrays.md).

---

## Recent Developments (last 30 days)

### 1. Advanced Structural Entry Models
*   **ICT Unicorn Model:** Fuses structural polarity flips with algorithmic inefficiencies. It is defined strictly as the **horizontal overlap of an ICT Breaker Block and an FVG** [unicorn-model-entry.md](concepts/concepts/unicorn-model-entry.md). Verification requires a session-based liquidity sweep, a clear MSS with energetic displacement, and the FVG forming directly within the vertical boundaries of the Breaker [unicorn-model-entry](concepts/concepts/concepts/unicorn-model-entry.md).
*   **ICT Suspension Block:** A specialized continuation candlestick whose body is completely overlapped by the wick of the prior candle, preventing a standard FVG from forming [advanced-pd-arrays](concepts/concepts/concepts/advanced-pd-arrays.md). When sandwiched between two volume imbalances, the body of this candle acts as a highly reliable support or resistance zone where the algorithm reloads order delivery [advanced-pd-arrays](concepts/concepts/concepts/advanced-pd-arrays.md).
*   **Institutional Order Flow Entry Drill (IOFED):** For high-momentum conditions where deep retracements do not materialize. Limit entries are placed directly at the proximal edge of an FVG rather than waiting for the 50% consequent encroachment [advanced-pd-arrays.md](concepts/concepts/advanced-pd-arrays.md).

### 2. Microstructure Validation: Footprint and Delta Divergences
To bypass the lag of standard candlesticks, professional execution increasingly integrates order flow diagnostics with price action [liquidity-sweep-mss-strategy](concepts/concepts/liquidity-sweep-mss-strategy.md):
*   **Absorption Verification:** Confirmed when massive aggressive market orders (visible on bid-ask footprint diagonals) fail to advance price, signaling that institutional limit orders (passive icebergs) are soaking up the flow [order-flow-absorption-dom.md](concepts/concepts/order-flow-absorption-dom.md).
*   **Cumulative Delta Divergence:** A warning signature where price continues to print higher highs while cumulative delta shows decreasing buying aggression, proving aggressive buyers are stepping down and passive limit sellers are absorbing remaining market orders [price-volume-delta-divergence](concepts/concepts/price-volume-delta-divergence.md).

### 3. Modernized Intermarket Confluence (SMT)
*   **Symmetric Market Transition (SMT) Divergence:** Bearish SMT occurs when one correlated asset (e.g., NQ) sweeps a key liquidity pool (HOD/PDH) while the other (e.g., ES) fails to do so [smt-divergence-trading-mechanics](concepts/concepts/concepts/smc-ict-methodology-framework.md). This divergence reveals institutional manipulation, confirming a high-probability reversal setup [smt-divergence-trading-mechanics](concepts/concepts/concepts/smc-ict-methodology-framework.md).

### 4. Dynamic Risk Management Protocols
*   **Volumetric Position Sizing:** Transitioning away from fixed percentage-based sizing to contract-based sizing scaled inversely with structural stop distance and ATR, ensuring absolute dollar risk remains constant across high and low volatility regimes [risk-management-and-position-sizing](concepts/concepts/risk-management-and-position-sizing.md).
*   **Multi-Stage Trailing Rules:** Rigid capital protection checklist:
    *   *At 1R:* Reduce risk by 50% (move stop-loss to 50% of original distance) [price-action-mechanics](recent/2026-07/recent/price-action-mechanics.md).
    *   *At 2R:* Move stop-loss to break-even (BE) [price-action-mechanics](recent/2026-07/recent/price-action-mechanics.md).
    *   *At 3R:* Secure full profit [price-action-case-studies](recent/2026-07/recent/price-action-case-studies.md).
*   **Process-Oriented Circuit Breakers (The Three-Mistake Rule):** Professional traders must shut down execution platforms immediately upon committing three operational errors (e.g., trading outside session killzones, adjusting a resting stop, or over-leveraging), protecting capital before a physical drawdown triggers a daily loss limit [trading-psychology-risk.md](concepts/concepts/trading-psychology-risk.md).

---

## Open Questions / Counter-Evidence

### 1. FVG and OB Statistical Hold Rates
*   **The 5,400-Gap Study:** Quantitative testing indicates that approximately **30% to 40% of printed FVGs remain completely unfilled**, making blind limit order entries at every gap mathematically unprofitable [smc-fvg-ob-mechanics](concepts/concepts/recent/2026-07/smc-fvg-ob-mechanics.md).
*   Furthermore, statistics reveal that **up to 84% of lower-timeframe (M15 and below) FVGs that get filled immediately reverse and break structure** unless they are nested directly within a higher-timeframe (H4 or Daily) Order Block or premium/discount array [smc-fvg-ob-mechanics](concepts/concepts/recent/2026-07/smc-fvg-ob-mechanics.md).

### 2. Systematic Backtest Drift vs. Live Execution
*   There remains a persistent execution gap between theoretical backtested win-rates of automated SMC indicators (such as commercial toolkits claiming up to 75.3% win rates on XAU/USD) and live trading performance [smart-money-concepts-indicators](recent/2026-07/recent/smart-money-concepts-indicators.md). 
*   This performance drift is driven by **lookahead bias, dirty off-exchange historical data, unmodeled transactional costs (spread friction and slippage), and historical parameter overfitting** [smc-fvg-ob-mechanics](recent/2026-07/smc-fvg-ob-mechanics.md). Discretionary top-down multi-timeframe mapping of macro draw-on-liquidity (DOL) remains superior to fully automated pattern detection [ict-market-structure-and-timing-mechanics](concepts/concepts/ict-market-structure-and-timing-mechanics.md).

### 3. The "Floating Risk Rule" in Prop Firm Environments
*   Modern proprietary trading firms are increasingly replacing standard static daily loss limits with a **"Floating Risk Rule"** [prop-firm-mechanics-and-risk.md](concepts/concepts/prop-firm-mechanics-and-risk.md). 
*   Under this rule, risk allowance is dynamically adjusted by automated risk engines based on real-time market volatility and live account equity [prop-firm-mechanics-and-risk.md](concepts/concepts/prop-firm-mechanics-and-risk.md). This introduces friction for traders executing pure structural setups, as sudden volatility spikes can automatically compress position-sizing allowances and daily loss caps mid-trade, forcing stop-outs independent of the physical invalidation levels on the chart [prop-firm-mechanics-and-risk.md](concepts/concepts/prop-firm-mechanics-and-risk.md).