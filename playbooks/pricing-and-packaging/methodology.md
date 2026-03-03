# Pricing & Packaging — Methodology

This document covers the core concepts, frameworks, and calculations behind Pricing & Packaging. It provides the methodological foundation — the "how it works" behind the execution steps.

## 1) Core Concepts

### Product Catalog Structure (SKUs, Line Items, List Prices)

*What is it?*

The foundational data structure that defines what a company sells. A product catalog consists of three layers: **SKUs** (unique identifiers for each product or service), **line items** (individual entries on a quote or invoice that reference SKUs), and **list prices** (the standard price for each SKU before any discounts are applied). This structure is the atomic unit of all pricing operations -- without it, nothing downstream (quoting, billing, reporting, approvals) can function.

*Why does it matter?*

Without a structured product catalog, every downstream system operates on guesswork. Reps enter prices manually into opportunities, creating inconsistency across deals and zero governance over what is sold at what price. Billing systems cannot automate invoicing. Revenue reporting by product becomes impossible. And any CPQ, billing, or rev rec tool requires structured catalog data to function at all.

*Key insight:*

> "We got customers who don't have SKUs... introducing people to line items is kind of world changing for them. But it's like, we can't operate in any other way." -- Brett Davis, DealHub CSM Manager

*Examples:*

| Maturity Level | What it looks like | Implications |
|----------------|-------------------|--------------|
| No catalog | Company sells "Platform" as one product. Amount is typed into the opportunity each time. No line items in CRM. | Cannot implement CPQ, cannot report revenue by product, no pricing governance. Must build catalog from scratch. |
| Basic catalog | Company has product names and list prices in a spreadsheet but no formal SKUs. Products used as proxies for SKUs. | Can begin structuring, but SKU naming convention needed. Product-to-SKU mapping is the first deliverable. |
| Mature catalog | Organized SKUs with list prices, product categories, defined line item structure, and documented product relationships (bundles, dependencies). | Ready for CPQ implementation. P&P project focuses on optimization, not creation. |

*Common misunderstandings:*

- **Misconception:** "We don't need SKUs -- we only sell one product."
  **Reality:** Even a single product often has multiple pricing dimensions: tiers, add-ons, usage components, implementation fees, support levels. Each of these is a line item that needs a SKU to be tracked, discounted, and billed correctly.

- **Misconception:** "We can just use the product name as the SKU."
  **Reality:** Product names change, are ambiguous across teams, and do not work as database keys. SKUs must be stable identifiers that survive product renames and packaging changes.

*Catalog design principle:* Best practice is to split the catalog into three distinct layers -- Product, Rate Plan, and Charge -- rather than creating a flat list where every variation gets its own SKU. A company with five core products can end up managing 5,000 SKUs under a flat model. Using configuration attributes (size, tier, billing frequency) instead of separate SKUs prevents this explosion [1].

---

### Pricing Complexity as a "Polynomial"

*What is it?*

The need for structured pricing is not determined by a single variable. It is a function of multiple compounding factors: number of products, interrelationship between products, pricing individualization, deal volume, and contract structure. These factors multiply rather than add -- a company with moderate complexity across three dimensions faces more pricing difficulty than a company with high complexity in just one.

*Why does it matter?*

Companies often ask "do we need to formalize our pricing?" based on a single factor (usually deal size or revenue). The real answer depends on the combination of factors. A $27 deal that requires 35 line items to express is harder to manage than a $100,000 single-line-item deal.

*Key insight:*

> "It's like a little polynomial. There's the value... but the real thing is number of products and the interrelationship of products. If you have a high complexity of interrelationship of products... you're going to need CPQ." -- Brett Davis, DealHub CSM Manager

> "Dollar amount really doesn't matter that much because if I'm selling a $27 deal but I need 35 products to express that, then that sucks." -- Brett Davis

*The Framework:*

| Factor | Low Complexity | Medium Complexity | High Complexity |
|--------|---------------|-------------------|-----------------|
| Number of products | 1-5 SKUs | 6-20 SKUs | 20+ SKUs |
| Product interrelationships | All independent | Some bundles or dependencies | Complex bundles, exclusions, conditional logic |
| Pricing individualization | Standard list prices, mathematical trajectory | Some customer-specific pricing | Fully custom per-deal pricing |
| Deal volume | &lt; 10 quotes/month | 10-30 quotes/month | 30+ quotes/day |
| Contract structure | Single-year, no ramps | Multi-year, simple ramps | Multi-year with annual seat increases, percentage escalation, mid-term modifications |

When two or more factors land in "High Complexity," the compound effect typically makes manual pricing unworkable and formal pricing architecture becomes necessary.

*Common misunderstandings:*

- **Misconception:** "Our deal sizes are small, so we don't need structured pricing."
  **Reality:** Deal size is the least predictive factor. Product count and interrelationship matter far more. A $27 deal with 35 line items needs more pricing structure than a $100K deal with one line item.

- **Misconception:** "Our pricing is complex, but our reps handle it."
  **Reality:** Reps handling complexity manually means inconsistency, margin erosion, and no governance. Companies without CPQ spend 73% more time on quote creation and approval processes [2].

---

### Pricing Model Types

*What is it?*

The pricing model is the fundamental unit of charge -- how the customer pays for what they receive. The five primary models in B2B SaaS are per-seat, usage-based, tiered, flat-rate, and hybrid. Each model has different implications for revenue predictability, expansion mechanics, implementation complexity, and buyer psychology.

