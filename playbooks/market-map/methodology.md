# Market Map — Methodology

Market Map methodology transforms ICP criteria from static documents into machine-readable infrastructure that powers CRM automation, territory design, and enrichment workflows. This reference covers the concepts, decision frameworks, benchmarks, and scoring logic behind ICP operationalization and TAM enrichment.

## 1) Core Concepts

### ICP as Infrastructure, Not Documentation

*What is it?*

Most companies have an ICP -- it sits in a Google Doc, a slide deck, or someone's head. ICP as Infrastructure means taking those criteria and making them machine-readable: every criterion is enrichable through data providers, scored with point values, and loaded into CRM fields that power automations, dashboards, and routing.

*Why does it matter?*

The 2025 FullCast report (co-published with LeanScale, analyzing 440,000 opportunities worth $43 billion) found that only 23% of pipeline actually fits ICP -- meaning 77% of deals are wrong fit. 63% of CROs admit they have little or no confidence in their own ICP definition. The problem is not that companies lack an ICP. The problem is the ICP is not operationalized.

*Key insight:*

> Your ICP goes from a document sitting in a Google Doc to infrastructure loaded into your CRM, powering your dashboards, telling your team where to focus. This is what it looks like when ICP is infrastructure -- it powers everything downstream.

*Examples:*

| Context | How ICP as Infrastructure Applies |
|---------|----------------------------------|
| Lead routing | Incoming leads are scored against ICP vectors automatically. T1 leads route to AEs instantly; T3 stays in marketing nurture. No manual triage needed. |
| Clay credit management | Enrichment workflows check Market Map before spending credits. Only ICP-qualified accounts get enriched -- no wasted spend on wrong-fit companies. |
| Signal monitoring | When a T1 account posts a job for a role your product supports, your rep knows about it that day. Without Market Map, that signal is noise in a sea of irrelevant alerts. |

*Common misunderstandings:*

- **Misconception:** "We already have our ICP so we can skip this."
  **Reality:** Having an ICP document and having an operationalized ICP are fundamentally different. Every criterion must be enrichable through data providers. You are re-engineering what exists into a format that Clay can actually score and automate. The ICP you have is a starting point, not a finished product.

- **Misconception:** "ICP is a one-time exercise."
  **Reality:** ICP criteria drift as business priorities change, products evolve, and competitive dynamics shift. Market Map requires at minimum twice-yearly validation reviews. After the first sales cycle (30-90 days post-launch), you should be checking closed won/lost by tier to validate assumptions against real performance.

---

### The Enrichable Criteria Constraint

*What is it?*

An enrichable criterion is an ICP attribute that can be answered by data providers at scale. "Has 500+ employees" is enrichable -- Apollo, Clearbit, and ZoomInfo all have headcount data. "Has active board committees" is not enrichable through standard providers -- no database has this field, so either you use Claygent with custom AI prompts (and accept lower hit rates), or you drop the criterion.

*Why does it matter?*

This is the core constraint that separates Market Map from traditional ICP exercises. Every vector in the ICP Matrix must pass the enrichability test: can we get this data point programmatically for thousands of accounts? If the answer is no, the criterion either gets replaced with a proxy, solved through Claygent, or removed.

*Key insight:*

> You are building your ICP "the Clay Way" -- every criterion must be answerable through data providers, not just a Google Doc. You are operationalizing what was previously tribal knowledge.

*Examples:*

| Criterion | Enrichable? | Source | Notes |
|-----------|-------------|--------|-------|
| Employee headcount | Yes | Apollo, Clearbit, ZoomInfo | Standard firmographic -- reliable across providers |
| Uses Salesforce | Yes | Clearbit, BuiltWith, HG Insights | Technographic -- coverage varies by company size |
| Nonprofit with 10+ board members | Yes (vertical) | Cause IQ | Requires vertical-specific data provider |
| "Company culture values innovation" | No (as stated) | N/A | Too subjective. Replace with proxy: R&amp;D headcount %, patent filings, or job posting patterns |
| Has active EV incentive programs | Partially | Claygent | Custom AI prompt can scan press releases, but hit rate may be &lt;50% |

