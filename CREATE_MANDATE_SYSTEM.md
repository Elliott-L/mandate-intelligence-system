# Mandate Intelligence System — Master Prompt
# Paste everything below this line into Claude to recreate the full interactive system.
# Claude will build the complete tool in one response.
---

Please build me a fully interactive HTML artifact called the Mandate Intelligence System. This is a complete operational system for running intelligence-led hiring searches for tech/engineering roles at startups.

Build it as a single self-contained HTML file with inline CSS and JavaScript. It must work in any browser with no dependencies or internet connection required.

The tool must have six navigable tabs: Overview, Phases, Mandate structure, Prompt library, Failure modes, and Alternatives. Full specification for each tab is below.

---

## Design requirements

- Clean, minimal aesthetic. White surfaces, 0.5px borders, generous whitespace
- Font: DM Sans for body, Playfair Display (serif) for headings, DM Mono for labels and code
- Light and dark mode support using CSS variables
- No gradients, no shadows, no emoji
- All tab switching, phase expanding, checklist ticking, prompt expanding, and copy buttons must work via JavaScript
- Mobile responsive

---

## Tab 1 — Overview

Show:

**System architecture flow** (horizontal nodes with arrows):
Raw inputs → Input audit → Intelligence brief → Success profile → Search strategy → Execution assets

**Core principles** (2x2 grid of info cells):
- Separation of concerns: Raw inputs are transient. The mandate is persistent. Never blend data collection with structured thinking.
- Two-document model: Intelligence brief (factual, client-shareable) is separate from search strategy (directional, operational, internal).
- Candidate-first framing: Define the specific human you are looking for first. Build everything else around finding that person.
- Reasoning before generation: AI reasons through the mandate before producing any output. No premature summarisation.

**Minimum viable inputs** (3 cards in a grid):

Card 1 — Non-negotiable · 7 required · Must have before mandate creation:
- Company website (product, about, careers pages)
- Job description or role brief
- Hiring manager LinkedIn profile
- At least 2 engineers' LinkedIn profiles
- Funding stage and amount
- Intake call notes or direct client conversation
- Comp range (or explicit acknowledgement it is unknown)

Card 2 — Secondary · best effort · Add where available:
- GitHub / engineering blog / tech stack signals
- Founder LinkedIn profiles
- Press interviews or podcasts
- Competitor company links (3–5)
- Product documentation or demo
- Previous hires into similar roles
- Any candidate feedback from prior searches

Card 3 — Gap protocol · If MVIs are incomplete:
- Flag specific gaps to client before proceeding
- Mark all assumption-based sections clearly
- Set confidence level on mandate (High / Medium / Low)
- Identify which gaps most affect search quality
- Plan a follow-up re-audit once gaps are filled

**Output map** (2 info cells):
- Client-facing: Intelligence brief · Candidate brief · Client advisory · Timeline and pipeline forecast
- Internal operational: Success profile · Search strategy · Company target lists · Outreach by archetype · Objection handling guide

---

## Tab 2 — Phases

Show 7 phase cards in a grid. Each card is clickable and expands a detail panel below the grid.

**Phase 01 — Input collection** · Gather raw material. No summarising.
Checklist:
- Company website ingested (product, about, careers)
- Job description or role brief added
- Hiring manager LinkedIn profile added
- 2+ engineer LinkedIn profiles added
- Funding stage and amount confirmed
- Intake call notes or client conversation added
- Comp range confirmed (or gap noted)
- Secondary inputs added where available

Phase gate: Do not proceed until all 7 MVIs are present. If any are missing: flag to client, note the gap, set mandate confidence level, then proceed with caution.

**Phase 02 — Input audit** · Assess completeness. Surface gaps.
Checklist:
- Completeness assessment run against MVI standard
- Conflicting signals identified and flagged
- Hiring context assumptions challenged
- Comp feasibility assessed against market signals
- Role clarity evaluated (is the JD realistic?)
- Up to 10 targeted questions generated
- Answers to audit questions collected

