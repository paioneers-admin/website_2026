# Paioneers Website Content Plan

## Overview
Swap all iTValuations content for Paioneers content while preserving the existing design system (cream/dark-teal palette, IBM Plex fonts, animations, single-page scroll layout). Two sections need structural code changes (VaaS → Problem, Services 6→3 tabs). Everything else is pure text replacement.

---

## HEADER
**Structure:** Logo + 4 nav links + 1 CTA button (no structural change)

| Element | Current (iTValuations) | New (Paioneers) |
|---------|----------------------|-----------------|
| Logo text | "iTValuations" | "Paioneers" |
| Nav link 1 | About → #approach | About → #approach |
| Nav link 2 | Services → #services | Services → #services |
| Nav link 3 | Successes → #stats | Results → #stats |
| Nav link 4 | Resources → #cta | Contact → #cta |
| CTA button | "Get A Valuation" | "Book a Workshop" |

Also update: mobile menu links, page title, meta description.

---

## SECTION 1: HERO
**Structure:** h1 + p + 1 CTA button + 5 animated chevrons (no structural change)

| Element | Current | New |
|---------|---------|-----|
| h1 | "Helping your IT company reach new heights." | "Your Sales Team Spends More Time Researching Than Selling" |
| p | "Whether buying, selling, merging..." | "We build AI-powered revenue systems that automate prospect research, personalise outreach at scale, and keep every deal moving — so your team focuses on selling." |
| CTA button | "Get A Valuation" | "Book a Bottleneck Workshop" |
| Chevrons | Keep as-is | Keep — abstract energy/motion works |

**Decision needed:** Add a secondary CTA text link ("See How It Works →") below the button? Current design only has one button.

---

## SECTION 2: STATS
**Structure:** "By The Numbers" label + bar chart SVG + 4 interactive list items + large number display + CTA button (no structural change)

| Stat | data-value | Label |
|------|-----------|-------|
| Stat 1 (active) | "8 hrs" | "Saved Per Rep, Per Week" |
| Stat 2 | "6" | "Qualified Meetings Guaranteed in 90 Days" |
| Stat 3 | "50+" | "Data Points Per Prospect" |
| Stat 4 | "4 wks" | "From Kickoff to System Live" |

| Element | Current | New |
|---------|---------|-----|
| Label | "By The Numbers" | "By The Numbers" (keep) |
| CTA button | "Let's Talk" | "Book a Workshop" |
| Bar chart SVG | Keep as-is | Keep — abstract visual decoration |

---

## SECTION 3: VaaS → "THE PROBLEM"
**Structure change needed:** Right column changes from financial dashboard to comparison table.

**Left column (same structure):**

| Element | Current | New |
|---------|---------|-----|
| h2 | "More than a multiple." | "What Most Sales Teams Look Like vs. What's Possible" |
| p | Valuation measurement text | "The left column isn't a bad company. It's a normal company. The right column is what happens when you treat sales like infrastructure." |
| CTA | "Get VaaS" | "Book a Workshop" |

**Right column — Replace dashboard with comparison table:**

Current: chart header + area chart SVG + gauge + 6 metrics grid.
New: Styled comparison table (7 rows, 2 columns) that gives same "data-rich" visual weight.

| What most companies have | What Paioneers builds |
|---|---|
| Reps manually researching prospects | AI-enriched dossiers before every touchpoint |
| Generic email templates sent to thousands | Hyper-personalised outreach, 50+ data points per prospect |
| CRM data that's 3 weeks old | CRM that updates itself after every interaction |
| Stalled deals that nobody notices | Daily AI pipeline scan with next-action recommendations |
| Follow-ups written from scratch | AI-drafted follow-ups based on actual call transcripts |
| Forecasts based on gut feeling | Forecasts based on live, structured, complete data |
| New reps take 3 months to ramp | Day-one reps perform like veterans with AI prep |

Style this as a dark-background card/panel that matches the section's dark teal aesthetic. Consider animating rows on scroll (fade-in stagger).

---

## SECTION 4: SERVICES
**Structure change needed:** 6 tabs → 3 tabs. Update JS tab-switching logic, icon SVGs, counter max.

**Tab nav:** Remove 3 items, keep 3:

| Tab | data-index | Label |
|-----|-----------|-------|
| Tab 1 | 0 | Bottleneck Workshop |
| Tab 2 | 1 | Pipeline Accelerator |
| Tab 3 | 2 | Revenue Conversion Engine |

**Tab content:**

### Tab 1 — Bottleneck Workshop (01)
- **Title:** "Bottleneck Workshop"
- **Description:** "A half-day diagnostic session that maps your complete sales process, identifies every bottleneck and leakage point, and delivers a prioritised roadmap within one week. If you don't walk out with at least 3 actionable insights, it's free."
- **Link text:** "Book a Workshop"
- **Icon:** New SVG icon (diagnostic/magnifying glass concept)

### Tab 2 — Pipeline Accelerator (02)
- **Title:** "Pipeline Accelerator"
- **Description:** "A fully automated outbound engine. AI-powered prospect research, hyper-personalised outreach across email and LinkedIn, and multi-channel sequencing — generating qualified meetings without your team writing a single email. 6 meetings guaranteed in 90 days."
- **Link text:** "Start With a Workshop"
- **Icon:** New SVG icon (pipeline/funnel concept)

