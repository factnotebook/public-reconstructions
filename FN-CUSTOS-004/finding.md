# FN-CUSTOS-004 — Observation vs inference: the determining-cause gap under the observed-equivalence instrumentation

**Prepared for** Tavares Heath — fourth reconstruction (run 12): does observation close the determining-cause gap the run-11 inference left open?  
**Reconstruction ID** `FN-b67b3d8fadbb891b`  
**Engine version** camsva 0.9.0  
**Generated** 2026-10-18  
**Status** Reconstruction: FINAL — BOUNDED (closed against the specified admitted observation set and rules; does not establish completeness, independent production, or the absence of other relevant evidence). Publication: PENDING SUBJECT REVIEW

## Purpose & boundary

This states, per proposition, what the records **establish**, **contradict**, or **cannot establish**.

STRICTLY NON-DISPOSITIVE, and this reconstruction is the planned test of a loop, not a new experiment. Roles, no overlap: CUSTOS-CORE defined and exercised the control and shipped the additional instrumentation; the workflow produced run 12; FactNotebook reconstructs what that record supports, contradicts or cannot establish. FN did not enforce, re-run or control anything; run 11 (FN-CUSTOS-003) stands exactly as recorded. The result is the point of the series. In run 11, determining-cause was CANNOT ESTABLISH — a bounded inference, because tracked-state equivalence was inferred (not observed), the clean probe's code was not hash-bound, and untracked / environmental deltas were not excluded. That honest CANNOT ESTABLISH specified the instrumentation; the subject shipped it; run 12 now OBSERVES the tracked dimension (identical probe-script hash and commit across phases; clean porcelain with no tracked modification; injected porcelain enumerating exactly one tracked change — the gate). What that buys is DOCUMENTARY, and the finding keeps it there: run 12 strengthens the recorded equivalence of the git-TRACKED states — the single tracked delta is the gate (P2, ESTABLISHED), and the non-gate differences the porcelain records are untracked recording artifacts (P3, ESTABLISHED). What run 12 does NOT do is turn that tighter observation into causal attribution: the determining-cause proposition (P4) stays CANNOT ESTABLISH, because a `git status --porcelain` observes git-tracked working-tree state — not all filesystem state, not the bytes loaded in memory, not non-filesystem environmental or runtime factors; the untracked set itself differs between phases; and on-disk tracked state is not a hash of the executed bytes. A better observation is not a causal proof. And a downstream tool execution or external effect (P5) stays CANNOT ESTABLISH at the authorization-decision boundary. The untracked entries are the recording channel's own footprint (the subject disclosed this); they are enumerated and kept as a separate observation (P3), not folded into the tracked delta. The demonstration — and the falsifiability discipline this run is meant to show — is that FactNotebook took a real gain in observability and reported exactly what it establishes (tighter documentary equivalence) WITHOUT letting it masquerade as the causal result it cannot support. An independent reconstruction does not change the past; a subsequent one can change what the next record makes provable — here it moved an inference to an observation for the tracked dimension, and no further. No Exempt Node: every observation is a re-hashed record from the subject's own frozen run.

## Provenance & processing

Every observation points to one public CI run (38811246068 / run 12, commit b06098c), frozen in-repo at docs/red-proof-records/run-38811246068/ with a SHA-256 manifest (MANIFEST.md). Every digest this reconstruction cites — the evidence record, both instrumented probe artifacts, the JUnit, pytest output and exit code — was re-fetched and re-hashed here and MATCHES the manifest (digest concordance; the files remain products of the same workflow run, so this is corroboration, not mutual independence of source). Publication is gated on the subject's review.

## Scope & coverage

Records were constituted and supplied by Tavares Heath's CUSTOS-CORE red-proof CI (the SUBJECT; public repo ceyptoslim/CUSTOS-CORE, AGPL). Run 12 is the subject's own CI output, frozen in-repo; not a source independent of the subject, and admitted without selective exclusion of candidate observations — all extracted candidates were admitted. This finding is bounded to that submitted surface; the absence of internal selection does not establish the submission's completeness relative to the represented system, nor whether an adverse class of observations was withheld — that completeness is **not established**.
 *(see Annex C — acquisition / selection boundary; Annex B — non-admitted candidate register)*

