# Sales Qualification Methodology — Implementation

## Project One-Pager

### Project Type

- Category: Balanced
- Primary Deliverable: A qualification framework (MEDDIC, BANT, SPICED, or custom) embedded in the CRM with structured fields, scoring rubrics, training materials, and a coaching infrastructure that drives sustained adoption.

#### Phase Relevance

| Phase          | Applies? | Weight | Notes                                                        |
| -------------- | -------- | ------ | ------------------------------------------------------------ |
| 1. Strategy    | Yes      | Medium | 2-3 meetings: current state audit, methodology selection, framework customization |
| 2. Engineering | Yes      | Medium | CRM field creation, validation rules, dashboards, stage gate configuration |
| 3. Enablement  | Yes      | Heavy  | Rep training, manager coaching training, pilot rollout, reinforcement cadence |
| 4. Handoff     | Yes      | Medium | Internal + External handoff with coaching playbook and maintenance schedule |

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │    Medium    │     │    Medium    │     │    Heavy     │     │    Medium    │
  │ 1a→1b→1c→1d │     │ 2a→2b→2c→2d │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   2-3 meetings         CRM fields +         Training + coaching  Coaching playbook
   audit + selection    dashboards           + pilot rollout      + maintenance
```

**This project's flow:**
- Full 4-phase. Medium strategy (audit + selection), medium engineering (CRM config + dashboards), heavy enablement (training + coaching + pilot), standard handoff.
- Enablement is the make-or-break phase. Sales methodology implementations frequently fail within 90 days when training is not reinforced with coaching [1]. Phase 3 gets the most time and attention.
- Some customers may compress Phase 2 if they already have basic qualification fields and need refinement rather than net-new CRM builds.

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Watch intro video explaining what a qualification methodology is and why it matters for pipeline quality and win rates
- [ ] Complete intake form: current sales motion, average deal size, sales cycle length, number of stakeholders per deal, existing qualification approach (if any), CRM platform and version
- [ ] Provide CRM access (Salesforce or HubSpot) with read access to Opportunity records (last 90 days)
- [ ] Identify 3-5 sales reps available for interviews during current state assessment
- [ ] Confirm VP Sales availability for methodology selection decision meeting

##### Track B: Architect Prep
- [ ] Pull CRM opportunity data for last 90 days: win/loss rates, field completion rates, deal stage progression
- [ ] Audit existing qualification-related fields on the Opportunity object (any BANT/MEDDIC fields, Budget, Authority, Need, Timeline fields)
- [ ] Analyze win/loss patterns: identify common attributes of won vs lost deals
- [ ] Draft gap analysis: current qualification maturity vs target state
- [ ] Pre-fill methodology recommendation based on deal complexity profile (deal size x stakeholder count x sales cycle length)

#### Refinement Loop (1b -> 1c -> 1d)

| Meeting        | Sub-Phase | Focus                                                    | Stakeholder             | Output                              |
| -------------- | --------- | -------------------------------------------------------- | ----------------------- | ----------------------------------- |
| Kickoff        | 1b        | Present current state audit, validate gap analysis, discuss methodology options | VP Sales, Sales Ops     | Validated gaps, methodology shortlist |
| Refinement 1   | 1c        | Present methodology recommendation with pros/cons, review customized criteria | VP Sales, Sales Managers | Selected methodology, draft scoring rubric |
| Refinement 2   | 1c        | Review CRM field design, stage gate mapping, validation rules | Sales Ops, RevOps       | Approved CRM configuration spec     |
| Sign-Off       | 1d        | Full framework walkthrough, sign-off on methodology + CRM design | All                     | Approved qualification framework package |

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held — gap analysis validated, methodology shortlisted
- [ ] 1c. Refinement loop complete — methodology selected, framework customized, CRM spec approved
- [ ] 1d. Strategic sign-off obtained on qualification framework + CRM design

##### Phase 2: Engineering
- [ ] 2a. Tech spec created — field mappings, validation rules, dashboard requirements
- [ ] 2b. Engineering handoff meeting held — RevOps/admin aligned on build sequence
- [ ] 2c. Build complete — all CRM fields, layouts, validation rules, dashboards live
- [ ] 2d. QA/Test + customer sign-off — sample opportunities tested, reports verified

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped — deck, job aids, CRM reference guide, role-play scenarios
- [ ] 3b. Training sessions delivered — all reps and managers trained
- [ ] 3c. Hypercare period complete — pilot group monitored, adoption tracked, issues resolved
- [ ] 3d. Enablement sign-off — team operating independently, coaching cadence established

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff complete
- [ ] 4c. External handoff (to Customer) complete
- [ ] 4d. Project closed and archived

#### Document Types

##### Working Documents (iterate together)

| Document                        | Purpose                                          | When Complete                                     |
| ------------------------------- | ------------------------------------------------ | ------------------------------------------------- |
| Current State Audit             | Document existing qualification practices, gaps  | All rep interviews done, CRM data analyzed        |
| Methodology Selection Matrix    | Compare framework options against sales motion   | VP Sales selects methodology with rationale       |
| Qualification Criteria Document | Define each criterion with company-specific language | Sales leadership signs off on definitions + rubric |
| CRM Configuration Spec         | Map fields, validation rules, stage gates        | RevOps/admin approves build plan                  |

##### Deliverables (polished outputs)

| Deliverable                    | Created From                    | Customer Uses For                                   |
| ------------------------------ | ------------------------------- | --------------------------------------------------- |
| Customized Qualification Framework | Methodology selection + criteria doc | Internal reference, onboarding new reps            |
| CRM Qualification Section      | CRM config spec                 | Daily rep usage for opportunity qualification       |
| Adoption Dashboard             | CRM config spec                 | Manager pipeline reviews, coaching conversations    |
| Training Package               | Framework + CRM config          | Ongoing rep onboarding and reinforcement            |

#### Enablement Details

##### Training Types

| Type       | Audience               | Focus                                                              | Duration |
| ---------- | ---------------------- | ------------------------------------------------------------------ | -------- |
| Rep Training | All sales reps        | Methodology principles, qualifying questions, CRM field usage      | 90 min   |
| Manager Training | Sales managers     | Coaching methodology, using qualification data in pipeline reviews, coaching question framework | 60 min   |
| RevOps/Admin | RevOps, CRM Admin    | Field maintenance, report adjustments, validation rule management   | 45 min   |

##### Hypercare
- Applies: Yes
- Duration: 3 weeks (2-week pilot + 1-week full rollout stabilization)
- Office Hours: Yes — weekly 30-min slot for first 3 weeks post-launch

##### Training Assets to Create
- [ ] Training deck: methodology principles, company-specific customizations, qualifying question examples
- [ ] One-pager job aid: qualification questions mapped to each criterion
- [ ] CRM reference guide: where to enter data, what "good" looks like per field
- [ ] Role-play scenario bank: 3-5 scenarios showing good vs poor qualification
- [ ] Video walkthrough: CRM walkthrough — how to enter qualification data on an Opportunity
- [ ] Manager coaching playbook: coaching questions tied to each qualification criterion

#### Handoff & Retention

##### Internal Handoff
- Key context to transfer: Which methodology was selected (and why), how it maps to sales stages, common rep adoption challenges observed during pilot, coaching cadence established
- Escalation trigger: Any changes to qualification criteria definitions, adding/removing fields, modifying validation rules or stage gates

##### External Handoff (to Customer)
- Final meeting agenda: Review adoption metrics, walk through maintenance tasks, confirm internal methodology owner, demonstrate dashboard usage for ongoing monitoring
- Documentation package: Qualification framework document, CRM configuration guide, training recordings, coaching playbook, adoption dashboard

##### Maintenance Schedule
- Monthly: review field completion rates, coach low-adoption reps, assess data quality
- Quarterly: review methodology fit, update scoring rubric if sales motion changes

#### Key Assets

| Asset                        | When Used        |
| ---------------------------- | ---------------- |
| Intake Form Template         | Phase 1a         |
| Methodology Selection Matrix | Phase 1b-1c      |
| CRM Configuration Spec      | Phase 2a         |
| Training Deck Template       | Phase 3a         |
| Coaching Playbook Template   | Phase 3a-3b      |
| Adoption Dashboard Template  | Phase 2c, 3c, 4a |

#### Definition Alignment Terms

| Term                | Typical Definition                                                    |
| ------------------- | --------------------------------------------------------------------- |
| Qualification Criteria | The specific attributes or conditions that determine whether a prospect is a fit for the solution (e.g., Budget, Authority, Need, Timeline for BANT) |
| Scoring Rubric      | A 1-5 rating scale with written definitions for each level that standardizes how reps assess each qualification criterion |
| Stage Gate          | A CRM validation rule that requires specific qualification fields to be completed before an Opportunity can advance to the next stage |
| Qualification Completeness | The percentage of required qualification fields filled in on an Opportunity record — tracked at rep, team, and stage level |
| Methodology Adoption Rate | The percentage of new Opportunities created after go-live that have all required qualification fields completed within 30 days |
| Coaching Cadence    | The recurring schedule (weekly 1:1s, pipeline reviews) where managers use qualification data to coach reps on deal quality |

#### Common Gotchas
- CRM fields added without training reps on why and how -> empty or generic data ("Budget: TBD") -> Always pair CRM config with training, reinforce with coaching
- Methodology too complex for the sales motion (MEDDPICC for transactional sales with 1-2 decision makers) -> Unnecessary friction, low adoption -> Match methodology complexity to deal complexity [2]
- No coaching infrastructure built into rollout plan -> Implementations fail within 90 days without reinforcement [1] -> Build manager coaching into the plan from day one
- Reps treat qualification as a checklist instead of a conversation -> Low-quality data, compliance without insight -> Train qualification as a conversation skill, not a CRM data entry task
- Validation rules too strict at launch -> Reps resent the system, find workarounds -> Start with advisory alerts, tighten to blocking rules after 30 days of adoption
- No pilot before full rollout -> Issues discovered at scale are expensive to fix -> Run a 2-week pilot with 5-10 reps first

#### Methodology Options

| Option     | When to Use                                           | Complexity |
| ---------- | ----------------------------------------------------- | ---------- |
| BANT       | Simple sales cycles, &lt;$25K ACV, 1-2 decision makers, &lt;30-day cycles | Low        |
| MEDDIC     | Complex enterprise sales, >$50K ACV, 3-5+ stakeholders, 60-180 day cycles | Medium     |
| MEDDPICC   | Enterprise with partners/competition, >$100K ACV, 5-12+ stakeholders | High       |
| SPICED     | Outcome-focused selling, customer success alignment, value-based positioning | Medium     |
| Custom/Hybrid | When no single framework fits the sales motion perfectly | Varies     |

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on which qualification methodology to implement, how it maps to the company's sales motion, and what the CRM configuration will look like.
>
> **Output:** Customized Qualification Framework Document + CRM Configuration Spec (signed off by VP Sales and RevOps).

### 1a. Pre-Kickoff

> Two parallel tracks run before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                        | Format             |
| ----------------------------- | -------------------------------------------------------------- | ------------------ |
| Intro video                   | Explain what qualification methodology is, why it matters for pipeline quality and win rates, what the project covers | Video walkthrough (5-10 min) |
| Definition Alignment Document | Get stakeholder sign-off on key terms (what counts as "qualified," how stages map to qualification) | Google Doc         |
| Pre-filled intake form        | Sales motion profile: ACV, cycle length, stakeholder count, current CRM state, current qualification approach | Google Form or Doc |
| CRM access request            | Read access to Opportunity records for data audit              | Email to CRM admin |

**Completion tracking:** RevOps or Sales Ops contact follows up. Do not cancel kickoff if incomplete, but push hard. CRM access is critical — cannot do Track B without it.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                            | Output                              |
| ---- | ----------------------------------------------------------------- | ----------------------------------- |
| 1    | Pull CRM opportunity data (last 90 days): win/loss, field usage   | Raw data export                     |
| 2    | Audit existing qualification fields on Opportunity object         | Field inventory with completion rates |
| 3    | Analyze win/loss correlation with qualification data completeness | Gap analysis draft                  |
| 4    | Pre-fill methodology recommendation based on sales motion profile | Methodology selection matrix (draft) |
| 5    | Prepare kickoff presentation with current state findings          | Slide deck with data-backed insights |

**Critical:** Mark everything as ASSUMED. The kickoff call validates. Quantify the problem: "Only 40% of Opportunities have Budget documented, win rate is 18% — companies using structured qualification see 20-30% higher close rates [3]."

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building anything.

| Term                         | Our Definition                                                  | Internally Approved? |
| ---------------------------- | --------------------------------------------------------------- | -------------------- |
| Qualified Opportunity        | An Opportunity where all required qualification criteria are documented with a score of 3+ on each | [ ] Yes / [ ] No     |
| Sales Qualified Lead (SQL)   | A Lead that meets minimum qualification thresholds and is ready for Opportunity creation | [ ] Yes / [ ] No     |
| Stage Gate                   | A CRM rule requiring specific qualification fields before stage advancement | [ ] Yes / [ ] No     |
| Scoring Rubric               | A 1-5 scale with written definitions for each qualification criterion | [ ] Yes / [ ] No     |
| Qualification Review Cadence | Weekly pipeline review where managers assess qualification quality | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your sales leadership team. Check "Yes" when approved. We cannot build CRM fields or training materials until terms are aligned.

---

### 1b. Kickoff Call

> **Purpose:** Present the current state audit and gap analysis. Validate findings, discuss methodology options, begin framework selection.

#### Agenda (60-90 min)

| Time  | Topic                        | What Happens                                                |
| ----- | ---------------------------- | ----------------------------------------------------------- |
| 0-15  | Walk through current state   | "Here's what we found in your CRM data and rep interviews"  |
| 15-30 | Gap analysis presentation    | Which qualification data is missing, win rate correlations   |
| 30-45 | Methodology options overview | BANT vs MEDDIC vs MEDDPICC vs SPICED — pros/cons for their motion |
| 45-55 | Definition alignment review  | Walk through Definition Alignment Doc, get initial reactions |
| 55-65 | Next steps                   | Schedule refinement meetings, assign homework               |

#### What We Bring

- Current state audit (CRM data analysis, field completion rates, win/loss patterns)
- Gap analysis showing qualification maturity level
- Methodology selection matrix (pre-filled with recommendation)
- Definition Alignment Document (pre-filled with our recommendations)

#### What We Leave With

- Validated gap analysis (confirmed or corrected by VP Sales)
- Methodology shortlist (typically narrowed to 2 options)
- Feedback on definitions
- Rep interview insights (who to talk to, known pain points)
- Refinement meetings scheduled

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Select the methodology, customize the framework, and design the CRM configuration. Same analysis from pre-kickoff is refined each round.

#### The Pattern

```
Kickoff Call (validate current state, shortlist methodology)
    |
    v
