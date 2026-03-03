# Marketing to Sales Handoff and SLA Tracking — Implementation

## Project One-Pager

### Marketing to Sales Handoff and SLA Tracking One-Pager

#### Project Type

- Category: Balanced
- Primary Deliverable: Documented handoff process with automated SLA timers, compliance dashboards, and a closed-loop feedback mechanism between Marketing and Sales

##### Phase Relevance

| Phase          | Applies? | Weight | Notes                                                      |
| -------------- | -------- | ------ | ---------------------------------------------------------- |
| 1. Strategy    | Yes      | Med    | 2-3 alignment loops to lock MQL/SAL/SQL definitions + SLAs |
| 2. Engineering | Yes      | Heavy  | CRM/MAP field config, automation rules, SLA timers, dashboards |
| 3. Enablement  | Yes      | Med    | SDR/AE training on process + dashboards, Marketing on feedback loop |
| 4. Handoff     | Yes      | Med    | Internal + External, maintenance of SLA thresholds ongoing |

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────>│ 2. ENGINEER  │────>│3. ENABLEMENT │────>│  4. HANDOFF  │
  │     Med      │     │    Heavy     │     │     Med      │     │     Med      │
  │ 1a->1b->1c->1d│     │ 2a->2b->2c->2d│     │ 3a->3b->3c->3d│     │ 4a->4b->4c->4d│
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   Align on MQL/SQL     Build automation     Train Sales + Mktg   Document & close
   defs, SLA targets    SLA timers, dashboards  on new process      maintenance plan
