# Lead Lifecycle — Implementation

---

## Project One-Pager

> Quick reference for architects. One per project type. Fill this out FIRST -- it serves as the project's identity card.

### Lead Lifecycle One-Pager

#### Project Type

- Category: Balanced (Strategic + Technical)
- Primary Deliverable: Fully implemented lead lifecycle with defined stages, automated transitions, timestamp tracking, and funnel dashboards in the CRM

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
  │    Medium    │     │    Heavy     │     │    Medium    │     │    Medium    │
  │ 1a→1b→1c→1d │     │ 2a→2b→2c→2d │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   3-4 meetings         CRM config +         Sales + Mktg        Maintenance +
   stage definitions    MAP sync             training             retention path
```

**This project's flow:**
- Full 4-phase. Medium strategy (stage definitions, criteria alignment), heavy engineering (CRM config, automation, MAP sync), standard enablement, standard handoff.
- Phase 1 typically requires 3-4 meetings: Kickoff, Stage Definition Workshop, Criteria Alignment, Sign-Off.
- Phase 2 is the heaviest -- building fields, automation rules, MAP integration, and dashboards.

· · ·

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Watch intro video explaining lead lifecycle concepts and why stage definitions matter
- [ ] Complete intake form documenting current lead statuses, hand-off points, and known pain points
- [ ] Get VP Sales + VP Marketing aligned on who attends the Stage Definition Workshop
- [ ] Provide CRM admin access (Salesforce or HubSpot) and MAP admin access

##### Track B: Architect Prep
- [ ] Pull CRM lead status report: all leads by current status value, identify inconsistencies
- [ ] Audit existing automation rules that touch Lead Status field
- [ ] Check for existing timestamp fields (MQL Date, SQL Date, etc.)
- [ ] Draft v0 stage architecture based on industry frameworks (Forrester Demand Waterfall, Winning by Design)
- [ ] Prepare current-state process map showing lead flow from creation to close/disqualification

· · ·

#### Refinement Loop (1b -> 1c -> 1d)

| Meeting              | Sub-Phase | Focus                                                      | Stakeholder                        | Output                           |
| -------------------- | --------- | ---------------------------------------------------------- | ---------------------------------- | -------------------------------- |
| Kickoff              | 1b        | Present v0 stage architecture, validate current-state map  | VP Marketing, VP Sales, RevOps     | Feedback for v1 stage proposal   |
| Stage Definition     | 1c        | Define entry criteria for each stage, transition rules     | VP Marketing, VP Sales, RevOps     | v2 with agreed stage criteria    |
| Criteria Alignment   | 1c        | Finalize MQL/SAL/SQL definitions, disqualification reasons | VP Marketing, VP Sales             | v3 with signed-off criteria      |
| Sign-Off             | 1d        | Full walkthrough of lifecycle design, approve for build    | All stakeholders                   | Final strategic package          |

· · ·

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held
- [ ] 1c. Refinement loop complete (v0 -> vFinal stage architecture)
- [ ] 1d. Strategic sign-off obtained on stage definitions and transition rules

##### Phase 2: Engineering
- [ ] 2a. Tech spec created (field list, automation logic, MAP sync rules)
- [ ] 2b. Engineering handoff meeting held
- [ ] 2c. Build complete (fields, automation, MAP sync, dashboards)
- [ ] 2d. QA/Test + customer sign-off

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped (sales guide, marketing guide, dashboard walkthrough)
- [ ] 3b. Training sessions delivered (sales team + marketing team)
- [ ] 3c. Hypercare period complete (2 weeks post-go-live)
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff complete
- [ ] 4c. External handoff complete
- [ ] 4d. Project closed and archived

· · ·

#### Document Types

##### Working Documents (iterate together)

| Document                        | Purpose                                           | When Complete                               |
| ------------------------------- | ------------------------------------------------- | ------------------------------------------- |
| Lead Status Audit Report        | Map current CRM lead statuses and data quality    | All current statuses documented             |
| Stage Architecture Draft        | Proposed lifecycle stages with entry criteria      | All stages defined with measurable criteria |
| Transition Rules Matrix         | Auto vs manual triggers for each stage change     | Every transition has a defined trigger      |
| MAP Sync Mapping                | CRM-to-MAP field mapping with sync direction      | All fields mapped, sync rules documented    |

##### Deliverables (polished outputs)

| Deliverable                    | Created From                 | Customer Uses For                          |
| ------------------------------ | ---------------------------- | ------------------------------------------ |
| Lead Lifecycle Process Map     | Stage Architecture Draft     | Internal alignment, board presentation     |
| Stage Definition Document      | Stage Architecture Draft     | Rep reference, onboarding new hires        |
| Funnel Dashboard               | Transition Rules + Timestamps| Conversion rate tracking, velocity analysis|

· · ·

#### Enablement Details

##### Training Types

| Type       | Audience                          | Focus                                                  | Duration |
| ---------- | --------------------------------- | ------------------------------------------------------ | -------- |
| Leadership | VP Marketing, VP Sales, RevOps    | How to read funnel dashboards, interpret conversion rates, take action on velocity data | 30 min   |
| Sales      | SDRs, AEs, Sales Managers         | Stage definitions, when/how to update lead status, what's automated vs manual           | 45 min   |
| Marketing  | Marketing Ops, Demand Gen         | MQL criteria, MAP sync behavior, how to monitor MQL volume and quality                  | 30 min   |
| Technical  | RevOps Admin                      | How to maintain automation rules, add/modify stages, troubleshoot sync issues            | 60 min   |

##### Hypercare
- Applies: Yes
- Duration: 2 weeks post-go-live
- Office Hours: Yes -- weekly 30-min slot for first 2 weeks

##### Training Assets to Create
- [ ] Video walkthrough: Dashboard walkthrough (conversion rates, velocity, leakage)
- [ ] Video walkthrough: How to update lead status (sales rep perspective)
- [ ] Doc: Stage definitions quick-reference 1-pager
- [ ] Doc: FAQ covering common scenarios (recycled leads, re-engagement, etc.)
- [ ] Doc: Automation logic reference (what fires when)

· · ·

#### Handoff & Retention

##### Internal Handoff
- Key context for Architect: Stage definitions and criteria, which automations exist, common data quality issues encountered during build, dashboard locations
- Escalation trigger: Any change to stage definitions, automation logic modifications, MAP sync issues

##### External Handoff
- Final meeting agenda: Review lifecycle implementation, walk through dashboards, confirm documentation package, answer questions
- Documentation package: Stage Definition Document, Automation Logic Reference, Dashboard Guide, Training recordings, FAQ, Maintenance Schedule

##### Maintenance Schedule
- Monthly: Review conversion rates and velocity; check for leads stuck in stages; audit data quality
- Quarterly: Re-validate stage definitions with sales and marketing; review disqualification reasons

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services -> if no -> Downsell: Lead Scoring project or Marketing-to-Sales Handoff SLA project -> Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~90 days post-go-live
- Internal prep trigger: 2 weeks before
- Decision: Architect handles / SME needed

· · ·

#### Definition Alignment Terms

| Term                     | Typical Definition                                                                                      |
| ------------------------ | ------------------------------------------------------------------------------------------------------- |
| Lead                     | An individual who has expressed interest or been identified as a potential buyer                         |
| MQL (Marketing Qualified Lead) | A lead that meets ICP criteria AND has taken a qualifying action (e.g., demo request, content download + ICP fit) |
| SAL (Sales Accepted Lead)      | An MQL that a sales rep has reviewed and accepted as worth pursuing (ICP verified, valid contact info)   |
| SQL (Sales Qualified Lead)     | A SAL where discovery has been completed and budget/timeline/authority confirmed                        |
| Working / Engaged              | A lead where the sales rep has made contact and a conversation is in progress                           |
| Meeting Set                    | A confirmed meeting on calendar with a decision-maker                                                  |
| Opportunity Created            | Lead has been converted to an opportunity record in the CRM                                            |
| Disqualified                   | Lead does not meet criteria -- with sub-reasons: bad fit, no budget, competitor, bad data, timing       |
| Recycled / Nurture             | Previously qualified lead returned to marketing for continued nurture (not lost, just not ready)        |
| Lead Velocity                  | Average time a lead spends in each stage before moving to the next                                      |
| Conversion Rate                | Percentage of leads that move from one stage to the next                                               |

· · ·

#### Common Gotchas
- Too many stages (10+) confuses reps and reduces adoption -> Limit to 5-7 stages maximum
- No timestamp fields built -> Velocity reporting becomes impossible; always build timestamps as part of the core build, not an add-on
- Sales and marketing disagree on MQL definition mid-build -> Get both VPs in the same room during Phase 1c and get written sign-off before any CRM work
- MAP sync conflicts overwrite CRM data -> Define sync direction (CRM-wins vs MAP-wins) per field before configuring
- Reps ignore new statuses post-go-live -> Automate as many transitions as possible so reps only update what requires human judgment
- Missing "Disqualified" sub-reasons -> Without sub-reasons, you cannot report on why leads are lost; require at least 4-5 sub-reasons from day one

· · ·

#### Methodology Options (if applicable)

| Option                        | When to Use                                    | Complexity |
| ----------------------------- | ---------------------------------------------- | ---------- |
| Simple (5-stage lifecycle)    | Early-stage company, &lt;50 leads/month, no MAP   | Low        |
| Standard (7-stage lifecycle)  | Growth-stage, MAP integrated, dedicated RevOps | Medium     |
| Advanced (7+ with scoring)    | Mature org, lead scoring in place, multi-segment ICP | High  |

> See Methodology for detailed decision framework on stage architecture selection.

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on lead lifecycle stage definitions, entry criteria, and transition rules.
>
> **Output:** Definition Alignment Document + Stage Architecture Document + Transition Rules Matrix (signed off by VP Marketing, VP Sales, and RevOps).

### 1a. Pre-Kickoff

> Two parallel tracks run after the deal closes and before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                         | Format             |
| ----------------------------- | --------------------------------------------------------------- | ------------------ |
| Intro video                   | Explain lead lifecycle concepts, stage definitions, and why this matters for conversion visibility | Video (5-10 min)   |
| Definition Alignment Document | Pre-filled with recommended definitions for MQL, SAL, SQL, Disqualified | Google Doc         |
| Lead Lifecycle Intake Form    | Capture current lead statuses, hand-off points, pain points, CRM/MAP details | Google Form or Doc |

**What to include in the intake form:**
- Current CRM platform and version (Salesforce Classic/Lightning, HubSpot Pro/Enterprise)
- Current MAP platform (HubSpot, Marketo, Pardot, etc.)
- List of current lead status values in use
- How do reps currently define "qualified"?
- What are the biggest friction points in lead hand-offs?
- Are there existing SLAs between marketing and sales?
- What frameworks do they reference internally (Forrester Demand Waterfall, Winning by Design Bowtie)?

**Completion tracking:** RevOps lead or Architect follows up. Do not cancel kickoff if incomplete, but push hard -- the intake form is critical for building a useful v0.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                               | Output                                  |
| ---- | -------------------------------------------------------------------- | --------------------------------------- |
| 1    | Pull CRM lead report by status -- identify messy/inconsistent values | Lead Status Audit Report                |
| 2    | Audit existing automation rules that update lead status              | Automation inventory                    |
| 3    | Check for existing timestamp fields and formula fields               | Field inventory (what exists vs needed) |
| 4    | Draft v0 stage architecture using intake + industry frameworks       | v0 Stage Architecture (all ASSUMED)     |
| 5    | Create current-state process map showing lead flow                   | Visual flowchart with pain points       |

**Critical:** Mark everything as ASSUMED. The kickoff call validates.

**CRM Audit focus areas:**
- How many leads have no status or a blank status value?
- How many unique status values exist? (Companies with 10+ are common and indicate sprawl.)
- Are there leads stuck in limbo stages for 90+ days?
- Do timestamp fields exist for any stages?

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building anything. The MQL definition is the single most contentious item in a lead lifecycle project -- resolving it early prevents weeks of rework [1].

| Term         | Our Definition                                                                    | Internally Approved? |
| ------------ | --------------------------------------------------------------------------------- | -------------------- |
| MQL          | Lead matches ICP profile AND has taken a qualifying action (demo request, pricing page visit + content download) | [ ] Yes / [ ] No     |
| SAL          | MQL reviewed by sales rep, ICP verified, valid contact info confirmed             | [ ] Yes / [ ] No     |
| SQL          | SAL where discovery is complete: budget, timeline, authority confirmed             | [ ] Yes / [ ] No     |
| Disqualified | Lead does not meet criteria; sub-reason required (bad fit, no budget, competitor, bad data, timing) | [ ] Yes / [ ] No     |
| Recycled     | Previously qualified lead returned to nurture; not lost, not ready now             | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your VP Sales and VP Marketing. Check "Yes" when approved. We cannot proceed to engineering until all terms are aligned. Expect this to take 1-2 meetings to finalize.

---

### 1b. Kickoff Call

> **Purpose:** Present v0 stage architecture and validate current-state assessment. We walk in with work done -- customer reacts, not creates from scratch.

#### Agenda (60-90 min)

| Time  | Topic                            | What Happens                                                      |
| ----- | -------------------------------- | ----------------------------------------------------------------- |
| 0-15  | Walk through current-state map   | "Here's what we found in your CRM audit"                          |
| 15-30 | Present v0 stage architecture    | "Here's what we recommend based on your intake and industry norms" |
| 30-45 | Validate definitions             | Review Definition Alignment Doc, ASSUMED -> CONFIRMED or corrected |
| 45-55 | Identify hand-off friction       | Where do leads fall through the cracks today?                      |
| 55-65 | MAP sync discussion              | What syncs today? What should sync?                                |
| 65-75 | Next steps                       | Schedule Stage Definition Workshop, assign homework                |

#### What We Bring

- Lead Status Audit Report (current-state data)
- v0 Stage Architecture (recommended 5-7 stages with draft criteria)
- Current-state process map (visual)
- Definition Alignment Document (pre-filled with recommendations)
- Questions list: What does your team consider a "hot lead"? How do you decide when a lead is dead?

#### What We Leave With

- Feedback and corrections on v0 (info needed for v1)
- Confirmed or challenged definitions (clear on where disagreements exist)
- Stage Definition Workshop scheduled (ideally within 1 week)
- Homework: VP Sales reviews SAL criteria, VP Marketing reviews MQL criteria

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Iterate on stage architecture until all stakeholders agree on definitions and transition rules.

#### The Pattern

```
Kickoff Call (present v0, gather feedback)
    |
