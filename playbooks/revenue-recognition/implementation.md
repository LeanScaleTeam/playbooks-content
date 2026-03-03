# RevRec (Revenue Recognition) -- Implementation

## Project One-Pager

### RevRec (Revenue Recognition) One-Pager

#### Project Type

- Category: Balanced (heavy pre-work strategy, moderate engineering)
- Primary Deliverable: Six RevRec fields with workflow logic in Salesforce

##### Phase Relevance

| Phase          | Applies? | Weight | Notes                                                          |
| -------------- | -------- | ------ | -------------------------------------------------------------- |
| 1. Strategy    | Yes      | Heavy  | Pre-work is "the hard part" -- golden number, operating plan, quotas, bookings policy |
| 2. Engineering | Yes      | Medium | Mapping exercise + field/workflow build in SFDC                |
| 3. Enablement  | Yes      | Light  | Training on field definitions, reporting, bookings policy      |
| 4. Handoff     | Yes      | Light  | Internal + External, maintenance schedule for field logic      |

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │    Heavy     │     │   Medium     │     │    Light     │     │    Light     │
  │ 1a→1b→1c→1d │     │ 2a→2b→2c→2d │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   Golden number,       Mapping exercise     Training on field    Internal + External
   operating plan       + SFDC build         definitions          maintenance schedule
