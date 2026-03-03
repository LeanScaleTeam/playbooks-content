# Customer Health Model — Implementation

## Project One-Pager

### Customer Health Model One-Pager

#### Project Type

- Category: Balanced
- Primary Deliverable: Multi-dimensional health scoring system with automated data collection, Red/Yellow/Green dashboards, and intervention playbooks for proactive churn prevention

##### Phase Relevance

| Phase          | Applies? | Weight | Notes                                                  |
| -------------- | -------- | ------ | ------------------------------------------------------ |
| 1. Strategy    | Yes      | Heavy  | Churn analysis, metric definition, scoring model design, 2-3 refinement loops |
| 2. Engineering | Yes      | Heavy  | Data integrations, CS platform configuration, dashboard builds |
| 3. Enablement  | Yes      | Med    | CSM team training, intervention playbook rollout       |
| 4. Handoff     | Yes      | Med    | Quarterly review cadence, model governance handoff     |

#### Phase Overview

```
  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
  │ 1. STRATEGY  │────>│ 2. ENGINEER  │────>│3. ENABLEMENT │────>│  4. HANDOFF  │
  │    Heavy     │     │    Heavy     │     │    Medium    │     │    Medium    │
  │ 1a>1b>1c>1d │     │ 2a>2b>2c>2d │     │ 3a>3b>3c>3d │     │ 4a>4b>4c>4d │
  └──────────────┘     └──────────────┘     └──────────────┘     └──────────────┘
   Churn analysis       Data integrations    CSM training         Governance &
   Metric design        Score config         Intervention         quarterly
   Weight calibration   Dashboard build      playbooks            review cadence
```

**This project's flow:**
- Full 4-phase. Heavy strategy (churn analysis, metric selection, weight calibration) and heavy engineering (data integrations, CS platform config, dashboards).
- Phase 1 and Phase 2 are tightly coupled — scoring model design directly translates to CS platform configuration.
- Some customers may compress Phase 1 if they already have churn analysis data and defined metrics.

#### Pre-Kickoff (1a)

##### Track A: Customer Homework
- [ ] Watch intro video on health scoring fundamentals (what it is, what it measures, why it matters)
- [ ] Complete intake form: current CS platform, data sources available, existing health/churn tracking
- [ ] Pull list of churned customers from past 12-24 months with reason codes (if available)
- [ ] Confirm admin access to CS platform, CRM, product analytics, and support system
- [ ] Review Definition Alignment Document and get stakeholder sign-off on key terms

##### Track B: Architect Prep
- [ ] Audit CRM for customer data completeness (account fields, activity history, renewal dates)
- [ ] Review available product analytics data (login frequency, feature adoption, usage trends)
- [ ] Analyze historical churn data if accessible — identify top 5 churn pattern signals
- [ ] Draft v0 health score framework: proposed dimensions, metrics, and weights
- [ ] Prepare kickoff presentation with benchmark data and recommended scoring approach

#### Refinement Loop (1b > 1c > 1d)

| Meeting      | Sub-Phase | Focus                                               | Stakeholder              | Output                           |
| ------------ | --------- | --------------------------------------------------- | ------------------------ | -------------------------------- |
| Kickoff      | 1b        | Present v0 scoring model, validate churn signals     | VP CS, CS Ops, RevOps    | Confirmed churn indicators       |
| Refinement 1 | 1c        | Review metric definitions, validate data sources     | CS Ops, Data/RevOps      | Approved metric list with sources|
| Refinement 2 | 1c        | Calibrate weights, set thresholds, segment rules     | VP CS, CS Managers       | Validated scoring model          |
| Sign-Off     | 1d        | Final model review, test against known churned accts | All stakeholders         | Approved scoring framework       |

#### Phase Checklists

##### Phase 1: Strategy
- [ ] 1a. Pre-Kickoff complete (Track A + Track B)
- [ ] 1b. Kickoff call held — churn signals validated
- [ ] 1c. Refinement loop complete (metric definitions, weights, thresholds finalized)
- [ ] 1d. Strategic sign-off on scoring model

##### Phase 2: Engineering
- [ ] 2a. Tech spec created (data integration map, score calculation logic, dashboard wireframes)
- [ ] 2b. Engineering handoff meeting held
- [ ] 2c. Build complete (integrations, score config, dashboards)
- [ ] 2d. QA/Test + customer sign-off (retroactive validation against churned accounts)

##### Phase 3: Enablement
- [ ] 3a. Training materials prepped (intervention playbooks, dashboard guides)
- [ ] 3b. Training sessions delivered to CS team
- [ ] 3c. Hypercare period complete (2-week pilot with subset of CSMs)
- [ ] 3d. Enablement sign-off

##### Phase 4: Handoff
- [ ] 4a. Maintenance schedule documented and handed off
- [ ] 4b. Internal handoff (SME > Architect) complete
- [ ] 4c. External handoff (delivery team > Customer) complete
- [ ] 4d. Project closed and archived

#### Document Types

##### Working Documents (iterate together)

| Document                       | Purpose                                      | When Complete                        |
| ------------------------------ | -------------------------------------------- | ------------------------------------ |
| Churn analysis spreadsheet     | Identify patterns in historical churn data   | Top 5-10 churn signals documented    |
| Metric definition table        | Define each health score metric with source  | All metrics approved by stakeholders |
| Weight calibration worksheet   | Test and refine metric weights               | Weights validated against history    |
| Threshold testing log          | Track accuracy of Red/Yellow/Green cutoffs   | False positive/negative rates &lt;30%   |

##### Deliverables (polished outputs)

| Deliverable                        | Created From                   | Customer Uses For                     |
| ---------------------------------- | ------------------------------ | ------------------------------------- |
| Health Score Model Documentation   | Metric definitions + weights   | Internal reference, new CSM onboarding|
| Intervention Playbook              | Threshold definitions          | Daily CSM workflow for at-risk accts  |
| Dashboard + Reporting Package      | Tech spec + platform config    | Executive visibility, CSM prioritization |

