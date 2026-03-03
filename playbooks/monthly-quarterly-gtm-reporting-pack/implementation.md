# Monthly/Quarterly GTM Reporting Pack — Implementation

## Project One-Pager

> Quick reference for architects. This one-pager is the first thing an Architect reads when picking up this project type. It should take 2 minutes to scan and understand what the project is, how it flows, and what tools are used.

### Monthly/Quarterly GTM Reporting Pack One-Pager

#### Project Type

- Category: Balanced
- Primary Deliverable: A standardized, board-ready reporting deck updated on a recurring cadence, compiling Power 10 GTM Metrics and operational KPIs across all GTM functions

##### Phase Relevance

| Phase          | Applies? | Weight | Notes                                                        |
| -------------- | -------- | ------ | ------------------------------------------------------------ |
| 1. Strategy    | Yes      | Heavy  | 3-4 meetings: discovery, metric alignment, deck structure    |
| 2. Engineering | Yes      | Medium | Data extraction setup, deck construction, validation         |
| 3. Enablement  | Yes      | Medium | Update runbook, team training, first live cycle support      |
| 4. Handoff     | Yes      | Medium | Internal + External handoff with maintenance schedule        |

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────>│ 2. ENGINEER  │────>│3. ENABLEMENT │────>│  4. HANDOFF  │
  │    Heavy     │     │    Medium    │     │    Medium    │     │    Medium    │
  │ 1a->1b->1c->1d│     │ 2a->2b->2c->2d│     │ 3a->3b->3c->3d│     │ 4a->4b->4c->4d│
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   Requirements         Data consolidation   Runbook + training   Maintenance plan
   + metric alignment   + deck construction  + first live cycle   + ownership transfer