v1 Stage Architecture
    |
Stage Definition Workshop (present v1, define entry criteria)
    |
v2 with agreed criteria
    |
Criteria Alignment Meeting (finalize MQL/SAL/SQL with both VPs)
    |
v3 (final draft)
    |
Sign-Off Review -> Approved
```

#### Before Each Meeting

1. Update stage architecture based on previous meeting feedback
2. Prepare specific questions for remaining ASSUMED items
3. Pre-circulate updated document so stakeholders can review before the meeting

#### During Each Meeting

1. Walk through current version, highlighting changes since last session
2. Capture corrections and new criteria
3. Track what moved from ASSUMED -> CONFIRMED
4. Flag remaining disagreements explicitly -- do not let them go unresolved

#### After Each Meeting

1. Update stage architecture document
2. Update transition rules matrix
3. Send summary email: what was confirmed, what's still open, homework for next session

#### Meeting Types for Lead Lifecycle

| Meeting Type            | Focus                                                    | Stakeholder                    |
| ----------------------- | -------------------------------------------------------- | ------------------------------ |
| Kickoff                 | Current state, v0 architecture, initial definitions      | VP Marketing, VP Sales, RevOps |
| Stage Definition        | Entry criteria per stage, transition rules (auto vs manual) | VP Marketing, VP Sales, RevOps |
| Criteria Alignment      | Final MQL/SAL/SQL definitions, disqualification reasons  | VP Marketing, VP Sales         |
| Sign-Off                | Full lifecycle design review, approve for engineering     | All stakeholders               |

#### Typical Timeline

| Milestone               | Timing                                |
| ----------------------- | ------------------------------------- |
| Pre-kickoff prep        | 2-3 days                              |
| Kickoff call            | Day 1 of engagement                   |
| Stage Definition        | Week 1-2                              |
| Criteria Alignment      | Week 2-3                              |
| Sign-Off                | Week 3-4 (when all definitions agreed)|

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything before proceeding to CRM build.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by VP Marketing AND VP Sales
- [ ] Stage architecture finalized (5-7 stages with clear entry criteria)
- [ ] Transition rules defined (which are automated, which are manual, which are time-based)
- [ ] Disqualification sub-reasons agreed
- [ ] Timestamp fields scoped (which stages get timestamps)
- [ ] MAP sync requirements documented (field mapping, sync direction)
- [ ] Dashboard requirements confirmed (conversion rates, velocity, volume, leakage)
- [ ] No blockers for engineering

#### Decision Point

- **Proceed to Engineering** -> Standard path for Lead Lifecycle projects. The strategic deliverable alone is not the end product.
- **Rare exit: Project complete** -> Only if customer realizes they need to resolve upstream issues first (e.g., CRM migration, data cleanup) before lifecycle implementation makes sense.

---

## Phase 2: Engineering

> **Goal:** Build and test the lead lifecycle system in the customer's CRM based on the approved strategic package.
>
> **Output:** Configured CRM with new lead status picklist, timestamp fields, automation rules, MAP sync, and funnel dashboards -- all tested and customer-approved.

| Project Type for Lead Lifecycle | Engineering Weight | Notes                                         |
| ------------------------------- | ------------------ | --------------------------------------------- |
| Balanced                        | Heavy (50-60%)     | CRM fields, automation, MAP sync, dashboards  |

### Sub-Phases

```
2a Tech Spec -> 2b Engineering Handoff -> 2c Build -> 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate the signed-off stage architecture into CRM-specific technical specifications.

