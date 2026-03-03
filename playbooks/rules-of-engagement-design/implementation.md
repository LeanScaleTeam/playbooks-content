# Rules of Engagement Design — Implementation

## Project One-Pager

### Rules of Engagement Design One-Pager

#### Project Type

- Category: Strategic (with light technical enforcement)
- Primary Deliverable: Comprehensive Rules of Engagement document with CRM enforcement configurations and dispute resolution process

##### Phase Relevance

| Phase          | Applies? | Weight | Notes                                                    |
| -------------- | -------- | ------ | -------------------------------------------------------- |
| 1. Strategy    | Yes      | Heavy  | 3-4 refinement loops; scenario mapping + stakeholder alignment |
| 2. Engineering | Yes      | Light  | CRM validation rules, ownership timeout automation       |
| 3. Enablement  | Yes      | Medium | Team-wide rollout meeting + rep acknowledgment           |
| 4. Handoff     | Yes      | Medium | Internal + External; dispute monitoring plan             |

· · ·

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │    Heavy     │     │    Light     │     │    Medium    │     │    Medium    │
  │ 1a→1b→1c→1d │     │ 2a→2b→2c→2d │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   3-4 refinement       CRM enforcement      Rollout meeting      Internal +
   loops + scenarios    configs              + acknowledgment     External handoff
