# Growth Model -- Implementation

> The end-to-end process for delivering Growth Model projects. Follows the 4-phase framework: Strategy, Engineering, Enablement, Handoff.

## Project One-Pager

> Quick reference for architects. Scan in 2 minutes to understand the project type, flow, and tools.

### Growth Model One-Pager

#### Project Type

- Category: Strategic
- Primary Deliverable: Integrated Growth Model (YAML + micro app + PDF export)

##### Phase Relevance

| Phase          | Applies?  | Weight | Notes                                                        |
| -------------- | --------- | ------ | ------------------------------------------------------------ |
| 1. Strategy    | Yes       | Heavy  | 7 meetings, ~70% of project hours. The model IS the strategy |
| 2. Engineering | Optional  | Light  | Vasco dashboard config -- only if customer wants tracking    |
| 3. Enablement  | Yes       | Medium | Role-based training for 5 stakeholder groups                 |
| 4. Handoff     | Yes       | Medium | Maintenance schedule + retention path                        |

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────▶│ 2. ENGINEER  │────▶│3. ENABLEMENT │────▶│  4. HANDOFF  │
  │    Heavy     │     │   Optional   │     │    Medium    │     │    Medium    │
  │ 1a→1b→1c→1d │     │ 2a→2b→2c→2d │     │ 3a→3b→3c→3d │     │ 4a→4b→4c→4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   7 meetings           Vasco config         5 training groups    Maintenance +
   ~70% of hours        (skip if no)         30-day hypercare     retention path
