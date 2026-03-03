# Metering — Implementation

> **Purpose**: The end-to-end process for delivering metering (usage-based billing measurement) projects. Follows the 4-phase framework: Strategy, Engineering, Enablement, Handoff.

## Project One-Pager

### Metering (Q2C) One-Pager

#### Project Type

- Category: Technical (Engineering-heavy)
- Primary Deliverable: Operational metering system that tracks product consumption events and feeds accurate usage data into billing workflows

##### Phase Relevance

| Phase          | Applies? | Weight | Notes                                                        |
| -------------- | -------- | ------ | ------------------------------------------------------------ |
| 1. Strategy    | Yes      | Medium | 2-4 alignment meetings: define billable units, event schema, pricing model mapping |
| 2. Engineering | Yes      | Heavy  | Event ingestion pipeline, rating engine, billing integration, usage dashboards |
| 3. Enablement  | Yes      | Light  | Finance team on usage reports, engineering on instrumentation, ops on monitoring |
| 4. Handoff     | Yes      | Medium | Internal + External — ongoing accuracy monitoring is critical |

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │    Medium    │     │    Heavy     │     │    Light     │     │    Medium    │
  │ 1a→1b→1c→1d │     │ 2a→2b→2c→2d │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   2-4 alignment        Event ingestion      Finance, Eng,        Internal +
   meetings             pipeline + rating    Ops training         External handoff
