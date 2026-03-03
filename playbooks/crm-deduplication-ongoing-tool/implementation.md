# CRM Deduplication Ongoing Tool — Implementation

## Project One-Pager

### CRM Deduplication Ongoing Tool One-Pager

#### Project Type

- Category: Technical
- Primary Deliverable: Deployed and configured deduplication tool with automated matching rules, prevention logic, merge workflows, and ongoing monitoring dashboard

##### Phase Relevance

| Phase          | Applies? | Weight | Notes                                                    |
| -------------- | -------- | ------ | -------------------------------------------------------- |
| 1. Strategy    | Yes      | Medium | Tool evaluation, requirements gathering, rule design     |
| 2. Engineering | Yes      | Heavy  | Tool setup, matching rules, automation, prevention logic |
| 3. Enablement  | Yes      | Medium | Training on tool usage, manual review queue, maintenance |
| 4. Handoff     | Yes      | Medium | Documentation package, monitoring cadence, ownership     |

· · ·

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │    Medium    │     │    Heavy     │     │    Medium    │     │    Medium    │
  │ 1a→1b→1c→1d │     │ 2a→2b→2c→2d │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   Tool evaluation      Tool setup +         Training + review    Docs + monitoring
   + rule design        automation build     queue + maintenance  cadence + ownership
