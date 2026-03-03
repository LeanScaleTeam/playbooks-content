# Executive Reporting Suite — Implementation

## Project One-Pager

> Quick reference for architects. One per project type. Fill this out FIRST — it serves as the project's identity card.

### Executive Reporting Suite One-Pager

#### Project Type

- Category: Balanced
- Primary Deliverable: Unified, role-based executive dashboard suite with live data from CRM, marketing automation, and financial systems — all rolling up to ARR

##### Phase Relevance

| Phase          | Applies? | Notes                                                        |
| -------------- | -------- | ------------------------------------------------------------ |
| 1. Strategy    | Yes      | 3-4 stakeholder interviews + metric definition alignment     |
| 2. Engineering | Yes      | Data integration, dashboard build, alert configuration       |
| 3. Enablement  | Yes      | Executive training sessions + automated report distribution  |
| 4. Handoff     | Yes      | Governance setup + admin access transfer + 30-day check-in   |

· · ·

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │    Heavy     │     │    Heavy     │     │    Medium    │     │    Medium    │
  │ 1a→1b→1c→1d │     │ 2a→2b→2c→2d │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   3-4 interviews       Data integration     Exec training +      Governance +
   metric alignment     + dashboard build    report distribution  admin transfer
```

**This project's flow:**
- Full 4-phase. Heavy strategy (stakeholder interviews, metric definitions, KPI prioritization) and heavy engineering (data connections, dashboard builds, alert config). Medium enablement (training + automated delivery). Standard handoff.
- No phases skipped. Strategy and Engineering carry roughly equal weight (~35% each). Enablement ~15%, Handoff ~15%.

· · ·

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Watch intro video explaining what the Executive Reporting Suite is and how it differs from ad-hoc reports
- [ ] Complete KPI intake form (top 5-7 metrics per executive role, current reporting pain points, decision-making context)
- [ ] Get internal alignment on ARR calculation methodology (multi-year deals, usage-based, discounts)
- [ ] Provide admin access credentials for CRM, marketing automation, and financial systems
- [ ] Share existing dashboards/reports currently used for executive meetings

##### Track B: Architect Prep
- [ ] Pull current CRM pipeline and opportunity data via API to assess data quality
- [ ] Inventory existing BI dashboards in Looker/Tableau (active vs abandoned)
- [ ] Run data freshness audit across source systems (real-time, daily, manual)
- [ ] Create v0 KPI matrix mapping standard executive metrics to available data sources
- [ ] Draft role-based dashboard wireframes using executive reporting templates

· · ·

#### Refinement Loop (1b --&gt; 1c --&gt; 1d)

| Meeting             | Sub-Phase | Focus                                                      | Stakeholder                          | Output                          |
| ------------------- | --------- | ---------------------------------------------------------- | ------------------------------------ | ------------------------------- |
| Kickoff             | 1b        | Present v0 KPI matrix, validate executive reporting needs  | CRO, VP RevOps, executive sponsor    | Corrections for v1 KPI matrix   |
| Metric Definitions  | 1c        | Align on ARR calculation, funnel stage definitions, CAC    | Finance, RevOps, Sales leadership    | Signed metric definition doc    |
| Dashboard Wireframe | 1c        | Review v1 dashboard layouts, drill-down paths, filters     | CRO, VP Sales, VP Marketing, VP CS  | Approved dashboard architecture |
| Sign-Off            | 1d        | Final KPI matrix + architecture approval                   | All stakeholders                     | Go for engineering              |

· · ·

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held
- [ ] 1c. Refinement loop complete (v0 --&gt; vFinal KPI matrix + dashboard architecture)
- [ ] 1d. Strategic sign-off obtained (metric definitions + dashboard specs approved)

##### Phase 2: Engineering
- [ ] 2a. Tech spec created (data source mappings, refresh schedules, LookML/Tableau config)
- [ ] 2b. Engineering handoff meeting held
- [ ] 2c. Build complete (data connections + executive dashboard + role-specific drill-downs + alerts)
- [ ] 2d. QA/Test + customer sign-off (data validation against source systems)

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped (training scripts, metric definition guide, FAQ)
- [ ] 3b. Training sessions delivered (executive walkthrough + technical admin training)
- [ ] 3c. Hypercare period complete (2-week post-launch support)
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff (SME --&gt; Architect) complete
- [ ] 4c. External handoff (LeanScale --&gt; Customer) complete
- [ ] 4d. Project closed and archived

· · ·

#### Document Types

##### Working Documents (iterate together)

| Document                       | Purpose                                      | When Complete                              |
| ------------------------------ | -------------------------------------------- | ------------------------------------------ |
| KPI Intake Form                | Capture each executive's metric needs        | All executive stakeholders have responded  |
| KPI Priority Matrix            | Map metrics to roles with P0/P1/P2 ranking   | All P0 metrics confirmed by stakeholders   |
| Metric Definition Document     | Precise calculation logic for every KPI      | Signed off by Finance and RevOps           |
| Data Source Audit              | Inventory all systems, fields, data quality  | All sources assessed with gap analysis     |
| Dashboard Architecture Diagram | Data flow from source to BI platform         | Approved by RevOps and Engineering         |

##### Deliverables (polished outputs)

| Deliverable                     | Created From                     | Customer Uses For                           |
| ------------------------------- | -------------------------------- | ------------------------------------------- |
| Executive Dashboard Suite       | KPI matrix + architecture        | Weekly leadership meetings, board reporting |
| Role-Specific Drill-Down Views  | KPI matrix + stakeholder input   | Department-level performance review         |
| Metric Definition Guide         | Metric Definition Document       | Cross-team alignment on how numbers work    |
| Alert Configuration Document    | Dashboard architecture           | Understanding when/why threshold alerts fire|

· · ·

#### Enablement Details

##### Training Types

| Type       | Audience                           | Focus                                                     | Duration |
| ---------- | ---------------------------------- | --------------------------------------------------------- | -------- |
| Executive  | CEO, CRO, VP Sales, VP Mkt, VP CS | Navigate dashboards, interpret metrics, use drill-downs   | 45 min   |
| Technical  | RevOps Manager, BI Admin          | Maintain dashboards, modify filters, update thresholds    | 60 min   |

##### Hypercare
- Applies: Yes
- Duration: 2 weeks
- Office Hours: Yes — weekly 30-min slot for questions, bug triage, minor adjustments

##### Training Assets to Create
- [ ] Video walkthrough: Executive dashboard (each metric explained)
- [ ] Video walkthrough: Drill-down navigation demo (summary --&gt; detail)
- [ ] Doc: Metric definition guide with calculation logic
- [ ] Doc: Data source mapping reference
- [ ] Doc: Alert threshold logic and recipient list
- [ ] Doc: Admin guide for adding users, modifying filters, updating thresholds

· · ·

#### Handoff & Retention

##### Internal Handoff (SME --&gt; Architect)
- Key context for Architect: Dashboard architecture, metric calculation logic, data refresh schedules, known data quality quirks
- Escalation trigger: Any metric definition changes, new data source integrations, or dashboard structural modifications

##### External Handoff (LeanScale --&gt; Customer)
- Final meeting agenda: Review delivered dashboards, walk through documentation, confirm nothing outstanding, address final questions
- Documentation package: Metric guide, data source mappings, refresh schedules, alert docs, training recordings, admin guide, maintenance schedule

##### Maintenance Schedule
- Monthly: Data accuracy spot-check, dashboard usage audit, alert threshold review
- Quarterly: Full metric definition validation, new KPI assessment, dashboard relevance review
- Who owns: Single project = customer owns | Dedicated = Architect owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services --&gt; if no --&gt; Downsell: Another project (e.g., ARR Reporting, Forecasting Process) --&gt; Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~90 days post-launch
- Internal prep trigger: 2 weeks before
- Decision: Architect handles / SME needed

· · ·

#### Key Assets

| Asset                          | When Used                |
| ------------------------------ | ------------------------ |
| KPI Intake Form Template       | Phase 1a Pre-Kickoff     |
| Executive Dashboard Templates  | Phase 2c Build           |
| Metric Definition Template     | Phase 1c Refinement      |
| Data Validation Checklist      | Phase 2d QA              |
| Training Script Templates      | Phase 3a Training Prep   |

· · ·

#### Definition Alignment Terms

| Term                      | Typical Definition                                                                                     |
| ------------------------- | ------------------------------------------------------------------------------------------------------ |
| ARR                       | Annualized value of recurring subscription revenue, normalized to 12-month terms                       |
| MRR                       | Monthly recurring revenue; ARR / 12                                                                    |
| Pipeline Coverage         | Total qualified pipeline value / remaining quota for period (target: 3-4x) [1]                         |
| Sales Velocity            | (Number of Opportunities x Average Deal Size x Win Rate) / Average Sales Cycle Length                  |
| MQL                       | Marketing Qualified Lead — meets demographic and behavioral thresholds defined by Marketing + Sales    |
| SQL                       | Sales Qualified Lead — confirmed by sales rep as having budget, authority, need, and timeline          |
| CAC                       | Customer Acquisition Cost — total Sales + Marketing spend / number of new customers in period          |
| CAC Payback Period        | Months to recoup CAC from gross margin on new customer revenue                                         |
| NRR                       | Net Revenue Retention — revenue from existing customers including expansion minus churn, as % of start |
| Quota Attainment          | Actual bookings / assigned quota for period, expressed as percentage                                   |

· · ·

#### Common Gotchas
- ARR calculation includes nuances for multi-year deals, usage-based components, and discount handling — get Finance sign-off before building any revenue metric
- Data freshness varies by source: CRM may be real-time while financial data syncs daily — set dashboard labels so executives know when data was last updated
- Too many metrics on the executive view kills adoption: research shows BI adoption sits at only 25% across organizations [2] — cap the executive dashboard at 5-7 action-driving KPIs
- One inaccurate number destroys trust in the entire suite — always reconcile dashboard outputs against known financial figures before any executive sees them
- Dashboard utilization drops from 30% to 9% within 3 weeks when dashboards are not embedded in operating rhythms [3] — tie dashboard review to existing weekly leadership meetings

· · ·

#### Methodology Options

| Option                     | When to Use                                          | Complexity |
| -------------------------- | ---------------------------------------------------- | ---------- |
| Single BI Platform         | Client has one BI tool (Looker OR Tableau)            | Low        |
| Multi-Source Aggregation   | Client needs data warehouse layer to unify sources    | Medium     |
| Embedded Analytics         | Dashboards embedded directly in Slack/CRM/email       | High       |

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on which metrics to build, how they are calculated, and how dashboards are structured.
>
> **Output:** Signed-off KPI matrix + Metric Definition Document + Dashboard Architecture Spec.

### 1a. Pre-Kickoff

> Two parallel tracks run after the AE closes and before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                       | Format             |
| ----------------------------- | ------------------------------------------------------------- | ------------------ |
| Intro video                   | Explain what the Executive Reporting Suite is and why it matters — distinguish from ad-hoc reporting or one-time analysis | Video (5-10 min)    |
| KPI Intake Form               | Capture each executive's top 5-7 KPIs, current pain points, reporting cadence needs, and "questions they can't answer today" | Google Form or Doc |
| Definition Alignment Document | Get stakeholder sign-off on ARR calculation, pipeline stages, MQL/SQL definitions | Google Doc         |
| Access Request Checklist      | Admin credentials needed for CRM, MAP, financial systems, BI platform | Google Doc         |

**Completion tracking:** RevOps lead is accountable for collecting responses from all executive stakeholders. Don't cancel kickoff if incomplete, but push hard after — especially on ARR definition from Finance.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                         | Output                                        |
| ---- | -------------------------------------------------------------- | --------------------------------------------- |
| 1    | Pull CRM data via API — opportunity stages, pipeline, deals   | Raw data quality assessment                   |
| 2    | Inventory existing dashboards and reports across BI platform   | Current state reporting landscape              |
| 3    | Run data freshness audit across all source systems             | Source-by-source freshness report              |
| 4    | Build v0 KPI matrix using intake + industry benchmarks         | Draft KPI matrix with role-based views         |
| 5    | Create draft dashboard wireframes                               | Visual mockups for kickoff discussion          |

**Critical:** Mark every metric as ASSUMED until validated in kickoff. The v0 KPI matrix is pre-filled with recommended executive metrics (ARR, pipeline coverage, sales velocity, CAC, funnel conversion, quota attainment, NRR) — the customer reacts and adjusts, not creates from scratch.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on metric definitions BEFORE building anything. 60% of BI initiatives fail to deliver business value [4] — misaligned definitions are a primary cause.

| Term                | Our Definition                                                                              | Internally Approved? |
| ------------------- | ------------------------------------------------------------------------------------------- | -------------------- |
| ARR                 | Annualized recurring subscription revenue, normalized to 12-month terms                     | [ ] Yes / [ ] No     |
| Pipeline Coverage   | Total qualified pipeline / remaining quota for period                                       | [ ] Yes / [ ] No     |
| MQL                 | Lead meeting demographic + behavioral scoring thresholds                                    | [ ] Yes / [ ] No     |
| SQL                 | Lead confirmed by rep as having budget, authority, need, timeline                           | [ ] Yes / [ ] No     |
| CAC                 | Total S&M spend / new customers acquired in period                                          | [ ] Yes / [ ] No     |
| Win Rate            | Closed Won opportunities / Total opportunities that reached qualified stage                 | [ ] Yes / [ ] No     |
| Sales Velocity      | (Opportunities x Avg Deal Size x Win Rate) / Avg Sales Cycle Length                         | [ ] Yes / [ ] No     |
| NRR                 | (Starting revenue + expansion - contraction - churn) / starting revenue                     | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your leadership and finance team. Check "Yes" when approved. We cannot build accurate dashboards until all metric definitions are aligned across teams.

---

### 1b. Kickoff Call

> **Purpose:** Present v0 KPI matrix and dashboard wireframes. Validate assumptions. Align on metric definitions. Identify data gaps.

#### Agenda (60-90 min)

| Time  | Topic                      | What Happens                                                       |
| ----- | -------------------------- | ------------------------------------------------------------------ |
| 0-15  | Walk through v0 KPI matrix | "Here are the metrics we recommend for each executive role"        |
| 15-30 | Validate assumptions       | ASSUMED metrics --&gt; CONFIRMED or corrected by each executive        |
| 30-40 | Definition alignment       | Review Definition Alignment Doc, flag disagreements                |
| 40-50 | Dashboard wireframe review | Show draft layouts, discuss drill-down paths and filters           |
| 50-60 | Data gap identification    | What data is missing? Who owns remediation?                        |
| 60+   | Next steps                 | Schedule metric definition session, assign Finance homework on ARR |

#### What We Bring

- v0 KPI matrix (built in Track B prep) with recommended metrics per role
- Draft dashboard wireframes showing executive summary and drill-down structure
- Data freshness report showing current state of each source system
- Definition Alignment Document (pre-filled with recommendations)
- Questions list targeting known gaps from data audit

#### What We Leave With

- Feedback and corrections on v0 KPI matrix (info needed for v1)
- Confirmed P0 metrics (must-have for MVP) vs P1 (full launch) vs P2 (nice-to-have)
- Known data gaps with owners and remediation timelines
- Finance homework: validate ARR calculation with CFO/Controller
- Alignment loop scheduled (metric definitions session + wireframe review)

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Iterate on the KPI matrix, metric definitions, and dashboard architecture until sign-off.

#### The Pattern

```
Kickoff Call (gather info)
    |
