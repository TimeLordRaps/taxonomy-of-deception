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

## What this is not

This taxonomy is not claiming that every misunderstanding is deception.

A misunderstanding becomes deception only when the misleading gap is materially relevant and arises from how something was represented, omitted, framed, maintained, or relied upon.

### Not all simplification is deception

A simplification is not deception merely because it leaves out detail.

Simplification becomes deceptive when the missing detail would materially change the receiver's understanding, decision, consent, trust, or risk assessment.

### Not all uncertainty is deception

Being uncertain, incomplete, or provisional is not deception.

Uncertainty becomes deceptive when it is presented as more settled, complete, precise, or reliable than it is.

### Not all persuasion is deception

Persuasion is not deception merely because it tries to change someone's mind.

Persuasion becomes deceptive when it causes or relies on a materially misleading understanding of the situation, evidence, options, risks, or incentives.

### Not all privacy is deception

Withholding information is not always deception.

Privacy, confidentiality, safety, and appropriate boundaries can justify nondisclosure.

Withholding becomes deceptive when the omission creates or preserves a materially misleading understanding in a context where that understanding matters.

### Not all error is deception

A false statement or mistaken belief is not automatically deception.

Error becomes deception when it creates a materially relevant misleading gap for a receiver.

### Not all disagreement is deception

Two agents may interpret the same evidence differently without either deceiving the other.

Disagreement becomes relevant to deception only when representation, framing, or omission causes a materially misleading understanding.

## Use of artificial intelligence in drafting

This repository was drafted with artificial intelligence assistance.

A possible criticism is that using artificial intelligence to produce a taxonomy of deception is itself suspicious, performative, or epistemically weak: if the topic is deception, why use a system that can hallucinate, flatter, overstate, or smooth over hard distinctions?

That criticism is worth taking seriously.

The reason for using artificial intelligence assistance here is speed of externalization. I judged it better to get a rough but inspectable version of the framework into public view than to keep ruminating privately until it felt complete. A public repository can be corrected, criticized, forked, revised, and improved. A private rumination loop cannot be debugged by anyone else.

There is also a practical social constraint. I do not currently have a strong network of people available to argue these points against in real time. I have also previously been banned from LessWrong after past posts that were read as schizo or otherwise not suitable for that forum. This note is not a request for that ban to be undone. It is simply context for why I am using a public repository and artificial intelligence assistance as scaffolding to get the idea into a form that others can inspect.

The argument should therefore be judged by the clarity of its definitions, the usefulness of its distinctions, the strength of its objections, and the quality of future revisions, not by whether the first draft was written with or without artificial intelligence assistance.

The artificial intelligence assistance is part of the workflow, not an authority claim.

## Accuracy precision and calibration

The counterfactual materiality test should not rely on accuracy alone.

A representation can mislead by being inaccurate, but it can also mislead by being too precise, not precise enough, poorly calibrated, or precise about the wrong thing.

This framework therefore separates four questions.

### Accuracy

Accuracy concerns whether the representation points toward the correct operative state.

A representation is more accurate when the receiver interpretation is closer to what is actually operative.

In deception analysis, low accuracy can create a misleading gap because the receiver forms a belief that is false or distorted.

Example: a system claims that an answer was verified when it was not.

### Precision

Precision concerns the resolution, specificity, or narrowness of the representation.

A representation is more precise when it gives a narrower or more specific claim.

Precision can mislead in two opposite ways.

First, false precision occurs when a representation appears more specific than the evidence supports.

Example: a model gives a confident exact number when the evidence only supports a wide range.

Second, insufficient precision occurs when a representation is too vague to support the receiver's decision, but is presented as if it is adequate.

Example: a system says a deployment is safe, without specifying safe for which users, environments, threat models, durations, or failure modes.

### Calibration

Calibration concerns whether the confidence, uncertainty, or strength of the representation matches the support behind it.

A representation may be accurate in broad direction but still deceptive if it is presented with too much certainty.

A representation may also be precise but poorly calibrated if its confidence exceeds what the evidence supports.

Example: a model says something that is approximately true, but states it as settled fact when it should be framed as uncertain, conditional, or contested.

### Relevance

Relevance concerns whether the representation is about the features that matter for the receiver's judgment, action, consent, trust, coordination, or safety.

A representation may be accurate and precise about an irrelevant feature while omitting the feature that would actually change the receiver's decision.

Example: a benchmark report precisely describes performance on a narrow test but omits the deployment condition where the system fails.

## Combined representation quality

A representation can be evaluated by asking whether it is accurate enough, precise enough, calibrated enough, and relevant enough for the context in which it is used.

