---
layout: default
title: Overview
permalink: /
description: A receiver-first taxonomy for separating misleading effects from evidence of intentional or strategic deception.
---

# Taxonomy of Misrepresentation

## What is this?

This is a formal research vocabulary for asking when a representation becomes a
**misrepresentation**, and when the evidence is strong enough to support the narrower
claim of **deception**.

It begins with observable relationships rather than an accusation:

```text
representation -> reception -> operative state -> material divergence
               -> representation contribution -> deceptive bridge
```

The deceptive bridge is the extra evidence connecting source-side state to knowing,
intentional, or strategic action. Without it, deception remains `UNKNOWN` even when a
misleading effect is well supported.

## Start here

| Read | If you want to... |
|---|---|
| [Full taxonomy](taxonomy/) | Inspect definitions, formal structure, materiality, non-examples, and proposed extensions |
| [AI-agent boundary](agent-misrepresentation/) | Evaluate agent self-presentation or strategic behavior without inferring hidden intent from output alone |
| [Synthetic examples](examples/) | See misrepresentation, conflicted intent evidence, failed deceptive attempts, and supported synthetic deception kept distinct |
| [VSTD relationship](vstd-relation/) | Understand how this work led toward verifier-standard and how the two may compose |
| [Research sources](references/) | Compare the proposal with published deception, causality, provenance, and documentation work |

The full taxonomy also introduces **meaning junctions**: bounded convergence points
where distinct representational paths are equivalent enough for one declared purpose
without merging their provenance, causes, intent, or wider meaning.

## What the taxonomy prevents

- a false statement becoming proof of intent;
- chronology or provenance becoming proof of causal contribution;
- awareness becoming proof of deceptive action;
- a deceptive attempt becoming successful deception without reception;
- missing evidence becoming a favorable result; and
- conflicting evidence disappearing into an undifferentiated “unknown.”

## Assessment vocabulary

| Result | Meaning in a bounded assessment |
|---|---|
| `SUPPORTED` | The declared evidence supports the facet under stated limits |
| `REFUTED` | The declared evidence establishes a contradictory result under stated limits |
| `UNKNOWN` | The available evidence does not establish the facet |
| `CONFLICTED` | Materially incompatible evidence is present and unresolved |

These words organize a review. They are not the output of a detector shipped by this
repository, and they do not make the underlying evidence true or complete.

## Why verifier-standard is related

This taxonomy was an intermediate research branch in the path that later produced
[verifier-standard](https://github.com/TimeLordRaps/verifier). The taxonomy focuses on
one domain; VSTD generalizes the claim-boundary discipline so results from different
verification substrates can be expressed and compared without replacing the native
verifiers.

## Project boundary

This is a founder-maintained research draft. It is not a lie detector, legal test,
clinical instrument, adopted standard, VSTD profile, or validated method for reading
an agent's hidden state. The public invitation is to challenge its distinctions and
construct counterexamples, not to use its vocabulary as an unsupported accusation.
