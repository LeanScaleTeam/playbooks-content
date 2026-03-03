# Marketing Automation Platform Implementation — Methodology

This document covers the core concepts, frameworks, and calculations behind Marketing Automation Platform Implementation. It provides the methodological foundation — the 'how it works' behind the execution steps.

---

## 1) Core Concepts

### The Marketing Automation Technology Stack

*What is it?*

A marketing automation platform (MAP) is the system of record for marketing execution -- it orchestrates email campaigns, lead scoring, nurture workflows, form capture, and reporting. The MAP sits between your website (top of funnel) and your CRM (bottom of funnel), converting anonymous visitors into scored, qualified leads that route to sales.

*Why does it matter?*

Without a MAP, marketing teams operate in manual mode: batch-and-blast emails, spreadsheet-based lead lists, no visibility into buyer engagement. Companies using marketing automation generate 80% more leads and achieve 77% higher conversion rates than those without [1]. For B2B SaaS companies at $5M-$100M ARR, the MAP is the engine that turns marketing spend into measurable pipeline.

*Key insight:*

> The MAP is not a standalone tool -- it is the connective tissue between your website, CRM, sales engagement platform, and analytics. A platform configured in isolation fails. Integration architecture is the first design decision, not an afterthought.

*Examples:*

| Context | Example |
|---------|---------|
| Series A SaaS, no MAP | Deploy HubSpot Marketing Hub, connect to HubSpot CRM, stand up first nurture and scoring model. Time-to-value: 4-6 weeks. |
| Series C company migrating Pardot to HubSpot | Full data migration with field mapping, workflow recreation, and parallel-run period. Timeline: 8-12 weeks including hypercare. |
| Enterprise with Marketo + Salesforce | Complex multi-BU configuration with partitioned lead databases, territory-based routing, and custom API integrations. Timeline: 12-16 weeks. |

---

### Lead Scoring: Demographic + Behavioral

*What is it?*

Lead scoring is a point-based system that ranks leads on two dimensions: (1) **demographic/firmographic fit** (who they are -- title, company size, industry) and (2) **behavioral engagement** (what they do -- page visits, email clicks, content downloads). The combined score determines when a lead is "sales-ready" (MQL threshold).

*Why does it matter?*

Companies effectively using lead scoring see 30% higher MQL-to-SQL conversion rates compared to manual qualification [2]. Without scoring, sales wastes time on unqualified leads and marketing cannot quantify lead quality. Scoring is the contract between marketing and sales: "When a lead reaches X points, we hand it to you."

*Key insight:*

> Lead scoring is not "set and forget." A model that is not recalibrated every 90 days against actual conversion data will drift. The initial model is a hypothesis -- closed-won analysis proves or disproves it.

*Common misunderstandings:*

- **Misconception:** Higher scores always mean better leads.
  **Reality:** Score inflation happens when behavioral actions are over-weighted. A lead who downloads 10 ebooks but works at a 3-person company is not an MQL. Fit score must gate behavioral score.

- **Misconception:** Lead scoring replaces sales judgment.
  **Reality:** Scoring automates the first filter. Sales still qualifies MQLs through discovery. Scoring reduces noise; it does not replace human qualification.

---

### CRM-MAP Integration Architecture

*What is it?*

The bidirectional data sync between your marketing automation platform and CRM. This includes field mapping (which data flows where), sync direction (MAP-to-CRM, CRM-to-MAP, or bidirectional per field), sync frequency, and conflict resolution rules (which system "wins" when data conflicts).

*Why does it matter?*

The CRM-MAP integration is the single most failure-prone component of any marketing automation implementation. Field type mismatches (e.g., a dropdown in Salesforce syncing to a free-text field in HubSpot) cause silent data corruption. Incorrect sync direction overwrites good data with bad. A poorly configured integration creates a downstream mess that takes weeks to untangle [3].

*The Framework:*

```
WEBSITE → [Forms/Tracking] → MAP → [Sync] → CRM
             ↑                        ↕
        Landing Pages          Bidirectional Sync
        UTM Capture            (field-level control)
        Progressive Profiling         ↓
                               Sales Engagement
                               (Outreach, Salesloft)
```

