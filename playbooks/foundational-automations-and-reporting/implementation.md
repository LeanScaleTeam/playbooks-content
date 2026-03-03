# Foundational Automations and Reporting Logic — Implementation

---

## Project One-Pager

### Foundational Automations and Reporting Logic One-Pager

#### Project Type

- Category: Technical
- Primary Deliverable: Working CRM automation workflows (lead capture, lifecycle stages, task assignment, renewal reminders) and reporting infrastructure (pipeline dashboards, CAC/CLV metrics, churn monitoring)

##### Phase Relevance

| Phase          | Applies? | Weight | Notes                                                     |
| -------------- | -------- | ------ | --------------------------------------------------------- |
| 1. Strategy    | Yes      | Medium | Audit current state, define system ownership, gather requirements across Sales/Marketing/CS |
| 2. Engineering | Yes      | Heavy  | Core of the project -- build all automation flows and reporting dashboards in CRM |
| 3. Enablement  | Yes      | Medium | Train RevOps, Sales, Marketing, CS on automation monitoring and dashboard usage |
| 4. Handoff     | Yes      | Medium | Internal + External with admin runbook and maintenance schedule |

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────>│ 2. ENGINEER  │────>│3. ENABLEMENT │────>│  4. HANDOFF  │
  │    Medium    │     │    Heavy     │     │    Medium    │     │    Medium    │
  │ 1a->1b->1c->1d │  │ 2a->2b->2c->2d │  │ 3a->3b->3c->3d │  │ 4a->4b->4c->4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   Audit & Align        Build Automations    Train Stakeholders   Document & Transfer
   Requirements          + Reporting Infra    on Dashboards        Ownership
