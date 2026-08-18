# Funder Security Terms Decoder
**Purpose:** Turn contract boilerplate into plain-English obligations. Used in the diagnostic call and every assessment's §2.

## Clause patterns and what they actually mean
| Clause pattern (paraphrased) | Real obligation | Typical trigger |
|---|---|---|
| "Contractor shall comply with NIST SP 800-171" | Full 110-control (Rev 2) / 14-family (Rev 3) program *if CUI is in scope*; SSP + POA&M + annual affirmation | Fed/DoD pass-through |
| "Offeror must demonstrate FedRAMP-compliant infrastructure" | **Your cloud vendors** must be FedRAMP-authorized — not you. You must *verify and document* | State/federal RFPs |
| "Vendor must meet state cloud security standards (GovRAMP/StateRAMP)" | Same as above, at state level; check the state's participation (`state-ramp-map.md`) | SLED contracts |
| "Provide evidence of security program" | Questionnaire or attestation → answer bank + evidence pack | Most foundations, many state grants |
| "Comply with applicable laws re: data protection" | HIPAA if covered entity/business associate; state breach-notice laws; CCPA-type if CA data | Health/data orgs |
| "Subcontractors subject to same terms" | Flow-down: your vendors need the same verification chain | DoD/GSA (CUI rule, effective Jan 5, 2026) |
| "Cyber incident notification within 72 hours" | Written IR plan with notification SLA; practice the drill | Federal/state contracts |
| "Maintain cybersecurity insurance" | Policy in force, minimum limits; renewal proof | Many state agencies |

## Decoder rules
- **Never read a clause as stricter than it is** — "compliant with NIST 800-171" in a contract with no CUI often means an SSP + self-attestation, not a 3PAO assessment. Over-reading sells fear; the client's budget is not fear-shaped.
- **Never read it looser than it is** — if CUI flows, 800-171 is real and CMMC Level 2 may follow (Nov 2026 deadline).
- Every clause in a client contract gets: obligation → who's obligated (org vs. vendor) → evidence required → deadline.
- Update quarterly — GSA CUI rule (Jan 2026) and FedRAMP 20x rules (consolidated rules due mid-2026) keep moving goalposts.
