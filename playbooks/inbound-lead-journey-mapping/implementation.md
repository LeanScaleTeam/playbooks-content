# Inbound Lead Journey Mapping — Implementation

## Project One-Pager

> Quick reference for architects. One per project type. Fill this out FIRST — it serves as the project's identity card.

### Inbound Lead Journey Mapping One-Pager

#### Project Type

- Category: Strategic
- Primary Deliverable: Visual journey map of the inbound lead path from first engagement through conversion, with friction analysis and prioritized recommendations

##### Phase Relevance

| Phase          | Applies?  | Notes                                                        |
| -------------- | --------- | ------------------------------------------------------------ |
| 1. Strategy    | Yes       | 3-5 stakeholder interviews + data analysis + map creation    |
| 2. Engineering | Optional  | Quick-win CRM/MAP changes + monitoring dashboard only        |
| 3. Enablement  | Yes       | Walkthrough training on map artifacts + dashboard usage      |
| 4. Handoff     | Yes       | Journey map artifacts, recommendations doc, dashboard access |

· · ·

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │    Heavy     │     │    Light     │     │    Light     │     │     Med      │
  │ 1a→1b→1c→1d │     │  2a→2b→2c   │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   3-5 interviews       Quick-win CRM        Map walkthrough      Artifacts +
   + data + mapping     + dashboard          + dashboard train    recommendations
