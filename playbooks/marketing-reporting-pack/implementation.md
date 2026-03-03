# Marketing Reporting Pack — Implementation

## Project One-Pager

### Marketing Reporting Pack One-Pager

#### Project Type

- Category: Balanced
- Primary Deliverable: Self-updating monthly reporting pack with standardized dashboards showing funnel performance, channel attribution, campaign ROI, and pipeline contribution

##### Phase Relevance

| Phase          | Applies? | Weight | Notes                                                    |
| -------------- | -------- | ------ | -------------------------------------------------------- |
| 1. Strategy    | Yes      | Medium | 2-3 refinement loops for KPI alignment and data strategy |
| 2. Engineering | Yes      | Heavy  | Dashboard builds, data pipelines, automation setup       |
| 3. Enablement  | Yes      | Medium | Training sessions + reporting cadence establishment      |
| 4. Handoff     | Yes      | Medium | Internal + External with maintenance schedule            |

· · ·

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │    Medium    │     │    Heavy     │     │    Medium    │     │    Medium    │
  │ 1a→1b→1c→1d │     │ 2a→2b→2c→2d │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   KPI alignment        Dashboard build      Team training        Ownership
   Data strategy         Data pipelines       Cadence setup        transfer
```

**This project's flow:**
- Full 4-phase. Medium strategy (KPI and metric definition alignment), heavy engineering (dashboard construction, data pipeline setup, automation), medium enablement (training + cadence establishment).
- Phase 2 carries the most weight because data pipeline reliability and dashboard accuracy are the core deliverables.
- Customers with existing BI infrastructure may have lighter Phase 2 if dashboards are extensions of existing systems.

· · ·

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Watch intro video explaining what the reporting pack delivers and why metric definitions matter
- [ ] Complete intake form: current reporting tools, KPIs tracked today, questions leadership needs answered monthly
- [ ] Get stakeholder sign-off on metric definitions (MQL, SQL, pipeline contribution, marketing-sourced vs. influenced)
- [ ] Provide admin access credentials for MAP (HubSpot/Marketo), CRM (Salesforce), ad platforms, and any BI tools

##### Track B: Architect Prep
- [ ] Pull current data source inventory from MAP and CRM
- [ ] Audit existing dashboards and reports for coverage gaps
- [ ] Run data quality diagnostic: UTM parameter consistency, naming conventions, duplicate records
- [ ] Create v0 reporting template mockup with recommended KPIs aligned to growth model

· · ·

#### Refinement Loop (1b &gt; 1c &gt; 1d)

| Meeting      | Sub-Phase | Focus                                                              | Stakeholder                     | Output                         |
| ------------ | --------- | ------------------------------------------------------------------ | ------------------------------- | ------------------------------ |
| Kickoff      | 1b        | Present v0 reporting template, validate KPI priorities             | VP Marketing, Marketing Ops     | Feedback for v1                |
| Refinement 1 | 1c        | Review v1 dashboard wireframes, validate data source mappings      | VP Marketing, Marketing Ops     | Approved dashboard design      |
| Refinement 2 | 1c        | Review metric definitions, attribution model, data gaps            | Marketing Ops, RevOps           | Final metric glossary          |
| Sign-Off     | 1d        | Approve reporting requirements, dashboard design, metric glossary  | VP Marketing, RevOps, Finance   | Approved strategic package     |

· · ·

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held
- [ ] 1c. Refinement loop complete (v0 &gt; vFinal)
- [ ] 1d. Strategic sign-off obtained

##### Phase 2: Engineering
- [ ] 2a. Tech spec created (dashboard components, data pipeline design, automation rules)
- [ ] 2b. Engineering handoff meeting held
- [ ] 2c. Build complete (dashboards, pipelines, automations)
- [ ] 2d. QA/Test + customer sign-off

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped (video scripts, quick-reference guide)
- [ ] 3b. Training sessions delivered (leadership + technical)
- [ ] 3c. Hypercare period complete (2 weeks)
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff complete
- [ ] 4c. External handoff (delivery team &gt; Customer) complete
- [ ] 4d. Project closed and archived

· · ·

#### Document Types

##### Working Documents (iterate together)

| Document                    | Purpose                                           | When Complete                          |
| --------------------------- | ------------------------------------------------- | -------------------------------------- |
| Intake form                 | Capture current tools, KPIs, reporting questions   | All fields filled by customer          |
| Data source inventory       | Map all data sources with gap analysis             | All sources cataloged, gaps documented |
| Metric glossary (draft)     | Define all KPIs with calculation methods           | All metrics defined, ownership assigned |
| Dashboard wireframe         | Visual layout of reporting pack sections           | Approved by stakeholders               |

##### Deliverables (polished outputs)

| Deliverable                     | Created From              | Customer Uses For                                |
| ------------------------------- | ------------------------- | ------------------------------------------------ |
| Monthly reporting pack dashboard | Dashboard wireframe + data pipeline | Monthly marketing performance review      |
| Metric glossary (final)         | Draft metric glossary      | Cross-team alignment on definitions              |
| Data source documentation       | Data source inventory      | Troubleshooting and expansion reference          |
| Automation configuration doc    | Tech spec                  | Understanding report generation and distribution |

· · ·

#### Enablement Details

##### Training Types

| Type       | Audience                          | Focus                                              | Duration |
| ---------- | --------------------------------- | -------------------------------------------------- | -------- |
| Leadership | VP Marketing, CMO, Finance        | How to interpret dashboards, read trends, take action | 30 min   |
| Technical  | Marketing Ops, RevOps Admin       | How to maintain dashboards, add metrics, troubleshoot | 60 min   |
| Team       | Full marketing team               | How to use reports in daily/weekly workflow          | 45 min   |

##### Hypercare
- Applies: Yes
- Duration: 2 weeks post-launch
- Office Hours: Yes — weekly 30-min slot for first 2 weeks

##### Training Assets to Create
- [ ] Video walkthrough: Executive dashboard (5 min)
- [ ] Video walkthrough: Technical maintenance guide (10 min)
- [ ] Doc: Metric glossary with calculation methods
- [ ] Doc: Quick-reference guide for common dashboard actions
- [ ] Doc: "How to add a new metric" expansion guide

· · ·

#### Handoff & Retention

##### Internal Handoff
- Key context to transfer: Dashboard tool used (Tableau/Looker/native CRM), data refresh schedules, known data quality quirks, metric definitions that were contentious
- Escalation trigger: Any changes to data pipeline connections, addition of new data sources, or metric definition changes

##### External Handoff
- Final meeting agenda: Review all dashboard sections, walk through maintenance schedule, confirm automation is running, hand over admin access
- Documentation package: Metric glossary, data source documentation, troubleshooting guide, maintenance schedule, training video walkthroughs

##### Maintenance Schedule
- Monthly: Data quality spot-check, metric accuracy validation, dashboard usage review
- Quarterly: Full metric definitions review, data source health audit, new KPI evaluation
- Who owns: Single project = customer owns | Dedicated = delivery team owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services (ongoing dashboard optimization and metric expansion) &gt; if no &gt; Downsell: Another project (e.g., Lead Attribution, Growth Model) &gt; Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~1 quarter after launch
- Internal prep trigger: 2 weeks before
- Decision: Project lead handles / specialist needed

· · ·

#### Key Assets

| Asset                        | When Used            |
| ---------------------------- | -------------------- |
| Reporting intake form        | Phase 1a Pre-Kickoff |
| Dashboard wireframe template | Phase 1c Refinement  |
| Metric glossary template     | Phase 1c Refinement  |
| Data audit diagnostic        | Phase 1a Pre-Kickoff |

· · ·

#### Definition Alignment Terms

| Term                     | Typical Definition                                                                                     |
| ------------------------ | ------------------------------------------------------------------------------------------------------ |
| MQL                      | A lead that meets marketing qualification criteria (behavioral + firmographic score thresholds)         |
| SQL                      | A lead accepted by sales as ready for direct outreach and qualification                                |
| Marketing-Sourced Pipeline | Opportunities where the first touch was a marketing activity (campaign, content, event)               |
| Marketing-Influenced Pipeline | Opportunities where marketing touched the contact at any point before close, regardless of first touch |
| Cost Per MQL             | Total marketing spend divided by total MQLs generated in the period                                    |
| Pipeline Velocity        | Average time from opportunity creation to close, measured in days                                      |
| Channel Attribution      | The method used to credit marketing channels for pipeline and revenue contribution                     |

· · ·

#### Common Gotchas
- MQL counts differ between MAP and CRM because sync timing and deduplication rules vary &gt; Align sync schedules and document known lag windows
- UTM parameters are inconsistently applied across campaigns &gt; Audit and enforce naming conventions before building dashboards
- Dashboard shows marketing-sourced pipeline but sales disputes the numbers &gt; Validate attribution logic with RevOps before launch; document the method in the metric glossary
- Data refreshes fail silently, causing stale dashboards &gt; Set up error alerting on all data connections with email notifications
- Stakeholders stop using dashboards after initial excitement &gt; Embed dashboards into standing meeting agendas and automate distribution

· · ·

#### Methodology Options

| Option                 | When to Use                                                         | Complexity |
| ---------------------- | ------------------------------------------------------------------- | ---------- |
| Native CRM Dashboards  | Small team, limited budget, Salesforce/HubSpot already in place     | Low        |
| BI Tool (Tableau/Looker) | Multiple data sources, advanced visualization needs, 10+ users    | High       |
| GTM Platform           | Managed reporting, need for growth model integration                | Medium     |

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on what KPIs to track, how to define them, and what the reporting pack structure looks like.
>
> **Output:** Approved metric glossary, dashboard wireframe, data source inventory, and definition alignment document.

### 1a. Pre-Kickoff

> Two parallel tracks run after the engagement is confirmed and before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                              | Format             |
| ----------------------------- | ---------------------------------------------------- | ------------------ |
| Intro video                   | Explain what the reporting pack delivers and why metric alignment matters | Video (5-10 min)    |
| Definition Alignment Document | Get stakeholder sign-off on MQL, SQL, attribution, pipeline definitions | Google Doc         |
| Pre-filled intake form        | Capture current tools, KPIs, reporting questions leadership asks | Google Form or Doc |

**Intake form captures:**
- Current marketing tech stack (MAP, CRM, ad platforms, analytics tools)
- Top 5-7 questions leadership needs answered monthly
- Current reporting pain points (what takes too long, what's unreliable)
- Preferred reporting tool (native CRM, BI tool, or open to recommendation)
- Historical data availability (how many months of clean data exist)
- Budget data access for channel spend tracking

**Completion tracking:** Marketing Ops lead follows up. Do not cancel kickoff if incomplete, but push hard — admin access to systems is a hard blocker for Track B.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                           | Output                                          |
| ---- | ---------------------------------------------------------------- | ------------------------------------------------ |
| 1    | Run data quality diagnostic on MAP and CRM                       | Data source inventory with quality scores         |
| 2    | Audit existing reports and dashboards for coverage gaps           | Gap analysis document                             |
| 3    | Map available metrics to growth model targets                     | KPI mapping table                                 |
| 4    | Design v0 dashboard wireframe with recommended sections           | Dashboard prototype with executive summary, funnel, channel, campaign, pipeline views |
| 5    | Prepare kickoff call questions and validation checklist           | Questions list and presentation deck              |

**Critical:** Mark all metric definitions and KPI thresholds as ASSUMED. The kickoff call validates.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building dashboards. Marketing teams lose confidence when MQL counts differ between systems [1]. 87% of B2B respondents identify data accuracy as a top challenge [2] — definition alignment prevents this.

| Term                           | Our Definition                                                          | Internally Approved? |
| ------------------------------ | ----------------------------------------------------------------------- | -------------------- |
| MQL                            | Lead meeting behavioral + firmographic score thresholds in MAP          | [ ] Yes / [ ] No     |
| SQL                            | Lead accepted by sales as qualified for direct outreach                 | [ ] Yes / [ ] No     |
| Marketing-Sourced Pipeline     | Opportunities where first touch was a marketing activity                | [ ] Yes / [ ] No     |
| Marketing-Influenced Pipeline  | Opportunities where marketing touched contact at any pre-close stage    | [ ] Yes / [ ] No     |
| Cost Per MQL                   | Total marketing spend / total MQLs generated in period                  | [ ] Yes / [ ] No     |
| Pipeline Velocity              | Average days from opportunity creation to close                         | [ ] Yes / [ ] No     |
| Channel Attribution Model      | First-touch, last-touch, or multi-touch (specify which)                 | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your marketing and RevOps leadership team. Check "Yes" when approved. We cannot build dashboards until all terms are aligned — inconsistent definitions are the number one reason reporting packs fail.

---

### 1b. Kickoff Call

> **Purpose:** Present v0 dashboard wireframe and KPI recommendations. We walk in with work done — customer reacts, not creates from scratch.

#### Agenda (60-90 min)

| Time  | Topic                        | What Happens                                                  |
| ----- | ---------------------------- | ------------------------------------------------------------- |
| 0-15  | Walk through v0 wireframe    | "Here's what we built from your intake and data audit"        |
| 15-30 | Validate KPI priorities      | Confirm top 5-7 questions the pack must answer                |
| 30-45 | Definition alignment review  | Walk through Definition Alignment Doc, resolve disagreements  |
| 45-55 | Data gap discussion          | Surface missing data sources, broken integrations, UTM issues |
| 55-70 | Reporting tool decision      | Confirm tool choice (native CRM, Tableau/Looker, GTM platform) |
| 70+   | Next steps                   | Schedule refinement meetings, assign data gap remediation      |

#### What We Bring

- v0 dashboard wireframe (built from intake + data audit)
- Data source inventory with quality assessment
- KPI mapping to growth model targets
- Definition Alignment Document (pre-filled with recommendations)
- Questions list for validation

#### What We Leave With

- Feedback and corrections on v0 wireframe (info needed to create v1)
- Confirmed or contested metric definitions
- Data gap remediation assignments (who fixes what by when)
- Reporting tool decision
- Refinement loop scheduled

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Iterate on dashboard design and metric definitions until sign-off. Typically 2-3 meetings for this project type.

#### The Pattern

```
Kickoff Call (present v0, gather feedback)
    |