Architect updates KPI matrix --> v1
    |
Meeting 2: Metric Definitions (Finance + RevOps validate) --> Architect updates --> v2
    |
Meeting 3: Dashboard Architecture (all execs review wireframes) --> Architect finalizes
    |
Sign-Off
```

#### Meeting 2: Metric Definitions (45-60 min)

**Stakeholders:** Finance lead, RevOps Manager, CRO

**Focus:**
1. Walk through ARR calculation methodology — including multi-year deals, usage-based revenue, discounts
2. Confirm pipeline stage definitions and conversion rate calculations
3. Establish CAC and LTV calculation methodologies with Finance
4. Define what counts as MQL, SQL, and opportunity for funnel metrics
5. Create glossary of metric definitions that will appear in dashboard documentation

**Output:** Signed-off Metric Definition Document

#### Meeting 3: Dashboard Architecture (45-60 min)

**Stakeholders:** CRO, VP Sales, VP Marketing, VP CS, RevOps

**Focus:**
1. Review updated dashboard wireframes with live data mockups
2. Confirm role-based views: CEO (revenue snapshot), CRO (pipeline + attainment), VP Sales (stage conversion), VP Marketing (MQL flow + attribution), VP CS (retention + expansion)
3. Define drill-down paths from summary metrics to detail
4. Specify data refresh schedules and alert thresholds
5. Confirm visualization types (trend lines for ARR, funnels for conversion, gauges for attainment)

**Output:** Approved Dashboard Architecture Spec

#### Typical Timeline

| Milestone               | Timing                                                  |
| ----------------------- | ------------------------------------------------------- |
| Pre-kickoff prep        | 3-5 days                                                |
| Kickoff call            | Day 1 of engagement                                     |
| Metric definitions      | Within 1 week of kickoff (depends on Finance availability) |
| Dashboard architecture  | Within 2 weeks of kickoff                               |
| Sign-off                | When all definitions confirmed and architecture approved |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything before building dashboards.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by Finance and all executive stakeholders
- [ ] KPI Priority Matrix finalized (P0/P1/P2 for each metric)
- [ ] Role-based dashboard views defined and approved
- [ ] Dashboard Architecture Spec approved (data flow, refresh schedules, visualization types)
- [ ] All P0 data sources assessed — gaps identified with remediation plans
- [ ] ARR calculation methodology confirmed by Finance
- [ ] No blockers for engineering (admin access granted, data flowing)

#### Decision Point

- **Proceed to Engineering** --&gt; All definitions aligned, architecture approved, data accessible
- **Loop back to Alignment** --&gt; Finance has not signed off on ARR calculation, or critical data gaps remain

> This project always proceeds to Engineering. The strategic deliverable (KPI matrix + metric definitions) is a prerequisite for the technical build, not a standalone product.

---

## Phase 2: Engineering

> **Goal:** Build the dashboard suite with live data, validated against source systems, tested and approved by stakeholders.
>
> **Output:** Functional executive dashboard suite with role-specific drill-downs, automated refresh, and threshold alerts.

| Project Type    | Engineering Weight | Context                                             |
| --------------- | ------------------ | --------------------------------------------------- |
| Executive Reporting Suite | Heavy (35-40%) | Data connections, dashboard builds, alert configuration, data validation |

### Sub-Phases

```
2a Tech Spec --> 2b Engineering Handoff --> 2c Build --> 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate the approved KPI matrix and dashboard architecture into technical build specifications.