#### Enablement Details

##### Training Types

| Type       | Audience                             | Focus                                          | Duration |
| ---------- | ------------------------------------ | ---------------------------------------------- | -------- |
| Leadership | VP CS, CS Managers                   | Interpret health distribution, intervention SLAs| 30 min   |
| Technical  | CS Ops, RevOps                       | Maintain scoring model, adjust weights/thresholds| 60 min  |
| CSM Team   | All CSMs                             | Dashboard navigation, intervention playbooks    | 45 min   |

##### Hypercare
- Applies: Yes
- Duration: 2 weeks (pilot period with 2-3 CSMs, then full team)
- Office Hours: Yes — Weekly 30-min slot for first 4 weeks post-launch

##### Training Assets to Create
- [ ] Video walkthrough: Health score dashboard walkthrough and drill-down navigation
- [ ] Video walkthrough: How to interpret and act on Red/Yellow/Green accounts
- [ ] Doc: Health score metric definitions and weight rationale
- [ ] Doc: Intervention playbook (Red, Yellow, Green actions)
- [ ] Doc: Quick-reference card for daily CSM workflow

#### Handoff & Retention

##### Internal Handoff (SME > Architect)
- Key context for Architect: Scoring model rationale, segment-specific rules, which metrics are most volatile
- Escalation trigger: Any weight changes, new metric additions, threshold restructuring, or segment rule changes

##### External Handoff (Delivery Team > Customer)
- Final meeting agenda: Review model accuracy (false positive/negative rates), walk through maintenance schedule, confirm quarterly review cadence
- Documentation package: Model documentation, intervention playbooks, dashboard access, training video walkthroughs, maintenance schedule

##### Maintenance Schedule
- Monthly: Score accuracy spot-check, data source health verification
- Quarterly: Full model accuracy review, weight recalibration if needed
- Who owns: Single Project = customer CS Ops owns | Dedicated = Architect owns

##### Retention/Expansion Path

**If Single Project:**
Upsell: Managed Services (ongoing model optimization, quarterly recalibration) > if no > Downsell: Adjacent project (Customer Segmentation, Renewal Management) > Retry retainer

**If Multi-Project (Dedicated):**
- Refinement check-in scheduled: ~1 quarter post-launch
- Internal prep trigger: 2 weeks before
- Decision: Architect handles routine recalibration / SME needed for structural model changes

#### Key Assets

| Asset                              | When Used           |
| ---------------------------------- | ------------------- |
| Churn Analysis Template            | Phase 1a-1b         |
| Health Score Model Template        | Phase 1b-1d         |
| Intervention Playbook Template     | Phase 3a            |
| CS Platform Config Checklist       | Phase 2c            |

#### Definition Alignment Terms

| Term                    | Typical Definition                                                              |
| ----------------------- | ------------------------------------------------------------------------------- |
| Health Score            | Composite numeric score (0-100) measuring customer likelihood to renew/expand   |
| Churn                   | Customer cancellation or non-renewal of subscription                            |
| At-Risk (Red)           | Account scoring below threshold, requiring immediate intervention               |
| Needs Attention (Yellow)| Account scoring in mid-range, requiring proactive monitoring                    |
| Healthy (Green)         | Account scoring above threshold, candidate for expansion                        |
| CSM Sentiment Override  | Manual qualitative input from CSM that can adjust the automated score           |
| Lookback Window         | Time period over which a metric is calculated (e.g., trailing 30 or 90 days)   |
| Product Adoption        | Percentage of licensed features or seats actively used by the customer          |

#### Common Gotchas
- Starting with 15+ metrics instead of 5-7 > Start lean, add complexity after base model is validated [1]
- Using identical thresholds across Enterprise and SMB segments > Benchmark usage by segment size, set segment-specific thresholds
- Not testing model against known churned accounts before launch > Run retroactive validation in Phase 2d to catch model blind spots
- CSMs ignoring the score because it contradicts their intuition > Include CSM sentiment as an override dimension and involve CSMs in calibration
- Data integration breaks silently after launch > Set up data freshness alerts in the CS platform for every integration

#### Methodology Options

| Option                     | When to Use                                          | Complexity |
| -------------------------- | ---------------------------------------------------- | ---------- |
| Simple weighted average    | &lt;500 accounts, limited data sources, first model     | Low        |
| Segment-specific scoring   | Multiple segments with different usage patterns      | Medium     |
| ML-assisted scoring        | 1000+ accounts, 12+ months data, data science team   | High       |

> See Methodology for detailed scoring frameworks, weight calibration approaches, and benchmark ranges.

---

## Phase 1: Strategy

> **Goal:** Get stakeholder sign-off on the health scoring model — which metrics, what weights, what thresholds, and how segments are handled.
>
> **Output:** Approved Health Score Model (metrics, weights, thresholds, segment rules) + Definition Alignment Document signed off by stakeholders.

### 1a. Pre-Kickoff

> Two parallel tracks run before the kickoff call.

#### Track A: Customer Homework

**What we send:**

| Item                          | Purpose                                                  | Format             |
| ----------------------------- | -------------------------------------------------------- | ------------------ |
| Intro video                   | Explain what a health score is, how it prevents churn, why dimensions matter | Video (5-10 min)    |
| Definition Alignment Document | Get stakeholder sign-off on Health Score, Churn, At-Risk, Healthy definitions | Google Doc         |
| Pre-filled intake form        | Confirm CS platform, data sources, segments, current churn tracking | Google Form or Doc |
| Churn data request            | Historical churned accounts (12-24 months) with reason codes | Spreadsheet        |

