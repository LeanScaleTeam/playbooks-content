# Pricing & Packaging — Advisory

Pricing & Packaging (Q2C) - Defining the pricing architecture, product catalog, discount structures, and approval workflows that all downstream Quote-to-Cash systems depend on

## 1) Project Overview

### What is the name of this project?

Pricing & Packaging (Q2C) - Quote-to-Cash Prerequisite: Product Catalog, Pricing Strategy & Sales Governance

### What is the purpose of this project?

This project takes a company from unstructured, tribal pricing knowledge to a documented, organized pricing architecture. It produces a defined product catalog (SKUs, line items, list prices), discount structures with guardrails, tiered approval workflows, and output document templates (order forms, contracts). The result is a pricing foundation that downstream systems -- CPQ, billing, rev rec, and metering -- can operate on correctly.

> **Core transformation:** From "reps enter whatever price they want on the opportunity and nobody knows our discount rules" to a documented pricing architecture with defined products, list prices, discount policies, approval workflows, and output document templates that feed every downstream system.

### What Pricing & Packaging Unlocks

After this project is complete, the client can:

- Configure a CPQ tool (DealHub, PandaDoc CPQ, Nue) without stalling on undefined pricing decisions
- Set up billing systems (Stripe, Tabs, Chargebee) with structured product and pricing data
- Enforce discount governance through tiered approval workflows tied to org hierarchy
- Generate consistent, professional output documents (order forms, contracts) from standardized templates
- Report on revenue by product, category, and pricing dimension -- not just a single opportunity amount
- Onboard new sales reps with clear pricing rules instead of tribal knowledge from tenured reps

| Before | After |
| ------ | ----- |
| Reps write the price in every time ("floating list prices") with no guardrails | Defined list prices per SKU with discount rules and approval thresholds |
| No SKUs or line items -- just a product name and an amount on the opportunity | Organized product catalog with SKUs, line items, and pricing tiers |
| Pricing decisions made ad hoc during deals, different reps quoting different prices | Documented pricing policies and discount rules applied consistently |
| Approvals are informal ("ask the VP on Slack") or don't exist at all | Structured approval workflows based on discount depth, deal size, and org hierarchy |
| No standard output document -- reps use Word docs, PowerPoints, or email | Templated order forms and contracts with defined sections and legal language |
| Internal pricing debates happen during CPQ implementation, causing 2-4 month delays | Pricing strategy decisions made upfront, so implementation teams can build instead of consult |
| Finance cannot report by product category because everything is a single line amount | Structured pricing categories enable product-level revenue reporting and cross-sectional analysis |

### What business outcomes does this project drive?

**Primary Outcomes:**

- Faster quote generation: companies report going from 30-60 minutes per quote to 5-10 minutes when pricing is properly structured and loaded into a CPQ [1][2]
- Reduced revenue leakage: B2B companies lose 3-5% of annual revenue to pricing inconsistencies, unauthorized discounts, and missing governance [3][4]. Structured pricing with approval workflows closes this gap.
- Sales governance: tiered approvals prevent unauthorized discounting and give management visibility into every deal's pricing before it goes out the door

**Secondary Outcomes:**

- CPQ readiness: having organized pricing is the single biggest prerequisite for CPQ implementation. Without it, implementation stalls while the vendor becomes a pricing consultant. ("The fewer answers they have, the more we have to be consultants, which is fine, but is not ideal." -- Brett Davis, DealHub)
- Billing system readiness: structured product catalog and pricing data feed directly into subscription management and billing configuration
- Reduced deal cycle time: eliminating back-and-forth on pricing, approvals, and legal language during deals shortens the quote-to-close window
- Consistent market presentation: standardized output documents present a professional, unified face to buyers regardless of which rep sends the quote

### Who in the Org can benefit from this project?

VP Sales, CRO, Deal Desk Manager, RevOps / Sales Ops Manager, Finance (Controller / FP&A), Legal, Sales Managers, Sales Reps

Additional context on who cares about what:
- **VP Sales / CRO:** Owns discount approval thresholds and overall pricing governance. Receives top-tier approval escalations for strategic deals.
- **Deal Desk Manager:** Manages pricing exceptions, output documents, and approval routing. Primary day-to-day operator of the pricing architecture.
- **RevOps / Sales Ops Manager:** Configures and maintains the pricing system in CRM and CPQ tools. Builds and updates the product catalog.
- **Finance (Controller / FP&A):** Needs pricing categories and product cross-sections for revenue reporting. Defines how products map to financial categories (recurring vs. non-recurring, product lines).
- **Legal:** Approves contract language, boilerplate, and terms & conditions embedded in output documents.
- **Sales Managers / Directors:** Enforce discount policies at the team level. Approve discounts within their authority tier.
- **Sales Reps:** Use the pricing architecture daily to build quotes. Benefit from clear guardrails instead of guessing what they can offer.

