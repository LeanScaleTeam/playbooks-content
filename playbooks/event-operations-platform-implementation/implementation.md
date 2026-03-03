# Event Operations Platform Implementation — Implementation

## Project One-Pager

### Event Operations Platform Implementation One-Pager

#### Project Type

- Category: Technical
- Primary Deliverable: Fully configured event management platform integrated with CRM and MAP, with automated registration tracking, attendance sync, and event attribution reporting

##### Phase Relevance

| Phase          | Applies? | Weight | Notes                                                    |
| -------------- | -------- | ------ | -------------------------------------------------------- |
| 1. Strategy    | Yes      | Medium | Requirements gathering, platform evaluation, integration design |
| 2. Engineering | Yes      | Heavy  | Platform configuration, CRM/MAP integration, registration forms, dashboards |
| 3. Enablement  | Yes      | Medium | Training Marketing Ops and Event teams on platform usage |
| 4. Handoff     | Yes      | Medium | Documentation package, troubleshooting guide, maintenance schedule |

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────>│ 2. ENGINEER  │────>│3. ENABLEMENT │────>│  4. HANDOFF  │
  │    Medium    │     │    Heavy     │     │    Medium    │     │    Medium    │
  │ 1a>1b>1c>1d │     │ 2a>2b>2c>2d │     │ 3a>3b>3c>3d │     │ 4a>4b>4c>4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   Requirements &       Platform config     Team training &       Docs, support
   platform eval        CRM/MAP integrate   pilot event run       & ownership
