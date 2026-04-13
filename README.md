# Mandate Intelligence System — v2.2

Intelligence-led hiring search for tech/engineering roles. One canonical brief. Query-based execution. Continuous intelligence capture.

---

## What it is

A repeatable AI-powered workflow for executing high-quality hiring searches. Built around a single Master Intelligence Brief — the permanent source of truth for each mandate. All execution outputs (outreach, candidate briefs, client advisories, market checks) are generated on demand by querying the brief. Nothing drifts. One thing to maintain.

---

## How it works

**Stage 1 — Build**
Three steps: input collection → input audit → brief creation. Output is one complete Master Intelligence Brief versioned and quality-gated before any sourcing begins.

**Stage 2 — Execute**
Query-based. Paste the full brief into any execution prompt. Outputs are ephemeral — regenerate whenever the brief updates.

---

## The Master Intelligence Brief

Four internal sections:

| Section | Contents |
|---------|----------|
| A — Factual context | Confirmed, verifiable facts only. Company, role, team, comp, funding. No interpretation. |
| B — Interpreted hiring understanding | Reasoned interpretation: success profile, motivators, objections, risks, competitive positioning. |
| C — Search logic | Exhaustive named company list, scored and ranked. CVP. Funnel assumptions. Failure scenarios. Coverage self-audit required. |
| D — Confidence and gaps | Confirmed vs. inferred vs. unknown. Hard decision triggers. Version history. Never thin. |

---

## Prompt library (12 prompts)

**Stage 1 — Build**
- p1: Session starter — input collection
- p2: Input audit — gap analysis and challenge
- p3: Brief creation — full Master Intelligence Brief (one prompt, all four sections)

**Stage 2 — Execute**
- p4: Market reality check
- p5: Success profile
- p6: Search strategy — exhaustive company target list, scored and ranked
- p7: Outreach by archetype
- p8: Candidate brief
- p9: Client advisory

**Maintain**
- p10: Intelligence capture — paste anything, confirm each delta
- p11: Brief re-audit — triggered by hard decision triggers

**Close**
- p12: End-of-search debrief

---

## Brief quality gate

All 9 items must be confirmed before Stage 2 begins:

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

## Hard decision triggers (Section D of every brief)

- Response rate below 10% after 30 outreach messages → reposition outreach before continuing
- Zero candidates to call after 2 weeks → trigger re-audit immediately
- Client rejects 3+ candidates without clear rationale → re-validate Section B before proceeding
- Comp objection from 2+ candidates → escalate to client before continuing
- Hiring manager changes → re-audit and re-validate Section A

---

## Version history

**v2.2** — Collapsed Step 3 into one prompt (removed two-pass structure). Replaced "50+ companies" hard minimum with coverage self-audit mechanic in Section C and p6.

**v2.1** — Two-pass brief creation. Intelligence capture redesigned with explicit per-delta confirmation. Hard decision triggers added to Section D. Action close on all strategic prompts. End-of-search debrief added. Brief quality gate formalised.

**v2.0** — Single canonical brief replacing three separate documents. Two-stage architecture. Ephemeral outputs. Section D as mandatory honesty layer.

**v1.0** — Four sequential phases, three separate documents. Deprecated.

---

## Design principles

**One source of truth** — One brief per mandate. All outputs queried from it.

**Understanding before outputs** — Market reality and success profile are derived from the brief, not prerequisites to building it.

**Full brief always in scope** — Section tags anchor reasoning, not restrict it.

**Exhaustive beats countable** — Section C requires a coverage self-audit, not a hard number. Every meaningful pocket of relevant experience represented, including the non-obvious ones.

**No passive absorption** — Intelligence capture requires explicit confirmation per proposed delta.

**Honest by design** — Section D is never optional. Decision triggers set before live search pressure makes them easy to ignore.

---

## Usage

Open `index.html` in any browser. No dependencies. No server required. Works offline.

Hosted at: `https://Elliott-L.github.io/mandate-intelligence-system`
