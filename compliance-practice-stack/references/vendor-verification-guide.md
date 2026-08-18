# Vendor Verification Guide
**Purpose:** Step-by-step for verifying a nonprofit's cloud vendors against FedRAMP/GovRAMP/SOC 2 — the "verify theirs, not yours" service.

## Step 1 — FedRAMP check (federal work)
1. Go to `marketplace.fedramp.gov` (legacy) — search vendor name.
2. Check authorization status: **Authorized** / In Process / Not Found. Note the authorization level (LI-SaaS/IL2/IL4/IL5/IL6) and the *impact level granted* — an IL2 authorization is not proof for IL4 data.
3. Check the **FedRAMP 20x** path: the original program sunsets late 2026; new authorizations flow through 20x (Phase 3 active since ~mid-2026). A vendor "in process" under 20x is not authorized — flag as such.
4. Record: marketplace URL, date, status, level.

## Step 2 — GovRAMP check (state work)
1. Go to `govramp.org` → participating government organizations + searchable vendor list (GovRAMP publishes verified providers).
2. Cross-check the *specific state agency* in the client's contract — participation is agency-level.
3. Record: status, agency relevance, date.

## Step 3 — SOC 2 / Trust Center check (commercial trust)
1. Vendor's Trust Center or security page — SOC 2 report availability.
2. Note report **type** (I vs. II) and **date** — a 2-year-old Type I report is weak evidence.
3. If no public report, request via vendor security contact; log the request date (a pending request is itself evidence of diligence).

## Step 4 — Risk scoring
| Data role of vendor | Unverified | SOC 2 only | GovRAMP | FedRAMP |
|---|---|---|---|---|
| P0: stores/processes CUI, PII, or beneficiary data | **Stop — remediate** | Weak (check date) | OK for state | OK for fed |
| P1: business systems w/o sensitive data | Watch | OK | OK | OK |
| P2: commodity (email provider, hosting) | Watch | OK | OK | OK |

## Step 5 — Deliverable
Output the §5 vendor table (prompt `05-vendor-verification`): vendor | data role | FedRAMP | GovRAMP | SOC 2 | verification date | risk | action.

## Rules
- Verification date on every row — funders ask "when did you check?"
- "NOT-FOUND" ≠ "non-compliant" — it means unverified. Different sentence.
- Quarterly cadence per `evidence/collection-matrix.md` (W2 sweep).
