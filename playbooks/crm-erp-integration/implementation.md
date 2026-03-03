# CRM-ERP Integration — Implementation

## Project One-Pager

> Quick reference for architects. One per project type. Fill this out FIRST — it serves as the project's identity card.

### CRM-ERP Integration One-Pager

#### Project Type

- Category: Technical
- Primary Deliverable: Bi-directional integration pipeline connecting CRM (Salesforce/HubSpot) and ERP systems with automated data sync for accounts, opportunities/sales orders, and invoices/payments

##### Phase Relevance

| Phase          | Applies? | Weight | Notes                                                        |
| -------------- | -------- | ------ | ------------------------------------------------------------ |
| 1. Strategy    | Yes      | Med    | 3-4 meetings: requirements, data mapping, architecture decisions |
| 2. Engineering | Yes      | Heavy  | Core of the project — build integration pipelines, test sync flows |
| 3. Enablement  | Yes      | Med    | Training Sales + Finance on new workflows, hypercare for sync stabilization |
| 4. Handoff     | Yes      | Med    | Internal + External — monitoring dashboards, maintenance runbook |

· · ·

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │   Medium     │     │    Heavy     │     │   Medium     │     │   Medium     │
  │ 1a→1b→1c→1d │     │ 2a→2b→2c→2d │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   Requirements &       Build pipelines     Train Sales &         Monitoring +
   data mapping         + test sync flows   Finance teams         maintenance docs
