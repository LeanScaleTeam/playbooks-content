# CRM Deduplication — Implementation

## Project One-Pager

> Quick reference for architects. One per project type. Fill this out FIRST — it serves as the project's identity card.

### CRM Deduplication One-Pager

#### Project Type

- Category: Technical
- Primary Deliverable: Clean CRM database with &lt;5% duplicate rate, prevention rules in place, and data governance SOP

##### Phase Relevance

| Phase          | Applies? | Notes                                                  |
| -------------- | -------- | ------------------------------------------------------ |
| 1. Strategy    | Yes      | 2-3 meetings: audit review, matching rules, sign-off   |
| 2. Engineering | Yes      | Tool configuration, batch dedup execution, QA           |
| 3. Enablement  | Yes      | One training session + quick-reference card              |
| 4. Handoff     | Yes      | Governance SOP, recurring scan setup, ownership transfer |

· · ·

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │    Medium    │     │    Heavy     │     │    Light     │     │    Medium    │
  │ 1a→1b→1c→1d │     │ 2a→2b→2c→2d │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   2-3 meetings         Tool config +        One training +       Governance SOP
   audit + rules        batch dedup          reference card       + recurring scans
```

**This project's flow:**
- Full 4-phase. Light-to-medium strategy (audit + matching rules), heavy engineering (tool config + batch processing), light enablement (training on prevention), medium handoff (governance + recurring scans).
- Engineering is the heaviest phase — extended deduplication processing and data integrity verification take the most time.
- Some customers skip 3c Hypercare if duplicate rates are already low post-cleanup and prevention rules are solid.

· · ·

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Provide CRM admin credentials or sandbox access
- [ ] Confirm which objects to deduplicate (contacts, leads, accounts, or all)
- [ ] List custom fields and integration IDs that must be preserved during merges
- [ ] Complete CRM backup before deduplication begins
- [ ] Identify any active integrations that affect duplicate handling (e.g., HubSpot-Salesforce sync)

##### Track B: Architect Prep
- [ ] Pull sample data export from CRM (last 90 days of created records minimum)
- [ ] Run native CRM duplicate detection report to quantify baseline
- [ ] Categorize duplicates by type: exact email, fuzzy name, company variations
- [ ] Calculate duplicate percentage per object
- [ ] Identify top 5 duplicate creation sources (web forms, imports, manual, integrations)
- [ ] Document sample duplicate clusters showing merge complexity

· · ·

#### Refinement Loop (1b --> 1c --> 1d)

| Meeting      | Sub-Phase | Focus                                              | Stakeholder                    | Output                           |
| ------------ | --------- | -------------------------------------------------- | ------------------------------ | -------------------------------- |
| Kickoff      | 1b        | Present audit findings, review duplicate landscape  | RevOps Manager, CRM Admin      | Validated baseline + pain points |
| Refinement 1 | 1c        | Define matching criteria and master record rules    | RevOps Lead, Sales Ops, Mktg Ops | Approved deduplication rules     |
| Sign-Off     | 1d        | Confirm rules, tool selection, and execution plan   | All stakeholders               | Green light for engineering      |

· · ·

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held — audit findings reviewed
- [ ] 1c. Matching criteria and master record rules approved
- [ ] 1d. Strategic sign-off obtained — tool selected, execution plan confirmed

##### Phase 2: Engineering
- [ ] 2a. Tech spec created (tool config + matching rules documented)
- [ ] 2b. Engineering handoff meeting held
- [ ] 2c. Build complete (tool configured, test batch run, full dedup executed)
- [ ] 2d. QA/Test + customer sign-off on data integrity

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped (prevention guide, quick-reference card)
- [ ] 3b. Training sessions delivered (sales + marketing teams)
- [ ] 3c. Hypercare period complete (if applicable — 2 weeks)
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented (recurring scans, review SLAs)
- [ ] 4b. Internal handoff (SME --> Architect) complete
- [ ] 4c. External handoff (LeanScale --> Customer) complete
- [ ] 4d. Project closed and archived

· · ·

#### Document Types

##### Working Documents (iterate together)

| Document                          | Purpose                                                | When Complete                                  |
| --------------------------------- | ------------------------------------------------------ | ---------------------------------------------- |
| Duplicate Audit Report            | Quantify baseline duplicate rates per object            | All objects audited with rates documented       |
| Matching Criteria Worksheet       | Define primary/secondary matching rules + thresholds    | Rules approved by RevOps lead and CRM admin     |
| Master Record Selection Hierarchy | Define which record wins in merge scenarios             | Hierarchy approved with edge cases documented   |
| Deduplication Execution Log       | Track batch processing results and exceptions           | All batches processed and verified              |

##### Deliverables (polished outputs)

| Deliverable                      | Created From                    | Customer Uses For                     |
| -------------------------------- | ------------------------------- | ------------------------------------- |
| Data Governance SOP              | Matching criteria + merge rules | Ongoing duplicate prevention          |
| Deduplication Results Report     | Execution log                   | Stakeholder reporting, ROI tracking   |
| Quick-Reference Card             | Training materials              | Day-to-day data entry guidance        |

· · ·

#### Enablement Details

##### Training Types

| Type       | Audience                        | Focus                                              | Duration |
| ---------- | ------------------------------- | -------------------------------------------------- | -------- |
| End User   | Sales reps, Marketing team      | How to search before creating, respond to alerts   | 30 min   |
| Technical  | RevOps Admin, CRM Administrator | How to run scans, interpret results, adjust rules  | 45 min   |

##### Hypercare
- Applies: Yes (optional — skip if duplicate rate under 3% post-cleanup)
- Duration: 2 weeks
- Office Hours: Yes — weekly 30-min slot for duplicate questions and edge cases

##### Training Assets to Create
- [ ] Video walkthrough: Duplicate alert walkthrough (what happens when you try to create a duplicate)
- [ ] Video walkthrough: How to search for existing records before creating new ones
- [ ] Doc: Quick-reference card with data entry standards
- [ ] Doc: Data Governance SOP (matching rules, scan schedule, escalation path)

· · ·

#### Handoff & Retention

##### Internal Handoff (SME --> Architect)
- Key context for Architect: Deduplication rules, tool configuration, recurring scan schedule, and common edge cases
- Escalation trigger: Any changes to matching criteria, integration changes that affect duplicate handling, or extended data imports exceeding 1,000 records

##### External Handoff (LeanScale --> Customer)
- Final meeting agenda: Review dedup results, walk through governance SOP, confirm scan schedule, demonstrate tool admin
- Documentation package: Data Governance SOP, dedup results report, training recordings, quick-reference card

##### Maintenance Schedule
- Weekly or monthly automated duplicate scans (depending on record creation volume)
- Who owns: Single project = customer RevOps team owns | Dedicated = Architect owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services --> if no --> Downsell: CRM Deduplication Ongoing Tool project or Data Enrichment project --> Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~90 days post-cleanup
- Internal prep trigger: 2 weeks before
- Decision: Architect handles if scan results are clean / SME needed if duplicate rate creeping above 5%

· · ·

#### Key Assets

| Asset                            | When Used              |
| -------------------------------- | ---------------------- |
| Duplicate Audit Report Template  | Phase 1 — Pre-Kickoff |
| Matching Criteria Worksheet      | Phase 1 — Strategy    |
| Deduplication Execution Log      | Phase 2 — Engineering |
| Data Governance SOP Template     | Phase 4 — Handoff     |
| Quick-Reference Card Template    | Phase 3 — Enablement  |

· · ·

#### Definition Alignment Terms

| Term                       | Typical Definition                                                                                     |
| -------------------------- | ------------------------------------------------------------------------------------------------------ |
| Duplicate                  | Two or more records representing the same real-world entity (person, company) in the CRM               |
| Master Record              | The surviving record after a merge — selected based on the master record hierarchy                     |
| Exact Match                | Two records sharing an identical value in the primary matching field (e.g., same email address)         |
| Fuzzy Match                | Two records with similar but not identical values that likely represent the same entity                 |
| False Positive             | Records flagged as duplicates that are actually distinct entities                                       |
| False Negative             | Actual duplicates that were not detected by the matching rules                                         |
| Merge                      | Combining two or more duplicate records into a single master record, preserving key data               |
| Duplicate Rate             | Percentage of total records that are duplicates (target: under 5% post-cleanup, under 1% at maturity) |
| Prevention Rule            | CRM configuration that blocks or warns when a user attempts to create a duplicate record               |
| Recurring Scan             | Scheduled automated process that identifies new duplicates for review                                  |

· · ·

#### Common Gotchas

- Merging records while HubSpot-Salesforce integration is active can break sync or create orphaned records --> Pause sync during extended merge operations, test in sandbox first
- Free email domains (Gmail, Yahoo, Hotmail) trigger false positive matches --> Exclude free email domains from exact email matching or add secondary criteria for these
- Native CRM tools only catch exact matches and miss "Bob" vs "Robert" or "Inc." vs "Incorporated" --> Use third-party tools with fuzzy matching and phonetic algorithms for B2B contexts
- Running full deduplication without a CRM backup --> Always verify backup completion with client IT/admin before any merge operation
- Treating deduplication as a one-time event --> Duplicates return within weeks without prevention rules. Always pair cleanup with automation.
- Merging records with linked opportunities can reassign revenue --> Verify opportunity ownership and related record linkages before processing account-level merges

· · ·

#### Methodology Options

| Option                      | When to Use                                                     | Complexity |
| --------------------------- | --------------------------------------------------------------- | ---------- |
| Native CRM Tools Only       | Small database (&lt;5K records), tight budget, exact matches only  | Low        |
| Third-Party Tool (Insycle, Cloudingo, DemandTools) | Mid-to-large database, need fuzzy matching, extended processing | Medium     |
| Custom Script + Tool Hybrid | Enterprise databases (>500K records), complex matching logic    | High       |

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on deduplication rules, tool selection, and execution plan.
>
> **Output:** Approved matching criteria document + master record selection hierarchy + tool decision.

### 1a. Pre-Kickoff

> Two parallel tracks run after the AE closes and before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                     | Format             |
| ----------------------------- | ----------------------------------------------------------- | ------------------ |
| Intro video                   | Explain what CRM deduplication is and why it matters         | Video walkthrough (5-10 min)    |
| Definition Alignment Document | Get stakeholder sign-off on key terms (duplicate, merge, master record) | Google Doc  |
| Pre-filled intake form        | Confirm CRM platform, objects to dedup, known problem areas  | Google Form or Doc |

**CRM Deduplication intake items:**
- CRM platform (Salesforce, HubSpot, or other)
- Estimated record counts per object (contacts, leads, accounts)
- Known problem areas (specific duplicate scenarios, recent bad imports)
- Active integrations that may affect duplicate handling
- Custom fields or integration IDs that must be preserved
- Budget range for third-party deduplication tools

**Completion tracking:** RevOps manager or CRM admin is the point of contact. Don't cancel kickoff if incomplete, but push hard — we need CRM access to run the audit.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                            | Output                                 |
| ---- | ----------------------------------------------------------------- | -------------------------------------- |
| 1    | Get CRM access, pull sample data exports                          | Raw data for analysis                  |
| 2    | Run native duplicate detection report                             | Baseline duplicate rates per object    |
| 3    | Categorize duplicates (exact email, fuzzy name, company variants) | Pattern analysis                       |
| 4    | Identify top duplicate creation sources                           | Source ranking (forms, imports, manual) |
| 5    | Document sample duplicate clusters                                | Visual examples for kickoff            |
| 6    | Draft initial matching criteria recommendations                   | Starting point for discussion          |

**Critical:** Mark everything as ASSUMED. The kickoff call validates. Duplicate rates and patterns are directional until confirmed with stakeholders who know their data.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building anything.

| Term             | Our Definition                                                                          | Internally Approved? |
| ---------------- | --------------------------------------------------------------------------------------- | -------------------- |
| Duplicate        | Two or more CRM records representing the same real-world person or company              | [ ] Yes / [ ] No     |
| Master Record    | The surviving record after merge, selected by the approved hierarchy                    | [ ] Yes / [ ] No     |
| Exact Match      | Records sharing identical values in the primary matching field (email)                  | [ ] Yes / [ ] No     |
| Fuzzy Match      | Records with similar but not identical values that likely represent the same entity      | [ ] Yes / [ ] No     |
| Merge            | Combining duplicate records into one master record while preserving critical data        | [ ] Yes / [ ] No     |
| Duplicate Rate   | Percentage of total records identified as duplicates                                    | [ ] Yes / [ ] No     |
| Prevention Rule  | System-enforced block or warning when creating a potential duplicate                    | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your RevOps and CRM administration team. Check "Yes" when approved. We need alignment on these terms before defining matching rules and executing merges.

---

### 1b. Kickoff Call

> **Purpose:** Present the duplicate audit findings and get alignment on scope and pain points. We walk in with work done — customer reacts, not creates from scratch.

#### Agenda (60 min)

| Time  | Topic                          | What Happens                                                  |
| ----- | ------------------------------ | ------------------------------------------------------------- |
| 0-15  | Walk through audit findings    | "Here's what we found in your CRM: X% duplicates, Y patterns" |
| 15-30 | Validate patterns and sources  | ASSUMED patterns --> CONFIRMED or corrected by stakeholders    |
| 30-40 | Gather pain points             | Sales rep frustrations, marketing email issues, reporting gaps |
| 40-50 | Review definition alignment    | Review Definition Alignment Document                          |
| 50-60 | Next steps                     | Schedule rules review meeting, assign homework                |

#### What We Bring

- Duplicate Audit Report (baseline rates per object, pattern analysis, source ranking)
- Sample duplicate clusters (visual examples of merge complexity)
- Draft matching criteria recommendations
- Definition Alignment Document (pre-filled with our recommendations)

#### What We Leave With

- Confirmed duplicate rates and patterns
- Prioritized pain points from sales, marketing, and CRM admin
- List of custom fields and integration IDs to preserve
- Understanding of any integration constraints (e.g., HubSpot-Salesforce sync)
- Homework: client to provide business rules for master record selection

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Finalize matching criteria and master record rules before any merges happen.

#### The Pattern

```
Kickoff Call (present audit, gather pain points)
    |
