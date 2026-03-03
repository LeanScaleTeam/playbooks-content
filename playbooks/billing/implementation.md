# Billing (Q2C) — Implementation

## Project One-Pager

> Quick reference for architects. One per project type. Fill this out FIRST -- it serves as the project's identity card.

### Billing (Q2C) One-Pager

#### Project Type

- Category: Balanced (both strategic and technical)
- Primary Deliverable: Configured billing system with CRM-to-invoice automation, or a documented billing information handoff from CRM/CPQ to the existing billing system

##### Phase Relevance

| Phase          | Applies?  | Weight | Notes                                                                 |
| -------------- | --------- | ------ | --------------------------------------------------------------------- |
| 1. Strategy    | Yes       | Heavy  | Discovery-driven -- must determine GTM motion, billing scope, and tool selection before building anything |
| 2. Engineering | Yes       | Medium | Tool configuration, integration setup, billing workflow automation    |
| 3. Enablement  | Yes       | Medium | Process rollout to Finance, RevOps, and leadership                   |
| 4. Handoff     | Yes       | Standard | Internal + External handoff with maintenance schedule               |

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │    Heavy     │     │   Medium     │     │    Medium    │     │   Standard   │
  │ 1a→1b→1c→1d │     │ 2a→2b→2c→2d │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   Discovery-driven     Tool config          Process rollout      Internal + External
   scope + tool select  integration setup    Finance + RevOps     maintenance schedule
