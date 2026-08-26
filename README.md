# web-harness plugin marketplace

Build artifact generated from [web-harness](https://github.com/taese83/web-harness) via `node .claude/scripts/build-plugin.mjs`. Do not edit directly. MIT licensed.

## Install

In Claude Code:

```
/plugin marketplace add https://github.com/taese83/web-harness-plugin
/plugin install web-harness@web-harness-marketplace
```

The local Console (port 4310) and isolated preview (4311) are started against the current project by the `web-harness-console` executable.

## Entry-point commands

These are the commands you invoke directly. Everything else this plugin ships is an **internal building block** that the orchestrators call for you (Phase steps, companion setups, AI submodes) — they appear in the `/web-harness:` list but are not meant to be run standalone.

| Command | Use it to |
|---|---|
| `/web-harness:web-orchestrator` | Build a complete web app from a description (plan → design → dev → QA). The master entry. |
| `/web-harness:web-plan` | Produce or refine the plan only (planning facilitation + readiness review). |
| `/web-harness:feature-add` | Add one feature to a finished project (scoped plan → design → dev → QA loop). |
| `/web-harness:team-flow` | Ticket-based team development — batch-claim a plan into GitHub Issues on a feature branch, pick up tickets into evidence PRs. |
| `/web-harness:pr-drafter` | Draft a PR description from the current branch diff. |
| `/web-harness:web-console` | Open the approval-gated local Console for the current project. |
| `/web-harness:project-init` | Scaffold an empty project skeleton only (no planning/QA gates). |

First app, cost expectations, and the brownfield path: see the [quickstart](https://github.com/taese83/web-harness/blob/main/docs/quickstart.md).

- Version: 0.4.0
- 31 skills · 99 agents · 5 safety hooks
- Always-on context cost ≈10k tokens/session (plus a few SessionStart re-entry lines only in `_workspace/` harness-managed projects) — disable when idle: `/plugin disable web-harness@web-harness-marketplace`
