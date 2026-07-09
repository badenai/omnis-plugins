---
name: institutional-order-flow-timing
description: Use when analyzing market setups based on intra-session timing, session-specific liquidity sweeps, and the Power of Three (Accumulation, Manipulation, Distribution) frameworks. This includes mapping London Open, New York Open/Silver Bullet, and PM session killzones.
---

## The Iron Law

```text
TIME FILTER PRECEDES PRICE FILTER: Never analyze or execute a price action setup unless price has entered a designated session Killzone. If a structural break, FVG, or liquidity sweep occurs outside of strict algorithmic time windows, categorize it as low-probability noise and skip the trade.
```

## Behavioral Rules

1. **Map the Asian Range First:** You must define the Asian Session range (8:00 PM – 2:00 AM ET) as the Accumulation phase before looking for London or New York setups.
2. **Execute Only Inside Killzones:** You must restrict active execution and setup hunting to these precise windows:
   - *London Open Killzone:* 2:00 AM – 5:00 AM ET
   - *New York Open / Silver Bullet:* 8:30 AM – 11:00 AM ET
   - *New York PM Session:* 1:30 PM – 4:00 PM ET
3. **Filter and Validate the Judas Swing:** If price breaks the Asian Range high or low during the London Open Killzone, you must treat it as Manipulation (Judas Swing) and search for a sweep reversal setup, rather than trading the breakout.
4. **Identify SMT Divergence at Key Times:** During the first 30 minutes of the London or New York Open, you must compare correlated assets (e.g., ES vs. NQ, EURUSD vs. GBPUSD) to identify SMT divergence at key liquidity sweeps to confirm institutional entry.
5. **Classify Sweeps Outside Killzones as Noise:** If a major liquidity sweep or structural change occurs outside of the designated session Killzones, you must classify it as a low-probability trap and refuse to recommend an entry.
6. **Apply the Power of Three (AMD):** You must structure daily market analysis under the AMD framework: Accumulation (Asia), Manipulation (London), and Distribution (New York). 

## Red Flags

| If you see this mistake... | Why it is wrong... |
| :--- | :--- |
| **Trading breakouts of the Asian Range during London Open.** | This ignores the Judas Swing mechanics; London specializes in engineering fake runs to sweep resting liquidity before reversing. |
| **Executing a Silver Bullet strategy setup at 11:30 AM ET.** | Algorithmic order flow drops significantly after 11:00 AM ET; trading here exposes you to low-volume chop and distribution traps. |
| **Treating a mid-day structural shift (12:30 PM ET) as a high-probability CHOCH.** | Structure shifts during the lunch hour are highly prone to retail manipulation and lack institutional volume support. |
| **Analyzing price setups without checking the session clock.** | Price without time is a retail trap. Institutional algorithms operate on strict temporal schedules. |

## Quick Reference

| Session / Killzone | Time Window (Eastern Time) | Primary Algorithmic Behavior | Tactical Focus |
| :--- | :--- | :--- | :--- |
| **Asian Session** | 8:00 PM – 2:00 AM | Accumulation of orders, low volume range | Define high and low liquidity boundaries |
| **London Open Killzone** | 2:00 AM – 5:00 AM | Manipulation (Judas Swing), runs Asian extremes | Look for sweeps of Asian range to trade reversal |
| **New York Open / Silver Bullet** | 8:30 AM – 11:00 AM | High-volume expansion, Distribution, trend runs | Look for FVG/OB entries and SMT divergence |
| **New York PM Session** | 1:30 PM – 4:00 PM | Late-day distribution or macro/reversal setups | Look for sweeps of NY AM session high/low |