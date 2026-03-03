# CRM Deduplication — Methodology

This document covers the core concepts, frameworks, and calculations behind CRM Deduplication. It provides the methodological foundation — the 'how it works' behind the execution steps.

---

## 1) Core Concepts

### What Is a Duplicate Record?

*What is it?*

A duplicate record is two or more entries in a CRM that represent the same real-world person, company, or entity. Duplicates range from exact copies (same email, same name) to near-matches where data entry variations create records that look different but refer to the same contact -- "Robert Smith at Acme Inc." and "Bob Smith at ACME" are the same person.

*Why does it matter?*

Duplicate records erode trust in CRM data across sales, marketing, and CS. Sales reps waste time on leads already being worked. Marketing inflates audience counts and sends duplicate emails. Attribution models break when the same person exists across multiple records. 91% of CRM data is estimated to be incomplete, stale, or duplicated in any given year [1]. Bad data costs the average organization $12.9 million annually according to Gartner [2].

*Key insight:*

> Duplicates are not a data problem -- they are a revenue problem. Every duplicate contact is a potential routing error, a broken automation, and a missed attribution. The CRM becomes unreliable not because of one bad record, but because thousands of small duplications compound into systemic distrust.

*Examples:*

| Context | Example |
|---------|---------|
| Exact duplicate | Two contact records with identical email `jsmith@acme.com` created by different reps |
| Fuzzy duplicate | "Robert Smith" at "Acme Inc" and "Bob Smith" at "ACME Incorporated" -- same person, different data entry |
| Cross-object duplicate | A Lead record and a Contact record for the same person, never converted |
| Account-level duplicate | "Acme Inc.", "Acme, Inc.", and "ACME Incorporated" -- three account records for one company |

### Matching Theory: How Deduplication Identifies Duplicates

*What is it?*

Matching is the algorithmic process of comparing records to determine whether they represent the same entity. It operates on a spectrum from exact matching (field values are identical) to fuzzy matching (field values are similar within a defined tolerance). The matching layer is the core engine of any deduplication project -- every other decision flows from how well matching performs.

*Why does it matter?*

Matching accuracy directly determines whether you clean up legitimate duplicates (true positives) or accidentally merge distinct records (false positives). A 2% false positive rate on a 100,000-record database means 2,000 records incorrectly merged -- potentially destroying deal history, notes, and relationships.

*The Framework:*

```
Record A fields ──┐
                   ├── Matching Algorithm ──> Confidence Score (0-100%)
Record B fields ──┘
                                                    │
                                        ┌───────────┼───────────┐
                                        │           │           │
                                    Auto-Merge   Review Queue   No Match
                                    (95-100%)    (70-94%)       (<70%)
```

**Matching methods ranked by precision:**

| Method | What It Compares | Best For | Limitation |
|--------|-----------------|----------|------------|
| Exact match | Character-for-character identity | Email addresses, phone numbers | Misses "Bob" vs "Robert" |
| Levenshtein distance | Minimum edits to transform string A into string B | Typos, minor spelling variations | Slow on large datasets |
| Jaro-Winkler | Character transposition tolerance weighted toward string start | Name matching | Less effective on short strings |
| Soundex / Metaphone | Phonetic encoding of words | Name pronunciation variants ("Smith" vs "Smyth") | Language-dependent |
| N-gram fingerprinting | Overlapping character sequences | Company name variations | Can match unrelated strings |

*Common misunderstandings:*

- **Misconception:** Exact email match catches all duplicates.
  **Reality:** Email match catches roughly 40-60% of duplicates. The rest require fuzzy matching on name + company combinations. People use multiple email addresses, and records created from different sources often have different email fields populated.

- **Misconception:** More matching rules = better deduplication.
  **Reality:** Overly broad matching rules increase false positives faster than they reduce false negatives. Start tight (exact email), validate accuracy, then widen incrementally. Salesforce limits you to five active matching rules per object for this reason [3].

### Data Survivorship: Building the Golden Record

*What is it?*

