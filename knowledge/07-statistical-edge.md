# 📐 07 — Statistical Edge & Risk Management Math

> **Source:** Distilled from Deep Dive Part 8 ([source-docs/deep-dive-full.md](./source-docs/deep-dive-full.md))
>
> **Use case:** This is the math that proves your system can work over time. When emotion screams "this isn't working," math whispers "wait 50 trades."

---

## 🎯 The Core Insight

> **A statistical edge is positive expected value over a sample size large enough to overcome variance.**
>
> You don't have an edge after 1 trade. You don't have an edge after 10 trades. You start to see edge data after 50-100 trades. You confirm edge after 200+ trades.
>
> Anything you "feel" before 50 trades is noise + bias.

---

## 1. The Expectancy Formula

```
Expectancy = (Win Rate × Avg Win) − (Loss Rate × Avg Loss)
```

### Example (Your Target System)

- Win Rate: 50%
- Avg Win: 2R
- Loss Rate: 50%
- Avg Loss: 1R
- Expectancy = (0.50 × 2) − (0.50 × 1) = **1.0 − 0.5 = +0.5R per trade**

### What That Means

At 0.5% risk per trade, +0.5R expectancy = +0.25% per trade on average.
Over 25 trades/month: ~6.25% account growth/month.
On $3,000: ~$187/month.

**This is the math that says your system works — IF you maintain rule compliance.**

---

## 2. Win Rate vs R:R Tradeoffs

The math of profitability allows MULTIPLE valid systems:

| Win Rate | Required R:R for Breakeven | Required R:R for Profitability |
|---|---|---|
| 30% | 1 : 2.33 | 1 : 3.0+ |
| 40% | 1 : 1.50 | 1 : 2.0+ |
| 50% | 1 : 1.00 | 1 : 1.5+ |
| 60% | 1 : 0.66 | 1 : 1.0+ |
| 70% | 1 : 0.43 | 1 : 0.7+ |

### Implications

- **High WR + low R:R** = "scalper" mindset (60-70% WR, 1:1 R:R)
- **Low WR + high R:R** = "trend follower" mindset (30% WR, 1:3 R:R)
- **Your system targets ~50% WR + 1:2 R:R** = balanced, sustainable

### Common Failure Mode

Traders chase 70% WR with poor R:R (1:0.5 or worse). Math says they're losing money. Brain says "I win more than I lose." **Brain is wrong.**

---

## 3. Profit Factor Benchmarks

### Definition

```
Profit Factor = Gross Profit / Gross Loss
```

If you made $1,000 in winners and lost $750 in losers: PF = 1.33.

### Benchmarks For Retail Traders

| PF | Quality |
|---|---|
| < 1.0 | Losing system — abandon or refine |
| 1.0 - 1.2 | Marginal — mostly luck, edge unclear |
| 1.2 - 1.5 | Decent — small but real edge |
| 1.5 - 2.0 | Strong — solid retail trader territory |
| 2.0 - 3.0 | Excellent — top retail performance |
| > 3.0 | Suspicious — likely curve-fit or small sample |

### Your Target

**PF > 1.5 over 50+ trades** = you have a real edge.
This is the threshold for considering Phase 4 (funded challenge).

---

## 4. Sample Size & Confidence Intervals

### The Mathematical Reality

To distinguish edge from noise with 95% confidence:
- 30 trades: VERY uncertain (huge confidence interval)
- 50 trades: SOMEWHAT uncertain (still wide interval)
- 100 trades: REASONABLY confident
- 200 trades: HIGH confidence
- 500+ trades: VERY HIGH confidence

### What This Means

**Don't make system changes based on:**
- Last 5 trades (pure noise)
- Last 10 trades (still noise)
- Last 20 trades (early signal)
- **WAIT until 50+ trades minimum** before any system refinement

### Your Phase 1 Backtest Target

50 backtested + 30 live = 80 trades. Still on the edge of statistical significance, but enough to see trends.

For Phase 3 refinement: target 100+ live trades.

---

## 5. Risk Of Ruin

### Definition

The mathematical probability of depleting your account entirely given current risk parameters.

### Your Setup

- Risk per trade: 0.5%
- Win rate: ~50% (target)
- R:R: 1:2 (target)
- Account: $3,000

**Risk of ruin: ~0%** (mathematically near-zero with positive expectancy + 0.5% sizing)

### But Wait — Sequence-Of-Returns Risk

Even with positive expectancy, you can hit losing streaks:
- 5 losses in a row = 2.5% drawdown (statistically common)
- 10 losses in a row = 5% drawdown (rare but happens)
- 15 losses in a row = 7.5% drawdown (very rare)

### Probability Of Streaks

At 50% win rate (independent trades):
- 5 in a row: ~3.1% (every 30 trades on average)
- 10 in a row: ~0.1% (every 1,000 trades on average)
- 15 in a row: ~0.003% (essentially never)

**Your psychological problem isn't the streak — it's how you respond to it.** A 5-loss streak triggers all 9 of your patterns. The math is fine; the psychology isn't.

---

## 6. Kelly Criterion (And Why You Use Fractional Kelly)

### Full Kelly Formula

```
Kelly % = (Win Rate × Avg Win - Loss Rate × Avg Loss) / Avg Win
```

### Example (Your System)

