# Customer Lifecycle — Methodology

This document covers the core concepts, frameworks, and calculations behind Customer Lifecycle. It provides the methodological foundation — the 'how it works' behind the execution steps.

---

## 1) Core Concepts

### Customer Lifecycle vs. Customer Journey

*What is it?*

The customer lifecycle is the structured, CRM-tracked progression of an account through defined stages from onboarding to retention and expansion. It is distinct from the customer journey, which describes the full experience a customer has with your product across every touchpoint. The lifecycle is an operational model; the journey is an experiential one.

*Why does it matter?*

Confusing these two concepts leads to CRM designs that try to track feelings rather than measurable states. The lifecycle gives CS and RevOps a concrete, automatable framework to manage accounts. The journey informs how you design experiences within each lifecycle stage. Both matter, but they serve different functions and belong in different systems.

*Key insight:*

> The lifecycle answers "where is this customer operationally?" The journey answers "how does this customer feel?" You need the lifecycle in your CRM to run the business; you need the journey map to improve the experience.

*Examples:*

| Context | Example |
|---------|---------|
| Lifecycle stage | Account is in "Adopting" stage because CSM marked onboarding complete and product usage exceeds threshold |
| Journey moment | Customer feels frustrated during onboarding because training sessions were rescheduled twice |
| How they connect | A customer stuck in "Onboarding" for 45+ days (lifecycle) signals a journey problem worth investigating |

*Common misunderstandings:*

- **Misconception:** The lifecycle and journey are the same thing, just different names.
  **Reality:** The lifecycle is a discrete set of CRM-tracked stages with explicit entry/exit criteria. The journey is continuous and overlapping. You can map journey moments to lifecycle stages, but they are not interchangeable.

- **Misconception:** You need to track the full customer journey in the CRM.
  **Reality:** Track lifecycle stages in the CRM. Use CS platforms (Gainsight, ChurnZero) or journey mapping tools for the experiential layer. Over-instrumenting the CRM with journey data creates fields nobody updates.

### Stage Mutual Exclusivity

*What is it?*

A design principle requiring that every customer account exists in exactly one lifecycle stage at any given time. A customer cannot be simultaneously "Onboarding" and "Adopting" -- stages are mutually exclusive and collectively exhaustive.

*Why does it matter?*

Without mutual exclusivity, funnel reporting breaks. If a customer can be in two stages at once, counts double, velocity metrics become meaningless, and automation logic conflicts. Every CS leader who has asked "how many customers are in onboarding?" and gotten three different answers has experienced this failure mode.

*Key insight:*

> If you cannot place every active customer into exactly one stage, your stage definitions overlap. Go back and tighten the entry/exit criteria until there is no ambiguity.

*Examples:*

| Context | Example |
|---------|---------|
| Correct design | Account moves from "Onboarding" to "Adopting" when CSM marks onboarding complete AND product usage exceeds 3 logins/week for 2 consecutive weeks |
| Incorrect design | Account is both "Onboarding" (because implementation is ongoing) and "Active" (because some users have started logging in) |
| Gray area | Multi-product customer where Product A is in "Adopting" and Product B is in "Onboarding" -- this requires a product-level lifecycle, not account-level |

### Time-in-Stage and Velocity

*What is it?*

Time-in-stage measures how long a customer spends in each lifecycle stage, calculated from stage entry timestamp to stage exit timestamp. Velocity is the rate at which customers move through the lifecycle funnel. Together, they form the quantitative backbone of lifecycle reporting.

*Why does it matter?*

Without timestamp data, CS leadership cannot identify bottlenecks. If the average time in "Onboarding" is 45 days but the target is 14 days, that gap represents delayed time-to-value, increased churn risk, and wasted CS capacity. Users who complete onboarding are 80% more likely to become long-term customers [1], so velocity through onboarding directly impacts retention.

*Key insight:*

> Stage timestamps are the most underinvested field type in CS CRM setups. They cost almost nothing to create but unlock the single most valuable metric for CS operations: where customers get stuck and for how long.

*The Framework:*

```
Stage Entry Date (auto-populated) --> Time-in-Stage = Exit Date - Entry Date --> Velocity Report
```

Each stage transition populates two dates: an exit date on the previous stage and an entry date on the new stage. Duration fields can be formula fields calculated from these timestamps.

*Common misunderstandings:*

- **Misconception:** You only need the current stage -- timestamps are nice-to-have.
  **Reality:** Without timestamps, you have a snapshot but no trend data. You cannot answer "is our onboarding getting faster or slower?" without historical stage dates.

