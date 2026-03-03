# Growth Model — Implementation

> The end-to-end process for delivering Growth Model projects. Follows the 4-phase framework: Strategy, Engineering, Enablement, Handoff.

---

## 1. Project One-Pager

> Quick reference. Scan in 2 minutes to understand the project type, flow, and tools.

### Project Type

- Category: Strategic
- Primary Deliverable: Integrated Growth Model (YAML + micro app + PDF export)

#### Phase Relevance

| Phase          | Applies?  |
| -------------- | --------- |
| 1. Strategy    | Yes       |
| 2. Engineering | Optional  |
| 3. Enablement  | Yes       |
| 4. Handoff     | Yes       |

### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │    Heavy     │     │   Optional   │     │    Medium    │     │    Medium    │
  │ 1a→1b→1c→1d │     │ 2a→2b→2c→2d │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   7 meetings           Dashboard config     5 training groups    Maintenance +
   ~70% of hours        (skip if no)         30-day hypercare     retention path
```

**This project's flow:**
- Full 4-phase for customers who want operational tracking dashboards
- Strategy-only exit available after Phase 1 -- the Growth Model itself IS the deliverable
- Phase 2 is skipped entirely for strategy-only engagements
- ~15 hours with AI-first approach (down from 30-60 hours traditional)

### Phase Checklists

#### Phase 1: Strategy
- 1a. Pre-Kickoff complete (customer homework + prep, v0 built)
- 1b. Kickoff call held (v0 presented, assumptions validated)
- 1c. Refinement loop complete (v0 -> v6, all inputs CONFIRMED)
- 1d. Strategic sign-off obtained (all stakeholders, totals tie)

#### Phase 2: Engineering (Optional)
- 2a. Tech spec created -- Growth Model metrics mapped to dashboard config
- 2b. Engineering handoff meeting held
- 2c. Build complete (dashboards, quota tracking, alerts)
- 2d. QA/Test + customer sign-off

#### Phase 3: Enablement
- 3a. Training materials prepped (video walkthroughs, written guides, FAQ)
- 3b. Training sessions delivered (5 stakeholder groups)
- 3c. Hypercare period complete (30 days)
- 3d. Enablement sign-off

#### Phase 4: Handoff
- 4a. Maintenance schedule documented and handed off
- 4b. Internal handoff complete
- 4c. External handoff complete
- 4d. Project closed and archived

### Document Types

#### Working Documents (iterate together)

| Document                     | Purpose                                         | When Complete                        |
| ---------------------------- | ----------------------------------------------- | ------------------------------------ |
| Intake Form                  | Pre-kickoff data collection from customer        | All fields filled, CRM access given  |
| Input Bank                   | Exhaustive list of ALL model inputs              | All inputs CONFIRMED or documented   |
| Definition Alignment Doc     | Stakeholder sign-off on ARR, Booking, Churn, SQL | All terms approved by Finance        |
| Assumptions Register         | Track data-backed vs strategic assumptions       | All assumptions categorized + owned  |

#### Deliverables (polished outputs)

| Deliverable                  | Created From                | Customer Uses For                               |
| ---------------------------- | --------------------------- | ----------------------------------------------- |
| Growth Model (YAML + PDF)    | Input Bank + agent outputs  | Board presentations, planning, hiring decisions |
| Definitions Document         | Definition Alignment Doc    | Cross-functional source of truth                |
| Assumptions Register (final) | Working assumptions register| Ongoing monitoring and plan adjustment           |
| Micro App Dashboard          | YAML model                  | Interactive exploration, what-if scenarios        |

### Enablement Details

#### Training Types

| Type             | Audience                           | Focus                                                    | Duration |
| ---------------- | ---------------------------------- | -------------------------------------------------------- | -------- |
| RevOps Manager   | RevOps lead                        | Full model walkthrough, monthly actuals entry, scenarios  | 60m      |
| Sales Leadership | CRO/VP Sales                       | Capacity model, quarterly projections, hiring triggers    | 45m      |
| Marketing        | CMO/VP Marketing                   | SQL targets, pipeline offset, budget-to-pipeline ratios   | 45m      |
| CS Leadership    | VP CS                              | Carry ratios, hiring triggers, net retention impact       | 30m      |
| Finance          | CFO/FP&A                           | Definitions, GTM costs, board reporting views             | 30m      |

#### Hypercare
- Duration: 30 days
- Office Hours: One check-in call + async Q&A
- Scope: One model adjustment if material change occurs (e.g., hiring freeze, target change)

### Handoff & Retention

#### Maintenance Schedule
- Monthly: Actual vs Plan tracking, assumption pulse check, hiring status update
- Quarterly: Full assumption review, CSM capacity reforecast, channel efficiency analysis
- Annually: Full model recalibration, segment mix review

#### Retention/Expansion Path

**If Single Project:**
Upsell to Managed Services -> if no -> Another project (Attribution, Lead Scoring) -> Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~1 quarter after handoff
- Decision: minor tweaks handled in-house / structural changes scoped as new engagement

### Definition Alignment Terms

| Term             | Typical Definition                                                                       |
| ---------------- | ---------------------------------------------------------------------------------------- |
| ARR              | Annualized recurring revenue. Excludes one-time fees, professional services, hardware    |
| Booking          | Contract value recognized at signature. Multi-year: total contract or first-year only?   |
| Churn            | Revenue lost from cancellations and downgrades. Distinguish logo churn vs revenue churn  |
| Net Retention    | (Starting ARR + Expansion - Contraction - Churn) / Starting ARR. Target: 100-120%       |
| SQL              | Sales Qualified Lead. Criteria: budget, authority, need, timeline confirmed              |
| Conversion Rate  | Stage-to-stage progression. Must agree on stage definitions before calculating           |
| Pipeline         | Total value of open opportunities at a given stage. Must agree on which stages count     |
| Sales Cycle      | Days from SQL creation to Closed-Won. Varies dramatically by segment                    |
| Quota            | Expected bookings per rep per year. Use expected (attainment-adjusted), not assigned     |
| Ramp Time        | Hire date to full productivity. Includes training + pipeline build + first close cycle   |

### Common Gotchas
- Ramp time assumed too short -> Hire produces less than modeled, capacity gap appears mid-year. Always validate: ramp >= sales cycle length.
- Attrition not factored -> Plan assumes zero turnover. Add 1 buffer hire per 3-4 planned hires (35% avg B2B sales attrition).
- Pipeline timing mismatch -> Q1 bookings fed by Q1 pipeline creation. Pipeline must be built ONE SALES CYCLE before target bookings period.
- Seasonality assumed linear -> 25/25/25/25 quarterly split when reality is 15/20/25/40. Pull historical quarterly patterns.
- Single efficiency ratio across channels -> SDR produces $20 pipeline per $1, Content produces $40. Calculate per-channel.
- CSM capacity on one dimension only -> Use both ARR carry AND logo carry. Binding constraint = whichever is higher.
- Dirty CRM data used as-is -> First 1-2 meetings often spent on data quality. Filter out reseller/PO deals, validate stage definitions.
- Definitions not aligned before modeling -> "Booking" means different things to Sales vs Finance. Force alignment FIRST via Definition Alignment Doc.
- Fiscal year mismatch -> Customer's fiscal year starts May, model starts January. Confirm fiscal year in kickoff.
- New/expansion deals blended -> Separate new business from expansion. Different conversion rates, different capacity owners.

### Methodology Options

| Option      | When to Use                                                    | Complexity |
| ----------- | -------------------------------------------------------------- | ---------- |
| Top-Down    | Board has set firm targets; limited time (&lt;2 weeks)            | Low        |
| Bottom-Up   | Strong historical data; team buy-in critical                   | Medium     |
| W Method    | Need strategic + operational alignment; 4+ weeks available     | High       |

---

## 2. Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on the complete Growth Model -- all inputs CONFIRMED, all functions aligned, totals tie top-down to bottom-up.
>
> **Output:** Signed-off Growth Model (YAML + micro app + PDF) + Definition Alignment Document + Assumptions Register.

Phase 1 is where the majority of the work happens (~70% of project hours). The Growth Model IS the strategy -- this phase produces it through a structured series of stakeholder conversations, each refining the model from assumptions to confirmed inputs.

**Key deliverables:**

- **v0 Growth Model** built from intake data, CRM export, and industry benchmarks before the kickoff call
- **Definition Alignment Document** -- stakeholder sign-off on ARR, Booking, Churn, SQL, Conversion Rate definitions before modeling begins
- **Iterative model versions (v0 -> v6)** refined after each stakeholder meeting via AI agent processing of meeting transcripts
- **Input Bank** tracking every model input as ASSUMED or CONFIRMED
- **Final signed-off Growth Model** (YAML + PDF + interactive micro app)

**The pattern:** Two parallel tracks run pre-kickoff. Track A educates the customer (intro video, definition alignment doc, intake form). Track B prepares the team (CRM data pull, benchmark research, v0 model build). At kickoff, both converge -- the customer is educated and the team has a 70% pre-filled model ready for reaction and refinement.

**Seven meeting topics** drive the refinement loop: Kickoff, Top-Down Review (Exec Sponsor + Finance), Sales Capacity (Sales Leader), Marketing Pipeline (Marketing Leader), CS Capacity (CS Leader), Finance/Unit Economics (CFO/FP&A), and Final Review + Sign-Off (all stakeholders). These are topics, not strict sequence -- book whoever is available, cover their topic, iterate. Timeline compresses with urgency.

**Decision point at completion:** Strategy-only engagements deliver the Growth Model as the final deliverable and skip to Phase 3 Enablement. Engagements that want operational tracking dashboards proceed to Phase 2 Engineering.

---

## 3. Phase 2: Engineering

> **Goal:** Load the Growth Model into an operational tracking dashboard for ongoing plan-vs-actual monitoring.
>
> **Output:** Configured dashboard instance matching the signed-off Growth Model, tested and customer-approved.

Phase 2 is optional and lightweight for Growth Model projects (10-20% of total hours). It only applies when the customer wants ongoing operational tracking beyond the static model.

**Key deliverables:**

- **Tech spec** mapping Growth Model metrics to dashboard fields, views, and alert thresholds
- **Executive dashboard** (ARR waterfall, bookings vs target, key metrics)
- **Quota tracking views** (rep-by-rep capacity vs actual by quarter)
- **Pipeline vs target views** (with timing offset visualization)
- **Hiring tracker** (planned vs actual hire dates, ramp status)
- **Variance alerts** (green/yellow/red thresholds for key metrics)
- **Department views** (Sales, Marketing, CS, Finance)

**Sub-phase flow:** Tech Spec (2a) -> Engineering Handoff (2b) -> Build (2c) -> QA/Test + Sign-Off (2d). The build is primarily dashboard configuration -- mapping model metrics to views, connecting CRM data sources, and setting alert thresholds.

---

## 4. Phase 3: Enablement

> **Goal:** Customer team can actually use the Growth Model and (if applicable) operational dashboards. Each stakeholder knows their targets, how to monitor them, and when to escalate.
>
> **Output:** Trained team with documentation, stabilized system, no critical issues.

Enablement ensures the Growth Model doesn't become shelfware. Each stakeholder group receives role-specific training on what matters to them.

**Key deliverables:**

- **Training package** -- video walkthroughs (full model for RevOps, executive summary for leadership, maintenance process for the owner), written guides (monthly actuals entry, assumption monitoring), FAQ compiled from discovery meetings
- **Role-based training sessions** delivered to 5 stakeholder groups: RevOps Manager (60 min), Sales Leadership (45 min), Marketing (45 min), CS Leadership (30 min), Finance (30 min)
- **30-day hypercare period** -- one scheduled check-in call, async Q&A support, one model adjustment if a material change occurs

**Sub-phase flow:** Training Prep (3a) -> Training Sessions (3b) -> Hypercare (3c) -> Enablement Sign-Off (3d).

**Enablement sign-off confirms:** All training delivered, recordings and documentation provided, hypercare complete, no critical issues outstanding, and the customer team can update actuals, monitor assumptions, and interpret outputs independently.

---

## 5. Phase 4: Handoff

> **Goal:** Clean project close with maintenance plan established and retention/expansion path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the system, project archived, future revenue path established.

The most common failure mode post-project is not a broken model -- it is a model that slowly becomes irrelevant because nobody updates it. Phase 4 prevents this by establishing explicit maintenance cadences and clear ownership.

**Key deliverables:**

- **Maintenance schedule** with monthly tasks (actual vs plan tracking, assumption pulse check, hiring status), quarterly tasks (full assumption review, capacity reforecast, channel efficiency analysis, sales cycle validation), and annual recalibration (full model rebuild with fresh data, segment mix review, market conditions assessment)
- **Documentation package** -- Growth Model (YAML + PDF), interactive micro app link, Definitions Document, Assumptions Register, all training recordings, written guides, FAQ, maintenance schedule
- **Retention/expansion path** -- single project engagements get an upsell conversation (managed services or adjacent project); dedicated engagements get a refinement check-in scheduled ~1 quarter out

**Sub-phase flow:** Maintenance Schedule (4a) -> Internal Handoff (4b) -> External Handoff (4c) -> Project Close (4d).

**Maintenance ownership depends on engagement type:** Single project engagements transfer maintenance to the customer at external handoff. Dedicated (multi-project) engagements transfer maintenance to the ongoing team at internal handoff.

#### Refinement Triggers

| Trigger                          | Threshold                                  | Response                                                        |
| -------------------------------- | ------------------------------------------ | --------------------------------------------------------------- |
| Bookings variance                | >20% above or below target for 2+ months   | Model adjustment or scope refinement project                    |
| Sales cycle shift                | Extending by >30 days vs modeled           | Adjust all pipeline timing offsets, revalidate capacity needs   |
| New hire ramp                    | Taking >1 quarter longer than modeled      | Revise ramp schedule assumptions, recalculate capacity          |
| Structural business change       | M&A, new product, new market, reorg        | Scope new Growth Model engagement                               |

---

## 6. Deliverables & Assets Summary

**Strategic Deliverables:**

| Deliverable              | Contents                                                          | Format            |
| ------------------------ | ----------------------------------------------------------------- | ----------------- |
| Growth Model             | Integrated model: top-down targets, sales capacity, marketing plan, CS capacity, assumptions | YAML + PDF + Micro App |
| Definitions Document     | Approved definitions for ARR, Booking, Churn, SQL, Conversion Rates, Pipeline | Document        |
| Assumptions Register     | All assumptions categorized (Product, GTM, Channel, External) with owners, confidence levels, monitoring cadence | Spreadsheet      |

**Technical Deliverables (if Phase 2 applies):**

| Deliverable                  | Contents                                              | Format     |
| ---------------------------- | ----------------------------------------------------- | ---------- |
| Executive Dashboard          | ARR waterfall, bookings vs target, key metrics        | Dashboard  |
| Quota Tracking Views         | Rep-by-rep capacity vs actual by quarter              | Dashboard  |
| Pipeline vs Target Views     | Pipeline generation vs required, with timing offset   | Dashboard  |
| Hiring Tracker               | Planned vs actual hire dates, ramp status             | Dashboard  |
| Variance Alerts              | Green/yellow/red thresholds for key metrics           | Dashboard  |

**Documentation Package:**

- Training recordings (per stakeholder role)
- Monthly actuals entry guide
- Assumption monitoring guide
- FAQ document
- Definition Alignment Document (final version)
- Maintenance Schedule