Architect drafts matching criteria + master record hierarchy
    |
Meeting 2 (present rules, refine thresholds, select tool)
    |
Architect finalizes rules document
    |
Sign-Off (approve everything before engineering)
```

#### Meeting 2: Matching Rules Review

| Time  | Topic                          | What Happens                                                    |
| ----- | ------------------------------ | --------------------------------------------------------------- |
| 0-15  | Present matching criteria      | Primary (email), secondary (name+company), fuzzy thresholds     |
| 15-30 | Present master record hierarchy | Most recent activity > most complete data > oldest created date |
| 30-40 | Tool recommendation            | Native CRM tools vs. Insycle, Cloudingo, DemandTools            |
| 40-50 | Edge cases discussion          | Free email domains, multi-subsidiary accounts, partial records  |
| 50-60 | Approval and next steps        | Get sign-off or identify remaining questions                    |

#### Typical Timeline

| Milestone               | Timing                                    |
| ----------------------- | ----------------------------------------- |
| Pre-kickoff prep        | 2-3 days                                  |
| Kickoff call            | Day 1 of engagement                       |
| Meeting 2 (rules)       | 3-5 days after kickoff                    |
| Sign-off                | Same meeting as rules review, or +2 days  |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything before merging any records.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off
- [ ] Matching criteria (primary + secondary) approved
- [ ] Master record selection hierarchy approved
- [ ] Fuzzy matching thresholds agreed
- [ ] Special handling rules documented (free email domains, integration IDs)
- [ ] Tool selected and budget approved
- [ ] CRM backup verified
- [ ] Customer understands the execution plan (test batch --> full dedup --> prevention)
- [ ] No blockers for engineering

#### Decision Point

- **Proceed to Engineering** --> Rules approved, tool selected, backup confirmed
- **Loop back to Strategy** --> Stakeholder disagreement on matching rules or merge behavior

---

## Phase 2: Engineering

> **Goal:** Configure the deduplication tool, execute the cleanup, and configure prevention rules.
>
> **Output:** Clean CRM database with verified data integrity + prevention rules active.

| Project Type    | Engineering Weight | Notes                                                  |
| --------------- | ------------------ | ------------------------------------------------------ |
| CRM Deduplication | Heavy (60-70%)   | Bulk of effort is tool config, batch execution, QA      |

### Sub-Phases

```
2a Tech Spec --> 2b Engineering Handoff --> 2c Build --> 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate approved matching rules into a technical configuration document.