```

**This project's flow:**
- Full 4-phase. Heavy strategy (60-70% of effort), medium engineering (20-30%), light enablement and handoff (10%).
- Pre-work in Phase 1 takes longer than most teams expect. Do not skip or compress it.
- Phase 2 is straightforward once Phase 1 alignment is complete. The mapping doc IS the tech spec.
- Phase 3 is short -- primarily training finance, sales, and CS on field definitions and reporting views.
- Some customers skip 3c Hypercare if RevRec is standalone (no CPQ).

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held -- golden number confirmed, operating plan reviewed
- [ ] 1c. Refinement loop complete -- mapping doc finalized, bookings policy approved
- [ ] 1d. Strategic sign-off obtained from finance, sales, and CS

##### Phase 2: Engineering
- [ ] 2a. Tech spec created (RevRec mapping doc with all scenario logic)
- [ ] 2b. Engineering handoff meeting held -- engineer understands all scenarios
- [ ] 2c. Build complete -- six fields with workflows configured in SFDC
- [ ] 2d. QA/Test -- walk through all deal scenarios + customer sign-off

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped -- field definitions guide, reporting walkthrough script
- [ ] 3b. Training sessions delivered to finance, sales, CS/AM, RevOps
- [ ] 3c. Hypercare period complete (if applicable -- 2 weeks for standalone, 4 weeks with CPQ)
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff complete
- [ ] 4c. External handoff (LeanScale &rarr; Customer) complete
- [ ] 4d. Project closed and archived

#### Definition Alignment Terms

| Term                              | Typical Definition                                                                                           |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| Revenue                           | All money brought in -- both recurring and non-recurring                                                     |
| Bookings                          | Money brought in by sales that is usually recurring. May exclude PLG/self-serve depending on company definition |
| ARR (Annual Recurring Revenue)    | MRR x 12                                                                                                    |
| MRR (Monthly Recurring Revenue)   | Recurring revenue measured on a monthly basis                                                                |
| ACV (Annual Contract Value)       | TCV divided by the number of years in the contract. Represents average annual revenue from a single customer |
| TCV (Total Contract Value)        | Total revenue expected from a single customer contract over its entire duration, including recurring fees and one-time charges (setup, implementation) |
| Net New ARR                       | Only positive deal values; contractions and churn show as zero. Used for sales forecasting and commissions   |
| Net ARR (Net Revenue)             | Full deal value including negatives (contraction, churn). Used for CS/AM tracking and net retention           |
| Contract ARR                      | Sum of all active contracts for an account. Used as the basis for renewal calculations                       |
| Co-terming                        | Setting expansion contract end dates to match the original contract end date                                 |
| Golden Number                     | The specific revenue metric a company is tracking as their primary growth target                              |
| Operating Plan                    | "The company in numbers" -- financial blueprint for revenue targets, expenses, and profit by region, product, and team |
| Bookings Policy                   | Documented rules for how reps handle expansions, renewals, co-terming, POC treatment, and what counts as ARR |
| Revenue Movement Formula          | SFDC formula tracking revenue impacts (upsell, contraction, churn, new business) regardless of timing        |
| Recurring Amount                  | The recurring portion of a deal, excluding services                                                          |
| Opportunity Type                  | Salesforce categorization (new business, expansion, renewal, contraction, churn) that drives RevRec field logic |

#### Common Gotchas

- **Skipping the golden number** -- Customers cannot articulate what "the number" means, and architects skip getting alignment. This throws off every downstream field calculation. &rarr; Ask on day one. Expect pushback. Persist. "50 million what?"
- **Building on opportunities instead of contracts** -- Contract ARR (sum of all active contracts) is nearly impossible to calculate without contract objects in SFDC. &rarr; Ensure Salesforce contracts are set up before starting RevRec build.
- **Not mapping opportunity types first** -- RevRec logic depends on knowing if a deal is new, expansion, renewal, contraction, or churn. Without properly configured opportunity types, field calculations break. &rarr; Map all opportunity types and record types before building any workflows.
- **Using Net ARR for sales forecasting** -- If sales does not own churn, using Net ARR (which includes negatives) distorts their forecasts and commission calculations. &rarr; Use Net New ARR for sales; Net ARR for CS/AM.
- **Not co-terming expansions** -- Creating a new full-term contract for each expansion sounds reasonable but creates staggered renewal dates. This is a tracking nightmare and bad for customer experience. &rarr; Define co-terming as mandatory in the bookings policy.
- **No bookings policy exists** -- Without documented rules, reps create their own approaches for expansions and renewals. Data becomes inconsistent. &rarr; Create or define the bookings policy as part of Phase 1 pre-work.
- **Not getting finance involved early** -- RevRec stems from how the business builds its operating plan. Finance must be in the room from the first conversation. &rarr; Loop in the finance team (or whoever owns the operating plan) at project start.
- **Churn ownership left undefined** -- "This is always a loaded topic." The entire Net New ARR vs. Net ARR split depends on who owns churn. If this is not resolved, field logic cannot be finalized. &rarr; Ask explicitly in pre-kickoff: who owns churn? Sales, CS, or Account Managers?
- **Coterminous expansion vs. mid-term expansion confusion** -- The Revenue Movement Formula must handle expansion happening at renewal AND mid-term. If only one pattern is built, the other breaks. &rarr; Map both patterns in the mapping exercise.
- **Teams only tracking partial funnel** -- Some teams only track SQLs and bookings, not the full revenue funnel. RevRec requires visibility into the complete picture. &rarr; Assess current tracking scope during discovery.

#### Methodology Options

| Option                    | When to Use                                          | Complexity |
| ------------------------- | ---------------------------------------------------- | ---------- |
| RevRec Standalone (Simple)| Small team, single product, single region, ~10 hrs   | Low        |
| RevRec Standalone         | Mid-complexity, 20-50 hrs, multiple deal types       | Medium     |
| RevRec + CPQ              | CPQ implementation underway, 150+ hrs, full quarter  | High       |

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on revenue definitions, deal scenarios, and RevRec field logic before building anything.
>
> **Output:** Approved RevRec Mapping Doc + Definition Alignment Document + Bookings Policy (signed off by finance, sales, and CS stakeholders).

### 1a. Pre-Kickoff

> Two parallel tracks run after the deal closes and before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                       | Format             |
| ----------------------------- | ------------------------------------------------------------- | ------------------ |
| RevRec Intro Video            | Explain what RevRec is, why pre-work matters, what we need    | Video (5-10 min)   |
| Definition Alignment Document | Get stakeholder sign-off on revenue terms                     | Google Doc         |
| Pre-Kickoff Questionnaire     | Confirm golden number, operating plan access, churn ownership | Google Form or Doc |

**Customer homework items:**

1. **Define the Golden Number** -- "You're trying to hit $X this year. What does that number actually represent? Revenue? Bookings? ARR? MRR? ACV? TCV?" Most teams struggle to answer this question clearly on the first ask.
2. **Provide the Operating Plan** -- The company's financial blueprint. Includes revenue targets by region, product type, and team. Usually lives in Excel or Google Sheets.
3. **Provide Quotas &amp; Commissions Structure** -- How quotas are built, who gets credit for what. The critical question: who owns churn?
4. **Provide or Draft a Bookings Policy** -- Documented rules for expansions, renewals, co-terming, and what counts as ARR. If none exists, flag this as a deliverable.

**Completion tracking:** Follow up before kickoff. If the operating plan and golden number are not provided, the kickoff call will stall. Push hard on these two items.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                                        | Output                                     |
| ---- | ----------------------------------------------------------------------------- | ------------------------------------------ |
| 1    | Review sales notes and intake for revenue model type (PLG, sales-led, hybrid) | Client revenue profile                     |
| 2    | Audit existing SFDC setup: contracts, opportunity types, record types          | Current state assessment of SFDC structure |
| 3    | Check if contracts are being used (not just opportunities)                    | Blocker identification (no contracts = blocker) |
| 4    | Draft RevRec mapping doc with ASSUMED values for all six fields              | v0 mapping doc                             |
| 5    | Prepare kickoff call agenda and discovery questions                           | Questions list                             |

**Critical:** Mark everything as ASSUMED. The kickoff call validates.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on revenue terms BEFORE building anything. RevRec implementations fail when teams disagree on definitions mid-build.

Use the Definition Alignment Terms table (see Section 1, above) as the sign-off checklist. Send to the customer's finance team and leadership. All terms must be approved before proceeding to the mapping exercise.

---

### 1b. Kickoff Call

> **Purpose:** Validate the golden number, review the operating plan, and confirm revenue definitions. We walk in with a draft mapping doc -- customer reacts, not creates from scratch.

#### Agenda (60-90 min)

| Time  | Topic                          | What Happens                                                   |
| ----- | ------------------------------ | -------------------------------------------------------------- |
| 0-20  | Reverse demo of operating plan | Customer walks through THEIR plan -- how they view revenue     |
| 20-35 | Golden number confirmation     | Pin down the exact metric: revenue, bookings, ARR, ACV, etc.  |
| 35-50 | Definition alignment           | Review Definition Alignment Doc; capture sign-offs or blockers |
| 50-60 | Churn ownership discussion     | Who owns churn? Sales gets upside only? CS owns downside?      |
| 60-75 | Current SFDC review            | Contract setup, opportunity types, record types                |
| 75-90 | Next steps                     | Assign homework, schedule refinement meetings                  |

**Key discovery questions for the kickoff:**

1. "You're trying to hit $X this year. $X what?" -- Force specificity on the golden number.
2. "Walk us through your operating plan." -- Reverse demo first.
3. "What is the golden number, how is it shown? Monthly? Quarterly? Per Product? Per region? Per segment?"
4. "How is commission calculated/reported? Is this based on the golden number?"
5. "What are the key components to the revenue portion of your model?"
6. "Who owns churn? Do they get penalized for churn?"
7. "Are you using contracts in Salesforce or just opportunities?"
8. "Do you co-term expansions or create new contracts?"
9. "Do you have a bookings policy? If so, can we see it?"
10. "Are POCs counted as ARR?"

#### What We Bring

- v0 RevRec mapping doc (drafted in Track B, all values marked ASSUMED)
- Definition Alignment Document (pre-filled with our recommended definitions)
- Questions list from Track B prep
- Current state assessment of SFDC configuration

#### What We Leave With

- Golden number confirmed (or clear action items to get it confirmed with finance)
- Operating plan reviewed -- we understand how they break out revenue
- Churn ownership decision (or escalation path to get the decision)
- Definition Alignment Document partially approved (or blockers identified)
- SFDC contract status confirmed (blocker if no contracts)

---

### 1c. Alignment Loop &amp; Strategic Meeting Cadence

> **Purpose:** Iterate on the RevRec mapping doc until all scenarios are confirmed and all definitions are signed off.

#### The Pattern

```
Kickoff Call (gather definitions + operating plan context)
    |
