# Fed/PubSec CRM Partitioning — Implementation

## Project One-Pager

> Quick reference for architects. One per project type. Fill this out FIRST — it serves as the project's identity card.

### Fed/PubSec CRM Partitioning One-Pager

#### Project Type

- Category: Technical
- Primary Deliverable: Fully partitioned CRM environment with Fed/PubSec data isolated from commercial data via RBAC, sharing rules, record types, and audit trails — compliant with ITAR, FedRAMP, DFARS, or CMMC as applicable.

##### Phase Relevance

| Phase          | Applies? |
| -------------- | -------- |
| 1. Strategy    | Yes      |
| 2. Engineering | Yes      |
| 3. Enablement  | Yes      |
| 4. Handoff     | Yes      |

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │    Heavy     │     │    Heavy     │     │     Med      │     │     Med      │
  │ 1a→1b→1c→1d │     │ 2a→2b→2c→2d │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   Compliance map       CRM config +         Admin + user         Audit schedule +
   + architecture       RBAC + migration     compliance trng      troubleshooting
```

**This project's flow:**
- Full 4-phase. Heavy strategy (compliance requirements drive every decision), heavy engineering (CRM configuration, RBAC, sharing rules, data migration), medium enablement (admin training + compliance-aware user training), medium handoff (compliance audit cadence critical).
- No phases are skipped. Phase 1 and Phase 2 carry the most weight. Strategy takes longer when multiple compliance frameworks overlap (ITAR + DFARS + CMMC).

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Watch intro video explaining what CRM partitioning means and why it matters for compliance
- [ ] Complete intake form: list all compliance frameworks that apply (ITAR, FedRAMP, DFARS, CMMC, EAR), identify Fed/PubSec sales leadership, and confirm number of CRM users by segment
- [ ] Provide list of all current CRM users with their roles, profiles, and intended segment (Fed/PubSec vs Commercial)
- [ ] Provide account classification criteria or list: which accounts are Fed/PubSec vs Commercial
- [ ] Get internal alignment on which compliance frameworks apply — legal/compliance must confirm

##### Track B: Architect Prep
- [ ] Pull CRM user list, current profiles, permission sets, and sharing model via admin export
- [ ] Document current OWD settings and role hierarchy structure
- [ ] Audit active integrations (marketing automation, BI, APIs, enrichment tools)
- [ ] Draft v0 data classification matrix based on intake form and CRM data
- [ ] Identify which objects contain potentially sensitive Fed/PubSec data

#### Refinement Loop (1b --> 1c --> 1d)

| Meeting              | Sub-Phase | Focus                                                     | Stakeholder                                  | Output                                   |
| -------------------- | --------- | --------------------------------------------------------- | -------------------------------------------- | ---------------------------------------- |
| Kickoff              | 1b        | Present v0 compliance map + architecture assessment        | VP Sales Ops, Fed/PubSec Lead, Legal         | Info for v1 partitioning strategy        |
| Compliance Deep Dive | 1c        | Validate compliance frameworks, data sensitivity levels    | Legal/Compliance, Fed/PubSec Sales Director  | Validated data classification matrix     |
| Architecture Review  | 1c        | Review partitioning approach, integration impact           | RevOps, IT/CRM Admin                         | Approved architecture + approach         |
| Sign-Off             | 1d        | Final alignment on partitioning strategy + scope           | All stakeholders                              | Signed-off strategic package             |

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held
- [ ] 1c. Refinement loop complete (compliance map + architecture approved)
- [ ] 1d. Strategic sign-off obtained

##### Phase 2: Engineering
- [ ] 2a. Tech spec created (profiles, permission sets, sharing rules, record types, data tagging)
- [ ] 2b. Engineering handoff meeting held
- [ ] 2c. Build complete (RBAC, sharing rules, record types, data migration, integration updates)
- [ ] 2d. QA/Test + customer sign-off (access testing matrix + data leakage audit)

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped (admin runbook, user quick reference cards)
- [ ] 3b. Training sessions delivered (admin training + segment-specific user training)
- [ ] 3c. Hypercare period complete (2 weeks post go-live)
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff (SME --> Architect) complete
- [ ] 4c. External handoff (LeanScale --> Customer) complete
- [ ] 4d. Project closed and archived

#### Document Types

##### Working Documents (iterate together)

| Document                       | Purpose                                    | When Complete                              |
| ------------------------------ | ------------------------------------------ | ------------------------------------------ |
| Compliance Requirements Map    | Document applicable frameworks + rules     | All frameworks identified + validated       |
| Data Classification Matrix     | Map objects/fields to sensitivity levels    | All CRM objects classified                 |
| Current State Access Audit     | Capture existing RBAC + sharing model      | All users, roles, and sharing rules mapped |
| Architecture Decision Record   | Evaluate partitioning approaches           | Approach selected + approved               |
| Data Tagging Ruleset           | Define classification triggers + automation | Rules documented + edge cases addressed    |

##### Deliverables (polished outputs)

| Deliverable                           | Created From                          | Customer Uses For                          |
| ------------------------------------- | ------------------------------------- | ------------------------------------------ |
| Partitioning Architecture Document    | Architecture Decision Record          | Internal compliance documentation           |
| Access Testing Matrix (completed)     | QA testing results                    | Compliance audit evidence                   |
| Security Audit Report                 | Data leakage audit results            | Regulatory compliance proof                 |
| Admin Runbook                         | Training materials + config docs      | Ongoing maintenance                         |

#### Enablement Details

##### Training Types

| Type       | Audience                                   | Focus                                                       | Duration |
| ---------- | ------------------------------------------ | ----------------------------------------------------------- | -------- |
| Admin      | CRM Admin, RevOps                          | Maintaining partitioning: adding users, changing segments, handling edge cases | 90 min   |
| Fed/PubSec | Fed/PubSec sales team                      | Why partitioning exists, data handling rules, creating records in correct segment | 45 min   |
| Commercial | Commercial sales team                      | What changed, what they can/cannot access, account handoff process | 30 min   |
| Leadership | VP Sales Ops, Fed/PubSec Director, Legal   | Executive dashboards, aggregate reporting, compliance posture | 30 min   |

##### Hypercare
- Applies: Yes
- Duration: 2 weeks post go-live
- Office Hours: Yes — daily 15-min slot during first week, then twice per week in week 2

##### Training Assets to Create
- [ ] Video walkthrough: Partitioning architecture walkthrough (for admin reference)
- [ ] Doc: Admin runbook (add/remove users, change segment, handle edge cases)
- [ ] Doc: User quick reference card (Fed/PubSec team)
- [ ] Doc: User quick reference card (Commercial team)
- [ ] Doc: Account handoff process between segments
- [ ] Doc: FAQ — common questions about data visibility and access

#### Handoff & Retention

##### Internal Handoff (SME --> Architect)
- Key context for Architect: Which compliance frameworks apply, what partitioning approach was used (single org RBAC vs separate instance), key stakeholders in Fed/PubSec and compliance
- Escalation trigger: Any changes to sharing rules, new compliance requirements, role hierarchy modifications, or integration changes that touch partitioned data

##### External Handoff (LeanScale --> Customer)
- Final meeting agenda: Review architecture, walk through admin runbook, demonstrate compliance audit process, confirm maintenance schedule, answer final questions
- Documentation package: Architecture document, admin runbook, training recordings, access testing matrix, security audit report, FAQ document, maintenance schedule

##### Maintenance Schedule
- Monthly: Access control spot checks, new user provisioning audit, classification rule review
- Quarterly: Full compliance audit, integration access review, sharing rule validation

#### Definition Alignment Terms

| Term                          | Typical Definition                                                                                              |
| ----------------------------- | --------------------------------------------------------------------------------------------------------------- |
| Fed/PubSec                    | Federal government agencies, state/local government entities, and organizations primarily contracting with them |
| Commercial                    | All non-government accounts and related records                                                                 |
| Partitioning                  | Logical or physical separation of data within the CRM to restrict cross-segment visibility                      |
| RBAC (Role-Based Access Control) | Security model where access permissions are tied to user roles rather than individual users                   |
| OWD (Organization-Wide Defaults) | Salesforce setting that defines the baseline level of record access for all users                              |
| CUI (Controlled Unclassified Information) | Government information that requires safeguarding per federal policy but is not classified                |
| ITAR                          | International Traffic in Arms Regulations — controls export of defense-related articles and services           |
| FedRAMP                       | Federal Risk and Authorization Management Program — security standards for cloud services used by government   |
| DFARS                         | Defense Federal Acquisition Regulation Supplement — cybersecurity requirements for DoD contractors              |
| CMMC                          | Cybersecurity Maturity Model Certification — DoD framework for assessing contractor cybersecurity practices     |
| Data Leakage                  | Unauthorized exposure of partitioned data to users outside the intended segment                                 |
| Business Segment Field        | Custom CRM field (picklist) that tags each record as Fed/PubSec or Commercial                                  |

#### Common Gotchas

- Implicit sharing creates access loopholes: child records inherit parent sharing --> Test all parent-child relationships; configure OWD at each object level; use sharing rule filters that account for object relationships
- Integration users bypass partitioning: API users often have elevated permissions --> Create dedicated integration users per segment with scoped permissions; audit all active integrations before go-live
- Report exports expose restricted data: users can export data visible in reports --> Restrict export permissions in Fed/PubSec profiles; configure report folder security and dashboard running user controls
- Edge case accounts fall through classification: companies with both government and commercial contracts --> Establish clear classification rules and escalation process; consider account splitting for hybrid customers; document decisions for audit trail
- Global search exposes partitioned records: search indexes may surface Fed/PubSec records to commercial users --> Test search functionality as each user type; configure search scope settings
- Marketing automation syncs break partitioning: MAP may sync all contacts without respecting segments --> Update MAP sync filters to respect Business Segment field; create segment-specific contact lists

#### Methodology Options

| Option                      | When to Use                                                  | Complexity |
| --------------------------- | ------------------------------------------------------------ | ---------- |
| Single Org + RBAC           | No ITAR data; standard compliance needs; cost-sensitive       | Medium     |
| Single Org + Business Units | Moderate compliance; need some physical separation within org | High       |
| Separate CRM Instance       | ITAR-controlled data; strict GovCloud requirements; zero-risk tolerance | Very High  |

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on the partitioning approach, compliance requirements, and data classification.
>
> **Output:** Compliance Requirements Map + Data Classification Matrix + Architecture Decision Record (signed off by stakeholders).

### 1a. Pre-Kickoff

> Two parallel tracks run after the AE closes and before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                                | Purpose                                                | Format             |
| ----------------------------------- | ------------------------------------------------------ | ------------------ |
| Intro video                         | Explain CRM partitioning, why compliance requires it    | Video walkthrough (5-10 min) |
| Definition Alignment Document       | Get sign-off on terms: Fed/PubSec, CUI, RBAC, etc.     | Google Doc         |
| Pre-filled intake form              | Confirm compliance frameworks, user counts, account list | Google Form or Doc |
| CRM user export request             | Full list of users with roles/profiles                  | CSV export         |

**Completion tracking:** RevOps or sales ops lead follows up. Do not cancel kickoff if incomplete, but the compliance framework confirmation from legal is the one hard prerequisite — push hard on this.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                     | Output                                    |
| ---- | ---------------------------------------------------------- | ----------------------------------------- |
| 1    | Pull CRM user list with roles, profiles, permission sets    | User access inventory                     |
| 2    | Document current OWD settings and sharing rules             | Current state sharing model               |
| 3    | Audit active integrations (MAP, BI, APIs)                   | Integration inventory                     |
| 4    | Draft v0 data classification matrix from intake data        | Data classification matrix v0             |
| 5    | Draft v0 compliance requirements map                        | Compliance requirements map v0            |
| 6    | Prepare kickoff presentation with architecture options      | Kickoff deck with 3 approach options      |

**Critical:** Mark everything as ASSUMED. The kickoff call validates. Compliance frameworks especially — never assume ITAR applies without legal confirmation.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building anything. This is especially critical for compliance-driven projects where misalignment on definitions can lead to regulatory violations.

| Term                  | Our Definition                                                                    | Internally Approved? |
| --------------------- | --------------------------------------------------------------------------------- | -------------------- |
| Fed/PubSec            | Federal, state, and local government entities + primary government contractors     | [ ] Yes / [ ] No     |
| Commercial            | All non-government accounts and contacts                                          | [ ] Yes / [ ] No     |
| CUI                   | Controlled Unclassified Information per NIST SP 800-171                            | [ ] Yes / [ ] No     |
| Partitioning Boundary | What data is isolated: Accounts, Contacts, Opportunities, Activities, Cases       | [ ] Yes / [ ] No     |
| Cross-Segment Access  | Whether any users need visibility into both segments (e.g., executive reporting)   | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your legal/compliance team and sales leadership. Check "Yes" when approved. We cannot proceed with architecture decisions until all terms are aligned — misalignment here creates compliance risk downstream.

---

### 1b. Kickoff Call

> **Purpose:** Present v0 compliance map and data classification matrix. Validate compliance frameworks and identify partitioning approach.

#### Agenda (60-90 min)

| Time  | Topic                           | What Happens                                              |
| ----- | ------------------------------- | --------------------------------------------------------- |
| 0-15  | Walk through v0 compliance map  | "Here's what we found from your intake"                   |
| 15-30 | Validate compliance frameworks  | ITAR, FedRAMP, DFARS, CMMC — which actually apply?        |
| 30-45 | Review data classification v0   | Which objects/fields contain sensitive Fed/PubSec data?   |
| 45-55 | Architecture options overview   | Present 3 approaches: single org RBAC, business units, separate instance |
| 55-65 | Definition alignment            | Review Definition Alignment Doc                           |
| 65-75 | Identify gaps and next steps    | What data is missing, schedule compliance deep dive       |

#### What We Bring

- v0 compliance requirements map (built from intake + research)
- v0 data classification matrix
- Architecture options comparison (3 approaches with pros/cons)
- Questions list: which compliance frameworks apply, who are the data stewards, are there cross-segment needs
- Definition Alignment Document (pre-filled with our recommendations)

#### What We Leave With

- Confirmed list of applicable compliance frameworks
- Corrections on data classification matrix
- Initial preference on partitioning approach
- Compliance deep dive meeting scheduled with legal/compliance
- Clear homework: customer confirms account classification list

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Iterate on compliance requirements, data classification, and architecture decisions until all stakeholders approve.

#### The Pattern

```
Kickoff Call (present v0, validate compliance frameworks)
    |
