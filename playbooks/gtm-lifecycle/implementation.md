# GTM Lifecycle — Implementation

> The end-to-end process for delivering GTM Lifecycle projects. Follows the 4-phase framework: Strategy, Engineering, Enablement, Handoff.

## Project One-Pager

### GTM Lifecycle One-Pager

#### Project Type

- Category: Strategic (with light engineering)
- Primary Deliverable: Unified lifecycle stage architecture with entry criteria, signed off by stakeholders and configured in CRM

##### Phase Relevance

| Phase          | Applies?  | Weight | Notes                                                                 |
| -------------- | --------- | ------ | --------------------------------------------------------------------- |
| 1. Strategy    | Yes       | Heavy  | 3-4 refinement loops to align stage definitions across all GTM teams  |
| 2. Engineering | Yes       | Light  | CRM field configuration, lifecycle stage setup, basic automation      |
| 3. Enablement  | Yes       | Light  | Training on new stage definitions, field usage, and dashboard reading |
| 4. Handoff     | Yes       | Light  | Maintenance cadence for stage definition governance                   |

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │    Heavy     │     │    Light     │     │    Light     │     │    Light     │
  │ 1a→1b→1c→1d │     │ 2a→2b→2c→2d │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   3-4 refinements      CRM config +         Stage training       Maintenance +
   ~60-70% of effort    automation           2-wk hypercare       governance
