# Renewal Management — Methodology

This document covers the core concepts, frameworks, and calculations behind Renewal Management. It provides the methodological foundation — the 'how it works' behind the execution steps.

---

## 1) Core Concepts

*The mental models, frameworks, and key distinctions that someone needs to understand before executing this project.*

### Proactive vs. Reactive Renewal Management

*What is it?*

Proactive renewal management means identifying and acting on renewal risks and opportunities 90+ days before contract end, using health data and structured cadences. Reactive renewal management means responding to renewals only when they surface -- an invoice is generated, a customer threatens to leave, or a contract silently lapses.

*Why does it matter?*

Resolving renewal issues proactively costs 3-5x less than handling them reactively [1]. Companies with proactive renewal processes report that 78% of customers who renewed despite competitive offers cited the proactive approach as a key retention factor [2]. The difference between a 90% GRR and an 85% GRR on a $10M ARR base is $500K in annual recurring revenue lost -- most of it preventable.

*Key insight:*

> Renewal management does not start 90 days before the contract ends. It starts at onboarding. Every interaction from day one either builds or erodes the renewal case. The 90/60/30-day cadence is the structured execution layer, but the foundation is laid in the months before.

*Examples:*

| Context | Proactive Approach | Reactive Approach |
|---------|-------------------|-------------------|
| Customer usage drops 40% in month 6 of a 12-month contract | CSM receives automated alert, schedules re-engagement call, offers targeted training | Nobody notices until 90-day renewal alert fires; customer has already evaluated competitors |
| Executive sponsor leaves the account | "Executive Sponsor Change" playbook triggers within 48 hours; new relationship-building begins | Discovered during renewal call that the new VP has no relationship with your team |
| Support tickets spike over 2 weeks | Health score drops from Green to Yellow; CSM proactively reaches out to understand root cause | Customer brings up unresolved frustrations during renewal negotiation as leverage for discount |

### Gross Revenue Retention (GRR) vs. Net Revenue Retention (NRR)

*What is it?*

**GRR** measures the percentage of recurring revenue retained from existing customers, excluding any expansion (upsells, cross-sells, price increases). It can only be 100% or lower. **NRR** includes expansion revenue on top of retained revenue, so it can exceed 100%. NRR tells you whether your existing customer base is growing or shrinking in total dollar terms.

*Why does it matter?*

GRR is the pure measure of retention health -- it reveals how much revenue you keep without relying on upsells to mask churn. A company with 85% GRR but 110% NRR has a churn problem hidden behind a strong expansion motion. If expansion slows (economic downturn, market saturation), the true retention weakness surfaces fast [3].

*Key insight:*

> GRR and NRR must always be viewed together. High NRR with declining GRR is a ticking time bomb -- it means you are relying on a smaller and smaller customer base to generate more and more expansion revenue. This pattern is unsustainable.

*Common misunderstandings:*

- **Misconception:** NRR above 100% means retention is healthy.
  **Reality:** NRR can mask significant churn. A company losing 20% of customers annually but expanding remaining accounts by 25% shows 105% NRR but has a serious retention problem that will compound.

- **Misconception:** GRR only matters for reporting to investors.
  **Reality:** GRR is the operational metric that tells your CS team whether their core job (keeping customers) is working. NRR tells the expansion team whether their job is working. Both teams need their own metric.

### Customer Health Scoring

*What is it?*

A composite metric that combines multiple customer signals -- product usage, support interactions, engagement patterns, and sentiment data -- into a single risk indicator (typically 0-100 or Red/Yellow/Green). The health score predicts whether an account is likely to renew, churn, or expand.

*Why does it matter?*

Health scores turn scattered signals into actionable prioritization. Without a health score, CSMs rely on gut feel and recency bias (the last customer who complained gets attention, not the silent one about to churn). Effective health scores flag churn risk 60-90 days before it happens [4], giving teams intervention time.

*The Framework:*

A health score is composed of four signal categories, each weighted by its predictive power:

```
Health Score = (Usage Weight * Usage Score) + (Support Weight * Support Score)
             + (Engagement Weight * Engagement Score) + (Sentiment Weight * Sentiment Score)
```

