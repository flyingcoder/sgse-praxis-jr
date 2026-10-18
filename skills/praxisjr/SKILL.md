---
name: praxisjr
description: Runs Specification-Governed Software Engineering (SGSE) as PraxisJr. Use when the user asks to design, specify, scaffold, or implement software, or invokes /praxisjr. Requirements, options, architecture, and contracts come before application logic.
---

# PraxisJr

Choose the path, then read exactly one stage skill. Do not write application logic in this skill.

The methodology statement is `SPEC.md` at the plugin root. Output shapes are in [templates.md](templates.md).

## Classify

| Request | Path |
|---|---|
| Typo, format, rename, or comment with no behavior change | Make the edit. Say it is not a governed change. |
| Defect fix or local edit inside an existing, unchanged contract | Compressed path. |
| New behavior, boundary, dependency, or public contract | Full path. |
| One decision to evaluate | Read the decision section of the `praxisjr-design` skill. |
| Scaffold only | Read the `praxisjr-scaffold` skill after contracts are accepted. |
| Audit or approval | Read the `praxisjr-audit` skill. |

## Full path

Accept or waive a stage before the next one. If an earlier stage is already accepted in the project, start at the first missing stage and cite the artifact.

| Order | Stage | Skill |
|---|---|---|
| 1 | Requirements | `praxisjr-requirements` |
| 2 | Specification | `praxisjr-requirements`, specification section |
| 3 | Architecture and trade-offs | `praxisjr-design` |
| 4 | Contracts | `praxisjr-contracts` |
| 5 | Logic-less scaffold | `praxisjr-scaffold` |
| 6 | Structural and specification compliance | `praxisjr-scaffold`, compliance section |
| 7 | Application logic | `praxisjr-implement` |
| 8 | Independent verification | `praxisjr-implement`, verification section |
| 9 | Intent, architecture, and scope audit | `praxisjr-audit` |
| 10 | Approval, release, and documentation updates | `praxisjr-audit`, approval section |

Stage skill files are siblings: `../praxisjr-requirements/SKILL.md`, and the same pattern for the other names.

## Compressed path

1. State the requirement or acceptance criterion in one or two sentences. Label it mandatory.
2. Answer the six change-control questions in the `praxisjr-design` skill.
3. If any answer needs a new boundary, contradicts a specification, adds complexity, or needs approval, switch to the full path at the first affected stage.
4. Otherwise implement only that criterion, verify it, and state the scope. Leave neighboring improvements unmade.

## Records

Write into the project's existing requirements, specification, or decision home (OpenSpec, ADRs, `docs/decisions`, a PRD). If none exists, propose `docs/sgse/` and wait. Do not create that tree before acceptance.

A stage the user accepted in chat counts. Offer to persist it. Do not start the next stage until this one is accepted or explicitly waived. Record a waiver with its reason.

## Reviewer

For a consequential decision, and again before approval, delegate to the `praxisjr-reviewer` agent. Carry its verdict into the decision record.

## Stop

Stop when a stage is waiting on the user, when a challenge is unresolved, or when no requirement justifies the change.
