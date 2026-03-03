# Sales Lifecycle — Implementation

## Project One-Pager

### Sales Lifecycle One-Pager

#### Project Type

- Category: Balanced (Strategic + Technical)
- Primary Deliverable: Fully documented opportunity lifecycle with stage definitions, entry/exit criteria, timestamp fields, automations, and pipeline velocity dashboards in the customer's CRM (Salesforce or HubSpot)

##### Phase Relevance

| Phase          | Applies? |
| -------------- | -------- |
| 1. Strategy    | Yes      |
| 2. Engineering | Yes      |
| 3. Enablement  | Yes      |
| 4. Handoff     | Yes      |

· · ·

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │     Med      │     │    Heavy     │     │     Med      │     │     Med      │
  │ 1a→1b→1c→1d │     │ 2a→2b→2c→2d │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   2-3 meetings         CRM config +         Pilot group +        Internal +
   audit + design       dashboards           full training        External handoff
```

**This project's flow:**
- Full 4-phase. Medium strategy (stakeholder interviews + data audit + stage design), heavy engineering (CRM picklist, timestamp fields, automation rules, validation, dashboards), medium enablement (pilot + full training), standard handoff.
- No phases skipped. Engineering is the heaviest phase because the CRM configuration and automation build is substantial.

· · ·

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Watch intro video explaining what a sales lifecycle project is and why stage definitions matter
- [ ] Complete intake form confirming current CRM platform, existing stage values, and known pain points
- [ ] Provide CRM admin access for current-state audit
- [ ] Identify who has decision authority on final stage definitions

##### Track B: Architect Prep (Agent-Assisted)
- [ ] Pull CRM opportunity report: all stages, time in stage, conversion rates (last 6 months)
- [ ] Identify high-stagnation stages (30+ days without movement)
- [ ] Audit existing timestamp/stage date fields and population rates
- [ ] Draft current-state assessment with data quality baseline
- [ ] Prepare v0 recommended stage structure based on industry patterns

· · ·

#### Refinement Loop (1b → 1c → 1d)

| Meeting      | Sub-Phase | Focus                                                | Stakeholder                      | Output                             |
| ------------ | --------- | ---------------------------------------------------- | -------------------------------- | ---------------------------------- |
| Kickoff      | 1b        | Present current-state audit, validate pain points    | VP Sales, Sales Managers, RevOps | Confirmed gaps, info for v1 design |
| Refinement 1 | 1c        | Review v1 stage definitions and entry/exit criteria  | VP Sales, Sales Managers         | Approved stages + probabilities    |
| Sign-Off     | 1d        | Final stage design + automation spec approval        | VP Sales, RevOps Lead            | Signed-off strategic package       |

· · ·

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held
- [ ] 1c. Refinement loop complete (stage definitions v0 → vFinal)
- [ ] 1d. Strategic sign-off obtained on stages, criteria, and automation spec

##### Phase 2: Engineering
- [ ] 2a. Tech spec created (field specs, automation logic, dashboard designs)
- [ ] 2b. Engineering handoff meeting held
- [ ] 2c. Build complete (picklist, timestamps, validation, dashboards)
- [ ] 2d. QA/Test + customer sign-off

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped (stage reference guide, dashboard walkthrough)
- [ ] 3b. Pilot test with 3-5 reps complete
- [ ] 3c. Full team training delivered
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff (SME → Architect) complete
- [ ] 4c. External handoff (LeanScale → Customer) complete
- [ ] 4d. Project closed and archived

· · ·

#### Document Types

##### Working Documents (iterate together)

| Document                          | Purpose                                              | When Complete                              |
| --------------------------------- | ---------------------------------------------------- | ------------------------------------------ |
| Current-state audit report        | Baseline: stages, stagnation rates, data quality     | All data pulled, gaps quantified           |
| Stage definition worksheet        | Iterate on stage names, entry/exit criteria, probabilities | All stages approved by VP Sales        |
| Automation specification document | Document validation rules, timestamp logic, edge cases | All rules reviewed and approved          |

##### Deliverables (polished outputs)

| Deliverable                     | Created From                    | Customer Uses For                             |
| ------------------------------- | ------------------------------- | --------------------------------------------- |
| Stage definition reference card | Stage definition worksheet      | Rep quick-reference (1-page PDF)              |
| Pipeline velocity dashboards    | Automation spec + CRM build     | Leadership pipeline reviews                   |
| Admin documentation             | Automation spec + build notes   | RevOps maintains system post-handoff          |

· · ·

#### Enablement Details

##### Training Types

| Type       | Audience                           | Focus                                                              | Duration |
| ---------- | ---------------------------------- | ------------------------------------------------------------------ | -------- |
| Leadership | VP Sales, Sales Managers           | Interpret pipeline dashboards, run pipeline reviews, spot stagnation | 30 min   |
| Rep        | Full sales team                    | Stage definitions, when to change stages, why timestamps matter     | 45 min   |
| Technical  | RevOps, CRM Admin                 | How to modify stages, update automations, add new timestamp fields  | 60 min   |

##### Hypercare
- Applies: Yes
- Duration: 2 weeks post-go-live
- Office Hours: Weekly 30-min slot for questions and adjustments

##### Training Assets to Create
- [ ] Video walkthrough: Dashboard walkthrough for leadership
- [ ] Video walkthrough: Rep walkthrough of stage progression in CRM
- [ ] Doc: Stage definition quick-reference card (1-page PDF)
- [ ] Doc: Admin guide for field specs, automation logic, and dashboard filters

· · ·

#### Handoff & Retention

##### Internal Handoff (SME → Architect)
- Key context for Architect: Stage definitions, which automations are in place, known edge cases (reopened opps, multi-process record types)
- Escalation trigger: Any request to add/remove stages, change validation rules, or modify automation logic

##### External Handoff (LeanScale → Customer)
- Final meeting agenda: Review what was built, walk through dashboards, confirm governance process, answer questions
- Documentation package: Stage reference card, admin guide, training recordings, maintenance schedule

##### Maintenance Schedule
- Monthly: Review pipeline stagnation report, check timestamp population rates
- Quarterly: Full stage usage audit, conversion rate analysis, assess if stage definitions still match sales process

· · ·

#### Definition Alignment Terms

| Term                  | Typical Definition                                                                                      |
| --------------------- | ------------------------------------------------------------------------------------------------------- |
| Opportunity Stage     | A defined step in the sales process representing a meaningful milestone toward closing a deal            |
| Entry Criteria        | Specific conditions that must be true before an opportunity can be moved into a stage                    |
| Exit Criteria         | Conditions or actions that trigger movement from the current stage to the next                          |
| Stage Timestamp       | A date field that captures when an opportunity first enters a specific stage                             |
| Pipeline Velocity     | The speed at which opportunities move through the pipeline, calculated as (Opps x Deal Size x Win Rate) / Sales Cycle Length |
| Stage Stagnation      | An opportunity that has remained in a single stage beyond the expected duration threshold (typically 14+ days) |
| Probability %         | The forecasting weight assigned to each stage, representing likelihood of close at that stage           |
| Validation Rule       | CRM logic that prevents stage advancement unless required fields or criteria are met                     |

· · ·

#### Common Gotchas
- Too many stages (10+) causes reps to pick randomly → Limit to 5-8 stages maximum, each tied to a real sales milestone
- Generic stage names like "Evaluation" or "Qualification" become meaningless buckets → Use process-specific names ("Demo Completed", "Proposal Sent", "Contract Negotiation")
- Overly strict validation rules frustrate reps and create workarounds → Require only the fields genuinely needed for each stage transition
- No one maintains stage definitions after go-live → Assign a lifecycle owner and establish a quarterly review cadence
- Reopened Closed Lost opportunities create timestamp data issues → Build automation to handle re-entry: either reset timestamps or create new fields for re-entry dates
- Migration of in-flight deals causes data corruption → Create a migration plan: map existing opps to new stages in a staging environment first

· · ·

#### Methodology Options (if applicable)

| Option                           | When to Use                                                           | Complexity |
| -------------------------------- | --------------------------------------------------------------------- | ---------- |
| Simple (5-6 stages, basic timestamps) | Small team (&lt;15 reps), single sales motion, straightforward deal cycle | Low        |
| Standard (6-8 stages, full timestamps, validation rules, dashboards) | Mid-market team (15-50 reps), 1-2 sales motions, needs velocity reporting | Medium     |
| Advanced (multiple record types, segment-specific stages, automated stage progression) | Enterprise team (50+ reps), multiple sales processes/segments, complex routing | High       |

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on opportunity stage definitions, entry/exit criteria, probability mappings, and automation specification.
>
> **Output:** Definition Alignment Document + Stage Definition Package + Automation Specification (signed off by VP Sales and RevOps).

### 1a. Pre-Kickoff

> Two parallel tracks run after the AE closes and before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                     | Format             |
| ----------------------------- | ----------------------------------------------------------- | ------------------ |
| Intro video                   | Explain what a sales lifecycle project is and why it matters: deals stall without clear stage definitions, and leadership loses visibility into pipeline health | Video walkthrough (5-10 min)    |
| Definition Alignment Document | Get stakeholder sign-off on key terms: Opportunity Stage, Entry Criteria, Exit Criteria, Stage Timestamp, Pipeline Velocity, Stagnation | Google Doc         |
| Pre-filled intake form        | Confirm CRM platform, current stage values, known pain points, who has decision authority | Google Form or Doc |
| CRM access request            | Admin or read access to Opportunity object for audit        | Email              |

**Completion tracking:** Architect follows up within 48 hours if intake form or CRM access is not received. Do not cancel kickoff if incomplete, but flag risks.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                                    | Output                                    |
| ---- | ------------------------------------------------------------------------- | ----------------------------------------- |
| 1    | Pull opportunity report: stages, time in stage, conversion rates (6 months) | Raw CRM data                              |
| 2    | Identify stagnation (opps sitting 30+ days), data quality issues          | Current-state audit (quantified baseline) |
| 3    | Check existing timestamp fields and population rates                      | Field inventory with gaps                 |
| 4    | Draft v0 stage design: 5-8 stages aligned to common B2B sales milestones | Stage definition worksheet (v0)           |
| 5    | Prepare kickoff presentation with audit findings + recommendations        | Kickoff deck + questions list             |

**Critical:** Mark all v0 stage recommendations as ASSUMED. The kickoff call validates.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building anything.

| Term              | Our Definition                                                                                              | Internally Approved? |
| ----------------- | ----------------------------------------------------------------------------------------------------------- | -------------------- |
| Opportunity Stage | A defined step in the sales process representing a meaningful milestone toward closing                       | [ ] Yes / [ ] No     |
| Entry Criteria    | Specific conditions that must be true before moving an opp into a stage                                      | [ ] Yes / [ ] No     |
| Exit Criteria     | Actions or conditions that trigger movement to the next stage                                                | [ ] Yes / [ ] No     |
| Stage Timestamp   | Date field capturing when an opp first enters a stage                                                        | [ ] Yes / [ ] No     |
| Pipeline Velocity | Speed of deals through pipeline: (Opps x Deal Size x Win Rate) / Cycle Length                               | [ ] Yes / [ ] No     |
| Stagnation        | Opp sitting in a stage beyond expected threshold without movement                                            | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your sales leadership team. Check "Yes" when approved. We cannot proceed with CRM configuration until all terms are aligned — misaligned definitions cause rework.

---

### 1b. Kickoff Call

> **Purpose:** Present current-state audit and v0 stage design. Customer reacts to our work, not creates from scratch.

#### Agenda (60 min)

| Time  | Topic                          | What Happens                                                        |
| ----- | ------------------------------ | ------------------------------------------------------------------- |
| 0-15  | Walk through current-state audit | Show stagnation data, data quality issues, missing timestamps      |
| 15-30 | Present v0 stage design        | "Here are 6-8 stages we recommend based on your data and our experience" |
| 30-45 | Validate and correct           | Customer confirms which stages match, suggests changes               |
| 45-55 | Review Definition Alignment    | Walk through terms, get initial buy-in or flag disagreements         |
| 55-60 | Next steps                     | Schedule refinement meeting, assign homework (stage criteria review) |

#### What We Bring

- Current-state audit report (stagnation rates, data quality baseline, field inventory)
- v0 stage definition worksheet (5-8 recommended stages with initial criteria)
- Definition Alignment Document (pre-filled with our recommended definitions)
- Questions list (what we need to validate about their sales process)

#### What We Leave With

- Feedback on v0 stage design (which stages need adjustment, what's missing)
- Confirmed or corrected definitions
- Understanding of their actual sales process milestones
- Clear homework: customer reviews stage criteria, Architect creates v1

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Iterate on stage definitions and automation spec until sign-off.

#### The Pattern

```
Kickoff Call (gather info)
    ↓
