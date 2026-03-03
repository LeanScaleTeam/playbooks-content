# Commission Plan Design and Implementation — Methodology

This document covers the core concepts, frameworks, and calculations behind Commission Plan Design and Implementation. It provides the methodological foundation — the 'how it works' behind the execution steps.

---

## 1) Core Concepts

### The Commission Basis Spectrum

*What is it?*

The commission basis is the revenue metric on which commissions are calculated. B2B SaaS companies must choose between several options — Annual Contract Value (ACV), Total Contract Value (TCV), Monthly Recurring Revenue (MRR), bookings, or collected revenue — each of which creates different incentive dynamics and timing implications.

*Why does it matter?*

The commission basis determines what behaviors reps optimize for. ACV incentivizes annual commitments. TCV incentivizes multi-year deals. MRR incentivizes monthly volume. Collected revenue delays payouts but aligns sales and finance. Choosing the wrong basis misaligns rep behavior with company strategy — for example, paying on TCV when the company needs cash flow from annual deals.

*Key insight:*

> The commission basis is the single most important design decision because it defines what reps see as "the number." Every other plan element (rates, accelerators, thresholds) operates downstream of this choice. Get this wrong and no amount of accelerator tuning will fix the incentive misalignment.

*Examples:*

| Context | Commission Basis | Rationale |
|---------|-----------------|-----------|
| Early-stage SaaS ($5M-$15M ARR) focused on land-and-expand | ACV on new business | Drives annual commitments; keeps plan simple at a stage where the company needs predictability |
| Growth-stage SaaS prioritizing long-term retention | TCV with multi-year kickers | Rewards reps for locking in 2-3 year contracts that reduce churn risk |
| Usage-based SaaS with monthly billing | MRR or net-new ARR | Aligns with how the company recognizes revenue and how customers buy |
| Company with long implementation timelines (90+ days to go-live) | Milestone-based (70% at close, 30% at go-live) | Prevents reps from closing bad-fit deals that never implement |

### Pay Mix and Variable Compensation Architecture

*What is it?*

Pay mix is the ratio of base salary to variable (at-risk) compensation that makes up a rep's On-Target Earnings (OTE). The median pay mix for SaaS AEs is approximately 53% base / 47% variable [1], though the standard benchmark remains 50/50 for quota-carrying AEs. SDRs and BDRs typically sit at 60/40 or 70/30 base-heavy, while enterprise AEs and sales leaders may extend to 40/60 favoring variable.

*Why does it matter?*

Pay mix signals the company's risk appetite and the rep's expected control over outcomes. A higher variable component rewards top performers disproportionately but increases turnover risk among mid-performers. A higher base component provides stability but reduces the gap between top and bottom performers — weakening the pay-for-performance signal.

*The Framework:*

```
Risk Tolerance Scale (Base : Variable)

Low Risk                                          High Risk
(for rep)                                         (for rep)
70:30 ──── 60:40 ──── 50:50 ──── 40:60 ──── 30:70
SDR/BDR    Mid-Market   Standard    Enterprise    CEO/Founder
                         AE         AE (long       Sales
                                    cycle)
```

*Common misunderstandings:*

- **Misconception:** A 50/50 pay mix means reps earn half their salary if they miss quota.
  **Reality:** 50/50 is the *at-target* split. Most plans include a threshold (typically 50-70% of quota) below which variable pay is reduced but not zero. A rep at 60% attainment on a 50/50 plan still earns their full base plus a reduced variable component.

- **Misconception:** Higher variable pay always attracts better talent.
  **Reality:** Experienced enterprise reps often prefer a slightly higher base because their deal cycles are 6-12 months and cash flow matters. The variable component's *structure* (accelerators, uncapped upside) matters more than its raw percentage.

### Accelerators and Decelerators

*What is it?*

Accelerators increase the commission rate once a rep exceeds a threshold (typically 100% quota attainment). Decelerators reduce the commission rate below a certain attainment threshold, acting as a cost-control mechanism for underperformance. Approximately 82% of SaaS companies use accelerators [2], and the typical accelerator boosts payout by 20-30% above the base rate for quota-exceeding performance.

