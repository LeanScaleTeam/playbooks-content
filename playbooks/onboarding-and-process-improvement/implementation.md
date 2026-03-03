# Onboarding and Process Improvement — Implementation

## Project One-Pager

### Onboarding and Process Improvement One-Pager

#### Project Type

- Category: Balanced
- Primary Deliverable: A working customer onboarding system in the CS platform with automated playbooks, milestone tracking, segment-specific workflows, and measurable time-to-value outcomes

##### Phase Relevance

| Phase          | Applies? | Weight | Notes                                                                 |
| -------------- | -------- | ------ | --------------------------------------------------------------------- |
| 1. Strategy    | Yes      | Heavy  | 3-4 refinement loops: current state audit, milestone definition, segmentation, journey mapping |
| 2. Engineering | Yes      | Heavy  | CS platform playbook configuration, automations, dashboards, CRM handoff fields |
| 3. Enablement  | Yes      | Med    | CSM training, pilot cohort, internal resource creation                |
| 4. Handoff     | Yes      | Med    | Internal + External: maintenance schedule, iteration cadence          |

· · ·

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │    Heavy     │     │    Heavy     │     │     Med      │     │     Med      │
  │ 1a→1b→1c→1d │     │ 2a→2b→2c→2d │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   3-4 refinement       CS platform          CSM training +       Maintenance +
   loops + journey      playbooks + CRM      pilot cohort         iteration cadence