```

**This project's flow:**
- Full 4-phase. Medium strategy (requirements + platform selection), heavy engineering (platform config + CRM/MAP integration + forms + dashboards), medium enablement (training + pilot event), medium handoff.
- Some customers skip Phase 1 if platform is already selected and procured. In that case, Phase 1 focuses only on integration architecture and field mapping decisions.

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Watch intro video on event platform integration architecture
- [ ] Complete event intake form (event types, frequency, current tools, pain points)
- [ ] Provide CRM and MAP admin credentials or confirm access
- [ ] Share brand assets (logos, colors, fonts, email sender domains)
- [ ] Provide event calendar/roadmap for next 6-12 months

##### Track B: Architect Prep
- [ ] Audit current CRM campaign structure and existing event data
- [ ] Review MAP program templates and email configuration
- [ ] Research client's current event platform (if any) and document gaps
- [ ] Draft integration architecture diagram (event platform &lt;> CRM &lt;> MAP)
- [ ] Prepare requirements matrix template pre-filled with common B2B SaaS event needs

#### Refinement Loop (1b > 1c > 1d)

| Meeting      | Sub-Phase | Focus                                          | Stakeholder                     | Output                          |
| ------------ | --------- | ---------------------------------------------- | ------------------------------- | ------------------------------- |
| Kickoff      | 1b        | Present requirements matrix, validate event types, confirm integration approach | VP Marketing, Marketing Ops, RevOps | Validated requirements, platform shortlist |
| Refinement 1 | 1c        | Platform demos review, integration design walkthrough | Marketing Ops, IT/Security      | Selected platform, approved architecture |
| Refinement 2 | 1c        | Field mapping review, registration form design, consent language approval | Marketing Ops, Legal (if GDPR applies) | Approved field mappings and form design |
| Sign-Off     | 1d        | Final integration architecture and rollout plan approval | VP Marketing, RevOps            | Signed-off strategic package    |

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held
- [ ] 1c. Refinement loop complete (requirements > platform selected > architecture approved)
- [ ] 1d. Strategic sign-off obtained

##### Phase 2: Engineering
- [ ] 2a. Tech spec created (field mappings, workflow logic, integration specs)
- [ ] 2b. Engineering handoff meeting held
- [ ] 2c. Build complete (platform config, CRM integration, MAP integration, forms, dashboards)
- [ ] 2d. QA/Test + customer sign-off (pilot event validation)

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped (video walkthrough scripts, quick-reference guides)
- [ ] 3b. Training sessions delivered (Marketing Ops + Event team)
- [ ] 3c. Hypercare period complete (2-week post-launch support)
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff (SME > Architect) complete
- [ ] 4c. External handoff complete
- [ ] 4d. Project closed and archived

#### Document Types

##### Working Documents (iterate together)

| Document                      | Purpose                                    | When Complete                              |
| ----------------------------- | ------------------------------------------ | ------------------------------------------ |
| Event Requirements Matrix     | Catalog event types mapped to features     | All event types scored against platform capabilities |
| Platform Evaluation Scorecard | Compare platform options against criteria  | Top platform selected with stakeholder buy-in |
| Integration Architecture Doc  | Map data flows between platform, CRM, MAP  | All sync points documented and approved    |
| Field Mapping Table           | Map registration fields to CRM/MAP fields  | All fields mapped with duplicate handling rules |
| Registration Form Wireframe   | Design form layout and field sequence      | Form approved by Marketing Ops and Legal   |

##### Deliverables (polished outputs)

| Deliverable                  | Created From                 | Customer Uses For                           |
| ---------------------------- | ---------------------------- | ------------------------------------------- |
| Integration Architecture Diagram | Integration Architecture Doc | Internal alignment, IT review               |
| Platform Configuration Runbook | Build documentation          | Day-to-day event creation reference         |
| Registration & Attribution Report Templates | Dashboard configuration      | Post-event performance reporting            |

#### Enablement Details

##### Training Types

| Type       | Audience                          | Focus                                                 | Duration |
| ---------- | --------------------------------- | ----------------------------------------------------- | -------- |
| Leadership | VP Marketing, Director Mktg Ops   | Interpreting event attribution reports, ROI dashboards | 30 min   |
| Technical  | Marketing Ops, Event Team         | Event creation, registration form setup, email config, troubleshooting sync issues | 60-90 min |

##### Hypercare
- Applies: Yes
- Duration: 2 weeks (covers at least one live event cycle)
- Office Hours: Yes — weekly 30-min slot for sync questions and troubleshooting

##### Training Assets to Create
- [ ] Video walkthrough: Event creation walkthrough (platform setup to go-live)
- [ ] Video walkthrough: Dashboard and reporting navigation
- [ ] Doc: Field mapping reference (registration fields > CRM/MAP fields)
- [ ] Doc: Quick-reference guide for event creation workflow
- [ ] Doc: Troubleshooting common sync failures

#### Handoff & Retention

##### Internal Handoff (SME > Architect)
- Key context for Architect: Integration architecture, which sync points are most fragile, platform admin credentials location
- Escalation trigger: Any changes to CRM field structure, new event types requiring different registration flows, integration sync failures not covered in troubleshooting guide

##### External Handoff
- Final meeting agenda: Walk through documentation package, demo event creation workflow, review maintenance schedule, answer questions
- Documentation package: Integration architecture, field mappings, platform runbook, training video walkthroughs, troubleshooting guide, maintenance schedule

##### Maintenance Schedule
- Monthly: Registration sync health check, dashboard accuracy review
- Quarterly: Platform feature review, integration audit, form conversion analysis
- Who owns: Single project = customer owns | Dedicated = Architect owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services (ongoing event ops support) > if no > Downsell: Another project (e.g., event attribution reporting, lead scoring refinement) > Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~1 quarter after go-live
- Internal prep trigger: 2 weeks before
- Decision: Architect handles / SME needed

#### Key Assets

| Asset                         | When Used         |
| ----------------------------- | ----------------- |
| Event Requirements Matrix     | Phase 1: Strategy |
| Platform Evaluation Scorecard | Phase 1: Strategy |
| Integration Architecture Doc  | Phase 1-2         |
| Field Mapping Table           | Phase 2: Build    |
| Platform Configuration Runbook| Phase 2-4         |
| Troubleshooting Guide         | Phase 4: Handoff  |

#### Definition Alignment Terms

| Term                   | Typical Definition                                                                 |
| ---------------------- | ---------------------------------------------------------------------------------- |
| Registration           | A form submission by a prospect or contact indicating intent to attend an event    |
| Attendance             | Confirmed participation in an event (virtual: joined session; in-person: checked in) |
| Campaign Member Status | CRM field tracking a contact's progression through an event (Registered > Attended > No Show) |
| Event Attribution      | Connecting pipeline or revenue creation to a specific event touchpoint in CRM      |
| Bi-directional Sync    | Data flowing both ways between event platform and CRM/MAP (registration out, attendance back) |
| Progressive Profiling  | Showing different form fields to known contacts to gather incremental data without repeating questions |
| Engagement Score       | Platform-calculated metric based on attendee behavior (session duration, poll responses, questions asked) |

#### Common Gotchas
- Duplicate records created when existing CRM contacts register for events — configure email-based duplicate matching rules before go-live
- Batch sync delays cause Sales to miss follow-up windows — configure real-time or near-real-time sync, not batch (nightly) sync
- Attendance data fails to sync back after virtual events — verify bi-directional sync is configured and test full lifecycle before launch
- Registration forms with 10+ fields cause 60%+ abandonment [1] — keep to 5-7 fields maximum for first-time registrants
- GDPR consent checkboxes missing from registration forms — confirm consent language with Legal during Phase 1
- UTM parameters not captured on registration forms — add hidden fields for UTM tracking during form design
- MAP program membership not updating on registration — test end-to-end flow from form submission to MAP program entry

#### Methodology Options

| Option                    | When to Use                                                  | Complexity |
| ------------------------- | ------------------------------------------------------------ | ---------- |
| Native Integration        | Event platform has built-in CRM/MAP connectors (Goldcast > Salesforce, Bizzabo > HubSpot) | Low        |
| API-Based Integration     | No native connector available, or custom data requirements beyond native capabilities | Medium     |
| iPaaS Middleware (Workato/Zapier) | Multiple systems to connect, complex data transformation needed, or when native connectors lack specific field mappings | High       |

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on event platform requirements, integration architecture, and field mapping design.
>
> **Output:** Requirements Matrix + Integration Architecture Document + Field Mapping Table (signed off by stakeholders).

### 1a. Pre-Kickoff

> Two parallel tracks run before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                   | Format             |
| ----------------------------- | --------------------------------------------------------- | ------------------ |
| Intro video                   | Explain the event platform integration project and expected outcomes | Video walkthrough (5-10 min) |
| Definition Alignment Document | Get stakeholder sign-off on key event ops terms           | Google Doc         |
| Event intake form             | Catalog event types, frequency, pain points, current tools | Google Form        |

**Intake form captures:**
- Event types run (webinars, virtual summits, hybrid, in-person conferences, executive dinners)
- Event frequency (monthly, quarterly, ad-hoc)
- Current event tools and pain points
- CRM and MAP details (version, admin access status)
- Brand assets availability
- Compliance requirements (GDPR, CCPA, data residency)
- Event calendar for next 6-12 months

**Completion tracking:** Marketing Ops owner follows up. Do not cancel kickoff if incomplete, but push hard after.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                       | Output                              |
| ---- | ------------------------------------------------------------ | ----------------------------------- |
| 1    | Review intake form responses and audit CRM campaign structure | Understanding of current event tracking |
| 2    | Map current state: how event data flows today (manual exports, CSV uploads, etc.) | Current state documentation         |
| 3    | Design future state: automated bi-directional sync architecture | Integration architecture draft      |
| 4    | Pre-fill requirements matrix with common B2B event platform features | Requirements matrix v0              |
| 5    | Research 2-3 event platforms matching stated requirements    | Platform shortlist with pros/cons   |

**Critical:** Mark everything as ASSUMED. The kickoff call validates.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building anything.

| Term                   | Our Definition                                                                 | Internally Approved? |
| ---------------------- | ------------------------------------------------------------------------------ | -------------------- |
| Registration           | A form submission indicating intent to attend; creates/updates CRM record      | [ ] Yes / [ ] No     |
| Attendance             | Confirmed participation (virtual: joined session; in-person: badge scan)       | [ ] Yes / [ ] No     |
| Campaign Member Status | CRM progression: Invited > Registered > Attended > No Show                     | [ ] Yes / [ ] No     |
| Event-Sourced Pipeline | Pipeline where the first meaningful touchpoint was an event registration or attendance | [ ] Yes / [ ] No     |
| Event-Influenced Pipeline | Pipeline where an event touchpoint occurred anywhere in the buyer journey      | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your leadership team. Check "Yes" when approved. We cannot proceed until all terms are aligned.

---

### 1b. Kickoff Call

> **Purpose:** Present v0 requirements matrix and draft integration architecture. Customer reacts and corrects, not creates from scratch.

#### Agenda (60-90 min)

| Time  | Topic                    | What Happens                                            |
| ----- | ------------------------ | ------------------------------------------------------- |
| 0-15  | Walk through requirements matrix | "Here's what we built from your intake form"            |
| 15-30 | Validate event types     | Confirm which event types need platform support         |
| 30-45 | Integration architecture | Present draft data flow: event platform > CRM > MAP    |
| 45-55 | Definition alignment     | Review Definition Alignment Doc, resolve ambiguities    |
| 55-70 | Platform shortlist       | Present 2-3 platform options, schedule demos            |
| 70-80 | Gap identification       | What data is missing, who owns it, next steps           |
| 80-90 | Homework assignments     | Schedule demos, collect brand assets, confirm admin access |

#### What We Bring

- Requirements matrix v0 (pre-filled from intake + CRM audit)
- Draft integration architecture diagram
- Platform shortlist with feature comparison
- Definition Alignment Document (pre-filled with our recommendations)

#### What We Leave With

- Validated event types and feature requirements
- Corrections to integration architecture
- Demo schedule for top 2-3 platforms
- Clear homework assignments (brand assets, admin access, Legal review for consent)

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Evaluate platforms, finalize integration architecture, and get field mapping approval.

#### The Pattern

```
Kickoff Call (validate requirements)
    |