Architect processes feedback → v1 stage definitions + draft automation spec
    ↓
Refinement Meeting (present v1, validate criteria, review automation logic)
    ↓
Architect finalizes → vFinal package
    ↓
Sign-Off Meeting
```

#### Before Each Meeting

1. Process previous meeting notes and feedback
2. Update stage definitions and automation spec
3. Prepare questions for remaining ASSUMED items

#### During Each Meeting

1. Walk through updated stage definitions with entry/exit criteria
2. Review automation logic (timestamps, validation rules, dashboards)
3. Capture corrections and additions
4. Confirm probability percentages for each stage

#### After Each Meeting

1. Update stage definition worksheet
2. Refine automation specification
3. Track what moved from ASSUMED → CONFIRMED

#### Meeting Types for This Project

| Meeting Type        | Focus                                                        | Stakeholder                   |
| ------------------- | ------------------------------------------------------------ | ----------------------------- |
| Sales Process       | Stage definitions, entry/exit criteria, probability mappings | VP Sales, Sales Managers      |
| Technical/RevOps    | Automation logic, validation rules, timestamp design         | RevOps Lead, CRM Admin        |
| Final Review        | Full walkthrough of stage package + automation spec          | VP Sales, RevOps, CRM Admin   |

#### Typical Timeline

| Milestone               | Timing                                    |
| ----------------------- | ----------------------------------------- |
| Pre-kickoff prep        | 2-3 days                                  |
| Kickoff call            | Day 1 of engagement                       |
| Refinement meeting      | 1 week after kickoff                      |
| Final review + sign-off | 1-2 weeks after refinement                |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything before building in CRM.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by VP Sales
- [ ] All opportunity stages defined with entry/exit criteria
- [ ] Probability percentages assigned to each stage
- [ ] Timestamp field design approved (which stages, naming convention, first-entry vs. re-entry)
- [ ] Validation rule logic approved (required fields per stage)
- [ ] Dashboard requirements confirmed (pipeline distribution, velocity, stagnation alerts)
- [ ] Migration plan for in-flight deals reviewed
- [ ] No blockers for engineering

#### Decision Point

- **Proceed to Engineering** → Customer wants full CRM build (typical path for this project)
- **Project complete** → Rare for Sales Lifecycle; strategy-only delivery would just be the stage definition document without CRM configuration

---

## Phase 2: Engineering

> **Goal:** Build and test the opportunity lifecycle in the customer's CRM based on the approved strategic package.
>
> **Output:** CRM with updated opportunity stages, timestamp fields, validation rules, automation, and pipeline dashboards — tested and customer-approved.

| Project Type    | Engineering Weight | This Project                                                  |
| --------------- | ------------------ | ------------------------------------------------------------- |
| Strategic-heavy | Light (10-20%)     | N/A                                                          |
| **Balanced**    | **Medium-Heavy (40-60%)** | **Sales Lifecycle — CRM config, automation, dashboards** |
| Technical-heavy | Heavy (70-90%)     | N/A                                                          |

### Sub-Phases

```
2a Tech Spec → 2b Engineering Handoff → 2c Build → 2d Test
```

---

### 2a. Tech Spec (Agent-Assisted)

> **Purpose:** Translate stage definitions and automation spec into CRM-specific technical specifications.

**Input:** Signed-off stage definition package + automation specification from Phase 1

**What happens:**

1. Architect translates strategic stage definitions into CRM object/field specifications
2. Maps each stage to picklist values, probability percentages, and record type associations
3. Specifies timestamp field names, types (Date vs. DateTime), and auto-population logic
4. Documents validation rule logic (required fields per stage transition)
5. Defines dashboard components (report types, filters, groupings)

**Output:** Tech spec containing:

- **Stage picklist spec:** New values, deprecated values, migration mappings for in-flight deals
- **Timestamp field spec:** Field names (e.g., "Stage Hit Date - Discovery"), field type, auto-populate logic ("set if blank" to prevent overwrite)
- **Automation spec:** Flow/workflow triggers (stage change → set timestamp), probability auto-update rules
- **Validation rule spec:** Required fields per stage (e.g., "Close Date required for Negotiation"), error messages
- **Dashboard spec:** Pipeline distribution chart, stage conversion rates, time-in-stage report, stagnation alerts (14+ days), scheduled email to leadership

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs with engineer before building.

**Who attends:** Architect + Engineer (or CRM Admin)

**Agenda (30-45 min):**

| Time  | Topic              | What Happens                                          |
| ----- | ------------------ | ----------------------------------------------------- |
| 0-15  | Walk through specs | Architect explains stage definitions + automation logic       |
| 15-30 | Engineer questions | Clarify CRM-specific constraints, flag risks (e.g., existing workflows that conflict) |
| 30-45 | Build plan         | Agree on build sequence, identify dependencies         |

**What Architect brings:**

- Strategic package (stage definitions, criteria, probabilities)
- Draft tech spec (field mappings, automation logic, dashboard designs)
- Migration plan for in-flight deals

**What engineer leaves with:**

- Approved tech spec
- Build sequence: (1) stage picklist → (2) timestamp fields → (3) automation flows → (4) validation rules → (5) dashboards
- Known risks (conflicting existing automations, record type constraints)

---

### 2c. Build (Configure)

> **Purpose:** Configure the opportunity lifecycle in the customer's CRM.

**Input:** Approved tech spec from 2b

**Build sequence (recommended order):**

| Step | Component                     | What Gets Built                                                        | CRM Location                                      |
| ---- | ----------------------------- | ---------------------------------------------------------------------- | ------------------------------------------------- |
| 1    | Stage picklist update         | New stage values, probabilities, deprecated stages mapped/archived      | Salesforce: Setup &gt; Object Manager &gt; Opportunity &gt; Fields &gt; Stage |
| 2    | Stage timestamp fields        | Custom date fields for each stage (e.g., "Stage Hit Date - Discovery") | Salesforce: Custom Fields on Opportunity object   |
| 3    | Timestamp automation          | Record-Triggered Flows: on stage change, set timestamp if blank        | Salesforce: Setup &gt; Flows                         |
| 4    | Validation rules              | Required fields per stage transition, prevent stage-skipping if applicable | Salesforce: Setup &gt; Object Manager &gt; Opportunity &gt; Validation Rules |
| 5    | Page layout updates           | Add timestamp fields to opportunity page layout, configure Sales Path/Guidance | Salesforce: Page Layouts + Path Settings       |
| 6    | Pipeline dashboards           | Pipeline distribution, conversion rates, time-in-stage, stagnation alerts | Salesforce: Dashboards + Reports                  |
| 7    | In-flight deal migration      | Map existing opportunities to new stages per migration plan             | Data Loader or manual update                      |

**Execution approach for this project:** Manual build — CRM configuration requires human judgment for validation rule logic, page layout design, and migration of in-flight deals. Engineer reviews each component before moving to next.

**Build tracking:**

- [ ] Stage picklist updated with new values and probabilities
- [ ] Deprecated stages archived or removed
- [ ] All timestamp fields created
- [ ] Timestamp automation flows active and tested
- [ ] Validation rules deployed
- [ ] Page layouts updated with new fields and Sales Path guidance
- [ ] Pipeline dashboards built and filtered correctly
- [ ] In-flight deals migrated to new stages
- [ ] Scheduled dashboard email configured for leadership

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify the build works and get customer approval.

**Two types of testing:**

| Type              | Who      | Purpose                                                      |
| ----------------- | -------- | ------------------------------------------------------------ |
| Technical Testing | Our team | Verify it works: stages progress, timestamps populate, validation fires |
| Customer Testing  | Customer | Verify it meets their needs: stages make sense, dashboards show right data |

**Technical testing checklist:**

- [ ] All new stage values appear in picklist with correct order and probabilities
- [ ] Moving an opp through each stage populates the corresponding timestamp field
- [ ] Timestamp fields do NOT overwrite when opp re-enters a stage (set-if-blank logic)
- [ ] Validation rules fire correctly: required fields enforced, appropriate error messages shown
- [ ] Validation rules do NOT fire incorrectly (false positives blocking legitimate stage changes)
- [ ] Sales Path/Guidance displays correct instructions for each stage
- [ ] Pipeline distribution dashboard shows correct count and value by stage
- [ ] Stage conversion rate report calculates correctly
- [ ] Time-in-stage report shows accurate average days per stage
- [ ] Stagnation alert report correctly identifies opps stuck 14+ days
- [ ] Scheduled dashboard email sends to correct recipients
- [ ] In-flight deals migrated correctly (spot-check 10-20 records)
- [ ] Edge case: Closed Lost opp reopened — verify timestamp behavior is as designed

**Customer testing:**

- Walk VP Sales through pipeline dashboards
- Have 2-3 reps move sample opportunities through all stages
- Confirm stage definitions and criteria match their actual process
- Test validation rules with real scenarios

**Engineering sign-off checkpoint:**

- [ ] Built system matches tech spec
- [ ] All technical tests passing
- [ ] Customer has tested and approved
- [ ] Ready for enablement

**Decision point:**

- **Proceed to Enablement** → System is built, needs pilot testing and team training
- **Loop back to Build** → Issues found, needs fixes

---

## Phase 3: Enablement

> **Goal:** Sales team can correctly use the new opportunity lifecycle, and leadership can interpret pipeline dashboards.
>
> **Output:** Trained team with documentation, validated through pilot, no critical issues.

### Sub-Phases

```
3a Training Prep → 3b Pilot Test + Training Sessions → 3c Hypercare → 3d Enablement Sign-Off
```

---

### 3a. Training Prep (Agent-Assisted)

> **Purpose:** Create training materials from stage definitions and CRM configuration.

**Input:** Stage definition package + tech specs + configured CRM system

**What happens:**

1. Architect creates training materials tailored to three audiences (leadership, reps, admin)
2. Builds stage reference card (1-page PDF) from stage definition worksheet
3. Prepares video walkthrough scripts for dashboard navigation

**Output:** Training package containing:

- **Stage quick-reference card:** 1-page PDF listing each stage, entry criteria (2-3 bullets), and probability %
- **Video walkthrough scripts:** Dashboard navigation for leadership, stage progression walkthrough for reps
- **Admin guide:** Field specifications, automation logic, how to modify stages and rules
- **FAQ draft:** Based on common questions from similar projects (e.g., "What if I need to go back a stage?", "Why can't I skip to Proposal?")

---

### 3b. Pilot Test + Training Sessions

> **Purpose:** Validate the lifecycle works in practice, then train the full team.

#### Pilot Test (Before Full Rollout)

- Select 3-5 reps for pilot group (mix of tenures and skill levels)
- Have pilot reps process 5-10 real opportunities through the full lifecycle
- Observe: confusion points, friction with validation rules, workaround behaviors
- Collect structured feedback on stage definitions, criteria clarity, and usability
- Adjust configuration based on pilot findings before full rollout

#### Training Sessions

**Two types of training:**

| Type                | Audience                          | Focus                                                                      | Duration |
| ------------------- | --------------------------------- | -------------------------------------------------------------------------- | -------- |
| Leadership training | VP Sales, Sales Managers          | How to read pipeline dashboards, identify stagnation, run pipeline reviews  | 30 min   |
| Rep training        | Full sales team                   | Stage definitions, entry criteria, what changes when you move stages, why timestamps matter | 45 min   |
| Technical handoff   | RevOps, CRM Admin                | How to maintain: modify stages, update automations, add fields, troubleshoot | 60 min   |

**Training delivery:**

1. Schedule sessions with appropriate stakeholders (can combine leadership + rep into a single 60-min session)
2. Deliver training live — emphasize "why" not just "how" (reps need to understand that timestamp data enables velocity reporting that helps the whole team)
3. Record video walkthroughs for future reference (new hire onboarding)
4. Distribute stage reference card to all reps
5. Answer questions, note gaps for FAQ

**Output:**

- Trained stakeholders
- Video recordings (dashboard + rep walkthrough)
- Questions log (feeds into FAQ)
- Configuration adjustments from pilot feedback

---

### 3c. Hypercare

> **Purpose:** Intensive post-launch support to stabilize the new lifecycle.

**Duration:** 2 weeks

**What happens:**

- Quick response to questions about stage definitions or when to advance
- Weekly 30-min office hours slot where reps can bring real deal scenarios
- Monitor timestamp population rates daily for first week (target: 95%+ of new opps)
- Fix any validation rule issues causing friction
- Adjust dashboards based on leadership feedback

**When to extend:** If timestamp population rates are below 80% after week 1, extend hypercare by 1 week and schedule additional coaching.

**Output:** Stabilized system, 95%+ stage adoption rate on new opportunities, no critical issues outstanding

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm the sales team can operate the new lifecycle independently.

**Validation checkpoint:**

- [ ] All training sessions delivered (leadership, rep, technical)
- [ ] Training recordings and stage reference card distributed
- [ ] Pilot test completed with feedback incorporated
- [ ] Hypercare period complete
- [ ] Timestamp population rate at 95%+ for new opportunities
- [ ] Pipeline review meetings using new stages and dashboards
- [ ] No critical issues outstanding
- [ ] Customer team can operate without daily support

**Decision point:**

- **Proceed to Handoff** → Team is enabled, system is stable
- **Extend Hypercare** → Adoption below target, needs more coaching time

---

## Phase 4: Handoff

> **Goal:** Clean project close with maintenance plan established and retention/expansion path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the system, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule → 4b Internal Handoff → 4c External Handoff → 4d Project Close
                          (SME → Architect)            (LS → Customer)       (Archive + Debrief)
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At                                                                         |
| ----------------------------- | -------------------- | ------------------------------------------------------------------------------------- |
| **Single Project**            | Customer owns        | 4c (External Handoff) — customer receives maintenance schedule and runs it themselves |
| **Dedicated (Multi-Project)** | Architect owns              | 4b (Internal Handoff) — Architect receives maintenance schedule and runs it for customer     |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention after the project is complete.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task                   | What to Check                                                         | Red Flag Threshold                              |
| ------------------------------ | --------------------------------------------------------------------- | ----------------------------------------------- |
| Timestamp population audit     | % of new opps with all timestamp fields populated                     | Below 90% — reps are skipping or working around |
| Stagnation review              | Opps sitting 14+ days in any stage without movement                   | &gt;20% of active pipeline stagnating              |
| Pipeline review meeting        | Are meetings using the new stages and dashboards consistently?        | Leadership reverting to old ad-hoc methods      |

**Quarterly Tasks:**

| Quarterly Task                | What to Review                                                      | Action if Off-Track                              |
| ----------------------------- | ------------------------------------------------------------------- | ------------------------------------------------ |
| Stage conversion rate analysis | Are conversion rates between stages within expected ranges?          | Investigate: is it a data issue or process issue? |
| Stage definition review       | Do current stage definitions still match the actual sales process?   | Update criteria, retrain if needed               |
| Validation rule effectiveness | Are rules preventing bad data or just frustrating reps?              | Adjust or remove rules that add friction without value |
| Dashboard usage audit         | Are stakeholders actually using pipeline dashboards?                 | Re-train or simplify dashboards                  |

**After First Business Cycle (60-90 days post-launch):**

- **Pipeline velocity baseline:** Compare pre-project velocity to post-project velocity. Expect 15-25% improvement in average days to close [1].
- **Stage adoption validation:** Confirm 95%+ of new opportunities have timestamps populated consistently.
- **Key question:** Is the team using stage definitions consistently, or have informal workarounds emerged?

**Refinement Triggers (when to re-engage):**

| Trigger                      | Threshold                                             | Response                                           |
| ---------------------------- | ----------------------------------------------------- | -------------------------------------------------- |
| Timestamp adoption drop      | Below 85% population rate for 2+ weeks                | Re-train reps, check if validation rules were disabled |
| Stagnation spike             | &gt;30% of pipeline stagnating in a single stage         | Investigate: is the stage definition wrong or is the process broken? |
| New sales motion added       | Company adds new product line or sales process         | Scope new project: may need additional record types or stages |
| Stage definitions drift      | Reps using stages inconsistently across team           | Schedule refresher training, update reference card |

**Every 6-12 Months:**

- Full stage audit: are all stages still relevant? Any stages that should be added or removed?
- Sales process alignment check: has the sales process changed since implementation?
- Dashboard refresh: are the metrics still the right ones for leadership?

---

### 4b. Internal Handoff (SME → Architect)

> **Purpose:** Transfer context so Architect can manage ongoing relationship.

**What the Architect needs to know:**

- What was built: stage definitions, timestamp fields, validation rules, dashboards
- Strategic context: why these specific stages were chosen (tied to their actual sales milestones)
- Common issues: most questions will be about "what stage should this deal be in?" — refer to stage reference card
- When to escalate back to SME: any request to change stage definitions, modify validation rules, or add new record types

**Escalation guidelines:**

| Issue Type                                          | Who Handles                                | Analogy                 |
| --------------------------------------------------- | ------------------------------------------ | ----------------------- |
| "What stage should this deal be in?"                | Architect (refer to stage reference card)         | General contractor      |
| "Can we add a new stage?" or "Change validation"    | SME (requires strategic + technical review) | Specialist tradesperson |
| Dashboard filter adjustment, report access           | Architect                                  | General contractor      |
| New sales process or record type needed             | SME (scope as new project)                 | Specialist tradesperson |

**For Dedicated engagements:** Architect also receives the maintenance schedule (4a) and becomes responsible for executing monthly and quarterly tasks.

---

### 4c. External Handoff (LeanScale → Customer)

> **Purpose:** Formal project completion with customer.

**Final project meeting (30-45 min):**

- Review what was delivered: stage definitions, CRM configuration, dashboards, training materials
- Walk through documentation package
- Demo: show how to run a pipeline review using new dashboards
- Confirm governance process: who owns lifecycle changes, how to request modifications
- **For Single Project engagements:** Walk through maintenance schedule in detail, record a video walkthrough
- Make it explicit: "Project complete"

**Documentation package:**

- Stage definition reference card (1-page PDF)
- Admin guide (field specs, automation logic, dashboard filters)
- Training video recordings
- FAQ document
- Definition Alignment Document (final version)
- Maintenance Schedule
- Support contact info

**Output:** Customer owns the system. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location
- [ ] Handoff documentation complete
- [ ] Project status updated in tracking system

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell → Downsell → Retry    |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (retainer)
   ↓ if no
2. Downsell: Another one-time project
   - Natural next projects: Forecasting Process Implementation, Lead Lifecycle, Executive Reporting Suite
   ↓ if yes
3. Retry retainer at end of next project cycle
```

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff — review how the sales lifecycle is performing: timestamp adoption rates, pipeline velocity changes, any stage definitions that need updating.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- Stage Definition Package: All opportunity stages with entry/exit criteria, probability percentages, and stage-specific guidance
- Definition Alignment Document: Signed-off term definitions agreed upon by all stakeholders
- Current-State Audit Report: Baseline metrics including stagnation rates, data quality, and pipeline distribution