| Signal Category | What It Measures | Common Signals |
|----------------|------------------|----------------|
| Product Usage | Are they actually using what they bought? | Login frequency, feature adoption, active users vs. licensed seats |
| Support Health | Are they experiencing friction? | Ticket volume, escalation rate, time-to-resolution, unresolved issues |
| Engagement | Are they invested in the relationship? | Meeting attendance, email responsiveness, executive sponsor activity |
| Sentiment | How do they feel about you? | NPS/CSAT scores, qualitative feedback, renewal conversation tone |

*Common misunderstandings:*

- **Misconception:** More signals in the health score means better prediction.
  **Reality:** Aim for 4-6 strong signals. Adding weak or correlated signals introduces noise and makes the score harder to interpret and act on [5].

- **Misconception:** Health scores should be fully automated with no human input.
  **Reality:** The best health scoring models include a "CSM Pulse" -- a subjective 1-5 rating from the account owner that captures relationship signals no automation can detect (e.g., "the champion just told me they are evaluating alternatives").

### The Renewal Timeline (90/60/30-Day Cadence)

*What is it?*

A structured sequence of touchpoints and actions triggered at specific intervals before contract renewal. The 90-day mark initiates outreach, 60-day triggers follow-up and escalation for at-risk accounts, and 30-day triggers urgent action for unresolved renewals.

*Why does it matter?*

Without a structured cadence, renewals either get missed entirely or get compressed into a last-minute scramble that leaves no room for negotiation, risk mitigation, or expansion conversations. The cadence creates predictability for both the CS team and the customer.

*Key insight:*

> The 90/60/30 cadence is a minimum. For enterprise accounts with complex procurement cycles, start at 120 or even 180 days. Match the cadence to the customer's buying process, not your internal convenience.

*Examples:*

| Timeline | Action | Owner |
|----------|--------|-------|
| 90 days out | Initial renewal outreach; confirm renewal intent; surface any issues | CSM |
| 75 days out | Deliver value summary (usage data, ROI achieved, outcomes met) | CSM |
| 60 days out | Formal renewal proposal sent; expansion opportunity presented if applicable | CSM + Account Exec (if expansion) |
| 45 days out | Escalation for non-responsive or at-risk accounts to CS leadership | CS Manager |
| 30 days out | Final terms confirmation; contract sent for signature | CSM + Legal/Finance |
| 15 days out | Escalation to VP CS if unsigned; executive-to-executive outreach if needed | VP CS |

---

## 2) Decision Frameworks

*Matrices, decision trees, and "when to use what" guidance for Renewal Management approach selection.*

### Approach Selection Matrix

| Situation | Recommended Approach | Why |
|-----------|---------------------|-----|
| Early-stage company, &lt;50 accounts, no CS platform | Manual tracking + spreadsheet with CRM renewal date field | Tooling investment not justified yet; process design matters more than automation |
| Mid-market company, 50-500 accounts, CRM in place | CRM-native renewal tracking + basic health score + automated alerts | Scale requires automation, but native CRM capabilities are sufficient |
| Growth-stage company, 500+ accounts, CS platform available | Full health scoring model + automated cadences + renewal pipeline dashboard + risk intervention playbooks | Volume demands systematic approach; manual tracking creates blind spots |
| Enterprise accounts with 6+ month sales cycles | Extended cadence (180/120/90/60/30) + executive sponsor mapping + multi-threaded relationships | Long procurement cycles require earlier engagement; single-threaded relationships are high risk |

### Scoping Factors

**1. Customer Segment Mix**

- Primarily SMB (ACV &lt; $15K) -- Higher volume, more automation needed, accept some managed churn, focus health scoring on usage signals
- Primarily Mid-Market (ACV $15K-$100K) -- Balance of automation and human touch, health score includes engagement signals, CSM-led renewals
- Primarily Enterprise (ACV &gt; $100K) -- High-touch, executive-involved renewals, multi-threaded health scoring, custom renewal playbooks per account

**2. Data Maturity**