Data survivorship (also called "master record selection") is the set of rules that determine which field values survive when two or more duplicate records are merged into one. The surviving record -- the "golden record" -- should contain the most complete, most recent, and most accurate data from all duplicate copies.

*Why does it matter?*

A merge that keeps the wrong data is worse than no merge at all. If the surviving record keeps an outdated phone number, loses 6 months of activity history, or drops a critical integration ID, the merge has created a new data problem while solving the old one. Picking the right master record determines the effectiveness of any deduplication campaign [4].

*The Framework:*

Survivorship operates at two levels:

**1. Master record selection** -- which record becomes the surviving container:

| Selection Criterion | When to Use | Example |
|---------------------|------------|---------|
| Most recent activity | Active sales cycles | Record with last activity 2 days ago beats record untouched for 6 months |
| Most complete data | Data enrichment contexts | Record with 18/20 fields populated beats record with 8/20 |
| Oldest created date | Preserving historical timeline | Original inbound lead from 2022 beats re-import from 2024 |
| Lifecycle stage priority | Complex funnel tracking | "Customer" record wins over "Lead" record for same person |
| Integration ID presence | Multi-system environments | Record with Salesforce sync ID preserved over record without |

**2. Field-level survivorship** -- for each field, which value wins:

| Strategy | Logic | Best For |
|----------|-------|----------|
| Most recent value | Latest non-null value across records | Phone, title, address |
| Longest value | Most characters (usually most complete) | Notes, descriptions |
| Concatenate | Combine values from all records | Tags, notes where each record may have unique info |
| Source priority | Prefer value from trusted source | Integration IDs, verified emails |
| Most frequent | Value appearing in the most records | Company name standardization |

*Common misunderstandings:*

- **Misconception:** The oldest record should always be the master.
  **Reality:** The oldest record often has the most stale data. Master selection should be context-dependent -- most recent activity for active accounts, most complete data for enrichment, lifecycle stage for funnel integrity.

- **Misconception:** Field merge behavior is the same for every field.
  **Reality:** Different fields need different survivorship rules. Email should use source priority (verified over unverified). Phone should use most recent. Notes should concatenate. A single "keep master value" rule across all fields guarantees data loss.

### Duplicate Prevention vs. Duplicate Cleanup

*What is it?*

Deduplication has two distinct workstreams: **cleanup** (finding and merging existing duplicates) and **prevention** (stopping new duplicates from being created). Most projects focus heavily on cleanup and underinvest in prevention, leading to a cycle where duplicates return within weeks.

*Why does it matter?*

92% of duplicate records are created during initial data entry phases when users create new records instead of searching for existing ones [5]. Without prevention rules, even a perfectly cleaned database will accumulate new duplicates at a rate proportional to record creation volume.

*Key insight:*

> Cleanup without prevention is a subscription to repeat work. Prevention without cleanup is governance on a dirty foundation. Both must happen, and prevention must come *with* cleanup -- not "someday after."

*Examples:*

| Context | Example |
|---------|---------|
| Prevention via alert | Rep types "John Smith" into new Contact form, CRM shows alert: "Potential match: John Smith at Acme (existing contact)" |
| Prevention via validation | Import CSV requires email column; rows without email are rejected to prevent unmatchable records |
| Prevention via standardization | Workflow auto-lowercases email, trims whitespace, and normalizes "Inc." / "Incorporated" / "Inc" at entry |
| Ongoing detection | Weekly scheduled scan finds 15 new potential duplicate pairs, queues for admin review |

---

## 2) Decision Frameworks

### Approach Selection Matrix

| Situation | Recommended Approach | Why |
|-----------|---------------------|-----|
| Database &lt;10,000 records, Salesforce or HubSpot | Native CRM tools only | Built-in duplicate management handles exact matches; volume is manageable for manual review of edge cases |
| Database 10,000-100,000 records, moderate duplicate rate (&lt;15%) | Native CRM tools + lightweight third-party (Dedupely, Koalify) | Native handles prevention; third-party adds fuzzy matching for cleanup |
| Database &gt;100,000 records or duplicate rate &gt;20% | Full third-party tool (Insycle, Cloudingo, DemandTools) | Need batch processing, advanced fuzzy matching, and automated merge rules at scale |
| Multi-CRM environment (Salesforce + HubSpot sync) | Full third-party tool + integration-aware merge strategy | Must account for sync behavior; merging in one system can create orphans in the other |
| Post-migration cleanup | Full third-party tool with rollback capability | Migrations generate high duplicate volumes; need preview and undo capabilities |

