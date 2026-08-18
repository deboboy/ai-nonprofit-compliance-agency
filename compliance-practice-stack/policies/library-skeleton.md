# Policy Library Skeleton (NIST 800-171 / SOC 2-aligned)
**Purpose:** Foundational policies every grant-holding nonprofit needs. Ship as part of Standards retainer and Readiness Assessment remediation. Each policy is a template — agents draft from `prompts/03-policy-draft.md`, humans tailor + approve.

## Minimum viable set (deploy order)
1. **Information Security Policy** — umbrella: scope, roles, security objectives, review cadence (annual).
2. **Access Control Policy** — least privilege, MFA everywhere, account lifecycle (join/move/leave), quarterly access review.
3. **Incident Response Plan** — severity levels, response roles, reporting obligations (funder breach clauses!), 72-hour internal escalation, after-action within 30 days.
4. **Security Awareness Training Policy** — annual training + phishing exercises, records retention of completion.
5. **Vendor Management Policy** — onboarding/offboarding of vendors, security due diligence (FedRAMP/GovRAMP/SOC 2 check), quarterly verification cadence.
6. **Data Protection & Retention Policy** — data classification (CUI/PII/internal/public), retention schedule, disposal.
7. **Acceptable Use Policy** — devices, accounts, personal use, consequences.

## Template structure (per policy)
- Header: policy name, version, owner (named human), effective date, next review date.
- Purpose & scope (2–3 sentences, plain English).
- Policy statements (numbered; each mapped to control family below).
- Roles & responsibilities (ED/board, security owner, staff).
- Exceptions process (documented, time-limited, approved by owner).
- Enforcement & review.

## Control family mapping (for crosswalk)
| Policy | NIST 800-171 families | SOC 2 criteria |
|---|---|---|
| Information Security | 3.1 overall program | CC1.1–CC1.5, CC5 |
| Access Control | 3.1 Access Control | CC6.1–CC6.3, CC6.6 |
| Incident Response | 3.6 Incident Response | CC7.3–CC7.5 |
| Awareness Training | 3.2 Awareness & Training | CC1.2, CC3.2 |
| Vendor Management | 3.11 (3rd-party) | CC9.1–CC9.2 |
| Data Protection | 3.8 Media Protection, 3.13 | CC6.5–CC6.7, CC8 |
| Acceptable Use | 3.1, 3.9 | CC6.1 |

## Deployment notes
- Board approval is a deliverable — policy adoption meeting = billable touchpoint.
- Version control + "last reviewed" dates are evidence; never backdate.
- Keep policies org-branded, not consultant-branded (client owns the program).
