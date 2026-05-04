# Agent Skills

A collection of reusable agent skills and system prompts for AI-powered development workflows. Each skill is tailored per platform while sharing a common intent, so the same capabilities work across every major AI coding assistant.

## Supported Platforms

| Platform | Directory | Format |
|----------|-----------|--------|
| [Claude Code](https://claude.ai/code) | `claude/` | Markdown skill files (`.md`) with YAML frontmatter |
| [OpenCode](https://github.com/opencode-ai/opencode) | `opencode/` | TOML/Markdown agent configs |
| [Codex](https://github.com/openai/codex) | `codex/` | Markdown system prompts |
| [Copilot](https://github.com/features/copilot) | `copilot/` | `.github/copilot-instructions.md` format |
| [Gemini CLI](https://github.com/google-gemini/gemini-cli) | `gemini/` | Gemini agent configs |

## Available Agents

### Developer

A senior full-stack development agent focused on writing clean, production-ready code with best practices baked in.

| Platform | Path | Status |
|----------|------|--------|
| Claude | [`claude/developer/`](claude/developer/) | In progress |
| OpenCode | [`opencode/developer/`](opencode/developer/) | Planned |
| Codex | [`codex/developer/`](codex/developer/) | Planned |
| Copilot | [`copilot/developer/`](copilot/developer/) | Planned |
| Gemini | [`gemini/developer/`](gemini/developer/) | Planned |

## Project Structure

```
agentskills/
├── README.md
├── claude/
│   └── developer/       # Claude Code skill files
├── opencode/
│   └── developer/       # OpenCode agent configs
├── codex/
│   └── developer/       # Codex system prompts
├── copilot/
│   └── developer/       # Copilot instruction files
└── gemini/
    └── developer/       # Gemini agent configs
```

## Design Principles

- **Platform-native**: Each skill uses the idiomatic format for its target platform — no lowest-common-denominator abstractions.
- **Consistent intent**: The same agent (e.g. "developer") should behave similarly regardless of which platform runs it.
- **Composable**: Skills are self-contained and can be mixed, extended, or overridden per-project.
- **Version-controlled**: Every change is committed so skill evolution is traceable.

## Usage

Each platform directory contains its own setup instructions. Generally:

1. Copy or symlink the relevant skill files into your project or global config.
2. Invoke the agent through your platform's normal mechanism (slash command, CLI flag, config reference).

Refer to the README inside each platform directory for platform-specific details.

## Adding a New Agent

1. Create a new subdirectory under each platform (e.g. `claude/reviewer/`, `codex/reviewer/`).
2. Write the skill definition in that platform's native format.
3. Update this README's "Available Agents" table.
4. Commit with a descriptive message.

## Adding a New Platform

1. Create a top-level directory named after the platform.
2. Add subdirectories for each existing agent.
3. Port the agent definitions to the new platform's format.
4. Update the "Supported Platforms" table above.

## License

Private — for personal development use.
