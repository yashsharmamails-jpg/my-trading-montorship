# 🔬 08 — Backtesting Methodology

> **Source:** Distilled from Deep Dive Part 9 ([source-docs/deep-dive-full.md](./source-docs/deep-dive-full.md))
>
> **Use case:** Phase 1 requires 50 backtests. Done badly, they're worthless. Done right, they save you months of live-account learning.

---

## 🎯 The Core Truth

> **Bad backtesting is worse than no backtesting.**
>
> You convince yourself you have an edge that doesn't exist, blow your account, and have no idea why.

This chapter ensures your Phase 1 backtests are valid.

---

## 1. Cognitive Biases That Destroy Backtests

### Look-Ahead Bias

**The mistake:** Using information that wouldn't have been available at the time of decision.

**Examples:**
- Looking at H4 candle close before M5 entry (you wouldn't know that intraday)
- Knowing the trade's outcome and rationalizing the entry
- Marking levels AFTER seeing where price went

**The fix:**
- Use TradingView replay mode (hides future bars)
- Make decisions based ONLY on what's visible at the candle close
- Never scroll forward before deciding

### Survivorship Bias

**The mistake:** Only testing on assets/timeframes that "worked" historically.

**Example:** Testing only on Gold during 2024 trending periods, ignoring 2023 ranging period.

**The fix:**
- Backtest across multiple regimes (trending + ranging + volatile + calm)
- Use 1+ year of data, not cherry-picked weeks

### Curve Fitting / Over-Optimization

**The mistake:** Adjusting rules to fit historical data perfectly.

**Example:** "If I require 4 confirmations instead of 3, win rate jumps to 80%!" — works on past data, fails on new data.

**The fix:**
- Define rules BEFORE backtesting, don't change them based on results
- Out-of-sample testing (see below)

### Confirmation Bias In Subjective Systems

**The mistake:** Marking only the setups that worked, ignoring the ones that didn't.

**SMC is highly subjective.** What looks like "displacement" to you in hindsight may have been ambiguous in real-time.

**The fix:**
- Binary checklist (did the rule fire YES/NO?) instead of "did this look like a setup?"
- Audit your backtest with a peer or post screenshots publicly

---

## 2. The Binary Checklist Approach

To backtest a subjective system without cherry-picking, every rule must be **binary**.

### Your 6-Step Framework As Binary

For EVERY potential trade:

| Step | Binary Question | Answer |
|---|---|---|
| 1. DIRECTION | H4 structure: bullish (HH+HL) or bearish (LH+LL)? | YES / NO / UNCLEAR |
| 2. LOCATION | At significant H1/H4 zone (untested or fresh)? | YES / NO |
| 3. SWEEP | Liquidity swept (M15/M5 high/low cleared with wick)? | YES / NO |
| 4. BOS | Structure broke in your direction with displacement (large body)? | YES / NO |
| 5. RETEST | Price returned to broken level (OB/FVG)? | YES / NO |
| 6. R:R | Minimum 1:2 R:R after spread accounted? | YES / NO |

**Rule:** If ANY answer is NO or UNCLEAR → no trade. Move on.

This eliminates "well, kind of, sort of" judgment calls.

---

## 3. Sample Size — The Non-Negotiable Number

### Minimum For Statistical Significance

**100-200 trades per asset/regime combination.**

Below this:
- 50 trades: ~70% confidence (not enough)
- 30 trades: ~50% confidence (coin flip)
- 10 trades: ~25% confidence (pure noise)

### For Phase 1 Of Your Roadmap

Your roadmap says 50 backtests minimum. **Treat that as the floor, not the target.**

If possible:
- 100 backtests on XAUUSD (your only pair)
- Across both London and NY sessions
- Across calm and volatile regimes
- This gives you a real edge picture

---

## 4. Out-Of-Sample (OOS) Testing

### The Method

1. Split historical data into TWO blocks:
   - **In-sample (IS):** First 70% — used to define your rules
   - **Out-of-sample (OOS):** Last 30% — UNTOUCHED until system is finalized
2. Backtest your system on IS, refine until performance is acceptable
3. ONLY THEN test on OOS data
4. If OOS performance matches IS → real edge
5. If OOS performance crashes → curve-fit, refine more

### Example For Your System

- IS: October 2025 - February 2026 (5 months)
- OOS: March 2026 - May 2026 (3 months)
- Define system on IS. Don't peek at OOS until system is locked.

### Why This Matters

Without OOS testing, you might think you have an edge that exists ONLY in the data you tested. Live trading reveals the truth painfully.

---

## 5. Forward Testing (Live Demo)

After backtesting → forward test on demo for 2-4 weeks BEFORE live.

### Why

- Tests psychological friction (real-time decisions vs hindsight)
- Tests broker execution (slippage, fills)
- Tests your speed (can you actually identify and execute setups in real-time?)
- Tests routine (can you maintain discipline live?)

### Rules For Forward Testing

- Same risk % as live (treat demo like real)
- Same journaling (full discipline)
- Same trade frequency (don't overtrade because it's "free")
- Track demo P&L separately from backtests

⚠️ **Caveat:** Demo is NOT the same as live. Psychological pressure shifts. Use demo to validate execution speed, not edge confirmation.

---

## 6. Tools For Proper Backtesting

| Tool | Best For | Cost |
|---|---|---|
| **TradingView Replay** | Manual SMC backtests, easy to use | Free with TradingView Pro |
| **Forex Tester** | Tick-by-tick simulation, multiple TFs | Paid |
| **NakedMarkets** | Multi-pair simulation, proper bar replay | Paid |
| **Soft4FX** | MT4/MT5 native replay | Paid |
| **GoCharting** | Free bar replay, web-based | Free tier |

### For Your Phase 1

**TradingView Replay is sufficient.** Don't pay for tools yet.

### How To Use TradingView Replay Properly

1. Pick a date 3-6 months in the past
2. Use the "Bar Replay" feature
3. Hide future bars
4. Move forward bar by bar (or candle by candle on entry TF)
5. At each candle, ask: "Does this trigger any of my 6 steps?"
6. If yes, "execute" the trade mentally — note entry/SL/TP
7. Continue forward until SL or TP hits
8. Log the result honestly

---

## 7. The Rules-Based Rubric (Use This)

For each backtested setup, fill out:

```
TRADE #___
Date: ____
Asset: XAUUSD
Session: London / NY / Asian

SETUP:
[ ] H4 Direction: Bull / Bear / Unclear
[ ] H1 Location: At zone? Yes / No
[ ] M15 Sweep: Confirmed? Yes / No
[ ] M5 BOS: Confirmed? Yes / No
[ ] M5 Retest: Confirmed? Yes / No
[ ] R:R: ___ (must be ≥ 1:2)

ALL 6 BOXES TICKED? Yes → Trade. No → Skip.

EXECUTION:
Entry: ___
SL: ___
TP: ___
Size: 0.5% risk

OUTCOME:
Result: TP hit / SL hit / Manual exit (rule violation if so)
P&L (R): ___
P&L ($ on $3,000): ___

GRADE:
A — All rules followed, regardless of outcome
B — Minor hesitation but executed
C — Broke 1 rule
D — Broke 2+ rules

NOTES:
[Honest assessment of what happened]
```

---

## 8. What Backtest Results Should Look Like

After 50-100 backtested trades, your data should reveal:

### Useful Statistics
- Win rate (%)
- Average win (R)
- Average loss (R)
- Profit factor
- Expectancy per trade
- Max drawdown
- Best session (London vs NY)
- Best day of week
- Most common failure mode

### What "Good Enough" Looks Like

For Phase 1 → Phase 2 transition:
- Win rate: 40-55%
- Avg R:R achieved: 1:1.5 or better
- Profit factor: > 1.3
- Compliance: 80%+ A/B grade trades

If results are below these → refine system or extend backtest.

If results are far ABOVE these → suspect curve-fitting or look-ahead bias. Recheck.

---

## 9. Common Backtest Failures (Avoid These)

### Failure 1: "I Found 50 Perfect Setups That All Won"

**Reality:** You're cherry-picking. Real markets aren't 100% win rate.

**Fix:** Forced binary checklist. If a setup partially fits, it's a NO.

### Failure 2: "All My Losses Were 'Special Cases'"

**Reality:** Confirmation bias. You're explaining away losses to preserve ego.

**Fix:** Write the loss reason ON THE TRADE, then NEVER edit it.

### Failure 3: "I'll Stop Backtesting When I Have 50 Wins"

**Reality:** You're optimizing for results, not sample size.

**Fix:** Backtest 50 setups REGARDLESS of outcome. Then review.

### Failure 4: "This Backtest Took 4 Hours, I'm Done"

**Reality:** 50 trades in 4 hours = ~5 minutes per setup. Not enough analysis.

**Fix:** Treat each setup like a real trade. 15-20 minutes minimum per setup.

### Failure 5: "I'll Just Skip Setups That Didn't Work"

**Reality:** Worst possible bias. Defines edge by hindsight.

**Fix:** Mark EVERY setup that fits criteria, even ones you "feel" won't work.

---

## 10. Backtest → Live Transition

After 50+ valid backtests with positive results:

1. Forward test on demo for 2 weeks (10-15 trades)
2. Reduce live risk to 0.25% for first 10 live trades
3. After 10 successful live trades → 0.5% live risk
4. After 30 live trades → review data, decide phase progression

**Don't skip steps.** The friction between backtest and live is where most accounts blow up.

---

## 📋 Phase 1 Backtest Plan

For your specific situation:

- [ ] Goal: 50-100 backtested setups on XAUUSD
- [ ] Timeframe: 3-6 month historical window
- [ ] Sessions: London and NY (no Asian for now)
- [ ] Use TradingView replay
- [ ] Binary checklist for every setup
- [ ] Track in spreadsheet: win/loss, R achieved, session, day of week
- [ ] Stop at 50 minimum, push to 100 if time allows
- [ ] Review with mentor before going live

**Time estimate:** 50 setups × 15 min = ~12 hours. Spread across 2 weeks (1 hour/day = sustainable).

---

## 📚 Sources

- David Aronson, *Evidence-Based Technical Analysis*
- Statistical inference fundamentals
- TradingView Replay documentation
- Forex Tester methodology guides

Full citations in [`source-docs/deep-dive-full.md`](./source-docs/deep-dive-full.md).

---

> **The honest truth:** *"Most retail backtests are wishful thinking dressed up as analysis. Yours doesn't have to be."*
