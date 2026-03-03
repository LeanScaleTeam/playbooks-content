# Event Operations Lead List Intake Process — Implementation

---

## Project One-Pager

> Quick reference for architects. Scan in 2 minutes to understand what the project is, how it flows, and what tools are used.

### Event Operations Lead List Intake Process One-Pager

#### Project Type

- Category: Technical
- Primary Deliverable: Standardized, automated event lead intake workflow with import templates, deduplication logic, routing rules, and event ROI reporting

##### Phase Relevance

| Phase          | Applies? | Weight | Notes                                                       |
| -------------- | -------- | ------ | ----------------------------------------------------------- |
| 1. Strategy    | Yes      | Light  | 1-2 alignment loops for data requirements and field mapping |
| 2. Engineering | Yes      | Heavy  | Import templates, automations, routing rules, reports       |
| 3. Enablement  | Yes      | Med    | Event marketing team + sales team training                  |
| 4. Handoff     | Yes      | Med    | Process documentation + first live event validation         |

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────>│ 2. ENGINEER  │────>│3. ENABLEMENT │────>│  4. HANDOFF  │
  │    Light     │     │    Heavy     │     │     Med      │     │     Med      │
  │ 1a>1b>1c>1d │     │ 2a>2b>2c>2d │     │ 3a>3b>3c>3d │     │ 4a>4b>4c>4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   Audit & align        Build templates,     Train event mktg    Hand off process
   on data schema       automations,         + sales on new      ownership +
   + field mapping      routing, reports     intake workflow      first live event
