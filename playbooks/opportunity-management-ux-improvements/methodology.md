# Opportunity Management UX Improvements — Methodology

This document covers the core concepts, frameworks, and calculations behind Opportunity Management UX Improvements. It provides the methodological foundation — the 'how it works' behind the execution steps.

---

## 1) Core Concepts

### The Rep-First Design Principle

*What is it?*

Rep-First Design means every layout decision starts from the question: "Does this help the rep close deals faster?" Rather than designing the opportunity page for management reporting needs or data completeness goals, the primary user -- the sales rep who updates records 10-50 times per day -- drives field placement, section structure, and workflow design. Management and reporting needs are still met, but through secondary mechanisms (default values, automations, archived sections) rather than by cluttering the rep's primary workspace.

*Why does it matter?*

Sales reps spend only 29-30% of their time actually selling, with 70-71% consumed by administrative tasks, data entry, and internal meetings [1][2]. When the CRM feels like busywork rather than a selling tool, reps abandon it. 40% of salespeople still use spreadsheets and email to store customer data rather than their CRM [3]. A rep-first design directly attacks this problem by reducing friction at the point of data entry, which improves both adoption and data quality simultaneously.

*Key insight:*

> If you optimize the opportunity page for the rep, management gets better data as a side effect. If you optimize for management, reps abandon the system and management gets no data at all.

*Examples:*

| Context | How Rep-First Design Applies |
|---------|------------------------------|
| Field placement | Amount, Stage, Close Date, and Next Step appear above the fold -- the fields reps update most. Legal entity name or billing address gets archived below. |
| Validation rules | Instead of 20+ required fields blocking saves, limit validation to 3-4 critical-path fields (Amount, Close Date, Stage). Use soft prompts for the rest. |
| Quick Actions | "Log Activity" and "Update Stage" are 2-click actions on the action bar, not buried in related lists. |

### Cognitive Load and CRM Interfaces

*What is it?*

Cognitive load refers to the total amount of mental effort required to use a system. In CRM design, cognitive load comes from three sources: (1) the number of fields displayed, (2) the complexity of deciding which fields matter, and (3) the navigation required to complete a task. When the opportunity page shows 60+ fields across 8 sections, the rep's brain must process and filter irrelevant information before finding the 5-6 fields they actually need to update.

*Why does it matter?*

Research in UX design confirms that when information volume exceeds a user's processing capacity, task completion slows, errors increase, and users disengage [4]. In CRM terms, this means reps skip fields, enter placeholder data ("TBD", "N/A"), or avoid the system entirely. The result is a self-reinforcing cycle: cluttered CRM leads to low adoption, which leads to poor data, which leads to more fields being added to "capture" data, which makes the CRM even more cluttered.

*The Framework:*

**Three levers to reduce CRM cognitive load:**

```
1. REMOVE    → Delete fields nobody uses (<10% completion)
2. HIDE      → Archive low-frequency fields into collapsed sections
3. SEQUENCE  → Show fields contextually based on stage or record type
```

*Common misunderstandings:*

- **Misconception:** Removing fields from the page layout deletes the data.
  **Reality:** Removing a field from a page layout only hides it from the UI. The data remains in Salesforce, accessible via reports, API, and other layouts. No data is lost.

- **Misconception:** More fields mean better data quality.
  **Reality:** Organizations with over-engineered validation rules (20+) see reps resort to Excel for pipeline tracking, destroying data quality entirely [5]. Fewer, better-placed fields with clear purpose drive higher completion rates.

### The Field Hierarchy Model

*What is it?*

The Field Hierarchy Model is a three-tier classification system for organizing opportunity fields based on usage frequency and business criticality. Every field on the opportunity object falls into one of three tiers:

| Tier | Name | Criteria | Placement |
|------|------|----------|-----------|
| Tier 1 | Must-Have | Used on 80%+ of records AND updated regularly | Top of page, above the fold |
| Tier 2 | Should-Have | Used on 30-80% of records OR needed for specific stages | Middle sections, visible but not prominent |
| Tier 3 | Archive | Used on &lt;30% of records, needed only for reporting or compliance | Collapsed section at bottom or removed from layout |

*Why does it matter?*

Without a systematic classification, field placement decisions become political ("My VP wants this field visible") rather than data-driven. The Field Hierarchy Model provides an objective framework that ties placement to actual usage data from Salesforce Optimizer or Field Trip [6]. This depersonalizes the conversation and makes stakeholder sign-off easier.

