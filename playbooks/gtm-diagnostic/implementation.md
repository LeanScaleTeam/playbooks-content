# GTM Diagnostic — Implementation

## Project One-Pager

> Quick reference for architects. Scan in 2 minutes to understand the project, flow, and tools.

### Project Type

- Category: Strategic
- Primary Deliverable: Power10 Scorecard, color-coded Inspection Report (80+ checkpoints), and prioritized Roadmap

#### Phase Relevance

| Phase          | Applies? | Weight | Notes                                                        |
| -------------- | -------- | ------ | ------------------------------------------------------------ |
| 1. Strategy    | Yes      | Heavy  | Intake, reverse demo, definition alignment, scope validation |
| 2. Engineering | No       | N/A    | No system build; analysis and benchmarking are strategic work |
| 3. Enablement  | Light    | Light  | Results walkthrough serves as training; no system to train on |
| 4. Handoff     | Yes      | Medium | Three deliverable artifacts + transition to paid engagement   |

· · ·

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │    Heavy     │     │    [SKIP]    │     │    Light     │     │   Medium     │
  │ 1a→1b→1c→1d │     │     N/A      │     │   3a→3b      │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   Intake + Access      No build phase       Results walkthrough   Deliverables +
   Reverse Demo         (analysis happens     serves as training   Roadmap handoff
   Data extraction       within Phase 1)                           SOW transition
