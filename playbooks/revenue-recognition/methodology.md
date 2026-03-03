# Revenue Recognition — Methodology

This document covers the core concepts, frameworks, and calculations behind Revenue Recognition (RevRec). It provides the methodological foundation — the "how it works" behind the execution steps.

## 1) Core Concepts

### The Golden Number

*What is it?*

The specific revenue metric a company is tracking as their primary growth target. This could be revenue, bookings, ARR, MRR, ACV, or TCV. Each has a different meaning, and teams routinely use these terms interchangeably without alignment.

*Why does it matter?*

Everything in RevRec maps back to this number. If you build field logic around "ARR" but the company actually tracks "bookings" (which may exclude product-led revenue), the entire build is misaligned. Quotas, commissions, and reporting all derive from this number. Getting it wrong means every downstream calculation is wrong.

*Key insight:*

> "We're trying to hit 50 million this year. 50 million what? And I think that question stumps a lot of teams."

*Examples:*

| Context | Golden Number Implications |
|---------|--------------------------|
| Company with PLG + sales-led motion | "Bookings" only counts signed deals, not self-serve revenue. The golden number may exclude a significant portion of total revenue. |
| Enterprise with multi-year deals | ACV = TCV / term. A $100M 5-year deal is $20M ACV, not $100M. If the golden number is "ARR," multi-year normalization is required. |
| Standard annual SaaS | ARR = MRR x 12. Straightforward, but the finance team still needs to confirm whether one-time charges (setup, services) are included. |
| Hybrid model (hardware + software) | Revenue recognition may be blocked until hardware is physically installed. The golden number must account for deferred recognition. |

*Common misunderstandings:*

- **Misconception:** All companies define revenue the same way
  **Reality:** Revenue, bookings, ARR, MRR, ACV, TCV all have different meanings and each company adds their own interpretation.

- **Misconception:** The finance team can immediately tell you their golden number
  **Reality:** Most teams struggle to articulate this on the first ask. Expect pushback and follow-up meetings to pin down the precise definition.

---

### Revenue Metric Definitions

*What is it?*

A set of related but distinct financial metrics that companies use to measure revenue. Aligning on these definitions before any field logic is built is non-negotiable.

*Why does it matter?*

Bookings provide forward-looking visibility into sales momentum and contractual commitments, while ARR offers a normalized view of recurring revenue at a specific point in time [1]. The RevRec fields must map to how the company actually measures and reports revenue. Getting the definitions wrong means the field logic produces numbers that do not match what finance and leadership are looking at.

*The Definitions:*

| Term | Definition | Notes |
|------|-----------|-------|
| **Revenue** | All money brought in — both recurring and non-recurring | Broadest measure |
| **Bookings** | Dollar amount of signed contracts with customers, usually recurring revenue from sales-led deals [2] | May exclude PLG/self-serve; recorded at contract signing, not delivery |
| **ARR (Annual Recurring Revenue)** | MRR x 12 | Excludes one-time charges; normalized annual view |
| **MRR (Monthly Recurring Revenue)** | Recurring revenue measured monthly | Base unit for ARR calculation |
| **ACV (Annual Contract Value)** | TCV / term in years | Includes services on top of recurring; normalizes multi-year deals to annual value [3] |
| **TCV (Total Contract Value)** | Full contract value over entire term, including recurring fees and one-time charges (setup, implementation) | Shows total financial commitment; higher uncertainty for long-term contracts [3] |

*Key insight:*

> "Common terms, but all depend on the finance team."

*When to use ACV vs. TCV:*

Use ACV when setting sales quotas and comparing deals of varying lengths — annual goals map cleanly to ACV [3]. Use TCV when evaluating total deal size for enterprise negotiations, commission design, or understanding full financial commitment. Enterprise companies signing multi-year deals ($1M+, 3-5 year terms) need both metrics actively tracked.

---

### The Six RevRec Fields

*What is it?*

The core output of a RevRec project: six calculated fields in Salesforce that together provide a complete picture of revenue across all deal types. These fields are built with workflow logic that triggers different calculations based on opportunity type (new business, expansion, contraction, renewal, churn).

*The Fields:*

