# NPS and Voice of Customer Launch — Implementation

## Project One-Pager

```markdown
# NPS and Voice of Customer Launch One-Pager

## Project Type

- Category: Balanced
- Primary Deliverable: Fully automated NPS/CSAT survey program with CRM integration, detractor alert workflows, promoter identification, and executive reporting dashboards

### Phase Relevance

| Phase          | Applies? | Weight | Notes                                                  |
| -------------- | -------- | ------ | ------------------------------------------------------ |
| 1. Strategy    | Yes      | Medium | 2-3 alignment meetings on touchpoints, segmentation, and program goals |
| 2. Engineering | Yes      | Heavy  | NPS tool configuration, CRM field creation, workflow automation, dashboard builds |
| 3. Enablement  | Yes      | Medium | CSM training on detractor follow-up, promoter advocacy, dashboard usage |
| 4. Handoff     | Yes      | Medium | Internal + External with maintenance schedule for ongoing program management |

---

## Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │    Medium    │     │    Heavy     │     │    Medium    │     │    Medium    │
  │ 1a→1b→1c→1d │     │ 2a→2b→2c→2d │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   2-3 alignment        NPS tool config       CSM detractor        Internal + External
   touchpoints + goals  CRM + workflows       follow-up training   maintenance schedule
```

**This project's flow:**
- Full 4-phase. Medium strategy (program design and touchpoint mapping), heavy engineering (NPS tool setup, CRM integration, workflow automation, dashboards), medium enablement (CSM training on closed-loop process), standard handoff.
- No phases skipped. Engineering carries the most weight due to multiple system configurations and integrations.

---

## Pre-Kickoff (1a)

### Track A: Customer Homework
- [ ] Watch NPS program overview video explaining NPS methodology, survey touchpoints, and expected outcomes
- [ ] Complete intake form: current CRM setup, existing survey tools, customer lifecycle stages, stakeholder roles, brand assets
- [ ] Get stakeholder sign-off on NPS/CSAT program goals and target response rates

### Track B: Architect Prep
- [ ] Review CRM data model: contact fields, account hierarchy, lifecycle stage fields
- [ ] Audit existing survey tools or feedback processes in use
- [ ] Draft survey touchpoint matrix based on customer lifecycle stages
- [ ] Prepare v0 NPS program design (touchpoints, frequency, audience segmentation)

---

## Refinement Loop (1b -> 1c -> 1d)

