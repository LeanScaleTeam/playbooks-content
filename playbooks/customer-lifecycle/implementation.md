# Customer Lifecycle — Implementation

## Project One-Pager

> Quick reference for architects. One per project type. Fill this out FIRST — it serves as the project's identity card.

### Customer Lifecycle One-Pager

#### Project Type

- Category: Balanced (Strategic + Technical)
- Primary Deliverable: Fully automated customer lifecycle stage structure in CRM with stage definitions, automated transitions, date stamps, and velocity reporting

##### Phase Relevance

| Phase          | Applies? | Notes                                                    |
| -------------- | -------- | -------------------------------------------------------- |
| 1. Strategy    | Yes      | 2-3 refinement loops for stage definitions and criteria  |
| 2. Engineering | Yes      | CRM field creation, automation builds, CS platform sync  |
| 3. Enablement  | Yes      | CSM training on manual transitions + dashboard usage     |
| 4. Handoff     | Yes      | Internal + External with maintenance schedule            |

· · ·

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │    Heavy     │     │    Heavy     │     │    Medium    │     │    Medium    │
  │ 1a→1b→1c→1d │     │ 2a→2b→2c→2d │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   2-3 refinement       CRM fields +         CSM training +       Internal +
   loops + criteria     CS platform sync     dashboard usage      External handoff
