# ⚙️ 06 — Trade Management: SL, BE, Partials, Trailing

> **Source:** Distilled from Deep Dive Part 7 ([source-docs/deep-dive-full.md](./source-docs/deep-dive-full.md))
>
> **Use case:** What you do AFTER entry decides if winners pay for losers. Most traders destroy good systems with bad management.

---

## 🚨 The Counter-Intuitive Truth

> **Standard trading wisdom on trade management is mostly WRONG.**
>
> "Move SL to BE at +1R" — psychologically comforting, mathematically destructive.
> "Always take partial profits" — feels safe, degrades expectancy.
> "Trail stops tightly" — gets you out of trends early.

This chapter is data-driven, not folklore-driven.

---

## 1. Stop Loss Placement — Beyond The Standards

### The Wrong Ways
- ❌ Fixed pip SL (e.g., "always 30 pips") — ignores market mechanics
- ❌ Percentage of equity SL (e.g., "always 1%") — backwards calculation
- ❌ Time-based SL (e.g., "out after 30 min") — abandons valid trades
- ❌ Round number SL — institutional algorithms specifically hunt these

### The Right Way: Structural SL + ATR Buffer

```
SL = beyond the sweep level + (0.25 - 1.0) × ATR-14
```

The multiplier depends on volatility regime:
- **Calm regime:** 0.25 × ATR buffer
- **Normal regime:** 0.5 × ATR buffer
- **Volatile regime:** 1.0 × ATR buffer

### Why This Works

- Beyond sweep = beyond the level where the trade thesis is invalidated
- ATR buffer = noise tolerance based on current market behavior
- Adapts to regime automatically
- Avoids stop hunts by institutional algorithms

### Example (Gold, calm regime, ATR-14 = $20)

- Sweep low at 4555.00
- ATR buffer: 0.25 × $20 = $5 = 50 points
- SL placement: 4555.00 - 50 points = 4554.50

Adjust position size to maintain 0.5% risk based on this SL distance.

---

## 2. Move To Break-Even? The Industry Standard Is Wrong

### What Most Traders Do
- Move SL to BE when price hits +1R
- "Risk-free trade" psychology
- Feels good, looks responsible

### Why It's Wrong

**Research (cited in source docs):**
> *"Moving SL to BE early often reduces expectancy."*

**Why:**
1. Markets need room to breathe, retest, and accumulate
2. Most trends require a retracement that violates +1R area
3. Premature BE stops you out **just before** the true expansion
4. You lose the trade WHILE STILL BEING RIGHT about direction

### The Math

If your average winner runs to +2R, and you're stopping yourself out at BE 30% of the time on what would be winners → you're losing ~30% of your average winning trade size as cost.

That's a massive expectancy hit.

### What To Do Instead

**Option A: Don't move SL at all**
- Leave SL at structural invalidation
- Either trade hits TP or hits original SL
- Cleanest from expectancy perspective
- **Best for: backtesting validation, learning**

**Option B: Move SL only after structural confirmation**
- Wait for price to break a NEW structural level in your direction (e.g., new HH in uptrend)
- Then move SL behind THAT new level (not to entry)
- Trail behind structure, not pip distance
- **Best for: live trading once you've proven your system**

**Option C: Hybrid for psychology**
- Move SL to BE only after price has moved +2R (not +1R)
- This gives the trade much more room
- Still psychologically comforting
- **Best for: traders who can't sleep with full SL exposure**

### For Your Phase 1