Architect updates compliance map + classification matrix --> v1
    |
Meeting 2: Compliance Deep Dive (validate with legal) --> v2
    |
Meeting 3: Architecture Review (approve approach with RevOps/IT) --> v3
    |
Final Review --> Sign-off
```

#### Meeting Schedule

| Meeting Type            | Focus                                              | Stakeholder                               |
| ----------------------- | -------------------------------------------------- | ----------------------------------------- |
| Compliance Deep Dive    | Data sensitivity levels, regulatory requirements    | Legal/Compliance, Fed/PubSec Director     |
| Architecture Review     | Partitioning approach, integration impact           | RevOps, CRM Admin, IT                     |
| Data Validation         | Account classification list, user role mapping      | Sales Ops, Fed/PubSec Sales Lead          |
| Final Review            | Full walkthrough of partitioning strategy           | All stakeholders                           |

#### Typical Timeline

| Milestone                     | Timing                                                |
| ----------------------------- | ----------------------------------------------------- |
| Pre-kickoff prep              | 2-3 days                                              |
| Kickoff call                  | Day 1 of engagement                                   |
| Compliance deep dive          | Days 3-5 (must have legal available)                  |
| Architecture review           | Days 5-8                                              |
| Data validation               | Days 8-10                                             |
| Final review + sign-off       | Days 10-14 (when all inputs confirmed)                |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything before proceeding to engineering.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by legal/compliance AND sales leadership
- [ ] Compliance frameworks confirmed (ITAR/FedRAMP/DFARS/CMMC — which apply)
- [ ] Data classification matrix finalized and approved
- [ ] Partitioning approach selected and approved (single org RBAC, business units, or separate instance)
- [ ] Account classification list provided (Fed/PubSec vs Commercial)
- [ ] User role mapping complete (who gets what access)
- [ ] Integration impact assessment reviewed
- [ ] No blockers for engineering

#### Decision Point

- **Proceed to Engineering** --> Standard path. Architecture approved, begin building RBAC + sharing rules.
- **Pause for external compliance review** --> If ITAR applies and GovCloud assessment is needed, may require external legal or compliance audit before building.

---

## Phase 2: Engineering

> **Goal:** Build and test the partitioned CRM environment based on approved strategy.
>
> **Output:** Fully configured CRM with RBAC, sharing rules, record types, data migration complete, integrations updated, reports built — tested and customer-approved.

This project is engineering-heavy. CRM configuration touches profiles, permission sets, role hierarchy, OWD settings, sharing rules, record types, custom fields, validation rules, page layouts, data migration, integration filters, and report/dashboard security. Expect 60-70% of project effort here.

### Sub-Phases

```
2a Tech Spec --> 2b Engineering Handoff --> 2c Build --> 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate the approved partitioning strategy into technical CRM specifications.