v1 dashboard wireframe + updated metric glossary
    |
Meeting 2 (review v1 with Marketing Ops, validate data mappings)
    |
v2 with confirmed data sources and calculations
    |
Meeting 3 (review v2 with RevOps, validate attribution + pipeline)
    |
vFinal
    |
Final Review > Sign-off
```

#### Before Each Meeting

1. Update dashboard wireframe based on previous feedback
2. Resolve data gaps identified in previous meeting
3. Prepare validation questions for next round

#### During Each Meeting

1. Walk through current dashboard version
2. Validate metric calculations with real data samples
3. Confirm what's now CONFIRMED vs. still ASSUMED
4. Identify any new gaps or stakeholder concerns

#### After Each Meeting

1. Update wireframe and metric glossary
2. Track what moved from ASSUMED &gt; CONFIRMED
3. Update data source inventory with new connections or fixes

#### Meeting Types for This Project

| Meeting Type         | Focus                                          | Stakeholder                    |
| -------------------- | ---------------------------------------------- | ------------------------------ |
| KPI Alignment        | Top-level metrics, dashboard sections          | VP Marketing, CMO              |
| Data Validation      | Source mappings, calculation verification       | Marketing Ops, RevOps          |
| Attribution Review   | Channel credit model, pipeline attribution     | Marketing Ops, RevOps, Sales   |
| Final Review         | Full dashboard walkthrough, metric glossary    | All stakeholders               |

#### Typical Timeline

| Milestone               | Timing                                           |
| ----------------------- | ------------------------------------------------ |
| Pre-kickoff prep        | 3-5 days (data audit takes time)                 |
| Kickoff call            | Day 1 of engagement                              |
| Meeting loop            | 1-2 weeks (2-3 meetings depending on complexity) |
| Final review + sign-off | When all definitions CONFIRMED                   |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything before building dashboards.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by VP Marketing and RevOps
- [ ] Metric glossary complete with calculation methods and ownership
- [ ] Dashboard wireframe approved (all sections, all drill-downs)
- [ ] Data source inventory confirmed — all connections available
- [ ] Attribution model agreed (first-touch, last-touch, or multi-touch)
- [ ] Reporting tool confirmed and access provisioned
- [ ] All critical data gaps resolved or accepted as known limitations
- [ ] Customer understands what we're building

#### Decision Point

- **Proceed to Engineering** — Standard path. Customer wants dashboards built and automated.
- This project does not have a natural exit after Phase 1. The strategic deliverables (metric glossary, wireframes) are inputs, not end products.

---

## Phase 2: Engineering

> **Goal:** Build and test the reporting infrastructure — data pipelines, dashboards, and automation.
>
> **Output:** Functional reporting pack with automated data refresh and distribution, tested against source systems and customer-approved.

| Project Type    | Engineering Weight | Example                                                  |
| --------------- | ------------------ | -------------------------------------------------------- |
| This project    | Heavy (50-60%)     | Data pipeline setup, dashboard builds, automation config |

### Sub-Phases

```
2a Tech Spec > 2b Engineering Handoff > 2c Build > 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate approved dashboard wireframe and metric glossary into a technical build specification.

