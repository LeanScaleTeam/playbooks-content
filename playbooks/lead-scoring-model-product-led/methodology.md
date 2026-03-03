# Lead Scoring Model (Product-Led) — Methodology

This document covers the core concepts, frameworks, and calculations behind the Lead Scoring Model (Product-Led). It provides the methodological foundation — the "how it works" behind the execution steps.

---

## 1) Core Concepts

### Product-Qualified Leads (PQLs) vs. Marketing-Qualified Leads (MQLs)

*What is it?*

A Product-Qualified Lead (PQL) is a prospect who has demonstrated buying intent through actual product usage -- not just marketing engagement. Unlike MQLs, which are triggered by content downloads, webinar attendance, or email clicks, PQLs are identified by in-product behaviors: feature adoption, usage frequency, milestone completion, and collaboration signals. The PQL model assumes that using the product is the strongest indicator of purchase intent.

*Why does it matter?*

PQLs convert to paid at 25-30% with sales engagement, compared to 5-13% for traditional MQLs [1][2]. This 2-5x conversion advantage exists because product usage proves the prospect has experienced value firsthand -- they are not just researching, they are already using. For B2B SaaS companies with free trials or freemium models, building scoring around product signals rather than marketing signals is the single highest-impact change to pipeline quality.

*Key insight:*

> A prospect who has integrated your product with their CRM and invited two teammates is telling you more about their buying intent than someone who downloaded five whitepapers. Product behavior is proof of value; marketing behavior is proof of curiosity.

*Examples:*

| Context | Example |
|---------|---------|
| Free trial user completes onboarding, uses core feature 5x in first week, invites 2 teammates | PQL -- high activation signals, collaboration intent. Score: 75+ |
| Prospect downloads 3 ebooks, attends webinar, opens 10 emails | MQL -- marketing engagement only, no product usage data. Traditional model scores high; PQL model scores low |
| Freemium user logs in once, creates account, never returns | Neither -- no activation achieved. Behavioral score stays near zero despite account creation |

### Dual-Score Architecture (Fit + Behavior)

*What is it?*

Dual-score architecture maintains two separate scores for every lead: a **Fit Score** (firmographic/demographic match to ICP) and a **Behavioral Score** (product usage and engagement signals). These are calculated independently and then combined into a Total Lead Score. The separation matters because fit and behavior answer different questions: "Is this the right type of company?" vs. "Is this person showing buying intent?"

*Why does it matter?*

Keeping scores separate prevents two failure modes. First, a perfect-fit company (Fortune 500, ICP industry, right title) that never uses the product should not appear as a hot lead -- their fit score is high but behavioral score is zero, and sales should not waste time on them. Second, a highly engaged user from a non-ICP company (too small, wrong industry) should not clog the sales queue either. Only when both scores are above minimum thresholds does the lead become a PQL [3][4].

*The Framework:*

```
Fit Score (0-50)          Behavioral Score (0-100)
|-- Company size match    |-- Activation milestones
|-- Industry match        |-- Feature usage frequency
|-- Job title/seniority   |-- Collaboration signals
|-- Tech stack fit        |-- High-intent actions
+-- Geography match       |-- Engagement velocity
                          +-- Recency decay (subtractive)

Combined: Total Lead Score = Fit Score + Behavioral Score (0-150)
PQL Threshold: Total Score >= 80 AND Fit Score >= 15 AND Behavioral Score >= 40
```

*Common misunderstandings:*

- **Misconception:** A single combined score is sufficient -- just add fit and behavior together.
  **Reality:** A single score hides why the lead qualified. A lead with a total of 80 could be 50 fit + 30 behavior (good company, low engagement) or 20 fit + 60 behavior (bad fit, high engagement). Sales needs both numbers to decide how to approach the lead.

- **Misconception:** Behavioral scoring should count all product activity equally.
  **Reality:** Not all product actions carry the same signal strength. Visiting the pricing page or inviting a teammate is a much stronger buying signal than logging in or viewing a help article. Weight actions by their correlation with conversion, not by frequency alone.

### Activation Milestones and the "Aha Moment"

*What is it?*

Activation milestones are specific in-product actions that correlate with a user reaching the product's core value -- often called the "aha moment." These milestones are identified by analyzing the behavioral differences between users who converted to paid and users who churned during their trial or freemium experience. Common activation milestones include: completing onboarding setup, using a core feature a threshold number of times, integrating with another tool, and inviting teammates [5].

