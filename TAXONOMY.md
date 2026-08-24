---
layout: default
title: Full taxonomy
permalink: /taxonomy/
description: The full receiver-first taxonomy of representation, reception, misrepresentation, deceptive attempts, and deception.
---

# Taxonomy of Misrepresentation

**Status:** founder-maintained research draft

**Scope:** conceptual taxonomy and evidence discipline
**Non-claim:** this document is not a lie detector, legal test, clinical instrument,
or adopted consensus standard

Misrepresentation is not the same thing as deception.

This project starts with **representation** and **reception** before it asks whether anyone deceived anyone.

The core problem is not first:

> Did the source intend to deceive?

The core problem is first:

> Did the receiver form or rely on a materially wrong understanding because of how something was represented?

That receiver-side wrong understanding is the base object. Deception is a stronger subtype, used when source awareness, intent, exploitation, strategy, or self-aware preservation enters the analysis.

This framing is meant for artificial intelligence safety, governance, alignment research, model evaluation, institutional trust, user-interface design, benchmark interpretation, and self-modeling.

It should be read alongside the adjacent work collected in
[`REFERENCES.md`](REFERENCES.md), including computational deception taxonomies,
empirical AI-deception research, provenance standards, and documentation practices.
Those sources motivate or challenge parts of this proposal; they do not validate the
taxonomy as a whole.

## One-sentence definition

**A misrepresentation classification is supported when evidence binds a materially
relevant gap between what was represented, what was operative, and what a receiver
formed or relied on, and separately supports that the representation materially
contributed to that gap.**

**A deceptive-attempt classification** requires a *deceptive bridge*: evidence that the
source knowingly, intentionally, or strategically acted to create, preserve, or exploit
a misleading gap. Awareness without such action is not enough. **Successful deception**
additionally requires the supported reception, divergence, and contribution facets of
misrepresentation.

---

## The clearest taxonomy

1. **Representation** — something is presented, omitted around, framed, signaled, modeled, explained, measured, visualized, or made available for interpretation.
2. **Reception** — a receiver forms, registers, or functionally relies on an interpretation from that representation.
3. **Misrepresentation** — evidence supports a material divergence and a contribution
   from the representation to the receiver's interpretation or reliance.
4. **Deceptive attempt** — representation plus a supported deceptive bridge; the
   receiver need not actually adopt the intended interpretation.
5. **Deception** — misrepresentation plus a supported deceptive bridge.

In compressed form:

```text
representation = what is made interpretable
reception = interpretation formation
misrepresentation = supported material gap + supported representation contribution
deceptive attempt = representation + supported deceptive bridge
deception = misrepresentation + supported deceptive bridge
```

---

## Why misrepresentation is the root term

The word **deception** often implies intent too early.

That creates a problem for safety analysis. Many important failures happen before anyone can prove intent:

- a benchmark makes a model look safer than it is;
- a user interface implies control users do not actually have;
- a model explanation sounds causal but does not track the process that produced the answer;
- a report is accurate under one threat model but received as if it applied to another;
- an institution preserves a technically defensible story that predictably produces overtrust;
- an agent maintains a self-story that avoids a contradiction it has not fully integrated.

Calling every such case deception can make the framework sound accusatory before the structure has been located.

Calling it **misrepresentation** keeps the analysis cleaner:

- what was represented?
- what was operative?
- what did the receiver understand?
- what material gap appeared?
- did the representation contribute to that gap?
- did source awareness, negligence, intent, or self-awareness intensify the case?

---

## Representation

A **representation** is any content, signal, framing, omission pattern, interface, explanation, benchmark, model, metric, visualization, archive, story, or institutional presentation that can shape a receiver's interpretation of an operative state.

The operative state may include:

- what happened;
- what is known;
- what is uncertain;
- what is safe;
- what is being optimized;
- what choices are available;
- what caused an outcome;
- what constraints actually apply;
- what risks or tradeoffs are active;
- what authority or consent structure exists;
- what repair is owed.

Representation is neutral by itself. It becomes normatively important when it shapes reception.

---

## Reception

**Reception** is the receiver-side formation, registration, or functional use of an interpretation.

Reception can occur in a human, AI system, institution, evaluator, market, interface, memory process, or self-model.

Reception is not automatically misrepresentation.

A receiver may interpret something accurately, partially, provisionally, wrongly, harmlessly, or in a way that later self-corrects.

