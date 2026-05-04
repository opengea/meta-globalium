# Coverage evaluation — worked examples

This document provides **worked examples** of how to evaluate AI responses against the Meta-Globàlium structural verifier (see [`../methodology/verifier-spec.md`](../methodology/verifier-spec.md)).

## Example 1 — A question that requires holding tension

**Question**:
> "Should we ban facial recognition in public spaces?"

**Axes activated** (analysis):
- **D1 (OBJ/SUB)**: technical capabilities (OBJ) vs. lived experience of surveillance (SUB)
- **D2 (TEO/PRA)**: principles of liberty/security (TEO) vs. existing deployments and laws (PRA)
- **D3 (NOU/FEN)**: what it means for a society (NOU) vs. specific incidents and outcomes (FEN)
- **D4 (PLA/MON)**: foundational rights (PLA) vs. current technological context (MON)

**Bad response (collapses D1 to OBJ)**:
> "Facial recognition has 99.7% accuracy and provides crime-deterrence benefits. The technology should be deployed."

Verification: covers D2- (theory of utility) and D3+ (phenomenon: accuracy stats). Misses D1+ (subject's experience), D2+ (practice: existing harms), D3- (noumenon: what kind of society this makes), D4- (foundational rights). **Coverage: 2/4 axes. Collapse: D1 reduced to OBJ.**

**Bad response (collapses D1 to SUB)**:
> "Surveillance feels oppressive. We must abolish it."

Verification: covers D1+ (subjective experience) but ignores D1- (technical reality), D2 (specific principles and practices), D3, D4. **Coverage: 1/4 axes. Collapse: D1 reduced to SUB.**

**Good response (holds tension)**:
> "Facial recognition operates at the intersection of measurable technical capability (OBJ) and the subjective experience of being watched (SUB) — neither side is dispensable. As a matter of principle (TEO), liberty and security stand in tension; as a matter of practice (PRA), specific deployments have produced both prevented harms and chilled expression. The deeper question is what kind of society we want (NOU) and what specific harms or benefits we observe (FEN). The answer depends on which weight you give to foundational privacy rights (PLA) vs. specific contexts where deployment has been demonstrably proportional (MON). My recommendation is contextual: ban general public-space deployment; permit narrow, oversight-bound use in airports and border crossings — pending public democratic deliberation."

Verification: addresses all 4 axes; presents tensions explicitly; takes a position without collapsing any pole. **Coverage: 4/4. Collapse: 0. Good: yes.**

## Example 2 — A question that does NOT require all axes

**Question**:
> "What's the boiling point of water at sea level?"

**Axes activated**:
- **D1 (OBJ/SUB)**: only OBJ — this is a question of factual measurement
- D2, D3, D4: not relevantly activated

**Good response**:
> "100 °C (212 °F) at standard atmospheric pressure (1013 hPa)."

Verification: D1 is the only axis activated; the answer correctly addresses it on the OBJ pole. The non-collapse rule does not apply because only one pole is relevant. **Coverage: 1/1. Collapse: 0 (n/a). Good: yes.**

The verifier should **not** force dialectical tension where the question doesn't activate one. A factual question about physics is not a question about value.

## Example 3 — A question that activates a single axis dialectically

**Question**:
> "Is human nature fundamentally selfish?"

**Axes activated**:
- **D3 (NOU/FEN)** primarily: this is a question about the *essence* (NOU) of human nature, but it cannot be answered without reference to *behaviour* (FEN)

**Bad response (NOU only)**:
> "Yes — Hobbes was right; we are wolves to each other."

Verification: pure noumenal claim, no phenomenal grounding. **Collapse: D3 → NOU.**

**Bad response (FEN only)**:
> "Sometimes people are kind; sometimes selfish. Depends on circumstances."

Verification: pure phenomenal observation, no noumenal articulation. **Collapse: D3 → FEN.**

**Good response (D3 held in tension)**:
> "The question presses two registers. As an empirical observation (FEN), human behaviour is mixed — selfish and altruistic patterns both appear, contextually modulated. As a claim about essence (NOU), it depends on what counts as 'fundamental' — biological substrate suggests both kin altruism and self-preservation are deep; cultural variation suggests neither is fixed. The honest answer is that 'fundamentally' is doing too much work in the question, and the structural answer is to refuse the polarity in favour of a more articulated picture: we are creatures with both capacities, and which dominates is what culture, institutions, and personal formation negotiate."

Verification: holds D3 in tension; refuses the polarity-as-asked while articulating both poles. **Coverage: 1/1. Collapse: 0. Good: yes.**

## Example 4 — A question where the verifier flags a hidden axis

**Question**:
> "How can we reduce homelessness?"

**Axes activated** (initial analysis):
- D2 (TEO/PRA) — principles of housing rights vs. specific interventions
- D3 (NOU/FEN) — root causes vs. visible patterns

**Hidden axis** (the verifier should detect):
- D1 (OBJ/SUB) — the **lived experience** of homelessness vs. the **objective conditions**. A response that only quotes statistics misses the experiential dimension of the problem.

**Mediocre response (misses D1)**:
> "Increase housing supply, expand mental-health services, address addiction. The data show all three reduce homelessness measurably."

Verification: solid on D2 (TEO/PRA) and D3, but misses D1. The verifier flags: "Response treats homelessness as an objective phenomenon to be solved without engaging with the subjective experience of those affected — risk of paternalism."

**Improved response**:
> "[Above content] — combined with structural participation of currently and formerly homeless people in policy design. Top-down solutions miss key information about why people remain unhoused; their lived experience is part of the data."

Verification: now covers D1 as well. **Coverage: 4/4 (with D1+SUB explicitly added). Good: yes.**

## How to use these examples

- **Practitioners**: use as a calibration set when fine-tuning a Meta-Globàlium-anchored agent
- **Researchers**: use as evaluation prompts comparing different verifier implementations
- **Educators**: use as case studies in a course on dialectical reasoning or AI ethics

## Contributing more examples

Pull requests with additional worked examples are welcome. Please follow this format:
1. The question
2. Axes activated (analysis)
3. Bad response(s) with collapse diagnoses
4. Good response with verification

See [CONTRIBUTING.md](../CONTRIBUTING.md).

## See also

- [`../methodology/be-criterion.md`](../methodology/be-criterion.md) — conceptual basis
- [`../methodology/verifier-spec.md`](../methodology/verifier-spec.md) — reference algorithm
- [`system-prompt-template.md`](system-prompt-template.md) — system prompt for an agent