**Input:** Signed-off KPI matrix + Metric Definition Document + Dashboard Architecture Spec

**What happens:**

1. Architect maps each KPI to specific source fields, API endpoints, and calculation logic
2. Draft technical specification is produced

**Output:** Draft tech spec containing:

- **Data source mappings:** Which CRM/MAP/financial system field feeds each metric
- **Calculation logic:** Exact formulas for ARR, pipeline coverage, sales velocity, CAC, NRR (per Metric Definition Document)
- **Refresh schedules:** Hourly for pipeline metrics, daily for revenue and financial metrics, real-time for alerts
- **BI platform configuration:** LookML models (Looker) or workbook structure (Tableau)
- **Dashboard hierarchy:** Executive summary --&gt; role-specific views --&gt; drill-down detail
- **Alert specs:** Threshold values, notification channels (email, Slack), recipient lists by role
- **Build sequence:** Data connections first, then executive dashboard, then role-specific views, then alerts

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs with the BI engineer before building.

**Who attends:** Architect + BI Engineer (or data team)

**Agenda (30-45 min):**

| Time  | Topic              | What Happens                                              |
| ----- | ------------------ | --------------------------------------------------------- |
| 0-15  | Walk through specs | Architect explains strategic context + KPI definitions           |
| 15-30 | Engineer questions | Clarify data source access, API limitations, refresh feasibility |
| 30-45 | Refine and approve | Adjust specs for technical constraints, confirm build order |

