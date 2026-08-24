# Taxonomy of Misrepresentation

**A receiver-first vocabulary for separating misleading effects from evidence of
intentional or strategic deception.**

[![License: Apache-2.0](https://img.shields.io/badge/license-Apache--2.0-2f7d6d.svg)](LICENSE)
[![Status: research draft](https://img.shields.io/badge/status-research%20draft-d97706.svg)](#status-and-limits)

**[Read the navigable site](https://timelordraps.github.io/taxonomy-of-deception/)**

This project asks a narrow question that is easy to overstate:

> When does an agent merely produce a misleading representation, and when does the
> evidence justify saying that the agent intentionally or strategically deceived?

The answer is not inferred from confidence, style, a false output, or an undesirable
outcome. The taxonomy separates the observable pieces first:

```text
representation -> reception -> operative state -> material divergence
               -> representation contribution -> deceptive bridge
```

The **deceptive bridge** is the additional evidence connecting source-side state to
knowing, intentional, or strategic creation, preservation, or exploitation of the
misleading gap. Without that bridge, deception remains `UNKNOWN` even when
misrepresentation is well supported.

## Core distinctions

| Classification | What must be supported |
|---|---|
| Representation | A bounded representation exists |
| Reception | A bounded receiver interpretation or reliance state is evidenced |
| Misrepresentation | Representation, reception, operative state, material divergence, and representation contribution |
| Deceptive attempt | Representation plus a deceptive bridge; successful reception is not required |
| Deception | Misrepresentation plus a deceptive bridge |

Recorded provenance is not causal contribution. Awareness is not automatically
deceptive action. An agent's output is not direct access to its hidden state. Missing
evidence remains `UNKNOWN`; materially incompatible evidence remains `CONFLICTED`.

## Relationship to verifier-standard

This repository is an intellectual predecessor and domain-specific companion to
[verifier-standard (VSTD)](https://github.com/TimeLordRaps/verifier). It captured an
intermediate problem in the development path that later produced VSTD: how to prevent
an assessment from silently becoming stronger than its evidence.

### Why the repository is still named `taxonomy-of-deception`

The repository slug is intentionally retained as both a historical coordinate and a
self-referential example. `taxonomy-of-deception` is the narrower representation that
first frames the reader's expectation; *Taxonomy of Misrepresentation* is the broader
operative scope reached by the work. The gap draws attention to how a label can shape
reception before the underlying distinctions are inspected.

That mismatch is disclosed rather than hidden. It is therefore **not automatically an
example of deception** under this taxonomy: a deception classification would still
require evidence of reception, material divergence, contribution, and a deceptive
bridge. The name demonstrates the depth at which misrepresentation can operate without
using its own lesson to overclaim intent.

The projects now have different jobs:

- **This taxonomy** names the parts of a bounded misrepresentation or deception
  assessment.
- **VSTD** is a standard domain language for expressing claim boundaries and portable
  result semantics across verification substrates.
- A domain verifier, proof engine, evaluator, provenance system, or human review can
  supply evidence. Neither project replaces those systems.
- VSTD can carry a bounded result about a taxonomy assessment, but a valid VSTD
  receipt does not make an allegation of deception true.

This repository is **not** a VSTD profile, conformance suite, or extension. It defines
no VSTD wire identifiers and claims no interoperability implementation. The exact
relationship is documented in [`docs/VSTD_RELATION.md`](docs/VSTD_RELATION.md).

## Read the project

| Document | Purpose |
|---|---|
| [`TAXONOMY.md`](TAXONOMY.md) | Full taxonomy, definitions, formal sketch, non-examples, and proposed extensions |
| [`docs/AGENT_MISREPRESENTATION.md`](docs/AGENT_MISREPRESENTATION.md) | Applying the intent boundary to AI agents without anthropomorphic overclaiming |
| [`examples/ASSESSMENTS.md`](examples/ASSESSMENTS.md) | Four synthetic cases showing the non-upgrade rules |
| [`docs/VSTD_RELATION.md`](docs/VSTD_RELATION.md) | Project lineage and the conceptual seam with VSTD |
| [`REFERENCES.md`](REFERENCES.md) | Research and standards that inform or challenge the proposal |

## Status and limits

This is a founder-maintained **research draft**, not an adopted standard or validated
detector. There is no demonstrated external adoption, independent implementation,
inter-rater validation, legal authority, clinical validity, or consensus terminology.

It must not be used to infer intent from linguistic style, confidence, model output,
or a single failure. It does not decide whether a person or system is dishonest. Its
purpose is to make each step in such a claim visible, bounded, and challengeable.

Useful review includes:

1. counterexamples to the classification prerequisites;
2. cases where `UNKNOWN`, `CONFLICTED`, and `REFUTED` are mishandled;
3. hidden cultural or domain assumptions in the materiality test;
4. evidence that a proposed facet cannot be observed or falsified; and
5. places where existing research already uses a better term.

Use [GitHub issues](https://github.com/TimeLordRaps/taxonomy-of-deception/issues) for
public, bounded counterexamples. Do not post private evidence, personal data, or
unsupported accusations about identifiable parties.

Apache License 2.0. See [`LICENSE`](LICENSE).