```

**This project's flow:**
- Full 4-phase. Medium strategy (audit-heavy), heavy engineering (automation + reporting build), medium enablement (multi-stakeholder training), medium handoff (admin documentation + maintenance schedule).
- Phase 2 is the majority of effort -- building 15-20+ automation flows and 10+ reports/dashboards across Sales, Marketing, and CS functions.
- Phase 1 may compress if the client has well-documented current state and clear requirements.

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Complete automation inventory spreadsheet (list all existing automations with status: working, broken, deprecated)
- [ ] Document current lead assignment rules (territories, round-robin logic, fallback rules)
- [ ] Provide lifecycle stage definitions for Lead, Contact, Account, and Opportunity objects
- [ ] Identify contract/renewal date field locations and formats
- [ ] Share marketing spend data for CAC calculation (by channel if available)
- [ ] Grant CRM admin access (Salesforce or HubSpot) with permissions to create automations and reports

##### Track B: Architect Prep
- [ ] Pull automation audit from Salesforce Setup > Process Automation or HubSpot Workflows
- [ ] Run report inventory export from CRM (all reports and dashboards with last accessed dates)
- [ ] Identify deprecated automations (Process Builders, Workflow Rules) needing migration to Flow
- [ ] Map data objects between Salesforce and HubSpot (if dual-system)
- [ ] Create v0 system ownership model draft based on CRM configuration

#### Refinement Loop (1b -> 1c -> 1d)

| Meeting      | Sub-Phase | Focus                                                       | Stakeholder                      | Output                            |
| ------------ | --------- | ----------------------------------------------------------- | -------------------------------- | --------------------------------- |
| Kickoff      | 1b        | Present audit findings, validate system ownership model     | RevOps Lead, VP Sales, VP Mktg  | Validated requirements for v1     |
| Refinement 1 | 1c        | Review automation logic designs, lead assignment rules      | RevOps Lead, Sales Ops           | Approved automation specifications|
| Refinement 2 | 1c        | Review reporting requirements, dashboard layouts, KPI defs  | VP Sales, VP Mktg, CS Leadership | Approved reporting specifications |
| Sign-Off     | 1d        | Final review of all specs before engineering begins         | All stakeholders                 | Signed-off strategic package      |

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held -- audit findings presented, system ownership validated
- [ ] 1c. Refinement loop complete (automation specs + reporting specs approved)
- [ ] 1d. Strategic sign-off obtained from RevOps Lead and executive stakeholders

##### Phase 2: Engineering
- [ ] 2a. Tech spec created (automation flow diagrams, field mapping, report calculations)
- [ ] 2b. Engineering handoff meeting held
- [ ] 2c. Build complete (all automations + all reports/dashboards)
- [ ] 2d. QA/Test + customer sign-off (automations running error-free, reports showing accurate data)

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped (admin runbook, dashboard usage guides, video walkthrough scripts)
- [ ] 3b. Training sessions delivered (Leadership + Technical)
- [ ] 3c. Hypercare period complete (2 weeks monitoring automation errors and report accuracy)
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff (SME -> Architect) complete
- [ ] 4c. External handoff (LS -> Customer) complete
- [ ] 4d. Project closed and archived

#### Document Types

##### Working Documents (iterate together)

| Document                        | Purpose                                            | When Complete                                  |
| ------------------------------- | -------------------------------------------------- | ---------------------------------------------- |
| Automation Inventory Spreadsheet | Catalog all existing automations with status flags | All automations audited and categorized        |
| System Ownership Model          | Define source of truth per data type and sync rules | Stakeholder sign-off on ownership + sync rules |
| Field Mapping Document          | Map fields between systems (SFDC &lt;-> HubSpot)      | All fields mapped with sync direction defined  |
| Report Requirements Matrix      | List all required reports by function and KPIs     | All reports specified with data sources         |

##### Deliverables (polished outputs)

| Deliverable                     | Created From                   | Customer Uses For                      |
| ------------------------------- | ------------------------------ | -------------------------------------- |
| Automation Flow Diagrams        | Automation inventory + specs   | Internal documentation and onboarding  |
| Dashboard Organization Map      | Report requirements matrix     | Understanding where to find reports    |
| Admin Runbook                   | Build documentation            | Self-service maintenance and troubleshooting |

#### Enablement Details

##### Training Types

| Type       | Audience                        | Focus                                              | Duration |
| ---------- | ------------------------------- | -------------------------------------------------- | -------- |
| Leadership | VP Sales, VP Marketing, CS Lead | Interpret dashboards, identify action items from data | 30 min   |
| Technical  | RevOps Lead, CRM Admin          | Monitor automations, troubleshoot errors, modify reports | 60 min   |
| End User   | Sales Reps, CSMs                | Use dashboards for daily work, understand lifecycle stages | 30 min   |

##### Hypercare
- Applies: Yes
- Duration: 2 weeks
- Office Hours: Yes -- weekly 30-min slot for questions on automation errors or report accuracy

##### Training Assets to Create
- [ ] Video walkthrough: Dashboard navigation (Sales, Marketing, CS, Executive dashboards)
- [ ] Video walkthrough: Automation monitoring -- how to check for errors in Salesforce Flow or HubSpot Workflows
- [ ] Doc: Field mapping reference (source of truth for each field)
- [ ] Doc: Report calculation reference (how CAC, CLV, and churn are calculated)
- [ ] Doc: Admin runbook (troubleshooting common automation issues)

#### Handoff & Retention

##### Internal Handoff (SME -> Architect)
- Key context for Architect: Which automations are most likely to break (lifecycle stage transitions, sync conflicts), where to find error logs, and which reports leadership relies on most
- Escalation trigger: Any changes to lifecycle stage definitions, addition of new lead sources, or modifications to CAC/CLV calculation logic

##### External Handoff (LS -> Customer)
- Final meeting agenda: Review all automation flows, walk through dashboard suite, confirm admin runbook accuracy, transfer admin credentials
- Documentation package: Admin runbook, field mapping doc, report calculation reference, training video walkthroughs, maintenance schedule

##### Maintenance Schedule
- Monthly: Check automation error logs, verify stage hit dates populating, review dashboard accuracy
- Quarterly: Audit for new automation conflicts, validate report calculations against known data, review report folder organization
- Who owns: Single project = customer owns | Dedicated = Architect owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services -> if no -> Downsell: Lead Scoring Model, Attribution, or Executive Reporting Suite -> Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~90 days post-launch
- Internal prep trigger: 2 weeks before
- Decision: Architect handles / SME needed

#### Key Assets

| Asset                           | When Used          |
| ------------------------------- | ------------------ |
| Automation Inventory Template   | Phase 1a (audit)   |
| System Ownership Model Template | Phase 1a-1c        |
| Field Mapping Template          | Phase 1c-2a        |
| Report Requirements Matrix      | Phase 1c           |
| Admin Runbook Template          | Phase 3a           |

#### Definition Alignment Terms

| Term                    | Typical Definition                                                                             |
| ----------------------- | ---------------------------------------------------------------------------------------------- |
| Lead Lifecycle Stage    | The progression stages a Lead record moves through: New, Contacted, Qualified, Converted, Disqualified |
| Stage Hit Date          | A custom date/time stamp field that records when a record first enters a specific stage         |
| System of Record (SoR)  | The authoritative system for a given data type -- where the "truth" lives                      |
| Sync Direction          | Whether data flows one-way (SFDC -> HubSpot) or bidirectional between systems                  |
| CAC                     | Customer Acquisition Cost -- total sales + marketing spend divided by new customers acquired    |
| CLV                     | Customer Lifetime Value -- average revenue per customer multiplied by average customer lifespan |
| Churn Rate              | Percentage of customers lost in a given period (monthly or quarterly)                          |
| Flow (Salesforce)       | Salesforce's current automation tool, replacing deprecated Process Builders and Workflow Rules  |

#### Common Gotchas
- Building new automations without deactivating deprecated Process Builders/Workflow Rules causes duplicate processing -> Deactivate old automations BEFORE activating new Flows
- Sync conflicts between Salesforce and HubSpot when system ownership is undefined -> Define and get sign-off on System Ownership Model in Phase 1 before any automation build
- Reports showing incorrect data because underlying automation fields are not populating -> Test each automation end-to-end before building reports that depend on its data
- Picklist value mismatches between systems causing sync errors -> Standardize picklist values across systems during field mapping in Phase 1
- Salesforce Flow governor limits hit on high-volume record processing -> Use batch processing and optimize Flow logic for objects with >10,000 records
- Forgetting to add date/time stamp fields before building lifecycle automations -> Create all custom fields first, then build the Flows that populate them

#### Methodology Options

| Option                 | When to Use                                           | Complexity |
| ---------------------- | ----------------------------------------------------- | ---------- |
| Single-CRM (SFDC only) | Client uses Salesforce only, no HubSpot integration   | Low        |
| Single-CRM (HS only)   | Client uses HubSpot only, no Salesforce integration   | Low        |
| Dual-CRM (SFDC + HS)   | Client uses both systems with integration/sync        | High       |

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on what automations and reports we are going to build, including system ownership model, lifecycle stage definitions, and reporting requirements.
>
> **Output:** Definition Alignment Document + Automation Specifications + Report Requirements Matrix (signed off by stakeholders).

### 1a. Pre-Kickoff

> Two parallel tracks run after the deal closes and before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                           | Purpose                                                  | Format             |
| ------------------------------ | -------------------------------------------------------- | ------------------ |
| Intro video                    | Explain the project scope: automations + reporting build | Video walkthrough (5-10 min) |
| Definition Alignment Document  | Get sign-off on lifecycle stages, KPI definitions         | Google Doc         |
| Automation Inventory Template  | Client fills in known automations and their status        | Google Sheet       |
| Pre-filled intake form         | Confirm lead assignment rules, renewal fields, spend data | Google Form or Doc |

**Completion tracking:** RevOps Lead follows up. Do not cancel kickoff if incomplete, but push hard for automation inventory and CRM admin access -- these are blockers.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                                 | Output                                    |
| ---- | ---------------------------------------------------------------------- | ----------------------------------------- |
| 1    | Pull automation list from CRM Setup (Flows, Process Builders, WFRs)    | Raw automation inventory with status flags |
| 2    | Export report/dashboard list with last accessed dates                   | Report inventory with quality ratings     |
| 3    | Identify deprecated automations needing migration                      | Migration candidate list                  |
| 4    | Draft System Ownership Model (which system owns which data)            | v0 ownership model                        |
| 5    | Prepare kickoff assets: audit summary, gap analysis, questions list    | Kickoff presentation materials            |

**Critical:** Mark everything as ASSUMED. The kickoff call validates. The automation audit is especially important -- sales reps spend only 28% of their time selling, with the rest consumed by administrative tasks [1]. This project directly attacks that problem by automating the manual work.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building anything.

| Term                   | Our Definition                                                                          | Internally Approved? |
| ---------------------- | --------------------------------------------------------------------------------------- | -------------------- |
| Lead Lifecycle Stages  | New -> Contacted -> Qualified -> Converted -> Disqualified                               | [ ] Yes / [ ] No     |
| Contact Lifecycle      | Active -> Engaged -> Customer -> Churned                                                 | [ ] Yes / [ ] No     |
| Account Lifecycle      | Prospect -> Customer -> Churned -> Partner                                               | [ ] Yes / [ ] No     |
| Opportunity Stages     | [Client-specific: e.g., Discovery -> Qualification -> Proposal -> Negotiation -> Closed] | [ ] Yes / [ ] No     |
| System of Record       | Salesforce = source of truth for [X], HubSpot = source of truth for [Y]                  | [ ] Yes / [ ] No     |
| CAC Formula            | (Total Sales Spend + Total Marketing Spend) / New Customers in Period                    | [ ] Yes / [ ] No     |
| CLV Formula            | Average Revenue Per Customer x Average Customer Lifespan                                 | [ ] Yes / [ ] No     |
| Churn Definition       | Contract cancellation, non-renewal, or downgrade below [threshold]                       | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your leadership team. Check "Yes" when approved. We cannot proceed with automation builds until lifecycle stages and KPI definitions are aligned.

---

### 1b. Kickoff Call

> **Purpose:** Present audit findings and v0 System Ownership Model. We walk in with work done -- customer reacts, not creates from scratch.

#### Agenda (60-90 min)

| Time  | Topic                        | What Happens                                                 |
| ----- | ---------------------------- | ------------------------------------------------------------ |
| 0-15  | Automation audit walkthrough | "Here's what we found: X working, Y broken, Z deprecated"   |
| 15-25 | System Ownership Model       | Present v0 ownership model, validate or correct              |
| 25-40 | Lifecycle stage definitions  | Review Lead, Contact, Account, Opportunity stage definitions |
| 40-50 | Lead assignment rules        | Confirm territories, round-robin logic, fallback rules       |
| 50-60 | Reporting requirements       | Initial discussion: what dashboards does leadership need?    |
| 60+   | Next steps                   | Schedule refinement meetings, assign homework                |

#### What We Bring

- Automation audit summary (working / broken / deprecated counts by object)
- v0 System Ownership Model
- Report inventory with gap analysis
- Definition Alignment Document (pre-filled with recommendations)
- Questions list (what we need to validate)

#### What We Leave With

- Validated system ownership decisions (or clear blockers needing executive input)
- Corrections on lifecycle stage definitions
- Confirmed lead assignment rules
- Initial reporting priorities ranked by stakeholder
- Clear homework assignments (theirs and ours)

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Iterate on automation specifications and reporting requirements until sign-off.

#### The Pattern

```
Kickoff Call (audit findings + initial requirements)
    |