**Input:** Signed-off Stage Architecture + Transition Rules Matrix + MAP Sync Requirements

**What happens:**

1. Receive strategic deliverables
2. Map each stage to CRM field values, API names, and automation triggers
3. Output draft technical specification

**Output:** Draft tech spec containing:

- **Lead Status Picklist Values:** Exact values with API-safe names (e.g., `Marketing_Qualified`, `Sales_Accepted`)
- **Timestamp Fields:** One date/time field per stage (e.g., `MQL_Date__c`, `SAL_Date__c`, `SQL_Date__c`)
- **Formula Fields:** Time-in-stage calculations (e.g., `Days_in_MQL__c = TODAY() - MQL_Date__c`)
- **Automation Rules:** For each transition -- trigger, conditions, actions, notifications
- **MAP Sync Mapping:** CRM field -> MAP field, sync direction (CRM-wins vs MAP-wins)
- **Dashboard Specs:** Reports needed (conversion funnel, velocity, volume by stage, leakage by disqualification reason)
- **Build Sequence:** What to build first (fields -> automation -> sync -> dashboards)

**Platform-specific notes:**

| Platform   | Status Field          | Automation Tool      | Timestamp Approach                  |
| ---------- | --------------------- | -------------------- | ----------------------------------- |
| Salesforce | Lead Status (standard)| Flow Builder         | Custom date/time fields + Flow      |
| HubSpot    | Lead Status (custom)  | Workflows            | Lifecycle Stage timestamps (native) |

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs before building. Catch issues before they become rework.