```

**This project's flow:**
- Full 4-phase. Heavy strategy (discovery determines tool selection and scope), medium engineering (billing tool configuration + integration), medium enablement (Finance + RevOps process rollout).
- Strategy phase is heavier than typical because billing has the most variation in outputs, tools, and approaches across customers. Discovery must determine PLG vs Sales-Led vs Hybrid, contract-based vs usage-based, and information handoff vs full system implementation before any build work begins.
- Some customers skip Phase 2 if the scope is "information handoff" only (making sure billing gets the data they need, not implementing a new billing tool).

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Review billing intro video (billing project overview, what Q2C means, why billing accuracy matters)
- [ ] Complete billing intake form: current billing tool(s), invoicing process, pricing model details, payment terms, contract structure
- [ ] Provide billing tool inventory: list of all systems involved in billing (ERP, payment processors, subscription tools, spreadsheets)
- [ ] Document current invoicing process: how does an invoice get generated after a contract is signed? Who is involved? What data flows where?
- [ ] Provide sample contract and corresponding invoice to show current contract-to-invoice translation
- [ ] Get stakeholder sign-off on Definition Alignment Document (billing-specific terms)

##### Track B: Architect Prep
- [ ] Audit current billing workflow: map the contract-to-invoice path, identify manual steps, flag data gaps between CRM and billing
- [ ] Pull CRM contract data to understand deal structures, pricing models, and contract terms in use
- [ ] Identify gaps between CRM/CPQ output and billing system input -- what data is missing or manually re-entered?
- [ ] Research client's billing tool ecosystem (ERP, Stripe, Tabs, Metronome, or other tools in use)
- [ ] Assess GTM motion (PLG, Sales-Led, Hybrid) and map billing implications for each
- [ ] Draft v0 billing assessment: current state, recommended future state, tool recommendation, gap analysis -- all marked ASSUMED
- [ ] Create kickoff presentation with billing workflow diagrams (current vs recommended)

#### Refinement Loop (1b &rarr; 1c &rarr; 1d)

| Meeting                   | Sub-Phase | Focus                                                          | Stakeholder                      | Output                                    |
| ------------------------- | --------- | -------------------------------------------------------------- | -------------------------------- | ----------------------------------------- |
| Kickoff                   | 1b        | Present v0 billing assessment, validate GTM motion and current billing flow | RevOps Lead, Finance Lead        | Feedback for v1, confirmed GTM motion     |
| Billing Process Deep Dive | 1c        | Walk through contract-to-invoice flow step by step, identify every manual handoff and data gap | Finance/Billing Team, RevOps     | Detailed process map, confirmed pain points |
| Tool Selection Review     | 1c        | Present tool recommendation (Tabs/Stripe/Metronome/ERP integration), validate fit | Finance Lead, IT/Engineering     | Approved tool selection, integration scope |
| Integration Design        | 1c        | Map field-level data flow: CRM &rarr; billing tool &rarr; invoice &rarr; ERP/accounting | RevOps, Finance, IT              | Approved integration design               |
| Final Review              | 1d        | Full billing strategy walkthrough, sign-off                    | All stakeholders                 | Signed-off strategic package              |

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held -- GTM motion confirmed, current billing flow validated
- [ ] 1c. Refinement loop complete -- billing process mapped, tool selected, integration designed
- [ ] 1d. Strategic sign-off obtained -- billing approach approved by Finance + RevOps

##### Phase 2: Engineering
- [ ] 2a. Tech spec created -- field mappings (contract &rarr; invoice), workflow triggers, integration specs
- [ ] 2b. Engineering handoff meeting held -- engineer understands billing logic and integration requirements
- [ ] 2c. Build complete -- billing tool configured, integrations connected, invoice templates created
- [ ] 2d. QA/Test + customer sign-off -- test invoices generated from real contracts, billing accuracy verified

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped -- billing process guides, tool walkthroughs, FAQ
- [ ] 3b. Training sessions delivered -- Finance team, RevOps, Leadership
- [ ] 3c. Hypercare period complete -- 4-week billing accuracy monitoring
- [ ] 3d. Enablement sign-off -- team can operate billing independently

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff complete
- [ ] 4c. External handoff (LeanScale &rarr; Customer) complete
- [ ] 4d. Project closed and archived

#### Document Types

##### Working Documents (iterate together)

| Document                          | Purpose                                                      | When Complete                              |
| --------------------------------- | ------------------------------------------------------------ | ------------------------------------------ |
| Billing Intake Form               | Capture current billing tools, process, pricing model        | All fields filled by customer              |
| Current State Billing Process Map  | Document how invoices are generated today, step by step      | Validated by Finance + RevOps in kickoff   |
| Gap Analysis Table                | Identify data gaps between CRM/CPQ and billing system        | Gaps prioritized and assigned              |
| Tool Selection Matrix             | Compare billing tool options against client requirements     | Tool selected and approved                 |
| Integration Design Document       | Map field-level data flow from CRM to billing to accounting  | All field mappings confirmed               |

##### Deliverables (polished outputs)

| Deliverable                       | Created From                        | Customer Uses For                          |
| --------------------------------- | ----------------------------------- | ------------------------------------------ |
| Future State Billing Flow Diagram | Current State Map + Gap Analysis    | Board/leadership presentation, internal alignment |
| Billing System Configuration Doc  | Integration Design + Tech Spec      | Internal reference for Finance/RevOps      |
| Invoice Template(s)               | Integration Design + Customer branding | Actual customer invoicing                  |
| Billing Process Runbook           | All working docs                    | Day-to-day billing operations              |

#### Enablement Details

##### Training Types

| Type        | Audience                           | Focus                                                    | Duration |
| ----------- | ---------------------------------- | -------------------------------------------------------- | -------- |
| Leadership  | CFO, VP Finance, VP RevOps         | Billing strategy rationale, reporting dashboards, KPIs   | 30 min   |
| Operations  | Finance/Billing team               | New billing workflow end-to-end, invoice generation, exception handling | 60 min   |
| Technical   | RevOps Admin, IT                   | System maintenance, integration monitoring, troubleshooting | 45 min   |

##### Hypercare
- Applies: Yes
- Duration: 4 weeks post-go-live
- Office Hours: Weekly 30-min slot for billing questions and issue triage

##### Training Assets to Create
- [ ] Video walkthrough: Billing workflow walkthrough (end-to-end: contract signed &rarr; invoice generated)
- [ ] Video walkthrough: Tool-specific walkthrough (Tabs/Stripe/Metronome -- whichever was implemented)
- [ ] Doc: Field mapping reference (CRM field &rarr; billing field &rarr; invoice field)
- [ ] Doc: Exception handling guide (mid-contract changes, refunds, credits, failed payments)
- [ ] Doc: Monthly billing operations checklist

#### Handoff & Retention

##### Internal Handoff
- Key context for Architect: Which billing tool was implemented, what the GTM motion is (PLG/Sales-Led/Hybrid), which integrations are active, and the key Finance/RevOps contacts
- Escalation trigger: Any billing logic changes, new pricing model introduction, integration failures, or mid-contract amendment handling changes

##### External Handoff (LeanScale &rarr; Customer)
- Final meeting agenda: Review billing workflow, walk through documentation package, confirm no outstanding issues, demonstrate maintenance tasks, record maintenance walkthrough video
- Documentation package: All training recordings, billing process runbook, field mapping reference, exception handling guide, FAQ, maintenance schedule

##### Maintenance Schedule
- Monthly: Invoice accuracy check, failed payment review, billing-to-contract reconciliation
- Quarterly: Full billing process review, integration health check, pricing model alignment
- Who owns: Single project = customer owns | Dedicated = Architect owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services (ongoing billing ops support) &rarr; if no &rarr; Downsell: Adjacent Q2C project (CPQ, RevRec, Pricing & Packaging) &rarr; Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~1 quarter after go-live
- Internal prep trigger: 2 weeks before check-in
- Decision: Architect handles minor billing tweaks / deeper expertise needed for pricing model changes or new integration work

#### Key Assets

| Asset                              | Link       | When Used                          |
| ---------------------------------- | ---------- | ---------------------------------- |
| Billing Intake Form Template       | [link]     | Phase 1a -- Pre-Kickoff             |
| Tool Selection Matrix Template     | [link]     | Phase 1c -- Tool Selection Review   |
| Integration Design Template        | [link]     | Phase 1c -- Integration Design      |
| Invoice Template Library           | [link]     | Phase 2c -- Build                   |
| Billing Process Runbook Template   | [link]     | Phase 3a -- Training Prep           |

#### Definition Alignment Terms

| Term                      | Typical Definition                                                                                                    |
| ------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| Invoice                   | A document sent to a customer requesting payment for goods or services delivered. Contains line items, amounts, payment terms, and due date. |
| Billing Schedule          | The cadence and timing of when invoices are generated and sent -- e.g., monthly on the 1st, quarterly in advance, upon contract milestones. |
| Net Terms (Net-30/60/90)  | The number of days a customer has to pay an invoice after it is issued. Net-30 means payment is due 30 days after invoice date. |
| Revenue Recognition (RevRec) | The accounting principle that determines when revenue is recorded on the books -- typically when the service is delivered, not when cash is received. Governed by ASC 606. |
| Metered Usage             | Billing based on actual product consumption (API calls, storage, seats used, etc.) rather than a fixed subscription fee. Requires a metering layer to track usage events. |
| Subscription Billing      | Recurring billing at a fixed amount on a set schedule (monthly, annually). Predictable for both customer and provider. |
| Usage-Based Billing       | Billing calculated from measured consumption. Variable amount each billing period. Requires usage event tracking and a rating engine. |
| Payment Terms             | The agreed-upon conditions for payment including method (ACH, wire, credit card), timing (Net-30, due on receipt), and currency. |
| Proration                 | Adjusting a bill proportionally when a customer upgrades, downgrades, or cancels mid-billing cycle. |
| Dunning                   | The process of following up on failed or overdue payments -- automated email sequences, payment retries, and escalation to collections. |
| Billing Entity            | The legal entity that issues invoices. Relevant for multi-entity companies billing from different subsidiaries or regions. |
| Contract Value (TCV/ACV)  | Total Contract Value = full contract amount over its term. Annual Contract Value = annualized value. Both feed into billing schedule generation. |
| Credit Memo               | A document that reduces the amount owed by a customer, used for refunds, billing corrections, or negotiated credits. |

#### Common Gotchas

- **Mid-contract changes break billing automation** &rarr; Build amendment handling into the billing workflow from the start. Define a process for upgrades, downgrades, and add-ons that triggers billing schedule updates automatically. Do not assume contracts are static after signing.
- **Multi-currency billing not properly configured** &rarr; If the customer has international customers, validate currency handling during discovery. Currency conversion rates, localized tax calculation, and multi-currency invoice formatting must be scoped explicitly -- not discovered during QA.
- **Usage events not flowing to billing system** &rarr; For usage-based billing, test the metering pipeline end-to-end before building billing logic on top of it. Confirm events are reaching the billing system at the expected volume and latency. A billing system with no usage data produces $0 invoices.
- **Tax calculation integration missed** &rarr; Sales tax / VAT compliance is often treated as "we'll figure it out later." Scope tax requirements in Phase 1. Tools like Avalara or Stripe Tax may need integration. Each jurisdiction has different rules, and SaaS-specific taxation is still evolving.
- **CRM data quality too poor for billing automation** &rarr; Billing automation depends on clean contract data in the CRM. If deal fields are inconsistently filled (missing close dates, wrong amounts, no payment terms), the billing system will generate incorrect invoices. Run a CRM data audit in Phase 1a.
- **Manual billing steps survive the automation project** &rarr; Teams often keep manual workarounds "just in case" alongside the new automated process. This creates dual processes, confusion, and eventually one system falls out of sync. Define a hard cutover date and enforce it.
- **ERP integration scope underestimated** &rarr; ERP integrations (NetSuite, Sage, SAP) are often the longest and most complex part of a billing project. Do not treat ERP integration as a "Phase 2 detail" -- scope it in Phase 1 with IT involvement.
- **Billing disconnected from RevRec** &rarr; Billing and revenue recognition are different processes but tightly coupled. What you bill is not always what you recognize as revenue. If the customer needs RevRec compliance (ASC 606), scope it during discovery -- it may require a separate sub-project or additional tool configuration.
- **Failed payment handling not designed** &rarr; SaaS businesses lose approximately 9% of MRR to failed payments and involuntary churn. Design dunning sequences (retry logic, email notifications, escalation) during the build phase, not after go-live.

#### Methodology Options

| Option                          | When to Use                                                      | Complexity |
| ------------------------------- | ---------------------------------------------------------------- | ---------- |
| Information Handoff             | Client has an existing billing system; gap is in data flow from CRM/CPQ to billing | Low        |
| Contract-Based Billing Setup    | Sales-led motion, standard subscription/contract billing, tools like Tabs or ERP integration | Medium     |
| PLG Self-Serve Billing Setup    | Product-led motion, automated sign-up-to-billing via Stripe or similar | Medium     |
| Usage-Based Billing Setup       | Usage/consumption-based pricing model, requires metering layer (Metronome) | High       |
| Hybrid Billing (PLG + Sales-Led)| Company has both self-serve and sales-led motions requiring separate billing paths | High       |

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on billing approach, tool selection, and integration design.
>
> **Output:** Definition Alignment Document + Billing Strategic Package (billing process map, tool selection, integration design -- signed off by Finance + RevOps).

### 1a. Pre-Kickoff

> Two parallel tracks run after the deal closes and before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                              | Purpose                                                              | Format             |
| --------------------------------- | -------------------------------------------------------------------- | ------------------ |
| Billing intro video               | Explain what the billing project is and why billing accuracy matters | Video (5-10 min)   |
| Definition Alignment Document     | Get stakeholder sign-off on billing terms (invoice, billing schedule, net terms, proration, etc.) | Google Doc         |
| Billing intake form               | Capture current billing tools, invoicing process, pricing model, payment terms, contract structure | Google Form or Doc |
| Billing tool inventory request    | List all systems involved in billing today (ERP, payment processors, subscription tools, spreadsheets) | Simple list        |
| Sample contract + invoice request | Show how a real contract translates to a real invoice today          | PDF/email          |

**Specific intake questions:**
- What billing tool(s) do you use today? (ERP name, Stripe, manual spreadsheet, etc.)
- How is an invoice generated after a contract is signed? Walk us through the steps.
- What is your pricing model? (Flat subscription, usage-based, tiered, per-seat, hybrid)
- What are your standard payment terms? (Net-30, Net-60, due on receipt, etc.)
- Do you have international customers? If so, do you bill in multiple currencies?
- Do you have a self-serve / PLG billing path separate from your sales-led path?
- What ERP or accounting system do you use? (NetSuite, QuickBooks, Sage, SAP, etc.)
- What is your current invoice error rate? How often do billing disputes occur?
- Who is responsible for billing today? (Finance team, RevOps, shared, outsourced)

**Completion tracking:** Follow up within 3 business days. Don't cancel kickoff if incomplete, but push hard -- especially on the billing tool inventory and sample contract/invoice.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                                     | Output                                         |
| ---- | -------------------------------------------------------------------------- | ---------------------------------------------- |
| 1    | Review intake form, billing tool inventory, sample contract/invoice        | Raw data collected                             |
| 2    | Pull CRM deal data: contract values, payment terms, deal structures       | Data for GTM motion assessment                 |
| 3    | Audit current billing workflow: map contract-to-invoice path              | Current state billing process map              |
| 4    | Determine GTM motion (PLG/Sales-Led/Hybrid) from deal patterns            | Motion classification                          |
| 5    | Assess scope: information handoff vs system implementation                | Scope recommendation                           |
| 6    | Research client's existing tools and integration capabilities             | Tool landscape assessment                      |
| 7    | Produce v0 billing assessment                                             | v0 billing assessment (all ASSUMED)            |
| 8    | Create kickoff presentation with billing workflow diagrams                | Kickoff assets                                 |

**v0 output:**
- Current state billing process map (ASSUMED)
- Recommended future state billing process map (ASSUMED)
- Tool recommendation with rationale (ASSUMED)
- Gap analysis: what must change between current and future state (ASSUMED)
- Risk flags: data quality issues, integration complexity, scope concerns

**Critical:** Mark everything as ASSUMED. The kickoff call validates.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on billing terms BEFORE building anything.

| Term                      | Our Definition                                                                                       | Internally Approved? |
| ------------------------- | ---------------------------------------------------------------------------------------------------- | -------------------- |
| Invoice                   | A document sent to a customer requesting payment for goods or services delivered                     | [ ] Yes / [ ] No     |
| Billing Schedule          | The cadence and timing of when invoices are generated and sent                                       | [ ] Yes / [ ] No     |
| Net Terms                 | The number of days a customer has to pay after invoice date (e.g., Net-30 = 30 days)                | [ ] Yes / [ ] No     |
| Revenue Recognition       | When revenue is recorded on the books per ASC 606 (service delivery, not cash receipt)              | [ ] Yes / [ ] No     |
| Metered Usage             | Billing based on actual product consumption rather than a fixed fee                                  | [ ] Yes / [ ] No     |
| Proration                 | Adjusting a bill proportionally for mid-cycle changes (upgrades, downgrades, cancellations)         | [ ] Yes / [ ] No     |
| Dunning                   | The automated process for following up on failed or overdue payments                                 | [ ] Yes / [ ] No     |
| Payment Terms             | Agreed conditions for payment: method (ACH, wire, card), timing, and currency                       | [ ] Yes / [ ] No     |
| Credit Memo               | A document reducing amount owed for refunds, corrections, or negotiated credits                     | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your Finance and RevOps leadership. Check "Yes" when approved. We cannot proceed with tool configuration until billing terms are aligned.

---

### 1b. Kickoff Call

> **Purpose:** Present v0 billing assessment and get alignment on GTM motion, billing scope, and current state. We walk in with work done -- customer reacts, not creates from scratch.

#### Agenda (60-90 min)

| Time  | Topic                              | What Happens                                                                   |
| ----- | ---------------------------------- | ------------------------------------------------------------------------------ |
| 0-15  | Walk through v0 billing assessment | "Here's what we built from your intake -- current billing flow, gaps we see"    |
| 15-25 | Validate GTM motion                | Confirm PLG vs Sales-Led vs Hybrid -- this determines the billing architecture  |
| 25-35 | Confirm billing scope              | Information handoff only, or full billing system implementation?                |
| 35-50 | Review current billing process     | Walk through contract-to-invoice flow, identify manual steps and pain points   |
| 50-60 | Definition alignment               | Review billing terms -- get initial sign-off or identify blockers               |
| 60-70 | Identify gaps                      | What data is missing? What systems need access? Who else needs to be involved? |
| 70+   | Next steps                         | Schedule Billing Process Deep Dive, assign homework                            |

#### What We Bring

- v0 billing assessment (current state, recommended future state, gap analysis)
- Billing workflow diagrams (current state, draft future state)
- Questions list (what we need to validate -- especially around contract structure, pricing model, and existing tool capabilities)
- Definition Alignment Document (pre-filled with our recommended definitions)
- Tool context: initial assessment of which billing tool(s) may fit

#### What We Leave With

- Confirmed GTM motion (PLG / Sales-Led / Hybrid)
- Confirmed scope (information handoff vs system implementation)
- Corrections and feedback on v0 (info needed to produce v1)
- Validated or corrected billing process understanding
- Homework assigned: system access, stakeholder introductions (Finance/Billing team for Deep Dive), Definition Alignment Document completion
- Billing Process Deep Dive scheduled

---

### 1c. Alignment Loop &amp; Strategic Meeting Cadence

> **Purpose:** Iterate on the billing strategic package until sign-off.

#### The Pattern

```
Kickoff Call (validate GTM motion, scope, current state)
    ↓