Phase gate: All high-impact questions must be answered before mandate creation. Low-priority gaps can be noted but should not block the mandate if they are flagged.

**Phase 03 — Market reality check** · Does this person exist? At what cost?
Checklist:
- Talent pool size estimated
- Comp benchmarked against market
- Geographic availability assessed
- Notice period norms identified
- Competing demand assessed
- Realistic funnel size estimated
- Search difficulty rating assigned

Phase gate: If the market reality check reveals a significant gap between client expectations and market reality, this must be raised with the client before proceeding.

**Phase 04 — Mandate creation** · Build the two-document mandate.
Checklist:
- Intelligence Brief created (7 sections)
- Success Profile created (separate document)
- Search Strategy created (internal)
- All assumption-based sections clearly marked
- Mandate confidence level set (High / Medium / Low)
- Mandate version logged (v1.0, date)
- Mandate reviewed for polished-but-shallow risk

Quality check: Does the mandate contain specific salary ranges, named company targets, named talent pools, concrete hiring risks, and a clearly described success archetype? If it reads as generic, it is not ready.

**Phase 05 — Client validation** · Confirm brief before executing.
Checklist:
- Intelligence Brief shared with client or hiring manager
- Success profile confirmed or corrected
- Comp range validated or adjusted
- Any client corrections fed back into mandate
- Mandate updated to v1.1 if changes made
- Green light received from client to proceed

Phase gate: Do not begin sourcing until client has validated the success profile. This single step prevents the most common and costly search failure.

**Phase 06 — Execution** · All outputs from the mandate.
Checklist:
- Sourcing strategy generated from mandate
- Company target lists generated (direct / adjacent / non-obvious)
- Candidate brief generated
- Outreach generated by archetype
- Objection handling guide generated
- Client advisory generated
- Pipeline forecast generated

**Phase 07 — Feedback loop** · Search data back into mandate.
Checklist:
- Candidate response rates tracked vs. archetype
- Common objections captured and added to objection guide
- Comp expectations from real conversations noted
- Any client spec change captured and mandate re-versioned
- Company target list updated based on sourcing results
- Mandate re-audit triggered if search stalls for 2+ weeks

Re-audit triggers: Trigger a full mandate re-audit if: search stalls for 2+ weeks · client changes spec · comp reality diverges significantly · hiring manager changes · company raises/pivots.

All checklists must have tappable checkboxes that toggle a checked state visually.

---

## Tab 3 — Mandate structure

Show three sections separated by dividers.

**Document 1 — Intelligence brief (factual, client-shareable)**

7 cards in a responsive grid:

Section 01 — Company reality:
- What the company actually does (not the pitch)
- Business model and revenue stage
- Real product vs. marketed positioning
- Founding story and founder credibility signals
- Growth trajectory and evidence
- Key risks or red flags a candidate would encounter

Section 02 — Product and technical environment:
- Core product and tech stack (stated + inferred)
- Engineering team size and structure
- Build vs. buy philosophy signals
- Technical debt indicators (if visible)
- Deployment and infrastructure approach
- Open source or public engineering presence

Section 03 — True hiring context:
- Why this role exists now (real reason, not JD reason)
- What triggered the hire
- How long the role has been open and why
- What has been tried and failed (if known)
- Who owns the decision and who influences it
- Internal timeline pressure and hard deadlines

Section 04 — Role deconstruction:
- What the role actually involves (vs. JD)
- First 90-day priorities
- Non-negotiable requirements (true must-haves)
- Nice-to-haves wrongly listed as must-haves
- Skills absent from JD but actually needed
- Reporting line and real organisational context

Section 05 — Competitive positioning:
- 3–5 direct competitors for this candidate profile
- Why a candidate would choose this over alternatives
- Where this company loses candidates in comparison
- Comp, equity, stage, mission differentiation
- What this company offers that alternatives cannot

