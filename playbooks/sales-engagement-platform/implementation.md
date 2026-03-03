# Sales Engagement Platform — Implementation

## Project One-Pager

```markdown
# Sales Engagement Platform One-Pager

## Project Type

- Category: Technical
- Primary Deliverable: Fully configured sales engagement platform (Outreach, Salesloft, Amplemarket, or similar) integrated with CRM, with automated sequences, dialer setup, email infrastructure, reporting dashboards, and trained sales team

### Phase Relevance

| Phase          | Applies? | Weight | Notes                                                      |
| -------------- | -------- | ------ | ---------------------------------------------------------- |
| 1. Strategy    | Yes      | Light  | Requirements gathering, platform selection, success criteria |
| 2. Engineering | Yes      | Heavy  | CRM integration, email infra, dialer, sequences, workflows  |
| 3. Enablement  | Yes      | Med    | Pilot testing, full team training, quick-reference guides    |
| 4. Handoff     | Yes      | Med    | Troubleshooting guide, maintenance schedule, ownership transfer |

---

## Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │    Light     │     │    Heavy     │     │     Med      │     │     Med      │
  │ 1a→1b→1c→1d │     │ 2a→2b→2c→2d │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   Requirements +       CRM + email infra     Pilot + full team    Troubleshooting +
   platform selection   dialer + sequences    training             maintenance schedule
```

**This project's flow:**
- Full 4-phase. Light strategy (requirements + platform selection), heavy engineering (CRM connection, email infrastructure, dialer, sequences, automations, dashboards), medium enablement (pilot + full team training), standard handoff.
- Phase 2 carries the bulk of the work. Typical timeline is 4-8 weeks end-to-end depending on platform complexity and team size.
- Some customers skip dialer setup (Step 3 in Phase 2) if phone-based outreach is not a priority channel.

---

## Pre-Kickoff (1a)

### Track A: Customer Homework
- [ ] Provide admin access to CRM (Salesforce or HubSpot) with API permissions
- [ ] Provide admin access to email system (Google Workspace or Microsoft 365)
- [ ] Complete intake form: current outreach tools, team size, territory structure, primary outreach channels
- [ ] Share current sequence/cadence examples if any exist
- [ ] Provide list of users to be licensed on the platform
- [ ] Share ideal customer profile (ICP) and target segments for sequence design

### Track B: Architect Prep
- [ ] Interview 3-5 SDRs/AEs on current outreach workflow (email, phone, LinkedIn, manual tasks)
- [ ] Pull activity metrics from CRM to establish baseline (emails sent, calls logged, response rates)
- [ ] Document current tools in use (CRM native sequences, spreadsheets, manual tracking)
- [ ] Quantify time spent on manual tasks vs. actual selling time
- [ ] Draft gap analysis: current state vs. target state
- [ ] Prepare platform comparison matrix (Outreach, Salesloft, Amplemarket, Apollo, Groove)

---

## Refinement Loop (1b → 1c → 1d)

| Meeting      | Sub-Phase | Focus                                          | Stakeholder                    | Output                           |
| ------------ | --------- | ---------------------------------------------- | ------------------------------ | -------------------------------- |
| Kickoff      | 1b        | Present gap analysis, confirm requirements     | VP Sales, RevOps, IT           | Validated requirements doc       |
| Platform Demo| 1c        | Demo shortlisted platforms, test use cases      | Sales leadership, RevOps, IT   | Platform selection + budget approval |
| Sign-Off     | 1d        | Confirm platform, success criteria, timeline    | All                            | Approved platform + project plan |

---

## Phase Checklists

### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held, requirements validated
- [ ] 1c. Platform demos conducted, selection made
- [ ] 1d. Strategic sign-off obtained (platform, budget, success criteria)

### Phase 2: Engineering
- [ ] 2a. Tech spec created (CRM integration, email infra, dialer, sequences, automations, dashboards)
- [ ] 2b. Engineering handoff meeting held
- [ ] 2c. Build complete (all platform components configured)
- [ ] 2d. QA/Test + customer sign-off

### Phase 3: Enablement
- [ ] 3a. Training materials prepped (video walkthrough scripts, quick-reference guides)
- [ ] 3b. Pilot testing with 3-5 users (1-2 weeks)
- [ ] 3c. Full team training sessions delivered
- [ ] 3d. Enablement sign-off

### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff (SME → Architect) complete
- [ ] 4c. External handoff (team → Customer) complete
- [ ] 4d. Project closed and archived

---

## Document Types

### Working Documents (iterate together)

| Document                    | Purpose                                  | When Complete                     |
|-----------------------------|------------------------------------------|-----------------------------------|
| Current State Audit         | Document current outreach process gaps   | All rep interviews complete, baseline metrics pulled |
| Platform Requirements Doc   | Must-have vs nice-to-have features       | Stakeholder agreement on requirements |
| Platform Comparison Matrix  | Score vendors against requirements       | Platform selected with budget approval |
| Sequence Framework          | Cadence patterns, channel mix, timing    | Naming conventions and governance rules defined |

### Deliverables (polished outputs)

| Deliverable                    | Created From              | Customer Uses For                   |
|--------------------------------|---------------------------|-------------------------------------|
| Configuration Documentation    | Build notes + tech spec   | Admin reference for platform settings |
| Sequence Library               | Sequence framework        | Reference for creating new sequences  |
| Quick-Reference Guide          | Training materials        | Daily rep usage guide                 |
| Dashboards & Reports           | Analytics setup           | Sales management visibility           |

---

## Enablement Details

### Training Types

