# Claude Code — Agent Skills

Agent skills for [Claude Code](https://claude.ai/code), Anthropic's official CLI for Claude. Claude Code has a native agent skill system: drop a markdown file into `.claude/agents/` and it becomes an invokable subagent with its own system prompt, role, and behavior.

## How It Works

Each skill file is a markdown document with YAML frontmatter:

```markdown
---
name: skill-name
description: One-line description — used by Claude to decide when to route to this agent.
---

[System prompt body]
```

The `description` field is critical. Claude reads it to decide whether to dispatch to the agent. Write it as a precise, specific sentence about when the agent should be used.

## Installation

**Project-level** (applies only in the current repo):

```bash
cp claude/<skill-name>/<skill-name>.md .claude/agents/<skill-name>.md
```

**Global** (applies across all projects):

```bash
cp claude/<skill-name>/<skill-name>.md ~/.claude/agents/<skill-name>.md
```

## Available Skills

| Skill | File | Description |
|-------|------|-------------|
| XR Educator | [`xr-educator/xr-educator.md`](xr-educator/xr-educator.md) | Workshop designer and educator for XR experiences |
| XR Researcher | [`xr-researcher/xr-researcher.md`](xr-researcher/xr-researcher.md) | Research strategist for incorporating XR into academic and R&D work |
| XR Safety Manager | [`xr-safety-manager/xr-safety-manager.md`](xr-safety-manager/xr-safety-manager.md) | Safety training specialist for XR-based HSE programs |

## Usage

Once installed, invoke a skill by asking Claude to use it:

```
Use the XR educator skill to help me plan a workshop for 30 nursing students.
```

Or Claude will route to it automatically when the task matches the skill's description.

## Notes

- Skills are isolated — each has its own system prompt and does not inherit from the parent Claude session.
- You can have multiple skills installed simultaneously.
- The `model` frontmatter key is optional — omit it to use the default model, or specify `claude-opus-4-5`, `claude-sonnet-4-5`, etc.