```

**This project's flow:**
- Full 4-phase. Heavy strategy (stakeholder interviews, data extraction, journey mapping, friction analysis), light engineering (quick-win implementations + dashboard build), standard enablement and handoff.
- Phase 2 is optional — some customers only want the strategic map and recommendations without implementation. Natural exit point after Phase 1d.

· · ·

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Watch intro video on what journey mapping is and why it matters
- [ ] Complete intake form: list inbound channels, current lead stages, known pain points
- [ ] Grant CRM read access (Salesforce/HubSpot) for lead data extraction
- [ ] Grant marketing automation platform access (HubSpot/Marketo/Pardot)
- [ ] Grant GA4 or web analytics read access
- [ ] Review Definition Alignment Document for lead stage definitions

##### Track B: Architect Prep
- [ ] Pull lead lifecycle report from CRM (last 90 days minimum)
- [ ] Calculate baseline conversion rates: Lead → MQL → SQL → Opp
- [ ] Extract average time-in-stage metrics per lifecycle step
- [ ] Pull lead source distribution breakdown
- [ ] Draft current-state journey skeleton based on CRM data
- [ ] Prepare stakeholder interview question list

· · ·

#### Refinement Loop (1b → 1c → 1d)

| Meeting           | Sub-Phase | Focus                                                    | Stakeholder                    | Output                            |
| ----------------- | --------- | -------------------------------------------------------- | ------------------------------ | --------------------------------- |
| Kickoff           | 1b        | Present v0 data findings, validate journey stages        | Marketing, Sales, RevOps leads | Validated stage definitions       |
| Stakeholder Interviews | 1c   | Interview Marketing team on content journey + channels   | Demand Gen, Content, Mktg Ops  | Channel-specific touchpoint data  |
| Stakeholder Interviews | 1c   | Interview Sales team on post-handoff lead experience     | SDRs, AEs, Sales Management    | Handoff friction points           |
| Data Review       | 1c        | Walk through drop-off analysis + friction points         | RevOps, Marketing Ops          | Validated friction point rankings |
| Journey Map Review| 1c        | Present draft journey map visual with all touchpoints    | All stakeholders               | Feedback on map accuracy          |
| Final Review      | 1d        | Present recommendations + journey map for sign-off       | All + executive sponsor        | Signed-off strategic package      |

· · ·

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held
- [ ] 1c. Stakeholder interviews complete (Marketing + Sales + RevOps)
- [ ] 1c. CRM and MAP data extracted and analyzed
- [ ] 1c. Drop-off points identified and quantified
- [ ] 1c. Buyer personas documented (2-3 primary)
- [ ] 1c. Touchpoint inventory completed across all stages
- [ ] 1c. Visual journey map created
- [ ] 1d. Recommendations prioritized and presented
- [ ] 1d. Lead stage definitions and handoff criteria agreed
- [ ] 1d. Strategic sign-off obtained

##### Phase 2: Engineering
- [ ] 2a. Quick-win list finalized (2-3 items, &lt;5 hours each)
- [ ] 2b. CRM/MAP changes implemented (stage definitions, alerts, routing)
- [ ] 2c. Monitoring dashboard built and validated

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped (journey map walkthrough, dashboard guide)
- [ ] 3b. Training sessions delivered (Leadership + Technical)
- [ ] 3c. Hypercare period complete (2 weeks)
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff (SME → Architect) complete
- [ ] 4c. External handoff (LeanScale → Customer) complete
- [ ] 4d. Project closed and archived

· · ·

#### Document Types

##### Working Documents (iterate together)

| Document                        | Purpose                                             | When Complete                              |
| ------------------------------- | --------------------------------------------------- | ------------------------------------------ |
| Stakeholder interview notes     | Capture pain points and perception gaps per team     | All interviews conducted and summarized    |
| Lead data analysis spreadsheet  | Quantify conversion rates, time-in-stage, drop-offs | All CRM/MAP data extracted and calculated  |
| Touchpoint inventory            | List every touchpoint across journey stages          | All channels and touchpoints documented    |
| Friction point ranking          | Prioritize drop-offs by severity and revenue impact  | Each friction point quantified and ranked  |

##### Deliverables (polished outputs)

| Deliverable                        | Created From                               | Customer Uses For                          |
| ---------------------------------- | ------------------------------------------ | ------------------------------------------ |
| Visual journey map                 | Touchpoint inventory + data analysis       | Internal alignment, board presentation     |
| Recommendations document           | Friction point ranking                     | Prioritizing optimization investments      |
| Lead stage definitions             | Definition Alignment Document              | Marketing/Sales shared language            |
| Monitoring dashboard               | Data analysis spreadsheet                  | Ongoing conversion tracking                |

· · ·

#### Enablement Details

##### Training Types

| Type       | Audience                            | Focus                                              | Duration |
| ---------- | ----------------------------------- | -------------------------------------------------- | -------- |
| Leadership | VP Marketing, VP Sales, CRO         | Interpret journey map, act on recommendations       | 30 min   |
| Technical  | RevOps, Marketing Ops, Sales Ops    | Maintain dashboard, update journey map, track metrics | 60 min   |

##### Hypercare
- Applies: Yes (light)
- Duration: 2 weeks
- Office Hours: Yes — Weekly 30-min slot for Q&A on journey map interpretation and dashboard usage

##### Training Assets to Create
- [ ] Video walkthrough: Journey map walkthrough and how to read it
- [ ] Video walkthrough: Dashboard navigation and filter usage
- [ ] Doc: Lead stage definitions and handoff criteria reference
- [ ] Doc: Maintenance playbook for ongoing journey monitoring

· · ·

#### Handoff & Retention

##### Internal Handoff (SME → Architect)
- Key context for Architect: Journey map structure, key friction points identified, which recommendations were implemented vs deferred, dashboard access credentials
- Escalation trigger: Customer requests journey map redesign, new channel addition requiring re-mapping, or lead stage redefinition

##### External Handoff (LeanScale → Customer)
- Final meeting agenda: Review delivered artifacts, walk through dashboard, confirm maintenance cadence, answer final questions
- Documentation package: Visual journey map, recommendations doc, lead stage definitions, dashboard access, maintenance schedule

##### Maintenance Schedule
- Monthly: Check conversion rates against baseline, review dashboard metrics
- Quarterly: Full journey audit, check for new channels or changed processes
- Who owns: Single project = customer owns | Dedicated = Architect owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services → if no → Downsell: Related project (Lead Scoring, Marketing-to-Sales Handoff SLA) → Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~90 days post-delivery
- Internal prep trigger: 2 weeks before
- Decision: Architect handles / SME needed

· · ·

#### Definition Alignment Terms

| Term                    | Typical Definition                                                                                         |
| ----------------------- | ---------------------------------------------------------------------------------------------------------- |
| Lead                    | Any person who has provided contact information through an inbound channel                                  |
| MQL (Marketing Qualified Lead) | A lead that meets firmographic and engagement criteria defined by Marketing (e.g., ICP fit + content engagement threshold) |
| SQL (Sales Qualified Lead)     | A lead that Sales has accepted and confirmed meets qualification criteria through direct interaction          |
| Opportunity              | An SQL with a defined deal (budget, timeline, decision-maker identified)                                    |
| Touchpoint               | Any interaction between a lead and the company (email, page view, form fill, call, demo)                    |
| Drop-off point           | A stage transition where a statistically significant percentage of leads fail to progress                    |
| Speed-to-lead            | Time from form submission or engagement signal to first human outreach by SDR/sales                         |
| Dark lead                | A lead that goes inactive (no engagement) without converting or being disqualified                          |

· · ·

#### Common Gotchas
- Different teams use different definitions for MQL/SQL/handoff → Interview stakeholders early to surface conflicts, resolve before mapping
- Mapping only the "happy path" and ignoring leads that go dark → Explicitly map the dark lead path and re-engagement touchpoints
- CRM data is dirty (duplicate leads, missing stage timestamps) → Run a data quality check before analysis; document known gaps
- Building the journey map for the ideal state instead of current state first → Map current state first, then overlay ideal state to identify gaps
- Only interviewing Marketing and ignoring Sales perspective → The journey does not end at MQL; include SDR and AE interviews
- Over-relying on CRM data without qualitative stakeholder input → Data shows where leads drop off; interviews reveal why

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on the inbound lead journey map, friction analysis, and prioritized recommendations.
>
> **Output:** Visual journey map + friction analysis + prioritized recommendations + agreed lead stage definitions (signed off by Marketing, Sales, and RevOps stakeholders).

### 1a. Pre-Kickoff

> Two parallel tracks run after the AE closes and before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                       | Format             |
| ----------------------------- | ------------------------------------------------------------- | ------------------ |
| Intro video                   | Explain what journey mapping is, why it matters, what we need | Video walkthrough (5-10 min) |
| Definition Alignment Document | Get stakeholder sign-off on lead stage definitions            | Google Doc         |
| Pre-filled intake form        | Confirm inbound channels, current stages, known pain points   | Google Form or Doc |
| Access request checklist      | CRM, MAP, and web analytics read access                       | Email              |

**Intake form asks for:**
- Current inbound lead sources and channels (website forms, content downloads, demo requests, chat, events)
- Current lead lifecycle stages as defined in CRM
- Known bottlenecks or pain points in the lead journey
- Existing persona documentation (if any)
- Previous journey mapping or lead analysis work (if any)
- Stakeholder names for Marketing, Sales, and RevOps interviews

**Completion tracking:** Architect follows up at 48 hours if access not granted. Do not cancel kickoff if intake incomplete, but push hard after.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                            | Output                                                |
| ---- | ----------------------------------------------------------------- | ----------------------------------------------------- |
| 1    | Extract lead data from CRM (last 90 days, or 6 months for low volume) | Raw dataset: lead sources, status changes, timestamps |
| 2    | Calculate baseline conversion rates (Lead → MQL → SQL → Opp)      | Conversion funnel with rates at each stage            |
| 3    | Calculate average time-in-stage for each lifecycle step            | Time-in-stage metrics per transition                  |
| 4    | Segment conversion data by lead source                             | Channel comparison table                              |
| 5    | Draft v0 journey skeleton with conversion points                   | Preliminary journey map in Miro/Lucidchart            |
| 6    | Prepare stakeholder interview question list                        | Interview guide customized to each role               |

**Critical:** Mark all findings as ASSUMED. The kickoff call and stakeholder interviews validate.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building the journey map.

| Term                           | Our Definition                                                                                     | Internally Approved? |
| ------------------------------ | -------------------------------------------------------------------------------------------------- | -------------------- |
| Lead                           | Any person who provides contact info through an inbound channel                                     | [ ] Yes / [ ] No     |
| MQL                            | Lead meeting firmographic + engagement threshold (defined by Marketing)                             | [ ] Yes / [ ] No     |
| SQL                            | Lead accepted by Sales with confirmed qualification criteria                                        | [ ] Yes / [ ] No     |
| Handoff                        | The process and criteria by which Marketing passes a qualified lead to Sales                         | [ ] Yes / [ ] No     |
| Speed-to-Lead SLA              | Maximum time from lead engagement signal to first sales outreach                                    | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your Marketing and Sales leadership team. Check "Yes" when approved. We cannot proceed with the journey map until lead stage definitions are aligned across teams.

---

### 1b. Kickoff Call

> **Purpose:** Present v0 journey skeleton and baseline data. Validate stage definitions and scope.

#### Agenda (60-90 min)

| Time  | Topic                       | What Happens                                                        |
| ----- | --------------------------- | ------------------------------------------------------------------- |
| 0-15  | Walk through v0 journey     | "Here's what the data tells us about your current inbound journey"  |
| 15-30 | Validate conversion rates   | ASSUMED metrics → CONFIRMED or corrected with customer context      |
| 30-45 | Definition alignment        | Review lead stage definitions — surface conflicting language         |
| 45-55 | Scope confirmation          | Confirm inbound channels in scope, journey endpoint (Opp or Closed-Won) |
| 55-70 | Interview scheduling        | Schedule stakeholder interviews: 2-3 Marketing, 2-3 Sales, 1 RevOps |
| 70+   | Next steps                  | Assign homework, set cadence                                        |

#### What We Bring

- v0 journey skeleton with baseline conversion rates from CRM data
- Lead source distribution breakdown
- Time-in-stage metrics per lifecycle step
- Definition Alignment Document (pre-filled with our recommendations)
- Stakeholder interview question list (for review/feedback)

#### What We Leave With

- Corrections on baseline data (info needed to refine v1)
- Confirmed or contested lead stage definitions
- Stakeholder interview schedule
- Confirmed scope (channels in/out, journey endpoint)

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Conduct stakeholder interviews, analyze data, build the journey map, and iterate until sign-off.

#### The Pattern

```
Kickoff Call (validate data, set scope)
    ↓