```

**This project's flow:**
- Full 4-phase. Heavy strategy (stage definitions and entry/exit criteria require stakeholder alignment), heavy engineering (CRM fields, Flows/workflows, date stamps, CS platform integration), medium enablement (CSM training and dashboard walkthrough), standard handoff.
- If customer has a CS platform (Gainsight, ChurnZero, Catalyst), Phase 2 extends for integration work.
- No phases skipped — every customer lifecycle project runs all four.

· · ·

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Watch intro video explaining what a customer lifecycle is and why stage tracking matters
- [ ] Complete intake form: current customer stages (formal or informal), CS team size, CS platform in use, current reporting gaps
- [ ] Get VP CS and RevOps Leader sign-off on Definition Alignment Document (stage names, "customer" definition)
- [ ] Provide CRM admin access and CS platform credentials (if applicable)

##### Track B: Architect Prep
- [ ] Pull CRM field audit — existing Account status/stage fields, date fields, automations
- [ ] Audit existing automations touching Account status or stage fields
- [ ] Run diagnostic against current-state rubric (Red/Yellow/Green for lifecycle tracking maturity)
- [ ] Draft v0 lifecycle stage structure based on industry best practice (4-6 stages) and intake form responses

· · ·

#### Refinement Loop (1b -> 1c -> 1d)

| Meeting      | Sub-Phase | Focus                                                      | Stakeholder               | Output                          |
| ------------ | --------- | ---------------------------------------------------------- | ------------------------- | ------------------------------- |
| Kickoff      | 1b        | Present v0 stage structure, validate pain points           | VP CS, RevOps, CS Manager | Feedback for v1                 |
| Refinement 1 | 1c        | Review v1 stages, define entry/exit criteria per stage     | VP CS, CS Manager         | v2 with criteria documented     |
| Refinement 2 | 1c        | Finalize criteria, confirm date stamp requirements         | RevOps, CS Ops            | v3 with tech requirements       |
| Sign-Off     | 1d        | Full walkthrough of lifecycle design, approve for build    | All stakeholders          | Final strategic package         |

· · ·

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held
- [ ] 1c. Refinement loop complete (v0 -> vFinal)
- [ ] 1d. Strategic sign-off obtained

##### Phase 2: Engineering
- [ ] 2a. Tech spec created (field mappings, automation logic, date stamp schema)
- [ ] 2b. Engineering handoff meeting held
- [ ] 2c. Build complete (fields, automations, manual flows, CS platform sync)
- [ ] 2d. QA/Test + customer sign-off

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped
- [ ] 3b. Training sessions delivered (CS team + leadership)
- [ ] 3c. Hypercare period complete (2 weeks)
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff (SME -> Architect) complete
- [ ] 4c. External handoff (LeanScale -> Customer) complete
- [ ] 4d. Project closed and archived

· · ·

#### Document Types

##### Working Documents (iterate together)

| Document                         | Purpose                                              | When Complete                                    |
|----------------------------------|------------------------------------------------------|--------------------------------------------------|
| Intake form                      | Capture current state, pain points, CS team structure | All fields filled by customer                    |
| Lifecycle stage definition table | Define each stage with entry/exit criteria            | All stages have measurable criteria              |
| Date stamp field inventory       | List all timestamp fields needed per stage            | Naming conventions confirmed, calculations noted |
| Gap analysis                     | Compare current vs. future state                      | All gaps prioritized with resolution plan        |

##### Deliverables (polished outputs)

| Deliverable                          | Created From                     | Customer Uses For                      |
|--------------------------------------|----------------------------------|----------------------------------------|
| Lifecycle stage reference document   | Stage definition table           | CSM daily reference, new hire training |
| Current/future state Mermaid diagram | Gap analysis + stage definitions | Leadership presentation                |
| Velocity metrics dashboard spec      | Date stamp inventory             | Board reporting, QBR preparation       |

· · ·

#### Enablement Details

##### Training Types

| Type       | Audience                              | Focus                                                 | Duration |
| ---------- | ------------------------------------- | ----------------------------------------------------- | -------- |
| Leadership | VP CS, CS Director                    | Interpret lifecycle funnel, velocity metrics, QBR use | 30 min   |
| Technical  | RevOps, CS Ops, CRM Admin             | Field maintenance, automation logic, troubleshooting  | 60 min   |
| End User   | CSMs, Account Managers                | Manual transitions, when/how to update stages         | 45 min   |

##### Hypercare
- Applies: Yes
- Duration: 2 weeks post-go-live
- Office Hours: Yes — weekly 30-min slot for CSM questions and edge case resolution

##### Training Assets to Create
- [ ] Video walkthrough: Lifecycle stage walkthrough and CRM navigation (5 min)
- [ ] Video walkthrough: Manual stage transition process via screen flow (3 min)
- [ ] Doc: Lifecycle stage definitions with entry/exit criteria quick-reference
- [ ] Doc: FAQ for edge cases (customer reactivation, multi-product scenarios, backdating)
- [ ] Doc: Dashboard interpretation guide for leadership

· · ·

#### Handoff & Retention

##### Internal Handoff (SME -> Architect)
- Key context for Architect: Lifecycle stage definitions, automation logic, which transitions are manual vs. automated, CS platform sync rules
- Escalation trigger: Any changes to stage definitions, new stage additions, automation modifications, CS platform integration changes

##### External Handoff (LeanScale -> Customer)
- Final meeting agenda: Review all stages, walk through maintenance schedule, demonstrate dashboard, confirm no outstanding issues
- Documentation package: Stage definitions, automation logic reference, field API names, dashboard access, training recordings, FAQ

##### Maintenance Schedule
- Monthly: Stage distribution audit, data quality spot-check
- Quarterly: Full criteria review, velocity metric validation
- Who owns: Single project = customer owns | Dedicated = Architect owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services -> if no -> Downsell: Customer Health Score project or Renewal Management project -> Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~90 days post-launch
- Internal prep trigger: 2 weeks before
- Decision: Architect handles if minor tweaks / SME needed if stage restructuring required

· · ·

#### Definition Alignment Terms

| Term                   | Typical Definition                                                                                  |
| ---------------------- | --------------------------------------------------------------------------------------------------- |
| Customer               | An Account with at least one Closed Won Opportunity and active subscription                         |
| Lifecycle Stage        | The current phase of a customer's post-sale journey (mutually exclusive, one stage per account)      |
| Entry Criteria         | Measurable conditions that must be true for a customer to enter a lifecycle stage                    |
| Exit Criteria          | Measurable conditions that trigger transition out of a stage into the next                           |
| Time to Value (TTV)    | Duration from Closed Won to customer achieving first meaningful outcome from the product             |
| Stage Velocity         | Average time customers spend in a given lifecycle stage before transitioning to the next             |
| At-Risk                | A lifecycle stage indicating the customer shows signals of potential churn                           |
| Churned                | A lifecycle stage for customers who have cancelled or not renewed their subscription                 |

· · ·

#### Common Gotchas
- Too many stages (8+) create confusion and reduce CSM adoption -> Start with 4-6 core stages, expand later
- No enforcement mechanism for manual transitions -> CSMs stop updating, data goes stale within weeks -> Use guided screen flows at natural workflow moments
- Backward stage progression allowed -> Breaks funnel metrics and velocity calculations -> Build validation rules enforcing linear progression (admin override for exceptions)
- CRM and CS platform showing different stages -> Teams lose trust in data -> Establish single source of truth upfront and document "which system wins" per stage
- Date stamp fields not populating on manual transitions -> Missing velocity data -> Ensure screen flows auto-populate timestamps, not just automated transitions
- Existing customers not migrated to stages at go-live -> Lifecycle funnel shows zero customers -> Run data migration and backfill in Phase 2c

· · ·

#### Methodology Options

| Option                         | When to Use                                                     | Complexity |
| ------------------------------ | --------------------------------------------------------------- | ---------- |
| Simple (4 stages, CRM-only)   | Small CS team (&lt;5 CSMs), no CS platform, Salesforce or HubSpot  | Low        |
| Standard (5-6 stages, CRM + manual flows) | Mid-size CS team, mix of automated and manual transitions | Medium     |
| Advanced (6+ stages, CRM + CS platform integration) | Large CS org, Gainsight/ChurnZero in place, bi-directional sync needed | High |

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on lifecycle stage definitions, entry/exit criteria, and date stamp requirements.
>
> **Output:** Definition Alignment Document + Lifecycle Stage Design Package (signed off by VP CS and RevOps).

### 1a. Pre-Kickoff

> Two parallel tracks run after the AE closes and before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                         | Format             |
| ----------------------------- | --------------------------------------------------------------- | ------------------ |
| Intro video                   | Explain what customer lifecycle tracking is and why it matters  | Video (5-10 min)   |
| Definition Alignment Document | Get stakeholder sign-off on key terms (Customer, Lifecycle Stage, TTV, Churned) | Google Doc |
| Pre-filled intake form        | Capture current CS process, stage names in use, team size, tools, reporting gaps | Google Form or Doc |

**What the intake form covers:**
- Current customer stage/status fields in CRM (even informal ones)
- CS team size and structure
- CS platform in use (Gainsight, ChurnZero, Catalyst, or none)
- Current reporting: what dashboards exist for customer funnel today
- Key pain points: "What questions about your customer base can you not answer today?"
- Definition of "customer" (Closed Won? Active subscription? Paid only?)

**Completion tracking:** Architect follows up. Don't cancel kickoff if incomplete, but push hard on the Definition Alignment Document — without agreed-upon terms, the kickoff call spins.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                                  | Output                                          |
| ---- | ----------------------------------------------------------------------- | ------------------------------------------------ |
| 1    | Pull CRM field inventory (Account object: status fields, date fields)   | Field audit spreadsheet                          |
| 2    | Audit existing automations touching Account stage/status                | Automation inventory with trigger logic           |
| 3    | Run lifecycle maturity diagnostic (Red/Yellow/Green)                     | Current-state assessment score                    |
| 4    | Draft v0 lifecycle stage structure (4-6 stages based on industry norms) | v0 stage definition table with ASSUMED criteria   |
| 5    | Prepare kickoff assets (transition flowchart draft, questions list)      | Kickoff presentation materials                    |

**Industry benchmark for v0 stage structure:**
A typical B2B SaaS customer lifecycle has 4-6 core stages. The recommended starting point:

| Stage          | Description                              | Typical Duration      |
|----------------|------------------------------------------|-----------------------|
| New Customer   | Closed Won, not yet onboarded            | 0-7 days              |
| Onboarding     | Active implementation / setup in progress| 14-90 days            |
| Adopting       | Using product, working toward first value| 30-90 days            |
| Healthy/Mature | Fully adopted, seeing ongoing value      | Ongoing               |
| At-Risk        | Churn signals detected                   | Variable              |
| Churned        | Subscription cancelled or not renewed    | Terminal               |

**Critical:** Mark everything as ASSUMED. The kickoff call validates.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building anything.

| Term                | Our Definition                                                                     | Internally Approved? |
| ------------------- | ---------------------------------------------------------------------------------- | -------------------- |
| Customer            | An Account with at least one Closed Won Opportunity and active subscription         | [ ] Yes / [ ] No     |
| Lifecycle Stage     | The current phase of a customer's post-sale journey (mutually exclusive)             | [ ] Yes / [ ] No     |
| Time to Value (TTV) | Duration from Closed Won to the customer achieving first meaningful product outcome  | [ ] Yes / [ ] No     |
| Onboarding Complete | Customer has completed implementation steps and is actively using the product        | [ ] Yes / [ ] No     |
| At-Risk             | Customer showing churn indicators (low usage, missed QBR, support escalation)        | [ ] Yes / [ ] No     |
| Churned             | Customer has cancelled or failed to renew their subscription                         | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your CS leadership and RevOps team. Check "Yes" when approved. We cannot proceed with engineering until all terms are aligned — disagreements on definitions mid-build cause rework and scope creep.

---

### 1b. Kickoff Call

> **Purpose:** Present v0 lifecycle stage structure and get alignment. We walk in with a draft — customer reacts, not creates from scratch.

#### Agenda (60-90 min)

| Time  | Topic                         | What Happens                                                  |
| ----- | ----------------------------- | ------------------------------------------------------------- |
| 0-15  | Walk through v0 stage design  | "Here's the lifecycle we drafted from your intake responses"  |
| 15-30 | Validate current pain points  | Confirm what's broken today with customer tracking            |
| 30-45 | Definition alignment review   | Walk through each term, capture disagreements                 |
| 45-60 | Discuss transition logic      | Which transitions should be automated vs. CSM-driven          |
| 60+   | Next steps                    | Schedule refinement calls, assign homework                    |

#### What We Bring

- v0 lifecycle stage definition table (built in Track B prep)
- Draft transition flowchart (Mermaid or whiteboard)
- CRM field audit findings (what exists today)
- Questions list (what we need validated)
- Definition Alignment Document (pre-filled with our recommendations)

#### What We Leave With

- Feedback and corrections on v0 stage structure (info needed to create v1)
- Confirmed or contested definitions (clear blockers if sign-off needed from absent stakeholders)
- Understanding of which transitions must be automated vs. manual
- Homework assignments: customer to confirm criteria with CS team, provide any missing data

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Iterate on lifecycle design until stakeholder sign-off. Typically 2-3 refinement meetings.

#### The Pattern

```
Kickoff Call (present v0, gather feedback)
    |
