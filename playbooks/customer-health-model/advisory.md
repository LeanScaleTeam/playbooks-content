# Customer Health Model — Advisory

Customer Health Model - Multi-Dimensional Customer Health Scoring for Proactive Retention

---

## 1) Project Overview

### What is the name of this project?

Customer Health Model - Multi-Dimensional Scoring System for Proactive Churn Prevention

### What is the purpose of this project?

This project creates a data-driven customer health scoring system that combines product usage signals, CSM sentiment, support interactions, and engagement metrics into a unified score with Red/Yellow/Green thresholds. The output is an automated, always-on health dashboard that replaces CSM gut-feel with objective, multi-dimensional account intelligence.

**Core transformation:** From reactive churn surprises driven by inconsistent CSM intuition to proactive, signal-based intervention that catches at-risk accounts 60-90 days before they churn.

### What Customer Health Model Unlocks

After this project is complete, the Customer Success organization gains:

- Objective, data-driven account prioritization across every CSM's book of business
- Automated alerts when accounts cross health thresholds (Green to Yellow, Yellow to Red)
- Drill-down visibility into which specific metrics are driving low scores
- Standardized intervention playbooks triggered by health score categories
- Foundation for predictive churn modeling and expansion opportunity identification
- Executive-level visibility into overall customer base health and trend direction

| Before                       | After                     |
| ---------------------------- | ------------------------- |
| CSMs rely on gut feel to assess account health | Objective, weighted health score across 5-7 dimensions |
| Churn surprises with no early warning | Red-flag alerts 60-90 days before renewal risk |
| No standard response to at-risk signals | Defined intervention playbooks for Red, Yellow, Green accounts |
| VP CS asks "how's the book?" and gets anecdotal answers | Real-time dashboard showing health distribution and trends |
| Different CSMs assess the same situation differently | Consistent scoring model applied uniformly across accounts |
| Expansion opportunities identified by chance | Green accounts flagged for expansion based on usage signals |

### What business outcomes does this project drive?

**Primary Outcomes:**

- Reduced surprise churn: accounts that churned without being flagged Red 60+ days prior drop by 40-50% within 6 months
- Increased CSM efficiency: prioritization shifts from "who called last" to "who needs attention now," reducing wasted effort on healthy accounts
- Faster intervention: average time from risk signal to CSM action drops from weeks to days through automated alerts

**Secondary Outcomes:**

- Foundation for renewal forecasting models that use health score as a primary input
- Data-driven QBR conversations with accounts showing exactly which health dimensions need attention
- Expansion pipeline identification from consistently Green accounts with high usage signals
- Companies using health scoring see NRR lift of 6-12 points, particularly in mid-market SaaS [1]

### Who in the Org can benefit from this project?

VP Customer Success, Head of Customer Operations, Customer Success Managers, CS Operations/RevOps, VP Sales (for at-risk revenue visibility), Product team (usage pattern insights), Executive team (board-level retention reporting)

### Pain Points this Project Solves

Customer health scoring is foundational infrastructure that enables proactive retention management. The specific pain it solves depends on whether the team is struggling with churn visibility, CSM consistency, or executive reporting.

| Pain Point              | What Customer Health Model Enables  |
| ----------------------- | ---------------------------- |
| "We get blindsided by churn -- accounts leave and nobody saw it coming" | Automated Red-flag alerts when accounts show declining health across multiple dimensions, giving 60-90 days of warning |
| "Every CSM assesses account health differently -- there's no consistency" | A weighted, multi-dimensional scoring model applied uniformly so every account is measured the same way |
| "We can't prioritize our book of business -- everyone feels equally urgent" | Clear Red/Yellow/Green categorization that tells CSMs exactly which accounts need immediate attention |
| "Leadership asks about retention risk and we give them guesses, not data" | Real-time dashboards showing health score distribution, trend direction, and segment-level breakdowns |
| "We only react to problems after the customer complains" | Proactive support outreach based on declining usage or support ticket spikes, before the customer escalates |
| "We have data in five systems but no single view of account health" | Unified health score pulling from CRM, product analytics, support system, and billing into one composite metric |