*Common misunderstandings:*

- **Misconception:** "If we can't enrich it, we should drop it from ICP entirely."
  **Reality:** Non-enrichable criteria can still inform strategy -- they just cannot be used for automated scoring. Separate your ICP into "enrichable vectors" (used in fit score) and "qualitative indicators" (used in manual evaluation by AEs during discovery calls). Only enrichable vectors go into the ICP Matrix.

---

### Tiering: T1 / T2 / T3 Account Classification

*What is it?*

Tiering is the classification of all accounts in your TAM into priority levels based on ICP fit score. Tier 1 accounts are the highest-fit -- they get the most attention, the best reps, personalized outreach. Tier 3 accounts are lowest-fit -- they get automated marketing nurture only. The tier assignment drives everything downstream: territory design, enrichment budget, outreach cadence, signal monitoring priority.

*Why does it matter?*

Without tiering, every account looks the same in CRM. Reps spend time on whatever is in front of them, not what fits best. Marketing sprays campaigns broadly. Territory design is arbitrary. Tiering creates a forcing function for prioritization across every GTM function.

*The Framework:*

| Tier | Definition | Treatment | Typical Volume |
|------|-----------|-----------|----------------|
| Tier 1 (T1) | Highest-fit accounts meeting X+ point threshold on fit score rubric | AE-driven, personalized outreach, top priority for enrichment and signals | 50-10k per rep |
| Tier 2 (T2) | Good-fit accounts meeting Y-X point threshold | SDR/marketing-driven, moderate personalization | 2-5x T1 volume |
| Tier 3 (T3) | Accounts below Y point threshold | Marketing nurture only, automated outreach | Remainder of TAM |

*Key insight:*

> Tiering is not just about labeling accounts. It is a resource allocation framework. Every downstream decision -- who gets enriched, who gets called first, whose signals get monitored -- flows from tier assignment. Get tiering wrong and every downstream motion is misfocused.

*Common misunderstandings:*

- **Misconception:** "T1 should be the biggest, most prestigious accounts."
  **Reality:** T1 should be the best-fit accounts based on data-driven criteria, not aspiration. One client discovered after 6 months that their T2 accounts were converting better than T1 because T1 accounts were too large and chose enterprise competitors. Aspirational T1 versus actual T1 is one of the most common failure modes.

- **Misconception:** "We should pull all tiers at once."
  **Reality:** Start with T1. Validate over one sales cycle. Expand to T2 and T3 only after T1 tiering is proven correct. Premature full-TAM pulls waste Clay credits and create noise.

---

### Account Valuation

*What is it?*

Account valuation is the estimated ARR (Annual Recurring Revenue) potential of each account, calculated from firmographic data using coefficient formulas. It answers the question: "If we won this account, what would it be worth?" Valuation is separate from fit score -- an account can be high-fit but low-value, or low-fit but high-value.

*Why does it matter?*

Territory design depends on valuation. Without it, you are assigning reps to territories without knowing how much revenue potential is in each. This is the Gold Miner problem: three miners sent to three mountains, but nobody checked how much gold was in each mountain first.

*Key insight:*

> Valuation enables equitable territory design. Instead of dividing accounts alphabetically or geographically, you divide by total estimated value -- ensuring each rep has a fair shot at quota.

*The Gold Miner Metaphor (for territory design benefit only):*

Imagine three experienced miners assigned to three different mountains. Miner 1 comes back with a couple of nuggets (you blame him). Miner 2 comes back with a wheelbarrow of gold (you praise him). Miner 3 comes back with a trainload (you promote him). But the question is: why did you not figure out how much gold was in each mountain first?

This is exactly what happens when organizations assign reps to territories without account valuation data. Market Map solves this by identifying every account, estimating its ARR potential, and then designing territories with data on where the value actually is.

*Common misunderstandings:*

- **Misconception:** "Valuation is just revenue times a multiplier."
  **Reality:** Valuation methodology varies by pricing model. Per-seat products use employee headcount coefficients. Usage-based products use revenue coefficients. Enterprise deals may require like-accounts comparison. The right formula depends on how the client charges and what data is available. See the Calculations & Scoring section for specifics.