| Type       | Audience                         | Focus                                          | Duration |
| ---------- | -------------------------------- | ---------------------------------------------- | -------- |
| Leadership | VP Sales, Sales Managers         | Dashboard interpretation, team analytics, ROI  | 30 min   |
| Rep        | SDRs, AEs                        | Sequences, tasks, dialer, daily workflow        | 60 min   |
| Admin      | RevOps, Sales Ops                | Platform admin, sequence governance, troubleshooting | 60 min   |

### Hypercare
- Applies: Yes
- Duration: 2 weeks post-full rollout
- Office Hours: Yes — weekly 30-min slot for Q&A and issue triage

### Training Assets to Create
- [ ] Video walkthrough: Platform overview and daily workflow for reps
- [ ] Video walkthrough: Dashboard walkthrough for managers
- [ ] Video walkthrough: Admin guide (user management, sequence governance, sync monitoring)
- [ ] Doc: Quick-reference guide for daily usage
- [ ] Doc: Sequence creation and editing SOP
- [ ] Doc: Troubleshooting guide for common issues

---

## Handoff & Retention

### Internal Handoff (SME → Architect)
- Key context for Architect: Platform type, CRM integration details, email infrastructure setup, sequence governance rules, daily send limits
- Escalation trigger: CRM sync failures, email deliverability drops below 85%, platform API changes, sequence logic changes

### External Handoff (Team → Customer)
- Final meeting agenda: Review platform configuration, walk through dashboards, confirm sequence library, review maintenance schedule
- Documentation package: Configuration settings, sequence library, governance doc, quick-reference guide, troubleshooting guide, training video walkthroughs

### Maintenance Schedule
- Monthly: Monitor email deliverability metrics, review sequence performance, audit CRM sync logs
- Quarterly: Full platform health review, sequence optimization, user license audit
- Who owns: Single project = customer owns | Dedicated = Architect owns

### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services (ongoing sequence optimization + deliverability monitoring) → if no → Downsell: Another project (e.g., Activity Capture, Conversation Intelligence) → Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~1 quarter post-launch
- Internal prep trigger: 2 weeks before
- Decision: Architect handles / SME needed

---

## Key Assets

| Asset                    | When Used           |
| ------------------------ | ------------------- |
| Platform Comparison Matrix | Phase 1 — platform selection |
| Sequence Framework Template | Phase 2 — sequence design |
| Email Deliverability Checklist | Phase 2 — email infrastructure |
| Quick-Reference Guide Template | Phase 3 — training |
| Troubleshooting Guide Template | Phase 4 — handoff |

---

## Definition Alignment Terms

| Term                    | Typical Definition                                                                                        |
| ----------------------- | --------------------------------------------------------------------------------------------------------- |
| Sales Engagement Platform | Software that automates multi-channel outreach sequences, tracks prospect communications, and provides engagement analytics (e.g., Outreach, Salesloft, Amplemarket) |
| Sequence                | A pre-defined series of multi-channel touchpoints (email, call, LinkedIn, manual tasks) with timed intervals between steps |
| Cadence                 | The timing pattern of a sequence — days between steps, time-of-day preferences, and total duration |
| Daily Send Limit        | Maximum number of outbound emails a single user can send per day to avoid triggering spam filters (typically 20-50/day) |
| Inbox Warm-Up           | Gradual increase of email volume from a new mailbox or domain over 2-4 weeks to build sender reputation |
| Custom Tracking Domain  | A subdomain (e.g., go.company.com) configured for link tracking to improve deliverability over shared tracking domains |
| Personalization Token   | A dynamic field placeholder (e.g., \{\{first_name\}\}, \{\{company\}\}) that auto-populates from CRM or enrichment data |
| A/B Test                | Running two variants of a sequence step (subject line, body copy, timing) to measure which performs better |
| Local Presence Dialing  | Dialer feature that displays a local area code to the prospect to increase answer rates |
| Activity Sync           | Bidirectional data flow between the sales engagement platform and CRM — activities logged in platform appear in CRM, and CRM data updates reflect in platform |

---

## Common Gotchas

- CRM sync breaks silently after API permission changes → Set up sync health alerts and check sync logs weekly during first month
- Reps exceed daily email limits during first week of rollout → Set hard send limits in platform settings, not just guidelines
- Custom tracking domain not configured before launch → Shared tracking domains hurt deliverability; always set up custom tracking domain in Phase 2
- Sequence governance not established → Without clear rules on who can create/edit sequences, teams end up with 50+ overlapping sequences within 2 months
- Inbox warm-up skipped for new domains → New mailboxes sending 50+ emails/day immediately will land in spam; enforce 2-4 week warm-up period
- Dialer call recording without consent → Recording laws vary by state/country; configure one-party vs. two-party consent settings before enabling call recording

---

## Methodology Options

