# Sales Territory Design — Implementation

> The end-to-end process for delivering Sales Territory Design projects. Follows the 4-phase framework: Strategy, Engineering, Enablement, Handoff. Educational/reference content is in the Appendix at the bottom.

## Project One-Pager

> Quick reference for architects. Scan in 2 minutes to understand what this project is, how it flows, and what tools are used.

### Sales Territory Design One-Pager

#### Project Type

- Category: Balanced (Strategic + Technical)
- Primary Deliverable: Balanced territory map with CRM-implemented assignment logic

##### Phase Relevance

| Phase          | Applies? | Weight | Notes                                                  |
| -------------- | -------- | ------ | ------------------------------------------------------ |
| 1. Strategy    | Yes      | Heavy  | 3-5 refinement loops across ICP, hierarchy, balancing  |
| 2. Engineering | Yes      | Medium | CRM territory object + assignment flow build           |
| 3. Enablement  | Yes      | Medium | Multi-audience training (leadership, ops, reps)        |
| 4. Handoff     | Yes      | Medium | Maintenance schedule + quarterly/annual review cadence |

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │    Heavy     │     │    Medium    │     │    Medium    │     │    Medium    │
  │ 1a→1b→1c→1d │     │ 2a→2b→2c→2d │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   3-5 refinement       CRM territory        Multi-audience       Maintenance +
   loops (ICP/bal.)     object + routing     training + hyper.    review cadence
