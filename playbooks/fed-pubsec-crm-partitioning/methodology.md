# Fed/PubSec CRM Partitioning — Methodology

This document covers the core concepts, frameworks, and calculations behind Fed/PubSec CRM Partitioning. It provides the methodological foundation — the 'how it works' behind the execution steps.

---

## 1) Core Concepts

### Concept 1: Compliance-Driven Data Partitioning

*What is it?*

Compliance-driven data partitioning is the practice of creating logical or physical boundaries within a CRM to isolate data that falls under government regulatory frameworks (ITAR, FedRAMP, DFARS, CMMC) from standard commercial data. Unlike performance-based partitioning (sharding for speed), this partitioning exists to prevent unauthorized access to controlled information and to maintain an auditable chain of custody.

*Why does it matter?*

ITAR violations carry civil fines of up to $500,000 per violation and criminal penalties of up to $1 million per violation with potential imprisonment of up to 10 years per offense [1]. In October 2024, Raytheon agreed to pay over $950 million to resolve investigations including ITAR violations [2]. For B2B SaaS companies selling into both commercial and government markets, a single misconfigured sharing rule can expose controlled data and trigger regulatory action.

*Key insight:*

> Partitioning is not a CRM architecture preference -- it is a legal requirement. The question is never "should we partition?" but "which partitioning approach satisfies the applicable compliance framework while maintaining operational efficiency?"

*Examples:*

| Context | Example |
|---------|---------|
| Defense contractor with commercial SaaS product | ITAR-controlled technical specifications in Opportunity records must be invisible to commercial sales reps, including non-US persons on the commercial team |
| State/local government sales team | Agency contact information and contract terms need isolation from commercial pipeline but don't require ITAR-level controls -- FedRAMP Moderate or CMMC Level 1 may suffice |
| Dual-use technology company | Some products sell to both DoD and commercial buyers. Account records may need splitting when a single customer has both government and commercial contracts |

### Concept 2: The Regulatory Framework Stack

*What is it?*

Federal/PubSec CRM partitioning is governed by a stack of overlapping regulatory frameworks. Each framework has different data handling requirements, and the most restrictive framework that applies dictates the partitioning approach.

*Why does it matter?*

Misidentifying which framework applies leads to either under-protection (compliance violation) or over-protection (unnecessary cost and operational friction). The CMMC program alone impacts more than 337,000 contractors and subcontractors, including nearly 230,000 small entities [3].

*The Framework:*

| Framework | Governs | Data Types | Key Requirement |
|-----------|---------|------------|-----------------|
| **ITAR** | Export of defense articles and technical data | Technical specs, defense-related contact info, contract details on USML items | Access restricted to US persons only; data must reside in US-controlled systems [1] |
| **FedRAMP** | Cloud services used by federal agencies | All data processed/stored by the cloud service | Cloud provider must meet security baseline (Low, Moderate, High) [4] |
| **DFARS 252.204-7012** | Safeguarding covered defense information | Controlled Unclassified Information (CUI) on contractor systems | Report cyber incidents within 72 hours; meet NIST SP 800-171 controls [3] |
| **CMMC 2.0** | Cybersecurity maturity for DoD contractors | FCI (Level 1) and CUI (Levels 2-3) | Tiered certification required before contract award; phased rollout 2025-2028 [3] |
| **EAR** | Export of dual-use commercial items | Technical data for items on Commerce Control List | Less restrictive than ITAR but still requires access controls for certain countries |

*Common misunderstandings:*

- **Misconception:** "FedRAMP certification means our CRM is compliant for all government data."
  **Reality:** FedRAMP covers the cloud infrastructure, not the data access controls within the application. A FedRAMP-authorized Salesforce org still needs properly configured sharing rules, profiles, and permission sets to isolate Fed/PubSec data.

- **Misconception:** "ITAR only applies to weapons manufacturers."
  **Reality:** ITAR covers any item on the US Munitions List, including software, technical data, and services related to defense articles. A SaaS company providing analytics to a defense contractor may need ITAR controls if CRM records contain technical data about USML items.

### Concept 3: Data Classification Levels for CRM Records

*What is it?*

A structured system for labeling CRM records and fields by sensitivity level, which then maps to specific access control requirements. Most organizations use a four-tier model adapted for their regulatory context [5].

