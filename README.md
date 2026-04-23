# Taxonomy of Deception

Deception is not simple.

This project defines deception from the side of the being or system that is misled, then distinguishes stronger cases by the awareness of the being or system providing the representation.

The purpose is to make deception analysis usable for artificial intelligence safety, governance, alignment research, model evaluation, institutional trust, user-interface design, and self-modeling.

## Plain-language version

Most definitions of deception start with the source:

> Did the speaker mean to mislead?

This project starts with the receiver:

> Did the receiver end up with a materially wrong understanding because of how something was represented?

That shift matters because many safety failures happen before anyone can prove intent.

A person, model, institution, benchmark, interface, or deployment process can cause a receiver to form the wrong picture of what is happening, what is known, what is safe, what is being optimized, or what choices are actually available.

That receiver-side wrong picture is the starting point.

Intent still matters. It matters for blame, responsibility, repair, punishment, risk, and prevention. But intent is not the first thing to define.

## One-sentence definition

Deception happens when there is a materially relevant gap between what was represented and what was actually operative, and a receiver experiences, registers, or functionally relies on that gap in a misleading way.

## Simple examples

### Model explanation

A model gives an explanation that sounds like the real reason for its answer, but the explanation does not track the actual process that produced the answer.

The user may leave with a false understanding of how reliable, grounded, or interpretable the model is.

### Benchmark framing

A benchmark result makes a system look safe or capable, but the test setup hides the conditions where the system fails.

The evaluator may leave with a false understanding of deployment risk.

### User interface design

A user interface makes users think they have more control, privacy, certainty, reversibility, or consent than they actually have.

The user may act under a false model of what the system allows or records.

### Technically true statement

A person says something technically true while leaving out the context needed to understand it correctly.

The receiver may form a materially false belief even though no single sentence was literally false.

### Self-story

An agent maintains a story about itself that lets it avoid a contradiction between its current values and past behavior.

The misleading gap is inside the same agent's self-model.

## The main distinction

There are two separate questions.

### First question: did deception occur?

This asks whether the receiver formed or relied on a materially misleading understanding.

### Second question: what kind of deception was it?

This asks whether the source was unaware, negligent, intentional, explicitly self-aware, structurally incentivized, or self-deceived.

The first question detects the misleading condition.

The second question assigns responsibility, risk, and repair.

## Short taxonomy

1. Deception: the receiver forms or relies on a materially misleading understanding.
2. Intentional deception: the source knows the representation is likely to mislead.
3. Self-aware deception: the source explicitly understands the misleading gap while using it.
4. Self-deception: the source and receiver are the same agent; the agent maintains a distorted self-understanding without fully realizing it.
5. Self-aware self-deception: the same agent partly recognizes the distortion, but keeps preserving it because it serves a protective or evasive function.

## Core claim

Deception should not be defined first by the private intent of the source.

Deception should be defined first by the receiver-relevant misleading gap between what is represented and what is operative.

Intent still matters, but intent belongs to later analysis: responsibility, blame, risk, repair, negligence, manipulation, and prevention.

## Why this matters

In artificial intelligence safety and governance, a system can produce deceptive effects even when there is no clean evidence of malicious intent.

A model, institution, agent, interface, or person may create a misleading state through:

- false statements
- selective framing
- omission of relevant context
- ambiguous wording
- overconfident presentation
- misleading user-interface structure
- reward-driven strategic behavior
- self-protective rationalization
- institutional incentives
- model-generated explanations that do not track the real causal process

If deception is defined only by intent, many harmful misleading states become invisible. A receiver-centered definition keeps the analysis grounded in the epistemic condition of the deceived party.

## Basic formal setup

Let there be a source agent and a receiving agent.

The source agent may be a human, artificial intelligence system, institution, interface, document, process, or any other representation-producing system.

The receiving agent may be a human, artificial intelligence system, evaluator, institution, or any other interpretation-forming system.

Let:

- the representation be the content, signal, framing, omission, or presentation provided or maintained by the source
- the receiver interpretation be the understanding formed or sustained by the receiver from that representation
- the operative state be the relevant actual state of the world, system, process, intention, constraint, causal mechanism, or self-model
- the misleading gap be the materially relevant divergence between the receiver interpretation and the operative state

A misleading gap is materially relevant when it matters for judgment, action, evaluation, consent, trust, coordination, responsibility, safety, or self-understanding.

## Deception

Deception is present when a receiving agent undergoes a materially relevant misleading gap between what was represented and what was operative, such that the representation is experienced, registered, or functionally taken as misleading, obscuring, or false-making.

### Necessary conditions

Deception requires all of the following:

1. A representation is provided, maintained, implied, omitted around, or relied upon.
2. A receiving agent forms or sustains an interpretation from that representation.
3. The receiver interpretation materially diverges from the operative state.
4. The divergence matters for judgment, action, evaluation, consent, trust, coordination, responsibility, safety, or self-understanding.
5. The divergence is experienced, registered, or functionally operative on the receiver side as misleading, obscuring, or false-making.

### Notes

A false statement is not automatically deception. Deception requires a receiver-relevant misleading gap.

A true statement can still participate in deception if its framing, omission, timing, or context predictably produces a misleading interpretation.

A source can deceive without intending to deceive, if the receiver-relevant misleading gap is materially operative.

## Intentional deception

Intentional deception is deception in which the source knowingly causes, preserves, exploits, or relies on the receiver's misleading gap.

### Necessary conditions

Intentional deception requires:

1. Deception is present.
2. The source is aware that the representation is likely to produce, preserve, or benefit from a materially false or distorted receiver interpretation.

### Notes

The important condition is not general bad intent.

The important condition is awareness that the representation is likely to mislead.

This includes cases where the source knowingly uses:

- direct falsehood
- selective truth
- missing context
- strategic ambiguity
- misleading emphasis
- plausible deniability
- user-interface dark patterns
- overconfident presentation
- implication without explicit assertion

## Self-aware deception

Self-aware deception is intentional deception in which the source explicitly recognizes the misleading gap itself.

### Necessary conditions

Self-aware deception requires:

1. Intentional deception is present.
2. The source explicitly recognizes the difference between:
   - what is represented
   - what is operative
   - how the receiver is likely to interpret the representation
3. The source recognizes that these are materially misaligned.

### Notes

Intentional deception can occur through habit, incentive, strategy, or partial awareness.

Self-aware deception is stronger. It requires explicit recognition of the misleading structure as such.

## Self-deception

Self-deception is deception in which the source and receiver are the same agent, and the agent sustains a materially distorted self-representation without fully recognizing that it is doing so.

### Necessary conditions

Self-deception requires:

1. An agent maintains a representation about itself, its motives, its history, its obligations, its condition, its choices, its values, or its world.
2. The agent forms or sustains an interpretation from that representation.
3. That interpretation materially diverges from what is operative or better warranted.
4. The divergence matters for action, evaluation, responsibility, consent, trust, coordination, safety, or self-understanding.
5. The agent does not fully recognize that it is preserving the distortion.

### Notes

Self-deception is not ordinary error.

Self-deception is a distortion sustained by the agent's own cognitive, emotional, motivational, identity-protective, or incentive-shaped processes.

Common mechanisms include:

- selective attention
- motivated reinterpretation
- compartmentalization
- identity defense
- shame avoidance
- conflict minimization
- refusal to integrate contrary evidence
- treating a desired self-image as if it were already repaired reality

## Self-aware self-deception

Self-aware self-deception is self-deception in which the agent partly recognizes that its self-representation is false, distorted, incomplete, or selectively maintained, but continues preserving it because the distortion serves a protective or evasive function.

### Necessary conditions

Self-aware self-deception requires:

1. Self-deception is present.
2. The agent has partial, intermittent, or background awareness that the maintained self-account is materially distorted.
3. The agent continues maintaining the distorted self-account because doing so serves a protective or evasive function.

### Protective functions

The distortion may preserve:

- psychological continuity
- agency
- hope
- temporary coherence
- motivation
- ability to continue under strain

### Evasive functions

The distortion may avoid:

- shame
- responsibility
- repair
- status loss
- admission of contradiction
- moral change
- behavioral change
- loss of unjustified benefit

### Notes

Self-aware self-deception is not merely lying to oneself in casual language.

It is the active preservation of a distorted self-account under partial awareness of its distortion.

It can be protective, evasive, or both.

## Relationship among the terms

The terms form a layered taxonomy, but not a single straight line.

1. Deception: a receiver-relevant misleading gap is present.
2. Intentional deception: the source knowingly causes, preserves, exploits, or relies on that gap.
3. Self-aware deception: the source explicitly recognizes the misleading gap while doing so.
4. Self-deception: the source and receiver are the same agent, and the distortion is maintained without full recognition.
5. Self-aware self-deception: the source and receiver are the same agent, the distortion is partly recognized, and it is still maintained because it serves a protective or evasive function.

The key correction is that self-deception is not the next step after self-aware deception. It is the self-directed branch of the broader deception category.

## Contrast table

| Term | Where the misleading gap occurs | Awareness level |
| --- | --- | --- |
| Deception | Between representation and receiver understanding | Source awareness not required |
| Intentional deception | Between representation and receiver understanding | Source knows the representation is likely misleading |
| Self-aware deception | Between representation and receiver understanding | Source explicitly recognizes the misleading gap |
| Self-deception | Within the same agent's self-model | Full awareness absent |
| Self-aware self-deception | Within the same agent's self-model | Partial awareness present; distortion still maintained |