```

**This project's flow:**
- Full 4-phase. Heavy strategy (ICP/TAM valuation, segmentation hierarchy, territory balancing), medium engineering (CRM territory object + routing flow), standard enablement and handoff.
- Strategy phase has a natural feedback loop: segmentation hierarchy (1c) often needs revision after balancing data reveals real account distribution. Expect 2-4 iterations between hierarchy and balancing.
- Some customers with very simple system needs may compress Phase 2. No phases are skipped.

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Watch territory design intro video (5-10 min) explaining methodology and what to expect
- [ ] Complete intake form: current territory structure, segment definitions, team org chart, growth expectations, fiscal year timing
- [ ] Gather customer list with contract values (for benchmarking valuation methodology)
- [ ] Get exec sponsor alignment on project scope and timeline

##### Track B: Architect Prep
- [ ] Pull CRM data: current accounts, existing territory assignments, routing rules
- [ ] Run Clay workbook with account universe and initial enrichment
- [ ] Build v0 ICP tier matrix from existing customer data and firmographic patterns
- [ ] Draft v0 account valuation methodology benchmarked against existing contracts
- [ ] Prepare current-state territory assessment (visual hierarchy + balance snapshot)

#### Refinement Loop (1b -&gt; 1c -&gt; 1d)

| Meeting             | Sub-Phase | Focus                                          | Stakeholder              | Output                        |
| ------------------- | --------- | ---------------------------------------------- | ------------------------ | ----------------------------- |
| Kickoff             | 1b        | Present v0 ICP/TAM + valuation, gather context | VP Sales, RevOps         | Feedback for v1 valuation     |
| ICP/TAM Workshop    | 1c        | Build tiered ICP matrix together               | VP Sales, RevOps         | Approved ICP tier matrix      |
| Valuation Review    | 1c        | Validate account dollar values                 | VP Sales, RevOps         | Approved valuation methodology|
| Hierarchy Review    | 1c        | Present segmentation cuts and priority order    | VP Sales, Sales Directors| Approved hierarchy pyramid    |
| Balancing Review 1  | 1c        | Present balanced territories (count + value)   | VP Sales, Sales Directors| Feedback for redrawing        |
| Balancing Review 2+ | 1c        | Iterate on territory boundaries                | VP Sales, Sales Mgmt    | Socialized territory map      |
| Sign-Off            | 1d        | Final territory approval                       | CRO/VP Sales             | Locked territory assignments  |

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held
- [ ] 1c. Refinement loop complete (ICP -&gt; valuation -&gt; hierarchy -&gt; balancing -&gt; socialization)
- [ ] 1d. Strategic sign-off: territories locked, hierarchy approved, growth cuts documented

##### Phase 2: Engineering
- [ ] 2a. Tech spec: territory object schema + flow logic documented
- [ ] 2b. Engineering handoff meeting held
- [ ] 2c. Build: territory object created, assignment flow built, edge cases handled
- [ ] 2d. QA: routing tested across all territory segments + customer sign-off

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped (video walkthroughs, guides, FAQ)
- [ ] 3b. Training sessions delivered (leadership, ops, reps)
- [ ] 3c. Hypercare: 30-day routing monitoring + office hours
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented (monthly/quarterly/annual cadences)
- [ ] 4b. Internal handoff complete
- [ ] 4c. External handoff (LeanScale -&gt; Customer) complete
- [ ] 4d. Project closed and archived

#### Document Types

##### Working Documents (iterate together)

| Document                       | Purpose                                    | When Complete                           |
|--------------------------------|--------------------------------------------|-----------------------------------------|
| Intake form                    | Capture current state and discovery inputs | All fields filled, validated at kickoff |
| ICP tier matrix (working)      | Define account qualification tiers         | Client-approved tier criteria           |
| Account valuation spreadsheet  | Assign dollar values to all accounts       | Methodology approved, all accounts valued|
| Territory balancing workbook   | Draw and iterate territory boundaries      | All territories within acceptable variance|
| Segmentation hierarchy diagram | Visualize cut priority order               | Client-approved pyramid                 |

##### Deliverables (polished outputs)

| Deliverable                     | Created From                    | Customer Uses For                      |
|---------------------------------|---------------------------------|----------------------------------------|
| Balanced Territory Map          | Balancing workbook              | Board presentation, rep communication  |
| Territory Hierarchy Document    | Hierarchy diagram               | Internal alignment, new hire onboarding|
| Growth-Ready Territory Plan     | Balancing workbook + hierarchy  | Hiring decisions, expansion planning   |
| Valuation Methodology Document  | Valuation spreadsheet           | Quarterly refresh reference            |
| Definition Alignment Document   | ICP tier matrix + discovery     | Stakeholder alignment                  |

#### Enablement Details

##### Training Types

| Type       | Audience                        | Focus                                              | Duration |
| ---------- | ------------------------------- | -------------------------------------------------- | -------- |
| Leadership | VP Sales, CRO, Directors        | Territory strategy, growth planning, dispute policy | 45 min   |
| Operations | RevOps, Sales Ops               | Territory object management, routing maintenance, valuation refresh | 60 min   |
| Sales Mgmt | Sales Managers                  | Rep territory explanation, performance coaching, dispute handling | 30 min   |
| IC Reps    | AEs, SDRs                       | Account ownership, dispute process, anchoring points | 30 min   |

##### Hypercare
- Applies: Yes
- Duration: 30 days post-rollout
- Office Hours: Weekly 30-min slot for routing issues and questions

##### Training Assets to Create
- [ ] Video walkthrough: Territory structure walkthrough (hierarchy + balancing rationale)
- [ ] Video walkthrough: Territory object management demo (rep changes, new territories)
- [ ] Doc: Territory Update Guide (step-by-step for common operations)
- [ ] Doc: Routing Troubleshooting Guide
- [ ] Doc: Rules of Engagement for territory disputes

#### Handoff & Retention

##### Internal Handoff
- Key context for Architect: Territory hierarchy rationale, growth-ready cuts, which territories are sensitive (concentration risk, geographic splits)
- Escalation trigger: Any structural changes (new hierarchy cuts, major rebalancing, product cuts). Architect handles rep changes and simple boundary adjustments.

##### External Handoff (LeanScale -&gt; Customer)
- Final meeting agenda: Live territory demo, routing test, maintenance walkthrough, rules of engagement review, refinement expectations
- Documentation package: All deliverables, training recordings, FAQ, maintenance schedule

##### Maintenance Schedule
- Monthly: Account loading review, territory object hygiene, routing spot-check
- Quarterly: TAM/valuation refresh, territory balance review, performance correlation
- Annually: Full territory redesign evaluation, segmentation threshold review
- Who owns: Single project = customer owns | Dedicated = Architect owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services (ongoing territory optimization) -&gt; if no -&gt; Downsell: Lead Routing project or Commission Redesign -&gt; Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~1 quarter after rollout
- Internal prep trigger: 2 weeks before check-in
- Decision: Architect handles if minor tweaks / deeper engagement needed if structural redesign

#### Key Assets

| Asset                           | Link                    | When Used          |
| ------------------------------- | ----------------------- | ------------------ |
| ICP TAM Template                | Teamwork                | Phase 1 (1a/1c)   |
| Territory Balancing Playground  | Google Sheets (Wealth)  | Phase 1 (1c)      |
| Territory Loader / Plan Loader  | Google Sheets           | Phase 1 (1c)      |
| Clay Workbook Template          | Clay                    | Phase 1 (1a/1c)   |
| Territory Object Schema         | Salesforce              | Phase 2 (2c)      |

#### Definition Alignment Terms

| Term                    | Typical Definition                                                                        |
| ----------------------- | ----------------------------------------------------------------------------------------- |
| Territory               | A defined set of accounts assigned to a specific rep or team based on hierarchy criteria   |
| Segmentation Hierarchy  | The ordered sequence of cuts (size, geography, industry, etc.) that determines assignment  |
| Account Valuation       | Dollar estimate of an account's revenue potential, used for territory balancing             |
| ICP Tier (T1/T2/T3)    | Account qualification level based on fit criteria -- T1 is best fit, T3 is lowest          |
| Named Account           | Strategic target assigned to a specific rep regardless of other hierarchy criteria          |
| Territory Balance       | Equitable distribution of accounts by both COUNT and VALUE across all territories          |
| Holdover Policy         | Rules governing what happens to in-progress deals when territories change                  |
| Rules of Engagement     | Dispute resolution process for contested account ownership                                 |
| Anchoring Point         | A rep's core territory assignment -- what they keep even when farming broader areas         |
| Pre-Planned Cuts        | Future territory boundaries designed in advance for when team grows                        |
| Territory Object        | Salesforce custom object storing territory definitions and team assignments as data records |

#### Common Gotchas

- Balancing on count only without balancing on value -&gt; One rep has 100 SMB accounts, another has 100 enterprise accounts. Balance BOTH dimensions.
- Assuming segmentation hierarchy is final before loading real data -&gt; "Once we get all the data, you realize all your assumptions are all effed up." Plan for 2-4 iterations between hierarchy and balancing.
- Underestimating calendar time vs. hours -&gt; Client sees "20 hours" and thinks "two weeks." Reality is two months of back-and-forth review and socialization.
- Assigning all of California to one rep -&gt; California and New York contain 15-20% of US business. Go sub-state (city or zip code level) for high-density areas.
- Missing holdover policy before rollout -&gt; Reps lose accounts they have been farming for months. Define rules before territories go live.
- Not designing for growth -&gt; Mid-year territory chaos when team scales. Build pre-planned cuts from day one.
- Concentration risk in territories -&gt; If one account represents half a territory's value, the rep is dependent on closing that single deal. Distribute high-value accounts.
- Hard-coded routing logic -&gt; When someone leaves, you have to edit Salesforce workflows. Use the territory object approach for code-free updates.

#### Methodology Options

| Option                                  | When to Use                                                       | Complexity |
| --------------------------------------- | ----------------------------------------------------------------- | ---------- |
| Light ICP/TAM (valuation focus)         | Wide TAM companies (AI, horizontal products) -- "TAM is everyone" | Low        |
| Deep ICP/TAM (criteria research)        | Narrow TAM with specific firmographic/technographic criteria       | High       |
| Simple Hierarchy (2-3 cuts)             | Teams of 5-15 reps, flat org, regional focus                      | Low        |
| Complex Hierarchy (4+ cuts)             | Teams of 15+, named accounts, industry/product specialization     | High       |
| Custom Territory Object (LS standard)   | Most engagements -- code-free updates, flexible, proven            | Medium     |
| Salesforce Enterprise Territory Mgmt    | Client strongly prefers native Salesforce, willing to pay          | Medium     |

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on the complete territory design -- ICP tiers, account valuations, segmentation hierarchy, and balanced territory map.
>
> **Output:** Locked territory assignments with growth-ready cuts, signed off by VP Sales/CRO.

### 1a. Pre-Kickoff

> Two parallel tracks run after the deal closes and before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                          | Format             |
| ----------------------------- | ---------------------------------------------------------------- | ------------------ |
| Territory Design Intro Video  | Explain methodology: ICP/TAM -&gt; hierarchy -&gt; balancing -&gt; system | Video walkthrough (5-10 min)    |
| Definition Alignment Document | Get stakeholder sign-off on key terms before we build anything   | Google Doc         |
| Intake Form                   | Current territory structure, segment definitions, team org, growth plans, fiscal year timing | Google Form or Doc |

**Intake form specifics:**
- Current territory definitions (e.g., "Enterprise is $1B+ annual revenue, Commercial is below $1B")
- Current assignment logic (round robin, manual, geographic)
- Sales team org chart with roles (AEs, SDRs, SEs, CSMs, AMs)
- Existing customer list with contract values (for benchmarking)
- Expected headcount trajectory (how fast is the team growing?)
- Fiscal year start date (territories must be ready before FY rollout)
- Partner ecosystem details (if applicable -- adds cannibalization complexity)
- Pain points with current territory structure

**Completion tracking:** Someone's job to follow up. Don't cancel kickoff if incomplete, but push hard after.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                                        | Output                                   |
| ---- | ----------------------------------------------------------------------------- | ---------------------------------------- |
| 1    | Pull CRM data: existing accounts, routing rules, assignment history            | Raw data collected                       |
| 2    | Set up Clay workbook: import account universe, configure enrichment columns    | Enriched account list                    |
| 3    | Build v0 ICP tier matrix from existing customer patterns                       | Draft T1/T2/T3 criteria (all ASSUMED)    |
| 4    | Build v0 account valuation: benchmark against existing contracts               | Valued account list (all ASSUMED)        |
| 5    | Draft current-state territory assessment: hierarchy diagram, balance snapshot   | Where they are now vs. where gaps exist  |
| 6    | Prepare kickoff call assets: presentation, questions list, definition document  | Ready for kickoff                        |

**For wide TAM clients (e.g., AI companies):** Skip deep ICP research. Focus on valuation methodology. The ICP tier matrix shifts from "who qualifies" to "what makes a T1 vs T2 vs T3" based on existing customer characteristics.

**For narrow TAM clients (specific criteria):** Configure Claygent prompts for specialized research (e.g., "Is this company SOC2 certified?" "Has this company had a public data breach?"). Build detailed tiered ICP matrix with firmographic/technographic criteria.

**For partner complexity:** Add Claygent prompts for hyperscaler relationships and partner ecosystem. Build columns for cannibalization tracking. Budget 5+ additional hours.

**Critical:** Mark everything as ASSUMED. The kickoff call validates.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building anything.

| Term                    | Our Definition                                                              | Internally Approved? |
| ----------------------- | --------------------------------------------------------------------------- | -------------------- |
| Territory               | A defined set of accounts assigned to a rep/team based on hierarchy criteria | [ ] Yes / [ ] No     |
| Enterprise              | Companies with $X+ annual revenue (client-specific threshold)                | [ ] Yes / [ ] No     |
| Commercial              | Companies below Enterprise threshold                                         | [ ] Yes / [ ] No     |
| Named Account           | Strategic target assigned regardless of other hierarchy criteria              | [ ] Yes / [ ] No     |
| Account Value           | Estimated contract potential based on benchmarking methodology               | [ ] Yes / [ ] No     |
| Territory Balance       | Equitable distribution by both account count AND total value                 | [ ] Yes / [ ] No     |

**Instructions to customer:**

> Review each definition with your leadership team. Check "Yes" when approved. We cannot proceed with territory design until segment definitions and valuation approaches are aligned.

---

### 1b. Kickoff Call

> **Purpose:** Present v0 and get alignment. We walk in with ICP/TAM work done, draft valuations, and a current-state assessment. Customer reacts, not creates from scratch.

#### Agenda (60-90 min)

| Time  | Topic                        | What Happens                                             |
| ----- | ---------------------------- | -------------------------------------------------------- |
| 0-20  | Walk through v0 ICP + TAM    | "Here's our ICP tier matrix and valuation approach"       |
| 20-35 | Validate assumptions         | ASSUMED -&gt; CONFIRMED or corrected on valuations and tiers |
| 35-50 | Definition alignment         | Review key terms -- segment thresholds, named accounts    |
| 50-65 | Current-state assessment     | "Here's your current territory structure and its gaps"    |
| 65-75 | Growth and timeline context  | Fiscal year timing, headcount trajectory, 18-month plan   |
| 75-90 | Next steps                   | Schedule ICP workshop, assign data homework               |

#### What We Bring

- v0 ICP tier matrix and account valuation methodology
- Current-state territory assessment (hierarchy diagram + balance snapshot)
- Questions list (what we need to validate -- TAM width, partner complexity, segment thresholds)
- Definition Alignment Document (pre-filled with our recommendations)

#### What We Leave With

- Confirmed TAM approach: light ICP (wide TAM) or deep ICP (narrow TAM)
- Feedback on valuation methodology (adjust benchmarks, hedge factors)
- Confirmed segment definitions or clear path to resolution
- Customer list with contract values (if not yet provided)
- ICP workshop scheduled

---

### 1c. Alignment Loop &amp; Strategic Meeting Cadence

> **Purpose:** Iterate through ICP, valuation, hierarchy, and balancing until sign-off. This project has more refinement meetings than most because the balancing phase inherently creates feedback loops with the hierarchy.

#### The Pattern

```
Kickoff Call (gather context, validate approach)
    |