*Why does it matter?*

Accelerators are the primary tool for retaining and motivating top performers. Without them, a rep at 120% attainment earns the same rate as a rep at 101%, removing incentive to push beyond quota. Decelerators protect company margins when reps underperform but must be balanced carefully — overly aggressive decelerators (below 50% of quota = $0 commission) can demoralize struggling reps and accelerate turnover.

*Key insight:*

> Fewer than 15% of SaaS companies cap commissions [2]. Uncapped plans with strong accelerators consistently outperform capped plans in rep satisfaction and top-performer retention. If Finance pushes for caps, propose a multi-tier accelerator with decreasing marginal rates instead — it provides budget predictability without a hard ceiling.

*Examples:*

| Context | Example |
|---------|---------|
| Standard 3-tier structure | 0-50% quota: 5% rate (decelerator); 50-100% quota: 10% base rate; 100%+: 15% accelerated rate |
| Aggressive accelerator for top performers | 100-120% quota: 1.5x base rate; 120-150% quota: 2x base rate; 150%+: 2.5x base rate |
| Decelerator as cap alternative | Instead of capping at 150% of OTE, rate steps down from 2x to 1.25x above 200% attainment |

### Clawback Mechanics

*What is it?*

A clawback provision recovers previously paid commissions when a customer churns, downgrades, or fails to pay within a defined period after the deal closes. 53% of SaaS companies use clawbacks [3], making them a standard (though controversial) plan element. The typical clawback window is 3-12 months post-close.

*Why does it matter?*

Clawbacks align rep incentives with customer retention by creating a financial consequence for closing bad-fit deals. Companies that implement clawbacks often see up to a 15% reduction in customer churn rates [4] because reps become more selective about deal quality. However, poorly designed clawbacks (too broad, too long, or applied retroactively) destroy rep trust and increase turnover.

*Common misunderstandings:*

- **Misconception:** Clawbacks should apply to all churn regardless of cause.
  **Reality:** Effective clawbacks distinguish between rep-controllable churn (bad-fit customer, oversold features) and company-controllable churn (product failure, poor onboarding). Clawing back commissions for product failures punishes reps for company shortcomings and erodes plan credibility.

- **Misconception:** Longer clawback windows are always better for the company.
  **Reality:** Windows beyond 6 months create administrative complexity and rep anxiety that outweigh the financial protection. A 90-day full clawback with a 90-180 day prorated clawback balances protection with fairness.

### Rules of Engagement (Deal Crediting Logic)

*What is it?*

Rules of engagement (RoE) define who gets credit for a deal and how credit is split when multiple reps, teams, or roles contribute to a closed opportunity. RoE covers territory assignments, account ownership, inbound vs. outbound sourcing, handoff rules, and split-credit scenarios.

*Why does it matter?*

Unclear crediting rules are the single largest source of commission disputes. When two AEs both claim credit for the same deal, or an SDR's sourced lead gets credited to marketing, trust in the compensation system breaks down. Clear RoE documented before plan launch prevents the majority of disputes.

*Key insight:*

> The best RoE documents are tested against 20-30 historical deal scenarios before going live. If the rules produce an unexpected or unfair result on any historical deal, revise the rules — not the outcome. Ad-hoc exceptions undermine the entire system.

---

## 2) Decision Frameworks

### Approach Selection Matrix

| Situation | Recommended Approach | Why |
|-----------|---------------------|-----|
| Early-stage SaaS ($5M-$15M ARR), &lt; 10 AEs | Simple flat-rate plan with 1 accelerator tier | Keep plan simple. Reps need to calculate their commission on a deal in &lt; 60 seconds. Only 24% of reps can easily calculate their earnings in complex plans [5]. |
| Growth-stage SaaS ($15M-$50M ARR), multiple segments | Tiered plan with role-specific rates and 2-3 accelerator tiers | Company has enough data to differentiate rates by segment (SMB vs. Mid-Market vs. Enterprise) and set meaningful tiers. |
| Enterprise SaaS ($50M+ ARR), long sales cycles (6+ months) | Multi-component plan with milestone payouts, SPIFFs, and team overlays | Deals are complex enough to warrant splitting commission across milestones (contract, implementation, expansion) and crediting multiple roles. |
| Usage-based or PLG SaaS | Net-new ARR basis with expansion commissions | Traditional ACV-based plans break when revenue is consumption-driven. Pay on net-new ARR to align with how the business grows. |
| Company with high churn (&gt;15% annual) | Plan with clawbacks and customer-quality kickers | Must address churn at the incentive level — rewarding deal quality, not just volume. |

