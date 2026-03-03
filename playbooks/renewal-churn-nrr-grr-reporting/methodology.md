# Renewal, Churn, NRR/GRR Reporting — Methodology

This document covers the core concepts, frameworks, and calculations behind Renewal, Churn, NRR/GRR Reporting. It provides the methodological foundation — the 'how it works' behind the execution steps.

---

## 1) Core Concepts

### Net Revenue Retention (NRR)

*What is it?*

Net Revenue Retention measures the percentage of recurring revenue retained from existing customers over a given period, **including** the impact of expansion (upsells, cross-sells, price increases), contraction (downgrades), and churn (cancellations). An NRR above 100% means the existing customer base is growing without any new customer acquisition.

*Why does it matter?*

NRR is the single most important indicator of long-term SaaS business health. Investors and boards treat it as a proxy for product-market fit and customer satisfaction. A company with 115% NRR grows 15% annually from its existing base alone, before counting any new sales [1].

*Key insight:*

> NRR is the "compounding engine" of a SaaS business. A 5-point difference in NRR (say, 105% vs 110%) compounds dramatically over time -- after 5 years, the 110% cohort is worth 26% more than the 105% cohort from the same starting revenue.

*Examples:*

| Context | Example |
|---------|---------|
| Strong expansion motion | Company with 90% GRR but 120% NRR: losing 10% to churn/contraction but making up for it with 30% expansion from existing accounts |
| Stagnant base | Company with 95% GRR and 97% NRR: low churn but almost no expansion, signaling limited upsell paths |
| Healthy mid-market | Company with 92% GRR and 108% NRR: typical pattern for $10M-$50M ARR B2B SaaS with seat-based pricing |

*Common misunderstandings:*

- **Misconception:** High NRR means low churn.
  **Reality:** NRR can mask significant churn if expansion is strong. A company can lose 20% of customers but still show 110% NRR through upsells. Always check GRR alongside NRR.

- **Misconception:** NRR below 100% means the business is failing.
  **Reality:** Early-stage companies without mature upsell motions commonly run 95-100% NRR. The issue is only critical if GRR is also below 85% [2].

### Gross Revenue Retention (GRR)

*What is it?*

Gross Revenue Retention measures the percentage of recurring revenue retained from existing customers, **excluding** expansion revenue. GRR captures only downgrades and churn -- it answers "how much of what we had are we keeping?" GRR is capped at 100% by definition.

*Why does it matter?*

GRR isolates the "leaky bucket" problem. While NRR can hide churn behind expansion, GRR shows the raw retention floor. A company with 80% GRR is losing 20% of its revenue base annually before any upsell -- that is an unsustainable foundation regardless of how strong expansion is.

*Key insight:*

> GRR is the floor of your business; NRR is the ceiling. You can only build the ceiling as high as the floor is solid. A company with 80% GRR needs 25% expansion just to break even on NRR, leaving zero room for error.

*Examples:*

| Context | Example |
|---------|---------|
| Enterprise with sticky contracts | GRR of 95%: minimal churn, long-term contracts, switching costs are high |
| SMB with monthly billing | GRR of 82%: high logo churn typical of self-serve, low-ACV models |
| Mid-market with product gaps | GRR of 87%: losing accounts to competitors on specific feature sets |

*Common misunderstandings:*

- **Misconception:** GRR close to 100% means everything is fine.
  **Reality:** GRR of 98% with NRR of 99% means almost no expansion. The company is retaining but not growing its base -- a different kind of problem.

- **Misconception:** GRR and NRR can be compared directly between segments.
  **Reality:** Enterprise segments naturally have higher GRR (90-95%) than SMB (75-85%) due to contract structure and switching costs [7]. Compare within segment, not across.

### Churn Types: Logo vs. Revenue, Voluntary vs. Involuntary

*What is it?*