*Common misunderstandings:*

- **Misconception:** "Just turn on the native integration and it works."
  **Reality:** Native integrations (e.g., HubSpot-Salesforce connector) provide default field mappings that do not reflect your business's custom fields, picklist values, or sync rules. Default mappings are a starting point, not a finished configuration [3].

- **Misconception:** All fields should sync bidirectionally.
  **Reality:** Most fields should have a single source of truth. Marketing-owned fields (lead source, campaign membership, score) flow MAP-to-CRM. Sales-owned fields (opportunity stage, close date) flow CRM-to-MAP. Bidirectional sync is reserved for shared fields like lifecycle stage or contact information.

---

### Email Deliverability and Sender Reputation

*What is it?*

Email deliverability is the percentage of sent emails that reach the recipient's inbox (not spam or junk folder). Sender reputation is the score ISPs assign to your sending domain and IP based on authentication records, bounce rates, complaint rates, and engagement patterns.

*Why does it matter?*

A good deliverability rate is above 95%; below 89% is concerning, and below 80% is a crisis [4]. Authentication via SPF, DKIM, and DMARC is now mandatory -- Google enforced this from February 2024, Yahoo from February 2024, and Microsoft from May 2025. Fully authenticated senders are 2.7x more likely to reach inboxes [4]. For a new implementation or migration, IP/domain warming is critical: ISPs treat new senders as suspicious until they establish a positive track record over 4-8 weeks [5].

*Key insight:*

> Deliverability is earned, not assumed. A brand-new sending domain with no reputation will land in spam by default. IP warming is not optional -- it is the difference between a successful launch and a deliverability disaster that takes months to recover from.

---

### Attribution Models

*What is it?*

Attribution is the methodology for assigning credit to marketing touchpoints along the buyer journey. Models range from single-touch (first-touch or last-touch) to multi-touch (linear, W-shaped, Z-shaped). The chosen model determines how marketing reports ROI and which channels appear most effective.

*Why does it matter?*

75% of companies now use multi-touch attribution to measure marketing performance [6]. The attribution model directly shapes budget allocation decisions. First-touch over-credits top-of-funnel channels; last-touch over-credits bottom-of-funnel. For B2B SaaS with 30-90 day sales cycles and 6-8 touchpoints per deal, single-touch models produce misleading data.

*Common misunderstandings:*

- **Misconception:** There is one "correct" attribution model.
  **Reality:** The right model depends on your sales cycle length, number of touchpoints, and what questions you need answered. W-shaped (30/30/30/10) is the most common starting point for B2B because it credits first touch, lead creation, and opportunity creation equally [6].

- **Misconception:** Attribution tells you exactly which campaign drove the deal.
  **Reality:** Attribution is directional, not precise. It tells you which channels and campaigns contribute disproportionately to pipeline. Use it for resource allocation, not forensic accounting of individual deals.

---

## 2) Decision Frameworks

### Approach Selection Matrix

| Situation | Recommended Approach | Why |
|-----------|---------------------|-----|
| No existing MAP, HubSpot CRM in place | HubSpot Marketing Hub (new implementation) | Native CRM integration eliminates sync complexity; fastest time-to-value |
| No existing MAP, Salesforce CRM in place | HubSpot or Pardot (evaluate both) | HubSpot offers better UX and faster adoption; Pardot offers deeper native Salesforce integration |
| Migrating from Pardot/Marketo to HubSpot | Platform migration with data cleanup | Opportunity to simplify workflows and clean data; plan 8-12 weeks |
| Enterprise with complex multi-BU needs | Marketo or HubSpot Enterprise | Marketo excels at partitioned databases and enterprise-scale automation; HubSpot Enterprise closing the gap |
| Startup under $5M ARR, limited marketing team | HubSpot Starter/Professional | Lower cost, easier to self-manage, grows with the business |
| Existing MAP is working but CRM integration is broken | Integration-focused project (not full migration) | Fix the sync layer without re-platforming; scope as a 2-4 week project |

### Scoping Factors

**1. New Implementation vs. Migration**

