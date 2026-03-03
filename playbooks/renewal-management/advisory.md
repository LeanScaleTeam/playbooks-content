# Renewal Management — Advisory

Renewal Management - Proactive Retention Infrastructure for Recurring Revenue

---

## 1) Project Overview

### What is the name of this project?

Renewal Management - Proactive Retention Infrastructure for Recurring Revenue

### What is the purpose of this project?

This project builds the workflows, automation, health scoring, and reporting infrastructure needed to proactively manage customer renewals, reduce churn, and maximize recurring revenue retention (GRR/NRR). The client ends up with a renewal engine that provides 90-day forward visibility, automated health-based alerts, standardized CSM playbooks, and real-time dashboards showing renewal pipeline and risk accounts.

**Core transformation:** From reactive firefighting where renewals are discovered at invoice time (or after churn) to a predictable, data-driven retention machine with full pipeline visibility and proactive intervention workflows.

### What Renewal Management Unlocks

After this project is complete, the CS organization can:

- See every upcoming renewal 90 days out with owner, value, and health status in a single view
- Receive automated alerts at 90/60/30-day intervals with specific CSM actions at each stage
- Score account health using product usage, support signals, and engagement data to predict churn risk
- Run standardized renewal conversations with playbooks, talk tracks, and objection handling
- Intervene proactively on at-risk accounts before the renewal window opens
- Report on renewal pipeline value, risk distribution, and CSM workload in real time
- Identify expansion opportunities during the renewal process

| Before | After |
| ------ | ----- |
| Renewals discovered at invoice time or after churn | 90-day forward visibility with automated alerts |
| Health signals scattered across tools, no single score | Composite health score combining usage, support, and engagement |
| No standardized renewal process; each CSM does it differently | Documented CSM playbook with templates, cadence, and escalation paths |
| No ownership model; renewals fall through the cracks | Every renewal assigned an owner with required accountability |
| Reactive firefighting on at-risk accounts | Proactive intervention workflows triggered by health score changes |
| Renewal outcomes unknown until quarter-end | Real-time dashboard showing pipeline, risk, and forecast |

### What business outcomes does this project drive?

**Primary Outcomes:**

- Improved Gross Revenue Retention (GRR) by 3-5 percentage points within two renewal cycles
- Near-zero surprise churn (accounts that churn without prior risk flagging)
- 100% renewal ownership coverage with 90-day alert accuracy
- Reduced time-to-action on at-risk accounts from weeks to hours

**Secondary Outcomes:**

- Foundation for expansion revenue motions (upsell/cross-sell identification during renewals)
- Data-driven input for CS capacity planning and territory design
- Accurate renewal forecasting for finance and board reporting
- Baseline GRR/NRR metrics that enable future improvement measurement

### Who in the Org can benefit from this project?

VP of Customer Success, Head of CS Operations, Customer Success Managers, RevOps Manager, VP Finance, CEO/CRO (for retention reporting and forecasting)

### Pain Points this Project Solves

The project is foundational infrastructure that enables predictable retention management. The specific pain it solves depends on where the client is losing renewals today.

| Pain Point | What Renewal Management Enables |
| ---------- | -------------------------------- |
| "We only find out about renewals when the invoice arrives" | 90-day automated visibility with staged alerts at 90/60/30 days |
| "We don't know which accounts are at risk until they cancel" | Health scoring that flags declining accounts before renewal window |
| "Every CSM handles renewals differently" | Standardized playbook with templates, talk tracks, and escalation paths |
| "Nobody owns the renewal and things fall through the cracks" | Required renewal owner assignment with accountability tracking |
| "We can't forecast retention or plan CS capacity" | Real-time renewal pipeline dashboard with risk distribution and CSM workload |
| "We're reactive on churn instead of getting ahead of it" | Proactive intervention workflows triggered by health score thresholds |

### The Data Behind the Problem

The financial case for proactive renewal management is well-established:

- Acquiring a new customer costs 5-25x more than retaining an existing one [1]. A 5% increase in customer retention can increase profits by 25-95% [1].
- The median Gross Revenue Retention for B2B SaaS companies is 90%, with top-quartile companies exceeding 95% [2]. Companies below 90% GRR are losing ground to peers.
- The average annual B2B SaaS churn rate is approximately 4.9% [3]. For a $10M ARR company, that represents $490K in annual lost revenue before accounting for the cost to replace it.
- Involuntary churn (payment failures, missed renewals) can represent 20-40% of total churn and is entirely preventable with proper systems [4].
- AI-enhanced customer health scores can predict churn 3-6 months in advance with 85%+ accuracy [5], giving CS teams the lead time needed to intervene.
- 84% of B2B software buyers cite excellent customer support as a key factor in renewal decisions [3].