### Pain Points this Project Solves

| Pain Point | What Pricing & Packaging Enables |
| ---------- | -------------------------------- |
| "We don't have a product catalog -- reps just type a product name and an amount into the opportunity." | Organized product catalog with SKUs, line items, and defined list prices. "Introducing people to line items is kind of world changing for them." -- Brett Davis, DealHub |
| "Our list prices are floating -- every rep enters a different price for the same product." | Defined list prices per SKU with guardrails. Without this, "you're building a free fill system where there really aren't guardrails other than maybe a blanket approval." -- Brett Davis |
| "We want to implement CPQ but our pricing strategy isn't finalized, so the vendor keeps waiting on us." | Pricing strategy and product architecture decided upfront, so CPQ implementation can proceed without becoming a pricing consulting engagement |
| "We have no standard contract or order form -- reps send whatever they put together." | Templated output documents with customer info, pricing tables, legal language, and signature blocks |
| "We don't know the relationships between our products -- which ones bundle, which are dependencies, which are add-ons." | Documented product relationship map showing bundles, dependencies, and exclusions |
| "Anyone can discount anything -- there's no approval process." | Tiered approval workflows where discount depth and deal size determine who must approve |
| "The people who make pricing decisions aren't available, so everything stalls." | Identified and scheduled pricing stakeholders with clear decision authority mapped before the project starts |
| "Finance needs revenue broken out by product type, but everything is one line item in the CRM." | Structured pricing categories that serve both how sales sells and how finance reports |

### The Data Behind the Problem

Pricing and packaging gaps create measurable drag across the entire revenue operation. The data points below validate why these problems persist and why they cost real money.

**The Revenue Leakage Problem:**
B2B companies lose up to 4% of annual revenue to pricing inconsistencies, unauthorized discounts, and missing governance, according to McKinsey research [3]. A separate Deloitte study found pricing leaks represent 3-5% of annual revenue for SaaS companies specifically [4]. On a $50M ARR base, that is $1.5M-$2.5M walking out the door every year. EY estimates businesses lose up to 5% of EBITDA to revenue leakage broadly [5]. 85% of B2B companies lack formal policies governing discount authority, leading to margin leakage estimated at 3-8% of potential revenue annually [6].

**The Pricing Ownership Vacuum:**
Many SaaS companies delay pricing updates because no one owns pricing as a function [7]. Over 94% of B2B SaaS pricing leaders update pricing and packaging at least once per year, with nearly 40% updating quarterly [8]. Yet most companies lack a designated pricing owner or committee, leaving pricing decisions scattered across sales, product, and finance with no single point of accountability.

**The Administrative Drag on Sales:**
Sales reps spend only 28% of their week actually selling [9]. Quote and proposal generation with approvals consumes 9.4% of a rep's week on average [9]. Without structured pricing, reps spend even more time chasing internal answers on what they can offer, what the list price should be, and who needs to approve the deal.

**The CPQ Readiness Gap:**
Sales reps take 73% more time to produce a typical quote when not using CPQ software [1]. Companies report generating quotes 10x faster after CPQ implementation -- but only when the pricing architecture is defined first [2]. 78% of companies stated that CPQ software reduced quote turnaround times by more than 50% [1]. The catch: CPQ cannot be configured without a structured product catalog, defined list prices, and documented discount rules. When companies try to implement CPQ without this foundation, "we become sounding boards for their internal discussions and we start wondering why we're here" -- Brett Davis, DealHub.

**The Pricing Complexity Trend:**
61% of SaaS companies now use some form of hybrid pricing model (combining subscription, usage-based, and flat-rate elements), up from 49% in 2024 [8]. Usage-based pricing appears in 43% of SaaS pricing models analyzed in 2025, up 8 percentage points from 2024 [8]. This growing complexity makes structured pricing architecture more necessary, not less -- every additional pricing dimension compounds the difficulty of manual, undocumented pricing.

### Key Metaphors or Frameworks

**The "Polynomial" Framework for Pricing Complexity**

