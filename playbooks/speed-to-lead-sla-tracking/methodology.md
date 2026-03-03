# Speed to Lead SLA Tracking — Methodology

This document covers the conceptual foundation behind Speed to Lead and SLA Tracking -- the "why" and "how it works" behind the project. It explains core concepts, decision frameworks, benchmarks, calculations, and edge cases so you can validate outputs, answer client "why?" questions, and navigate tricky scenarios.

## 1) Core Concepts

### Speed to Lead vs SLA Tracking

*What is it?*

Speed to Lead and SLA Tracking are two separate but related concepts that are frequently confused. **Speed to Lead** measures the total elapsed time from a lead's engagement (form submission, CTA click, list upload) to the first sales follow-up touch. **SLA Tracking** measures only the human response time -- from when a lead is assigned to a rep to when that rep follows up -- against a set of business-defined rules.

They are combined into one project because the measurement infrastructure overlaps, but they answer different questions and hold different teams accountable.

*Why does it matter?*

Conflating the two creates unfair accountability. If systems take 30 minutes to route a lead and a rep responds within 5 minutes of assignment, the total speed-to-lead number looks terrible -- but the rep did their job. Separating the concepts lets you hold the right teams accountable: ops owns systems delay, sales owns human response time.

*Key insight:*

> "Speed to Lead is more about how long it takes from the lead's perspective... SLA tracking is basically a set of rules that the business has aligned on... It's not the human's fault if there's a bunch of tech debt in the system." -- LeanScale

*Common misunderstandings:*

- **Misconception:** Speed to lead and SLA tracking are the same thing.
  **Reality:** Speed to lead = total time (systems + human). SLA tracking = human response time only, measured against business rules. They are related, which is why they are combined into the same project, but they are two separate concepts.

- **Misconception:** The sales team is fully responsible for speed to lead.
  **Reality:** Speed to lead responsibility is split: the operations team owns systems delay, the sales team owns human delay. SLA tracking is the metric that is fully in the sales team's control.

- **Misconception:** You can fix speed to lead by telling reps to respond faster.
  **Reality:** If 30 of 45 minutes of delay are systems delay, coaching reps changes nothing. You need to fix the systems first.

*Examples:*

| Context | How the Distinction Applies |
|---------|---------------------------|
| 30+ min average speed to lead | Investigation revealed the majority was systems delay (workflow wait times, routing graph processing), not rep laziness. Fixing systems was the priority. |
| A rep misses their SLA on a hand-raiser lead | SLA tracking shows this is a human delay issue. The rep was alerted promptly but didn't follow up within the 30-minute window. Coaching conversation. |
| Speed to lead spikes after a platform update | This is a systems delay issue. The MAP had an outage or a new workflow introduced a hard-coded delay. No rep is at fault. |

### Systems Delay vs Human Delay

*What is it?*

Speed to lead breaks down into two measurable components:

1. **Systems delay:** Time from lead engagement (e.g., form submission) to lead being fully assigned to a sales rep and the rep being notified. This covers all automation: logging in the marketing automation platform, firing workflows, setting lifecycle status/stage, enrichment processing, routing logic, and final assignment.

2. **Human delay:** Time from when a lead is properly assigned and the rep is alerted to when the rep actually follows up with a first touch (call, email, etc.).

*Why does it matter?*

You cannot fix what you cannot measure separately. The MIT/InsideSales.com Lead Response Management Study found that leads contacted within 5 minutes are 100x more likely to be reached and 21x more likely to be qualified than leads contacted after 30 minutes [1][2]. But if your systems delay alone is 30 minutes, even the fastest rep in the world cannot hit a 5-minute total response time.

*The Framework:*

```
Total Speed to Lead = Systems Delay + Human Delay

Form Submission ──> [Systems Delay] ──> Rep Notified ──> [Human Delay] ──> First Touch

                     MAP processing                        Rep responds
                     Workflow firing                        Makes call/sends email
                     Enrichment                             Logs activity
                     Routing logic
                     Assignment
```