**Input:** Signed-off matching criteria + master record hierarchy from Phase 1

**What happens:**

1. Map approved matching rules to tool-specific configuration settings
2. Define field merge behavior per field (master value vs. concatenate vs. most recent)
3. Define handling for related records (activities, tasks, opportunities linked to merged records)
4. Document the execution sequence (which objects first, batch sizes, rollback plan)

**Output:** Tech spec containing:

- Tool configuration settings (matching fields, thresholds, merge behavior)
- Field-by-field merge rules (for each CRM field: keep master, keep most recent, concatenate, or ignore)
- Related record handling rules (how activities, opportunities, and tasks transfer)
- Execution plan (object order, batch sizes, verification checkpoints)
- Rollback plan (what happens if something goes wrong)

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs before configuring the tool.

**Who attends:** Architect + CRM Admin (or engineer handling configuration)

**Agenda (30-45 min):**

| Time  | Topic              | What Happens                                                  |
| ----- | ------------------ | ------------------------------------------------------------- |
| 0-15  | Walk through specs | Architect explains matching rules, merge behavior, execution plan    |
| 15-30 | Review edge cases  | Integration constraints, custom field handling, rollback plan |
| 30-45 | Confirm approach   | Agree on tool config, batch sizes, verification checkpoints   |

**What Architect brings:**

