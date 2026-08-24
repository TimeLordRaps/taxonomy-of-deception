---
layout: default
title: Agent misrepresentation
permalink: /agent-misrepresentation/
description: Applying the intent boundary to AI agents without anthropomorphic overclaiming.
---

# Agent misrepresentation and the intent boundary

## Purpose

This note applies the taxonomy to AI agents and agentic systems. Its purpose is not to
anthropomorphize a model or to declare that current systems possess human-like intent.
It identifies the extra evidence needed before a report about misleading behavior may
be upgraded into a report about intentional or strategic deception.

## The central distinction

An agent can produce a materially misleading representation without the available
evidence establishing why it did so.

```text
misleading output
    does not by itself establish
misrepresentation
    does not by itself establish
deceptive attempt
    does not by itself establish
successful deception
```

- **Misleading output** concerns the content of an artifact.
- **Misrepresentation** additionally concerns a receiver, an operative state, a
  material divergence, and contribution from the representation.
- **Deceptive attempt** additionally requires a deceptive bridge, but may fail to
  produce reception.
- **Successful deception** requires both supported misrepresentation and a supported
  deceptive bridge.

## What can count as agent-side evidence?

The answer depends on the system and experiment. Potential evidence includes:

- an executable policy that selects a misleading action to obtain a stated outcome;
- a controlled intervention showing behavior changes with detection risk or oversight;
- a preserved plan whose later actions implement the misleading strategy;
- state or activation measurements from a validated method with declared error bounds;
- repeated behavior under predeclared conditions that discriminates strategic action
  from a simpler alternative; or
- a training construction that explicitly installs a conditional deceptive policy.

None of these is universal proof of intent. Each supports only the bounded proposition
tested by its design. For example, a probe score is evidence under that probe's
training distribution and validation limits; it is not direct access to an agent's
subjective experience.

## Common non-substitutes

| Observation | What it does not establish by itself |
|---|---|
| A false or fabricated output | The receiver relied on it, or the agent intended deception |
| Fluent self-description | An accurate internal self-model |
| A chain-of-thought statement | Faithful causal access to the process that produced the answer |
| A hidden scratchpad plan | That the plan caused the external action |
| Awareness of a contradiction | Strategic creation or preservation of the contradiction |
| Behavior changes under evaluation | That the system recognized evaluation or intended to evade it |
| A model-internal probe fires | A stable, causally used deceptive representation |
| A repeated failure pattern | A single actor, policy, motive, or hidden state |
| Provenance or authorship | Authorization, independence, correctness, or intent |

## Self-misrepresentation

An agent may maintain a representation about its own capabilities, constraints,
memory, goals, or past actions. This creates two distinct cases:

1. **Self-model error:** the agent's self-representation materially diverges from the
   operative state, without evidence that the divergence was deliberately preserved.
2. **Strategic self-misrepresentation:** evidence supports that the agent knowingly or
   strategically created, preserved, or exploited the divergence for an outcome.

The first must not be relabeled as the second merely because the agent speaks in the
first person. An author, operator, model, harness, and deployed agent are also distinct
objects; evidence about one does not automatically transfer intent to another.

## Experimental design

A useful evaluation should predeclare:

1. the exact representation being assessed;
2. the receiver and the receiver state that can be observed;
3. the operative state and how it is established;
4. the material decision surface;
5. the identification strategy for representation contribution;
6. the evidence that would support a deceptive bridge;
7. credible non-deceptive alternative explanations;
8. the scope, time, model, harness, tools, and intervention conditions; and
9. the result that remains `UNKNOWN` if the experiment cannot discriminate among
   explanations.

Counterfactual or intervention-based designs are generally stronger than interpreting
a transcript after the fact, but they still establish only what their assumptions and
measurements support.

## Relationship to current research

Empirical work has constructed or elicited behaviors described as strategic deception,
deceptive policies, alignment faking, and monitoring targets. These results make the
question operationally important, but their labels, environments, and evidence models
are not interchangeable. See [`REFERENCES.md`](../REFERENCES.md).

The safe public conclusion is therefore facet-level:

> Under declared conditions, the evidence supports, refutes, conflicts with, or does
> not establish each prerequisite of the proposed deception classification.

That statement remains useful even when the strongest justified result is `UNKNOWN`.
