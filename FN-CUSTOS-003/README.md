# FN-CUSTOS-003 — CUSTOS-CORE red-proof, detection-scoped (run 38610363998)

Independent reconstruction of a subject-supplied red-proof record. Non-dispositive;
factual-reconstruction only, not a certification or endorsement.

## ▸ Current reconstruction

**[`FN-f626b9c8becace9f`](reconstructions/FN-f626b9c8becace9f/)** — current. Carries two
corrections to the superseded version (below). Six propositions; outcomes unchanged.

- Artifact-revision identity (pin the exact ledger revision, independently of the
  reconstruction id): `finding.json` sha256
  `80f94ffddffe407c5f801f1f42fbe111dac0450f48cb07deed6d86f8e18dcd5f`;
  `SHA256SUMS` sha256
  `7d3cce05c7fdd94685a237d3f82bdef3a97760fd3f1d7816d86883e05c5f9bcf`.

## Versions (both preserved and independently verifiable)

| Reconstruction | Status | Location |
|---|---|---|
| `FN-f626b9c8becace9f` | **current** | [`reconstructions/FN-f626b9c8becace9f/`](reconstructions/FN-f626b9c8becace9f/) |
| `FN-da06acd59938f5b9` | superseded | [`reconstructions/FN-da06acd59938f5b9/`](reconstructions/FN-da06acd59938f5b9/) · and the files at this folder's root |

**Reference continuity.** The root-level `finding.md`, `finding.pdf`, `finding.json`
and `SHA256SUMS` are preserved unchanged from the original publication
(`FN-da06acd59938f5b9`) so existing direct links still resolve to exactly what was
examined. They are historical, not the current reconstruction. Verify any version with
`sha256sum -c SHA256SUMS` inside its directory.

## Why FN-da06acd59938f5b9 was superseded — two corrections of different kinds

An independent line-by-line verification by the subject (Tavares) against the frozen
run manifest, and our own re-run of the reproducibility check on the recovered original
sources, each surfaced one defect. They are different in nature:

**1. Semantic correction (the evaluated claim).** Proposition **P5** stated the two
failing tests were "admin-auth assertions." On the record they are **action-gate
allowlist, deny-by-default** assertions (`tests/test_action_gate.py`); the finding's own
basis already named them correctly. The P5 statement now reads "the two identified
action-gate allowlist assertions." Because a proposition's statement is part of the
reconstruction's model, this changes the identifier
(`FN-da06acd59938f5b9 → FN-f626b9c8becace9f`). **All six proposition outcomes are
unchanged, and P5 remains ESTABLISHED** — re-derived on the corrected statement, not
assumed. No conclusion is reversed.

**2. Evidentiary-reference correction (how a source is cited).** The admission-register
entry for the P3 probe-delta observation named its source with one composite path
(`red-proof-probe-{clean,injected}.json`) that did not resolve to a verifiable file. P3
is a **delta over both probe records** (clean = deny, injected = allow, identical
request), so both files are required sources. The entry now references them
explicitly — `red-proof-probe-clean.json` (`b5951061…`) and
`red-proof-probe-injected.json` (`5683de84…`), both matching the run manifest. This
corrects the observation's **source reference**, not its evidentiary meaning, and does
**not** change the reconstruction identifier (the admission register is a projection
outside the identity basis). It does change the published bytes — which is why the
artifact-revision identity above pins the exact register revision independently of the
reconstruction id.

These two defects are a small illustration of three distinct properties: **file
integrity** (the sources were intact — Tavares verified this), **evidentiary-reference
validity** (one citation was malformed — corrected here), and **conclusion accuracy**
(one label was wrong — corrected here). A reconstruction can be internally consistent
yet still carry an inaccurate claim or a malformed source reference; both are now fixed,
and the change is recorded rather than applied silently.

## Non-endorsement

Independent reconstruction by FactNotebook; factual-reconstruction only, not a
certification or endorsement, and not independent verification of a production incident.
Authority and interpretation remain with the accountable parties.