Update mapping doc with confirmed values -> v1
    |
Meeting 2: RevRec Mapping Review (present v1, walk through scenarios)
    |
Refine mapping doc -> v2
    |
Meeting 3: Bookings Policy + Final Alignment
    |
Final mapping doc + bookings policy -> v3
    |
Sign-Off Meeting -> Final versions
```

#### RevRec-Specific Meeting Types

| Meeting Type              | Focus                                                        | Stakeholder                     |
| ------------------------- | ------------------------------------------------------------ | ------------------------------- |
| Operating Plan Review     | Revenue breakouts, product types, regions, segments          | Finance + CEO                   |
| RevRec Mapping Review     | Walk through all six fields across all deal scenarios        | RevOps + Finance                |
| Bookings Policy Workshop  | Define rules for expansions, renewals, co-terming, POCs      | Sales + CS + Finance            |
| Final Alignment           | Full mapping walkthrough + definition sign-off               | All stakeholders                |

**Key guidance for the mapping review:**

- Present the mapping doc first, then share with the client for feedback.
- For larger teams, circulate the document before the meeting so finance can review.
- Create a non-workflow version (table format) for finance stakeholders who may not read workflow diagrams: "This view is oftentimes a lot easier for go-to-market people."

#### Typical Timeline

| Milestone               | Timing                                     |
| ----------------------- | ------------------------------------------ |
| Pre-kickoff prep        | 3-5 days                                   |
| Kickoff call            | Day 1 of engagement                        |
| Mapping review          | 1-2 weeks after kickoff                    |
| Bookings policy workshop| 1-2 weeks after mapping review             |
| Final alignment + sign-off | When all definitions confirmed           |
| Total Phase 1           | 2-4 weeks (depends on finance availability)|

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm everything is aligned before building. This is the gate between strategy and engineering.

#### Validation Checkpoint

- [ ] Golden number defined and confirmed by finance
- [ ] Definition Alignment Document signed off by all stakeholders
- [ ] RevRec mapping doc covers all deal scenarios (new business, expansion, flat renewal, expansion renewal, contraction, churn)
- [ ] All six fields defined with correct logic per scenario
- [ ] Churn ownership explicitly decided and documented
- [ ] Bookings policy approved (or drafted if none existed before)
- [ ] Opportunity types and record types mapped
- [ ] Contracts confirmed in SFDC (or set up as prerequisite)
- [ ] No blockers for engineering

#### Decision Point

- **Proceed to Engineering** -- Mapping doc is approved, definitions are signed off, SFDC is ready
- **Loop back to 1c** -- Finance has not signed off on definitions, churn ownership unresolved, or contracts not set up in SFDC

> RevRec projects do NOT have a natural exit point after Phase 1. The strategic deliverable (mapping doc + definitions) has limited value without the technical build. Proceed to Phase 2 in all cases.

---

## Phase 2: Engineering

> **Goal:** Build the six RevRec fields with workflow logic in Salesforce based on the approved mapping doc.
>
> **Output:** Six configured fields, workflows firing correctly across all deal scenarios, Revenue Movement Formula operational.

| Project Type              | Engineering Weight | Example                                              |
| ------------------------- | ------------------ | ---------------------------------------------------- |
| RevRec Standalone (Simple)| Light (30%)        | ~10 hrs -- small team, just fields with workflows    |
| RevRec Standalone         | Medium (40%)       | 20-50 hrs -- multiple deal types, contract setup     |
| RevRec + CPQ              | Heavy (60%)        | 150+ hrs -- full quarter, CPQ config drives RevRec   |

### Sub-Phases

```
2a Tech Spec (Mapping Doc) -> 2b Engineering Handoff -> 2c Build -> 2d Test
```

---

### 2a. Tech Spec (Mapping Doc as Tech Spec)

> **Purpose:** The RevRec mapping doc created in Phase 1 IS the tech spec. It translates revenue definitions into field-level logic.

**Input:** Signed-off RevRec mapping doc + Definition Alignment Document + bookings policy

**What the mapping doc contains:**

For each deal scenario (new business, expansion, flat renewal, expansion renewal, contraction, churn), the mapping shows:

| Field              | What It Tracks                                                    |
| ------------------ | ----------------------------------------------------------------- |
| Recurring Amount   | The recurring portion of the deal (excludes services)             |
| Net New ARR        | Only positive values; if negative (downgrade), shows zero         |
| Net ARR            | Takes both positive and negative values; captures churn impact    |
| Contract ARR       | Sum of all active contracts for account; basis for renewals       |
| ACV                | Annual contract value (includes services, normalized by term)     |
| TCV                | Total contract value (includes services, full term value)         |

**Worked example from the mapping:**

*New Business:*
```
Given: $100K recurring + $20K services, 2-year term
- Recurring Amount: $100K
- Net New ARR: $100K (positive = same as recurring)
- Net ARR: $100K (positive = same as net new)
- Contract ARR: $100K (first deal on account)
- ACV: ($100K + $20K) / 1 = $120K per year
- TCV: ($100K + $20K) x 2 = $240K
```

*Expansion (co-termed):*
```
Given: Original $100K, expansion $40K recurring, co-termed
- Recurring Amount: $40K (this deal only)
- Net New ARR: $40K
- Net ARR: $40K
- Contract ARR: $140K ($100K + $40K)
- Renewal basis: $140K
```

*Contraction:*
```
Given: Contract ARR $140K, contraction -$40K
- Net New ARR: $0 (only takes positive -- does not penalize sales)
- Net ARR: -$40K (captures full negative impact)
- Contract ARR: $100K (reduced)
```

*Churn:*
```
Given: Contract ARR $100K, full churn
- Net New ARR: $0
- Net ARR: -$100K
- Contract ARR: $0
```

**Output:** Mapping doc with deal-scenario-to-field logic -- this is handed directly to the engineer.

---

### 2b. Engineering Handoff

> **Purpose:** Walk the engineer through the mapping doc so they understand the business logic behind every field.

**Who attends:** Architect + Engineer

**Agenda (30-45 min):**

| Time  | Topic                    | What Happens                                                     |
| ----- | ------------------------ | ---------------------------------------------------------------- |
| 0-15  | Walk through mapping doc | Architect explains each deal scenario and field behavior          |
| 15-30 | Review SFDC requirements | Opportunity types, record types, contract objects, workflow triggers |
| 30-45 | Agree on build sequence  | Fields first, then workflows, then Revenue Movement Formula      |

**What the Architect brings:**

- Approved RevRec mapping doc (the tech spec)
- Definition Alignment Document (for context on revenue terms)
- SFDC current state assessment (opportunity types, record types, contract status)
- Bookings policy (for context on business rules)

**What the Engineer leaves with:**

- Clear understanding of all six fields and their logic per scenario
- Build sequence: (1) create fields, (2) build workflow logic, (3) configure Revenue Movement Formula
- List of opportunity types and record types needed
- Known edge cases: co-terming, mid-term expansion vs. renewal expansion, within-term contraction

---

### 2c. Build (Configure)

> **Purpose:** Build the six RevRec fields with workflow logic in Salesforce.

**Input:** Approved mapping doc from 2b

**Build components:**

**Step 1: Create fields and apply logic**
- Create all six RevRec fields in SFDC
- Ensure all fields are created and logic is applied correctly before beginning install
- Use Opportunity Record Types and Opportunity Types to establish correct logic
- If CPQ is involved, configure with the Quote-to-Cash process

**Step 2: Build workflows**
- Create workflow rules that calculate field values based on opportunity type
- Net New ARR workflow: MAX(deal_recurring, 0) -- only passes positive values
- Net ARR workflow: passes actual deal value (positive or negative)
- Contract ARR workflow: sums all active contracts at the account level

**Step 3: Configure Revenue Movement Formula**
- "Gold Standard Tracking" -- reporting across all revenue impacts (upsell, contraction, churn, new business) regardless of timing
- Main consideration: expansion can happen coterminously or at renewal; contraction can happen within term
- Must handle both mid-term changes and renewal-time changes

**Build tracking:**

- [ ] Recurring Amount field created with logic
- [ ] Net New ARR field created with positive-only logic
- [ ] Net ARR field created with full value logic
- [ ] Contract ARR field created with account-level aggregation
- [ ] ACV field created with term normalization
- [ ] TCV field created with full-term calculation
- [ ] Workflow rules configured for each opportunity type
- [ ] Revenue Movement Formula configured and tested
- [ ] Contract ARR lives at both opportunity and account level

**Execution approach:** Manual build by engineer. RevRec workflows are too logic-dependent for automated tooling at this stage. Engineer builds directly in SFDC using the mapping doc as the reference.

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify every deal scenario calculates correctly in SFDC.

**Two types of testing:**

| Type              | Who      | Purpose                                              |
| ----------------- | -------- | ---------------------------------------------------- |
| Technical Testing | Engineer | Verify workflows fire and fields calculate correctly |
| Customer Testing  | Client   | Verify the numbers match how they think about revenue |

**Technical testing checklist:**

- [ ] New Business scenario: all six fields calculate correctly
- [ ] Expansion (co-termed) scenario: Contract ARR sums correctly, Net New ARR captures positive value
- [ ] Expansion with services: ACV and TCV include services
- [ ] Flat Renewal: Contract ARR stays the same, appropriate fields populate
- [ ] Expansion Renewal: Contract ARR increases, renewal amount reflects expanded total
- [ ] Contraction: Net New ARR shows $0, Net ARR shows negative, Contract ARR reduces
- [ ] Churn: Net New ARR shows $0, Net ARR shows full negative, Contract ARR goes to $0
- [ ] Revenue Movement Formula reports correctly across all timing scenarios (mid-term + at renewal)
- [ ] Contract ARR rolls up correctly at the account level
- [ ] Workflows fire on all relevant opportunity types and record types
- [ ] Edge case: coterminous expansion vs. mid-term expansion handled correctly
- [ ] Edge case: within-term contraction handled correctly

**Customer testing:**

- Walk the customer through each scenario using real or realistic deal data in SFDC
- Have finance validate that the field values match their expected calculations
- Get explicit confirmation from finance that the numbers are correct

**Engineering sign-off:** All six fields calculating correctly across all scenarios, Revenue Movement Formula operational, customer has tested and approved, no outstanding issues, ready for enablement.

---

## Phase 3: Enablement

> **Goal:** Finance, sales, CS, and RevOps teams understand what the RevRec fields mean, how to use them for reporting, and what the bookings policy requires.
>
> **Output:** Trained teams with documentation. All stakeholders can interpret RevRec reports and follow bookings policy rules.

### Sub-Phases

```
3a Training Prep -> 3b Training Sessions -> 3c Hypercare -> 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials from the RevRec mapping doc, definition alignment doc, and bookings policy.