*Key insight:*

> "In a perfect world, you're actually able to separate out the system's delay speed from the human delay speed, and then you have an overall delay speed." -- LeanScale

Separating these two measurements is the core technical requirement of this project. Without the separation, you have a single number that nobody can act on because nobody knows who owns the problem.

### Three Project Components

*What is it?*

Speed to Lead (&amp; SLA Tracking) contains three optional components. Each can be included or excluded based on client needs:

| Component | What It Covers | Include When |
|-----------|---------------|-------------|
| 1. Systems Delay Mitigation | Investigating and reducing the time between lead engagement and rep notification | Significant systems delay is discovered (&gt;10 min average) |
| 2. SLA Tracking &amp; Alert System | Building the infrastructure to measure, track, and alert on rep follow-up times | Almost always -- this is the core deliverable |
| 3. Automated Meeting Scheduling | Allowing leads to self-book meetings with the right rep directly from forms or chat | Client wants to further reduce follow-up time; usually scoped as a separate project (50+ hours alone) |

*Why does it matter?*

Not every client needs all three. Component 2 (SLA tracking) is the baseline -- it is completed in nearly every engagement. Component 1 (systems delay) is included when investigation reveals a systems problem worth fixing. Component 3 (automated scheduling) is large enough to be its own dedicated project and is usually separated to avoid scope creep.

*Key insight:*

> "Component number two is really the only thing that is likely to be completed every single time." -- LeanScale

> "That project alone [automated meeting scheduling] typically takes 50 hours plus to implement. By itself. So at that point, it probably makes more sense to just have that be its own separate project." -- LeanScale

### SLA Hit vs SLA Miss

*What is it?*

SLA (Service Level Agreement) tracking uses business-defined rules for acceptable follow-up times by lead type. Each lead is measured against the threshold for its type. If a rep follows up at or before the threshold, the SLA is "hit." If not, the SLA is "missed." Performance is tracked as a hit/miss percentage over time.

*Why does it matter?*

It creates measurable accountability and a trend line. You can see whether follow-up discipline is improving or degrading across the team over weeks and months. Organizations with formal sales-marketing SLAs achieve 31% higher close rates and 24% faster revenue growth compared to those without clear agreements [3].

*Key insight:*

> "If you follow up at or earlier than the defined SLA time frame, the SLA is considered hit. If not, the SLA is considered missed. And that's just another way to report on performance here over time." -- LeanScale

*Examples:*

| Lead Type | SLA Rule | Scenario | Result |
|-----------|---------|----------|--------|
| Demo request (hand-raiser) | 30 minutes | Rep follows up in 22 minutes | SLA Hit |
| Demo request (hand-raiser) | 30 minutes | Rep follows up in 45 minutes | SLA Miss |
| Content download (non-hand-raiser) | 24 hours | Rep follows up in 18 hours | SLA Hit |
| Event attendee (non-hand-raiser) | 48 hours | Rep follows up in 3 days | SLA Miss |

### Hard-Coded Delays and Tech Debt

*What is it?*

Hard-coded delays are intentional time delays built into workflows or routing flows -- for example, a "wait 5 minutes" step in a MAP workflow or a delay node in a routing graph. They are typically added to prevent race conditions between systems (e.g., waiting for enrichment data to populate before routing triggers). While they solve one problem, they directly increase systems delay and accumulate as tech debt over time.

*Why does it matter?*

Hard-coded delays are the most common cause of high systems delay. In one engagement, the team discovered multiple 5-6 minute delays stacked across MAP workflows and the routing graph, resulting in a 30+ minute average systems delay. The alternative is to design systems using custom fields (like "latest attribution completed datetime") that act as completion triggers instead of arbitrary time delays.

*Key insight:*

