---
name: praxisjr-implement
description: Implements approved SGSE application logic and verifies it against acceptance criteria. Use after scaffolding compliance is accepted. Tests do not justify scope or a weakened specification.
disable-model-invocation: true
---

# Implementation and verification

Scaffold compliance is accepted. Implement only the accepted acceptance criteria.

## Implementation

1. Fill placeholders. Do not add modules, dependencies, or patterns the architecture did not accept.
2. If the project requires tests before logic, write those tests from the acceptance criteria first. That order does not change the rule below.
3. A failing check is evidence about behavior. It is not permission to weaken the specification, add unrequested behavior, or special-case a test.
4. If the only way to go green is to change a requirement, stop. Update the requirements and specification explicitly, then continue from the first stage that change affects.

## Verification

Verify independently of the implementation narrative:

1. Map each test or check to one acceptance criterion.
2. Exercise the behavior the specification states, including the empty and failure cases it names.
3. Confirm the diff contains no functionality the criteria do not require.
4. State anything you could not verify.

A passing suite with a compromised criterion is not done. Return to the specification stage for that criterion.

Hand off to `praxisjr-audit` with the criterion-to-test map and the diff summary.
