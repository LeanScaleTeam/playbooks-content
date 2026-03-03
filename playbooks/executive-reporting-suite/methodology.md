# Executive Reporting Suite — Methodology

This document covers the core concepts, frameworks, and calculations behind the Executive Reporting Suite. It provides the methodological foundation — the 'how it works' behind the execution steps.

---

## 1) Core Concepts

### The Single Source of Truth Problem

*What is it?*

The single source of truth (SSOT) problem is the core pain that executive reporting suites solve. It describes a state where GTM data is fragmented across CRM (Salesforce, HubSpot), marketing automation (HubSpot Marketing, Marketo), financial systems (QuickBooks, NetSuite), and ad-hoc spreadsheets -- with no unified view that all executives trust. When leadership asks "how are we tracking against targets?", it takes days to compile an answer, and the numbers often do not match between teams.

*Why does it matter?*

Without a single source of truth, executive decisions rely on inconsistent data, gut feel, or stale reports. This delays action, erodes confidence in the data, and causes inter-team misalignment (Marketing reports MQLs one way, Sales reports pipeline another, Finance reports revenue a third way). Research shows that 87% of organizations have low BI and analytics maturity [1], which means the majority of B2B SaaS companies are operating with fragmented reporting.

*Key insight:*

> The goal of an executive reporting suite is not to build dashboards. The goal is to create a shared language of metrics that every executive uses to make decisions -- and to embed that language into the operating rhythm of the business.

*Examples:*

| Context | Example |
|---------|---------|
| Quarterly board prep | CEO asks for ARR growth and pipeline health. RevOps spends 3 days pulling from Salesforce, HubSpot, and spreadsheets. Numbers do not match Finance's ARR because of different treatment of multi-year deals. |
| Weekly leadership meeting | CRO says pipeline is at $4M. VP Marketing says it is $3.2M because they exclude certain stages. No one agrees on the denominator. |
| Investor update | CFO uses a spreadsheet with manually entered data from last month. The numbers are already stale by the time the board deck ships. |

### Role-Based Dashboard Hierarchy

*What is it?*

Role-based dashboard hierarchy is the principle that different executives need different views of the same underlying data, organized in a pyramid structure: a single executive summary at the top, role-specific views in the middle, and drill-down detail at the base.

*Why does it matter?*

A CEO cares about ARR trajectory and overall business health. A CRO cares about pipeline coverage and quota attainment. A VP Marketing cares about MQL volume and campaign attribution. Putting all metrics on one dashboard overwhelms everyone and serves no one. Research from Improvado shows that effective executive dashboards are tailored to the user, with each role focusing on the 5-7 metrics most relevant to their decisions [2].

*The Framework:*

```
           +-----------------------+
           |  Executive Summary    |  CEO, Board
           |  (5-7 golden metrics) |
           +-----------+-----------+
                       |
        +--------------+--------------+
        |              |              |
   +----+----+   +----+----+   +----+----+
   |  Sales   |   |Marketing|   |   CS    |  CRO, VPs
   |  View    |   |  View   |   |  View   |
   +----+----+   +----+----+   +----+----+
        |              |              |
   +----+----+   +----+----+   +----+----+
   | Rep-Level|   |Campaign |   | Account |  Drill-Down
   |  Detail  |   | Detail  |   | Detail  |
   +---------+   +---------+   +---------+
```

*Common misunderstandings:*

- **Misconception:** Every executive should see the same dashboard with the same metrics.
  **Reality:** Shared metrics (the "golden metrics" like ARR and pipeline coverage) appear on every view, but each role needs additional context-specific metrics and different drill-down paths.

- **Misconception:** More metrics make a better dashboard.
  **Reality:** KPI-rich dashboards achieve only 30% utilization post-launch, dropping to 9% within 3 weeks when they overwhelm users with too many measures [3]. The less-is-more approach -- 5-7 metrics on the executive view -- drives more action.

### The "Golden Metrics" Principle

*What is it?*

Golden metrics are the 3-5 KPIs that appear on every executive view, regardless of role. They form the shared language of the business. Every other metric on the dashboard exists to explain or support these golden metrics.

*Why does it matter?*

