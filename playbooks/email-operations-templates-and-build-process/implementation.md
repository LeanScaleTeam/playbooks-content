# Email Operations Templates and Build Process — Implementation

## Project One-Pager

### Email Operations: Templates & Build Process One-Pager

#### Project Type

- Category: Technical
- Primary Deliverable: A library of 5-10 modular, responsive email templates in HubSpot or Marketo with a documented, repeatable email build process

##### Phase Relevance

| Phase          | Applies? | Weight | Notes                                                    |
| -------------- | -------- | ------ | -------------------------------------------------------- |
| 1. Strategy    | Yes      | Light  | 2-3 meetings: audit, requirements, process mapping       |
| 2. Engineering | Yes      | Heavy  | Core work: template design, build, dynamic content, QA   |
| 3. Enablement  | Yes      | Med    | Training session + documentation handoff                 |
| 4. Handoff     | Yes      | Light  | Documentation package delivery + 30-day check-in         |

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────>│ 2. ENGINEER  │────>│3. ENABLEMENT │────>│  4. HANDOFF  │
  │    Light     │     │    Heavy     │     │     Med      │     │    Light     │
  │ 1a->1b->1c->1d │     │ 2a->2b->2c->2d │     │ 3a->3b->3c->3d │     │ 4a->4b->4c->4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   Audit & reqs         Template build       Team training        Docs & ownership
   Process mapping      QA & testing         Hypercare            Maintenance plan
