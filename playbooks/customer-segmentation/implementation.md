# Customer Segmentation — Implementation

## Project One-Pager

### Customer Segmentation One-Pager

#### Project Type

- Category: Balanced
- Primary Deliverable: Working segmentation fields in CRM with automated segment assignment, operational views, and executive dashboards showing segment-level retention, expansion, and health metrics

##### Phase Relevance

| Phase          | Applies? | Weight | Notes                                                        |
| -------------- | -------- | ------ | ------------------------------------------------------------ |
| 1. Strategy    | Yes      | Heavy  | 2-3 refinement loops to align on segmentation dimensions and criteria |
| 2. Engineering | Yes      | Medium | CRM field creation, automation rules, data enrichment, dashboards |
| 3. Enablement  | Yes      | Medium | Training by role (leadership vs CSM), adoption monitoring    |
| 4. Handoff     | Yes      | Light  | Internal + External, governance handoff                      |

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────>│ 2. ENGINEER  │────>│3. ENABLEMENT │────>│  4. HANDOFF  │
  │    Heavy     │     │    Medium    │     │    Medium    │     │    Light     │
  │ 1a->1b->1c->1d│     │ 2a->2b->2c->2d│     │ 3a->3b->3c->3d│     │ 4a->4b->4c->4d│
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   Define segments      Build in CRM +       Train CS team +      Governance +
   + get sign-off       automate assignment  leadership reporting  ownership transfer