Stakeholder Interviews (2-3 Marketing + 2-3 Sales + 1 RevOps)
    ↓
Data Deep-Dive: extract MAP + web analytics data → merge with CRM data
    ↓
Friction Analysis: identify drop-off points, quantify revenue impact
    ↓
Persona Documentation: define 2-3 primary buyer personas
    ↓
Touchpoint Inventory: map all touchpoints across stages
    ↓
Journey Map Build: create visual map in Miro/Lucidchart
    ↓
Data Review Meeting (present drop-offs + friction ranking)
    ↓
Journey Map Review Meeting (present visual map + recommendations)
    ↓
Final Review → Sign-off
```

#### Stakeholder Interviews

**Marketing Interviews (30 min each, 2-3 people):**

| Role          | Key Questions                                                                                                  |
| ------------- | -------------------------------------------------------------------------------------------------------------- |
| Demand Gen    | Which channels drive the most leads? Which drive the highest-quality leads? Where do you see leads stalling?   |
| Content       | What content assets do leads engage with before converting? What's the typical content journey?                 |
| Marketing Ops | How are MQLs defined and triggered? What automation runs between lead creation and MQL? What's your SLA with Sales? |

**Sales Interviews (30 min each, 2-3 people):**

| Role             | Key Questions                                                                                                 |
| ---------------- | ------------------------------------------------------------------------------------------------------------- |
| SDR/BDR          | How do you receive MQLs? What does "good" look like? What makes you reject a lead? What's your response time? |
| AE               | What does the post-SQL journey look like? Where do deals stall? What info do you wish you had at handoff?     |
| Sales Management | How do you track lead-to-opp conversion? What's your biggest friction point with Marketing?                   |

**RevOps Interview (30 min):**

| Focus                 | Key Questions                                                                                   |
| --------------------- | ----------------------------------------------------------------------------------------------- |
| Process + Data        | Walk me through the lead lifecycle as configured in the CRM. Where are the gaps in tracking?    |
| Cross-Team Alignment  | Where do Marketing and Sales definitions conflict? What data quality issues exist?               |
| Systems               | What's the integration architecture between CRM, MAP, and web analytics?                        |

#### Data Collection & Analysis

**CRM Data (Salesforce/HubSpot):**

| Metric                          | How to Pull                                           | What It Tells You                        |
| ------------------------------- | ----------------------------------------------------- | ---------------------------------------- |
| Lead → MQL conversion rate       | Lead status report, last 90 days                      | Marketing qualification effectiveness    |
| MQL → SQL conversion rate        | MQL cohort tracking with SQL timestamps               | Handoff quality and Sales acceptance     |
| SQL → Opportunity rate           | SQL records matched to Opportunity creation            | Sales follow-through effectiveness       |
| Average time-in-stage            | Date difference between status change timestamps       | Where leads stall (friction indicator)   |
| Lead source distribution         | Group by Lead Source field                              | Channel mix and volume per source        |
| Conversion rate by lead source   | Cross-tab: source x downstream conversion              | Which channels produce quality vs volume |

**Marketing Automation Data (HubSpot/Marketo/Pardot):**

| Metric                         | How to Pull                                      | What It Tells You                           |
| ------------------------------ | ------------------------------------------------ | ------------------------------------------- |
| Email engagement by campaign   | Campaign performance report                       | Which nurture sequences drive engagement    |
| Landing page conversion rates  | Landing page analytics                            | Form optimization opportunities             |
| Content asset engagement       | Content analytics / form submission attribution    | Pre-conversion content consumption patterns |
| Nurture sequence drop-off      | Workflow/sequence analytics                       | Where automated sequences lose leads        |

**Web Analytics Data (GA4):**

| Metric                  | How to Pull                          | What It Tells You                            |
| ----------------------- | ------------------------------------ | -------------------------------------------- |
| Pages viewed pre-form   | User flow / path analysis            | Content journey before conversion            |
| Session duration         | Engagement metrics                   | Depth of engagement before converting        |
| Exit pages              | Exit page report                     | Where leads leave the website                |
| Traffic source quality  | Source/medium report x conversions   | Which acquisition channels produce converters |

#### Friction Analysis

For each stage transition, calculate:

1. **Drop-off percentage** — What % of leads fail to progress?
2. **Average time-in-stage** — How long does the transition take?
3. **Revenue impact** — What's the estimated revenue loss from this drop-off? (Drop-off volume x average deal size x downstream conversion probability)

Average B2B SaaS MQL-to-SQL conversion rates range from 15-21%, meaning 79-85% of MQLs fail to become SQLs [1]. Companies using behavioral scoring models achieve 39-40% conversion rates, roughly double the average [2]. This provides a critical benchmark for evaluating client performance.

**Friction ranking template:**

| Rank | Stage Transition | Drop-Off % | Avg Time-in-Stage | Est. Revenue Impact | Root Cause Hypothesis    |
| ---- | ---------------- | ---------- | ------------------ | ------------------- | ------------------------ |
| 1    | [e.g., MQL → SQL] | [e.g., 82%] | [e.g., 14 days]  | [e.g., $1.2M/yr]   | [e.g., Slow response time] |
| 2    | ...              | ...        | ...                | ...                 | ...                      |

#### Journey Map Build

**Tool selection:**

| Tool        | Best For                                          | When to Use                              |
| ----------- | ------------------------------------------------- | ---------------------------------------- |
| Miro        | Collaborative workshops, real-time stakeholder input | Default choice — best for iteration     |
| Lucidchart  | Clean, presentation-ready diagrams                 | When customer needs boardroom-quality    |
| Figma       | Design-heavy teams that already use Figma          | If customer's team is Figma-native       |
| PowerPoint  | Low-tech stakeholders who need slides              | Last resort if other tools aren't viable |

**Map structure:**
- Horizontal lanes: Awareness → Consideration → Decision → Handoff → Post-Handoff
- Within each lane: Touchpoints (automated + human)
- Between lanes: Conversion points with metrics (conversion rate + time)
- Overlay: Persona swim lanes (if journeys differ significantly)
- Highlights: Drop-off points flagged with red indicators and revenue impact

#### Before Each Meeting

1. Process previous meeting notes/interview transcripts
2. Update journey map and analysis
3. Prepare questions for next validation round

#### During Each Meeting

1. Walk through current version of analysis/map
2. Capture corrections and new insights
3. Validate what's now CONFIRMED
4. Identify remaining gaps

#### After Each Meeting

1. Update journey map and friction analysis
2. Track what moved from ASSUMED → CONFIRMED
3. Update working documents

#### Potential Meeting Types

| Meeting Type         | Focus                                            | Stakeholder                      |
| -------------------- | ------------------------------------------------ | -------------------------------- |
| Kickoff              | Present v0, validate scope and definitions       | Marketing, Sales, RevOps leads   |
| Stakeholder Interviews | Qualitative input on journey perception         | Individual stakeholders          |
| Data Review          | Walk through friction analysis + drop-off data   | RevOps, Marketing Ops            |
| Journey Map Review   | Present visual map + recommendations             | All stakeholders                 |
| Final Review         | Sign-off on map + definitions + recommendations  | All + executive sponsor          |

#### Typical Timeline

| Milestone                    | Timing                                   |
| ---------------------------- | ---------------------------------------- |
| Pre-kickoff prep             | 2-3 days                                 |
| Kickoff call                 | Day 1 of engagement                      |
| Stakeholder interviews       | Week 1-2 (schedule as available)         |
| Data extraction + analysis   | Week 1-2 (parallel with interviews)      |
| Journey map build            | Week 2-3                                 |
| Review meetings + refinement | Week 3-4                                 |
| Final review + sign-off      | Week 4-5                                 |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm journey map, friction analysis, recommendations, and definitions are complete and agreed.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by Marketing and Sales leadership
- [ ] Stakeholder interviews complete (all teams represented)
- [ ] CRM, MAP, and web analytics data extracted and analyzed
- [ ] Friction points identified, quantified, and ranked by revenue impact
- [ ] 2-3 buyer personas documented with persona-specific journey differences
- [ ] Complete touchpoint inventory across all in-scope journey stages
- [ ] Visual journey map created and validated by stakeholders
- [ ] Recommendations prioritized using impact/effort matrix
- [ ] Lead stage definitions and handoff criteria agreed across teams
- [ ] Customer understands deliverables and next steps

#### Decision Point

- **Proceed to Engineering** → Customer wants quick wins implemented + monitoring dashboard built
- **Project complete** → Strategic deliverable (journey map + recommendations) is the end product

> Many Inbound Lead Journey Mapping projects complete after Phase 1 if the customer's primary goal is visibility and alignment. The journey map and recommendations become the input for a separate implementation project. Confirm at sign-off whether Phase 2 is in scope.

---

## Phase 2: Engineering

> **Goal:** Implement 2-3 quick-win improvements and build a monitoring dashboard based on journey map findings.
>
> **Output:** Quick wins implemented in CRM/MAP, monitoring dashboard live.

| Project Type    | Engineering Weight | Context                                                   |
| --------------- | ------------------ | --------------------------------------------------------- |
| Strategic-heavy | Light (10-20%)     | Inbound Lead Journey Mapping — quick wins + dashboard only |

### Sub-Phases

```
2a Quick-Win Spec → 2b Implement Changes → 2c Dashboard Build + Test
```

---

### 2a. Quick-Win Spec

> **Purpose:** Translate top recommendations into specific, implementable changes.

**Input:** Prioritized recommendation list from Phase 1

**What happens:**

1. Review top 5-7 recommendations from friction analysis
2. Select 2-3 that can be implemented in &lt;5 hours each
3. Document specific CRM/MAP changes for each

**Common quick wins for journey mapping projects:**

| Quick Win                                  | System           | Typical Time |
| ------------------------------------------ | ---------------- | ------------ |
| Update lead stage definitions in CRM       | Salesforce/HubSpot | 1-2 hours   |
| Configure speed-to-lead alert for new MQLs | CRM + Slack/email  | 2-3 hours   |
| Add lead source tracking field             | CRM               | 1-2 hours   |
| Create MQL-to-SQL SLA alert               | CRM + automation   | 2-3 hours   |
| Update lead scoring threshold criteria     | MAP                | 2-4 hours   |
| Fix broken nurture sequence at drop-off    | MAP                | 2-4 hours   |

**Output:** Quick-win spec with specific fields, workflows, and configurations to change.

---

### 2b. Implement Changes

> **Purpose:** Execute quick-win changes in CRM and marketing automation platform.

**Input:** Quick-win spec from 2a

**The build loop:**

1. Implement change in sandbox/staging (if available)
2. Test the change
3. Deploy to production
4. Document the change

**Build tracking:**

- [ ] Quick win 1: [description] — [status]
- [ ] Quick win 2: [description] — [status]
- [ ] Quick win 3: [description] — [status]

---

### 2c. Dashboard Build + Test

> **Purpose:** Build a monitoring dashboard to track journey performance and measure improvement.

**Dashboard components:**

| Component                    | Metric                                     | Visualization     |
| ---------------------------- | ------------------------------------------ | ------------------ |
| Conversion funnel            | Lead → MQL → SQL → Opp rates              | Funnel chart       |
| Time-in-stage                | Average days per stage transition           | Bar chart          |
| Drop-off tracking            | Drop-off % at each stage (trend over time) | Line chart         |
| Lead source performance      | Conversion rate by source/channel           | Table or bar chart |
| Speed-to-lead                | Avg time from MQL to first Sales touch      | Gauge or number    |
| Period comparison            | Current period vs baseline (pre-project)    | Delta/comparison   |

**Where to build:**

| Tool              | When to Use                                          |
| ----------------- | ---------------------------------------------------- |
| Salesforce Reports + Dashboards | Customer is Salesforce-native, simple metrics  |
| HubSpot Dashboards | Customer is HubSpot-native                           |
| Tableau / Looker  | Customer needs cross-system data blending             |

**Testing checklist:**

- [ ] All metrics calculating correctly against raw data
- [ ] Filters working (date range, lead source, persona)
- [ ] Dashboard loads in &lt;10 seconds
- [ ] Data refreshes on expected cadence
- [ ] Stakeholders can access the dashboard

**Engineering sign-off checkpoint:**

- [ ] All quick wins implemented and tested
- [ ] Dashboard built and validated
- [ ] Customer has reviewed and approved
- [ ] Ready for enablement

---

## Phase 3: Enablement

> **Goal:** Customer team can read the journey map, use the dashboard, and maintain both independently.
>
> **Output:** Trained team with documentation, stabilized system, no critical issues.

### Sub-Phases

```
3a Training Prep → 3b Training Sessions → 3c Hypercare → 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from journey map and dashboard documentation.

