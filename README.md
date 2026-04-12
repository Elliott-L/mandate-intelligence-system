# Mandate Intelligence System

An intelligence-led hiring search system for tech/engineering roles at startups. Built to move from reactive, JD-driven search to a deliberate, structured model where AI acts as a reasoning and execution layer.

---

## What this is

A complete operational system for running high-quality hiring searches. It replaces ad hoc prompting with a repeatable, phased workflow built around a central asset — the **Mandate Intelligence Brief** — from which all search outputs are generated.

The system was designed with the following principles:

- Extract once, reuse repeatedly
- Separate raw data from structured thinking
- Reasoning before generation — no premature summarisation
- Mandate is the core asset; chats are disposable
- Prioritise hiring reality over surface-level information

---

## Files

| File | Description |
|------|-------------|
| `mandate_intelligence_system.html` | The full interactive system — open in any browser |
| `README.md` | This file |

---

## How to open

Download `mandate_intelligence_system.html` and open it in any browser. No internet connection required after download. Works in Chrome, Firefox, Safari, and Edge.

---

## System overview

The system is organised into six tabs:

### 1. Overview
Architecture diagram, core principles, minimum viable inputs (MVIs), and output map. Start here before any new mandate.

### 2. Phases
Seven workflow phases with interactive checklists and phase gates:
- Phase 01 — Input collection
- Phase 02 — Input audit
- Phase 03 — Market reality check
- Phase 04 — Mandate creation (three documents)
- Phase 05 — Client validation
- Phase 06 — Execution
- Phase 07 — Feedback loop

### 3. Mandate structure
The full three-document model:
- **Intelligence Brief** — factual, client-shareable (7 sections)
- **Success Profile** — internal, standalone
- **Search Strategy** — internal, operational

### 4. Prompt library
Nine prompts with copy buttons, ready to paste into Claude:
- Session starter (Phase 01)
- Input audit (Phase 02)
- Market reality check (Phase 03)
- Intelligence brief creation (Phase 04A)
- Success profile creation (Phase 04B)
- Search strategy creation (Phase 04C)
- Outreach by archetype
- Candidate brief
- Company target lists
- Client advisory
- Mandate re-audit (mid-search)

### 5. Failure modes
Eight failure modes with risk ratings, early warning signals, and catch mechanisms.

### 6. Alternatives
Three alternative configurations for different situations:
- Two-document model (default)
- Candidate-first model (for rare/senior roles)
- Lean mandate (for time-constrained searches)

---

## How to run this in Claude

### Session 1 — Build the mandate

1. Open a fresh Claude chat
2. Paste the **Session Starter** prompt from the Prompt Library tab
3. Feed in your inputs one by one (JD, LinkedIn profiles, intake notes, company URL, observations)
4. When inputs are complete, paste the **Input Audit** prompt and answer the questions
5. Run the **Market Reality Check** prompt
6. Run the three mandate creation prompts back to back (04A, 04B, 04C)
7. Copy the full mandate output and save it — Notion, Google Doc, wherever you work

### Session 2+ — Execution

Open a new Claude chat and start every execution session with:

> Here is the mandate for [Company / Role]. [Paste full mandate text.] Using this mandate, [paste whichever execution prompt you need].

Run one execution session per output type for cleanest results.

### The one rule

**Never run an execution prompt without the mandate in the same message.** Claude has no memory between chats. Paste the mandate every time.

---

## Minimum viable inputs

Before mandate creation, you need all seven of these:

1. Company website (product, about, careers pages)
2. Job description or role brief
3. Hiring manager LinkedIn profile
4. At least 2 engineer LinkedIn profiles from the company
5. Funding stage and amount
6. Intake call notes or direct client conversation
7. Comp range (or explicit acknowledgement it is unknown)

If any are missing: flag the gap, note it in the mandate, set confidence to Low, and plan a re-audit once filled.

---

## Mandate versioning

Version your mandate document every time it is updated:

- `v1.0` — initial mandate, post client validation
- `v1.1` — minor update (spec clarification, comp adjustment)
- `v2.0` — significant change (success profile revised, hiring manager changed)

Trigger a full re-audit if: search stalls for 2+ weeks · client changes spec · comp reality diverges significantly · hiring manager changes · company raises or pivots.

---

## Re-generating this system

If you need a fresh copy of the HTML tool, return to the original Claude conversation or paste the system document into a new Claude chat and ask it to rebuild the interactive tool.

---

## Tooling

- **Claude** — reasoning, mandate creation, all structured outputs
- **ChatGPT** (optional) — scaling outreach messages, formatting variation
- This HTML file — operational reference during live searches

---

*Built with Claude · Mandate Intelligence System v1.0*
