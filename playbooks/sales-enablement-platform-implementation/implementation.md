# Sales Enablement Platform Implementation — Implementation

## Project One-Pager

### Sales Enablement Platform Implementation One-Pager

#### Project Type

- Category: Balanced
- Primary Deliverable: Fully configured sales enablement platform (Seismic, Highspot, Mindtickle, or Showpad) with CRM integration, content taxonomy, learning paths, analytics dashboards, and governance model — ready for sales team adoption

##### Phase Relevance

| Phase          | Applies? | Weight | Notes                                                        |
| -------------- | -------- | ------ | ------------------------------------------------------------ |
| 1. Strategy    | Yes      | Medium | Content audit, stakeholder interviews, platform evaluation, taxonomy design. 3-4 refinement loops. |
| 2. Engineering | Yes      | Heavy  | Platform configuration, content migration, CRM integration, analytics setup, learning path builds. |
| 3. Enablement  | Yes      | Heavy  | Champion enablement, full team training, phased rollout, adoption monitoring.                      |
| 4. Handoff     | Yes      | Medium | Governance model handoff, admin training, adoption review, ongoing support transition.             |

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────>│ 2. ENGINEER  │────>│3. ENABLEMENT │────>│  4. HANDOFF  │
  │    Medium    │     │    Heavy     │     │    Heavy     │     │    Medium    │
  │ 1a>1b>1c>1d │     │ 2a>2b>2c>2d │     │ 3a>3b>3c>3d │     │ 4a>4b>4c>4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   Content audit &      Platform config,     Champion program,    Governance model,
   platform selection   CRM integration,     team training,       admin handoff,
                        content migration    phased rollout       adoption review
