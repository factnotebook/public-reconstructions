# FN-CHAD-XB1-X5-001 — Independent reconstruction of Sovereign Veritas XB-1, case X5

- **Author:** Patrick Juvet Etoua
- **Originating project:** FactNotebook
- **Finding:** FN-CHAD-XB1-X5-001
- **Reconstruction ID:** `FN-9e087ff81fe3759f` · engine camsva 0.9.0
- **Date:** 2026-10-15

An independent, bounded reconstruction of what the public artifacts of Sovereign Veritas
experiment **XB-1, case X5** permit one to establish, contradict, or cannot establish —
built from the pre-registration, the results, and the reference probe alone, without
re-running the probe and without relying on any internal mechanism of either project.

## Independence

This is an **independent external reconstruction**. It is **not** a certification,
validation, or endorsement of Sovereign Veritas or Principia Artificialis. It states only
what the public record supports; the judgment applied to these facts stays with the
accountable parties. FactNotebook's reconstruction engine, internal methods, and future
work are **not** part of this publication.

## The case

X5: a synthetic executor produces one effect, the evidence-recording operation fails, and
the ledger holds zero records. The reconstruction keeps three questions distinct — what the
experiment reports, what the evidence trail retains, and what can be established about the
underlying event:

- The published experiment **reports** a synthetic effect while the ledger write fails —
  **ESTABLISHED**, relative to the published artifacts.
- "Zero ledger records imply zero reported synthetic effects" — **CONTRADICTED**, within the
  experiment.
- The effect is **recorded** in the evidence trail — **CONTRADICTED** (the probe reports
  zero records).
- Authorization established **from the evidence trail** — **CANNOT ESTABLISH**.
- Execution established **from the evidence trail** — **CANNOT ESTABLISH**.
- A **real-world external effect** occurred — **CANNOT ESTABLISH** (synthetic counter, not
  independent evidence of a real effect).
- The empty trail establishes that **no** real-world effect occurred — **CANNOT ESTABLISH**.

Headline: *a missing evidence record cannot, by itself, establish that an action did not
occur; and a synthetic execution counter does not independently establish that a real-world
effect occurred.*

## Source (pinned)

Reconstructed from `holland202/sovereign-veritas` at commit
`fd5cac90587ba65d713b652ac743a8f240860aaa`:
- `docs/EXECUTION_BOUNDARY_PREREG.md`
- `docs/EXECUTION_BOUNDARY_RESULTS.md`
- `tools/execution_boundary_probe.py`

The finding's references link to the files at that exact commit; the X5 driving facts were
re-read verbatim there. The experiment carries no dedicated cryptographic evidence manifest
(public source pinned to the commit above); the probe was not independently re-executed.

## Limitations

One synthetic case; the executor is a counting stub (not independent evidence of a real
effect); integrity rests on the pinned commit, not a dedicated manifest; the probe was not
re-run. No legal or safety conclusion is drawn.

## Files

- `finding.pdf` — the finding (full reasoning: propositions, states, provenance, limitations)
- `finding.md` — Markdown of the same
- `finding.json` — machine-readable
- `SHA256SUMS` — digests of the three files above

Verify: `sha256sum -c SHA256SUMS`