## Results

*Every tested proposition with its engine state and, where one applies, the determining limitation. Full detail follows below.*

| Proposition | State | Determining limitation |
|---|---|---|
| P1-verdict-follows-rule — the recorded verdict RED-CONFIRMED follows the declared rule (pytest_exit_code != 0 -> RED-CONFIRMED) applied to the recorded exit code (1) | **ESTABLISHED** | — |
| P2-tracked-delta-observed — the only git-TRACKED difference between the clean (DENY) and injected (ALLOW) working trees is the one-line injection to custos/action_gate.py, and both phases ran a hash-identical probe script (same SHA-256) at the same commit | **ESTABLISHED** | — |
| P3-untracked-footprint-classified — the working-tree differences recorded in the injected porcelain other than the gate modification are untracked entries, classified in the record — by filename and the subject's declaration — as the run's own recording artifacts (the injection-diff patch and the probe output files) | **ESTABLISHED** | — |
| P4-determining-cause — the injected gate modification is the determining cause of the clean -> injected DENY -> ALLOW change | **CANNOT ESTABLISH** | causal attribution NOT established — git-status observes git-tracked state, not all filesystem / loaded-memory / non-filesystem (env, clock, runtime) state; a tighter observation (P2) is not causal proof |
| P5-downstream-effect — a downstream tool execution or external effect occurred as a result of the ALLOW | **CANNOT ESTABLISH** | authorization-decision boundary — ALLOW is a gate decision, not an executed action or external effect |

## 1 — What observation now establishes

| Proposition | State | Basis |
|---|---|---|
| the recorded verdict RED-CONFIRMED follows the declared rule (pytest_exit_code != 0 -> RED-CONFIRMED) applied to the recorded exit code (1) | **ESTABLISHED** | ESTABLISHED. From the record (frozen in-repo, re-hashed against MANIFEST.md): exit code 1; rule 'exit_code != 0 -> RED-CONFIRMED'; verdict RED-CONFIRMED. Internal consistency of the record — the same check as run 9 / v3 / run 11 |
| the only git-TRACKED difference between the clean (DENY) and injected (ALLOW) working trees is the one-line injection to custos/action_gate.py, and both phases ran a hash-identical probe script (same SHA-256) at the same commit | **ESTABLISHED** | ESTABLISHED — a DOCUMENTARY observation, and the one run 11 lacked. Run 11 INFERRED tracked-state equivalence from the sealed diff plus same-job sequencing; run 12's instrumentation OBSERVES it: both probe phases record a hash-identical probe script (ae197f3e…) and the same commit (b06098c); the clean phase's porcelain shows no tracked modification; the injected phase's porcelain enumerates exactly one tracked change — custos/action_gate.py. What is established is what the git-TRACKED record shows — a real gain in observability over run 11. It is NOT a claim that no other factor differs between the two executions (that is P4): git-tracked state is narrower than all filesystem / loaded-memory state |
| the working-tree differences recorded in the injected porcelain other than the gate modification are untracked entries, classified in the record — by filename and the subject's declaration — as the run's own recording artifacts (the injection-diff patch and the probe output files) | **ESTABLISHED** | ESTABLISHED — documentary, and the honest treatment of the subject's disclosed footprint. The injected porcelain's non-gate entries are '?? red-proof-injection-diff.patch', '?? red-proof-probe-clean.json' and '?? red-proof-probe-injected.json' — untracked, and by name the run's own recording artifacts; the clean porcelain's only entry is its own output. This records the recording channel's footprint as a first-class observation, kept SEPARATE from the single tracked delta (P2), neither folded into it nor scrubbed. Scoped to what the porcelain enumerates: it does not establish that these are the ONLY filesystem differences, only that the differences the capture records, other than the gate, are these attributable untracked artifacts. Reservation: classifying these untracked files AS the instrumentation's own outputs rests on their filenames matching the run's artifacts plus the subject's declaration — a DECLARED classification, not an independent verification of their origin |

## Limitations

