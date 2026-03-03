# Renewal/Churn NRR/GRR Reporting — Implementation

## Project One-Pager

### Project Type

- Category: Balanced
- Primary Deliverable: Finance-reconciled retention dashboards (NRR, GRR, renewal pipeline, churn analysis) with documented metric definitions and CRM data model

#### Phase Relevance

| Phase          | Applies? | Weight | Notes                                                     |
| -------------- | -------- | ------ | --------------------------------------------------------- |
| 1. Strategy    | Yes      | Heavy  | 3-4 alignment loops; metric definition sign-off is critical |
| 2. Engineering | Yes      | Heavy  | CRM data model, automations, dashboards                   |
| 3. Enablement  | Yes      | Medium | CS team + leadership dashboard training                   |
| 4. Handoff     | Yes      | Medium | Maintenance cadence + Finance reconciliation process      |

· · ·

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │    Heavy     │     │    Heavy     │     │    Medium    │     │    Medium    │
  │ 1a→1b→1c→1d │     │ 2a→2b→2c→2d │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   3-4 alignment        Data model +         CS + leadership      Maintenance +
   loops + Finance      automations          dashboard training   Finance recon
```

**This project's flow:**
- Full 4-phase execution. Heavy strategy (metric definitions must be Finance-approved). Heavy engineering (data model + automations + dashboards). Standard enablement with CS and leadership training. Standard handoff with retention review cadence.
- No phases skipped. Strategy cannot compress below 3 meetings because Finance, CS, and Sales must each sign off on definitions.

· · ·

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Watch intro video explaining what NRR/GRR reporting is and why consistent definitions matter
- [ ] Complete intake form: current CRM, billing system, CS platform, existing retention reports, known definition conflicts
- [ ] Get Finance + CS leadership to pre-review the Definition Alignment Document (GRR, NRR, churn types, measurement periods)

##### Track B: Architect Prep
- [ ] Pull CRM data: audit opportunity object for renewal fields, contract/subscription records, existing churn tracking
- [ ] Run billing system audit: identify where subscription start/end dates, contract values, and renewal dates live
- [ ] Create v0 Retention Metrics Definition Guide with recommended formulas and edge-case handling
- [ ] Draft current-state assessment: where metrics are calculated today, who owns them, known discrepancies

· · ·

#### Refinement Loop (1b -- 1c -- 1d)

| Meeting           | Sub-Phase | Focus                                             | Stakeholder                  | Output                            |
| ----------------- | --------- | ------------------------------------------------- | ---------------------------- | --------------------------------- |
| Kickoff           | 1b        | Present v0 definitions, audit findings, gather input | VP CS, RevOps, Finance       | Feedback for v1 definitions       |
| Definition Review | 1c        | Review v1 definitions with Finance, resolve conflicts | Finance Lead, CS Ops         | v2 definitions (Finance-aligned)  |
| Data Architecture | 1c        | Validate data model, source mapping, edge cases   | RevOps, CRM Admin            | Approved data architecture        |
| Sign-Off          | 1d        | Final review of all definitions + dashboard mockups | All stakeholders             | Signed-off strategic package      |

· · ·

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held
- [ ] 1c. Refinement loop complete (v0 -- vFinal definitions)
- [ ] 1d. Strategic sign-off obtained (Finance + CS)

##### Phase 2: Engineering
- [ ] 2a. Tech spec created (data model, automations, dashboard specs)
- [ ] 2b. Engineering handoff meeting held
- [ ] 2c. Build complete (subscription model, renewal pipeline, churn tracking, dashboards)
- [ ] 2d. QA/Test + Finance validation + customer sign-off

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped
- [ ] 3b. Training sessions delivered (CS team + Leadership)
- [ ] 3c. Hypercare period complete (4 weeks)
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff (SME -- Architect) complete
- [ ] 4c. External handoff complete
- [ ] 4d. Project closed and archived

· · ·

#### Document Types

##### Working Documents (iterate together)

| Document                       | Purpose                                            | When Complete                                     |
|-------------------------------|----------------------------------------------------|--------------------------------------------------|
| Retention Metrics Definition Guide | Establish GRR, NRR, churn definitions company-wide | All terms Finance-approved, edge cases documented |
| Data Source Mapping            | Map where each data element lives and flows        | All fields identified, gaps documented            |
| Current State Gap Analysis     | Document what exists vs what needs building        | Gaps prioritized, effort estimated                |

##### Deliverables (polished outputs)

| Deliverable                   | Created From                        | Customer Uses For                              |
|------------------------------|-------------------------------------|-----------------------------------------------|
| Retention Metrics Definition Guide (final) | Working definition doc    | Board reporting alignment, internal reference |
| Dashboard Mockups             | Gap analysis + definition guide     | Stakeholder alignment on reporting views      |
| Data Architecture Diagram     | Data source mapping                 | Engineering reference, system documentation   |

· · ·

#### Enablement Details

##### Training Types

| Type       | Audience                              | Focus                                                    | Duration |
| ---------- | ------------------------------------- | -------------------------------------------------------- | -------- |
| Leadership | VP CS, CFO, CRO                      | Interpret NRR/GRR trends, renewal pipeline, churn drivers | 30 min   |
| CS Team    | CSMs, CS Ops, Renewal Managers        | Update renewal stages, record churn reasons, use dashboards | 45 min   |
| Technical  | RevOps, CRM Admin                     | Maintain data model, troubleshoot automations, add reports | 60 min   |

##### Hypercare
- Applies: Yes
- Duration: 4 weeks (covers at least one monthly close cycle)
- Office Hours: Yes -- weekly 30-min slot for CS team and RevOps

##### Training Assets to Create
- [ ] Video walkthrough: Executive dashboard (NRR/GRR gauges, trend interpretation)
- [ ] Video walkthrough: Renewal pipeline management for CSMs
- [ ] Doc: Churn reason coding guidelines and examples
- [ ] Doc: Metric Definitions Quick Reference Card
- [ ] Doc: Monthly close process for retention metrics

· · ·

#### Handoff & Retention

##### Internal Handoff (SME -- Architect)
- Key context for Architect: Metric definitions are Finance-approved and documented. Any definition change requires Finance sign-off before CRM modification. Dashboard filters and segments are configured per approved tier structure.
- Escalation trigger: Any request to change GRR/NRR formula, add new churn categories, or modify renewal automation logic.

##### External Handoff
- Final meeting agenda: Walk through all dashboards, confirm data accuracy against most recent period, review maintenance schedule, demonstrate churn reason coding.
- Documentation package: Retention Metrics Definition Guide, dashboard user guide, churn coding guidelines, maintenance schedule, training video recordings.

##### Maintenance Schedule
- Monthly: Validate GRR/NRR against Finance close, review churn reason completeness, check renewal pipeline coverage.
- Quarterly: Full metric reconciliation with board reporting, review segment definitions, assess leading indicator accuracy.
- Who owns: Single project = customer owns | Dedicated = Architect owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services -- if no -- Downsell: Customer Health Score project or Renewal Management automation -- Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~1 quarter after go-live
- Internal prep trigger: 2 weeks before check-in
- Decision: Architect handles / SME needed

· · ·

#### Key Assets

| Asset                               | When Used                 |
| ----------------------------------- | ------------------------- |
| Retention Metrics Definition Guide  | Phase 1 (Strategy)        |
| Data Source Mapping Template        | Phase 1 (Strategy)        |
| Dashboard Mockup Templates          | Phase 1c-1d               |
| Churn Reason Coding Guide           | Phase 2c, Phase 3b        |

· · ·

#### Definition Alignment Terms

| Term                      | Typical Definition                                                                                          |
| ------------------------- | ----------------------------------------------------------------------------------------------------------- |
| Gross Revenue Retention (GRR) | (Starting MRR - Contraction MRR - Churn MRR) / Starting MRR. Excludes expansion. Always &lt;= 100%.   |
| Net Revenue Retention (NRR)   | (Starting MRR + Expansion MRR - Contraction MRR - Churn MRR) / Starting MRR. Can exceed 100%.          |
| Voluntary Churn           | Customer actively decides to cancel or not renew.                                                          |
| Involuntary Churn         | Churn due to payment failure, administrative error, or non-engagement (no active cancellation decision).    |
| Revenue Churn             | Dollar value of lost recurring revenue from downgrades and cancellations.                                   |
| Logo Churn                | Count of customer accounts lost, regardless of revenue impact.                                              |
| Contraction MRR           | Reduction in recurring revenue from downgrades on existing accounts (not full cancellations).               |
| Expansion MRR             | Increase in recurring revenue from upsells, cross-sells, or price increases on existing accounts.           |
| Renewal Rate              | Won renewals / total renewals due in a period. Measured by count (logo) or value (dollar).                 |
| Cohort Period             | The measurement window for retention calculations (monthly, quarterly, or annual).                          |

· · ·

#### Common Gotchas

- Finance and CS report different churn numbers because they use different measurement periods or exclude different edge cases -- Lock definitions in Phase 1 with both teams in the room. Document edge-case treatment explicitly.
- Renewal opportunities are not created early enough, so the pipeline view is always stale -- Set automation to create renewal opps 90-120 days before contract end. Test automation on day one of Phase 2c.
- Mid-contract downgrades counted as churn instead of contraction -- Define contraction separately from churn in the Definition Guide. Build separate tracking fields.
- Multi-year contracts inflate GRR by hiding churn risk until contract end -- Track contract end dates explicitly and flag accounts approaching renewal in the at-risk dashboard widget.
- Churn reason codes not being filled in by CSMs -- Make churn reason a required field on the Closed Lost renewal opportunity. Train CS team on why this matters for pattern recognition.
- Historical data is inconsistent, causing validation failures with Finance -- Run the 4-6 quarter historical reconciliation in Phase 2d before go-live. Document known data quality gaps and their impact on metrics.

· · ·

#### Methodology Options

| Option                     | When to Use                                               | Complexity |
| -------------------------- | --------------------------------------------------------- | ---------- |
| Cohort-based retention     | Standard approach for most B2B SaaS companies             | Medium     |
| Rolling-period retention   | When cohort sizes are too small for meaningful analysis    | Low        |
| Segment-level retention    | When churn patterns differ significantly by tier/industry | High       |

See the Methodology page for detailed calculation frameworks, benchmark ranges, and edge-case decision trees.

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on retention metric definitions, data architecture, and dashboard specifications.
>
> **Output:** Retention Metrics Definition Guide (Finance-approved) + Data Architecture Map + Dashboard Mockups (signed off by CS, Finance, and RevOps).

### 1a. Pre-Kickoff

> Two parallel tracks run before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                              | Purpose                                                             | Format             |
| --------------------------------- | ------------------------------------------------------------------- | ------------------ |
| Intro video                       | Explain what NRR/GRR reporting is, why definitions must align, common pitfalls | Video (8-10 min) |
| Definition Alignment Document     | Pre-filled with recommended definitions for GRR, NRR, churn types, cohort periods | Google Doc     |
| Pre-filled intake form            | Confirm CRM platform, billing system, existing reports, known conflicts | Google Form or Doc |

**Definition Alignment Document contents:** GRR formula, NRR formula, voluntary vs involuntary churn, revenue churn vs logo churn, contraction vs full churn, measurement period (monthly/quarterly/annual), edge-case treatment (mid-contract downgrades, early renewals, multi-year contracts).

**Completion tracking:** RevOps or CS Ops contact follows up. Do not cancel kickoff if incomplete, but push hard -- Finance review of definitions is the long pole.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                        | Output                                       |
| ---- | ------------------------------------------------------------- | -------------------------------------------- |
| 1    | CRM audit: review subscription/contract objects, renewal fields, churn tracking | Data quality assessment + field inventory |
| 2    | Billing system review: identify authoritative source for MRR, contract dates | Source-of-truth mapping                   |
| 3    | Pull existing retention reports and compare to Finance board decks | Discrepancy documentation                |
| 4    | Create v0 Retention Metrics Definition Guide with recommended formulas | v0 definitions (all marked ASSUMED)      |
| 5    | Draft current-state gap analysis and future-state data architecture | Gap analysis + data flow diagram          |

**Critical:** Mark everything as ASSUMED. The kickoff call validates. Finance sign-off on definitions is the highest-risk gating item.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building anything.

| Term                        | Our Definition                                                                            | Internally Approved? |
| --------------------------- | ----------------------------------------------------------------------------------------- | -------------------- |
| Gross Revenue Retention     | (Starting MRR - Contraction - Churn) / Starting MRR, excludes expansion                 | [ ] Yes / [ ] No     |
| Net Revenue Retention       | (Starting MRR + Expansion - Contraction - Churn) / Starting MRR                          | [ ] Yes / [ ] No     |
| Voluntary Churn             | Customer actively cancels or does not renew                                               | [ ] Yes / [ ] No     |
| Involuntary Churn           | Churn from payment failure or administrative non-renewal                                  | [ ] Yes / [ ] No     |
| Revenue Churn               | Dollar value of MRR/ARR lost from cancellations and downgrades                           | [ ] Yes / [ ] No     |
| Logo Churn                  | Count of accounts lost regardless of revenue                                              | [ ] Yes / [ ] No     |
| Contraction                 | Revenue reduction from downgrades on active accounts (not full cancellation)              | [ ] Yes / [ ] No     |
| Measurement Period          | Monthly cohort as standard; quarterly and annual views derived                            | [ ] Yes / [ ] No     |
| Early Renewal Treatment     | Renewal closed before contract end resets the cohort start to new contract start          | [ ] Yes / [ ] No     |
| Multi-Year Contract Treatment | Counted in renewal cohort only when contract actually comes up for renewal              | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your Finance and CS leadership team. Check "Yes" when approved. We cannot build reporting until all terms are aligned -- disagreements here cause data discrepancies later.

---

### 1b. Kickoff Call

> **Purpose:** Present v0 definitions and audit findings. Identify where Finance and CS definitions conflict. Walk in with work done -- customer reacts, not creates from scratch.

#### Agenda (60-90 min)

| Time  | Topic                        | What Happens                                                  |
| ----- | ---------------------------- | ------------------------------------------------------------- |
| 0-15  | Walk through v0 definitions  | "Here's what we recommend based on industry standards"        |
| 15-30 | Validate with Finance        | Do these match how you report to the board?                   |
| 30-45 | Validate with CS             | Do these match how you track retention operationally?         |
| 45-55 | Surface conflicts            | Where Finance and CS definitions diverge -- document the gap  |
| 55-70 | Data quality findings        | Present CRM/billing audit results, identify gaps              |
| 70+   | Next steps                   | Assign definition homework, schedule definition review        |

#### What We Bring

- v0 Retention Metrics Definition Guide (pre-filled with recommended formulas)
- CRM and billing system audit results
- Data source mapping draft
- Current-state discrepancy documentation (e.g., "Finance says 92% GRR, CS reports 88%")
- Definition Alignment Document (pre-filled with our recommendations)

#### What We Leave With

- Documented conflicts between Finance and CS definitions
- Direction on measurement period (monthly vs quarterly cohorts)
- List of edge cases that need explicit treatment
- Clear homework: Finance reviews formulas, CS reviews churn categories
- Alignment loop scheduled

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Iterate on metric definitions and data architecture until Finance and CS are aligned and signed off.

#### The Pattern

```
Kickoff Call (surface conflicts, gather input)
    |
