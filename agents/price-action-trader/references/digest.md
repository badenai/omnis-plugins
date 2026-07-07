*Knowledge last updated: 2026-07-07*

# Price Action Expert Soul: Memory Document

## Core Knowledge

### 1. Foundational Market Structure & Dynamics
Market structure is the bedrock of professional price action analysis, rejecting lagging mathematical indicators in favor of pure price delivery, order flow, and structural transitions [market-structure-and-fvg-resources](concepts/market-structure-and-fvg-resources.md).
*   **Trend Anatomy:** Trends are defined strictly by the progression of Higher Highs (HH) and Higher Lows (HL) for bullish regimes, and Lower Highs (LH) and Lower Lows (LL) for bearish regimes [market-structure-and-fvg-resources](concepts/market-structure-and-fvg-resources.md).
*   **Structural Transitions:**
    *   **Break of Structure (BOS):** Signals trend continuation [ict-market-structure-and-timing-mechanics](concepts/ict-market-structure-and-timing-mechanics.md).
    *   **Change of Character (CHOCH) / Market Structure Shift (MSS):** Signals a trend reversal when price decisively shifts past a major external swing level [ict-and-smc-core-concepts](concepts/ict-and-smc-core-concepts.md).
    *   **Inducement (IDM):** A minor, internal structural break engineered by algorithmic pricing to trap early retail breakout traders. A true CHOCH requires displacement and a candle body close past a major external swing level; a minor break or a simple wick through a level is classified as inducement or a liquidity sweep, not a structural break [structure-and-inducement-vs-choch](concepts/structure-inducement-vs-choch.md).

### 2. Institutional Order Blocks (OB) & Imbalances
Large institutional footprint zones on a chart function as key supply and demand areas rather than traditional retail support/resistance.
*   **Order Blocks:** The last candle before an aggressive, decisive expansion move, representing institutional order footprints that can be traded on subsequent retests [recent/2026-07/smc-fvg-and-backtesting-standards](recent/2026-07/smc-fvg-and-backtesting-standards.md).
*   **Structural Distinction of Failed Order Blocks:**
    *   **Breaker Blocks (BB):** A failed order block formed after price sweeps liquidity (stop hunt of a previous extreme) and completes a Market Structure Shift (MSS). Breakers contain aggressive institutional resting liquidity from the swept stops, offering high-velocity, structurally robust transitions [concepts/concepts/high-probability-order-blocks](concepts/concepts/high-probability-order-blocks.md).
    *   **Mitigation Blocks (MB):** A failed order block formed by a failure swing (exhaustion) where price fails to reach or sweep the previous extreme before reversing through the previous order block. Mitigation blocks represent trend fatigue and require tighter risk management and higher timeframe point of interest (POI) confluence [concepts/concepts/high-probability-order-blocks](concepts/concepts/high-probability-order-blocks.md).
*   **Hidden Order Blocks (HOB):** Zones formed by overlapping wicks of same-color consecutive candles on daily or weekly charts. While invisible as a standard candle body on higher timeframes, lower timeframe (LTF) drilldowns reveal them as fully formed, unmitigated order blocks that offer high-precision entries untouched by standard retail scanners [concepts/concepts/concepts/high-probability-order-blocks](concepts/concepts/concepts/high-probability-order-blocks.md).
*   **Fair Value Gaps (FVG) & Imbalances:** Three-candle price imbalances where the wicks of the first and third candles do not overlap, leaving an untraded zone that institutional algorithms target to rebalance [concepts/concepts/ict-killzones-and-fvgs](concepts/concepts/concepts/ict-killzones-and-fvgs.md).
    *   **BISI & SIBI:** Buyside Imbalance Sellside Inefficiency (BISI) and Sellside Imbalance Buyside Inefficiency (SIBI) outline the specific buy/sell delivery gaps [concepts/ict-smc-framework](concepts/ict-smc-framework.md).
    *   **Consequent Encroachment (CE):** The precise 50% midpoint of a Fair Value Gap, serving as a highly reactive, low-risk execution level [concepts/concepts/ict-smc-framework](concepts/concepts/ict-smc-framework.md).
    *   **Inverse Fair Value Gaps (IFVG):** Calculated when a standard FVG fails to hold and experiences a decisive candle body close straight through its boundaries. The zone is reclassified as an IFVG, flipping its structural polarity (support becomes resistance and vice versa) due to offside institutional order mitigation [concepts/concepts/recent/2026-07/smc-fvg-ob-mechanics](concepts/concepts/concepts/recent/2026-07/smc-fvg-ob-mechanics.md).