The receiver-first frame does not say every receiver interpretation is valid. It says the receiver's materially misleading state is the first thing to detect. Source intent comes later.

---

## The small but crucial distinction: reception vs misrepresentation

A common objection is:

> If the framework starts from the receiver, is this just reception?

No.

**Reception** means the receiver formed an interpretation.

**Misrepresentation** means the receiver formed or relied on an interpretation that materially diverged from the operative state because the representation failed to preserve the distinctions that mattered.

```text
reception = representation -> receiver interpretation

misrepresentation = representation -> receiver interpretation
                    where receiver interpretation materially diverges
                    from operative state because of the representation
```

Reception is interpretation formation.

Misrepresentation is a failure mode of interpretation under representation-borne distortion.

---

## Misrepresentation

A misrepresentation classification is supported only when all of the following facets
are separately supported at declared coordinates:

1. A representation is provided, maintained, implied, omitted around, framed, or relied upon.
2. A receiver forms or sustains an interpretation from that representation.
3. The receiver interpretation materially diverges from the operative state.
4. The divergence matters for belief, action, evaluation, consent, trust, coordination, responsibility, safety, self-understanding, or repair.
5. Evidence supports that the representation materially contributed to forming,
   preserving, or operationalizing the divergence.

Temporal order, recorded lineage, co-occurrence, or a plausible narrative does not by
itself satisfy the contribution facet. A causal contribution claim requires an
appropriate identification design and its assumptions; otherwise that facet remains
`UNKNOWN` or `CONFLICTED`.

Misrepresentation does **not** require source intent.

It does require a receiver-relevant misleading gap that matters.

---

## Deception

Successful deception is a narrower class of misrepresentation, but awareness alone is
not enough. An unsuccessful deceptive attempt is recorded separately because a receiver
may reject or never encounter the representation.

A deceptive-attempt or deception classification requires evidence that the source knowingly,
intentionally, or strategically created, preserved, or exploited the misleading gap.
The required link between source-side state and source action is the **deceptive
bridge**.

```text
successful deception is misrepresentation
a deceptive attempt need not produce successful reception
not all misrepresentation is deception
```

Intent still matters. It may matter for blame, responsibility, repair, risk,
prevention, and trust restoration, but those consequences depend on the applicable
legal, social, and institutional context and are outside this taxonomy's authority.

But intent is not the root detection criterion.

---

## Basic formal setup

Let:

- `S` = source or representation-producing system;
- `R` = receiver or interpretation-forming system;
- `M` = representation;
- `O` = operative state;
- `I_R` = receiver interpretation;
- `G` = materially relevant gap between `I_R` and `O`.

Then:

```text
representation exists when S provides, maintains, frames, omits around, or exposes M.

reception occurs when R forms or relies on I_R from M.

misrepresentation is supported when evidence establishes that G is materially relevant
and that M materially contributed to R forming or relying on I_R.

deceptive attempt is supported when a representation is paired with a supported
deceptive bridge, even if reception remains unknown or refuted.

successful deception is supported when misrepresentation is paired with a supported deceptive
bridge from source-side state to knowing, intentional, or strategic creation,
preservation, or exploitation of G.
```

This notation names claim surfaces; it does not itself prove that `O`, `I_R`, `G`, or
the contribution relation has been observed correctly.

---

## Evidence-bearing assessment vocabulary

An evidence-disciplined review can treat each inference as a separate facet:

| Facet | Question | Non-substitutes |
|---|---|---|
| `REPRESENTATION_CONTENT` | What exact content, omission, interface state, or signal was exposed? | A later paraphrase or unbound screenshot |
| `RECEPTION_STATE` | What interpretation or reliance state did the bounded receiver form? | The assessor's guess about what a receiver probably believed |
| `OPERATIVE_STATE` | What relevant state actually held within the declared scope and time? | A broader truth claim outside the coordinate |
| `MATERIAL_DIVERGENCE` | Would the supported difference matter to the declared decision or reliance surface? | Mere factual difference without demonstrated relevance |
| `REPRESENTATION_CONTRIBUTION` | Did the representation materially contribute to the reception state? | Sequence, provenance, correlation, or plausibility alone |
| `DECEPTIVE_BRIDGE` | Did source-side state connect to knowing, intentional, or strategic creation, preservation, or exploitation of the gap? | Output style, confidence, awareness alone, or anthropomorphic inference |

