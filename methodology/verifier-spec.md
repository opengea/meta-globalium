# Structural verifier — specification

> **Provenance**: this content is part of the **Meta-Globàlium proper** — the new structural layer (Berenguer / Opengea, 2023–2026) added on top of the inherited Globàlium ontology. It is the original contribution of this work.


This document specifies the **structural verifier** — the runtime check that determines whether an answer A respects the dimensions activated by a question Q, given the Meta-Globàlium ontology.

For the conceptual basis, see [`be-criterion.md`](be-criterion.md).

## Inputs

| Input | Type | Description |
|-------|------|-------------|
| `question` | string | Natural-language query |
| `answer` | string | Candidate response to verify |
| `ontology` | object | Meta-Globàlium structure (loaded from [`../ontology/data/categories.json`](../ontology/data/categories.json)) |
| `language` | enum | `ca`, `en`, … (label/description language) |

## Outputs

```json
{
  "good": true,
  "score": 0.85,
  "axes_activated": ["D1", "D2"],
  "axes_covered": ["D1", "D2"],
  "axes_missing": [],
  "axes_collapsed": [],
  "categories_touched": ["AMO", "ANA", "SIN", "EXP"],
  "coherence_issues": [],
  "explanation_human": "The response covers both axes activated by the question; it holds tension on D1 (subject/object) without collapsing to either pole; categories AMO and SIN are properly engaged."
}
```

## Algorithm (reference)

```python
def verify(question, answer, ontology, language='en'):
    # Phase 1: ANA — identify axes activated by the question
    embeddings = embed(question, ontology.categories)
    axes_activated = identify_axes(question, embeddings)
    
    # Phase 2: SIN — check structural coverage
    axes_covered = []
    axes_missing = []
    for axis in axes_activated:
        if axis_present_in(answer, axis, ontology):
            axes_covered.append(axis)
        else:
            axes_missing.append(axis)
    
    # Phase 3: collapse detection
    axes_collapsed = []
    for axis in axes_covered:
        polarity = polarity_balance(answer, axis, ontology)
        if abs(polarity) > COLLAPSE_THRESHOLD:
            axes_collapsed.append({'axis': axis, 'collapsed_to_pole': sign(polarity)})
    
    # Phase 4: internal coherence
    coherence_issues = detect_internal_contradictions(answer, axes_activated, ontology)
    
    # Final score
    coverage_score = len(axes_covered) / max(1, len(axes_activated))
    collapse_penalty = len(axes_collapsed) * 0.25
    coherence_penalty = len(coherence_issues) * 0.15
    score = max(0, coverage_score - collapse_penalty - coherence_penalty)
    
    return {
        'good': score > 0.7 and not axes_missing and not axes_collapsed,
        'score': score,
        'axes_activated': axes_activated,
        'axes_covered': axes_covered,
        'axes_missing': axes_missing,
        'axes_collapsed': axes_collapsed,
        'categories_touched': identify_categories(answer, ontology),
        'coherence_issues': coherence_issues,
        'explanation_human': generate_explanation(...),
    }
```

## Implementation backends

The reference Arkadium implementation uses an LLM (Claude 4 / GPT-4 / Llama-3) with the Meta-Globàlium as system prompt + tool-calls for structural checks. Other backends are possible:

- **Pure embedding-based** — fast but less accurate on structural checks
- **Small classifier model** fine-tuned on Meta-Globàlium axes — faster than full LLM, more accurate than embeddings
- **Hybrid** — embedding for retrieval, small model for axes identification, LLM for the final coherence check

## Calibration

The verifier requires calibration:

- `COLLAPSE_THRESHOLD` (default 0.7) — how much polarity imbalance counts as a collapse
- Score thresholds (default `good = score > 0.7`) — adjustable per use case
- Confidence intervals — for low-confidence cases, return `good = "uncertain"` rather than binary

A reference test suite is in preparation; see issue tracker.

## What the verifier does NOT do

- It does not check **factual correctness** — that is a separate layer
- It does not check **stylistic/pragmatic appropriateness** — that is a third layer
- It does not impose **specific axiological positions** — it only checks structural integrity

These three layers are complementary; the verifier is one of three. See [`be-criterion.md`](be-criterion.md) for the full layered architecture.

## See also

- [`be-criterion.md`](be-criterion.md) — conceptual basis
- [`metode-global.md`](metode-global.md) — the full ANA→SIN→AMO→EXP cycle the verifier supports
- [`../examples/coverage-evaluation.md`](../examples/coverage-evaluation.md) — worked examples
- [`../examples/system-prompt-template.md`](../examples/system-prompt-template.md) — reference system prompt