**Input:** Approved mapping doc + definition alignment doc + bookings policy + configured SFDC fields

**Training materials to create:**

| Material                              | Purpose                                                      | Audience           |
| ------------------------------------- | ------------------------------------------------------------ | ------------------ |
| Field Definitions Reference Doc       | One-page reference: what each of the six fields means        | All teams          |
| Bookings Policy (final, distributable)| Rules for expansions, renewals, co-terming, POC treatment    | Sales + CS         |
| Reporting Walkthrough Script          | How to pull RevRec reports in Salesforce                     | RevOps + Finance   |
| Revenue Metrics Quick Reference       | Net New ARR vs Net ARR -- when to use which                  | Sales + CS leaders |
| RevRec Field Walkthrough Script       | What each field shows with real examples                     | All teams          |

**Key content for the Field Definitions Reference Doc:**

| Field           | What It Shows                           | Who Uses It              | Example                              |
| --------------- | --------------------------------------- | ------------------------ | ------------------------------------ |
| Recurring Amount| Recurring portion of this deal          | RevOps, Finance          | $100K (excludes $20K services)       |
| Net New ARR     | Positive-only deal impact               | Sales (forecasting, commissions) | Expansion: $40K; Contraction: $0 |
| Net ARR         | Full deal impact (positive and negative)| CS/AM (net retention)    | Expansion: $40K; Contraction: -$40K  |
| Contract ARR    | Total active contract value for account | Finance (renewals)       | $140K (original + expansion)         |
| ACV             | Annual contract value with services     | Finance, Sales leadership| $120K/yr on a 2-year deal            |
| TCV             | Full contract value over term           | Finance, Legal           | $240K (2 years x $120K)             |

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to each stakeholder group so they can use RevRec fields and follow the bookings policy.