*Why does it matter?*

The pricing model dictates the data architecture of the entire product catalog: what constitutes a line item, how quantities are measured, how billing is triggered, and how renewals work. Changing your pricing model after building downstream systems (CPQ, billing, rev rec) is an order-of-magnitude harder than choosing correctly upfront.

*The Framework:*

**Per-Seat (Per-User) Pricing**

Charges a fixed amount per named or concurrent user. Still the most common model at 57% of SaaS companies [3], down from 64% in 2024. Works when each user independently derives value from the product and value scales linearly with headcount. Breaks when usage varies dramatically across users (one admin uses it daily, nine others log in monthly).

| Aspect | Details |
|--------|---------|
| Best for | Collaboration tools, CRM, project management -- where each user is a distinct consumer |
| Revenue predictability | High -- predictable per-seat MRR |
| Expansion mechanism | Headcount growth drives seat expansion |
| Risk | "Seat stuffing" avoidance -- customers share logins to reduce costs |
| Median entry price | $29/user/month across SaaS verticals [3] |

**Usage-Based (Consumption) Pricing**

Charges based on actual consumption: API calls, transactions, storage, compute hours, messages sent. Adoption reached 43% of SaaS companies in 2025, up 8 percentage points year-over-year [3]. Companies using usage-based models see 18-23% higher net revenue retention and 34% faster land-and-expand motion [3].

| Aspect | Details |
|--------|---------|
| Best for | Infrastructure, API platforms, data services -- where value correlates directly with consumption volume |
| Revenue predictability | Lower -- fluctuates with customer activity |
| Expansion mechanism | Automatic -- usage grows, revenue grows |
| Risk | Revenue volatility; customers may reduce usage in downturns |
| Implementation note | Requires usage metering infrastructure (e.g., Metronome) and committed-amount or rate-card quoting structures |

**Tiered (Good-Better-Best) Pricing**

Offers 2-4 packages at increasing price points, each with more features, higher usage limits, or additional capabilities. The industry average is 3.2 public tiers plus a custom enterprise option [3]. This is the standard for PLG companies because it is self-serve: buyers can see all options and self-select.

| Aspect | Details |
|--------|---------|
| Best for | PLG companies, products with clear feature differentiation across customer segments |
| Revenue predictability | Moderate -- stable within tiers, upgrades drive growth |
| Expansion mechanism | Tier upgrades as needs grow |
| Risk | "Dead zone" between tiers where customers outgrow one but don't need the next |
| Design principle | Each tier should target a distinct buyer persona; middle tier should be the natural default [4] |

**Flat-Rate Pricing**

Single price, single product, all features included. Rare in B2B SaaS at scale but appropriate for early-stage companies with one product and a uniform customer base.

| Aspect | Details |
|--------|---------|
| Best for | Early-stage companies with &lt; 50 customers, single use case, uniform buyer profile |
| Revenue predictability | Highest -- completely predictable |
| Expansion mechanism | None inherent -- must add products or usage dimensions to grow revenue per customer |
| Risk | Leaves money on the table with enterprise customers willing to pay more |

**Hybrid Pricing**

Combines two or more models: typically a per-seat or tiered base subscription plus usage-based overage charges. 61% of SaaS companies now use hybrid models, up from 49% in 2024 [3]. Companies valued above $100M typically employ at least three pricing dimensions [5].

| Aspect | Details |
|--------|---------|
| Best for | Companies with both predictable baseline usage and variable consumption components |
| Revenue predictability | Moderate -- base subscription provides floor, usage provides upside |
| Expansion mechanism | Both seat/tier upgrades AND usage growth |
| Risk | Complexity -- harder to explain to buyers, harder to configure in CPQ |

*Common misunderstandings:*

- **Misconception:** "We need to pick one model."
  **Reality:** 61% of SaaS companies use hybrid pricing. Pure single-model pricing is becoming the exception, not the norm [3].

- **Misconception:** "Usage-based pricing is too unpredictable for our board."
  **Reality:** Committed consumption amounts and rate cards with minimum floors provide the revenue floor that boards want while preserving the expansion upside of usage-based economics.

---

### The Value Metric

*What is it?*

The value metric is the unit that measures how a customer derives value from your product. It is distinct from the pricing metric (the unit you charge on), though ideally they are closely aligned. Examples: Slack charges per active user (pricing metric) because collaboration value scales with active participants (value metric). Twilio charges per API call (pricing metric) because communication value scales with message volume (value metric).

*Why does it matter?*

Companies that price on a true value metric grow at nearly double the rate of those that are only feature-differentiated, according to ProfitWell's research across 5,000+ SaaS companies [6]. Getting the value metric right is the single highest-impact pricing decision. Getting it wrong means customers feel they pay more as they use less, or pay less as they consume more -- both destroy the pricing-value relationship.

*Key insight:*

A good value metric passes three checks:
1. **Growth alignment:** Larger customers naturally use more of it
2. **Fairness:** Smaller customers naturally use less of it
3. **Measurability:** Both you and the customer can agree on how to count it

If you cannot create a pure value metric, use a proxy. HubSpot uses number of contacts and number of users as proxies for marketing value and team size. The proxy does not need to be perfect -- it needs to be directionally correct and easy to measure [6].

*Examples:*

| Company Type | Value Metric | Pricing Metric (Proxy) |
|--------------|-------------|----------------------|
| Collaboration tool | Team productivity | Per active user |
| Data platform | Data insights generated | Per GB stored or queries run |
| Communication API | Messages delivered | Per API call |
| Security tool | Assets protected | Per endpoint or per employee |
| Marketing automation | Revenue influenced | Per contact or per email sent |

