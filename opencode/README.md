# OpenCode — Agent Skills

Agent skills for [OpenCode](https://github.com/opencode-ai/opencode), the open-source AI coding terminal. OpenCode supports custom agents defined as markdown files with TOML frontmatter, placed in the `.opencode/agents/` directory of your project or home directory.

## How It Works

Each skill file is a markdown document with TOML frontmatter:

```markdown
---
name = "skill-name"
description = "One-line description of when to use this agent."
---

[System prompt body]
```

OpenCode reads the `description` to surface agents in the UI and for automatic routing.

## Installation

**Project-level** (applies only in the current repo):

```bash
mkdir -p .opencode/agents
cp opencode/<skill-name>/<skill-name>.md .opencode/agents/<skill-name>.md
```

**Global** (applies across all projects):

```bash
mkdir -p ~/.opencode/agents
cp opencode/<skill-name>/<skill-name>.md ~/.opencode/agents/<skill-name>.md
```

## Available Skills

| Skill | File | Description |
|-------|------|-------------|
| XR Educator | [`xr-educator/xr-educator.md`](xr-educator/xr-educator.md) | Workshop designer and educator for XR experiences |
| XR Researcher | [`xr-researcher/xr-researcher.md`](xr-researcher/xr-researcher.md) | Research strategist for incorporating XR into academic and R&D work |
| XR Safety Manager | [`xr-safety-manager/xr-safety-manager.md`](xr-safety-manager/xr-safety-manager.md) | Safety training specialist for XR-based HSE programs |

## Usage

Once installed, select the agent from the OpenCode agent picker, or reference it by name in your prompt.