### Scoping Factors

**1. CRM Platform**

- Salesforce → Native Duplicate Management (matching rules + duplicate rules, up to 5 per object [3]) + third-party for fuzzy matching
- HubSpot → Native deduplication (Operations Hub Professional+) + Koalify/Insycle/Dedupely for advanced matching [6]
- Other CRM → Almost always requires third-party tool

**2. Database Size**

- &lt;10K records → Manual review feasible for edge cases, native tools sufficient
- 10K-50K records → Semi-automated approach, batch sizes of 500-1000
- 50K-500K records → Fully automated with human review of low-confidence matches only
- 500K+ records → Requires high-performance tool with parallel processing, strict batching

**3. Integration Complexity**

- Standalone CRM → Standard deduplication workflow
- CRM + MAP (Salesforce + HubSpot/Marketo) → Must coordinate merge timing; pause sync during extended operations
- CRM + ERP + MAP → Integration ID preservation is critical; each system's unique identifiers must survive merges

**4. Duplicate Rate Severity**

- &lt;10% duplicate rate → Cleanup is a tune-up; focus on prevention rules
- 10-25% duplicate rate → Standard deduplication project; full cleanup + prevention
- &gt;25% duplicate rate → Major data quality remediation; consider phased approach starting with highest-value records

**5. Data Governance Maturity**

- No existing governance → Must build governance alongside cleanup
- Basic governance (some naming standards) → Extend existing framework with deduplication-specific rules
- Mature governance → Focus on tool configuration and process integration

### Native CRM Tools Approach

*Best for:*
- Small databases (&lt;10K records)
- Exact-match-dominant duplicate problems
- Teams with Salesforce Admin or HubSpot Operations Hub access
- Prevention-focused projects (alerting, blocking)

*Not recommended for:*
- Large-scale cleanup (&gt;10K duplicates to merge)
- Fuzzy matching requirements ("Bob" vs "Robert")
- Multi-object deduplication in a single pass
- Environments needing preview/undo capability

*Key differences from third-party:*

| Aspect | Native CRM | Third-Party Tool |
|--------|------------|------------------|
| Matching | Exact + limited fuzzy | Advanced fuzzy, phonetic, N-gram |
| Merge preview | Limited or none | Full preview with field-by-field comparison |
| Batch processing | Manual, record-by-record | Automated batches of 500-5000+ |
| Rollback | No native undo | Most offer undo/rollback window |
| Cost | Included in CRM license | $30-500+/month depending on scale |
| Custom survivorship | Basic (keep master value) | Field-level rules (most recent, longest, concatenate) |

### Third-Party Tool Approach

*Best for:*
- Databases &gt;10K records
- Duplicate rates &gt;15%
- Fuzzy matching needs (name variants, company abbreviations)
- Environments requiring audit trail and rollback
- Multi-object deduplication

*Not recommended for:*
- Tiny databases where manual review is faster than tool setup
- One-time micro-cleanups (&lt;500 duplicates)

*Tool selection factors:*

| Factor | Insycle | Dedupely | Koalify | Cloudingo | DemandTools |
|--------|---------|----------|---------|-----------|-------------|
| Primary CRM | HubSpot, Salesforce | HubSpot, Salesforce, Pipedrive | HubSpot only | Salesforce only | Salesforce only |
| Fuzzy matching | Advanced (any field, custom rules) | Basic-moderate | Moderate (HubSpot-native) | Advanced | Advanced |
| Pricing entry | ~$30/mo (30K records) | Free tier available | ~50% cheaper than competitors for large portals | ~$15/user/mo | ~$20/user/mo |
| Rollback | Yes | Limited | Yes | Yes | Yes |
| Best fit | Complex rules, multi-object | Simple dedup, budget-conscious | HubSpot-native automation | Salesforce power users | Salesforce admins with complex needs |