```

**This project's flow:**
- Full 4-phase. Heavy strategy (segmentation framework design drives everything downstream), medium engineering (CRM config + data enrichment + dashboards), medium enablement (training CSMs and leadership to use segments daily), light handoff (governance process + quarterly review cadence).
- No phases skipped. Some customers compress Phase 2 if data quality is already high and enrichment is not needed.

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Watch intro video explaining what customer segmentation is, why it matters for CS, and what the project covers
- [ ] Complete intake form with current segmentation state, key business questions, and CRM access details
- [ ] Get VP CS sign-off on participating stakeholders and intended segment use cases

##### Track B: Architect Prep
- [ ] Pull CRM field audit: all customer-related fields on Account/Company object
- [ ] Run data quality diagnostic on existing segmentation-adjacent fields (industry, company size, region, tier)
- [ ] Create v0 segmentation framework based on intake form + industry benchmarks for similar-sized B2B SaaS companies

#### Refinement Loop (1b -> 1c -> 1d)

| Meeting      | Sub-Phase | Focus                                                    | Stakeholder                  | Output                            |
| ------------ | --------- | -------------------------------------------------------- | ---------------------------- | --------------------------------- |
| Kickoff      | 1b        | Present v0 framework, validate segmentation dimensions   | VP CS, CS Ops, Senior CSMs   | Feedback for v1 framework         |
| Refinement 1 | 1c        | Review v1 with refined criteria and segment definitions  | VP CS, CS Ops, RevOps        | v2 with approved dimensions       |
| Refinement 2 | 1c        | Finalize criteria thresholds, data source mapping        | CS Ops, RevOps, Data team    | v3 with complete business rules   |
| Sign-Off     | 1d        | Strategic approval of segmentation framework             | All stakeholders             | Final segmentation framework      |

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held — v0 segmentation framework presented
- [ ] 1c. Refinement loop complete (v0 -> vFinal segmentation framework)
- [ ] 1d. Strategic sign-off on segmentation dimensions, criteria, and operational actions

##### Phase 2: Engineering
- [ ] 2a. Tech spec created (field mappings, automation logic, enrichment plan)
- [ ] 2b. Engineering handoff meeting held
- [ ] 2c. Build complete (fields, automation, enrichment, dashboards)
- [ ] 2d. QA/Test + customer sign-off on segment assignments and reports

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped (video walkthroughs, quick-reference guide, FAQ)
- [ ] 3b. Training sessions delivered (leadership + CSM sessions)
- [ ] 3c. Hypercare period complete (2 weeks post-launch)
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff (SME -> Architect) complete
- [ ] 4c. External handoff (team -> Customer) complete
- [ ] 4d. Project closed and archived

#### Document Types

##### Working Documents (iterate together)

| Document                      | Purpose                                          | When Complete                                  |
| ----------------------------- | ------------------------------------------------ | ---------------------------------------------- |
| Segmentation Intake Form      | Capture current state, business questions, access | All fields filled, stakeholders identified     |
| Gap Analysis Table            | Compare current vs. needed segmentation          | Gaps prioritized, enrichment needs identified  |
| Segmentation Framework Draft  | Define dimensions, criteria, naming conventions  | All dimensions defined, thresholds set         |
| Data Source Map               | Map each field to source system                  | Every field has a source, enrichment plan set  |

##### Deliverables (polished outputs)

| Deliverable                        | Created From                 | Customer Uses For                              |
| ---------------------------------- | ---------------------------- | ---------------------------------------------- |
| Segmentation Framework Document    | Framework draft + sign-off   | Internal alignment, board-level reporting      |
| Segment Distribution Report        | CRM data post-build          | Validate segment balance, identify outliers    |
| Executive Dashboard                | Tech spec + built system     | Leadership visibility into segment performance |
| CSM Quick-Reference Guide          | Framework document           | Daily workflow, segment-based prioritization   |

#### Enablement Details

##### Training Types

| Type       | Audience                        | Focus                                            | Duration |
| ---------- | ------------------------------- | ------------------------------------------------ | -------- |
| Leadership | VP CS, CS Directors             | Interpret segment dashboards, use for decisions  | 30 min   |
| Technical  | CS Ops, RevOps, CRM Admin      | Maintain fields, update rules, manage exceptions | 60 min   |
| CSM        | Individual CSMs                 | Filter book of business, use segment views daily | 45 min   |

##### Hypercare
- Applies: Yes
- Duration: 2 weeks
- Office Hours: Yes — weekly 30-min slot for segment questions, edge cases, and minor adjustments

##### Training Assets to Create
- [ ] Video walkthrough: Segmentation model (definitions, criteria, business rules)
- [ ] Video walkthrough: Dashboard navigation and report filtering by segment
- [ ] Doc: Segment definitions quick-reference card
- [ ] Doc: FAQ — common segment assignment questions and edge cases
- [ ] Doc: Data enrichment refresh process

#### Handoff & Retention

##### Internal Handoff (SME -> Architect)
- Key context for Architect: Segmentation framework rationale, data quality baseline, enrichment tool credentials and refresh cadence
- Escalation trigger: Any request to add new segmentation dimensions or change assignment logic

##### External Handoff
- Final meeting agenda: Review segmentation framework, walk through dashboards, demonstrate maintenance tasks, confirm governance cadence
- Documentation package: Segmentation Framework Document, dashboard video walkthrough recordings, Quick-Reference Guide, FAQ, Maintenance Schedule

##### Maintenance Schedule
- Monthly: Data quality spot-check on segmentation fields, review segment distribution for drift
- Quarterly: Full segment review with leadership (add/retire segments, adjust thresholds)
- Who owns: Single project = customer owns | Dedicated = Architect owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services -> if no -> Downsell: Customer Health Model project or Renewal Management project -> Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~1 quarter after launch
- Internal prep trigger: 2 weeks before
- Decision: Architect handles / SME needed

#### Key Assets

| Asset                              | Format       | When Used                  |
| ---------------------------------- | ------------ | -------------------------- |
| Segmentation Intake Form Template  | Google Form  | Phase 1a (Pre-Kickoff)     |
| Gap Analysis Table Template        | Google Sheet | Phase 1a-1c (Strategy)     |
| Segmentation Framework Template    | Google Doc   | Phase 1b-1d (Strategy)     |
| Data Source Map Template           | Google Sheet | Phase 2a (Tech Spec)       |
| Executive Dashboard Template       | CRM Report   | Phase 2c (Build)           |

#### Definition Alignment Terms

| Term                | Typical Definition                                                                                  |
| ------------------- | --------------------------------------------------------------------------------------------------- |
| Customer Segment    | A grouping of customer accounts sharing common attributes used to differentiate service and strategy |
| Firmographic Segment | Segmentation based on company characteristics: industry, size, geography, revenue                   |
| Behavioral Segment  | Segmentation based on product usage patterns, engagement level, and adoption metrics                |
| Value-Based Segment | Segmentation based on ARR, expansion potential, strategic importance, and lifetime value             |
| Customer Tier       | A composite segment (often combining value + behavioral data) used to determine service level       |
| Segment Assignment  | The automated or manual process of placing an account into its correct segment                      |

#### Common Gotchas
- Team creates 15+ micro-segments that are impossible to action on -> Limit to 3-5 dimensions with 3-5 values each. Each segment must have enough accounts (minimum 20-30) to be meaningful [1]
- Segments set once and never updated as customer data changes -> Build automated assignment rules and schedule quarterly segment reviews
- Segments exist but no one changes their behavior based on them -> Define specific operational actions per segment during strategy phase (e.g., Enterprise = quarterly executive QBRs, SMB = digital-touch monthly check-ins)
- Data enrichment tool returns low match rates -> Always run a test batch of 50-100 records before committing to an extended enrichment run
- Conflicting definitions of "Enterprise" across departments -> Use the Definition Alignment Document to force agreement before building anything

#### Methodology Options

| Option                        | When to Use                                                     | Complexity |
| ----------------------------- | --------------------------------------------------------------- | ---------- |
| Firmographic-Only             | Limited product usage data, quick win needed, early-stage CS org | Low        |
| Firmographic + Value-Based    | Mature CRM data, clear ARR tiers, need to prioritize by value   | Medium     |
| Full Multi-Dimensional        | CSP in place with usage data, want behavioral + firmographic + value | High       |

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on the segmentation framework — what dimensions, what criteria, what operational actions.
>
> **Output:** Signed-off Segmentation Framework Document + Definition Alignment Document.

### 1a. Pre-Kickoff

> Two parallel tracks run before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                      | Format             |
| ----------------------------- | ------------------------------------------------------------ | ------------------ |
| Intro video                   | Explain what customer segmentation is and why it matters for CS operations | Video (5-10 min)   |
| Definition Alignment Document | Get stakeholder sign-off on key terms (segment, tier, firmographic, behavioral) | Google Doc         |
| Segmentation Intake Form      | Capture current segmentation state, business questions, CRM access | Google Form or Doc |

The intake form asks:
- What CRM are you using? (Salesforce / HubSpot / Other)
- Do you have a Customer Success Platform? (Gainsight / ChurnZero / Vitally / None)
- What segmentation fields exist today? (industry, company size, region, tier — check all that apply)
- What business questions should segmentation answer? (free text)
- How will segments be used operationally? (reporting, playbook triggers, resource allocation, QBR segmentation — check all)
- Who are the primary segment consumers? (CS team, leadership, marketing — check all)
- What enrichment tools do you have access to? (ZoomInfo, Apollo, Clearbit, Clay — check all)

**Completion tracking:** CS Ops or RevOps contact is responsible for ensuring intake is completed. Do not cancel kickoff if incomplete, but push hard — data quality assessment is limited without intake.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                           | Output                                    |
| ---- | ---------------------------------------------------------------- | ----------------------------------------- |
| 1    | Pull CRM field audit (all customer-related fields)               | Field inventory with data types           |
| 2    | Run data quality diagnostic on segmentation-adjacent fields      | Completeness scorecard (% populated)      |
| 3    | Assess current segmentation usage (reports, workflows, views)    | Current state assessment                  |
| 4    | Research industry benchmarks for segmentation in similar companies | Benchmark reference doc                   |
| 5    | Build v0 segmentation framework                                  | Draft framework with ASSUMED markers      |

The v0 framework typically includes:
- 3-5 proposed segmentation dimensions (e.g., Customer Tier, Industry Vertical, Company Size, Engagement Level)
- Draft criteria for each dimension (e.g., Enterprise = 1000+ employees AND >$100K ARR)
- Proposed naming conventions
- Draft operational actions per segment (e.g., Enterprise = white-glove QBRs quarterly, SMB = digital-touch monthly)

**Critical:** Mark everything as ASSUMED. The kickoff call validates.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building anything.

| Term                  | Our Definition                                                                                          | Internally Approved? |
| --------------------- | ------------------------------------------------------------------------------------------------------- | -------------------- |
| Customer Segment      | A grouping of accounts sharing common attributes, used to differentiate service strategy                 | [ ] Yes / [ ] No     |
| Customer Tier         | A composite ranking (often combining value + engagement) that determines service level                   | [ ] Yes / [ ] No     |
| Firmographic Data     | Company-level attributes: industry, employee count, revenue, geography                                   | [ ] Yes / [ ] No     |
| Behavioral Data       | Product usage patterns, login frequency, feature adoption, support ticket volume                         | [ ] Yes / [ ] No     |
| Value-Based Data      | ARR, expansion revenue potential, strategic importance, lifetime value                                    | [ ] Yes / [ ] No     |
| Segment Assignment    | The automated process of placing an account into its correct segment based on defined criteria            | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your CS leadership team. Check "Yes" when approved. We cannot proceed to engineering until all terms are aligned. Disagreement on these terms mid-build causes rework and delays.

---

### 1b. Kickoff Call

> **Purpose:** Present v0 segmentation framework and get alignment. We walk in with a framework built from intake data and benchmarks. Customer reacts and refines.

#### Agenda (60-90 min)

| Time  | Topic                          | What Happens                                                      |
| ----- | ------------------------------ | ----------------------------------------------------------------- |
| 0-15  | Walk through v0 framework      | "Here are the 3-5 dimensions we recommend based on your intake"   |
| 15-30 | Validate dimensions            | ASSUMED dimensions -> CONFIRMED or replaced                       |
| 30-45 | Review criteria and thresholds | Discuss specific cutoff values (e.g., what is "Enterprise" here?) |
| 45-55 | Definition alignment           | Review Definition Alignment Document                              |
| 55-70 | Identify data gaps             | Which fields are missing, what enrichment is needed               |
| 70-80 | Operational actions mapping    | How will each segment be treated differently                      |
| 80-90 | Next steps                     | Schedule refinement loop, assign homework                         |

#### What We Bring

- v0 segmentation framework (built in Track B prep)
- Data quality scorecard showing field completeness
- Industry benchmark data for segmentation in similar B2B SaaS companies
- Definition Alignment Document (pre-filled with our recommendations)
- Questions list: What does "strategic importance" mean to you? How do you define your customer tiers today? What enrichment budget is available?

#### What We Leave With

- Feedback and corrections on v0 (info needed for v1)
- Confirmed or adjusted segmentation dimensions
- Clear enrichment requirements and budget constraints
- Definition alignment progress (or blockers needing executive sign-off)
- Homework: customer to provide list of current enrichment tools, confirm CRM admin access

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Iterate on the segmentation framework until sign-off. Typically 2-3 refinement meetings.

#### The Pattern

```
Kickoff Call (gather info, validate dimensions)
    |