```

**This project's flow:**
- Full 4-phase. Heavy strategy (current state audit + milestone definition + segmentation + journey design), heavy engineering (CS platform playbook build + automations + dashboards), standard enablement with pilot cohort.
- Some customers with existing onboarding documentation may compress Phase 1 by 1-2 meetings. Customers without a CS platform in place cannot start this project (dependency).

· · ·

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Watch onboarding project intro video (explains what structured onboarding means, why milestone-based &gt; checklist-based)
- [ ] Complete onboarding intake form (current process, tools, team size, customer segments, known pain points)
- [ ] Review Definition Alignment Document (milestone definitions, onboarding stage names, handoff criteria)
- [ ] Gather churned customer feedback or exit survey data (last 6-12 months)
- [ ] Provide CS platform admin access and CRM access

##### Track B: Architect Prep
- [ ] Pull CRM data: closed-won deals last 12 months, time from closed-won to first activity, churn data
- [ ] Audit existing onboarding artifacts (emails, playbooks, task lists in CS platform)
- [ ] Map current Sales-to-CS handoff process from CRM fields and opportunity data
- [ ] Build v0 onboarding journey map with ASSUMED milestones based on industry benchmarks
- [ ] Prepare current state assessment with gap analysis draft

· · ·

#### Refinement Loop (1b -> 1c -> 1d)

| Meeting          | Sub-Phase | Focus                                                       | Stakeholder                    | Output                          |
| ---------------- | --------- | ----------------------------------------------------------- | ------------------------------ | ------------------------------- |
| Kickoff          | 1b        | Present v0 journey map, validate current state, align on milestones | VP CS, CS Ops, RevOps         | Info for v1 journey + milestones |
| Refinement 1     | 1c        | Review v1 segmentation, validate Sales-to-CS handoff design | VP CS, VP Sales, RevOps        | v2 with confirmed tiers + handoff |
| Refinement 2     | 1c        | Review v2 full workflow, confirm playbook logic + automations | CS Ops, CSM leads             | v3 ready for platform build     |
| Sign-Off         | 1d        | Strategic approval of onboarding framework + milestone definitions | VP CS, VP Sales, all stakeholders | Final strategic package         |

· · ·

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held
- [ ] 1c. Refinement loop complete (v0 -> vFinal)
- [ ] 1d. Strategic sign-off obtained

##### Phase 2: Engineering
- [ ] 2a. Tech spec created
- [ ] 2b. Engineering handoff meeting held
- [ ] 2c. Build complete (playbooks, automations, dashboards, handoff fields)
- [ ] 2d. QA/Test + customer sign-off

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped
- [ ] 3b. Training sessions delivered (CSMs + leadership)
- [ ] 3c. Pilot cohort complete (5-10 customers)
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff complete
- [ ] 4c. External handoff complete
- [ ] 4d. Project closed and archived

· · ·

#### Document Types

##### Working Documents (iterate together)

| Document                       | Purpose                                           | When Complete                              |
| ------------------------------ | ------------------------------------------------- | ------------------------------------------ |
| Onboarding intake form         | Capture current state, team structure, segments    | All fields filled, validated at kickoff     |
| Current state journey map      | Document existing onboarding workflow              | Gaps identified, baseline metrics captured  |
| Milestone definition table     | Define progressive milestones per segment          | Validated by CS + Sales leadership          |
| Segmentation matrix            | Map customers to onboarding tiers                  | Tier assignments agreed, touch levels set   |
| Sales-to-CS handoff checklist  | Standardize deal context transfer                  | Required fields defined, CRM mapping done   |

##### Deliverables (polished outputs)

| Deliverable                        | Created From                    | Customer Uses For                        |
| ---------------------------------- | ------------------------------- | ---------------------------------------- |
| Onboarding journey map (Mermaid)   | Current state + future state    | Internal alignment, board presentations  |
| Milestone tracking framework       | Milestone definition table      | CS platform configuration, reporting     |
| Segmentation + tier playbook guide | Segmentation matrix             | CSM reference for customer assignments   |
| Handoff process documentation      | Handoff checklist               | Sales + CS daily execution               |

· · ·

#### Enablement Details

##### Training Types

| Type       | Audience                         | Focus                                              | Duration |
| ---------- | -------------------------------- | -------------------------------------------------- | -------- |
| Leadership | VP CS, CS Ops, Head of RevOps    | Interpret onboarding dashboards, act on metrics     | 30 min   |
| Technical  | CSMs, CS Ops admins              | Execute playbooks, manage stalled onboarding, maintain platform | 60 min   |
| Sales      | VP Sales, AEs                    | Sales-to-CS handoff process, required CRM fields    | 30 min   |

##### Hypercare
- Applies: Yes
- Duration: 4 weeks (covers first pilot cohort cycle)
- Office Hours: Yes — weekly 30-min slot for CSMs during pilot

##### Training Assets to Create
- [ ] Video walkthrough: Onboarding playbook walkthrough in CS platform
- [ ] Video walkthrough: Dashboard navigation and metric interpretation
- [ ] Doc: CSM quick-reference guide for onboarding execution
- [ ] Doc: Sales-to-CS handoff process and CRM field guide
- [ ] Doc: Troubleshooting guide for stalled onboarding scenarios

· · ·

#### Handoff & Retention

##### Internal Handoff
- Key context: Onboarding tier structure, milestone definitions, which playbooks are segment-specific, dashboard locations, common CSM questions during pilot
- Escalation trigger: Any structural changes to onboarding stages, new segment additions, CS platform workflow logic changes

##### External Handoff
- Final meeting agenda: Review onboarding system, walk through dashboards, confirm ownership, answer questions, deliver documentation package
- Documentation package: Journey map, milestone framework, playbook guide, training video recordings, FAQ, maintenance schedule

##### Maintenance Schedule
- Monthly: Review onboarding completion rates, check milestone SLA adherence, update playbook tasks if needed
- Quarterly: Full onboarding process retrospective, iterate on segmentation tiers, review churn data for onboarding cohorts
- Who owns: Single Project = customer CS Ops owns | Dedicated = Architect owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services -> if no -> Downsell: Customer Health Model or Renewal Management project -> Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~quarter out from handoff
- Internal prep trigger: 2 weeks before
- Decision: Architect handles / SME needed

· · ·

#### Definition Alignment Terms

| Term                    | Typical Definition                                                                                     |
| ----------------------- | ------------------------------------------------------------------------------------------------------ |
| Time-to-Value (TTV)     | Days from closed-won to first value milestone achieved by the customer                                 |
| Aha! Moment             | The point at which a customer first experiences the core value of the product                           |
| Onboarding Milestone    | A measurable event indicating progress through the onboarding journey (e.g., first login, setup complete, first value achieved) |
| High-Touch Onboarding   | CSM-led onboarding with scheduled calls, live walkthroughs, and dedicated support                      |
| Tech-Touch Onboarding   | Automated onboarding with email sequences, in-app guidance, and milestone triggers without dedicated CSM calls |
| Self-Service Onboarding | Fully automated onboarding with documentation, videos, and in-app prompts only                         |
| Handoff Checklist       | CRM-based checklist of required fields and context that must transfer from Sales to CS at closed-won    |
| Playbook (CS Platform)  | Automated task sequence in the CS platform triggered by an event (e.g., closed-won) with owners, due dates, and dependencies |

· · ·

#### Common Gotchas
- One-size-fits-all playbook applied to all customers regardless of ARR or complexity -> Build segment-specific variations from Day 1. See Methodology for tiering frameworks.
- Sales-to-CS handoff has no mandatory fields, so deals arrive with missing context -> Configure CRM validation rules that block CS assignment until handoff checklist is complete.
- Milestones track activity completion (e.g., "training attended") instead of value outcomes (e.g., "first feature adopted") -> Define outcome-based milestones in Strategy phase. See Methodology for milestone design principles.
- CSMs treat playbook tasks as checkbox compliance instead of customer value drivers -> Train on the "why" behind each milestone during Enablement. Reinforce with dashboard metrics tied to outcomes.
- No escalation path for stalled onboarding -> Configure automated alerts in CS platform when SLA thresholds are breached. Define escalation owners per segment.
- Pilot skipped, full rollout goes live with untested workflows -> Always run a 5-10 customer pilot cohort before full launch. Fix issues before scale.

· · ·

#### Methodology Options

| Option             | When to Use                                          | Complexity |
| ------------------ | ---------------------------------------------------- | ---------- |
| High-Touch Only    | &lt;50 customers/year, all enterprise, complex product   | Low        |
| Tiered (2-tier)    | 50-200 customers/year, clear enterprise vs. mid-market split | Medium     |
| Tiered (3-tier)    | 200+ customers/year, enterprise + mid-market + SMB    | High       |
| Hybrid PLG + Touch | Product-led onboarding with CSM overlay for key accounts | High       |

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on the onboarding framework — milestones, segmentation, journey design, and Sales-to-CS handoff process.
>
> **Output:** Definition Alignment Document + Onboarding Strategic Package (journey map, milestone framework, segmentation matrix, handoff checklist) signed off by VP CS, VP Sales, and CS Ops.

### 1a. Pre-Kickoff

> Two parallel tracks run before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                                 | Format             |
| ----------------------------- | ----------------------------------------------------------------------- | ------------------ |
| Intro video                   | Explain what structured onboarding is, why milestone-based beats checklist-based, what "time-to-value" means | Video (5-10 min)   |
| Definition Alignment Document | Get stakeholder sign-off on milestone names, stage definitions, handoff criteria | Google Doc         |
| Pre-filled intake form        | Current onboarding process, team size, customer segments, known pain points, CS platform details | Google Form or Doc |
| Churn data request            | Churned customer feedback, exit surveys, or cancellation reasons from last 6-12 months | CSV or report      |

**Why this matters:** 83% of B2B buyers say slow onboarding is a dealbreaker [1]. Customers need to understand that structured onboarding directly impacts retention before they can participate meaningfully in the kickoff.

**Completion tracking:** Do not cancel kickoff if incomplete, but push hard — the churn data and intake form are critical inputs for the v0 journey map.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                                          | Output                                 |
| ---- | ------------------------------------------------------------------------------- | -------------------------------------- |
| 1    | Pull CRM data: closed-won deals (12 months), time from closed-won to first activity, churn by cohort | Raw data: baseline TTV, churn timing   |
| 2    | Audit existing onboarding artifacts in CS platform (playbooks, emails, tasks)   | Current state inventory                |
| 3    | Map current Sales-to-CS handoff from CRM fields and opportunity records         | Handoff gap analysis                   |
| 4    | Analyze CRM data + intake form + churn feedback to build v0 journey map         | v0 onboarding journey map (ASSUMED)    |
| 5    | Prepare current state assessment with baseline metrics and gap analysis          | Kickoff presentation materials         |

**Critical:** Mark everything as ASSUMED. The kickoff call validates. Over 20% of voluntary churn ties directly to poor onboarding [2] — the current state assessment should quantify this for the customer's own data.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building anything.

| Term                    | Our Definition                                                         | Internally Approved? |
| ----------------------- | ---------------------------------------------------------------------- | -------------------- |
| Time-to-Value (TTV)     | Days from closed-won to first value milestone achieved                 | [ ] Yes / [ ] No     |
| Aha! Moment             | The point where customer first experiences core product value           | [ ] Yes / [ ] No     |
| Onboarding Complete     | Customer has achieved \[defined value milestone\] and is transitioned to BAU CS | [ ] Yes / [ ] No     |
| High-Touch Onboarding   | CSM-led with scheduled calls and dedicated support                     | [ ] Yes / [ ] No     |
| Tech-Touch Onboarding   | Automated sequences with milestone triggers, no dedicated CSM calls    | [ ] Yes / [ ] No     |
| Handoff Complete        | All mandatory CRM fields populated, CS assignment triggered            | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your CS and Sales leadership. Check "Yes" when approved. We cannot proceed with CS platform configuration until all terms are aligned.

---

### 1b. Kickoff Call

> **Purpose:** Present v0 journey map and current state assessment. Customer reacts and corrects — does not create from scratch.

#### Agenda (75-90 min)

| Time  | Topic                               | What Happens                                                    |
| ----- | ----------------------------------- | --------------------------------------------------------------- |
| 0-15  | Walk through current state assessment | "Here's what your onboarding looks like today based on our audit" |
| 15-30 | Present v0 journey map              | Show proposed milestones, stages, and timeline per segment       |
| 30-45 | Validate milestones                 | ASSUMED -> CONFIRMED or corrected for each milestone             |
| 45-55 | Review Sales-to-CS handoff gaps     | Walk through handoff gap analysis, discuss mandatory fields      |
| 55-70 | Definition Alignment review         | Review terms, identify where stakeholder disagreement exists     |
| 70-80 | Segmentation discussion             | Validate proposed tiers, discuss touch levels per segment        |
| 80-90 | Next steps                          | Schedule refinement meetings, assign homework                   |

#### What We Bring

- v0 onboarding journey map with ASSUMED milestones
- Current state assessment (baseline TTV, completion rates, churn data)
- Sales-to-CS handoff gap analysis
- Definition Alignment Document (pre-filled with recommendations)
- Questions list (what we need to validate)

#### What We Leave With

- Corrections on v0 milestones and journey map (info needed for v1)
- Confirmed or contested definitions
- Segmentation direction (number of tiers, criteria)
- Clear homework assignments for next meeting

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Iterate on the onboarding framework until sign-off.

#### The Pattern

```
Kickoff Call (gather info)
    |