```

**This project's flow:**
- Full 4-phase. Light strategy (audit + requirements), heavy engineering (template design, build, QA), medium enablement (training + docs), light handoff.
- Phase 2 is where 60-70% of the effort sits. Template architecture, MAP build, dynamic content, and cross-client rendering testing are the core deliverables.

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Watch intro video explaining what a standardized email template library is and why it reduces production time
- [ ] Complete email operations intake form (current MAP, template count, email types sent, build process pain points)
- [ ] Gather brand assets (logos in PNG/SVG, hex color codes, approved fonts, CTA button styles)
- [ ] Provide access to 10-15 recent email sends as examples of current state
- [ ] Grant MAP admin or template-creation-level access

##### Track B: Architect Prep
- [ ] Pull list of all existing email templates in the MAP
- [ ] Review 10-15 recent emails sent for design consistency, mobile rendering, and quality
- [ ] Document current email build workflow (request to send) based on intake form
- [ ] Identify gaps: which email types are missing templates (promotional, transactional, newsletter, event)
- [ ] Create v0 template requirements document with recommended use cases

#### Refinement Loop (1b -> 1c -> 1d)

| Meeting      | Sub-Phase | Focus                                                | Stakeholder                        | Output                             |
| ------------ | --------- | ---------------------------------------------------- | ---------------------------------- | ---------------------------------- |
| Kickoff      | 1b        | Present audit findings, validate pain points         | Marketing Ops, Demand Gen Lead     | Confirmed template requirements    |
| Refinement 1 | 1c        | Review template architecture and design system       | Marketing Ops, Brand/Design Lead   | Approved modular design system     |
| Sign-Off     | 1d        | Approve final template scope, use cases, build plan  | Marketing Leadership               | Signed-off template requirements   |

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held — audit findings presented, pain points validated
- [ ] 1c. Refinement loop complete — template architecture approved
- [ ] 1d. Strategic sign-off obtained on template scope and build plan

##### Phase 2: Engineering
- [ ] 2a. Tech spec created (template architecture + modular block definitions)
- [ ] 2b. Engineering handoff meeting held
- [ ] 2c. Build complete (all templates in MAP + dynamic content configured)
- [ ] 2d. QA/Test complete (cross-client rendering + accessibility + end-to-end build test)

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped (template guide, build process runbook, QA checklist)
- [ ] 3b. Training session delivered (45-60 min hands-on)
- [ ] 3c. Hypercare period complete (2 weeks)
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff (SME -> Architect) complete
- [ ] 4c. External handoff complete
- [ ] 4d. Project closed and archived

#### Document Types

##### Working Documents (iterate together)

| Document                       | Purpose                                           | When Complete                                    |
| ------------------------------ | ------------------------------------------------- | ------------------------------------------------ |
| Email operations intake form   | Capture current state, pain points, MAP details   | All fields filled by customer                    |
| Template requirements document | Define use cases, personalization, content blocks  | Approved by marketing leadership                 |
| Current state process map      | Map existing email build workflow with bottlenecks | Pain points identified and prioritized           |
| Brand asset kit                | Collect logos, colors, fonts, CTA styles           | All assets received and format-verified          |

##### Deliverables (polished outputs)

| Deliverable                     | Created From                    | Customer Uses For                              |
| ------------------------------- | ------------------------------- | ---------------------------------------------- |
| Template library (5-10 in MAP)  | Template requirements + brand kit| On-brand email production at speed             |
| Email build process runbook     | Current state process map       | Standardized workflow for all team members      |
| Template style guide            | Brand asset kit + requirements  | Self-service customization within guardrails    |
| QA checklist                    | Testing results + best practices| Pre-send quality verification                  |

#### Enablement Details

##### Training Types

| Type       | Audience                              | Focus                                         | Duration |
| ---------- | ------------------------------------- | --------------------------------------------- | -------- |
| Hands-on   | Marketing Ops, Email Marketers        | Build an email using templates, run QA process | 45-60m   |
| Leadership | VP Marketing, Demand Gen Lead         | Template library overview, expected velocity gains | 20m  |

##### Hypercare
- Applies: Yes
- Duration: 2 weeks
- Office Hours: Yes — Weekly 30-min slot for template questions and build process issues

##### Training Assets to Create
- [ ] Video walkthrough: Template library walkthrough (which template for which use case)
- [ ] Video walkthrough: Email build process demo (request to send)
- [ ] Doc: Template customization guide (what can and cannot be changed)
- [ ] Doc: Content block reference with image specs and copy guidelines
- [ ] Doc: QA checklist for pre-send verification

#### Handoff & Retention

##### Internal Handoff (SME -> Architect)
- Key context for Architect: Which templates were built, design system decisions, MAP folder structure, known rendering quirks per email client
- Escalation trigger: New template type requests, major design system changes, MAP upgrade or migration

##### External Handoff
- Final meeting agenda: Review template library, walk through build process runbook, demonstrate QA checklist, confirm maintenance ownership
- Documentation package: Template guide, runbook, QA checklist, training recordings, style guide

##### Maintenance Schedule
- Monthly: Review template usage, check for broken rendering in updated email clients
- Quarterly: Audit for template drift, review new use case requests
- Who owns: Single project = customer owns | Dedicated = Architect owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services (ongoing email ops support) -> if no -> Downsell: Email nurture program project or email deliverability optimization -> Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~1 quarter after handoff
- Internal prep trigger: 2 weeks before
- Decision: Architect handles template iteration / SME needed for new template types

#### Key Assets

| Asset                          | When Used            |
| ------------------------------ | -------------------- |
| Email operations intake form   | Phase 1a Pre-Kickoff |
| Template requirements document | Phase 1b-1d Strategy |
| Template style guide           | Phase 2c Build       |
| QA checklist                   | Phase 2d Test        |
| Build process runbook          | Phase 3b Training    |

#### Definition Alignment Terms

| Term                    | Typical Definition                                                                                   |
| ----------------------- | ---------------------------------------------------------------------------------------------------- |
| Email Template          | A pre-built, reusable email layout in the MAP with modular content blocks and locked brand elements  |
| Content Block           | A reusable component within a template (header, hero, body, CTA, footer, social)                    |
| Modular Architecture    | A design system where templates are composed of interchangeable content blocks                        |
| Dynamic Content         | Email sections that change based on contact properties (lifecycle stage, industry, region)            |
| Personalization Token   | A merge field that inserts contact-specific data (first name, company) into the email                |
| Responsive Design       | Template layout that adapts to render correctly on desktop, tablet, and mobile devices                |
| Cross-Client Rendering  | Testing that an email displays correctly in Gmail, Outlook, Apple Mail, Yahoo, and mobile clients     |
| Build Process           | The standardized workflow from email request intake to deployment                                     |
| QA Checklist            | A pre-send verification document covering links, rendering, personalization, accessibility, compliance|

#### Common Gotchas
- Building too many templates upfront (15+) before validating adoption -> Start with 5-7 covering 80% of use cases [1]
- Skipping dark mode testing -> Over 80% of smartphone users enable dark mode and color inversion breaks designs [2]
- Creating templates only one person can edit -> Document everything, train 2+ team members
- Not setting up template governance (versioning, change log, master template lock) -> Assign ownership, prevent drift
- Ignoring accessibility (no alt text, low contrast, small fonts) -> WCAG AA requires 4.5:1 contrast ratio for normal text [3]
- Testing only in Gmail and assuming everything works -> Outlook desktop renders HTML email differently than all other clients

#### Methodology Options

| Option                   | When to Use                                                | Complexity |
| ------------------------ | ---------------------------------------------------------- | ---------- |
| HubSpot drag-and-drop    | Team has HubSpot Marketing Hub, prefers no-code approach   | Low        |
| HubSpot coded templates  | Need pixel-perfect control, team has HTML/CSS skills       | Medium     |
| Marketo Email 2.0        | Team uses Marketo, needs modular sections with variables   | Medium     |
| Third-party builder (Knak, Stensul) | High volume, need collaboration features, approval workflows | High  |

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on which templates to build and how the build process will work.
>
> **Output:** Approved template requirements document + build process design (signed off by marketing leadership).

### 1a. Pre-Kickoff

> Two parallel tracks run after the deal closes and before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                        | Format             |
| ----------------------------- | -------------------------------------------------------------- | ------------------ |
| Intro video                   | Explain what standardized email templates deliver and why      | Video (5-10 min)   |
| Definition Alignment Document | Get sign-off on terms: template, content block, dynamic content| Google Doc         |
| Email operations intake form  | Current MAP, email volume, pain points, brand assets           | Google Form        |

**Intake form key fields:**
- Which MAP? (HubSpot / Marketo / Other)
- How many email templates exist today?
- How many emails does the team send per month?
- What is the average time to build and send one email (hours)?
- What email types are used most? (promotional, newsletter, event, transactional, onboarding)
- Who is involved in the email build process? (roles and handoffs)
- What brand assets exist? (style guide, logo files, color codes, font specs)
- What are the top 3 pain points with current email production?

**Completion tracking:** Marketing Ops lead follows up. Do not cancel kickoff if incomplete, but push hard after.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                        | Output                               |
| ---- | ------------------------------------------------------------- | ------------------------------------ |
| 1    | Log into MAP, pull full template inventory                    | Template list with last-used dates   |
| 2    | Review 10-15 recent email sends for consistency and quality   | Quality assessment with screenshots  |
| 3    | Interview 2-3 marketing team members on build workflow        | Current state process map            |
| 4    | Document average build time (hours from request to send)      | Baseline metric for improvement      |
| 5    | Identify missing template types and mobile rendering issues   | Gap analysis                         |
| 6    | Create v0 template requirements document                      | Draft use cases, blocks, personalization|

**Critical:** Mark everything as ASSUMED. The kickoff call validates.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building anything.

| Term                   | Our Definition                                                              | Internally Approved? |
| ---------------------- | --------------------------------------------------------------------------- | -------------------- |
| Email Template         | Pre-built, reusable email layout in MAP with modular blocks and locked brand| [ ] Yes / [ ] No     |
| Content Block          | Reusable component (header, hero, body, CTA, footer, social)               | [ ] Yes / [ ] No     |
| Dynamic Content        | Sections that change based on contact properties                            | [ ] Yes / [ ] No     |
| Personalization Token  | Merge field inserting contact-specific data                                 | [ ] Yes / [ ] No     |
| Build Process          | Standardized workflow from request intake to email deployment               | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your marketing leadership. Check "Yes" when approved. We cannot proceed until all terms are aligned.

---

### 1b. Kickoff Call

> **Purpose:** Present audit findings and v0 template requirements. Customer reacts and corrects — they do not create from scratch.

#### Agenda (60 min)

| Time  | Topic                     | What Happens                                          |
| ----- | ------------------------- | ----------------------------------------------------- |
| 0-15  | Audit findings            | "Here's what we found in your MAP and recent emails"  |
| 15-30 | Pain point validation     | Confirm build time, inconsistency, mobile issues      |
| 30-45 | Template use case review  | Prioritize which email types need templates first     |
| 45-55 | Definition alignment      | Review Definition Alignment Doc                       |
| 55-60 | Next steps                | Schedule architecture review, assign brand asset homework|

#### What We Bring

- Template inventory audit with quality scores
- Current state process map with bottlenecks highlighted
- v0 template requirements document (use cases, content blocks, personalization needs)
- Definition Alignment Document pre-filled with recommendations
- Screenshots of rendering issues found in current emails

#### What We Leave With

- Confirmed pain points and prioritized template use cases
- Brand assets or clear timeline for delivery
- Any corrections to v0 requirements (info needed for v1)
- Architecture review meeting scheduled

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Finalize template architecture and design system before building.

#### The Pattern

```
Kickoff Call (validate audit, prioritize use cases)
    |
    v