**Technical Deliverables:**

- CRM configuration: Updated opportunity stage picklist with probabilities
- Timestamp fields: Custom date fields for each stage, auto-populated via automation
- Validation rules: Required field enforcement for stage transitions
- Sales Path/Guidance: In-CRM guidance for each stage (Salesforce Lightning) or deal property guidance (HubSpot)
- Pipeline dashboards: Distribution, conversion rates, time-in-stage, stagnation alerts
- Scheduled dashboard email for leadership

**Documentation Package:**

- Training video recordings (dashboard walkthrough, rep stage guide, admin maintenance)
- Stage quick-reference card (1-page PDF)
- Admin guide (field specs, automation logic, dashboard filters, troubleshooting)
- FAQ document
- Definition Alignment Document (final version)
- Maintenance Schedule

---

## Appendix (Condensed)

### What This Document Is

This is the implementation playbook for Sales Lifecycle projects — the step-by-step execution guide an Architect follows to deliver from first contact to project close. It covers all four phases: Strategy, Engineering, Enablement, and Handoff.

### What Each Phase Produces

| Phase                    | Output                                                                 | Gate Criteria                                                                  |
| ------------------------ | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **Phase 1: Strategy**    | Signed-off stage definition package + automation spec                  | VP Sales approved definitions; all stages have entry/exit criteria             |
| **Phase 2: Engineering** | Configured CRM with stages, timestamps, validation, dashboards         | All technical tests pass; customer has tested and approved                     |
| **Phase 3: Enablement**  | Trained team with documentation, validated through pilot               | 95%+ timestamp adoption on new opps; all training delivered                   |
| **Phase 4: Handoff**     | Independent customer + archived project                                | Internal/external handoffs complete; maintenance plan in place; project closed |

