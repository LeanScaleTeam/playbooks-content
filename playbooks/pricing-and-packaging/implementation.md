## Project One-Pager

### Pricing & Packaging (P&P) One-Pager

#### Project Type

- Category: Balanced (Strategic + Enablement)
- Primary Deliverable: Documented pricing architecture — product catalog, pricing strategy document, discount structure, approval workflow design, and output document template

##### Phase Relevance

| Phase          | Applies?  | Weight | Notes                                                                 |
| -------------- | --------- | ------ | --------------------------------------------------------------------- |
| 1. Strategy    | Yes       | Heavy  | Discovery-heavy; 4-6 refinement loops typical. Every company's pricing is different — cannot template a default opinion like Growth Model. |
| 2. Engineering | Optional  | Light  | CRM product catalog configuration, price book setup. No custom code. Some customers stop after strategy. |
| 3. Enablement  | Yes       | Heavy  | Sales team training on new pricing, discount policies, approval workflows, output document usage. This is where adoption happens. |
| 4. Handoff     | Yes       | Medium | Internal + External. Maintenance is pricing review cadence + catalog updates. |

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │    Heavy     │     │   Light      │     │    Heavy     │     │    Medium    │
  │ 1a→1b→1c→1d │     │ 2a→2b→2c→2d │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   Discovery-heavy      CRM catalog +        Sales training       Internal +
   4-6 refine loops     price book config    on new pricing       External handoff