**Who attends:** Architect + Engineer (or RevOps admin doing the build)

**Agenda (30-45 min):**

| Time  | Topic              | What Happens                                                |
| ----- | ------------------ | ----------------------------------------------------------- |
| 0-15  | Walk through specs | Architect explains strategic context + tech spec output            |
| 15-30 | Engineer questions | Clarify field naming conventions, automation order, sandbox availability |
| 30-45 | Refine and approve | Adjust specs for platform-specific constraints, confirm build approach  |

**What Architect brings:**
- Signed-off Stage Architecture (strategic context)
- Draft tech spec (from 2a)
- Known risks: large lead volume could slow automation, existing rules that might conflict

**What engineer leaves with:**
- Approved tech spec with clear build sequence
- Sandbox access confirmed
- Known dependencies (MAP sync timing, existing automation to deactivate/modify)

---

### 2c. Build (Configure)

> **Purpose:** Configure the CRM with the approved lead lifecycle system.

**Input:** Approved tech spec from 2b

**Build sequence (order matters):**

**Step 1: Create/Update Lead Status Picklist**
- Create or update Lead Status picklist with approved values
- Add Lead Sub-Status field if using sub-status for disqualification reasons
- Deprecate old status values (create mapping for data migration of existing leads)
- Test field visibility across user profiles and page layouts