> "Hard-coded delays within workflows, or lead routing flows, to solve a particular problem should be avoided at all costs... there's usually always a better way to go about it." -- LeanScale

> "We build a field called latest attribution completed datetime. That is a field that will never be used by anyone outside of the ops team. That is purely a field that is used for the ops team from a race condition perspective." -- LeanScale

*The pattern:*

| Anti-Pattern | Better Approach |
|-------------|----------------|
| "Wait 5 minutes" delay step in workflow to allow enrichment to complete | Create a "latest enrichment completed datetime" field. Trigger the next workflow step when this field is populated, not after an arbitrary wait. |
| "Wait 10 minutes" delay in routing graph to allow lifecycle stage to update | Create a "lifecycle stage updated datetime" field. Route based on field population, not time. |
| Multiple stacked delays across different systems | Map every delay, understand the race condition it solves, replace each with a field-based trigger |

### Lead Routing and Its Relationship to Speed

*What is it?*

Lead routing determines which rep gets assigned a lead. There are three primary approaches, and each has different speed characteristics:

| Routing Approach | Speed Characteristic | Accuracy Characteristic |
|-----------------|---------------------|------------------------|
| Round Robin | Fastest -- immediate assignment, no decision logic | Lowest -- no specialization matching |
| Territory-Based | Medium -- multiple decision nodes in routing hierarchy | High -- matches by geography, industry, product |
| Target Account | Variable -- fast for named accounts (direct lookup), medium for fallback leads | Highest for key accounts |

*Why does it matter?*

Routing is the upstream process that feeds into speed to lead. Every decision node in the routing hierarchy adds latency. A 5-node territory check takes longer than a 1-node round robin assignment. The choice of routing approach directly determines the lower bound of your systems delay.

*Key insight:*

The speed vs. accuracy tradeoff is central to scoping: round robin is fastest but least precise; territory-based is slower but more accurate. For most B2B SaaS companies, the right answer is accurate routing done as fast as possible -- not sacrificing accuracy for speed.

---

## 2) Decision Frameworks

### Approach Selection Matrix

| Situation | Recommended Approach | Why |
|-----------|---------------------|-----|
| No known systems delay issue | Component 2 only (SLA tracking) | Core deliverable; most repeatable; always valuable |
| Systems delay &gt;10 min average discovered | Components 1 + 2 | Need to fix systems first for SLA data to be meaningful |
| Systems delay &gt;15-20 min | Components 1 + 2 (urgent priority) | Critical issue -- no business reason for delay this high |
| Client also wants automated meeting scheduling | Recommend Component 3 as separate project | 50+ hours alone; high scope creep risk if combined |
| Inbound Lead Journey System Map already done | Use findings to scope Component 1 | Saves discovery time; systems delays likely already identified |
| No Lead Journey Map AND no known delay issue | Sample a dozen leads manually to assess systems delay | Quick diagnostic before committing to Component 1 |

### Scoping Factors

**1. Systems Delay Severity**

- Unknown / not measured --> Sample 12+ leads manually to assess; if average is under 10 min, likely skip Component 1
- 5-10 min average --> Yellow flag; worth investigating but may not justify full Component 1
- 10+ min average --> Include Component 1; significant delay worth fixing
- 15-20+ min average --> Urgent priority; this is actively destroying conversion rates

**2. Lead Type Complexity**

- Single lead type (e.g., all inbound demo requests) --> Simpler SLA rules; faster build
- 2-3 lead types (hand-raiser, non-hand-raiser, event) --> Standard complexity; different SLA thresholds per type
- 4+ lead types with different urgency tiers --> More complex SLA rule matrix; more custom fields and workflows required

**3. Existing Tech Stack**

- HubSpot + Salesforce --> Standard build; most repeatable pattern
- HubSpot + Salesforce + LeanData --> Additional complexity for systems delay investigation in routing graph
- Other MAP/CRM combinations --> Approach is the same; specific field types and workflow capabilities may vary