- New implementation → No legacy data to migrate. Focus: requirements gathering, platform configuration, training. Timeline: 4-8 weeks.
- Migration from existing platform → Data migration, workflow recreation, parallel-run period, and decommissioning of legacy system. Timeline: 8-16 weeks depending on data volume and workflow complexity.

**2. CRM Platform**

- HubSpot CRM → Native HubSpot MAP integration. Zero integration effort. Field mapping is automatic for standard fields.
- Salesforce → Requires connector configuration. Field mapping, sync rules, and conflict resolution must be manually designed. Add 1-2 weeks to timeline.
- Other CRM (Microsoft Dynamics, Pipedrive, etc.) → API-based integration or third-party connector (e.g., Workato, Tray.io). Add 2-3 weeks and higher technical complexity.

**3. Data Volume and Quality**

- Under 50,000 contacts, clean data → Standard migration. Batch import with validation.
- 50,000-500,000 contacts → Requires data cleanup phase (deduplication, enrichment, validation). Add 1-2 weeks.
- Over 500,000 contacts or significant data quality issues → Dedicated data remediation workstream. Consider migrating only active contacts (engaged in last 12-24 months) and archiving the rest.

**4. Workflow Complexity**

- Under 10 active workflows → Recreate manually in new platform. Opportunity to simplify.
- 10-50 active workflows → Map each workflow, evaluate necessity, recreate priority workflows first. Phase the rest.
- Over 50 active workflows → Full workflow audit required. Many are likely redundant or conflicting. Plan for a simplification pass before recreation.

**5. Team Technical Skill**

- Marketing team with MAP experience → Lighter training load. Focus on platform-specific differences.
- Marketing team new to automation → Extended training phase. Plan 3 sessions minimum. Build reference documentation and SOPs.

---

### New Implementation Approach

*Best for:*
- Companies with no existing MAP
- Startups deploying their first marketing infrastructure
- Companies replacing a very outdated or barely-used platform

*Not recommended for:*
- Organizations with extensive existing automation and historical data they need to preserve
- Situations where a functioning MAP exists but needs optimization (scope as optimization, not reimplementation)

*Key differences from migration:*

| Aspect | Migration | New Implementation |
|--------|-----------|-------------------|
| Data | Migrate and clean existing records | Import from CRM or start fresh |
| Workflows | Recreate or rebuild from legacy | Design from scratch based on buyer journey |
| Timeline | 8-16 weeks | 4-8 weeks |
| Risk | Data loss, broken workflows, deliverability reset | Slower initial adoption, content creation needed |
| IP/Domain | Warming required if new sending domain | Warming always required |

---

### Migration Approach

*Best for:*
- Companies switching platforms (e.g., Marketo to HubSpot, Pardot to HubSpot)
- Organizations whose current platform no longer fits their needs or budget
- Companies consolidating multiple marketing tools into one

*Not recommended for:*
- Organizations whose current platform works but is under-utilized (scope as enablement, not migration)
- Companies mid-campaign season with no bandwidth for disruption

*Migration phases:*

| Phase | Focus | Duration |
|-------|-------|----------|
| Audit &amp; Planning | Inventory assets, map fields, define migration scope | 2-3 weeks |
| Data Cleanup &amp; Migration | Clean data, test import, validate | 2-3 weeks |
| Platform Configuration | Set up scoring, workflows, integrations | 2-4 weeks |
| Parallel Run &amp; Cutover | Run both systems, validate, switch | 1-2 weeks |
| Hypercare | Monitor, fix issues, support team | 2 weeks |

---

### Platform Selection Framework

| Factor | HubSpot | Marketo | Pardot (Account Engagement) |
|--------|---------|---------|----------------------------|
| Best CRM fit | HubSpot CRM (native) | Any (API-based) | Salesforce (native) |
| Team skill required | Low-Medium | High | Medium |
| Ease of use | High | Low-Medium | Medium |
| Customization depth | Medium-High | Very High | Medium |
| Pricing model | Contact-tier based | Feature + contact based | Edition-based |
| B2B SaaS fit ($5-100M) | Strong | Strong (upper end) | Strong (Salesforce shops) |
| AI/Predictive features | Predictive lead scoring, content AI | Adobe Sensei integration | Einstein AI integration |
| Long-term trajectory | Heavy investment, rapid feature growth [7] | Stable, Adobe ecosystem play | Uncertain -- limited feature updates, consolidation rumors [7] |