```

**This project's flow:**
- Full 4-phase. Heavy strategy (scenario mapping, rule drafting, stakeholder review), light engineering (CRM enforcement configs), medium enablement (rollout meeting + acknowledgment), standard handoff.
- Some customers skip 2c/2d if they handle CRM enforcement internally. Phase 1 is where the majority of time is spent.

· · ·

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Watch intro video explaining what ROE is and why it matters
- [ ] Complete pre-intake form: current team structure, segments, existing ownership rules (if any)
- [ ] Provide access to Salesforce/HubSpot for ownership audit
- [ ] Gather 3-5 examples of recent ownership disputes or rep complaints

##### Track B: Architect Prep
- [ ] Pull CRM ownership data: reassignment history, duplicate outreach events, inactive opportunity count (past 90 days)
- [ ] Review existing ROE docs (wiki pages, tribal knowledge)
- [ ] Draft scenario matrix v0 based on team structure and CRM data
- [ ] Create gap analysis: what rules exist vs. what's missing

· · ·

#### Refinement Loop (1b -> 1c -> 1d)

| Meeting        | Sub-Phase | Focus                                                    | Stakeholder                  | Output                     |
| -------------- | --------- | -------------------------------------------------------- | ---------------------------- | -------------------------- |
| Kickoff        | 1b        | Present gap analysis + v0 scenario matrix, gather input  | VP Sales, Sales Ops Lead     | Info for v1 ROE draft      |
| Refinement 1   | 1c        | Review v1 ROE rules, stress-test against past disputes   | VP Sales, Sales Managers     | v2 with edge cases added   |
| Refinement 2   | 1c        | Review partner/channel rules, dispute resolution process | VP Sales, Channel Lead       | v3 near-final              |
| Sign-Off       | 1d        | Final review, leadership approval                        | VP Sales, CRO (if sponsor)   | Approved ROE document      |

· · ·

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held
- [ ] 1c. Refinement loop complete (v0 -> vFinal ROE)
- [ ] 1d. Strategic sign-off obtained from VP Sales

##### Phase 2: Engineering
- [ ] 2a. Tech spec created for CRM enforcement rules
- [ ] 2b. Engineering handoff meeting held with CRM admin
- [ ] 2c. CRM enforcement configurations built
- [ ] 2d. QA/Test + customer sign-off on enforcement rules

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped (quick reference card, full ROE doc, FAQ)
- [ ] 3b. Team-wide rollout session delivered
- [ ] 3c. Hypercare period complete (2 weeks)
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff (SME -> Architect) complete
- [ ] 4c. External handoff complete
- [ ] 4d. Project closed and archived

· · ·

#### Document Types

##### Working Documents (iterate together)

| Document                  | Purpose                                                  | When Complete                            |
| ------------------------- | -------------------------------------------------------- | ---------------------------------------- |
| Scenario matrix           | Map all ownership scenarios requiring rules              | All scenarios categorized and prioritized |
| Dispute log (past 90 days)| Quantify current conflict frequency and types            | All known disputes cataloged             |
| Draft ROE rules           | Iterate ownership rules with if/then language            | All scenarios have specific rules         |
| Escalation process draft  | Define dispute resolution path and SLAs                  | Approved by VP Sales                     |

##### Deliverables (polished outputs)

| Deliverable                     | Created From               | Customer Uses For                         |
| ------------------------------- | -------------------------- | ----------------------------------------- |
| Final ROE Document              | Draft ROE rules + feedback | Official reference for all reps           |
| 1-Page Quick Reference Card     | Final ROE Document         | Daily reference for reps                  |
| CRM Enforcement Config Doc      | Tech spec                  | Maintaining automation rules              |
| Dispute Resolution Flowchart    | Escalation process draft   | Resolving ownership conflicts             |

· · ·

#### Enablement Details

##### Training Types

| Type       | Audience                        | Focus                                              | Duration |
| ---------- | ------------------------------- | -------------------------------------------------- | -------- |
| Leadership | VP Sales, Sales Managers        | How to enforce ROE, arbitrate disputes, review cadence | 30 min   |
| Team-wide  | All Sales Reps, SDRs/BDRs      | What the rules are, examples, how to resolve disputes  | 45 min   |
| Technical  | RevOps/Sales Ops, CRM Admin    | CRM enforcement configs, monitoring dashboard, maintenance | 45 min   |

##### Hypercare
- Applies: Yes
- Duration: 2 weeks post-rollout
- Office Hours: Yes -- 2x weekly 30-min slots for dispute questions during first 2 weeks

##### Training Assets to Create
- [ ] Video walkthrough: ROE overview (10 min)
- [ ] Doc: 1-Page Quick Reference Card for reps
- [ ] Doc: Full ROE Document (version-controlled)
- [ ] Doc: Dispute Resolution Flowchart
- [ ] Doc: FAQ covering top 10 scenario questions
- [ ] Video walkthrough: CRM enforcement walkthrough for admins (5 min)

· · ·

#### Handoff & Retention

##### Internal Handoff (SME -> Architect)
- Key context for Architect: Which rules caused the most debate, who the final arbiter is, any pending edge cases to monitor
- Escalation trigger: Any request to change ownership rules or add new scenario categories

##### External Handoff
- Final meeting agenda: Review final ROE doc, walk through CRM enforcement, confirm dispute monitoring process, answer remaining questions
- Documentation package: ROE Document, Quick Reference Card, CRM Config Doc, Dispute Resolution Flowchart, FAQ, Training recordings, Maintenance Schedule

##### Maintenance Schedule
- Quarterly ROE review cadence (see Phase 4a for full schedule)
- Who owns: Single project = RevOps/Sales Ops owns | Dedicated = Architect owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services (ongoing ROE monitoring + quarterly reviews) -> if no -> Downsell: Territory Design or Lead Routing project -> Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~quarter out
- Internal prep trigger: 2 weeks before
- Decision: Architect handles routine ROE updates / SME needed for structural changes

· · ·

#### Key Assets

| Asset                        | Link   | When Used         |
| ---------------------------- | ------ | ----------------- |
| Scenario Matrix Template     | [link] | Phase 1a-1c       |
| ROE Document Template        | [link] | Phase 1c-1d       |
| Quick Reference Card Template| [link] | Phase 3a          |
| Dispute Resolution Flowchart | [link] | Phase 1c, 3b      |
| CRM Enforcement Config Guide | [link] | Phase 2a-2c       |

· · ·

#### Definition Alignment Terms

| Term                    | Typical Definition                                                                  |
| ----------------------- | ----------------------------------------------------------------------------------- |
| Account Ownership       | The rep designated as primary point of contact for a given account in CRM           |
| Opportunity Ownership   | The rep responsible for advancing a specific deal through the pipeline              |
| Named Account           | An account explicitly assigned to a rep regardless of inbound activity              |
| Ownership Timeout       | Maximum days an opportunity can remain inactive before reassignment triggers         |
| Cooling-Off Period      | Duration after an opportunity is closed-lost before another rep can re-engage        |
| Deal Registration       | Formal claim on a partner-sourced opportunity with a defined protection window       |
| Segment Handoff         | Transfer of account ownership when a customer moves between segments (e.g., SMB to MM)|
| Final Arbiter           | The designated individual (usually VP Sales or RevOps Lead) who makes final ownership decisions |
| Split Credit            | Shared revenue credit when legitimate overlap exists between two reps               |

· · ·

#### Common Gotchas
- Rules written in vague language ("the rep who has the relationship") -> Use specific if/then language with measurable criteria: "IF account has no activity for 60+ days, THEN ownership reverts to round-robin pool"
- No CRM data quality check before enforcement -> Validate that Industry, Employee Count, and Revenue fields are populated enough to enforce rules; address data gaps before automating
- Designing ROE without frontline rep input -> Interview 3-5 reps before drafting; rules designed exclusively top-down face resistance at rollout
- Forgetting partner/channel scenarios -> Include deal registration, co-selling, and partner-sourced lead rules even if partner program is small; these cause disproportionate disputes
- No version control on ROE document -> Store in a single accessible location (wiki, Notion) with change history; multiple floating versions cause confusion

· · ·

#### Methodology Options

| Option                        | When to Use                                           | Complexity |
| ----------------------------- | ----------------------------------------------------- | ---------- |
| Simple (core rules only)      | &lt;20 reps, single segment, no partner channel          | Low        |
| Standard (full scenario coverage) | 20-100 reps, multiple segments, basic partner deals | Medium     |
| Advanced (with CRM enforcement + monitoring) | 100+ reps, multiple segments, active partner program, history of disputes | High |

---

## Phase 1: Strategy

> **Goal:** Get VP Sales and sales leadership sign-off on a complete, enforceable Rules of Engagement document covering all ownership scenarios.
>
> **Output:** Final ROE Document + Dispute Resolution Process + Definition Alignment Document (signed off by stakeholders).

### 1a. Pre-Kickoff

> Two parallel tracks run after the engagement is scoped and before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                    | Format             |
| ----------------------------- | ---------------------------------------------------------- | ------------------ |
| Intro video                   | Explain what ROE design is, why it matters, what we deliver | Video walkthrough (5-10 min) |
| Definition Alignment Document | Get stakeholder sign-off on key ownership terms            | Google Doc         |
| Pre-filled intake form        | Confirm team structure, segments, existing rules            | Google Form or Doc |

The intake form should capture:
- Current sales team roster (reps, SDRs, AMs, CSMs) with segment assignments
- Existing ROE documentation or tribal knowledge (links or copy-paste)
- 3-5 examples of recent ownership disputes or gray areas
- Whether partner/channel deals exist
- CRM type (Salesforce or HubSpot) and admin access contact

**Completion tracking:** Sales Ops or RevOps contact is responsible for follow-up. Do not cancel kickoff if incomplete, but push hard after.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                          | Output                                |
| ---- | --------------------------------------------------------------- | ------------------------------------- |
| 1    | Pull CRM ownership data (reassignments, inactive opps, dupes)  | Raw dispute/conflict data (90 days)   |
| 2    | Review existing ROE docs and wiki pages                         | Current state summary                 |
| 3    | Map team structure to segments and territories                  | Org-scenario mapping                  |
| 4    | Build v0 scenario matrix from intake + CRM data                | v0 scenario matrix                    |
| 5    | Create gap analysis (rules that exist vs. rules missing)        | Gap analysis document                 |
| 6    | Prepare kickoff call deck with conflict data and scenario matrix| Kickoff presentation                  |

**Critical:** Mark everything in v0 as ASSUMED. The kickoff call validates.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE drafting rules.

| Term                  | Our Definition                                                              | Internally Approved? |
| --------------------- | --------------------------------------------------------------------------- | -------------------- |
| Account Ownership     | Rep designated as primary contact for an account in CRM                     | [ ] Yes / [ ] No     |
| Opportunity Ownership | Rep responsible for advancing a specific deal through the pipeline          | [ ] Yes / [ ] No     |
| Named Account         | Account explicitly assigned to a rep regardless of inbound activity         | [ ] Yes / [ ] No     |
| Ownership Timeout     | Max days an opp can sit inactive before reassignment triggers               | [ ] Yes / [ ] No     |
| Cooling-Off Period    | Duration after closed-lost before another rep can re-engage the account     | [ ] Yes / [ ] No     |
| Segment Handoff       | Ownership transfer when customer moves between segments (SMB -> MM -> Ent)  | [ ] Yes / [ ] No     |
| Deal Registration     | Formal partner claim on an opportunity with a defined protection window     | [ ] Yes / [ ] No     |
| Split Credit          | Shared revenue credit when legitimate overlap exists between reps           | [ ] Yes / [ ] No     |
| Final Arbiter         | Person who makes final ownership decisions when escalation path is exhausted| [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your sales leadership team. Check "Yes" when approved. We cannot draft enforceable rules until all terms are aligned -- ambiguous definitions produce ambiguous rules.

---

### 1b. Kickoff Call

> **Purpose:** Present v0 scenario matrix and gap analysis. Validate assumptions about team structure, current conflicts, and priority scenarios.

#### Agenda (60-90 min)

| Time  | Topic                       | What Happens                                           |
| ----- | --------------------------- | ------------------------------------------------------ |
| 0-15  | Walk through gap analysis   | "Here's what we found in your CRM and existing docs"   |
| 15-30 | Review v0 scenario matrix   | "Here are all the ownership scenarios we've mapped"    |
| 30-45 | Validate assumptions        | ASSUMED -> CONFIRMED or corrected for team structure    |
| 45-55 | Definition alignment review | Review key terms, flag any disagreements               |
| 55-65 | Prioritize scenarios        | Rank by frequency and conflict potential               |
| 65+   | Next steps                  | Schedule refinement loop, assign homework              |

#### What We Bring

- v0 scenario matrix
- Gap analysis (existing rules vs. missing rules)
- CRM ownership data summary (dispute count, reassignment trends)
- Definition Alignment Document (pre-filled with our recommendations)
- Questions list: specific disputes to discuss, edge cases to validate

#### What We Leave With

- Validated team structure and segment definitions
- Confirmed priority scenarios (which rules to draft first)
- Feedback on v0 (corrections, missing scenarios)
- Confirmed definitions (or clear blockers needing executive input)
- Alignment loop scheduled with appropriate stakeholders

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Iterate on the ROE document until all scenarios are covered and VP Sales signs off.

#### The Pattern

```
Kickoff Call (validate scenarios + priorities)
    |