```

**This project's flow:**
- Full 4-phase. Heavy engineering (60-70% of effort), medium strategy, medium enablement.
- Phase 1 focuses on system audit, data mapping, and architecture decisions — not strategic modeling.
- Phase 2 is the extended: building Account/Customer sync, Opportunity/Sales Order sync, and Invoice/Payment sync pipelines.
- Phase 3 covers training for both Sales and Finance since the integration changes daily workflows for both teams.
- No phases skipped. Phased rollout (pilot group first) happens within Phase 2.

· · ·

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Grant admin-level API access to CRM and ERP systems (integration user accounts preferred)
- [ ] Complete data mapping intake form: current fields, custom objects, and picklist values in CRM
- [ ] Provide ERP data dictionary: chart of accounts, customer master, product/item catalog, sales order structure
- [ ] Identify and document current manual workflows between CRM and ERP (who enters what, where, when)
- [ ] Confirm executive sponsors from both Sales/RevOps and Finance

##### Track B: Architect Prep
- [ ] Pull CRM schema: objects, fields, relationships, custom fields
- [ ] Pull ERP data dictionary and API documentation
- [ ] Run data quality audit on both systems (duplicates, incomplete records, formatting inconsistencies)
- [ ] Document API capabilities: REST/SOAP availability, rate limits, authentication methods, sandbox access
- [ ] Draft preliminary data mapping matrix (Account/Customer, Opportunity/Sales Order, Invoice/Payment)

· · ·

#### Refinement Loop (1b → 1c → 1d)

| Meeting            | Sub-Phase | Focus                                                    | Stakeholder                      | Output                           |
| ------------------ | --------- | -------------------------------------------------------- | -------------------------------- | -------------------------------- |
| Kickoff            | 1b        | Present system audit findings, validate pain points      | VP Sales, Finance Controller, RevOps | Confirmed requirements + priorities |
| Data Mapping Review | 1c       | Walk through field mapping matrix, resolve conflicts     | RevOps Lead, Finance Ops         | Approved data mapping document   |
| Architecture Decision | 1c     | Present integration approach options (iPaaS vs custom), agree on tool | RevOps Lead, IT/Engineering | Signed-off architecture spec     |
| Sign-Off           | 1d        | Final review of data governance rules + sync specs       | All stakeholders                 | Approved strategic package       |

· · ·

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held — pain points confirmed, priorities ranked
- [ ] 1c. Refinement loop complete (data mapping + architecture decision)
- [ ] 1d. Strategic sign-off obtained (data governance + integration specs approved)

##### Phase 2: Engineering
- [ ] 2a. Tech spec created (field mappings, sync triggers, error handling rules)
- [ ] 2b. Engineering handoff meeting held
- [ ] 2c. Build complete (Account sync + Opportunity/SO sync + Invoice/Payment sync)
- [ ] 2d. QA/Test + customer sign-off (unit tests, integration tests, pilot validation)

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped (separate tracks for Sales vs Finance)
- [ ] 3b. Training sessions delivered
- [ ] 3c. Hypercare period complete (2-week intensive monitoring)
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff (SME to Architect) complete
- [ ] 4c. External handoff to Customer complete
- [ ] 4d. Project closed and archived

· · ·

#### Document Types

##### Working Documents (iterate together)

| Document                    | Purpose                                        | When Complete                              |
| --------------------------- | ---------------------------------------------- | ------------------------------------------ |
| Data Mapping Matrix         | Map CRM fields to ERP fields with sync direction | All fields mapped, transformations defined |
| System Audit Report         | Document current state of both systems         | Both systems fully documented              |
| Data Quality Assessment     | Identify duplicates, gaps, formatting issues   | All issues cataloged and remediation planned |
| Integration Architecture Spec | Define tool, authentication, sync frequency  | Architecture approved by stakeholders      |

##### Deliverables (polished outputs)

| Deliverable                  | Created From                | Customer Uses For                 |
| ---------------------------- | --------------------------- | --------------------------------- |
| Integration Architecture Diagram | System audit + architecture spec | Internal alignment, IT documentation |
| Field Mapping Reference      | Data mapping matrix          | Ongoing reference for data governance |
| Monitoring Dashboard         | Build phase configuration    | Daily/weekly sync health monitoring |
| Troubleshooting Runbook      | QA findings + edge cases     | Self-service issue resolution     |

· · ·

#### Enablement Details

##### Training Types

| Type       | Audience                            | Focus                                              | Duration |
| ---------- | ----------------------------------- | -------------------------------------------------- | -------- |
| Sales      | VP Sales, AEs, Sales Managers       | What syncs automatically, invoice status visibility, what to stop doing manually | 30m      |
| Finance    | Finance Controller, AR team         | Sales order auto-creation, payment status sync, exception handling | 45m      |
| Technical  | RevOps Admin, IT team               | Monitoring dashboards, error triage, API credential rotation, change procedures | 60m      |

##### Hypercare
- Applies: Yes
- Duration: 2 weeks (daily monitoring first week, reduced to 2x/week second week)
- Office Hours: Yes — daily 15-min sync review first week, then weekly 30-min slot

##### Training Assets to Create
- [ ] Video walkthrough: Integration overview — what syncs, when, in which direction
- [ ] Video walkthrough: Monitoring dashboard walkthrough — how to check sync status
- [ ] Doc: Field mapping reference (1-page quick reference)
- [ ] Doc: Troubleshooting runbook — common issues and resolution steps
- [ ] Doc: Admin guide — API credential rotation, change procedures, alert response

· · ·

#### Handoff & Retention

##### Internal Handoff (SME to Architect)
- Key context for Architect: Data mapping decisions, sync frequency rationale, known edge cases (multi-currency, partial payments, international addresses)
- Escalation trigger: Any changes to sync logic, new object types to sync, API version upgrades, ERP schema changes

##### External Handoff (to Customer)
- Final meeting agenda: Review integration architecture, walk through monitoring dashboard, confirm maintenance schedule, transfer admin credentials
- Documentation package: Architecture diagram, field mapping reference, troubleshooting runbook, admin guide, training video walkthroughs, maintenance schedule

##### Maintenance Schedule
- Monthly: Sync health review, data quality spot-check, API usage monitoring
- Quarterly: Full data mapping validation, performance review, governance update
- Who owns: Single project = customer owns | Dedicated = Architect owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services (ongoing monitoring + optimization) → if no → Downsell: Related project (reporting/BI dashboards, lead lifecycle automation) → Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~quarter after go-live
- Internal prep trigger: 2 weeks before
- Decision: Architect handles routine maintenance / SME needed for sync logic changes

· · ·

#### Key Assets

| Asset                    | When Used            |
| ------------------------ | -------------------- |
| Data Mapping Matrix      | Phase 1 → Phase 2   |
| Integration Architecture Diagram | Phase 1d → ongoing |
| Monitoring Dashboard     | Phase 2d → ongoing   |
| Troubleshooting Runbook  | Phase 3 → ongoing    |

· · ·

#### Definition Alignment Terms

| Term                  | Typical Definition                                                              |
| --------------------- | ------------------------------------------------------------------------------- |
| System of Record      | The authoritative source for a given data element (e.g., ERP owns billing address, CRM owns contacts) |
| Sync Direction        | Which system pushes data: CRM-to-ERP, ERP-to-CRM, or bi-directional           |
| Closed-Won Trigger    | The CRM stage change that initiates sales order creation in ERP                 |
| Data Transformation   | Rules that convert data formats between systems (e.g., "CA" to "California")   |
| Conflict Resolution   | The rule applied when the same field has different values in CRM and ERP (timestamp-based, source priority, or manual review) |
| Integration User      | A dedicated service account with scoped permissions for API access (not a personal admin account) |
| Rate Limit            | The maximum number of API calls allowed per time period by each system          |
| Idempotent Sync       | A sync operation that produces the same result whether run once or multiple times (prevents duplicate records) |

· · ·

#### Common Gotchas
- Starting integration before cleaning data in both systems → Run data quality audit first; 91% of CRM data is incomplete [1] and syncing dirty data amplifies problems across both systems
- No single source of truth for shared fields → Define data ownership matrix specifying which system owns each data type before building anything
- "Big bang" rollout → Start with highest-value sync (Opportunity to Sales Order), validate, then expand
- Inconsistent field formatting ("CA" vs "California") → Build transformation layer that standardizes formats before sync; test with edge cases
- Silent sync failures → Configure monitoring with alerts on any failure; review dashboards daily during first 2 weeks
- Using admin accounts for API access → Create dedicated integration users with least-privilege permissions; admin accounts change passwords, breaking syncs
- Not accounting for API rate limits → Design throttling strategy; monitor usage at 80% threshold

· · ·

#### Methodology Options

| Option              | When to Use                                       | Complexity |
| ------------------- | ------------------------------------------------- | ---------- |
| Native Connector    | Both systems from same vendor, simple use case    | Low        |
| iPaaS (Celigo, Workato) | Mid-market, multiple use cases, limited dev team | Medium     |
| Custom API (MuleSoft, code) | Enterprise, complex transformations, high volume | High       |

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on data mapping, integration architecture, and data governance rules.
>
> **Output:** Approved Data Mapping Matrix + Integration Architecture Spec + Data Governance Rules (signed off by VP Sales, Finance Controller, and RevOps Lead).

### 1a. Pre-Kickoff

> Two parallel tracks run after the sale closes and before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                    | Format             |
| ----------------------------- | ---------------------------------------------------------- | ------------------ |
| Intro video                   | Explain what CRM-ERP integration involves and project scope | Video walkthrough (5-10 min) |
| Definition Alignment Document | Get stakeholder sign-off on data ownership and sync terms  | Google Doc         |
| Pre-filled intake form        | Confirm system versions, API access, current manual workflows | Google Form or Doc |

**What the intake form asks:**
- CRM platform and version (Salesforce edition, HubSpot tier)
- ERP platform and version (NetSuite, SAP, Microsoft Dynamics, etc.)
- Current manual workflows: who enters data where, how often, what triggers it
- Priority use cases ranked by business impact
- Known data quality issues
- Existing integration attempts (if any) and why they failed
- Desired sync frequency by data type
- Compliance requirements (GDPR, SOC2, industry-specific)

**Completion tracking:** RevOps Lead owns follow-up. Do not cancel kickoff if incomplete, but push hard — API access is a blocker for Track B.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                        | Output                              |
| ---- | ------------------------------------------------------------- | ----------------------------------- |
| 1    | Run System Audit against CRM and ERP                          | System schema documentation         |
| 2    | Run data quality assessment on both systems                   | Data quality report (duplicates, gaps, formatting) |
| 3    | Document API capabilities (rate limits, auth, sandbox access) | API capability matrix               |
| 4    | Generate draft data mapping matrix from system schemas        | Draft mapping with ASSUMED markers  |
| 5    | Prepare kickoff assets (audit summary, mapping preview)       | Kickoff presentation materials      |

**Critical:** Mark everything as ASSUMED. The kickoff call validates. Do not build anything before data mapping is confirmed.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building anything.

| Term                 | Our Definition                                                          | Internally Approved? |
| -------------------- | ----------------------------------------------------------------------- | -------------------- |
| System of Record     | ERP owns billing/financial data; CRM owns contacts and opportunity data | [ ] Yes / [ ] No     |
| Closed-Won Trigger   | Opportunity stage = "Closed Won" initiates ERP sales order creation     | [ ] Yes / [ ] No     |
| Sync Frequency       | Real-time for Closed-Won; hourly for customer updates; daily for invoices | [ ] Yes / [ ] No   |
| Conflict Resolution  | Timestamp-based: most recent update wins, with manual review for financial fields | [ ] Yes / [ ] No |
| Integration User     | Dedicated service account with scoped API permissions (not admin accounts) | [ ] Yes / [ ] No  |
| Data Transformation  | Standardize state/country codes, currency formats, date formats before sync | [ ] Yes / [ ] No  |

**Instructions to customer:**

> Review each definition with your Sales and Finance leadership teams. Check "Yes" when approved. We cannot proceed until all terms are aligned — misalignment here causes rework during the build.

---

### 1b. Kickoff Call

> **Purpose:** Present system audit findings, validate pain points, and begin data mapping alignment. We walk in with work done — customer reacts, not creates from scratch.

#### Agenda (60-90 min)

| Time  | Topic                                | What Happens                                           |
| ----- | ------------------------------------ | ------------------------------------------------------ |
| 0-15  | System audit walkthrough             | "Here's what we found in your CRM and ERP"             |
| 15-30 | Data quality findings                | Present duplicate counts, incomplete fields, format gaps |
| 30-45 | Validate pain points                 | Confirm manual workflows, quantify time spent on re-entry |
| 45-55 | Review draft data mapping            | Walk through Account/Customer mapping, get reactions    |
| 55-70 | Priority use case ranking            | Which sync pipeline matters most? (usually Opp to SO)  |
| 70-80 | Definition alignment review          | Review terms doc, identify disagreements               |
| 80-90 | Next steps                           | Assign homework, schedule data mapping deep-dive       |

#### What We Bring

- System audit report (CRM and ERP schemas, API capabilities)
- Data quality assessment (duplicates, gaps, formatting issues)
- Draft data mapping matrix (ASSUMED — needs validation)
- Definition Alignment Document (pre-filled with our recommendations)
- Priority use case recommendations based on industry patterns

#### What We Leave With

- Confirmed pain points with estimated time/cost impact
- Reactions to data mapping (corrections, additions, questions)
- Priority use cases ranked by customer
- Clear homework: resolve data quality issues, finalize definition alignment
- Data mapping review session scheduled

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Iterate on data mapping and integration architecture until sign-off. Typically 2-3 meetings after kickoff.

#### The Pattern

```
Kickoff Call (validate pain points, review draft mapping)
    |