**Input:** Signed-off strategic package (metric glossary, wireframe, data source inventory, attribution model)

**What happens:**

1. Review strategic deliverables
2. Translate KPI definitions into data queries and calculations
3. Map data sources to dashboard components
4. Output draft technical specification

**Output:** Draft tech spec containing:

- Data pipeline architecture (which sources connect to what, via which method)
- Dashboard component specifications (each section mapped to data queries)
- Metric calculation logic (formulas for CPL, conversion rates, pipeline velocity, ROI)
- Automation rules (refresh schedules, distribution lists, alert thresholds)
- Build sequence (data pipelines first, then dashboards, then automation)

**Data pipeline design:**

| Source System         | Data Type                  | Connection Method      | Refresh Frequency |
| --------------------- | -------------------------- | ---------------------- | ----------------- |
| MAP (HubSpot/Marketo) | Leads, MQLs, campaigns     | Native integration/API | Daily             |
| CRM (Salesforce)      | SQLs, pipeline, closed-won | Native integration/API | Daily             |
| Ad platforms          | Spend, impressions, clicks | API or connector       | Daily             |
| Google Analytics      | Web traffic, conversions   | API or connector       | Daily             |
| BI tool               | Consolidated views         | Native                 | On-demand         |

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs with engineer before building.

**Who attends:** Architect + Engineer (or engineering team)