### Key Metaphors or Frameworks

**The Weather Forecast Metaphor:** Renewal management without health scoring is like running a city without a weather forecast. You only know about the storm when it hits. Health scores are the forecast: they give you lead time to prepare, evacuate (escalate), or reinforce (intervene). The 90/60/30-day cadence is the forecast window: 90 days out you see the system forming, 60 days you track its path, 30 days you execute the response plan.

Use this metaphor when clients say "we already know our accounts." The response: "You know them today. The question is whether you can see what's coming 90 days from now."

Do NOT use this metaphor with clients who have already built health scoring but lack the workflow layer. For those clients, the framing is about operationalizing the data they already have.

### Target Motion

This project is designed for Sales-Led Growth (SLG) and hybrid SLG/PLG B2B SaaS companies with recurring revenue models (annual or multi-year contracts). It is most applicable to companies with 50+ customers and a dedicated CS function.

Not a fit for: Pure PLG companies with self-serve churn/renewal (they need product-led retention, not CSM-driven renewal management). Also not a fit for companies with fewer than 20 customers, where a spreadsheet-based approach is sufficient and the overhead of automation is not justified.

---

## 2) Tools & Systems

### Primary Tools

**Salesforce**

CRM platform where renewal tracking objects, health score fields, automated alert workflows, and renewal pipeline dashboards are built. Used as the system of record for renewal dates, contract values, renewal owners, and health status. Supports formula fields for health score calculation and Flow for alert automation.

**HubSpot**

Alternative CRM platform for clients not on Salesforce. Uses custom Deal properties for renewal tracking, calculated properties for health scoring, and Workflows for automated alerts. Service Hub provides additional support ticket data for health score inputs.

**Gainsight**

Dedicated Customer Success Platform that sits on top of Salesforce. Provides native health scoring with machine learning, renewal center for pipeline management, playbook automation (CTAs), and advanced reporting. Recommended for clients with 200+ accounts who need sophisticated health scoring and CS workflow automation.

**ChurnZero**

Alternative CS platform with strong in-app engagement tracking. Offers fully customizable health scores with unlimited score definitions, renewal forecasting, and automated playbook triggers. Strong fit for product-led or hybrid motion clients who need product usage signals deeply integrated into health scoring.

**Data Providers (if applicable):**

- Product usage analytics: Pendo, Mixpanel, Amplitude, or native product analytics
- Support data: Zendesk, Intercom, Freshdesk, Salesforce Service Cloud
- Survey data: Delighted, SurveyMonkey, Salesforce Surveys
- Communication tracking: Gong (for engagement signals), Outreach/Salesloft (for email engagement)

---

## 3) Stakeholders & Roles

### Client-Side Stakeholders

**VP of Customer Success (Executive Sponsor)**

- Required for: Kickoff, requirements alignment, playbook approval, sign-off checkpoints
- Responsibilities: Defines renewal process requirements, approves health score methodology, owns adoption post-launch

**CS Operations Manager (Technical Owner)**

- Required for: All phases -- primary day-to-day contact
- Responsibilities: Provides CRM access, coordinates data source integrations, manages CSM training logistics, owns system maintenance post-handoff

**CSM Team Leads (Input Providers)**

- Required for: Discovery interviews, playbook co-design, training sessions, pilot testing
- Responsibilities: Provide current-state workflow input, validate health score accuracy, test renewal playbooks with live accounts

**RevOps Manager (Input Provider)**

- Required for: Data architecture review, CRM configuration alignment, reporting requirements
- Responsibilities: Ensures renewal tracking aligns with existing CRM architecture and reporting standards

**Finance Lead (Input Provider)**

- Required for: Baseline metrics calculation, renewal forecast alignment
- Responsibilities: Provides contract data, validates GRR/NRR calculations, aligns on renewal forecast reporting format

### Technical Owners

**CS Operations Manager**