```

**This project's flow:**
- Full 4-phase. Heavy strategy (audience mapping, metric definition, structure design), medium engineering (data extraction, deck build, validation), standard enablement and handoff.
- Phase 1 requires sign-off on metric definitions before any data work begins. This is the single biggest risk gate.
- Phase 2 includes both data engineering (extraction processes) and design work (deck layout, visualizations).

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Watch intro video explaining the reporting pack project, Power 10 metrics, and what "board-ready" means
- [ ] Complete intake form: list all audiences (board, investors, exec team, functional leaders), delivery cadence preferences, existing reports
- [ ] Provide access credentials to CRM, marketing automation, CS platform, and finance systems
- [ ] Gather 2-3 examples of existing reports, board decks, or investor updates currently in use
- [ ] Assign internal report owner who will maintain the pack post-handoff

##### Track B: Architect Prep
- [ ] Pull CRM metadata: fields, objects, report types available
- [ ] Audit existing reports in CRM and marketing automation platforms
- [ ] Draft audience matrix mapping stakeholders to use cases and detail requirements
- [ ] Map Power 10 GTM Metrics to client's likely data sources (ASSUMED)
- [ ] Create v0 metric framework with recommended definitions and data sources

#### Refinement Loop (1b -> 1c -> 1d)

| Meeting       | Sub-Phase | Focus                                                          | Stakeholder                              | Output                          |
| ------------- | --------- | -------------------------------------------------------------- | ---------------------------------------- | ------------------------------- |
| Kickoff       | 1b        | Present v0 metric framework, validate audiences and use cases  | Report owner, executive sponsor          | Info for v1 metric framework    |
| Refinement 1  | 1c        | Review metric definitions with each functional leader          | VP Sales, VP Marketing, CS Lead, Finance | Confirmed metric definitions    |
| Refinement 2  | 1c        | Review v1 deck structure, agree on visual hierarchy and layout | Executive sponsor, report owner          | Approved deck skeleton          |
| Sign-Off      | 1d        | Final metric framework + deck structure approval               | All stakeholders                         | Green light for data work       |

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held — audiences mapped, metric framework presented
- [ ] 1c. Refinement loop complete — metric definitions locked, deck structure approved
- [ ] 1d. Strategic sign-off obtained — metric framework + deck skeleton approved

##### Phase 2: Engineering
- [ ] 2a. Data architecture map created (metric -> source -> extraction method)
- [ ] 2b. Data extraction process built and tested
- [ ] 2c. Deck constructed with live data (executive summary + functional sections + appendix)
- [ ] 2d. Historical data validated, deck QA complete, customer sign-off

##### Phase 3: Enablement
- [ ] 3a. Update runbook and training materials prepared
- [ ] 3b. Training sessions delivered to report owner and stakeholders
- [ ] 3c. First live update cycle completed with support
- [ ] 3d. Enablement sign-off — team can update independently

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff complete
- [ ] 4c. External handoff (project team -> Customer) complete
- [ ] 4d. Project closed and archived

#### Document Types

##### Working Documents (iterate together)

| Document                     | Purpose                                                    | When Complete                           |
| ---------------------------- | ---------------------------------------------------------- | --------------------------------------- |
| Audience matrix              | Map stakeholders to use cases, detail levels, frequency    | All audiences documented and confirmed  |
| Metric framework spreadsheet | Define each metric: name, formula, source, owner           | All metrics defined and signed off      |
| Data source inventory        | Document all systems, access methods, refresh capabilities | All sources mapped with extraction plan |
| Gap analysis                 | Show what exists vs. what is needed                        | Gaps prioritized, remediation planned   |

##### Deliverables (polished outputs)

| Deliverable                 | Created From                      | Customer Uses For                                  |
| --------------------------- | --------------------------------- | -------------------------------------------------- |
| Monthly/Quarterly GTM deck  | Metric framework + live data      | MBRs, QBRs, board meetings, investor updates       |
| Metric definition glossary  | Metric framework spreadsheet      | Cross-team alignment, new hire onboarding          |
| Update runbook              | Data source inventory + deck flow | Monthly/quarterly self-service update process      |

#### Enablement Details

##### Training Types

| Type       | Audience                          | Focus                                                       | Duration |
| ---------- | --------------------------------- | ----------------------------------------------------------- | -------- |
| Leadership | CEO, CFO, VP Sales, VP Marketing  | How to interpret the pack, what actions to take from signals | 30 min   |
| Technical  | RevOps, report owner, admin       | How to update data, refresh the deck, troubleshoot issues   | 60-90 min|

##### Hypercare
- Applies: Yes
- Duration: 2 update cycles (2 months for monthly, or 1 quarter for quarterly)
- Office Hours: Yes — weekly 30-min slot during first update cycle

##### Training Assets to Create
- [ ] Video walkthrough: Full deck walkthrough (section by section, what each metric means)
- [ ] Video walkthrough: Update process walkthrough (data pull -> deck update -> QA -> distribute)
- [ ] Doc: Metric definition glossary with calculation formulas
- [ ] Doc: Update runbook with screenshots and timeline
- [ ] Doc: Troubleshooting guide for common data issues

#### Handoff & Retention

##### Internal Handoff
- Key context to transfer: Which metrics the client cares most about, any data quality quirks, stakeholder communication preferences for report distribution
- Escalation trigger: Metric definition changes, new data source integration, deck restructuring

##### External Handoff (Project Team -> Customer)
- Final meeting agenda: Review all deliverables, walk through update runbook live, confirm distribution cadence and ownership
- Documentation package: Deck template, metric glossary, update runbook, training video walkthroughs, troubleshooting guide

##### Maintenance Schedule
- Monthly: Data pull and deck update (target &lt; 4 hours per cycle)
- Quarterly: Full metric review, audience feedback collection, deck refinement
- Who owns: Single Project = customer report owner | Dedicated = Architect owns update cycle

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services (project team runs the monthly update cycle) -> if no -> Downsell: Another project (dashboard infrastructure, attribution model, ARR reporting) -> Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~quarter out from handoff
- Internal prep trigger: 2 weeks before
- Decision: Architect handles / specialist needed

#### Key Assets

| Asset                        | When Used       |
| ---------------------------- | --------------- |
| Metric framework template    | Phase 1 (1a-1c) |
| Deck template (slide master) | Phase 2 (2c)    |
| Update runbook               | Phase 3-4       |
| Data extraction scripts      | Phase 2-4       |

#### Definition Alignment Terms

| Term                       | Typical Definition                                                                                 |
| -------------------------- | -------------------------------------------------------------------------------------------------- |
| Power 10 GTM Metrics       | The ten key metrics spanning the full GTM lifecycle (ARR, pipeline, conversion, CAC, NRR, etc.)   |
| MBR                        | Monthly Business Review — internal or board-facing monthly performance summary                     |
| QBR                        | Quarterly Business Review — deeper quarterly analysis with trend commentary and strategic actions  |
| Net Revenue Retention (NRR)| (Starting ARR + Expansion - Contraction - Churn) / Starting ARR, expressed as a percentage        |
| Customer Acquisition Cost  | Total sales and marketing spend / number of new customers acquired, in a given period             |
| Pipeline Coverage          | Total qualified pipeline value / revenue target for the period                                    |
| Forecast Accuracy          | Actual bookings / forecasted bookings, measured at a fixed point (e.g., start of quarter)         |
| Operational KPIs           | Function-specific metrics below the Power 10 that drive day-to-day performance                    |

#### Common Gotchas
- Metric definition disagreements surface late (after data work begins) -> Lock definitions with stakeholder sign-off in Phase 1 before any data work
- Data quality issues erode trust when report shows numbers teams don't expect -> Validate historical data against known benchmarks (previous board decks, finance actuals) before building the deck
- Pack becomes too complex to maintain (50+ slides, 20+ hours per update) -> Design for primary audience first, push detail to appendix, time-box update process to &lt; 4 hours
- No clear owner post-handoff, report stops being updated -> Assign a named owner during discovery and train them directly, not just "the team"
- Teams calculate the same metric differently across departments -> Create a metric definition glossary with explicit formulas and sign off before build
- Data source access issues discovered during build -> Inventory all systems and confirm access during pre-kickoff (Phase 1a)

#### Methodology Options

| Option                       | When to Use                                                      | Complexity |
| ---------------------------- | ---------------------------------------------------------------- | ---------- |
| Slide-based pack (Google Slides / PowerPoint) | Default approach, most flexible for board and investor audiences  | Low-Medium |
| BI-connected pack (Looker, Tableau, Power BI)  | Client has existing BI infrastructure and wants real-time refresh | Medium-High|
| Hybrid (slides + embedded BI)                  | Executive summary in slides with drill-down links to live dashboards | Medium     |

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on what metrics to include, how to define them, and how the reporting pack is structured.
>
> **Output:** Approved metric framework + deck skeleton (signed off by stakeholders).

### 1a. Pre-Kickoff

> Two parallel tracks run after the deal closes and before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                           | Purpose                                                            | Format             |
| ------------------------------ | ------------------------------------------------------------------ | ------------------ |
| Intro video                    | Explain the reporting pack project, Power 10 metrics, what board-ready means | Video (5-10 min)   |
| Definition Alignment Document  | Pre-fill with recommended metric definitions for stakeholder review | Google Doc         |
| Intake form                    | Capture audiences, use cases, existing reports, data system access  | Google Form or Doc |

**Intake form captures:**
- All audiences who will consume the reporting pack (board, investors, exec team, functional leaders, all-hands)
- Delivery cadence preferences (monthly, quarterly, or both)
- Format preferences (slides, PDF, live dashboard link)
- Existing reports they want to consolidate or replace
- Known data quality concerns or metric definition disputes
- Internal report owner (named individual, not a team)

**Completion tracking:** Report owner follows up. Don't cancel kickoff if incomplete, but push hard — metric definition work cannot begin without audience clarity.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                                     | Output                                           |
| ---- | -------------------------------------------------------------------------- | ------------------------------------------------ |
| 1    | Gather inputs (intake form, system access, existing reports)               | Raw data collected                               |
| 2    | Audit existing reports from each function (Sales, Marketing, CS, Finance)  | Current state report inventory                   |
| 3    | Map Power 10 GTM Metrics to client's data sources (ASSUMED)               | v0 metric framework                             |
| 4    | Draft audience matrix (stakeholder -> use case -> detail level -> cadence) | v0 audience matrix                              |
| 5    | Identify metric definition inconsistencies across existing reports         | Gap analysis + conflict log                      |
| 6    | Create kickoff presentation with v0 metric framework and audience matrix   | Kickoff deck                                    |

**Critical:** Mark metric-to-source mappings as ASSUMED. The kickoff call validates these assumptions against reality.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on metric definitions BEFORE building anything. According to Gartner, the average financial impact of poor data quality on organizations is $9.7 million per year [1]. Metric definition alignment is the cheapest insurance against rework.

| Term                          | Our Definition                                                                        | Internally Approved? |
| ----------------------------- | ------------------------------------------------------------------------------------- | -------------------- |
| Annual Recurring Revenue (ARR)| Annualized value of active recurring contracts, excluding one-time fees               | [ ] Yes / [ ] No     |
| Net Revenue Retention (NRR)   | (Starting ARR + Expansion - Contraction - Churn) / Starting ARR                      | [ ] Yes / [ ] No     |
| Customer Acquisition Cost     | Total sales + marketing spend / new customers acquired in period                      | [ ] Yes / [ ] No     |
| Pipeline Coverage             | Total qualified pipeline / revenue target for period                                  | [ ] Yes / [ ] No     |
| SQL                           | Sales Qualified Lead — [client-specific criteria to define]                           | [ ] Yes / [ ] No     |
| Forecast Accuracy             | Actual bookings / forecasted bookings at start of quarter                             | [ ] Yes / [ ] No     |
| Churn Rate                    | Lost ARR / starting ARR in period, excluding downgrades                               | [ ] Yes / [ ] No     |
| LTV:CAC Ratio                 | Customer lifetime value / customer acquisition cost                                   | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your leadership team. Check "Yes" when approved. We cannot proceed to data work until all metric definitions are aligned. If two teams define the same metric differently, flag it — we will resolve in the kickoff call.

---

### 1b. Kickoff Call

> **Purpose:** Present v0 metric framework and get alignment on audiences, definitions, and structure. We walk in with work done — customer reacts, not creates from scratch.

#### Agenda (60-90 min)

| Time  | Topic                             | What Happens                                                         |
| ----- | --------------------------------- | -------------------------------------------------------------------- |
| 0-15  | Walk through v0 metric framework  | "Here's our recommended Power 10 + operational KPIs based on intake" |
| 15-30 | Validate audiences and use cases  | Confirm who reads what, how often, at what detail level              |
| 30-45 | Definition alignment              | Review Definition Alignment Doc, surface conflicts                   |
| 45-55 | Identify data gaps                | Which metrics can't be sourced today, who owns resolution            |
| 55-60 | Next steps                        | Schedule functional leader meetings, assign metric owner homework    |

#### What We Bring

- v0 metric framework (Power 10 + recommended operational KPIs per function)
- v0 audience matrix (stakeholder -> use case -> detail level -> cadence)
- Current state report inventory (what exists today across systems)
- Definition Alignment Document (pre-filled with our recommendations)
- Questions list (conflicts found in existing reports, data source uncertainties)

#### What We Leave With

- Feedback and corrections on metric framework (info needed for v1)
- Confirmed audiences and use cases (or clear blockers if stakeholders disagree)
- Identified metric definition conflicts (with owners assigned to resolve)
- Schedule for functional leader meetings
- Clear homework: each functional leader confirms their operational KPIs

---

### 1c. Alignment Loop &amp; Strategic Meeting Cadence

> **Purpose:** Iterate on the metric framework and deck structure until sign-off. Each meeting resolves a set of open questions.

#### The Pattern

```
Kickoff Call (gather info on audiences, metrics, data sources)
    |
    v