```

**This project's flow:**
- Full 4-phase for most clients. Heavy strategy (discovery + pricing decisions), light engineering (catalog/CRM config), heavy enablement (training sales on new pricing/processes), standard handoff.
- Some customers skip Phase 2 entirely if the deliverable is a pricing strategy document and catalog spreadsheet — no system configuration required.
- Phase 3 is where most of the effort lands. P&P is an enablement-heavy project (20-30% Strategy, 20-30% Engineering, 40-50% Enablement) because the value is in getting the sales team to actually USE the new pricing structure, not just documenting it.

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Watch P&P intro video (5-10 min) explaining what the project covers and why it matters
- [ ] Provide current product catalog / SKU list (even if informal — spreadsheet, CRM export, or product page)
- [ ] Provide existing pricing documents (price lists, rate cards, discount schedules — whatever exists)
- [ ] Provide current output document (order form, sales order, contract template, or MSA + order form)
- [ ] Document current approval process (who approves discounts, at what thresholds, formal or informal)
- [ ] Document year-over-year ramp structures (if applicable — seat increases, percentage increases over contract years)
- [ ] Complete Definition Alignment Document (review key terms with leadership team)
- [ ] Identify and confirm availability of pricing decision makers for the project duration

##### Track B: Architect Prep
- [ ] Pull CRM product/price book data (if exists) to understand current catalog state
- [ ] Audit CRM opportunity structure — are line items used? Or is pricing a single amount field on the opportunity?
- [ ] Review any existing output documents provided by customer for structure, content, and completeness
- [ ] Assess pricing complexity using the Pricing Complexity Polynomial (see Methodology document): number of products, interrelationships, individualization, ramp structures
- [ ] Identify GTM motion (PLG, SLG, or hybrid) to determine which pricing architecture patterns apply
- [ ] Create v0 Product Catalog Draft from whatever inputs are available (CRM data, pricing page, provided docs)
- [ ] Create v0 Pricing Architecture Assessment — current state summary with ASSUMED flags on everything not yet confirmed

#### Refinement Loop (1b → 1c → 1d)

| Meeting       | Sub-Phase | Focus                                           | Stakeholder                        | Output                        |
| ------------- | --------- | ----------------------------------------------- | ---------------------------------- | ----------------------------- |
| Kickoff       | 1b        | Present v0 catalog + pricing assessment, validate assumptions, align on definitions | RevOps Lead, Sales Leader          | Corrections for v1            |
| Product Audit | 1c        | Walk through every product/SKU — confirm names, relationships, pricing, line item structure | RevOps Lead, Product (if needed)   | Validated product catalog v1  |
| Pricing & Discounts | 1c  | Define discount structure, approval tiers, guardrail policies | Sales Leader, Finance, Deal Desk   | Discount matrix + approval workflow draft |
| Output Document | 1c      | Design or refine order form / contract template sections | Deal Desk, Legal, Sales Leader     | Output document template v1   |
| Ramps & Edge Cases | 1c   | Year-over-year ramps, consumption/usage pricing, rate cards, bundles | Finance, RevOps Lead               | Edge case documentation       |
| Final Review  | 1d        | Full walkthrough of all deliverables, strategic approval | All stakeholders (incl. executive sponsor) | Signed-off pricing architecture |

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held — v0 presented, assumptions validated
- [ ] 1c. Product catalog audit complete — all SKUs documented with list prices, relationships, and line item structure
- [ ] 1c. Pricing strategy confirmed — pricing model(s) agreed, no decisions still in flux
- [ ] 1c. Discount structure defined — tiers, guardrails, approval thresholds documented
- [ ] 1c. Approval workflow designed — who approves what, at what level, for which deal types
- [ ] 1c. Output document template reviewed — sections defined, legal language confirmed, design approved
- [ ] 1d. Strategic sign-off obtained from executive sponsor

##### Phase 2: Engineering
- [ ] 2a. Tech spec created — CRM product catalog configuration, price book setup, approval automation rules
- [ ] 2b. Engineering handoff meeting held — RevOps or admin understands what gets built
- [ ] 2c. Build complete — products/SKUs created in CRM, price books configured, approval workflows automated
- [ ] 2d. QA/Test + customer sign-off — test quotes generated, approval routing verified, output document renders correctly

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped — pricing guides, discount policy docs, approval workflow diagrams, output document walkthrough
- [ ] 3b. Training sessions delivered — sales team, deal desk, management, legal
- [ ] 3c. Hypercare period complete — first 2-4 weeks of live usage monitored
- [ ] 3d. Enablement sign-off — team can generate quotes, follow discount policies, route approvals independently

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented — pricing review cadence, catalog update process, approval rule changes
- [ ] 4b. Internal handoff complete
- [ ] 4c. External handoff (LeanScale → Customer) complete — all documentation delivered
- [ ] 4d. Project closed and archived

#### Document Types

##### Working Documents (iterate together)

| Document                     | Purpose                                         | When Complete                              |
|------------------------------|------------------------------------------------|-------------------------------------------|
| Product Catalog Worksheet    | Capture all SKUs, prices, relationships         | All products documented with list prices   |
| Pricing Strategy Worksheet   | Capture pricing model decisions, guardrails     | Pricing model(s) agreed, no open questions |
| Discount Matrix Draft        | Define discount tiers and approval thresholds   | All tiers defined, approvers named         |
| Approval Workflow Map        | Document approval chain per deal type           | All routing rules defined                  |
| Output Document Draft        | Design order form / contract template sections  | Design approved by legal and sales leader  |

##### Deliverables (polished outputs)

| Deliverable                       | Created From                  | Customer Uses For                          |
|----------------------------------|-------------------------------|-------------------------------------------|
| Product Catalog (final)           | Product Catalog Worksheet     | CRM product setup, CPQ configuration       |
| Pricing Strategy Document         | Pricing Strategy Worksheet    | Internal alignment, board/investor reporting |
| Discount & Approval Policy        | Discount Matrix + Workflow Map| Sales governance, deal desk operations      |
| Output Document Template          | Output Document Draft         | Quote/contract generation                  |
| Pricing Architecture Diagram      | All working documents         | Executive presentation, onboarding new hires |

#### Enablement Details

##### Training Types

| Type           | Audience                             | Focus                                                          | Duration |
| -------------- | ------------------------------------ | -------------------------------------------------------------- | -------- |
| Leadership     | VP Sales, CRO, Finance              | Pricing strategy rationale, discount governance philosophy, how to read pricing reports | 30 min   |
| Sales Team     | AEs, SDRs                           | New product catalog, how to quote, discount guardrails, when to escalate | 45 min   |
| Deal Desk      | Deal Desk, Sales Ops                | Approval workflow operation, output document generation, exception handling | 60 min   |
| Technical      | RevOps, CRM Admin                   | Product catalog maintenance, price book updates, approval rule changes | 60 min   |
| Legal          | Legal team                          | Output document template, terms and conditions placement, approval routing for legal review | 30 min   |

##### Hypercare
- Applies: Yes
- Duration: 2-4 weeks post-launch
- Office Hours: Yes — weekly 30-min slot for questions on pricing, discounting, approvals

##### Training Assets to Create
- [ ] Video walkthrough: Product catalog walkthrough (what we sell, how it is structured)
- [ ] Video walkthrough: Discount policy and approval workflow walkthrough
- [ ] Video walkthrough: Output document / order form generation walkthrough
- [ ] Doc: Pricing quick reference card (one-pager for sales reps — products, list prices, discount limits)
- [ ] Doc: Approval routing reference (who approves what, thresholds, escalation path)
- [ ] Doc: Product catalog maintenance guide (how to add/modify SKUs, update prices)

#### Handoff & Retention

##### Internal Handoff
- Key context for Architect: Pricing strategy rationale, which decisions were contentious, which stakeholders are sensitive about pricing changes
- Escalation trigger: Any structural pricing change (new product, new pricing model, new approval tier), discount policy exceptions, product catalog restructuring

##### External Handoff (LeanScale → Customer)
- Final meeting agenda: Review all deliverables, walk through maintenance schedule, confirm documentation is accessible, answer final questions
- Documentation package: Product catalog, pricing strategy document, discount & approval policy, output document template, all training recordings, maintenance schedule

##### Maintenance Schedule
- Monthly: Spot-check discount compliance, review new product requests
- Quarterly: Full pricing review with stakeholders, catalog audit, approval workflow effectiveness check
- Who owns: Single project = customer RevOps owns | Dedicated = Architect owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: CPQ Implementation (the natural next step — P&P is the prerequisite for CPQ) → if no → Downsell: Managed pricing maintenance (quarterly review cadence) → Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~1 quarter after project close
- Internal prep trigger: 2 weeks before check-in
- Decision: Architect handles pricing maintenance / specialist needed for structural changes
- Natural expansion: CPQ implementation, billing system setup, rev rec configuration — all downstream Q2C projects that P&P unlocks

#### Key Assets

| Asset                          | Link   | When Used              |
| ------------------------------ | ------ | ---------------------- |
| Product Catalog Template       | [link] | Phase 1a — Architect Prep     |
| Pricing Strategy Worksheet     | [link] | Phase 1b — Kickoff     |
| Discount Matrix Template       | [link] | Phase 1c — Pricing & Discounts meeting |
| Approval Workflow Template     | [link] | Phase 1c — Pricing & Discounts meeting |
| Output Document Template       | [link] | Phase 1c — Output Document meeting |
| Pricing Quick Reference Card   | [link] | Phase 3b — Sales Training |

#### Definition Alignment Terms

| Term                    | Typical Definition                                                                                   |
| ----------------------- | ---------------------------------------------------------------------------------------------------- |
| SKU (Stock Keeping Unit)| A unique identifier for each distinct product or service offering. Even if you "only sell one product," different tiers, add-ons, or configurations each get their own SKU. |
| Line Item               | A single entry on a quote, invoice, or order form representing one product/service with its quantity and price. Companies that "adjust the amount on the opportunity" are not using line items. |
| List Price              | The standard, published price for a SKU before any discounts. If reps type the price in each time, you have "floating list prices" — which means you effectively have no list price. |
| Recurring vs Non-Recurring | Recurring items generate ongoing charges (subscriptions, licenses). Non-recurring items are one-time (implementation fees, setup costs). Some items may appear recurring but are actually non-recurring — this distinction affects billing, rev rec, and reporting. |
| Year-over-Year Ramp     | A pricing structure where the cost changes across years of a multi-year contract — typically seat count increases or percentage price increases each year. If ramps exist, line items must be structured year-by-year. |
| Output Document         | The customer-facing document generated from a quote — could be called an order form, sales order, contract, or SOW. This is what the buyer signs. |
| Discount Tier           | A predefined discount range that determines who needs to approve the deal. Example: 0-10% = rep approved, 11-20% = manager approved, 21%+ = VP approved. |
| Approval Workflow       | The routing logic that determines which person or role must approve a deal based on discount depth, deal size, product type, or other criteria. |
| Product Relationship    | How products relate to each other — bundles (sold together), dependencies (B requires A), exclusions (cannot sell C with D), or add-ons (optional extras for a base product). |
| Price Book              | A collection of products and their prices in the CRM. Companies may have one price book or multiple (by region, customer segment, or currency). |
| Rate Card               | A pricing table used for consumption/usage-based pricing that shows price per unit at different volume tiers. |

#### Common Gotchas

- **Pricing strategy not finalized before project starts** → Require pricing strategy sign-off as a Phase 1 gate. The fewer answers the customer has, the more the engagement becomes a consulting exercise — which is fine, but not ideal. Set a deadline for outstanding pricing decisions — do not leave them open-ended.

- **Decision makers more than a phone call away** → Identify and schedule all pricing stakeholders during Pre-Kickoff. When the people making the decisions are more than a phone call away, the project ends up with a lot of back-and-forth waiting. If a key decision maker cannot attend meetings, escalate before kickoff — not mid-project.

- **No existing output document** → Ask for current contracting artifacts on day one: "What are you contracting with right now?" If nothing exists, explicitly scope document design as a separate workstream. Without a template, the client treats design like a "candy store" — they want everything, and scope creeps fast.

- **Wanting guardrails AND full flexibility simultaneously** → Force explicit tradeoff conversations early. People want guardrails, but then they also want full flexibility — and that is where things get into trouble. Use the Discount Matrix to make these tradeoffs visible and concrete.

- **Changing pricing decisions mid-implementation** → Lock down pricing decisions at strategic sign-off (1d). Any changes after sign-off require a formal change request with timeline and scope impact. Treat pricing changes after sign-off the same way you would treat scope changes — because that is what they are.

- **Finance cross-section requirements differ from sales categories** → Discover finance reporting needs during the Product Audit meeting (1c). Products may need dual categorization — how sales sells them vs. how finance reports them.

- **CRM complexity blocking catalog setup** → Audit CRM complexity (required fields, validation rules, restricted picklists, custom flows) during Pre-Kickoff. The higher CRM complexity, the more challenging implementation will be. A 5-minute CRM audit in Track B can save hours of debugging in Phase 2.

- **Treating P&P as a documentation exercise instead of a change management exercise** → P&P is 40-50% enablement. A perfect pricing document that no one follows is worth nothing. Budget more time for training and adoption than for documentation. 85% of B2B companies lack formal discount authority policies, which means the sales team has likely never worked under pricing governance before.

- **Starting CPQ implementation before P&P is done** → P&P is a prerequisite for CPQ. If a customer pushes to start CPQ in parallel, they will build on an unstable foundation. Data quality issues in the product catalog translate directly into incorrect quotes in the CPQ system. Finish P&P first.

#### Methodology Options (if applicable)

| Option                         | When to Use                                                              | Complexity |
| ------------------------------ | ------------------------------------------------------------------------ | ---------- |
| Catalog-Only P&P               | Company has clear pricing strategy but no organized product catalog. Focus on SKU structure, list prices, and line item design. | Low        |
| Full P&P (SLG)                 | Sales-led company needs complete pricing architecture: catalog + pricing strategy + discounts + approvals + output document. | Medium-High |
| Full P&P (Hybrid PLG+SLG)      | Company has both self-serve and sales-led motions. Must design pricing that works across both — PLG pricing page tiers AND SLG custom quoting. Most complex because the two motions must coexist without contradicting each other. | High       |
| P&P + Output Document Design   | Company has no existing order form or contract template. Adds significant scope for document design, internal alignment (SVP/CEO approval), and legal review. | Medium-High (additive) |
| P&P Readiness Assessment Only  | Company is unsure if they need P&P work. Deliver a readiness assessment using the Pricing Complexity Polynomial from the Methodology document. Output is a recommendation, not a full project. | Low        |

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on the complete pricing architecture — product catalog, pricing strategy, discount structure, approval workflows, and output document template.
>
> **Output:** Definition Alignment Document + Pricing Architecture Package (signed off by stakeholders).

### 1a. Pre-Kickoff

> Two parallel tracks run after the AE closes and before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                         | Format             |
| ----------------------------- | ----------------------------------------------- | ------------------ |
| P&amp;P intro video               | Explain what a P&amp;P project covers and why pricing decisions must be made before implementation can begin | Video (5-10 min)    |
| Definition Alignment Document | Get stakeholder sign-off on pricing terms (SKU, line item, list price, etc.) — see Definition Alignment Terms table above | Google Doc         |
| Pricing intake checklist      | Request specific artifacts: product list, pricing docs, output document, approval process, ramp structures | Google Doc or Form |

**Why homework is critical for P&amp;P specifically:**

P&amp;P has more variation than any other LeanScale project type. Unlike Growth Model or Attribution, where LeanScale can come in with a templated opinion, P&amp;P requires heavy upfront discovery because every company's pricing is different.

The top delay factors in P&amp;P projects all trace back to missing homework:
- No product catalog or SKU list → cannot assess pricing complexity
- Pricing strategy in flux → project stalls while internal debates happen
- No output document → cannot design downstream deliverables
- Decision makers unavailable → approval decisions drag

**Completion tracking:** Follow up within 3 days of sending. Push hard before kickoff. If the customer cannot provide a product list or current output document, that itself is diagnostic — it means the project starts from a more foundational level.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                 | Output                            |
| ---- | ------------------------------------------------------ | --------------------------------- |
| 1    | Pull CRM product/price book data + audit line item usage on opportunities | Raw catalog data + CRM complexity assessment |
| 2    | Assess pricing complexity using the Polynomial framework (see Methodology document): products x interrelationships x individualization x ramps | Complexity rating (Low/Medium/High) + methodology option recommendation |
| 3    | Identify GTM motion (PLG, SLG, hybrid) from website, intake, and sales notes | Motion classification → determines pricing architecture approach |
| 4    | Build v0 Product Catalog from available data — SKUs, list prices, categories, relationships (all ASSUMED) | Product Catalog v0 (working document) |
| 5    | Build v0 Pricing Architecture Assessment — current state summary, identified gaps, recommended approach | Pricing Assessment v0 (presentation-ready) |

**Critical:** Mark everything as ASSUMED. The kickoff call validates. For P&amp;P, expect a higher percentage of ASSUMED items than other project types — this is normal given the discovery-heavy nature.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building anything.

| Term                    | Our Recommended Definition                                                 | Internally Approved? |
| ----------------------- | -------------------------------------------------------------------------- | -------------------- |
| SKU                     | A unique identifier for each distinct product or service you sell          | [ ] Yes / [ ] No     |
| Line Item               | A single entry on a quote/invoice representing one product with quantity and price | [ ] Yes / [ ] No     |
| List Price              | The standard published price for a SKU before discounts                    | [ ] Yes / [ ] No     |
| Recurring vs Non-Recurring | Recurring = ongoing charges; Non-Recurring = one-time charges           | [ ] Yes / [ ] No     |
| Year-over-Year Ramp     | Pricing changes across contract years (seat increases, % increases)        | [ ] Yes / [ ] No     |
| Output Document         | The customer-facing document the buyer signs (order form, contract, SOW)   | [ ] Yes / [ ] No     |
| Discount Tier           | A predefined discount range that determines approval routing               | [ ] Yes / [ ] No     |
| Approval Workflow       | Routing logic for who must approve based on discount depth or deal criteria | [ ] Yes / [ ] No     |
| Product Relationship    | How products relate: bundles, dependencies, exclusions, add-ons            | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your leadership team. These terms will be used throughout the project. Check "Yes" when approved internally. We cannot proceed with catalog design or discount structures until terms are aligned. This prevents the scenario where we build a pricing architecture and discover mid-project that your team defines "recurring" differently than we do.

---

### 1b. Kickoff Call

> **Purpose:** Present v0 product catalog and pricing assessment. Validate assumptions. Align on terminology. Identify which meetings are needed in the alignment loop.

#### Agenda (60-90 min)

| Time  | Topic                                      | What Happens                                                              |
| ----- | ------------------------------------------ | ------------------------------------------------------------------------- |
| 0-15  | Walk through v0 product catalog            | "Here's what we found in your CRM and intake — is this your full product set?" |
| 15-30 | Walk through v0 pricing assessment         | Present complexity rating, current state gaps, recommended approach        |
| 30-45 | Validate assumptions on product catalog    | ASSUMED → CONFIRMED or corrected. Flag missing products, undefined relationships |
| 45-55 | Review Definition Alignment Document       | Confirm or discuss any terms not yet approved                              |
| 55-65 | Identify gaps and missing stakeholders     | Who else needs to be in the room? What data is missing?                    |
| 65-75 | Plan alignment loop                        | Schedule topic-specific meetings: Product Audit, Pricing &amp; Discounts, Output Document, Edge Cases |
| 75-90 | Next steps and homework                    | Assign: who provides what, by when                                         |

#### What We Bring

- v0 Product Catalog (from Track B prep)
- v0 Pricing Architecture Assessment (current state, complexity rating, gaps, recommended approach)
- Definition Alignment Document (pre-filled with our recommended definitions)
- Questions list — what we need to validate, organized by topic
- Meeting plan proposal — which alignment meetings we think are needed based on complexity

#### What We Leave With

- Corrections on v0 product catalog (info needed for v1)
- Confirmed definitions (or clear blockers — e.g., "VP Sales disagrees on discount tier definitions, need separate call")
- Alignment loop scheduled by topic
- Clear homework: who provides missing product data, who gets sign-off on terms
- Understanding of which methodology option applies: Catalog-Only, Full SLG, Full Hybrid, or P&amp;P + Output Document Design

---

### 1c. Alignment Loop &amp; Strategic Meeting Cadence

> **Purpose:** Iterate on all pricing architecture deliverables until sign-off. Each meeting covers a specific topic.

#### The Pattern

```
Kickoff Call (present v0, gather corrections)
    ↓
