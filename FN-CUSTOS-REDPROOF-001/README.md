# FN-CUSTOS-REDPROOF-001 — CUSTOS-CORE red-proof, run 9 (record v2)

Reconstruction id **`FN-b27fe08ed9252198`**. An early member of the CUSTOS-CORE
red-proof series. Published here for completeness so the series is re-walkable; it
predates conventions introduced in the later entries (notably the admission register).

## What it reconstructs

Four propositions over the run-9 red-proof record:

| Proposition | Outcome |
|---|---|
| P1 — verdict follows the declared rule | ESTABLISHED |
| P2 — exit code faithful | ESTABLISHED |
| P3 — the regression was detected | ESTABLISHED |
| P4 — the regression *class* was covered | **CANNOT ESTABLISH** |

P4 cannot be established here because the suite ran under `pytest -x` (fail-fast): the
first failing assertion stopped the run, so the record does not show that the rest of
the class was exercised. Detecting one regression is not covering the class. This is the
"before" state of an establishability lifecycle — see **FN-CUSTOS-REDPROOF-002**, where
the same P4 becomes ESTABLISHED once the record improves (fail-fast removed), with
FactNotebook unchanged.

## Three properties, kept distinct

- **Artifact integrity** — the files in this folder match the digests in `SHA256SUMS`
  (`sha256sum -c SHA256SUMS`). This is deterministic and holds now.
- **Historical reconstruction** — this finding was produced *before* the current
  conventions. In particular it carries **no admission register**: the admitted
  observations are not enumerated as a candidate→admitted/rejected trail.
- **Independent re-derivability** — the propositions were read from the subject's CI
  red-proof record (run 9). A third party can re-walk the *outcomes* against that record
  where it is available, **but** this artifact predates two machine-checkable
  conventions used in the later entries: it has **no admission register** and **no
  structured Results table**. So the **admission boundary** (which candidates were
  admitted) and the **state/limitation projection** are not machine-re-verifiable from
  this artifact alone. These are declared limits of re-verifiability — stated, not
  masked, and **not** retrofitted.

**Contract status (declared, not hidden).** Under the current finding-consistency
contract (v0.2.2): **artifact integrity passes** (`validate_publication`: files present
and matching `SHA256SUMS`). The finding-level contract does **not** fully pass on this
historical artifact — `candidate_partition` flags the absent admission register and
`proposition_projection` flags the absent structured Results table. Both reflect
pre-convention structure; they are not, by themselves, evidence of a substantive
inconsistency in the finding, and equally they do not establish the absence of one —
the historical verification confirms only what it checks (artifact integrity, and the
stated outcomes as read from the record). This entry is published as a historical
record, not as one satisfying the current contract.

Manifest scope: `SHA256SUMS` covers all four published files in this folder —
`finding.md`, `finding.pdf`, `finding.json` and this `README.md` — so the declared
limits and historical-status statements are themselves under the manifest.

## Series

Part of the CUSTOS-CORE red-proof series: **-001** (this, run 9 / v2) → **-002**
(lifecycle successor, P4 ESTABLISHED) → **[FN-CUSTOS-003](../FN-CUSTOS-003/)**
(detection-scoped, run 38610363998) → **[FN-CUSTOS-004](../FN-CUSTOS-004/)**. The
provisional -003 referenced in earlier correspondence is not published as a separate
artifact. The corresponding case is documented under
[FN-CUSTOS-003](../FN-CUSTOS-003/), where the published versions and correction history
are preserved.

## Non-endorsement

Independent reconstruction by FactNotebook; factual-reconstruction only, not a
certification or endorsement, and not independent verification of a production incident.
