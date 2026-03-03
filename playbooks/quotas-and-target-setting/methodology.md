# Quotas and Target Setting — Methodology

This document covers the core concepts, frameworks, and calculations behind Quotas and Target Setting. It provides the methodological foundation — the "how it works" behind the execution steps.

---

## 1) Core Concepts

*The mental models, frameworks, and key distinctions that someone needs to understand before executing this project.*

### Top-Down vs. Bottom-Up vs. Blended Quota Setting

*What is it?*

Three distinct methodologies for allocating revenue targets to individual sellers. **Top-down** starts with the board-approved revenue number and divides it across the sales organization. **Bottom-up** starts with each territory's historical performance, applies growth assumptions, and aggregates upward. **Blended** (also called hybrid) reconciles both approaches to produce quotas that satisfy company targets while remaining achievable at the rep level.

*Why does it matter?*

The methodology choice determines whether quotas are defensible. A top-down-only approach often produces targets disconnected from territory reality, while bottom-up-only may not satisfy investor growth expectations. Forrester reports average quota attainment across B2B organizations is only 47% [1] - often because quotas are set using one methodology without validation from the other.

*Key insight:*

> Blended is the modern standard for enterprise teams because it forces a reconciliation conversation: leadership states what the business needs, field data shows what's realistic, and the gap between the two becomes a strategic decision rather than a hidden risk [2].

*Examples:*

| Context | Example |
|---------|---------|
| Series B SaaS ($15M ARR, targeting $25M) | Top-down says $25M split across 12 AEs = ~$2.1M each. Bottom-up shows historical AE production of $1.4M average. Blended approach identifies the gap requires 4 additional hires or improved win rates to close. |
| Enterprise expansion team | Bottom-up aggregation of existing account potential shows $8M growth capacity. Top-down target is $6M. Blended approach validates the target is achievable and identifies which accounts drive the upside. |
| SMB velocity team scaling from 5 to 15 reps | Top-down divides $4.5M equally ($300K each). Blended approach recognizes 10 ramping reps should carry reduced quotas, loading more onto tenured reps to hit the number. |

*Common misunderstandings:*

- **Misconception:** Bottom-up is always more accurate because it uses historical data.
  **Reality:** Bottom-up can systematically undercount potential. Reps anchor to past performance and may not account for new product lines, marketing investments, or market expansion. Bottom-up aggregated totals frequently fall 15-25% short of board targets [3].

- **Misconception:** Top-down quotas are "unfair" because leadership just picks a number.
  **Reality:** Top-down provides the constraint that forces resource allocation decisions. The problem is not top-down itself - it is when top-down is the *only* methodology, with no validation against territory capacity.

### Territory Weighting

*What is it?*

A scoring methodology that adjusts quota targets based on the relative opportunity within each territory. Rather than assigning identical quotas regardless of market conditions, territory weighting applies multipliers that account for account density, market maturity, competitive intensity, and historical win rates.

*Why does it matter?*

Identical quotas across unequal territories is the single most common cause of perceived quota unfairness. A rep covering Manhattan has structurally different opportunity than a rep covering rural markets. Territory weighting ensures equivalent *opportunity to earn*, not identical *numbers to hit*. Companies that align quotas with territory potential see 14-20% higher attainment rates compared to flat quota distribution [4].

*Key insight:*

> The goal is equivalent opportunity, not identical numbers. A $1.5M quota in a high-density territory and a $900K quota in a low-density territory can represent the same level of difficulty if the weighting factors are calibrated correctly.

*Examples:*

| Context | Example |
|---------|---------|
| Geographic territories (US regions) | Northeast territory weighted at 1.3x (high account density, mature market); Mountain West weighted at 0.7x (sparse accounts, growth market). A $1M base quota becomes $1.3M and $700K respectively. |
| Named account territories | Strategic accounts territory weighted by total addressable contract value rather than account count. 5 enterprise accounts with $2M potential each vs. 50 mid-market accounts with $40K potential each. |
| Vertical territories | Healthcare vertical weighted 0.85x due to longer sales cycles and compliance requirements; Technology vertical weighted 1.15x due to faster adoption and shorter cycles. |