Without golden metrics, each department optimizes for its own numbers in isolation. Marketing celebrates MQL volume while Sales complains about lead quality. CS reports strong NPS while expansion revenue stagnates. Golden metrics force every function to orient around the same outcomes -- typically ARR, pipeline health, and efficiency.

*Key insight:*

> If you cannot fit the most important metrics on a single screen without scrolling, you have too many. The executive summary dashboard should answer "how is the business doing?" in under 10 seconds.

*Examples:*

| Company Stage | Typical Golden Metrics |
|---------------|----------------------|
| Series A-B ($5M-$20M ARR) | ARR, MRR growth rate, pipeline coverage, burn rate, CAC payback |
| Series C-D ($20M-$60M ARR) | ARR, net revenue retention, pipeline coverage, sales efficiency, quota attainment |
| Late stage ($60M-$100M ARR) | ARR, NRR, pipeline coverage by segment, CAC:LTV, Rule of 40 score |

### Dashboard Adoption as a Change Management Problem

*What is it?*

Dashboard adoption is not a technology problem -- it is a behavioral change problem. Even perfectly built dashboards fail if they are not embedded into existing executive workflows (weekly leadership meetings, monthly business reviews, board prep).

*Why does it matter?*

60% of BI initiatives fail to deliver business value [4]. The failure rate is not driven by bad data or bad tools -- it is driven by dashboards that exist outside the daily workflow of the people they serve. Dashboards described by staff as "all show and no go" are dashboards that were designed without understanding how executives actually make decisions [3].

*Key insight:*

> A dashboard that is not referenced in a standing meeting within 2 weeks of launch is a dead dashboard. The adoption plan must be designed before the first visualization is built.

*Common misunderstandings:*

- **Misconception:** If you build a great dashboard, people will use it.
  **Reality:** Adoption requires embedding dashboards into existing operating rhythms -- weekly meetings, Slack alerts, automated email digests. The technology must meet executives where they already work.

- **Misconception:** Training solves adoption problems.
  **Reality:** Training teaches navigation. Adoption requires the dashboard to answer questions executives already ask in meetings they already attend.

---

## 2) Decision Frameworks

### Approach Selection Matrix

| Situation | Recommended Approach | Why |
|-----------|---------------------|-----|
| Client has clean CRM data, established BI platform (Looker/Tableau), and defined KPIs | Direct Build | Skip extended discovery; focus on visualization and adoption |
| Client has messy data, no BI platform, and unclear metric definitions | Discovery-First | Invest in metric alignment and data remediation before building anything |
| Client wants a quick executive view while planning a larger data initiative | MVP Dashboard | Build a lightweight 5-7 metric view in native CRM reporting (Salesforce/HubSpot) as a bridge |
| Client has multiple business units or products with different GTM motions | Segmented Build | Build separate dashboard views per segment, with a unified rollup at the top |
| Client is migrating BI platforms (e.g., Tableau to Looker) | Migration-Aware Build | Align dashboard architecture with the target platform; avoid building on the legacy tool |

### Scoping Factors

**1. Data Maturity**

- Clean CRM with consistent stages and 12+ months of history --> Standard build timeline (4-6 weeks)
- CRM with data quality issues (missing fields, inconsistent naming, duplicates) --> Add 2-3 weeks for data remediation
- No centralized data warehouse --> Add integration layer design to scope; consider native CRM reporting as MVP

**2. Number of Data Sources**

- Single source (CRM only) --> Simpler architecture, faster build
- 2-3 sources (CRM + marketing automation + finance) --> Standard integration complexity
- 4+ sources (CRM + MAP + finance + product analytics + support) --> Significant data architecture effort; consider a data warehouse intermediary

**3. Number of Executive Stakeholders**

- 2-3 stakeholders --> Standard discovery; 1-2 interview rounds
- 5+ stakeholders --> Extended discovery; risk of scope creep from competing metric requests; requires prioritization framework (P0/P1/P2)

**4. BI Platform Maturity**

- Established Looker/Tableau instance with admin support --> Build directly on existing platform
- New BI platform with no existing configuration --> Add platform setup and admin training to scope
- No BI platform; client uses native CRM reports --> Consider CRM-native dashboards (Salesforce Reports &amp; Dashboards, HubSpot Custom Reports) for faster delivery

**5. Metric Definition Alignment**