v1 produced (milestones confirmed, journey updated)
    |
Meeting 2 (present v1, segmentation + handoff focus) -> v2
    |
Meeting 3 (present v2, full workflow + automation logic) -> v3
    |
Meeting 4: Final Review -> Sign-off
```

#### Meeting Types

| Meeting Type          | Focus                                                     | Stakeholder                |
| --------------------- | --------------------------------------------------------- | -------------------------- |
| Milestone Validation  | Confirm milestone definitions, target timeframes per segment | VP CS, CS Ops              |
| Segmentation + Handoff | Validate tier assignments, touch levels, Sales-to-CS handoff design | VP CS, VP Sales, RevOps    |
| Full Workflow Review  | Complete journey with automation triggers, escalation paths, dashboard requirements | CS Ops, CSM leads, RevOps  |
| Final Review          | Full walkthrough, sign-off                                | All stakeholders           |

#### Typical Timeline

| Milestone               | Timing                    |
| ----------------------- | ------------------------- |
| Pre-kickoff prep        | 3-5 days                  |
| Kickoff call            | Day 1 of engagement       |
| Refinement meetings     | 2-3 weeks (2-3 meetings)  |
| Final review + sign-off | Week 3-4                  |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything before proceeding to CS platform build.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by VP CS and VP Sales
- [ ] Onboarding milestones defined per segment with target timeframes
- [ ] Customer segmentation tiers confirmed (high-touch, tech-touch, self-service)
- [ ] Sales-to-CS handoff process designed with mandatory CRM fields
- [ ] Onboarding journey map (future state) approved
- [ ] Automation logic documented (triggers, escalations, notifications)
- [ ] Dashboard requirements agreed
- [ ] All critical inputs CONFIRMED (vs ASSUMED)
- [ ] No blockers for engineering

#### Decision Point

- **Proceed to Engineering** -> Customer wants the full onboarding system built in CS platform
- **Partial Engineering** -> Customer wants playbooks and handoff process only (no automated dashboards)

This project type does not naturally exit after Phase 1. The strategic deliverable (journey map + milestone framework) needs platform implementation to deliver value.

---

## Phase 2: Engineering

> **Goal:** Build and test the onboarding system in the CS platform and CRM based on the approved strategic package.
>
> **Output:** Working onboarding playbooks, automated communications, Sales-to-CS handoff fields, and dashboards — all tested and customer-approved.

This is a **heavy engineering** project. The CS platform configuration, CRM handoff fields, automated email sequences, and dashboards are substantial. Expect 40-50% of total project time in this phase.

### Sub-Phases

```
2a Tech Spec -> 2b Engineering Handoff -> 2c Build -> 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate the strategic onboarding package into CS platform and CRM configuration specifications.