*Common misunderstandings:*

- **Misconception:** Territory weighting makes quota setting too complex.
  **Reality:** A simple 3-4 factor model with 1-5 scoring per factor takes one day to build and dramatically improves fairness perception. Complexity is not the barrier - willingness to differentiate is.

- **Misconception:** Weighted quotas mean some reps have "easier" targets.
  **Reality:** Proper weighting means all reps face equivalent difficulty. If the weighting is correct, attainment distributions should be similar across territories.

### Ramp Schedules and Quota Proration

*What is it?*

A structured timeline defining the percentage of full quota a new hire carries during their first months on the job. Ramp schedules account for onboarding, training, pipeline building, and the natural time required to reach full productivity.

*Why does it matter?*

Without explicit ramp schedules, new hires either carry full quota from day one (demoralizing and inaccurate for forecasting) or carry no quota (creating a coverage gap the team must absorb). The average ramp-up time for SaaS sales reps is 5.3 months for inside sales and 5.8 months for field sales [5]. Companies with structured 30-60-90 day ramp plans see new reps reach quota 25% faster than those with informal onboarding [6].

*Key insight:*

> Ramp schedules are not just an HR exercise - they are a capacity planning input. Every ramping rep is a fractional seller, and the team's total capacity must account for this. A 12-person team with 4 ramping reps has an effective capacity closer to 10 fully-loaded sellers.

*Examples:*

| Context | Example |
|---------|---------|
| SDR ramping (2-3 month cycle) | Month 1: 25% quota (learning ICP, shadowing). Month 2: 50% (running own sequences). Month 3: 75%. Month 4+: 100%. |
| AE ramping (5-6 month cycle) | Month 1-2: 0% quota (training, shadowing). Month 3: 25%. Month 4: 50%. Month 5: 75%. Month 6+: 100%. |
| Account Manager ramping | Month 1: 0% (account transition, relationship building). Month 2: 50% (renewal targets only). Month 3+: 100% (full expansion + renewal quota). |

*Common misunderstandings:*

- **Misconception:** Ramp quota should be based on activities (calls, meetings) rather than revenue.
  **Reality:** Activity-based milestones belong in the onboarding plan, not the quota model. Ramp quotas should still be expressed as a percentage of the revenue target, with activity milestones as leading indicators. SDR ramp schedules are the exception where activity metrics (meetings set, pipeline generated) are the primary quota measure.

- **Misconception:** All new hires should follow the same ramp schedule.
  **Reality:** An experienced AE joining from a competitor with existing relationships may warrant an accelerated ramp (Month 1: 50%, Month 2: 75%, Month 3+: 100%), while a career-changer may need an extended ramp.

### Quota-to-OTE Ratio

*What is it?*

The multiplier between a seller's on-target earnings (OTE) and their assigned quota. A 5x ratio means a rep with $200K OTE carries a $1M quota. This ratio determines the cost of sale and directly impacts the company's unit economics.

*Why does it matter?*

The quota-to-OTE ratio is the primary lever connecting compensation design to quota setting. If the ratio is too low (2-3x), the cost of sale is unsustainable. If it is too high (8x+), quota feels unattainable and drives attrition. The median quota-to-OTE ratio in 2024 is 4.2x, with typical ranges of 3.2x to 4.8x for AEs [7].

*Key insight:*

> A quota-to-OTE ratio below 4x signals either the company is overpaying for the revenue or the quota is too low. A ratio above 6x for new business AEs signals the quota may be unrealistic given the compensation. The "sweet spot" of 4-6x balances seller motivation with company economics.

*The Framework:*

```
Quota-to-OTE Ratio = Annual Quota / Annual OTE

Example: $1,000,000 quota / $200,000 OTE = 5.0x ratio
```

| Role | Typical Ratio | Rationale |
|------|---------------|-----------|
| Field AE (New Business) | 4-6x | High-effort, full sales cycle ownership |
| Inside AE | 4-5x | Smaller deals, higher volume |
| Account Manager (Expansion) | 6-8x | Existing relationships lower effort per dollar |
| SDR (Pipeline Generation) | Not applicable in same way | Measured by meetings/pipeline, not closed revenue |