Architect creates template architecture v1
    |
    v
Architecture Review (present design system, get approval)
    |
    v
Final adjustments -> Sign-off
```

#### Meeting: Template Architecture Review

**Before the meeting:**
1. Create modular content block library (header, hero, 1-column, 2-column, CTA, footer, social)
2. Design 2-3 layout variations for each major email type
3. Define responsive breakpoints (mobile: 320-480px, tablet: 481-768px, desktop: 769px+)
4. Establish spacing, padding, and margin standards
5. Build email-specific color and typography style guide

**During the meeting:**
1. Walk through modular block library with visual mockups
2. Review layout variations for each email type
3. Confirm dynamic content rules (which fields drive content swaps)
4. Get design approval from brand/marketing team
5. Agree on template scope (final count and priority order)

**After the meeting:**
1. Finalize template architecture document
2. Update requirements with any design changes
3. Prepare build sequence for Phase 2

#### Typical Timeline

| Milestone                | Timing                |
| ------------------------ | --------------------- |
| Pre-kickoff prep         | 2-3 days              |
| Kickoff call             | Day 1 of engagement   |
| Architecture review      | Day 5-7               |
| Sign-off                 | Day 7-10              |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything before building.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by stakeholders
- [ ] Template use cases prioritized and approved (types and count)
- [ ] Modular design system approved by brand/marketing team
- [ ] Content block library defined (all components specified)
- [ ] Dynamic content requirements documented (which fields, which rules)
- [ ] Brand assets received and verified (logos, colors, fonts, CTA styles)
- [ ] Current state build process mapped with baseline metrics
- [ ] No blockers for engineering

#### Decision Point

- **Proceed to Engineering** -> Template architecture approved, brand assets received, ready to build
- **Project complete** -> This project always proceeds to Engineering. Templates must be built.

---

## Phase 2: Engineering

> **Goal:** Build and test the complete email template library and validate the build process.
>
> **Output:** 5-10 functional, tested email templates in the MAP + documented build process, ready for training.

| Project Type    | Engineering Weight | This Project                                        |
| --------------- | ------------------ | --------------------------------------------------- |
| Technical-heavy | Heavy (60-70%)     | Template build, dynamic content, rendering QA       |

### Sub-Phases

```
2a Tech Spec -> 2b Engineering Handoff -> 2c Build -> 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate approved template architecture into technical build specifications for the MAP.