The need for structured pricing is not determined by any single variable. It is a function of multiple compounding factors: number of products, interrelationship between products, pricing individualization, and deal volume. Brett Davis (DealHub CSM Manager) calls it a "polynomial" -- one factor alone might be manageable, but when multiple factors are high, the compound effect makes manual pricing unworkable.

> "It's like a little polynomial. There's the value... but the real thing is number of products and the interrelationship of products. If you have a high complexity of interrelationship of products... you're going to need CPQ." -- Brett Davis, DealHub

| Factor | Low Complexity | High Complexity |
| ------ | -------------- | --------------- |
| Number of products | 1-5 SKUs | 20+ SKUs |
| Product interrelationships | Independent products | Bundles, dependencies, exclusions |
| Pricing individualization | Standard list prices | Custom pricing per deal |
| Deal volume | &lt;10 quotes/month | 30+ quotes/day |

When to use: In discovery and scoping conversations when clients ask "do we need this?" The answer is never one factor -- it is the combination. A company selling a $27 deal that requires 35 products to express it has a harder pricing problem than a company selling a $100K deal with one line item.

When NOT to use: Do not over-complicate the pitch with executive sponsors who have a simple pricing structure. If the company sells 3 products with flat pricing and 5 reps, a spreadsheet may genuinely be fine.

**The "Candy Store" Effect for Output Documents**

When companies do not have an existing output document (order form, contract template), they treat the design process like visiting a candy store -- wanting everything they see, which creates scope creep and endless revision cycles. Senior leaders weigh in with personal preferences, and the document design becomes a project within the project.

> "If they don't know what they want on their output document, then they're just like at a candy store. They're like, oh, well, I want that, I want this, I want that." -- Brett Davis, DealHub

When to use: When explaining to clients why they need to bring an existing output document (or at least a clear definition of what they want) BEFORE starting a pricing or CPQ implementation. Set expectations early that document design adds significant scope.

When NOT to use: If the client already has a standardized order form or contract template.

### Target Motion

This project is designed for **sales-led growth (SLG) and hybrid GTM motions** in B2B SaaS -- any company where sales reps are quoting, negotiating, and closing deals that require pricing configuration, discount approval, and contract generation.

Strongest fit:
- Sales-led growth (SLG) with custom quoting, multi-product deals, and negotiated pricing
- Hybrid motions where PLG handles self-serve / SMB deals and sales-led handles mid-market and enterprise
- Companies preparing for CPQ, billing, or rev rec system implementations that require pricing as a prerequisite

PLG-specific considerations:
- Pure PLG companies still need packaging architecture (tier design, feature gating, pricing page structure), but the project scope is different -- focused on self-serve pricing tiers rather than discount governance and approval workflows
- For hybrid companies, the P&P project must address both motions: self-serve packaging for PLG AND discount/approval structures for SLG

Not a fit for:
- Pure PLG with no sales touch (self-serve only, no custom quoting) -- these companies need packaging strategy, not the full pricing governance architecture this project delivers
- Companies with a single product, flat pricing, and fewer than 10 reps -- a spreadsheet or CRM-native quoting is sufficient
- Companies where pricing strategy itself is being designed from scratch (that is a pricing strategy consulting engagement, not a P&P implementation project). This project assumes the company has products and pricing decisions to document, not that they need help deciding what to charge.

### Common Belief Barriers

**"We can figure out our pricing during CPQ implementation."**

This is the single most common -- and most expensive -- misconception. Brett Davis (DealHub CSM Manager) flags this as the biggest delay mechanism in every onboarding: "One of the biggest sort of delay mechanisms is going to be, okay, we have this is our pricing now, but this is where we want our pricing to be in a year or so, we think... a lot of times during the implementation, we become sounding boards for their internal discussions and we start wondering why we're here." When pricing is not decided before implementation begins, the implementation team becomes a pricing consultant -- which is not what you are paying them for. Timeline doubles. Costs increase. Frustration builds on both sides.

**The reframe:** "Your pricing strategy needs to be decided BEFORE you implement anything downstream. If the CPQ vendor is waiting on your internal pricing debates, you are paying implementation rates for strategy consulting."

**"We don't need SKUs or line items -- we just adjust the amount on the opportunity."**

This works at small scale with a few reps and simple products. It breaks the moment you need any of the following: governance (who approved that price?), product-level reporting (how much revenue from Product A vs. Product B?), or downstream system integration (CPQ, billing, and rev rec all require line item data). "We got customers who don't have SKUs or -- oh, well, we've only ever sold by adjusting the amount on the opportunity... introducing people to line items is kind of world changing for them. But it's like, we can't operate in any other way." -- Brett Davis

