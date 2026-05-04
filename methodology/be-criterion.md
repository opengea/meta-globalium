# The Good as harmony — a structural verifier

> **Provenance**: this content is part of the **Meta-Globàlium proper** — the new structural layer (Berenguer / Opengea, 2023–2026) added on top of the inherited Globàlium ontology. It is the original contribution of this work.


> **The Good is the geometric property of not collapsing any dimension.**

Most attempts to give AI a "good" answer rely on **lists of rules** (constitutional AI, value lists, RLHF preferences). These are textual, axiological, and culturally non-neutral. They work only as far as the rules anticipate the situation; they fail in adversarial cases, edge cases, and cross-cultural ones.

The Meta-Globàlium proposes a different verifier. **The Good is not a list. The Good is a geometric property** — specifically, the property of not collapsing any of the dimensions that are structurally relevant to the question being asked.

## Formal statement

Given:
- A model with **n** dimensions (axes), each defined by a polarity (negative pole / positive pole)
- A question Q that activates a subset of dimensions D ⊂ {1...n}
- An answer A

Then **A is good** iff:

1. **Coverage**: A explicitly addresses every dimension in D
2. **Non-collapse**: A does not reduce a polarity to one of its poles, except where the question explicitly demands it
3. **Coherence**: A's positions across dimensions hold together (no internal contradiction)

The first two are *structural*. The third is *logical*.

## The criterion is internal, not external

Unlike axiological criteria ("be honest", "respect autonomy", "minimize harm"), this criterion is **internal to the question's own structure**. There is no list of values to apply from outside. The answer is good when it matches the dimensional shape of the question.

This makes the criterion:

- **Computable**: given a model with explicit axes and a method for identifying which axes a question touches, the verifier can be implemented as a structural check.
- **Culturally neutral**: it does not import a particular tradition's values. Different traditions weight the poles differently; the criterion only requires that no pole is structurally ignored.
- **Auditable**: the verifier's judgment can be made transparent — "this answer ignores axis X" or "this answer collapses Y to its negative pole".

## Example: the classical formulation

The classical question of *the good as the equilibrium between individual freedom and the freedom of others* is exactly the structural form:

- **Axis**: individual ↔ collective (a thematized expression of D1: subject ↔ object)
- **Collapse**: an answer that absolutizes individual freedom collapses the *collective* pole; an answer that dissolves individuals into the collective collapses the *individual* pole.
- **Good answer**: one that holds both poles in tension — recognizing freedom while also recognizing its bounded reach.

This is Aristotelian *mesotes*; this is Confucian *zhongyong*; this is Buddhist mādhyamika. The structural criterion is what those traditions independently arrived at.

## What the criterion does NOT replace

The structural verifier operates **above factual correctness**. An answer that is factually wrong is wrong even if it touches every dimension. The verifier is a layer of *structural integrity*, not a layer of *truth*.

| Layer | Question | Failure mode |
|-------|----------|--------------|
| **Factual correctness** | Is the content accurate? | Hallucination, false claim |
| **Structural verifier** | Does the answer respect the dimensions? | Dimensional collapse |
| **Stylistic/pragmatic** | Is it well-said for this audience? | Unintelligible, off-tone |

The Meta-Globàlium contributes specifically to the middle layer. It does not solve hallucination (factual checking is a separate problem). It addresses *the kind of error that current AI fails to even detect*: the structural reduction.

## Implementation outline

A reference verifier:

```python
def verify(question, answer, ontology):
    # 1. Identify axes touched by the question
    axes_in_q = identify_axes(question, ontology)

    # 2. For each axis, check coverage
    coverage = {a: covers(answer, a) for a in axes_in_q}

    # 3. For each axis covered, check non-collapse
    collapse = {a: collapses(answer, a) for a in axes_in_q if coverage[a]}

    # 4. Check internal coherence
    coherence = check_coherence(answer, axes_in_q)

    return {
        'good': all(coverage.values()) and not any(collapse.values()) and coherence,
        'missing_axes': [a for a, c in coverage.items() if not c],
        'collapsed_axes': [a for a, c in collapse.items() if c],
        'coherence_issues': coherence_details(answer),
    }
```

`identify_axes`, `covers`, `collapses`, `check_coherence` are concrete tasks for an LLM-with-tool-calls or for a separate small classifier. The reference Arkadium implementation uses an LLM with the Meta-Globàlium as system prompt.

## Why this is alignment without value-loading

A common worry about AI alignment: whose values? The structural verifier sidesteps this question. It does not require agreement on what is good; it requires only agreement on **what dimensions are structurally relevant** to a class of question.

This is not value-neutrality in a vacuous sense. The model embodies values: it values **completeness**, **non-reduction**, **dialectical integrity**. But these are *meta-values* — values about the *form* of any answer, not its content.

A culture that disagrees with the model's specific axes can propose its own. The structural form (axes-as-polarities, good-as-non-collapse) is more general than any specific instantiation. The Meta-Globàlium's 80 categories are one defensible instantiation, grounded in the European philosophical tradition; other traditions can propose their own. **The form survives the disagreement**.

## See also

- [`metode-global.md`](metode-global.md) — the process this verifier accompanies
- [`verifier-spec.md`](verifier-spec.md) — concrete API specification
- [`../ontology/4-axes.md`](../ontology/4-axes.md) — the four axes the verifier operates on
- [`protocol-N2.md`](protocol-N2.md) — protocol for thematizing the verifier to specific domains