```

**This project's flow:**
- Full 4-phase. Heavy engineering (50-60% of effort), medium strategy (20-30%), light enablement (15-20%), standard handoff.
- Phase 1 focuses on defining billable units, event schema, and pricing model alignment — this determines the entire engineering build.
- Phase 2 is the core: event ingestion pipeline, aggregation logic, rating engine, billing integration.
- No phases are skipped. Phase 3 is lighter but required — finance and ops teams must understand usage reports and monitoring.

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Watch metering intro video explaining usage-based billing measurement concepts and how metering fits into the Q2C pipeline
- [ ] Complete metering intake form: current pricing model, billable dimensions, event volume estimates, existing billing tools, data infrastructure
- [ ] Gather stakeholder sign-off on billable unit definitions (what counts as a "unit" of usage)
- [ ] Provide system access: product database, event logs, current billing system (Stripe, Chargebee, etc.), data warehouse

##### Track B: Architect Prep
- [ ] Pull current product usage data from customer's data warehouse or analytics platform
- [ ] Audit existing billing system configuration (Stripe metered billing, manual invoicing, etc.)
- [ ] Map customer's pricing model to metering requirements: which events need tracking, at what granularity
- [ ] Draft v0 event schema based on intake form and product documentation
- [ ] Identify metering tool recommendation (Metronome, Orb, m3ter, Amberflo, or custom) based on event volume, pricing complexity, and existing stack

#### Refinement Loop (1b &rarr; 1c &rarr; 1d)

| Meeting      | Sub-Phase | Focus                                                              | Stakeholder                     | Output                          |
| ------------ | --------- | ------------------------------------------------------------------ | ------------------------------- | ------------------------------- |
| Kickoff      | 1b        | Present v0 event schema, validate billable units, review pricing model mapping | RevOps, Product, Finance        | Corrections for v1              |
| Refinement 1 | 1c        | Review v1 event schema + aggregation rules, align on metering tool | Engineering, RevOps             | Validated schema + tool decision|
| Refinement 2 | 1c        | Review billing integration spec, confirm edge case handling        | Finance, Engineering            | Final integration spec          |
| Sign-Off     | 1d        | Strategic approval of metering design                              | All stakeholders                | Approved metering spec package  |

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held
- [ ] 1c. Refinement loop complete (v0 &rarr; vFinal)
- [ ] 1d. Strategic sign-off obtained

##### Phase 2: Engineering
- [ ] 2a. Tech spec created (event schema, aggregation rules, integration specs)
- [ ] 2b. Engineering handoff meeting held
- [ ] 2c. Build complete (event ingestion, aggregation, rating, billing integration, dashboards)
- [ ] 2d. QA/Test + customer sign-off (accuracy validation, volume testing, edge case testing)

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped (usage reports guide, instrumentation guide, monitoring runbook)
- [ ] 3b. Training sessions delivered (Finance, Engineering, RevOps)
- [ ] 3c. Hypercare period complete (4-week billing cycle monitoring)
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff complete
- [ ] 4c. External handoff (LeanScale &rarr; Customer) complete
- [ ] 4d. Project closed and archived

#### Document Types

##### Working Documents (iterate together)

| Document                       | Purpose                                    | When Complete                                          |
|--------------------------------|--------------------------------------------|--------------------------------------------------------|
| Metering intake form           | Capture pricing model, event types, volumes | All fields filled, stakeholder reviewed                |
| Event schema draft             | Define event structure and dimensions      | Schema validated against real product data              |
| Billable unit mapping table    | Map product actions &rarr; billable units       | All units agreed and signed off by Finance + Product   |
| Aggregation rules document     | Define how raw events become billable totals| Rules validated with sample data                       |

##### Deliverables (polished outputs)

| Deliverable                          | Created From              | Customer Uses For                     |
|--------------------------------------|---------------------------|---------------------------------------|
| Metering architecture diagram        | Event schema + tool decision | Engineering implementation reference |
| Billable metrics definition document | Billable unit mapping table | Finance and billing team reference   |
| Integration specification            | Aggregation rules + billing tool audit | Engineering build guide        |
| Usage dashboard configuration        | Billable metrics definitions | Ongoing usage monitoring             |

#### Enablement Details

##### Training Types

| Type        | Audience                          | Focus                                                     | Duration |
| ----------- | --------------------------------- | --------------------------------------------------------- | -------- |
| Finance     | CFO, Controller, Billing Ops      | Read usage reports, validate invoices, understand billing data flow | 45m      |
| Engineering | Backend Engineers, DevOps          | Instrument new events, maintain event schema, debug ingestion failures | 60m      |
| RevOps      | RevOps Manager, Sales Ops          | Understand metering impact on quoting, interpret usage dashboards | 30m      |
| Leadership  | VP Product, VP Finance              | Interpret usage trends, unit economics from metering data  | 30m      |

##### Hypercare
- Applies: Yes
- Duration: 4 weeks (one full billing cycle minimum)
- Office Hours: Yes — weekly 30-min slot for billing accuracy questions

##### Training Assets to Create
- [ ] Video walkthrough: Event schema walkthrough and how events flow to invoices
- [ ] Video walkthrough: Usage dashboard navigation and key metrics
- [ ] Doc: Event instrumentation guide for engineering team
- [ ] Doc: Billing reconciliation runbook for finance team
- [ ] Doc: Monitoring and alerting reference for ops

#### Handoff & Retention

##### Internal Handoff
- Key context for Architect: Metering tool in use, event schema version, billing integration architecture, known edge cases (e.g., event deduplication behavior, aggregation window timing)
- Escalation trigger: Any event schema changes, aggregation rule modifications, billing integration errors, or metering tool upgrades

##### External Handoff (LeanScale &rarr; Customer)
- Final meeting agenda: Architecture review, usage dashboard walkthrough, maintenance schedule review, Q&A
- Documentation package: All training recordings, event schema doc, integration spec, monitoring runbook, maintenance schedule

##### Maintenance Schedule
- Monthly: Usage accuracy audit, event volume monitoring, billing reconciliation spot-check
- Quarterly: Pricing model review, aggregation rule validation, metering tool health check
- Who owns: Single project = customer owns | Dedicated = Architect owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services &rarr; if no &rarr; Downsell: Adjacent Q2C project (billing optimization, RevRec, CPQ) &rarr; Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~1 quarter out (aligned to quarterly business review)
- Internal prep trigger: 2 weeks before
- Decision: Architect handles / specialist needed

#### Key Assets

| Asset                          | Link   | When Used            |
| ------------------------------ | ------ | -------------------- |
| Metering intake form template  | [link] | Phase 1a             |
| Event schema template          | [link] | Phase 1a-1c          |
| Metering architecture diagram  | [link] | Phase 2a             |
| Billing reconciliation runbook | [link] | Phase 3-4            |

#### Definition Alignment Terms

| Term                     | Typical Definition                                                                                       |
| ------------------------ | -------------------------------------------------------------------------------------------------------- |
| Usage Event              | A discrete, timestamped record of a customer action in the product (e.g., API call, message sent, GB stored) |
| Billable Unit            | The unit of measurement that appears on an invoice (e.g., 1,000 API calls, 1 GB of storage)              |
| Billable Metric          | The aggregation of raw usage events into a quantity that drives billing (e.g., total API calls per billing period) |
| Metering Period           | The time window over which usage is aggregated before billing (e.g., hourly, daily, monthly)             |
| Aggregation Rule          | The logic that transforms raw events into billable totals (e.g., SUM of bytes transferred, COUNT of API calls) |
| Rating                    | The process of applying a price to a metered quantity (e.g., $0.01 per API call above 10,000)            |
| Event Schema              | The structured format for usage events: what fields are required, what dimensions are tracked            |
| Idempotency Key           | A unique identifier per event that prevents double-counting if the same event is sent more than once     |
| Dimension                 | A property attached to a usage event used for filtering or segmenting (e.g., region, model, tier)        |
| Entitlement               | A pre-purchased usage commitment or included allowance before overage pricing applies                    |
| Overage                    | Usage that exceeds the entitlement or committed amount, billed at a specified overage rate               |
| Event Ingestion            | The process of receiving, validating, and storing raw usage events from the product                      |
| Billing Integration        | The connection between the metering system and the invoicing/payment system (e.g., Metronome &rarr; Stripe)  |

#### Common Gotchas
- **Double-counting events** &rarr; Require idempotency keys on every event; validate deduplication logic in QA
- **Finance and Engineering define "usage" differently** &rarr; Create a shared data dictionary during Phase 1 and get sign-off before building
- **Event schema changes break billing** &rarr; Version the event schema from day one; store schema configs as code
- **Aggregation window mismatch** &rarr; Align metering period with billing period during strategy — a daily metering window with a monthly invoice needs explicit rollup rules
- **Late-arriving events** &rarr; Define a grace period (typically 24 hours) after which events are rejected or flagged for manual review
- **Bill shock for customers** &rarr; Build usage alerts that notify customers at 50%, 75%, 90%, and 100% of their entitlement or expected usage
- **Testing with production volumes** &rarr; Synthetic test data rarely catches volume-related issues; run a parallel shadow billing period with real data before go-live

#### Methodology Options

| Option                         | When to Use                                                     | Complexity |
| ------------------------------ | --------------------------------------------------------------- | ---------- |
| Managed metering platform      | Event volume &gt;100K/day, complex pricing models, multiple dimensions | Low-Medium (vendor handles infrastructure) |
| Custom metering pipeline       | Unique event types, existing data infrastructure, need full control | High (build and maintain ingestion + aggregation) |
| Billing platform native metering | Simple metering needs, already on Stripe/Chargebee with metered billing | Low (limited flexibility) |

Managed platforms: Metronome, Orb, m3ter, Amberflo
Custom pipeline: Kafka/event bus &rarr; aggregation layer &rarr; billing API
Native: Stripe Metered Billing, Chargebee Usage-Based

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on what we're going to build.
>
> **Output:** Definition Alignment Document + Metering Design Package (event schema, billable unit definitions, aggregation rules, metering tool recommendation, billing integration spec) signed off by stakeholders.

### 1a. Pre-Kickoff

> Two parallel tracks run after the deal closes and before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                          | Format             |
| ----------------------------- | ---------------------------------------------------------------- | ------------------ |
| Intro video                   | Explain what metering is, how it fits into billing, and why accurate measurement matters | Video walkthrough (5-10 min)    |
| Definition Alignment Document | Get stakeholder sign-off on billable unit, metering period, aggregation rule definitions | Google Doc         |
| Metering intake form          | Capture pricing model, billable dimensions, event volume estimates, current billing tools, data infrastructure | Google Form or Doc |
| System access request         | Request access to product event logs, billing system (Stripe, Chargebee), data warehouse | Email/Doc          |

**Metering-specific intake questions:**

1. What is your current pricing model? (flat-rate, per-seat, usage-based, hybrid)
2. If usage-based: what dimensions are you charging on today? (API calls, data volume, compute time, messages, seats, etc.)
3. What is your estimated daily event volume? (&lt;10K, 10K-100K, 100K-1M, &gt;1M)
4. What billing system do you use today? (Stripe, Chargebee, Zuora, manual invoicing, other)
5. Do you have a data warehouse or event bus in place? (Snowflake, BigQuery, Kafka, Segment, etc.)
6. Who owns billing accuracy today? (Finance, Engineering, RevOps, no clear owner)
7. Are you instrumenting product events today? If so, how? (Segment, custom event logging, Mixpanel, etc.)
8. Do you have entitlements or committed usage tiers? (free tier, committed spend, overage pricing)
9. What is your billing cycle? (monthly, quarterly, annual, custom)
10. Are there any known billing disputes or accuracy issues today?

**Completion tracking:** Follow up actively. Don't cancel kickoff if incomplete, but push hard after. System access is critical — without access to product event data, the Architect cannot build a meaningful v0.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                                 | Output                                          |
| ---- | ---------------------------------------------------------------------- | ----------------------------------------------- |
| 1    | Pull current product usage data (event logs, analytics, billing records) | Raw data on what events exist and their volume  |
| 2    | Audit current billing configuration (Stripe metered billing, manual invoicing, etc.) | Current state assessment of billing infrastructure |
| 3    | Map customer's pricing model to metering requirements — which product actions need tracking | Draft billable unit mapping table              |
| 4    | Draft v0 event schema with fields, dimensions, and aggregation rules   | Event schema (all values marked ASSUMED)        |
| 5    | Evaluate metering tool options against requirements                     | Tool recommendation with rationale              |
| 6    | Create kickoff call assets: event flow diagram, billable unit mapping, questions list | Presentation materials                        |

**Metering tool evaluation criteria:**

| Criteria               | Metronome       | Orb             | m3ter          | Amberflo       | Native (Stripe) |
|------------------------|-----------------|-----------------|----------------|----------------|-----------------|
| Event volume handling  | High            | High            | High           | High           | Low-Medium      |
| Pricing model flexibility | High         | High            | High           | Medium         | Low             |
| Pre-built integrations | Stripe, Salesforce | Stripe, NetSuite | Stripe, custom | Stripe, AWS   | Stripe only     |
| Self-serve dashboard   | Yes             | Yes             | Yes            | Yes            | Limited         |
| Contract/entitlement support | Yes       | Yes             | Yes            | Limited        | No              |
| Implementation complexity | Medium       | Medium          | Medium-High    | Medium         | Low             |

**Critical:** Mark everything as ASSUMED. The kickoff call validates.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on metering terms BEFORE building anything.

| Term                 | Our Definition                                                                                        | Internally Approved? |
| -------------------- | ----------------------------------------------------------------------------------------------------- | -------------------- |
| Usage Event          | A discrete, timestamped record of a customer action (e.g., API call, message sent, GB stored)         | [ ] Yes / [ ] No     |
| Billable Unit        | The unit of measurement on an invoice (e.g., 1,000 API calls, 1 GB storage)                           | [ ] Yes / [ ] No     |
| Billable Metric      | The aggregation of raw events into a billing quantity (e.g., total API calls per billing period)       | [ ] Yes / [ ] No     |
| Metering Period      | The time window for aggregation before billing (e.g., hourly, daily, monthly)                         | [ ] Yes / [ ] No     |
| Aggregation Rule     | Logic that transforms raw events into billable totals (e.g., SUM bytes, COUNT calls)                  | [ ] Yes / [ ] No     |
| Entitlement          | Pre-purchased usage commitment or included allowance before overage pricing                           | [ ] Yes / [ ] No     |
| Overage              | Usage exceeding entitlement, billed at specified overage rate                                          | [ ] Yes / [ ] No     |
| Rating               | Applying a price to a metered quantity (e.g., $0.01/API call above 10,000)                            | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your finance and product leadership. Check "Yes" when approved. We cannot build the metering system until all terms are aligned — billing accuracy depends on shared definitions.

---

### 1b. Kickoff Call

> **Purpose:** Present v0 event schema and get alignment on billable units and metering approach. We walk in with work done — customer reacts, not creates from scratch.

#### Agenda (60-90 min)

| Time  | Topic                          | What Happens                                              |
| ----- | ------------------------------ | --------------------------------------------------------- |
| 0-15  | Walk through v0 event schema   | "Here's the event schema we built from your intake data"  |
| 15-30 | Validate billable units        | ASSUMED units &rarr; CONFIRMED or corrected                    |
| 30-45 | Definition alignment           | Review Definition Alignment Doc, get sign-off on terms    |
| 45-55 | Metering tool recommendation   | Present tool evaluation, get directional agreement        |
| 55-70 | Pricing model mapping review   | Walk through: product action &rarr; event &rarr; aggregation &rarr; invoice line item |
| 70-80 | Identify gaps                  | Missing event types, unclear dimensions, access blockers  |
| 80-90 | Next steps                     | Schedule refinement meetings, assign homework             |

**Metering-specific kickoff focus:**
- Validate which product actions are billable vs. non-billable
- Confirm event granularity (per-request vs. per-minute vs. per-hour)
- Identify dimensions that matter for billing segmentation (region, tier, model, etc.)
- Surface pricing edge cases: free tiers, committed spend, overages, prorations

#### What We Bring

- v0 event schema (built in Track B prep)
- Billable unit mapping table (product action &rarr; billable unit)
- Event flow diagram (product &rarr; metering &rarr; billing &rarr; invoice)
- Metering tool evaluation matrix
- Questions list (what we need to validate)
- Definition Alignment Document (pre-filled with our recommendations)

#### What We Leave With

- Feedback and corrections on event schema (info needed to create v1)
- Confirmed or corrected billable unit definitions
- Directional agreement on metering tool
- Alignment loop scheduled
- Clear homework: customer provides sample event data, confirms system access

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Iterate on the metering design package until sign-off. Each round incorporates more real data and moves from ASSUMED to CONFIRMED.

#### The Pattern

```
Kickoff Call (validate billable units, gather corrections)
    ↓