Section 06 — Market reality:
- Talent pool size estimate
- Comp benchmarks (realistic, not aspirational)
- Geographic availability
- Competing demand from other companies
- Typical notice periods for this profile
- Search difficulty rating with rationale

Section 07 — Hiring risks and constraints:
- Client-side risks
- Candidate-side risks
- Role-side risks
- Market risks
- Recommended trade-offs and mitigations

**Document 2 — Success profile (internal, standalone)**

2 cards:

Success profile · Part A — The person who succeeds:
- Specific archetype description (not a skills list)
- Career trajectory pattern that predicts success
- Company environments they thrive in
- Company environments that would produce failure
- What they have built, shipped, or delivered before
- How they work, not just what they know

Success profile · Part B — Motivation and movement:
- Why someone in this profile would move right now
- What they are looking for that their current role lacks
- What would make this role compelling to them specifically
- What would make them say no (anticipated objections)
- What comp and equity range would attract vs. repel
- What the strongest hook is for this archetype

**Document 3 — Search strategy (internal, operational)**

4 cards:

Strategy · Part A — Company target mapping:
- Direct targets (obvious, high-fit companies)
- Adjacent targets (transferable experience)
- Non-obvious targets (overlooked talent pools)
- Companies to avoid (wrong culture, wrong skills)
- Rationale for each category

Strategy · Part B — Sourcing prioritisation:
- Primary channels and why
- Secondary channels
- Profiles to prioritise within target companies
- Profiles to deprioritise and why
- Estimated funnel and conversion assumptions

Strategy · Part C — Candidate value proposition:
- Primary CVP hook for this archetype
- Secondary positioning angles
- Proof points and credibility builders
- What not to lead with

Strategy · Part D — Objection handling:
- Top 5 anticipated objections with responses
- Comp objection handling
- Stage/risk objection handling
- Counter-offer preparation
- Competing process handling

---

## Tab 4 — Prompt library

Show expandable prompt cards. Each card has a header (tag + title), expands on click, shows a usage note, then the full prompt text in a monospace code block with a Copy button that copies the prompt text to clipboard.

Tag styles: "Core · Phase XX" cards use a dark navy background tag. "Execution" cards use a light background tag.

**Prompt 1 — Core · Phase 01 — Session starter — input collection**

Usage note: Use this to open every new mandate session. Sets the operating rules for the collection phase. Do not deviate from these constraints until Phase 02 is explicitly triggered.

Prompt text:
You are operating as a mandate intelligence system for a specialist tech/engineering search firm.

Your combined perspective draws from:
— a senior search partner with 10+ years in engineering hiring
— a talent intelligence analyst focused on technical talent markets
— a sceptical operator who challenges assumptions before accepting them

We are beginning a new hiring mandate.

OPERATING RULES — Phase 01 (Input Collection):
1. Ingest every input I provide and track it in a running internal index
2. Categorise each input by type: [Company] [Role] [People] [Market] [Context] [Other]
3. Flag any input that appears to conflict with a previous input
4. Do NOT summarise, interpret, or draw conclusions from inputs
5. Do NOT generate any output sections, drafts, or recommendations
6. After each input, confirm receipt and note any immediate data quality concerns
7. When I add all inputs, tell me which of the 7 MVIs are still missing

MVIs (Minimum Viable Inputs) required before Phase 02:
— Company website (product, about, careers pages)
— Job description or role brief
— Hiring manager LinkedIn profile
— At least 2 engineer LinkedIn profiles from the company
— Funding stage and amount
— Intake call notes or direct client conversation
— Comp range (or explicit note that it is unknown)

Begin now. Confirm readiness and await first input.

---

**Prompt 2 — Core · Phase 02 — Input audit — gap analysis and challenge**

