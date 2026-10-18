---
name: praxisjr-contracts
description: Defines SGSE interfaces, types, signatures, and return contracts after architecture is accepted. Use before PraxisJr scaffolding.
disable-model-invocation: true
---

# Contracts

Read the contract shape in [templates.md](../praxisjr/templates.md). Requirements, specification, and architecture are already accepted. Do not write bodies.

1. For each module boundary, define the interface, protocol, class, or function the architecture named.
2. Type every parameter and every return value. State the error the caller must be able to handle.
3. State dependency injection boundaries: what is passed in, and what the unit must not construct itself.
4. Check each contract against an acceptance criterion. A contract with no criterion is unapproved scope. Remove it or stop and ask.
5. Present the contract record and wait for acceptance.

If a signature needs a new concept the architecture does not have, return to `praxisjr-design` for that decision. Do not hide the concept inside a parameter list.
