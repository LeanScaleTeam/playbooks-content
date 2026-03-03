# Customer Health Model — Methodology

This document covers the core concepts, frameworks, and calculations behind the Customer Health Model. It provides the methodological foundation — the "how it works" behind the execution steps.

---

## 1) Core Concepts

### Multi-Dimensional Health Scoring

*What is it?*

A multi-dimensional health score combines signals from several distinct categories -- product usage, engagement, support activity, financial behavior, and CSM sentiment -- into a single composite number (typically 0-100) that indicates how likely a customer is to renew, expand, or churn. Each dimension captures a different facet of the customer relationship that, alone, would give an incomplete picture.

*Why does it matter?*

Single-metric approaches miss critical signals. A customer with high product usage but escalating support tickets looks "healthy" if you only track logins. Companies integrating at least three data sources into their health models see 32% higher prediction accuracy than single-source approaches [1]. The multi-dimensional approach forces your CS team to define what "healthy" actually means across every touchpoint.

*Key insight:*

> No single metric predicts churn. The accounts that surprise you -- the ones that churn despite high usage or renew despite low engagement -- are the ones where your model was only looking at one dimension. Health scoring works because it triangulates across signals that individually lie.

*Examples:*

| Context | Example |
|---------|---------|
| High usage, low engagement | Customer has strong DAU but has not attended a QBR in two quarters and the executive sponsor is unresponsive. Score drops because engagement dimension pulls overall health down despite strong product metrics. |
| Low usage, high engagement | Customer's power users log in infrequently (monthly cadence) but attend every QBR, respond to emails within hours, and actively participate in the product roadmap. Engagement offsets usage concerns. |
| All green except support | Product usage and engagement are strong but support ticket volume tripled in 30 days with two escalations. Support dimension drags the composite score into Yellow, triggering proactive outreach. |

### Leading vs. Lagging Indicators in Health Scoring

*What is it?*

Leading indicators are behaviors that predict future outcomes (login frequency declining over 30 days, missed QBR). Lagging indicators confirm what already happened (churn event, renewal, NPS score submitted). A health score should be constructed primarily from leading indicators so CSMs have time to intervene.

*Why does it matter?*

If your health score is built on lagging indicators, it becomes a rearview mirror -- it tells you what already went wrong, not what is about to. The goal of a health model is proactive intervention, which requires signals that precede the outcome by 30-90 days. The best churn prediction models achieve 75-82% accuracy at a 90-day prediction horizon [2], but only when built on forward-looking signals.

*The Framework:*

```
LEADING (Action Window)               LAGGING (Confirmation)
------------------------------        -------------------------
Login frequency declining             Churn event
Feature adoption stalling             Non-renewal
QBR attendance dropping               Downgrade request
Support ticket escalations            NPS score submitted
Champion job change detected          Contract cancellation
Payment delays starting               Revenue lost
```

*Common misunderstandings:*

- **Misconception:** NPS is a good health score input because it measures sentiment.
  **Reality:** NPS is a lagging indicator -- by the time a customer submits a low score, the damage is done. Use NPS as a validation data point for your model, not as a primary input. CSM-reported sentiment captured during regular touchpoints is a better leading indicator.

- **Misconception:** More metrics always produce a better health score.
  **Reality:** The most predictive health scores use 5-10 well-chosen metrics [3]. Models with 15+ inputs become opaque, CSMs cannot explain what drives a score, and they stop trusting it. Start with the five metrics most correlated with your historical churn data, then add incrementally.

### Signal Decay and Lookback Windows

*What is it?*

Signal decay is the principle that older data is less predictive than recent data. A lookback window defines the time period over which a metric is measured (e.g., trailing 30 days of login frequency vs. trailing 90 days). Different metrics have different optimal lookback windows based on their natural cadence and volatility.

*Why does it matter?*

Using the wrong lookback window distorts your score. A 7-day window on product usage creates false alarms every holiday week. A 180-day window on support tickets buries a sudden spike that started last week. Each metric needs a lookback window calibrated to its natural cycle and the speed at which it signals risk.

*Key insight:*