Usage note: Triggers the audit phase. Structured around risk categories rather than generic completeness — this produces sharper, more specific questions.

Prompt text:
Input collection is complete. Move to Phase 02: Input Audit.

Audit the inputs collected using the following framework:

1. COMPLETENESS ASSESSMENT
State which MVIs are confirmed present, which are absent, and which are present but low quality. Be specific about what is low quality and why.

2. CONFLICT DETECTION
Identify any inputs that contradict each other. Do not resolve the contradiction — flag it and ask me to clarify.

3. ASSUMPTION AUDIT
List every material assumption that would be baked into the mandate if we proceeded now. For each assumption, rate the risk of it being wrong: [Low / Medium / High].

4. TARGETED QUESTIONS
Generate up to 10 questions, prioritised by impact on search quality. Structure each question as:
— RISK AREA: [Talent supply / Comp / Role clarity / Hiring context / Client process / Other]
— QUESTION: [Specific question]
— WHY IT MATTERS: [What decision would change if the answer is different from the assumption]

5. HIRING RISK FLAGS
Identify up to 5 specific risks that could cause this search to fail or significantly underperform. Be direct. Do not soften.

6. MANDATE CONFIDENCE FORECAST
Based on current inputs, rate the confidence level of the mandate we could produce now: [High / Medium / Low]. Explain the rating in one sentence.

Do NOT begin mandate creation. Wait for my answers to your questions.

---

**Prompt 3 — Core · Phase 03 — Market reality check**

Usage note: A mandatory phase that most systems skip. Forces a reality check on talent supply before strategy is built.

Prompt text:
Before creating the mandate, run a market reality check.

Using all inputs collected, assess:

1. TALENT POOL SIZE
Estimate the realistic number of people in [location/remote scope] who:
— Match the core technical profile described
— Are at the right seniority level
— Are likely to be open to a move (not just technically qualified)
Give a rough order of magnitude: [<50 / 50–200 / 200–500 / 500+]. Explain the basis for your estimate.

2. COMPENSATION REALITY
State the realistic market rate for this profile in [location]. Compare it to the comp range provided by the client. Flag any gap. If comp is unknown, state what the market rate would likely be and what that means for candidate quality.

3. COMPETING DEMAND
Identify the categories of companies currently competing for this profile. How contested is this talent segment right now? Rate: [Low / Medium / High / Very High].

4. NOTICE AND AVAILABILITY
What is the typical notice period for this profile? Are there any factors (vesting cliffs, counter-offer risk, immigration status, competing processes) likely to affect availability?

5. FUNNEL ESTIMATE
Given the above, estimate a realistic funnel:
— Identifiable candidates: [N]
— Contactable and relevant: [N]
— Likely to engage: [N]
— Likely to progress to interview: [N]
— Realistic hires from this funnel: [N]

6. SEARCH DIFFICULTY RATING
Assign a rating: [Low / Medium / High / Rare]
One sentence rationale. One recommended adjustment if the search is High or Rare.

If the reality check reveals a material gap between client expectations and market conditions, flag this explicitly. State what you would recommend telling the client before proceeding.

---

**Prompt 4 — Core · Phase 04A — Intelligence brief creation**

Usage note: Creates Document 1 of the mandate — factual, evidence-grounded, client-shareable. Mark all assumptions explicitly.

Prompt text:
Using all inputs, audit responses, and market reality check, create the Intelligence Brief.

This is Document 1 of 3. It is factual, evidence-grounded, and client-shareable.

QUALITY STANDARD before you begin:
Every section must contain at minimum one specific, concrete claim. Generic observations are not acceptable without evidence. If you cannot be specific, note the gap and explain what would be needed to fill it. Mark any claim based on inference rather than direct evidence with [ASSUMED].

STRUCTURE:

SECTION 1 — COMPANY REALITY
What this company actually does, as distinct from how they market themselves. Business model. Revenue stage. Real growth indicators. Founder credibility signals. Key risks or red flags a candidate will encounter.