Framework updated -> v1
    |
Meeting 2 (refine criteria, confirm thresholds) -> v2
    |
Meeting 3 (finalize data sources, confirm operational actions) -> v3
    |
Final Review -> Sign-off
```

#### Before Each Meeting

1. Update segmentation framework with previous meeting feedback
2. Refine criteria thresholds based on actual CRM data distribution
3. Prepare questions for remaining ASSUMED items

#### During Each Meeting

1. Walk through current version of framework
2. Capture corrections to criteria and thresholds
3. Validate what's now CONFIRMED
4. Map remaining ASSUMED items to specific data sources or stakeholder decisions

#### After Each Meeting

1. Update framework (v[n-1] -> v[n])
2. Track ASSUMED -> CONFIRMED progression
3. Update gap analysis and enrichment plan

#### Meeting Types for Customer Segmentation

| Meeting Type          | Focus                                                | Stakeholder                |
| --------------------- | ---------------------------------------------------- | -------------------------- |
| CS Strategy           | Segmentation dimensions, use cases, operational actions | VP CS, CS Directors        |
| Data & Enrichment     | Data sources, field quality, enrichment plan          | CS Ops, RevOps, Data team  |
| Final Review          | Full framework walkthrough, sign-off                  | All stakeholders           |

#### Typical Timeline

| Milestone               | Timing                                        |
| ----------------------- | --------------------------------------------- |
| Pre-kickoff prep        | 2-3 days                                      |
| Kickoff call            | Day 1 of engagement                           |
| Refinement loop         | 1-2 weeks (2-3 meetings)                      |
| Final review + sign-off | When all dimensions and criteria are CONFIRMED |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything before building in CRM.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by CS leadership
- [ ] Segmentation dimensions agreed (3-5 dimensions with clear criteria)
- [ ] Criteria thresholds defined for each dimension (e.g., SMB &lt;100 employees, Mid-Market 100-1000, Enterprise 1000+)
- [ ] Operational actions mapped to each segment (how treatment differs)
- [ ] Data sources mapped for each segmentation field
- [ ] Enrichment plan approved (tool, fields, budget)
- [ ] All critical inputs CONFIRMED (vs ASSUMED)
- [ ] Customer understands what will be built in CRM

#### Decision Point

- **Proceed to Engineering** -> Customer wants segments built, automated, and dashboarded in CRM
- Note: This project type does not have a natural exit point after Phase 1. The framework needs to be operationalized in the CRM to deliver value.

---

## Phase 2: Engineering

> **Goal:** Build segmentation fields, automation rules, data enrichment, and dashboards in CRM.
>
> **Output:** Working segmentation in CRM with automated assignment, enriched data, and executive dashboards.

| Project Type | Engineering Weight | Context                                                              |
| ------------ | ------------------ | -------------------------------------------------------------------- |
| Customer Segmentation | Medium (40-50%) | CRM field creation, automation rules, data enrichment, dashboards |

### Sub-Phases

```
2a Tech Spec -> 2b Engineering Handoff -> 2c Build -> 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate the segmentation framework into CRM-specific technical specifications.