*Why does it matter?*

Without clear classification, teams either over-restrict (blocking legitimate collaboration) or under-restrict (creating compliance gaps). Classification is the foundation that sharing rules, permission sets, and audit requirements build on.

*The Framework:*

```
Level 4: RESTRICTED    --> ITAR-controlled data, classified references
                         Access: Named US persons only, audit every access
                         CRM fields: Technical specs, USML references, defense contract values

Level 3: CONFIDENTIAL  --> CUI, sensitive government agency data
                         Access: Fed/PubSec team with need-to-know, US persons
                         CRM fields: Agency contacts, proposal details, pricing

Level 2: INTERNAL      --> General Fed/PubSec business data
                         Access: Fed/PubSec team members
                         CRM fields: Account names, activity logs, pipeline stage

Level 1: PUBLIC        --> Non-sensitive, shareable across segments
                         Access: All CRM users
                         CRM fields: Industry, company size, public website
```

*Common misunderstandings:*

- **Misconception:** "We just need to tag accounts as Fed or Commercial and we're done."
  **Reality:** Classification needs to happen at the field level, not just the record level. An Account record for a government agency may have a public-facing address (Level 1) alongside ITAR-controlled contract values (Level 4). Field-level security must enforce different visibility within the same record.

- **Misconception:** "Our data classification is a one-time setup."
  **Reality:** Accounts change status (commercial company wins a government subcontract), new compliance requirements emerge (CMMC phased rollout through 2028), and data sensitivity evolves. Classification rules need ongoing governance and re-evaluation.

### Concept 4: The Three Partitioning Models

*What is it?*

There are three architectural approaches to isolating Fed/PubSec data within CRM systems, each with different levels of isolation, cost, and operational complexity. See Decision Frameworks for when to use each.

*Why does it matter?*

Choosing the wrong model creates either compliance gaps (too little isolation) or operational paralysis (too much isolation). The model choice is the single most consequential architecture decision in this project.

*The Framework:*

| Model | Isolation Level | Cost | Operational Impact |
|-------|----------------|------|-------------------|
| **Model A: Single Org + RBAC** | Logical (sharing rules, profiles, permission sets) | Low | Low -- single admin team, unified reporting possible |
| **Model B: Separate Business Units** | Logical with stronger boundaries (territory management, separate role hierarchies) | Medium | Medium -- shared infrastructure but distinct operational domains |
| **Model C: Separate CRM Instance** | Physical (entirely separate org/tenant) | High | High -- duplicate admin, separate integrations, no cross-segment reporting without ETL |

*Common misunderstandings:*

- **Misconception:** "Separate instances are always safer."
  **Reality:** A poorly administered separate instance can have weaker controls than a well-configured single org with strict RBAC. Security depends on configuration quality, not architecture alone.

- **Misconception:** "Single org RBAC is never sufficient for ITAR."
  **Reality:** For CRM data that references but does not contain ITAR-controlled technical data (e.g., pipeline tracking for defense accounts without technical specs in CRM fields), single org RBAC with field-level security can be sufficient. The question is what data actually lives in the CRM versus external controlled systems.

---

## 2) Decision Frameworks

### Approach Selection Matrix

| Situation | Recommended Approach | Why |
|-----------|---------------------|-----|
| CRM stores ITAR-controlled technical data (USML items, defense specs) | **Model C: Separate Instance** (Salesforce Government Cloud or equivalent) | ITAR requires US-person-only access and US-sovereign infrastructure; logical partitioning may not satisfy audit requirements |
| CRM handles CUI under DFARS/CMMC but no ITAR data | **Model B: Separate Business Units** or **Model A: Single Org + RBAC** with strict field-level security | CUI requires documented access controls and audit trails but does not mandate physical separation |
| Fed/PubSec team sells non-defense government solutions (state/local, civilian agencies) | **Model A: Single Org + RBAC** with criteria-based sharing rules | Lower regulatory bar; sharing rules and profiles provide sufficient isolation |
| Company has &lt;50 CRM users and a small Fed/PubSec team (3-5 reps) | **Model A: Single Org + RBAC** | Operational overhead of separate instances is disproportionate to team size |
| Company has >200 CRM users with dedicated Fed/PubSec operations, separate leadership, and compliance staff | **Model B or C** depending on data types | Scale justifies the operational overhead; dedicated teams can manage distinct configurations |
| Existing GovCloud or government-specific CRM environment already in place | **Extend existing Model C** | Migrating back to a shared model introduces risk and rework |