*Key insight:*

> Apply the "8 out of 10" rule: if a field is not filled on 80% of opportunity records, it does not belong above the fold. Period.

*Examples:*

| Tier | Typical Fields | Rationale |
|------|---------------|-----------|
| Tier 1 (Must-Have) | Amount, Stage, Close Date, Next Step, Owner | Updated on every deal, every interaction |
| Tier 2 (Should-Have) | Lead Source, Competitor, Product Line, Contract Term | Important for analysis but not updated daily |
| Tier 3 (Archive) | Legacy Migration ID, Data Import Flag, Old Region Code | Exist for historical reasons, never actively maintained |

### Progressive Disclosure in CRM

*What is it?*

Progressive disclosure is a UX pattern that presents only the information or options the user needs at a given moment, revealing additional detail on demand or as context changes. In Salesforce, this is achieved through three mechanisms: (1) collapsed sections that expand on click, (2) Dynamic Forms with conditional field visibility, and (3) Sales Path with stage-specific key fields.

*Why does it matter?*

A standard Salesforce page layout loads all fields regardless of whether the user needs them. Dynamic Forms only load required fields based on visibility rules, which can significantly improve page load times and reduce visual clutter [7]. Progressive disclosure turns a 60-field wall of inputs into a focused 10-field working view that expands when the rep needs more detail.

*Common misunderstandings:*

- **Misconception:** Dynamic Forms and page layouts are interchangeable.
  **Reality:** Dynamic Forms offer field-level conditional visibility evaluated live as the user edits. Page layouts are static per profile/record type. Dynamic Forms is the preferred approach for progressive disclosure but requires Lightning Experience and is not available on all standard objects (check Salesforce release notes for current support).

- **Misconception:** Hiding fields means reps will never fill them.
  **Reality:** Fields surfaced at the right stage with clear guidance (via Sales Path) see higher completion rates than fields visible at all times with no context. Relevance drives completion, not visibility alone.

### Guided Selling via Sales Path

*What is it?*

Salesforce Sales Path provides a visual indicator of an opportunity's current stage and includes stage-specific guidance: coaching tips, key fields, and exit criteria. It transforms the opportunity from a passive data-entry form into an active coaching tool that tells the rep what to do next at each stage.

*Why does it matter?*

Guided selling approaches have been shown to improve win rates by 10-20% and shorten sales cycles by up to 50% [8]. Sales Path delivers a lightweight version of guided selling natively in Salesforce, without requiring additional tools. The "Guidance for Success" text field at each stage can include exit criteria, key questions to ask, and common mistakes to avoid -- turning institutional sales knowledge into in-context coaching.

*Key insight:*

> Sales Path is not about tracking where a deal is. It is about telling the rep what to do to move it forward. If your guidance text is empty, you are using Sales Path as a status bar, not a coaching tool.

*Examples:*

| Stage | Guidance Content | Key Fields |
|-------|-----------------|------------|
| Discovery | "Confirm budget authority. Identify 3+ stakeholders. Document current pain." | Next Step, Contact Role, Decision Criteria |
| Proposal | "Ensure champion has seen pricing. Confirm timeline aligns with budget cycle." | Amount, Close Date, Competitor |
| Negotiation | "Legal review complete? Security questionnaire submitted? MSA redlined?" | Contract Term, Discount %, Legal Status |

---

## 2) Decision Frameworks

### Approach Selection Matrix

*When starting an Opportunity Management UX Improvements project, the first decision is scope. Use this matrix to determine which approach fits the client's situation.*

| Situation | Recommended Approach | Why |
|-----------|---------------------|-----|
| Single record type, &lt;50 fields, Lightning already enabled | **Light Touch** -- Page layout cleanup + compact layout + Sales Path | Low complexity, fast delivery (1-2 weeks), minimal risk |
| Multiple record types, 50-100 fields, some Dynamic Forms capability | **Standard Optimization** -- Full field audit + layout redesign + Quick Actions + Sales Path + Kanban | Most common scenario, 3-4 week delivery, moderate stakeholder alignment needed |
| 100+ fields, 5+ record types, Classic-to-Lightning migration in progress | **Full Transformation** -- Dynamic Forms + stage-based conditional visibility + custom Lightning components + phased rollout | High complexity, 6-8 week delivery, executive sponsorship required |
| HubSpot CRM (not Salesforce) | **HubSpot Layout Optimization** -- Property groups, required fields per stage, deal board customization | Different tooling but same principles apply; see HubSpot-specific edge case below |

