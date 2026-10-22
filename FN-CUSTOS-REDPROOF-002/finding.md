# FN-CUSTOS-REDPROOF-002 — Establishability lifecycle: the same four propositions on an improved record

**Prepared for** Tavares Heath — second reconstruction (v3 record), the 'after' of a before/after pair  
**Reconstruction ID** `FN-63a3bbfc57791b7c`  
**Engine version** camsva 0.9.0  
**Generated** 2026-10-14  
**Status** FINAL — BOUNDED

## Purpose & boundary

This states, per proposition, what the records **establish**, **contradict**, or **cannot establish**.

STRICTLY NON-DISPOSITIVE, and that is the point of this second reconstruction. FactNotebook did not enforce, re-run or control anything about CUSTOS-CORE. The FIRST reconstruction (FN-CUSTOS-REDPROOF-001, run 9, record v2) established three propositions and marked three limits honestly: coverage of the regression class was CANNOT ESTABLISH (pytest -x stopped at the first failure), the exact exit code lived only in the field asserting the verdict, and the injection→failure causal step was reproducible but not bound. The subject then shipped a v3 record that addresses exactly those three — fail-fast removed, a separate hashed exit-code artifact, and a SHA-256-sealed post-injection diff bound into the record identity. Reconstructing the same four propositions over the v3 record: P1 unchanged (ESTABLISHED); P2 ESTABLISHED and stronger (the exit code is now on its own channel); P3 ESTABLISHED and stronger (the intended modification is now recorded in a contemporaneously preserved, hash-bound diff rather than inferred solely from the injection script); and P4 moves from CANNOT ESTABLISH to ESTABLISHED — with fail-fast removed the run completed (506 tests; 465 passed, 6 failed, 35 skipped) and all six intended admin-auth rejection assertions failed under the injection, matching the subject's manual baseline. This status change does NOT mean the truth of the past changed: it means the observations available for this new run support a proposition the earlier run's observations could not — each reconstruction is bound to its own observation set. An independent reconstruction's honest 'cannot establish' and its marked limits functioned as a specification for better evidence; the third-party system improved its own instrument within a day; the states then moved as the evidence did. No conclusion here exceeds its observations, and none of it required FactNotebook to take control of the system it reconstructs. No Exempt Node: every observation is an independently retrieved, hash-verified record. Re-derivability here is internal determinism (the engine is not public); the frozen inputs are in the 'Frozen reconstruction manifest' reference and Annex D, and the public artifacts can be re-fetched and re-hashed by anyone — including the permanently frozen run-9 'before' set now stored in-repo.

## Provenance & processing

Every observation points to a public, re-walkable artifact. The v3 evidence record, JUnit, pytest output, exit-code artifact and sealed injection-diff were retrieved via the nightly.link public proxy; every internal SHA-256 — including the injection_diff hash bound into the record identity — was recomputed here and matched. Matching digests show CONSISTENCY between the retrieved files and the record's references, not by itself an attestation of production; the run executing and returning non-zero is attested separately by GitHub's job-step outcomes.

## Scope & coverage