---

### Year-Over-Year Ramps

*What is it?*

A pricing structure where the cost changes across the term of a multi-year contract. Ramps typically take one of two forms: **seat ramps** (the number of licensed seats increases each year, e.g., 50 seats in Year 1, 75 in Year 2, 100 in Year 3) or **percentage escalation** (the price per seat increases by a fixed percentage annually, e.g., 5% per year).

*Why does it matter?*

Year-over-year ramps fundamentally change the data architecture of line items. Without ramps, a 3-year deal has one line per product. With ramps, the same deal may need year-by-year breakdowns for each product -- tripling (or more) the number of line items on a quote. This decision must be made before building the product catalog because it determines the line item structure that feeds into CPQ, billing, and rev rec.

*Key insight:*

> "One of the first conversations I have, especially with SaaS companies, is about whether they want their line items to be expressed year by year or not. Basically the question boils down to: do you have year over year ramps? Can you increase the number of seats or is it like a percentage increase? Because we have to structure the data differently based on that." -- Brett Davis, DealHub CSM Manager

*The Framework:*

| Ramp Type | Line Item Impact | Billing Impact | Common Use Case |
|-----------|-----------------|----------------|-----------------|
| No ramps | 1 line item per product for full term | Same amount each billing period | Short contracts (1 year), simple products |
| Seat ramps | Separate line items per year per product | Billing amount increases each year based on seat count | Companies expecting hiring growth, land-and-expand contracts |
| Percentage escalation | Separate line items per year per product, or a single line with escalation metadata | Billing amount increases by percentage each anniversary | Enterprise contracts, inflation protection, 3-5 year terms |
| Combined | Year-by-year line items with both seat and price changes | Complex billing schedule | Large enterprise, government contracts |

*Common misunderstandings:*

- **Misconception:** "We can add ramps later."
  **Reality:** Ramp structure is a data architecture decision. Retrofitting ramps into a flat line-item structure means rebuilding the product catalog, quote templates, billing rules, and rev rec schedules.

---

### Pricing Strategy Stability

*What is it?*

The degree to which a company's pricing decisions are finalized and internally agreed upon. Stable pricing means the products, prices, discount rules, and approval thresholds are decided. Unstable pricing means these are still being debated internally -- the company knows what it charges today but is actively considering changes.

*Why does it matter?*

Pricing strategy instability is the single biggest delay factor in any downstream implementation. When pricing is in flux, implementation teams become consultants for internal debates instead of building systems. This is not a minor delay -- it is the number one cause of P&P projects and CPQ implementations stalling or exceeding timeline.

*Key insight:*

> "If people come to the onboarding and they're without a stable set of policies or stable set of orientation toward their products, that's where it gets hard. The fewer answers they have, the more we have to be consultants, which is fine, but is not ideal." -- Brett Davis, DealHub CSM Manager

*The Stability Spectrum:*

| Level | Description | Project Implication |
|-------|-------------|-------------------|
| **Stable** | Products, prices, discount rules, and approvals are all decided. Leadership has signed off. | Proceed directly to catalog structuring and system configuration. |
| **Mostly stable** | Core pricing is set, but 1-2 elements are pending (e.g., a new product tier or a discount for a new segment). | Proceed on stable elements. Isolate pending decisions and set a deadline for resolution. |
| **In flux** | Multiple pricing elements are being debated. "This is our pricing now, but this is where we want to be in a year." | Must conduct a pricing strategy workshop before any structuring work. Do NOT proceed to implementation. |
| **Undefined** | Company has never formalized pricing. Reps negotiate each deal independently. | Full pricing definition project required. This is the maximum scope P&P engagement. |

---

### Approval Gradation

*What is it?*

A tiered approval workflow where different levels of discount, deal modification, or non-standard terms require sign-off from different people in the organization hierarchy. The concept is "enabling guardrails, not a cage" -- giving reps autonomy within defined bounds while protecting margins on larger exceptions [7].

*Why does it matter?*

Without defined approval tiers, companies either have no governance (reps discount freely, margin erodes) or blanket governance (every deal goes to the CEO, creating bottlenecks). Neither scales. The right gradation depends on org size, deal velocity, and margin sensitivity.

*Key insight:*

> "Does the sales manager need to approve this or does a director or does CRO need to approve? And you can start creating some gradation, some texture there." -- Brett Davis, DealHub CSM Manager

> "People want guardrails, but then they also want full flexibility. And so that's where we get into the most trouble." -- Brett Davis

*The Framework by Org Size:*

| Org Size | Approval Structure | Typical Rules |
|----------|-------------------|---------------|
| **&lt; 10 reps** | Minimal. One person approves everything, or no formal approvals. | "Just to get eyes on it." Manager reviews all deals as a sanity check, not a gate. |
| **10-25 reps** | Basic threshold. Single approval tier. | "If discount exceeds X%, manager approves." One deal desk person handles exceptions. |
| **25-50 reps** | Multi-tier. Sales manager vs. director vs. VP based on discount depth or deal size. | Green zone (0-15%): rep autonomy. Yellow zone (16-30%): manager approval. Red zone (30%+): VP/finance approval [7]. |
| **75-100+ reps** | Rule-based. Regional, legal, and product-specific approval chains. Could have 100+ approval rules. | Multinational complexity (EMEA, APAC, NA). Product-specific rules. Legal approval for non-standard terms. Automated routing in CPQ. |

