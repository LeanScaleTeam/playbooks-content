## Project One-Pager

### Lead Routing One-Pager

#### Project Type

- Category: Technical / Balanced (depends on approach -- Round Robin is light, Territory-Based is heavy)
- Primary Deliverable: Active routing system in CRM or dedicated tool that automatically assigns incoming leads to the right person based on predefined rules

##### Phase Relevance

| Phase          | Applies? | Weight      | Notes                                                                 |
| -------------- | -------- | ----------- | --------------------------------------------------------------------- |
| 1. Strategy    | Yes      | Medium      | Approach selection, hierarchy design, tool selection (1-2 meetings)   |
| 2. Engineering | Yes      | Heavy       | Build routing flows, configure tools, QA test scenarios               |
| 3. Enablement  | Yes      | Light-Med   | Train ops team on updates, train reps on routing logic                |
| 4. Handoff     | Yes      | Medium-Heavy| Ongoing maintenance is significant for territory-based                |

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │    Medium    │     │    Heavy     │     │   Light-Med  │     │  Med-Heavy   │
  │ 1a→1b→1c→1d │     │ 2a→2b→2c→2d │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   Approach selection   Build routing flows  Train ops + reps     Ongoing maintenance
   1-2 meetings         Configure + QA       on routing logic     significant at scale
