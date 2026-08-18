# Readiness Assessment — Report Template
**Deliverable for the $3,500–$6,500 wedge product · human signs page 1.**

> Copy this file per client (`assessments/clients/<org>/report.md`). Keep the section order. Fill every section; "Not applicable" is a valid answer, empty is not.

---

# Security Compliance Readiness Assessment
**Prepared for:** <Org name> · <Date> · **Prepared by:** <Named human, credentials> · Reviewed by: <Name>
**Engagement ref:** <ID> · **Basis:** NIST SP 800-171 Rev 3 (as flowed down), NIST SP 800-53 (GovRAMP), SOC 2 Trust Services Criteria, <funder-specific>

## 1. Executive summary (1 page, board-readable)
- What triggered this: <funder clause / contract / renewal, verbatim where possible>
- The bottom line: <1–3 sentences: which awards are exposed, what it costs to fix>
- Frameworks that apply: <table: framework → applies? → why>
- Top 3 gaps: <gap → risk → cost-to-fix estimate>
- 90-day plan headline: <3 bullets>

## 2. Funder & contract inventory
| Funder | Award | Value | Security terms found | Clause type (decoder) | Exposure |
|---|---|---|---|---|---|
| | | | | | |

## 3. Applicability analysis (the core value)
For each framework: does it apply, why/why not, and **who is actually obligated** (org vs. its vendors).
- NIST 800-171 / CMMC: <applies if CUI in scope; which requirements flow from which contract>
- GovRAMP / state RAMP: <applies to org's cloud vendors more than org itself — state the distinction>
- SOC 2: <applies if org is a service org to beneficiaries/partners with trust criteria expectations>
- FedRAMP 20x: <context only — org is a *buyer*, verify its vendors; org does not seek authorization>
- Other: <HIPAA, PCI, state data-sharing agreements>

## 4. Gap analysis (vs. applicable controls)
| Control area | Requirement | Current state | Gap | Evidence seen? | Priority |
|---|---|---|---|---|---|
| Access control / MFA | | | | | |
| Training & awareness | | | | | |
| Incident response | | | | | |
| Risk assessment | | | | | |
| Vendor management | | | | | |
| Data protection | | | | | |
| Logging & monitoring | | | | | |

## 5. Vendor verification summary
| Vendor | Data role | FedRAMP status | GovRAMP status | SOC 2 | Risk | Action |
|---|---|---|---|---|---|---|
| | | | | | | |

## 6. 90-day remediation plan (prioritized, owner + date)
1. <Quick win — e.g., enforce MFA everywhere>
2. <Policy gap — deploy 3 foundational policies from policies/ library>
3. <Evidence gap — stand up monthly collection from evidence/ matrix>
4. <Vendor risk — replace or contractually remediate unverified vendor>
5. <Funder deliverable — submit attestation pack by deadline>

## 7. Funder-questionnaire pack (answers to the 5 most common questions)
1. "Describe your security program." → <drafted from policy library>
2. "Do you comply with NIST 800-171?" → <honest answer + POA&M reference>
3. "List your subcontractors and their security posture." → <from §5>
4. "Do you have an incident response plan?" → <yes + summary>
5. "Provide evidence of training." → <evidence refs>

## 8. Cost of remediation (estimates)
| Item | One-time | Annual | Fundable via |
|---|---|---|---|
| MFA enforcement | | | NSGP/SLCGP/grant TA |
| Policy library deployment | | | |
| Evidence collection (retainer tier) | | | |
| SOC 2 readiness sprint (if applicable) | | | |

## 9. Sign-off
**Prepared by:** <human, signature/date> — **Reviewed by:** <human, date>
*This report is advisory. [Agency] does not certify, attest, or act as a 3PAO/CPA. Certification authority rests with licensed assessors.*

---

## Writing guide (rules for the drafting agent + human)
- **Plain English first.** A board member must understand §1 without the glossary. Jargon goes in footnotes.
- **Never invent evidence.** Every "current state" claim needs a source: seen config, screenshot, policy doc, or "not verified — gap."
- **Name the award.** Every risk statement ties to a specific funder/contract or it's cut.
- **Honesty over comfort:** if the org is not compliant, the report says "not compliant" with a plan, not "on track."
- **Audit-safe language:** avoid "certified," "authorized," "compliant" as adjectives for the org. Use "aligned," "prepared," "in remediation."
