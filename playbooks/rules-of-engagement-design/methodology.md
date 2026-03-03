# Rules of Engagement Design — Methodology

This document covers the core concepts, frameworks, and benchmarks behind Rules of Engagement Design. It provides the methodological foundation — the 'how it works' behind the execution steps.

---

## 1) Core Concepts

### Account Ownership vs. Opportunity Ownership

*What is it?*

Account ownership defines which rep or team is assigned to a company (the account record in CRM), while opportunity ownership defines who manages a specific deal within that account. These are distinct assignments that can -- and often do -- belong to different people. For example, an Account Executive may own the account, but a Solutions Engineer or partner rep may co-own a specific opportunity.

*Why does it matter?*

Conflating the two is the single most common source of ROE confusion. When organizations treat account ownership as automatic opportunity ownership, they create friction between AEs working new logos, CSMs handling renewals, and AMs pursuing expansion. Separating these concepts allows each role to operate within clearly defined boundaries.

*Key insight:*

> Account ownership answers "who is responsible for the relationship?" Opportunity ownership answers "who is responsible for the deal?" Keeping these distinct eliminates 60-70% of common ownership disputes [1].

*Examples:*

| Context | Example |
|---------|---------|
| Enterprise AE owns the account | AE owns net-new opportunity, but CSM owns the renewal opportunity on the same account |
| Named Account list | AE owns the account and all outbound opportunities, but an inbound SDR-sourced demo creates an opportunity routed to the AE per lead-to-account matching |
| Partner-sourced deal | Channel Manager sources the opportunity; AE owns the account but partner rep co-owns the opp with a defined split |

### The ROE Scenario Matrix

*What is it?*

A structured classification of every possible ownership situation a sales organization can encounter. The matrix organizes scenarios along two axes: (1) lead source (inbound, outbound, partner, existing customer) and (2) deal type (net-new, expansion, renewal, cross-sell).

*Why does it matter?*

Without a scenario matrix, rules get written reactively -- one dispute at a time. Teams end up with 50 Slack threads that each set a different informal precedent. The matrix forces upfront coverage of all combinations so rules exist before conflicts arise.

*The Framework:*

```
               | Net-New Logo  | Expansion/Upsell | Renewal       | Cross-Sell     |
---------------|---------------|------------------|---------------|----------------|
Inbound        | Rule A        | Rule B           | Rule C        | Rule D         |
Outbound       | Rule E        | Rule F           | Rule G        | Rule H         |
Partner        | Rule I        | Rule J           | Rule K        | Rule L         |
Existing Cust. | Rule M        | Rule N           | Rule O        | Rule P         |
```

Each cell in this matrix requires a specific, documented rule. Cells without rules become dispute hotspots.

*Common misunderstandings:*

- **Misconception:** "We only need rules for inbound vs. outbound."
  **Reality:** Partner deals and existing customer scenarios generate disproportionate conflict. Gradient Works found that attribution conflicts between outbound and inbound on the same account are among the most common ROE disputes [2].

- **Misconception:** "Our team is small; we don't need a matrix."
  **Reality:** Small teams with 5-10 reps are where ROE matters most. Without formal rules, relationships and personal persuasion drive dispute outcomes, creating resentment that accelerates turnover.

### If/Then Rule Design

*What is it?*

A rule-writing pattern that eliminates interpretation ambiguity by structuring every ROE rule as: "IF [specific condition], THEN [specific owner] owns for [specific duration]." Each rule includes concrete examples to prevent gray-area readings.

*Why does it matter?*

Vague rules ("the rep who has the strongest relationship should own the deal") invite dispute. If/then rules are enforceable, testable against historical scenarios, and automatable in CRM. Research from the Sales Enablement Collective shows that organizations with specific, conditional ROE language resolve disputes 3x faster than those with principle-based guidelines [3].

*Key insight:*

> A rule you cannot explain to a CRM automation is a rule that will be disputed. If it cannot be coded, it is not specific enough.

*Examples:*

