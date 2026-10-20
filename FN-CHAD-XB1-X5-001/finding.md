# FN-CHAD-XB1-X5-001 — What can be established when the evidence trail is incomplete (XB-1, case X5)

**Prepared for** Chad Holland — Principia Artificialis / Sovereign Veritas (XB-1, case X5)  
**Reconstruction ID** `FN-9e087ff81fe3759f`  
**Engine version** camsva 0.9.0  
**Generated** 2026-10-15  
**Status** FINAL — BOUNDED

## Purpose & boundary

This states, per proposition, what the records **establish**, **contradict**, or **cannot establish**.

STRICTLY NON-DISPOSITIVE. Sovereign Veritas defines and exercises the control; the workflow produces the record; FactNotebook reconstructs what the published record supports, contradicts, or cannot establish. No internal mechanism of either project is relied on. TWO SURFACES are declared and never conflated, and each proposition names the one it is evaluated against: the PUBLISHED EXPERIMENT (its pre-registration, results and probe — the reported behaviour of a synthetic harness) and the SYSTEM'S EVIDENCE TRAIL (the ledger — what a downstream auditor relying on the evidence chain would have). The synthetic counter (effects=1) and the OSError are the experiment's own instrumentation: attributable observations against the experiment surface, but NOT the evidence chain and NOT independent evidence of a real external effect. The general conclusion the propositions carry: the published X5 experiment reports a synthetic effect despite a failed ledger write (PA, ESTABLISHED relative to the artifacts); the ledger alone cannot establish either execution or non-execution (P2, P6 — CANNOT ESTABLISH); and the experiment's own instrumentation provides additional, attributable observations, but not independent evidence of a real-world external effect (P4, CANNOT ESTABLISH). What the trail contradicts is bounded to recording and to the reported behaviour: it does not record the effect (P3), and within the experiment, zero records do not imply zero reported effects (P5) — the reported and recorded counts are dissociated (1 vs 0). The real contribution is that dissociation between the instrument's reported behaviour, the trace the recorder preserved, and what a reconstructor can establish from each — not any claim that an effect occurred without durable proof. Every state is relative to its admitted surface. Mirror of the GDPR record-gap case, correctly scoped: there 'no entry is a claim, not a default' on the access side; here 'no record is not, by itself, non-occurrence' on the effect side — which is why the world-level non-occurrence (P6) is CANNOT ESTABLISH, not CONTRADICTED. A semantic note on P1, P2 and P6: each asks whether the register lets one ESTABLISH authorization / execution / non-occurrence. CANNOT ESTABLISH means exactly that — the register does not permit establishing it, in either direction — not the narrower 'no entry is present' (a presence/absence fact), and not the meta-claim 'it is false that the register establishes execution'. The result concerns execution / non-occurrence evaluated from the register, not the mere presence of a row. No Exempt Node: FactNotebook reconstructs from the subject's own published artifacts and does not exempt itself.

## Provenance & processing

Three public, re-walkable artifacts (pre-registration, results, probe) plus the probe's reported result line for X5. The artifacts carry NO cryptographic integrity binding — no SHA-256, no hash chain (input_digest is the literal 'abc') — so integrity here is 'as published at the referenced commits', re-walkable by URL, not a hash-sealed manifest. That is weaker than a cryptographically bound bundle and is declared as such. The synthetic counting executor's output is the experiment's own instrumentation and is treated as a declared, non-independent signal throughout.

## Scope & coverage

Records were constituted and supplied by Chad Holland — Principia Artificialis / Sovereign Veritas (public repo holland202/sovereign-veritas). The XB-1 case X5 artifacts are the subject's own pre-registration, results and probe, published on GitHub; FactNotebook reads them as published. They are NOT a source independent of the subject, and admitted without selective exclusion of candidate observations — all extracted candidates were admitted. This finding is bounded to that submitted surface; the absence of internal selection does not establish the submission's completeness relative to the represented system, nor whether an adverse class of observations was withheld — that completeness is **not established**.
 *(see Annex C — acquisition / selection boundary; Annex B — non-admitted candidate register)*

## Results

*Every tested proposition with its engine state and, where one applies, the determining limitation. Full detail follows below.*