v1 (incorporate feedback, draft entry/exit criteria)
    |
Refinement 1 (review v1, workshop criteria details)
    |
v2 (finalize criteria, add date stamp requirements)
    |
Refinement 2 (review v2 with RevOps, confirm tech feasibility)
    |
v3 (final version)
    |
Sign-Off (approve for engineering)
```

#### Before Each Meeting

1. Process previous meeting transcript/notes
2. Update lifecycle stage design (v[n-1] -> v[n])
3. Prepare questions for next validation round

#### During Each Meeting

1. Walk through current version of stage definitions and criteria
2. Capture corrections and refinements
3. Validate what's now CONFIRMED
4. Identify remaining ASSUMED items

#### After Each Meeting

1. Update stage definitions based on meeting output
2. Track what moved from ASSUMED -> CONFIRMED
3. Update working documents (stage table, criteria matrix)

#### Meeting Types for This Project

| Meeting Type          | Focus                                                  | Stakeholder               |
| --------------------- | ------------------------------------------------------ | ------------------------- |
| CS Leadership         | Stage definitions, what business decisions lifecycle enables | VP CS, CS Director    |
| CS Operations         | Entry/exit criteria, manual vs. automated transitions  | CS Manager, CS Ops        |
| RevOps/Technical      | CRM field design, automation logic, date stamp schema  | RevOps Lead, CRM Admin    |
| Final Review          | Full lifecycle design walkthrough, sign-off             | All stakeholders          |

#### Typical Timeline

| Milestone               | Timing                                          |
| ----------------------- | ----------------------------------------------- |
| Pre-kickoff prep        | 3-5 days                                        |
| Kickoff call            | Day 1 of engagement                             |
| Refinement meetings     | 1-2 weeks (2-3 meetings)                        |
| Final review + sign-off | When all stage criteria are CONFIRMED            |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything needed before building in the CRM.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by VP CS and RevOps
- [ ] All lifecycle stages defined with entry/exit criteria
- [ ] Automated vs. manual transition logic confirmed for each stage change
- [ ] Date stamp field requirements documented with naming conventions
- [ ] CS platform integration scope defined (if applicable)
- [ ] Customer understands what we're building and timeline for engineering
- [ ] No blockers for engineering

#### Decision Point

- **Proceed to Engineering** -> Customer wants lifecycle built and automated in CRM (standard path)
- **This project always proceeds to Engineering** — the strategic deliverable (stage definitions) requires system implementation to deliver value

---

## Phase 2: Engineering

> **Goal:** Build and test the lifecycle stage structure, automations, and reporting in the CRM.
>
> **Output:** Fully configured lifecycle with automated transitions, date stamps, manual flows, and CS platform sync (if applicable). Tested and customer-approved.

| Project Type    | Engineering Weight | This Project                                              |
| --------------- | ------------------ | --------------------------------------------------------- |
| Balanced        | Heavy (50-60%)     | CRM fields, Flows/Workflows, date stamps, platform sync  |

### Sub-Phases

```
2a Tech Spec -> 2b Engineering Handoff -> 2c Build -> 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate lifecycle stage design into CRM-specific technical specifications.