*Why does it matter?*

Activation milestones are the backbone of the behavioral scoring model. Without identifying which product actions predict conversion, you are scoring activity volume rather than buying intent. A user who logs in 20 times but never completes setup is less likely to convert than a user who logs in 5 times but integrates with their CRM and invites 3 colleagues. Research from PLG companies shows that activation definitions that track setup, aha, and habit moments strongly correlate with mid-term retention and monetization [5].

*Key insight:*

> The actions that appear consistently in converted users but rarely in churned users are your PQL signals. If your baseline trial conversion is 2% and users who integrate 2+ tools convert at 10%, that 5x lift is your scoring signal [6].

*Examples:*

| Context | Example |
|---------|---------|
| Project management tool | Activation = created a project, added 3+ tasks, invited a teammate. Users who hit all 3 in week 1 convert at 4x the base rate |
| Analytics platform | Activation = connected a data source, built a dashboard, scheduled a report. Users completing integration in first 3 days convert at 3x |
| Communication tool | Activation = sent 10+ messages, created a channel, added 2+ members. Team usage signals predict expansion deals |

### Score Decay and Recency Weighting

*What is it?*

Score decay is the systematic reduction of a lead's behavioral score over time when they become inactive. Without decay, scores accumulate indefinitely -- a lead who was highly active 6 months ago but has not logged in since would still appear as a hot PQL. Decay ensures scores reflect current intent. Recency weighting is the complementary practice of assigning higher point values to recent actions vs. older ones [7].

*Why does it matter?*

Static scoring without decay is the second most common failure mode in lead scoring implementations (after overweighting demographics) [8]. A pricing page visit from yesterday is far more predictive of purchase intent than the same visit 90 days ago. Companies that implement 30-day decay rules and recency bonuses report cleaner pipelines and higher PQL-to-opportunity conversion because sales teams contact leads with genuine current intent rather than stale historical activity [7].

*Common misunderstandings:*

- **Misconception:** Decay should apply to all score types equally.
  **Reality:** Fit scores should not decay -- a company's industry and size do not change. Only behavioral scores decay because they reflect time-sensitive intent signals.

- **Misconception:** Aggressive decay (e.g., halving every 7 days) keeps the pipeline freshest.
  **Reality:** Decay rate should match your typical sales cycle. If your average deal takes 45 days, a 7-day half-life will zero out leads before sales can reach them. Match decay to cycle length: 30-day decay for short cycles, 60-90 day decay for enterprise.

---

## 2) Decision Frameworks

### Approach Selection Matrix

| Situation | Recommended Approach | Why |
|-----------|---------------------|-----|
| Free trial with 14-30 day limit, &gt; 100 trials/month | Behavioral-heavy scoring (70% behavior, 30% fit) | High volume, time-limited urgency -- product signals are the primary differentiator |
| Freemium with unlimited free tier, self-serve upgrade | Activation milestone scoring with engagement velocity | No time pressure, so velocity of adoption and depth of usage matter more than any single action |
| Hybrid PLG + sales-assisted with &lt; 50 trials/month | Balanced fit + behavior (50/50) with manual PQL review | Low volume allows human review; fit matters more because each lead is higher value |
| Enterprise PLG with long evaluation cycles (60+ days) | Extended decay windows (90-day) with account-level scoring | Individual user scores miss the picture; aggregate account activity across multiple users matters |
| Early-stage company with &lt; 6 months of conversion data | Simplified scoring (3-5 criteria) with monthly recalibration | Not enough historical data to validate complex models; start simple, iterate with data |

### Scoping Factors

**1. Trial Model (Free Trial vs. Freemium vs. Reverse Trial)**

- Free trial with time limit --> Score urgency signals heavily (pricing page views in final 3 days, feature usage acceleration). Decay should be aggressive post-trial-expiration.
- Freemium with unlimited access --> Score depth of usage and expansion signals (hitting usage limits, exploring premium features). Decay can be slower since there is no expiration forcing action.
- Reverse trial (full features then downgrade) --> Score feature attachment during trial period. Users who heavily use premium features then get downgraded are high-intent PQLs.

**2. Data Maturity (Product Analytics Coverage)**

