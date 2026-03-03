# Rules of Engagement Design — Advisory

## 1) Project Overview

### What is the name of this project?

Rules of Engagement Design - Sales Ownership & Dispute Resolution Policy

### What is the purpose of this project?

This project creates a comprehensive, enforceable set of policies defining how sales representatives interact with leads, accounts, and opportunities. It produces a documented ROE covering ownership rules for every deal scenario (inbound, outbound, expansion, partner), a dispute resolution process with clear escalation paths and SLAs, and CRM enforcement configurations that automate rule compliance.

**Core transformation:** From ad hoc, tribal-knowledge ownership decisions that breed conflict and slow deals, to a codified, CRM-enforced system where every rep knows exactly who owns what -- and disputes resolve in hours, not weeks.

### What Rules of Engagement Design Unlocks

After this project is complete, the sales organization can:

- Assign ownership for any deal scenario without manager intervention
- Resolve disputes within 24-48 hours through a documented escalation path instead of weeks of Slack threads
- Enforce ownership rules automatically through CRM validation and automation
- Onboard new reps with clear, written guidelines instead of relying on tribal knowledge
- Track and report on dispute frequency, resolution time, and fairness metrics

| Before                       | After                     |
| ---------------------------- | ------------------------- |
| Reps argue over who owns an account; manager spends hours mediating | Written if/then rules resolve 80%+ of scenarios without escalation |
| New reps cold-call accounts already being worked by a colleague | CRM alerts flag potential ROE violations before outreach happens |
| Customers get contacted by multiple reps from the same company | Single-owner model with clear handoff rules prevents duplicate outreach |
| Upsell/expansion ownership is unclear between AE, CSM, and AM | Documented boundaries define who owns what at each stage of the customer lifecycle |
| Partner deals stall because nobody knows who gets credit | Deal registration windows and sourced-vs-influenced rules are published and enforced |

### What business outcomes does this project drive?

**Primary Outcomes:**

- Reduced ownership disputes escalated to management (target: 50% reduction within 30 days of rollout)
- Faster deal progression -- no more stalled opportunities while ownership is debated
- Improved rep morale and reduced voluntary turnover driven by perceived fairness

**Secondary Outcomes:**

- Foundation for territory redesign projects (clean ROE is a prerequisite for territory changes)
- Improved forecasting accuracy -- clear ownership means cleaner pipeline data
- Better customer experience through single-thread communication
- Data for future compensation plan design (ROE clarifies who earns credit)

### Who in the Org can benefit from this project?

VP of Sales, CRO, Sales Managers, Account Executives, SDRs/BDRs, Account Managers, Customer Success Managers, RevOps/Sales Ops Manager, Channel/Partner Manager

### Pain Points this Project Solves

Rules of Engagement Design is foundational infrastructure for a functional sales organization. The specific pain it solves depends on the organization's scale and GTM complexity, but most clients experience several of these simultaneously.

| Pain Point              | What Rules of Engagement Design Enables  |
| ----------------------- | ---------------------------- |
| "Our managers spend 5+ hours per week arbitrating ownership disputes" | Documented if/then rules resolve most scenarios without escalation; disputes that do escalate have a defined SLA and final arbiter |
| "We lose deals because two reps reach out to the same prospect" | CRM enforcement flags duplicate outreach and assigns clear single ownership |
| "New reps don't know who owns what -- they rely on asking around" | Published ROE document with concrete examples for every scenario eliminates tribal knowledge dependency |
| "Our reps think the system is unfair, and we're losing good people" | Transparent, written rules with visible leadership sign-off build trust; appeal process handles edge cases |
| "Partner deals are a mess -- nobody knows who gets credit" | Deal registration windows, sourced-vs-influenced credit rules, and split mechanisms are defined up front |
| "We can't do territory changes because ownership rules are unclear" | ROE provides the policy foundation that territory design depends on |

### The Data Behind the Problem

The cost of unclear rules of engagement is measurable across multiple dimensions:

**Rep productivity loss:** Sales reps spend only 28% of their time actually selling [1]. Administrative overhead -- including ownership disputes, CRM hygiene, and internal negotiation -- consumes the majority of rep time. Every hour a rep spends arguing over account ownership is an hour not spent in pipeline.

**Territory and ownership conflict frequency:** 58% of B2B companies rate their territory design efforts as ineffective [2], and territory overlap is a primary driver of ownership disputes. When industries and geographies overlap, reps waste time debating boundaries instead of selling.