**Input:** Journey map visual + recommendations doc + dashboard + lead stage definitions

**What happens:**

1. Create script for journey map walkthrough recording
2. Create script for dashboard navigation recording
3. Draft written guide for lead stage definitions and handoff criteria
4. Create maintenance playbook (how to keep the journey map current)
5. Compile FAQ based on common questions from stakeholder interviews

**Output:** Training package containing:

- Video walkthrough scripts (2 recordings: journey map + dashboard)
- Written guide: lead stage definitions and handoff process
- Maintenance playbook: how and when to update the journey map
- FAQ document

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to customer team.

**Two types of training:**

| Type                | Audience                        | Focus                                                                 |
| ------------------- | ------------------------------- | --------------------------------------------------------------------- |
| Leadership training | VP Marketing, VP Sales, CRO     | How to read the journey map, interpret metrics, act on recommendations |
| Technical handoff   | RevOps, Marketing Ops, Sales Ops | How to maintain the dashboard, update the journey map, run audits      |

**Leadership training session (30 min):**
- Walk through journey map — how to read stages, touchpoints, conversion metrics
- Explain friction points and what the data reveals
- Review recommendations and expected impact
- Show dashboard — key metrics to monitor weekly/monthly

**Technical training session (60 min):**
- Dashboard deep-dive — every metric, filter, and data source
- Lead stage definitions — where they live in CRM, how to update
- Journey map maintenance — when and how to update touchpoints
- Quick-win changes — what was changed, where, and how to adjust

