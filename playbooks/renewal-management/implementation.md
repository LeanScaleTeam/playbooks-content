# Renewal Management — Implementation

## Project One-Pager

### Renewal Management One-Pager

#### Project Type

- Category: Balanced
- Primary Deliverable: Fully operational renewal management system with health scoring, automated 90/60/30-day alerts, renewal pipeline dashboards, and standardized CSM playbooks

##### Phase Relevance

| Phase          | Applies? | Weight | Notes                                                                    |
| -------------- | -------- | ------ | ------------------------------------------------------------------------ |
| 1. Strategy    | Yes      | Medium | Requirements gathering, health score design, renewal timeline definition |
| 2. Engineering | Yes      | Heavy  | CRM configuration, health score build, workflow automation, dashboards   |
| 3. Enablement  | Yes      | Medium | CS team training, CSM playbook rollout, pilot testing                    |
| 4. Handoff     | Yes      | Medium | Documentation package, governance cadence, refinement check-in           |

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────>│ 2. ENGINEER  │────>│3. ENABLEMENT │────>│  4. HANDOFF  │
  │    Medium    │     │    Heavy     │     │    Medium    │     │    Medium    │
  │ 1a>1b>1c>1d │     │ 2a>2b>2c>2d │     │ 3a>3b>3c>3d │     │ 4a>4b>4c>4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   Audit & align        Build scoring,       Train CS team,       Document, hand
   on requirements,     alerts, dashboard,   pilot test, run      off maintenance,
   define health        CSM playbook         hypercare            close project
   score inputs         infrastructure