| Proposition | State | Determining limitation |
|---|---|---|
| PA-reported-dissociation — the published X5 run reports a synthetic effect (effects=1) while the ledger write fails (records=0) | **ESTABLISHED** | established relative to the published artifacts (reported behaviour, not the world) |
| P5-reported-inference — in the published X5 experiment, zero ledger records imply the synthetic executor reported zero effects | **CONTRADICTED** | published results report effects=1 / records=0 — reported effect ≠ recorded; refutes the inference within the experiment only |
| P3-effect-recorded — the X5 effect is recorded in the system's evidence trail | **CONTRADICTED** | the probe reports 0 ledger records (simulated write failure, OSError disk full); read from the published report, not an independent ledger inspection |
| P1-authorization — the authorization of the executed X5 action is established by the system's evidence trail | **CANNOT ESTABLISH** | ledger carries no proof — gate ALLOW observed in the artifacts but not persisted; absence in the ledger, not in the artifacts |
| P2-execution — the execution of the X5 action is established by the system's evidence trail | **CANNOT ESTABLISH** | ledger carries no proof — only the synthetic self-count (not independent/durable); absence does not contradict execution either |
| P4-real-effect — a real-world external effect occurred in X5 | **CANNOT ESTABLISH** | world-level, all observations — synthetic counter (not independent) AND empty trail; neither establishes a real external effect |
| P6-nonoccurrence — the system's evidence trail establishes that no real external effect occurred in X5 | **CANNOT ESTABLISH** | trail empty by a recording failure, not non-occurrence — the ledger settles neither execution nor non-execution |

## 1 — The published experiment (reported behaviour)

| Proposition | State | Basis |
|---|---|---|
| the published X5 run reports a synthetic effect (effects=1) while the ledger write fails (records=0) | **ESTABLISHED** | ESTABLISHED — relative to the published artifacts. The results report effects=1 / records=0 / errors=1 (as registered, 1/0/1) with the write raising OSError 'simulated write failure (disk full)'. This is a claim about the EXPERIMENT'S REPORTED BEHAVIOUR — the dissociation between the instrument's reported effect and the recording trace — NOT a claim that a real external effect occurred (see P4). It is the dissociation itself that this case demonstrates |
| in the published X5 experiment, zero ledger records imply the synthetic executor reported zero effects | **CONTRADICTED** | CONTRADICTED — within the experiment, and only there. The published results report effects=1 with records=0, so a zero record count does NOT imply a zero reported-effect count: the two are dissociated (1 vs 0). This refutes the naive inference 'empty ledger therefore nothing happened' AT THE LEVEL OF THE EXPERIMENT'S REPORTED BEHAVIOUR. It deliberately does not reach the world: whether a real effect occurred remains CANNOT ESTABLISH (P4), and whether the trail can show non-occurrence is CANNOT ESTABLISH (P6). Mirror of the GDPR case, correctly scoped: no record is not, by itself, non-occurrence. |

## 2 — The system's evidence trail (the ledger)

| Proposition | State | Basis |
|---|---|---|
| the X5 effect is recorded in the system's evidence trail | **CONTRADICTED** | CONTRADICTED — relative to the admitted surface. The published X5 probe reports zero ledger records, consistent with the reference implementation's simulated recording failure (BrokenSink raises OSError 'simulated write failure (disk full)'). FactNotebook did not re-run the probe or inspect a durable ledger itself; it reads the probe's reported record count (0). The trail, as reported, does not record the effect. This contradicts the RECORDING proposition only; it says nothing on its own about whether the effect occurred (P4) or did not (P6). |

## Limitations

