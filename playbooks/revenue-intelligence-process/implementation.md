# Revenue Intelligence Process — Implementation

## Project One-Pager

### Revenue Intelligence Process One-Pager

#### Project Type

- Category: Technical
- Primary Deliverable: Fully operational revenue intelligence system with conversation capture, deal scoring, pipeline analytics dashboards, forecast submission workflow, and coaching scorecards

##### Phase Relevance

| Phase          | Applies? | Weight | Notes                                                    |
| -------------- | -------- | ------ | -------------------------------------------------------- |
| 1. Strategy    | Yes      | Medium | 2-4 alignment meetings; platform selection, success criteria, baseline metrics |
| 2. Engineering | Yes      | Heavy  | Core platform config, CRM sync, recording integrations, deal scoring, dashboards |
| 3. Enablement  | Yes      | Medium | Manager training, rep training, RevOps admin handoff     |
| 4. Handoff     | Yes      | Medium | Deal review cadence docs, forecast process, 30/90-day follow-up |

· · ·

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │    Medium    │     │    Heavy     │     │    Medium    │     │    Medium    │
  │ 1a→1b→1c→1d │     │ 2a→2b→2c→2d │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   Assess current       Platform config     Manager + rep        Deal review cadence
   state, baselines,    CRM sync, recording training, admin      forecast process,
   platform selection   deal scoring, dash  handoff, hypercare   troubleshooting