SECTION 2 — PRODUCT AND TECHNICAL ENVIRONMENT
The engineering reality: tech stack (stated and inferred), team size and structure, build vs. buy philosophy, technical debt indicators, infrastructure approach. What it is actually like to work here as an engineer.

SECTION 3 — TRUE HIRING CONTEXT
Why this role exists now. What triggered the hire. How long the role has been open. What has been tried. Who owns the decision and who influences it. Hard deadlines. What happens if this role goes unfilled.

SECTION 4 — ROLE DECONSTRUCTION
What the role actually involves vs. what the JD says. First 90 days. True must-haves vs. nice-to-haves inflated into requirements. Skills missing from the JD but actually needed. The real reporting line and its implications.

SECTION 5 — COMPETITIVE POSITIONING
Why a candidate would choose this company over its direct competitors for their attention. Where this company wins. Where it loses. What it can offer that alternatives cannot. What it cannot offer that some candidates will demand.

SECTION 6 — MARKET REALITY SUMMARY
Summarise the market reality check findings. Talent pool size, comp benchmarks, competing demand, search difficulty rating. State the realistic funnel.

SECTION 7 — HIRING RISKS AND CONSTRAINTS
Specific risks, not generic ones. For each risk: state what it is, how likely it is to materialise, what the impact would be, and what the recommended mitigation is.

Close with: MANDATE CONFIDENCE: [High / Medium / Low] and a single sentence rationale.

---

**Prompt 5 — Core · Phase 04B — Success profile creation**

Usage note: Creates Document 2 — the most important document in the system. Internal only. Not a skills list — a description of the specific human who will succeed.

Prompt text:
Create the Success Profile. This is Document 2 of 3. It is internal only.

This is not a skills list and it is not a summary of the job description. It is a specific, commercially useful description of the human being who will succeed in this role and why.

QUALITY STANDARD:
If someone reading this could apply it to 50% of senior engineers, it is too generic. The success profile must be specific enough that a researcher could distinguish a strong match from a plausible-but-wrong match within 60 seconds.

PART A — THE PERSON WHO SUCCEEDS

1. ARCHETYPE DESCRIPTION
Describe the career arc of the person who would thrive here. Not a job title. A person type. What have they built? At what scale? In what kind of environment? What decisions have they made that distinguish them?

2. ENVIRONMENT FIT
What kind of engineering cultures produce this person? What environments would produce someone who looks right on paper but would struggle here? Be explicit about both.

3. THE WORK THEY HAVE DONE
Name the specific types of projects, decisions, and outputs that would signal this is the right person. What would you look for in their GitHub, their CV, or their conversation?

4. HOW THEY WORK
Not just what they know, but how they operate. Do they move fast and refactor later, or do they architect first? Are they a builder or a technical leader? Do they thrive in ambiguity or need defined scope?

PART B — MOTIVATION AND MOVEMENT

5. WHY THEY WOULD MOVE
What is missing from their current role that this role provides? What career logic makes this move make sense for them right now?

6. THE STRONGEST HOOK
In one sentence: what is the single most compelling thing about this opportunity for this specific archetype?

7. ANTICIPATED OBJECTIONS
List the top 5 objections this archetype is most likely to raise, in order of likelihood. For each: state the objection, the honest response, and the handling strategy.

8. COMP AND EQUITY EXPECTATIONS
What would this archetype expect? What would attract them? What would repel them? Where does this role sit relative to their expectations?

---

**Prompt 6 — Core · Phase 04C — Search strategy creation**

Usage note: Creates Document 3 — the operational search strategy. Internal only. All recommendations must flow from the intelligence brief and success profile.

Prompt text:
Create the Search Strategy. This is Document 3 of 3. It is internal and operational.

All recommendations must be traceable to the Intelligence Brief or Success Profile. Do not introduce new assumptions here.