| Meeting      | Sub-Phase | Focus                                                        | Stakeholder           | Output                        |
| ------------ | --------- | ------------------------------------------------------------ | --------------------- | ----------------------------- |
| Kickoff      | 1b        | Present v0 program design, validate touchpoints and goals    | VP CS, CS Ops         | Info for v1                   |
| Refinement 1 | 1c        | Review v1 survey cadence, refine segmentation and alerting   | VP CS, CS Ops, IT/Admin | v2                          |
| Refinement 2 | 1c        | Finalize NPS tool selection, confirm CRM field requirements  | VP CS, CS Ops, IT/Admin | v3                          |
| Sign-Off     | 1d        | Strategic approval of full program design                    | All                   | Final strategic package       |
```

---

## Phase Checklists

### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held
- [ ] 1c. Refinement loop complete (v0 -> vFinal)
- [ ] 1d. Strategic sign-off obtained

### Phase 2: Engineering
- [ ] 2a. Tech spec created (NPS tool config, CRM fields, workflow logic, dashboard specs)
- [ ] 2b. Engineering handoff meeting held
- [ ] 2c. Build complete (NPS tool, CRM integration, workflows, dashboards)
- [ ] 2d. QA/Test + customer sign-off

### Phase 3: Enablement
- [ ] 3a. Training materials prepped
- [ ] 3b. Training sessions delivered (CS leadership + CSM operational)
- [ ] 3c. Hypercare period complete (pilot monitoring + stabilization)
- [ ] 3d. Enablement sign-off

### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff (SME -> Architect) complete
- [ ] 4c. External handoff complete
- [ ] 4d. Project closed and archived

---

## Document Types

### Working Documents (iterate together)

| Document                       | Purpose                                                    | When Complete                         |
|-------------------------------|------------------------------------------------------------|---------------------------------------|
| NPS Program Intake Form       | Capture CRM state, existing tools, lifecycle stages         | All fields filled by customer         |
| Survey Touchpoint Matrix      | Map when/who/how surveys deploy at each lifecycle stage     | All touchpoints confirmed by VP CS    |
| NPS Tool Evaluation Scorecard | Compare tool options against requirements                   | Tool selected and budget approved     |
| CRM Field Mapping Document    | Define NPS fields on Contact and Account objects            | All fields mapped and approved        |
| Workflow Logic Document       | Define detractor alert, promoter flag, and automation rules | All workflow rules documented         |

### Deliverables (polished outputs)

| Deliverable                       | Created From                    | Customer Uses For                          |
|-----------------------------------|---------------------------------|--------------------------------------------|
| NPS Program Design Document       | Touchpoint matrix + intake form | Internal alignment on survey strategy      |
| CRM Integration Spec              | Field mapping + workflow logic  | IT/Admin reference for ongoing maintenance |
| NPS Executive Dashboard           | Dashboard build in CRM          | Board reporting, leadership visibility     |
| NPS Operational Dashboard         | Dashboard build in CRM          | CSM daily workflow, detractor management   |

---

## Enablement Details

### Training Types

| Type       | Audience                        | Focus                                                          | Duration |
| ---------- | ------------------------------- | -------------------------------------------------------------- | -------- |
| Leadership | VP CS, CS Director              | Interpret NPS trends, use executive dashboard, board reporting  | 30m      |
| Operational| CSMs, CS Ops                    | Detractor follow-up workflow, promoter advocacy, dashboard use  | 60m      |
| Technical  | CS Ops Admin, RevOps            | Survey automation rules, CRM field maintenance, troubleshooting | 45m      |

### Hypercare
- Applies: Yes
- Duration: 3 weeks (covers pilot launch through first full survey cycle)
- Office Hours: Yes — Weekly 30-min slot for first 3 weeks

### Training Assets to Create
- [ ] Video walkthrough: NPS program overview and dashboard walkthrough
- [ ] Video walkthrough: Detractor follow-up process demonstration
- [ ] Doc: Survey automation rules and exclusion logic reference
- [ ] Doc: CRM field reference (NPS fields on Contact and Account)
- [ ] Doc: Quick-reference guide for CSMs (detractor SLA, promoter advocacy steps)

---

## Handoff & Retention

### Internal Handoff (SME -> Architect)
- Key context for Architect: NPS program goals, survey cadence, detractor SLA requirements, key stakeholders and their roles
- Escalation trigger: Any changes to survey logic, new touchpoint additions, CRM field modifications, or NPS tool configuration changes

### External Handoff
- Final meeting agenda: Program performance review, dashboard walkthrough, documentation package delivery, maintenance schedule review
- Documentation package: All training video walkthroughs, CRM field reference, automation rules doc, troubleshooting guide, maintenance schedule

### Maintenance Schedule
- Monthly: Response rate check, detractor follow-up SLA compliance, dashboard accuracy validation
- Quarterly: NPS trend analysis, survey touchpoint effectiveness review, closed-loop process audit
- Who owns: Single project = customer owns | Dedicated = Architect owns

### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services -> if no -> Downsell: Customer Health Score project or Customer Segmentation project -> Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~1 quarter after launch
- Internal prep trigger: 2 weeks before
- Decision: Architect handles / SME needed

---

## Key Assets

| Asset                          | When Used                     |
| ------------------------------ | ----------------------------- |
| NPS Program Intake Form        | Phase 1a Pre-Kickoff          |
| Survey Touchpoint Matrix       | Phase 1b-1c Strategy          |
| NPS Tool Evaluation Scorecard  | Phase 1c Strategy             |
| CRM Field Mapping Document     | Phase 2a Tech Spec            |
| Detractor Follow-Up Playbook   | Phase 3b Training             |

---

## Definition Alignment Terms

| Term                  | Typical Definition                                                                                   |
| --------------------- | ---------------------------------------------------------------------------------------------------- |
| NPS (Net Promoter Score) | Single-question loyalty metric: "How likely are you to recommend us?" scored 0-10                  |
| Promoter              | Respondent scoring 9-10 on NPS question — actively loyal and likely to refer                         |
| Passive               | Respondent scoring 7-8 on NPS question — satisfied but not enthusiastic                             |
| Detractor             | Respondent scoring 0-6 on NPS question — unhappy and at risk of churning                            |
| CSAT                  | Customer Satisfaction Score — measures satisfaction with a specific interaction (1-5 or 1-10 scale)   |
| Closed-Loop Feedback  | Process of following up with survey respondents to acknowledge feedback and take action               |
| Transactional NPS     | NPS survey triggered by a specific event (post-onboarding, post-support)                            |
| Relational NPS        | NPS survey sent on a regular cadence (quarterly) to measure overall relationship health              |
| Survey Throttling     | Rules preventing over-surveying the same contact (e.g., max one NPS per quarter per contact)         |
| Detractor SLA         | Maximum time allowed for CSM follow-up after receiving a detractor response (typically 48 hours)      |

---

## Common Gotchas
- Low response rates (&lt;15%) make data unreliable -> Keep surveys to 2-3 questions, optimize send timing, use in-app delivery when possible. B2B NPS response rates in the 12-40% range are typical; below 12% signals a distribution problem [1].
- Detractor alerts fire but nobody follows up -> Enforce 48-hour SLA with auto-created CRM tasks, track compliance on operational dashboard. Companies that close the loop with all customers see an 8.5% increase in retention [2].
- NPS scores tracked but never acted on at the program level -> Establish monthly NPS review cadence with CS leadership, quarterly themes analysis for systemic issues.
- Surveying only end-users, missing decision-maker sentiment -> Configure audience segmentation to include multiple roles per account (users, influencers, sponsors).
- Survey fatigue from over-surveying -> Implement throttling rules: max one NPS survey per contact per quarter, apply exclusion lists for recently churned or opted-out contacts.
- NPS tool and CRM data get out of sync -> Build validation checks in QA; schedule monthly sync audits during maintenance.

---

## Methodology Options

| Option                  | When to Use                                                          | Complexity |
| ----------------------- | -------------------------------------------------------------------- | ---------- |
| Relational NPS Only     | Small customer base, early-stage CS team, limited survey tool budget | Low        |
| Transactional + Relational | Mature CS org, multiple lifecycle touchpoints, dedicated CS Ops    | Medium     |
| Full VoC Program        | Large customer base, cross-functional feedback needs (CS + Product + Support) | High |

> See Methodology for detailed decision frameworks on relational vs. transactional NPS and scoring approaches.

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on the NPS program design — touchpoints, tool selection, survey logic, and CRM integration approach.
>
> **Output:** Definition Alignment Document + NPS Program Design Package (signed off by VP CS and CS Ops).

### 1a. Pre-Kickoff

> Two parallel tracks run before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                         | Format             |
| ----------------------------- | --------------------------------------------------------------- | ------------------ |
| NPS Program Overview Video    | Explain NPS methodology, program benefits, and project timeline | Video walkthrough (5-10 min) |
| Definition Alignment Document | Get sign-off on NPS, Promoter, Passive, Detractor, CSAT terms   | Google Doc         |
| NPS Program Intake Form       | Capture CRM state, existing tools, lifecycle stages, brand assets | Google Form        |

**Completion tracking:** CS Ops lead is accountable for intake form completion. Push hard for completion before kickoff; proceed with available info if incomplete but flag gaps.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                          | Output                                   |
| ---- | --------------------------------------------------------------- | ---------------------------------------- |
| 1    | Review intake form and CRM data model                           | Raw data on current state                |
| 2    | Map customer lifecycle stages from CRM                          | Lifecycle stage document                 |
| 3    | Draft survey touchpoint matrix (when, who, what channel)        | v0 touchpoint matrix                     |
| 4    | Research NPS tool options based on tech stack                    | Tool evaluation shortlist                |
| 5    | Create kickoff presentation with v0 program design              | Presentation deck + questions list       |

**Critical:** Mark all touchpoints and tool recommendations as ASSUMED. The kickoff call validates.

#### Stakeholder Alignment Document

| Term                  | Our Definition                                                                        | Internally Approved? |
| --------------------- | ------------------------------------------------------------------------------------- | -------------------- |
| NPS                   | Single-question loyalty metric scored 0-10; calculated as %Promoters - %Detractors    | [ ] Yes / [ ] No     |
| Promoter              | Score 9-10 — actively loyal, likely to refer, candidate for advocacy programs          | [ ] Yes / [ ] No     |
| Passive               | Score 7-8 — satisfied but vulnerable to competitive offers                            | [ ] Yes / [ ] No     |
| Detractor             | Score 0-6 — at risk of churning, requires proactive follow-up within SLA              | [ ] Yes / [ ] No     |
| CSAT                  | Satisfaction score for specific interactions, distinct from relationship NPS            | [ ] Yes / [ ] No     |
| Closed-Loop Feedback  | Mandatory process of following up with all respondents, especially detractors          | [ ] Yes / [ ] No     |
| Detractor SLA         | Maximum follow-up time (e.g., 48 hours) after detractor response is received           | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your CS leadership team. Check "Yes" when approved. We cannot proceed to tool configuration until all terms are aligned.

---

### 1b. Kickoff Call

> **Purpose:** Present v0 program design and get alignment on NPS program strategy. We walk in with a draft touchpoint matrix and tool shortlist — customer reacts and refines.

#### Agenda (60-90 min)

| Time  | Topic                                  | What Happens                                                      |
| ----- | -------------------------------------- | ----------------------------------------------------------------- |
| 0-15  | Walk through v0 program design         | "Here's what we recommend based on your intake and lifecycle"     |
| 15-30 | Validate touchpoint matrix             | Confirm or adjust survey timing, audience, and channels           |
| 30-40 | Definition alignment                   | Review Definition Alignment Document                              |
| 40-50 | NPS tool discussion                    | Present shortlist, discuss integration requirements                |
| 50-60 | Identify gaps                          | What data is missing, who provides brand assets, tool budget status |
| 60+   | Next steps                             | Schedule refinement meetings, assign homework                      |

#### What We Bring

- v0 NPS program design (touchpoint matrix, survey cadence, audience segmentation)
- NPS tool evaluation shortlist (2-3 options with pros/cons)
- Definition Alignment Document (pre-filled with our recommendations)
- Questions list (touchpoint validation, tool preferences, budget constraints)

#### What We Leave With

- Feedback on v0 program design (info to create v1)
- Confirmed or updated touchpoint matrix
- Tool preference direction (or scheduled vendor demos)
- Clear homework: brand assets, tool budget approval, contact list for pilot

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Iterate on the NPS program design until all components are finalized and signed off.

#### The Pattern

```
Kickoff Call (gather info on program goals, touchpoints)
    |