| # | Field | What It Captures | Who Uses It |
|---|-------|-----------------|-------------|
| 1 | **Recurring Amount** | The recurring portion of the deal (excludes services) | Finance, RevOps |
| 2 | **Net New ARR** | Only takes positive values; contractions show as $0 | Sales (forecasting, commissions) |
| 3 | **Net ARR** | Takes both positive and negative values; captures full impact including churn/contraction | CS/Account Managers |
| 4 | **Contract ARR** | Sum of all active contracts for an account; the basis for renewal calculations | Finance, CS (renewal management) |
| 5 | **ACV** | Annual contract value including services, normalized by term | Sales, Finance (annual reporting) |
| 6 | **TCV** | Total contract value including services, full term value | Finance, Deal Desk |

*Why does it matter?*

Each field exists for a specific operational reason. Net New ARR prevents churn from distorting sales forecasting. Net ARR gives CS and account managers the full picture of customer health. Contract ARR ensures renewals are based on the actual total of all active contracts, not just the initial deal.

*The Critical Split: Net New ARR vs. Net ARR*

These two fields look identical when deals are positive. They diverge on contraction and churn:

| Scenario | Net New ARR | Net ARR | Why |
|----------|-------------|---------|-----|
| New Business: $100K | $100K | $100K | Positive deal — fields match |
| Expansion: $40K | $40K | $40K | Positive deal — fields match |
| Contraction: -$40K | **$0** | **-$40K** | Net New ARR protects sales forecasting; Net ARR shows the real impact for CS |
| Churn: -$100K | **$0** | **-$100K** | Same logic — sales not penalized, CS sees the full loss |

This split directly maps to the churn ownership question: sales gets the upside (Net New ARR), CS/AMs own the downside (Net ARR).

*Common misunderstandings:*

- **Misconception:** Net New ARR and Net ARR are the same thing
  **Reality:** They look the same on positive deals and diverge on negative ones. Using Net ARR for sales forecasting distorts pipeline numbers when contractions occur.

- **Misconception:** You can build RevRec on opportunities alone
  **Reality:** Contract ARR requires contract objects in Salesforce. Tracking everything in opportunities makes it nearly impossible to calculate the sum of all active contracts for an account.

---

### The Revenue Recognition Trigger

*What is it?*

Revenue recognition is not automatic upon deal close. Different businesses have different triggers that must be met before revenue can be recognized by finance. The tracking infrastructure to monitor these triggers is a core component of RevRec.

Under ASC 606, revenue is recognized when a performance obligation is satisfied — meaning the promised good or service has been transferred to the customer [4]. For SaaS companies, this typically means recognizing revenue ratably over the subscription period rather than at the point of contract signing.

*Why does it matter?*

The recognition trigger determines what tracking infrastructure the RevRec build must include. A company that sells only SaaS subscriptions has a straightforward trigger (subscription start date). A company that bundles hardware, services, and software has compound triggers that require operational tracking systems.

*Recognition Trigger Types:*

| Trigger Type | Example | Tracking Required |
|-------------|---------|-------------------|
| Subscription start | Standard SaaS annual contract | Subscription start/end dates in CRM |
| Hardware installation | Sells hardware + software; cannot recognize revenue until hardware is installed | Installation status tracking that notifies finance upon completion |
| Hours/services delivered | Revenue recognized as hours are delivered per client | Per-client hours tracking with finance notification pipeline |
| Usage-based consumption | Metered SaaS products | Usage metering tool (e.g., Metronome) feeding into billing and recognition |
| Milestone completion | Professional services with defined deliverables | Project milestone tracking connected to finance systems |

---

### The Operating Plan

*What is it?*

The company expressed in numbers. Run by the CEO, it pulls data from accounting systems (QuickBooks, Xero), the revenue model, and the hiring plan. It is the financial blueprint showing revenue targets, expenses, and expected profit. Typically built in Excel or Google Sheets, though platforms like Runway are operationalizing this process.

*Why does it matter?*

The operating plan reveals how the company structures its revenue — by region, product, segment, and team. This directly informs how RevRec fields should be architected. If the operating plan breaks out revenue by US and international regions, RevRec fields need to support that same segmentation.