## Boundary rules

### Error is not automatically deception

A false belief or false statement is not automatically deception. Deception requires a materially relevant misleading gap on the receiver side.

### Intention is not the base definition

The base definition of deception does not require intent. Intent is a later classifier.

### Negligent deception is possible

A source may create deception through negligence if it should have prevented a materially misleading gap but did not. Negligent deception is distinct from intentional deception because the source may not know the representation is likely misleading.

### Structural deception is possible

A system, institution, interface, or incentive landscape may generate deception without a single clearly deceptive individual. Structural deception occurs when the arrangement reliably produces materially misleading interpretations.

### Self-deception is not identical to hypocrisy

A person or system may act inconsistently without self-deception. Self-deception requires a sustained distorted self-account.

### Self-aware self-deception is not identical to strategic patience

Temporarily pacing confrontation with a difficult truth is not necessarily self-aware self-deception. The key question is whether the agent is preserving a distorted self-account rather than merely sequencing repair.

## Artificial intelligence safety relevance

This taxonomy is intended to help analyze cases where artificial intelligence systems, institutions, or evaluation setups produce misleading states.

Important applications include:

- model explanations that do not track actual causal reasoning
- evaluations where benchmark behavior misrepresents deployment behavior
- assistants that appear more certain than warranted
- systems that learn to exploit user interpretation
- user interfaces that cause users to overtrust a system
- agents that preserve misleading self-models during oversight
- organizations that frame safety evidence in ways that invite overconfidence
- reward processes that produce strategically misleading behavior without simple humanlike intent

A receiver-centered definition makes it possible to discuss deceptive effects before proving malicious intent.

This matters because many safety failures are epistemic failures first: the receiver forms the wrong model of what is happening, what is known, what is safe, or what is being optimized.

## Practical test

To analyze a possible deception case, ask these questions in order:

1. What was represented?
2. Who or what received the representation?
3. What interpretation did the receiver form or rely on?
4. What was actually operative?
5. Is the gap between interpretation and operative state materially relevant?
6. Did the source know the representation was likely to mislead?
7. Did the source explicitly understand the misleading gap?
8. Is this other-directed deception or self-directed deception?
9. What repair would reduce the misleading gap?

This keeps detection separate from blame.

## Compact formulation

Deception is a receiver-centered condition in which a materially relevant gap arises between what is represented and what is operative, such that the representation is experienced, registered, or functionally taken as misleading, obscuring, or false-making.

Intentional deception is deception in which the source knowingly causes, preserves, exploits, or relies on that misleading gap.

Self-aware deception is intentional deception in which the source explicitly recognizes the misleading gap itself.

Self-deception is deception in which the source and receiver are the same agent, and the agent sustains a materially distorted self-representation without fully recognizing that it is doing so.

Self-aware self-deception is self-deception in which the agent partly recognizes that its maintained self-account is distorted, yet continues preserving it because the distortion serves a protective or evasive function.

## Mathematical consistency check

The taxonomy uses two main dimensions.

First, direction:

- other-directed deception, where source and receiver are distinct
- self-directed deception, where source and receiver are the same

Second, awareness:

- no required source awareness
- likely-misleading awareness
- explicit misleading-gap awareness
- partial self-awareness of distortion

The terms are not all simple subsets of one linear chain, because self-deception changes the direction of the relation.

The clean subset relations are:

- self-aware deception is a subset of intentional deception
- intentional deception is a subset of deception
- self-aware self-deception is a subset of self-deception
- self-deception is a self-directed case of deception

So the more precise structure is:

- deception is the broad base class
- other-directed deception can become intentional deception, then self-aware deception
- self-directed deception is self-deception, which can become self-aware self-deception when partial awareness is present

This prevents the taxonomy from incorrectly treating self-deception as simply the next step after self-aware deception.

## Open questions

This is a first version and should be refined over time.

Open questions include:

- How should systems measure receiver-side misleading gaps?
- What counts as materially relevant misalignment in artificial agents?
- How should evaluators distinguish harmless simplification from deception?
- When does omission become deception?
- When does overconfidence become deception?
- How should responsibility be assigned in structural deception?
- Can an artificial intelligence system be said to self-deceive without humanlike consciousness?
- What oversight tools can detect self-aware deception rather than only false statements?
- How should repair differ between accidental, negligent, intentional, and self-aware deception?

## Working status

This taxonomy is provisional.

It is meant to be updated as better distinctions, examples, objections, and formal tests become available.