```

**This project's flow:**
- Full 4-phase. Medium strategy (tool evaluation + rule design), heavy engineering (tool configuration + automation), standard enablement and handoff.
- Phase 1 includes tool selection and procurement — budget approval can be a bottleneck. Plan for 1-2 week procurement lead time after selection.
- Phase 2 is the core of the work: configuring matching rules for Contacts/Leads and Accounts/Companies, defining master record survivorship, building prevention and automation workflows, and testing.
- No phases skipped. All clients need training (Phase 3) to manage manual review queues and ongoing rule tuning.

· · ·

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Watch intro video explaining deduplication tool project scope and why ongoing prevention matters
- [ ] Complete intake form: CRM platform, edition/tier, current duplicate volume estimates, integration landscape
- [ ] Provide list of critical fields that must be preserved during merges
- [ ] Confirm budget approval range for tool licensing
- [ ] Identify RevOps owner for ongoing tool management
- [ ] Provide CRM admin access credentials and API permissions

##### Track B: Architect Prep
- [ ] Run duplicate audit reports in CRM (Contacts, Leads, Accounts/Companies)
- [ ] Document duplicate sources: manual entry, imports, form submissions, integrations
- [ ] Quantify duplicate rate per object (e.g., "15% of Contacts have duplicates")
- [ ] Review existing deduplication rules or validation checks
- [ ] Assess CRM-MAP sync configuration (HubSpot-Salesforce sync, if applicable)
- [ ] Prepare tool comparison matrix with 2-3 shortlisted options

· · ·

#### Refinement Loop (1b → 1c → 1d)

| Meeting      | Sub-Phase | Focus                                                       | Stakeholder           | Output                          |
| ------------ | --------- | ----------------------------------------------------------- | --------------------- | ------------------------------- |
| Kickoff      | 1b        | Present duplicate audit, review tool options, gather rules  | RevOps, Sales Ops     | Requirements confirmed for v1   |
| Refinement 1 | 1c        | Review tool recommendation, define matching rules, discuss master record criteria | RevOps, IT/Admin      | Tool selected, rules drafted    |
| Refinement 2 | 1c        | Finalize survivorship logic, prevention strategy, automation thresholds | RevOps, Compliance    | Configuration spec finalized    |
| Sign-Off     | 1d        | Approve tool, rules, thresholds, and automation schedule    | All stakeholders      | Strategic sign-off, procurement |

· · ·

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held — duplicate audit presented, tool options reviewed
- [ ] 1c. Refinement loop complete — tool selected, rules designed, thresholds set
- [ ] 1d. Strategic sign-off obtained — budget approved, procurement initiated

##### Phase 2: Engineering
- [ ] 2a. Tech spec created — matching rules, survivorship logic, automation schedules
- [ ] 2b. Engineering handoff meeting held — tool admin walkthrough
- [ ] 2c. Build complete — tool connected, rules configured, automation live
- [ ] 2d. QA/Test + customer sign-off — preview merge run approved

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped — manual review SOP, quick-reference guide
- [ ] 3b. Training sessions delivered — RevOps team trained on tool usage
- [ ] 3c. Hypercare period complete — 30-day monitoring, queue review support
- [ ] 3d. Enablement sign-off — team operating independently

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff (SME → Architect) complete
- [ ] 4c. External handoff (delivery team → Customer) complete
- [ ] 4d. Project closed and archived

· · ·

#### Document Types

##### Working Documents (iterate together)

| Document                    | Purpose                                          | When Complete                                      |
| --------------------------- | ------------------------------------------------ | -------------------------------------------------- |
| Duplicate Audit Report      | Baseline: volume, sources, patterns per object   | All objects audited, rates quantified              |
| Tool Comparison Matrix      | Evaluate 2-3 tools against requirements          | Client selects tool, budget approved               |
| Matching Rules Spec         | Document matching fields, thresholds, cross-obj  | Rules validated with sample data                   |
| Survivorship Rules Doc      | Master record selection + field-level rules      | Compliance reviewed, opt-out handling confirmed    |

##### Deliverables (polished outputs)

| Deliverable                     | Created From              | Customer Uses For                          |
| ------------------------------- | ------------------------- | ------------------------------------------ |
| Tool Configuration Runbook      | Matching + survivorship   | Reference for rule changes and maintenance |
| Automation Schedule Doc         | Build outputs             | Understanding when auto-merge runs         |
| Manual Review SOP               | Training materials        | Day-to-day duplicate review process        |

· · ·

#### Enablement Details

##### Training Types

| Type       | Audience                        | Focus                                           | Duration |
| ---------- | ------------------------------- | ----------------------------------------------- | -------- |
| Leadership | VP Sales, VP Marketing          | Why dedup matters, dashboard metrics, ROI review | 20 min   |
| Technical  | RevOps, Sales Ops, CRM Admin   | Tool usage, manual review queue, rule tuning, unmerge process | 45 min   |

##### Hypercare
- Applies: Yes
- Duration: 30 days
- Office Hours: Yes — weekly 30-min slot for queue review and rule tuning questions

##### Training Assets to Create
- [ ] Video walkthrough: Tool dashboard and manual review queue
- [ ] Video walkthrough: How to run on-demand deduplication scans
- [ ] Doc: Manual review SOP with merge/reject criteria
- [ ] Doc: Quick-reference guide for common tasks (run scan, review queue, adjust threshold, unmerge)

· · ·

#### Handoff & Retention

##### Internal Handoff (SME → Architect)
- Key context for Architect: Tool name and version, automation schedule, current duplicate rate, manual review queue cadence
- Escalation trigger: Any matching rule changes, survivorship logic updates, cross-object rule modifications, or new integration data sources

##### External Handoff (Delivery Team → Customer)
- Final meeting agenda: Review delivered configuration, walk through maintenance schedule, demo unmerge/rollback, confirm ongoing support path
- Documentation package: Configuration runbook, automation schedule, manual review SOP, training video walkthroughs, quick-reference guide

##### Maintenance Schedule
- Monthly: Review manual queue, check duplicate rate trending, verify automation runs
- Quarterly: Review matching rule accuracy, adjust thresholds, audit new data sources
- Who owns: Single Project = customer owns | Dedicated = Architect owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services → if no → Downsell: Another project (CRM Data Enrichment, Lead Routing) → Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~1 quarter out
- Internal prep trigger: 2 weeks before
- Decision: Architect handles / SME needed (rule changes = SME)

· · ·

#### Key Assets

| Asset                    | When Used           |
| ------------------------ | ------------------- |
| Duplicate Audit Template | Phase 1a (Architect Prep)  |
| Tool Comparison Matrix   | Phase 1b-1c         |
| Matching Rules Spec      | Phase 2a-2c         |
| Manual Review SOP        | Phase 3b, Phase 4c  |
| Configuration Runbook    | Phase 4c            |

· · ·

#### Definition Alignment Terms

| Term                   | Typical Definition                                                                                           |
| ---------------------- | ------------------------------------------------------------------------------------------------------------ |
| Duplicate              | Two or more records representing the same real-world entity (person or company) in the CRM                   |
| Master Record          | The surviving record after a merge — retains the record ID and becomes the single source of truth           |
| Survivorship Rules     | Logic determining which field values are kept from merged records (e.g., most recent, most complete)         |
| Matching Rule          | Criteria used to identify potential duplicates (e.g., exact email match, fuzzy name match)                   |
| Confidence Score       | Numeric or categorical measure of how likely two records are true duplicates (drives auto-merge vs. review)  |
| False Positive         | Two records flagged as duplicates that are actually distinct entities                                         |
| False Negative         | Two records that are true duplicates but were not detected by matching rules                                  |
| Cross-Object Matching  | Deduplication across different objects (e.g., Contact vs. Lead) rather than within the same object            |
| Fuzzy Matching         | Matching algorithm that accounts for name variations, typos, abbreviations (e.g., "Inc" vs "Incorporated")   |
| Manual Review Queue    | Holding area for potential duplicates below the auto-merge confidence threshold, requiring human decision     |

· · ·

#### Common Gotchas
- HubSpot auto-creates Company records from Contact activity — disable this setting before configuring dedup rules if Salesforce is the source of truth, or duplicates re-enter constantly [1]
- Salesforce limits you to 5 active Duplicate Rules per object and 5 active Matching Rules per object — plan rule allocation carefully [2]
- Merging records with active Opportunities or open Cases can break ownership and workflow triggers — test merge behavior on records with related objects before bulk operations
- Opt-out/unsubscribe preferences must be preserved during merge — configure survivorship to always keep the most restrictive opt-out status from any merged record (GDPR/CAN-SPAM compliance)
- Third-party tools connected via API may re-sync deleted duplicates back into the CRM if sync rules are not updated to respect the merge

· · ·

#### Methodology Options (if applicable)

| Option                              | When to Use                                                    | Complexity |
| ----------------------------------- | -------------------------------------------------------------- | ---------- |
| Native CRM Tools Only               | Low duplicate volume (&lt;5%), simple matching needs, tight budget | Low        |
| Third-Party Tool (Insycle/Dedupely) | Mid-market, moderate volume, HubSpot or Salesforce, need automation | Medium     |
| Enterprise Platform (Openprise/RingLead) | High volume, complex matching, multi-CRM, cross-object needs | High       |

> See Methodology for detailed tool evaluation frameworks, matching algorithm comparisons, and scoring rubrics.

---

## Phase 1: Strategy

> **Goal:** Assess duplicate landscape, select deduplication tool, design matching and survivorship rules, and get stakeholder sign-off before building.
>
> **Output:** Approved tool selection + Configuration Spec (matching rules, survivorship logic, automation schedule, prevention strategy) signed off by RevOps and compliance stakeholders.

### 1a. Pre-Kickoff

> Two parallel tracks run before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                                 | Format             |
| ----------------------------- | ----------------------------------------------------------------------- | ------------------ |
| Intro video                   | Explain the project: why ongoing dedup matters, what the tool does      | Video (5-10 min)   |
| Definition Alignment Document | Get sign-off on terms: duplicate, master record, survivorship, matching | Google Doc         |
| Pre-filled intake form        | CRM platform, edition, integrations, current dedup pain, budget range   | Google Form or Doc |

**Specific intake questions:**
- CRM platform and edition (Salesforce Enterprise, HubSpot Professional, etc.)
- Current estimated duplicate rate (or "unknown")
- Primary duplicate sources: manual entry, imports, form submissions, integrations
- Existing dedup rules or validation checks in place
- CRM-MAP sync configuration (HubSpot-Salesforce sync, Marketo sync, etc.)
- Critical fields that must be preserved during merges
- Budget range for tool licensing ($5K-$50K/year typical range)
- Identified RevOps owner for ongoing management

**Completion tracking:** Follow up to ensure completion. Do not cancel kickoff if incomplete, but push hard after for admin access and budget range — these gate the tool selection timeline.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                                 | Output                                                |
| ---- | ---------------------------------------------------------------------- | ----------------------------------------------------- |
| 1    | Run duplicate audit reports in CRM for all target objects              | Duplicate rate per object, volume, pattern analysis   |
| 2    | Document duplicate sources (manual entry, imports, forms, integrations)| Source breakdown with estimated contribution per channel |
| 3    | Review CRM-MAP sync configuration                                      | Sync direction, conflict resolution rules, auto-create settings |
| 4    | Research tool options based on CRM platform and requirements           | Tool comparison matrix (2-3 options)                  |
| 5    | Create kickoff assets: audit summary, tool comparison, questions list  | Kickoff presentation deck                             |

**Critical:** Mark all audit findings as ASSUMED until validated with the RevOps team. They may know about duplicate sources that cannot be detected from CRM data alone.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE configuring anything.

| Term                  | Our Definition                                                                  | Internally Approved? |
| --------------------- | ------------------------------------------------------------------------------- | -------------------- |
| Duplicate             | Two or more records representing the same real-world entity in the CRM          | [ ] Yes / [ ] No     |
| Master Record         | The surviving record after merge — retains record ID, becomes source of truth  | [ ] Yes / [ ] No     |
| Survivorship Rules    | Logic for which field values are kept from merged records                        | [ ] Yes / [ ] No     |
| Confidence Threshold  | The score above which duplicates auto-merge vs. route to manual review          | [ ] Yes / [ ] No     |
| Cross-Object Match    | Deduplication across Contacts and Leads (not just within one object)            | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your RevOps and compliance teams. Check "Yes" when approved. We cannot configure matching rules until terms are aligned — particularly "master record" selection criteria and "survivorship" logic, as these are irreversible once merges execute.

---

### 1b. Kickoff Call

> **Purpose:** Present duplicate audit findings, review tool options, and gather matching rule requirements. We walk in with the audit done — customer reacts, not creates from scratch.

#### Agenda (60-90 min)

| Time  | Topic                          | What Happens                                                    |
| ----- | ------------------------------ | --------------------------------------------------------------- |
| 0-20  | Present duplicate audit        | "Here's what we found: X% duplicate Contacts, Y% Accounts"     |
| 20-35 | Validate sources and patterns  | Confirm which sources generate the most duplicates              |
| 35-50 | Review tool options            | Walk through comparison matrix, discuss pros/cons               |
| 50-65 | Matching rule priorities       | Which fields matter most? Email, domain, name? Cross-object?   |
| 65-75 | Master record preferences      | Most complete? Most recent? Earliest created? Field-by-field?  |
| 75-90 | Next steps                     | Homework: budget approval, admin access, schedule refinement   |

#### What We Bring

- Duplicate audit summary (rates per object, source breakdown, pattern examples)
- Tool comparison matrix with 2-3 options
- Draft matching field priority list (based on B2B best practices)
- Definition Alignment Document (pre-filled with recommendations)

#### What We Leave With

- Validated duplicate sources and patterns
- Tool preference or shortlist narrowed to 1-2
- Matching field priorities confirmed
- Master record selection preference captured
- Homework assigned: budget approval, admin access provisioning

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Iterate on tool selection, matching rules, and survivorship logic until sign-off.

#### The Pattern

```
Kickoff Call (gather requirements, present audit)
    |
    v