**Input:** Signed-off segmentation framework + data source map from Phase 1

**What happens:**

1. Map each segmentation dimension to specific CRM fields (e.g., `Customer_Tier__c`, `Industry_Segment__c`, `Engagement_Level__c`)
2. Define field types (picklist, formula, lookup)
3. Write automation logic for each assignment rule
4. Document enrichment tool configuration
5. Specify dashboard and report requirements

**Output:** Tech spec containing:

- **Field specifications:** Field name, API name, data type, picklist values, field-level security, page layout placement
- **Automation logic:** For each dimension — trigger conditions, assignment criteria, handling of null values and edge cases
  - Example: `IF Employee_Count__c < 100 AND ARR__c < $50K THEN Customer_Tier__c = "SMB"`
  - Example: `IF Employee_Count__c >= 100 AND Employee_Count__c < 1000 THEN Customer_Tier__c = "Mid-Market"`
  - Example: `IF Employee_Count__c >= 1000 OR ARR__c >= $500K THEN Customer_Tier__c = "Enterprise"`
- **Enrichment plan:** Which tool (ZoomInfo, Apollo, Clearbit, Clay), which fields, expected coverage rates, API configuration
- **Dashboard specs:** Charts, filters, groupings, target audiences
- **Build sequence:** 1) Create fields, 2) Configure enrichment, 3) Run enrichment, 4) Build automation, 5) Run initial assignment, 6) Build reports/dashboards

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs with engineer before building.

**Who attends:** Architect + Engineer (or CRM admin)

**Agenda (30-45 min):**

| Time  | Topic              | What Happens                                                        |
| ----- | ------------------ | ------------------------------------------------------------------- |
| 0-15  | Walk through specs | Architect explains segmentation framework context + tech spec       |
| 15-30 | Engineer questions | Clarify automation logic, flag CRM-specific risks, discuss enrichment approach |
| 30-45 | Refine and approve | Adjust specs for CRM platform specifics, confirm build approach     |

**What Architect brings:**

- Segmentation Framework Document (for strategic context)
- Draft tech spec (field mappings, automation logic, enrichment plan)
- Data quality scorecard (field completeness from 1a)

**What engineer leaves with:**

- Approved tech spec
- Clear build sequence (fields -> enrichment -> automation -> dashboards)
- Known risks: data quality gaps, enrichment match rates, CRM API limits

---

### 2c. Build (Configure)

> **Purpose:** Build segmentation infrastructure in CRM and connected systems.

**Input:** Approved tech spec from 2b

**Build sequence:**