Refinement 1: Methodology selection + criteria customization
    |
    v
Refinement 2: CRM design review + stage gate mapping
    |
    v
Final Review -> Sign-off
```

#### Meeting Details

| Meeting Type           | Focus                                                    | Stakeholder             |
| ---------------------- | -------------------------------------------------------- | ----------------------- |
| Methodology Selection  | Choose framework, define each criterion with company language, draft scoring rubric | VP Sales, Sales Managers |
| CRM Design Review      | Review field design, validation rules, stage gates, dashboard specs | Sales Ops, RevOps, CRM Admin |
| Final Review           | Full framework walkthrough, confirm everything before build | All stakeholders        |

#### Typical Timeline

| Milestone               | Timing                          |
| ----------------------- | ------------------------------- |
| Pre-kickoff prep        | 3-5 days                        |
| Kickoff call            | Day 1 of engagement             |
| Meeting loop            | 1-2 weeks (3-4 meetings total)  |
| Final review + sign-off | End of week 2-3                 |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything approved before building.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by VP Sales and sales leadership
- [ ] Qualification methodology selected with documented rationale
- [ ] Each criterion defined with company-specific language and examples
- [ ] Scoring rubric (1-5 scale) finalized with written definitions per level
- [ ] Stage gate mapping approved (which criteria required at which stage)
- [ ] CRM configuration spec approved by RevOps/admin
- [ ] Dashboard and reporting requirements documented
- [ ] No blockers for engineering

#### Decision Point

- **Proceed to Engineering** -> Customer wants CRM fields, dashboards, and validation rules built
- **Rare: Project scope reduction** -> Customer decides to implement methodology without CRM enforcement (training-only). Proceed to Phase 3, skip Phase 2.

---

## Phase 2: Engineering

> **Goal:** Build and configure the qualification methodology into the CRM with structured fields, validation rules, dashboards, and reporting.
>
> **Output:** CRM Opportunity object updated with qualification section, stage gates active, adoption dashboard live.

| Project Type                  | Engineering Weight | What Gets Built                                              |
| ----------------------------- | ------------------ | ------------------------------------------------------------ |
| Full implementation (typical) | Medium (30-40%)    | Custom fields, page layouts, validation rules, dashboards, reports |
| Light implementation          | Light (15-20%)     | Existing fields repurposed, minimal validation rules, basic reports |

### Sub-Phases

```
2a Tech Spec -> 2b Engineering Handoff -> 2c Build -> 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate the approved qualification framework into a CRM configuration specification.

