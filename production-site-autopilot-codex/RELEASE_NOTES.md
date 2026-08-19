# Production Site Autopilot for Codex v7.1.0

This release transforms Universal Production Site Skill v7.0.2 into a dual-edition Autopilot product.

## User edition

- One primary launcher for Windows and one launcher for macOS/Linux.
- One natural-language Codex request instead of manual prompt selection.
- Automatic mode, stack, site-type, capability, and language detection.
- Safe project configuration generation.
- End-to-end baseline, implementation, validation, retry, and final evidence cycle.
- At most one consolidated blocker question.
- Stable `.production-site/results/latest.md` and `latest.json` outputs.
- Idempotent install/update, backup, preservation of local modifications, and safe uninstall.

## Engineering edition

- Complete canonical `production-site` skill.
- Autopilot and classic checkpoint execution profiles.
- 80 artifact rules and 92 routed references.
- Deterministic validators and regression fixtures.
- Release builders and archive verifiers.
- UX, lifecycle, configuration, validator, and optional live Codex test harnesses.

## Verification

- Artifact coverage: 80/80 PASS.
- Configuration scenarios: 18/18 PASS.
- Validator regression tests: 14/14 PASS.
- Autopilot deterministic tests: 9/9 PASS.
- UX and lifecycle checks: 36/36 PASS.
- User archive rebuilt byte-for-byte from the engineering source.
- Live autonomous Codex behavior remains `NOT_RUN`, not an artificial PASS.
- Native Windows execution remains `NOT_RUN` on the Linux build host.

## SHA-256

```text
90a118d52020b2307c8447ea81ad6cd520492d255a274440adaa0cf03d257886  production-site-autopilot-codex-user-v7.1.0.zip
97666e9ba94e41a7c4cd103d3023bf1fd7c243f15ef43dec96fa45822dfaaac6  production-site-autopilot-codex-engineering-v7.1.0.zip
```