**Input:** Signed-off lifecycle design package from Phase 1

**What happens:**

1. Architect (with tooling support) receives stage definitions, entry/exit criteria, and date stamp requirements
2. Maps each stage to CRM picklist values, date fields, and automation triggers
3. Outputs draft tech spec with field API names, Flow/Workflow logic, and build sequence

**Output:** Draft tech spec containing:

- **Field specifications:**
  - `Customer_Lifecycle_Stage__c` (Picklist on Account: New Customer, Onboarding, Adopting, Healthy, At-Risk, Churned)
  - `Lifecycle_[StageName]_Entry_Date__c` (Date field for each stage)
  - `Days_in_Current_Stage__c` (Formula field calculating duration)
  - `Time_to_Value_Days__c` (Formula: Adopting Entry Date - New Customer Entry Date)

- **Automation logic:**
  - Trigger: Opportunity Closed Won -> Set Stage to "New Customer," populate entry date
  - Trigger: Onboarding milestone met -> Set Stage to "Onboarding," populate entry date
  - Trigger: Product usage threshold reached -> Set Stage to "Adopting"
  - Manual: CSM marks Onboarding Complete via screen flow
  - Manual: CSM flags At-Risk via screen flow with required reason field

- **Validation rules:**
  - Prevent backward stage progression (unless Admin profile)
  - Require reason field for At-Risk stage entry
  - Prevent manual edit of date stamp fields (automation-only)

- **CS platform sync rules (if applicable):**
  - Source of truth mapping per stage
  - Sync frequency and direction
  - Conflict resolution logic

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs with engineer before building.

**Who attends:** Architect + Engineer (or CRM Admin)

**Agenda (30-45 min):**

| Time  | Topic              | What Happens                                              |
| ----- | ------------------ | --------------------------------------------------------- |
| 0-15  | Walk through specs | Architect explains strategic context + tech spec output          |
| 15-30 | Engineer questions | Clarify field dependencies, Flow trigger order, edge cases|
| 30-45 | Refine and approve | Adjust specs, confirm build sequence                      |

**What Architect brings:**
- Strategic package (lifecycle stage design)
- Draft tech spec (from 2a)
- Questions list (anything flagged as unclear, e.g., "Which object tracks product usage?")

**What engineer leaves with:**
- Approved tech spec
- Build sequence: Fields first -> Automations second -> Manual flows third -> Validation rules fourth -> CS platform sync last
- Known risks (e.g., existing automations that may conflict)

---

### 2c. Build (Configure)