**Input:** Signed-off Qualification Framework Document + CRM Configuration Spec from Phase 1

**What happens:**

1. Map each qualification criterion to a CRM field type (picklist, text area, lookup, checkbox)
2. Define field attributes: API names, picklist values, help text with examples
3. Document validation rules: which fields required at which stage transition
4. Specify page layout: qualification section placement and field ordering
5. Define dashboard components: completion rate charts, quality scoring, rep comparison

**Output:** Technical specification containing:

- Field mapping table (criterion -> CRM field name, type, picklist values)
- Validation rule logic (e.g., "Require Budget\_Confidence\_\_c >= 3 before Stage = Proposal")
- Page layout wireframe showing qualification section on Opportunity record
- Dashboard mockup with component specifications
- Build sequence (fields first, then layouts, then rules, then dashboards)

---

### 2b. Engineering Handoff

> **Purpose:** Review tech spec with CRM admin/RevOps before building.

**Who attends:** Architect + RevOps/CRM Admin

**Agenda (30-45 min):**

| Time  | Topic              | What Happens                                              |
| ----- | ------------------ | --------------------------------------------------------- |
| 0-15  | Walk through spec  | Architect explains each field, validation rule, and dashboard requirement |
| 15-30 | Admin questions     | Clarify field types, existing field conflicts, permission sets |
| 30-45 | Refine and approve | Adjust spec, confirm build approach and sequence          |