**Input:** Signed-off template requirements + modular design system + brand assets

**What happens:**

1. Map each content block to MAP module syntax (HubSpot drag-and-drop modules or Marketo Email 2.0 modules)
2. Define personalization token mappings (contact property -> template field)
3. Specify dynamic content rules (IF lifecycle stage = X, THEN show content block Y)
4. Document responsive CSS breakpoints and inline styles required
5. Create build sequence (master template first, then individual templates in priority order)

**Output:** Tech spec containing:

- MAP module definitions for each content block (header, hero, 1-column, 2-column, CTA, footer, social)
- Personalization token list with fallback values (e.g., `\{\{first_name | "there"\}\}`)
- Dynamic content decision tree (which properties trigger which content variations)
- CSS/inline style specifications for responsive behavior
- Build sequence with estimated hours per template
- Folder structure in MAP for template organization

**HubSpot-specific tech spec items:**
- Module field types (rich text, image, choice, boolean)
- Drag-and-drop template vs coded template decision per template type
- Global module vs local module decisions
- Design Manager folder structure

**Marketo-specific tech spec items:**
- Email 2.0 module definitions with `mktoModule` attributes
- Variable declarations (`mktoString`, `mktoColor`, `mktoImg`, `mktoBoolean`)
- Editable vs locked section boundaries
- Program template associations

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs with engineer before building.

**Who attends:** Architect + Engineer (or Marketing Ops builder)

**Agenda (30-45 min):**

| Time  | Topic              | What Happens                                              |
| ----- | ------------------ | --------------------------------------------------------- |
| 0-15  | Walk through specs | Architect explains template architecture + module definitions |
| 15-30 | Engineer questions | Clarify MAP-specific implementation, flag rendering risks |
| 30-45 | Refine and approve | Adjust specs, confirm build sequence and timeline         |

**What Architect brings:**
- Strategic package (approved template requirements + design system)
- Draft tech spec (from 2a)
- Brand asset kit (verified formats)
- Known rendering risks (Outlook desktop, dark mode, etc.)

**What engineer leaves with:**
- Approved tech spec with MAP-specific implementation details
- Build sequence with priority order
- Brand asset files in correct formats
- Access credentials and folder structure in MAP

---

### 2c. Build (Configure)

> **Purpose:** Build all templates in the MAP following the approved tech spec.

**Input:** Approved tech spec from 2b

**Build sequence:**

1. **Set up MAP infrastructure**
   - Create folder structure in MAP (e.g., `Email Templates > Promotional`, `Email Templates > Newsletter`)
   - Upload brand assets (logos, images) to MAP file manager
   - Configure global styles (colors, fonts, button styles)

2. **Build master template**
   - Create master template with all modular content blocks
   - Configure responsive breakpoints (inline CSS + media queries)
   - Set up locked brand elements (header, footer, social links, legal)
   - Test master template renders correctly in MAP preview

3. **Build individual templates (in priority order)**
   - Promotional email template (sale, discount, product launch) — 1-column hero + CTA-heavy layout
   - Newsletter/roundup template — multi-section layout with 2-column content blocks
   - Event invitation template — hero image + RSVP/registration CTA + event details block
   - Transactional email templates (confirmation, receipt, notification) — clean, minimal layout
   - Welcome email template — onboarding flow with personalization

4. **Configure dynamic content and personalization**
   - Add personalization tokens with fallback values to all templates
   - Set up dynamic content modules for industry-specific messaging
   - Configure smart content rules based on lifecycle stage (HubSpot) or segmentation (Marketo)
   - Add conditional logic for product lines or regions (if applicable)
   - Configure pre-header text and subject line variable fields

**Build tracking:**

- [ ] MAP folder structure created
- [ ] Brand assets uploaded
- [ ] Master template built and previewed
- [ ] Promotional template complete
- [ ] Newsletter template complete
- [ ] Event invitation template complete
- [ ] Transactional templates complete
- [ ] Welcome template complete
- [ ] Dynamic content configured
- [ ] Personalization tokens with fallbacks verified

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify templates render correctly across email clients and the build process works end-to-end.

**Three types of testing for this project:**

| Type                        | Who          | Purpose                                                      |
| --------------------------- | ------------ | ------------------------------------------------------------ |
| Cross-client rendering test | Our team     | Verify templates display correctly in 90+ email clients [4]  |
| Accessibility audit         | Our team     | Verify WCAG AA compliance, CAN-SPAM elements                 |
| End-to-end build process    | Customer     | Verify a marketing team member can build an email using templates|

**Cross-client rendering checklist:**

