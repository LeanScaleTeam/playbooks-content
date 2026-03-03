# HubSpot to Salesforce Migration — Advisory

HubSpot to Salesforce Migration - CRM Platform Migration & Transformation

## 1) Project Overview

### What is the name of this project?

HubSpot to Salesforce Migration - CRM Platform Migration & Transformation

### What is the purpose of this project?

A HubSpot to Salesforce migration takes an organization's CRM from one platform to another, involving transformation of processes, data architecture, and operational workflows. The project spans scoping decisions across five key object categories (accounts, opportunities, contacts/leads, technology, and data structure), workback plan creation, field mapping and data transformation, Salesforce automation and layout builds, data migration, third-party tool reconnection, and launch with enablement and hyper-care support.

> **Core transformation:** Without a structured migration process, organizations risk data loss, broken workflows, extended downtime, and user adoption failures. With this process: decisions are documented across all five object categories, dependencies are mapped in a workback plan, transformational improvements are captured during the move, and the new system launches clean with proper enablement.

### What HubSpot to Salesforce Migration Unlocks

- Transition to a CRM platform that better supports operational scale and reporting needs
- Opportunity to clean up technical debt and implement process improvements during the move (the "T" in ETL)
- Proper architecture of leads, contacts, accounts, and opportunities for downstream reporting and operations
- Standardized data structure with reduced duplicates and junk data
- Foundation for Salesforce's broader ecosystem of tools and integrations (CPQ, advanced reporting, AppExchange)
- Documented decisions across all five object categories with dependencies mapped

| Before (HubSpot)                                    | After (Salesforce)                                          |
| --------------------------------------------------- | ----------------------------------------------------------- |
| Single Contact object for leads and customers        | Separate Lead and Contact objects with defined lifecycle     |
| Native quoting with limited CPQ functionality        | Full CPQ tool ecosystem (DealHub, Subskribe, native CPQ)    |
| Limited reporting on pipeline velocity and attribution | Timestamps, stage timing, ACV/TCV calculations built in    |
| Contacts can be free-floating (no account required)  | Contacts attached to Accounts with proper hierarchy          |
| Workflow automations in HubSpot format               | Salesforce flows with "The Hits" foundational automations    |
| Data quality issues accumulated over time            | Clean, audited fields with junk data and duplicates removed  |

### What business outcomes does this project drive?

**Primary Outcomes:**

- Transition to a CRM platform that better supports the organization's operational needs (often driven by team comfort with Salesforce or scaling requirements)
- Proper architecture of leads, contacts, accounts, and opportunities for downstream reporting and operations
- Standardized data structure with reduced duplicates and junk data
- Clean field mapping with unused and redundant fields removed

**Secondary Outcomes:**

- Foundation for advanced revenue operations (attribution, CPQ, territory management)
- Improved data visibility for executive reporting and pipeline forecasting
- Process improvements captured during migration that would not happen in day-to-day operations
- Access to Salesforce's AppExchange ecosystem for future tool needs

### Who in the Org can benefit from this project?

- **Sales teams** - New CRM for daily operations with improved workflows
- **Marketing teams** - Improved lead lifecycle tracking and attribution
- **Revenue Operations** - Cleaner data architecture, better reporting, proper lead/contact/account structure
- **Executive leadership** - Accurate pipeline and revenue reporting
- **Customer Success** - Structured account data for renewals and expansion tracking

### Pain Points this Project Solves

| Pain Point | What the Migration Enables |
| --- | --- |
| "I can't get the insights I want from our CRM" (data visibility) | Properly structured data with clean fields, accurate reporting, and executive dashboards in Salesforce |
| "XYZ is not easy to do in HubSpot" (end user adoption and usability) | Salesforce workflows, page layouts, and automations designed around how the team actually works |
| "We have too many duplicate and junk records" | Field audit process identifies and removes duplicates, junk data, and unused fields before migration |
| "Our workflows break and nobody knows why" | Documented automations in Salesforce with "The Hits" foundational automations built as standard |
| "We've outgrown HubSpot's reporting and tooling" | Access to Salesforce's ecosystem: CPQ, advanced analytics, AppExchange integrations |

Data visibility and end user adoption are overwhelmingly the primary reasons organizations pursue this project.

### The Data Behind the Problem

CRM migrations are high-stakes projects with well-documented failure modes:

- **Over 80% of data migration projects exceed their timelines or budgets**, with cost overruns averaging 30% and time delays reaching 41% [1]
- **Poor data quality costs organizations an average of $12.9 million per year**, according to Gartner research. Most organizations (59%) do not even measure their data quality [2]
- **B2B data decays at approximately 30% per year** (Gartner), meaning a CRM that has not been actively maintained for 2-3 years may have more bad records than good ones [3]
- **20-70% of CRM projects fail**, with the leading cause being poor user adoption, followed by lack of integration with other tools (17%) and complexity of use (7%) [4]
- **72% of migrations break at least one critical integration** (email sync, calendar, accounting software), creating downstream disruption [1]
- **Sales teams spend approximately 546 hours per year dealing with data quality issues**, according to a Dun & Bradstreet study - time that could be spent selling [3]

The combination of data decay, integration fragility, and adoption risk is why a structured migration process - not a lift-and-shift - produces materially different outcomes.

### Key Metaphors or Frameworks

**ETL vs ELT (Extract, Transform, Load vs Extract, Load, Transform)**

The migration approach decision that sets the tone for the entire project. ETL transforms data before loading into Salesforce (cleaner end state, more upfront work). ELT loads data as-is and transforms after (faster start, risk of downstream complications). Use this framework in scoping conversations to align on appetite for transformation.

- **When to use:** Every initial scoping conversation - this is the first major decision
- **When NOT to use:** With non-technical stakeholders who need outcomes, not process language

**The Big Five**

Five object categories that must be scoped in every HubSpot-to-Salesforce migration: Accounts, Opportunities, Contacts/Leads, Technology, and Data Structure. Frames the scoping phase as a finite set of decisions rather than an open-ended exploration.

- **When to use:** Framing the scoping phase and setting expectations for decision volume
- **When NOT to use:** Deep technical discussions about specific object architectures

### Target Motion

Applicable to all GTM motions: SLG (Sales-Led Growth), PLG (Product-Led Growth), and ELG (Ecosystem-Led Growth). The motion type impacts how the end system is designed - particularly the contacts-to-leads architecture and lead lifecycle.

- **SLG companies:** Standard lead-based architecture with full lead lifecycle (most common, ~14 of 15 migrations)
- **PLG companies:** May require contact-only architecture if user signups create high-volume free-floating contacts (rare, ~1 of 15)
- **Hybrid/ELG:** Lead-based architecture with additional partner object considerations

*Not a fit for:* Organizations moving FROM Salesforce TO HubSpot (different project type). Also not a fit for organizations that only need a HubSpot-Salesforce sync/integration rather than a full migration.

---

## 2) Tools & Systems

### Primary Tools

**HubSpot** — Source CRM system. Used for data extraction, field inventory, workflow documentation, and understanding current-state architecture during scoping.

**Salesforce** — Destination CRM system. Used for building automations, page layouts, data import, and all post-migration operations.

**Excel / Google Sheets** — Used for field audit spreadsheets, data mapping documents, and workback plan creation. Core working document for field-by-field analysis decisions (keep, transform, or delete).

**Lucidchart** — Used for architecture diagrams, particularly for contacts-to-leads architecture decisions and data flow mapping.

**Third-Party Tools (Client-Specific):** Varies by client. Common tools requiring migration strategy: Gong, Salesloft, Outreach, ChurnZero, CPQ tools (DealHub, Subskribe), data enrichment tools.

---

## 3) Stakeholders & Roles

### Client-Side Stakeholders

**Executive Sponsor (VP Sales, VP RevOps, or CRO)**

- Required for: Scoping workshops, go/no-go decisions, migration approach sign-off
- Responsibilities: Budget approval, timeline alignment, championing adoption internally

**Operations Lead (RevOps Manager, Sales Ops Manager)**

- Required for: All scoping sessions, field audit reviews, workflow documentation
- Responsibilities: Providing context on existing business processes, making field-level decisions, coordinating internal team input

**Day-to-Day Point of Contact (Operations Analyst or Admin)**

- Required for: Ongoing build sessions, QA testing, integration coordination
- Responsibilities: Testing workflows, validating data accuracy, coordinating third-party vendor contacts

### Technical Owners

**Client-Side CRM Admin or RevOps Lead**

- Provides admin access to both HubSpot and Salesforce
- Owns ongoing system maintenance post-migration
- Participates in enablement training to understand new architecture