```

**This project's flow:**
- Full 4-phase. Phase 2 (Engineering) carries the most weight -- the build varies significantly by approach.
- Three build paths exist: Round Robin (lightest), Territory-Based (heaviest), Target Account/Hybrid (medium).
- Phase 1 may compress to 1 meeting if approach is obvious (e.g., small flat team = Round Robin).
- Phase 3c (Hypercare) is 1-2 weeks for territory-based, may skip for Round Robin.
- Phase 4 maintenance intensity varies: minimal (Round Robin) to 40+ hours/month (Territory-Based at scale).

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Watch intro video: what lead routing is, why it matters, and the three approach options
- [ ] Complete intake form: team size, team structure, deal volume, deal size, CRM platform, existing routing, PTO handling
- [ ] Confirm whether Sales Territory project is complete (required for Territory-Based and Target Account approaches)
- [ ] Provide territory hierarchy document if available (from Sales Territory project)
- [ ] Identify who will manage ongoing routing changes post-launch

##### Track B: Architect Prep
- [ ] Review intake form and identify likely approach (Round Robin / Territory-Based / Target Account)
- [ ] Pull CRM data: current lead assignment fields, existing automation, team roster
- [ ] If Territory-Based: review territory hierarchy from Sales Territory project
- [ ] Prepare approach recommendation with rationale
- [ ] Draft Definition Alignment Document with key terms pre-filled

#### Refinement Loop (1b &rarr; 1c &rarr; 1d)

| Meeting   | Sub-Phase | Focus                                              | Stakeholder                   | Output                            |
| --------- | --------- | -------------------------------------------------- | ----------------------------- | --------------------------------- |
| Kickoff   | 1b        | Present approach recommendation, validate scoping  | Sales Leadership + RevOps     | Confirmed approach + tool choice  |
| Design    | 1c        | Review routing hierarchy, define rules and fallback | RevOps + CRM Admin            | Routing spec document             |
| Sign-Off  | 1d        | Approve routing spec, confirm build readiness       | Sales Leadership + RevOps     | Signed-off routing spec           |

Note: For Round Robin, Meetings 1 and 2 often combine into a single session. Territory-Based may need an additional design session for complex hierarchies.

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held -- approach confirmed
- [ ] 1c. Routing hierarchy and rules designed (if Territory-Based/Target Account)
- [ ] 1d. Strategic sign-off obtained -- routing spec approved

##### Phase 2: Engineering
- [ ] 2a. Tech spec created (routing flow logic, field mappings, tool config)
- [ ] 2b. Engineering handoff meeting held
- [ ] 2c. Build complete (flows built in INACTIVE state)
- [ ] 2d. QA/Test complete + customer sign-off on test results

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped (per approach)
- [ ] 3b. Training sessions delivered (ops team + client team)
- [ ] 3c. Hypercare period complete (1-2 weeks for Territory-Based; may skip for Round Robin)
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff complete
- [ ] 4c. External handoff (LeanScale &rarr; Customer) complete
- [ ] 4d. Project closed and archived

#### Document Types

##### Working Documents (iterate together)

| Document                        | Purpose                                               | When Complete                                      |
|---------------------------------|-------------------------------------------------------|----------------------------------------------------|
| Intake form                     | Capture scoping inputs (team size, structure, volume)  | All fields filled, approach selected               |
| Routing spec / hierarchy design | Define routing logic, decision nodes, fallback rules   | All branches documented, override logic defined     |
| Territory assignment table      | Map territories to owners (Territory-Based/Target)     | All territories assigned, reviewed by sales leadership |

##### Deliverables (polished outputs)

| Deliverable                     | Created From                   | Customer Uses For                              |
|---------------------------------|--------------------------------|------------------------------------------------|
| Active routing flow             | Routing spec                   | Automated lead assignment                      |
| Routing hierarchy diagram       | Routing spec                   | Internal documentation, onboarding new reps     |
| Territory object (if SF)        | Territory assignment table     | Code-free territory updates                     |
| Change log template             | Maintenance schedule           | Tracking routing changes over time              |

#### Enablement Details

##### Training Types

| Type       | Audience                          | Focus                                                         | Duration |
| ---------- | --------------------------------- | ------------------------------------------------------------- | -------- |
| Client Team| Sales reps, SDRs/BDRs, AEs       | What determines their assignments, how to flag misrouted leads | 30 min   |
| Ops Team   | RevOps, CRM Admin                 | How to make routing updates, change log process, PTO handling  | 60 min   |
| Leadership | Sales Leadership                  | How routing works, how to request territory changes            | 30 min   |

##### Hypercare
- Applies: Yes for Territory-Based / Target Account; Optional for Round Robin
- Duration: 1-2 weeks (Territory-Based), 1 week (Target Account), skip or 3 days (Round Robin)
- Office Hours: Yes -- weekly 30-min slot during hypercare

##### Training Assets to Create
- [ ] Video walkthrough: Routing logic walkthrough (how the flow works end-to-end)
- [ ] Video walkthrough: How to make common updates (add/remove rep, PTO handling)
- [ ] Doc: Change log template with instructions
- [ ] Doc: QA checklist for ongoing routing validation

#### Handoff & Retention

##### Internal Handoff
- Key context for Architect: Which approach was implemented, maintenance level required, key edge cases encountered
- Escalation trigger: Any routing logic changes, territory restructuring, or tool migration

##### External Handoff (LeanScale &rarr; Customer)
- Final meeting agenda: Walk through routing logic, demonstrate common updates, set maintenance expectations
- Documentation package: Routing hierarchy diagram, training recordings, change log template, QA checklist, maintenance schedule

##### Maintenance Schedule
- See Phase 4a below for full schedule
- Round Robin: As needed when team changes
- Territory-Based: Can require daily/weekly updates at scale; quarterly territory rebalancing
- Target Account: As needed when named account list changes
- Who owns: Single project = customer owns | Dedicated = Architect owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services (routing maintenance retainer) &rarr; if no &rarr; Downsell: Sales Territory project or Speed to Lead project &rarr; Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~1 quarter after go-live
- Decision: Architect handles if minor tweaks / specialist needed if territory restructuring

#### Definition Alignment Terms

| Term                  | Typical Definition                                                                                   |
| --------------------- | ---------------------------------------------------------------------------------------------------- |
| Territory             | A defined segment of the market (by geography, industry, company size, or product) assigned to a specific rep or team |
| Named Account         | A specific company explicitly assigned to a particular rep, regardless of territory rules              |
| Routing Node          | A decision point in the routing flow where lead criteria are evaluated against a rule                  |
| Assignment Rule       | The logic that determines which rep receives a lead (e.g., territory match, round robin rotation)     |
| Round Robin           | A rotation-based assignment method where leads distribute evenly across a pool of reps                |
| Fallback Routing      | The default path a lead follows when it does not match any defined routing criteria                    |
| Override              | A manual flag that bypasses automated routing and preserves the current lead owner                     |
| Territory Object      | A custom Salesforce object that stores territory definitions and assignments as records -- acts as a "Vlookup table" the routing flow references |
| Routing Hierarchy     | The ordered sequence of criteria (e.g., Federal overlay &rarr; Enterprise/SMB &rarr; Geography &rarr; Industry &rarr; Assignment) that determines how a lead is evaluated |

#### Common Gotchas

- **Missing routing criteria** -- A lead comes in that does not match any defined territory or rule. Always build a fallback/default path. Real example: a lead from a financial services company got routed to a team that sells electric trucks -- because no routing criteria existed for that segment.
- **PTO handling gaps** -- Without a dedicated tool, PTO requires manual flow edits or record updates. LeanData automates this via calendar integration.
- **Team changes not reflected** -- Every hire or departure requires immediate routing updates. Stale routing = leads going to inactive users.
- **Stale enrichment data** -- If upstream enrichment (Automated Inbound project) provides bad data, routing decisions are wrong. Verify enrichment pipeline health before blaming routing.
- **Override conflicts** -- Manual overrides can conflict with automated routing. Build override logic explicitly: the flow checks for an override flag first -- if true, it leaves the current owner in place.
- **No Sales Territory project completed** -- Territory-Based and Target Account routing cannot work without territory definitions. Either complete the Sales Territory project first or fall back to Round Robin.
- **Underestimating maintenance** -- Territory-based routing at scale can require 40+ hours/month of ongoing maintenance. Set this expectation in Phase 1.

#### Methodology Options

| Option                              | When to Use                                                    | Complexity | Sales Territory Required? |
| ----------------------------------- | -------------------------------------------------------------- | ---------- | ------------------------- |
| Round Robin                         | High volume, low ACV, flat team (&lt;10), no territory design     | Low        | No                        |
| Territory-Based (CRM-native)        | &lt;10 reps, clear segments, stable team, budget-conscious        | Medium     | Yes                       |
| Territory-Based (SF Custom Object)  | &lt;10 reps, want code-free updates, transition from Round Robin  | Medium     | Yes                       |
| Territory-Based (LeanData)          | 10+ reps, frequent changes, PTO automation needed              | High       | Yes                       |
| Target Account / Hybrid             | Named accounts need dedicated owners + fallback for the rest   | Medium-High| Yes                       |

**Decision shortcut:**
- "Is your team flat or specialized?" -- Flat = Round Robin viable; Specialized = Territory-Based
- "Do you have named accounts that need specific owners?" -- Yes = Target Account approach
- "Has territory design been completed?" -- No = Round Robin or do Sales Territory first
- "How many people need routing?" -- 10+ = Consider dedicated tool regardless of approach

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on the routing approach, tool selection, and routing hierarchy design.
>
> **Output:** Confirmed approach + approved routing spec document.

### 1a. Pre-Kickoff

> Two parallel tracks run after the deal closes and before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                        | Format             |
| ----------------------------- | -------------------------------------------------------------- | ------------------ |
| Intro video                   | Explain what lead routing is, the three approaches, and why territory definitions matter | Video walkthrough (5-10 min)    |
| Definition Alignment Document | Get stakeholder sign-off on routing terms (territory, named account, routing node, etc.) | Google Doc         |
| Pre-filled intake form        | Confirm team size, structure, deal volume, CRM, Sales Territory status | Google Form or Doc |

**Completion tracking:** RevOps contact owns filling out the intake form. Do not cancel kickoff if incomplete, but push for territory hierarchy document before the design meeting.

#### Track B: Architect Prep

| Step | Action                                                                    | Output                                |
| ---- | ------------------------------------------------------------------------- | ------------------------------------- |
| 1    | Review intake form responses and Sales Territory project status           | Scoping assessment                    |
| 2    | Identify likely approach (Round Robin / Territory-Based / Target Account) | Approach recommendation with rationale |
| 3    | If Territory-Based: review territory hierarchy from Sales Territory project | Understanding of routing nodes needed |
| 4    | Assess tool requirements (CRM-native vs. dedicated tool)                  | Tool recommendation                   |
| 5    | Prepare kickoff presentation with approach recommendation                 | Kickoff assets                        |

**Critical:** Mark everything as ASSUMED. The kickoff call validates.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on routing terms BEFORE building anything.

| Term                  | Our Definition                                                                       | Internally Approved? |
| --------------------- | ------------------------------------------------------------------------------------ | -------------------- |
| Territory             | A defined market segment (geography, industry, size, product) assigned to a rep/team | [ ] Yes / [ ] No     |
| Named Account         | A specific company assigned to a particular rep regardless of territory rules         | [ ] Yes / [ ] No     |
| Routing Hierarchy     | The ordered sequence of criteria used to evaluate and assign incoming leads           | [ ] Yes / [ ] No     |
| Round Robin           | Rotation-based assignment distributing leads evenly across a rep pool                | [ ] Yes / [ ] No     |
| Fallback Routing      | Default path for leads that do not match any defined routing criteria                 | [ ] Yes / [ ] No     |
| Override              | Manual flag that bypasses automated routing                                          | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your sales leadership team. Check "Yes" when approved. These definitions determine how the routing system will behave. Misalignment here = misrouted leads later.

---

### 1b. Kickoff Call

> **Purpose:** Present approach recommendation and get alignment. We walk in with a recommendation -- customer reacts, not creates from scratch.

#### Agenda (60 min)

| Time  | Topic                         | What Happens                                                                         |
| ----- | ----------------------------- | ------------------------------------------------------------------------------------ |
| 0-15  | Walk through recommendation   | "Based on your team size, structure, and volume, we recommend [approach] because..." |
| 15-30 | Validate scoping factors      | Confirm team size, structure, deal volume, deal size, named account needs             |
| 30-40 | Confirm approach + tool       | Final approach decision. If dedicated tool needed, initiate procurement.              |
| 40-50 | Definition alignment          | Review Definition Alignment Document                                                 |
| 50-60 | Next steps                    | Assign homework (territory hierarchy, named account list), schedule design meeting    |

#### What We Bring

- Approach recommendation with rationale (built in Track B prep)
- Scoping factor assessment table
- Definition Alignment Document (pre-filled)
- Questions list: territory status, PTO handling, override needs

#### What We Leave With

- Confirmed approach (Round Robin / Territory-Based / Target Account)
- Tool decision (CRM-native / SF Custom Object / LeanData / Chili Piper)
- Homework assigned: territory hierarchy document, team roster, named account list (as applicable)
- Design meeting scheduled

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Design the routing hierarchy and rules. For Round Robin, this may happen in the kickoff call itself.

#### The Pattern

```
Kickoff Call (confirm approach + tool)
    |
    v