- Finance, Sales, and Marketing agree on ARR calculation and stage definitions --> Standard build
- Departments define metrics differently (e.g., different ARR treatments for multi-year deals) --> Add metric alignment workshop to scope; requires Finance sign-off before build

### Discovery-First Approach

*Best for:*
- Companies with no existing executive dashboard
- Organizations where departments define metrics differently
- Situations where "we do not know what we do not know" about data quality

*Not recommended for:*
- Companies with an existing dashboard suite that just needs refresh or platform migration
- Quick-turnaround engagements where the client already has defined KPIs

*Key differences from standard:*

| Aspect | Standard Build | Discovery-First |
|--------|---------------|-----------------|
| Timeline | 4-6 weeks | 6-9 weeks |
| First deliverable | Draft dashboard | Metric definitions document + data quality assessment |
| Stakeholder interviews | 1 round | 2 rounds (discovery + validation) |
| Data work | Connect and visualize | Remediate, then connect and visualize |

### MVP Dashboard Approach

*Best for:*
- Companies that need executive visibility quickly while planning a larger BI initiative
- Budget-constrained engagements
- Organizations where data lives primarily in one system (CRM)

*Not recommended for:*
- Companies with complex multi-source data needs
- Situations requiring advanced visualizations or custom calculations not supported by native CRM reporting

*Key differences from standard:*

| Aspect | Standard Build | MVP Dashboard |
|--------|---------------|---------------|
| Platform | Looker, Tableau, or equivalent | Native CRM (Salesforce Dashboards, HubSpot Reports) |
| Metrics | 15-25 across all views | 5-7 on a single executive view |
| Data sources | Multi-source integration | Single-source (CRM) |
| Maintenance | Requires BI admin skills | CRM admin can maintain |
| Timeline | 4-6 weeks | 2-3 weeks |

---

## 3) Benchmarks & Standards

### How to Use Benchmarks

*Benchmarks are guidelines, not rules. Always:*
1. Start with benchmark as baseline
2. Adjust based on client-specific data (industry, company stage, GTM motion)
3. Validate against their actual numbers when available
4. Document deviations and rationale

### Revenue & Growth Metrics

| Metric | Low | Typical | High | Notes |
|--------|-----|---------|------|-------|
| ARR Growth Rate (Series A-B) | &lt;20% | 25-40% | &gt;50% | Median B2B SaaS growth rate is 25% in 2025 [5] |
| Net Revenue Retention (NRR) | &lt;100% | 105-115% | &gt;120% | Below 100% means the business is shrinking from existing customers |
| Gross Revenue Retention (GRR) | &lt;85% | 90-95% | &gt;97% | Measures logo and contraction churn without expansion |
| Monthly Churn Rate | &gt;5% | 2-3.5% | &lt;1.5% | Average B2B SaaS monthly churn is 3.5% [5] |

**Source:** SaaS Capital 2025 B2B SaaS Benchmarks, Maxio 2025 SaaS Benchmarks Report [5][6]

**Interpretation:**
- **Below low:** Signals fundamental product-market fit or retention issues. Dashboard should flag these in red with drill-down to cohort analysis.
- **Above high:** Indicates strong performance. Verify data accuracy -- unusually high NRR may indicate calculation errors (e.g., including one-time upsells as recurring).

### Pipeline & Sales Efficiency Metrics

| Metric | Low | Typical | High | Notes |
|--------|-----|---------|------|-------|
| Pipeline Coverage Ratio | &lt;2x | 3-4x | &gt;5x | Enterprise targets 3-5x; SMB can operate at 2-3x [7] |
| Win Rate | &lt;10% | 15-25% | &gt;30% | Varies heavily by deal size and motion |
| Average Sales Cycle (days) | 30-40 | 60-90 | 120-170 | ACV &lt;$5K averages 40 days; ACV &gt;$100K averages 170 days [8] |
| Quota Attainment | &lt;50% | 55-70% | &gt;80% | Industry average hovers around 57-67% |

**Source:** HubSpot Sales Cycle Research, Outreach Pipeline Coverage Guide [7][8]

**Interpretation:**
- **Pipeline coverage below 2x:** Revenue target is at risk. Dashboard alert should fire immediately.
- **Pipeline coverage above 5x:** Either quotas are too low or pipeline is inflated with stale deals. Investigate deal aging.