- [ ] Templates tested in Litmus or Email on Acid (90+ client previews) [4]
- [ ] Gmail (desktop + mobile) rendering verified
- [ ] Outlook desktop (2016, 2019, O365) rendering verified — this is where most issues occur
- [ ] Apple Mail rendering verified
- [ ] Yahoo Mail rendering verified
- [ ] iOS Mail and Android Gmail rendering verified
- [ ] Dark mode rendering tested and compatible [2]
- [ ] Responsive design adapts correctly at all breakpoints (mobile, tablet, desktop)
- [ ] Screenshot library created showing expected rendering per client

**Accessibility and compliance checklist:**

- [ ] All images have descriptive alt text
- [ ] Color contrast ratios meet WCAG AA (4.5:1 for body text, 3:1 for large text) [3]
- [ ] Font sizes readable (minimum 14px body, 22px headers)
- [ ] Unsubscribe link present and functional
- [ ] Physical mailing address in footer per CAN-SPAM
- [ ] Screen reader compatibility tested for key content
- [ ] Links are descriptive (not "click here")

**End-to-end build process test:**

- [ ] Marketing team member (not the builder) attempts to create an email from template
- [ ] Build time measured start to finish — target: under 1 hour for standard email
- [ ] Confusion or friction points documented
- [ ] QA checklist catches common errors (broken links, missing alt text, wrong personalization)
- [ ] Approval workflow functions correctly
- [ ] Email deploys successfully to test segment

**Engineering sign-off checkpoint:**

- [ ] All templates render correctly in target email clients (95%+ pass rate)
- [ ] Accessibility audit passed
- [ ] End-to-end build test completed successfully by non-builder
- [ ] Build time meets target (50%+ reduction from baseline)
- [ ] Customer has tested and approved
- [ ] Ready for enablement

**Decision point:**

- **Proceed to Enablement** -> All templates built, tested, and approved
- **Loop back to Build** -> Rendering issues or design changes needed

---

## Phase 3: Enablement

> **Goal:** Marketing team can build and send on-brand emails independently using the new template library and process.
>
> **Output:** Trained team with documentation, stabilized system, no template or process issues outstanding.

### Sub-Phases

```
3a Training Prep -> 3b Training Sessions -> 3c Hypercare -> 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from template documentation and build process specs.

**Input:** Template library + tech specs + QA results + build process runbook

**What happens:**

1. Compile template guide describing each template and its use case
2. Create customization guide (what can and cannot be changed in each template)
3. Build content block reference with visual examples
4. Document image specifications (dimensions, file size limits, format requirements)
5. Write email build process runbook (step-by-step from request to send)
6. Create QA checklist for pre-send verification
7. Prepare hands-on training exercise (build a promotional email from template)

**Output:** Training package containing:

- Template overview document (which template for which use case)
- Customization guide (editable vs locked sections, safe modifications)
- Content block reference with image specs
- Email build process runbook (step-by-step with screenshots)
- QA checklist for pre-send verification
- Hands-on exercise: "Build a promotional email in 30 minutes"
- Copywriting guidelines for CTAs, subject lines, and body text

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to marketing team so they can produce emails independently.

**Two types of training:**

| Type                | Audience                          | Focus                                                      |
| ------------------- | --------------------------------- | ---------------------------------------------------------- |
| Hands-on training   | Email marketers, Marketing Ops    | Build an email using templates, run QA checklist, submit for approval |
| Leadership overview | VP Marketing, Demand Gen Lead     | Template library tour, expected velocity gains, governance rules |

**Hands-on training session (45-60 min):**

1. Walk through template library — when to use each template (10 min)
2. Demonstrate email build process step-by-step in MAP (15 min)
3. Cover customization best practices and common mistakes to avoid (10 min)
4. Hands-on exercise: Each participant builds a promotional email from template (15 min)
5. Run QA checklist on the built email together (5 min)
6. Q&A (5 min)

**Leadership overview (20 min):**

1. Template library tour — what was built and why
2. Expected outcomes: 50%+ reduction in email build time, brand consistency, mobile responsiveness
3. Governance: who can edit master templates, versioning rules, change request process

**Training delivery:**

1. Schedule sessions with appropriate stakeholders
2. Deliver training live via video call or in-person
3. Record video walkthroughs for each session for future reference
4. Answer questions, note gaps for FAQ document

**Output:**

- Trained email marketers who can build from templates independently
- Trained leadership on governance and expected outcomes
- Video walkthrough recordings for onboarding future team members
- Questions log feeding into FAQ

---

### 3c. Hypercare

> **Purpose:** Intensive post-launch support as the team starts using templates in production.

**Duration:** 2 weeks

**What happens:**

- Weekly 30-min office hours for template questions and build process issues
- Quick response to rendering issues discovered in production sends
- Template adjustments if a use case was missed or a content block needs modification
- Build process refinement based on real-world friction points

**Common hypercare issues for this project:**
- "I can't figure out how to swap the dynamic content section" -> Walk through smart content rules
- "The email looks broken in Outlook" -> Check inline CSS, provide Outlook-specific fix
- "I need a template for \[use case not in original scope\]" -> Assess: modify existing template or note for future iteration
- "The approval workflow is too slow" -> Review routing rules, adjust SLAs

**When to skip:** Do not skip for this project type. Teams always have questions in the first 2 weeks of using new templates.

**Output:** Stabilized template system, team building emails independently, no critical issues

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm marketing team can operate without daily support.

**Validation checkpoint:**

- [ ] All training sessions delivered
- [ ] Training recordings and documentation provided
- [ ] Hypercare period complete (2 weeks)
- [ ] Team has built at least 3 production emails using new templates without assistance
- [ ] No critical rendering or process issues outstanding
- [ ] FAQ document updated with hypercare questions
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** -> Team is enabled, building emails independently
- **Extend Hypercare** -> Still struggling with template usage or process adoption

---

## Phase 4: Handoff

> **Goal:** Clean project close with maintenance plan for template updates and governance.
>
> **Output:** Customer owns the template library and build process. Maintenance schedule in place. Project archived.

**Structure:**

```
4a Maintenance Schedule -> 4b Internal Handoff -> 4c External Handoff -> 4d Project Close
                          (SME -> Architect)                              (Archive + Debrief)
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At                                                     |
| ----------------------------- | -------------------- | ----------------------------------------------------------------- |
| **Single Project**            | Customer owns        | 4c (External Handoff) — customer runs maintenance themselves      |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) — Architect manages template system ongoing |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention to prevent template drift and keep the system current.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task                    | What to Check                                    | Red Flag Threshold                                  |
| ------------------------------- | ------------------------------------------------ | --------------------------------------------------- |
| Template usage audit            | Which templates are used vs ignored              | Any template unused for 30+ days — investigate      |
| Rendering spot check            | Test 1-2 templates in Litmus/Email on Acid       | Any new rendering break in top 5 email clients      |
| Build time tracking             | Average hours from request to send               | Build time creeping above baseline + 25%            |

