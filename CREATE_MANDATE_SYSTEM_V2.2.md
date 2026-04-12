# CREATE_MANDATE_SYSTEM_V2.2.md
## Rebuild prompt — paste into Claude to recreate the Mandate Intelligence System from scratch

---

Paste the following into a fresh Claude session to rebuild the complete Mandate Intelligence System v2.2 interactive tool.

---

Build me a single-file HTML tool called the Mandate Intelligence System v2.2.

It is an interactive reference system for a specialist tech/engineering search firm running intelligence-led hiring mandates. The tool lives at index.html, requires no dependencies or server, and works offline.

## Design

Clean, minimal, professional. Use these Google Fonts: DM Sans (body), Cormorant Garamond (headings), DM Mono (labels, tags, prompt text). Support light and dark mode via CSS prefers-color-scheme. No frameworks.

Colour palette (light mode):
- --ink: #1a1a18
- --muted: #6b6b67
- --hint: #a8a8a2
- --surface: #fafaf8
- --raised: #f2f2ee
- --border: rgba(0,0,0,0.08)
- Section A accent: #e8f0fb / #1a3a6b / #b8ccf0
- Section B accent: #fef3e2 / #7a4000 / #f0c878
- Section C accent: #eaf5ee / #1a5c2a / #90d0a0
- Section D accent: #f5eafa / #5a1a7a / #c890e8

## Structure

Six tabs: Overview · Stages · Brief structure · Prompt library · Failure modes · Design rationale

Version badge in header: V 2.2

---

## Tab 1 — Overview

Show:
- System architecture flow: Stage 1 Build → Input collection → Input audit → Master Intelligence Brief → Stage 2 Execute → Query prompts → Ephemeral outputs
- Four core principles grid (2x2): One source of truth · Understanding before outputs · Structured not a blob · Ephemeral outputs
- Four brief section cards (2x2) with section colour coding: A Factual context · B Interpreted hiring understanding · C Search logic (exhaustive company list, self-audit, CVP, funnel, failure scenarios) · D Confidence and gaps
- Brief quality gate (blue accent box) — 9 items all required before Stage 2
- Minimum viable inputs — three cards: Non-negotiable 7 · Secondary best effort · Gap protocol
- Output map grid: Client-facing · Internal operational

Brief quality gate items:
1. Section A contains specific comp range, named investors, confirmed tech stack
2. Section B success profile passes the 60-second test
3. Section B contains the strongest hook in one sentence
4. Section C contains a meaningful, exhaustive company target list — each scored and ranked
5. Section C contains an explicit CVP statement (one sentence)
6. Section C contains stated funnel assumptions
7. Section C contains at least one failure scenario
8. Section D confidence rating is set and minimum 3 inferences are named
9. Client has confirmed Section B success profile before sourcing begins

---

## Tab 2 — Stages

Grid of 11 clickable stage cards. Each expands a detail panel below with description, interactive checklist, and a gate note.

Stages:
- Stage 1 · Step 1: Input collection
- Stage 1 · Step 2: Input audit
- Stage 1 · Step 3: Brief creation (full brief, one prompt)
- Stage 2 · Execute: Market reality check
- Stage 2 · Execute: Success profile
- Stage 2 · Execute: Search strategy + targets
- Stage 2 · Execute: Outreach by archetype
- Stage 2 · Execute: Client advisory
- Stage 2 · Capture: Intelligence capture
- Stage 2 · Maintain: Brief re-audit
- Stage 2 · Close: End-of-search debrief

Step 3 note: One prompt builds the full brief. Claude flags Section B for client validation mid-output. That conversation happens outside the session. No two-pass split.

Search strategy note: Exhaustive coverage self-audit — not a hard number. Goal is every meaningful pocket represented including non-obvious ones.

Re-audit gate note: Hard decision triggers — Response rate below 10% after 30 outreach → reposition · Zero to call after 2 weeks → re-audit · 3+ unexplained client rejections → re-validate Section B · 2+ comp objections → escalate to client · Hiring manager changes → re-audit Section A