---

## 2) Decision Frameworks

*Matrices, decision trees, and "when to use what" guidance for quota methodology selection.*

### Approach Selection Matrix

| Situation | Recommended Approach | Why |
|-----------|---------------------|-----|
| Early-stage company (&lt;$5M ARR), limited data | Top-down with market-based validation | Insufficient historical data for bottom-up; use industry benchmarks and market sizing instead |
| Growth-stage company ($5M-$50M ARR), 12+ months CRM data | Blended (top-down + bottom-up reconciliation) | Enough data for meaningful bottom-up analysis; board targets provide top-down constraint |
| Mature organization ($50M+ ARR), stable territories | Bottom-up with top-down ceiling | Deep historical data makes bottom-up reliable; top-down ensures alignment with growth plan |
| New market or product launch | Top-down with aggressive ramp assumptions | No relevant historical data for the new motion; use market sizing and comparable company benchmarks |
| Post-M&A with combined sales teams | Blended with territory re-weighting | Historical data from both organizations needs normalization; territories likely need restructuring |

### Scoping Factors

*The variables that determine which approach, complexity, and timeline apply.*

**1. Data Maturity**

- 24+ months clean CRM data -- Full blended model with back-testing
- 12-24 months CRM data -- Blended model with limited back-testing
- &lt;12 months CRM data -- Top-down with market benchmarks; flag data gaps for future iterations

**2. Sales Organization Complexity**

- Single role type, uniform territories -- Simple allocation model (1-2 weeks to build)
- Multiple roles (AE + SDR + AM), segmented territories -- Multi-layer model with role-specific quotas (2-3 weeks)
- Multiple business units, products, geographies -- Complex model with sub-allocations and cross-functional alignment (3-4 weeks)

**3. Territory Maturity**

- Stable territories (no changes in 12+ months) -- Use historical territory data as-is for bottom-up
- Recently redesigned territories -- Requires territory potential estimation since historical data does not map cleanly; add 1 week for weighting analysis
- Territories being redesigned concurrently -- Quota setting must wait for territory finalization or use scenario modeling

**4. Headcount Plan Stability**

- Finalized headcount with confirmed start dates -- Build ramp schedules directly into model
- Tentative headcount (hiring in progress) -- Model current team at full load; add "new hire" capacity in scenarios
- Major expansion (doubling team) -- Ramp impact dominates the model; expect 30-40% of team capacity to be in ramp at any given time

**5. Revenue Model Complexity**

- Single revenue type (new business ARR) -- Straightforward quota = bookings target
- Multiple types (new + expansion + renewal) -- Requires role-specific quota splits; see Calculations section for allocation formulas
- Usage-based or consumption revenue -- Quota may need to be expressed as net-new ARR equivalent or consumption targets; requires custom modeling

### Top-Down Approach

*Best for:*
- Early-stage companies with limited data
- When board/investor targets are the primary constraint
- New product or market launches with no historical baseline

*Not recommended for:*
- Organizations with 12+ months of CRM data (wastes available intelligence)
- Teams with significant territory variation (creates fairness issues)
- Situations where rep buy-in is critical (lacks transparency)

| Aspect | Standard (Blended) | Top-Down Only |
|--------|-------------------|---------------|
| Data required | 12+ months CRM, territory data | Revenue target, headcount plan |
| Timeline | 2-4 weeks | 1 week |
| Rep buy-in | Higher (data-backed) | Lower (perceived as arbitrary) |
| Accuracy | Higher (validated) | Lower (assumption-heavy) |

### Bottom-Up Approach

*Best for:*
- Mature organizations with deep historical data
- Stable territories and tenured reps
- When revenue predictability is the primary objective

*Not recommended for:*
- Companies targeting step-change growth (bottom-up will under-forecast)
- New markets or products with no sales history
- Teams with high turnover (historical data does not reflect current capacity)