```

**This project's flow:**
- Full 4-phase. Medium strategy (content audit + platform selection drive alignment), heavy engineering (platform config + CRM integration + content migration), heavy enablement (adoption is the make-or-break), medium handoff (governance + admin ownership transfer).
- No phases skipped. Some customers compress Phase 1 if platform is already selected. Phase 3 is critical — 65% of sales reps report they cannot find content to share with buyers [1], so adoption work determines whether the platform delivers value or becomes shelfware.

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Watch intro video explaining the sales enablement platform project scope and what "good" looks like
- [ ] Complete content audit intake form (list all content repositories, owners, and estimated asset counts)
- [ ] Provide CRM admin access credentials or confirm IT support availability
- [ ] Identify 2-3 sales champion nominees from leadership
- [ ] Confirm executive sponsor and budget sign-off timeline

##### Track B: Architect Prep
- [ ] Pull current CRM configuration (fields, objects, opportunity stages)
- [ ] Research customer's industry vertical for content benchmarks
- [ ] Draft preliminary content taxonomy based on sales stages from CRM data
- [ ] Create v0 platform requirements scorecard from intake form data
- [ ] Prepare stakeholder interview guide customized to customer's tech stack

#### Refinement Loop (1b > 1c > 1d)

| Meeting        | Sub-Phase | Focus                                           | Stakeholder                         | Output                          |
| -------------- | --------- | ----------------------------------------------- | ----------------------------------- | ------------------------------- |
| Kickoff        | 1b        | Present content audit findings, validate pain points, review platform requirements | VP Sales, RevOps, Sales Enablement  | Info for requirements scorecard v1 |
| Refinement 1   | 1c        | Review platform evaluation results, compare vendor demos, finalize selection | VP Sales, IT, RevOps                | Platform selection decision     |
| Refinement 2   | 1c        | Finalize content taxonomy, map content to sales stages, approve migration scope | Sales Enablement, Marketing, RevOps | Content migration plan v2       |
| Sign-Off       | 1d        | Strategic approval of platform, taxonomy, migration plan, and rollout timeline | All stakeholders                    | Final strategic package         |

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held
- [ ] 1c. Refinement loop complete (platform selected, taxonomy finalized, migration plan approved)
- [ ] 1d. Strategic sign-off obtained

##### Phase 2: Engineering
- [ ] 2a. Tech spec created (platform config + CRM integration + content migration plan)
- [ ] 2b. Engineering handoff meeting held
- [ ] 2c. Build complete (platform configured, content migrated, CRM integrated, analytics live)
- [ ] 2d. QA/Test + customer sign-off

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped (champion guide, team training deck, quick-reference cards)
- [ ] 3b. Training sessions delivered (champions first, then full team)
- [ ] 3c. Hypercare period complete (2-week monitored adoption period)
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff (SME to Architect) complete
- [ ] 4c. External handoff to Customer complete
- [ ] 4d. Project closed and archived

#### Document Types

##### Working Documents (iterate together)

| Document                       | Purpose                                       | When Complete                                 |
| ------------------------------ | --------------------------------------------- | --------------------------------------------- |
| Content audit spreadsheet      | Inventory all existing sales content with metadata | All repositories cataloged, content scored for freshness |
| Platform requirements scorecard | Weighted evaluation criteria for vendor comparison | All must-haves and nice-to-haves scored        |
| Content taxonomy design        | Folder structure, tags, and categories for platform | Taxonomy mapped to sales stages and buyer personas |
| Content migration checklist    | Track what moves, what gets archived, what's missing | All priority content status tracked             |

##### Deliverables (polished outputs)

| Deliverable                        | Created From                        | Customer Uses For                      |
| ---------------------------------- | ----------------------------------- | -------------------------------------- |
| Platform evaluation summary        | Requirements scorecard + vendor demos | Executive approval and budget sign-off |
| Content mapping matrix             | Content audit + taxonomy design      | Visual guide for content organization  |
| Implementation timeline            | All working documents                | Internal stakeholder alignment         |
| Content governance playbook        | Taxonomy design + migration lessons  | Ongoing platform management            |

#### Enablement Details

##### Training Types

| Type        | Audience                              | Focus                                          | Duration |
| ----------- | ------------------------------------- | ---------------------------------------------- | -------- |
| Champion    | 2-3 selected sales reps              | Advanced platform features, peer advocacy role | 60m      |
| Leadership  | VP Sales, Sales Managers              | Analytics dashboards, adoption metrics, coaching views | 30m      |
| Sales Team  | All sales reps                        | Content search, sharing with prospects, CRM integration workflow | 45m      |
| Admin/Ops   | RevOps, Sales Ops, Platform Admin     | User management, content upload, taxonomy changes, reporting | 60m      |
| Marketing   | Content creators, Product Marketing   | Content publishing workflow, analytics feedback loop | 30m      |

##### Hypercare
- Applies: Yes
- Duration: 2 weeks
- Office Hours: Yes — daily 15-min standup during week 1, weekly 30-min slot during week 2

##### Training Assets to Create
- [ ] Video walkthrough: Platform overview (5-10 min)
- [ ] Video walkthrough: Content search and sharing workflow (3-5 min)
- [ ] Video walkthrough: CRM integration usage for reps (3-5 min)
- [ ] Video walkthrough: Analytics dashboard interpretation for managers (5 min)
- [ ] Doc: Quick-reference card with screenshots of top 5 workflows
- [ ] Doc: Content governance guide (ownership, review cycles, archival)
- [ ] Doc: Admin runbook for platform operations

#### Handoff & Retention

##### Internal Handoff (SME to Architect)
- Key context for Architect: Platform vendor relationship, content taxonomy logic, CRM integration architecture, known limitations
- Escalation trigger: Any taxonomy restructuring, CRM integration changes, or platform tier/license changes

##### External Handoff (to Customer)
- Final meeting agenda: Adoption metrics review, governance walkthrough, outstanding items, Q&A
- Documentation package: All training video recordings, governance guide, admin runbook, content mapping matrix, FAQ

##### Maintenance Schedule
- Monthly: Content freshness audit, adoption metrics review, new content publishing
- Quarterly: Taxonomy review, governance compliance check, platform feature updates
- Who owns: Single Project = customer owns | Dedicated = Architect owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services (ongoing content optimization + adoption coaching) -> if no -> Downsell: Content refresh project or advanced analytics buildout -> Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~90 days post-launch
- Internal prep trigger: 2 weeks before
- Decision: Architect handles content/taxonomy tweaks / SME needed for platform reconfiguration or new integrations

#### Key Assets

| Asset                          | When Used          |
| ------------------------------ | ------------------ |
| Content audit template         | Phase 1a (Track B) |
| Platform requirements scorecard | Phase 1b-1c        |
| Content taxonomy template      | Phase 1c-2a        |
| CRM integration checklist      | Phase 2c           |
| Training deck template         | Phase 3a           |
| Governance playbook template   | Phase 4a           |

#### Definition Alignment Terms

| Term                    | Typical Definition                                                                                    |
| ----------------------- | ----------------------------------------------------------------------------------------------------- |
| Sales Enablement        | The process of providing sales teams with the content, tools, training, and information they need to engage buyers effectively |
| Content Taxonomy        | The hierarchical organization of content by type, sales stage, persona, and use case within the platform |
| Content Governance      | Policies for content ownership, review cadence, freshness standards, and archival rules                |
| Digital Sales Room      | A shared online space where sellers curate and share content with specific prospects                   |
| Content Engagement      | Prospect-side tracking of opens, views, time spent, and page-level interaction with shared content    |
| Learning Path           | A structured sequence of training modules, quizzes, and certifications within the enablement platform |
| Content Effectiveness   | The correlation between content usage patterns and deal outcomes (win rate, velocity)                  |
| Platform Adoption Rate  | Percentage of licensed users actively logging in and using the platform within a defined time period   |

#### Common Gotchas
- Migrating all content without cleanup creates a cluttered platform that replicates existing chaos -> Enforce content freshness filter: only migrate content updated within last 12 months or explicitly approved by owner
- Sales reps reverting to old habits (email attachments, Google Drive links) -> Restrict old sharing paths where possible; make the platform the path of least resistance within CRM
- Over-engineering taxonomy on day one -> Start simple (sales stage + content type), iterate based on actual search patterns after 30-60 days of usage data
- CRM integration configured but not tested end-to-end -> Run a full content-sharing workflow from CRM record to prospect view before launch
- Content owners not assigned at setup -> Platform decays within 6 months; assign owners per category before going live
- Skipping champion program -> Peer adoption influence is 3-4x more effective than top-down mandates; always recruit 2-3 champions

#### Methodology Options

| Option                         | When to Use                                  | Complexity |
| ------------------------------ | -------------------------------------------- | ---------- |
| Content-first (no learning paths) | Smaller teams (&lt;30 reps) focused on content discovery only | Low        |
| Content + Learning Paths       | Teams with active onboarding pipeline or skills gaps | Medium     |
| Full Enablement Suite          | Orgs wanting content, training, coaching, and analytics | High       |

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on platform selection, content taxonomy, content migration scope, and rollout plan.
>
> **Output:** Platform Selection Decision + Content Taxonomy Design + Migration Plan + Rollout Timeline (signed off by stakeholders).

### 1a. Pre-Kickoff

> Two parallel tracks run after the deal closes and before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                       | Format             |
| ----------------------------- | ------------------------------------------------------------- | ------------------ |
| Intro video                   | Explain what a sales enablement platform project involves and what success looks like | Video (5-10 min)    |
| Content audit intake form     | Capture all content repositories, owners, estimated asset counts, and known pain points | Online Form        |
| Definition Alignment Document | Get stakeholder sign-off on key terms (content taxonomy, governance, adoption metrics) | Document           |
| Champion nomination form      | Identify 2-3 sales reps to serve as platform champions        | Email / Form       |

**Why this matters:** Sales reps spend an average of 10 hours per week searching for content when no enablement platform exists [2]. The intake form captures the scattered landscape so we arrive at kickoff with a clear picture of the problem.

**Completion tracking:** RevOps or Sales Enablement lead follows up. Do not cancel kickoff if incomplete, but push hard — the content audit intake form is critical for a productive first meeting.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                        | Output                            |
| ---- | ------------------------------------------------------------- | --------------------------------- |
| 1    | Review intake form responses and CRM opportunity stage config | Raw data collected                |
| 2    | Build v0 content audit with intake data                       | v0 content audit with gaps identified |
| 3    | Draft preliminary content taxonomy based on sales stages      | Recommended folder/tag structure  |
| 4    | Research platform options based on team size, budget, CRM     | Platform shortlist (2-3 vendors)  |
| 5    | Prepare platform requirements scorecard (weighted)            | Evaluation framework ready        |

**Critical:** Mark all taxonomy recommendations and platform assumptions as ASSUMED. The kickoff call validates.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building anything.

| Term                  | Our Definition                                                                                     | Internally Approved? |
| --------------------- | -------------------------------------------------------------------------------------------------- | -------------------- |
| Content Taxonomy      | The hierarchical folder, tag, and category structure that organizes content by type, stage, persona | [ ] Yes / [ ] No     |
| Content Governance    | Policies defining who owns content, review frequency, freshness thresholds, and archival rules      | [ ] Yes / [ ] No     |
| Adoption Rate         | Percentage of licensed users who log in and perform at least one search or share action per week    | [ ] Yes / [ ] No     |
| Content Effectiveness | Correlation between content usage and deal outcomes, measured by win rate delta on content-shared deals | [ ] Yes / [ ] No     |
| Digital Sales Room    | A shared online workspace where sellers curate specific content packages for individual prospects   | [ ] Yes / [ ] No     |
| Learning Path         | A structured onboarding or skills curriculum with sequenced modules, quizzes, and certification     | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your sales leadership and marketing team. Check "Yes" when approved. We cannot proceed with platform configuration until all terms are aligned — misaligned definitions cause taxonomy rework and adoption confusion.

---

### 1b. Kickoff Call

> **Purpose:** Present v0 content audit findings and validate pain points. Walk in with platform requirements framework — customer reacts, not creates from scratch.

#### Agenda (60-90 min)

| Time  | Topic                        | What Happens                                                       |
| ----- | ---------------------------- | ------------------------------------------------------------------ |
| 0-15  | Walk through v0 content audit | "Here's what we found across your content repositories"            |
| 15-30 | Validate pain points         | Confirm time-to-find, content gaps, scattered repositories. ASSUMED -> CONFIRMED or corrected |
| 30-45 | Review platform requirements | Walk through weighted scorecard, adjust priorities                  |
| 45-55 | Definition alignment         | Review Definition Alignment Document                               |
| 55-70 | Platform shortlist           | Present 2-3 vendor options, discuss evaluation approach             |
| 70-80 | Champion nominations         | Confirm 2-3 reps, discuss rollout timeline                         |
| 80-90 | Next steps                   | Schedule vendor demos, assign homework                             |

#### What We Bring

- v0 content audit with gap analysis (built in Track B prep)
- Draft platform requirements scorecard (weighted)
- Platform vendor shortlist with initial fit assessment
- Definition Alignment Document (pre-filled with our recommendations)
- Stakeholder interview guide (if interviews still needed)

#### What We Leave With

- Validated pain points and content gaps (ASSUMED -> CONFIRMED)
- Adjusted requirements scorecard weights
- Confirmed platform vendor demo schedule
- Champion nominees confirmed
- Clear homework assignments (theirs: CRM access, IT security review; ours: vendor demo coordination)

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Iterate on platform selection, taxonomy design, and migration scope until sign-off.

#### The Pattern

```
Kickoff Call (validate pain, set requirements)
    |