---

## Tab 3 — Brief structure

Four expandable section panels, each in their accent colour. Click to expand.

Section A — Factual context: company reality, business model, funding, tech stack, team size, role as stated, comp range, location, timeline
Section B — Interpreted hiring understanding: true hiring context, role deconstruction, success profile archetype, motivators, strongest hook (mandatory), top 5 objections, competitive positioning, client-side risks
Section C — Search logic: exhaustive named company list scored and ranked, coverage self-audit (what pools have I missed?), CVP statement, funnel assumptions, failure scenario, avoid list, sourcing channels, within-company targeting
Section D — Confidence and gaps: CONFIRMED / INFERRED (min 3, risk-rated) / UNKNOWN, brief confidence rating, highest risk gap, hard decision triggers (list all 5), version history

Brief discipline rules footer note.

---

## Tab 4 — Prompt library

12 prompts total. Organised by section labels: Stage 1 Build · Stage 2 Execute · Maintain · Close

Each prompt is a collapsible card showing: tag label · title · section pills · chevron. Expanded state shows: pnote (context) · draws (which sections it anchors in) · monospaced prompt text · Copy button (copies text to clipboard, shows "Copied" confirmation).

Tag styles:
- Core prompts: dark filled tag (tag-core)
- Execute prompts: raised background (tag-exec)
- Capture/Debrief: green accent (tag-new)

### p1 — Session starter (Core · Step 1)
Anchors: A B C D
Opens every mandate session. Constraint-based rules. Tracks 7 MVIs. Do not interpret or summarise inputs. Categorise as [Company][Role][People][Market][Context][Other]. List MVIs still missing after each input.

MVIs: Company website · Job description · Hiring manager LinkedIn · 2+ engineer LinkedIn profiles · Funding stage and amount · Intake call notes · Comp range

### p2 — Input audit (Core · Step 2)
Anchors: A B C D
Completeness assessment · Conflict detection · Assumption audit with risk ratings · Up to 10 targeted questions (RISK AREA / QUESTION / WHY IT MATTERS) · Up to 5 hiring risk flags · Brief confidence forecast [High/Medium/Low]. Do not begin brief creation. Wait for answers.

### p3 — Brief creation (Core · Step 3)
Anchors: A B C D
One prompt. Full brief. Quality standard: specific and concrete, mark inferences [ASSUMED].

Section A: facts only — company reality, tech environment, funding, role as stated, hiring context facts

Section B: interpretation only — true hiring context, role deconstruction, success profile archetype, motivators, strongest hook (mandatory one sentence), top 5 objections with handling, competitive positioning, client-side risks. After Section B insert: "── VALIDATION FLAG: Share the success profile above with your client before sourcing begins. Confirm they agree with who you are looking for. This is a conversation outside this session. ──" Then continue.

Section C: exhaustive named companies. Goal is coverage not a number. Tiers: Tier 1 Direct Targets (where archetype almost certainly exists, ranked by priority, start week 1) · Tier 2 Adjacent Targets (transferable experience, ranked, activate week 2) · Tier 3 Non-obvious Targets (overlooked pools, explain non-obvious logic each). Avoid list with rationale. Then COVERAGE SELF-AUDIT: What talent pools have I missed? What non-obvious backgrounds not yet in this list? Adjacent industries, stages, functions not represented? Add genuine gaps or state exhaustive. CVP Statement. Sourcing prioritisation. Funnel assumptions. Failure scenario.

For each company: Name | Tier | Priority rank | Match score (1–10) | Why this produces the right profile | Which team to target | Openness signal | Likely hesitation

Match score guide: 9–10 near-perfect · 7–8 strong · 5–6 adjacent · 3–4 speculative

Section D: CONFIRMED / INFERRED (min 3, risk-rated Low/Medium/High) / UNKNOWN / Brief confidence / Highest risk gap / Decision triggers (all 5) / Version v1.0 [date]. After Section D confirm all 9 quality gate items met before Stage 2.