| Option                     | When to Use                                                | Complexity |
| -------------------------- | ---------------------------------------------------------- | ---------- |
| Single-platform deployment | One platform for entire team, standard CRM integration     | Low        |
| Multi-platform setup       | Different platforms for SDR vs AE teams, or multiple CRMs  | High       |
| Platform migration         | Replacing existing engagement platform with new one        | Medium     |
```

---

## Phase 1: Strategy

> **Goal:** Confirm platform requirements, select the right sales engagement platform, and get stakeholder alignment on success criteria.
>
> **Output:** Validated requirements doc + platform selection + success criteria (signed off by VP Sales, RevOps, IT).

### 1a. Pre-Kickoff

> Two parallel tracks run before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                       | Format             |
| ----------------------------- | ------------------------------------------------------------- | ------------------ |
| Intro video                   | Explain what a sales engagement platform project delivers and why it matters | Video walkthrough (5-10 min) |
| Definition Alignment Document | Get stakeholder sign-off on terms (sequence, cadence, daily limits, sync) | Google Doc         |
| Pre-filled intake form        | Confirm CRM type, email provider, team size, channel priorities, current tools | Google Form or Doc |

**What we need from them:**

- Admin access to CRM with API permissions (read/write for contacts, accounts, activities, opportunities)
- Admin access to email system for OAuth connection
- List of users to be licensed, with roles (SDR, AE, Manager)
- Current sequence/cadence examples if any exist
- ICP and target segment definitions for sequence design
- Budget range and decision-making timeline

**Completion tracking:** RevOps or Sales Ops owner follows up. Do not cancel kickoff if incomplete, but push hard after.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                                  | Output                                      |
| ---- | ----------------------------------------------------------------------- | ------------------------------------------- |
| 1    | Interview 3-5 SDRs/AEs on current outreach workflow                    | Workflow documentation with pain points      |
| 2    | Pull CRM activity metrics (last 90 days) for baseline                  | Baseline metrics: emails, calls, responses, meetings |
| 3    | Document current tools and data sources                                 | Tool inventory with integration notes        |
| 4    | Quantify manual task time vs. selling time                              | Time allocation analysis                     |
| 5    | Draft gap analysis and platform comparison matrix                       | Requirements-scored vendor comparison         |

**Key context:** Sales reps spend only 30% of their time actively selling, with the remaining 70% consumed by administrative tasks, data entry, and internal meetings [1]. Research confirms reps spend roughly 2 hours per day on actual selling [2]. This baseline framing helps justify the platform investment.

**Critical:** Mark all assumptions from CRM data pulls and rep interviews as ASSUMED. The kickoff call validates.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE configuring anything.

| Term                       | Our Definition                                                              | Internally Approved? |
| -------------------------- | --------------------------------------------------------------------------- | -------------------- |
| Sequence                   | A pre-defined series of multi-channel touchpoints with timed intervals       | [ ] Yes / [ ] No     |
| Daily Send Limit           | Max emails per user per day to protect domain reputation (recommended 20-50) | [ ] Yes / [ ] No     |
| Activity Sync              | Bidirectional data flow between platform and CRM                             | [ ] Yes / [ ] No     |
| Sequence Governance        | Rules for who can create, edit, and archive sequences                        | [ ] Yes / [ ] No     |
| Success Criteria           | Specific metrics that define project success (e.g., 50% increase in daily touches) | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your sales leadership team. Check "Yes" when approved. We cannot proceed until all terms are aligned.

---

### 1b. Kickoff Call

> **Purpose:** Present gap analysis, validate requirements, and confirm platform selection approach. We walk in with work done.

#### Agenda (60 min)

| Time  | Topic                      | What Happens                                    |
| ----- | -------------------------- | ----------------------------------------------- |
| 0-15  | Present gap analysis       | "Here's what we found from rep interviews and CRM data" |
| 15-25 | Validate requirements      | Confirm must-have vs. nice-to-have features      |
| 25-35 | Definition alignment       | Review Definition Alignment Doc                  |
| 35-50 | Platform shortlist review  | Walk through comparison matrix, agree on shortlist |
| 50-60 | Next steps                 | Schedule vendor demos, assign homework            |

#### What We Bring

- Gap analysis document (current state vs. target state)
- CRM baseline metrics (emails sent, calls logged, response rates, meetings booked)
- Platform comparison matrix (scored against requirements)
- Definition Alignment Document (pre-filled with our recommendations)
- Questions list (what we need to validate)

#### What We Leave With

- Confirmed platform requirements (must-haves vs. nice-to-haves)
- Shortlist of 2-3 platforms for demos
- Confirmed definitions (or clear blockers if stakeholder sign-off needed)
- Demo schedule set
- Clear homework assignments (theirs: budget approval process, ours: schedule demos)

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Conduct vendor demos, evaluate platforms, and make final selection.

#### The Pattern

```
Kickoff Call (validate requirements)
    ↓
Schedule vendor demos (2-3 platforms)
    ↓
Demo 1: Vendor A → score against matrix
    ↓
Demo 2: Vendor B → score against matrix
    ↓
[Optional] Demo 3: Vendor C → score against matrix
    ↓
Present recommendation with ROI analysis
    ↓