Architect drafts matching rules spec, refines tool recommendation --> v1
    |
    v
Meeting 2 (review rules, finalize tool selection) --> Architect refines --> v2
    |
    v
Meeting 3 (survivorship logic, prevention strategy, automation schedule) --> Architect finalizes --> v3
    |
    v
Final Review --> Sign-off
```

#### Before Each Meeting

1. Update matching rules spec with previous meeting's feedback
2. Research any open questions (tool capabilities, CRM limitations, compliance requirements)
3. Prepare decision items for next validation round

#### During Each Meeting

1. Walk through current version of configuration spec
2. Capture corrections and refinements
3. Validate what is now CONFIRMED vs. still ASSUMED
4. Identify remaining decisions needed

#### After Each Meeting

1. Update configuration spec (matching rules, survivorship, prevention, automation)
2. Track what moved from ASSUMED to CONFIRMED
3. Update tool procurement status if applicable

#### Meeting Schedule

| Meeting Type              | Focus                                                      | Stakeholder                     |
| ------------------------- | ---------------------------------------------------------- | ------------------------------- |
| Kickoff                   | Audit results, tool options, initial requirements          | RevOps Lead, Sales Ops          |
| Tool Selection + Rules    | Finalize tool, design matching rules per object            | RevOps, IT/Admin                |
| Prevention + Automation   | Survivorship logic, prevention strategy, automation design | RevOps, Compliance (if needed)  |
| Final Review              | Full configuration spec walkthrough, sign-off              | All stakeholders                |

#### Typical Timeline

| Milestone               | Timing                                                           |
| ----------------------- | ---------------------------------------------------------------- |
| Pre-kickoff prep        | 2-3 days                                                         |
| Kickoff call            | Day 1 of engagement                                              |
| Meeting loop            | 1-2 weeks (tool procurement can extend by 1-2 weeks)            |
| Final review + sign-off | When tool procured, rules confirmed, thresholds agreed           |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything before proceeding to build.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by stakeholders
- [ ] Duplicate audit validated by RevOps team
- [ ] Tool selected and procurement completed (license active, admin access granted)
- [ ] Matching rules designed for Contacts/Leads (primary + secondary fields, fuzzy thresholds)
- [ ] Matching rules designed for Accounts/Companies (domain, name variations, parent/child)
- [ ] Cross-object matching scope confirmed (Contact vs. Lead dedup: yes/no)
- [ ] Master record survivorship rules defined (field-level, opt-out preservation)
- [ ] Confidence thresholds set (auto-merge cutoff vs. manual review cutoff)
- [ ] Prevention strategy agreed (real-time alerts, blocks, form/import rules)
- [ ] Automation schedule defined (daily/weekly, notification recipients)
- [ ] No blockers for engineering

#### Decision Point

- **Proceed to Engineering** — Tool procured, rules designed, thresholds set. This project always proceeds to Engineering.

---

## Phase 2: Engineering

> **Goal:** Configure the deduplication tool end-to-end: matching rules, survivorship, prevention, automation, and manual review queue. Test and validate with preview merge runs.
>
> **Output:** Fully configured deduplication tool, tested against real data, initial duplicate backlog cleared, customer-approved.

| Project Type    | Engineering Weight | Notes                                                              |
| --------------- | ------------------ | ------------------------------------------------------------------ |
| CRM Dedup Tool  | Heavy (60-70%)     | Core of the project — tool setup, rules, automation, testing      |

### Sub-Phases

```
2a Tech Spec --> 2b Engineering Handoff --> 2c Build --> 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate strategic configuration spec into technical implementation plan.