| Aspect | Standard (Blended) | Bottom-Up Only |
|--------|-------------------|----------------|
| Growth ambition reflected | Yes (top-down provides ceiling) | Not always (reps anchor to past) |
| Territory fairness | Weighted and validated | Based on historical which may embed unfairness |
| Risk of sandbagging | Lower (reconciliation catches it) | Higher (reps may lowball potential) |

### Blended Approach

*Best for:*
- Most B2B SaaS companies between $5M-$100M ARR
- Organizations with 12+ months of CRM data AND a defined growth target
- Teams where both revenue achievement and rep retention matter

*Not recommended for:*
- Companies with no CRM data (nothing to blend bottom-up from)
- Situations requiring extreme speed (blending adds 1-2 weeks)

| Aspect | Blended | Either Standalone |
|--------|---------|-------------------|
| Accuracy | Highest | Lower |
| Buy-in from both leadership and reps | Strongest | Partial |
| Effort to build | Moderate (2-4 weeks) | Lower (1-2 weeks) |
| Defensibility | Strongest (dual validation) | Weaker |

---

## 3) Benchmarks & Standards

### How to Use Benchmarks

*Benchmarks are guidelines, not rules. Always:*
1. Start with benchmark as baseline
2. Adjust based on client-specific data
3. Validate against their actual numbers when available
4. Document deviations and rationale

### Quota Attainment Rates

| Metric | Low | Typical | High | Notes |
|--------|-----|---------|------|-------|
| Org-wide quota attainment (% of reps hitting quota) | 30-40% | 43-50% | 70-80% | Industry average is 43-47% per Forrester [1]; a well-designed model targets 70-80% |
| Individual rep attainment (% of quota achieved) | &lt;60% | 80-100% | 120%+ | Median AE achieves ~50-60% of quota; top quartile achieves 100%+ |
| Company revenue vs. plan | &lt;85% | 90-100% | 105%+ | Well-set quotas at the org level should deliver 95-105% of revenue plan |

**Source:** Forrester B2B Sales Research [1], Salesforce State of Sales [8], Hyperbound B2B Sales Performance Benchmark [9]

**Interpretation:**
- **Below 30% attainment:** Quotas are likely set too aggressively, or there are fundamental go-to-market issues. Investigate territory allocation, pipeline coverage, and whether targets were back-tested.
- **Above 80% attainment:** Quotas may be too conservative (sandbagging risk). Verify that the company is still hitting its aggregate revenue plan - high individual attainment with missed company numbers indicates poor allocation.

### Quota-to-OTE Ratios by Role

| Role | Low | Typical | High | Notes |
|------|-----|---------|------|-------|
| Field AE (New Business) | 3.5x | 4-5x | 6x | Median is 4.2x in 2024 [7] |
| Inside AE | 3x | 4-5x | 6x | Lower deal sizes, higher volume |
| Account Manager (Expansion) | 5x | 6-8x | 10x | Existing relationships lower effort per dollar |
| Enterprise AE | 4x | 4-6x | 7x | Higher deal values offset lower volume |

**Source:** Bridge Group 2024 AE Metrics & Compensation Benchmark [7], Everstage SaaS Compensation Benchmarks [10]

**Interpretation:**
- **Below 3.5x:** Cost of sale is likely unsustainable. Either the OTE is too high for the role or the quota is set too low.
- **Above 7x (for new business):** Quota may be unattainable at the assigned compensation level. Expect retention issues.

### Ramp Timeline Benchmarks

| Role | Typical Ramp to Full Productivity | Fastest (Top Performers) | Slowest |
|------|----------------------------------|--------------------------|---------|
| SDR | 2.9-3.2 months | 2 months | 4 months |
| Inside AE | 5.3 months | 3-4 months | 7 months |
| Field AE | 5.8 months | 4-5 months | 8 months |
| Enterprise AE | 6-9 months | 5 months | 12 months |

**Source:** Bridge Group SDR/AE Benchmarks [5], Hyperbound Ramp Statistics [6]

**Interpretation:**
- **Ramp faster than benchmark by 30%+:** Rep may have prior industry experience, or the territory has strong inbound pipeline. Validate that early deals are not one-time pipeline gifts.
- **Ramp slower than benchmark by 30%+:** Check onboarding quality, territory assignment, and whether the rep is receiving adequate coaching and pipeline support.