**What Architect brings:**

- Strategic framework document (for context on why each field exists)
- Technical specification (from 2a)
- Questions list (field naming conflicts, existing field overlap, permission considerations)

**What admin leaves with:**

- Approved tech spec
- Clear build sequence
- Known risks (e.g., "existing Budget\_\_c field needs to be deprecated in favor of new Budget\_Confidence\_\_c")

---

### 2c. Build (Configure)

> **Purpose:** Build the qualification methodology into the CRM.

**Input:** Approved tech spec from 2b

**Build sequence (Salesforce example):**

1. Create custom fields on Opportunity object:
   - For each qualification criterion: picklist field (1-5 score) + text field (notes/evidence)
   - Example MEDDIC fields: Metrics\_\_c, Economic\_Buyer\_\_c (Contact Lookup), Decision\_Criteria\_\_c, Decision\_Process\_\_c, Identified\_Pain\_\_c, Champion\_\_c (Contact Lookup)
2. Build qualification section on Opportunity page layout:
   - Group all qualification fields together with score prominently displayed [4]
   - Add field-level help text with examples of what "good" looks like per score level
3. Configure validation rules and stage gates:
   - Advisory alerts first (warning, not blocking) for first 30 days
   - Example: "Warn if Opportunity advances to Proposal without Identified\_Pain score >= 3"
   - Convert to blocking rules after adoption stabilizes
4. Build adoption dashboard:
   - Qualification field completion rate by rep (bar chart)
   - Qualification field completion rate by team (bar chart)
   - Completion rate by stage (shows where data drops off)
   - Qualification score vs win rate correlation (scatter plot)
   - Opportunities advancing without required fields (exception list)
5. Build manager coaching reports:
   - Pipeline review view with qualification data inline
   - Rep-level qualification quality scorecard
   - Alerts for opportunities advancing without required qualification

**Build tracking:**

- [ ] Custom fields created and configured
- [ ] Qualification section added to Opportunity page layout
- [ ] Field-level help text added to all fields
- [ ] Validation rules created (advisory mode for launch)
- [ ] Adoption dashboard built and tested
- [ ] Manager pipeline review report configured
- [ ] Alert rules for missing qualification data active

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify the CRM build works correctly and get customer approval.

**Technical testing checklist:**

- [ ] All qualification fields visible on Opportunity record for correct profiles
- [ ] Picklist values match approved scoring rubric exactly
- [ ] Help text displays correctly with examples
- [ ] Validation rules fire at correct stage transitions (test with sample Opportunities at each stage)
- [ ] Dashboard components render correctly with real data
- [ ] Manager reports show correct qualification data
- [ ] Alerts trigger for Opportunities advancing without required fields
- [ ] Field permissions correct (reps can edit, managers can view, admin can manage)

**Customer testing:**

- Walk RevOps through the build — field by field, rule by rule
- Have 2-3 reps test with real Opportunities (update qualification fields, advance stages)
- Have a manager test the pipeline review report and coaching dashboard
- Capture feedback, fix issues immediately

**Engineering sign-off checkpoint:**

- [ ] Built CRM configuration matches tech spec
- [ ] All technical tests passing
- [ ] Customer RevOps and sales leadership have tested and approved
- [ ] Ready for enablement (training can reference actual CRM configuration)

**Decision point:**

- **Proceed to Enablement** -> CRM is built and tested, ready for training
- **Loop back to Build** -> Issues found during testing, needs fixes before training

---

## Phase 3: Enablement

> **Goal:** The sales team can use the qualification methodology in their daily work — asking the right questions, entering data correctly, and managers can coach to it.
>
> **Output:** Trained reps and managers, pilot group validated, full rollout stabilized, coaching cadence established.

### Sub-Phases