Architect updates program design -> v1
    |
Meeting 2 (tool selection, survey design) -> v2
    |
Meeting 3 (workflow logic, dashboard design) -> v3
    |
Final Review -> Sign-off
```

#### Meeting Types for NPS and Voice of Customer Launch

| Meeting Type          | Focus                                                     | Stakeholder                |
| --------------------- | --------------------------------------------------------- | -------------------------- |
| Program Design        | Goals, touchpoints, segmentation, survey cadence           | VP CS, CS Ops              |
| Tool Selection        | Vendor demos, evaluation scoring, budget approval          | VP CS, CS Ops, IT/Admin    |
| Workflow & Dashboard  | Detractor alert logic, promoter workflows, dashboard specs | CS Ops, RevOps             |
| Final Review          | Full program walkthrough and sign-off                      | All stakeholders           |

#### Typical Timeline

| Milestone               | Timing                                    |
| ----------------------- | ----------------------------------------- |
| Pre-kickoff prep        | 2-3 days                                  |
| Kickoff call            | Day 1 of engagement                       |
| Meeting loop            | 1-2 weeks (3-4 meetings)                  |
| Final review + sign-off | When all program components confirmed     |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything approved before building.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by CS leadership
- [ ] Survey touchpoint matrix confirmed (timing, audience, channel for each touchpoint)
- [ ] NPS tool selected and budget approved
- [ ] CRM field requirements documented and approved
- [ ] Detractor alert and promoter workflow logic agreed
- [ ] Dashboard requirements (executive + operational) documented
- [ ] Pilot segment identified (which CSM book, which customer segment)
- [ ] Brand assets received (logo, colors for survey customization)
- [ ] No blockers for engineering

#### Decision Point

- **Proceed to Engineering** -> Customer wants full NPS program built (standard path)
- **Project complete** -> Not typical for this project type; NPS requires engineering build

---

## Phase 2: Engineering

> **Goal:** Build and test the NPS tool configuration, CRM integration, workflows, and dashboards based on approved program design.
>
> **Output:** Fully configured NPS program — tool connected, surveys designed, workflows firing, dashboards live — tested and customer-approved.

| Project Type    | Engineering Weight | This Project                                                    |
| --------------- | ------------------ | --------------------------------------------------------------- |
| Balanced        | Heavy (50-60%)     | NPS tool setup, CRM field creation, workflow automation, dashboards |

### Sub-Phases

```
2a Tech Spec -> 2b Engineering Handoff -> 2c Build -> 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate the approved NPS program design into technical specifications for CRM and NPS tool configuration.