---

### Persona Tiering

*What is it?*

Persona tiering applies the same fit-scoring logic to contacts that account tiering applies to companies. Persona vectors include title, seniority, department, geography, and tenure. A Tier 1 persona is an exact match (right title, right seniority, right department). A Tier 2 persona is adjacent (close but not exact). A Tier 3 persona is a weak match.

*Why does it matter?*

Accounts do not buy products -- people at accounts do. Having T1 accounts without knowing WHO to contact at those accounts limits the value of Market Map. Persona tiering ensures outbound sequences target the right people, not just any contact at a target account.

*Key insight:*

> Account lists are stable for 6-12 months. People move constantly. Persona enrichment should be treated as ongoing, not one-time. Priority: get the right accounts with the right values first, then layer personas. Persona enrichment is often a fast-follow or ongoing engagement.

---

### The Clay Use Case Pyramid

*What is it?*

At LeanScale, Clay has four primary use cases, and Market Map sits at the base -- the foundation everything else relies on. The pyramid (from bottom to top) represents increasing specialization, with each layer depending on the one below it.

*Why does it matter?*

Without Market Map, every other Clay workflow operates in a silo. Automated inbound flows do not know if a lead is at a T1 account before spending credits on enrichment. Automated outbound systems have no reference for who to target. Signal workflows (job changes, intent triggers, competitor moves) cannot prioritize because there is no tiered account foundation.

*The Framework:*

```
        /\
       /  \        Signals & ABM
      /    \       (Job changes, intent, competitor moves)
     /------\
    /        \     Outbound Enrichment
   /          \    (Sequence targeting, persona data)
  /------------\
 /              \  Inbound Automation
/                \ (Lead scoring, routing, enrichment)
/------------------\
| MARKET MAP        |  Foundation Layer
| ICP + TAM + Tiers |  (All other use cases reference this)
\------------------/
```

With Market Map as the foundation, every other Clay use case becomes more efficient because it has a tiered, valued account foundation to build on. Without it, you are burning credits in silos -- re-enriching the same accounts across different workflows, enriching accounts that do not matter, with no single source of truth.

---

## 2) Decision Frameworks

### Approach Selection Matrix

The first decision in any Market Map project is which approach to use. This determines scope, timeline, and cost.

| Situation | Recommended Approach | Why |
|-----------|---------------------|-----|
| Vertical company, narrow TAM (&lt;100k accounts), 5+ reps | Approach 1: Full TAM Pull | Finite, definable market. Pull everything, tier everything, enrich everything. |
| Horizontal product, 500k+ accounts, smaller team | Approach 2: Tiered Pull (T1/T2/T3) | TAM too large for full pull. Define T1 criteria tightly, pull T1 initially, expand later. |
| Small team, limited budget, want quick wins | Approach 3: T1 Only | Minimum viable Market Map. 500-2k accounts, fast delivery (2-3 weeks), validate before expanding. |
| Messy CRM with garbage data, domains not normalized | Approach 4: CRM Cleanup First | Cannot build on bad data. Audit, clean, normalize, THEN enrich. |
| 200+ closed won/lost, robust firmographic data | Approach 5: Historical Data Heavy | Let data inform ICP. Correlation analysis reveals what actually converts, not what stakeholders believe converts. |
| Early stage (&lt;50 customers), sparse data | Approach 6: No Historical Data | No data to analyze. Rely on interviews, Clay Searcher real-time validation, hypothesis-driven approach. |

### Scoping Factors

These variables determine which approach to recommend. Evaluate each during discovery.

**1. Company Type (Vertical vs Horizontal)**

- Vertical company (e.g., nonprofits, financial services, healthcare) --> TAM is finite and definable. Full TAM pull is usually feasible.
- Horizontal company (e.g., any company could be a customer) --> TAM is effectively infinite. Do NOT pull full TAM. Focus on tiers only, with very restrictive T1 criteria.

**2. TAM Size**

- &lt;100k accounts --> Full TAM pull feasible
- 100k-500k accounts --> Tiered approach recommended
- 500k+ accounts --> T1 only mandatory, at least initially
- Millions of accounts --> T1 only with extremely restrictive criteria