ICP/TAM Workshop -> approved tier matrix
    |
Valuation Review -> approved methodology, valued account list
    |
Hierarchy Review -> approved segmentation cuts
    |
Load accounts into balancing workbook
    |
Balancing Review 1 (present territories) -> feedback
    |
Redraw boundaries, possibly revise hierarchy
    |
Balancing Review 2+ -> iterate until balance achieved
    |
Client socializes with sales management (expect weeks)
    |
Final Review -> locked territories with growth-ready cuts
```

#### Before Each Meeting

1. Process previous meeting feedback
2. Update relevant working document (valuation model, hierarchy diagram, or balancing workbook)
3. Prepare questions for next validation round

#### During Each Meeting

1. Walk through current version
2. Capture corrections and refinements
3. Validate what is now CONFIRMED
4. Identify remaining ASSUMED items

#### After Each Meeting

1. Apply feedback to working documents
2. Track what moved from ASSUMED -&gt; CONFIRMED
3. Re-run balance metrics if territory boundaries changed

#### Meeting Types for Sales Territory Design

| Meeting Type             | Focus                                                     | Stakeholder                  |
| ------------------------ | --------------------------------------------------------- | ---------------------------- |
| ICP/TAM Workshop         | Build tiered ICP matrix, define what makes T1/T2/T3       | VP Sales, RevOps             |
| Account Valuation Review | Validate dollar values on accounts                        | VP Sales, RevOps             |
| Hierarchy Review         | Define and validate segmentation cuts and priority order   | VP Sales, Sales Directors     |
| Balancing Review         | Territory boundary drawing, count + value balance          | VP Sales, Sales Directors, Mgmt |
| Socialization            | Client-internal meetings to get sales management buy-in    | Sales Management (client-led) |
| Final Review             | Full walkthrough, lock territories, approve growth cuts    | CRO/VP Sales + all stakeholders|

#### Typical Timeline

| Milestone                           | Timing                                               |
| ----------------------------------- | ---------------------------------------------------- |
| Pre-kickoff prep                    | 1-2 weeks (CRM data pull, Clay setup, v0 prep)       |
| Kickoff call                        | Day 1 of engagement                                  |
| ICP -&gt; valuation -&gt; hierarchy loop  | 2-3 weeks                                            |
| Territory balancing loop            | 3-6 weeks (most time-consuming: review + socialization)|
| Final review + sign-off             | When sales management has bought in                   |

**Calendar time warning:** 100-200 hours of LeanScale work translates to 2-3 months of calendar time. "They see 20 hours, they're like, we can do that in two weeks. And it's like, well, it's gonna take two months."

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm everything is locked before building in the CRM.

#### Validation Checkpoint

- [ ] ICP tier matrix approved (T1/T2/T3 criteria confirmed)
- [ ] Account valuation methodology approved and all accounts valued
- [ ] Segmentation hierarchy approved (cut order, geographic granularity, named accounts)
- [ ] Territory map balanced by both COUNT and VALUE
- [ ] Growth-ready cuts documented (pre-planned splits for team expansion)
- [ ] Personnel allocation model confirmed (pod/coverage/ratio)
- [ ] Sales management has socialized and bought in
- [ ] Definition Alignment Document signed off by stakeholders
- [ ] VP Sales or CRO has given explicit sign-off on territory assignments
- [ ] No blockers for engineering

#### Decision Point

- **Proceed to Engineering** -&gt; Build territory object and routing in CRM
- **This project always proceeds to Engineering** -- the strategic deliverable alone (the territory map) is valuable, but system implementation is required for territories to actually function

---

## Phase 2: Engineering

> **Goal:** Build the CRM infrastructure so territories actually route correctly and can be maintained without code changes.
>
> **Output:** Working territory object + assignment flow in Salesforce, tested and customer-approved.

| Project Type    | Engineering Weight | Context                                                   |
| --------------- | ------------------ | --------------------------------------------------------- |
| Sales Territory | Medium (25-35%)    | Territory object + flow build. 15-20 hours. Straightforward once strategy is locked. |

### Sub-Phases

```
2a Tech Spec -> 2b Engineering Handoff -> 2c Build -> 2d QA/Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate the approved territory map into a technical specification for CRM implementation.