---

## 3) Benchmarks & Standards

### How to Use Benchmarks

Benchmarks are guidelines, not rules. Always:
1. Start with benchmark as baseline
2. Adjust based on client-specific data
3. Validate against their actual numbers when available
4. Document deviations and rationale

### Duplicate Rate Benchmarks

| Metric | Low | Typical | High | Notes |
|--------|-----|---------|------|-------|
| Contact duplicate rate | 5-10% | 15-25% | 30-50% | Uncleaned databases average 20-30% [7] |
| Lead duplicate rate | 10-15% | 20-30% | 40-60% | Higher than contacts due to form submissions and imports |
| Account duplicate rate | 3-5% | 8-15% | 20-30% | Lower volume but higher impact per duplicate |
| Post-cleanup target rate | &lt;1% | 1-3% | 3-5% | 1% is the achievable industry standard; 22% of organizations meet it [1] |
| New duplicate creation rate | &lt;1%/month | 2-5%/month | &gt;5%/month | With prevention rules active, target &lt;1% |

**Source:** Landbase Duplicate Record Rate Statistics 2026 [1]

**Interpretation:**
- **Below low:** Either very clean data governance already exists, or the audit methodology is too narrow (only checking exact email matches)
- **Above high:** Indicates systemic data entry problems -- multiple uncontrolled entry points, no validation rules, extended imports without dedup checks

### Matching Accuracy Benchmarks

| Metric | Good | Warning | Red Flag |
|--------|------|---------|----------|
| False positive rate (records flagged as duplicates that are not) | &lt;2% | 2-5% | &gt;5% |
| False negative rate (true duplicates missed by matching rules) | &lt;10% | 10-20% | &gt;20% |
| Match confidence threshold for auto-merge | 95-100% | 85-94% | &lt;85% |
| Match confidence threshold for review queue | 70-94% | 60-69% | &lt;60% |

**Source:** Insycle deduplication best practices [4], Data Ladder fuzzy matching guide [8]

**Interpretation:**
- **False positive rate &gt;5%:** Matching rules are too loose. Tighten fuzzy thresholds, add secondary confirmation fields (e.g., require email OR company+name match, not just name alone)
- **False negative rate &gt;20%:** Matching rules are too tight. Consider adding fuzzy matching, phonetic matching, or lowering similarity thresholds

### Data Decay Benchmarks

| Metric | Rate | Impact |
|--------|------|--------|
| B2B contact data decay | ~70% per year [9] | Even clean databases accumulate stale records that generate new duplicates when re-entered from fresh sources |
| Job title change frequency | ~30% per year | Title changes on existing records create matching confusion |
| Company name/domain changes | ~5-10% per year | Mergers, acquisitions, and rebrands create account-level duplicates |
| Email address changes | ~20-30% per year | People change jobs, companies change domains |

**Source:** Various B2B data quality reports [9]

### Quick Reference Thresholds

| Question | Good | Warning | Red Flag |
|----------|------|---------|----------|
| What duplicate rate is acceptable post-cleanup? | &lt;3% | 3-5% | &gt;5% |
| How many records should I review manually in test batch? | 50+ pairs | 25-50 | &lt;25 |
| How long before duplicates return without prevention? | 6+ months | 2-6 months | &lt;2 months |
| What batch size for extended merges? | 500-1000 | 1000-3000 | &gt;3000 |
| How often should recurring scans run? | Weekly | Monthly | Quarterly or never |

---

## 4) Calculations & Scoring

### Formula Quick Reference