### Pipeline Coverage Requirements

| Segment | Minimum Coverage | Target Coverage | Notes |
|---------|-----------------|-----------------|-------|
| SMB | 2.5x | 3x | Higher win rates, shorter cycles |
| Mid-Market | 3x | 3.5-4x | Moderate cycles, multiple stakeholders |
| Enterprise | 4x | 4-5x | Long cycles, complex deals, lower win rates |

**Source:** Forrester B2B Sales Research [1], industry practice

**Interpretation:**
- **Below minimum:** Rep is unlikely to hit quota without significant pipeline acceleration. Flag for immediate attention.
- **Above 5x:** Either the rep is hoarding unqualified pipeline or the territory has strong lead flow. Audit pipeline quality.

### Quick Reference Thresholds

| Question | Good | Warning | Red Flag |
|----------|------|---------|----------|
| What % of reps are hitting quota? | 60-80% | 40-60% | &lt;40% |
| What is the quota-to-OTE ratio for AEs? | 4-5x | 3-4x or 6-7x | &lt;3x or >7x |
| How long to ramp a new AE? | 4-6 months | 7-8 months | 9+ months |
| What pipeline coverage do reps carry? | 3-4x | 2-3x | &lt;2x |
| Are top and bottom performers within 2x of each other? | Yes | Moderate spread | 3x+ spread (territory problem) |

---

## 4) Calculations & Scoring

### Formula Quick Reference

| Calculation | Formula | Example |
|-------------|---------|---------|
| Rep Quota (Top-Down) | `Company Target / Number of Fully-Loaded Reps` | $20M / 10 reps = $2M each |
| Territory-Weighted Quota | `Base Quota x Territory Weight` | $1.5M x 1.2 = $1.8M |
| Effective Capacity | `Full Reps + (Ramping Reps x Ramp %)` | 8 + (4 x 0.5) = 10 effective reps |
| Quota-to-OTE Ratio | `Annual Quota / Annual OTE` | $1M / $200K = 5.0x |
| Back-Test Attainment | `Reps Who Would Hit / Total Reps` | 8/12 = 67% |
| Pipeline Coverage | `Weighted Pipeline / Remaining Quota` | $3M / $1M = 3.0x |

### Top-Down Quota Allocation

**Formula:**
```
Individual Quota = (Company Revenue Target x Coverage Buffer) / Effective Seller Capacity
```

**Variables explained:**
- `Company Revenue Target` = Board-approved ARR or bookings target for the period
- `Coverage Buffer` = Multiplier to account for expected non-attainment (typically 1.05-1.15x, meaning total assigned quota is 5-15% above the company target)
- `Effective Seller Capacity` = Sum of fully-loaded rep equivalents, accounting for ramp

**Worked Example:**

*Scenario: Series B SaaS company targeting $20M in new business ARR*

```
Given:
- Company Revenue Target = $20,000,000
- Coverage Buffer = 1.10 (10% over-assignment)
- Team: 8 fully ramped AEs + 4 AEs in ramp (average 50% productivity)
- Effective Capacity = 8 + (4 x 0.50) = 10.0 fully-loaded equivalents

Calculate:
- Total Quota Pool = $20,000,000 x 1.10 = $22,000,000
- Base Quota Per Fully-Ramped Rep = $22,000,000 / 10.0 = $2,200,000
- Ramping AE Quota = $2,200,000 x 0.50 = $1,100,000 (prorated)

Validation:
- If 75% of reps hit quota: 0.75 x $22M = $16.5M + overachievement should reach $20M
- Quota-to-OTE check: $2.2M / $200K OTE = 11.0x
  (TOO HIGH - this indicates the team is undersized for the target.
   Either add headcount or revise the revenue target.)
```

**Validation:**
- Total assigned quota should be 105-115% of the revenue target
- If quota-to-OTE ratio exceeds 6x for new business AEs, investigate whether headcount is sufficient or the target is realistic
- If the back-test shows &lt;50% attainment, the model needs adjustment