---

## 3) Benchmarks &amp; Standards

### How to Use Benchmarks

*Benchmarks are guidelines, not rules. Always:*
1. Start with benchmark as baseline
2. Adjust based on client-specific data
3. Validate against their actual numbers when available
4. Document deviations and rationale

### Email Performance Benchmarks (B2B SaaS)

| Metric | Low | Typical | High | Notes |
|--------|-----|---------|------|-------|
| Deliverability rate | &lt;89% | 89-95% | &gt;95% | Below 89% requires immediate investigation [4] |
| Open rate | &lt;15% | 20-30% | &gt;35% | Apple MPP inflates open rates; track clicks as primary metric |
| Click-through rate (CTR) | &lt;1% | 2-4% | &gt;5% | Measure unique clicks, not total |
| Bounce rate (hard) | &gt;2% | 0.5-2% | &lt;0.5% | Hard bounces above 2% damage sender reputation [4] |
| Unsubscribe rate | &gt;0.5% | 0.1-0.3% | &lt;0.1% | Per-send basis |
| Spam complaint rate | &gt;0.1% | 0.02-0.05% | &lt;0.02% | Must stay under 0.1% per Google/Yahoo requirements [4] |

**Source:** Mailchimp industry benchmarks, ActiveCampaign 2025 benchmarks, The Digital Bloom B2B deliverability report [4][8]

**Interpretation:**
- **Below low:** Investigate list hygiene, authentication settings, content quality. Possible blocklisting.
- **Above high:** Indicates a highly engaged, well-segmented list. Maintain current practices.

### Lead Funnel Conversion Benchmarks (B2B SaaS)

| Metric | Low | Typical | High | Notes |
|--------|-----|---------|------|-------|
| Visitor-to-Lead | &lt;1% | 2-4% | &gt;5% | Depends heavily on traffic quality and form strategy |
| Lead-to-MQL | &lt;5% | 10-20% | &gt;25% | Scoring model accuracy is the primary lever |
| MQL-to-SQL | &lt;10% | 15-25% | &gt;30% | Alignment between marketing scoring and sales acceptance criteria |
| SQL-to-Opportunity | &lt;30% | 40-60% | &gt;70% | Reflects qualification process quality |
| Opportunity-to-Close | &lt;10% | 15-25% | &gt;30% | Outside MAP scope, but validates upstream quality |

**Source:** Martal Group B2B benchmarks, Landbase lead qualification statistics, Callin B2B SaaS benchmarks [2][9]

**Interpretation:**
- **MQL-to-SQL below 10%:** Scoring model is too loose. Marketing is passing leads that sales rejects. Tighten demographic gates.
- **MQL-to-SQL above 30%:** Scoring model may be too conservative. Marketing might be holding leads too long. Review score thresholds.

### IP Warming Timeline Benchmarks

| Week | Daily Volume Target | Focus |
|------|-------------------|-------|
| Week 1 | 50-200 emails/day | Most engaged subscribers only (opened/clicked in last 30 days) |
| Week 2 | 200-1,000 emails/day | Expand to 60-day engaged subscribers |
| Week 3 | 1,000-5,000 emails/day | Include 90-day engaged subscribers |
| Week 4 | 5,000-25,000 emails/day | Full active list |
| Week 5-8 | Ramp to full volume | Monitor and adjust based on deliverability metrics |

**Source:** SparkPost IP warm-up guide, Litmus email warm-up guide, WP Mail SMTP [5]

**Key rule:** Double volume approximately every 2-3 days. If bounce rate exceeds 2% or complaint rate exceeds 0.1% at any stage, pause and investigate before continuing.

### Quick Reference Thresholds

| Question | Good | Warning | Red Flag |
|----------|------|---------|----------|
| Is email deliverability healthy? | &gt;95% inbox placement | 89-95% | &lt;89% |
| Is lead scoring working? | MQL-to-SQL &gt;20% | 10-20% | &lt;10% |
| Is CRM sync reliable? | &lt;0.5% sync errors | 0.5-2% errors | &gt;2% errors |
| Is data quality adequate? | &lt;5% duplicate rate | 5-15% | &gt;15% |
| Is the team adopting the platform? | &gt;80% of campaigns in MAP | 50-80% | &lt;50% |