**3. Sales Team Size**

- 1-3 reps --> T1 only (50-2k accounts total). Reps cannot work more accounts effectively.
- 5-10 reps --> T1/T2 pull (2,500-10k accounts total)
- 10+ reps --> Full TAM pull viable IF the company is vertical

**4. Historical Data Availability**

- &lt;50 customers --> Approach 6 (No Historical Data). Not enough data for statistical patterns.
- 100-500 customers --> Approach 5 (Historical Data Heavy). Sufficient for correlation analysis.
- 500+ customers --> Full data analysis. Strong statistical confidence in patterns.

The threshold for meaningful correlation analysis is approximately 100 closed-won customers or 200 total closed won/lost opportunities.

**5. CRM Data Quality**

- Clean CRM (domains normalized, fields populated, no duplicates) --> Standard approach
- Messy CRM (mixed domains, duplicates, missing fields) --> Approach 4 (CRM Cleanup First). Do not build on bad data.
- No CRM or net-new CRM --> Net-new only approach. No cleanup needed.

**6. Data Provider Coverage by Vertical**

| Vertical | Primary Data Provider | What It Provides | Notes |
|----------|-----------------------|------------------|-------|
| Standard B2B SaaS | Apollo, Clearbit, ZoomInfo | Firmographic, technographic, contact data | Default stack for most projects |
| Nonprofits / Associations | Cause IQ | NTEE codes, board size, related entities, grant data | Essential for nonprofit ICP vectors |
| Financial Services | iBanknet | AUM, advisor count, branch locations | Essential for financial services ICP vectors |
| Healthcare | Definitive Healthcare | Provider data, facility size, specialties | Specialized healthcare data |
| Education | IPEDS data | Enrollment, program offerings, institutional data | Federal education data |

If the client's vertical requires a specialized data provider, confirm the subscription exists and is connected to Clay before scoping.

**7. Product Pricing Model**

This directly determines the valuation methodology (see Calculations & Scoring):

- Per-seat pricing --> Employee headcount coefficient
- Usage-based pricing --> Revenue coefficient
- Enterprise deals --> Like-accounts comparison
- Tiered packages --> Combination approach

**8. Clay Credit Budget**

- Unlimited credits --> Enrich aggressively, use waterfall enrichment across multiple providers
- Limited credits (5k-10k) --> T1 only. Use "only run if" conditions on expensive enrichments. Use free Score Row for calculations.
- Very limited (&lt;5k) --> Minimal enrichment, focus on firmographics only, skip persona enrichment initially

### Approach 1: Full TAM Pull

*Best for:*
- Vertical companies targeting a specific industry
- TAM is &lt;100k accounts
- Sales team of 5+ reps who need full market coverage
- Company wants complete visibility for territory design and capacity planning

*Not recommended for:*
- Horizontal companies (TAM too large, will produce millions of accounts)
- Teams with &lt;3 reps (cannot work that many accounts)
- Limited Clay credit budgets (enriching 100k accounts is expensive)

*Key differences from standard:*

| Aspect | Standard (Tiered) | Full TAM |
|--------|--------------------|----------|
| Account volume | 500-10k (T1 focused) | Entire addressable market |
| Clay credit investment | Moderate | High (enrich all accounts) |
| CRM impact | Incremental additions | Major data load |
| Time to value | 2-4 weeks | 6-8 weeks |
| Territory design readiness | Partial (T1 only) | Complete (all tiers valued) |

### Approach 2: Tiered Pull (T1/T2/T3)

*Best for:*
- Large TAMs (500k+ accounts) where full pull is not feasible
- Companies that want a phased approach -- start with T1, validate, expand
- Medium-sized sales teams (5-10 reps)

*Not recommended for:*
- Very small TAMs (&lt;5k total accounts) -- just pull everything
- Teams that need full territory coverage immediately (use Approach 1 if vertical allows)

*The phasing logic:*