v1 ROE draft produced
    |
Meeting 2 (present v1, stress-test against disputes) -> v2
    |
Meeting 3 (partner rules, escalation process) -> v3
    |
Meeting 4: Final Review -> Sign-off
```

#### Before Each Meeting

1. Update ROE document from previous meeting notes (v[n-1] -> v[n])
2. Prepare stress-test scenarios from historical dispute data
3. Flag any definitions still lacking sign-off

#### During Each Meeting

1. Walk through current version of rules
2. Stress-test: "Given this rule, here's how Dispute X would have been resolved"
3. Capture corrections, new edge cases, and language refinements
4. Validate what's now CONFIRMED vs. remaining ASSUMED items

#### After Each Meeting

1. Update document with corrections
2. Track what moved from ASSUMED -> CONFIRMED
3. Update scenario matrix with any newly identified scenarios

#### Meeting Types for This Project

| Meeting Type          | Focus                                                    | Stakeholder                     |
| --------------------- | -------------------------------------------------------- | ------------------------------- |
| Kickoff               | Scenario validation, priorities, gap analysis            | VP Sales, Sales Ops Lead        |
| Refinement 1          | Core rules (inbound, outbound, existing customer)        | VP Sales, Sales Managers        |
| Refinement 2          | Partner/channel rules, dispute resolution, CRM approach  | VP Sales, Channel Lead (if any) |
| Final Review          | Full document walkthrough, sign-off                      | VP Sales, CRO (if sponsor)      |

#### Typical Timeline

| Milestone               | Timing                                        |
| ----------------------- | --------------------------------------------- |
| Pre-kickoff prep        | 2-3 days                                      |
| Kickoff call            | Day 1 of engagement                           |
| Refinement meetings     | 1-2 weeks (2-3 meetings, depends on complexity)|
| Final review + sign-off | End of week 2-3                               |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm the ROE document is complete and enforceable before proceeding to CRM configuration.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by VP Sales
- [ ] All priority scenarios have specific if/then rules with examples
- [ ] Escalation path documented with named decision-makers and SLAs
- [ ] Ownership timeout thresholds defined and agreed upon
- [ ] Parent-child account rules addressed
- [ ] Partner/channel deal rules included (or explicitly scoped out)
- [ ] Rules stress-tested against 5+ historical disputes
- [ ] VP Sales has given final approval

#### Decision Point

- **Proceed to Engineering** -> Customer wants CRM enforcement automated (most cases)
- **Project complete (Phase 1 only)** -> Customer will enforce manually; skip to Enablement for rollout training

> ROE Design can complete after Phase 1 if the customer only needs the documented rules and will handle CRM enforcement themselves. This is common for smaller teams (&lt;20 reps) where manual enforcement is practical.

---

## Phase 2: Engineering

> **Goal:** Configure CRM to automate enforcement of approved ROE where possible.
>
> **Output:** CRM validation rules, ownership timeout automation, duplicate outreach alerts, and dispute tracking dashboard -- all tested and approved.

| Project Type       | Engineering Weight | Example                                            |
| ------------------ | ------------------ | -------------------------------------------------- |
| ROE Design (light) | Light (15-25%)     | Ownership timeouts + basic validation rules only   |
| ROE Design (full)  | Medium (25-35%)    | Full automation including alerts, dashboards, flows |

### Sub-Phases

```
2a Tech Spec -> 2b Engineering Handoff -> 2c Build -> 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate approved ROE rules into CRM configuration specifications.