Platform demos (2-3 platforms with stakeholders)
    |
Meeting 2 (platform selection, integration architecture review)
    |
Meeting 3 (field mapping review, form design, consent approval)
    |
Final Review > Sign-off
```

#### Potential Meeting Types

| Meeting Type         | Focus                                              | Stakeholder                  |
| -------------------- | -------------------------------------------------- | ---------------------------- |
| Platform Demo        | Evaluate platform features against requirements    | VP Marketing, Marketing Ops  |
| Architecture Review  | Validate CRM/MAP integration design                | Marketing Ops, RevOps, IT    |
| Field Mapping Review | Approve registration > CRM field mappings          | Marketing Ops, Sales Ops     |
| Compliance Review    | Approve consent language and data handling          | Legal, Marketing Ops         |
| Final Review         | Full walkthrough and sign-off                      | All stakeholders             |

#### Typical Timeline

| Milestone                   | Timing                               |
| --------------------------- | ------------------------------------ |
| Pre-kickoff prep            | 2-3 days                             |
| Kickoff call                | Day 1 of engagement                  |
| Platform demos              | Week 1-2 (depends on vendor availability) |
| Architecture + field mapping| Week 2-3                             |
| Final review + sign-off     | Week 3-4                             |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything before proceeding to build.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by stakeholders
- [ ] Event platform selected and procurement initiated
- [ ] Integration architecture approved (event platform > CRM > MAP data flows)
- [ ] Field mapping table approved (registration fields > CRM Lead/Contact fields)
- [ ] Campaign Member status values agreed (Invited, Registered, Attended, No Show)
- [ ] Registration form design approved (fields, consent language, UTM tracking)
- [ ] Duplicate handling rules defined (create new vs. update existing, email as match key)
- [ ] Customer understands what we are building
- [ ] No blockers for engineering

#### Decision Point

- **Proceed to Engineering** — Customer wants system built (standard path)
- **Pause for procurement** — Platform not yet procured, Engineering waits for vendor contract

---

## Phase 2: Engineering

> **Goal:** Configure event platform, build CRM/MAP integrations, create registration forms and dashboards, and validate with a pilot event.
>
> **Output:** Fully configured event platform integrated with CRM and MAP, tested end-to-end with pilot event.

| Project Type | Engineering Weight | This Project                                           |
| ------------ | ------------------ | ------------------------------------------------------ |
| Technical-heavy | Heavy (70-80%) | Platform config + CRM integration + MAP integration + forms + dashboards |

### Sub-Phases

```
2a Tech Spec > 2b Engineering Handoff > 2c Build > 2d Test (Pilot Event)
```

---

### 2a. Tech Spec

> **Purpose:** Translate strategic package into technical specifications for platform configuration and integration build.

**Input:** Signed-off strategic package (requirements matrix, integration architecture, field mappings)

**Output:** Draft tech spec containing:

- Event platform account configuration (user roles, branding settings, default timezone)
- CRM integration specifications:
  - Connection method (native connector, API, middleware)
  - Field mapping: registration form field > CRM Lead/Contact field (exact API names)
  - Duplicate handling logic (match on email, update existing vs. create new)
  - Campaign Member status mapping (platform status > CRM Campaign Member status)
- MAP integration specifications:
  - Program template structure (one per event type)
  - Trigger logic (registration > program membership, attendance > follow-up sequence)
  - Email sequence specs (confirmation, reminder, post-event follow-up by attendance status)
- Registration form specifications:
  - Field sequence and validation rules
  - Hidden fields (UTM source, UTM medium, UTM campaign, lead source)
  - Consent checkbox configuration (opt-in language, GDPR compliance)
  - Progressive profiling rules (if platform supports)
- Dashboard specifications:
  - Registration velocity report (daily/weekly sign-ups by event)
  - Attendance tracking report (attendance rate, engagement scores)
  - Event attribution report (pipeline sourced/influenced by event)

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs with engineer before building.

**Agenda (30-45 min):**

| Time  | Topic              | What Happens                                            |
| ----- | ------------------ | ------------------------------------------------------- |
| 0-15  | Walk through specs | Architect explains integration architecture + tech spec |
| 15-30 | Engineer questions | Clarify API limits, sync frequency, error handling      |
| 30-45 | Refine and approve | Adjust specs, confirm build sequence                    |

**What Architect brings:**

- Strategic package (for context on why these decisions were made)
- Draft tech spec (from 2a)
- Questions list (any ambiguities from field mapping or sync logic)

**What engineer leaves with:**

- Approved tech spec with exact CRM API field names
- Clear build sequence: (1) platform config > (2) CRM integration > (3) MAP integration > (4) forms > (5) dashboards
- Known risks (API rate limits, sync frequency constraints, vendor-specific quirks)

---

### 2c. Build (Configure)

> **Purpose:** Configure the event platform, build integrations, create forms and dashboards.

**Input:** Approved tech spec from 2b

**Build sequence:**

**Component 1: Event Platform Account Configuration**
- [ ] Create admin account and configure user roles (Admin, Event Manager, Viewer)
- [ ] Upload brand assets (logos, colors, fonts) to platform theme settings
- [ ] Set organizational defaults (timezone, date format, sender email domain)
- [ ] Create branded email templates (registration confirmation, event reminder, post-event follow-up)
- [ ] Configure default registration form fields and consent language

**Component 2: CRM Integration (Salesforce/HubSpot)**
- [ ] Connect event platform to CRM via native integration or API
- [ ] Map registration form fields to CRM Lead/Contact fields per tech spec
- [ ] Configure duplicate handling rules (email as primary match key)
- [ ] Set up Campaign creation rules (one Campaign per event)
- [ ] Configure Campaign Member status values (Invited > Registered > Attended > No Show)
- [ ] Configure real-time sync (not batch) — registration-to-CRM record creation target under 5 minutes [2]
- [ ] Set up sync failure alerts (email notification to Marketing Ops on failed syncs)

**Component 3: MAP Integration (Marketo/HubSpot Marketing)**
- [ ] Connect event platform to MAP via native connector or API
- [ ] Configure bi-directional sync for registration and attendance data
- [ ] Create program templates for each event type (webinar, virtual summit, in-person)
- [ ] Build registration confirmation email sequence
- [ ] Build reminder email sequence (7 days, 1 day, 1 hour before event)
- [ ] Build attendance-based follow-up sequences (attended vs. no-show, differentiated content)
- [ ] Test end-to-end flow from registration to email delivery

**Component 4: Registration Forms**
- [ ] Build primary registration form template with essential fields only (5-7 fields max)
- [ ] Add hidden fields for UTM tracking (source, medium, campaign, content, term)
- [ ] Configure consent checkboxes (GDPR opt-in, email marketing opt-in)
- [ ] Set up progressive profiling for returning contacts (if platform supports)
- [ ] Create custom fields for event-specific segmentation (e.g., job function, company size)
- [ ] Test form submission and validate data flows to CRM and MAP

**Component 5: Dashboards & Reporting**
- [ ] Configure event platform native registration analytics
- [ ] Build CRM report: registrants by event, source, and segment
- [ ] Build registration velocity dashboard (daily/weekly sign-ups per event)
- [ ] Set up registration milestone alerts (e.g., 50%, 75%, 100% of target capacity)
- [ ] Build audience segmentation views (by title, company size, industry)
- [ ] Configure attendance tracking (virtual: join time, duration, engagement score; in-person: badge scan)
- [ ] Map attendance status back to CRM Campaign Member records
- [ ] Configure lead scoring rules for event attendance in CRM/MAP
- [ ] Build post-event attendance report template
- [ ] Set up multi-touch attribution credits for event touchpoints

---

### 2d. QA / Test + Sign-Off (Pilot Event)

> **Purpose:** Run a full pilot event to validate end-to-end process before live rollout.

**Two types of testing:**

| Type              | Who      | Purpose                                                    |
| ----------------- | -------- | ---------------------------------------------------------- |
| Technical Testing | Our team | Verify integrations fire, data syncs, emails trigger       |
| Customer Testing  | Customer | Verify it meets their needs for a real event scenario      |

**Technical testing checklist:**

- [ ] Create test event in platform with full configuration
- [ ] Submit 5-10 test registrations with varied data (new leads, existing contacts, known duplicates)
- [ ] Verify registrations appear in CRM within 5 minutes (Campaign Members created with correct status)
- [ ] Verify MAP program membership updated (registrants added to correct program)
- [ ] Confirm registration confirmation emails fire correctly
- [ ] Confirm reminder emails trigger at correct intervals
- [ ] Run test virtual event — verify attendance tracking captures join time, duration, engagement
- [ ] Verify attendance status syncs back to CRM Campaign Member records after event
- [ ] Confirm follow-up email sequences trigger based on attendance status (attended vs. no-show)
- [ ] Verify lead scoring rules update based on attendance
- [ ] Verify dashboards populate with accurate data
- [ ] Verify duplicate handling works correctly (existing contacts updated, not duplicated)
- [ ] Test UTM parameter capture on registration form
- [ ] Verify attribution data flows to CRM for pipeline reporting

**Customer testing:**

- Walk customer through the pilot event results
- Have Marketing Ops create a test event using the quick-reference guide
- Verify they can run event creation workflow independently
- Capture feedback, fix issues

**Engineering sign-off checkpoint:**

- [ ] Built system matches tech spec
- [ ] All technical tests passing
- [ ] Registration-to-CRM sync time under 5 minutes confirmed
- [ ] Attendance data syncs back to CRM within 15 minutes of event end
- [ ] Duplicate handling rules working correctly
- [ ] Dashboards reporting accurately
- [ ] Customer has tested and approved
- [ ] Ready for enablement

**Decision point:**

- **Proceed to Enablement** — System is built and pilot event validated
- **Loop back to Build** — Issues found during pilot, needs fixes

---

## Phase 3: Enablement

> **Goal:** Customer team can create events, manage registrations, and interpret reports independently.
>
> **Output:** Trained team with documentation, stabilized system through at least one live event.

### Sub-Phases

```
3a Training Prep > 3b Training Sessions > 3c Hypercare > 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from strategic documentation, tech specs, and platform configuration.