**Completion tracking:** CS Ops or VP CS is the primary contact. Push hard on churn data — without it, the model lacks a validation baseline. Don't cancel kickoff if incomplete, but flag that model accuracy testing will be limited.

#### Track B: Architect Prep

**What the Architect does:**

| Step | Action                                                           | Output                                    |
| ---- | ---------------------------------------------------------------- | ----------------------------------------- |
| 1    | Gather inputs (intake form, CRM access, product analytics access)| Raw data collected                        |
| 2    | Analyze historical churn data — categorize reasons, find patterns| Churn signal inventory (5-10 signals)     |
| 3    | Draft health score dimensions and metrics                        | Proposed metric list with data sources    |
| 4    | Propose initial weights based on churn correlation analysis      | Draft weighted model                      |
| 5    | Create kickoff assets (scoring model overview, benchmark data)   | Presentation with ASSUMED labels          |

**Critical:** Mark all proposed metrics and weights as ASSUMED. The kickoff call validates. Industry benchmarks suggest starting with 5-7 high-impact metrics rather than 15+ [1]. Best-performing health score models use 8-10 metrics at most to maintain interpretability [2].

#### Stakeholder Alignment Document

> Get stakeholder sign-off on terms BEFORE building anything.

| Term                    | Our Definition                                                          | Internally Approved? |
| ----------------------- | ----------------------------------------------------------------------- | -------------------- |
| Health Score            | Composite 0-100 score combining product, engagement, support, and financial signals | [ ] Yes / [ ] No    |
| Churn                   | Non-renewal or cancellation of subscription (exclude downgrades unless specified) | [ ] Yes / [ ] No    |
| At-Risk (Red)           | Score 0-40: Immediate intervention required, escalation to management   | [ ] Yes / [ ] No    |
| Needs Attention (Yellow)| Score 41-70: Proactive monitoring with increased touchpoints            | [ ] Yes / [ ] No    |
| Healthy (Green)         | Score 71-100: Expansion candidate, standard engagement cadence          | [ ] Yes / [ ] No    |
| Product Adoption        | Percentage of licensed features/seats actively used in trailing 30 days | [ ] Yes / [ ] No    |
| CSM Sentiment Override  | Manual qualitative adjustment by CSM (can shift score up/down one tier) | [ ] Yes / [ ] No    |

**Instructions to customer:**

> Review each definition with your CS leadership team. Check "Yes" when approved. We cannot finalize the scoring model until all terms are aligned. Pay special attention to what constitutes "churn" vs. "downgrade" — this directly affects model training accuracy.

---

### 1b. Kickoff Call

> **Purpose:** Present v0 health scoring model and get alignment on which signals matter most. We walk in with work done — customer reacts, not creates from scratch.

#### Agenda (60-90 min)

| Time  | Topic                       | What Happens                                            |
| ----- | --------------------------- | ------------------------------------------------------- |
| 0-15  | Churn analysis findings     | "Here's what we found in your historical churn data"    |
| 15-30 | Walk through v0 model       | Present proposed dimensions, metrics, weights           |
| 30-45 | Validate signals            | ASSUMED metrics > CONFIRMED or replaced                 |
| 45-55 | Definition alignment        | Review Definition Alignment Doc, get sign-off on terms  |
| 55-65 | Data source validation      | Confirm which data sources are available and accessible |
| 65-75 | Segment discussion          | Identify if segment-specific scoring is needed          |
| 75-90 | Next steps                  | Schedule refinement meetings, assign data access tasks  |

#### What We Bring

- v0 health score model (dimensions, metrics, proposed weights — all marked ASSUMED)
- Churn analysis findings (patterns, signal inventory)
- Industry benchmarks for similar B2B SaaS companies
- Definition Alignment Document (pre-filled with our recommendations)
- Questions list (data availability, segment structure, CS team workflow)

#### What We Leave With

- Confirmed churn signals that resonate with CS leadership
- Feedback on proposed metrics — which to keep, drop, or add
- Data source access confirmations or blockers identified
- Definition Alignment status (approved or needs internal circulation)
- Refinement meeting schedule and homework assignments

---

### 1c. Alignment Loop & Strategic Meeting Cadence

> **Purpose:** Iterate on the health scoring model until sign-off. Refine metrics, weights, and thresholds through stakeholder validation.

#### The Pattern

```
Kickoff Call (validate churn signals, confirm metrics)
    |
    v
Refinement 1: Metric definitions + data source validation
    |
    v
Refinement 2: Weight calibration + threshold testing
    |
    v
Final Review: Full model validation against historical data > Sign-off
```

#### Before Each Meeting

1. Process previous meeting feedback
2. Update scoring model (v[n-1] > v[n])
3. Run retroactive tests if new data available
4. Prepare questions for next validation round

#### During Each Meeting

1. Walk through current model version
2. Capture corrections and refinements
3. Validate what's now CONFIRMED
4. Test specific scenarios ("Would account X have been flagged Red 60 days before churn?")

#### After Each Meeting

1. Update scoring model with new CONFIRMED items
2. Run retroactive accuracy tests where possible
3. Update working documents

#### Meeting Schedule

| Meeting Type         | Focus                                          | Stakeholder               |
| -------------------- | ---------------------------------------------- | ------------------------- |
| Metric Validation    | Finalize metric definitions, confirm data sources | CS Ops, RevOps, Data team |
| Weight Calibration   | Test weights against historical data, set thresholds | VP CS, CS Managers       |
| Segment Review       | Adjust scoring rules per customer segment      | VP CS, CS Ops             |
| Final Review         | Full model walkthrough, retroactive test results| All stakeholders          |

#### Typical Timeline

| Milestone               | Timing                                          |
| ----------------------- | ----------------------------------------------- |
| Pre-kickoff prep        | 3-5 days (churn analysis is time-intensive)     |
| Kickoff call            | Day 1 of engagement                             |
| Meeting loop            | 2-3 weeks (depends on data availability)        |
| Final review + sign-off | When all metrics CONFIRMED and model tested     |