Architect processes info -> v1 automation specs + report requirements
    |
Meeting 2 (review automation specs) -> updates -> v2
    |
Meeting 3 (review reporting specs) -> updates -> v3
    |
Final Review -> Sign-off
```

#### Before Each Meeting

1. Process previous meeting transcript/notes
2. Update automation specifications and reporting requirements
3. Prepare questions for next validation round

#### During Each Meeting

1. Walk through current version of specs
2. Capture corrections and refinements
3. Validate what is now CONFIRMED
4. Identify remaining ASSUMED items

#### After Each Meeting

1. Update automation specs and reporting matrix
2. Track what moved from ASSUMED -> CONFIRMED
3. Update working documents

#### Meeting Types for This Project

| Meeting Type            | Focus                                                    | Stakeholder                         |
| ----------------------- | -------------------------------------------------------- | ----------------------------------- |
| Automation Review       | Lead capture, assignment, lifecycle, renewal automation  | RevOps Lead, Sales Ops              |
| Reporting Review        | Pipeline, CAC, CLV, churn, campaign dashboards           | VP Sales, VP Marketing, CS Lead     |
| Data Validation         | Field mapping, sync rules, picklist standardization      | RevOps Lead, CRM Admin              |
| Final Review            | Full walkthrough of all specs, sign-off                  | All stakeholders                    |

#### Typical Timeline

| Milestone               | Timing                                          |
| ----------------------- | ----------------------------------------------- |
| Pre-kickoff prep        | 2-3 days                                        |
| Kickoff call            | Day 1 of engagement                             |
| Refinement meetings     | 1-2 weeks (2-3 meetings)                        |
| Final review + sign-off | When all automation + reporting specs CONFIRMED  |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything before proceeding to engineering.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by stakeholders
- [ ] System Ownership Model approved (source of truth per data type, sync direction)
- [ ] Lifecycle stage definitions confirmed for all objects (Lead, Contact, Account, Opportunity)
- [ ] Lead assignment rules documented and approved
- [ ] Reporting requirements matrix complete with KPI definitions and calculation formulas
- [ ] Field mapping document complete (if dual-CRM)
- [ ] All critical inputs CONFIRMED (vs ASSUMED)
- [ ] Customer understands what we are building
- [ ] No blockers for engineering

#### Decision Point

- **Proceed to Engineering** -> Customer wants automations built and reports configured (standard path for this project)
- **Phase 1 is not an exit point for this project type** -- the automation and reporting build IS the core deliverable. Strategy alone does not deliver value here.

---

## Phase 2: Engineering

> **Goal:** Build and test all automation workflows and reporting dashboards in the CRM based on approved specifications.
>
> **Output:** Working automation system + reporting infrastructure, tested and customer-approved.

This is the heaviest phase for Foundational Automations and Reporting Logic. Expect 60-70% of total project effort here. CRM automation reduces administrative tasks by up to 80%, allowing reps to spend more time selling [2] -- but only if the automations are built correctly and tested thoroughly.

| Project Type                    | Engineering Weight | This Project                              |
| ------------------------------- | ------------------ | ----------------------------------------- |
| Strategic-heavy (Growth Model)  | Light (10-20%)     | N/A                                       |
| **This project (Automations)**  | **Heavy (60-70%)** | **Core CRM automation + reporting build** |
| Balanced (Attribution)          | Medium (40-60%)    | N/A                                       |

### Sub-Phases

```
2a Tech Spec -> 2b Engineering Handoff -> 2c Build -> 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate approved automation specs and reporting requirements into technical build specifications.

