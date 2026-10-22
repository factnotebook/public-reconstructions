# FN-CUSTOS-REDPROOF-002 — CUSTOS-CORE red-proof, record v3 (establishability lifecycle)

Reconstruction id **`FN-63a3bbfc57791b7c`**. The lifecycle successor to
**FN-CUSTOS-REDPROOF-001**: the **same four propositions**, reconstructed on an improved
record. Published here for series completeness; like -001, it predates the admission-
register convention.

## What it reconstructs — and the lifecycle it shows

| Proposition | -001 (run 9) | -002 (v3, this) |
|---|---|---|
| P1 — verdict follows the declared rule | ESTABLISHED | ESTABLISHED |
| P2 — exit code faithful | ESTABLISHED | ESTABLISHED |
| P3 — the regression was detected | ESTABLISHED | ESTABLISHED |
| P4 — the regression *class* was covered | **CANNOT ESTABLISH** | **ESTABLISHED** |

The single moving outcome is P4. In -001 the suite ran under `pytest -x`, so only the
first failing assertion executed and class coverage could not be established. In the v3
record the fail-fast flag was removed, the whole class ran, and P4 becomes **ESTABLISHED**.

The point: the decisive difference between these two findings is the **evidentiary
record** — the v3 run no longer used fail-fast and captured the class execution that
assessing P4 requires. A proposition moved from CANNOT ESTABLISH to ESTABLISHED because
the record now supports it; the reconstruction reflects what each record supports.
"Cannot establish" is a statement about the available evidence at a point in time, not a
permanent verdict.

This reconstruction makes that gain in establishability **visible**; it does **not**
claim to have **caused** it. Whether the limit surfaced at -001 prompted the change in
the v3 record is a separate question of chronology, not confirmed here.

## Three properties, kept distinct

- **Artifact integrity** — the files here match `SHA256SUMS` (`sha256sum -c SHA256SUMS`);
  deterministic, holds now.
- **Historical reconstruction** — produced *before* the current conventions; it carries
  **no admission register** (the admitted observations are not enumerated as a
  candidate→admitted/rejected trail).
- **Independent re-derivability** — the outcomes were read from the subject's v3 CI
  red-proof record and can be re-walked against it where available; **but** this
  artifact predates two machine-checkable conventions (no admission register, no
  structured Results table), so the admission boundary and the state/limitation
  projection are not machine-re-verifiable from it alone — declared limits of
  re-verifiability, stated not masked, and not retrofitted.

**Contract status (declared, not hidden).** Under the current finding-consistency
contract (v0.2.2): **artifact integrity passes** (`validate_publication`). The
finding-level contract does **not** fully pass on this historical artifact —
`candidate_partition` (absent admission register) and `proposition_projection` (absent
structured Results table) flag pre-convention structure; they are not, by themselves,
evidence of a substantive inconsistency, nor do they establish the absence of one.
Published as a historical record, not as one satisfying the current contract.

Manifest scope: `SHA256SUMS` covers all four published files in this folder —
`finding.md`, `finding.pdf`, `finding.json` and this `README.md`.

## Series

**[-001](../FN-CUSTOS-REDPROOF-001/)** (run 9 / v2, P4 CANNOT ESTABLISH) → **-002** (this,
v3, P4 ESTABLISHED) → **[FN-CUSTOS-003](../FN-CUSTOS-003/)** → **[FN-CUSTOS-004](../FN-CUSTOS-004/)**.

## Non-endorsement

Independent reconstruction by FactNotebook; factual-reconstruction only, not a
certification or endorsement, and not independent verification of a production incident.