Architect updates mapping with feedback
    |
Meeting 2: Data Mapping Review (field-by-field walkthrough)
    |
Architect finalizes mapping, drafts architecture spec
    |
Meeting 3: Architecture Decision (tool selection, sync specs)
    |
Architect creates final strategic package
    |
Meeting 4: Sign-Off (all stakeholders approve)
```

#### Before Each Meeting

1. Process previous meeting notes and update data mapping matrix
2. Update ASSUMED to CONFIRMED for validated items
3. Prepare questions for remaining open items

#### During Each Meeting

1. Walk through current version of data mapping / architecture spec
2. Capture corrections and refinements
3. Validate what is now CONFIRMED
4. Identify remaining ASSUMED items and assign owners to resolve

#### After Each Meeting

1. Update data mapping matrix and/or architecture spec
2. Track what moved from ASSUMED to CONFIRMED
3. Update working documents and flag blockers

#### Meeting Types for CRM-ERP Integration

| Meeting Type           | Focus                                          | Stakeholder                  |
| ---------------------- | ---------------------------------------------- | ---------------------------- |
| Kickoff                | System audit, pain points, draft mapping       | VP Sales, Finance, RevOps    |
| Data Mapping Review    | Field-by-field mapping, transformations, sync direction | RevOps Lead, Finance Ops |
| Architecture Decision  | Tool selection, sync frequency, error handling | RevOps Lead, IT/Engineering  |
| Final Review / Sign-Off | Complete package approval                     | All stakeholders             |

#### Typical Timeline

| Milestone               | Timing                                    |
| ----------------------- | ----------------------------------------- |
| Pre-kickoff prep        | 3-5 days (depends on API access timing)   |
| Kickoff call            | Day 1 of engagement                       |
| Meeting loop            | 1-2 weeks (3 meetings typical)            |
| Final review + sign-off | When all mappings CONFIRMED, architecture approved |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything before proceeding to build.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by VP Sales, Finance Controller, and RevOps Lead
- [ ] Data Mapping Matrix complete — all fields mapped with sync direction and transformation rules
- [ ] Integration architecture decided — tool selected, authentication method agreed
- [ ] Data governance rules documented — system of record per data type, conflict resolution rules
- [ ] Sync frequency agreed per data type (real-time, hourly, daily)
- [ ] Error handling requirements defined (retry logic, failure notifications, manual override)
- [ ] Data quality remediation plan in place (or completed)
- [ ] No blockers for engineering

#### Decision Point

- **Proceed to Engineering** → All mappings confirmed, architecture approved, data quality acceptable
- **Pause for data cleanup** → Data quality too poor to sync; customer needs to remediate first (provide remediation plan with timeline)

> This project does NOT have a natural exit point after Phase 1. The strategic deliverable (data mapping + architecture spec) has no value without the technical build. Always proceed to Phase 2.

---

## Phase 2: Engineering

> **Goal:** Build and test the integration pipelines based on approved data mapping and architecture spec.
>
> **Output:** Working integration: Account/Customer sync, Opportunity/Sales Order sync, Invoice/Payment sync — tested and customer-approved.

| Project Type    | Engineering Weight | Example                                            |
| --------------- | ------------------ | -------------------------------------------------- |
| Strategic-heavy | Light (10-20%)     | Growth Model — mostly strategy, light tool setup   |
| **This project** | **Heavy (60-70%)** | **CRM-ERP Integration — multiple sync pipelines, testing, pilot** |
| Balanced        | Medium (40-60%)    | Attribution — CRM fields, workflows, integrations  |

### Sub-Phases

```
2a Tech Spec → 2b Engineering Handoff → 2c Build → 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate approved data mapping and architecture spec into technical build instructions.