**Input:** Signed-off automation specifications, reporting requirements matrix, System Ownership Model, field mapping document

**What happens:**

1. Translate automation logic into CRM-specific configurations (Salesforce Flow definitions or HubSpot Workflow configurations)
2. Output draft technical specification

**Output:** Draft tech spec containing:

- **Custom field specifications:** Object, field name, field type, API name, default value, help text
  - Stage hit date fields for each lifecycle stage (e.g., `Lead_Stage_Qualified_Date__c`)
  - Churn tracking fields, contract end date fields
- **Automation flow specifications:** Trigger object, trigger event, entry criteria, actions, error handling
  - Lead capture flows (form -> CRM with UTM capture)
  - Lead assignment flows (territory/round-robin logic with fallback)
  - Lifecycle stage automation flows (with date stamp population)
  - Task assignment flows (trigger events, templates, due dates)
  - Renewal reminder flows (90/60/30 day triggers)
  - Upsell detection flows (usage threshold triggers)
- **Report specifications:** Report type, filters, groupings, calculated fields, chart type
- **Dashboard specifications:** Components, layout, filters, refresh schedule
- **Build sequence:** What to build first (fields -> automations -> reports -> dashboards)

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs with engineer before building.

**Who attends:** Architect + Engineer (or engineering team)

**Agenda (30-45 min):**

| Time  | Topic              | What Happens                                                            |
| ----- | ------------------ | ----------------------------------------------------------------------- |
| 0-15  | Walk through specs | Architect explains strategic context + tech spec output                 |
| 15-30 | Engineer questions | Clarify governor limits, sync timing, optimization needs               |
| 30-45 | Refine and approve | Adjust specs for technical constraints, confirm build sequence          |

**What Architect brings:**

- Strategic package (lifecycle definitions, assignment rules, KPI formulas)
- Draft tech spec (from 2a)
- Questions list (anything flagged: governor limit concerns, sync timing, complex logic)

**What engineer leaves with:**

- Approved tech spec with build sequence
- Known risks: high-volume objects, complex assignment logic, dual-CRM sync timing
- Clear priority order: fields first -> lifecycle automations -> lead capture -> task automations -> renewal -> reports -> dashboards

---

### 2c. Build (Configure)

> **Purpose:** Build all automation workflows and reporting infrastructure in the CRM.

**Input:** Approved tech spec from 2b

**Build sequence (order matters):**

**Step 1: Create Custom Fields (all objects)**
- [ ] Lead lifecycle stage hit date fields (`Lead_Stage_New_Date__c`, `Lead_Stage_Qualified_Date__c`, etc.)
- [ ] Contact lifecycle stage hit date fields
- [ ] Account lifecycle stage hit date fields
- [ ] Opportunity stage hit date fields (one per stage)
- [ ] Stage duration formula fields (time in stage calculations)
- [ ] Churn tracking fields (churn reason, churn date)
- [ ] Contract end date field (if not already present)

**Step 2: Build Lead Capture Automations**
- [ ] Configure form-to-CRM integrations (HubSpot forms, Salesforce Web-to-Lead)
- [ ] Map form fields to CRM lead fields
- [ ] Set up UTM parameter capture for campaign attribution
- [ ] Configure lead source and campaign tracking
- [ ] Test each lead source with sample submissions

**Step 3: Build Lead Assignment Flows**
- [ ] Build assignment Flow/Workflow with territory + round-robin logic
- [ ] Configure fallback logic for unmatched leads
- [ ] Set up notification to assigned rep
- [ ] Build exception handling for leads that fail assignment
- [ ] Test across all rule scenarios