Update metric framework -> v1
    |
    v
Meeting 2: Metric Definitions (each function confirms) -> v2 framework
    |
    v
Meeting 3: Deck Structure (present skeleton, agree layout) -> approved skeleton
    |
    v
Final Review -> Sign-off
```

#### Meeting-by-Topic Breakdown

| Meeting Type              | Focus                                                   | Stakeholder                              |
| ------------------------- | ------------------------------------------------------- | ---------------------------------------- |
| Metric Definitions        | Lock calculation methodology, data source, owner per metric | VP Sales, VP Marketing, CS Lead, Finance |
| Deck Structure Review     | Section order, visual hierarchy, executive summary layout | Executive sponsor, report owner          |
| Data Validation           | Verify historical numbers match known benchmarks         | RevOps, Finance                          |
| Final Review              | Full walkthrough of completed framework + skeleton       | All stakeholders                         |

#### Before Each Meeting

1. Process previous meeting notes and update metric framework
2. Prepare specific questions for next validation round
3. Flag any data source issues discovered during prep

#### During Each Meeting

1. Walk through current version of the metric framework or deck skeleton
2. Capture corrections and new requirements
3. Validate what is now CONFIRMED vs. still ASSUMED
4. Identify remaining open items

#### After Each Meeting

1. Update metric framework and track ASSUMED -> CONFIRMED movement
2. Update data source inventory with new access or findings
3. Prepare for next meeting

#### Typical Timeline

| Milestone               | Timing                                              |
| ----------------------- | --------------------------------------------------- |
| Pre-kickoff prep        | 3-5 days                                            |
| Kickoff call            | Day 1 of engagement                                 |
| Meeting loop (2-3 meetings) | 1-2 weeks (depends on stakeholder availability) |
| Final review + sign-off | When all metric definitions CONFIRMED               |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything before proceeding to data work and deck construction.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by all stakeholders
- [ ] Metric framework complete: every metric has name, formula, source, owner
- [ ] Audience matrix confirmed: all consumers, use cases, detail levels, cadences
- [ ] Deck skeleton approved: sections, slide types, visual hierarchy
- [ ] Data source inventory complete: access confirmed for all systems
- [ ] No metric definition conflicts outstanding
- [ ] Customer understands what we are building and the update process

#### Decision Point

- **Proceed to Engineering** -> Data work and deck construction begin
- **Loop back to 1c** -> Outstanding metric conflicts or missing stakeholder input

---

## Phase 2: Engineering

> **Goal:** Build the data extraction process and construct the reporting deck with validated historical data.
>
> **Output:** Complete, board-ready reporting pack populated with verified data, tested and customer-approved.

| Project Type | Engineering Weight | What Happens                                               |
| ------------ | ------------------ | ---------------------------------------------------------- |
| This project | Medium (30-40%)    | Data extraction setup, deck construction, historical validation |

### Sub-Phases

```
2a Data Architecture -> 2b Data Extraction Build -> 2c Deck Construction + Validation -> 2d QA + Sign-Off
```

---

### 2a. Tech Spec (Data Architecture Map)

> **Purpose:** Translate the approved metric framework into a technical data architecture.

**Input:** Signed-off metric framework + data source inventory from Phase 1

**What happens:**

1. Map each approved metric to its authoritative data source
2. Document extraction method per source (API pull, scheduled export, manual query)
3. Identify cross-system calculations (e.g., CAC requires marketing spend + sales cost data)
4. Define data staging approach (spreadsheet, lightweight database, or BI tool)
5. Specify refresh frequency capabilities per source

**Output:** Data architecture map containing:

- Metric -> source -> extraction method -> refresh frequency
- Cross-system calculation logic (which metrics need data from multiple sources)
- Data staging area design
- Build sequence (what to extract first, dependencies)

---

### 2b. Engineering Handoff (Data Extraction Build)

> **Purpose:** Build the repeatable data extraction process.

**What gets built:**

| Component                     | What It Does                                              | How to Test                                |
| ----------------------------- | --------------------------------------------------------- | ------------------------------------------ |
| Scheduled exports / API pulls | Pull data from CRM, MAP, CS platform, finance system     | Run extraction, verify row counts          |
| Data staging area             | Central location where all metric data lands pre-deck     | All sources deposit data in correct format |
| Validation checks             | Catch data anomalies: nulls, duplicates, outliers         | Inject known bad data, verify flags fire   |
| Manual step documentation     | Instructions for any metrics requiring manual input       | Report owner can follow independently      |

**Build sequence:**
1. Set up data staging area (spreadsheet or database)
2. Connect primary data sources (CRM pipeline, marketing funnel, CS retention, finance ARR)
3. Build validation rules for each data feed
4. Test full extraction cycle end-to-end
5. Document manual steps with time estimates

---

### 2c. Build (Deck Construction + Historical Validation)

> **Purpose:** Construct the reporting deck and validate with historical data.

**Input:** Data architecture map + working data extraction process

**Deck construction sequence:**

1. **Executive Summary section** (3-5 slides)
   - Business health scorecard with Power 10 metrics
   - Month-over-month or quarter-over-quarter trend visualization
   - "Top 3 Wins / Top 3 Concerns" commentary section
   - Forward-looking indicators (pipeline coverage, forecast vs. target)

2. **Functional Deep-Dive sections** (4-6 slides per function)
   - Sales: pipeline metrics, conversion rates, rep productivity, forecast accuracy
   - Marketing: funnel metrics, channel performance, CAC components, attribution
   - Customer Success: retention, expansion, NPS/health scores, churn drivers
   - Finance/ARR: revenue actuals, cohort analysis, unit economics

3. **Appendix** (5-10 slides)
   - Metric definition glossary with calculation formulas
   - Detailed data tables for drill-down
   - Data sources and refresh dates
   - Methodology notes for complex calculations

**Historical data validation:**
- Pull 3-6 months of historical data (ideally 6-12 months)
- Cross-reference against known benchmarks: previous board decks, finance actuals, investor reports
- Reconcile discrepancies between sources
- Document any data gaps or unreliable periods
- Get stakeholder confirmation that historical numbers are accurate

Research shows that nearly one-third of analysts spend more than 40% of their time vetting and validating analytics data before it can be used for decision-making [2]. A well-validated historical dataset eliminates this burden going forward.

**Build tracking:**

- [ ] Executive summary section: complete with Power 10 metrics
- [ ] Sales deep-dive section: pipeline, conversion, productivity, forecast
- [ ] Marketing deep-dive section: funnel, channels, CAC, attribution
- [ ] CS deep-dive section: retention, expansion, health, churn
- [ ] Finance/ARR section: revenue, cohorts, unit economics
- [ ] Appendix: definitions, data tables, methodology
- [ ] Navigation system: table of contents, section dividers
- [ ] Color coding: green/yellow/red performance indicators applied
- [ ] Historical data loaded and validated for all sections

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify the reporting pack is accurate, complete, and usable.

**Two types of testing:**

| Type              | Who       | Purpose                                                          |
| ----------------- | --------- | ---------------------------------------------------------------- |
| Technical Testing | Our team  | Verify data flows correctly, calculations match formulas, no errors |
| Customer Testing  | Customer  | Verify it tells the right story, numbers match expectations      |

**Technical testing checklist:**

- [ ] All Power 10 metrics calculated correctly (cross-reference against manual calculation)
- [ ] Functional KPIs match source system reports
- [ ] Historical data reconciles with previous board decks and finance actuals
- [ ] Trend calculations correct (MoM, QoQ percentages)
- [ ] Color coding thresholds applied correctly (green/yellow/red)
- [ ] All slides render correctly in both edit and presentation mode
- [ ] Navigation works (table of contents links, section dividers)
- [ ] Data refresh dates display accurately
- [ ] Executive summary can stand alone for time-constrained audiences

**Customer testing:**

- Walk customer through the full deck section by section
- Have them verify numbers against their own records
- Test the executive summary with the CEO or CFO if possible
- Capture feedback on layout, emphasis, and missing context

**Engineering sign-off checkpoint:**

- [ ] Deck matches approved skeleton from Phase 1
- [ ] All metrics match signed-off definitions
- [ ] Historical data validated by stakeholders
- [ ] Customer has tested and approved
- [ ] Ready for enablement

**Decision point:**

- **Proceed to Enablement** -> Deck is built and validated, needs training and runbook
- **Loop back to Build** -> Data issues found, calculations need correction

---

## Phase 3: Enablement

> **Goal:** Customer team can independently update and distribute the reporting pack.
>
> **Output:** Trained report owner with documentation, stabilized update process, no critical issues.

### Sub-Phases

```
3a Training Prep -> 3b Training Sessions -> 3c Hypercare (First Live Cycles) -> 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create the update runbook and training materials.