Final Selection + Budget Approval → Sign-Off
```

#### Platform Evaluation Criteria

| Criterion                  | Weight | What to Assess                                              |
| -------------------------- | ------ | ----------------------------------------------------------- |
| CRM integration depth      | High   | Bidirectional sync quality, field mapping, real-time vs batch |
| Email deliverability features | High | Inbox warm-up, rotation, custom tracking domain, send limits |
| Dialer functionality        | Med    | Native vs third-party, local presence, call recording, voicemail drop |
| Sequence builder            | High   | Multi-channel steps, A/B testing, personalization tokens     |
| Analytics & reporting       | Med    | Rep dashboards, manager views, sequence performance, pipeline attribution |
| Data enrichment integrations | Med   | ZoomInfo, Clay, Apollo, Clearbit native connectors           |
| Learning curve              | Med    | Time to proficiency, admin complexity, documentation quality  |
| Cost per seat               | High   | License cost + implementation + ongoing admin effort          |

#### Platform Quick-Reference

| Platform    | CRM Strength          | Key Differentiator                        | Best For                        |
| ----------- | --------------------- | ----------------------------------------- | ------------------------------- |
| Outreach    | Salesforce (deep)     | Most mature enterprise SEP, extensive analytics | Large sales teams on Salesforce |
| Salesloft   | Salesforce + HubSpot  | 394% 3-year ROI reported [3], fast go-live | Mid-market, Salesforce/HubSpot  |
| Amplemarket | HubSpot (strong)      | AI personalization, built-in warm-up       | AI-first outbound teams         |
| Apollo      | HubSpot + Salesforce  | Built-in data + sequences, lower cost      | SMBs with prospecting needs     |
| Groove      | Salesforce (native)   | Lives inside Salesforce UI                 | Salesforce-first teams          |

**During each demo:**

1. Test specific use cases: create a sequence, enroll a prospect, check CRM sync, view reports
2. Evaluate with all key stakeholders: Sales leadership, RevOps, IT (for security review)
3. Score against comparison matrix immediately after each demo

#### Typical Timeline

| Milestone               | Timing                          |
| ----------------------- | ------------------------------- |
| Pre-kickoff prep        | 2-3 days                        |
| Kickoff call            | Day 1 of engagement             |
| Vendor demos            | 1-2 weeks                       |
| Final selection + approval | 3-5 days after last demo      |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm platform selection, budget, and success criteria before engineering begins.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by VP Sales and RevOps
- [ ] Platform selected with budget approved
- [ ] Success criteria defined and measurable (e.g., 50% increase in daily touches, 20% improvement in response rates)
- [ ] CRM admin access confirmed with proper API permissions
- [ ] Email system admin access confirmed
- [ ] User license list finalized
- [ ] Contract initiated with selected vendor
- [ ] No blockers for engineering

#### Decision Point

- **Proceed to Engineering** → Platform selected, budget approved, access confirmed
- **Hold** → Budget approval pending or stakeholder alignment needed (rare for this project type)

---

## Phase 2: Engineering

> **Goal:** Configure the complete sales engagement platform — CRM integration, email infrastructure, dialer, sequences, automations, and dashboards.
>
> **Output:** Fully configured platform tested and customer-approved.

| Project Type    | Engineering Weight | This Project                                                  |
| --------------- | ------------------ | ------------------------------------------------------------- |
| Technical-heavy | Heavy (70-80%)     | CRM integration, email infra, dialer, sequences, automations, dashboards |

### Sub-Phases

```
2a Tech Spec → 2b Engineering Handoff → 2c Build → 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate approved requirements into technical specifications for platform configuration.

**Input:** Signed-off requirements doc + platform selection from Phase 1

**What happens:**

1. Map CRM objects and fields to platform equivalents
2. Define API permission requirements (read/write for contacts, accounts, activities, opportunities)
3. Specify email infrastructure requirements (tracking domain, authentication protocols, send limits)
4. Document sequence architecture (types, cadence rules, channel mix, naming conventions)
5. Define automation rules (lead-to-sequence routing, engagement triggers, exit criteria)
6. Specify dashboard and reporting requirements

**Output:** Tech spec containing:

| Component              | Specification Details                                                  |
| ---------------------- | ---------------------------------------------------------------------- |
| CRM Integration        | OAuth connection, field mappings, sync direction, sync frequency        |
| Email Infrastructure   | Tracking domain, SPF/DKIM/DMARC, warm-up schedule, daily send limits   |
| Dialer                 | Native vs third-party, local presence, recording consent, dispositions  |
| Sequences              | Types (cold, inbound, re-engagement), step counts, timing, channel mix  |
| Automations            | Lead routing rules, status update triggers, bounce handling, alerts      |
| Dashboards             | Rep-level metrics, manager views, sequence performance, deliverability   |

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs before building.

**Who attends:** Architect + Engineer (or RevOps engineer)

**Agenda (30-45 min):**

| Time  | Topic              | What Happens                                      |
| ----- | ------------------ | ------------------------------------------------- |
| 0-15  | Walk through specs | Architect explains requirements context + tech spec       |
| 15-30 | Engineer questions | CRM API specifics, email domain setup, dialer config |
| 30-45 | Refine and approve | Adjust specs, confirm build sequence               |

**Build sequence (recommended order):**

1. CRM connection + bidirectional sync
2. Email infrastructure (tracking domain, authentication, warm-up)
3. Dialer setup (if applicable)
4. Sequence framework + core sequences
5. Workflow automations
6. Dashboards and analytics

---

### 2c. Build (Configure)

> **Purpose:** Configure all platform components per approved tech spec.

**Input:** Approved tech spec from 2b

#### Component 1: CRM Connection & Field Mappings

- [ ] Create platform account with admin/user hierarchy
- [ ] Connect to Salesforce/HubSpot via OAuth authentication
- [ ] Configure API permissions (read/write for contacts, accounts, activities, opportunities)
- [ ] Set up field mappings between platform and CRM objects
- [ ] Enable bidirectional sync for activity logging
- [ ] Test sync with 10+ sample records to verify data flow (contacts, activities, tasks)
- [ ] Document admin credentials for client handoff

#### Component 2: Email Infrastructure

- [ ] Connect email provider (Google Workspace or Microsoft 365) for each user
- [ ] Set up custom tracking domain (e.g., go.company.com) for link tracking
- [ ] Verify domain authentication: SPF, DKIM, DMARC records configured correctly
- [ ] Configure inbox warm-up schedule (if platform supports — Amplemarket, Apollo have built-in)
- [ ] Set daily send limits per user: 20-30 emails/day initially, increase gradually over 2-4 weeks [4]
- [ ] Configure inbox rotation if team needs higher volume
- [ ] Set up unsubscribe handling and compliance settings
- [ ] Test email deliverability with sample sends to seed list

