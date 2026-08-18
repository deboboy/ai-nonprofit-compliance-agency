# Grant Security Scorecard (gated lead magnet + intake)
**Purpose:** 10-question self-assessment that scores a nonprofit's grant-security risk. Qualifies leads, generates the diagnostic call, and feeds the intake triage prompt.

## The 10 questions (score 0–2 each; max 20)

| # | Question | 0 | 1 | 2 |
|---|---|---|---|---|
| 1 | Do you hold federal grants or contracts (direct or pass-through)? | No | Indirect only | Yes, direct |
| 2 | Do any funders require a security attestation or questionnaire today? | No | Some/verbal | Yes, written |
| 3 | Do you handle Controlled Unclassified Information (CUI) or beneficiary PII? | No | Some PII | CUI/PII at scale |
| 4 | Do you have written security policies (access, incident response, training)? | No | Partial | Yes, current |
| 5 | Who owns security? | No one | IT staff by accident | Named person |
| 6 | Is multi-factor authentication enforced on all accounts? | No | Partially | Yes |
| 7 | Do you know the security status (FedRAMP/GovRAMP/SOC 2) of your top 10 vendors? | No | Some | Yes |
| 8 | Have you had a funder or partner require a vendor security review in the last 12 months? | No | Once | Repeatedly |
| 9 | Do you have an incident response plan tested in the last 12 months? | No | Written only | Tested |
| 10 | Could you produce an evidence pack (logs, training records, access reviews) in 2 weeks? | No | Mostly | Yes |

## Scoring bands

| Score | Band | Outcome |
|---|---|---|
| 0–6 | **Low exposure** | Nurture: newsletter + "when you get your first federal grant" guide. No sales call. |
| 7–13 | **Emerging risk** | Invite to $500 Funded-Security Review diagnostic. Primary conversion target. |
| 14–20 | **At risk now** | Priority: direct call this week. One missed attestation can stall a renewal. |

## What the scorecard is NOT
- Not a compliance assessment (say so on the page).
- Not a security audit.
- No CUI/PII collected at this stage — email + org name + answers only.

## Conversion flow
Scorecard submit → auto-score → email result + CTA ("Book a 20-min Funded-Security Review") → `intake/qualification-checklist.md` → diagnostic call (`intake/diagnostic-call-script.md`).