Customer provides territory hierarchy / team roster / named account list
    |
    v
Meeting 2: Design Review
  - Review routing hierarchy and decision nodes
  - Define fallback routing path
  - Confirm override logic
  - Document routing spec
    |
    v
Architect creates tech spec from routing spec
    |
    v
Build begins
```

**For Round Robin:** The design meeting often collapses into the kickoff call. Team roster + exclusion rules are the only inputs needed.

**For Territory-Based:** The design meeting is critical. Walk through the full routing hierarchy: which criteria get checked first, second, third. Example hierarchy: Federal (overlay) &rarr; Enterprise/SMB split &rarr; Geography &rarr; Industry &rarr; Assignment.

**For Target Account:** Two-part design: (1) named account check logic, (2) fallback approach design (territory or round robin).

#### Information Needed Before Design Meeting

**For Round Robin:**
- Team roster (who is in the rotation)
- Any exclusion rules needed
- Tool of choice (CRM assignment rules, HubSpot workflow, Calendly)

**For Territory-Based (assumes Sales Territory complete):**
- Territory hierarchy document (from Sales Territory project)
- Territory assignments (who owns what)
- SDR/AE split logic if applicable
- Override requirements

**For Target Account:**
- Named account list with assigned owners
- Fallback approach decision (territory-based or round robin)

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything before building.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by sales leadership
- [ ] Approach confirmed: Round Robin / Territory-Based / Target Account
- [ ] Tool confirmed: CRM-native / SF Custom Object / LeanData / Chili Piper
- [ ] Routing hierarchy designed and documented (if Territory-Based / Target Account)
- [ ] Fallback routing path defined
- [ ] Override requirements documented
- [ ] Team roster / territory assignments / named account list provided
- [ ] Sales Territory project status confirmed (complete OR not required for Round Robin)
- [ ] No blockers for engineering

#### Decision Point

- **Proceed to Engineering** &rarr; Build the routing system
- **Pause: Sales Territory needed** &rarr; Territory-Based or Target Account requested but territory design is not complete. Recommend completing Sales Territory project first, or scope Round Robin as an interim solution.

---

## Phase 2: Engineering

> **Goal:** Build and test the routing system based on the approved routing spec.
>
> **Output:** Active routing system, tested and customer-approved.

| Approach        | Engineering Weight | Notes                                           |
| --------------- | ------------------ | ----------------------------------------------- |
| Round Robin     | Light (20-30%)     | Simple rotation config, minimal flow logic       |
| Territory-Based | Heavy (60-80%)     | Complex flow with decision nodes, object config  |
| Target Account  | Medium (40-60%)    | Named account check + fallback routing           |

### Sub-Phases

```
2a Tech Spec -> 2b Engineering Handoff -> 2c Build -> 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate the routing spec into technical specifications for the build.