> **Purpose:** Build the lifecycle stage structure in the customer's CRM.

**Input:** Approved tech spec from 2b

**Build sequence:**

| Step | Component                              | System              | Estimated Time |
|------|----------------------------------------|----------------------|----------------|
| 1    | Create lifecycle picklist field        | Salesforce/HubSpot   | 30 min         |
| 2    | Create date stamp fields per stage     | Salesforce/HubSpot   | 1-2 hours      |
| 3    | Add fields to Account page layout      | Salesforce/HubSpot   | 30 min         |
| 4    | Set field-level security               | Salesforce/HubSpot   | 30 min         |
| 5    | Build automated transition Flows       | Salesforce Flow / HubSpot Workflow | 3-5 hours |
| 6    | Build manual transition screen flow    | Salesforce Flow / HubSpot | 2-3 hours |
| 7    | Build validation rules                 | Salesforce/HubSpot   | 1-2 hours      |
| 8    | Create formula fields (Days in Stage, TTV) | Salesforce/HubSpot | 1 hour     |
| 9    | Configure CS platform sync (if applicable) | Gainsight/ChurnZero | 3-5 hours  |
| 10   | Build lifecycle funnel dashboard       | Salesforce/HubSpot   | 2-3 hours      |
| 11   | Build velocity metrics report          | Salesforce/HubSpot   | 1-2 hours      |
| 12   | Run data migration (assign existing customers to stages) | Data loader/import | 2-4 hours |

**Execution approach for this project:** Manual build for Steps 1-8 (CRM configuration requires precision and edge case handling). Steps 10-11 (reporting/dashboard builds follow established patterns).

**Build tracking:**

- [ ] Component 1: Lifecycle picklist field created
- [ ] Component 2: Date stamp fields created (one per stage)
- [ ] Component 3: Fields added to page layout
- [ ] Component 4: Field-level security configured
- [ ] Component 5: Automated transitions built and individually tested
- [ ] Component 6: Manual transition screen flow built
- [ ] Component 7: Validation rules active
- [ ] Component 8: Formula fields (Days in Stage, TTV) calculating correctly
- [ ] Component 9: CS platform sync configured (if applicable)
- [ ] Component 10: Lifecycle funnel dashboard built
- [ ] Component 11: Velocity metrics report built
- [ ] Component 12: Data migration complete (existing customers assigned to stages)

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify the lifecycle works end-to-end and get customer approval.

**Technical testing checklist:**

- [ ] Automated transition: Closed Won Opportunity -> Account moves to "New Customer" + date stamp populates
- [ ] Automated transition: Onboarding trigger fires -> Account moves to "Onboarding" + date stamp populates
- [ ] Manual transition: CSM uses screen flow to move customer -> Stage updates + date stamp populates + reason captured
- [ ] Validation rule: Backward progression blocked (test moving Healthy -> Onboarding, expect error)
- [ ] Validation rule: At-Risk requires reason field (test blank submission, expect error)
- [ ] Formula field: Days in Current Stage calculates correctly
- [ ] Formula field: Time to Value calculates correctly (Adopting Entry Date - New Customer Entry Date)
- [ ] CS platform sync: Stage change in CRM reflects in CS platform (and vice versa, if bi-directional)
- [ ] Dashboard: Lifecycle funnel shows correct customer counts by stage
- [ ] Report: Velocity report shows accurate time-in-stage metrics
- [ ] Data migration: Spot-check 10-15 existing customers for correct stage assignment
- [ ] Edge case: Customer reactivation (Churned -> New Customer) handled correctly
- [ ] Edge case: Multi-product customer with different lifecycle stages per product (if applicable)

**Customer testing (UAT):**

- Select 2-3 CSMs for pilot testing
- Have them process 5-10 real customer transitions using screen flows
- Gather feedback on usability: Is the screen flow intuitive? Are stage definitions clear in context?
- Address critical issues before full rollout
- Get formal sign-off from CS leadership

**Engineering sign-off checkpoint:**

- [ ] All lifecycle fields and automations match tech spec
- [ ] All technical tests passing
- [ ] Data migration complete and verified
- [ ] Customer has tested and approved
- [ ] Ready for enablement

**Decision point:**

- **Proceed to Enablement** -> System is built, needs training/adoption
- **Loop back to Build** -> Issues found in UAT, needs fixes

---

## Phase 3: Enablement

> **Goal:** CS team can use the lifecycle system in their daily workflow.
>
> **Output:** Trained team with documentation, stabilized system, no critical issues.

### Sub-Phases