**Input:** Signed-off data mapping matrix + integration architecture spec + data governance rules

**Output:** Draft tech spec containing:

- Middleware/iPaaS configuration specs (connection setup, authentication)
- Sync pipeline definitions per data type:
  - **Pipeline 1: Account/Customer Sync** — trigger logic, field transformations, duplicate detection rules, merge/update logic
  - **Pipeline 2: Opportunity/Sales Order Sync** — Closed-Won trigger, line item mapping, multi-currency handling, approval workflow for discount thresholds
  - **Pipeline 3: Invoice/Payment Status Sync** — reverse sync triggers (invoice creation, payment posting), custom CRM field creation, partial payment handling
- API throttling strategy (request batching, rate limit compliance)
- Error handling specs: retry intervals, failure notification channels, manual override procedures
- Data validation rules: required field checks, format validation, referential integrity
- Build sequence: Pipeline 1 first (foundational), then Pipeline 2 (highest value), then Pipeline 3 (reverse flow)

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs with engineer before building.

**Who attends:** Architect + Engineer (or engineering team)

**Agenda (45-60 min):**

| Time  | Topic                           | What Happens                                          |
| ----- | ------------------------------- | ----------------------------------------------------- |
| 0-15  | Strategic context               | Why this integration matters, stakeholder expectations |
| 15-30 | Walk through sync pipeline specs | Field mappings, triggers, transformations per pipeline |
| 30-45 | Error handling + edge cases     | Rate limits, conflict resolution, multi-currency, partial payments |
| 45-60 | Build sequence + timeline       | Which pipeline first, dependencies, testing approach  |

**What Architect brings:**

- Data mapping matrix (for context)
- Draft tech spec (from 2a)
- Known edge cases: international addresses, special characters, multi-currency scenarios

**What engineer leaves with:**

- Approved tech spec with build sequence
- Clear understanding of data governance rules (what overrides what)
- Known risks: API rate limits, data volume estimates, concurrent update scenarios
- Test data specifications (sample records for each scenario)

---

### 2c. Build (Configure)

> **Purpose:** Build integration pipelines in the middleware/iPaaS platform.