**Input:** Signed-off configuration spec from Phase 1 (matching rules, survivorship logic, thresholds, automation schedule, prevention strategy)

**What happens:**

1. Translate matching rule designs into tool-specific configurations (field mappings, algorithm selections, threshold values)
2. Map survivorship rules to tool settings (field-by-field merge behavior)
3. Document API connection requirements and permissions
4. Sequence the build order: connection first, then Contact/Lead rules, then Account/Company rules, then prevention, then automation, then manual review queue

**Output:** Technical implementation plan containing:

- Tool connection checklist (OAuth/API key, permissions, sandbox vs. production)
- Matching rule configurations per object (exact fields, fuzzy fields, algorithm type, thresholds)
- Cross-object matching configuration (Contact-to-Lead, if applicable)
- Survivorship rule mappings (field-level: keep most recent, keep most complete, keep non-null, always preserve opt-out)
- Prevention rule setup (real-time detection: warn, block, or auto-merge; form/import rules)
- Automation schedule configuration (frequency, confidence threshold, notification recipients)
- Manual review queue setup (routing rules, assignment, checklist criteria)
- Test plan (known duplicate pairs, known non-duplicate pairs, edge cases)

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs before configuring the tool.

**Agenda (30-45 min):**

| Time  | Topic                    | What Happens                                                      |
| ----- | ------------------------ | ----------------------------------------------------------------- |
| 0-15  | Walk through tech spec   | Review matching rules, survivorship, prevention, automation       |
| 15-30 | Clarify tool specifics   | API permissions, CRM field access, sandbox availability           |
| 30-45 | Confirm build sequence   | Agree on order, identify risks (sync conflicts, API limits)       |

**What to bring:**

- Configuration spec (from Phase 1)
- Tech spec (from 2a)
- Tool admin credentials and CRM access confirmation

**What to leave with:**

- Approved tech spec with build sequence
- Known risks: HubSpot auto-create company setting, Salesforce duplicate rule limits, sync conflicts
- Test data: known duplicate pairs and known non-duplicate pairs for validation

---

### 2c. Build (Configure)

> **Purpose:** Configure the deduplication tool in the client's CRM environment.

**Input:** Approved tech spec from 2b

**Build sequence:**

| Step | Component                              | Details                                                                                    |
| ---- | -------------------------------------- | ------------------------------------------------------------------------------------------ |
| 1    | Tool account + CRM connection          | Create accounts, connect via OAuth/API, verify read/write permissions                      |
| 2    | Contact/Lead matching rules            | Primary: email (exact). Secondary: name (fuzzy), phone, company, domain. Set thresholds.   |
| 3    | Account/Company matching rules         | Primary: domain/website (exact). Secondary: company name (fuzzy). Handle parent/child.     |
| 4    | Cross-object matching (if applicable)  | Contact-to-Lead matching rules, confidence thresholds                                      |
| 5    | Master record survivorship rules       | Field-level: most complete, most recent, non-null. Always preserve opt-out. Related records.|
| 6    | Real-time duplicate prevention         | Alert/block on record creation. Form submission prevention. Import duplicate checking.     |
| 7    | Automated merge workflows              | Schedule (daily/weekly). High-confidence auto-merge. Lower-confidence to review queue.     |
| 8    | Manual review queue                    | Assignment rules, review criteria checklist, unmerge capability confirmed                  |
| 9    | Dashboard/reporting                    | Duplicate rate trending, merge volume, queue backlog, false positive tracking              |

