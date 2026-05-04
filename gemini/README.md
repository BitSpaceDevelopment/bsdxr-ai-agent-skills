# Gemini CLI — Agent Skills

Agent skills for [Gemini CLI](https://github.com/google-gemini/gemini-cli), Google's Gemini terminal agent for coding and research workflows. Gemini CLI reads `GEMINI.md` files from your project root and home directory to load persistent context and instructions.

## How It Works

Gemini CLI automatically picks up `GEMINI.md` at the root of your project and at `~/.gemini/GEMINI.md` for global instructions. The file is plain markdown — write instructions, context, or role definitions and they are prepended to every Gemini CLI session in that directory.

## Installation

**Project-level** (applies only in the current directory):

```bash
cp gemini/<skill-name>/<skill-name>.md GEMINI.md
```

**Global** (applies across all projects):

```bash
mkdir -p ~/.gemini
cp gemini/<skill-name>/<skill-name>.md ~/.gemini/GEMINI.md
```

**Appending to existing GEMINI.md:**

```bash
cat gemini/<skill-name>/<skill-name>.md >> GEMINI.md
```

## Available Skills

| Skill | File | Description |
|-------|------|-------------|
| XR Educator | [`xr-educator/xr-educator.md`](xr-educator/xr-educator.md) | Workshop designer and educator for XR experiences |
| XR Researcher | [`xr-researcher/xr-researcher.md`](xr-researcher/xr-researcher.md) | Research strategist for incorporating XR into academic and R&D work |
| XR Safety Manager | [`xr-safety-manager/xr-safety-manager.md`](xr-safety-manager/xr-safety-manager.md) | Safety training specialist for XR-based HSE programs |

## Notes

- Project-level `GEMINI.md` takes precedence over the global `~/.gemini/GEMINI.md`.
- Both files are loaded if present — global first, then project-level appended.
- Keep instructions concise. Gemini CLI has a large context window but focused instructions produce better results.