```

**This project's flow:**
- Full 4-phase. Strategy focuses on getting Marketing and Sales leadership to agree on shared definitions and SLA targets. Engineering is heavy — CRM field configuration, automation rules, SLA timers, notification workflows, and dashboard builds. Enablement covers SDR/AE training and Marketing Ops feedback loop training. Handoff includes troubleshooting guide and ongoing SLA governance cadence.
- No phases skipped. Some customers compress Phase 1 if they already have agreed MQL/SQL definitions.

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Watch intro video explaining what SLA tracking is and why it matters (include stat: 78% of customers buy from the first responder [1])
- [ ] Complete intake form: current lead stages, CRM platform, response time expectations, existing routing rules
- [ ] Get VP Marketing and VP Sales to review and pre-approve recommended MQL/SAL/SQL definitions
- [ ] Provide CRM and MAP admin access credentials

##### Track B: Architect Prep
- [ ] Pull MQL-to-SQL conversion rates from CRM for last 90 days
- [ ] Audit current lead status picklist values and stage transition rules
- [ ] Measure current average response time to new MQLs (baseline)
- [ ] Quantify lead leakage: leads passed to Sales but never worked
- [ ] Draft v0 SLA framework with recommended response times by lead type
- [ ] Create gap analysis: current handoff points vs. recommended future state

#### Refinement Loop (1b -> 1c -> 1d)

| Meeting      | Sub-Phase | Focus                                          | Stakeholder                        | Output                             |
| ------------ | --------- | ---------------------------------------------- | ---------------------------------- | ---------------------------------- |
| Kickoff      | 1b        | Present v0 SLA framework, validate definitions | VP Marketing, VP Sales, RevOps     | Corrected definitions, info for v1 |
| Refinement 1 | 1c        | Review v1 SLA targets, routing rules, escalation paths | Sales Ops, Marketing Ops, SDR Mgr | v2 with confirmed SLAs             |
| Refinement 2 | 1c        | Finalize field mapping, notification preferences, dashboard requirements | RevOps, Sales Ops                  | v3 ready for sign-off              |
| Sign-Off     | 1d        | Strategic approval of full SLA framework       | All stakeholders                   | Final SLA framework document       |

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held — MQL/SAL/SQL definitions validated
- [ ] 1c. Refinement loop complete (v0 -> vFinal SLA framework)
- [ ] 1d. Strategic sign-off from VP Marketing and VP Sales

##### Phase 2: Engineering
- [ ] 2a. Tech spec created (field mappings, automation logic, SLA timer rules)
- [ ] 2b. Engineering handoff meeting held
- [ ] 2c. Build complete (CRM fields, automation, SLA timers, dashboards)
- [ ] 2d. QA/Test + customer sign-off on all automation and dashboards

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped (SDR guide, dashboard walkthrough, feedback loop doc)
- [ ] 3b. Training sessions delivered to Sales, Marketing Ops, and leadership
- [ ] 3c. Hypercare period complete (2 weeks post-launch)
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff (SME -> Architect) complete
- [ ] 4c. External handoff complete
- [ ] 4d. Project closed and archived

#### Document Types

##### Working Documents (iterate together)

| Document                      | Purpose                                       | When Complete                              |
| ----------------------------- | --------------------------------------------- | ------------------------------------------ |
| Intake form                   | Capture current lead flow, CRM setup, pain points | All fields filled by customer              |
| MQL/SAL/SQL Definition Sheet  | Align on qualification criteria               | Approved by VP Marketing + VP Sales        |
| SLA Framework Document        | Response times, follow-up cadence, escalation rules | All SLA targets signed off                 |
| Gap Analysis Table            | Document current vs. future state             | Gaps prioritized and assigned              |
| CRM Field Mapping Sheet       | Map strategic terms to CRM fields             | All fields mapped, data dictionary updated |

##### Deliverables (polished outputs)

| Deliverable                    | Created From                 | Customer Uses For                           |
| ------------------------------ | ---------------------------- | ------------------------------------------- |
| SLA Compliance Dashboard       | Gap analysis + SLA framework | Real-time monitoring of response times      |
| Handoff Conversion Report      | CRM field mapping            | Funnel reporting MQL -> SAL -> SQL -> Opp   |
| Feedback Loop Report           | SLA framework                | Marketing uses to improve lead quality      |
| Process Flow Diagram           | Gap analysis                 | Internal alignment and onboarding new hires |

#### Enablement Details

##### Training Types

| Type       | Audience                              | Focus                                              | Duration |
| ---------- | ------------------------------------- | -------------------------------------------------- | -------- |
| Leadership | VP Marketing, VP Sales, CRO          | Interpret SLA dashboards, act on compliance trends  | 30 min   |
| Sales      | SDR/AE team, SDR Manager             | Lead handling process, SLA requirements, CRM actions | 45 min   |
| Technical  | RevOps, Marketing Ops, Sales Ops     | Maintain automation, update SLA rules, run reports   | 60 min   |
| Marketing  | Marketing Ops, Demand Gen            | Feedback loop reporting, how to act on rejection data | 30 min   |

##### Hypercare
- Applies: Yes
- Duration: 2 weeks
- Office Hours: Yes — weekly 30-min slot for first 2 weeks post-launch

##### Training Assets to Create
- [ ] Video walkthrough: SLA dashboard walkthrough (for leadership)
- [ ] Video walkthrough: SDR lead handling process and SLA notifications demo
- [ ] Doc: CRM field definitions and status transition rules reference
- [ ] Doc: SLA playbook with response time requirements and escalation paths
- [ ] Doc: FAQ document addressing common questions

#### Handoff & Retention

##### Internal Handoff (SME -> Architect)
- Key context for Architect: SLA thresholds, escalation rules, which automation rules are most fragile (SLA timer pause conditions, business hours configuration)
- Escalation trigger: Any changes to MQL/SQL definition criteria, SLA threshold changes, or new lead source additions requiring routing updates

##### External Handoff
- Final meeting agenda: Review delivered dashboards, walk through SLA governance cadence, confirm maintenance ownership
- Documentation package: SLA playbook, CRM field reference, training video recordings, FAQ, maintenance schedule

##### Maintenance Schedule
- Monthly: Review SLA compliance rates and rejection reason trends
- Quarterly: Revisit MQL/SQL criteria and SLA thresholds based on conversion data
- Who owns: Single project = customer owns | Dedicated = Architect owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services -> if no -> Downsell: Lead Scoring or Lead Routing project -> Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~90 days post-launch
- Internal prep trigger: 2 weeks before
- Decision: Architect handles / SME needed

#### Key Assets

| Asset                         | When Used                |
| ----------------------------- | ------------------------ |
| SLA Framework Template        | Phase 1 Strategy         |
| CRM Field Mapping Template    | Phase 2 Engineering      |
| SLA Dashboard Template        | Phase 2 Engineering      |
| SDR Quick-Reference Guide     | Phase 3 Enablement       |
| Maintenance Schedule Template | Phase 4 Handoff          |

#### Definition Alignment Terms

| Term                    | Typical Definition                                                                                      |
| ----------------------- | ------------------------------------------------------------------------------------------------------- |
| MQL (Marketing Qualified Lead) | A lead that meets firmographic criteria (industry, company size, title) AND has taken a qualifying behavioral action (demo request, content download, webinar attendance) |
| SAL (Sales Accepted Lead)     | A lead that Sales has acknowledged receipt of and committed to working within the SLA timeframe       |
| SQL (Sales Qualified Lead)    | A lead that Sales has validated against BANT or equivalent criteria and confirmed as a real opportunity |
| SLA (Service Level Agreement) | The contractual response time commitment between Marketing and Sales for lead follow-up               |
| Lead Recycling               | The process of returning an unresponsive or unqualified lead from Sales back to Marketing for nurture |
| SLA Breach                   | When a lead has not been contacted within the agreed-upon response time window                         |
| Lead Leakage                 | Leads that are passed to Sales but never worked — they fall through the cracks entirely              |

#### Common Gotchas
- Marketing and Sales spend weeks debating MQL definitions -> Start with data: show which criteria correlate with closed-won deals in the last 90 days, then iterate
- SLA timers calculate based on calendar hours instead of business hours -> Always configure business hours and holiday exclusions BEFORE activating SLA timers
- Lead rejection picklist has too many options, causing low adoption -> Keep to 5-7 rejection reasons maximum. Fewer options = higher completion rates
- SLA notifications go to generic inboxes instead of individual reps -> Route to personal email AND messaging app DM for each assigned rep
- Dashboard filters default to "all time" instead of current period -> Set default date filters to "This Month" or "Last 30 Days" to show actionable data

#### Methodology Options

| Option                         | When to Use                                      | Complexity |
| ------------------------------ | ------------------------------------------------ | ---------- |
| Simple SLA (single timer)      | Small team (&lt;10 reps), one lead type, one SLA target | Low        |
| Tiered SLA (by lead type)      | Multiple lead sources with different urgency levels (demo vs. content) | Medium     |
| Full SLA + Feedback Loop       | Mature orgs wanting closed-loop reporting with lead quality scoring | High       |

---

## Phase 1: Strategy

> **Goal:** Get Marketing and Sales leadership to agree on shared MQL/SAL/SQL definitions, SLA response time targets, and the handoff process design.
>
> **Output:** Signed-off SLA Framework Document + Definition Alignment Document + Gap Analysis.

### 1a. Pre-Kickoff

> Two parallel tracks run after the deal is closed and before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                            | Format             |
| ----------------------------- | ------------------------------------------------------------------ | ------------------ |
| Intro video                   | Explain the cost of slow lead response (42-hour avg response time [2], 78% buy from first responder [1]) and what SLA tracking solves | Video (5-10 min)    |
| Definition Alignment Document | Get VP Marketing + VP Sales to agree on MQL, SAL, SQL definitions pre-kickoff | Google Doc         |
| Pre-filled intake form        | Confirm CRM platform, current lead stages, existing routing rules, team size | Google Form or Doc |

**What we pre-fill:**
- Recommended MQL criteria based on B2B SaaS best practices (firmographics + behavioral triggers)
- Recommended SLA targets by lead type (demo request: 5 min, content download: 4 hours, webinar attendee: 24 hours)
- Common SAL/SQL frameworks (BANT, MEDDIC) for their consideration

**Completion tracking:** Marketing Ops or RevOps follows up. Do not cancel kickoff if incomplete, but push hard — definitions alignment is the #1 blocker for this project type.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                                  | Output                                     |
| ---- | ----------------------------------------------------------------------- | ------------------------------------------ |
| 1    | Pull CRM data: MQL-to-SQL conversion rates, avg response time, lead leakage for last 90 days | Baseline metrics document                  |
| 2    | Audit current lead status picklist values and stage transition rules     | Current state assessment                   |
| 3    | Identify where leads get stuck or fall through (gap analysis)           | Gap analysis with specific bottlenecks     |
| 4    | Analyze CRM data + intake form to build v0 SLA Framework Document       | v0 SLA Framework Document (all values ASSUMED) |
| 5    | Create kickoff call assets: current vs. future state diagram, questions list | Kickoff presentation                       |

**Critical:** Mark everything as ASSUMED. The kickoff call validates. Typical findings include:
- Lead leakage of 30-50% (leads passed but never worked)
- Average response time of 24-72 hours (well above the 5-minute optimal window [3])
- No SLA enforcement mechanism in place
- Lead rejection without feedback (no rejection reason captured)

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building anything.

| Term                          | Our Definition                                                                                     | Internally Approved? |
| ----------------------------- | -------------------------------------------------------------------------------------------------- | -------------------- |
| MQL (Marketing Qualified Lead) | Meets firmographic fit (target industry, company size 50-5000, director+ title) AND qualifying action (demo request, pricing page visit 3x, content download + 2 return visits) | [ ] Yes / [ ] No     |
| SAL (Sales Accepted Lead)     | Sales rep has acknowledged the lead within SLA window and committed to working it                 | [ ] Yes / [ ] No     |
| SQL (Sales Qualified Lead)    | Sales rep has confirmed Budget, Authority, Need, and Timeline via qualifying conversation          | [ ] Yes / [ ] No     |
| Lead Recycling Criteria       | Lead returns to Marketing nurture after 3 contact attempts with no response OR Sales rejects with documented reason | [ ] Yes / [ ] No     |
| SLA Response Time             | Demo requests: 5 min. Content leads: 4 hours. Event/webinar leads: 24 hours.                     | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your Marketing and Sales leadership team. Check "Yes" when approved. We cannot proceed with system configuration until all terms are aligned. Disagreement at this stage is expected — that is what the kickoff call is for.

---

### 1b. Kickoff Call

> **Purpose:** Present v0 SLA Framework and get alignment on definitions, SLA targets, and handoff process design. We walk in with work done — customer reacts, not creates from scratch.

#### Agenda (60-90 min)

| Time  | Topic                        | What Happens                                                    |
| ----- | ---------------------------- | --------------------------------------------------------------- |
| 0-15  | Current state walkthrough    | "Here's what we found: X% lead leakage, Y-hour avg response time" |
| 15-30 | MQL/SAL/SQL definition review | Walk through Definition Alignment Doc, confirm or adjust        |
| 30-45 | SLA targets and routing rules | Present recommended SLAs by lead type, discuss assignment logic  |
| 45-55 | Escalation and recycling rules | Define what happens when SLA breaches, when leads recycle       |
| 55-65 | Dashboard requirements       | What does leadership need to see? What does the SDR manager need? |
| 65-75 | Next steps                   | Schedule refinement, assign homework (data access, stakeholder approvals) |

#### What We Bring

- v0 SLA Framework Document (built in Track B prep)
- Current vs. future state diagram
- Baseline metrics (conversion rates, response times, leakage rate)
- Definition Alignment Document (pre-filled with recommendations)
- Questions list (what we need to validate)

#### What We Leave With

- Confirmed or corrected MQL/SAL/SQL definitions (info needed to create v1)
- Agreement on SLA response time targets (or clear blockers)
- Dashboard requirements captured
- Alignment loop scheduled
- Homework assignments: CRM admin access, stakeholder sign-offs, team roster for routing rules

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Iterate on the SLA Framework Document until sign-off. Typically 2-3 meetings for this project type.

#### The Pattern

```
Kickoff Call (gather info, validate definitions)
    |