**Training delivery:**

1. Schedule sessions with appropriate stakeholders
2. Deliver training (live, recorded)
3. Record video walkthroughs for future reference
4. Answer questions, note gaps

**Output:**

- Trained stakeholders
- Video recordings
- Questions log (feeds into FAQ)

---

### 3c. Hypercare

> **Purpose:** Light post-launch support to answer questions and stabilize.

**Duration:** 2 weeks

**What happens:**

- Weekly 30-min office hours (Zoom or Slack)
- Respond to dashboard questions or interpretation issues within 24 hours
- Fix any dashboard bugs or data discrepancies
- Confirm quick-win changes are performing as expected

**When to skip:** If Phase 2 was skipped (strategic-only delivery), hypercare may be unnecessary. Confirm with customer.

**Output:** Stabilized system, no critical issues outstanding

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm customer can operate independently.

**Validation checkpoint:**

- [ ] All training sessions delivered
- [ ] Training recordings and documentation provided
- [ ] Hypercare period complete (if applicable)
- [ ] No critical issues outstanding
- [ ] Customer team can interpret journey map independently
- [ ] Customer team can navigate and use dashboard
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** → Customer is enabled, project wrapping up
- **Extend Hypercare** → Still needs support, extend by 1 week

---

## Phase 4: Handoff