**Input:** Signed-off strategic package (journey map, milestones, segmentation, handoff checklist, automation logic)

**What happens:**

1. Translate journey stages -> CS platform playbook objects
2. Map milestones -> trackable events/fields in CS platform
3. Translate handoff checklist -> CRM field requirements

**Output:** Draft tech spec containing:

- CS platform playbook configuration (stages, tasks, owners, dependencies, triggers)
- Milestone tracking objects linked to customer records
- Segment-specific playbook variations (high-touch vs. tech-touch vs. self-service)
- CRM handoff field list with validation rules
- Automated email sequence specifications (welcome, milestone achievement, stalled alerts)
- Dashboard and report specifications (individual progress, CSM portfolio, leadership aggregate)
- Integration requirements (CRM &lt;-> CS platform sync for closed-won trigger)

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs with CS Ops admin / engineer before building.

**Who attends:** Architect + CS Ops Admin (or RevOps engineer)

**Agenda (45-60 min):**

| Time  | Topic                   | What Happens                                                     |
| ----- | ----------------------- | ---------------------------------------------------------------- |
| 0-15  | Walk through specs      | Architect explains strategic context and spec output             |
| 15-30 | Platform-specific review | Discuss CS platform capabilities vs. spec requirements           |
| 30-45 | CRM field review        | Confirm handoff fields, validation rules, sync configuration     |
| 45-60 | Refine and approve      | Adjust specs for platform constraints, confirm build sequence    |