SLA Framework Document updated -> v1
    |
Meeting 2 (present v1, refine SLA targets + routing logic) -> v2
    |
Meeting 3 (present v2, finalize escalation rules + dashboard specs) -> v3
    |
Final Review -> Sign-off
```

#### Before Each Meeting

1. Process previous meeting transcript/notes and update SLA Framework Document (v[n-1] -> v[n])
2. Prepare specific questions for next validation round

#### During Each Meeting

1. Walk through updated SLA Framework version
2. Capture corrections and refinements
3. Validate what is now CONFIRMED
4. Identify remaining ASSUMED items

#### After Each Meeting

1. Update SLA Framework Document
2. Track what moved from ASSUMED -> CONFIRMED
3. Update CRM field mapping sheet if definitions changed

#### Meeting Types for This Project

| Meeting Type       | Focus                                                    | Stakeholder                        |
| ------------------ | -------------------------------------------------------- | ---------------------------------- |
| Definition Review  | MQL/SAL/SQL criteria, rejection reasons, recycling rules | VP Marketing, VP Sales, RevOps     |
| Operations Design  | Routing rules, SLA thresholds, notification preferences  | Sales Ops, Marketing Ops, SDR Mgr  |
| Dashboard Design   | What metrics to show, who sees what, drill-down needs    | VP Marketing, VP Sales, RevOps     |
| Final Review       | Full walkthrough of SLA Framework + field mapping        | All stakeholders                   |

#### Typical Timeline

| Milestone               | Timing                           |
| ----------------------- | -------------------------------- |
| Pre-kickoff prep        | 2-3 days                         |
| Kickoff call            | Day 1 of engagement              |
| Meeting loop            | 1-2 weeks (2-3 meetings)         |
| Final review + sign-off | When all definitions CONFIRMED   |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything before building.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by VP Marketing and VP Sales
- [ ] MQL/SAL/SQL criteria documented with specific, measurable thresholds
- [ ] SLA response time targets confirmed by lead type
- [ ] Follow-up cadence (number of touches, spacing) agreed
- [ ] Recycling rules and rejection criteria documented
- [ ] Escalation paths defined (who gets notified at what thresholds)
- [ ] Dashboard requirements captured
- [ ] CRM field mapping complete (strategic term -> CRM field name)
- [ ] No blockers for engineering

#### Decision Point

- **Proceed to Engineering** -> All definitions confirmed, ready to build automation and dashboards
- **Loop back to Strategy** -> Stakeholder disagreement on definitions (common — push for data-driven resolution)

---

## Phase 2: Engineering

> **Goal:** Build and test the CRM/MAP configuration: fields, automation, SLA timers, notifications, and dashboards.
>
> **Output:** Working system with automated handoff, SLA tracking, compliance dashboards, and feedback loop reporting.

| Project Type    | Engineering Weight | This Project                                     |
| --------------- | ------------------ | ------------------------------------------------ |
| Strategic-heavy | Light (10-20%)     | --                                               |
| Balanced        | Medium (40-60%)    | **This project: ~50%** — significant CRM config |
| Technical-heavy | Heavy (70-90%)     | --                                               |

### Sub-Phases

```
2a Tech Spec -> 2b Engineering Handoff -> 2c Build -> 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate the signed-off SLA Framework Document into technical specifications for CRM/MAP configuration.

