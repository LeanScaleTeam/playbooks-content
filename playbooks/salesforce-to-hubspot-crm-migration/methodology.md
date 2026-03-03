# Salesforce to HubSpot CRM Migration — Methodology

This document covers the core concepts, frameworks, and calculations behind the Salesforce to HubSpot CRM Migration playbook. It provides the methodological foundation — the 'how it works' behind the execution steps.

---

## 1) Core Concepts

*The mental models, frameworks, and key distinctions needed before executing a Salesforce to HubSpot migration.*

### CRM Data Model Divergence

*What is it?*

Salesforce and HubSpot store CRM data using fundamentally different data models. Salesforce uses an object-relational structure with Accounts, Contacts, Leads, and Opportunities as distinct objects connected by lookup and master-detail relationships. HubSpot uses an association-based model where Companies, Contacts, and Deals are connected through flexible associations rather than rigid parent-child hierarchies [1].

*Why does it matter?*

Every migration decision flows from understanding these structural differences. Mapping is not a 1:1 rename -- it requires rethinking how data relationships work. Misunderstanding the model leads to broken associations, orphaned records, and lost relationship context after migration.

*Key insight:*

> Salesforce separates Leads and Contacts as distinct objects with a conversion event between them. HubSpot has no Lead object -- all people are Contacts, and the Lifecycle Stage property (Subscriber, Lead, MQL, SQL, Opportunity, Customer) tracks their progression. This single difference affects routing workflows, reporting logic, and every automation that references "Leads."

*Examples:*

| Context | Example |
|---------|---------|
| Lead/Contact merge | A Salesforce org with 50,000 Leads and 30,000 Contacts becomes 80,000 Contacts in HubSpot, with Lifecycle Stage properties mapped from Lead Status and Opportunity Stage |
| Account hierarchy | Salesforce parent-child Account hierarchies must map to HubSpot's Parent Company associations, which support fewer nesting levels |
| Record types | Salesforce Opportunity Record Types (New Business, Renewal, Expansion) become separate Deal Pipelines in HubSpot, each with distinct stages |

### Migration vs. Integration vs. Sync

*What is it?*