- **Misconception:** Backfilling historical timestamps is easy.
  **Reality:** If you did not capture stage dates from the start, historical data is often unrecoverable. The earlier you implement timestamps, the more data you have.

### Entry/Exit Criteria

*What is it?*

Entry criteria define the specific, measurable conditions that must be true for a customer to enter a lifecycle stage. Exit criteria define the conditions that trigger movement to the next stage. Together, they form the business rules that govern stage transitions.

*Why does it matter?*

Vague criteria -- such as "customer is onboarded when they feel ready" -- lead to inconsistent stage assignments across CSMs, unreliable funnel data, and automation that cannot be built. Clear criteria enable automation, ensure consistency, and make stage definitions auditable.

*Key insight:*

> Every criterion must pass the "new CSM test": could a CSM in their first week determine whether this criterion is met by looking at CRM data alone, without asking a colleague?

*Examples:*

| Context | Example |
|---------|---------|
| Quantitative criterion | "Onboarding Complete" when product usage &gt; 3 logins/week for 2 consecutive weeks AND implementation checklist = 100% complete |
| Qualitative criterion with guardrails | "CSM marks onboarding complete" via guided screen flow that requires selecting a reason and confirming checklist completion |
| Mixed criterion | Closed Won opportunity (automatic) AND kickoff meeting scheduled (manual CSM confirmation) triggers entry into "Onboarding" |

### Automatic vs. Manual Transitions

*What is it?*

Lifecycle stages can transition automatically (triggered by CRM data meeting defined criteria) or manually (requiring a CSM or ops team member to update the stage). The design decision of which transitions are automatic vs. manual is a core architecture choice.

*Why does it matter?*

Fully automatic lifecycles sound ideal but ignore the reality that some transitions require human judgment. Fully manual lifecycles depend on CSM discipline and consistently decay. The right balance uses automation for clear, data-driven triggers and manual processes for judgment-based transitions -- with guardrails (guided flows, required fields) that make manual updates reliable.

*Key insight:*

> The question is not "can we automate this?" but "should we?" Automating a transition that requires CSM judgment creates false positives. Leaving a clear data-driven transition manual creates data lag.

*Common misunderstandings:*

- **Misconception:** More automation is always better.
  **Reality:** Automating the "At-Risk" to "Churned" transition without CSM review means you might mark accounts as churned that are in active renewal discussions. Automation should handle high-confidence, data-driven transitions. Human review should gate judgment calls.

- **Misconception:** Manual transitions will stay current if you train the team.
  **Reality:** Without enforcement mechanisms (guided flows, manager dashboards, inclusion in team metrics), manual stage updates decay within 60-90 days post-launch.

---

## 2) Decision Frameworks

### Approach Selection Matrix

| Situation | Recommended Approach | Why |
|-----------|---------------------|-----|
| Startup/early-stage, &lt;50 customers | Lightweight lifecycle (4 stages, mostly manual) | Low volume does not justify automation investment; iterate on definitions first |
| Growth stage, 50-500 customers, single product | Standard lifecycle (5-6 stages, mixed auto/manual) | Enough volume to need automation, simple enough for one lifecycle model |
| Scale stage, 500+ customers, multi-product | Advanced lifecycle (6+ stages, product-level tracking, mostly automated) | Volume demands automation; multi-product requires segmented lifecycle per product |
| CS platform already deployed (Gainsight, ChurnZero) | CS-platform-anchored lifecycle with CRM sync | Avoid duplicating lifecycle logic; use CS platform as source of truth for post-sale stages |
| No CS team / founder-led CS | Simplified lifecycle (3 stages: New, Active, Churned) | Complexity will not be maintained; start minimal and expand when CS team is hired |

### Scoping Factors

**1. Number of Active Customers**

- &lt;50 customers --> Manual lifecycle sufficient; focus on getting definitions right before automating
- 50-200 customers --> Mixed automation needed; automate clear triggers, keep judgment-based transitions manual
- 200+ customers --> Full automation required for data-driven transitions; manual processes become a bottleneck

**2. CRM Platform**

- Salesforce --> Use Flow Builder for automations, custom picklist + date fields on Account object, consider custom Lifecycle object for audit trail [2]
- HubSpot --> Use Workflows for automations, lifecycle stage property, pipeline feature for visual tracking
- Other CRM --> Evaluate automation capabilities; may need middleware (Zapier, Workato) for complex transition logic

**3. CS Platform Presence**