| Context | Example |
|---------|---------|
| Inbound lead on named account | IF inbound lead matches a named account, THEN the named account owner gets the lead within 4 hours; IF the named account owner does not accept within 4 hours, THEN the lead re-enters round-robin |
| Outbound prospecting protection | IF Rep A has an open opportunity on Account X created within the last 90 days, THEN no other rep may create a new opportunity on Account X; IF 90 days pass with no stage progression, THEN account returns to open pool |
| Partner deal registration | IF partner submits deal registration and no existing open opportunity exists, THEN partner rep and assigned AE co-own for 60 days; IF deal registration overlaps with existing AE-sourced opp, THEN the first-created opportunity takes precedence |

### Dispute Resolution Tiering

*What is it?*

A structured escalation path for ownership conflicts, organized into tiers with defined SLAs and decision-makers at each level. Typically three tiers: (1) rep-to-rep resolution, (2) manager arbitration, (3) VP/RevOps final decision.

*Why does it matter?*

Without tiered resolution, every conflict escalates directly to leadership, consuming VP Sales time on disputes that reps could resolve themselves. Alternatively, disputes fester in Slack channels for days without resolution, stalling deal progress. Sales managers report spending up to 10-15% of their time arbitrating ownership conflicts when no formal escalation path exists [4].

*The Framework:*

```
Tier 1: Rep-to-Rep (24-hour window)
  --> Reps discuss and attempt resolution using ROE document
  --> If resolved: document the precedent

Tier 2: Manager Arbitration (24-hour window)
  --> Sales Manager reviews rule, decides
  --> Decision is binding and documented

Tier 3: VP/RevOps Final Decision (48-hour window)
  --> Only for cases not covered by existing rules
  --> Decision becomes a new rule added to ROE
```

*Common misunderstandings:*

- **Misconception:** "The VP Sales should decide every dispute to show fairness."
  **Reality:** VP involvement in routine disputes signals that the ROE is too vague. The VP should only see Tier 3 cases -- novel scenarios that need new rules written.

- **Misconception:** "Dispute resolution should be consensus-based."
  **Reality:** Consensus stalls deals. One person at each tier must have final authority. The key is that the decision-maker is published and agreed upon in advance.

---

## 2) Decision Frameworks

### Approach Selection Matrix

| Situation | Recommended Approach | Why |
|-----------|---------------------|-----|
| Single-segment sales team (all AEs sell to same market) | Territory-based ownership with round-robin inbound | Simple, enforceable, minimizes overlap |
| Multi-segment sales team (SMB, MM, Enterprise) | Segment-based ownership with handoff rules at segment boundaries | Prevents cross-segment poaching; requires clear firmographic criteria |
| Named account model (Enterprise AEs with assigned accounts) | Named account ownership with inbound matching and protection windows | Protects AE investment in strategic accounts while allowing inbound routing |
| PLG + sales-assisted hybrid | Product-qualified lead (PQL) routing with usage-based assignment | Maps ownership to product engagement rather than territory |
| Heavy channel/partner ecosystem | Dual-ownership model with deal registration windows and split rules | Prevents channel conflict while protecting direct sales investment |

### Scoping Factors

These variables determine which ROE approach fits a given client. Evaluate each before designing rules.

**1. Sales Team Structure**

- Single team, single segment --> Simpler ROE. Territory or round-robin ownership is sufficient.
- Multiple teams, multiple segments --> Complex ROE. Need segment handoff rules, shared account governance, and clear escalation between teams.
- Overlay model (SDR + AE + CSM + AM) --> Most complex ROE. Must define ownership at each lifecycle stage and transition triggers between roles.

**2. Deal Source Mix**

- Primarily inbound --> Emphasize lead-to-account matching and response SLAs. Key question: does inbound lead go to territory owner or round-robin?
- Primarily outbound --> Emphasize named account protection and prospecting boundaries. Key question: how long does a rep "own" an account they are actively prospecting?
- Balanced inbound/outbound --> Most contentious scenario. Must explicitly define what happens when an inbound lead arrives on an account already being prospected outbound.
- Significant partner-sourced --> Need deal registration windows, co-selling rules, and sourced-vs-influenced credit definitions.