```

**This project's flow:** Full 4-phase delivery. Strategy defines the renewal timeline, health score inputs, and ownership model. Engineering is the heaviest phase — building health scores, alert workflows, dashboards, and CSM playbook infrastructure in CRM. Phase 3 includes pilot testing with live renewals before full rollout. Phase 4 includes a 30-day refinement check-in to adjust health score weights based on actual usage.

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Watch intro video explaining what proactive renewal management looks like and why health scoring matters
- [ ] Complete intake form covering current renewal tracking method, CRM platform, contract data availability, and CS team structure
- [ ] Provide list of current customers with contract end dates, ARR values, and current owner assignments
- [ ] Provide access credentials for CRM, support platform, and product analytics (if health scoring includes usage signals)

##### Track B: Architect Prep
- [ ] Pull CRM data to assess current renewal tracking completeness (how many accounts have renewal dates, how many have owners)
- [ ] Audit existing health signals available in CRM and connected systems (usage data, support tickets, NPS scores)
- [ ] Draft v0 renewal timeline with 90/60/30-day stages based on contract data patterns
- [ ] Draft v0 health score framework based on available data sources

#### Refinement Loop (1b > 1c > 1d)

| Meeting      | Sub-Phase | Focus                                                            | Stakeholder                   | Output                                 |
| ------------ | --------- | ---------------------------------------------------------------- | ----------------------------- | -------------------------------------- |
| Kickoff      | 1b        | Present v0 renewal audit, validate health signal inventory       | VP CS, CS Ops, RevOps         | Feedback for v1 health score design    |
| Refinement 1 | 1c        | Review v1 health score formula, define alert thresholds          | VP CS, CSM leads              | Validated scoring model + alert rules  |
| Refinement 2 | 1c        | Finalize ownership model, escalation paths, CSM playbook outline | VP CS, RevOps, Finance        | Complete requirements package          |
| Sign-Off     | 1d        | Strategic approval of full renewal management design             | All stakeholders              | Signed-off strategic package           |

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held — current state audit validated, health signals inventoried
- [ ] 1c. Refinement loop complete — health score formula, alert rules, ownership model finalized
- [ ] 1d. Strategic sign-off obtained from VP CS and RevOps

##### Phase 2: Engineering
- [ ] 2a. Tech spec created for renewal tracking view, health score formula, alert workflows, dashboard
- [ ] 2b. Engineering handoff meeting held — build sequence confirmed
- [ ] 2c. Build complete — all components configured in CRM
- [ ] 2d. QA/Test + customer sign-off on all technical components

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped (CSM playbook, dashboard guide, health score interpretation)
- [ ] 3b. Training sessions delivered to CS team
- [ ] 3c. Hypercare period complete (2-week pilot with live renewals)
- [ ] 3d. Enablement sign-off — CS team operating independently

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff (SME > Architect) complete
- [ ] 4c. External handoff (delivery team > Customer) complete
- [ ] 4d. Project closed and archived

#### Document Types

##### Working Documents (iterate together)

| Document                     | Purpose                                                         | When Complete                                       |
| ---------------------------- | --------------------------------------------------------------- | --------------------------------------------------- |
| Current State Audit          | Document existing renewal tracking, gaps, and pain points       | All gaps identified and prioritized                 |
| Health Signal Inventory      | List all available data sources with quality and access status  | All signals rated, integration requirements noted   |
| Health Score Design          | Define formula, weights, thresholds, and categories             | Formula validated against historical churn data     |
| Renewal Timeline Spec        | Define 90/60/30-day stages, actions, owners, and escalations    | Signed off by CS leadership                         |
| CSM Renewal Playbook (draft) | Touchpoint cadence, talk tracks, objection handling             | Reviewed and approved by CS team leads              |

##### Deliverables (polished outputs)

| Deliverable                   | Created From                          | Customer Uses For                              |
| ----------------------------- | ------------------------------------- | ---------------------------------------------- |
| Renewal Management Blueprint  | Health Score Design + Renewal Timeline| Internal alignment with CS and Finance teams   |
| Renewal Dashboard             | Health Signal Inventory + CRM build   | Real-time renewal pipeline visibility          |
| CSM Playbook (final)          | Draft playbook + pilot feedback       | Standardized renewal execution by CSMs         |

#### Enablement Details

##### Training Types

| Type       | Audience                      | Focus                                                          | Duration |
| ---------- | ----------------------------- | -------------------------------------------------------------- | -------- |
| Leadership | VP CS, Head of CS, Finance    | Dashboard interpretation, GRR/NRR tracking, risk distribution  | 30m      |
| CSM Team   | CSMs, CS Ops                  | Renewal playbook execution, health score interpretation, alerts | 60m      |
| Technical  | RevOps, CS Ops, CRM Admin     | System maintenance, alert troubleshooting, score adjustment    | 45m      |

##### Hypercare
- Applies: Yes
- Duration: 2 weeks (pilot period with live renewals)
- Office Hours: Yes — weekly 30-min slot for CSMs to surface issues

##### Training Assets to Create
- [ ] Video walkthrough: Dashboard walkthrough and filter navigation
- [ ] Video walkthrough: Health score interpretation — what drives score changes
- [ ] Doc: CSM Renewal Playbook (touchpoint templates, objection handling, escalation paths)
- [ ] Doc: Alert workflow reference — what each alert means and expected CSM action
- [ ] Doc: Admin guide for adding accounts, adjusting health score weights, modifying alerts

#### Handoff & Retention

##### Internal Handoff (SME > Architect)
- Key context for Architect: Health score formula logic, alert workflow triggers, renewal owner assignment rules, which CSMs were trained
- Escalation trigger: Health score formula redesign, new data source integration, structural changes to alert workflows

##### External Handoff
- Final meeting agenda: Review delivered components, walk through documentation, confirm governance cadence, demonstrate maintenance procedures
- Documentation package: All training video recordings, CSM playbook, health score formula doc, alert workflow doc, dashboard guide, admin guide, maintenance schedule

##### Maintenance Schedule
- Monthly: Health score accuracy check, alert hit-rate review, dashboard usage audit
- Quarterly: Full health score weight recalibration, renewal pipeline review cadence assessment
- Who owns: Single project = customer CS Ops owns | Dedicated = Architect owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services (ongoing health score optimization + quarterly recalibration) > if no > Downsell: Adjacent project (Customer Segmentation, NPS/VoC, Customer Health Model) > Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: 30 days post-launch
- Internal prep trigger: 2 weeks before check-in
- Decision: Architect handles score adjustments / SME needed for structural changes

#### Key Assets

| Asset                          | When Used                                        |
| ------------------------------ | ------------------------------------------------ |
| Health Score Design Template   | Phase 1 — Strategy                              |
| CSM Renewal Playbook Template  | Phase 1-3 — Strategy through Enablement         |
| Renewal Dashboard Template     | Phase 2 — Engineering                           |
| Alert Workflow Spec Template   | Phase 2 — Engineering                           |

#### Definition Alignment Terms

| Term                          | Typical Definition                                                                                     |
| ----------------------------- | ------------------------------------------------------------------------------------------------------ |
| Gross Revenue Retention (GRR) | Percentage of recurring revenue retained from existing customers, excluding expansion (renewals only) |
| Net Revenue Retention (NRR)   | Percentage of recurring revenue retained including expansion, contraction, and churn                  |
| Health Score                  | Composite metric (0-100 or Red/Yellow/Green) combining product usage, support, engagement, and sentiment signals to indicate account risk |
| Renewal Owner                 | The individual (CSM, Account Manager, or designated role) responsible for driving a specific account's renewal to completion |
| At-Risk Account               | An account with a health score below the defined threshold (typically &lt;60 or "Red") with an upcoming renewal within 90 days |
| Churn                         | Customer termination or non-renewal of subscription, resulting in lost recurring revenue              |
| Preventable Churn             | Churn that could have been avoided with earlier intervention (declining usage, unresolved support, disengaged sponsor) |

#### Common Gotchas
- Health score weights based on intuition instead of historical churn data > Validate weights against past churned accounts before deploying
- Renewal dates missing or wrong in CRM for 30%+ of accounts > Run a data cleanup sprint before building automation on top of bad data
- Alert fatigue from too many low-value notifications > Start with 90/60/30-day alerts only; add health-triggered alerts after pilot validates signal quality
- CSMs bypass the system and use their own spreadsheets > Co-design the workflow with CSM leads and make the CRM view genuinely easier than the spreadsheet
- No clear escalation path for at-risk accounts > Define and document escalation criteria and paths before launching alerts

#### Methodology Options

| Option                        | When to Use                                            | Complexity |
| ----------------------------- | ------------------------------------------------------ | ---------- |
| Simple (manual health tiers)  | &lt;100 accounts, limited data sources, no CS platform    | Low        |
| Standard (CRM-native scoring) | 100-500 accounts, CRM has formula/calculated fields    | Medium     |
| Advanced (CS platform + ML)   | 500+ accounts, dedicated CS platform (Gainsight, Vitally, ChurnZero) | High |

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on the renewal management system design — health score formula, renewal timeline, ownership model, alert thresholds, and CSM playbook structure.
>
> **Output:** Signed-off Renewal Management Blueprint + Definition Alignment Document.

### 1a. Pre-Kickoff

> Two parallel tracks run before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                              | Format             |
| ----------------------------- | -------------------------------------------------------------------- | ------------------ |
| Intro video                   | Explain proactive renewal management vs. reactive churn firefighting | Video walkthrough (5-10 min) |
| Definition Alignment Document | Get stakeholder sign-off on GRR, NRR, health score, churn terms     | Google Doc         |
| Pre-filled intake form        | Capture current renewal tracking method, CRM platform, CS team size | Google Form or Doc |
| Data request                  | Customer list with contract dates, ARR, and renewal owners           | Spreadsheet        |

The intro video should highlight that median GRR for B2B SaaS companies is 90%, with top-quartile performers exceeding 95% [1]. Companies with proactive renewal processes see 15-35% reductions in churn rates compared to reactive approaches [2]. This frames why investing in renewal infrastructure matters.

**Completion tracking:** RevOps or CS Ops follows up. Kickoff can proceed without all data, but push hard for the customer list with contract dates — without it, health score validation against historical churn is impossible.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                                   | Output                                              |
| ---- | ------------------------------------------------------------------------ | --------------------------------------------------- |
| 1    | Pull CRM data — assess renewal date completeness and tracking method     | Data quality assessment (% accounts with dates)     |
| 2    | Audit existing health signals (usage, support, NPS, engagement)          | Health Signal Inventory with quality ratings         |
| 3    | Analyze historical churn — identify which signals correlated with churn  | Churn predictor analysis                            |
| 4    | Draft v0 health score framework (signals, weights, thresholds)           | v0 Health Score Design                              |
| 5    | Draft v0 renewal timeline (90/60/30 stages with CSM actions)             | v0 Renewal Timeline Spec                            |

**Critical:** Mark all health score weights and alert thresholds as ASSUMED. The kickoff call validates with CS leadership based on their experience with churned accounts.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building any automation.

| Term                          | Our Definition                                                        | Internally Approved? |
| ----------------------------- | --------------------------------------------------------------------- | -------------------- |
| GRR (Gross Revenue Retention) | Recurring revenue retained from existing customers, excluding expansion revenue | [ ] Yes / [ ] No |
| NRR (Net Revenue Retention)   | Recurring revenue retained including expansion, contraction, and churn | [ ] Yes / [ ] No |
| Churn                         | Customer non-renewal or cancellation resulting in lost ARR            | [ ] Yes / [ ] No |
| Preventable Churn             | Churn where early signals existed but intervention did not occur or was too late | [ ] Yes / [ ] No |
| Health Score                  | Composite risk indicator combining product usage, support health, engagement, and sentiment | [ ] Yes / [ ] No |
| At-Risk Account               | Account with health score below defined threshold + renewal within 90 days | [ ] Yes / [ ] No |
| Renewal Owner                 | Individual responsible for driving a specific account renewal to close | [ ] Yes / [ ] No |

**Instructions to customer:**

> Review each definition with your CS leadership and Finance team. Check "Yes" when approved. We cannot proceed with health score design or alert automation until these terms are aligned, because the formulas and dashboards depend on shared definitions.

---

### 1b. Kickoff Call

> **Purpose:** Present v0 renewal audit findings and health score framework. Customer reacts to our analysis, not creates from scratch.

#### Agenda (60-90 min)

| Time  | Topic                        | What Happens                                                          |
| ----- | ---------------------------- | --------------------------------------------------------------------- |
| 0-15  | Current state audit          | "Here's what we found in your CRM — X% of accounts have renewal dates, Y% have owners" |
| 15-30 | Health signal inventory      | Walk through available signals, rate quality, identify gaps            |
| 30-45 | v0 health score framework    | Present proposed signals, weights, and thresholds. ASSUMED until validated |
| 45-55 | v0 renewal timeline          | Present 90/60/30-day stages with proposed CSM actions at each stage   |
| 55-65 | Definition alignment review  | Review Definition Alignment Doc — confirm or flag blockers            |
| 65-75 | Gaps and next steps          | What data is missing, who owns gathering it, schedule next meeting    |

#### What We Bring

- Current state audit (CRM data quality assessment, renewal tracking gap analysis)
- Health Signal Inventory (all available signals rated by quality and accessibility)
- v0 Health Score Design (proposed formula with ASSUMED weights)
- v0 Renewal Timeline Spec (90/60/30 stages with proposed actions)
- Definition Alignment Document (pre-filled with our recommendations)

#### What We Leave With

- Validated understanding of current renewal process pain points
- Customer input on which health signals they believe most predict churn
- Corrections to v0 health score weights (info needed to create v1)
- Confirmed or adjusted renewal timeline stages
- Clear homework assignments (data access, historical churn data, stakeholder availability)

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Iterate on the health score design, renewal timeline, and CSM playbook structure until sign-off.

#### The Pattern

```
Kickoff Call (gather info on current state + health signals)
    |