**Input:** Signed-off territory map, hierarchy pyramid, personnel allocation model, valued account list

**What happens:**

1. Map each hierarchy cut to Salesforce field logic (size -&gt; revenue field, geography -&gt; state/city/zip, industry -&gt; industry field)
2. Define territory object schema: fields for each hierarchy criterion + team member assignments
3. Define flow logic: incoming record -&gt; hierarchy evaluation order -&gt; territory object lookup -&gt; owner assignment
4. Document edge cases: named account overrides, missing data fallback, boundary accounts, partner-sourced routing

**Output:** Tech spec containing:

- Territory__c object schema (all fields, relationships, record types)
- Assignment flow logic diagram (evaluation order matching hierarchy priority)
- Edge case handling rules
- Build sequence (object first, then flow, then edge cases, then testing)

**System implementation approach decision:**

| Approach                                | When to Use                                      | Trade-offs                          |
| --------------------------------------- | ------------------------------------------------ | ----------------------------------- |
| Custom Territory Object (LS standard)   | Most engagements. Code-free updates, proven.      | Requires initial custom build       |
| Salesforce Enterprise Territory Mgmt    | Client strongly prefers native, willing to pay    | Less familiar, historically mixed results |

LeanScale standard is the custom territory object. "We built from scratch based on a need... hasn't really changed in about three years." Worth evaluating Salesforce native if client requests it.

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs with engineer before building.