Process kickoff → v1 catalog, v1 assessment
    ↓
Product Audit Meeting (walk through every SKU) → v2 catalog
    ↓
Pricing & Discounts Meeting (discount tiers, approvals) → discount matrix + approval workflow
    ↓
Output Document Meeting (order form design) → output document template
    ↓
Edge Cases Meeting (ramps, usage-based, bundles) → edge case documentation
    ↓
Final Review → Sign-off
```

#### Before Each Meeting

1. Process previous meeting transcript/notes
2. Update relevant deliverables (catalog, discount matrix, approval workflow, output document)
3. Prepare questions for next topic — focus on what is still ASSUMED

#### During Each Meeting

1. Walk through current version of the relevant deliverable
2. Capture corrections, additions, and decisions
3. Validate what is now CONFIRMED
4. Identify remaining ASSUMED items
5. Flag blockers — especially pricing decisions that require people not in the room

#### After Each Meeting

1. Process transcript and previous version to produce updated version
2. Track what moved from ASSUMED → CONFIRMED
3. Update working documents
4. Send summary to stakeholders with action items

#### P&amp;P-Specific Meeting Types

| Meeting Type             | Focus                                                                         | Stakeholder                              | Typical Duration |
| ----------------------- | ----------------------------------------------------------------------------- | ---------------------------------------- | ---------------- |
| Product Audit           | SKU-by-SKU walkthrough: names, prices, categories, relationships, line item structure | RevOps Lead, Product (if applicable)     | 60 min           |
| Pricing &amp; Discounts     | Discount tiers, guardrails, approval thresholds, governance policies           | Sales Leader, Finance, Deal Desk         | 60 min           |
| Output Document Design  | Order form sections, legal language, pricing table layout, signature flow       | Deal Desk, Legal, Sales Leader           | 45-60 min        |
| Edge Cases              | Year-over-year ramps, consumption/usage pricing, rate cards, bundles, multi-currency | Finance, RevOps Lead                     | 45 min           |
| Executive Alignment     | Pricing strategy rationale, major tradeoffs (guardrails vs flexibility)         | VP Sales / CRO, CEO (if involved in pricing) | 30 min           |
| Final Review            | Full walkthrough of all deliverables for sign-off                              | All stakeholders                         | 60 min           |

**Note on meeting sequencing:** Product Audit should happen before Pricing &amp; Discounts (you need to know what you sell before defining discount rules). Output Document Design can happen in parallel with Pricing &amp; Discounts if different stakeholders are involved. Edge Cases meeting is only needed if the customer has ramps, usage-based pricing, or complex bundling.

#### Typical Timeline

| Milestone               | Timing                                          |
| ----------------------- | ----------------------------------------------- |
| Pre-kickoff prep        | 2-5 days (longer than typical because discovery is heavier) |
| Kickoff call            | Day 1 of engagement                             |
| Meeting loop            | 2-4 weeks (depends on stakeholder availability and pricing decision readiness) |
| Final review + sign-off | When all inputs CONFIRMED and no pricing decisions are still in flux |

**Timeline risk:** The biggest variable is pricing strategy stability. If pricing decisions are being made during the project instead of before, the timeline can stretch significantly.

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm the complete pricing architecture is approved before proceeding to engineering or closing the project.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by all stakeholders
- [ ] Product catalog complete — all SKUs documented with list prices, categories, relationships, and line item structure
- [ ] Pricing strategy confirmed — no pricing decisions still in flux, model(s) agreed
- [ ] Discount tiers and guardrails defined and approved by sales leadership
- [ ] Approval workflow designed and approved — all routing rules, approvers, and thresholds documented
- [ ] Output document template designed and approved by legal, sales, and executive sponsor
- [ ] Year-over-year ramp structure documented (if applicable)
- [ ] Consumption/usage-based pricing documented — rate cards, committed amounts, overages (if applicable)
- [ ] Finance reporting requirements captured — any dual categorization needs addressed
- [ ] All critical inputs CONFIRMED (no remaining ASSUMED items in deliverables)

#### Decision Point

- **Proceed to Engineering** → Customer wants pricing architecture built into CRM/CPQ systems
- **Project complete** → Pricing architecture documentation IS the deliverable (customer's internal team or another vendor will do the build)
- **Proceed to CPQ project** → P&amp;P is complete, customer is ready for CPQ implementation as a separate engagement

> **Note:** Many P&amp;P projects end here. The strategic deliverable — the documented pricing architecture — is often the primary value. Engineering (Phase 2) is optional and depends on whether the customer wants LeanScale to configure their systems or whether they will use the deliverables to configure themselves or hand off to a CPQ vendor.

---

## Phase 2: Engineering

> **Goal:** Build the approved pricing architecture into the customer's systems — CRM product catalog, price books, approval automation, and output document template.
>
> **Output:** Configured system that matches the approved pricing architecture, tested and customer-approved.

| Project Type    | Engineering Weight | Example                                           |
| --------------- | ------------------ | ------------------------------------------------- |
| P&amp;P (this project) | Light (10-20%) | Product catalog in CRM, price books, basic approval rules. No custom code. |

### Sub-Phases

```
2a Tech Spec → 2b Engineering Handoff → 2c Build → 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate the approved pricing architecture into CRM/system configuration specifications.