---

### 1d. Strategic Sign-Off

> **Purpose:** Confirm we have everything before building the system.

#### Validation Checkpoint

- [ ] Definition Alignment Document signed off by stakeholders
- [ ] All health score metrics defined with data sources confirmed
- [ ] Metric weights assigned and validated against historical churn data
- [ ] Red/Yellow/Green thresholds set and tested retroactively
- [ ] Segment-specific rules documented (if applicable)
- [ ] CSM sentiment override rules defined
- [ ] Customer understands what we're building and how scores will be used
- [ ] No data access blockers for engineering

#### Decision Point

- **Proceed to Engineering** > Customer wants system built in CS platform with dashboards
- **Model-only deliverable** > Customer wants the scoring model documentation only (rare for this project — most proceed to build)

---

## Phase 2: Engineering

> **Goal:** Build and test the health scoring system in the customer's CS platform based on the approved model.
>
> **Output:** Configured health score with automated data collection, dashboards, and alerts — tested and customer-approved.

| Project Type    | Engineering Weight | Notes                                                    |
| --------------- | ------------------ | -------------------------------------------------------- |
| Customer Health Model | Heavy (40-50%) | Multiple data integrations, platform configuration, dashboards |

### Sub-Phases

```
2a Tech Spec > 2b Engineering Handoff > 2c Build > 2d Test
```

---

### 2a. Tech Spec

> **Purpose:** Translate the approved scoring model into technical specifications for CS platform configuration.

**Input:** Signed-off health score model (metrics, weights, thresholds, segment rules)

**Output:** Draft tech spec containing:

- Data integration map: which systems connect, via what method (native, API, CSV), sync frequency
- Score calculation logic: formula per metric, weight application, composite score calculation
- Segment rules: how accounts are categorized, different scoring variations per segment
- Dashboard wireframes: executive view, CSM view, account drill-down, trend views
- Alert configuration: threshold crossing triggers, notification targets
- Refresh frequency: daily score recalculation (recommended)

**Platform-specific considerations:**

| Platform    | Integration Method        | Health Score Feature         | Notes                          |
| ----------- | ------------------------- | ---------------------------- | ------------------------------ |
| Gainsight   | Native + S3 connector     | Scorecards with measures     | Most feature-rich, complex setup |
| ChurnZero   | Native integrations       | Custom health scores         | 100% customizable, unlimited scores [2] |
| Vitally     | Native + API              | Health indicators            | Good for SMB/mid-market        |
| Totango     | Native integrations       | SuccessBlocs with scoring    | Template-based approach        |
| Catalyst    | Native + API              | Health scores                | CRM-native feel                |

---

### 2b. Engineering Handoff

> **Purpose:** Review tech specs with engineer before building.

**Who attends:** Architect + Engineer (or CS Ops admin who will configure)

**Agenda (30-45 min):**

| Time  | Topic              | What Happens                                           |
| ----- | ------------------ | ------------------------------------------------------ |
| 0-15  | Walk through specs | Architect explains scoring model context + tech spec   |
| 15-25 | Data integrations  | Review each integration: source, method, field mapping |
| 25-35 | Build sequence     | Prioritize: integrations first, then scores, then dashboards |
| 35-45 | Risk review        | Flag: data quality issues, missing fields, API limits  |

**What Architect brings:**
- Strategic scoring model (for context)
- Draft tech spec (from 2a)
- Data source access credentials / confirmation
- Questions on data transformation or edge cases

**What engineer leaves with:**
- Approved tech spec
- Clear build sequence: (1) Integrations > (2) Score measures > (3) Score composition > (4) Dashboards > (5) Alerts
- Known risks/dependencies (e.g., product analytics API rate limits)

---

### 2c. Build (Configure)

> **Purpose:** Build the health scoring system in the customer's CS platform.

**Input:** Approved tech spec from 2b

**Build sequence:**

| Order | Component                     | What Gets Built                                        | Estimated Time |
| ----- | ----------------------------- | ------------------------------------------------------ | -------------- |
| 1     | Data integrations             | CRM sync, product analytics, support system, billing   | 2-4 hours      |
| 2     | Health score measures          | Individual metric calculations with lookback windows   | 2-3 hours      |
| 3     | Score composition             | Weighted composite score with segment variations       | 1-2 hours      |
| 4     | CSM sentiment field           | Manual override input mechanism for CSMs               | 30 min         |
| 5     | Dashboards                    | Executive summary, CSM book-of-business, account drill-down | 3-4 hours   |
| 6     | Alerts and CTAs               | Threshold crossing notifications, automated task creation | 1-2 hours    |

**Data integration details:**

| Source System      | Data Pulled                                      | Integration Method                 | Sync Frequency |
| ------------------ | ------------------------------------------------ | ---------------------------------- | -------------- |
| CRM (Salesforce/HubSpot)  | Account data, renewal dates, ARR, opportunity history | Native connector               | Real-time / hourly |
| Product Analytics  | Login frequency, feature adoption, active users  | API (Segment, Amplitude, Mixpanel) or direct | Daily          |
| Support System     | Ticket volume, escalations, resolution time      | Native (Zendesk, Intercom, Freshdesk) | Daily       |
| Billing System     | Payment timeliness, expansion history            | API or CSV import                  | Weekly         |

**Score measure configuration example:**