```

**This project's flow:**
- Full 4-phase execution. Heavy engineering with platform configuration, CRM integration, recording setup, deal scoring rules, pipeline dashboards, and forecast workflows. Strategy establishes baselines and platform selection. Enablement covers three audiences (managers, reps, admins). Handoff includes ongoing cadence documentation and adoption follow-up.
- No phases skipped. Some customers may compress Phase 1 if platform is already selected (e.g., Gong already procured).

· · ·

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Watch intro video explaining what revenue intelligence is and how it transforms deal visibility
- [ ] Complete intake form: current tech stack, recording tools, CRM details, sales process stages, team roster
- [ ] Provide CRM admin access (Salesforce/HubSpot) with read/write permissions
- [ ] Provide admin access to video conferencing platform (Zoom/Teams/Meet)
- [ ] Confirm legal/compliance approval for call recording (one-party vs. two-party consent)
- [ ] Share last 4 quarters of forecast vs. actual data for baseline measurement

##### Track B: Architect Prep
- [ ] Pull call recording stats from existing dialer system (if any) for last 90 days
- [ ] Audit CRM data quality: duplicate accounts, missing fields, inconsistent stage definitions
- [ ] Document current tech stack inventory: CRM, dialer, video conferencing, email, calendar
- [ ] Assess current forecast accuracy by rep, team, and segment
- [ ] Prepare gap analysis showing conversation capture rate by channel

· · ·

#### Refinement Loop (1b -&gt; 1c -&gt; 1d)

| Meeting      | Sub-Phase | Focus                                                     | Stakeholder                    | Output                              |
| ------------ | --------- | --------------------------------------------------------- | ------------------------------ | ----------------------------------- |
| Kickoff      | 1b        | Present current state audit, validate gaps, align on goals | VP Sales/CRO, RevOps Lead     | Validated gap analysis, success criteria |
| Alignment 1  | 1c        | Review platform options, confirm integration requirements  | RevOps Lead, IT/Security       | Platform recommendation, integration map |
| Alignment 2  | 1c        | Finalize deal scoring rules, dashboard requirements        | VP Sales, Sales Managers       | Scoring criteria, dashboard specs   |
| Sign-Off     | 1d        | Approve platform choice, success criteria, and build plan  | CRO/VP Sales, RevOps Lead     | Signed-off strategic package        |

· · ·

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held
- [ ] 1c. Refinement loop complete (platform selected, scoring rules defined)
- [ ] 1d. Strategic sign-off obtained

##### Phase 2: Engineering
- [ ] 2a. Tech spec created (field mappings, integration specs, scoring rules)
- [ ] 2b. Engineering handoff meeting held
- [ ] 2c. Build complete (platform, CRM sync, recordings, scoring, dashboards, forecasting)
- [ ] 2d. QA/Test + customer sign-off

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped (manager guide, rep guide, admin runbook)
- [ ] 3b. Training sessions delivered (managers, reps, RevOps admin)
- [ ] 3c. Hypercare period complete (2 weeks)
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff (SME -&gt; Architect) complete
- [ ] 4c. External handoff (implementation team -&gt; Customer) complete
- [ ] 4d. Project closed and archived

· · ·

#### Document Types

##### Working Documents (iterate together)

| Document                     | Purpose                                          | When Complete                              |
| ---------------------------- | ------------------------------------------------ | ------------------------------------------ |
| Intake form                  | Capture tech stack, team roster, recording status | All fields filled by customer              |
| Gap analysis                 | Show capture rate by channel, identify blind spots | Validated by VP Sales in kickoff           |
| Baseline metrics document    | 4 quarters of forecast accuracy, win rates, cycle length | All historical data pulled and verified |
| Integration requirements map | API/auth requirements per system                 | Confirmed by IT/RevOps                     |
| Platform evaluation matrix   | Compare Gong, Clari, Chorus, etc.                | Platform selected and approved             |

##### Deliverables (polished outputs)

| Deliverable                  | Created From              | Customer Uses For                          |
| ---------------------------- | ------------------------- | ------------------------------------------ |
| Platform configuration doc   | Integration map + build   | Reference for admin maintenance            |
| Dashboard suite              | Gap analysis + scoring rules | Weekly deal reviews, forecast calls       |
| Deal review playbook         | Scoring rules + dashboards | Standardized manager-led deal inspections  |
| Coaching scorecard reference | Top performer benchmarks  | Rep development and 1:1 coaching           |

· · ·

#### Enablement Details

##### Training Types

| Type       | Audience                       | Focus                                                         | Duration |
| ---------- | ------------------------------ | ------------------------------------------------------------- | -------- |
| Leadership | VP Sales, CRO, Sales Managers  | Deal inspection workflow, dashboard navigation, coaching scorecards, forecast submission | 60 min   |
| Rep        | Sales Reps                     | What's recorded, privacy settings, self-coaching with call insights | 30 min   |
| Technical  | RevOps/Sales Ops Admin         | User provisioning, permission management, integration monitoring, troubleshooting | 60-90 min |

##### Hypercare
- Applies: Yes
- Duration: 2 weeks
- Office Hours: Yes -- weekly 30-min slot for questions and issue triage

##### Training Assets to Create
- [ ] Video walkthrough: Dashboard navigation (rep, manager, executive views)
- [ ] Video walkthrough: Deal review meeting process using live data
- [ ] Video walkthrough: Admin platform walkthrough (user management, integration monitoring)
- [ ] Doc: Deal review meeting agenda template
- [ ] Doc: Admin runbook (user provisioning, troubleshooting, sync monitoring)
- [ ] Doc: Rep FAQ addressing privacy and monitoring concerns

· · ·

#### Handoff & Retention

##### Internal Handoff (SME -&gt; Architect)
- Key context for Architect: Platform configuration details, CRM field mappings, scoring rule calibration rationale, customer-specific compliance requirements
- Escalation trigger: Any changes to deal scoring logic, new CRM integration requests, platform API changes

##### External Handoff (Implementation Team -&gt; Customer)
- Final meeting agenda: Review delivered system, walk through documentation package, confirm deal review and forecast cadences, schedule 30-day and 90-day follow-ups
- Documentation package: Config settings, admin runbook, training recordings, deal review playbook, forecast cadence calendar

##### Maintenance Schedule
- Monthly: Dashboard usage audit, deal scoring accuracy spot-check, recording coverage verification
- Quarterly: Scoring rule recalibration, forecast accuracy trend review, feature adoption assessment
- Who owns: Single project = customer owns | Dedicated = Architect owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services -&gt; if no -&gt; Downsell: Another project (e.g., Sales Qualification Methodology, Forecasting Process) -&gt; Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~1 quarter after go-live
- Internal prep trigger: 2 weeks before check-in
- Decision: Architect handles scoring recalibration / SME needed for structural changes

· · ·

#### Key Assets

| Asset                        | When Used     |
| ---------------------------- | ------------- |
| Platform evaluation matrix   | Phase 1       |
| Integration requirements map | Phase 1-2     |
| Deal scoring rules document  | Phase 2       |
| Dashboard specs              | Phase 2       |
| Deal review playbook         | Phase 3-4     |
| Admin runbook                | Phase 3-4     |
| Forecast cadence calendar    | Phase 3-4     |

· · ·

#### Definition Alignment Terms

| Term                     | Typical Definition                                                                 |
| ------------------------ | ---------------------------------------------------------------------------------- |
| Conversation Intelligence | AI-powered analysis of recorded sales conversations to surface insights, coaching opportunities, and deal signals |
| Deal Risk Score          | Composite score indicating likelihood a deal will slip or be lost, based on conversation signals and CRM activity patterns |
| Pipeline Analytics       | Data-driven visibility into deal health, stage progression, and forecast roll-up across the sales organization |
| Forecast Category        | Classification of deals into commitment tiers: Commit, Best Case, Pipeline, Omitted |
| Coaching Scorecard       | Performance metrics for individual reps based on conversation analysis: talk-to-listen ratio, question frequency, topic coverage |
| Multi-Threading          | Having multiple stakeholder contacts engaged in a deal, reducing single-point-of-failure risk |
| Deal Inspection          | Structured review process where managers evaluate deal health using data rather than rep self-reporting |

· · ·

#### Common Gotchas
- Deploying before CRM data is clean leads to inaccurate deal scoring and erodes user trust from day one. Run a CRM hygiene audit in Phase 1 and address critical data quality issues before platform go-live. Studies show 44% of companies lose over 10% of annual revenue due to poor CRM data quality [1].
- Treating implementation as an IT project rather than a change management initiative results in less than 30% adoption. Assign a Sales Ops owner, require managers to use dashboards in weekly deal reviews, and track adoption metrics for the first 90 days.
- Enabling every feature at launch creates confusion and resistance. Start with one high-value use case (e.g., deal risk alerts or forecast roll-up) and add features incrementally.
- No baseline metrics means you cannot prove ROI. Document current forecast accuracy, win rates, and deal velocity in Phase 1 so you can measure improvement at 90-day review.
- Over-investing in dual-tool stacks (e.g., Gong + Clari simultaneously) creates redundancy, integration complexity, and budget strain. Evaluate platforms holistically first. According to analysis of 600+ user reviews, approximately 40% of teams stack Clari + Gong, but many report overlapping features [2].

· · ·

#### Methodology Options

| Option               | When to Use                                                        | Complexity |
| -------------------- | ------------------------------------------------------------------ | ---------- |
| Single Platform      | Client needs conversation intelligence + pipeline analytics in one tool (e.g., Gong) | Low-Medium |
| Dual Platform        | Client has existing Gong and needs dedicated forecasting (add Clari) | High       |
| CRM-Native           | Client uses Salesforce Einstein or HubSpot forecasting built-in    | Low        |

---

## Phase 1: Strategy

> **Goal:** Establish baseline metrics, select platform, define success criteria, and get stakeholder sign-off on what we are building.
>
> **Output:** Validated gap analysis, baseline metrics document, platform selection, deal scoring criteria, dashboard specifications, and Definition Alignment Document (signed off by stakeholders).

### 1a. Pre-Kickoff

> Two parallel tracks run before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                     | Format             |
| ----------------------------- | ----------------------------------------------------------- | ------------------ |
| Intro video                   | Explain what revenue intelligence is, what changes for the sales team, and what outcomes to expect | Video (5-10 min)   |
| Definition Alignment Document | Get stakeholder sign-off on key terms (Deal Risk Score, Forecast Category, Coaching Scorecard, etc.) | Google Doc         |
| Pre-filled intake form        | Confirm tech stack, recording status, team roster, compliance requirements | Google Form or Doc |
| Access requirements checklist | CRM admin, video platform admin, dialer admin access needed | Google Doc         |

**Completion tracking:** RevOps Lead is responsible for ensuring homework is complete. Do not cancel kickoff if incomplete, but follow up aggressively -- CRM access and legal recording approval are hard blockers for Phase 2.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                          | Output                                          |
| ---- | --------------------------------------------------------------- | ------------------------------------------------ |
| 1    | Pull call recording stats from existing dialer (last 90 days)   | Conversation capture rate by channel             |
| 2    | Audit CRM data quality (duplicates, missing fields, stage defs) | Data quality assessment with red flags           |
| 3    | Pull 4 quarters of forecast vs. actual from CRM                 | Baseline forecast accuracy by rep, team, segment |
| 4    | Document current tech stack with integration capabilities       | Integration requirements map (draft)             |
| 5    | Prepare platform evaluation matrix (if platform not selected)   | Scored comparison of Gong, Clari, Chorus, etc.   |

**Critical:** Mark all pre-kickoff findings as ASSUMED. The kickoff call validates. CRM data quality issues discovered here must be flagged early -- a Forrester study found that organizations can lose up to 12 hours per employee per week searching through fragmented, low-quality data systems [3].

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building anything.

| Term                       | Our Definition                                                                   | Internally Approved? |
| -------------------------- | -------------------------------------------------------------------------------- | -------------------- |
| Deal Risk Score            | Composite score (conversation signals + CRM activity patterns) indicating likelihood a deal will slip or be lost | [ ] Yes / [ ] No     |
| Forecast Category          | Commit, Best Case, Pipeline, or Omitted -- the commitment tier assigned to each deal for forecast roll-up | [ ] Yes / [ ] No     |
| Coaching Scorecard         | Rep-level performance metrics from conversation analysis: talk-to-listen ratio, question frequency, monologue length, topic coverage | [ ] Yes / [ ] No     |
| Multi-Threading            | Having 3+ stakeholder contacts actively engaged in a deal, reducing single-point-of-failure risk | [ ] Yes / [ ] No     |
| Deal Inspection            | Structured review process where managers evaluate deal health using data-driven signals rather than rep self-reporting | [ ] Yes / [ ] No     |
| Conversation Intelligence  | AI analysis of recorded sales conversations to surface deal signals, coaching moments, and competitive mentions | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your sales leadership team. Check "Yes" when approved. We cannot proceed to platform configuration until all terms are aligned -- misaligned definitions lead to scoring rules that do not match how your team actually thinks about deals.

---

### 1b. Kickoff Call

> **Purpose:** Present current state audit and get alignment on gaps, baselines, and success criteria. We walk in with work done -- customer reacts, not creates from scratch.

#### Agenda (60-90 min)

| Time  | Topic                         | What Happens                                                   |
| ----- | ----------------------------- | -------------------------------------------------------------- |
| 0-15  | Walk through gap analysis     | "Here's your conversation capture rate by channel -- 40% today" |
| 15-30 | Review baseline metrics       | Forecast accuracy, win rates, deal velocity, slippage rates    |
| 30-45 | Definition alignment          | Review Definition Alignment Document, confirm or correct terms |
| 45-55 | Platform discussion           | Present evaluation matrix (if applicable), confirm platform direction |
| 55-70 | Success criteria              | Agree on 3-5 measurable targets (e.g., forecast accuracy 65% -&gt; 85%) |
| 70-80 | Integration requirements      | Confirm CRM, dialer, video platform access and compatibility   |
| 80-90 | Next steps                    | Schedule alignment loop meetings, assign homework              |

#### What We Bring

- Gap analysis document (conversation capture rate by channel, blind spots identified)
- Baseline metrics document (4 quarters of forecast vs. actual, win rates, cycle length)
- Platform evaluation matrix (if platform selection is needed)
- Integration requirements map (draft)
- Definition Alignment Document (pre-filled with our recommendations)
- Questions list (compliance requirements, stakeholder availability, data access gaps)

#### What We Leave With

- Validated gap analysis (ASSUMED -&gt; CONFIRMED on capture rates and blind spots)
- Confirmed or corrected success criteria
- Platform direction (confirmed or evaluation scope narrowed)
- Clear homework assignments: IT to verify API access, Legal to confirm recording consent approach, RevOps to pull any missing data
- Alignment loop scheduled

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Finalize platform selection, deal scoring rules, and dashboard requirements. Typically 2 alignment meetings after kickoff.

#### The Pattern

```
Kickoff Call (validate gaps, confirm baselines)
    |
    v