**Input:** Signed-off strategic package (compliance map, data classification matrix, architecture decision, account classification list, user role mapping)

**Output:** Draft tech spec containing:

- Profile configuration specs: Fed/PubSec profiles cloned from existing sales profiles with field-level security adjustments
- Permission set definitions: Fed/PubSec data access permission sets with object and field permissions
- Role hierarchy design: Fed/PubSec branch separated from Commercial branch
- OWD settings: Private for Accounts, Contacts, Opportunities (per object)
- Sharing rule definitions: criteria-based rules for Fed/PubSec and Commercial segments
- Record type specifications: Fed/PubSec record types for Account, Contact, Opportunity, Lead
- Custom field specs: Business Segment picklist field, validation rules
- Page layout assignments: segment-appropriate fields per profile
- Data migration plan: existing record classification + update sequence
- Integration update specs: per-integration filter and permission changes
- Report/dashboard specs: segment-specific + executive roll-up views

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs with CRM admin/engineer before building.

**Who attends:** Architect + CRM Admin/Engineer

**Agenda (45-60 min):**

| Time  | Topic                           | What Happens                                                  |
| ----- | ------------------------------- | ------------------------------------------------------------- |
| 0-15  | Walk through strategy context   | Architect explains compliance requirements + partitioning approach    |
| 15-30 | Review tech spec                | Profile configs, sharing rules, role hierarchy, record types  |
| 30-45 | Integration impact review       | Which integrations need updates, what filters to apply        |
| 45-60 | Data migration planning         | Sequence, rollback plan, validation checkpoints               |