> The right lookback window depends on the metric's cadence, not your reporting cadence. Match the window to how often the behavior naturally occurs: daily-use features get 14-30 day windows; quarterly events (QBRs, business reviews) get 90-180 day windows.

*Examples:*

| Metric | Recommended Lookback | Why |
|--------|---------------------|-----|
| Daily Active Users / Login Frequency | 14-30 days | Usage patterns shift weekly; 30 days smooths noise while catching real decline |
| Support Ticket Volume | 30 days | Spikes can be short-lived; 30 days separates a bad week from a trend |
| Feature Adoption Rate | 60-90 days | New features take time to adopt; shorter windows penalize accounts still onboarding a feature |
| QBR Attendance | 90-180 days | QBRs happen quarterly; a 30-day window would show 0 attendance for most accounts most of the time |
| Payment Timeliness | 90 days | Payment cycles are monthly or quarterly; need at least 2-3 cycles to see a pattern |
| CSM Sentiment | Current + 30-day trend | Sentiment is point-in-time; compare current to 30-day-ago snapshot to detect trajectory |

### The CSM Override Principle

*What is it?*

A CSM override allows a Customer Success Manager to manually adjust an account's health score (or category) based on contextual information that the automated model cannot capture -- such as a known leadership change, an upcoming product launch that explains temporary usage dips, or a verbal commitment to expand.

*Why does it matter?*

Automated scores are built on patterns, not context. A CSM who just had a call with the champion knows things the data does not. Without an override mechanism, CSMs lose trust in the score ("it says Red but I know they are fine") and stop using it entirely. The override bridges the gap between quantitative signals and human judgment.

*Common misunderstandings:*

- **Misconception:** Overrides undermine the objectivity of the health score.
  **Reality:** Overrides add a dimension the model cannot capture. The key is governance: require a reason for every override, time-limit overrides (e.g., expires in 30 days), and audit override accuracy quarterly. If a CSM overrides to Green and the account churns, that is a coaching signal.

- **Misconception:** CSM sentiment should replace automated scoring for key accounts.
  **Reality:** Sentiment is one input, not a replacement. Gainsight's research shows that product usage is not necessarily the most important churn predictor for every segment [4], but neither is sentiment alone. The best models balance both -- use automated signals as the baseline and sentiment as a modifier.

---

## 2) Decision Frameworks

### Approach Selection Matrix

| Situation | Recommended Approach | Why |
|-----------|---------------------|-----|
| First health score build, limited data (&lt;12 months), &lt;200 accounts | Simple Weighted Average (5-7 metrics, uniform-ish weights) | Low complexity, fast to validate, builds organizational trust before sophistication |
| Established CS org, 12+ months data, 200+ accounts, CS platform in place | Data-Informed Weighted Composite (weights derived from churn correlation analysis) | Enough historical data to statistically validate which metrics actually predict outcomes |
| PLG motion with strong product analytics, high account volume (1000+) | Product-Led Health Score (usage-heavy weighting, automated triggers) | Product signals are abundant and timely; engagement signals are sparse for self-serve accounts |
| Enterprise-heavy book, low volume (&lt;100 accounts), relationship-driven | Relationship-Led Health Score (engagement + sentiment heavy, usage as secondary) | Enterprise accounts have low-frequency usage patterns; relationship signals are more predictive |
| Multi-product or multi-BU company | Segment-Specific Composite (separate models per product/segment) | Usage norms differ so dramatically across products that a single model produces misleading scores |

### Scoping Factors

**1. Data Maturity**

- Less than 6 months of customer data --> Cannot validate a model against historical churn. Build a provisional score using industry benchmarks for thresholds, plan to recalibrate at 6 months.
- 6-12 months of data --> Enough to run basic correlation analysis. Build model and validate against known churn events, but acknowledge small sample size.
- 12+ months of data --> Full correlation analysis possible. Run retrospective scoring against churned accounts to validate model accuracy before launch.

**2. Account Volume**