1. Define T1/T2/T3 criteria and thresholds
2. Pull T1 accounts first (500-2k per rep)
3. Enrich and load T1 into CRM
4. Validate T1 over one sales cycle (30-90 days)
5. If T1 tiering validates, expand to T2
6. T3 is typically marketing-only and gets lighter enrichment

### Approach 3: T1 Only (Minimum Viable Market Map)

*Best for:*
- Small teams (1-3 reps) with limited capacity
- Limited Clay credit budgets
- Companies that want quick wins before committing to a larger build
- Proving the concept before scaling

*Not recommended for:*
- Companies with territory design urgency (need all accounts valued)
- Organizations with 10+ reps (not enough accounts per rep)

*Timeline:* 2-3 weeks typical. 500-2k accounts total.

### Approach 4: CRM Cleanup First

*Best for:*
- CRMs with garbage data: domains not normalized, duplicates, stale records
- Organizations where existing CRM data prevents accurate matching

*Not recommended for:*
- Clean CRMs (unnecessary overhead)
- Net-new CRM instances (nothing to clean)

*Why cleanup must come first:*

Clay matches on domains. If CRM has "www.acme.com", "acme.com", "http://acme.com", and "ACME, Inc." as separate account records, enrichment will create duplicates or miss matches entirely. Normalize first, then enrich.

### Approach 5: Historical Data Heavy

*Best for:*
- Mature sales organizations with 200+ closed won/lost
- Companies with robust CRM data (firmographic fields populated)
- Situations where stakeholders disagree on ICP -- data forces alignment

*Not recommended for:*
- Early-stage companies (&lt;50 customers)
- Organizations with poor CRM data quality (clean first)

*Why this approach is powerful:*

Instead of building ICP from opinions and stakeholder interviews (which introduces bias), correlation analysis on actual closed won/lost data reveals what segments win at higher rates, close faster, and churn less. This is how you separate aspirational ICP from actual ICP.

### Approach 6: No Historical Data

*Best for:*
- Early-stage companies (&lt;50 customers)
- Companies with limited closed-lost tracking
- New market entries where historical patterns do not exist

*Not recommended for:*
- Organizations with sufficient data (use Approach 5 instead -- data beats opinions)

*How to compensate for missing data:*

1. Rely heavily on stakeholder interviews for initial hypotheses
2. Use Clay Searcher for real-time validation during workshops (test whether proposed criteria return a reasonable number of accounts)
3. Use AI deep research tools for market sizing and benchmarking
4. Mark all criteria as ASSUMED and plan for aggressive refinement after first sales cycle
5. Build in shorter validation cycles (30 days instead of 90)

---

## 3) Benchmarks & Standards

### How to Use Benchmarks

Benchmarks are guidelines, not rules. Always:
1. Start with benchmark as baseline
2. Adjust based on client-specific data
3. Validate against their actual numbers when available
4. Document deviations and rationale

### ICP & Pipeline Benchmarks

| Metric | Low | Typical | High | Notes |
|--------|-----|---------|------|-------|
| Pipeline that fits ICP | &lt;20% | 23% | >40% | 2025 FullCast/LeanScale report. Most companies are shocked at how low their number is. |
| CRO confidence in own ICP definition | &lt;30% | ~37% | >60% | 63% of CROs have little or no confidence. Use this stat to sell the project. |
| Quota attainment rate | &lt;40% | ~23% hit quota | >50% | 77% of sellers missed quota in 2025 even after 13% quota cuts. |
| Wrong-fit deal close difficulty | N/A | 8x harder | N/A | Wrong-fit deals are 8x harder to close than right-fit deals. |

**Source:** 2025 FullCast report, co-published with LeanScale. 440,000 opportunities, $43 billion in pipeline analyzed.

**Interpretation:**
- **Below 23% pipeline fit:** Common. This is why Market Map exists -- most companies are here.
- **Above 40% pipeline fit:** Uncommon. Indicates strong existing ICP discipline. Market Map can still add value through enrichment and automation, but the ICP definition work will be lighter.

### Account Volume Per Rep Benchmarks