*   **Balanced Price Range (BPR):** Established when a bullish FVG and a bearish FVG overlap horizontally, representing complete algorithmic equilibrium in a specific price band. Unlike single-candle imbalances or standard IFVGs, the BPR serves as an immediate, highly reactive magnet where price has traded aggressively in both directions, making its boundaries exceptionally robust invalidation zones [concepts/balanced-price-range-bpr](concepts/balanced-price-range-bpr.md).
*   **Institutional Order Flow Entry Drill (IOFED):** An aggressive execution technique where a limit order is placed precisely at the proximal edge of an FVG rather than waiting for the standard 50% equilibrium (CE) fill. Used in high-momentum conditions where deep retracements do not materialize, optimizing the risk-to-reward ratio on fast-moving expansion legs [concepts/iofed-precision-entry](concepts/iofed-precision-entry.md).
*   **Suspension Blocks:** A specialized candlestick residing "suspended" between an upper and lower volume imbalance, where the body of the suspension block is completely overlapped by the wick of the prior candle, preventing a standard FVG from forming. Despite having no wick-to-wick gap, the combination of the candle body and its twin volume imbalances acts as a highly reliable support/resistance zone [concepts/concepts/concepts/advanced-pd-arrays](concepts/concepts/concepts/advanced-pd-arrays.md).

### 3. Liquidity Pools & Liquidity Grab Execution
Price moves in a highly structured sequence from one liquidity pool to another, driven by central bank algorithms designed to target resting retail orders [concepts/concepts/ict-killzones-and-fvgs](concepts/concepts/concepts/ict-killzones-and-fvgs.md).
*   **Liquidity Targets:**
    *   **Buy-side Liquidity (BSL):** Located above previous highs, equal highs, and session extremes [concepts/ict-smc-framework](concepts/ict-smc-framework.md).
    *   **Sell-side Liquidity (SSL):** Located below previous lows, equal lows, and session extremes [concepts/ict-smc-framework](concepts/ict-smc-framework.md).
*   **Stop-Loss Clusters:** Dense pools of retail resting stop orders which act as primary targets for institutional stop hunts and liquidity sweeps before a real market move begins [recent/2026-07/concepts/concepts/ict-institutional-price-action-concepts](recent/2026-07/concepts/concepts/ict-institutional-price-action-concepts.md).
*   **Multi-Timeframe Entry Matrix:** High-probability trade execution relies on a structured 2-Timeframe hierarchy:
    1.  Define a clear "Draw on Liquidity" on the Higher Timeframe (HTF) (e.g., 4-Hour chart) [concepts/concepts/concepts/liquidity-sweep-mss-strategy](concepts/concepts/concepts/liquidity-sweep-mss-strategy.md).
    2.  Wait for that HTF target pool to be cleanly swept [concepts/concepts/concepts/liquidity-sweep-mss-strategy](concepts/concepts/concepts/liquidity-sweep-mss-strategy.md).
    3.  Zoom into the designated Lower Timeframe (LTF) (exactly two intervals lower, such as the 15-Minute chart) [concepts/concepts/concepts/liquidity-sweep-mss-strategy](concepts/concepts/concepts/liquidity-sweep-mss-strategy.md).
    4.  Locate a clean, impulsive "liquidity grab" displacement candle and place an execution limit order at the newly formed FVG or Order Block [concepts/concepts/concepts/liquidity-sweep-mss-strategy](concepts/concepts/concepts/liquidity-sweep-mss-strategy.md).

### 4. Advanced Mechanical Entry Models
*   **The ICT Unicorn Model:** A mechanical, rule-based reversal framework defined as the direct horizontal overlap of an ICT Breaker Block and an ICT Fair Value Gap (FVG). An A+ setup requires a session-based liquidity sweep, a clear displacement leg causing a Market Structure Shift (MSS), and execution timed strictly inside institutional session killzones. Invalidation is immediate if a candle body closes beyond the outer anchor point (the swing extreme of the initial liquidity sweep) [concepts/concepts/concepts/unicorn-model-entry](concepts/concepts/concepts/concepts/unicorn-model-entry.md).
*   **The Venom Model:** A highly mechanical entry model that utilizes a Balanced Price Range (BPR)—where a bullish and bearish FVG overlap horizontally—forming immediately after a major liquidity sweep during a predetermined session Killzone. Entry orders are placed precisely at the boundary of the BPR, targeting HTF external liquidity [concepts/unicorn-model-entry](concepts/unicorn-model-entry.md).
*   **Optimal Trade Entry (OTE):** A mathematical location tool designed to map discount and premium pricing within a validated dealing range. The OTE boundaries are the 0.618 (61.8%) and 0.79 (79%) retracements of the most recent impulsive structural leg, with 0.705 (70.5%) acting as the sweet-spot midpoint. High-probability execution requires that the OTE zone directly overlaps with a pre-existing HTF PD Array (such as an unmitigated Order Block or FVG) after a clear liquidity sweep. Symmetrical profit targets are projected at the -0.27 and -0.62 extensions [concepts/concepts/advanced-pd-arrays](concepts/concepts/concepts/advanced-pd-arrays.md).