Update event schema → v1
    ↓
Meeting 2 (validate schema against real data, confirm tool) → update → v2
    ↓
Meeting 3 (validate billing integration spec, edge cases) → update → v3
    ↓
Final Review → Sign-off
```

#### Before Each Meeting

1. Process previous meeting transcript/notes
2. Update metering design package (event schema, aggregation rules, integration spec)
3. Prepare questions for next validation round
4. Test schema against any sample data provided

#### During Each Meeting

1. Walk through current version of event schema and specs
2. Capture corrections and refinements
3. Validate what's now CONFIRMED
4. Identify remaining ASSUMED items

#### After Each Meeting

1. Update event schema and specs
2. Track what moved from ASSUMED &rarr; CONFIRMED
3. Update working documents
4. If sample data available, validate schema against it

#### Metering Alignment Meeting Types

| Meeting Type           | Focus                                              | Stakeholder                 |
| ---------------------- | -------------------------------------------------- | --------------------------- |
| Billable Unit Alignment | Define and validate what counts as a billable unit | Finance, Product, RevOps    |
| Schema + Tool Validation | Validate event schema against real data, confirm tool choice | Engineering, RevOps |
| Integration Spec Review  | Billing system integration, edge case handling    | Finance, Engineering        |
| Final Review            | Full metering design walkthrough, sign-off         | All stakeholders            |

#### Typical Timeline

| Milestone               | Timing                                              |
| ----------------------- | --------------------------------------------------- |
| Pre-kickoff prep        | 2-3 days (needs system access for meaningful prep)  |
| Kickoff call            | Day 1 of engagement                                 |
| Meeting loop            | 1-2 weeks (2-3 refinement meetings)                 |
| Final review + sign-off | When all billable units CONFIRMED and tool selected |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything before proceeding to engineering.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by Finance, Product, and Engineering
- [ ] All billable units defined, validated, and CONFIRMED
- [ ] Event schema validated against real product data
- [ ] Aggregation rules specified for each billable metric
- [ ] Metering tool selected and approved
- [ ] Billing integration approach agreed (metering tool &rarr; billing system &rarr; invoicing)
- [ ] Edge cases documented: free tiers, entitlements, overages, prorations, late-arriving events
- [ ] Customer understands what we're building and data flow end-to-end
- [ ] No blockers for engineering (system access, tool licenses, API keys)

**Metering-specific sign-off criteria:**
- Event schema covers all billable product actions
- Aggregation rules produce numbers that Finance agrees match expected billing
- Metering tool can handle estimated event volume with headroom (2-3x current peak)
- Billing integration path is technically feasible (API compatibility confirmed)

#### Decision Point

- **Proceed to Engineering** &rarr; Customer wants metering system built and integrated
- **This project does not have a natural Phase 1 exit point.** Unlike strategic-only projects, metering requires engineering to deliver value — a signed-off design package without implementation does not track usage or generate invoices.

---

## Phase 2: Engineering

> **Goal:** Build and test the metering system based on approved metering design package.
>
> **Output:** Operational metering system — event ingestion running, aggregation producing accurate billable metrics, billing integration generating correct invoice line items, usage dashboards live.

| Project Type    | Engineering Weight | Example                                           |
| --------------- | ------------------ | ------------------------------------------------- |
| Strategic-heavy | Light (10-20%)     | Growth Model — mostly strategy, light Vasco setup |
| Balanced        | Medium (40-60%)    | Attribution — CRM fields, workflows, integrations |
| Technical-heavy | Heavy (70-90%)     | CRM Migration — massive data/config work          |

**Metering is Technical-heavy: Engineering weight is 50-60%.** The event ingestion pipeline, aggregation engine, rating rules, and billing integration are the core deliverables.

### Sub-Phases

```
2a Tech Spec → 2b Engineering Handoff → 2c Build → 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate metering design package into technical build specifications.