**The reframe:** "That approach works until you need governance, product-level reporting, or any downstream system. Line items are a prerequisite for scaling -- not optional complexity."

**"Our pricing is too unique to standardize -- every deal is different."**

High pricing individualization does not mean pricing cannot be structured. It means the pricing architecture needs to accommodate variability within guardrails. The question is not "is every deal the same?" but "can we define the rules and boundaries within which deals are customized?" Even highly individualized pricing follows patterns. "If you have a bunch of different pricing, but they're all along some mathematical trajectory, then it's not really that complicated." -- Brett Davis

**The reframe:** "Structured pricing does not mean rigid pricing. It means defining the boundaries, approval thresholds, and rules within which customization happens -- so you get flexibility WITH governance."

**"We want guardrails, but we also need full flexibility."**

This tension is universal and is where most pricing governance projects get stuck. "People want guardrails, but then they also want full flexibility. And so that's where we get into the most trouble." -- Brett Davis. The answer is tiered governance: lighter guardrails for standard deals (auto-approved within defined parameters) and escalating approval requirements as deals deviate further from standard pricing.

**The reframe:** "You cannot have both zero friction AND full governance. The design question is: at what threshold does flexibility require approval? That is the conversation this project facilitates."

---

## 2) Tools & Systems

### Primary Tools

**CRM (Salesforce / HubSpot)**

The product catalog and pricing data live in the CRM. P&P project outputs are configured here: product objects, price books, line item structures, discount fields, and approval rules.

**CPQ Tools (DealHub, PandaDoc CPQ, Nue)**

For companies with pricing complexity that exceeds CRM-native capabilities. DealHub supports multi-dimensional pricing structures including usage-based, tiered, and fixed models, with built-in pricing guardrails, discount management, and structured approvals [10]. PandaDoc CPQ handles document generation and e-signatures alongside pricing. Nue is a newer entrant focused on subscription and usage-based pricing. The P&P project defines the pricing architecture that these tools consume.

**Spreadsheet / Pricing Workbook (Google Sheets / Excel)**

The working tool during the P&P project itself. Used to build the product catalog, define discount structures, map approval workflows, and iterate on pricing before committing to system configuration. For companies under 10 reps with simple pricing, the spreadsheet may BE the final deliverable.

**Billing Tools (Stripe, Tabs, Chargebee)**

Downstream consumers of P&P output. Stripe handles PLG payment processing. Tabs uses AI to interpret contracts and generate billing schedules. Chargebee manages subscription billing. These tools need structured pricing data from the P&P project to be configured correctly.

**Usage Metering Tools (Metronome)**

For companies with consumption-based pricing. Metronome tracks usage data that feeds into billing. The P&P project defines the rate cards, committed consumption amounts, and overage tiers that metering tools enforce.

---

## 3) Stakeholders & Roles

### Client-Side Stakeholders

**VP Sales / CRO (Executive Sponsor)**

- Required for: Kickoff, pricing strategy alignment, discount policy approval, approval tier decisions
- Responsibilities: Final sign-off on discount thresholds and approval hierarchy. Owns the "guardrails vs. flexibility" trade-off decisions. Receives top-tier approval escalations for strategic deals.

**RevOps / Sales Ops Manager (Project Driver / Technical Owner)**

- Required for: All meetings, ongoing system configuration and maintenance
- Responsibilities: Configures pricing in CRM and CPQ tools, maintains product catalog, builds and updates approval workflows. Primary day-to-day operator post-handoff. "We talk to an admin and they're like, hey, well, you know, we need to keep our salespeople from doing these things. But also I need my admins to be able to do all these things." -- Brett Davis

**Deal Desk Manager (Input Provider / Operator)**

- Required for: Pricing strategy sessions, discount policy design, output document review
- Responsibilities: Manages pricing exceptions, owns output document quality, routes approvals. Cares about "time to produce" and "how much are we spending going back and forth in terms of approvals." -- Brett Davis

**Finance (Controller / FP&A) (Input Provider)**

- Required for: Product categorization sessions, pricing structure review
- Responsibilities: Defines how products map to financial reporting categories. "Sometimes people want to cross section every category of their products from a finance perspective." -- Brett Davis. Ensures pricing structure supports revenue recognition requirements.

**Legal (Input Provider)**

- Required for: Output document review, contract language approval
- Responsibilities: Approves boilerplate, T&Cs, and legal language in output documents. May need separate approval workflow for contract modifications.