```

**This project's flow:**
- Full 4-phase for customers who want Vasco operational tracking
- Strategy-only exit available after Phase 1 -- the Growth Model itself IS the deliverable
- Phase 2 is skipped entirely for strategy-only engagements
- ~15 hours with AI-first approach (down from 30-60 hours traditional)

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- Watch intro video explaining Growth Model and why it matters (5-10 min)
- Complete intake form with ARR, rep count, segments, growth targets, fiscal year
- Review Definition Alignment Document -- approve definitions for ARR, Booking, Churn, SQL, Conversion Rates
- Provide CRM access or export (Opportunities, Accounts, Contacts, Leads -- 12-24 months)

##### Track B: Architect Prep (Agent-Assisted)
- Process intake form through Growth Model Agent -- extract inputs, flag unknowns
- Pull CRM data -- opportunities, accounts, historical conversion by segment
- Run external research -- company context, industry benchmarks, competitor intel
- Build v0 model -- Growth Model Agent produces `growth-model-v0.yaml` with all inputs marked ASSUMED
- Generate micro app link -- shareable dashboard ready for kickoff
- Copy `input-bank.md` to customer working-documents folder

#### Refinement Loop (1b -&gt; 1c -&gt; 1d)

| Meeting                  | Sub-Phase | Focus                                                 | Stakeholder                | Output                        |
| ------------------------ | --------- | ----------------------------------------------------- | -------------------------- | ----------------------------- |
| Kickoff                  | 1b        | Present v0, validate assumptions, align on definitions | Exec Sponsor, RevOps       | Info for v1                   |
| Top-Down Review          | 1c        | Exit ARR, bookings, pipeline, SQLs, MQLs by segment   | Exec Sponsor, Finance      | v2                            |
| Sales Capacity           | 1c        | Rep roster, ramp, hiring timeline, attrition buffer    | Sales Leader               | v3                            |
| Marketing Pipeline       | 1c        | SQL targets by channel, budget allocation, timing      | Marketing Leader            | v4                            |
| CS Capacity              | 1c        | CSM capacity, 3-constraint model, hiring timeline      | CS Leader                  | v5                            |
| Finance / Unit Economics | 1c        | CAC:LTV, GTM costs, sensitivity, payment terms         | Finance (CFO/FP&A)         | v6                            |
| Final Review + Sign-Off  | 1d        | Full model walkthrough, each leader confirms targets   | All Stakeholders           | Final YAML -&gt; PDF deliverable |

**Reality check:** 7 topics matter, not strict sequence. Book whoever is available, cover their topic, iterate. Multiple sessions can happen same day. Timeline compresses with urgency.

#### Phase Checklists

##### Phase 1: Strategy
- 1a. Pre-Kickoff complete (Track A + Track B, v0 built)
- 1b. Kickoff call held (v0 presented, assumptions validated)
- 1c. Refinement loop complete (v0 -&gt; v6, all inputs CONFIRMED)
- 1d. Strategic sign-off obtained (all stakeholders, totals tie)

##### Phase 2: Engineering (Optional)
- 2a. Tech spec created -- Growth Model metrics mapped to Vasco config
- 2b. Engineering handoff meeting held
- 2c. Vasco build complete (dashboards, quota tracking, alerts)
- 2d. QA/Test + customer sign-off

##### Phase 3: Enablement
- 3a. Training materials prepped (video walkthrough scripts, written guides, FAQ)
- 3b. Training sessions delivered (5 stakeholder groups)
- 3c. Hypercare period complete (30 days)
- 3d. Enablement sign-off

##### Phase 4: Handoff
- 4a. Maintenance schedule documented and handed off
- 4b. Internal handoff complete
- 4c. External handoff (LeanScale -&gt; Customer) complete
- 4d. Project closed and archived

#### Document Types

##### Working Documents (iterate together)

| Document                     | Purpose                                         | When Complete                        |
| ---------------------------- | ----------------------------------------------- | ------------------------------------ |
| Intake Form                  | Pre-kickoff data collection from customer        | All fields filled, CRM access given  |
| Input Bank                   | Exhaustive list of ALL model inputs              | All inputs CONFIRMED or documented   |
| Definition Alignment Doc     | Stakeholder sign-off on ARR, Booking, Churn, SQL | All terms approved by Finance        |
| Assumptions Register         | Track data-backed vs strategic assumptions       | All assumptions categorized + owned  |

##### Deliverables (polished outputs)

| Deliverable                  | Created From                | Customer Uses For                               |
| ---------------------------- | --------------------------- | ----------------------------------------------- |
| Growth Model (YAML + PDF)    | Input Bank + Agent outputs  | Board presentations, planning, hiring decisions |
| Definitions Document         | Definition Alignment Doc    | Cross-functional source of truth                |
| Assumptions Register (final) | Working assumptions register| Ongoing monitoring and plan adjustment           |
| Micro App Dashboard          | YAML model                  | Interactive exploration, what-if scenarios        |

#### Enablement Details

##### Training Types

| Type             | Audience                           | Focus                                                    | Duration |
| ---------------- | ---------------------------------- | -------------------------------------------------------- | -------- |
| RevOps Manager   | RevOps lead                        | Full model walkthrough, monthly actuals entry, scenarios  | 60m      |
| Sales Leadership | CRO/VP Sales                       | Capacity model, quarterly projections, hiring triggers    | 45m      |
| Marketing        | CMO/VP Marketing                   | SQL targets, pipeline offset, budget-to-pipeline ratios   | 45m      |
| CS Leadership    | VP CS                              | Carry ratios, hiring triggers, net retention impact       | 30m      |
| Finance          | CFO/FP&A                           | Definitions, GTM costs, board reporting views             | 30m      |

##### Hypercare
- Applies: Yes
- Duration: 30 days
- Office Hours: One check-in call + async Q&A via email
- Scope: One model adjustment if material change occurs (e.g., hiring freeze, target change)

##### Training Assets to Create
- Video walkthrough: Full model walkthrough (RevOps audience)
- Video walkthrough: Executive summary and key metrics (Leadership audience)
- Video walkthrough: Maintenance schedule walkthrough (whoever owns maintenance)
- Doc: Monthly actuals entry guide
- Doc: Assumptions monitoring guide

#### Handoff & Retention

##### Internal Handoff
- Key context for Architect: Model structure, segment definitions, which assumptions are highest-risk, seasonal patterns
- Escalation trigger: Structural model changes (add segment, change sales cycle), annual recalibration

##### External Handoff (LeanScale -&gt; Customer)
- Final meeting agenda: Deliverables walkthrough, maintenance schedule review, recording of maintenance process
- Documentation package: Growth Model (YAML + PDF), Definitions Doc, Assumptions Register, all recordings, maintenance schedule

##### Maintenance Schedule
- Monthly: Actual vs Plan tracking, assumption pulse check, hiring status update
- Quarterly: Full assumption review, CSM capacity reforecast, channel efficiency analysis
- Annually: Full model recalibration, segment mix review
- Who owns: Single project = customer owns | Dedicated = Architect owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services -&gt; if no -&gt; Downsell: Another project (Attribution, Lead Scoring) -&gt; Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~1 quarter after handoff
- Internal prep trigger: 2 weeks before check-in
- Decision: Architect handles minor tweaks / structural changes scoped as new engagement

#### Definition Alignment Terms

| Term             | Typical Definition                                                                       |
| ---------------- | ---------------------------------------------------------------------------------------- |
| ARR              | Annualized recurring revenue. Excludes one-time fees, professional services, hardware    |
| Booking          | Contract value recognized at signature. Multi-year: total contract or first-year only?   |
| Churn            | Revenue lost from cancellations and downgrades. Distinguish logo churn vs revenue churn  |
| Net Retention    | (Starting ARR + Expansion - Contraction - Churn) / Starting ARR. Target: 100-120%       |
| SQL              | Sales Qualified Lead. Criteria: budget, authority, need, timeline confirmed              |
| Conversion Rate  | Stage-to-stage progression. Must agree on stage definitions before calculating           |
| Pipeline         | Total value of open opportunities at a given stage. Must agree on which stages count     |
| Sales Cycle      | Days from SQL creation to Closed-Won. Varies dramatically by segment                    |
| Quota            | Expected bookings per rep per year. Use expected (attainment-adjusted), not assigned     |
| Ramp Time        | Hire date to full productivity. Includes training + pipeline build + first close cycle   |

#### Common Gotchas
- Ramp time assumed too short -&gt; Hire produces less than modeled, capacity gap appears mid-year. Always validate: ramp &gt;= sales cycle length.
- Attrition not factored -&gt; Plan assumes zero turnover. Add 1 buffer hire per 3-4 planned hires (35% avg B2B sales attrition).
- Pipeline timing mismatch -&gt; Q1 bookings fed by Q1 pipeline creation. Pipeline must be built ONE SALES CYCLE before target bookings period.
- Seasonality assumed linear -&gt; 25/25/25/25 quarterly split when reality is 15/20/25/40. Pull historical quarterly patterns.
- Single efficiency ratio across channels -&gt; SDR produces $20 pipeline per $1, Content produces $40. Calculate per-channel.
- CSM capacity on one dimension only -&gt; Use both ARR carry AND logo carry. Binding constraint = whichever is higher.
- Dirty CRM data used as-is -&gt; First 1-2 meetings often spent on data quality. Filter out reseller/PO deals, validate stage definitions.
- Definitions not aligned before modeling -&gt; "Booking" means different things to Sales vs Finance. Force alignment FIRST via Definition Alignment Doc.
- Fiscal year mismatch -&gt; Customer's fiscal year starts May, model starts January. Confirm fiscal year in kickoff.
- New/expansion deals blended -&gt; Separate new business from expansion. Different conversion rates, different capacity owners.

#### Methodology Options

| Option      | When to Use                                                    | Complexity |
| ----------- | -------------------------------------------------------------- | ---------- |
| Top-Down    | Board has set firm targets; limited time (&lt;2 weeks)            | Low        |
| Bottom-Up   | Strong historical data; team buy-in critical                   | Medium     |
| W Method    | Need strategic + operational alignment; 4+ weeks available     | High       |

See the Methodology document for detailed Decision Frameworks guidance.

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on the complete Growth Model -- all inputs CONFIRMED, all functions aligned, totals tie top-down to bottom-up.
>
> **Output:** Signed-off Growth Model (YAML + micro app + PDF) + Definition Alignment Document + Assumptions Register.

### 1a. Pre-Kickoff

> Two parallel tracks run after the deal closes and before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                  | Format             |
| ----------------------------- | -------------------------------------------------------- | ------------------ |
| Intro video                   | Explain Growth Model: what it is, why it matters, what to expect | Video (5-10 min)    |
| Definition Alignment Document | Get stakeholder sign-off on ARR, Booking, Churn, SQL, Conversion Rate definitions | Google Doc         |
| Pre-filled intake form        | Confirm our assumptions: ARR, rep count, segments, growth targets, fiscal year, CRM type | Google Form or Doc |

**Why homework matters:** Customers cannot give intelligent input on conversion rates and capacity assumptions without understanding what a Growth Model is. The intro video educates them first. The Definition Alignment Doc forces internal alignment before we start building -- projects stall when Finance defines "Booking" differently than Sales.

**Completion tracking:** Follow up at day 3 if incomplete. Offer to fill intake form together on a call if customer is slow. Do not cancel kickoff if incomplete, but push hard.

#### Track B: Architect Prep

**What the Architect does (agent-assisted):**

| Step | Action                                                      | Output                                              |
| ---- | ----------------------------------------------------------- | --------------------------------------------------- |
| 1    | Process intake form through Growth Model Agent              | Extracted inputs with unknowns flagged              |
| 2    | Pull CRM data (opportunities, accounts, 12-24 months)      | Historical conversion rates, sales cycles, ACV data |
| 3    | Run external research (company, industry, competitors)      | Benchmarks and context for assumptions              |
| 4    | Build v0 model (agent takes intake + CRM + benchmarks)      | `growth-model-v0.yaml` -- all gaps marked ASSUMED   |
| 5    | Generate micro app link                                     | Shareable dashboard for kickoff presentation        |
| 6    | Copy input-bank.md to customer working-documents folder     | Tracking doc for ASSUMED vs CONFIRMED inputs        |

**The two-swarm pattern:**

| Swarm                | Source                                                | Goal                                          |
| -------------------- | ----------------------------------------------------- | --------------------------------------------- |
| **Swarm 1: Extract** | Intake form, CRM export, transcripts from sales calls | Make educated guesses, reduce customer burden |
| **Swarm 2: Enrich**  | Industry benchmarks, best practices, competitor data  | Anchor in what we have seen work              |

**Result:** v0 is 70% pre-filled. Customer reacts and corrects at kickoff -- they never create from scratch.

**Critical:** Mark EVERYTHING as ASSUMED until validated. The kickoff call is where ASSUMED becomes CONFIRMED.

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building anything.

| Term            | Our Definition                                                                           | Internally Approved? |
| --------------- | ---------------------------------------------------------------------------------------- | -------------------- |
| ARR             | Annualized recurring revenue excluding one-time fees, professional services, and hardware                   | Yes / No     |
| Booking         | Contract value at signature. Multi-year treatment: \{first year / total contract\}          | Yes / No     |
| Churn           | Revenue lost from cancellations + downgrades within \{fiscal year / trailing 12 months\}   | Yes / No     |
| Net Retention   | (Starting ARR + Expansion - Contraction - Churn) / Starting ARR                          | Yes / No     |
| SQL             | Lead with confirmed \{budget/authority/need/timeline\} handed to AE                        | Yes / No     |
| Conversion Rate | \{SQL-to-Closed-Won / Opp-to-Closed-Won\} measured from \{stage entry / SQL creation date\}  | Yes / No     |

**Instructions to customer:**

> Review each definition with your leadership team. Check "Yes" when approved. We cannot build the model until all terms are aligned -- different definitions produce different numbers, which causes rework.

---

### 1b. Kickoff Call

> **Purpose:** Present v0 and get alignment. We walk in with work done -- customer reacts, not creates from scratch.

#### Agenda (60-90 min)

| Time  | Topic                  | What Happens                                          |
| ----- | ---------------------- | ----------------------------------------------------- |
| 0-20  | Walk through v0        | Present model via micro app: "Here's what we built from your intake" |
| 20-35 | Validate assumptions   | ASSUMED -&gt; CONFIRMED or corrected                     |
| 35-50 | Definition alignment   | Review Definition Alignment Doc with Finance present  |
| 50-60 | Strategic context      | Board expectations, constraints, timeline, fiscal year |
| 60-75 | Identify gaps          | What data is missing, who owns it, homework assigned  |

**Discovery questions for kickoff:**

*Business Context:*
- What is your revenue target for next year and how was it set? (board mandate vs internal goal)
- What growth rate does this represent? Any strategic milestones? (fundraising, acquisition, IPO)

*Current State:*
- Current ARR and net retention rate?
- Quota-carrying reps today? Average attainment by segment?
- Marketing budget and channel allocation?
- CSM count and average book of business?

*Timing & Constraints:*
- Timeline for plan completion? Who approves the final plan?
- Any constraints? (hiring freeze, budget cap, territory restrictions)
- Fiscal year start month?

#### What We Bring

- v0 model (micro app link) built from intake + CRM + benchmarks
- Questions list (what we need to validate)
- Definition Alignment Document (pre-filled with our recommendations)

#### What We Leave With

- Feedback and corrections on v0 (info needed to create v1)
- Confirmed definitions (or clear blockers if stakeholder sign-off needed)
- Segment definitions confirmed (Enterprise, Mid-Market, SMB, International variants)
- Clear homework assignments (theirs: data requests; ours: v1 build)

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Iterate on the Growth Model until every input is CONFIRMED and totals tie top-down to bottom-up. Growth Model Agent processes each meeting's transcript to refine the YAML model.

#### The Pattern

```
Kickoff Call (gather info)
    |