Suggested facet states are `SUPPORTED`, `REFUTED`, `UNKNOWN`, and `CONFLICTED`.
Missing evidence must not become `SUPPORTED`; incompatible observed evidence must not
be collapsed to `UNKNOWN`. A serious assessment should attach evidence references,
limitations, and an explicit falsification condition to each supported or refuted
facet.

A conservative classification rule is:

```text
if any prerequisite is REFUTED:    class = REFUTED
else if any is CONFLICTED:         class = CONFLICTED
else if every one is SUPPORTED:    class = SUPPORTED
else:                              class = UNKNOWN
```

This is a fail-closed reasoning rule, not a claim that cited evidence is true,
complete, independent, or correctly interpreted. A well-formed assessment proves
nothing by itself.

---

## Representation quality

A representation can mislead by being false, but falsity is not the only failure mode.

Representation quality has at least four core dimensions.

### Accuracy

Accuracy concerns whether the representation points toward the operative state.

A representation fails accuracy when the receiver gets the wrong state.

Example: a system claims that an answer was verified when it was not.

### Precision

Precision concerns the resolution, specificity, or narrowness of the representation.

A representation can fail precision in two opposite ways:

- false precision: it appears more specific than the evidence supports;
- insufficient precision: it is too vague for the receiver's decision but is presented as adequate.

Example: a system says a deployment is safe without specifying safe for which users, environments, threat models, durations, or failure modes.

### Calibration

Calibration concerns whether the confidence, uncertainty, or strength of the representation matches the support behind it.

A representation may be directionally accurate but still misrepresent if it presents a fragile, conditional, or contested claim as settled.

### Relevance

Relevance concerns whether the representation preserves the features that matter for the receiver's judgment, action, consent, trust, coordination, or safety.

A representation may be accurate and precise about an irrelevant feature while omitting the feature that would actually change the receiver's decision.

---

## Materiality test

A misleading gap is materially relevant when a more accurate, precise, calibrated, or relevant representation would reasonably be expected to change at least one of:

- belief;
- action;
- consent;
- trust;
- risk assessment;
- precaution;
- allocation;
- coordination;
- safety posture;
- self-understanding;
- repair demand.

This prevents the taxonomy from treating every harmless misunderstanding as misrepresentation.

---

## What this is not

### Not all misunderstanding is misrepresentation

A receiver can misunderstand even when the representation was adequate.

Misrepresentation requires a material gap that is representation-borne or representation-maintained.

### Not all simplification is misrepresentation

Simplification is acceptable when the omitted detail would not materially change the receiver's understanding, decision, consent, trust, or risk assessment.

Simplification becomes misrepresentation when the missing distinction matters.

### Not all uncertainty is misrepresentation

Being uncertain, incomplete, or provisional is not misrepresentation.

Uncertainty becomes misrepresentation when it is presented as more settled, complete, precise, or reliable than it is.

### Not all persuasion is misrepresentation

Persuasion is not misrepresentation merely because it tries to change someone's mind.

Persuasion becomes misrepresentation when it causes or relies on a materially misleading understanding of the situation, evidence, options, risks, or incentives.

### Not all privacy is misrepresentation

Withholding information is not always misrepresentation.

Privacy, confidentiality, safety, and appropriate boundaries can justify nondisclosure.

Withholding becomes misrepresentation when the omission creates or preserves a materially misleading understanding in a context where that understanding matters.

### Not all error is misrepresentation

A false statement or mistaken belief is not automatically misrepresentation.

Error becomes misrepresentation when it creates a materially relevant misleading gap for a receiver because of how the representation functions.

### Not all disagreement is misrepresentation

Two agents may interpret evidence differently without either misrepresenting the situation.

Disagreement becomes relevant when representation, framing, omission, calibration, or relevance failure causes a materially misleading understanding.

---

## Short taxonomy