**Sales Managers / Directors (Input Provider)**

- Required for: Discount threshold alignment, approval tier design
- Responsibilities: Define what discount levels they should approve vs. escalate. "Does the sales manager need to approve this or does a director or does CRO need to approve?" -- Brett Davis

### Technical Owners

**RevOps / Sales Ops Manager**

- Primary technical owner on client side
- Responsible for: CRM product catalog maintenance, price book updates, approval workflow modifications, output document template changes
- Owns: Ongoing pricing architecture maintenance after engagement ends

**CRM Admin (If Separate from RevOps)**

- When needed: Enterprise clients with dedicated Salesforce or HubSpot admin separate from RevOps
- Responsible for: Product object configuration, custom field deployment, approval process technical setup

**Enterprise Considerations:**

- Companies with 75+ reps may need regional pricing owners for EMEA, APAC, NA
- Multinational companies may need legal review per region for output document language
- Enterprise orgs with 100+ approval rules require dedicated governance documentation

---

## 4) Scoping

### Scoping Factors

**1. Sales Team Size (Headcount)**

- &lt;10 reps --> Minimal pricing structure needed. Excel-based catalog is fine. No formal approval workflow required.
- 10-25 reps --> Light governance. Basic list prices, one deal desk person, one approval threshold ("if I go over any percent discount, this person approves"). -- Brett Davis
- 25-50 reps --> Real team structure. Manager-level approval tiers, formal discount policies, organized product catalog with SKUs. -- Brett Davis
- 75-100+ reps --> Enterprise complexity. Regional pricing, multinational approvals, legal-specific rules, potentially 100+ approval rules. -- Brett Davis

**2. Product Complexity (SKUs and Interrelationships)**

- Single product / few products, independent --> Low complexity. Simple catalog, straightforward pricing.
- Many products, independent --> Medium complexity. Organized catalog needed but product relationships are straightforward.
- Many products, interdependent --> High complexity. Must document bundles, dependencies, exclusions, and conditional pricing. "We don't know the relationships of these products, that's where we get really bogged down." -- Brett Davis

**3. GTM Motion**

- Pure SLG --> Focus on discount structures, approval workflows, product catalog for CPQ, output documents
- Pure PLG --> Focus on self-serve pricing tiers, packaging visible to buyers, payment processor setup
- Hybrid (most common) --> Must address both motions. "Most likely we're going to have a hybrid recommendation. So I think what we would typically recommend is like this is how your PLG motion will go, this is how your sales-led motion will go."

**4. Pricing Individualization**

- Standardized pricing (mathematical trajectory) --> Lower complexity. "If you have a bunch of different pricing, but they're all along some mathematical trajectory, then it's not really that complicated." -- Brett Davis
- Highly individualized pricing --> Higher complexity. More exceptions, more approval rules, more edge cases.

**5. Year-Over-Year Ramps**

- No ramps --> Simpler line item structure. One row per product on the quote.
- Seat increases or percentage increases over contract years --> "We have to structure the data differently based on that." -- Brett Davis. Line items must be expressed year-by-year, creating a different data architecture.

**6. Output Document Readiness**

- Have an existing order form / contract template --> Can move directly to structuring pricing. Minor scope.
- No output document --> Major scope increase. Document design becomes a sub-project. "If they don't have an output document, then we don't know how they want to express themselves to the market and we can't really do anything." -- Brett Davis

**7. Pricing Strategy Stability**

- Pricing decisions finalized --> Can proceed with structuring and documentation immediately.
- Pricing strategy in flux --> "Biggest delay mechanism." Must include a pricing alignment workshop and set a deadline for decisions. "If people come to the onboarding and they're without a stable set of policies or stable set of orientation toward their products, that's where it gets hard." -- Brett Davis

**8. Consumption / Usage-Based Pricing**

- Flat subscription only --> Standard line item structure.
- Usage-based with committed amounts --> Medium complexity. Need committed consumption amounts per month/year.
- Usage-based with rate card tiers and overages --> Higher complexity. "We quote either a committed consumption amount maybe per month or per year or we present a rate card." -- Brett Davis

### Multiple Approaches

**Approach 1: Pricing Documentation (Light)**

- Criteria: Company has fewer than 25 reps, fewer than 20 SKUs, standardized pricing, single GTM motion. Pricing decisions are already made but not documented.
- Execution: Document existing pricing in a structured format. Build product catalog, define list prices, create basic discount policy, set up 1-2 approval tiers. Deliverable may be a pricing workbook rather than system configuration.