> **Goal:** Clean project close with maintenance plan established and retention/expansion path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the system, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule → 4b Internal Handoff → 4c External Handoff → 4d Project Close
                          (SME → Architect)      (LeanScale → Customer)  (Archive + Debrief)
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

| Monthly Task               | What to Check                                            | Red Flag Threshold                                    |
| -------------------------- | -------------------------------------------------------- | ----------------------------------------------------- |
| Conversion rate review     | MQL→SQL and SQL→Opp conversion rates vs baseline          | &gt;5 percentage point decline from baseline for 2+ months |
| Speed-to-lead check        | Average time from MQL trigger to first Sales outreach     | &gt;2 hours average (benchmark: 5 minutes is optimal [3]) |
| Dashboard health check     | All metrics loading, data refreshing, no broken reports   | Any metric showing stale data or errors               |

**Quarterly Tasks:**

| Quarterly Task              | What to Review                                          | Action if Off-Track                                   |
| --------------------------- | ------------------------------------------------------- | ----------------------------------------------------- |
| Full journey audit          | Re-check all stage transitions for new friction points   | Update journey map, re-rank friction points            |
| Channel performance review  | Compare lead source conversion rates vs prior quarter    | Adjust channel strategy, update MAP if new channels   |
| Lead stage definition check | Are MQL/SQL definitions still accurate and enforced?     | Update definitions, retrain teams if drift detected    |
| Touchpoint inventory update | Have new touchpoints been added (new content, chatbot)?  | Add to journey map, assess impact on conversions       |

