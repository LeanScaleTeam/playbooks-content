# Sales Qualification Methodology — Methodology

This document covers the core concepts, frameworks, and calculations behind the Sales Qualification Methodology. It provides the methodological foundation — the "how it works" behind the execution steps.

---

## 1) Core Concepts

*The mental models, frameworks, and key distinctions that someone needs to understand before executing a Sales Qualification Methodology project.*

### Qualification vs. Discovery

*What is it?*

Qualification is the structured evaluation of whether an opportunity meets predefined criteria that indicate it can be won. Discovery is the broader process of understanding a prospect's situation, pain, and goals. Qualification is a subset of discovery -- the part where you determine deal viability, not just gather information.

*Why does it matter?*

Reps who conflate the two either skip qualification entirely ("I had a great discovery call, the deal is real") or turn qualification into an interrogation that damages rapport. 67% of lost sales opportunities stem from reps not properly qualifying leads before pursuit [1]. Separating these concepts lets teams build genuine discovery conversations that naturally surface qualification data.

*Key insight:*

> Qualification is not a checklist you fill out after a call. It is the judgment you make *during* a conversation based on what the prospect reveals through genuine discovery questions.

*Examples:*

| Context | Example |
|---------|---------|
| Discovery without qualification | Rep learns about the prospect's tech stack, team size, and growth plans but never determines if there is budget or a decision timeline. The deal stays in pipeline for 6 months. |
| Qualification without discovery | Rep asks "What's your budget? Who's the decision-maker? When do you need this?" in rapid succession. Prospect feels interrogated and goes dark. |
| Qualification embedded in discovery | Rep asks "Walk me through how you evaluated your last major vendor purchase" -- this surfaces decision process, authority, and timeline naturally. |

### The Three Levels of Qualification

*What is it?*

Effective qualification operates at three distinct levels, each answering a different question about whether to pursue a deal:

1. **Organization-level qualification**: Does this company fit our ICP? (firmographics, segment, tech stack)
2. **Opportunity-level qualification**: Is this a real, winnable deal? (budget, timeline, compelling event, competition)
3. **Stakeholder-level qualification**: Are we talking to the right people with the right access? (economic buyer, champion, decision criteria influence)

*Why does it matter?*

Most failed qualification implementations only address one level -- usually opportunity-level. A deal can look qualified at the opportunity level (budget exists, timeline is real) but fail at the stakeholder level (your champion has no influence, the economic buyer has different priorities). Addressing all three levels is what separates accurate forecasts from wish-list pipelines.

*The Framework:*

```
Organization Level     → "Should we be selling to this company at all?"
  ↓ (passes)
Opportunity Level      → "Is this deal real and winnable?"
  ↓ (passes)
Stakeholder Level      → "Are we positioned to win with the right people?"
  ↓ (passes)
QUALIFIED OPPORTUNITY  → Worth full pursuit resources
```

*Common misunderstandings:*

- **Misconception:** "If the company fits our ICP, it's a qualified opportunity."
  **Reality:** ICP fit is necessary but not sufficient. A perfect-fit company with no budget, no timeline, and no internal champion is not a qualified opportunity.

- **Misconception:** "Qualification happens once, at the beginning of the sales cycle."
  **Reality:** Qualification is continuous. A deal that was qualified in Stage 2 can become disqualified in Stage 4 if the champion leaves, the budget gets reallocated, or the decision criteria shift.

### Qualification as Conversation, Not Checklist

*What is it?*

The principle that qualification data must be gathered through natural sales conversations -- not by treating CRM fields as a data entry form to fill out after each call. When reps treat qualification as a checklist, they produce low-quality data ("Budget: TBD", "Timeline: Q4", "Decision Maker: VP") that adds no actual insight into deal viability.

*Why does it matter?*

This is the single most common reason qualification methodology implementations fail. Reps treat qualification fields as boxes to check rather than genuine discovery questions. The result is CRM data that looks complete (fields are filled) but is actually useless for forecasting or coaching.

*Key insight:*

> If a rep can fill out every qualification field without having an actual conversation with the prospect, the fields are wrong. Good qualification fields require genuine buyer engagement to answer.

*Examples:*