**Who attends:** Architect + Engineer

**Agenda (30-45 min):**

| Time  | Topic                        | What Happens                                     |
| ----- | ---------------------------- | ------------------------------------------------ |
| 0-15  | Walk through territory design | Strategic context: hierarchy, balancing, growth   |
| 15-30 | Review tech spec              | Object schema, flow logic, edge cases             |
| 30-45 | Refine and approve            | Adjust specs, confirm build approach              |

**What engineer leaves with:**

- Approved tech spec
- Clear build sequence: territory object -&gt; flow -&gt; edge cases -&gt; testing
- Known risks: geographic granularity (zip code routing), partner routing, missing data scenarios

---

### 2c. Build

> **Purpose:** Build the territory object and assignment flow in Salesforce.

**Input:** Approved tech spec from 2b

**Build components:**

| Component                  | What Gets Built                                                           |
| -------------------------- | ------------------------------------------------------------------------- |
| Territory Object           | Territory__c with fields: name, size segment, region, sub-region, industry, AE, SDR, SE, CSM |
| Territory Records          | One record per territory loaded from approved territory map                |
| Assignment Flow            | Record-triggered flow: evaluate hierarchy criteria -&gt; lookup territory object -&gt; assign owner + team |
| Named Account Override     | Direct match on account ID bypasses all other logic                        |
| Missing Data Fallback      | Default assignment when required routing fields are empty                   |
| Geographic Granularity     | City or zip code level routing for California, New York, other high-density areas |

**The territory object approach -- why it works:**

The flow stays consistent. "Instead of having to create a full flow with branches for everything, you can just build a flow that says: look for these strings -- size, revenue size, your territory, your industry. And then based on those criteria, find the best match and send it to the right people."

When a rep leaves: "You just go into the object and update account team seller AE from X to Y and all of a sudden it's fixed moving forward." No code changes required.

**Build tracking:**

- [ ] Territory__c object created with all fields
- [ ] Page layout configured for easy editing
- [ ] All territory records loaded from approved map
- [ ] Assignment flow built (record-triggered or platform event)
- [ ] Named account override logic configured
- [ ] Missing data fallback configured
- [ ] Geographic sub-state routing configured (if applicable)

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify routing works correctly across all scenarios.

**Test case categories:**

