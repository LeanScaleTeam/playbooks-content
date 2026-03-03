# Email Operations Subscription and Compliance — Implementation

## Project One-Pager

### Email Operations Subscription and Compliance One-Pager

#### Project Type

- Category: Technical
- Primary Deliverable: Fully configured subscription management framework with preference center, consent tracking fields, GDPR/CCPA compliance mechanisms, and automated opt-in/opt-out workflows in HubSpot or Marketo

##### Phase Relevance

| Phase          | Applies? | Weight | Notes                                                      |
| -------------- | -------- | ------ | ---------------------------------------------------------- |
| 1. Strategy    | Yes      | Light  | 1-2 alignment loops to confirm subscription types and compliance requirements |
| 2. Engineering | Yes      | Heavy  | Core build: subscription types, preference center, consent fields, compliance automations |
| 3. Enablement  | Yes      | Medium | Training on subscription management, compliance SOPs, data subject request handling |
| 4. Handoff     | Yes      | Medium | Internal + External with compliance checklist and maintenance schedule |

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────>│ 2. ENGINEER  │────>│3. ENABLEMENT │────>│  4. HANDOFF  │
  │    Light     │     │    Heavy     │     │   Medium     │     │   Medium     │
  │ 1a->1b->1c->1d │     │ 2a->2b->2c->2d │     │ 3a->3b->3c->3d │     │ 4a->4b->4c->4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   Audit + align        Build subs,          Train team,          Compliance
   subscription types   pref center,         compliance SOPs,     checklist +
   & compliance reqs    consent tracking     DSAR handling        ownership transfer