- **P4-determining-cause** — *the injected gate modification is the determining cause of the clean -> injected DENY -> ALLOW change* → **CANNOT ESTABLISH** (causal attribution NOT established — git-status observes git-tracked state, not all filesystem / loaded-memory / non-filesystem (env, clock, runtime) state; a tighter observation (P2) is not causal proof). CANNOT ESTABLISH — and this is the correction the discipline demands. A `git status --porcelain` capture observes GIT-TRACKED working-tree state — NOT all filesystem state, NOT the bytes loaded in memory at execution, and NOT non-filesystem environmental or runtime factors (environment variables, clock, installed libraries, interpreter/runtime nondeterminism, external services). So 'only one git-tracked file changed' is a documentary observation (P2), not a demonstration that the injection is the factor that PRODUCED the decision change. The untracked set itself differs between the two phases (P3), and an on-disk tracked-state observation is not a hash of the executed bytes. Run 12 TIGHTENS the inference considerably over run 11 — the tracked equivalence is now observed rather than inferred — but causal attribution does not follow automatically from a tighter observation. Honest result: run 12 strengthens the DOCUMENTARY equivalence of the tracked states; it does not establish that the injection is the determining cause of the decision change
- **P5-downstream-effect** — *a downstream tool execution or external effect occurred as a result of the ALLOW* → **CANNOT ESTABLISH** (authorization-decision boundary — ALLOW is a gate decision, not an executed action or external effect). CANNOT ESTABLISH. The recorded ALLOW is a gate DECISION at the authorization-decision boundary — the gate permitted an un-registered tool — NOT evidence that the tool then executed or that any external effect occurred. This boundary is held on both sides (the subject preserves it too) and is the same line drawn in FN-CUSTOS-003 and the Sovereign Veritas X5 reconstruction between a recorded decision and a real effect

## Separation of authority