| Calculation | Formula | Example |
|-------------|---------|---------|
| Duplicate rate | `(duplicate records / total records) x 100` | 5,000 duplicates / 25,000 total = 20% |
| Records after merge | `total records - (duplicate pairs x merge ratio)` | 25,000 - (2,500 x 1) = 22,500 |
| False positive rate | `(false matches / total flagged matches) x 100` | 8 false / 200 flagged = 4% |
| Estimated time saved | `(duplicates resolved x minutes per manual resolution) / 60` | 2,500 x 15 min / 60 = 625 hours |
| Cost of duplicates | `duplicate records x cost per bad record` | 5,000 x $10 = $50,000 |

### Duplicate Rate Calculation

**Formula:**
```
Duplicate Rate = (Number of Duplicate Records / Total Records in Object) x 100
```

**Variables explained:**
- `Number of Duplicate Records` = Count of records identified as duplicates by matching rules (not the number of duplicate *pairs* -- count each extra record beyond the first)
- `Total Records in Object` = Total contacts, leads, or accounts in the CRM object

**Worked Example:**

*Scenario: Mid-market SaaS company, 30,000 contacts in Salesforce*

```
Given:
- Total contacts: 30,000
- Duplicate scan identifies 3,200 duplicate pairs (6,400 records involved)
- Each pair merges 2 → 1, so 3,200 records to be removed

Calculate:
- Duplicate rate: (6,400 / 30,000) x 100 = 21.3%
- Records after merge: 30,000 - 3,200 = 26,800
- Reduction: 10.7% fewer records
```

**Validation:**
- A 20-25% duplicate rate is typical for an uncleaned B2B database [7]
- If the calculated rate is below 5%, the matching rules may be too strict
- If above 40%, verify the matching rules are not producing excessive false positives

### ROI Estimation

**Formula:**
```
Annual ROI = (Time Savings + Revenue Recovery + Tool Cost Savings) - Project Cost
```

**Variables explained:**
- `Time Savings` = Hours saved per rep per week x hourly cost x number of reps x 52 weeks. Sales reps lose approximately 550 hours annually to inaccurate CRM data [10]
- `Revenue Recovery` = Percentage of revenue lost to bad data x annual revenue. Companies lose an estimated 10-12% of revenue to poor CRM data quality [11]
- `Tool Cost Savings` = Reduction in CRM license costs if deduplication reduces record count below a pricing tier
- `Project Cost` = Consulting fees + tool licensing + internal time commitment

**Worked Example:**

*Scenario: $15M ARR B2B SaaS, 20 sales reps, 50,000 CRM records, 22% duplicate rate*

```
Given:
- Reps save 1 hour/week on duplicate-related confusion
- Fully loaded rep cost: $75/hour
- Conservative revenue recovery: 1% (not the full 10-12%, just direct duplicate impact)
- Dedup tool: $200/month
- Project cost: $15,000

Calculate:
- Time savings: 1 hr x $75 x 20 reps x 52 weeks = $78,000/year
- Revenue recovery: 1% x $15,000,000 = $150,000/year
- Tool cost: $2,400/year
- Net annual ROI: ($78,000 + $150,000 - $2,400) - $15,000 = $210,600
```

**Validation:**
- If ROI exceeds $500K for a company under $10M ARR, the revenue recovery percentage is likely too aggressive
- Time savings alone should justify the project for most mid-market companies

### Match Confidence Scoring

**Scoring Rubric:**

| Criterion | Points | Threshold |
|-----------|--------|-----------|
| Exact email match | 50 pts | Identical email address (case-insensitive) |
| Fuzzy name match (&gt;90% Jaro-Winkler) | 20 pts | First + last name within 90% similarity |
| Company name match (&gt;85% similarity) | 15 pts | After normalization (trim, lowercase, remove Inc/LLC) |
| Phone number match | 10 pts | After standardization (remove spaces, dashes, country code) |
| Domain match | 5 pts | Email domain or website domain matches |
| **Total** | **100 pts** | |

**Tier Thresholds:**
- **Auto-merge:** 95+ points (exact email + at least one confirming field)
- **Review queue:** 70-94 points (strong fuzzy match, needs human verification)
- **No action:** Below 70 points (insufficient evidence of duplication)

*Note: These weights are a starting point. Adjust based on client's data quality and matching patterns.*

---

