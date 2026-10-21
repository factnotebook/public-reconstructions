# FN-PIOTR-CASE2-001 — "No recorded access" is not "access did not occur": a GDPR record-gap reconstruction

- **Author:** Patrick Juvet Etoua
- **Originating project:** FactNotebook · engine camsva 0.9.0
- **Finding:** FN-PIOTR-CASE2-001
- **Reconstruction ID:** `FN-8c66ed94f110fa24`
- **Date:** 2026-10-21 (current version — open to the reviewer's ongoing critical read; non-dispositive, supersedable)

A bounded reconstruction, on a **synthetic** incident bundle, of what surviving access logs permit a controller to establish about **non-access** to particular records after an API-key exposure — the evidentiary question upstream of a GDPR Art. 33 "which records are affected?" decision.

## Independence & review

The incident bundle is **synthetic** and was constituted and submitted by **Piotr Reder** (case-2 pack). Piotr also acts as an **independent reviewer** of the reconstruction; his critical reading of this revision is **ongoing**, and a superseding version will issue if it surfaces anything. This page is a reconstruction **output**, **not** a certification, validation, or endorsement — and FactNotebook does **not** certify the controller's logging as adequate. **No Exempt Node:** FactNotebook does not exempt its own evidence-selection — the per-candidate admission register (Annex A/B, full register in the JSON) is itself inspectable.

## What the records establish — two levels, every record (11 propositions / 6 observations)

**Record level — what the submitted log contains:**
- R-A / R-B / R-C / R-D (no read of the respective record attributed to the exposed key is recorded) → **ESTABLISHED** (documentary silences).
- R-E (a read of I-3301 attributed to the key *is* recorded) → **CONTRADICTED** (the log contains the read).

**World level — real-world non-access:**
- R-A / R-B / R-C / R-D / R-E world → **CANNOT ESTABLISH**, each for a **distinct, named reason** (declared/simulated anchor + capture not demonstrated · coverage gap · object granularity · absent integrity structure · attribution declared-not-verified).
- BROAD path-completeness → **CANNOT ESTABLISH**.

Headline: *"not accessed" is a claim the records must affirmatively support — not a default that holds whenever a log happens to be silent.* Four recorded absences are established **at the record level** without establishing four real-world non-occurrences; and the one recorded read contradicts a record-level silence **without** establishing that the access occurred in the world (attribution is declared, not independently verified). Any precautionary classification of a record as "potentially affected" is a **controller decision**, kept separate from the reconstruction's findings.

The **determining limitation** for each world-level row is a **recorded field** (a column in the Results table + the machine-readable finding), kept outside the three engine states — so a reader of the table alone sees *why* each row cannot be established.

## Source (synthetic)

One integrity-verified synthetic bundle; `MANIFEST.sha256` over eight evidence files + three scripts (eleven total) recomputed here and matched **11/11**; every driving fact separately re-derived from the submitted files. Integrity is verified; **independence and completeness are declared, not established**.

## Limitations

Synthetic bundle (anchor signatures / RFC-3161 tokens simulated); same-source (controller's own bundle), not independent; does **not** determine whether the incident is a personal-data breach under GDPR Art. 4(12) or whether Art. 33 notification arises — those remain with the controller and its supervisory authority.

## Identity (publication convention)

| Identity | Designates |
|---|---|
| Reconstruction ID `FN-8c66ed94f110fa24` | the reconstruction state (observation model + admitted observations + rules) |
| SHA-256 of `finding.{pdf,md,json}` (see `SHA256SUMS`) | the exact bytes of this documentary representation |
| Canonical status | current version, open to the reviewer's ongoing critical read |

## Files

- `finding.pdf` / `finding.md` / `finding.json` — the finding (11 propositions, states, provenance, **Annex A/B admission register**, limitations). The **JSON carries the full register and complete (non-abbreviated) SHA-256 digests** for autonomous verification; the PDF abbreviates them.
- `SHA256SUMS` — digests of the three files above · verify: `sha256sum -c SHA256SUMS`