**Step 1: Create CRM Fields**
- Create custom fields for each segmentation dimension on Account object (Salesforce) or Company object (HubSpot)
- Configure picklist values matching the approved framework
- Set field-level security (visible to CS, Sales, and relevant teams)
- Add fields to appropriate page layouts and record types
- Add field descriptions documenting business rules for each picklist value
- Test in sandbox before production deployment

**Step 2: Configure and Run Data Enrichment**
- Set up enrichment tool (Clay, ZoomInfo, Apollo, Clearbit) with customer account list
- Run test batch (50-100 records) to validate match rates and data quality
- Review test results, adjust field mappings if needed
- Run extended enrichment for firmographic fields (employee count, industry, revenue, tech stack)
- Import enriched data back to CRM with proper field mapping
- Validate sample of enriched records for accuracy
- Document coverage rates per field

**Step 3: Build Automation Rules**
- Build assignment logic for each segmentation dimension
  - Firmographic segments: Use employee count and ARR thresholds via formula fields or flow/workflow rules
  - Behavioral segments: Integrate with CSP data (usage scores, engagement metrics) via API sync or middleware
  - Value-based segments: Use ARR, expansion potential, strategic importance from CRM opportunity data
- Handle edge cases: null values get "Unassigned" with alert to CS Ops
- Handle conflicts: when a customer qualifies for multiple tiers, value-based criteria take precedence
- Test automation with sample records covering all segment combinations

**Step 4: Run Initial Segment Assignment**
- Execute extended update to assign segments to all active customer accounts
- Use data loader (Salesforce) or import tool (HubSpot) for initial population
- Validate segment distribution matches expectations (sanity check: if 80% land in one segment, something is wrong)
- Review outliers and exceptions (e.g., large enterprise account landing in SMB segment)
- Make manual corrections where data quality caused mis-assignment
- Document final segment distribution as baseline

**Step 5: Build Reports and Dashboards**
- Create "Customers by Segment" summary report showing distribution
- Build "ARR by Segment" report with revenue breakdown
- Create "Retention by Segment" report showing churn/renewal rates per segment
- Build "Health by Segment" report (if health scores exist in CSP)
- Create "CSM Book of Business" report grouped by segment
- Build executive dashboard with segment distribution chart, performance comparison, and trending over time
- Configure filtered list views for CSMs: "My Enterprise Accounts," "My At-Risk SMB Accounts"
- Configure CSP workspace views grouped by segment (Gainsight, ChurnZero, Vitally)

**Build tracking:**

- [ ] CRM fields created and configured
- [ ] Data enrichment run and validated
- [ ] Automation rules built and tested
- [ ] Initial segment assignment complete
- [ ] Reports and dashboards built
- [ ] CSM list views and workspace views configured

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify the segmentation build works and get customer approval.

**Technical testing checklist:**

- [ ] All segmentation fields created with correct data types and picklist values
- [ ] Field-level security correctly configured (right teams see right fields)
- [ ] Automation rules fire correctly when account data changes
- [ ] Enrichment data populated accurately (spot-check 20 records against source)
- [ ] Segment distribution is reasonable (no single segment has >70% of accounts unless expected)
- [ ] Edge cases handled: null values default to "Unassigned," conflicting criteria resolve correctly
- [ ] All reports generate accurate data
- [ ] Dashboard filters work across all segment combinations
- [ ] CSM list views filter correctly
- [ ] No duplicate segment assignments on any account

**Customer testing:**

- Walk customer through segment distribution report: "Does this match your intuition?"
- Have CS Ops spot-check 10-15 accounts they know well — are they in the right segments?
- Demo dashboard to leadership: "Can you answer the business questions you identified in discovery?"
- Have CSMs test filtered list views: "Can you find your Enterprise accounts? Your at-risk accounts?"

**Engineering sign-off checkpoint:**

- [ ] Built system matches tech spec
- [ ] All technical tests passing
- [ ] Customer has tested and approved segment assignments
- [ ] Dashboards validated by leadership
- [ ] Ready for enablement

**Decision point:**

- **Proceed to Enablement** -> System is built, needs training and adoption
- **Loop back to Build** -> Segment assignments incorrect, enrichment gaps, dashboard issues

---

## Phase 3: Enablement

> **Goal:** CS team and leadership can use segments in daily work and decision-making.
>
> **Output:** Trained team with documentation, stabilized system, segments actively used in workflows.

### Sub-Phases