*Key insight:*

> "A lot of people have to start with the operating plan because this is how they raise their fundraising round."

SaaS financial models for Series B and beyond typically include 3 years of projections across P&L, Balance Sheet, and Cash Flows [5]. The operating plan is the source document that RevRec must align to.

*What to look for in the operating plan:*

| Component | RevRec Implication |
|-----------|-------------------|
| Revenue breakouts by region | RevRec fields may need regional segmentation; currency conversion must be considered |
| Revenue breakouts by product type | Product catalog must be structured to support reporting per product line |
| Revenue breakouts by segment (enterprise, mid-market, SMB) | Opportunity record types may need segment-based logic |
| Discount methodology | How discounts are applied affects recurring amount calculations |
| Revenue targets by team | Determines which teams see which RevRec field outputs |
| Committed (sales-led) vs. product-led revenue | Bookings may only capture one side; RevRec fields must cover both |

*Common misunderstandings:*

- **Misconception:** The operating plan is a finance-only document
  **Reality:** It is the CEO's document that defines how every team contributes to the revenue number. Sales targets, CS retention goals, and marketing pipeline — all flow from the operating plan.

- **Misconception:** You can skip the operating plan walkthrough and go straight to field mapping
  **Reality:** The operating plan reveals structural assumptions that determine field architecture. Skipping it means building fields that do not match how the company measures success.

---

### Co-terming

*What is it?*

Setting expansion contract end dates to match the original contract's end date, rather than creating a new full-term contract for each add-on. If a customer signed a 12-month contract starting January 1 and adds users in June, the expansion co-terms to December 31 (the original end date), not to the following June.

*Why does it matter?*

Without co-terming, a customer with multiple expansions ends up with contracts renewing at different dates. A customer who started with 3 licenses and added 2 more mid-term would have 3 licenses renewing in December and 2 renewing the following June. This creates a nightmare for renewal management, confusing customer experiences, and distorted revenue forecasting.

*The co-terming decision:*

| Approach | What Happens | Consequence |
|----------|-------------|-------------|
| **Co-term (best practice)** | Expansion ends on same date as original contract; expansion amount is prorated for remaining term | Single renewal date per account; clean contract ARR; simpler renewal management |
| **New full-term contract** | Expansion gets its own 12-month (or multi-year) term starting from expansion date | Staggered renewal dates; fragmented contract ARR; multiple renewal conversations per account |

*Revenue Movement considerations:*

Expansion can happen either mid-term (co-termed to existing end date) or at renewal (coterminous with the renewal). The Revenue Movement Formula must handle both timing patterns. Same applies to contraction — customers may downsell within their term, not just at renewal.

---

### Bookings Policy

*What is it?*

A documented set of rules that define how reps handle different contract scenarios: expansions, renewals, co-terming, POCs, and what counts toward ARR. It serves as the operating rulebook for sales and CS teams.

*Why does it matter?*

Without a bookings policy, reps create their own rules. Different reps handle the same scenario differently, producing inconsistent data that RevRec logic cannot accurately process. The bookings policy also serves as an onboarding document — when new leadership or ops people join, they have a single reference for how the company handles contracts.

*What the bookings policy should define:*

| Scenario | Policy Question | Example Rule |
|----------|----------------|--------------|
| Mid-term expansion | Prorate for remaining term, or renew all licenses? | "All expansions are co-termed and prorated to the existing contract end date" |
| POCs (Proof of Concept) | Do they count as ARR? | "POCs are not counted as ARR and must be flagged as POC opportunity type" |
| Expansion types | Sales-led committed vs. product-led consumption | "Only signed contract expansions count as bookings; usage overages are recognized separately" |
| Renewal timing | When does the renewal process start? | "Renewal opportunities created 90 days before contract end date" |
| Multi-product add-ons | Same contract or new contract? | "All add-ons co-termed to primary contract" |
| Churn/downgrade process | Who initiates, what approval is required? | "CS initiates contraction opps; requires manager approval for >20% reduction" |

---

### Opportunity Types and Record Types

*What is it?*