| Metric                | Dimension   | Weight | Lookback Window | Scoring Logic                                    |
| --------------------- | ----------- | ------ | --------------- | ------------------------------------------------ |
| Login frequency       | Product     | 15%    | Trailing 30d    | Daily=100, Weekly=70, Monthly=40, None=0         |
| Feature adoption      | Product     | 15%    | Trailing 90d    | % of licensed features used                      |
| License utilization   | Product     | 10%    | Trailing 30d    | Active users / purchased seats                   |
| QBR attendance        | Engagement  | 10%    | Trailing 180d   | Attended last QBR=100, Missed 1=50, Missed 2+=0  |
| Email response rate   | Engagement  | 8%     | Trailing 90d    | &lt;24h avg=100, 24-72h=60, >72h=20                |
| Exec sponsor engaged  | Engagement  | 7%     | Trailing 90d    | Active=100, Partially=50, None=0                 |
| Ticket volume trend   | Support     | 10%    | Trailing 30d vs 90d | Declining=100, Stable=70, Increasing=30       |
| Escalation frequency  | Support     | 5%     | Trailing 90d    | None=100, 1=60, 2+=20                           |
| Payment timeliness    | Financial   | 10%    | Trailing 180d   | On-time=100, &lt;30d late=50, >30d late=10         |
| CSM sentiment         | Qualitative | 10%    | Current         | Green=100, Yellow=50, Red=0                     |

**Build tracking:**

- [ ] Component 1: Data integrations (CRM, product, support, billing)
- [ ] Component 2: Health score measures (individual metric calculations)
- [ ] Component 3: Composite score with weights
- [ ] Component 4: Segment-specific scoring rules (if applicable)
- [ ] Component 5: CSM sentiment override field
- [ ] Component 6: Executive dashboard
- [ ] Component 7: CSM book-of-business dashboard
- [ ] Component 8: Account-level drill-down view
- [ ] Component 9: Health score trend charts
- [ ] Component 10: Threshold crossing alerts and CTAs

---

### 2d. QA / Test + Sign-Off

> **Purpose:** Verify the health score system works correctly and get customer approval.

**Two types of testing:**

| Type                       | Who      | Purpose                                                    |
| -------------------------- | -------- | ---------------------------------------------------------- |
| Retroactive Validation     | Our team | Run scores against historical churned accounts — did Red flag them? |
| Live Data Verification     | Our team | Confirm data flows, calculations are correct, dashboards render |
| Customer Validation        | Customer + CSMs | Validate scores match CSM intuition for known accounts |

**Retroactive validation checklist:**

- [ ] Run health scores retroactively for accounts that churned 6+ months ago
- [ ] Calculate false positive rate: % of Green accounts that actually churned
- [ ] Calculate false negative rate: % of Red accounts that actually renewed/expanded
- [ ] Target: Combined accuracy >70% (best models achieve 75-82% accuracy at 90-180 day prediction horizon [3])
- [ ] If accuracy &lt;70%, adjust thresholds or weights and retest
- [ ] Document accuracy baseline for future comparison

**Live data verification checklist:**

- [ ] All data integrations syncing at specified frequency
- [ ] Score calculations producing expected ranges (no all-0s or all-100s)
- [ ] Segment rules applying correctly
- [ ] Dashboards rendering with correct data
- [ ] Drill-down to metric-level detail working
- [ ] Alerts firing when accounts cross thresholds
- [ ] CSM sentiment override functioning correctly

**Customer validation:**

- Walk through top 10 and bottom 10 accounts by health score with 2-3 CSMs
- CSMs confirm: "Does this match what I know about this account?"
- Capture any accounts where score significantly mismatches CSM knowledge
- Identify missing signals or metrics that should be added in v2

**Engineering sign-off checkpoint:**

- [ ] Health scores calculating correctly for all accounts
- [ ] Model accuracy validated against historical data (baseline documented)
- [ ] All dashboards built and tested
- [ ] Alerts configured and tested
- [ ] Customer has tested with real accounts and approved
- [ ] Ready for enablement

**Decision point:**

- **Proceed to Enablement** > System is built, CSM team needs training on using scores
- **Loop back to Build** > Accuracy too low, data integration issues, or significant model changes needed

---

## Phase 3: Enablement

> **Goal:** CS team can use health scores in their daily workflow and respond appropriately to Red/Yellow/Green accounts.
>
> **Output:** Trained CS team with intervention playbooks, stabilized system, adoption metrics baseline.

### Sub-Phases

```
3a Training Prep > 3b Training Sessions > 3c Hypercare > 3d Enablement Sign-Off
```

---

### 3a. Training Prep

> **Purpose:** Create training materials and intervention playbooks from scoring model documentation.

**Input:** Scoring model documentation + tech specs + configured system

**Output:** Training package containing:

- **Intervention Playbooks:** Step-by-step response protocols for each health category
- **Dashboard Navigation Guide:** How to find your accounts, interpret scores, drill down
- **FAQ Draft:** Based on common CSM questions from similar implementations
- **Video Walkthrough Scripts:** What to record for asynchronous training

**Intervention playbook structure:**

| Health Category | Response SLA | Actions Required | Escalation Path |
| --------------- | ------------ | ---------------- | --------------- |
| Red (0-40)      | Within 24 hours | Schedule immediate check-in, review account history, create action plan, escalate to CS Manager | CS Manager > VP CS if no response in 48h |
| Yellow (41-70)  | Within 1 week | Increase touchpoint frequency, schedule proactive QBR, identify specific declining metrics | CS Manager if trending toward Red |
| Green (71-100)  | Standard cadence | Identify expansion opportunities, request referral/case study, monitor for sudden drops | No escalation needed |

---

### 3b. Training Sessions

> **Purpose:** Transfer knowledge to the CS team so they use health scores daily, not just during QBR prep.

**Training sessions by audience:**

| Session              | Audience              | Focus                                                      | Duration | Format     |
| -------------------- | --------------------- | ---------------------------------------------------------- | -------- | ---------- |
| CS Leadership        | VP CS, CS Managers    | Health distribution trends, intervention SLAs, reporting    | 30 min   | Live       |
| CS Ops / Admin       | CS Ops, RevOps admin  | Model maintenance, weight adjustments, threshold changes    | 60 min   | Live       |
| CSM Team             | All CSMs              | Dashboard navigation, intervention playbooks, score interpretation | 45 min | Live       |

