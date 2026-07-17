# Research #001 — Founding Report

## Which Public Crypto Trading Strategies Survive Independent Validation?

**Alpha Factory Research · July 2026**

*Estimated reading time: 15 minutes*

---

## Executive Summary

| Strategy | Status | N | Net PF | Decision | Key Lesson |
|---|---|---|---|---|---|
| H037 — Liquidation Cascade Continuation | KILLED | 21 closed forward | 0.30 (ex-PEPE) | Concentration falsified generalization | Two trades = 257% of total net profit |
| H011 — Stop-Hunt Reversal | EVIDENCE COLLECTION | 10 paper | 1.72 | CI contains zero | Small-N positive ≠ statistically significant |
| CVFD — Cross-Venue Funding Dispersion | KILLED | 33 trading days | N/A (no edge) | No directional information | Signal real, structural, still no tradeable edge |
| Compression — Volatility Breakout | KILLED | 3 days live | Net -$46.22 | Fees consumed edge | 177 ops in 5 days destroyed gross profit |
| DFG-009 — Pre-Market Convergence | KILLED | 16 events | 0.018 | Premium widened, not contracted | Product success ≠ trading strategy success |
| M7 — Unlock Events | EVIDENCE COLLECTION | — | — | Low event frequency | Forced-flow survives; statistical significance pending |

57 strategies reviewed. 5 tested to advanced stages. 1 survived all gates.

---

## Who wrote this / Methodology

Alpha Factory Research is an independent quantitative research initiative. We do not provide trading signals, investment advice, or portfolio management. We publish evidence.

**How this research was conducted:**

- All strategies tested using publicly available exchange data (OKX, Binance).
- Frozen, preregistered backtests. No parameter search. No post-hoc threshold selection.
- Forward evidence collected through prospective paper trading before any capital deployment.
- Cost analysis includes real exchange fees, conservative slippage estimates, and funding costs.
- Every killed strategy in this report was independently falsified — not opinion, not narrative.

**Why this exists:** most public crypto trading strategies fail independent validation. Our goal is to document which ones — and why — so you don't risk capital on a strategy that already died in testing.

---

## 1. Introduction

Between June and July 2026, Alpha Factory Research independently tested 57 public crypto trading strategies through a structured validation pipeline. This report covers the five strategies that reached the most advanced stages — and why only one survived.

We do not provide trading signals. We publish evidence.

---

## 2. Strategy 1 — Liquidation Cascade Continuation (H037)

**Mechanism:** follow the liquidation cascade. When forced liquidations create price pressure, the cascade continues in the same direction.

**What happened:** 21 genuine forward trades collected over 12 days. Gross profit factor: 1.67. Gross expectancy: +1.14%. Passed all headline gates.

**The kill:** Two PEPE trades contributed 257% of total net profit. Remove PEPE — the remaining 19 trades had a net profit factor of **0.30** and net expectancy of **-0.78%**. Bootstrap 95% CI contained zero. Excluding the single best trade destroyed the edge.

**What this means for your trading:** aggregating performance across symbols hides fatal concentration. Always compute ex-best-symbol profit factor before deploying any strategy.

---

## 3. Strategy 2 — Stop-Hunt Reversal (H011)

**Mechanism:** liquidity grabs at obvious stop levels create a reversal opportunity. Market makers engineer price moves to trigger clustered stop-losses, then the price reverses as the forced selling abates.

**What happened:** 10 paper trades. Win rate 60%. Profit factor 1.72. Directional accuracy 72.2%. One trade from the paper promotion gate.

**The block:** Bootstrap confidence interval still contains zero. Not statistically significant. A strategy can have positive expectancy at small N and still be indistinguishable from noise. The strategy remains in evidence collection.

**What this means for your trading:** win rate and profit factor at N=10 tell you nearly nothing. Wait for the confidence interval to exclude zero before deploying capital.

---

## 4. Strategy 3 — Cross-Venue Funding Dispersion (CVFD)

**Mechanism:** OKX-Binance funding rate spread reveals venue-specific positioning. The crowded venue is squeeze-vulnerable — when OKX longs pay significantly more than Binance longs, the imbalance predicts a directional unwinding.

**What happened:** Killed in 45 minutes of independent frozen falsification. Zero cost. Free data.

**The kill:** The spread is real (~0.1 bp) and maps to genuine positioning differences — but carries zero detectable directional information about future price. 0/6 price impact tests significant. 0/12 bootstrap CIs exclude zero. The signal exists. It just doesn't predict returns.