| Metric | Low | Typical | High | Notes |
|--------|-----|---------|------|-------|
| T1 accounts per AE | 50 | 200-500 | 2,000 | Depends on deal complexity and sales cycle length |
| T1 accounts per SDR | 200 | 500-1,000 | 2,000 | SDRs work higher volume, lower touch |
| Total accounts per rep (all tiers) | 500 | 2,000-5,000 | 10,000 | Upper bound is for reps with automated outreach support |

**Source:** Internal LeanScale data across multiple client implementations.

**Interpretation:**
- **Below 50 per rep:** Concentrated TAM. Standard tiering may not apply.
- **Above 10,000 per rep:** Too many accounts to work meaningfully. Tighten T1 criteria.

### Tier Distribution Benchmarks

| Metric | Low | Typical | High | Notes |
|--------|-----|---------|------|-------|
| T1 as % of total TAM | 1-5% | 5-15% | 15-25% | T1 should be selective. If T1 is 50%+ of TAM, criteria are too loose. |
| T2 as % of total TAM | 10-20% | 20-40% | 40-50% | T2 is the "good but not great" middle. |
| T3 as % of total TAM | 40-60% | 50-70% | 70-80% | Largest tier by volume, lowest priority. |
| T1 total valuation vs T3 | N/A | T1 > T3 per account | N/A | If T3 total valuation dwarfs T1, tier thresholds may be too restrictive. |

**Interpretation:**
- **T1 too large (>25% of TAM):** Criteria too loose. Reps cannot prioritize effectively when "everything is T1."
- **T1 too small (&lt;1% of TAM):** Criteria too restrictive. You may need to adjust tier boundaries to be actionable.

### Project Timeline Benchmarks

| Approach | Planning | Execution | Total |
|----------|----------|-----------|-------|
| T1 Only (Minimum) | 1 week | 1-2 weeks | 2-3 weeks |
| Tiered Pull (T1/T2) | 2 weeks | 2-4 weeks | 4-6 weeks |
| Full TAM Pull | 2-3 weeks | 4-5 weeks | 6-8 weeks |
| CRM Cleanup + Market Map | 1-2 weeks cleanup + standard | +2 weeks | 6-10 weeks |

**Source:** Internal LeanScale delivery data.

### Hours Estimate Benchmarks

| Scope | Estimated Hours | Primary Cost Drivers |
|-------|-----------------|----------------------|
| T1 Only | 40 hours | ICP definition, Clay build, CRM push |
| Tiered or Full TAM | 60-80 hours | TAM size, number of ICP vectors, CRM complexity |
| With CRM Cleanup | +15-20 hours | Domain normalization, deduplication, data quality |
| With Complex ICP (vertical-specific providers) | +10-15 hours | Custom enrichment prompts, provider integration, data validation |

### Quick Reference Thresholds

| Question | Good | Warning | Red Flag |
|----------|------|---------|----------|
| T1 accounts per rep | 50-2,000 | 2,000-5,000 | >10,000 or &lt;20 |
| ICP vectors in Matrix | 5-10 | 3-4 or 11-15 | &lt;3 or >15 |
| Fit score spread (T1 vs T3) | 30+ point gap | 15-29 point gap | &lt;15 point gap (tiers too similar) |
| Tier distribution review cycles | 1-2 | 3-4 | 5+ (signals fundamental scoping issue) |
| Clay credit burn vs budget | &lt;80% of budget | 80-100% | >100% (runaway enrichments) |
| Accounts with blank tier fields post-push | 0% | 1-5% | >5% (data push failure) |

---

## 4) Calculations & Scoring

### Formula Quick Reference

| Calculation | Formula | Example |
|-------------|---------|---------|
| Revenue Coefficient Valuation | `Company Revenue x Coefficient` | $50M revenue x 0.002 = $100K estimated ARR |
| Headcount Coefficient Valuation | `Employee Count x Seat Price` | 500 employees x $200/seat = $100K estimated ARR |
| ICP Fit Score | `Sum of (Vector Score x Weight)` | Geography(20) + Size(25) + Tech(15) + Industry(20) = 80/100 |
| Tier Assignment | `IF Fit Score >= T1 threshold THEN T1` | IF 80 >= 75 THEN T1 |

### Account Valuation Methodology