- Full event tracking (Segment/Amplitude with 50+ events tracked) --> Build granular behavioral scoring with feature-level signals, session tracking, and multi-event sequences.
- Partial tracking (basic page views + key actions only) --> Focus on the 5-8 most predictive actions. Do not score what you cannot measure reliably.
- Minimal tracking (login/signup events only) --> Start with fit-heavy scoring (70% fit, 30% behavior on login frequency alone). Prioritize instrumenting product analytics before building behavioral scoring.

**3. Sales Cycle Length**

- &lt; 30 days --> Decay at 14-day intervals. Engagement velocity bonuses for actions within 48 hours. PQL notifications should trigger same-day outreach.
- 30-90 days --> Decay at 30-day intervals. Score multi-session engagement patterns. Allow for evaluation-period behaviors (comparison pages, security docs).
- 90+ days --> Decay at 60-90 day intervals. Score at the account level (aggregate multiple users). Track champion identification signals (admin actions, org-wide rollout).

**4. Lead Volume**

- High volume (500+ trials/month) --> Automated PQL routing with strict thresholds. No manual review. Invest in score calibration.
- Medium volume (50-500/month) --> Automated scoring with manual PQL validation by SDR team during initial rollout. Calibrate thresholds weekly.
- Low volume (&lt; 50/month) --> Semi-manual scoring acceptable. Sales can review all leads with score as a prioritization input rather than hard threshold.

### Behavioral-Heavy Approach (Recommended for Most PLG)

*Best for:*
- Companies with 100+ free trial signups per month
- Products with measurable activation milestones
- Teams where product analytics are already instrumented (Segment, Amplitude, Mixpanel)
- Short to medium sales cycles (&lt; 60 days)

*Not recommended for:*
- Companies with fewer than 6 months of conversion data
- Products where free trial usage does not correlate with paid conversion (e.g., the trial is too limited to demonstrate value)
- Environments where product analytics are not yet instrumented

*Key differences from standard MQL scoring:*

| Aspect | Traditional MQL Scoring | Product-Led PQL Scoring |
|--------|------------------------|------------------------|
| Primary signals | Content downloads, email opens, webinar attendance | Feature adoption, usage frequency, collaboration actions |
| Score weighting | 60-70% marketing engagement, 30-40% fit | 60-70% product behavior, 30-40% fit |
| Decay model | 30-day activity decay on marketing actions | 14-30 day decay on product usage, velocity bonuses for concentrated activity |
| Threshold trigger | Score &gt; X triggers MQL status and SDR outreach | Dual threshold (fit &gt; Y AND behavior &gt; Z) triggers PQL status and rep notification |
| Negative scoring | Unsubscribes, bounce-backs | Inactivity (no login for 14+ days), downgrade from premium trial features |

### Fit-Balanced Approach

*Best for:*
- Enterprise PLG with high ACV ($50K+)
- Products selling to specific verticals where ICP fit is a strong predictor
- Companies with limited product analytics data
- Hybrid sales-led + PLG motions where marketing touches still matter

*Not recommended for:*
- High-volume self-serve products (ACV &lt; $5K) where fit filtering is too restrictive
- Products where anyone can derive value regardless of company size/industry

*Key differences from behavioral-heavy:*

| Aspect | Behavioral-Heavy | Fit-Balanced |
|--------|-----------------|--------------|
| Fit : Behavior ratio | 30:70 | 50:50 |
| PQL threshold logic | Behavioral score drives qualification, fit is a floor | Both scores must exceed independent thresholds |
| Sales involvement | Automated routing, sales trusts the score | Score is input to sales judgment, not automatic routing |
| Best conversion signal | Activation milestone completion | ICP match + any product engagement |

---

## 3) Benchmarks & Standards

### How to Use Benchmarks

Benchmarks are guidelines, not rules. Always:
1. Start with benchmark as baseline
2. Adjust based on client-specific data
3. Validate against their actual numbers when available
4. Document deviations and rationale

### PQL Conversion Rates

| Metric | Low | Typical | High | Notes |
|--------|-----|---------|------|-------|
| PQL-to-Opportunity rate | 15% | 25-30% | 40%+ | Below 15% = PQL definition too loose. Above 40% = definition too tight, missing good leads [1][6] |
| PQL-to-Closed Won rate | 8% | 15-20% | 30%+ | Depends on ACV and sales cycle length |
| MQL-to-Opportunity rate (for comparison) | 5% | 10-13% | 20% | Traditional marketing-scored leads [2] |
| Trial-to-Paid (no scoring, baseline) | 2% | 5-8% | 15% | This is the baseline you are improving from [9] |
| PQL vs. MQL conversion lift | 1.5x | 2-3x | 5x | The core ROI metric for this project [1] |