**Input:** Signed-off routing spec from Phase 1

**Output:** Draft tech spec containing:

- Tool and platform configuration details (which CRM, which tool)
- Routing flow logic (decision nodes, branching, assignment actions)
- Field mappings (which lead fields drive routing decisions)
- Object design (if using Salesforce Custom Object approach)
- Override logic specification
- Fallback routing specification
- Build sequence (what to build first)

**For Round Robin:**
- Rotation pool members
- Distribution method (equal vs. weighted)
- Out-of-office handling method
- Tool-specific configuration (Salesforce assignment rules, HubSpot workflow rotation, Calendly settings)

**For Territory-Based (SF Custom Object):**
- Custom object schema: Territory name, criteria fields (size, geography, industry, product), assigned team members (AE, SDR, etc.)
- Flow logic: how the flow pings the object to find a matching record
- Hierarchy of decision nodes

**For Territory-Based (LeanData):**
- LeanData flow configuration spec
- Node types and routing logic
- Availability/PTO calendar integration setup

**For Target Account:**
- Named account matching logic (first node: is this a target account?)
- Fallback routing spec (territory or round robin)
- Override logic for named accounts

---

### 2b. Engineering Handoff

> **Purpose:** Review tech spec with engineer before building.

**Who attends:** Architect + Engineer (or CRM admin)

**Agenda (30-45 min):**

| Time  | Topic              | What Happens                                               |
| ----- | ------------------ | ---------------------------------------------------------- |
| 0-15  | Walk through spec  | Architect explains routing hierarchy, approach, and tool choices  |
| 15-30 | Engineer questions  | Clarify flow logic, flag CRM-specific risks, confirm access |
| 30-45 | Refine and approve  | Adjust spec, confirm build sequence                         |

**What Architect brings:**
- Routing spec (from Phase 1)
- Draft tech spec (from 2a)
- CRM access confirmation
- Tool licenses confirmed (if dedicated tool)

**What engineer leaves with:**
- Approved tech spec
- Clear build sequence
- Known dependencies (e.g., Sales Territory object exists, LeanData license provisioned)

---

### 2c. Build

> **Purpose:** Build the routing system in the customer's CRM or dedicated tool.

**Input:** Approved tech spec from 2b

**CRITICAL:** All routing flows are built in INACTIVE state first. Activation happens only after QA is complete and customer has signed off.

#### Build Path A: Round Robin

No Sales Territory prerequisite required.

**Step 1:** Select tool based on CRM:
- Salesforce: Assignment rules or Flow-based rotation
- HubSpot: Workflow-based rotation
- Standalone: Calendly round robin

**Step 2:** Identify rotation pool:
- List all team members to include
- Document any exclusion criteria (specific lead types, etc.)

**Step 3:** Configure rotation settings:
- Equal distribution vs. weighted
- Queue order (alphabetical, random, etc.)