Growth Model Agent + transcript -> v1
    |
Meeting 2: Top-Down (present v1, gather) -> Agent -> v2
    |
Meeting 3: Sales Capacity (present v2) -> Agent -> v3
    |
Meeting 4: Marketing (present v3) -> Agent -> v4
    |
Meeting 5: CS Capacity (present v4) -> Agent -> v5
    |
Meeting 6: Finance (present v5) -> Agent -> v6
    |
Meeting 7: Final Review -> Sign-off -> PDF Export
```

#### Before Each Meeting

1. Growth Model Agent processes previous meeting transcript + previous YAML
2. Agent produces next version YAML with updated ASSUMED/CONFIRMED status
3. Micro app refreshes with new data
4. Architect reviews agent output, prepares questions for next validation round

#### During Each Meeting

1. Walk through current version via micro app (shareable link, no login required)
2. Capture corrections and refinements -- agent handles simple tweaks (change NRR from 105% to 103%)
3. Validate what is now CONFIRMED
4. Identify remaining ASSUMED items
5. Assign homework for anything still missing

#### After Each Meeting

1. Run Growth Model Agent with transcript -&gt; next version YAML
2. Track what moved from ASSUMED -&gt; CONFIRMED in input-bank.md
3. Update working documents
4. Generate new micro app link if structural changes (add segment, change sales cycle)

#### The 7 Meeting Topics

**Meeting 2: Top-Down Review** -- Exec Sponsor + Finance

Present: Exit ARR target, required new bookings (Exit ARR - Starting ARR x NRR), pipeline requirements with sales cycle offset, SQL/MQL targets by quarter and segment. Validate quarterly weighting (seasonality), confirm segment-level starting and exit ARR.

**Meeting 3: Sales Capacity** -- Sales Leader

Present: Rep-by-rep capacity by quarter with ramp schedules. Capacity gap = Booking Target - Expected Bookings (total capacity x 0.85 attainment). Validate rep roster (filter out forecasted attrition vs actual departures), confirm ramp time by segment (Enterprise 6mo, Mid-Market 5mo, SMB 4mo), agree on attrition buffer (1 hire per 3-4 planned), review pipeline generation split across AE/SDR/Marketing/Channel.

**Meeting 4: Marketing Pipeline** -- Marketing Leader

Present: SQL targets by channel with timing offset (pipeline must be built one sales cycle before bookings period). Budget-to-pipeline ratios per channel (SDR 1:20, Content 1:40, Paid 1:20, Events 1:20, Partnerships 1:40). Validate channel scalability vs inventory constraints -- some channels scale linearly (SDR, Paid), others do not (Partnerships, Content). Confirm cost-per-SQL by channel.

**Meeting 5: CS Capacity** -- CS Leader

Present: CSM capacity using three constraints (ARR per CSM, logos per CSM, activations per CSM). Binding constraint = whichever requires more CSMs. Validate carry ratios by segment. Confirm CSM hiring timeline accounting for ramp. Review net retention assumptions -- split expansion vs contraction vs churn. If account management is separate from CS, model AM capacity for upsell/renewal.

**Meeting 6: Finance / Unit Economics** -- CFO/FP&A

Present: CAC:LTV by channel, GTM cost roll-up, efficiency metrics. Run sensitivity scenarios: what if conversion drops 10%? What if hiring is delayed one quarter? What if NRR drops 5%? Validate payment term assumptions (monthly vs annual vs multi-year -- impacts cash flow significantly). Confirm budget constraints. Review OTE data for unit economics (may need separate locked sheet for compensation sensitivity).

**Meeting 7: Final Review + Sign-Off** -- All Stakeholders

Full model walkthrough (30 min). Each leader confirms their section's targets (15 min). Address final questions (15 min). Sign-off and next steps (15 min). Generate PDF export from micro app.

#### Data Validation Loop

Expect 1-2 rounds of "clean the data" in early meetings. Common issues:

- "This conversion rate looks wrong" -&gt; Filter out reseller/PO deals that close same day
- "These termination dates are incorrect" -&gt; Forecasted attrition dates vs actual departures
- "Fiscal year starts in May, not January" -&gt; Shift all timelines
- "Win rate of 85% is unrealistic" -&gt; Definition issue: opp-to-close not SQL-to-close
- "We have 2,300 enterprise deals" -&gt; Blended new + expansion; separate them

**Pattern:** Agent builds from CRM -&gt; first meeting spots data issues -&gt; clean/filter -&gt; rebuild -&gt; second meeting validates. THEN the real strategic discussion happens.

#### Typical Timeline

| Milestone               | Typical Timing                             |
| ----------------------- | ------------------------------------------ |
| Pre-kickoff prep        | 1-2 days (intake + CRM pull + v0)          |
| Stakeholder sessions    | 1-3 weeks (multiple per week if available) |
| Data validation rounds  | Happens within stakeholder sessions        |
| Final review + sign-off | When all inputs CONFIRMED                  |

Timeline compresses with urgency (board meeting, fundraise, planning cycle). Do not assume "7 weeks for 7 meetings" -- if stakeholders are available, do the calls back-to-back.

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything before proceeding (or completing for strategy-only engagements).

#### Validation Checkpoint

- All 7 meetings complete (topics covered, not necessarily 7 separate calls)
- Model validated by Sales, Marketing, CS, and Finance
- Definition Alignment Document signed off by Finance
- Top-down = sum of bottom-up (totals tie across all segments)
- All critical inputs CONFIRMED (remaining ASSUMED items documented with rationale)
- Assumptions register complete with owners and monitoring cadences
- Customer has signed off on the complete Growth Model

#### Decision Point

- **Strategy-only complete** -&gt; Growth Model IS the deliverable. Skip Phase 2. Proceed to Phase 3 Enablement for training, then Phase 4 Handoff.
- **Proceed to Engineering** -&gt; Customer wants Vasco operational tracking dashboard. Continue to Phase 2.

---

## Phase 2: Engineering

> **Goal:** Load the Growth Model into Vasco for operational tracking and ongoing plan-vs-actual monitoring.
>
> **Output:** Configured Vasco instance matching the signed-off Growth Model, tested and customer-approved.

| Project Type          | Engineering Weight | Note                                      |
| --------------------- | ------------------ | ----------------------------------------- |
| Growth Model          | Light (10-20%)     | Mostly strategy. Vasco config only        |

### Sub-Phases

```
2a Tech Spec -> 2b Engineering Handoff -> 2c Build -> 2d Test
```

---

### 2a. Tech Spec (Agent-Assisted)

> **Purpose:** Translate the signed-off Growth Model into Vasco configuration specifications.

**Input:** Signed-off Growth Model YAML + PDF from Phase 1

**What happens:**

1. Map Growth Model metrics to Vasco dashboard structure
2. Define which metrics to track, alert thresholds, reporting cadence
3. Determine dashboard hierarchy: executive summary, segment views, department views

**Output:** Vasco configuration plan containing:

- Metric mapping (Growth Model metric -&gt; Vasco field)
- Dashboard structure (views by segment, by department, by quarter)
- Alert thresholds (green/yellow/red status triggers)
- Data source connections (CRM sync for actuals vs plan)
- Build sequence (what to configure first)

---

### 2b. Engineering Handoff

> **Purpose:** Review Vasco specs before building.

**Who attends:** Architect + Engineer (or Vasco admin)

**Agenda (30-45 min):**

| Time  | Topic              | What Happens                                        |
| ----- | ------------------ | --------------------------------------------------- |
| 0-15  | Walk through specs | Architect explains model context + Vasco config plan       |
| 15-30 | Engineer questions | Clarify data sources, CRM sync requirements         |
| 30-45 | Refine and approve | Adjust specs, confirm build approach and timeline   |

---

### 2c. Build (Configure Vasco)

> **Purpose:** Configure Vasco dashboards and tracking to match the Growth Model.

**What gets built:**

- Growth Model executive dashboard (ARR waterfall, bookings vs target)
- Quota tracking by rep (capacity vs actual by quarter)
- Pipeline vs target views (with timing offset visualization)
- Hiring tracker (planned vs actual hire dates, ramp status)
- Variance alerts (green/yellow/red thresholds for key metrics)
- Department views (Sales, Marketing, CS, Finance)

**The build loop:**

1. Pick next component from build sequence
2. Configure in Vasco
3. Verify data sync from CRM
4. Mark complete, note any issues
5. Repeat until all dashboards configured

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify the Vasco build works and get customer approval.

**Technical testing (our team):**

- All dashboards render correctly
- Data flows from CRM source systems
- Calculations match the spreadsheet/YAML model exactly
- Alerts trigger at defined thresholds
- Segment views filter correctly

**Customer testing:**

- Customer can navigate dashboards
- Numbers match their expectations from the model
- Views show what each stakeholder needs
- Customer can update actuals (if self-service)

**Engineering sign-off checkpoint:**

- Vasco system matches signed-off Growth Model
- All technical tests passing
- Customer has tested and approved
- Ready for enablement

---

## Phase 3: Enablement

> **Goal:** Customer team can actually use the Growth Model and (if applicable) Vasco dashboards. Each stakeholder knows their targets, how to monitor them, and when to escalate.
>
> **Output:** Trained team with documentation, stabilized system, no critical issues.

### Sub-Phases

```
3a Training Prep -> 3b Training Sessions -> 3c Hypercare -> 3d Enablement Sign-Off
```

---

### 3a. Training Prep (Agent-Assisted)

> **Purpose:** Create training materials from the Growth Model documentation and Vasco configuration.

**Input:** Signed-off Growth Model + Vasco dashboards (if applicable) + meeting transcripts

**What happens:**

1. Architect creates video walkthrough scripts tailored to each stakeholder role
2. Written guides drafted for recurring tasks (monthly actuals entry, quarterly review)
3. FAQ compiled from questions asked during the 7 meetings

**Output:** Training package containing:

- Video walkthrough scripts: Full model walkthrough (RevOps), executive summary (Leadership), maintenance process (whoever owns it)
- Written guides: Monthly actuals entry, assumption monitoring, when to escalate
- FAQ: Common questions from discovery meetings + anticipated questions by role

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to customer team by stakeholder role.

| Role             | Training Content                                                             | Duration |
| ---------------- | ---------------------------------------------------------------------------- | -------- |
| RevOps Manager   | Full model walkthrough: how tabs interconnect, monthly actuals entry, scenarios, Vasco navigation (if applicable) | 60 min   |
| Sales Leader     | Rep-by-rep capacity model, quarterly capacity vs target, when to accelerate/delay hiring, risk register | 45 min   |
| Marketing Leader | SQL targets by channel, pipeline-to-bookings offset logic, channel efficiency monitoring, budget-to-pipeline ratios | 45 min   |
| CS Leader        | CSM capacity calculations (ARR/logo/activation), bookings -&gt; CS hiring requirements, net retention impact | 30 min   |
| Finance          | Definitions repository, GTM cost flow to operating budget, board reporting views, validation checkpoints | 30 min   |

**Training delivery:**

1. Schedule sessions with appropriate stakeholders (can combine if convenient)
2. Deliver training (live preferred, recorded as backup)
3. Record each session for future reference
4. Answer questions, note gaps for FAQ updates

**Output:** Trained stakeholders, recordings, updated FAQ

---

### 3c. Hypercare

> **Purpose:** Intensive post-launch support to stabilize the Growth Model in practice.

**Duration:** 30 days

**What is included:**

- One scheduled check-in call (~30 min, 2-3 weeks after training)
- Async Q&A support via email
- One model adjustment if a material change occurs (e.g., hiring freeze announced, target revised by board, key departure)

**What is NOT included:**

- Structural model changes (adding segments, changing methodology) -- scope as new engagement
- Ongoing monthly actuals entry -- customer's responsibility after training
- Vasco configuration changes beyond what was built in Phase 2

**Output:** Stabilized model in use, no critical questions outstanding

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm customer can operate the Growth Model independently.

**Validation checkpoint:**

- All training sessions delivered (5 stakeholder groups)
- Training recordings and documentation provided
- Hypercare period complete (30 days)
- No critical issues outstanding
- Customer team can update actuals, monitor assumptions, and interpret outputs without daily support
- Ready for handoff

**Decision point:**

- **Proceed to Handoff** -&gt; Customer is enabled, project wrapping up
- **Extend Hypercare** -&gt; Still unstable, customer needs more support time

---

## Phase 4: Handoff

> **Goal:** Clean project close with maintenance plan established and retention/expansion path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the system, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule -> 4b Internal Handoff -> 4c External Handoff -> 4d Project Close
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At                                                  |
| ----------------------------- | -------------------- | -------------------------------------------------------------- |
| **Single Project**            | Customer owns        | 4c (External Handoff) -- customer receives schedule, runs it   |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) -- Architect receives schedule, runs it  |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention after the Growth Model project is complete. The most common failure mode post-project is not a broken model -- it is a model that becomes irrelevant because nobody updates it. This schedule prevents drift.

#### Monthly Tasks

| Monthly Task               | What to Check                                                                     | Red Flag Threshold                                     |
| -------------------------- | --------------------------------------------------------------------------------- | ------------------------------------------------------ |
| Actual vs Plan Tracking    | Compare actual bookings, SQLs, pipeline, headcount against model projections      | Any metric &gt;10% off plan for 2+ consecutive months     |
| Assumption Pulse Check     | Quick review of high-risk assumptions (conversion rates, sales cycles, ramp times)| Any assumption showing &gt;10% variance from modeled value|
| Hiring Status Update       | Update rep-by-rep model with actual hire dates, departures, ramp status changes   | Planned hire delayed &gt;1 month or unplanned departure   |

**How to execute:** Load actuals into Vasco (if configured) or update tracking spreadsheet. Flag green/yellow/red status. Share summary with relevant stakeholder.

#### Quarterly Tasks

| Quarterly Task                 | What to Review                                                              | Action if Off-Track                                         |
| ------------------------------ | --------------------------------------------------------------------------- | ----------------------------------------------------------- |
| Full Assumption Register Review| Walk through ALL documented assumptions, update confidence levels           | Mark invalid assumptions, adjust dependent model inputs     |
| CSM Capacity Reforecast        | Recalculate CSM needs based on actual ARR growth and new logo velocity      | Adjust hiring timeline if variance &gt;15%                     |
| Channel Efficiency Analysis    | Compare actual cost-per-SQL and budget-to-pipeline ratios by channel        | Reallocate budget from underperforming to overperforming    |
| Sales Cycle Validation         | Check if actual sales cycles match modeled assumptions by segment           | Adjust pipeline offset timing if cycles shifted &gt;30 days    |

#### After First Business Cycle (30-90 Days Post-Launch)

First major validation checkpoint -- this is when pipeline-to-bookings conversion can actually be measured against the model.

- **Pipeline-to-Bookings Validation:** Did pipeline created in Period 0 convert at the expected rate? If conversion differs by &gt;5 points, investigate root cause (volume, quality, timing, or rate issue).
- **New Hire Productivity Check:** Are new hires tracking to the modeled ramp curve? If not, adjust Year 1 productivity factor.
- **Key Question:** Are we on track for bookings targets? If gap exists, is it pipeline volume, conversion rate, rep capacity, or timing?

#### Refinement Triggers (When to Re-Engage)

| Trigger                          | Threshold                                  | Response                                                        |
| -------------------------------- | ------------------------------------------ | --------------------------------------------------------------- |
| Bookings variance                | &gt;20% above or below target for 2+ months   | Re-engage for model adjustment or scope refinement project      |
| Sales cycle shift                | Extending by &gt;30 days vs modeled           | Adjust all pipeline timing offsets, revalidate capacity needs   |
| New hire ramp                    | Taking &gt;1 quarter longer than modeled      | Revise ramp schedule assumptions, recalculate capacity          |
| Structural business change       | M&A, new product, new market, reorg        | Scope new Growth Model engagement                               |

#### Every 6-12 Months (Annual Recalibration)

- **Full Model Recalibration:** Update ALL conversion rates, sales cycles, and efficiency ratios with fresh 12-month historical data. This is a rebuild of assumptions, not just a tweak.
- **Segment Mix Review:** Has the segment mix shifted? Enterprise vs Mid-Market vs SMB proportions may have changed. May require segment-specific replanning or adding/removing segments.
- **Market Conditions Assessment:** External factors (economy, competitive landscape, new products, pricing changes) may require re-baselining core assumptions.

Key validation questions:
- Is the foundational logic still valid (conversion rates, sales cycles, efficiency ratios)?
- Have business priorities shifted (new product lines, new markets, M&A)?
- What assumptions from last year proved most wrong?

---

### 4b. Internal Handoff

> **Purpose:** Transfer context so Architect can manage ongoing relationship without involvement for routine matters.

**What the Architect needs to know:**

- Model structure: what was built, how segments work, which assumptions are highest-risk
- Customer context: stakeholders, their concerns, communication preferences, fiscal year
- Common requests and how to handle them (see escalation guidelines below)
- Maintenance schedule (if Dedicated engagement -- Architect runs this)

**Escalation guidelines:**

| Issue Type                                    | Who Handles     | Examples                                                |
| --------------------------------------------- | --------------- | ------------------------------------------------------- |
| Actual vs plan entry, simple number changes   | Architect       | "Update Q2 actuals," "Change NRR from 105% to 103%"    |
| Dashboard filter changes, user access         | Architect       | "Add new user to Vasco," "Change default segment view"  |
| Structural model changes, methodology shifts  | Specialist      | "Add new segment," "Change from Top-Down to W Method"   |
| Annual recalibration, segment additions        | Specialist      | "Full model refresh for next fiscal year"               |

**For Dedicated engagements:** Architect receives the maintenance schedule (4a) and becomes responsible for executing monthly/quarterly tasks. The specialist walks Architect through each maintenance task before handoff.

---

### 4c. External Handoff (LeanScale -&gt; Customer)

> **Purpose:** Formal project completion with customer.

**Final project meeting:**

- Review what was delivered (Growth Model, definitions, assumptions register)
- Walk through documentation package
- Walk through maintenance schedule in detail
- Record a video walkthrough of the maintenance process
- Confirm nothing outstanding
- Answer final questions
- Make it explicit: "Project complete"

**For Single Project engagements:** This is where maintenance ownership transfers. Walk the customer through each monthly/quarterly task. Make sure they understand what to check, how often, and when to call us back.

**Documentation package delivered:**

- Growth Model (YAML + PDF export)
- Micro App link (interactive dashboard)
- Definitions Document (final approved version)
- Assumptions Register (with owners and monitoring cadences)
- All training recordings
- Written guides (monthly actuals entry, assumption monitoring)
- FAQ document
- Maintenance Schedule
- Support contact info

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- All project artifacts saved to customer folder
- Handoff documentation complete
- Project status updated in tracking system
- Time/billing finalized

#### Internal Debrief (Optional but Recommended)

- What went well?
- What would we do differently?
- Any learnings to feed back into the playbook or agent?
- Data quality issues to flag for future similar customers?

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell -&gt; Downsell -&gt; Retry  |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (retainer)
   | if no
2. Downsell: Another one-time project (Attribution, Lead Scoring, CRM Optimization)
   | if yes
3. Retry retainer at end of next project cycle
```

