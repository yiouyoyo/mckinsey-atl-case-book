# AI Practice Cases — McKinsey Format

Five original practice case interviews inspired by real McKinsey AI engagements. Each follows the standard McKinsey structure: client situation → objective → clarifying context → framework → data/exhibits → hypothesis → analysis → recommendation → risks and next steps.

Use these as solo practice (read and work through) or as interviewer–interviewee pairs (interviewer holds the exhibits section, reveals on request).

---

## Case 01 — Real-Time Retail Intelligence

**Inspired by:** McKinsey + QuantumBlack work with a major POS technology provider and NVIDIA on retail data personalization

---

### Client Situation

Your client is **RetailTech Co.**, a mid-sized point-of-sale (POS) technology company that serves grocery and specialty retailers across North America. Retailers use the client's terminals to process millions of transactions daily — generating enormous volumes of purchase data.

For years, that data was used only for backward-looking reports: weekly sales summaries, end-of-month category analysis, post-promotion reviews. Real-time use of the data — personalized offers at checkout, dynamic promotion adjustments, long-tail catalog optimization — has remained technically out of reach.

RetailTech's enterprise customers are increasingly asking for these capabilities. Two large grocery chains have issued RFPs citing real-time personalization as a required feature. A competitor recently launched a pilot with a rival technology provider.

RetailTech's CEO has hired McKinsey to help the company figure out how to build and commercialize a next-generation AI analytics platform before it loses these accounts.

---

### Objective

Help RetailTech determine whether and how to build a real-time AI analytics platform — and if yes, define the business model, technical approach, and go-to-market strategy.

---

### Clarifying Context

*(Reveal to candidate if asked)*

- RetailTech processes ~2 billion transactions annually across 4,000 retail locations
- Current data infrastructure: batch processing, overnight refresh cycles
- The company has a software engineering team of ~120; no internal ML/AI team
- Gross margin on current software: ~65%; current platform revenue: $180M ARR
- Top 10 customers account for 60% of revenue; two are threatening to churn
- Technology option under consideration: GPU-accelerated inference infrastructure via a cloud partnership
- Build timeline pressure: RFPs close in 90 days

---

### Framework

Structure your approach around three questions:

1. **Should we build it?** (strategic case and market opportunity)
   - What is the TAM for real-time retail analytics?
   - What is the churn risk if we don't build vs. cost to build?
   - Does this fit our core capability, or is it a distraction?

2. **How should we build it?** (technical and partnership strategy)
   - Build in-house, acquire an AI startup, or partner (e.g. cloud + AI provider)?
   - What is the minimum viable technical architecture?
   - What talent/capability gaps need to be filled?

3. **How do we commercialize it?** (go-to-market and pricing)
   - Add-on module vs. new product tier vs. open platform?
   - Pricing model: per-transaction, per-seat, or outcome-based (% uplift)?
   - Which customers do we pilot with first, and why?

---

### Exhibits

**Exhibit A — Market sizing (interviewer reveals on request)**

| Segment | Annual spend on retail analytics (US) | Growth rate |
|---------|--------------------------------------|-------------|
| Batch/historical analytics | $3.2B | 4% |
| Real-time personalization | $1.1B | 28% |
| AI-driven promotion optimization | $0.8B | 35% |

**Exhibit B — Customer churn risk model**

| Customer tier | ARR at risk | Churn probability (no action) |
|---------------|-------------|-------------------------------|
| Enterprise (>$5M ARR) | $72M | 65% |
| Mid-market ($1–5M ARR) | $36M | 30% |
| SMB (<$1M ARR) | $18M | 10% |

**Exhibit C — Build vs. partner cost estimate**

| Option | Upfront cost | Time to market | Gross margin on new product |
|--------|-------------|----------------|-----------------------------|
| Build in-house | $45M | 24 months | 70% |
| Acquire AI startup | $90M | 12 months | 60% |
| Cloud + AI partnership | $8M | 6 months | 45% |

---