**What Architect brings:**

- Strategic package (for context)
- Draft tech spec (from 2a)
- Questions list (anything flagged as unclear or platform-specific)

**What engineer/admin leaves with:**

- Approved tech spec
- Clear build sequence (playbooks first -> automations -> handoff fields -> dashboards)
- Known risks/dependencies (e.g., CS platform license tier limitations, CRM permission requirements)

---

### 2c. Build (Configure)

> **Purpose:** Configure the onboarding system in CS platform and CRM.

**Input:** Approved tech spec from 2b

**Build sequence:**

| # | Component                           | Platform     | Estimated Effort |
| - | ----------------------------------- | ------------ | ---------------- |
| 1 | Create onboarding journey program   | CS Platform  | 2-4 hours        |
| 2 | Configure playbook triggers (closed-won) | CS Platform | 1-2 hours       |
| 3 | Build task sequences per segment    | CS Platform  | 4-8 hours        |
| 4 | Set up milestone tracking objects   | CS Platform  | 2-3 hours        |
| 5 | Build welcome email sequence        | CS Platform  | 2-3 hours        |
| 6 | Configure stalled onboarding alerts | CS Platform  | 1-2 hours        |
| 7 | Create Sales-to-CS handoff fields   | CRM          | 2-3 hours        |
| 8 | Configure CRM validation rules      | CRM          | 1-2 hours        |
| 9 | Build individual progress tracker   | CS Platform  | 2-3 hours        |
| 10 | Build CSM portfolio dashboard      | CS Platform  | 2-3 hours        |
| 11 | Build leadership aggregate dashboard | CS Platform | 3-4 hours        |
| 12 | Configure automated reports         | CS Platform  | 1-2 hours        |

**Build tracking:**

- [ ] Component 1: Onboarding journey program
- [ ] Component 2: Playbook triggers
- [ ] Component 3: Task sequences (high-touch)
- [ ] Component 4: Task sequences (tech-touch)
- [ ] Component 5: Task sequences (self-service, if applicable)
- [ ] Component 6: Milestone tracking objects
- [ ] Component 7: Welcome email sequence
- [ ] Component 8: Milestone achievement notifications
- [ ] Component 9: Stalled onboarding alerts
- [ ] Component 10: CRM handoff fields + validation rules
- [ ] Component 11: Individual progress dashboard
- [ ] Component 12: CSM portfolio dashboard
- [ ] Component 13: Leadership aggregate dashboard
- [ ] Component 14: Automated weekly/monthly reports

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify the onboarding system works end-to-end and get customer approval.

**Technical testing checklist:**

- [ ] Closed-won trigger fires correctly and initiates onboarding playbook
- [ ] Correct playbook variant assigned based on customer segment
- [ ] Task sequences execute in correct order with proper dependencies
- [ ] Milestone tracking objects update when milestones are achieved
- [ ] Welcome email sends with correct personalization tokens
- [ ] Stalled onboarding alerts fire when SLA thresholds are breached
- [ ] CRM handoff fields enforce validation (cannot create CS assignment without required data)
- [ ] Individual progress dashboard renders correctly
- [ ] CSM portfolio view shows all customers in onboarding pipeline
- [ ] Leadership dashboard displays aggregate metrics (TTV, completion rates, stage duration)
- [ ] Automated reports generate and deliver on schedule
- [ ] Segment-specific variations behave differently per tier

**Customer testing:**

- Walk CS Ops admin through the full system
- Create a test customer record and trigger the onboarding playbook
- Verify each stage, task, and automation
- Have CSM test daily workflow in their portfolio view
- Capture feedback, fix issues

**Engineering sign-off checkpoint:**

- [ ] Built system matches tech spec
- [ ] All technical tests passing
- [ ] Customer CS Ops admin has tested and approved
- [ ] Ready for enablement (CSM training + pilot)

**Decision point:**

- **Proceed to Enablement** -> System is built, needs CSM training and pilot validation
- **Loop back to Build** -> Issues found, needs fixes

---

## Phase 3: Enablement

> **Goal:** CS team can execute the new onboarding process confidently, validated through a pilot cohort.
>
> **Output:** Trained CS and Sales teams with documentation, pilot cohort completed with lessons learned, stabilized system.

### Sub-Phases