### Scoping Factors

These are the variables that determine which partitioning approach to use. Assess each factor during discovery.

**1. Regulatory Framework Applicability**

- ITAR applies (USML technical data in CRM) --> Model C strongly recommended
- CMMC Level 2+ applies (CUI in CRM) --> Model B minimum, Model C if technical data present
- CMMC Level 1 only (FCI in CRM) --> Model A sufficient with proper RBAC
- No specific defense framework (state/local government sales) --> Model A sufficient

**2. Data Sensitivity in CRM**

- CRM contains actual technical data or defense specs --> Model C
- CRM contains CUI metadata (contract values, agency contacts, proposal details) --> Model B or strict Model A
- CRM contains only pipeline/relationship data (no controlled info) --> Model A
- Mixed: some records contain controlled data, others don't --> Field-level security within Model A or B; consider splitting high-sensitivity records to separate system

**3. Team Size and Structure**

- Fewer than 10 Fed/PubSec users --> Model A (overhead of B/C is excessive)
- 10-50 Fed/PubSec users with dedicated manager --> Model A or B
- 50+ Fed/PubSec users with separate leadership and operations --> Model B or C
- Fed/PubSec team is in a different legal entity or subsidiary --> Model C (simplifies compliance boundary)

**4. Integration Landscape**

- Few integrations (CRM + email only) --> Any model works
- Marketing automation shared across segments --> Model A is simpler; Model B/C requires duplicate or filtered integration configurations
- BI/analytics tools pull from CRM --> Model A/B allow unified analytics with row-level security; Model C requires ETL or data warehouse for cross-segment reporting
- API integrations with government systems (SAM.gov, FPDS, etc.) --> Dedicated integration user per segment regardless of model

**5. Audit and Reporting Requirements**

- Quarterly compliance audits required --> Any model, but document access controls thoroughly
- Real-time audit trail required for all data access --> Model B or C (logging is easier with clear boundaries)
- External auditors need to verify isolation --> Model C provides the simplest audit story; Model A/B require detailed sharing rule documentation

### Model A: Single Org + RBAC

*Best for:*
- State/local government or civilian agency sales (no ITAR/CMMC Level 2+)
- Small Fed/PubSec teams within a larger commercial org
- Companies where Fed/PubSec data in CRM is pipeline/relationship data, not controlled information
- Organizations that need unified reporting across segments

*Not recommended for:*
- ITAR-controlled data stored in CRM fields
- CUI that requires physical isolation per contract requirements
- Organizations where external auditors expect physical separation
- Teams with non-US persons who have admin or elevated CRM access

*Key differences from standard:*

| Aspect | Standard CRM Setup | Model A Partitioned |
|--------|-------------------|-------------------|
| OWD Settings | Often Public Read or Public Read/Write | Private for all objects containing Fed/PubSec data |
| Sharing Rules | Role-hierarchy based | Criteria-based sharing rules tied to segment field + role hierarchy |
| Profiles | Generic sales profiles | Separate Fed/PubSec and Commercial profiles with distinct FLS |
| Record Types | None or product-based | Segment-based record types (Fed/PubSec, Commercial) |
| Reporting | Open access | Report folder security + dashboard running user controls |

### Model B: Separate Business Units

*Best for:*
- Mid-size orgs handling CUI under CMMC Level 2
- Companies with dedicated Fed/PubSec operations leadership
- Situations where Model A sharing rules become too complex (>50 criteria-based rules)
- Organizations using Salesforce Enterprise/Unlimited with territory management

*Not recommended for:*
- ITAR-controlled technical data (still need Model C)
- Very small teams where business unit overhead adds unnecessary complexity
- Organizations on CRM platforms that don't support business unit or territory isolation

*Key differences from standard:*