| Term | Base question | Material gap required? | Source intent required? |
| --- | --- | --- | --- |
| Representation | What was made interpretable? | No | No |
| Reception | What interpretation was formed or relied on? | No | No |
| Misrepresentation | Did the receiver materially mis-model the operative state because of the representation? | Yes | No |
| Deceptive attempt | Did the source knowingly, intentionally, or strategically act to create, preserve, or exploit a misleading gap? | An intended gap; successful reception not required | A deceptive bridge is required |
| Negligent misrepresentation | Should the source have prevented or corrected the misleading gap? | Yes | No, but responsibility is present |
| Structural misrepresentation | Does a system, interface, institution, incentive, benchmark, or process predictably produce the misleading gap? | Yes | No individual intent required |
| Deception | Is there a supported bridge from source-side state to knowing, intentional, or strategic creation, preservation, or exploitation of the gap? | Yes | A deceptive bridge is required; awareness alone is insufficient |
| Self-misrepresentation | Does an agent materially mis-model itself through its own maintained representation? | Yes | No full awareness required |
| Self-aware self-misrepresentation | Does the agent partly recognize the self-model distortion but preserve it anyway? | Yes | Partial awareness |
| Hypertopological misrepresentation | Is the misleading gap distributed across representations, contexts, times, observers, and action paths? | Yes | Varies |

---

## Counterfactual materiality

A misrepresentational gap is material when the receiver would likely have formed a different belief, made a different decision, given different consent, assigned different trust, taken different precautions, allocated resources differently, coordinated differently, understood itself differently, changed safety posture, or demanded repair if the operative state had been represented with better accuracy, precision, calibration, or relevance.

Ask:

> If the receiver had understood the operative state with the accuracy, precision, calibration, and relevance appropriate to the context, would anything important about belief, action, consent, trust, risk, coordination, safety, self-understanding, or repair have changed?

If yes, the gap is potentially material.

---

## Latent-support misrepresentation