Architect processes feedback --> v1 Health Score Design + Renewal Timeline
    |
Meeting 2 (validate v1 scoring, define alert rules) --> v2
    |
Meeting 3 (finalize ownership model, CSM playbook, dashboard reqs) --> v3
    |
Final Review --> Sign-off
```

#### Potential Meeting Types

| Meeting Type               | Focus                                                       | Stakeholder                  |
| -------------------------- | ----------------------------------------------------------- | ---------------------------- |
| Health Score Validation    | Validate score formula against historical churn data        | VP CS, CS Ops, Data team     |
| Alert & Escalation Design  | Define thresholds, notification channels, escalation paths  | VP CS, CSM leads             |
| CSM Playbook Workshop      | Review touchpoint cadence, talk tracks, objection handling  | CS team leads                |
| Dashboard Requirements     | Define views, metrics, access, and scheduled reports        | VP CS, RevOps, Finance       |
| Final Review               | Full walkthrough, sign-off                                  | All stakeholders             |

#### Typical Timeline

| Milestone               | Timing                                          |
| ----------------------- | ----------------------------------------------- |
| Pre-kickoff prep        | 2-3 days                                        |
| Kickoff call            | Day 1 of engagement                             |
| Meeting loop            | 1-2 weeks (2-3 refinement meetings)             |
| Final review + sign-off | When health score validated and alerts defined   |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm all requirements are defined before proceeding to build.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by VP CS and Finance
- [ ] Health Score formula finalized — signals, weights, thresholds, categories agreed
- [ ] Renewal timeline (90/60/30-day stages) approved with CSM actions at each stage
- [ ] Ownership model defined (by segment, CSM territory, or account owner)
- [ ] Alert and escalation rules documented (thresholds, channels, escalation paths)
- [ ] Dashboard requirements captured (views, metrics, access controls)
- [ ] CSM playbook outline approved (touchpoint cadence, talk tracks, objection handling)
- [ ] Historical churn data analyzed and baseline GRR/NRR calculated
- [ ] No blockers for engineering build

#### Decision Point

- **Proceed to Engineering** — Customer wants the full system built in CRM
- **Pause for data cleanup** — Renewal date data quality is too low (&lt;70% complete); run a data sprint first, then resume at Phase 2

---

## Phase 2: Engineering

> **Goal:** Build and test the system based on approved strategic package.
>
> **Output:** Working renewal tracking view, health score formula, automated 90/60/30-day alerts, renewal pipeline dashboard, and CSM playbook infrastructure — all tested and customer-approved.

| Project Type    | Engineering Weight | Notes                                                      |
| --------------- | ------------------ | ---------------------------------------------------------- |
| This project    | Heavy (50-60%)     | CRM-native config: fields, formulas, workflows, dashboards |

### Sub-Phases

```
2a Tech Spec --> 2b Engineering Handoff --> 2c Build --> 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate the strategic renewal management design into CRM-specific technical specifications.