**Quarterly Tasks:**

| Quarterly Task                | What to Review                                     | Action if Off-Track                                 |
| ----------------------------- | -------------------------------------------------- | --------------------------------------------------- |
| Full template library audit   | All templates still match brand guidelines         | Update templates with any brand changes             |
| Email client compatibility    | Run full cross-client test suite                   | Fix rendering issues from email client updates      |
| New use case assessment       | Are there email types without templates?           | Scope and build new templates if needed             |
| Process efficiency review     | Is the build process still being followed?         | Retrain if shortcuts are causing quality issues     |

**After First Business Cycle (30-60 days post-launch):**

- Measure actual email build time reduction vs baseline (target: 50%+)
- Review email engagement metrics (open rate, click rate) for template-sent emails vs pre-project sends
- Assess whether team is self-sufficient or needs additional training
- Key question: Are templates accelerating campaign velocity as expected?

**Refinement Triggers (when to re-engage):**

| Trigger                              | Threshold                                    | Response                                              |
| ------------------------------------ | -------------------------------------------- | ----------------------------------------------------- |
| Build time regression                | >25% increase from post-project baseline     | Investigate process compliance, retrain if needed     |
| Brand refresh                        | Logo, color, or font changes                 | Update all master templates, re-test rendering        |
| MAP platform upgrade                 | Major version update to HubSpot or Marketo   | Re-run cross-client tests, fix any breaking changes   |
| New template request volume          | 3+ new use cases identified in a quarter     | Scope template expansion project                      |

**Every 6-12 Months:**

- Full template library refresh: update designs for current email trends, add new content block types
- Email client landscape review: new clients (e.g., new Outlook versions) may require template adjustments
- Competitive benchmark: review competitor emails for design inspiration and identify gaps

---

### 4b. Internal Handoff (SME -> Architect)

> **Purpose:** Transfer context so Architect can manage ongoing template relationship.

**What the Architect needs to know:**

- What was built: template inventory, design system decisions, MAP folder structure
- Customer context: who the email marketers are, their skill level, brand sensitivity
- Common issues: Outlook rendering quirks, dark mode workarounds, specific template limitations
- When to escalate back to SME: new template type builds, major design system changes, MAP migration
- **Maintenance schedule** (if Dedicated engagement — Architect runs this)

**Escalation guidelines:**

| Issue Type                                           | Who Handles           | Example                                          |
| ---------------------------------------------------- | --------------------- | ------------------------------------------------ |
| Content block tweaks, minor rendering fixes          | Architect             | "Footer social icons are misaligned in Apple Mail"|
| New template types, design system changes            | SME                   | "We need a webinar registration template"         |
| MAP platform issues, email deliverability problems   | SME                   | "Templates stopped rendering after HubSpot update"|

**For Dedicated engagements:** Architect also receives the maintenance schedule (4a) and becomes responsible for executing it. SME walks Architect through each maintenance task.

---

### 4c. External Handoff

> **Purpose:** Formal project completion with customer.

**Final project meeting:**

- Review complete template library (walk through each template and its use case)
- Demo the email build process one final time
- Walk through documentation package
- Confirm nothing outstanding
- Answer final questions
- Make it explicit: "Project complete"
- **For Single Project engagements:** Hand over the maintenance schedule (4a) and walk the customer through monthly/quarterly tasks

**Documentation package:**