### Scoping Factors

**1. Number of Covered Roles**

- 1-2 roles (AE only, or AE + SDR) → Single plan document with role-specific rate tables
- 3-5 roles (AE, SDR, AM, CS, SE) → Multiple plan documents with shared RoE framework
- 6+ roles (including overlays, channel, management) → Full compensation architecture with governance committee

**2. Commission Basis Complexity**

- Single metric (ACV or ARR) → Straightforward calculation, spreadsheet-trackable
- Dual metric (new business ACV + expansion ARR) → Requires weighting and potential double-counting rules
- Multi-metric (new ACV + expansion + retention + product mix) → Requires commission software; spreadsheets will fail at scale

**3. Tracking System Maturity**

- No existing tracking → Build structured spreadsheets first, plan for software adoption at 20+ reps
- Spreadsheet-based → Evaluate whether current process can support new plan complexity; migrate to software if &gt; 3 commission components
- Commission software in place → Configure new plan within existing platform; validate calculation logic

**4. Data Quality in CRM**

- Clean opportunity data (amounts, dates, owners consistently populated) → Can proceed with automation immediately
- Moderate data issues (some fields inconsistent) → Include 2-4 week data cleanup sprint before commission system configuration
- Poor data quality → Must fix CRM data hygiene before commission tracking is viable; this is a prerequisite project

### Flat-Rate vs. Tiered Plan

*Best for flat-rate:*
- Early-stage companies with &lt; 10 reps
- Transactional sales with short cycles (&lt; 30 days)
- Companies launching their first formal commission plan

*Not recommended for flat-rate:*
- Companies with wide variation in deal size
- Organizations wanting to differentiate top-performer compensation
- Companies with multiple product lines requiring different incentive weights

*Best for tiered:*
- Growth-stage companies with established quota methodology
- Companies with clear attainment benchmarks from historical data
- Organizations that want to drive overperformance

*Not recommended for tiered:*
- Companies without 6+ months of historical attainment data to set tiers
- Organizations where quota methodology is still being established
- Companies with fewer than 5 reps (sample size too small for tier design)

| Aspect | Flat-Rate | Tiered |
|--------|-----------|--------|
| Simplicity | Rep calculates commission instantly | Requires attainment tracking to know current rate |
| Top performer upside | Same rate regardless of performance | Higher rates reward exceeding quota |
| Budget predictability | Highly predictable (linear cost) | Less predictable (accelerators create non-linear cost) |
| Administration | Minimal — multiply deal size by rate | Moderate — requires attainment calculation each period |
| Rep perception | Fair but not exciting | Motivating for top performers, potentially frustrating for mid-performers |

### Commission Software Selection Framework

| Factor | Spreadsheet | QuotaPath | CaptivateIQ | Everstage |
|--------|-------------|-----------|-------------|-----------|
| Best for | &lt; 20 reps, simple plans | 20-100 reps, SMB/Mid-Market | 100-500 reps, complex plans | 50-300 reps, fast deployment |
| Plan complexity | 1-2 components | 2-4 components | Unlimited | Unlimited |
| Implementation time | 1-2 weeks | 4-6 weeks | 4-6 months | 6-8 weeks |
| Annual cost (50 reps) | $0 (internal labor) | $15K-$30K | $30K-$50K | $25K-$45K |
| CRM integration | Manual export | Native Salesforce/HubSpot | Native Salesforce/HubSpot | Native Salesforce/HubSpot |
| Self-service for reps | Limited (shared spreadsheet) | Strong (rep portal) | Strong (rep portal) | Strong (rep portal) |
| Key trade-off | Free but error-prone, doesn't scale | Fast to deploy but limited depth | Most flexible but longest implementation | Modern UX but newer vendor |

