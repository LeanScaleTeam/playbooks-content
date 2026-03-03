# Customer Success Platform Implementation — Implementation

## Project One-Pager

```markdown
# Customer Success Platform Implementation One-Pager

## Project Type

- Category: Technical (heavy integration and configuration work)
- Primary Deliverable: Fully configured customer success platform (Gainsight, ChurnZero, Vitally, Totango, Planhat, or Catalyst) with health scoring, automated playbooks, dashboards, and integrations to CRM, product analytics, support, and billing systems

### Phase Relevance

| Phase          | Applies? | Weight | Notes                                                        |
| -------------- | -------- | ------ | ------------------------------------------------------------ |
| 1. Strategy    | Yes      | Med    | Platform selection, data architecture, health score design   |
| 2. Engineering | Yes      | Heavy  | Integration setup, health scoring, automation, dashboards    |
| 3. Enablement  | Yes      | Med    | CSM training, pilot program, full rollout                    |
| 4. Handoff     | Yes      | Med    | Admin handoff, troubleshooting guide, maintenance schedule   |

---

## Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │     Med      │     │    Heavy     │     │     Med      │     │     Med      │
  │ 1a→1b→1c→1d │     │ 2a→2b→2c→2d │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   Platform selection    Integrations +       CSM training          Admin handoff +
   + data architecture   health + dashboards  pilot + rollout       maintenance schedule
```

**This project's flow:**
- Full 4-phase execution. Light-to-medium strategy (platform selection and data mapping), heavy engineering (integrations, health scoring, automations, dashboards), medium enablement (pilot + full team rollout training), standard handoff.
- Phase 1 may compress if the client has already selected a platform — skip evaluation steps, move directly to data architecture.
- Phase 2 is the heaviest phase: 4-8 weeks for mid-market platforms (ChurnZero, Vitally), 3-6 months for enterprise platforms (Gainsight) [1].

---

## Pre-Kickoff (1a)

### Track A: Customer Homework
- [ ] Watch intro video explaining CSP project scope and what "customer health visibility" means
- [ ] Complete intake form: current CS tools, CRM details, product analytics platform, support ticketing, billing system, team size, customer segments
- [ ] Provide CRM admin access (Salesforce/HubSpot) and integration credentials
- [ ] Document current renewal tracking process and health scoring approach (if any)
- [ ] Get stakeholder sign-off on customer segmentation tiers and lifecycle stage definitions

### Track B: Architect Prep
- [ ] Pull CRM account data: account hierarchy, ARR/MRR distribution, renewal dates, historical churn
- [ ] Audit existing integrations: what data flows where today
- [ ] Run diagnostic on data quality: completeness of account records, contact roles, opportunity data
- [ ] Research client's current platform shortlist (if any) and prepare vendor comparison
- [ ] Create v0 data architecture diagram showing proposed integration flows

---

## Refinement Loop (1b → 1c → 1d)

| Meeting      | Sub-Phase | Focus                                                      | Stakeholder                      | Output                          |
| ------------ | --------- | ---------------------------------------------------------- | -------------------------------- | ------------------------------- |
| Kickoff      | 1b        | Present v0 data architecture, validate current state       | VP CS, CS Ops, RevOps            | Corrections for v1              |
| Refinement 1 | 1c        | Platform selection review, integration requirements        | VP CS, IT/Engineering            | Platform decision, v2           |
| Refinement 2 | 1c        | Health score component design, playbook priorities         | CS Leadership, CSM leads         | Health score model, v3          |
| Sign-Off     | 1d        | Final data model, integration plan, health score formula   | All stakeholders                 | Approved strategic package      |

---

## Phase Checklists

### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held
- [ ] 1c. Refinement loop complete (v0 → vFinal)
- [ ] 1d. Strategic sign-off obtained (platform selected, data model approved, health score designed)

### Phase 2: Engineering
- [ ] 2a. Tech spec created (integration architecture, field mappings, health score formula, automation rules)
- [ ] 2b. Engineering handoff meeting held
- [ ] 2c. Build complete (CRM integration, data sources connected, health scores configured, playbooks built, dashboards deployed)
- [ ] 2d. QA/Test + customer sign-off (pilot with 2-4 CSMs, data quality validated)

### Phase 3: Enablement
- [ ] 3a. Training materials prepped (video walkthroughs, quick-reference guides, FAQ)
- [ ] 3b. Training sessions delivered (CSM team + leadership)
- [ ] 3c. Hypercare period complete (2-4 weeks post-rollout)
- [ ] 3d. Enablement sign-off

### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff (SME → Architect) complete
- [ ] 4c. External handoff complete
- [ ] 4d. Project closed and archived

---

## Document Types

### Working Documents (iterate together)

| Document                      | Purpose                                          | When Complete                                  |
| ----------------------------- | ------------------------------------------------ | ---------------------------------------------- |
| CS Operations Intake Form     | Capture current tools, processes, data sources   | All fields filled, reviewed in kickoff         |
| Data Architecture Diagram     | Map data flows from source systems to CSP        | All integrations documented, approved          |
| Health Score Design Document  | Define components, weights, thresholds           | Validated against historical churn data        |
| Platform Evaluation Matrix    | Compare vendor options against requirements      | Platform selected, budget approved             |