| Context | Example |
|---------|---------|
| Checklist behavior | Rep fills in "Budget: $100K" because the prospect mentioned they "have budget for tools this year." No validation of whether that budget is allocated, approved, or competitive. |
| Conversation behavior | Rep asks "Help me understand your budget process -- when you bought [similar tool], what did the approval process look like?" and learns the $100K is a department-level discretionary budget that does not require CFO approval if under $150K. |
| Coaching on the difference | Manager reviews an opportunity where "Decision Process" says "Committee review." Manager coaches: "Who is on the committee? When do they meet? What criteria are they using? If you can't answer those, we don't actually know the decision process." |

### Qualification Maturity Model

*What is it?*

A four-stage model that describes how organizations progress from ad-hoc qualification to data-driven deal management. Understanding where a client sits on this spectrum determines the right scope and approach for the project.

*Why does it matter?*

Implementing MEDDPICC for a team at Stage 1 maturity will fail -- they need to walk before they run. Conversely, implementing BANT for a team at Stage 3 will feel like a step backward. Matching methodology complexity to qualification maturity is the primary scoping decision.

*The Framework:*

| Stage | Name | Characteristics | Typical Win Rate |
|-------|------|-----------------|-----------------|
| Stage 1 | Ad Hoc | No formal qualification; reps use gut feel; no CRM fields for qualification | 10-15% |
| Stage 2 | Basic | Simple qualification criteria exist (often BANT-like); inconsistent adoption; managers don't coach on it | 15-22% |
| Stage 3 | Structured | Formal methodology selected; CRM fields configured; training delivered; coaching inconsistent | 22-30% |
| Stage 4 | Data-Driven | Qualification data actively used in forecasting; managers coach weekly on qualification quality; continuous refinement | 30-40%+ |

---

## 2) Decision Frameworks

*The matrices, decision trees, and "when to use what" guidance for selecting and customizing a sales qualification methodology.*

### Approach Selection Matrix

*The first thing to check when scoping a Sales Qualification Methodology project. Match methodology to sales motion complexity.*

| Situation | Recommended Methodology | Why |
|-----------|------------------------|-----|
| Transactional sales, &lt;$50K ACV, 1-2 decision makers, &lt;30 day cycle | BANT | Simple, low friction, fast qualification. Reps can apply it immediately without extensive training [2]. |
| Mid-market SaaS, $50K-$250K ACV, 3-5 stakeholders, 60-120 day cycle | MEDDIC | Addresses multi-stakeholder complexity without overloading reps. 73% of SaaS companies selling $100K+ use some version of MEDDIC [3]. |
| Enterprise sales, $250K+ ACV, 6+ stakeholders, 120+ day cycle, formal procurement | MEDDPICC | Adds Competition and Paper Process to handle RFPs, procurement teams, and competitive displacement. |
| Outcome-focused/consultative SaaS, recurring revenue models, $50K+ ACV | SPICED | Buyer-centric approach that maps well to recurring revenue models where demonstrating impact drives expansion [4]. |
| Hybrid: PLG with sales-assisted enterprise motion | BANT (self-serve) + MEDDIC (enterprise) | Different motions need different qualification depth. Don't force enterprise rigor on product-led conversions. |

### Scoping Factors

*Variables that affect which approach to use and how to customize it. For each factor, the decision points.*

**1. Sales Cycle Length**

- &lt;30 days → Lightweight framework (BANT or simplified custom). Full MEDDIC adds friction that slows a motion that should be fast.
- 30-90 days → Standard MEDDIC or SPICED. Enough cycle length to justify structured qualification without overwhelming reps.
- 90+ days → MEDDPICC or extended MEDDIC with additional procurement and competition tracking. Long cycles require more qualification checkpoints.

**2. Average Deal Size (ACV)**

- &lt;$50K → BANT or 3-4 custom criteria. The cost of qualification should not exceed the cost of losing a deal.
- $50K-$250K → 6-8 qualification criteria (MEDDIC range). Investment in qualification pays off with higher win rates on these deal sizes.
- $250K+ → Full MEDDPICC (8-10 criteria). The revenue impact of disqualifying one bad deal or winning one extra deal justifies the rigor.

**3. Number of Stakeholders in Typical Deal**