```

**This project's flow:**
- Full 4-phase. Heavy strategy (~60-70% of effort), light engineering (~15-20%), light enablement (~10-15%).
- Phase 1 is where 80% of the value is created: defining the shared stage language, aligning stakeholders across Marketing, Sales, CS, and RevOps.
- Phase 2 is CRM configuration only -- no custom code, no complex integrations.
- Some customers skip 3c Hypercare if the engineering build is minimal (e.g., only lifecycle stage fields and basic automation).

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Watch GTM Lifecycle intro video (5-10 min) -- explains what lifecycle stages are, why entry criteria matter, and what the project delivers
- [ ] Complete the Lifecycle Intake Form -- current CRM platform, number of GTM teams, current stage definitions (if any), known pain points
- [ ] Review the Definition Alignment Document -- pre-filled with LeanScale-recommended stage definitions for Lead, Sales, Customer, and optionally POC/POV stages

##### Track B: Architect Prep
- [ ] Pull current lifecycle stage data from CRM (Salesforce Lead Status, Opportunity Stages, HubSpot Lifecycle Stages, custom fields)
- [ ] Document current-state stage map: every lifecycle field, status field, and pipeline stage in use
- [ ] Build v0 lifecycle architecture showing recommended stages across all four domains (Lead, Sales, Customer, Company) with entry/exit criteria
- [ ] Flag misuse patterns: non-lifecycle concepts stored in lifecycle fields, overlapping status systems, missing handoff stages (e.g., no SAL)

#### Refinement Loop (1b → 1c → 1d)

| Meeting      | Sub-Phase | Focus                                                  | Stakeholder                         | Output                            |
| ------------ | --------- | ------------------------------------------------------ | ----------------------------------- | --------------------------------- |
| Kickoff      | 1b        | Present v0 lifecycle architecture, validate assumptions | VP RevOps + representatives from Sales, Marketing, CS | Corrections and info for v1       |
| Refinement 1 | 1c        | Review v1 stage definitions, align on entry criteria    | VP RevOps + department leads        | v2 with confirmed stage names     |
| Refinement 2 | 1c        | Finalize entry/exit criteria, resolve edge cases        | VP RevOps + CRM Admin               | v3 (near-final)                   |
| Sign-Off     | 1d        | Strategic approval of full lifecycle architecture       | All stakeholders                    | Final strategic package            |

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held
- [ ] 1c. Refinement loop complete (v0 → vFinal stage architecture)
- [ ] 1d. Strategic sign-off obtained from all department leads

##### Phase 2: Engineering
- [ ] 2a. Tech spec created (CRM field mapping, automation rules)
- [ ] 2b. Engineering handoff meeting held (Architect walks through specs with CRM admin)
- [ ] 2c. Build complete (lifecycle stages, pipelines, automation, dashboards)
- [ ] 2d. QA/Test + customer sign-off on CRM configuration

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped (video scripts, stage reference guide, FAQ)
- [ ] 3b. Training sessions delivered (leadership + technical)
- [ ] 3c. Hypercare period complete (if applicable -- 2 weeks for this project type)
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff complete
- [ ] 4c. External handoff (LeanScale → Customer) complete
- [ ] 4d. Project closed and archived

#### Document Types

##### Working Documents (iterate together)

| Document                       | Purpose                                    | When Complete                                   |
| ------------------------------ | ------------------------------------------ | ----------------------------------------------- |
| Lifecycle Intake Form          | Capture current state and known pain points | All fields filled by customer                   |
| Current State Audit            | Map every existing lifecycle field/stage    | All CRM objects audited, problems documented    |
| Stage Architecture Table       | Define recommended stages + entry criteria  | All stages named with entry/exit criteria       |

##### Deliverables (polished outputs)

| Deliverable                        | Created From                  | Customer Uses For                              |
| ---------------------------------- | ----------------------------- | ---------------------------------------------- |
| Lifecycle Architecture Diagram     | Stage Architecture Table      | Board/exec presentation, team alignment        |
| Definition Alignment Document      | Stage Architecture Table      | Cross-team reference for what each stage means |
| CRM Configuration Spec             | Stage Architecture Table      | CRM admin builds from this                     |
| Lifecycle Measurement Dashboard    | Measurement framework         | Ongoing funnel health monitoring               |

#### Enablement Details

##### Training Types

| Type       | Audience                                   | Focus                                              | Duration |
| ---------- | ------------------------------------------ | -------------------------------------------------- | -------- |
| Leadership | VP RevOps, VP Sales, VP Marketing, VP CS   | How to read lifecycle dashboards, what metrics mean | 30 min   |
| Technical  | RevOps, CRM Admin, Sales Ops               | How stages are configured, how to maintain fields   | 45 min   |
| End User   | SDRs, AEs, CSMs                            | How to update stages correctly, what entry criteria mean | 30 min   |

##### Hypercare
- Applies: Optional (only if engineering build includes automation)
- Duration: 2 weeks
- Office Hours: Weekly 30-min slot for first 2 weeks post-launch

##### Training Assets to Create
- [ ] Video walkthrough: Lifecycle architecture walkthrough (what the stages are, why they matter)
- [ ] Video walkthrough: CRM field usage guide (how to update lifecycle stages correctly)
- [ ] Video walkthrough: Dashboard interpretation guide (how to read funnel conversion reports)
- [ ] Doc: Stage definition reference card (one-page PDF with all stages and entry criteria)
- [ ] Doc: FAQ document (common questions from past lifecycle projects)

#### Handoff & Retention

##### Internal Handoff
- Key context for Architect: Which stages were customized vs standard, any edge cases discussed, stakeholder dynamics
- Escalation trigger: Any request to add new stages, change entry criteria, or restructure pipelines

##### External Handoff (LeanScale → Customer)
- Final meeting agenda: Review lifecycle architecture, walk through maintenance schedule, record maintenance video walkthrough
- Documentation package: All video recordings, stage reference card, Definition Alignment Doc (final), CRM Configuration Spec, FAQ

##### Maintenance Schedule
- Monthly: Check stage conversion rates for drift, verify no new rogue stages created
- Quarterly: Full lifecycle stage review with RevOps lead

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services → if no → Downsell: Lead Scoring, Attribution, or Sales Stages depth project → Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~1 quarter out
- Internal prep trigger: 2 weeks before
- Decision: Architect handles / specialist needed (stage changes = specialist needed)

#### Key Assets

| Asset                           | When Used                   |
| ------------------------------- | --------------------------- |
| GTM Lifecycle Intro Video       | Pre-Kickoff (Track A)       |
| Lifecycle Intake Form           | Pre-Kickoff (Track A)       |
| Definition Alignment Template   | Pre-Kickoff + all meetings  |
| Current State Audit Template    | Pre-Kickoff (Track B)       |
| Stage Architecture Template     | Strategy refinement loop    |
| CRM Config Spec Template        | Phase 2a Tech Spec          |

#### Definition Alignment Terms

| Term                      | Typical Definition                                                                                                      |
| ------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| Anonymous Visitor         | A website visitor who has not provided identifiable information                                                          |
| Known Lead                | Any contact in the database with an email, phone, or name -- no engagement required                                     |
| Marketing Engaged Lead    | A lead engaging with content (downloads, webinars, video views) but not requesting sales contact                        |
| MQL (Marketing Qualified) | The handoff point from Marketing to Sales. Qualified based on ICP fit and intent level (scoring threshold or hand-raise) |
| SAL (Sales Accepted Lead) | Sales has received the MQL and agreed to work it. Not yet qualified -- just accepted for outreach                       |
| SQL (Sales Qualified Lead)| Stage 0 opportunity. Discovery call scheduled or completed. Pipeline creation point.                                    |
| SAO (Sales Accepted Opp)  | Stage 1 opportunity. Discovery/demo occurred, prospect meets qualification criteria (e.g., BANT). Pipeline value assigned.|
| Evaluation / Use Case     | Stage 2 opportunity. Evaluation kicked off to prove value based on expected use case                                     |
| Proposal / Negotiation    | Stage 3 opportunity. Proposal sent, terms under negotiation                                                              |
| Closed Won                | Prospect agreed to terms and signed a contract                                                                           |
| Pre-Onboarding            | CS engagement before closed-won: intro, implementation planning, onboarding prep                                         |
| Onboarding                | Post-closed-won: customer introduced to CSM, roadmap outlined, success criteria defined                                  |
| Implementation            | Technical or process-oriented work to connect, integrate, and set up product                                             |
| Early Adoption            | First time to value (FTV) achieved. Customer getting results and operating independently                                 |
| Mature Adoption           | Customer fully proficient, getting maximum value, churn risk extremely low                                               |
| First Time to Value (FTV) | The point where a customer first realizes actual value from the product -- the goal of onboarding + implementation        |
| Golden Stages             | SQL, Closed Won, and Early Adoption -- the three most critical transition points in the lifecycle                         |
| Entry Criteria             | Objective benchmarks that determine when a record moves from one stage to the next                                       |
| Contact Status             | The current working state of a contact (New, Working, Engaged, Nurture) -- distinct from lifecycle stage                 |
| Lifecycle vs Status        | Lifecycle = funnel position (where they are in the journey). Status = working state (what's happening now)               |

#### Common Gotchas
- **Naming stages as activities instead of completed milestones** → Use past-tense: "Demo Completed" not "Demo"
- **Mixing lifecycle and status concepts in one field** → Keep lifecycle stages (funnel position) and contact statuses (working state) as separate fields
- **Putting deal outcomes (Won/Lost) in lifecycle stages** → Lifecycle tracks forward progression; deal outcomes go in the deal pipeline
- **Putting CS stages in Sales pipelines** → Use a dedicated CS pipeline (Tickets in HubSpot, custom object in Salesforce) to separate customer health from revenue forecasting
- **Using time-based renewal stages (120/90/60/30-day)** → Replace with commercial progression stages reflecting customer intent
- **Not defining entry criteria before building in CRM** → Define every stage's entry/exit criteria on paper first, get sign-off, then build
- **Using generic stages that don't match the business's actual process** → Customize stages to reflect the company's real sales/CS motion
- **Skipping SAL stage** → Without SAL, you cannot measure Marketing-to-Sales handoff speed or acceptance rate
- **Averaging metrics without segmentation** → Break lifecycle metrics by segment, region, and individual contributor to surface hidden problems

#### Methodology Options (if applicable)

| Option                     | When to Use                                                      | Complexity |
| -------------------------- | ---------------------------------------------------------------- | ---------- |
| Foundation Only            | $0-5M company, no existing lifecycle, small team (&lt;15 people)    | Low        |
| Foundation + Single Depth  | $5M+ company, has basic lifecycle but one area is broken         | Medium     |
| Foundation + All Depth     | $10M+ company, complete overhaul, separate Marketing/Sales/CS teams | High   |
| Reunification              | Post-merger or re-org, teams use different stage definitions     | Medium     |

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on the unified lifecycle stage architecture.
>
> **Output:** Signed-off Definition Alignment Document + Lifecycle Architecture (stage names, entry/exit criteria for all domains).

### 1a. Pre-Kickoff

> Two parallel tracks run after the deal closes and before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                              | Format             |
| ----------------------------- | -------------------------------------------------------------------- | ------------------ |
| GTM Lifecycle intro video     | Explain what lifecycle stages are, why entry criteria matter, what Golden Stages are | Video walkthrough (5-10 min)    |
| Definition Alignment Document | Pre-filled with LeanScale-recommended definitions for all lifecycle stages | Google Doc         |
| Lifecycle Intake Form         | Capture current CRM, team structure, existing stage definitions, known pain points | Google Form or Doc |

**GTM Lifecycle intro video covers:**
- What the GTM lifecycle is (spans marketing through renewal, not just sales stages)
- Why entry criteria matter (accurate reporting, data-driven decisions, team alignment)
- The Golden Stages concept: SQL, Closed Won, and Early Adoption as the three most critical transition points
- What the project delivers: a shared stage language with defined handoff points

**Definition Alignment Document includes pre-filled definitions for:**
- Lead stages: Anonymous Visitor, Known Lead, Marketing Engaged, MQL, SAL, SQL
- Sales stages: SQL, SAO, Evaluation/Use Case, Proposal/Negotiation, Closed Won
- Customer stages: Pre-Onboarding, Onboarding, Implementation, Early Adoption, Mature Adoption
- (If applicable) POC/POV stages: POC Entry, Operational Steps (2-3), Value Assessment
- (If applicable) Renewal stages: Open Renewal, Review, Proposal, Negotiation, Closed Won/Lost

**Lifecycle Intake Form captures:**
- CRM platform (Salesforce, HubSpot, other)
- Number of GTM teams and their sizes
- Current lifecycle stage definitions (screenshot or export)
- Current pipeline names and stages
- Known pain points with current tracking
- Whether they have a POC/POV process
- Whether they have a formal renewal process
- Lead scoring: none, action-based, simple scoring, or matrix scoring

**Completion tracking:** Architect follows up. Don't cancel kickoff if intake is incomplete, but push hard. Intake data is essential for Track B quality.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                         | Output                                           |
| ---- | -------------------------------------------------------------- | ------------------------------------------------ |
| 1    | Pull current CRM lifecycle data (all lifecycle/status fields, pipeline stages, custom fields) | Raw data export from CRM                         |
| 2    | Run Current State Audit: map every lifecycle-related field across Lead, Contact, Opportunity, Account, and (if applicable) Ticket objects | Current State Audit document                     |
| 3    | Document problems ("Notes on Current State"): overlapping systems, missing stages (no SAL?), non-lifecycle concepts in lifecycle fields (deal outcomes, time-based stages), inconsistent naming | Problem list per domain                          |
| 4    | Build v0 lifecycle architecture: recommended stages across Lead, Sales, Customer, and Company domains, with entry/exit criteria | v0 Stage Architecture Table (all items marked ASSUMED) |
| 5    | Create kickoff assets: architecture diagram, current vs recommended comparison, questions list | Presentation-ready materials                     |

**Current State Audit pattern:**

The audit follows a repeatable four-domain structure:

1. **Lead/Contact Lifecycle** -- Map all lead status fields, contact lifecycle stages, and any lead pipeline stages. Look for: overlapping systems (e.g., Lead Pipeline + Contact Lifecycle + Lead Status all tracking similar concepts), missing SAL stage, deal outcomes stored in lifecycle stages.

2. **Sales Pipelines** -- Map all deal pipelines and their stages. Look for: too many pipelines (consolidate to 3 max: New Business, Renewal, Expansion), time-based stages (120/90/60/30-day renewal countdowns), internal signal stages (Trending Up/Down), task-level stages (50%/75%/90% complete).

3. **Customer Lifecycle** -- Map all post-sale tracking systems. Look for: CS stages inside Sales pipelines, fragmented tracking across multiple objects, no defined customer lifecycle stages at all (lifecycle ending at Closed Won).

4. **Company Lifecycle** -- Map all company-level fields. Look for: company fields mixing lifecycle, type, and status concepts.

**v0 Architecture includes:**
- Recommended stage names for all four domains
- Entry criteria for each stage (what triggers entry)
- Exit criteria for each stage (what triggers advancement, and where the record goes)
- Identification of Golden Stages (SQL, Closed Won, Early Adoption)
- Notes on which stages are standard vs may need customization

**Critical:** Mark everything as ASSUMED. The kickoff call validates.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building anything in CRM.

| Term                     | Our Definition                                                                  | Internally Approved? |
| ------------------------ | ------------------------------------------------------------------------------- | -------------------- |
| MQL                      | The handoff point from Marketing to Sales. Qualified based on ICP fit + intent. | [ ] Yes / [ ] No     |
| SAL                      | Sales has accepted the MQL and agreed to work it. Not yet qualified.            | [ ] Yes / [ ] No     |
| SQL                      | Discovery call scheduled/completed. Pipeline creation point.                    | [ ] Yes / [ ] No     |
| SAO                      | Discovery/demo occurred, prospect meets qualification criteria. Pipeline value assigned. | [ ] Yes / [ ] No     |
| Closed Won               | Contract signed.                                                                | [ ] Yes / [ ] No     |
| Early Adoption           | Customer has achieved first time to value.                                       | [ ] Yes / [ ] No     |
| Mature Adoption          | Customer fully proficient, maximum value, low churn risk.                        | [ ] Yes / [ ] No     |
| First Time to Value      | The specific milestone that means the customer has realized value.               | [ ] Yes / [ ] No     |
| Entry Criteria           | Objective benchmarks for stage transitions.                                      | [ ] Yes / [ ] No     |
| Contact Status vs Stage  | Status = working state; Lifecycle = funnel position.                             | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your leadership team across Marketing, Sales, CS, and RevOps. Check "Yes" when approved. We cannot proceed to CRM configuration until all terms are aligned. Disagreements on definitions are normal -- that's what the refinement meetings are for.

---

### 1b. Kickoff Call

> **Purpose:** Present v0 lifecycle architecture and get alignment. We walk in with work done -- customer reacts, not creates from scratch.

#### Agenda (60-75 min)

| Time  | Topic                             | What Happens                                                      |
| ----- | --------------------------------- | ----------------------------------------------------------------- |
| 0-20  | Walk through current state audit  | "Here's what we found in your CRM -- these are your current stages, and here's where we see problems" |
| 20-35 | Present v0 lifecycle architecture | "Here's what we recommend -- these are the stages, here are the entry criteria" |
| 35-50 | Validate assumptions              | ASSUMED → CONFIRMED or corrected. Focus on biggest disagreements first. |
| 50-60 | Review Definition Alignment Doc   | Get initial reactions on the terms. Mark any that need discussion. |
| 60-75 | Next steps                        | Schedule refinement meetings, assign homework (e.g., "Get VP Sales to confirm SAO definition") |

#### What We Bring

- Current State Audit (the problems we found)
- v0 Lifecycle Architecture (our recommendations)
- Lifecycle architecture diagram (visual of the full lifecycle)
- Current state vs recommended state comparison table
- Definition Alignment Document (pre-filled with our recommendations)
- Questions list (what we need to validate)

#### What We Leave With

- Corrections and feedback on v0 (info needed to create v1)
- Initial positions on contested definitions (especially MQL, SAL, and what "Early Adoption" means)
- Clear homework assignments: "VP Sales needs to approve SAO definition," "CS lead needs to define what First Time to Value means for your product"
- Refinement meeting 1 scheduled

---

### 1c. Alignment Loop &amp; Strategic Meeting Cadence

> **Purpose:** Iterate on the lifecycle architecture until all stages and entry criteria are signed off.

#### The Pattern

```
Kickoff Call (present current state + v0, gather corrections)
    |