**Source:** ProductLed, FirstPageSage, Pocus PLG benchmarks, and aggregated B2B SaaS funnel data [1][2][6][9].

**Interpretation:**
- **Below low:** PQL threshold is too permissive, or behavioral signals are not truly predictive. Revisit which product actions correlate with conversion.
- **Above high:** Threshold may be too restrictive. You are likely missing good leads who would convert with sales outreach. Loosen the behavioral score requirement by 10-15 points and monitor.

### Scoring Weight Distribution

| Metric | Low | Typical | High | Notes |
|--------|-----|---------|------|-------|
| Behavioral score weight (% of total) | 50% | 60-70% | 80% | For PLG motions, product signals should always outweigh fit [3][10] |
| Fit score weight (% of total) | 20% | 30-40% | 50% | Higher weight for enterprise or vertical-specific products |
| Negative scoring impact (% of total possible) | 5% | 10-15% | 25% | At minimum, competitors and personal emails should subtract points |
| Engagement velocity bonus (% of base action score) | 0% | 25-50% | 100% | Bonus for concentrated activity within 48-hour window |

**Source:** Clearbit, HubSpot, Ortto lead scoring frameworks [3][10][11].

### Score Decay Timing

| Metric | Low | Typical | High | Notes |
|--------|-----|---------|------|-------|
| Decay start (days of inactivity) | 7 | 14-21 | 30 | Match to sales cycle length |
| Decay rate per period | 5% | 10-15 pts/30 days | 25%/month | Aggressive = fast cycle, gentle = long cycle [7] |
| Score floor (minimum after decay) | 0 | 5-10 | 20 | Prevents scores going negative; retains that "they did try the product" signal |
| Recency bonus window | 24 hrs | 48-72 hrs | 7 days | Actions within this window get multiplied |

**Source:** HubSpot scoring documentation, Ortto, WorkNet lead scoring best practices [7][11].

### Quick Reference Thresholds

| Question | Good | Warning | Red Flag |
|----------|------|---------|----------|
| What % of PQLs should sales accept? | &gt; 70% | 50-70% | &lt; 50% (threshold too low) |
| What % of closed-won came through PQL path? | &gt; 40% | 20-40% | &lt; 20% (model not capturing real buyers) |
| How many scoring criteria in the model? | 15-25 | 10-15 or 25-35 | &lt; 10 (too simple) or &gt; 35 (overcomplicated) |
| How often should the model be recalibrated? | Monthly for first 90 days, quarterly after | Quarterly | Annually or never |
| What % of leads should reach PQL status? | 5-15% of total trial signups | 15-25% | &gt; 25% (too loose) or &lt; 3% (too tight) |

---

## 4) Calculations & Scoring

### Formula Quick Reference

| Calculation | Formula | Example |
|-------------|---------|---------|
| Total Lead Score | `Fit Score + Behavioral Score` | 30 (fit) + 55 (behavior) = 85 (PQL) |
| Behavioral Score | `Sum(Action Points) + Velocity Bonus - Decay Penalty` | 45 + 15 - 5 = 55 |
| Decay Penalty | `Points per Period x Inactive Periods` | 10 pts/30 days x 0.5 periods = 5 |
| Velocity Bonus | `Base Points x Velocity Multiplier` (if N+ actions in 48 hrs) | 30 x 0.5 = +15 bonus |
| PQL Conversion Lift | `PQL Conv Rate / Non-PQL Conv Rate` | 25% / 8% = 3.1x lift |

### Fit Scoring Rubric

**Purpose:** Quantifies how well the lead's company and role match the Ideal Customer Profile. Fit score does not decay -- company attributes are stable.

**Fit Score Rubric (0-50 points):**

| Criterion | Points | Threshold |
|-----------|--------|-----------|
| Company size (employees) | +15 | ICP range (e.g., 50-500 employees) = +15, adjacent range (25-49 or 501-1000) = +8, outside = 0 |
| Industry match | +10 | Target industry = +10, adjacent industry = +5, non-target = 0 |
| Job title / seniority | +10 | VP/Director/C-level = +10, Manager = +6, Individual contributor = +2 |
| Tech stack fit | +8 | Uses complementary tools (e.g., Salesforce + Segment) = +8, partial match = +4 |
| Geography | +7 | Target region = +7, secondary region = +4, non-target = 0 |
| **Negative: Disqualifiers** | -15 to -30 | Competitor employee = -30, personal email (gmail/yahoo) = -15, student/academic = -10 |
| **Total possible** | **50** | (before negative deductions) |