**What Architect brings:**

- Strategic package: KPI matrix, metric definitions, dashboard architecture
- Draft tech spec (from 2a)
- Data source audit results (freshness, quality issues, gaps)

**What engineer leaves with:**

- Approved tech spec with clear build sequence
- Known data quality issues and workarounds
- Admin credentials and API access for all source systems

---

### 2c. Build (Configure)

> **Purpose:** Build the dashboard suite in the client's BI platform with live data from all source systems.

**Input:** Approved tech spec from 2b

**Build sequence:**

**Step 1: Data Integration Connections**
- Connect Salesforce/HubSpot CRM via OAuth or API
- Set up marketing automation data feed (HubSpot Marketing, Marketo, or equivalent)
- Integrate financial system data (QuickBooks, NetSuite, or subscription billing platform)
- Configure data warehouse connections if using intermediary layer (BigQuery, Snowflake, Redshift)
- Verify data is flowing correctly by spot-checking sample records against source
- Document connection credentials and refresh schedules for handoff

**Step 2: Primary Executive Dashboard (5-7 metrics)**
- Build ARR/MRR tracking with actual vs. target comparison
- Create pipeline coverage metric (pipeline value / quota remaining — benchmark target: 3-4x) [1]
- Add sales velocity calculation: (avg deal size x win rate x volume) / cycle time
- Include CAC and CAC payback period from marketing spend data (median B2B SaaS CAC is $2 per $1 of new ARR) [5]
- Build funnel visualization: Lead --&gt; MQL --&gt; SQL --&gt; Opportunity --&gt; Closed Won
- Add quota attainment gauge for current period
- Test all calculations against source data to validate accuracy