```

**This project's flow:**
- Full Phase 1 (heavy): Intake, NDA, access requests, reverse demo, data extraction, and analysis all happen within a compressed one-week timeline.
- Phase 2 is skipped entirely. There is no system build. The "engineering" equivalent is the analysis and benchmarking work, which is part of the strategic phase.
- Phase 3 is light: The results walkthrough (presenting Power10 Scorecard, Inspection Report, Roadmap) is the only enablement activity.
- Phase 4 covers deliverable handoff, engagement close-out, and transition to paid projects.

· · ·

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Sign NDA (or counter-sign their NDA)
- [ ] Complete intake questionnaire (company overview, GTM structure, known pain points, ARR range, team size, growth targets)
- [ ] Identify primary stakeholder and key contacts across Sales, Marketing, RevOps
- [ ] Provide read-only access to CRM (Salesforce or HubSpot)
- [ ] Provide access to marketing automation platform (HubSpot, Marketo, Pardot)
- [ ] Provide access to sales engagement tools (Outreach, Salesloft, Gong)
- [ ] Provide access to reporting/BI tools if separate from CRM

##### Track B: Architect Prep
- [ ] Validate all system access works; document login credentials securely
- [ ] Confirm data retention period available for analysis (minimum 90 days recommended)
- [ ] Review intake questionnaire responses for missing information
- [ ] Prepare reverse demo question list based on intake form gaps
- [ ] Schedule reverse demo session (60-90 min) and results walkthrough in advance

· · ·

#### Refinement Loop (1b → 1c → 1d)

| Meeting             | Sub-Phase | Focus                                                  | Stakeholder                    | Output                           |
| ------------------- | --------- | ------------------------------------------------------ | ------------------------------ | -------------------------------- |
| Reverse Demo        | 1b        | Client walks through their GTM processes and systems    | VP Sales, VP Marketing, RevOps | Documented current-state context |
| Analysis Check-in   | 1c        | Validate initial findings, clarify data questions       | RevOps lead, primary contact   | Confirmed analysis direction     |
| Results Walkthrough | 1d        | Present Scorecard, Report, Roadmap; gather feedback     | All stakeholders (CEO/CRO)     | Approved deliverables            |

· · ·

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (NDA signed, intake form returned, access granted)
- [ ] 1b. Reverse demo session held and recorded
- [ ] 1c. Data extraction and analysis complete (80+ checkpoints scored)
- [ ] 1d. Power10 Scorecard, Inspection Report, and Roadmap drafted

##### Phase 2: Engineering
- [ ] [SKIP] No engineering phase for GTM Diagnostic

##### Phase 3: Enablement
- [ ] 3a. Results walkthrough presentation prepared
- [ ] 3b. Results walkthrough delivered to stakeholders (60 min)

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented (quarterly re-diagnostic cadence)
- [ ] 4b. Internal handoff (SME to Architect) complete
- [ ] 4c. External handoff to customer complete with all three artifacts
- [ ] 4d. Project closed, SOW generated if client proceeds

· · ·

#### Document Types

##### Working Documents (iterate together)

| Document                     | Purpose                                           | When Complete                           |
| ---------------------------- | ------------------------------------------------- | --------------------------------------- |
| Intake questionnaire         | Capture company context, pain points, tool stack   | All fields filled by client             |
| Systems access tracker       | Track read-only access to all GTM tools            | All systems accessed and validated      |
| Raw data exports             | Consolidated dataset for 80+ checkpoint analysis   | Data organized into standardized format |
| Analysis working spreadsheet | Score checkpoints, calculate Power10 metrics       | All 80+ checkpoints rated R/Y/G         |

##### Deliverables (polished outputs)

| Deliverable         | Created From                    | Customer Uses For                                 |
| ------------------- | ------------------------------- | ------------------------------------------------- |
| Power10 Scorecard   | Analysis working spreadsheet     | Board presentation, investor updates, exec review |
| Inspection Report   | 80+ checkpoint scores + context  | Internal alignment on GTM gaps                    |
| Prioritized Roadmap | Grouped findings + effort est.   | Project planning, budget allocation               |

· · ·

#### Enablement Details

##### Training Types

| Type       | Audience                          | Focus                                   | Duration |
| ---------- | --------------------------------- | --------------------------------------- | -------- |
| Leadership | CEO/CRO, VP Sales, VP Marketing   | Interpret Power10 Scorecard and Roadmap | 60 min   |
| Technical  | RevOps, Sales Ops, Marketing Ops  | Understand Inspection Report details    | 30 min   |

##### Hypercare
- Applies: No (one-week bounded diagnostic; no system to support)
- Duration: N/A
- Office Hours: No (follow-up questions handled via email for 1 week post-delivery)

##### Training Assets to Create
- [ ] Video walkthrough: Power10 Scorecard (how to read, interpret, and act on scores)
- [ ] Doc: Inspection Report legend (what R/Y/G means, how to prioritize)
- [ ] Doc: Roadmap reading guide (sequencing rationale, effort estimates explained)

· · ·

#### Handoff & Retention

##### Internal Handoff (SME to Architect)
- Key context for Architect: Which findings resonated most with client, any pushback on recommendations, client's budget and appetite for follow-on work
- Escalation trigger: Client wants to change diagnostic scope or re-run specific sections

##### External Handoff (to Customer)
- Final meeting agenda: Deliver all three artifacts, answer remaining questions, discuss next steps
- Documentation package: Power10 Scorecard, Inspection Report, Prioritized Roadmap, recording of results walkthrough

##### Maintenance Schedule
- Recommended re-diagnostic cadence: every 6-12 months to track improvement
- Who owns: Customer owns (single project engagement)

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services (retainer to execute roadmap items) → if no → Downsell: Specific roadmap project (e.g., Lead Lifecycle, CRM Deduplication) → Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: 90 days post-diagnostic
- Internal prep trigger: 2 weeks before check-in
- Decision: Architect handles / SME needed

· · ·

#### Key Assets

| Asset                      | Format                  | When Used               |
| -------------------------- | ----------------------- | ----------------------- |
| Intake questionnaire       | Google Form / Doc       | Pre-kickoff (1a)        |
| NDA template               | Google Drive            | Pre-kickoff (1a)        |
| 80+ checkpoint checklist   | Spreadsheet template    | Analysis phase (1c)     |
| Power10 Scorecard template | Google Sheets / Excel   | Benchmarking (1c)       |
| Inspection Report template | Google Slides / Doc     | Report compilation (1d) |
| Roadmap template           | Google Slides / Sheets  | Roadmap build (1d)      |
| Brand template             | Google Slides           | All deliverables        |

· · ·

#### Definition Alignment Terms

| Term               | Typical Definition                                                                                              |
| ------------------ | --------------------------------------------------------------------------------------------------------------- |
| MQL                | Marketing Qualified Lead: A lead that meets demographic/firmographic criteria AND has taken a qualifying action  |
| SQL                | Sales Qualified Lead: A lead that sales has accepted and confirmed has budget, authority, need, and timeline     |
| SAL                | Sales Accepted Lead: A lead that has been accepted by sales for follow-up but not yet fully qualified           |
| Pipeline Coverage  | Total open pipeline value divided by quota/target for the period (3x is standard benchmark)                     |
| Win Rate           | Percentage of opportunities that close as won (from SQL or Opportunity Created stage)                           |
| CAC                | Customer Acquisition Cost: Total sales + marketing spend divided by new customers acquired in the period        |
| LTV                | Lifetime Value: Average revenue per customer multiplied by average customer lifespan                            |
| NRR                | Net Revenue Retention: Starting revenue + expansion - contraction - churn, divided by starting revenue           |
| Pipeline Velocity  | Number of deals x average deal value x win rate, divided by average sales cycle length (in days)                |
| CAC Payback Period | Months to recover the cost of acquiring a customer from gross margin                                            |

· · ·

#### Common Gotchas
- Systems access delayed by IT security review → Send access requests same day as NDA signing; identify IT contact upfront
- Client CRM has less than 90 days of usable data → Set expectations early; use directional analysis; document data gaps as a finding
- Definitions vary across teams (e.g., "MQL" means different things to Marketing and Sales) → Document definitions found in each system; call out inconsistencies as a finding
- Client expects strategy recommendations, not just a diagnosis → Set clear scope in intake call; diagnostic identifies WHAT to fix, not HOW; position roadmap as sequenced projects
- Data quality too poor for reliable metrics → Use data quality itself as a finding; flag in Inspection Report; prioritize data hygiene in Roadmap
- Stakeholders skip reverse demo or delegate to junior staff → Require VP-level attendance; explain that surface-level participation produces surface-level findings

· · ·

#### Methodology Options

| Option              | When to Use                                          | Complexity |
| ------------------- | ---------------------------------------------------- | ---------- |
| Full Diagnostic     | Standard engagement; 80+ checkpoints, all GTM areas  | Medium     |
| Focused Diagnostic  | Client wants specific area only (e.g., funnel only)  | Low        |
| Extended Diagnostic | Complex org with multiple BUs or GTM motions         | High       |

---

## Phase 1: Strategy

> **Goal:** Collect all inputs, conduct analysis, and produce three diagnostic deliverables ready for client presentation.
>
> **Output:** Power10 Scorecard, Inspection Report, and Prioritized Roadmap (all in draft for sign-off at results walkthrough).

### 1a. Pre-Kickoff

> Two parallel tracks run after the deal closes and before the reverse demo session.

#### Track A: Customer Homework

**What we send:**

| Item                   | Purpose                                                                                                         | Format                                    |
| ---------------------- | --------------------------------------------------------------------------------------------------------------- | ----------------------------------------- |
| NDA                    | Establish legal framework for system access                                                                      | PDF / DocuSign                            |
| Intake questionnaire   | Capture company overview, GTM structure, known pain points, ARR range, team size, growth targets                 | Google Form or Doc                        |
| Systems access request | Get read-only access to CRM, MAP, sales engagement, BI                                                          | Email with specific instructions per tool |

**GTM Diagnostic intake specifics:**
- Company stage: ARR range ($5M-$100M), growth rate, funding stage
- GTM team structure: headcount by function (Sales, SDR, Marketing, CS, RevOps)
- Current tool stack: CRM, marketing automation, sales engagement, enrichment, reporting
- Known pain points: What they think is broken (helps focus analysis)
- Growth targets: Where they want to be in 12 months (context for roadmap prioritization)
- Key contacts: Primary stakeholder + IT/admin for access troubleshooting

**Completion tracking:** Follow up daily on access requests. Do not start analysis until all system access is confirmed. Systems access is the number-one bottleneck -- according to RevOps practitioners, 40-60% of diagnostic delays stem from IT approval cycles and access provisioning [4].

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                              | Output                          |
| ---- | ------------------------------------------------------------------- | ------------------------------- |
| 1    | Validate all system access works; document credentials securely      | Access confirmation log         |
| 2    | Review intake questionnaire for missing information                  | Gap list for reverse demo       |
| 3    | Confirm data retention (minimum 90 days)                             | Data availability assessment    |
| 4    | Prepare reverse demo question list based on intake gaps              | Structured question doc         |
| 5    | Pre-schedule both sessions (reverse demo + results walkthrough)      | Calendar holds for stakeholders |

**Critical:** If access is delayed, escalate immediately. Every day of access delay compresses the analysis window. Build a 1-day buffer into the timeline.

#### Stakeholder Alignment Document

> The GTM Diagnostic has a lighter alignment requirement than build projects. Key terms to confirm:

| Term               | Our Definition                                                            | Internally Approved? |
| ------------------ | ------------------------------------------------------------------------- | -------------------- |
| MQL                | Lead meeting demographic/firmographic criteria + qualifying action        | [ ] Yes / [ ] No     |
| SQL                | Lead accepted by sales with confirmed BANT criteria                       | [ ] Yes / [ ] No     |
| Opportunity stages | The specific pipeline stages used in CRM (document each)                  | [ ] Yes / [ ] No     |
| Win                | Closed-Won in CRM with signed contract and booked ARR                     | [ ] Yes / [ ] No     |
| Churn              | Customer cancellation with no renewal; revenue fully lost                 | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition and confirm it matches your internal usage. Where your definitions differ, note the difference. Inconsistencies across teams are expected -- calling them out is part of the diagnostic value.

---

### 1b. Kickoff Call (Reverse Demo)

> **Purpose:** Have the client walk through their current GTM processes, systems, and setup. We observe and document -- the client demonstrates, not us.

#### Agenda (60-90 min)

| Time  | Topic                        | What Happens                                                                |
| ----- | ---------------------------- | --------------------------------------------------------------------------- |
| 0-10  | Introductions and scope      | Confirm diagnostic scope, timeline, and deliverable expectations            |
| 10-40 | Lead flow walkthrough        | Client demos lead journey: first touch → MQL → SQL → Opportunity → Close   |
| 40-55 | Handoff and reporting review | Document Marketing → SDR → AE → CS handoffs; review reporting cadence      |
| 55-70 | Pain points and workarounds  | Capture known issues, tribal knowledge, manual processes                    |
| 70-80 | Questions and follow-up      | Ask prepared questions from Track B prep; assign follow-up items            |
| 80-90 | Next steps                   | Confirm results walkthrough date; request any additional data access         |

#### What We Bring

- Structured question list (from Track B prep)
- Intake questionnaire responses (pre-read, with gaps highlighted)
- Access confirmation log (which systems we can/cannot reach)

#### What We Leave With

- Recorded session for reference during analysis
- Documented understanding of actual GTM operations
- List of handoff points and their stated SLAs
- Current reporting cadence and which metrics leadership reviews
- Known pain points, workarounds, and tribal knowledge
- Any additional data access needed

---

### 1c. Alignment Loop (Analysis Phase)

> **Purpose:** Execute the 80+ checkpoint analysis. This replaces the typical alignment loop because the GTM Diagnostic is analysis-driven, not iteration-driven. The Architect does the analysis work and may have one check-in with the client to validate initial findings.

#### The Pattern

```
Reverse Demo (gather context)
    |