### Deliverables (polished outputs)

| Deliverable                    | Created From                  | Customer Uses For                              |
| ------------------------------ | ----------------------------- | ---------------------------------------------- |
| Integration Architecture Map   | Data Architecture Diagram     | Internal documentation, IT alignment           |
| Health Score Methodology Doc   | Health Score Design Document  | CS team education, ongoing score refinement    |
| CSP Configuration Playbook     | Build notes + tech spec       | Admin reference for ongoing maintenance        |

---

## Enablement Details

### Training Types

| Type       | Audience                        | Focus                                                    | Duration |
| ---------- | ------------------------------- | -------------------------------------------------------- | -------- |
| Leadership | VP CS, CCO, CS Directors        | Interpret dashboards, portfolio risk, NRR tracking       | 45 min   |
| CSM Team   | Individual CSMs                 | Daily workflows: account views, CTAs, playbooks, health  | 90 min   |
| Technical  | CS Ops Admin, RevOps            | Platform admin: user management, playbook editing, integrations, reporting | 60 min   |

### Hypercare
- Applies: Yes
- Duration: 2-4 weeks post full-team rollout
- Office Hours: Yes — twice-weekly 30-min slots during first 2 weeks, then weekly

### Training Assets to Create
- [ ] Video: Platform navigation and account 360 walkthrough
- [ ] Video: Health score interpretation — what green/yellow/red means and when to act
- [ ] Video: CTA management — daily workflow for CSMs
- [ ] Video: Dashboard walkthrough for leadership
- [ ] Doc: Quick-reference guide for CSM daily workflows
- [ ] Doc: Admin guide — user management, playbook editing, integration troubleshooting
- [ ] Doc: Health score methodology and component definitions

---

## Handoff & Retention

### Internal Handoff (SME → Architect)
- Key context for Architect: Which platform was deployed, integration architecture, health score methodology, key stakeholder contacts, any known data quality issues or integration limitations
- Escalation trigger: Health score formula changes, new integration requests, platform migration, structural playbook redesign

### External Handoff
- Final meeting agenda: Review delivered configuration, walk through documentation package, confirm admin access transferred, demonstrate maintenance tasks, answer final questions
- Documentation package: Integration architecture map, health score methodology, admin guide, training video walkthroughs, FAQ, maintenance schedule

### Maintenance Schedule
- Monthly: Health score accuracy check, integration sync validation, CTA completion rate review
- Quarterly: Health score recalibration, playbook effectiveness review, new segment/lifecycle stage evaluation
- Who owns: Single project = customer CS Ops owns | Dedicated = Architect owns

### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services (ongoing CSP optimization, new playbook development, quarterly health score recalibration) → if no → Downsell: Another project (e.g., CS-to-Sales handoff process, expansion revenue workflow) → Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~90 days after go-live
- Internal prep trigger: 2 weeks before
- Decision: Architect handles routine optimization / SME needed for structural changes

---

## Key Assets

| Asset                          | When Used          |
| ------------------------------ | ------------------ |
| CS Operations Intake Form      | Phase 1a           |
| Platform Evaluation Matrix     | Phase 1c           |
| Data Architecture Template     | Phase 1c-2a        |
| Health Score Design Template   | Phase 1c-2a        |
| CSP Configuration Checklist    | Phase 2c           |
| Training Deck Template         | Phase 3a           |

---

## Definition Alignment Terms

| Term                    | Typical Definition                                                                                     |
| ----------------------- | ------------------------------------------------------------------------------------------------------ |
| Customer Health Score   | A composite metric (0-100 or color-coded) combining product usage, engagement, support sentiment, and payment history to predict retention risk |
| CTA (Call to Action)    | A prioritized task generated by the CSP when a customer signal triggers intervention — appears in CSM's task queue |
| Playbook                | An automated workflow of tasks and touchpoints triggered by a customer event or signal (e.g., onboarding, at-risk, renewal) |
| Lifecycle Stage         | A customer's current phase in the post-sale journey: Onboarding, Adoption, Growth, Renewal, At-Risk    |
| Customer Segment        | A grouping of customers by ARR tier, industry, use case, or service level that determines CSM allocation and playbook assignment |
| NRR (Net Revenue Retention) | Percentage of recurring revenue retained from existing customers including expansion minus contraction and churn. Median is 106% for venture-backed SaaS; best-in-class exceeds 130% [2] |
| Digital CS Motion       | Low-touch automated engagement (email sequences, in-app messages) for customers that don't have a dedicated CSM |

---