**Step 2: Create Timestamp Fields**
- Create date/time field for each stage: `MQL_Date__c`, `SAL_Date__c`, `SQL_Date__c`, `Disqualified_Date__c`
- Create formula fields for time-in-stage: `Days_in_MQL__c`, `Days_in_SAL__c`
- Consider "First Stage Hit" vs "Most Recent Stage Hit" distinction for recycled leads
- Document all field API names for reporting and integration use [2]

**Step 3: Build Automation Rules**
- Inbound lead creation rules (set initial status based on source)
- MQL qualification automation (form submission triggers, lead score threshold triggers)
- Timestamp population automation (stamp date on each stage change)
- Time-based rules (auto-disqualify after 90 days of inactivity -- configurable per client)
- Notification rules (alert assigned SDR on new MQL assignment)
- Reverse transition logic (Working -> Nurture if discovery cancelled)
- Test all automation paths with sample records in sandbox

**Step 4: Configure MAP Sync**
- Map CRM Lead Status field to MAP lifecycle stage field
- Configure sync direction per field (CRM-wins for status, MAP-wins for marketing engagement data)
- Set up sync filters to prevent bad data from syncing
- Test bidirectional sync with new leads and status changes
- Document sync logic for troubleshooting

**Step 5: Build Dashboards and Reports**
- Conversion rate report (MQL -> SAL -> SQL -> Opp -> CW)
- Velocity report (average days in each stage)
- Volume report (leads by stage over time, trended)
- Leakage report (disqualified leads by sub-reason)
- Executive dashboard combining key lifecycle KPIs
- Set up scheduled report delivery to leadership (weekly or monthly)

**Build tracking:**

- [ ] Lead Status picklist updated with new values
- [ ] Old status values deprecated/mapped
- [ ] Timestamp fields created for all stages
- [ ] Formula fields created for time-in-stage
- [ ] Automation: Inbound lead creation rules
- [ ] Automation: MQL qualification triggers
- [ ] Automation: Timestamp population
- [ ] Automation: Time-based disqualification
- [ ] Automation: Notifications on key transitions
- [ ] Automation: Reverse transitions
- [ ] MAP sync configured and tested
- [ ] Dashboards and reports built
- [ ] Scheduled report delivery configured

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify the lifecycle system works end-to-end before rollout.

**Two types of testing:**

| Type              | Who      | Purpose                                             |
| ----------------- | -------- | --------------------------------------------------- |
| Technical Testing | Our team | Verify fields, automation, sync, and dashboards work|
| Pilot Testing     | 2-3 reps | Validate usability with real leads in production    |

**Technical testing checklist:**

- [ ] All Lead Status picklist values visible and correct
- [ ] Timestamp fields populate on stage change (test each transition)
- [ ] Formula fields calculate correctly (time-in-stage)
- [ ] Automation rules fire in correct order (no conflicts with existing rules)
- [ ] MAP sync works bidirectionally without data conflicts
- [ ] Dashboards render correctly with test data
- [ ] Notifications fire on key transitions (new MQL assigned)
- [ ] Reverse transitions work (Working -> Nurture)
- [ ] Time-based rules trigger correctly (stale lead disqualification)
- [ ] Edge case: lead re-entering MQL after being Recycled -- timestamps handled correctly

**Pilot testing (50-100 leads, 2-3 reps, 1 week):**

- Select a mix of leads across various current stages
- Assign 2-3 reps to work pilot leads using new lifecycle
- Monitor for automation failures or unexpected behavior
- Gather rep feedback: Are stage definitions clear? Is anything confusing?
- Fix issues identified before full rollout

**Engineering sign-off checkpoint:**

- [ ] All technical tests passing in sandbox
- [ ] Pilot completed with issues resolved
- [ ] Customer has reviewed dashboards and confirmed they show what's needed
- [ ] Ready for full rollout and enablement