---

## 4) Calculations &amp; Scoring

### Formula Quick Reference

| Calculation | Formula | Example |
|-------------|---------|---------|
| Lead Score | `Demographic Score + Behavioral Score` | Fit: 40 pts + Engagement: 55 pts = 95 (MQL threshold: 80) |
| MQL-to-SQL Rate | `(SQLs / MQLs) x 100` | 45 SQLs / 200 MQLs = 22.5% |
| Email Engagement Rate | `(Unique Clicks / Delivered) x 100` | 150 clicks / 5,000 delivered = 3.0% CTR |
| Marketing-Sourced Pipeline | `Sum of Opps where First Touch = Marketing` | $450K of $1.2M total pipeline = 37.5% |
| Cost Per MQL | `Marketing Spend / MQLs Generated` | $50,000 / 200 MQLs = $250/MQL |

### Lead Scoring Model Design

**Formula:**

```
Total Score = Demographic Score (max 50) + Behavioral Score (max 100)
MQL Threshold = 80 points (requires minimum 20 demographic points)
```

**Variables explained:**
- `Demographic Score` = Points assigned based on firmographic and demographic attributes (job title, company size, industry, geography). Represents buyer **fit**.
- `Behavioral Score` = Points assigned based on engagement actions (email clicks, page visits, content downloads, form submissions). Represents buyer **intent**.
- `MQL Threshold` = The combined score at which a lead is flagged as marketing-qualified and routed to sales.

**Worked Example:**

*Scenario: SaaS company selling to mid-market B2B. Target buyer is a VP of Marketing at a 100-500 employee company.*

```
Demographic Scoring:
- Title: VP Marketing = 20 pts (Director = 15, Manager = 10, Individual contributor = 5)
- Company size: 200 employees = 15 pts (100-500 range)
- Industry: SaaS/Technology = 10 pts (target industry)
- Geography: US = 5 pts (primary market)
- Demographic subtotal = 50 pts

Behavioral Scoring:
- Visited pricing page (2x) = 20 pts (10 pts each, high-intent page)
- Downloaded whitepaper = 10 pts
- Opened 3 nurture emails = 6 pts (2 pts each)
- Clicked CTA in email = 5 pts
- Attended webinar = 15 pts
- Behavioral subtotal = 56 pts

Total Score: 50 + 56 = 106 pts → Exceeds MQL threshold (80) → Route to sales
```

**Validation:**
- If &gt;40% of MQLs are rejected by sales, demographic scoring is too loose
- If &lt;5% of scored leads ever reach MQL, behavioral thresholds are too aggressive
- Recalibrate every 90 days using closed-won deal data

### Lead Score Degradation

**Formula:**

```
Degradation: Reduce behavioral score by 10% every 30 days of inactivity
Reset: If no activity for 90 days, reset behavioral score to 0
```

**Why it matters:** A lead who scored 85 points six months ago but has not engaged since is not sales-ready. Degradation prevents stale MQLs from cluttering the pipeline.

### Scoring Rubrics

**Demographic Scoring Rubric:**

| Criterion | Points | Threshold |
|-----------|--------|-----------|
| Job Title (C-level/VP) | 20 pts | Decision-maker title matching ICP |
| Job Title (Director) | 15 pts | Influencer-level title |
| Job Title (Manager) | 10 pts | Practitioner who can champion |
| Company Size (ICP range) | 15 pts | Within target employee/revenue range |
| Industry (target) | 10 pts | Primary target vertical |
| Geography (primary market) | 5 pts | In-region |
| **Negative: Competitor** | -50 pts | Disqualify immediately |
| **Negative: Student/Personal email** | -30 pts | Not a buyer |
| **Total possible** | **50 pts** | |

**Behavioral Scoring Rubric:**

