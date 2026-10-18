# PraxisJr

Cursor plugin for [Specification-Governed Software Engineering](SPEC.md) (SGSE).

Agents act as engineering decision partners. Requirements, options, architecture, and contracts come before application logic. The full methodology is [SPEC.md](SPEC.md).

Guiding principle: build the simplest correct solution that satisfies current requirements while preserving justified paths for future growth.

## Commands

| Command | What it does |
|---|---|
| `/praxisjr` | Classify the change and continue at the current stage. |
| `/praxisjr-decide` | Options, criteria, reviewer, and a proposed decision record. |
| `/praxisjr-scaffold` | Logic-less scaffolding from accepted contracts, then a compliance check. |
| `/praxisjr-audit` | Intent, architecture, and scope drift. |
| `/praxisjr-approve` | Definition of success, then record and documentation updates. |

A typo, format change, rename, or comment that does not change behavior is not a governed change. A defect fix inside an existing contract uses a short change-control path. New behavior, a new boundary, a new dependency, or a new public contract walks all ten stages.

## Stages

1. Requirements
2. Specification
3. Architecture and trade-offs
4. Contracts
5. Logic-less scaffold
6. Structural and specification compliance
7. Application logic
8. Independent verification
9. Intent, architecture, and scope audit
10. Approval, release, and documentation updates

Each stage waits for acceptance. Records go in the project's existing spec home. If the project has none, the plugin proposes `docs/sgse/` and waits before creating it.

## What the plugin loads

| Path | Role |
|---|---|
| `rules/praxisjr.mdc` | Operating constraint. Applies in every session once the plugin is enabled. |
| `skills/` | Stage procedure. The `praxisjr` skill chooses the path and names the next stage. |
| `commands/` | Slash commands above. |
| `agents/praxisjr-reviewer.md` | Challenges a decision that contradicts the specification, and records when a choice beats the baseline. |
| `SPEC.md` | The methodology statement. |

## Install

Cursor loads a local plugin only when the plugin directory itself is under `~/.cursor/plugins/local`. A symlink whose target sits outside that directory is rejected, so the plugin never appears in Customize.

```bash
git clone https://github.com/flyingcoder/sgse-praxis-jr.git ~/.cursor/plugins/local/praxisjr
```

Reload Cursor, then enable **PraxisJr** in plugin settings if `/praxisjr` does not appear.

## License

[MIT](LICENSE)