**Input:** Approved tech spec from 2b

**Build sequence:**

**Pipeline 1: Account/Customer Sync (build first — foundational)**
- [ ] Configure API connections to CRM and ERP (OAuth/token-based authentication)
- [ ] Create integration user accounts with least-privilege permissions in both systems
- [ ] Build trigger logic: sync on account creation and specified field updates (billing address, payment terms)
- [ ] Implement field transformations: state/country standardization, address formatting, required field defaults
- [ ] Configure duplicate detection using matching rules (company name, domain, tax ID)
- [ ] Build merge/update logic for existing customers vs new customer creation
- [ ] Test with 10-15 sample accounts (new, update, international, special characters)

**Pipeline 2: Opportunity/Sales Order Sync (build second — highest value)**
- [ ] Build trigger on Opportunity Stage = Closed Won
- [ ] Map opportunity line items to ERP sales order line items (product, quantity, price, discount)
- [ ] Handle multi-currency with exchange rate logic
- [ ] Implement pre-sync validation: verify customer exists in ERP, create if missing (uses Pipeline 1)
- [ ] Build approval workflow for discounts exceeding ERP policy thresholds
- [ ] Test with opportunities: single line, multi-line, discounted, various currencies

**Pipeline 3: Invoice/Payment Status Sync (build third — reverse flow)**
- [ ] Create custom fields in CRM: Invoice Status, Invoice Number, Payment Status, Outstanding Balance
- [ ] Build trigger on ERP invoice creation and payment posting events
- [ ] Map invoice data to CRM opportunity and account records
- [ ] Handle partial payments and credit memos
- [ ] Test with invoices: pending, sent, partial payment, paid in full, overdue

**Cross-pipeline configuration:**
- [ ] Configure API throttling to stay within rate limits (batch requests, queue management)
- [ ] Set up error handling: retry logic (3 retries with exponential backoff), failure notifications (email/alert)
- [ ] Configure data validation layer (required fields, format checks, referential integrity)
- [ ] Build manual override capability for failed records

**Execution approach for this project:**

| Approach       | When to Use                                        | Example                                    |
| -------------- | -------------------------------------------------- | ------------------------------------------ |
| Manual build   | First CRM-ERP integration for this client/ERP combo | Engineer builds in middleware directly     |
| Template-based | Standard CRM-ERP combo with mature templates       | Pre-built Celigo/Workato templates         |

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify all sync pipelines work and get customer approval.

**Two types of testing:**

| Type              | Who      | Purpose                                              |
| ----------------- | -------- | ---------------------------------------------------- |
| Technical Testing | Our team | Verify sync fires, data maps correctly, errors handled |
| Customer Testing  | Customer | Verify data accuracy meets business needs            |

**Technical testing checklist:**

Unit Testing:
- [ ] Account/Customer sync: new accounts, updates, international addresses, special characters, duplicate detection
- [ ] Opportunity/Sales Order sync: single and multi-line items, discounts, multi-currency, missing customer scenario
- [ ] Invoice/Payment sync: all invoice states (pending, sent, partial, paid, overdue), credit memos

Integration Testing (end-to-end):
- [ ] Full flow: create opportunity → close won → verify sales order in ERP → create invoice → post payment → verify CRM update
- [ ] Test with realistic volume (50-100 records) to identify performance issues
- [ ] Error scenarios: API timeout, duplicate record, missing required field, rate limit hit
- [ ] Verify error handling: alerts fire, records queue for retry, manual override works
- [ ] Concurrent update test: same record updated in both systems simultaneously — verify conflict resolution

Pilot Validation:
- [ ] Select pilot group: 10-20 accounts (mix of new and existing, domestic and international)
- [ ] Deploy for pilot accounts with manual monitoring
- [ ] Run parallel operation for 1-2 weeks: continue manual process alongside integration
- [ ] Compare integration results vs manual process — catch discrepancies
- [ ] Expand to full account base after pilot validation (2-3 waves)

**Customer testing:**

- Walk Sales team through: closed opportunity → sales order auto-creation in ERP
- Walk Finance team through: invoice status visibility in CRM, payment data accuracy
- Demonstrate exception handling and manual override for sync failures
- Collect feedback and document change requests

**Engineering sign-off checkpoint:**

- [ ] All three sync pipelines tested and passing
- [ ] Error handling verified (retries, alerts, manual override)
- [ ] Pilot validation complete — integration matches or exceeds manual accuracy
- [ ] Monitoring dashboard configured and operational
- [ ] Customer has tested and approved
- [ ] Ready for enablement

**Decision point:**

- **Proceed to Enablement** → All pipelines working, pilot validated, monitoring in place
- **Loop back to Build** → Issues found in pilot, needs fixes before wider rollout

---

## Phase 3: Enablement

> **Goal:** Sales, Finance, and RevOps teams can operate with the integrated workflow and know what changed.
>
> **Output:** Trained teams, documentation delivered, system stabilized through hypercare.

### Sub-Phases