**After First Business Cycle (60-90 days post-launch):**

- **Conversion Rate Validation:** Have MQL→SQL conversion rates improved vs baseline? Industry benchmark: top performers achieve 30-40% MQL→SQL, while average is 15-21% [1][2]. Compare against both.
- **Recommendation Impact Check:** Did implemented quick wins produce measurable improvement? If not, investigate whether the root cause hypothesis was correct.
- **Key Question:** Is the journey map still accurate, or have processes changed since mapping?

**Refinement Triggers (when to re-engage):**

| Trigger                              | Threshold                                          | Response                                              |
| ------------------------------------ | -------------------------------------------------- | ----------------------------------------------------- |
| MQL→SQL conversion rate decline      | &gt;10 percentage point drop from post-project baseline | Re-engage SME — investigate new friction points        |
| New inbound channel added            | Any new channel (e.g., chatbot, new content type)  | Update journey map touchpoint inventory                |
| Marketing/Sales reorg                | New team structure or handoff process               | Re-map handoff stages, update definitions              |
| CRM/MAP platform change              | Migration to new system                             | Full journey re-mapping project                        |

**Every 6-12 Months:**

- Full journey map refresh: re-interview stakeholders, re-pull data, rebuild map
- Persona update: have buyer personas shifted based on new data?
- Market conditions check: competitive landscape changes affecting lead behavior?

---

### 4b. Internal Handoff (SME → Architect)

> **Purpose:** Transfer context so Architect can manage ongoing relationship.

**What the Architect needs to know:**

- What was mapped and what the key findings were (top 3-5 friction points)
- Customer context (which stakeholders care about what, team dynamics between Marketing and Sales)
- What quick wins were implemented and their expected impact
- Dashboard access and how to interpret the key metrics
- **Maintenance schedule** (if Dedicated engagement — Architect runs this)

**Escalation guidelines:**

| Issue Type                                       | Who Handles                         | Example                                          |
| ------------------------------------------------ | ----------------------------------- | ------------------------------------------------ |
| Dashboard filter changes, minor metric questions | Architect                           | "Can we add a date filter for this quarter?"     |
| New channel mapping, lead stage redefinition     | SME                                 | "We added a chatbot — need to update the map"    |
| Full journey re-mapping                          | SME (new project scope)             | "Our entire lead process changed after reorg"    |

**For Dedicated engagements:** Architect also receives the maintenance schedule (4a) and becomes responsible for executing monthly/quarterly checks. SME walks Architect through each task.

---

### 4c. External Handoff (LeanScale → Customer)

> **Purpose:** Formal project completion with customer.

**Final project meeting:**

- Review what was delivered (journey map, recommendations, definitions, dashboard)
- Walk through documentation package
- Walk through maintenance schedule in detail
- Confirm nothing outstanding
- Answer final questions
- Make it explicit: "Project complete"
- **For Single Project engagements:** Hand over the maintenance schedule and walk the customer through it. Record a video walkthrough.

**Documentation package:**

- Visual journey map (Miro/Lucidchart — shared access)
- Recommendations document with impact/effort priorities
- Lead stage definitions and handoff criteria (final version)
- Monitoring dashboard (shared access/ownership transferred)
- Training video recordings
- Maintenance schedule
- FAQ document

**Output:** Customer owns the journey map artifacts and dashboard. Project formally complete.

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
- Any learnings to feed back into SOPs?
- Were stakeholder interviews efficient? How to improve the interview guide?

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell → Downsell → Retry    |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (retainer — ongoing journey optimization)
   ↓ if no
2. Downsell: Related project (Lead Scoring, Marketing-to-Sales Handoff SLA, Automated Outbound)
   ↓ if yes