Churn is not a single metric -- it splits along two axes. **Logo churn** counts the number of customers lost; **revenue churn** measures the dollar value lost. **Voluntary churn** is when customers actively decide to leave (cancellation, competitive switch); **involuntary churn** is when customers leave passively (failed payment, expired card, non-renewal by oversight) [3].

*Why does it matter?*

Each churn type points to a different root cause and requires a different intervention. Treating all churn the same leads to misdirected effort. A company with high involuntary churn needs better dunning and payment recovery, not product improvements.

*The Framework:*

```
                    Voluntary                 Involuntary
                    (Customer decides)        (Payment/process failure)
Logo Churn          Competitive loss,         Expired card,
(# of customers)    poor fit, budget cut      failed payment

Revenue Churn       Downgrade, partial        Auto-downgrade from
($ value lost)      cancellation              payment failure
```

*Common misunderstandings:*

- **Misconception:** Involuntary churn is a small problem.
  **Reality:** Involuntary churn accounts for roughly 20-40% of total churn in SaaS companies [4]. For companies with monthly billing, it can be even higher. Proper dunning and payment retry logic can recover 30-70% of failed payments.

- **Misconception:** Logo churn and revenue churn tell the same story.
  **Reality:** Losing 10 small accounts (high logo churn) has a completely different impact than losing 1 enterprise account (high revenue churn). Always report both dimensions.

### The ARR Waterfall (Bridge)

*What is it?*

The ARR waterfall (also called an ARR bridge) is a visualization that shows how recurring revenue moves from one period to the next. It breaks down the components: Beginning ARR + New Business + Expansion - Contraction - Churn = Ending ARR. Each component is shown as a separate bar, making it clear where revenue is growing and where it is leaking [5].

*Why does it matter?*

The ARR waterfall is the primary communication tool between CS, Finance, and leadership for retention reporting. It turns abstract percentages into concrete dollar movements. When the board asks "what happened to revenue this quarter?", the waterfall answers it visually.

*Key insight:*

> The waterfall is not just a chart -- it is the data model. If you cannot produce a clean waterfall, your underlying data has gaps. Every dollar of ARR must be categorizable into one of the movement types, or the model breaks.

*Examples:*

| Context | Example |
|---------|---------|
| Quarterly board report | Waterfall showing: $10M starting ARR + $1.5M new + $800K expansion - $200K contraction - $600K churn = $11.5M ending ARR |
| CS team review | Waterfall filtered to a single segment showing which tier is driving churn vs. expansion |
| Finance reconciliation | Waterfall compared against billing system totals to validate data accuracy |

### Cohort-Based vs. Period-Based Measurement

*What is it?*

**Period-based measurement** compares total revenue at the start and end of a time period (e.g., Q1 start vs. Q1 end) across all active customers. **Cohort-based measurement** groups customers by a shared attribute (sign-up date, contract start) and tracks each cohort's revenue over time independently.

*Why does it matter?*

Period-based measurement can be misleading because new customer additions and churned customer removals happen continuously within the period. Cohort analysis controls for this by holding the customer set constant, producing a more accurate picture of true retention behavior.

*Key insight:*

> Period-based NRR can look artificially high when new customers expand quickly in their first months. Cohort-based NRR strips out this noise and shows how a stable set of customers actually behaves over time.

*Common misunderstandings:*

- **Misconception:** Period-based and cohort-based give the same answer.
  **Reality:** They can diverge significantly. A fast-growing company adding many new accounts may see 5-10 points of difference between the two methods, because period-based includes "expansion" from recently acquired customers that are still ramping.

---

## 2) Decision Frameworks

### Approach Selection Matrix