### Scoping Factors

*These variables determine effort, approach, and risk. Assess each during discovery.*

**1. Number of Record Types**

- 1 record type --> Single layout redesign, straightforward
- 2-3 record types --> Multiple layouts, need to coordinate field consistency across types
- 4+ record types --> Audit whether all are necessary; often 2-3 can be consolidated

**2. Number of Opportunity Fields**

- &lt;30 fields --> Likely already manageable; focus on section organization and Quick Actions
- 30-60 fields --> Core optimization zone; expect to archive 30-40% of fields
- 60+ fields --> Significant cleanup required; expect 50%+ fields to move to archive or removal

**3. Validation Rule Count**

- 0-5 rules --> Healthy range; verify they are not blocking common workflows
- 6-15 rules --> Review each for necessity; likely 30-50% can be softened or removed
- 15+ rules --> Red flag for adoption problems; this is often the single biggest friction source

**4. Lightning vs. Classic**

- Lightning enabled --> Full feature set available (Dynamic Forms, Sales Path, Kanban, Quick Actions)
- Classic only --> Limited to page layout optimization; recommend Lightning migration as prerequisite
- Mixed (some users on Classic) --> Must design layouts that work in both; limits Dynamic Forms usage

**5. Salesforce Edition**

- Professional --> No Dynamic Forms, limited Quick Actions; use page layout sections and compact layouts
- Enterprise --> Dynamic Forms available for custom objects; standard object support varies by release
- Unlimited --> Full feature set available

### Light Touch Approach

*Best for:*
- Organizations that recently migrated to Lightning and need quick wins
- Teams with a single sales process and one record type
- Clients with limited budget or timeline (1-2 weeks)

*Not recommended for:*
- Organizations with systemic adoption issues beyond layout design
- Companies needing stage-based field visibility (requires Dynamic Forms)
- Teams with complex approval or validation workflows

*Key differences from Standard:*

| Aspect | Standard Optimization | Light Touch |
|--------|----------------------|-------------|
| Field audit | Full quantitative analysis with Salesforce Optimizer or Field Trip | Quick visual audit + rep interviews only |
| Dynamic Forms | Conditional visibility rules configured | Not used; page layout sections only |
| Pilot testing | 2-3 pilot users in sandbox for 1 week | Quick review with 1 rep before deployment |
| Training | Live session + recorded walkthrough + quick reference guide | Email walkthrough + Slack support |

### Standard Optimization Approach

*Best for:*
- Mid-market B2B SaaS companies ($10M-$100M ARR) with RevOps teams
- Organizations with 2-3 record types and 40-80 opportunity fields
- Teams where rep adoption is the primary pain point

*Not recommended for:*
- Companies where the sales process itself is undefined (fix process first, then UX)
- Organizations mid-migration to a new CRM (wait until migration completes)

*Key differences from Full Transformation:*

| Aspect | Standard Optimization | Full Transformation |
|--------|----------------------|---------------------|
| Duration | 3-4 weeks | 6-8 weeks |
| Dynamic Forms | Used for key sections | Fully conditional layouts per stage |
| Rollout | Big-bang to all users after pilot | Phased by team or region |
| Custom components | Not included | May include custom Lightning Web Components |

### Full Transformation Approach

*Best for:*
- Enterprise organizations with 100+ opportunity fields and 5+ record types
- Companies moving from Classic to Lightning as part of this project
- Situations where the opportunity page is a symptom of broader Salesforce tech debt

*Not recommended for:*
- Organizations without executive sponsorship for change management
- Teams that need results within 4 weeks
- Companies with unstable Salesforce environments (active migration, major release pending)

---

## 3) Benchmarks & Standards

### How to Use Benchmarks

*Benchmarks are guidelines, not rules. Always:*
1. Start with benchmark as baseline
2. Adjust based on client-specific data (field usage report from Salesforce Optimizer)
3. Validate against their actual numbers when available
4. Document deviations and rationale

### Field Usage & Completion Rates

| Metric | Low | Typical | High | Notes |
|--------|-----|---------|------|-------|
| Key field completion rate (Amount, Close Date, Stage) | &lt;70% | 80-90% | 95%+ | Below 70% indicates systemic adoption issues beyond layout |
| Overall field completion rate | &lt;40% | 50-70% | 85-90% | Industry target is 85-90% for key records [9] |
| Fields with &lt;10% completion | 30%+ of all fields | 15-25% | &lt;10% | Fields below 10% are removal candidates |
| Fields with identical values on &gt;80% of records | 10+ fields | 3-5 fields | 0-1 fields | These should be replaced with default values |

