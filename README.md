# web-harness plugin marketplace

[web-harness](https://github.com/taese83/web-harness)에서 `node .claude/scripts/build-plugin.mjs`로 생성되는 배포 산출물입니다. 직접 편집하지 마세요.

## 설치

Claude Code에서:

```
/plugin marketplace add https://github.com/taese83/web-harness-plugin
/plugin install web-harness@web-harness-marketplace
```

이후 아무 프로젝트 디렉터리에서 `/web-harness:web-orchestrator`, `/web-harness:web-plan`, `/web-harness:web-console` 등을 사용할 수 있습니다. 로컬 Console(4310)과 격리 프리뷰(4311)는 `web-harness-console` 실행 파일이 현재 프로젝트를 대상으로 구동합니다.

- 버전: 0.1.2
- 스킬 30 · 에이전트 98 · 안전 훅 5종
- always-on 컨텍스트 비용 약 10k tokens/세션 — 사용하지 않을 때는 `/plugin disable web-harness@web-harness-marketplace`