**Input:** Signed-off ROE document from Phase 1

**What happens:**

1. Map each enforceable rule to a CRM mechanism (validation rule, flow, assignment rule, alert)
2. Identify which rules can be automated vs. which remain manual
3. Specify field-level requirements (fields needed, picklist values, formulas)

**Output:** Draft tech spec containing:

- Ownership timeout automation specs (field: Last Activity Date, threshold: X days, action: reassign to queue)
- Validation rule specs (prevent unauthorized owner changes on protected accounts)
- Alert/notification specs (duplicate outreach detection, ROE violation flags)
- Dashboard/report specs (dispute tracking, ownership distribution, timeout triggers)
- Build sequence (what to configure first)

**Salesforce-specific considerations:**
- Territory Management does not assign record ownership -- it only grants access [1]. Use Flow or Apex for owner reassignment automation.
- Assignment rules distribute leads based on criteria like geography, industry, or round-robin [2]. Configure these to align with ROE inbound lead rules.
- Validation rules can prevent unauthorized field changes but cannot trigger reassignment; pair with Flow for enforcement.

**HubSpot-specific considerations:**
- Use workflows to update lifecycle stages and trigger ownership changes based on engagement [3]
- Use HubSpot's duplicate management tools to flag potential ROE violations from overlapping outreach
- Configure deal rotation settings to match ROE round-robin rules

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs with CRM admin before building.

**Who attends:** Architect + CRM Admin

**Agenda (30-45 min):**

| Time  | Topic              | What Happens                                           |
| ----- | ------------------ | ------------------------------------------------------ |
| 0-15  | Walk through specs | Architect explains ROE rules and corresponding CRM configs    |
| 15-30 | Admin questions    | Clarify CRM-specific constraints, existing automation  |
| 30-45 | Refine and approve | Adjust specs for CRM version/edition limits, confirm build approach |

**What Architect brings:**

- Approved ROE document (for strategic context)
- Draft tech spec (from 2a)
- Questions list (CRM edition limits, existing conflicting automation)

**What engineer/admin leaves with:**

- Approved tech spec
- Clear build sequence
- Known risks (existing automation conflicts, edition limits)

---

### 2c. Build (Configure)

> **Purpose:** Configure CRM enforcement rules and monitoring.

**Input:** Approved tech spec from 2b

**Build components:**