### Territory Weighting Calculation

**Formula:**
```
Territory Weight = (Account Density Score + Market Maturity Score + Historical Performance Score
                    + Competitive Intensity Score) / Max Possible Score

Adjusted Quota = Base Quota x Normalized Territory Weight
```

**Variables explained:**
- Each factor scored 1-5 (1 = lowest potential, 5 = highest potential)
- `Max Possible Score` = Number of factors x 5 (e.g., 4 factors x 5 = 20)
- `Normalized Territory Weight` = Territory's raw score / Median territory score (so median territory = 1.0x)

**Worked Example:**

*Scenario: Calculating weights for 3 territories*

```
Scoring (1-5 scale):

                    Account    Market    Historical    Competitive    Raw
Territory           Density    Maturity  Performance   Intensity*     Score
Northeast           5          4         4             3              16
Southeast           3          3         3             4              13
Mountain West       2          2         2             5              11

* Competitive Intensity: Higher score = LESS competition = more opportunity

Median Raw Score = 13 (Southeast)

Normalized Weights:
- Northeast: 16/13 = 1.23x
- Southeast: 13/13 = 1.00x
- Mountain West: 11/13 = 0.85x

Applied to $1,000,000 base quota:
- Northeast: $1,000,000 x 1.23 = $1,230,000
- Southeast: $1,000,000 x 1.00 = $1,000,000
- Mountain West: $1,000,000 x 0.85 = $850,000

Total: $3,080,000 (vs. $3,000,000 flat) - adjust base quota downward
to ensure total pool matches the company target
```

**Validation:**
- No territory weight should deviate more than +/- 40% from the median (0.6x to 1.4x range)
- If a territory requires >1.4x, consider splitting it
- If a territory scores &lt;0.6x, consider merging or reassigning accounts

### Ramp Schedule Proration

**Formula:**
```
Ramping Rep Quota = Full Quota x Weighted Average Ramp % for Period

Standard AE Ramp % by Month:
- Month 1-2: 0% (training, no quota)
- Month 3: 25%
- Month 4: 50%
- Month 5: 75%
- Month 6+: 100%
```

**Worked Example:**

*Scenario: AE hired March 1, calculating Q2 quota (Apr-May-Jun)*

```
Given:
- Full quarterly quota = $500,000
- AE start date: March 1
- Month counting from hire date:
  - March = Month 1 (0%)
  - April = Month 2 (0%)
  - May = Month 3 (25%)
  - June = Month 4 (50%)

Calculate Q2 quota:
- April contribution: $500K x (1/3) x 0% = $0
- May contribution: $500K x (1/3) x 25% = $41,667
- June contribution: $500K x (1/3) x 50% = $83,333
- Q2 Ramping Quota = $125,000 (vs. $500K full quota)

Team impact:
- This rep contributes 25% of a full slot for Q2 capacity planning
```

**Validation:**
- Total ramp quota for a new hire's first year should be approximately 40-50% of a full year's quota (reflecting ~5-6 months to full ramp)
- If a new hire is exceeding ramp milestones, do not increase their quota mid-period - recognize the overachievement and adjust for next period

### Revenue Type Allocation

**Formula:**
```
For reps carrying multiple revenue types:

New Business Quota = Total Quota x New Business Weight
Expansion Quota = Total Quota x Expansion Weight
Renewal Quota = Total Quota x Renewal Weight

Where weights sum to 1.0
```

**Worked Example:**

*Scenario: Full-cycle AE carrying new business and expansion*

```
Given:
- Total Quota = $1,200,000
- Weights: 70% new business, 30% expansion

Calculate:
- New Business Quota = $1,200,000 x 0.70 = $840,000
- Expansion Quota = $1,200,000 x 0.30 = $360,000

Commission rates may differ by type:
- New Business: 10% commission rate
- Expansion: 6% commission rate (lower effort per dollar)
```

**Validation:**
- Verify that the aggregate of all reps' new business quotas covers the company's new business target
- Verify that expansion quotas align with the installed base's expansion potential
- If a rep consistently over-delivers on one type and under-delivers on the other, consider separating the roles (dedicated AE + dedicated AM)