Architect extracts raw data from all systems
    |
Architect runs 80+ checkpoint analysis
    |
Optional: mid-analysis check-in (clarify data questions)
    |
Architect compiles three deliverables
    |
Results Walkthrough (present findings)
```

#### Analysis Workflow

**Step 1: Extract and Organize Raw Data**

| Data Category         | Source                         | Export Format                                |
| --------------------- | ------------------------------ | -------------------------------------------- |
| Lead/contact records  | CRM (Salesforce/HubSpot)       | CSV with source, status, conversion dates    |
| Opportunity data      | CRM                            | CSV with stage history, close dates, amounts |
| Activity data         | CRM + Outreach/Salesloft/Gong  | CSV (emails, calls, meetings)                |
| Campaign performance  | Marketing automation platform   | CSV (spend, leads, conversions by campaign)  |
| Report configurations | CRM + BI tools                  | Screenshots + export configs                 |

**Step 2: Run Systems Inspection (Checkpoints 1-20+)**

| Inspection Area    | What to Assess                                                       | Rating Criteria                                                                                                                           |
| ------------------ | -------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| CRM data hygiene   | Required fields populated, picklist standardization, duplicate rate  | Green: &lt;5% dupe rate, &gt;90% field fill. Yellow: 5-15% / 70-90%. Red: &gt;15% / &lt;70% |
| Lead routing       | Assignment rules exist, fire correctly, cover all scenarios          | Green: Automated, tested. Yellow: Partial. Red: Manual/missing                                                                            |
| Integration health | CRM &lt;-&gt; MAP sync, activity capture, data consistency          | Green: Real-time sync, &lt;1% errors. Yellow: Batch sync, some gaps. Red: Broken/manual                                                   |
| User adoption      | Login frequency, data entry compliance, feature usage                | Green: &gt;80% weekly active. Yellow: 50-80%. Red: &lt;50%                                                                                |
| Data silos         | Disconnected tools, manual data transfer, shadow systems             | Green: Fully integrated. Yellow: 1-2 gaps. Red: Major silos                                                                               |

**Step 3: Analyze Funnel Process (Checkpoints 20-40+)**

For mid-market B2B SaaS companies ($10M-$100M ARR), benchmark conversion rates are [1][2]:
- Visitor to Lead: 1.4%
- Lead to MQL: 41%
- MQL to SQL: 39% (this is the biggest drop-off for most companies -- the MQL-to-SQL transition loses 15-21% of leads [2])
- SQL to Opportunity: 42%
- Opportunity to Close: 39%

Calculate each conversion rate for the client and compare against these benchmarks. Flag any stage more than 10 percentage points below benchmark as Red.

**Step 4: Evaluate Reporting Infrastructure (Checkpoints 40-60+)**

| Assessment Area       | Key Questions                                                                    |
| --------------------- | -------------------------------------------------------------------------------- |
| Metric definitions    | Are MQL/SQL/SAL defined consistently across CRM and MAP?                         |
| Data conflicts        | Do attribution models, source tracking, and conversion dates match?              |
| Leadership visibility | Does leadership have real-time dashboard access to pipeline and performance?     |
| Reporting gaps        | What should they track but do not? (e.g., pipeline velocity, CAC by channel)    |
| Data trustworthiness  | Can they make decisions based on their current data? Rate HIGH/MEDIUM/LOW        |

**Step 5: Calculate Power10 Scorecard (Checkpoints 60-80+)**

| Metric             | How to Calculate                                          | Benchmark (Mid-Market B2B SaaS)                       |
| ------------------ | --------------------------------------------------------- | ----------------------------------------------------- |
| CAC                | Total S&M spend / new customers acquired                   | Varies; New CAC Ratio median $2.00 per $1 ARR [3]     |
| CAC Payback Period | CAC / (monthly gross margin per customer)                  | Median 8.6 months; top quartile 5-7 months [3]        |
| LTV                | ARPA x gross margin % x (1 / churn rate)                  | Target: 3x+ CAC                                       |
| LTV:CAC Ratio      | LTV / CAC                                                 | 3:1 to 5:1 is healthy [3]                             |
| Win Rate           | Closed-Won / Total Opportunities                          | 20-30% for mid-market B2B SaaS [1]                    |
| Average Deal Size  | Total bookings / number of deals                          | Company-specific; benchmark against cohort            |
| Pipeline Coverage  | Total open pipeline / quota                               | 3x minimum; 4x preferred [5]                          |
| Pipeline Velocity  | (# deals x avg deal value x win rate) / avg cycle (days) | Company-specific; track trend                         |
| NRR                | (Start ARR + expansion - contraction - churn) / Start ARR | 100%+ is healthy; 110%+ is strong [6]                 |
| Churn Rate         | Churned ARR / Starting ARR (monthly or annual)            | &lt;10% annual gross churn for healthy SaaS [6]       |

---

### 1d. Strategic Sign-Off (Results Walkthrough Prep)

> **Purpose:** Confirm all analysis is complete and deliverables are ready before presenting to client.

#### Validation Checkpoint

- [ ] All 80+ checkpoints scored with R/Y/G ratings
- [ ] Power10 Scorecard complete with current values, benchmarks, and gap analysis
- [ ] Inspection Report drafted with four sections (Systems, Funnel, Reporting, Performance)
- [ ] Executive summary written (top 3-5 critical findings)
- [ ] Quick wins identified (low effort, high impact)
- [ ] Prioritized Roadmap built with project clusters, sequencing, and effort estimates
- [ ] All deliverables formatted with brand template
- [ ] Supporting data and screenshots included

#### Decision Point

- **Proceed to Results Walkthrough** → All analysis complete, deliverables polished
- **Extend Analysis** → Data access issues or data quality issues require more time (rare; communicate proactively)

---

## Phase 2: Engineering

> **[SKIP]** The GTM Diagnostic has no engineering phase. There is no system build, CRM configuration, or technical implementation. The analysis and benchmarking work that would conceptually map to "engineering" is performed within Phase 1 (1c: Alignment Loop / Analysis Phase).
>
> See the Methodology guide for detailed scoring frameworks and checkpoint definitions.

---

## Phase 3: Enablement

> **Goal:** Client stakeholders understand their diagnostic findings and can act on the Roadmap.
>
> **Output:** Informed stakeholders with clear next steps and recorded reference materials.

### Sub-Phases

```
3a Training Prep -> 3b Results Walkthrough
```

Note: 3c (Hypercare) and 3d (Enablement Sign-Off) are not applicable. The diagnostic is a bounded engagement with no ongoing system to support.

---

### 3a. Training Prep

> **Purpose:** Prepare the results walkthrough presentation from the three diagnostic deliverables.

**Input:** Completed Power10 Scorecard, Inspection Report, Prioritized Roadmap

**What happens:**

1. Architect assembles the presentation narrative: Scorecard first (headline metrics), then Inspection Report (detailed findings), then Roadmap (what to do about it)
2. Architect identifies the top 3-5 "aha moments" -- findings that will resonate most with this specific client based on reverse demo context
3. Architect prepares the upsell narrative: which Roadmap items map to available services

**Output:** Results walkthrough deck ready for live presentation

**GTM Diagnostic training materials:**
- Results walkthrough slide deck (branded)
- Power10 Scorecard one-pager (standalone artifact)
- Inspection Report (standalone artifact, color-coded)
- Prioritized Roadmap (standalone artifact, sequenced)

---

### 3b. Training Sessions (Results Walkthrough)

> **Purpose:** Present findings, scorecard, and roadmap to client stakeholders. This is the primary value delivery moment.

**Session: Results Walkthrough (60 min)**

| Time  | Topic                        | What Happens                                                           |
| ----- | ---------------------------- | ---------------------------------------------------------------------- |
| 0-5   | Recap scope and approach     | Remind stakeholders what we inspected and how                          |
| 5-20  | Power10 Scorecard review     | Walk through each metric with benchmark comparisons                    |
| 20-40 | Inspection Report highlights | Focus on critical findings (Red items), call out patterns              |
| 40-50 | Prioritized Roadmap review   | Present sequencing rationale, discuss dependencies                     |
| 50-55 | Quick wins                   | Highlight low-effort, high-impact fixes they can start immediately     |
| 55-60 | Q&A and next steps           | Answer questions, discuss engagement options                           |

**Audience:** CEO/CRO, VP Sales, VP Marketing, RevOps Leader (require VP-level attendance minimum)

**Output:**
- Client understands current GTM state and gaps
- Quick wins identified for immediate action
- Roadmap discussed and feedback gathered
- Session recorded for internal distribution

---

## Phase 4: Handoff

> **Goal:** Clean close with deliverables transferred, internal context documented, and retention path established.
>
> **Output:** Customer owns all three artifacts, project archived, SOW ready if proceeding.

**Structure:**

```
4a Maintenance Schedule -> 4b Internal Handoff -> 4c External Handoff -> 4d Project Close
                           (SME -> Architect)      (to Customer)          (Archive + Debrief)