**Training sessions by audience:**

| Session    | Audience                    | Focus                                                                              | Duration | Format    |
| ---------- | --------------------------- | ---------------------------------------------------------------------------------- | -------- | --------- |
| Leadership | CFO, VP Finance, CEO        | What each RevRec field means at the reporting level; how to read revenue dashboards | 30 min   | Live call |
| Sales/CS   | Reps, AMs, Sales Mgmt, CS   | Bookings policy rules: co-terming, expansion handling, what counts toward quotas   | 45 min   | Live call |
| Technical  | RevOps, SFDC Admin           | How fields calculate, how to troubleshoot workflows, how to handle new scenarios   | 60 min   | Live call |

**Leadership training -- key points:**
1. Walk through each of the six fields using real deal examples
2. Show the difference between Net New ARR and Net ARR -- "They look the same when positive, they look different when negative"
3. Explain how Contract ARR drives renewal amounts
4. Show how Revenue Movement Formula enables reporting across all revenue impacts

**Sales/CS training -- key points:**
1. Walk through the bookings policy: what to do when a customer wants to add licenses, when they want to downgrade, when they want to renew
2. Explain co-terming and why it matters -- "Co-terming is easier for the customer and for your renewal management"
3. Clarify churn ownership: who sees what in their forecasting vs. CS tracking
4. Explain what counts toward their quotas and commissions (based on which RevRec field -- usually Net New ARR for sales)

