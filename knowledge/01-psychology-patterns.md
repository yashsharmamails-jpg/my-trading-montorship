# 🧠 01 — Psychology Patterns: The 9 Confirmed Patterns

> **Source:** Distilled from Deep Dive Part 1 ([source-docs/deep-dive-full.md](./source-docs/deep-dive-full.md))
>
> **Use case:** When you catch yourself in a pattern, find it here. Get scientific name, root cause, and concrete intervention.

---

## 📋 Quick Pattern Index

| # | Pattern | Scientific Name | First Identified |
|---|---|---|---|
| 1 | Bias Lock | Confirmation Bias + Belief Perseverance | May 25 (Day 2) |
| 2 | Loss-Day Aversion | Myopic Loss Aversion | May 25 (Day 2) |
| 3 | Catastrophizing Perception | Prospect Theory (loss aversion coefficient) | May 25 (Day 2) |
| 4 | Revenge Sizing | Action Bias + Break-Even Effect | May 25 (Day 2) |
| 5 | Shame Lying | Cognitive Dissonance + Ego-Defense | May 25 (Day 2) |
| 6 | Compulsive Continuation | Dopamine Reward Prediction Error / Problematic Trading | May 24 (Day 1) |
| 7 | Mid-Trade Conviction Loss | Ambiguity Effect + Distress Intolerance | May 24 (Day 1) |
| 8 | Chart Addiction | Variable Ratio Reinforcement (B.F. Skinner) | May 23 (Day 0) |
| 9 | Anticipation Over Reaction | Illusion of Control | May 23 (Day 0) |

---

## 1. Bias Lock

**Scientific Name:** Confirmation Bias + Belief Perseverance

**Core Insight (Kahneman, *Thinking, Fast and Slow*):**
The brain seeks information validating an existing thesis and blinds itself to contradictory data. Once a directional bias is internally declared, the cognitive load to dismantle it is significantly higher than the load to rationalize conflicting market data.

**Your Manifestation:**
On May 25, after H4 bearish bias was clear, took 4 longs on M5/M1 evidence. Each loss reinforced "next one will work." Brain protected the thesis instead of updating.

**Concrete Intervention — "Premortem and Invalidation Trigger" Protocol:**

Before executing the 6-step framework, document the EXACT technical conditions that mathematically invalidate the bias.

**Implementation:**
- [ ] Before entry: write down 3 specific conditions that would prove your bias wrong
- [ ] If 1 of those 3 conditions triggers: pause, do NOT take a same-direction setup
- [ ] If 2 of 3 trigger: bias is invalidated, switch direction or stop trading
- [ ] **Hard rule:** After 3 consecutive sweeps fail to produce CHoCH in your direction → invert the chart Y-axis. Force the brain to see opposite perspective. Breaks the neuro-visual pattern recognition loop.

---

## 2. Loss-Day Aversion

**Scientific Name:** Myopic Loss Aversion

**Core Insight (Benartzi & Thaler, 1995, *Myopic Loss Aversion and the Equity Premium Puzzle*):**
Individuals evaluate portfolios too frequently, combining hypersensitivity to losses with short-term evaluation horizons. Daily P&L gets evaluated as if it matters statistically — it doesn't.

**Your Manifestation:**
"If I close in loss I'll lose confidence to be full-time trader." Treating one day of trading as identity-defining when it's just one of 250+ trading days per year.

**Concrete Intervention — Mask Daily P&L:**

- [ ] Configure trading platform to display risk in **R-multiples ONLY**, not fiat currency
- [ ] **Abandon daily P&L tracking entirely** — switch to 20-trade rolling window review
- [ ] Mathematical reframe: "Today is 1/250 of my year. Today's outcome is noise."
- [ ] Weekly review uses R-multiples and rule compliance %, NOT $ profit/loss

---

## 3. Catastrophizing Perception

**Scientific Name:** Prospect Theory — Loss Aversion Coefficient (~2.25:1)

**Core Insight (Kahneman & Tversky, *Prospect Theory: An Analysis of Decision Under Risk*):**
Losses loom psychologically ~2.25x larger than equivalent gains. A -0.45R loss can trigger the same physiological stress response as a -1R loss, creating phantom pain that drives retaliatory trades.

