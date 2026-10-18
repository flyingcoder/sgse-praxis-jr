---
name: praxisjr-scaffold
description: Generates logic-less SGSE scaffolding from accepted contracts and checks structural compliance. Use when the user invokes /praxisjr-scaffold or PraxisJr reaches scaffolding.
disable-model-invocation: true
---

# Scaffold and compliance

Contracts are accepted. Read the compliance list in [templates.md](../praxisjr/templates.md).

## Scaffold

Create only structure:

- Directories and files.
- Classes, interfaces, protocols, and modules.
- Function and method signatures.
- Typed parameters and return contracts.
- Dependency injection boundaries.
- Documentation and test placeholders.
- Configuration and integration boundaries.

Bodies are placeholders. No business logic, no speculative helper, no unapproved scope.

Follow the project's conventions and the language's ordinary idiom. Apply OOP, FP, SOLID, or MVP only when the accepted architecture selected that pattern.

Test placeholders name the acceptance criterion they will cover. They do not assert a finished behavior and they are not a green suite.

## Compliance

Before calling the scaffold valid, check:

- Every accepted contract has a file and a signature.
- No body implements behavior.
- Every pattern in the tree was selected.
- Dependencies match the architecture.
- Names match project standards.

Report gaps as a list. Fix structural gaps. If a gap means the contract or the architecture is wrong, stop and name the stage to reopen. Do not paper over it with logic.

Wait for acceptance before implementation.