Process feedback --> v1
    |
Refinement 1 (present v1, focus on Marketing/Sales handoff definitions) --> v2
    |
Refinement 2 (present v2, focus on edge cases and remaining ASSUMED items) --> v3
    |
Final Review --> Sign-off
```

#### Before Each Meeting

1. Process previous meeting notes/transcript
2. Update lifecycle architecture (v\[n-1\] → v\[n\])
3. Mark items that moved from ASSUMED → CONFIRMED
4. Prepare questions for next validation round
5. Identify remaining ASSUMED items that need specific stakeholder input

#### During Each Meeting

1. Walk through current version -- focus on what changed since last meeting
2. Capture corrections and refinements
3. Validate what's now CONFIRMED
4. Address edge cases: "What happens when a customer churns and comes back?" "What about multi-product lifecycle recycling?" "What if you have a PLG motion alongside sales-led?"

#### After Each Meeting

1. Produce next version
2. Track what moved from ASSUMED → CONFIRMED
3. Update Definition Alignment Document

#### GTM Lifecycle Meeting Structure

| Meeting      | Focus                                                    | Key Stakeholder                | Output         |
| ------------ | -------------------------------------------------------- | ------------------------------ | -------------- |
| Kickoff      | Current state audit, v0 presentation, initial alignment  | VP RevOps + all department reps| Info for v1    |
| Refinement 1 | Lead + Sales stage definitions, MQL/SAL/SQL alignment    | VP RevOps, VP Marketing, VP Sales | v2          |
| Refinement 2 | Customer lifecycle stages, edge cases, measurement plan  | VP RevOps, VP CS, CRM Admin   | v3 (near-final)|
| Final Review | Full lifecycle walkthrough, sign-off                     | All stakeholders               | Signed-off architecture |

**Note:** Meetings are organized by topic, not strict sequence. If VP Sales is available for Refinement 1 and VP CS is not available until next week, run them separately. Multiple sessions can happen the same day. Timeline compresses with stakeholder urgency and availability.

#### Typical Timeline

| Milestone               | Timing                                           |
| ----------------------- | ------------------------------------------------ |
| Pre-kickoff prep        | 2-3 days                                         |
| Kickoff call            | Day 1 of engagement                              |
| Refinement loop         | 1-2 weeks (depends on stakeholder availability)  |
| Final review + sign-off | When all definitions CONFIRMED                   |
| Total Phase 1           | ~2-3 weeks                                       |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything before proceeding to CRM configuration (or completing the project if strategy-only).

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by VP RevOps, VP Marketing, VP Sales, VP CS
- [ ] All lifecycle stages named with entry/exit criteria documented
- [ ] Current state vs future state comparison reviewed and accepted
- [ ] Golden Stages (SQL, Closed Won, Early Adoption) defined with specific criteria for this business
- [ ] Contact Status vs Lifecycle Stage separation agreed upon
- [ ] Measurement framework agreed (which of the 6 metric categories to prioritize)
- [ ] Edge cases addressed: multi-product lifecycle recycling, churned customer re-activation, PLG motion handling
- [ ] No blockers for CRM configuration

#### Decision Point

- **Proceed to Engineering** → Customer wants lifecycle stages configured in CRM, automation built, dashboards created
- **Project complete** → Strategic deliverable (lifecycle architecture + Definition Alignment Doc) is the end product

> **GTM Lifecycle can complete after Phase 1.** For $0-5M companies with a small RevOps team, the lifecycle architecture document itself may be the primary deliverable. Their CRM admin can configure it themselves using the spec. For $5M+ companies, Phase 2 configuration is typical.

---

## Phase 2: Engineering

> **Goal:** Configure lifecycle stages, pipelines, automation, and reporting in the customer's CRM based on the signed-off lifecycle architecture.
>
> **Output:** CRM configured with correct lifecycle stages, automated stage transitions, and a lifecycle measurement dashboard.

| Project Type    | Engineering Weight | This Project                                          |
| --------------- | ------------------ | ----------------------------------------------------- |
| Strategic-heavy | Light (10-20%)     | GTM Lifecycle -- mostly strategy, light CRM config    |
| Balanced        | Medium (40-60%)    | N/A for this project                                  |
| Technical-heavy | Heavy (70-90%)     | N/A for this project                                  |

### Sub-Phases

```
2a Tech Spec --> 2b Engineering Handoff --> 2c Build --> 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate the signed-off lifecycle architecture into CRM-specific configuration instructions.