| Aspect | Model A | Model B |
|--------|---------|---------|
| Hierarchy | Single role hierarchy with segment branches | Separate role hierarchies per business unit |
| Data Ownership | Shared object space with sharing rules | Territory-based ownership with automatic assignment |
| Admin Complexity | Moderate (sharing rules can get complex) | Higher (separate hierarchies, territory rules) |
| Cross-segment visibility | Controlled by sharing rules (can be overridden) | Controlled by territory membership (stronger boundary) |

### Model C: Separate CRM Instance

*Best for:*
- ITAR-controlled data that must reside in US-sovereign infrastructure
- DoD contracts that contractually require physical data isolation
- Companies with a large Fed/PubSec division that operates independently
- Acquisitions where the Fed/PubSec business was a separate entity

*Not recommended for:*
- Small Fed/PubSec teams (cost and admin overhead is disproportionate)
- Organizations that need real-time cross-segment pipeline visibility
- Companies without dedicated CRM admin capacity for a second instance

*Key differences from standard:*

| Aspect | Model A/B (Single Org) | Model C (Separate Instance) |
|--------|----------------------|---------------------------|
| Infrastructure | Shared multi-tenant (standard or GovCloud) | Dedicated GovCloud or separate tenant |
| Admin Team | Single team manages both segments | Dedicated admin for each instance |
| Integrations | Single set of integrations with filters | Duplicate integration configurations per instance |
| Reporting | Unified with sharing rule filters | Requires ETL/data warehouse for cross-segment views |
| Cost | Standard licensing | Additional licenses + GovCloud premium (typically 20-40% markup) |
| Audit Story | "We configured access controls within our CRM" | "The data is in a physically separate system" |

---

## 3) Benchmarks & Standards

### How to Use Benchmarks

