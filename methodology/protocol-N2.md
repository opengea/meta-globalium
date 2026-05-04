---
title: Protocol N2 — Frame creation and revision checklist
date: 2026-05-03
status: binding — extension of Protocol N2 with learnings from the Mathematics frame
applies_to: all N2 frames (thematized expressions of the Meta-Globàlium)
license: CC BY-SA 4.0
---

# Protocol N2 — Frame creation and revision checklist

> **Provenance**: this content is part of the **Meta-Globàlium proper** — the new structural layer (Berenguer / Opengea, 2023–2026) added on top of the inherited Globàlium ontology.

> **Consolidated learning from the Mathematics frame (consolidation 2026-05-03)**

This document extends the base Protocol N2 with **20 operational rules + 2 governing principles**. It is **binding**: apply to any new frame before considering it complete, and to any existing frame before any substantial modification.

---

## ⭐ Two governing principles (absolute priority)

### Principle 1 — Holistic understanding over exhaustiveness

> **The point is NOT to understand every possible variant, but to understand the concept of the frame as a whole, its major areas, and how they connect.**

Practical implications:

- The frame must function first as a **connected map of major areas**, not as an exhaustive taxonomy.
- If the sum of the 80 cells reads well but the 6 cardinals do not form a coherent vision of the domain → the frame is miscalibrated.
- If a PLA/MON cell is left empty or conceptual because there is no natural discipline → it is better to leave it as an explicit *concept* than to fill it artificially to complete the cube.
- Pedagogy starts from the 6-8 foundational points; the 80-cell detail is for the specialist.
- Never sacrifice **structural readability** to fill all the cube's holes.

**Validation consequence**: if a domain specialist, looking at the 6 cardinals + 12 disciplinary bridges (zoom 26), does not understand the cartography of their own discipline, the frame has failed — even if all 80 cells are perfectly filled.

### Principle 2 — Coherence of opposite dialectics

> **What matters most is that the dialectics of opposites remain coherent in the model.**

The dialectics **are** the load-bearing architecture of the cube. If they fail, the cube becomes a flat taxonomy without structural value. Verify exhaustively:

| Type | Count | Dialectics |
|------|-------|------------|
| Cardinal | 3 | TEO ↔ PRA · OBJ ↔ SUB · NOU ↔ FEN |
| Face-vertex | 2 | MTP ↔ CIE · MTF ↔ ART |
| Disciplinary | 4 | LOG ↔ MIS · TEC ↔ MIT · EST ↔ ETI · PSI ↔ IDE |
| Mediator | 4 | ANA ↔ SIN · AMO ↔ EXP · STM ↔ SGE · SGT ↔ STT |
| **Total** | **13** | |

Each pair of opposites must **be verbalisable as a productive tension** in the specific domain (e.g.: "Geometry ↔ Probability" = deterministic ↔ random). If the tension cannot be articulated, **the dialectic is broken** and the frame requires reformulation at that cell.

**No pole can be filled without verifying its dialectical counterpart.** If a cell is perfect but its dialectical opposite is forced, the architecture has broken: **prefer to empty the perfect cell rather than maintain an incoherent dialectic**.

---

## A. Ontological principles

1. **Mandatory double anchoring** (base Protocol N2). No cell without Card A (Xirinacs 1997 source) + Card B (Meta-Globàlium parent=28 structural mapping). If A and B do not converge → stop and resolve the canonical tension before mapping.