**CRM-specific considerations:**

**Salesforce:**
- Use native Duplicate Rules + Matching Rules for prevention (up to 5 active per object) [2]
- Third-party tool handles fuzzy matching and automation beyond native capabilities
- Test that Duplicate Rules do not conflict with third-party tool's real-time detection

**HubSpot:**
- Disable "auto-create company from contact activity" if Salesforce is source of truth [1]
- Native dedup requires Professional or Enterprise subscription; bulk dedup requires Operations Hub [3]
- Third-party tools (Insycle, Koalify, Dedupely) provide automation that HubSpot native lacks

**Build tracking:**

- [ ] Tool account created and CRM connected
- [ ] Contact/Lead matching rules configured
- [ ] Account/Company matching rules configured
- [ ] Cross-object matching configured (if applicable)
- [ ] Survivorship rules defined and configured
- [ ] Real-time prevention active
- [ ] Automated merge workflow scheduled
- [ ] Manual review queue operational
- [ ] Dashboard/reporting built

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify all configurations work correctly and get customer approval before production rollout.

**Two types of testing:**

| Type              | Who      | Purpose                                                                   |
| ----------------- | -------- | ------------------------------------------------------------------------- |
| Technical Testing | Our team | Verify matching accuracy, false positive/negative rates, merge integrity  |
| Customer Testing  | Customer | Verify tool catches their known duplicates, doesn't merge non-duplicates  |

**Technical testing checklist:**

- [ ] Matching rules correctly identify known duplicate pairs (true positives)
- [ ] Matching rules do not flag known non-duplicate pairs (false positive rate acceptable — target &lt;5%)
- [ ] Matching rules catch fuzzy matches (name variations, typos, abbreviations)
- [ ] Cross-object matching works correctly (Contact vs. Lead)
- [ ] Master record selection follows survivorship rules
- [ ] Field-level survivorship preserves correct values (most recent, most complete, non-null)
- [ ] Opt-out/unsubscribe preferences always preserved from any merged record
- [ ] Related records (activities, opportunities, notes) transfer correctly to master
- [ ] Real-time prevention fires on record creation (alerts/blocks as configured)
- [ ] Prevention works for form submissions and data imports
- [ ] Automated merge workflow runs on schedule with correct thresholds
- [ ] Low-confidence matches route to manual review queue
- [ ] Unmerge/rollback capability confirmed working
- [ ] Dashboard displays accurate metrics

**Initial production run (preview mode):**

1. Generate preview report of all detected duplicates across objects
2. Review preview with client RevOps team — flag any unexpected matches
3. Address false positives by adjusting rules or thresholds
4. Execute merge on approved duplicates (high confidence first, then reviewed lower confidence)
5. Verify post-merge: related records intact, no broken workflows, audit trail complete
6. Generate post-merge report: records merged, duplicate rate reduction, remaining queue

**Engineering sign-off checkpoint:**

- [ ] All matching rules tested and validated
- [ ] False positive rate below 5%
- [ ] Initial duplicate backlog cleared via approved preview merge
- [ ] Post-merge data integrity verified
- [ ] Automation running on schedule
- [ ] Customer has tested and approved results
- [ ] Ready for enablement

**Decision point:**

- **Proceed to Enablement** — Tool configured, tested, initial backlog cleared
- **Loop back to Build** — False positive rate too high, rules need adjustment

---

## Phase 3: Enablement

> **Goal:** RevOps team can independently operate the deduplication tool: manage the manual review queue, run on-demand scans, adjust rules, and troubleshoot.
>
> **Output:** Trained team with documentation, stabilized tool running in production, no critical issues.

### Sub-Phases