- Under 50 accounts --> Health scoring may not be worth automating. CSMs likely know every account personally. Consider a simple Red/Yellow/Green tracker in a spreadsheet before investing in a platform-based model.
- 50-500 accounts --> Sweet spot for a platform-based health score. Enough accounts that CSMs cannot hold every detail in memory, but manageable enough for manual override governance.
- 500+ accounts --> Automation is essential. Consider automated intervention triggers (not just visibility), segment-specific models, and exception-based workflows where CSMs only engage accounts crossing thresholds.

**3. CS Platform Availability**

- No CS platform --> Build in CRM with formula fields and reports. Limited to metrics available in CRM. Plan for platform adoption as a follow-on project.
- CS platform in place (Gainsight, ChurnZero, Vitally, Totango, Catalyst, Planhat) --> Full health score build with automated data ingestion, configurable weights, and dashboard reporting.
- Product analytics platform only (Amplitude, Mixpanel, Pendo) --> Can build a usage-heavy health score; pair with CRM data for engagement and financial dimensions via integration.

**4. Motion Type**

- Sales-led / high-touch --> Weight engagement and sentiment higher (combined 40-50%). Product usage matters but CSM relationship is the primary retention driver.
- Product-led / low-touch --> Weight product usage higher (50-60%). Many accounts have no CSM relationship; usage signals are the most timely and actionable.
- Hybrid --> Build segment-specific weights. PLG accounts get usage-heavy scoring; enterprise accounts get engagement-heavy scoring.

### Simple Weighted Average Approach

*Best for:*
- First-time health score implementations
- Teams with limited data science resources
- Organizations building CS discipline for the first time
- Pilot programs testing the concept before investing in a platform

*Not recommended for:*
- Companies with 1000+ accounts needing automated interventions
- Organizations with strong data science teams who can build predictive models
- Multi-product companies where a single weight set produces misleading scores

*Key differences from standard:*

| Aspect | Data-Informed Composite | Simple Weighted Average |
|--------|------------------------|------------------------|
| Weight assignment | Statistical correlation with churn outcomes | SME judgment + best-practice ranges |
| Validation | Retrospective backtest against churned accounts | CSM gut-check ("does this feel right?") |
| Recalibration | Quarterly statistical review | Quarterly team discussion |
| Time to launch | 4-6 weeks (requires data analysis) | 1-2 weeks (faster, based on assumptions) |

### Data-Informed Weighted Composite Approach

*Best for:*
- Organizations with 12+ months of churn data and reason codes
- Teams with RevOps or data analyst support
- Companies scaling past 200 accounts where gut feel no longer works

*Not recommended for:*
- New companies without historical churn data
- Organizations where churn reasons are not documented
- Teams without analyst capacity to run correlation analysis

*Key differences from standard:*

| Aspect | Simple Weighted Average | Data-Informed Composite |
|--------|------------------------|------------------------|
| Weight source | Industry best practices | Your company's actual churn correlation data |
| Accuracy at launch | Moderate (~60-70%) | Higher (~70-82%) [2] |
| Maintenance burden | Low (adjust annually) | Medium (quarterly statistical review) |
| Explainability | Easy ("we picked these based on best practices") | Harder ("the math says support tickets matter 2x more than we expected") |

---

## 3) Benchmarks & Standards

### How to Use Benchmarks

*Benchmarks are guidelines, not rules. Always:*
1. Start with benchmark as baseline
2. Adjust based on client-specific data
3. Validate against their actual numbers when available
4. Document deviations and rationale

### B2B SaaS Churn Rate Benchmarks

| Metric | SMB | Mid-Market | Enterprise | Notes |
|--------|-----|------------|------------|-------|
| Monthly logo churn | 3-5% | 1.5-3% | 1-2% | Vitally 2025 SaaS Churn Benchmarks [5] |
| Annual logo churn | 31-46% | 17-31% | 10-22% | Derived from monthly; median annual logo churn across all segments is 13% per KBCM survey [6] |
| Annual revenue churn | 10-15% | 5-7% | 2-5% | Smaller companies face higher revenue churn [6] |
| Net revenue retention | 90-100% | 100-110% | 110-130% | Top performers push NRR past 120% through expansion revenue [7] |