```

**This project's flow:**
- Full 4-phase. Light strategy (subscription type definitions + compliance requirements scoping), heavy engineering (MAP configuration, preference center, consent fields, automations), medium enablement, medium handoff.
- Strategy can compress to 2-3 meetings if the client has a clear picture of their email programs and compliance requirements.

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Complete email program inventory (all email types currently sent, frequency, audience)
- [ ] Provide list of geographic regions they market to (EU, California, Canada, other)
- [ ] Confirm MAP admin access is ready (HubSpot or Marketo)
- [ ] Gather brand assets for preference center (logo, brand colors, approved copy)
- [ ] Identify legal/compliance stakeholder (if available) for GDPR/CCPA requirements review

##### Track B: Architect Prep
- [ ] Pull current subscription type configuration from HubSpot/Marketo
- [ ] Audit existing opt-in mechanisms (forms, landing pages, import processes)
- [ ] Review current consent tracking (fields, timestamps, source tracking)
- [ ] Identify existing preference center or unsubscribe flow
- [ ] Draft gap analysis: current state vs. GDPR/CCPA/CAN-SPAM requirements

#### Refinement Loop (1b -> 1c -> 1d)

| Meeting      | Sub-Phase | Focus                                                    | Stakeholder                      | Output                              |
| ------------ | --------- | -------------------------------------------------------- | -------------------------------- | ----------------------------------- |
| Kickoff      | 1b        | Present gap analysis, confirm subscription type list     | VP Marketing, MOps Manager       | Validated subscription type list    |
| Refinement 1 | 1c        | Review compliance requirements by region, consent rules  | MOps Manager, Legal (if avail)   | Approved compliance framework       |
| Sign-Off     | 1d        | Final subscription type + compliance spec approval       | VP Marketing, MOps Manager       | Signed-off strategic package        |

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held — gap analysis presented, subscription types validated
- [ ] 1c. Refinement loop complete — compliance framework approved
- [ ] 1d. Strategic sign-off obtained on subscription types, consent rules, and preference center scope

##### Phase 2: Engineering
- [ ] 2a. Tech spec created (subscription types, consent fields, preference center design, automation logic)
- [ ] 2b. Engineering handoff meeting held
- [ ] 2c. Build complete (subscription types, preference center, consent tracking, GDPR/CCPA workflows, automations)
- [ ] 2d. QA/Test + customer sign-off on all compliance mechanisms

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped (subscription management guide, compliance SOPs, DSAR handling process)
- [ ] 3b. Training sessions delivered (technical + leadership)
- [ ] 3c. Hypercare period complete (2 weeks)
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff complete
- [ ] 4c. External handoff complete
- [ ] 4d. Project closed and archived

#### Document Types

##### Working Documents (iterate together)

| Document                         | Purpose                                          | When Complete                          |
| -------------------------------- | ------------------------------------------------ | -------------------------------------- |
| Email program inventory          | Catalog all current email types and audiences    | All email types documented             |
| Subscription type mapping table  | Map email programs to subscription categories    | Stakeholder-approved type list         |
| Compliance requirements matrix   | Document GDPR/CCPA/CAN-SPAM requirements by region | All applicable regulations addressed |
| Consent field mapping            | Define consent tracking fields and data sources  | Fields mapped to all consent events    |

##### Deliverables (polished outputs)

| Deliverable                     | Created From                   | Customer Uses For                      |
| ------------------------------- | ------------------------------ | -------------------------------------- |
| Subscription type configuration | Subscription type mapping      | Reference for email program setup      |
| Preference center (live)        | Design spec + brand assets     | Contact self-service subscription mgmt |
| Compliance documentation        | Requirements matrix            | Audit trail and regulatory reference   |
| DSAR response SOP               | Compliance requirements matrix | Handling data subject requests         |

#### Enablement Details

##### Training Types

| Type       | Audience                         | Focus                                        | Duration |
| ---------- | -------------------------------- | -------------------------------------------- | -------- |
| Leadership | VP Marketing, Marketing Director | Compliance obligations, risk overview, preference center KPIs | 30m |
| Technical  | MOps Manager, Marketing Ops team | Subscription type management, preference center admin, consent field maintenance, DSAR handling | 60m |

##### Hypercare
- Applies: Yes
- Duration: 2 weeks
- Office Hours: Yes — Weekly 30-min slot for compliance questions and subscription management issues

##### Training Assets to Create
- [ ] Video walkthrough: Preference center walkthrough and admin guide
- [ ] Video walkthrough: How to set up emails with correct subscription type filtering
- [ ] Doc: Subscription type definitions and email program mapping
- [ ] Doc: DSAR response SOP (with disclaimer: not legal advice)
- [ ] Doc: Compliance checklist for ongoing email operations

#### Handoff & Retention

##### Internal Handoff
- Key context: Subscription type structure, consent field logic, which regions have GDPR vs. CCPA treatment, preference center customization details
- Escalation trigger: Any changes to compliance requirements, new geographic regions, or subscription type restructuring

##### External Handoff
- Final meeting agenda: Walk through subscription types, preference center, consent tracking, compliance checklist, maintenance schedule
- Documentation package: Subscription type definitions, field mappings, workflow documentation, compliance checklist, DSAR SOP

##### Maintenance Schedule
- Monthly: Audit subscription filter compliance in email sends, review unsubscribe rates by type
- Quarterly: Full compliance audit, consent tracking validation, preference center usage review
- Who owns: Single project = customer owns | Dedicated = Architect owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services -> if no -> Downsell: Email Operations Nurture Program or Email Templates & Build Process project -> Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~quarter out
- Internal prep trigger: 2 weeks before
- Decision: Architect handles / SME needed

#### Key Assets

| Asset                          | When Used      |
| ------------------------------ | -------------- |
| Subscription type mapping template | Phase 1 Strategy |
| Consent field specification doc | Phase 2 Engineering |
| Compliance checklist template  | Phase 4 Handoff |
| DSAR response SOP template    | Phase 3 Enablement |

#### Definition Alignment Terms

| Term                    | Typical Definition                                                                 |
| ----------------------- | ---------------------------------------------------------------------------------- |
| Subscription Type       | A category of email communication a contact can opt into or out of (e.g., Marketing Newsletter, Product Updates) |
| Preference Center       | A self-service web page where contacts manage their email subscription preferences |
| Consent                 | A contact's documented permission to receive a specific type of communication      |
| Double Opt-In           | A two-step consent process where the contact confirms their subscription via a confirmation email |
| Transactional Email     | System-generated emails tied to a specific action (e.g., password reset, order confirmation) — not subject to marketing opt-out |
| Data Subject Access Request (DSAR) | A formal request from a contact to access, modify, or delete their personal data under GDPR or CCPA |
| Lawful Basis            | The legal justification for processing personal data under GDPR (consent, legitimate interest, contractual necessity) |
| Suppression List        | A list of contacts who have unsubscribed and must not receive marketing emails     |

#### Common Gotchas
- Over-complicated subscription types (too many options confuse contacts) -> Start with 3-5 broad categories, expand only when data supports it
- Missing consent timestamps -> Always capture consent source, date, and method at field level from day one
- Treating transactional emails as marketing -> Clearly separate transactional from marketing subscription types; transactional must never be unsubscribable
- Delayed unsubscribe processing -> Ensure unsubscribes are honored immediately (within hours), not batched — CAN-SPAM requires processing within 10 business days [1], but GDPR expects "without undue delay" [2]
- Pre-checked consent boxes for EU contacts -> Violates GDPR; consent must be affirmative and explicit [2]
- Forgetting "Do Not Sell" tracking for CCPA -> California residents have the right to opt out of personal data sale; must track this separately [3]

#### Methodology Options

| Option                     | When to Use                                      | Complexity |
| -------------------------- | ------------------------------------------------ | ---------- |
| HubSpot-native preference center | Client uses HubSpot Marketing Hub Pro+, standard needs | Low |
| Custom preference center   | Client needs advanced frequency controls, multi-brand, or non-standard UX | High |
| Marketo subscription management | Client uses Marketo, needs subscription categories + tokens | Medium |
| Hybrid (MAP + external consent tool) | Client has multiple MAPs or needs centralized consent management across platforms | High |

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on subscription types, compliance requirements, and preference center scope.
>
> **Output:** Approved subscription type list + compliance requirements matrix + preference center design spec.

### 1a. Pre-Kickoff

> Two parallel tracks run before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                | Format             |
| ----------------------------- | ------------------------------------------------------ | ------------------ |
| Email program inventory form  | Catalog all email types, frequencies, and audiences    | Google Form        |
| Geographic region questionnaire | Determine GDPR/CCPA/CAN-SPAM applicability           | Google Form        |
| Brand asset request           | Collect logo, colors, and copy for preference center   | Email with checklist |
| Definition Alignment Document | Get sign-off on subscription, consent, and compliance terms | Google Doc    |

**Completion tracking:** Push hard before kickoff — missing email inventory or region data slows the entire project.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                     | Output                              |
| ---- | ---------------------------------------------------------- | ----------------------------------- |
| 1    | Pull current MAP subscription type configuration           | Existing subscription type list     |
| 2    | Audit opt-in mechanisms (forms, landing pages, imports)    | Opt-in source inventory             |
| 3    | Review consent tracking (fields, timestamps, source)       | Consent tracking gap analysis       |
| 4    | Identify existing preference center or unsubscribe flow    | Current preference center assessment |
| 5    | Map applicable regulations to client's geographic footprint | Compliance requirements matrix (draft) |

**Critical:** Mark all findings as ASSUMED. The kickoff call validates.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building anything.

| Term                    | Our Definition                                                             | Internally Approved? |
| ----------------------- | -------------------------------------------------------------------------- | -------------------- |
| Subscription Type       | A category of email communication a contact can opt into or out of         | [ ] Yes / [ ] No     |
| Marketing Email         | Any email sent for promotional purposes (newsletters, events, offers)      | [ ] Yes / [ ] No     |
| Transactional Email     | System emails tied to a specific user action (not subject to opt-out)      | [ ] Yes / [ ] No     |
| Consent                 | Documented permission to receive a specific communication type             | [ ] Yes / [ ] No     |
| Double Opt-In           | Two-step confirmation process required for EU contacts under GDPR          | [ ] Yes / [ ] No     |
| Lawful Basis            | Legal justification for processing data (consent, legitimate interest)     | [ ] Yes / [ ] No     |
| Data Subject Access Request | Formal request to access, modify, or delete personal data             | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your marketing and legal teams. Check "Yes" when approved. We cannot proceed to build until all terms are aligned.

---

### 1b. Kickoff Call

> **Purpose:** Present gap analysis and get alignment on subscription types, compliance requirements, and preference center scope.

#### Agenda (60 min)

| Time  | Topic                            | What Happens                                           |
| ----- | -------------------------------- | ------------------------------------------------------ |
| 0-15  | Walk through current state audit | "Here's what we found in your MAP"                     |
| 15-30 | Present gap analysis             | Identify compliance risks and missing capabilities     |
| 30-40 | Validate subscription type list  | Review proposed categories, adjust based on feedback   |
| 40-50 | Compliance requirements review   | Confirm GDPR/CCPA/CAN-SPAM applicability by region     |
| 50-60 | Next steps                       | Assign homework, schedule refinement meeting           |

#### What We Bring

- Current state audit (subscription types, consent tracking, preference center)
- Gap analysis document (compliance risks ranked by severity)
- Proposed subscription type list with descriptions
- Definition Alignment Document (pre-filled with recommendations)

#### What We Leave With

- Validated subscription type list (or clear action items to finalize)
- Confirmed geographic compliance requirements
- Identified stakeholders for consent language review
- Homework assignments for next meeting

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Iterate on subscription type definitions, compliance framework, and preference center scope until sign-off.

#### The Pattern

```
Kickoff Call (present audit, gather feedback)
    |
