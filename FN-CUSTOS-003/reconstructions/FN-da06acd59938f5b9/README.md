# FN-CUSTOS-003 — The action gate under a blind pre-registered injection (bounded reconstruction)

- **Author:** Patrick Juvet Etoua
- **Originating project:** FactNotebook · engine camsva
- **Finding:** FN-CUSTOS-003
- **Reconstruction ID:** `FN-da06acd59938f5b9`
- **Canonical status:** 2026-10-20 rendering — the **sole canonical text** behind this identifier (supersedes the 2026-10-18 rendering and the provisional `FN-c220610b1c492d66`; all share the same `observation_model` and `observation_set`, so the identifier is unchanged — only the P3 basis sentence and generated date differ)
- **Companion:** read with [FN-CUSTOS-004](../FN-CUSTOS-004/) (run 12) — the two-run arc of one evidence-improvement loop
- **Date:** 2026-10-20

A bounded reconstruction of what the subject's own frozen CI record (CUSTOS-CORE "red-proof" run 11) permits one to establish, contradict, or cannot establish, about a blind, pre-registered single-line injection into a pre-flight action gate.

## Independence & review

**Strictly non-dispositive.** Roles, no overlap: **CUSTOS-CORE defined and exercised the control** (its pre-flight action gate) and froze the pre-registration; the workflow produced the record; **FactNotebook reconstructs** what that record supports — it did not define, enforce, re-run, or control anything. **No Exempt Node:** every observation is a record from the subject's own run, re-hashed here against its manifest (match). Corroboration is **same-workflow, not mutual independence of source**.

**Tavares Heath / CUSTOS-CORE** independently recomputed every cited digest against the frozen records and confirmed **no discrepancy** in this report's descriptions of the preserved record. That review is a **factual verification of the preserved records only — not a certification, validation, or endorsement** of the interpretation or conclusions, which remain FactNotebook's.

## What the record establishes (6 propositions)

| Proposition | Result |
|---|---|
| **P1** verdict RED-CONFIRMED follows the declared rule (exit code 1 ≠ 0) | **ESTABLISHED** |
| **P2** the record contains a sealed description (SHA-256) of the injected modification | **ESTABLISHED** |
| **P3** clean and injected probe records report DENY vs ALLOW for an identically-specified request | **ESTABLISHED** |
| **P4** the injection is the *determining cause* of the ALLOW (causal attribution) | **CANNOT ESTABLISH** |
| **P5** the suite *detected* this regression (two named admin-auth assertions failed) | **ESTABLISHED** |
| **P6** RED-CONFIRMED establishes *universal* coverage (every weakening would be caught) | **CANNOT ESTABLISH** |

Headline: a **detected regression, bounded** — the gate's DENY→ALLOW delta and its detection are established on the record; whether the injection is the *determining cause* is a bounded inference, not an observation (P4); and detection of this class is **not** a clean bill of health (P6). Even if P4 held, an ALLOW is a violation at the **authorization-decision** boundary — not evidence the tool executed or that a real-world effect occurred (the same line drawn in the Sovereign Veritas X5 reconstruction).

## Source (pinned)

One public CI run — **38610363998 (run 11), commit `f5d48c9`** — frozen in-repo at `docs/red-proof-records/run-38610363998/` with a SHA-256 manifest. Every cited digest (sealed injection diff `74456f76…`, both probe artifacts, JUnit, pytest output, exit code) was re-fetched and re-hashed here and matches the manifest. Subject repo: `ceyptoslim/CUSTOS-CORE` (AGPL).

## Limitations

Same-workflow corroboration (not independent of the subject); P4 held at CANNOT ESTABLISH (clean-probe code not hash-bound, untracked/environmental deltas not excluded); P6 records that 30 other gate tests passed without a scope analysis; the blindness of the run rests partly on subject-declared protocol. No legal or safety conclusion is drawn.

## Identity (publication convention)

| Identity | Designates |
|---|---|
| Reconstruction ID `FN-da06acd59938f5b9` | the reconstruction state (bound to its observation model + admitted observations + rules) |
| SHA-256 of `finding.{pdf,md,json}` (see `SHA256SUMS`) | the exact bytes of this documentary representation |
| Canonical status | the 2026-10-20 rendering, designated for publication |
| Version history | 2026-10-18 rendering and provisional `FN-c220610b1c492d66` — superseded |

## Files

- `finding.pdf` / `finding.md` / `finding.json` — the finding (full propositions, states, provenance, limitations)
- `SHA256SUMS` — digests of the three files above · verify: `sha256sum -c SHA256SUMS`