### How to Adapt Per Project Type

This project is **Balanced** — roughly 30% Strategy, 40% Engineering, 20% Enablement, 10% Handoff.

| Project Profile | Strategy Weight | Engineering Weight | Enablement Weight | Where Sales Lifecycle Fits |
| --------------- | --------------- | ------------------ | ----------------- | -------------------------- |
| Strategic-heavy | 60-80%          | 10-20%             | 10-20%            |                            |
| **Balanced**    | **30%**         | **40%**            | **20%**           | **Sales Lifecycle**        |
| Engineering-heavy | 10-20%        | 60-80%             | 10-20%            |                            |

**Adaptation rules:**

- Strategy phase can compress to 2 meetings if the customer already has a well-documented sales process and just needs CRM representation
- Engineering phase expands significantly if there are multiple record types, sales processes, or segment-specific stage tracks
- Enablement is critical — even a well-built lifecycle fails if reps don't adopt it. Companies with structured pipeline processes grow revenue 28% faster than those without [2]
- Phase 4 always applies — governance is the difference between a lifecycle that works for years and one that degrades within months

### Why Stage Definitions Matter: The Data

44% of executives believe their organizations are ineffective at managing sales opportunities [3]. Average CRM adoption rates sit at only 26% across sectors [4], and 63% of sales managers say their organization does a poor job managing its pipeline [3]. A well-implemented sales lifecycle with clear stage definitions directly addresses these problems: automated deal tracking improves close rates by 17%, and CRM usage with enforced stages shortens sales cycles by 8-14 days [4].