**Decision point:**

- **Proceed to Enablement** -> All tests pass, pilot validated, dashboards approved
- **Loop back to Build** -> Issues found, need fixes before rollout

---

## Phase 3: Enablement

> **Goal:** Sales, marketing, and RevOps teams can use the new lead lifecycle system and understand their responsibilities.
>
> **Output:** Trained teams with documentation, stabilized system, no critical issues.

### Sub-Phases

```
3a Training Prep -> 3b Training Sessions -> 3c Hypercare -> 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from the strategic and technical documentation.

**Input:** Stage Definition Document + Tech Spec + Built System + Dashboards

**What happens:**

1. Receive all project documentation
2. Generate draft training materials tailored to each audience
3. Architect reviews and refines

**Output:** Training package containing:

- **Sales Rep Quick-Reference 1-Pager:** Stage definitions, what's automated, what reps must update manually, when to disqualify
- **Marketing Guide:** MQL criteria, MAP sync behavior, how to monitor MQL volume and quality
- **Dashboard Walkthrough Script:** How to read conversion rates, velocity, volume, and leakage reports
- **FAQ Document:** Common scenarios (recycled leads, leads from partners, hand-off disputes, "my lead disappeared")
- **Video Scripts:** What to record for each audience

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge so teams adopt the new lifecycle on day one.

**Training schedule:**

| Session               | Audience                     | Focus                                                                       | Duration | Format         |
| --------------------- | ---------------------------- | --------------------------------------------------------------------------- | -------- | -------------- |
| Sales Team Training   | SDRs, AEs, Sales Managers    | Stage definitions, how to update status, what's automated, disqualification flow | 45 min   | Live + recorded|
| Marketing Team Training | Marketing Ops, Demand Gen  | MQL criteria, MAP sync, monitoring MQL quality, dashboard navigation         | 30 min   | Live + recorded|
| Leadership Briefing   | VP Sales, VP Marketing, RevOps | Dashboard walkthrough, how to interpret funnel metrics, action triggers      | 30 min   | Live + recorded|
| Technical Handoff     | RevOps Admin                 | Automation maintenance, field management, troubleshooting sync issues        | 60 min   | Live + recorded|

**Training delivery:**

1. Schedule sessions within the first week of go-live
2. Record all sessions for future onboarding
3. Distribute quick-reference 1-pager to all sales reps
4. Post FAQ in shared team wiki or CRM knowledge base

**Output:**

- Trained stakeholders across all roles
- Recordings for future hires
- Questions log from sessions (feeds into FAQ updates)

---

### 3c. Hypercare

> **Purpose:** Intensive post-launch support to catch issues fast and build confidence.

**Duration:** 2 weeks

**What happens:**

- Weekly 30-min office hours slot -- anyone can join with questions
- Slack/email support for bug reports and "how do I..." questions
- Monitor automation logs daily for the first week (catch failures early)
- Review dashboard data after first full week: Are conversion rates realistic? Any stages with 0% throughput?
- Fix issues as they surface

**Common hypercare issues for Lead Lifecycle:**

| Issue                                    | Resolution                                              |
| ---------------------------------------- | ------------------------------------------------------- |
| Reps not updating lead status manually   | Reinforce training, automate more transitions if possible|
| Timestamp not populating for one stage   | Check automation trigger conditions and execution order  |
| MAP sync creating duplicate records      | Review sync filters and deduplication rules              |
| Leads stuck in "New" status indefinitely | Add time-based automation to flag or reassign            |
| Dashboard showing unexpected numbers     | Verify report filters and date ranges                    |

**When to extend hypercare:** If automation failure rate exceeds 5% or rep adoption is below 70% after 2 weeks, extend by 1-2 weeks.

**Output:** Stabilized system, no critical issues outstanding, rep adoption confirmed

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm customer can operate the lead lifecycle independently.

**Validation checkpoint:**

- [ ] All training sessions delivered and recorded
- [ ] Quick-reference 1-pager distributed to all reps
- [ ] FAQ document delivered and accessible
- [ ] Hypercare period complete (2 weeks minimum)
- [ ] No critical automation issues outstanding
- [ ] Rep adoption above 80% (measured by lead status update frequency)
- [ ] Customer RevOps admin can troubleshoot basic issues independently
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** -> Customer is enabled, system stabilized
- **Extend Hypercare** -> Still unstable, needs more support time

---

## Phase 4: Handoff

> **Goal:** Clean project close with maintenance plan, ownership transfer, and retention path established.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the system, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule -> 4b Internal Handoff -> 4c External Handoff -> 4d Project Close
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At                                                                         |
| ----------------------------- | -------------------- | ------------------------------------------------------------------------------------- |
| **Single Project**            | Customer owns        | 4c (External Handoff) -- customer receives maintenance schedule and runs it themselves |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) -- Architect receives maintenance schedule and runs it for customer     |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention to keep the lead lifecycle healthy and accurate.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task                    | What to Check                                              | Red Flag Threshold                                  |
| ------------------------------- | ---------------------------------------------------------- | --------------------------------------------------- |
| Conversion Rate Review          | MQL->SAL, SAL->SQL, SQL->Opp rates vs baseline            | Any stage drops &gt;15% from baseline for 2+ months    |
| Stuck Lead Audit                | Leads in any stage for &gt;2x the average velocity            | &gt;10% of active leads are "stuck"                    |
| Data Quality Check              | Leads with blank status, missing timestamps, orphan records| &gt;5% of new leads have data quality issues            |
| Automation Health Check         | Review automation error logs for failed transitions         | Any automation failure rate &gt;2%                      |

**Quarterly Tasks:**

| Quarterly Task                  | What to Review                                             | Action if Off-Track                                 |
| ------------------------------- | ---------------------------------------------------------- | --------------------------------------------------- |
| Stage Definition Review         | Are MQL/SAL/SQL criteria still valid? Business changes?    | Convene VP Sales + VP Marketing to re-align         |
| Disqualification Reason Audit   | Top disqualification reasons -- any new patterns?          | Add new sub-reasons, adjust MQL criteria upstream    |
| Dashboard Relevance Check       | Are leadership using the dashboards? Any gaps?             | Add/modify reports based on stakeholder feedback     |
| MAP Sync Audit                  | Any sync errors accumulating? Data drift between systems?  | Re-validate field mapping and sync direction         |

**After First Business Cycle (60-90 days post-launch):**

- **Conversion Rate Baseline:** Establish baseline conversion rates for each stage transition. B2B SaaS companies should benchmark against: MQL->SQL conversion of 15-21% (median), SQL->Opportunity of 30-42%, Opportunity->Close of 20-39% depending on deal size [1][3].
- **Velocity Baseline:** Establish average time-in-stage for each lifecycle stage. Average B2B sales cycles now exceed 100 days end-to-end [4], but individual stage velocity varies significantly by company size and deal complexity.
- **Leakage Analysis:** Which disqualification reasons dominate? Are there upstream fixes possible?

**Refinement Triggers (when to re-engage):**

| Trigger                          | Threshold                           | Response                                                 |
| -------------------------------- | ----------------------------------- | -------------------------------------------------------- |
| Conversion rate collapse         | Any stage drops &gt;20% for 2+ months  | Re-engage SME to audit criteria and automation           |
| Stage definition disputes        | Sales/marketing disagreeing on MQL  | Scope definition re-alignment workshop                   |
| New product line or segment      | Company launches new ICP segment    | Scope lifecycle extension project (new stage criteria)   |
| CRM or MAP platform change       | Migrating systems                   | Scope re-implementation project                          |

**Every 6-12 Months:**

- Full lifecycle audit: Are all stages still relevant? Has the business model shifted?
- Benchmark conversion rates against industry: B2B SaaS median lead-to-customer conversion is approximately 2.9% [7]. Top performers with behavioral scoring achieve 39-40% MQL-to-SQL conversion [3].
- Evaluate whether lead scoring should be layered on top of lifecycle (natural expansion project)

---

### 4b. Internal Handoff

> **Purpose:** Transfer context so Architect can manage ongoing relationship.

**What the Architect needs to know:**

- Stage definitions and criteria (share the Definition Alignment Document)
- Which automations exist and what they do (share Automation Logic Reference)
- Common issues encountered during build (MAP sync quirks, data quality patterns)
- Dashboard locations and how to read them
- When to escalate back to SME
- **Maintenance schedule** (if Dedicated engagement -- Architect runs this)

**Escalation guidelines:**

| Issue Type                                      | Who Handles                      | Example                                        |
| ----------------------------------------------- | -------------------------------- | ---------------------------------------------- |
| Dashboard question, report filter change         | Architect                        | "Can we add a date filter to this report?"     |
| Rep training for new hire                        | Architect                        | Share recordings + 1-pager                     |
| Stage definition change request                  | SME                              | "We want to add a new stage between SAL and SQL"|
| Automation logic change                          | SME                              | "We need a different MQL trigger"              |
| MAP sync issues                                  | SME                              | "Lifecycle stages are out of sync"             |

**For Dedicated engagements:** Architect receives the maintenance schedule (4a) and becomes responsible for executing it. SME walks Architect through each maintenance task in a 30-min handoff session.

---

### 4c. External Handoff (LeanScale -> Customer)

> **Purpose:** Formal project completion with customer.

**Final project meeting (30-45 min):**

- Review what was delivered: stages, automation, dashboards, training
- Walk through documentation package
- Demo the maintenance tasks (show them what "monthly conversion rate review" looks like in practice)
- Confirm nothing outstanding
- Answer final questions
- Make it explicit: "Project complete. Here's who to call if you need us."
- **For Single Project engagements:** Walk customer through the maintenance schedule in detail. Record a video walkthrough.

**Documentation package:**

- Stage Definition Document (final version)
- Automation Logic Reference (what fires when, in what order)
- Dashboard Guide (how to read each report)
- All training recordings
- Quick-reference 1-pager for reps
- FAQ document
- Maintenance Schedule (monthly + quarterly tasks)
- Support contact info

**For Single Project engagements:** Record a video walkthrough of the maintenance schedule so the customer's RevOps admin can reference it.

**Output:** Customer owns the system. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location
- [ ] Handoff documentation complete
- [ ] Project status updated in tracking system

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell -> Downsell -> Retry  |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (retainer) -- "We handle ongoing lifecycle optimization"
   | if no
2. Downsell: Lead Scoring project -- natural next step after lifecycle
   OR: Marketing-to-Sales Handoff SLA project -- directly related
   | if yes
3. Retry retainer at end of next project cycle
```

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On \[date ~90 days out\], we'll review how the lifecycle is performing against the baselines we established and see if any adjustments are needed."

