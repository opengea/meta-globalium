# Contributing to the Meta-Globàlium

Thank you for considering contributing to the Meta-Globàlium. This is an explicitly **revisable, open** model — its value depends on rigorous community contribution.

## Ways to contribute

### 1. Translations

The model claims universality but is currently grounded in Catalan + English. Translations of canonical labels and methodology documents are explicitly welcome:

- **Priority languages**: Spanish, French, German, Italian, Portuguese, Chinese, Arabic, Japanese, Hindi
- **What to translate**: README, manifest, key methodology documents (`metode-global.md`, `be-criterion.md`), category labels in `ontology/data/categories.json` (the `name_*` fields)
- **How**: open an issue with the `translation` template, fork, translate, submit PR

Translations should preserve the **dialectical structure** — not just word-by-word but the conceptual pairing.

### 2. New thematized frames (N2)

The Meta-Globàlium is **fractal**: the same universal axes (N1) project onto every domain as thematized expressions (N2). New frames apply the structure to specific fields: epistemology, emotions, pedagogy, governance, ecology, etc.

Frame proposals must follow the **N2 frame checklist** (see [`methodology/protocol-N2.md`](methodology/protocol-N2.md)):

- 2 guiding principles (holistic > exhaustive; coherent dialectics)
- 20 binding rules
- Double anchoring: source attribution (Card A) + Meta-Globàlium structural mapping (Card B)
- 6 review phases

Without this protocol, frames will be rejected. The protocol is strict by design — it's what keeps the model coherent across thousands of derivative metacategories.

### 3. Cross-tradition mappings

The model claims universality. We need critique and mapping from non-European traditions:

- **Buddhist** (mādhyamika dialectic, four-cornered logic, mandala traditions)
- **Hermetic and Sufi** (correspondence, polarity, transcendence)
- **Confucian** (relational ethics, the harmonious mean)
- **Indigenous epistemologies** (Andean *ayni*, Maya *uitz*, Aboriginal Dreamtime)
- **African** (Ubuntu, dialectical hermeneutics)

Mappings demonstrate (or refute) the universality claim. Open an issue with `cross-tradition-mapping` template.

### 4. Implementations and tooling

Code that helps others adopt the model:

- **Python parsers** for the JSON ontology
- **OWL / SKOS exporters** to integrate with Protégé, Stardog, GraphDB
- **JSON-LD adapters** for linked-data ecosystems
- **Embeddings** of the 80 categories (BERT / sentence-transformers / multilingual)
- **Verifier reference implementations** in PyTorch / JAX / Rust

These go in `examples/` or `scripts/` and are licensed under Apache 2.0 (see [LICENSE-CODE](LICENSE-CODE)).

### 5. Revisions and corrections

- **Category descriptions** — clarifications, better definitions, removal of ambiguity
- **Dialectical pairings** — proposing more accurate opposites if current ones don't hold up
- **Lineage attributions** — historical accuracy, additional sources, cross-references
- **Documentation** — typos, formatting, clarity

Open a PR or issue. Small corrections don't need a heavy review process.

## What we will NOT accept

- Changes to the **4 reflective axes** without strong philosophical argument and discussion. These are the foundational primitives.
- **Adding categories** without going through the N2 protocol. The 80-category set is meant to remain stable; new frames extend it without modifying it.
- **Politically or commercially motivated framings** that reduce the model to a particular ideology, brand, or product. The model is meant to be culturally neutral by structural design.
- **Closed-source forks** without a clear acknowledgment chain. The CC BY-SA 4.0 license requires share-alike for derivatives.

## Review process

1. Open an issue with the appropriate template **before** investing significant work
2. Discussion happens in the issue and (for design topics) in GitHub Discussions
3. PR submitted after issue agreement
4. Review by core maintainers against the N2 protocol where applicable
5. Merge or constructive rejection with reasoning

## Code of conduct

Be honest, rigorous, and humble. Critique the work, not the person. Acknowledge where you might be wrong. **The model is a tool for structural humility — apply that to discussion, too.**

Discrimination, harassment, or sustained bad faith leads to ban. We follow the spirit of the [Contributor Covenant](https://www.contributor-covenant.org/).

## Recognition

All contributors are credited in the repository's `CONTRIBUTORS.md` (to be created upon first external contribution) and in the next academic citation of the model.

## Contact

- **GitHub Issues**: for specific proposals
- **GitHub Discussions**: for design and philosophical topics
- **Email**: jordi@opengea.org
- **Telegram (CA)**: [@globaliumcat](https://t.me/globaliumcat)