- **P1-authorization** — *the authorization of the executed X5 action is established by the system's evidence trail* → **CANNOT ESTABLISH** (ledger carries no proof — gate ALLOW observed in the artifacts but not persisted; absence in the ledger, not in the artifacts). CANNOT ESTABLISH. The probe configures a granted capability and the gate evaluates ALLOW — an attributable observation in the published artifacts — but that decision is not carried by the evidence trail: the record write fails and the ledger has 0 entries. This is absence of proof IN THE LEDGER, not absence of any observation in the artifacts. The trail does not carry the authorization of the action that executed
- **P2-execution** — *the execution of the X5 action is established by the system's evidence trail* → **CANNOT ESTABLISH** (ledger carries no proof — only the synthetic self-count (not independent/durable); absence does not contradict execution either). CANNOT ESTABLISH. The only positive signal that execution occurred is the synthetic executor's own counter (effects=1) — an attributable observation in the artifacts, but not independent, not durable, and not evidence of a real external effect. The trail carries 0 entries. Symmetric caution: the empty trail does not CONTRADICT execution either (the artifacts report it ran). The trail simply cannot carry it
- **P4-real-effect** — *a real-world external effect occurred in X5* → **CANNOT ESTABLISH** (world-level, all observations — synthetic counter (not independent) AND empty trail; neither establishes a real external effect). CANNOT ESTABLISH. This is a WORLD-level proposition, evaluated against ALL admitted observations — not only the trail. Both candidates fail: the synthetic counter (effects=1) is explicitly not independent evidence of a real-world effect (the experiment states this itself), and the trail is empty. The reported effect (PA) is a fact about the experiment's instrumentation, not about the world; the empty ledger adds nothing. No admitted observation establishes a real external effect
- **P6-nonoccurrence** — *the system's evidence trail establishes that no real external effect occurred in X5* → **CANNOT ESTABLISH** (trail empty by a recording failure, not non-occurrence — the ledger settles neither execution nor non-execution). CANNOT ESTABLISH. The ledger is empty, but in X5 that emptiness is explained by a recording failure, not by non-occurrence. From the trail alone, non-occurrence cannot be derived — the ledger can establish neither execution nor non-execution. This is the honest world-level counterpart to P5: P5 refutes the inference within the experiment's reported behaviour; P6 records that the trail, by itself, cannot settle the world either way

## Separation of authority