*Source: Vendor documentation and G2/Gartner peer reviews, 2024-2025* [6][7][8]

---

## 3) Benchmarks & Standards

### How to Use Benchmarks

*Benchmarks are guidelines, not rules. Always:*
1. Start with benchmark as baseline
2. Adjust based on client-specific data (company stage, market, role, geography)
3. Validate against their actual numbers when available
4. Document deviations and rationale

### Commission Rate Benchmarks

| Metric | Low | Typical | High | Notes |
|--------|-----|---------|------|-------|
| AE base commission rate (on ACV) | 8% | 10-12% | 15% | Median at 100% attainment is 11.5% [1]. Higher rates for complex enterprise sales. |
| SDR commission (per qualified meeting/SQL) | $50 | $100-$250 | $500 | Or 2-5% of pipeline generated. Flat-rate per meeting common at early stage. |
| Account Manager commission (on expansion) | 5% | 7-10% | 12% | Lower than new business because AM has lower cost of sale. |
| Customer Success commission (on renewal) | 1% | 2-5% | 8% | Bonus-based more common than commission-based for CS. |
| Accelerator rate (above 100% quota) | 1.2x | 1.5x | 2.5x | Typical boost is 20-30% above base rate [2]. Multi-tier preferred. |

**Source:** Everstage Sales Compensation Statistics 2025 [1], ActivatedScale SaaS Benchmarks 2025 [9]

**Interpretation:**
- **Below low:** Rates below 8% on ACV for AEs signal underpayment relative to market. Expect difficulty attracting talent and high turnover.
- **Above high:** Rates above 15% on ACV may indicate the company is overcompensating on variable vs. base, or that quota is set too high (pushing rates up to keep OTE competitive).

### Pay Mix & OTE Benchmarks

| Metric | Low | Typical | High | Notes |
|--------|-----|---------|------|-------|
| AE pay mix (base:variable) | 60:40 | 50:50 | 40:60 | Median in 2024 is 53:47 [1]. Enterprise AEs trend toward 45:55. |
| SDR pay mix | 70:30 | 65:35 | 55:45 | Higher base because SDRs have less control over deal outcomes. |
| AE OTE (Mid-Market SaaS) | $140K | $180K-$200K | $250K+ | Median AE OTE hit $190K in 2024 [1]. Geography and company stage drive variation. |
| SDR OTE | $65K | $75K-$85K | $100K | SDR base averages $57,739 [1]. |
| Quota-to-OTE ratio | 3.2x | 4x-5x | 6x+ | Median 4.2x in 2024 [1]. Ratios above 6x may indicate quota is unrealistically high. |

**Source:** Everstage Sales Compensation Statistics 2025 [1], ActivatedScale SaaS Benchmarks 2025 [9]

### Plan Design Benchmarks

| Metric | Low | Typical | High | Notes |
|--------|-----|---------|------|-------|
| Quota attainment threshold | 0% (first dollar) | 50-70% | 80% | Threshold below which variable pay is reduced or zero. |
| Ramp period for new hires | 1 month | 3-4 months | 6 months | Common ramp: 25%/50%/75%/100% over 4 months. |
| Clawback window | 30 days | 90 days | 12 months | 53% of SaaS companies use clawbacks [3]. |
| Commission cap | Uncapped | Uncapped | 2-3x OTE | Fewer than 15% of SaaS companies cap [2]. |
| Number of plan components | 1 | 2-3 | 5+ | Limit to 2-3 metrics per role for clarity [5]. |
| Quota attainment distribution (healthy) | 40% of reps | 60-70% of reps | 80%+ of reps | If &lt;40% hit quota, quotas may be unrealistic. If &gt;80%, quotas are likely too easy. |

### Quick Reference Thresholds