2. **Explicit ontological caveat at the MON-anchor**. A projection of a domain onto the cube *is not* the natural classification of that domain (it is not MSC2020, not Bloom's taxonomy, not Linnaean). Document this so specialists read it as a *philosophical lens*, not a normative taxonomy.

3. **Accept transversality** as a real property of knowledge, not a defect of the frame. List at the MON-anchor the disciplines/concepts that live as *intersections* of multiple cells.

## B. Structural rules

4. **Cardinals = foundational pillars of the domain**, not philosophical labels without correlate. Choose real umbrella disciplines that a specialist would recognise as a "pillar". Never use secondary concepts or canonical Xirinacs labels ("Globality" instead of a discipline).

5. **Do not use NEU operation names for PLA/MON poles**. PLA poles are *plasmatic potentialities* (pre-formal matter); MON poles are *unfolded manifestations*. If you see "Distinction" at a PLA → structural error (Distinction is the NEU of OBJ).

6. **Family coherence within trios**. PLA → NEU → MON must belong to the same family of the domain. If NEU = abstract algebra and PLA = connectedness (topology) → tension that must be resolved. The trio's narrative must be plausible and unified.

7. **Real disciplines, not forced concepts**. "Variables", "Conjectures", "Special cases", "Critical points" are *concepts*, not disciplines. Replace with real discipline-fragments ("Parametric systems", "Morse theory", "Non-standard models") wherever possible.

8. **No imposed mythological narrative**. Xirinacs labels (Tiamat, Magma, Inebriation, Akasha) carry mythological resonance. Do NOT use it as *reasoning* in the domain `description`. Justify only by Card B (canonical operation) + pure domain discipline. Keep mythology as *historical anchoring*, not as active explanation.

## C. Load-bearing dialectics (see Principle 2)

9. **Verify the 13 dialectics** before closing the frame. Mark weak ones explicitly; strong ones are what validate the frame.

10. **PLA-NEU-MON narrative trios**. Each trio must read as a coherent *potential → discipline → manifestation* story. If the story does not close, something is missing.

## D. Multi-scale pedagogy (see Principle 1)

11. **Three zooms with different purposes**:
    - **8 points** (cardinals + 2 anchors): basic pedagogy, dissemination, *"what is this domain?"*
    - **26 points** (full NEU): structure, bridges between cardinals, dialectics, *"how do the major areas connect?"*
    - **80 points** (PLA + NEU + MON): specialised ontological reflection, *"how is each trio articulated?"*

    The frame must work well at each of the 3 levels, not only one.

12. **Disciplinaries as bridges**, not as a list. Each disciplinary connects 2 cardinals (in the cube's geometry) and must be verbalisable as *bridge between X and Y*. Document this explicitly at the MON-anchor.

13. **Mediators as methodic operators**. The 8 mediators articulate 3 cycles (Method ANA→SIN→AMO→EXP, Orientation, Knowledge) — not a "flat taxonomy", but *how one operates within the domain*.

## E. Operational process

14. **Backup before massive changes**. Always `CREATE TABLE backup_X AS SELECT *`. Multiple backups for intermediate states is not wrong — they are cheap.

15. **Card A + Card B + A↔B coherence + Affines** in each `description`. Format from Phase 6 of Protocol N2. Traceability is part of metadata, not optional.

16. **Verify absence of duplicates** after each batch UPDATE. Query: `SELECT name, COUNT(*) c FROM … GROUP BY name HAVING c > 1`.

17. **Validate 0 `xxxx` cells** at the end. If any remain, mark them explicitly pending at the MON-anchor.

18. **If a proposal is not defensible to a domain specialist, reject it**. LLM intuition is not enough. A mathematician / physicist / humanist must accept the mapping without flinching.

## F. Documentation at the MON-anchor

19. **Complete frame-card** at the MON-anchor with:
    - Explicit cardinalization (the 6 + ontological caveat)
    - 12 bridges between cardinals (table)
    - 4 disciplinary dialectics (table)
    - 4-5 canonical pedagogical narratives
    - Transversal (cross-cutting) disciplines listed (non-localizable)
    - Review status + available backups

## G. Hierarchical metadata

20. **`rang` field for abstraction levels**. Allows filtering the visualization by audience and switching between multiple "views" of the same domain (pedagogical vs research). Schema: `kms_kb_metacategories.rang VARCHAR(50)`.

---

## Final checklist before closing a frame

```
[ ] Principle 1: the frame reads well as a connected map of major areas
[ ] Principle 2: the 13 opposite dialectics are coherent
[ ] 0 'xxxx' cells; all names are real disciplines or sub-disciplines
[ ] 0 internal duplicates
[ ] Cardinals = foundational pillars recognized by the domain
[ ] PLA poles are potentialities (not NEU operations)
[ ] Coherent families within each trio (P→N→M from the same family)
[ ] 13 dialectics verified; weak ones marked explicitly
[ ] No imposed mythological narrative in descriptions
[ ] MON-anchor with caveat + zooms + bridges + dialectics + transversals
[ ] `rang` field populated for multi-scale filtering (if applicable)
[ ] Backups created before massive changes
[ ] Card A + Card B + coherence in each description (Phase 6)
[ ] External validation with domain specialist (recommended)
```

---

## Immediate application

To any new frame (e.g. *Human community*, future *Subject*, future *Health*, etc.) or re-validation of existing frames, apply this checklist in sequence.

If canonical tensions are found between Card A and Card B during the anchoring phase, document them in an *annex of canonical tensions* within the repository — do not force the mapping.

---

## History

- **2026-05-03**: protocol created from learnings of the Mathematics frame. Includes:
  - Pass 1 + Pass 2 + Pass 3 (structural corrections and cell-filling)
  - Option C (cardinals as natural branches)
  - 5 Improvements (family coherence, dialectic, concept→discipline, rang, narrative)
  - 3 additional trio coherence fixes (POL, DET, CAV)

## See also

- [`metode-global.md`](metode-global.md) — the Method cycle that frames operationalize
- [`be-criterion.md`](be-criterion.md) — the structural verifier criterion
- [`../ontology/principles-and-operations.md`](../ontology/principles-and-operations.md) — the 13 dialectics in canonical form
- [`../ontology/fractal-N1-N2.md`](../ontology/fractal-N1-N2.md) — the N1 vs N2 distinction