**Email deliverability note:** Organizations with fully authenticated domains (SPF + DKIM + DMARC) consistently achieve 85-95% inbox placement and are 2.7x more likely to reach the inbox vs. unauthenticated senders [5]. Never skip authentication setup.

#### Component 3: Dialer & Phone Settings (if applicable)

- [ ] Configure dialer integration (native or third-party: Dialpad, Aircall, RingCentral)
- [ ] Set up local presence dialing if required (increases answer rates by 3-4x)
- [ ] Configure call recording settings (verify compliance with recording laws — one-party vs. two-party consent)
- [ ] Map call dispositions to CRM activity types (Connected, Voicemail, No Answer, Wrong Number)
- [ ] Set up voicemail drop templates (pre-recorded messages for one-click voicemail)
- [ ] Test call logging flow to CRM (verify task creation and activity association)
- [ ] Configure call analytics tracking (call duration, connect rates, dispositions)

#### Component 4: Sequence Framework & Core Sequences

- [ ] Define and document naming conventions for sequences (e.g., `[Type]-[Segment]-[Version]`)
- [ ] Establish cadence timing rules (days between steps, time-of-day windows)
- [ ] Set multi-channel step mix per sequence type
- [ ] Build cold outbound prospecting sequence (8-12 steps over 3-4 weeks: mix of email, call, LinkedIn, manual research)
- [ ] Build inbound lead follow-up sequence (5-7 steps over 2 weeks: faster cadence, phone-heavy)
- [ ] Build re-engagement/nurture sequence for stale opportunities (4-6 steps over 4-6 weeks)
- [ ] Configure personalization tokens (\{\{first_name\}\}, \{\{company\}\}, \{\{industry\}\}, \{\{title\}\})
- [ ] Set up task types for manual steps (Research, LinkedIn Connect, Video, Custom)
- [ ] Configure reply handling rules (remove on reply, move to different sequence, alert rep)
- [ ] Set up A/B testing framework for subject lines and messaging variants
- [ ] Define exit criteria and completion rules per sequence
- [ ] Configure sequence governance (who can create, edit, archive)
- [ ] Note: Use placeholder copy for sequence content — client owns messaging strategy. We configure the structure and technical framework.

#### Component 5: Workflow Automations

- [ ] Build lead-to-sequence assignment rules based on lead source, segment, and territory
- [ ] Configure automation for lead status updates based on engagement (e.g., email reply → status change)
- [ ] Set up automatic task creation for key trigger events (hot lead alert, meeting booked, demo requested)
- [ ] Build integration with data enrichment tools (Clay, ZoomInfo, Apollo) if applicable
- [ ] Configure automation for bounced email handling (hard bounce → remove from sequence, soft bounce → retry)
- [ ] Set up alerts for hot prospect engagement signals (3+ emails opened in 24 hours, link clicked, etc.)
- [ ] Test all automation workflows end-to-end with sample data

#### Component 6: Dashboards & Analytics

- [ ] Configure activity metrics to track: emails sent, emails opened, replies received, calls made, calls connected, meetings booked
- [ ] Build rep-level activity dashboard (daily touches, response rates, meetings booked, sequence progress)
- [ ] Create team/manager dashboard (aggregate metrics, rep comparisons, quota attainment)
- [ ] Set up sequence performance reporting (open rates, reply rates, click rates by sequence)
- [ ] Configure pipeline attribution to track sequence influence on deals (sequence → meeting → opportunity)
- [ ] Build email deliverability monitoring dashboard (bounce rates, spam complaints, domain health)
- [ ] Set up A/B test tracking for subject lines and templates
- [ ] Configure real-time alerts for engagement spikes
- [ ] Build best-time-to-send analysis report (if platform supports)

**Build tracking:**

- [ ] Component 1: CRM Connection & Field Mappings [status]
- [ ] Component 2: Email Infrastructure [status]
- [ ] Component 3: Dialer & Phone Settings [status]
- [ ] Component 4: Sequence Framework & Core Sequences [status]
- [ ] Component 5: Workflow Automations [status]
- [ ] Component 6: Dashboards & Analytics [status]

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify the build works and get customer approval.

**Technical testing checklist:**

| Test Area                | Test Action                                              | Pass Criteria                              |
| ------------------------ | -------------------------------------------------------- | ------------------------------------------ |
| CRM Sync                 | Enroll 10 contacts, verify sync in CRM within 5 min      | All 10 contacts synced, activities logged   |
| Email Deliverability     | Send 20 test emails to seed list                          | &gt;90% inbox placement, no spam folder        |
| Dialer                   | Make 5 test calls, verify CRM logging                     | All calls logged with correct dispositions  |
| Sequences                | Run each sequence through 3 steps with test contacts      | Steps fire on schedule, personalization works |
| Automations              | Trigger each automation rule with test data                | Lead routing, status updates, alerts all fire |
| Dashboards               | Verify all metrics populate after test activities          | Accurate counts, no data gaps               |
| A/B Testing              | Create test A/B split on one sequence                     | Both variants serving, tracking working      |
| Bounce Handling          | Send to known-bad address                                 | Auto-removed from sequence, flagged in CRM   |

**Customer testing:**

- Walk customer through each component
- Have a pilot rep run through the daily workflow: enroll prospect, execute sequence steps, manage tasks, log calls
- Verify dashboards display meaningful data
- Capture feedback, fix issues