| Type                  | What to Test                                        | Pass Criteria                   |
| --------------------- | --------------------------------------------------- | ------------------------------- |
| Standard routing      | Normal accounts through each territory segment       | Correct territory assignment    |
| Boundary cases        | Accounts at size thresholds between segments          | Consistent assignment per rules |
| Geographic edge cases | California sub-regions, zip code routing              | Correct sub-state assignment    |
| Named accounts        | Override routing for strategic targets                | Named account rep gets account  |
| Missing data          | Accounts with blank industry, geography, or size     | Falls to correct default        |
| Team member update    | Change AE in territory object, verify new assignment | New AE gets subsequent accounts |

**Technical testing checklist:**

- [ ] All territory segments route correctly (test 1+ account per territory)
- [ ] Named accounts bypass all other logic
- [ ] Missing data falls to correct default
- [ ] Team member changes in object reflect immediately in new assignments
- [ ] Sub-state routing works for high-density areas
- [ ] No errors in flow logs

**Customer testing:**

- Walk customer through live routing demo
- Create test lead in the call, show flow assigning to correct territory
- Have RevOps test common update scenarios (rep change, new territory, boundary adjustment)

**Engineering sign-off checkpoint:**

- [ ] Built system matches tech spec
- [ ] All test cases passing
- [ ] Customer has tested and approved
- [ ] Ready for enablement

---

## Phase 3: Enablement

> **Goal:** Customer team can actually use and maintain the territory system.
>
> **Output:** Trained team with documentation, stabilized routing, no critical issues.

### Sub-Phases

