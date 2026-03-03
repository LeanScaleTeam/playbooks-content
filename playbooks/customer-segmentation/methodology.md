# Customer Segmentation — Methodology

This document covers the core concepts, frameworks, and calculations behind Customer Segmentation. It provides the methodological foundation — the 'how it works' behind the execution steps.

---

## 1) Core Concepts

### Segmentation vs. Categorization

*What is it?*

Segmentation is the practice of dividing a customer base into distinct groups that share meaningful characteristics and then mapping those groups to differentiated operational actions. Categorization is simply tagging records with labels. The difference: segmentation without action is just categorization.

*Why does it matter?*

Companies that execute personalized strategies based on segments generate 10-15% more revenue than those using one-size-fits-all approaches, with top performers reaching up to 25% revenue lift [1]. If segments exist in the CRM but do not drive different treatment -- different QBR cadence, different service levels, different playbooks -- they are categorization, not segmentation.

*Key insight:*

> Every segment must answer two questions: "Who is in this group?" and "What do we do differently for them?" If you cannot answer the second question, the segment does not belong in your model.

*Examples:*

| Context | Example |
|---------|---------|
| Segment with action | Enterprise accounts ($100K+ ARR) get a dedicated CSM, monthly executive check-ins, and custom QBRs |
| Segment with action | Mid-market accounts ($25K-$100K ARR) get pooled CSM coverage, quarterly business reviews, and automated onboarding flows |
| Category without action | Accounts tagged as "Healthcare" in CRM but receiving identical treatment to every other industry |

*Common misunderstandings:*

- **Misconception:** More segments mean better segmentation.
  **Reality:** Over-segmentation creates micro-segments too small to be statistically meaningful or operationally actionable. Aim for 3-5 dimensions with 3-5 values each [2].

- **Misconception:** Segmentation is a one-time project.
  **Reality:** Segments must be re-evaluated as customer data changes. Static segments become stale within one quarter. Automated assignment rules that re-evaluate on data changes are required.

---

### The Three Segmentation Dimensions

*What is it?*

Customer segmentation in B2B SaaS operates across three primary dimensions, each answering a different question about the customer:

1. **Firmographic** -- Who is this company? (industry, size, geography, growth stage)
2. **Behavioral** -- How does this company use our product? (login frequency, feature adoption, support ticket volume, engagement scores)
3. **Value-Based** -- What is this company worth to us? (ARR, expansion potential, strategic importance, lifetime value)

*Why does it matter?*

Each dimension serves different operational needs. Firmographic segmentation drives resource allocation and go-to-market strategy. Behavioral segmentation drives retention and adoption plays. Value-based segmentation drives prioritization and service-level decisions. Most effective segmentation models combine at least two dimensions [3].

*The Framework:*

```
FIRMOGRAPHIC (Who are they?)        BEHAVIORAL (How do they engage?)       VALUE-BASED (What are they worth?)
├── Industry                        ├── Product Usage Frequency             ├── Current ARR
├── Employee Count / Revenue        ├── Feature Adoption Depth              ├── Expansion Potential
├── Geography / Region              ├── Support Ticket Volume               ├── Strategic / Logo Value
├── Growth Stage                    ├── Engagement Score (CSP)              ├── Contract Length / Stickiness
└── Tech Stack                      └── NPS / Satisfaction                  └── Referral / Advocacy Value
```

*Common misunderstandings:*

- **Misconception:** Firmographic segmentation alone is sufficient.
  **Reality:** Firmographics tell you who the customer is, not how healthy the relationship is. Two $50K ARR accounts in the same industry can have completely different churn risk depending on usage patterns. Combining firmographic and behavioral dimensions is where segmentation becomes predictive.

- **Misconception:** Behavioral segmentation requires a Customer Success Platform.
  **Reality:** Basic behavioral signals (support tickets, login data, renewal dates) can be pulled from CRM and support systems. A CSP like Gainsight, ChurnZero, or Vitally adds depth but is not a prerequisite for v1 behavioral segmentation.

---

### Service Model Mapping (High-Touch, Low-Touch, Tech-Touch)

*What is it?*

Service model mapping is the practice of aligning each customer segment to a specific engagement model that defines how the CS team interacts with those accounts. The three standard models form a spectrum from fully personalized human interaction to fully automated digital engagement [4]:

- **High-Touch:** Dedicated CSM, personalized onboarding, monthly executive check-ins, custom QBRs. Typical ratio: 15-50 accounts per CSM.
- **Low-Touch:** Pooled CSM coverage, templated onboarding, quarterly check-ins, group webinars. Typical ratio: 50-200 accounts per CSM.
- **Tech-Touch (Digital):** Automated onboarding sequences, in-app guidance, self-serve resources, automated health alerts. Typical ratio: 200-1,000+ accounts per CSM.

*Why does it matter?*

Without service model mapping, segmentation is an intellectual exercise. The service model is the operational translation of "what do we do differently." It determines headcount planning, CS tool requirements, and content needs. Companies that segment their CS engagement model see a 6-12 point lift in net revenue retention [5].

*Key insight:*

> The service model is not about how much you care about a customer -- it is about how you deliver value at the right cost. A well-designed tech-touch program can achieve higher NPS than a poorly executed high-touch model.

*Examples:*

| Segment | Service Model | What Changes |
|---------|--------------|--------------|
| Enterprise ($100K+ ARR) | High-Touch | Dedicated CSM, custom success plan, monthly executive sync, on-site QBR option |
| Mid-Market ($25K-$100K ARR) | Low-Touch | Pooled CSM, templated success plan, quarterly business review, email-based check-ins |
| SMB (&lt; $25K ARR) | Tech-Touch | Automated onboarding, in-app walkthroughs, self-serve knowledge base, triggered email sequences |

---

### Segment Governance

*What is it?*

Segment governance is the set of processes that keep segments accurate, current, and operationally useful over time. It covers who owns segment definitions, how often they are reviewed, and what happens when a customer crosses a segment boundary.

*Why does it matter?*

Segments decay. Customers grow, shrink, change industries (via acquisition), and shift usage patterns. Without governance, segment assignments drift from reality. A quarterly review cadence is the minimum; automated re-evaluation on data changes is the target state.

*The Framework:*

| Governance Component | Cadence | Owner |
|---------------------|---------|-------|
| Segment definition review | Quarterly | VP CS + CS Ops |
| Data quality audit (field completeness) | Monthly | RevOps / CS Ops |
| Automated assignment rule validation | Quarterly | RevOps |
| Segment distribution sanity check | Monthly | CS Ops |
| Service model threshold review | Semi-annually | VP CS + Finance |

*Common misunderstandings:*

- **Misconception:** Once segments are built, they maintain themselves.
  **Reality:** Even with automation, governance is needed. New products, pricing changes, and M&A activity all require segment model updates. Assign an explicit owner.

- **Misconception:** Data quality is someone else's problem.
  **Reality:** Garbage in, garbage out. If the industry field is 40% blank and 20% inaccurate, firmographic segmentation will misclassify a third of your accounts. Data cleanup and enrichment are prerequisites, not nice-to-haves.

---

## 2) Decision Frameworks

### Approach Selection Matrix

| Situation | Recommended Approach | Why |
|-----------|---------------------|-----|
| Early-stage CS team, &lt;200 customers, limited data | Firmographic-only (value-based tiers) | Fast to implement, requires only CRM data, delivers 80% of the value |
| Established CS team with CSP, 200-2,000 customers | Firmographic + Behavioral composite | Adds predictive power, CSP provides behavioral data, manageable complexity |
| Mature CS org, 2,000+ customers, multiple products | Multi-dimensional (Firmographic + Behavioral + Value-based) | Scale requires nuance, different products may have different segments |
| PLG / self-serve heavy, high-volume low-ARR base | Behavioral-first with value overlay | Usage data is the primary signal, firmographics are secondary |
| CS team with no Customer Success Platform | Firmographic + basic behavioral (from CRM/support data) | Don't let tool gaps block progress; use what you have |

### Scoping Factors

**1. Customer Base Size**

- &lt; 200 customers --> Simple 3-tier model (e.g., Enterprise / Mid-Market / SMB) is sufficient. Manual segment assignment is feasible.
- 200-2,000 customers --> Automation required. 3-5 dimensions with automated assignment rules.
- 2,000+ customers --> Full automation required. Consider product-line-specific segmentation layers.

**2. Data Maturity**