Salesforce categorizations that determine the logic behind RevRec field calculations. Each opportunity type (new business, expansion, renewal, contraction, churn) triggers different field behavior. Record types control which fields, page layouts, and picklist values appear for each deal type [6].

*Why does it matter?*

The RevRec field logic depends entirely on knowing what type of deal is being processed. A new business deal adds to Contract ARR. An expansion adds to it. A contraction subtracts from it. A churn zeroes it out. Without properly configured opportunity types, the system cannot determine which calculation to run.

*Standard RevRec opportunity types:*

| Opportunity Type | RevRec Field Behavior |
|-----------------|----------------------|
| **New Business** | All fields populate; Contract ARR = recurring amount |
| **Expansion** | Recurring amount is the expansion delta; Contract ARR = previous + expansion |
| **Flat Renewal** | Recurring amount stays the same; Contract ARR unchanged |
| **Expansion Renewal** | Recurring amount increases; Contract ARR = new total |
| **Contraction** | Recurring amount is negative delta; Net New ARR = $0; Net ARR = negative amount; Contract ARR reduced |
| **Churn** | All recurring amounts go to zero; Net ARR = negative of full contract ARR |

---

### Quotas & Commissions Dependency

*What is it?*

Most GTM teams need RevRec fields to calculate quotas and commissions. RevRec is the foundational data layer that quotas and commissions are built on top of.

*Why does it matter?*

If RevRec fields are not properly configured, quota attainment and commission calculations will be inaccurate or impossible to automate. The churn ownership decision (who gets penalized for downgrades) directly shapes which RevRec fields feed into which team's compensation plans.

*Typical quota/commission field mapping:*

| Role | RevRec Field Used | Why |
|------|------------------|-----|
| Sales (AEs) | Net New ARR | Sales gets credit for positive deals only; not penalized for churn they do not control |
| CS / Account Managers | Net ARR | CS sees the full picture including contractions and churn they are responsible for managing |
| Renewal Specialists | Contract ARR (as renewal basis) | Renewal target = current Contract ARR, not the original deal amount |
| Finance / Executive | All six fields | Complete view for reporting, forecasting, and board-level metrics |

---

## 2) Decision Frameworks

### Approach Selection Matrix

| Situation | Recommended Approach | Why |
|-----------|---------------------|-----|
| Very small team, simple revenue model, single product | RevRec Standalone — Simple | Just fields with workflows; minimal pre-work needed |
| Mid-size company, needs revenue reporting fields, not doing CPQ | RevRec Standalone | Focused scope; full pre-work (golden number, operating plan, quotas) but straightforward build |
| Company implementing CPQ | RevRec with CPQ | RevRec bleeds into CPQ; product catalog and territories must be built for reporting. 60-70% of RevRec projects accompany CPQ. |
| Hardware + software bundle | RevRec with Installation Tracking | Recognition trigger is hardware installation; requires integration between project management and CRM |
| Usage-based pricing model | RevRec with Metering | Requires metering infrastructure (e.g., Metronome) feeding into billing and recognition |

### Scoping Factors

These variables determine which approach to use and the overall level of effort.

**1. Standalone vs. CPQ Accompaniment**

- Standalone: Client only needs revenue reporting fields. Pre-work + field build.
- With CPQ: RevRec is a component of a larger quote-to-cash implementation. Product catalog, territories, and pricing must all be built to support RevRec reporting.

**2. Revenue Model Complexity**

- Single product, single region: Straightforward field logic. One set of calculations.
- Multi-product: Product catalog must be structured to support per-product reporting.
- Multi-region: Currency conversion, tax variations, and regional revenue breakouts add complexity.
- Hybrid (PLG + sales-led): Must handle both committed (signed deal) and consumption-based recognition.

**3. Contract Structure**

- Co-termed contracts: Best practice. Single renewal date per account. Simpler Contract ARR calculation.
- Multiple contract end dates: Creates staggered renewals. Requires more complex Contract ARR logic and renewal tracking.
- No contracts in Salesforce: Blocker. Contract objects must be set up before RevRec can be built properly.

**4. Enterprise Motion / Deal Size**