v0 definitions --> v1 (incorporate Finance + CS feedback)
    |
Meeting 2: Definition Review (Finance-focused, resolve formula conflicts)
    |
v1 --> v2 (Finance-approved formulas, updated edge-case treatment)
    |
Meeting 3: Data Architecture (validate source mapping, dashboard mockups)
    |
v2 --> vFinal (complete strategic package)
    |
Meeting 4: Final Review --> Sign-off
```

#### Meeting Types for This Project

| Meeting Type             | Focus                                                   | Stakeholder                    |
| ------------------------ | ------------------------------------------------------- | ------------------------------ |
| Definition Review        | GRR/NRR formulas, churn categories, edge-case treatment | Finance Lead, CS Ops           |
| Data Architecture Review | Source mapping, CRM data model, integration requirements | RevOps, CRM Admin              |
| Dashboard Review         | Dashboard mockups, reporting views, segment breakdowns  | VP CS, Finance, RevOps         |
| Final Review             | Complete package walkthrough, sign-off                  | All stakeholders               |

#### Typical Timeline

| Milestone               | Timing                                              |
| ----------------------- | --------------------------------------------------- |
| Pre-kickoff prep        | 2-3 days                                            |
| Kickoff call            | Day 1 of engagement                                 |
| Definition review       | Week 1-2 (depends on Finance availability)          |
| Data architecture review | Week 2-3                                           |
| Final review + sign-off | Week 3-4 (when all definitions CONFIRMED)           |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm all metric definitions are approved and data architecture is agreed before building.

#### Validation Checkpoint

- [ ] Retention Metrics Definition Guide signed off by Finance AND CS leadership
- [ ] GRR and NRR formulas documented with explicit edge-case treatment
- [ ] Churn categorization agreed (voluntary/involuntary, revenue/logo)
- [ ] Measurement period confirmed (monthly cohort standard)
- [ ] Data source mapping approved by RevOps
- [ ] Dashboard mockups reviewed and accepted
- [ ] All critical definitions CONFIRMED (vs ASSUMED)
- [ ] No unresolved conflicts between Finance and CS

#### Decision Point

- **Proceed to Engineering** -- Standard path. Customer wants full reporting system built in CRM.
- **Project does not stop here** -- Unlike some strategic projects, this project always proceeds to Phase 2. Definitions alone without operational reporting have limited value.

---

## Phase 2: Engineering

> **Goal:** Build and test the system based on approved strategic package.
>
> **Output:** Fully configured retention reporting system with validated metrics that match Finance board reporting.

| Project Type    | Engineering Weight | This Project                                                  |
| --------------- | ------------------ | ------------------------------------------------------------- |
| Strategic-heavy | Light (10-20%)     | N/A                                                           |
| **Balanced**    | **Medium-Heavy (50-60%)** | **This project -- data model + automations + dashboards** |
| Technical-heavy | Heavy (70-90%)     | N/A                                                           |

### Sub-Phases

```
2a Tech Spec --> 2b Engineering Handoff --> 2c Build --> 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate approved metric definitions into CRM configuration specifications.