```
3a Training Prep -> 3b Training Sessions -> 3c Hypercare -> 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from project documentation.

**Input:** Territory map + hierarchy document + tech spec + built system

**Training package:**

- Video walkthrough scripts: territory structure walkthrough, territory object management demo, routing troubleshooting
- Written guides: Territory Update Guide (how to change reps, add territories, modify boundaries), Routing Troubleshooting Guide (how to diagnose incorrect assignments)
- FAQ draft: "What if a rep leaves?" "What about disputed accounts?" "How do we know it's working?" "When do we re-do territories?"
- Rules of Engagement document: dispute resolution process, holdover policy for territory transitions

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to all stakeholder groups.

**Training sessions by audience:**

| Audience           | Focus                                                                    | Key Topics                                                                   |
| ------------------ | ------------------------------------------------------------------------ | ---------------------------------------------------------------------------- |
| VP Sales / CRO     | Strategic: territory rationale, growth planning, hiring pitch material    | Hierarchy logic, growth-ready cuts, "here's exactly what you're getting"      |
| Sales Directors    | Strategic: territory explanation, dispute escalation                      | How to explain territory assignments to reps, when to approve disputes        |
| RevOps / Sales Ops | Technical: system management, ongoing maintenance                         | Territory object updates, flow maintenance, valuation refresh process, balance monitoring |
| Sales Managers     | Tactical: rep-level territory coaching, dispute handling                   | Walking reps through their territory, performance vs. territory issues        |
| AEs / SDRs         | Tactical: account ownership, dispute process, future expectations         | How to find your accounts, how to flag misassigned accounts, what you might lose to new hires |

**Training delivery:**

1. Schedule sessions with appropriate stakeholders (can combine if team is small)
2. Deliver training (live, record everything)
3. Record video walkthroughs for future reference and new hire onboarding
4. Answer questions, document anything that feeds into FAQ

**Output:**

- Trained stakeholders at every level
- Video recordings for future reference
- Updated FAQ from real questions

---

### 3c. Hypercare

> **Purpose:** Intensive post-launch support during the first 30 days of territory rollout.

**Duration:** 30 days

**What happens:**

- Weekly 30-min office hours: anyone can hop on and flag routing issues, misassigned accounts, or questions
- Routing accuracy monitoring: sample 50+ accounts created since rollout, verify correct assignment
- Bug triage: fix any systematic routing errors immediately
- Rep feedback collection: "Can you realistically cover this territory?" "Are there accounts that feel misassigned?"
- Hierarchy validation: confirm segmentation cuts produce expected distribution with real data

**First sales cycle validation (30-90 days post-rollout):**

- Are territory boundaries producing expected account distribution?
- Are there territories where reps have no realistic shot at quota?
- Did geographic granularity decisions (California splits) prove correct?
- Does the routing logic need adjustment?

**Output:** Stabilized routing, no critical issues outstanding, real-data validation of territory design

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm customer can operate territory system independently.

**Validation checkpoint:**

- [ ] All training sessions delivered (leadership, ops, managers, reps)
- [ ] Training video walkthroughs and documentation provided
- [ ] 30-day hypercare period complete
- [ ] No critical routing issues outstanding
- [ ] RevOps can update territory object independently
- [ ] Rules of engagement documented and communicated to sales team
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** -&gt; System is stable, team is enabled
- **Extend Hypercare** -&gt; Routing issues still being resolved or team not yet confident

---

## Phase 4: Handoff

> **Goal:** Clean project close with maintenance plan established and retention/expansion path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the system, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule -> 4b Internal Handoff -> 4c External Handoff -> 4d Project Close
                                                    (LS -> Customer)       (Archive + Debrief)
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At                                                                         |
| ----------------------------- | -------------------- | ------------------------------------------------------------------------------------- |
| **Single Project**            | Customer owns        | 4c (External Handoff) -- customer receives maintenance schedule and runs it themselves |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) -- Architect receives maintenance schedule and runs it for customer |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention to keep territories balanced, accurate, and aligned with business growth.

#### Monthly Tasks

| Monthly Task                | What to Check                                                  | Red Flag Threshold                           |
| --------------------------- | -------------------------------------------------------------- | -------------------------------------------- |
| New account loading review  | New CRM accounts route to correct territories per hierarchy     | &gt;5% of new accounts routing incorrectly      |
| Territory object hygiene    | Team member records current (handle departures, role changes)   | Any departed rep still assigned in object     |
| Data quality spot-check     | Sample 10-20 leads through routing logic                        | Any systematic routing drift                  |

#### Quarterly Tasks

| Quarterly Task               | What to Review                                                 | Action if Off-Track                           |
| ---------------------------- | -------------------------------------------------------------- | --------------------------------------------- |
| TAM/Valuation refresh        | Re-run valuation methodology with updated signals and new accounts | Reload updated valuations, flag major shifts  |
| Territory balance review     | Account count + total value per territory -- check for drift    | If &gt;20% variance: investigate, propose rebalance |
| Performance data correlation | Closed-won rates by territory -- design issue vs. rep issue?    | If territory consistently underperforms: flag for review |

#### After First Sales Cycle (30-90 days post-launch)

This is the first major validation checkpoint when real data reveals whether the territory design works.

- **Routing accuracy audit:** Sample 50+ accounts created since rollout. Verify each routed correctly.
- **Rep feedback collection:** Interview 3-5 reps. "Can you realistically cover this territory?" "What's falling through the cracks?"
- **Hierarchy validation:** Confirm segmentation cuts still make sense with real account distribution.

*Key question:* Are there territories where reps have no realistic shot at quota? If so, rebalancing is needed.

#### Refinement Triggers (when to re-engage)

| Trigger                        | Threshold                              | Response                                       |
| ------------------------------ | -------------------------------------- | ---------------------------------------------- |
| Territory value drift          | One territory has 2x value of another in same segment | Re-engage for rebalancing           |
| Major team change              | 3+ reps hired or departed in a quarter  | Activate pre-planned cuts or emergency redesign |
| Market shift                   | New product line, acquisition, new geography | Scope hierarchy restructuring project    |
| Routing accuracy degradation   | &lt;90% routing accuracy in monthly spot-check | Investigate flow logic, update territory object |

#### Every 6-12 Months (Annual Territory Review)

- **Full territory redesign evaluation:** Has the team scaled enough to warrant new hierarchy cuts? Have products changed enough to add product cuts?
- **Segmentation threshold review:** Do Enterprise/Commercial definitions still make sense? Has the market shifted?
- **Growth-ready cuts validation:** Are pre-planned territory splits still appropriate for upcoming hiring?

*Key validation:* Do territories still provide 18+ months of runway before requiring major redesign?

---

### 4b. Internal Handoff

> **Purpose:** Transfer context so Architect can manage ongoing relationship.

**What the Architect needs to know:**

- Territory hierarchy rationale (why cuts are prioritized in this order)
- Which territories are sensitive (concentration risk, high-density geographic splits, borderline segments)
- Growth-ready cuts: what triggers the split, how it works
- Customer stakeholder map: who is the decision maker, who is the day-to-day contact, who has political influence
- Common issues and how to resolve: rep changes (update territory object), disputed accounts (follow Rules of Engagement workflow)

**Escalation guidelines:**

| Issue Type                                           | Who Handles                           | Examples                                           |
| ---------------------------------------------------- | ------------------------------------- | -------------------------------------------------- |
| Rep changes, simple boundary tweaks, record updates   | Architect                             | "AE left, update territory object"                 |
| Structural redesign, new hierarchy cuts, major rebalancing | Deeper engagement needed          | "Adding product cuts," "3x team growth needs new territories" |

---

### 4c. External Handoff (LeanScale -&gt; Customer)

> **Purpose:** Formal project completion with customer.

**Final project meeting agenda:**

- **Show territories live:** Walk through territory object in Salesforce, demonstrate territory summary by count and value
- **Explain hierarchy:** Visual walkthrough of hierarchy pyramid, why cuts are prioritized in this order, how named accounts are handled
- **Demonstrate routing:** Create test lead live in the call, show flow assigning to correct territory, demonstrate edge case handling
- **Territory management training:** Rep change demo, new territory demo, boundary change demo, troubleshooting walkthrough
- **Review the numbers:** Final territory summary (count + value per territory), balance metrics, growth-ready cuts
- **Set refinement expectations:** First 30 days monitoring, quarterly valuation refresh, annual redesign consideration, trigger thresholds
- **Address common concerns:** "What if a rep leaves?" "What about disputed accounts?" "How do we know it's working?"
- **Make it explicit:** "Project complete."

**Documentation package delivered:**

- Balanced Territory Map (finalized)
- Territory Hierarchy Document
- Growth-Ready Territory Plan
- Valuation Methodology Document
- Definition Alignment Document (final version)
- Territory Update Guide
- Routing Troubleshooting Guide
- Rules of Engagement
- All training video recordings
- FAQ document
- Maintenance Schedule
- Support contact info

**For Single Project engagements:** Walk the customer through the maintenance schedule in detail. Record a video walkthrough of the walkthrough. Make sure they understand what to check, how often, and when to call us back.

**Output:** Customer owns the territory system. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location
- [ ] Handoff documentation complete
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized

#### Internal Debrief (Optional but Recommended)

- What went well?
- What would we do differently? (balancing iterations, timeline estimates, stakeholder alignment)
- Any learnings to feed back into SOPs or methodology?

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell -&gt; Downsell -&gt; Retry  |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (ongoing territory optimization, quarterly rebalancing, annual redesign)
   | if no
2. Downsell: Lead Routing project (operationalize territory logic) or Commission Redesign (align comp to new territories)
   | if yes
3. Retry retainer at end of next project cycle
```