- SMB / standard annual deals: ACV/TCV distinction is minimal. Simpler calculations.
- Enterprise / multi-year deals: ACV/TCV distinction is critical. A 5-year, $100M deal must be recognized as $20M ACV, not $100M.

**5. Churn Ownership**

- CS owns churn (most common): Net New ARR = sales metric (positive only). Net ARR = CS metric (positive and negative).
- Sales owns churn: Both Net New ARR and Net ARR may need to capture negatives. Commission logic changes.
- Undefined: Must be defined before building. This is a prerequisite, not something to figure out during the build.

**6. Recognition Trigger Type**

- Subscription start (standard SaaS): Straightforward. Recognition begins at subscription activation.
- Hardware installation: Requires installation tracking. Revenue deferred until physical delivery confirmed.
- Hours/services delivered: Requires time tracking integration. Revenue recognized as hours are consumed.
- Usage-based: Requires metering infrastructure. Revenue recognized based on consumption data.

### RevRec Standalone

*Best for:*
- Companies that need revenue reporting without a full CPQ overhaul
- Companies with straightforward pricing (per-seat, flat annual subscription)
- Smaller teams where stakeholder alignment is faster

*Not recommended for:*
- Companies actively implementing CPQ (do both together)
- Companies with complex multi-product quoting needs
- Companies with no contracts in Salesforce (set up contracts first)

| Aspect | Standard | Standalone RevRec |
|--------|----------|-------------------|
| Pre-work | Golden number, operating plan, quotas/commissions, bookings policy | Same — pre-work does not change |
| Build | Six fields with workflow logic | Same — output is identical |
| Scope boundary | Revenue fields only; no product catalog, no quoting | Clear boundary — do not scope creep into CPQ |

### RevRec with CPQ

*Best for:*
- Companies implementing CPQ where RevRec is a natural extension
- Companies with complex product catalogs that need per-product revenue reporting
- Enterprise companies with multi-year, multi-product deals

*Not recommended for:*
- Companies that only need RevRec (over-engineered for the need)
- Companies without the budget or timeline for a full-quarter project

| Aspect | Standalone | With CPQ |
|--------|-----------|----------|
| Product catalog | Not in scope | Must be built to support RevRec reporting |
| Territory structure | Not in scope | Must be built for regional breakouts |
| Stakeholders | Finance + RevOps + Sales/CS | Add: Deal Desk, Product, Engineering |
| Integration points | Salesforce fields + workflows | CPQ + Salesforce + potentially billing system |

---

## 3) Benchmarks & Standards

### How to Use Benchmarks

Benchmarks are guidelines, not rules. Always:
1. Start with the benchmark as a baseline
2. Adjust based on the client's specific data and business model
3. Validate against their actual numbers when available
4. Document deviations and rationale

### ASC 606 Revenue Recognition Standard

ASC 606, established in 2017 by FASB and IASB, replaced all prior industry-specific revenue recognition guidelines [4]. It applies to all US GAAP reporting companies and is the regulatory framework that defines how revenue must be recognized.

**The Five-Step Model:**

| Step | Description | RevRec Relevance |
|------|-------------|-----------------|
| 1. Identify the contract | Determine if a valid contract exists with commercial substance | Maps to contract object creation in Salesforce |
| 2. Identify performance obligations | Determine distinct goods/services promised | Drives recognition trigger type (subscription vs. installation vs. services) |
| 3. Determine transaction price | Calculate total consideration expected | Maps to TCV calculation |
| 4. Allocate transaction price | Distribute price across performance obligations by standalone selling price | Critical for bundled deals (software + services + hardware) |
| 5. Recognize revenue | Recognize when/as obligations are satisfied | Determines recognition timing — point-in-time vs. over time |

For SaaS companies, Step 5 typically means recognizing revenue ratably over the subscription period. A customer who pays $120K annually has $10K recognized each month as the service is delivered [4].

**Why this matters:** The RevRec fields you build must produce outputs that align with how the finance team recognizes revenue under ASC 606. If the fields calculate ACV differently than how finance recognizes it, the numbers will not match board reports.

### SaaS Revenue Retention Benchmarks

These benchmarks help validate whether a client's RevRec outputs are within expected ranges for their size and stage.