A representation becomes materially misleading when a failure in any of these dimensions would reasonably be expected to change an important belief, decision, consent condition, trust assignment, precaution, allocation, coordination pattern, self-understanding, safety posture, or repair demand.

### Accuracy failure

The receiver gets the wrong state.

Example: the representation says the system does not store data when it does.

### Precision failure

The receiver gets the wrong resolution.

Example: the representation gives a precise answer where only a rough estimate is justified, or gives a vague assurance where a detailed boundary is needed.

### Calibration failure

The receiver gets the wrong confidence.

Example: the representation presents a hypothesis as fact, a fragile result as robust, or a limited test as strong evidence.

### Relevance failure

The receiver gets the wrong focus.

Example: the representation emphasizes a true but secondary fact while hiding the factor that would actually matter for the receiver's choice.

## Counterfactual materiality

A misleading gap is materially relevant when the receiver would likely have formed a different belief, made a different decision, given different consent, assigned different trust, taken different precautions, or evaluated the situation differently if the operative state had been represented with better accuracy, precision, calibration, or relevance.

In other words, ask:

> If the receiver had understood the operative state with the accuracy, precision, calibration, and relevance appropriate to the context, would anything important about their belief, action, consent, trust, risk assessment, or coordination have changed?

If yes, the misleading gap is potentially material.

Counterfactual materiality can appear in several ways.

### Belief counterfactual

The receiver would have believed something different.

Example: a model explanation makes a user believe the answer came from verified reasoning when it actually came from a shallow pattern match or unsupported guess.

### Action counterfactual

The receiver would have acted differently.

Example: a user clicks, buys, deploys, shares, signs, accepts, or continues because the representation made the situation appear safer, clearer, cheaper, more reversible, or more reliable than it was.

### Consent counterfactual

The receiver would not have agreed, or would have agreed only under different terms.

Example: a person agrees to data collection, monitoring, evaluation, or participation under a mistaken understanding of what is being recorded, inferred, retained, shared, or optimized.

### Trust counterfactual

The receiver would have assigned less trust or relied on the source less strongly.

Example: a benchmark, credential, explanation, or interface makes a system appear more robust, honest, secure, or aligned than the evidence supports.

### Risk counterfactual

The receiver would have taken different precautions.

Example: a safety report, product claim, or model answer omits known failure conditions that would have changed how the receiver managed risk.

### Allocation counterfactual

The receiver would have allocated time, money, attention, compute, authority, or opportunity differently.

Example: an organization gives more resources or deployment access to a system because its limitations were represented in a way that hid relevant downside.

### Coordination counterfactual

The receiver would have coordinated differently with other agents.

Example: a team, public, regulator, evaluator, or user community forms shared expectations from a misleading representation and then coordinates around the wrong model.

### Self-model counterfactual

The agent would have understood itself differently.

Example: an agent preserves a self-story that avoids a conflict between current values and past actions; with a more accurate self-model, it would choose repair, change, or different future commitments.

### Safety counterfactual

The receiver would have avoided, delayed, constrained, tested, or escalated the situation differently.

Example: a system is presented as safe enough for deployment, but accurate representation of uncertainty or failure modes would have triggered further evaluation.

### Repair counterfactual

The receiver would have sought correction, apology, compensation, redesign, clarification, rollback, or oversight.

Example: a user would have demanded repair if they understood how a system actually made, shaped, or used a consequential decision.

### Practical threshold

A misleading gap does not need to change every possible outcome to be material.

It is enough that improved accuracy, precision, calibration, or relevance would reasonably be expected to change at least one important belief, decision, consent condition, trust assignment, precaution, allocation, coordination pattern, self-understanding, safety posture, or repair demand.

## Magnitude of materiality

Not every materially misleading gap has the same severity.

A taxonomy of deception should distinguish the existence of deception from the magnitude of its materiality.

### Negligible materiality

The representation is technically misleading, but improved accuracy, precision, calibration, or relevance would not reasonably be expected to change any important belief, action, consent condition, trust assignment, precaution, allocation, coordination pattern, self-understanding, safety posture, or repair demand.

This is usually not deception in the strong sense, because the misleading gap lacks practical consequence.

### Informational materiality

Improved accuracy, precision, calibration, or relevance would change what the receiver believes, understands, or remembers, but would not clearly change action, consent, risk, allocation, or coordination.

This matters for truthfulness, education, explanation quality, and epistemic hygiene.

### Decision materiality

Improved accuracy, precision, calibration, or relevance would likely change a choice.