**Source:** Vitally 2025 SaaS Churn Benchmarks [5], KBCM SaaS Survey [6], Maxio 2025 SaaS Benchmarks Report [7]

**Interpretation:**
- **Below benchmark:** Client's churn is better than average -- health scoring can still add value for early warning and expansion identification
- **Above benchmark:** Health scoring is urgent. Every point of churn prevented has direct ARR impact. Prioritize the model build.

### Health Score Model Accuracy Benchmarks

| Metric | Minimum Viable | Good | Excellent | Notes |
|--------|---------------|------|-----------|-------|
| Overall accuracy (correct Red/Yellow/Green classification) | 60% | 70% | 80%+ | Validated against 6+ months of historical outcomes |
| False negative rate (churned accounts scored Green) | &lt;20% | &lt;10% | &lt;5% | Most dangerous error -- missed churn signals |
| False positive rate (healthy accounts scored Red) | &lt;30% | &lt;20% | &lt;10% | Creates alert fatigue if too high |
| Prediction horizon | 30 days | 60 days | 90 days | Best models achieve 75-82% accuracy at 90-day horizon [2] |

**Source:** FunnelStory churn prediction research [2], industry practitioner data

**Interpretation:**
- **Below minimum viable:** Model needs recalibration. Check if weights reflect actual churn drivers or are based on assumptions. Run fresh correlation analysis.
- **Above excellent:** Validate that the model is not overfitting. Check if a few accounts are skewing results. Cross-validate across customer segments.

### Product Usage Benchmarks by Segment

| Metric | SMB (Expected Range) | Mid-Market (Expected Range) | Enterprise (Expected Range) |
|--------|---------------------|---------------------------|---------------------------|
| Weekly Active Users (% of licenses) | 60-80% | 40-60% | 25-45% |
| Login frequency (per user/week) | 4-5x | 2-4x | 1-2x |
| Feature adoption (% of core features used) | 30-50% | 40-60% | 50-70% |
| License utilization (% of seats active) | 70-90% | 50-75% | 40-65% |

**Source:** Industry averages from Gainsight and Vitally customer benchmarks [4][8]

**Interpretation:**
- SMB accounts are expected to have higher per-user engagement but lower feature depth
- Enterprise accounts have lower frequency but deeper feature usage when they do engage
- Using SMB thresholds for Enterprise (or vice versa) will produce systematic misclassification

### Quick Reference Thresholds

| Question | Good | Warning | Red Flag |
|----------|------|---------|----------|
| Is the account using the product? | &gt;50% license utilization, weekly logins | 25-50% utilization, biweekly logins | &lt;25% utilization, monthly or less |
| Is the account engaged with us? | QBR attended, email response &lt;48h | Missed 1 QBR, response &gt;48h | Missed 2+ QBRs, no response in 2 weeks |
| Is support a concern? | &lt;3 tickets/month, no escalations | 3-6 tickets/month, 1 escalation | &gt;6 tickets/month, 2+ escalations |
| Is the financial relationship healthy? | Pays on time, expansion in pipeline | 1 late payment, no expansion | 2+ late payments, downgrade discussion |
| Does the CSM feel good about this account? | Confident in renewal, champion engaged | Some concerns, champion distracted | Worried, champion left or disengaged |

---

## 4) Calculations & Scoring

### Formula Quick Reference

| Calculation | Formula | Example |
|-------------|---------|---------|
| Weighted Composite Score | `Sum(Metric_i * Weight_i) for i=1 to n` | `(Usage * 0.40) + (Engagement * 0.25) + (Support * 0.20) + (Financial * 0.15) = Score` |
| Metric Normalization (linear) | `Normalized = ((Raw - Min) / (Max - Min)) * 100` | Raw logins = 12, Min = 0, Max = 20: `(12/20)*100 = 60` |
| Inverse Normalization (for "bad" metrics) | `Normalized = (1 - ((Raw - Min) / (Max - Min))) * 100` | 5 support tickets, Min = 0, Max = 10: `(1 - 5/10)*100 = 50` |
| Score Trend (30-day) | `Trend = Current_Score - Score_30_Days_Ago` | Current = 65, 30 days ago = 78: Trend = -13 (declining) |