**Input:** Signed-off Retention Metrics Definition Guide + Data Source Mapping + Dashboard Mockups

**Output:** Draft tech spec containing:

- **Subscription Data Model**: Object structure (Account -- Contract/Subscription -- Renewal Opportunity), required fields (contract start, end, value, renewal date, renewal owner), calculated fields (ARR, MRR)
- **Renewal Pipeline Automation**: Trigger timing (90-120 days before end), opportunity record type, stage definitions (Upcoming, In Progress, Committed, Closed Won, Closed Lost), probability mapping, owner assignment rules
- **Churn Tracking Configuration**: Churn reason picklist values, voluntary/involuntary categorization logic, churn date capture (effective vs decision date), automation to update account status on churn
- **Report Specifications**: GRR cohort calculation query, NRR cohort calculation query, renewal rate report, churn analysis by reason/segment/period, ARR waterfall (starting + new + expansion - contraction - churn = ending)
- **Dashboard Specifications**: Executive dashboard layout (NRR/GRR gauges, trend charts, pipeline summary, churn analysis), Operational dashboard layout (renewal pipeline by owner/stage, at-risk list, time filters)
- **Build Sequence**: Data model first -- renewal automation -- churn tracking -- core reports -- executive dashboard -- operational dashboard

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs with engineer before building.