```
3a Training Prep -> 3b Training Sessions -> 3c Pilot + Hypercare -> 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from strategic and technical documentation.

**Input:** Strategic package + tech specs + built system

**Output:** Training package containing:

- **CSM training deck:** Playbook walkthrough, daily workflow, milestone tracking, stalled onboarding handling, escalation procedures
- **Sales training deck:** Handoff process, required CRM fields, what CS needs from them
- **Leadership training deck:** Dashboard navigation, metric interpretation, when to intervene
- **CSM quick-reference guide:** One-page daily reference (where to find things, what to do when)
- **FAQ draft:** Based on common questions from similar onboarding projects
- **Kickoff call script:** Template for CSMs to use with new customers entering onboarding

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to CS team, Sales team, and leadership.

**Training sessions:**

| Session          | Audience                    | Focus                                                                        | Duration | Format     |
| ---------------- | --------------------------- | ---------------------------------------------------------------------------- | -------- | ---------- |
| CSM Training     | All CSMs + CS Ops           | Full playbook walkthrough, live demo in CS platform, role-play kickoff calls, stalled onboarding scenarios | 60 min   | Live + recorded |
| Sales Training   | AEs + Sales leadership      | Sales-to-CS handoff process, required CRM fields, why this matters for them  | 30 min   | Live + recorded |
| Leadership       | VP CS, CS Ops, Head RevOps  | Dashboard walkthrough, metric interpretation, escalation triggers            | 30 min   | Live + recorded |

**Training delivery:**

1. Schedule all three sessions within the same week if possible
2. Deliver CSM training first (they need the most time to absorb)
3. Record all sessions as video walkthroughs for future hires
4. Distribute quick-reference guide to CSMs after training
5. Answer questions, note gaps for FAQ update

---

### 3c. Pilot + Hypercare

> **Purpose:** Test the new onboarding process with a real customer cohort before full rollout.

**Pilot design:**

- Select 5-10 new customers across different segments (at least 1 per tier)
- Assign designated CSMs who attended training
- Monitor closely for the first 2-4 weeks

**What happens during pilot:**

- CSMs execute new onboarding playbooks with pilot customers
- CS Ops monitors dashboards and automation triggers
- Weekly 30-min office hours for CSM questions and feedback
- Track pilot metrics against baseline (TTV, completion rates, satisfaction)
- Document what worked and what needs adjustment

**Pilot success criteria:**

- [ ] All pilot customers entered onboarding playbooks correctly
- [ ] Milestone tracking updated accurately
- [ ] No critical automation failures
- [ ] CSMs report confidence in new process
- [ ] Pilot TTV on track to beat baseline

**Hypercare specifics:**

- Duration: 4 weeks (covers full pilot)
- Weekly office hours: 30-min slot, anyone can join
- Bug triage: Same-day response for blocking issues, 48-hour for non-blocking
- Scope: Process questions, automation bugs, dashboard fixes. Out of scope: new feature requests or structural changes.

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm CS team can operate the onboarding system independently.

**Validation checkpoint:**

- [ ] All training sessions delivered and recorded
- [ ] Training recordings and documentation distributed
- [ ] Pilot cohort complete with lessons learned documented
- [ ] Pilot adjustments made (if any)
- [ ] No critical issues outstanding
- [ ] CS team can operate without daily support
- [ ] Ready for full rollout and handoff

**Decision point:**

- **Proceed to Handoff** -> Pilot validated, team enabled, ready for full rollout
- **Extend Pilot** -> Still unstable, needs another cohort or more training
- **Loop back to Engineering** -> Structural issues found during pilot requiring rebuild

---

## Phase 4: Handoff

> **Goal:** Clean project close with full rollout launched, maintenance plan established, and retention/expansion path set.
>
> **Output:** All new customers on new onboarding system, maintenance schedule documented, internal context transferred, customer owns the system, project archived.

**Structure:**

```
4a Maintenance Schedule -> 4b Internal Handoff -> 4c External Handoff -> 4d Project Close
```

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention after the project is complete.

**Monthly Tasks:**

| Monthly Task                      | What to Check                                     | Red Flag Threshold                              |
| --------------------------------- | ------------------------------------------------- | ----------------------------------------------- |
| Onboarding completion rate        | % of customers completing all milestones on time   | &lt;60% completion within target timeframe       |
| Time-to-Value trend               | Average TTV for new cohort vs. baseline            | TTV increasing &gt;20% from baseline             |
| Stalled onboarding review         | Customers stuck at same stage &gt;2 weeks          | &gt;15% of active onboarding stalled            |
| Playbook task accuracy            | Tasks still relevant, no outdated steps            | CSM feedback on irrelevant tasks                 |

**Quarterly Tasks:**

| Quarterly Task                    | What to Review                                    | Action if Off-Track                              |
| --------------------------------- | ------------------------------------------------- | ------------------------------------------------ |
| Milestone definition review       | Are milestones still reflecting actual value?      | Revise milestones with CS leadership              |
| Segmentation tier review          | Are tiers still accurate given customer mix?       | Adjust tier criteria, update playbook variations  |
| Sales-to-CS handoff audit         | Are handoff fields being completed consistently?   | Reinforce with Sales, tighten CRM validation      |
| Churn cohort analysis             | Are onboarded customers churning less than before? | Deep dive into churn reasons, adjust process      |

**After First Business Cycle (60-90 days post-launch):**

- Compare TTV for new-process customers vs. baseline
- Review 90-day retention rate for first full cohort
- Validate that milestone completion correlates with retention — companies that achieve value within 90 days retain at significantly higher rates [3]
- Document first-cycle learnings

**Refinement Triggers (when to re-engage):**

| Trigger                                 | Threshold                          | Response                                          |
| --------------------------------------- | ---------------------------------- | ------------------------------------------------- |
| TTV increasing                          | &gt;25% above baseline for 2+ months | Re-engage to audit onboarding workflow            |
| Onboarding completion rate dropping     | &lt;50% for any segment            | Scope refinement project for affected segment      |
| New product launch or major feature     | Any significant product change     | Update milestones and playbook tasks               |
| Customer segment mix shift              | New tier needed (e.g., PLG launch) | Scope new onboarding tier design                   |

**Every 6-12 Months:**

- Full onboarding framework review against business objectives
- Reassess customer segmentation tiers
- Audit CS platform playbook performance data
- Consider advanced onboarding capabilities (in-app guidance, product analytics integration)

---

### 4b. Internal Handoff

> **Purpose:** Transfer context so the ongoing relationship can be managed effectively.

**What the Architect needs to know:**

- What was built: Onboarding system with \[X\] segment tiers, \[Y\] playbooks, \[Z\] automated sequences
- Strategic context: Why milestones were defined this way, what the customer's "Aha! Moment" is
- Customer context: Key stakeholders, CS Ops admin capabilities, any quirks from pilot
- Common issues: Stalled onboarding patterns, automation edge cases discovered during pilot
- When to escalate: Any structural changes, new segment creation, milestone redefinition

**Escalation guidelines:**

| Issue Type                                   | Who Handles              |
| -------------------------------------------- | ------------------------ |
| Task wording changes, dashboard filter tweaks | Architect                |
| New segment tier, milestone logic changes     | SME                      |
| Playbook not triggering for certain records   | Architect first, escalate to SME if not a simple config fix |

**For Dedicated engagements:** Architect receives the maintenance schedule (4a) and becomes responsible for executing monthly and quarterly tasks. SME walks Architect through each maintenance task during handoff.

---

### 4c. External Handoff

> **Purpose:** Formal project completion with customer. Launch full rollout.

**Final project meeting:**

- Review what was delivered (playbooks, automations, dashboards, handoff process)
- Walk through documentation package
- Transition all new customers to new onboarding playbooks (full rollout go-live)
- Transfer admin access and documentation to client CS Ops
- Walk through maintenance schedule in detail
- Answer final questions
- Make it explicit: "Project complete"
- **For Single Project engagements:** Record a video walkthrough of the maintenance schedule

**Documentation package:**

- Onboarding journey map (final version)
- Milestone framework document
- Segmentation and tier assignment guide
- Sales-to-CS handoff process documentation
- All training video recordings
- CSM quick-reference guide
- FAQ document
- Definition Alignment Document (final version)
- Troubleshooting guide
- Maintenance Schedule
- Support contact info

**Output:** Customer owns the onboarding system. Full rollout launched. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location
- [ ] Handoff documentation complete
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized
- [ ] Pilot results and lessons learned documented

#### Internal Debrief (Optional but Recommended)

- What went well? (e.g., milestone definition process, pilot feedback loop)
- What would we do differently? (e.g., more time on segmentation, earlier Sales involvement)
- Any learnings to feed back into SOPs?
- Customer satisfaction signal?

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell -> Downsell -> Retry  |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (retainer for ongoing onboarding optimization)
   | if no
2. Downsell: Customer Health Model project (natural next step after onboarding)
   or: Renewal Management project
   | if yes
3. Retry retainer at end of next project cycle
```