## Common Gotchas
- Health scores configured without validating against historical churn data → CSMs distrust the system within weeks → Always back-test scoring model before go-live [3]
- CRM data quality issues discovered after integration is built → Sync errors and incomplete account records → Run CRM data audit in Phase 1a, resolve before Phase 2c
- Platform selected based on feature checklist instead of CS maturity fit → Over-buying complexity the team can't use → Match platform to maturity: ChurnZero/Vitally for speed, Gainsight for enterprise complexity [4]
- Integration capabilities oversold during vendor demo → Discover gaps mid-implementation → Validate integrations with technical tests during evaluation, not just vendor claims
- Launching without killing legacy tools → CSMs maintain parallel systems, adoption drops → Explicitly retire spreadsheets and manual tracking on go-live day
- Playbooks configured but never tested with real scenarios → Automation fires incorrectly or misses triggers → Run controlled test scenarios for every playbook before full rollout

---

## Methodology Options

| Option                     | When to Use                                                      | Complexity |
| -------------------------- | ---------------------------------------------------------------- | ---------- |
| Quick-start (Vitally/Totango) | Team &lt; 10 CSMs, &lt; 500 accounts, need value in 2-3 weeks  | Low        |
| Mid-market (ChurnZero/Planhat) | Team 10-30 CSMs, 500-5000 accounts, need balance of speed and depth | Medium |
| Enterprise (Gainsight)     | Team 30+ CSMs, 5000+ accounts, complex hierarchy, multi-product  | High       |

See Methodology for detailed platform selection frameworks and scoring rubrics.
```

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on platform selection, data architecture, health score design, and automation priorities.
>
> **Output:** Definition Alignment Document + Strategic Package (platform decision, data model, health score formula, playbook priorities — signed off by stakeholders).

### 1a. Pre-Kickoff

> Two parallel tracks run before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                             | Format             |
| ----------------------------- | ------------------------------------------------------------------- | ------------------ |
| Intro video                   | Explain what a CSP implementation involves and expected outcomes     | Video (8-10 min)   |
| Definition Alignment Document | Get stakeholder sign-off on health score, lifecycle, segment terms   | Google Doc         |
| CS Operations Intake Form     | Capture current tools, processes, data sources, team structure       | Google Form or Doc |

**CSP-specific intake questions:**
- What CRM are you using? (Salesforce / HubSpot / Other)
- What product analytics tool do you use? (Amplitude / Pendo / Mixpanel / Other / None)
- What support ticketing system? (Zendesk / Intercom / Freshdesk / Other)
- What billing/subscription system? (Stripe / Chargebee / Zuora / Other)
- How many CSMs on the team? What's the account-to-CSM ratio?
- How do you currently track renewals? (CRM / Spreadsheet / Platform / Other)
- Do you have a health scoring approach today? If so, describe it.
- What are your top 3 objectives for this platform? (reduce churn / improve NRR / scale CS ops / expand revenue / other)
- Have you evaluated any platforms already? Which ones?

**Completion tracking:** CS Ops or RevOps lead owns follow-up. Don't cancel kickoff if incomplete, but push hard to get CRM access and tool inventory before the call.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                              | Output                                      |
| ---- | ------------------------------------------------------------------- | ------------------------------------------- |
| 1    | Gather inputs (intake form, CRM access, integration credentials)    | Raw data collected                          |
| 2    | Audit CRM accounts, contacts, opportunities                         | Current state assessment with data quality score |
| 3    | Map existing data flows between CRM, support, product analytics     | v0 data architecture diagram                |
| 4    | Identify integration gaps and data quality issues                   | Gap analysis with recommended fixes         |
| 5    | Prepare platform comparison (if not yet selected)                   | Evaluation matrix with weighted criteria    |

**Critical:** Mark all data mappings and recommendations as ASSUMED. The kickoff call validates.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building anything.

| Term                    | Our Definition                                                    | Internally Approved? |
| ----------------------- | ----------------------------------------------------------------- | -------------------- |
| Customer Health Score   | Composite metric combining usage, engagement, support, payment signals | \[ \] Yes / \[ \] No |
| At-Risk Customer        | Health score below threshold (e.g., &lt;60/100) for 2+ consecutive weeks | \[ \] Yes / \[ \] No |
| Lifecycle Stages        | Onboarding → Adoption → Growth → Renewal → At-Risk               | \[ \] Yes / \[ \] No |
| Customer Segments       | Tier definitions by ARR (Enterprise / Mid-Market / SMB)           | \[ \] Yes / \[ \] No |
| Expansion Opportunity   | Usage signals indicating readiness for upsell or cross-sell       | \[ \] Yes / \[ \] No |
| Playbook                | Automated workflow of tasks triggered by customer signal           | \[ \] Yes / \[ \] No |

**Instructions to customer:**

> Review each definition with your CS leadership team. Check "Yes" when approved. We cannot proceed with health score configuration until all terms are aligned.

---

### 1b. Kickoff Call

> **Purpose:** Present v0 data architecture and current state assessment. We walk in with work done — customer reacts, not creates from scratch.

#### Agenda (60-90 min)

| Time  | Topic                          | What Happens                                              |
| ----- | ------------------------------ | --------------------------------------------------------- |
| 0-15  | Walk through current state     | "Here's what we found from your CRM audit and intake"     |
| 15-30 | Present v0 data architecture   | Proposed integration flows from source systems to CSP     |
| 30-45 | Validate integration needs     | Confirm which systems connect, API access, data formats   |
| 45-55 | Definition alignment           | Review health score terms, lifecycle stages, segments     |
| 55-70 | Platform discussion            | If not yet selected: review evaluation criteria and shortlist |
| 70-80 | Identify gaps                  | Missing data, access issues, who owns resolution          |
| 80-90 | Next steps                     | Schedule refinement meetings, assign homework             |

#### What We Bring

- v0 data architecture diagram (built in Track B prep)
- CRM data quality assessment
- Platform evaluation matrix (if selection is in scope)
- Definition Alignment Document (pre-filled with our recommendations)
- Questions list (integration specifics, data gaps to validate)

#### What We Leave With

- Confirmed integration requirements and data source priorities
- Feedback on v0 architecture (info needed to create v1)
- Platform shortlist narrowed (or confirmed if pre-selected)
- Clear homework: CRM admin access, API credentials, historical churn data
- Alignment loop scheduled

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Iterate on platform selection, data architecture, and health score design until sign-off.

#### The Pattern

```
Kickoff Call (validate current state, integration needs)
    ↓
