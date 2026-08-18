# Framework Crosswalk — What Applies to a Nonprofit (and what doesn't)
**Purpose:** One table to end the confusion. This is the heart of the advisory value — most orgs think they need FedRAMP; almost none do.

## The decision table
| Framework | Applies when | Who's obligated | Typical cost for org | What we deliver |
|---|---|---|---|---|
| **NIST 800-171** | CUI in scope (federal contract/flow-down) | The org | $25K–$100K+ if assessed; self-attestation cheaper | SSP + POA&M + evidence loop |
| **CMMC 2.0** | DoD contract w/ CUI (Level 2) or FCI (Level 1) | The org; 3PAO assesses Level 2 (Phase 2 deadline Nov 2026) | $30K–$150K | Gap assessment + readiness + RP partnership |
| **SOC 2** | Org is a *service org* to beneficiaries/partners (data intermediary, SaaS-like) | The org; CPA audits | $15K–$40K audit + platform | Readiness sprint + evidence + audit support |
| **GovRAMP / state RAMP** | Org *buys* cloud services used in state work | **The org's vendors** | Vendor-borne | Vendor verification + procurement language |
| **FedRAMP 20x** | Org *buys* cloud services used in federal work | **The org's vendors** | Vendor-borne | Vendor verification (marketplace check) |
| **HIPAA** | Covered entity / business associate | The org | Policy + BAA + risk analysis | BAA workflow + risk analysis |
| **ISO 27001** | Foundation/partner explicitly requires cert | The org | $20K–$60K | Rare in nonprofit segment; refer out |
| **CIS Controls / CISA guides** | Baseline good practice, no mandate | The org | Near-zero | Free CISA resources + our gap layer |

## The two sentences that win the diagnostic call
1. *"FedRAMP and GovRAMP are badges for the companies you buy software from — your job is to verify theirs, not earn your own."*
2. *"The frameworks that land on *your* desk are NIST 800-171 flow-down, CMMC if you touch DoD data, and SOC 2 if you handle data for others."*

## Notes
- FedRAMP 20x sunsetting the original program late 2026 — vendor verification must check the 20x path, not just the legacy marketplace.
- GSA CUI rule (effective Jan 5, 2026) extends 800-171-style obligations to civilian-agency contractors — nonprofits with any GSA-adjacent contract should be treated as 800-171 candidates by default.