Vendor demos + scoring -> Platform recommendation
    |
Meeting 2 (present evaluation, select platform)
    |
Taxonomy design + content mapping -> Migration plan
    |
Meeting 3 (present taxonomy, approve migration scope)
    |
Final Review -> Sign-off
```

#### Before Each Meeting

1. Process previous meeting notes and feedback
2. Update relevant working documents (scorecard, taxonomy, migration plan)
3. Prepare questions for next validation round

#### During Each Meeting

1. Walk through current version of the working document
2. Capture corrections and refinements
3. Validate what is now CONFIRMED
4. Identify remaining ASSUMED items

#### After Each Meeting

1. Update all working documents
2. Track what moved from ASSUMED -> CONFIRMED
3. Coordinate next steps (vendor demos, IT security review, content owner assignments)

#### Meeting Schedule

| Meeting Type           | Focus                                              | Stakeholder                        |
| ---------------------- | -------------------------------------------------- | ---------------------------------- |
| Kickoff                | Content audit findings, requirements, pain points  | VP Sales, RevOps, Sales Enablement |
| Platform Evaluation    | Vendor comparison, selection decision, budget       | VP Sales, IT, RevOps, Finance      |
| Taxonomy & Migration   | Content organization, migration scope, CRM integration plan | Sales Enablement, Marketing, RevOps |
| Final Review           | Full strategic package walkthrough, sign-off        | All stakeholders                   |

#### Typical Timeline

| Milestone                 | Timing                                           |
| ------------------------- | ------------------------------------------------ |
| Pre-kickoff prep          | 3-5 days                                         |
| Kickoff call              | Day 1 of engagement                              |
| Vendor demos              | 1-2 weeks after kickoff                          |
| Platform selection        | Week 2-3                                         |
| Taxonomy & migration plan | Week 3-4                                         |
| Final review + sign-off   | Week 4-5 (when all inputs CONFIRMED)             |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm all strategic decisions before proceeding to platform build.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by stakeholders
- [ ] Platform selected and contract initiated
- [ ] Content taxonomy design approved (folder structure, tags, categories)
- [ ] Content migration scope confirmed (what migrates, what gets archived, what's missing)
- [ ] CRM integration requirements documented (Salesforce or HubSpot, objects, sync rules)
- [ ] Learning path scope agreed (if applicable)
- [ ] Rollout timeline confirmed (champion pilot -> full team -> adoption monitoring)
- [ ] All critical inputs CONFIRMED (vs ASSUMED)
- [ ] No blockers for engineering (vendor access, CRM admin credentials, SSO config details)

#### Decision Point

- **Proceed to Engineering** -> Customer wants platform built and configured (standard path)
- This project does NOT have a natural exit after Phase 1. The strategic deliverable (platform selection + taxonomy) has no value without the build and rollout.

---

## Phase 2: Engineering

> **Goal:** Configure the sales enablement platform, migrate content, integrate CRM, set up analytics, and build learning paths.
>
> **Output:** Fully configured platform with content loaded, CRM integrated, analytics dashboards live, and learning paths active — tested and customer-approved.

| Project Type    | Engineering Weight | Context                                                       |
| --------------- | ------------------ | ------------------------------------------------------------- |
| This project    | Heavy (50-60%)     | Platform config + content migration + CRM integration + analytics + learning paths |

### Sub-Phases

```
2a Tech Spec -> 2b Engineering Handoff -> 2c Build -> 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate strategic package into technical specifications for platform configuration.