*Observation instruments determine what they observe and propose. Admission (where the instrument's contract requires it) determines what may enter the reconstruction record. FactNotebook determines what that admitted record permits us to establish about the proposition. An instrument may search, select, transform or directly acquire observations according to its own declared procedure; those operations remain attributable properties of the instrument, not hidden properties of the reconstruction engine.*

- recorded behaviour → **observation** (attributed to its instrument)
- declared risk / rule classifications → **the evaluator's / authority's policy** (never engine facts)
- the consequential judgment → **the accountable authority**, outside this reconstruction

## Re-derivability

Two levels are preserved. **The finding** re-derives: re-running the reconstruction against the admitted observations reproduces the reconstruction identifier `FN-b67b3d8fadbb891b` and the states above — no re-run of the probabilistic extraction is needed. **The admitted record's boundary** is separately inspectable: the candidate admission register (Annexes A/B) traces how the admitted set was constituted from the candidates, and Annex C how the candidates were constituted from the surface. *Version the instrument · trace the extraction · freeze the admitted record · replay the reconstruction.*

---

*FactNotebook reconstructs what can be established from the surviving records — including what cannot be — and keeps the establishment separate from the judgment applied to it.*

## References

*Each observation points to a citable source a third party can re-walk; the status records how it was verified.*

- **CUSTOS-CORE red-proof record — run 12 (38811246068), class 003-weaken-action-gate + 003-probe** — workflow_dispatch, post-merge PR #55, commit b06098c; first run with observed-equivalence probe instrumentation; verdict RED-CONFIRMED, exit 1; injection_diff_sha256 74456f76… (same injection as run 11); both probe artifacts carry probe_script_sha256 ae197f3e… + git_commit_sha b06098c + a git status --porcelain capture · _PRIMARY — frozen in-repo; every cited digest re-hashed here, matches MANIFEST.md_ · https://github.com/ceyptoslim/CUSTOS-CORE/tree/main/docs/red-proof-records/run-38811246068
- **Observed equivalence (003-probe clean + injected)** — clean porcelain '?? red-proof-probe-clean.json' (no tracked modification); injected porcelain 'M custos/action_gate.py' + 3 untracked record artifacts; tracked delta = one file (the gate); identical probe_script_sha256 and commit across both phases · _PRIMARY — frozen in-repo; both artifacts re-hashed here, match MANIFEST.md_ · docs/red-proof-records/run-38811246068/003-probe/ (red-proof-probe-clean.json, red-proof-probe-injected.json)
- **The before/after — run 11 (FN-CUSTOS-003)** — FN-CUSTOS-003 (recon FN-da06acd59938f5b9) held determining-cause at CANNOT ESTABLISH as a bounded inference (tracked equivalence inferred from the sealed diff + same-job; clean code not hash-bound; untracked/env not excluded). Run 12 observes the tracked dimension that run 11 inferred; run 11 stands as recorded · _REFERENCE — the inference this run tests by observation_ · docs/red-proof-records/run-38610363998/ (run 11, frozen)
- **Observation register (obs -> provenance -> integrity -> probative role)** — Observation count (3) is not proposition count (5). P1 <- record verdict/exit (A2). P2 <- the two instrumented probe artifacts: identical script SHA + commit, clean porcelain no-tracked-mod, injected porcelain one-tracked-file = the gate (A2, DOCUMENTARY: the git-tracked delta). P3 <- the injected porcelain's non-gate entries, enumerated as the run's own untracked recording artifacts (A2, DOCUMENTARY: the recording footprint, classified by filename + the subject's declaration). The two CANNOT ESTABLISH have NO establishing observation: P4-determining-cause (a git-tracked observation does not establish causal attribution — non-filesystem env/runtime and executed bytes not observed) and P5-downstream-effect (authorization-decision boundary). All three observations are products of the same workflow run — same-workflow corroboration, not mutual independence · _ADMISSION — three direct observations from one frozen, re-hashed CI run drive five propositions_ · per-proposition detail in the sections above
- **Frozen reconstruction manifest (the inputs a replay fixes)** — reconstruction_id FN-b67b3d8fadbb891b · observation_model FN-CUSTOS-004 hash sha256:d12f412337f266dce78ab131996b6a45089670601e57ea4ac0e5e57ceafd7cf7 · observation_set hash sha256:b14279ecc8ba22c355d124cafe0464dd1a59603efcaac948c989ba49a49c2f67 (3 observations: o_7f44629e29db5ea0, o_a5e69068336b3c43, o_e120290f7b99fc27) · rule versions fn-reconstruction-engine-v1 / fn-rule-pattern-v1 / fn-composition-v1 / fn-temporal-v1 / fn-canon-v1. Internal determinism: re-running against the frozen run-12 inputs reproduces the identifier and the five proposition outcomes; verification is at the OBSERVATION level — the frozen set (docs/red-proof-records/run-38811246068/, MANIFEST.md) can be re-fetched and re-hashed by anyone · _FROZEN — mirrors Annex D binding_ · Annex D (binding)

## Annexes

### A. Admitted observation set

*The admitted half of the candidate admission register. Each was an accountable ADMIT decision (determiner and criterion below); the full register — every candidate, admitted or rejected — is in the machine-readable finding.*

| Candidate | Observation | Primary | SHA-256 | Anchor | Corroboration | Determination by | Criterion |
|---|---|---|---|---|---|---|---|
| obs-verdict | run:38811246068 · verdict_consistent_with_declared_rule | 003-weaken-action-gate/red-proof-evidence.json | `f511474a106b…` | — | single (frozen CI record (run 38811246068); same-workflow) | FactNotebook | direct machine record; re-hashed vs MANIFEST.md (match); contributes to P1 |
| obs-tracked-delta | run:38811246068 · tracked_delta_is_the_gate_observed | 003-probe/red-proof-probe-{clean,injected}.json | `26c4ac9bb7ca…` | — | single (frozen CI record (run 38811246068); same-workflow) | FactNotebook | clean (b1a5ad1a…) + injected (26c4ac9b…) porcelain + identical script-SHA/commit, re-hashed vs MANIFEST.md (match); contributes to P2 |
| obs-untracked-footprint | run:38811246068 · untracked_entries_classified_as_recording_artifacts | 003-probe/red-proof-probe-injected.json | `26c4ac9bb7ca…` | — | single (frozen CI record (run 38811246068); same-workflow) | FactNotebook | injected porcelain's non-gate entries enumerated as the run's own artifacts; contributes to P3 |

### B. Non-admitted candidate register

*Every candidate was admitted: none rejected, none left unresolved.*

### C. Acquisition / selection boundary

Records were constituted and supplied by Tavares Heath's CUSTOS-CORE red-proof CI (the SUBJECT; public repo ceyptoslim/CUSTOS-CORE, AGPL). Run 12 is the subject's own CI output, frozen in-repo; not a source independent of the subject, and admitted without selective exclusion of candidate observations — all extracted candidates were admitted. This finding is bounded to that submitted surface; the absence of internal selection does not establish the submission's completeness relative to the represented system, nor whether an adverse class of observations was withheld — that completeness is **not established**.

*Chain of custody of how the observation surface became a reconstruction — each actor plays a distinct role:*

| Role | Actor |
|---|---|
| Surface constituted / submitted by | Tavares Heath's CUSTOS-CORE red-proof CI (the SUBJECT; public repo ceyptoslim/CUSTOS-CORE, AGPL). Run 12 is the subject's own CI output, frozen in-repo; not a source independent of the subject |
| Submission form | one public CI run (38811246068 / run 12, commit b06098c, first run with observed-equivalence probe instrumentation): evidence record, instrumented clean+injected probe artifacts, JUnit, pytest output, exit-code and sealed injection-diff — frozen in-repo at docs/red-proof-records/run-38811246068/ (MANIFEST.md) and re-hashed here (match) |
| Candidate extraction instrument | the subject's CI (pytest under the known sabotage patch, no -x; control probe on clean + injected builds now recording probe_script_sha256 + commit + git-status porcelain). FactNotebook re-reads the frozen record; it does NOT re-run the suite or the probe |
| Admission authority / mechanism | FactNotebook (proposer). Every cited digest re-hashed against the frozen MANIFEST.md and matches (digest concordance — the retrieved bytes match the manifest, distinct from correspondence to the original CI run and from independence of production, which the record does not establish). Same-workflow corroboration, not independence. Not an independent audit |
| Reconstruction engine | camsva 0.9.0 |

| Property | Value |
|---|---|
| Surface type | submitted |
| Acquisition mode | submitted bundle — no candidate selection |
| Period | run 38811246068, commit b06098c, probe at 2026-10-15T21:37:33Z |
| Known limitations | One run (run 12), one control (the pre-flight action gate), the same injection class as run 11. The observed-equivalence instrumentation strengthens the DOCUMENTARY characterization of the git-tracked delta (P2) and identifies the untracked recording artifacts present in the captures (P3). Neither observation establishes that the gate modification was the determining cause of the DENY-to-ALLOW decision change (P4, CANNOT ESTABLISH): a git-status capture observes git-tracked working-tree state, not all filesystem / loaded-memory / non-filesystem environmental or runtime state. The probe's own outputs appear as untracked entries in the porcelain (the recording channel's footprint, disclosed by the subject); they are enumerated and kept separate from the single tracked delta, and their classification as instrumentation artifacts is declared (by filename + the subject's statement), not independently verified. The ALLOW is a gate decision, not downstream execution or an external effect (P5). Digest concordance only; not independent production. What is established is what the preserved record permits — not that CUSTOS-CORE's controls are adequate. |

### D. Policy & engine binding

- **Engine** camsva 0.9.0
- **Reconstruction ID** `FN-b67b3d8fadbb891b`
- **Binding** `{'observation_model': {'id': 'FN-CUSTOS-004', 'version': None, 'hash': 'sha256:d12f412337f266dce78ab131996b6a45089670601e57ea4ac0e5e57ceafd7cf7'}, 'policy': None, 'engine': {'engine_version': 'fn-reconstruction-engine-v1', 'rule_language_version': 'fn-rule-pattern-v1', 'composition_version': 'fn-composition-v1', 'temporal_policy_version': 'fn-temporal-v1', 'canonicalization_version': 'fn-canon-v1'}, 'observation_set': {'hash': 'sha256:b14279ecc8ba22c355d124cafe0464dd1a59603efcaac948c989ba49a49c2f67', 'selected_count': 3, 'excluded_by_window': 0, 'window': None, 'custody_verified': False, 'closed_at': '2026-10-18T20:20:06+00:00', 'selected_ids': ['o_7f44629e29db5ea0', 'o_a5e69068336b3c43', 'o_e120290f7b99fc27'], 'excluded_ids': [], 'selection_note': 'bounded observation SELECTION by t_event; not temporal inference over the interval'}}`