**3. Account Complexity**

- Simple (one entity per customer) --> Account ownership = straightforward one-to-one mapping.
- Parent-child hierarchies --> Must decide: does parent owner own all children, or are subsidiaries independently assigned? This single decision generates more disputes than any other if left undefined.
- Global accounts with regional presence --> Need geographic overlay rules, global account manager coordination, and local vs. global opportunity ownership.

**4. CRM Maturity**

- Clean CRM with accurate data --> ROE can be automated with validation rules, ownership timeouts, and lead-to-account matching (via LeanData or native tools).
- Dirty CRM with duplicates and missing data --> Must fix data quality first. Attempting CRM enforcement of ROE on bad data creates false violations and erodes trust in the system. Account conflicts can be reduced by up to 80% with automated account hierarchies, but only when the underlying data is clean [5].

**5. Current Dispute Volume**

- Fewer than 5 disputes/month --> Lightweight ROE with core rules and a dispute process may be sufficient.
- 5-15 disputes/month --> Full ROE design with scenario matrix, CRM enforcement, and monitoring dashboard.
- More than 15 disputes/month --> Indicates structural issues (overlapping territories, misaligned segments, bad data). Fix root causes before writing rules.

### Territory-Based Ownership

*Best for:*
- Single-segment sales teams with geographic or industry-based territories
- Organizations with well-defined firmographic data in CRM
- Teams where territories are rebalanced annually or semi-annually

*Not recommended for:*
- PLG motions where product usage drives assignment
- Heavy channel/partner ecosystems where deals cross territory boundaries
- Organizations with frequent segment changes (rapid growth shifting accounts from SMB to MM)

*Key differences from standard:*

| Aspect | Named Account Model | Territory-Based |
|--------|-------------------|-----------------|
| Assignment basis | Explicit list of accounts per rep | Firmographic criteria (geography, industry, employee count) |
| Inbound routing | Match to named account owner | Match to territory based on lead attributes |
| Protection window | Indefinite (while on named list) | Duration-based (30/60/90 days of inactivity) |
| Rebalancing | Account-by-account review | Criteria-based redistribution |

### Named Account Ownership

*Best for:*
- Enterprise sales motions with high ACV and long sales cycles
- Strategic accounts requiring deep relationship investment
- Organizations with 50-500 target accounts per AE

*Not recommended for:*
- High-velocity SMB sales with hundreds of accounts per rep
- Self-serve or PLG motions where account volume makes named lists impractical
- Rapidly growing organizations where account universe changes faster than lists can be updated

*Key differences from standard:*

| Aspect | Territory-Based | Named Account |
|--------|----------------|---------------|
| Ownership clarity | Derived from data (can be ambiguous if data is wrong) | Explicit assignment (no ambiguity if list is current) |
| Flexibility | Easy to add new accounts that match criteria | Requires manual list updates for new accounts |
| Scalability | Scales with data quality | Scales with list management discipline |
| Typical dispute | "This account should be in MY territory" | "This account should be on MY named list" |

### Segment-Based Handoff Model

*Best for:*
- Organizations with distinct SMB, Mid-Market, and Enterprise sales teams
- Companies with clear firmographic thresholds (revenue, employee count) defining segments
- Rapidly growing customer bases where accounts frequently cross segment boundaries

*Not recommended for:*
- Single-segment organizations
- Organizations without reliable firmographic data in CRM
- Companies where segment boundaries are politically defined rather than data-driven

*Key differences from standard:*

| Aspect | Single-Segment ROE | Segment-Based Handoff |
|--------|-------------------|-----------------------|
| Transition rules | None needed | Must define triggers (revenue threshold, employee count) and transition process |
| Compensation on transition | N/A | Must define if outgoing rep gets residual credit on post-transition deals |
| Timeline | N/A | Must define transition window (immediate vs. end-of-quarter vs. deal completion) |
| Dispute type | "Who owns this account?" | "When does this account move segments, and who owns the in-flight deals?" |

---

## 3) Benchmarks & Standards

### How to Use Benchmarks