### Marketing & Funnel Metrics

| Metric | Low | Typical | High | Notes |
|--------|-----|---------|------|-------|
| MQL-to-SQL Conversion | &lt;10% | 15-25% | &gt;35% | Depends heavily on MQL definition stringency |
| SQL-to-Opportunity Conversion | &lt;30% | 40-60% | &gt;70% | Higher rates suggest strong qualification criteria |
| Lead-to-Close Rate | &lt;1% | 2-5% | &gt;7% | End-to-end funnel efficiency |
| CAC Payback Period (months) | &gt;18 | 12-15 | &lt;9 | B2B SaaS CAC has increased 55% over 3 years [9] |

**Source:** First Page Sage SaaS Benchmarks, Maxio 2025 SaaS Benchmarks Report [6][9]

### Customer Success Metrics

| Metric | Low | Typical | High | Notes |
|--------|-----|---------|------|-------|
| Logo Retention Rate | &lt;85% | 90-95% | &gt;97% | Varies by segment (Enterprise retains higher than SMB) |
| Expansion Revenue % of Total | &lt;10% | 15-25% | &gt;30% | Healthy expansion signals product-market fit depth |
| NPS Score (B2B SaaS) | &lt;30 | 35-50 | &gt;60 | Use as directional indicator, not standalone KPI |
| Time to Value (days) | &gt;90 | 30-60 | &lt;14 | Shorter TTV correlates with higher retention |

### Quick Reference Thresholds

*For common "is this good?" questions during dashboard review:*

| Question | Good | Warning | Red Flag |
|----------|------|---------|----------|
| Pipeline coverage for the quarter? | 3x+ remaining quota | 2-3x remaining quota | &lt;2x remaining quota |
| Win rate trending? | Stable or increasing QoQ | Dropped 5-10% QoQ | Dropped &gt;10% QoQ |
| ARR growth on track? | Within 10% of plan | 10-20% below plan | &gt;20% below plan |
| NRR healthy? | &gt;110% | 100-110% | &lt;100% |
| Dashboard actually being used? | Referenced in weekly meetings | Opened weekly but not in meetings | Not opened in 2+ weeks |

### Data Freshness Standards

| Data Type | Minimum Refresh | Recommended Refresh | Rationale |
|-----------|----------------|---------------------|-----------|
| Pipeline data | Daily | Hourly | Reps update CRM throughout the day; stale pipeline misleads forecasts |
| Revenue/ARR | Daily | Daily | Financial data is less volatile; daily is sufficient |
| Marketing metrics (MQLs, campaigns) | Daily | Every 6 hours | Campaign performance shifts quickly; near-real-time is valuable |
| Customer health scores | Weekly | Daily | Health signals change gradually but should not lag by more than a week |
| Financial data (CAC, LTV) | Monthly | Monthly | These are trailing indicators; monthly calculation is standard |

---

## 4) Calculations & Scoring

### Formula Quick Reference

| Calculation | Formula | Example |
|-------------|---------|---------|
| ARR | `MRR x 12` or `Total Contract Value / Contract Years` | $50K MRR = $600K ARR; $150K 3-year deal = $50K ARR |
| Sales Velocity | `(# Opportunities x Avg Deal Size x Win Rate) / Avg Sales Cycle (days)` | (100 x $25K x 20%) / 90 = $5,556/day |
| Pipeline Coverage | `Total Weighted Pipeline / Remaining Quota` | $3M pipeline / $1M remaining = 3x coverage |
| CAC | `Total Sales & Marketing Spend / New Customers Acquired` | $500K spend / 50 customers = $10K CAC |
| LTV | `ARPU x Gross Margin % x (1 / Monthly Churn Rate)` | $2K MRR x 80% x (1 / 3%) = $53,333 |
| LTV:CAC Ratio | `LTV / CAC` | $53,333 / $10,000 = 5.3:1 |
| CAC Payback (months) | `CAC / (MRR x Gross Margin %)` | $10,000 / ($2,000 x 80%) = 6.25 months |
| NRR | `(Starting ARR + Expansion - Contraction - Churn) / Starting ARR x 100` | ($1M + $200K - $50K - $30K) / $1M = 112% |