*Benchmarks are guidelines, not rules. Always:*
1. Start with the regulatory requirement as the baseline (compliance is binary -- you either meet it or you don't)
2. Use industry benchmarks for operational planning (timelines, complexity, audit cadence)
3. Adjust based on client-specific factors (team size, data volume, existing infrastructure)
4. Document deviations and rationale for audit purposes

### Compliance Framework Thresholds

| Framework | Certification Level | CRM Implication | Audit Frequency |
|-----------|-------------------|-----------------|-----------------|
| ITAR | N/A (self-certification + State Dept registration) | Physical isolation of controlled data from non-US persons | Ongoing; annual State Dept registration renewal |
| FedRAMP | Low / Moderate / High | Cloud provider must hold authorization at required level | Annual assessment + continuous monitoring |
| CMMC 2.0 | Level 1 (FCI) | Self-assessment; 17 practices | Annual self-assessment, posted to SPRS |
| CMMC 2.0 | Level 2 (CUI) | Third-party assessment; 110 practices (NIST 800-171) | Triennial third-party assessment |
| CMMC 2.0 | Level 3 (highest CUI sensitivity) | Government-led assessment; 110+ practices | Triennial government assessment |
| DFARS 252.204-7012 | N/A (contract clause) | CUI protection + 72-hour incident reporting | Per contract; typically quarterly review |

**Source:** DoD CMMC Final Rule (December 2024) [3], FedRAMP Baselines [4]

**Interpretation:**
- **Below minimum:** Contract ineligibility. As of November 2025, defense contractors cannot receive awards without current CMMC status in SPRS at the required level [3].
- **At minimum:** Compliant but vulnerable to audit findings on implementation quality. Configuration must be documented and defensible.

### Data Access Control Benchmarks

| Metric | Minimum Standard | Recommended | Notes |
|--------|-----------------|-------------|-------|
| OWD Setting for Fed/PubSec objects | Private | Private | No exceptions for objects containing controlled data |
| Sharing rule recalculation time | Under 4 hours | Under 1 hour | Salesforce limits: 300 total sharing rules per object, 50 criteria-based [6] |
| Permission set review cadence | Quarterly | Monthly | 83% of organizations reported insider attacks in 2024 [7]; regular review reduces privilege creep |
| User access audit cadence | Annually | Quarterly | Aligns with DFARS quarterly review expectations |
| Inactive user deactivation SLA | 30 days | 14 days | ITAR requires prompt removal of access for departing employees [1] |
| Integration user audit cadence | Semi-annually | Quarterly | API users often have elevated permissions that bypass sharing rules |

**Source:** Salesforce Security Implementation Guide [6], IBM 2024 Insider Threat Report [7]

### Project Timeline Benchmarks

| Project Scope | Model A | Model B | Model C |
|--------------|---------|---------|---------|
| Discovery & requirements | 1-2 weeks | 1-2 weeks | 2-3 weeks |
| Architecture design | 1 week | 1-2 weeks | 2-3 weeks |
| Configuration & build | 2-3 weeks | 3-4 weeks | 4-6 weeks |
| Data migration & tagging | 1-2 weeks | 1-2 weeks | 2-4 weeks |
| Testing & validation | 1-2 weeks | 2-3 weeks | 3-4 weeks |
| Training & rollout | 1 week | 1-2 weeks | 2-3 weeks |
| **Total** | **7-11 weeks** | **9-14 weeks** | **15-23 weeks** |

### Quick Reference Thresholds

| Question | Good | Warning | Red Flag |
|----------|------|---------|----------|
| How many users have cross-segment access? | 0 (except designated admins) | 1-3 users with documented business need | 4+ users or any without documented justification |
| How many sharing rules per object? | Under 20 | 20-40 | 40+ (approaching Salesforce limit of 50 criteria-based) |
| Time to detect unauthorized access? | Under 24 hours | 24-72 hours | Over 72 hours (exceeds DFARS incident reporting window) |
| Percentage of records properly tagged? | 100% | 95-99% (with remediation plan) | Below 95% (systemic classification gap) |
| Integration users with cross-segment access? | 0 | 1 with documented need | 2+ (integration architecture needs redesign) |

---

## 4) Calculations & Scoring

> **Note:** This project is primarily qualitative (compliance-driven, process-heavy). The scoring below provides a structured way to assess compliance readiness and data sensitivity, which drives the partitioning approach selection.

### Formula Quick Reference

| Calculation | Formula | Example |
|-------------|---------|---------|
| Compliance Readiness Score | Sum of readiness criteria scores (0-100) | Score of 72 = moderate readiness, gaps to address before build |
| Data Sensitivity Index | `(Restricted records x 4) + (Confidential x 3) + (Internal x 2) + (Public x 1) / Total records` | Index of 2.8 = high average sensitivity, Model B or C likely needed |
| Partitioning Complexity Score | `(Users x 0.3) + (Integrations x 0.4) + (Objects x 0.3)` normalized to 100 | Score of 65 = moderate complexity, expect 10-14 week timeline |

### Compliance Readiness Assessment

**Purpose:** Score the client's current state to estimate effort required and identify gaps before build begins.

| Criterion | Points | What Earns These Points |
|-----------|--------|------------------------|
| OWD set to Private for key objects | 15 pts | All Account, Contact, Opportunity OWDs are Private |
| Role hierarchy exists with segment branches | 10 pts | Distinct Fed/PubSec branch in role hierarchy |
| Sharing rules use criteria-based logic | 10 pts | At least some criteria-based sharing rules in place |
| Permission sets exist for segment access | 10 pts | Named permission sets for Fed/PubSec data access |
| Field-level security configured for sensitive fields | 15 pts | Sensitive fields restricted at profile level |
| User access audit completed in last 90 days | 10 pts | Documented audit with findings addressed |
| Integration users have scoped permissions | 10 pts | Dedicated integration users per segment or filtered access |
| Data classification rules documented | 10 pts | Written criteria for Fed/PubSec vs Commercial classification |
| Compliance framework requirements mapped | 10 pts | Document listing which frameworks apply and their requirements |
| **Total** | **100 pts** | |

**Tier Thresholds:**
- Tier 1 (75+ points): Strong foundation. Partitioning is an enhancement of existing controls. Expect faster timeline.
- Tier 2 (40-74 points): Moderate gaps. Several foundational controls need to be built or strengthened before partitioning.
- Tier 3 (Below 40 points): Significant gaps. Project scope likely needs to include CRM security fundamentals alongside partitioning.

### Data Sensitivity Index

**Formula:**
```
DSI = (R x 4 + C x 3 + I x 2 + P x 1) / (R + C + I + P)
```

**Variables explained:**
- `R` = Count of records classified as Restricted (ITAR-controlled)
- `C` = Count of records classified as Confidential (CUI)
- `I` = Count of records classified as Internal (general Fed/PubSec)
- `P` = Count of records classified as Public (shareable)

**Worked Example:**

*Scenario: Mid-market defense subcontractor with 5,000 CRM accounts*

```
Given:
- Restricted (R) = 200 accounts (direct USML contract accounts)
- Confidential (C) = 800 accounts (CUI-holding government accounts)
- Internal (I) = 1,500 accounts (general Fed/PubSec pipeline)
- Public (P) = 2,500 accounts (commercial accounts)

Calculate:
- Numerator = (200 x 4) + (800 x 3) + (1,500 x 2) + (2,500 x 1) = 800 + 2,400 + 3,000 + 2,500 = 8,700
- Denominator = 200 + 800 + 1,500 + 2,500 = 5,000
- DSI = 8,700 / 5,000 = 1.74
```

**Validation:**
- DSI 1.0-1.5: Low sensitivity average. Model A likely sufficient.
- DSI 1.5-2.5: Moderate sensitivity. Model A with strict FLS or Model B.
- DSI 2.5-3.0: High sensitivity. Model B or C recommended.
- DSI 3.0+: Very high sensitivity. Model C strongly recommended.

---

## 5) Edge Cases & Deep Dives

### Edge Case 1: Hybrid Accounts (Commercial Company with Government Subcontract)

*Scenario:*

A commercial account in the CRM wins a government subcontract. The account now has both commercial opportunities (visible to the full sales team) and a government subcontract opportunity (containing CUI that must be restricted to the Fed/PubSec team).

*Challenge:*

The account itself cannot be cleanly classified as "Fed/PubSec" or "Commercial" because it is both. Record-level partitioning at the Account level would either over-restrict (blocking commercial reps from their own accounts) or under-restrict (exposing government opportunity data).

*Approach:*

1. Keep the Account record as Commercial with a flag field ("Has Government Contract: Yes")
2. Create the government Opportunity with Fed/PubSec record type and criteria-based sharing rules
3. Use field-level security to hide sensitive fields on the government Opportunity from commercial profiles
4. Assign the government Opportunity to a Fed/PubSec rep while the Account owner remains the commercial rep
5. Document the split-ownership arrangement for audit purposes

*Key validation:*

Log in as the commercial Account owner and confirm they cannot see the government Opportunity details. Log in as Fed/PubSec rep and confirm they can see the government Opportunity but not unrelated commercial Opportunities on the same Account.

### Edge Case 2: Integration Users Bypassing Partitioning

*Scenario:*

A marketing automation platform (HubSpot, Marketo) syncs with the CRM using an API integration user. The integration user has elevated permissions to read/write across all records, effectively bypassing the sharing rules that partition Fed/PubSec data from commercial.

*Challenge:*

Integration users typically need broad access to function, but that broad access creates a data leakage vector. A marketing team member could see Fed/PubSec contact data through the marketing platform even if they can't see it in the CRM. CRM application users and internal systems account for more than 75% of data breaches [8].

*Approach:*

1. Create separate integration users for each segment: one for commercial data sync, one for Fed/PubSec data sync
2. Assign each integration user a profile with segment-appropriate permissions
3. Configure the marketing platform to use the correct integration user for each data segment
4. Add criteria-based filters in the sync configuration (sync only records where Business_Segment__c = "Commercial" for the commercial integration user)
5. Audit integration user activity logs monthly to verify no cross-segment data access

*Key validation:*

Attempt to access Fed/PubSec data via the commercial integration user's API credentials. Confirm 403/no-data response. Check marketing platform for any Fed/PubSec contacts in commercial segments.

### Edge Case 3: Multi-Framework Overlap (ITAR + CMMC + FedRAMP)

*Scenario:*

A client sells both ITAR-controlled defense products and non-ITAR government IT services. Their CRM contains data subject to ITAR (defense product pipeline), CMMC Level 2 (IT services CUI), and FedRAMP requirements (they also resell a FedRAMP-authorized SaaS product to agencies). Different frameworks have different requirements, and the client wants a single partitioning strategy.

*Challenge:*

The most restrictive framework (ITAR) sets the floor for the ITAR-controlled data, but applying ITAR-level controls to all Fed/PubSec data creates unnecessary operational friction for the non-ITAR government IT sales team. Teams need different levels of access control within the same "Fed/PubSec" partition.

*Approach:*

1. Create sub-segments within Fed/PubSec: "Fed-Defense" (ITAR) and "Fed-IT" (CMMC/FedRAMP)
2. Fed-Defense data goes to a separate CRM instance (Model C) on GovCloud or equivalent
3. Fed-IT data stays in the main CRM with Model A or B partitioning from commercial data
4. Create clear classification criteria: if any record touches USML items, it goes to Fed-Defense; all other government records go to Fed-IT
5. Document the framework-to-segment mapping for compliance auditors

*Key validation:*

Map every active government opportunity to a framework and segment. Confirm zero unclassified government records. Verify that Fed-Defense users cannot see Fed-IT data and vice versa (separate isolation, not shared).

### Edge Case 4: New Hire Onboarding with Incorrect Segment Access

*Scenario:*

A new sales rep is hired for the commercial team but is accidentally assigned a Fed/PubSec profile during CRM onboarding. They access Fed/PubSec records for 3 days before the error is caught.

*Challenge:*

This is both an operational issue (process gap in onboarding) and a compliance event (unauthorized access to controlled information that may need to be documented or reported depending on the framework).

*Approach:*

1. Immediately reassign the user to the correct commercial profile
2. Pull audit logs for the user's 3-day access period: which records were viewed, downloaded, or exported
3. Assess whether any accessed records contained CUI or ITAR-controlled data
4. If CUI was accessed: document the incident per DFARS 252.204-7012 requirements (may trigger 72-hour reporting if data was compromised)
5. If ITAR data was accessed: verify the user is a US person. If not, this is a potential ITAR violation requiring legal review.
6. Implement onboarding checklist with profile/segment verification step and manager sign-off

*Key validation:*

After remediation, log in as the corrected user and confirm zero visibility to Fed/PubSec records. Review onboarding process to confirm checklist and approval gate are in place. Run a monthly report of new user profile assignments for ongoing verification.

### Edge Case 5: Data Migration with Untagged Historical Records

*Scenario:*

The client has 50,000 historical Account records. Only 20% are clearly identifiable as Fed/PubSec or Commercial. The remaining 80% have no segment tag, inconsistent naming, or ambiguous industry classifications.

*Challenge:*

Partitioning cannot be "turned on" until all records are classified. Untagged records in a Private OWD environment become invisible to everyone (orphaned data), or if left in a permissive state, they create compliance gaps.

*Approach:*

1. Run automated classification first: match against known government domains (.gov, .mil), NAICS codes for government, DUNS numbers in SAM.gov
2. Use enrichment tools (ZoomInfo, Apollo) to fill gaps in industry/sector data
3. Create a "Pending Classification" segment with restricted access (visible only to the data migration team)
4. Set a hard deadline for manual review of remaining unclassified records
5. Do NOT go live with partitioning until 100% of active records are classified. Archived/inactive records can be classified post-launch with restricted access in the interim.

*Key validation:*

Run a report of all records with null or "Pending Classification" segment value. This number must be zero for active records before go-live. Confirm archived records are in a restricted-access holding area.

---

## References

[1] [Fortra - What is ITAR Compliance?](https://www.fortra.com/blog/what-itar-compliance)
[2] [PreVeil - ITAR Compliance Guide](https://www.preveil.com/blog/itar-compliance/)
[3] [DoD CMMC Final Rule - SBA Office of Advocacy](https://advocacy.sba.gov/2024/10/24/dod-final-cmmc-rule/)
[4] [FedRAMP - Understanding Baselines and Impact Levels](https://www.fedramp.gov/understanding-baselines-and-impact-levels/)
[5] [Secureframe - Data Classification Guide](https://secureframe.com/blog/data-classification)
[6] [Salesforce Security Implementation Guide - Data Access Controls](https://developer.salesforce.com/docs/atlas.en-us.securityImplGuide.meta/securityImplGuide/security_data_access.htm)
[7] [IBM - 83% of Organizations Reported Insider Attacks in 2024](https://www.ibm.com/think/insights/83-percent-organizations-reported-insider-threats-2024)
[8] [Schellman - Data Breach in Your CRM System](https://www.schellman.com/blog/data-breach-in-crm)