**Input:** Signed-off NPS Program Design Package from Phase 1

**Output:** Draft tech spec containing:

- **CRM Field Mapping:** NPS fields on Contact (NPS Score, NPS Category, NPS Survey Date, NPS Verbatim) and Account (Latest NPS Score, NPS Trend, NPS Response Count, Last Survey Date)
- **NPS Tool Configuration:** Survey templates, conditional follow-up logic, branding specs, automation trigger rules
- **Workflow Logic:** Detractor alert triggers (score 0-6), promoter flag triggers (score 9-10), notification channels, task creation rules, SLA tracking
- **Dashboard Specs:** Executive dashboard (overall NPS, trend, response rate, distribution) and Operational dashboard (NPS by segment, recent responses, open detractor tasks)
- **Integration Spec:** NPS tool &lt;-> CRM connection method (OAuth/API), field sync direction, data refresh frequency
- **Build Sequence:** Tool setup -> CRM fields -> Survey templates -> Workflows -> Dashboards -> Automation rules

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs with engineer before building.

**Who attends:** Architect + Engineer (or CRM Admin)

**Agenda (30-45 min):**

| Time  | Topic                        | What Happens                                              |
| ----- | ---------------------------- | --------------------------------------------------------- |
| 0-15  | Walk through tech spec       | Architect explains program design context + spec          |
| 15-25 | CRM field and workflow review | Engineer validates field types, workflow feasibility       |
| 25-35 | Integration approach          | Confirm NPS tool &lt;-> CRM connection method and permissions |
| 35-45 | Build sequence and timeline   | Agree on build order, estimate time per component          |

**What Architect brings:**

- NPS Program Design Package (for context)
- Draft tech spec (from 2a)
- Questions list (API limitations, field-level security, workflow firing limits)

**What engineer leaves with:**

- Approved tech spec
- Clear build sequence
- Known risks (API rate limits, field count limits, workflow governor limits)

---

### 2c. Build (Configure)

> **Purpose:** Build and configure the NPS program across NPS tool and CRM.

**Input:** Approved tech spec from 2b

**Build components:**

| # | Component                        | System        | Estimated Effort |
|---|----------------------------------|---------------|------------------|
| 1 | NPS tool account setup           | NPS Tool      | 1-2 hours        |
| 2 | CRM connection (OAuth/API)       | NPS Tool + CRM| 1-2 hours        |
| 3 | CRM field creation (Contact)     | CRM           | 2-3 hours        |
| 4 | CRM field creation (Account)     | CRM           | 2-3 hours        |
| 5 | Survey template design + branding| NPS Tool      | 2-3 hours        |
| 6 | Conditional follow-up logic      | NPS Tool      | 1-2 hours        |
| 7 | Detractor alert workflow         | CRM           | 2-3 hours        |
| 8 | Promoter identification workflow | CRM           | 1-2 hours        |
| 9 | Executive dashboard              | CRM           | 3-4 hours        |
| 10| Operational dashboard            | CRM           | 3-4 hours        |
| 11| Survey automation rules          | NPS Tool      | 2-3 hours        |
| 12| Survey throttling and exclusions | NPS Tool      | 1-2 hours        |