### Tab 3 — Revenue Conversion Engine (03)
- **Title:** "Revenue Conversion Engine"
- **Description:** "AI infrastructure that prepares reps before every call, automates CRM updates and follow-ups after every interaction, and monitors your pipeline daily. No deal stalls without someone knowing about it. System live in 4 weeks."
- **Link text:** "Start With a Workshop"
- **Icon:** New SVG icon (engine/gear concept)

**The Loop — below tabs (not a tab itself):**
Add a short text line below the services display area:
"Both engines connect through The Loop — insights from every closed and lost deal feed back into targeting and messaging. The system gets smarter every cycle."

**JS changes required:**
- Update servicesData array from 6 to 3 items
- Update counter max from 06 to 03
- Update gradient background positions (currently 6 positions → 3)
- Remove references to deleted service tabs

---

## SECTION 5: APPROACH / ABOUT
**Structure:** h2 + subheadline + paragraph + 2 buttons + image (no structural change)

| Element | Current | New |
|---------|---------|-----|
| h2 | "Our Approach" | "Technical Background. Commercial Execution." |
| Subheadline | "IT Business Valuators optimizing for your life, not just the biggest check." | "Paioneers was built by sales reps and GTM engineers who lived the problem before solving it." |
| Paragraph | Generic consultant positioning | "We've carried quota at Salesforce and LinkedIn, built commercial engines at agencies and SMBs, and felt the pain of manual research, inconsistent data, and tools that don't talk to each other. We stopped solving the same problems manually and started building systems." |
| Button 1 | "Get In Touch" | "Book a Workshop" |
| Button 2 | "Our Services" | "Our Services" (keep) |
| Image | Unsplash stock photo | Team photo or relevant image (use placeholder for now) |

**Optional addition:** A quote block with "We don't replace your salespeople. We give your best people superpowers." — can be added below the paragraph without breaking layout.

---

## SECTION 6: CTA
**Structure:** separator + h2 + p + CTA button + SVG graphics (no structural change)

| Element | Current | New |
|---------|---------|-----|
| h2 | "We'd love to show how we help." | "Let's Find Where Your Pipeline Leaks" |
| p | "Get in touch with us to talk through how we can help you know and grow the value of your IT services firm." | "The Bottleneck Workshop maps your sales process in half a day and gives you a prioritised roadmap within a week. If you don't walk away with at least 3 actionable insights, it's free." |
| CTA | "Let's Talk" | "Book a Bottleneck Workshop" |
| SVG graphics | Keep as-is | Keep — abstract shapes work universally |

---

## FOOTER
**Structure:** Brand + address + contact + credentials box + CTA + copyright + social links (no structural change)

| Element | Current | New |
|---------|---------|-----|
| Brand name | "iTValuations" | "Paioneers" |
| Address | 900 Long Lake Road, Suite 205, New Brighton, MN 55112 | Meander 877, 1181WN Amstelveen, Netherlands |
| Phone | 612-895-7590 | +31 (0) 646492246 |
| Email | info@itvaluations.com | info@paioneers.nl |
| Credential 1 label | "Member" | "Certified" |
| Credential 1 text | "National Association of Certified Valuators and Analysts" | "Clay Certified Expert" |
| Credential 2 label | "Credentials" | "Experience" |
| Credential 2 text | "Certified Valuation Analyst" | "Salesforce · LinkedIn · Juniper" |
| CTA button | "Let's Talk" | "Book a Workshop" |
| Copyright | "© 2026 iTValuations. All Rights Reserved" | "© 2026 Paioneers BV. All Rights Reserved" |
| Social: LinkedIn | Keep | Update href to Paioneers LinkedIn |
| Social: Facebook | Keep or remove | Decision needed |
| Social: YouTube | Keep or remove | Decision needed |

---

## MODAL
**Structure:** Left (label + headline + description + calendar link) + Right (form with 7 fields) (no structural change)

| Element | Current | New |
|---------|---------|-----|
| Label | "Let's Connect" | "Let's Connect" (keep) |
| Headline | "Ready to know your IT company's worth?" | "Find Out Where Your Pipeline Leaks" |
| Description | "Book a free consultation directly on our calendar..." | "Book a Bottleneck Workshop directly, or fill out the form and we'll get back to you within 24 hours." |
| Calendar link | Google Calendar (iTValuations) | Update to Paioneers booking link |
| Form: Company placeholder | "Your IT Company" | "Your Company" |
| Form: Service dropdown | Valuations, Buying, Selling, Merging, VCA, iT Tax Advisors, General Inquiry | Bottleneck Workshop, Pipeline Accelerator, Revenue Conversion Engine, General Inquiry |
| Form: Message placeholder | "What are you looking to achieve?" | "Tell us about your current sales process..." |
| Success message | "Our team will review your information..." | "We'll review your details and get back to you within 24 hours." |

---

## SUMMARY OF CHANGES

| Section | Change Type | Effort |
|---------|------------|--------|
| Header + Mobile Menu | Text swap | Low |
| Hero | Text swap | Low |
| Stats | Text swap (4 items) | Low |
| VaaS → Problem | Text swap + new right-column HTML/CSS (dashboard → comparison table) | Medium |
| Services | Text swap + reduce 6→3 tabs + update JS + new icons | Medium |
| Approach | Text swap + new image | Low |
| CTA | Text swap | Low |
| Footer | Text swap | Low |
| Modal | Text swap + update dropdown options + booking link | Low |
| Page meta | Title, description, favicon | Low |

**Two medium-effort items:** Section 3 (new comparison table component) and Section 4 (3 tabs + JS update). Everything else is straightforward find-and-replace.