**4. Prerequisite Projects**

- Inbound Lead Journey System Map completed --> Component 1 scoping is straightforward; delays already identified
- No prior system mapping --> Either scope a system map as prerequisite or manually sample leads for delay assessment

### Tool Selection Framework

| Need | Recommended Tool | When to Choose It |
|------|-----------------|-------------------|
| Speed to lead (fast meeting booking from forms) | ChiliPiper Concierge | Client prioritizes reducing time-to-meeting; simpler routing needs |
| Complex routing logic with many decision nodes | LeanData | 10+ reps, territory-based routing, multiple business units, PTO automation needed |
| Both speed and complex routing | ChiliPiper + LeanData together | Client needs accurate routing AND fast meeting booking; budget allows both |
| Simple round robin, budget-conscious | CRM-native (Salesforce Assignment Rules, HubSpot Workflows) | &lt;10 reps, flat team structure, stable team composition |
| Chat-based routing | Qualified or ChiliPiper | Client wants live chat as a lead capture channel |
| Automated meeting scheduling (Component 3) | ChiliPiper, LeanData BookIt, Qualified, or Default | Depends on existing stack and routing complexity |

ChiliPiper reduces time-to-meeting through real-time form enrichment, form shortening, and instant calendar booking. LeanData excels at complex routing with automated PTO coverage via calendar integration. For many B2B SaaS companies at scale, the combination of both produces the best speed-to-lead outcome.

### Routing Approach Decision Tree

Use this when a client's lead routing approach has not been determined yet and needs to be scoped as part of (or before) the Speed to Lead project:

| Question | If Answer Is... | Then... |
|----------|-----------------|---------|
| Is your team flat or specialized? | Flat (everyone sells everything) | Round Robin is viable and fastest |
| | Specialized (by product, industry, geo) | Territory-Based routing needed |
| Do you have named accounts with specific owners? | Yes | Target Account approach (with fallback for non-named leads) |
| Has a Sales Territory design been completed? | No | Either do Round Robin or complete Sales Territory project first |
| How many reps need leads routed? | &lt;10 | CRM-native routing is usually sufficient |
| | 10+ | Consider dedicated tool (LeanData, ChiliPiper) regardless of approach |

---

## 3) Benchmarks & Standards

### How to Use Benchmarks

Benchmarks are guidelines, not rules. Always:
1. Start with benchmark as baseline
2. Measure the client's actual current state
3. Set targets based on what is achievable given their stack and team
4. Document deviations and rationale
5. Reassess quarterly as systems and processes mature

### Systems Delay Benchmarks

These thresholds represent the average time from lead engagement (form submission) to lead assignment and rep notification. They are based on LeanScale's experience across multiple B2B SaaS implementations.

| Systems Delay Average | Rating | Interpretation |
|----------------------|--------|----------------|
| 2-3 minutes | Best possible | Near-theoretical minimum given MAP processing, enrichment, and routing. Almost never seen in practice. |
| ~5 minutes | Realistic best-in-class | Achievable target for well-optimized systems. |
| 5-10 minutes | Acceptable | Common range for companies with reasonable automation; monitor but not urgent |
| 10+ minutes | Yellow flag | Time to raise yellow flags and take a deeper dive. Investigate for hard-coded delays and tech debt. |
| 15-20+ minutes | Red alert | Should not be happening. There's no reason why that should be necessary. Immediate action required. |
| 30+ minutes | Critical | Multiple stacked hard-coded delays across systems. |

**Important caveat:** These are averages, not outliers. Platform outages (HubSpot downtime, Salesforce maintenance windows) will create temporary spikes that should not be counted against the average.

### Industry Lead Response Time Benchmarks

External research on how fast companies actually respond to leads:

| Metric | Data Point | Source |
|--------|-----------|--------|
| Average B2B lead response time | 42-47 hours | Forbes; HBR [1][4] |
| Percentage of leads never contacted | Up to 73% | Kixie/industry surveys [5] |
| Companies responding within 5 minutes | Only 7% | Drift study of 433 companies [6] |
| Companies taking 5+ days to respond | 55% | Drift study [6] |
| Percentage of sales won by first responder | 35-50% | InsideSales.com [2] |
| Percentage of customers buying from first responder | 78% | LeanData industry research [7] |

**Interpretation:** The bar is shockingly low. Most B2B companies respond in days, not minutes. Any company that achieves sub-5-minute total speed to lead is operating in the top tier. This makes speed to lead a genuine competitive advantage, not just an operational improvement.

### Speed to Lead Impact on Conversion

Research consistently shows a direct, measurable relationship between response time and conversion rates:

| Response Time | Impact | Source |
|--------------|--------|--------|
| Within 1 minute | 391% increase in conversion rate | Web engagement studies [5] |
| Within 5 minutes | 100x more likely to connect; 21x more likely to qualify | MIT/InsideSales.com study [1][2] |
| 5 to 10 minutes | Odds of qualifying drop by 400% compared to 5-minute response | HBR [4] |
| After 10 minutes | Odds of qualifying drop by 80% from peak | MIT/InsideSales.com study [1] |
| After 30 minutes | 21x less likely to qualify vs. 5-minute response | HBR [4] |

**Key takeaway:** The conversion curve is not linear -- it drops dramatically after 5 minutes and is nearly flat after 30 minutes. The difference between a 3-minute and 15-minute response is far greater than the difference between a 15-minute and 60-minute response.

### SLA Rule Benchmarks

Typical SLA thresholds by lead type, based on LeanScale implementation experience and industry practice:

| Lead Type | Typical SLA Range | Rationale |
|-----------|------------------|-----------|
| Demo request / hand-raiser | 15 minutes - 2 hours (30 min typical) | Highest buying intent; prospect is actively evaluating; speed directly impacts conversion |
| Pricing page / high-intent signal | 30 minutes - 2 hours | Strong intent signal but may not have explicitly requested contact |
| Content download / webinar attendee | 24 - 48 hours | Lower urgency; prospect is in research phase; overly fast outreach can feel aggressive |
| Event attendee / conference lead | 24 - 48 hours | Similar to content; batch-uploaded leads may not expect immediate contact |
| Cold outbound reply / re-engagement | 30 minutes - 4 hours | Prospect responded to outreach; momentum matters but urgency is lower than inbound hand-raiser |

**Note:** Clients may define 3-4 tiers (e.g., hot, warm, cold) with different SLA rules per tier. The exact tiers and thresholds are a business decision, not a technical one.

### Quick Reference Thresholds

| Question | Good | Warning | Red Flag |
|----------|------|---------|----------|
| What's our average systems delay? | &lt;5 min | 5-10 min | &gt;10 min |
| What's our total speed to lead (hand-raiser)? | &lt;10 min | 10-30 min | &gt;30 min |
| What's our SLA hit rate? | &gt;85% | 70-85% | &lt;70% |
| How many leads go uncontacted? | &lt;5% | 5-15% | &gt;15% |
| How long to respond to a demo request? | &lt;30 min | 30 min - 2 hrs | &gt;2 hrs |

---

## 4) Calculations & Scoring

### Formula Quick Reference

| Calculation | Formula | Example |
|-------------|---------|---------|
| Total Speed to Lead | `First_Sales_Touch_Datetime - Lead_Engagement_Datetime` | Form submitted at 10:00 AM, rep calls at 10:42 AM = 42 min |
| Systems Delay | `Rep_Notified_Datetime - Lead_Engagement_Datetime` | Form submitted at 10:00 AM, lead assigned and alert sent at 10:08 AM = 8 min |
| Human Delay | `First_Sales_Touch_Datetime - Rep_Notified_Datetime` | Rep notified at 10:08 AM, rep calls at 10:42 AM = 34 min |
| SLA Status | `IF(Human_Delay &lt;= SLA_Threshold, "Hit", "Miss")` | SLA threshold = 30 min, human delay = 34 min = SLA Miss |
| SLA Hit Rate | `Count(SLA_Hit) / Count(All_Leads_With_SLA) * 100` | 85 hits out of 100 tracked leads = 85% hit rate |