| Question | Good | Warning | Red Flag |
|----------|------|---------|----------|
| What % of reps hit quota? | 55-70% | 40-55% or 70-85% | &lt;40% or &gt;85% |
| Commission expense as % of revenue | 8-12% | 12-18% | &gt;18% or &lt;5% |
| Disputes per payout cycle | &lt;5% of reps | 5-15% of reps | &gt;15% of reps |
| Payout error rate | &lt;1% | 1-3% | &gt;3% |
| Time to calculate commissions | &lt; 2 days | 2-5 days | &gt; 5 business days |
| Rep dashboard adoption (first 30 days) | &gt;80% | 50-80% | &lt;50% |

---

## 4) Calculations & Scoring

### Formula Quick Reference

| Calculation | Formula | Example |
|-------------|---------|---------|
| OTE | `Base Salary + Target Variable` | $100K base + $100K variable = $200K OTE |
| Quota (from OTE) | `OTE x Quota-to-OTE Ratio` | $200K OTE x 5x = $1M annual quota |
| Base commission rate | `Target Variable / Annual Quota` | $100K / $1M = 10% |
| Commission on a deal | `Deal ACV x Commission Rate x Attainment Multiplier` | $50K ACV x 10% x 1.0 = $5,000 |
| Quota attainment | `(Closed Revenue / Quota) x 100` | ($400K / $500K) x 100 = 80% attainment |
| Ramp quota | `Full Quota x Ramp %` | $250K quarterly x 50% ramp = $125K ramp quota |
| Clawback amount | `Commission Paid x (1 - Days Active / Clawback Window)` | $5,000 x (1 - 45/90) = $2,500 clawback |

### OTE and Quota Design

**Formula:**
```
OTE = Base Salary + Target Variable Pay
Annual Quota = OTE x Quota-to-OTE Ratio
Base Commission Rate = Target Variable Pay / Annual Quota
```

**Variables explained:**
- `Base Salary` = Fixed compensation, paid regardless of performance
- `Target Variable Pay` = Variable compensation earned at exactly 100% quota attainment
- `Quota-to-OTE Ratio` = Multiplier expressing how much revenue a rep must produce relative to their total comp. Industry median: 4.2x [1]
- `Base Commission Rate` = The percentage earned on each dollar of closed revenue at standard attainment

**Worked Example:**

*Scenario: Design compensation for a Mid-Market AE at a $30M ARR SaaS company*

```
Given:
- Market-competitive base salary: $100,000
- Pay mix target: 50/50
- Quota-to-OTE ratio: 5x (company growth stage)

Calculate:
- OTE = $100,000 + $100,000 = $200,000
- Annual Quota = $200,000 x 5 = $1,000,000
- Quarterly Quota = $1,000,000 / 4 = $250,000
- Base Commission Rate = $100,000 / $1,000,000 = 10% on ACV

Validation:
- 10% commission rate falls within typical range (8-15%)
- $250K quarterly quota is achievable for Mid-Market
- OTE of $200K aligns with market median ($190K in 2024)
```

**Validation:**
- Commission rate should be between 8% and 15% on ACV for AEs
- If rate falls outside this range, revisit either the pay mix or the quota-to-OTE ratio
- If quota feels unrealistically high, reduce the ratio; if OTE seems too low, increase base or variable

### Tiered Commission Calculation

**Formula:**
```
Total Commission = Sum of (Revenue in Tier x Tier Rate) for each tier

Tier 1: 0% to Threshold → Rate_1 (decelerator or reduced rate)
Tier 2: Threshold to 100% → Rate_2 (base rate)
Tier 3: 100% to Cap/Unlimited → Rate_3 (accelerated rate)
```

**Worked Example:**

*Scenario: AE with $250K quarterly quota, 10% base rate, 3-tier structure*

```
Plan design:
- Tier 1 (0-50% attainment / $0-$125K): 5% rate (decelerator)
- Tier 2 (50-100% attainment / $125K-$250K): 10% rate (base)
- Tier 3 (100%+ attainment / $250K+): 15% rate (accelerator)

Example: AE closes $320K in Q1 (128% attainment)

Calculate:
- Tier 1: $125,000 x 5% = $6,250
- Tier 2: $125,000 x 10% = $12,500
- Tier 3: $70,000 x 15% = $10,500
- Total Commission: $6,250 + $12,500 + $10,500 = $29,250
```