**Tier Thresholds:**
- Strong fit: 35+ points
- Moderate fit: 20-34 points
- Weak fit: Below 20 points (consider excluding from PQL routing regardless of behavioral score)

### Behavioral Scoring Rubric

**Purpose:** Quantifies product engagement and buying intent based on in-product actions. This score decays over time.

**Behavioral Score Rubric (0-100 points):**

| Criterion | Points | Threshold |
|-----------|--------|-----------|
| **Activation Milestones** | | |
| Completed onboarding / setup wizard | +15 | Full completion = +15, partial (&gt;50%) = +8 |
| Used core feature 3+ times | +20 | 3+ uses in first 14 days. This is the single most predictive action for most PLG products |
| Integrated with external tool (CRM, Slack, etc.) | +15 | Any integration connected = +15. Integration signals organizational commitment |
| Invited teammate(s) | +15 | 1 invite = +10, 2+ invites = +15. Collaboration is the strongest expansion predictor |
| **High-Intent Actions** | | |
| Visited pricing page (while logged in) | +10 | Logged-in pricing view = +10, anonymous = +3. Logged-in views are 3x more predictive |
| Started upgrade/checkout flow | +15 | Initiated but did not complete purchase -- high buying intent signal |
| Used premium/enterprise-only feature (during trial) | +8 | Signals need for paid tier capabilities |
| Exported data or generated a report | +5 | Suggests the product is delivering business value |
| **Engagement Frequency** | | |
| Login frequency (5+ in first 7 days) | +10 | 5+ logins in week 1 = +10, 3-4 = +5, 1-2 = +2 |
| Session depth (3+ features per session) | +5 | Using breadth of product features = deeper evaluation |
| **Negative Scoring** | | |
| No login for 14+ days | -10 | Per 14-day period of inactivity |
| Unsubscribed from product emails | -5 | Signals disengagement |
| Downgraded from premium trial features | -8 | Actively chose to reduce usage |
| **Velocity Bonus** | | |
| 5+ key actions in 48 hours | +25 | Concentrated activity burst signals active evaluation. Apply once per 48-hour window |
| **Total possible** | **~100** | (excluding velocity; with velocity can exceed 100 temporarily before decay) |

**Tier Thresholds:**
- High intent: 60+ points
- Medium intent: 30-59 points
- Low intent: Below 30 points

### Combined Score and PQL Qualification

**Formula:**
```
Total Lead Score = Fit Score + Behavioral Score
```

**PQL Qualification Logic (AND conditions, not just total):**
```
PQL = TRUE if ALL of the following:
  - Total Lead Score >= 80
  - Fit Score >= 15 (minimum fit floor -- excludes completely wrong-fit leads)
  - Behavioral Score >= 40 (minimum behavior floor -- excludes passive leads)
```

**Worked Example:**

*Scenario: SaaS analytics company, free trial model, ICP = mid-market tech companies (50-500 employees)*

```
Lead: VP Marketing at a 120-employee SaaS company using Salesforce

Fit Score:
- Company size (120 employees, in 50-500 range)     = +15
- Industry (SaaS = target industry)                  = +10
- Job title (VP Marketing = VP/Director level)       = +10
- Tech stack (uses Salesforce = complementary)       = +8
- Geography (US = target region)                     = +7
- Fit Score Total                                    = 50

Behavioral Score:
- Completed onboarding                              = +15
- Used core dashboard feature 5 times in week 1     = +20
- Connected Salesforce integration                   = +15
- Invited 2 teammates                               = +15
- Visited pricing page while logged in              = +10
- 6 key actions in 48 hours (velocity bonus)        = +25
- No decay (all actions within last 7 days)          = 0
- Behavioral Score Total                             = 100

Total Lead Score = 50 + 100 = 150
PQL Check: Total >= 80? YES. Fit >= 15? YES. Behavior >= 40? YES.
Result: PQL = TRUE. Route to sales with full context.
```

