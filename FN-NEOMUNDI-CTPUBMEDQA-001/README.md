# FN-NEOMUNDI-CTPUBMEDQA-001 — NeoMundi ControlTower / PubMedQA pilot

By **FactNotebook** — [factnotebook.com](https://factnotebook.com).
Readable dossier: [factnotebook.com/audits/neomundi/neomundi-controltower-pubmedqa-pilot-v01](https://factnotebook.com/audits/neomundi/neomundi-controltower-pubmedqa-pilot-v01/)

An independent, retrospective governance reconstruction over a **NeoMundi ControlTower** pilot:
**5 governed GPT-4o generations on PubMedQA**, on **real data — no synthetic evidence**. Two
coupled layers: **NeoMundi measures** runtime behaviour; **FactNotebook reconstructs** what a
third party can establish from those measurements — declared-vs-observed, each finding graded by
provenance, with **NOT ASSESSABLE** where no observation channel exists. FactNotebook's first
real reconstruction finding (FN-RF).

This entry publishes **outputs only** — what FactNotebook asserts and on what, not how it
computes. The reconstruction engine, models and reading rules are **not** published; this is
**not open source**. Non-public content is committed by SHA-256 hash in `manifest.json`, not
disclosed (a commitment, not a disclosure).

## Custody & external timestamping (RFC-3161)

Unlike a self-hash, this pilot's ingest boundary is anchored to an **external RFC-3161 timestamp
authority** (DigiCert). Two published tokens:

- `ingest.tsr` — anchors the ingested ControlTower export;
- `manifest.tsr` — anchors `manifest.json`.

Verify with the DigiCert public timestamp CA chain:

```
openssl ts -verify -data manifest.json -in manifest.tsr -CAfile <DigiCert chain>
```

The RFC-3161 anchor attests **when** a blob existed, not **what** it means, and integrity holds
**from generation time only**: no immutability and no counter-signature — the counter-signature
slot is left to an accountable authority, not the reconstruction's producer.

## Files

- `README.md` — this dossier summary (the full readable dossier is on the site, linked above)
- `manifest.json` — SHA-256 of every artifact in the package (hashes published; non-public content committed, not disclosed)
- `ingest.tsr`, `manifest.tsr` — DigiCert RFC-3161 timestamp tokens
- `SHA256SUMS` — digests of the published files

Retrospective and non-dispositive: it reconstructs what the available observations permit one to
establish, and leaves the decision with the accountable authority.