- 1-2 → Single "Authority" field is sufficient. Simple decision process.
- 3-5 → Need "Economic Buyer" + "Champion" distinction. Multi-threading becomes important.
- 6+ → Full stakeholder mapping required. Decision Criteria and Decision Process fields must track multiple perspectives.

**4. Current Qualification Maturity (see Core Concepts)**

- Stage 1 (Ad Hoc) → Start with BANT or 4-5 custom criteria. Focus on building the habit of qualifying at all.
- Stage 2 (Basic) → Graduate to MEDDIC or SPICED. Refine existing habits into a structured approach.
- Stage 3-4 (Structured/Data-Driven) → Optimize existing methodology. Focus on coaching quality, not framework change.

**5. CRM Platform**

- Salesforce → Full flexibility for custom fields, validation rules, dependent picklists, and automation. Can implement any methodology with scoring.
- HubSpot → Good field customization on Professional+. Scoring properties available. Some limitations on complex validation rules compared to Salesforce.
- Other CRMs → Assess custom field and validation capabilities before scoping. May need workarounds for field dependencies.

### BANT (Budget, Authority, Need, Timeline)

*Best for:*
- Transactional and velocity sales models
- SDR/BDR initial qualification before passing to AEs
- Companies with short sales cycles and low deal complexity
- Teams new to formal qualification (Stage 1 maturity)

*Not recommended for:*
- Enterprise sales with 6+ stakeholders and formal procurement
- Deals where budget is created (not allocated) -- asking "do you have budget?" kills deals where the value proposition creates the business case
- Consultative, outcome-focused selling motions

*Key differences from standard:*

| Aspect | BANT | MEDDIC/SPICED |
|--------|------|---------------|
| Budget approach | Binary: "Do they have budget?" | Nuanced: "What are the economic metrics that justify the investment?" |
| Authority model | Single decision maker | Economic buyer + champion + buying committee |
| Need assessment | Surface-level pain identification | Deep pain mapping with quantified business impact |
| Timeline | "When do you need this?" | "What is the compelling event driving urgency?" |
| Complexity handling | Low (4 criteria) | High (6-8+ criteria) |

### MEDDIC / MEDDPICC

*Best for:*
- Mid-market to enterprise B2B SaaS sales
- Multi-stakeholder deals with formal evaluation processes
- Companies that need to improve forecast accuracy (the correlation between MEDDIC scoring and win rates is well documented [5])
- Sales teams ready for structured methodology (Stage 2+ maturity)

*Not recommended for:*
- Transactional sales where the overhead exceeds the deal value
- Early-stage startups with &lt;5 reps and no formal sales process
- Teams without manager commitment to coach on it (73% of methodology implementations fail within 90 days without coaching reinforcement [6])

*MEDDIC Component Breakdown:*

| Component | Question It Answers | CRM Field Type | Example "Good" Answer |
|-----------|-------------------|----------------|----------------------|
| **M**etrics | What quantifiable outcomes does the buyer need? | Text/Number | "Reduce sales cycle from 90 to 60 days, saving $2M in annual carrying costs" |
| **E**conomic Buyer | Who has the budget authority and final say? | Lookup/Text | "CFO Sarah Chen, met her on call 3, she owns the $500K discretionary budget" |
| **D**ecision Criteria | What factors will they evaluate vendors on? | Multi-select/Text | "Integration with Salesforce (must-have), implementation timeline &lt;8 weeks, SOC 2 compliance" |
| **D**ecision Process | What steps and timeline to reach a decision? | Text/Picklist | "Technical eval (Week 1-2) > Business case to CFO (Week 3) > Legal/procurement (Week 4-5)" |
| **I**dentify Pain | What specific pain is driving this initiative? | Text | "Reps spend 3 hours/day on manual data entry, leading to 40% pipeline data being stale" |
| **C**hampion | Who is your internal advocate with power and influence? | Lookup/Text | "Director of RevOps, Jake Miller -- he initiated the RFP and is running the evaluation" |
| **C**ompetition (MEDDPICC) | Who else are they evaluating? | Picklist/Text | "Evaluating us vs. Competitor X and build-in-house option" |
| **P**aper Process (MEDDPICC) | What is the procurement/legal process? | Text/Picklist | "Standard MSA review (2 weeks), security questionnaire required, DPA for EU data" |