- Low (&lt; 60% field completeness) --> Start with data cleanup and enrichment. Build firmographic-only segments as a baseline while enriching.
- Medium (60-85% completeness) --> Firmographic + basic behavioral segmentation feasible. Plan enrichment for remaining gaps.
- High (85%+ completeness) --> Full multi-dimensional segmentation. Focus on behavioral and value-based dimensions for differentiation.

**3. CS Tool Stack**

- CRM only (Salesforce / HubSpot) --> Firmographic + value-based segmentation. Limited behavioral data (support cases, activity history).
- CRM + enrichment tool (ZoomInfo, Apollo, Clay) --> Strong firmographic segmentation. Enrichment fills data gaps.
- CRM + CSP (Gainsight, ChurnZero, Vitally) --> Full behavioral segmentation. Health scores, usage data, engagement metrics available.
- CRM + CSP + BI tool (Looker, Tableau) --> Advanced analytics. Predictive segmentation, cohort analysis, segment performance dashboards.

**4. Number of Products / Business Units**

- Single product --> One segmentation model for the entire customer base.
- Multiple products --> Consider product-specific behavioral layers on top of a shared firmographic base. A customer may be Enterprise for Product A but Mid-Market for Product B.

### Firmographic-Only Approach

*Best for:*
- Early-stage CS teams building their first segmentation model
- Companies with limited behavioral data (no CSP, minimal product analytics)
- Quick wins: can be implemented in 1-2 weeks

*Not recommended for:*
- Mature CS orgs where all customers already have basic firmographic tags (the value is in behavioral/value-based differentiation)
- PLG companies where usage behavior is the primary signal

*Key differences from standard:*

| Aspect | Standard (Multi-Dimensional) | Firmographic-Only |
|--------|------------------------------|-------------------|
| Data requirements | CRM + CSP + enrichment | CRM + enrichment (optional) |
| Implementation time | 4-8 weeks | 1-2 weeks |
| Predictive power | High (behavioral signals predict churn) | Moderate (descriptive, not predictive) |
| Maintenance burden | Higher (more data sources to keep current) | Lower (firmographic data changes slowly) |

### Composite Multi-Dimensional Approach

*Best for:*
- Companies with 500+ customers and a CSP in place
- CS orgs that need to differentiate service models beyond simple ARR tiers
- Situations where firmographic peers have very different health profiles

*Not recommended for:*
- Teams without clean foundational data (fix data quality first)
- Organizations that have not yet operationalized their existing segments

*Key differences from standard:*

| Aspect | Firmographic-Only | Composite |
|--------|-------------------|-----------|
| Segments created | 3-5 tiers based on 1-2 attributes | Matrix of segments across 3-5 dimensions |
| Operational actions per segment | 3-5 distinct service models | 10-15+ differentiated playbooks possible |
| Data refresh needs | Quarterly (firmographics change slowly) | Real-time or daily (behavioral data changes constantly) |
| Tool requirements | CRM + optional enrichment | CRM + CSP + enrichment |

---

## 3) Benchmarks & Standards

### How to Use Benchmarks

Benchmarks are guidelines, not rules. Always:
1. Start with benchmark as baseline
2. Adjust based on client-specific data (ACV distribution, CS team size, product complexity)
3. Validate against their actual numbers when available
4. Document deviations and rationale

### Customer Tier Thresholds (by ARR)

| Metric | SMB / Tech-Touch | Mid-Market / Low-Touch | Enterprise / High-Touch | Notes |
|--------|-------------------|------------------------|-------------------------|-------|
| ARR Range | &lt; $25K | $25K - $100K | $100K+ | Adjust based on client's ACV distribution |
| CSM Ratio | 200-1,000:1 | 50-200:1 | 15-50:1 | Lower ratios = more personalized service |
| QBR Cadence | None (automated health emails) | Quarterly | Monthly or Bi-monthly | Enterprise may want on-site annually |
| Onboarding Model | Self-serve / automated | Guided (CSM-led, templated) | Custom (dedicated implementation) | Complexity drives this more than ARR |

**Source:** ChurnZero CS Benchmarks [2], CSM Practice SMB Engagement Research [6], industry practitioner surveys.