**What Architect brings:**
- Strategic package (compliance map, data classification, architecture decision)
- Draft tech spec (from 2a)
- Questions: edge case account handling, integration user permissions, report folder structure

**What engineer leaves with:**
- Approved tech spec
- Build sequence: (1) Profiles/permissions --> (2) Role hierarchy --> (3) OWD + sharing rules --> (4) Record types + fields --> (5) Data migration --> (6) Integration updates --> (7) Reports/dashboards
- Known risks: implicit sharing, integration user bypass, search scope

---

### 2c. Build (Configure)

> **Purpose:** Build the partitioned CRM environment per approved tech spec.

**Input:** Approved tech spec from 2b

**Build sequence and components:**

**Step 1: Configure Profiles, Permission Sets, and Role Hierarchy**
- [ ] Create Fed/PubSec-specific profiles cloned from existing sales profiles
- [ ] Build permission sets for Fed/PubSec data access (object + field level)
- [ ] Configure role hierarchy: separate Fed/PubSec branch from Commercial branch
- [ ] Set profile-level field security to restrict sensitive fields from Commercial users
- [ ] Assign users to appropriate profiles and permission sets

**Step 2: Implement OWD and Sharing Rules**
- [ ] Set OWD to Private for Accounts, Contacts, Opportunities (if not already)
- [ ] Create criteria-based sharing rules: Fed/PubSec users --> Fed/PubSec records
- [ ] Create criteria-based sharing rules: Commercial users --> Commercial records
- [ ] Configure sharing rules for related objects (Activities, Cases, custom objects)
- [ ] Test implicit sharing (child records) for unintended access