**Input:** Strategic package + tech specs + configured platform

**Output:** Training package containing:

- Video walkthrough script: Event creation walkthrough (platform setup to go-live, 10-15 min)
- Video walkthrough script: Dashboard and reporting navigation (5-10 min)
- Written guide: Event creation quick-reference (step-by-step for creating a new event)
- Written guide: Field mapping reference (registration fields > CRM/MAP fields)
- Written guide: Troubleshooting common issues (sync failures, duplicate records, email delivery problems)
- FAQ draft: Answers to common questions based on similar project deployments

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to customer team so they can operate the event platform independently.

**Two types of training:**

| Type                | Audience                       | Focus                                                                       |
| ------------------- | ------------------------------ | --------------------------------------------------------------------------- |
| Leadership training | VP Marketing, Director Mktg Ops | How to interpret event attribution reports, ROI dashboards, registration metrics |
| Technical training  | Marketing Ops, Event Team       | Event creation, registration form setup, email configuration, troubleshooting |

**Technical training session (60-90 min):**

1. Event creation workflow: walk through creating a new event from scratch
2. Registration form configuration: fields, consent, UTM tracking
3. Email sequence setup: confirmation, reminders, post-event follow-ups
4. Dashboard usage: registration velocity, attendance tracking, attribution
5. Troubleshooting: sync failure alerts, duplicate handling, common errors
6. Q&A and hands-on practice