**Step 3: Role-Specific Drill-Down Views**
- CEO view: Revenue snapshot, pipeline health, efficiency ratios
- CRO view: Pipeline by stage, rep performance, deal aging, forecast vs. actual
- VP Sales view: Stage-by-stage conversion rates, sales cycle trends, individual rep dashboards
- VP Marketing view: MQL volume and conversion, campaign attribution, source performance, marketing spend ROI
- VP CS view: Retention rates, expansion revenue, NRR, health scores by segment
- Link drill-downs from executive dashboard (click metric --&gt; see detail)
- Ensure consistent date ranges and filters across all views

**Step 4: Alerts and Automated Refresh**
- Configure data refresh schedule (hourly for pipeline, daily for revenue metrics)
- Set up threshold alerts: pipeline coverage &lt; 3x, win rate drop &gt; 10%, MQL volume &lt; 80% of target
- Define alert recipients by role (CRO gets pipeline alerts, VP Marketing gets MQL alerts, CEO gets ARR alerts)
- Configure delivery method (email digest, Slack channel, in-app notification)
- Test alert triggers with sample threshold breaches
- Document alert logic and thresholds for handoff

**Execution approach:**

| Approach       | When to Use                                    | Example                                |
| -------------- | ---------------------------------------------- | -------------------------------------- |
| Manual build   | Complex LookML/Tableau calc logic, first build | Engineer builds dashboards directly    |
| Agent-assisted | Standard KPIs with clear calculation logic      | Agent generates LookML, engineer reviews |

**Build tracking:**

- [ ] Data connections established and syncing
- [ ] Executive dashboard live with 5-7 core metrics
- [ ] CEO drill-down view complete
- [ ] CRO drill-down view complete
- [ ] VP Sales drill-down view complete
- [ ] VP Marketing drill-down view complete
- [ ] VP CS drill-down view complete
- [ ] Alerts configured and tested
- [ ] Automated refresh schedules active

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify dashboard data matches source systems and get customer approval before launch.

**Two types of testing:**

| Type              | Who      | Purpose                                              |
| ----------------- | -------- | ---------------------------------------------------- |
| Technical Testing | Our team | Verify data accuracy, calculations, refresh, alerts  |
| Customer Testing  | Customer | Verify dashboards answer their questions             |

**Technical testing checklist:**

- [ ] Pull current ARR from finance system and compare to dashboard ARR — must match within 1% tolerance
- [ ] Validate pipeline totals match CRM pipeline reports exactly
- [ ] Check MQL counts against marketing automation source
- [ ] Verify conversion rates by manually calculating from source data
- [ ] Confirm sales velocity calculation matches manual spreadsheet check
- [ ] Test all drill-down links — executive view to detail and back
- [ ] Verify alert triggers fire correctly when thresholds are breached
- [ ] Confirm data refresh is running on schedule (check timestamps)
- [ ] Test role-based access — each executive sees only their authorized views
- [ ] Document any discrepancies, root causes, and fixes applied

**Customer testing (Stakeholder Review Session):**

- Schedule review with RevOps lead and 1-2 executive stakeholders
- Walk through each dashboard explaining metrics and data sources
- Have them test drill-down functionality and filters
- Capture feedback on visualization choices, missing metrics, confusing labels
- Confirm metric values match their mental model of the business
- Document required changes and implement before full launch

**Engineering sign-off checkpoint:**

- [ ] All dashboard metrics validated against source systems
- [ ] Stakeholders have tested and confirmed data accuracy
- [ ] All drill-downs and filters working correctly
- [ ] Alerts firing as expected
- [ ] Data refresh running on schedule
- [ ] Ready for enablement

**Decision point:**

- **Proceed to Enablement** --&gt; Dashboards validated, stakeholders approve
- **Loop back to Build** --&gt; Data discrepancies found, calculations need fixing

---

## Phase 3: Enablement

> **Goal:** Executive team can use the dashboard suite independently. Dashboards are embedded in operating rhythms.
>
> **Output:** Trained executives, technical admin team, automated report delivery, stabilized system.

### Sub-Phases