```

**This project's flow:**
- Full 4-phase. Light strategy (data requirements already well-understood for most clients), heavy engineering (import templates, MAP workflows, CRM routing, dashboards), medium enablement (two audience tracks: event marketing and sales), medium handoff (validated with first live event).
- Strategy compresses to 2-3 meetings if the client has clear event history and existing campaign hierarchy. Expands if campaign structure needs to be built from scratch.

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Provide sample event lead lists from last 2-3 events (CSV exports from event platforms)
- [ ] Document current process for importing event leads into CRM/MAP
- [ ] List all event platforms in use (Eventbrite, Cvent, Splash, ON24, badge scanners)
- [ ] Provide CRM/MAP admin access with permissions to create fields, workflows, and reports
- [ ] Share planned event calendar for next quarter

##### Track B: Architect Prep
- [ ] Review sample event lists for data quality patterns (missing fields, inconsistent formats, duplicates)
- [ ] Audit existing CRM lead source and campaign hierarchy
- [ ] Draft preliminary field mapping document (event platform fields to CRM/MAP fields)
- [ ] Identify existing deduplication rules and assess gaps
- [ ] Build current state process map from list capture to CRM entry

#### Refinement Loop (1b > 1c > 1d)

| Meeting      | Sub-Phase | Focus                                                        | Stakeholder                     | Output                            |
| ------------ | --------- | ------------------------------------------------------------ | ------------------------------- | --------------------------------- |
| Kickoff      | 1b        | Present current state audit, validate field mapping draft     | Marketing Ops, Event Marketing  | Confirmed data requirements       |
| Refinement 1 | 1c        | Review campaign hierarchy, lead source taxonomy, routing rules | Marketing Ops, Sales Ops        | Approved field mapping + routing  |
| Sign-Off     | 1d        | Final approval of data schema, campaign naming, assignment rules | Marketing Ops, Event Marketing, Sales Leadership | Strategic sign-off to build      |

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (sample lists reviewed, CRM access verified, draft field mapping ready)
- [ ] 1b. Kickoff call held (current state validated, data requirements confirmed)
- [ ] 1c. Refinement loop complete (campaign hierarchy, lead source taxonomy, routing rules finalized)
- [ ] 1d. Strategic sign-off obtained (all stakeholders approve data schema and process design)

##### Phase 2: Engineering
- [ ] 2a. Tech spec created (import templates, workflow logic, routing rules, report specifications)
- [ ] 2b. Engineering handoff meeting held
- [ ] 2c. Build complete (templates, automations, routing, dashboards configured)
- [ ] 2d. QA/Test + customer sign-off (end-to-end test with sample event data)

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped (event team process guide, sales follow-up guide)
- [ ] 3b. Training sessions delivered (event marketing track + sales track)
- [ ] 3c. Hypercare period complete (first live event monitored)
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff (SME to Architect) complete
- [ ] 4c. External handoff to Customer complete
- [ ] 4d. Project closed and archived

#### Document Types

##### Working Documents (iterate together)

| Document                        | Purpose                                          | When Complete                                  |
| ------------------------------- | ------------------------------------------------ | ---------------------------------------------- |
| Current State Process Map       | Visualize existing event lead flow and pain points | All bottlenecks and manual steps documented    |
| Field Mapping Template          | Translate event platform fields to CRM/MAP fields | Every event source has validated mappings       |
| Lead Source Taxonomy            | Define picklist values and sub-categories          | Approved by Marketing Ops                      |
| Campaign Naming Convention      | Standardize event campaign structure               | Convention documented with examples            |
| Assignment Rules Matrix         | Define routing logic for event leads               | All routing scenarios covered                  |

##### Deliverables (polished outputs)

| Deliverable                    | Created From              | Customer Uses For                      |
| ------------------------------ | ------------------------- | -------------------------------------- |
| Import Template Package        | Field Mapping Template    | Standardized event lead imports        |
| Automation Workflow Diagrams   | Assignment Rules Matrix   | Internal documentation of routing logic|
| Event Lead Dashboard           | Report specifications     | Event ROI tracking and performance     |
| Process Guide                  | Current State Process Map | Ongoing reference for intake workflow  |

#### Enablement Details

##### Training Types

| Type       | Audience                         | Focus                                                       | Duration |
| ---------- | -------------------------------- | ----------------------------------------------------------- | -------- |
| Event Team | Event Marketing, Marketing Ops   | Import templates, naming conventions, submission workflow    | 45 min   |
| Sales      | AEs, SDRs, Sales Leadership      | Event lead identification, follow-up SLAs, context usage    | 30 min   |
| Technical  | Marketing Ops, RevOps Admin      | Automation maintenance, troubleshooting, report adjustments | 45 min   |

##### Hypercare
- Applies: Yes
- Duration: 2-3 weeks (covers at least one live event cycle)
- Office Hours: Yes -- weekly 30-min slot during first live event period

##### Training Assets to Create
- [ ] Video walkthrough: Import template walkthrough and submission process
- [ ] Video walkthrough: Event lead dashboard navigation
- [ ] Doc: Step-by-step import process guide with screenshots
- [ ] Doc: Event lead follow-up playbook for sales (templates + SLA expectations)
- [ ] Doc: Troubleshooting guide for common import errors

#### Handoff & Retention

##### Internal Handoff (SME to Architect)
- Key context for Architect: Import template versions, event platform integrations configured, deduplication match rules, assignment routing logic
- Escalation trigger: Any changes to deduplication logic, new event platform integrations, or campaign hierarchy restructuring

##### External Handoff
- Final meeting agenda: Process walkthrough, dashboard demo, maintenance schedule review, Q&A
- Documentation package: Import templates, process guide, troubleshooting doc, training recordings, maintenance schedule

##### Maintenance Schedule
- Monthly: Review import SLA compliance, duplicate rate audit, data quality scorecard
- Quarterly: Campaign hierarchy review, routing rule validation, event platform mapping updates
- Who owns: Single Project = customer owns | Dedicated = Architect owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services (ongoing event ops optimization) > if no > Downsell: Lead scoring model or attribution project > Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~1 quarter after initial launch
- Internal prep trigger: 2 weeks before
- Decision: Architect handles / SME needed

#### Key Assets

| Asset                  | When Used           |
| ---------------------- | ------------------- |
| Import Template (CSV)  | Every event import  |
| Field Mapping Doc      | New event platforms |
| Process Guide          | Ongoing reference   |
| Event Lead Dashboard   | Post-event reviews  |

#### Definition Alignment Terms

| Term                 | Typical Definition                                                                                 |
| -------------------- | -------------------------------------------------------------------------------------------------- |
| Event Lead           | A contact record captured at or through a company-sponsored or attended event                      |
| Lead Source          | The channel through which a lead entered the database (Trade Show, Webinar, Conference, etc.)      |
| Sub-Source           | The specific interaction type at an event (Booth Visit, Session Attendance, Demo Request, Badge Scan) |
| Campaign Membership  | Association of a lead record to a specific CRM campaign for attribution tracking                   |
| Import SLA           | Maximum time from event close to leads available in CRM (target: under 24 hours)                   |
| Hot Lead             | Event lead with high-priority interaction signals (demo request, pricing discussion, executive contact) |
| Deduplication        | Process of identifying and merging/flagging duplicate lead records based on matching criteria       |

#### Common Gotchas
- Event platform exports use different column headers for the same data -- always map before importing, never assume field names match
- Badge scan data often contains vendor/sponsor contacts mixed with real prospects -- build a filter step before import
- GDPR/CCPA consent fields are frequently missing from event platform exports -- add consent capture to event registration or have a post-event consent workflow
- Campaign membership requires Campaign ID at import time -- if the campaign does not exist in CRM yet, the import will fail silently or orphan records
- Round-robin assignment breaks when territories overlap -- define tiebreaker rules (existing account ownership wins first, then territory, then round-robin)

#### Methodology Options

| Option                   | When to Use                                                  | Complexity |
| ------------------------ | ------------------------------------------------------------ | ---------- |
| Manual Import Process    | Low event volume (&lt;4 events/quarter), simple data structure   | Low        |
| Semi-Automated (Templates + Workflows) | Moderate volume (4-12 events/quarter), multiple event types   | Medium     |
| Fully Automated (API Integration) | High volume (12+ events/quarter), dedicated event platform    | High       |

---

## Phase 1: Strategy

> **Goal:** Align on event lead data requirements, field mappings, campaign hierarchy, lead source taxonomy, and routing rules before building anything.
>
> **Output:** Approved field mapping document, lead source taxonomy, campaign naming convention, and assignment rules matrix.

### 1a. Pre-Kickoff

> Two parallel tracks run after the engagement is confirmed and before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                    | Format             |
| ----------------------------- | ---------------------------------------------------------- | ------------------ |
| Intro video                   | Explain the lead intake standardization project and outcomes | Video (5-10 min)  |
| Definition Alignment Document | Get sign-off on event lead, lead source, campaign terms     | Google Doc         |
| Pre-filled intake form        | Confirm event platforms in use, list volume, current SLAs   | Google Form or Doc |

**What the customer provides:**
- Sample event lead lists from last 2-3 events (CSV/Excel exports)
- List of event platforms currently in use (Eventbrite, Cvent, Splash, ON24, badge scan tools)
- Current campaign hierarchy structure (if one exists)
- CRM/MAP admin credentials with field creation and workflow editing permissions
- Upcoming event calendar for next 1-2 quarters

**Completion tracking:** Marketing Ops lead follows up. Do not cancel kickoff if homework is incomplete, but push hard -- the sample event lists are critical for pre-kickoff analysis.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                                   | Output                                          |
| ---- | ------------------------------------------------------------------------ | ----------------------------------------------- |
| 1    | Analyze sample event lists for data quality (field completeness, dupes)  | Data quality assessment with specific findings  |
| 2    | Audit existing CRM lead source picklist and campaign structure            | Current state inventory                         |
| 3    | Draft field mapping: event platform columns to CRM/MAP fields            | Draft field mapping template                    |
| 4    | Propose lead source taxonomy and campaign naming convention               | Lead source taxonomy document                   |
| 5    | Identify deduplication gaps in current CRM/MAP configuration             | Gap analysis with recommendations               |

**Data quality patterns to check in sample lists:**
- What percentage of records have valid email addresses?
- What percentage are missing required fields (company, title)?
- How many duplicates exist within a single list? Across lists?
- Are company names standardized or do they vary (e.g., "IBM" vs "International Business Machines")?
- Is consent/opt-in captured for GDPR/CCPA compliance?

Industry context: On average, 40% of B2B generated leads contain invalid, incomplete, or duplicate entries [1]. Sales reps waste approximately 550 hours annually -- nearly 14 weeks -- dealing with inaccurate CRM data [2]. These numbers increase for event leads because data comes from multiple capture methods (badge scans, manual forms, third-party apps) with no standardized schema.

**Critical:** Mark all draft mappings and proposed taxonomies as ASSUMED. The kickoff call validates.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building anything.

| Term                 | Our Definition                                                               | Internally Approved? |
| -------------------- | ---------------------------------------------------------------------------- | -------------------- |
| Event Lead           | Contact captured at or through a company-sponsored or attended event          | [ ] Yes / [ ] No     |
| Lead Source          | Primary channel (Trade Show, Webinar, Conference, Virtual Event, Roadshow)    | [ ] Yes / [ ] No     |
| Sub-Source           | Interaction type (Booth Visit, Session Attendance, Demo Request, Badge Scan)  | [ ] Yes / [ ] No     |
| Import SLA           | Maximum 24 hours from event close to leads available in CRM                   | [ ] Yes / [ ] No     |
| Hot Lead             | Event lead with demo request, pricing discussion, or executive-level contact  | [ ] Yes / [ ] No     |
| Campaign Membership  | Association to CRM campaign for attribution (requires Campaign ID on import)  | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your marketing and sales leadership. Check "Yes" when approved. We cannot proceed with the build until all terms are aligned -- misalignment here causes rework downstream, especially on lead source attribution and reporting.

---

### 1b. Kickoff Call

> **Purpose:** Present current state audit findings and validate draft field mappings. We walk in with analysis done -- customer reacts, not creates from scratch.

#### Agenda (60 min)

| Time  | Topic                         | What Happens                                                    |
| ----- | ----------------------------- | --------------------------------------------------------------- |
| 0-15  | Current state audit findings  | Present data quality issues found in sample lists               |
| 15-25 | Field mapping walkthrough     | Validate draft event platform to CRM/MAP field mappings          |
| 25-35 | Lead source taxonomy proposal | Review proposed picklist values and sub-source categories         |
| 35-45 | Campaign hierarchy review     | Align on naming convention and event type to campaign mapping    |
| 45-55 | Routing and assignment rules  | Discuss territory logic, round-robin, hot lead alerts             |
| 55-60 | Next steps                    | Schedule refinement meeting, assign homework for open items      |

#### What We Bring

- Data quality assessment from sample event lists (duplicate rates, field completeness percentages, format issues)
- Draft field mapping template
- Proposed lead source taxonomy with sub-source categories
- Campaign naming convention proposal (e.g., EVT-2025-Dreamforce-Booth)
- Questions on routing rules and SLA expectations

#### What We Leave With

- Validated or corrected field mappings
- Confirmed lead source picklist values
- Input on assignment rules and territory logic
- Clear list of open items (who owns what by when)
- Refinement meeting scheduled

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Iterate on data schema, routing rules, and reporting requirements until sign-off.

#### The Pattern

```
Kickoff Call (validate field mappings + taxonomy)
    |
    v