Process kickoff feedback → v1
    ↓
Meeting 2: Billing Process Deep Dive (detailed process walk-through with Finance)
    → process feedback → v2 (detailed process map + edge cases)
    ↓
Meeting 3: Tool Selection Review (present recommendation, validate fit)
    → v3 (confirmed tool + integration scope)
    ↓
Meeting 4: Integration Design (field-level mapping, workflow triggers)
    → v4 (integration design doc)
    ↓
Meeting 5: Final Review → Sign-off
```

#### Before Each Meeting

1. Process previous meeting transcript/notes
2. Update billing assessment (v\[n-1\] &rarr; v\[n\])
3. Prepare questions for next validation round
4. Update process maps and gap analysis

#### During Each Meeting

1. Walk through current version of the billing assessment
2. Capture corrections and refinements
3. Validate what's now CONFIRMED (vs ASSUMED)
4. Identify remaining unknowns

#### After Each Meeting

1. Update billing assessment
2. Track what moved from ASSUMED &rarr; CONFIRMED
3. Update working documents (process map, gap analysis, tool selection matrix)

#### Billing-Specific Meeting Types

| Meeting Type                | Focus                                                                 | Stakeholder                    |
| --------------------------- | --------------------------------------------------------------------- | ------------------------------ |
| Kickoff                     | GTM motion, billing scope, current state overview                     | RevOps Lead, Finance Lead      |
| Billing Process Deep Dive   | Step-by-step contract-to-invoice walk-through, edge cases, exceptions | Finance/Billing Team, RevOps   |
| Tool Selection Review       | Tool recommendation, capabilities vs requirements, integration scope  | Finance Lead, IT/Engineering   |
| Integration Design          | Field-level data mapping, workflow triggers, invoice templates         | RevOps, Finance, IT            |
| Final Review                | Full strategic package walkthrough, sign-off                          | All stakeholders               |

#### Typical Timeline

| Milestone                      | Timing                                                       |
| ------------------------------ | ------------------------------------------------------------ |
| Pre-kickoff prep               | 3-5 days                                                     |
| Kickoff call                   | Day 1 of engagement                                          |
| Billing Process Deep Dive      | Week 1-2                                                     |
| Tool Selection Review          | Week 2-3                                                     |
| Integration Design             | Week 3-4                                                     |
| Final Review + Sign-off        | Week 4-5 (when all inputs CONFIRMED)                         |

**Note:** Billing projects are discovery-heavy. Expect the strategy phase to take longer than other project types because every customer's billing situation is different.

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything before proceeding to engineering.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by Finance and RevOps stakeholders
- [ ] GTM motion confirmed (PLG / Sales-Led / Hybrid) and billing path defined for each motion
- [ ] Current state billing process fully documented and validated
- [ ] Future state billing process approved
- [ ] Tool selection confirmed (Tabs, Stripe, Metronome, ERP integration, or combination)
- [ ] Integration design reviewed and approved (field mappings, triggers, data flow)
- [ ] Gap analysis reviewed and accepted -- all gaps have an owner and a plan
- [ ] Billing edge cases documented (mid-contract changes, refunds, credits, multi-currency)
- [ ] Tax and compliance requirements scoped (or explicitly out of scope)
- [ ] All critical inputs CONFIRMED (vs ASSUMED)
- [ ] Customer understands what we're building and the expected timeline
- [ ] No blockers for engineering

#### Decision Point

- **Proceed to Engineering** &rarr; Customer wants billing system configured/integrated
- **Project complete at Phase 1** &rarr; Scope was "information handoff" only -- strategic deliverable (billing process documentation + integration requirements) is the end product. Customer's internal team or another vendor implements.

**Note:** If the scope is "information handoff" (making sure billing gets the data they need from CRM/CPQ), the project may complete after Phase 1 with a documented billing process and integration requirements. If the scope is "system implementation," proceed to Phase 2.

---

## Phase 2: Engineering

> **Goal:** Configure the billing system, build integrations, and test that invoices are generated accurately from contract data.
>
> **Output:** Configured billing tool with CRM-to-invoice automation, tested and customer-approved.

| Project Scope              | Engineering Weight | Example                                                    |
| -------------------------- | ------------------ | ---------------------------------------------------------- |
| Information handoff only   | Light (10-20%)     | Document data requirements, map fields, no system build    |
| Single-tool configuration  | Medium (40-50%)    | Configure Tabs or Stripe, build CRM integration            |
| Multi-tool + ERP integration | Heavy (60-70%)   | Billing tool + metering + ERP integration + payment processor |

### Sub-Phases

```
2a Tech Spec → 2b Engineering Handoff → 2c Build → 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate billing strategic package into technical specifications.