---

## 4) Scoping

### Scoping Factors

**1. Go-to-Market Motion**

- PLG (Product-Led Growth) -&gt; Impacts contacts-to-leads architecture; may require contact-only approach for high-volume user signups
- SLG (Sales-Led Growth) -&gt; Standard lead-based architecture (most common)
- ELG (Ecosystem-Led Growth) -&gt; May require partner object considerations

**2. Appetite for Change (ETL vs ELT)**

- High appetite for transformation -&gt; ETL approach (extract, transform, then load). Cleaner end state, more upfront hours.
- Low appetite / tight timeline -&gt; ELT approach (extract, load, then transform). Faster start, risk of downstream complications.

**3. Timeline**

- Standard timeline (~3-4 months) -&gt; Full ETL with field audits and transformation
- Compressed timeline (&lt;2 months) -&gt; May force ELT approach; increases risk

**4. Existing Infrastructure & Tech Debt**

- Many third-party integrations -&gt; More cutover coordination, more hours
- HubSpot-native features in use (e.g., quoting) -&gt; Need Salesforce equivalents (CPQ evaluation)
- Accumulated junk data and duplicates -&gt; More transformation work during field audit

**5. Data Structure**

- Standard objects only -&gt; Simpler migration
- Custom objects in HubSpot -&gt; Need Salesforce custom object equivalents
- Transformational changes needed (e.g., consolidating renewal opps) -&gt; Additional scoping and build hours

**6. Data Volume**

- Low record counts (&lt;50K across objects) -&gt; Simpler data migration
- High record counts (100K+) -&gt; More testing, potential for performance issues during import

**7. Contacts-to-Leads Architecture**

- Lead-based (recommended, ~14 of 15 cases) -&gt; HubSpot contacts split into Salesforce Leads and Contacts based on lifecycle stage. Requires lead lifecycle design.
- Contact-only (rare, ~1 of 15 cases) -&gt; All records go to Contacts. Challenge: Gmail/personal email signups have nowhere to attach because there is no Google Account in Salesforce. May need "orphanage" accounts as workaround.

**8. Third-Party Tool Ecosystem**

- Few integrations (&lt;5) -&gt; Standard migration
- Many integrations (10+) -&gt; Significant cutover coordination; some tools have tight just-in-time cutover windows (e.g., Salesloft)

**9. Merger vs. Single-Instance Migration**

- Single instance -&gt; Standard scoping
- Merger (two instances into one Salesforce org) -&gt; Must scope BOTH instances and design unified vision. Non-linear complexity increase.

### Multiple Approaches

**Approach 1: ETL (Recommended)**

- Criteria: Cleanup is needed, budget allows, timeline is not severely compressed
- Execution: Extract data from HubSpot, transform (clean, deduplicate, restructure) before loading into Salesforce. Field audit drives what gets kept, transformed, or deleted. Produces a cleaner end state.

**Approach 2: ELT**

- Criteria: Very tight timeline or constrained budget; client accepts risk of post-load cleanup
- Execution: Extract from HubSpot, load into Salesforce as-is, transform after. Faster initial setup but can cause downstream complications.

**Approach 3: Lead-Based Architecture (Recommended)**

- Criteria: Most migration scenarios (~14 of 15 cases)
- Execution: Anything earlier than an opportunity in the lifecycle goes to Salesforce Leads. Requires lead lifecycle design including statuses, conversion triggers, and creation flows.

**Approach 4: Contact-Only Architecture**

- Criteria: Very rare. Only viable with tight control over data universe (no open signups, no Gmail/personal email contacts).
- Execution: All records go to Contacts attached to Accounts. Challenge: Gmail signups have nowhere to attach because there is no Google Account to attach them to in Salesforce. May need "orphanage" accounts as workaround.

---

## 5) Discovery Questions

### Questions for Project Kickoff

**Overall Approach & Goals**

- What is driving the decision to move from HubSpot to Salesforce? *(Distinguishes comfort-driven vs. capability-driven migration)*
- Do you want to clean up and transform data during migration, or port over as-is and iterate in the new instance? *(ETL vs ELT decision)*
- What is your target go-live date? *(Determines timeline pressure and approach viability)*

**Data Quality & Structure**