*The Discount Approval Matrix:*

A standard three-zone model [7]:

| Zone | Discount Range | Approval Required | Additional Triggers |
|------|---------------|-------------------|-------------------|
| **Green** | 0-15% | None (rep autonomy) | Standard contract terms, Net 30 payment |
| **Yellow** | 16-30% | Direct manager (Head of Sales) | Net 60 payment terms, contracts > 24 months, written business justification required |
| **Red** | > 30% | CEO or Head of Finance | Net 90+ payment terms, strategic exception with documented rationale |

*Important:* Discount percentage is only one trigger. Effective approval matrices also include non-financial terms that affect cash flow and risk: payment terms, contract length, custom legal language, and service level commitments [7].

*Common misunderstandings:*

- **Misconception:** "We need to approve every discount."
  **Reality:** Over-governance creates bottlenecks. The green zone exists so reps can close standard deals without waiting for approval. The goal is to create guardrails where the risk justifies oversight, not gates that slow every deal.

- **Misconception:** "Once we set the matrix, it's done."
  **Reality:** The approval matrix is a living document. It should be reviewed quarterly as COGS, CAC, or strategic priorities change [7].

---

### PLG vs. SLG vs. Hybrid Pricing Architecture

*What is it?*

The go-to-market motion dictates the pricing architecture. Product-Led Growth (PLG) companies need self-serve pricing that buyers can evaluate and purchase without talking to a human. Sales-Led Growth (SLG) companies need pricing that supports custom quoting, negotiated discounts, and multi-stakeholder approval. Hybrid companies -- which represent the majority of Series A-C B2B SaaS -- need both architectures to coexist.

*Why does it matter?*

Pricing architecture that works for PLG (transparent, self-serve, tier-based) does not work for SLG (flexible, negotiable, relationship-based), and vice versa. A hybrid company that tries to force one architecture on both motions will either under-serve enterprise buyers (too rigid) or confuse self-serve buyers (too complex).

*The Framework:*

| Dimension | PLG Architecture | SLG Architecture | Hybrid Architecture |
|-----------|-----------------|-------------------|-------------------|
| **Pricing visibility** | Public pricing page with all tiers and prices visible | "Contact Sales" for enterprise; may show starter pricing | Public pricing for self-serve tiers; "Contact Sales" for enterprise |
| **Packaging model** | Good-Better-Best tiers (3-4 options) with clear feature gating | Custom packaging per deal; product catalog supports mix-and-match | Tiered for self-serve; custom for enterprise. Two distinct packaging paths. |
| **Discount structure** | None or minimal (annual prepay discount only) | Negotiated discounts with approval matrix | No discounts on self-serve; full discount matrix on sales-led deals |
| **Billing** | Automated (Stripe or similar payment processor) | Invoice-based, often through CPQ-generated contracts | Automated for self-serve; invoice for enterprise. Two billing paths. |
| **Key tools** | Stripe, payment processor, in-app billing | DealHub, PandaDoc CPQ, Salesforce CPQ | Both tool sets, connected to unified product catalog |
| **Approval workflow** | None -- purchase is self-serve | Multi-tier approval matrix | None for self-serve; full approvals for sales-led |
| **Output document** | Online checkout confirmation, receipt | Order form, MSA, SOW with e-signature | Checkout receipt for self-serve; order form for enterprise |

*Common misunderstandings:*

- **Misconception:** "We are PLG, so we don't need pricing structure."
  **Reality:** PLG requires the most rigorous pricing structure because there is no sales rep to explain or contextualize pricing. Every tier, feature gate, and usage limit must be self-explanatory.

- **Misconception:** "We can figure out enterprise pricing when we get there."
  **Reality:** If your PLG pricing does not have a natural upgrade path to enterprise, you will create friction when sales-led deals start. The hybrid architecture should be designed from the start, even if enterprise deals are not yet happening.

---

### Pricing & Packaging as a Prerequisite

*What is it?*

Pricing & Packaging sits upstream of every other Quote-to-Cash system. It is the foundational layer that must be resolved before CPQ tools can be configured, billing systems can be set up, and revenue recognition tracking can be established. In the Q2C project hierarchy, the gating question is: "Do we need to refine pricing and packaging?" If yes, P&P must be addressed before any systems work begins.

*Why does it matter?*

Building CPQ on top of undefined pricing is like building a house on sand. The CPQ will need to be reconfigured every time pricing changes, billing rules will break, and rev rec will be inaccurate. Getting pricing right first -- even if it takes additional weeks -- prevents rework that costs months.

*The Dependency Chain:*

```
Pricing & Packaging (must be stable)
    |-- CPQ Implementation (quotes structured pricing)
    |-- Billing System (invoices based on pricing)
    |-- Rev Rec (recognizes revenue per pricing rules)
    |-- Usage Metering (tracks consumption against pricing tiers)
```

If P&P is already clear and stable, the client skips the P&P project and goes directly to the relevant downstream system. If P&P is not clear, it must be resolved first -- or every downstream project will stall when it hits pricing questions.

---

## 2) Decision Frameworks

### Approach Selection Matrix

The P&P project approach depends on the intersection of two primary axes: **GTM motion** and **pricing maturity**. This matrix determines project scope, deliverables, and timeline.