**Step 4: Build Lifecycle Stage Automations**
- [ ] Lead lifecycle Flow: stage transitions with date/time stamp population
- [ ] Contact lifecycle Flow: stage transitions with date/time stamps
- [ ] Account lifecycle Flow: stage transitions with date/time stamps
- [ ] Opportunity stage Flow: stage hit dates on stage change
- [ ] Stale opportunity alerts (time-in-stage exceeds threshold)
- [ ] Stage skip validation (if required)

**Step 5: Build Task Assignment Automations**
- [ ] Define trigger events (form fill, email open, website visit)
- [ ] Configure task templates with due dates
- [ ] Set task priority based on engagement level
- [ ] Build notification system for new tasks
- [ ] Create escalation logic for overdue tasks

**Step 6: Build Renewal & Customer Automations**
- [ ] Renewal reminder Flow: 90/60/30 day triggers based on contract end date
- [ ] Configure reminder recipients (Account Owner, CS Manager)
- [ ] Create Task or Email notifications for each reminder milestone
- [ ] Upsell detection automation (usage threshold triggers, if applicable)

**Step 7: Build Reports**
- [ ] Opportunity pipeline report by stage
- [ ] Stage conversion rate report (using stage hit dates)
- [ ] Average time-in-stage analysis
- [ ] Pipeline by rep/team/territory views
- [ ] CAC report with channel/campaign breakdowns
- [ ] CLV report by customer segment
- [ ] Monthly and quarterly churn rate reports
- [ ] Churn by reason/segment analysis
- [ ] Campaign conversion funnel report
- [ ] Campaign ROI calculation report

**Step 8: Build Dashboards**
- [ ] Sales Pipeline Dashboard (pipeline by stage, conversion rates, time-in-stage, pipeline by rep)
- [ ] Executive Dashboard (CAC, CLV, churn, pipeline health)
- [ ] Marketing Dashboard (campaign performance, lead source analysis, conversion funnels)
- [ ] CS Dashboard (renewal pipeline, churn trends, account health)

**Step 9: Organize Reports & Dashboards**
- [ ] Create folder structure: Sales / Marketing / CS / Executive
- [ ] Move all reports to appropriate folders
- [ ] Apply naming convention: `Function - Report Name - Timeframe`
- [ ] Set folder permissions by role/team
- [ ] Archive or delete orphaned/duplicate reports

**Execution approach for this project:**

| Approach       | When to Use                                            | Components                              |
| -------------- | ------------------------------------------------------ | --------------------------------------- |
| Manual build   | Complex assignment logic, dual-CRM sync, first build   | Lead assignment, lifecycle automations  |
| Assisted       | Specs are clear, pattern established                   | Custom fields, report/dashboard builds  |

**Important:** Salesforce is fully retiring Workflow Rules and Process Builder by December 31, 2025 [3]. All automations must be built using Salesforce Flow (or HubSpot Workflows). Migrate any existing Process Builders before building new logic on top. Best practice: consolidate to no more than 3 Flows per object (Before Save, After Save, Before Delete) rather than creating separate Flows per automation [3].

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify all automations work correctly and reports show accurate data.

**Two types of testing:**

| Type              | Who      | Purpose                                                              |
| ----------------- | -------- | -------------------------------------------------------------------- |
| Technical Testing | Our team | Verify automations fire correctly, fields populate, reports are accurate |
| Customer Testing  | Customer | Verify it does what they need, data looks right to them              |

**Technical testing checklist:**

- [ ] **Lead capture:** Submit test leads from each source -- verify CRM record creation with all fields populated
- [ ] **Lead assignment:** Test leads matching each assignment rule -- verify correct owner assignment and notifications
- [ ] **Lifecycle automations:** Move test records through each stage -- verify date/time stamps populate correctly
- [ ] **Task automations:** Trigger each task creation event -- verify task created with correct assignee, due date, priority
- [ ] **Renewal reminders:** Set test contract end dates at 91, 61, 31 days out -- verify reminders fire
- [ ] **Reports:** Compare report data against known data points -- verify calculations match manual checks
- [ ] **Dashboards:** Verify all dashboard components render, filters work, refresh schedule configured
- [ ] **No automation conflicts:** Verify no duplicate processing from old Process Builders / new Flows running simultaneously
- [ ] **Error logs clean:** Check Salesforce Flow error emails or HubSpot workflow error logs -- zero errors

**Customer testing:**

- Walk customer through each automation with real scenarios
- Have them submit a test lead, watch it flow through capture -> assignment -> lifecycle
- Review each dashboard together -- confirm data accuracy and usability
- Capture feedback, fix issues

**Engineering sign-off checkpoint:**

- [ ] All automations running error-free for 48+ hours on real data
- [ ] All reports showing accurate data (spot-checked against known values)
- [ ] All dashboards accessible to appropriate stakeholders
- [ ] Customer has tested and approved
- [ ] Ready for enablement

**Decision point:**

- **Proceed to Enablement** -> System is built, needs training/adoption
- **Loop back to Build** -> Issues found, needs fixes

---

## Phase 3: Enablement

> **Goal:** Customer team can actually use the automations and dashboards we built.
>
> **Output:** Trained team with documentation, stabilized system, no critical issues.

### Sub-Phases

