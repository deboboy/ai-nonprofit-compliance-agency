# Funder Security Questionnaire — Answer Bank & Workflow
**Purpose:** The most common concrete ask from funders is a security questionnaire. Speed + honesty here wins renewals. This bank + drafting workflow makes responses a 1-day SLA instead of a 2-week panic.

## The 5 most common questions (with answer guidance)
1. **"Describe your organization's security program."**
   → 3-paragraph standard: governance (owner + board oversight), technical controls (MFA, patching, backups), program maturity (training cadence, IR plan, vendor management). Pull from client's policy library; never generic boilerplate — customize org name, tools, owner name.

2. **"Do you comply with [NIST 800-171 / SOC 2 / ISO 27001]?"**
   → Honest tiers: (a) "Yes, aligned — assessment on file" / (b) "Partially — POA&M with target dates" / (c) "In remediation via [Agency] Readiness Assessment." **Never claim compliance without an assessment or attestation backing it.** If the funder demands full compliance and the client isn't there, surface it as a go/no-go decision with cost — do not paper over it.

3. **"List your vendors/subcontractors and their security posture."**
   → Table from the vendor verification sweep: vendor, data role, FedRAMP/GovRAMP/SOC 2 status, verification date. Unverified vendors are listed as such with remediation date.

4. **"Do you have an incident response plan? Describe your notification process."**
   → Yes + 3-bullet summary: severity levels, who decides notification, funder/contract notification SLA (check the actual contract clause — many require 72-hour notice).

5. **"Provide evidence of security training / MFA / backups."**
   → Evidence pack from `evidence/collection-matrix.md` — dated exports, not screenshots of dashboards from 8 months ago.

## Workflow (1-day SLA)
1. Funder questionnaire lands → classify question type against bank (`prompts/04-questionnaire-response.md`).
2. Agent drafts answers from client's policy library + evidence vault (reads only indexed, approved docs).
3. Human reviews → client ED/COO approves → submit with evidence pack.
4. Log submission in the answer-bank archive (dated, funder, version) — 36-mo retention.

## Rules
- **Answer only what's asked.** No volunteering gaps; no hiding them either — if a question is material, answer it.
- **Versioned and archived:** funders reuse questions; keep a searchable history per client.
- **Never promise remediation dates the client hasn't committed to.**