**Input:** Signed-off strategic package from Phase 1 (billing process map, tool selection, integration design, field mappings)

**Output:** Draft tech spec containing:

- **Field mappings:** CRM contract fields &rarr; billing tool fields &rarr; invoice line items (e.g., CRM "Contract Value" &rarr; Tabs "Total Contract Amount" &rarr; Invoice "Subtotal")
- **Workflow triggers:** What event initiates billing? (e.g., Salesforce Opportunity.Stage = "Closed Won" triggers billing schedule creation in Tabs)
- **Billing schedule logic:** How are billing schedules generated? (Monthly on contract start date, quarterly in advance, milestone-based, usage-based rating)
- **Integration specs:** API connections, data sync frequency, error handling, retry logic
- **Invoice template specs:** Required fields, branding, format, delivery method (email, portal, API)
- **Payment processing specs:** Payment methods accepted, dunning sequence, retry schedule
- **Tax calculation specs:** Tax engine integration (Avalara, Stripe Tax), jurisdiction rules
- **Build sequence:** What to configure first (product catalog &rarr; pricing &rarr; billing schedules &rarr; integrations &rarr; invoice templates &rarr; payment processing &rarr; dunning)

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs with engineer before building.

**Who attends:** Architect + Engineer (or engineering team)

**Agenda (30-45 min):**