```
3a Training Prep -> 3b Training Sessions -> 3c Hypercare -> 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from automation specs, build documentation, and dashboard configurations.

**Input:** Strategic package + tech specs + built system

**Output:** Training package containing:

- **Video walkthrough scripts:**
  - Dashboard navigation walkthrough (per dashboard: Sales, Marketing, CS, Executive)
  - Automation monitoring -- how to check for and resolve errors
  - How to add new lead sources or modify assignment rules
- **Written guides:**
  - Admin runbook: where automations live, how to troubleshoot, when to escalate
  - Field mapping reference: source of truth for each field, sync direction
  - Report calculation reference: how CAC, CLV, churn are calculated, data sources
  - Dashboard folder map: what lives where and who should access it
- **FAQ draft:**
  - "Why is my lifecycle stage not updating?" (check trigger criteria)
  - "Why does this report show different numbers than my spreadsheet?" (check date filters, data sources)
  - "How do I add a new territory to lead assignment?" (step-by-step)
  - "What happens when a lead does not match any assignment rule?" (fallback logic)

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to customer team.

**Three types of training:**

| Type                | Audience                         | Focus                                                                  |
| ------------------- | -------------------------------- | ---------------------------------------------------------------------- |
| Leadership training | VP Sales, VP Mktg, CS Lead       | Interpret dashboards, identify action items, understand what KPIs mean |
| Technical handoff   | RevOps Lead, CRM Admin           | Monitor automations, troubleshoot errors, modify reports, add new fields |
| End user training   | Sales Reps, CSMs                 | Understand lifecycle stages, use dashboards in daily work              |

**Training delivery:**

1. Schedule sessions with appropriate stakeholders (3 sessions, 30-60 min each)
2. Deliver training (live with screen share)
3. Record video walkthroughs for future reference
4. Answer questions, note gaps

**Output:**

- Trained stakeholders across all three audiences
- Video recordings for onboarding future team members
- Questions log (feeds into FAQ updates)

---

### 3c. Hypercare

> **Purpose:** Intensive post-launch support to stabilize automations and catch data issues.

**Duration:** 2 weeks

**What happens:**

- Monitor automation error logs daily for the first week, then every other day
- Office hours: weekly 30-min slot for questions
- Bug triage and fixes (automation not firing, report showing wrong data, sync conflicts)
- Validate that automations continue running error-free as real data volume increases
- Spot-check report accuracy against known data points

**Common issues during hypercare:**
- Automation governor limit errors on high-volume days (large lead imports, end-of-month processing)
- Lifecycle stage date stamps not populating because of trigger criteria edge cases
- Reports showing nulls because custom fields were not backfilled on existing records
- Sync conflicts creating duplicate records or overwriting data

**When to skip:** This project type always needs hypercare. Automations running on live data will surface edge cases that testing does not catch.

**Output:** Stabilized system, no critical issues outstanding, automation error rate at zero for 7+ consecutive days

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm customer can operate independently.

**Validation checkpoint:**

- [ ] All training sessions delivered (Leadership + Technical + End User)
- [ ] Training recordings and documentation provided
- [ ] Hypercare period complete -- 7+ days of error-free automation execution
- [ ] No critical issues outstanding
- [ ] Customer team can check automation errors without calling us
- [ ] Customer team can interpret dashboards and pull ad-hoc reports
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** -> Customer is enabled, project wrapping up
- **Extend Hypercare** -> Still seeing automation errors or data issues, needs more support time

---

## Phase 4: Handoff

> **Goal:** Clean project close with maintenance plan established and retention/expansion path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the system, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule -> 4b Internal Handoff -> 4c External Handoff -> 4d Project Close
                          (SME -> Architect)        (LS -> Customer)     (Archive + Debrief)
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At                                                                         |
| ----------------------------- | -------------------- | ------------------------------------------------------------------------------------- |
| **Single Project**            | Customer owns        | 4c (External Handoff) -- customer receives maintenance schedule and runs it themselves |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) -- Architect receives maintenance schedule and runs it for customer |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention after the project is complete -- cadences, tasks, triggers for re-engagement.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task                  | What to Check                                              | Red Flag Threshold                                     |
| ----------------------------- | ---------------------------------------------------------- | ------------------------------------------------------ |
| Automation Error Log Review   | Check Flow error emails (SFDC) or Workflow error log (HS)  | Any errors persisting >24 hours                        |
| Stage Hit Date Audit          | Sample 10 records -- verify stage dates populating          | >5% of new records missing stage dates                 |
| Report Accuracy Spot-Check    | Compare 3 key reports to known data points                 | >5% variance from manual calculation                   |
| Dashboard Usage Review        | Check last accessed dates on all dashboards                | Any dashboard not accessed in 30 days (user adoption)  |

**Quarterly Tasks:**

| Quarterly Task                     | What to Review                                        | Action if Off-Track                                  |
| ---------------------------------- | ----------------------------------------------------- | ---------------------------------------------------- |
| Full Automation Audit              | Check for new conflicting automations, deprecated logic | Deactivate conflicts, update documentation           |
| Report Calculation Validation      | Recalculate CAC, CLV, churn manually and compare       | Fix formula errors, update data sources              |
| Report Folder Cleanup              | Archive unused reports, check for orphans              | Clean up, update naming conventions                  |
| Lifecycle Stage Definition Review  | Confirm stage definitions still match business process | Update definitions, retrain if changed               |

**After First Business Cycle (30-60 days post-launch):**

- Validate that automations handle full month-end volume without errors
- Confirm CAC and CLV calculations produce accurate results with a full month of data
- Review churn reporting against finance team's numbers -- resolve discrepancies
- Check that renewal reminders fired correctly for contracts within the 90-day window

**Refinement Triggers (when to re-engage):**

| Trigger                         | Threshold                                   | Response                                                   |
| ------------------------------- | ------------------------------------------- | ---------------------------------------------------------- |
| Automation error rate           | >0 errors per week for 2+ consecutive weeks | Re-engage SME to diagnose root cause                       |
| Report accuracy drift           | >10% variance from manual calculation       | Audit data sources, check for schema changes               |
| New lead source added           | Client adds new form, channel, or integration | Scope lead capture automation update                       |
| Lifecycle stage changes         | Client redefines stages or adds new ones    | Scope automation update project                            |
| CRM schema changes              | New objects, fields, or integrations added   | Audit for automation conflicts, update field mappings      |

**Every 6-12 Months:**

- Full system health check: all automations, reports, dashboards
- Review against current business processes -- has anything changed that automations do not reflect?
- Assess dashboard adoption -- are stakeholders actually using the reports? If not, why?
- Consider additional automation opportunities (e.g., lead scoring, attribution) based on data maturity

---

### 4b. Internal Handoff (SME -> Architect)

> **Purpose:** Transfer context so Architect can manage ongoing relationship.

**What the Architect needs to know:**

- What was built: X automation flows, Y reports, Z dashboards across Sales/Marketing/CS/Executive functions
- System ownership model: which system is source of truth for which data
- Common issues: lifecycle stage dates not populating (check trigger criteria), sync conflicts (check system ownership model), report accuracy complaints (check date filters first)
- When to escalate back to SME: any changes to lifecycle stage definitions, modifications to CAC/CLV formulas, new system integrations, automation governor limit issues

**Escalation guidelines:**

| Issue Type                                          | Who Handles                                               | Analogy                 |
| --------------------------------------------------- | --------------------------------------------------------- | ----------------------- |
| Dashboard filter changes, adding new users           | Architect                                                 | General contractor      |
| Report customization, adding new report views        | Architect with admin runbook                              | General contractor      |
| Lifecycle stage changes, new automation logic        | SME                                                       | Specialist tradesperson |
| Governor limit errors, sync conflict resolution      | SME                                                       | Specialist tradesperson |

**For Dedicated engagements:** Architect also receives the maintenance schedule (4a) and becomes responsible for executing it. SME walks Architect through each maintenance task -- especially the monthly automation error log review and quarterly report validation.

---

### 4c. External Handoff (LS -> Customer)

> **Purpose:** Formal project completion with customer.

**Final project meeting:**

- Review all automation flows built (lead capture, assignment, lifecycle, task, renewal)
- Walk through each dashboard (Sales, Marketing, CS, Executive)
- Walk through admin runbook and troubleshooting guide
- Confirm nothing outstanding
- Answer final questions
- Make it explicit: "Project complete"
- **For Single Project engagements:** Hand over the maintenance schedule (4a) and walk the customer through monthly and quarterly tasks

**Documentation package:**

- Admin runbook (automation monitoring, error troubleshooting, common fixes)
- Field mapping document (source of truth per field, sync direction)
- Report calculation reference (CAC, CLV, churn formulas with data sources)
- Dashboard folder map (what lives where, who should access it)
- All training video recordings
- Definition Alignment Document (final version)
- FAQ document
- Maintenance Schedule
- Support contact info

**For Single Project engagements:** Walk the customer through the maintenance schedule in detail. Record a video walkthrough of the walkthrough.

**Output:** Customer owns the system. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location
- [ ] Handoff documentation complete
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized

#### Internal Debrief (Optional but Recommended)

- What went well? (e.g., client had clean data, stakeholders were responsive)
- What would we do differently? (e.g., build lifecycle automations before lead capture next time)
- Any learnings to feed back into SOPs? (e.g., new governor limit workaround, better test data approach)

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell -> Downsell -> Retry   |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (retainer)
   | if no
2. Downsell: Lead Scoring Model, Attribution, or Executive Reporting Suite
   | if yes
3. Retry retainer at end of next project cycle
```