**Input:** Signed-off Pricing Architecture Package from Phase 1

**What happens:**

1. Map each product/SKU from the catalog to a CRM product record (product name, SKU, list price, product family/category)
2. Map discount tiers to approval rules (trigger conditions, approver assignments, escalation paths)
3. Map output document sections to template fields in the CPQ or document generation tool
4. Identify build sequence: products first, then price books, then approval rules, then output document template

**Output:** Draft tech spec containing:

- Product-to-CRM field mapping (catalog SKU → CRM product record fields)
- Price book structure (single price book vs. multiple by region/segment/currency)
- Approval rule specifications (conditions, approvers, escalation, auto-approve thresholds)
- Output document template spec (sections, field placements, conditional logic, legal blocks)
- Build sequence and dependencies

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs with the person who will configure the systems (RevOps, CRM admin, or engineer).

**Who attends:** Architect + RevOps Lead / CRM Admin

**Agenda (30-45 min):**

| Time  | Topic              | What Happens                                 |
| ----- | ------------------ | -------------------------------------------- |
| 0-15  | Walk through specs | Architect explains pricing context + tech spec output |
| 15-30 | Admin questions    | Clarify CRM-specific considerations: existing validation rules, required fields, active flows that might conflict |
| 30-45 | Refine and approve | Adjust specs for CRM realities, confirm build approach |