**Input:** Signed-off SLA Framework Document + CRM Field Mapping Sheet from Phase 1

**Output:** Draft tech spec containing:

- **Field specifications:**
  - Lead Status picklist values: New, MQL, SAL, SQL, Recycled, Disqualified
  - Date/time stamp fields: MQL Date, SAL Date, SQL Date, First Response Date
  - SLA Breach checkbox or formula field
  - Lead Rejection Reason picklist (5-7 values based on alignment meetings)
  - Lead Source / Last Campaign field for feedback loop reporting

- **Automation rules:**
  - MQL qualification trigger (scoring threshold OR specific behavioral criteria)
  - Lead assignment rules (round-robin, territory-based, or account-based)
  - Stage transition automation (auto-stamp dates on status changes)
  - SLA timer start trigger (MQL Date or assignment timestamp)

- **SLA timer configuration:**
  - Timer rules by lead type (demo: 5 min, content: 4 hours, event: 24 hours)
  - Business hours and holiday exclusions
  - Tiered notifications: 50% elapsed, 80% elapsed, SLA breached
  - Escalation to manager on breach

- **Dashboard and report specs:**
  - SLA Compliance Dashboard: response time distribution, compliance rate by rep/team, trending over time
  - Handoff Conversion Report: MQL -> SAL -> SQL -> Opportunity funnel with conversion rates and cycle times
  - Feedback Loop Report: rejection reasons by volume and trend, lead quality by source/campaign

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs with engineer before building.

**Who attends:** Architect + Engineer (or engineering team)

**Agenda (30-45 min):**

| Time  | Topic              | What Happens                                                        |
| ----- | ------------------ | ------------------------------------------------------------------- |
| 0-15  | Walk through specs | Architect explains SLA Framework context + tech spec                |
| 15-30 | Engineer questions | Clarify CRM-specific implementation details, flag risks             |
| 30-45 | Refine and approve | Adjust specs, confirm build sequence, agree on QA approach          |

**What Architect brings:**

- SLA Framework Document (for strategic context)
- Draft tech spec (from 2a)
- CRM field mapping sheet
- Questions list (anything flagged as unclear)

**What engineer leaves with:**

- Approved tech spec
- Clear build sequence: fields first -> automation -> SLA timers -> dashboards
- Known risks: business hours configuration complexity, SLA timer pause conditions, data migration for retroactive baseline

---

### 2c. Build (Configure)

> **Purpose:** Build/configure the handoff system in the customer's CRM and MAP.

**Input:** Approved tech spec from 2b

**Build sequence:**

**Step 1: CRM Field Configuration**
- Create or update Lead Status picklist (New, MQL, SAL, SQL, Recycled, Disqualified)
- Add date/time stamp fields: MQL Date, SAL Date, SQL Date, First Response Date
- Create SLA Breach checkbox or formula field (calculated from MQL Date vs. First Response Date vs. SLA target)
- Configure Lead Rejection Reason picklist (5-7 options from Phase 1 alignment)
- Document all field definitions in data dictionary

**Step 2: Handoff Automation Rules**
- Build MQL qualification automation based on scoring threshold or trigger criteria defined in Phase 1
- Configure lead assignment rules (round-robin via Salesforce Lead Assignment Rules or HubSpot Rotate Leads action, territory-based via LeanData, or account-based)
- Set up auto-assignment to SDR queues or specific reps
- Create workflow to stamp MQL Date when lead qualifies
- Build SAL transition rule: when rep changes status to SAL, stamp SAL Date and stop SLA timer
- Build SQL transition rule: when rep confirms qualification, stamp SQL Date
- Build recycling automation: after X failed contact attempts or Sales rejection, return to Marketing with status = Recycled

**Step 3: SLA Timer and Notifications**
- Configure SLA timer starting from MQL Date (or assignment timestamp)
- Set up tiered notifications:
  - 50% of SLA elapsed: Gentle reminder to assigned rep via messaging app + email
  - 80% of SLA elapsed: Urgent alert to rep + cc SDR manager
  - SLA breached: Manager notification + lead reassignment queue (if configured)
- Route notifications via email AND messaging app integration (using native integrations or tools like Chilipiper)
- Configure business hours and holiday exclusions for SLA calculations [4]
- Set up pause conditions: SLA timer pauses if lead responds or if status changes to SAL

**Step 4: Dashboard and Report Build**
- Build SLA Compliance Dashboard:
  - Response time distribution chart (under SLA, approaching, breached)
  - SLA compliance rate by SDR/AE and by team
  - Trending view of SLA performance over time (week-over-week)
  - Drill-down capability to individual lead records
  - Filters: date range, lead source, lead owner, team