Three distinct approaches to connecting two CRM systems, often confused. **Migration** is a one-time move where all data transfers from Salesforce to HubSpot and Salesforce is decommissioned. **Integration** keeps both systems active with bidirectional data flow. **Sync** is a subset of integration using native connectors (like HubSpot's Salesforce integration) for ongoing data exchange.

*Why does it matter?*

Clients frequently conflate these terms, leading to misaligned expectations. A migration project has a clear end state (Salesforce off, HubSpot on). An integration has no end -- it requires ongoing maintenance. Scoping a migration as if it were an integration (or vice versa) causes budget overruns and timeline failures.

*Key insight:*

> If the client says "migration" but plans to keep Salesforce active for 6+ months while teams gradually move, that is a **phased integration with eventual migration** -- a fundamentally different project with different complexity, cost, and risk profile.

*Common misunderstandings:*

- **Misconception:** "We'll just use the HubSpot-Salesforce connector to migrate."
  **Reality:** The native HubSpot-Salesforce integration is designed for ongoing sync, not extended historical data migration. It does not transfer historical activities, attachments, or custom object data. Migration requires export/import tooling or dedicated migration platforms (Trujay/SyncMatters, Import2, or custom ETL).

- **Misconception:** "Migration is just moving the data."
  **Reality:** Data is typically 30-40% of the effort. Workflow rebuild, reporting recreation, integration reconfiguration, user training, and change management account for the remaining 60-70% [2].

### The "Clean Before You Move" Principle

*What is it?*

The discipline of auditing and cleaning data in the source system (Salesforce) before migrating it to the target system (HubSpot). This means deduplicating, standardizing, archiving stale records, and validating field completeness before any data leaves Salesforce.

*Why does it matter?*

Migrating dirty data is the most cited cause of migration failure [3]. The average B2B CRM has a 15-30% duplicate rate [4]. Importing duplicates, incomplete records, and stale data into a new system poisons adoption from day one -- reps lose trust in data accuracy and revert to spreadsheets or memory.

*Key insight:*

> A 25-person SaaS company migrated 180,000 contacts from Salesforce to HubSpot without deduplication. Result: 54,000 duplicate records (30% duplicate rate), 120 hours of manual cleanup, and $23,000 in lost productivity [3]. Cleaning before migration would have cost a fraction of that.

*The Framework:*

```
Source Assessment --> Cleanup --> Validation --> Test Migration --> Production Migration

  [Salesforce]                                              [HubSpot]
  - Audit duplicates    --> Merge/purge         --> Verify counts match
  - Check field rates   --> Standardize values  --> Validate field mapping
  - Identify stale data --> Archive/delete       --> Confirm clean import
```

*Common misunderstandings:*

- **Misconception:** "We'll clean the data after we migrate it to HubSpot."
  **Reality:** Post-migration cleanup in a new system is 3-5x more expensive and disruptive than pre-migration cleanup. Users are already trying to work in HubSpot while data quality issues undermine their confidence.

- **Misconception:** "Our data is pretty clean."
  **Reality:** Without measurement, this is always an assumption. Run duplicate detection, field completion analysis, and stale record counts before accepting any data quality claim. Typical B2B CRMs have 10-25% incomplete contact records and 15-30% duplicates [4].

### Platform Capability Mapping

*What is it?*

The process of understanding which Salesforce capabilities have direct HubSpot equivalents, which require alternative approaches, and which have no equivalent. This is not just field mapping -- it covers workflows, automations, reports, integrations, custom code, and user experience patterns.

*Why does it matter?*

Not everything in Salesforce translates to HubSpot. Apex triggers have no direct equivalent. Complex Process Builder flows may need Operations Hub for equivalent logic. Salesforce CPQ does not map cleanly to HubSpot Quotes. Understanding these gaps early prevents mid-project scope creep and client frustration.

*Key insight:*

> The goal is not to replicate Salesforce in HubSpot. The goal is to achieve the same business outcomes using HubSpot's native capabilities. Often this means simpler, fewer automations -- HubSpot's workflow builder can replace 3-5 Salesforce automations with a single workflow [5].

*Examples:*

| Salesforce Capability | HubSpot Equivalent | Migration Note |
|----------------------|-------------------|----------------|
| Apex Triggers | Workflows + Operations Hub custom code | Requires rewrite; no 1:1 migration path |
| Process Builder / Flow | HubSpot Workflows | Many can be simplified; complex branching may need Operations Hub |
| Validation Rules | Required properties + Workflow-based validation | Less granular; some rules become process guidance |
| Reports &amp; Dashboards | HubSpot Custom Reports | Rebuild required; HubSpot reporting has different strengths/limits |
| Record Types | Pipelines or property-based segmentation | Fundamental architecture difference |
| Profiles &amp; Permission Sets | Teams + Permission Sets | Simpler model; may need to consolidate complex Salesforce permission structures |
| Formula Fields | Calculated Properties or Operations Hub | Limited formula support natively; complex formulas need custom code |
| Campaign object | Marketing Campaigns (Marketing Hub) | Different tracking model; requires rethinking attribution |
| Custom Objects (unlimited) | Custom Objects (Enterprise only, max 10 per account) | Major constraint; requires object consolidation strategy [6] |

---

## 2) Decision Frameworks

*Matrices, decision trees, and "when to use what" guidance for migration approach selection.*

### Approach Selection Matrix

| Situation | Recommended Approach | Why |
|-----------|---------------------|-----|
| &lt;50K total records, &lt;10 active workflows, no custom objects | Big Bang migration | Low complexity; rip-the-bandaid approach is faster and cheaper |
| 50K-500K records, 10-50 workflows, 1-3 custom objects | Phased by object type | Moderate complexity; migrate core objects first, then layer complexity |
| 500K+ records, 50+ workflows, heavy Apex, multiple BUs | Phased by department/BU | High complexity; isolate risk by migrating one team at a time |
| Dual-CRM period required (sales in SF, marketing in HS) | Integration-first, then migration | Teams need parallel access; sync during transition, then cut over |
| Regulatory/compliance requirements (audit trail mandatory) | Phased with extended parallel run | Need verifiable data integrity at each stage; read-only Salesforce for 90+ days |

### Scoping Factors

*Variables that determine migration approach, timeline, and effort.*

**1. Data Volume**

- &lt;50,000 records total --> Simple: 4-6 week timeline, single migration event
- 50,000-500,000 records --> Medium: 6-10 week timeline, phased object migration
- 500,000+ records --> Complex: 10-16 week timeline, requires dedicated migration tooling and staged approach [7]

**2. Customization Depth**

- Standard Salesforce (mostly out-of-box) --> Lower effort; direct mapping possible for most elements
- Moderate customization (custom fields, some Process Builder flows) --> Medium effort; 1-2 weeks for workflow audit and rebuild planning
- Heavy customization (Apex, Lightning components, complex automations) --> High effort; 3-5 weeks for capability mapping and alternative design

**3. Integration Footprint**

- 0-3 third-party integrations --> Minimal impact; reconfigure point-to-point
- 4-10 integrations --> Moderate; need integration cutover plan with sequencing
- 10+ integrations --> Significant; some tools (Outreach, Salesloft) can only connect to one CRM at a time -- requires careful cutover sequencing

**4. Number of Business Units / Teams**

- Single team/BU --> Straightforward; one set of pipelines, one training cohort
- 2-4 teams --> Need per-team pipeline configuration and training schedules
- 5+ teams or multi-region --> Consider phased rollout by team; increases timeline by 2-4 weeks per additional cohort

**5. HubSpot Subscription Level**

- Professional --> No custom objects, limited workflow triggers, no calculated properties. Migration scope must account for these constraints.
- Enterprise --> Full custom objects (up to 10), Operations Hub available, custom coded actions in workflows. Needed for complex Salesforce environments.

### Big Bang Approach

*Best for:*
- Small to mid-size companies (&lt;100 users)
- Clean, well-structured Salesforce orgs
- Strong executive mandate for fast transition
- Budget-conscious projects (shorter parallel run = lower cost)

*Not recommended for:*
- Organizations with complex Apex customizations
- Multi-BU companies with different sales processes
- Risk-averse organizations or regulated industries
- Teams with low technology adoption maturity

*Key differences from standard:*

| Aspect | Phased | Big Bang |
|--------|--------|----------|
| Migration event | Multiple weekends over 4-8 weeks | Single weekend or scheduled downtime |
| Parallel system cost | 2-4 months of dual licenses | 1-2 months max |
| Risk profile | Incremental, contained failures | All-or-nothing; rollback is complex |
| Team disruption | Gradual adaptation | One sharp transition |
| Timeline | 10-16 weeks total | 6-10 weeks total |
| Best for | Complexity, risk mitigation | Speed, cost savings |

### Phased Migration Approach

*Best for:*
- Enterprise organizations with multiple sales processes
- Heavy Salesforce customization requiring HubSpot alternatives
- Organizations needing to maintain business continuity during transition
- Teams where adoption risk is high and gradual change management is needed

*Not recommended for:*
- Small teams where dual-system confusion outweighs risk mitigation
- Tight budget constraints (parallel licensing costs add up)
- Organizations with urgent Salesforce contract end dates

*Phasing options:*

| Phasing Strategy | Description | When to Use |
|-----------------|-------------|-------------|
| By object type | Companies/Contacts first, then Deals, then Activities | Standard choice; lets you validate core data before adding complexity |
| By department | Marketing first, then Sales, then CS | When departments have distinct data needs and can operate independently |
| By geography | NA first, then EMEA, then APAC | Multi-region orgs with region-specific processes |
| By data age | Active/recent records first, then historical | When historical volume is very large and active data is priority |

---

## 3) Benchmarks & Standards

### How to Use Benchmarks

*Benchmarks are guidelines, not rules. Always:*
1. Start with benchmark as baseline
2. Adjust based on client-specific Salesforce complexity
3. Validate against their actual data volumes and customization depth
4. Document deviations and rationale

### Data Quality Benchmarks

| Metric | Acceptable | Good | Excellent | Notes |
|--------|-----------|------|-----------|-------|
| Duplicate rate (Contacts) | &lt;5% | &lt;2% | &lt;1% | Typical B2B CRM starts at 15-30% pre-cleanup [4] |
| Duplicate rate (Companies) | &lt;3% | &lt;1% | &lt;0.5% | Company matching is harder; name variations are common |
| Field completion (critical fields) | &gt;85% | &gt;90% | &gt;95% | Critical = email, company, lifecycle stage, owner |
| Stale record rate | &lt;20% | &lt;10% | &lt;5% | No activity in 24+ months |
| Email validity rate | &gt;80% | &gt;90% | &gt;95% | Based on bounce history and format validation |
| Owner assignment accuracy | &gt;95% | &gt;98% | 100% | Every record needs a valid owner in HubSpot |

**Source:** Industry CRM data quality benchmarks compiled from Databar, RevBlack, and LeanScale client data [4][8].

**Interpretation:**
- **Below acceptable:** Do not proceed with migration. Mandate cleanup phase first. Migrating data below these thresholds guarantees adoption problems.
- **Above excellent:** Rare for Salesforce orgs that have been active 3+ years. If a client claims these numbers without evidence, verify independently.

### Migration Timeline Benchmarks

| Migration Complexity | Planning | Data Cleanup | Build &amp; Configure | Data Migration | Testing &amp; QA | Training &amp; Cutover | Total |
|---------------------|----------|-------------|-------------------|---------------|-------------|-------------------|-------|
| Simple (&lt;50K records, minimal custom) | 1-2 weeks | 1-2 weeks | 1-2 weeks | 1 week | 1 week | 1 week | 6-10 weeks |
| Medium (50K-500K, moderate custom) | 2-3 weeks | 2-3 weeks | 2-4 weeks | 1-2 weeks | 1-2 weeks | 2 weeks | 10-16 weeks |
| Complex (500K+, heavy custom, multi-BU) | 3-4 weeks | 3-4 weeks | 4-6 weeks | 2-3 weeks | 2-3 weeks | 3-4 weeks | 16-24 weeks |

**Source:** Aggregated from HubSpot migration partners (Aptitude 8, Huble, SyncMatters) and LeanScale project data [5][9][10].

### Cost Benchmarks

| Metric | Range | Notes |
|--------|-------|-------|
| Salesforce per-user cost (Enterprise) | $150-300/user/month | Varies by edition; does not include add-ons |
| HubSpot per-user cost (Enterprise) | $50-150/user/month | Seat-based pricing; varies by Hub bundle |
| Typical TCO reduction (3-year) | 25-50% | Mid-market (25-100 users): HubSpot TCO roughly 1/3 of Salesforce TCO [11] |
| Migration project cost (agency/partner) | $15,000-$150,000+ | Depends on complexity; simple = $15-30K, medium = $30-75K, complex = $75-150K+ |
| Workflow rebuild effort (% of total project) | 30-40% | Workflows do not auto-migrate; this is consistently underestimated |
| Post-migration productivity dip | 2-4 weeks | Expect 15-25% productivity drop during learning curve |

**Source:** Aptitude 8 TCO analysis, Huble Digital, LeanScale project estimates [11][10][3].

### Quick Reference Thresholds

| Question | Good | Warning | Red Flag |
|----------|------|---------|----------|
| Data cleanup needed before migration? | &lt;5% duplicates, &gt;90% field fill | 5-15% duplicates, 80-90% fill | &gt;15% duplicates, &lt;80% fill |
| Workflow rebuild timeline realistic? | 2-4 weeks budgeted for rebuild | 1 week budgeted | "We'll just import the workflows" |
| User adoption plan in place? | Role-based training + 2-4 week hypercare | Generic training session planned | No training planned |
| Historical data scope manageable? | Last 2-3 years of closed deals | All data, all time | "Migrate everything, including archived records from 2010" |
| Custom object count in Salesforce | 0-3 custom objects | 4-8 custom objects | 10+ custom objects (exceeds HubSpot Enterprise limit of 10) |

---

## 4) Calculations & Scoring

### Formula Quick Reference

| Calculation | Formula | Example |
|-------------|---------|---------|
| Duplicate Rate | `(Duplicate Records / Total Records) x 100` | 12,000 dupes / 80,000 contacts = 15% |
| Field Completion Rate | `(Records with Field Populated / Total Records) x 100` | 72,000 with email / 80,000 contacts = 90% |
| Migration Complexity Score | `Sum of weighted factor scores (see rubric below)` | Volume(3) + Custom(4) + Integrations(2) + Teams(2) = 11/20 (Medium) |
| Estimated Cost Savings (Annual) | `(SF Annual Cost - HS Annual Cost) / SF Annual Cost x 100` | ($180K - $90K) / $180K = 50% reduction |

### Migration Complexity Scoring Rubric

Use this rubric during discovery to classify migration complexity and set appropriate timeline and budget expectations.

**Data Volume Score:**

| Criterion | Points | Threshold |
|-----------|--------|-----------|
| Total record count &lt;50K | 1 pt | Simple volume |
| Total record count 50K-500K | 3 pts | Moderate volume |
| Total record count 500K+ | 5 pts | High volume; requires staged migration |

**Customization Depth Score:**

| Criterion | Points | Threshold |
|-----------|--------|-----------|
| Standard Salesforce, &lt;10 custom fields per object | 1 pt | Minimal customization |
| Moderate: 10-50 custom fields, Process Builder flows | 3 pts | Typical mid-market |
| Heavy: 50+ custom fields, Apex triggers, Lightning components | 5 pts | Requires significant rebuild effort |

**Integration Footprint Score:**

| Criterion | Points | Threshold |
|-----------|--------|-----------|
| 0-3 third-party tools | 1 pt | Minimal integration risk |
| 4-10 third-party tools | 3 pts | Moderate; need cutover sequencing |
| 10+ third-party tools | 5 pts | High; integration migration is its own workstream |

**Organizational Complexity Score:**

| Criterion | Points | Threshold |
|-----------|--------|-----------|
| Single team, single pipeline | 1 pt | Straightforward |
| 2-4 teams, 2-4 pipelines | 3 pts | Moderate; per-team configuration needed |
| 5+ teams, multi-region, multiple BUs | 5 pts | Complex; phased rollout required |

**Tier Thresholds:**
- **Simple** (4-8 points): Big bang feasible. 6-10 week timeline. $15-30K budget range.
- **Medium** (9-14 points): Phased recommended. 10-16 week timeline. $30-75K budget range.
- **Complex** (15-20 points): Phased mandatory. 16-24 week timeline. $75-150K+ budget range.

### Data Quality Index (DQI)

Calculate before migration to determine if data cleanup phase is required.

**Formula:**
```
DQI = (0.30 x Completeness) + (0.25 x Accuracy) + (0.25 x Uniqueness) + (0.20 x Timeliness)
```

**Variables explained:**
- `Completeness` = % of records with all critical fields populated (email, company, owner, lifecycle stage)
- `Accuracy` = % of records with validated data (valid email format, correct phone format, matching company name)
- `Uniqueness` = 100% minus duplicate rate
- `Timeliness` = % of records with activity in the last 24 months

**Worked Example:**

*Scenario: Mid-market SaaS company with 120,000 contacts in Salesforce*

```
Given:
- Completeness = 82% (critical fields populated)
- Accuracy = 88% (validated formats)
- Uniqueness = 78% (22% duplicate rate)
- Timeliness = 65% (35% of records have no activity in 2+ years)

Calculate:
- DQI = (0.30 x 82) + (0.25 x 88) + (0.25 x 78) + (0.20 x 65)
- DQI = 24.6 + 22.0 + 19.5 + 13.0
- DQI = 79.1
```

**Validation:**
- DQI &gt; 85: Proceed to migration with standard cleanup
- DQI 70-85: Mandatory cleanup phase before migration (add 2-4 weeks)
- DQI &lt; 70: Extended cleanup required; consider data quality project as prerequisite before migration scoping

---

## 5) Edge Cases & Deep Dives

*Tricky scenarios that require special handling -- the institutional knowledge that prevents mid-project surprises.*

### Edge Case 1: Heavy Apex / Custom Code Dependency

*Scenario:*

The client's Salesforce org has 20+ Apex triggers, custom Lightning components, and Visualforce pages that support core business processes. Sales reps rely on custom UIs for deal registration, approval workflows, and commission tracking.

*Challenge:*

HubSpot has no Apex equivalent. Custom coded actions in HubSpot Workflows (Operations Hub) support JavaScript/Node.js but with execution limits and a fundamentally different architecture. Lightning components have no HubSpot parallel -- HubSpot's UI customization is limited to custom cards and CRM extensions.

*Approach:*

1. Inventory all Apex triggers and classify by function: data validation, field updates, notifications, external callouts, complex business logic
2. Map each to HubSpot alternatives: Workflows for field updates and notifications, Operations Hub custom code for complex logic, third-party tools (Zapier, Make) for external callouts
3. Identify any functions with no HubSpot equivalent -- these become process changes or external tool requirements
4. Budget 4-8 additional weeks for custom code rewrite and testing

*Fallback assumptions:*

| Missing Capability | Use This Instead | Source |
|-------------------|------------------|--------|
| Apex trigger for validation | HubSpot required properties + workflow-based validation | Covers 70-80% of validation use cases |
| Lightning component for custom UI | HubSpot CRM extensions (beta) or external app iframe | Limited; may require process change |
| Complex approval workflows | HubSpot approval workflows (Sales Hub Enterprise) | Supports linear approvals; complex branching may need Operations Hub |

### Edge Case 2: Multi-Business Unit with Separate Sales Processes

*Scenario:*

A company has 3 business units (SMB, Mid-Market, Enterprise) each with their own Salesforce record types, page layouts, sales processes, and automation rules. They want all three on a single HubSpot instance.

*Challenge:*

HubSpot does not have Record Types. The equivalent is separate Deal Pipelines, but pipeline-level configuration is less granular than Salesforce Record Type + Page Layout combinations. Property visibility cannot be pipeline-specific in the same way Salesforce controls field visibility per record type.

*Approach:*

1. Create one Deal Pipeline per business unit (SMB Pipeline, Mid-Market Pipeline, Enterprise Pipeline)
2. Use conditional property logic and required fields per pipeline stage to approximate page layout differences
3. Build separate workflow branches for each BU's automation needs
4. Configure team-based permissions so each BU sees their relevant data
5. Consider HubSpot Business Units add-on if marketing also needs BU-level separation (branding, email domains)

*Fallback assumptions:*

| Missing Data | Use This Instead | Source |
|--------------|------------------|--------|
| Record Type page layouts | Pipeline-specific required properties + property groups | Functional equivalent, less visual control |
| Record Type-specific automations | Workflow enrollment filters by Pipeline | Same outcome, different trigger mechanism |
| BU-specific reporting | Dashboard filters by Pipeline or Team | Requires discipline in deal creation; no hard enforcement |

### Edge Case 3: Historical Data Volume Exceeds Practical Limits

*Scenario:*

Client has 2+ million records in Salesforce spanning 10+ years, including massive activity history (emails, calls, meeting logs). They want "everything" migrated.

*Challenge:*

Migrating all historical data is technically possible but practically counterproductive. Import times increase exponentially, data quality degrades in older records, and the cost of cleaning decade-old data exceeds its value.

*Approach:*

1. Negotiate a historical data cutoff: active records + last 3 years of closed deals + all open pipeline is the standard recommendation
2. For data beyond the cutoff, offer read-only Salesforce access for 90 days (safety net) plus a full Salesforce data export archived in cloud storage (S3, Google Cloud Storage) for compliance
3. Migrate activity history selectively: last 12-24 months of emails/calls for active contacts; older activity summarized in a "Historical Notes" field
4. Use HubSpot's import API for large volumes rather than CSV uploads; batch into 500K-record chunks with validation between batches

*Fallback assumptions:*

| Missing Data | Use This Instead | Source |
|--------------|------------------|--------|
| Activity history older than 2 years | Summary note on contact record: "Pre-migration: X emails, Y calls, last activity [date]" | Preserves context without migrating millions of activity records |
| Archived deals older than 3 years | Salesforce data export in cloud storage; linked from HubSpot via URL property | Accessible for compliance, not cluttering active CRM |

### Edge Case 4: Parallel Operation Requirement (Integration Bridge)

*Scenario:*

The client cannot do a hard cutover. Sales must stay in Salesforce during the transition while marketing moves to HubSpot first. A 2-4 month parallel operation period is required.

*Challenge:*

Running two CRMs simultaneously creates data fragmentation, sync conflicts, and user confusion. Which system is the "source of truth" during the bridge period? How do you prevent data divergence?

*Approach:*

1. Use HubSpot's native Salesforce integration as a bridge during the parallel period -- this is what it was designed for
2. Define clear rules: Salesforce is system of record for sales data (deals, activities), HubSpot is system of record for marketing data (forms, campaigns, email engagement)
3. Set sync direction rules per property: Salesforce-wins for sales fields, HubSpot-wins for marketing fields
4. Build a sync health dashboard monitoring record counts, last sync times, and error rates daily
5. Plan a definitive cutover date. Open-ended parallel operation becomes permanent integration by default.

*Fallback assumptions:*

| Missing Data | Use This Instead | Source |
|--------------|------------------|--------|
| Real-time bidirectional sync for all fields | Prioritized sync for 20-30 critical fields; non-critical fields sync nightly | Reduces sync errors and API consumption |
| Unified reporting across both systems | HubSpot for marketing metrics, Salesforce for sales metrics; manual monthly reconciliation | Accept temporary reporting gap during bridge period |

### Edge Case 5: Salesforce CPQ / Complex Quoting in Use

*Scenario:*

Client uses Salesforce CPQ (Configure, Price, Quote) with product rules, pricing rules, discount schedules, and approval chains. They generate quotes and contracts from within Salesforce.

*Challenge:*

HubSpot Quotes is significantly simpler than Salesforce CPQ. There is no product rule engine, no multi-tier discount schedules, and limited approval workflows for quotes. This is one of the most common blockers for enterprise Salesforce-to-HubSpot migrations.

*Approach:*

1. Assess actual CPQ usage: many organizations only use 20-30% of Salesforce CPQ's capabilities. Identify what features are actively used vs. configured but unused.
2. For simple quoting (product catalog, basic discounts, single approval): HubSpot's native Quotes tool is sufficient
3. For complex quoting: evaluate third-party CPQ tools that integrate with HubSpot (PandaDoc, DealHub, Proposify)
4. For advanced CPQ (multi-tier pricing, complex product bundling, advanced approvals): this may be a migration blocker. Document it explicitly in the migration scope as a constraint.

---

## References

[1] [RevBlack - HubSpot vs Salesforce: Data Model Differences](https://www.revblack.com/articles/data-model-differences-hubspot-salesforce)
[2] [Huble Digital - 10 Pitfalls to Avoid When Migrating from Salesforce to HubSpot](https://huble.com/blog/salesforce-to-hubspot)
[3] [Optif.ai - Zero-Downtime CRM Migration Checklist &amp; Framework 2025](https://optif.ai/media/articles/crm-data-migration-checklist/)
[4] [Databar - The Complete Guide to CRM Data Quality Metrics](https://databar.ai/blog/article/the-complete-guide-to-crm-data-quality-metrics-standards-best-practices)
[5] [Aptitude 8 - How to Migrate from Salesforce to HubSpot](https://aptitude8.com/how-to-migrate-from-salesforce-to-hubspot)
[6] [ATAK Interactive - Custom Objects in HubSpot and Salesforce: Integration Challenges](https://www.atakinteractive.com/blog/custom-objects-in-hubspot-and-salesforce-integration-challenges-and-solutions)
[7] [MarTech Do - Master Data Migration: 7 Essential Best Practices for B2B RevOps 2025](https://www.martechdo.com/data-migration-best-practices/)
[8] [RevBlack - The 6 Pillars of CRM Data Quality](https://www.revblack.com/guides/the-6-pillars-of-crm-data-quality)
[9] [SyncMatters - Salesforce to HubSpot Migration Guide](https://syncmatters.com/blog/salesforce-to-hubspot-migration-a-detailed-step-by-step-guide)
[10] [Huble Digital - Salesforce to HubSpot Migration](https://huble.com/blog/salesforce-to-hubspot)
[11] [Aptitude 8 - Total Cost of Ownership: HubSpot vs Salesforce](https://aptitude8.com/a-look-at-the-total-cost-of-ownership-of-hubspot-vs-salesforce)