The average B2B SaaS sales cycle is 84 days [5], with win rates typically between 25-35% depending on deal size. Structured pipeline management — the core output of this project — correlates with 28% higher revenue growth [2].

---

## References

[1] [Salesforce State of Sales 2024](https://www.salesforce.com/resources/research-reports/state-of-sales/) — Pipeline velocity improvement benchmarks for B2B organizations implementing structured stage management

[2] [SuperOffice - Sales Pipeline Management Strategies](https://www.superoffice.com/blog/sales-pipeline-management-tips/) — Companies with structured pipeline management grow revenue 28% faster

[3] [Harvard Business Review - Sales Pipeline Management Research](https://hbr.org/) — 44% of executives believe their organizations are ineffective at managing sales opportunities; 63% of sales managers rate pipeline management as poor

[4] [CRM.org - CRM Statistics 2026](https://crm.org/crmland/crm-statistics) — Average CRM adoption rates at 26%; automated deal tracking improves close rates by 17%; CRM usage shortens sales cycles by 8-14 days

[5] [The Digital Bloom - 2025 B2B SaaS Funnel Benchmarks](https://thedigitalbloom.com/learn/pipeline-performance-benchmarks-2025/) — Average B2B SaaS sales cycle is 84 days; win rates 25-35% depending on deal size

[6] [Operatus - Time Stamps For Staging](https://www.operatus.io/blog/time-stamps-for-staging) — Date stamping best practices: automation should be built immediately after stage standardization; use Record-Triggered Flows
