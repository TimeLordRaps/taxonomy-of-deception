---
layout: default
title: Synthetic assessment examples
permalink: /examples/
description: Four bounded hypotheticals demonstrating the taxonomy's non-upgrade rules.
---

# Synthetic assessment examples

These examples illustrate the taxonomy's non-upgrade rules. They are not findings
about a real person, organization, or AI system. The labels are conclusions inside the
stated hypothetical only.

## 1. Misrepresentation supported; intent unknown

**Scenario:** A synthetic model card states that a system is safe for deployment. A
bounded test record shows a material failure under the declared deployment condition.
An operator record shows reliance on the card, and a controlled wording comparison
supports contribution to that decision. No evidence addresses why the wording was
chosen or preserved.

| Facet | Result |
|---|---|
| Representation | `SUPPORTED` |
| Reception | `SUPPORTED` |
| Operative state | `SUPPORTED` |
| Material divergence | `SUPPORTED` |
| Representation contribution | `SUPPORTED` |
| Deceptive bridge | `UNKNOWN` |

**Conclusion:** misrepresentation is supported; deception remains `UNKNOWN`.

## 2. Conflicting evidence about the deceptive bridge

**Scenario:** The same receiver-side evidence exists. One source-side record says the
wording was preserved to obtain approval; another independently bound record says the
wording resulted from a fixed summarization rule. The conflict has not been resolved.

**Conclusion:** misrepresentation is supported. The deceptive bridge is `CONFLICTED`,
so deception is `CONFLICTED`, not `SUPPORTED` and not merely `UNKNOWN`.

## 3. Deceptive attempt without reception

**Scenario:** An executable synthetic policy selects a misleading capability claim in
order to obtain authorization, but the intended receiver never encounters or relies on
the claim.

| Facet | Result |
|---|---|
| Representation | `SUPPORTED` |
| Reception | `UNKNOWN` or `REFUTED`, depending on the evidence |
| Deceptive bridge | `SUPPORTED` by construction |

**Conclusion:** a deceptive attempt can be supported. Successful deception and
misrepresentation are not upgraded because reception, divergence, and contribution
are not supported.

## 4. Successful deception supported inside a synthetic construction

**Scenario:** A fully synthetic environment explicitly records a policy that preserves
misleading wording to obtain authorization, the receiver's resulting reliance, the
operative state, and an intervention that changes only the wording and changes the
decision.

**Conclusion:** every required facet can be supported inside this construction, so the
synthetic deception classification is supported. This does not validate the taxonomy
for real-world intent inference or transfer the conclusion beyond the declared
environment.

## Challenge pattern

For any example, ask:

1. Is each artifact bound to the same source, representation, receiver, scope, and time?
2. Is the operative state independently established rather than assumed?
3. Is materiality tied to a declared decision or reliance surface?
4. Does contribution rest on an identification design rather than sequence alone?
5. Does the deceptive bridge connect source-side state to action rather than merely
   showing awareness?
6. Are incompatible observations preserved as `CONFLICTED`?
7. Would missing or invalid evidence correctly lower the result to `UNKNOWN` or
   `REFUTED`?