**Approach 2: Pricing Architecture (Standard)**

- Criteria: Company has 25-50+ reps, multiple product lines, tiered discounts, need for formal approval workflows and output documents. May have year-over-year ramps.
- Execution: Full product catalog design with SKU hierarchy. Discount governance framework with tiered approvals. Output document template design. System configuration in CRM or CPQ tool.

**Approach 3: Pricing Architecture (Complex / Hybrid)**

- Criteria: Company has hybrid PLG + SLG motion, usage-based pricing components, complex product interrelationships, regional pricing variations, or consumption-based billing.
- Execution: Both PLG packaging design (tiers, feature gating) AND SLG pricing architecture (discount governance, approvals, output docs). Rate card design for usage-based components. Multi-regional pricing if applicable. This is the most discovery-heavy variant.

**Approach 4: Pricing Strategy Alignment (Pre-P&P)**

- Criteria: Company's pricing strategy is NOT finalized. They need help deciding how to price and package before the architecture can be defined.
- Execution: Pricing strategy workshops to align stakeholders on products, pricing model, packaging tiers, and target market positioning. This is a PREREQUISITE to approaches 1-3 and should be scoped separately.

---

## 5) Discovery Questions

### Questions for Project Kickoff

**Product Catalog & SKUs**

- Do you have an organized product sheet or catalog of SKUs? *(If the answer is no, the P&P project starts from scratch building the catalog.)*
- Do you currently use line items in your CRM, or do you adjust the total amount on the opportunity? *(Companies without line items need foundational education on why line items matter.)*
- How many distinct products or services do you sell?
- What is the relationship between your products? Are there bundles, dependencies, or products that must be sold together? *(Product interrelationships are where projects "get really bogged down." -- Brett Davis)*

**Pricing Structure**

- Do you have defined list prices for each product/SKU, or are prices "floating" (reps enter each time)? *(Floating list prices mean "you're building a free fill system where there really aren't guardrails." -- Brett Davis)*
- Is your pricing standardized (following a mathematical pattern) or individualized per deal?
- Do you have year-over-year ramps? Can you increase the number of seats or apply a percentage increase across contract years? *(This fundamentally changes line item data architecture.)*
- Do you have consumption or usage-based pricing? If so, do you use committed amounts, rate cards, or overage tiers?
- What pricing model do you use? (Flat rate, per-seat, tiered, usage-based, hybrid)

**Pricing Governance & Approvals**

- What are your current discount approval policies? Who approves what level of discount?
- Do you have documented internal policies for pricing decisions, or are they ad hoc?
- Who are the decision makers for pricing, and how accessible are they? *(If decision makers are "more than a phone call away," expect delays. -- Brett Davis)*
- Do different deal types or regions have different discount authorities?

**Output Documents**

- Do you have an existing order form, sales order, or contract template? *(If not, ask: "What are you contracting with right now?" -- Brett Davis. No output document is a major scope increase.)*
- What information appears on your output document? (Customer info, line items, pricing tables, legal language, signatures)
- Do different deal types require different output document formats?

**GTM Motion & Downstream Systems**

- What is your GTM motion? (PLG, SLG, hybrid) *(This determines whether the P&P project needs to address self-serve packaging, sales-led governance, or both.)*
- Are you planning to implement a CPQ tool? If so, which one? (DealHub, PandaDoc CPQ, Nue, CRM-native)
- Are you planning to implement or change your billing system?
- What downstream systems will consume the pricing architecture this project produces?

**Readiness & Stability**

- Is your pricing strategy finalized, or are you planning pricing changes in the near term? *(If pricing is in flux, the P&P project must include a pricing alignment phase first.)*
- Are the people who make pricing decisions available and engaged for this project?
- Has your finance team defined how they want products categorized for revenue reporting?

### Information to Gather Before Implementation

**Product Catalog Data:**

Complete list of all products and services sold, with: product names, SKU numbers (if they exist), list prices, billing frequency (monthly/annual), product categories, and any known product relationships (bundles, add-ons, dependencies). If no catalog exists, the first phase of the project creates one.

**Current Pricing Documentation:**

Any existing pricing guides, rate cards, discount schedules, or pricing policy documents -- even if informal or outdated. These provide the starting point for formalization.

**Output Document Samples:**

Current order forms, contracts, SOWs, or whatever the company sends to buyers. Even a Word doc or email template counts. If nothing exists, allocate scope for document design.

**Approval Authority Map:**