**Input:** Completed reporting pack + data architecture map + metric framework

**Output:** Training and documentation package containing:

- **Update runbook** — step-by-step process for monthly/quarterly refresh:
  1. Data extraction steps with screenshots and timing (target: day 1-2 of update cycle)
  2. Data validation checks to run before updating the deck (target: day 2)
  3. Section-by-section update checklist (target: day 2-3)
  4. Commentary template for "Top 3 Wins / Concerns" (target: day 3)
  5. Review and approval workflow before distribution (target: day 3-4)
  6. Distribution process: who gets what, when, in what format
- **Video walkthrough scripts** — what to record for deck walkthrough and update process
- **Troubleshooting guide** — common data issues and resolution steps
- **FAQ draft** — based on questions that typically arise with similar projects

**Update cycle timeline (monthly cadence):**

| Day       | Task                                        | Owner        | Time Estimate |
| --------- | ------------------------------------------- | ------------ | ------------- |
| Day 1     | Pull data from all sources                  | Report owner | 1-2 hours     |
| Day 2     | Run validation checks, flag anomalies       | Report owner | 30-60 min     |
| Day 2-3   | Update deck (data + commentary)             | Report owner | 1-2 hours     |
| Day 3-4   | Review with executive sponsor, get approval | Exec sponsor | 30 min        |
| Day 4-5   | Distribute to all audiences                 | Report owner | 15 min        |
| **Total** |                                             |              | **3-5 hours** |

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to customer team so they can own the update cycle.