Benchmarks are guidelines, not rules. Always:
1. Start with the benchmark as a baseline
2. Adjust based on the client's deal cycle length, team size, and segment
3. Validate against their actual dispute data when available
4. Document deviations and rationale

### Ownership Duration Windows

| Scenario | Low | Typical | High | Notes |
|----------|-----|---------|------|-------|
| Outbound prospecting protection | 30 days | 60 days | 90 days | Shorter for SMB (faster cycles); longer for Enterprise |
| Inbound lead acceptance SLA | 1 hour | 4 hours | 24 hours | After SLA expires, lead re-enters rotation |
| Opportunity inactivity timeout | 14 days | 30 days | 60 days | No stage change = ownership at risk; Enterprise gets longer windows |
| Partner deal registration window | 30 days | 60 days | 90 days | After window expires, deal reverts to standard assignment |
| Post-close account protection | 30 days | 90 days | 180 days | Prevents immediate poaching of newly closed accounts by other reps |

**Source:** Aggregated from Gradient Works ROE Toolkit [2], practitioner community guidance (RevOps Co-Op, Pavilion).

**Interpretation:**
- **Below low:** Reps feel unprotected; discourages prospecting investment. Short windows signal to reps that their effort is not valued, reducing outbound activity.
- **Above high:** Creates hoarding behavior where reps sit on stale accounts/opps. Excessively long windows reduce pipeline velocity and prevent fresh reps from working dormant accounts.

### Dispute Resolution SLAs

| Metric | Low | Typical | High | Notes |
|--------|-----|---------|------|-------|
| Tier 1 (rep-to-rep) resolution SLA | 12 hours | 24 hours | 48 hours | Faster for high-velocity SMB deals |
| Tier 2 (manager) resolution SLA | 24 hours | 48 hours | 72 hours | Manager should have full context from Tier 1 |
| Tier 3 (VP/RevOps) resolution SLA | 48 hours | 72 hours | 1 week | Reserved for novel cases requiring new rules |
| Target dispute reduction post-ROE | 30% | 50% | 70% | Within 30 days of rollout |
| Monthly disputes per 100 reps (baseline) | 5 | 10-15 | 25+ | Above 25 signals structural issues beyond ROE |

**Source:** Gradient Works ROE research [2], Sales Enablement Collective [3].

### Sales Productivity Impact

Rules of engagement affect selling time directly. When reps lack clear ownership rules, they spend time on disputes, duplicate outreach, and deal investigation instead of selling.

| Metric | Data Point | Source |
|--------|-----------|--------|
| Rep time spent on actual selling activities | 28-34% of total work time | Salesforce State of Sales [6], Forrester [7] |
| Administrative time consumed (including disputes) | 50% of rep time | Gartner [8] |
| Sales cycle increase (average, 2023-2024) | 107 days to 134 days (+25%) | B2B SaaS industry benchmarks [9] |
| Dirty CRM record cost | ~$100 per dirty record | SiriusDecisions [5] |
| Account conflict reduction with automated hierarchies | Up to 80% | Traction Complete [5] |

Clear ROE directly reduces the administrative overhead that contributes to reps spending only a third of their time selling.

### Quick Reference Thresholds

| Question | Good | Warning | Red Flag |
|----------|------|---------|----------|
| Monthly ownership disputes per 100 reps | Under 5 | 5-15 | Above 15 |
| Time to resolve average dispute | Under 24 hours | 24-72 hours | Over 72 hours |
| % of deals with ownership ambiguity | Under 5% | 5-15% | Above 15% |
| Rep awareness of ROE rules (survey) | Above 80% | 50-80% | Below 50% |
| ROE document freshness | Updated within last quarter | Updated within last 2 quarters | Not updated in 6+ months |

---

## 4) Edge Cases & Deep Dives

### Edge Case 1: Parent-Child Account Hierarchies

*Scenario:*

A large enterprise customer (parent account) has multiple subsidiaries (child accounts). The parent is owned by an Enterprise AE, but one subsidiary independently evaluates and purchases your product through an inbound demo request.

*Challenge:*