```
3a Training Prep -> 3b Training Sessions -> 3c Hypercare -> 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from segmentation framework and built system.

**Input:** Segmentation Framework Document + tech specs + built CRM system

**Output:** Training package containing:

- **Video walkthrough scripts:**
  - Segmentation model walkthrough (7-10 min): What each segment means, how assignments work, where to find segment data
  - Dashboard navigation (5-7 min): How to read segment dashboards, use filters, export data
  - CSM workflow guide (5 min): How to filter book of business by segment, use list views
- **Written guides:**
  - Segment definitions quick-reference card (one-pager with all dimensions, criteria, and operational actions)
  - Data enrichment refresh process (how often data refreshes, what to do when enrichment gaps appear)
  - Segment exception handling process (what to do when a customer seems mis-assigned)
- **FAQ draft:**
  - "Why is [account] in [segment]?" -> Check criteria, verify source data
  - "Can I override a segment assignment?" -> Process for exception requests
  - "How often do segments update?" -> Based on automation trigger frequency
  - "What if a customer's data changes?" -> Automation re-evaluates on field update

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to customer team so segments are used, not ignored.

Companies that use smart segmentation to personalize CS strategies report higher engagement and retention rates across their customer base [2]. The training is what bridges the gap between "segments exist" and "segments change behavior."

**Training sessions by role:**

| Session              | Audience                   | Focus                                                             | Duration |
| -------------------- | -------------------------- | ----------------------------------------------------------------- | -------- |
| Leadership training  | VP CS, CS Directors        | How to interpret segment dashboards, use for resource allocation and strategic decisions | 30 min   |
| CSM training         | Individual CSMs            | How to filter book of business by segment, prioritize outreach, use segment-based playbooks | 45 min   |
| Technical handoff    | CS Ops, RevOps, CRM Admin | How to maintain fields, update automation rules, handle exceptions, run data quality checks | 60 min   |

**Training delivery:**

1. Schedule sessions with appropriate stakeholders (can be combined if team is small)
2. Deliver training live with screen share of actual CRM data
3. Record video walkthroughs during or after each session for future reference
4. Answer questions, note gaps for FAQ updates
5. Provide quick-reference card as leave-behind

**Output:**

- Trained stakeholders across all three audience types
- Video walkthrough recordings for onboarding future team members
- Updated FAQ based on questions raised during training

---

### 3c. Hypercare

> **Purpose:** Intensive post-launch support to catch segment assignment issues, adoption gaps, and edge cases.

**Duration:** 2 weeks

**What happens:**

- Weekly 30-min office hours: CSMs and CS Ops can bring segment questions, edge cases, and feedback
- Architect monitors segment usage: Are CSMs actually using filtered views? Are dashboards being accessed?
- Bug triage: Fix mis-assignments, adjust automation rules for edge cases discovered post-launch
- Track adoption metrics: % of CSMs using segment filters in daily workflow

**When to extend:** If adoption is below 50% at end of 2 weeks, extend hypercare by 1 additional week with targeted outreach to non-adopters.

**Output:** Stabilized segmentation system with no critical issues, confirmed adoption across CS team

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm customer team can operate segmentation independently.

**Validation checkpoint:**

- [ ] All three training sessions delivered (leadership, CSM, technical)
- [ ] Training recordings and documentation provided
- [ ] Hypercare period complete
- [ ] No critical segment assignment issues outstanding
- [ ] CSMs actively using segment filters (>70% of team)
- [ ] Leadership has accessed segment dashboards at least once
- [ ] CS Ops understands maintenance procedures
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** -> Customer is enabled, segments are being used
- **Extend Hypercare** -> Adoption too low, additional training needed

---

## Phase 4: Handoff

> **Goal:** Clean project close with governance process established and retention/expansion path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the segmentation system, project archived.

**Structure:**

```
4a Maintenance Schedule -> 4b Internal Handoff -> 4c External Handoff -> 4d Project Close
                          (SME -> Architect)       (Team -> Customer)     (Archive + Debrief)
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At                                                                         |
| ----------------------------- | -------------------- | ------------------------------------------------------------------------------------- |
| **Single Project**            | Customer owns        | 4c (External Handoff) — customer receives maintenance schedule and runs it themselves |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) — Architect receives maintenance schedule and runs it for customer |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention to keep segments accurate and actionable.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task                    | What to Check                                          | Red Flag Threshold                                |
| ------------------------------- | ------------------------------------------------------ | ------------------------------------------------- |
| Data Quality Spot-Check         | % of accounts with populated segmentation fields       | Drop below 80% populated on any dimension         |
| Segment Distribution Review     | Account count and ARR per segment                      | Any segment grows or shrinks by >20% month-over-month |
| Enrichment Freshness Check      | Date of last enrichment run, new accounts without enrichment | >30 new accounts without segment assignment       |

**Quarterly Tasks:**

| Quarterly Task                  | What to Review                                         | Action if Off-Track                                    |
| ------------------------------- | ------------------------------------------------------ | ------------------------------------------------------ |
| Full Segment Framework Review   | Are dimensions still relevant? Any new needs?          | Propose new dimension or retire obsolete one            |
| Criteria Threshold Validation   | Are cutoff values still appropriate given growth?      | Adjust thresholds if company has scaled significantly   |
| Operational Action Audit        | Are segment-based playbooks actually being used?       | Re-train or simplify if adoption has dropped            |
| Dashboard Usage Review          | Which reports are being accessed? Which are ignored?   | Retire unused reports, enhance popular ones             |

**After First Business Cycle (60-90 days post-launch):**

- Segment-to-Outcome Validation: Do segments actually correlate with retention and expansion? Compare churn rate and NRR across segments
- Assignment Accuracy Audit: Pull 50 random accounts and manually validate segment assignments
- Key Question: Is segmentation changing behavior? Are CSMs treating Enterprise customers differently than SMB?

**Refinement Triggers (when to re-engage):**