### The Data Behind the Problem

The cost of reactive churn management is well-documented:

- The average B2B SaaS company experiences 3.5% annual gross churn, with small/medium firms running 3-5% monthly [2]. For a $20M ARR company, even 1% improvement in retention translates to $200K in preserved revenue.
- Companies using predictive analytics for customer retention experience a 15-20% reduction in churn rates [3]. Proactive support (outreach before an issue escalates) reduces churn by 27% among customers who experienced a problem [4].
- Firms with dedicated CSMs see up to 25% higher NRR than those without, but CSM effectiveness depends on data quality -- without health scoring, CSMs spend time on accounts that don't need attention and miss those that do [1].
- B2B SaaS companies report an average annual retention rate of 74%, with top performers pushing NRR past 120% [5]. The gap between average and top performers is largely driven by proactive, data-informed retention practices.
- Proactive problem resolution before customer contact achieves 89% retention rates [4], compared to significantly lower rates when companies wait for the customer to raise the issue.

### Key Metaphors or Frameworks

**The Dashboard vs. Warning Lights Metaphor**

A car dashboard doesn't wait for the engine to seize before telling you something is wrong. It monitors oil pressure, temperature, fuel, and battery continuously -- and lights up a warning when any dimension crosses a threshold. A customer health score works the same way: it monitors product usage, engagement, support load, and financial signals continuously, giving you a warning light (Red status) before the engine fails (churn).

*When to use it:* When explaining to CS leaders why a single metric (like NPS or login frequency) isn't sufficient. The dashboard metaphor helps them see that health requires multiple simultaneous signals.

*When NOT to use it:* When talking to data teams or engineers. They'll want to discuss the actual scoring model, weights, and thresholds -- not analogies.

### Target Motion

Customer Health Model is designed for SLG (Sales-Led Growth) and hybrid SLG/PLG companies with a dedicated Customer Success function. The project works for both high-touch enterprise CS and mid-market pooled CS models, though the health dimensions and weights differ by motion.

*Not a fit for:* Pure self-serve PLG companies with no named CSMs (they need product analytics and in-app health monitoring instead). Also not a fit for companies with fewer than 50 customers -- at that scale, CSMs typically know every account personally and a formal scoring model adds overhead without proportional benefit.

### Common Belief Barriers

**"Our CSMs already know which accounts are at risk -- we don't need a score."** -- CSM intuition is valuable but inconsistent and doesn't scale. Research shows that teams building health scores with 30+ variables found "no one on the team trusted it" [6], but the solution isn't to skip scoring -- it's to build a simple, explainable model that augments CSM judgment rather than replacing it. The best health scores use CSM sentiment as one input dimension alongside objective data.

**"We don't have enough data to build a meaningful health score."** -- You don't need perfect data to start. Gainsight's research shows you can structure a health score with as few as 4 metrics [7]. Start with what you have (login frequency, support tickets, renewal date proximity, CSM sentiment) and add dimensions as data matures. Waiting for perfect data means waiting forever while accounts churn.

**"We tried a health score before and nobody used it."** -- Most failed health scores fail for one of two reasons: too many metrics making the score uninterpretable, or no defined action based on the score. This project includes intervention playbooks (what to do for Red, Yellow, Green) and dashboard training so CSMs know exactly how to act on the score. See Implementation for the enablement plan.

**"A single number can't capture the complexity of a customer relationship."** -- Correct -- which is why this isn't a single number. It's a weighted composite across 5-7 dimensions with drill-down visibility into which specific metrics are driving the score. The aggregate provides prioritization; the dimensions provide diagnosis.

---

## 2) Tools & Systems

### Primary Tools

**Customer Success Platform (Gainsight, ChurnZero, Vitally, Totango, Catalyst, Planhat)**