| Situation | Recommended Approach | Why |
|-----------|---------------------|-----|
| Early-stage, &lt;$5M ARR, limited data | Period-based monthly with simple formulas | Not enough cohort depth; keep it simple and auditable |
| Growth-stage, $5M-$30M ARR, mixed contract terms | Cohort-based quarterly with ARR waterfall | Enough data for cohort analysis; quarterly smooths out noise |
| Mature, >$30M ARR, board/investor reporting | Cohort-based monthly + period-based quarterly reconciliation | Dual approach satisfies both operational and financial audiences |
| Primarily annual contracts | Annual cohort NRR/GRR with quarterly check-ins | Annual cohorts match the natural renewal cycle |
| Primarily monthly contracts | Monthly cohort NRR/GRR with rolling 12-month view | Monthly contracts need higher-frequency measurement |
| Multi-product company | Per-product GRR/NRR plus blended total | Product-level segmentation reveals which products drive churn vs. expansion |

### Scoping Factors

**1. Contract Structure**

- Primarily annual contracts --> Measure on annual cohorts; renewal date is the natural measurement point
- Primarily monthly contracts --> Measure on monthly cohorts; rolling 12-month window smooths seasonality
- Mixed (annual + monthly + multi-year) --> Normalize all to monthly MRR for calculation; segment reporting by contract type

**2. Data Maturity**

- Clean subscription data in CRM with renewal dates --> Full cohort analysis with ARR waterfall; proceed to dashboard build
- Partial data (some fields missing, inconsistent entry) --> Data cleanup phase required before calculations; start with simple period-based while cleaning
- Data in spreadsheets or billing system only --> Extract and model first; cannot build reliable dashboards until data is in a queryable system

**3. Stakeholder Reporting Needs**

- Board/investor reporting --> Needs finance-reconciled numbers; use GAAP-aligned definitions; prioritize accuracy over speed
- CS operational reporting --> Needs actionable renewal pipeline; prioritize timeliness and drill-down over perfection
- Executive weekly review --> Needs trend-line summaries; prioritize simplicity and consistency of methodology

**4. Number of Products/Pricing Tiers**

- Single product, flat pricing --> Straightforward calculation; one ARR waterfall suffices
- Multiple products or usage-based pricing --> Need to define how product swaps count (expansion vs. churn-and-rebook); usage-based adds complexity to "starting MRR" baseline
- Bundled pricing --> Must decide if bundle discount counts as contraction when customer drops one product from bundle

### Simple-Start Approach

*Best for:*
- Companies with less than 12 months of clean subscription data
- Teams that have never tracked retention metrics formally
- Situations where Finance and CS definitions are not yet aligned

*Not recommended for:*
- Companies with complex multi-product pricing
- Board-level reporting at scale-stage companies

*Key differences from standard:*

| Aspect | Standard (Cohort) | Simple-Start (Period) |
|--------|-------------------|-----------------------|
| Measurement unit | Cohort of customers at a point in time | All active customers in the period |
| Complexity | Higher; requires cohort tagging | Lower; just compare start vs. end MRR |
| Accuracy | Higher; controls for new customer additions | Lower; can be distorted by rapid growth |
| Setup time | 2-3 weeks for data modeling | 3-5 days for basic calculation |
| Best output | Cohort retention curves, segmented waterfall | Single NRR/GRR number per period |

### Full Cohort Approach

*Best for:*
- Companies with 12+ months of clean subscription data
- Board and investor reporting
- Multi-segment businesses wanting per-segment retention views

*Not recommended for:*
- Companies still cleaning up foundational subscription data
- Teams without a dedicated analyst or RevOps resource to maintain it

*Key differences from standard:*

| Aspect | Simple-Start | Full Cohort |
|--------|-------------|-------------|
| Segmentation | None or basic | By tier, industry, contract size, cohort quarter |
| Waterfall | Optional | Required; drives board narrative |
| Reconciliation | Against billing totals | Against billing + GAAP recognized revenue |
| Maintenance | Low; update monthly | Medium; requires data quality monitoring |

---

## 3) Benchmarks & Standards

### How to Use Benchmarks

*Benchmarks are guidelines, not rules. Always:*
1. Start with benchmark as baseline
2. Adjust based on client-specific segment (SMB vs. enterprise, industry, contract model)
3. Validate against their actual numbers when available
4. Document deviations and rationale