## 5) Edge Cases & Deep Dives

### Edge Case 1: Free Email Domains (Gmail, Yahoo, Hotmail)

*Scenario:*

Two contacts share the email address format `firstname.lastname@gmail.com`, or multiple contacts at different companies all use `@gmail.com` domains. Matching on email alone would incorrectly flag different people as duplicates, or conversely, a person using a personal Gmail across multiple form fills would not match their corporate email record.

*Challenge:*

Free email domains cannot be used as company-level grouping signals. "jsmith@gmail.com" at Company A is a different context than "jsmith@gmail.com" at Company B. But they may also be the same person who submitted two forms at different times.

*Approach:*

1. Exclude free email domains from domain-based matching rules
2. For records with free emails, require name + company match as secondary criteria
3. Never auto-merge records where both have free email domains -- route to review queue
4. Flag free email contacts for data enrichment (use ZoomInfo or Apollo to find corporate email)

*Fallback assumptions:*

| Missing Data | Use This Instead | Source |
|--------------|------------------|--------|
| Corporate email | Free email + company name + full name match at &gt;90% | Requires 3-field match to compensate for missing anchor field |
| Company name on free-email record | IP-based enrichment or form field "Company" | Many form fills with free emails have company populated separately |

*Key validation:*

Check the false positive rate specifically for free-email matches. It should be reviewed separately from the overall false positive rate, as it will be higher.

### Edge Case 2: HubSpot-Salesforce Integration Active During Merge

*Scenario:*

Client runs both HubSpot (marketing) and Salesforce (sales) with bidirectional sync enabled. Merging contacts in HubSpot while the integration is active can create orphaned records in Salesforce, break association mappings, or trigger sync conflicts that re-create deleted records.

*Challenge:*

HubSpot cannot merge company records when the Salesforce integration is active [7]. Contact merges may propagate unpredictably depending on sync field mappings and conflict resolution settings. A merge in one system does not automatically merge the corresponding record in the other.

*Approach:*

1. Document the full sync field mapping before starting (which fields sync, which direction, conflict resolution)
2. For company/account merges: pause the integration, merge in the primary system, then re-enable and verify
3. For contact merges: test 5-10 merges with sync active and verify behavior in both systems
4. Merge in the system of record first (usually Salesforce for sales data, HubSpot for marketing data)
5. After extended merge in primary system, run duplicate scan in secondary system to catch orphans

*Fallback assumptions:*

| Missing Data | Use This Instead | Source |
|--------------|------------------|--------|
| Sync field mapping documentation | Export HubSpot Settings &gt; Integrations &gt; Salesforce field mappings | Available in HubSpot UI |
| Conflict resolution settings | Default is "most recent update wins" | Verify in HubSpot sync settings before proceeding |

*Key validation:*

After merge, compare record counts in both systems. Salesforce contact count and HubSpot contact count should be within 5% of each other (exact match is unlikely due to different counting logic).

### Edge Case 3: Bulk Import Creates Mass Duplicates

*Scenario:*

A list import (from event, purchased list, or partner) creates hundreds or thousands of duplicates in a single batch because the import was not deduplicated against existing records before upload.

*Challenge:*

The duplicates from a single import often have identical data quality (same source, same timestamp), making master record selection ambiguous. If the import included new data not in existing records (e.g., event attendance, specific campaign response), you need to preserve that data during merge.

*Approach:*

1. Isolate import-created records using created date and source field
2. Run deduplication scan scoped to "import records vs. existing records" (not import records vs. each other)
3. Set survivorship rule: existing record is always master (it has historical activity)
4. Set field-level rule: for fields populated in import but empty in existing record, take import value
5. After merge, verify campaign membership and list associations transferred correctly

*Fallback assumptions:*

| Missing Data | Use This Instead | Source |
|--------------|------------------|--------|
| Source field not populated on import | Use created date range to identify import batch | Filter for records created within the import time window |
| No campaign association on import records | Manually associate surviving records with original campaign | Preserves attribution for the event/list |

*Key validation:*