**Script:**

> "Now that the Growth Model is complete, there are two ways we can continue working together. Option 1: We set you up on managed services where we handle the monthly/quarterly maintenance, run scenarios when things change, and keep the model current. Option 2: If there is another specific project -- like Attribution or Lead Scoring -- we can scope that out. Which sounds more interesting?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On \{date ~quarter out\}, we will review how the Growth Model is performing against actuals and see if any adjustments are needed."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                                  |
| ------------------- | ------------------------------------------------------------- |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks              |
| 2. Review metrics   | Pull actuals vs plan data from Vasco or tracking sheet        |
| 3. Decide ownership | Can Architect handle this check-in, or need specialist?       |
| 4. Prep materials   | If specialist needed, brief them. If Architect, prep talking points. |

**At the refinement check-in:**

- Review performance against original Growth Model
- Identify adjustments needed (assumption updates, hiring timeline changes)
- If minor: Architect handles tweaks
- If major: Scope new engagement (annual recalibration, segment expansion)

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

| Deliverable              | Contents                                                          | Format            |
| ------------------------ | ----------------------------------------------------------------- | ----------------- |
| Growth Model             | Integrated model: top-down targets, sales capacity, marketing plan, CS capacity, assumptions | YAML + PDF + Micro App |
| Definitions Document     | Approved definitions for ARR, Booking, Churn, SQL, Conversion Rates, Pipeline | Google Doc        |
| Assumptions Register     | All assumptions categorized (Product, GTM, Channel, External) with owners, confidence levels, monitoring cadence | Google Sheet      |