### SPICED (Situation, Pain, Impact, Critical Event, Decision)

*Best for:*
- Outcome-focused, consultative sales motions
- Recurring revenue SaaS where expansion and retention depend on demonstrated impact
- Teams transitioning from feature-selling to value-selling
- Organizations that want buyer-centric qualification (starts with buyer's situation, not seller's checklist)

*Not recommended for:*
- Highly transactional sales where speed is more important than depth
- Deals with simple, single-stakeholder decisions
- Teams that need heavy procurement process tracking (MEDDPICC handles this better)

*Key differences from standard:*

| Aspect | MEDDIC | SPICED |
|--------|--------|--------|
| Starting point | Metrics (what the seller wants to prove) | Situation (where the buyer is today) |
| Pain approach | "Identify Pain" (seller identifies) | "Pain" (buyer articulates) |
| Urgency driver | Implied in timeline/process | "Critical Event" (explicit forcing function) |
| Buyer-centricity | Moderate (seller-structured) | High (buyer-journey aligned) |
| Best ACV range | $100K-$500K+ enterprise deals | $50K-$250K consultative SaaS [4] |

---

## 3) Benchmarks & Standards

### How to Use Benchmarks

*Benchmarks are guidelines, not rules. Always:*
1. Start with benchmark as baseline
2. Adjust based on client-specific data (industry, deal size, team maturity)
3. Validate against their actual numbers when available (pull 90 days of CRM data)
4. Document deviations and rationale

### Win Rate Benchmarks by Qualification Maturity

| Metric | No Formal Qualification | Basic (BANT-level) | Structured (MEDDIC-level) | Data-Driven (Coached) | Notes |
|--------|------------------------|--------------------|--------------------------|-----------------------|-------|
| Overall Win Rate | 10-15% | 18-25% | 25-35% | 35-45% | Teams using MEDDIC see 20-30% higher win rates than unstructured approaches [5] |
| Forecast Accuracy (within 10%) | 20-30% | 35-45% | 50-65% | 70-85% | Only 20% of sales orgs achieve forecasts within 5% of actual [7] |
| Average Sales Cycle (relative) | Baseline | -5-10% | -15-25% | -25-35% | Branch reduced cycles 30% while doubling deal size after MEDDIC adoption [5] |
| Pipeline-to-Close Ratio | 5-6x | 4-5x | 3-4x | 2.5-3.5x | Tighter qualification means less pipeline needed per dollar of revenue |

**Source:** Aggregated from MEDDICC.com benchmarks, Korn Ferry 2025 Sales Effectiveness Study [8], and Xactly 2024 Forecasting Report [7].

**Interpretation:**
- **Below "No Formal Qualification" range:** Likely a data quality issue (not tracking wins/losses accurately) rather than a qualification issue.
- **Above "Data-Driven" range:** Either a niche market with limited competition, or the team has exceptional product-market fit. Validate that the numbers are real.

### Adoption Metrics Benchmarks

| Metric | First 30 Days | 60 Days | 90 Days | Sustained (6mo+) |
|--------|---------------|---------|---------|-------------------|
| Qualification Field Completion Rate | >60% | >75% | >85% | >90% |
| Reps Using Methodology Consistently | 40-50% | 60-70% | 75-85% | 85%+ |
| Manager Coaching on Qualification (weekly) | 50% of 1:1s | 70% of 1:1s | 80%+ of 1:1s | Embedded in pipeline reviews |
| Data Quality Score (fields with substantive answers vs. "TBD") | 30-40% | 50-60% | 65-75% | 80%+ |

**Interpretation:**
- **Field completion below 60% at 30 days:** Training did not land. Assess whether the issue is tool friction (too many fields), relevance (wrong fields for the motion), or commitment (managers not reinforcing).
- **Data quality below 50% at 60 days:** Reps are checking boxes, not qualifying. Shift coaching focus from "fill in the field" to "what does a good answer look like?"

### Quick Reference Thresholds

*For common "is this working?" questions during and after implementation:*