Update mappings, refine routing rules
    |
    v
Refinement Meeting (finalize campaign hierarchy, review routing, confirm reporting scope)
    |
    v
Final tech spec ready
    |
    v
Sign-Off
```

This project typically requires only 1 refinement meeting between kickoff and sign-off. The data schema and routing rules are concrete enough to finalize quickly. If campaign hierarchy needs to be built from scratch, add a second refinement meeting.

#### Before Refinement Meeting

1. Update field mapping document based on kickoff feedback
2. Build complete campaign naming convention with examples for each event type
3. Draft assignment rules matrix (all routing scenarios)
4. Prepare report specification outline (what dashboards and reports will be built)

#### During Refinement Meeting

1. Walk through updated field mappings -- confirm all ASSUMED items are now CONFIRMED
2. Review campaign hierarchy with real examples from upcoming events
3. Validate routing rules cover all edge cases (no territory match, existing customer, unknown company)
4. Confirm reporting requirements (which dashboards, which metrics, who sees what)

#### After Refinement Meeting

1. Finalize tech spec with all approved configurations
2. Create build sequence for engineering
3. Identify first target event for live validation

#### Potential Meeting Types

| Meeting Type     | Focus                                            | Stakeholder                    |
| ---------------- | ------------------------------------------------ | ------------------------------ |
| Data/Technical   | Field mappings, deduplication logic, integrations | Marketing Ops, RevOps          |
| Process/Workflow | Import workflow, SLAs, assignment rules           | Marketing Ops, Sales Ops       |
| Reporting        | Dashboard scope, metrics, attribution setup       | VP Marketing, Marketing Ops    |

#### Typical Timeline

| Milestone               | Timing                  |
| ----------------------- | ----------------------- |
| Pre-kickoff prep        | 2-3 days                |
| Kickoff call            | Day 1 of engagement     |
| Refinement meeting      | 3-5 days after kickoff  |
| Sign-off                | 5-7 days after kickoff  |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm all data schema, routing logic, and reporting scope are approved before building.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by Marketing Ops and Sales Leadership
- [ ] Field mapping template finalized for all event platforms in scope
- [ ] Lead source taxonomy and sub-source categories approved
- [ ] Campaign naming convention documented with examples
- [ ] Assignment/routing rules confirmed for all scenarios
- [ ] Deduplication matching criteria agreed (email primary, company+name secondary)
- [ ] Report and dashboard scope confirmed
- [ ] Import SLA target confirmed (under 24 hours)
- [ ] First live event identified for production validation

#### Decision Point

- **Proceed to Engineering** -- All data schema and process decisions approved. Build import templates, workflows, routing, and dashboards.

This project does not have a natural exit point after Phase 1. The strategic deliverable (field mapping, taxonomy) has no value without the engineering build.

---

## Phase 2: Engineering

> **Goal:** Build and test all import templates, MAP automation workflows, CRM routing rules, and reporting dashboards.
>
> **Output:** Fully configured intake system tested end-to-end with sample event data.

This project is engineering-heavy (60-70% of total effort). The build covers five workstreams: import templates, data processing workflows, routing/assignment rules, tracking configuration, and reporting/dashboards.

### Sub-Phases

```
2a Tech Spec > 2b Engineering Handoff > 2c Build > 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate approved field mappings, routing rules, and report requirements into technical specifications.