**Turnover driven by perceived unfairness:** Average annual B2B sales rep turnover is 13.9% [3], and unbalanced territories and unclear ownership rules are a contributing factor. With commission often representing 50% or more of total compensation [4], ownership disputes directly impact rep income and retention.

**Productivity upside of clear rules:** Organizations that design well-structured territory and ownership models see up to 25% improvement in salesperson productivity [2], primarily by eliminating ambiguity and reducing time spent on non-selling activities.

### Key Metaphors or Frameworks

**The "Traffic Laws" metaphor:** Rules of engagement are like traffic laws for your sales organization. Without them, every intersection (overlapping accounts, segment boundaries, partner deals) becomes a negotiation. With them, everyone knows who has right-of-way, and disputes are the exception rather than the norm. Use this when clients resist the documentation effort -- "You wouldn't drive without traffic laws; you shouldn't sell without ROE."

**When NOT to use it:** Avoid this metaphor with clients who view ROE as punitive or restrictive. For those teams, frame ROE as "removing ambiguity" rather than "enforcing rules."

### Target Motion

Sales-led growth (SLG) organizations with multiple reps, segments, or channels are the primary fit. The project is most critical for organizations with:

- Multiple sales roles touching the same accounts (AE + CSM + AM)
- Both inbound and outbound motions running simultaneously
- Named account or territory-based selling
- Channel/partner programs generating co-sell or deal registration scenarios

*Not a fit for:* Solo-founder sales (one person selling), pure PLG with no sales team, or organizations with fewer than 3 sales reps where informal communication is sufficient.

### Common Belief Barriers

**"We don't need this written down -- our team just knows the rules."** -- Tribal knowledge breaks the moment you hire a new rep, promote someone, or have a disputed deal. If the rules aren't documented, they don't exist -- they're just opinions. Every scaling sales team we've worked with has at least 3-5 active ownership disputes that could have been prevented by written ROE.

**"This will slow our reps down with bureaucracy."** -- The opposite is true. Reps currently waste time in Slack threads, manager 1:1s, and all-hands debates about ownership. Clear ROE eliminates that overhead. The goal is fewer meetings about "who owns this," not more.

**"We tried this before and nobody followed the rules."** -- That usually means the rules were either too vague, not enforced in the CRM, or rolled out without team buy-in. This project addresses all three: specific if/then language, CRM automation, and a structured rollout with rep acknowledgment.

---

## 2) Tools & Systems

### Primary Tools

**Salesforce**

Primary CRM for ROE enforcement. Used for: ownership assignment automation, validation rules preventing unauthorized ownership changes, workflow alerts for potential ROE violations, dispute tracking reports and dashboards. Salesforce Enterprise Territory Management 2.0 provides the native framework for territory-based ownership rules [5].

**HubSpot**

Alternative CRM for ROE enforcement. Used for: contact/company ownership automation via workflows, deal pipeline ownership rules, rotation and round-robin assignment for inbound leads. HubSpot's workflow engine handles ownership timeout automation and reassignment logic.

**LeanData**

Lead-to-account matching and routing platform. Used in ROE enforcement to match inbound leads to existing accounts, ensuring the right owner gets the lead automatically rather than relying on manual checks. Critical for preventing inbound leads from going to the wrong rep when an account is already owned.

**Google Docs / Notion / Confluence**

Documentation platform for the ROE policy document itself. The final deliverable must live in a location accessible to all reps and be version-controlled to track changes over time.

---

## 3) Stakeholders & Roles

### Client-Side Stakeholders

**VP of Sales (Executive Sponsor)**

- Required for: Discovery interviews, leadership review session, final sign-off
- Responsibilities: Approves final ROE document, serves as final arbiter for dispute resolution process, champions rollout to team

**CRO (Executive Sponsor -- if applicable)**

- Required for: Initial scoping, final approval on cross-functional rules (Sales vs. CS vs. Partners)
- Responsibilities: Ensures ROE aligns with overall GTM strategy; resolves any cross-departmental disputes about scope

**Sales Managers (Input Providers + Approvers)**

- Required for: Discovery interviews, leadership review session, rollout meeting
- Responsibilities: Provide frontline perspective on dispute frequency and common scenarios, validate that proposed rules would have resolved past disputes, enforce ROE post-rollout

**RevOps / Sales Ops Manager (Technical Owner)**

