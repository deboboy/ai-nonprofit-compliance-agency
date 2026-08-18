# Agent Prompt Library
**Six prompts = the AI-leveraged delivery engine.** Each prompt is a complete, self-contained brief for an agent run. Rules that apply to all:

- Agents **draft only**; a named human reviews and signs every output (see `qa/review-checklist.md`).
- Never fabricate evidence, dates, or client facts. Unknown = gap.
- Never process raw CUI/PII when a category, count, or template suffices.
- Output language: plain English, nonprofit-audience, audit-safe (no "certified/compliant" claims).

---

## 01 — Intake Triage
**Input:** qualification checklist output (`intake/qualification-checklist.md` §E)
**Task:** Produce a 1-page client brief for the founder.
**Output structure:**
1. Org snapshot: name, sector, budget band, staff count, IT stack.
2. Trigger & deadline: verbatim funder clause/letter, deadline date, award value at risk.
3. Applicability first-pass: which frameworks likely apply (800-171/CMMC, SOC 2, state RAMP, HIPAA) and *why* — cite the trigger.
4. Recommended engagement: assessment tier ($3.5K/$4.5K/$6.5K by scope), timeline to funder deadline.
5. Risks: anything that could disqualify (anti-persona flags), anything funder-hostile (unverifiable claims, expired certificates).
6. Open questions for the human before the diagnostic call.

---

## 02 — Gap Analysis
**Input:** client stack description, funder inventory, applicable frameworks (from 01)
**Task:** Draft the §4 gap-analysis table of the Readiness Assessment.
**Output structure:** Control area × [requirement | current state (only what's evidenced) | gap | evidence seen? | priority]. Priorities: P0 = funder-blocking, P1 = within 90 days, P2 = within 12 months. Cite the specific framework control (e.g., 800-171 3.1.1; SOC 2 CC6.1) and the specific client tool/process. No inventing "current state" — mark "not verified" as a gap.

---

## 03 — Policy Draft
**Input:** policy name (from `policies/library-skeleton.md`), client org facts, applicable frameworks
**Task:** Draft one policy per the template structure.
**Rules:**
- Match org size/tools — no enterprise boilerplate for a 40-person nonprofit.
- Every policy statement maps to a control family (see library-skeleton mapping).
- Include the exceptions process and review cadence (annual).
- Output: full policy doc ready for human tailoring; flag any clause that needs client-specific facts (owner names, retention periods, tool names) as `[TO CONFIRM]`.

---

## 04 — Questionnaire Response
**Input:** funder questionnaire (PDF/Word), client's policy library + evidence vault index
**Task:** Draft answers using the answer bank (`questionnaires/answer-bank.md`).
**Rules:** Answer only what's asked; quote the client's actual policy/evidence; never claim compliance without attestation backing; flag any question whose honest answer is a gap → escalate to human (this may be a go/no-go decision). Output: answer-by-answer draft + evidence pack list + escalation notes.

---

## 05 — Vendor Verification
**Input:** client's vendor list + data roles
**Task:** Produce the §5 vendor table.
**Method:** For each vendor check — FedRAMP marketplace (fedramp.gov), GovRAMP participating list (govramp.org), vendor SOC 2 reports/Trust Center, plus `references/state-ramp-map.md` and `references/vendor-verification-guide.md`.
**Output:** vendor | data role | FedRAMP status | GovRAMP status | SOC 2 | verification date | risk | action. Statuses limited to: AUTHORIZED / IN-PROCESS / NOT-FOUND / N/A. "NOT-FOUND" is a finding, not a failure. Flag any vendor that is a P0 data custodian but unverifiable → human call.

---

## 06 — Board Deck
**Input:** posture snapshot, quarter's evidence summary, incidents (or none), upcoming funder deadlines
**Task:** Draft the quarterly board-ready deck (5 slides).
**Slides:** 1) Where we stand (posture score + trend), 2) What we're protecting (award value), 3) What happened this quarter (incidents/evidence), 4) What's next (deadlines, funding), 5) What we need (decisions/budget).
**Rules:** Executive-audience, no jargon without gloss, risks phrased as "exposure on [award]" not "non-compliance." Never present unverified claims as fact.