```
3a Training Prep → 3b Training Sessions → 3c Hypercare → 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials tailored to each audience (Sales, Finance, Technical).

**Input:** Data mapping matrix + tech specs + built system + monitoring dashboard

**Output:** Training package containing:

- **Sales training deck:** What syncs automatically, what they see in CRM (invoice status, payment status), what they no longer need to do manually, how to check if a record synced
- **Finance training deck:** How sales orders appear in ERP, data accuracy expectations, exception handling process, how to trigger manual re-sync
- **Technical admin guide:** Monitoring dashboard navigation, error triage process, API credential rotation, change procedures, alert response
- **Video walkthrough scripts:** Separate recordings for each audience
- **FAQ draft:** Based on common questions from similar CRM-ERP integration projects

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to Sales, Finance, and RevOps teams.

**Three training sessions:**

| Type       | Audience                      | Focus                                                              | Duration |
| ---------- | ----------------------------- | ------------------------------------------------------------------ | -------- |
| Sales      | VP Sales, AEs, Sales Managers | What changed: invoice/payment visibility in CRM, what to stop doing manually, how to spot sync issues | 30 min   |
| Finance    | Finance Controller, AR team   | What changed: auto-generated sales orders, data accuracy, exception handling, manual override | 45 min   |
| Technical  | RevOps Admin, IT              | How to maintain: monitoring, error triage, credential rotation, escalation procedures | 60 min   |

**Training delivery:**

1. Schedule sessions with appropriate stakeholders (separate sessions — Sales and Finance have different needs)
2. Deliver training live with screen shares of actual integrated system
3. Record video walkthroughs for future reference and onboarding new team members
4. Answer questions, note gaps — feed into FAQ

**Output:**

- Trained stakeholders who understand what changed and what to do
- Video walkthrough recordings (3 separate recordings by audience)
- Questions log (feeds into FAQ and troubleshooting runbook)

---

### 3c. Hypercare

> **Purpose:** Intensive post-launch support to stabilize the integration and catch issues early.

**Duration:** 2 weeks

**Week 1 (Intensive):**
- Daily 15-minute sync review meeting with technical team
- Monitor all sync pipelines in real-time
- Triage issues: critical/blocking vs minor
- Fix critical issues immediately; queue minor issues
- Document edge cases discovered in production

**Week 2 (Reduced):**
- 2x per week sync review (Monday/Thursday)
- Review weekly sync metrics: records synced, failed, pending
- Adjust sync frequency or throttling if performance issues arise
- Finalize any outstanding minor fixes

**What to watch for during hypercare:**
- Sync failures spiking above baseline
- Data discrepancies reported by Sales or Finance
- API rate limit warnings approaching threshold
- New edge cases not covered in testing (unusual product configs, non-standard payment terms)

**When to skip:** Never for CRM-ERP integration. This is a technical project with multiple data flows — hypercare is required.

**Output:** Stabilized integration with no critical issues, all edge cases documented

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm customer can operate independently with the integrated system.

**Validation checkpoint:**

- [ ] All three training sessions delivered (Sales, Finance, Technical)
- [ ] Training video walkthroughs recorded and distributed
- [ ] Troubleshooting runbook delivered
- [ ] Hypercare period complete — no critical issues outstanding
- [ ] Monitoring dashboard reviewed and understood by RevOps/IT
- [ ] Customer team can check sync status, identify failures, and escalate appropriately
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** → System stable, team enabled, no critical issues
- **Extend Hypercare** → Still seeing sync failures or team not confident in monitoring

---

## Phase 4: Handoff

> **Goal:** Clean project close with maintenance plan established and retention/expansion path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the system, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule → 4b Internal Handoff → 4c External Handoff → 4d Project Close
                          (SME → Architect)       (to Customer)        (Archive + Debrief)
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At                                                                         |
| ----------------------------- | -------------------- | ------------------------------------------------------------------------------------- |
| **Single Project**            | Customer owns        | 4c (External Handoff) — customer receives maintenance schedule and runs it themselves |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) — Architect receives maintenance schedule and runs it for customer |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention after the integration is live — cadences, tasks, triggers for re-engagement.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task               | What to Check                                       | Red Flag Threshold                                |
| -------------------------- | --------------------------------------------------- | ------------------------------------------------- |
| Sync Health Review         | Records synced/failed/pending by pipeline, error rates | Failure rate >2% or any pipeline down >4 hours   |
| Data Quality Spot-Check    | Sample 20 recently synced records for accuracy      | >5% mismatch rate between CRM and ERP             |
| API Usage Monitoring       | API call volume vs rate limits per system            | Usage >80% of rate limit threshold                |
| Sync Latency Check         | Time between trigger event and sync completion       | Latency >2x agreed SLA (e.g., >30 min for real-time) |

**Quarterly Tasks:**

| Quarterly Task               | What to Review                                        | Action if Off-Track                              |
| ---------------------------- | ----------------------------------------------------- | ------------------------------------------------ |
| Full Data Mapping Validation | Walk through field mapping — any new fields added? Any deprecated? | Update mapping matrix and sync configuration    |
| Performance Review           | Sync volumes, error trends, user-reported issues      | Adjust throttling, add error handling for new edge cases |
| Data Governance Audit        | Is system-of-record still respected? Any workarounds? | Retrain team, enforce governance rules           |
| API Credential Rotation      | Rotate integration user credentials per security policy | Update middleware config, test connectivity      |

**After First Business Cycle (30-60 days post-launch):**

- Full sync accuracy audit: compare 100 records end-to-end (opportunity to invoice to CRM status)
- Volume validation: is the system handling actual production volume without performance degradation?
- User adoption check: are Sales and Finance actually relying on synced data, or reverting to manual?
- Key question: Is the order-to-cash cycle actually faster? Measure and compare to pre-integration baseline.

**Refinement Triggers (when to re-engage):**

| Trigger                       | Threshold                           | Response                                               |
| ----------------------------- | ----------------------------------- | ------------------------------------------------------ |
| Sync failure spike            | >5% failure rate for 3+ consecutive days | Investigate root cause, fix, update error handling    |
| New ERP/CRM object needed     | Business adds new product line, entity, or process | Scope mapping extension, build new sync pipeline      |
| API version deprecation       | Vendor announces API version sunset  | Plan migration before deprecation date                |
| Data quality degradation      | >10% mismatch rate on monthly spot-check | Re-run data quality audit, remediate, retrain users   |
| System upgrade                | CRM or ERP major version upgrade     | Test integration in sandbox, update configs if needed |

**Every 6-12 Months:**

- Full integration health assessment: architecture review, performance benchmarking, vendor roadmap alignment
- Evaluate new integration capabilities from middleware/iPaaS vendor (new connectors, AI features)
- Review data governance policies against any compliance changes (GDPR updates, SOC2 controls)
- Assess whether sync scope should expand (new objects, new systems, new business processes)

---

### 4b. Internal Handoff (SME to Architect)

> **Purpose:** Transfer context so Architect can manage ongoing relationship.

**What the Architect needs to know:**

- Integration architecture: what tools connect what systems, and how
- Data mapping decisions: why certain fields sync in certain directions (strategic context behind technical choices)
- Known edge cases: multi-currency handling, international address formatting, partial payment scenarios
- Common issues: which sync pipelines are most fragile, typical failure causes and fixes
- When to escalate back to SME
- **Maintenance schedule** (if Dedicated engagement — Architect runs this)

**Escalation guidelines:**

| Issue Type                                       | Who Handles  | Example                                              |
| ------------------------------------------------ | ------------ | ---------------------------------------------------- |
| Sync failure for known error type                | Architect    | Retry failed record, check error log, apply known fix |
| New field mapping request                        | Architect    | Add field to mapping, configure in middleware        |
| Sync logic change (new trigger, new pipeline)    | SME          | Changing what triggers sync or adding new object type |
| API version migration                            | SME          | Vendor deprecates API, need to migrate integration   |
| Architecture change (new middleware, new system)  | SME          | Switching tools or adding third system to integration |

**For Dedicated engagements:** Architect also receives the maintenance schedule (4a) and becomes responsible for executing it. SME walks Architect through each maintenance task and known failure patterns.

---

### 4c. External Handoff (to Customer)

> **Purpose:** Formal project completion with customer.

**Final project meeting:**

- Review what was delivered: 3 sync pipelines, monitoring dashboard, documentation package
- Walk through monitoring dashboard: how to check sync status, how to spot failures
- Walk through troubleshooting runbook: common issues and resolution steps
- Confirm nothing outstanding from hypercare
- Answer final questions
- Make it explicit: "Project complete"
- **For Single Project engagements:** Hand over the maintenance schedule (4a) and walk the customer through every task

**Documentation package:**

- Integration architecture diagram (data flow between CRM, middleware, ERP)
- Data mapping matrix (final version with all fields, transformations, sync directions)
- Troubleshooting runbook (scenario + resolution tables for common issues)
- Admin guide (API credential rotation, monitoring procedures, change management)
- Training video walkthroughs (Sales, Finance, Technical — 3 separate recordings)
- Definition Alignment Document (final version)
- FAQ document
- Maintenance schedule (monthly/quarterly task tables)
- Support contact info and escalation path

**For Single Project engagements:** Walk the customer through the maintenance schedule in detail. Record a video walkthrough of the session. Make sure they understand: what to check, how often, and when to re-engage.

**Output:** Customer owns the integration. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved (data mapping, architecture spec, tech spec, test results)
- [ ] Handoff documentation complete and delivered
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized

#### Internal Debrief (Optional but Recommended)

- What went well? (data mapping process, tool selection, pilot approach)
- What would we do differently? (data quality issues caught late, stakeholder scheduling delays)
- Any learnings to feed back into SOPs? (new edge cases, improved error handling patterns)
- How long did each phase actually take vs estimate? (calibrate future scoping)

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell → Downsell → Retry    |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (ongoing monitoring + integration optimization)
   | if no
2. Downsell: Related project (reporting/BI dashboards, lead lifecycle, CPQ integration)
   | if yes
3. Retry retainer at end of next project cycle
```

