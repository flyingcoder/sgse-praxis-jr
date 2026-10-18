---
name: praxisjr-design
description: Evaluates SGSE architecture options and records the decision. Use when PraxisJr is choosing modules, boundaries, and dependencies, or when the user invokes /praxisjr-decide.
disable-model-invocation: true
---

# Architecture and decisions

Read [templates.md](../praxisjr/templates.md). Do not generate files and do not define full signatures. That is the contracts stage.

## When a decision is consequential

A decision is consequential when it adds a boundary, a dependency, a public contract, or a pattern, or when reversing it later has migration cost. A local name or private helper is not consequential.

## Options

For each consequential decision, present at least two viable options. For each option state advantages, disadvantages, trade-offs, risks, and expected impact. Include the smallest option that meets the accepted requirements.

Evaluate every option on correctness, simplicity, efficiency, maintainability, extensibility, consistency, and risk. Use weights only when they clarify a comparison. Write the assumptions beside any numbers. Do not treat a score as objective truth.

Prefer the simplest option that meets current requirements and leaves a justified path for growth the requirements already make plausible. Reject a speculative abstraction.

## Change control

Answer these before recommending implementation:

1. Does it satisfy an established requirement?
2. Does it contradict an existing specification or decision?
3. Does it introduce unnecessary complexity?
4. Does it improve the current design measurably?
5. Does it create future constraints or migration costs?
6. Does it require approval or a specification update?

## Review

Delegate the recommended option to the `praxisjr-reviewer` agent. If the verdict is `challenge` or `clarify`, stop and present that finding. If the verdict is `agree`, record which criterion beat which alternative.

## Record

Write the decision record with status `proposed`. Wait for acceptance before status becomes `accepted`. Name modules, boundaries, dependencies, and the patterns this architecture actually selects. Patterns not selected are out.