**Leadership training session (30 min):**

1. Event attribution dashboard walkthrough
2. How to read registration-to-pipeline reports
3. Where to find event ROI data for board reporting
4. When to escalate vs. handle internally

**Training delivery:**

1. Schedule sessions with appropriate stakeholders
2. Deliver training live and record for future reference
3. Record video walkthroughs for specific workflows
4. Answer questions, note gaps for FAQ updates

**Output:**

- Trained stakeholders who can operate independently
- Video walkthrough recordings for future onboarding
- Updated FAQ based on questions raised

---

### 3c. Hypercare

> **Purpose:** Intensive post-launch support covering the first live event cycle.

**Duration:** 2 weeks (should cover at least one live event from registration open to post-event follow-up)

**What happens:**

- Quick response to sync issues, email delivery problems, or form errors during first live event
- Office hours: weekly 30-min slot for Marketing Ops to bring questions
- Monitor registration-to-CRM sync times and flag delays
- Monitor duplicate record creation rate and adjust matching rules if needed
- Bug triage and fixes for any integration issues
- Verify attendance data flows correctly after first live event

**When to extend:** If first live event reveals integration issues that require rebuilding sync logic or field mappings, extend hypercare to cover the fix + one additional event cycle.

**Output:** Stabilized system with at least one successful live event completed end-to-end

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm customer can operate the event platform independently.