**Input:** Signed-off field mapping template, lead source taxonomy, assignment rules matrix, report scope

**What happens:**

1. Convert field mapping document into CRM/MAP field creation spec (field names, types, picklist values)
2. Define MAP workflow logic (triggers, conditions, actions) for lead processing
3. Specify deduplication match rules and merge/update behavior
4. Document assignment rule logic as executable routing rules
5. Spec out report and dashboard components with data sources and filters

**Output:** Tech spec containing:

- **Field specifications:** New CRM fields to create (Lead Source picklist values, Event Sub-Source, Event Name, Campaign ID, Import Date, Assignment Date, First Touch Date)
- **Import template specs:** Column headers, validation rules, required vs optional fields, file format requirements
- **Workflow logic:** Lead processing workflow triggered on Lead Source = event types. Steps: data standardization (company name normalization, title formatting) > field population (region from country, segment from company size) > duplicate check (match on email, then company+name) > status assignment > routing
- **Routing rules:** Territory-based assignment with round-robin fallback. Hot lead alert triggers for demo requests and pricing discussions. Existing account ownership takes priority.
- **Dashboard specs:** Lead intake volume by event, conversion funnel (Event Lead > MQL > SQL > Opportunity), speed-to-lead by event/rep, data quality scorecard (duplicate rate, field completeness, invalid records), event ROI summary

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs with engineer before building.

**Agenda (30-45 min):**

| Time  | Topic              | What Happens                                          |
| ----- | ------------------ | ----------------------------------------------------- |
| 0-15  | Walk through specs | Architect explains strategic context + tech spec       |
| 15-30 | Engineer questions | Clarify MAP workflow logic, dedup rules, API limits    |
| 30-45 | Refine and approve | Adjust specs, confirm build sequence and dependencies  |

**What Architect brings:**
- Strategic package (field mapping, taxonomy, routing matrix)
- Tech spec (field creation, workflow logic, report specs)
- Build sequence recommendation (fields first > templates > workflows > routing > reports)

**What engineer leaves with:**
- Approved tech spec
- Clear build sequence with dependencies
- Known risks: MAP rate limits for extended imports, CRM duplicate rule interaction with existing rules

---

### 2c. Build (Configure)

> **Purpose:** Build all components in the client's CRM and MAP systems.

**Input:** Approved tech spec from 2b

**Build sequence and components:**

#### Workstream 1: CRM/MAP Field Configuration
- [ ] Create or update Lead Source picklist (Trade Show, Webinar, Conference, Roadshow, Virtual Event)
- [ ] Create Sub-Source picklist (Booth Visit, Session Attendance, Demo Request, Badge Scan)
- [ ] Create Event Name text field
- [ ] Create/verify Campaign ID lookup field
- [ ] Create timestamp fields: Import Date, Assignment Date, First Touch Date
- [ ] Create lead status values for intake stages: New, Processing, Assigned, Contacted, Qualified

#### Workstream 2: Import Templates
- [ ] Build CSV import template with required columns, formatting guidelines, and sample data row
- [ ] Configure data validation rules in MAP (email format regex, required field checks)
- [ ] Build field mapping configurations for each event platform in scope (Eventbrite, Cvent, Splash, ON24)
- [ ] Test import template with sample data from each platform to verify mapping accuracy