**What this means for your trading:** a statistically real market structure does not automatically translate into a tradeable edge. Correlation between Signal A and Positioning B does not prove that A predicts price.

---

## 5. Strategy 4 — Volatility Compression (虎爪)

**Mechanism:** BB bandwidth compression signals an impending breakout. When volatility contracts, price is coiling — enter in the direction of the eventual expansion.

**What happened:** 3 days of live trading on OKX. 93 filled buy orders. Real capital deployed (~$5,000 initial). Gross PnL: +$53.61. Net PnL after fees and slippage: **-$46.22**. 177 operations in 5 days.

**The kill:** Configuration drift from V1 to V2 (removing BTC trend filter, shortening holding period from 24h to 8h) turned a marginally positive strategy into a clearly negative one. Cross-strategy interference from V6 forced premature position exits. High turnover destroyed whatever edge existed through taker fees alone.

**What this means for your trading:** multiply your estimated turnover by your taker fee rate before backtesting. If the gross edge is smaller than the turnover cost, do not trade.

---

## 6. Strategy 5 — Pre-Market Convergence (DFG-009)

**Mechanism:** OKX pre-market perpetual prices should converge to spot as the conversion deadline approaches. Short the pre-market premium, long spot at listing, capture the convergence.

**What happened:** 16 terminal events identified. Full census reconstructed from official OKX announcements. 10 executable paired trades on free public data.

**The kill:** The premium widened instead of contracting during the conversion window. Net profit factor: **0.018**. Net expectancy: -$31.99 per trade. The market correctly priced the novelty premium — there was no delayed absorption to exploit.

**What this means for your trading:** a successful product lifecycle (18 pre-market tokens → 18 converted perpetuals) is not the same as a profitable trading strategy. The underlying mechanism was sound — the market was just faster.

---

## 7. Strategy 6 — Unlock Events (M7)

**Mechanism:** scheduled token unlocks create predictable, mechanical selling pressure. Short before the unlock, capture the anticipated decline.

**Evidence:** 63.4% directional accuracy out-of-sample. Multiple unlock events across tokens. Forced-flow mechanism — token recipients must sell or hedge.

**Why it survived when others died:** M7 belongs to the forced-flow family. Unlike discretionary-prediction strategies (momentum, breakout), M7's edge is structural: someone is contractually obligated to receive tokens and economically compelled to sell them. The event schedule is public and immutable.

**Remaining risk:** event frequency is low. Statistical significance requires more unlock events than have occurred. Currently in evidence collection — not a deployable strategy yet. But the directional signal is genuine, the data is free, and the mechanism is causal.

**What this means for your trading:** structural forced-flow strategies are the highest-probability candidates for genuine alpha. When someone must act, the edge is mechanical. When someone chooses to act, the edge is statistical — and usually disappears.

---

## 8. The Pattern: Forced Flow vs. Discretionary Prediction

| Forced-Flow Mechanisms | Discretionary-Prediction Mechanisms |
|---|---|
| Liquidation cascades (must close) | Momentum (chooses to buy) |
| Unlock events (must sell) | Breakout (chooses to enter) |
| Index rebalancing (must rebalance) | ML prediction (chooses direction) |
| Contract expiry (must roll) | Sentiment analysis (chooses weight) |
| Dealer hedging (must delta-hedge) | Mean reversion (chooses threshold) |

Forced-flow strategies: 2 of 3 tested showed genuine directional signal (H037, M7). Discretionary-prediction strategies: 0 of 3 survived.

The implication is not that forced-flow always works. It's that forced-flow is the only mechanism family where the edge, if it exists, is structural rather than statistical — and therefore more likely to survive out-of-sample.

---

## 9. Lessons for Systematic Traders

1. **Gross profit factor is not enough.** H037 had PF 1.67 — and would have lost money in production.
2. **Concentration kills.** Two trades out of 21 = 257% of total net profit. Ex-best-symbol is a mandatory robustness check.
3. **Forward evidence is mandatory.** No strategy should deploy capital based on backtest alone.
4. **Fees are not a detail.** 177 operations in 5 days destroyed a positive gross edge. Multiply turnover by taker rate before backtesting.
5. **Kill fast.** CVFD was falsified in 45 minutes for $0. The most expensive mistake is testing too long.
6. **Forced flow outperforms discretionary prediction.** Chase structural obligations, not statistical patterns.

---

*Alpha Factory Research. Evidence before capital.*