- Build Handoff Conversion Report:
  - Funnel visualization: MQL -> SAL -> SQL -> Opportunity
  - Conversion rates at each stage
  - Average cycle time between stages
  - Lead source performance by conversion rate
- Build Feedback Loop Report:
  - Rejection reasons by volume and trend
  - Lead quality score: SAL acceptance rate by source/campaign
  - Which campaigns produce highest SQL conversion
  - Scheduled weekly digest to Marketing Ops

**Execution approaches:**

| Approach       | When to Use                                          | Example                                  |
| -------------- | ---------------------------------------------------- | ---------------------------------------- |
| Manual build   | First implementation, complex routing logic           | Engineer builds in Salesforce/HubSpot directly |
| Tool-assisted  | Complex routing with LeanData or Chilipiper           | LeanData handles territory-based assignment |

**Build tracking:**

- [ ] Component 1: Lead Status picklist and date fields
- [ ] Component 2: MQL qualification automation
- [ ] Component 3: Lead assignment rules
- [ ] Component 4: SLA timer configuration with business hours
- [ ] Component 5: Tiered notification workflows
- [ ] Component 6: SAL/SQL transition automation
- [ ] Component 7: Recycling automation
- [ ] Component 8: SLA Compliance Dashboard
- [ ] Component 9: Handoff Conversion Report
- [ ] Component 10: Feedback Loop Report

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify the handoff system works end-to-end and get customer approval.

**Two types of testing:**

| Type              | Who      | Purpose                                                         |
| ----------------- | -------- | --------------------------------------------------------------- |
| Technical Testing | Our team | Verify automation fires, SLA timers calculate correctly, dashboards render |
| Customer Testing  | Customer | Verify the process matches their expectations and workflows     |

**Technical testing checklist:**

- [ ] Create test lead -> confirm MQL automation fires and stamps MQL Date
- [ ] Verify lead assignment routes to correct rep (test each rule: round-robin, territory, etc.)
- [ ] Confirm SLA timer starts correctly on MQL Date
- [ ] Verify notification at 50% SLA elapsed (test with shortened timer for QA)
- [ ] Verify notification at 80% SLA elapsed
- [ ] Verify SLA breach notification fires and escalates to manager
- [ ] Test SLA timer pause when lead responds or status changes to SAL
- [ ] Test SLA calculation uses business hours (not calendar hours) [4]
- [ ] Verify SAL Date stamps when rep accepts lead
- [ ] Verify SQL Date stamps when rep qualifies lead
- [ ] Test recycling automation: lead returns to Marketing after rejection
- [ ] Verify rejection reason field is required on status change to Recycled/Disqualified
- [ ] Confirm all dashboard data populates correctly with test data
- [ ] Verify dashboard filters work (date range, lead source, owner)
- [ ] Test scheduled report delivery for feedback loop digest

**Customer testing:**

- Walk customer through a complete lead handoff scenario
- Have SDR manager test SLA notifications (receive alert, take action)
- Have Marketing Ops review feedback loop report with real data
- Capture feedback, fix issues

**Engineering sign-off checkpoint:**

- [ ] All automation rules firing correctly
- [ ] SLA timers calculating with business hours
- [ ] All dashboards rendering with correct data
- [ ] Notifications reaching correct recipients via correct channels
- [ ] Customer has tested and approved
- [ ] Ready for enablement

**Decision point:**

- **Proceed to Enablement** -> System is built, needs training/adoption
- **Loop back to Build** -> Issues found, needs fixes

---

## Phase 3: Enablement

> **Goal:** Sales and Marketing teams can actually use the new handoff process and dashboards.
>
> **Output:** Trained team with documentation, stabilized system, no critical issues.

### Sub-Phases

