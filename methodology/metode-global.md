# The Global Method

> ANA → SIN → AMO → EXP

The Global Method is the **process** of structured reasoning the Meta-Globàlium proposes. It is not a list of steps to follow rigidly; it is a cycle that any thorough deliberation passes through, often iteratively. The method is what gives the model its operational dimension — without a method, the geometry would be static.

The four phases sit at four corners of the Cartesian skeleton (see [`../ontology/4-axes.md`](../ontology/4-axes.md) and [`../ontology/8-root-categories.md`](../ontology/8-root-categories.md)).

## The eight-point trajectory

The four phases lie on a circular trajectory across the Meta-Globàlium hypersphere. **Between each pair of phases, the trajectory passes through an axial mediator** — a cardinal pole that joins them:

```
ANA  →  TEO  →  SIN  →  NOU  →  AMO  →  PRA  →  EXP  →  FEN  →  (ANA)
phase   axis    phase   axis    phase   axis    phase   axis
```

| # | Point | Kind | Role |
|---|-------|------|------|
| 1 | **ANA** | phase (corner OBJ+TEO+NOU) | Analysis: distinguish parts |
| 2 | **TEO** | axial mediator (D2-) | Theoretical bridge from analysis to synthesis |
| 3 | **SIN** | phase (corner OBJ+TEO+FEN) | Synthesis: relate parts |
| 4 | **NOU** | axial mediator (D3-) | Noumenal bridge from synthesis to commitment |
| 5 | **AMO** | phase (corner SUB+PRA+NOU) | Love: plan of action |
| 6 | **PRA** | axial mediator (D2+) | Practical bridge from plan to execution |
| 7 | **EXP** | phase (corner SUB+PRA+FEN) | Experience: implementation |
| 8 | **FEN** | axial mediator (D3+) | Phenomenal bridge from experience back to analysis |

The four phases (ANA, SIN, AMO, EXP) are root categories — corners of the Cartesian skeleton. The four mediators (TEO, NOU, PRA, FEN) are cardinal axis-poles the trajectory passes through. The Globalística book calls this the **Volta d'Aplicació** (Application Loop) — one of three basic *voltes* in the Meta-Globàlium.

## The four phases

### 1. ANA — *Analysis* (determination of parts)

In ANA, we break the question into its parts. We list what is at stake, what categories are touched, what dimensions are involved. We resist the temptation to answer too soon. The discipline of ANA is **distinguishing without yet relating**.

In an AI system: ANA is the retrieval phase. Vector search over the 80 categories. Identification of the relevant axes. The answer is not yet attempted — only the field is mapped.

→ Trajectory then passes through **TEO** (theoretical bridge) toward SIN.

### 2. SIN — *Synthesis* (determination of relations)

In SIN, we relate the parts identified in ANA. We ask: what are the dialectical tensions here? What axis (or axes) is the question really about? Which poles are in play, and which are at risk of being collapsed?

In an AI system: SIN is the structural validation phase. Coherence checking against the global geometry. Identification of dimensional collapse risks (blind spots).

→ Trajectory then passes through **NOU** (noumenal bridge) toward AMO.

### 3. AMO — *Love* (plan of action)

In AMO, we choose. The analysis and synthesis don't determine the answer — they prepare the ground for a decision that must be made by a *subject*. AMO is the moment of care: what is the plan that respects the dimensions identified, that does not collapse what should not be collapsed, that takes responsibility?

The choice of *Love* (rather than "decision" or "judgment") is intentional. AMO names the moment when the structural rigor of the prior phases gives way to **commitment** — the plan is not only correct, it is *cared for*. The verifier's coherence is necessary; the subject's care is what makes the plan livable.

In an AI system: AMO is the generation phase. The LLM produces an answer that is structurally validated and explicitly oriented (not value-neutral). The system prompt makes the orientation transparent and revisable.

→ Trajectory then passes through **PRA** (practical bridge) toward EXP.

### 4. EXP — *Experience* (implementation)

In EXP, the plan is enacted and the world responds. EXP is what closes the loop: the world's response feeds back into the next ANA. Without EXP, the method is sterile — pure deliberation without consequence.

In an AI system: EXP is the user-facing response and the feedback loop. The user reads the answer, interacts with it, gives feedback (explicit or implicit). The trace of the conversation enters the system's memory and shapes the next cycle.

→ Trajectory then passes through **FEN** (phenomenal bridge) back to ANA, closing the loop.

## The cycle is iterative

A complete deliberation passes through the four phases not once but many times, at multiple levels of resolution. A new question may begin with ANA, but a refined formulation often loops back to ANA from EXP — the world's response reveals new aspects to analyze.

The number of iterations is not fixed. The Globalística book proposes **6 maximal voltes** (turns) for full canonical deliberation, but most practical questions resolve in fewer.

## The Solve-Coagula meta-operation

Beyond the four phases, the cycle itself can be characterized by a meta-operation: **Solve-Coagula** (dissolve and re-form). Each cycle dissolves the current understanding (ANA breaks it apart) and re-forms it more articulately (SIN, AMO, EXP). The model itself, applied to itself, generates this iteration.

See [`solve-coagula.md`](solve-coagula.md) for the formal characterization.

## Mapping to other process frameworks

| Mètode Global | OODA loop (Boyd) | PDCA (Deming) | Hegelian dialectic | Buddhist 4 noble truths |
|---------------|------------------|---------------|---------------------|--------------------------|
| ANA | Observe | Plan | Thesis | Suffering (dukkha) |
| SIN | Orient | (Plan) | Antithesis | Cause |
| AMO | Decide | Do | (Synthesis-as-care) | Cessation (commitment) |
| EXP | Act | Check + Act | Synthesis | Path |

These mappings are not perfect — each framework has its own emphasis — but they show that the structure of the Mètode Global is not idiosyncratic. It is what any structured deliberation looks like, given a particular emphasis on **structural verification** (the SIN phase as a rigorous discipline, not an afterthought).

## Implementation in an Arkadium-style agent

A reference implementation outline:

```
on user_query:
    1. ANA:
       embed(query) -> retrieve top-k categories from ontology
       identify_axes_touched(query, retrieved_categories)
    2. SIN:
       structural_check: are all relevant axes represented?
       collapse_check: which dimensions are at risk of being ignored?
       if collapse_risk: flag and re-prompt
    3. AMO:
       generate_response(query, retrieved, axes, structural_constraints)
       attach_provenance(response, retrieved_categories)
    4. EXP:
       deliver_response_with_visible_coverage_map
       record_user_feedback for next iteration
```

The Arkadium product implements this; this repository specifies the model and methodology that any architecture can adopt.

## Sources

- Berenguer, J. (forthcoming). *Globalística — Estudi i aplicació de models globals de la realitat*. Mètode Global ANA→SIN→AMO→EXP, 6 voltes maximes.
- Xirinacs, L.M. (1997). *A global model of reality*. Foundational dialectical structure.
- Agustí-Cullell, J. & Schorlemmer, M. (2021). *A Humanist Perspective on Artificial Intelligence*. COMPRENDRE 23/1, IIIA-CSIC. External validation of the cycle through the three dimensions of intelligence (functional/axiological/liberating).