Update subscription type list + compliance matrix
    |
Refinement Meeting (present updated spec, gather final inputs)
    |
Final Review -> Sign-off
```

This project typically requires only 1-2 refinement meetings. The main variables are:
- Whether legal/compliance stakeholders need separate review time
- Whether the client markets to EU contacts (adds GDPR complexity)
- Whether a custom preference center is needed (adds design review)

#### Potential Meeting Types

| Meeting Type            | Focus                                            | Stakeholder                    |
| ----------------------- | ------------------------------------------------ | ------------------------------ |
| Subscription Definition | Finalize subscription type names, descriptions, defaults | VP Marketing, MOps Manager |
| Compliance Review       | GDPR consent rules, CCPA requirements, legal basis mapping | MOps Manager, Legal/Compliance |
| Preference Center Design | Layout, branding, frequency controls, UX review | MOps Manager, Marketing        |
| Final Review            | Full spec walkthrough, sign-off                  | All stakeholders               |

#### Typical Timeline

| Milestone               | Timing                      |
| ----------------------- | --------------------------- |
| Pre-kickoff prep        | 1-2 days                    |
| Kickoff call            | Day 1 of engagement         |
| Refinement meeting(s)   | 1-2 weeks                   |
| Final review + sign-off | When all inputs confirmed   |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything before building.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by stakeholders
- [ ] Subscription type list approved (names, descriptions, defaults, required vs. optional)
- [ ] Compliance requirements confirmed by region (GDPR, CCPA, CAN-SPAM)
- [ ] Preference center scope agreed (native vs. custom, frequency controls, branding)
- [ ] Consent field design validated (status, timestamp, source, legal basis)
- [ ] No blockers for engineering

#### Decision Point

- **Proceed to Engineering** -> Customer wants the full subscription framework built
- This project does NOT have a natural exit point after Phase 1 — the value is in the technical build

---

## Phase 2: Engineering

> **Goal:** Build and test the complete subscription management infrastructure.
>
> **Output:** Fully configured subscription types, preference center, consent tracking fields, compliance workflows, and subscription management automations — all tested and customer-approved.

| Project Type         | Engineering Weight | Example                                                |
| -------------------- | ------------------ | ------------------------------------------------------ |
| This project         | Heavy (60-70%)     | MAP subscription types, preference center, consent fields, GDPR/CCPA workflows, automations |

### Sub-Phases

```
2a Tech Spec -> 2b Engineering Handoff -> 2c Build -> 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate the approved subscription type list, compliance framework, and preference center scope into technical specifications.