Update data architecture → v1
    ↓
Meeting 2 (platform selection, integration design) → v2
    ↓
Meeting 3 (health score design, playbook priorities) → v3
    ↓
Final Review → Sign-off
```

#### Meeting Types for CSP Implementation

| Meeting Type                  | Focus                                                    | Stakeholder                     |
| ----------------------------- | -------------------------------------------------------- | ------------------------------- |
| Platform Selection            | Vendor evaluation, demos, decision                       | VP CS, IT, Finance              |
| Integration Architecture      | Data flows, API requirements, sync schedules             | CS Ops, RevOps, IT/Engineering  |
| Health Score & Automation     | Health score components, playbook priorities, CTA design  | CS Leadership, CSM Leads        |
| Final Review                  | Complete strategic package walkthrough, sign-off          | All stakeholders                |

#### Typical Timeline

| Milestone               | Timing                                                |
| ----------------------- | ----------------------------------------------------- |
| Pre-kickoff prep        | 3-5 days                                              |
| Kickoff call            | Day 1 of engagement                                   |
| Platform selection      | 1-2 weeks (skip if pre-selected)                      |
| Meeting loop            | 2-3 weeks (depends on stakeholder availability)       |
| Final review + sign-off | When data model and health score design confirmed     |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything before proceeding to build.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by CS leadership
- [ ] Platform selected with budget approved and procurement initiated
- [ ] Data architecture finalized — all integration sources documented
- [ ] Health score components and weights defined
- [ ] Customer segments and lifecycle stages agreed
- [ ] Priority playbooks identified (onboarding, at-risk, renewal, expansion)
- [ ] Dashboard requirements documented (CSM views + leadership reporting)
- [ ] All CRM/integration admin access confirmed
- [ ] No blockers for engineering

#### Decision Point

- **Proceed to Engineering** → Platform procured, data model approved, ready to build
- **Loop back to Strategy** → Platform evaluation still ongoing or stakeholder alignment incomplete

> This project does NOT have a natural exit at Phase 1. The strategic deliverable (data model, health score design) is only valuable when configured in the platform.

---

## Phase 2: Engineering

> **Goal:** Build and configure the CSP with all integrations, health scoring, automations, and dashboards.
>
> **Output:** Fully configured platform tested and approved by customer.

This is the heaviest phase for CSP implementation. Mid-market platforms (ChurnZero, Vitally) typically take 4-8 weeks for the build; enterprise platforms (Gainsight) can take 3-6 months [1]. The build follows a specific sequence: integrations first, then data model, then health scores, then automations, then dashboards.

### Sub-Phases

```
2a Tech Spec → 2b Engineering Handoff → 2c Build → 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate strategic package into technical configuration specifications.

**Input:** Signed-off strategic package from Phase 1 (data architecture, health score design, playbook priorities)

**Output:** Draft tech spec containing:

- **Integration specifications:** For each source system (CRM, product analytics, support, billing) — connection method, sync frequency, field mappings, data transformation rules
- **Health score configuration:** Formula, component weights, threshold definitions, trend calculation logic
- **Automation rules:** For each playbook — trigger conditions, CTA types, task sequences, email templates
- **Dashboard specifications:** For each view — data sources, visualizations, filters, access permissions
- **Build sequence:** Recommended order of configuration (integrations → data model → health scores → automations → dashboards)

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs with engineer before building.

**Who attends:** Architect + CS Ops Engineer (or platform admin)

**Agenda (45-60 min):**

| Time  | Topic                    | What Happens                                                    |
| ----- | ------------------------ | --------------------------------------------------------------- |
| 0-15  | Walk through integration specs | Architect explains data architecture context                      |
| 15-30 | Review health score logic     | Walk through scoring formula, weights, thresholds           |
| 30-45 | Review automation specs       | Playbook triggers, CTA sequences, email templates           |
| 45-60 | Refine and approve            | Adjust specs, confirm build sequence, flag risks            |