**What Architect brings:**

- Pricing Architecture Package (for strategic context)
- Draft tech spec (from 2a)
- CRM complexity notes (from Pre-Kickoff audit)

**What admin/engineer leaves with:**

- Approved tech spec
- Clear build sequence
- Known risks: CRM flows that might block, required fields that conflict, existing approval processes to deactivate or modify

---

### 2c. Build (Configure)

> **Purpose:** Configure the pricing architecture in the customer's systems.

**Input:** Approved tech spec from 2b

**Build components for P&amp;P:**

| Component                | System            | What Gets Built                                          |
| ------------------------ | ----------------- | -------------------------------------------------------- |
| Product Catalog          | CRM (Salesforce/HubSpot) | Product records with SKUs, list prices, categories, relationships |
| Price Book(s)            | CRM               | Standard price book + any segment/region-specific books   |
| Discount Approval Rules  | CRM or CPQ tool   | Approval routing based on discount tiers from approved matrix |
| Output Document Template | CPQ tool or doc gen| Order form / contract template with all approved sections  |

**Execution approach for P&amp;P:** Manual build by RevOps/admin. P&amp;P configuration is typically straightforward CRM setup — product records, price books, approval rules. This is not custom code. The complexity is in the decisions (Phase 1), not the build.

**Build tracking:**

- [ ] Products/SKUs created in CRM
- [ ] List prices assigned in price book(s)
- [ ] Product categories and families configured
- [ ] Product relationships configured (bundles, dependencies — if CRM supports)
- [ ] Discount approval rules created and activated
- [ ] Output document template built and configured
- [ ] Test data prepared for QA

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify the CRM configuration matches the approved pricing architecture and get customer approval.

**Technical testing checklist:**

- [ ] All products visible in CRM product selector
- [ ] List prices pulling correctly from price book
- [ ] Discount approval triggers at correct thresholds (test: quote with 5% discount = auto-approved, quote with 25% discount = routes to manager)
- [ ] Approval routing goes to correct person at each tier
- [ ] Output document generates with all required sections
- [ ] Output document displays correct product/pricing information
- [ ] Output document renders legal language correctly
- [ ] Multi-year deals display year-over-year ramp correctly (if applicable)
- [ ] Rate cards render correctly in output document (if usage-based pricing)

**Customer testing:**

- Generate 3-5 test quotes using real deal scenarios:
  1. Standard deal (no discount) — verify product selection and list prices
  2. Discounted deal within rep authority — verify auto-approval or simple approval
  3. Heavily discounted deal — verify multi-level approval routing
  4. Multi-year deal with ramps — verify year-by-year pricing (if applicable)
  5. Bundle deal — verify product relationships and pricing (if applicable)