**Input:** Signed-off strategic package from Phase 1

**Output:** Draft tech spec containing:

- Subscription type configuration (names, descriptions, default opt-in/opt-out per type, required vs. optional)
- Preference center design spec (layout, branding, subscription checkboxes/toggles, frequency options, "Unsubscribe from All" behavior)
- Consent tracking field definitions (consent\_status, consent\_date, consent\_source, legal\_basis per subscription type)
- GDPR-specific workflow logic (double opt-in flow, geographic consent rules, consent withdrawal mechanism)
- CCPA-specific workflow logic (Do Not Sell field, DSAR response workflow, deletion/anonymization process)
- Unsubscribe handling spec (one-click header, confirmation page, suppression list automation)
- Subscription management automation logic (form submission workflows, import rules, sunset automation, welcome workflows)
- Build sequence (what to build first)

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs with engineer before building.

**Agenda (30-45 min):**

| Time  | Topic              | What Happens                                          |
| ----- | ------------------ | ----------------------------------------------------- |
| 0-15  | Walk through specs | Architect explains compliance context + subscription logic |
| 15-30 | Engineer questions | Clarify MAP-specific implementation details, flag risks |
| 30-45 | Refine and approve | Adjust specs, confirm build approach                  |

**What Architect brings:**

- Strategic package (subscription type list, compliance requirements, preference center scope)
- Draft tech spec (from 2a)
- MAP access credentials and any platform-specific constraints

**What engineer leaves with:**

- Approved tech spec with clear build sequence
- Known risks (e.g., MAP edition limitations, custom preference center complexity)
- Platform-specific notes (HubSpot Marketing Hub Pro+ required for custom subscription types, Marketo tokens for preference center)

---

### 2c. Build (Configure)

> **Purpose:** Build the complete subscription management infrastructure in the client's MAP.

**Input:** Approved tech spec from 2b

**Build sequence — execute in this order:**

**Step 1: Create Subscription Types in MAP**
- Create each subscription type in HubSpot Settings > Marketing > Email > Subscription Types (or Marketo Admin > Email > Subscription Management) [7]
- Configure default opt-in/opt-out status for new contacts per type
- Set subscription type descriptions (visible in preference center)
- Define which types are required vs. optional
- Configure email associations (which emails map to which subscription type)
- Test subscription type behavior with sample contacts

**Step 2: Build Preference Center**
- Design preference center layout (subscription options, frequency settings if applicable)
- Configure branding (logo, colors, copy per brand guidelines)
- Implement subscription type checkboxes or toggles
- Add "Unsubscribe from All" option with appropriate warning messaging
- Include email frequency options if applicable (daily digest vs. immediate) [8]
- Set up confirmation messaging for preference updates
- Test preference center across devices (desktop, mobile, tablet) and browsers

**Step 3: Configure Consent Tracking Fields**
- Create `consent_status` field (Opted In, Opted Out, Not Set) per subscription type
- Create `consent_date` timestamp field per subscription type
- Create `consent_source` field (form name, import, API, preference center) per subscription type
- Create `legal_basis` field for GDPR contacts (consent, legitimate interest, contract)
- Set up field update automation when consent changes (any status change triggers timestamp + source update)
- Document field mapping for DSAR handling

**Step 4: Implement GDPR-Specific Flows**
- Configure double opt-in workflow for EU contacts (geographic trigger based on country field or IP)
- Create confirmation email with explicit consent language (no pre-checked boxes)
- Set up geographic-based consent rules (EU vs. non-EU treatment)
- Implement consent withdrawal mechanism (preference center opt-out triggers consent\_status update)
- Document lawful basis for each email type (consent vs. legitimate interest)

**Step 5: Implement CCPA-Specific Flows**
- Create `do_not_sell` tracking field
- Configure opt-out of sale mechanism (if applicable)
- Set up DSAR response workflow (10-day acknowledgment requirement, 45-day response window) [3]
- Document data categories collected for disclosure requests
- Configure contact deletion/anonymization workflow
- Create internal SOP for handling CCPA requests within required timeframes