```
3a Training Prep -> 3b Training Sessions -> 3c Hypercare -> 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials that teach the methodology as a selling skill, not just a CRM data entry task.

**Input:** Customized qualification framework + CRM configuration + scoring rubric

**What happens:**

1. Create training deck covering:
   - Why this methodology was selected (connect to their sales pain)
   - Each criterion explained with company-specific examples
   - How to ask qualifying questions naturally in conversation
   - Where and how to enter data in the CRM
2. Build one-pager job aid:
   - Each qualification criterion with 2-3 qualifying questions
   - Scoring rubric summary (what 1 vs 3 vs 5 looks like for each criterion)
3. Develop role-play scenarios:
   - 3-5 scenarios showing good vs poor qualification conversations
   - Include common customer pushback and how to navigate it
4. Create CRM reference guide:
   - Screenshots showing qualification section on Opportunity record
   - Step-by-step for entering each field
   - What "good data" looks like vs "checkbox compliance"
5. Build manager coaching playbook:
   - Coaching questions tied to each qualification criterion
   - How to use the adoption dashboard in pipeline reviews
   - Example coaching conversations: "I see your Champion score is 2 — tell me about your access to the economic buyer"
6. Record video walkthroughs:
   - CRM qualification data entry (5-7 min)
   - Dashboard navigation for managers (5 min)

**Output:** Complete training package ready for delivery

---

### 3b. Training Sessions

> **Purpose:** Train the sales team on the methodology as a selling approach and CRM usage as a tool to support it.

**Two types of training:**

| Type                   | Audience               | Focus                                                   | Duration |
| ---------------------- | ---------------------- | ------------------------------------------------------- | -------- |
| Rep methodology training | All sales reps        | Why this methodology, what each criterion means, how to ask qualifying questions, CRM data entry | 90 min   |
| Manager coaching training | Sales managers, team leads | Using qualification data in pipeline reviews, coaching question framework, adoption dashboard walkthrough | 60 min   |
| RevOps/admin training  | RevOps, CRM admin      | Field maintenance, report adjustments, validation rule management, dashboard updates | 45 min   |

**Rep training session structure (90 min):**

| Time  | Topic                             | Activity                                         |
| ----- | --------------------------------- | ------------------------------------------------ |
| 0-15  | Why this methodology              | Data from their CRM audit — "here's the gap"     |
| 15-35 | Criterion-by-criterion walkthrough | Each criterion with company-specific examples     |
| 35-50 | Qualifying questions practice     | Role-play exercise: practice asking questions naturally |
| 50-65 | CRM walkthrough                   | Live demo: entering qualification data on a real Opportunity |
| 65-80 | Role-play: full qualification     | Pair exercise: qualify a mock deal end-to-end     |
| 80-90 | Q&A + resources                   | Share job aid, CRM guide, video walkthroughs      |

**Manager coaching training session structure (60 min):**

| Time  | Topic                             | Activity                                         |
| ----- | --------------------------------- | ------------------------------------------------ |
| 0-10  | Why coaching matters              | Methodology implementations fail without reinforcement [1]. Gartner research: frontline manager coaching produces a 19% increase in success [5] |
| 10-25 | Coaching question framework       | Tied to each qualification criterion              |
| 25-40 | Dashboard + report walkthrough    | How to use adoption data in pipeline reviews      |
| 40-55 | Practice: mock pipeline review    | Manager practices coaching a rep on qualification quality |
| 55-60 | Establish coaching cadence        | Weekly 1:1 qualification review, weekly team pipeline review |

**Output:**

- Trained reps and managers
- Training recordings (video)
- Questions log (feeds into FAQ and refinements)

---

### 3c. Hypercare

> **Purpose:** Pilot rollout with monitoring, then full rollout with intensive support to stabilize adoption.

**Duration:** 3 weeks total (2-week pilot + 1-week full rollout stabilization)

**Week 1-2: Pilot Group**

- Select pilot group: 1 team or 5-10 reps (ideally mix of top performers and average)
- Monitor field completion rates daily
- Track data quality (are scores meaningful or all "3s"?)
- Gather rep feedback: What questions feel awkward? What fields are confusing?
- Adjust training materials and CRM configuration based on pilot learnings
- Office hours: 30-min weekly slot for pilot group Q&A

**Week 3: Full Rollout**

- Announce full launch with VP Sales sponsorship and communication
- Monitor qualification field completion rates daily
- Provide a support channel for questions
- Address common issues with targeted micro-training (5-min video walkthroughs)
- Publish daily adoption metrics for first week, then weekly
- Celebrate early wins: "Top qualifier this week" recognition

**Adoption targets:**

| Metric                           | Week 1 (Pilot) | Week 2 (Pilot) | Week 3 (Full) | Day 30 Target |
| -------------------------------- | --------------- | --------------- | -------------- | ------------- |
| Field completion rate (new opps) | 50%+            | 70%+            | 60%+           | 80%+          |
| Data quality (meaningful scores) | Baseline        | 60%+            | 50%+           | 70%+          |
| Manager coaching sessions held   | 1+ per manager  | 2+ per manager  | 1+ per manager | Weekly cadence |

**When to skip pilot:** Only if the sales team is fewer than 10 reps total. In that case, do full rollout with tighter monitoring.

**Output:** Stabilized system, adoption metrics baselined, no critical issues outstanding

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm the sales team can operate the methodology independently.

**Validation checkpoint:**

- [ ] All rep training sessions delivered and recorded
- [ ] Manager coaching training delivered
- [ ] RevOps/admin training delivered
- [ ] Pilot complete with lessons learned documented and applied
- [ ] Full rollout live for at least 1 week
- [ ] Field completion rate trending toward 80% target
- [ ] Managers conducting qualification reviews in 1:1s and pipeline meetings
- [ ] No critical CRM issues outstanding
- [ ] FAQ document created from questions log
- [ ] Team can operate without daily external support

**Decision point:**

- **Proceed to Handoff** -> Sales team is using the methodology, managers are coaching to it, adoption is tracking positively
- **Extend Hypercare** -> Adoption below 50% after 3 weeks, or managers not coaching — extend support by 1-2 weeks

---

## Phase 4: Handoff

> **Goal:** Clean project close with coaching cadence established, maintenance plan documented, and the customer self-sufficient.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the methodology and CRM configuration, project archived.

**Structure:**

```
4a Maintenance Schedule -> 4b Internal Handoff -> 4c External Handoff -> 4d Project Close
                                                   (to Customer)         (Archive + Debrief)
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At |
| ----------------------------- | -------------------- | ------------- |
| **Single Project**            | Customer owns        | 4c (External Handoff) |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention to keep the methodology alive and adoption strong.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task                | What to Check                                   | Red Flag Threshold                                   |
| --------------------------- | ----------------------------------------------- | ---------------------------------------------------- |
| Field completion rate audit | % of new Opportunities with all required fields  | Below 70% (was 80%+ at launch)                       |
| Data quality spot check     | Review 5-10 random Opportunities for meaningful scores | More than 30% have all-3s or generic text            |
| Coaching compliance check   | Are managers reviewing qualification in 1:1s?    | Fewer than 50% of managers conducting reviews weekly  |
| New rep onboarding status   | Are new hires getting methodology training?      | Any rep active for 30+ days without training          |