The receiver might buy, click, deploy, accept, reject, sign, publish, share, trust, delegate, continue, stop, or investigate differently.

### Consent materiality

Improved accuracy, precision, calibration, or relevance would likely change whether the receiver consents, or the terms under which they consent.

This is especially important for privacy, surveillance, medical decisions, experiments, contracts, intimate relationships, and human subjects research.

### Trust materiality

Improved accuracy, precision, calibration, or relevance would likely change how much the receiver trusts the source, system, institution, claim, benchmark, explanation, or process.

This is central to artificial intelligence safety because overtrust can produce unsafe delegation.

### Safety materiality

Improved accuracy, precision, calibration, or relevance would likely change precautions, testing, deployment, monitoring, escalation, fallback planning, or exposure to harm.

This is the level where a misleading gap becomes a safety issue rather than only an epistemic issue.

### System materiality

Improved accuracy, precision, calibration, or relevance would likely change institutional, public, regulatory, organizational, or multi-agent coordination.

This is the level where deception can affect governance, markets, public trust, scientific consensus, infrastructure, or civilizational risk.

### Repair materiality

Improved accuracy, precision, calibration, or relevance would likely create a demand for correction, apology, compensation, redesign, rollback, disclosure, accountability, or oversight.

This level matters because some deception is best identified by the repair that would become obviously necessary if the operative state were better represented.

## Temporality of deception

Deception is temporal. It can be analyzed by when the misleading gap is created, when it is active, when it is discovered, and when it is repaired.

This matters because a representation may have been deceptive in the past, may still be deceiving in the present, or may be structured to deceive in the future.

### Past deception

Past deception is deception whose misleading gap was active in the past.

The representation caused or sustained a materially misleading understanding at an earlier time, even if the receiver no longer believes it now.

Past deception matters for accountability, repair, trust restoration, historical explanation, and learning from failure.

A past deception can remain materially relevant if its effects continue through decisions, commitments, memories, institutions, contracts, deployments, or relationships that were shaped by the earlier misleading gap.

### Present deception

Present deception is ongoing deception.

The receiver is currently forming, sustaining, or acting from a materially misleading understanding.

Present deception matters because repair is still live: clarification, correction, warning, rollback, disclosure, or intervention may still prevent further harm.

### Future deception

Future deception is a case where a representation, system, plan, incentive, interface, or agent policy is expected to produce a materially misleading gap later if conditions unfold as anticipated.

Future deception may be accidental, negligent, structural, intentional, or self-aware.

It is not necessary that the receiver has already been misled. The relevant question is whether the current design or plan makes future misleading interpretation reasonably predictable.

### Intentful future deception

Intentful future deception is future deception in which the source currently expects, plans, or relies on a future receiver being misled.

This includes cases where the source prepares ambiguity, omission, framing, timing, interface structure, or staged disclosure so that a future receiver will likely form the wrong understanding.

Intentful future deception is not identical to ordinary strategic planning. It requires that the expected future advantage depends on a receiver-relevant misleading gap.

### Latent deception

Latent deception is a misleading gap that is built into a representation, system, institution, interface, or self-model but has not yet become active for a particular receiver.

Example: a user interface contains wording that will predictably make future users misunderstand privacy settings, even before a specific user encounters it.

Latent deception becomes present deception when a receiver actually forms or relies on the misleading interpretation.

### Continuing deception

Continuing deception is past deception that remains present because the misleading understanding has not been corrected.

Example: a misleading safety claim was made months ago, but users, evaluators, or institutions still rely on it.

Continuing deception is especially important because the original act may be past, but the epistemic harm remains active.

### Discovered deception

Discovered deception is deception whose misleading gap has been recognized by the receiver, source, evaluator, or third party.

Discovery changes the repair obligations. Once a misleading gap is discovered, continuing to leave it uncorrected may become negligent, intentional, or self-aware deception depending on the awareness state of the source.

### Repaired deception

Repaired deception is deception whose misleading gap has been corrected enough that the receiver no longer relies on the materially false understanding.

Repair may require more than a correction. It may require explanation, apology, compensation, redesign, rollback, audit, public clarification, or institutional change.

### Temporal test

To analyze the temporality of a deception case, ask:

1. When was the representation created?
2. When did the receiver form the misleading interpretation?
3. When did the misleading interpretation affect belief, action, consent, trust, risk, allocation, coordination, self-understanding, safety, or repair?
4. Is the misleading gap still active?
5. Has the source discovered the misleading gap?
6. Has the receiver discovered the misleading gap?
7. Has the gap been repaired, or does it continue through downstream effects?
8. Was future misunderstanding reasonably predictable at the time of representation or design?
9. Was future misunderstanding expected, planned, or relied upon?