**Engineering sign-off checkpoint:**

- [ ] All 6 components built and tested
- [ ] CRM sync verified with production data
- [ ] Email deliverability above 85% threshold
- [ ] All sequences functioning correctly
- [ ] All automations firing as expected
- [ ] Dashboards populating accurately
- [ ] Customer has tested and approved
- [ ] Ready for enablement

**Decision point:**

- **Proceed to Enablement** → All components built and tested
- **Loop back to Build** → Issues found, needs fixes

---

## Phase 3: Enablement

> **Goal:** Sales team can use the platform confidently for daily outreach. Pilot validates configuration, full training ensures adoption.
>
> **Output:** Trained team with documentation, stabilized system, no critical issues.

### Sub-Phases

```
3a Training Prep → 3b Pilot Testing → 3c Full Team Training → 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from configuration documentation and platform setup.

**Input:** Tech spec + built platform + sequence library

**Output:** Training package containing:

- Video walkthrough scripts for reps (daily workflow: adding prospects, running sequences, managing tasks, using dialer)
- Video walkthrough scripts for managers (dashboard navigation, team analytics, sequence performance)
- Video walkthrough scripts for admins (user management, sequence governance, sync monitoring, troubleshooting)
- Quick-reference guide: 1-page PDF covering the 5 daily actions a rep needs (enroll prospect, manage tasks, log calls, check replies, update CRM)
- Sequence creation SOP: how to build new sequences following governance rules
- FAQ draft: answers to common questions based on similar projects

---

### 3b. Pilot Testing

> **Purpose:** Validate configuration with a small group before full rollout.

**Pilot structure:**

- Select 3-5 pilot users (mix of SDRs and AEs, ideally including one power user and one less tech-savvy rep)
- Deliver pilot training (30-45 min, hands-on walkthrough of daily workflow)
- Run pilot for 1-2 weeks with daily monitoring

**What to monitor during pilot:**

| Metric                    | Check Frequency | Red Flag                                  |
| ------------------------- | --------------- | ----------------------------------------- |
| CRM sync accuracy         | Daily           | Any sync failures or duplicate activities  |
| Email deliverability      | Daily           | Bounce rate &gt;5% or spam complaints         |
| Rep activity volume       | Daily           | Reps not using platform (0 activities)     |
| Sequence enrollment count | Daily           | Below expected enrollment rates            |
| User feedback             | End of each week | Workflow confusion, missing features       |

**After pilot:**

- Collect structured feedback from each pilot user
- Resolve all configuration issues identified
- Refine sequences and automations based on real usage
- Validate CRM sync accuracy with production data
- Adjust daily send limits if deliverability is healthy

---

### 3c. Full Team Training Sessions

> **Purpose:** Transfer knowledge to entire sales team for daily platform usage.

**Training sessions:**

| Session  | Audience           | Focus                                                           | Duration | Format       |
| -------- | ------------------ | --------------------------------------------------------------- | -------- | ------------ |
| Session 1 | All SDRs/AEs      | Adding prospects, running sequences, managing daily tasks, using dialer | 60 min   | Live + recorded |
| Session 2 | Sales Managers     | Dashboard interpretation, team analytics, coaching with data     | 30 min   | Live + recorded |
| Session 3 | RevOps / Admins    | Platform admin, user management, sequence governance, sync health, troubleshooting | 60 min   | Live + recorded |

**Training delivery:**

1. Schedule sessions by role (do not combine rep training with admin training)
2. Use live demo in the actual platform with real sequences
3. Walk through common daily scenarios step by step
4. Distribute quick-reference guide before training starts
5. Record all sessions as video walkthroughs for future onboarding
6. Address questions in real-time, log unanswered questions for follow-up

**Key topics to cover per audience:**

**Reps:** How to add prospects to sequences, execute daily tasks (calls, emails, LinkedIn), handle replies, update CRM, view personal metrics

**Managers:** How to read team activity dashboards, identify underperforming sequences, track meetings booked vs. target, use data for 1:1 coaching

**Admins:** How to create/edit/archive sequences, manage users, monitor CRM sync health, read deliverability metrics, handle bounce management, maintain governance rules

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm the sales team can operate independently.

**Validation checkpoint:**

- [ ] Pilot testing complete (1-2 weeks) with issues resolved
- [ ] All training sessions delivered (reps, managers, admins)
- [ ] Training video walkthroughs recorded and shared
- [ ] Quick-reference guide distributed to all reps
- [ ] Sequence creation SOP delivered to admins
- [ ] No critical issues outstanding from pilot or training
- [ ] CRM sync running cleanly for 1+ week
- [ ] Email deliverability stable above 85%
- [ ] Reps executing daily workflows without constant support
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** → Team is trained, platform is stable
- **Extend Hypercare** → Adoption issues or unresolved bugs need more support time

---

## Phase 4: Handoff

> **Goal:** Clean project close with maintenance plan, troubleshooting guide, and retention/expansion path.
>
> **Output:** Customer owns the platform. Maintenance schedule documented. Internal context transferred. Project archived.

**Structure:**

```
4a Maintenance Schedule → 4b Internal Handoff → 4c External Handoff → 4d Project Close
                          (SME → Architect)     (Team → Customer)     (Archive + Debrief)
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

**Weekly Tasks (first month only):**