**Input:** Signed-off lifecycle architecture + Definition Alignment Document from Phase 1

**What happens:**

1. Architect translates strategic stage definitions into CRM-specific field specifications
2. Maps each lifecycle stage to the correct CRM object and field
3. Documents automation rules for stage transitions
4. Defines dashboard/report specifications

**Output:** CRM Configuration Spec containing:

**For Salesforce:**
- Lead Status picklist values (add/remove/rename to match lifecycle stages)
- Opportunity Stage picklist values with probability percentages (25%/50%/75%/90%/100%)
- Custom Contact Lifecycle Stage field (if using Contact-based model)
- Account-level lifecycle field (rolls up from Contact activity)
- Validation rules for entry criteria (e.g., "Cannot move to SQL without an Opportunity record")
- Flow/Process Builder automation for stage transitions (e.g., "When Opportunity created, set Contact Lifecycle to Opportunity")
- Report types and dashboards for lifecycle measurement

**For HubSpot:**
- Lifecycle Stage property configuration (custom stages if needed -- requires Enterprise tier)
- Lead Status property values
- Deal Pipeline stages for each pipeline (New Business, Renewal, Expansion)
- Workflow automation for lifecycle stage progression
- Contact-to-Company lifecycle sync rules
- Dashboard and report specifications
- Important: Disable HubSpot's native lifecycle automation before configuring custom rules (Settings → Objects → Contacts → Lifecycle Stage)

