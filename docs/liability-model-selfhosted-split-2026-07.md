# Liability Architecture: Self-Hosted Split for the Signal Layer
**Builds on:** `dd-signal-engineering-layer-2026-07.md` · Prepared July 2026
**Decision being designed:** Last Myle Engineering does **not** own/custody the partner-facing data layer (capability #4); nonprofits self-host what they own. Preserve the revenue embedded in capability #1 (universal system interface).

---

## 1. The liability logic

The DD update flagged two new HIGH risks that both stem from one fact: **a hosted platform aggregates security posture across dozens of nonprofits and becomes a breach target holding everyone's exposures.** Remove custody and both risks collapse:

| Risk | Hosted model | Self-hosted split |
|---|---|---|
| Platform-as-target (aggregated posture of all clients) | You are the jackpot | Each client holds only their own data — no aggregation prize |
| CUI/PII custody & DPA exposure | You're a processor (or worse, sub-processor chain) | Data never leaves client tenant; you ship code, not custody |
| E&O / cyber insurance premiums | Priced for a data platform | Priced for a software vendor + consultant — materially cheaper |
| Write-access automation liability | Your systems mutate client estates | Automations run *inside* the client's tenant, under their authority |
| Vendor security questionnaires about *you* | Every client must assess you | Software supply-chain questionnaire only (SBOM, signing, update integrity) |

Rule that follows: **Last Myle touches derived signals and metadata by default; raw events, evidence, and dictionaries stay in the client's tenant unless the client explicitly grants scoped, revocable access.**

## 2. What each party owns

### Nonprofit owns (self-hosted in their tenant)
- **Canonical store** — the validated signal warehouse (their M365/Google Drive, SharePoint lists, or a small Postgres container we provision).
- **Data dictionaries** — plain-English field meanings, refresh cadence, caveats (capability #4's core artifact).
- **Partner views** — read-only query surfaces for funders/auditors/board.
- **Evidence vault** — dated exports, sign-offs, questionnaire archive.
- **Automations** — any write-actions (stale-account disable, etc.) execute under *their* admin authority with *their* approval trail.

### Last Myle provides (and bills for)
- **Connector agents** — small containers/scripts deployed into the client tenant; read-only OAuth scopes; pull → standardize → validate → write to *their* store.
- **Validation-rule packs** — the schema checks, freshness monitors, quarantine logic, derived-field definitions (write-time validation). This is the IP.
- **Update channel** — signed releases, changelog, compatibility matrix.
- **Remote operations (opt-in)** — least-privilege, scoped, revocable access to the client's store for monitoring/QA/questionnaire drafting; off switch is one toggle.
- **Enablement services** — onboarding, dictionary authoring, funder-view configuration, training.

### The line, stated once
> We build and maintain the machinery inside your walls; the data, the meaning, and the keys stay yours.

## 3. Preserving the revenue (capability #1 economics)

Self-hosting removes data gravity — so the moat must move from **custody** to **(a) engineering leverage, (b) recurring software value, (c) operational trust.** Five revenue lines survive the split:

| # | Line | Why it survives self-hosting | Price shape |
|---|---|---|---|
| 1 | **Signal-source onboarding (services)** | End-to-end bring-up (discovery→scoping→ingestion→standardization→live) is skilled labor regardless of where the store sits | $1,500–$4,000 per source, one-time |
| 2 | **Software subscription (open-core)** | Free: core agent + 2 base connectors. Licensed: premium connector packs (Salesforce NPSP, Bloomerang, HRIS, state portals), validation-rule pack updates, funder-report templates | $150–$600/mo per org by tier |
| 3 | **Managed operations retainer** | Clients *can* self-operate; almost none will. We monitor heartbeats, patch agents, triage quarantines, refresh vendor verifications | $500–$2,000/mo (folds into existing GTM tiers) |
| 4 | **Attestation & questionnaire outputs** | Generated from *their* store via our templates/prompts; every answer cites their source rows | Included in retainer; à la carte $750–$2,500 per funder cycle |
| 5 | **Enablement & certification** | Train client staff/partners on the dictionary and views; certify third-party IT contractors on our connector framework (they pay us to be listed) | Workshops $2–5K; contractor listing $500–$1,500/yr |

**Key pricing principle:** charge for *engineering and judgment*, never for *holding their data*. This is also a sales weapon — "we can't leak what we don't hold" closes security-conscious EDs faster than any feature.

## 4. The honest tradeoffs

| Tradeoff | Reality | Mitigation |
|---|---|---|
| **Support burden of heterogeneous self-hosts** | Version skew, broken containers, "it stopped working" tickets | Hard version policy (N-1 supported max), auto-update default, health-check beacon (metadata only, opt-out honored) |
| **Weaker lock-in** | Client can drop us and keep the store | Lock-in shifts to validation-rule packs, funder templates, and the relationship — acceptable; churn was the base-DD risk anyway |
| **Slower iteration / no network effects from pooled data** | Can't benchmark across clients ("orgs like you see X") | Opt-in anonymized benchmarking program — clients who share derived metrics get benchmarks free; consented, documented, revocable |
| **Clients lack capacity to operate anything** | Some will fail at self-hosting entirely | Two SKUs: pure self-host (they run everything) vs. managed-self-host (we operate inside their tenant, still zero custody of raw data off-site beyond scoped reads) |
| **Open-core leakage** | Premium packs get copied | Packs are config + know-how; the durable IP is the update cadence and the compliance mapping maintenance — same reason TurboTax isn't pirated out of existence |

## 5. Contract & insurance deltas (updates qa/engagement-letter-language.md direction)

1. **Split agreements:** (a) *Software License* — AS-IS core + licensed packs, disclaims all data custody; (b) *Services Agreement* — onboarding/operations, standard advisory disclaimers; (c) *DPA only when remote operations are enabled* — scoped to derived metrics actually accessed, not blanket processing rights.
2. **No-custody representation:** contract states Last Myle servers do not store client raw events/evidence; scoped remote access sessions are logged and revocable.
3. **Client responsibility clause expanded:** client owns store availability, access control to their own views, and approval of automations executed under their authority.
4. **Insurance right-sizing:** E&O for advisory; cyber policy sized for the metadata we *do* touch (opt-in beacons, ops-session logs) — expect materially lower premiums than a hosted-platform posture. Re-quote after the first pilot.
5. **Automation authorization form:** every write-action enabled requires a signed schedule naming the action, trigger, and human approver — this is the audit trail that keeps automation liability with the authorizing client.

## 6. Verdict

The balance works because the two things Frank doesn't want to own (data custody, partner-meaning ownership) were never the profit centers — they were the liability centers. The profit centers (engineering the ingestion/validation layer, operating it, generating funder-ready outputs) survive intact and become easier to sell and insure.

- **Commit** to: self-hosted-by-default architecture; open-core licensing; managed-self-host SKU for low-capacity clients; split contracting; insurance re-quote post-pilot.
- **Watch:** whether premium-pack subscription converts at $150–$600/mo without managed ops attached — if attach rate is high, price them together and stop pretending self-serve exists in this segment.
- **Sequencing unchanged:** Phase A pilots prove delivery-hours drop; this decision changes *where the bytes live*, not the phase plan.

---
*Sources: inherits dd-signal-engineering-layer-2026-07.md source list; no new external research required — this is an architecture/business-model decision memo.*