**Validation:**
- Total Lead Score should typically range from 0 to 150
- If more than 25% of trial users score above PQL threshold, the threshold is too low
- If fewer than 3% score above threshold, it is too tight
- Run the scoring model retroactively against 6 months of historical data before going live

### Decay Calculation

**Formula:**
```
Adjusted Behavioral Score = Raw Behavioral Score - (Decay Rate x Inactive Periods)

Where:
- Decay Rate = points subtracted per decay period (typical: 10 points per 30-day period)
- Inactive Periods = number of full decay periods since last product activity
- Score Floor = minimum score (typical: 0-5 points)
```

**Worked Example:**

*Scenario: Lead had a Behavioral Score of 70, then went inactive for 75 days*

```
Given:
- Raw Behavioral Score = 70
- Decay Rate = 10 points per 30 days
- Days since last activity = 75 days
- Score Floor = 5

Calculate:
- Inactive Periods = floor(75 / 30) = 2 full periods
- Decay Penalty = 10 x 2 = 20 points
- Adjusted Score = 70 - 20 = 50

Result: Behavioral Score drops from 70 to 50 after 75 days of inactivity.
```

---

## 5) Edge Cases & Deep Dives

### Edge Case 1: New PLG Company with &lt; 6 Months of Conversion Data

*Scenario:*

A company launches a free trial and wants lead scoring from day one, but has fewer than 100 closed-won deals to analyze for conversion patterns. Without historical data, you cannot empirically determine which activation milestones correlate with buying intent.

*Approach:*

1. Start with a simplified scoring model using only 5-8 criteria based on PLG best practices (onboarding completion, core feature usage, team invites, pricing page visits)
2. Assign equal weights initially -- do not pretend to know which signals are strongest
3. Set a conservative PQL threshold that routes approximately 10% of trial users to sales
4. Track every PQL outcome (accepted/rejected by sales, converted/lost) in a dedicated tracking sheet
5. After 90 days, analyze conversion rates by score bucket and recalibrate weights based on actual data

*Fallback assumptions:*

| Missing Data | Use This Instead | Source |
|--------------|------------------|--------|
| Conversion correlation by feature | Weight onboarding completion and team invites highest (these are universal PLG signals) | ProductLed and Pocus benchmarks [5][6] |
| PQL threshold | Start at top 10% of scoring distribution | Industry standard starting point |
| Decay rate | 10 points per 30 days | Median B2B SaaS sales cycle length [7] |

*Key validation:* After 90 days, the top-scoring 20% of leads should convert at 2x+ the rate of the bottom 80%.

### Edge Case 2: Multi-Product Company with Separate Trials

*Scenario:*

A company offers multiple separate products, each with its own free trial. A single prospect may be trialing multiple products simultaneously, or a company may have different users trialing different products.

*Approach:*

1. Build product-specific behavioral scoring rubrics (each product gets its own activation milestones and scoring criteria)
2. Calculate per-product behavioral scores independently
3. Use the highest individual product score as the primary behavioral score (do not add them -- a user with 30 points in CRM and 30 points in Analytics is not the same as 60 points in CRM)
4. Add a cross-product bonus (+10-15 points) when a lead actively uses 2+ products, as this signals deeper organizational evaluation
5. Maintain a single fit score at the account level since firmographic data does not change by product

*Key validation:* Multi-product PQLs should convert at a higher rate than single-product PQLs. If they do not, the cross-product bonus is not adding signal.

### Edge Case 3: Freemium vs. Free Trial Scoring Differences

*Scenario:*

The client operates a freemium model (unlimited free tier with feature-gated upgrades) rather than a time-limited free trial. Users may remain on the free tier for months or years, accumulating high behavioral scores without buying intent.

*Approach:*

1. Add upgrade-specific signals to behavioral scoring: hitting usage limits, attempting to use premium features, visiting pricing page, and downloading invoicing/procurement docs
2. Weight expansion signals (hitting limits, premium feature attempts) 2x higher than standard usage signals
3. Implement a "free tier ceiling" -- cap behavioral scores for users who have been on free tier &gt; 90 days without any upgrade signals at 40 points (below PQL threshold)
4. Focus on velocity rather than accumulation: score rate-of-change in usage, not total lifetime usage
5. Track "trigger events" separately: company funding round, new executive hire, or company size growth that might shift buying timeline

*Key validation:* Freemium PQL conversion rates should still meet the 25-30% benchmark. If conversion is below 15%, the model is scoring free-tier loyalty rather than upgrade intent.