- Required for: All phases -- discovery through handoff
- Responsibilities: Provides CRM access, supplies dispute data, owns ongoing ROE maintenance and quarterly reviews

**Sales Reps (Input Providers)**

- Required for: Discovery interviews (3-5 reps), rollout meeting, acknowledgment
- Responsibilities: Share frontline frustrations, validate proposed rules against real scenarios, acknowledge final ROE

### Technical Owners

**RevOps / Sales Ops Manager**

- Owns CRM enforcement configurations post-handoff
- Manages ongoing dispute tracking report/dashboard
- Runs quarterly ROE review process
- Proposes ROE amendments as organization evolves

**CRM Administrator (If Separate from RevOps)**

- When this role is needed: Organizations where RevOps does not have Salesforce admin access
- What they handle: Validation rule deployment, Flow automation, Territory Management configuration

**Enterprise Considerations (If Applicable)**

- Legal review may be required if ROE ties to compensation or employment terms
- Multiple regional sales leaders may need to approve region-specific rules
- IT security review if CRM automation changes affect data access controls

---

## 4) Scoping

### Scoping Factors

**1. Number of Sales Segments**

- Single segment (e.g., all AEs sell to one market) --> Simpler ROE with fewer ownership handoff scenarios
- Multiple segments (SMB, Mid-Market, Enterprise) --> Requires segment handoff rules, boundary definitions, and escalation for accounts that change segment

**2. Sales Roles Involved**

- AEs only --> Straightforward ownership rules (who opens, who owns)
- AE + SDR/BDR --> Requires meeting-booked handoff rules and SLA for follow-up
- AE + CSM + AM --> Requires upsell/expansion ownership boundaries, renewal ownership, and cross-sell rules
- All of the above + Partner Manager --> Full complexity with channel deal registration and co-sell rules

**3. GTM Motion Mix**

- Inbound only --> Focus on round-robin/territory assignment and account matching
- Outbound only --> Focus on named account protections and prospecting boundaries
- Inbound + Outbound --> Requires rules for when inbound leads hit accounts being actively prospected outbound (most common conflict trigger)

**4. Partner/Channel Involvement**

- No partners --> Eliminates an entire scenario category
- Active partner program --> Requires deal registration windows, sourced-vs-influenced credit rules, co-sell engagement rules

**5. CRM Platform and Maturity**

- Salesforce with clean data --> Full CRM enforcement is feasible
- HubSpot with clean data --> Enforcement via workflows; some limitations on territory management
- CRM with poor data quality --> Data cleanup may be needed before enforcement rules can work

**6. Existing ROE Documentation**

- No existing ROE --> Full build from scratch (higher effort, 60-80 hours)
- Existing but outdated/incomplete ROE --> Audit and update (moderate effort, 40-60 hours)
- Existing ROE that needs CRM enforcement only --> Configuration focus (lower effort, 30-50 hours)

### Multiple Approaches

**Approach 1: Full Build**

- Criteria: No existing ROE, or existing documentation is so outdated/vague it's functionally useless. Multiple segments and roles involved.
- Execution: Full discovery with stakeholder interviews, complete scenario mapping, draft from scratch, leadership review, team rollout, CRM enforcement build

**Approach 2: Audit & Update**

- Criteria: Existing ROE documentation covers some scenarios but has gaps (e.g., no partner rules, no segment handoff rules, no escalation process). Team has grown since last update.
- Execution: Gap analysis against current team structure, update and expand existing document, add missing scenarios, strengthen CRM enforcement

**Approach 3: Enforcement-Only**

- Criteria: Written ROE exists and is current, but it's not enforced in the CRM. Reps follow rules inconsistently because there's no automation.
- Execution: Map existing rules to CRM configurations, build validation rules and automation, create monitoring dashboards, minimal document updates

---

## 5) Discovery Questions

### Questions for Project Kickoff

**Business Context**

- How many sales reps do you have, and how are they segmented? *(Determines scope and number of scenarios)*
- What's your GTM motion mix -- primarily inbound, outbound, or both? *(Drives which scenario categories to prioritize)*
- Do you have a channel/partner program? If so, how active is it? *(Determines if partner ROE is in scope)*
- When was the last time you hired a batch of new reps? *(Recent hires often surface ROE gaps fastest)*

**Current State**