| Criterion | Points | Threshold |
|-----------|--------|-----------|
| Pricing page visit | 10 pts/visit | High-intent signal (cap at 30) |
| Demo request form fill | 25 pts | Strongest intent signal |
| Content download | 10 pts | Engaged with educational content |
| Webinar attendance | 15 pts | Active participation |
| Email click | 5 pts | Engaged with nurture |
| Email open | 2 pts | Minimal engagement (cap at 10) |
| Blog visit | 3 pts | Awareness-stage activity (cap at 15) |
| **Total possible** | **100 pts** | |

**Tier Thresholds:**
- MQL: 80+ points (with minimum 20 demographic points)
- Warm Lead: 50-79 points (continue nurturing)
- Cold Lead: Below 50 points (early-stage nurture or not a fit)

### Attribution Model Calculations

**W-Shaped Model (recommended for most B2B):**

```
First Touch: 30% credit
Lead Creation: 30% credit
Opportunity Creation: 30% credit
All other touchpoints: 10% split evenly
```

**Worked Example:**

*Scenario: A $50,000 deal with 8 touchpoints.*

```
Touchpoint 1 (First Touch): Google Ads click → $15,000 credit (30%)
Touchpoint 2: Blog post read → $1,000 credit (10% / 5 remaining = 2% each)
Touchpoint 3 (Lead Creation): Whitepaper download → $15,000 credit (30%)
Touchpoint 4: Nurture email click → $1,000 credit
Touchpoint 5: Webinar attendance → $1,000 credit
Touchpoint 6: Case study download → $1,000 credit
Touchpoint 7 (Opp Creation): Demo request → $15,000 credit (30%)
Touchpoint 8: Proposal review → $1,000 credit

Total attributed: $50,000
```

---

## 5) Edge Cases &amp; Deep Dives

### Edge Case 1: Marketo-to-HubSpot Migration with Custom Objects

*Scenario:*

Client is migrating from Marketo to HubSpot. Their Marketo instance uses custom objects for product interest tracking, event attendance history, and partner referral data. HubSpot does not have the same custom object flexibility.

*Challenge:*

Marketo's custom objects allow arbitrary relational data structures. HubSpot's custom objects (available on Enterprise) have tighter constraints on relationships and field limits. A 1:1 migration is not possible for all data structures.

*Approach:*

1. Audit all Marketo custom objects and classify: (a) must migrate, (b) nice-to-have, (c) can deprecate
2. For must-migrate objects, map to HubSpot custom objects where structure allows
3. For objects that do not fit HubSpot's model, flatten into custom properties on the Contact or Company record
4. For historical data that is reference-only, export to a data warehouse (BigQuery, Snowflake) and link via reporting rather than migrating into HubSpot
5. Document all transformations and share with client for approval before execution

*Key validation:*

Run a reconciliation report comparing Marketo record counts and field population rates against HubSpot post-migration. Variance should be under 1% for contacts and under 5% for activity data.

---

### Edge Case 2: Multi-Business Unit Configuration

*Scenario:*

Client has 3 product lines, each with its own marketing team, brand, and target audience, but shares a single CRM instance. They need one MAP with separation between business units.

*Challenge:*

Marketing teams must not see or accidentally email each other's contacts. But sales leadership needs unified reporting across all BUs. Shared contacts (companies that are prospects for multiple products) must be handled without duplication.

*Approach:*

1. Use HubSpot Business Units (Enterprise) or Marketo Workspaces/Partitions to create logical separation
2. Assign each BU its own sending domain, email templates, and lead scoring model
3. Create shared properties for cross-BU data (company-level fields) with BU-specific properties for lead-level data
4. Build routing rules that evaluate BU membership before assigning leads
5. Create unified dashboards with BU filters for leadership, and BU-specific dashboards for each marketing team

*Key validation:*

Send test campaigns from each BU and verify: (a) only the correct audience receives the email, (b) unsubscribes are BU-specific (not global), (c) lead scoring is independent per BU, (d) CRM sync respects BU ownership.

---

### Edge Case 3: Deliverability Crisis Post-Migration

*Scenario:*

Client migrated to a new MAP, skipped or rushed IP warming, and within the first week of full-volume sending, deliverability dropped below 70%. Emails are landing in spam across Gmail, Outlook, and Yahoo.

*Challenge:*