**At the refinement check-in:**

- Review conversion rates vs 60-day baseline
- Review velocity vs baseline
- Identify any stage definition changes needed
- If minor: Architect handles tweaks
- If major: Scope lead scoring or lifecycle refinement project

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- Stage Definition Document (5-7 stages with entry criteria, transition rules, disqualification sub-reasons)
- Definition Alignment Document (MQL, SAL, SQL, Disqualified definitions -- signed off)
- Current-State Process Map (visual flowchart of lead flow before and after)
- Transition Rules Matrix (automated vs manual triggers per stage change)

**Technical Deliverables:**

- CRM Lead Status picklist (configured with new values, old values deprecated)
- Timestamp fields for each stage (date/time + formula fields for velocity)
- Automation rules (stage transitions, notifications, time-based rules)
- MAP sync configuration (field mapping, sync direction, filters)
- Funnel dashboards (conversion rates, velocity, volume, leakage)
- Scheduled report delivery to leadership

**Documentation Package:**

- Training video recordings (sales, marketing, leadership, technical)
- Quick-reference 1-pager for reps
- Automation Logic Reference
- Dashboard Guide
- FAQ document
- Definition Alignment Document (final version)
- Maintenance Schedule (monthly + quarterly)

---

## Appendix

### What This Document Is