- Approved matching criteria from Phase 1
- Draft tech spec (field mapping, merge behavior)
- Questions list (anything needing CRM admin input)

**What we leave with:**

- Approved tech spec
- Clear execution sequence
- CRM admin availability for testing support

---

### 2c. Build (Configure + Execute)

> **Purpose:** Configure the deduplication tool and execute the cleanup.

**Input:** Approved tech spec from 2b

**The build sequence:**

**Step 1: Configure Tool**
1. Install/connect deduplication tool to CRM environment
2. Configure primary matching field (email) with exact match rules
3. Configure secondary matching fields with approved fuzzy match thresholds
4. Set up master record selection logic per approved hierarchy
5. Configure field merge behavior per tech spec
6. Define handling for related records
7. Save configuration and document settings

**Step 2: Test Batch**
1. Select test batch of 300-500 records across objects
2. Run tool in preview mode (no actual merges)
3. Manually review 50+ potential duplicate pairs for accuracy
4. Calculate false positive rate (flagged but not duplicates)
5. Calculate false negative rate (known duplicates missed)
6. Adjust thresholds if false positive rate exceeds 5%
7. Document any edge cases requiring special handling

**Step 3: Execute Full Deduplication**
1. Verify CRM backup is current (confirm with client IT/admin)
2. Start with lowest-risk object (typically contacts before accounts)
3. Process in batches of 500-1,000 records
4. Review batch results before proceeding to next batch
5. Document merge counts per batch: records before, records after, merge ratio
6. Handle exceptions and edge cases flagged during processing
7. Move to next object type after completing current object
8. Generate deduplication results report