The CS platform is the primary execution layer where the health score is built, calculated, and displayed. Gainsight is the market leader and named a Leader in both the Gartner Magic Quadrant and Forrester Wave for Customer Success Platforms [3]. ChurnZero scores highest in health score customization with fully customizable "churn scores" and no limit on the number of scores [8]. Vitally is known for fast implementation (2-3 week deployment) and a modern UI with strong automation [8].

**CRM (Salesforce or HubSpot)**

Source of customer account data, renewal dates, contract values, expansion history, and CSM assignments. The CRM provides the account-level container that health score dimensions attach to.

**Product Analytics Platform (Segment, Amplitude, Mixpanel, Pendo, Heap)**

Source of product usage signals: login frequency, feature adoption, active user counts, session duration, and license utilization. This is typically the highest-weighted dimension in health scoring.

**Support System (Zendesk, Intercom, Freshdesk, Salesforce Service Cloud)**

Source of support interaction data: ticket volume, escalation frequency, time-to-resolution, and CSAT scores. Support patterns are a strong leading indicator of churn.

**Data Providers (if applicable):**

- Standard analytics integration: Segment (event routing to CS platform)
- Enterprise product analytics: Amplitude, Mixpanel (deep usage analysis)
- In-app engagement: Pendo, Gainsight PX (feature-level adoption tracking)
- BI layer (optional): Looker, Tableau, Power BI (executive-level health dashboards beyond CS platform native reporting)

---

## 3) Stakeholders & Roles

### Client-Side Stakeholders

**VP Customer Success (Executive Sponsor)**

- Required for: Discovery, metric validation, threshold approval, final sign-off
- Responsibilities: Approves health score model, defines intervention SLAs, champions adoption across CS team

**Head of CS Operations or RevOps Manager (Technical Owner)**

- Required for: All phases -- discovery through handoff
- Responsibilities: Validates data availability, owns CS platform configuration post-handoff, manages ongoing model calibration

**CS Managers (Input Providers)**

- Required for: Discovery (churn analysis interviews), pilot validation, training
- Responsibilities: Share historical churn insights, validate scores against known account situations, provide feedback during pilot

**Data/Analytics Engineer (Technical Support)**

- Required for: Integration phase
- Responsibilities: Provides product analytics access, configures API connections, validates data freshness and accuracy

### Technical Owners

**Head of CS Operations / RevOps Manager**

- Owns CS platform health score configuration post-handoff
- Manages quarterly health score calibration reviews
- Handles metric weight or threshold adjustments based on model performance

**Product Analytics Lead (If Separate)**

- When this role is needed: When product usage data requires custom API integrations or transformations
- What they handle: Event tracking implementation, data pipeline maintenance for usage signals flowing to CS platform

**Enterprise Considerations (If Applicable)**

- IT/Security approval may be needed for new data integrations between product analytics, support, and CS platform
- Data governance review may be required if health score incorporates PII or usage data subject to customer agreements

---

## 4) Scoping

### Scoping Factors

**1. Number of Customer Segments**

- Single segment (all accounts scored the same) -&gt; Simpler model, faster build, 40-50 hours
- 2-3 segments (Enterprise, Mid-Market, SMB) -&gt; Segment-specific weights and thresholds, 50-65 hours
- 4+ segments or product-line splits -&gt; Significant complexity, may need multiple health score models, 65-80 hours

**2. CS Platform Maturity**

- CS platform already in production with data flowing -&gt; Focus is model design and configuration, saves 10-15 hours
- CS platform recently implemented but not fully configured -&gt; Need to set up integrations first, adds integration overhead
- No CS platform yet -&gt; This project depends on platform implementation completing first (see Customer Success Platform Implementation playbook)

**3. Data Source Availability**

- Product analytics, CRM, and support data all accessible via native integrations -&gt; Straightforward data setup
- Some data sources require custom API work or CSV imports -&gt; Add 10-20 hours for integration engineering
- Key data sources missing entirely (no product analytics tracking) -&gt; Must scope a data instrumentation phase first or proceed with available dimensions only