**Agenda (30-45 min):**

| Time  | Topic                 | What Happens                                                |
| ----- | --------------------- | ----------------------------------------------------------- |
| 0-15  | Walk through specs    | Architect explains KPIs, metric logic, attribution model    |
| 15-30 | Engineer questions    | Clarify data connection methods, handle edge cases          |
| 30-45 | Refine and approve    | Confirm build sequence, identify risks (data quality, APIs) |

**What Architect brings:**

- Strategic package (metric glossary, wireframe, definition alignment doc)
- Draft tech spec (from 2a)
- Data source access credentials
- Known data quality issues from audit

**What engineer leaves with:**

- Approved tech spec with build sequence
- Clear priority order: data pipelines &gt; core dashboards &gt; automation &gt; alerts
- Known risks (API rate limits, data freshness constraints, historical data gaps)

---

### 2c. Build (Configure)

> **Purpose:** Build the reporting infrastructure in the customer's systems.

**Input:** Approved tech spec from 2b

**Build sequence:**

**Step 1: Data Pipeline Setup**
1. Connect primary data sources (MAP, CRM) via native integrations or API
2. Connect secondary data sources (ad platforms, Google Analytics)
3. Build data transformations to harmonize metrics across platforms
4. Configure refresh schedules (daily for pipeline data, weekly acceptable for campaign metrics)
5. Set up error alerting for failed data syncs