**Step 3: Build Record Types and Data Segmentation**
- [ ] Create Fed/PubSec record types for Account, Contact, Opportunity, Lead
- [ ] Create custom "Business Segment" picklist field (Fed/PubSec, Commercial)
- [ ] Build validation rules to enforce record type / segment alignment
- [ ] Configure page layouts with segment-appropriate fields
- [ ] Set default record type assignments by profile

**Step 4: Migrate and Tag Existing Data**
- [ ] Export existing accounts and classify as Fed/PubSec or Commercial using approved criteria
- [ ] Update Account records with Business Segment field values (batch update)
- [ ] Cascade segmentation to child records (Contacts, Opportunities, Cases)
- [ ] Run data validation: confirm zero untagged records
- [ ] Document records requiring manual review for ambiguous classification

**Step 5: Update Integrations**
- [ ] Audit all active integrations (MAP, enrichment tools, BI, APIs)
- [ ] Update API user permissions to respect partitioning (dedicated integration users per segment)
- [ ] Configure MAP to segment Fed/PubSec contacts (separate lists/segments)
- [ ] Update data sync filters to prevent cross-segment data flow
- [ ] Test each integration for data leakage

**Step 6: Build Segment-Specific Reports and Dashboards**
- [ ] Build Fed/PubSec pipeline and activity reports
- [ ] Build Commercial pipeline and activity reports
- [ ] Create executive dashboard with aggregate metrics (no record-level detail exposure)
- [ ] Configure report folder security to restrict access appropriately
- [ ] Set dashboard running user to appropriate segment-scoped user

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify the partitioned system works and get customer approval.

**Two types of testing:**

| Type                    | Who        | Purpose                                                        |
| ----------------------- | ---------- | -------------------------------------------------------------- |
| Access Testing          | Our team   | Verify each role can only see appropriate data                 |
| Data Leakage Audit      | Our team   | Verify no leakage paths exist (API, search, reports, implicit) |
| Reporting Validation    | Our team   | Verify reports respect partitioning and show accurate data     |
| Customer Testing        | Customer   | Verify the system works for their real-world scenarios         |

**Access testing matrix:**

- [ ] Log in as Fed/PubSec rep: confirm only Fed/PubSec records visible
- [ ] Log in as Commercial rep: confirm only Commercial records visible
- [ ] Log in as Fed/PubSec manager: confirm Fed/PubSec team + record visibility
- [ ] Log in as Commercial manager: confirm Commercial team + record visibility
- [ ] Log in as executive: confirm aggregate dashboard access without record detail leakage
- [ ] Test search: confirm Fed/PubSec records do not appear for Commercial users
- [ ] Test list views: confirm proper filtering by segment
- [ ] Test report access: confirm report folders respect segment boundaries

**Data leakage audit:**

- [ ] Attempt API access to Fed/PubSec data as Commercial integration user
- [ ] Test report exports: confirm partitioning holds in exported data
- [ ] Verify implicit sharing does not create unintended access (child records)
- [ ] Check global search respects partitioning for all user types
- [ ] Review audit trail for any unauthorized access during testing

**Reporting validation:**

- [ ] Compare Fed/PubSec dashboard totals to direct database queries
- [ ] Verify executive roll-up aggregates correctly without exposing detail
- [ ] Test dashboard running user settings for proper data scoping
- [ ] Confirm historical data appears correctly after migration

**Engineering sign-off checkpoint:**

- [ ] All access tests pass (zero failures in testing matrix)
- [ ] Data leakage audit clean (zero critical findings)
- [ ] Reports and dashboards validated
- [ ] Customer has tested real scenarios and approved
- [ ] Ready for enablement

ITAR compliance violations carry civil penalties exceeding $1 million per violation and criminal penalties of up to $1 million and 20 years imprisonment [1]. In 2024, Raytheon paid over $950 million to resolve ITAR-related investigations [2]. A partitioning failure that exposes controlled data to unauthorized users is not a minor bug — it is a regulatory event. QA must be exhaustive.

**Decision point:**