### Speed to Lead Calculation

**Formula:**
```
Total Speed to Lead = First_Sales_Touch_Datetime - Lead_Engagement_Datetime
```

**Variables explained:**
- `Lead_Engagement_Datetime` = The moment the lead took action: form submission timestamp, CTA click timestamp, list upload processing timestamp. This is the starting clock from the lead's perspective.
- `First_Sales_Touch_Datetime` = The moment the assigned rep makes first contact: outbound call logged, email sent, LinkedIn message sent. This must be a logged activity in the CRM, not just "opened the record."

**Worked Example:**

*Scenario: A demo request comes in via website form on a Tuesday morning.*

```
Given:
- Lead_Engagement_Datetime = 10:00:00 AM
- Lead assigned to Rep (notification sent) = 10:07:00 AM
- Rep makes first call = 10:25:00 AM

Calculate:
- Systems Delay = 10:07 - 10:00 = 7 minutes
- Human Delay = 10:25 - 10:07 = 18 minutes
- Total Speed to Lead = 10:25 - 10:00 = 25 minutes
- SLA Threshold for hand-raiser = 30 minutes
- SLA Status = Hit (18 min human delay < 30 min threshold)
```

**Validation:**
- Systems delay should typically be 2-10 minutes. If consistently above 10, investigate for hard-coded delays.
- Human delay varies widely. Track trends over time rather than individual data points.
- If total speed to lead is under 5 minutes for hand-raisers, the client is performing at the top tier of B2B SaaS companies.

### SLA Performance Scoring

**Formula:**
```
SLA Hit Rate = (Number of SLA Hits / Total Leads Tracked) * 100
```

**Important:** SLA performance is measured against the human delay only, not total speed to lead. The SLA clock starts when the rep is notified, not when the lead submits a form.

**Reporting dimensions:**
- By lead type (hand-raiser vs. non-hand-raiser)
- By rep (individual performance)
- By team (SDR team, AE team)
- Over time (weekly/monthly trend)

**Escalation tier logic:**

| Tier | Trigger | Alert Recipient | Timing |
|------|---------|----------------|--------|
| Tier 1 | SLA missed | Assigned rep | Immediately on miss |
| Tier 2 | SLA missed + no follow-up | Rep's manager | 2-3 hours after miss with no follow-up |
| Tier 3 | SLA missed + still no follow-up | CRO or CMO | Full business day with no follow-up |

### Business Hours Considerations

SLA calculations should account for business hours to avoid penalizing reps for leads arriving outside working hours.

**Recommended approach:**
- Define standard business hours per client (e.g., 8 AM - 6 PM local time, Mon-Fri)
- For hand-raiser leads during business hours: SLA clock starts immediately on notification
- For hand-raiser leads outside business hours: SLA clock starts at next business day open
- For non-hand-raiser leads: Business hours calculation is standard since the SLA window is 24-48 hours
- Document holiday handling (company holidays pause the SLA clock)
- Address this explicitly in sales team training so reps understand the rules
- For clients with global teams across time zones, consider follow-the-sun SLA rules where the clock starts based on the nearest team's business hours

---

## 5) Edge Cases

### Hard-Coded Workflow Delays (Tech Debt)

*Scenario:* Client has multiple hard-coded delays built into MAP workflows and routing flows, resulting in a 30+ minute average systems delay. Each delay was originally added to prevent a race condition between systems.

*Approach:*