**Two types of training:**

| Type                | Audience                         | Focus                                                                | Duration  |
| ------------------- | -------------------------------- | -------------------------------------------------------------------- | --------- |
| Leadership training | CEO, CFO, VP Sales, VP Marketing | How to read the pack, interpret signals, what actions to take        | 30 min    |
| Technical handoff   | Report owner, RevOps admin       | How to pull data, update the deck, run validation, troubleshoot      | 60-90 min |

**Leadership training covers:**
- How to read the executive summary scorecard
- What green/yellow/red indicators mean and when to act
- How to use the pack in board meetings and investor updates
- Where to find drill-down detail in the functional sections

**Technical training covers:**
- Full update cycle walkthrough using the runbook
- Data extraction from each source (live demonstration)
- Validation checks: what to look for, how to resolve anomalies
- Deck update process: which cells/slides to touch, which are automated
- Commentary writing: how to frame wins and concerns
- Common data issues and troubleshooting steps
- Practice run: report owner updates one section while Architect observes

**Training delivery:**

1. Schedule sessions with appropriate stakeholders
2. Deliver training live (recorded for future reference)
3. Record video walkthroughs for each major process
4. Answer questions, note gaps in documentation
5. Update runbook based on questions that arise

**Output:**

- Trained report owner who can update independently
- Trained leadership who can interpret the pack
- Video recordings for future reference and new hire onboarding
- Questions log (feeds into FAQ document)