**Step 2: Core Dashboard Components**
1. Build executive summary page with top-level KPIs and red/yellow/green status indicators
2. Create funnel conversion visualization (Lead &gt; MQL &gt; SQL &gt; Opportunity &gt; Closed Won)
3. Build channel performance tables with spend, leads, CPL, and pipeline contribution by channel
4. Add campaign-level performance reports with ROI calculations
5. Build pipeline velocity metrics (average time between stages)
6. Create forecast vs. actual comparison views tied to growth model targets
7. Add filters for date range, segment, region, and other relevant dimensions

**Step 3: Automation Setup**
1. Configure scheduled report snapshots at month-end
2. Set up automated email distribution to marketing team and leadership
3. Create PDF export templates for board/executive presentations
4. Configure metric threshold alerts (e.g., MQLs below target triggers notification)
5. Test end-to-end automation cycle

**Build tracking:**

- [ ] Data pipeline: MAP connection
- [ ] Data pipeline: CRM connection
- [ ] Data pipeline: Ad platform connections
- [ ] Data pipeline: Data transformations + refresh schedules
- [ ] Data pipeline: Error alerting
- [ ] Dashboard: Executive summary page
- [ ] Dashboard: Funnel conversion view
- [ ] Dashboard: Channel performance tables
- [ ] Dashboard: Campaign ROI reports
- [ ] Dashboard: Pipeline velocity metrics
- [ ] Dashboard: Forecast vs. actual views
- [ ] Dashboard: Filters and drill-downs
- [ ] Automation: Scheduled snapshots
- [ ] Automation: Email distribution
- [ ] Automation: PDF export templates
- [ ] Automation: Threshold alerts

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify the reporting pack works and get customer approval.

**Two types of testing:**

| Type              | Who      | Purpose                                                    |
| ----------------- | -------- | ---------------------------------------------------------- |
| Technical Testing | Our team | Verify data flows, calculations are correct, automation fires |
| Customer Testing  | Customer | Verify reports answer their questions, numbers match expectations |

**Technical testing checklist:**

- [ ] All data source connections active and refreshing on schedule
- [ ] MQL counts in dashboard match source MAP system (spot-check 3 months)
- [ ] Pipeline numbers match Salesforce opportunity reports
- [ ] Funnel conversion rates calculate correctly (manual verification against raw data)
- [ ] Channel attribution credits sum correctly (100% for first/last-touch, appropriate for multi-touch)
- [ ] Forecast vs. actual views align with growth model targets
- [ ] Automated reports generate and distribute on schedule
- [ ] Threshold alerts fire correctly when test data crosses thresholds
- [ ] Filters work correctly across all dashboard sections
- [ ] PDF exports render cleanly
- [ ] No error logs in data pipeline

**Customer testing:**

- Walk customer through each dashboard section with live data
- Have them verify MQL and pipeline numbers match what they see in their own systems
- Test filter combinations they'll use regularly
- Demonstrate automated report delivery
- Capture feedback, fix issues before sign-off

**Engineering sign-off checkpoint:**

- [ ] Built system matches tech spec
- [ ] All technical tests passing
- [ ] Dashboard numbers validated against source systems
- [ ] Automation running correctly
- [ ] Customer has tested and approved
- [ ] Ready for enablement

**Decision point:**

- **Proceed to Enablement** — Dashboards are built, automation works, needs training/adoption
- **Loop back to Build** — Data discrepancies found, needs fixes before training

---

## Phase 3: Enablement

> **Goal:** Marketing team can use the reporting pack for regular decision-making, and the pack is embedded into operating rhythms.
>
> **Output:** Trained team with documentation, established reporting cadence, stabilized system.