**Quarterly Tasks:**

| Quarterly Task               | What to Review                                   | Action if Off-Track                                  |
| ---------------------------- | ------------------------------------------------ | ---------------------------------------------------- |
| Methodology fit assessment   | Has the sales motion changed (new segment, new ACV)? | If deal profile shifted materially, re-evaluate methodology |
| Scoring rubric calibration   | Are scores consistent across reps? Compare with outcomes | Re-train on rubric definitions, update if criteria shifted |
| Win rate correlation analysis | Is qualification data predicting wins?           | If no correlation, investigate data quality or rubric fit |
| Stage gate effectiveness     | Are gates catching unqualified deals or just creating friction? | Adjust gate thresholds based on data                 |

**After First Business Cycle (30-90 days post-launch):**

- Win rate comparison: pre-methodology vs post-methodology (target: 10-15% improvement within 90 days)
- Forecast accuracy comparison: is qualification data improving forecast reliability?
- Sales cycle analysis: are qualified deals closing faster than unqualified ones?
- Rep adoption segmentation: who's using it well, who needs re-training?

**Refinement Triggers (when to re-engage):**

| Trigger                      | Threshold                              | Response                                             |
| ---------------------------- | -------------------------------------- | ---------------------------------------------------- |
| Field completion rate decline | Drops below 60% for 2+ consecutive weeks | Re-train, identify root cause (manager coaching lapsed?) |
| Win rate regression          | No improvement after 90 days            | Audit data quality, review methodology fit            |
| Sales motion change          | New market segment, ACV shift >50%, new buyer persona | Scope refinement project: re-evaluate methodology     |
| Manager turnover             | 2+ new managers who haven't been trained | Schedule manager coaching training for new hires      |

**Every 6-12 Months:**

- Full methodology review: is this still the right framework?
- Scoring rubric update based on 6+ months of outcome data
- CRM field audit: any fields unused or new ones needed?
- Training material refresh with new examples from won deals

---

### 4b. Internal Handoff

> **Purpose:** Transfer context so the ongoing relationship and methodology health can be managed.

**What needs to be transferred:**

- Which methodology was selected and why (BANT for simple motion, MEDDIC for enterprise, etc.)
- Customer context: who the internal methodology owner is, which managers are strong coaches, which reps adopted reluctantly
- Current adoption metrics and trends (is it healthy or needs attention?)
- Common issues observed during rollout
- When to escalate (methodology refinement = requires deeper expertise)

**Escalation guidelines:**

| Issue Type                                    | Who Handles                | Example                                    |
| --------------------------------------------- | -------------------------- | ------------------------------------------ |
| Small tweaks: add picklist value, update help text | Architect                  | "Can we add a 'No Budget' option?"          |
| New rep onboarding to methodology             | Architect (use training materials) | Run new hire through training deck + video  |
| Scoring rubric changes, methodology adjustments | SME                        | "We're moving upmarket, need MEDDPICC"      |
| Stage gate logic changes                      | SME                        | "Want to add Decision Process requirement at Discovery" |
| Full methodology refresh                      | SME (new project scope)    | Complete re-evaluation of framework         |

**For Dedicated engagements:** The ongoing owner also receives the maintenance schedule (4a) and becomes responsible for executing monthly and quarterly checks. Walk them through each maintenance task during handoff.

---

### 4c. External Handoff (to Customer)

> **Purpose:** Formal project completion with the customer team owning the methodology.

**Final project meeting agenda:**

- Review adoption metrics: field completion rate, data quality trends, win rate trajectory
- Walk through all deliverables: framework document, CRM configuration, training materials, coaching playbook
- Confirm internal methodology owner (who runs the maintenance schedule)
- Walk through maintenance schedule (monthly, quarterly, annual tasks)
- Answer final questions
- Make it explicit: "Project complete. Your team owns this now."

**Documentation package:**

- Customized Qualification Framework Document (final version)
- CRM Configuration Guide (fields, validation rules, stage gates, dashboards)
- Training recordings (video: rep training, CRM walkthrough, dashboard navigation)
- One-pager job aid (qualification questions + scoring rubric)
- Manager Coaching Playbook
- Adoption Dashboard + reporting package
- FAQ document
- Maintenance Schedule
- Definition Alignment Document (final version)

**For Single Project engagements:** Walk the customer through the maintenance schedule in detail. Record a video of the walkthrough. Emphasize the coaching cadence — this is what keeps the methodology alive.