**Script:**

> "Now that the CRM-ERP integration is live and stable, there are two ways we can continue working together. Option 1: We handle ongoing monitoring and optimization — catching sync issues before they impact your team, and expanding the integration as your needs grow. Option 2: If there's another project you need help with — like building the reporting layer on top of this integrated data, or automating your quote-to-cash process — we can scope that out. Which sounds more interesting?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On [date ~quarter out], we'll review how the integration is performing — sync accuracy, volume trends, any new use cases — and see if adjustments are needed."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                                    |
| ------------------- | --------------------------------------------------------------- |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks                |
| 2. Review metrics   | Pull sync metrics, error rates, user feedback                   |
| 3. Decide ownership | Can Architect handle this check-in, or need SME?               |
| 4. Prep materials   | If SME needed, brief them. If Architect, prep talking points.   |

**At the refinement check-in:**

- Review sync performance against original success criteria
- Identify any new integration needs (new fields, new objects, new systems)
- If minor: Architect handles configuration tweaks
- If major: Scope new project (e.g., adding CPQ integration, BI layer)

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- Data Mapping Matrix (field-level mapping between CRM and ERP with sync direction and transformation rules)
- Integration Architecture Spec (tool selection, authentication, sync frequency, error handling design)
- Data Governance Rules (system of record per data type, conflict resolution policies)
- Definition Alignment Document (stakeholder-approved terms and definitions)