### Ramp Quota Schedule

**Standard 4-Month Ramp:**

| Month | Ramp % | Quarterly Quota Equivalent | Commission Treatment |
|-------|--------|---------------------------|---------------------|
| Month 1 | 25% | $62,500 (on $250K) | Full rate on ramp quota; guarantee or draw common |
| Month 2 | 50% | $125,000 | Full rate on ramp quota |
| Month 3 | 75% | $187,500 | Full rate on ramp quota |
| Month 4+ | 100% | $250,000 | Standard plan applies |

**Draw vs. Guarantee during ramp:**
- **Non-recoverable draw:** Company pays minimum variable during ramp regardless of performance. No payback required. Preferred for competitive hiring.
- **Recoverable draw:** Advance against future commissions. Must be repaid from future earnings. Creates anxiety; use cautiously.
- **Guarantee:** Fixed variable amount for ramp period, with upside if rep exceeds ramp quota. Most rep-friendly option.

### Clawback Calculation

**Formula:**
```
Clawback Amount = Original Commission x Clawback Percentage

Where Clawback Percentage depends on churn timing:
- Churn in Month 1-3: 100% clawback
- Churn in Month 4-6: 50% clawback (prorated)
- Churn in Month 7-12: 25% clawback (prorated)
- Churn after Month 12: No clawback
```

**Worked Example:**

*Scenario: AE closed a $60K ACV deal, earned $6,000 commission (10% rate). Customer churns at Month 5.*

```
Given:
- Commission earned: $6,000
- Churn timing: Month 5 (within 4-6 month window)
- Clawback percentage: 50%

Calculate:
- Clawback amount: $6,000 x 50% = $3,000
- Net commission retained: $6,000 - $3,000 = $3,000

Processing:
- Deducted from next payout cycle (not invoiced to rep)
- If rep has insufficient future commissions, carry balance forward
```

---

## 5) Edge Cases & Deep Dives

### Edge Case 1: Mid-Year Plan Changes

*Scenario:*

Company decides to change commission plan mid-year — new rates, new quotas, or new metrics. This typically happens after a board meeting resets revenue targets, an acquisition changes the product portfolio, or leadership concludes the current plan isn't driving desired behavior.

*Challenge:*

Mid-year changes create a fairness problem: reps made decisions (pipeline building, deal pacing, territory investment) based on the original plan. Changing the rules mid-game can destroy trust and trigger turnover — especially among top performers who built pipeline under the old plan's incentive structure.

*Approach:*

1. Grandfather all deals already in pipeline under the original plan terms (deals with created date before change effective date)
2. Apply new plan only to deals created after the effective date
3. If quotas change, prorate: original quota for months 1-6, new quota for months 7-12, measured independently
4. Provide a transition guarantee: for the first full quarter under the new plan, guarantee reps earn at least 90% of their average quarterly variable from the prior two quarters
5. Communicate changes 30 days before effective date with written documentation

### Edge Case 2: Multi-Product / Multi-Motion Companies

*Scenario:*

Company sells multiple products (e.g., core platform + add-on modules + professional services) or has multiple sales motions (PLG self-serve + sales-assisted + enterprise direct). Different products have different margins, sales cycles, and strategic priorities.

*Challenge:*

A single commission rate across all products either overpays for low-effort/low-margin products or underpays for high-effort/high-value products. Reps will optimize for the easiest path to commission, which may not align with company strategy.

*Approach:*

1. Set product-specific commission rates weighted by strategic priority and gross margin
2. Create a rate card: Core platform at base rate (10%), strategic add-on at premium rate (14%), professional services at reduced rate (5%)
3. Use a "blended attainment" model: quota is total, but commission rate varies by product
4. Add SPIFFs for product launches or strategic pushes (time-limited bonuses)
5. Cap professional services commission to prevent reps from padding deals with unnecessary services

### Edge Case 3: Territory or Account Reassignment Mid-Cycle

*Scenario:*

Accounts are reassigned between reps due to territory realignment, rep departure, or segment restructuring. Deals in various pipeline stages are affected.

*Challenge:*