**Technical Deliverables (if Phase 2 applies):**

| Deliverable                  | Contents                                              | Format     |
| ---------------------------- | ----------------------------------------------------- | ---------- |
| Vasco Executive Dashboard    | ARR waterfall, bookings vs target, key metrics        | Vasco      |
| Quota Tracking Views         | Rep-by-rep capacity vs actual by quarter              | Vasco      |
| Pipeline vs Target Views     | Pipeline generation vs required, with timing offset   | Vasco      |
| Hiring Tracker               | Planned vs actual hire dates, ramp status             | Vasco      |
| Variance Alerts              | Green/yellow/red thresholds for key metrics           | Vasco      |

**Documentation Package:**

- Training recordings (per stakeholder role)
- Monthly actuals entry guide
- Assumption monitoring guide
- FAQ document
- Definition Alignment Document (final version)
- Maintenance Schedule

---

## Appendix

### What This Document Is

This is the implementation playbook -- the step-by-step execution guide an Architect follows to deliver a Growth Model project from first contact to project close. It is the third file in a 3-file playbook structure: Overview (what the project IS), Methodology (HOW the math works), and Implementation (WHAT to DO).

### What Each Phase Produces

| Phase                    | Output                                                                 | Gate Criteria                                                                  |
| ------------------------ | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **Phase 1: Strategy**    | Signed-off strategic package (Definition Alignment Doc + deliverables) | Customer stakeholders have approved definitions and strategic asset            |
| **Phase 2: Engineering** | Built and tested system                                                | System matches tech spec, all tests pass, customer has approved                |
| **Phase 3: Enablement**  | Trained team with documentation                                        | All training delivered, hypercare complete, team can operate independently     |
| **Phase 4: Handoff**     | Independent customer + archived project                                | Internal/external handoffs complete, maintenance plan in place, project closed |

### How to Adapt Per Project Type

Not every project weighs each phase equally. Before starting, determine the project's profile:

| Project Profile       | Strategy Weight | Engineering Weight | Enablement Weight | Example Projects               |
| --------------------- | --------------- | ------------------ | ----------------- | ------------------------------ |
| **Strategic-heavy**   | 60-80%          | 10-20%             | 10-20%            | Growth Model, GTM Strategy     |
| **Engineering-heavy** | 10-20%          | 60-80%             | 10-20%            | CRM Migration, Data Pipeline   |
| **Enablement-heavy**  | 20-30%          | 20-30%             | 40-50%            | Quote-to-Cash, Process Rollout |
| **Balanced**          | 30-40%          | 30-40%             | 20-30%            | Attribution, Lead Scoring      |

**Adaptation rules:**

- **Light phases** can compress sub-phases (e.g., a strategic-only project may skip Phase 2 entirely)
- **Heavy phases** expand with more sub-steps, more meetings, more agent runs
- **Phase 4 always applies** -- every project needs handoff, but the maintenance schedule complexity varies