```
3a Training Prep --> 3b Training Sessions --> 3c Hypercare --> 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from the configuration spec and build documentation.

**Input:** Configuration spec + tech spec + built/tested tool + post-merge report

**What happens:**

1. Create video walkthrough scripts (dashboard, review queue, on-demand scan)
2. Write manual review SOP (when to merge, when to reject, when to escalate)
3. Create quick-reference guide (common tasks: run scan, review queue, adjust threshold, unmerge)
4. Draft FAQ from common questions encountered during build and testing

**Output:** Training package containing:

- Video walkthrough scripts (3 videos: dashboard overview, manual review process, on-demand scanning + unmerge)
- Manual Review SOP (decision criteria, merge checklist, escalation triggers)
- Quick-reference guide (1-page task reference)
- FAQ document (10-15 common questions with answers)

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to the RevOps/Sales Ops team.

**Two types of training:**

| Type                | Audience                         | Focus                                                                        |
| ------------------- | -------------------------------- | ---------------------------------------------------------------------------- |
| Leadership training | VP Sales, VP Marketing           | Why dedup matters: duplicate records waste 27% of rep selling time [4]. Dashboard metrics, ROI tracking. |
| Technical handoff   | RevOps, Sales Ops, CRM Admin    | Manual review queue operation, on-demand scanning, rule adjustment, unmerge   |

**Technical training session (45 min):**

1. Dashboard walkthrough: duplicate rate trending, merge volume, queue backlog
2. Manual review queue: how to review, merge, reject, and escalate matches
3. On-demand scanning: how to run a scan outside the automated schedule
4. Rule adjustment: when and how to modify matching thresholds
5. Unmerge/rollback: how to reverse an incorrect merge
6. Automation monitoring: how to verify scheduled runs are executing

**Leadership training session (20 min):**

1. Dashboard metrics overview: duplicate rate, reduction trend, queue health
2. Business impact: 10-30% of CRM records are typically duplicates, costing $12.9M annually in poor data quality for the average organization [5][6]
3. Success criteria: maintain duplicate rate below 5% ongoing, queue processed weekly

**Training delivery:**

1. Schedule sessions with appropriate stakeholders
2. Deliver live training (record for future reference)
3. Record supplementary video walkthroughs for async consumption
4. Answer questions, note gaps for FAQ updates

**Output:**

- Trained RevOps team
- Video walkthrough recordings (3 videos)
- Updated FAQ based on training questions

---

### 3c. Hypercare

> **Purpose:** Intensive post-launch support to stabilize the tool and build team confidence.

**Duration:** 30 days

**What happens:**

- Weekly 30-minute office hours: RevOps team can ask questions, review queue together, troubleshoot
- Monitor automated merge runs: verify no errors, check false positive reports
- Review and adjust matching thresholds if false positive or negative rates shift
- Support the team through their first full manual review queue cycle
- Address any new duplicate sources discovered (new integration, new form, new import process)

**What is in scope:**
- Threshold adjustments based on production data
- Queue review support and merge decision guidance
- Minor rule modifications (adding a secondary matching field, adjusting fuzzy tolerance)

**What is out of scope:**
- Adding entirely new objects to dedup (requires scoping as new project)
- Changing the dedup tool (requires new procurement cycle)
- CRM-MAP sync reconfiguration (separate project)

**When to skip:** Never — every CRM deduplication tool deployment needs a hypercare period. Production data always surfaces edge cases that testing does not.

**Output:** Stabilized tool, no critical issues, team processing manual review queue independently

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm customer team can operate the dedup tool independently.

**Validation checkpoint:**

- [ ] All training sessions delivered
- [ ] Training recordings and documentation provided
- [ ] Hypercare period complete (30 days)
- [ ] Manual review queue being processed on schedule by RevOps team
- [ ] No critical issues outstanding
- [ ] Automated merges running without errors
- [ ] Team can run on-demand scans without support
- [ ] Team understands when to escalate
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** — Team is enabled, tool stabilized
- **Extend Hypercare** — Queue backlog growing, team not yet confident, rule tuning still needed

---

## Phase 4: Handoff

> **Goal:** Clean project close with maintenance plan established and retention/expansion path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the tool, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule --> 4b Internal Handoff --> 4c External Handoff --> 4d Project Close
                          (SME --> Architect)       (Team --> Customer)    (Archive + Debrief)
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At                                                                         |
| ----------------------------- | -------------------- | ------------------------------------------------------------------------------------- |
| **Single Project**            | Customer owns        | 4c (External Handoff) — customer receives maintenance schedule and runs it themselves |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) — Architect receives maintenance schedule and runs it for customer     |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention to keep the dedup tool effective and duplicate rates low.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task                  | What to Check                                         | Red Flag Threshold                                |
| ----------------------------- | ----------------------------------------------------- | ------------------------------------------------- |
| Manual Review Queue           | Queue backlog size, processing frequency               | >50 unreviewed matches (queue growing, not shrinking) |
| Duplicate Rate Trending       | Current duplicate rate vs. previous month              | Rate increasing >2% month-over-month              |
| Automation Run Verification   | Scheduled merges executing, no errors in logs          | Any failed run or error notification              |
| New Data Source Check         | Any new integrations, forms, or import processes added | New source without prevention rules configured    |

**Quarterly Tasks:**

| Quarterly Task                   | What to Review                                          | Action if Off-Track                              |
| -------------------------------- | ------------------------------------------------------- | ------------------------------------------------ |
| Matching Rule Accuracy Audit     | False positive and false negative rates from review queue| Adjust thresholds or add/remove matching fields  |
| Survivorship Rule Review         | Are the right field values surviving merges?             | Update survivorship logic if business rules changed |
| Cross-Object Match Effectiveness | Contact-to-Lead matching catching real duplicates?       | Adjust cross-object thresholds or criteria       |
| Tool License Review              | Usage vs. license limits, feature utilization            | Downgrade/upgrade if usage patterns changed      |

**After First Business Cycle (30-90 days post-launch):**

- Duplicate rate reduction: target 80%+ reduction from baseline within 90 days
- Ongoing duplicate rate: should be below 5% and trending toward 2% [6]
- Manual review queue velocity: team processing queue within 1 week of matches appearing
- False positive rate: below 5% of flagged matches

**Refinement Triggers (when to re-engage):**

| Trigger                          | Threshold                                | Response                                              |
| -------------------------------- | ---------------------------------------- | ----------------------------------------------------- |
| Duplicate rate climbing          | >5% for 2+ consecutive months            | Investigate new sources, adjust prevention rules      |
| False positive rate spiking      | >10% of flagged matches are non-dupes    | Re-tune matching thresholds, review fuzzy tolerance   |
| Queue backlog growing            | >100 unreviewed matches for 30+ days     | Re-train team, adjust auto-merge threshold upward     |
| New CRM integration added        | Any new data source connected to CRM     | Configure prevention rules for new source immediately |

**Every 6-12 Months:**

- Full matching rule recalibration: test rules against fresh data sample, update thresholds
- Tool version/feature review: evaluate new capabilities released by vendor
- Compliance review: verify opt-out preservation rules still meet current regulations
- Duplicate source analysis: reassess which entry points generate the most duplicates

---

### 4b. Internal Handoff (SME → Architect)

> **Purpose:** Transfer context so the Architect can manage the ongoing relationship.

**What the Architect needs to know:**

- Tool name, version, and login credentials (admin vs. read-only)
- Automation schedule (what runs when, who gets notified)
- Current duplicate rate and trend direction
- Manual review queue cadence and who processes it
- Common issues and how to resolve (see troubleshooting guide below)
- When to escalate back to SME

**Escalation guidelines:**

| Issue Type                                          | Who Handles                      | Example                                             |
| --------------------------------------------------- | -------------------------------- | --------------------------------------------------- |
| Queue review questions, minor threshold adjustments | Architect                        | "Should we merge these two?" "Queue is backed up."  |
| Rule changes, new object dedup, survivorship changes| SME                              | "We need to dedup Deals now." "Matching rules wrong."|

**Troubleshooting Guide:**

| Scenario                                    | Resolution                                                                                           |
| ------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| Automated merge run failed                  | Check tool dashboard for error logs. Common cause: API rate limit exceeded. Reduce batch size or reschedule to off-peak. |
| False positive reported by sales rep         | Review the flagged pair in tool. If legitimate non-duplicate, reject and note pattern. If pattern repeats, adjust matching threshold. |
| Duplicates re-entering after cleanup         | Check for new data sources without prevention rules. Verify form submissions and imports have dedup checks active. |
| Opt-out preference lost after merge          | Check survivorship rules — opt-out must be "keep most restrictive." If misconfigured, fix immediately and notify compliance. Attempt unmerge if available. |
| HubSpot-Salesforce sync creating duplicates  | Verify HubSpot "auto-create company" setting is disabled. Check sync conflict resolution rules. Ensure dedup tool runs after sync, not before. |
| Manual review queue growing faster than team processes | Raise auto-merge confidence threshold to reduce queue volume. Or add reviewers. Or increase automation frequency. |

**For Dedicated engagements:** Architect also receives the maintenance schedule (4a) and becomes responsible for executing it. SME walks Architect through each maintenance task in the internal handoff meeting.

---

### 4c. External Handoff (Delivery Team → Customer)

> **Purpose:** Formal project completion with customer.

**Final project meeting:**

- Review what was delivered: tool configured, rules active, initial backlog cleared, automation running
- Walk through documentation package
- Walk through maintenance schedule in detail (monthly, quarterly, annual tasks)
- Demo unmerge/rollback one more time as a safety refresher
- Confirm nothing outstanding
- Answer final questions
- Make it explicit: "Project complete"
- **For Single Project engagements:** Hand over the maintenance schedule and walk through each task. Record a video walkthrough of the maintenance process.

**Documentation package:**

- Tool Configuration Runbook (all rules, thresholds, settings documented)
- Automation Schedule Document (what runs when, notification recipients)
- Manual Review SOP (merge/reject criteria, escalation triggers)
- Quick-Reference Guide (common tasks 1-pager)
- All training video walkthrough recordings (3 videos)
- FAQ document
- Definition Alignment Document (final version)
- Maintenance Schedule
- Support contact info

**Output:** Customer owns the deduplication tool and ongoing management. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location (audit report, configuration runbook, training materials)
- [ ] Handoff documentation complete
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized

#### Internal Debrief (Optional but Recommended)

- What went well? (Tool selection speed, rule accuracy, training effectiveness)
- What would we do differently? (Better test data, earlier compliance involvement, different tool)
- Any learnings to feed back into SOPs? (New matching patterns, tool-specific quirks)

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell → Downsell → Retry |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (retainer -- ongoing dedup monitoring + rule tuning)
   | if no
2. Downsell: Another one-time project (CRM Data Enrichment, Lead Routing, Data Governance)
   | if yes
3. Retry retainer at end of next project cycle
```

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On [date ~quarter out], we'll review how the dedup tool is performing — duplicate rate trends, queue health, whether matching rules need adjustment."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                                     |
| ------------------- | ---------------------------------------------------------------- |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks                 |
| 2. Review metrics   | Pull duplicate rate trend, queue backlog, automation run history |
| 3. Decide ownership | Can Architect handle this check-in, or need SME?                |
| 4. Prep materials   | If SME needed, brief them. If Architect, prep talking points.   |