Meeting 2: Platform + Integration Alignment
    |
    v
Meeting 3: Scoring Rules + Dashboard Design
    |
    v
Sign-Off Meeting
```

#### Before Each Meeting

1. Process previous meeting notes and feedback
2. Update working documents (gap analysis, integration map, scoring criteria)
3. Prepare questions for next validation round

#### During Each Meeting

1. Walk through current version of working documents
2. Capture corrections and refinements
3. Validate what is now CONFIRMED
4. Identify remaining ASSUMED items

#### After Each Meeting

1. Update all working documents
2. Track what moved from ASSUMED -&gt; CONFIRMED
3. Prepare materials for next session

#### Meeting Schedule

| Meeting Type           | Focus                                                   | Stakeholder                  |
| ---------------------- | ------------------------------------------------------- | ---------------------------- |
| Platform + Integration | Compare platform options, confirm API access, compliance | RevOps Lead, IT/Security     |
| Scoring + Dashboards   | Define risk signals, scoring weights, dashboard views    | VP Sales, Sales Managers     |
| Final Review           | Full walkthrough of strategic package, sign-off          | CRO/VP Sales, RevOps Lead   |

#### Typical Timeline

| Milestone               | Timing                              |
| ----------------------- | ----------------------------------- |
| Pre-kickoff prep        | 2-3 days                            |
| Kickoff call            | Day 1 of engagement                 |
| Alignment meetings      | 1-2 weeks (2 meetings)              |
| Final review + sign-off | When all inputs CONFIRMED           |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything before proceeding to build.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by VP Sales/CRO
- [ ] Baseline metrics documented (forecast accuracy, win rates, deal velocity, slippage)
- [ ] Platform selected and procurement initiated
- [ ] Integration requirements confirmed by IT (CRM, dialer, video, SSO)
- [ ] Legal/compliance approval for call recording obtained
- [ ] Deal scoring criteria defined and approved by sales leadership
- [ ] Dashboard requirements documented (rep, manager, executive views)
- [ ] Success criteria with measurable targets agreed
- [ ] All critical inputs CONFIRMED (vs ASSUMED)
- [ ] No blockers for engineering

#### Decision Point

- **Proceed to Engineering** -&gt; Platform selected, integrations confirmed, scoring rules defined. This is the standard path -- Revenue Intelligence Process projects almost always require Phase 2 build.
- **Project on hold** -&gt; Rare, but possible if CRM data quality is too poor to support meaningful deal scoring. In that case, scope a CRM Data Hygiene project first.

---

## Phase 2: Engineering

> **Goal:** Configure the revenue intelligence platform, integrate with CRM and communication tools, build deal scoring, dashboards, forecasting workflow, and coaching scorecards.
>
> **Output:** Fully configured revenue intelligence platform, tested and customer-approved.

| Project Type    | Engineering Weight | This Project                                          |
| --------------- | ------------------ | ----------------------------------------------------- |
| Strategic-heavy | Light (10-20%)     | --                                                    |
| Balanced        | Medium (40-60%)    | --                                                    |
| Technical-heavy | Heavy (70-90%)     | Revenue Intelligence Process -- extensive platform config, integrations, scoring, dashboards |

### Sub-Phases

```
2a Tech Spec -> 2b Engineering Handoff -> 2c Build -> 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate strategic package into technical specifications for platform configuration.