**Step 6: Configure Unsubscribe Handling**
- Enable one-click unsubscribe in email headers (RFC 8058 compliance, required by Gmail and Yahoo as of February 2024) [4]
- Configure unsubscribe confirmation page messaging
- Set up suppression list automation for hard unsubscribes
- Define behavior for partial unsubscribes (one type vs. all types)
- Verify unsubscribe requests are honored immediately (not batched)

**Step 7: Build Subscription Management Automations**
- Build form submission workflow to update subscription types based on form selections
- Create import process rules for setting subscription status on list uploads
- Configure API integration rules for subscription updates from external systems
- Set up re-engagement workflow triggers based on subscription changes
- Build sunset automation for chronically unengaged contacts (e.g., no opens in 90+ days -> move to suppression)
- Create welcome workflow triggered by new subscription opt-ins

**Step 8: Validate Subscription Filtering in Email Sends**
- Audit all existing email programs for subscription type filtering
- Update email send lists to respect subscription preferences
- Configure smart lists/segments that dynamically filter by subscription status
- Document email program -> subscription type mapping

**Build tracking:**

- [ ] Subscription types created and configured
- [ ] Preference center built and branded
- [ ] Consent tracking fields created
- [ ] GDPR workflows configured
- [ ] CCPA workflows configured
- [ ] Unsubscribe handling configured
- [ ] Subscription management automations built
- [ ] Email send filtering validated

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify the subscription management framework works end-to-end and get customer approval.

**Two types of testing:**

| Type              | Who      | Purpose                                              |
| ----------------- | -------- | ---------------------------------------------------- |
| Technical Testing | Our team | Verify all subscription types, consent fields, preference center, and automations work correctly |
| Customer Testing  | Customer | Verify the system handles their real-world scenarios |

**Technical testing checklist:**

- [ ] Each subscription type correctly filters email sends (opted-in contacts receive, opted-out do not)
- [ ] Preference center renders correctly across devices and browsers
- [ ] Preference center updates propagate to contact record immediately
- [ ] Consent tracking fields update with correct status, timestamp, and source on every consent change
- [ ] Double opt-in workflow fires for EU contacts and does NOT fire for non-EU contacts
- [ ] GDPR consent checkboxes are NOT pre-checked on forms
- [ ] One-click unsubscribe works in email headers
- [ ] Unsubscribe requests are honored immediately (no batch delays)
- [ ] Suppression list automation prevents re-subscribing unsubscribed contacts
- [ ] "Unsubscribe from All" removes contact from all marketing subscription types
- [ ] Transactional emails are NOT affected by marketing unsubscribes
- [ ] CCPA "Do Not Sell" field correctly populates when opt-out is submitted
- [ ] DSAR workflow triggers correctly and meets acknowledgment timeline
- [ ] Sunset automation correctly identifies unengaged contacts
- [ ] Form submission workflows correctly update subscription types
- [ ] Import rules correctly set subscription status on list uploads

**Customer testing:**

- Walk customer through preference center self-service flow
- Have them test opt-in and opt-out scenarios
- Verify email filtering with a real email send to a test list
- Confirm compliance documentation matches their understanding

**Engineering sign-off checkpoint:**

- [ ] Built system matches tech spec
- [ ] All technical tests passing
- [ ] Customer has tested and approved
- [ ] Ready for enablement

**Decision point:**

- **Proceed to Enablement** -> System is built and tested, needs training/adoption
- **Loop back to Build** -> Issues found, needs fixes

---

## Phase 3: Enablement

> **Goal:** Customer team can manage subscriptions, handle compliance requests, and maintain the system independently.
>
> **Output:** Trained team with documentation, stabilized system, no critical issues.

### Sub-Phases