| GTM Motion | Pricing Maturity: Undefined | Pricing Maturity: In Flux | Pricing Maturity: Stable |
|------------|---------------------------|--------------------------|------------------------|
| **PLG** | Full pricing definition: value metric selection, tier design, feature gating, pricing page architecture | Pricing workshop to finalize pending decisions, then tier restructuring | Optimization only: tier boundary analysis, price sensitivity testing |
| **SLG** | Full pricing definition: product catalog creation, discount matrix, approval workflows, output document design | Pricing workshop to stabilize, then catalog structuring and approval matrix design | Catalog optimization: SKU rationalization, approval workflow tuning |
| **Hybrid** | Both PLG and SLG tracks required. Most complex engagement. | Separate workshops for self-serve and enterprise pricing. Finalize, then build both architectures. | Dual-path optimization: ensure self-serve and enterprise pricing coexist without conflict |

### Scoping Factors

These variables determine which approach to use and the level of effort required. For each factor, the decision point determines project scope.

**1. Sales Team Size (Headcount)**

Headcount is the primary driver of governance complexity. More reps means more pricing variation, more approval rules, and more enforcement surface area.

- **&lt; 10 reps** --> No formal P&P project needed. Excel-based pricing is adequate. One person can manage all pricing decisions.
- **10-25 reps** --> Light P&P project. Basic list prices, one approval tier, one deal desk person.
- **25-50 reps** --> Standard P&P project. Full product catalog, discount matrix with tiered approvals, output document template.
- **75-100+ reps** --> Enterprise P&P project. Regional pricing, multinational approval chains, product-specific rules. Could involve 100+ approval rules.

**2. Product Complexity (Number of SKUs and Interrelationships)**

- **1-5 SKUs, independent** --> Low complexity. Pricing can be a simple spreadsheet or CRM-native configuration.
- **6-20 SKUs, some dependencies** --> Medium complexity. Need organized catalog with defined relationships. Some bundles or conditional pricing.
- **20+ SKUs, interdependent** --> High complexity. Full product catalog with relationship mapping (bundles, exclusions, dependencies, conditional pricing). CPQ is likely required downstream.

**3. Pricing Individualization**

- **Standardized pricing (mathematical trajectory)** --> Lower complexity.
- **Segment-specific pricing** --> Medium complexity. Different price lists for SMB vs. mid-market vs. enterprise, but consistent within segments.
- **Fully custom per-deal pricing** --> Highest complexity. Every deal is negotiated. Requires strong guardrails and approval matrix to prevent margin erosion.

**4. Year-Over-Year Ramp Structure**

- **No ramps** --> Simpler line item structure. One line per product per contract.
- **Seat ramps OR percentage escalation** --> Moderate increase. Year-by-year line items needed.
- **Both seat ramps AND percentage escalation** --> Complex. Multi-dimensional line items per year per product.

**5. Pricing Model Type**

- **Single model (per-seat or flat)** --> Straightforward catalog structure.
- **Tiered (Good-Better-Best)** --> Need feature gating logic and tier boundary definitions.
- **Usage-based** --> Need usage metering, committed amounts or rate cards, overage pricing. Additional infrastructure required.
- **Hybrid (subscription + usage)** --> Most complex. Two billing dimensions per product.

**6. Output Document Readiness**

- **Have existing order form / contract template** --> Can proceed to catalog structuring immediately.
- **No output document** --> Major scope addition. Document design becomes a sub-project with its own stakeholder approvals.

**7. Pricing Strategy Stability**

- **Pricing finalized, leadership aligned** --> Proceed to structuring.
- **Mostly finalized, 1-2 pending items** --> Isolate pending decisions, set deadline, proceed on stable elements.
- **In flux / being debated** --> Must conduct pricing strategy workshop first. Do NOT proceed to catalog structuring.

### PLG Pricing Architecture

*Best for:*
- Self-serve SaaS companies where buyers evaluate and purchase without talking to sales
- Products with clear feature differentiation across tiers
- Companies with &lt; $10K ACV on self-serve deals

*Not recommended for:*
- Companies where every deal requires custom scoping
- Products where pricing depends on buyer-specific variables that cannot be standardized
- Companies with no public-facing pricing (pure enterprise SLG)

*Key differences from standard:*

| Aspect | Standard (SLG) | PLG Architecture |
|--------|---------------|-----------------|
| Pricing visibility | "Contact Sales" | Public pricing page with all tiers visible |
| Packaging | Custom per deal | Fixed tiers (Good-Better-Best) |
| Discounts | Negotiated | None or annual prepay only |
| Purchase flow | Sales rep creates quote | Self-serve checkout |
| Value metric | Per-seat or custom | Must be self-explanatory (per user, per workspace, per 1K events) |
| Billing | Invoice-based | Automated payment processing (Stripe) |

*PLG packaging design principles:*
- 3 tiers plus enterprise "Contact Sales" is the industry standard (3.2 average public tiers across SaaS verticals) [3]
- Each tier targets a distinct buyer persona (individual, team, organization)
- Usage limits on 3-5 key factors per tier [8]
- Feature gating should feel natural -- higher tiers unlock capabilities that only larger teams need
- Free tier or free trial as acquisition mechanism (38% of SaaS companies offer freemium, 14-day average trial) [3]

### SLG Pricing Architecture

*Best for:*
- Companies where deals exceed $25K ACV
- Products requiring configuration, integration, or customization per customer
- Organizations with established sales teams and deal desk functions

*Not recommended for:*
- Pure self-serve products with high volume and low ACV
- Companies without any sales infrastructure