```
3a Training Prep -> 3b Training Sessions -> 3c Hypercare -> 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from strategic and technical documentation.

**Input:** Lifecycle stage design + tech specs + built system screenshots

**Output:** Training package containing:

- **CSM Training Deck:** Stage definitions, when to use manual transitions, screen flow walkthrough, common scenarios
- **Leadership Guide:** How to read the lifecycle funnel dashboard, velocity metrics, what actions to take when bottlenecks appear
- **Technical Reference:** Field API names, automation logic, how to add/modify stages (for RevOps/Admin)
- **Quick-Reference One-Pager:** Stage definitions with entry/exit criteria — print-friendly for CSM desks
- **FAQ Document:** Edge cases (customer reactivation, stage disputes, backdating requests)

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to customer team.

**Training sessions by audience:**

| Session               | Audience              | Focus                                                                        | Duration |
|-----------------------|-----------------------|------------------------------------------------------------------------------|----------|
| CSM Team Training     | All CSMs              | Stage definitions, manual transition process, when to flag At-Risk, daily workflow integration | 45 min |
| Leadership Training   | VP CS, CS Directors   | Dashboard interpretation, velocity metrics, using funnel data in QBRs and board reporting | 30 min |
| Technical Training    | RevOps, CRM Admin     | Automation logic, field maintenance, adding new stages, troubleshooting      | 60 min   |

**Training delivery:**

1. Schedule CSM session first (they're the primary users)
2. Deliver live training with screen sharing in the actual CRM
3. Record all sessions as video recordings for future reference
4. Walk through 3-5 real customer scenarios during CSM training
5. Answer questions, note gaps for FAQ updates

**Output:**

- Trained stakeholders at all levels
- Video recordings (3 sessions)
- Updated FAQ based on questions raised

---

### 3c. Hypercare

> **Purpose:** Intensive post-launch support to stabilize the lifecycle system.

**Duration:** 2 weeks

**What's included:**

- Weekly 30-min office hours slot for CSM questions
- Bug triage within 4 business hours
- Quick fixes for automation issues or edge cases discovered in production
- Monitoring data quality: Are CSMs actually updating stages? Are automations firing?

**What's out of scope:**

- New stage additions (scope as change request)
- CS platform integration changes (scope separately)
- Historical data backfill beyond initial migration

**Hypercare monitoring checklist (check weekly):**

- [ ] % of accounts with lifecycle stage assigned (target: 100% within 1 week)
- [ ] Manual transitions per CSM per week (are CSMs actually using the screen flow?)
- [ ] Automation error logs (any Flows failing?)
- [ ] Data quality: any accounts stuck in wrong stage for >7 days?

**Output:** Stabilized system, no critical issues outstanding, CSMs comfortable with workflow

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm customer can operate independently.

**Validation checkpoint:**

- [ ] All training sessions delivered (CSM, leadership, technical)
- [ ] Training recordings and documentation provided
- [ ] Hypercare period complete (2 weeks)
- [ ] No critical issues outstanding
- [ ] CSM adoption: >90% of manual transitions happening via screen flow (not direct field edit)
- [ ] 100% of accounts have lifecycle stage assigned
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** -> Customer is enabled, system is stable
- **Extend Hypercare** -> Adoption below targets, need additional support time

---

## Phase 4: Handoff

> **Goal:** Clean project close with maintenance plan established and retention/expansion path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the system, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule -> 4b Internal Handoff -> 4c External Handoff -> 4d Project Close
                          (SME -> Architect)     (LeanScale -> Customer)  (Archive + Debrief)
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At                                                                         |
| ----------------------------- | -------------------- | ------------------------------------------------------------------------------------- |
| **Single Project**            | Customer owns        | 4c (External Handoff) — customer receives maintenance schedule and runs it themselves |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) — Architect receives maintenance schedule and runs it for customer |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention after the project is complete.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task                   | What to Check                                             | Red Flag Threshold                                      |
| ------------------------------ | --------------------------------------------------------- | ------------------------------------------------------- |
| Stage Distribution Audit       | Customer count per lifecycle stage                        | >20% of accounts in a single non-terminal stage         |
| Data Quality Spot-Check        | 10-15 random accounts: is stage accurate?                 | >10% with incorrect stage assignment                    |
| Manual Transition Compliance   | Are CSMs using screen flows or editing fields directly?   | >15% of transitions happening via direct field edit     |
| Automation Health Check        | Review Flow/Workflow error logs                           | Any failed automations in past 30 days                  |

**Quarterly Tasks:**

| Quarterly Task                    | What to Review                                          | Action if Off-Track                                     |
| --------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- |
| Stage Criteria Validation         | Are entry/exit criteria still accurate?                  | Update criteria, retrain CSMs on changes                |
| Velocity Metrics Review           | Average time-in-stage by lifecycle phase                 | Investigate bottleneck stages, adjust thresholds        |
| CS Platform Sync Audit            | Are CRM and CS platform stages still aligned?            | Re-sync, resolve conflicts, update mapping              |
| New Edge Case Review              | Any new scenarios not covered by current design?         | Document in FAQ, add validation rules if needed         |

**After First Business Cycle (60-90 days post-launch):**

- Validate that lifecycle funnel data is being used in weekly CS leadership reviews
- Confirm Time to Value metrics are available for QBR preparation
- Check if "where is this customer?" questions have decreased (the original pain point)
- Assess whether any stages need splitting or merging based on real usage data

**Refinement Triggers (when to re-engage):**

| Trigger                                        | Threshold                                        | Response                                                      |
| ---------------------------------------------- | ------------------------------------------------ | ------------------------------------------------------------- |
| Churn rate increases                           | >2 percentage points above baseline              | Re-engage SME to audit At-Risk stage criteria                 |
| CSM adoption drops                             | &lt;70% manual transitions via screen flow          | Schedule refresher training, review UX of screen flow         |
| New product line launched                      | Any new product requiring separate lifecycle      | Scope new lifecycle design project                            |
| CS platform change                             | Switching from Gainsight to ChurnZero (or similar) | Scope re-integration project                                |

**Every 6-12 Months:**

- Full lifecycle audit: Are all 4-6 stages still serving the business? Any stages that should be added, merged, or retired?
- Benchmark velocity metrics against industry standards (see Methodology for benchmarks)
- Review whether lifecycle data is influencing retention strategy and churn reduction efforts

---

### 4b. Internal Handoff (SME -> Architect)

> **Purpose:** Transfer context so Architect can manage ongoing relationship.

**What the Architect needs to know:**

- What was built: Lifecycle stage structure, automation logic, manual flows, dashboard/reports
- Customer context: Who the key stakeholders are (VP CS, CS Manager, RevOps Lead), their communication preferences, any political dynamics around stage definitions
- Common issues: CSM not updating stages (nudge via email), automation errors (check Flow logs), stage disputes (refer to Definition Alignment Document)
- When to escalate back to SME: Any changes to stage definitions, new stage requests, CS platform integration changes, automation modifications
- **Maintenance schedule** (if Dedicated engagement — Architect runs this)

**Escalation guidelines:**

| Issue Type                                          | Who Handles                          | Example                                              |
| --------------------------------------------------- | ------------------------------------ | ---------------------------------------------------- |
| CSM questions, dashboard filter changes, minor tweaks | Architect                          | "How do I add a filter to the funnel report?"        |
| Stage definition changes, automation modifications    | SME                                | "We need to add a 'Renewal Pending' stage"           |
| CS platform re-integration, lifecycle restructure     | SME (scope as new project)         | "We're switching from ChurnZero to Gainsight"        |

**For Dedicated engagements:** Architect receives the maintenance schedule (4a) and becomes responsible for executing monthly/quarterly checks. SME walks Architect through each task during handoff.

---

### 4c. External Handoff (LeanScale -> Customer)

> **Purpose:** Formal project completion with customer.

**Final project meeting (45-60 min):**

| Time  | Topic                                        | What Happens                                              |
|-------|----------------------------------------------|-----------------------------------------------------------|
| 0-10  | Review what was delivered                    | Walk through lifecycle stages, automations, reports       |
| 10-25 | Documentation package walkthrough            | Show where everything lives, how to find reference docs   |
| 25-40 | Maintenance schedule review                  | Walk through monthly/quarterly tasks                      |
| 40-50 | Final questions                              | Address anything outstanding                              |
| 50-60 | Formal close + next steps                    | "Project complete" + retention/expansion conversation     |

**Documentation package:**

- Lifecycle stage definitions (final version)
- Entry/exit criteria reference document
- CRM field reference (API names, picklist values, date fields)
- Automation logic reference (what triggers what)
- Transition flowchart (Mermaid or diagram)
- Training video recordings (CSM, leadership, technical)
- FAQ document
- Dashboard/report access and interpretation guide
- Maintenance Schedule with monthly/quarterly task list
- Definition Alignment Document (final signed version)

**For Single Project engagements:** Walk the customer through the maintenance schedule in detail. Record a walkthrough video. The customer owns maintenance from this point forward.

**Output:** Customer owns the system. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location
- [ ] Handoff documentation complete
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized
- [ ] Maintenance walkthrough recorded (if Single Project)

#### Internal Debrief (Optional but Recommended)

- What went well? (e.g., "Stage definitions aligned faster than expected because we came with a strong v0")
- What would we do differently? (e.g., "Should have scoped CS platform integration upfront, not discovered mid-project")
- Any learnings to feed back into SOPs? (e.g., "Common edge case: multi-product companies need per-product lifecycle")

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell -> Downsell -> Retry  |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (retainer for ongoing lifecycle optimization)
   | if no
2. Downsell: Another one-time project (Customer Health Score, Renewal Management, or Customer Segmentation)
   | if yes
3. Retry retainer at end of next project cycle
```