- **Proceed to Enablement** --> All tests pass, system is partitioned correctly
- **Loop back to Build** --> Access failures or leakage found, remediate and re-test

---

## Phase 3: Enablement

> **Goal:** Customer teams understand the partitioned system, compliance requirements, and how to operate within boundaries.
>
> **Output:** Trained admins and users, documented procedures, stabilized system through hypercare.

### Sub-Phases

```
3a Training Prep --> 3b Training Sessions --> 3c Hypercare --> 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials tailored to each audience (admin, Fed/PubSec users, Commercial users, leadership).

**Input:** Strategic package + tech specs + built system + compliance requirements

**Output:** Training package containing:

- Admin runbook: step-by-step for adding users, changing segments, handling edge cases, running compliance checks
- Fed/PubSec user guide: why partitioning exists, data handling rules, creating records correctly, requesting access
- Commercial user guide: what changed, what is restricted, account handoff process
- Leadership briefing: executive dashboard walkthrough, compliance posture overview
- FAQ document: common questions about visibility, access, and data handling
- Quick reference cards: one-page cards for Fed/PubSec and Commercial users

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to customer team, with special attention to compliance awareness.

**Training delivery:**

| Session                 | Audience                                 | Focus                                                                     | Duration |
| ----------------------- | ---------------------------------------- | ------------------------------------------------------------------------- | -------- |
| Admin Training          | CRM Admin, RevOps Manager                | Maintaining partitioning: user provisioning, segment changes, compliance checks, edge case handling, escalation procedures | 90 min   |
| Fed/PubSec Team         | Fed/PubSec sales reps and managers       | Why partitioning exists, what data is restricted, how to create records in correct segment, account handoff process | 45 min   |
| Commercial Team         | Commercial sales reps and managers       | What changed in the system, data visibility boundaries, how to request access or handoffs | 30 min   |
| Leadership Briefing     | VP Sales Ops, Directors, Legal           | Executive dashboard walkthrough, compliance posture, audit schedule | 30 min   |

**Training delivery process:**

1. Schedule sessions by audience (separate sessions for Fed/PubSec and Commercial)
2. Deliver training live with screen share of actual CRM
3. Record sessions for future reference
4. Answer questions, note gaps for FAQ updates
5. Distribute quick reference cards to all users

**Output:**
- Trained stakeholders across all segments
- Session recordings for each training
- Updated FAQ based on questions asked

---

### 3c. Hypercare

> **Purpose:** Intensive post-launch support to catch access issues and user confusion.

**Duration:** 2 weeks

**What happens:**

- **Week 1:** Daily 15-min office hours for immediate issue resolution. Monitor for access issues, misclassified records, user confusion about visibility boundaries.
- **Week 2:** Twice-per-week 15-min office hours. Focus shifts to edge cases and fine-tuning.
- Bug triage and fixes for any partitioning gaps found in production
- Monitor audit trail for unauthorized access attempts
- Rapid response to compliance-related issues (these are escalated immediately, not batched)

**When to extend:** If data leakage issues are found during hypercare, extend until remediated and re-tested. Compliance issues are never deferred.

**Output:** Stabilized partitioned system, no critical issues outstanding, audit trail clean

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm customer can operate the partitioned system independently.

**Validation checkpoint:**

- [ ] All training sessions delivered (admin + both segment teams + leadership)
- [ ] Training recordings and documentation provided
- [ ] Hypercare period complete (2 weeks)
- [ ] No critical issues outstanding (especially no data leakage findings)
- [ ] Admin can demonstrate: adding a new user to correct segment, handling a re-classification request, running an access audit
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** --> System stable, team trained, no compliance issues
- **Extend Hypercare** --> Unresolved access issues or compliance findings require more support

---

## Phase 4: Handoff

> **Goal:** Clean project close with compliance audit schedule established and retention/expansion path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the partitioned system, compliance audit cadence established, project archived.

**Structure:**

```
4a Maintenance Schedule --> 4b Internal Handoff --> 4c External Handoff --> 4d Project Close
                          (SME --> Architect)       (LeanScale --> Customer)   (Archive + Debrief)
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At                                                                     |
| ----------------------------- | -------------------- | --------------------------------------------------------------------------------- |
| **Single Project**            | Customer owns        | 4c (External Handoff) — customer receives maintenance schedule + runs it         |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) — Architect receives maintenance schedule + runs it for customer  |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention to maintain compliance and partitioning integrity.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task                    | What to Check                                            | Red Flag Threshold                                            |
| ------------------------------- | -------------------------------------------------------- | ------------------------------------------------------------- |
| Access Control Spot Check       | Log in as each user type, verify record visibility       | Any user sees records outside their segment                   |
| New User Provisioning Audit     | Verify new users added with correct profile/segment      | Any user without Business Segment assignment                  |
| Classification Rule Review      | Check auto-tagging rules for new accounts               | Any new accounts without segment classification               |
| Audit Trail Review              | Review login and data access logs for anomalies          | Any unauthorized access attempts flagged                      |