### Weighted Composite Health Score Calculation

**Formula:**
```
Health_Score = (D_usage * W_usage) + (D_engagement * W_engagement) + (D_support * W_support) + (D_financial * W_financial) + (D_sentiment * W_sentiment)

Where:
- D = Dimension score (0-100, normalized)
- W = Dimension weight (decimal, all weights sum to 1.0)
- Health_Score output range: 0-100
```

**Variables explained:**
- `D_usage` = Product usage dimension score, calculated from login frequency, feature adoption, and license utilization, each normalized to 0-100 and averaged within the dimension
- `D_engagement` = Engagement dimension score, calculated from QBR attendance, email responsiveness, and executive sponsor activity
- `D_support` = Support dimension score, calculated from ticket volume (inverse-normalized), escalation count (inverse-normalized), and resolution satisfaction
- `D_financial` = Financial dimension score, calculated from payment timeliness, expansion history, and renewal timing
- `D_sentiment` = CSM sentiment score, a manual 0-100 input updated at each touchpoint
- `W_*` = Weights assigned per dimension. Common starting points are listed in the Approach Selection Matrix.

**Worked Example:**

*Scenario: Mid-market SaaS customer, 50 licenses, 8 months into contract*

```
Given:
- D_usage = 72 (55% license utilization, 3x weekly logins, 45% feature adoption)
- D_engagement = 58 (attended last QBR, email response avg 72h, exec sponsor missed last 2 meetings)
- D_support = 45 (7 tickets in 30 days, 1 escalation -- inverse normalized)
- D_financial = 85 (pays on time, small expansion 3 months ago)
- D_sentiment = 55 (CSM rates as "some concerns, main contact seems distracted")

Weights (mid-market default):
- W_usage = 0.35
- W_engagement = 0.25
- W_support = 0.20
- W_financial = 0.10
- W_sentiment = 0.10

Calculate:
- (72 * 0.35) = 25.2
- (58 * 0.25) = 14.5
- (45 * 0.20) = 9.0
- (85 * 0.10) = 8.5
- (55 * 0.10) = 5.5

Health_Score = 25.2 + 14.5 + 9.0 + 8.5 + 5.5 = 62.7
```

**Validation:**
- This score (62.7) falls in the Yellow range (41-70) -- needs attention
- The low support score (45) and declining engagement (58) are the primary drivers
- If this were above 85, investigate whether the support dimension is being calculated correctly (7 tickets + 1 escalation should not produce a green-range support score)
- If below 30, check whether all data sources are syncing -- a 0 in any dimension pulls the score down disproportionately

### Metric Normalization

Each raw metric must be converted to a 0-100 scale before applying weights. There are two types:

**Positive Metrics (higher raw = better health):**
```
Normalized_Score = ((Raw_Value - Floor) / (Ceiling - Floor)) * 100

Example: Login frequency
- Raw = 3.5 logins/week
- Floor = 0 (no logins)
- Ceiling = 5 (daily login)
- Normalized = (3.5 / 5) * 100 = 70
```

**Negative Metrics (higher raw = worse health):**
```
Normalized_Score = (1 - ((Raw_Value - Floor) / (Ceiling - Floor))) * 100

Example: Support tickets per month
- Raw = 4 tickets
- Floor = 0 (no tickets)
- Ceiling = 10 (heavy support load)
- Normalized = (1 - (4/10)) * 100 = 60
```

**Setting Floors and Ceilings:**
- Use segment-specific ranges (see Benchmarks section)
- Cap at floor/ceiling: if raw value exceeds ceiling, score = 0 (for negative) or 100 (for positive)
- Review and adjust quarterly as customer behavior shifts

### Scoring Rubrics

**Health Category Rubric:**