**For both platforms:**
- Automation rule: When deal moves to Closed Won, set Contact Lifecycle to Customer
- Automation rule: When meeting booked, set Contact Lifecycle to SAL (if not already SQL or higher)
- Automation rule: When deal created, set Contact Lifecycle to Opportunity
- Automation rule: Company lifecycle rolls up from most advanced Contact lifecycle stage

---

### 2b. Engineering Handoff

> **Purpose:** Review CRM configuration specs with whoever will build it.

**Who attends:** Architect + CRM Admin (or RevOps engineer)

**Agenda (30 min):**

| Time  | Topic                 | What Happens                                               |
| ----- | --------------------- | ---------------------------------------------------------- |
| 0-10  | Walk through specs    | Architect explains lifecycle architecture + CRM mapping           |
| 10-20 | Admin questions       | Clarify: field types, automation triggers, edge cases      |
| 20-30 | Agree on build order  | What to build first (lifecycle fields before automation)   |

**Build order recommendation:**
1. Create/update lifecycle stage field values (add new stages, rename, remove deprecated)
2. Create/update pipeline stages (if applicable)
3. Build automation rules for stage transitions
4. Build dashboards and reports
5. Test with sample records

---

### 2c. Build (Configure)

> **Purpose:** Configure lifecycle stages, automation, and reporting in the customer's CRM.

**Input:** Approved CRM Configuration Spec from 2b

**Build components for GTM Lifecycle:**

| Component                        | What to Build                                                          | CRM Object             |
| -------------------------------- | ---------------------------------------------------------------------- | ---------------------- |
| Lead/Contact Lifecycle Stages    | Add/rename/remove stages to match architecture                        | Lead, Contact          |
| Sales Pipeline Stages            | Configure deal stages with weightings and entry criteria              | Opportunity/Deal       |
| Customer Lifecycle Stages        | Configure post-sale stages (if using CS pipeline)                     | Custom Object/Ticket   |
| Company Lifecycle                | Add company-level lifecycle field that rolls up from Contact activity  | Account/Company        |
| Stage Transition Automation      | Workflows/Flows for automatic stage advancement                       | Cross-object           |
| Lifecycle Measurement Dashboard  | Reports for production by stage, conversion rates, time in stage      | Reporting              |
| Drop-off Reason Fields           | Picklist fields for documenting why records don't advance             | Lead, Opportunity      |

**Execution approach:** Manual build for this project type. GTM Lifecycle CRM configuration is straightforward enough for a CRM admin to build from the spec. No custom code required.

**Build tracking:**

- [ ] Lead/Contact lifecycle stage values configured
- [ ] Sales pipeline stages configured (with probability weights)
- [ ] Customer lifecycle stages configured (if applicable)
- [ ] Company lifecycle field configured
- [ ] Automation rules for stage transitions built and activated
- [ ] Drop-off reason picklist fields created
- [ ] Lifecycle measurement dashboard built
- [ ] Contact Status field configured (separate from Lifecycle Stage)

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify the CRM configuration works and get customer approval.

**Technical testing checklist:**