**Output:** Customer owns the methodology and CRM configuration. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location
- [ ] Handoff documentation complete
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized
- [ ] Final adoption metrics documented (baseline for future comparison)

#### Internal Debrief (Optional but Recommended)

- What went well? (methodology selection process, training approach, pilot results)
- What would we do differently? (timeline, stakeholder involvement, training format)
- Any learnings to feed back into playbooks or tooling? (new role-play scenarios, CRM config patterns)

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell -> Downsell -> Retry  |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (retainer) — ongoing methodology coaching, quarterly reviews
   | if no
2. Downsell: Another one-time project — Lead Scoring, Forecasting Process, Pipeline Analytics
   | if yes
3. Retry retainer at end of next project cycle
```

**Script:**

> "Now that your qualification methodology is live and adoption is trending well, there are two ways we can continue. Option 1: We handle ongoing optimization — quarterly reviews, coaching refreshers, methodology refinements as your sales motion evolves. Option 2: If there's another specific area to improve, like lead scoring or forecasting, we can scope that out. Which sounds more interesting?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On [date ~90 days out], we'll review how qualification adoption is holding, check win rate trends, and see if the methodology needs any adjustments."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                        |
| ------------------- | --------------------------------------------------- |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks     |
| 2. Review metrics   | Pull adoption data, win rate trends, data quality    |
| 3. Decide ownership | Can this check-in be handled without SME, or is SME needed? |
| 4. Prep materials   | If SME needed, brief them. If not, prep talking points. |

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- Customized Qualification Framework Document: selected methodology with company-specific criterion definitions, scoring rubrics, and qualifying question bank
- Methodology Selection Rationale: documented comparison and decision (useful for future re-evaluation)
- Definition Alignment Document: signed-off terminology

**Technical Deliverables:**

- CRM qualification fields configured on Opportunity object
- Validation rules and stage gate logic
- Adoption dashboard (completion rates by rep, team, stage)
- Manager pipeline review reports with qualification data
- Alert rules for missing qualification data

**Documentation Package:**

- Training recordings (video: rep training, CRM walkthrough, dashboard navigation)
- One-pager job aid (questions + rubric summary)
- Manager Coaching Playbook
- CRM Reference Guide
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
| **SME** | Brought in for project-specific methodology expertise |

### What Each Phase Produces

| Phase                    | Output                                                                   | Gate Criteria                                                               |
| ------------------------ | ------------------------------------------------------------------------ | --------------------------------------------------------------------------- |
| **Phase 1: Strategy**    | Signed-off qualification framework + CRM configuration spec             | VP Sales approves methodology, criteria, scoring rubric, and CRM design     |
| **Phase 2: Engineering** | CRM fields, validation rules, dashboards built and tested               | All fields work, stage gates fire correctly, dashboards render, customer approved |
| **Phase 3: Enablement**  | Trained reps and managers, pilot complete, full rollout stabilized       | 80%+ field completion rate, managers coaching weekly, no critical issues     |
| **Phase 4: Handoff**     | Customer owns methodology + CRM configuration, project archived         | Internal/external handoffs complete, maintenance plan in place, coaching cadence running |

### How to Adapt Per Project Type

| Project Profile          | Strategy Weight | Engineering Weight | Enablement Weight | When This Applies                    |
| ------------------------ | --------------- | ------------------ | ----------------- | ------------------------------------ |
| **Full implementation**  | 25%             | 30%                | 45%               | New methodology, CRM build, full training |
| **Methodology refresh**  | 30%             | 15%                | 55%               | Existing fields, need better training + coaching |
| **CRM-only enhancement** | 15%             | 45%                | 40%               | Methodology chosen, need better CRM tooling |

**Adaptation rules:**

- Enablement is always the heaviest phase for this project type. The methodology fails without coaching reinforcement.
- If the customer already has qualification fields, Phase 2 compresses (repurpose existing fields, add what's missing).
- Phase 4 always applies — every implementation needs a coaching handoff.

### Single vs Dedicated Engagement

| Engagement Type               | What It Means                        | Key Difference                              |
| ----------------------------- | ------------------------------------ | ------------------------------------------- |
| **Single Project**            | One-off qualification implementation | Customer owns coaching cadence post-handoff  |
| **Dedicated (Multi-Project)** | Ongoing retainer                     | Architect monitors adoption metrics, runs quarterly reviews |

### Phase Guides

#### Phase 1: Strategy

**How We Create Value in Strategy**

For Sales Qualification Methodology projects, four principles apply:

**1. We educate.** Most customers know they need "better qualification" but cannot articulate what that means operationally. We educate them on methodology options, what each criterion measures, and how structured qualification drives win rates. 56% of seller time is wasted on unqualified, low-potential leads [6] — we show them the cost of the status quo.

**2. We drive alignment.** VP Sales and frontline managers often disagree on what "qualified" means. We force that conversation with the Definition Alignment Document. No building until terms are agreed.

**3. We come with an opinion.** We do not ask "which methodology do you want?" We assess their sales motion and recommend the right framework. They confirm and adjust.

**4. We show best practices.** We anchor in data: companies implementing structured qualification see 20-30% higher close rates [3]. We show what scoring rubrics look like at companies with similar sales motions.

**Why Phase 1 Matters**

The biggest risk in this project is selecting a methodology that does not match the sales motion complexity. MEDDPICC for a transactional cycle creates friction. BANT for enterprise deals leaves gaps. Getting this right in Phase 1 prevents a painful mid-project pivot.

#### Phase 2: Engineering

**Key Principles**

**Tech Spec (2a):** The CRM configuration must make qualification easy, not burdensome. Field-level help text, sensible picklist values, and logical page layout ordering reduce friction.

**Build (2c):** Start with advisory validation rules (warnings), not blocking rules. Let reps build the habit before enforcing compliance. Organizations using graduated enforcement see adherence rates increase from 40-50% to 90%+ within 30 days [7].

**Stage Gates:** Implement exit criteria between stages — for example, require Identified Pain and Economic Buyer identification before advancing from Discovery to Solution Alignment [4]. But start permissive — blocking rules at launch breed resentment.

#### Phase 3: Enablement

**Key Principles**

**This is where the project succeeds or fails.** Sales methodology implementations fail when training is not reinforced with ongoing coaching [1]. Enablement is not a one-time event — it is the establishment of a coaching infrastructure.

**Training Prep (3a):** Train qualification as a conversation skill, not a CRM compliance task. Reps who see it as "more admin work" will enter garbage data. Reps who see it as "a framework for asking better questions" will use it.

**Pilot (3c):** The pilot group is a pressure test. Use it to find issues before they scale. Common pilot discoveries: a criterion that does not make sense for their buyer, a CRM field that is confusing, a coaching question that misses the point.

**Reinforcement matters:** Sales teams using conversation intelligence and ongoing coaching see 25-40% better retention of training concepts compared to workshop-only approaches [7]. Build the coaching cadence into the plan — do not rely on managers to self-organize.

#### Phase 4: Handoff

**Why Maintenance Schedules Matter**

The qualification methodology degrades without active maintenance. New reps join without training. Managers stop coaching to it. The sales motion evolves but the rubric does not. The maintenance schedule prevents this drift.

The 30-day and 90-day check-ins are critical. At 30 days, you catch adoption problems early. At 90 days, you can measure win rate impact — the lagging indicator that proves the methodology is working.

### Troubleshooting Guide

| Scenario | Symptoms | Resolution |
| -------- | -------- | ---------- |
| Low field completion after training | Completion rate below 50% after 2 weeks | Check: Are managers reinforcing in 1:1s? Is VP Sales sponsoring? Re-train low-adoption reps individually. Consider reminders or gamification. |
| All scores are "3" (checkbox compliance) | Data quality review shows all-3s pattern | Reps are filling fields to pass validation, not qualifying genuinely. Re-train on what each score level means with real examples from their deals. Pair with manager coaching. |
| Methodology feels too complex | Reps complain about too many fields, too many questions | Evaluate: did we select the right methodology? If MEDDPICC feels heavy, consider simplifying to MEDDIC or creating a staged rollout (3 criteria first, add more after adoption stabilizes). |
| Managers not coaching to methodology | No pipeline review structure around qualification | Schedule a manager re-training. Provide the coaching question cheat sheet. Have VP Sales mandate qualification review in weekly pipeline meetings. |
| Validation rules creating friction | Reps finding workarounds, complaints escalating | Switch blocking rules back to advisory (warnings). Investigate which specific rules cause the most friction. Keep only the highest-impact gates as blocking. |
| New reps not trained | Reps hired after go-live do not know the methodology | Build methodology training into new hire onboarding checklist. Assign training videos + job aid on Day 1. Schedule 1:1 coaching session by Day 14. |
| Sales motion changed post-implementation | New segment, higher ACV, more stakeholders | Trigger a methodology review. If deal complexity shifted materially, scope a refinement project. May need to upgrade (BANT -> MEDDIC) or adjust scoring rubric. |

### Edge Cases

| Edge Case | How to Handle |
| --------- | ------------- |
| Customer already has partial qualification fields in CRM | Audit existing fields. Repurpose where possible (rename, update picklist values). Deprecate conflicting fields. Do not create duplicates. |
| Multiple sales motions requiring different frameworks | Implement primary methodology for dominant motion. Add supplementary criteria for secondary motion. Consider a hybrid framework. Document when to apply which criteria. |
| Customer uses HubSpot instead of Salesforce | All CRM configuration principles apply, but implementation differs: use HubSpot Deal properties instead of Opportunity fields, use workflow automation instead of Salesforce validation rules, use custom Deal card layouts. |
| VP Sales leaves during implementation | Identify new executive sponsor immediately. Re-present methodology rationale and get fresh sign-off before proceeding. Do not skip this — new leader may want a different approach. |
| Small team (&lt;5 reps) | Skip pilot phase. Do full rollout with tighter monitoring. Compress training into single session (reps + manager together). Simplify adoption dashboard. |
| Customer wants AI/conversation intelligence integration | Scope as a follow-on project or Phase 2 enhancement. Tools like Gong or Chorus can auto-populate qualification fields from call transcripts. Requires separate integration work. |

### References

[1] [Forrester - Ignore These Three Things To Guarantee A Sales Methodology Disastrophy](https://www.forrester.com/blogs/ignore-these-three-things-to-guarantee-a-sales-methodology-disastrophy/)

[2] [Demodesk - Sales Qualification Frameworks in 2024](https://demodesk.com/resources-guides/sales-qualification-frameworks-in-2024-how-to-choose-the-right-one-for-your-business)

[3] [MEDDICC - MEDDIC Sales Qualification and Frameworks](https://meddicc.com/meddic-sales-qualification-and-frameworks)

[4] [GoRattle - The RevOps Guide to MEDDIC Adherence in Salesforce](https://www.gorattle.com/blog/the-revops-guide-to-meddic-adherence-in-salesforce)

[5] [Gartner - 6 Essential Steps to Deploy Your Sales Methodology](https://www.gartner.com/en/articles/6-essential-steps-to-deploy-your-sales-methodology)

[6] [Gong - State of Sales Productivity 2024](https://www.gong.io/blog/b2b-sales-process)

[7] [Federico Presicci - 27 Sales Methodology Metrics: Track Adoption & Impact](https://federicopresicci.com/blog/sales-methodology/sales-methodology-metrics/)
