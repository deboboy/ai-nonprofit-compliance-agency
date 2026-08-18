# Compliance Practice Delivery Stack
**AI-leveraged compliance office for small nonprofits · scaffold v1 · July 2026**

Template/prompt/checklist library that lets 1 senior consultant + agents run 20–40 nonprofit clients. **This is the operational backbone of the GTM plan** (`../gtm-ai-compliance-nonprofits-2026-07.md`).

---

## Operating model (read this first)

```
Client intake (scorecard / diagnostic)   →  intake/            → human confirms fit
        ↓
Readiness Assessment (wedge deliverable)  →  assessments/       → human signs report
        ↓
Retainer: policies + evidence + answers  →  policies/, evidence/, questionnaires/
        ↓
Frameworks & grant knowledge             →  references/        → updated quarterly
        ↓
ALL client-facing output                 →  qa/ gate: human review + sign-off BEFORE delivery
```

**Non-negotiable rules:**
1. **Humans sign everything.** No client-facing deliverable ships without a named human reviewer. Agents draft; humans own.
2. **We advise, we never certify.** Engagement letters disclaim certification authority (see `qa/engagement-letter-language.md`). 3PAOs/CPAs certify.
3. **Evidence must be real.** Never fabricate screenshots, dates, or controls evidence. If evidence doesn't exist, the deliverable says "gap."
4. **Every invoice maps to a grant.** Deliverables ship with a grant-justification memo (`references/grant-justification-memo.md`).
5. **No CUI in prompts.** Client data stays in client workspace; agents never get raw CUI/PII when a template or aggregation will do.

---

## Directory map

| Path | Contents |
|---|---|
| `intake/` | Scorecard, qualification checklist, diagnostic call script |
| `assessments/` | Readiness assessment report template + writing guide |
| `policies/` | Policy library skeleton (NIST 800-171 / SOC 2 aligned), policy generation brief |
| `evidence/` | Evidence collection matrix, monthly cadence, collection checklist |
| `questionnaires/` | Funder security questionnaire answer bank + response workflow |
| `prompts/` | Agent prompt library (intake triage, gap analysis, policy draft, questionnaire, vendor verify, board deck) |
| `references/` | Grant-justification memo, funder security terms decoder, framework crosswalk, state RAMP map, vendor verification guide |
| `qa/` | Human review checklist, engagement letter language, delivery KPIs |

---

## Quick start (first client, first 2 weeks)

1. Run the Scorecard (`intake/scorecard.md`) → qualify with `intake/qualification-checklist.md`.
2. Kick off assessment with `prompts/01-intake-triage.md` and `prompts/02-gap-analysis.md`.
3. Draft report from `assessments/report-template.md`; write from `assessments/writing-guide.md`.
4. Pass through `qa/review-checklist.md`; sign; deliver with grant memo.
5. Convert to retainer → stand up `evidence/collection-matrix.md`, deploy policy library (`policies/`), load questionnaire bank (`questionnaires/answer-bank.md`).

## Maintenance

- **Quarterly:** update `references/state-ramp-map.md` and `references/framework-crosswalk.md` (GovRAMP 2026 modernization; FedRAMP 20x rules; CMMC timeline).
- **Per audit cycle:** append real controls evidence patterns to `evidence/collection-matrix.md`.
- **Per client:** add anonymized lessons to the relevant template — never to a client file.