**Build tracking:**

- [ ] Component 1: NPS tool account setup
- [ ] Component 2: CRM connection established and tested
- [ ] Component 3: Contact-level NPS fields created with proper visibility
- [ ] Component 4: Account-level NPS fields created with roll-up logic
- [ ] Component 5: Survey templates branded and tested on desktop + mobile
- [ ] Component 6: Conditional follow-up logic configured (Promoter/Passive/Detractor paths)
- [ ] Component 7: Detractor alert workflow live (notification + task creation)
- [ ] Component 8: Promoter flag workflow live (flag + CSM notification)
- [ ] Component 9: Executive dashboard built and shared with leadership
- [ ] Component 10: Operational dashboard built and shared with CSMs
- [ ] Component 11: Survey automation rules configured per touchpoint
- [ ] Component 12: Throttling rules active (max one NPS per contact per quarter)

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify all NPS program components work end-to-end and get customer approval.

**Technical testing checklist:**

- [ ] NPS tool &lt;-> CRM connection active and syncing
- [ ] Sample survey sent and response received
- [ ] NPS score, category, date, and verbatim populate correctly on Contact record
- [ ] Account-level roll-up calculates correctly from Contact responses
- [ ] Detractor response (score 0-6) triggers alert notification within 2 minutes
- [ ] Detractor response creates follow-up task assigned to correct CSM
- [ ] Promoter response (score 9-10) creates promoter flag on Contact/Account
- [ ] Promoter response triggers CSM notification for advocacy follow-up
- [ ] Passive response (score 7-8) logs correctly without triggering detractor or promoter workflows
- [ ] Survey throttling prevents duplicate surveys to same contact within exclusion window
- [ ] Executive dashboard renders correctly with sample data
- [ ] Operational dashboard shows recent responses, open detractor tasks, NPS by segment
- [ ] Survey displays correctly on desktop and mobile
- [ ] Automation rules fire at correct touchpoints
- [ ] Reminder logic sends follow-up 5 days after initial survey with no response

**Customer testing:**

- Walk customer through each workflow with test data
- Have CS Ops admin verify field visibility and security
- Have CSM test detractor alert and follow-up task creation
- Confirm dashboard data matches expected results
- Capture feedback, fix issues

**Engineering sign-off checkpoint:**

- [ ] All 12 build components verified
- [ ] All technical tests passing
- [ ] Customer has tested detractor and promoter workflows
- [ ] Dashboards approved by VP CS
- [ ] Ready for pilot launch

**Decision point:**

- **Proceed to Enablement** -> System is built, needs training + pilot before full launch
- **Loop back to Build** -> Issues found, needs fixes

---

## Phase 3: Enablement

> **Goal:** CS team can use the NPS program effectively — follow up on detractors within SLA, identify promoters for advocacy, and use dashboards for account planning.
>
> **Output:** Trained CS team with documentation, pilot validated, system stabilized.

### Sub-Phases