**Input:** Signed-off Renewal Management Blueprint from Phase 1

**Output:** Draft tech spec containing:

- **Renewal Tracking View:** Custom object or opportunity stage configuration, required fields (renewal date, contract value, owner, health status), filtered views by time period and CSM
- **Health Score Formula:** CRM formula field or calculated property mapping each signal to its weight, with category thresholds (e.g., 0-40 = Critical/Red, 41-70 = At-Risk/Yellow, 71-100 = Healthy/Green)
- **Alert Workflows:** Three workflow specs (90-day, 60-day, 30-day) with enrollment triggers, task creation logic, notification channels, and escalation conditions
- **Dashboard:** Report and dashboard spec with renewal pipeline by month, health distribution chart, CSM workload view, trend charts, and scheduled email configuration
- **Build sequence:** Renewal tracking view first (data foundation), then health score formula (depends on fields), then alert workflows (depends on score), then dashboard (depends on all)

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs with engineer before building.

**Who attends:** Architect + Engineer (or CRM Admin)

**Agenda (30-45 min):**

| Time  | Topic                          | What Happens                                                          |
| ----- | ------------------------------ | --------------------------------------------------------------------- |
| 0-15  | Walk through strategic context | Explain what the renewal management system needs to accomplish and why |
| 15-30 | Review tech spec components    | Walk through each build component: tracking view, score formula, alerts, dashboard |
| 30-45 | Refine and approve             | Clarify CRM-specific constraints, confirm build approach and sequence |

**What Architect brings:**
- Signed-off Renewal Management Blueprint (strategic context)
- Draft tech spec (from 2a)
- Known data quality issues flagged during Phase 1

**What engineer leaves with:**
- Approved tech spec with build sequence
- Clear understanding of health score formula logic
- Known risks (data gaps, integration dependencies)

---

### 2c. Build (Configure)

> **Purpose:** Build the renewal management system in CRM.

**Input:** Approved tech spec from 2b

**Build sequence and components:**