- [ ] All lifecycle stage values appear correctly in the CRM
- [ ] Stage transitions fire correctly (test: create a lead, advance through stages, verify automation works)
- [ ] Lifecycle cannot move backward accidentally (if using forward-only model)
- [ ] Contact-to-Company lifecycle sync works (most advanced contact dictates company stage)
- [ ] Pipeline stages have correct probability weightings
- [ ] Dashboard shows accurate data (create test records, verify they appear in reports)
- [ ] Drop-off reason fields appear and are required when moving to disqualified/lost stages
- [ ] No conflicts with existing automation (check for legacy workflows that might override new rules)
- [ ] Edge cases: what happens when a churned customer re-engages? Does the lifecycle handle multi-product correctly?

**Customer testing:**

- Walk customer's RevOps/CRM admin through the full configuration
- Have them create a test record and advance it through stages
- Show them the lifecycle measurement dashboard
- Capture feedback, fix issues

**Engineering sign-off checkpoint:**

- [ ] CRM configuration matches the approved lifecycle architecture
- [ ] All automation rules firing correctly
- [ ] Customer RevOps/admin has tested and approved
- [ ] Dashboard data is accurate
- [ ] Ready for enablement

---

## Phase 3: Enablement

> **Goal:** Customer team can use the new lifecycle stages correctly and read the measurement dashboards.
>
> **Output:** Trained team with documentation. Everyone knows what each stage means, how to update stages, and how to interpret the reports.

### Sub-Phases