Count records in the import campaign before and after merge. Campaign member count should remain the same (just pointing to surviving records instead of duplicates).

### Edge Case 4: Duplicate Accounts with Different Ownership

*Scenario:*

Two account records exist for the same company, each owned by a different sales rep, each with different opportunities and activity history. Merging would reassign all opportunities to one rep.

*Challenge:*

This is not just a data problem -- it is a territory and compensation problem. Merging accounts without sales leadership alignment can cause rep conflicts and trust issues.

*Approach:*

1. Flag multi-owner account duplicates separately from standard duplicates
2. Route to sales leadership for ownership decision before merge
3. Document the merge's impact: which opportunities move, which rep loses account ownership
4. Consider timing: merge after quarter close if active deals exist on both accounts
5. Update territory assignments and routing rules post-merge to prevent re-creation

*Fallback assumptions:*

| Missing Data | Use This Instead | Source |
|--------------|------------------|--------|
| Territory rules not documented | Ask sales leadership which rep "should" own the account based on current rules | This is a business decision, not a data decision |
| Active opportunity impact unclear | Run report: opportunities by account for both duplicate accounts, show to sales manager | Let stakeholders see the full picture before deciding |

*Key validation:*

After merge, verify all opportunities are associated with surviving account and correct owner. Run pipeline report pre- and post-merge to confirm no revenue dropped.

### Edge Case 5: Records with Conflicting Data Across Fields

*Scenario:*

Two duplicate records have conflicting information: Record A has phone number X and title "VP Sales", Record B has phone number Y and title "Director of Sales". Both could be correct at different points in time, or one could be wrong.

*Challenge:*

Standard survivorship rules (most recent, longest value) may not pick the right answer. A title change from "Director" to "VP" is progression; "VP" to "Director" would be unusual. Phone numbers may both be valid (office vs. mobile).

*Approach:*

1. For title fields: prefer the value from the most recently active record (last activity date, not last modified)
2. For phone fields: if tool supports it, map to separate fields (Phone to Phone, other phone to Mobile) rather than overwriting
3. For address fields: prefer the record with verified/enriched data source
4. When neither value is clearly better: concatenate into a "needs review" note field and flag for manual cleanup

*Key validation:*

Spot-check 20-30 records where field conflicts existed. Verify the surviving value makes business sense. If more than 10% of spot-checked records have wrong surviving values, revisit survivorship rules.

---

## References

[1] [Landbase - Duplicate Record Rate Statistics: 32 Key Facts](https://www.landbase.com/blog/duplicate-record-rate-statistics)
[2] [Gartner - Data Quality Market Survey (via Plauti)](https://www.plauti.com/blog/hidden-costs-poor-data-quality-crm-fixes)
[3] [Salesforce - Things to Know About Duplicate Rules](https://help.salesforce.com/s/articleView?id=sales.duplicate_rules_overview.htm&language=en_US&type=5)
[4] [Insycle - CRM Deduplication: Why Picking the Right Master Record is Critical](https://blog.insycle.com/picking-master-record-crm-deduplication)
[5] [Landbase - 92% of Duplicates Created During Registration](https://www.landbase.com/blog/duplicate-record-rate-statistics)
[6] [Hubsessed - The HubSpot Deduplication Tool Comparison Guide](https://www.hubsessed.io/p/the-hubspot-deduplication-tool-comparison-guide)
[7] [Insycle - HubSpot Deduplication &amp; Integration Tools](https://www.insycle.com/hubspot/deduplication/)
[8] [Data Ladder - Fuzzy Matching 101: The Complete Guide](https://dataladder.com/fuzzy-matching-101/)
[9] [FindStack - CRM Statistics](https://findstack.com/resources/crm-statistics)
[10] [Validity - How Poor Data Quality is Sabotaging Your Business](https://www.validity.com/blog/poor-data-quality-is-sabotaging-businesses-in-2022/)
[11] [Grazitti Interactive - Bad Data Can Cost Over 12% of Revenue](https://www.grazitti.com/blog/bad-data-can-cost-you-over-12-of-your-revenue/)