**Step 4:** Set up out-of-office handling:
- Manual exclusion process OR
- Calendar integration if tool supports

**Step 5:** Test rotation:
- Create test leads
- Verify distribution is working as expected

**Step 6:** Document maintenance process:
- How to add new team members
- How to remove departed team members
- How to handle temporary exclusions (PTO)

#### Build Path B: Territory-Based

Requires Sales Territory project to be complete.

**Step 1:** Gather territory design from Sales Territory project:
- Territory hierarchy (what gets checked first, second, third)
- Territory definitions (geography, size, industry, product)
- Territory assignments (who owns what)

**Step 2:** Select tool based on complexity:
- &lt;10 reps: CRM-native flows (Salesforce Flow, HubSpot Workflow)
- 10+ reps: LeanData or Chili Piper

**Step 3:** IF using CRM-native, decide on implementation approach:
- **Hardcoded:** Decision nodes directly in flow (simpler but harder to maintain)
- **Salesforce Custom Object (recommended):** Create "Vlookup table" that flow references

> The reason for the Custom Object approach is to make it easy to manage territories from a code-free perspective. With hardcoded logic, any team change requires editing a Salesforce workflow. With the territory object, anyone can update the account team seller assignment in the record and the routing updates automatically.

**Step 4:** IF using Salesforce Custom Object approach:
- Create custom object to store territory records
- Each record contains: Territory name, criteria fields (size, geography, industry), assigned team members
- Think of it as a list of all possible territories and the factors that determine assignment
- Flow pings object to find matching record rather than hardcoding assignments

> Instead of using routing via traditional Salesforce infrastructure, the flow pings the object first, finds the matching territory record, and assigns the team -- setting the right person and tagging everyone automatically.

**Step 5:** Build routing flow in INACTIVE state:
- Create decision nodes matching territory hierarchy
- Example hierarchy: Federal (overlay) &rarr; Enterprise/SMB split &rarr; Geography &rarr; Industry &rarr; Assignment
- Each branch ends with owner assignment (or object lookup)

**Step 6:** Add override logic if required:
- Manual override checkbox that bypasses routing
- The flow checks for an override flag -- if true, it leaves the current owner in place

**Step 7:** Build fallback/default routing:
- What happens if no criteria match?
- Default assignment queue or round robin fallback
- Every lead should be assigned -- nothing should fall through untouched

**Step 8:** Test routing flow (see 2d for full QA)

**Step 9:** Review with client:
- Walk through inactive flow
- Demonstrate test records routing correctly
- Use CRM test functionality to trace each record's path

#### Build Path C: Target Account / Hybrid

Requires Sales Territory project to be complete.

**Step 1:** Gather inputs:
- Named account list with assigned owners
- Fallback approach decision (territory-based or round robin)

**Step 2:** Select tool:
- Simple hybrid: CRM-native
- Complex: LeanData

**Step 3:** Build routing flow in INACTIVE state:
- First node: Is this a target/named account?
  - YES &rarr; Route to assigned owner
  - NO &rarr; Continue to fallback

**Step 4:** Build fallback routing:
- IF fallback is territory-based &rarr; Follow Build Path B steps for the fallback path
- IF fallback is round robin &rarr; Follow Build Path A steps for the fallback path

**Step 5:** Add override logic for named accounts:
- The flow checks for an override flag -- if true, it leaves the current owner in place

**Step 6:** Test routing flow (see 2d for full QA)

**Step 7:** Review with client

**Build tracking:**

- [ ] Routing flow: [approach] -- [status]
- [ ] Fallback routing: [status]
- [ ] Override logic: [status]
- [ ] Territory object (if applicable): [status]
- [ ] Named account matching (if applicable): [status]

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify the routing system works correctly before activation.

**Two types of testing:**

| Type              | Who      | Purpose                                              |
| ----------------- | -------- | ---------------------------------------------------- |
| Technical Testing | Our team | Verify flow logic, routing paths, edge cases         |
| Customer Testing  | Customer | Verify leads route to correct people per their rules |

**Testing process:**

**Step 1:** Run test records through the flow -- use CRM test functionality to trace each record's path. Document results for each test case.

**Step 2:** Address any issues found -- adjust flow logic, re-test.

**Step 3:** Create QA checklist for ongoing use (especially for Territory-Based).

**QA Checklist by Approach:**

**Round Robin:**
- [ ] Multiple sequential leads distribute evenly across rotation pool
- [ ] Excluded members do not receive leads
- [ ] New members successfully added to rotation
- [ ] Out-of-office exclusions work correctly
- [ ] Distribution resets properly after member changes

**Territory-Based:**
- [ ] Every territory/region routes correctly
- [ ] Size tier splits work (leads above/below thresholds go to right teams)
- [ ] Override logic respects manual assignments
- [ ] Fallback routing catches unmatched leads
- [ ] No leads fall through without assignment
- [ ] Custom object updates reflect correctly in assignments (if using that approach)
- [ ] Test with records that match each major branch of the decision tree
- [ ] Test with records that match NO branch (verify fallback)

**Target Account:**
- [ ] Named accounts route to correct assigned owners
- [ ] Non-named accounts fall back correctly (to territory or round robin)
- [ ] Override functionality works
- [ ] New named account additions route correctly
- [ ] Removed named accounts fall to default routing