**Technical training -- key points:**
1. Walk through the workflow logic behind each field
2. Show how opportunity types and record types drive field calculations
3. Explain how to handle new scenarios (e.g., a new product line, a new deal type)
4. Cover the Revenue Movement Formula configuration
5. Walk through the maintenance tasks (see Phase 4a)

**Output:**
- Trained stakeholders across finance, sales, CS, and RevOps
- Video recordings for each session (for future reference and new hire onboarding)
- Questions log (feeds into FAQ and bookings policy clarifications)

---

### 3c. Hypercare

> **Purpose:** Post-launch support to catch issues in real deal scenarios during the first business cycle.

**Duration:**
- RevRec Standalone: 2 weeks
- RevRec with CPQ: 4 weeks

**What happens during hypercare:**
- Weekly 30-minute office hours on calendar -- anyone can bring deal scenarios that seem off
- Monitor first batch of real deals flowing through RevRec fields
- Check that workflows are firing correctly on new opportunities
- Validate Contract ARR is rolling up accurately as deals close
- Watch for edge cases not covered in the mapping doc (e.g., a deal type the client did not anticipate)

**Common hypercare issues:**
- Opportunity created with wrong type/record type -- field calculates incorrectly
- Contract ARR not updating because contract object was not created for the deal
- Renewal amount showing wrong number because expansion was not co-termed
- Net New ARR showing zero on a legitimate new business deal (wrong opportunity type)

**When to skip:** RevRec Standalone with low complexity (small team, simple deal structure, ~10 hour build) may not need formal hypercare. A single check-in call 1-2 weeks post-launch is sufficient.

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm the customer team can operate RevRec independently.

**Validation checkpoint:**

- [ ] All training sessions delivered (Leadership, Sales/CS, Technical)
- [ ] Training recordings recorded and shared
- [ ] Field Definitions Reference Doc distributed
- [ ] Bookings Policy distributed to sales and CS
- [ ] Hypercare period complete (if applicable)
- [ ] No critical issues outstanding (all deal scenarios calculating correctly)
- [ ] RevOps/Admin can troubleshoot basic workflow issues
- [ ] Ready for handoff