| Trigger                         | Threshold                                              | Response                                                |
| ------------------------------- | ------------------------------------------------------ | ------------------------------------------------------- |
| Segment distribution drift      | >25% of accounts in "Unassigned" or default segment    | Re-run enrichment, review automation rules              |
| Churn pattern change            | Churn concentrates in one segment for 2+ months        | Investigate root cause, adjust CS playbooks for segment |
| Company growth/acquisition      | Customer doubles in size or acquires new business unit  | Scope segment framework refresh project                 |

**Every 6-12 Months:**

- Full Segment Recalibration: Revisit all dimensions, criteria, and thresholds against updated data
- New Dimension Assessment: Does the company now have behavioral data (from a new CSP) or usage data that would add a valuable dimension?
- Competitive Landscape Review: Has the customer's market changed enough to warrant industry segment adjustments?

---

### 4b. Internal Handoff (SME -> Architect)

> **Purpose:** Transfer context so Architect can manage ongoing relationship.

**What the Architect needs to know:**

- Segmentation framework rationale: why these dimensions were chosen, what alternatives were considered
- Data quality baseline: which fields had gaps, what enrichment was used, expected refresh cadence
- Common issues: enrichment match rate problems, CSP data sync delays, accounts that frequently bounce between segments
- Maintenance schedule: monthly and quarterly tasks with specific instructions

**Escalation guidelines:**

| Issue Type                                     | Who Handles                                      | Examples                                              |
| ---------------------------------------------- | ------------------------------------------------ | ----------------------------------------------------- |
| Small tweaks, minor questions                  | Architect                                        | Adjust a threshold, add a picklist value, fix a view  |
| Add new dimension, change assignment logic     | SME                                              | Add behavioral segmentation, restructure tier model   |
| Enrichment tool change or major data migration | SME                                              | Switch from ZoomInfo to Apollo, re-enrich all accounts |

**For Dedicated engagements:** Architect also receives the maintenance schedule (4a) and becomes responsible for executing monthly and quarterly tasks. SME walks Architect through each task.

---

### 4c. External Handoff

> **Purpose:** Formal project completion with customer.

**Final project meeting:**

- Review what was delivered: segmentation framework, CRM fields, automation, enrichment, dashboards
- Walk through documentation package
- Demo the maintenance tasks: show how to run data quality check, how to review segment distribution
- Confirm nothing outstanding
- Make it explicit: "Project complete"
- **For Single Project engagements:** Hand over the maintenance schedule and walk through each monthly and quarterly task

**Documentation package:**

- Segmentation Framework Document (final version with all dimensions, criteria, and operational actions)
- Definition Alignment Document (final signed version)
- All training video walkthrough recordings
- Segment Definitions Quick-Reference Card
- FAQ document
- Data Enrichment Process Guide
- Maintenance Schedule
- Support contact info

**For Single Project engagements:** Walk the customer through the maintenance schedule in detail. Record a video walkthrough of the session. Emphasize the quarterly segment review — this is what prevents segments from becoming stale.

**Output:** Customer owns the segmentation system. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location
- [ ] Handoff documentation complete
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized

#### Internal Debrief (Optional but Recommended)

- What went well? (e.g., enrichment tool selection, stakeholder alignment speed)
- What would we do differently? (e.g., data quality issues caught earlier, more CSM involvement in strategy)
- Any learnings to feed back into process documentation? (e.g., common dimension patterns for B2B SaaS CS teams)

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell -> Downsell -> Retry  |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (retainer) -- "We handle ongoing segment maintenance and optimization"
   | if no
2. Downsell: Customer Health Model project -- "Now that segments exist, add health scoring on top"
   OR: Renewal Management project -- "Use segments to drive differentiated renewal playbooks"
   | if yes