```
3a Training Prep -> 3b Training Sessions -> 3c Hypercare -> 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from the SLA Framework Document, tech specs, and built system.

**Input:** SLA Framework Document + tech specs + built system screenshots

**Output:** Training package containing:

- **Video walkthrough scripts:**
  - Leadership: SLA Compliance Dashboard walkthrough — how to read compliance trends, when to escalate
  - SDR/AE: Lead handling process — what happens when you get an MQL, how to respond within SLA, how to accept/reject/recycle
  - Marketing Ops: Feedback loop reporting — how to read rejection reasons, how to act on lead quality data

- **Written guides:**
  - SDR Quick-Reference Card: Lead status definitions, SLA requirements per lead type, CRM actions required at each step
  - CRM Field Reference: All new fields, their purpose, valid values
  - Process Flow Diagram: Visual showing the complete handoff from MQL -> SAL -> SQL -> Opportunity (or Recycled)

- **FAQ draft:**
  - "What happens if I miss my SLA?" -> Notification goes to your manager, lead may be reassigned
  - "When does the SLA timer pause?" -> When lead responds or you change status to SAL
  - "How do I reject a lead?" -> Change status to Recycled, rejection reason field is required
  - "Who sees my SLA performance?" -> Your manager and leadership via the SLA Compliance Dashboard

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to Sales, Marketing, and leadership teams.

**Training schedule:**

| Session | Audience                    | Focus                                                              | Duration | Timing           |
| ------- | --------------------------- | ------------------------------------------------------------------ | -------- | ---------------- |
| 1       | SDR/AE team + SDR Manager   | Lead handling process, SLA requirements, CRM actions, notifications | 45 min   | Day 1 of go-live |
| 2       | Marketing Ops, Demand Gen   | Feedback loop reporting, how to act on rejection data, quality scoring | 30 min   | Day 1 of go-live |
| 3       | VP Marketing, VP Sales, CRO | Dashboard walkthrough, SLA trends, how to use data in 1:1s         | 30 min   | Day 2 of go-live |
| 4       | RevOps, Sales Ops           | System maintenance, how to adjust SLA rules, run ad-hoc reports    | 60 min   | Day 2 of go-live |

**Training delivery:**

1. Record all sessions as video walkthroughs for future reference and new hire onboarding
2. Distribute SDR Quick-Reference Card to every SDR/AE
3. Answer questions live, note gaps for FAQ updates
4. Demo a real lead flowing through the system end-to-end during SDR training

**Output:**

- Trained stakeholders across all four audiences
- Video recordings for each session
- Questions log (feeds into FAQ updates)
- Any identified gaps or concerns documented

---

### 3c. Hypercare

> **Purpose:** Intensive post-launch support to stabilize the handoff system and catch issues early.

**Duration:** 2 weeks

**What happens:**

- Monitor SLA compliance rates daily for the first week
- Quick response to automation errors or notification issues
- Office hours: weekly 30-min slot where anyone can join and report issues
- Common hypercare issues for this project type:
  - SLA timer not pausing correctly when leads respond
  - Notifications routing to wrong channel
  - Business hours misconfigured (timezone issues)
  - Reps not seeing the rejection reason field as required
  - Dashboard showing stale data due to report refresh timing

**When to skip:** This project type always needs hypercare. SLA enforcement changes daily behavior — teams need support adjusting.

**Output:** Stabilized system, no critical issues outstanding, SLA compliance trending above 70% in first 2 weeks

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm customer team can operate the handoff process independently.

**Validation checkpoint:**

- [ ] All four training sessions delivered
- [ ] Training recordings and documentation provided
- [ ] Hypercare period complete — no critical issues outstanding
- [ ] SDR team demonstrating >70% SLA compliance in first 2 weeks
- [ ] Marketing Ops receiving and acting on weekly feedback digest
- [ ] Leadership accessing dashboards without assistance
- [ ] RevOps can adjust SLA thresholds and run reports independently
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** -> Customer is enabled, system stabilized
- **Extend Hypercare** -> SLA compliance below 70%, automation issues persist, or teams still confused on process

---

## Phase 4: Handoff

> **Goal:** Clean project close with maintenance plan established and retention/expansion path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the system, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule -> 4b Internal Handoff -> 4c External Handoff -> 4d Project Close
                          (SME -> Architect)            (-> Customer)       (Archive + Debrief)
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At                                                                         |
| ----------------------------- | -------------------- | ------------------------------------------------------------------------------------- |
| **Single Project**            | Customer owns        | 4c (External Handoff) — customer receives maintenance schedule and runs it themselves |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) — Architect receives maintenance schedule and runs it for customer |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention after go-live — cadences, tasks, triggers for re-engagement.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task                  | What to Check                                                 | Red Flag Threshold                                |
| ----------------------------- | ------------------------------------------------------------- | ------------------------------------------------- |
| SLA Compliance Review         | Overall compliance rate, by-rep compliance, breach trends     | Compliance drops below 80% for any team           |
| Response Time Trending        | Average response time by lead type vs. SLA target             | Avg response time exceeding 2x SLA target         |
| Rejection Reason Analysis     | Top rejection reasons by volume, new patterns emerging        | Any single rejection reason >40% of total rejects |
| Lead Leakage Check            | Leads in MQL status for >7 days with no activity              | >10% of MQLs showing no Sales activity            |
| Dashboard Usage Audit         | Are stakeholders actually using the dashboards?               | &lt;50% of leadership accessing dashboard monthly    |

**Quarterly Tasks:**

| Quarterly Task                    | What to Review                                          | Action if Off-Track                                  |
| --------------------------------- | ------------------------------------------------------- | ---------------------------------------------------- |
| MQL Criteria Validation           | Are MQL criteria still correlating with closed-won?     | Adjust criteria based on last quarter's conversion data |
| SLA Threshold Review              | Are SLA targets realistic given current team capacity?  | Tighten if consistently hitting, loosen if >20% breach rate |
| Conversion Funnel Analysis        | MQL->SAL->SQL->Opp rates vs. baseline and benchmarks   | Investigate bottleneck stage, adjust process          |
| Sales-Marketing Alignment Check   | Are both teams satisfied with lead quality and follow-up? | Hold alignment meeting, adjust definitions if needed |

**After First Business Cycle (30-90 days post-launch):**

- Pull SLA compliance metrics for first 30 days and compare to zero baseline
- Calculate MQL-to-SQL conversion rate vs. pre-project baseline (benchmark: B2B SaaS average is 15-21% [5], top performers reach 40% [6])
- Review rejection reasons and lead quality feedback — are the right leads being passed?
- Gather qualitative feedback from SDRs: "Are you getting better leads? Is the process working?"
- Key question: Has response time improved? Target is >50% reduction from pre-project baseline

**Refinement Triggers (when to re-engage):**

| Trigger                        | Threshold                                    | Response                                                |
| ------------------------------ | -------------------------------------------- | ------------------------------------------------------- |
| SLA compliance drop            | Below 70% for 2+ consecutive months          | Investigate root cause, adjust thresholds or escalation |
| MQL-to-SQL conversion decline  | >5 point drop from post-launch baseline      | Review MQL criteria with Marketing, audit lead quality  |
| Lead leakage increase          | >15% of MQLs unworked                        | Audit assignment rules, check for routing errors        |
| Sales rejection spike          | Rejection rate >50% for 2+ months            | Re-examine MQL criteria, hold alignment meeting         |

**Every 6-12 Months:**

- Full SLA framework review: Are response time targets still appropriate given team growth, new products, market changes?
- MQL criteria recalibration with fresh conversion data
- Evaluate if new lead types or channels need separate SLA tiers
- Assess whether feedback loop is driving measurable improvement in lead quality
- Review competitive response time benchmarks (78% of deals go to the first responder [1])

---

### 4b. Internal Handoff (SME -> Architect)

> **Purpose:** Transfer context so Architect can manage ongoing relationship.

**What the Architect needs to know:**

- SLA Framework Document: definitions, thresholds, escalation rules
- Which automation rules are most fragile: SLA timer pause conditions, business hours configuration (timezone edge cases), round-robin assignment (what happens when a rep is OOO)
- Dashboard access: who has access, who checks it regularly
- Common issues and how to resolve (see troubleshooting guide below)

**Escalation guidelines:**

| Issue Type                                    | Who Handles                                   | Examples                                                  |
| --------------------------------------------- | --------------------------------------------- | --------------------------------------------------------- |
| Small tweaks, minor questions                 | Architect                                      | Adding a new rep to rotation, adjusting dashboard filter  |
| Definition changes, structural modifications  | SME                                            | Changing MQL criteria, adding new SLA tier, restructuring routing logic |

**For Dedicated engagements:** Architect receives the maintenance schedule (4a) and becomes responsible for executing monthly and quarterly tasks. SME walks Architect through each maintenance task.

---

### 4c. External Handoff (-> Customer)

> **Purpose:** Formal project completion with customer.

**Final project meeting:**

- Review what was delivered: fields, automation, SLA timers, dashboards, reports
- Walk through documentation package
- Demo the maintenance tasks: how to check SLA compliance monthly, how to run quarterly reviews
- Confirm nothing outstanding
- Answer final questions
- Make it explicit: "Project complete"
- **For Single Project engagements:** Walk customer through maintenance schedule in detail. Record a video walkthrough.

**Documentation package:**

- SLA Playbook: response time requirements, escalation paths, process flow
- CRM Field Reference: all fields, definitions, valid values
- SDR Quick-Reference Card
- Training video recordings (all 4 sessions)
- FAQ document
- Definition Alignment Document (final version)
- Maintenance Schedule (for Single Project — this becomes customer's responsibility)
- Troubleshooting Guide (see below)

**Troubleshooting Guide:**

| Scenario                                   | Symptoms                                           | Resolution                                                     |
| ------------------------------------------ | -------------------------------------------------- | -------------------------------------------------------------- |
| SLA timer not starting                     | Lead moves to MQL but no timer visible             | Check MQL automation fired correctly, verify MQL Date stamped  |
| Notifications not reaching reps            | Reps report not seeing SLA alerts                  | Verify messaging integration active, check email delivery     |
| SLA calculating on calendar hours          | Weekend leads showing as breached on Monday        | Reconfigure SLA formula to use business hours, check timezone   |
| Dashboard showing stale data               | Numbers do not match recent lead activity           | Check report refresh schedule, verify field-level security     |
| Rejection reason field not required         | Reps changing to Recycled without providing reason | Update page layout/validation rule to enforce required field    |
| Round-robin skipping reps                  | Some reps getting 2x leads, others getting none    | Check assignment rules, verify all reps active in rotation      |
| Lead stuck in MQL with no activity         | Lead assigned but no first touch logged            | Check assignment notification, verify rep has access to lead    |
| SLA breach not escalating                  | Timer shows breached but manager not notified      | Verify escalation workflow active, check manager field populated |

**Output:** Customer owns the system. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location
- [ ] Handoff documentation complete
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized

#### Internal Debrief (Optional but Recommended)

- What went well? (e.g., definitions aligned faster than expected, dashboard adoption strong)
- What would we do differently? (e.g., should have configured business hours earlier in build phase)
- Any learnings to feed back into SOPs or future projects? (e.g., common rejection reasons to pre-populate)

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell -> Downsell -> Retry  |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (retainer -- ongoing SLA governance + optimization)
   | if no
2. Downsell: Lead Scoring project (natural next step to improve MQL quality)
   | if no
3. Downsell: Lead Routing project (optimize assignment beyond round-robin)
   | if yes to any
4. Retry retainer at end of next project cycle
```