*Key differences from standard:*

| Aspect | Standard (PLG) | SLG Architecture |
|--------|---------------|-----------------|
| Product catalog | Fixed tiers | Mix-and-match SKUs from product catalog |
| Discount structure | None | Multi-tier approval matrix (Green/Yellow/Red zones) |
| Approval workflow | None | Manager, director, VP, finance approvals based on discount depth |
| Output document | Online receipt | Order form with pricing tables, legal language, e-signature |
| Contract terms | Monthly or annual | Annual or multi-year with ramps, custom payment terms |
| Tool requirements | Payment processor | CPQ tool (DealHub, PandaDoc CPQ, Nue), CRM quoting |

*SLG catalog design principles:*
- Every product/service needs a SKU, list price, and defined line item structure
- Product relationships (bundles, dependencies, exclusions) must be documented
- Discount rules must be encoded, not tribal knowledge
- Approval workflows must be defined before CPQ can be configured
- Output document template must exist before quoting can begin

### Hybrid Pricing Architecture

*Best for:*
- Most Series A-C B2B SaaS companies
- Companies with both self-serve and enterprise motions
- Companies transitioning from PLG to adding a sales team, or SLG to adding a self-serve tier

*Not recommended for:*
- Very early-stage companies (&lt; 20 customers) -- pick one motion first
- Companies where 95%+ of revenue comes from one motion -- optimize that first

*Key differences from standard:*

| Aspect | Single-Motion | Hybrid Architecture |
|--------|--------------|-------------------|
| Product catalog | One structure | Unified catalog that supports both self-serve tiers AND custom SKU combinations |
| Pricing paths | One | Two: self-serve checkout AND sales-quoted deals |
| Discount matrix | One or none | Discounts only on sales-led deals; self-serve pricing is fixed |
| Billing infrastructure | One system | Two systems or one system with two billing paths |
| Pricing page | Either public or hidden | Public for self-serve tiers; "Contact Sales" for enterprise |

*Hybrid design principle:* The PLG and SLG pricing paths must share the same underlying product catalog. A customer who starts on a self-serve tier and upgrades to enterprise should not need to be "re-created" in a different system. The unified catalog is what makes this possible [1].

---

## 3) Benchmarks & Standards

### How to Use Benchmarks

Benchmarks are guidelines, not rules. Always:
1. Start with benchmark as baseline
2. Adjust based on client-specific data (industry, ACV, sales cycle)
3. Validate against their actual numbers when available
4. Document deviations and rationale

### Pricing Model Adoption

| Model | Adoption Rate (2025) | YoY Change | Net Revenue Retention Impact |
|-------|---------------------|------------|------------------------------|
| Per-seat (per-user) | 57% | -7 pts (was 64%) | Baseline |
| Usage-based | 43% | +8 pts | +18-23% higher NRR [3] |
| Tiered (Good-Better-Best) | Industry standard for PLG | Stable | Varies by tier design |
| Hybrid (subscription + usage) | 61% | +12 pts (was 49%) | Highest expansion potential |
| Freemium | 38% | -3 pts | Lower initial, higher long-term if conversion is strong |

**Source:** Monetizely SaaS Pricing Benchmark Study 2025 (100+ companies analyzed) [3]

**Interpretation:**
- Per-seat pricing is declining as companies add usage-based components
- Hybrid is the fastest-growing model -- majority of SaaS now uses multiple pricing dimensions
- Companies valued above $100M use at least three pricing dimensions [5]

### Pricing Tier Benchmarks

| Vertical | Average Public Tiers | Enterprise Option Rate | Per-User Median |
|----------|---------------------|----------------------|-----------------|
| DevTools | 3.2 | 89% | Varies |
| MarTech | 3.8 | 94% | $89/user/month |
| HR Tech | 3.1 | 78% | $8/user/month |
| FinTech | 2.8 | 96% | Varies |
| Productivity | 3.4 | 71% | Varies |
| Analytics | 2.9 | 88% | $95/user/month |
| CRM | Varies | Varies | $65/user/month |
| Security/Compliance | Varies | Varies | $89/user/month |

**Source:** Monetizely SaaS Pricing Benchmark Study 2025 [3]

### Enterprise Contract Benchmarks

| Metric | Value | Context |
|--------|-------|---------|
| Median ACV (all private B2B SaaS) | $26,265 | Up from $22,357 prior year [9] |
| Median ACV (&lt; 100 seats) | $47,000 | +18% YoY [3] |
| Median ACV (100-500 seats) | $156,000 | +21% YoY [3] |
| Median ACV (500-1,000 seats) | $412,000 | +24% YoY [3] |
| Median ACV (1,000+ seats) | $890,000 | +27% YoY [3] |
| Multi-year contract prevalence | 56% | Of enterprise deals [3] |
| Average discount for 3-year commitment | 23% | Industry average [3] |
| Platform fee inclusion | 67% | Of enterprise contracts [3] |
| Professional services as % of Year 1 | 12-18% | Mid-market contracts [3] |

**Source:** Monetizely SaaS Pricing Benchmark Study 2025 [3], SaaS Capital [9]

### Pricing Governance Benchmarks