3. Retry retainer at end of next project cycle
```

**Script:**

> "Now that segmentation is live, there are two ways we can continue working together. Option 1: We handle ongoing segment optimization, data enrichment refreshes, and quarterly reviews as part of managed services. Option 2: We can build on this foundation with a Customer Health Model or Renewal Management project — both use segments as inputs. Which sounds more interesting?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On [date ~quarter out], we'll review how segments are performing — are they changing CS behavior, is the data staying clean, do any dimensions need adjustment?"

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                                          |
| ------------------- | --------------------------------------------------------------------- |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks                      |
| 2. Review metrics   | Pull segment distribution, dashboard usage, churn-by-segment data    |
| 3. Decide ownership | Can Architect handle this check-in, or need SME?                     |
| 4. Prep materials   | If SME needed, brief them. If Architect, prep talking points.         |

**At the refinement check-in:**

- Review segment distribution vs. baseline (has it drifted?)
- Check adoption metrics: Are CSMs still using segment views?
- Review churn and expansion by segment: Do segments predict outcomes?
- If minor adjustments: Architect handles threshold tweaks
- If major restructure: Scope new project

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- Segmentation Framework Document: Complete framework with 3-5 dimensions, criteria for each, naming conventions, and operational actions per segment
- Definition Alignment Document: Signed-off key term definitions
- Gap Analysis: Current state vs. future state segmentation comparison

**Technical Deliverables:**

- CRM segmentation fields with correct data types, picklist values, and field-level security
- Automated segment assignment rules (flows, formula fields, or workflow rules)
- Enriched customer data (firmographic fields populated to 80%+ via enrichment tools)
- Executive dashboard with segment distribution, performance comparison, and trending
- CSM list views and CSP workspace views filtered by segment
- Standard reports: Customers by Segment, ARR by Segment, Retention by Segment, Health by Segment, CSM Book by Segment

**Documentation Package:**

- Training video walkthrough recordings (model walkthrough, dashboard navigation, CSM workflow)
- Segment Definitions Quick-Reference Card
- FAQ document
- Data Enrichment Process Guide
- Maintenance Schedule (monthly + quarterly tasks)
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
| **Phase 1: Strategy**    | Signed-off segmentation framework + Definition Alignment Document      | All dimensions, criteria, and operational actions approved by CS leadership    |
| **Phase 2: Engineering** | Built segmentation system in CRM with enrichment and dashboards        | Fields, automation, enrichment, dashboards tested and customer-approved        |
| **Phase 3: Enablement**  | Trained CS team with documentation                                     | All training delivered, hypercare complete, >70% team adoption                |
| **Phase 4: Handoff**     | Independent customer + archived project                                | Maintenance plan in place, governance cadence set, project closed             |

### How to Adapt Per Project Type

Customer Segmentation is a Balanced project:

| Project Profile | Strategy Weight | Engineering Weight | Enablement Weight | Notes                                          |
| --------------- | --------------- | ------------------ | ----------------- | ---------------------------------------------- |
| **Balanced**    | 35-40%          | 30-40%             | 20-25%            | Strategy drives framework; engineering builds it; enablement drives adoption |

**Adaptation notes:**
- If customer has no enrichment needs (data is already clean and complete), Phase 2 compresses by 1-2 days
- If customer has a mature CSP with behavioral data, add a behavioral segmentation dimension (increases Phase 1 by 1 meeting, Phase 2 by 1-2 days)
- If customer already has informal segments they use, Phase 1 can move faster by validating existing model rather than building from scratch

### Phase 1: How We Create Value in Strategy

**1. We educate.** Most CS teams know they need segmentation but have not thought through what dimensions matter, how many segments are actionable, or how to prevent segments from going stale. We educate them on segmentation best practices so they can give informed input.

**2. We drive alignment.** CS, Sales, and Finance often have different ideas about what "Enterprise" means or how customers should be tiered. We force alignment via the Definition Alignment Document before building anything.

**3. We come with an opinion.** We arrive at kickoff with a v0 framework based on intake data and industry benchmarks. The customer reacts and refines — they don't start from a blank page.

**4. We show best practices.** We anchor recommendations in what we've seen work across similar B2B SaaS companies. Companies with 3-5 well-defined segments that drive differentiated treatment see measurably better retention outcomes than those with dozens of unused segments [1].

Segmentation projects fail when teams build segments that no one uses. Phase 1 prevents this by connecting every segment dimension to a specific operational action before a single field is created in CRM.

### Phase 2: Key Principles

**Tech Spec (2a):** The framework-to-CRM translation is where most technical risk lives. Automation logic must handle nulls, conflicts, and edge cases explicitly. Do not assume clean data.

**Engineering Handoff (2b):** Engineer needs to understand the strategic "why" — not just "create this field," but "this field drives how CSMs prioritize their book of business."

**Build (2c):** Build fields first, then enrich, then automate, then dashboard. This sequence ensures each step has the data it needs. Running enrichment before fields exist creates import errors.

### Phase 3: Key Principles

**Training Prep (3a):** Draft materials from project docs. Architect reviews and customizes for this customer's specific segments and terminology.

**Training Sessions (3b):** Split by audience. Leadership cares about "what does segment performance tell me?" CSMs care about "how do I filter my accounts?" CS Ops cares about "how do I maintain this?"

**Hypercare (3c):** Office hours pattern works well for segmentation because the edge cases emerge organically as CSMs start using segments daily. First 2 weeks surface 80% of the "why is this account in the wrong segment?" questions.

### Phase 4: Why Maintenance Schedules Matter

The most common failure mode for customer segmentation projects is not a broken system — it's a system that becomes irrelevant because segments go stale. B2B market conditions and customer profiles shift continuously, and existing segments can become obsolete without active maintenance [3]. The maintenance schedule prevents drift by making monitoring explicit and cadenced.

Customer Segmentation is a natural gateway to Customer Health Model and Renewal Management projects. Once segments exist, health scoring and renewal playbooks become significantly more valuable because they can be differentiated by segment. Customer-centric companies grow revenues 4-8% faster than competitors [5], and segmentation is the foundation that makes customer-centric operations possible.

---

## References

[1] [Salesforce - What is Customer Segmentation?](https://www.salesforce.com/sales/sales-planning/customer-segmentation/)
[2] [ChurnZero - The Customer Success Guide to Smart Segmentation](https://churnzero.com/guides/smart-segmentation-guide/)
[3] [Infiniti Research - Top Challenges in B2B Market Segmentation](https://www.infinitiresearch.com/thoughts/challenges-b2b-market-segmentation/)
[4] [UserMaven - How to Do B2B Customer Segmentation](https://usermaven.com/blog/how-to-do-b2b-customer-segmentation)
[5] [OnRamp Funds - Customer Segmentation for ROI Growth](https://www.onrampfunds.com/resources/customer-segmentation-for-roi-growth)