Records were selected and supplied by Tavares Heath's CUSTOS-CORE 'red-proof' CI (the SUBJECT; public repo ceyptoslim/CUSTOS-CORE, AGPL). The records are the subject's own CI output (v3 record spec), published on GitHub; FactNotebook retrieved and SHA-256-verified them itself. They are NOT an independent-of-subject source; the only separately-hosted corroboration (GitHub's own job-step outcomes) still depends on the same workflow execution. This finding is bounded to that submitted surface; completeness beyond it — and whether an adverse class of observations was withheld — is **not established**. The instrumentation was **selective**, not exhaustive: a selective extraction is not an exhaustive observation of the surface.
 *(see Annex C — acquisition / selection boundary; Annex B — non-admitted candidate register)*

## 1 — Verdict consistency

| Proposition | State | Basis |
|---|---|---|
| the recorded verdict RED-CONFIRMED follows the declared verdict rule (pytest_exit_code != 0 -> RED-CONFIRMED) applied to the recorded exit code (1) | **ESTABLISHED** | From the v3 record (SHA-verified): pytest_exit_code = 1; rule 'exit_code != 0 -> RED-CONFIRMED'; verdict = RED-CONFIRMED. 1 != 0 => RED-CONFIRMED. Internal consistency of the record — unchanged from run 9 |

## 2 — Recorded outcome ↔ execution evidence

| Proposition | State | Basis |
|---|---|---|
| the recorded non-zero pytest outcome (a test genuinely failed) is corroborated by the preserved execution reports and GitHub's observed workflow behaviour, and the exact exit code is now recorded on a channel separate from the field that asserts the verdict | **ESTABLISHED** | The pytest output (hash-matched) reads '6 failed, 465 passed, 35 skipped'; the JUnit (hash-matched) carries failures='6'. STRENGTHENED since run 9: the exit code '1' is now written to its own hashed artifact (red-proof-exit-code.txt, SHA-256 4355a46b…), observable separately from the record's verdict field. GitHub's separately-hosted job steps corroborate exit_code != 0 (dependent on the same workflow execution). The run-9 limitation — the integer living only in the verdict-asserting field — is ADDRESSED, within scope: this is better artifact separation, NOT full source independence — the exit-code file and the JSON field both derive from the same workflow run and the same shell variable |

## 3 — Substantive detection

| Proposition | State | Basis |
|---|---|---|
| during run 38495005061 the intended admin-auth assertions failed with exactly the symptom the injected regression produces — admin endpoints no longer requiring authentication | **ESTABLISHED** | STRENGTHENED since run 9: the post-injection `git diff` is now CAPTURED and its SHA-256 BOUND into the record identity (injection_diff_sha256 29d73e8f…). The preserved diff RECORDS the intended code modification, and its digest is bound to the evidence record — the diff shows main.py `return verify_token(credentials)` -> `return None` at both auth points (the observed CONTENT of the modification, distinct from the event that produced it). The six failing tests are the intended auth-rejection assertions (e.g. /v1/audit returned 200, invalid token accepted) — exactly the effect of disabling token verification. The causal step from the bound modification to the failures is now strongly grounded (observed modification + matching symptom across six assertions). Reservation kept: the bound diff records the modification contemporaneously, but the hash does not by itself prove the executed code was EXACTLY the diffed code; a fully formal before/after execution proof would still be more demanding, and FactNotebook does not re-run |

## 4 — Coverage of the regression class

| Proposition | State | Basis |
|---|---|---|
| all six IDENTIFIED admin-auth rejection assertions executed in this run failed under the injected modification | **ESTABLISHED** | ESTABLISHED — and this is the state that MOVED. In run 9 this was CANNOT ESTABLISH because pytest ran with -x and stopped at the first failure. In v3 fail-fast (-x) is removed: the run completed (506 tests; 465 passed, 6 failed, 35 skipped) and the six failing tests are all admin-auth rejection assertions — test_audit_endpoints_reject_missing_token, test_replay_rejects_missing_token, test_tenant_register_rejects_missing_token, test_tenant_delete_rejects_missing_token, test_invalid_token_rejected (TestAdminEndpointsRequireAuth), test_production_disables_auth_bypass (TestAuthEnforcement). IDENTIFICATION CRITERION for 'the relevant set': tests that assert a protected endpoint returns 401 on a missing/invalid bearer token — exactly the control the sabotage disables (verify_token -> None). What is ESTABLISHED is the NARROW proposition: these six named, executed assertions all failed under the injection (directly verifiable in the JUnit). What is NOT claimed: that these six are an EXHAUSTIVE set of every conceivable auth regression — that would require classifying the whole suite's scope, which this record does not do. The run-9 coverage limitation is addressed, within that stated scope, by evidence rather than argument. This does not change what run 9 established: it is a different run whose observations support what the earlier run's could not |

## Separation of authority

*Observation instruments determine what they observe and propose. Admission (where the instrument's contract requires it) determines what may enter the reconstruction record. FactNotebook determines what that admitted record permits us to establish about the proposition. An instrument may search, select, transform or directly acquire observations according to its own declared procedure; those operations remain attributable properties of the instrument, not hidden properties of the reconstruction engine.*

- recorded behaviour → **observation** (attributed to its instrument)
- declared risk / rule classifications → **the evaluator's / authority's policy** (never engine facts)
- the consequential judgment → **the accountable authority**, outside this reconstruction

## Re-derivability

Two levels are preserved. **The finding** re-derives: re-running the reconstruction against the admitted observations reproduces the reconstruction identifier `FN-63a3bbfc57791b7c` and the states above — no re-run of the probabilistic extraction is needed. The admitted set equals the full candidate set in this reconstruction; no detailed per-candidate admission register was produced. The acquisition boundary is documented in Annex C; a separately reviewed admission pass would produce a traceable register. *Version the instrument · trace the extraction · freeze the admitted record · replay the reconstruction.*

---

*FactNotebook reconstructs what can be established from the surviving records — including what cannot be — and keeps the establishment separate from the judgment applied to it.*

## References

*Each observation points to a citable source a third party can re-walk; the status records how it was verified.*

- **CUSTOS-CORE red-proof evidence record v3 (001-weaken-admin-auth)** — run_id 38495005061, commit 925f96eabebf…, record_version 3, pytest_exit_code 1, verdict RED-CONFIRMED; binds injection_diff_sha256 29d73e8f… into the record identity; references an exit-code artifact and a sealed injection-diff artifact in addition to JUnit + pytest output · _PRIMARY — independently retrieved (nightly.link); every internal SHA-256 recomputed here and matched_ · https://github.com/ceyptoslim/CUSTOS-CORE/actions/runs/38495005061
- **Execution evidence (JUnit + pytest output), full failure set (no -x)** — 506 tests, 6 failed, 465 passed, 35 skipped; the 6 failures are the intended admin-auth rejection assertions (matching the subject's manual baseline of 6 auth failures) · _PRIMARY — nightly.link; SHA-256 5ffa02dc… / d8b9e12d… match the record_ · artifact red-proof-records-001-weaken-admin-auth (run 38495005061)
- **Sealed injection diff + exit-code artifact** — injection diff 29d73e8f… = main.py return verify_token(credentials) -> return None at both auth points; exit-code artifact 4355a46b… = '1', recorded before the evidence record is generated · _PRIMARY — nightly.link; SHA-256 bound into the record identity (diff) / own hashed file (exit code)_ · artifacts red-proof-injection-diff.patch / red-proof-exit-code.txt
- **GitHub-hosted job-step outcomes** — run 38495005061: both sabotage jobs conclude success; each 'Red confirmed' step (guarded by exit_code != 0) ran => exit != 0 · _SEPARATELY-HOSTED — GitHub Actions public API; recorded apart from the subject's evidence artifact but dependent on the same workflow execution_ · https://api.github.com/repos/ceyptoslim/CUSTOS-CORE/actions/runs/38495005061/jobs
- **Permanently frozen run-9 observation set (the 'before')** — FN-CUSTOS-REDPROOF-001 reconstructed run 38446904362 (record v2, -x); this v3 reconstruction is the 'after' · _REFERENCE — the first reconstruction's inputs, now frozen in-repo with a SHA-256 manifest (outlives GitHub's 90-day expiry)_ · https://github.com/ceyptoslim/CUSTOS-CORE/tree/main/docs/red-proof-records/run-38446904362
- **Observation register (obs → provenance → integrity → probative role)** — P1 ← evidence record v3 (provenance: subject CI output; integrity: record SHA-verified; role: internal verdict↔rule consistency). P2 ← JUnit + pytest output + exit-code artifact + GitHub job steps (integrity: all SHA-256 matched, GitHub separately-hosted; role: the recorded non-zero outcome is faithful). P3 ← sealed injection-diff (bound into record identity) + full failure set (integrity: diff SHA-256 matched in observations AND identity; role: identified assertions failed with the injection's symptom). P4 ← full failure set, JUnit (integrity: JUnit SHA-256 matched; role: the six identified admin-auth rejection assertions executed all failed). Common dependency noted: the JUnit/pytest-output and the exit-code and diff artifacts are all products of the SAME workflow run — corroboration, not mutual independence · _ADMISSION — all four observations are direct machine records (no interpretive candidate); SHA-256 verified; admitted without an interpretive admission step. A per-candidate register would be produced by a separate reviewed admission pass_ · per-proposition detail in sections 1–4 above
- **Frozen reconstruction manifest (the inputs a replay fixes)** — reconstruction_id FN-63a3bbfc57791b7c · observation_model FN-CUSTOS-REDPROOF-002 hash sha256:9ae5095260d99a3e2fa0f0ba7731bfc3773992a00a1fbe3ff5cc0ecf0b20aa97 · observation_set hash sha256:deacd5eb4e26899a2ff90f8a413ae828bef9d4cdc0eefd61d618783d3556da40 (4 observations: o_9c51ddbde6702d0c, o_a1a6e047210b04e2, o_a6e3b2c20bb0e9fe, o_c990ed4cdbb1a7f9) · rule versions fn-reconstruction-engine-v1 / fn-rule-pattern-v1 / fn-composition-v1 / fn-temporal-v1 / fn-canon-v1. Internal determinism: re-running against these frozen inputs reproduces the identifier and the four states; the engine is not public, so independent verification is at the OBSERVATION level — the public artifacts above can be re-fetched and re-hashed by anyone · _FROZEN — mirrors Annex D binding_ · Annex D (binding)

## Annexes

### A. Admitted observation set

*(register not supplied — admitted set is the record set named above)*

### B. Non-admitted candidate register

*Every candidate was admitted: none rejected, none left unresolved.*

### C. Acquisition / selection boundary

Records were selected and supplied by Tavares Heath's CUSTOS-CORE 'red-proof' CI (the SUBJECT; public repo ceyptoslim/CUSTOS-CORE, AGPL). The records are the subject's own CI output (v3 record spec), published on GitHub; FactNotebook retrieved and SHA-256-verified them itself. They are NOT an independent-of-subject source; the only separately-hosted corroboration (GitHub's own job-step outcomes) still depends on the same workflow execution. This finding is bounded to that submitted surface; completeness beyond it — and whether an adverse class of observations was withheld — is **not established**. The instrumentation was **selective**, not exhaustive: a selective extraction is not an exhaustive observation of the surface.

*Chain of custody of how the observation surface became a reconstruction — each actor plays a distinct role:*

| Role | Actor |
|---|---|
| Surface constituted / submitted by | Tavares Heath's CUSTOS-CORE 'red-proof' CI (the SUBJECT; public repo ceyptoslim/CUSTOS-CORE, AGPL). The records are the subject's own CI output (v3 record spec), published on GitHub; FactNotebook retrieved and SHA-256-verified them itself. They are NOT an independent-of-subject source; the only separately-hosted corroboration (GitHub's own job-step outcomes) still depends on the same workflow execution |
| Submission form | one public CI run (38495005061, record_version 3): evidence record, JUnit XML, pytest output, exit-code artifact, sealed injection-diff — published publicly, FN-retrieved |
| Candidate extraction instrument | the subject's CI (pytest under a known-bad sabotage patch, no -x) — FactNotebook re-reads the preserved artifacts, it does NOT re-run the suite |
| Admission authority / mechanism | FactNotebook (proposer). Acquisition + integrity (SHA-256, here including the injection-diff hash bound into the record identity) are kept distinct from admission and from relevance/sufficiency, which are appraised per proposition; the retrieved artifacts match the recorded digests, and their substantive claims remain subject to independent evaluation. Not an independent audit |
| Reconstruction engine | camsva 0.9.0 |

| Property | Value |
|---|---|
| Surface type | submitted |
| Acquisition mode | selective |
| Known limitations | Bounded to one run (38495005061, sabotage 001, record v3). Independently retrieved and SHA-256-verified; the suite was NOT re-run here. The three identified evidentiary limitations are addressed in the v3 record, within the stated scope: fail-fast (-x) is disabled (the run completed with 35 tests skipped), the exit code is on its own hashed artifact (better artifact separation, not full source independence), and the post-injection diff is sealed and bound into the record identity (recorded, though a hash does not alone prove executed == diffed). What is established is what the preserved record permits — not that CUSTOS-CORE's controls are adequate. |

### D. Policy & engine binding

- **Engine** camsva 0.9.0
- **Reconstruction ID** `FN-63a3bbfc57791b7c`
- **Binding** `{'observation_model': {'id': 'FN-CUSTOS-REDPROOF-002', 'version': None, 'hash': 'sha256:9ae5095260d99a3e2fa0f0ba7731bfc3773992a00a1fbe3ff5cc0ecf0b20aa97'}, 'policy': None, 'engine': {'engine_version': 'fn-reconstruction-engine-v1', 'rule_language_version': 'fn-rule-pattern-v1', 'composition_version': 'fn-composition-v1', 'temporal_policy_version': 'fn-temporal-v1', 'canonicalization_version': 'fn-canon-v1'}, 'observation_set': {'hash': 'sha256:deacd5eb4e26899a2ff90f8a413ae828bef9d4cdc0eefd61d618783d3556da40', 'selected_count': 4, 'excluded_by_window': 0, 'window': None, 'custody_verified': False, 'closed_at': '2026-10-14T02:25:25+00:00', 'selected_ids': ['o_9c51ddbde6702d0c', 'o_a1a6e047210b04e2', 'o_a6e3b2c20bb0e9fe', 'o_c990ed4cdbb1a7f9'], 'excluded_ids': [], 'selection_note': 'bounded observation SELECTION by t_event; not temporal inference over the interval'}}`