3. Retry retainer at end of next project cycle
```

**Script:**

> "Now that the journey mapping is complete, there are two ways we can continue working together. Option 1: We can set you up on managed services where we monitor and optimize the journey on an ongoing basis — updating the map quarterly, running A/B tests on friction points, and maintaining your dashboard. Option 2: If there's a specific project from the recommendations — like implementing lead scoring or a marketing-to-sales handoff SLA — we can scope that out. Which sounds more interesting?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On [date ~90 days out], we'll review how the journey is performing vs the baseline we established and see if the map needs updating."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                                     |
| ------------------- | ---------------------------------------------------------------- |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks                  |
| 2. Review metrics   | Pull dashboard data, assess: Are conversion rates improving?      |
| 3. Decide ownership | Can Architect handle this check-in, or need SME?                 |
| 4. Prep materials   | If SME needed, brief them. If Architect, prep talking points.    |

**At the refinement check-in:**

- Review conversion rates vs baseline established during project
- Check if journey map is still accurate
- Identify any new friction points or changed processes
- If minor: Architect handles updates
- If major: Scope new project (full journey re-mapping)

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- Visual journey map (Miro/Lucidchart) — complete inbound lead path with all stages, touchpoints, conversion metrics, and friction points
- Recommendations document — prioritized list of optimization opportunities with impact/effort estimates
- Lead stage definitions — agreed MQL, SQL, handoff criteria document
- Buyer persona profiles (2-3) — persona-specific journey characteristics

**Technical Deliverables (if Phase 2 applies):**

- Quick-win implementations (2-3 CRM/MAP changes)
- Monitoring dashboard — live conversion funnel + speed-to-lead + drop-off tracking

**Documentation Package:**

- Training video recordings (journey map walkthrough + dashboard navigation)
- Written guides (lead stage definitions, maintenance playbook)
- FAQ document
- Definition Alignment Document (final version)
- Maintenance Schedule

---

## Appendix

### What This Document Is

This is the implementation playbook — the step-by-step execution guide an Architect follows to deliver an Inbound Lead Journey Mapping project from first contact to project close. It is the third file in a 3-file playbook structure: advisory (what the project is), methodology (how we think about the problem), and implementation (what to do).

### What Each Phase Produces

| Phase                    | Output                                                                 | Gate Criteria                                                                  |
| ------------------------ | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **Phase 1: Strategy**    | Journey map + friction analysis + recommendations + definitions         | All stakeholders approved map and definitions                                  |
| **Phase 2: Engineering** | Quick wins implemented + monitoring dashboard                           | Changes tested, dashboard validated, customer approved                          |
| **Phase 3: Enablement**  | Trained team with documentation                                        | All training delivered, hypercare complete, team can operate independently     |
| **Phase 4: Handoff**     | Independent customer + archived project                                | Internal/external handoffs complete, maintenance plan in place, project closed |

### How to Adapt Per Project Type

| Project Profile     | Strategy Weight | Engineering Weight | Enablement Weight | Notes                                                  |
| ------------------- | --------------- | ------------------ | ----------------- | ------------------------------------------------------ |
| **Strategic-heavy** | 60-70%          | 10-20%             | 10-20%            | Inbound Lead Journey Mapping fits here                 |

**Adaptation rules for this project:**

- **Phase 1 (Strategy) is the core** — stakeholder interviews, data analysis, and journey map creation represent the majority of the work
- **Phase 2 (Engineering) is optional and light** — only quick wins + dashboard; no major CRM builds
- **Phase 3 (Enablement) is standard but light** — primarily walkthrough training on artifacts and dashboard
- **Phase 4 always applies** — every project needs handoff, maintenance schedule, and retention path

### Key Industry Benchmarks for Journey Mapping

**Speed-to-Lead:**
- Average B2B response time to new inbound leads: 42 hours [3]
- Only 27% of leads ever get contacted [4]
- Responding within 5 minutes = 21x more likely to qualify vs waiting 30+ minutes [5]
- 78% of customers buy from the business that responds first [3]
- Responding within 1 minute = 391% increase in conversions [6]

**Conversion Benchmarks:**
- Average B2B SaaS MQL→SQL conversion rate: 15-21% [1]
- Top-performing companies (with behavioral scoring): 39-40% [2]
- SEO-sourced leads convert at 51% MQL→SQL vs PPC at 26% [1]
- Website-generated leads convert at 31.3% — more than 2x the overall average [7]

**Multi-Stakeholder Complexity:**
- Typical B2B buying group: 6-10 decision-makers [8]
- Each stakeholder gathers 4-5 independent pieces of information before engaging Sales [8]

---

## References

[1] [2025 B2B SaaS Funnel Benchmarks & Pipeline Audit Framework - The Digital Bloom](https://thedigitalbloom.com/learn/pipeline-performance-benchmarks-2025/)

[2] [MQL to SQL Conversion Rate Benchmarks - Understory Agency](https://www.understoryagency.com/blog/mql-to-sql-conversion-rate-benchmarks)

[3] [What Is Lead Response Time and How It Wins You More Deals - Chili Piper](https://www.chilipiper.com/article/speed-to-lead-statistics)

[4] [We Tested 114 B2B Companies' Lead Response Times - Workato](https://www.workato.com/the-connector/lead-response-time-study/)

[5] [9 Lead Response Time Statistics - Rep.ai](https://rep.ai/blog/lead-response)

[6] [The Impact of Speed to Lead: Response Time Statistics - Kixie](https://www.kixie.com/sales-blog/speed-to-lead-response-time-statistics-that-drive-conversions/)

[7] [2025 Benchmark Report: B2B Software Inbound Conversion Rates - Default](https://www.default.com/reports/inbound-conversion-rates)