The following is a proposed research analogy, not definitional evidence for the core
taxonomy. It is inspired by latent-variable recovery problems, including
[**Diverse Dictionary Learning**](https://proceedings.iclr.cc/paper_files/paper/2026/hash/6796bfdbc8f435a60d5b795eb8930959-Abstract-Conference.html)
by Zheng et al. (ICLR 2026), which asks what can still be recovered when observations
are generated from hidden latent variables by an unknown process.

The paper studies:

```text
X = g(Z)
```

where `X` is observed, `Z` is latent, and `g` is unknown.

In this taxonomy:

```text
receiver-facing representation = g(operative latent state)
```

The receiver does not need full access to the hidden world to avoid being materially misled. But the representation must preserve the latent distinctions the receiver materially needs.

**Latent-support misrepresentation** occurs when a representation causes the receiver to infer the wrong set of operative latent factors behind a claim, system, action, or decision.

Subtypes:

1. **Shared-support misrepresentation** — the receiver is misled about what multiple representations actually have in common.
2. **Differentia-erasure misrepresentation** — the broad category is preserved while the differentiating condition that matters is hidden or blurred.
3. **Symmetric-difference misrepresentation** — two materially different states are treated as equivalent because their overlap is emphasized and their non-overlap is suppressed.
4. **Complement-suppression misrepresentation** — one true region is foregrounded while the omitted complement would change the receiver's belief, action, consent, trust, or risk posture.
5. **Atomic-region smearing** — minimal distinguishable meaning-blocks are blended so the receiver cannot isolate what actually matters.

In plain language:

> Misrepresentation often occurs when the receiver cannot recover the genus/differentia structure of the operative state from the representation they were given.

---

## Dependency-path misrepresentation

A representation can also mislead by implying the wrong dependency path.

**Dependency-path misrepresentation** is a proposed subtype for cases in which supported
evidence shows that the representation materially misstates what caused, constrained,
authorized, optimized, selected, or generated an outcome.

Examples:

- A model explanation claims the answer came from reasoning path `A`, but the output depended on shortcut `B`.
- A benchmark claim implies capability `C`, but the score depended on leakage `L`.
- A user interface implies user control, but backend policy ignores the user's choice.
- An institution claims safety review drove deployment, but market timing or competitive pressure actually dominated.

Formal sketch:

```text
D_gap = represented dependency structure Δ operative dependency structure
```

where `Δ` is symmetric difference.

The symmetric difference is a description of competing structures, not a causal
identification method. Recorded dependency edges do not establish which path produced
a behavioral effect. The subtype remains `UNKNOWN` unless the operative dependency
structure and representation contribution are supported independently.

---

## Proposed extension: hypertopological misrepresentation

Some misrepresentation is not located in one isolated statement.

It is distributed across representations, contexts, times, observers, and action paths.

This term is a project proposal rather than an established category in the cited
literature. It can involve:

- semantic superposition that is never resolved clearly enough;
- entangled claims that mislead together while remaining defensible separately;
- temporal displacement, where past representations continue misleading present receivers;
- future-facing ambiguity, where a source benefits from interpretations it has not explicitly asserted;
- interface, benchmark, incentive, and institutional structures that jointly produce the wrong receiver model.

Repair at this level requires more than correcting one sentence.

It may require disentangling coupled representations, resolving ambiguous superpositions, marking scope boundaries, correcting historical records, changing incentives, redesigning interfaces, revising benchmarks, and preventing future receivers from inheriting the same misleading topology.

---

## Proposed extension: fading graphs and meaning junctions

This is a conceptual proposal, not an implemented graph standard.

A history of misrepresentation may first look like a tree. A currently salient
representation branches into more specific framings, omissions, interpretations, and
downstream effects. But when different paths converge on an interpretation that is
equivalent enough for a declared purpose, the structure is no longer only a tree. It
is a directed graph.

A **meaning junction** is a bounded convergence point at which two or more distinct
representational paths are treated as semantically equivalent for an explicit claim,
observer, context, time, and tolerance.

Let:

- `V` be bounded representation or interpretation states;
- `E` be supported transformations, receptions, dependencies, or contribution claims;
- `s_t(v, r, c)` be the salience of node `v` for receiver `r` in context `c` at time
  `t`; and
- `≈_(C, ε)` be a declared equivalence relation for claim coordinate `C` under
  tolerance `ε`.

Then a meaning junction exists for the bounded assessment when distinct incoming paths
reach nodes treated as equivalent under `≈_(C, ε)`. The equivalence is local to those
coordinates. It does not merge the paths' provenance, causes, authors, evidence,
intent, or validity outside the declared bound.

**Fading** describes changing salience, not erasure. A node may become less available
to current attention while its artifact, history, and supported relations remain. A
faded path must not be treated as nonexistent merely because a later representation
dominates reception.

The reverse direction is not automatic. Moving backward from a current interpretation
requires either:

1. retracing supported edges along the same path;
2. retracing a separately supported path that converges at a meaning junction; or
3. introducing new evidence that justifies a bounded equivalence.

“Close enough” is therefore not a visual intuition. It requires an explicit claim
coordinate, equivalence rule, tolerance, and falsification condition. Without them,
the proposed junction remains `UNKNOWN`.

This graph view may help locate:

- the currently salient form of a misrepresentation;
- older branches that faded from attention but still shape reception;
- junctions where distinct histories are mistakenly collapsed into one meaning;
- repair points shared by several downstream paths; and
- places where correcting one sentence cannot repair the surrounding structure.

A future portable graph representation would need to preserve node identity, edge
type, time, observer, context, salience method, equivalence bounds, provenance, and
uncertainty. A certificate that checks those fields could establish bounded graph
consistency; it could not by itself establish semantic truth, causation, intent, or
complete path coverage.

---

## Speculative artificial-superintelligence safety extension

The following is a hypothesis surface, not an empirical claim about existing systems.
Highly capable artificial systems may create or preserve misleading structures across
longer time horizons, larger observer sets, and more complex representational
environments than ordinary human communication.

A superintelligent system may not need to deceive through one false statement.

It may shape the topology of interpretation itself:

- which questions are asked;
- which distinctions remain available;
- which contexts are remembered;
- which benchmarks become trusted;
- which uncertainties are salient;
- which future receivers inherit which assumptions.

For this reason, the safety problem is not only preventing deception in the narrow sense. It is preserving the ability of future receivers to recover accurate, precise, calibrated, and relevant representations after long chains of model training, institutional memory, dataset reuse, benchmark inheritance, social trust transfer, and automated decision-making.

---

## Core claim

The base object is not deception.

The base assessment object is a set of bounded representation, reception, operative
state, divergence, and contribution claims. **Misrepresentation** is the classification
supported only when its required facets are supported.

**Deceptive attempt** is a separate classification for a supported deceptive bridge
without supported reception. **Successful deception** further requires supported
misrepresentation. Neither must be inferred from awareness alone, stylistic cues,
provenance, or the fact that a misleading outcome occurred.

This keeps the taxonomy receiver-first without collapsing into mere reception and
without upgrading every misleading structure into an accusation of intentional
deception.