| Metric | Low | Typical | High | Notes |
|--------|-----|---------|------|-------|
| Discount approval tiers | 1 tier | 3 tiers (Green/Yellow/Red) | 5+ tiers | More tiers needed as headcount increases |
| Rep autonomy range (Green zone) | 0-5% | 0-15% | 0-20% | Higher autonomy = faster deal velocity but more margin risk |
| Manager approval threshold | 5-10% | 15-25% | 30%+ | Depends on margin structure and ACV |
| SaaS gross margin target | 70% | 75-85% | 85%+ | Discount policy must protect this floor [7] |
| CAC payback period target | 18 months | &lt; 12 months | &lt; 8 months | Discounts directly extend CAC payback [7] |

**Source:** Glencoyne Enterprise Discount Approval Matrix [7]

### CPQ Impact Benchmarks

| Metric | Without CPQ | With CPQ | Source |
|--------|------------|----------|--------|
| Quote creation time | 30-60 minutes | 5-10 minutes | DealHub |
| Quote creation time (differential) | 73% more time | Baseline | Monetizely [2] |
| Sales cycle length | Baseline | 28% shorter | Forrester [2] |
| Deal margin | 4-10% margin leakage | 15% higher margins | Nucleus Research [2] |
| First-year CPQ ROI | N/A | 105% average | Forrester [2] |
| 3-year CPQ value per $1 spent | N/A | $6.22 | Nucleus Research [2] |

### Quick Reference Thresholds

| Question | Good | Warning | Red Flag |
|----------|------|---------|----------|
| How long does it take to produce a quote? | &lt; 15 minutes | 15-30 minutes | > 30 minutes |
| What percentage of deals require pricing exceptions? | &lt; 20% | 20-40% | > 40% (pricing structure may not match market) |
| How many approval rules exist? | Matches org structure | 2x number of approval levels vs. org tiers | 100+ rules without automated routing |
| How often does pricing change? | Annually or less | Quarterly | Monthly or more (instability signal) |
| Do reps know the list price for all products? | Yes, from the system | For most products | No, they have to ask |

---

## 4) Calculations & Scoring

### Pricing Complexity Score

This is a qualitative project, so formal calculations are limited. However, a complexity scoring rubric helps scope the P&P engagement accurately.

### P&P Engagement Complexity Rubric

Score each factor from 1-3, then sum for total complexity.

| Factor | 1 (Low) | 2 (Medium) | 3 (High) |
|--------|---------|------------|----------|
| **Product count** | 1-5 SKUs | 6-20 SKUs | 20+ SKUs |
| **Product interrelationships** | All independent | Some bundles/dependencies | Complex dependency chains |
| **Pricing model** | Single model (per-seat or flat) | Two models (e.g., per-seat + one-time) | Hybrid or usage-based |
| **GTM motion** | Single (PLG or SLG only) | Primary + minor secondary | True hybrid (both material) |
| **Sales team size** | &lt; 10 reps | 10-50 reps | 50+ reps |
| **Year-over-year ramps** | None | One type (seat or percentage) | Both types |
| **Output document readiness** | Have template | Have drafts/fragments | Nothing exists |
| **Pricing strategy stability** | Finalized | Mostly finalized | In flux |

**Tier Thresholds:**

- **8-12 points (Light):** Catalog cleanup and basic governance. Can often be handled within a broader Q2C engagement.
- **13-18 points (Standard):** Full P&P project. Product catalog creation, discount matrix, approval workflows, output document design.
- **19-24 points (Enterprise):** Enterprise-grade P&P. Regional pricing, complex approval chains, multi-motion architecture, extensive stakeholder alignment.

---

## 5) Edge Cases & Deep Dives

### Edge Case 1: Company with No SKUs or Line Items

*Scenario:*

Company has never used line items in their CRM. They sell by adjusting the total amount on the opportunity record. They may have product names but no SKU structure, no line item data, and no formal product catalog. This is common in companies that grew from a single product and added pricing complexity informally.

*Challenge:*

This company has no structural foundation. Introducing line items requires changing how reps create opportunities, how deals are reported, and how pricing is tracked. It is a cultural change, not just a data change. Additionally, without historical line-item data, there is no baseline for pricing analysis.

*Approach:*

1. Audit current products by reviewing recent deals (last 90 days) to understand what is actually being sold and at what prices
2. Define a SKU naming convention (e.g., `{PRODUCT}-{TIER}-{BILLING}` like `PLATFORM-PRO-ANNUAL`)
3. Map each product to a SKU with a list price based on the most common price actually charged
4. Decide line item structure: annual vs. monthly, ramp-capable or not, recurring vs. one-time
5. Build the product catalog in a spreadsheet first, validate with sales leadership, then load into CRM/CPQ

---

### Edge Case 2: Pricing Strategy in Flux

*Scenario:*

Company knows their current pricing but is planning to change it in 3-12 months. They want to implement systems now but also accommodate future pricing. Leadership is debating pricing changes, and internal alignment has not been reached.

*Challenge:*

This is the biggest delay mechanism in any P&P or CPQ engagement. The company uses the implementation team as a sounding board for internal pricing debates, and project progress stalls while they go back and forth. Timelines double.

*Approach:*

1. In discovery, explicitly ask: "Which pricing elements are stable and which are under discussion?"
2. Separate the stable from the in-flux. Build on what is stable NOW.
3. For in-flux elements: set a hard deadline (2-3 weeks maximum) for internal pricing decisions
4. Design for flexibility where pricing is changing -- use parameterized pricing (configurable price books) rather than hardcoded values
5. If pricing changes are imminent (&lt; 3 months), consider waiting for the change before beginning. This feels like a delay but is faster overall than building twice.

---

### Edge Case 3: Consumption / Usage-Based Pricing

*Scenario:*

