

**PAIONEERS**  
GTM Consultancy | AI-Powered Growth

**Pain-Based Segmentation**

**& PQL Framework**

*How Paioneers identifies, scores, and prioritises prospects*

*based on the pain they experience — not just the profile they match.*

**CONFIDENTIAL — INTERNAL DOCUMENT**

Version 1.0 | March 2026

# **Table of Contents**

[Table of Contents	2](#heading=)

[Part 1: The Framework	5](#heading=)

[From ICP Scoring to Pain Qualified Leads	5](#heading=)

[The Shift: Signals to Pain Segments	5](#heading=)

[The Dual Scoring Architecture	5](#heading=)

[Routing Logic	6](#heading=)

[Part 2: The Seven Pain Segments	7](#heading=)

[Segment 1: "Hiring Their Way Out"	7](#heading=)

[Existential Data Point	7](#heading=)

[Why It Is Existential	7](#heading=)

[Vacancy Type as Sub-Indicator	7](#heading=)

[Detection in Clay	8](#heading=)

[Messaging Kernel	8](#heading=)

[TAM Estimate (NL)	8](#heading=)

[Pain-Based Forecast	8](#heading=)

[Segment 2: "Automation Hunger"	9](#heading=)

[Existential Data Point	9](#heading=)

[Why It Is Existential	9](#heading=)

[Detection in Clay	9](#heading=)

[Offer Match	9](#heading=)

[Messaging Kernel	9](#heading=)

[TAM Estimate (NL)	9](#heading=)

[Pain-Based Forecast	10](#heading=)

[Segment 3: "Knowledge Island"	11](#heading=)

[Existential Data Point	11](#heading=)

[Why It Is Existential	11](#heading=)

[Detection in Clay	11](#heading=)

[Offer Match	11](#heading=)

[Messaging Kernel	11](#heading=)

[TAM Estimate (NL)	12](#heading=)

[Pain-Based Forecast	12](#heading=)

[Segment 4: "Revenue Leadership Reset"	13](#heading=)

[Existential Data Point	13](#heading=)

[Why It Is Existential	13](#heading=)

[Detection in Clay	13](#heading=)

[Offer Match	13](#heading=)

[Messaging Kernel	13](#heading=)

[TAM Estimate (NL)	13](#heading=)

[Pain-Based Forecast	14](#heading=)

[Segment 5: "Growth Without System"	15](#heading=)

[Existential Data Point	15](#heading=)

[Why It Is Existential	15](#heading=)

[Detection in Clay	15](#heading=)

[Offer Match	15](#heading=)

[Messaging Kernel	15](#heading=)

[TAM Estimate (NL)	16](#heading=)

[Pain-Based Forecast	16](#heading=)

[Segment 6: "New Market Entry"	17](#heading=)

[Existential Data Point	17](#heading=)

[Why It Is Existential	17](#heading=)

[Detection in Clay	17](#heading=)

[Offer Match	17](#heading=)

[Messaging Kernel	17](#heading=)

[TAM Estimate (NL)	17](#heading=)

[Pain-Based Forecast	18](#heading=)

[Segment 7: "Manual Process Bottleneck"	19](#heading=)

[Existential Data Point	19](#heading=)

[Why It Is Existential	19](#heading=)

[Chronic vs. Acute: Classification Note	19](#heading=)

[Detection in Clay	19](#heading=)

[Offer Match	19](#heading=)

[Messaging Kernel	20](#heading=)

[TAM Estimate (NL)	20](#heading=)

[Pain-Based Forecast	20](#heading=)

[Part 3: Combined Forecast & Prioritisation	21](#heading=)

[The Pain-Based Forecast Formula	21](#heading=)

[Segment Prioritisation Matrix	21](#heading=)

[Recommended Campaign Priority	22](#heading=)

[Part 4: Scoring Architecture	23](#heading=)

[Gate 1: ICP Score (0–100)	23](#heading=)

[Scoring Components	23](#heading=)

[Gate 2: PQL Score (0–100)	23](#heading=)

[Signal Scoring	24](#heading=)

[PQL Tier Classification	24](#heading=)

[Part 5: Offer Mapping Matrix	26](#heading=)

[Key Pattern: The Bottleneck Workshop as Universal Entry	26](#heading=)

[Part 6: Anti-ICP Definition	27](#heading=)

[Hard Exclusions (Disqualify Immediately)	27](#heading=)

[Soft Exclusions (Penalty Points, Not Disqualifying)	27](#heading=)

[Important Nuance	27](#heading=)

[Part 7: Detection Architecture in Clay	28](#heading=)

[Overview: Two Tables, Two Refresh Cycles	28](#heading=)

[Signal Detection: Data Sources per Segment	28](#heading=)

[Part 8: Next Steps	30](#heading=)

[Immediate (Week 1–2)	30](#heading=)

[Short-Term (Week 3–4)	30](#heading=)

[Medium-Term (Month 2–3)	30](#heading=)

[Ongoing	30](#heading=)

# **Part 1: The Framework**

## **From ICP Scoring to Pain Qualified Leads**

Paioneers has built a solid ICP-based targeting system: firmographic scoring to determine if a company fits our profile, combined with signal detection to find timing indicators. This works. But it leaves a critical gap.

The current system answers: *"Does this company fit our profile?"* and *"Are there any signals that suggest they might need us?"*

Pain-based segmentation adds a deeper question: **"What specific pain is this company experiencing, and how acutely?"**

The difference is operational. An ICP score tells you whether to call. A PQL score tells you why you call and what you say.

### **The Shift: Signals to Pain Segments**

Signals (hiring, news, LinkedIn activity, growth indicators) are symptoms. They are observable from the outside. Pain segments are the underlying conditions that those symptoms point to. A company posting three SDR vacancies is a signal. The underlying pain is that they are trying to solve a system problem by adding headcount — and burning cash in the process.

By mapping signals to pain segments, we achieve three things:

* Every outreach message is grounded in a specific, relatable pain — not a generic observation.

* Our offer mapping becomes precise: different pains map to different Paioneers services.

* Our scoring becomes predictive: pain intensity \+ pain type determines priority and messaging angle.

### **The Dual Scoring Architecture**

We build two parallel scoring systems in Clay that work in sequence:

**Gate 1: ICP Score (0–100)** — "Can we work with this company?"

Firmographic fit: B2B vs B2C, company size, sector, region, language, presence of manual processes (industry classification), and anti-ICP exclusion criteria. This is a static score based on company characteristics that rarely change. Stored in the firmographic/static table in Clay.

**Gate 2: PQL Score (0–100)** — "Do they need us, and how urgently?"

Pain signal detection: which pain segments are active, how many signals are firing simultaneously, how strong each signal is. This is a dynamic score based on live signals that are refreshed periodically. Stored in the signal table in Clay.

### **Routing Logic**

| ICP Score | Action | Description |
| :---- | :---- | :---- |
| **≥ 50** | Full PQL Enrichment | All pain signals are checked. Full enrichment pipeline runs. PQL score determines priority, messaging angle, and offer mapping. |
| **25 – 49** | Ultra Signals Only | Only the 1–2 strongest, cheapest-to-detect signals are checked (e.g. 3+ sales vacancies, new CRO appointed). If an ultra signal fires, the prospect qualifies despite lower ICP fit. No full enrichment to save credits. |
| **\< 25** | Disqualified | No further enrichment. Company is excluded from the pipeline. Examples: B2C, wrong region, anti-ICP match. |

*An ICP score tells you whether to call. A PQL score tells you why you call, and what you say.*

# **Part 2: The Seven Pain Segments**

Each pain segment follows a structured breakdown inspired by the Cannonball GTM framework for pain-based segmentation. For each segment we define: the existential data point (what makes this urgent), why it is existential (the consequence of inaction), how we detect it (current Clay capabilities and ideal future proxies), which Paioneers offer maps to it, and the messaging kernel for outbound.

## **Segment 1: "Hiring Their Way Out"**

*They are solving a system problem by adding headcount.*

### **Existential Data Point**

The company has one or more sales vacancies open: SDR, BDR, AE, Sales Manager, Head of Sales, or related roles. The vacancy itself is the signal. The type of vacancy indicates the type of pain.

### **Why It Is Existential**

An SDR in the Dutch SME market costs €4,500–€6,000 per month all-in (salary, employer costs, tooling, management time). Two SDRs equal €9,000–€12,000 per month in burn before they produce a single meeting. Ramp-up takes 2–3 months. During that period: zero output, full cost. If those SDRs then spend their days on manual prospect research, writing emails from scratch, and updating the CRM by hand, the company is paying human rates for machine work.

Every month that a sales seat is filled with manual labour instead of infrastructure is a month of compounding inefficiency. The longer they wait to systematise, the more expensive the problem becomes.

### **Vacancy Type as Sub-Indicator**

| Vacancy Type | Indicates | Primary Offer Match |
| :---- | :---- | :---- |
| **SDR / BDR** | Not enough pipeline. They need more top-of-funnel activity. They are looking for people to generate meetings. | Pipeline Accelerator |
| **Account Executive** | They have leads/meetings but need more closing capacity. The bottleneck is conversion, not generation. | Revenue Conversion Engine |
| **Sales Manager / Head of Sales** | They need structure, process, and oversight. The team exists but lacks a system. | Revenue System / Bottleneck Workshop |

### **Detection in Clay**

**Currently available:** LinkedIn Jobs API or vacancy scraping. Filter on sales-related job titles. One or more vacancies is sufficient to qualify. Company size filter: 10–250 FTE.

**Ideal future proxy:** Combine vacancy count \+ vacancy type \+ company growth rate. A company that is growing headcount by 20%+ and simultaneously posting sales vacancies has compounding urgency.

### **Messaging Kernel**

*"Jullie investeren in nieuwe salesmedewerkers om de pipeline te vullen. Uit ervaring weet ik dat de ramp-up maanden duurt en de kosten snel oplopen, terwijl het handwerk hetzelfde blijft. Wij bouwen de infrastructuur waardoor jullie team direct meer kan verkopen, zonder de wachttijd en het prijskaartje van een extra hire."*

### **TAM Estimate (NL)**

On any given day, approximately 10–15% of B2B companies in the 10–250 FTE range have at least one open sales vacancy. Within our addressable market of \~8,000–12,000 B2B companies: estimated 800–1,200 companies in this segment at any time.

### **Pain-Based Forecast**

1,000 (TAM) × 0.8 (Pain Intensity) × 0.03 (Conversion Rate) × €24,000 (ACV, based on Pipeline Accelerator Start × 12 months) × 1.1 (Sales Efficiency) \= **€633,600 ARR potential**

## **Segment 2: "Automation Hunger"**

*They are actively searching for someone to build their GTM automation internally.*

### **Existential Data Point**

The company has an open vacancy for: growth hacker, outbound specialist, marketing automation specialist, RevOps manager, Clay specialist, sales operations manager, or comparable roles that indicate they want to build automated sales infrastructure internally.

### **Why It Is Existential**

The person they hire will need 3–6 months to learn the toolstack, build the workflows, test them, and deliver first results. That single hire costs €50,000–€70,000 per year. All knowledge concentrates in one head. If that person leaves, the entire system leaves with them. Meanwhile, the clock is ticking on the sales targets that motivated the hire in the first place.

The alternative: Paioneers delivers a working system in 4–8 weeks, with documented processes and no single-person dependency.

### **Detection in Clay**

**Currently available:** LinkedIn Jobs scraping filtered on automation/growth/RevOps keywords in job titles. Keywords to scan: growth hacker, outbound specialist, sales automation, RevOps, revenue operations, marketing automation, Clay, sales operations, GTM engineer.

**Ideal future proxy:** Automation-related vacancy \+ no existing team member with a similar title visible on LinkedIn (indicating they are building this capability from scratch, not expanding a team).

### **Offer Match**

Primary: Revenue System / Bottleneck Workshop. The Workshop becomes the comparison moment: what does it cost to build this internally vs. with Paioneers? Secondary: Pipeline Accelerator if the vacancy specifically indicates outbound/lead generation needs.

### **Messaging Kernel**

*"Jullie zoeken iemand die jullie GTM-automatisering gaat opzetten. Uit ervaring weet ik dat zo iemand maanden nodig heeft om het stack te leren en de eerste resultaten te leveren — terwijl jullie nu al pipeline nodig hebben. Wij leveren een werkend systeem in weken, gedocumenteerd en zonder afhankelijkheid van één persoon. Zou het nuttig zijn om even te kijken wat dat voor jullie zou betekenen?"*

### **TAM Estimate (NL)**

Smaller segment: \~200–400 companies at any given time. These are specific vacancies. But conversion potential is high because the need is explicit and the budget is already allocated (they were willing to hire someone).

### **Pain-Based Forecast**

300 (TAM) × 0.85 (Pain Intensity) × 0.04 (Conversion Rate) × €30,000 (ACV, blended Workshop \+ System) × 1.2 (Sales Efficiency) \= **€367,200 ARR potential**

## **Segment 3: "Knowledge Island"**

*They have one person handling GTM/automation — but that person is isolated and they want external expertise.*

### **Existential Data Point**

The company has exactly one person (or a very small team) in a GTM, automation, or RevOps role. They have some capability but no depth. They know enough to know what is possible, but not enough to build it at scale. They are looking for external expertise to accelerate and expand what they have.

### **Why It Is Existential**

Single-person dependency is a structural risk. If that person leaves, the knowledge leaves. If that person is stretched thin, quality drops. And critically: they often do not know where to start on the next level of sophistication. They have built version 1.0 and need help getting to version 3.0.

This is the CloudMuscle pattern: a team that has some smart people in-house, but the owner recognises they need external expertise to level up. The proposition is not replacement, but acceleration.

### **Detection in Clay**

**Currently available:** LinkedIn people search within the company: count team members with GTM/automation/RevOps/sales operations titles. If count \= 1, this is a Knowledge Island. If count \= 0, this is Segment 2 (Automation Hunger). If count \= 3+, they may be too mature (anti-ICP check).

**Ideal future proxy:** Single GTM person \+ company is posting content about digital transformation or automation goals on LinkedIn/website \+ no recent automation-related hire beyond that one person.

### **Offer Match**

Primary: Bottleneck Workshop (diagnose what they have and what they need) → Revenue System (co-build with their existing person). This positions Paioneers as the accelerator, not the replacement. The existing person becomes the internal champion.

### **Messaging Kernel**

*"Ik zie dat jullie \[naam\] hebben die zich bezighoudt met jullie sales operations. Uit ervaring weet ik dat het lastig is om met één persoon het volledige plaatje te overzien — er is altijd meer mogelijk dan je in je eentje kunt bouwen. Wij werken vaak samen met interne teams om samen die volgende stap te zetten. Zou het waardevol zijn om eens te kijken waar de grootste kansen liggen?"*

### **TAM Estimate (NL)**

Moderate segment: \~300–500 companies. Many B2B companies in the 50–250 FTE range have exactly one person in this type of role.

### **Pain-Based Forecast**

400 (TAM) × 0.65 (Pain Intensity) × 0.04 (Conversion Rate) × €24,000 (ACV) × 1.0 (Sales Efficiency) \= **€249,600 ARR potential**

## **Segment 4: "Revenue Leadership Reset"**

*A new sales leader has been appointed in the last 0–6 months.*

### **Existential Data Point**

A CRO, VP Sales, Head of Revenue, Commercial Director, Head of Sales, or comparable role has started within the last 6 months. This is one of the strongest public signals that exists. It is 100% detectable via LinkedIn and the urgency is built into the role change itself.

### **Why It Is Existential**

A new revenue leader has an implicit mandate to change things. They have 90–180 days to demonstrate impact. They inherit a pipeline they did not build, a team they do not yet know, and a forecast that is probably unreliable. They need quick wins and they need to understand where the gaps are — fast.

This creates a natural window of openness: they are actively looking for solutions, they have budget authority (or can secure it as part of their mandate), and they want to put their stamp on the process.

### **Detection in Clay**

**Currently available:** LinkedIn profile change detection. For each company in the pipeline, search for people in sales leadership roles who started within the last 6 months. This gives us both the company signal and the direct contact to approach.

**Ideal future proxy:** New leader (0–6 months) \+ predecessor departed (indicating something was not working) \+ company has 20+ FTE. The combination of leadership turnover \+ departure signal is stronger than a new hire alone.

### **Offer Match**

Primary: Bottleneck Workshop. This is the perfect entry point: "You have just started. Within two weeks, we give you a complete picture of where your sales process leaks — so your first quarter has immediate impact." Follow-up: Pipeline Accelerator or Revenue Conversion depending on Workshop findings.

### **Messaging Kernel**

*"Ik zag dat je laatst bent gestart als \[rol\] bij \[bedrijf\]. Uit ervaring weet ik dat de eerste maanden cruciaal zijn — je erft een pipeline en een team die je nog moet leren kennen, terwijl de druk om te presteren er vanaf dag één is. Wij helpen sales leaders om binnen twee weken scherp te krijgen waar de grootste kansen liggen. Zou dat nuttig zijn in je huidige fase?"*

### **TAM Estimate (NL)**

Sales leadership changes approximately every 18–24 months on average. At any given time, roughly 5–8% of B2B companies in our range have a sales leader who started within the last 6 months: estimated 400–700 companies.

### **Pain-Based Forecast**

550 (TAM) × 0.9 (Pain Intensity) × 0.05 (Conversion Rate) × €18,000 (ACV, Workshop \+ follow-on) × 1.3 (Sales Efficiency) \= **€579,150 ARR potential**

## **Segment 5: "Growth Without System"**

*The company is growing fast, but sales infrastructure has not kept pace.*

### **Existential Data Point**

The company shows clear growth signals — headcount growth, funding rounds, acquisitions, expansion announcements, revenue milestones — but the sales team is disproportionately small for the company size, or there is no visible investment in sales infrastructure.

### **Why It Is Existential**

When a company doubles in ambition but keeps the same sales process, everything breaks. CRM becomes chaotic. Forecasting becomes guesswork. Deals fall through the cracks. The sales manager becomes a firefighter. Every new customer costs the same effort as the last one because there is no compound effect from the system.

Growth-stage companies face a specific timing pressure: the board or investors expect results that scale with the investment. Manual sales processes create a linear output curve against exponential expectations.

### **Detection in Clay**

**Currently available:** Headcount growth data via LinkedIn (Clay has this). News enrichment for funding, acquisitions, and expansion announcements. Sources to scan: Techleap.nl, Emerce, Sprout, MT/Sprout, Crunchbase (partial NL data), company LinkedIn posts about milestones.

**Sales team ratio indicator:** Count LinkedIn profiles with sales titles at the company vs. total headcount. Proposed thresholds: B2B company with 50+ FTE but \<3 sales-titled people \= indicator. 100+ FTE with \<5 sales-titled people \= strong indicator. This ratio needs empirical validation via a Clay sample run.

**Ideal future proxy:** Growth signal (any of: funding, 20%+ headcount growth in 12 months, acquisition, expansion announcement) \+ low sales-to-total-headcount ratio \+ no visible GTM/RevOps investment.

### **Offer Match**

Primary: Revenue System / Bottleneck Workshop. These companies need a systemic approach. The pain is not one thing — it is the gap between where they are and where their growth demands them to be. The Workshop diagnoses; the Revenue System builds.

### **Messaging Kernel**

*"Ik zag dat \[bedrijf\] flink aan het groeien is — \[specifiek signaal: nieuwe funding, acquisitie, headcount groei\]. Uit ervaring weet ik dat de salesinfrastructuur dat tempo vaak niet bijhoudt. Het team groeit, maar de processen blijven hetzelfde. Wij helpen groeiende bedrijven om hun sales te systematiseren zodat de groei ook schaalbaar wordt. Zou het waardevol zijn om eens te kijken waar de grootste knelpunten zitten?"*

### **TAM Estimate (NL)**

Approximately 500–800 B2B companies in our size range are in active growth mode at any time (based on headcount growth \>15%, recent funding, or expansion signals).

### **Pain-Based Forecast**

650 (TAM) × 0.75 (Pain Intensity) × 0.03 (Conversion Rate) × €36,000 (ACV, Workshop \+ Revenue System) × 1.1 (Sales Efficiency) \= **€579,150 ARR potential**

## **Segment 6: "New Market Entry"**

*The company is expanding into a new market, country, or segment — starting from zero.*

### **Existential Data Point**

The company announces or shows signs of entering a new geographic market, a new vertical, or launching a new product line. In the new market, they have no existing pipeline, no network, no referrals, and no inbound. They are starting cold.

### **Why It Is Existential**

In a new market, you have no shortcuts. No brand awareness, no word-of-mouth, no warm introductions. You must do outbound or you must wait months for inbound to build. And the internal expectation is usually that the new market produces results within 1–2 quarters. That gap between expectation and reality creates acute pain.

This was the NoRisk pattern: expanding to Sweden, needing fast lead enrichment and market intelligence because their existing Dutch network was useless in the new market.

### **Detection in Clay**

**Currently available:** News enrichment scanning for expansion-related keywords: new market, expansion, international growth, new office, entering \[country\]. Vacancy postings in a new country or city. LinkedIn posts from leadership about expansion plans.

**Important caveat:** Market entry decisions are often made internally before public announcement. Detection may lag the actual decision. However, when the announcement comes, the urgency is already high — they need to move fast.

### **Offer Match**

Primary: Pipeline Accelerator (build the outbound engine for the new market). Secondary/Downsell: Data Enrichment & List Building (if they want to do outreach themselves but need the intelligence). Also relevant: Bottleneck Workshop if they want to plan the full go-to-market for the new market.

### **Messaging Kernel**

*"Ik zag dat \[bedrijf\] bezig is met \[expansie naar X / nieuwe markt / internationalisering\]. Uit ervaring weet ik dat je in een nieuwe markt vanaf nul begint — geen netwerk, geen referrals, geen inbound. Wij bouwen voor bedrijven in die fase een outbound engine die snel de eerste gekwalificeerde gesprekken op de kalender zet. Zou het nuttig zijn om te kijken hoe dat er voor jullie uit zou zien?"*

### **TAM Estimate (NL)**

Smaller but high-urgency segment: \~150–300 companies at any given time. Conversion potential is above average because the need is acute and time-bound.

### **Pain-Based Forecast**

225 (TAM) × 0.85 (Pain Intensity) × 0.05 (Conversion Rate) × €24,000 (ACV) × 1.2 (Sales Efficiency) \= **€275,400 ARR potential**

## **Segment 7: "Manual Process Bottleneck"**

*The company has high volumes of repetitive, standardisable manual work in their commercial processes.*

### **Existential Data Point**

The company operates in an industry or business model that inherently involves high-volume, formulaic manual work: processing applications, qualifying leads by hand, generating proposals manually, managing onboarding paperwork, routing service requests. These processes follow predictable rules but are executed by humans.

### **Why It Is Existential**

Every manual step in a standardisable process is a bottleneck that increases throughput time, introduces errors, and caps scalability. At NoRisk (insurance), every event insurance application was manually reviewed against standardised acceptance criteria. That manual step created a queue, slowed revenue, and added no strategic value — because the criteria were predictable enough to automate.

This is a chronic pain, not an acute one. It does not suddenly appear — it has always been there. But it becomes existential when growth ambitions collide with manual capacity limits. More volume \= more manual work \= more people needed \= cost structure that scales linearly instead of logarithmically.

### **Chronic vs. Acute: Classification Note**

**This segment differs from segments 1–6 because it is an ongoing structural characteristic, not a triggered event.** Therefore, the Manual Process indicator is stored in Gate 1 (ICP Score) as a firmographic characteristic, not in Gate 2 (PQL Score) as a dynamic signal. Industries with high manual process density receive a higher ICP base score. However, when combined with an acute trigger from another segment (e.g. Segment 5: growth pressure), the chronic pain becomes acute.

### **Detection in Clay**

**Currently available:** Industry classification (SBI codes or LinkedIn industry tags). Target industries with high manual process density: insurance, financial services, real estate/property management, legal services, recruitment/staffing, logistics/freight, wholesale distribution, accounting/audit.

**Advanced detection (build later):** Scrape company descriptions and service pages. Use AI classification to estimate process complexity: "Does this company likely have high-volume, rule-based manual processes?" This is a hypothesis layer that can be validated over time.

**Supporting indicator:** Vacatures for operations, process improvement, or office automation roles can confirm the pain is active.

### **Offer Match**

Primary: Bottleneck Workshop as entry (discover where the manual work sits and what is automatable). Follow-up: Custom automation workflows. This is outside the three standard offers (Pipeline Accelerator, Revenue Conversion, Revenue System) and should be scoped and priced per engagement after the Workshop.

### **Messaging Kernel**

*"Ik werk vaak met bedrijven in \[branche\] en uit ervaring weet ik dat er in jullie type processen — \[specifiek: aanvraagverwerking, offertebeoordeling, lead-kwalificatie\] — nog veel handwerk zit dat tegenwoordig geautomatiseerd kan worden. Niet alles, maar de voorspelbare, repetitieve stappen. Wij helpen bedrijven ontdekken welke stappen dat zijn en bouwen daar de workflows voor. Zou het waardevol zijn om eens te kijken waar de grootste tijdswinst zit?"*

### **TAM Estimate (NL)**

Potentially the largest segment by volume (every organisation has manual processes), but detectability from the outside is the lowest. Focusing on the high-density industries listed above, and within our size range: estimated 1,000–2,000 companies. However, only a fraction will have this as an active, articulated pain. Effective TAM for outbound targeting: \~400–700.

### **Pain-Based Forecast**

550 (TAM) × 0.5 (Pain Intensity — lower because chronic) × 0.03 (Conversion Rate) × €20,000 (ACV, Workshop \+ custom) × 0.9 (Sales Efficiency) \= **€148,500 ARR potential**

# **Part 3: Combined Forecast & Prioritisation**

## **The Pain-Based Forecast Formula**

Following the Cannonball GTM methodology, each segment is scored using:

*Segment ARR Forecast \= TAM × Pain Intensity Factor × Conversion Rate × ACV × Sales Efficiency Factor*

Where TAM is the estimated number of companies currently in the segment (NL). Pain Intensity Factor (0–1.0) reflects urgency and acuteness. Conversion Rate is the estimated percentage of segment companies that would become clients. ACV is the average contract value based on primary offer match. Sales Efficiency Factor (0.5–1.5) adjusts for expected sales cycle efficiency (pain-driven segments convert faster).

## **Segment Prioritisation Matrix**

| Segment | TAM | Pain | Conv% | ACV | Eff. | ARR | Priority |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **1\. Hiring Their Way Out** | 1,000 | 0.80 | 3% | €24K | 1.1 | **€634K** | **HIGH** |
| **4\. Leadership Reset** | 550 | 0.90 | 5% | €18K | 1.3 | **€579K** | **HIGH** |
| **5\. Growth Without System** | 650 | 0.75 | 3% | €36K | 1.1 | **€579K** | **HIGH** |
| **2\. Automation Hunger** | 300 | 0.85 | 4% | €30K | 1.2 | **€367K** | **MEDIUM** |
| **6\. New Market Entry** | 225 | 0.85 | 5% | €24K | 1.2 | **€275K** | **MEDIUM** |
| **3\. Knowledge Island** | 400 | 0.65 | 4% | €24K | 1.0 | **€250K** | **MEDIUM** |
| **7\. Manual Process** | 550 | 0.50 | 3% | €20K | 0.9 | **€149K** | **LOWER** |
| **TOTAL** | **3,675** |  |  |  |  | **€2.83M** |  |

Total addressable ARR across all seven pain segments: approximately €2.83M. This is the theoretical ceiling based on conservative conversion estimates for the Dutch B2B market within our size range (10–250 FTE).

Note: these segments overlap. A single company can be in multiple segments simultaneously (e.g. Growth Without System \+ Hiring Their Way Out). Overlapping signals should increase PQL score, not double-count TAM.

## **Recommended Campaign Priority**

Based on the matrix above, the recommended first two campaign segments are:

**Campaign 1: Segment 1 (Hiring Their Way Out)** — Largest TAM, highest ARR potential, easiest to detect (vacancies), and maps directly to the Pipeline Accelerator which is the most developed offer.

**Campaign 2: Segment 4 (Revenue Leadership Reset)** — Highest pain intensity, highest conversion rate, strong detection (LinkedIn job changes), and the Bottleneck Workshop is the ideal entry point for these prospects. Added benefit: the contact to approach is the new leader themselves.

Segments 5 (Growth Without System) and 2 (Automation Hunger) are strong third and fourth priorities for when the first two campaigns are running and optimised.

# **Part 4: Scoring Architecture**

## **Gate 1: ICP Score (0–100)**

The ICP Score is a static firmographic assessment stored in the firmographic table. It answers: "Can we work with this company?" It is calculated once and updated periodically (e.g. quarterly) or when new data becomes available.

### **Scoring Components**

| Criterion | Max Points | Scoring Logic |
| :---- | :---- | :---- |
| **B2B Classification** | 15 | B2B \= 15pts. B2B2C \= 10pts. Mixed \= 5pts. B2C \= 0pts (hard disqualifier below 25 threshold). |
| **Company Size (FTE)** | 15 | 20–100 FTE \= 15pts (sweet spot). 100–250 \= 12pts. 10–20 \= 8pts. 250–500 \= 5pts. \<10 or \>500 \= 0pts. |
| **Region & Language** | 10 | Netherlands \= 10pts. Belgium (NL-speaking) \= 8pts. DACH \= 5pts. Other \= 2pts. |
| **Industry Relevance** | 15 | SaaS/Tech \= 15pts. Professional services \= 12pts. Financial services/Insurance \= 12pts. Recruitment/Staffing \= 10pts. Wholesale/Distribution \= 8pts. Other B2B \= 5pts. |
| **Manual Process Density** | 15 | AI classification of company type/industry: high expected manual process density \= 20pts. Medium \= 10pts. Low \= 5pts. This is the Segment 7 firmographic indicator. |
| **Sales Team Presence** | 10 | Has identifiable sales roles on LinkedIn \= 10pts. Has commercial leadership \= 8pts. No visible sales function \= 3pts. (No sales team \= harder to sell to, but not disqualifying.) |
| **Revenue Model Fit** | 10 | Recurring revenue (SaaS, subscriptions, retainers) \= 10pts. Project-based with repeat \= 7pts. One-time transactional \= 3pts. |
| **Anti-ICP Penalties** | \-30 to 0 | Competitor/ Automation agency \= \-100pts. Mature GTM team (3+ dedicated GTM/RevOps/automation people) \= \-15pts. Very long sales cycle industry (e.g. heavy industry, government) \= \-10pts. |

**Maximum possible score: 90 points** (before anti-ICP penalties). A perfect-fit B2B SaaS company in the Netherlands with 50 FTE, high manual process density, a visible sales team, and recurring revenue scores 90\.

## **Gate 2: PQL Score (0–100)**

The PQL Score is a dynamic signal-based assessment stored in the signal table. It answers: "Do they need us right now, and how urgently?" It is recalculated on each signal refresh cycle.

### **Signal Scoring**

| Signal | Points | Segment | Ultra Signal? |
| :---- | :---- | :---- | :---- |
| **2+ sales vacancies open simultaneously** | 25 | Seg 1 | YES — check even for ICP 25–49 companies |
| **1 sales vacancy open** | 15 | Seg 1 | No |
| **Automation/GTM vacancy open** | 20 | Seg 2 | YES |
| **Single GTM/automation person (Knowledge Island)** | 10 | Seg 3 | No |
| **New sales leader (0–6 months)** | 25 | Seg 4 | YES |
| **Growth signal (funding/acquisition/expansion)** | 15 | Seg 5 | No |
| **Headcount growth \>20% in 12 months** | 10 | Seg 5 | No |
| **Low sales-to-headcount ratio** | 10 | Seg 5 | No |
| **New market entry signals** | 20 | Seg 6 | No |
| **Operations/process vacancy** | 5 | Seg 7 | No |

Signals are additive. A company with a new sales leader (25pts) who is also hiring SDRs (15pts) and shows headcount growth (10pts) scores 50 on PQL — and is flagged with both Segment 1 and Segment 4 pain angles for messaging.

### **PQL Tier Classification**

| PQL Score | Tier | Action |
| :---- | :---- | :---- |
| **≥ 40** | **Tier 1: Hot** | Immediate outreach. Highest priority. Full briefing for Bart. Messaging uses the strongest pain segment as primary angle. Multiple signals \= multi-angle approach. |
| **20 – 39** | **Tier 2: Warm** | Queue for outreach in next cycle. Single strongest pain segment drives messaging. Standard briefing. |
| **1 – 19** | **Tier 3: Watch** | Store for future. LinkedIn profile visit only. Re-check signals on next refresh cycle. Can be activated by marketing/content campaigns. |
| **0** | **No Signal** | ICP fit exists but no active pain detected. Hold in database. Marketing nurture only. |

# **Part 5: Offer Mapping Matrix**

Each pain segment maps to one or more Paioneers offers. The primary offer is the most natural fit; the secondary offer is available as follow-up or cross-sell. The entry point is how the first conversation begins.

| Segment | Entry Point | Primary Offer | Cross-Sell | Downsell |
| :---- | :---- | :---- | :---- | :---- |
| **1\. Hiring (SDR/BDR)** | Direct pitch or Workshop | Pipeline Accelerator | Rev. Conversion | Data Enrichment |
| **1\. Hiring (AE)** | Workshop | Revenue Conversion | Pipeline Accel. | Baseline Audit |
| **1\. Hiring (Manager)** | Workshop | Revenue System | Both engines | Workshop only |
| **2\. Automation Hunger** | Workshop | Revenue System | Pipeline Accel. | Workshop only |
| **3\. Knowledge Island** | Workshop | Revenue System | Rev. Conversion | Workshop only |
| **4\. Leadership Reset** | Workshop | Workshop → varies | Both engines | Quick Win Guide |
| **5\. Growth w/o System** | Workshop | Revenue System | Both engines | Workshop only |
| **6\. New Market Entry** | Direct pitch | Pipeline Accelerator | Data Enrichment | Data Enrichment |
| **7\. Manual Process** | Workshop | Custom Automation | Rev. Conversion | Workshop only |

## **Key Pattern: The Bottleneck Workshop as Universal Entry**

Six of seven segments use the Bottleneck Workshop as the primary entry point. Only Segment 1 (SDR/BDR hiring, where the pain is directly addressable by the Pipeline Accelerator) and Segment 6 (New Market Entry, where urgency favours a direct pitch) can bypass the Workshop.

This confirms the Revenue System document’s positioning: the Workshop is the front door. It is the most efficient client acquisition mechanism because it pre-qualifies, builds trust, and lets the roadmap sell the follow-on services.

# **Part 6: Anti-ICP Definition**

The Anti-ICP defines which companies should be explicitly excluded from the pipeline, regardless of pain signals. These are companies where Paioneers cannot deliver value, where the sales cycle is unsuitable, or where the relationship would be unprofitable.

### **Hard Exclusions (Disqualify Immediately)**

* B2C companies (consumer-only business model).

* Direct competitors: other GTM consultancies, outbound agencies, Clay agencies, RevOps consultancies that offer similar services.

* Companies with fewer than 10 employees (too small to benefit from systematisation).

* Companies with more than 500 employees (enterprise complexity exceeds current delivery model).

* Government institutions and public-sector organisations (procurement cycles incompatible with our model).

### **Soft Exclusions (Penalty Points, Not Disqualifying)**

* Mature GTM teams: companies with 3+ dedicated people in GTM, RevOps, or sales automation roles. They may still need help, but the sales conversation is harder and the value proposition is different. Penalty: \-15 ICP points.

* Very long sales cycle industries: heavy industry, construction, infrastructure projects where deal cycles exceed 12 months. Our guarantee model (6 meetings in 90 days) does not translate well. Penalty: \-10 ICP points.

* Companies already using advanced automation stacks (Clay \+ n8n \+ CRM automation visible). They may want optimisation but not foundational build. Penalty: \-10 ICP points. Note: tech stack data is unreliable, so only apply this penalty when confirmed through multiple sources.

### **Important Nuance**

A company can have soft exclusion penalties and still qualify if their PQL score is high enough. A company with a \-15 penalty for having a mature GTM team (reducing ICP from 70 to 55\) that also has a new CRO (PQL \= 25\) and is posting SDR vacancies (PQL \+= 15 \= 40\) is still a Tier 1 prospect. The pain overrides the fit concern.

This is by design. The dual scoring system ensures we do not miss opportunities where the pain is real, even if the company profile is not our textbook ICP.

# **Part 7: Detection Architecture in Clay**

## **Overview: Two Tables, Two Refresh Cycles**

| Table | Content | Refresh Cycle |
| :---- | :---- | :---- |
| **Firmographic / Static Table** | Company characteristics: size, sector, region, B2B classification, manual process density, sales team presence, revenue model, anti-ICP flags. Produces: ICP Score (0–100). | Initial enrichment \+ quarterly refresh. Low API cost per company. Can run on full prospect database. |
| **Signal / Dynamic Table** | Live pain signals: vacancies, job changes, news, headcount growth, market entry indicators. Produces: PQL Score (0–100) \+ primary pain segment tag \+ messaging angle. | Periodic refresh (weekly to bi-weekly for Tier 1/2 prospects, monthly for the rest). Higher API cost — only runs on companies that pass ICP Gate 1 (≥50) or ultra-signal check (25–49). |

## **Signal Detection: Data Sources per Segment**

| Segment | Primary Data Source | Detection Method | Status |
| :---- | :---- | :---- | :---- |
| **Seg 1: Hiring** | LinkedIn Jobs / vacancy APIs | Keyword filter on sales-related titles. Count \+ type classification. | Available now in Clay |
| **Seg 2: Automation** | LinkedIn Jobs / vacancy APIs | Keyword filter on automation/GTM titles. | Available now in Clay |
| **Seg 3: Knowledge Island** | LinkedIn People Search | Count people with GTM/automation titles per company. Flag if count \= 1\. | Available now in Clay |
| **Seg 4: Leadership Reset** | LinkedIn Profile Changes | Detect job title changes on sales leadership roles. Filter start date \<6 months. | Available now in Clay |
| **Seg 5: Growth** | News enrichment \+ LinkedIn headcount | News scan on funding/acquisition/expansion keywords. Headcount growth % via LinkedIn. | Partially available |
| **Seg 6: New Market** | News enrichment \+ LinkedIn Jobs | News scan for expansion keywords. Vacancies in new geographies. | Partially available |
| **Seg 7: Manual Process** | Industry classification \+ AI | SBI code mapping \+ AI hypothesis on process density. Stored in firmographic table. | Build required |

# **Part 8: Next Steps**

## **Immediate (Week 1–2)**

* Validate Segment 1 (Hiring Their Way Out) detection in Clay: run a test scrape of B2B companies (20–250 FTE, NL) with open sales vacancies. Verify data quality and volume.

* Validate Segment 4 (Revenue Leadership Reset) detection: test LinkedIn job change detection for sales leadership roles. Verify recency filtering works.

* Define the ICP Score formula in Clay: implement the firmographic scoring table with the criteria from Part 4\.

* Establish the sales-to-headcount ratio baseline: run a sample of 100 known-good prospects and 100 random companies to test the ratio thresholds proposed for Segment 5\.

## **Short-Term (Week 3–4)**

* Build the PQL Score workflow in Clay: implement signal detection for Segments 1–4 (the four segments with fully available data sources).

* Build the routing logic: ICP ≥ 50 → full PQL enrichment; ICP 25–49 → ultra signals only; ICP \< 25 → disqualify.

* Create message briefing templates per segment: one briefing template for each of the seven segments, pre-loaded with the messaging kernel and offer mapping.

* Run the first outbound campaign targeting Segment 1 and Segment 4 simultaneously.

## **Medium-Term (Month 2–3)**

* Add Segments 5 and 6 (Growth Without System, New Market Entry): implement news enrichment scanning and headcount growth detection.

* Research and test funding data sources for NL: Techleap.nl, Crunchbase NL coverage, KvK API, Emerce/Sprout news scraping.

* Build the Segment 7 (Manual Process) AI classification: test company description analysis to estimate manual process density.

* Implement the Segment 3 (Knowledge Island) detection: LinkedIn people count per company for GTM/automation roles.

* First iteration of conversion tracking: which segments produce the most qualified conversations and meetings?

## **Ongoing**

* Refine PQL scoring weights based on actual conversion data. The current weights are estimates — real-world performance will shift them.

* Expand proxy signal research: identify new detectable indicators per segment. Every new proxy that works increases detection coverage.

* Feed closed/lost deal data back into segment definitions: which segments convert best? Which have the shortest sales cycle? Adjust priorities accordingly.

* Quarterly TAM refresh: re-run the segment sizing to track market dynamics and validate our estimates.

*— End of Document —*