### NRR Benchmarks by Company Segment

| Segment | Low | Typical (Median) | High | Notes |
|---------|-----|-------------------|------|-------|
| Enterprise (>$50K ACV) | 105% | 118% | 135%+ | High switching costs drive retention; expansion from seat/usage growth |
| Mid-Market ($15K-$50K ACV) | 95% | 108% | 120% | Moderate expansion; renewal rates drive performance |
| SMB (&lt;$15K ACV) | 85% | 97% | 110% | Higher logo churn offset by volume; self-serve expansion limited |
| All B2B SaaS (median) | 95% | 106% | 120%+ | Venture-backed median; bootstrapped companies average 104% |

**Source:** Optifai analysis of 939 B2B SaaS companies (2024); SaaS Capital Annual Survey 2025 [1][6]

**Interpretation:**
- **Below low:** Signals product-market fit issues or pricing misalignment. Investigate churn reasons immediately.
- **Above high:** Strong expansion motion. Verify that expansion is genuine (not reclassified new business or pricing tricks).

### GRR Benchmarks by Company Segment

| Segment | Low | Typical (Median) | High | Notes |
|---------|-----|-------------------|------|-------|
| Enterprise | 90% | 94% | 98% | Long contracts and high switching costs |
| Mid-Market | 85% | 90% | 95% | Variable by industry and competitive intensity |
| SMB | 75% | 85% | 92% | Monthly billing and low switching costs drive higher churn |
| All B2B SaaS (median) | 82% | 90% | 95%+ | Top quartile exceeds 95% |

**Source:** KeyBanc Capital Markets SaaS Survey 2024-2025; Vitally SaaS Churn Benchmarks 2025 [2][7]

**Interpretation:**
- **Below 85%:** Serious retention problem. The business is losing more than 15% of its base annually before expansion. Prioritize churn analysis and root-cause investigation.
- **Above 95%:** Exceptional. Validate that churn is not being hidden (e.g., reactivated accounts counted as retained, or long grace periods masking true cancellation dates).

### Churn Rate Benchmarks

| Metric | Good | Warning | Red Flag |
|--------|------|---------|----------|
| Annual gross revenue churn | &lt;8% | 8-15% | >15% |
| Annual logo churn | &lt;10% | 10-20% | >20% |
| Monthly revenue churn | &lt;0.7% | 0.7-1.5% | >1.5% |
| Involuntary churn as % of total | &lt;20% | 20-35% | >35% |
| Churn reason capture rate | >90% | 70-90% | &lt;70% |

**Source:** Recurly Churn Rate Benchmarks; Vitally SaaS Churn Benchmarks 2025 [4][7]

### Quick Reference Thresholds

| Question | Good | Warning | Red Flag |
|----------|------|---------|----------|
| Is our NRR healthy? | >105% | 95-105% | &lt;95% |
| Is our GRR solid? | >90% | 85-90% | &lt;85% |
| Are we capturing churn reasons? | >90% of churned accounts coded | 70-90% coded | &lt;70% coded |
| Is our renewal pipeline proactive? | Renewals created 90+ days out | 60-90 days out | &lt;60 days or reactive |
| Do Finance and CS numbers match? | &lt;2% variance | 2-5% variance | >5% variance |
| Is our data clean enough to report? | All contracts have start/end dates + values | >90% complete | &lt;90% complete |

---

## 4) Calculations & Scoring

### Formula Quick Reference

| Calculation | Formula | Example |
|-------------|---------|---------|
| GRR | `(Starting MRR - Contraction MRR - Churn MRR) / Starting MRR` | ($500K - $15K - $35K) / $500K = 90.0% |
| NRR | `(Starting MRR + Expansion MRR - Contraction MRR - Churn MRR) / Starting MRR` | ($500K + $60K - $15K - $35K) / $500K = 102.0% |
| Logo Churn Rate | `Customers Lost in Period / Customers at Start of Period` | 8 / 200 = 4.0% |
| Revenue Churn Rate | `MRR Lost to Churn / Starting MRR` | $35K / $500K = 7.0% |
| Net Revenue Churn | `(Churn MRR + Contraction MRR - Expansion MRR) / Starting MRR` | ($35K + $15K - $60K) / $500K = -2.0% (negative = net expansion) |
| Renewal Rate | `Renewed Contracts / Total Contracts Up for Renewal` | 45 / 50 = 90.0% |