### Scoring Rubrics

**Territory Scoring Rubric:**

| Criterion | 1 pt (Low) | 3 pts (Medium) | 5 pts (High) |
|-----------|------------|-----------------|---------------|
| Account Density | &lt;50 target accounts | 50-150 target accounts | 150+ target accounts |
| Market Maturity | Pre-product-market fit; no established demand | Growing adoption; some competitors | Mature market; established budgets |
| Historical Performance | Territory &lt;60% to plan last 2 years | Territory at 80-100% to plan | Territory >110% to plan consistently |
| Competitive Intensity\* | 3+ well-funded competitors dominating | 1-2 competitors with moderate share | Limited or weak competition |

*\*Scored inversely: less competition = higher opportunity score*

**Tier Thresholds for Territory Classification:**
- Tier 1 (Premium): 16+ points - High quota, experienced rep assignment
- Tier 2 (Standard): 11-15 points - Standard quota, any rep assignment
- Tier 3 (Development): Below 11 points - Reduced quota, growth-oriented strategy

---

## 5) Edge Cases

*The tricky scenarios that require special handling.*

### Edge Case 1: New Company or Division with No Historical Data

*Scenario:* A startup or newly formed business unit has less than 6 months of CRM data. There is no reliable historical baseline for bottom-up analysis, yet leadership needs quotas to hire against and to set compensation plans.

*Challenge:* Without historical data, the blended methodology breaks down. Bottom-up is impossible, and top-down risks being disconnected from reality since there is no actual performance to calibrate against.

*Approach:*

1. Use top-down as the primary methodology, anchored to the company's growth model and fundraising targets
2. Replace bottom-up with **market-based benchmarks**: apply industry-average productivity per rep ($800K median ACV quota for SaaS AEs [7]) adjusted for ASP and sales motion
3. Build **conservative ramp assumptions** (assume 6-month ramp for all AEs since there is no company-specific ramp data)
4. Set quotas for one quarter only, with explicit commitment to re-evaluate with actual data before setting Q2 quotas
5. Use a **wider coverage buffer** (1.15-1.20x) to account for higher uncertainty

*Fallback assumptions:*

| Missing Data | Use This Instead | Source |
|--------------|------------------|--------|
| Historical win rate | 20-25% for new business (B2B SaaS average) | Bridge Group Benchmarks [7] |
| Average sales cycle | 3-4 months SMB, 6-9 months Enterprise | Industry practice |
| Rep productivity | $800K ACV per AE (median) | Bridge Group 2024 [7] |
| Ramp timeline | 5.3 months inside, 5.8 months field | Bridge Group SDR/AE data [5] |

### Edge Case 2: Mid-Year Territory Realignment

*Scenario:* Territories are restructured mid-year due to new hires, departures, or strategic shifts. Existing reps gain or lose accounts, and historical territory data no longer maps to the new structure.

*Challenge:* Quota credit becomes contested, and the quota model built on old territories no longer reflects reality.

*Approach:*

1. **Freeze in-progress deals**: All opportunities past Stage 3 (or equivalent) stay with the current rep regardless of territory reassignment
2. **Prorate quotas**: Reduce the outgoing quota proportionally to the accounts removed, and increase the receiving rep's quota proportionally - but apply a 60-day grace period before the new accounts' quota kicks in
3. **Re-weight territories**: Run the territory scoring model on the new structure and recalculate weights
4. **Never change quotas retroactively**: Changes apply going forward only
5. **Document everything**: Create a change log showing old quota, new quota, accounts transferred, and effective date

### Edge Case 3: Multi-Product or Multi-Motion Sales Team

*Scenario:* A company sells multiple products or has distinct sales motions (e.g., inbound-driven SMB vs. outbound-driven Enterprise). Reps may carry quota across products or motions with different sales cycles, deal sizes, and win rates.

*Challenge:* A single blended quota does not account for the different economics of each product or motion.

*Approach:*