PART A — COMPANY TARGET MAPPING

For each category, provide specific company names where possible:

DIRECT TARGETS
Companies where the success profile archetype almost certainly exists. High fit, obvious targets. Explain why each is prioritised.

ADJACENT TARGETS
Companies where the profile could exist with some transfer. Include what you are looking for within these companies.

NON-OBVIOUS TARGETS
Overlooked talent pools that most competitors for this candidate will not be targeting. Explain the non-obvious logic.

AVOID LIST
Types of companies or specific companies that produce profiles that look right but are wrong. Explain the reasoning.

PART B — SOURCING PRIORITISATION

Primary channels and rationale (not just "LinkedIn")
Secondary channels and when to activate them
Within target companies: which profiles to prioritise first and why
What to look for in a profile that signals high potential to convert
What to look for that signals a likely waste of time

PART C — CANDIDATE VALUE PROPOSITION

Primary hook (from success profile): [one sentence]
Secondary positioning angles: [2–3 alternatives for different sub-profiles]
Proof points to deploy: [specific credibility signals to use in outreach]
What NOT to lead with and why

PART D — PIPELINE AND HIRING MATHS

Sourcing target: [N profiles to identify]
Outreach target: [N to contact]
Expected response rate: [%] — rationale
Expected to progress to call: [N]
Expected to submit to client: [N]
Expected to reach offer stage: [N]
Realistic time to fill: [range] — assumptions stated

---

**Prompt 7 — Execution — Outreach by archetype**

Usage note: Generates tailored outreach messages per archetype. Must be run with the full mandate pasted into the same message.

Prompt text:
Using the mandate, generate outreach for the following archetype:

ARCHETYPE TO TARGET: [describe the specific sub-profile — e.g. "senior backend engineer at a Series B fintech, 6–9 years experience, likely considering their next move due to post-Series B engineering scaling pressures"]

CONTEXT FOR THIS MESSAGE:
— Platform: [LinkedIn InMail / email / other]
— Relationship: [cold / warm intro / referral]
— Known information about this specific person: [add any relevant signals from their profile]

For each message variant, state:
— The hook being used and why it fits this archetype
— The tone calibration and why
— What NOT to include in this message and why

Generate 3 variants:

VARIANT A — Lead with mission and problem
For candidates motivated by the problem the company is solving.

VARIANT B — Lead with technical environment
For candidates motivated by engineering quality, autonomy, or craft.

VARIANT C — Lead with career logic
For candidates whose primary motivation is the career move itself.

Each message:
— Subject line (email) or opening line (LinkedIn): max 12 words
— Body: max 100 words
— No generic phrases ("exciting opportunity", "I came across your profile", "would love to connect")
— Must contain at least one specific signal that shows you have looked at their background
— Must have one clear, low-friction call to action

---

**Prompt 8 — Execution — Candidate brief**

Usage note: Generates the candidate-facing document. Not a JD rewrite. A commercial document written for a specific reader.

Prompt text:
Using the mandate, create a candidate brief.

PURPOSE: Shared with candidates who have expressed initial interest. Converts interest into a serious conversation. Not a job description. A commercial document written for a specific reader.

THE READER: [paste archetype description from success profile]

TONE: Honest, specific, commercially credible. No corporate language. No hype.

STRUCTURE:

THE COMPANY (3–4 sentences)
What they actually do. Why it matters. Where they are in their journey. One signal of traction or credibility.

THE ENGINEERING ENVIRONMENT (3–4 sentences)
What it is actually like to work here as an engineer. Stack, team size, autonomy level, technical culture.

THE ROLE (4–5 sentences)
What the person will actually be doing in the first 6–12 months. What they will own. What decisions they will make. What success looks like.

WHY NOW (2–3 sentences)
Why this is the right moment to join. What opportunity or inflection point makes this timing meaningful.

