# FN-PIOTR-CASE2-001 — "No entry is a claim, not a default"

Synthetic case (Piotr Reder, case 2): *can a controller show each record was NOT
accessed through an exposed API key?* Strictly non-dispositive — it reconstructs
what the submitted bundle lets us establish; it does not make a GDPR finding.

## ▸ Current reconstruction

**[`FN-e84c721fb7ff3f2e`](reconstructions/FN-e84c721fb7ff3f2e/)** — seven admitted
observations, twelve propositions. This is the current reconstruction.

> **Reference continuity.** The root-level `finding.md`, `finding.pdf`,
> `finding.json`, and `SHA256SUMS` are preserved unchanged from the original
> publication (`FN-8c66ed94f110fa24`) to maintain existing direct links. They are
> historical, not the current reconstruction. For the current finding, use
> `FN-e84c721fb7ff3f2e`.

## Versions (both preserved and independently verifiable)

| Reconstruction | Status | Location | Obs | Props |
|---|---|---|---|---|
| `FN-e84c721fb7ff3f2e` | **current** | [`reconstructions/FN-e84c721fb7ff3f2e/`](reconstructions/FN-e84c721fb7ff3f2e/) | 7 | 12 |
| `FN-8c66ed94f110fa24` | superseded | [`reconstructions/FN-8c66ed94f110fa24/`](reconstructions/FN-8c66ed94f110fa24/) · **and the files at this folder's root** | 6 | 11 |

### Addressing & verification

The `finding.md`, `finding.pdf`, `finding.json` and `SHA256SUMS` **at the root of
this folder are unchanged** — they remain the originally published
`FN-8c66ed94f110fa24`, so any link already shared to them still resolves to exactly
the artifact that was examined. They are **not** replaced by the current
reconstruction. The current reconstruction is published alongside them, separately
addressable under `reconstructions/FN-e84c721fb7ff3f2e/`. The same bytes of the
superseded version are also mirrored under `reconstructions/FN-8c66ed94f110fa24/`
so each version is addressable by its identifier.

Verify any version with `sha256sum -c SHA256SUMS` inside its directory.

## Why FN-8c66ed94f110fa24 was superseded

Following Piotr Reder's review, the controller's database-snapshot integrity
attestation (`storage_attestation.json`, whose own field is
`covers_access_logs=false`) was reconsidered. It had been recorded as a *rejected*
candidate, because it does not establish that the access logs were protected. On
review that was too narrow: a piece that is non-probative for a **control** can
still bear on a **limitation** of that control. The attestation is now **admitted**
as a positive observation of its own declared scope, under a new, strictly bounded
proposition:

> **R-D-attestation-scope** — "the attestation extends to the access-logging
> pipeline" → **CONTRADICTED**.

This establishes the declared scope of *this* attestation only. It does **not**
establish that no other integrity mechanism protects the logs (that would require
evidence of completeness over all mechanisms), and it **corroborates** the
R-D-world limitation (absent log-chaining, db-admin-writable store) without
**constituting** it.

Admitting the attestation changed the admitted observation set from six to seven,
so the reconstruction identifier changed. **No prior conclusion is reversed:** the
eleven earlier proposition states are unchanged; a bounded limitation that was
noted in prose is now positively recorded in its own fields.

## Non-endorsement

Synthetic data; no real organisation, person or system. Independent reconstruction
by FactNotebook; it does not endorse, and is not endorsed by, any other party. It
reports establishability and is non-dispositive — authority and decisions remain
with the accountable parties.