```
3a Training Prep -> 3b Training Sessions -> 3c Hypercare -> 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from strategic and technical documentation.

**Input:** Strategic package + tech specs + built system

**Output:** Training package containing:

- Video walkthrough script: Preference center admin walkthrough (how to view/manage subscriptions, add new types)
- Video walkthrough script: How to set up emails with correct subscription type filtering
- Written guide: Subscription type definitions with email program mapping
- Written guide: DSAR response SOP (step-by-step process with timeline requirements, with disclaimer: not legal advice)
- Written guide: Ongoing compliance checklist for email operations
- FAQ draft: Common questions about subscription management, consent tracking, and compliance scenarios

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to customer team.

**Two types of training:**

| Type                | Audience                         | Focus                                                                     |
| ------------------- | -------------------------------- | ------------------------------------------------------------------------- |
| Leadership training | VP Marketing, Marketing Director | Compliance risk overview, preference center KPIs, what regulatory obligations look like |
| Technical handoff   | MOps Manager, Marketing Ops team | Day-to-day subscription management, preference center admin, consent field maintenance, DSAR handling, adding new subscription types |

**Leadership training (30 min):**
- Why subscription compliance matters: GDPR fines exceeded EUR 1.6 billion in 2024 alone [1], and CAN-SPAM penalties can reach $53,088 per non-compliant email [5]
- How the preference center reduces risk and improves subscriber experience
- Key KPIs to monitor (unsubscribe rate by type, preference center self-service rate, compliance audit results)
- When to involve legal (new regions, new data collection practices, regulatory changes)

**Technical training (60 min):**
- Subscription type management: how to add/edit types, set defaults, map to emails
- Preference center administration: branding updates, adding frequency options, troubleshooting
- Consent tracking: how fields update, where to audit consent history
- DSAR handling: step-by-step walkthrough of the response process with timeline requirements
- Email send compliance: how to verify subscription filtering before every send
- Common scenarios and edge cases

**Training delivery:**

1. Schedule sessions with appropriate stakeholders
2. Deliver training (live, recorded for future reference)
3. Record video walkthroughs of key workflows
4. Answer questions, note gaps

**Output:**

- Trained stakeholders
- Video walkthrough recordings
- Questions log (feeds into FAQ)

---

### 3c. Hypercare

> **Purpose:** Intensive post-launch support to stabilize the subscription management system.

**Duration:** 2 weeks

**What happens:**

- Quick response to issues (subscription filtering errors, consent tracking gaps, preference center bugs)
- Office hours: weekly 30-min slot for compliance and subscription management questions
- Monitor first 2-3 email sends for correct subscription filtering
- Verify DSAR process works with a real (or simulated) request if possible
- Bug triage and fixes

**When to extend:** If the client has a complex multi-region setup (EU + California + other jurisdictions) or a custom preference center with ongoing design iterations.

**Output:** Stabilized system, no critical compliance gaps outstanding

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm customer can operate independently.

**Validation checkpoint:**

- [ ] All training sessions delivered
- [ ] Training recordings and documentation provided
- [ ] Hypercare period complete
- [ ] No critical issues outstanding
- [ ] MOps team can add new subscription types without support
- [ ] MOps team can handle a DSAR without support
- [ ] Marketing team sends emails with correct subscription filtering consistently
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** -> Customer is enabled, project wrapping up
- **Extend Hypercare** -> Still unstable, needs more support time

---

## Phase 4: Handoff

> **Goal:** Clean project close with maintenance plan established and retention/expansion path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the system, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule -> 4b Internal Handoff -> 4c External Handoff -> 4d Project Close
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At                                                                         |
| ----------------------------- | -------------------- | ------------------------------------------------------------------------------------- |
| **Single Project**            | Customer owns        | 4c (External Handoff) — customer receives maintenance schedule and runs it themselves |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) — Architect receives maintenance schedule and runs it for customer |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention after the project is complete.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task                     | What to Check                                     | Red Flag Threshold                          |
| -------------------------------- | ------------------------------------------------- | ------------------------------------------- |
| Subscription filter audit        | All email sends used correct subscription type filtering | Any email sent without proper filtering |
| Unsubscribe rate review          | Unsubscribe rate per subscription type per send   | >0.5% sustained unsubscribe rate per send [6] |
| Consent tracking validation      | Spot-check 10-20 recent contacts for consent field accuracy | Any contacts missing consent timestamps |
| Preference center usage review   | Self-service preference updates vs. direct unsubscribes | Self-service rate drops below 50%        |

**Quarterly Tasks:**

| Quarterly Task                   | What to Review                                    | Action if Off-Track                        |
| -------------------------------- | ------------------------------------------------- | ------------------------------------------ |
| Full compliance audit            | GDPR/CCPA/CAN-SPAM compliance across all email programs | Remediate gaps, update SOPs              |
| Subscription type relevance      | Are current types still aligned with email programs? | Consolidate or add types as needed        |
| DSAR process test                | Simulate a DSAR to verify workflow still fires correctly | Fix any broken steps, update SOP         |
| Consent database health check    | % of contacts with valid consent tracking fields  | Target >95% coverage; remediate gaps       |

**After First Business Cycle (30-60 days post-launch):**

- Validate that unsubscribe rates are within healthy range (0.1-0.3% per send)
- Confirm preference center self-service rate (target: >80% of preference changes happen via self-service vs. direct unsubscribe)
- Verify zero compliance violations or unsubscribe complaints
- Review subscription type engagement rates — are contacts using the granularity or defaulting to "Unsubscribe from All"?

**Refinement Triggers (when to re-engage):**

| Trigger                          | Threshold                                        | Response                                     |
| -------------------------------- | ------------------------------------------------ | -------------------------------------------- |
| Compliance violation/complaint   | Any reported violation                           | Immediate audit, remediate, update SOPs      |
| New geographic region            | Client expands to EU, California, Canada, etc.   | Re-engage to add compliance mechanisms       |
| Unsubscribe spike                | >0.5% sustained across 3+ sends                 | Review email frequency, content relevance, subscription type structure |
| Regulatory change                | New privacy law or amendment (e.g., new state privacy law) | Assess impact and update configurations |

**Every 6-12 Months:**

- Full system review: subscription types, preference center, consent tracking, compliance workflows
- Regulatory landscape check: any new laws or enforcement trends affecting email operations
- Preference center UX review: update design, add features based on subscriber feedback
- Re-train any new marketing team members

---

### 4b. Internal Handoff

> **Purpose:** Transfer context so Architect can manage ongoing relationship.

**What the Architect needs to know:**

- Subscription type structure and which email programs map to each type
- Consent tracking field logic (how fields update, what triggers changes)
- Which regions have GDPR vs. CCPA treatment and how geographic rules work
- Preference center customization details (native vs. custom, any platform-specific quirks)
- DSAR handling SOP and timeline requirements
- Common issues and how to resolve them
- When to escalate

**Escalation guidelines:**

| Issue Type                                       | Who Handles                | Analogy                 |
| ------------------------------------------------ | -------------------------- | ----------------------- |
| Adding a new subscription type, minor preference center updates | Architect           | General contractor      |
| Compliance framework changes, new region setup, GDPR/CCPA workflow modifications | SME | Specialist tradesperson |

**For Dedicated engagements:** Architect receives the maintenance schedule (4a) and becomes responsible for executing monthly and quarterly tasks.

---

### 4c. External Handoff

> **Purpose:** Formal project completion with customer.

**Final project meeting:**

- Review what was delivered (subscription types, preference center, consent tracking, compliance workflows, automations)
- Walk through documentation package
- Walk through compliance checklist for ongoing operations
- Demonstrate preference center admin tasks
- Walk through DSAR response SOP (with reminder: this does not constitute legal advice)
- Confirm nothing outstanding
- Make it explicit: "Project complete"
- **For Single Project engagements:** Walk customer through the maintenance schedule (4a) in detail

**Documentation package:**

- Subscription type definitions (names, descriptions, defaults, email mappings)
- Consent field specification (field names, data types, update triggers)
- Preference center documentation (URL, admin access, customization guide)
- Workflow documentation (all automations with trigger conditions and actions)
- Compliance checklist for ongoing email operations
- DSAR response SOP (with legal disclaimer)
- Video walkthrough recordings
- FAQ document
- Definition Alignment Document (final version)
- Maintenance schedule

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

- What went well?
- What would we do differently?
- Any compliance edge cases to feed back into the playbook?
- Any MAP-specific quirks to document for future projects?

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell -> Downsell -> Retry  |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (retainer for ongoing compliance monitoring + email ops support)
   | if no
2. Downsell: Email Operations Nurture Program OR Email Templates & Build Process project
   | if yes
3. Retry retainer at end of next project cycle
```