- Owns health score configuration and ongoing weight adjustments
- Manages alert workflow logic and escalation thresholds
- Maintains renewal pipeline dashboard and reporting cadence
- Handles new account onboarding into renewal tracking system

**RevOps Manager (If Separate)**

- When this role is needed: When CS Ops does not have CRM admin access or when renewal data must align with broader revenue reporting
- Handles CRM custom object creation, field-level security, and data integration configurations

**Enterprise Considerations (If Applicable)**

- IT Security review may be required for CS platform (Gainsight/ChurnZero) procurement and data access
- Multi-region deployments may require separate health score models per region
- Shared service CS teams may need additional routing logic for renewal owner assignment

---

## 4) Scoping

### Scoping Factors

**1. Customer Base Size**

- Under 50 accounts -- Simple CRM views and manual alerts may suffice; full automation may not justify the investment
- 50-200 accounts -- Standard project scope; CRM-native health scoring and alert automation
- 200+ accounts -- Dedicated CS platform (Gainsight, ChurnZero) recommended; increases scope by 20-30 hours for platform configuration

**2. CRM Platform**

- Salesforce -- Full flexibility with custom objects, formula fields, and Flow Builder; most integrations available
- HubSpot -- Requires Professional/Enterprise tier; calculated properties are less flexible than Salesforce formula fields
- Other CRM -- May require significant workarounds or external tooling; adds 10-20 hours

**3. Health Signal Data Sources**

- CRM-only signals (engagement, support cases) -- Lower complexity; 2-3 integrations
- Product usage data available via API -- Moderate complexity; requires integration build (Segment, Pendo, Mixpanel)
- Product usage requires manual export -- Higher complexity; manual process until integration is built
- No product usage data -- Health score is limited to engagement and support signals; less predictive

**4. Contract Complexity**

- Standard annual contracts -- Straightforward renewal date tracking
- Multi-year with co-term dates -- Requires contract hierarchy logic
- Usage-based or consumption pricing -- Renewal value is variable; requires consumption-based forecasting
- Mix of contract types -- Requires segmented renewal workflows and dashboard views

**5. Existing CS Tooling**

- No CS platform (CRM only) -- Build everything in CRM; full project scope
- CS platform already deployed -- Focus on configuration and process design; reduce build hours by 20-30%
- CS platform being evaluated -- Project may include platform selection advisory; adds 10-15 hours

**6. CS Team Maturity**

- New CS function (under 1 year) -- Heavier emphasis on process design and playbook development
- Established CS team with ad hoc processes -- Focus on standardization and automation
- Mature CS org seeking optimization -- Focus on health score refinement and advanced reporting

### Multiple Approaches

**Approach 1: CRM-Native Build**

- Criteria: Under 200 accounts, no CS platform budget, Salesforce or HubSpot Enterprise
- Execution: Build renewal tracking, health scoring, alerts, and dashboards entirely within the CRM. Lower tool cost but more manual maintenance. See Methodology for health score design within CRM constraints.

**Approach 2: CS Platform Implementation**

- Criteria: 200+ accounts, budget for Gainsight/ChurnZero/Totango, need for advanced health scoring with ML
- Execution: Deploy CS platform on top of CRM, configure native health scoring and renewal management modules, build playbook automation (CTAs). Higher tool cost but more scalable and lower maintenance. See Implementation for platform-specific build steps.

**Approach 3: Hybrid (CRM + Lightweight Automation)**

- Criteria: 50-200 accounts, want more than CRM-native but not ready for a full CS platform
- Execution: Build core renewal tracking in CRM, add lightweight health scoring with a tool like Vitally or Planhat, use Slack/email integrations for alerts. Balance of cost and capability.

---

## 5) Discovery Questions

### Questions for Project Kickoff

**Business Context**

- What is your current GRR and NRR? If unknown, what data exists to calculate them? *(Establishes baseline and urgency)*
- How many active customers do you have, and what is the distribution by segment (Enterprise/Mid-Market/SMB)? *(Drives approach and complexity)*
- What percentage of your revenue comes from renewals vs. new logos? *(Quantifies renewal importance)*
- Have you experienced any churn spikes recently? What do you attribute them to? *(Identifies root causes)*

**Current State**