**Script:**

> "Now that your SLA tracking is live, there are two ways we can continue working together. Option 1: We can set you up on managed services where we handle ongoing SLA governance, quarterly optimization, and MQL criteria tuning. Option 2: If you want to improve the quality of leads hitting the SLA — which directly affects conversion rates — we can scope a Lead Scoring project. Which sounds more interesting?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On [date ~90 days out], we'll review your SLA compliance trends, conversion rate improvements, and see if any MQL criteria or SLA thresholds need adjusting."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                                      |
| ------------------- | ----------------------------------------------------------------- |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks                  |
| 2. Review metrics   | Pull SLA compliance, conversion rates, rejection trends           |
| 3. Decide ownership | Can Architect handle this check-in, or need SME?                  |
| 4. Prep materials   | If SME needed, brief them. If Architect, prep talking points.     |

**At the refinement check-in:**

- Review SLA compliance vs. 30-day post-launch baseline
- Review MQL-to-SQL conversion rate improvement
- Identify any MQL criteria or SLA threshold adjustments needed
- If minor: Architect handles tweaks
- If major (e.g., need to rebuild scoring model, add new SLA tiers): Scope new project

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- SLA Framework Document: definitions, response time targets, escalation rules, recycling criteria
- Definition Alignment Document: agreed MQL/SAL/SQL definitions signed by VP Marketing + VP Sales
- Gap Analysis: current state vs. future state with prioritized changes

**Technical Deliverables:**

- CRM field configurations: Lead Status picklist, date stamps, SLA Breach field, Rejection Reason
- Automation rules: MQL qualification, lead assignment, stage transitions, recycling
- SLA timer configuration with business hours, tiered notifications, and escalation
- SLA Compliance Dashboard (real-time, filtered by rep/team/source/date)
- Handoff Conversion Report (MQL -> SAL -> SQL -> Opp funnel with conversion rates)
- Feedback Loop Report (rejection reasons, lead quality by source/campaign)

**Documentation Package:**

- Training video recordings (4 sessions)
- SDR Quick-Reference Card
- CRM Field Reference
- SLA Playbook
- FAQ document
- Definition Alignment Document (final version)
- Maintenance Schedule
- Troubleshooting Guide

---

## Appendix

### What Each Phase Produces