**Script:**

> "Now that your subscription management framework is in place, there are two ways we can continue working together. Option 1: We can put you on managed services where we handle ongoing compliance monitoring, subscription type optimization, and email operations support. Option 2: If you need help building out your nurture programs or email templates on top of this compliance foundation, we can scope that as a next project. Which sounds more interesting?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On [date ~quarter out], we'll review how the subscription framework is performing — unsubscribe rates, preference center usage, and compliance audit results — and see if any adjustments are needed."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                            |
| ------------------- | ------------------------------------------------------- |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks        |
| 2. Review metrics   | Pull unsubscribe rates, preference center usage, compliance audit results |
| 3. Decide ownership | Can Architect handle this check-in, or need SME?       |
| 4. Prep materials   | If SME needed, brief them. If Architect, prep talking points. |

**At the refinement check-in:**

- Review performance against original goals (zero compliance violations, >80% preference center self-service rate, &lt;0.3% unsubscribe rate)
- Identify any adjustments needed (new subscription types, preference center updates, new region compliance)
- If minor: Architect handles tweaks
- If major: Scope new project (e.g., new region compliance, preference center redesign)

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- Subscription type mapping (email programs -> subscription categories with definitions and defaults)
- Compliance requirements matrix (regulations by region with specific requirements)
- Preference center design spec (layout, branding, features)

**Technical Deliverables:**

- Configured subscription types in HubSpot/Marketo
- Live preference center (branded, responsive, self-service)
- Consent tracking fields (status, timestamp, source, legal basis per subscription type)
- GDPR compliance workflows (double opt-in, geographic consent rules, consent withdrawal)
- CCPA compliance workflows (Do Not Sell tracking, DSAR response automation, deletion/anonymization)
- Unsubscribe handling (one-click header, confirmation pages, suppression automation)
- Subscription management automations (form workflows, import rules, sunset automation, welcome workflows)
- Validated email send filtering (all programs respect subscription preferences)

**Documentation Package:**

- Video walkthrough recordings (preference center admin, email setup with subscription filtering)
- Written guides (subscription type definitions, consent field mapping, DSAR response SOP)
- Compliance checklist for ongoing email operations
- FAQ document
- Definition Alignment Document (final version)
- Maintenance schedule

---

## Troubleshooting Guide

> Common scenarios and resolutions for subscription management and compliance issues.