### GRR Calculation (Detailed)

**Formula:**
```
GRR = (Starting MRR - Contraction MRR - Churn MRR) / Starting MRR
```

**Variables explained:**
- `Starting MRR` = Total monthly recurring revenue from all active subscriptions at the beginning of the measurement period. Exclude one-time fees (implementation, training, professional services) [8].
- `Contraction MRR` = Revenue lost from customers who downgraded but did not cancel entirely
- `Churn MRR` = Revenue lost from customers who fully cancelled or did not renew

**Worked Example:**

*Scenario: Mid-market B2B SaaS company, quarterly measurement*

```
Given:
- Starting MRR (Jan 1): $500,000 (200 active customers)
- Contraction MRR (Q1): $15,000 (12 customers downgraded)
- Churn MRR (Q1): $35,000 (8 customers cancelled)

Calculate:
- GRR = ($500,000 - $15,000 - $35,000) / $500,000
- GRR = $450,000 / $500,000
- GRR = 90.0%
```

**Validation:**
- This number should be between 75% and 100% (quarterly)
- If below 80% quarterly, investigate whether churn events are being double-counted or if a single large customer departure is skewing results
- GRR can never exceed 100% -- if your calculation shows >100%, expansion is incorrectly included

### NRR Calculation (Detailed)

**Formula:**
```
NRR = (Starting MRR + Expansion MRR - Contraction MRR - Churn MRR) / Starting MRR
```

**Variables explained:**
- `Starting MRR` = Same as GRR (recurring revenue only, no one-time fees)
- `Expansion MRR` = Revenue gained from existing customers through upsells, cross-sells, seat additions, and price increases
- `Contraction MRR` = Revenue lost from downgrades (customer still active)
- `Churn MRR` = Revenue lost from full cancellations

**Worked Example:**

*Scenario: Same company as above, adding expansion data*

```
Given:
- Starting MRR (Jan 1): $500,000 (200 active customers)
- Expansion MRR (Q1): $60,000 (25 customers expanded)
- Contraction MRR (Q1): $15,000 (12 customers downgraded)
- Churn MRR (Q1): $35,000 (8 customers cancelled)

Calculate:
- NRR = ($500,000 + $60,000 - $15,000 - $35,000) / $500,000
- NRR = $510,000 / $500,000
- NRR = 102.0%
```

**Validation:**
- NRR above 100% means expansion exceeds losses -- the existing base is growing
- NRR above 130% is unusual and warrants investigation (verify expansion is not reclassified new business)
- If NRR is below GRR, something is wrong in the calculation (NRR >= GRR always, since NRR adds expansion)

### ARR Waterfall Calculation

**Formula:**
```
Ending ARR = Beginning ARR + New ARR + Expansion ARR - Contraction ARR - Churn ARR
```

**Worked Example:**

*Scenario: Annual ARR waterfall for board reporting*

```
Given:
- Beginning ARR (Jan 1): $6,000,000
- New ARR (full year): $1,800,000 (from new customers)
- Expansion ARR: $720,000 (from existing customers)
- Contraction ARR: $180,000 (from downgrades)
- Churn ARR: $420,000 (from cancellations)

Calculate:
- Ending ARR = $6,000,000 + $1,800,000 + $720,000 - $180,000 - $420,000
- Ending ARR = $7,920,000

Derived metrics:
- GRR = ($6,000,000 - $180,000 - $420,000) / $6,000,000 = 90.0%
- NRR = ($6,000,000 + $720,000 - $180,000 - $420,000) / $6,000,000 = 102.0%
- Net New ARR = $1,920,000 ($1,800,000 new + $720,000 expansion - $180,000 contraction - $420,000 churn)
- ARR Growth Rate = $1,920,000 / $6,000,000 = 32.0%
```