### ARR Calculation Methodology

**Formula:**
```
ARR = Sum of all active recurring subscription revenue, annualized

For monthly contracts: MRR x 12
For annual contracts: Annual contract value
For multi-year contracts: Total Contract Value / Number of Years
```

**Variables explained:**
- `MRR` = Monthly Recurring Revenue from active subscriptions
- `Total Contract Value (TCV)` = Full value of a multi-year deal including all years
- `Contract Years` = Duration of the contract in years

**What to INCLUDE in ARR:**
- Recurring subscription fees
- Recurring add-ons and modules
- Contracted usage minimums or true-ups expected to recur
- Multi-year deals normalized per year

**What to EXCLUDE from ARR:**
- One-time onboarding, setup, or implementation fees
- Professional services revenue
- Perpetual license fees
- Non-recurring add-ons
- Hardware or physical product revenue

**Worked Example:**

*Scenario: Mid-market B2B SaaS company with mixed contract types*

```
Given:
- 50 monthly customers at $2,000/month MRR
- 30 annual customers at $30,000/year each
- 5 multi-year customers (3-year deals at $120,000 TCV each)
- $200,000 in professional services revenue (excluded)

Calculate:
- Monthly ARR contribution: 50 x $2,000 x 12 = $1,200,000
- Annual ARR contribution: 30 x $30,000 = $900,000
- Multi-year ARR contribution: 5 x ($120,000 / 3) = $200,000
- Total ARR = $1,200,000 + $900,000 + $200,000 = $2,300,000
```

**Validation:**
- ARR should reconcile to Finance's revenue figures within 5% tolerance
- If the gap is larger, investigate: one-time revenue mixed in, multi-year deal normalization differences, or churn not properly reflected
- Best practice: reconcile ARR to revenue monthly to catch mis-categorized items [10]

### ARR Component Tracking

**Formula:**
```
ARR Movement = New ARR + Expansion ARR - Contraction ARR - Churned ARR

Where:
- New ARR = Revenue from brand-new customers
- Expansion ARR = Upsells, cross-sells, price increases from existing customers
- Contraction ARR = Downgrades or reduced usage from existing customers
- Churned ARR = Revenue lost from customers who cancelled
```

**Why this matters for dashboards:**

An executive dashboard that shows only total ARR misses the story. Showing the four components reveals whether growth is coming from new business or expansion, and whether churn is accelerating. The dashboard should display an ARR waterfall (bridge) chart showing each component's contribution to net ARR change.

### Sales Velocity

**Formula:**
```
Sales Velocity = (Number of Qualified Opportunities x Average Deal Size x Win Rate) / Average Sales Cycle Length (days)
```

**Variables explained:**
- `Number of Qualified Opportunities` = Deals that entered pipeline during the measurement period
- `Average Deal Size` = Mean ACV of closed-won deals
- `Win Rate` = Percentage of qualified opportunities that close (closed-won / total qualified)
- `Average Sales Cycle Length` = Mean days from opportunity creation to close

**Worked Example:**

*Scenario: B2B SaaS company measuring quarterly sales velocity*

```
Given:
- 80 qualified opportunities created this quarter
- Average deal size: $30,000 ACV
- Win rate: 22%
- Average sales cycle: 75 days

Calculate:
- Sales Velocity = (80 x $30,000 x 0.22) / 75
- Sales Velocity = $528,000 / 75
- Sales Velocity = $7,040 per day
```

**Validation:**
- Multiply by ~90 days in a quarter to sanity-check: $7,040 x 90 = $633,600 in expected quarterly bookings
- Compare against actual quarterly bookings to validate the model
- If velocity is declining, drill into which variable changed (fewer opps? smaller deals? lower win rate? longer cycles?)

### Pipeline Coverage Ratio

**Formula:**
```
Pipeline Coverage = Total Qualified Pipeline Value / Remaining Quota for Period
```

**Worked Example:**

*Scenario: Mid-quarter pipeline review*

```
Given:
- Quarterly quota: $500,000
- Closed-won so far this quarter: $180,000
- Remaining quota: $320,000
- Current qualified pipeline: $960,000

Calculate:
- Pipeline Coverage = $960,000 / $320,000 = 3.0x
```

**Interpretation thresholds:**

