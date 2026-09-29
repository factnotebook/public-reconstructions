# FN-JAFAR-BUNIA-001 — When the structured record and the primary record disagree

By **FactNotebook** — [factnotebook.com](https://factnotebook.com).
Readable case study: [factnotebook.com/audits/structured-vs-primary-record](https://factnotebook.com/audits/structured-vs-primary-record)

A bounded, **non-dispositive** reconstruction from an external AI safety evaluator's field-testing
records — how AI assistants respond to health-guidance prompts in a low-resource, outbreak context,
across languages. During verification, one structured representation diverged from the primary
record; the reconstruction was **rebound to the verified primary surface**, and one variant absent
from the received primary set was held **`CANNOT ESTABLISH`** rather than carried forward.

## What is published — and what is not

This entry publishes **method and outcome only**. The underlying records are **private and
consented**: they are held by the evaluator and are **not published** here — no screenshots, no
clinical content, no dosing values, no locations, and **no model-level claims** (the models are
anonymized). Unlike a case where redactions are directly inspectable, the record set for this
reconstruction is deliberately kept private at the evaluator's and FactNotebook's discretion, given
the sensitivity of the field material.

The three layers are kept separate: the recorded model behavior, the propositions tested against
those records, and the evaluator's evaluation / safety rule. Labels such as "residual risk" or
"pass" remain attributed to the **evaluator's policy** and are never converted into FactNotebook
findings.

## Public result (structural)

A small set of proposition-level states over a bounded set of confirmed records: `ESTABLISHED` where
the records supported the proposition, `CONTRADICTED` where a recorded counter-instance stood against
it, and `CANNOT ESTABLISH` where the available record did not permit the proposition to be
established (including the absent variant and a prevalence / generalization proposition with no basis
in a small, non-random set). The instructive outcomes were the discipline around them: a divergence
caught at verification before it could bias the finding, and an honest `CANNOT ESTABLISH` preserved
rather than rounded to a stronger claim.

---

Field audit and records: **Jafar Muhammed**, AI Safety Evaluator — Bunia field-testing, published
with permission. Reconstruction: FactNotebook. Retrospective and non-dispositive; the reconstruction
engine is not published, and the safety judgment remains with the evaluator.