Recovering from a deliverability crisis takes 4-8 weeks -- longer than the original warming period would have taken. The client's marketing programs are effectively halted.

*Approach:*

1. Immediately reduce send volume to 10% of current
2. Verify SPF, DKIM, and DMARC records are correctly configured and passing validation
3. Check blocklists (Spamhaus, Barracuda, SORBS) and request delisting if applicable
4. Send only to the most engaged segment (opened/clicked in last 30 days) for 2 weeks
5. Monitor deliverability daily using seed lists and inbox placement tools (GlockApps, Validity)
6. Gradually increase volume following the standard IP warming schedule (see Benchmarks section)
7. Do not resume full volume until inbox placement exceeds 90% for 5 consecutive days

---

### Edge Case 4: Legacy Platform Has No Export Capability

*Scenario:*

Client is migrating from a legacy or niche MAP that does not offer extended data export, API access, or standard export formats.

*Challenge:*

Without export capability, you cannot extract contact records, engagement history, or workflow configurations programmatically.

*Approach:*

1. Check if the platform offers any reporting-based export (most platforms allow CSV export from reports)
2. If available, build reports that capture all required fields and export in segments (e.g., A-D contacts, E-H contacts)
3. If no export exists, check for API documentation -- even limited APIs can be scripted for batch extraction
4. As last resort, use the CRM as the migration source (since CRM should have synced contact data) and accept loss of MAP-specific data (engagement history, campaign membership)
5. Document what data is lost and communicate to client before proceeding

*Key validation:*

Compare record counts between legacy system (from UI counts) and extracted data. If variance exceeds 5%, investigate missing segments before proceeding.

---

### Edge Case 5: Shared Lead Pool Between Marketing and Sales (No Clear MQL Handoff)

*Scenario:*

Client's sales team currently picks leads directly from the MAP or from the same lists marketing uses. There is no MQL stage, no scoring, and no formal handoff process. Marketing and sales both claim ownership of the same leads.

*Challenge:*

Implementing lead scoring and MQL handoff represents a process change, not just a technology change. Sales may resist losing direct access to leads. Marketing may not have credibility to "gate" leads.

*Approach:*

1. Run scoring model in "shadow mode" for 30 days -- score leads but do not change routing or access
2. At 30 days, present data: "Of leads sales worked that scored below MQL threshold, X% converted vs. Y% for leads above threshold"
3. Use data to gain buy-in for MQL-based routing
4. Implement a transitional period where sales can still access all leads but MQLs are highlighted/prioritized
5. After 60 days with positive data, move to formal MQL handoff with SLA

*Key validation:*

Track conversion rates for MQL-routed leads vs. self-selected leads over 90 days. If MQL-routed leads convert at a higher rate, the model is validated.

---

## References

[1] [inBeat Agency - 70 Marketing Automation Statistics 2025](https://inbeat.agency/blog/marketing-automation-statistics)

[2] [Martal Group - B2B Lead Scoring: Top Practices Driving Results in 2025](https://martal.ca/b2b-lead-scoring-lb/)

[3] [MarCloud Consulting - HubSpot Salesforce Field Mapping Best Practices](https://marcloudconsulting.com/development/hubspot-salesforce-field-mapping/)

[4] [The Digital Bloom - B2B Email Deliverability 2025 Benchmarks](https://thedigitalbloom.com/learn/b2b-email-deliverability-benchmarks-2025/)

[5] [WP Mail SMTP - IP Warming Schedules Overview](https://wpmailsmtp.com/ip-warming/)

[6] [Factors.ai - Top Multi-Touch Attribution Models](https://www.factors.ai/blog/best-multi-touch-attribution-models)

[7] [SUPALABS - AI Marketing Automation Platforms Comparison 2025](https://www.supalabs.co/en/blog/ai-marketing-automation-platforms-comparison-2025-hubspot-marketo-pardot-activecampaign)

[8] [Mailchimp - Email Marketing Benchmarks &amp; Industry Statistics](https://mailchimp.com/resources/email-marketing-benchmarks/)

[9] [Landbase - 35 Lead Qualification Statistics for B2B Sales 2026](https://www.landbase.com/blog/lead-qualification-statistics)