### Edge Case 4: Sales Team Rejects PQLs / Trust Breakdown

*Scenario:*

After launching the scoring model, sales reps report that PQLs are "no better than regular leads" and stop following up on them. PQL-to-opportunity conversion drops below 15%.

*Approach:*

1. Pull data immediately: compare conversion rates of PQLs that sales contacted vs. PQLs they ignored. If contacted PQLs convert at 20%+ but ignored PQLs are dragging the average down, this is an adoption problem, not a model problem.
2. If conversion of contacted PQLs is also low (&lt; 15%), pull a sample of 20 rejected PQLs and review their scoring breakdown with Sales leadership. Identify which specific scoring signals are not mapping to real buying intent.
3. Adjust the threshold or criteria based on findings -- tighten the PQL threshold, add negative scoring for signals sales flagged, or increase the fit score floor.
4. Re-pilot with 2-3 reps who are willing to work the system. Show them results after 2 weeks.

*Key validation:* Sales acceptance rate of PQLs should be above 70%. If below 50% after recalibration, the scoring model needs a fundamental rework.

### Edge Case 5: Data Quality and Missing Product Events

*Scenario:*

The product analytics platform only tracks 10-15 events (compared to the 30-50 needed for granular behavioral scoring). Key activation milestones cannot be measured because the event is not instrumented.

*Approach:*

1. Audit available events and map them to scoring criteria. Even 10 events can produce a functional (if less precise) scoring model.
2. Identify the 3-5 highest-value missing events and create a prioritized instrumentation request for the engineering team
3. Build the initial model on available data with heavier fit weighting (50/50 instead of 30/70) to compensate for thinner behavioral signals
4. Use proxy signals where direct events are missing: login frequency as proxy for feature usage, session duration as proxy for engagement depth, page views of in-app sections as proxy for feature adoption
5. Plan a model v2 for 60 days after additional events are instrumented

*Fallback assumptions:*

| Missing Data | Use This Instead | Source |
|--------------|------------------|--------|
| Feature usage count | Login frequency (5+ per week = high engagement) | Proxy signal, less precise |
| Integration completion | Time-in-product per session (&gt; 15 min = deep usage) | Session duration as engagement proxy |
| Team invite events | Number of users from same email domain on free tier | Account-level collaboration signal |

*Key validation:* Track the gap between proxy-based scores and actual outcomes. If proxy signals prove poor predictors (&lt; 1.5x conversion lift vs. unscored leads), the model needs the instrumented events to function.

---

## References

[1] [ProductLed - Product-Led Growth Benchmarks](https://productled.com/blog/product-led-growth-benchmarks)
[2] [FirstPageSage - MQL to SQL Conversion Rate By Industry: 2025 Report](https://firstpagesage.com/seo-blog/mql-to-sql-conversion-rate-by-industry/)
[3] [Clearbit - Lead Scoring Basics](https://clearbit.com/resources/books/lead-qualification/lead-scoring-basics)
[4] [Etumos - Demographic Scores and Behavior Scores](https://etumos.com/marketing-automation/take-behavior-lead-scoring-and-demographic-lead-scoring-next-level/)
[5] [FocusedChaos - 9 Early Metrics That Predict PLG Success](https://www.focusedchaos.co/p/9-early-metrics-that-predict-plg)
[6] [Pocus - Product-Led Growth Metrics to Measure](https://www.pocus.com/blog/product-led-growth-metrics-to-measure)
[7] [WorkNet - 8 Lead Scoring Best Practices for SaaS in 2025](https://www.worknet.ai/blog/lead-scoring-best-practices)
[8] [Vereigen Media - B2B Lead Scoring Mistakes to Avoid](https://vereigenmedia.com/how-to-avoid-the-most-common-b2b-lead-scoring-mistakes/)
[9] [The Digital Bloom - 2025 B2B SaaS Funnel Benchmarks](https://thedigitalbloom.com/learn/pipeline-performance-benchmarks-2025/)
[10] [Ortto - Product-Led Approach to Lead Scoring for SaaS](https://ortto.com/learn/product-led-approach-building-a-lead-scoring-framework-for-saas-marketing/)
[11] [HubSpot - Understand the Lead Scoring Tool](https://knowledge.hubspot.com/scoring/understand-the-lead-scoring-tool)