### Hypothesis

> Real-time AI capabilities are now table stakes for RetailTech's enterprise segment. The fastest path to protecting revenue and capturing the new market is a partnership model — trading some margin for speed — while simultaneously building internal AI capability to bring the platform in-house over 18–24 months.

---

### Analysis

- **Churn math:** Enterprise churn at 65% = ~$47M ARR lost. Build-in-house cost is $45M over 24 months — by the time it launches, the accounts are already gone.
- **Partnership IRR:** Cloud + AI partnership costs $8M, gets to market in 6 months, protects $47M at risk, and captures share in a 28–35% growth segment. Break-even is within 6 months of launch.
- **Long-tail coverage gap:** Current catalog coverage for personalization is ~8% (only high-velocity SKUs have enough data). GPU-accelerated inference can push this toward 99%+ by processing low-frequency items in real time — this is the core technical differentiation.
- **Pricing recommendation:** Outcome-based pricing (% of measured uplift in basket size) aligns incentives and creates stickiness. Pilot with two at-risk enterprise customers.

---

### Recommendation

RetailTech should pursue a **cloud + AI technology partnership** immediately to protect its enterprise base and enter the real-time analytics market within 6 months. In parallel, it should hire an AI/ML team and begin building proprietary models, targeting a full in-house platform by month 24 to recapture margins.

Three priorities:

1. Sign a partnership agreement with a GPU cloud provider within 30 days
2. Pilot the real-time personalization module with the two churning enterprise accounts under a co-development agreement
3. Launch a hiring plan for 15–20 ML engineers; consider acqui-hire to accelerate

---

### Risks & Next Steps

- **Risks:** Partnership dependency creates vendor lock-in risk; margin dilution is real if volume growth is slower than projected; internal engineering culture may resist third-party architecture
- **Validate:** Customer willingness to pay for outcome-based pricing; actual uplift measurability in retailer P&Ls
- **Next steps:** 30-day sprint to finalize partnership terms; 60-day pilot design with two anchor customers; 90-day talent plan

---

## Case 02 — Revenue Growth Management at Scale

**Inspired by:** McKinsey's work with a global consumer health company to deploy AI-enabled revenue growth management tools across fragmented international markets

---

### Client Situation

Your client is **GlobalCPG**, a multinational consumer packaged goods company with a portfolio of over 200 brands across personal care, nutrition, and home health. It operates in 60 countries with $18B in annual revenue.

GlobalCPG's Revenue Growth Management (RGM) function — responsible for pricing, trade promotion, and channel mix decisions — is under pressure. Margins have compressed 300 bps over the past two years due to inflation, private label competition, and aggressive retailer negotiations.

The company's RGM approach is fragmented: each market uses different tools, different data, and relies heavily on the judgment of local commercial leaders. A pricing decision in Germany takes 3 weeks to model; the same decision in the US takes 4 days. Promotion ROI tracking is largely manual and retrospective.

The CEO has mandated a global RGM transformation and has given the Chief Commercial Officer 18 months to deliver measurable margin improvement. McKinsey has been brought in to design and implement the solution.

---

### Objective

Design an AI-enabled RGM transformation that can be deployed across markets with varying levels of data maturity — and deliver measurable margin improvement within 18 months.

---

### Clarifying Context

*(Reveal to candidate if asked)*

- 5 "core" markets (US, UK, Germany, Canada, Australia): strong data infrastructure, ERP-integrated, 3–5 years of clean transaction data
- 55 "emerging" markets: inconsistent data, fragmented systems, limited analytics capability
- Annual trade promotion spend: ~$2.1B globally (12% of revenue)
- Current promotion ROI measurement: post-hoc, 6–8 week lag, covers ~40% of promotions
- Internal analytics team: 35 people globally, mostly in Excel/BI tools
- Budget for transformation: $120M over 3 years

---

### Framework

Structure your approach around three tracks:

1. **Diagnostic: Where is the margin leaking?**
   - Which markets, brands, and channels have the worst promotion ROI?
   - Where is pricing power being given away unnecessarily?
   - What's the cost of the current decision lag?

2. **Solution design: What does "good" RGM look like?**
   - Core markets: AI-powered pricing and promotion optimization (real-time recommendations)
   - Emerging markets: standardized data collection and fact-based decision templates
   - Governance: who owns the model output? How do local leaders interact with it?

3. **Change management: How do you get adoption?**
   - What's the change story for local commercial teams who distrust models?
   - How do you sequence the rollout to build credibility early?
   - What capabilities need to be built internally for sustainability?

---

### Exhibits

**Exhibit A — Promotion ROI by market tier (interviewer reveals)**

| Market tier | Avg. promotion ROI | % of promotions with negative ROI | Data quality score (1–5) |
|-------------|-------------------|-------------------------------------|--------------------------|
| Core (5 markets) | 1.4x | 28% | 4.2 |
| Emerging (55 markets) | 0.9x | 47% | 2.1 |

**Exhibit B — Decision speed benchmark**

| Decision type | Current time (GlobalCPG) | Best-in-class benchmark |
|---------------|--------------------------|------------------------|
| Price change approval | 18 days | 3 days |
| Promotion ROI measurement | 7 weeks lag | Real-time |
| Trade term negotiation prep | 6 weeks | 2 weeks |

**Exhibit C — AI tool deployment options**

| Option | Markets served | Upfront cost | Expected margin impact |
|--------|---------------|--------------|------------------------|
| Full AI suite (RGMx-equivalent) | Core 5 only | $85M | +150–200 bps |
| Tiered deployment (full + lite version) | All 60 | $120M | +120–170 bps |
| Lite version only (standardized templates) | All 60 | $30M | +60–90 bps |

---

### Hypothesis

> The majority of margin leakage is concentrated in trade promotion spend — nearly half of promotions in emerging markets have negative ROI. A tiered deployment (full AI in core markets, standardized data discipline in emerging markets) will capture the most margin within budget and build the foundation for full AI deployment globally over time.

---

### Analysis

- **Promotion math:** $2.1B spend × 47% negative ROI promotions in emerging markets ≈ ~$500M in value-destroying promotion activity. Even recovering 20% of that = $100M gross margin improvement.
- **Core markets first:** With data quality score of 4.2 and 3+ years of clean data, core markets can go live with AI-powered recommendations in 6–9 months. Emerging markets need 12–18 months of data remediation before AI is reliable.
- **Sequencing insight:** Pilot in one core market (recommend US for scale, UK for speed) within 90 days. Use measurable results to build credibility with local commercial leaders before broader rollout.
- **Change management is the constraint:** The model is not the hard part — adoption is. Local teams need to see their own market's data validate the recommendations before they trust them.

---

### Recommendation

Deploy a **tiered AI-enabled RGM transformation**: full AI-powered pricing and promotion optimization in the 5 core markets in year one, standard data templates and decision frameworks in emerging markets simultaneously, with a path to full AI deployment in emerging markets by year three.

Three priorities:

1. Stand up the AI recommendation engine in the US market within 90 days as the credibility-building pilot
2. Launch a global data remediation program in emerging markets immediately — this is the long-pole in the tent
3. Embed RGM analytics translators (1–2 per core market) who can bridge model output and commercial teams

---

### Risks & Next Steps

- **Risks:** Local leader resistance to model-driven decisions; data quality in emerging markets worse than assessed; $120M budget constrained if early results disappoint
- **Validate:** US pilot promotion ROI lift before scaling; data audit in 10 emerging markets before committing to full rollout timeline
- **Next steps:** 30-day diagnostic deep-dive in US and Germany; 60-day data quality audit in 10 emerging markets; 90-day pilot launch in US

---

## Case 03 — Decarbonization Planning Automation

**Inspired by:** McKinsey's work with a major agricultural equipment manufacturer to automate emissions baselining and decarbonization cost-curve modeling using AI