- Win Rate: 50%
- Avg Win: 2R
- Avg Loss: 1R
- Full Kelly = (0.5 × 2 - 0.5 × 1) / 2 = 0.5 / 2 = **25%**

### Why You DON'T Use Full Kelly

Full Kelly = mathematically optimal compounding. But:
- Assumes infinite trades and stable parameters
- 25% risk per trade = catastrophic drawdowns (-50% drawdown is normal)
- Psychologically intolerable
- One regime change destroys you

### Fractional Kelly (Industry Standard)

- Quarter Kelly: 25% / 4 = 6.25% per trade (still aggressive)
- Tenth Kelly: 25% / 10 = 2.5% per trade (institutional)
- **Your 0.5% risk = ~1/50th Kelly** (extremely conservative)

### Why Your 0.5% Is Right

For your situation:
- Mental health recovery → reduced cognitive resilience to drawdowns
- Building habits → don't want emotional volatility
- Small account → preserving capital matters more than fast growth
- **0.5% is correct for Year 1. Don't increase it.**

---

## 7. Drawdown Management Protocol

### Phase 1 / Phase 2 (Where You Are)

| Account Drawdown | Action |
|---|---|
| 0% to -2% | Normal trading |
| -2% to -3% | Reflect, no rule changes |
| -3% to -5% | Reduce risk to 0.25%, review last 10 trades for pattern |
| -5% to -7% | Stop trading 3 days. Full system review. |
| > -7% | Stop trading 1 week. Mentor session. Possible system refinement. |

### Why It Matters

Recovery math is asymmetric:
- -10% drawdown requires +11% gain to recover
- -25% drawdown requires +33% gain to recover
- -50% drawdown requires +100% gain to recover

**Preserving capital is mathematically more important than chasing returns.**

---

## 8. Expected Drawdowns At Your Risk

At 0.5% per trade with positive expectancy, expect:

| Frequency | Expected Drawdown |
|---|---|
| Every 1-2 weeks | -1% to -2% |
| Every 1-2 months | -2% to -3% |
| Every 6-12 months | -3% to -5% |
| Once every 1-2 years | -5% to -7% |
| Once in a decade | -7% to -10% |

**Anything beyond -5% in a month is a signal to check for: regime change, system breakdown, or trader behavior issue.**

---

## 9. The Math That Saves You

### When Emotion Says "I Need To Trade More"

- Your system: 50% WR, 1:2 R:R = +0.5R per trade
- 25 trades/month = 12.5R = 6.25% account growth
- 50 trades/month = 25R BUT (with overtrading, win rate drops to 40%)
- 50 trades at 40% WR, 1:2 R:R = +0.2R per trade = 10R = 5% account growth
- **More trades, less money.**

### When Emotion Says "I Should Increase Risk"

- 0.5% risk × 50% WR × 1:2 = +0.25% per trade
- 1.0% risk × 50% WR × 1:2 = +0.5% per trade BUT
- Drawdown doubles, psychological pain doubles, behavioral compliance drops to 30%
- 1.0% risk × 30% WR × 1:2 (with broken behavior) = -0.4% per trade
- **More risk, less compliance, less money.**

### When Emotion Says "This System Doesn't Work"

After 20 trades with mediocre results:
- Statistical confidence: ~25%
- The chance you're seeing real underperformance: ~50%
- The chance it's just variance: ~50%
- **You can't tell after 20 trades. Math says wait.**

---

## 10. The Daily/Weekly/Monthly Math Mindset

### Daily P&L Should Be Ignored

A single day:
- Sample size: 1-2 trades
- Statistical meaning: zero
- Emotional weight: high
- **Daily P&L is noise. Track it for journaling, ignore for decisions.**

### Weekly P&L Is The Minimum Useful Window

A week:
- Sample size: 5-10 trades
- Statistical meaning: minimal but starting
- **Weekly review is the smallest valid review window**

### Monthly P&L Tells A Story

A month:
- Sample size: 20-30 trades
- Statistical meaning: moderate
- Trends emerging
- **Monthly reviews drive system refinements, not weekly**

### Quarterly P&L Is Truth

A quarter:
- Sample size: 60-100 trades
- Statistical meaning: high
- Edge confirmed or denied
- **Quarterly is when you decide phases (Phase 1 → 2 → 3 → 4)**

---

## 📋 Statistical Health Checklist

After every 50 trades, check:

- [ ] Win rate: ___% (target: 40%+)
- [ ] Avg win: ___R (target: 2R)
- [ ] Avg loss: ___R (target: 1R)
- [ ] Profit factor: ___ (target: > 1.5)
- [ ] Expectancy: ___R per trade (target: > +0.3R)
- [ ] Max drawdown: ___% (target: < 5%)
- [ ] Rules compliance %: ___% (target: > 80%)
- [ ] Average R:R achieved: ___ (target: matches plan)

If 4+ are below target → review BEFORE making any system changes. Most likely it's a behavioral issue, not a system issue.

---

## 📚 Sources

- Standard expectancy formulas (universal across literature)
- Kelly Criterion (Edward Thorp adaptations)
- Risk of Ruin tables (Ralph Vince, *Mathematics of Money Management*)
- Sample size theory (statistical inference fundamentals)

Full citations in [`source-docs/deep-dive-full.md`](./source-docs/deep-dive-full.md).

---

> **The math doesn't lie. Your system has positive expectancy. The question is never "does it work?" — it's "can YOU follow it long enough for the math to play out?"**