**Net Revenue Retention (NRR):**

| Company Size (ARR) | Median NRR | Top Quartile | Notes |
|--------------------|-----------|--------------|-------|
| $3M-$20M | 104% | 115%+ | Indicates healthy expansion within existing accounts [7] |
| $20M-$50M | 105-110% | 120%+ | Expansion revenue increasingly drives growth at this stage |
| $50M+ | 108-115% | 125%+ | Best-in-class public SaaS companies exceed 130% |

**Gross Revenue Retention (GRR):**

| Company Size (ARR) | Median GRR | 90th Percentile | Notes |
|--------------------|-----------|-----------------|-------|
| $3M-$20M | 92% | 98% | GRR below 85% is a red flag — the business is leaking [7] |

**Expansion as Growth Driver:**

Companies with $15M-$30M+ ARR are seeing 40% of their growth driven by expansion, up from 30% in early 2021 [8]. This makes RevRec field accuracy on expansion deals increasingly important — misattributed expansion revenue directly distorts growth reporting.

**Source:** SaaS Capital 2025 Benchmarking Report [7], Benchmarkit 2025 SaaS Performance Metrics [8]

**Interpretation:**
- **NRR below 100%:** The business is shrinking within its existing base. RevRec fields (Net ARR) will show net negative impact.
- **GRR below 85%:** High churn rate. RevRec project should prioritize churn tracking accuracy and ensure Contract ARR correctly reflects losses.
- **NRR above 120%:** Strong expansion motion. Verify that RevRec fields correctly separate expansion from new business for accurate attribution.

### Revenue Recognition Error Impact

Revenue recognition errors carry material financial consequences:

- Revenue recognition issues are among the leading causes of financial restatements per FASB [9]
- Professional services firms charge $100,000+ for restatement remediation work [9]
- Material weakness remediation often requires external consultants, incremental audit costs, and leads to accounting/finance personnel attrition [9]
- Disconnected systems, manual data entry, and inconsistent definitions are the primary root causes [9]

This is the cost of NOT doing RevRec properly. When a company's Salesforce opportunity data does not align with how finance recognizes revenue, the discrepancy compounds with every deal.

### Quick Reference Thresholds

| Question | Good | Warning | Red Flag |
|----------|------|---------|----------|
| Net Revenue Retention | >105% | 95-105% | &lt;95% |
| Gross Revenue Retention | >92% | 85-92% | &lt;85% |
| Expansion contribution to growth | >30% | 15-30% | &lt;15% at scale |
| RevRec field accuracy vs. finance reports | Exact match | &lt;5% variance | >5% variance |
| Time to close books (monthly) | &lt;5 days | 5-10 days | >10 days |

---

## 4) Calculations & Scoring

### Formula Quick Reference

| Calculation | Formula | Example |
|-------------|---------|---------|
| ACV | `TCV / Term (years)` | $200K TCV / 2-year term = $100K ACV |
| ARR | `MRR x 12` | $8.33K MRR x 12 = $100K ARR |
| TCV | `(Recurring + Services) x Term` | ($100K + $20K) x 2 years = $240K |
| Contract ARR | `Sum of all active contract recurring amounts` | $100K initial + $40K expansion = $140K contract ARR |
| Net New ARR | `MAX(deal_recurring, 0)` | New: $100K = $100K; Contraction: -$40K = $0 |
| Net ARR | `deal_recurring (positive or negative)` | New: $100K = $100K; Contraction: -$40K = -$40K |

### Worked Examples by Deal Scenario

**Scenario 1: New Business**

```
Given:
- Deal: $100K recurring + $20K services
- Term: 2 years

Calculate:
- Recurring Amount: $100K (excludes services)
- Net New ARR: $100K (positive — passes through)
- Net ARR: $100K (positive — passes through)
- Contract ARR: $100K (first deal on account)
- ACV: ($100K + $20K) / 2 = $60K
- TCV: ($100K + $20K) x 2 = $240K
```

**Validation:** ACV should be less than or equal to recurring + services. TCV = ACV x term. Contract ARR = recurring amount for a first deal.

---

**Scenario 2: Expansion (Co-termed)**