**What Architect brings:**

- Strategic package (for context on WHY each decision was made)
- Draft tech spec (from 2a)
- Questions list (anything flagged as unclear — e.g., specific API endpoints, custom field requirements)

**What engineer leaves with:**

- Approved tech spec with clear build sequence
- Known risks/dependencies (e.g., "Product analytics API rate limits may require batched sync")
- Access credentials for all systems

---

### 2c. Build (Configure)

> **Purpose:** Build and configure the CSP across all integration, scoring, automation, and reporting layers.

**Input:** Approved tech spec from 2b

**Build sequence (order matters):**

| Step | Component                    | What Gets Configured                                          | Duration (Mid-Market) |
| ---- | ---------------------------- | ------------------------------------------------------------- | --------------------- |
| 1    | CRM Integration              | Managed package install, OAuth, account/contact/opp sync      | 3-5 days              |
| 2    | Additional Data Sources      | Product analytics, support ticketing, billing integrations    | 3-7 days              |
| 3    | Data Model & Segmentation    | Account hierarchy, customer segments, lifecycle stages         | 2-3 days              |
| 4    | Health Score Configuration   | Components, weights, thresholds, trend indicators             | 3-5 days              |
| 5    | Automated Playbooks          | Onboarding, at-risk, renewal, expansion CTAs and sequences    | 5-7 days              |
| 6    | Dashboards & Reporting       | CSM portfolio views, leadership dashboards, executive reports  | 3-5 days              |
| 7    | CSM Workspace Setup          | User accounts, territory assignments, notification preferences | 1-2 days              |

**Build tracking:**

- [ ] CRM integration: account sync validated, contact sync validated, opportunity sync validated
- [ ] Product analytics integration: usage data flowing, key events mapped
- [ ] Support ticketing integration: ticket volume and CSAT syncing
- [ ] Billing integration: contract dates, ARR/MRR, renewal dates syncing
- [ ] Customer segments configured and auto-assigning
- [ ] Lifecycle stages configured with progression rules
- [ ] Health score formula active and calculating across customer base
- [ ] Onboarding playbook built and tested
- [ ] At-risk playbook built and tested
- [ ] Renewal playbook built and tested (triggers 90-120 days before expiration)
- [ ] Expansion playbook built and tested
- [ ] CSM portfolio dashboard deployed
- [ ] Leadership executive dashboard deployed
- [ ] CSM user accounts created with territory assignments

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify the build works through controlled pilot before full rollout.

**Two types of testing:**

| Type              | Who      | Purpose                                                        |
| ----------------- | -------- | -------------------------------------------------------------- |
| Technical Testing | Our team | Verify integrations sync, health scores calculate, automations fire |
| Pilot Testing     | 2-4 CSMs | Validate platform works for daily workflows with real accounts |

**Technical testing checklist:**

- [ ] CRM sync: accounts, contacts, opportunities flowing correctly (spot-check 10 accounts)
- [ ] Product usage data: key events and metrics populating (validate against source system)
- [ ] Support data: ticket counts and CSAT scores syncing (compare to Zendesk/Intercom)
- [ ] Billing data: ARR/MRR, contract dates, renewal dates accurate
- [ ] Health scores: calculating for all accounts, trend indicators working
- [ ] Health score validation: compare scores to known churned/renewed accounts — do at-risk accounts score red? [3]
- [ ] Playbook triggers: test each playbook with controlled scenarios (e.g., drop health score below threshold → at-risk CTA appears)
- [ ] CTA creation and assignment: CTAs appearing in correct CSM's queue
- [ ] Email automations: digital CS emails sending to correct recipients with correct content
- [ ] Dashboards: all visualizations rendering, data accurate, filters working
- [ ] Sync timing: data freshness within acceptable latency (real-time or &lt;1 hour for CRM, &lt;24h for analytics)

**Pilot program (2-3 weeks):**

1. Select 2-4 CSMs representing different segments/tiers
2. Provide focused training on core workflows: health monitoring, CTAs, account views
3. Run pilot with regular check-ins (2x per week)
4. Collect feedback: usability, data accuracy, workflow fit, missing features
5. Identify issues: incorrect health scores, missing data, broken automations
6. Document and prioritize fixes
7. Refine playbooks and scoring based on pilot learnings

**Engineering sign-off checkpoint:**

- [ ] All integrations syncing correctly with no errors
- [ ] Health scores validated against known customer outcomes
- [ ] All playbook triggers tested and working
- [ ] Pilot CSMs confirm platform supports daily workflows
- [ ] Data quality issues resolved
- [ ] Ready for full team rollout

**Decision point:**

- **Proceed to Enablement** → Pilot successful, system stable, ready for full rollout
- **Loop back to Build** → Critical issues found, needs fixes before expanding

---

## Phase 3: Enablement

> **Goal:** Full CS team trained, legacy tools retired, platform adopted as primary operating system for CS.
>
> **Output:** Trained team with documentation, stabilized system through hypercare, no critical issues.

### Sub-Phases