**CSM Team training agenda (45 min):**

| Time  | Topic                              | Activity                                              |
| ----- | ---------------------------------- | ----------------------------------------------------- |
| 0-10  | What's in the score                | Walk through each metric, weight, and why it matters  |
| 10-20 | Dashboard navigation               | Live demo: find your accounts, sort by score, drill down |
| 20-30 | Intervention playbooks             | Review Red/Yellow/Green response protocols             |
| 30-40 | Practice scenarios                 | "This account is Red — what do you do?" (2-3 examples) |
| 40-45 | Q&A + CSM sentiment override       | How and when to use the manual override               |

**Training delivery:**

1. Schedule sessions with appropriate stakeholders
2. Deliver training (live, record for future reference)
3. Record video walkthrough of dashboard for async reference
4. Note all questions — feeds into FAQ and identifies model gaps

**Output:**

- Trained stakeholders who understand scores and response protocols
- Video walkthrough recordings for new CSM onboarding
- Questions log (feeds into FAQ and potentially v2 model refinements)

---

### 3c. Hypercare

> **Purpose:** Pilot period with subset of CSMs to validate score usefulness and build confidence before full rollout.

**Duration:** 2 weeks pilot + 2 weeks full-team support (4 weeks total)

**Week 1-2: Pilot (2-3 CSMs)**

- Select CSMs with mix of tenure and segment coverage
- Each CSM reviews their full book of business sorted by health score
- Daily async check-in: "Any scores that feel wrong? Any actions you took based on scores?"
- Track: number of score-driven actions taken, scores that contradicted intuition
- Gather feedback on missing signals or incorrect assessments

**Week 3-4: Full Team Rollout**

- Extend to all CSMs with pilot learnings incorporated
- Weekly office hours: 30-min slot for questions and feedback
- Track dashboard login frequency and score-based action metrics

**Bug triage and model adjustments:**

- Minor issues (data freshness, dashboard display): Fix within 24 hours
- Model issues (metric misbehaving, wrong weight): Document for next calibration cycle
- Critical (integration broken, scores all wrong): Fix immediately

**Output:** Stabilized system, pilot feedback incorporated, adoption baseline established

---

### 3d. Enablement Sign-Off

> **Purpose:** Confirm CS team can operate independently with the health scoring system.

**Validation checkpoint:**

- [ ] All training sessions delivered
- [ ] Training recordings and documentation provided
- [ ] Pilot period complete (2-3 CSMs validated score usefulness)
- [ ] Full team rollout complete
- [ ] No critical issues outstanding
- [ ] CSM team using health scores in weekly workflow (measured by dashboard views)
- [ ] Intervention playbooks being followed (measured by actions taken on Red accounts within SLA)
- [ ] Ready for handoff

**Decision point:**

- **Proceed to Handoff** > CS team is using scores, system is stable
- **Extend Hypercare** > Adoption too low, critical issues remain, model needs significant adjustment

---

## Phase 4: Handoff

> **Goal:** Clean project close with model governance plan established, maintenance schedule in place, and retention/expansion path set.
>
> **Output:** Maintenance schedule documented, internal context transferred, customer owns the system and knows how to keep it accurate, project archived, future revenue path established.

**Structure:**

```
4a Maintenance Schedule > 4b Internal Handoff > 4c External Handoff > 4d Project Close
                          (SME > Architect)      (Delivery > Customer) (Archive + Debrief)
```

**Maintenance ownership by engagement type:**

| Engagement Type               | Who Owns Maintenance | Handed Off At                                                                         |
| ----------------------------- | -------------------- | ------------------------------------------------------------------------------------- |
| **Single Project**            | Customer CS Ops owns | 4c (External Handoff) — customer receives maintenance schedule and runs it themselves |
| **Dedicated (Multi-Project)** | Architect owns       | 4b (Internal Handoff) — Architect receives maintenance schedule and runs it for customer |

---

### 4a. Maintenance Schedule

> **Purpose:** Document what needs ongoing attention to keep the health score model accurate and useful over time. Health score models that are not recalibrated become unreliable within 2-3 quarters as customer behavior and product features change [4].

#### Standard Maintenance Framework

**Monthly Tasks:**

| Monthly Task               | What to Check                                        | Red Flag Threshold                              |
| -------------------------- | ---------------------------------------------------- | ----------------------------------------------- |
| Data source health check   | All integrations syncing at expected frequency        | Any source >24h stale                           |
| Score distribution review  | Percentage of accounts in Red/Yellow/Green            | >50% in one category (model may be miscalibrated) |
| Intervention SLA audit     | CSM response time for Red accounts                   | >30% of Red accounts not contacted within SLA    |
| Dashboard usage check      | Number of CSM logins to health dashboard              | &lt;50% of CSMs logging in weekly                  |

**Quarterly Tasks:**

| Quarterly Task                | What to Review                                    | Action if Off-Track                                   |
| ----------------------------- | ------------------------------------------------- | ----------------------------------------------------- |
| Model accuracy assessment     | False positive and false negative rates            | If accuracy drops >10 points from baseline, recalibrate |
| Weight recalibration          | Do current weights still correlate with retention? | Run correlation analysis, adjust weights if needed    |
| Threshold review              | Are thresholds producing actionable distributions? | Adjust if too many accounts in one category           |
| New metric evaluation         | Any new data sources that should be added?         | Evaluate and pilot new metrics before adding          |
| CSM feedback collection       | Survey CSMs on score accuracy and usefulness       | If &lt;60% find scores useful, investigate root cause    |

**After First Business Cycle (60-90 days post-launch):**