**Engineering sign-off checkpoint:**

- [ ] Built system matches routing spec from Phase 1
- [ ] All QA test cases passing
- [ ] Customer has reviewed test results and approved
- [ ] Ready for activation and enablement

**Decision point:**

- **Proceed to Enablement** &rarr; System is built, tested, ready to activate
- **Loop back to Build** &rarr; Issues found, needs fixes

---

## Phase 3: Enablement

> **Goal:** Customer team can operate and maintain the routing system independently.
>
> **Output:** Trained team with documentation, stabilized system after initial go-live.

### Sub-Phases

```
3a Training Prep -> 3b Training Sessions -> 3c Hypercare -> 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials customized for the approach that was built.

**Input:** Routing spec + tech spec + built system

**Output:** Training package containing:

- Video walkthrough scripts for routing walkthrough (approach-specific)
- Written guide for common updates (add/remove rep, PTO, named account changes)
- Change log template with instructions (for Territory-Based)
- QA checklist for ongoing validation

**Materials vary by approach:**

| Approach        | Key Training Material                                                |
| --------------- | -------------------------------------------------------------------- |
| Round Robin     | How to add/remove from rotation, PTO exclusion steps                  |
| Territory-Based | How to update territory object or request flow changes, change log process |
| Target Account  | How to update named account list, manage fallback routing             |

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge so the customer team understands and can maintain routing.

**Two training tracks:**

**Track 1: Client Team Training (30 min)**
- What determines their lead assignments
- How to identify and report a misrouted lead
- Who to contact for routing issues

**Track 2: Ops Team Training (60 min)**

Training content varies by approach:

- **Round Robin:** How to add/remove members from rotation
- **Territory-Based (Custom Object):** How to update territory object without code changes -- go into the object and update the account team seller assignment directly
- **Territory-Based (Hardcoded):** How to request flow changes from CRM admin
- **Territory-Based (LeanData):** How to use the LeanData UI for routing updates
- **Target Account:** How to update the named account list and owner assignments

**Additional training:**
- **Sales leadership:** How to request territory changes (coordinate with Sales Territory)
- **Reps:** Understanding how routing affects their assignments

**Output:**
- Trained stakeholders
- Video recordings of training sessions
- Questions log (feeds into FAQ)

---

### 3c. Hypercare

> **Purpose:** Intensive post-launch support to catch edge cases with real leads.

**Duration by approach:**

| Approach        | Hypercare Duration | What to Watch For                                      |
| --------------- | ------------------ | ------------------------------------------------------ |
| Round Robin     | 3-5 days (light)   | Even distribution, exclusion rules working              |
| Territory-Based | 1-2 weeks          | Edge cases with real leads, unmatched routing criteria   |
| Target Account  | 1 week             | Named account matching accuracy, fallback behavior       |

**What happens:**
- Monitor first batch of real leads routed through the system
- Watch for routing failures or unexpected assignments
- Track if any leads fall through without assignment
- Address edge cases that surface with real data (vs. test data)
- Quick response to issues via scheduled office hours

**Go-live coordination:**
- Coordinate activation timing -- do not activate during high-volume periods
- Activate flow/rotation
- Watch first batch of leads and verify behavior matches expectations
- Communicate to team: how routing now works, who to contact for issues

**Output:** Stabilized system, no critical issues outstanding

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm customer can operate independently.

**Validation checkpoint:**

- [ ] All training sessions delivered
- [ ] Training video recordings provided
- [ ] Change log template delivered (Territory-Based)
- [ ] QA checklist provided for ongoing validation
- [ ] Hypercare period complete (if applicable)
- [ ] No critical routing issues outstanding
- [ ] Ops team can make common updates without LeanScale support
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** &rarr; Customer is enabled, project wrapping up
- **Extend Hypercare** &rarr; Routing issues still surfacing, needs more support time

---

## Phase 4: Handoff

> **Goal:** Clean project close with maintenance plan established and retention/expansion path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the routing system, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule -> 4b Internal Handoff -> 4c External Handoff -> 4d Project Close
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At                                                                         |
| ----------------------------- | -------------------- | ------------------------------------------------------------------------------------- |
| **Single Project**            | Customer owns        | 4c (External Handoff) -- customer receives maintenance schedule and runs it themselves |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) -- Architect receives maintenance schedule and runs it for customer |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention -- cadences, tasks, triggers for re-engagement. Lead routing is one of the most maintenance-intensive project types, especially Territory-Based.

#### Maintenance Level by Approach

| Approach        | Maintenance Level | Key Ongoing Tasks                                          |
| --------------- | ----------------- | ---------------------------------------------------------- |
| Round Robin     | Minimal           | Add/remove from rotation as team changes                    |
| Territory-Based | High              | Change logs, PTO coverage, new hires/departures, territory rebalancing |
| Target Account  | Medium            | Named account list updates + fallback routing maintenance    |

> At scale, territory-based routing can consume 40+ hours/month of ongoing maintenance -- with a working change log document updated daily with patch notes.

#### Immediate (First 1-2 Weeks Post-Launch)

| Task                              | What to Check                          | Red Flag Threshold                             |
| --------------------------------- | -------------------------------------- | ---------------------------------------------- |
| Routing accuracy spot check       | Are leads going to the right people?   | Any systematic misrouting pattern               |
| Fallback/default routing check    | Are unmatched leads being caught?      | Any leads falling through with no assignment    |
| Distribution balance (Round Robin) | Is rotation distributing evenly?       | &gt;20% imbalance between reps                    |
| Edge case log                     | What scenarios surfaced with real data? | Any scenario not covered in original QA         |

#### Monthly Tasks

| Monthly Task                       | What to Check                            | Red Flag Threshold                         |
| ---------------------------------- | ---------------------------------------- | ------------------------------------------ |
| Routing health check               | Review routing failures or misassignments | Any increase in misrouted leads             |
| Team roster validation             | Confirm all active reps are in routing    | Any inactive users still receiving leads    |
| Change log review (Territory-Based)| Review changes made since last check      | Undocumented changes found                  |

#### Quarterly Tasks

| Quarterly Task                      | What to Review                            | Action if Off-Track                           |
| ----------------------------------- | ----------------------------------------- | --------------------------------------------- |
| Territory rebalancing assessment    | Distribution fairness across territories   | Coordinate with Sales Territory for rebalance  |
| Tool evaluation                     | Is current tool still sufficient?          | If team has grown past tool's capacity, scope migration |
| PTO handling review                 | Is current PTO process working?            | If manual process is failing, evaluate LeanData |

#### Common Maintenance Scenarios

**New hire:**
- Round Robin: Add to rotation pool
- Territory-Based: Add to territory assignments (object or flow), may require territory rebalancing (coordinate with Sales Territory)
- Target Account: Add to named account assignments if applicable

**Departure:**
- Round Robin: Remove from rotation
- Territory-Based: Remove from assignments immediately, redistribute territory coverage
- Target Account: Reassign named accounts, update all hardcoded references

**PTO:**
- Round Robin: Temporary exclusion from rotation (usually manual)
- Territory-Based (CRM-native): Manual exclusion or temporary assignment update
- Territory-Based (LeanData): Automated via calendar integration -- connects to availability calendar and automatically shuts off routing when someone is on PTO
- Target Account: Coverage assignment for named accounts during absence

#### Refinement Triggers (when to re-engage LeanScale)

| Trigger                            | Threshold                                   | Response                                                      |
| ---------------------------------- | ------------------------------------------- | ------------------------------------------------------------- |
| Team size crosses 10 reps          | Currently on CRM-native, growing past 10    | Scope dedicated tool migration (LeanData)                     |
| Maintenance hours exceeding budget | Ops team spending &gt;10 hrs/month on routing  | Evaluate tool upgrade or process simplification                |
| Territory restructuring            | Major reorg, new segments, market expansion  | Re-engage for Sales Territory + Lead Routing refresh           |
| Routing failure rate increasing    | &gt;5% of leads misrouted in a month           | Diagnose root cause: data quality, stale rules, or tool limits |

#### Review Cadence Summary

- **Round Robin:** As needed when team changes
- **Territory-Based:** Immediate (first 1-2 weeks), regular (every significant team change), periodic (quarterly for rebalancing), for mature implementations daily/weekly
- **Target Account:** As needed when named account list changes

---

### 4b. Internal Handoff

> **Purpose:** Transfer context so Architect can manage ongoing relationship.

**What the Architect needs to know:**

- Which approach was implemented and why (Round Robin / Territory-Based / Target Account)
- Maintenance intensity expectation (minimal for Round Robin, significant for Territory-Based)
- Key edge cases that were encountered and how they were resolved
- Customer contacts: who manages routing day-to-day, who approves territory changes
- When to escalate back to the specialist

**Escalation guidelines:**

| Issue Type                              | Who Handles           | Example                                                   |
| --------------------------------------- | --------------------- | --------------------------------------------------------- |
| Add/remove rep from routing             | Architect / Customer ops | New hire needs to be added to Round Robin                  |
| Territory assignment update             | Architect / Customer ops | Rep X now owns California instead of Rep Y                 |
| Routing logic changes                   | Specialist            | Add new routing branch for new product line                |
| Tool migration (CRM-native &rarr; LeanData) | Specialist            | Team has grown past 10, need dedicated tool                |
| Territory restructuring                 | Specialist            | Major reorg requires hierarchy redesign                    |

**For Dedicated engagements:** Architect also receives the maintenance schedule (4a) and becomes responsible for executing it.

---

### 4c. External Handoff (LeanScale &rarr; Customer)

> **Purpose:** Formal project completion with customer.

**Deliverables by approach:**

**Round Robin:**
- Configured rotation in tool of choice
- Documentation of rotation pool and exclusion rules
- Maintenance guide (how to add/remove, handle PTO)

**Territory-Based:**
- Active routing flow/workflow in CRM or dedicated tool
- Routing hierarchy documentation (diagram) if complex
- Territory object and assignments (if Salesforce Custom Object approach)
- Test documentation showing QA scenarios validated
- Change log template
- Maintenance guide with update procedures

**Target Account:**
- Active routing flow with named account check and fallback
- Named account list with owner assignments
- Fallback routing documentation
- Maintenance guide for named account updates

**Final project meeting agenda:**
- Walk through the routing logic and how decisions are made
- Demonstrate how to make common updates (live, in their instance)
- Explain what happens in edge cases (fallback, override, PTO)
- Set expectations for ongoing maintenance needs
- Identify who owns routing going forward
- Make it explicit: "Project complete"

**Documentation package:**
- Training video recordings
- Routing hierarchy diagram
- Change log template (Territory-Based)
- QA checklist for ongoing validation
- Definition Alignment Document (final version)
- Maintenance Schedule

**Output:** Customer owns the routing system. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location
- [ ] Handoff documentation complete
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell &rarr; Downsell &rarr; Retry  |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (routing maintenance retainer)
   | if no
2. Downsell: Another project (Sales Territory if not done, Speed to Lead, Automated Inbound)
   | if yes
3. Retry retainer at end of next project cycle
```

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in ~1 quarter after go-live to review routing performance, distribution fairness, and edge cases.

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- Routing spec document (approach, hierarchy, rules, fallback, override logic)
- Definition Alignment Document (routing terms agreed with stakeholders)
- Routing hierarchy diagram (visual representation of decision tree)