**Natural expansion projects from Customer Lifecycle:**
- Customer Health Score: Build scoring model that feeds into the At-Risk stage criteria
- Renewal Management: Automate renewal tracking based on lifecycle stages
- Customer Segmentation: Segment customers for differentiated lifecycle experiences
- Executive Reporting Suite: Build board-ready dashboards from lifecycle velocity data

**Script:**

> "Now that the customer lifecycle is live, there are two ways we can continue. Option 1: We put you on managed services where we handle the monthly/quarterly maintenance, optimization, and any stage adjustments as your business evolves. Option 2: A natural next step is building a Customer Health Score that feeds directly into your At-Risk stage — that's often the highest-impact follow-on. Which sounds more relevant?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On [date ~90 days out], we'll review how the lifecycle is performing — are the stages still right, is the velocity data useful, does anything need adjusting?"

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                                    |
| ------------------- | --------------------------------------------------------------- |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks                |
| 2. Review metrics   | Pull lifecycle funnel data, velocity metrics, adoption rates    |
| 3. Decide ownership | Can Architect handle this check-in, or need SME?               |
| 4. Prep materials   | If SME needed, brief them. If Architect, prep talking points.  |

**At the refinement check-in:**

- Review funnel distribution against expectations
- Check velocity metrics (is Time to Value improving?)
- Identify any stages that need criteria adjustments
- If minor: Architect handles tweaks
- If major: Scope new project (lifecycle restructure or expansion)

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- Definition Alignment Document (signed off)
- Lifecycle stage design with entry/exit criteria
- Transition flowchart (automated + manual paths)
- Date stamp field inventory and naming conventions