- Run full accuracy analysis: How many churned accounts were flagged Red 60+ days before churn?
- Compare actual churn vs. predicted risk distribution
- Validate: Are CSMs taking different actions because of health scores?
- Key question: Has "surprise churn" (accounts that churn without prior Red flag) decreased?

**Refinement Triggers (when to re-engage):**

| Trigger                        | Threshold                                      | Response                                            |
| ------------------------------ | ---------------------------------------------- | --------------------------------------------------- |
| Model accuracy decline         | False positive/negative rate increases >10 pts | Schedule recalibration session with CS leadership    |
| New customer segment           | New product tier or market segment added        | Create segment-specific scoring rules                |
| CS platform migration          | Customer switches CS tool                       | Scope new implementation project                    |
| Major product change           | Significant feature addition or removal         | Review product usage metrics and thresholds          |
| CSM adoption decline           | Dashboard usage drops >30% month-over-month    | Investigate root cause, retrain if needed            |

**Every 6-12 Months:**

- Full model recalibration with fresh historical data
- Review all metric weights against actual renewal/churn correlation
- Assess whether scoring approach should evolve (e.g., from simple weighted average to ML-assisted)
- Evaluate expansion: should health scores feed into renewal forecasting?

---

### 4b. Internal Handoff (SME > Architect)

> **Purpose:** Transfer context so Architect can manage ongoing relationship.

**What the Architect needs to know:**

- What was built and why (scoring model rationale, metric choices, weight calibration decisions)
- Customer context (key stakeholders, CS team size, which CSMs were pilot participants)
- Common issues and how to resolve them (data sync delays, score distribution imbalances)
- When to escalate back to SME (structural model changes, new segment scoring rules)
- **Maintenance schedule** (if Dedicated engagement — Architect runs this)

**Escalation guidelines:**

| Issue Type                                    | Who Handles                                                 |
| --------------------------------------------- | ----------------------------------------------------------- |
| Data integration hiccups, dashboard tweaks    | Architect (routine maintenance)                             |
| CSM questions about score interpretation      | Architect (training reinforcement)                          |
| Weight recalibration, threshold adjustments   | Architect with SME guidance (quarterly calibration)         |
| New metric addition, segment rule changes     | SME (structural model changes)                              |
| Scoring methodology change (e.g., add ML)     | SME (new project scope)                                     |

**For Dedicated engagements:** Architect also receives the maintenance schedule (4a) and becomes responsible for executing it. SME walks Architect through each maintenance task, especially quarterly accuracy assessments and weight recalibration.

---

### 4c. External Handoff (Delivery Team > Customer)

> **Purpose:** Formal project completion with customer.

**Final project meeting:**

- Review what was delivered: health scoring model, configured system, dashboards, intervention playbooks
- Walk through accuracy metrics: baseline false positive/negative rates
- Present adoption metrics: CSM dashboard usage, intervention SLA compliance
- Walk through documentation package
- **For Single Project engagements:** Walk through maintenance schedule in detail, record video walkthrough
- Make it explicit: "Project complete — here's how you keep the model accurate"

**Documentation package:**

- Health Score Model Documentation (metrics, weights, thresholds, segment rules, rationale)
- Data Integration Reference (source systems, sync methods, field mappings)
- Intervention Playbook (Red/Yellow/Green response protocols with SLAs)
- Dashboard User Guide (navigation, filters, drill-down)
- Training video walkthrough recordings (CSM, leadership, admin)
- Definition Alignment Document (final version)
- FAQ document
- Maintenance Schedule (monthly, quarterly, annual tasks)
- Model accuracy baseline (for future comparison)

**Output:** Customer owns the system. Governance process established. Project formally complete.

---

### 4d. Project Close

> **Purpose:** Clean internal wrap-up + establish retention/expansion path.

#### Archive Checklist

- [ ] All project artifacts saved to proper location
- [ ] Handoff documentation complete
- [ ] Project status updated in tracking system
- [ ] Time/billing finalized
- [ ] Model accuracy baseline documented for internal reference

#### Internal Debrief (Optional but Recommended)

- What went well? (e.g., churn analysis findings, stakeholder engagement)
- What would we do differently? (e.g., data quality issues discovered late, metric gaps)
- Any learnings to feed back into SOPs? (e.g., new churn signals, better weight calibration approach)

#### Retention / Expansion

**Two paths based on engagement type:**

| Engagement Type               | Path                         |
| ----------------------------- | ---------------------------- |
| **Single Project**            | Upsell > Downsell > Retry    |
| **Multi-Project (Dedicated)** | Schedule Refinement Check-In |

**Single Project Path:**

```
1. Upsell: Managed Services (ongoing model optimization, quarterly recalibration, new metric development)
   | if no
   v
2. Downsell: Adjacent project (Customer Segmentation, Renewal Management, NPS/VoC Launch)
   | if yes
   v
3. Retry retainer at end of next project cycle
```

**Script:**

> "Now that the Customer Health Model is live, there are two ways we can continue working together. Option 1: We handle ongoing model optimization — quarterly recalibrations, new metric development as your product evolves, and accuracy monitoring. Option 2: If there's a specific adjacent project like renewal management or customer segmentation, we can scope that. Which sounds more relevant?"

**Multi-Project (Dedicated) Path:**

Schedule a refinement check-in at handoff:

> "On [date ~1 quarter post-launch], we'll review how the health scoring model is performing — accuracy trends, CSM adoption, and whether any recalibration is needed."

**Internal prep (2 weeks before check-in):**

| Step                | What Happens                                                 |
| ------------------- | ------------------------------------------------------------ |
| 1. Get pinged       | System reminder: refinement check-in in 2 weeks             |
| 2. Pull accuracy    | Run false positive/negative analysis, compare to baseline    |
| 3. Review adoption  | Dashboard usage trends, intervention SLA compliance          |
| 4. Decide ownership | Can Architect handle this check-in, or need SME?            |
| 5. Prep materials   | If SME needed, brief them. If Architect, prep talking points |