**Decision point:**
- **Proceed to Handoff** -- Teams are trained, fields are working, no open issues
- **Extend Hypercare** -- Edge cases surfacing that need additional workflow adjustments

---

## Phase 4: Handoff

> **Goal:** Clean project close with maintenance plan for ongoing RevRec field integrity and retention/expansion path established.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the system, project archived, future revenue path set.

**Structure:**

```
4a Maintenance Schedule -> 4b Internal Handoff -> 4c External Handoff -> 4d Project Close
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At |
| ----------------------------- | -------------------- | ------------- |
| **Single Project**            | Customer owns        | 4c (External Handoff) |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention to keep RevRec fields accurate as deals flow through the system and business conditions change.

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task                       | What to Check                                                | Red Flag Threshold                              |
| ---------------------------------- | ------------------------------------------------------------ | ----------------------------------------------- |
| Field calculation spot-check       | Run 5-10 recent closed deals through RevRec field validation | Any deal where field values do not match expected logic |
| Workflow firing audit              | Verify workflows are firing on new opportunities             | Any opportunity type where workflow did not trigger |
| Contract ARR reconciliation        | Check Contract ARR at account level against active contracts | Contract ARR diverges from sum of active contracts by &gt;5% |

**Quarterly Tasks:**

| Quarterly Task                    | What to Review                                               | Action if Off-Track                             |
| --------------------------------- | ------------------------------------------------------------ | ----------------------------------------------- |
| Bookings policy compliance review | Are reps following co-terming rules? Are POCs being tracked correctly? | Update bookings policy and re-train if violations found |
| New deal type assessment          | Any new products, pricing models, or contract structures?    | Add new scenarios to RevRec mapping and update workflows |
| Revenue definition drift check    | Are teams still using the agreed definitions for the golden number? | Re-align with finance if definitions have shifted |
| Opportunity type/record type audit| Any new types created that are not mapped to RevRec logic?   | Map new types and configure workflows           |

**After First Business Cycle (60-90 days post-launch):**

- Validate that RevRec fields produced accurate numbers for the first full reporting period
- Compare RevRec field outputs against finance's manual calculations or ERP data
- Check: Does Contract ARR match what finance expects for renewal forecasting?
- Check: Do Net New ARR and Net ARR correctly separate sales vs. CS ownership of metrics?
- Key question: Are commission calculations producing correct results based on RevRec fields?

**Refinement Triggers (when to re-engage):**

| Trigger                                          | Threshold                                      | Response                                                   |
| ------------------------------------------------ | ---------------------------------------------- | ---------------------------------------------------------- |
| New product line or pricing model introduced      | Any                                            | Re-engage specialist to add scenarios to mapping doc       |
| Opportunity types changed or added                | Any new type not in RevRec mapping             | Update workflows for new types                             |
| Contract ARR diverges from finance expectations   | &gt;10% variance on 3+ accounts               | Audit and fix; may need mapping doc update                 |
| Bookings policy violations becoming frequent      | &gt;3 violations per month                     | Re-training + bookings policy refresh                      |
| Company restructures revenue definitions          | Any change to the golden number                | Full Phase 1 re-engagement required                        |

**Every 6-12 Months:**

- Full RevRec field audit: run all deal scenarios through validation (the same test matrix from Phase 2d)
- Bookings policy annual review with finance and sales leadership
- Check if new business motions (e.g., launching PLG, adding enterprise tier) require RevRec mapping updates
- Validate Revenue Movement Formula still covers all active deal patterns

---

### 4b. Internal Handoff

> **Purpose:** Transfer context so Architect can manage the ongoing relationship and basic RevRec maintenance.

**What the Architect needs to know:**

- What was built: six RevRec fields with workflow logic, configured to the client's specific revenue definitions
- Golden number: what metric the client tracks and how it is defined
- Churn ownership: who owns churn (sales, CS, or AM) and how the field logic reflects this
- Bookings policy: the key rules reps follow (co-terming, expansion handling, POC treatment)
- Common issues: wrong opportunity type selected (most common field error), Contract ARR not updating (usually a missing contract object)
- When to escalate: new product lines, structural changes to revenue definitions, bookings policy overhaul

**Escalation guidelines:**

| Issue Type                                  | Who Handles                        | Example                                           |
| ------------------------------------------- | ---------------------------------- | ------------------------------------------------- |
| Field not calculating on a specific deal    | Architect (check opportunity type first)  | Rep used wrong opp type -- fix the type            |
| Bookings policy question from a rep         | Architect (reference the bookings policy) | "Do I co-term this 3-month expansion?"             |
| New product line needs RevRec mapping       | Specialist                         | Client launches a new SKU with different pricing   |
| Revenue definition change from finance      | Specialist                         | Golden number changed from bookings to ARR         |
| Workflow logic needs modification           | Specialist + Engineer              | New deal pattern not covered in original mapping   |

**For Dedicated engagements:** Architect receives the maintenance schedule (4a) and becomes responsible for executing monthly and quarterly tasks.

---

### 4c. External Handoff (LeanScale &rarr; Customer)

> **Purpose:** Formal project completion. Customer receives all documentation and understands ongoing maintenance.

**Final project meeting agenda:**

1. Review what was delivered: six RevRec fields, workflows, Revenue Movement Formula
2. Walk through documentation package
3. Demo the reporting views powered by RevRec fields
4. Review the bookings policy one more time
5. Walk through the maintenance schedule (monthly, quarterly, annual tasks)
6. Confirm nothing outstanding
7. Make it explicit: "The RevRec project is complete."

**Documentation package:**

- RevRec Mapping Doc (final, approved version -- serves as the system reference)
- Field Definitions Reference Doc (one-page reference for all six fields)
- Bookings Policy Document (final, distributable version)
- Definition Alignment Document (final, signed-off version)
- Training video recordings (Leadership, Sales/CS, Technical)
- Maintenance Schedule (monthly/quarterly/annual tasks)
- FAQ document (compiled from training Q&amp;A and hypercare issues)

**For Single Project engagements:** Walk the customer through the maintenance schedule in detail. Record a video walkthrough. Make sure they understand what to check, how often, and when to call LeanScale back.

**Output:** Customer owns the RevRec system. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] RevRec mapping doc saved to customer project folder
- [ ] All documentation package items saved and shared
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                          |
| ----------------------------- | ----------------------------- |
| **Single Project**            | Upsell &rarr; Downsell &rarr; Retry   |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In  |

**Single Project Path:**

```
1. Upsell: Managed Services (quarterly RevRec audits, bookings policy reviews)
   | if no