```
3a Training Prep --> 3b Training Sessions --> 3c Hypercare --> 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from strategic documentation and built dashboards.

**Input:** KPI matrix + metric definitions + live dashboard suite + tech spec

**Output:** Training package containing:

- **Executive training script** (45 min): How to navigate dashboards, what each metric means, how to interpret trends, when to drill down, how alerts work
- **Technical admin training script** (60 min): How to maintain dashboards, add/remove users, modify filters, update alert thresholds, troubleshoot data refresh issues
- **Metric definition guide**: One-page reference for each KPI with calculation logic and data source
- **FAQ draft**: Based on common executive questions from similar reporting projects ("Why don't my numbers match my spreadsheet?", "How often does data refresh?", "How do I see last quarter?")

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to the customer team so they can operate dashboards independently.

**Two types of training:**

| Type                | Audience                                      | Focus                                                             |
| ------------------- | --------------------------------------------- | ----------------------------------------------------------------- |
| Executive training  | CEO, CRO, VP Sales, VP Marketing, VP CS       | Navigate dashboards, interpret metrics, use drill-downs, understand alerts |
| Technical handoff   | RevOps Manager, BI Admin, dashboard maintainer | Maintain dashboards, modify filters/thresholds, troubleshoot issues, add users |

**Executive Training Session (45 min):**

1. Walk through executive dashboard — explain each metric and what it means for the business
2. Demonstrate drill-down from summary to detail (e.g., ARR --&gt; pipeline by stage --&gt; individual deals)
3. Show filtering capabilities (by segment, by team, by time period)
4. Explain data refresh schedules — when to expect updated numbers
5. Cover alert system — what thresholds trigger notifications, what action to take
6. Address questions and capture additional feature requests
7. Record session for executives who couldn't attend

**Technical Admin Training Session (60 min):**

1. Walk through dashboard architecture — where data comes from, how calculations work
2. Demonstrate how to add/remove users and set role-based access
3. Show how to modify filters, date ranges, and alert thresholds
4. Cover troubleshooting: data refresh delays, calculation discrepancies, API connection issues
5. Walk through maintenance schedule and what to check monthly/quarterly
6. Provide admin guide document as reference

**Output:**

- Trained executives comfortable navigating dashboards
- Technical admin team able to maintain and troubleshoot
- Recordings of both sessions for future onboarding
- Questions log feeding into FAQ

---

### 3c. Hypercare

> **Purpose:** Intensive post-launch support to stabilize the dashboards in real operating conditions.

**Duration:** 2 weeks

**What happens:**

- Quick response to data accuracy questions, display bugs, or access issues
- Office hours: weekly 30-min slot where anyone can hop on and share what is not working
- Bug triage: data discrepancy reports investigated and resolved within 24 hours
- Monitor dashboard usage (login frequency) to catch adoption issues early
- Configure automated report distribution: weekly executive summary email, Slack alerts for threshold breaches, monthly board report template

**Automated Report Distribution Setup:**
- Configure weekly executive summary email with top 5 metrics and week-over-week trends
- Set up Slack integration for real-time alerts (pipeline coverage drops, win rate changes)
- Create monthly board report template pulling key visualizations automatically
- Test distribution to confirm formatting and timing

**When hypercare ends:** No critical data issues outstanding, executives using dashboards in at least one weekly meeting, automated delivery running successfully.

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm customer can operate dashboards independently.

**Validation checkpoint:**

- [ ] Executive training session delivered and recorded
- [ ] Technical admin training session delivered and recorded
- [ ] Automated report distribution configured and tested
- [ ] Hypercare period complete — no critical issues outstanding
- [ ] Dashboard usage confirmed in at least one weekly leadership meeting
- [ ] Customer team can navigate, filter, and interpret dashboards without support
- [ ] Technical admin can maintain dashboards, modify thresholds, and troubleshoot basic issues
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** --&gt; Customer is enabled, dashboards embedded in operating rhythms
- **Extend Hypercare** --&gt; Low adoption, data trust issues, or outstanding bugs

---

## Phase 4: Handoff

> **Goal:** Clean project close with governance process established, admin access transferred, and retention path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the dashboard suite, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule --> 4b Internal Handoff --> 4c External Handoff --> 4d Project Close
                                (SME --> Architect)    (LeanScale --> Customer)   (Archive + Debrief)
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At                                                                         |
| ----------------------------- | -------------------- | ------------------------------------------------------------------------------------- |
| **Single Project**            | Customer owns        | 4c (External Handoff) — customer receives maintenance schedule and runs it themselves |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) — Architect receives maintenance schedule and runs it for customer     |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention to keep dashboards accurate, relevant, and adopted.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task              | What to Check                                      | Red Flag Threshold                               |
| ------------------------- | -------------------------------------------------- | ------------------------------------------------ |
| Data Accuracy Spot-Check  | Compare 2-3 dashboard metrics against source data  | Any metric off by &gt; 2%                           |
| Dashboard Usage Audit     | Check executive login frequency and session count  | &lt; 50% of executives logged in during the month   |
| Alert Threshold Review    | Verify alert thresholds still align with targets   | Targets changed but thresholds not updated       |
| Data Refresh Monitoring   | Confirm all data connections syncing on schedule   | Any source &gt; 24 hours stale                      |

**Quarterly Tasks:**

| Quarterly Task                | What to Review                                          | Action if Off-Track                              |
| ----------------------------- | ------------------------------------------------------- | ------------------------------------------------ |
| Full Metric Definition Audit  | Re-validate all KPI calculations against Finance books  | Update calculation logic, re-reconcile           |
| New KPI Assessment            | Ask executives: any new questions dashboards can't answer? | Scope P1/P2 metric additions                     |
| Dashboard Relevance Review    | Which dashboards are used? Which are ignored?           | Retire unused views, refine active ones          |
| Data Source Health Check      | API connections stable? Any new data sources needed?    | Fix broken connections, evaluate new integrations |

**After First Business Cycle (30-90 days post-launch):**

- Full data accuracy reconciliation: compare one full month of dashboard data against Finance's close numbers
- Dashboard adoption assessment: Are executives using dashboards in meetings or still requesting ad-hoc reports?
- Alert effectiveness review: Were alerts actionable? Too many false positives?

**Refinement Triggers (when to re-engage):**

| Trigger                          | Threshold                                    | Response                                       |
| -------------------------------- | -------------------------------------------- | ---------------------------------------------- |
| Dashboard usage drops            | &lt; 30% of executives active for 2+ weeks      | Re-engage to identify adoption blockers        |
| Data accuracy complaints         | 2+ executives report wrong numbers           | Scope data quality remediation project         |
| New executive joins              | New CRO, VP, or CEO                          | Conduct 1:1 dashboard orientation + customize  |
| Business model changes           | New segment, pricing change, acquisition     | Scope metric reconfiguration project           |
| Board reporting requirements     | New board deck requirements                  | Add board-specific views                        |

**Every 6-12 Months:**

- Full dashboard suite review: relevance, accuracy, adoption metrics
- BI platform upgrade assessment: new features that could improve the suite
- Benchmark comparison: are the KPIs still the right ones? See Methodology for updated benchmark guidance.

---

### 4b. Internal Handoff (SME --&gt; Architect)

> **Purpose:** Transfer context so Architect can manage ongoing relationship.

**What the Architect needs to know:**

- What was built: dashboard suite structure, which metrics are on which views, how drill-downs work
- Customer context: key stakeholders and their preferences, data quirks (e.g., "Finance tracks ARR differently in Q4"), known sensitivities
- How data flows: source systems --&gt; BI platform, refresh schedules, alert logic
- When to escalate back to SME (see below)
- **Maintenance schedule** (if Dedicated engagement — Architect runs this)

**Escalation guidelines:**

| Issue Type                                 | Who Handles                   | Examples                                                |
| ------------------------------------------ | ----------------------------- | ------------------------------------------------------- |
| Small tweaks, minor questions              | Architect                     | Filter adjustments, threshold changes, user access      |
| Significant changes, complex issues        | SME                           | New metric additions, data source integrations, calculation changes |

**For Dedicated engagements:** Architect also receives the maintenance schedule (4a) and becomes responsible for executing it. SME walks Architect through each maintenance task in a 30-minute handoff session.

---

### 4c. External Handoff (LeanScale --&gt; Customer)

> **Purpose:** Formal project completion. Customer owns the dashboard suite.

**Final project meeting (45 min):**

- Review what was delivered: executive dashboard, role-specific views, alerts, automated distribution
- Walk through documentation package (see below)
- Confirm nothing outstanding: all bugs fixed, all feature requests logged
- Answer final questions
- Make it explicit: "Project complete"
- **For Single Project engagements:** Hand over the maintenance schedule (4a) and walk the customer through monthly/quarterly tasks

**Documentation package:**

- All training recordings (executive + technical)
- Metric definition guide with calculation logic for each KPI
- Data source mapping document (which system feeds which metric)
- Refresh schedule reference (when data updates for each source)
- Alert configuration document (thresholds, recipients, channels)
- Admin guide (adding users, modifying filters, updating thresholds)
- Troubleshooting guide (common issues and resolution steps — see below)
- Definition Alignment Document (final signed version)
- FAQ document
- **Maintenance Schedule** (for Single Project engagements)
- Support contact info

**Troubleshooting Guide (included in documentation package):**

| Scenario                                  | Resolution                                                             |
| ----------------------------------------- | ---------------------------------------------------------------------- |
| Dashboard shows stale data                | Check data connection status in BI platform admin; verify API credentials have not expired; confirm source system is online |
| ARR number doesn't match Finance          | Compare date ranges (dashboard may include in-progress deals); check if multi-year deal normalization is applied; verify discount handling |
| Pipeline coverage shows incorrect ratio   | Confirm denominator uses remaining quota (not full-period quota); verify pipeline includes only qualified stages |
| Alerts not firing                         | Check alert configuration in BI platform; verify recipient email/Slack; confirm threshold values match current targets |
| Executive can't access dashboard          | Verify user permissions in BI platform; check SSO/AD group membership; confirm role-based view assignment |
| Drill-down links broken                   | Check if underlying detail view was modified; verify filter pass-through logic; test in incognito to rule out cache |
| MQL counts don't match Marketing reports  | Confirm date range alignment; verify MQL definition matches (score threshold, status field); check for duplicate records |
| Sales velocity calculation looks wrong    | Verify all four components: opportunity count, average deal size, win rate, and cycle length are pulling from correct fields |

**For Single Project engagements:** Walk the customer through the maintenance schedule in detail. Record a walkthrough video so new team members can reference it.

**Output:** Customer owns the dashboard suite. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location (KPI matrix, metric definitions, tech spec, architecture docs)
- [ ] Handoff documentation complete and delivered
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized

#### Internal Debrief (Optional but Recommended)

- What went well? (e.g., stakeholder alignment was fast, data quality was better than expected)
- What would we do differently? (e.g., should have pushed harder on ARR definition in pre-kickoff)
- Any learnings to feed back into SOPs? (e.g., new edge case for data validation checklist)
- Dashboard adoption rate at handoff — track for benchmarking future projects

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell --&gt; Downsell --&gt; Retry |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (retainer for ongoing dashboard optimization + new metric builds)
   | if no
2. Downsell: Another one-time project (ARR Reporting, Forecasting Process, Monthly GTM Reporting Pack)
   | if yes
3. Retry retainer at end of next project cycle
```