---

### Client Situation

Your client is **AgroMach**, a global manufacturer of agricultural machinery with 28 manufacturing facilities across North America, Europe, South America, and Southeast Asia. It has $9B in annual revenue and approximately 22,000 employees.

Under pressure from institutional investors, regulators, and major agricultural customers (who face their own Scope 3 reporting requirements), AgroMach has committed to reducing its Scope 1 and 2 greenhouse gas emissions by 50% by 2032 and achieving net zero by 2050.

The company's sustainability team — 8 people — currently builds decarbonization plans manually: gathering emissions data from each facility, modeling abatement options, estimating costs, and producing a marginal abatement cost curve (MACC) that ranks interventions by cost-effectiveness. This process takes 8 weeks per planning cycle and is already consuming most of the team's capacity. As the 2032 deadline approaches, the frequency and granularity of planning will need to increase — but headcount can't scale proportionally.

AgroMach's CFO has asked McKinsey to help the company design an AI-powered solution to automate and accelerate its decarbonization planning process.

---

### Objective

Design an AI-enabled decarbonization planning capability that can reduce planning cycle time, improve analytical accuracy, and allow the sustainability team to operate at the speed and scale the 2032 commitment requires — without a proportional increase in headcount.

---

### Clarifying Context

*(Reveal to candidate if asked)*

- Current planning cycle: 8 weeks, twice per year; target: 4 cycles per year with facility-level granularity
- Data sources: utility bills, fuel receipts, production logs, facility-level ERP data — most are in different formats, manually consolidated in Excel
- Abatement options being modeled: renewable energy procurement, electrification of equipment, process efficiency upgrades, on-site solar, fuel switching
- Cloud infrastructure: AgroMach runs on AWS; data lake exists but sustainability data is siloed
- Budget: $15M for the AI tool development; $3M/year operational budget
- External constraint: Scope 3 reporting (supply chain emissions) will be required by 2027

---

### Framework

Structure your approach around three questions:

1. **What is the automation opportunity?**
   - Which steps in the current 8-week process are manual and automatable?
   - Where is the biggest time sink, and where is human judgment genuinely irreplaceable?

2. **What should the AI tool do?**
   - Automated data ingestion and normalization from facility-level sources
   - MACC generation: model each abatement option's cost and emissions impact automatically
   - Scenario modeling: what if energy prices change? What if a facility is sold?
   - Output: decision-ready recommendation ranked by cost per ton of CO₂ abated

3. **What does sustainable capability look like?**
   - How does the team's role change from data gatherers to decision-makers?
   - How do you extend the tool to Scope 3 (supply chain) by 2027?
   - Build vs. buy vs. configure existing sustainability software?

---

### Exhibits

**Exhibit A — Current process time breakdown (8 weeks total)**

| Step | Time (weeks) | Manual/automated today |
|------|-------------|------------------------|
| Data collection from 28 facilities | 3.5 | Manual (email + Excel) |
| Data cleaning and normalization | 1.5 | Manual |
| Abatement option modeling | 2.0 | Semi-manual (Excel models) |
| MACC build and presentation | 1.0 | Manual |

**Exhibit B — Abatement option cost estimates (sample)**

| Intervention | Cost per ton CO₂ abated | Emissions reduction potential | Feasibility (1–5) |
|-------------|------------------------|-------------------------------|-------------------|
| Renewable energy procurement | $18 | High | 5 |
| On-site solar (owned facilities) | $34 | Medium | 4 |
| Equipment electrification | $67 | High | 3 |
| Process efficiency upgrades | $12 | Low–Medium | 5 |
| Fuel switching (gas → green H₂) | $145 | Medium | 2 |

**Exhibit C — Build vs. configure options**

| Option | Cost | Time to first output | Coverage |
|--------|------|---------------------|----------|
| Build custom on AWS | $14M | 12 months | Scope 1+2 now, Scope 3 by 2027 |
| Configure existing sustainability SaaS | $6M | 4 months | Scope 1+2; Scope 3 roadmap unclear |
| Hybrid (SaaS core + custom extensions) | $9M | 7 months | Scope 1+2 now, Scope 3 extensible |