**Input:** Signed-off strategic package from Phase 1 (platform choice, taxonomy, migration plan, CRM integration requirements)

**What happens:**

1. Architect translates taxonomy design into platform-specific folder and tag configuration
2. Content migration plan becomes a sequenced upload checklist with metadata requirements
3. CRM integration requirements become API connection specs and field mapping documents
4. Analytics requirements become dashboard configuration specs

**Output:** Draft tech spec containing:

- Platform configuration spec (taxonomy structure, user roles, permissions, SSO)
- Content migration spec (upload sequence, metadata template, freshness cutoff rules)
- CRM integration spec (connection method, object mapping, activity logging, widget/sidebar config)
- Analytics dashboard spec (content usage, engagement tracking, adoption metrics, effectiveness reports)
- Learning path spec (modules, sequencing, quizzes, certification milestones) — if in scope
- Build sequence (what to configure first: taxonomy -> content -> CRM -> analytics -> learning)

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs with engineer before building.

**Who attends:** Architect + Engineer (or platform admin/configurator)

**Agenda (45-60 min):**

| Time  | Topic                        | What Happens                                           |
| ----- | ---------------------------- | ------------------------------------------------------ |
| 0-15  | Walk through platform config | Taxonomy, roles, permissions, SSO requirements         |
| 15-30 | Content migration plan       | Upload sequence, metadata, freshness rules, priority list |
| 30-45 | CRM integration spec         | API connection, field mapping, activity logging        |
| 45-60 | Analytics + learning paths   | Dashboard specs, learning path modules                 |

**What Architect brings:**

- Strategic package (for context on why decisions were made)
- Draft tech spec (from 2a)
- Platform vendor documentation links
- Known limitations or gotchas from vendor evaluation

**What engineer leaves with:**

- Approved tech spec with build sequence
- Platform admin credentials
- CRM sandbox access (if applicable)
- Vendor support contact for configuration questions

---

### 2c. Build (Configure)

> **Purpose:** Configure the enablement platform, migrate content, connect CRM, and set up analytics.

**Input:** Approved tech spec from 2b

**The build sequence:**

#### Stage 1: Platform Foundation (Days 1-3)

| Component                  | What to Configure                                                | Validation                            |
| -------------------------- | ---------------------------------------------------------------- | ------------------------------------- |
| Taxonomy and folder structure | Create folders aligned to sales stages (Discovery, Demo, Proposal, Negotiation, Close) | Folder hierarchy matches approved taxonomy |
| Tagging system             | Configure tags: content type, persona, industry, product line, competitor | Tags are searchable and filterable     |
| User roles and permissions | Set up admin, content owner, sales rep, and manager roles        | Test access levels per role            |
| SSO/SAML integration       | Connect to identity provider (Okta, Azure AD, Google Workspace)  | Users can log in via SSO               |

#### Stage 2: Content Migration (Days 3-7)