**Validation checkpoint:**

- [ ] All training sessions delivered
- [ ] Training recordings and documentation provided
- [ ] At least one live event completed successfully (registration > attendance > CRM sync > follow-up emails)
- [ ] Hypercare period complete
- [ ] No critical sync or integration issues outstanding
- [ ] Customer team can create events, manage registrations, and pull reports without support
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** — Customer is enabled, system is stable
- **Extend Hypercare** — First live event had issues, needs more support time

---

## Phase 4: Handoff

> **Goal:** Clean project close with maintenance plan established and retention/expansion path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the system, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule > 4b Internal Handoff > 4c External Handoff > 4d Project Close
                          (SME > Architect)            (> Customer)       (Archive + Debrief)
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At                                                                    |
| ----------------------------- | -------------------- | -------------------------------------------------------------------------------- |
| **Single Project**            | Customer owns        | 4c (External Handoff) — customer receives maintenance schedule and runs it themselves |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) — Architect receives maintenance schedule and runs it for customer |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention after the project is complete.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task                   | What to Check                                      | Red Flag Threshold                                  |
| ------------------------------ | -------------------------------------------------- | --------------------------------------------------- |
| Registration Sync Health Check | Verify registration > CRM sync is working and &lt;5 min latency | Any sync failure in past 30 days; latency >15 min  |
| Dashboard Accuracy Review      | Spot-check 5 recent events for correct registration/attendance counts in CRM | >5% discrepancy between platform and CRM counts    |
| Email Delivery Audit           | Check confirmation and reminder email delivery rates | Delivery rate &lt;95% or bounce rate >3%               |

**Quarterly Tasks:**

| Quarterly Task             | What to Review                                    | Action if Off-Track                                  |
| -------------------------- | ------------------------------------------------- | ---------------------------------------------------- |
| Platform Feature Review    | Check for new platform features or connector updates | Evaluate and implement relevant improvements        |
| Integration Audit          | Verify all sync points operational, check API version compatibility | Re-test integrations, update connectors if deprecated |
| Form Conversion Analysis   | Review registration form completion rates per event type | Optimize form fields if abandonment >40%            |
| Data Quality Spot Check    | Sample 20 recent event registrations for duplicate or missing data | Tighten matching rules or add validation            |

**After First Business Cycle (30-60 days post-launch):**

- Registration-to-Pipeline Validation: Did event registrations generate the expected pipeline in CRM?
- Attribution Accuracy Check: Is event-sourced pipeline being credited correctly?
- Key Question: Are we accurately tracking event ROI? If not, is it a data issue (sync) or a process issue (attribution model)?

**Refinement Triggers (when to re-engage):**

| Trigger                           | Threshold                                    | Response                                              |
| --------------------------------- | -------------------------------------------- | ----------------------------------------------------- |
| Sync failure rate                 | >5% of registrations failing to sync in a month | Re-engage SME to diagnose and fix integration         |
| Duplicate record creation rate    | >10% of event registrations creating duplicates | Tighten matching rules, consider deduplication tool   |
| Form abandonment rate             | >50% across multiple events                  | Redesign form, reduce field count, add progressive profiling |
| Attribution data gaps             | >20% of event-sourced pipeline unattributed  | Audit Campaign Member status logic and attribution model |

**Every 6-12 Months:**

- Full Integration Health Check: Re-test all sync points end-to-end with test registrations
- Platform Contract Review: Evaluate usage vs. licensing, negotiate renewal if applicable
- Event Program Audit: Assess whether event types and platform capabilities still match organizational needs

---

### 4b. Internal Handoff (SME > Architect)

> **Purpose:** Transfer context so Architect can manage ongoing relationship.

**What the Architect needs to know:**

- Integration architecture overview (what connects to what, how data flows)
- Platform admin access location (credentials, SSO, etc.)
- Common issues and resolutions (sync delays, duplicate records, email delivery)
- When to escalate back to SME
- **Maintenance schedule** (if Dedicated engagement — Architect runs this)

**Escalation guidelines:**

| Issue Type                                   | Who Handles                            | Example                                         |
| -------------------------------------------- | -------------------------------------- | ------------------------------------------------ |
| New event creation questions, minor form changes | Architect                          | "How do I add a new field to the registration form?" |
| Dashboard filter changes, report adjustments | Architect                              | "Can we add a new segment view?"                 |
| Integration sync failures, API errors        | SME                                    | "Registrations stopped syncing to CRM"           |
| New event type requiring different workflow   | SME                                    | "We want to add hybrid events with in-person check-in" |
| CRM field structure changes affecting sync   | SME                                    | "We renamed the Campaign Member status values"   |