| Phase                    | Output                                                                 | Gate Criteria                                                                  |
| ------------------------ | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **Phase 1: Strategy**    | Signed-off SLA Framework Document + Definition Alignment Document      | VP Marketing + VP Sales have approved definitions and SLA targets             |
| **Phase 2: Engineering** | Built CRM fields, automation, SLA timers, dashboards                   | All automation firing, dashboards rendering, customer approved                 |
| **Phase 3: Enablement**  | Trained Sales + Marketing teams with documentation                     | All training delivered, hypercare complete, >70% SLA compliance               |
| **Phase 4: Handoff**     | Independent customer + archived project                                | Internal/external handoffs complete, maintenance plan in place, project closed |

### Project Profile

This project is **Balanced** — significant strategy work (aligning two departments on definitions and SLAs) combined with substantial engineering work (automation, timers, dashboards). Enablement is meaningful because it changes daily behavior for SDRs and AEs.

| Project Profile       | Strategy Weight | Engineering Weight | Enablement Weight | This Project |
| --------------------- | --------------- | ------------------ | ----------------- | ------------ |
| **Strategic-heavy**   | 60-80%          | 10-20%             | 10-20%            |              |
| **Balanced**          | 30-40%          | 30-40%             | 20-30%            | **&lt;--**      |
| **Engineering-heavy** | 10-20%          | 60-80%             | 10-20%            |              |
| **Enablement-heavy**  | 20-30%          | 20-30%             | 40-50%            |              |

### Engagement Types

| Engagement Type               | What It Means                        | Key Difference                              |
| ----------------------------- | ------------------------------------ | ------------------------------------------- |
| **Single Project**            | One-off project engagement           | Customer owns maintenance post-handoff (4c) |
| **Dedicated (Multi-Project)** | Ongoing retainer / multiple projects | Architect owns maintenance post-handoff (4b) |

### Phase Guides

#### Phase 1: Strategy — Key Principles

**We educate.** Most B2B companies do not know that their average response time is 42 hours [2], or that 78% of deals go to the first responder [1]. Educate them on the cost of slow response first — then they can make informed decisions about SLA targets.

**We drive alignment.** The biggest blocker in this project is disagreement between Marketing and Sales on what constitutes a qualified lead. Push them to define MQL/SAL/SQL with specific, measurable criteria — no vague language allowed. The Definition Alignment Document is the forcing function.

**We come with an opinion.** Show up with recommended SLA targets (demo: 5 min, content: 4 hours) based on B2B SaaS benchmarks. They are confirming and adjusting, not creating from scratch.

**We show best practices.** Anchor everything in benchmarks: average MQL-to-SQL conversion rates (15-21% [5], top performers at 40% [6]), industry SLA standards.

**Why Definition Alignment Matters:** Projects stall when Marketing says "we sent 500 MQLs" and Sales says "only 50 were real." Getting sign-off on MQL/SAL/SQL criteria BEFORE building anything prevents this. CRM baseline data grounds the conversation in reality, not opinions.

#### Phase 2: Engineering — Key Principles

**Tech Spec (2a):** Translate SLA Framework Document into CRM-specific configuration. Human reviews and confirms field names, automation trigger logic, and business hours settings.

**Engineering Handoff (2b):** Engineer must understand WHY each SLA threshold was chosen (strategic context) — not just the WHAT (timer configuration). This prevents engineers from making "obvious" simplifications that break the strategic intent.

**Build (2c):** Build fields and status values first. Then automation. Then SLA timers. Then dashboards. This sequence matters because dashboards depend on data from automation, and automation depends on fields existing. Common build risk: business hours configuration is deceptively tricky — timezone differences between reps, holiday calendars, and DST changes all create edge cases [4].

#### Phase 3: Enablement — Key Principles

**Training Prep (3a):** Key insight: SDR training must be hands-on with live demo of a lead flowing through the system — do not just show slides.

**Training Sessions (3b):** Separate sessions by audience. SDR/AE session focuses on "what do I do when I get an MQL alert?" Leadership session focuses on "how do I read this dashboard?" Do not mix — different concerns, different depth.

**Hypercare (3c):** Office hours pattern works well for this project type. First week is the riskiest — most automation bugs surface when real lead volume hits the system. Monitor daily for the first 5 business days.

#### Phase 4: Handoff — Key Principles

**Why Maintenance Schedules Matter:** SLA systems drift over time. MQL criteria that worked 6 months ago may no longer correlate with closed-won deals as the product or market shifts. SLA thresholds set for a 10-person SDR team become too aggressive when the team grows to 25. The maintenance schedule prevents drift by making monitoring explicit and cadenced.

**Internal Handoff — When to Escalate:**
- Architect handles: adding new rep to rotation, adjusting dashboard filters, updating a single SLA threshold, onboarding new hires to the process
- SME handles: changing MQL qualification criteria, restructuring routing logic, adding new SLA tiers for new lead types, integrating new lead sources, responding to dramatic conversion rate changes

**Retention — Natural Expansion Paths:** Once SLA tracking is in place, customers naturally want:
1. **Lead Scoring** — improve the quality of leads hitting the SLA (directly improves conversion rates)
2. **Lead Routing** — optimize assignment beyond round-robin (territory, account-based, capacity-weighted)
3. **Managed Services** — ongoing SLA governance, quarterly optimization, MQL criteria tuning

---

## References

[1] [Chili Piper - Speed to Lead Statistics](https://www.chilipiper.com/article/speed-to-lead-statistics)
[2] [Workato - Lead Response Time Study](https://www.workato.com/the-connector/lead-response-time-study/)
[3] [Rep.ai - Lead Response Time Statistics](https://rep.ai/blog/lead-response)
[4] [Salesforce Help - Business Hours in SLA Management](https://help.salesforce.com/s/articleView?id=service.sla_policy_business_hours.htm&language=en_US&type=5)
[5] [The Digital Bloom - 2025 B2B SaaS Funnel Benchmarks](https://thedigitalbloom.com/learn/pipeline-performance-benchmarks-2025/)
[6] [Understory - MQL to SQL Conversion Rate Benchmarks](https://www.understoryagency.com/blog/mql-to-sql-conversion-rate-benchmarks)