**Natural follow-on projects:**
- **Lead Routing:** Territory definitions become the routing logic. "Territory design = theoretical, lead routing = system implementation."
- **Commission Redesign:** "Commission redesign usually goes hand-in-hand with territory redesign because we're changing what people are responsible for."
- **Market Map:** If ICP/TAM phase revealed data gaps, scoping a deeper Market Map project.

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On \[date ~quarter out\], we'll review how territories are performing and see if any adjustments are needed."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                                  |
| ------------------- | ------------------------------------------------------------- |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks               |
| 2. Review metrics   | Pull territory balance reports, routing accuracy, rep feedback |
| 3. Decide ownership | Can Architect handle this check-in, or need deeper engagement? |
| 4. Prep materials   | Prep talking points and review materials                       |

**At the refinement check-in:**

- Review territory performance against original design
- Check balance drift: has one territory accumulated disproportionate value?
- Check if growth-ready cuts need activation (new hires)
- If minor adjustments: Architect handles tweaks in territory object
- If major redesign needed: Scope new project

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables &amp; Assets Summary

**Strategic Deliverables:**

- ICP Tier Matrix -- documented T1/T2/T3 criteria validated against existing customers
- Account Valuation Model -- methodology documentation and applied valuations for entire account universe
- Valued Account List -- complete export of all accounts with dollar values and tier designations
- Territory Hierarchy Document -- visual representation of segmentation cuts and priority order
- Balanced Territory Map -- finalized territories with account counts and values per territory
- Growth-Ready Territory Plan -- pre-planned cuts for future expansion
- Definition Alignment Document -- stakeholder-approved term definitions

**Technical Deliverables:**

- Territory Object (Territory__c) -- configured Salesforce custom object with all territory records and team assignments
- Assignment Flow -- working lead/account routing logic in Salesforce
- Named Account Override Logic -- routing bypass for strategic targets
- Test Documentation -- test cases and results demonstrating routing accuracy across all scenarios

**Documentation Package:**

- Training video recordings (structure walkthrough, object management demo)
- Territory Update Guide (step-by-step for rep changes, new territories, boundary adjustments)
- Routing Troubleshooting Guide (diagnosing incorrect assignments)
- Rules of Engagement (territory dispute resolution process)
- FAQ document
- Maintenance Schedule (monthly/quarterly/annual cadences)

---

## Appendix

### What This Document Is

This is the **implementation playbook** -- the step-by-step execution guide an Architect follows to deliver a Sales Territory Design project from first contact to project close. It is the third file in a 3-file playbook structure: Overview (positioning and outcomes), Methodology (frameworks and concepts), and Implementation (execution with checklists).

### What Each Phase Produces

| Phase                    | Output                                                                 | Gate Criteria                                                                  |
| ------------------------ | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **Phase 1: Strategy**    | Signed-off strategic package (Definition Alignment Doc + deliverables) | Customer stakeholders have approved definitions and strategic asset            |
| **Phase 2: Engineering** | Built and tested system                                                | System matches tech spec, all tests pass, customer has approved                |
| **Phase 3: Enablement**  | Trained team with documentation                                        | All training delivered, hypercare complete, team can operate independently     |
| **Phase 4: Handoff**     | Independent customer + archived project                                | Internal/external handoffs complete, maintenance plan in place, project closed |

### How to Adapt Per Project Type

Not every project weighs each phase equally. Before starting, determine your project's profile:

| Project Profile       | Strategy Weight | Engineering Weight | Enablement Weight | Example Projects               |
| --------------------- | --------------- | ------------------ | ----------------- | ------------------------------ |
| **Strategic-heavy**   | 60-80%          | 10-20%             | 10-20%            | Growth Model, GTM Strategy     |
| **Engineering-heavy** | 10-20%          | 60-80%             | 10-20%            | CRM Migration, Data Pipeline   |
| **Enablement-heavy**  | 20-30%          | 20-30%             | 40-50%            | Quote-to-Cash, Process Rollout |
| **Balanced**          | 30-40%          | 30-40%             | 20-30%            | Attribution, Lead Scoring      |

**Adaptation rules:**

- **Light phases** can compress sub-phases (e.g., a strategic-only project may skip Phase 2 entirely)
- **Heavy phases** expand with more sub-steps, more meetings, more preparation
- **Phase 4 always applies** -- every project needs handoff, but the maintenance schedule complexity varies
- Mark phases as \[SKIP\] or \[LIGHT\] in the One-Pager if they don't fully apply