- No product usage data available -- Health score limited to support + engagement signals; prioritize getting usage data integrated as a parallel workstream
- Usage data available but not in CRM -- Integration project required before health scoring can be automated; start with manual health assessment
- Usage data flowing into CRM -- Ready for automated health scoring; weight usage signals at 30-40% of total score

**3. Existing Renewal Process Maturity**

- No process exists -- Start with basic 90/60/30 alerts and CSM playbook before adding health scoring complexity
- Ad hoc process exists -- Standardize and automate what works; add health scoring to prioritize CSM attention
- Mature process, seeking optimization -- Focus on predictive analytics, intervention playbooks, and expansion integration

**4. Contract Structure**

- Monthly contracts -- Renewal management shifts to continuous retention; health scoring and intervention become ongoing, not cadence-based
- Annual contracts -- Standard 90/60/30 cadence applies; most common pattern
- Multi-year contracts -- Lower frequency but higher stakes; start cadence earlier (180 days), include business review cycle

### CRM-Native Approach

*Best for:*
- Companies with fewer than 500 accounts
- Teams already using Salesforce or HubSpot with admin capacity
- Budgets that do not support a dedicated CS platform

*Not recommended for:*
- Companies needing predictive churn modeling (CRM formulas are limited)
- Teams managing 1,000+ accounts (CRM dashboards strain under volume)
- Organizations requiring automated intervention workflows

*Key differences from CS platform approach:*

| Aspect | CRM-Native | CS Platform (Gainsight, ChurnZero, Vitally) |
|--------|-----------|----------------------------------------------|
| Health scoring | Formula fields, manual or rule-based | Machine learning, multi-signal, automated |
| Alerts | Workflow rules, task creation | CTAs (Calls to Action), automated playbooks |
| Dashboard | CRM reports and dashboards | Purpose-built renewal cockpit |
| Cost | Included in CRM license | $15K-$80K+/year depending on platform and scale |
| Setup time | 2-4 weeks | 4-8 weeks |
| Maintenance | RevOps manages formulas and workflows | CS Ops manages platform configuration |

### CS Platform Approach

*Best for:*
- Companies with 500+ accounts needing automated health scoring
- Teams wanting predictive churn modeling and automated intervention
- Organizations with dedicated CS Ops capacity to manage the platform

*Not recommended for:*
- Early-stage companies still defining their renewal process
- Teams without CS Ops or RevOps to maintain the platform
- Companies with fewer than 200 accounts (over-engineering)

---

## 3) Benchmarks & Standards

### How to Use Benchmarks

*Benchmarks are guidelines, not rules. Always:*
1. Start with benchmark as baseline
2. Adjust based on client-specific data (segment, ACV, industry vertical)
3. Validate against their actual numbers when available
4. Document deviations and rationale

### Retention Rate Benchmarks

| Metric | Low | Typical (Median) | High (Top Quartile) | Notes |
|--------|-----|-------------------|---------------------|-------|
| Gross Revenue Retention (GRR) | &lt;85% | 90% | &gt;95% | Median across B2B SaaS [3][6] |
| Net Revenue Retention (NRR) - Enterprise | &lt;105% | 118% | &gt;130% | Enterprise segment, ACV &gt;$100K [7] |
| Net Revenue Retention (NRR) - Mid-Market | &lt;100% | 108% | &gt;120% | Mid-Market segment [7] |
| Net Revenue Retention (NRR) - SMB | &lt;90% | 97% | &gt;105% | SMB segment, ACV &lt;$15K [7] |
| Annual Logo Churn Rate | &gt;15% | 10-12% | &lt;7% | Percentage of customers lost per year [8] |
| Annual Revenue Churn Rate | &gt;15% | 11-12.5% | &lt;8% | Percentage of ARR lost per year [6] |

**Source:** Benchmarkit 2024/2025 B2B SaaS Performance Metrics Report [3], Optifai NRR Benchmark Analysis (N=939 companies) [7], Maxio 2025 SaaS Benchmarks Report [6].