**Script:**

> "Now that your onboarding system is live, there are two ways we can continue working together. Option 1: We can set you up on managed services where we handle ongoing optimization — monitoring TTV trends, adjusting playbooks as your product evolves, and tuning segmentation as your customer base grows. Option 2: If there's a specific next project, Customer Health Scoring or Renewal Management are natural follow-ons. Which sounds more interesting?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On \[date ~quarter out\], we'll review how the onboarding system is performing — TTV trends, completion rates, churn impact — and see if any adjustments are needed."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                                    |
| ------------------- | --------------------------------------------------------------- |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks                |
| 2. Review metrics   | Pull onboarding dashboards, assess: Is TTV improving? Completion rates stable? |
| 3. Decide ownership | Can Architect handle this check-in, or need SME?                |
| 4. Prep materials   | If SME needed, brief them. If Architect, prep talking points.   |

**At the refinement check-in:**

- Review TTV and completion rates against baseline and targets
- Identify any segments underperforming
- If minor: Architect adjusts playbook tasks, updates email templates
- If major: Scope new project (new segment tier, milestone redesign, platform migration)

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- Onboarding journey map (current state + future state, Mermaid diagrams)
- Milestone framework document (milestones per segment with target timeframes)
- Customer segmentation matrix (tier assignments with criteria)
- Sales-to-CS handoff process design (required fields, validation rules, workflow)
- Definition Alignment Document (signed off)