- No CS platform --> CRM is source of truth for all lifecycle stages; build everything in CRM
- CS platform deployed --> Determine source of truth per stage (typically: CRM for "New Customer" triggered by Closed Won; CS platform for "Onboarding" through "At-Risk"; CRM for "Churned")
- CS platform planned --> Design lifecycle in CRM now, but use field naming and architecture that supports future CS platform sync

**4. Product Complexity**

- Single product, simple onboarding --> 4-5 lifecycle stages sufficient; onboarding can be a single stage
- Single product, complex onboarding --> 5-6 stages; consider splitting onboarding into "Implementation" and "Training" sub-stages
- Multi-product --> Product-level lifecycle tracking needed; account-level lifecycle becomes a rollup of product lifecycles

**5. Existing Data Quality**

- Clean CRM data --> Can launch lifecycle with data migration to assign existing customers to stages
- Messy CRM data --> Need data cleanup phase before lifecycle rollout; inaccurate initial assignments undermine trust in the new system

### Standard Lifecycle (Recommended Default)

*Best for:*
- B2B SaaS companies with 50-500 customers
- Single product or simple product suite
- CS team of 3-15 CSMs
- Salesforce or HubSpot as CRM

*Not recommended for:*
- Companies with no formal CS function
- Multi-product companies needing product-level granularity
- Companies already running lifecycle in a CS platform (adapt, don't rebuild)

*Key differences from minimal lifecycle:*

| Aspect | Minimal (3-stage) | Standard (5-6 stage) |
|--------|-------------------|---------------------|
| Stages | New, Active, Churned | New Customer, Onboarding, Adopting, Healthy/Mature, At-Risk, Churned |
| Automation | None or basic | Mixed auto/manual transitions |
| Timestamps | Current stage only | Entry date per stage, duration calculations |
| Reporting | Customer count by stage | Funnel view, velocity metrics, bottleneck identification |
| Maintenance | Minimal | Requires quarterly review of stage definitions and criteria |

### Product-Level Lifecycle Approach

*Best for:*
- Multi-product B2B SaaS companies
- Companies where customers onboard products at different times
- Situations where account-level stage is misleading (e.g., account is "Healthy" on Product A but "At-Risk" on Product B)

*Not recommended for:*
- Single-product companies (unnecessary complexity)
- Companies where products are always sold and onboarded together

*Key differences from standard:*

| Aspect | Standard (Account-level) | Product-Level |
|--------|------------------------|---------------|
| Tracking object | Account | Custom junction object (Account-Product) |
| Stage assignment | One stage per account | One stage per account-product combination |
| Reporting | Single funnel | Funnel per product, rollup to account |
| Complexity | Moderate | High -- requires custom object and more automation |
| Account-level stage | Direct field | Derived from product-level stages (e.g., "worst" product stage drives account stage) |

---

## 3) Benchmarks & Standards

### How to Use Benchmarks

*Benchmarks are guidelines, not rules. Always:*
1. Start with benchmark as baseline
2. Adjust based on client-specific data
3. Validate against their actual numbers when available
4. Document deviations and rationale

### Customer Retention and Churn

| Metric | Low | Typical | High | Notes |
|--------|-----|---------|------|-------|
| Gross Revenue Retention (GRR) | &lt;85% | 90% | &gt;95% | KeyBanc 2024 survey median is ~90% [3] |
| Net Revenue Retention (NRR) | &lt;97% | 106% | &gt;118% | Median NRR for venture-backed SaaS is 106% (ChartMogul 2024, N=2,100) [4]; enterprise segment median is 118% [5] |
| Monthly logo churn | &gt;5% | 3.5% | &lt;2% | Average B2B SaaS monthly churn in 2025 is 3.5% [6] |
| Expansion revenue share | &lt;20% | 30-40% | &gt;50% | Top SaaS companies generate 50%+ of new ARR from existing customers [3] |

**Source:** KeyBanc Capital Markets & Sapphire Ventures 2024-2025 SaaS Survey [3]; ChartMogul SaaS Retention Report 2024 [4]; Optifai NRR Benchmark Analysis (939 companies) [5]

**Interpretation:**
- **Below low:** Signals significant customer value delivery problems. A lifecycle project may expose these issues but cannot fix them alone -- product and CS process improvements needed.
- **Above high:** Indicates strong post-sale operations. Lifecycle project should focus on maintaining and measuring what is already working, plus identifying expansion opportunities.

### Onboarding Velocity

| Metric | Low | Typical | High | Notes |
|--------|-----|---------|------|-------|
| Onboarding completion time (SMB) | &gt;30 days | 7-14 days | &lt;7 days | Most mid-market SaaS companies target 14 days [7] |
| Onboarding completion time (Enterprise) | &gt;90 days | 30-60 days | &lt;30 days | Enterprise implementations commonly run 30+ days |
| Onboarding completion rate | &lt;40% | 40-60% | &gt;70% | 40-60% is a good benchmark for B2B businesses [7] |
| Time-to-value impact on retention | -- | 80% more likely to retain | -- | Users who complete onboarding are 80% more likely to become long-term customers [1] |

**Source:** Dock.us Customer Onboarding Metrics [7]; Userpilot Time-to-Value Benchmark Report 2024 [1]

**Interpretation:**
- **Below low:** Onboarding is likely a churn driver. Lifecycle instrumentation will quantify the problem; the fix typically requires process redesign (see Implementation).
- **Above high:** Onboarding is a competitive advantage. Focus lifecycle tracking on measuring consistency and preventing regression.

### Lifecycle Stage Distribution

| Stage | Expected Distribution | Warning Signs |
|-------|----------------------|---------------|
| New Customer | 5-10% of active base | &gt;15% means onboarding is a bottleneck or stage is not transitioning |
| Onboarding | 10-20% | &gt;25% means customers are stuck; check entry/exit criteria and CSM capacity |
| Adopting | 15-25% | &lt;10% means the stage may be too narrowly defined or auto-transitions are too aggressive |
| Healthy/Mature | 40-60% | &lt;30% indicates systemic adoption or retention problems |
| At-Risk | 5-15% | &gt;20% requires immediate CS intervention review; &lt;3% may mean the at-risk criteria are too strict |
| Churned | Varies | Track trend, not absolute number; rising churn month-over-month is the real alert |

**Source:** Contextual reasoning based on B2B SaaS customer success operational patterns.

### Quick Reference Thresholds

| Question | Good | Warning | Red Flag |
|----------|------|---------|----------|
| How long are customers in Onboarding? | &lt;14 days (SMB), &lt;45 days (Enterprise) | 14-30 days (SMB), 45-75 days (Enterprise) | &gt;30 days (SMB), &gt;90 days (Enterprise) |
| What % of customers have a lifecycle stage assigned? | &gt;95% within 1 week of go-live | 80-95% | &lt;80% indicates adoption problems |
| Are CSMs updating manual transitions? | &gt;90% within SLA | 70-90% | &lt;70% means enforcement mechanism is needed |
| Is the funnel distribution stable week-over-week? | &lt;5% variance per stage | 5-10% variance | &gt;10% variance indicates automation or data quality issues |

---

## 4) Calculations & Scoring

### Formula Quick Reference

| Calculation | Formula | Example |
|-------------|---------|---------|
| Time-in-Stage | `Stage Exit Date - Stage Entry Date` | Entered Onboarding Jan 1, exited Jan 18 = 17 days |
| Stage Velocity | `Total customers exiting stage / Time period` | 30 customers exited Onboarding in January = 30/month velocity |
| Funnel Conversion Rate | `Customers entering next stage / Customers entering current stage` | 80 of 100 New Customers reached Onboarding = 80% conversion |
| Average Lifecycle Duration | `Sum(Time-in-Stage across all stages) / Customer count` | Average customer takes 120 days from New to Healthy |

### Time-in-Stage Calculation

**Formula:**
```
Time-in-Stage (days) = Stage_Exit_Date - Stage_Entry_Date
```

**Variables explained:**
- `Stage_Entry_Date` = Timestamp auto-populated when the customer enters a lifecycle stage (via automation or manual transition)
- `Stage_Exit_Date` = Timestamp auto-populated when the customer moves to the next stage

**Worked Example:**

```
Given:
- Onboarding_Entry_Date = 2025-03-01
- Onboarding_Exit_Date = 2025-03-22

Calculate:
- Time-in-Onboarding = 2025-03-22 - 2025-03-01 = 21 days
- Compare to benchmark: 14 days (SMB typical)
- Result: 7 days over benchmark -- investigate if implementation was delayed or CSM handoff was slow
```

**Validation:**
- This number should be positive (exit date after entry date). A negative number indicates a data quality problem (backdated entry or future-dated exit).
- If the value is 0, the customer transitioned the same day they entered -- verify this is not an automation firing incorrectly.

### Funnel Conversion Rate

**Formula:**
```
Stage Conversion Rate = (Customers who reached Stage N+1) / (Customers who entered Stage N) x 100
```

**Worked Example:**

```
Given:
- New Customers entered in Q1: 50
- Reached Onboarding: 48 (2 churned before onboarding started)
- Completed Onboarding (entered Adopting): 38
- Reached Healthy/Mature: 30

Calculate:
- New --> Onboarding: 48/50 = 96%
- Onboarding --> Adopting: 38/48 = 79%
- Adopting --> Healthy: 30/38 = 79%
- Overall Q1 funnel: 30/50 = 60% reach Healthy/Mature
```

**Validation:**
- Conversion rates below 70% at any stage indicate a bottleneck worth investigating.
- If New --> Onboarding is below 90%, there is likely a Sales-to-CS handoff problem (see Advisory for related scoping).

### NRR Connection to Lifecycle Data

Companies with strong retention (NRR &gt; 100%) grow almost 2.5x faster than their low-NRR counterparts [8]. While NRR is not directly calculated from lifecycle data, lifecycle instrumentation provides the underlying data to diagnose NRR problems.

**Connection to lifecycle stages:**

| NRR Component | Lifecycle Data Source |
|---------------|---------------------|
| Churn | Customers entering "Churned" stage / Total active customers |
| Contraction | Revenue decrease tracked at stage transitions (requires revenue field on Account) |
| Expansion | Revenue increase tracked when customer enters "Expansion" or upgrades product tier |
| Retention | Customers remaining in "Healthy/Mature" through renewal date |

---

## 5) Edge Cases & Deep Dives

### Edge Case 1: Multi-Product Customer with Staggered Onboarding

*Scenario:*

A customer purchases Product A on day 1, then adds Product B 6 months later. Product A is in "Healthy/Mature" while Product B is in "Onboarding." What lifecycle stage does the account sit in?

*Challenge:*

Account-level lifecycle cannot represent two simultaneous states. If you assign "Onboarding," your funnel report falsely shows a healthy customer as onboarding. If you assign "Healthy," the new product's onboarding gets no visibility.

*Approach:*

1. If multi-product is rare (&lt;10% of customers): Keep account-level lifecycle on the primary product. Track additional products via a separate field or notes. Accept the limitation.
2. If multi-product is common (&gt;10%): Build a product-level lifecycle using a custom junction object (Account-Product) with its own stage and timestamp fields. Roll up to an account-level "worst stage" summary field.
3. For the rollup, use a "worst stage wins" rule: if any product is At-Risk, the account shows At-Risk. If any product is Onboarding, the account shows Onboarding (unless another product is At-Risk).

*Key validation:*

Spot-check 10 multi-product accounts after implementation. Verify that the account-level stage accurately reflects the combined state of all products.

### Edge Case 2: Customer Re-Activation After Churn

*Scenario:*

A customer that previously churned returns as a new customer (signs a new contract). Should they re-enter the lifecycle as "New Customer" or skip to a later stage?

*Challenge:*

Re-activated customers have institutional knowledge of the product, so full onboarding may be unnecessary. But their CRM history shows previous lifecycle data that could confuse reporting.

*Approach:*

1. Create the lifecycle transition as "New Customer" to maintain funnel accuracy -- every new contract should enter at stage 1.
2. Add a boolean field "Returning Customer" (or "Re-Activation") on the Account to flag these accounts.
3. Build a filtered report that separates new-new customers from re-activated customers in velocity reporting.
4. CSM can fast-track through Onboarding if appropriate, but the stage progression should still be recorded for data integrity.

*Key validation:*

After 90 days, review re-activated accounts separately. Compare their onboarding velocity and adoption metrics against true new customers to determine if the fast-track process is working.

### Edge Case 3: Backward Stage Movement

*Scenario:*

A customer in "Healthy/Mature" shows declining usage and engagement signals. Should they move backward to "At-Risk?" What about a customer in "Adopting" who has a major implementation setback -- can they go back to "Onboarding?"

*Challenge:*

Allowing backward progression breaks velocity metrics and funnel accuracy. But real-world customer health fluctuates.

*Approach:*

1. **Do not move backward in the primary lifecycle.** The lifecycle is a forward-only funnel (New --> Onboarding --> Adopting --> Healthy --> At-Risk --> Churned). At-Risk is a forward stage, not a backward one.
2. **At-Risk is the catch-all for regression.** A customer in any active stage (Onboarding, Adopting, Healthy) can move forward to At-Risk. At-Risk can then transition forward to Churned or return forward to the recovery stage (Healthy).
3. **If you need to track regression detail**, add a "Regression Reason" field that populates when entering At-Risk, capturing which stage the customer came from and why.
4. Build validation rules in the CRM that prevent backward movement (e.g., cannot go from Adopting back to Onboarding).

*Key validation:*

Run a monthly report of At-Risk entries by source stage. If &gt;30% of At-Risk entries come from Onboarding or Adopting, the entry/exit criteria for those stages may need tightening.

### Edge Case 4: No Usage Data Available

*Scenario:*

The client does not have product usage analytics (no Mixpanel, Amplitude, or built-in telemetry). Entry/exit criteria cannot include usage-based triggers.

*Challenge:*

Most lifecycle frameworks assume usage data is available for automated transitions. Without it, criteria must rely on CSM judgment and proxy data, which are less reliable.

*Approach:*

1. Use proxy metrics available in CRM: support ticket volume, login frequency (if CRM-tracked), NPS/CSAT scores, contract utilization (seats used vs. purchased).
2. Default to CSM-driven transitions with guided screen flows that require the CSM to confirm specific milestones (training completed, key feature configured, etc.).
3. Add a recommendation to the handoff documentation: "Implement product usage tracking to enable automated lifecycle transitions in Phase 2."
4. Set up a review cadence (weekly or bi-weekly) where CSMs update lifecycle stages based on their customer knowledge.

*Key validation:*

Compare CSM-assigned stages against available proxy data quarterly. If CSMs are assigning "Healthy" to accounts with high support ticket volume or low engagement, recalibrate criteria.

### Edge Case 5: Data Migration for Existing Customers at Go-Live

*Scenario:*

You are launching the lifecycle for a company with 300 existing customers. These customers need to be assigned to lifecycle stages, but there is no historical data to determine their actual progression.

*Challenge:*

Assigning stages to existing customers is inherently imprecise. Historical timestamps cannot be reconstructed. The initial assignment will be a best-guess snapshot, not a true lifecycle progression.

*Approach:*

1. Build a decision tree for initial assignment based on available data:
   - Closed Won in last 30 days --> "New Customer"
   - Active implementation or training in progress --> "Onboarding"
   - Contract &gt;90 days old, usage above threshold --> "Healthy/Mature"
   - Contract &gt;90 days old, usage below threshold --> "Adopting"
   - Open churn risk flags or declining renewal likelihood --> "At-Risk"
   - Contract ended / not renewed --> "Churned"
2. Populate Stage_Entry_Date with the go-live date for all existing customers. Document that historical duration data is unavailable.
3. Run the assignment logic as a one-time data load, then have CSMs review their assigned accounts within 1 week and flag misassignments.
4. After correction, lock the initial assignments and begin tracking transitions going forward.

*Key validation:*

One week post-go-live, check that &gt;95% of active customers have a lifecycle stage assigned. Review the stage distribution against expected benchmarks. If &gt;40% of customers are in a single non-Healthy stage, the assignment criteria may need adjustment.

---

## References

[1] [Userpilot - Time-to-Value Benchmark Report 2024](https://userpilot.com/blog/time-to-value-benchmark-report-2024/)
[2] [Mastering Revenue Operations - Building a Customer Lifecycle Object in Salesforce](https://masteringrevenueoperations.com/p/building-a-customer-lifecycle-object)
[3] [KeyBanc Capital Markets & Sapphire Ventures - 2024-2025 SaaS Survey / Maxio 2025 Benchmarks Report](https://www.maxio.com/resources/2025-saas-benchmarks-report)
[4] [ChartMogul - The SaaS Retention Report: The New Normal For SaaS](https://chartmogul.com/reports/saas-retention-the-new-normal/)
[5] [Optifai - B2B SaaS NRR Benchmark: 97-118% by Segment (939 Companies)](https://optif.ai/learn/questions/b2b-saas-net-revenue-retention-benchmark/)
[6] [Vitally - B2B SaaS Churn Rate Benchmarks 2025](https://www.vitally.io/post/saas-churn-benchmarks)
[7] [Dock.us - Customer Onboarding Metrics: 14 Metrics, KPIs & Benchmarks](https://www.dock.us/library/customer-onboarding-metrics)
[8] [McKinsey - The Net Revenue Retention Advantage: Driving Success in B2B Tech](https://www.mckinsey.com/industries/technology-media-and-telecommunications/our-insights/the-net-revenue-retention-advantage-driving-success-in-b2b-tech)