**Quarterly Tasks:**

| Quarterly Task                      | What to Review                                          | Action if Off-Track                                     |
| ----------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- |
| Full Compliance Audit               | Run complete access testing matrix, data leakage tests  | Remediate any findings immediately, document in audit   |
| Integration Access Review           | Verify all integration users respect partitioning       | Update API user permissions, re-test                    |
| Sharing Rule Validation             | Confirm no new sharing rules bypass partitioning        | Remove or modify conflicting rules                      |
| Role Hierarchy Review               | Verify hierarchy still enforces segment separation      | Adjust hierarchy if organizational changes occurred     |

**After First Business Cycle (30-90 days post-launch):**

- First formal compliance audit: run the full access testing matrix and data leakage audit as done during QA
- Verify no drift: new users, new integrations, new sharing rules should all respect partitioning
- Key question: Has anyone reported seeing data they should not? If yes, investigate and remediate immediately.

**Refinement Triggers (when to re-engage):**

| Trigger                                    | Threshold                                             | Response                                                |
| ------------------------------------------ | ----------------------------------------------------- | ------------------------------------------------------- |
| Compliance framework change                | New CMMC level, ITAR scope expansion                  | Re-engage SME, scope architecture review                |
| Organizational restructure                 | New sales segments, team realignment                   | Review role hierarchy and sharing rules                 |
| Data leakage incident                      | Any unauthorized access to partitioned data            | Immediate remediation, root cause analysis, audit       |
| CRM platform upgrade                       | Major Salesforce release affecting sharing model       | Pre-upgrade testing of partitioning integrity           |
| New integration added                      | Any system connecting to CRM                           | Verify integration user permissions before activation    |

**Every 6-12 Months:**

- Full architecture review: confirm partitioning approach still meets compliance requirements
- Reassess compliance landscape: new regulations, updated frameworks (e.g., CMMC 2.0 changes)
- Re-validate data classification matrix: new data types, new objects, changed sensitivity levels

---

### 4b. Internal Handoff (SME --> Architect)

> **Purpose:** Transfer context so Architect can manage the ongoing relationship.

**What the Architect needs to know:**

- Which compliance frameworks apply and what they require
- What partitioning approach was implemented (single org RBAC, business units, or separate instance)
- Key stakeholders: who is the compliance contact, who is the Fed/PubSec lead, who is the CRM admin
- Common issues: new user provisioning, account re-classification, edge case accounts
- When to escalate back to SME: any changes to sharing rules, compliance framework updates, data leakage incidents, integration changes

**Escalation guidelines:**

| Issue Type                                   | Who Handles                                  |
| -------------------------------------------- | -------------------------------------------- |
| Add/remove user to correct segment           | Architect (follow runbook)                   |
| Account re-classification request            | Architect (follow documented process)        |
| Sharing rule modification                    | SME                                          |
| New integration touching partitioned data    | SME                                          |
| Compliance framework change or audit finding | SME                                          |
| Data leakage incident                        | SME (urgent escalation)                      |

**For Dedicated engagements:** Architect also receives the maintenance schedule (4a) and becomes responsible for executing monthly/quarterly tasks. SME walks Architect through each task during handoff.

---

### 4c. External Handoff (LeanScale --> Customer)

> **Purpose:** Formal project completion with customer. Transfer compliance ownership.

**Final project meeting:**

- Review what was delivered: partitioning architecture, RBAC configuration, data migration, reports
- Walk through documentation package
- Walk through compliance audit process (how to run access testing matrix)
- Review maintenance schedule in detail: monthly, quarterly, and trigger-based tasks
- Confirm compliance audit cadence (quarterly recommended for Fed/PubSec [3])
- Answer final questions
- Make it explicit: "Project complete. Compliance maintenance is now your responsibility."

**Documentation package:**

- Partitioning Architecture Document
- Admin Runbook (user provisioning, segment changes, edge cases)
- Access Testing Matrix (completed, reusable for future audits)
- Security Audit Report
- Data Classification Matrix (final version)
- Definition Alignment Document (final version)
- Training session recordings (all sessions)
- Quick reference cards (Fed/PubSec + Commercial)
- FAQ document
- Maintenance Schedule
- Support contact info

**Output:** Customer owns the partitioned system. Compliance audit cadence established. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location
- [ ] Handoff documentation complete
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized
- [ ] Access testing matrix results archived (compliance evidence)

#### Internal Debrief (Optional but Recommended)

- What went well?
- What would we do differently? (compliance deep dive timing, stakeholder availability, data migration approach)
- Were there edge cases we should document for future Fed/PubSec projects?

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                                              |
| ----------------------------- | ------------------------------------------------- |
| **Single Project**            | Upsell --> Downsell --> Retry                     |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In (90-day compliance audit) |

**Single Project Path:**

```
1. Upsell: Managed Services (ongoing compliance monitoring + quarterly audits)
   | if no
2. Downsell: Another one-time project (e.g., CRM cleanup, reporting suite, lead lifecycle)
   | if yes
3. Retry retainer at end of next project cycle
```