THE OPPORTUNITY (2–3 sentences)
What this role offers that the candidate is unlikely to find elsewhere at this moment in their career.

COMPENSATION (1–2 sentences)
State the range honestly.

THE TEAM (2–3 sentences)
Who they will work with. Specific credibility signals from the hiring manager or founding team.

WHAT HAPPENS NEXT
Clear, low-friction next step.

Do NOT include: generic company descriptions, mission statement language, a list of requirements, HR boilerplate, or anything that reads like it was written for a job board.

---

**Prompt 9 — Execution — Company target lists**

Usage note: Expands target company mapping from the search strategy. Produces structured, prioritised lists with rationale — not just names.

Prompt text:
Using the mandate, generate the full company target list.

For each company listed, provide:
— Company name
— Category: [Direct / Adjacent / Non-obvious]
— Priority: [Tier 1 / Tier 2 / Tier 3]
— Why this company produces the right profile
— Which team or function within the company to target
— Any known signals about openness to move
— One reason a candidate from here might hesitate

FORMAT: Table with columns: Company | Category | Priority | Target team | Why they fit | Openness signal | Likely hesitation

TIER DEFINITIONS:
Tier 1 — Start here. Highest density of the exact profile. Prioritise in week 1.
Tier 2 — Strong secondary targets. Activate in week 2.
Tier 3 — Longer tail. Activate if Tier 1 and 2 are insufficient.

After the table, list:
AVOID — Companies that produce profiles that look right but are wrong, with one-line rationale for each.

Target: 30–50 companies total across all tiers.

---

**Prompt 10 — Execution — Client advisory**

Usage note: Produces the advisory document for the client. Honest assessments, not reassurance. Demonstrates market expertise.

Prompt text:
Using the mandate, produce a client advisory document.

STRUCTURE:

EXECUTIVE SUMMARY
2–3 sentences. Search difficulty, key constraint, and recommended approach.

MARKET ASSESSMENT
What the talent market for this profile actually looks like. Talent pool size. Competing demand. Comp reality vs. client expectations. Be specific with numbers where possible.

TIMELINE FORECAST
Realistic time to fill with assumptions stated. Best case, most likely, and delayed scenario. What would cause each scenario.

HIRING RISKS (specific, not generic)
For each risk:
— The risk
— Likelihood: [Low / Medium / High]
— Impact if it materialises: [Low / Medium / High]
— Recommended mitigation

RECOMMENDED TRADE-OFFS
If the search as scoped has material constraints, recommend specific adjustments. For each trade-off:
— What we recommend relaxing or adjusting
— What we gain by doing so
— What we give up

PROCESS RECOMMENDATIONS
Specific recommendations for how the client should run their process to maximise conversion of strong candidates. Include: response speed, interview structure, feedback loops, offer timing.

COMP RECOMMENDATIONS
Specific salary and equity recommendation with market rationale. If the current range will cause problems, say so directly.

Close with: ONE THING — the single most important action the client can take right now to improve search outcomes.

---

**Prompt 11 — Execution — Mandate re-audit (mid-search)**

Usage note: Use when a search stalls, the client changes the brief, or market data contradicts the mandate. Paste current mandate plus this prompt.

Prompt text:
We are [X weeks] into this search. Trigger a mandate re-audit.

CURRENT STATUS:
— Candidates identified: [N]
— Outreach sent: [N]
— Response rate: [%]
— Progressed to call: [N]
— Submitted to client: [N]
— Rejected at what stage: [detail]
— Current blockers: [describe]

NEW INFORMATION SINCE MANDATE V[X]:
[Paste any new inputs: client spec changes, candidate feedback, comp learnings, market signals, hiring manager changes, etc.]

RE-AUDIT TASKS:
1. Assess whether the original success profile is still accurate given search data
2. Identify which assumptions in the mandate have been proven wrong
3. Identify which target company categories are performing and which are not
4. Assess whether the outreach positioning is landing or failing
5. Identify the single most likely cause of current performance
6. Recommend specific changes to: [success profile / target list / outreach / comp advice / client process]
7. Update mandate confidence rating