**4. Historical Data Depth**

- 12+ months of customer data with churn records -&gt; Full model validation possible, highest confidence in weights
- 6-12 months of data -&gt; Sufficient for initial model, plan for recalibration at 6-month mark
- Less than 6 months -&gt; Can build directional model but validation will be limited; flag as higher risk

**5. Number of Health Score Metrics**

- 3-5 metrics -&gt; Simple, explainable, fast to build and validate
- 6-8 metrics -&gt; Standard complexity, good balance of signal coverage and interpretability
- 9+ metrics -&gt; Risk of overcomplication; recommend consolidating to 7 or fewer based on churn correlation analysis

**6. Intervention Playbook Scope**

- Basic (Red/Yellow/Green actions defined) -&gt; Standard inclusion, 5-8 hours
- Advanced (automated triggers, multi-step playbooks in CS platform, escalation workflows) -&gt; 15-20 hours additional

### Multiple Approaches

**Approach 1: Quick-Start Health Score**

- Criteria: CS platform in production, product analytics available, single segment, fewer than 200 accounts
- Execution: 5-7 metrics, single set of weights and thresholds, manual CSM sentiment input, basic dashboard. Focus on getting a working score live in 3-4 weeks rather than optimizing the model.

**Approach 2: Standard Multi-Dimension Model**

- Criteria: 2-3 customer segments, multiple data sources available, 200-2,000 accounts, CS team of 5-15 CSMs
- Execution: Full discovery with churn analysis, segment-specific weights, automated data collection, dashboards with drill-down, intervention playbooks. 6-8 week timeline.

**Approach 3: Enterprise Health Score Program**

- Criteria: 4+ segments or product lines, 2,000+ accounts, complex data architecture, multiple CS teams or geos
- Execution: Phased rollout starting with one segment, custom API integrations, advanced dashboard suite with executive views, automated intervention workflows, formal pilot and validation phase. 10-14 week timeline.

---

## 5) Discovery Questions

### Questions for Project Kickoff

**Business Context**

- What does your churn profile look like today? *(Establishes baseline and reveals whether churn is concentrated in specific segments or reasons)*
- How many customers churned in the past 12 months, and what were the primary reasons? *(Identifies which health dimensions matter most)*
- Do you have a renewal process today, and how far in advance do you start? *(Reveals whether health scoring feeds into an existing workflow or needs to create one)*
- What's your current NRR/GRR and what's the board target? *(Quantifies the business case and urgency)*

**Current State**

- How do CSMs currently assess account health? *(Reveals the gap between gut-feel and data-driven approaches)*
- Do you have any existing health score or risk assessment? If so, what's working and what isn't? *(Avoids rebuilding what works, focuses on gaps)*
- How are at-risk accounts identified and escalated today? *(Maps current intervention workflow)*
- What data sources do you currently use to understand customer behavior? *(Scoping for integration work)*

**Technical Environment**

- Which CS platform are you using, and what tier/plan? *(Determines health score module availability)*
- Where does product usage data live -- do you have Segment, Amplitude, Mixpanel, or a homegrown system? *(Scoping data integration complexity)*
- What's your support system, and is ticket data accessible via API or integration? *(Confirms support dimension feasibility)*
- How is billing data managed -- integrated with CRM or in a separate system like Stripe or Chargebee? *(Determines financial dimension data path)*

**Expectations**

- What does success look like 90 days after launch? *(Aligns on measurable outcomes)*
- Who will own the health score model after handoff -- CS Ops, RevOps, or a CS manager? *(Identifies handoff recipient and training needs)*
- Are there specific accounts you'd want to test the model against as a sanity check? *(Lines up pilot validation candidates)*

### Information to Gather Before Implementation

**Data Access:**

Admin access to CS platform, CRM (Salesforce/HubSpot) with reporting permissions, product analytics platform read access, support system reporting access, billing system data export or API access

**Historical Data:**