---

### Hypothesis

> The 8-week planning cycle is driven almost entirely by manual data collection and normalization — steps with no analytical value. Automating these alone reduces the cycle to under 2 weeks. A hybrid approach (configure a sustainability SaaS platform for the core MACC engine, build custom data pipelines on AWS) delivers the fastest time-to-value and preserves flexibility for Scope 3 extension.

---

### Analysis

- **Time compression:** Data collection (3.5 weeks) + normalization (1.5 weeks) = 5 of 8 weeks are pure logistics. Automated ingestion pipelines from facility ERP systems reduce this to hours. Planning cycles drop from 8 weeks to under 1 week.
- **Abatement cost insight:** Renewable energy procurement and process efficiency upgrades dominate the cost-effective end of the MACC. Prioritizing these alone captures most of the 50% reduction target at less than $35/ton — within range for the CFO's business case.
- **Hybrid build rationale:** Custom-build at $14M takes 12 months to first output — too slow for a 2032 deadline where every planning cycle counts. SaaS configuration at $6M misses Scope 3 requirements. Hybrid at $9M hits the market in 7 months and is extensible.
- **Capability shift:** The sustainability team moves from data gatherers (8 weeks of manual work) to scenario analysts and decision advisors — higher leverage, lower burnout risk.

---

### Recommendation

Build a **hybrid AI-powered decarbonization planning platform**: configure a leading sustainability SaaS tool as the MACC engine, and build custom AWS data pipelines to automate ingestion from all 28 facilities. Target first planning cycle output within 7 months.

Three priorities:

1. Automate data ingestion from all facilities via AWS-native pipelines — this is the highest-ROI step and can begin immediately
2. Select and configure a sustainability SaaS platform for MACC generation within 60 days; use pilot output from 3 facilities to validate
3. Design the Scope 3 data architecture now so the extension to supply chain emissions in 2027 doesn't require a rebuild

---

### Risks & Next Steps

- **Risks:** Facility-level data quality varies significantly; some facilities in Southeast Asia may lack digital records; SaaS vendor Scope 3 roadmap may be vaporware
- **Validate:** Data audit at 5 representative facilities before committing to ingestion architecture; reference checks on SaaS vendor Scope 3 claims
- **Next steps:** 30-day data audit across 5 facilities; 60-day SaaS selection and pilot; 90-day AWS pipeline build kickoff

---

## Case 04 — GenAI for Field Service Operations

**Inspired by:** McKinsey QuantumBlack's work with a heavy equipment distributor to deploy a generative AI tool that helps field service agents diagnose machine issues in real time

---

### Client Situation

Your client is **HeavyServ**, the after-sales service division of a large heavy equipment distributor operating across Europe and Latin America. HeavyServ distributes and maintains construction, agricultural, and industrial machinery from 25+ manufacturers.

When a customer's machine goes down on a job site, they call HeavyServ's service center. An agent must identify the exact machine (model, serial number, configuration), pull up its service history, then navigate manufacturer technical documentation — spread across thousands of PDFs and multiple databases — to diagnose the fault and dispatch the right technician with the right parts.

Currently this process takes up to 30 minutes per case. With 1,400 agents handling 2.8 million service calls annually, average handle time has a massive impact on customer satisfaction, agent morale, and operational cost. Customer satisfaction scores have been declining; two major construction firms have flagged slow diagnosis as a contract renewal risk.

The VP of Service Operations has asked McKinsey to design an AI solution that meaningfully reduces diagnostic time while maintaining accuracy.

---

### Objective

Design and assess the business case for a GenAI-powered field service diagnostic tool that reduces average handle time and improves first-call resolution for HeavyServ's service center.

---

### Clarifying Context

*(Reveal to candidate if asked)*