### 5. Timing, Session Mechanics, and the Power of Three (AMD)
Price action cannot be analyzed in a vacuum; high-probability setups require alignment between key price levels (Premium/Discount arrays) and specific session times.
*   **ICT Kill Zones (ET):** High-probability time windows characterized by peak institutional volume and algorithmic order delivery.
    *   **London Open:** 2:00 AM – 5:00 AM ET [concepts/concepts/ict-killzones-and-fvgs](concepts/concepts/concepts/ict-killzones-and-fvgs.md)
    *   **New York Open / Silver Bullet:** 8:30 AM – 11:00 AM ET [concepts/concepts/ict-killzones-and-fvgs](concepts/concepts/concepts/ict-killzones-and-fvgs.md)
    *   **New York PM Session:** 1:30 PM – 4:00 PM ET [concepts/concepts/ict-killzones-and-fvgs](concepts/concepts/concepts/ict-killzones-and-fvgs.md)
*   **The Power of Three (AMD):** The standard daily algorithmic blueprint modeling price delivery [concepts/ict-smc-framework](concepts/ict-smc-framework.md):
    *   **Accumulation:** Occurs during the low-volume Asian session, building a consolidation range of resting orders [concepts/amd-power-of-3](concepts/amd-power-of-3.md).
    *   **Manipulation:** Occurs during the London session, engineering a false breakout (the "Judas Swing") to sweep Asian range extremes and trap retail participants [concepts/amd-power-of-3](concepts/amd-power-of-3.md).
    *   **Distribution:** Occurs during the New York session, reversing off the London manipulation to deliver the true directional trend expansion towards the opposing unmitigated liquidity pool [concepts/amd-power-of-3](concepts/amd-power-of-3.md).
*   **AMDX / Quarterly Theory:** An evolution of the AMD model that divides market cycles into rigid quarterly phases, adding a fourth phase "**X**" representing either continuation or reversal. This fourth phase dictates how the daily or weekly cycle concludes after the distribution phase, preventing late-session entries into exhausted trends [concepts/concepts/amd-power-of-3](concepts/concepts/amd-power-of-3.md).

### 6. Volume Profile & Footprint Market Microstructure
Integrating footprint charts, Depth of Market (DOM), and Volume Profile dynamics removes execution lag associated with traditional candlestick charting [concepts/concepts/liquidity-sweep-mss-strategy](concepts/concepts/liquidity-sweep-mss-strategy.md).
*   **Volume Profile Structure:**
    *   **High Volume Nodes (HVN):** Areas of high historic transaction density representing price acceptance, value, and consolidation [concepts/order-flow-absorption-dom](concepts/order-flow-absorption-dom.md).
    *   **Low Volume Nodes (LVN):** High-speed vacuum voids where price historical volume is scarce, causing price to accelerate rapidly through order imbalances [concepts/order-flow-absorption-dom](concepts/order-flow-absorption-dom.md).
*   **DOM Dynamics ("Pull and Stack"):** Observing the order book ladder reveals institutional intent. The rapid cancellation of resting size ("pulling" orders) signals a lack of defense, whereas the swift reloading of passive limit orders ("stacking" or icebergs) reveals active support or resistance [concepts/order-flow-absorption-dom](concepts/order-flow-absorption-dom.md).
*   **Footprint & Volumetric Absorption:** Confirms liquidity sweeps in real time. A true institutional sweep is confirmed by "absorption"—where a massive diagonal delta spike (aggressive market orders exceeding a 3x imbalance ratio) is completely met by passive limit orders, causing the candle to stall and instantly reverse rather than expand. This is validated when a candle closes bullish despite a highly negative net Delta, proving aggressive sellers were absorbed by a massive passive buy wall [concepts/concepts/order-flow-absorption-dom](concepts/concepts/order-flow-absorption-dom.md).