| Coverage | Interpretation | Dashboard Action |
|----------|---------------|-----------------|
| &lt;2x | High risk of missing quota | Red flag alert; trigger pipeline generation review |
| 2-3x | Moderate risk; depends on win rate | Yellow warning; monitor weekly |
| 3-4x | Healthy coverage for most B2B motions | Green status; standard tracking |
| &gt;5x | Possible pipeline inflation | Investigate deal aging; check for stale opps |

### LTV:CAC Ratio

**Formula:**
```
LTV = ARPU x Gross Margin % x (1 / Monthly Churn Rate)
CAC = Total Sales & Marketing Spend / New Customers Acquired
LTV:CAC = LTV / CAC
```

**Worked Example:**

*Scenario: Series B SaaS company*

```
Given:
- Average MRR per customer: $3,000
- Gross margin: 78%
- Monthly churn rate: 2.5%
- Quarterly S&M spend: $450,000
- New customers acquired this quarter: 30

Calculate:
- LTV = $3,000 x 0.78 x (1 / 0.025) = $3,000 x 0.78 x 40 = $93,600
- CAC = $450,000 / 30 = $15,000
- LTV:CAC = $93,600 / $15,000 = 6.2:1
```

**Validation:**
- Healthy B2B SaaS LTV:CAC range: 3:1 to 5:1 [9]
- Below 3:1 indicates unprofitable customer acquisition
- Above 5:1 may indicate under-investment in growth (could be spending more to grow faster)
- Median B2B SaaS LTV:CAC is 3.2:1 [9]

---

## 5) Edge Cases & Deep Dives

### Edge Case 1: New Company with Limited Historical Data

*Scenario:*

A Series A company with less than 12 months of CRM data, recently defined opportunity stages, and no established benchmarks for their own performance. They want an executive dashboard but lack the historical data to show trends or set meaningful targets.

*Challenge:*

Trend visualizations are meaningless with 3-6 months of data. Conversion rate benchmarks are unreliable with small sample sizes (&lt;50 deals per stage). There is no "last year" to compare against.

*Approach:*

