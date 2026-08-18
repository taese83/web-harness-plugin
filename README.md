# web-harness plugin marketplace

Build artifact generated from [web-harness](https://github.com/taese83/web-harness) via `node .claude/scripts/build-plugin.mjs`. Do not edit directly. MIT licensed.

## Install

In Claude Code:

```
/plugin marketplace add https://github.com/taese83/web-harness-plugin
/plugin install web-harness@web-harness-marketplace
```

Then use `/web-harness:web-orchestrator`, `/web-harness:web-plan`, `/web-harness:web-console`, and more from any project directory. The local Console (port 4310) and isolated preview (4311) are started against the current project by the `web-harness-console` executable.

First app, cost expectations, and the brownfield path: see the [quickstart](https://github.com/taese83/web-harness/blob/main/docs/quickstart.md).

- Version: 0.1.2
- 30 skills · 98 agents · 5 safety hooks
- Always-on context cost ≈10k tokens/session (plus a few SessionStart re-entry lines only in `_workspace/` harness-managed projects) — disable when idle: `/plugin disable web-harness@web-harness-marketplace`
