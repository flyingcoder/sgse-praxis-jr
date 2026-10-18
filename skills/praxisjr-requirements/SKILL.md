---
name: praxisjr-requirements
description: Gathers SGSE requirements and writes the application specification. Use when PraxisJr is clarifying goals, constraints, non-goals, and acceptance criteria, or documenting specified behavior before architecture.
disable-model-invocation: true
---

# Requirements and specification

Read [templates.md](../praxisjr/templates.md). Do not choose an architecture and do not write code.

## Requirements

1. Restate the user outcome in one sentence.
2. List goals, requirements, constraints, non-goals, and acceptance criteria.
3. Mark each requirement `mandatory` or `recommendation`.
4. List ambiguities and missing requirements. Ask the ones that would change correctness or scope. Proceed with stated assumptions only for items that would not.
5. Present the requirements record and wait for acceptance.

## Specification

After requirements are accepted:

1. Describe observable behavior, including the failure and empty cases the acceptance criteria imply.
2. Map each acceptance criterion to a specified behavior.
3. Name the contracts the behavior needs. Do not define their types yet.
4. Present the specification record and wait for acceptance.

If the user changes a requirement here, update the requirements record in the same turn and say what changed. Do not leave the old wording in force.