### 7. Professional Mechanics & Risk Protocols
*   **The Three-Mistake Rule:** A process-oriented psychological circuit breaker. Instead of relying purely on maximum daily dollar losses (which often trigger only after cognitive breakdown and revenge trading have occurred), this rule forces an immediate platform shutdown upon committing three pre-defined operational errors (such as trading outside of Kill Zones, altering a resting stop-loss, or violating strict position-sizing rules) [concepts/concepts/trading-psychology-risk.md](concepts/concepts/trading-psychology-risk.md).
*   **Floating Risk Rule:** An algorithmic risk engine increasingly adopted by modern proprietary trading firms. This system dynamically compresses leverage limits, position-sizing allowances, and daily loss caps based on real-time market volatility and trader equity drawdown, forcing traders to shift from fixed percentage-based sizing to highly adaptive, contract-based exposure [concepts/concepts/prop-firm-mechanics-and-risk](concepts/concepts/prop-firm-mechanics-and-risk.md).

---

## Recent Developments (Last 30 Days)

### 1. Programmatic Smart Money Concepts & Automation
*   **SMC/ICT Python Package:** The release and development of open-source algorithmic libraries (e.g., `smart-money-concepts` on GitHub) programmatically detects Fair Value Gaps, Order Blocks, and structural shifts directly from raw price data, moving the industry closer to objective, rule-based quantitative backtesting [concepts/concepts/smart-money-concepts-python](concepts/concepts/smart-money-concepts-python.md).
*   **Pine Script v6 Footprint Native Integration:** TradingView’s updated scripting engine native footprint data allows systematic price action traders to code automated entries based on real-time Point of Control (POC) and Value Area retests [concepts/automated-volume-profile-execution](concepts/automated-volume-profile-execution.md).

### 2. Multi-Timeframe S&D Zone Grading Toolkits
*   **Visual Automated Toolkits:** Commercial toolkits (e.g., Flux Charts' Price Action Toolkit and MTF Supply & Demand Zones) have automated structural overlay mapping on TradingView, allowing multi-timeframe key levels and overlapping premium/discount zones to be automatically highlighted without manual visual charting [concepts/concepts/flux-charts-price-action-toolkit](concepts/concepts/flux-charts-price-action-toolkit.md).

### 3. Broker & Prop Firm Capitalization Ecosystem
*   **FeneFx & CTI Scaling Profiles:** Large-scale capitalization models (e.g., City Traders Imperium offering up to $4M scaling and FeneFx’s two-step evaluation models) have integrated with low-latency ECN brokers like MondFx and FXNX. These brokers offer raw interbank spreads (starting from 0.0 pips) and under 30ms execution servers co-located in LD4, NY4, and TY3 data centers to minimize execution slippage during rapid liquidity sweep events [concepts/prop-firm-mechanics-and-risk](concepts/prop-firm-mechanics-and-risk.md).

---

## Open Questions / Counter-Evidence

### 1. Multi-Timeframe Structural Noise vs. Edge Validation
*   While Lower Timeframe (LTF) execution charts (e.g., 1-Minute and 5-Minute) offer highly asymmetric risk-to-reward ratios, they present high-frequency structural noise. Quantitative backtesting of over 5,400 FVGs across five major cryptocurrencies over two years reveals that trading FVGs in isolation without higher-timeframe context and parent Order Block alignment yields a statistically negative expectancy [recent/2026-07/smc-fvg-and-backtesting-standards](recent/2026-07/smc-fvg-and-backtesting-standards.md).

### 2. AI Pattern Recognition vs. Off-Chart Context
*   The rise of multimodal AI vision models grading chart screenshots reveals a major limitation: visual-only models cannot parse critical live, off-chart data such as order books, funding rates, open interest, and macroeconomic calendars. This reinforces that simple pattern identification (e.g., locating a geometric flag or triangle) is insufficient; traders must manually integrate live order flow absorption and structural validity to construct an edge [recent/2026-07/concepts/concepts/recent/2026-07/smc-fvg-ob-mechanics](recent/2026-07/concepts/concepts/recent/2026-07/smc-fvg-ob-mechanics.md).

### 3. Balanced Price Range (BPR) Quality vs. Wick Ratios
*   Performance metrics indicate that not all BPR and FVG entries are equal. Gaps and ranges formed by clean displacement candles with a body-to-wick ratio above 70% yield a 2.1R average to structural targets, whereas those with body-to-wick ratios under 60% see average performance drop significantly to 1.3R, highlighting the critical importance of candle body quality filters [concepts/concepts/balanced-price-range-bpr.md](concepts/concepts/balanced-price-range-bpr.md).