- [ ] Ownership timeout automation (Flow/Workflow: reassign inactive opps after X days to queue or manager)
- [ ] Validation rules (prevent unauthorized ownership changes on named/protected accounts)
- [ ] Duplicate outreach alerts (flag when multiple reps contact the same account within X days)
- [ ] Dispute tracking report/dashboard (disputes raised, resolution time, outcomes)
- [ ] ROE violation notifications (email alert to manager when rules are breached)

**Build tracking:**

- [ ] Component 1: Ownership timeout Flow -- [status]
- [ ] Component 2: Validation rules for protected accounts -- [status]
- [ ] Component 3: Duplicate outreach detection -- [status]
- [ ] Component 4: Dispute tracking dashboard -- [status]
- [ ] Component 5: ROE violation email alerts -- [status]

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify enforcement rules work correctly and do not create unintended side effects.

**Technical testing checklist:**

- [ ] Ownership timeout fires correctly when opportunity is inactive for X days
- [ ] Validation rule prevents unauthorized owner changes on protected accounts
- [ ] Validation rule allows legitimate changes (manager override, segment handoff)
- [ ] Duplicate outreach alert triggers when two reps contact same account within window
- [ ] Dashboard accurately shows dispute count, resolution SLA adherence, ownership distribution
- [ ] No conflicts with existing CRM automation (lead routing, assignment rules)
- [ ] Error messages are clear and actionable ("This account is protected under Named Account rules. Contact your manager to request ownership transfer.")

**Customer testing:**

- Walk CRM admin through each enforcement rule
- Test 3-5 scenarios from the ROE document (inbound overlap, timeout reassignment, partner deal registration)
- Have admin attempt to break rules (unauthorized change, duplicate outreach) to verify blocking
- Capture feedback, fix issues

**Engineering sign-off checkpoint:**

- [ ] All enforcement rules match tech spec
- [ ] All technical tests passing
- [ ] CRM admin has tested and approved
- [ ] No unintended side effects on existing automation
- [ ] Ready for enablement

**Decision point:**

- **Proceed to Enablement** -> CRM enforcement is built and tested
- **Loop back to Build** -> Issues found, needs fixes

---

## Phase 3: Enablement

> **Goal:** Sales team understands, accepts, and can operate under the new ROE.
>
> **Output:** Trained team with documentation, signed acknowledgments, stabilized dispute resolution process.

### Sub-Phases