Who gets credit for deals that started under one rep but close under another? The originating rep built the relationship and pipeline; the receiving rep must close it. Both feel entitled to full credit.

*Approach:*

1. Define a cutoff based on pipeline stage at transfer:
   - Pre-qualification (Stage 1-2): 100% credit to receiving rep
   - Active evaluation (Stage 3-4): Split credit (40% originating / 60% receiving, or per RoE)
   - Late stage (Stage 5+): 80% originating / 20% receiving
2. Time-based override: if deal closes within 30 days of transfer, originating rep gets full credit regardless of stage
3. Document all transfers with effective date and pipeline snapshot in CRM
4. Create a "transfer log" reviewed by RevOps each payout cycle

### Edge Case 4: Company Without Historical Commission Data

*Scenario:*

Startup or early-stage company implementing their first formal commission plan. No historical attainment data, no existing plan to benchmark against, and limited revenue history.

*Challenge:*

Without historical data, every plan element (rates, quotas, thresholds, accelerators) is an educated guess. Setting quotas too high demoralizes the team. Setting them too low overpays and creates budget problems.

*Approach:*

1. Start with industry benchmarks as baseline (see Section 3)
2. Set a conservative quota-to-OTE ratio (4x instead of 5x) to reduce risk of unrealistic quotas
3. Use a 3-month "observation period" where the plan is active but quotas are adjusted retroactively if attainment data reveals systemic issues
4. Design the plan with quarterly quotas (not annual) so you can adjust after Q1
5. Build in a mid-year plan review checkpoint from day one
6. Track all plan economics weekly for the first quarter to spot issues early

### Edge Case 5: Channel / Partner Deal Crediting

*Scenario:*

Company has a channel or partner program where deals are sourced or co-sold with partners. Internal reps may or may not be involved in the sale.

*Challenge:*

Double compensation risk: paying both the partner margin/referral fee AND internal rep commission on the same deal. Conversely, if reps get no credit for partner deals, they will actively block the channel to protect their pipeline.

*Approach:*

1. Partner-sourced, partner-closed (no rep involvement): No internal commission. Partner receives full margin.
2. Partner-sourced, rep-closed: Rep receives 50-75% of standard commission. Partner receives referral fee.
3. Rep-sourced, partner-assisted (overlay model): Rep receives full commission. Partner receives reduced service/implementation fee.
4. Co-sell (both parties active): Rep receives 75% commission. Partner receives co-sell margin. Total cost-of-sale documented and approved by Finance.
5. Document all channel deal types in the RoE with explicit examples.

*Key validation:*

Calculate total cost-of-sale (internal commission + partner fees) for each channel scenario. If total exceeds 25-30% of ACV on any deal type, the economics are unsustainable and rates need adjustment.

---

## References

[1] [Everstage - Sales Compensation Statistics 2025](https://www.everstage.com/sales-compensation/sales-compensation-statistics)
[2] [Everstage - SaaS Sales Compensation Benchmarks](https://www.everstage.com/sales-compensation/saas-sales-compensation-benchmarks)
[3] [Everstage - Sales Commission Clawback 2025 Best Practices](https://www.everstage.com/sales-commission/sales-commission-clawback)
[4] [DemandFarm - Clawback in Sales Commission: A Strategic Guide](https://www.demandfarm.com/blog/clawback-in-sales-commission/)
[5] [Everstage - Sales Compensation Statistics 2025](https://www.everstage.com/sales-compensation/sales-compensation-statistics)
[6] [QuotaPath - CaptivateIQ Alternatives Comparison](https://www.quotapath.com/blog/captivateiq-alternatives/)
[7] [Everstage - CaptivateIQ vs QuotaPath Comparison](https://www.everstage.com/commission-software-comparison/captivateiq-vs-quotapath)
[8] [SelectHub - CaptivateIQ vs QuotaPath 2024](https://www.selecthub.com/sales-commission-software/captivateiq-vs-quotapath/)
[9] [ActivatedScale - SaaS Sales Compensation Benchmarks 2025](https://www.activatedscale.com/blog/saas-sales-compensation-benchmarks)