```

---

### 4a. Maintenance Schedule

> **Purpose:** Define what ongoing monitoring looks like after the diagnostic. The diagnostic itself is a point-in-time snapshot -- value degrades without periodic re-assessment.

#### Standard Maintenance Framework

**Monthly Tasks:**

The GTM Diagnostic is a one-time engagement, so monthly maintenance is not included in scope. However, the Roadmap should recommend that the client track these monthly:

| Monthly Task                     | What to Check                                       | Red Flag Threshold                        |
| -------------------------------- | --------------------------------------------------- | ----------------------------------------- |
| Funnel conversion monitoring     | MQL-to-SQL and SQL-to-Opp conversion rates           | &gt;5 point drop from diagnostic baseline |
| Pipeline coverage check          | Open pipeline vs quota (3x minimum)                  | Coverage drops below 2.5x                 |
| Quick win implementation tracker | Are they executing the quick wins from the Roadmap?  | Zero quick wins completed after 30 days   |

**Quarterly Tasks:**

| Quarterly Task                | What to Review                                     | Action if Off-Track                        |
| ----------------------------- | -------------------------------------------------- | ------------------------------------------ |
| Power10 metric re-calculation | Recalculate all 10 scorecard metrics                | Compare to diagnostic baseline; flag drift |
| Roadmap progress review       | Are they executing roadmap items in sequence?        | Reprioritize if blocked                    |
| Data quality re-assessment    | Has CRM hygiene improved since diagnostic?           | If not improving, escalate data cleanup    |

**After First Business Cycle (90 days post-diagnostic):**

- Re-calculate Power10 Scorecard and compare to diagnostic baseline
- Assess whether quick wins have produced measurable improvement
- Key question: Are the critical Red findings moving toward Yellow or Green?

**Refinement Triggers (when to re-engage):**

| Trigger                             | Threshold                          | Response                              |
| ----------------------------------- | ---------------------------------- | ------------------------------------- |
| Pipeline coverage sustained decline | Below 2x for 2+ months             | Scope funnel optimization project     |
| Win rate deterioration              | &gt;5 point drop from baseline     | Scope sales process review            |
| Major GTM change                    | New segment, product, or motion    | Re-run full diagnostic with new scope |
| Post-roadmap execution              | 3+ roadmap items completed         | Re-diagnostic to measure improvement  |

**Every 6-12 Months:**

- Full GTM re-diagnostic recommended (can be lighter if baseline exists)
- Compare current state to previous diagnostic to measure improvement trajectory
- Update Roadmap based on new findings and completed items

---

### 4b. Internal Handoff (SME to Architect)

> **Purpose:** Transfer context so Architect can manage the ongoing relationship and any follow-on work.

**What the Architect needs to know:**

- Which findings resonated most with the client (and which were surprising)
- Client's stated priorities and budget for follow-on work
- Key stakeholder dynamics (who has decision authority, who was skeptical)
- Any data quality caveats that affected the analysis
- Which Roadmap items should be proposed first

**Escalation guidelines:**

| Issue Type                                   | Who Handles                        |
| -------------------------------------------- | ---------------------------------- |
| Client questions about reading the report    | Architect                          |
| Client wants to re-scope or re-run analysis  | SME                                |
| Follow-on project scoping                    | Architect (using Roadmap as input) |
| Methodology questions about benchmarks       | SME                                |

---

### 4c. External Handoff (to Customer)

> **Purpose:** Formal project completion with all deliverables transferred.

**Final deliverable email:**

Send within 24 hours of results walkthrough:

1. Power10 Scorecard (branded PDF or Excel)
2. Inspection Report (branded PDF or Slides, color-coded)
3. Prioritized Roadmap (branded PDF or Slides)
4. Recording of results walkthrough session
5. Quick reference: Inspection Report legend + Roadmap reading guide

**Explicit close:**

> "The GTM Diagnostic engagement is now complete. All three artifacts are attached. We recommend reviewing the Roadmap with your leadership team to prioritize next steps. If you'd like to discuss executing any of the recommended projects, we're ready to scope those out."

**For Single Project engagements:** Walk the customer through the recommended re-diagnostic cadence (every 6-12 months). Explain that the Power10 Scorecard is most valuable when tracked over time.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved (intake form, raw data exports, analysis spreadsheet, final deliverables)
- [ ] Handoff documentation complete
- [ ] Project status updated in internal tracking
- [ ] Time/billing finalized
- [ ] System access revoked

#### Internal Debrief (Optional but Recommended)

- What went well? (Which findings had the most impact? What was the client reaction?)
- What would we do differently? (Access delays? Data quality issues? Missing checkpoints?)
- Any learnings to feed back into the 80+ checkpoint list or Power10 framework?

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                       |
| ----------------------------- | -------------------------- |
| **Single Project**            | Upsell → Downsell → Retry  |
| **Multi-Project (Dedicated)** | Schedule Re-Diagnostic     |

**Single Project Path:**

```
1. Upsell: Managed Services retainer (execute full Roadmap)
   | if no