| Scenario | Symptoms | Resolution |
| -------- | -------- | ---------- |
| Contact receives email after unsubscribing | Unsubscribe processed but email already queued; or email mapped to wrong subscription type | Verify email-to-subscription-type mapping; check for batch send timing; confirm suppression list automation fires immediately |
| Preference center not updating contact record | Contact clicks "Save Preferences" but consent fields unchanged | Check preference center -> MAP integration; verify field mapping; test in incognito browser to rule out caching |
| Double opt-in email not sending for EU contacts | EU contacts added but no confirmation email triggered | Verify geographic trigger logic (country field or IP-based); check workflow enrollment criteria; confirm confirmation email is active |
| Consent timestamps missing for imported contacts | Bulk import does not trigger consent field automations | Create import-specific workflow that sets consent\_source = "Import" and consent\_date = import timestamp; add to import SOP |
| "Unsubscribe from All" not removing from all types | Contact clicks global unsubscribe but still receives some emails | Verify transactional vs. marketing separation; check if any email types are bypassing subscription filtering |
| Unsubscribe rate spiking after launch | >0.5% unsubscribe rate on multiple sends | Review email frequency (sending more than 1 promotional email per day doubles unsubscribe rates [6]); check subscription type relevance; audit that preference center frequency controls work |
| DSAR request not acknowledged within timeline | DSAR received but no auto-acknowledgment fires | Verify DSAR workflow trigger (form submission, email alias, API endpoint); check 10-day acknowledgment email is active |
| Pre-checked consent boxes on forms | GDPR audit reveals pre-checked consent checkboxes | Remove default checked states from all forms with consent capture; re-test all forms across all pages |

---

## References

[1] [MailDiver - GDPR Email Marketing Compliance Guide 2025](https://maildiver.com/blog/gdpr-email-marketing-compliance-guide/)
[2] [Scrut - Avoiding GDPR Fines in 2025: Enforcement Trends and Tips](https://www.scrut.io/hub/gdpr/gdpr-fines-penalties-us-eu-guide)
[3] [Termly - CCPA DSAR Requirements](https://termly.io/resources/guides/ccpa-dsar-requirements/)
[4] [Mailjet - Email Compliance Audit: GDPR, CAN-SPAM, and CCPA](https://www.mailjet.com/blog/email-best-practices/email-compliance-audit/)
[5] [Zoho Campaigns - Email Laws GDPR CAN-SPAM Compliance Best Practices](https://www.zoho.com/campaigns/marketingmatchbox/email-laws-gdpr-can-spam-compliance-best-practices.html)
[6] [Amra and Elma - Email Unsubscribe Rate Statistics 2025](https://www.amraandelma.com/email-unsubscribe-rate-statistics/)
[7] [HubSpot - Set Up Email Subscription Types](https://knowledge.hubspot.com/marketing-email/set-up-email-subscription-types)
[8] [Moosend - Email Preference Center Best Practices 2026](https://moosend.com/blog/email-preference-center-best-practices/)

---

## Appendix

### Roles

| Role | What They Do |
|---|---|
| **Architect** | Owns the customer relationship, leads strategy, creates specs, does enablement, owns account post-delivery |
| **Engineer** | MAP build, automation, configuration (Phase 2) |
| **SME** | Specialist brought in for project-specific compliance and technical work |

### Phase Gate Summary

| Phase                    | Output                                                                 | Gate Criteria                                                                  |
| ------------------------ | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **Phase 1: Strategy**    | Signed-off strategic package (subscription types + compliance framework + preference center scope) | Customer stakeholders have approved definitions and strategic assets |
| **Phase 2: Engineering** | Built and tested subscription management system                        | System matches tech spec, all tests pass, customer has approved                |
| **Phase 3: Enablement**  | Trained team with documentation                                        | All training delivered, hypercare complete, team can operate independently     |
| **Phase 4: Handoff**     | Independent customer + archived project                                | Internal/external handoffs complete, maintenance plan in place, project closed |

### How to Adapt Per Project Type

This project is **Engineering-heavy**:

| Project Profile       | Strategy Weight | Engineering Weight | Enablement Weight |
| --------------------- | --------------- | ------------------ | ----------------- |
| **Engineering-heavy** | 10-20%          | 60-70%             | 15-25%            |

**Adaptation rules:**

- **Phase 1 (Light):** 2-3 meetings total. Strategy is about defining subscription types and confirming compliance requirements, not deep strategic modeling.
- **Phase 2 (Heavy):** The core of the project. 8 build steps executed in sequence. Most time spent here.
- **Phase 3 (Medium):** Standard training + 2-week hypercare. Compliance SOP training is important — do not skip the DSAR walkthrough.
- **Phase 4 (Always applies):** Every project needs handoff. The compliance checklist and maintenance schedule are particularly important for this project type.

### Single vs. Dedicated Engagement

| Engagement Type               | What It Means                        | Key Difference                              |
| ----------------------------- | ------------------------------------ | ------------------------------------------- |
| **Single Project**            | One-off project engagement           | Customer owns maintenance post-handoff (4c) |
| **Dedicated (Multi-Project)** | Ongoing retainer / multiple projects | Architect owns maintenance post-handoff (4b) |