**Use Option A (don't move SL).** Keep it simple. Validate the system without trade management complexity. You can introduce Option B in Phase 3 once you have data.

---

## 3. Partial Profits — Convenient Lie

### What Most Traders Do
- Close 50% at 1:1 R:R
- "Lock in profit"
- Let the rest run

### Why The Math Doesn't Work

**Research:**
> *"While taking partials reduces emotional pressure, it systematically degrades the mathematical expectancy of the system."*

**The math:**
- Let's say you take 50% off at 1R, full close at 3R
- Effective average winner: (0.5 × 1R) + (0.5 × 3R) = 2R
- vs. full position to 3R: 3R
- You sacrificed 1R of expectancy for psychological comfort

**Over 100 winning trades:** that's 100R of lost expectancy. At 0.5% risk, that's 50% of account growth.

### When Partials DO Make Sense

- Major resistance/supply zone reached
- Logical structural target hit (PDH, weekly high)
- Volatility regime shifted mid-trade
- News event approaching

NOT mechanical "take 50% at 1R."

### For Your Phase 1

**Don't take partials.** Full close at TP. This is what your system says. Stick to it. Validate first, optimize later.

---

## 4. Trailing Stops — Mostly Wrong

### What Most Retail Traders Do
- Trail SL by fixed pip count (e.g., 20 pips behind price)
- Get stopped out on minor pullbacks
- Miss the meat of moves

### Why It's Wrong

Markets pull back. That's what they do. A tight trailing stop guarantees you exit on the pullback before continuation.

### The Right Way: Trail Behind Structure

In an uptrend:
- Wait for price to make a new HH
- Wait for the resulting HL (pullback that holds)
- Move SL to JUST BELOW that HL
- Repeat

This way:
- Stops aren't moving constantly
- You only move SL after STRUCTURE confirms continuation
- You give the market room to retrace within structure

### When NOT To Trail

- High-impact news within next 30 min — fixed SL only
- Late session (after 10 PM IST) — close before liquidity dries
- Volatile regime — wider stops, no trailing

### For Your Phase 1

**Don't trail.** Set SL once, set TP once, walk away. This is the rule.

---

## 5. The "No-Touch" Rule (Critical For You)

### Definition

**Once entry, SL, and TP are set: do NOT modify the trade.**

The ONLY exception:
- News event imminent that wasn't expected at entry → consider closing (but only if 30+ min before release)
- Trade has been open >24 hours and structural invalidation occurred → reassess

### Why This Matters For You Specifically

You have:
- Mid-trade conviction loss (Pattern #7)
- Compulsive engagement (Pattern #6)
- Manual exit history (Trade #2 BTC, Trade #7 XAUUSD)

The act of "managing" the trade is an opportunity for these patterns to fire.

**The cure: physically REMOVE the option to manage.**

### Implementation

- [ ] Set entry, SL, TP
- [ ] Take screenshot of trade
- [ ] **Minimize the platform**
- [ ] Set alert for SL hit, TP hit
- [ ] Walk away — phone, gym, food, anything
- [ ] Return only when alert fires

### The Psychological Benefit

Mark Douglas (*Trading in the Zone*) emphasizes:
> *"The mistake is in being IN the trade. Once you're in, you're done. The rest is just watching the market do what the market does."*

---

## 6. Holding Through News — Don't

### The Reality
- Spreads widen 5-20x during news
- Slippage destroys SL placement
- Order flow vacuum (no counter-orders)
- Price often whipsaws both directions

### The Math
On a 0.07 lot trade with normal $14 spread cost vs $200 news spread cost:
- You enter expecting $14 friction
- You actually pay $200
- That's a $186 unexpected loss BEFORE the trade thesis even plays out

### The Rule
- Check ForexFactory at start of session
- Block out 30 min before to 60 min after high-impact events
- If a trade is open and news approaches: close 30+ min before
- Re-enter with structure 1+ hour after the dust settles

---

## 7. End-Of-Session Management

### The "Last Hour" Trap
- 9 PM - 11:30 PM IST in NY session: setups appear but liquidity thins
- "Last chance" psychology: traders take marginal setups
- These often fail — institutions are squaring positions, not opening new ones

### Hard Rules
- [ ] No new entries after 10 PM IST
- [ ] If trade is in profit at 10:30 PM IST → consider closing (illiquidity overnight risk)
- [ ] Friday after 9 PM IST: close all positions, no new entries (weekend gap risk)
- [ ] If trade is in drawdown at session end → keep SL, accept overnight risk OR close at small loss (your choice, document the decision)

---

## 8. The Trade Management Hierarchy

For Phase 1 (where you are now):

```
Priority 1: Don't touch the trade after entry
Priority 2: Let SL or TP close the position
Priority 3: Don't take partials
Priority 4: Don't trail SL
Priority 5: Don't move SL to BE
Priority 6: Don't add to losers
Priority 7: Don't add to winners
```

**Phase 1 is about VALIDATION. Trade management complexity is for Phase 3 after data exists.**

---

## 📋 Pre-Trade & Post-Trade Management Checklist

### Before Entry
- [ ] SL placed at structural invalidation + ATR buffer
- [ ] TP placed at next significant liquidity pool
- [ ] R:R minimum 1:2 after spread
- [ ] Position size calculated to maintain 0.5% risk

### After Entry (within 1 minute)
- [ ] SL order set on platform (not mental)
- [ ] TP order set on platform (not mental)
- [ ] Screenshot taken
- [ ] Journal entry started

### After Entry (rest of trade)
- [ ] DO NOT move SL
- [ ] DO NOT move TP
- [ ] DO NOT take partials
- [ ] DO NOT close manually
- [ ] DO NOT add to position
- [ ] Minimize platform, set alerts, walk away

### After Trade Closes (immediately)
- [ ] Update journal with exit price
- [ ] Calculate actual R achieved
- [ ] Note any rules broken
- [ ] Grade A/B/C/D based on PROCESS, not outcome
- [ ] If a winner: do NOT immediately look for next trade

---

## 🚨 Your Specific Trade Management Failures (Reference)

To remember why these rules exist:

### May 24 Trade #2 (BTC)
- **Failure:** Manually exited in profit at +$5
- **Should have:** Held to TP target, would have made +$30+
- **Pattern:** Mid-trade conviction loss

### May 25 Trade #7 (XAUUSD)
- **Failure:** Manual close at +$45 above TP
- **Should have:** Either let TP fire OR not been in this trade (5th of day)
- **Pattern:** Loss-day aversion + manual exit + revenge sizing

**Your trade management is the second-biggest leak in your account, after overtrading.**

---

## 📚 Sources

- Binance Square: Breakeven Stop Loss research
- Heygotrade: Partial Profit Taking explained
- ActivTrades: Partial vs full TP analysis
- Reddit r/algotrading: Quantitative partials experiments
- NAGA: ATR usage research
- EBC: True Volatility Index ATR

Full citations in [`source-docs/deep-dive-full.md`](./source-docs/deep-dive-full.md).

---

> **The mantra:** *"Once entered, only SL or TP closes the trade. Period. Always."*
>
> — Non-negotiable rule, your own ROADMAP