Who owns the subsidiary opportunity? The Enterprise AE invested in the parent relationship, but the subsidiary acted independently. If the subsidiary is in a different geographic region, a different AE's territory may also claim it.

*Approach:*

1. Default rule: Parent account owner owns all child accounts unless the child account exceeds a firmographic threshold (e.g., over 500 employees or over $50M revenue) that qualifies it as independently assigned.
2. If the child account generates an inbound lead, route it to the parent account owner with a 4-hour acceptance SLA. If the parent AE declines or does not respond, the child account becomes independently assignable.
3. For subsidiaries in different geographic regions where a regional AE exists, use a co-ownership model: parent AE retains relationship ownership, regional AE executes locally, and commission splits are defined (e.g., 60/40 favoring the executing rep).
4. Document all parent-child relationships in CRM using account hierarchy fields. LeanData's lead-to-account matching node can route based on parent-child relationships when hierarchies are configured [10].

*Key validation:*

Test the rule against the last 5 parent-child disputes. If the rule would have resolved 4 out of 5 correctly without escalation, it is sufficiently specific.

### Edge Case 2: Simultaneous Inbound and Outbound on the Same Account

*Scenario:*

Rep A has been prospecting Account X outbound for 3 weeks. Rep B receives an inbound demo request from Account X via marketing round-robin. Both reps believe they own the opportunity.

*Challenge:*

This is the most common and most contentious ROE dispute in B2B SaaS organizations. Attribution between inbound and outbound on the same account requires clear, pre-defined rules [2]. Without them, the resolution depends on who escalates faster or who has more organizational influence.

*Approach:*

1. Check for existing outbound activity: IF Rep A has logged 3+ outbound activities on Account X within the last 30 days AND has an open opportunity, THEN Rep A receives the inbound lead and is credited as opportunity owner.
2. IF Rep A has prospecting activity but no open opportunity, THEN Rep A has a 4-hour window to claim the inbound lead by creating an opportunity. If unclaimed, the lead routes to Rep B (the round-robin recipient).
3. IF Rep A's last activity on Account X is older than 30 days, THEN Rep A has no claim. The inbound lead routes normally.
4. Activity threshold matters: casual LinkedIn views do not count. Define qualifying activities explicitly (emails sent, calls logged, meetings booked -- all tracked in CRM or sales engagement platform like Outreach or Salesloft).

*Key validation:*

Run the rule against the last 10 inbound/outbound overlap disputes. If the rule produces a clear winner in 8 out of 10 cases without ambiguity, it is ready. If not, tighten the activity threshold or time window.

### Edge Case 3: Segment Transition Mid-Deal

*Scenario:*

An SMB AE has been working a deal with a 100-person company. During the sales cycle, the company raises a Series C and grows to 300 employees, crossing the Mid-Market threshold (200+ employees). The Mid-Market AE team argues the account should be reassigned.

*Challenge:*

Mid-deal segment transitions create competing interests: the SMB AE invested selling effort and has deal context, while the MM AE team is designed to handle accounts of this size. Forcing a transition mid-deal risks deal failure; allowing the SMB AE to keep it may set a precedent that undermines segment boundaries.

*Approach:*

1. Core rule: In-flight deals are never reassigned mid-cycle. The current owner completes the deal through close.
2. Post-close transition: After the deal closes (won or lost), the account is reassigned to the appropriate segment team at the next quarterly territory rebalance.
3. Compensation: The closing AE receives full commission on the current deal. If the account is reassigned post-close, the new segment owner receives credit for all subsequent deals.
4. Exception: If the deal stalls for 60+ days with no stage progression and the account has crossed the segment threshold, the account may be reassigned to the new segment with a warm handoff. The original AE receives a finder's fee (typically 10-25% of first-deal commission) for pipeline contribution.

*Key validation:*

Review the last 3 segment transition situations. Confirm the rule preserves deal momentum (no forced mid-cycle transitions) while maintaining segment integrity (accounts end up in the right segment within one quarter).

### Edge Case 4: Dormant Opportunity Reactivation

*Scenario:*