### p4 — Market reality check (Execute)
Anchors: A B C D
Talent pool size (order of magnitude) · Compensation reality vs Section A range · Competing demand rating · Notice and availability · Funnel estimate (5 numbers) · Search difficulty rating. If material gap between client expectations and market reality, state what to tell client. Close: THREE ACTIONS (48 hours) · ONE THING TO STOP · ONE EXPERIMENT (next week).

### p5 — Success profile (Execute)
Anchors: A B C D
60-second test mandatory. Part A: Archetype description (career arc not job title) · Environment fit (thrives in / fails in) · The work they have done · How they work. Part B: Why they would move · Strongest hook (one sentence) · Top 5 objections (objection / honest response / handling) · Comp and equity expectations. Flag elements resting on Section D inferences.

### p6 — Search strategy (Execute)
Anchors: A B C D
Exhaustive named company list — coverage not a number. Same tier structure and per-company columns as p3. Coverage self-audit after all tiers. CVP statement. Sourcing prioritisation. Pipeline forecast. Failure scenario. Close: THREE ACTIONS · ONE THING TO STOP · ONE EXPERIMENT.

### p7 — Outreach by archetype (Execute)
Anchors: A B C D
Run per archetype. Specify: archetype to target · platform · relationship · known signals. Three variants: Variant A (mission/problem hook) · Variant B (technical environment hook) · Variant C (career logic hook). Each: subject/opening max 12 words · body max 100 words · zero generic phrases · one specific signal · one low-friction CTA.

### p8 — Candidate brief (Execute)
Anchors: A B C D
Not a JD rewrite. Reader = Section B archetype. Sections: The company (3–4 sentences) · Engineering environment (3–4) · The role (4–5) · Why now (2–3) · The opportunity (2–3) · Compensation (1–2) · The team (2–3) · What happens next. No generic descriptions, mission statement language, requirements list, HR boilerplate.

### p9 — Client advisory (Execute)
Anchors: A B C D
Executive summary · Market assessment with numbers · Timeline forecast (best/likely/delayed) · Hiring risks (risk / likelihood / impact / mitigation) · Recommended trade-offs · Process recommendations · Comp recommendation. Close: ONE THING (single most important action client can take right now).

### p10 — Intelligence capture (Capture)
Anchors: A B C D
Paste any raw signal. Steps: 1 Signal classification (source / format / reliability / completeness) · 2 Signal interpretation (2–3 sentences, flag ambiguities) · 3 Proposed brief updates — ONE DELTA AT A TIME in formatted box: "PROPOSED CHANGE — SECTION [X] / [change description] / Confirm to accept, or tell me why you are rejecting it." Wait for confirmation before next delta. 4 Section D update · 5 Downstream flags · 6 Version recommendation (colour only → hold / refines B → v[X.X] / material B or C change → v[X.1] / contradicts A or shifts profile → v[X+1.0] flag loudly).

### p11 — Brief re-audit (Maintain)
Anchors: A B C D
State trigger. Provide search data: candidates / outreach / response rate / progressed / submitted / rejections / objections / comp expectations / which companies produced conversations / blockers. Re-audit tasks: confirm/correct Section A · validate/update Section B · assess Section C performance · identify best/worst outreach · single most likely cause · specific edits per section · update Section D · update triggers · update confidence. Output: section-by-section change list, new version. Close: THREE ACTIONS · ONE THING TO STOP · ONE EXPERIMENT.

### p12 — End-of-search debrief (Debrief)
State outcome. Provide: time / offers / submitted / outreach / response rate. Sections: Section A accuracy · Section B accuracy (interpretations right vs wrong, real motivators vs predicted) · Section C performance (which companies produced conversations, best outreach variant) · Intelligence capture surprises · Section D gaps that mattered · What would change if starting again · ONE THING for the next mandate.

---

## Tab 5 — Failure modes