**Interpretation:**
- **Below SMB threshold:** If most customers fall below $10K ARR, the entire base may be tech-touch by default. Focus segmentation on behavioral signals (usage, engagement) rather than ARR tiers.
- **Above Enterprise threshold:** Customers at $250K+ ARR often justify a named, senior CSM plus an executive sponsor. Treat this as a sub-segment within Enterprise.

### Segment Count Benchmarks

| Metric | Low | Typical | High | Notes |
|--------|-----|---------|------|-------|
| Number of segmentation dimensions | 1 | 3 | 5 | More than 5 creates unmanageable matrix |
| Values per dimension | 2 | 3-4 | 6 | More than 6 per dimension = over-segmentation |
| Total distinct segments operationalized | 3 | 6-12 | 20 | Each segment must map to a distinct action |
| Accounts per segment (minimum viable) | 10 | 30+ | 100+ | Below 10 accounts, segment is not statistically meaningful |

**Source:** ChurnZero Smart Segmentation Guide [2], B2B International segmentation research [7].

**Interpretation:**
- **Below low:** Single-tier treatment. Acceptable for &lt;100 customer startups, but revisit at scale.
- **Above high (20+ segments):** Over-engineering risk. Check that each segment drives a unique operational action. Consolidate segments that receive identical treatment.

### Data Quality Thresholds for Segmentation

| Metric | Minimum Viable | Target | Ideal | Notes |
|--------|---------------|--------|-------|-------|
| Key field completeness (industry, employee count, ARR) | 60% | 80% | 95%+ | Below 60%, segmentation will misclassify >30% of accounts |
| Data accuracy (spot-check sample) | 70% | 85% | 95%+ | Validate 50-record sample against enrichment sources |
| Enrichment coverage after tool run | 70% | 85% | 95%+ | ZoomInfo/Apollo/Clay typically achieve 75-90% match rates for B2B |
| Duplicate rate (account-level) | &lt; 10% | &lt; 5% | &lt; 2% | Dedup before segmentation; dupes skew segment distribution |

### Quick Reference Thresholds

| Question | Good | Warning | Red Flag |
|----------|------|---------|----------|
| How many segments are operationalized? | 4-8 with distinct actions | 9-15 (review for consolidation) | 16+ or 1-2 (under/over-segmented) |
| What % of accounts have segments assigned? | 95%+ | 80-94% | Below 80% |
| How often are segments reviewed? | Quarterly with data audit | Semi-annually | Never after initial build |
| What % of key fields are populated? | 85%+ | 60-84% | Below 60% |
| Do segments drive different CS actions? | Each segment has a distinct playbook | Some segments have differentiated actions | Segments exist but all customers treated the same |

---

## 4) Calculations & Scoring

### Formula Quick Reference

| Calculation | Formula | Example |
|-------------|---------|---------|
| Composite Segment Score | `(Firmographic Score x W1) + (Behavioral Score x W2) + (Value Score x W3)` | (4 x 0.3) + (3 x 0.4) + (5 x 0.3) = 3.9 |
| Segment Coverage Rate | `(Accounts with segment assigned / Total active accounts) x 100` | (450 / 500) x 100 = 90% |
| Field Completeness Rate | `(Non-null values for field / Total active accounts) x 100` | (420 / 500) x 100 = 84% |
| Segment Concentration Index | `Largest segment account count / Total accounts` | 280 / 500 = 56% (warning: >60% means one segment dominates) |

### Composite Segment Scoring Method

**When to use:** When clients want a single score that combines multiple segmentation dimensions into a unified tier assignment. Common in mature CS orgs with 500+ customers.

**Formula:**
```
Composite Score = (Firmographic Score x W_firm) + (Behavioral Score x W_behav) + (Value Score x W_value)

Where:
  W_firm + W_behav + W_value = 1.0
```

**Variables explained:**
- `Firmographic Score` (1-5) = Based on company size, industry strategic fit, and geography. Scored via lookup table matching CRM fields to a rubric.
- `Behavioral Score` (1-5) = Based on product usage, engagement, and support patterns. Sourced from CSP health score or manual calculation.
- `Value Score` (1-5) = Based on current ARR, expansion potential, and strategic importance. Sourced from CRM opportunity and contract data.
- `W_firm / W_behav / W_value` = Weights determined during stakeholder discovery. Typical starting weights: 0.25 / 0.40 / 0.35 (behavioral weighted highest for retention-focused orgs).

