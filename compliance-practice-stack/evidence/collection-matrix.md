# Evidence Collection Matrix & Monthly Cadence
**Purpose:** Turn "prove it" into a repeating, low-effort loop. AI aggregates; client staff confirm; human reviews. Evidence is the product — funders and auditors buy proof.

## Monthly collection cadence (per client, ~45 min staff time)
| Week | Task | Owner | Tool |
|---|---|---|---|
| W1 | Access review: pull user lists from M365/Google/CRM; flag stale accounts | AI agent (read-only export) | Client admin exports |
| W1 | MFA enforcement check (all accounts enrolled?) | AI agent | Config export |
| W2 | Training records: completion report | HR/admin | LMS/HRIS export |
| W2 | Vendor verification sweep (FedRAMP/GovRAMP/SOC 2 status changes) | AI agent | references/state-ramp-map.md + marketplaces |
| W3 | Log/backup check: backups ran, restore spot-test logged | IT person | Cloud console |
| W3 | Policy review: any changes? exceptions expired? | Human (us) | Policy tracker |
| W4 | Incident log: any events, near-misses, funder notifications? | Client staff | 5-min form |
| W4 | Monthly posture snapshot (1-pager to ED) | Us | Aggregated dashboard |

## Evidence inventory (the thing auditors/funders ask for)
| Evidence item | Source | Retention | Ready? |
|---|---|---|---|
| MFA configuration report | M365/Google admin | 12 mo | |
| Access review sign-offs | Quarterly review doc | 24 mo | |
| Training completion records | LMS report | 12 mo | |
| Backup success logs + restore test | Cloud console | 12 mo | |
| Incident response log (even "no incidents") | IR plan + log | 24 mo | |
| Vendor verification records | Quarterly sweep | 24 mo | |
| Policy review/approval signatures | Policy tracker | Life of policy | |
| Funder questionnaire submissions | Answer bank + submitted copies | 36 mo | |

## Rules
- **Evidence = dated, attributed, immutable.** Screenshot or export with timestamp; never a verbal claim.
- **No fabrication, ever.** An agent that can't find evidence marks a gap — that's a selling point, not a failure.
- **Automate the pull, humanize the sign-off:** each month's pack is reviewed by a named human before it enters the client's evidence vault.
- Client owns the evidence vault (their M365/Google Drive/SharePoint); we hold the index, never sole custody of their data.