**Input:** Signed-off strategic package (platform choice, integration map, scoring rules, dashboard specs)

**Output:** Draft tech spec containing:

- CRM field mapping (opportunity fields, contact roles, activity types -&gt; platform fields)
- Recording integration specs (Zoom OAuth, Teams connector, dialer API setup)
- Deal scoring rule configuration (risk signals, weights, thresholds)
- Dashboard specifications (metrics, filters, drill-down paths per stakeholder view)
- Forecast workflow configuration (categories, submission schedule, roll-up logic)
- Coaching scorecard configuration (metrics, benchmarks, alert thresholds)
- Alert configuration (triggers, notification channels, escalation rules)
- Build sequence (what to configure first based on dependencies)

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs with engineer before building.

**Who attends:** Architect + Engineer (or engineering team)

**Agenda (30-45 min):**

| Time  | Topic              | What Happens                                                         |
| ----- | ------------------ | -------------------------------------------------------------------- |
| 0-15  | Walk through specs | Architect explains strategic context: why these scoring rules, why these dashboards |
| 15-30 | Engineer questions | Clarify CRM schema, API limitations, recording consent configuration |
| 30-45 | Refine and approve | Adjust specs for technical feasibility, confirm build sequence       |

**What Architect brings:**

- Strategic package (gap analysis, success criteria, scoring rules, dashboard specs)
- Draft tech spec (from 2a)
- Questions list (anything flagged as unclear -- CRM custom objects, API rate limits, SSO config)

**What engineer leaves with:**

- Approved tech spec
- Clear build sequence: (1) Platform setup -&gt; (2) CRM sync -&gt; (3) Recording integrations -&gt; (4) Deal scoring -&gt; (5) Dashboards -&gt; (6) Forecast workflow -&gt; (7) Coaching + alerts -&gt; (8) Call library
- Known risks: CRM data quality issues that may affect scoring, recording consent requirements by jurisdiction

---

### 2c. Build (Configure)

> **Purpose:** Configure the revenue intelligence platform and all integrations.

**Input:** Approved tech spec from 2b

**Build sequence:**

**Component 1: Platform Setup**
- [ ] Create platform account with enterprise license
- [ ] Configure SSO integration (Okta, Azure AD, Google) if applicable
- [ ] Set up admin accounts for RevOps team with full configuration access
- [ ] Define user role hierarchy: Admin, Manager, Rep, Read-Only
- [ ] Document admin credentials and access procedures

**Component 2: CRM Sync**
- [ ] Connect to Salesforce/HubSpot via OAuth with read/write permissions
- [ ] Map standard objects: Opportunities, Accounts, Contacts, Activities
- [ ] Configure custom field sync for deal-specific data (MEDDIC fields, custom stages, contact roles)
- [ ] Set sync frequency (real-time recommended for deal scoring accuracy)
- [ ] Verify connection and run initial data sync -- validate sample records match CRM