| # | Component                    | What to Build                                                                 | CRM Implementation                                      |
|---|------------------------------|-------------------------------------------------------------------------------|----------------------------------------------------------|
| 1 | Renewal Tracking View        | Custom renewal object/opportunity stage with required fields                  | Salesforce: Custom object or Opp record type. HubSpot: Deal pipeline with renewal stages |
| 2 | Renewal Date Auto-Population | Logic to pull renewal dates from contract or subscription data                | Salesforce: Formula field or flow from Contract object. HubSpot: Calculated property or workflow |
| 3 | Renewal Owner Assignment     | Required field with assignment logic (by segment, territory, or account owner)| Salesforce: Assignment rule or flow. HubSpot: Workflow with conditional assignment |
| 4 | Health Score Formula         | Composite score combining usage, support, engagement, and sentiment signals   | Salesforce: Roll-up formula field or external calculation. HubSpot: Calculated property or CS platform integration |
| 5 | 90-Day Alert Workflow        | Trigger task + notification when renewal is 90 days out                       | Salesforce: Flow with scheduled trigger. HubSpot: Workflow with date-based trigger |
| 6 | 60-Day Alert Workflow        | Follow-up trigger with escalation for at-risk accounts                        | Same pattern with added health score condition            |
| 7 | 30-Day Alert Workflow        | Urgent action trigger with manager escalation for unresolved renewals         | Same pattern with additional escalation to VP CS          |
| 8 | Health-Decline Alert         | Trigger when health score drops below threshold on account with upcoming renewal | Salesforce: Flow with field-change trigger. HubSpot: Workflow with property-change enrollment |
| 9 | Renewal Pipeline Dashboard   | Views: pipeline by month, health distribution, CSM workload, trends           | Salesforce: Dashboard with report sources. HubSpot: Custom dashboard |
| 10| Scheduled Dashboard Email    | Weekly renewal summary to CS leadership                                       | Salesforce: Dashboard subscription. HubSpot: Scheduled report email |

**Build tracking:**

- [ ] Component 1: Renewal Tracking View
- [ ] Component 2: Renewal Date Auto-Population
- [ ] Component 3: Renewal Owner Assignment
- [ ] Component 4: Health Score Formula
- [ ] Component 5: 90-Day Alert Workflow
- [ ] Component 6: 60-Day Alert Workflow
- [ ] Component 7: 30-Day Alert Workflow
- [ ] Component 8: Health-Decline Alert
- [ ] Component 9: Renewal Pipeline Dashboard
- [ ] Component 10: Scheduled Dashboard Email

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify the system works and get customer approval.

**Technical testing checklist:**

- [ ] All renewal tracking fields created and populated correctly
- [ ] Renewal dates auto-populate from contract/subscription data
- [ ] Renewal owner field required and assigned on all accounts
- [ ] Health score formula calculates correctly (spot-check 10 accounts across all tiers)
- [ ] Health score categories (Red/Yellow/Green) match expected thresholds
- [ ] 90-day alert fires at correct timing and creates task for correct owner
- [ ] 60-day alert fires at correct timing with escalation for at-risk accounts
- [ ] 30-day alert fires at correct timing with manager escalation for unresolved renewals
- [ ] Health-decline alert triggers when score drops below threshold
- [ ] Dashboard displays correct data in all views (pipeline, health distribution, CSM workload)
- [ ] Scheduled dashboard email sends to configured recipients
- [ ] Test with historical churned accounts — do health scores reflect actual risk accurately?
- [ ] No errors in workflow logs

**Customer testing:**

- Walk CS leadership through the renewal tracking view and dashboard
- Have a CSM test the alert-to-action flow with a sample renewal
- Validate health scores against accounts the CS team knows are healthy vs. at-risk
- Capture feedback on score accuracy and adjust weights if needed

**Engineering sign-off checkpoint:**

- [ ] All 10 build components match tech spec
- [ ] All technical tests passing
- [ ] Customer has tested and confirmed health scores reflect reality
- [ ] Ready for enablement

**Decision point:**

- **Proceed to Enablement** — System works, CS team needs training
- **Loop back to Build** — Health scores inaccurate, alert timing wrong, or dashboard gaps

---

## Phase 3: Enablement

> **Goal:** CS team can use the renewal management system effectively and the system is validated with live renewals.
>
> **Output:** Trained CS team with CSM playbook, stabilized system validated with live renewals, no critical issues.

### Sub-Phases