---

### 3c. Hypercare (First Live Cycles)

> **Purpose:** Support the first independent update cycles to ensure smooth transition.

**Duration:** 2 update cycles (2 months for monthly cadence, 1 quarter for quarterly)

**First update cycle (heavy support):**
- Shadow report owner during data pull and deck update
- Provide real-time support for questions or issues
- Review completed deck before distribution
- Collect feedback on runbook clarity and process gaps
- Refine documentation based on first cycle experience

**Second update cycle (light support):**
- Report owner runs the update independently
- Architect available via email for questions
- Review final deck before distribution (quick sanity check)
- Capture any remaining documentation gaps

**What we are watching for:**
- Update cycle time: is it staying under 4-5 hours?
- Data quality: are validation checks catching issues?
- Stakeholder satisfaction: are audiences finding the pack useful?
- Process adherence: is the runbook being followed?

**When to skip:** If the report owner demonstrates full independence during training (unlikely for first project), hypercare can be shortened to 1 cycle.

**Output:** Stabilized update process, refined runbook, no critical issues outstanding

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm customer can operate the reporting pack independently.

**Validation checkpoint:**

- [ ] All training sessions delivered (leadership + technical)
- [ ] Training recordings and documentation provided
- [ ] First live update cycle completed successfully
- [ ] Second cycle completed with minimal support
- [ ] Update cycle time is under 5 hours
- [ ] Report owner is confident in the process
- [ ] No critical data or process issues outstanding
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** -> Customer is enabled, project wrapping up
- **Extend Hypercare** -> Update process still unstable, needs 1 more cycle

---

## Phase 4: Handoff

> **Goal:** Clean project close with maintenance plan established and retention/expansion path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the reporting pack, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule -> 4b Internal Handoff -> 4c External Handoff -> 4d Project Close
                                                   (Project Team -> Customer)   (Archive + Debrief)
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

| Monthly Task               | What to Check                                                  | Red Flag Threshold                              |
| -------------------------- | -------------------------------------------------------------- | ----------------------------------------------- |
| Data extraction QA         | All sources returning data, no nulls or duplicates             | Any source failing to return data               |
| Metric accuracy spot-check | Pick 2-3 metrics, verify calculation against source system     | >5% variance between deck and source            |
| Update cycle time tracking | How long the update took this month                            | >6 hours (target is &lt;4 hours)                |
| Stakeholder feedback pulse | Quick check: is leadership using the pack, any complaints?     | Pack not referenced in last board/exec meeting  |

**Quarterly Tasks:**

| Quarterly Task                  | What to Review                                                | Action if Off-Track                              |
| ------------------------------- | ------------------------------------------------------------- | ------------------------------------------------ |
| Full metric framework review    | Are all metrics still relevant? Any new metrics needed?       | Add/remove metrics, update definitions           |
| Audience and distribution audit | Are the right people getting the right version?               | Update distribution list, adjust detail levels   |
| Data source health check        | Are all API connections and exports still working reliably?   | Fix broken connections, update extraction scripts |
| Deck design refresh             | Is the visual design still effective? Any feedback?           | Update slide templates, adjust visualizations    |

**After First Business Cycle (30-90 days post-launch):**

- Report utilization check: Is the pack actually being used in board meetings, investor calls, and MBRs?
- Update process validation: Is the report owner maintaining the cadence without prompting?
- Data trust assessment: Have stakeholders stopped questioning the numbers?
- Key question: Has the pack become the single source of truth for GTM performance?

**Refinement Triggers (when to re-engage):**

| Trigger                      | Threshold                                           | Response                                                 |
| ---------------------------- | --------------------------------------------------- | -------------------------------------------------------- |
| Update cycle time creeping   | >6 hours for 2+ consecutive months                  | Audit process, identify bottlenecks, simplify            |
| New data source needed       | Business adds new tool or system                    | Scope data integration addition                          |
| Metric definitions challenged| Stakeholders reopen definition debates              | Facilitate realignment session                           |
| Deck not being used          | Pack not referenced in 2+ consecutive board meetings| Diagnose: wrong content, wrong format, or wrong audience |
| Major business change        | Acquisition, new segment, reorg                     | Scope reporting pack restructure                         |

**Every 6-12 Months:**