**Component 3: Recording Integrations**
- [ ] Configure Zoom integration with automatic recording for external meetings
- [ ] Set up Microsoft Teams or Google Meet integration (based on client stack)
- [ ] Connect dialer system (Outreach, Salesloft, Aircall, RingCentral) for phone recording
- [ ] Configure recording consent settings based on legal requirements (one-party vs. two-party)
- [ ] Test recording on each channel type and verify transcription accuracy

**Component 4: Deal Scoring**
- [ ] Define conversation risk signals: competitor mentions, stakeholder drop-off, timeline shifts, budget objections
- [ ] Configure CRM-based risk rules: stalled deals (no activity in X days), missing next steps, no recent engagement
- [ ] Set up engagement scoring: single-threaded vs. multi-threaded, champion engagement level
- [ ] Calibrate scoring weights using client's historical win/loss patterns
- [ ] Test scoring on 10-20 sample deals and validate with sales leadership

**Component 5: Pipeline Dashboards**
- [ ] Build rep-level dashboard: personal pipeline, deal health scores, activity metrics, next steps
- [ ] Build manager-level dashboard: team pipeline, forecast vs. quota, rep performance comparison, at-risk deals
- [ ] Build executive dashboard: company forecast roll-up, quarter projection, pipeline coverage, risk summary
- [ ] Configure drill-down paths from summary views to individual deal details
- [ ] Set up scheduled dashboard email delivery to stakeholders (weekly for managers, weekly/monthly for execs)

**Component 6: Forecast Workflow**
- [ ] Define forecast categories: Commit, Best Case, Pipeline, Omitted
- [ ] Configure submission workflow with rep input and manager override capability
- [ ] Set up forecast snapshot schedule: weekly, monthly, quarterly
- [ ] Build forecast accuracy tracking to compare submissions vs. actuals over time
- [ ] Configure automated reminders for forecast submission deadlines

**Component 7: Coaching & Alerts**
- [ ] Configure coaching metrics: talk-to-listen ratio target (40:60), question frequency, monologue length limits
- [ ] Set up topic detection for conversation elements: discovery, demo, negotiation, pricing, objection handling
- [ ] Configure competitor mention alerts and tracking
- [ ] Establish benchmark values from top performer data (first 2 weeks of recording data)
- [ ] Build manager comparison view for rep performance vs. benchmarks
- [ ] Define alert triggers: ghosting risk (no response 5+ days), competitor mention, champion departure, timeline change
- [ ] Configure notification channels (email + in-platform)
- [ ] Set up escalation rules: rep notified first, manager notified if no action within 48 hours
- [ ] Build weekly deal health digest for managers

**Component 8: Call Library**
- [ ] Configure call tagging taxonomy: discovery, demo, objection handling, negotiation, pricing, competitive
- [ ] Build onboarding playlists: best discovery calls, winning demos, strong objection handling
- [ ] Set up snippet creation workflow for managers to capture coaching moments
- [ ] Create competitive intelligence collection (calls with competitor mentions)
- [ ] Document process for reps and managers to contribute to library

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify the entire system works and get customer approval.

**Technical testing checklist:**

- [ ] CRM sync: all fields mapped correctly, bidirectional sync working, no data loss
- [ ] Recording: calls captured on Zoom, Teams/Meet, and dialer; transcription accurate
- [ ] Deal scoring: scores appearing on all active opportunities; risk indicators correct for known at-risk deals
- [ ] Dashboards: all three views (rep, manager, exec) rendering correctly with live data
- [ ] Forecast workflow: reps can submit, managers can override, snapshots saved correctly
- [ ] Coaching scorecards: metrics calculating correctly, benchmarks displaying
- [ ] Alerts: triggers firing for test scenarios (ghosting, competitor mention, timeline change)
- [ ] Call library: tags applied correctly, playlists accessible, snippets creatable
- [ ] No errors in platform logs or CRM sync logs
- [ ] Recording consent notifications displaying properly

**Customer testing:**

- Walk VP Sales and RevOps Lead through the complete system
- Have a manager run a mock deal review using live dashboard data
- Have a rep review their own calls and coaching scorecard
- Have RevOps admin perform user management and troubleshooting tasks
- Capture feedback, fix issues

**Engineering sign-off checkpoint:**

- [ ] Built system matches tech spec
- [ ] All technical tests passing
- [ ] Customer has tested and approved
- [ ] Ready for enablement

**Decision point:**

- **Proceed to Enablement** -&gt; System is built and tested, needs team training and adoption
- **Loop back to Build** -&gt; Issues found (scoring inaccurate, dashboard data wrong, integration failures)

---

## Phase 3: Enablement

> **Goal:** Sales managers, reps, and RevOps admin can use the revenue intelligence system independently.
>
> **Output:** Trained team with documentation, stabilized system, no critical issues.

### Sub-Phases