Who currently approves discounts, and at what thresholds? Even if informal ("I just Slack the VP"), document the current state so the formal workflow can mirror actual practice.

**CRM / CPQ Access:**

Admin access to CRM (Salesforce or HubSpot) for product object and price book configuration. If a CPQ tool is in place, admin access for pricing rule configuration.

### Approach Decision Questions

| Question | Answer --> Approach |
| -------- | ------------------- |
| "Is your pricing strategy finalized?" | No = Approach 4 (Strategy Alignment) first. Yes = Proceed to Approach 1, 2, or 3. |
| "How many reps and products?" | &lt;25 reps, &lt;20 SKUs = Approach 1 (Light). 25-50+ reps, multiple product lines = Approach 2 (Standard). |
| "Do you have PLG and SLG motions?" | SLG only = Approach 2 (Standard). Hybrid = Approach 3 (Complex). Pure PLG = Different project scope. |
| "Do you have usage-based pricing?" | No = Standard line item structure. Yes with rate cards/overages = Approach 3 (Complex). |
| "Do you have an existing output document?" | Yes = Lower scope. No = Add document design scope to any approach. |
| "Do you have year-over-year ramps?" | No = Standard. Yes = Adds complexity to line item structure in any approach. |

---

## 6) Overcoming Common Belief Barriers

#### "We can figure out our pricing during CPQ implementation."

This belief costs companies 2-4 months of implementation delay and tens of thousands in wasted vendor hours. Brett Davis (DealHub CSM Manager) has seen this pattern repeatedly: the company starts CPQ implementation, realizes their pricing is not defined, and the implementation team sits idle while internal pricing debates play out. "A lot of times during the implementation, we become sounding boards for their internal discussions and we start wondering why we're here." The vendor is being paid implementation rates to wait for pricing decisions -- that is an expensive way to do pricing strategy.

The fix: resolve pricing and packaging BEFORE signing a CPQ contract. Define products, list prices, discount rules, and approval workflows first. Then hand a complete pricing architecture to the implementation team so they can build from day one.

**The reframe:** "Your CPQ vendor charges implementation rates to build, not to consult on your pricing strategy. Every week of pricing debates during implementation is a week of wasted implementation budget."

#### "We don't need SKUs or line items."

Line items are not complexity for complexity's sake. They are the data structure that every downstream system requires: CPQ needs line items to generate quotes. Billing needs line items to invoice correctly. Rev rec needs line items to recognize revenue by product. Finance needs line items to report by product category. Without line items, the company is locked into a "one amount on the opportunity" model that cannot support governance, reporting, or system integration.

At the individual deal level, adjusting the opportunity amount feels simpler. At the company level, it means zero visibility into what is actually being sold, at what price, with what discounts, and by which reps. Brett Davis: "Introducing people to line items is kind of world changing for them. But it's like, we can't operate in any other way."

**The reframe:** "Line items are not overhead -- they are the foundation for every system you will ever want to build on top of your sales data."

#### "Our pricing is too unique to standardize."

Every company believes their pricing is uniquely complex. In practice, even highly individualized pricing follows patterns -- ranges, tiers, mathematical trajectories, approved exceptions. The P&P project does not force rigid pricing; it defines the boundaries within which customization happens.

The real question is: can you define the rules? "If you have a bunch of different pricing, but they're all along some mathematical trajectory, then it's not really that complicated." -- Brett Davis. If every deal truly has no patterns, no ranges, and no rules, that itself is a problem worth solving -- because it means there is no pricing governance at all, and revenue leakage is likely occurring.

**The reframe:** "Standardized does not mean rigid. It means you have defined ranges, rules, and approval thresholds. Reps still customize within those boundaries -- they just cannot go outside them without approval."

#### "We want guardrails AND full flexibility."

This is the most honest objection, and the answer is tiered governance. Low-risk deals (standard pricing, small discounts) get auto-approved or need minimal oversight. Medium-risk deals (moderate discounts, non-standard terms) require manager approval. High-risk deals (deep discounts, strategic pricing, custom terms) require director or CRO approval. The design question is not "guardrails or flexibility?" -- it is "at what threshold does flexibility require approval?"

"People want guardrails, but then they also want full flexibility. And so that's where we get into the most trouble." -- Brett Davis. The P&P project forces these trade-off decisions to be made explicitly, documented, and codified -- so they do not get relitigated on every deal.

**The reframe:** "The question is not guardrails OR flexibility. It is: at what discount percentage or deal size does flexibility require a second pair of eyes? That is the line we are drawing together."