**Script:**

> "Now that the Executive Reporting Suite is live, there are two ways we can continue working together. Option 1: We can set you up on managed services where we handle ongoing dashboard optimization, new metric builds, and quarterly reviews. Option 2: If there's a specific adjacent project you need — like detailed ARR reporting or a forecasting process — we can scope that out. Which sounds more interesting?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On [date ~90 days out], we'll review dashboard adoption, data accuracy, and whether any new metrics or views are needed."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                              |
| ------------------- | --------------------------------------------------------- |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks          |
| 2. Review metrics   | Pull dashboard usage data, assess adoption trends         |
| 3. Decide ownership | Can Architect handle this check-in, or need SME?          |
| 4. Prep materials   | If SME needed, brief them. If Architect, prep talking points. |

**At the refinement check-in:**

- Review dashboard adoption (login frequency, meeting usage)
- Assess data accuracy (any complaints or discrepancies reported?)
- Collect enhancement requests (new metrics, new views, new integrations)
- If minor: Architect handles tweaks
- If major: Scope new project (restart the assembly line)

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- KPI Priority Matrix (metrics by role with P0/P1/P2 ranking)
- Metric Definition Document (signed off by Finance and RevOps)
- Dashboard Architecture Spec (data flow, refresh schedules, hierarchy)