- Customer reviews output documents generated from each test scenario

**Engineering sign-off checkpoint:**

- [ ] All products configured correctly in CRM
- [ ] Approval rules firing as designed
- [ ] Output document template approved by customer
- [ ] Test quotes match expected pricing and approvals
- [ ] Ready for enablement

**Decision point:**

- **Proceed to Enablement** → System is configured, sales team needs training
- **Loop back to Build** → Issues found, needs fixes

---

## Phase 3: Enablement

> **Goal:** Sales team, deal desk, and management can actually use the new pricing structure, discount policies, and approval workflows.
>
> **Output:** Trained team with documentation, first live deals successfully processed, no critical issues.

### Sub-Phases

```
3a Training Prep → 3b Training Sessions → 3c Hypercare → 3d Enablement Sign-Off
```

**Why enablement is the heaviest phase for P&amp;P:** P&amp;P projects are enablement-heavy (40-50% of total effort). The reason: you are changing how salespeople price and sell. A documented pricing architecture that nobody follows is worthless. The sales team needs to understand the new product catalog, know the discount guardrails, follow the approval workflow, and generate output documents correctly. This is behavioral change, not just knowledge transfer.

---

### 3a. Training Prep

> **Purpose:** Create training materials from the finalized pricing architecture documentation.

**Input:** Pricing Architecture Package + tech specs + configured system

**What happens:**

1. Receive all project documentation
2. Generate draft training materials organized by audience
3. Architect reviews, refines, and records video walkthroughs

**Output:** Training package containing:

- **Pricing Quick Reference Card** — one-page summary for sales reps: products, list prices, discount limits, who to call for exceptions
- **Discount Policy Guide** — full discount tier breakdown, approval workflow diagram, escalation path
- **Product Catalog Reference** — complete catalog with SKUs, descriptions, relationships, and categories
- **Output Document Guide** — how to generate an order form / contract, what each section contains
- **Admin Maintenance Guide** — how to add new products, update prices, modify approval rules, update output document template

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to the customer's team — different audiences need different training.

| Type            | Audience                    | Focus                                                                          | Duration |
| --------------- | --------------------------- | ------------------------------------------------------------------------------ | -------- |
| Leadership      | VP Sales, CRO, Finance      | Pricing strategy rationale: why these guardrails, what outcomes to expect, how to read pricing compliance reports | 30 min   |
| Sales Team      | AEs, SDRs                   | New product catalog, how to build quotes, discount guardrails, when and how to escalate for approval | 45 min   |
| Deal Desk       | Deal Desk, Sales Ops        | Approval workflow operation, output document generation, handling exceptions, managing non-standard deals | 60 min   |
| Technical Admin | RevOps, CRM Admin           | Product catalog maintenance (add/modify SKUs, update prices), approval rule changes, output document template updates | 60 min   |
| Legal           | Legal team                  | Output document template, where legal language appears, approval routing for deals requiring legal review | 30 min   |

**Training delivery:**

1. Schedule sessions with appropriate stakeholders (can combine audiences if small team)
2. Deliver training live — walk through real scenarios, not theoretical examples
3. Record each session for future reference and new hire onboarding
4. Run a "first deal" exercise: have a rep build a real quote, route it for approval, generate the output document
5. Answer questions, note gaps in understanding

**Output:**

- Trained stakeholders across all relevant roles
- Session recordings for each audience
- Questions log (feeds into FAQ and identifies areas needing reinforcement)

---

### 3c. Hypercare

> **Purpose:** Intensive post-launch support to catch issues in the first live deals and reinforce new behaviors.

**Duration:** 2-4 weeks (standard for P&amp;P projects)

**What happens:**

- Monitor first 10-20 live deals for pricing compliance, approval routing accuracy, and output document quality
- Weekly 30-min office hours: anyone can join with questions about pricing, discounts, approvals
- Spot-check: are reps using the new catalog or reverting to old habits (typing amounts manually, skipping approvals)?
- Bug triage: fix any approval routing errors, output document rendering issues, or product catalog problems
- Reinforce: if reps are circumventing guardrails, address with sales leadership

**When enablement issues surface:**

| Issue | Response |
|-------|----------|
| Reps bypassing approval workflow | Escalate to sales leadership; clarify that bypassing is not acceptable |
| Quotes with incorrect products/prices | One-on-one coaching session; may indicate training gap |
| Output document rendering errors | Technical fix (Phase 2 loop-back); not an enablement issue |
| Approval bottleneck (deals stuck waiting) | Review approval workflow design — may need to adjust thresholds or add backup approvers |

**Output:** Stabilized system, first deals successfully processed, no critical issues outstanding

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm the customer's team can operate independently with the new pricing architecture.

**Validation checkpoint:**

- [ ] All training sessions delivered across all audience types
- [ ] Training recordings and documentation provided
- [ ] Hypercare period complete
- [ ] First 10+ live deals processed successfully through new pricing/approval/output workflow
- [ ] No critical issues outstanding (approval routing correct, output documents rendering, no pricing errors)
- [ ] Sales team can build quotes using the product catalog without reverting to manual pricing
- [ ] Deal desk can manage approval routing and exception handling independently
- [ ] Admin can add products, update prices, and modify approval rules independently
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** → Team is enabled, pricing architecture is in production use
- **Extend Hypercare** → Still seeing compliance issues, reps reverting to old behaviors, need more coaching time

---

## Phase 4: Handoff

> **Goal:** Clean project close with pricing maintenance plan established and retention/expansion path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the pricing architecture, project archived, CPQ or other Q2C expansion path identified.

**Structure:**