**Technical Deliverables:**

- Account/Customer sync pipeline (CRM to ERP, bi-directional updates)
- Opportunity/Sales Order sync pipeline (CRM Closed-Won to ERP sales order)
- Invoice/Payment status sync pipeline (ERP to CRM reverse flow)
- Monitoring dashboard (sync status, error rates, API usage)
- Error handling configuration (retry logic, alerts, manual override)
- Data validation layer (format checks, required fields, referential integrity)

**Documentation Package:**

- Training video walkthroughs (Sales, Finance, Technical — 3 separate recordings)
- Integration architecture diagram
- Field mapping reference (1-page quick reference)
- Troubleshooting runbook
- Admin guide (credential rotation, monitoring, change procedures)
- FAQ document
- Definition Alignment Document (final version)
- Maintenance Schedule

---

## Appendix

### Roles

| Role | What They Do |
|---|---|
| **Architect** | Owns the customer relationship, leads strategy, creates specs, does enablement, owns account post-delivery |
| **Engineer** | CRM build, automation, dashboards (Phase 2) |
| **SME** | Project/implementation team brought in for project-specific work |

### What Each Phase Produces

| Phase                    | Output                                                                 | Gate Criteria                                                                  |
| ------------------------ | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **Phase 1: Strategy**    | Signed-off data mapping + architecture spec + data governance rules    | VP Sales, Finance Controller, and RevOps Lead have approved all strategic documents |
| **Phase 2: Engineering** | 3 sync pipelines built, tested, and pilot-validated                    | All pipelines passing, pilot validation complete, monitoring operational       |
| **Phase 3: Enablement**  | Trained Sales, Finance, and Technical teams with documentation         | All training delivered, hypercare complete, team can operate independently     |
| **Phase 4: Handoff**     | Independent customer + archived project                                | Internal/external handoffs complete, maintenance plan in place, project closed |

### How to Adapt Per Project Type

CRM-ERP Integration is an **engineering-heavy** project:

| Project Profile       | Strategy Weight | Engineering Weight | Enablement Weight |
| --------------------- | --------------- | ------------------ | ----------------- |
| Strategic-heavy       | 60-80%          | 10-20%             | 10-20%            |
| **Engineering-heavy** | **15-20%**      | **60-70%**         | **15-20%**        |
| Enablement-heavy      | 20-30%          | 20-30%             | 40-50%            |
| Balanced              | 30-40%          | 30-40%             | 20-30%            |

### Engagement Types

| Engagement Type               | What It Means                        | Key Difference                              |
| ----------------------------- | ------------------------------------ | ------------------------------------------- |
| **Single Project**            | One-off CRM-ERP integration          | Customer owns monitoring and maintenance post-handoff (4c) |
| **Dedicated (Multi-Project)** | Ongoing retainer / multiple projects | Architect owns monitoring and maintenance post-handoff (4b) |

### Key Statistics and Benchmarks

- 91% of CRM data is incomplete, and 70% of that data deteriorates annually [1] — data cleansing before integration is not optional
- Organizations achieve 40% faster deal cycles and 25% faster revenue recognition after implementing quote-to-cash automation [2]
- O2C automation improves end-to-end cycle time by up to 60% [3]
- One electronics OEM reduced quote-to-cash from 18 days to 6 days (-66%) after CRM-ERP integration, with sales conversion rising 22% [2]
- 94% of companies do not believe in the accuracy of their customer and prospect data [4]
- Poor data quality costs organizations an average of $15 million annually [6]
- 37% of teams report losing revenue as a direct consequence of poor data quality [7]
- Median timeline for ERP integration projects is 15.5 months from kickoff to final go-live [8] — CRM-ERP integration (a subset) typically runs 6-12 weeks for mid-market

### References

[1] [Salesforce — CRM Data Quality Statistics](https://www.salesforce.com/resources/research-reports/state-of-sales/)

[2] [Webvillee — CRM ERP Integration Quote to Cash: Stop Revenue Leakage](https://webvillee.com/blogs/quote-to-cash-optimization-how-crm-erp-integration-eliminates-revenue-leakage/)

[3] [HighRadius — Order to Cash Process Optimization](https://www.highradius.com/resources/Blog/order-to-cash-process-optimization/)

[4] [Experian — Data Quality Research](https://www.experian.com/business/resources/data-quality)

[5] [Scratchpad — CRM Data Quality](https://www.scratchpad.com/blog/crm-data-quality)

[6] [Gartner — Data Quality Cost Study](https://www.gartner.com/en)

[7] [Validity — State of CRM Data Management 2025](https://www.validity.com/blog/data-quality-management/)

[8] [Panorama Consulting Group — 2024 ERP Report](https://www.panorama-consulting.com/resource-center/erp-report/)