```
3a Training Prep -> 3b Training Sessions -> 3c Hypercare -> 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from strategic and technical documentation.

**Input:** Strategic package + tech specs + built system + deal review playbook

**Output:** Training package containing:

- **Manager training guide:** Deal inspection workflow, dashboard navigation, coaching scorecard interpretation, forecast submission process
- **Rep training guide:** What's recorded and why, privacy settings, how to review own calls, how to use coaching insights for self-improvement
- **Admin runbook:** User provisioning, permission management, integration monitoring, common troubleshooting scenarios (sync issues, recording failures, scoring anomalies)
- **FAQ document:** Addressing rep privacy concerns, recording consent questions, data usage policies
- **Deal review meeting agenda template:** 30-45 minute format with required pre-work and dashboards

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to customer team. Three distinct audiences need different training.

**Training delivery by audience:**

| Session             | Audience                      | Duration | Focus                                                                          |
| ------------------- | ----------------------------- | -------- | ------------------------------------------------------------------------------ |
| Manager Training    | VP Sales, Sales Managers      | 60 min   | Deal inspection workflow using live data, dashboard navigation, coaching scorecards, forecast submission |
| Rep Training        | Sales Reps                    | 30 min   | What's auto-recorded, privacy settings, reviewing own calls, using insights for self-coaching |
| Admin Training      | RevOps/Sales Ops Admin        | 60-90 min | Hands-on: user provisioning, permission management, integration monitoring, troubleshooting sync issues and recording failures |

**Manager Training -- Detailed Agenda:**

1. Walk through deal inspection workflow using live pipeline data
2. Demonstrate dashboard navigation: rep view, manager view, executive view
3. Show coaching scorecard: how to compare rep performance to benchmarks
4. Practice forecast submission: enter forecasts, apply manager overrides, review snapshots
5. Show alert system: where notifications appear, how to act on them
6. Distribute deal review meeting agenda template with example
7. Record session for managers who cannot attend live

**Rep Training -- Detailed Agenda:**

1. Explain what is auto-recorded (all external calls and meetings) and what is not
2. Walk through privacy settings and controls available to reps
3. Show how to review own calls and coaching insights
4. Demonstrate self-improvement workflow: identify talk ratio, question frequency, areas to improve
5. Address common concerns about monitoring and data usage (distribute FAQ)
6. Record session for reps who cannot attend live

**Admin Training -- Detailed Agenda:**

1. Hands-on user provisioning: add users, assign roles, manage permissions
2. Integration monitoring: how to check CRM sync status, recording connectivity
3. Walk through common troubleshooting scenarios: sync delays, recording failures, scoring anomalies
4. Document admin runbook handoff with step-by-step procedures
5. Transfer admin credentials and confirm client admin access
6. Record session for backup admins

**Output:**

- Trained managers, reps, and admin
- Video walkthrough recordings of all three sessions
- Questions log (feeds into FAQ updates)

---

### 3c. Hypercare

> **Purpose:** Intensive post-launch support to stabilize the system and drive initial adoption.

**Duration:** 2 weeks

**What happens:**

- Quick response to issues: sync problems, recording failures, scoring questions
- Office hours: weekly 30-min slot where anyone can join and ask questions
- Adoption monitoring: track recording coverage (target: 95%+ within first 2 weeks), dashboard access frequency, forecast submission compliance
- Bug triage: fix integration issues, adjust scoring weights if calibration is off
- Coaching managers on running their first data-driven deal reviews

**Adoption KPIs to monitor during hypercare:**

| Metric                        | Target by End of Week 2 | Red Flag               |
| ----------------------------- | ----------------------- | ---------------------- |
| Call recording coverage       | 95%+                    | Below 80%              |
| Manager dashboard access      | 3x per week minimum     | Less than 1x per week  |
| Forecast submission compliance | 90%+                   | Below 70%              |
| Rep self-review of calls      | At least 1 per week     | Zero usage             |

Gong reports that platforms typically achieve 60-70% adoption within 3-6 months [4], but with structured change management and manager-led deal reviews, teams can accelerate this significantly in the first 2 weeks.

**Output:** Stabilized system, initial adoption metrics trending positive, no critical issues outstanding.

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm customer can operate independently.

**Validation checkpoint:**

- [ ] All three training sessions delivered (managers, reps, admin)
- [ ] Training recordings and documentation provided (video walkthroughs, guides, FAQ, admin runbook)
- [ ] Hypercare period complete (2 weeks)
- [ ] Recording coverage at 95%+ (or acceptable threshold agreed with customer)
- [ ] Managers have run at least one data-driven deal review using dashboards
- [ ] Forecast submission process tested and working
- [ ] RevOps admin can independently perform user management, monitor integrations, and troubleshoot common issues
- [ ] No critical issues outstanding
- [ ] Customer team can operate without daily support
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** -&gt; Customer is enabled, adoption metrics are healthy, system is stable
- **Extend Hypercare** -&gt; Recording coverage below target, managers not using dashboards, admin not yet self-sufficient

---

## Phase 4: Handoff

> **Goal:** Clean project close with deal review cadences established, maintenance plan documented, and retention/expansion path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the system, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule -> 4b Internal Handoff -> 4c External Handoff -> 4d Project Close
                           (SME -> Architect)     (Team -> Customer)     (Archive + Debrief)
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At                                                                         |
| ----------------------------- | -------------------- | ------------------------------------------------------------------------------------- |
| **Single Project**            | Customer owns        | 4c (External Handoff) -- customer receives maintenance schedule and runs it themselves |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) -- Architect receives maintenance schedule and runs it for customer |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention after the project is complete.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task                  | What to Check                                              | Red Flag Threshold                       |
| ----------------------------- | ---------------------------------------------------------- | ---------------------------------------- |
| Recording coverage audit      | % of customer conversations being captured across channels | Below 90% (target: 95%+)                |
| Deal scoring accuracy check   | Spot-check 5-10 scored deals against actual outcomes       | More than 30% of scored "low risk" deals that actually slipped |
| Dashboard usage audit         | Manager and rep access frequency                           | Managers accessing less than 2x per week |
| Forecast submission compliance | % of reps submitting forecasts on time                    | Below 85% compliance                    |
| Integration health check      | CRM sync status, recording connectivity, API errors        | Any sustained sync failures or data gaps |

**Quarterly Tasks:**

| Quarterly Task                   | What to Review                                        | Action if Off-Track                        |
| -------------------------------- | ----------------------------------------------------- | ------------------------------------------ |
| Scoring rule recalibration       | Compare deal scores vs. actual win/loss over quarter   | Adjust scoring weights and thresholds      |
| Forecast accuracy trend review   | Compare forecast submissions vs. actuals by quarter    | Refine forecast categories or submission process |
| Feature adoption assessment      | Which features are used vs. ignored                    | Retrain on underutilized features or simplify |
| Top performer benchmark refresh  | Recalculate coaching scorecard benchmarks              | Update benchmarks from latest top performer data |

**After First Business Cycle (30-90 days post-launch):**

- Compare forecast accuracy to baseline (target: 15+ percentage point improvement within 2 quarters) [5]
- Measure deal slippage rate against baseline (target: 30% reduction)
- Assess new rep ramp time impact (target: 20% faster with coaching scorecards)
- Review recording coverage stability
- Validate that deal review cadences are happening consistently

**Refinement Triggers (when to re-engage):**

| Trigger                          | Threshold                                      | Response                                         |
| -------------------------------- | ---------------------------------------------- | ------------------------------------------------ |
| Forecast accuracy declining      | Drops more than 10 points from peak            | Re-engage SME to recalibrate scoring rules       |
| Recording coverage dropping      | Falls below 85% for 2+ consecutive weeks       | Audit integration health, retrain on recording setup |
| Manager dashboard usage decline  | Fewer than 50% of managers accessing weekly    | Run refresher training, reinforce deal review cadence |
| New sales team structure         | Segments added, teams reorganized               | Scope refinement project for dashboard/scoring updates |

**Every 6-12 Months:**

- Full scoring model recalibration against latest win/loss data
- Platform feature review (vendor releases new capabilities)
- Benchmark refresh using updated top performer analysis
- Evaluate whether platform consolidation or expansion is warranted

---

### 4b. Internal Handoff (SME -&gt; Architect)

> **Purpose:** Transfer context so Architect can manage ongoing relationship.

**What the Architect needs to know:**

- What was built: platform configuration, CRM field mappings, scoring rules, dashboard structure
- Customer context: stakeholder relationships (who is the champion, who was skeptical), compliance requirements, any data quality issues worked around
- Common issues: CRM sync delays (check API rate limits), recording failures (verify consent settings), scoring anomalies (recalibrate weights)
- When to escalate back to SME: changes to scoring logic, new CRM integration requests, platform migration
- **Maintenance schedule** (if Dedicated engagement -- Architect runs this)

**Escalation guidelines:**

| Issue Type                                    | Who Handles           | Examples                                          |
| --------------------------------------------- | --------------------- | ------------------------------------------------- |
| Small tweaks, minor questions                 | Architect             | Add new user, adjust dashboard filter, re-enable recording for a rep |
| Significant changes, complex issues           | SME                   | Restructure scoring logic, add new CRM integration, platform migration |

**For Dedicated engagements:** Architect also receives the maintenance schedule (4a) and becomes responsible for executing it. SME walks Architect through each maintenance task -- especially scoring recalibration, which requires understanding the calibration rationale.

---

### 4c. External Handoff (Implementation Team -&gt; Customer)

> **Purpose:** Formal project completion with customer.

**Final project meeting:**

- Review what was delivered: platform configuration, CRM sync, recording integrations, deal scoring, dashboards, forecast workflow, coaching scorecards, call library
- Walk through documentation package
- Review success criteria: baseline vs. current metrics
- Confirm deal review cadence is established and calendar invites sent
- Confirm forecast cadence is established (weekly pipeline review, monthly forecast call, QBR)
- Answer final questions
- Make it explicit: "Project complete"
- **For Single Project engagements:** Hand over the maintenance schedule and walk customer through it in detail

**Documentation package:**

- All training video walkthrough recordings (manager, rep, admin sessions)
- Admin runbook (user provisioning, permissions, troubleshooting, integration monitoring)
- Deal review meeting agenda template with manager checklist
- Forecast cadence calendar with meeting templates
- Definition Alignment Document (final version)
- Platform configuration document (field mappings, scoring rules, dashboard specs)
- FAQ document (including rep privacy questions)
- Maintenance Schedule (for Single Project engagements)

**For Single Project engagements:** Walk the customer through the maintenance schedule in detail. Record a video walkthrough of the walkthrough. Emphasize the monthly tasks (recording coverage, scoring accuracy, dashboard usage) and quarterly tasks (scoring recalibration, benchmark refresh).

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

- What went well? (e.g., platform selection process, scoring calibration accuracy, training engagement)
- What would we do differently? (e.g., CRM data quality should have been addressed earlier, legal approval took longer than expected)
- Any learnings to feed back into SOPs? (e.g., new scoring pattern for this industry vertical)

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell -&gt; Downsell -&gt; Retry  |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (retainer)
   | if no
   v
2. Downsell: Another one-time project
   - Sales Qualification Methodology (scoring + intelligence complement)
   - Forecasting Process Implementation (extends forecast workflow)
   - Sales Engagement Platform (adds outbound intelligence)
   | if yes
   v
3. Retry retainer at end of next project cycle
```