### Sub-Phases

```
3a Training Prep > 3b Training Sessions > 3c Hypercare > 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from strategic and technical documentation.

**Input:** Strategic package + tech specs + built dashboards

**Output:** Training package containing:

- Video walkthrough scripts: Executive dashboard (5 min), Technical maintenance guide (10 min)
- Written guides: Metric glossary, dashboard navigation quick-reference, "How to add a new metric" guide
- FAQ draft: Common questions like "Why don't MQL counts match between tools?" and "How do I change the date range?"
- Meeting agenda template for monthly marketing review (tied to dashboard sections)

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to the customer team.

**Three training sessions:**

| Type       | Audience                         | Focus                                                        | Duration |
| ---------- | -------------------------------- | ------------------------------------------------------------ | -------- |
| Leadership | VP Marketing, CMO, Finance       | How to interpret dashboards, what red/yellow/green means, what actions to take when metrics are off-target | 30 min   |
| Technical  | Marketing Ops, RevOps Admin      | How to maintain dashboards, troubleshoot data issues, add new metrics, manage data connections | 60 min   |
| Team       | Full marketing team              | How to use dashboards in daily/weekly work, apply filters, export data, create ad-hoc views | 45 min   |

**Training delivery:**

1. Schedule sessions with appropriate stakeholders (leadership first, then technical, then team)
2. Deliver training live with screen sharing
3. Record all sessions as video walkthroughs for future reference
4. Address questions, note gaps for FAQ
5. Distribute quick-reference guide after sessions

**Output:**

- Trained stakeholders at all levels
- Video recordings for onboarding future team members
- Updated FAQ based on questions raised during training

---

### 3c. Hypercare

> **Purpose:** Intensive post-launch support to catch data issues and build confidence.

**Duration:** 2 weeks

**What happens:**

- Weekly 30-min office hours slot for Marketing Ops to ask questions
- Quick response to data discrepancy reports (target: same-day resolution)
- Monitor automated report delivery for first 2 cycles
- Fix any data pipeline issues that surface with real production data
- Validate month-end report generation runs correctly

**Hypercare scope:**
- In scope: Data discrepancies, dashboard bugs, automation failures, filter issues, training questions
- Out of scope: New metric additions, dashboard redesign, new data source connections (these are change requests)

**Output:** Stabilized reporting system, team confident in the data, no critical issues outstanding

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm the customer team can operate the reporting pack independently.

**Validation checkpoint:**

- [ ] All training sessions delivered and recorded
- [ ] Training recordings and documentation provided
- [ ] Hypercare period complete — no critical issues
- [ ] Marketing Ops can troubleshoot common data issues without support
- [ ] Monthly reporting cadence established (meeting scheduled, agenda set)
- [ ] Marketing team is actively referencing dashboards in weekly meetings
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** — Team is enabled, reporting cadence established
- **Extend Hypercare** — Still seeing data issues or low adoption

---

## Phase 4: Handoff

> **Goal:** Clean project close with maintenance plan established and customer self-sufficient.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the reporting system, project archived.

**Structure:**

```
4a Maintenance Schedule > 4b Internal Handoff > 4c External Handoff > 4d Project Close
                                                  (Delivery Team > Customer)   (Archive + Debrief)
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At                                                      |
| ----------------------------- | -------------------- | ------------------------------------------------------------------ |
| **Single Project**            | Customer owns        | 4c — customer receives maintenance schedule and runs it themselves |
| **Dedicated (Multi-Project)** | Architect owns       | 4b — Architect receives maintenance schedule and runs it for customer |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention to keep the reporting pack accurate and relevant.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task                  | What to Check                                                    | Red Flag Threshold                              |
| ----------------------------- | ---------------------------------------------------------------- | ----------------------------------------------- |
| Data accuracy spot-check      | Compare dashboard MQL/pipeline numbers against source systems    | &gt;5% variance between dashboard and source       |
| Data pipeline health          | Verify all connections active, no failed refreshes               | Any failed refresh in past 7 days               |
| Dashboard usage audit         | Check who's accessing dashboards and how often                   | &lt;50% of target users accessed in past month     |
| Metric definition drift       | Verify MQL/SQL criteria haven't changed in MAP/CRM without update | Any unannounced definition change                |

**Quarterly Tasks:**

| Quarterly Task               | What to Review                                                   | Action if Off-Track                              |
| ---------------------------- | ---------------------------------------------------------------- | ------------------------------------------------ |
| Full metric definitions review | Walk through glossary with Marketing Ops, verify all definitions still match system configs | Update glossary + recalibrate dashboards |
| Data source health audit     | Check all API connections, integration versions, data freshness  | Reconnect or upgrade integrations                |
| New KPI evaluation           | Are there new questions leadership needs answered?               | Scope dashboard extension if needed              |
| Attribution model review     | Is the current attribution model still serving the team?         | Adjust model or add new attribution view         |