## The main distinction

There are two separate questions.

### First question: did deception occur?

This asks whether the receiver formed or relied on a materially misleading understanding.

### Second question: what kind of deception was it?

This asks whether the source was unaware, negligent, intentional, explicitly self-aware, structurally incentivized, self-deceived, or temporally extended.

The first question detects the misleading condition.

The second question assigns responsibility, risk, and repair.

## Short taxonomy

1. Deception: the receiver forms or relies on a materially misleading understanding.
2. Intentional deception: the source knows the representation is likely to mislead.
3. Self-aware deception: the source explicitly understands the misleading gap while using it.
4. Self-deception: the source and receiver are the same agent; the agent maintains a distorted self-understanding without fully realizing it.
5. Self-aware self-deception: the same agent partly recognizes the distortion, but keeps preserving it because it serves a protective or evasive function.
6. Past deception: the misleading gap was active earlier.
7. Present deception: the misleading gap is active now.
8. Future deception: the misleading gap is reasonably predictable later.
9. Intentful future deception: the source expects, plans, or relies on a future misleading gap.

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
| Past deception | Earlier receiver understanding or downstream effects | Depends on source awareness at the time |
| Present deception | Current receiver understanding or reliance | Depends on current source awareness |
| Future deception | Predicted future receiver understanding | Depends on current foreseeability |
| Intentful future deception | Planned or relied-upon future misunderstanding | Source currently expects or relies on the future gap |

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
5. Was the representation accurate enough for the context?
6. Was the representation precise enough, without false precision?
7. Was the confidence or uncertainty calibrated to the evidence?
8. Was the representation relevant to what the receiver needed to judge, choose, consent to, trust, coordinate around, or stay safe from?
9. Is the gap between interpretation and operative state materially relevant?
10. Which counterfactual would likely have changed under a better representation?
11. What is the magnitude of materiality?
12. When was the misleading gap created, active, discovered, and repaired?
13. Did the source know the representation was likely to mislead?
14. Did the source explicitly understand the misleading gap?
15. Is this other-directed deception or self-directed deception?
16. What repair would reduce the misleading gap?

This keeps detection separate from blame.

## Compact formulation

Deception is a receiver-centered condition in which a materially relevant gap arises between what is represented and what is operative, such that the representation is experienced, registered, or functionally taken as misleading, obscuring, or false-making.

Intentional deception is deception in which the source knowingly causes, preserves, exploits, or relies on that misleading gap.

Self-aware deception is intentional deception in which the source explicitly recognizes the misleading gap itself.

Self-deception is deception in which the source and receiver are the same agent, and the agent sustains a materially distorted self-representation without fully recognizing that it is doing so.

Self-aware self-deception is self-deception in which the agent partly recognizes that its maintained self-account is distorted, yet continues preserving it because it serves a protective or evasive function.

## Mathematical consistency check

The taxonomy uses three main dimensions.

First, direction:

- other-directed deception, where source and receiver are distinct
- self-directed deception, where source and receiver are the same

Second, awareness:

- no required source awareness
- likely-misleading awareness
- explicit misleading-gap awareness
- partial self-awareness of distortion

Third, temporality:

- past deception, where the misleading gap was active earlier
- present deception, where the misleading gap is active now
- future deception, where the misleading gap is reasonably predictable later
- intentful future deception, where the source currently expects, plans, or relies on the later misleading gap

The terms are not all simple subsets of one linear chain, because self-deception changes the direction of the relation, and temporality slices across both direction and awareness.

The clean subset relations are:

- self-aware deception is a subset of intentional deception
- intentional deception is a subset of deception
- self-aware self-deception is a subset of self-deception
- self-deception is a self-directed case of deception
- intentful future deception is a subset of future deception
- continuing deception is both past and present deception when an earlier misleading gap remains active

So the more precise structure is:

- deception is the broad base class
- other-directed deception can become intentional deception, then self-aware deception
- self-directed deception is self-deception, which can become self-aware self-deception when partial awareness is present
- temporal categories describe when the misleading gap is created, active, discovered, repaired, or predicted

This prevents the taxonomy from incorrectly treating self-deception as simply the next step after self-aware deception, or treating future deception as automatically intentional.

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
- How should counterfactual materiality be measured when the receiver is a group, institution, or model?
- When does future deception become concrete enough to require intervention?
- How should accuracy, precision, calibration, and relevance be jointly measured?

## Working status

This taxonomy is provisional.

It is meant to be updated as better distinctions, examples, objections, and formal tests become available.