#### Workstream 3: Lead Processing Workflows
- [ ] Build lead processing workflow triggered by Lead Source = Event types
- [ ] Configure data standardization steps (company name normalization, title standardization)
- [ ] Set up automated field population (region from country, segment from company size)
- [ ] Create deduplication logic: match on email (primary), then company+name (secondary)
- [ ] Configure duplicate handling: update existing record with latest event data OR create new with merge flag
- [ ] Set up lead status assignment based on data completeness and engagement signals

#### Workstream 4: Assignment and Routing
- [ ] Configure territory-based assignment rules for event leads
- [ ] Set up round-robin assignment for unowned/new accounts
- [ ] Build hot lead alert automation (email + in-app notification for demo requests, pricing discussions)
- [ ] Create fallback assignment rules (no territory match > default pool, existing customer > account owner)
- [ ] Test assignment logic across all routing scenarios

#### Workstream 5: Reporting and Dashboards
- [ ] Build lead intake report: volume by event, source breakdown, import SLA compliance
- [ ] Create conversion funnel report: Event Lead > MQL > SQL > Opportunity by event
- [ ] Build speed-to-lead report: time from import to first sales touch by event/rep
- [ ] Create data quality scorecard: duplicate rate, field completeness, invalid records per import
- [ ] Assemble executive dashboard with event ROI summary and trend analysis
- [ ] Configure MAP-to-CRM sync for unified engagement data view

**Execution approach:** Manual build for this project type. Workflow logic, deduplication rules, and assignment routing require careful configuration and testing that does not lend itself to automation.

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify the complete intake system works end-to-end and get customer approval.

**Two types of testing:**

| Type              | Who         | Purpose                                            |
| ----------------- | ----------- | -------------------------------------------------- |
| Technical Testing | Our team    | Verify all workflows fire, fields populate, routing works |
| Customer Testing  | Customer    | Verify process meets their operational needs       |

**Technical testing checklist:**

- [ ] Import template correctly maps all fields from each event platform
- [ ] Data validation rejects records with missing required fields (email, first name, last name)
- [ ] Data validation rejects malformed email addresses
- [ ] Lead processing workflow fires on new event lead creation
- [ ] Company names normalize correctly (test with common variations)
- [ ] Deduplication correctly identifies existing records by email match
- [ ] Deduplication correctly handles company+name secondary match
- [ ] Duplicate handling creates merge flag (not silent overwrites)
- [ ] Territory-based assignment routes to correct owner
- [ ] Round-robin distributes evenly for unowned accounts
- [ ] Hot lead alerts fire within 5 minutes for demo request leads
- [ ] Fallback routing handles no-territory-match and existing-customer scenarios
- [ ] All timestamp fields populate correctly (Import Date, Assignment Date)
- [ ] Lead status transitions work through full lifecycle (New > Processing > Assigned > Contacted > Qualified)
- [ ] Reports display accurate data with correct filters
- [ ] Dashboard loads within acceptable time (&lt;5 seconds)
- [ ] MAP-to-CRM sync pushes engagement data correctly

**Customer testing:**

- Walk event marketing team through full import process using a test list
- Have sales team verify lead appearance in CRM with correct source tags and assignment
- Review dashboards with Marketing Ops to confirm attribution accuracy
- Test hot lead alert with sales rep to verify notification timing and content

**Engineering sign-off checkpoint:**

- [ ] Built system matches tech spec
- [ ] All technical tests passing
- [ ] Customer has tested import process and routing
- [ ] Customer has reviewed dashboards and approved report logic
- [ ] Ready for enablement

**Decision point:**
- **Proceed to Enablement** -- System is built and tested. Train teams.
- **Loop back to Build** -- Issues found in testing. Fix and re-test.

---

## Phase 3: Enablement

> **Goal:** Event marketing team can execute imports independently. Sales team understands follow-up expectations and knows how to use event context in outreach.
>
> **Output:** Trained teams with documentation, stabilized system validated with at least one live event.

### Sub-Phases