**Script:**

> "Now that Foundational Automations and Reporting Logic is complete, there are two ways we can continue working together. Option 1: We can set you up on managed services where we handle ongoing automation monitoring, report optimization, and quarterly health checks. Option 2: If there's another specific project you need -- like Lead Scoring to prioritize the leads your automations are now capturing, or Attribution to understand which campaigns are actually driving pipeline -- we can scope that out. Which sounds more interesting?"

**Natural upsell paths from this project:**
- **Lead Scoring Model** -- now that lifecycle stages and engagement data are flowing, build a scoring model on top
- **Attribution** -- now that campaigns are tracked and pipeline reports exist, add attribution modeling
- **Executive Reporting Suite** -- expand the dashboards built here into a full executive reporting package
- **Renewal Management** -- expand the renewal reminder automations into a full renewal management process

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On [date ~90 days out], we'll review how the automations and dashboards are performing and see if any adjustments are needed."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                              |
| ------------------- | --------------------------------------------------------- |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks          |
| 2. Review metrics   | Check automation error rates, dashboard usage, report accuracy |
| 3. Decide ownership | Can Architect handle this check-in, or need SME?          |
| 4. Prep materials   | If SME needed, brief them. If Architect, prep talking points. |

**At the refinement check-in:**

- Review automation performance (error rates, processing volume)
- Review dashboard adoption (who is using what, what is ignored)
- Identify any adjustments needed
- If minor: Architect handles tweaks
- If major: Scope new project (restart the assembly line)

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- Definition Alignment Document (lifecycle stages, KPI definitions, system ownership)
- System Ownership Model (source of truth per data type, sync rules)
- Automation Specifications (trigger logic, actions, exception handling for all flows)
- Report Requirements Matrix (all reports with KPI definitions, calculation formulas, data sources)

**Technical Deliverables:**