This is the implementation playbook for Lead Lifecycle -- the step-by-step execution guide an Architect follows to deliver a lead lifecycle project from first contact to project close. It is the third file in a 3-file playbook structure (Advisory, Methodology, Implementation).

### What Each Phase Produces

| Phase                    | Output                                                                 | Gate Criteria                                                                  |
| ------------------------ | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **Phase 1: Strategy**    | Signed-off Stage Architecture + Definition Alignment Document          | VP Marketing and VP Sales have approved stage definitions and transition rules |
| **Phase 2: Engineering** | Configured CRM with fields, automation, MAP sync, dashboards           | All automation tests pass, pilot validated, dashboards approved                |
| **Phase 3: Enablement**  | Trained teams with documentation                                       | All training delivered, hypercare complete, &gt;80% rep adoption                  |
| **Phase 4: Handoff**     | Independent customer + archived project                                | Internal/external handoffs complete, maintenance schedule in place             |

### Project Profile

Lead Lifecycle is a **Balanced** project:

| Project Profile | Strategy Weight | Engineering Weight | Enablement Weight | Notes                           |
| --------------- | --------------- | ------------------ | ----------------- | ------------------------------- |
| **Balanced**    | 30%             | 50%                | 20%               | Heavy engineering, standard enablement |

**Adaptation notes:**
- Phase 1 typically takes 3-4 meetings to align stage definitions
- Phase 2 is the heaviest phase -- CRM configuration, automation, MAP sync, and dashboards
- Phase 3 is standard -- training for sales, marketing, leadership, and technical admin
- Phase 4 always applies -- maintenance schedule is critical for ongoing lifecycle health

---

## References

[1] [2025 B2B SaaS Funnel Benchmarks & Pipeline Audit Framework - The Digital Bloom](https://thedigitalbloom.com/learn/pipeline-performance-benchmarks-2025/)

[2] [A Beginners Guide to Date Stamping in Salesforce - The Spot for Pardot](https://thespotforpardot.com/2020/03/01/a-beginners-guide-to-date-stamping-in-salesforce/)

[3] [MQL to SQL Conversion Rates: B2B SaaS Benchmarks - Understory](https://www.understoryagency.com/blog/mql-to-sql-conversion-rate-benchmarks)

[4] [Essential B2B Sales Funnel Metrics and KPIs - Lead Forensics](https://www.leadforensics.com/blog/b2b-sales-pipeline-metrics-the-essential-list/)

[5] [The Demand Waterfall: A Modular System - Forrester](https://go.forrester.com/blogs/demand-waterfall-modular-system/)

[6] [Salesforce Lead Status Best Practices - Iceberg RevOps](https://icebergops.com/how-to-manage-lead-status-in-salesforce/)

[7] [Lead Conversion Rate Statistics: Benchmarks & Industry Averages - Thunderbit](https://thunderbit.com/blog/lead-conversion-rate-statistics-benchmarks)