| Question | Good | Warning | Red Flag |
|----------|------|---------|----------|
| What % of opps have all required qualification fields filled? | >80% | 50-80% | &lt;50% |
| What % of Stage 3+ opps have Economic Buyer identified by name? | >70% | 40-70% | &lt;40% |
| Are managers reviewing qualification in pipeline meetings? | Weekly, with specific field review | Monthly or ad-hoc | Never or "we just look at amount and close date" |
| Win rate change after 90 days? | +10-15% improvement | Flat (no change) | Declining (reps gaming the system) |
| Forecast accuracy change after 90 days? | Within 10% of actual | Within 15-20% | Off by >20% |
| Average sales cycle change? | -10-20% reduction | Flat | Increasing (over-qualification slowing deals) |

---

## 4) Calculations & Scoring

### Formula Quick Reference

| Calculation | Formula | Example |
|-------------|---------|---------|
| Qualification Score | Sum of individual criterion scores (each 1-5) | 6 criteria x max 5 = 30 max, score of 22 = 73% qualified |
| Qualification Completion Rate | `(Fields filled / Total required fields) x 100` | 5 of 7 fields filled = 71% completion |
| Data Quality Score | `(Substantive answers / Total filled fields) x 100` | 4 substantive out of 5 filled = 80% quality |
| Weighted Pipeline Value | `Deal Amount x (Qualification Score / Max Score)` | $100K deal x (22/30) = $73.3K weighted value |
| Coaching Coverage | `(Reps receiving qual coaching / Total reps) x 100` | 8 of 10 reps coached this week = 80% |

### Qualification Scoring Rubric (MEDDIC Example)

**Formula:**
```
Qualification Score = M_score + E_score + D1_score + D2_score + I_score + C_score
```

Where each component is scored 1-5 based on evidence quality.

**Variables explained:**
- `M_score` = Metrics score: How well-defined are the buyer's success metrics?
- `E_score` = Economic Buyer score: How confirmed is access to the budget holder?
- `D1_score` = Decision Criteria score: How well do we understand evaluation factors?
- `D2_score` = Decision Process score: How mapped is the buying process and timeline?
- `I_score` = Identify Pain score: How validated and quantified is the business pain?
- `C_score` = Champion score: How strong and active is our internal advocate?

**Worked Example:**

*Scenario: Mid-market SaaS deal, $120K ACV, 90-day sales cycle, currently in Stage 3.*

```
Given:
- Metrics: Buyer wants to reduce sales cycle by 20% (partially quantified) = 3
- Economic Buyer: VP Sales identified, met on call 2, confirmed budget authority = 4
- Decision Criteria: Know 3 of 5 criteria, missing security requirements = 3
- Decision Process: Mapped to "eval > business case > legal" but no dates = 2
- Identify Pain: "Reps spend too much time on admin" (vague, not quantified) = 2
- Champion: Director of Ops, actively sharing info, but untested on influence = 3

Calculate:
- Total Score = 3 + 4 + 3 + 2 + 2 + 3 = 17 out of 30
- Percentage = 57%
- Tier = Tier 2 (Partially Qualified)
```

**Validation:**
- A Stage 3 deal at 57% qualification should trigger coaching intervention: the pain is vague and the decision process lacks dates. These are coachable gaps.
- If a deal is in Stage 4+ with &lt;60% qualification, it should not be in commit forecast.

### Scoring Rubrics

**Per-Criterion Scoring Rubric (1-5 Scale):**

| Score | Definition | CRM Indicator |
|-------|-----------|---------------|
| 1 - Unknown | No information gathered | Field empty or "TBD" |
| 2 - Assumed | Rep has a hypothesis but no buyer confirmation | Generic answer like "Q4" or "VP level" |
| 3 - Partially Confirmed | Some evidence from buyer, but gaps remain | Specific but incomplete: "VP Sales mentioned budget exists" |
| 4 - Confirmed | Direct buyer confirmation with specifics | Named person, specific amount, documented process |
| 5 - Validated | Confirmed by multiple sources or demonstrated through buyer action | Champion introduced you to EB, EB confirmed budget in writing |

**Tier Thresholds (for 6-criterion MEDDIC, 30-point max):**

- **Tier 1 (Fully Qualified):** 24+ points (80%+) -- pursue aggressively, include in commit forecast
- **Tier 2 (Partially Qualified):** 15-23 points (50-79%) -- continue pursuing, coach on gaps, include in best-case forecast
- **Tier 3 (Under-Qualified):** Below 15 points (&lt;50%) -- coach or disqualify, do not include in forecast