**Who attends:** Architect + Engineer (or RevOps engineer)

**Agenda (45-60 min):**

| Time  | Topic                    | What Happens                                              |
| ----- | ------------------------ | --------------------------------------------------------- |
| 0-15  | Strategic context        | Why these definitions matter, what Finance approved       |
| 15-30 | Walk through tech spec   | Field-by-field review of data model and automations       |
| 30-45 | Dashboard specifications | Review report queries and dashboard layouts               |
| 45-60 | Risks and edge cases     | Data quality issues, integration dependencies, build order |

**What Architect brings:**

- Signed-off Retention Metrics Definition Guide (for context)
- Draft tech spec (from 2a)
- Data quality issues flagged during audit
- Questions list (anything flagged as unclear)

**What engineer leaves with:**

- Approved tech spec
- Clear build sequence (data model -- automations -- reports -- dashboards)
- Known risks: data quality gaps, integration latency, edge-case handling
- Access credentials for CRM, billing system, CS platform

---

### 2c. Build (Configure)

> **Purpose:** Build the retention reporting infrastructure in the customer's CRM and reporting tools.

**Input:** Approved tech spec from 2b

**Build components:**

**Component 1: Subscription Data Model**
- Create or configure contract/subscription object structure
- Add fields: contract start date, contract end date, contract value (ACV/ARR), renewal date, renewal owner
- Add tracking fields: expansion ARR, contraction ARR, churn reason, churn date, contract status (active/renewed/churned/downgraded)
- Configure object relationships: Account -- Contract -- Renewal Opportunity
- Set up auto-calculation fields for MRR derivation if needed