**Step 4: Configure Prevention Rules**
1. Enable native duplicate detection rules in CRM
2. Configure alert behavior (block vs. warn) based on match confidence
3. Set up alerts for key entry points: manual creation, lead forms, imports
4. Create validation rules requiring email on contact/lead creation
5. Set up email domain validation (standardize formatting, lowercase)
6. Create workflow to standardize company names at entry
7. Schedule recurring duplicate scans (weekly for high-volume, monthly for lower)
8. Configure scan notification to RevOps admin

**Build tracking:**

- [ ] Component 1: Tool installation and configuration
- [ ] Component 2: Test batch execution and validation
- [ ] Component 3: Contact deduplication (all batches)
- [ ] Component 4: Lead deduplication (all batches)
- [ ] Component 5: Account deduplication (all batches)
- [ ] Component 6: Prevention rules configured
- [ ] Component 7: Recurring scans scheduled

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify merges preserved critical data and related records remain linked.

**Two types of testing:**

| Type              | Who             | Purpose                                                      |
| ----------------- | --------------- | ------------------------------------------------------------ |
| Technical Testing | LeanScale team  | Verify data integrity, related records intact                |
| Customer Testing  | Client RevOps   | Verify key records look correct, reports still work          |

**Technical testing checklist:**

- [ ] Spot-check 20-30 merged records — field values preserved correctly
- [ ] Related records (activities, opportunities, tasks) still linked to surviving records
- [ ] Integration IDs (Salesforce ID, HubSpot ID, etc.) preserved per rules
- [ ] Critical reports and dashboards still return accurate data
- [ ] Prevention rules trigger correctly (test with sample duplicate creation)
- [ ] Recurring scan runs and generates report
- [ ] No errors in CRM logs related to merge operations

**Customer testing:**

- Walk customer through 5-10 merged records they recognize
- Have them run their standard reports to verify data integrity
- Test duplicate alert by attempting to create a known duplicate
- Capture feedback, fix any issues found

**Engineering sign-off checkpoint:**

- [ ] All objects deduplicated per approved rules
- [ ] False positive rate under 5% (verified in test batch)
- [ ] Data integrity verified (spot-checks + report validation)
- [ ] Prevention rules active and tested
- [ ] Recurring scans configured and running
- [ ] Customer has reviewed and approved results
- [ ] Ready for enablement

**Decision point:**

- **Proceed to Enablement** --> Clean database, prevention active, customer approved
- **Loop back to Build** --> Data integrity issues found, additional edge cases to handle

---

## Phase 3: Enablement

> **Goal:** Sales and marketing teams understand duplicate prevention and can maintain data quality.
>
> **Output:** Trained team with documentation, prevention rules understood, governance SOP delivered.

### Sub-Phases