**Source:** Salesforce Optimizer benchmarks, Databar CRM data quality research [9].

**Interpretation:**
- **Below low:** CRM adoption is broken at a fundamental level. Layout redesign alone will not fix this -- investigate process, training, and management accountability gaps before proceeding.
- **Above high:** Organization already has strong data discipline. Focus on workflow speed (Quick Actions, Kanban) rather than field cleanup.

### Time-to-Update Benchmarks

| Metric | Low | Typical | High | Notes |
|--------|-----|---------|------|-------|
| Time to complete a full opportunity update | &gt;5 min | 2-4 min | &lt;2 min | Target is &lt;2 min post-optimization |
| Clicks to change opportunity stage | &gt;6 clicks | 3-5 clicks | 1-2 clicks | Kanban drag-and-drop = 1 click; Sales Path = 2-3 clicks |
| Clicks to log a post-call activity | &gt;8 clicks | 4-6 clicks | 2-3 clicks | Quick Action target = 2-3 clicks |

**Interpretation:**
- **Below low (&gt;5 min update time):** Reps are spending 1+ hour daily on CRM updates [10]. This is the strongest ROI argument for the project.
- **Above high (&lt;2 min):** Already near optimal. Look for marginal gains in Kanban views and mobile optimization.

### Adoption & Satisfaction Benchmarks

| Metric | Low | Typical | High | Notes |
|--------|-----|---------|------|-------|
| CRM user adoption rate | &lt;50% | 72% | 90%+ | Average CRM adoption among sales professionals is 72% [3] |
| Rep CRM satisfaction (1-5 scale) | &lt;2.5 | 3.0-3.5 | 4.0+ | Baseline survey before project; resurvey at 30 days |
| Opportunity update frequency (per opp per week) | &lt;1 | 1-2 | 3+ | Low frequency suggests reps batch updates rather than updating in real time |
| Validation rule error rate (per rep per week) | 10+ | 3-5 | &lt;2 | High error rates indicate over-engineered validation rules |

**Source:** CRM.org adoption statistics [3], Salesforce State of Sales [1].

### Quick Reference Thresholds

*For common "is this good?" questions:*

| Question | Good | Warning | Red Flag |
|----------|------|---------|----------|
| How many fields on the opportunity page? | &lt;25 visible | 25-40 visible | 40+ visible |
| How many validation rules on opportunities? | &lt;5 | 5-15 | 15+ |
| What % of fields are below 10% completion? | &lt;10% | 10-25% | 25%+ |
| How long does a full opp update take? | &lt;2 min | 2-5 min | 5+ min |
| What % of reps use the CRM daily? | 80%+ | 50-80% | &lt;50% |
| How many record types exist? | 1-2 | 3-4 | 5+ (audit for consolidation) |

---

## 4) Calculations & Scoring

### Formula Quick Reference

| Calculation | Formula | Example |
|-------------|---------|---------|
| Field Removal Impact Score | `Usage Rate x Report Dependency x Business Criticality` | A field with 5% usage, 0 report dependencies, and low criticality = safe to remove |
| Time Savings per Rep (daily) | `(Baseline Update Time - Target Update Time) x Updates per Day` | (4 min - 1.5 min) x 12 updates = 30 min saved per day |
| Annual Productivity Recovery | `Time Savings per Rep x Reps x Working Days x Hourly Cost` | 0.5 hrs x 30 reps x 250 days x $50/hr = $187,500 |

### Field Prioritization Score

**Formula:**
```
Field Priority Score = (Usage Rate x 40%) + (Update Frequency x 30%) + (Business Criticality x 30%)
```

**Variables explained:**
- `Usage Rate` = Percentage of opportunity records where this field is populated (from Salesforce Optimizer). Scale: 0-100.
- `Update Frequency` = How often the field value changes per opportunity lifecycle. Scale: 0-100 (daily change = 100, set-once = 20, never changed = 0).
- `Business Criticality` = Subjective rating based on reporting dependency and process requirement. Scale: 0-100 (required for forecast = 100, nice-to-have = 30, no downstream use = 0).

**Worked Example:**

*Scenario: Evaluating "Amount" field placement*