- Are there duplicates or junk data in the system today? *(Scopes transformation work)*
- How many custom objects exist in HubSpot? *(Identifies custom object migration needs)*
- What is the approximate record count across contacts, companies, and deals? *(Data volume scoping)*

**Contacts & Leads**

- How do you want to manage contacts versus leads in Salesforce? *(Architecture decision)*
- If a record is earlier than an opportunity in the lifecycle, should it be treated as a lead? *(Lead-based vs. contact-only)*
- Do you have signups from Gmail or personal email domains? *(Contact-only architecture blocker)*

**Technology & Integrations**

- What third-party tools are connected to HubSpot that need to be migrated? *(Integration inventory)*
- Are there any HubSpot-only tools or features that need Salesforce alternatives? *(Gap analysis)*
- Do you need CPQ / quoting functionality? HubSpot has native quoting; Salesforce does not. *(CPQ evaluation trigger)*

**Team & Adoption**

- Who on your team has Salesforce experience? *(Training scope)*
- Who will be the day-to-day admin maintaining Salesforce post-migration? *(Technical owner identification)*
- How many users will need access to the new system? *(License planning)*

### Information to Gather Before Implementation

**System Inventory:**

Complete inventory of HubSpot fields per object (contacts, companies, deals) - exported from HubSpot settings, including field types and fill rates

**Workflow Documentation:**

List of all active workflows and automations in HubSpot, including trigger conditions and actions

**Integration Map:**

List of all connected third-party tools with connection type (native integration, API, Zapier/middleware)

**Lead Lifecycle:**

Understanding of current lead lifecycle and statuses - how leads are created, qualified, and converted today

**Data Quality Sample:**

Sample assessment of data quality: duplicate rate, field fill rates across key objects, presence of junk records

**Opportunity Structure:**

Current opportunity/deal structure - single opportunity per customer vs. multiple (renewals, expansions), stage definitions

### Approach Decision Questions