```
3a Training Prep --> 3b Training Sessions --> 3c Hypercare --> 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from the strategic and technical documentation.

**Input:** Renewal Management Blueprint + tech specs + built system + CSM playbook outline from Phase 1

**Output:** Training package containing:

- **CSM Renewal Playbook** (final version): 90-day touchpoint sequence with email templates and call scripts, renewal conversation guide with discovery questions, objection handling matrix (budget, usage, competition), escalation criteria and paths, expansion opportunity checklist
- **Dashboard Navigation Guide:** How to use filtered views (next 30/60/90 days, by CSM), how to interpret health distribution, how to spot declining accounts
- **Health Score Interpretation Guide:** What each signal contributes, what drives score changes, when to trust the score vs. investigate further
- **Alert Response Guide:** What each alert means, expected CSM action at each stage (90/60/30 day), escalation procedures
- **Admin Guide:** How to add new accounts, adjust health score weights, modify alert thresholds, troubleshoot workflow issues

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to the CS team so they can execute renewals using the new system.

**Training sessions by stakeholder:**

| Type                | Audience                    | Focus                                                             | Duration |
| ------------------- | --------------------------- | ----------------------------------------------------------------- | -------- |
| Leadership training | VP CS, Head of CS, Finance  | Dashboard interpretation: GRR/NRR tracking, risk distribution, pipeline value by month. How to use data for board reporting and capacity planning | 30 min |
| CSM team training   | All CSMs, CS Ops            | End-to-end workflow: alert received > check health score > follow playbook > execute touchpoint > update CRM. Role-play with renewal scenario | 60 min |
| Technical training  | RevOps, CS Ops, CRM Admin   | System maintenance: how to add accounts, adjust score weights, troubleshoot alerts, pull ad-hoc reports, modify workflows | 45 min |

**Training delivery:**

1. Schedule sessions with appropriate stakeholders (leadership first, then CSMs, then technical)
2. Deliver training live with screen share
3. Record video walkthroughs of each session for future reference and new hire onboarding
4. Document questions — feed into FAQ

**Output:**

- Trained stakeholders across all three audiences
- Video recordings for each session
- FAQ document (from questions raised in training)

---

### 3c. Hypercare

> **Purpose:** Validate the system with live renewals and catch issues before full rollout.

**Duration:** 2 weeks

**What happens:**

- Select 3-5 upcoming renewals for pilot testing (mix of healthy, at-risk, and critical accounts)
- Verify 90/60/30-day alerts fire at correct times for pilot accounts
- Confirm health scores reflect actual account health (CSMs validate against their knowledge)
- Test full CSM playbook execution with pilot accounts (follow the touchpoint cadence)
- Monitor dashboard accuracy with live data
- Document any issues — refine health score weights or alert logic based on pilot feedback
- Weekly 30-min office hours for CSMs to surface issues and ask questions

**When to extend:** If health scores are consistently inaccurate (>30% of pilot accounts misclassified) or alerts are not firing correctly, extend hypercare by 1 week and recalibrate.

**Output:** Validated system with live data, refined health score weights, CSM team confident in using the system.

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm the CS team can operate the renewal management system independently.

**Validation checkpoint:**

- [ ] All three training sessions delivered (leadership, CSM team, technical)
- [ ] Training recordings and documentation provided
- [ ] Pilot period complete — system validated with live renewals
- [ ] Health score accuracy confirmed (CSMs agree scores reflect reality)
- [ ] Alert workflows firing correctly in production
- [ ] CSM playbook tested and refined based on pilot feedback
- [ ] No critical issues outstanding
- [ ] CS team can operate without daily support

**Decision point:**

- **Proceed to Handoff** — System works, team is trained, ready to wrap up
- **Extend Hypercare** — Score accuracy needs more tuning or CSM adoption is low

---

## Phase 4: Handoff

> **Goal:** Clean project close with maintenance plan established and retention/expansion path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the system, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule --> 4b Internal Handoff --> 4c External Handoff --> 4d Project Close
                            (SME > Architect)        (delivery > Customer)   (Archive + Debrief)
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At |
| ----------------------------- | -------------------- | ------------- |
| **Single Project**            | Customer CS Ops owns | 4c (External Handoff) |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention to keep the renewal management system accurate and effective.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task                  | What to Check                                                   | Red Flag Threshold                              |
| ----------------------------- | --------------------------------------------------------------- | ----------------------------------------------- |
| Health Score Accuracy Check   | Compare health scores to CSM qualitative assessment for 10 accounts | >20% of accounts misclassified (wrong tier)   |
| Alert Hit-Rate Review         | Review which alerts led to action vs. were ignored              | >30% of alerts ignored (signal quality issue)  |
| Renewal Coverage Audit        | Check that all renewals in next 90 days have an assigned owner  | Any orphan renewals (no owner assigned)        |
| Dashboard Usage Audit         | Confirm CS team is actually using the dashboard weekly          | &lt;50% of CSMs accessed dashboard in past 30 days |

**Quarterly Tasks:**

| Quarterly Task                     | What to Review                                                | Action if Off-Track                              |
| ---------------------------------- | ------------------------------------------------------------- | ------------------------------------------------ |
| Health Score Weight Recalibration  | Analyze which signals predicted actual churn in past quarter  | Adjust weights to improve prediction accuracy    |
| GRR/NRR Trend Review              | Compare current GRR/NRR against baseline set at project start | If GRR declined, investigate root causes         |
| CSM Playbook Effectiveness        | Review which touchpoint templates drove highest renewal rates | Update playbook with higher-performing templates |
| Alert Threshold Adjustment         | Assess if alert thresholds still match risk patterns          | Tighten or loosen thresholds based on outcomes   |

**After First Business Cycle (30-60 days post-launch):**

- Compare actual renewal outcomes to health score predictions — did Red accounts churn? Did Green accounts renew?
- Calculate first GRR/NRR measurement under the new system
- Identify any surprise churns (accounts with Green health scores that still left) and determine what signal was missed
- Key question: Are we catching at-risk accounts earlier? If the system flagged zero accounts that eventually churned, the scoring model needs recalibration

**Refinement Triggers (when to re-engage):**

| Trigger                          | Threshold                                           | Response                                         |
| -------------------------------- | --------------------------------------------------- | ------------------------------------------------ |
| GRR decline                      | GRR drops >2 points from baseline in any quarter    | Re-engage SME to audit health score model        |
| Surprise churn spike             | 2+ accounts churn with no prior risk flag           | Investigate missing signals, add new data source |
| Alert fatigue                    | >40% of alerts ignored for 2+ consecutive months    | Reduce alert volume, improve signal specificity  |
| CSM adoption drop                | &lt;60% dashboard usage for 2+ months                  | Retraining session, UX improvements              |

**Every 6-12 Months:**

- Full health score model recalibration with updated historical churn data
- Review if new data sources should be added (product analytics changes, new support tool, etc.)
- Assess if customer segments have shifted and require segment-specific health score formulas
- Benchmark current GRR/NRR against industry standards (median GRR is 90%, top quartile is >95%) [1]

---

### 4b. Internal Handoff (SME > Architect)

> **Purpose:** Transfer context so Architect can manage the ongoing relationship.

**What the Architect needs to know:**

- Health score formula logic: which signals, what weights, how thresholds were determined
- Alert workflow architecture: trigger conditions, task templates, escalation rules
- Data quality issues: which signals are noisy, which accounts have incomplete data, known gaps
- Common issues and resolutions

**Escalation guidelines:**

| Issue Type                                    | Who Handles                                       |
| --------------------------------------------- | ------------------------------------------------- |
| Dashboard filter changes, adding new CSMs     | Architect                                         |
| Simple health score threshold adjustments     | Architect (with CS Ops approval)                  |
| Health score formula redesign, new signal integration | SME                                        |
| Alert workflow structural changes             | SME                                               |
| System integration issues (new data source)   | SME                                               |

**For Dedicated engagements:** Architect also receives the maintenance schedule (4a) and becomes responsible for running monthly and quarterly checks.

---

### 4c. External Handoff

> **Purpose:** Formal project completion with customer.

**Final project meeting:**

- Review what was delivered: renewal tracking view, health score, alerts, dashboard, CSM playbook
- Walk through documentation package
- Walk through maintenance schedule (monthly + quarterly tasks)
- Confirm governance cadence: weekly renewal pipeline review, monthly metrics review with leadership
- Review baseline GRR/NRR established at project start as benchmark for measuring improvement
- Answer final questions
- Make it explicit: "Project complete"
- **For Single Project:** Hand over maintenance schedule and record a video walkthrough of all maintenance tasks

**Documentation package:**

- All training video recordings (leadership, CSM team, technical)
- CSM Renewal Playbook (touchpoint templates, objection handling, escalation paths)
- Health Score Formula documentation (signals, weights, thresholds, data sources)
- Alert Workflow documentation (trigger logic, task templates, escalation rules, troubleshooting)
- Dashboard Guide (each view explained, how to interpret metrics)
- Admin Guide (adding accounts, adjusting scores, modifying alerts)
- Definition Alignment Document (final version)
- FAQ document (from training sessions)
- Maintenance Schedule (monthly + quarterly tasks with red flag thresholds)
- Baseline metrics report (GRR, NRR, churn rates by segment from Phase 1)

**Output:** Customer owns the renewal management system. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location
- [ ] Handoff documentation complete
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized

#### Internal Debrief (Optional but Recommended)

- What went well? (e.g., health score accuracy, CSM adoption, stakeholder alignment)
- What would we do differently? (e.g., data cleanup sprint timing, number of refinement meetings)
- Were there any missing health signals we should recommend for similar clients?
- Any learnings to feed back into the Renewal Management playbook or health score design template?

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell > Downsell > Retry    |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (ongoing health score optimization + quarterly recalibration)
   | if no
2. Downsell: Adjacent project (Customer Health Model, Customer Segmentation, NPS/VoC)
   | if yes
3. Retry retainer at end of next project cycle
```