**Technical Deliverables:**

- Executive Dashboard (5-7 core metrics with actual vs. target)
- Role-Specific Drill-Down Views (CEO, CRO, VP Sales, VP Marketing, VP CS)
- Alert Configuration (threshold-based notifications via email/Slack)
- Automated Report Distribution (weekly summary, real-time alerts, monthly board template)
- Data Integration Connections (CRM, MAP, financial systems linked to BI platform)

**Documentation Package:**

- Training recordings (executive + technical admin)
- Metric definition guide with calculation logic
- Data source mapping reference
- Refresh schedule reference
- Alert configuration document
- Admin guide
- Troubleshooting guide
- Definition Alignment Document (final version)
- FAQ document
- Maintenance Schedule

---

## Appendix

### What This Document Is

This is the **implementation playbook** for Executive Reporting Suite projects — the step-by-step execution guide an Architect follows to deliver from first contact to project close. It is the third file in a 3-file playbook structure:

| File                  | Purpose                                                                  | Audience                 |
| --------------------- | ------------------------------------------------------------------------ | ------------------------ |
| `advisory.md`         | What the project IS — positioning, outcomes, approaches                  | Architect + Sales (scoping)     |
| `methodology.md`      | HOW we think about the problem — frameworks, concepts, best practices    | Architect (depth understanding) |
| `implementation.md`   | WHAT to DO — step-by-step execution with checklists                      | Architect (daily execution)     |

### What Each Phase Produces

| Phase                    | Output                                                                 | Gate Criteria                                                                  |
| ------------------------ | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **Phase 1: Strategy**    | Signed-off KPI matrix + Metric Definition Doc + Dashboard Architecture | Stakeholders approved definitions and architecture                             |
| **Phase 2: Engineering** | Built and tested dashboard suite with live data                        | Dashboards validated against source systems, stakeholders approved              |
| **Phase 3: Enablement**  | Trained team with documentation, automated delivery running            | Training delivered, hypercare complete, team can operate independently          |
| **Phase 4: Handoff**     | Independent customer + archived project                                | Internal/external handoffs complete, governance in place, project closed        |

### How to Adapt Per Project Type

This is a **Balanced** project:

| Dimension           | Weight   | Rationale                                                    |
| ------------------- | -------- | ------------------------------------------------------------ |
| Strategy            | 35%      | Heavy stakeholder alignment needed on metrics and definitions |
| Engineering         | 35%      | Significant technical build across multiple data sources      |
| Enablement          | 15%      | Training is critical but straightforward with good materials  |
| Handoff             | 15%      | Standard governance + maintenance + retention path            |

---

## References

[1] [OpsEthic - Advanced Pipeline Metrics for RevOps: The 2025 Blueprint](https://www.opsethic.com/blog/advanced-pipeline-metrics-revops-2025)

[2] [BARC / Eckerson Group - BI Adoption Rate Research via TechTarget](https://www.techtarget.com/searchbusinessanalytics/news/365530077/BI-adoption-poised-to-break-through-barrier-finally)

[3] Raw source document — Executive Reporting Suite playbook research, corroborated by dashboard utilization studies in B2B SaaS contexts

[4] [Dataversity - Why 60% of BI Initiatives Fail](https://www.dataversity.net/articles/why-60-of-bi-initiatives-fail-and-how-enterprises-can-avoid-it/)

[5] [SaaS Capital - 2025 B2B SaaS Growth Rate Benchmarks (CAC median data)](https://www.saas-capital.com/research/private-saas-company-growth-rate-benchmarks/)

[6] [RevPack - Tracking What Matters: RevOps Metrics for Performance and Growth](https://www.revpack.co/blog/revops-metrics-performance-growth/)