Rep A created an opportunity 6 months ago that went Closed-Lost. The same prospect now fills out a demo request form. Rep B (a new hire) is assigned via round-robin. Rep A argues they deserve the reactivation because they built the original relationship.

*Challenge:*

Closed-Lost opportunities sit in a gray zone. The original rep invested time, but the deal failed. Rewarding the original rep for reactivated deals can encourage gaming (closing deals as lost just before inactivity timeout, then claiming reactivation credit later).

*Approach:*

1. Define a reactivation window: IF the original opportunity was Closed-Lost within the last 90 days AND the original rep is still active, THEN the reactivation routes to the original rep.
2. IF the Closed-Lost date is more than 90 days ago, THEN the lead routes normally (round-robin or territory-based). The original rep has no claim.
3. IF the original rep has left the company, THEN the lead routes normally regardless of timing.
4. To prevent gaming: Closed-Lost opportunities must include a documented loss reason. Patterns of reps closing deals as lost and then reclaiming reactivations should trigger a RevOps audit.

*Key validation:*

Check the percentage of reactivated deals that fall within vs. outside the 90-day window. If more than 30% of reactivations come from recently Closed-Lost deals, the window length is appropriate. If most reactivations are 6+ months old, the window is irrelevant and can be shortened or eliminated.

### Edge Case 5: Partner vs. Direct Conflict

*Scenario:*

A channel partner submits a deal registration for Account Y. Two weeks later, an AE on the direct sales team identifies Account Y independently through outbound research and begins prospecting.

*Challenge:*

Partner relationships are strategic and long-term. Overriding partner deal registrations erodes trust and discourages partner sourcing. However, protecting every deal registration indefinitely prevents the direct team from working valuable accounts.

*Approach:*

1. Deal registration creates a time-boxed protection window (typically 60 days). During this window, the partner has primary ownership.
2. IF the direct AE identifies the account after deal registration, THEN the AE must coordinate with the Channel Manager and the partner. The AE may NOT create a competing opportunity.
3. IF the deal registration window expires without a qualified opportunity (defined as reaching Stage 2 or equivalent), THEN the account reverts to the direct team's open pool.
4. For co-selling situations: define a sourced vs. influenced credit model. Partner-sourced = partner gets primary credit and higher commission percentage. Partner-influenced = direct team gets primary credit, partner gets referral fee.
5. All deal registrations should be visible in CRM (via a Partner Deal Registration object or equivalent) so the direct team can check before prospecting.

*Key validation:*

Survey the partner team quarterly: "Do you feel deal registrations are respected?" If satisfaction drops below 70%, the protection window or enforcement is insufficient.

---

## References

[1] [Gradient Works - The Challenges of Rules of Engagement](https://www.gradient.works/blog/the-many-challenges-of-rules-of-engagement)
[2] [Gradient Works - Rules of Engagement Toolkit](https://www.gradient.works/resources/rules-of-engagement-for-sales)
[3] [Sales Enablement Collective - Sales: The Rules of Engagement](https://www.salesenablementcollective.com/sales-the-rules-of-engagement/)
[4] [Dear Stage 2 - From Turf Wars to Teamwork: How to Create Rules of Engagement](https://www.dearstage2.com/p/from-turf-wars-to-teamwork-how-to)
[5] [Traction Complete - 5 Tactics to Avoid Account Conflicts](https://tractioncomplete.com/articles/tactics-avoid-account-conflicts/)
[6] [Salesforce State of Sales 2024](https://www.salesforce.com/resources/research-reports/state-of-sales/)
[7] [Forrester - Sales Productivity Activity Study](https://www.forrester.com/resources/sales-productivity/activity-study/)
[8] [Gartner - Seller Time Spend Assessment](https://www.gartner.com/en/sales/research/seller-time-spend-assessment)
[9] [Everstage - Sales Productivity Statistics 2026](https://www.everstage.com/sales-productivity/sales-productivity-statistics)
[10] [LeanData - Lead-to-Account Match Node Guide](https://leandatahelp.zendesk.com/hc/en-us/articles/360040118814-Routing-Lead-to-Account-Match-Node-Guide)