```
3a Training Prep -> 3b Training Sessions -> 3c Hypercare -> 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from the approved ROE document and CRM enforcement configurations.

**Input:** Final ROE document + CRM enforcement configs + dispute resolution flowchart

**What happens:**

1. Create 1-page Quick Reference Card (key rules, examples, escalation contacts)
2. Create FAQ document (top 10 scenario questions reps will ask)
3. Draft scripts for overview video walkthroughs
4. Prepare team-wide rollout meeting deck with concrete examples

**Output:** Training package containing:

- Quick Reference Card (laminate-ready 1-pager)
- FAQ document (10-15 questions with specific answers referencing ROE rules)
- Video walkthrough scripts (ROE overview, CRM enforcement walkthrough)
- Rollout meeting deck (rules + examples + dispute process + Q&A)
- Rep acknowledgment form (signature/checkbox confirming they've read and understood)

---

### 3b. Training Sessions

> **Purpose:** Roll out ROE to the entire sales organization with clear communication and buy-in.

**Training sessions by audience:**

| Session             | Audience                        | Focus                                                              | Duration |
| ------------------- | ------------------------------- | ------------------------------------------------------------------ | -------- |
| Leadership briefing | VP Sales, Sales Managers        | Enforcement approach, dispute arbitration role, review cadence      | 30 min   |
| Team-wide rollout   | All Sales Reps, SDRs/BDRs, AMs | Key rules with examples, dispute resolution process, Q&A           | 45 min   |
| Technical handoff   | RevOps/Sales Ops, CRM Admin    | CRM enforcement configs, monitoring dashboard, maintenance tasks   | 45 min   |

**Rollout meeting best practices:**

1. Open with the "why" -- share conflict data from discovery (number of disputes, time wasted, deals lost)
2. Walk through 5-6 key rules with concrete examples using if/then language
3. Show the dispute resolution flowchart -- who to talk to, in what order, with what SLA
4. Address the 3 most common objections (see Methodology for belief barriers)
5. Have all reps sign/acknowledge they've read and understood ROE
6. Store final document in accessible location (wiki, Notion, Google Drive)

**Output:**

- Trained stakeholders at every level
- Video walkthrough recordings for future onboarding
- Signed acknowledgment from all reps
- Questions log (feeds into FAQ updates)

---

### 3c. Hypercare

> **Purpose:** Intensive post-rollout support to catch edge cases and build confidence in the new process.

**Duration:** 2 weeks

**What happens:**

- 2x weekly 30-min office hours for dispute questions and gray-area scenarios
- Quick response to ROE interpretation questions
- Monitor first disputes under new rules -- are they being resolved correctly?
- Update FAQ with new questions that surface
- Flag any rules that need immediate adjustment (rare but possible)

**When to extend:** If >3 disputes per week are escalating past first-line resolution, extend hypercare by 1 week.

**Output:** Stabilized dispute resolution process, no critical interpretation gaps

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm the sales team can operate under ROE independently.

**Validation checkpoint:**

- [ ] All training sessions delivered
- [ ] All reps have signed acknowledgment
- [ ] Training recordings and documentation provided
- [ ] Hypercare period complete with no critical issues outstanding
- [ ] Dispute resolution process tested on at least 2-3 real disputes
- [ ] FAQ updated with hypercare questions
- [ ] Customer team can resolve disputes without daily support
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** -> Team is operating under ROE, disputes resolving through process
- **Extend Hypercare** -> Still too many escalations or interpretation gaps

---

## Phase 4: Handoff

> **Goal:** Clean project close with ROE maintenance plan established, monitoring in place, and retention/expansion path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the ROE, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule -> 4b Internal Handoff -> 4c External Handoff -> 4d Project Close
                           (SME -> Architect)                               (Archive + Debrief)
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At                                                            |
| ----------------------------- | -------------------- | ------------------------------------------------------------------------ |
| **Single Project**            | Customer owns        | 4c (External Handoff) -- customer receives maintenance schedule          |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) -- Architect receives maintenance schedule and runs it |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention after the project is complete.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task              | What to Check                                             | Red Flag Threshold                            |
| ------------------------- | --------------------------------------------------------- | --------------------------------------------- |
| Dispute frequency         | Number of ownership disputes escalated to management      | >5 disputes/month after first 60 days         |
| Timeout reassignment count| Number of opps auto-reassigned due to inactivity timeout  | >10% of pipeline hitting timeout              |
| ROE violation alerts      | CRM alerts for unauthorized ownership changes             | Any unresolved violations older than 48 hours |

**Quarterly Tasks:**

| Quarterly Task             | What to Review                                              | Action if Off-Track                            |
| -------------------------- | ----------------------------------------------------------- | ---------------------------------------------- |
| Full ROE document review   | Are all rules still relevant given team/segment changes?    | Update rules, republish, re-acknowledge        |
| Dispute resolution audit   | Are disputes being resolved within SLA? Any patterns?       | Adjust escalation path or SLAs                 |
| CRM enforcement check      | Are automation rules still firing correctly?                | Fix broken flows, update validation rules      |
| New scenario assessment    | Any new deal types, segments, or partners requiring rules?  | Draft new rules, get sign-off, update document |

**After First Business Cycle (30-60 days post-rollout):**

- Dispute Resolution Effectiveness: Did disputes decrease by target 50% vs. pre-ROE baseline? Effective territory realignment can increase overall revenue by 2-7% without additional sales resources [4].
- Rep Satisfaction Pulse: Quick survey -- do reps feel ownership rules are fair and clear?
- Key Question: Are the most common disputes from discovery phase now resolved by the rules? If not, which rules need refinement?

**Refinement Triggers (when to re-engage):**

| Trigger                        | Threshold                                   | Response                                          |
| ------------------------------ | ------------------------------------------- | ------------------------------------------------- |
| Dispute frequency increase     | >2x baseline for 2+ consecutive months      | Re-engage SME, review and update rules            |
| New segment added              | Any new segment (e.g., adding Enterprise)    | Scope new rules for segment handoffs              |
| Team restructure               | Major reorg (new roles, territory changes)   | Full ROE refresh project                          |
| Partner program launch/change  | New partner channel or deal reg changes      | Add partner-specific ROE section                  |

**Every 6-12 Months:**

- Full ROE recalibration: Review all rules against current team structure, segment mix, and business model
- Benchmark against dispute data: Has the ROE reduced conflicts to target levels?
- Assess CRM enforcement: Are automation rules still aligned with current ROE? Any new CRM capabilities to use?

---

### 4b. Internal Handoff (SME -> Architect)

> **Purpose:** Transfer context so Architect can manage ongoing ROE relationship.

**What the Architect needs to know:**

- Which rules were most debated and why (context for future change requests)
- Who the final arbiter is and their decision-making style
- Common edge cases that surfaced during the project
- CRM enforcement configurations and how to verify they're working
- **Maintenance schedule** (if Dedicated engagement -- Architect runs quarterly reviews)

**Escalation guidelines:**

| Issue Type                                    | Who Handles          | Example                                           |
| --------------------------------------------- | -------------------- | ------------------------------------------------- |
| Small tweaks: threshold adjustments, FAQ updates | Architect          | "Change timeout from 60 to 90 days"               |
| Structural changes: new scenario categories, new segments | SME        | "We're adding an Enterprise segment with new rules"|
| Dispute resolution process changes            | SME                  | "We want to change the final arbiter role"         |

**For Dedicated engagements:** Architect also receives the maintenance schedule (4a) and becomes responsible for executing quarterly ROE reviews. SME walks Architect through each maintenance task.

---

### 4c. External Handoff

> **Purpose:** Formal project completion with customer.

**Final project meeting:**

- Review what was delivered (ROE document, CRM configs, training materials)
- Walk through documentation package
- Walk through maintenance schedule (especially quarterly review cadence)
- Confirm ROE owner within client organization (typically RevOps Lead or Sales Ops Manager)
- Confirm dispute tracking process is running
- Answer final questions
- Make it explicit: "Project complete"
- **For Single Project engagements:** Walk customer through maintenance schedule in detail, record a video walkthrough

**Documentation package:**

- Final ROE Document (version-controlled)
- 1-Page Quick Reference Card
- Dispute Resolution Flowchart
- CRM Enforcement Configuration Documentation
- FAQ Document
- All training video walkthrough recordings
- Dispute Tracking Dashboard link
- Maintenance Schedule
- Support contact info

**Output:** Customer owns the ROE system. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location
- [ ] Handoff documentation complete
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized

#### Internal Debrief (Optional but Recommended)

- What went well? (Which rules were easiest to align on?)
- What would we do differently? (Which scenarios caused the most iteration?)
- Any learnings to feed back into ROE template or process?

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                              |
| ----------------------------- | --------------------------------- |
| **Single Project**            | Upsell -> Downsell -> Retry       |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In      |

**Single Project Path:**

```
1. Upsell: Managed Services (ongoing ROE monitoring + quarterly reviews)
   | if no