**After First Business Cycle (30-60 days post-launch):**

- First full month-end report: Does the automated pack generate correctly? Do numbers tell the expected story?
- Stakeholder confidence check: Is leadership referencing dashboard data in decisions?
- Process validation: Is the monthly review meeting happening and using the pack as primary input?

**Refinement Triggers (when to re-engage):**

| Trigger                         | Threshold                                  | Response                                         |
| ------------------------------- | ------------------------------------------ | ------------------------------------------------ |
| Data discrepancy                | &gt;10% variance between dashboard and source for 2+ months | Re-engage, audit data pipeline        |
| Low adoption                   | &lt;30% of stakeholders using dashboards monthly | Re-engage for adoption workshop, simplify views |
| New data source needed         | Customer adds new MAP, ad platform, or CRM  | Scope pipeline extension project                 |
| Metric definitions changed     | Customer changes MQL/SQL criteria in system  | Update glossary and recalibrate dashboards       |

**Every 6-12 Months:**

- Full reporting pack audit: Are all sections still relevant? Any sections unused?
- KPI recalibration: Update benchmark thresholds based on 6-12 months of actuals
- Growth model alignment: Do reporting pack targets still match current growth model?
- Tool evaluation: Is the current BI tool still the right choice?

---

### 4b. Internal Handoff

> **Purpose:** Transfer context so the ongoing relationship owner can manage the account.

**What the Architect needs to know:**

- Reporting tool used and how to access it (admin credentials, login method)
- Data pipeline architecture: which connections exist, refresh schedules, known lag windows
- Contentious metric definitions: which definitions had stakeholder disagreements and how they were resolved
- Known data quality issues: what discrepancies are expected vs. concerning
- Maintenance schedule (if Dedicated engagement — Architect runs this)

**Escalation guidelines:**

| Issue Type                               | Who Handles           | Example                                          |
| ---------------------------------------- | --------------------- | ------------------------------------------------ |
| Dashboard filter or display issues       | Architect             | "Chart is showing wrong date range"              |
| Training for new team members            | Architect             | "New VP Marketing needs dashboard walkthrough"   |
| Data pipeline connection failures        | SME                   | "Salesforce API stopped syncing"                 |
| Metric definition changes                | SME                   | "We need to redefine MQL criteria"               |
| New data source additions                | SME                   | "We started using a new ad platform"             |

**For Dedicated engagements:** Architect receives the maintenance schedule (4a) and becomes responsible for executing monthly and quarterly tasks.

---

### 4c. External Handoff (Delivery Team &gt; Customer)

> **Purpose:** Formal project completion with customer.

**Final project meeting:**

- Review all dashboard sections with live data
- Walk through metric glossary and confirm definitions are accurate
- Demonstrate automation is running (show recent auto-generated report)
- Walk through maintenance schedule in detail
- Confirm documentation package is complete
- Transfer admin access to customer Marketing Ops lead
- Answer final questions
- Make it explicit: "Project complete"
- **For Single Project engagements:** Walk customer through maintenance schedule, record a video walkthrough

**Documentation package:**

- Metric glossary with calculation methodologies
- Data source connections and refresh schedules documentation
- Troubleshooting guide for common issues (failed refreshes, data discrepancies, stale data)
- "How to add a new metric" expansion guide
- Access permissions and admin credentials documentation
- All training video recordings
- FAQ document
- Definition Alignment Document (final version)
- Maintenance Schedule
- Monthly review meeting agenda template

**Output:** Customer owns the reporting system. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location
- [ ] Handoff documentation complete
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized

#### Internal Debrief (Optional but Recommended)

- What went well? (E.g., data audit caught issues early, metric alignment saved rework)
- What would we do differently? (E.g., should have pushed harder on UTM conventions earlier)
- Any learnings to feed back into SOPs?

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell &gt; Downsell &gt; Retry    |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (ongoing reporting optimization, new metric development)
   | if no
2. Downsell: Another one-time project (Lead Attribution, Growth Model, Campaign Operations)
   | if yes