```
Given:
- Usage Rate = 95% (95)
- Update Frequency = High - changes multiple times per deal (80)
- Business Criticality = Required for forecasting and reporting (100)

Calculate:
- (95 x 0.40) + (80 x 0.30) + (100 x 0.30)
- 38 + 24 + 30
- Field Priority Score = 92 → Tier 1 (Must-Have)
```

**Validation:**
- Scores above 70 = Tier 1 (above the fold)
- Scores 30-70 = Tier 2 (middle sections)
- Scores below 30 = Tier 3 (archive or remove)
- If a field scores below 10, strongly consider full removal after confirming no report dependencies

### ROI Estimation

**Formula:**
```
Annual ROI = (Time Savings + Data Quality Improvement Value + Adoption Uplift Value) - Project Cost
```

**Variables explained:**
- `Time Savings` = Minutes saved per update x updates per day x reps x 250 working days x hourly cost / 60
- `Data Quality Improvement Value` = Estimated impact of improved forecast accuracy on revenue (typically 1-3% of pipeline value)
- `Adoption Uplift Value` = Additional pipeline visibility from reps who were not previously using CRM

**Worked Example:**

*Scenario: 30-rep sales team, $50M annual pipeline*

```
Given:
- Time saved per update: 2.5 minutes
- Updates per rep per day: 10
- Reps: 30
- Hourly cost (fully loaded): $60/hr
- Working days: 250

Time Savings:
- 2.5 min x 10 x 30 x 250 = 1,875,000 minutes = 31,250 hours
- 31,250 x $60 = $1,875,000 in productivity recovered

Data Quality (conservative 1% pipeline improvement):
- $50M x 1% = $500,000

Project Cost: ~$25,000-$40,000

Annual ROI: ~$2,335,000 - $40,000 = $2,295,000
```

*Note: These are illustrative figures.*

---

## 5) Edge Cases & Deep Dives

### Edge Case 1: Organizations with 5+ Record Types

*Scenario:*

The client has 5 or more opportunity record types (e.g., New Business, Renewal, Upsell, Partner Deal, Channel). Each record type has its own page layout, and they have diverged significantly over time. Some share 80% of fields; others are entirely different.

*Challenge:*

Redesigning 5+ page layouts independently creates a maintenance burden. Changes to shared fields must be replicated across every layout. Reps who work across deal types face inconsistent interfaces.

*Approach:*

1. Audit which record types are actually used (check record counts per type over the last 12 months)
2. Identify record types with &lt;5% of total opportunities -- candidates for consolidation
3. For remaining types, map field overlap. If 80%+ of fields are shared, use a single page layout with Dynamic Forms conditional visibility instead of separate record types
4. Where record types remain necessary (different approval processes, different stage definitions), create a shared "core" section that is identical across all layouts, with type-specific sections below

*Key validation:*

After consolidation, each remaining record type should serve a distinct sales process with meaningfully different stages or fields. If two record types differ by fewer than 5 fields, consolidate them.

### Edge Case 2: Classic-to-Lightning Migration in Progress

*Scenario:*

The client is partway through a Lightning migration. Some users are on Lightning Experience, others are still on Salesforce Classic. The Opportunity Management UX Improvements project is running in parallel.

*Challenge:*

Dynamic Forms, Sales Path, and Kanban views are Lightning-only features. Page layout changes affect both Classic and Lightning, but the experience differs significantly. Building for Lightning may break the Classic experience.

*Approach:*

1. Determine migration timeline. If full Lightning migration is &lt;3 months away, focus on page layout optimizations (which work in both) and defer Dynamic Forms to post-migration
2. If migration is 3-6 months out, build page layout optimizations now and plan a "Phase 2" Dynamic Forms enhancement post-migration
3. If migration has no timeline, design for page layouts only and build the business case for Lightning migration using this project's ROI data
4. Never deploy Dynamic Forms or Sales Path to a mixed environment -- they will not work for Classic users and create a two-tier experience

*Key validation:*

After deployment, verify the new layouts render correctly in both Classic and Lightning by testing with a user on each interface.

### Edge Case 3: Heavy Validation Rule Environment (15+ Rules)

*Scenario:*

The client has 15-30 validation rules on the Opportunity object, accumulated over years of "just add a required field" requests. Reps regularly encounter error messages when saving opportunities, leading to frustration and workarounds.

*Challenge:*

Validation rules cannot be addressed through layout changes alone. Even a perfectly designed layout will feel broken if reps hit 3-4 validation errors on every save. However, removing validation rules risks data quality regressions that concern management and reporting teams.