```
Given:
- Original deal: $100K recurring, ending Dec 31
- Expansion in June: $40K recurring (annualized), no services, co-termed to Dec 31

Calculate:
- Recurring Amount: $40K (annualized expansion value)
- Net New ARR: $40K
- Net ARR: $40K
- Contract ARR: $140K (original $100K + expansion $40K)
- Renewal basis going forward: $140K
```

**Validation:** Contract ARR should equal the sum of all active recurring amounts on the account.

---

**Scenario 3: Contraction**

```
Given:
- Contract ARR before contraction: $140K
- Customer downsells: -$40K recurring

Calculate:
- Recurring Amount: -$40K
- Net New ARR: $0 (only takes positive values — sales not penalized)
- Net ARR: -$40K (captures the full negative impact for CS/AM tracking)
- Contract ARR: $100K ($140K - $40K)
```

**Validation:** Net New ARR should always be >= $0. Net ARR should match the actual deal impact. Contract ARR should reflect the new total active recurring amount.

---

**Scenario 4: Full Churn**

```
Given:
- Contract ARR before churn: $100K
- Customer does not renew

Calculate:
- Recurring Amount: $0
- Net New ARR: $0 (only takes positive)
- Net ARR: -$100K (full negative impact)
- Contract ARR: $0
```

**Validation:** After a full churn, Contract ARR should be $0. Net ARR should equal the negative of the pre-churn Contract ARR.

---

### Revenue Movement Formula

The Revenue Movement Formula, configured in Salesforce, is what enables "Gold Standard Tracking" — reporting across all revenue impacts (upsell, contraction, churn, new business) regardless of when the movement occurs.

```
Revenue Movement = New Business + Expansion - Contraction - Churn
```

The formula must account for two timing patterns:
- **Mid-term movements:** Expansion or contraction happens within the contract term (co-termed to existing end date)
- **At-renewal movements:** Expansion or contraction happens at the renewal point (coterminous with renewal)

Both patterns must produce correct field values across all six RevRec fields.

---

## 5) Edge Cases

### Edge Case 1: Multi-Year Enterprise Deals

*Scenario:* Companies signing very large, multi-year contracts (e.g., 5-year, $100M partnerships).

*Challenge:* Putting the full value in year one distorts every annual metric. ACV, ARR, and forecasting all break if the full value is recognized upfront. Under ASC 606, multi-year SaaS contracts must be recognized over the service delivery period, not at signing [4].

*Approach:*

1. Calculate ACV = TCV / term ($100M / 5 years = $20M ACV)
2. Use ACV for annual reporting, quota attainment, and forecasting
3. Use TCV for total deal value tracking, deal strategy, and commission design where applicable
4. Confirm with finance how they recognize the contract under ASC 606
5. Ensure RevRec fields normalize the values — Recurring Amount should reflect the annual portion, not the total

---

### Edge Case 2: Churn Ownership Disputes

*Scenario:* Different teams have different opinions on whether sales, CS, or account managers should be penalized for churn. This comes up on every RevRec project.

*Challenge:* The RevRec field logic (specifically the Net New ARR vs. Net ARR split) depends entirely on this decision.

*Approach:*

1. Ask upfront: Who owns churn? Do not wait until the build phase.
2. Document the decision in the bookings policy.
3. Default assumption (most common): Sales only gets the upside (Net New ARR). CS/AMs own the downside (Net ARR).
4. Build field logic accordingly — Net New ARR = MAX(deal_recurring, 0).

Research supports a nuanced view: NRR requires input from multiple teams — sales, product, finance, and executive — not just CS [10]. And poor GRR often starts with sales qualification problems, not CS retention failures [11]. Use this to frame the churn ownership conversation: it is not about blame, it is about which team has operational control over the outcome.

---

### Edge Case 3: Multi-Region / Multi-Currency

*Scenario:* Companies operating in multiple countries with separate revenue targets per region.

*Challenge:* Currency conversion, taxes, and discount variations all affect how RevRec fields calculate. A deal closed in EUR must convert to the company's reporting currency at either spot rate or a locked conversion rate.

*Approach:*