```
3a Training Prep → 3b Training Sessions → 3c Hypercare → 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from strategic and technical documentation.

**Input:** Strategic package + tech specs + configured platform + pilot feedback

**Output:** Training package containing:

- **CSM Team Training** (90 min): Platform navigation, account 360 view, health score interpretation, CTA management, playbook workflows, daily routine
- **Leadership Training** (45 min): Portfolio health dashboard, ARR at risk view, renewal forecast, NRR tracking, CSM productivity metrics
- **Admin Training** (60 min): User management, playbook editing, health score weight adjustments, integration monitoring, report customization
- **Quick-reference guides:** One-page cheat sheets for daily CSM workflows
- **FAQ document:** Based on pilot feedback and common questions from similar implementations

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to full CS team.

**Training sessions by role:**

| Type       | Audience                      | Focus                                                              | Duration |
| ---------- | ----------------------------- | ------------------------------------------------------------------ | -------- |
| CSM Team   | All CSMs                      | Daily workflows: account views, CTAs, playbooks, health scores     | 90 min   |
| Leadership | VP CS, CCO, CS Directors      | Dashboard interpretation: portfolio risk, NRR, team productivity   | 45 min   |
| Admin      | CS Ops, RevOps Admin          | Platform admin: users, playbooks, scoring adjustments, integrations | 60 min   |

**Training delivery:**

1. Schedule sessions 1-2 weeks before planned go-live
2. Deliver CSM training with hands-on exercises using real accounts
3. Deliver leadership training focused on "what actions to take from this data"
4. Deliver admin training with step-by-step walkthrough of common maintenance tasks
5. Record all sessions as video walkthroughs for future reference
6. Set up a dedicated channel for post-training questions

**Output:**

- Trained team across all roles
- Video recordings for ongoing reference
- Questions log (feeds into FAQ updates)

---

### 3c. Hypercare

> **Purpose:** Intensive post-launch support to stabilize the system and drive adoption.

**Duration:** 2-4 weeks (CSP implementations need heavy hypercare due to integration complexity)

**What happens:**

- **Week 1:** Daily standups (15 min) to address issues. Monitor platform usage — are CSMs logging in? Are CTAs being worked?
- **Week 2:** Twice-weekly check-ins. Fix data quality issues, automation bugs, UX friction
- **Week 3-4:** Weekly office hours (30-min slot). Focus on refinement — adjusting health score weights, tuning playbook triggers, adding missing automations

**Key adoption metrics to track during hypercare:**

| Metric                   | Target                    | Red Flag                          |
| ------------------------ | ------------------------- | --------------------------------- |
| CSM daily active usage   | >80% within 30 days [5]  | &lt;50% after 2 weeks             |
| CTAs completed on time   | >70% completion rate      | &lt;40% after 2 weeks             |
| Health scores populating | 100% of accounts scored   | Any accounts with null scores     |
| Integration errors       | Zero critical sync failures | Any recurring sync errors        |

**When issues arise:**

- Data accuracy problems → Investigate integration sync, fix field mappings
- CSMs not using platform → 1:1 sessions to understand blockers, simplify workflows
- Health scores don't match reality → Adjust component weights, review data inputs
- Playbooks triggering incorrectly → Refine trigger conditions, add exclusion rules

**Output:** Stabilized system, adoption metrics on track, no critical issues outstanding

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm customer can operate the platform independently.

**Validation checkpoint:**

- [ ] All training sessions delivered and recorded
- [ ] CSM daily active usage above 80%
- [ ] CTAs being completed on schedule
- [ ] Health scores validated and trusted by CS team
- [ ] All integrations stable with no recurring errors
- [ ] No critical issues outstanding
- [ ] CS Ops admin can perform routine maintenance tasks
- [ ] Customer team can operate without daily support
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** → Customer is enabled, system stable, adoption healthy
- **Extend Hypercare** → Usage below target, ongoing data issues, team not confident

---

## Phase 4: Handoff

> **Goal:** Clean project close with maintenance plan established and retention/expansion path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the system, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule → 4b Internal Handoff → 4c External Handoff → 4d Project Close
                          (SME → Architect)                              (Archive + Debrief)
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At |
| ----------------------------- | -------------------- | ------------- |
| **Single Project**            | Customer CS Ops owns | 4c (External Handoff) |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention after the project is complete.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task                    | What to Check                                           | Red Flag Threshold                              |
| ------------------------------- | ------------------------------------------------------- | ----------------------------------------------- |
| Health Score Accuracy Audit     | Compare health scores to actual customer outcomes (renewals, churn) | >20% of churned accounts were scored "healthy" |
| Integration Sync Validation     | Verify all data sources syncing correctly, check error logs | Any recurring sync failures or data staleness >24h |
| CTA Completion Rate Review      | CSM team CTA completion and timeliness                   | Completion rate drops below 60%                 |
| Platform Usage Check            | CSM daily active usage and engagement                    | Usage drops below 70% of team                   |

**Quarterly Tasks:**

| Quarterly Task                  | What to Review                                          | Action if Off-Track                              |
| ------------------------------- | ------------------------------------------------------- | ------------------------------------------------ |
| Health Score Recalibration      | Component weights vs actual churn/renewal correlation    | Adjust weights, add/remove components            |
| Playbook Effectiveness Review   | CTA conversion rates, playbook completion rates          | Retire underperforming playbooks, create new ones |
| New Segment/Lifecycle Evaluation | New customer segments or lifecycle stages needed         | Configure new segments, adjust automation rules   |
| Dashboard & Reporting Audit     | Are dashboards being used? Are reports accurate?         | Remove unused dashboards, add requested views     |

**After First Business Cycle (60-90 days post-launch):**

- Validate health score predictive accuracy against first full cycle of renewals
- Review at-risk playbook effectiveness: did interventions reduce churn?
- Assess CSM productivity impact: time savings vs pre-CSP baseline
- First NRR comparison: compare to pre-implementation baseline

**Refinement Triggers (when to re-engage):**

| Trigger                          | Threshold                                     | Response                                          |
| -------------------------------- | --------------------------------------------- | ------------------------------------------------- |
| Health score accuracy degrades   | >25% false positives/negatives for 2+ months  | Re-engage SME for health score recalibration      |
| New product line or segment      | Major business change requiring new data model | Scope expansion project for new integrations      |
| CSM team grows significantly     | >50% headcount increase                       | Re-engage for workspace restructure and retraining |
| Platform migration               | Decision to switch CSP vendors                 | Scope new implementation project                  |

**Every 6-12 Months:**

- Full health score model recalibration with updated churn/renewal data
- Integration architecture review — any new systems to connect?
- Playbook library audit — retire stale playbooks, create new ones for emerging patterns
- Platform feature review — are there new vendor features to enable?
- NRR trend analysis: target improvement of 5-15% points over pre-implementation baseline [2]

---

### 4b. Internal Handoff (SME → Architect)

> **Purpose:** Transfer context so Architect can manage ongoing relationship.

**What the Architect needs to know:**

- What was built and why: platform choice, integration architecture, health score methodology, playbook strategy
- Customer context: key stakeholders (VP CS, CS Ops admin, CSM leads), communication preferences, any political dynamics
- Known limitations: integrations that required workarounds, data quality caveats, features not yet enabled
- Common issues and resolution: typical sync errors, health score edge cases, playbook tuning
- When to escalate back to SME
- **Maintenance schedule** (if Dedicated engagement — Architect runs this)

**Escalation guidelines:**

| Issue Type                                          | Who Handles                              | Example                                         |
| --------------------------------------------------- | ---------------------------------------- | ------------------------------------------------ |
| New CSM onboarding, dashboard filter changes        | Architect                                | "New CSM hired, needs account assignment"        |
| Playbook trigger adjustments, CTA priority changes  | Architect                                | "Renewal playbook should start at 120 days"      |
| Health score formula changes, new integration       | SME ("anything with electrical")         | "Need to add NPS data as health score component" |
| Platform migration or major restructure             | SME                                      | "Moving from ChurnZero to Gainsight"             |

**For Dedicated engagements:** Architect also receives the maintenance schedule (4a) and becomes responsible for executing it. SME walks Architect through each maintenance task with a live demonstration.

---

### 4c. External Handoff

> **Purpose:** Formal project completion with customer.

**Final project meeting:**

- Review what was delivered: integrations, health scores, playbooks, dashboards, training materials
- Walk through documentation package
- Demonstrate maintenance tasks live (health score audit, integration monitoring, playbook editing)
- Confirm admin access fully transferred to CS Ops team
- Answer final questions
- Make it explicit: "Project complete"
- **For Single Project engagements:** Walk through maintenance schedule in detail and record a video walkthrough

**Documentation package:**

- Integration architecture map (source systems, sync methods, field mappings)
- Health score methodology document (components, weights, thresholds, recalibration guide)
- Playbook documentation (trigger conditions, CTA sequences, email templates)
- Admin guide (user management, playbook editing, dashboard customization, integration troubleshooting)
- All training video walkthroughs
- FAQ document
- Maintenance Schedule with escalation paths
- Vendor support contact information

**Output:** Customer owns the system. CS Ops admin can operate independently. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location
- [ ] Handoff documentation complete
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized

#### Internal Debrief (Optional but Recommended)

- What went well? (integration smooth, health scores accurate from pilot)
- What would we do differently? (data quality audit earlier, more pilot time)
- Any learnings to feed back into SOPs? (new integration patterns, health score shortcuts)
- Platform-specific learnings to document? (vendor quirks, API gotchas)

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell → Downsell → Retry    |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (quarterly health score recalibration, playbook optimization, new integration builds)
   ↓ if no
2. Downsell: Another one-time project (CS-to-Sales handoff workflow, expansion revenue playbook, digital CS automation)
   ↓ if yes
3. Retry retainer at end of next project cycle
```