**Input:** Signed-off metering design package from Phase 1 (event schema, billable unit definitions, aggregation rules, tool selection, billing integration spec)

**Output:** Draft tech spec containing:

- **Event schema specification** — Field names, data types, required vs. optional fields, dimension definitions, idempotency key format, event versioning strategy
- **Ingestion pipeline architecture** — How events flow from product to metering system (webhook, API push, event bus, batch upload). Includes: authentication, rate limiting, error handling, retry logic
- **Aggregation rules configuration** — For each billable metric: aggregation type (SUM, COUNT, MAX, UNIQUE), aggregation window (hourly, daily, monthly), dimension filters, rounding rules
- **Rating rules** — Price per unit, tiered pricing breakpoints, entitlement thresholds, overage rates, volume discount tiers
- **Billing integration specification** — API mapping between metering system and billing system (e.g., Metronome billable metric &rarr; Stripe invoice line item), sync frequency, error handling
- **Usage dashboard configuration** — Metrics to display, refresh frequency, customer-facing vs. internal dashboards, alert thresholds
- **Build sequence** — What to build first (ingestion before aggregation, aggregation before rating, etc.)

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs with engineer before building.

**Who attends:** Architect + Engineer (or engineering team)

**Agenda (30-45 min):**

| Time  | Topic                         | What Happens                                            |
| ----- | ----------------------------- | ------------------------------------------------------- |
| 0-15  | Walk through metering specs   | Architect explains strategic context: why these billable units, why this tool |
| 15-30 | Engineer questions            | Clarify: event volume expectations, peak load handling, deduplication approach, aggregation timing |
| 30-45 | Refine and approve            | Adjust specs for technical feasibility, confirm build sequence |