**Stage-Gate Requirements:**

| Sales Stage | Minimum Qualification Score | Required Criteria at Score 3+ |
|-------------|----------------------------|-------------------------------|
| Stage 1 (Discovery) | No minimum | None (still gathering) |
| Stage 2 (Scoping) | 10+ (33%) | Pain identified, at least partially |
| Stage 3 (Evaluation) | 15+ (50%) | Pain, Metrics, Decision Criteria |
| Stage 4 (Proposal) | 20+ (67%) | All criteria at 2+; EB and Champion at 3+ |
| Stage 5 (Negotiation) | 24+ (80%) | All criteria at 3+; Decision Process at 4+ |

---

## 5) Edge Cases & Deep Dives

### Edge Case 1: Methodology Too Complex for the Sales Motion

*Scenario:*

A client sells a $30K ACV SaaS product with a 21-day average sales cycle and 1-2 decision makers. They want to implement full MEDDIC. Implementing it would add friction that lengthens sales cycles and frustrates reps.

*Approach:*

1. Validate the intent: "You're right that structured qualification will improve your win rate. Let's choose the right level of structure for your motion."
2. Show the data: map their deal complexity (ACV, cycle, stakeholders) against the Approach Selection Matrix. BANT or a 4-criteria custom framework is the right fit.
3. Position the custom approach as "MEDDIC-inspired" if needed -- take the 2-3 most relevant MEDDIC components (e.g., Identify Pain + Champion) and combine with budget/timeline for a lightweight 4-criterion model.
4. Build in a growth path: "When your ACV grows past $80K and you start seeing 3+ stakeholders, we'll graduate to full MEDDIC."

*Key validation:*

If reps are filling out qualification fields in &lt;2 minutes per opportunity without frustration, the complexity level is right. If they are spending 10+ minutes or skipping fields, it is too complex.

### Edge Case 2: No Coaching Infrastructure (the "Launch and Leave" Risk)

*Scenario:*

Client wants to implement MEDDIC but has no formal 1:1 cadence between managers and reps, no structured pipeline review process, and managers are player-coaches who carry their own quota. The methodology will be trained but not reinforced.

*Challenge:*

73% of methodology implementations fail within 90 days when training is not reinforced with coaching [6]. Without coaching, reps revert to old habits within 3-4 weeks, CRM fields go empty, and the client concludes "MEDDIC doesn't work for us."

*Approach:*

1. **Make coaching infrastructure a prerequisite.** Before training reps, establish: weekly pipeline review cadence (30 min/team), manager 1:1 structure (15 min/rep/week with qualification focus), and a coaching question bank tied to each criterion.
2. **Train managers first.** Dedicate a separate session to managers on how to use qualification data in pipeline reviews and how to coach using the scoring rubric.
3. **Build accountability into the CRM.** Manager dashboards that show team qualification completion rates, data quality scores, and qualification-to-win-rate correlation.
4. **Set a 30-day checkpoint.** If field completion is below 60% at day 30, pause and diagnose. The issue is almost always manager reinforcement, not rep capability.

*Key validation:*

Track manager coaching activity alongside rep adoption metrics. If manager coaching coverage drops below 50%, adoption will decline within 2-3 weeks regardless of rep enthusiasm.

### Edge Case 3: Multi-Product or Multi-Segment Organization

*Scenario:*

Client sells three products at different ACVs ($15K, $75K, $300K) to different segments (SMB, Mid-Market, Enterprise). They want "one qualification methodology" for consistency.

*Approach:*

1. **Design a tiered qualification framework.** Use a common set of qualification categories (Pain, Budget, Authority, Timeline, Competition) but vary the depth required per segment:
   - SMB: 4 criteria, binary (yes/no), no scoring
   - Mid-Market: 6 criteria (MEDDIC), 1-5 scoring
   - Enterprise: 8 criteria (MEDDPICC), 1-5 scoring with stage gates