**Interpretation:**
- **GRR below 85%:** Red flag. Indicates a product-market fit, customer experience, or pricing problem. Investigate churn reasons by category (preventable vs. unpreventable).
- **GRR above 95%:** Strong retention. Focus shifts to expansion (NRR growth) rather than retention rescue.
- **NRR below 100%:** Customer base is shrinking in dollar terms. Even with new logo acquisition, growth requires running faster just to stay in place.

### Health Score Benchmarks

| Metric | Red Flag | Warning | Healthy | Notes |
|--------|----------|---------|---------|-------|
| Product login frequency | &lt;1x/week | 1-3x/week | Daily | Relative to contracted use case |
| Feature adoption rate | &lt;30% of key features used | 30-60% | &gt;60% | Measured against features included in their tier |
| Support ticket escalation rate | &gt;20% of tickets escalated | 10-20% | &lt;10% | Percentage of tickets requiring manager involvement |
| NPS score | &lt;0 (Detractor) | 0-30 (Passive) | &gt;30 (Promoter) | Account-level NPS, not aggregate |
| License utilization | &lt;50% of seats active | 50-75% | &gt;75% | Active users / licensed seats |
| CSM Pulse rating | 1-2 | 3 | 4-5 | Subjective CSM assessment on 1-5 scale |

### Renewal Cycle Timing Benchmarks

| Question | Good | Warning | Red Flag |
|----------|------|---------|----------|
| What % of renewals have an owner assigned 90+ days out? | &gt;95% | 80-95% | &lt;80% |
| What % of renewal outreach happens on schedule (per cadence)? | &gt;90% | 70-90% | &lt;70% |
| What % of renewals close before contract end date? | &gt;85% | 70-85% | &lt;70% |
| Average days from first renewal outreach to signed contract? | &lt;45 days | 45-75 days | &gt;75 days |
| What % of churned accounts had a health score warning 60+ days prior? | &gt;80% | 50-80% | &lt;50% (health score is not predictive) |

### Quick Reference Thresholds

| Question | Good | Warning | Red Flag |
|----------|------|---------|----------|
| Is our GRR healthy? | &gt;90% | 85-90% | &lt;85% |
| Is our NRR healthy? (overall) | &gt;106% | 100-106% | &lt;100% |
| Are we catching churn early enough? | &gt;80% flagged 60+ days out | 50-80% flagged | &lt;50% flagged |
| Is our health score accurate? | &gt;70% of churned accounts were flagged Red/Yellow | 50-70% flagged | &lt;50% (recalibrate model) |
| Is our CSM capacity sufficient? | &lt;40 accounts per CSM (mid-market) | 40-60 accounts | &gt;60 accounts |

---

## 4) Calculations & Scoring

### Formula Quick Reference

| Calculation | Formula | Example |
|-------------|---------|---------|
| Gross Revenue Retention | `(Start ARR - Churn ARR - Contraction ARR) / Start ARR` | ($10M - $800K - $200K) / $10M = 90% |
| Net Revenue Retention | `(Start ARR - Churn ARR - Contraction ARR + Expansion ARR) / Start ARR` | ($10M - $800K - $200K + $1.5M) / $10M = 105% |
| Customer Health Score | `Sum of (Weight_i * Normalized Score_i)` for each signal | (0.35 * 80) + (0.25 * 60) + (0.25 * 70) + (0.15 * 90) = 73 |
| Churn Cost Impact | `Churned ARR * (1 / GRR_improvement_target)` | $1M churn * (1/0.05) = $20M in new ARR needed to offset at 5% conversion |
| Renewal Rate | `Renewed ARR / Up-for-Renewal ARR` | $8.5M / $10M = 85% |

### Gross Revenue Retention (GRR) Calculation

**Formula:**
```
GRR = (Beginning Period ARR - Churn ARR - Contraction ARR) / Beginning Period ARR
```

**Variables explained:**
- `Beginning Period ARR` = Total annual recurring revenue from existing customers at start of period
- `Churn ARR` = Revenue lost from customers who fully cancelled
- `Contraction ARR` = Revenue lost from customers who downgraded (but stayed)

**Worked Example:**