**At the refinement check-in:**

- Review duplicate rate against target (&lt;5% ongoing, &lt;2% best-in-class)
- Check manual review queue health
- Identify any rule adjustments needed
- If minor: Architect handles threshold tweaks
- If major: Scope refinement project (new objects, new matching patterns, tool migration)

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- Duplicate Audit Report (baseline rates, sources, patterns per object)
- Tool Comparison Matrix (evaluated options with recommendation)
- Definition Alignment Document (signed-off terms)
- Configuration Spec (matching rules, survivorship, thresholds, automation schedule)

**Technical Deliverables:**

- Configured deduplication tool with active matching rules for Contacts/Leads and Accounts/Companies
- Master record survivorship rules configured (field-level, opt-out preservation)
- Real-time duplicate prevention active on record creation, forms, and imports
- Automated merge workflow running on defined schedule
- Manual review queue with assignment rules and review criteria
- Monitoring dashboard (duplicate rate trending, merge volume, queue backlog)

**Documentation Package:**

- Tool Configuration Runbook
- Automation Schedule Document
- Manual Review SOP
- Quick-Reference Guide (common tasks 1-pager)
- Training video walkthrough recordings (3 videos)
- FAQ document
- Definition Alignment Document (final version)
- Maintenance Schedule

---

## Appendix: Reference Guide

### Phase Outputs & Gate Criteria

| Phase                    | Output                                                                     | Gate Criteria                                                                   |
| ------------------------ | -------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| **Phase 1: Strategy**    | Tool selected, configuration spec signed off (rules, survivorship, thresholds) | RevOps and compliance stakeholders approved, tool procured                     |
| **Phase 2: Engineering** | Configured and tested dedup tool, initial backlog cleared                  | All rules tested, false positive rate &lt;5%, customer approved preview merge      |
| **Phase 3: Enablement**  | Trained team with documentation, stabilized tool                           | All training delivered, 30-day hypercare complete, team operating independently |
| **Phase 4: Handoff**     | Independent customer + archived project                                    | Internal/external handoffs complete, maintenance plan in place, project closed  |