Churn list for past 12-24 months with reason codes (if available), customer account list with segment/tier classifications, product usage data for at least 6 months, support ticket history by account

**Organizational:**

CSM-to-account assignments and book of business sizes, current QBR or touchpoint cadence by segment, existing intervention workflows or escalation paths, 2-3 CSMs available for pilot testing (mix of tenure levels)

### Approach Decision Questions

| Question     | Answer -&gt; Approach                                    |
| ------------ | ---------------------------------------------------- |
| How many customer segments need distinct scoring? | 1 = Quick-Start, 2-3 = Standard, 4+ = Enterprise |
| Is the CS platform already in production with data flowing? | Yes = Standard or Quick-Start, No = Prerequisite first |
| Do you have product analytics tracking in place? | Yes = Standard, No = Quick-Start with limited dimensions or data instrumentation phase |
| How many total accounts need scoring? | &lt;200 = Quick-Start, 200-2,000 = Standard, 2,000+ = Enterprise |
| Is there executive pressure for a quick win or thorough rollout? | Quick win = Quick-Start (iterate later), Thorough = Standard or Enterprise |

---

## 6) Overcoming Common Belief Barriers

#### "Our CSMs already know which accounts are at risk -- we don't need a score."

CSM intuition is a real and valuable signal, which is exactly why the health model includes CSM sentiment as one of its dimensions. But intuition alone has two problems: it doesn't scale (a CSM with 50+ accounts can't deeply know each one), and it isn't consistent (different CSMs assess the same signals differently). Companies using predictive analytics for retention see a 15-20% reduction in churn rates [3], not because the data replaces the CSM, but because it surfaces signals the CSM would otherwise miss.

**The reframe:** "We're not replacing CSM judgment -- we're giving them a co-pilot that watches all the signals they can't track manually across every account, every day."

#### "We don't have enough data to build a meaningful health score."

This is the most common reason companies delay, and it creates a catch-22: you won't build the score because you lack data, but you won't collect the right data without knowing what to score. The reality is you can start with 4 metrics -- login frequency, support tickets, renewal date proximity, and CSM sentiment -- and build from there [7]. Starting with an imperfect score that gets refined quarterly is far better than having no score while accounts silently churn.

**The reframe:** "Start with what you have. A 4-metric health score that's 70% accurate is infinitely more useful than a perfect score that never gets built."

#### "We tried a health score before and nobody used it."

Failed health scores almost always fail for one of two reasons. First, overcomplexity: teams build 20-30 variable models that no CSM can explain or trust [6]. Second, no defined action: the score exists but there's no playbook saying "when an account turns Red, do these three things within 48 hours." This project addresses both by keeping the model to 5-7 high-impact metrics and building intervention playbooks as part of the deliverable. See Implementation for the full enablement plan.

**The reframe:** "The score failed last time because it was too complex and had no action plan. We build simple scores with clear playbooks -- so CSMs know exactly what to do when a number changes."

#### "A single number can't capture the complexity of a customer relationship."

This objection is technically correct and practically irrelevant. The health score isn't a single number -- it's a weighted composite with multiple dimensions that can be drilled into. The aggregate score answers "which accounts need attention now?" The individual dimension scores answer "what's specifically wrong?" It's the same principle as a credit score: one number for prioritization, detailed factors for diagnosis.

**The reframe:** "The composite score tells you WHERE to look. The dimension breakdown tells you WHAT to fix. You need both, and that's exactly what this model provides."

| Objection Pattern | Root Cause | Counter-Evidence |
| ----------------- | ---------- | ---------------- |
| "We already know" | Overconfidence in intuition | Proactive analytics reduces churn 15-20% [3] |
| "Not enough data" | Perfectionism / analysis paralysis | 4 metrics is enough to start [7] |
| "Tried it, didn't work" | Past failure from overcomplexity | Simple models with action plans drive adoption |
| "Too simplistic" | Misunderstanding of composite scoring | Multi-dimension drill-down provides the complexity |