### Cohort Retention Calculation

**Formula:**
```
Cohort NRR (12-month) = ARR of Cohort at Month 12 / ARR of Cohort at Month 0
```

**Worked Example:**

*Scenario: Q1 2024 cohort analysis*

```
Given (Q1 2024 cohort = 30 customers signed in Q1):
- Cohort ARR at sign-up (Month 0): $900,000
- By Month 12:
  - 27 customers still active
  - 3 customers churned (ARR: $90,000)
  - 5 customers expanded (added $75,000)
  - 2 customers downgraded (lost $20,000)

Calculate:
- Cohort ARR at Month 12 = $900,000 - $90,000 + $75,000 - $20,000 = $865,000
- Cohort NRR = $865,000 / $900,000 = 96.1%
- Cohort GRR = ($900,000 - $90,000 - $20,000) / $900,000 = 87.8%
- Cohort Logo Retention = 27 / 30 = 90.0%
```

---

## 5) Edge Cases & Deep Dives

### Edge Case 1: Multi-Year Contracts

*Scenario:*

A customer signs a 3-year contract at $120K/year. No renewal event occurs until Year 3. How do you count this customer in Year 1 and Year 2 retention metrics?

*Challenge:*

If you only measure retention at renewal events, multi-year contracts artificially inflate GRR/NRR because these "guaranteed" customers never appear as renewal candidates. But if you include them, they always show as 100% retained, which also inflates the metric.

*Approach:*

1. Include multi-year contracts in the denominator (Starting MRR) every period
2. Treat them as 100% retained for GRR/NRR in non-renewal years (they are, contractually)
3. Segment reporting: show "up for renewal" cohort separately from "under contract" cohort
4. Create a blended metric and a "renewal cohort" metric -- board sees both

*Key validation:*

Compare your "up for renewal" GRR/NRR against your "all customers" GRR/NRR. The "up for renewal" number is the true test of retention strength. If they diverge by more than 5 points, multi-year contracts are masking churn risk.

### Edge Case 2: Mid-Contract Downgrades and Expansions

*Scenario:*

A customer on an annual contract downgrades from the Enterprise tier ($5K/month) to the Pro tier ($3K/month) six months into the contract. When does the $2K/month contraction count?

*Challenge:*

If contraction is recognized immediately, it shows up in the current period and distorts the cohort that was measured at contract start. If deferred to renewal, the dashboard shows misleading "healthy" retention until the renewal date.

*Approach:*

1. Recognize the contraction at the effective date of the change (when MRR actually changes in the billing system)
2. Do not spread the contraction over the remaining term -- take the MRR reduction immediately [8]
3. Adjust the customer's "Starting MRR" for the next measurement period to reflect the new rate
4. Document the timing policy in the Metric Definitions Guide so Finance and CS interpret the same way

*Key validation:*

Run a reconciliation: sum of all individual customer MRR changes should equal the difference between Beginning and Ending MRR in the waterfall. If it does not, there are unaccounted-for mid-contract changes.

### Edge Case 3: Implementation Fees and Non-Recurring Revenue in ARR

*Scenario:*

A customer signs for $90K/year subscription + $10K one-time implementation fee. Year 1 total billing is $100K. Year 2 billing is $90K. Does this look like 10% contraction?

*Challenge:*

Including non-recurring revenue in ARR makes Year 2 look like a downgrade when it is actually flat retention. This is one of the most common data quality issues in retention reporting [8].

*Approach:*