```
3a Training Prep --> 3b Training Sessions --> 3c Hypercare --> 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from the lifecycle architecture and CRM configuration.

**Input:** Signed-off lifecycle architecture + CRM Configuration Spec + configured system

**Output:** Training package containing:

- **Video walkthrough: "What Are Our Lifecycle Stages?"** -- walks through the full lifecycle architecture, explains what each stage means, why the Golden Stages matter
- **Video walkthrough: "How to Update Stages in CRM"** -- screen recording of how to update lifecycle stages correctly, what entry criteria to check before advancing
- **Video walkthrough: "Reading the Lifecycle Dashboard"** -- explains each report: production by stage, conversion rates, time in stage, drop-off reasons, cost per stage
- **Stage Reference Card** -- one-page PDF with all stages, entry criteria, and who owns each transition
- **FAQ document** -- common questions:
  - "What's the difference between SAL and SQL?"
  - "When exactly do I move a lead to MQL?"
  - "What does 'First Time to Value' mean for our product?"
  - "How do I record a drop-off reason?"
  - "What if a customer churns and then comes back?"

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to customer team so everyone uses lifecycle stages consistently.

**Three types of training for GTM Lifecycle:**

| Type        | Audience                                    | Focus                                                              | Duration |
| ----------- | ------------------------------------------- | ------------------------------------------------------------------ | -------- |
| Leadership  | VP RevOps, VP Sales, VP Marketing, VP CS    | How to read lifecycle dashboards, what conversion rate changes mean, when to act | 30 min   |
| Technical   | RevOps, CRM Admin                           | How stages are configured, how automation works, how to add/modify stages, how to troubleshoot | 45 min   |
| End User    | SDRs, AEs, CSMs                             | How to update stages correctly, what entry criteria mean, how to record drop-off reasons | 30 min   |

**Leadership training covers:**
- The 6-metric measurement framework: production by stage, stage conversion, time in stage, drop-off reasons, cost to enter stage, segmentation
- How to read the lifecycle dashboard
- What red flags to look for (conversion rate drops, stage duration increases)
- When to trigger a lifecycle review

**Technical training covers:**
- Where lifecycle stages live in the CRM (which objects, which fields)
- How automation rules work (what triggers stage advancement)
- How to add a new stage or modify entry criteria
- How to troubleshoot: "Why didn't this record advance automatically?"
- How to run lifecycle reports

**End User training covers:**
- What each stage means (the "when do I move this?" question)
- How to check entry criteria before advancing a record
- How to record drop-off reasons when a record doesn't advance
- What NOT to do: don't skip stages, don't move records backward, don't use lifecycle stage as a status tracker

**Training delivery:**
1. Schedule sessions with appropriate stakeholders
2. Deliver live training (or pre-record if team is distributed)
3. Record all sessions as video walkthroughs for future onboarding
4. Collect questions -- feed into FAQ document

---

### 3c. Hypercare

> **Purpose:** Light-touch post-launch support to catch issues early.

**Duration:** 2 weeks (GTM Lifecycle is a light-engineering project, so hypercare is brief)

**What happens:**
- Weekly 30-min office hours slot for first 2 weeks
- Support for quick questions
- Monitor: are teams using the new stages correctly? Are automation rules firing?
- Fix any bugs found (wrong automation trigger, missing picklist value)

**When to skip:** If the project was strategy-only (no Phase 2 engineering), hypercare is unnecessary. Customer is just using the Definition Alignment Document as a reference.

**Output:** Stabilized system, no critical issues, teams using stages correctly.

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm customer can operate independently.

**Validation checkpoint:**

- [ ] All three training sessions delivered (leadership, technical, end user)
- [ ] Training video walkthroughs recorded and shared
- [ ] Stage Reference Card delivered
- [ ] FAQ document delivered
- [ ] Hypercare period complete (if applicable)
- [ ] No critical issues outstanding
- [ ] Teams are updating lifecycle stages correctly (spot-check CRM data)
- [ ] Ready for handoff

---

## Phase 4: Handoff

> **Goal:** Clean project close with maintenance plan for ongoing lifecycle governance.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the lifecycle system, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule --> 4b Internal Handoff --> 4c External Handoff --> 4d Project Close
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At                                                                         |
| ----------------------------- | -------------------- | ------------------------------------------------------------------------------------- |
| **Single Project**            | Customer owns        | 4c (External Handoff) -- customer receives maintenance schedule and runs it themselves |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) -- Architect receives maintenance schedule and runs it for customer     |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention to prevent lifecycle stage drift and keep definitions current.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task                    | What to Check                                              | Red Flag Threshold                                |
| ------------------------------- | ---------------------------------------------------------- | ------------------------------------------------- |
| Stage Conversion Rate Check     | MQL→SAL, SAL→SQL, SQL→Opp, Opp→CW conversion rates | Any rate drops &gt;5 percentage points from baseline |
| Production by Stage Volume      | Volume of records entering each stage this month           | Any stage volume drops &gt;20% without explanation   |
| Rogue Stage Audit               | Check if anyone has created new picklist values or custom stages without approval | Any new values found = governance issue            |
| Drop-off Reason Review          | Top 3 reasons records are not advancing at each stage      | Same reason appearing &gt;30% of the time            |

**Quarterly Tasks:**

| Quarterly Task                     | What to Review                                    | Action if Off-Track                               |
| ---------------------------------- | ------------------------------------------------- | ------------------------------------------------- |
| Full Lifecycle Stage Review        | Are all stage definitions still accurate? Do entry criteria need updating? | Schedule refinement session with RevOps lead       |
| Time in Stage Analysis             | Average days between stages -- has velocity changed? | Investigate bottleneck stages                     |
| Cost to Enter Stage Review         | Is cost per MQL, SQL, CW trending up?              | Review marketing spend efficiency                 |
| Segmentation Deep Dive             | Break all metrics by segment, region, rep          | Identify underperforming segments for targeted action |
| Definition Alignment Check         | Ask department leads: "Are these definitions still correct?" | Update Definition Alignment Doc if anything changed |

**After First Business Cycle (30-60 days post-launch):**

- **Stage Adoption Check:** Are all teams actually using the new lifecycle stages? Pull CRM data to verify. Look for: records stuck in old stages, records with no stage assigned, stages being skipped.
- **Conversion Rate Baseline:** Establish baseline conversion rates for each stage transition. These become the benchmarks for monthly monitoring.
- **Key Question:** Are the entry criteria working in practice, or are teams finding them too strict/too loose?

**Refinement Triggers (when to re-engage):**

| Trigger                                       | Threshold                          | Response                                                 |
| --------------------------------------------- | ---------------------------------- | -------------------------------------------------------- |
| Conversion rate decline                       | &gt;10% drop sustained for 2+ months | Review stage definitions and entry criteria              |
| New GTM motion added (e.g., PLG, partner)     | Any new motion launched            | Add lifecycle stages for new motion, update architecture |
| Team restructure (Marketing/Sales/CS re-org)  | Any re-org affecting stage ownership | Re-validate handoff definitions (MQL, SAL, SQL owners)   |
| CRM migration                                 | Moving platforms                   | Full lifecycle re-implementation required                |
| Stage definitions contested by stakeholders   | Any stakeholder disagreement       | Schedule definition alignment session                    |

**Every 6-12 Months:**

- **Full Lifecycle Architecture Review:** Walk through the entire lifecycle from lead to mature adoption. Are all stages still relevant? Have new stages emerged that need to be formalized?
- **Benchmark Comparison:** Compare current conversion rates against initial baselines. Typical B2B SaaS benchmarks: MQL-to-SQL 13-21% (average), top performers hit 39-40% with behavioral scoring.
- **Cross-Team Alignment Check:** Bring department leads together to confirm definitions are still shared. Drift happens naturally as teams evolve.

---

### 4b. Internal Handoff

> **Purpose:** Transfer context so Architect can manage ongoing lifecycle governance.

**What the Architect needs to know:**

- What lifecycle architecture was built and why (any customizations from LeanScale standard)
- Customer context: which stakeholders were hardest to align, any ongoing disagreements, political dynamics around stage definitions
- Common issues for this customer: "Marketing and Sales disagree on when MQL becomes SAL -- watch for this resurfacing"
- The measurement framework: which of the 6 metric categories this customer prioritizes
- Maintenance schedule: what to check monthly and quarterly

**Escalation guidelines:**

| Issue Type                                          | Who Handles                    |
| --------------------------------------------------- | ------------------------------ |
| Questions about what a stage means                  | Architect (point to Definition doc)   |
| Adding a new picklist value to an existing stage    | Architect (simple CRM change)         |
| Adding a new lifecycle stage                        | Specialist (requires architecture review) |
| Changing entry criteria for a stage                 | Specialist (requires stakeholder alignment) |
| Restructuring pipelines (e.g., adding Expansion pipeline) | Specialist (significant scope)       |
| Conversion rates dropping significantly             | Specialist (diagnostic work needed)   |

**For Dedicated engagements:** Architect also receives the maintenance schedule (4a) and becomes responsible for executing monthly and quarterly checks. The specialist walks Architect through each maintenance task during handoff.

---

### 4c. External Handoff (LeanScale → Customer)

> **Purpose:** Formal project completion with customer.

**Final project meeting agenda:**

1. Review the lifecycle architecture one final time (5 min)
2. Walk through the documentation package (10 min)
3. Walk through the maintenance schedule (15 min) -- this is the most important part
4. Show them how to run the lifecycle measurement dashboard (5 min)
5. Q&amp;A and final questions (10 min)
6. Make it explicit: "Project complete. Here's when to call us back." (5 min)

**Documentation package:**

- Lifecycle Architecture Diagram (final version)
- Definition Alignment Document (final, signed-off version)
- Stage Reference Card (one-page PDF)
- CRM Configuration Spec (for their CRM admin's reference)
- All training video recordings
- FAQ document
- Maintenance Schedule

**For Single Project engagements:** Walk the customer through the maintenance schedule in detail. Record a video walkthrough of the process. Make sure they understand: what to check monthly, what to check quarterly, and what triggers a call back to LeanScale.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location
- [ ] Handoff documentation complete
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized

#### Internal Debrief (Optional but Recommended)

- What went well?
- What would we do differently?
- Were there definition alignment battles that could inform future projects?
- Any learnings to feed back into the standard lifecycle template?

#### Retention / Expansion

**Single Project Path:**

```
1. Upsell: Managed Services (lifecycle governance retainer)
   | if no