2. Downsell: Related project (Territory Design, Lead Routing, Commission Plan)
   | if yes
3. Retry retainer at end of next project cycle
```

**Script:**

> "Now that Rules of Engagement is complete, there are two ways we can continue working together. Option 1: We can set you up on managed services where we handle quarterly ROE reviews, monitor dispute trends, and update rules as your team evolves. Option 2: If there's a related project you need -- like Territory Design or Lead Routing -- we can scope that out. Which sounds more interesting?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On [date ~quarter out], we'll review how the ROE is performing -- dispute trends, any new scenarios, and whether any rules need adjustment."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                              |
| ------------------- | --------------------------------------------------------- |
| 1. Get pinged       | System reminder: ROE refinement check-in in 2 weeks      |
| 2. Review metrics   | Pull dispute data, timeout triggers, ROE violation alerts |
| 3. Decide ownership | Can Architect handle this check-in, or need SME?          |
| 4. Prep materials   | If SME needed, brief them. If Architect, prep talking points. |

**At the refinement check-in:**

- Review dispute frequency vs. baseline
- Identify any new scenarios or edge cases
- If minor: Architect updates rules and republishes
- If major: Scope ROE refresh project (restart the assembly line)

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- Final Rules of Engagement Document (comprehensive, all scenarios covered, if/then language)
- Dispute Resolution Process & Flowchart (escalation path with named roles and SLAs)
- Definition Alignment Document (signed off by VP Sales)
- 1-Page Quick Reference Card (for daily rep use)

**Technical Deliverables (if Phase 2 applies):**

- CRM ownership timeout automation (Flow/Workflow configuration)
- CRM validation rules (unauthorized change prevention)
- Duplicate outreach alerts
- Dispute tracking dashboard/report
- CRM Enforcement Configuration Documentation

**Documentation Package:**

- Training video walkthrough recordings (overview + CRM enforcement walkthrough)
- Written guides (Quick Reference Card, FAQ)
- Dispute Resolution Flowchart
- Definition Alignment Document (final version)
- Maintenance Schedule

---

## Appendix

### Roles

| Role | What They Do |
|---|---|
| **Architect** | Owns the customer relationship, leads strategy, creates specs, does enablement, owns account post-delivery |
| **Engineer** | CRM build, automation, dashboards (Phase 2) |
| **SME** | Project/implementation team brought in for project specific work |

### What Each Phase Produces

| Phase                    | Output                                                                    | Gate Criteria                                                                         |
| ------------------------ | ------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| **Phase 1: Strategy**    | Signed-off ROE document + Dispute Resolution Process + Definition Alignment Doc | VP Sales has approved all rules; stress-tested against historical disputes          |
| **Phase 2: Engineering** | CRM enforcement configurations tested and approved                       | Automation matches ROE rules; no conflicts with existing CRM setup                    |
| **Phase 3: Enablement**  | Trained team with signed acknowledgments                                 | All reps acknowledge ROE; dispute resolution tested on real cases                     |
| **Phase 4: Handoff**     | Independent customer + archived project                                  | Maintenance plan in place; ROE owner assigned; quarterly review scheduled             |

### How to Adapt Per Project Type

ROE Design is a **strategic-heavy** project. Most effort is in Phase 1 (scenario mapping, rule drafting, stakeholder alignment). Phase 2 is light (CRM enforcement). Phase 3 is medium (rollout and adoption). Phase 4 is standard.

| Project Profile          | Strategy Weight | Engineering Weight | Enablement Weight | Applies To                              |
| ------------------------ | --------------- | ------------------ | ----------------- | --------------------------------------- |
| **Simple ROE**           | 70%             | 0%                 | 20%               | &lt;20 reps, single segment, manual enforcement |
| **Standard ROE**         | 55%             | 20%                | 15%               | 20-100 reps, multiple segments, CRM enforcement |
| **Complex ROE**          | 45%             | 25%                | 20%               | 100+ reps, partner channel, complex org hierarchy |

**Adaptation rules:**

- **Simple ROE** may skip Phase 2 entirely -- customer enforces manually
- **Complex ROE** expands Phase 1 with additional refinement meetings for partner/channel rules
- **Phase 4 always applies** -- every ROE project needs a maintenance plan because rules become stale as orgs change

### Phase 1 Guide: Strategy (ROE-Specific)

#### How We Create Value in ROE Strategy

1. **We educate.** Most sales teams have never seen a well-structured ROE. We show them what "good" looks like -- specific if/then rules, concrete examples, clear escalation paths -- so they understand the standard we're building toward.

2. **We drive alignment.** ROE projects stall when Sales Managers disagree on ownership rules. We facilitate those hard conversations using data (dispute frequency, lost deals) and force alignment through the Definition Alignment Document.

3. **We come with an opinion.** We show up with v0 scenario matrix and recommended rules based on similar company patterns. The customer reacts and adjusts, not creates from scratch.

4. **We show best practices.** We anchor in what we've seen work across B2B SaaS companies at similar stage and complexity -- ownership timeout thresholds, dispute resolution SLAs, partner deal registration windows.

#### Why ROE-Specific Definition Alignment Matters

Ownership terms are particularly prone to ambiguity. "Account ownership" can mean different things to different Sales Managers within the same company. Getting sign-off on definitions BEFORE drafting rules prevents the most common failure mode: rules that are technically correct but interpreted differently by different managers.

#### The Dispute Data Advantage

The most powerful tool in ROE strategy is historical dispute data. Pulling 90 days of CRM reassignments and manager escalations does two things: (1) quantifies the problem for executive buy-in, and (2) provides real test cases to validate every rule we draft.

### Phase 2 Guide: Engineering (ROE-Specific)

#### Engineering for ROE is Enforcement, Not Creation

Unlike technical-heavy projects, ROE engineering is about enforcing rules that already exist in the document. The CRM doesn't create the rules -- it prevents violations and automates the mechanical parts (timeouts, reassignments, alerts).

#### Key Principle: Don't Over-Automate

Not every rule should be automated. Some rules are better enforced through culture and process:

| Automate                              | Keep Manual                                |
| ------------------------------------- | ------------------------------------------ |
| Ownership timeouts (inactivity)       | First-line dispute resolution (rep-to-rep) |
| Unauthorized change prevention        | Manager judgment on edge cases             |
| Duplicate outreach alerts             | Split credit decisions                     |
| Dispute tracking/reporting            | Final arbiter decisions                    |

### Phase 3 Guide: Enablement (ROE-Specific)

#### The Rollout is the Make-or-Break Moment

Research shows that workplace disputes cost approximately 2.8 hours per employee per week [5], and managers spend 20-40% of their time handling conflicts [6]. A well-executed ROE rollout directly reduces this burden -- but only if reps believe the rules are fair. The rollout meeting must address both the rules AND the rationale.

#### Getting Rep Buy-In

Reps accept rules when they understand three things:
1. **The data** -- show them the dispute count and time wasted (from discovery phase)
2. **The logic** -- explain WHY each rule exists, not just WHAT it says
3. **The process** -- show them exactly how to escalate when they disagree

#### The Acknowledgment Form

Having reps formally acknowledge they've read and understood the ROE is not bureaucratic theater. It creates accountability and prevents "I didn't know that was a rule" disputes. It also creates a clear starting point: ROE is enforceable from the moment it's acknowledged.

### Phase 4 Guide: Handoff (ROE-Specific)

#### Why ROE Maintenance Matters

ROE documents become stale faster than most deliverables. Teams grow, segments change, new partner channels launch, and org structures shift. Without a quarterly review cadence, rules designed for a 30-person team become unenforceable for a 60-person team within 6 months.

#### The Quarterly Review Pattern

Each quarter, the ROE owner should:
1. Pull dispute data from CRM dashboard
2. Review any new scenarios that surfaced since last review
3. Check if team structure or segment definitions changed
4. Update rules if needed, get sign-off, republish
5. Re-acknowledge if material changes were made

#### Retention: Natural Expansion Path

ROE Design connects naturally to several adjacent projects:
- **Territory Design** -- once rules exist, territories can be optimized
- **Lead Routing** -- ROE defines who owns what; Lead Routing automates delivery
- **Commission Plan Design** -- ROE defines credit; Commission Plan defines payout
- **Sales Lifecycle** -- ROE fits within the broader sales process framework

---

## References

[1] [Salesforce Territory Management Implementation Guide](https://resources.docs.salesforce.com/latest/latest/en-us/sfdc/pdf/salesforce_implementing_territory_mgmt2_guide.pdf)

[2] [Salesforce Assignment Rules: Setup, Tips & Best Practices](https://kubaru.io/blog/salesforce-assignment-rules/)

[3] [Best Practices for HubSpot & Salesforce Integration](https://www.blueoshan.com/blog/boost-crm-efficiency-best-practices-for-hubspot-salesforce-integration)

[4] [Gradient Works - The Trouble with Sales Territories](https://www.gradient.works/blog/the-trouble-with-sales-territories)

[5] [Pollack Peacebuilding - Workplace Conflict Statistics](https://pollackpeacebuilding.com/workplace-conflict-statistics/)

[6] [Peaceful Leaders Academy - Workplace Conflict Statistics 2025](https://peacefulleadersacademy.com/blog/workplace-conflict-statistics/)