```
3a Training Prep --> 3b Training Sessions --> 3c Hypercare --> 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from the deduplication rules and prevention configuration.

**Input:** Matching criteria + prevention rules + deduplication results

**What happens:**

1. Create end-user training deck covering: what changed, what's in place now, how to respond to alerts
2. Create quick-reference card for data entry best practices
3. Create technical admin guide for running scans and adjusting rules
4. Draft FAQ from common questions encountered during similar projects

**Output:** Training package containing:

- End-user training presentation (30 min)
- Quick-reference card (1 page — search before creating, email format, company name standards)
- Technical admin guide (how to run scans, interpret results, adjust thresholds)
- FAQ document (common duplicate scenarios and how to handle them)

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to customer team so they maintain data quality.

**Two types of training:**

| Type                | Audience                        | Focus                                                           |
| ------------------- | ------------------------------- | --------------------------------------------------------------- |
| End User Training   | Sales reps, Marketing team      | How duplicates hurt their work, what prevention is in place, how to respond to alerts |
| Technical Training  | RevOps Admin, CRM Administrator | How to run scans, interpret results, adjust rules, handle edge cases |

**End User Training (30 min):**

1. Why duplicates matter: "Your pipeline reports were inflated by X%, your emails were bouncing at Y%"
2. What we did: "Merged Z,000 records, here's what changed"
3. What's different now: "You'll see alerts when creating potential duplicates"
4. What to do: "Search before creating, follow the alert guidance, use standard email format"
5. Demo: Create a record that triggers a duplicate alert and show proper response

**Technical Training (45 min):**

1. Tool walkthrough: Admin access, configuration settings, how to adjust matching rules
2. Recurring scan demo: How to run, interpret results, action flagged duplicates
3. Edge case handling: What to do with low-confidence matches requiring manual review
4. Escalation path: When to handle internally vs. when to engage LeanScale

**Training delivery:**

1. Schedule sessions with appropriate stakeholders
2. Deliver training (live, screen-shared)
3. Record for future reference and new employee onboarding
4. Answer questions, note gaps for FAQ update

---

### 3c. Hypercare

> **Purpose:** Post-cleanup support to catch any issues and verify prevention rules work in practice.

**Duration:** 2 weeks (skip if duplicate rate is under 3% post-cleanup and prevention rules are firing correctly)

**What happens:**

- Quick response to duplicate-related questions
- Office hours: weekly 30-min slot where anyone can drop in
- Monitor prevention rule trigger rate — are alerts firing too often (rules too loose) or never (rules too tight)?
- Review first recurring scan results
- Address any data integrity issues discovered post-cleanup

**When to skip:** If the cleanup was small-scope (one object, low duplicate rate), prevention rules passed testing, and the RevOps admin is technically strong.

**Output:** Verified prevention system working in production, no critical issues outstanding.

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm customer can maintain data quality independently.

**Validation checkpoint:**

- [ ] End-user training delivered and recorded
- [ ] Technical admin training delivered
- [ ] Quick-reference card distributed
- [ ] FAQ document delivered
- [ ] Hypercare period complete (if applicable)
- [ ] Prevention rules working as expected (verified by scan results)
- [ ] No critical data integrity issues outstanding
- [ ] Customer team can run scans and handle results without support
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** --> Team is enabled, prevention working, no open issues
- **Extend Hypercare** --> Prevention rules need tuning, or team needs more support time

---

## Phase 4: Handoff

> **Goal:** Clean project close with ongoing governance plan in place and retention/expansion path set.
>
> **Output:** Data Governance SOP delivered, maintenance schedule active, internal context transferred, project archived.

**Structure:**

```
4a Maintenance Schedule --> 4b Internal Handoff --> 4c External Handoff --> 4d Project Close
                          (SME --> Architect)            (LS --> Customer)       (Archive + Debrief)
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance  | Handed Off At |
| ----------------------------- | --------------------- | ------------- |
| **Single Project**            | Customer RevOps team  | 4c — customer receives governance SOP and runs scans themselves |
| **Dedicated (Multi-Project)** | Architect owns               | 4b — Architect receives governance SOP and monitors scan results      |

---

### 4a. Maintenance Schedule

> **Purpose:** Document ongoing data quality activities to prevent duplicate re-creation.

#### Standard Maintenance Framework

**Weekly Tasks (for high-volume databases >10K new records/month):**

| Weekly Task              | What to Check                                    | Red Flag Threshold                             |
| ------------------------ | ------------------------------------------------ | ---------------------------------------------- |
| Review scan results      | New duplicates flagged since last scan            | >20 new duplicates in a single scan            |
| Check prevention alerts  | Alert trigger frequency — too many or too few    | >50 alerts/week (too loose) or 0 (too tight)   |

**Monthly Tasks:**

| Monthly Task                 | What to Check                                      | Red Flag Threshold                          |
| ---------------------------- | -------------------------------------------------- | ------------------------------------------- |
| Duplicate rate audit         | Run full duplicate detection report                | Rate exceeding 5% (was &lt;5% post-cleanup)    |
| Source analysis              | Which entry points are creating the most duplicates | Any single source accounting for >50% of new dupes |
| Import review                | Review any extended data imports for duplicate creation | Import created >100 duplicates              |

**Quarterly Tasks:**

| Quarterly Task                | What to Review                                    | Action if Off-Track                          |
| ----------------------------- | ------------------------------------------------- | -------------------------------------------- |
| Matching rule effectiveness   | False positive/negative rates from scan results   | Adjust thresholds, add secondary criteria    |
| Tool configuration audit      | Verify settings haven't drifted                   | Reconfigure to approved spec                 |
| Integration impact assessment | Check if new integrations are creating duplicates | Add prevention rules for new integration     |

**After First Business Cycle (30 days post-cleanup):**

- Run comprehensive duplicate detection report
- Compare current rate to post-cleanup baseline
- Verify prevention rules are catching new duplicates before they're created
- Check that recurring scans are running on schedule

**Refinement Triggers (when to re-engage):**

| Trigger                       | Threshold                                    | Response                                                     |
| ----------------------------- | -------------------------------------------- | ------------------------------------------------------------ |
| Duplicate rate rising         | Exceeds 5% for 2+ consecutive monthly audits | Re-engage SME to investigate sources and tighten rules       |
| New integration added         | Any new data source feeding into CRM         | Scope prevention rules for new integration (mini-project)    |
| Major data import planned     | >5,000 records                               | Run dedup on import file BEFORE loading into CRM             |
| Platform migration            | Moving CRM platforms                         | Full dedup project needed post-migration                     |