```
4a Maintenance Schedule → 4b Internal Handoff → 4c External Handoff → 4d Project Close
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At                                                                         |
| ----------------------------- | -------------------- | ------------------------------------------------------------------------------------- |
| **Single Project**            | Customer owns        | 4c (External Handoff) — customer receives maintenance schedule and runs it themselves |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) — Architect receives maintenance schedule and runs it for customer |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention after the project is complete — pricing reviews, catalog updates, discount compliance monitoring.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task                  | What to Check                                          | Red Flag Threshold                         |
| ----------------------------- | ------------------------------------------------------ | ------------------------------------------ |
| Discount compliance spot-check | Sample 10 closed deals: were discount policies followed? | &gt;20% of deals violated discount guardrails |
| Approval workflow accuracy    | Were deals routed to correct approvers? Any bypasses?   | Any approval bypass or mis-routing         |
| New product requests          | Were any new products sold that are not in the catalog? | Any product quoted that is not in catalog  |
| Output document quality       | Spot-check 5 output documents for accuracy and completeness | Missing sections, incorrect pricing, broken formatting |

**Quarterly Tasks:**

| Quarterly Task                 | What to Review                                          | Action if Off-Track                        |
| ------------------------------ | ------------------------------------------------------- | ------------------------------------------ |
| Full pricing review            | Are list prices still accurate? Any market changes requiring adjustment? | Update price books, communicate changes to sales team |
| Product catalog audit          | Any new products to add? Deprecated products to remove? Relationships changed? | Update catalog, retrain if significant changes |
| Discount tier effectiveness    | Are the discount tiers working? Too restrictive (deals stalling)? Too loose (margin erosion)? | Adjust tiers, update approval workflow     |
| Approval workflow optimization | Are approvals happening within target SLA? Any bottleneck roles? | Add backup approvers, adjust auto-approve thresholds |
| Finance alignment check        | Do product categories still match finance reporting needs? | Update categorization if needed            |

**After First Business Cycle (30-90 days post-launch):**

- Discount compliance rate: What percentage of deals followed pricing policies? Target: &gt;90%.
- Approval cycle time: How long are deals waiting for approval? Target: &lt;24 hours for standard tiers.
- Output document accuracy: Are output documents generating correctly with current pricing? Any rendering issues?
- Key Question: Is the pricing architecture actually being used, or are reps reverting to old habits?

**Refinement Triggers (when to re-engage):**

| Trigger                        | Threshold                          | Response                                                         |
| ------------------------------ | ---------------------------------- | ---------------------------------------------------------------- |
| Discount compliance            | &lt;80% compliance for 2+ months      | Re-engage specialist for pricing governance reinforcement               |
| New product launch             | Any new product or pricing model   | Scope catalog update project — add SKUs, update price books      |
| Pricing model change           | Shift from flat to usage-based, or adding a new pricing tier | Scope new P&amp;P engagement — significant structural change         |
| CPQ implementation readiness   | Customer wants to implement CPQ    | Scope CPQ project — P&amp;P deliverables are the input               |
| Sales team growth              | &gt;50% increase in sales headcount   | Refresh enablement — new hire pricing training                   |

**Every 6-12 Months:**

- Full pricing strategy review: Is the pricing model still competitive? Any market shifts?
- Product catalog rationalization: Identify dormant SKUs, consolidate overlapping products
- Discount policy recalibration: Update tiers based on actual deal data from the past 6-12 months
- Output document refresh: Update legal language, add new sections if needed, refresh design

---

### 4b. Internal Handoff

> **Purpose:** Transfer context so Architect can manage ongoing relationship.

**What the Architect needs to know:**

- Pricing strategy rationale — why specific discount tiers were chosen, what tradeoffs were made
- Contentious decisions — which stakeholders pushed back on guardrails, who wanted more flexibility
- Customer context — who owns pricing decisions, who is the day-to-day contact for pricing questions
- Common issues and how to resolve them — typical: "rep exceeded discount limit," "new product not in catalog"
- When to escalate back to specialist

**Escalation guidelines:**

| Issue Type                                  | Who Handles           |
| ------------------------------------------- | --------------------- |
| New product added to catalog                | Architect (add record, set price) |
| Price change on existing product            | Architect (update price book)     |
| New discount tier or approval rule          | Specialist (structural change)    |
| Pricing model change (e.g., flat → usage)   | Specialist (requires new P&amp;P engagement) |
| Sales team asking for exceptions to policy  | Architect escalates to sales leadership |

**For Dedicated engagements:** Architect also receives the maintenance schedule (4a) and becomes responsible for executing monthly/quarterly tasks.

---

### 4c. External Handoff (LeanScale → Customer)

> **Purpose:** Formal project completion with customer.

**Final project meeting:**

- Review what was delivered: product catalog, pricing strategy document, discount &amp; approval policy, output document template
- Walk through documentation package
- Walk through maintenance schedule in detail — monthly, quarterly, and annual tasks
- Confirm nothing outstanding
- Answer final questions
- Make it explicit: "Project complete"
- **For Single Project engagements:** Hand over the maintenance schedule and walk the customer through it — they own it from here

**Documentation package:**

- Product Catalog (final version — all SKUs, list prices, categories, relationships)
- Pricing Strategy Document (pricing model(s), rationale, competitive context)
- Discount &amp; Approval Policy (tiers, guardrails, approval workflow, escalation path)
- Output Document Template (order form / contract template)
- Definition Alignment Document (final version — all terms approved)
- Pricing Quick Reference Card (one-pager for sales reps)
- All training session recordings
- Admin Maintenance Guide
- Maintenance Schedule
- FAQ document (compiled from training sessions and hypercare)

**For Single Project engagements:** Walk the customer through the maintenance schedule in detail. Record a video walkthrough. Make sure they understand what to check, how often, and when to call LeanScale back.

**Output:** Customer owns the pricing architecture. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location
- [ ] Handoff documentation complete
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell → Downsell → Retry    |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: CPQ Implementation (natural next step — P&P is the prerequisite)
   ↓ if no
2. Upsell: Managed Services (quarterly pricing review retainer)
   ↓ if no
3. Downsell: Another one-time project (billing setup, rev rec, etc.)
   ↓ if yes
4. Retry retainer at end of next project cycle
```

**Script:**

> "Now that your pricing architecture is in place, there are two natural next steps. Option 1: We can implement CPQ — your pricing is now organized enough to power a quoting tool like DealHub or PandaDoc, which would automate quote generation and approval routing. Option 2: If CPQ is not the priority right now, we can set you up on a quarterly pricing review where we monitor discount compliance, update the catalog, and keep the architecture current. Which sounds more relevant?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On [date ~quarter out], we'll review how the pricing architecture is performing — discount compliance rates, approval cycle times, and any catalog updates needed."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                           |
| ------------------- | ------------------------------------------------------ |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks        |
| 2. Review metrics   | Pull discount compliance data, approval cycle times, deal velocity changes |
| 3. Decide ownership | Can Architect handle this check-in, or need specialist? |
| 4. Prep materials   | If specialist needed, brief them. If Architect, prep talking points. |