### Project Profile

| Project Profile    | Strategy Weight | Engineering Weight | Enablement Weight | Notes                                    |
| ------------------ | --------------- | ------------------ | ----------------- | ---------------------------------------- |
| **CRM Dedup Tool** | 20-30%          | 50-60%             | 15-20%            | Engineering-heavy: tool config is the core work |

### Key Data Points

Organizations lose an estimated $12.9 million annually due to poor data quality [5]. In a typical B2B CRM, 10-30% of records are duplicates [6], and sales reps lose approximately 27% of their working hours — about 546 hours per year — dealing with bad or duplicate prospect data [4]. Best-in-class organizations maintain duplication rates below 2%, while anything above 5% signals a significant problem [6].

### CRM-Specific Technical Notes

#### Salesforce Duplicate Management

Salesforce provides native Duplicate Rules and Matching Rules [2]:
- Up to 5 active Duplicate Rules per object
- Up to 5 active Matching Rules per object (3 matching rules per duplicate rule)
- Duplicate Rules can warn users, block creation, or allow with alert
- Duplicate Rules do NOT fire on API-created records, recycle bin restores, or manual merges
- Third-party dedup tools fill gaps: fuzzy matching, automation, cross-object, bulk operations

Start with warning-only mode to assess volume before enforcing blocks.

#### HubSpot Duplicate Management

HubSpot provides native deduplication [3]:
- Automatic dedup on email address for Contacts
- Duplicate Manager tool requires Professional or Enterprise subscription
- Bulk duplicate management requires Operations Hub Professional or Enterprise
- Native tool does not support automated scheduled merges
- Third-party tools (Insycle, Koalify, Dedupely) add automation, custom matching rules, and scheduling
- Disable "auto-create company from contact activity" if syncing with Salesforce

#### Cross-Platform Sync Considerations

When the client runs both HubSpot and Salesforce with a sync:
- Determine source of truth per object (usually Salesforce for Accounts, HubSpot for marketing Contacts)
- Run dedup AFTER sync completes, not before — otherwise sync re-creates merged records
- Align dedup rules across both platforms to prevent one system's merge from conflicting with the other
- Disable HubSpot auto-create company setting to prevent phantom Account duplicates

### Troubleshooting Reference

| Scenario | Symptoms | Root Cause | Resolution |
| -------- | -------- | ---------- | ---------- |
| Automated merge run failed | Error notification, no merges completed | API rate limit exceeded, CRM maintenance window, expired credentials | Check tool error logs. If rate limit: reduce batch size or reschedule off-peak. If credentials: re-authenticate. |
| False positives flagged by users | "These aren't the same person" | Matching threshold too low, fuzzy matching too aggressive | Review flagged pair. If pattern: raise threshold for that rule. If one-off: reject and move on. |
| Duplicates keep appearing after cleanup | Duplicate count rising despite automation | New data source without prevention rules, import process bypassing checks, sync re-creating records | Audit all data entry points. Configure prevention for any unprotected source. Check sync timing. |
| Opt-out/consent data lost after merge | Compliance alert, contacts receiving emails after opting out | Survivorship rule not preserving most restrictive opt-out | Fix survivorship rule immediately. Notify compliance. Attempt unmerge. Audit all recent merges for same issue. |
| Wrong master record selected | Important record data overwritten | Survivorship criteria not matching business intent | Review master selection logic. Unmerge if possible. Adjust survivorship rules. Re-test with similar scenarios. |
| Tool not detecting known duplicates | Manual review finds missed duplicates | Matching fields too narrow, fuzzy tolerance too strict | Expand matching criteria (add secondary fields). Lower fuzzy threshold. Consider cross-field matching. |
| HubSpot-Salesforce sync conflict | Records merged in one system reappear as duplicates in the other | Sync runs before or during dedup. Auto-create company setting still enabled. | Reschedule dedup to run after sync. Verify auto-create setting disabled. Align rules across platforms. |
| Manual review queue overwhelming team | Queue growing faster than team can review | Auto-merge threshold too conservative | Raise auto-merge confidence threshold. Add reviewers. Increase automation frequency. |

---

## References

[1] [HubSpot - Deduplication of Records](https://knowledge.hubspot.com/records/deduplication-of-records)

[2] [Salesforce Ben - Complete Guide to Salesforce Duplicate Rules](https://www.salesforceben.com/salesforce-duplicate-rules/)

[3] [HubSpot - Operations Hub Duplicate Management](https://www.smartbugmedia.com/blog/hubspot-operations-hub-to-manage-duplicate-records)

[4] [SalesForge - How Duplicate Data Impacts Sales Outreach](https://www.salesforge.ai/blog/how-duplicate-data-impacts-sales-outreach)

[5] [Gartner via Databar - Duplicate Record Management in CRM: The Hidden Revenue Killer](https://databar.ai/blog/article/duplicate-record-management-in-crm-the-hidden-revenue-killer-and-how-to-fix-thousands-fast)

[6] [Landbase - CRM Match Rate Statistics: 25 Key Facts Every B2B Marketer Should Know](https://www.landbase.com/blog/crm-match-rate-statistic)

[7] [Insycle - HubSpot Deduplication &amp; Integration Tools](https://www.insycle.com/hubspot/deduplication/)

[8] [Openprise - CRM Data Deduplication Software](https://www.openprisetech.com/revops-data-automation-platform/capabilities/orchestrate-data/deduplication/)