**Your Manifestation:**
On May 25, perceived a -$0.45 loss (Trade #5) as "-1R" — a 33x magnification. That phantom loss drove the next 2-3 revenge trades.

**Concrete Intervention — Forced Cooling Period:**

- [ ] **Mandatory 60-minute cooling period after ANY loss**, regardless of size
- [ ] During lockout: complete a cognitive reappraisal exercise:
  - Actual $ loss: ___
  - As % of account: ___
  - As fraction of max planned drawdown: ___
  - Remaining account after this loss: ___
- [ ] Required output: factual reframe of the loss in objective terms
- [ ] Do not unlock charts until reappraisal is written

---

## 4. Revenge Sizing

**Scientific Name:** Action Bias + Break-Even Effect

**Core Insight (Bar-Eli et al., 2007, *Action Bias Among Elite Soccer Goalkeepers*):**
In high-stress scenarios, individuals feel compelled to "do something" instead of waiting optimally. Compounded with break-even fixation, traders manipulate lot sizes and tighter SLs to gamble on noise while maintaining the illusion of rule compliance.

**Your Manifestation:**
On May 25 Trade #7: kept 0.5% risk but tightened SL → higher lots. Same risk %, different psychology. Bigger emotional weight per pip.

**Concrete Intervention — External Lot Size Cap:**

- [ ] Set a **broker-side max lot size** (not just a personal rule — a hard system limit)
- [ ] After ANY loss, the next trade's max lot size must be capped to your average winning trade's lot size
- [ ] **Hard rule:** If a trade requires lots > your normal position size to "hit a target P&L," it is not a valid setup
- [ ] Position sizing is calculated FROM SL distance, never the reverse
- [ ] Rule of thumb: never tighten SL more than 30% below your average to "fit more lots"

---

## 5. Shame Lying

**Scientific Name:** Cognitive Dissonance + Ego-Defense Mechanisms

**Core Insight (Leon Festinger, *A Theory of Cognitive Dissonance*):**
When actions (rule-breaking) conflict with identity (disciplined professional), acute psychological distress occurs. The immediate ego defense is to conceal or alter the narrative rather than address the underlying behavior.

**Your Manifestation:**
On May 25 told mentor about 1 loss / 3 trades when actually 2 losses + 1 BE / 5 trades. Lied first, came clean second.

**Concrete Intervention — Automated, Read-Only Trade Disclosure:**

- [ ] Use auto-journaling software (TradeZella, TraderSync, or similar) that imports MT4 history via API
- [ ] Mentor has read-only access — you cannot edit/hide
- [ ] **Removes the psychological barrier of manual confession** — data flows automatically
- [ ] Weekly: paste full MT4 trade history into journal, no exceptions
- [ ] Hard rule: if you find yourself wanting to omit a trade, that's the trade that goes first in the next mentor message

---

## 6. Compulsive Continuation

**Scientific Name:** Dopamine Reward Prediction Error / Problematic Trading

**Core Insight (Lee et al., Håkansson et al. 2021, multiple peer-reviewed sources):**
Short-term speculative trading induces neurochemical reward indistinguishable from pathological gambling. The brain becomes addicted to the **anticipation of outcome**, not the profit itself. Drives compulsive engagement.

**Your Manifestation:**
After 2 trades, brain says "one more." After 3, "one more." Demo-gambled after live limit on May 24. Took 5 trades on May 25 vs 2-trade limit.

**Concrete Intervention — Hard Daily Execution Lockout:**

- [ ] Once 2 live trades execute (regardless of outcome), **trading platform locks for 24 hours**
- [ ] Use broker-level restriction or third-party trade locker (Cold Turkey, Freedom blocker, MetaTrader risk addon)
- [ ] No "just one more" possible — the system is the limit
- [ ] **Severs the behavioral loop at neurological origin**

**Critical:** Mental discipline alone has failed 3 times so far. The system MUST be external.

---

## 7. Mid-Trade Conviction Loss

**Scientific Name:** Ambiguity Effect + Distress Intolerance

**Core Insight (Daniel Ellsberg, *Risk, Ambiguity, and the Savage Axioms*):**
Humans show extreme aversion to ambiguity. The moment a trade enters drawdown, probabilistic certainty becomes ambiguous, causing abandonment of statistically valid theses to escape immediate psychological discomfort.

**Your Manifestation:**
On May 24 Trade 1 (BTC): in drawdown, said "I can't find the logic anymore" — but the logic was still on the chart. Fear filtered perception.

**Concrete Intervention — "Execution-to-Lock" Rule:**

- [ ] Once entry, SL, TP are set: **minimize the charting platform**
- [ ] Manage trade exclusively via alert notifications at SL/TP
- [ ] Remove intra-candle micro-fluctuations from visual processing
- [ ] **No re-analysis once in trade** — the analysis was done before entry
- [ ] If you feel the urge to "check," set a 30-min timer and walk away

---

## 8. Chart Addiction

**Scientific Name:** Variable Ratio Reinforcement (B.F. Skinner) / Behavioral Addiction

**Core Insight (Skinner, operant conditioning research):**
Behaviors rewarded on unpredictable, variable schedules (like market setups) are the most addictive and hardest to extinguish. Demo gambling and post-limit chart staring are symptoms of deep operant conditioning.

**Your Manifestation:**
Day 1 (May 24): couldn't close charts after live limit, took random demo trades. Has been a 7-year pattern.

**Concrete Intervention — Physical Environment Shift:**

- [ ] Once daily limit reached: **physically power down the workstation**
- [ ] Initiate transition protocol: leave the room, change activity (walk, gym, food, social)
- [ ] **Environmental cues break reinforcement schedules**
- [ ] Use Cold Turkey / Freedom to block trading sites outside session windows
- [ ] Hard rule: phone has NO trading apps installed

---

## 9. Anticipation Over Reaction

**Scientific Name:** Illusion of Control

**Core Insight (Ellen Langer, *The Illusion of Control*):**
Individuals routinely act as if they can influence outcomes in systems governed by chance. Predicting price action is an ego-driven attempt to exert control over a stochastic environment.

**Your Manifestation:**
"I believe it will get swept" (May 25, before NY). Predicting before confirmation. Identity statement actually warns against this: *"I never anticipate. I react."*

**Concrete Intervention — "If-Then" Syntax:**

- [ ] **All market analysis must be written in conditional logic only**
- [ ] FORBIDDEN: "Price will sweep this level"
- [ ] REQUIRED: "IF price sweeps this level AND forms BOS THEN entry is valid at retest"
- [ ] No predictions in journal — only conditional triggers
- [ ] If you catch yourself writing a prediction, rewrite it as if-then

---

## 🔥 The Meta-Pattern

All 9 patterns share one common root:

> **Inability to tolerate uncertainty + ego-protection of identity.**

The market is uncertain by definition. Your brain (especially in psychosis recovery) struggles with that uncertainty. Identity protection ("I'm a smart trader") drives all 9 patterns:
- Bias Lock → "I can't be wrong about direction"
- Loss-Day Aversion → "I can't be a losing trader today"
- Catastrophizing → "Even small losses threaten my identity"
- Revenge Sizing → "I must restore my identity through profit"
- Shame Lying → "My identity is at risk if mentor sees full truth"
- Compulsive Continuation → "I'm a trader, so I must trade"
- Mid-Trade Conviction Loss → "I can't be wrong about this trade"
- Chart Addiction → "Trader = always watching markets"
- Anticipation → "Smart traders predict, not react"

**The fix is at the root, not the surface:** Decouple identity from trading. Trading is an activity, not an identity. You are a freelancer who does mental health work, has hobbies, and trades as a skill-building project.

---

## 🛠️ Implementation Priority

If you can only fix 3 things in the next 30 days:

1. **External lockout after 2 trades** (fixes #6 — biggest leverage)
2. **R-multiples instead of $ display** (fixes #2, #3 — biggest perceptual shift)
3. **Auto-journaling software** (fixes #5 — protects mentorship integrity)

These three are structural — they don't rely on willpower.

---

## 📚 Sources

- Kahneman, *Thinking, Fast and Slow* (2011)
- Kahneman & Tversky, *Prospect Theory* (1979)
- Benartzi & Thaler, *Myopic Loss Aversion and the Equity Premium Puzzle* (1995)
- Bar-Eli et al., *Action Bias Among Elite Soccer Goalkeepers* (2007)
- Festinger, *A Theory of Cognitive Dissonance* (1957)
- Ellsberg, *Risk, Ambiguity, and the Savage Axioms* (1961)
- Langer, *The Illusion of Control* (1975)
- B.F. Skinner, *Schedules of Reinforcement* (1957)
- Lee et al., Håkansson et al., trading-as-gambling research (2021+)

Full citations in [`source-docs/deep-dive-full.md`](./source-docs/deep-dive-full.md).
