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

These are the commands you invoke directly, and the only ones in the `/web-harness:` menu. Everything else this plugin ships is an **internal building block** (orchestrators, Phase steps, companion setups, AI submodes) that is hidden from the menu and read by `/web-harness:wh` for you, so the lane banner and its gates always apply.

| Command | Use it to |
|---|---|
| `/web-harness:wh` | **The single entry point.** Judges the lane and shows it: `/web-harness:wh plan` (planning only, stops at the plan-reviewer readiness gate) · `/web-harness:wh new` (plan → design → dev → QA) · `/web-harness:wh change` (add behaviour) · `/web-harness:wh fix` · `/web-harness:wh verify`. Force a lane by leading with it; plugin skills are always namespaced. |
| `/web-harness:team-flow` | Ticket-based team development — decompose a reviewed plan into WORK items, publish them to GitHub Issues or Jira, pick them up and complete them with PRs. |
| `/web-harness:pr-drafter` | Draft a PR description from the current branch diff. |
| `/web-harness:web-console` | Open the approval-gated local Console for the current project. |
| `/web-harness:project-init` | Scaffold an empty project skeleton only (no planning/QA gates). |
| `/web-harness:version-bump` | Recommend a semantic version bump from the git history and changes. |

First app, cost expectations, and the brownfield path: see the [quickstart](https://github.com/taese83/web-harness/blob/main/docs/quickstart.md).

- Version: 0.49.1
- 22 skills · 42 agents · 5 safety hooks
- Always-on context cost ≈10k tokens/session (plus a few SessionStart re-entry lines only in `_workspace/` harness-managed projects) — disable when idle: `/plugin disable web-harness@web-harness-marketplace`
