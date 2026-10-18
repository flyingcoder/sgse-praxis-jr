# PraxisJr records

Use the project's existing spec home. Proposed default when none exists and the user accepts it: `docs/sgse/`.

## Requirements

```markdown
# Requirements: <name>

## Goals
## Requirements
- [mandatory] ...
- [recommendation] ...
## Constraints
## Non-goals
## Acceptance criteria
- [ ] ...
## Ambiguities
- ... or none
## Trace
- Specification:
- Decisions:
- Contracts:
- Tests:
```

## Specification

```markdown
# Specification: <name>

## Behavior
What the system does when the requirements hold.

## Out of scope
## Contracts expected
Names only. Definitions live in the contract record.

## Acceptance mapping
| Criterion | Specified behavior |
|---|---|
```

## Decision

```markdown
# ADR-<NNN>: <title>

## Status
proposed | accepted | superseded by ADR-<NNN>

## Context
## Options
### Option A
- Advantages
- Disadvantages
- Trade-offs
- Risks
- Expected impact
### Option B
...

## Decision
## Consequences
## Criteria
| Criterion | Assessment |
|---|---|
| Correctness | Satisfies requirements and contracts. |
| Simplicity | Minimizes unnecessary concepts and complexity. |
| Efficiency | Uses appropriate time, memory, and resources. |
| Maintainability | Supports understandable, testable changes. |
| Extensibility | Supports justified future evolution. |
| Consistency | Aligns with specifications and established standards. |
| Risk | Minimizes technical debt and unintended consequences. |

Assumptions:
Weights, if used: <assumption>. Scores compare options under those assumptions. They are not objective truth.

## Review
agree | challenge | clarify — <one sentence from praxisjr-reviewer>
```

## Change control

Answer before a significant change:

1. Does it satisfy an established requirement?
2. Does it contradict an existing specification or decision?
3. Does it introduce unnecessary complexity?
4. Does it improve the current design measurably?
5. Does it create future constraints or migration costs?
6. Does it require approval or a specification update?

## Contract

```markdown
# Contracts: <name>

## Boundaries
## Dependencies
## <module or type>
- Kind: class | interface | protocol | function | module
- Signature:
- Parameters:
- Returns:
- Errors:
- Must not contain business logic until implementation is approved.
```

## Scaffold compliance

- Every accepted contract has a file and a signature.
- Bodies are placeholders (`NotImplementedError`, `unimplemented`, or an empty protocol). No business logic.
- Test placeholders name an acceptance criterion and do not assert a finished behavior.
- Patterns present were selected in the architecture. No extra pattern was applied "because it is standard."
- Dependencies match the architecture.

## Definition of success

- [ ] Satisfies approved requirements.
- [ ] Follows the documented architecture and contracts.
- [ ] Contains no unjustified functionality or complexity.
- [ ] Passes meaningful tests without compromising intent.
- [ ] Remains understandable and maintainable.
- [ ] Accommodates plausible growth through justified design decisions.
- [ ] Provides traceable reasoning for significant engineering choices.