```
3a Training Prep -> 3b Training Sessions -> 3c Hypercare -> 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from the NPS program design, tech specs, and built system.

**Input:** NPS Program Design Package + tech specs + configured system

**Output:** Training package containing:

- **Leadership Training Deck:** NPS methodology basics, executive dashboard walkthrough, how to use NPS data in QBRs and board reporting
- **CSM Operational Guide:** Detractor follow-up playbook (48-hour SLA, what to say, how to log outcomes), promoter advocacy steps, dashboard navigation
- **Technical Admin Guide:** Survey automation rules, CRM field reference, troubleshooting common sync issues
- **Quick-Reference Card:** One-page CSM cheat sheet — detractor response flow, promoter response flow, key dashboard views
- **FAQ Draft:** Common questions about NPS scores, response rates, and follow-up expectations

---

### 3b. Training Sessions

> **Purpose:** Transfer NPS program knowledge to all stakeholders.

**Training sessions for NPS and Voice of Customer Launch:**

| Session       | Audience                  | Focus                                                              | Duration | Format    |
| ------------- | ------------------------- | ------------------------------------------------------------------ | -------- | --------- |
| Leadership    | VP CS, CS Director        | NPS trends interpretation, executive dashboard, board reporting use | 30 min   | Live      |
| Operational   | All CSMs                  | Detractor follow-up (with role-play), promoter advocacy, dashboard use | 60 min | Live      |
| Technical     | CS Ops Admin, RevOps      | Automation rules, field maintenance, troubleshooting, report building | 45 min  | Live      |

**Training delivery:**

1. Schedule sessions with 3-5 day gaps between each for absorption
2. Deliver leadership session first (sets tone for program expectations)
3. Deliver CSM operational session (includes live role-play of detractor follow-up conversations)
4. Deliver technical session last (admin skills for ongoing management)
5. Record all sessions as video walkthroughs for future onboarding

**Output:**

- Trained stakeholders across all three levels
- Video walkthrough recordings for all sessions
- Questions log (feeds into FAQ updates)

---

### 3c. Hypercare

> **Purpose:** Support the pilot launch and first full survey cycle to catch issues early and build team confidence.

**Duration:** 3 weeks

**Week 1 — Pilot Launch:**
- Launch surveys to pilot segment (one CSM's book, 50-100 contacts)
- Monitor response rate and score distribution daily
- Verify all workflows firing correctly with real data
- Resolve any sync or automation issues immediately

**Week 2 — Pilot Review + Full Launch:**
- Review pilot results with CS Ops
- Address any configuration adjustments
- Launch full program to all segments
- Monitor first 48 hours of full launch closely

**Week 3 — Stabilization:**
- Weekly 30-min office hours for CSM questions
- Monitor detractor SLA compliance
- Verify dashboard accuracy with accumulating real data
- Bug triage and minor fixes

**When to extend:** If response rates are below 10% after week 2, or if major workflow issues surface during full launch, extend hypercare by 1-2 weeks.

**Output:** Stabilized NPS program, no critical issues, response rates at expected levels

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm the CS team can operate the NPS program independently.

**Validation checkpoint:**

- [ ] All three training sessions delivered and recorded
- [ ] Pilot launch completed successfully
- [ ] Full program launched to all segments
- [ ] Response rate above 15% in first full cycle
- [ ] Detractor follow-up SLA compliance above 80% in first cycle
- [ ] No critical workflow or sync issues outstanding
- [ ] CSMs can navigate dashboards and execute detractor follow-up without support
- [ ] CS Ops admin can troubleshoot basic issues using documentation
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** -> Program is stable, team is enabled
- **Extend Hypercare** -> Response rates too low, workflow issues, or team not confident

---

## Phase 4: Handoff

> **Goal:** Clean project close with maintenance plan for ongoing NPS program management, internal context transferred, customer owns the system.
>
> **Output:** Maintenance schedule documented, internal context transferred to Architect, customer self-sufficient, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule -> 4b Internal Handoff -> 4c External Handoff -> 4d Project Close
```

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention to keep the NPS program healthy and actionable.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task                      | What to Check                                              | Red Flag Threshold                                    |
| --------------------------------- | ---------------------------------------------------------- | ----------------------------------------------------- |
| Response Rate Monitoring          | Overall response rate by touchpoint and segment            | Below 15% for any touchpoint for 2+ consecutive months |
| Detractor SLA Compliance          | % of detractor responses followed up within 48 hours       | Below 85% compliance                                  |
| Dashboard Accuracy Validation     | Verify NPS scores, trends, and distributions are rendering correctly | Any data discrepancy between NPS tool and CRM     |
| Data Sync Audit                   | Confirm NPS tool &lt;-> CRM sync is running without errors | Any sync failures in logs                             |

**Quarterly Tasks:**

| Quarterly Task                    | What to Review                                             | Action if Off-Track                                   |
| --------------------------------- | ---------------------------------------------------------- | ----------------------------------------------------- |
| NPS Trend Analysis                | Score trend over quarter, segment breakdowns               | If NPS drops >5 points, escalate to CS leadership     |
| Closed-Loop Process Audit         | % of responses with documented follow-up and outcomes      | If &lt;70% closed, retrain team on process            |
| Survey Touchpoint Effectiveness   | Response rates and score variance by touchpoint            | Retire low-performing touchpoints, test new ones      |
| Feedback Themes Analysis          | Common verbatim feedback themes across all responses       | Feed product-related themes to Product team           |

**After First Business Cycle (60-90 days post-launch):**

- Full NPS program health check: response rates, score distribution, SLA compliance
- Validate that NPS data is being used in QBRs and renewal planning
- Assess whether current touchpoints capture the right moments
- Key question: Is the closed-loop process driving measurable retention improvement?

**Refinement Triggers (when to re-engage):**

| Trigger                          | Threshold                                  | Response                                              |
| -------------------------------- | ------------------------------------------ | ----------------------------------------------------- |
| Response Rate Decline            | Below 10% for 2+ months                   | Audit survey delivery, timing, and channel; consider in-app option |
| NPS Score Drop                   | >10 point decline over 2 quarters          | Deep-dive analysis, escalate to CS leadership         |
| Detractor SLA Breakdown          | Below 70% compliance for 1+ months         | Retrain CSMs, review alert configuration              |
| New Customer Segment Added       | New segment not covered by existing surveys | Scope touchpoint additions as mini-project            |

**Every 6-12 Months:**

- Full program review: Are touchpoints still aligned with customer journey?
- Survey question refresh: Update follow-up questions based on emerging themes
- Tool health check: NPS platform updates, new features, pricing changes
- Benchmark comparison: Compare NPS scores against industry benchmarks (B2B SaaS average NPS is 38 as of 2025 [3])

---

### 4b. Internal Handoff (SME -> Architect)

> **Purpose:** Transfer context so Architect can manage the ongoing NPS program relationship.

**What the Architect needs to know:**

- NPS program goals and how they tie to customer retention strategy
- Survey cadence and touchpoint matrix (what fires when)
- Key stakeholders: VP CS (executive sponsor), CS Ops lead (day-to-day), CSM team (follow-up owners)
- Detractor SLA requirements and current compliance rate
- Dashboard locations and how to pull key metrics for QBRs
- **Maintenance schedule** (if Dedicated engagement — Architect runs this)

**Escalation guidelines:**