| Category | Score Range | Meaning | Expected CSM Action |
|----------|------------|---------|---------------------|
| Green | 71-100 | Healthy. Signals indicate likely renewal. | Identify expansion opportunities. Standard touchpoint cadence. |
| Yellow | 41-70 | Needs attention. One or more dimensions below acceptable range. | Increase touchpoint frequency. Investigate declining dimensions. Schedule proactive outreach. |
| Red | 0-40 | At risk. Multiple signals indicate churn risk. | Immediate intervention. Executive escalation. Develop save plan. |
| Black (optional) | N/A | Insufficient data to score. Account lacks minimum data threshold. | Prioritize data collection. Cannot classify until baseline data exists. |

**Tier Thresholds:**
- Green: 71+ points (renewal expected, expansion possible)
- Yellow: 41-70 points (intervention within 7 business days)
- Red: 0-40 points (intervention within 24-48 hours, escalation path activated)
- Black: Applied when fewer than 3 of 5 dimensions have sufficient data to score

### Default Weight Sets by Segment

| Dimension | Sales-Led / Enterprise | Hybrid / Mid-Market | Product-Led / SMB |
|-----------|----------------------|--------------------|--------------------|
| Product Usage | 0.25 | 0.35 | 0.50 |
| Engagement | 0.30 | 0.25 | 0.10 |
| Support | 0.15 | 0.20 | 0.20 |
| Financial | 0.15 | 0.10 | 0.15 |
| CSM Sentiment | 0.15 | 0.10 | 0.05 |
| **Total** | **1.00** | **1.00** | **1.00** |

These are starting points. After 6 months of data, run correlation analysis to adjust weights based on which dimensions actually predicted churn in your client's specific context. Segment-specific models can improve prediction accuracy by 23% compared to a universal model [2].

---

## 5) Edge Cases & Deep Dives

### Edge Case 1: New Customer with Insufficient Data (&lt; 90 Days)

*Scenario:*

A customer signed 3 weeks ago. They have no historical usage trends, no QBR attendance data (first QBR is scheduled for month 2), no support history, and limited financial data (only one invoice paid). The automated health score produces a score of 22 (Red) because most dimensions return 0 or near-0 due to missing data.

*Challenge:*

New customers almost always score Red or Yellow in an automated model because lookback windows capture little-to-no data. This creates false alarms and erodes CSM trust in the model from day one.

*Approach:*

1. Apply the "Black" status for accounts under 90 days old (insufficient data, no classification)
2. Create an onboarding-specific health score with different metrics: implementation milestone completion, onboarding call attendance, time-to-first-value milestones
3. Transition to the standard health model at day 90 (or after onboarding completion, whichever comes first)
4. During the Black period, CSM manages the account through the onboarding playbook rather than the health score playbook

*Fallback assumptions:*

| Missing Data | Use This Instead | Source |
|--------------|------------------|--------|
| Product usage trend | Onboarding milestone completion rate | Implementation tracker |
| QBR attendance | Onboarding call attendance | Meeting records |
| Support ticket trend | Implementation support ticket resolution | Onboarding team feedback |
| Financial history | Contract terms and payment method (auto-pay = lower risk) | CRM contract record |

### Edge Case 2: Champion Departure

*Scenario:*

The primary champion (the person who bought the product, attends QBRs, and drives internal adoption) leaves the company. Product usage may remain stable for 30-60 days (other users continue their workflows), but the relationship dimension collapses: no executive sponsor, no one attending QBRs, email engagement drops.

*Challenge:*

The health score may not flag this quickly because product usage (often the highest-weighted dimension) remains unchanged. By the time usage declines (usually 60-90 days after champion departure), the window for intervention has narrowed.

*Approach:*

1. If champion departure is detected (via LinkedIn integration, bounce-back emails, CSM report), apply a temporary score penalty of -15 to -20 points regardless of other dimensions
2. Trigger an automatic intervention play: identify new internal champion within 14 days
3. CSM should override the engagement dimension to reflect reality even if automated signals have not caught up
4. Track new champion identification as a milestone; remove penalty once a new champion is confirmed and attending QBR

### Edge Case 3: Multi-Product or Multi-BU Account

*Scenario:*

A customer uses three different products from the same vendor (or operates across three business units with separate contracts). Product A has high usage and strong engagement. Product B has declining usage and no QBR attendance. Product C was purchased 2 months ago and is in onboarding.