1. Exclude all one-time fees from ARR and MRR calculations -- implementation, training, professional services, setup fees
2. Tag revenue line items in the billing system as "recurring" vs. "non-recurring"
3. Build validation reports that flag any customer whose ARR decreased by exactly the amount of a known non-recurring fee
4. Document the exclusion policy in the Metric Definitions Guide

*Key validation:*

GRR should not change when you add or remove a non-recurring fee. If excluding implementation fees causes GRR to jump by 3+ points, you have a data tagging problem.

### Edge Case 4: Early Renewals and Late Renewals

*Scenario:*

A customer's contract is up for renewal on March 31. They sign a renewal on February 15 (early) or May 10 (late, with month-to-month holdover).

*Challenge:*

Early renewals can create duplicate ARR in the overlap period if both old and new contracts are counted. Late renewals create ambiguity: is the customer churned until they sign, or retained with a gap?

*Approach:*

1. **Early renewals:** Use the new contract start date as the "renewal event" date. Do not double-count ARR during the overlap period. If the renewal includes an expansion, recognize the expansion at the new contract start date.
2. **Late renewals:** Define a "grace period" (typically 30-60 days past contract end). If the customer renews within the grace period, treat them as retained and backdate the renewal event to the original end date. If they renew after the grace period, treat as churn-and-rebook (new business, not renewal).
3. Document the grace period policy and apply it consistently.

*Key validation:*

Check your renewal rate calculation: the denominator should be "contracts expiring in the period" and the numerator "contracts renewed." Late renewals inside the grace period should appear as "renewed" in the original period, not the period they actually signed.

### Edge Case 5: Conflicting Definitions Between Finance and CS

*Scenario:*

Finance calculates GRR at 92% using recognized revenue from the billing system. CS calculates GRR at 88% using CRM opportunity data. The board sees two different numbers.

*Challenge:*

This is the most common and most politically charged edge case in retention reporting. Different source systems, different definitions (recognized revenue vs. contracted ARR), and different timing (invoice date vs. renewal date) produce different answers.

*Approach:*

1. Identify the source of divergence: run both calculations on the same customer set and compare line by line
2. Common causes: (a) timing differences -- Finance uses invoice date, CS uses contract start date; (b) scope differences -- Finance includes all revenue, CS excludes professional services; (c) definition differences -- Finance treats partial-year contracts differently
3. Agree on a single "source of truth" definition and document it. Typically, Finance's number wins for board reporting, but CS needs an operational metric that aligns.
4. Build a reconciliation report that shows: CS number, Finance number, and the bridge between them (timing adjustments, scope adjustments, definition adjustments).

*Key validation:*

The two numbers should be within 2% after reconciliation adjustments. If they diverge by more than 5%, there is a fundamental data or definition problem that needs resolution before any dashboard is published.

---

## References

[1] [Optifai - B2B SaaS NRR Benchmark: 97-118% by Segment (939 Companies)](https://optif.ai/learn/questions/b2b-saas-net-revenue-retention-benchmark/)
[2] [SaaS Capital - Benchmarking Metrics for Bootstrapped SaaS Companies 2025](https://www.saas-capital.com/blog-posts/benchmarking-metrics-for-bootstrapped-saas-companies/)
[3] [Paddle - Customer Churn 101: Types of Churn](https://www.paddle.com/resources/customer-churn)
[4] [Recurly - Customer Churn Rate Benchmarks](https://recurly.com/research/churn-rate-benchmarks/)
[5] [AccountAim - ARR Waterfall Analysis](https://www.accountaim.com/arr-waterfall-analysis/)
[6] [Pavilion - 2025 B2B SaaS Benchmarks](https://www.joinpavilion.com/resource/b2b-saas-performance-benchmarks)
[7] [Vitally - B2B SaaS Churn Rate Benchmarks 2025](https://www.vitally.io/post/saas-churn-benchmarks)
[8] [SaaS Capital - Pitfalls in Measuring SaaS Churn](https://www.saas-capital.com/blog-posts/grrumbling-about-retention-metrics-or-pitfalls-in-measuring-saas-churn/)