**What Architect brings:**

- Metering design package (for strategic context)
- Draft tech spec (from 2a)
- Event schema validated against sample data
- Questions list (anything flagged as unclear in tool evaluation)

**What engineer leaves with:**

- Approved tech spec
- Clear build sequence: ingestion &rarr; aggregation &rarr; rating &rarr; billing integration &rarr; dashboards
- Known risks: event volume spikes, late-arriving events, billing system API limitations
- Access credentials for metering tool and billing system

---

### 2c. Build (Configure)

> **Purpose:** Build the metering system in their infrastructure.

**Input:** Approved tech spec from 2b

**The build loop:**

1. Pick next component from build sequence
2. Build/configure in system
3. Validate with sample data
4. Mark complete, note any issues
5. Repeat until done

**Execution approaches:**

| Approach       | When to Use                                                    | Example                                       |
| -------------- | -------------------------------------------------------------- | --------------------------------------------- |
| Manual build   | First metering implementation, complex custom pipeline          | Engineer configures Metronome + Stripe integration |
| Agent-assisted | Schema and rules are clear, using managed platform             | Agent generates Metronome billable metric configs |
| Automated      | SOP is mature, standard pipeline patterns established          | Template-based pipeline deployment              |

**Metering build components:**

- [ ] **Component 1: Event ingestion pipeline** — Configure event receiver (API endpoint or webhook), validate event format, route to metering system. Include idempotency checking and event deduplication.
- [ ] **Component 2: Billable metric configuration** — Set up each billable metric in metering tool: aggregation type, filters, dimensions, windows. For Metronome: use Basic Filters or SQL Editor depending on complexity.
- [ ] **Component 3: Rating/pricing rules** — Configure price-per-unit, tiered pricing, entitlements, overage rates. Map to customer contracts.
- [ ] **Component 4: Billing system integration** — Connect metering output to billing system (e.g., Metronome &rarr; Stripe). Configure: sync frequency, invoice line item mapping, error handling.
- [ ] **Component 5: Customer-facing usage dashboard** — Build real-time or near-real-time usage visibility for customers: current period usage, usage by dimension, historical trends.
- [ ] **Component 6: Internal usage dashboard** — Build internal monitoring: event ingestion health, aggregation accuracy, billing sync status, alert thresholds.
- [ ] **Component 7: Usage alerts** — Configure customer-facing alerts at usage thresholds (50%, 75%, 90%, 100% of entitlement). Configure internal alerts for ingestion failures, volume spikes, billing sync errors.

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify the metering system produces accurate billable metrics and billing data.

**Two types of testing:**

| Type              | Who      | Purpose                                                         |
| ----------------- | -------- | --------------------------------------------------------------- |
| Technical Testing | Our team | Verify accuracy, reliability, and edge case handling            |
| Customer Testing  | Customer | Verify billing output matches expectations and business logic   |

**Metering technical testing checklist:**

**Accuracy tests:**
- [ ] Send known quantity of test events &rarr; verify aggregated total matches exactly
- [ ] Test each billable metric independently with controlled data
- [ ] Verify aggregation windows align with billing period (no event leakage between periods)
- [ ] Confirm rating calculations: unit price x aggregated quantity = expected invoice amount
- [ ] Validate entitlement logic: usage below entitlement = $0, usage above = correct overage amount
- [ ] Test tiered pricing breakpoints: verify correct tier applied at each threshold

**Volume tests:**
- [ ] Send 2-3x expected peak volume &rarr; verify no event drops or processing delays
- [ ] Monitor ingestion latency under load — target &lt;5 seconds event-to-metering-system
- [ ] Verify aggregation completes within billing window even at peak volume
- [ ] Test burst patterns: 10x normal volume for 5 minutes &rarr; verify recovery

**Edge case tests:**
- [ ] Duplicate events (same idempotency key) &rarr; verify counted only once
- [ ] Late-arriving events (past the aggregation window) &rarr; verify handled per grace period rules
- [ ] Malformed events (missing required fields) &rarr; verify rejected with clear error
- [ ] Zero-usage period &rarr; verify $0 invoice or no invoice generated (per business rules)
- [ ] Mid-period pricing change &rarr; verify prorated correctly
- [ ] Customer with entitlement: usage at exactly the entitlement boundary
- [ ] Multiple dimensions on same event &rarr; verify correct dimension-based billing