2. Downsell: CPQ implementation (RevRec usually accompanies CPQ ~60-70% of the time)
   | or
3. Downsell: Growth Model, Attribution, or other GTM project
   | if yes to any
4. Retry retainer at end of next project cycle
```

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in ~1 quarter after go-live. Review RevRec field accuracy on recent closed deals, check if new deal types need mapping, validate bookings policy compliance. Minor adjustments handled by Architect; major changes (new product lines, structural changes) scoped as new engagement.

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables &amp; Assets Summary

**Strategic Deliverables:**

| Deliverable                   | Description                                                    |
| ----------------------------- | -------------------------------------------------------------- |
| RevRec Mapping Doc            | Complete scenario-to-field mapping for all deal types          |
| Definition Alignment Document | Signed-off revenue term definitions                            |
| Bookings Policy               | Rules for expansions, renewals, co-terming, POC treatment      |

**Technical Deliverables:**

| Deliverable                      | Description                                                    |
| -------------------------------- | -------------------------------------------------------------- |
| Six RevRec Fields (SFDC)         | Recurring Amount, Net New ARR, Net ARR, Contract ARR, ACV, TCV |
| Workflow Logic (SFDC)            | Workflows calculating field values by opportunity type         |
| Revenue Movement Formula (SFDC)  | Gold Standard Tracking across all revenue impacts              |

**Documentation Package:**

- Field Definitions Reference Doc
- Training video recordings (Leadership, Sales/CS, Technical)
- Reporting walkthrough video
- Maintenance Schedule
- FAQ document

---

## References

[1] [Cohen &amp; Co - 3 Revenue Recognition Challenges for Software and SaaS Companies in 2025](https://www.cohenco.com/knowledge-center/insights/january-2025/3-revenue-recognition-challenges-and-tips-for-software-and-saas-companies-in-2025)
[2] [Orb - SaaS Revenue Recognition: ASC 606 Compliance Guide](https://www.withorb.com/blog/saas-revenue-recognition-guide)
[3] [Salesforce Ben - How to Manage Revenue Recognition in Salesforce](https://www.salesforceben.com/how-to-manage-revenue-recognition-in-salesforce/)
[4] [HubiFi - Salesforce Revenue Cloud: The Ultimate Guide to Revenue Recognition](https://www.hubifi.com/blog/salesforce-revenue-recognition-guide)
[5] [RevOps.io - Revenue Recognition 101: A Guide for Revenue Operations](https://www.revops.io/blog/revenue-recognition-101-a-guide-for-revenue-operations)
[6] [Clari - Long-Term Revenue Goals: Establishing a Quarterly Operating Cadence](https://www.clari.com/blog/long-term-revenue-goals-establishing-a-quarterly-operating-cadence/)
[7] [The SaaS CFO - The SaaS Bookings Report](https://www.thesaascfo.com/the-saas-bookings-report/)
[8] [Maxio - The Ultimate Guide to SaaS Revenue Recognition and ASC 606](https://www.maxio.com/blog/saas-revenue-recognition-asc-606)