- How are renewals currently tracked? (CRM field, spreadsheet, calendar reminders, nothing) *(Determines gap size)*
- Who owns the renewal process today? Is it the CSM, account owner, or unassigned? *(Identifies ownership gaps)*
- Walk me through what happens when a renewal is 90 days away. What about 30 days? *(Maps current workflow)*
- When was the last time a renewal was missed or discovered late? What happened? *(Surfaces real pain)*
- Do you have any customer health tracking today? If so, what signals do you use? *(Determines health score starting point)*

**Technical Environment**

- What CRM are you on, and what tier/edition? *(Determines build approach)*
- Where does product usage data live? Is it accessible via API? *(Determines health score signal availability)*
- What support platform do you use? Can we pull ticket data into CRM? *(Health score input)*
- Do you have a CS platform (Gainsight, ChurnZero, etc.) deployed or under evaluation? *(Determines tooling approach)*
- Are there existing automations or workflows in CRM that might conflict? *(Avoids build conflicts)*

**Expectations**

- What does "success" look like 90 days after launch? *(Aligns on measurable outcomes)*
- Which segments or account types are highest priority for renewal management? *(Enables phased rollout)*
- How much CSM time per week can be dedicated to the new process during rollout? *(Gauges adoption capacity)*
- Is there executive sponsorship for enforcing the new renewal process? *(Predicts adoption risk)*

### Information to Gather Before Implementation

**Contract Data:**

Complete list of active customers with contract end dates, ARR values, contract type (annual/multi-year/usage-based), and auto-renewal clauses. Must be exported from CRM or billing system in CSV format with at minimum: Account Name, Contract End Date, ARR/ACV, Contract Type, Current Owner.

**Historical Churn Data:**

Last 12 months of churned accounts with churn date, churn reason (if documented), ARR at churn, and segment. Needed for baseline GRR/NRR calculation and health score validation.

**System Access:**

CRM admin credentials, support platform read access, product analytics read access (if available), CS platform admin access (if deployed). All integrations should be documented with API keys or OAuth configurations.

**Stakeholder Availability:**

CS leadership available for 2-3 hours during requirements phase. 2-3 CSMs available for 30-minute discovery interviews. CS Ops or RevOps available for 4-6 hours/week during build phase.

### Approach Decision Questions

| Question | Answer --&gt; Approach |
| -------- | ------------------- |
| How many active customers? | Under 200 = CRM-Native, 200+ = CS Platform, 50-200 with budget constraints = Hybrid |
| Is a CS platform deployed or budgeted? | Yes = CS Platform approach, No = CRM-Native or Hybrid |
| Is product usage data available via API? | Yes = Full health scoring, No = Engagement + support signals only |
| What CRM tier are you on? | SF Enterprise+ or HubSpot Enterprise = Full build, HubSpot Pro = Limited automation |
| How complex are your contract structures? | Standard annual = Simple, Mixed/usage-based = Add 15-20 hours for contract logic |

---

## 6) Overcoming Common Belief Barriers

#### "We already track renewals in a spreadsheet -- this is overkill."

Spreadsheets are where renewal management starts, and they work fine for the first 20-30 accounts. The problem is what happens at scale: spreadsheets do not send alerts, do not update automatically when contract dates change, and do not surface health signals. A CS leader managing 100+ renewals in a spreadsheet is spending 3-5 hours per week on manual data entry and status updates that an automated system handles in zero hours. More importantly, spreadsheets create single-point-of-failure risk: if the person maintaining the spreadsheet is out, renewals get missed.

**The reframe:** "The spreadsheet got you here. The question is whether it can get you through the next 12 months of growth without a missed renewal costing you a six-figure account."

#### "Our CSMs know their accounts -- they don't need a system to tell them who's at risk."

CSM intuition is valuable and should be a health score input (CSM pulse score). But intuition does not scale: a CSM managing 30 accounts cannot track login frequency trends, support ticket patterns, and engagement changes across all 30 simultaneously. Research shows that data-driven health scores identify at-risk accounts that CSMs rate as "healthy" 15-20% of the time, because declining usage patterns happen gradually and are invisible without trend data [5]. The system does not replace CSM judgment; it gives CSMs data they cannot track manually.

**The reframe:** "Your CSMs are the experts. This gives them X-ray vision -- the data behind the gut feeling."

#### "We should be focused on growth, not retention."

