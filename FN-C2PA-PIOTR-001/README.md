# FN-C2PA-PIOTR-001 — Separation of authorities: an independent admission pass

By **FactNotebook** — [factnotebook.com](https://factnotebook.com).
Readable case study: [factnotebook.com/audits/c2pa-admission](https://factnotebook.com/audits/c2pa-admission)

A bounded, **non-dispositive** reconstruction of a C2PA provenance case across four hops
(*signed ≠ delivered ≠ instrument ≠ published*), reconstructed **twice**: once as FactNotebook
proposed it, and once after an **independent admission pass** by a separate authority.

The instructive result is not the C2PA verdict. It is what happened when **observation, admission
and reconstruction were placed under separate authorities**: the system lost a conclusion without
declaring the underlying observation false.

## What the admission pass demonstrated

FactNotebook extracted records from the supplied evidence and **proposed** interpretive
observations. It did not admit its own candidates. An independent admission authority reviewed each
proposed observation against the records **he could independently verify**, and could **admit** it,
**require a correction**, or keep it **outside his admission scope**.

One candidate relied on a **PSNR content-match measurement** produced by a third party. The
admission authority had not run that measurement himself, so he did **not** admit it on the third
party's behalf. The measurement did not become false — it remains in the record, attributed to its
author — but it could not contribute to the reconstruction under his admission authority.

That changed the result of the content-match proposition:

> **ESTABLISHED → CANNOT ESTABLISH**

Not contradicted. Not disproven. The *authorized* record simply no longer permitted that
proposition to be established. The measurement stays a declared external result, **beside** the
admitted record rather than **inside** it.

## Three authorities, kept separate

- **Observation / measurement** — attributed to the instrument or the party that produced it
  (e.g. the validator-version/EKU divergence as the discoverer's finding; the PSNR as a declared
  external result).
- **Admission** — the independent authority decides what may enter the admitted record, strictly
  within what he can verify. He admits, corrects, or holds outside his scope.
- **Reconstruction** — FactNotebook determines what the *admitted* record permits one to establish
  about each proposition. It never admits its own candidates (**No Exempt Node**).

The consequential judgment stays with the accountable authority, outside this reconstruction.

## Public result (structural)

Twenty-one propositions across four hops, each marked `ESTABLISHED`, `CONTRADICTED`, or
`CANNOT ESTABLISH`, with its basis and limits. Representative outcomes:

- Hop 1 (signed state) — the declarations are `ESTABLISHED` *as declarations*; that a specific actor
  **produced** the asset is `CANNOT ESTABLISH`.
- Hop 2 (delivered) — the delivered representation `differs from the validating representation by an
  injected chunk` (`ESTABLISHED`); "delivered is Valid" is `CONTRADICTED`; the injecting actor is
  `CANNOT ESTABLISH`.
- Hop 3 (instrument) — the tool reports Valid (`ESTABLISHED`), but the verdict is
  **version/EKU-dependent** (`ESTABLISHED`); intrinsic validity is `CANNOT ESTABLISH`.
- Hop 4 (publication) — the served image does **not** carry the manifest (`CONTRADICTED`);
  **content-match is `CANNOT ESTABLISH`** (the PSNR held outside admission scope); byte-provenance is
  `CANNOT ESTABLISH`.

The register of candidate observations — admitted, corrected, and **held outside admission scope** —
is in `reconstruction.json` and in the finding (`finding.pdf`).

## Files

| File | What it is |
|---|---|
| `reconstruction.json` | the sealed reconstruction output — propositions, states, basis, and the candidate-admission register (outputs only; no engine, no rule patterns, no raw observation text) |
| `finding.pdf` | the human-readable finding |
| `SHA256SUMS` | digests of the files in this entry |

Publication of this reconstruction does **not** imply publication of the reconstruction engine.
What is published is the sealed *output* and the manifest committed to by the Reconstruction ID
`FN-785efaab56d2e1f7`; the engine, models and reading rules are not published.

---

Independent admission pass: **Piotr Reder** (eucomplyhub). Original technical work — the
validator-version/EKU divergence (independently reproduced by Piotr) and the PSNR content-match
measurement: **Hlias Staurou**. Both reviewed and confirmed how their contributions are represented,
and consented to this public worked example. Reconstruction: FactNotebook. Retrospective and
non-dispositive; the reconstruction engine is not published.
