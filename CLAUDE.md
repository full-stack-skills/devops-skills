# CLAUDE.md

## Project Overview

`devops-skills` is a curated collection of 9 Agent Skills for AI coding agents, part of the [Full Stack Skills](https://github.com/partme-ai/full-stack-skills) ecosystem maintained by [PartMe.AI](https://github.com/partme-ai). Each skill is loaded on demand.

## Skills (9)

| Skill | Domain |
|-------|--------|
| `ansible` | Configuration management — playbooks, roles, inventory, modules |
| `cloudformation` | AWS IaC — templates, stacks, parameters, nested stacks |
| `github-actions` | GitHub CI/CD — workflows, actions, secrets, matrix builds |
| `gitlab-ci` | GitLab CI/CD — pipelines, runners, artifacts, environments |
| `kubernetes` | Container orchestration — pods, deployments, services, ingress |
| `linuxmirrors-awesome` | LinuxMirrors overview, source-backed research, compatibility, and task routing |
| `linuxmirrors-os` | GNU/Linux package mirror switching, validation, troubleshooting, and rollback |
| `linuxmirrors-docker` | Docker Engine installation, Docker CE mirrors, Registry Mirrors, and rollback |
| `terraform` | Multi-cloud IaC — providers, modules, state, workspaces |

## Directory Structure

```
devops-skills/
├── skills/
│   ├── ansible/SKILL.md + LICENSE.txt
│   ├── cloudformation/SKILL.md + LICENSE.txt
│   ├── github-actions/SKILL.md + LICENSE.txt
│   ├── gitlab-ci/SKILL.md + LICENSE.txt
│   ├── kubernetes/SKILL.md + LICENSE.txt
│   ├── linuxmirrors-awesome/SKILL.md + agents/ + references/ + examples/
│   ├── linuxmirrors-os/SKILL.md + agents/ + references/ + examples/
│   ├── linuxmirrors-docker/SKILL.md + agents/ + references/ + examples/
│   └── terraform/SKILL.md + LICENSE.txt
├── .claude-plugin/plugin.json          # Plugin manifest — name, version, skill paths
├── README.md / README.zh-CN.md         # Bilingual project docs
└── LICENSE                             # Apache 2.0
```

## SKILL.md Authoring Conventions

Each `SKILL.md` follows this structure:

1. **YAML frontmatter** — `name`, `description` (English usage guidance), `license` pointer
2. **When to use this skill** — trigger conditions in Chinese (the working language for these skills)
3. **How to use this skill** — core workflow: config format, CLI commands, environment setup
4. **Best Practices** — 3-5 bullet points covering secrets, isolation, formatting
5. **Keywords** — comma-separated tags in both English and Chinese

Rules:
- Keep each SKILL.md under 30 lines — agents load these on-demand, so shorter is better
- Frontmatter `description` is the primary trigger text; make it specific about when to use
- Body content is bilingual: section headers in English, bullet content in Chinese
- Each skill gets its own directory with `SKILL.md` + `LICENSE.txt`
- New skills must be registered in `.claude-plugin/plugin.json` under `skills[]`

### LinuxMirrors skill family exception

The three `linuxmirrors-*` skills use the current Agent Skills progressive-disclosure layout: concise workflow instructions in `SKILL.md`, UI metadata in `agents/openai.yaml`, source-backed detail in `references/`, and end-to-end scenarios in `examples/`. Their `SKILL.md` files may exceed the legacy 30-line limit but must remain below 150 lines; frontmatter contains only `name` and `description`.

## Key Files

| File | Purpose |
|------|---------|
| `.claude-plugin/plugin.json` | Plugin manifest; add new skill paths here |
| `README.md` / `README.zh-CN.md` | Public-facing docs; update skill table on add/remove |
| `skills/<name>/SKILL.md` | The skill itself — the only file agents read |
| `skills/<name>/LICENSE.txt` | Apache 2.0 license copy per skill |