```
3a Training Prep > 3b Training Sessions > 3c Hypercare > 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from the built system and process documentation.

**Input:** Configured system + tech specs + approved process design

**What happens:**

1. Create step-by-step import guide with screenshots for each event platform
2. Build follow-up playbook for sales with email/call templates
3. Draft FAQ document from common questions seen in similar projects
4. Prepare scripts for recording video walkthroughs

**Output:** Training package containing:

- **Event Marketing Team Guide:** Step-by-step import process (download list > format per template > validate > upload), campaign naming checklist, timing expectations (submit within 4 hours of event close)
- **Sales Follow-Up Playbook:** How to identify event leads in CRM, follow-up SLA (first touch within 24 hours), how to use event context (booth notes, session attended, demo request details) in personalized outreach, email/call templates
- **Technical Admin Guide:** Workflow maintenance, troubleshooting common import errors, how to add new event platforms, report adjustment procedures
- **FAQ Document:** Covering common scenarios (what if a lead already exists? what if no Campaign ID? what if consent is missing?)

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to customer teams.

**Three training tracks:**

| Track             | Audience                        | Focus                                                               | Duration |
| ----------------- | ------------------------------- | ------------------------------------------------------------------- | -------- |
| Event Marketing   | Event team, Marketing Ops       | Import templates, naming convention, submission timing, common scenarios (trade show, webinar, third-party event) | 45 min   |
| Sales             | AEs, SDRs, Sales Leadership     | Event lead identification in CRM, 24-hour SLA, using event context in outreach, where to find event pipeline reports | 30 min   |
| Technical Admin   | Marketing Ops Admin, RevOps     | Workflow maintenance, adding new event platforms, troubleshooting, report adjustments | 45 min   |

**Training delivery:**

1. Schedule sessions by track -- event marketing first, sales second, technical third
2. Deliver live with screenshare showing the actual system (not slides)
3. Walk through real scenarios: trade show booth list, webinar attendee export, third-party event badge scan data
4. Record each session as a video walkthrough for future onboarding
5. Answer questions live, capture any gaps for FAQ update

**Output:**
- Trained stakeholders across all three tracks
- Video recordings for each training session
- Updated FAQ with questions from live sessions

---

### 3c. Hypercare

> **Purpose:** Monitor and support the first live event processed through the new system.

**Duration:** 2-3 weeks (timed to cover at least one live event from list receipt through sales follow-up completion)

**What happens during hypercare:**

- **Day of import:** Monitor first production import in real-time. Verify field mapping, deduplication, and routing work with live data.
- **First 24 hours:** Confirm hot lead alerts fire. Verify sales reps receive correct assignments. Check import SLA compliance.
- **First week:** Review data quality scorecard for first import. Address any mapping issues or routing misconfires. Hold office hours (30-min weekly slot) for questions.
- **Week 2-3:** Monitor sales follow-up rates. Review speed-to-lead metrics. Address any edge cases that emerged with real data.

**When to skip:** This project should not skip hypercare. The first live event is the true test -- sample data testing cannot fully replicate the variety of real event data. Research shows that 71% of internet leads are wasted due to poor or slow follow-up [3], and event leads go cold within 48-72 hours [4]. The hypercare period ensures the system works before the next event.

**Output:** Validated system with at least one successful live event cycle. No critical issues outstanding.

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm the customer team can operate the intake process independently.

**Validation checkpoint:**

- [ ] Event marketing team successfully executed at least one production import without assistance
- [ ] Sales team followed up on event leads within 24-hour SLA
- [ ] Import SLA met (&lt;24 hours from event close to leads in CRM)
- [ ] All training sessions delivered and recorded
- [ ] FAQ document updated with real questions from hypercare
- [ ] No critical issues outstanding
- [ ] Technical admin can troubleshoot common import errors independently
- [ ] Ready for handoff

**Decision point:**
- **Proceed to Handoff** -- Customer is enabled, first event validated
- **Extend Hypercare** -- Significant issues in first live event, need additional monitoring

---

## Phase 4: Handoff

> **Goal:** Clean project close with maintenance plan established, documentation delivered, and retention/expansion path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the process, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule > 4b Internal Handoff > 4c External Handoff > 4d Project Close
                          (SME > Architect)     (LS > Customer)       (Archive + Debrief)
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At |
| ----------------------------- | -------------------- | ------------- |
| **Single Project**            | Customer owns        | 4c (External Handoff) |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention after the project is complete.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task                  | What to Check                                        | Red Flag Threshold                                  |
| ----------------------------- | ---------------------------------------------------- | --------------------------------------------------- |
| Import SLA Compliance         | Time from event close to leads in CRM for each event | Any event exceeding 48 hours                        |
| Duplicate Rate Audit          | Percentage of imported records flagged as duplicates  | Duplicate rate exceeding 10% on any single import   |
| Data Quality Scorecard        | Field completeness, invalid emails, missing Campaign IDs | Field completeness below 85% for required fields    |
| Follow-Up SLA Monitoring      | Percentage of event leads with first touch within 24 hours | Below 70% first-touch compliance                   |

**Quarterly Tasks:**

| Quarterly Task                       | What to Review                                       | Action if Off-Track                                 |
| ------------------------------------ | ---------------------------------------------------- | --------------------------------------------------- |
| Campaign Hierarchy Review            | New event types or naming that does not follow convention | Update taxonomy, retrain event team on naming       |
| Routing Rule Validation              | Territory changes, new rep onboarding, reassignments | Update assignment rules, test with sample leads      |
| Event Platform Mapping Audit         | New platforms added, schema changes in existing ones  | Create new field mappings, update import templates   |
| Conversion Funnel Analysis           | Event Lead > MQL > SQL > Opp rates by event type     | Investigate underperforming events, adjust targeting |

**After First Business Cycle (60-90 days post-launch):**

- **Event ROI Validation:** Do closed-won opportunities have correct event campaign attribution? Can you calculate cost per lead and ROI by event?
- **Speed-to-Lead Impact Check:** Has faster follow-up (under 24 hours vs previous 5+ days) produced measurable improvement in SQL conversion? Research shows leads contacted within 5 minutes are 21x more likely to qualify [5], and event leads contacted within 1 hour drive 7x higher qualification versus follow-up after 24 hours [6].
- **Process Adoption Check:** Is the event marketing team consistently using the import templates? Are there any manual workarounds that bypass the standardized process?

**Refinement Triggers (when to re-engage):**

| Trigger                        | Threshold                              | Response                                            |
| ------------------------------ | -------------------------------------- | --------------------------------------------------- |
| Duplicate rate spike           | >15% duplicates for 2+ consecutive events | Audit dedup rules, check for new data sources      |
| Import SLA degradation         | >48 hours for 3+ events in a quarter   | Investigate bottleneck, retrain or automate          |
| Sales follow-up compliance drop | Below 50% first-touch within 24 hours  | Escalate to sales leadership, review alert config   |
| Event platform change           | New platform adopted or existing deprecated | Scope field mapping update project                  |

**Every 6-12 Months:**

- Full process review: Is the intake process still matching current event strategy?
- Lead source taxonomy audit: Any new event types that need picklist additions?
- Report and dashboard refresh: Are stakeholders still using the dashboards? Any new metrics needed?
- Technology review: Has the client added or changed CRM/MAP platforms?

---

### 4b. Internal Handoff (SME to Architect)

> **Purpose:** Transfer context so Architect can manage ongoing relationship.

**What the Architect needs to know:**

- Which event platforms are configured and how field mappings work for each
- Deduplication matching logic and what to do when merge conflicts arise
- Assignment routing hierarchy (territory > account ownership > round-robin)
- Hot lead alert configuration and who receives notifications
- Dashboard structure and common filter adjustments
- **Maintenance schedule** (if Dedicated engagement -- Architect runs this)

**Escalation guidelines:**

| Issue Type                                          | Who Handles | Example                                           |
| --------------------------------------------------- | ----------- | ------------------------------------------------- |
| Template formatting questions, minor field updates  | Architect   | "Add a new Sub-Source value to the picklist"       |
| New rep added to routing, dashboard filter changes   | Architect   | "Update round-robin to include new SDR hire"       |
| New event platform integration, dedup rule changes   | SME         | "We switched from Eventbrite to Cvent"             |
| Campaign hierarchy restructuring, workflow logic changes | SME     | "We need to add a new event type category"         |

**For Dedicated engagements:** Architect receives the maintenance schedule (4a) and executes monthly/quarterly tasks. SME walks Architect through each maintenance task with real examples.

---

### 4c. External Handoff

> **Purpose:** Formal project completion with customer.

**Final project meeting agenda:**

1. Review what was delivered (summary of all configured components)
2. Walk through documentation package
3. Demo: Execute a sample import using the standardized template (live in their system)
4. Walk through dashboards and reports
5. Review maintenance schedule (monthly and quarterly tasks)
6. Confirm next event on calendar and readiness
7. Answer final questions
8. Make it explicit: "Project complete"
9. **For Single Project engagements:** Walk customer through the maintenance schedule in detail

**Documentation package:**

- Import template package (CSV template, formatting guide, per-platform instructions)
- Process guide (step-by-step: event close > list download > format > validate > import > verify)
- Field mapping reference document
- Lead source taxonomy and campaign naming convention document
- Assignment rules documentation
- Troubleshooting guide (common import errors, dedup conflicts, routing mismatches)
- All training video recordings
- FAQ document
- Definition Alignment Document (final version)
- **Maintenance Schedule** (for Single Project engagements)

**For Single Project engagements:** Record a video walkthrough of the maintenance schedule. Make sure the customer's Marketing Ops lead understands what to check monthly, quarterly, and when to re-engage.

**Output:** Customer owns the process. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved (field mapping doc, tech spec, test results, training recordings)
- [ ] Handoff documentation delivered to customer
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized

#### Internal Debrief (Optional but Recommended)

- What went well? (e.g., sample data analysis in pre-kickoff saved time, first live event ran clean)
- What would we do differently? (e.g., needed more time for campaign hierarchy design, should have audited badge scan data separately)
- Any learnings to feed back into SOPs? (e.g., specific event platform quirks, new dedup edge case)

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell > Downsell > Retry    |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (ongoing event ops + new event platform integrations)
   | if no
2. Downsell: Lead scoring model (natural next project after intake is standardized)
             OR Event attribution/ROI reporting (if not fully covered in this scope)
   | if yes
3. Retry retainer at end of next project cycle
```

