---
name: praxisjr-audit
description: Audits an SGSE change for intent, architecture, and scope drift, then applies the definition of success before approval. Use when the user invokes /praxisjr-audit or /praxisjr-approve.
disable-model-invocation: true
---

# Audit and approval

Read the definition of success in [templates.md](../praxisjr/templates.md).

## Audit

Compare the diff with the accepted requirements, specification, architecture, and contracts.

Report:

- Criteria satisfied, and criteria with no evidence.
- Behavior in the diff that no criterion requires.
- Boundaries, dependencies, or patterns that were not accepted.
- Requirements that changed during implementation and whether their records changed with them.
- Tests that pass by narrowing a criterion.

Delegate to the `praxisjr-reviewer` agent with that report. A `challenge` or `clarify` verdict blocks approval.

## Approval

When the audit is clear, walk the definition of success. Each unmet item blocks release.

On approval:

1. Mark accepted decisions `accepted`.
2. Update the trace links among requirements, decisions, contracts, and tests.
3. Update user-facing or project documentation the change made stale.
4. State residual risks and waived items with their reasons.

Do not approve by noting that the tests passed.