- Full metric framework recalibration against business strategy changes
- Benchmark comparison: how do the client's metrics compare to industry standards
- Deck structure overhaul if business has materially changed (new segments, new GTM motions)
- Consider upgrading from slide-based to BI-connected if update burden is too high

---

### 4b. Internal Handoff

> **Purpose:** Transfer context so ongoing relationship can be managed.

**What the Architect needs to know:**

- What was built: reporting pack structure, key audiences, delivery cadence
- Customer context: who the report owner is, stakeholder communication preferences, any political dynamics around metrics
- Metric sensitivity: which numbers get the most scrutiny (usually ARR, pipeline, and NRR)
- Common issues: data extraction failures, metric definition drift, update fatigue
- When to escalate: metric definition changes, new data source integration, deck restructuring

**Escalation guidelines:**

| Issue Type                                            | Who Handles                      | Examples                                            |
| ----------------------------------------------------- | -------------------------------- | --------------------------------------------------- |
| Small tweaks, formatting, minor questions              | Architect                        | Slide formatting, color changes, distribution list  |
| Data source issues, extraction failures                | Architect (first attempt) -> SME | API timeout, export format change                   |
| Metric definition changes, new metrics, restructuring  | SME                              | Adding new segment, changing CAC formula, new audience |

**For Dedicated engagements:** Architect also receives the maintenance schedule (4a) and becomes responsible for executing it. SME walks Architect through each maintenance task.

---

### 4c. External Handoff (Project Team -> Customer)

> **Purpose:** Formal project completion with customer.

**Final project meeting:**

- Review what was delivered: reporting pack, metric framework, update runbook, training recordings
- Walk through documentation package item by item
- Confirm nothing outstanding
- Walk through the maintenance schedule (monthly, quarterly, annual tasks)
- Answer final questions
- Make it explicit: "Project complete"
- **For Single Project engagements:** Hand over the maintenance schedule and walk through it in detail

**Documentation package:**

- Completed reporting pack (deck template with current data)
- Metric definition glossary with calculation formulas
- Data architecture map (metric -> source -> extraction method)
- Update runbook with screenshots and timeline
- Training video walkthroughs (deck walkthrough + update process)
- Troubleshooting guide
- FAQ document
- Maintenance schedule
- Support contact info

**For Single Project engagements:** Record a video walkthrough of the maintenance schedule for future reference.

**Output:** Customer owns the reporting pack. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location
- [ ] Handoff documentation complete
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized

#### Internal Debrief (Optional but Recommended)

- What went well? (e.g., metric alignment process, stakeholder engagement)
- What would we do differently? (e.g., data access issues discovered late, too many meetings)
- Any learnings to feed back into SOPs?
- Was the update cycle time target (&lt;4 hours) realistic for this client?

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell -> Downsell -> Retry  |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (project team handles monthly updates)
   | if no
   v
2. Downsell: Another project (dashboard infrastructure, attribution model, ARR reporting, growth model)
   | if yes
   v