**At the refinement check-in:**

- Review discount compliance against target (&gt;90%)
- Review approval cycle times against target (&lt;24 hours)
- Identify any catalog updates needed (new products, price changes)
- If minor: Architect handles tweaks
- If major (pricing model change, new product line): Scope new P&amp;P or CPQ engagement

**Output:** Project archived. Future revenue path established (CPQ implementation is the highest-probability expansion). Ready for next engagement.

---

## Deliverables &amp; Assets Summary

**Strategic Deliverables:**

| Deliverable                    | Description                                                                  |
| ------------------------------ | ---------------------------------------------------------------------------- |
| Product Catalog                | Complete catalog of SKUs with list prices, categories, relationships, and line item structure |
| Pricing Strategy Document      | Documented pricing model(s), rationale, competitive context, and GTM motion considerations |
| Discount &amp; Approval Policy     | Discount tiers with guardrails, approval workflow with routing rules, escalation path, governance policies |
| Output Document Template       | Order form / contract template with customer info, pricing tables, legal language, and signature block |
| Pricing Architecture Diagram   | Visual summary of the complete pricing architecture for executive presentation |

**Technical Deliverables (if Phase 2 applies):**

| Deliverable                    | Description                                                                  |
| ------------------------------ | ---------------------------------------------------------------------------- |
| CRM Product Catalog            | Products/SKUs configured in CRM with list prices, categories, and relationships |
| Price Book(s)                  | Standard price book + any segment/region/currency-specific books              |
| Approval Automation            | Discount approval rules configured and tested in CRM or CPQ                   |
| Output Document Template       | Order form / contract template configured in CPQ or document generation tool   |

**Documentation Package:**

- Pricing Quick Reference Card (one-pager for sales reps)
- Discount Policy Guide (full breakdown with workflow diagrams)
- Product Catalog Reference (complete catalog for ongoing reference)
- Output Document Guide (how to generate and customize)
- Admin Maintenance Guide (how to update products, prices, approvals, templates)
- Training session recordings (one per audience type)
- FAQ document
- Definition Alignment Document (final version)
- Maintenance Schedule

---

## Appendix

### What This Document Is

This is the implementation playbook — the step-by-step execution guide an Architect follows to deliver a Pricing &amp; Packaging project from first contact to project close. It follows the 4-phase framework: Strategy, Engineering, Enablement, Handoff. It is the third file in a 3-file playbook structure (Overview, Methodology, Implementation).

### What Each Phase Produces

| Phase                    | Output                                                                 | Gate Criteria                                                                  |
| ------------------------ | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **Phase 1: Strategy**    | Signed-off Pricing Architecture Package (Definition Alignment Doc + product catalog + pricing strategy + discount policy + approval workflow + output document template) | All stakeholders have approved definitions, pricing decisions are finalized, no ASSUMED items remain |
| **Phase 2: Engineering** | Configured CRM/CPQ system                                              | Products in CRM, approval rules active, output document renders correctly, test quotes pass |
| **Phase 3: Enablement**  | Trained team with documentation                                        | All training delivered, hypercare complete, 10+ live deals processed successfully |
| **Phase 4: Handoff**     | Independent customer + archived project                                | Internal/external handoffs complete, maintenance schedule in place, CPQ expansion path identified |

### How to Adapt Per Project Type

| Project Profile       | Strategy Weight | Engineering Weight | Enablement Weight | Example Projects               |
| --------------------- | --------------- | ------------------ | ----------------- | ------------------------------ |
| **Strategic-heavy**   | 60-80%          | 10-20%             | 10-20%            | Growth Model, GTM Strategy     |
| **Engineering-heavy** | 10-20%          | 60-80%             | 10-20%            | CRM Migration, Data Pipeline   |
| **Enablement-heavy**  | 20-30%          | 20-30%             | 40-50%            | **Pricing &amp; Packaging**, Process Rollout |
| **Balanced**          | 30-40%          | 30-40%             | 20-30%            | Attribution, Lead Scoring      |

P&amp;P is **enablement-heavy**. The hard work is not documenting the pricing architecture (strategy) or configuring the CRM (engineering) — it is getting the sales team to actually follow the new pricing, discount policies, and approval workflows. Budget accordingly.

---

## References

[1] [Pricing Solutions - B2B Discount Authority Study](https://www.getmonetizely.com/articles/pricing-governance-establishing-effective-policies-for-discounts-and-exceptions)
[2] [Experlogix - The 7 Traps of Bad CPQ Implementation](https://www.experlogix.com/blog/cpq-implementation)
[3] [Salesforce - Structured Approval Hierarchies Research](https://www.glencoyne.com/guides/enterprise-discount-approval-matrix)
[4] [OpenView Partners - SaaS Benchmarks: Disciplined Discounting](https://www.getmonetizely.com/articles/discounting-strategy-amp-guardrails-preventing-a-race-to-the-bottom)
[5] [Tacton - CPQ Implementation Readiness](https://www.tacton.com/cpq-blog/cpq-implementation-readiness-8-steps-for-a-successful-transformation/)
[6] [DealHub - Discount Approval Best Practices](https://dealhub.io/blog/revenue-operations/approval-workflows-best-practices/)
[7] [RevOps Co-op - Building a Deal Desk Function in B2B](https://www.revopscoop.com/post/building-a-deal-desk-function-in-b2b)
[8] [Glen Coyne - SaaS Discount Strategy Guardrails](https://www.glencoyne.com/guides/discount-strategy-b2b-saas)
[9] [NetSuite - CPQ Requirements &amp; Implementation Checklist](https://www.netsuite.com/portal/resource/articles/crm/cpq-requirements.shtml)
[10] [Zilliant - Pricing Governance 101](https://zilliant.com/blog/pricing-governance-101-building-guardrails-without-slowing-down-sales)
[11] [Growth Unhinged - State of SaaS Pricing 2025](https://www.growthunhinged.com/p/2025-state-of-saas-pricing-changes)
[12] [Maxio - Guide to SaaS Pricing Models](https://www.maxio.com/blog/guide-to-saas-pricing-models-strategies-and-best-practices)