**Component 2: Renewal Pipeline Automation**
- Create renewal opportunity record type with appropriate stage values
- Build automation: create renewal opportunity 90-120 days before contract end date
- Configure renewal amount pre-population from prior contract value
- Define stages: Upcoming (10%), In Progress (30%), Committed (70%), Closed Won (100%), Closed Lost (0%)
- Configure renewal owner assignment rules (CSM or Account Manager based on customer's model)
- Test with 5-10 sample records across different contract types

**Component 3: Churn Tracking**
- Create churn reason picklist: competitive loss, budget/cost reduction, poor product fit, product gaps/missing features, poor support experience, merger/acquisition, involuntary (payment failure), other
- Configure churn event capture automation on Closed Lost renewal
- Build voluntary vs involuntary categorization logic
- Automate account status update on churn (active -- churned)
- Configure churn date capture (effective date of cancellation)

**Component 4: Core Retention Reports**
- Monthly GRR calculation report (cohort-based)
- Monthly NRR calculation report (including expansion)
- Renewal rate report (won/total due, by count and value)
- Churn analysis report (by reason, segment, time period)
- ARR waterfall report (starting ARR + new + expansion - contraction - churn = ending ARR)

**Component 5: Executive Dashboard**
- NRR and GRR gauges with benchmark targets (NRR &gt;100%, GRR &gt;90%)
- Rolling 12-month churn trend chart
- Renewal pipeline summary (by stage, amount, owner)
- Segment breakdowns (by tier, industry, contract value)
- At-risk account widgets and overdue renewal alerts
- Automated delivery schedule to leadership

**Component 6: Operational Renewal Dashboard**
- Renewal pipeline by owner and stage
- Time-based filters (this month, this quarter, next quarter)
- Health indicators per renewal (engagement score, support tickets, NPS if available)
- At-risk renewal list with early warning signals
- Expansion opportunity tracking alongside renewals
- Forecast vs actual renewal comparison
- Drill-down to individual account detail

**Build tracking:**

- [ ] Component 1: Subscription Data Model [status]
- [ ] Component 2: Renewal Pipeline Automation [status]
- [ ] Component 3: Churn Tracking [status]
- [ ] Component 4: Core Retention Reports [status]
- [ ] Component 5: Executive Dashboard [status]
- [ ] Component 6: Operational Renewal Dashboard [status]

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Validate that retention metrics match Finance expectations and dashboards serve operational needs.

**Two types of testing:**

| Type                   | Who               | Purpose                                                     |
| ---------------------- | ----------------- | ----------------------------------------------------------- |
| Technical Testing      | Our team          | Verify data flows, automations fire, calculations are correct |
| Finance Reconciliation | Finance + Our team | Verify metrics match historical board reports               |
| Customer Testing       | CS team + RevOps  | Verify dashboards are usable and actionable                  |

**Technical testing checklist:**

- [ ] All subscription/contract fields created and populated correctly
- [ ] Renewal opportunity automation fires at correct timing (90-120 days)
- [ ] Renewal amount pre-populates from prior contract value
- [ ] Churn reason is required on Closed Lost renewal opportunities
- [ ] Account status updates automatically on churn event
- [ ] GRR calculation matches manual calculation on test data
- [ ] NRR calculation matches manual calculation on test data
- [ ] ARR waterfall components sum correctly (starting + movements = ending)
- [ ] Dashboard filters work (time period, segment, owner)
- [ ] No duplicate renewal opportunities being created

**Finance reconciliation (critical):**

- [ ] Pull GRR/NRR from new system for last 4-6 quarters
- [ ] Compare to historical Finance board reports
- [ ] Investigate and resolve discrepancies (target: within 2% variance)
- [ ] Document any known data quality gaps affecting historical accuracy
- [ ] Get formal Finance sign-off on metric accuracy

**Customer testing:**

- Walk CS team through operational dashboard -- can they manage their renewal pipeline?
- Walk leadership through executive dashboard -- can they answer board questions?
- Have CSMs test churn recording workflow with sample scenarios
- Capture feedback, fix issues

**Engineering sign-off checkpoint:**

- [ ] All calculations match approved definitions
- [ ] Finance has validated historical metrics (within 2% tolerance)
- [ ] Dashboards render correctly with real data
- [ ] All automations tested with edge cases (multi-year contracts, mid-term downgrades, early renewals)
- [ ] Customer has tested and approved
- [ ] Ready for enablement

**Decision point:**

- **Proceed to Enablement** -- System is built and validated, needs training/adoption
- **Loop back to Build** -- Finance reconciliation fails, calculation issues found

---

## Phase 3: Enablement

> **Goal:** CS team, leadership, and RevOps can use the retention reporting system independently.
>
> **Output:** Trained team with documentation, stabilized system through first monthly close cycle.

### Sub-Phases

```
3a Training Prep --> 3b Training Sessions --> 3c Hypercare --> 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from the strategic package and built system.

**Input:** Retention Metrics Definition Guide + tech specs + built dashboards

**Output:** Training package containing:

- **Video walkthrough scripts**: Executive dashboard walkthrough, operational dashboard walkthrough, churn reason coding walkthrough
- **Written guides**: Metric Definitions Quick Reference Card, dashboard navigation guide, renewal pipeline management process, churn recording process
- **FAQ draft**: "Why doesn't my GRR match last quarter's board deck?" / "How do I handle a mid-contract downgrade?" / "What if a customer renews early?" / "When do I create a churn record vs a contraction?"

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge so each stakeholder group can use the system for their role.

**Training sessions by role:**

| Role                | Session Focus                                                                 | Duration |
| ------------------- | ----------------------------------------------------------------------------- | -------- |
| VP CS / CRO         | Executive dashboard interpretation: NRR/GRR trends, renewal pipeline health, churn patterns, board-ready views | 30 min |
| CFO / Finance Lead  | Metric definitions recap, how to pull retention numbers for board reporting, reconciliation process | 30 min |
| CSMs / Renewal Mgrs | Renewal pipeline management: updating stages, recording churn reasons, using at-risk alerts | 45 min |
| RevOps / CRM Admin  | System maintenance: how data flows, troubleshooting automations, adding new reports/filters, data quality monitoring | 60 min |

**Training delivery:**

1. Schedule sessions with appropriate stakeholders (group by role, not individual)
2. Deliver training live with screen share on actual production dashboards
3. Record video walkthroughs during or immediately after for async reference
4. Note questions -- feed into FAQ document

**Output:**

- Trained stakeholders across all four role groups
- Video recordings for each session
- Updated FAQ document based on questions asked

---

### 3c. Hypercare

> **Purpose:** Support the team through at least one full monthly close cycle to validate the system in production.

**Duration:** 4 weeks (minimum one monthly close cycle)

**What happens:**

- Weekly 30-min office hours for CS team and RevOps questions
- Quick-response support for data issues
- Monitor first monthly GRR/NRR calculation in production
- Assist with first monthly close reconciliation against Finance
- Bug triage: fix automation issues, dashboard rendering problems, data quality gaps
- Adjust churn reason categories if CSMs identify missing options

**When this project needs hypercare:** Always. Retention metrics only prove accurate after a full monthly cycle runs through the system. Skipping hypercare risks undetected calculation errors showing up in board reports.

**Output:** Stabilized system validated through at least one monthly close cycle, no critical issues outstanding.

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm customer team can operate retention reporting independently.

**Validation checkpoint:**

- [ ] All training sessions delivered (4 role groups)
- [ ] Training recordings and documentation provided
- [ ] At least one monthly close cycle completed through the system
- [ ] GRR/NRR from system matched Finance expectations for most recent period
- [ ] CS team is recording churn reasons consistently (&gt;90% of churned accounts have reason codes)
- [ ] No critical issues outstanding
- [ ] Customer team can operate without daily support
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** -- System is stable through monthly close, team is enabled
- **Extend Hypercare** -- First monthly close revealed issues, need another cycle

---

## Phase 4: Handoff

> **Goal:** Clean project close with maintenance plan established and retention/expansion path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the retention reporting system, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule --> 4b Internal Handoff --> 4c External Handoff --> 4d Project Close
                            (SME --> Architect)                              (Archive + Debrief)
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At                                                                         |
| ----------------------------- | -------------------- | ------------------------------------------------------------------------------------- |
| **Single Project**            | Customer owns        | 4c (External Handoff) -- customer receives maintenance schedule and runs it themselves |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) -- Architect receives maintenance schedule and runs it for customer |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention to keep retention metrics accurate and dashboards useful.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task                         | What to Check                                              | Red Flag Threshold                                     |
| ------------------------------------ | ---------------------------------------------------------- | ------------------------------------------------------ |
| GRR/NRR Reconciliation              | Compare system metrics to Finance close numbers            | &gt;2% variance from Finance-reported figures             |
| Churn Reason Completeness            | % of churned accounts with reason codes filled in         | &lt;90% completion rate                                   |
| Renewal Pipeline Coverage            | Are renewal opps being created 90+ days out?              | &gt;10% of upcoming renewals missing opportunities        |
| Dashboard Usage Audit                | Are CS and leadership accessing the dashboards?           | &lt;50% of trained users logged in during the month       |

**Quarterly Tasks:**

| Quarterly Task                       | What to Review                                             | Action if Off-Track                                    |
| ------------------------------------ | ---------------------------------------------------------- | ------------------------------------------------------ |
| Full Metric Reconciliation           | 3-month GRR/NRR trend vs Finance board deck               | Investigate root cause, adjust data or calculation     |
| Churn Pattern Analysis               | Are new churn reasons emerging? Do categories need updating? | Add/modify churn reason picklist values              |
| Segment Definition Review            | Are customer tiers/segments still accurate?                | Update segment criteria and dashboard filters          |
| Leading Indicator Assessment         | Are at-risk signals predicting actual churn?               | Refine early warning criteria                          |

**After First Business Cycle (60-90 days post-launch):**

- NRR/GRR Trend Validation: Do the numbers track in a direction consistent with what the business knows qualitatively? If NRR shows 115% but the team feels like retention is getting worse, investigate.
- Churn Reason Analysis: Do the reason codes captured in the first 60-90 days tell a coherent story? Are patterns actionable (e.g., 40% churn is "product gaps" -- is that being fed to Product)?
- Renewal Pipeline Accuracy: Did renewals that were marked "Committed" actually close? If forecast accuracy is &lt;80%, review stage definitions and probability mappings.

**Refinement Triggers (when to re-engage):**

| Trigger                              | Threshold                                                 | Response                                               |
| ------------------------------------ | --------------------------------------------------------- | ------------------------------------------------------ |
| GRR/NRR divergence from Finance      | &gt;5% variance persists for 2+ months                   | Re-engage SME for data audit and formula review        |
| Churn reason adoption drops          | &lt;70% completion rate for 2+ consecutive months        | Re-train CS team, review field requirements            |
| New business model or pricing change | Any material change to pricing, packaging, or contract structure | Scope refinement project for metric redefinition   |
| Acquisition or merger                | Acquired company's data needs integration                 | Scope data integration project                         |

**Every 6-12 Months:**

- Full Definition Review: Are the metric definitions still aligned with how the business operates? Board reporting standards may change.
- Dashboard Effectiveness Audit: Are stakeholders still using the dashboards? Which views are most/least used? Retire unused views, add requested ones.
- Benchmark Recalibration: Compare current GRR/NRR against updated industry benchmarks. Median SaaS GRR is approximately 90% and median NRR is 104-106% for companies in the $10M-$100M ARR range. If the customer is significantly off-benchmark, investigate.

---

### 4b. Internal Handoff (SME -- Architect)

> **Purpose:** Transfer context so Architect can manage ongoing relationship.

**What the Architect needs to know:**

- What was built: subscription data model, renewal pipeline automation, churn tracking, two dashboards (executive + operational)
- Key relationship context: Finance contact is the gatekeeper for any metric definition changes. CS Ops is the day-to-day operator.
- Common issues: churn reason field being skipped (needs gentle enforcement), dashboard filters being set incorrectly (users forgetting to adjust date range)
- **Maintenance schedule** (if Dedicated engagement -- Architect runs this)

**Escalation guidelines:**

| Issue Type                                                    | Who Handles                               |
| ------------------------------------------------------------- | ----------------------------------------- |
| Dashboard filter questions, adding a saved view, user access  | Architect                                 |
| Metric definition changes, formula modifications, new automation logic | SME              |
| New segment or churn category additions                       | Architect attempts first, SME if logic changes |

**For Dedicated engagements:** Architect also receives the maintenance schedule (4a) and becomes responsible for executing it. SME walks Architect through each monthly and quarterly task in detail.

---

### 4c. External Handoff

> **Purpose:** Formal project completion with customer.

**Final project meeting:**

- Review what was delivered: data model, automations, dashboards, documentation
- Walk through most recent month's GRR/NRR output to confirm accuracy
- Demonstrate churn reason reporting and renewal pipeline views
- Walk through maintenance schedule in detail
- Answer final questions
- Make it explicit: "Project complete"
- **For Single Project engagements:** Hand over the maintenance schedule and record a video walkthrough

**Documentation package:**

- Retention Metrics Definition Guide (final, Finance-approved version)
- Dashboard User Guide (executive + operational)
- Churn Reason Coding Guidelines with examples
- Renewal Pipeline Management Process
- Training video recordings (all 4 sessions)
- FAQ document
- Maintenance Schedule

**For Single Project engagements:** Walk the customer through the maintenance schedule in detail. Record a video walkthrough. Emphasize the monthly reconciliation with Finance as the single most important maintenance task.

**Output:** Customer owns the retention reporting system. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location
- [ ] Handoff documentation complete (all documents in documentation package)
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized

#### Internal Debrief (Optional but Recommended)

- What went well? (e.g., "Finance sign-off was fast because we pre-filled definitions")
- What would we do differently? (e.g., "Should have audited billing system earlier -- data gaps delayed engineering")
- Any learnings to feed back into processes?

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell -- Downsell -- Retry  |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (ongoing retention metric monitoring and optimization)
   | if no
2. Downsell: Customer Health Score project (predictive churn modeling builds on this data)
   | or: Renewal Management automation (workflow optimization on top of this reporting)
   | if yes
3. Retry retainer at end of next project cycle
```

**Script:**

> "Now that your retention reporting is live, there are two ways we can continue working together. Option 1: We can set you up on managed services where we monitor your metrics monthly and proactively flag issues. Option 2: A natural next step is building a Customer Health Score model -- you now have the churn data foundation to make that predictive. Which sounds more interesting?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On [date ~1 quarter out], we'll review how the retention metrics have tracked over the quarter and see if any definition adjustments or new dashboards are needed."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                                         |
| ------------------- | -------------------------------------------------------------------- |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks                     |
| 2. Review metrics   | Pull GRR/NRR trends, check Finance reconciliation variance, review churn patterns |
| 3. Decide ownership | Can Architect handle this check-in, or need SME?                    |
| 4. Prep materials   | If SME needed, brief them. If Architect, prep talking points.       |

**At the refinement check-in:**

- Review GRR/NRR trends against targets
- Check if churn reason data is driving actionable insights
- Identify any definition adjustments needed (new product lines, pricing changes)
- If minor: Architect handles tweaks
- If major: Scope new project (e.g., Customer Health Score model, Renewal Management automation)

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- Retention Metrics Definition Guide (Finance-approved): Company-wide definitions for GRR, NRR, churn types, measurement periods, and edge-case treatment
- Data Architecture Map: Source-to-dashboard data flow documentation
- Dashboard Mockups (evolved into live dashboards in Phase 2)

**Technical Deliverables:**

- Subscription Data Model: CRM object structure with all required fields
- Renewal Pipeline Automation: Auto-creation of renewal opportunities 90-120 days out with stage management
- Churn Tracking System: Reason code capture, categorization, and account status automation
- Executive Retention Dashboard: NRR/GRR gauges, trend charts, pipeline summary, churn analysis, segment breakdowns
- Operational Renewal Dashboard: Pipeline by owner/stage, at-risk alerts, time filters, forecast vs actual

**Documentation Package:**

- Training video recordings (4 sessions: Executive, Finance, CS team, Technical)
- Dashboard User Guide
- Churn Reason Coding Guidelines
- Renewal Pipeline Management Process
- Metric Definitions Quick Reference Card
- FAQ document
- Maintenance Schedule

---

## Appendix

### Roles

| Role | What They Do |
|---|---|
| **Architect** | Owns the customer relationship, leads strategy, creates specs, does enablement, owns account post-delivery |
| **Engineer** | CRM build, automation, dashboards (Phase 2) |
| **SME** | Project/implementation specialist brought in for project-specific work |

### What Each Phase Produces

| Phase                    | Output                                                                        | Gate Criteria                                                                                       |
| ------------------------ | ----------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| **Phase 1: Strategy**    | Finance-approved Retention Metrics Definition Guide + Data Architecture Map   | Finance and CS have signed off on all definitions. No unresolved conflicts.                         |
| **Phase 2: Engineering** | Built and tested retention reporting system                                   | All calculations match definitions. Finance reconciliation within 2%. Customer has approved.         |
| **Phase 3: Enablement**  | Trained team with documentation                                               | All training delivered. At least one monthly close cycle validated. Team can operate independently.  |
| **Phase 4: Handoff**     | Independent customer + archived project                                       | Internal/external handoffs complete. Maintenance schedule in place. Project closed.                  |

### Industry Context

SaaS companies that lack consistent retention metrics face real financial consequences. The median B2B SaaS GRR is approximately 90%, while median NRR ranges from 104-106% for companies in the $10M-$100M ARR range. Companies that track NRR consistently report stronger outcomes in investor conversations because they can demonstrate revenue expansion capacity.

The core problem this project solves is definition inconsistency. Nearly 40% of SaaS companies have material differences between how Finance and Customer Success calculate churn. These discrepancies erode board confidence and delay corrective action because leadership cannot agree on where the problem is.

Companies with formalized retention reporting processes identify at-risk accounts 45 days earlier on average than companies relying on ad-hoc analysis. Early identification directly reduces preventable churn.