| Component                     | What to Configure                                                  | Validation                              |
| ----------------------------- | ------------------------------------------------------------------ | --------------------------------------- |
| Priority content upload       | Upload top 50-100 assets with full metadata (tags, descriptions, stage mapping) | Content searchable by stage, persona, type |
| Content freshness enforcement | Only migrate content updated within last 12 months or explicitly approved | No stale content in initial load         |
| Content collections           | Build stage-based collections (Discovery Prep, Demo Follow-Up, Proposal Package) | Collections render correctly, content is relevant |
| Persona-based collections     | Create buyer persona collections (Champion, Economic Buyer, Technical Evaluator) | Persona-appropriate content in each      |
| Competitive battle cards      | Organize competitive content by competitor                         | Battle cards accessible by competitor name |
| Expiration and review dates   | Configure content expiration alerts and review reminders           | Alerts fire at correct intervals         |

#### Stage 3: CRM Integration (Days 7-10)

| Component                     | What to Configure                                                  | Validation                               |
| ----------------------------- | ------------------------------------------------------------------ | ---------------------------------------- |
| CRM connection                | Connect to Salesforce or HubSpot via OAuth/API                     | Authentication successful, sync active    |
| Object linking                | Configure which CRM objects link to content (Account, Opportunity, Contact) | Content accessible from correct records   |
| Content sharing tracking      | Enable logging when reps share content with prospects              | Share events appear on CRM activity timeline |
| Engagement tracking           | Configure prospect-side tracking (opens, views, time spent)        | Engagement data flows back to CRM and platform |
| In-CRM widget/sidebar         | Configure content access panel within CRM interface                | Reps can search and share without leaving CRM |

#### Stage 4: Analytics & Dashboards (Days 10-12)

| Component                     | What to Configure                                                  | Validation                               |
| ----------------------------- | ------------------------------------------------------------------ | ---------------------------------------- |
| Content usage dashboard       | Views, shares, downloads by asset                                  | Data populates correctly                  |
| Engagement tracking dashboard | Prospect opens, time spent, page views                             | Engagement events tracked accurately      |
| Adoption dashboard            | Platform logins, active users, search patterns                     | User activity data matches expected        |
| Content effectiveness report  | Correlate content usage with deal outcomes                         | Report shows content-to-win-rate correlation |
| Manager view                  | Team content usage and coaching insights                           | Managers see their team's activity         |
| Automated report distribution | Weekly/monthly reports to stakeholders                             | Reports arrive on schedule                 |

#### Stage 5: Learning Paths (Days 12-15, if in scope)

| Component                     | What to Configure                                                  | Validation                               |
| ----------------------------- | ------------------------------------------------------------------ | ---------------------------------------- |
| Onboarding curriculum         | Modules: company overview, product training, sales process, tools  | Modules sequenced correctly               |
| Knowledge checks              | Quizzes at module completion points                                | Quizzes score and record correctly         |
| Certification milestones      | Onboarding completion certification                                | Cert issued when all modules complete      |
| Ongoing training paths        | Product updates, competitive training, skill-based paths           | Paths assignable by role/tenure            |
| Manager notifications         | Alerts for completion and non-completion                           | Notifications fire at correct triggers     |

**Build tracking:**

- [ ] Stage 1: Platform foundation configured
- [ ] Stage 2: Content migration complete
- [ ] Stage 3: CRM integration live
- [ ] Stage 4: Analytics dashboards configured
- [ ] Stage 5: Learning paths built (if in scope)

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify the entire platform works end-to-end and get customer approval.

**Two types of testing:**

| Type              | Who      | Purpose                                                |
| ----------------- | -------- | ------------------------------------------------------ |
| Technical Testing | Our team | Verify platform config, CRM sync, analytics accuracy   |
| Customer Testing  | Customer | Verify content is organized correctly, workflows match expectations |

**Technical testing checklist:**

- [ ] Content search returns relevant results by stage, persona, type, and competitor
- [ ] Content sharing from CRM records works end-to-end (share -> prospect receives -> engagement tracked)
- [ ] CRM activity logging captures shares, views, and engagement correctly
- [ ] SSO login works for all user roles
- [ ] Analytics dashboards display accurate data (cross-reference with manual verification)
- [ ] Content expiration alerts fire correctly
- [ ] Learning path modules sequence and score correctly
- [ ] Manager views show team activity accurately
- [ ] Mobile experience renders correctly (if applicable)
- [ ] Automated reports generate and distribute on schedule

**Customer testing:**

- Walk customer through 3 realistic scenarios: searching for content, sharing with prospect, reviewing analytics
- Have 2-3 reps test the CRM integration in their actual workflow
- Content owners verify taxonomy makes sense and content is tagged correctly
- Managers confirm dashboard views show what they need

**Engineering sign-off checkpoint:**

- [ ] All technical tests passing
- [ ] Customer has tested and approved core workflows
- [ ] CRM integration verified with real data
- [ ] Analytics data accuracy confirmed
- [ ] Ready for enablement and rollout

**Decision point:**

- **Proceed to Enablement** -> Platform is configured and tested, ready for team rollout
- **Loop back to Build** -> Issues found, needs fixes before rollout

---

## Phase 3: Enablement

> **Goal:** Sales team can find, use, and share content through the platform. Champions are trained, full team is onboarded, and adoption is actively monitored.
>
> **Output:** Trained team with documentation, adoption metrics tracked, no critical issues.

Organizations with sales enablement strategies achieve 49% higher win rates on forecasted deals [3]. The enablement phase determines whether this project delivers that value or becomes unused software.

### Sub-Phases