**Script:**

> "Now that your event lead intake process is standardized and running, there are two ways we can continue. Option 1: We handle ongoing event ops optimization -- new platform integrations, quarterly process reviews, report enhancements. Option 2: If there's a specific next project, like implementing lead scoring on your event leads or building deeper event attribution, we can scope that out. Which sounds more relevant?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On \[date ~quarter out\], we'll review how the event intake process is performing after a full quarter of events and see if any adjustments are needed."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                                    |
| ------------------- | --------------------------------------------------------------- |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks                |
| 2. Review metrics   | Pull import SLA compliance, duplicate rates, conversion funnel   |
| 3. Decide ownership | Can Architect handle this, or need SME?                         |
| 4. Prep materials   | If SME needed, brief them. If Architect, prep talking points.   |

**At the refinement check-in:**

- Review event lead conversion rates vs pre-project baseline
- Check import SLA compliance trend
- Identify any new event platforms or process changes needed
- If minor: Architect handles adjustments
- If major: Scope new project (event platform migration, lead scoring, etc.)

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- Definition Alignment Document (event lead terminology and source taxonomy)
- Field Mapping Template (event platform fields to CRM/MAP schema)
- Lead Source Taxonomy (picklist values, sub-source categories, campaign naming convention)
- Assignment Rules Matrix (routing logic for all event lead scenarios)

**Technical Deliverables:**

- Import Template Package (standardized CSV templates with validation rules per event platform)
- MAP Lead Processing Workflows (data standardization, enrichment, deduplication, status assignment)
- CRM Assignment/Routing Rules (territory-based, round-robin, hot lead alerts, fallback logic)
- Event Lead Dashboard (intake volume, conversion funnel, speed-to-lead, data quality scorecard, ROI summary)

**Documentation Package:**

- Step-by-step process guide (event close through CRM assignment)
- Training video recordings (event marketing track, sales track, technical admin track)
- Troubleshooting guide (import errors, dedup conflicts, routing issues)
- FAQ document
- Maintenance Schedule (monthly/quarterly/annual tasks)
- Definition Alignment Document (final version)