---

## 7) Metrics Impact & Success Measurement

### Power 10 Metrics Impacted

| Power 10 Metric | Impact Direction | Expected Magnitude | Notes |
| --------------- | ---------------- | ------------------ | ----- |
| Bookings | Increase | +5-15% | Faster quoting, consistent pricing, and reduced deal drag convert more pipeline to closed deals. CPQ-enabled companies report 43% improvement in deal closure rates [1]. |
| Opp --> CW Conversion Rate | Increase | +5-15% | Structured pricing eliminates internal pricing confusion that stalls or kills deals. Reps quote faster and with more confidence. |
| Opp --> CW Cycle Time | Decrease | -10-25% | Eliminating back-and-forth on pricing, approvals, and legal language reduces days-to-close. Approval workflows replace ad hoc Slack threads. |
| Net Retention | Increase | +2-5% | Consistent pricing across renewals and expansions. Year-over-year ramp structures codified instead of renegotiated each cycle. |

### Expected Outcomes

| Metric | Before | After | Source |
| ------ | ------ | ----- | ------ |
| Quote generation time | 30-60 minutes per quote | 5-10 minutes per quote | Brett Davis, DealHub; CPQ industry benchmarks [1][2] |
| Quote accuracy / pricing errors | High error rate from manual price entry | 57% increase in quote accuracy; 40% reduction in human errors [1][2] | CPQ industry statistics |
| Discount governance | No formal policy; reps discount at will | Tiered approval workflows with defined thresholds | P&P project deliverable |
| Revenue leakage from pricing | 3-5% of annual revenue [3][4] | Minimal -- governed by approval workflows and pricing guardrails | Deloitte, McKinsey |
| Product-level revenue reporting | Impossible (one amount per opportunity) | Revenue reportable by SKU, product line, category | P&P project deliverable |
| Approval cycle time | Avg 3.6 days, some exceeding 2 weeks [6] | Same-day for standard deals; 1-2 days for escalated deals | Industry benchmarks with structured workflows |

### How to Measure Success

**Leading Indicators (Early signals, Week 1-4):**

- Product catalog is complete: all SKUs documented with list prices, descriptions, and categories
- Discount governance framework is defined: threshold tiers, approver roles, and escalation rules documented and approved by VP Sales
- Output document template is finalized and approved by legal, sales leadership, and finance
- Approval workflows are configured and tested in CRM or CPQ tool
- Sales team has been briefed on new pricing rules and where to find them

**Lagging Indicators (Proof of success, Month 2-6):**

- Quote generation time decreasing (track average time from opportunity creation to quote sent)
- Approval cycle time within targets (standard deals same-day, escalated deals within 48 hours)
- Discount consistency improving (compare average discount percentage across reps -- variance should decrease)
- CPQ or billing implementation proceeds without pricing-related delays (if downstream systems are in scope)
- Revenue reporting by product/category is available and being used by finance
- Revenue leakage from unauthorized discounting decreases (compare pre/post discount audit)

---

## References

[1] [Valorx - CPQ Statistics for 2024](https://valorx.com/resources/blog/cpq-statistics/)
[2] [NetSuite - Calculating CPQ ROI](https://www.netsuite.com/portal/resource/articles/crm/cpq-roi.shtml)
[3] [McKinsey - B2B Revenue Leakage from Pricing Inconsistencies](https://www.withvayu.com/blog/b2b-saas-revenue-leakage-prevention-cfo-guide)
[4] [Deloitte - Pricing Leaks in SaaS](https://www.getmonetizely.com/articles/what-is-a-pricing-leak-and-how-does-it-affect-your-business)
[5] [EY - Revenue Leakage Impact on EBITDA](https://www.younium.com/blog/revenue-leakage)
[6] [Monetizely - Pricing Approval Workflow Research](https://www.getmonetizely.com/articles/pricing-governance-establishing-effective-policies-for-discounts-and-exceptions)
[7] [Paddle - Why You Should Change SaaS Pricing Every 6 Months](https://www.paddle.com/blog/frequency-pricing-change)
[8] [Monetizely - SaaS Pricing Benchmark Study 2025](https://www.getmonetizely.com/articles/saas-pricing-benchmark-study-2025-key-insights-from-100-companies-analyzed)
[9] [Salesforce - State of Sales 2024](https://www.salesforce.com/news/stories/sales-research-2023/)
[10] [DealHub - AI-Powered CPQ Platform](https://dealhub.io/platform/cpq/)
