# Codex — Agent Skills

Agent skills for [OpenAI Codex CLI](https://github.com/openai/codex), the AI coding agent for automated engineering tasks. Codex supports custom instructions via `AGENTS.md` files placed at the root of your project, or passed directly via the `--instructions` flag.

## How It Works

Codex reads `AGENTS.md` at the project root (and in subdirectories) to understand the context and instructions for the current codebase. Each skill file in this directory is a standalone markdown document containing the system prompt — copy it into your project as `AGENTS.md`, or reference it directly.

## Installation

**As AGENTS.md** (Codex picks it up automatically from the project root):

```bash
cp codex/<skill-name>/<skill-name>.md AGENTS.md
```

**Via the `--instructions` flag** (one-off use):

```bash
codex --instructions codex/<skill-name>/<skill-name>.md "your task here"
```

**Via config** (`~/.codex/config.yaml`):

```yaml
instructions: /path/to/codex/<skill-name>/<skill-name>.md
```

## Available Skills

| Skill | File | Description |
|-------|------|-------------|
| XR Educator | [`xr-educator/xr-educator.md`](xr-educator/xr-educator.md) | Workshop designer and educator for XR experiences |
| XR Researcher | [`xr-researcher/xr-researcher.md`](xr-researcher/xr-researcher.md) | Research strategist for incorporating XR into academic and R&D work |
| XR Safety Manager | [`xr-safety-manager/xr-safety-manager.md`](xr-safety-manager/xr-safety-manager.md) | Safety training specialist for XR-based HSE programs |

## Notes

- Codex supports multiple `AGENTS.md` files at different directory levels — deeper files take precedence.
- The skill files in this directory are plain markdown with no frontmatter, ready to use as-is.