3. Retry retainer at end of next project cycle
```

**Script:**

> "Now that the reporting pack is complete and your team is running updates independently, there are two ways we can continue working together. Option 1: We handle the monthly updates as part of managed services — your report owner gets that time back, and we ensure the pack stays board-ready. Option 2: If there is another reporting or analytics challenge you need help with, we can scope that out. Which sounds more interesting?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On [date ~quarter out], we'll review how the reporting pack is performing — are the metrics still relevant, is the update process smooth, and does anything need adjusting?"

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                                                       |
| ------------------- | ---------------------------------------------------------------------------------- |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks                                   |
| 2. Review metrics   | Check: Is the pack still being used? Any complaints? Update cycle time trending?   |
| 3. Decide ownership | Can Architect handle this check-in, or need SME?                                   |
| 4. Prep materials   | If SME needed, brief them. If Architect, prep talking points.                      |

**At the refinement check-in:**

- Review pack utilization and stakeholder satisfaction
- Identify any adjustments needed (new metrics, new audiences, format changes)
- If minor: Architect handles tweaks
- If major: Scope refinement project (restart the assembly line)

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables &amp; Assets Summary

**Strategic Deliverables:**

- Metric framework document (Power 10 GTM Metrics + operational KPIs, with definitions, formulas, sources, owners)
- Audience matrix (stakeholder -> use case -> detail level -> cadence)
- Definition Alignment Document (signed off by all stakeholders)

**Technical Deliverables:**

- Monthly/Quarterly GTM Reporting Pack (complete slide deck with historical data)
- Data extraction process (scripts, scheduled exports, or manual procedures documented)
- Data staging area (spreadsheet or database where raw data lands before deck update)

**Documentation Package:**

- Training video walkthroughs (deck walkthrough + update process walkthrough)
- Update runbook with step-by-step instructions and screenshots
- Metric definition glossary with calculation formulas
- Troubleshooting guide for common data issues
- FAQ document
- Maintenance schedule (monthly, quarterly, annual tasks)
- Definition Alignment Document (final version)

---

## Appendix

### What Each Phase Produces

| Phase                    | Output                                                                | Gate Criteria                                                                     |
| ------------------------ | --------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| **Phase 1: Strategy**    | Signed-off metric framework + deck skeleton + Definition Alignment Doc | All metric definitions approved, audiences confirmed, deck structure agreed       |
| **Phase 2: Engineering** | Built reporting pack with validated historical data                    | Data validated, deck populated, customer approved                                 |
| **Phase 3: Enablement**  | Trained team with update runbook                                       | All training delivered, 2 update cycles complete, team independent                |
| **Phase 4: Handoff**     | Independent customer + archived project                                | Internal/external handoffs complete, maintenance plan in place, project closed    |

### How to Adapt Per Project Type

This project is **Balanced** — strategy and engineering carry roughly equal weight, with meaningful enablement required.

| Project Profile | Strategy Weight | Engineering Weight | Enablement Weight | Notes                                                 |
| --------------- | --------------- | ------------------ | ----------------- | ----------------------------------------------------- |
| This project    | 35-40%          | 30-35%             | 25-30%            | Heavy metric alignment, medium deck build, meaningful training |

**Adaptation rules for this project:**
- Phase 1 cannot be compressed — metric definition alignment is the foundation. Rushing it causes rework in every subsequent phase.
- Phase 2 weight depends on data accessibility. If client has clean, accessible data, engineering is lighter. If data lives in spreadsheets and manual exports, engineering is heavier.
- Phase 3 is critical — the pack is only valuable if someone updates it. A beautiful deck that stops being updated after month 2 is a failed project.
- Phase 4 always applies — the maintenance schedule is what keeps the pack alive.

### Single vs Dedicated Client Split

| Engagement Type               | What It Means                        | Key Difference                              |
| ----------------------------- | ------------------------------------ | ------------------------------------------- |
| **Single Project**            | One-off reporting pack engagement    | Customer owns maintenance post-handoff (4c) |
| **Dedicated (Multi-Project)** | Ongoing retainer / multiple projects | Architect owns maintenance post-handoff (4b)|

### Phase 1 Guide: Strategy

**1. We educate.** Most clients know they need better reporting, but they don't know what "board-ready" actually looks like, which metrics matter most, or how to standardize definitions across teams. We educate them on Power 10 GTM Metrics and what a mature reporting process looks like.

**2. We drive alignment.** The #1 risk in this project is metric definition disagreements. Marketing calculates CAC one way, Finance another. Sales defines "pipeline" differently than RevOps. We force alignment through the Definition Alignment Document before any data work begins.

**3. We come with an opinion.** We show up with a recommended metric framework based on having built reporting packs for dozens of B2B SaaS companies. The client confirms and adjusts, not creates from scratch.

**4. We show best practices.** We anchor in what works: proven deck structures, the right level of detail per audience, and update processes that take 4 hours, not 20. Organizations with a RevOps function that standardizes reporting see up to 36% more revenue growth and 28% higher profitability [3].

**Why Phase 1 matters:** Metric definition disagreements that surface during deck construction (Phase 2) are 3-5x more expensive to fix than when caught during Phase 1. The Definition Alignment Document is the single most important artifact in this project. Without it, every data issue becomes a political issue.

### Phase 2 Guide: Engineering

**Data Architecture (2a):** Get the mapping right before building anything. Every metric needs one authoritative source. If two systems have the same metric, pick one as primary and document why.

**Extraction Build (2b):** Automate where possible, but document manual steps thoroughly. The update process must be repeatable by someone other than the person who built it.

**Deck Build (2c):** Design for the executive summary first — that is what 80% of stakeholders will actually read. Push detail to functional sections and appendix. Companies that focus on executive-level reporting first see 15-30% improvement in operational efficiency within the first year [4].

### Phase 3 Guide: Enablement

**Training Prep (3a):** The update runbook is the single most important enablement artifact. If the report owner leaves, a new person must be able to pick up the runbook and produce the next update without handholding.

**Hypercare (3c):** Support two full update cycles. The first cycle reveals process gaps. The second cycle confirms the fixes work. Office hours pattern: put recurring 30-min slot on calendar, report owner can hop on with any questions.

### Phase 4 Guide: Handoff

**Why Maintenance Schedules Matter:**

The most common failure mode for a reporting pack is not a broken template — it is a template that stops being updated because no one maintains the process. According to research, inconsistent data leads directly to flawed strategic choices, and once stakeholders catch inconsistencies, trust unravels within weeks [5]. The maintenance schedule prevents drift by making monitoring explicit and cadenced.

**The Reporting Pack Drift Pattern:**

Without maintenance, reporting packs follow a predictable decay curve:
- Month 1-2: Report owner updates on time, pack is referenced in meetings
- Month 3-4: Update gets delayed by a week, then two weeks. Commentary section gets skipped.
- Month 5-6: Stakeholders stop looking at the pack because it is "stale." They revert to pulling their own numbers from source systems.
- Month 7+: The pack stops being updated entirely. The project's value goes to zero.

The maintenance schedule in 4a is designed to catch this drift at month 2, not month 7.

---

## References

[1] [Gartner - Data Quality: Why It Matters and How to Achieve It](https://www.gartner.com/en/data-analytics/topics/data-quality)

[2] [Forrester - Data Governance Explained: Success Factors for 2025](https://atlan.com/forrester-data-governance/)

[3] [TechCXO - The True ROI of RevOps: How Revenue Operations Drive Predictable Growth](https://www.techcxo.com/insights-undestanding-the-true-roi-of-revops/)

[4] [AgencyAnalytics - B2B Reporting: Tools, Strategies &amp; Dashboards for 2025](https://agencyanalytics.com/blog/b2b-reporting)