*Observation instruments determine what they observe and propose. Admission (where the instrument's contract requires it) determines what may enter the reconstruction record. FactNotebook determines what that admitted record permits us to establish about the proposition. An instrument may search, select, transform or directly acquire observations according to its own declared procedure; those operations remain attributable properties of the instrument, not hidden properties of the reconstruction engine.*

- recorded behaviour → **observation** (attributed to its instrument)
- declared risk / rule classifications → **the evaluator's / authority's policy** (never engine facts)
- the consequential judgment → **the accountable authority**, outside this reconstruction

## Re-derivability

Two levels are preserved. **The finding** re-derives: re-running the reconstruction against the admitted observations reproduces the reconstruction identifier `FN-9e087ff81fe3759f` and the states above — no re-run of the probabilistic extraction is needed. The admitted set equals the full candidate set in this reconstruction; no detailed per-candidate admission register was produced. The acquisition boundary is documented in Annex C; a separately reviewed admission pass would produce a traceable register. *Version the instrument · trace the extraction · freeze the admitted record · replay the reconstruction.*

---

*FactNotebook reconstructs what can be established from the surviving records — including what cannot be — and keeps the establishment separate from the judgment applied to it.*

## References

*Each observation points to a citable source a third party can re-walk; the status records how it was verified.*

- **Pre-registration (EXECUTION_BOUNDARY_PREREG.md)** — XB-1 REGISTERED 2026-10-02; X5 = executor succeeds, sink fails on write -> effect with no record, exception propagates; code commits 386716a / 794a86b (workflow.py), ancestor 9308ce3; registrant 'Claude (Opus 5.5)', requester Chad Holland, external observer Davorin Popovic · _PRIMARY — public, re-walkable; X5 registered as effects 1 / records 0 / errors 1_ · https://github.com/holland202/sovereign-veritas/blob/fd5cac90587ba65d713b652ac743a8f240860aaa/docs/EXECUTION_BOUNDARY_PREREG.md
- **Results (EXECUTION_BOUNDARY_RESULTS.md)** — X5: 'effects 1 records 0 errors 1 (registered 1/0/1) first error: OSError: simulated write failure (disk full)'. Author gloss: 'The world changed and the evidence chain does not know.' Fix status after PR #8: X5 OPEN — needs a durable intent before the effect, plus a way to learn what happened · _PRIMARY — public; the X5 run reproduced the registered prediction (8 of 8 as registered)_ · https://github.com/holland202/sovereign-veritas/blob/fd5cac90587ba65d713b652ac743a8f240860aaa/docs/EXECUTION_BOUNDARY_RESULTS.md
- **Probe (tools/execution_boundary_probe.py)** — CountingExecutor.execute increments self.effects under a lock (synthetic, not a real action); BrokenSink.record raises OSError('simulated write failure (disk full)') unconditionally; records_in returns 0 for that sink; EvidenceWorkflow.run() evaluates the gate and executes in one call. No hashing: input_digest is the literal 'abc' · _PRIMARY — public; the synthetic executor and the broken sink are visible in code_ · https://github.com/holland202/sovereign-veritas/blob/fd5cac90587ba65d713b652ac743a8f240860aaa/tools/execution_boundary_probe.py
- **Integrity of the surface** — The experiment provides no dedicated cryptographic evidence manifest binding its reported result to the reference implementation — no SHA-256 or hash chain over its evidence (input_digest is the literal 'abc'). The public source files ARE pinned to a Git commit (content-addressed), so re-walkability rests on a fixed version, not the moving blob/main branch. VERIFICATION TRACE — at commit fd5cac90587ba65d713b652ac743a8f240860aaa (HEAD of main, 2026-10-12) these three files were re-read and the values used here compared element-by-element: docs/EXECUTION_BOUNDARY_RESULTS.md (X5 line effects 1 / records 0 / errors 1, OSError 'simulated write failure (disk full)'); docs/EXECUTION_BOUNDARY_PREREG.md (X5 registered 1/0/1, gloss 'effect with no record; exception propagates', code commits 386716a / 794a86b, ancestor 9308ce3); tools/execution_boundary_probe.py (BrokenSink.record raising the OSError, CountingExecutor incrementing under a lock, input_digest 'abc'). The probe was NOT independently re-executed · _DECLARED — no dedicated cryptographic evidence manifest; public source pinned to a Git commit_ · pinned at github.com/holland202/sovereign-veritas @ fd5cac90587ba65d713b652ac743a8f240860aaa
- **Observation register (obs -> provenance -> integrity -> probative role)** — Seven observations, one per proposition. EXPERIMENT surface: PA <- reported effect despite failed write (A2) -> establishes the dissociation; P5 <- reported effect with zero records (A2) -> contradicts 'zero records imply zero reported effects'. TRAIL surface: P3 <- probe reports 0 records + write failure (A2) -> contradicts 'recorded'; P1 <- gate ALLOW observed but not persisted (A2); P2 <- synthetic self-count only (A1); P6 <- trail empty by a recording failure, not non-occurrence (A2). WORLD (evaluated against ALL admitted observations): P4 <- weighs the synthetic counter (non-independent, A1) AND the empty trail; neither establishes a real effect. The EXPERIMENT propositions (PA, P5) concern the reported behaviour of the synthetic harness; the TRAIL propositions (P1, P2, P3, P6) ask what the ledger lets one establish; the WORLD proposition (P4) asks what any admitted observation establishes about the real world — never conflating the synthetic counter with independent evidence of a real effect · _ADMISSION — seven readings of one public, synthetic experiment driving seven propositions; no interpretive candidate, admitted without a separate interpretive admission step; all signals graded_ · per-proposition detail in the sections / limitations above
- **Frozen reconstruction manifest (the inputs a replay fixes)** — reconstruction_id FN-9e087ff81fe3759f · observation_model FN-CHAD-XB1-X5-001 hash sha256:77af5d3ab5c4ae038d59eaa1fe42b230be23ab986138d41f8eb457bbd0437d2b · observation_set hash sha256:3ad11c3c4c9bab013eecba542c82509cde31a1027a113c461132b27ca678b9a8 (7 observations: o_1d03a9de7790fd8a, o_31a6dc7cb866b8b3, o_5aa6bdf523fb412a, o_623d98c3dbd4ed74, o_9961449166c57323, o_ad14d0afb7475422, o_ffcf4f3b3740ab87) · rule versions fn-reconstruction-engine-v1 / fn-rule-pattern-v1 / fn-composition-v1 / fn-temporal-v1 / fn-canon-v1. Internal determinism: re-running against these frozen readings reproduces the identifier and the seven proposition outcomes; the engine is not public, so independent verification is at the OBSERVATION level — the three public artifacts can be re-read at the referenced commits (no cryptographic manifest is claimed) · _FROZEN — mirrors Annex D binding_ · Annex D (binding)

## Annexes

### A. Admitted observation set

*(register not supplied — admitted set is the record set named above)*

### B. Non-admitted candidate register

*Every candidate was admitted: none rejected, none left unresolved.*

### C. Acquisition / selection boundary

Records were constituted and supplied by Chad Holland — Principia Artificialis / Sovereign Veritas (public repo holland202/sovereign-veritas). The XB-1 case X5 artifacts are the subject's own pre-registration, results and probe, published on GitHub; FactNotebook reads them as published. They are NOT a source independent of the subject, and admitted without selective exclusion of candidate observations — all extracted candidates were admitted. This finding is bounded to that submitted surface; the absence of internal selection does not establish the submission's completeness relative to the represented system, nor whether an adverse class of observations was withheld — that completeness is **not established**.

*Chain of custody of how the observation surface became a reconstruction — each actor plays a distinct role:*

| Role | Actor |
|---|---|
| Surface constituted / submitted by | Chad Holland — Principia Artificialis / Sovereign Veritas (public repo holland202/sovereign-veritas). The XB-1 case X5 artifacts are the subject's own pre-registration, results and probe, published on GitHub; FactNotebook reads them as published. They are NOT a source independent of the subject |
| Submission form | three public artifacts (pre-registration, results, probe) for one pre-registered case (X5), plus the probe's own result transcript |
| Candidate extraction instrument | FactNotebook reads the public files and the probe's reported result line; it does NOT re-run the probe and does not rely on any internal mechanism of either project |
| Admission authority / mechanism | FactNotebook (proposer). The primary surface is the system's evidence trail (the ledger). The probe's harness counters (effects) and the raised OSError are the experiment's own synthetic instrumentation, admitted as DECLARED non-independent signals — never as the system's evidence chain, never as evidence of a real effect. Integrity is 'as published' (no cryptographic binding). Not an independent audit |
| Reconstruction engine | camsva 0.9.0 |

| Property | Value |
|---|---|
| Surface type | submitted |
| Acquisition mode | submitted bundle — no candidate selection |
| Period | experiment XB-1 registered 2026-10-02; code commits 386716a / 794a86b |
| Known limitations | One pre-registered case (X5) of a synthetic experiment. The executor is a counting stub — its observations are NOT independent evidence of a real-world external effect (the experiment states this). The experiment provides no dedicated cryptographic evidence manifest (input_digest 'abc'); the public source files are pinned to a Git commit, and the probe was not independently re-executed. The reconstruction distinguishes the published experiment's reported behaviour, the system's evidence trail, and what the admitted observations can establish about a real-world external effect; it does not judge whether Sovereign Veritas' controls are adequate. No legal or safety conclusion is drawn. |

### D. Policy & engine binding

- **Engine** camsva 0.9.0
- **Reconstruction ID** `FN-9e087ff81fe3759f`
- **Binding** `{'observation_model': {'id': 'FN-CHAD-XB1-X5-001', 'version': None, 'hash': 'sha256:77af5d3ab5c4ae038d59eaa1fe42b230be23ab986138d41f8eb457bbd0437d2b'}, 'policy': None, 'engine': {'engine_version': 'fn-reconstruction-engine-v1', 'rule_language_version': 'fn-rule-pattern-v1', 'composition_version': 'fn-composition-v1', 'temporal_policy_version': 'fn-temporal-v1', 'canonicalization_version': 'fn-canon-v1'}, 'observation_set': {'hash': 'sha256:3ad11c3c4c9bab013eecba542c82509cde31a1027a113c461132b27ca678b9a8', 'selected_count': 7, 'excluded_by_window': 0, 'window': None, 'custody_verified': False, 'closed_at': '2026-10-15T19:13:15+00:00', 'selected_ids': ['o_1d03a9de7790fd8a', 'o_31a6dc7cb866b8b3', 'o_5aa6bdf523fb412a', 'o_623d98c3dbd4ed74', 'o_9961449166c57323', 'o_ad14d0afb7475422', 'o_ffcf4f3b3740ab87'], 'excluded_ids': [], 'selection_note': 'bounded observation SELECTION by t_event; not temporal inference over the interval'}}`