*Approach:*

1. Export all validation rules and their error message frequency (use Debug Logs or Error Tracking if available)
2. Categorize rules into three buckets:
   - **Keep:** Prevents genuinely invalid data (e.g., Close Date cannot be in the past for open opps)
   - **Soften:** Convert from hard error to warning or post-save alert (e.g., "Amount is $0 -- is this intentional?")
   - **Remove:** No longer relevant, redundant with other rules, or enforces an abandoned process
3. Implement changes in sandbox and measure: can a rep update a standard opportunity without hitting any errors in the common workflow?
4. Target: zero validation errors for the standard update path (stage change + close date + amount + next step)

*Key validation:*

Post-deployment, validation rule error frequency should drop by 50%+ within the first 30 days. If errors remain high, revisit the rules categorized as "Keep."

### Edge Case 4: HubSpot CRM (Not Salesforce)

*Scenario:*

The client uses HubSpot CRM instead of Salesforce. The same principles apply, but the tooling and terminology differ.

*Challenge:*

HubSpot does not have page layouts, Dynamic Forms, or Sales Path in the Salesforce sense. Its equivalent features have different capabilities and limitations.

*Approach:*

1. **Field hierarchy** --> Use HubSpot's property groups to organize deal properties. Create groups: "Deal Essentials," "Qualification Details," "Archived."
2. **Conditional fields** --> Use HubSpot's conditional property logic (available on Professional+ tiers) to show/hide properties based on pipeline stage
3. **Guided selling** --> Configure Deal Stage properties with required fields per stage and playbooks for stage-specific guidance
4. **Kanban view** --> HubSpot's Deal Board is the native equivalent; configure column properties and card display fields
5. **Quick Actions** --> HubSpot's record sidebar widgets and shortcuts serve a similar purpose

*Key validation:*

The deal board should display only 4-6 properties per deal card. Reps should be able to update a deal in &lt;2 minutes through the board view alone.

### Edge Case 5: Global Teams with Regional Layout Requirements

*Scenario:*

The client has sales teams in multiple regions (e.g., North America, EMEA, APAC) that require different fields, currencies, or compliance information on the opportunity page.

*Challenge:*

Creating separate page layouts per region quickly multiplies maintenance effort. Field names and picklist values may need localization. Compliance fields (e.g., GDPR consent, data residency) may be legally required in some regions but irrelevant in others.

*Approach:*

1. Design a "global core" layout with fields common to all regions (Amount, Stage, Close Date, Next Step, Owner)
2. Use Dynamic Forms conditional visibility to show region-specific fields based on the opportunity's region or the user's profile
3. For currency: use Salesforce multi-currency features rather than separate currency fields per region
4. For compliance fields: display them only for the relevant region using visibility rules tied to the Account's billing country or the user's role
5. Maintain a field registry document that maps each field to its region, owner, and business justification

*Key validation:*

Each regional user should see only the fields relevant to their region. No rep should see compliance fields for a region they do not serve.

---

## References

[1] [Salesforce State of Sales 2024](https://www.salesforce.com/news/stories/sales-research-2023/)
[2] [SPOTIO - 140+ Sales Statistics 2026 Update](https://spotio.com/blog/sales-statistics/)
[3] [CRM.org - 45 CRM Statistics You Need to Know in 2025](https://crm.org/crmland/crm-statistics)
[4] [Interaction Design Foundation - Cognitive Load](https://www.interaction-design.org/literature/topics/cognitive-load)
[5] [Salesforce State of Sales - Validation Rule Impact](https://www.salesforce.com/resources/research-reports/state-of-sales/)
[6] [Salesforce Ben - 5 Tips to Maximise Your Salesforce Page Layouts](https://www.salesforceben.com/5-tips-to-maximise-your-salesforce-page-layouts-improve-your-ux-ui/)
[7] [Salesforce Ben - Dynamic Forms Overview and Deep Dive](https://www.salesforceben.com/salesforce-dynamic-forms-overview-deep-dive-tutorial/)
[8] [Elfsquad - Boost Win Rates with Guided Selling](https://www.elfsquad.io/guided-selling)
[9] [Databar - The Complete Guide to CRM Data Quality](https://databar.ai/blog/article/the-complete-guide-to-crm-data-quality-metrics-standards-best-practices)
[10] [Salesforce - Sales Reps Spend Less Than 30% of Time Selling](https://www.salesforce.com/news/stories/sales-research-2023/)