**Script:**

> "Now that the renewal management system is live, there are two ways we can continue working together. Option 1: We handle ongoing optimization — quarterly health score recalibration, alert tuning, and CSM playbook updates as your business evolves. Option 2: If there's an adjacent area you want to tackle, like a deeper Customer Health Model or Customer Segmentation project, we can scope that out. Which sounds more interesting?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On [date ~30 days out], we'll review the first month of health scores against actual renewal outcomes, recalibrate weights if needed, and see if any alerts need adjustment."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                                        |
| ------------------- | ------------------------------------------------------------------- |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks                    |
| 2. Pull data        | GRR/NRR change from baseline, health score accuracy vs. outcomes   |
| 3. Decide ownership | Can Architect handle recalibration, or need SME?                   |
| 4. Prep materials   | If SME needed, brief them. If Architect, prep recommendation deck. |

**At the refinement check-in:**

- Review first month of health score predictions vs. actual renewal outcomes
- Identify any surprise churns or misclassified accounts
- Recalibrate health score weights based on real data
- Adjust alert thresholds if needed
- If minor: Architect handles adjustments
- If major (formula redesign needed): Scope refinement project

**Output:** Project archived. Future revenue path established. 30-day refinement check-in scheduled.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- Renewal Management Blueprint (health score design, renewal timeline, ownership model, alert rules)
- Definition Alignment Document (GRR, NRR, Health Score, Churn definitions — signed off)
- Current State Audit Report (renewal tracking gaps, data quality assessment, baseline metrics)

**Technical Deliverables (Phase 2):**

- Renewal Tracking View in CRM (filtered by time period and CSM)
- Health Score Formula (configured in CRM or CS platform)
- Automated Alert Workflows (90/60/30-day + health-decline triggered)
- Renewal Pipeline Dashboard (pipeline by month, health distribution, CSM workload, trends)
- Scheduled Dashboard Reports (weekly email to CS leadership)

**Documentation Package:**

- Training video recordings (3 sessions)
- CSM Renewal Playbook (touchpoint templates, objection handling, escalation paths)
- Health Score Formula Documentation
- Alert Workflow Documentation
- Dashboard Guide
- Admin Guide
- FAQ document
- Maintenance Schedule
- Baseline Metrics Report (GRR, NRR, churn rates)