- Template library overview (which template, which use case, when to use)
- Template customization guide (editable sections, safe modifications, common mistakes)
- Content block reference with image specifications
- Email build process runbook (step-by-step with screenshots)
- QA checklist for pre-send verification
- Training video walkthrough recordings
- FAQ document (compiled from training + hypercare)
- Template style guide (brand elements, spacing, typography)
- Maintenance schedule (for Single Project engagements)

**For Single Project engagements:** Walk the customer through the maintenance schedule in detail. Record a video walkthrough of the session. Make sure they understand what to check, how often, and when to re-engage.

**Output:** Customer owns the template system. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location (template specs, design files, QA results)
- [ ] Handoff documentation complete
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized
- [ ] Baseline metrics documented (pre-project build time vs post-project build time)

#### Internal Debrief (Optional but Recommended)

- What went well? (e.g., clean brand assets sped up build, strong stakeholder engagement)
- What would we do differently? (e.g., should have tested dark mode earlier, underestimated Outlook quirks)
- Any learnings to feed back into SOPs? (e.g., add Outlook-specific CSS patterns to template library)

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell -> Downsell -> Retry  |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (ongoing email ops support, template updates, QA)
   | if no
   v
2. Downsell: Email nurture program project, email deliverability optimization, or subscription/compliance project
   | if yes
   v