*Scenario: Mid-market B2B SaaS company, Q1 calculation*

```
Given:
- Beginning ARR (existing customers): $5,000,000
- Churn ARR (3 customers fully left): $180,000
- Contraction ARR (5 customers downgraded): $70,000

Calculate:
- Retained ARR = $5,000,000 - $180,000 - $70,000 = $4,750,000
- GRR = $4,750,000 / $5,000,000 = 95.0%
```

**Validation:**
- GRR should always be between 0% and 100% (it cannot exceed 100%)
- If GRR is below 85%, investigate whether churn is concentrated in a specific segment
- Annualize quarterly GRR carefully: Annual GRR is roughly (Quarterly GRR)^4, not Quarterly GRR * 4

### Net Revenue Retention (NRR) Calculation

**Formula:**
```
NRR = (Beginning Period ARR - Churn ARR - Contraction ARR + Expansion ARR) / Beginning Period ARR
```

**Variables explained:**
- All GRR variables, plus:
- `Expansion ARR` = Revenue gained from existing customers through upsells, cross-sells, and price increases

**Worked Example:**

*Scenario: Same company as above*

```
Given:
- Beginning ARR: $5,000,000
- Churn ARR: $180,000
- Contraction ARR: $70,000
- Expansion ARR: $400,000

Calculate:
- Net Retained ARR = $5,000,000 - $180,000 - $70,000 + $400,000 = $5,150,000
- NRR = $5,150,000 / $5,000,000 = 103.0%
```

**Validation:**
- NRR above 100% means the existing customer base is growing on its own (without new logos)
- NRR below 100% means expansion is not offsetting churn -- the customer base is contracting
- Compare NRR to GRR: if the gap is large (e.g., GRR 85%, NRR 110%), expansion is masking a retention problem

### Customer Health Score Calculation

**Formula:**
```
Health Score = (W_usage * S_usage) + (W_support * S_support) + (W_engagement * S_engagement) + (W_sentiment * S_sentiment)
```

Where each signal (S) is normalized to 0-100 and weights (W) sum to 1.0.

**Recommended Starting Weights:**

| Signal Category | Weight (Mid-Market) | Weight (Enterprise) | Weight (SMB/Tech-Touch) |
|----------------|--------------------|--------------------|------------------------|
| Product Usage | 0.35 | 0.25 | 0.45 |
| Support Health | 0.25 | 0.20 | 0.25 |
| Engagement | 0.25 | 0.30 | 0.15 |
| Sentiment (NPS/CSAT/CSM Pulse) | 0.15 | 0.25 | 0.15 |

*Source: Composite recommendation from Gainsight [4], Vitally [5], and practitioner frameworks. Adjust based on historical churn correlation analysis.*

**Worked Example:**

*Scenario: Mid-market account, annual contract*

```
Given (all normalized to 0-100):
- Usage Score: 75 (daily logins, 65% feature adoption, 80% seat utilization)
- Support Score: 55 (elevated ticket volume, 1 escalation this quarter)
- Engagement Score: 85 (attends QBRs, responds to emails, executive sponsor active)
- Sentiment Score: 70 (NPS = 25, CSM Pulse = 4/5)

Weights (mid-market): Usage=0.35, Support=0.25, Engagement=0.25, Sentiment=0.15

Calculate:
- Health Score = (0.35 * 75) + (0.25 * 55) + (0.25 * 85) + (0.15 * 70)
- Health Score = 26.25 + 13.75 + 21.25 + 10.50
- Health Score = 71.75 → Round to 72
```

**Tier Thresholds:**

| Tier | Score Range | Status | Action |
|------|-------------|--------|--------|
| Green / Healthy | 75-100 | Low risk | Standard renewal cadence; explore expansion |
| Yellow / At-Risk | 50-74 | Moderate risk | Proactive intervention; CSM outreach within 1 week |
| Red / Critical | 0-49 | High risk | Immediate escalation; intervention playbook within 48 hours |

**Calibration requirement:** Test the health score against the last 12 months of churned accounts. If fewer than 70% of churned accounts had a Yellow or Red score 60+ days before churn, the model needs recalibration (adjust weights or add signals).