*Challenge:*

A single composite score averages across products, making the account look Yellow when in reality Product A is Green, Product B is Red, and Product C is Black. The CSM needs product-level visibility to take the right action for each.

*Approach:*

1. Calculate a health score per product/contract, not just per account
2. Display both product-level and account-level scores on dashboards
3. Account-level score = weighted average of product scores, where weight = ARR contribution of each product
4. Alert logic should trigger on product-level Red scores, not just account-level
5. In the CS platform, configure separate scorecard views per product

### Edge Case 4: Seasonal Usage Patterns

*Scenario:*

An accounting software customer shows dramatic usage drops in January (post-tax-season wind-down) and July (vacation season). Every year, the health score flags them Red in January and July, then returns to Green in February and August. CSMs have learned to ignore these alerts.

*Challenge:*

Seasonal patterns create recurring false positives. CSMs develop "alert fatigue" and may ignore a genuine Red signal that coincides with a seasonal dip.

*Approach:*

1. Identify accounts with seasonal usage patterns by analyzing 12+ months of usage data for cyclical trends
2. Apply a seasonal adjustment factor: compare current period usage to the same period last year (YoY) rather than to the trailing 30-day average
3. Flag as at-risk only if current-period usage is significantly below the same period last year (e.g., 20%+ decline YoY)
4. Document seasonal accounts in the CS platform with a "Seasonal" tag so CSMs have context

### Edge Case 5: Data Quality Issues -- Stale or Missing Integrations

*Scenario:*

The product analytics integration stopped syncing 5 days ago due to an API credential expiration. Product usage scores for all accounts drop to 0, turning 60% of accounts Red overnight. CSMs are flooded with false alerts.

*Challenge:*

Data integration failures silently corrupt health scores. The model does not know the difference between "no usage" and "no data." This destroys trust in the health score system faster than any other issue.

*Approach:*

1. Build a data freshness monitor: for each data source, track the last successful sync timestamp
2. If any data source is stale (&gt;24 hours for daily-sync sources, &gt;7 days for weekly-sync), suppress that dimension from the health score calculation and redistribute weights across remaining dimensions
3. Display a "Data Quality Warning" badge on the dashboard when a dimension is suppressed
4. Configure alerts to the CS Ops team (not CSMs) when a data source goes stale
5. Require manual acknowledgment before re-enabling a dimension after an outage (to prevent score whiplash)

*Fallback assumptions:*

| Missing Data | Use This Instead | Source |
|--------------|------------------|--------|
| Product usage (integration down) | Last known scores + CSM sentiment override | Most recent valid sync + CSM input |
| Support data (system migration) | Manual ticket count from support team lead | Weekly email summary |
| Financial data (billing system change) | CRM contract and payment records | Salesforce/HubSpot |

---

## References

[1] [FunnelStory - Multi-Source Data Advantage in Churn Prediction](https://funnelstory.ai/blog/predicting-churn-retention-in-b2b-saas-101)
[2] [FunnelStory - Predicting Churn & Retention in B2B SaaS](https://funnelstory.ai/blog/predicting-churn-retention-in-b2b-saas-101)
[3] [ChurnZero - The Customer Health Score Handbook](https://churnzero.com/blog/the-customer-health-score-handbook-overview/)
[4] [Gainsight - Customer Health Scores Explained](https://www.gainsight.com/blog/customer-health-scores/)
[5] [Vitally - B2B SaaS Churn Rate Benchmarks 2025](https://www.vitally.io/post/saas-churn-benchmarks)
[6] [KBCM / Powered by Search - B2B SaaS Churn Rate Benchmarks](https://www.poweredbysearch.com/learn/b2b-saas-churn-rate-benchmarks/)
[7] [Maxio - 2025 B2B SaaS Benchmarks Report](https://www.maxio.com/resources/2025-saas-benchmarks-report)
[8] [Vitally - How to Create a Customer Health Score with 4 Metrics](https://www.vitally.io/post/how-to-create-a-customer-health-score-with-four-metrics)