2. Downsell: Specific project from Roadmap (e.g., Lead Lifecycle, CRM Deduplication, Funnel Optimization)
   | if yes
3. Retry retainer at end of next project
```

**Script:**

> "Based on the diagnostic findings, there are two ways to move forward. Option 1: We work through the Roadmap systematically -- that's the fastest path to fixing the gaps we found. Option 2: If there's a specific area you want to tackle first, we can scope a focused project around your highest-priority Roadmap item. Which sounds more interesting?"

**Multi-Project (Dedicated) Path:**

Schedule a re-diagnostic at handoff:

> "In [6 months], we'll re-run the Power10 Scorecard to measure progress against the baseline we established today."

**Internal prep (2 weeks before re-diagnostic):**

| Step | What Happens                                                      |
| ---- | ----------------------------------------------------------------- |
| 1    | System reminder: re-diagnostic in 2 weeks                         |
| 2    | Pull original diagnostic scores, compare to current state         |
| 3    | Decide ownership: Can Architect handle this, or is SME needed?    |
| 4    | If SME needed, brief them. If Architect, prep comparison deck.    |

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

| Deliverable         | Description                                                                                                 | Format               |
| ------------------- | ----------------------------------------------------------------------------------------------------------- | -------------------- |
| Power10 Scorecard   | 10 critical GTM metrics scored against industry benchmarks                                                   | Branded PDF / Excel  |
| Inspection Report   | 80+ checkpoint assessment with R/Y/G ratings across Systems, Funnel, Reporting, Performance                 | Branded PDF / Slides |
| Prioritized Roadmap | Sequenced action plan with project clusters, effort estimates, and dependencies                              | Branded PDF / Slides |

**Technical Deliverables:**

None (no system build in this project type).

**Documentation Package:**

- Power10 Scorecard (standalone)
- Inspection Report (standalone, color-coded)
- Prioritized Roadmap (standalone)
- Results walkthrough recording (video)
- Quick reference: Inspection Report legend + Roadmap reading guide
- Definition Alignment Document (if applicable -- showing where definitions differed across teams)

---

## Appendix

### Roles

| Role          | What They Do                                                                             |
| ------------- | ---------------------------------------------------------------------------------------- |
| **Architect** | Owns the client relationship, leads the diagnostic, conducts analysis, presents findings  |
| **Engineer**  | Not applicable for GTM Diagnostic (no system build)                                       |
| **SME**       | Project/implementation team member with deep GTM benchmarking expertise                   |

---

### What Each Phase Produces

| Phase                    | Output                                                            | Gate Criteria                                                             |
| ------------------------ | ----------------------------------------------------------------- | ------------------------------------------------------------------------- |
| **Phase 1: Strategy**    | Power10 Scorecard + Inspection Report + Roadmap (drafted)          | All 80+ checkpoints scored, all 10 Power10 metrics calculated            |
| **Phase 2: Engineering** | [SKIP]                                                            | N/A                                                                       |
| **Phase 3: Enablement**  | Informed stakeholders with recorded walkthrough                    | Results walkthrough delivered, questions answered, artifacts transferred  |
| **Phase 4: Handoff**     | Customer owns artifacts, project closed, retention path set        | All deliverables sent, access revoked, SOW ready if proceeding           |

---

### How the Diagnostic Creates Value

**1. External benchmark.** Clients know something is broken but cannot tell whether their metrics are good or bad because they have no external reference point. The Power10 Scorecard provides that benchmark -- 76% of SaaS companies report a CAC payback period under 12 months [3], so a client at 18 months immediately knows they have a problem.

**2. Inspection of what they cannot see.** Leadership reviews pipeline and bookings but rarely audits the plumbing: CRM data hygiene, integration health, routing logic, activity capture completeness. The Inspection Report surfaces problems that have been invisible.

**3. Prioritization.** A list of 80+ findings is overwhelming. The Roadmap groups findings into executable projects, sequences them by impact and dependency, and estimates effort -- turning a diagnosis into an action plan.

**4. Gateway to execution.** Companies that conduct a structured GTM audit before making changes execute follow-on projects more effectively because the diagnostic establishes a shared understanding of what needs to change and why [4].

---

### The Reverse Demo Approach

The reverse demo is the defining feature of the GTM Diagnostic's strategy phase. Instead of presenting TO the client, we ask the client to present to US. This accomplishes three things:
1. Reveals actual processes (not documented processes) -- what people really do day-to-day
2. Surfaces tribal knowledge and workarounds that data alone cannot show
3. Builds client engagement (they feel heard, not talked at)

---

### Why One Week Works

The diagnostic is designed to be completed in 5 business days. This compressed timeline works because:
- Read-only access means no risk to client systems
- The 80+ checkpoint framework eliminates scope creep (fixed inspection points)
- Analysis templates and benchmark databases enable rapid comparison
- The client's biggest need is clarity, not perfection -- directional findings are more valuable than exhaustive analysis

---

### Diagnostic-to-Engagement Conversion

The diagnostic-to-paid-engagement conversion rate depends on three factors:
- Findings include at least 2-3 "aha moments" that validate known pain
- The Roadmap includes specific, scoped projects with effort estimates
- The follow-up SOW is sent within 48 hours of results walkthrough

Speed matters: send the SOW while findings are fresh. Every week of delay reduces conversion likelihood as organizational attention shifts to other priorities.

---

## References

[1] [First Page Sage - B2B SaaS Funnel Conversion Benchmarks](https://firstpagesage.com/seo-blog/b2b-saas-funnel-conversion-benchmarks-fc/)

[2] [The Digital Bloom - 2025 B2B SaaS Funnel Benchmarks &amp; Pipeline Audit Framework](https://thedigitalbloom.com/learn/pipeline-performance-benchmarks-2025/)

[3] [Benchmarkit - 2025 SaaS Performance Metrics](https://www.benchmarkit.ai/2025benchmarks)

[4] [OPEXEngine - GTM Audit Checklist: 20 Questions to Assess Your Strategy](https://www.opexengine.com/post/gtm-audit-checklist-20-questions-to-assess-your-strategy)

[5] [RevPartners - 2024 SaaS Metrics &amp; Benchmark Cheat Sheet](https://revpartners.io/hubfs/PDFs/SaaS%20Metric%20Cheat%20sheet.pdf)

[6] [Maxio - 2025 B2B SaaS Benchmarks Report](https://www.maxio.com/resources/2025-saas-benchmarks-report)