| Weekly Task             | What to Check                               | Red Flag Threshold                        |
| ----------------------- | ------------------------------------------- | ----------------------------------------- |
| CRM Sync Health         | Sync log for errors, failed records          | Any sync failures &gt; 24 hours unresolved   |
| Email Deliverability    | Bounce rate, spam complaints, inbox placement | Bounce rate &gt; 5% or inbox placement &lt; 85% |
| Rep Adoption            | Daily activity counts per rep                | Reps with 0 activities for 3+ consecutive days |

**Monthly Tasks:**

| Monthly Task              | What to Check                                    | Red Flag Threshold                            |
| ------------------------- | ------------------------------------------------ | --------------------------------------------- |
| Sequence Performance      | Open rates, reply rates, meeting rates by sequence | Reply rate drops &gt; 20% from baseline          |
| Email Deliverability Trend | Domain reputation, authentication status, spam rate | SPF/DKIM/DMARC failures or domain blacklisted |
| User License Audit        | Active users vs. licensed seats                   | Paying for &gt; 20% unused licenses              |
| CRM Sync Audit            | Verify bidirectional sync accuracy                | Data mismatches between platform and CRM      |

**Quarterly Tasks:**

| Quarterly Task               | What to Review                                  | Action if Off-Track                         |
| ---------------------------- | ----------------------------------------------- | ------------------------------------------- |
| Full Platform Health Review  | All integrations, automations, sequences         | Fix broken automations, update stale sequences |
| Sequence Optimization        | A/B test results, underperforming sequences      | Archive low performers, build new variants   |
| Automation Rule Audit        | Lead routing accuracy, trigger relevance          | Update rules for new segments or sources     |
| Dashboard Relevance          | Are managers using dashboards? Missing metrics?   | Add/remove metrics based on feedback         |

**After First Business Cycle (30-60 days post-launch):**

- Validate meeting booking rate vs. baseline (target: 20%+ improvement)
- Assess daily touch volume per rep vs. pre-platform baseline
- Check sequence-influenced pipeline in CRM attribution
- Review rep adoption rate (target: 80%+ reps using platform daily within 30 days)
- Key question: Are reps spending less time on admin and more time selling?

**Refinement Triggers (when to re-engage):**

| Trigger                          | Threshold                            | Response                                     |
| -------------------------------- | ------------------------------------ | -------------------------------------------- |
| Email deliverability degradation | Inbox placement &lt; 80% for 2+ weeks  | Re-engage SME for deliverability audit        |
| CRM sync failures                | &gt; 10% failed syncs for 1+ week      | Re-engage SME for integration troubleshooting |
| Rep adoption decline             | &lt; 60% reps active for 2+ weeks      | Re-engage for additional training             |
| Sequence performance drop        | Reply rates drop &gt; 30% from baseline | Re-engage for sequence optimization project   |

**Every 6-12 Months:**

- Full platform configuration review (are all features still relevant?)
- Sequence library overhaul (archive old, build new based on updated ICP)
- Evaluate platform version updates (new features, deprecated features)
- Assess whether team has outgrown current platform (scaling needs)
- Review vendor contract terms and renewal pricing

---

### 4b. Internal Handoff (SME → Architect)

> **Purpose:** Transfer context so Architect can manage the ongoing relationship.

**What the Architect needs to know:**

- Platform deployed: [Outreach / Salesloft / Amplemarket / Other]
- CRM integration type: [Salesforce / HubSpot] via [OAuth / API key]
- Email infrastructure: custom tracking domain, daily send limits, warm-up status
- Number of active users and license count
- Key stakeholders: VP Sales (executive sponsor), RevOps lead (admin), SDR Manager (day-to-day)
- Sequence governance rules: who can create/edit, naming convention
- Known quirks: any workarounds, platform limitations discovered during build

**Escalation guidelines:**

| Issue Type                                  | Who Handles                        |
| ------------------------------------------- | ---------------------------------- |
| New user onboarding, basic questions        | Architect (quick reference guide covers this) |
| Dashboard filter changes, report tweaks     | Architect                          |
| New sequence creation (following SOP)       | Architect can guide, customer executes     |
| CRM sync failures, API permission issues    | SME ("electrical work")             |
| Email deliverability problems               | SME                                 |
| Platform migration or major reconfiguration | SME                                 |

**For Dedicated engagements:** Architect receives the maintenance schedule (4a) and becomes responsible for executing monthly/quarterly checks. SME walks Architect through each maintenance task during handoff.

---

### 4c. External Handoff (Team → Customer)

> **Purpose:** Formal project completion with customer.

**Final project meeting agenda:**

1. Walk through all configured components (CRM integration, email infra, sequences, automations, dashboards)
2. Review documentation package
3. Walk through maintenance schedule (monthly + quarterly tasks)
4. Review troubleshooting guide for common issues
5. Confirm admin credentials transferred
6. Answer final questions
7. Schedule 30-day optimization check-in
8. State explicitly: "Project complete"

**Documentation package:**

- Platform configuration documentation (all settings, field mappings, API permissions)
- Sequence library (all sequences with structure, timing, channel mix)
- Sequence governance SOP (who can create/edit/archive, naming conventions)
- Quick-reference guide for reps (daily workflow)
- Dashboard guide for managers
- Admin guide (user management, sync monitoring, troubleshooting)
- All training video walkthrough recordings
- Definition Alignment Document (final version)
- Maintenance Schedule
- Troubleshooting guide (see below)
- Vendor support resources and escalation paths

**Troubleshooting Guide:**