**Worked Example:**

```
Given:
- Firmographic Score = 4 (Mid-market, 500 employees, target industry, US-based)
- Behavioral Score = 2 (Low product usage, declining login frequency, 3 open support tickets)
- Value Score = 5 ($85K ARR, strong expansion pipeline, multi-year contract)
- Weights: W_firm = 0.25, W_behav = 0.40, W_value = 0.35

Calculate:
- Composite Score = (4 x 0.25) + (2 x 0.40) + (5 x 0.35)
- Composite Score = 1.0 + 0.8 + 1.75 = 3.55

Interpretation:
- Tier 1 (High-Touch): 4.0+
- Tier 2 (Low-Touch): 2.5 - 3.99
- Tier 3 (Tech-Touch): Below 2.5

Result: Tier 2 (Low-Touch), but flagged for intervention due to low behavioral score despite high value.
```

**Validation:**
- Composite scores should distribute roughly: 15-25% Tier 1, 40-55% Tier 2, 25-35% Tier 3
- If more than 60% of accounts fall in a single tier, adjust thresholds or weights
- Accounts with high Value Score but low Behavioral Score are at-risk and should trigger alerts regardless of tier

### Firmographic Scoring Rubric

| Criterion | 5 Points | 4 Points | 3 Points | 2 Points | 1 Point |
|-----------|----------|----------|----------|----------|---------|
| Company Size (employees) | 1,000+ | 500-999 | 100-499 | 50-99 | &lt; 50 |
| Industry Fit | Target vertical | Adjacent vertical | General B2B | Non-target but viable | Poor fit |
| Geography | Primary market | Secondary market | Supported region | Limited-support region | Unsupported |
| Growth Stage | Growth / Scale-up | Established | Mature | Early-stage | Unknown / Pre-revenue |

**Tier Thresholds (Firmographic only):**
- Tier 1: 16+ points (out of 20)
- Tier 2: 10-15 points
- Tier 3: Below 10 points

### Value Scoring Rubric

| Criterion | 5 Points | 4 Points | 3 Points | 2 Points | 1 Point |
|-----------|----------|----------|----------|----------|---------|
| Current ARR | $100K+ | $50K-$99K | $25K-$49K | $10K-$24K | &lt; $10K |
| Expansion Potential | Strong (2x+ current ARR) | Moderate (1.5x) | Some (1.2x) | Limited | Contracting |
| Contract Length | Multi-year | Annual (renewing) | Annual (new) | Month-to-month | At risk / Past due |
| Strategic Importance | Named logo / reference customer | Industry influencer | Standard customer | Commodity fit | Misaligned |

**Tier Thresholds (Value only):**
- Tier 1: 16+ points
- Tier 2: 10-15 points
- Tier 3: Below 10 points

---

## 5) Edge Cases & Deep Dives

### Edge Case 1: New Company with No Historical Behavioral Data

*Scenario:*

A recently closed customer has no product usage history, no engagement score, and no NPS data. They need to be assigned to a segment immediately for onboarding routing.

*Challenge:*

Behavioral scores require 30-90 days of data to be meaningful. Assigning a segment based only on firmographics and value may place the account in the wrong service model.

*Approach:*

1. Assign an initial segment based on firmographic + value scores only (skip behavioral weighting)
2. Set a 30-day "provisional segment" flag in the CRM
3. After 30 days, run behavioral scoring and recalculate composite score
4. If the recalculated tier differs from the provisional assignment, reassign and notify the CSM

*Fallback assumptions:*

| Missing Data | Use This Instead | Source |
|--------------|------------------|--------|
| Product usage score | Assume median (3/5) | Avoids over- or under-weighting new accounts |
| NPS / satisfaction | Skip from composite | Not meaningful for accounts &lt; 30 days old |
| Engagement score | Use onboarding completion rate as proxy | CSP or manual tracking |

### Edge Case 2: Multi-Product Organization

*Scenario:*

The client sells three products. A customer may be Enterprise for the core platform ($120K ARR) but only trialing an analytics add-on ($5K pilot). They need different segment treatment per product.

*Approach:*