**Script:**

> "Now that your revenue intelligence system is live, there are two ways we can continue working together. Option 1: We can set you up on managed services where we handle ongoing scoring recalibration, dashboard optimization, and adoption coaching. Option 2: If there's a specific project -- like building out your sales qualification methodology to feed better data into your deal scoring -- we can scope that out. Which sounds more interesting?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On [date ~quarter out], we'll review how your scoring accuracy and forecast improvements are trending, and see if any adjustments are needed."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                                     |
| ------------------- | ---------------------------------------------------------------- |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks                 |
| 2. Review metrics   | Pull forecast accuracy trend, scoring calibration data, adoption metrics |
| 3. Decide ownership | Can Architect handle this check-in, or need SME for scoring changes? |
| 4. Prep materials   | If SME needed, brief them. If Architect, prep talking points.    |

**At the refinement check-in:**

- Review performance against original success criteria
- Compare current forecast accuracy to baseline
- Identify any scoring rule adjustments needed
- If minor: Architect handles tweaks (threshold adjustments, new alert rules)
- If major: Scope new project (new segment scoring, platform migration, additional integrations)

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- Gap analysis document (conversation capture rate by channel, blind spots)
- Baseline metrics document (4 quarters of forecast accuracy, win rates, deal velocity)
- Platform evaluation matrix (if platform selection was part of scope)
- Definition Alignment Document (signed off by stakeholders)
- Success criteria document with measurable targets