---

## Appendix

### Roles

| Role | What They Do |
|---|---|
| **Architect** | Owns the customer relationship, leads strategy, creates specs, does enablement, owns account post-delivery |
| **Engineer** | CRM build, automation, dashboards (Phase 2) |
| **SME** | Project/implementation team brought in for project-specific work |

### What Each Phase Produces

| Phase                    | Output                                                                 | Gate Criteria                                                                  |
| ------------------------ | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **Phase 1: Strategy**    | Approved field mapping, lead source taxonomy, routing rules, report scope | Marketing Ops and Sales Leadership sign off on data schema and process design  |
| **Phase 2: Engineering** | Built import templates, workflows, routing, dashboards -- tested end-to-end | All technical tests pass, customer UAT approved                                |
| **Phase 3: Enablement**  | Trained event marketing + sales teams, first live event validated       | All training delivered, hypercare complete, team operates independently        |
| **Phase 4: Handoff**     | Customer owns process, maintenance schedule in place, project archived  | Internal/external handoffs complete, documentation delivered, project closed   |

### How to Adapt Per Project Type

This project is **engineering-heavy** with a profile of:

| Component         | Weight  | Notes                                         |
| ----------------- | ------- | --------------------------------------------- |
| Strategy          | 15-20%  | Data requirements are concrete; fast alignment |
| Engineering       | 50-60%  | Bulk of work: templates, workflows, routing, reports |
| Enablement        | 15-20%  | Two audience tracks, validated with live event |
| Handoff           | 10-15%  | Documentation + first event cycle validation   |

**Adaptation rules:**
- Strategy compresses to 2-3 meetings. Expands only if campaign hierarchy needs full redesign.
- Engineering is the longest phase. Plan 1-2 weeks for build + testing.
- Enablement requires coordination with a real upcoming event. Schedule training before the event.
- Handoff includes the first live event validation as proof the system works.

### Phase 1: Key Principles

**Why Phase 1 Matters for Event Lead Intake**

94% of marketers believe their company fails to convert event leads into opportunities [7]. The primary reason is not bad events -- it is a broken handoff from event capture to sales follow-up. Phase 1 ensures we solve the right problem: getting the data schema, routing, and SLAs right before building automation.

**How we create value in Strategy:**
1. **We audit first.** Most clients know their event lead process is broken but cannot articulate where. We analyze their sample lists and find the specific data quality issues, quantify duplicate rates, and document the time lag from event to CRM entry.
2. **We bring a data schema.** We do not ask "what fields do you want?" We present a proven field mapping template and the customer confirms and adjusts.
3. **We standardize naming.** Campaign naming conventions seem trivial until you try to do event ROI reporting without them. We propose the convention (e.g., EVT-2025-Dreamforce-Booth) and show why it matters for downstream attribution.
4. **We define routing before building.** Assignment rules are the #1 source of post-launch issues. We force the conversation about territory overlaps, existing customer handling, and hot lead criteria before touching the CRM.

### Phase 2: Key Principles

**Build order matters:** Build fields first, then templates, then workflows, then routing, then reports. Each workstream depends on the previous one. Do not build reports until routing is confirmed working.

**Test with dirty data:** Real event lists have inconsistent company names, missing fields, and duplicates. If you test with perfect data, the first real import will break.

### Phase 3: Key Principles

**Training Prep:** The process guide matters more than slide decks. Event marketing teams need a checklist they can follow every time.

**Training Sessions:** Run the training in the actual CRM/MAP, not in slides. Import a real (or realistic) test list during training so attendees see the full flow.

**Hypercare:** Time the hypercare period to cover the next scheduled event. If the next event is 6 weeks out, start hypercare when the event happens -- not immediately after training.

### Phase 4: Key Principles

**Why Maintenance Matters:** Event lead intake processes degrade faster than most other RevOps systems because the input sources change constantly. New events use new platforms, event teams rotate, and CRM territories shift quarterly. Without explicit monthly checks, the process that worked for Q1 breaks silently for Q2.

**External Handoff best practice:** Include performance data from the first live event processed through the new system. Example: "Before this project, leads from your last trade show took 7 days to reach the CRM and had a 23% duplicate rate. With the new process, leads were in CRM within 6 hours with a 3% duplicate rate."

---

## References

[1] [SalesIntel - How Bad CRM Data Can Impact Your Sales Team](https://salesintel.io/blog/how-and-why-bad-crm-data-is-hurting-your-sales-team-performance-and-b2b-lead-generation/)

[2] [SalesIntel - How B2B Companies Can Improve CRM Data](https://salesintel.io/blog/improve-crm-data-quality/)

[3] [Kixie - Speed to Lead Response Time Statistics](https://www.kixie.com/sales-blog/speed-to-lead-response-time-statistics-that-drive-conversions/)

[4] [Chili Piper - Speed to Lead Statistics](https://www.chilipiper.com/article/speed-to-lead-statistics)

[5] [Rep.ai - Lead Response Time Statistics 2024](https://rep.ai/blog/lead-response)

[6] [Momencio - Event Lead Conversion Data and Analysis](https://www.momencio.com/event-lead-conversion-data-and-analysis/)

[7] [Splash - Event Marketing Statistics](https://splashthat.com/blog/event-marketing-statistics)

[8] [Cvent - Trade Show Statistics 2025](https://www.cvent.com/en/blog/events/trade-show-statistics)

[9] [Landbase - Duplicate Record Rate Statistics](https://www.landbase.com/blog/duplicate-record-rate-statistics)