**Every 6-12 Months:**

- Full re-audit of duplicate rates across all objects
- Review and update matching criteria based on new data patterns
- Assess if current tool still meets needs or if upgrade is warranted
- Re-run extended deduplication if rate has crept above 5%

---

### 4b. Internal Handoff (SME --> Architect)

> **Purpose:** Transfer context so Architect can manage ongoing relationship.

**What the Architect needs to know:**

- What was built: Deduplication rules, tool configuration, prevention setup
- Customer context: Key stakeholders, CRM platform, integration landscape, data volume
- Common issues: False positive alerts on free email domains, import-related duplicates
- When to escalate back to SME: Matching rule changes, integration changes, re-audit needed
- **Maintenance schedule** (if Dedicated engagement — Architect monitors scan results)

**Escalation guidelines:**

| Issue Type                                          | Who Handles            | Example                                         |
| --------------------------------------------------- | ---------------------- | ------------------------------------------------ |
| Scan result review, alert threshold tuning          | Architect              | "Monthly scan found 15 dupes — merge them"      |
| Matching rule changes, new integration prevention   | SME                    | "We added a new form — need prevention rules"   |
| Re-audit, extended dedup re-run                         | SME                    | "Duplicate rate is back above 10%"               |

**For Dedicated engagements:** Architect also receives the maintenance schedule (4a) and becomes responsible for monitoring recurring scans and flagging drift.

---

### 4c. External Handoff (LeanScale --> Customer)

> **Purpose:** Formal project completion with customer.

**Final project meeting (45 min):**

- Review deduplication results: records before, records after, merge ratio per object
- Walk through Data Governance SOP (matching rules, scan schedule, escalation path)
- Demonstrate tool admin: how to run ad-hoc scans, adjust thresholds
- Walk through recurring scan schedule and notification setup
- Confirm no outstanding issues
- Answer final questions
- Make it explicit: "Project complete. Here's your governance playbook."
- **For Single Project engagements:** Walk customer through maintenance schedule in detail. Record for reference.

**Documentation package:**

- Data Governance SOP (matching rules, master record hierarchy, prevention rules, scan schedule)
- Deduplication Results Report (before/after metrics per object)
- Training recordings (end-user + technical admin)
- Quick-Reference Card (data entry standards)
- FAQ document
- Tool admin credentials and configuration documentation
- Maintenance Schedule
- Support contact info

**For Single Project engagements:** The customer owns recurring scans and data quality from this point. The governance SOP is their playbook.

**Output:** Customer owns the clean database and the governance process. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved (audit report, matching criteria, execution log, governance SOP)
- [ ] Handoff documentation complete
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized

#### Internal Debrief (Optional but Recommended)

- What went well? (e.g., "Test batch caught the free email domain issue before full run")
- What would we do differently? (e.g., "Should have paused Salesforce-HubSpot sync earlier")
- Any learnings to feed back into SOPs? (e.g., "Add integration constraint check to pre-kickoff checklist")

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                                  |
| ----------------------------- | ------------------------------------- |
| **Single Project**            | Upsell --> Downsell --> Retry          |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In (90 day) |

**Single Project Path:**

```
1. Upsell: Managed Services (retainer -- we monitor scans, handle imports, maintain quality)
   | if no
2. Downsell: CRM Deduplication Ongoing Tool project (set up long-term tooling)
   or: Data Enrichment project (now that data is clean, enrich it)
   | if yes
3. Retry retainer at end of next project cycle
```

**Script:**

> "Now that your CRM is clean, there are two ways we can keep it that way. Option 1: We manage ongoing data quality for you — monitoring scans, handling imports, tuning rules as your data evolves. Option 2: If there's a specific next project, like enriching your now-clean data or setting up your ongoing dedup tooling, we can scope that. Which sounds more relevant?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On [date ~90 days out], we'll review your duplicate rates and see if the rules need any adjustment based on real-world data patterns."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                                     |
| ------------------- | ---------------------------------------------------------------- |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks                 |
| 2. Review metrics   | Pull latest scan results: current duplicate rate, trend over time |
| 3. Decide ownership | Can Architect handle this check-in, or need SME?                        |
| 4. Prep materials   | If SME needed, brief them. If Architect, prep talking points.           |

**At the refinement check-in:**

- Review duplicate rate trend (should be stable under 5%)
- Identify any new duplicate sources (new integrations, new forms, large imports)
- If minor: Architect tunes alert thresholds
- If major: Scope re-audit or matching rule update (restart relevant phases)

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- Duplicate Audit Report (baseline rates per object, pattern analysis, source ranking)
- Matching Criteria Document (primary/secondary rules, fuzzy thresholds, approved by stakeholders)
- Master Record Selection Hierarchy (which record wins, edge case handling)

