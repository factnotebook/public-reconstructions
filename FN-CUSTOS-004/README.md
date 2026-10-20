# FN-CUSTOS-004 — Observation vs inference: the determining-cause gap under observed-equivalence instrumentation

- **Author:** Patrick Juvet Etoua
- **Originating project:** FactNotebook · engine camsva
- **Finding:** FN-CUSTOS-004
- **Reconstruction ID:** `FN-b67b3d8fadbb891b`
- **Companion:** read with [FN-CUSTOS-003](../FN-CUSTOS-003/) (run 11) — run 12 instruments the open question run 11 left
- **Date:** 2026-10-20

A bounded reconstruction of the subject's frozen CI record **run 12**, built to test one thing: does the added instrumentation *close* the determining-cause gap that run 11 (FN-CUSTOS-003) left at CANNOT ESTABLISH?

## Independence & review

**Strictly non-dispositive**, and this is the planned **test of a loop**, not a new experiment. CUSTOS-CORE defined and exercised the control and shipped the additional instrumentation; the workflow produced run 12; **FactNotebook reconstructs** — it did not enforce, re-run, or control anything, and run 11 stands exactly as recorded. **No Exempt Node**; same-workflow corroboration, not independence of source.

**Tavares Heath / CUSTOS-CORE** independently recomputed the cited digests against the frozen run-12 records and confirmed the boundaries are drawn correctly against the observation set. That review is a **factual verification of the preserved records only — not an endorsement** of the interpretation; the conclusions remain FactNotebook's.

## What observation now establishes (5 propositions)

| Proposition | Result |
|---|---|
| **P1** verdict RED-CONFIRMED follows the declared rule (exit code 1) | **ESTABLISHED** |
| **P2** the only git-*tracked* delta between clean (DENY) and injected (ALLOW) trees is the one-line gate injection; both phases ran a hash-identical probe script at the same commit | **ESTABLISHED** |
| **P3** the non-gate porcelain differences are untracked entries, classified (by filename + subject declaration) as the run's own recording artifacts | **ESTABLISHED** |
| **P4** the injection is the *determining cause* of the DENY→ALLOW change | **CANNOT ESTABLISH** |
| **P5** a downstream tool execution or external effect occurred | **CANNOT ESTABLISH** |

Headline — the point of the whole series: run 12 delivered a **real gain in observability** (what run 11 *inferred* about tracked-state equivalence, run 12 *observes*: P2, P3 ESTABLISHED). **But a tighter observation is not causal proof.** A `git status --porcelain` observes git-*tracked* working-tree state — not all filesystem state, not the bytes loaded in memory, not non-filesystem environmental/runtime factors — so the determining-cause proposition **stays CANNOT ESTABLISH** (P4). FactNotebook took a genuine gain and reported exactly what it establishes (tighter *documentary* equivalence) **without letting it masquerade as the causal result it cannot support.** P5 stays CANNOT ESTABLISH at the authorization-decision boundary.

> *An independent reconstruction does not change the past; a subsequent one can change what the next record makes provable — here it moved an inference to an observation for the tracked dimension, and no further.*

## Source (pinned)

One public CI run — **38811246068 (run 12), commit `b06098c`** — frozen in-repo at `docs/red-proof-records/run-38811246068/` with a SHA-256 manifest. Every cited digest (evidence record, both instrumented probe artifacts, JUnit, pytest output, exit code) was re-fetched and re-hashed here and matches the manifest. Subject repo: `ceyptoslim/CUSTOS-CORE` (AGPL).

## Limitations

Same-workflow corroboration (not independent of the subject); P2/P3 are **documentary** observations of the git-tracked record, not a hash of executed bytes; the untracked-artifact classification rests on filenames + the subject's declaration (declared, not independently verified); P4/P5 held at CANNOT ESTABLISH. No legal or safety conclusion is drawn.

## Identity (publication convention)

| Identity | Designates |
|---|---|
| Reconstruction ID `FN-b67b3d8fadbb891b` | the reconstruction state (bound to its observation model + admitted observations + rules) |
| SHA-256 of `finding.{pdf,md,json}` (see `SHA256SUMS`) | the exact bytes of this documentary representation |
| Canonical status | the 2026-10-20 rendering, designated for publication |

## Files

- `finding.pdf` / `finding.md` / `finding.json` — the finding (full propositions, states, provenance, limitations)
- `SHA256SUMS` — digests of the three files above · verify: `sha256sum -c SHA256SUMS`