Account valuation estimates the ARR potential of each account. The methodology depends on the client's pricing model.

#### Method 1: Revenue Coefficient

**Best for:** License-based or usage-based products where a company's revenue correlates with how much they would spend on your product.

**Formula:**
```
Estimated ARR = Company Revenue x Revenue Coefficient
```

**Variables explained:**
- `Company Revenue` = Annual revenue of the target account. Source: Apollo, Clearbit, or financial data providers.
- `Revenue Coefficient` = Ratio derived from existing customer data. Calculate by dividing average customer ARR by average customer revenue.

**Worked Example:**

*Scenario: SaaS company selling compliance software. Average customer pays $80K/year. Average customer revenue is $40M.*

```
Given:
- Revenue Coefficient = $80K / $40M = 0.002
- Target account revenue = $100M

Calculate:
- Estimated ARR = $100M x 0.002 = $200K
```

**Validation:**
- This number should fall within the client's typical deal size range
- If estimated ARR exceeds their largest deal by 5x+, the coefficient needs adjustment
- Test formula against 10-20 known customers before applying at scale

#### Method 2: Employee Headcount Coefficient

**Best for:** Per-seat pricing models (HR tech, collaboration tools, security products).

**Formula:**
```
Estimated ARR = Employee Count x Seat Price x Adoption Rate
```

**Variables explained:**
- `Employee Count` = Number of employees at the target account. Source: Apollo, Clearbit, LinkedIn.
- `Seat Price` = Price per seat/user in the client's pricing model.
- `Adoption Rate` = Estimated percentage of employees who would use the product (not always 100%).

#### Method 3: Product-Specific Coefficient

**Best for:** Niche products where standard firmographics do not correlate with value. Value comes from product-specific signals.

**Examples:**
- Web traffic for an advertising platform
- Funding stage for a startup-targeting product
- Number of physical locations for a logistics product
- AUM (assets under management) for financial services

**Formula:**
```
Estimated ARR = Product-Specific Signal x Product Coefficient
```

#### Method 4: Like-Accounts Comparison

**Best for:** When no clean coefficient can be derived, typically early-stage companies or complex pricing models.

**Formula:**
```
Estimated ARR = Average ARR of similar existing customers
```

**How to implement:**
1. Cluster existing customers by firmographic similarity (industry, size, geography)
2. For each cluster, calculate average ARR
3. Assign target accounts to clusters based on firmographic match
4. Apply cluster average as estimated ARR

#### Method 5: Combination Approach

**Best for:** When multiple data points are available and no single method is sufficient.

**Formula:**
```
Estimated ARR = Average(Method 1 result, Method 2 result)
```

Use when: revenue coefficient and headcount coefficient produce different results. Averaging triangulates a more reliable estimate.

### ICP Fit Scoring Rubric

Fit scoring converts ICP vector data into a single numeric score (0-100) that determines tier assignment.

**Structure:**

| Vector Category | Example Vectors | Typical Weight |
|-----------------|-----------------|----------------|
| Geography | Country, region, state | 10-20 points |
| Firmographics | Revenue, headcount, growth rate | 20-30 points |
| Technographics | Tech stack, specific tools used | 10-20 points |
| Industry / Vertical | NAICS code, sub-vertical | 15-25 points |
| Custom Criteria | Vertical-specific attributes | 10-20 points |
| **Total** | | **100 points** |

**Scoring approach:**

Each vector is scored on a scale within its weight allocation. For example, a Geography vector weighted at 15 points:
- Exact target geography = 15 points
- Adjacent geography = 10 points
- Non-target but acceptable = 5 points
- Excluded geography = 0 points

**Tier Thresholds (typical starting point):**
- Tier 1: 75-100 points
- Tier 2: 50-74 points
- Tier 3: 25-49 points
- Below 25: Not in TAM (do not load into CRM)

These thresholds are adjusted during ICP Data Review calls based on actual tier distribution from Clay pulls. The numbers above are starting points, not fixed rules.

**Validation:**
- Score 20-30 existing customers against the rubric during ICP Workshop
- Known T1 customers should score in the T1 range
- If known good customers score T2 or T3, the rubric needs adjustment
- The spread between T1 and T3 average scores should be 30+ points (see Benchmarks)