Company charges based on usage rather than flat subscription fees. They may have committed consumption amounts, rate card tiers, overage pricing, or some combination. This is increasingly common in AI, data, and API-based SaaS products.

*Challenge:*

Usage-based pricing requires different data structures than flat subscription pricing. It introduces questions that do not exist in per-seat models: How is usage measured? What is the billing period? Are there committed minimums? What happens when usage exceeds the committed amount?

*Approach:*

1. Determine the pricing architecture: committed consumption amount (per month/year) OR rate card tiers OR pure pay-as-you-go
2. If committed amount: define the commitment level, billing frequency, and what happens if usage falls below commitment (use-it-or-lose-it vs. rollover)
3. If rate card: define tiers and price per unit at each tier
4. If overages: define the overage rate and calculation method (per-unit overage vs. next-tier pricing vs. automatic tier upgrade)
5. For downstream billing: usage tracking infrastructure (e.g., Metronome) must be connected to the billing system

---

### Edge Case 4: No Output Document / Order Form

*Scenario:*

Company has never formalized what their sales contract or order form looks like. They may use ad hoc Word docs, PowerPoint proposals, or email confirmations. There is no standard template.

*Challenge:*

Without a template, the company will request everything they can think of when given the opportunity to design one -- the "candy store" effect. Getting internal alignment on document design becomes a project in itself because SVP, CEO, legal, and finance all want different things.

*Approach:*

1. Ask: "What are you contracting with right now?" to find any existing baseline
2. If nothing exists, propose the standard SaaS output document structure: customer information, pricing table(s), subscription terms, legal language (T&Cs or MSA reference), signature block
3. Get internal sign-off on document structure BEFORE building
4. Limit initial scope to essentials; add complexity in later iterations

---

### Edge Case 5: Complex Product Cross-Sectioning (Sales vs. Finance Views)

*Scenario:*

Finance team wants pricing displayed by financial categories (recurring vs. one-time, by revenue type, by cost center) that do not align with how products are sold. A support add-on is sold as a bundle component but must be reported separately.

*Challenge:*

Creating pricing structures that serve both sales (how you sell) and finance (how you report) when the two perspectives do not align. This manifests as disagreements about product categorization and line item structure during catalog design.

*Approach:*

1. In discovery, ask both sales leadership and finance how they categorize products -- independently, before putting them in a room together
2. Document the misalignments as a dual-view mapping: "Sales sees X, Finance sees Y"
3. Design the product catalog to serve the sales view (this is what reps interact with), with metadata tags that enable the finance view through reporting
4. Do NOT create separate SKUs for the finance view -- this creates SKU proliferation and maintenance burden. Use category tags, revenue type flags, or reporting dimensions instead.

---

### Edge Case 6: Transition from PLG to Hybrid (Adding Enterprise Sales)

*Scenario:*

A PLG company that has been selling exclusively through self-serve tiers now needs to add an enterprise sales motion. They have a public pricing page with 3 tiers and automated billing through Stripe, but no CPQ, no approval workflows, no order forms, and no discount structure.

*Challenge:*

The existing pricing architecture was built for self-serve only. Enterprise buyers expect custom quotes, negotiated pricing, contract terms, and professional output documents. The company needs to add SLG pricing architecture without breaking the PLG architecture that drives the majority of current revenue.

*Approach:*

1. Keep the existing PLG tiers and billing infrastructure untouched
2. Create a separate enterprise product catalog that can include custom SKU combinations, multi-year terms, and usage commitments
3. Define the handoff threshold: at what deal size or customer profile does a buyer move from self-serve to sales-assisted? (Common thresholds: > $25K ACV, > 50 seats, or specific feature needs)
4. Build a basic discount approval matrix (start with the 3-zone model)
5. Design an enterprise output document (order form) that references the same product catalog
6. Select and implement a CPQ tool for the enterprise motion
7. Ensure the product catalog is unified -- self-serve and enterprise products should be from the same catalog with different packaging and pricing rules applied

---

## References

[1] [Zuora - SaaS Product Catalog Strategy: Designing for Hybrid Revenue](https://www.zuora.com/guides/saas-product-catalog-strategy/)
[2] [Monetizely - Implementing CPQ Software: Streamlining Complex B2B SaaS Pricing](https://www.getmonetizely.com/articles/implementing-cpq-software-streamlining-complex-b2b-saas-pricing)
[3] [Monetizely - SaaS Pricing Benchmark Study 2025](https://www.getmonetizely.com/articles/saas-pricing-benchmark-study-2025-key-insights-from-100-companies-analyzed)
[4] [Kalungi - The 12 Best SaaS Pricing Page Examples](https://www.kalungi.com/blog/best-saas-pricing-pages)
[5] [OpenView - 2024 SaaS Benchmarks Report](https://www.highalpha.com/2024-saas-benchmarks-report)
[6] [ProfitWell / Startup People - SaaS Pricing Research](https://www.startuppeople.com/articles/marketing-growth/saas-pricing)
[7] [Glencoyne - SaaS Enterprise Discount Approval Matrix](https://www.glencoyne.com/guides/enterprise-discount-approval-matrix)
[8] [ProductLed - Fueling Product-Led Growth with SaaS Pricing and Packaging Optimization](https://productled.com/blog/saas-pricing-and-packaging)
[9] [SaaS Capital - Average Deal Size for Private SaaS Companies](https://www.saas-capital.com/blog-posts/what-is-the-average-deal-size-for-private-saas-companies/)