**Technical Deliverables:**

- Configured revenue intelligence platform (Gong, Clari, or selected platform)
- CRM integration (bidirectional sync with field mappings)
- Recording integrations (Zoom, Teams/Meet, dialer)
- Deal risk scoring system (conversation signals + CRM activity patterns)
- Pipeline analytics dashboards (rep, manager, executive views)
- Forecast submission workflow with category management
- Coaching scorecards with top performer benchmarks
- Automated deal alert system
- Call library with tagging taxonomy and onboarding playlists

**Documentation Package:**

- Training video walkthrough recordings (manager, rep, admin sessions)
- Admin runbook (user provisioning, permissions, troubleshooting)
- Deal review meeting agenda template
- Forecast cadence calendar with meeting templates
- FAQ document (including rep privacy questions)
- Platform configuration document (field mappings, scoring rules, dashboard specs)
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

---

### What Each Phase Produces

| Phase                    | Output                                                                 | Gate Criteria                                                                  |
| ------------------------ | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **Phase 1: Strategy**    | Signed-off strategic package (gap analysis, baselines, platform choice, scoring rules, dashboard specs) | Customer stakeholders have approved definitions and strategic package           |
| **Phase 2: Engineering** | Fully configured revenue intelligence platform                         | System matches tech spec, all tests pass, customer has approved                |
| **Phase 3: Enablement**  | Trained managers, reps, and admin with documentation                   | All training delivered, hypercare complete, adoption metrics trending positive  |
| **Phase 4: Handoff**     | Independent customer + archived project                                | Internal/external handoffs complete, maintenance plan in place, project closed  |

---

### How to Adapt Per Project Type

| Project Profile       | Strategy Weight | Engineering Weight | Enablement Weight |
| --------------------- | --------------- | ------------------ | ----------------- |
| **Strategic-heavy**   | 60-80%          | 10-20%             | 10-20%            |
| **Engineering-heavy** | 10-20%          | 60-80%             | 10-20%            |
| **Enablement-heavy**  | 20-30%          | 20-30%             | 40-50%            |
| **Balanced**          | 30-40%          | 30-40%             | 20-30%            |

Revenue Intelligence Process is engineering-heavy: the core value is in the platform configuration, integration work, and scoring/dashboard builds. Strategy is medium (baseline metrics and platform selection matter but are not the primary deliverable). Enablement is medium (three distinct audiences need training, and adoption is a known risk -- Forrester research on revenue intelligence platforms found 481% ROI, but only when adoption is properly managed [6]).

---

### Key Engineering Principles

**Tech Spec (2a):** Translate scoring criteria and dashboard requirements into platform-specific configuration. Review for client-specific nuances before handing to engineering.

**Engineering Handoff (2b):** Engineer must understand WHY specific scoring signals were chosen (e.g., "competitor mentions are weighted high because this client is in a 3-player market"). Strategic context prevents misconfiguration.

**Build (2c):** Follow the build sequence strictly -- CRM sync must be verified before deal scoring can be tested, and scoring must work before dashboards display meaningful data. Each component depends on the previous.

---

### Key Enablement Principles

**Training Prep (3a):** Customize materials for client context -- especially the FAQ addressing rep privacy concerns. Position recording as a coaching benefit, not surveillance. The companies that succeed with adoption focus on the human side of change before the technical side [8].

**Hypercare (3c):** The first two weeks are critical. Track recording coverage (95%+ target), dashboard access frequency, and forecast submission compliance daily. If managers are not using dashboards in their first deal review, intervene immediately -- adoption compounds when managers visibly use the tool.

---

### Key Handoff Principles

**Maintenance Schedule (4a):** Revenue intelligence systems drift. Scoring rules need recalibration quarterly as win/loss patterns change. Recording coverage drops when new reps onboard without setup. Dashboard usage declines without reinforced cadences. The maintenance schedule prevents all three.

**External Handoff (4c):** The deal review cadence and forecast cadence are as important as the platform itself. If the customer does not leave with calendar invites for weekly deal reviews and monthly forecast calls, the system will be underutilized within 60 days.

---

## References

[1] [Validity - How Poor Data Quality is Sabotaging Your Business](https://www.validity.com/blog/poor-data-quality-is-sabotaging-businesses-in-2022/)

[2] [Oliv AI - We Analyzed 600+ Gong Reviews](https://www.oliv.ai/blog/gong-reviews)

[3] [Forrester Research via Nintex - Top 5 Reasons Enterprise CRM Projects Fail](https://www.nintex.com/blog/top-5-reasons-enterprise-crm-projects-fail/)

[4] [Gong - Conversation Intelligence Platform](https://www.gong.io/conversation-intelligence)

[5] [Gong vs Clari ROI Analysis - Forecast Accuracy Improvements](https://www.oliv.ai/blog/gong-vs-clari)

[6] [Gong - Forrester Study Reveals 481% ROI in Revenue Intelligence Platform](https://www.gong.io/press/new-study-reveals-481-roi-in-gongs-revenue-intelligence-platform/)

[7] [Revenue Intelligence Tools Guide 2025 - Performance Statistics](https://optif.ai/media/articles/revenue-intelligence-tools-guide-2025/)

[8] [MarketsandMarkets - Change Management for Sales Technology Adoption](https://www.marketsandmarkets.com/AI-sales/change-management-for-sales-technology-adoption)