**Technical Deliverables (Phase 2):**

| Approach        | Technical Deliverables                                                         |
| --------------- | ------------------------------------------------------------------------------ |
| Round Robin     | Configured rotation in CRM or scheduling tool                                   |
| Territory-Based | Active routing flow + Territory Object (if SF) + change log template            |
| Target Account  | Active routing flow with named account check + fallback + named account list    |

**Documentation Package:**

- Training video recordings (routing walkthrough + how to make updates)
- QA checklist for ongoing validation
- Change log template with instructions (Territory-Based)
- Maintenance schedule
- Definition Alignment Document (final version)

---

## Appendix

This is the implementation playbook for Lead Routing -- the step-by-step execution guide for delivering a lead routing project from first contact to project close, following the 4-phase framework: Strategy, Engineering, Enablement, Handoff.

### What Each Phase Produces

| Phase                    | Output                                                                 | Gate Criteria                                                                  |
| ------------------------ | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **Phase 1: Strategy**    | Confirmed approach + approved routing spec                             | Approach and tool confirmed, routing hierarchy designed, definitions aligned    |
| **Phase 2: Engineering** | Built and tested routing system (in INACTIVE, then activated)          | All QA test cases pass, customer has approved routing behavior                 |
| **Phase 3: Enablement**  | Trained team with documentation, stabilized system                     | All training delivered, hypercare complete, ops team can make updates independently |
| **Phase 4: Handoff**     | Independent customer + archived project                                | Internal/external handoffs complete, maintenance schedule in place, project closed |