**Technical Deliverables:**

- CRM fields: Lifecycle Stage picklist + date stamp fields per stage + formula fields
- Automated transitions: Salesforce Flows / HubSpot Workflows for each automated stage change
- Manual transition screen flow for CSMs
- Validation rules enforcing stage progression and data integrity
- CS platform sync configuration (if applicable)
- Lifecycle funnel dashboard
- Velocity metrics report (time-in-stage, Time to Value)
- Data migration: all existing customers assigned to correct stage

**Documentation Package:**

- Training video recordings (3 sessions)
- Written guides: stage definitions, automation logic, field reference
- FAQ document (edge cases and common questions)
- Definition Alignment Document (final version)
- Maintenance Schedule (monthly + quarterly tasks)

---

## Appendix

### What This Document Is

This is the implementation playbook for Customer Lifecycle projects — the step-by-step execution guide an Architect follows to deliver a customer lifecycle stage structure from first contact to project close. It is the third file in a 3-file playbook structure: advisory (positioning and outcomes), methodology (concepts and frameworks), and implementation (execution steps and checklists).

### What Each Phase Produces

| Phase                    | Output                                                                 | Gate Criteria                                                                  |
| ------------------------ | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **Phase 1: Strategy**    | Signed-off lifecycle design (Definition Alignment Doc + stage package) | VP CS and RevOps have approved stage definitions and entry/exit criteria        |
| **Phase 2: Engineering** | Built and tested lifecycle system in CRM                               | All fields, automations, and reports match tech spec; customer has approved     |
| **Phase 3: Enablement**  | Trained CS team with documentation                                     | All training delivered, hypercare complete, CSMs using screen flows correctly   |
| **Phase 4: Handoff**     | Independent customer + archived project                                | Internal/external handoffs complete, maintenance plan in place, project closed  |

### How to Adapt Per Project Type

| Project Profile | Strategy Weight | Engineering Weight | Enablement Weight | Notes                               |
| --------------- | --------------- | ------------------ | ----------------- | ----------------------------------- |
| **Balanced**    | 30-40%          | 40-50%             | 15-20%            | Heavy strategy + heavy engineering  |

This project sits in the "Balanced" category. Strategy is heavy because lifecycle stage definitions require cross-functional alignment (CS, RevOps, leadership). Engineering is heavy because the CRM build involves fields, automations, manual flows, validation rules, and potentially CS platform integration. Enablement is medium because CSMs need to learn the manual transition process and leadership needs to learn dashboard interpretation.

**Adaptation rules:**
- If no CS platform integration: Phase 2c shortens by 3-5 hours
- If customer has existing lifecycle stages that just need automation: Phase 1 compresses to 1-2 meetings
- If large CS team (>15 CSMs): Phase 3 expands with multiple training sessions and extended hypercare
- Phase 4 always applies — every lifecycle project needs handoff and maintenance schedule

### Key Industry Context

Customer lifecycle visibility is a top priority for CS organizations. A 5% increase in customer retention can boost profitability by 25-95% [1]. The average B2B SaaS churn rate is 3.5% monthly for SMBs and under 1% for enterprise [2]. Users who complete onboarding are 80% more likely to become long-term customers [3], which is why the "Onboarding" to "Adopting" transition is typically the most critical stage gate to instrument.

95% of customer success managers report that customer adoption is their primary focus [4], yet most B2B SaaS companies lack the lifecycle stage tracking to measure adoption systematically. This project closes that gap.

See Methodology for detailed lifecycle stage design frameworks and benchmarking data. See Advisory for scoping factors and discovery questions.

---

## References

[1] [Bain & Company - Prescription for Cutting Costs](https://www.bain.com/insights/retaining-customers)
[2] [Vitally - B2B SaaS Churn Rate Benchmarks 2025](https://www.vitally.io/post/saas-churn-benchmarks)
[3] [Databox - Customer Onboarding Metrics](https://databox.com/customer-onboarding-metrics)
[4] [Zapnito - B2B Customer Engagement Trends 2025](https://knowledge.zapnito.com/posts/5-b2b-customer-engagement-trends-for-2025-statistics-afb2f2ac-0199-47ce-b27c-9b92540f9bc0)
[5] [Maxio - 2025 B2B SaaS Benchmarks Report](https://www.maxio.com/resources/2025-saas-benchmarks-report)
[6] [HubSpot - Use Lifecycle Stages](https://knowledge.hubspot.com/records/use-lifecycle-stages)
[7] [SaaScend - Lifecycle Stage Tracking Optimization](https://www.saascend.com/the-three-phases-to-lifecycle-stage-tracking-optimization/)