**For Dedicated engagements:** Architect receives the maintenance schedule (4a) and becomes responsible for executing it. SME walks Architect through each maintenance task.

---

### 4c. External Handoff

> **Purpose:** Formal project completion with customer.

**Final project meeting:**

- Review what was delivered (configured platform, integrations, forms, dashboards)
- Walk through documentation package
- Demo: customer creates a new event using the quick-reference guide (they do it, we observe)
- Confirm nothing outstanding
- Answer final questions
- Make it explicit: "Project complete"
- **For Single Project engagements:** Hand over the maintenance schedule and walk the customer through it

**Documentation package:**

- Integration architecture diagram (event platform > CRM > MAP data flows)
- Field mapping reference (registration fields > CRM/MAP field API names)
- Platform configuration runbook (branding, defaults, templates)
- Event creation quick-reference guide
- All training video walkthrough recordings
- Troubleshooting guide (common issues + resolution steps)
- FAQ document
- Definition Alignment Document (final version)
- Maintenance Schedule
- Vendor support contacts and escalation paths

**For Single Project engagements:** Walk the customer through the maintenance schedule in detail. Record a video walkthrough of the session.

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

- What went well? (Platform selection process, integration build quality, training effectiveness)
- What would we do differently? (Sync configuration order, form design process, vendor coordination)
- Any learnings to feed back into SOPs?

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell > Downsell > Retry    |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (ongoing event ops support + optimization)
   | if no
2. Downsell: Another one-time project (e.g., event attribution deep-dive, lead scoring with event data)
   | if yes