- Custom fields created across Lead, Contact, Account, Opportunity objects (stage hit dates, churn tracking, contract dates)
- Automation flows: Lead capture, lead assignment, lifecycle stage automation (all 4 objects), task assignment, renewal reminders, upsell detection
- Reports: Pipeline analysis, stage conversion, time-in-stage, CAC, CLV, churn, campaign performance (10+ reports)
- Dashboards: Sales Pipeline, Executive, Marketing, CS (4 dashboards with drill-down)
- Organized report/dashboard folder structure with appropriate permissions

**Documentation Package:**

- Admin runbook (automation monitoring, error troubleshooting, common fixes)
- Field mapping document
- Report calculation reference
- Dashboard folder map
- Training video recordings (3-4 videos)
- Written guides and SOPs
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

| Phase                    | Output                                                                 | Gate Criteria                                                                                     |
| ------------------------ | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| **Phase 1: Strategy**    | Definition Alignment Document + Automation Specs + Reporting Matrix    | Stakeholders have approved all definitions, automation logic, and reporting requirements           |
| **Phase 2: Engineering** | Working automations + reporting dashboards in CRM                      | All automations running error-free, reports showing accurate data, customer has approved            |
| **Phase 3: Enablement**  | Trained team with documentation                                        | All training delivered, 7+ days error-free operation, team can operate independently               |
| **Phase 4: Handoff**     | Independent customer + archived project                                | Internal/external handoffs complete, maintenance plan in place, project closed                     |

### How to Adapt Per Project Type

This project is **Engineering-heavy**:

| Project Profile       | Strategy Weight | Engineering Weight | Enablement Weight |
| --------------------- | --------------- | ------------------ | ----------------- |
| **Engineering-heavy** | 15-20%          | 60-70%             | 15-20%            |

**Adaptation notes:**
- Phase 1 can compress to 1-2 weeks if client has clear requirements and defined lifecycle stages
- Phase 2 is the core -- expect 3-5 weeks of build time depending on number of automations and reports
- Phase 3 is standard -- 2 weeks hypercare is the minimum for automation projects
- Phase 4 always applies -- the maintenance schedule is especially important because automations degrade over time as CRM schemas evolve

### Key Principles by Phase

**Phase 1 — Strategy**
- We educate. Most clients do not realize how many deprecated automations are running in their CRM, or that their Process Builders will stop working after December 2025 [3]. We show them the current state and educate them on modern automation best practices.
- We drive alignment. Cross-functional projects (Sales + Marketing + CS) stall when stakeholders disagree on lifecycle stage definitions or which system is source of truth. We force alignment through the Definition Alignment Document.
- We come with an opinion. We show up with a recommended System Ownership Model, recommended lifecycle stages based on industry standards, and recommended reporting structure based on what we have seen work at similar companies.

**Phase 2 — Engineering**
- Build sequence matters. Custom fields must exist before automations can populate them. Automations must run before reports can display their data. Do not skip ahead.
- Test before stacking. Each automation must be verified before building reports that depend on it.
- Consolidate flows. Salesforce best practice: no more than 3 Flows per object (Before Save, After Save, Before Delete) [3].
- Governor limits are real. For clients with >10,000 records on any object, optimize Flow logic and use batch processing.

**Phase 3 — Enablement**
- Three audiences, three training types. Leadership needs to interpret dashboards. RevOps/Admin needs to monitor and troubleshoot. End users need to understand lifecycle stages. Do not combine these audiences.
- Hypercare catches real-world edge cases. Bulk lead imports, end-of-quarter pushes, and holiday-adjacent processing gaps all create edge cases that only appear in production. Two weeks of hypercare is the minimum.

**Phase 4 — Handoff**
- Automations degrade silently. Unlike a broken dashboard (which is visible), a broken automation runs without anyone noticing -- until data quality erodes. The maintenance schedule (monthly error log reviews, quarterly audits) prevents silent degradation.
- Natural expansion path. Foundational Automations creates the data infrastructure that higher-value projects build on: Lead Scoring requires lifecycle stage data, Attribution requires campaign tracking, Executive Reporting requires clean pipeline data.

---

## References

[1] [Salesforce State of Sales Report](https://www.salesforce.com/resources/research-reports/state-of-sales/) - Sales reps spend only 28% of their time selling; rest is administrative work including manual data entry.

[2] [Nutshell - CRM Statistics for Sales Professionals](https://www.nutshell.com/blog/crm-stats) - CRM automation reduces administrative tasks by up to 80%, and businesses report a 29% increase in sales revenue after CRM implementation.

[3] [Salesforce Ben - Migrate Process Builder to Flow](https://www.salesforceben.com/migrate-salesforce-workflow-rules-process-builder-to-flow-video/) - Salesforce is retiring Workflow Rules and Process Builder by December 31, 2025. Best practice: consolidate to no more than 3 Flows per object.

[4] [Workato Lead Response Time Study](https://www.workato.com/the-connector/lead-response-time-study/) - Over 63% of businesses did not respond to inbound leads at all; first responders win 35-50% of sales.

[5] [Vitally - B2B SaaS Churn Rate Benchmarks 2025](https://www.vitally.io/post/saas-churn-benchmarks) - B2B SaaS average churn is 4.2% (2024); automatic renewal continuation decreases churn by 34% versus manual renewal requirements.

[6] [Rep.ai - Lead Response Time Statistics](https://rep.ai/blog/lead-response) - Businesses that respond to leads in 5 minutes or less are 100x more likely to connect and convert opportunities.

[7] [CRM.org - CRM Statistics 2025](https://crm.org/crmland/crm-statistics) - Businesses using CRM report an average ROI of $8.71 for every $1 invested; 61% of sales leaders automated their CRM in 2023.