| Question | Answer -&gt; Approach |
| --- | --- |
| How clean is your current data? | If messy -&gt; ETL preferred (transform before loading) |
| How tight is your timeline? | If very tight -&gt; ELT may be necessary (load first, transform later) |
| How much budget is available for cleanup? | More budget = more transformation possible during migration |
| Do you have Gmail/personal email signups? | If yes -&gt; Lead-based architecture required (contact-only won't work) |
| Is this a single-instance migration or a merger? | Merger -&gt; Significantly more hours, scope both instances |

---

## 6) Overcoming Common Belief Barriers

#### "We can just export and import - it's a data move, not a project."

HubSpot and Salesforce have fundamentally different data architectures. HubSpot uses a single Contact object for both leads and customers. Salesforce separates these into Lead and Contact objects with different fields, behaviors, and lifecycle rules. Every contact in HubSpot requires a routing decision: does it become a Lead or a Contact in Salesforce? Then there are field transformations, workflow recreation, third-party tool reconnection, layout design, and enablement. Industry data shows over 80% of data migration projects that are treated as simple transfers exceed their timelines or budgets [1].

**The reframe:** "A HubSpot to Salesforce migration is a system redesign with a data move inside it, not the other way around."

#### "Let's move everything over and clean it up in Salesforce later."

This is the ELT approach, and it has a documented failure mode. The migration itself is the single best window for transformational cleanup because disruption is already happening. Deferring cleanup means your new Salesforce instance starts with the same data problems your HubSpot had - and B2B data decays at 30% per year [3], so the problems compound. If you're not doing any transformation, it's just field mapping and data migration - which is how zero migrations actually get done successfully.

**The reframe:** "The migration is the cheapest time to fix data problems because you're already touching every record. Cleaning up later means paying twice."

#### "This will shut down our sales team for weeks."

The first ~30 days of the project are scoping and architecture work. No one touches the live HubSpot system. The Salesforce instance is built, tested, and QA'd in parallel while the sales team continues working normally. The actual cutover is coordinated, and the hyper-care period (2-4 weeks post-launch) exists specifically to catch and fix edge cases quickly.

**The reframe:** "Your sales team keeps working in HubSpot until the new Salesforce instance is built, tested, and ready. The cutover is a coordinated switch, not a shutdown."

#### "We don't need a field audit - just move the fields we're using."

The field audit is where 30-50% of migration value is captured. It routinely reveals that a significant portion of fields have low fill rates, are duplicates, or are no longer used by any workflow. Moving unused fields into Salesforce creates a cluttered, hard-to-maintain system from day one. Organizations with 500 fields in HubSpot should not expect to lift and replace all of them - the audit analyzes which fields are actually being used and providing value.

**The reframe:** "The field audit doesn't slow the project down - it prevents you from building a new system that inherits all the problems of the old one."

#### "Our team knows Salesforce, so we don't need much training."

Individual Salesforce familiarity does not translate to adoption of a new instance with new architecture, new workflows, and new data structures. Average CRM adoption rates across sectors sit at just 26% [4], and 25% of organizations cite training and adoption as their biggest CRM implementation challenge [6]. The hyper-care period exists because every migration surfaces edge cases that only appear with real user data at scale.

**The reframe:** "Knowing Salesforce and knowing YOUR Salesforce are two different things. Enablement covers the specific architecture decisions made for your business."

---

## 7) Metrics Impact & Success Measurement

### Power 10 Metrics Impacted

| Power 10 Metric | Impact Direction | Expected Magnitude | Notes |
| --- | --- | --- | --- |
| Pipeline Accuracy | ↑ Increase | Significant improvement | Clean data structure + proper opportunity architecture = accurate pipeline reporting |
| MQL -&gt; Opp Conversion | ↑ Increase | Indirect | Proper lead lifecycle design and conversion flows improve handoff tracking |
| Opp -&gt; CW Conversion | -- Neutral initially | Stabilizes post-migration | Migration itself does not change win rates, but accurate data enables diagnosis |
| Cycle Time | -- Neutral to ↑ | Measurement improvement | Timestamps and stage timing automations ("The Hits") enable cycle time measurement that may not have existed before |

*Note: This migration is primarily an infrastructure project. Its metrics impact is enabling accurate measurement and reporting rather than directly moving specific conversion rates. The downstream projects it enables (lead lifecycle redesign, attribution, deduplication) are where conversion rate improvements materialize.*

### Expected Outcomes

| Metric | Before | After | Source |
| --- | --- | --- | --- |
| CRM data accuracy | Accumulated duplicates, junk records, low fill-rate fields | Audited fields, deduplicated records, junk data removed | Field audit process |
| Reporting reliability | Limited visibility into pipeline velocity and attribution | Timestamps, stage timing, ACV/TCV calculations built in via "The Hits" | Foundational automations |
| Integration health | HubSpot-specific tool connections | Salesforce-native integrations with documented cutover strategy per tool | Third-party tool strategy |
| User adoption | N/A (new system) | Target: 80%+ daily active usage within 60 days of launch | Industry benchmark: average CRM adoption is 26% [4]; structured enablement targets significantly higher |

### How to Measure Success

**Leading Indicators (Week 1-4 post-launch):**

- Daily active users logging into Salesforce (target: 80%+ of licensed users)
- Number of support tickets / issues reported during hyper-care (expect high initially, declining weekly)
- All critical integrations flowing data correctly (zero broken integrations)
- Record count validation: Salesforce record counts match expected migration totals

**Lagging Indicators (Month 2-6 post-launch):**

- Reduction in duplicate record creation rate vs. pre-migration baseline
- Executive reporting dashboards populated and actively used (measured by dashboard view frequency)
- Sales team self-reported satisfaction with new system (survey at 60 and 90 days)
- Time-to-first-report: How quickly new reports can be built vs. old system limitations
- Zero reversion to HubSpot or shadow systems (spreadsheets, notes apps) for CRM data

---

## References

[1] [Zero-Downtime CRM Migration - Revenue Velocity Lab / Optif.ai](https://optif.ai/media/articles/crm-data-migration-checklist/)
[2] [Gartner - Data Quality: Why It Matters and How to Achieve It](https://www.gartner.com/en/data-analytics/topics/data-quality)
[3] [ZoomInfo - The True Cost of Poor Data Quality](https://pipeline.zoominfo.com/operations/poor-data-quality-impact)
[4] [CRM.org - 45 CRM Statistics You Need to Know in 2025](https://crm.org/crmland/crm-statistics)
[5] [BeyondCRM - Avoid These CRM Migration Pitfalls](https://www.beyondcrm.com.au/crm-migration-risk/)
[6] [VisualSP - CRM Adoption: How to Increase End-User Adoption Rates](https://www.visualsp.com/blog/crm-adoption-how-to-increase-end-user-adoption-rates/)