**Technical Deliverables:**

- Deduplication tool configured and operational
- Prevention rules active (duplicate alerts, validation rules, company name standardization)
- Recurring automated scans scheduled and running
- Deduplication Results Report (records before/after per object, merge ratio, exceptions log)

**Documentation Package:**

- Data Governance SOP
- Training recordings (end-user + technical admin)
- Quick-Reference Card (data entry standards)
- FAQ document
- Definition Alignment Document (final version)
- Maintenance Schedule

---

## Appendix

### What This Document Is

This is the implementation playbook for CRM Deduplication — the step-by-step execution guide an Architect follows to deliver the project from first contact to project close. It is the third file in a 3-file playbook structure:

| File                  | Purpose                                                                  | Audience                 |
| --------------------- | ------------------------------------------------------------------------ | ------------------------ |
| `advisory`       | What the project IS — positioning, outcomes, approaches                 | Architect + Sales (scoping)     |
| `methodology`    | HOW we think about the problem — frameworks, concepts, best practices   | Architect (depth understanding) |
| `implementation` | WHAT to DO — step-by-step execution with checklists | Architect (daily execution)    |

### What Each Phase Produces

| Phase                    | Output                                                                 | Gate Criteria                                                                  |
| ------------------------ | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **Phase 1: Strategy**    | Approved matching criteria + master record hierarchy + tool decision   | RevOps lead and CRM admin have signed off on all rules                         |
| **Phase 2: Engineering** | Clean CRM + prevention rules active + recurring scans running          | Duplicate rate &lt;5%, data integrity verified, customer approved                 |
| **Phase 3: Enablement**  | Trained team with documentation                                        | All training delivered, team can handle scans and alerts independently         |
| **Phase 4: Handoff**     | Independent customer + archived project                                | Governance SOP delivered, maintenance schedule active, project closed          |

### How to Adapt Per Project Type

CRM Deduplication is a **technical-heavy** project:

| Project Profile         | Strategy Weight | Engineering Weight | Enablement Weight | Notes                           |
| ----------------------- | --------------- | ------------------ | ----------------- | ------------------------------- |
| **CRM Deduplication**   | 20-30%          | 50-60%             | 10-20%            | Heavy on engineering, light enablement |

**Adaptation rules for this project type:**

- Phase 1 can compress to 2 meetings if client already knows their matching rules and has tool budget approved
- Phase 2 is the heaviest — don't rush batch execution. Process slowly and verify.
- Phase 3 can be a single combined training session if the team is small
- Phase 4 always applies — governance SOP is critical for preventing re-creation

### Key Industry Context

CRM databases accumulate duplicates at a significant rate. Research indicates that B2B contact data decays at approximately 70% per year [1], meaning even clean databases quickly accumulate stale and duplicated records. Organizations without active data quality programs commonly see duplication rates between 10-30% [2]. Sales departments lose an estimated 550 hours annually per representative due to inaccurate CRM information, including time spent navigating duplicate records and resolving ownership conflicts [3]. The financial impact is substantial — poor data quality costs U.S. businesses an estimated $3.1 trillion annually [4]. At the individual company level, the cost to identify, review, and properly merge a single duplicate record averages $96, making a 10% duplicate rate in a 50,000-record database a $480,000 problem [5].

The good news: organizations implementing structured deduplication approaches with advanced matching algorithms reduce duplicates by 30-40% within the first few months [6], and 22% of organizations have already achieved the 1% duplicate rate benchmark through sustained effort [6].

---

## References

[1] [Landbase - Duplicate Record Rate Statistics](https://www.landbase.com/blog/duplicate-record-rate-statistics) - B2B data decay rate of 70% annually

[2] [Experian Data Quality Research](https://www.edq.com/resources/data-quality-infographic/) - 94% of organizations suspect inaccurate customer data; 10-30% duplication rates common

[3] [Landbase - Duplicate Record Rate Statistics](https://www.landbase.com/blog/duplicate-record-rate-statistics) - Sales departments lose 550 hours annually due to inaccurate CRM data

[4] [IBM / HBR - The Business Costs of Bad Data](https://hbr.org/2016/09/bad-data-costs-the-u-s-3-trillion-per-year) - $3.1 trillion annual cost of poor data quality in the U.S.

[5] [Databar - Duplicate Record Management in CRM](https://databar.ai/blog/article/duplicate-record-management-in-crm-the-hidden-revenue-killer-and-how-to-fix-thousands-fast) - $96 average cost per duplicate record

[6] [Landbase - Duplicate Record Rate Statistics](https://www.landbase.com/blog/duplicate-record-rate-statistics) - 30-40% duplicate reduction with advanced algorithms; 1% benchmark achievable

[7] [Landbase - Duplicate Record Rate Statistics](https://www.landbase.com/blog/duplicate-record-rate-statistics) - 92% of duplicates created during initial data entry