| Issue Type                                        | Who Handles                                   |
| ------------------------------------------------- | --------------------------------------------- |
| Dashboard filter changes, report exports          | Architect                                     |
| Response rate questions, basic troubleshooting     | Architect (using troubleshooting doc)          |
| New survey touchpoint additions                    | SME                                           |
| Workflow logic changes (alert rules, SLA changes)  | SME                                           |
| NPS tool configuration changes                     | SME                                           |
| CRM field modifications or additions               | SME                                           |

**For Dedicated engagements:** Architect receives the maintenance schedule (4a) and becomes responsible for executing monthly and quarterly tasks. SME walks Architect through each task in detail.

---

### 4c. External Handoff

> **Purpose:** Formal project completion with customer.

**Final project meeting agenda:**

1. Review what was delivered (program design, tool configuration, workflows, dashboards, training)
2. Walk through NPS program performance since launch (response rate, initial NPS scores, SLA compliance)
3. Demonstrate dashboards one final time
4. Walk through documentation package
5. Review maintenance schedule in detail
6. Confirm nothing outstanding
7. Make it explicit: "Project complete"
8. **For Single Project engagements:** Walk the customer through the maintenance schedule and record a video walkthrough

**Documentation package:**

- NPS Program Design Document (final version)
- CRM Field Reference (all NPS fields on Contact and Account)
- Survey Automation Rules Document (triggers, exclusions, throttling, reminders)
- Detractor Follow-Up Playbook (SLA, conversation guide, outcome logging)
- Dashboard User Guide (executive and operational views)
- Troubleshooting Guide (common issues and resolutions)
- All training video walkthrough recordings
- Definition Alignment Document (final version)
- Maintenance Schedule
- NPS tool admin credentials transfer

**Output:** Customer owns the NPS program. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location
- [ ] Handoff documentation complete
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized
- [ ] NPS tool admin credentials transferred to customer

#### Internal Debrief (Optional but Recommended)

- What went well? (tool selection process, training effectiveness, response rates)
- What would we do differently? (timing, stakeholder engagement, pilot scope)
- Any learnings to feed back into NPS playbook?

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell -> Downsell -> Retry  |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (retainer for ongoing NPS program management + optimization)
   | if no
2. Downsell: Customer Health Score project (extends NPS with usage, support, engagement data)
   | or
3. Downsell: Customer Segmentation project (better target survey audiences)
   | if yes
