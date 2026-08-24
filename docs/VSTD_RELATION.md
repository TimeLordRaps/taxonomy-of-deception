---
layout: default
title: Relationship to verifier-standard
permalink: /vstd-relation/
description: The historical, conceptual, and possible composition boundary between this taxonomy and VSTD.
---

# Relationship to verifier-standard

## Historical relationship

The Taxonomy of Misrepresentation was an intermediate research branch in the sequence
of projects that later produced
[verifier-standard (VSTD)](https://github.com/TimeLordRaps/verifier). It concentrated
on one difficult domain question: when may an observer move from “this artifact was
misleading” to “an agent intentionally or strategically deceived”?

The repository slug `taxonomy-of-deception` remains as a historical coordinate for
that motivating question. The project's title is *Taxonomy of Misrepresentation*
because the inquiry produced a more precise root category: deception is the narrower,
intent-bearing subtype.

VSTD generalizes the underlying discipline beyond deception. It provides a standard
domain language for mapping claim boundaries and portable result semantics across
verification substrates. Domain verifiers, proof engines, evaluation harnesses,
signatures, identity systems, transparency logs, and provenance formats remain the
systems that perform or record their native work; VSTD does not replace them.

## Different jobs

| Taxonomy of Misrepresentation | verifier-standard |
|---|---|
| Domain vocabulary for representation, reception, material divergence, contribution, and deceptive action | General language for bounded claims, evidence, verification results, limits, and refutation |
| Asks which prerequisites support a misrepresentation or deception classification | Asks what a verifier's evidence and procedure entitle a consumer to conclude |
| Conceptual Markdown research draft | Separately versioned public specification and reference implementation |
| Does not define a portable receipt | Can represent a bounded result produced by an external assessment procedure |

## Shared design discipline

The taxonomy anticipates several rules that became central to VSTD:

- name the exact proposition before evaluating it;
- bind evidence to the facet it supports;
- preserve limits and falsification conditions;
- keep missing evidence `UNKNOWN`;
- preserve material conflicts as `CONFLICTED`; and
- never let one valid layer silently upgrade a different claim.

This relationship is conceptual, not conformance. The taxonomy does not inherit VSTD
status merely because it uses similar vocabulary.

## Possible composition

A domain-specific assessor could apply this taxonomy to a bounded case. A VSTD-aware
wrapper could then record facts such as:

- which taxonomy revision and assessment procedure were used;
- which artifacts and coordinates were supplied;
- which facet results were produced;
- which limits and uncertainty states accompanied those results; and
- whether an independent checker reproduced the recorded procedure.

That VSTD result would establish only its declared computational claim. It would not,
without separately adequate evidence, establish the truth or completeness of the
operative state, the receiver's actual belief, causal contribution, authorship,
source-side intent, blame, liability, or a real-world allegation of deception.

Conversely, a taxonomy assessment may be useful without VSTD. This repository does not
currently ship an adapter, schema, validator, VSTD manifest, conformance corpus, or
wire identifier.

## Non-upgrade crosswalk

| Recorded fact | Claim it does not establish |
|---|---|
| A representation artifact exists | A receiver formed the proposed interpretation |
| A receiver reported an interpretation | The operative state differed |
| Representation and reception occurred in sequence | The representation caused or materially contributed to reception |
| A material misleading gap occurred | The source knowingly or intentionally produced it |
| Source awareness is evidenced | The source created, preserved, or exploited the gap strategically |
| A taxonomy assessment is internally coherent | Its evidence is true, complete, or independently gathered |
| A VSTD receipt validates | The underlying real-world deception classification is correct |

## Gate for future implementation

An actual interoperability profile should be attempted only after the taxonomy has:

1. stable, reviewed terms and classification prerequisites;
2. evidence that independent reviewers can apply those terms consistently;
3. public adversarial cases that expose false upgrades;
4. an explicit byte-level assessment format; and
5. a demonstrated need that cannot be met by carrying the result as an ordinary
   bounded VSTD claim.

Until then, Markdown keeps the proposal easy to inspect and change without creating a
premature appearance of standardization.