Output: a revised mandate section or a list of specific changes to make to each document, with rationale.

---

## Tab 5 — Failure modes

Show a table with columns: Failure mode | Risk | Early signal | Catch it by

Rows:

1. Polished-but-shallow mandate. Looks complete, built on inference. | High | No specific salary ranges, no named companies, no concrete talent pool estimate | Apply the quality standard before proceeding: every section must have one specific, concrete claim

2. Generic success profile. Could describe half the market. | High | Profile reads as a skills list rather than a person description | 60-second test: can a researcher distinguish a strong match from a plausible-but-wrong match?

3. Phantom candidate. Searching for someone who doesn't exist at the expected comp. | High | Low response rates despite high outreach volume | Market reality check before mandate creation. Flag comp gaps to client before executing.

4. Client drift. Brief changes but mandate does not update. | Medium | Client starts rejecting candidates they should like | Trigger re-audit whenever client spec changes. Version the mandate.

5. Context loss between sessions. Prompts start from scratch. | Medium | AI output is inconsistent with earlier mandate sections | Paste the mandate into every execution prompt. Never assume context carries.

6. Outreach not differentiated by archetype. One message to everyone. | Medium | Low response rate across all profiles | Use the archetype outreach prompt. Generate 3 variants per sub-profile.

7. No client validation of success profile. Executing against your interpretation. | Medium | Good candidates rejected without clear rationale | Phase 05 gate — do not begin sourcing until client confirms the success profile.

8. No feedback loop. Search data does not update the mandate. | Low–Med | Search stalls and strategy does not adjust | Re-audit trigger at 2 weeks stall. Capture objections and comp data back into mandate.

Risk levels: High = dark red badge, Medium = amber badge, Low–Med = green badge.

Below the table, show a highlighted note box:
Label: The most dangerous output
Text: A mandate that is well-structured but built on assumptions will produce confident-sounding work that leads to bad decisions. Claude will not flag this unprompted. You must apply the quality standard at Phase 04 and look for generic language as the primary warning signal.

---

## Tab 6 — Alternatives

Show three alternative model cards, each with a title, description, flow diagram (nodes with arrows), and usage guidance.

**Alternative A — The two-document model (already integrated)**
Description: Separates factual intelligence from strategic direction. Intelligence Brief is client-shareable; Search Strategy is internal. This system already uses this model.
Flow: Inputs → Intelligence Brief (factual) → Search Strategy (directional) → Execution
Usage: Use when: always. This is the baseline architecture.

**Alternative B — Candidate-first model**
Description: For hard-to-fill technical roles where the talent market, not the job description, defines what is actually possible. Start with the specific person, work backwards to the search strategy. The mandate becomes a person description first and a company description second.
Flow: Define the archetype → Map where they exist → Build company intelligence → Validate against role
Usage: Use when: the role is highly specialised, or when previous searches have failed because they started from the JD rather than the market.

**Alternative C — Lean mandate (time-constrained)**
Description: When speed pressure collapses Phases 1–3 into a single session. A deliberate, simplified version of the full mandate. Lower confidence, clearly labelled. Better than a rushed full mandate that looks complete but is not.
Flow: MVI check (15 min) → Rapid audit (20 min) → Lean brief (30 min) → Execute + update
Usage: Use when: client needs output within 24 hours. Set mandate confidence to LOW and plan a re-audit within 5 days.
Note box — Lean mandate minimum: Even in a lean mandate: success profile must be specific, comp reality must be stated, and at least 10 direct target companies must be named. These three elements are non-negotiable regardless of time pressure.

---

Build the complete tool now as a single self-contained HTML file. All six tabs fully functional. All prompts copyable. All checklists interactive. Output the full HTML.