2. Downsell: Depth project -- Lead Scoring, Sales Stages depth, Customer Lifecycle depth, Attribution
   | if yes
3. Retry retainer at end of next project cycle
```

**Script:**

> "Now that the GTM Lifecycle architecture is in place, there are two ways we can continue. Option 1: We set up managed services where we run the monthly/quarterly lifecycle reviews and keep everything calibrated. Option 2: If there's a specific area that needs deeper work -- like building out a lead scoring model or going deeper on sales stage optimization -- we can scope a focused project. Which sounds more relevant?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On \[date ~quarter out\], we'll review how the lifecycle stages are performing -- conversion rates, adoption, any definitions that need updating."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                                |
| ------------------- | ----------------------------------------------------------- |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks             |
| 2. Review metrics   | Pull lifecycle dashboard data. Are conversion rates stable?  |
| 3. Decide ownership | Can Architect handle this check-in, or need specialist?     |
| 4. Prep materials   | If specialist needed, brief them. If Architect, prep talking points. |

---

## Deliverables &amp; Assets Summary

**Strategic Deliverables:**

| Deliverable                    | Description                                                    |
| ------------------------------ | -------------------------------------------------------------- |
| Lifecycle Architecture Diagram | Visual showing all stages across Lead, Sales, Customer domains |
| Definition Alignment Document  | All stage names with definitions, entry/exit criteria, signed off by stakeholders |
| Current State Audit            | Documentation of current CRM lifecycle fields and identified problems |
| Measurement Framework          | Which of the 6 metric categories to track and how              |

**Technical Deliverables (if Phase 2 applies):**

| Deliverable                    | Description                                                    |
| ------------------------------ | -------------------------------------------------------------- |
| CRM Configuration Spec         | Field-level specification for lifecycle stages, pipelines, automation |
| Configured Lifecycle Stages    | Lifecycle stage picklist values in CRM                         |
| Automation Rules               | Stage transition workflows (configured and tested)             |
| Lifecycle Measurement Dashboard| Reports for production, conversion, velocity, drop-off, cost   |
| Drop-off Reason Fields         | Picklist fields for recording why records don't advance        |

**Documentation Package:**

- Training video recordings (3: architecture, CRM usage, dashboard)
- Stage Reference Card (one-page PDF)
- FAQ document
- Definition Alignment Document (final version)
- Maintenance Schedule
- CRM Configuration Spec

---

## Appendix

### What This Document Is

This is the implementation playbook -- the step-by-step execution guide for delivering a GTM Lifecycle project from first contact to project close. It is the third file in a 3-file playbook structure: Overview (what the project IS), Methodology (HOW we think about the problem), and Implementation (WHAT to DO).

### What Each Phase Produces

| Phase                    | Output                                                                 | Gate Criteria                                                                  |
| ------------------------ | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **Phase 1: Strategy**    | Signed-off lifecycle architecture (Definition Alignment Doc + stage architecture with entry/exit criteria) | All department leads have approved definitions and stage architecture           |
| **Phase 2: Engineering** | Configured CRM with lifecycle stages, automation, and dashboards       | CRM matches spec, automation fires correctly, customer admin has approved      |
| **Phase 3: Enablement**  | Trained team with documentation                                        | All training delivered, hypercare complete, team can update stages independently |
| **Phase 4: Handoff**     | Independent customer + archived project                                | Internal/external handoffs complete, maintenance schedule in place, project closed |

### How to Adapt Per Project Type

GTM Lifecycle is a **Strategic-heavy** project:

| Project Profile       | Strategy Weight | Engineering Weight | Enablement Weight | This Project              |
| --------------------- | --------------- | ------------------ | ----------------- | ------------------------- |
| **Strategic-heavy**   | 60-80%          | 10-20%             | 10-20%            | GTM Lifecycle             |

**Adaptation rules for GTM Lifecycle:**

- **Phase 1 is the main event.** 60-70% of time and value is here. The lifecycle architecture IS the primary deliverable.
- **Phase 2 is light.** CRM field configuration, basic automation, and a dashboard. No custom code, no complex integrations.
- **Phase 3 is brief.** Training is about definitions and dashboard reading, not complex system usage.
- **Phase 4 always applies.** Lifecycle stages need ongoing governance or they drift.
- **Some projects skip Phase 2 entirely.** For $0-5M companies, the strategy deliverable may be the end product. The customer's CRM admin configures from the spec.

---

## References

- [HubSpot - Lifecycle Stage and Lead Status Guide](https://www.default.com/post/hubspot-lead-status-lifecycle-stages)
- [RevBlack - Salesforce Lead Stage vs Lead Status](https://www.revblack.com/guides/salesforce-lead-stage-vs-lead-status)
- [LeanScale - Measuring GTM Lifecycle](https://youtu.be/7l1VtgNSEYY)
- [RT Dynamic - The Ultimate Guide to Salesforce Opportunity Stages](https://www.rtdynamic.com/blog/salesforce-opportunity-stages-guide/)
- [HubSpot - Create and Customize Lifecycle Stages](https://knowledge.hubspot.com/object-settings/create-and-customize-lifecycle-stages)
- [HubSpot - Automatically Set and Sync Record Lifecycle Stages](https://knowledge.hubspot.com/object-settings/manage-how-lifecycle-stages-sync-between-objects)
- [RevBlack - How to Use Custom Lifecycle Stages in HubSpot](https://www.revblack.com/guides/how-to-use-custom-lifecycle-stages-in-hubspot)
- [The Digital Bloom - B2B SaaS Funnel Benchmarks](https://thedigitalbloom.com/learn/pipeline-performance-benchmarks-2025/)
- [Data-Mania - MQL to SQL Conversion Rate Benchmarks](https://www.data-mania.com/blog/mql-to-sql-conversion-rate-benchmarks-2025/)
- [Kalungi - HubSpot CRM Optimization for SaaS Companies](https://www.kalungi.com/blog/hubspot-crm-optimization-for-saas-companies)