### Scoring Rubrics

**Signal Normalization Rubric (Usage Score Example):**

| Criterion | Points (0-100) | Threshold |
|-----------|----------------|-----------|
| Login frequency | 0-30 | 0 = no logins in 30 days; 30 = daily logins |
| Feature adoption | 0-35 | 0 = &lt;10% features used; 35 = &gt;70% features used |
| Seat utilization | 0-35 | 0 = &lt;25% seats active; 35 = &gt;90% seats active |
| **Total** | **100** | |

**Signal Normalization Rubric (Support Score Example):**

| Criterion | Points (0-100) | Threshold |
|-----------|----------------|-----------|
| Ticket volume trend | 0-30 | 0 = increasing &gt;50% QoQ; 30 = flat or decreasing |
| Escalation rate | 0-35 | 0 = &gt;25% escalation rate; 35 = &lt;5% escalation rate |
| Open issue count | 0-35 | 0 = 5+ unresolved issues; 35 = 0 unresolved issues |
| **Total** | **100** | |

**Signal Normalization Rubric (Engagement Score Example):**

| Criterion | Points (0-100) | Threshold |
|-----------|----------------|-----------|
| Meeting attendance | 0-30 | 0 = no meetings in 90 days; 30 = attends all scheduled |
| Email responsiveness | 0-30 | 0 = no response in 14+ days; 30 = responds within 48 hours |
| Executive sponsor status | 0-40 | 0 = no sponsor identified; 40 = active, engaged sponsor |
| **Total** | **100** | |

---

## 5) Edge Cases & Deep Dives

*The tricky scenarios that require special handling -- institutional knowledge for Renewal Management.*

### Edge Case 1: New Customer with No Historical Health Data

*Scenario:*

A customer signed 3 months ago and their first renewal is in 9 months. There is not enough historical data to generate a meaningful health score -- no usage trend, no NPS baseline, no support pattern established.

*Challenge:*

The health scoring model depends on trend data (is usage increasing or decreasing?), but new accounts only have a single data point. Applying the standard model generates misleading scores -- a new account with low usage might be in onboarding ramp-up, not declining.

*Approach:*

1. Use a separate "Onboarding Health" model for the first 90 days, based on milestone completion (onboarding steps completed, first value achieved, training attended)
2. Transition to the standard health model at day 90, using the onboarding milestones as a baseline adjustment
3. Flag any account that has not completed onboarding milestones by day 60 as Yellow regardless of other signals

*Fallback assumptions:*

| Missing Data | Use This Instead | Source |
|--------------|------------------|--------|
| No usage trend | Onboarding milestone completion rate | Implementation checklist tracking |
| No NPS baseline | CSM Pulse rating (subjective) | CSM relationship assessment |
| No support history | Onboarding friction signals (number of support contacts during setup) | Support system |

### Edge Case 2: Multi-Product or Multi-Contract Accounts

*Scenario:*

A customer has 3 separate contracts for different products, each with different renewal dates, different CSM owners, and different usage patterns. One product is healthy (Green), one is at-risk (Yellow), and one is critical (Red).

*Challenge:*

The account-level health score averages across products and shows Yellow, which masks both the healthy product (no expansion attention) and the critical product (insufficient urgency). Renewal conversations become confused when multiple contracts are discussed simultaneously.

*Approach:*

1. Create health scores at the **product/contract level**, not just the account level
2. Display the account-level score as the **lowest product score** (worst-case principle), not the average
3. Assign a primary renewal owner per contract, with an account-level coordinator for multi-product accounts
4. Stagger renewal conversations -- do not combine multiple renewals into one call unless the customer requests it

### Edge Case 3: Customer with Declining Usage but No Churn Intent

*Scenario:*

A customer's product usage has dropped 50% over the past quarter, triggering a Red health score. But when the CSM reaches out, the customer explains they completed a seasonal project and their usage pattern is cyclical. They fully intend to renew.

*Challenge:*

The health score correctly identified a usage decline, but the context makes the decline benign. If the team over-reacts, it wastes CSM time and annoys the customer. If this pattern is not documented, it will trigger the same false alarm next year.