- Technical documentation: ~14,000 PDFs across 25+ brands; updated frequently by manufacturers; some only available in Portuguese, Spanish, or German
- CRM: Salesforce Service Cloud (fully deployed); agent desktop is Salesforce-native
- Average handle time: 24 minutes (industry benchmark: 9 minutes)
- First-call resolution rate: 61% (benchmark: 82%)
- Agent base: 1,400 agents; average tenure 2.2 years; high turnover (32% annually)
- Cost of a service call: $38 all-in; premium technician dispatch (when wrong parts sent): adds $210/incident
- Data: 5 years of case history in Salesforce; machine telemetry available for ~40% of fleet

---

### Framework

Structure your approach around three questions:

1. **Where does time go in the 24-minute handle?**
   - Break down the diagnostic process into steps
   - Identify which steps are manual search vs. judgment vs. customer communication
   - Determine which steps AI can accelerate vs. which require human expertise

2. **What should the AI tool do?**
   - Retrieval-augmented generation (RAG) on the technical document library
   - Machine identification from serial number → auto-pull service history
   - Suggested diagnostic paths and likely fault codes based on symptom description
   - Multilingual support for documentation in Portuguese/Spanish/German

3. **What is the business case?**
   - Quantify the handle time reduction and first-call resolution improvement
   - Calculate cost savings and revenue protection (contract renewal risk)
   - Estimate build cost and payback period

---

### Exhibits

**Exhibit A — Handle time breakdown (24 min avg)**

| Step | Avg. time | AI-addressable? |
|------|-----------|----------------|
| Customer and machine identification | 4 min | Yes (auto-lookup) |
| Searching technical documentation | 11 min | Yes (RAG retrieval) |
| Diagnosing fault / recommending fix | 5 min | Partial (AI suggests, agent confirms) |
| Logging case and dispatching | 4 min | Partial (auto-fill) |

**Exhibit B — Financial impact model (annual)**

| Metric | Current state | Target state (AI-enabled) |
|--------|--------------|--------------------------|
| Avg. handle time | 24 min | 10 min |
| First-call resolution | 61% | 80% |
| Incorrect dispatch incidents/year | 84,000 | 25,000 |
| Cost of incorrect dispatches | $17.6M | $5.3M |
| Agent capacity freed (hours) | — | 560,000 hrs |

**Exhibit C — Build options**

| Option | Approach | Est. cost | Time to deploy |
|--------|----------|-----------|----------------|
| Build custom RAG system | Internal ML team + cloud | $4.2M | 14 months |
| Configure existing AI platform (Salesforce Einstein + GenAI) | Native Salesforce integration | $1.8M | 5 weeks |
| Hybrid (Salesforce + custom document indexing) | Best of both | $2.4M | 10 weeks |

---

### Hypothesis

> The 24-minute handle time is driven primarily by document search — a step that GenAI retrieval is purpose-built to accelerate. Deploying a RAG-based tool natively within Salesforce Service Cloud (lowest switching cost for agents) can halve handle time within 10 weeks and pay back its build cost within 6 months.

---

### Analysis

- **Time math:** Document search alone (11 min) + machine ID (4 min) = 15 of 24 minutes are AI-addressable. Even partial automation (60% of search time) cuts handle time from 24 to ~13 minutes.
- **Financial case:** Incorrect dispatch reduction from 84K to 25K incidents saves $12.3M annually. Agent capacity freed (560K hours) can absorb volume growth without headcount adds — worth ~$8M in avoided hiring.
- **Salesforce-native rationale:** Agents already live in Salesforce. A native integration requires zero workflow change and near-zero retraining. Custom builds take 14 months and require agent behavior change — both are risks given 32% annual turnover.
- **Multilingual requirement:** RAG system must index documents across 3+ languages. This is technically solvable but adds 2–3 weeks to build; validate with vendor before contracting.

---

### Recommendation

