---
layout: default
title: References and related work
permalink: /references/
description: Research and standards informing or challenging the Taxonomy of Misrepresentation.
---

# References and related work

This project does not claim to have invented deception, misrepresentation,
provenance, causal identification, documentation, or bounded verification. The
receiver-first decomposition proposed here should be evaluated against adjacent work,
not treated as a replacement for it.

The annotations below state why each source is relevant and what it does **not**
establish for this project.

## Deception definitions and computational taxonomies

- Verma et al., [“Domain-independent deception: a new taxonomy and linguistic
  analysis”](https://doi.org/10.3389/fdata.2025.1581734), *Frontiers in Big Data* 8
  (2025). This peer-reviewed article proposes a computational definition and a
  multi-dimensional taxonomy for domain-independent deception. Its categories and
  empirical results do not validate this project's receiver-first prerequisites.
- Park et al., [“AI Deception: A Survey of Examples, Risks, and Potential
  Solutions”](https://doi.org/10.1016/j.patter.2024.100988), *Patterns* 5(5) (2024).
  This peer-reviewed survey defines AI deception in terms of systematically inducing
  false beliefs in pursuit of an outcome and surveys reported cases and risks. A case
  described in a survey is not direct evidence for a new allegation.
- Papantoniou, Papadakos, and Plexousakis,
  [“Evaluating LLMs on Deceptive Text across Cultures”](https://aclanthology.org/2025.ranlp-1.101/),
  RANLP (2025). The results show context-dependent performance across languages,
  domains, and cultural proxies. They caution against treating linguistic cues as a
  universal intent detector.

## Agent behavior and strategic deception

- Scheurer, Balesni, and Hobbhahn,
  [“Large Language Models can Strategically Deceive their Users when Put Under
  Pressure”](https://arxiv.org/abs/2311.07590) (arXiv preprint, 2023). This controlled
  simulated-agent study motivates separating misleading behavior, reported reasons,
  and evidence about strategy. Its setup does not establish a general property of
  language models.
- Hubinger et al., [“Sleeper Agents: Training Deceptive LLMs that Persist Through
  Safety Training”](https://arxiv.org/abs/2401.05566) (arXiv preprint, 2024). The work
  constructs proof-of-concept conditional policies as model organisms of
  misalignment. Constructed behavior supports claims about that experimental design,
  not the prevalence of naturally arising deception.
- Goldowsky-Dill et al., [“Detecting Strategic Deception with Linear
  Probes”](https://proceedings.mlr.press/v267/goldowsky-dill25a.html), ICML (2025).
  This peer-reviewed study tests activation probes on selected deceptive-behavior
  settings and explicitly reports that current performance is not a robust defense.
  A probe score must therefore remain bounded to its validation conditions.
- Chaudhury and Shiromani, [“ChameleonBench: Quantifying Alignment Faking in Large
  Language Models”](https://proceedings.mlr.press/v304/chaudhury26a.html), ACML 2025
  proceedings (published 2026). This benchmark operationalizes one form of behavioral
  inconsistency. A benchmark label does not by itself prove a hidden motive or stable
  internal state.

These experiments use different interventions, labels, and evidence models. This
repository does not treat “strategic deception,” “deceptive policy,” “alignment
faking,” and “misrepresentation” as interchangeable outcomes.

## Causal identification and provenance

- W3C, [PROV-DM](https://www.w3.org/TR/prov-dm/) and
  [PROV-O](https://www.w3.org/TR/prov-o/) (W3C Recommendations, 2013). These standards
  represent entities, activities, agents, derivations, and qualified influence.
  Provenance is relevant evidence, but a recorded lineage or influence relation must
  not be silently upgraded into behavioral causation or intent.
- W3C, [SKOS Simple Knowledge Organization System
  Reference](https://www.w3.org/TR/skos-reference/) (W3C Recommendation, 2009). SKOS
  distinguishes hierarchical and associative concept relations and separates
  `exactMatch` from weaker mapping relations such as `closeMatch`. The proposed
  “meaning junction” should reuse that discipline: bounded similarity must not become
  universal identity, and distinct provenance paths must remain distinct.
- Hernán and Robins, [*Causal Inference: What
  If*](https://miguelhernan.org/whatifbook) (2020; living online edition).
  Counterfactual effects require an identification strategy and assumptions. This is
  why chronological order or plausible narrative does not satisfy the taxonomy's
  representation-contribution facet by itself.

## Documentation and disclosure

- Mitchell et al., [“Model Cards for Model
  Reporting”](https://doi.org/10.1145/3287560.3287596), FAT* (2019).
- Gebru et al., [“Datasheets for
  Datasets”](https://doi.org/10.1145/3458723), *Communications of the ACM* (2021).

These formats make scope, intended use, provenance, limitations, and evaluation
conditions more visible. Better disclosure can reduce misleading reception, but the
existence of a model card or datasheet does not establish correctness, completeness,
or good intent.

## Bounded verification

- TimeLordRaps, [verifier-standard
  (VSTD)](https://github.com/TimeLordRaps/verifier), release
  [`v1.1.3`](https://github.com/TimeLordRaps/verifier/releases/tag/v1.1.3) (2026).
  VSTD is a separate founder-maintained alpha project that standardizes bounded claim
  boundaries and portable result semantics across verification substrates. This
  taxonomy is not a VSTD profile or conformance implementation. See
  [`docs/VSTD_RELATION.md`](docs/VSTD_RELATION.md).

## Latent-variable analogy

- Zheng et al., [“Diverse Dictionary
  Learning”](https://proceedings.iclr.cc/paper_files/paper/2026/hash/6796bfdbc8f435a60d5b795eb8930959-Abstract-Conference.html),
  ICLR (2026). The taxonomy uses its set-theoretic latent-support results only as a
  research analogy. Those results do not validate this project's materiality,
  contribution, or deception definitions.

## Open research gaps

The cited literature does not establish for this repository:

- construct validity or inter-rater reliability for the proposed facets;
- cross-cultural stability of the materiality test;
- a generally valid method for observing receiver state or source-side intent;
- legal equivalence to fraud, deceit, negligent misrepresentation, or disclosure duty;
- accuracy of an automated taxonomy classifier; or
- applicability to the hidden internal states of arbitrary advanced AI systems.