**Script:**

> "Now that your CSP is live and your team is using it daily, there are two ways we can continue working together. Option 1: We handle ongoing optimization — quarterly health score recalibration, new playbook development, integration expansions — on a managed services retainer. Option 2: If there's a specific next project like building out your expansion revenue workflow or CS-to-Sales handoff process, we can scope that out. Which sounds more interesting?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On [date ~90 days out], we'll review how the CSP is performing — health score accuracy, playbook effectiveness, NRR impact — and see if any adjustments are needed."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                           |
| ------------------- | ------------------------------------------------------ |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks        |
| 2. Review metrics   | Pull platform adoption data, health score accuracy, NRR trend |
| 3. Decide ownership | Can Architect handle this check-in, or need SME?              |
| 4. Prep materials   | If SME needed, brief them. If Architect, prep talking points. |

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- Definition Alignment Document (health score, lifecycle, segment definitions — signed off)
- Platform Evaluation Matrix (if platform selection was in scope)
- Data Architecture Map (source systems, field mappings, sync rules)
- Health Score Design Document (components, weights, thresholds, methodology)

**Technical Deliverables:**

- Configured CRM integration (Salesforce/HubSpot ↔ CSP)
- Configured product analytics integration
- Configured support ticketing integration
- Configured billing/subscription integration
- Health score formula active and calculating
- Customer segments and lifecycle stages configured
- 4+ automated playbooks (onboarding, at-risk, renewal, expansion)
- CSM portfolio dashboards
- Leadership/executive dashboards
- Digital CS email sequences (if applicable)