**Script:**

> "Now that Fed/PubSec CRM Partitioning is complete, there are two ways we can continue working together. Option 1: We set you up on managed services where we handle ongoing compliance monitoring, quarterly access audits, and partitioning maintenance. Given the regulatory requirements, many clients find this reduces their compliance burden. Option 2: If there's another project you need help with — like reporting or lifecycle automation — we can scope that out. Which sounds more interesting?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On [date ~90 days out], we'll run a full compliance audit of the partitioning — the same access testing and data leakage checks we did during QA. We'll review if any adjustments are needed based on org changes, new hires, or updated regulations."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                                  |
| ------------------- | ------------------------------------------------------------- |
| 1. Get pinged       | System reminder: compliance check-in in 2 weeks               |
| 2. Review metrics   | Pull audit trail, check for access anomalies                  |
| 3. Decide ownership | Can Architect run the compliance audit, or does SME need to?  |
| 4. Prep materials   | If SME needed, brief them. If Architect, prep audit checklist. |

**Output:** Project archived. Compliance audit cadence established. Future revenue path set.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**
- Compliance Requirements Map (applicable frameworks + specific requirements)
- Data Classification Matrix (objects, fields, sensitivity levels, compliance frameworks)
- Architecture Decision Record (approach selection with rationale)
- Definition Alignment Document (signed off by all stakeholders)

**Technical Deliverables:**
- Configured CRM: profiles, permission sets, role hierarchy, OWD settings, sharing rules, record types, Business Segment field, validation rules, page layouts
- Migrated data: all existing records classified and tagged
- Updated integrations: API users, MAP segments, BI filters
- Segment-specific reports and dashboards + executive roll-up
- Completed access testing matrix (reusable for future audits)
- Security audit report

**Documentation Package:**
- Admin Runbook
- Training session recordings (4 sessions)
- Quick reference cards (Fed/PubSec + Commercial)
- FAQ document
- Maintenance Schedule (monthly, quarterly, trigger-based)

---

## Appendix

### What This Document Is

This is the end-to-end execution guide for delivering a Fed/PubSec CRM Partitioning engagement. It covers the full 4-phase framework from compliance strategy through engineering build, enablement, and handoff. It is designed to be used as a live project reference — the phase checklists, meeting agendas, and validation checkpoints are built to be followed in sequence.

### What Each Phase Produces

| Phase          | Primary Output                                                                 |
| -------------- | ------------------------------------------------------------------------------ |
| 1. Strategy    | Compliance Requirements Map + Data Classification Matrix + Architecture Decision Record |
| 2. Engineering | Configured CRM (RBAC, sharing rules, record types) + migrated data + tested system |
| 3. Enablement  | Trained admins and users + documentation package + stabilized system            |
| 4. Handoff     | Maintenance schedule + compliance audit cadence + project archive               |

### How to Adapt Per Project Type

| Project Type            | Key Adjustments                                                                 |
| ----------------------- | ------------------------------------------------------------------------------- |
| ITAR-only               | Evaluate separate CRM instance; GovCloud assessment may be required before build |
| FedRAMP/DFARS/CMMC only | Single org RBAC is usually sufficient; confirm with legal                        |
| Multiple frameworks     | Strategy phase takes longer; compliance deep dive requires separate sessions per framework |
| Large user base (&gt;200) | Consider Business Units approach; role hierarchy design is more complex          |
| Hybrid accounts         | Account splitting process required; document classification decisions for audit trail |

---

## References

[1] [ITAR Compliance: Requirements, Violations, Examples and More - PreVeil](https://www.preveil.com/blog/six-things-you-have-to-know-about-itar-compliance/)

[2] [ITAR Violations: Types, Examples &amp; Consequences - Securiti](https://securiti.ai/blog/itar-violations/)

[3] [Navigating ITAR Compliance: What You Need to Know in 2024 - IT Solutions](https://www.itsolutions-inc.com/articles/navigating-itar-compliance-what-you-need-to-know-in-2024/)

[4] [FedRAMP - GSA](https://www.gsa.gov/technology/government-it-initiatives/fedramp)

[5] [Closing the Gaps: DFARS 7012-7021 Updates - BDO](https://www.bdo.com/insights/advisory/closing-the-gaps-dfars-7012-7021-updates-cmmc-integration-and-what-contractors-need-to-know)

[6] [How ITAR Impacts CMMC's FedRAMP Requirements - Keiter Technologies](https://keitertechnologies.com/blog/how-itar-impacts-cmmcs-fedramp-requirements/)

[7] [Salesforce Sharing Rules: A Complete Guide - Salesforce Ben](https://www.salesforceben.com/tips-for-planning-and-creating-salesforce-sharing-rules/)

[8] [The Rising Cost of a Data Breach in 2024 - Jeskell Systems](https://jeskell.com/the-rising-cost-of-data-breaches-in-2024-why-its-time-to-act/)