**Integration tests:**
- [ ] End-to-end: product event &rarr; metering &rarr; aggregation &rarr; rating &rarr; billing system &rarr; invoice line item
- [ ] Billing sync error recovery: simulate billing API failure &rarr; verify retry and eventual consistency
- [ ] Dashboard data matches billing data (no discrepancy between what customer sees and what they're invoiced)

**Parallel billing run (recommended):**
- [ ] Run metering system in parallel with existing billing for 1-2 billing cycles
- [ ] Compare metered amounts vs. current billing amounts
- [ ] Investigate and resolve any discrepancies before cutover

**Customer testing:**

- Walk customer through usage dashboard
- Have Finance validate sample invoice against expected usage
- Have Engineering send test events and verify they appear in metering
- Capture feedback, fix issues

**Engineering sign-off checkpoint:**

- [ ] All billable metrics producing accurate totals (verified with test data)
- [ ] Event ingestion handling expected volume without drops
- [ ] Billing integration producing correct invoice line items
- [ ] Edge cases handled per spec
- [ ] Dashboards showing accurate, current data
- [ ] Customer has tested and approved
- [ ] Ready for enablement

**Decision point:**

- **Proceed to Enablement** &rarr; Metering system is live, needs training/adoption
- **Loop back to Build** &rarr; Accuracy issues found, integration errors, needs fixes

---

## Phase 3: Enablement

> **Goal:** Customer team can operate the metering system, read usage reports, maintain instrumentation, and monitor billing accuracy.
>
> **Output:** Trained team with documentation, stabilized system through one full billing cycle, no billing discrepancies.

### Sub-Phases

```
3a Training Prep → 3b Training Sessions → 3c Hypercare → 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from metering design docs and built system.

**Input:** Metering design package + tech specs + built system

**Output:** Training package containing:

**For Finance/Billing Ops:**
- Video walkthrough script: "How usage flows from product to invoice" — event &rarr; metering &rarr; aggregation &rarr; rating &rarr; invoice
- Written guide: How to read usage reports, how to validate invoice accuracy, how to spot billing discrepancies
- Reconciliation runbook: Step-by-step billing reconciliation process with expected vs. actual comparison
- FAQ: "Why does my invoice show X when I expected Y?" — common discrepancy causes and resolutions

**For Engineering:**
- Video walkthrough script: "How to instrument a new billable event" — event schema requirements, testing process, deployment checklist
- Written guide: Event schema reference, dimension definitions, idempotency key format, error handling
- Instrumentation checklist: What to do when adding a new product feature that needs metering
- Troubleshooting guide: Common ingestion failures, how to diagnose, how to fix

**For RevOps/Leadership:**
- Video walkthrough script: "Understanding usage dashboards" — key metrics, trends, what actions to take
- Written guide: How metering connects to quoting and pricing decisions
- FAQ: Common questions from sales reps about usage-based pricing

---

### 3b. Training Sessions

> **Purpose:** Transfer metering knowledge to customer team.

**Metering training sessions by stakeholder role:**

| Type                    | Audience                           | Focus                                                                    | Duration |
| ----------------------- | ---------------------------------- | ------------------------------------------------------------------------ | -------- |
| Finance training        | CFO, Controller, Billing Ops       | Read usage reports, validate invoices, run billing reconciliation, understand data flow from event to invoice | 45 min   |
| Engineering training    | Backend Engineers, DevOps          | Instrument new events, maintain event schema, debug ingestion failures, understand deduplication and error handling | 60 min   |
| RevOps training         | RevOps Manager, Sales Ops          | Interpret usage dashboards, understand impact on quoting and renewals    | 30 min   |
| Leadership briefing     | VP Product, VP Finance             | Interpret usage trends, unit economics from metering, pricing optimization signals | 30 min   |

**Training delivery:**

1. Schedule sessions with appropriate stakeholders (Finance and Engineering are mandatory; RevOps and Leadership are recommended)
2. Deliver training (live recommended for Finance and Engineering; recorded acceptable for RevOps and Leadership)
3. Record sessions for future reference and onboarding new team members
4. Answer questions, note gaps in documentation

**Output:**

- Trained stakeholders across Finance, Engineering, RevOps
- Session recordings for each training
- Questions log (feeds into FAQ and documentation updates)

---

### 3c. Hypercare

> **Purpose:** Intensive post-launch support through at least one full billing cycle to verify metering accuracy under real conditions.

**Duration:** 4 weeks minimum (must cover one full billing cycle). Extend to 6-8 weeks if billing cycle is monthly and first cycle reveals issues.

**Metering hypercare specifics:**
- Weekly 30-min office hours for billing accuracy questions
- Daily monitoring of event ingestion health and aggregation accuracy during first 2 weeks
- Active comparison of metered billing vs. expected billing for first invoice cycle
- Bug triage for any billing discrepancies — root cause analysis within 24 hours
- Adjustment of alert thresholds based on actual usage patterns (initial thresholds are estimates)

**Hypercare monitoring checklist:**
- [ ] Event ingestion rate stable (no unexplained drops or spikes)
- [ ] Aggregation producing consistent, accurate totals
- [ ] First invoice cycle accurate — metered amount matches Finance expectations
- [ ] No duplicate billing (idempotency working correctly)
- [ ] Customer-facing dashboard showing accurate, current data
- [ ] Usage alerts firing correctly at configured thresholds
- [ ] No billing disputes from end customers

**What happens:**

- Quick response to billing accuracy issues — these are high priority because they directly affect revenue
- Office hours: scheduled weekly availability (Finance + Engineering can join)
- Bug triage and fixes for any metering discrepancies
- Stabilization before steady-state

**When to extend:** If first billing cycle reveals accuracy issues &gt;1% variance, extend hypercare until resolved. Billing accuracy is non-negotiable — unlike some project types, metering hypercare should not be shortened.

**Output:** Stabilized metering system, first billing cycle completed accurately, no critical discrepancies

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm customer can operate the metering system independently.

**Validation checkpoint:**

- [ ] All training sessions delivered (Finance, Engineering mandatory; RevOps, Leadership recommended)
- [ ] Training recordings and documentation provided
- [ ] At least one full billing cycle completed accurately
- [ ] No billing discrepancies outstanding
- [ ] Finance team can validate invoices independently
- [ ] Engineering team can instrument new events without LeanScale support
- [ ] Monitoring dashboards and alerts are operational
- [ ] Customer team can operate without daily support
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** &rarr; Customer is enabled, at least one billing cycle verified accurate
- **Extend Hypercare** &rarr; Billing accuracy issues persist, need more monitoring time

---

## Phase 4: Handoff

> **Goal:** Clean project close with metering maintenance plan established and retention/expansion path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the metering system, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule → 4b Internal Handoff → 4c External Handoff → 4d Project Close
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At                                                                         |
| ----------------------------- | -------------------- | ------------------------------------------------------------------------------------- |
| **Single Project**            | Customer owns        | 4c (External Handoff) — customer receives maintenance schedule and runs it themselves |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) — Architect receives maintenance schedule and runs it for customer     |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention to keep metering accurate and billing reliable.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task                  | What to Check                                                      | Red Flag Threshold                                                  |
| ----------------------------- | ------------------------------------------------------------------ | ------------------------------------------------------------------- |
| Usage accuracy audit          | Compare metered totals to independent usage data source (product analytics, data warehouse) | &gt;1% variance between metered and independent totals                 |
| Event ingestion health check  | Review ingestion error rates, dropped events, latency              | Error rate &gt;0.1%, any dropped events, latency &gt;30 seconds           |
| Billing reconciliation        | Compare metered invoice amounts to expected revenue per customer   | Any discrepancy &gt;$100 or &gt;2% of invoice amount                     |
| Event volume trend review     | Track event volume trends, identify unexpected spikes or drops     | &gt;50% volume change without corresponding product change             |

**Quarterly Tasks:**

| Quarterly Task                  | What to Review                                                   | Action if Off-Track                                                |
| ------------------------------- | ---------------------------------------------------------------- | ------------------------------------------------------------------ |
| Pricing model fitness check     | Do current billable units still align with product value delivery? | If misaligned: scope pricing model update project                  |
| Aggregation rule validation     | Run aggregation rules against raw events; verify no drift in logic | If rules drifted: fix and audit affected billing periods           |
| Metering tool health review     | Check tool performance, storage usage, API rate limit headroom   | If approaching limits: plan capacity upgrade                       |
| New feature metering assessment | Identify product features launched without metering instrumentation | If missed: scope instrumentation sprint                            |

**After First Business Cycle (30-90 days post-launch):**

- **Billing accuracy validation:** Compare first 2-3 full billing cycles. Are metered amounts consistent? Do they match Finance expectations?
- **Volume baseline establishment:** Set baseline event volumes for monitoring. First 90 days establishes "normal" patterns.
- **Customer feedback check:** Any billing disputes or confusion from end customers? Any usage reporting gaps?
- **Key question:** Is the metering system producing accurate, trusted billing data? If Finance is manually adjusting invoices, something is wrong.

**Refinement Triggers (when to re-engage):**

| Trigger                        | Threshold                                         | Response                                                          |
| ------------------------------ | ------------------------------------------------- | ----------------------------------------------------------------- |
| Billing accuracy drift         | &gt;1% variance for 2+ consecutive months            | Re-engage specialist for root cause analysis and fix                     |
| Event volume growth            | Approaching 80% of metering tool capacity          | Scope capacity upgrade or architecture review                     |
| New pricing model              | Customer changing pricing structure (new tiers, dimensions) | Scope pricing model update — may require new billable metrics     |
| Billing disputes               | 3+ customer disputes in a billing cycle            | Re-engage specialist for metering audit                                  |
| New product line               | Customer launching new product that needs metering | Scope metering expansion — new event types, new billable units    |

**Every 6-12 Months:**

- **Full metering system review:** Audit event schema for deprecated fields, unused dimensions, schema version hygiene
- **Billing integration audit:** Verify API connections are current, no deprecated endpoints, error handling still appropriate
- **Pricing model recalibration:** Work with Finance to assess whether billable units and pricing tiers still align with customer value
- **Technology assessment:** Evaluate if metering tool is still the right choice given current volumes and requirements

---

### 4b. Internal Handoff

> **Purpose:** Transfer metering context so Architect can manage ongoing relationship.

**What the Architect needs to know:**

- What was built and why (metering architecture: event types, aggregation rules, billing integration)
- Metering tool in use and how to access admin dashboard
- Customer context (stakeholders, billing cycle timing, known edge cases)
- Current event schema version and any recent changes
- Common issues and how to resolve them
- When to escalate back to specialist
- **Maintenance schedule** (if Dedicated engagement — Architect runs this)

**Metering-specific escalation guidelines:**

| Issue Type                                        | Who Handles                    | Examples                                           |
| ------------------------------------------------- | ------------------------------ | -------------------------------------------------- |
| Dashboard access issues, usage report questions   | Architect                      | "How do I filter by region?" "Where's the export?" |
| Small billing discrepancies (&lt;$100, one customer) | Architect (with runbook)       | Invoice rounding difference, timezone edge case     |
| Event schema changes, new billable metrics        | Specialist                     | New product feature needs metering                 |
| Aggregation rule modifications                    | Specialist                     | Changing from daily to hourly aggregation          |
| Billing integration errors, sync failures         | Specialist                     | Stripe API errors, metering tool outage            |
| Pricing model changes                             | Specialist                     | New tier, new dimension, new entitlement structure |

**For Dedicated engagements:** Architect also receives the maintenance schedule (4a) and becomes responsible for executing monthly accuracy audits and quarterly reviews. Specialist walks Architect through each maintenance task with real examples from this customer's data.

---

### 4c. External Handoff (LeanScale &rarr; Customer)

> **Purpose:** Formal project completion with customer.

**Final project meeting:**

- Review what was delivered (metering architecture, billable metrics, billing integration, dashboards)
- Walk through documentation package
- Demo: send a test event &rarr; watch it flow through metering &rarr; appear on dashboard &rarr; show up on draft invoice
- Confirm nothing outstanding (no billing discrepancies, no missing instrumentation)
- Answer final questions
- Make it explicit: "Project complete"
- **For Single Project engagements:** Hand over the maintenance schedule (4a) and walk the customer through monthly accuracy audits and quarterly reviews

**Documentation package:**

- All training session recordings (Finance, Engineering, RevOps, Leadership)
- Event schema documentation (current version)
- Billing integration specification
- Monitoring and alerting reference
- Billing reconciliation runbook
- Definition Alignment Document (final version)
- FAQ document
- Support contact info
- **Maintenance Schedule** (for Single Project engagements — this becomes the customer's responsibility)

**For Single Project engagements:** Walk the customer through the maintenance schedule in detail. Record a video walkthrough. Emphasize the monthly accuracy audit — this is the most important maintenance task. If they stop doing this, billing drift becomes invisible.

**Output:** Customer owns the metering system. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location (event schema, tech specs, design docs, test results)
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
1. Upsell: Managed Services (metering monitoring + billing accuracy management on retainer)
   ↓ if no
2. Downsell: Adjacent Q2C project (billing optimization, RevRec setup, CPQ implementation, pricing & packaging)
   ↓ if yes
3. Retry retainer at end of next project cycle
```

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On [date ~quarter out], we'll review metering accuracy over the past quarter, check if any new product features need instrumentation, and see if your pricing model needs updates."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                                           |
| ------------------- | ---------------------------------------------------------------------- |
| 1. Get pinged       | System reminder: metering refinement check-in in 2 weeks              |
| 2. Review metrics   | Pull billing accuracy data, event volume trends, any support tickets   |
| 3. Decide ownership | Can Architect handle this check-in, or need specialist?               |
| 4. Prep materials   | If specialist needed, brief them. If Architect, prep talking points.   |

**At the refinement check-in:**

- Review billing accuracy over the past quarter
- Identify any new product features that need metering instrumentation
- Check if pricing model changes are planned that would affect metering
- If minor: Architect handles (e.g., alert threshold adjustment)
- If major: Scope new project (e.g., new billable dimension, pricing model overhaul)

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- Definition Alignment Document (billable unit definitions, metering terms, signed off by stakeholders)
- Billable Unit Mapping Table (product action &rarr; billable unit &rarr; aggregation rule)
- Event Schema Specification (fields, dimensions, versioning, idempotency key format)
- Metering Architecture Diagram (end-to-end event flow: product &rarr; metering &rarr; billing &rarr; invoice)
- Metering Tool Evaluation (recommendation with rationale)

**Technical Deliverables:**

- Configured metering system (event ingestion, billable metrics, aggregation rules, rating/pricing rules)
- Billing integration (metering system &rarr; billing system, tested and operational)
- Customer-facing usage dashboard (real-time usage visibility, historical trends, dimension breakdowns)
- Internal monitoring dashboard (ingestion health, aggregation accuracy, billing sync status)
- Usage alert configuration (customer alerts at entitlement thresholds, internal alerts for system issues)

**Documentation Package:**

- Training session recordings (Finance, Engineering, RevOps, Leadership)
- Event instrumentation guide (for Engineering: how to add new billable events)
- Billing reconciliation runbook (for Finance: step-by-step accuracy validation)
- Monitoring and alerting reference (for Ops: what alerts mean, how to respond)
- FAQ document
- Definition Alignment Document (final version)
- Maintenance Schedule

---

## Appendix

### What This Document Is

This is the **implementation playbook** — the step-by-step execution guide an Architect follows to deliver a metering project from first contact to project close. It is the third file in a 3-file playbook structure: Overview (positioning and outcomes), Methodology (frameworks and concepts), and Implementation (execution with checklists).

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
- **Phase 4 always applies** — every project needs handoff, but the maintenance schedule complexity varies
- Mark phases as `[SKIP]` or `[LIGHT]` in the One-Pager if they don't fully apply

---

## References

- [FlexPrice - Best Practices for Usage Metering in Cloud Services](https://flexprice.io/blog/best-practices-for-usage-metering-in-cloud-services)
- [Vayu - How to Implement Metered Billing Software](https://www.withvayu.com/blog/implementing-metered-billing-software)
- [Metronome Documentation](https://docs.metronome.com/)
- [Orb - Metered Billing Software for SaaS](https://www.withorb.com/blog/metered-billing-software)
- [m3ter - Usage-Based Billing Software](https://www.m3ter.com/)
- [Stripe - Pay-as-you-go Pricing Implementation Guide](https://docs.stripe.com/billing/subscriptions/usage-based/implementation-guide)
- [Metronome - Create Billable Metrics](https://docs.metronome.com/connect-metronome/create-billable-metrics/)