This is the most expensive misconception in B2B SaaS. Bain &amp; Company research shows that acquiring a new customer costs 5-25x more than retaining one, and a 5% improvement in retention increases profits by 25-95% [1]. For a $10M ARR company with 90% GRR, improving to 95% GRR is equivalent to closing $500K in new-logo revenue -- without the sales cycle, onboarding cost, or time-to-value delay. Growth without retention is a leaky bucket: you pour more in, but the water level stays the same.

| Scenario | Impact on ARR (Year 1) |
| -------- | ---------------------- |
| $10M ARR with 85% GRR (no change) | $8.5M retained + new logos |
| $10M ARR with 90% GRR (+5pts) | $9.0M retained + new logos |
| $10M ARR with 95% GRR (+10pts) | $9.5M retained + new logos |

**The reframe:** "Growth and retention aren't either/or. Retention is what makes growth investments compound instead of leak."

#### "We tried this before and it didn't work."

Past failures in renewal management usually stem from one of three root causes: (1) alerts without context (CSMs got tasks with no health data or action guidance), (2) no ownership model (alerts fired but nobody was accountable), or (3) the system was built without CSM input (so the team ignored it). This project addresses all three by co-designing the playbook with CSMs, building health-context into every alert, and enforcing renewal ownership as a required field. See Implementation for the specific co-design process and pilot testing approach.

**The reframe:** "The last attempt told you what not to do. This project is designed around those lessons."

---

## 7) Metrics Impact & Success Measurement

### Power 10 Metrics Impacted

| Power 10 Metric | Impact Direction | Expected Magnitude | Notes |
| --------------- | ---------------- | ------------------ | ----- |
| Gross Revenue Retention (GRR) | Increase | +3-5 percentage points | Direct impact: fewer missed renewals and proactive churn intervention |
| Net Revenue Retention (NRR) | Increase | +5-10 percentage points | Indirect: renewal conversations surface expansion opportunities |
| Customer Lifetime Value (LTV) | Increase | +15-25% | Higher retention rates compound LTV over multiple renewal cycles |
| CAC Payback Period | Decrease | Shorter by 1-3 months | Retained revenue reaches payback faster than replacement new-logo |

### Expected Outcomes

| Metric | Before | After | Source |
| ------ | ------ | ----- | ------ |
| Renewal visibility window | 0-30 days (reactive) | 90 days (proactive) | Project design |
| Renewal ownership coverage | 60-70% (many unassigned) | 100% (required field) | Project design |
| Surprise churn rate (no prior risk flag) | 30-50% of churned accounts | Under 5% of churned accounts | Health score accuracy [5] |
| CSM time on renewal admin | 3-5 hours/week manual tracking | Under 1 hour/week (automated) | Automation ROI |
| GRR | Median 90% for B2B SaaS [2] | Target 93-95% | Benchmarkit 2024 [2] |
| At-risk account identification lead time | Days (or after the fact) | 3-6 months with health scoring [5] | Health score research |

### How to Measure Success

**Leading Indicators (Early signals, Week 1-4):**

- 100% of active customers have a renewal date, renewal owner, and health score populated in CRM
- 90/60/30-day alerts are firing accurately for upcoming renewals (validated against a test cohort)
- CSMs are completing alert-triggered tasks within SLA (e.g., 48 hours for 90-day tasks)
- Weekly renewal pipeline review meetings are occurring with documented actions

**Lagging Indicators (Proof of success, Month 2-6):**

- Gross Revenue Retention (GRR) improves by 3-5 percentage points vs. pre-project baseline
- Surprise churn (accounts that churned with no prior risk flag) drops to near zero
- Renewal forecast accuracy within 5% of actual (renewals closed vs. pipeline value)
- Health score accuracy validated: 80%+ of accounts flagged "at-risk" either churn or require intervention
- CSM adoption rate above 90% (measured by task completion rates and playbook usage)

---

## References

[1] [HBR - The Value of Keeping the Right Customers](https://hbr.org/2014/10/the-value-of-keeping-the-right-customers)
[2] [Benchmarkit - 2024 SaaS Performance Metrics](https://www.benchmarkit.ai/2024benchmarks)
[3] [Vitally - B2B SaaS Churn Rate Benchmarks 2025](https://www.vitally.io/post/saas-churn-benchmarks)
[4] [ChurnBuster - Full Guide to B2B SaaS Churn Rate Management](https://churnbuster.io/articles/b2b-saas-churn-rate)
[5] [Gainsight - Customer Health Scores Explained](https://www.gainsight.com/blog/customer-health-scores/)