1. Create a **primary segment** based on total relationship value (all products combined) -- this drives the overall service model and CSM assignment
2. Create **product-level behavioral tags** (not full segments) that indicate adoption maturity per product
3. Use the primary segment for CSM assignment and executive reporting
4. Use product-level tags to trigger product-specific playbooks and onboarding flows
5. Report on segment performance both at the aggregate level and per product line

### Edge Case 3: Poor Data Quality Blocking Segmentation

*Scenario:*

Discovery reveals that the industry field is 35% blank, employee count is 50% populated, and there are 800+ duplicate account records. The client wants to proceed with segmentation immediately.

*Approach:*

1. **Phase 0 (1-2 weeks):** Run deduplication first (use DemandTools, Cloudingo, or Ringlead). Merge duplicates before any segmentation work.
2. **Phase 0.5 (1 week):** Run extended enrichment via ZoomInfo, Apollo, or Clay to fill firmographic gaps. Target 80%+ coverage on key fields.
3. **Phase 1 (1-2 weeks):** Build initial segmentation using enriched data. Assign segments only to accounts with complete key fields.
4. **Phase 1.5 (ongoing):** Flag accounts with missing data as "Unsegmented" with a data quality reason. Create a queue for manual research or targeted enrichment.
5. **Phase 2:** As data quality improves, extend segmentation to remaining accounts.

*Fallback assumptions:*

| Missing Data | Use This Instead | Source |
|--------------|------------------|--------|
| Industry | "Unknown" category; route to SMB playbook by default | Prevents false categorization |
| Employee count | Use ARR as size proxy (&lt; $25K = SMB, $25-100K = MM, $100K+ = Ent) | Contract data is usually 100% populated |
| Geography | Use billing address country code | Billing system data |

### Edge Case 4: Customer Crosses Segment Boundary

*Scenario:*

A Mid-Market account ($45K ARR) signs a major expansion deal and jumps to $130K ARR, crossing into Enterprise territory. The CSM relationship and success plan are built around the Mid-Market service model.

*Approach:*

1. Automated rules should flag the segment change but not auto-reassign CSM immediately
2. CS Ops reviews flagged accounts weekly and creates a transition plan
3. Transition plan includes: 30-day joint coverage (old CSM + new CSM), updated success plan, and customer notification
4. Update segment in CRM after transition plan is approved, not at the moment of contract change
5. Document the transition in the account record for continuity

### Edge Case 5: Acquisition-Driven Industry Change

*Scenario:*

A customer was segmented as "Technology" industry. They are acquired by a Healthcare conglomerate. Their product usage, team, and contract remain the same, but their parent company is now in Healthcare.

*Approach:*

1. Add a "Manual Override" flag to the segmentation model that prevents automated re-assignment
2. When enrichment data conflicts with existing data due to M&A, flag for CS Ops review rather than auto-updating
3. CS Ops evaluates: Has the buying center changed? Has the use case changed? Has the contract been modified?
4. If the operational reality is unchanged, keep the existing segment with a note. If the account is being absorbed into the parent, update the segment.

---

## References

[1] [McKinsey - The Value of Getting Personalization Right or Wrong Is Multiplying](https://www.mckinsey.com/capabilities/growth-marketing-and-sales/our-insights/the-value-of-getting-personalization-right-or-wrong-is-multiplying)

[2] [ChurnZero - Customer Segmentation Models: Frameworks & Best Practices](https://churnzero.com/blog/importance-of-customer-success-segmentation/)

[3] [Twilio Segment - A Guide to B2B Customer Segmentation](https://segment.com/growth-center/customer-segmentation/b2b/)

[4] [EverAfter - High-Touch vs Low-Touch vs Tech-Touch Customer Success Models Explained](https://www.everafter.ai/glossary/high-touch-low-touch-tech-touch)

[5] [Vitally - What Is Tech Touch Customer Success and How Does It Fit Into the SaaS Business Model](https://www.vitally.io/post/what-is-tech-touch-customer-success)

[6] [CSM Practice - How Low Can You Go: Customer Success for Your SMB Segment](https://csmpractice.com/how-low-can-you-go-customer-success-for-your-smb-segment/)

[7] [B2B International - Effective B2B Market Segmentation](https://www.b2binternational.com/publications/b2b-segmentation-research/)

[8] [Delve AI - Firmographic Segmentation: Examples and Variables in B2B Marketing](https://www.delve.ai/blog/firmographic-segmentation)
