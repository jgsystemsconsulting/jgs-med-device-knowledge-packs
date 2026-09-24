<!--
Copyright (c) 2026 JG Systems Consulting Ltd. - MIT License (see LICENSE).
SPDX-License-Identifier: MIT
-->

<h1 align="center">jgs-med-device-knowledge-packs</h1>

<p align="center">
  <img src="https://img.shields.io/badge/license-MIT%20(tooling)-blue" alt="License: MIT (tooling)">
  <img src="https://img.shields.io/badge/version-0.1.0-green" alt="Version 0.1.0">
</p>

<p align="center">
  <strong>An installable catalogue of knowledge-pack skills for coding agents that
  build medical device software. The fda-med-device pack distills 13 FDA sources
  into reference notes covering FDA device-software guidance, computer system
  validation, the Quality Management System Regulation (QMSR), cybersecurity, and
  premarket submissions; the /med orchestrator routes free-text sector questions to
  the right pack. This catalogue provides engineering knowledge, not legal or
  regulatory advice; EU/UK guidance packs are forthcoming.</strong>
</p>

**Copyright (c) 2026 JG Systems Consulting Ltd. - MIT License (tooling); pack content under each source's own licence (see [NOTICE](NOTICE)).**

---

## What it is

This repo is an installable catalogue of knowledge-pack skills for coding agents
that build medical device software. Each pack distills vetted public sources into
reference notes an agent can load on demand, and a single orchestrator routes
free-text sector questions to the right pack. Pack structure follows
[docs/PACK-SPEC.md](docs/PACK-SPEC.md); usage guidance for agents is in
[docs/skill-usage.md](docs/skill-usage.md).

## Install

Preview what would be installed and where, then install:

```bash
python install.py --dry-run
python install.py
```

`install.py` targets Claude by default. Use `--agent <name>` for another supported
agent or `--agent all`, and `--list-agents` to see every target. Transform-style
agents get the SKILL.md index inlined into a single file (see the note in
`install.py --help`).

## Use

- `/med <question>`: the orchestrator. Ask in free text; it routes to the right
  pack.
- `/fda-med-device`: the pack skill, loaded directly when you already know you
  need it.
- Packs are plain Markdown skills: open any `packs/<slug>/SKILL.md` to read the
  reference notes without installing anything.

## Gates

Run all three from the repo root:

```bash
python tooling/validate_pack.py --all   # every pack matches docs/PACK-SPEC.md
python tooling/check_release.py         # release readiness: files, versions, leaks, links, index, headers
python tooling/test_ci_gate.py          # proves CI (.github/workflows/validate.yml) checks the same things
```

CI green is not release-ready: `check_release.py` is the pre-tag gate. It prints a
`RELEASE CHECK: PASS (v<version> @ <sha>)` receipt; run it before tagging and confirm
the sha matches the commit you tag. The repo is release-ready only when all three
gates exit 0.

## Licence

Two separable layers:

- **Tooling and scaffolding:** [MIT](LICENSE) (JG Systems Consulting Ltd.).
- **Pack content:** each pack carries its source's own licence, declared in
  `packs/<slug>/LICENSE` and `packs/<slug>/PACK.yaml`, independent of the repo's MIT
  licence. Attributions live in [NOTICE](NOTICE); the model is set out in
  [docs/LICENSING.md](docs/LICENSING.md).