| Time  | Topic                        | What Happens                                                         |
| ----- | ---------------------------- | -------------------------------------------------------------------- |
| 0-15  | Walk through billing specs   | Architect explains billing strategy context + tech spec                    |
| 15-25 | Integration complexity review | Discuss CRM/ERP integration approach, API capabilities, data volume |
| 25-35 | Risk identification          | Flag: data quality issues, API limitations, multi-currency, tax      |
| 35-45 | Build plan approval          | Confirm build sequence, timeline, and who builds what                |

**What Architect brings:**

- Strategic package (billing process maps, tool selection rationale)
- Draft tech spec (from 2a)
- Integration design document
- Questions list (anything flagged as unclear -- e.g., custom contract terms that don't map to standard billing fields)

**What engineer leaves with:**

- Approved tech spec with field-level detail
- Clear build sequence
- Known risks/dependencies (especially ERP integration timelines)
- Access credentials to billing tool and CRM sandbox/test environment

---

### 2c. Build (Configure)

> **Purpose:** Configure the billing system and build integrations.

**Input:** Approved tech spec from 2b

**Build components for billing:**

| Component                     | What Gets Built                                                              | Tool              |
| ----------------------------- | ---------------------------------------------------------------------------- | ----------------- |
| Product catalog               | Create products, pricing tiers, billing frequencies in billing tool          | Tabs/Stripe/etc.  |
| Billing schedule configuration | Set up billing rules: cadence, proration, ramp schedules, minimum commits  | Tabs/Stripe/etc.  |
| CRM-to-billing integration    | Connect CRM contract data to billing tool via API or native integration      | Integration layer |
| Invoice templates             | Create branded invoice templates with required fields                         | Billing tool      |
| Payment processing            | Configure payment methods, auto-charge, manual invoice delivery              | Stripe/processor  |
| Dunning workflows             | Set up failed payment retry logic, notification emails, escalation           | Billing tool      |
| Usage metering (if applicable)| Configure event ingestion, rating rules, usage-to-invoice mapping            | Metronome         |
| ERP sync (if applicable)      | Connect billing tool to ERP for invoice and payment data sync                | Integration layer |
| Tax integration (if applicable)| Connect tax calculation engine for automated tax on invoices                 | Avalara/Stripe Tax|

**Execution approaches:**

| Approach       | When to Use                                                                 | Example                                   |
| -------------- | --------------------------------------------------------------------------- | ----------------------------------------- |
| Manual build   | First implementation of this billing tool, complex contract structures      | Engineer configures Tabs directly          |
| Template-based | Standard setup, well-defined field mappings                                 | Template-based configuration, engineer reviews |
| Automated      | Repeat implementations with same tool, established patterns                 | Fully automated configuration              |

**Build tracking:**

- [ ] Product catalog configured
- [ ] Billing schedules created for each pricing model
- [ ] CRM-to-billing integration connected and syncing
- [ ] Invoice template(s) created and branded
- [ ] Payment processing configured
- [ ] Dunning workflows set up
- [ ] Usage metering connected (if applicable)
- [ ] ERP sync configured (if applicable)
- [ ] Tax calculation integrated (if applicable)

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify billing accuracy and get customer approval.

**Two types of testing:**

| Type                  | Who      | Purpose                                                          |
| --------------------- | -------- | ---------------------------------------------------------------- |
| Technical Testing     | Our team | Verify integrations work, data flows correctly, invoices generate |
| Customer Testing      | Customer | Verify invoices are accurate and match contract terms            |

**Technical testing checklist:**

- [ ] CRM contract data syncs to billing tool correctly (all mapped fields present)
- [ ] Billing schedules generated from contract data match expected cadence and amounts
- [ ] Invoice line items match contract terms (amount, description, quantity, pricing)
- [ ] Invoice totals are correct (subtotal + tax = total)
- [ ] Tax calculation returns correct rates for customer jurisdiction
- [ ] Payment processing works (test charge, test refund)
- [ ] Dunning workflow triggers on failed payment (test with declined card)
- [ ] Usage events flow to billing system and rate correctly (if usage-based)
- [ ] ERP sync pushes invoice and payment data correctly (if applicable)
- [ ] Mid-contract change scenario: upgrade/downgrade generates correct prorated invoice
- [ ] Multi-currency invoices display correct currency and conversion (if applicable)
- [ ] Edge case: annual contract with monthly billing generates 12 correct invoices
- [ ] Edge case: contract with ramp schedule generates correct amounts per period

**Customer testing:**

- Walk Finance team through 3-5 test invoices generated from real contract data
- Have them compare test invoices to what they would have generated manually
- Test the full flow: contract signed &rarr; billing schedule created &rarr; invoice generated &rarr; payment collected
- Capture feedback, fix any discrepancies

**Engineering sign-off checkpoint:**

- [ ] All billing configurations match tech spec
- [ ] All technical tests passing
- [ ] Test invoices reviewed and approved by Finance team
- [ ] Invoice accuracy rate: 100% on test set (no tolerance for billing errors)
- [ ] Integration monitoring in place (alerts for sync failures)
- [ ] Ready for enablement

**Decision point:**

- **Proceed to Enablement** &rarr; Billing system is configured, invoices are accurate, needs training/rollout
- **Loop back to Build** &rarr; Invoice discrepancies found, integration issues, needs fixes

---

## Phase 3: Enablement

> **Goal:** Finance team and RevOps can operate the billing system independently.
>
> **Output:** Trained team with documentation, stabilized billing system, no billing errors in production.

### Sub-Phases

```
3a Training Prep → 3b Training Sessions → 3c Hypercare → 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create billing-specific training materials from strategic and technical documentation.

**Input:** Strategic package + tech specs + configured billing system

**Output:** Training package containing:

- **Video walkthrough scripts:**
  - "End-to-End Billing Workflow" -- contract signed &rarr; billing schedule &rarr; invoice &rarr; payment &rarr; reconciliation
  - "Billing Tool Walkthrough" -- navigating Tabs/Stripe/Metronome (whichever was implemented)
  - "Handling Billing Exceptions" -- mid-contract changes, refunds, credits, failed payments
  - "Monthly Billing Operations" -- what to check, when to check it, what to escalate
- **Written guides:**
  - Field mapping reference (CRM field &rarr; billing field &rarr; invoice field)
  - Exception handling playbook (upgrade/downgrade, refund, credit memo, cancellation)
  - Billing operations checklist (daily/weekly/monthly tasks)
  - Integration monitoring guide (what to watch, what alerts mean, how to troubleshoot)
- **FAQ draft:**
  - "Why does this invoice amount not match the CRM deal amount?" (proration, tax, credits)
  - "What happens when a payment fails?" (dunning sequence explanation)
  - "How do I handle a mid-contract pricing change?" (amendment workflow)
  - "Where do I see billing data in the CRM?" (field locations and meanings)
  - "How do I generate a credit memo?" (step-by-step)

---

### 3b. Training Sessions

> **Purpose:** Transfer billing knowledge to customer team.

**Training sessions by stakeholder:**

| Session           | Audience                       | Focus                                                                          | Duration |
| ----------------- | ------------------------------ | ------------------------------------------------------------------------------ | -------- |
| Finance/Billing   | Billing team, AR team          | Full billing workflow: invoice generation, payment tracking, exception handling, dunning | 60 min   |
| RevOps/Admin      | RevOps team, system admin      | System maintenance: integration monitoring, field mapping changes, troubleshooting, adding new products/pricing | 45 min   |
| Leadership        | CFO, VP Finance, VP RevOps     | Billing KPIs: invoice accuracy rate, DSO, failed payment rate, billing lag. Dashboard walkthrough. | 30 min   |

**Training delivery:**

1. Schedule sessions with appropriate stakeholders (Finance first, then RevOps, then Leadership)
2. Deliver training live with screen sharing -- walk through actual billing system with real (or realistic) data
3. Record every session as a video walkthrough for future reference
4. Run a "billing scenario" exercise: give Finance team a test contract and have them generate an invoice using the new system
5. Answer questions, note gaps for FAQ updates

**Output:**

- Trained Finance team that can generate and manage invoices
- Trained RevOps team that can maintain and troubleshoot the billing system
- Informed leadership with KPI dashboards
- Video recordings for each session
- Updated FAQ with questions raised during training

---

### 3c. Hypercare

> **Purpose:** Intensive post-launch support to catch and fix billing issues before they reach customers.

**Duration:** 4 weeks

**What happens during hypercare:**

- **Week 1:** Daily monitoring of all invoices generated. Compare every invoice against contract terms. Fix any discrepancies immediately.
- **Week 2:** Shift to every-other-day monitoring. Focus on edge cases (mid-contract changes, new customers, unusual pricing).
- **Week 3-4:** Weekly monitoring. Office hours for questions. Focus on exception handling and team confidence.

**Weekly office hours:** 30-minute slot, open to Finance and RevOps. Bring questions, issues, or scenarios they're unsure about.

**Hypercare metrics to track:**

| Metric                  | Target              | Red Flag                              |
| ----------------------- | ------------------- | ------------------------------------- |
| Invoice accuracy rate   | 100%                | Any invoice error                     |
| Billing lag             | &lt; 24 hours          | Invoice generated &gt; 48 hours after trigger |
| Failed payment rate     | &lt; 5%                | &gt; 10% failed payments                 |
| Manual intervention rate| &lt; 10% of invoices   | &gt; 25% require manual correction       |
| Support tickets (billing)| Decreasing weekly  | Increasing week-over-week             |

**When to skip:** If the project scope was "information handoff" only (Phase 1 completion), hypercare may not apply. If a billing system was configured, hypercare is required.

**Output:** Stabilized billing system, no critical billing errors, team operating independently

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm customer can operate billing independently.

**Validation checkpoint:**

- [ ] All training sessions delivered (Finance, RevOps, Leadership)
- [ ] Training video recordings and documentation provided
- [ ] Hypercare period complete -- 4 weeks of billing accuracy monitoring
- [ ] No critical billing errors in the last 2 weeks of hypercare
- [ ] Finance team has independently generated invoices without LeanScale assistance
- [ ] RevOps team has independently resolved a billing system issue (integration error, field mapping change, etc.)
- [ ] FAQ document complete and distributed
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** &rarr; Team is enabled, billing system stable, no critical issues
- **Extend Hypercare** &rarr; Billing errors still occurring, team not yet confident, more support needed

---

## Phase 4: Handoff

> **Goal:** Clean project close with billing maintenance plan established and retention/expansion path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the billing system, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule → 4b Internal Handoff → 4c External Handoff → 4d Project Close
                                                  (LeanScale → Customer)   (Archive + Debrief)
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At                                                                |
| ----------------------------- | -------------------- | ---------------------------------------------------------------------------- |
| **Single Project**            | Customer owns        | 4c (External Handoff) -- customer receives maintenance schedule and runs it   |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) -- Architect receives maintenance schedule and runs it  |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention to keep the billing system accurate and current.

#### Standard Billing Maintenance Framework

**Monthly Tasks:**

| Monthly Task                       | What to Check                                                        | Red Flag Threshold                          |
| ---------------------------------- | -------------------------------------------------------------------- | ------------------------------------------- |
| Invoice accuracy reconciliation    | Compare invoices generated vs active contracts -- do amounts match?   | Any discrepancy &gt; $100 or &gt; 1% of invoice total |
| Failed payment review              | Review all failed payments, confirm dunning sequences fired correctly | Failed payment rate &gt; 10%                   |
| Billing-to-contract reconciliation | Confirm all active contracts have corresponding billing schedules    | Any contract missing a billing schedule     |
| New customer billing validation    | Spot-check invoices for customers added this month                   | Invoice errors on new customers             |
| Integration health check           | Confirm CRM-to-billing sync is running, check error logs             | Any sync failures in the last 7 days        |

**Quarterly Tasks:**

| Quarterly Task                   | What to Review                                                      | Action if Off-Track                                |
| -------------------------------- | ------------------------------------------------------------------- | -------------------------------------------------- |
| Full billing process review      | Walk through the billing workflow end-to-end -- any manual workarounds appearing? | Document workarounds, decide if automation needed |
| Pricing model alignment          | Have pricing/packaging changed? Do billing schedules reflect current pricing? | Update billing tool product catalog and pricing    |
| Integration performance review   | Sync speed, error rates, data accuracy trends over the quarter      | Escalate persistent integration issues             |
| Dunning effectiveness review     | Are dunning sequences recovering failed payments? What's the recovery rate? | Adjust retry timing, add manual outreach step      |
| Tax rate validation              | Are tax rates current for all jurisdictions? Any regulatory changes? | Update tax engine configuration                    |

**After First Business Cycle (30-60 days post-launch):**

- **Invoice accuracy audit:** Pull all invoices generated since go-live. Compare against contracts. Calculate invoice accuracy rate. Target: &gt;99%.
- **DSO measurement:** Compare Days Sales Outstanding before and after billing system implementation. If DSO increased, investigate payment processing or dunning issues.
- **Customer feedback check:** Have any customers raised billing disputes or questions about new invoice format? If so, adjust invoice template or communication.

**Refinement Triggers (when to re-engage):**

| Trigger                              | Threshold                        | Response                                                         |
| ------------------------------------ | -------------------------------- | ---------------------------------------------------------------- |
| Invoice error rate                   | &gt; 2% of invoices have errors    | Audit billing configuration                                     |
| Failed payment rate                  | &gt; 10% for 2+ consecutive months | Review dunning sequences, payment processing setup               |
| New pricing model introduced         | Any new pricing structure        | Scope billing update project -- may need new billing schedules    |
| CRM-to-billing sync failures         | &gt; 5 failures per month           | Investigate integration                                          |
| Mid-contract amendment volume spikes | &gt; 20% of contracts amended/month | Review amendment handling workflow, may need automation           |

**Every 6-12 Months:**

- **Full billing system review:** Audit entire billing configuration against current business reality. Products, pricing, billing schedules, integrations.
- **Tool evaluation:** Is the billing tool still the right fit? Has the business outgrown it? New tools available? (Check against latest tool landscape.)
- **Process optimization:** Identify remaining manual steps and evaluate automation opportunities.

---

### 4b. Internal Handoff

> **Purpose:** Transfer billing context so Architect can manage ongoing relationship.

**What the Architect needs to know:**

- Which billing tool was implemented and why (Tabs for contract-based, Stripe for PLG, Metronome for usage, etc.)
- GTM motion: PLG, Sales-Led, or Hybrid -- and which billing path applies to each
- Integration architecture: what connects to what (CRM &rarr; billing &rarr; ERP &rarr; accounting)
- Key Finance/RevOps contacts and their roles in billing operations
- Known edge cases and how they're handled (mid-contract changes, multi-currency, etc.)
- Common issues and resolution steps (integration sync failures, invoice template changes)
- **Maintenance schedule** (if Dedicated engagement -- Architect runs this)

**Billing-specific escalation guidelines:**

| Issue Type                                    | Who Handles              | Examples                                             |
| --------------------------------------------- | ------------------------ | ---------------------------------------------------- |
| Invoice template changes, minor field updates | Architect                | Update company address, add a field to invoice        |
| New product/pricing added to billing tool     | Architect (if simple)    | Simple tier addition vs complex usage-based pricing   |
| Billing logic changes                         | Escalate to specialist   | New billing schedule type, proration rule changes     |
| Integration failures                          | Escalate to specialist   | CRM-to-billing sync broken, API changes              |
| New pricing model support                     | Scope new project        | Company introduces usage-based pricing alongside subscription |
| Multi-entity or multi-currency additions      | Scope new project        | Company expands internationally, needs new billing entity |

---

### 4c. External Handoff (LeanScale &rarr; Customer)

> **Purpose:** Formal billing project completion with customer.

**Final project meeting:**

- Review what was delivered: billing system configuration, integrations, invoice templates, process documentation
- Walk through documentation package (see below)
- Walk through maintenance schedule in detail -- what to check, how often, when to call us
- Have Finance team demonstrate they can generate an invoice independently (live during meeting)
- Answer final questions
- Make it explicit: "Billing project complete"
- **For Single Project engagements:** Hand over the maintenance schedule and walk the customer through it in detail. Record a video walkthrough.

**Documentation package:**

- All training video recordings (billing workflow, tool walkthrough, exception handling, monthly operations)
- Billing process runbook (end-to-end billing operations guide)
- Field mapping reference (CRM &rarr; billing &rarr; invoice &rarr; ERP)
- Exception handling guide (amendments, refunds, credits, failed payments)
- Definition Alignment Document (final version with all terms CONFIRMED)
- FAQ document
- Integration architecture diagram
- Maintenance schedule
- Support contact info and escalation path

**Output:** Customer owns the billing system. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location (strategic package, tech specs, process maps, training materials)
- [ ] Handoff documentation complete
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell &rarr; Downsell &rarr; Retry    |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (ongoing billing ops + monitoring)
   ↓ if no
2. Downsell: Adjacent Q2C project (CPQ implementation, RevRec setup, Pricing & Packaging)
   ↓ if yes
3. Retry retainer at end of next project cycle
```

**Script:**

> "Now that your billing system is live, there are two ways we can continue. Option 1: We handle ongoing billing operations -- monitoring invoice accuracy, managing integration health, handling pricing changes as they come up. Option 2: If there's an adjacent project you need -- like CPQ configuration, revenue recognition setup, or pricing and packaging strategy -- we can scope that out. Which sounds more relevant?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On \[date ~1 quarter after go-live\], we'll review how the billing system is performing -- invoice accuracy, payment success rates, any integration issues -- and see if any adjustments are needed."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                                              |
| ------------------- | ------------------------------------------------------------------------- |
| 1. Get pinged       | System reminder: billing refinement check-in in 2 weeks                  |
| 2. Review metrics   | Pull billing KPIs: invoice accuracy rate, DSO, failed payment rate       |
| 3. Decide ownership | Can Architect handle this check-in, or need specialist?                  |
| 4. Prep materials   | If specialist needed, brief them. If Architect, prep talking points.     |

**At the refinement check-in:**

- Review billing performance against original goals (invoice accuracy, DSO improvement, automation rate)
- Identify any adjustments needed (new products, pricing changes, integration issues)
- If minor: Architect handles tweaks (invoice template update, new product addition)
- If major: Scope new project (new pricing model, international expansion, RevRec implementation)

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables &amp; Assets Summary

**Strategic Deliverables:**

- Billing process documentation (current state + future state process maps)
- Definition Alignment Document (all billing terms confirmed)
- Tool selection rationale (why this tool for this customer)
- Integration design document (field mappings, triggers, data flow architecture)
- Gap analysis (what changed between current and future state)

**Technical Deliverables (Phase 2):**

- Configured billing tool (products, pricing, billing schedules)
- CRM-to-billing integration (tested and operational)
- Invoice template(s) (branded, with all required fields)
- Payment processing configuration (payment methods, auto-charge, dunning)
- Usage metering configuration (if applicable -- Metronome or equivalent)
- ERP sync (if applicable -- NetSuite, Sage, SAP integration)
- Tax calculation integration (if applicable -- Avalara, Stripe Tax)

**Documentation Package:**

- Training video recordings (billing workflow, tool walkthrough, exception handling, monthly ops)
- Billing process runbook
- Field mapping reference
- Exception handling guide
- FAQ document
- Definition Alignment Document (final version)
- Maintenance schedule
- Integration architecture diagram

---

## Appendix

### What This Document Is

This is the implementation playbook -- the step-by-step execution guide an Architect follows to deliver a Billing (Q2C) project from first contact to project close. It follows the 4-phase framework: Strategy, Engineering, Enablement, Handoff.

### What Each Phase Produces

| Phase                    | Output                                                                 | Gate Criteria                                                                  |
| ------------------------ | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **Phase 1: Strategy**    | Signed-off strategic package (Definition Alignment Doc + deliverables) | Customer stakeholders have approved definitions and strategic asset            |
| **Phase 2: Engineering** | Built and tested system                                                | System matches tech spec, all tests pass, customer has approved                |
| **Phase 3: Enablement**  | Trained team with documentation                                        | All training delivered, hypercare complete, team can operate independently     |
| **Phase 4: Handoff**     | Independent customer + archived project                                | Internal/external handoffs complete, maintenance plan in place, project closed |

### How to Adapt Per Project Type

Not every project weighs each phase equally. Before starting, determine your project's profile:

| Project Profile       | Strategy Weight | Engineering Weight | Enablement Weight | Example Projects               |
| --------------------- | --------------- | ------------------ | ----------------- | ------------------------------ |
| **Strategic-heavy**   | 60-80%          | 10-20%             | 10-20%            | Growth Model, GTM Strategy     |
| **Engineering-heavy** | 10-20%          | 60-80%             | 10-20%            | CRM Migration, Data Pipeline   |
| **Enablement-heavy**  | 20-30%          | 20-30%             | 40-50%            | Quote-to-Cash, Process Rollout |
| **Balanced**          | 30-40%          | 30-40%             | 20-30%            | Attribution, Lead Scoring      |

**Adaptation rules:**

- **Light phases** can compress sub-phases (e.g., a strategic-only project may skip Phase 2 entirely)
- **Heavy phases** expand with more sub-steps, more meetings, more iterations
- **Phase 4 always applies** -- every project needs handoff, but the maintenance schedule complexity varies
- Mark phases as \[SKIP\] or \[LIGHT\] in the One-Pager if they don't fully apply

---

## References

[1] [Emersion - Mastering Multi-currency Billing and International Tax Compliance](https://www.emersion.com/blog/saas-billing/the-global-saas-conundrum-mastering-multi-currency-billing-and-international-tax-compliance/)
[2] [Commenda - 10 Best Sales Tax Software for SaaS Companies](https://www.commenda.io/sales-tax/10-best-sales-tax-software-for-saas-businesses/)
[3] [Kaplan Group - 55 SaaS and B2B Payment Statistics for 2025](https://www.kaplancollectionagency.com/news/subscription-facts-55-saas-and-b2b-payment-statistics-for-2025/)