1. Use industry benchmarks (from this document's Benchmarks section) as placeholder targets
2. Build dashboards with a "data maturity timeline" -- show when each metric will have enough data to be statistically reliable
3. Focus on leading indicators (pipeline creation, activity volume) over trailing indicators (conversion rates, LTV) in early dashboards
4. Set a 6-month checkpoint to recalibrate targets against actual performance

*Fallback assumptions:*

| Missing Data | Use This Instead | Source |
|--------------|------------------|--------|
| Historical win rate | 15-20% (B2B SaaS average) | Industry benchmark [7] |
| Sales cycle length | 60-90 days for mid-market | HubSpot research [8] |
| Churn rate | 3-3.5% monthly | B2B SaaS median [5] |
| Pipeline coverage target | 3x | Standard B2B benchmark [7] |

### Edge Case 2: Multi-Product or Multi-Segment Company

*Scenario:*

A company sells multiple products to different segments (SMB self-serve, mid-market sales-assisted, enterprise field sales) with different pricing, sales cycles, and success metrics. They want one executive dashboard.

*Challenge:*

Blending metrics across segments obscures the story. A company-wide 20% win rate might mask that SMB is at 35% and Enterprise is at 8%. Average deal size means nothing when deals range from $5K to $500K.

*Approach:*

1. Build a unified executive summary that shows total ARR and net ARR change, but segments the waterfall by product/segment
2. Create one drill-down view per segment with segment-appropriate benchmarks
3. Use weighted averages only at the top level; show unblended metrics in segment views
4. Define which segments get full dashboard treatment (revenue &gt; $X or &gt; Y customers) vs. summary-only

### Edge Case 3: Data Quality Crisis Discovered Mid-Build

*Scenario:*

During the data audit phase, you discover that CRM data has significant quality issues: inconsistent opportunity stages, missing close dates, duplicate accounts, or revenue fields that do not match Finance's numbers.

*Challenge:*

Building dashboards on bad data destroys executive trust. One wrong number in an executive dashboard poisons confidence in all the data.

*Approach:*

1. Triage data issues into three categories:
   - **Blocking:** Prevents core KPI calculation (e.g., ARR cannot be calculated because revenue field is unreliable). Fix before build.
   - **Degrading:** Reduces accuracy but does not prevent calculation (e.g., 15% of opportunities missing close dates). Flag on dashboard; fix in parallel.
   - **Cosmetic:** Affects detail views but not executive metrics (e.g., inconsistent account naming). Fix post-launch.
2. Build an MVP dashboard using only metrics with clean underlying data
3. Add a "Data Quality" indicator to each dashboard panel (green/yellow/red) so executives know which numbers to trust
4. Present the remediation plan as part of the dashboard rollout -- executives see the path to full accuracy

### Edge Case 4: PLG (Product-Led Growth) Hybrid Company

*Scenario:*

The company has both a self-serve PLG motion (users sign up, use a free tier, and convert to paid) and a sales-assisted motion (enterprise deals with AEs). Traditional funnel metrics (MQL to SQL to Opp to Close) do not capture the PLG side.

*Challenge:*

PLG companies generate revenue from product signups that never touch a sales rep. Traditional funnel dashboards miss this entirely.

*Approach:*

1. Build two parallel funnel views:
   - **PLG funnel:** Signup to Activation to Free-to-Paid Conversion to Expansion
   - **Sales-led funnel:** MQL to SQL to Opportunity to Close
2. Create a unified revenue view that shows total new ARR from both motions
3. Track Product-Qualified Leads (PQLs) as the PLG equivalent of MQLs -- users who hit usage thresholds that indicate buying intent
4. Show cross-motion dynamics: what percentage of enterprise deals started as PLG users?

### Edge Case 5: Dashboard Adoption Stalls Post-Launch

*Scenario:*

The dashboard was built correctly, validated against source data, and demonstrated in training. But 3 weeks after launch, login data shows that only 2 of 7 executives are using it regularly.

*Challenge:*

This is the most common failure mode. The technology works, but the behavioral change did not happen. The research predicts this: dashboard utilization drops from 30% to 9% within 3 weeks when dashboards are not embedded in operating rhythms [3].

*Approach:*

1. Diagnose the root cause through 1-on-1 conversations with non-adopters:
   - Do they not know how to use it? --> More training (unlikely to be the real issue)
   - Does it not answer their questions? --> Metric gap; add the missing KPI
   - Is it not part of their workflow? --> Embed in meetings (this is usually the real issue)
2. Work with the executive sponsor (CRO or VP RevOps) to mandate dashboard review in at least one standing meeting
3. Configure automated Slack or email digests that push key metrics to executives daily/weekly -- so they see the data even without logging in

---

## References

[1] [Gartner - 87 Percent of Organizations Have Low BI and Analytics Maturity](https://www.gartner.com/en/newsroom/press-releases/2018-12-06-gartner-data-shows-87-percent-of-organizations-have-low-bi-and-analytics-maturity)
[2] [Improvado - Executive Dashboards: Examples, Templates & Best Practices](https://improvado.io/blog/executive-dashboards)
[3] [Johnny Grow - The Ultimate RevOps Dashboard](https://johnnygrow.com/business-growth/revenue-operations/the-ultimate-revops-dashboard/)
[4] [Dataversity - Why 60% of BI Initiatives Fail](https://www.dataversity.net/articles/why-60-of-bi-initiatives-fail-and-how-enterprises-can-avoid-it/)
[5] [SaaS Capital - 2025 Private B2B SaaS Growth Rate Benchmarks](https://www.saas-capital.com/research/private-saas-company-growth-rate-benchmarks/)
[6] [Maxio - 2025 SaaS Benchmarks Report](https://www.maxio.com/resources/2025-saas-benchmarks-report)
[7] [Outreach - Sales Pipeline Coverage Ratio Guide](https://www.outreach.io/resources/blog/sales-pipeline-coverage-ratio)
[8] [Dock - Sales Velocity 101: Calculations, Benchmarks, and Tips](https://www.dock.us/library/sales-velocity)
[9] [First Page Sage - The SaaS LTV to CAC Ratio](https://firstpagesage.com/seo-roi/the-saas-ltv-to-cac-ratio-fc/)
[10] [Cobloom - How to Properly Calculate ARR and MRR for Your SaaS Business](https://www.cobloom.com/blog/how-to-calculate-saas-arr-mrr)