Deploy a **Salesforce-native GenAI field service tool** using a hybrid approach: Salesforce Einstein for core RAG retrieval, augmented with a custom document indexing layer for the 14,000-PDF library. Target live deployment in 10 weeks.

Three priorities:

1. Index the full technical document library (all languages) within 30 days — this is the foundation for everything else
2. Build the Salesforce-native interface in parallel; involve 8–10 frontline agents in co-design to ensure output is trusted and usable
3. Instrument every interaction from day one — measure handle time, first-call resolution, and agent override rates daily to validate ROI and tune the model

---

### Risks & Next Steps

- **Risks:** Model hallucination on technical documents could worsen incorrect dispatches (catastrophic failure mode); agent distrust of AI suggestions; manufacturer PDF quality varies widely
- **Validate:** Human-in-the-loop override rate; accuracy on sample of 200 historical cases before live deployment
- **Next steps:** 2-week document library audit; 5-week Salesforce integration build; 10-week pilot with 50 volunteer agents; 16-week full rollout

---

## Case 05 — AI-Driven Hospital Operations Transformation

**Inspired by:** McKinsey's engagement with a large public health system to deploy predictive analytics for OR scheduling, workforce management, and patient flow optimization

---

### Client Situation

Your client is **Meridian Health**, a large urban public health system with six hospitals, 1,800 licensed beds, and $2.4B in annual operating revenue. As the safety-net system for its county, Meridian serves a high proportion of Medicaid, uninsured, and complex-acuity patients.

Meridian is facing a structural financial crisis: operating margin has declined to -3.2% over the past two years, driven by rising labor costs (premium agency staff now account for 22% of nursing hours), underutilized surgical capacity, and chronic patient flow bottlenecks that leave patients boarding in emergency departments for hours.

The system's board has given the CEO 24 months to reach operating breakeven. A previous cost-reduction initiative reduced supply costs by $18M but left clinical operations — the largest cost driver — largely untouched. The CEO believes AI-enabled operational transformation is the path to breakeven, and has engaged McKinsey to design and implement it.

---

### Objective

Design an AI-enabled operations transformation that closes Meridian's $77M operating margin gap within 24 months without compromising care quality for its safety-net patient population.

---

### Clarifying Context

*(Reveal to candidate if asked)*

- OR utilization: 61% (benchmark for comparable systems: 78%); 12% of OR time is blocked but unfilled
- Agency labor spend: $89M annually; benchmark for comparable systems: $45M
- Average ED boarding time (admitted patients waiting for inpatient bed): 6.4 hours (benchmark: 2.1 hours)
- EHR: Epic (fully deployed across all 6 hospitals); scheduling data is in Epic
- Existing analytics capability: a 4-person data analytics team; operational dashboards exist but are not predictive
- Capital constraint: no new capital for facility expansion; must optimize within existing footprint
- Political constraint: any workforce changes require consultation with nursing union (18-month contract cycle)

---

### Framework

Structure your approach around three operational levers:

1. **OR scheduling optimization**
   - What is driving the 61% utilization? Is it demand (not enough surgeries booked) or supply (blocks held by surgeons who don't fill them)?
   - AI opportunity: predictive scheduling that identifies unfilled blocks 48–72 hours in advance and automatically reaches out to surgeons with available time

2. **Workforce management**
   - What is driving agency labor overreliance? Is it chronic understaffing, poor shift-to-demand matching, or unpredictable patient volume?
   - AI opportunity: predictive staffing models that match nursing staff to patient volume and acuity by shift, reducing last-minute agency calls

3. **Patient flow optimization**
   - What is causing 6.4-hour ED boarding times? Is it discharge delays, bed assignment inefficiency, or transfer bottlenecks?
   - AI opportunity: predictive discharge and bed management tools that free capacity earlier in the day

---

### Exhibits

**Exhibit A — OR utilization breakdown**

| Driver of unutilized OR time | % of total unused time |
|-----------------------------|------------------------|
| Surgeon blocks held but not filled (>48hr notice) | 38% |
| Cases cancelled same-day (patient/prep issues) | 24% |
| Turnover time inefficiency | 21% |
| Late starts / early ends | 17% |

**Exhibit B — Labor cost bridge ($M)**

| Driver | Annual premium cost |
|--------|-------------------|
| Agency nursing (chronic short positions) | $41M |
| Agency nursing (surge/unpredicted demand) | $31M |
| Overtime (core staff) | $17M |

**Exhibit C — Patient flow bottleneck analysis**

| Bottleneck | Avg. delay contributed | AI-addressable? |
|-----------|----------------------|----------------|
| Discharge orders written late in day | 2.1 hours | Yes (predictive rounding prompts) |
| Bed cleaning/turnover coordination | 1.4 hours | Partial |
| Transfer coordination delays | 1.8 hours | Yes (automated bed assignment) |
| ED boarding (admitted, no bed assigned) | 1.1 hours | Yes (predictive bed demand) |

**Exhibit D — Margin impact model**

| Lever | Annual savings potential |
|-------|------------------------|
| OR utilization: +12 pts → +$28M revenue | $28M |
| Agency labor: -40% → $36M savings | $36M |
| ED boarding reduction → avoided diversion revenue | $14M |
| **Total** | **$78M** |

---

### Hypothesis

> Meridian's margin gap is concentrated in two areas: $89M in avoidable agency labor and $45M+ in recoverable OR revenue. Both are driven by poor demand predictability — which AI is purpose-built to solve. Deploying predictive scheduling and staffing tools on top of the existing Epic data infrastructure can close the gap within 24 months without requiring new capital or breaching union constraints.

---

### Analysis

- **OR math:** 12% of OR time is blocked-but-unfilled with >48 hours notice — this is recoverable. Adding 12 percentage points of utilization across 6 hospitals ≈ 8,400 additional surgical hours/year. At $3,300 average contribution per case, this is ~$28M in additional margin.
- **Labor math:** Surge agency spend ($31M) is the immediate AI target — predictive volume models give managers 48–72 hours of lead time to use core staff or per-diem rather than agency. Chronic short positions ($41M) require a separate hiring plan but benefit from AI-driven shift optimization.
- **Flow math:** Discharge delay (2.1 hrs) + transfer delay (1.8 hrs) = 3.9 hours of the 6.4-hour boarding time are directly AI-addressable. Cutting boarding to 2.5 hours reduces ED diversion, recovering an estimated $14M in avoided lost admissions.
- **Union constraint:** Workforce management changes should be framed as "better information for schedulers" not "AI replacing judgment" — reduces resistance and fits within existing contract language on scheduling tools.

---

### Recommendation

Launch a **three-lever AI operations program** built on Meridian's existing Epic infrastructure: predictive OR scheduling in 90 days, AI-driven staffing models in 120 days, and patient flow optimization in 180 days. Total target: $78M annual margin improvement, reaching breakeven by month 22.

Three priorities:

1. Deploy OR scheduling prediction (unfilled block identification + automated surgeon outreach) within 90 days — fastest payback, no union exposure, builds credibility for broader program
2. Stand up predictive staffing dashboards for nurse managers by month 4; frame as decision-support tool in all union communications
3. Implement predictive discharge and bed management by month 6; requires ED, hospitalist, and nursing leadership alignment upfront

---

### Risks & Next Steps

- **Risks:** Union resistance if staffing AI is perceived as a headcount tool; Epic data quality varies by hospital (some have poor documentation compliance); surgeon adoption of automated scheduling outreach may be low
- **Validate:** OR block data quality audit before building model; union counsel review of staffing tool framing; surgeon survey on scheduling outreach preferences
- **Next steps:** 2-week Epic data audit; 4-week co-design sprint with OR schedulers and nurse managers; 8-week pilot at one hospital before system-wide rollout

---

*Practice cases authored for interview prep. Inspired by publicly available McKinsey case studies — business situations, figures, and frameworks are original constructs for educational use.*