3. Retry retainer at end of next project cycle
```

**Script:**

> "Now that the event platform is live and your team is running events independently, there are two ways we can continue working together. Option 1: We handle ongoing event ops optimization — new event types, platform updates, integration maintenance. Option 2: If there's a specific project like event attribution modeling or lead scoring refinement that uses this new event data, we can scope that out. Which sounds more interesting?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On [date ~quarter out], we'll review how the event platform is performing — sync health, registration conversion rates, attribution accuracy — and see if any adjustments are needed."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                           |
| ------------------- | ------------------------------------------------------ |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks        |
| 2. Review metrics   | Pull sync health, form conversion, attribution data    |
| 3. Decide ownership | Can Architect handle this check-in, or need SME?       |
| 4. Prep materials   | If SME needed, brief them. If Architect, prep talking points. |

**At the refinement check-in:**

- Review sync health and integration stability
- Check form conversion rates and registration trends
- Review event attribution accuracy
- If minor: Architect handles tweaks (form field changes, dashboard filters)
- If major: Scope new project (new event type integration, platform migration)

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- Event Requirements Matrix (event types mapped to platform capabilities)
- Platform Evaluation Scorecard (comparison of 2-3 platforms with recommendation)
- Integration Architecture Document (event platform > CRM > MAP data flows)
- Field Mapping Table (registration fields > CRM/MAP field API names)
- Definition Alignment Document (event ops terms agreed by stakeholders)

**Technical Deliverables:**

- Configured event platform (branding, templates, defaults, user roles)
- CRM integration (registration sync, attendance sync, Campaign Member status mapping)
- MAP integration (program templates, email sequences, attendance-based triggers)
- Registration form templates (with UTM tracking, consent, progressive profiling)
- Dashboards and reports (registration velocity, attendance tracking, event attribution)

**Documentation Package:**

- Training video walkthrough recordings (event creation walkthrough, dashboard navigation)
- Written guides (event creation quick-reference, field mapping reference)
- Troubleshooting guide (common issues + resolution steps)
- FAQ document
- Definition Alignment Document (final version)
- Maintenance Schedule

---

## Appendix

### What Each Phase Produces

| Phase                    | Output                                                                  | Gate Criteria                                                                      |
| ------------------------ | ----------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| **Phase 1: Strategy**    | Requirements matrix + integration architecture + field mappings (signed off) | Stakeholders approved platform, architecture, and field mappings                   |
| **Phase 2: Engineering** | Configured platform, integrations, forms, dashboards (pilot-tested)      | Pilot event completed, all sync points verified, customer approved                 |
| **Phase 3: Enablement**  | Trained team with documentation and at least one live event completed     | Training delivered, hypercare complete, team operates independently                |
| **Phase 4: Handoff**     | Independent customer + archived project                                  | Internal/external handoffs complete, maintenance plan in place, project closed     |

### Adaptation Notes

This project is **engineering-heavy**:

| Project Profile       | Strategy Weight | Engineering Weight | Enablement Weight | This Project |
| --------------------- | --------------- | ------------------ | ----------------- | ------------ |
| **Engineering-heavy** | 20-30%          | 50-60%             | 15-20%            | Yes          |

- Phase 1 may compress if platform is pre-selected (skip evaluation, focus on integration design)
- Phase 2 is the core — platform config, 2 integrations (CRM + MAP), forms, and dashboards
- Phase 3 must cover at least one live event cycle during hypercare
- Phase 4 always applies — integration-heavy projects need detailed troubleshooting guides

### Key Industry Context

The event management software market reached $15.5 billion in 2024 and is projected to grow to $34.7 billion by 2029 at a 17.4% CAGR [1]. Over 71% of enterprises globally reported using at least one SaaS-based event platform as of 2024 [2]. For B2B SaaS companies, events represent a disproportionately high-value channel: HockeyStack's analysis of 2.6 million deals across 198 B2B SaaS companies found that virtual events convert to qualified opportunities 33% more efficiently than other channels, despite representing less than 3% of total deal volume [3].

The challenge is not the events themselves but the operational plumbing. Manual event data handling creates delays that directly impact pipeline: 92% of duplicate CRM records are created during initial registration or data entry phases [4], and poor CRM data quality costs organizations an average of $12 million annually [5]. Registration form design also matters — reducing form fields from 4 to 3 can increase conversion rates by nearly 50% [6], and 27% of users abandon forms because they are too long [7].

This project exists to close the gap between event execution and revenue attribution by automating the registration-to-CRM-to-follow-up pipeline.

### Phase 1 Reference: Strategy

**Three decisions that determine project success:**

**1. Platform selection.** The wrong platform creates integration headaches for years. Evaluate against the client's actual requirements (not vendor marketing) and weight CRM/MAP integration quality heavily. Native connectors with real-time sync are strongly preferred over API-only options. The event platform landscape is consolidating — Cvent acquired both Goldcast (~$300M) and ON24 (~$400M) in December 2024 [8] — which may affect long-term platform stability.

**2. Integration architecture.** The data flow between event platform, CRM, and MAP must be designed before building. Key decisions: sync direction (uni vs. bi-directional), sync frequency (real-time vs. batch), duplicate handling strategy, and Campaign Member status schema.

**3. Field mapping.** Which registration fields map to which CRM/MAP fields determines data quality downstream. Getting this wrong creates garbage data that pollutes lead scoring, attribution, and reporting.

**Why Definition Alignment matters:** Event ops has ambiguous terminology. "Attended" means different things for virtual (joined the session for any duration? for 50%+ of runtime?) vs. in-person (badge scanned? signed attendance sheet?). "Event-sourced pipeline" vs. "event-influenced pipeline" creates attribution disagreements. Aligning on these terms before building prevents rework.

### Phase 2 Reference: Engineering

**Key principles:**

**Build order matters.** Always build in this sequence: (1) platform account + branding, (2) CRM integration, (3) MAP integration, (4) registration forms, (5) dashboards. Each layer depends on the previous — you cannot test form-to-CRM sync without the CRM integration in place.

**Test with real-like data.** Use test registrations that include existing CRM contacts, net-new leads, and known duplicates. This surfaces duplicate handling issues before go-live.

**Real-time sync is non-negotiable for registration.** Batch/nightly syncs cause leads to go cold. Configure real-time or near-real-time sync for registration-to-CRM and set up monitoring for sync failures. Goldcast, for example, syncs registrants, attendees, and engagement data through Custom Activities to Salesforce Sales Cloud in near-real-time [9].

### Phase 3 Reference: Enablement

**Key principles:**

**Hypercare must cover at least one full live event cycle** (registration open > event > post-event follow-up). Office hours pattern — put a recurring 30-min slot on the calendar so Marketing Ops can bring real-time issues from their first live event.

**The pilot event in Phase 2 is not the same as the first live event in Phase 3.** The pilot uses test data. Hypercare covers the first real event with real registrations and real attendee data.

### Phase 4 Reference: Handoff

**Why maintenance schedules matter for event ops:** Event platform integrations are particularly prone to drift because CRM schema changes (field renames, new picklist values) can silently break sync mappings, event platform vendors release updates that change API behavior, marketing teams add new event types requiring different registration flows, and email deliverability degrades over time without monitoring. The maintenance schedule prevents these issues from compounding into a broken system that no one notices until a critical event launch fails.

**Escalation boundaries:**
- **Architect handles:** New event creation from existing templates, form field additions, dashboard filter changes, simple report modifications, training new team members using existing video walkthroughs
- **SME handles:** Integration sync failures, new event types requiring different workflows, CRM field structure changes affecting mappings, platform migration or major version upgrades, attendance tracking configuration changes

---

## References

[1] [MarketsandMarkets - Event Management Software Market](https://www.marketsandmarkets.com/Market-Reports/event-management-software-market-136859992.html)

[2] [Grand View Research - Event Management Software Market Report](https://www.grandviewresearch.com/industry-analysis/event-management-software-market-report)

[3] [HockeyStack - The State of Event Marketing in 2025](https://www.hockeystack.com/lab-blog-posts/the-state-of-event-marketing-in-2025-so-far)

[4] [Landbase - Duplicate Record Rate Statistics](https://www.landbase.com/blog/duplicate-record-rate-statistics)

[5] [SalesIntel - How Bad CRM Data Can Impact Your Sales Team](https://salesintel.io/blog/how-and-why-bad-crm-data-is-hurting-your-sales-team-performance-and-b2b-lead-generation/)

[6] [Feathery - Online Form Statistics](https://www.feathery.io/blog/online-form-statistics)

[7] [Insiteful - Form Abandonment Statistics](https://insiteful.co/blog/form-abandonment-statistics/)

[8] [Event Tech Live - Cvent's $700 Million December Buying Spree](https://eventtechlive.com/cvents-700-million-december-buying-spree-signals-event-techs-consolidation-era/)

[9] [Goldcast - Salesforce Integration Documentation](https://help.goldcast.io/en_US/7805592005531-Salesforce)