1. Identify all regions from the operating plan during pre-work
2. Determine the reporting currency and conversion methodology
3. Ensure RevRec fields handle currency changes — Salesforce supports multi-currency, but the conversion timing must be defined
4. Build product catalog and territory structures to support per-region reporting

---

### Edge Case 4: No Contracts in Salesforce

*Scenario:* The company tracks everything in opportunities and is not using Salesforce contract objects.

*Challenge:* Contract ARR is nearly impossible to calculate accurately without contract objects. With only opportunities, there is no clear way to determine the total active recurring value across multiple expansions.

*Approach:*

1. Flag this as a blocker during pre-work discovery
2. Contract objects must be set up before RevRec fields can be built properly
3. If contracts truly cannot be implemented, build a workaround using a roll-up summary field on the account — but document this as a known limitation

---

### Edge Case 5: No Bookings Policy Exists

*Scenario:* The client has no documented rules for how reps handle expansions, renewals, or contract management.

*Challenge:* Reps create their own rules, producing inconsistent data that RevRec logic cannot accurately process.

*Approach:*

1. Define the bookings policy as part of the RevRec pre-work (not a separate project)
2. Cover at minimum: co-terming rules, expansion handling, POC treatment, what counts as ARR
3. Get sign-off from finance AND sales leadership

---

### Edge Case 6: Coterminous Expansion at Renewal vs. Mid-Term

*Scenario:* An expansion happens at the same time as a renewal, not mid-term.

*Challenge:* If the system treats the entire renewed + expanded amount as "new," it over-counts expansion and distorts retention metrics.

*Approach:*

1. Separate the renewal component from the expansion component at the opportunity level
2. Confirm with the client which approach their sales process supports
3. Ensure the Revenue Movement Formula correctly attributes the renewal base vs. the expansion increment

---

### Edge Case 7: Within-Term Contraction (Downsell)

*Scenario:* A customer downsells mid-term, reducing their subscription before the contract renewal date.

*Challenge:* Some companies do not allow within-term contraction contractually. Others do. The RevRec system must handle both patterns.

*Approach:*

1. During pre-work, ask: "Can customers downsell within their contract term?"
2. If yes: Contract ARR updates immediately upon contraction close. Net ARR reflects the negative amount. Net New ARR shows $0.
3. If no (contraction only at renewal): Contract ARR stays unchanged until renewal.
4. Document the within-term contraction policy in the bookings policy.

---

## References

[1] [Stripe — Bookings vs ARR Explained](https://stripe.com/resources/more/bookings-vs-arr-explained-what-each-is-and-how-businesses-should-use-both)
[2] [Chargebee — Bookings vs Billings vs Revenue](https://www.chargebee.com/blog/bookings-vs-billings-vs-revenue/)
[3] [Stripe — ACV vs TCV: Important Metrics for SaaS Businesses](https://stripe.com/resources/more/annual-contract-value-vs-total-contract-value)
[4] [Maxio — The Ultimate Guide to SaaS Revenue Recognition and ASC 606](https://www.maxio.com/blog/saas-revenue-recognition-asc-606)
[5] [Corporate Finance Institute — SaaS Financial Modeling Overview](https://corporatefinanceinstitute.com/resources/financial-modeling/saas-financial-model/)
[6] [Salesforce Ben — Salesforce Record Type Best Practices](https://www.salesforceben.com/salesforce-record-type-best-practices-tutorial/)
[7] [SaaS Capital — 2025 Benchmarking Metrics for Bootstrapped SaaS Companies](https://www.saas-capital.com/blog-posts/benchmarking-metrics-for-bootstrapped-saas-companies/)
[8] [Benchmarkit — 2025 SaaS Performance Metrics](https://www.benchmarkit.ai/2025benchmarks)
[9] [RightRev — Top Reasons for Material Weakness in Revenue Recognition](https://www.rightrev.com/revenue-recognition-management/)
[10] [ChurnZero — Net Revenue Retention](https://churnzero.com/churnopedia/net-revenue-retention/)
[11] [Revic — Gross Revenue Retention: The Metric That Doesn't Flinch](https://www.revic.ai/blog/gross-revenue-retention-the-metric-that-doesnt-flinch/)