2. **Use a shared CRM field set with conditional visibility.** The Opportunity record has all 8 MEDDPICC fields, but layout rules show only the relevant subset based on the Segment picklist value.
3. **Create segment-specific training tracks.** One base module on "why qualification matters" (shared), then segment-specific modules on "how to qualify in your motion."
4. **Align reporting at the category level.** You can roll up "% of opps with Pain identified" across all segments for executive dashboards.

*Key validation:*

After implementation, check adoption rates by segment. If one segment has significantly lower adoption, the methodology is likely mismatched to that motion.

### Edge Case 4: Post-Acquisition or Merger -- Competing Methodologies

*Scenario:*

Two organizations have merged. Team A uses MEDDIC, Team B uses their own custom 5-criteria framework. Leadership wants to standardize but each team is attached to their methodology.

*Approach:*

1. **Map both methodologies to common categories.** Usually, 80% of the criteria overlap conceptually even if named differently.
2. **Build the unified framework from the best of both.** Take the strongest elements from each, validate with reps from both teams, and brand it as "new."
3. **Migrate in phases.** Phase 1: Unified CRM fields. Phase 2: Unified training on the merged framework. Phase 3: Unified coaching and reporting.
4. **Allow a 60-day transition.** Both old and new fields are visible. After 60 days, deprecate old fields.

*Key validation:*

Unified adoption above 70% within 90 days of the merged framework launch, with no measurable decline in win rates for either team during transition.

### Edge Case 5: PLG (Product-Led Growth) with Sales-Assist Hybrid

*Scenario:*

Client has a self-serve product with freemium users. When users hit certain usage thresholds or request enterprise features, they are routed to a sales team. The sales team needs to qualify which product-qualified leads (PQLs) are worth pursuing for enterprise conversion.

*Challenge:*

Traditional qualification frameworks assume the rep initiates the relationship. In PLG, the buyer is already using the product. The qualification question shifts from "should we pursue this?" to "is this user ready for an enterprise conversation?"

*Approach:*

1. **Replace traditional qualification criteria with PQL scoring.** Instead of BANT, score on: product usage depth, account size (seats/users), feature requests that indicate enterprise need (SSO, RBAC, audit logs), and firmographic fit.
2. **Use a two-stage qualification.** Stage 1 (automated): PQL score based on product telemetry + firmographics. Stage 2 (human): When PQL score crosses threshold, AE engages with a modified MEDDIC focused on Metrics, Economic Buyer, and Decision Process.
3. **Configure CRM to ingest product usage data.** Product telemetry flows into the CRM via integration (Segment, Hightouch, or native connector), populating the PQL score automatically.
4. **Training focus shifts.** Train reps on "how to interpret usage data and start enterprise conversations with existing users."

*Key validation:*

PQL-to-enterprise conversion rate should be 2-3x higher than cold outbound conversion rate. If it is not, the PQL scoring criteria need refinement.

---

## References

[1] [Landbase - 35 Lead Qualification Statistics for B2B Sales](https://www.landbase.com/blog/lead-qualification-statistics)
[2] [Demodesk - Sales Qualification Frameworks in 2024](https://demodesk.com/resources-guides/sales-qualification-frameworks-in-2024-how-to-choose-the-right-one-for-your-business)
[3] [MEDDICC - MEDDPICC Sales Methodology and Process](https://meddicc.com/meddpicc-sales-methodology-and-process)
[4] [Claap - BANT vs SPICED: Sales Framework Comparison 2025](https://www.claap.io/blog/bant-vs-spiced)
[5] [MEDDICC.com - MEDDIC Benchmark Data and Case Studies](https://meddicc.com/meddpicc-sales-methodology-and-process)
[6] [Saber - Sales Qualification Frameworks: BANT vs MEDDIC vs SPIN](https://www.saber.app/blog/sales-qualification-frameworks-comparison)
[7] [Xactly - 2024 Sales Forecasting Benchmark Report](https://www.xactlycorp.com/blog/forecasting/2024-sales-forecasting-benchmarks)
[8] [Korn Ferry - 2025 Supercharging Sales Effectiveness Study](https://www.kornferry.com)
[9] [Salesforce - State of Sales 2024](https://www.salesforce.com/resources/research-reports/state-of-sales/)
[10] [HubSpot - Sales Qualification Guide](https://blog.hubspot.com/sales/ultimate-guide-to-sales-qualification)