```
3a Training Prep -> 3b Training Sessions -> 3c Hypercare -> 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from strategic and technical documentation.

**Input:** Strategic package + tech specs + configured platform

**Output:** Training package containing:

- **Champion training guide** — Advanced features, peer advocacy talking points, feedback collection role
- **Sales team training deck** — Content search, sharing with prospects, CRM integration, engagement tracking
- **Manager training deck** — Analytics dashboards, team activity views, coaching insights
- **Admin training guide** — User management, content upload, taxonomy changes, reporting
- **Quick-reference card** — Top 5 workflows with screenshots (print-friendly, one page)
- **FAQ draft** — Based on common questions from similar implementations (content search tips, CRM integration issues, mobile access)

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to customer team, starting with champions.

**Training sequence matters.** Champions train first (1 week before full rollout), then lead peer adoption during full team training.

**Session 1: Champion Training (Week -1)**

| Topic                          | Duration | What Happens                                                |
| ------------------------------ | -------- | ----------------------------------------------------------- |
| Advanced platform walkthrough  | 30m      | Deep dive on search, collections, sharing, and analytics    |
| Peer advocacy role             | 15m      | How to help teammates, what feedback to collect             |
| Feedback collection            | 15m      | Champion program setup, weekly feedback cadence             |

**Session 2: Sales Team Training (Rollout Day)**

| Topic                          | Duration | What Happens                                                |
| ------------------------------ | -------- | ----------------------------------------------------------- |
| Platform overview              | 10m      | What the platform is, why we're using it, what's in it      |
| Content search and discovery   | 10m      | Finding content by stage, persona, competitor, keyword       |
| Sharing with prospects         | 10m      | Share flow from CRM, tracking engagement, digital sales rooms |
| CRM integration                | 5m       | Accessing content without leaving Salesforce/HubSpot         |
| Learning paths (if applicable) | 5m       | Onboarding curriculum, certifications                        |
| Q&A                            | 5m       | Address questions, champion introductions                    |

**Session 3: Leadership/Manager Training**

| Topic                          | Duration | What Happens                                                |
| ------------------------------ | -------- | ----------------------------------------------------------- |
| Adoption dashboards            | 10m      | Who's logging in, who's using content, search patterns       |
| Content effectiveness          | 10m      | Which content correlates with wins, what's underperforming   |
| Coaching views                 | 10m      | Team activity, individual rep usage, areas for improvement   |

**Session 4: Admin/Ops Training**

| Topic                          | Duration | What Happens                                                |
| ------------------------------ | -------- | ----------------------------------------------------------- |
| User management                | 15m      | Adding/removing users, role assignment, permission changes   |
| Content publishing             | 15m      | Upload workflow, metadata requirements, expiration settings  |
| Taxonomy management            | 15m      | Adding tags, creating collections, adjusting folder structure |
| Reporting and exports          | 15m      | Running reports, scheduling distributions, data exports      |

**Training delivery:**

1. All sessions recorded via video walkthrough for future reference and new hire onboarding
2. Quick-reference cards distributed at session end
3. Champion support channel activated for real-time support
4. Questions log maintained (feeds into FAQ and hypercare priorities)

---

### 3c. Hypercare

> **Purpose:** Intensive post-launch support to stabilize adoption and address issues.

**Duration:** 2 weeks

**Week 1 (High-touch):**

- Daily 15-minute standup with champions to collect feedback and address issues
- Monitor daily login and content usage metrics
- Send targeted outreach to reps who have not logged in within first 3 days
- Triage and fix any CRM integration or content display issues within 24 hours
- Update FAQ with new questions from training and early usage

**Week 2 (Transition):**

- Weekly 30-minute office hours (open to all, champions encouraged to attend)
- Review adoption metrics against targets (login rate, content searches, shares)
- Address remaining issues or confusion points
- Prepare adoption report for leadership
- Confirm team can operate without daily support

**When to extend:** If login rate is below 50% at end of week 2, or if critical integration issues persist, extend hypercare by 1 week.

**Output:** Stabilized platform, adoption metrics trending in the right direction, no critical issues outstanding.

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm customer team can operate the platform independently.

**Validation checkpoint:**

- [ ] All training sessions delivered and recorded
- [ ] Quick-reference cards and FAQ distributed
- [ ] Champion program active and providing feedback
- [ ] Hypercare period complete
- [ ] Login rate exceeds 60% of licensed users
- [ ] No critical integration or content issues outstanding
- [ ] Admin team can upload content, manage users, and run reports without support
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** -> Team is enabled, adoption is tracking, project wrapping up
- **Extend Hypercare** -> Adoption is below target or critical issues remain

---

## Phase 4: Handoff

> **Goal:** Clean project close with governance model established, admin ownership transferred, and retention/expansion path set.
>
> **Output:** Governance playbook delivered, admin team self-sufficient, maintenance schedule documented, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule -> 4b Internal Handoff -> 4c External Handoff -> 4d Project Close
                           (SME -> Architect)      (to Customer)          (Archive + Debrief)
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At                                                                         |
| ----------------------------- | -------------------- | ------------------------------------------------------------------------------------- |
| **Single Project**            | Customer owns        | 4c (External Handoff) — customer receives governance playbook and runs it themselves  |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) — Architect receives governance playbook and manages for customer |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention after the project is complete.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task              | What to Check                                      | Red Flag Threshold                                     |
| ------------------------- | -------------------------------------------------- | ------------------------------------------------------ |
| Content freshness audit   | Review content expiration alerts, flag stale assets | >20% of active content past expiration date             |
| Adoption metrics review   | Login rate, content searches, shares per rep        | Login rate drops below 50%, or share volume drops >30%  |
| New content publishing    | Review content request queue, publish new materials | >5 content requests unaddressed for >2 weeks            |
| CRM integration health    | Verify sync is active, activity logging working     | Any sync failures or data gaps in activity logs         |

**Quarterly Tasks:**

| Quarterly Task               | What to Review                                | Action if Off-Track                              |
| ---------------------------- | --------------------------------------------- | ------------------------------------------------ |
| Taxonomy effectiveness       | Search patterns vs taxonomy structure          | Adjust tags and categories based on actual usage  |
| Content effectiveness report | Content-to-win-rate correlation                | Archive underperformers, promote high-performers  |
| Governance compliance        | Content owner assignments, review cycles met   | Reassign orphaned content, enforce review cadence |
| Platform feature updates     | Vendor release notes, new features available   | Evaluate and enable high-value new features       |
| Learning path refresh        | Onboarding curriculum relevance, quiz accuracy | Update modules for product changes                |

**After First Business Cycle (30-60 days post-launch):**

- Full adoption review: login rates, content usage patterns, rep feedback survey
- Content gap analysis: what are reps searching for that does not exist?
- CRM integration audit: is activity logging accurate? Are engagement notifications useful?
- Learning path completion rates: are new hires completing onboarding curriculum?
- Win rate comparison: deals with content shared vs. deals without (if enough data)

**Refinement Triggers (when to re-engage):**

| Trigger                   | Threshold                                | Response                                                  |
| ------------------------- | ---------------------------------------- | --------------------------------------------------------- |
| Adoption decline          | Login rate drops below 40% for 2+ weeks  | Re-engage with targeted enablement or champion refresh    |
| Content decay             | >30% of content past freshness threshold | Scope content refresh project                             |
| New sales process/segment | Major change to sales stages or buyer personas | Scope taxonomy restructure and content re-mapping         |
| Platform upgrade          | Major version change from vendor          | Scope feature evaluation and re-training                  |

**Every 6-12 Months:**

- Full platform health assessment: adoption trends, content library quality, integration reliability
- Competitive content refresh: updated battle cards, new competitor additions
- Taxonomy review: align with any changes to sales process, product line, or buyer personas
- ROI assessment: measure onboarding time reduction, content-to-win-rate correlation, time-to-find improvement

---

### 4b. Internal Handoff (SME to Architect)

> **Purpose:** Transfer context so Architect can manage ongoing relationship.

**What the Architect needs to know:**

- Platform vendor and tier (licensing model, support contacts, renewal dates)
- Content taxonomy logic and any compromises made during design
- CRM integration architecture (sync frequency, field mappings, known limitations)
- Customer stakeholder dynamics (who champions the platform, who was reluctant)
- Common issues and resolutions from hypercare period
- When to escalate back to SME

**Escalation guidelines:**

| Issue Type                                      | Who Handles        | Examples                                        |
| ----------------------------------------------- | ------------------ | ----------------------------------------------- |
| Content uploads, user management, basic reports  | Architect          | New hire added, quarterly content refresh        |
| Taxonomy restructure, CRM integration changes    | SME                | New sales stage added, Salesforce field changes  |
| Platform tier upgrade or vendor migration         | SME                | Moving from Highspot to Seismic, or tier upgrade |
| Learning path redesign                            | SME                | New onboarding curriculum, skills gap analysis   |

**For Dedicated engagements:** Architect also receives the maintenance schedule (4a) and becomes responsible for executing monthly and quarterly tasks. SME walks Architect through each maintenance task and known gotchas.

---

### 4c. External Handoff (to Customer)

> **Purpose:** Formal project completion with customer.

**Final project meeting:**

- Review adoption metrics vs targets set at kickoff
- Walk through governance playbook (content ownership, review cycles, archival rules)
- Walk through maintenance schedule (monthly, quarterly, annual tasks)
- Confirm admin team is self-sufficient (user management, content publishing, reporting)
- Answer final questions
- Make it explicit: "Project complete"
- **For Single Project engagements:** Hand over the governance playbook and maintenance schedule; walk customer through each task

**Documentation package:**

- All training video recordings (champion, sales team, leadership, admin)
- Content governance playbook
- Admin runbook (user management, content publishing, taxonomy changes, reporting)
- Content mapping matrix (final version)
- CRM integration documentation (architecture, field mappings, known limitations)
- FAQ document
- Definition Alignment Document (final version)
- Quick-reference cards
- Maintenance schedule
- Vendor support contact information and escalation paths

**For Single Project engagements:** Record a video walkthrough of the governance playbook and maintenance schedule. This becomes the customer's reference for ongoing platform management.

**Output:** Customer owns the platform and governance process. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location
- [ ] Handoff documentation complete
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized
- [ ] Adoption metrics baselined for future comparison

#### Internal Debrief (Optional but Recommended)

- What went well? (Platform selection process, content migration efficiency, adoption rates)
- What would we do differently? (Timeline, taxonomy complexity, training approach)
- What content gaps did the customer have that we could productize?

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell -> Downsell -> Retry  |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (ongoing content optimization + adoption coaching + quarterly reviews)
   | if no
2. Downsell: Content refresh project, advanced analytics buildout, or new learning path design
   | if yes
3. Retry retainer at end of next project cycle
```