1. **Separate quotas by product or motion**: Assign distinct quota targets (e.g., 60% core platform, 25% add-ons, 15% services) rather than a single blended number
2. **Apply different commission rates per product** to steer behavior: higher commission on strategic products, lower on products that sell themselves
3. **Weight the territory scoring by product potential**: A territory rich in accounts for Product A may be weak for Product B
4. **Back-test each product's quota independently**: Attainment on Product A should be 70-80% AND attainment on Product B should be 70-80%

### Edge Case 4: High-Growth Scenario with Rapid Hiring

*Scenario:* The company plans to double the sales team within 2 quarters. At any given time, 30-50% of the team is in ramp.

*Challenge:* The total quota pool must account for ramp drag, but leadership still expects aggressive revenue growth.

*Approach:*

1. **Model two capacity scenarios**: "conservative" (actual ramp speeds from benchmarks) and "aggressive" (accelerated ramp from structured onboarding)
2. **Communicate the capacity gap honestly**: Show leadership that 20 reps with 10 ramping is equivalent to 15 fully-loaded reps, not 20
3. **Do not inflate tenured rep quotas to cover the gap**: This destroys morale and credibility. Instead, flag the gap as a timing risk in the revenue plan.
4. **Build monthly capacity tracking**: Update effective capacity each month as reps progress through ramp milestones

*Fallback assumptions:*

| Scenario | Assumption | Impact |
|----------|------------|--------|
| All hires land on schedule | Use planned start dates | Best case capacity |
| 25% hiring slippage | Delay 25% of start dates by 1 month | Reduce H2 capacity by 10-15% |
| 50% hiring slippage | Delay 50% of start dates by 2 months | Reduce H2 capacity by 20-30% |

### Edge Case 5: Seasonal or Cyclical Revenue Patterns

*Scenario:* The company's revenue has strong seasonal patterns (e.g., 40% of annual bookings in Q4, or government clients with fiscal year purchasing cycles). Flat quarterly quotas do not reflect this reality.

*Challenge:* Equal quarterly quotas mean Q1 always looks like underperformance and Q4 always looks like overperformance.

*Approach:*

1. **Analyze 2+ years of monthly bookings data** to identify the seasonal pattern
2. **Apply quarterly weighting**: If Q4 historically represents 35% of annual bookings, set Q4 quota at 35% of annual target (not 25%)
3. **Normalize attainment reporting** to account for seasonality - show "% of seasonal plan" not just "% of flat plan"
4. **Set leading indicator targets per quarter** that reflect the seasonal pipeline build pattern

---

## References

[1] [Forrester - Your Company's Quota Attainment Is Probably Around 50%](https://www.forrester.com/blogs/your-companys-quota-attainment-is-probably-around-50-and-thats-not-a-bad-thing/)

[2] [Varicent - Top-Down vs. Bottom-Up Sales Planning](https://www.varicent.com/blog/top-down-bottom-up-sales-planning)

[3] [Forma.ai - Defining Sales Quotas: How to Set Methodology and Test](https://www.forma.ai/resources/article/setting-sales-quotas)

[4] [SalesGlobe - 10 Sales Quota Best Practices](https://www.salesglobe.com/sales-quota-best-practice/)

[5] [Sales So - Sales Ramp-Up Statistics 2025: Benchmarks & Best Practices](https://salesso.com/blog/sales-ramp-up-statistics-2025-benchmarks-best-practices/)

[6] [Hyperbound - 30/60/90 Day Ramp Plan for Winning Sales Teams](https://www.hyperbound.ai/blog/30-60-90-day-ramp-plan)

[7] [Bridge Group - 2024 SaaS AE Metrics & Compensation Benchmark Report](https://blog.bridgegroupinc.com/2024-ae-metrics-compensation-benchmark)

[8] [Salesforce - State of Sales 2024](https://www.salesforce.com/resources/research-reports/state-of-sales/)

[9] [Hyperbound - 2025 B2B Sales Performance Benchmark Report](https://www.hyperbound.ai/blog/b2b-sales-performance-benchmark-2025)

[10] [Everstage - SaaS Sales Compensation Benchmarks](https://www.everstage.com/sales-compensation/saas-sales-compensation-benchmarks)
