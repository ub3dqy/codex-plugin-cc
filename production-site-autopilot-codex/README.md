# Production Site Autopilot for Codex v7.1.0

Production Site Autopilot turns one repository-level request into a complete production-site checkpoint: project detection, safe mode selection, baseline capture, implementation, deterministic validation, regression checks, and one concise result.

## Download

### User edition

For everyday use. One launcher installs or updates the skill and starts Codex with the prepared Autopilot task.

[Download `production-site-autopilot-codex-user-v7.1.0.zip`](https://github.com/ub3dqy/codex-plugin-cc/releases/download/production-site-autopilot-v7.1.0/production-site-autopilot-codex-user-v7.1.0.zip)

Windows:

1. Extract the ZIP.
2. Run `START_SITE_AUTOPILOT_WINDOWS.cmd`.
3. Choose the website or project directory.

macOS / Linux:

```bash
./START_SITE_AUTOPILOT_MAC_LINUX.sh
```

After installation, open any project in Codex and write:

```text
Создай или доведи этот сайт до production. Сам всё проанализируй, исправь и проверь.
```

### Engineering edition

For maintaining contracts, routing, validators, installers, tests, evals, and reproducible releases.

[Download `production-site-autopilot-codex-engineering-v7.1.0.zip`](https://github.com/ub3dqy/codex-plugin-cc/releases/download/production-site-autopilot-v7.1.0/production-site-autopilot-codex-engineering-v7.1.0.zip)

The complete browsable engineering source is published in the [`production-site-autopilot-v7.1.0-source`](https://github.com/ub3dqy/codex-plugin-cc/tree/production-site-autopilot-v7.1.0-source) branch.

## Checksums

```text
90a118d52020b2307c8447ea81ad6cd520492d255a274440adaa0cf03d257886  production-site-autopilot-codex-user-v7.1.0.zip
97666e9ba94e41a7c4cd103d3023bf1fd7c243f15ef43dec96fa45822dfaaac6  production-site-autopilot-codex-engineering-v7.1.0.zip
```

## What the user edition does

The user no longer has to copy a long prompt, create YAML before the first run, choose an internal mode, select an entrypoint, run validators manually, or send a new prompt after each checkpoint.

The default path is:

```text
Unpack
  → run one START file
  → choose the project directory
  → Codex performs the safe end-to-end pass
  → latest.md + latest.json + concise chat result
```

Autopilot automatically detects Greenfield, Adoption, Audit-only, Redesign, or Migration mode. It applies reversible high-confidence changes, retries failed checks, and combines genuinely consequential decisions into at most one blocker question.

Detailed output is written to:

```text
.production-site/results/latest.md
.production-site/results/latest.json
```

## Safety boundaries

Without an explicit owner decision, Autopilot does not:

- change URLs, domains, or the primary technology stack;
- delete pages or data;
- publish unverified public claims;
- enable analytics or tracking;
- purchase paid services;
- push changes or deploy to production.

Missing external services or tools are marked `DEFERRED`; they do not block independent safe work.

## Validation status

- Artifact coverage: 80/80 PASS.
- Reference routes: 92.
- Configuration scenarios: 18/18 PASS.
- Validator regressions: 14/14 PASS.
- Autopilot deterministic fixtures: 9/9 PASS.
- UX and lifecycle checks: 36/36 PASS.
- User ZIP reproducibility: byte-for-byte PASS.
- Live autonomous Codex behavior: `NOT_RUN` in the original build environment.
- Native Windows runtime execution: `NOT_RUN` on the Linux build host; the PowerShell contract was checked statically and the cross-platform lifecycle equivalent passed.

The workflow in this repository reconstructs the engineering package, verifies its SHA-256, reruns deterministic checks, rebuilds the user package, confirms the expected byte-identical hash, publishes the full source branch, and creates the GitHub Release.

## License status

Public repository access does not itself grant reuse rights. See [`LICENSE.md`](./LICENSE.md).