### Persona Fit Scoring Rubric

Persona scoring follows the same pattern as account scoring, applied to contacts.

**Typical Persona Vectors:**

| Vector | Typical Weight | Notes |
|--------|---------------|-------|
| Title | 30-40 points | Highest weight. Exact title match (e.g., "VP of Sales") scores full points. Adjacent titles (e.g., "Director of Sales") score partial. |
| Seniority | 20-25 points | VP/C-level vs Director vs Manager vs IC |
| Department | 15-20 points | Right department (Sales, Marketing, RevOps) vs adjacent |
| Geography | 5-10 points | Relevant if the product has geographic constraints |
| Tenure | 5-10 points | Newer hires may be more open to new tools |
| **Total** | **100 points** | |

**Persona Tier Thresholds:**
- Persona Tier 1: Exact match across primary vectors (right title, right seniority, right department)
- Persona Tier 2: Adjacent match (close but not exact -- e.g., Director of Ops when targeting VP of RevOps)
- Persona Tier 3: Weak match (right department, wrong level)

**Negative Personas:** Define titles to explicitly exclude (e.g., "Intern", "Coordinator" for enterprise-targeted products). These contacts are not loaded into CRM regardless of other vector scores.

---

## 5) Edge Cases & Deep Dives

### Horizontal Company with Massive TAM

*Scenario:* The client sells a product that any company could use (like a collaboration tool, cybersecurity product, or HR platform). Their theoretical TAM is millions of accounts.

*Approach:*

1. Force T1 Only approach (Approach 3) with extremely restrictive criteria
2. Add multiple constraint vectors to narrow the TAM to 500-2,000 accounts per rep
3. Use negative criteria aggressively to exclude segments that do not convert
4. Plan for expansion only after T1 validates over one sales cycle

### Concentrated TAM (Very Small Market)

*Scenario:* The client has a very small number of potential customers -- fewer than 500 total accounts in their entire addressable market.

*Approach:*

1. Skip standard tiering. All accounts are effectively T1.
2. Shift focus to deep account intelligence: know everything about each account, monitor all signals.
3. Invest heavily in persona enrichment -- if you have 100 target accounts, you need multiple contacts at each one.
4. Focus on expansion signals rather than acquisition signals (current customer upsell, competitive displacement opportunities).

### Aspirational T1 vs Actual T1

*Scenario:* Stakeholders define T1 as their "dream customers" -- typically the largest, most prestigious companies in their space. After 6 months of selling, the data shows T2 is actually converting better.

*Approach:*

1. During pre-kickoff, run correlation analysis on historical closed won/lost. If T1 (by stakeholder definition) has lower win rates than T2, surface this data early.
2. Present findings at kickoff: "Your best-converting segment is actually X, not Y."
3. If stakeholders insist on aspirational T1, implement it but build in a 90-day validation checkpoint.

### ICP Criteria Not Enrichable

*Scenario:* Stakeholders define ICP criteria that no data provider can answer. Examples: "has active board committees," "company culture values innovation," "CEO is a thought leader."

*Approach:*

1. First, check if a proxy exists. "Company culture values innovation" might be proxied by R&amp;D headcount percentage, patent filings, or recent product launches.
2. Second, test Claygent. Custom AI enrichment prompts can sometimes answer non-standard questions by scanning press releases, LinkedIn profiles, or company websites. Test on a sample of 50 accounts.
3. If Claygent hit rate is below 50%, the criterion is not enrichable at sufficient quality. Remove it from the automated scoring rubric.
4. Move non-enrichable criteria to a "qualitative indicators" list that AEs evaluate manually during discovery calls.

*Fallback assumptions:*

| Missing Data | Use This Instead | Source |
|--------------|------------------|--------|
| Board committee activity | Board size (>10 = higher governance maturity) | Cause IQ |
| Company culture | Glassdoor rating + recent awards + job posting language | Claygent (moderate reliability) |
| CEO thought leadership | LinkedIn follower count + recent speaking engagements | Claygent (moderate reliability) |