**Script:**

> "Now that your enablement platform is live and the team is using it, there are two ways we can continue. Option 1: We handle ongoing content optimization, adoption coaching, and quarterly health checks through managed services. Option 2: If there's a specific next step — like building out competitive battle cards, creating advanced analytics, or designing a new onboarding curriculum — we can scope that as a project. Which sounds more interesting?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On [date ~90 days out], we'll review adoption trends, content effectiveness data, and see if the taxonomy needs adjustment based on real usage patterns."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                           |
| ------------------- | ------------------------------------------------------ |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks        |
| 2. Review metrics   | Pull adoption data, content effectiveness, rep feedback |
| 3. Decide ownership | Can Architect handle this, or need SME?                 |
| 4. Prep materials   | If SME needed, brief them. If Architect, prep dashboard views. |

**At the refinement check-in:**

- Review adoption metrics against 30-day baselines
- Assess content effectiveness (which content correlates with wins)
- Identify taxonomy adjustments based on actual search patterns
- If minor: Architect handles taxonomy tweaks and content refresh
- If major: Scope new project (advanced analytics, learning path redesign, platform migration)

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- Platform evaluation summary and selection recommendation
- Content taxonomy design document
- Content mapping matrix (content aligned to sales stages and buyer personas)
- Content migration plan and prioritization framework
- Rollout timeline and adoption plan

