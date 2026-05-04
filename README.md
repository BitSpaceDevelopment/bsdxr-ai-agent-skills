# Agent Skills

Precision-built system prompts for AI coding assistants. Each skill is a carefully engineered set of instructions that transforms an AI coding tool into a focused, opinionated development partner — consistent behavior, every session.

The accompanying `index.html` is a single-page reference site: explains what agent skills are, lists supported platforms, and provides copyable prompts for each skill.

## Supported Platforms

| Platform | Directory | Format |
|----------|-----------|--------|
| [Claude Code](https://claude.ai/code) | `claude/` | Markdown skill file with YAML frontmatter — place in `.claude/agents/` |
| [OpenCode](https://github.com/opencode-ai/opencode) | `opencode/` | TOML/Markdown agent config |
| [Codex](https://github.com/openai/codex) | `codex/` | Markdown system prompt, pass via `--instructions` or config |
| [GitHub Copilot](https://github.com/features/copilot) | `copilot/` | Paste into `.github/copilot-instructions.md` |
| [Gemini CLI](https://github.com/google-gemini/gemini-cli) | `gemini/` | Add to `GEMINI.md` or agent config |

## Available Skills

### Developer

A senior full-stack development agent. Writes clean, production-ready code with strong opinions on architecture, testing, and security.

**Use for:** implementation tasks, code review, debugging, technical design decisions.

**Covers:** core behavior, code quality, architecture, error handling, security, testing, debugging, communication, workflow.

| Platform | Path | Status |
|----------|------|--------|
| Claude Code | [`claude/developer/developer.md`](claude/developer/developer.md) | Active |
| OpenCode | [`opencode/developer/`](opencode/developer/) | Planned |
| Codex | [`codex/developer/`](codex/developer/) | Planned |
| Copilot | [`copilot/developer/`](copilot/developer/) | Planned |
| Gemini CLI | [`gemini/developer/`](gemini/developer/) | Planned |

To use on Claude Code, copy to your project:
```
cp claude/developer/developer.md .claude/agents/developer.md
```

## Project Structure

```
agentskills/
├── index.html               # Single-page reference site
├── README.md
├── bsd-branding-repo/       # Branding submodule (logos, colors, fonts)
├── .claude/
│   └── agents/
│       └── developer.md     # Active Claude Code agent
├── claude/
│   └── developer/
│       └── developer.md     # Source skill definition
├── opencode/
│   └── developer/
├── codex/
│   └── developer/
├── copilot/
│   └── developer/
└── gemini/
    └── developer/
```

## Design Principles

- **Platform-native** — each skill uses the idiomatic format for its target platform, no lowest-common-denominator abstractions.
- **Consistent intent** — the same agent (e.g. developer) behaves the same regardless of which platform runs it.
- **Composable** — skills are self-contained and can be mixed, extended, or overridden per-project.
- **Version-controlled** — every change is committed so skill evolution is traceable.

## Adding a New Skill

1. Create subdirectories under each platform (e.g. `claude/reviewer/`, `codex/reviewer/`).
2. Write the skill definition in each platform's native format, starting with Claude.
3. Update `index.html` — add an entry to the `SKILLS` array in the `<script>` section.
4. Update this README's "Available Skills" table.
5. Copy the Claude version into `.claude/agents/` so it's immediately usable.
6. Commit.

## Adding a New Platform

1. Create a top-level directory named after the platform.
2. Add subdirectories for each existing skill.
3. Port skill definitions to the new platform's format.
4. Add the platform to the `PLATFORMS` array in `index.html`.
5. Update the "Supported Platforms" table above.

## Branding

This project uses the BSD XR brand system from the `bsd-branding-repo` submodule. See [`bsd-branding-repo/branding.md`](bsd-branding-repo/branding.md) for the full specification: colors, typography, component patterns, and voice guidelines.

---

Bit Space Development Ltd. — [bsdxr.com](https://bsdxr.com)