1. Map every hard-coded delay in the system (workflows, routing graphs, process builders)
2. For each delay, document the race condition it was solving
3. Design custom fields or datetime stamps that act as completion triggers instead of time delays
4. Configure downstream workflows to trigger off the completion field rather than an arbitrary wait
5. Test thoroughly that the race condition is actually resolved before removing the delay
6. Measure systems delay before and after to confirm improvement

### Rep on Vacation or Leaves Company

*Scenario:* A sales rep goes on vacation or leaves the company, and lead routing is not updated to reflect their unavailability. Leads get assigned to the unavailable person and sit unworked.

*Approach:*

1. Identify the routing tool's PTO handling capability:
   - LeanData: Automated via calendar integration
   - CRM-native routing: Manual exclusion required
   - ChiliPiper: Calendar-based availability built into scheduling
2. For tools without automated PTO: Build an operational process for removing reps from routing when they are OOO
3. Exclude SLA misses caused by routing-to-unavailable-rep from rep performance reporting (flag these separately as "process failures")

### Lead Routing Breaks

*Scenario:* Upstream routing processes break or malfunction -- a workflow errors out, a routing graph has a logic gap, or a CRM integration fails. SLA data gets polluted with misses caused by routing failures, not rep behavior.

*Approach:*

1. When SLA miss rates spike unexpectedly, first investigate whether there was a routing or system issue during that period
2. Cross-reference SLA miss spikes with systems delay spikes -- if both spike simultaneously, the cause is almost certainly a system issue
3. Flag affected leads in reporting so they can be excluded from rep performance evaluation
4. Build a monitoring alert for when systems delay exceeds a threshold (e.g., 2x the normal average) to catch routing breaks early

> "If lead routing breaks or whatever, that has a downstream effect on SLA performance, speed to lead performance. And you can see a big spike in time it takes to follow up, or SLAs being missed. But that may not necessarily be because the humans are doing a worse job." -- LeanScale

### Missing Routing Criteria (Leads Fall Through)

*Scenario:* A lead comes in that doesn't match any defined territory or routing criteria. Unmatched leads sit in a queue with no owner assigned.

*Approach:*

1. Always build a default/fallback routing path that catches any lead not matching defined criteria
2. Route fallback leads to a designated person or queue (usually a sales ops manager or team lead)
3. Monitor the fallback queue volume -- if it is consistently receiving leads, the routing criteria need expansion
4. Set alerts when leads hit the fallback path so they are not ignored

---

## References

[1] [MIT/InsideSales.com Lead Response Management Study](https://www.insidesales.com/response-time-matters/)
[2] [InsideSales.com Lead Response Management Best Practices](https://resources.insidesales.com/wp-content/uploads/2019/11/infograpic-_LeadRespMgmt.pdf)
[3] [Johnny Grow - 7 Lead Management SLA Best Practices](https://johnnygrow.com/marketing/lead-management/7-lead-management-service-level-agreement-best-practices/)
[4] [HBR - The Short Life of Online Sales Leads](https://hbr.org/2011/03/the-short-life-of-online-sales-leads)
[5] [Kixie - Speed to Lead Response Time Statistics](https://www.kixie.com/sales-blog/speed-to-lead-response-time-statistics-that-drive-conversions/)
[6] [Drift - State of Conversational Marketing (433 Company Study)](https://martal.ca/speed-to-lead-lb/)
[7] [LeanData - Speed to Lead: Speed is the Key](https://www.leandata.com/blog/speed-to-lead-speed-is-the-key-to-lead-conversion/)
[8] [Freshworks - SLA Response Time Guide](https://www.freshworks.com/itsm/sla/response-time/)
[9] [Microsoft - SLA Time Calculation Scenarios](https://learn.microsoft.com/en-us/dynamics365/customer-service/administer/sla-time-scenarios)
[10] [Rep.ai - 9 Lead Response Time Statistics](https://rep.ai/blog/lead-response)