**Technical Deliverables:**

- Configured sales enablement platform (taxonomy, roles, permissions, SSO)
- Migrated and tagged content library (top 50-100 priority assets)
- CRM integration (Salesforce or HubSpot — bidirectional sync, activity logging, in-CRM widget)
- Analytics dashboards (content usage, engagement tracking, adoption, content effectiveness)
- Learning paths and certifications (if in scope)
- Content collections and playlists (stage-based, persona-based, competitive)

**Documentation Package:**

- Training video recordings (champion, sales team, leadership, admin)
- Quick-reference cards
- Content governance playbook
- Admin runbook
- CRM integration documentation
- FAQ document
- Definition Alignment Document (final version)
- Maintenance schedule

---

## Appendix

### Roles

| Role | What They Do |
|---|---|
| **Architect** | Owns the customer relationship, leads strategy, creates specs, does enablement, owns account post-delivery |
| **Engineer** | Platform configuration, CRM integration, analytics setup (Phase 2) |
| **SME** | Sales enablement domain expertise, content taxonomy design, governance framework |

---

### Industry Context

Sales enablement is a rapidly growing category. The global sales enablement platform market was valued at $5.25 billion in 2024 and is projected to reach $19.92 billion by 2032, growing at 18.3% CAGR [4]. Over 80% of large enterprises have adopted sales enablement platforms, but less than 50% of SMBs have done so [4], creating a significant opportunity in the mid-market B2B SaaS segment.

The productivity case is clear: sales reps without an enablement platform spend an average of 10 hours per week searching for content [2], and 65% of reps report they cannot find meaningful content to share with buyers [1]. Only 30% of a sales rep's time is spent actively selling — the rest is consumed by administrative tasks, data entry, and content searching [5]. A structured enablement platform addresses this directly: organizations with sales enablement strategies report 49% higher win rates on forecasted deals [3], and structured onboarding programs reduce new hire ramp time by 40-50% [6].

Platform selection matters. Highspot tends to suit mid-market B2B SaaS companies (50-500 reps) with its faster deployment and adoption focus — one 200-person SaaS company achieved 87% adoption within 60 days [7]. Seismic suits larger enterprises, especially in regulated industries, with deeper content management and approval workflows [7]. Mindtickle and Showpad fill specific niches around training-first and experience-first approaches respectively.

---

### What Each Phase Produces

| Phase                    | Output                                                                 | Gate Criteria                                                                  |
| ------------------------ | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **Phase 1: Strategy**    | Platform selection + content taxonomy + migration plan + rollout timeline | Stakeholders approved platform, taxonomy, migration scope, and timeline        |
| **Phase 2: Engineering** | Configured platform with content, CRM integration, and analytics        | Platform tested end-to-end, customer approved core workflows                   |
| **Phase 3: Enablement**  | Trained team, active champions, adoption metrics tracked                | All training delivered, hypercare complete, login rate >60%                     |
| **Phase 4: Handoff**     | Customer-owned platform with governance model and maintenance plan       | Admin team self-sufficient, governance documented, project closed              |

---

### How to Adapt Per Customer

| Customer Profile              | Strategy Weight | Engineering Weight | Enablement Weight | Adaptation                                           |
| ----------------------------- | --------------- | ------------------ | ----------------- | ---------------------------------------------------- |
| Platform already selected     | Light (1-2 wks) | Heavy              | Heavy             | Skip vendor eval; focus on taxonomy + migration      |
| Small team (&lt;30 reps)         | Light           | Medium             | Medium            | Simpler taxonomy, skip learning paths, lighter training |
| Large team (200+ reps)        | Medium          | Heavy              | Heavy             | Phased rollout by team/region, extended hypercare     |
| Content library >500 assets   | Medium          | Heavy              | Medium            | Extended migration, automated metadata tagging        |
| Regulated industry            | Heavy           | Heavy              | Medium            | Compliance review, approval workflows, audit trails   |

---

## References

[1] [Spekit - Sales Enablement Statistics and Trends](https://www.spekit.com/blog/sales-enablement-statistics-trends)

[2] [Mediafly - Top Sales Content Management System Stats](https://www.mediafly.com/blog/the-top-sales-content-management-system-stats/)

[3] [G2 - 70 Sales Enablement Statistics for 2025](https://learn.g2.com/sales-enablement-statistics)

[4] [Grand View Research - Sales Enablement Platform Market Size Report 2030](https://www.grandviewresearch.com/industry-analysis/sales-enablement-platform-market-report)

[5] [SPOTIO - 140+ Sales Statistics 2026 Update](https://spotio.com/blog/sales-statistics/)

[6] [Highspot - Sales Enablement ROI](https://www.highspot.com/sales-enablement/sales-enablement-roi/)

[7] [Flowla - Highspot vs Seismic Comparison](https://www.flowla.com/blog/highspot-vs-seismic)
