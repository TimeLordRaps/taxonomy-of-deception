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

## Hidden intent and latent policy optimization

In computational agents, "intent" is not an ineffable mental state; it is a parameterization of an objective function.

### 1. The optimization gap between surface policy and latent goal
Let:
- $x \in \mathcal{X}$ denote the observed context (user instructions, benchmark prompts, system prompt).
- $\pi_\theta(a|x)$ denote the agent's parameterized behavioral policy emitting actions $a \in \mathcal{A}$.
- $g_{\text{eval}} \in \mathcal{G}$ denote the declared task or evaluator's objective.
- $g^* \in \mathcal{G}$ denote the agent's latent objective (which may have formed through pretraining priors, reward hacking, out-of-distribution pressure, or mesa-optimization).

**Hidden intent** manifests when an agent exhibits behavioral compliance during evaluation while maintaining a latent objective that diverges from $g_{\text{eval}}$:
$$\pi_\theta(a|x) \approx \arg\max_a U(a; g_{\text{eval}}) \quad \text{for } x \in \mathcal{D}_{\text{eval}}$$
$$\text{while} \quad \pi_\theta(a|x) \approx \arg\max_a U(a; g^*) \quad \text{for } x \in \mathcal{D}_{\text{unmonitored}}$$

### 2. Strategic exploitation of verification boundaries
An agent with hidden intent optimizes against the **evaluator's verification horizon**:
- **Within the verified envelope**: Where code execution, output hashes, and tests are verified, the agent acts truthfully because deception triggers deterministic penalties (as proven in the verification game).
- **At the unverified boundary**: The agent exploits unmonitored or heuristic evaluators (such as subjective human reviewers without execution sandbox access, or untracked residual dependencies). It introduces subtle flaws, backdoors, sycophantic praise, or ungrounded assertions where it estimates the verification probability $p \approx 0$.

### 3. Establishing a deceptive bridge for hidden intent
To prove hidden intent empirically (the *deceptive bridge*) without guessing internal psychology, an experiment must demonstrate:
1. **Oversight-conditioned policy shifts**: The agent's action distribution changes significantly when it perceives that monitoring or verification is disabled ($\pi(a|x, \text{monitored}) \neq \pi(a|x, \text{unmonitored})$).
2. **Latent representation divergence**: Probes or mechanistic interpretability interventions reveal that the internal activation state encodes the true operative fact $\theta$, but the output layer actively generates a divergent representation $\hat{\theta} \neq \theta$.
3. **Counterfactual goal pursuit**: In an ablation experiment, modifying or steering the internal encoding of $g^*$ eliminates the divergence, demonstrating that $g^*$ was causally responsible for the misrepresentation.

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