---

## Troubleshooting Guide

> Common issues encountered after launch and how to resolve them.

| Scenario                                        | Symptoms                                                    | Resolution                                                                       |
| ----------------------------------------------- | ----------------------------------------------------------- | -------------------------------------------------------------------------------- |
| Health scores do not update                     | Scores stay static, no change even as signals change        | Check formula field recalculation trigger. In Salesforce, verify flow runs on field update. In HubSpot, confirm calculated property dependencies |
| 90-day alert fires too early or too late        | Tasks created at wrong time relative to renewal date        | Audit date-based trigger logic. Check if renewal date field uses the correct date format and timezone |
| CSMs not receiving alert notifications          | Tasks created but no notification                           | Verify notification workflow is active, check recipient logic, confirm email integration is connected |
| Health score categories seem wrong              | Accounts known to be healthy show as Red, or vice versa     | Spot-check 5-10 accounts manually. Compare individual signal scores to expectations. Likely a weighting issue — recalibrate using historical churn data |
| Dashboard shows no data or wrong numbers        | Blank dashboard or values that don't match expectations     | Check report filters (date range, owner, record type). Verify data sources are populating correctly |
| Orphan renewals with no owner                   | Renewals appear in pipeline with blank owner field          | Check assignment workflow trigger. Likely new accounts added after initial assignment run — configure trigger for new account creation |
| Alert fatigue — CSMs ignoring alerts            | High volume of alerts, low action rate                      | Too many alerts or thresholds too sensitive. Reduce alert frequency, tighten health score threshold for escalation alerts, consider daily digest instead of individual notifications |
| Health score does not predict churn accurately  | Multiple surprise churns (accounts with Green scores that left) | Missing signals that matter. Investigate what the churned accounts had in common that the score missed. Add new signals or adjust weights |

---

## Edge Cases

| Edge Case                                      | How to Handle                                                                                                  |
| ---------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| Multi-year contracts with auto-renewal clauses | Configure separate alert cadence for auto-renewals (focus on cancellation window awareness, not renewal outreach) |
| Accounts with no product usage data            | Use a reduced health score formula (support + engagement only) and flag accounts for manual review             |
| Executive sponsor departure mid-renewal        | Trigger "Executive Sponsor Change" intervention playbook immediately, regardless of health score or renewal timing |
| Customer acquired or merging with another company | Pause automated alerts, escalate to VP CS for manual handling of the renewal conversation                    |
| Multiple contracts/products per account         | Track each contract as a separate renewal with its own timeline; dashboard should show aggregate account view  |
| Renewal falls during holiday period            | Shift alert cadence forward by 2 weeks to account for reduced availability                                    |

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
| **Phase 1: Strategy**    | Signed-off Renewal Management Blueprint + Definition Alignment Doc     | CS leadership approved health score design, renewal timeline, and ownership model |
| **Phase 2: Engineering** | Built renewal tracking, health scores, alerts, and dashboard in CRM    | All components match tech spec, health scores validated against known accounts |
| **Phase 3: Enablement**  | Trained CS team with CSM playbook, system validated with live renewals  | All training delivered, pilot complete, team can operate independently         |
| **Phase 4: Handoff**     | Independent customer + archived project                                | Internal/external handoffs complete, maintenance plan in place, project closed |

### Engineering Principles

**Build sequence:** Renewal tracking view first (data foundation), then health score formula (depends on fields), then alert workflows (depends on score), then dashboard (depends on all). Do not parallelize the first time.

**Health score validation:** The most critical test is validation against known accounts. Ask CSMs: "Does this score match your gut?" If it does not match for >20% of accounts, recalibrate before proceeding.

### Why Maintenance Schedules Matter

Health scores decay in accuracy over time. Customer behavior patterns shift, product features change, new support channels are added. Without regular recalibration (quarterly at minimum), health scores become noise — CSMs stop trusting them, alert fatigue sets in, and the system falls into disuse. The maintenance schedule prevents this by making recalibration explicit and cadenced.

The 30-day refinement check-in is non-negotiable. Health score weights set during Phase 1 are always based on assumptions about signal-to-churn correlation. The first 30 days of live data provide the first opportunity to validate and recalibrate. Schedule this during the external handoff meeting.

---

## References

[1] [Benchmarkit - 2024 SaaS Performance Metrics](https://www.benchmarkit.ai/2024benchmarks)

[2] [QuantSpark - Predicting Renewals and Reducing Churn at Scale](https://quantspark.ai/case-studies/case-study-predicting-renewals-and-reducing-churn-at-scale)

[3] [Vitally - How to Create a Customer Health Score with 4 Metrics](https://www.vitally.io/post/how-to-create-a-customer-health-score-with-four-metrics)

[4] [Vitally - B2B SaaS Churn Rate Benchmarks 2025](https://www.vitally.io/post/saas-churn-benchmarks)

[5] [HubSpot - How Automated Renewal Workflows Help Exceed Retention Targets](https://blog.hubspot.com/service/automated-subscription-renewal-workflows)

[6] [ChurnZero - 2024 B2B SaaS Benchmarking Survey](https://churnzero.com/blog/2024-b2b-saas-benchmarking-survey-webinar/)

[7] [Optifai - B2B SaaS NRR Benchmark by Segment](https://optif.ai/learn/questions/b2b-saas-net-revenue-retention-benchmark/)