---

## 7) Metrics Impact & Success Measurement

### Power 10 Metrics Impacted

| Power 10 Metric | Impact Direction        | Expected Magnitude     | Notes                         |
| --------------- | ----------------------- | ---------------------- | ----------------------------- |
| Gross Retention Rate (GRR) | ↑ Increase | +3-8% within 12 months | Direct impact: proactive intervention prevents churn that reactive approaches miss. Companies using health scoring see 6-12 point NRR lift [1]. |
| Net Revenue Retention (NRR) | ↑ Increase | +5-12 points within 12 months | Combines churn reduction with expansion identification from Green accounts. Top B2B SaaS performers push NRR past 120% [5]. |
| Customer Acquisition Cost (CAC) | ↓ Indirect decrease | Indirect | Higher retention means less reliance on new logos to replace churned revenue, reducing effective CAC pressure. |

### Expected Outcomes

| Metric                 | Before          | After            | Source        |
| ---------------------- | --------------- | ---------------- | ------------- |
| Surprise churn rate (accounts that churn without Red flag 60+ days prior) | 40-60% of churn events are "surprises" | &lt;20% of churn events are unflagged | Health score alert system + intervention playbooks |
| CSM intervention response time | Days to weeks (reactive, triggered by customer complaint) | 24-48 hours (proactive, triggered by score threshold crossing) | Automated alerts in CS platform |
| Account health visibility | Anecdotal, CSM-dependent | Real-time dashboard with Red/Yellow/Green distribution | CS platform health score dashboard |
| Health score model accuracy | N/A (no score exists) | 70%+ accuracy against historical churn within 6 months | Retrospective validation against known churn events |
| QBR preparation time | 2-4 hours per account (manual data gathering) | 30-60 minutes per account (health score drill-down pre-populated) | Dashboard + dimension detail views |

### How to Measure Success

**Leading Indicators (Early signals, Week 1-4):**

- CSMs are logging into the health score dashboard daily (measured by platform analytics -- target: 80%+ daily active CSM usage within 2 weeks of launch)
- Intervention actions are being taken within 48 hours of Red score alerts (measured by playbook completion timestamps)
- CSMs provide feedback that health scores match their intuition for known accounts during pilot validation (qualitative signal)

**Lagging Indicators (Proof of success, Month 2-6):**

- Reduction in surprise churn (accounts that churned without being flagged Red 60+ days prior) by 50% within first 6 months
- Gross retention rate improves by 3-5 percentage points within 12 months
- Health score model accuracy exceeds 70% when validated against renewal and churn outcomes at the 6-month mark
- NRR improvement of 5-12 points as proactive intervention combines with expansion identification from Green accounts [1]

---

## References

[1] [Vitally - B2B SaaS Churn Rate Benchmarks 2025](https://www.vitally.io/post/saas-churn-benchmarks)
[2] [ChurnFree - B2B SaaS Benchmarks: A Complete Guide 2026](https://churnfree.com/blog/b2b-saas-churn-rate-benchmarks/)
[3] [Gartner - Customer Retention Strategies](https://www.gartner.com/en/digital-markets/insights/customer-retention-strategies)
[4] [Marketing LTB - Customer Retention Statistics 2025](https://marketingltb.com/blog/statistics/customer-retention-statistics/)
[5] [Velaris - Essential B2B SaaS Benchmarks Every CSM Should Track](https://www.velaris.io/articles/b2b-saas-benchmarks-key-metrics)
[6] [Gainsight - Customer Health Scoring: Misunderstandings, Myths &amp; Truths](https://www.gainsight.com/blog/customer-health-scoring/)
[7] [Vitally - How to Create a Customer Health Score with 4 Metrics](https://www.vitally.io/post/how-to-create-a-customer-health-score-with-four-metrics)
[8] [The CS Cafe - Best Customer Success Platforms 2025 Comparison](https://www.thecscafe.com/p/best-customer-success-platforms)