Table with four columns: Failure mode · Risk · Early signal · Prevention / Trigger

Rows:
1. Brief quality gate not enforced | High | Researcher has no starting point | Gate mandatory, all 9 items, no exceptions
2. Section C generic — categories not named organisations, stops at obvious names | High | Nothing actionable | Coverage self-audit mandatory, named companies only, scored and ranked
3. Section D thin or absent | High | Brief reads confident throughout | Mandatory, min 3 inferences, every B interpretation needs D entry
4. Generic success profile, fails 60-second test | High | Poor response rates across all profiles | 60-second test before any execution
5. Full brief not pasted into execution sessions | High | Outputs contradict brief | Non-negotiable, Claude has no memory between chats
6. Intelligence capture absorbs signal passively | Medium | Brief drifts, operator can't recall changes | One delta at a time, explicit confirmation
7. Search continues past hard decision triggers | Medium | Response rate below 10% for 2 weeks, no action | Hard triggers in Section D, checked actively
8. Client never validates success profile | Medium | Strong candidates rejected inconsistently | Validation flag in Step 3 brief output
9. Outreach not differentiated by archetype | Medium | Uniform low response rate | Per-archetype prompt, three variants per run
10. No end-of-search debrief | Low–Med | Same mistakes on next mandate | Debrief at close regardless of outcome

Primary warning signal footer: Generic language anywhere in the brief is the most reliable indicator of a problem.

Hard decision triggers warning box: Response rate below 10% after 30 outreach → reposition · Zero to call after 2 weeks → re-audit · 3+ unexplained rejections → re-validate Section B · 2+ comp objections → escalate to client · Hiring manager changes → re-audit Section A

---

## Tab 6 — Design rationale

Seven rationale cards with serif heading and body text:

1. From v1 to v2 — the core architecture change: V1 = four phases, three documents, prone to drift. V2 = two stages, one canonical brief, four sections, ephemeral outputs.

2. v2.2 — two changes from v2.1: Step 3 collapsed into one prompt — client validation still happens, flagged in brief output, just not a structural gate splitting the prompt library. Section C "50+" replaced with coverage self-audit — produces better companies than counting does.

3. Why Section C uses a coverage self-audit, not a hard number: Hard minimum risks padding — Claude hits the number with weak companies. Self-audit forces Claude to look for what it missed. Exhaustive beats countable for markets like London.

4. Why intelligence capture requires confirmation, not passive absorption: Without decision layer, every signal absorbed whether it deserves to be. A candidate who passed for personal reasons can corrupt Section B. One delta at a time keeps operator in control during live search.

5. Why hard decision triggers are in Section D: Without triggers, stalled searches continue because stalled is undefined. Triggers set when brief is built — before live search pressure makes them easy to ignore.

6. Why execution closes with 3 actions, 1 stop, 1 experiment: Analysis without action is expensive thinking. Every strategic prompt converts intelligence into operational momentum.

7. The lean path: Under time pressure — Steps 1+2 + Sections A+B (full) + C-lite (10 named Tier 1 companies, one CVP, one funnel assumption) + D-lite (top 3 unknowns, confidence rating, key risk). Set confidence Low, full re-audit within 5 days. Section D never optional even lean. Show flow diagram: Step 1+2 → Sections A+B → C-lite + D-lite → Execute → Full C+D within 5 days.

---

## JavaScript behaviours

- showTab(id, btn): switches active tab
- togglePhase(id): expands one stage detail panel at a time, collapses others, scrolls into view
- toggleBrief(id): toggles brief section panels
- togglePrompt(card): expands one prompt at a time, collapses others
- toggleChk(icon): toggles checkbox on/off with ✓ mark
- copyText(id, btn, e): copies prompt text to clipboard, shows "Copied" with green border for 1.8s

---

Build the complete file. Single HTML file. No external dependencies except the Google Fonts link. All CSS inline in style tag. All JS inline in script tag at bottom. Version badge shows V 2.2.