| Scenario                              | Symptoms                                        | Resolution                                              |
| ------------------------------------- | ----------------------------------------------- | ------------------------------------------------------- |
| CRM sync breaks                       | Activities not appearing in CRM, sync error logs | Check OAuth token expiration, re-authenticate, verify API permissions |
| Email deliverability drops            | Low open rates, emails in spam folders           | Check SPF/DKIM/DMARC records, reduce daily send volume, pause warm-up and restart |
| Emails bouncing at high rate          | &gt; 5% bounce rate, hard bounces increasing        | Audit email list quality, remove invalid addresses, check domain reputation on blacklists |
| Sequence steps not firing             | Prospects stuck in sequence, no emails sent      | Check send window settings, verify email connection, check daily limit not reached |
| Reps not seeing tasks                 | Empty task queue despite active sequences        | Check timezone settings, verify sequence enrollment, check filter settings |
| Dialer not logging calls              | Calls made but not appearing in CRM              | Verify dialer integration credentials, check call disposition mapping, test with sample call |
| Automation rules not triggering       | Leads not being routed to sequences              | Check trigger criteria, verify lead field values match rule conditions |
| Data enrichment not populating        | Missing contact data despite integration          | Verify API key for enrichment tool, check credit balance, test with known contact |
| Dashboard showing incorrect numbers   | Metrics don't match expected activity counts     | Check date range filters, verify activity sync delay, clear cache and refresh |
| Platform running slowly               | Long load times, timeout errors                  | Check browser extensions, clear cache, verify internet connection, contact vendor support |

**For Single Project engagements:** Walk the customer through the maintenance schedule in detail. Record a video walkthrough of the walkthrough. Ensure RevOps admin understands each monthly and quarterly task.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location
- [ ] Configuration documentation complete
- [ ] Handoff documentation delivered to customer
- [ ] Admin credentials transferred
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized

#### Internal Debrief

- What went well? (Platform selection process, build quality, training effectiveness)
- What would we do differently? (Timeline, scope, stakeholder engagement)
- Any learnings to feed back into SOPs? (New platform quirks, better sequence patterns)

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell → Downsell → Retry    |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (ongoing sequence optimization + deliverability monitoring)
   ↓ if no
2. Downsell: Adjacent project (Activity Capture, Conversation Intelligence, Automated Outbound Process)
   ↓ if yes
3. Retry retainer at end of next project cycle
```

**Script:**

> "Now that the sales engagement platform is configured and your team is trained, there are two ways we can continue working together. Option 1: We can set you up on managed services where we handle ongoing sequence optimization, deliverability monitoring, and platform health management. Option 2: If there's another specific project you need help with — like Activity Capture to auto-log all rep communications, or Conversation Intelligence to analyze calls — we can scope that out. Which sounds more interesting?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On [date ~1 quarter out], we'll review platform performance, sequence effectiveness, and see if any adjustments are needed."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                                |
| ------------------- | ----------------------------------------------------------- |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks             |
| 2. Review metrics   | Pull sequence performance, deliverability trends, adoption rates |
| 3. Decide ownership | Can Architect handle this check-in, or need SME?            |
| 4. Prep materials   | If SME needed, brief them. If Architect, prep talking points. |

**At the refinement check-in:**

- Review sequence performance against original success criteria
- Assess email deliverability trends
- Identify any new sequence types needed (new segments, new campaigns)
- If minor: Architect handles tweaks (new sequence from template, user additions)
- If major: Scope new project (platform migration, ABM sequence design, data enrichment integration)

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- Requirements Document (must-have vs. nice-to-have features, scored)
- Platform Comparison Matrix (vendor scores against requirements)
- Platform Selection Recommendation (with ROI analysis)
- Definition Alignment Document (signed off by stakeholders)

**Technical Deliverables:**

- Configured sales engagement platform with:
  - CRM bidirectional sync (Salesforce or HubSpot)
  - Email infrastructure (custom tracking domain, SPF/DKIM/DMARC, warm-up, send limits)
  - Dialer setup (if applicable — local presence, recording, voicemail drop)
  - 3-5 core sequences (cold outbound, inbound follow-up, re-engagement)
  - Workflow automations (lead routing, status updates, engagement alerts)
  - Dashboards and analytics (rep-level, manager-level, sequence performance, deliverability)

**Documentation Package:**

- Platform configuration documentation
- Sequence library with governance SOP
- Quick-reference guide for reps
- Dashboard guide for managers
- Admin guide (user management, sync monitoring, troubleshooting)
- Training video walkthrough recordings (reps, managers, admins)
- Troubleshooting guide
- Maintenance schedule
- Definition Alignment Document (final version)

---

## Appendix

### Roles

| Role | What They Do |
|---|---|
| **Architect** | Owns the customer relationship, leads strategy, creates specs, does enablement, owns account post-delivery |
| **Engineer** | CRM build, automation, dashboards (Phase 2) |
| **SME** | Project/implementation team brought in for project-specific work |

---

## References

[1] [Salesforce - Sales Reps Spend Less Than 30% of Time Actually Selling](https://www.salesforce.com/news/stories/sales-research-2023/)

[2] [HubSpot 2024 Sales Trends Report](https://www.hubspot.com/hubfs/HubSpots%202024%20Sales%20Trends%20Report.pdf)

[3] [Salesloft vs. Outreach 2025 Comparison (Salesloft)](https://www.salesloft.com/salesloft-vs-outreach)

[4] [Amplemarket Email Deliverability Guide 2026](https://www.amplemarket.com/blog/email-deliverability-guide-2026)

[5] [SalesHive - DKIM, DMARC, SPF Best Practices for Email Security and Deliverability](https://saleshive.com/blog/dkim-dmarc-spf-best-practices-email-security-deliverability/)