3. Retry retainer at end of next project cycle
```

**Script:**

> "Now that your email template library is live, there are two ways we can continue. Option 1: We can handle ongoing template updates, new template builds, and email QA through managed services. Option 2: If you have a specific project like setting up nurture programs or improving deliverability, we can scope that out. Which sounds more interesting?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On \[date ~quarter out\], we'll review how the template library is performing — template usage, build times, any new use case requests — and see if adjustments are needed."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                                 |
| ------------------- | ------------------------------------------------------------ |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks             |
| 2. Review metrics   | Pull template usage data, build time trends, engagement metrics|
| 3. Decide ownership | Can Architect handle this check-in, or need SME?            |
| 4. Prep materials   | If SME needed, brief them. If Architect, prep talking points.|

**At the refinement check-in:**

- Review template usage and build time metrics against baseline
- Identify new use cases or template gaps
- If minor: Architect builds additional templates
- If major: Scope template expansion project (restart the assembly line)

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- Template requirements document (approved use cases, content blocks, personalization specs)
- Current state email audit report with quality scores
- Modular design system documentation (block library, layout variations, responsive specs)

**Technical Deliverables:**

- 5-10 modular, responsive email templates built in MAP (HubSpot or Marketo)
- Dynamic content configuration (lifecycle stage, industry, region-based content swapping)
- Personalization token setup with fallback values
- MAP folder structure for template organization
- Cross-client rendering test results with screenshot library

**Documentation Package:**

- Template overview guide (which template for which use case)
- Template customization guide (editable vs locked, safe modifications)
- Content block reference with image specifications
- Email build process runbook (request to send, step-by-step)
- QA checklist for pre-send verification
- Training video walkthrough recordings (library walkthrough, build process demo)
- FAQ document
- Template style guide (brand elements, spacing, typography)
- Maintenance schedule

---

## Appendix: Reference Guide

### How to Use This Playbook

This is the **implementation playbook** — the step-by-step execution guide for delivering Email Operations: Templates &amp; Build Process from first contact to project close. It is the third file in a 3-file playbook structure:

| File                  | Purpose                                                                  |
| --------------------- | ------------------------------------------------------------------------ |
| `1-advisory.md`       | What the project IS — positioning, outcomes, approaches                  |
| `2-methodology.md`    | HOW we think about the problem — frameworks, concepts, best practices    |
| `3-implementation.md` | WHAT to DO — step-by-step execution with checklists                     |

#### What Each Phase Produces

| Phase                    | Output                                                                 | Gate Criteria                                                                  |
| ------------------------ | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **Phase 1: Strategy**    | Signed-off template requirements + design system + build process plan  | Marketing leadership has approved template scope and architecture              |
| **Phase 2: Engineering** | Built and tested template library in MAP                               | All templates render correctly, accessibility passed, customer approved        |
| **Phase 3: Enablement**  | Trained team with documentation                                        | Team has built 3+ production emails independently during hypercare             |
| **Phase 4: Handoff**     | Independent customer + archived project                                | Documentation delivered, maintenance plan in place, project closed             |

#### Phase Weight

| Phase Weight  | Strategy | Engineering | Enablement | Handoff |
| ------------- | -------- | ----------- | ---------- | ------- |
| This project  | 15%      | 60%         | 15%        | 10%     |

**Key adaptation:** The number of templates varies by client (5-10 is the standard range). Scope this in Phase 1. Do not over-build — start with templates covering 80% of use cases and iterate.

---

### Phase 1 Notes: Strategy

#### Why Phase 1 Matters

Marketing teams have strong opinions about email design. Rushing to build without alignment causes rework. Phase 1 forces agreement on template types, design system, and governance before any MAP work begins. The audit baseline also creates the "before" metric needed to demonstrate build time reduction.

#### Pre-Kickoff: The Two-Swarm Pattern

| Swarm                | Source                                                  | Goal                                          |
| -------------------- | ------------------------------------------------------- | --------------------------------------------- |
| **Swarm 1: Extract** | MAP template inventory, recent email sends, intake form | Understand current state, identify gaps        |
| **Swarm 2: Enrich**  | Email design best practices, cross-client compatibility data | Anchor recommendations in what works          |

**Result:** v0 template requirements are 70% pre-filled. Customer reacts and corrects, does not create from scratch.

---

### Phase 2 Notes: Engineering

#### Engineering Sub-Phase Flow

```
+-----------------+-----------------+-----------------+-----------------+
|  2a TECH SPEC   |  2b ENG HANDOFF |  2c BUILD       |  2d TEST        |
|                 |                 |                 |                 |
|  Map design     |  Review meeting |  Build templates|  Cross-client   |
|  system to MAP  |  Architect +    |  in MAP, config |  rendering +    |
|  module syntax  |  Engineer       |  dynamic content|  accessibility  |
+-----------------+-----------------+-----------------+-----------------+
|  OUTPUT:        |  OUTPUT:        |  OUTPUT:        |  OUTPUT:        |
|  MAP-specific   |  Approved       |  Complete       |  Tested +       |
|  tech spec      |  tech spec      |  template       |  approved       |
|                 |                 |  library        |  system         |
+-----------------+-----------------+-----------------+-----------------+
```

#### Key Principles

**Tech Spec (2a):** The critical translation is design system -> MAP module syntax. HubSpot and Marketo handle modules differently. Get this right and the build is fast. Get it wrong and you rebuild.

**Build (2c):** Build the master template first. All individual templates inherit from it. This ensures brand consistency and makes future updates efficient — change the master, update all templates.

**QA (2d):** Email marketing generates $36-$42 for every $1 spent [5], but broken rendering destroys that ROI. Test in 90+ clients. Outlook desktop is the most problematic — always test there first.

---

### Phase 3 Notes: Enablement

#### Key Principles

**Training Prep (3a):** The build process runbook is the most important training asset. Templates are only useful if the team follows a consistent process to use them. Document every step from "I need to send an email" to "email deployed."

**Hands-on Training (3b):** Do not lecture. Have each participant build an email from a template during the session. Friction discovered in training is friction prevented in production.

**Hypercare (3c):** The first 2 weeks of production use will surface edge cases the QA process missed. Common: "I need a layout that doesn't exist in the current blocks" and "this looks different in my Outlook than in the test." Office hours pattern works well — put recurring time on calendar, anyone can join.

---

### Phase 4 Notes: Handoff

#### Why Maintenance Matters for Templates

The most common failure mode is not broken templates — it is template drift. Marketing team members start editing master templates, adding one-off sections, breaking the modular system. The maintenance schedule includes governance checks specifically to prevent this.

Email clients also update their rendering engines. An email that looked correct in Gmail six months ago may not render correctly after a Gmail update. Quarterly rendering spot checks catch these issues before they affect live sends.

#### Internal Handoff: What Makes This Project Unique

The Architect must understand the MAP-specific implementation details, not just the design system. Key context: which CSS hacks were used for Outlook, where the brand assets live in the file manager, and what the dynamic content rules are. Without this, the Architect cannot troubleshoot rendering issues.

#### Retention: Natural Expansion Paths

Email templates are a foundation project. Once templates are in place, natural next projects include:
- **Email nurture programs** — use the templates to build automated nurture sequences
- **Email deliverability optimization** — ensure the emails actually reach the inbox
- **Subscription and compliance management** — manage opt-in/opt-out, preference centers, regulatory compliance
- **Marketing automation platform optimization** — expand MAP capabilities beyond email

---

## References

[1] [Marketo Success Series: Email Templates](https://nation.marketo.com/t5/product-blogs/marketo-success-series-email-templates/ba-p/314007) — Marketo recommends starting with a core set of modular templates covering primary use cases before expanding.

[2] [Email on Acid: Accessibility and Dark Mode](https://www.emailonacid.com/blog/article/email-development/accessibility-and-dark-mode-the-latest-buzz-words/) — Over 80% of smartphone users enable dark mode, and automatic color inversion can break email designs that were accessible in light mode.

[3] [WCAG 2 Overview - W3C](https://www.w3.org/WAI/standards-guidelines/wcag/) — WCAG Level AA requires a minimum contrast ratio of 4.5:1 for normal text and 3:1 for large text.

[4] [Email on Acid vs Litmus Testing Comparison](https://emailwarmup.com/blog/email-on-acid-vs-litmus/) — Both platforms provide previews for 70-90+ email clients and devices, enabling cross-client rendering validation without manual test sends.

[5] [Omnisend Email Marketing Statistics 2026](https://www.omnisend.com/blog/email-marketing-statistics/) — Email marketing generates between $36 and $42 for every $1 spent, representing a 3,600-4,200% ROI.

[6] [HubSpot Email Design Best Practices](https://blog.hubspot.com/marketing/email-design) — Maintain brand consistency by documenting your email style guide and creating modular templates that lock down branded elements.

[7] [Knak Guide to Marketo Email Templates](https://knak.com/blog/guide-to-marketo-email-templates/) — Marketo Email 2.0 modules function as building blocks allowing users to create fully designed emails from reusable components.