3. Retry retainer at end of next project cycle
```

**Script:**

> "Now that the Marketing Reporting Pack is live, there are two ways we can continue working together. Option 1: We can set you up on managed services where we handle ongoing dashboard optimization, new metric development, and quarterly recalibrations. Option 2: If there's another specific project you need help with — like Lead Attribution or Growth Model — we can scope that out. Which sounds more interesting?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On [date ~quarter out], we'll review how the reporting pack is performing and see if any adjustments are needed."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                                   |
| ------------------- | -------------------------------------------------------------- |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks               |
| 2. Review metrics   | Check dashboard usage, data accuracy, any open issues          |
| 3. Decide ownership | Can Architect handle, or need SME?                             |
| 4. Prep materials   | If SME needed, brief them. If Architect, prep talking points.  |

**At the refinement check-in:**

- Review dashboard usage and adoption rates
- Check data accuracy against source systems
- Identify any new KPI requests or metric changes
- If minor: Architect handles tweaks
- If major: Scope new project (restart the assembly line)

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- Metric glossary with calculation methodologies and ownership assignments
- Dashboard wireframe/design (approved layout for all reporting sections)
- Data source inventory with gap analysis
- Definition Alignment Document (final version)
- Attribution model documentation

**Technical Deliverables:**

- Functional dashboard with all components (executive summary, funnel, channel, campaign, pipeline, forecast views)
- Data pipeline connections (MAP, CRM, ad platforms, analytics &gt; BI tool)
- Automated report generation and distribution
- Threshold alert configuration
- PDF export templates for executive presentations

**Documentation Package:**

- Training video recordings (leadership, technical, team)
- Metric glossary (published version)
- Data source and pipeline documentation
- Troubleshooting guide
- "How to add a new metric" expansion guide
- Quick-reference guide for common actions
- FAQ document
- Maintenance Schedule
- Monthly review meeting agenda template

---

## Appendix

### Roles

| Role         | What They Do                                                                                   |
| ------------ | ---------------------------------------------------------------------------------------------- |
| **Architect** | Owns the customer relationship, leads strategy, creates specs, does enablement, owns account post-delivery |
| **Engineer** | Dashboard builds, data pipeline configuration, automation setup (Phase 2)                      |
| **SME**      | Marketing analytics specialist brought in for metric definition and attribution model design   |

### What Each Phase Produces

| Phase                    | Output                                                                 | Gate Criteria                                                                  |
| ------------------------ | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **Phase 1: Strategy**    | Approved metric glossary, dashboard wireframe, data strategy           | Stakeholders signed off on definitions, design, and tool selection             |
| **Phase 2: Engineering** | Built and tested reporting pack with automation                        | Dashboard numbers match source systems, automation running, customer approved  |
| **Phase 3: Enablement**  | Trained team with documentation, reporting cadence established         | All training delivered, hypercare complete, team operating independently       |
| **Phase 4: Handoff**     | Independent customer + archived project                                | Maintenance plan in place, project closed, retention path established          |

### How to Adapt Per Customer

This project sits in the **Balanced** profile with heavy engineering. Adaptation points:

- **Customers with existing BI infrastructure** (already have Tableau/Looker): Phase 2 is lighter — extend existing dashboards rather than building from scratch.
- **Customers without a growth model yet**: Phase 1 Strategy may need to define baseline targets. Consider scoping Growth Model as a prerequisite project.
- **Customers with clean data**: Phase 1a data audit is lighter. Phase 2c build moves faster.
- **Customers with messy data**: Phase 1a data audit is heavier. May need a data cleanup sprint between Phase 1 and Phase 2.

### Key Research & Benchmarks

Marketing teams spend 24% of their data-related time just collecting data, with another 19% on cleaning it — over 40% of effort goes to preparation tasks that reporting automation eliminates [3]. One real-world example: monthly reporting required three analysts working for two full weeks to manually combine data from Salesforce, Marketo, Google Ads, LinkedIn, and events platforms [3]. Organizations that consolidate reporting infrastructure cut up to 80% of reporting time [4].

40% of B2B marketers report they are not confident they can prove their return on investment [5]. 26% of B2B marketers cite ROI measurement as their primary challenge [6]. When marketing teams have standardized dashboards with agreed metric definitions, they can answer performance questions in minutes instead of hours.

The overall B2B lead-to-customer conversion rate averages 2-5%, with the steepest loss at the MQL-to-SQL transition (15-21% conversion) [7]. A well-built reporting pack makes these conversion drop-offs visible so marketing can identify and address the specific stage where leads are lost.

### References

[1] [Cometly - Marketing Data Accuracy Challenges](https://www.cometly.com/post/marketing-data-accuracy-challenges)

[2] [DemandScience - B2B Data Deprecation: A Marketer's Guide](https://demandscience.com/resources/blog/b2b-data-deprecation-marketers-guide/)

[3] [Improvado - B2B Marketing Report: 2025 Benchmarks, Trends & Insights](https://improvado.io/blog/b2b-marketing-reporting)

[4] [Supermetrics - Marketing Data: Types, Benefits, and Solutions](https://supermetrics.com/blog/marketing-data)

[5] [Ruler Analytics - B2B Marketing Statistics: 90+ Statistics Every Marketer Needs to Know](https://www.ruleranalytics.com/blog/inbound-marketing/b2b-marketing-statistics/)

[6] [Martal - 2025 B2B Marketing ROI Benchmarks](https://martal.ca/b2b-digital-marketing-benchmarks-lb/)