**At the refinement check-in:**

- Review model accuracy vs. baseline
- Review CSM adoption and score-driven action metrics
- Identify any metrics that need adjustment
- If minor: Architect handles weight tweaks and threshold adjustments
- If major: Scope new project (ML scoring upgrade, new segment model, expanded data sources)

**Output:** Project archived. Future revenue path established. Ready for next engagement.

---

## Deliverables & Assets Summary

**Strategic Deliverables:**

- Health Score Model Documentation (dimensions, metrics, weights, thresholds, segment rules with rationale)
- Churn Analysis Report (historical patterns, signal inventory, correlation findings)
- Definition Alignment Document (signed off by stakeholders)
- Intervention Playbooks (Red, Yellow, Green response protocols with SLAs)

**Technical Deliverables:**

- Configured health score in CS platform (measures, weights, segment rules, refresh frequency)
- Data integrations (CRM, product analytics, support system, billing)
- Dashboards (executive summary, CSM book-of-business, account drill-down, trend views)
- Alert configuration (threshold crossing notifications, automated CTAs)
- CSM sentiment override field

**Documentation Package:**

- Training video walkthrough recordings (CSM walkthrough, leadership overview, admin maintenance)
- Dashboard navigation guide
- Health score metric reference document
- Intervention playbook quick-reference card
- FAQ document
- Definition Alignment Document (final version)
- Maintenance Schedule (monthly, quarterly, annual tasks)
- Model accuracy baseline report

---

## Appendix

### Roles

| Role | What They Do |
|---|---|
| **Architect** | Owns the customer relationship, leads strategy, creates specs, does enablement, owns account post-delivery |
| **Engineer** | CS platform configuration, data integrations, dashboards (Phase 2) |
| **SME** | Health scoring methodology expertise, weight calibration, model design |

### Project Profile

This project is **Balanced** — roughly equal weight between strategy and engineering, with meaningful enablement:

| Phase           | Weight  | Why                                                           |
| --------------- | ------- | ------------------------------------------------------------- |
| Strategy        | 35-40%  | Churn analysis, metric selection, weight calibration, stakeholder alignment |
| Engineering     | 35-40%  | Multiple data integrations, CS platform config, dashboards    |
| Enablement      | 15-20%  | CSM training, intervention playbooks, pilot period            |
| Handoff         | 10%     | Maintenance schedule, governance transfer                     |

### Phase Guides

#### Phase 1: Strategy

The most common failure mode for health score projects is not a technical misconfiguration — it is choosing the wrong metrics or miscalibrating weights. Companies that start with 20+ metrics produce scores that are confusing and untrustworthy [1]. The strategy phase forces rigor: analyze actual churn data, validate signals with CS leadership, and test weights against historical outcomes before building anything.

**Key Principle: Data-Backed Signal Selection.** Do not ask CSMs "what do you think predicts churn?" and build from opinions alone. Start with historical churn analysis, identify correlating signals, then validate with CSM intuition. This produces a model grounded in evidence, refined by experience.

**Segment-Specific Scoring is Not Optional.** A 50% product usage rate might indicate a healthy Enterprise customer (power users who log in weekly for specific workflows) but a declining SMB customer (who should be using it daily). Set segment-specific thresholds from the start, or the model will produce misleading scores for at least one segment [1].

#### Phase 2: Engineering

**Data Integration Quality.** Health scores are only as good as the data feeding them. Silent integration failures are the most common post-launch issue — a product analytics sync breaks, login frequency drops to 0 for all accounts, and suddenly every account looks at-risk. Set up data freshness monitoring for every integration from day one.

**Build Order Matters.** Always build in this order: (1) Data integrations, (2) Individual score measures, (3) Composite score, (4) Dashboards, (5) Alerts. Each layer depends on the previous one. Testing each layer independently catches issues early.

#### Phase 3: Enablement

**CSM Adoption is the Make-or-Break.** A technically correct health score that CSMs ignore produces zero value. The enablement phase must address the "so what?" question for every CSM: "This account is Red — what exactly do I do, and how is this different from what I was already doing?" Intervention playbooks with specific actions and SLAs answer that question.

**The CSM Sentiment Override.** Including CSM sentiment as a scoring dimension (typically 10% weight) serves two purposes: (1) it captures qualitative signals that data cannot (e.g., champion departure, reorg, budget freeze), and (2) it gives CSMs ownership in the score, increasing trust and adoption.

#### Phase 4: Handoff

**Why Quarterly Model Reviews Are Non-Negotiable.** Customer behavior changes, product features evolve, and scoring models drift. Companies that implement health scores and never recalibrate report a steady decline in model accuracy — what was a strong churn predictor in Q1 may be irrelevant by Q4 [4]. The quarterly review cadence in the maintenance schedule prevents this decay.

**Expansion Opportunity: From Reactive to Predictive.** Once the base health model is stable (typically after 2-3 quarters of data), the natural expansion path is ML-assisted predictive scoring. With sufficient historical data (12+ months of health scores correlated with actual outcomes), machine learning models can achieve 75-82% prediction accuracy at 90-180 day horizons [3]. This is a natural upsell for managed services engagements.

### References

[1] [Vitally - How to Create a Customer Health Score with 4 Metrics](https://www.vitally.io/post/how-to-create-a-customer-health-score-with-four-metrics)

[2] [ChurnZero - The Customer Health Score Handbook](https://churnzero.com/guides/the-customer-health-score-handbook/)

[3] [Funnelstory - Predicting Churn & Retention in B2B SaaS](https://funnelstory.ai/blog/predicting-churn-retention-in-b2b-saas-101)

[4] [Gainsight - Customer Health Scores Explained](https://www.gainsight.com/blog/customer-health-scores/)