### How to Adapt Per Project Type

Lead Routing is a **Technical / Balanced** project. Engineering carries the most weight, but the approach varies significantly:

| Approach        | Strategy Weight | Engineering Weight | Enablement Weight | Handoff Weight |
| --------------- | --------------- | ------------------ | ----------------- | -------------- |
| Round Robin     | 20%             | 30%                | 20%               | 30%            |
| Territory-Based | 25%             | 40%                | 15%               | 20%            |
| Target Account  | 25%             | 35%                | 15%               | 25%            |

**Adaptation rules:**
- **Round Robin** compresses Phases 1 and 2. Heaviest weight shifts to Phase 4 (maintenance expectations).
- **Territory-Based** expands Phase 2 significantly (complex flow with many decision nodes). Phase 4 maintenance is ongoing and intensive.
- **Target Account** is a hybrid -- Phase 2 includes both the named account check and the fallback routing build.
- **Phase 4 always applies** -- maintenance schedule complexity varies dramatically by approach.

---

## References

- [Workato - We Tested 114 B2B Companies' Lead Response Times](https://www.workato.com/the-connector/lead-response-time-study/) -- Average B2B response time is 42 hours; 63% of businesses did not respond to inbound leads at all.
- [Chili Piper - Speed to Lead Statistics](https://www.chilipiper.com/article/speed-to-lead-statistics) -- 391% increase in conversions when contacted within same minute.
- [Kixie - Speed to Lead Response Time Statistics](https://www.kixie.com/sales-blog/speed-to-lead-response-time-statistics-that-drive-conversions/) -- Businesses responding within 5 minutes are 100x more likely to connect and convert.
- [Rep.ai - Lead Response Time Statistics](https://rep.ai/blog/lead-response) -- As few as 27% of leads ever get contacted.
- [Gartner via Trysidekick - ROI of Lead Management Automation](https://trysidekick.com/roi-lead-management-automation) -- Companies that automate lead management see 10%+ revenue increase in 6-9 months.
- [LeanData - Lead Routing Platform](https://www.leandata.com/lead-routing-flow-and-assignment/) -- 95%+ matching accuracy, no-code orchestration, PTO/availability automation.
- [Chili Piper vs LeanData Comparison](https://www.chilipiper.com/compare/chili-piper-vs-leandata) -- Feature comparison for dedicated routing tools.