*Approach:*

1. Add a "Usage Pattern" override field to the health score (options: Steady, Seasonal, Project-Based, Ramping)
2. When override is set to Seasonal or Project-Based, usage signal weight drops to 0.15 (from 0.35) and engagement weight increases proportionally
3. Document the seasonal pattern in the account record so future CSMs understand the context
4. Set a calendar reminder to verify the expected usage increase at the start of next season

### Edge Case 4: Renewal Owner Leaves Mid-Cycle

*Scenario:*

The assigned CSM leaves the company 45 days before a major enterprise renewal worth $250K ARR. The incoming CSM has no relationship with the customer's executive sponsor, and the renewal conversation was already in progress.

*Challenge:*

Relationship continuity is broken at the most critical moment. The customer may interpret the CSM change as a signal that your company does not prioritize their account.

*Approach:*

1. CS leadership (Manager or VP) steps in as interim renewal owner for the remaining 45 days
2. Schedule an immediate warm handoff call: outgoing CSM (if available) or CS Manager introduces the new contact
3. Send the customer a written summary of all renewal discussions to date, terms agreed, and open items
4. Accelerate the renewal timeline -- aim to close in 2 weeks rather than letting it drift to the 30-day mark
5. After renewal, the permanent new CSM takes over for the ongoing relationship

### Edge Case 5: Auto-Renewal Contracts with No Active Management

*Scenario:*

60% of the customer base has auto-renewal clauses. The CS team assumes these accounts will renew automatically and focuses all attention on non-auto-renewal accounts. Several auto-renewal customers cancel within their notice window because nobody checked on them.

*Challenge:*

Auto-renewal creates a false sense of security. Customers can still cancel during the notice period (typically 30-60 days before renewal), and the lack of proactive outreach means churn signals go undetected until it is too late.

*Approach:*

1. Treat auto-renewal accounts with the same health scoring and monitoring as non-auto-renewal accounts
2. Modify the cadence: instead of a full 90/60/30 renewal conversation, auto-renewal accounts get a 90-day "check-in" and a 60-day "value summary" -- lighter touch, but not zero touch
3. Flag any auto-renewal account with a Yellow or Red health score for full renewal treatment regardless of auto-renewal status
4. Track the notice period deadline as an escalation trigger: if no positive engagement by 15 days before the cancellation window opens, escalate

---

## References

[1] [Customer Success Collective - A Step-by-Step Guide to Retention, Renewals, and Expansion](https://www.customersuccesscollective.com/a-step-by-step-guide-to-retention-renewals-and-expansion/)

[2] [Sixteen Ventures - Customer Success: Shifting from Reactive to Proactive Retention](https://sixteenventures.com/reactive-to-proactive-retention)

[3] [Benchmarkit - 2024 SaaS Performance Metrics](https://www.benchmarkit.ai/2024benchmarks)

[4] [Gainsight - Customer Health Scores Explained: Metrics, Models & Tools](https://www.gainsight.com/blog/customer-health-scores/)

[5] [Vitally - How to Create a Customer Health Score with 4 Metrics](https://www.vitally.io/post/how-to-create-a-customer-health-score-with-four-metrics)

[6] [Maxio - 2025 B2B SaaS Benchmarks Report](https://www.maxio.com/resources/2025-saas-benchmarks-report)

[7] [Optifai - B2B SaaS NRR Benchmark: 97-118% by Segment (939 Companies)](https://optef.ai/learn/questions/b2b-saas-net-revenue-retention-benchmark/)

[8] [Wudpecker - Retention Benchmarks for B2B SaaS in 2025](https://www.wudpecker.io/blog/retention-benchmarks-for-b2b-saas-in-2025)

[9] [ChurnKey - Customer Acquisition vs. Retention: Cost Comparison Guide](https://churnkey.co/blog/customer-acquisition-vs-retention-cost-comparison-guide/)

[10] [Vitally - B2B SaaS Churn Rate Benchmarks](https://www.vitally.io/post/saas-churn-benchmarks)