4. Retry retainer at end of next project cycle
```

**Script:**

> "Now that the NPS program is live and generating data, there are two ways we can continue. Option 1: We manage the ongoing optimization — adjusting touchpoints, adding new segments, running quarterly reviews. Option 2: We can scope out a related project like Customer Health Scoring, which combines NPS with product usage and support data for a fuller picture. Which sounds more useful?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On [date ~quarter out], we'll review how the NPS program is performing — response rates, score trends, closed-loop compliance — and see if any adjustments are needed."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                                    |
| ------------------- | --------------------------------------------------------------- |
| 1. Get pinged       | System reminder: NPS refinement check-in in 2 weeks            |
| 2. Review metrics   | Pull NPS trends, response rates, SLA compliance                |
| 3. Decide ownership | Can Architect handle this check-in, or need SME?                |
| 4. Prep materials   | If SME needed, brief them. If Architect, prep talking points.   |

**At the refinement check-in:**

- Review NPS score trends against launch baseline
- Check response rate trends by touchpoint
- Assess closed-loop compliance
- If minor adjustments: Architect handles touchpoint timing tweaks
- If major changes: Scope refinement project (new segments, new tool features, workflow redesign)

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- NPS Program Design Document (touchpoint matrix, survey cadence, audience segmentation, program goals)
- Definition Alignment Document (signed off by CS leadership)
- NPS Tool Evaluation Scorecard (with selection rationale)

**Technical Deliverables:**

- Configured NPS tool (survey templates, branding, conditional logic, automation rules)
- CRM fields on Contact and Account objects (NPS Score, Category, Trend, Verbatim, etc.)
- Detractor alert workflow (notification + task creation)
- Promoter identification workflow (flag + CSM notification)
- Executive NPS dashboard
- Operational NPS dashboard
- Survey automation rules with throttling and exclusion logic

**Documentation Package:**

- Training video walkthrough recordings (3 sessions)
- Detractor Follow-Up Playbook
- CRM Field Reference
- Survey Automation Rules Document
- Dashboard User Guide
- Troubleshooting Guide
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

### Phase Outputs & Gate Criteria

| Phase                    | Output                                                                    | Gate Criteria                                                                   |
| ------------------------ | ------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| **Phase 1: Strategy**    | Signed-off NPS program design (touchpoint matrix + tool selection + workflow logic) | VP CS and CS Ops have approved all program components                   |
| **Phase 2: Engineering** | Built and tested NPS system (tool, CRM, workflows, dashboards)            | All components verified, workflows firing, customer has tested and approved      |
| **Phase 3: Enablement**  | Trained CS team, pilot validated, program launched                         | All training delivered, pilot + full launch complete, team operating independently |
| **Phase 4: Handoff**     | Independent customer + archived project                                   | Internal/external handoffs complete, maintenance plan in place, project closed   |

### Phase 1 Guide: Strategy for NPS Programs

NPS programs fail when stakeholders disagree on what the program should achieve. A VP CS who wants board-ready metrics has different needs than a CSM who wants early churn warnings. Phase 1 forces alignment on goals, definitions, and touchpoints before configuring anything.

Companies that run NPS surveys quarterly see a 51% increase in retention rate compared to 44% for annual-only surveys [2]. Getting the cadence right during strategy directly impacts program ROI.

**Key Strategy Decisions:**

1. **Relational vs. Transactional NPS** — Relational surveys measure overall relationship health on a cadence. Transactional surveys trigger after specific events. Most B2B SaaS implementations benefit from both. See Methodology for the decision framework.

2. **Survey Touchpoints** — Post-onboarding (30-60 days), post-support interaction, quarterly relationship check-in, pre-renewal (90 days out). Each needs a defined audience and channel.

3. **Tool Selection** — NPS platform choice depends on CRM integration depth, in-app vs. email capability, alerting features, and budget. Common options: Delighted (SMB, simple automation), Qualtrics (enterprise, advanced analytics), AskNicely (mid-market, strong CRM integration), or native CRM survey tools (budget-friendly, limited features) [4].

4. **Response Rate Targets** — B2B NPS response rates typically range from 12-40% [1]. Setting realistic targets upfront prevents disappointment and guides channel optimization.

### Phase 2 Guide: Engineering for NPS Programs

**Key Principles:**

**CRM Fields:** Create fields on both Contact (individual response) and Account (aggregated view). Account-level roll-ups are critical — a single detractor contact on a $500K account needs more visibility than aggregate NPS scores suggest.

**Workflow Design:** Detractor alerts must be immediate (within 2 minutes of response submission). Build both notification AND task creation (CRM) — notifications get attention, tasks ensure follow-through.

**Dashboard Design:** Executive dashboard shows trends and distribution. Operational dashboard shows action items. Never combine them — executives care about "are we getting better," CSMs care about "who do I call today."

### Phase 3 Guide: Enablement for NPS Programs

NPS programs generate ROI only when teams act on the data. Collecting scores without acting on them is worse than not collecting at all — customers who give feedback and see no response become more negative [2].

**Training Focus by Role:**

- **VP CS / CS Director:** How to read NPS trends in board context, what "good" looks like (B2B SaaS median NPS is 38 [3]), how NPS connects to retention and expansion metrics
- **CSMs:** The closed-loop process is the core competency — how to follow up with detractors (empathy, problem resolution, outcome logging), how to activate promoters (referral asks, case study candidates, testimonials)
- **CS Ops / Admin:** Automation rule maintenance, new touchpoint configuration, field and workflow troubleshooting, report building

**Pilot Strategy:** Always run a pilot before full launch. Select one CSM's book of business (50-100 contacts). Monitor for one full survey cycle (7-10 days including reminder sends). This catches survey delivery issues, CRM sync failures, workflow misfires, and unexpected response patterns.

### Phase 4 Guide: Handoff for NPS Programs

NPS programs degrade silently. Response rates drop as survey fatigue sets in. Detractor follow-up SLAs slip when there is no tracking. Dashboards become stale when nobody checks data accuracy. The maintenance schedule makes monitoring explicit and cadenced.

**Common Post-Launch Failure Modes:**

| Failure Mode                     | Symptom                                     | Prevention (Maintenance Task)              |
| -------------------------------- | ------------------------------------------- | ------------------------------------------ |
| Survey fatigue                   | Response rate drops below 10%               | Monthly response rate monitoring           |
| Detractor neglect                | SLA compliance drops below 70%              | Monthly SLA compliance check               |
| Dashboard abandonment            | Nobody logs into dashboards                 | Quarterly dashboard usage audit            |
| Feedback themes ignored          | Same complaints repeat quarter over quarter | Quarterly themes analysis + Product routing|
| Contact list staleness           | Surveys going to churned or wrong contacts  | Monthly data sync audit                    |

**Retention Path for NPS Projects:**

NPS is a natural gateway to deeper Customer Success infrastructure:
- **Customer Health Score** — Combine NPS with product usage, support ticket, and engagement data for a composite health model
- **Customer Segmentation** — Use NPS data alongside firmographic and behavioral data to segment the customer base
- **Renewal Management** — Feed NPS scores into renewal risk scoring and playbook triggers

---

## References

[1] [Survicate - NPS Benchmarks 2025](https://survicate.com/nps-benchmarks/)
[2] [CustomerGauge - NPS Impact on Revenue](https://customergauge.com/blog/nps-impact-on-revenue)
[3] [CustomerGauge - B2B NPS Benchmarks 2025](https://customergauge.com/blog/b2b-nps-benchmarks-tying-revenue-to-your-experience-program)
[4] [Zonka Feedback - 14 Best NPS Tools & Software Platforms 2026](https://www.zonkafeedback.com/blog/best-nps-tools)
[5] [SurveySensum - NPS in B2B Implementation and Best Practices Guide](https://www.surveysensum.com/customer-experience/net-promoter-score-b2b)
[6] [ClearlyRated - B2B NPS Benchmarks 2024 Industry Study Report](https://www.clearlyrated.com/industry-benchmark/nps-benchmarks-for-the-b2b-services-industry)