**Technical Deliverables:**

- CS platform onboarding playbooks (configured per segment)
- Automated email sequences (welcome, milestone achievement, stalled alerts)
- CRM handoff fields with validation rules
- Onboarding dashboards (individual progress, CSM portfolio, leadership aggregate)
- Automated reporting (weekly/monthly onboarding performance)

**Documentation Package:**

- Training video recordings (CSM, Sales, Leadership)
- CSM quick-reference guide
- Sales-to-CS handoff field guide
- Troubleshooting guide
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
| **Phase 1: Strategy**    | Signed-off onboarding framework (milestones, segments, journey, handoff) | VP CS and VP Sales have approved all definitions and strategic package         |
| **Phase 2: Engineering** | Built and tested onboarding system in CS platform + CRM                | All playbooks, automations, dashboards working; CS Ops admin has approved      |
| **Phase 3: Enablement**  | Trained CS + Sales teams, pilot cohort validated                       | All training delivered, pilot complete, team can operate independently          |
| **Phase 4: Handoff**     | Independent customer + full rollout launched + archived project         | Internal/external handoffs complete, maintenance plan in place, project closed |

### How to Adapt Per Project Type

This is a **balanced** project with heavy strategy and heavy engineering:

| Project Profile | Strategy Weight | Engineering Weight | Enablement Weight |
| --------------- | --------------- | ------------------ | ----------------- |
| **Balanced**    | 35%             | 40%                | 25%               |

**Adaptation notes:**

- If customer already has milestone definitions and segmentation: compress Phase 1 by 1-2 meetings
- If customer does not have a CS platform: this project cannot start (dependency — see Advisory for scoping)
- If customer has &lt;50 customers/year: may only need high-touch tier, simplifying Phase 2 build
- If customer has existing onboarding playbooks in CS platform: Phase 2 becomes "optimize and extend" rather than "build from scratch"

### Single vs. Dedicated Client Split

| Engagement Type               | What It Means                        | Key Difference                              |
| ----------------------------- | ------------------------------------ | ------------------------------------------- |
| **Single Project**            | One-off onboarding system build      | Customer owns maintenance post-handoff (4c) |
| **Dedicated (Multi-Project)** | Ongoing retainer / multiple projects | Architect owns maintenance post-handoff (4b) |

### Phase 2 Platform Notes

- **Gainsight:** Use Journey Orchestrator for automated sequences, Playbooks for task management, MDA for milestone tracking rules
- **ChurnZero:** Use Plays for automated task creation, Segments for tier-based routing, Custom Dashboards for progress tracking
- **Catalyst:** Use Playbooks for task sequences, Alerts for stalled onboarding, Notes for handoff context

### Expansion Opportunity

Onboarding and Process Improvement is a natural entry point to broader CS operations work. After the customer sees TTV improvement and retention impact, the conversation naturally flows to:

1. **Customer Health Model** — extend milestone tracking into ongoing health scoring
2. **Renewal Management** — connect onboarding success signals to renewal risk
3. **Customer Segmentation** — deepen the tiering model across the full customer lifecycle

---

## References

[1] [OnRamp - Customer Onboarding Statistics](https://onramp.us/blog/customer-onboarding-statistics)

[2] [Custify - SaaS Customer Onboarding and Retention Statistics](https://www.custify.com/blog/saas-customer-onboarding-and-retention-statistics/)

[3] [Rivo - B2B Customer Retention Statistics 2026](https://www.rivo.io/blog/b2b-customer-retention-statistics)

[4] [UserGuiding - User Onboarding Statistics 2026](https://userguiding.com/blog/user-onboarding-statistics)

[5] [UserLens - Impact of Onboarding on SaaS Retention](https://userlens.io/blog/impact-of-onboarding-on-saas-retention)

[6] [Userpilot - Time-to-Value Benchmark Report 2024](https://userpilot.com/blog/time-to-value-benchmark-report-2024/)

[7] [Cloud Coach - 51 Statistics: State of SaaS Onboarding and Implementation](https://cloudcoach.com/blog/51-statistics-you-need-to-know-the-state-of-saas-onboarding-and-implementation/)

[8] [Gainsight - Customer Onboarding Best Practices](https://www.gainsight.com/blog/six-essential-customer-onboarding-steps/)

[9] [ChurnZero - Customer Success Playbooks Guide](https://churnzero.com/blog/7-smart-customer-success-playbooks-guide/)