- Do you have any written ROE today -- even informal wiki pages or Slack posts? *(Establishes starting point)*
- How many ownership disputes come up per month, roughly? *(Quantifies the problem)*
- How are disputes resolved today? Who makes the call? *(Reveals if an informal process exists)*
- What's the most common type of dispute -- inbound overlap, outbound poaching, upsell ownership, or something else? *(Prioritizes scenario mapping)*
- Have you lost any reps in the past year who cited unfairness or territory issues? *(Connects ROE to retention)*

**Technical Environment**

- Which CRM are you on -- Salesforce or HubSpot? What edition? *(Determines enforcement options)*
- Do you use a routing tool like LeanData, Chilipiper, or native CRM routing? *(Affects inbound assignment rules)*
- How clean is your CRM data -- specifically account hierarchy, industry, and revenue fields? *(Determines if CRM enforcement is immediately feasible)*
- Do you have a CRM admin or does RevOps handle administration? *(Identifies the technical counterpart)*

**Expectations**

- What does "done" look like for you? A document, CRM enforcement, or both? *(Scopes deliverables)*
- Who is the final decision-maker on ROE? *(Identifies the approval gate)*
- Are there any scenarios you already know are contentious? *(Gets ahead of political landmines)*
- What's your timeline -- is this tied to a new territory plan, hiring wave, or comp cycle? *(Drives urgency and phasing)*

### Information to Gather Before Implementation

**Dispute Data:**

Pull Salesforce/HubSpot data on ownership changes, opportunity reassignments, and duplicate contacts/leads from the past 90 days. Also collect any Slack threads or email chains about disputed deals.

**Team Structure:**

Complete org chart of customer-facing roles: AEs, SDRs, CSMs, AMs, Partner Managers. Include segment assignments (SMB/MM/Enterprise) and any named account lists.

**Existing Documentation:**

Any written ROE, territory plans, compensation plan documents that reference ownership, or onboarding materials that describe "how we sell."

**CRM Access:**

Admin-level access to Salesforce or HubSpot for the Engineer to audit current automation, validation rules, and territory settings.

### Approach Decision Questions

| Question     | Answer --> Approach                                    |
| ------------ | ---------------------------------------------------- |
| Do you have any written ROE today? | No or unusable = Full Build, Partial = Audit & Update, Yes and current = Enforcement-Only |
| Is the main problem "we don't have rules" or "we have rules but they're not enforced"? | No rules = Full Build, Not enforced = Enforcement-Only |
| How many segments and roles touch deals? | 1 segment + AEs only = Simpler scope, Multiple segments + AE/CSM/AM/Partner = Full complexity |
| Is a partner/channel program in scope? | Yes = adds 15-20 hours for partner-specific scenarios, No = standard scope |

---

## 6) Overcoming Common Belief Barriers

#### "We don't need this written down -- our team just knows the rules."

Every sales team under 10 people believes this. It works until it doesn't. The breaking point is predictable: a new hire's first disputed deal, a rep transfer between segments, or a manager leaving who was the "source of truth." At that point, the absence of written ROE becomes an urgent crisis instead of a planned project.

The data supports this: 58% of B2B companies rate their territory design as ineffective [2], and the root cause is often that ownership rules were never documented in the first place. Tribal knowledge scales to about 5-8 reps before it starts generating 2-3 disputes per week.

**The reframe:** "Your team knows *their version* of the rules. The question is whether all versions match. We find that when we interview 5 reps separately, we get 3-4 different answers about who should own a given scenario."

#### "This will slow our reps down with bureaucracy."

This objection comes from confusing documentation with process overhead. Written ROE doesn't add steps to the sales process -- it removes the unplanned interruptions that happen when ownership is ambiguous. Reps currently spend time in Slack threads asking "is this my account?", waiting for manager rulings, and avoiding outreach to accounts they're unsure about.

Sales reps already spend only 28% of their time selling [1]. The rest is administrative overhead, internal communication, and CRM work. Clear ROE reduces the "internal negotiation" portion of that overhead.

**The reframe:** "ROE doesn't add process -- it removes the hidden process you already have. Right now, every ambiguous deal triggers an ad hoc process of Slack messages, manager calls, and delayed outreach. Written ROE replaces that with a 30-second lookup."

#### "We tried this before and nobody followed the rules."

This is the most important objection to handle well, because it's usually rooted in real experience. The three failure modes for previous ROE attempts are:

1. **Rules were too vague.** "The AE owns the account" doesn't help when an SDR books a meeting at a CSM's account. If/then language with specific examples is required.
2. **No CRM enforcement.** If the CRM allows behavior that violates the ROE, the ROE is optional. Validation rules, automation, and alerts make compliance the path of least resistance.
3. **No buy-in process.** Rules imposed without rep input feel punitive. This project includes rep interviews during discovery and a structured rollout with Q&A.

**The reframe:** "What specifically broke last time? We'll design around those failure modes. Usually it's one of three things: vague rules, no CRM enforcement, or no buy-in process. We address all three."

#### "Our sales team is too small to need this."

Organizations with 3-5 reps often believe ROE is only for large teams. But the cost of a single disputed deal at a startup ($50K-$200K ACV) is proportionally much larger than at an enterprise company. And writing ROE early -- before it's urgent -- takes 30-40% less effort than writing it during a crisis.

**The reframe:** "The best time to write ROE is before you need it. You're hiring, which means every new rep joining without clear rules increases dispute risk. Writing it now takes 40 hours. Writing it after a blown deal takes 40 hours plus whatever that deal was worth."

---

## 7) Metrics Impact & Success Measurement

### Power 10 Metrics Impacted

| Power 10 Metric | Impact Direction        | Expected Magnitude     | Notes                         |
| --------------- | ----------------------- | ---------------------- | ----------------------------- |
| Opp-to-CW Conversion Rate | Increase | +5-15% | Deals no longer stall while ownership is debated; faster progression through pipeline |
| Sales Cycle Length | Decrease | -10-20% | Eliminates ownership-dispute delays that add days or weeks to deal cycles |
| Pipeline Production | Increase | +10-20% | Reps prospect with confidence knowing which accounts are theirs; less hesitation on outreach |
| Rep Productivity (Revenue/Rep) | Increase | +15-25% | Well-designed ownership models can boost productivity by up to 25% [2] |

### Expected Outcomes

| Metric                 | Before          | After            | Source        |
| ---------------------- | --------------- | ---------------- | ------------- |
| Ownership disputes per month | 8-15 (typical for 20-person team) | 2-4 | LeanScale project benchmarks |
| Time to resolve a dispute | 3-7 days (Slack threads + manager intervention) | 24-48 hours (documented SLA) | ROE escalation SLA |
| Manager time on dispute arbitration | 5+ hours/week | &lt;1 hour/week | Discovery interviews + post-project tracking |
| Rep confidence in ownership clarity | Low (varies by tenure) | High (measured via quarterly survey) | Pre/post rollout survey |
| CRM ownership data accuracy | Inconsistent (manual, tribal) | Automated enforcement | CRM audit pre/post |

### How to Measure Success

**Leading Indicators (Early signals, Week 1-4):**

- Reduction in ownership dispute Slack messages and manager escalations (track volume weekly)
- All reps have signed/acknowledged the ROE document (100% completion within 2 weeks)
- CRM enforcement rules are active and firing (monitor validation rule trigger count)
- Zero "who owns this?" questions in team Slack channels

**Lagging Indicators (Proof of success, Month 2-6):**

- 50%+ reduction in ownership disputes escalated to management within 30 days
- Zero ambiguous ownership situations causing deal delays or lost revenue within 90 days
- Rep satisfaction with ownership fairness in quarterly survey (target: 80%+ positive)
- Reduced voluntary rep turnover attributable to territory/ownership frustration
- ROE quarterly review cadence established and running (first review completed within 90 days)

---

## References

[1] [Salesforce - State of Sales Report (2024)](https://www.salesforce.com/resources/research-reports/state-of-sales/)
[2] [Highspot - Sales Territory Management: Planning Tips](https://www.highspot.com/blog/sales-territory-management/)
[3] [Alexander Group - Why Are Your Reps Leaving?](https://www.alexandergroup.com/insights/why-are-your-reps-leaving/)
[4] [Everstage - Sales Rules of Engagement Policy Document](https://www.everstage.com/revenue-operations/settling-disputes-between-reps-with-rules-of-engagement)
[5] [Salesforce Help - Enterprise Territory Management](https://help.salesforce.com/s/articleView?id=sales.tm2_intro.htm&language=en_US&type=5)
[6] [Gradient Works - Rules of Engagement Toolkit](https://www.gradient.works/resources/rules-of-engagement-for-sales)
[7] [InsideSales - Time Management for Sales Reps](https://www.insidesales.com/time-management-for-sales-reps/)
