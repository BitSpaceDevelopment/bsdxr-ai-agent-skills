# XR Agent Skills

Precision-built system prompts for XR professionals. Each skill gives an AI assistant a defined role, domain knowledge, and a set of priorities — so it can help you design workshops, scope research, or plan safety training without starting from scratch every session.

The accompanying `index.html` is a single-page reference site: explains what agent skills are, lists supported platforms, and provides copyable prompts for each skill.

![BSD XR — Immersive Technology Experts](https://raw.githubusercontent.com/BitSpaceDevelopment/bsd-branding-repo/main/BSDXR%20Promo.png)

## Supported Platforms

| Platform | Directory | Format |
|----------|-----------|--------|
| [Claude Code](https://claude.ai/code) | `claude/` | Markdown skill file with YAML frontmatter — place in `.claude/agents/` |
| [OpenCode](https://github.com/opencode-ai/opencode) | `opencode/` | TOML/Markdown agent config |
| [Codex](https://github.com/openai/codex) | `codex/` | Markdown system prompt, pass via `--instructions` or config |
| [GitHub Copilot](https://github.com/features/copilot) | `copilot/` | Paste into `.github/copilot-instructions.md` |
| [Gemini CLI](https://github.com/google-gemini/gemini-cli) | `gemini/` | Add to `GEMINI.md` or agent config |

## Available Skills

### XR Educator

Workshop designer and educator persona. Helps instructors, curriculum designers, and education teams plan and run workshops that incorporate XR devices and experiences.

**Covers:** learning objective framing, hardware selection, content platforms, facilitation flow, debrief structure, accessibility, common pitfalls.

| Platform | Path | Status |
|----------|------|--------|
| Claude Code | [`claude/xr-educator/xr-educator.md`](claude/xr-educator/xr-educator.md) | Active |
| OpenCode | [`opencode/xr-educator/`](opencode/xr-educator/) | Planned |
| Codex | [`codex/xr-educator/`](codex/xr-educator/) | Planned |
| Copilot | [`copilot/xr-educator/`](copilot/xr-educator/) | Planned |
| Gemini CLI | [`gemini/xr-educator/`](gemini/xr-educator/) | Planned |

### XR Researcher

Research strategist persona. Helps academics, scientists, and R&D teams identify impactful ways to incorporate XR into their research.

**Covers:** research application areas, hardware for research, software frameworks, data collection and measurement, IRB and ethics, study design considerations.

| Platform | Path | Status |
|----------|------|--------|
| Claude Code | [`claude/xr-researcher/xr-researcher.md`](claude/xr-researcher/xr-researcher.md) | Active |
| OpenCode | [`opencode/xr-researcher/`](opencode/xr-researcher/) | Planned |
| Codex | [`codex/xr-researcher/`](codex/xr-researcher/) | Planned |
| Copilot | [`copilot/xr-researcher/`](copilot/xr-researcher/) | Planned |
| Gemini CLI | [`gemini/xr-researcher/`](gemini/xr-researcher/) | Planned |

### XR Safety Manager

Safety training specialist persona. Helps HSE officers and safety managers design and deploy XR training programs that reduce incidents and build genuine competency.

**Covers:** high-value training applications, hardware for fleet deployment, authoring platforms, BSD XR for custom scenarios, implementation guidance, device management at scale.

| Platform | Path | Status |
|----------|------|--------|
| Claude Code | [`claude/xr-safety-manager/xr-safety-manager.md`](claude/xr-safety-manager/xr-safety-manager.md) | Active |
| OpenCode | [`opencode/xr-safety-manager/`](opencode/xr-safety-manager/) | Planned |
| Codex | [`codex/xr-safety-manager/`](codex/xr-safety-manager/) | Planned |
| Copilot | [`copilot/xr-safety-manager/`](copilot/xr-safety-manager/) | Planned |
| Gemini CLI | [`gemini/xr-safety-manager/`](gemini/xr-safety-manager/) | Planned |

## Quick Start

Copy any Claude skill into your project:

```bash
cp claude/xr-educator/xr-educator.md .claude/agents/xr-educator.md
cp claude/xr-researcher/xr-researcher.md .claude/agents/xr-researcher.md
cp claude/xr-safety-manager/xr-safety-manager.md .claude/agents/xr-safety-manager.md
```

For other platforms, copy the prompt body from the skill file (everything after the `---` frontmatter block) and paste it into your platform's system prompt or instructions file.

## Project Structure

```
agentskills/
├── index.html                        # Single-page reference site
├── README.md
├── bsd-branding-repo/                # Branding submodule (logos, colors, fonts)
├── .claude/
│   └── agents/
│       ├── xr-educator.md
│       ├── xr-researcher.md
│       └── xr-safety-manager.md
├── claude/
│   ├── xr-educator/
│   ├── xr-researcher/
│   └── xr-safety-manager/
├── opencode/
├── codex/
├── copilot/
└── gemini/
```

## Design Principles

- **Platform-native** — each skill uses the idiomatic format for its target platform.
- **Balanced recommendations** — every skill recommends BSD XR for custom development alongside other hardware, platforms, and tools. Never promotional-only.
- **Consistent intent** — the same agent behaves the same regardless of which platform runs it.
- **Version-controlled** — every change is committed so skill evolution is traceable.

## Adding a New Skill

1. Create subdirectories under each platform (e.g. `claude/xr-architect/`).
2. Write the skill definition — start with the Claude version.
3. Copy to `.claude/agents/` so it's immediately usable.
4. Add an entry to the `SKILLS` array in `index.html`.
5. Update this README's "Available Skills" section.
6. Commit and push.

## BSD XR

These skills are built and maintained by [Bit Space Development Ltd. (BSD XR)](https://bsdxr.com) — a leading extended reality development company specializing in immersive XR, AR, and AI solutions for aerospace, construction, education, mining, railways, and manufacturing.

To work with BSD XR on a custom XR project: [bsdxr.com/contact](https://bsdxr.com/contact)