**Documentation Package:**

- Training video walkthroughs (CSM, Leadership, Admin)
- Quick-reference guides for CSM daily workflows
- Admin guide for CS Ops (platform maintenance, troubleshooting)
- Health score methodology document
- Integration architecture documentation
- FAQ document
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
| **Phase 1: Strategy**    | Platform selected, data architecture approved, health score designed   | Stakeholders signed off on definitions, platform, data model, health score     |
| **Phase 2: Engineering** | Fully configured CSP with integrations, scoring, automations, dashboards | All integrations syncing, pilot tested, customer approved                      |
| **Phase 3: Enablement**  | Trained CS team, retired legacy tools, system stabilized               | All training delivered, usage >80%, hypercare complete, team operating independently |
| **Phase 4: Handoff**     | Independent customer + archived project                                | Internal/external handoffs complete, maintenance plan in place, project closed |

### Project Profile

This is a **Technical-heavy / Balanced** project:

| Phase          | Weight  | Rationale                                                  |
| -------------- | ------- | ---------------------------------------------------------- |
| Strategy       | 20-30%  | Platform selection, data architecture, health score design |
| Engineering    | 40-50%  | Heavy integration work, scoring, automations, dashboards   |
| Enablement     | 15-25%  | Pilot + full team training + hypercare                     |
| Handoff        | 10-15%  | Standard handoff with detailed admin documentation         |

### Key Industry Context

The global Customer Success Platforms market was valued at approximately $1.86 billion in 2024 and is projected to reach $9.17 billion by 2032 at a 22.1% CAGR [6]. A well-deployed CSP can reduce churn by 25-32% within the first 6-12 months [1]. However, success depends on implementation quality: companies that base decisions on comprehensive customer success metrics achieve up to 23% higher revenue growth [7].

Average B2B SaaS churn benchmarks: annual gross churn of 10-15% for mid-market is typical, with best-in-class companies under 7% [8]. Median NRR for venture-backed SaaS is 106%, while best-in-class exceeds 130% [2]. A CSP implementation directly targets these metrics by making churn signals visible and actionable before renewal dates.

Advanced health scoring systems can identify potential churn risks up to 90 days in advance by examining user behavior patterns [9].

---

## References

[1] [The CS Cafe - Best Customer Success Platforms Comparison Guide](https://www.thecscafe.com/p/best-customer-success-platforms)
[2] [Optifai - B2B SaaS NRR Benchmark: 97-118% by Segment](https://optif.ai/learn/questions/b2b-saas-net-revenue-retention-benchmark/)
[3] [Gainsight - Customer Health Scores Explained](https://www.gainsight.com/blog/customer-health-scores/)
[4] [Avoma - Gainsight vs ChurnZero: Objective Evaluation](https://www.avoma.com/blog/gainsight-vs-churnzero)
[5] [Custify - 2026 Customer Success Industry Market Statistics](https://www.custify.com/blog/customer-success-statistics/)
[6] [OpenPR - Customer Success Platforms Market Growth](https://www.openpr.com/news/4223826/customer-success-platforms-market-growth-key-drivers-to-push)
[7] [DigiFlute - The Ultimate Guide to Customer Success Metrics 2025](https://www.digiflute.com/the-ultimate-guide-to-customer-success-metrics-that-drive-business-growth-in-2025/)
[8] [Vitally - B2B SaaS Churn Rate Benchmarks 2025](https://www.vitally.io/post/saas-churn-benchmarks)
[9] [Union Square Consulting - Predict Churn with a Customer Health Scoring System](https://unionsquareconsulting.com/newsletter/predict-churn-with-a-customer-health-scoring-system/)
