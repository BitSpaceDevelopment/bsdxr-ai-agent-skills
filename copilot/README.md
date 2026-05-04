# GitHub Copilot — Agent Skills

Agent skills for [GitHub Copilot](https://github.com/features/copilot), the AI assistant for VS Code, JetBrains, and GitHub.com. Copilot supports repository-level custom instructions via a `.github/copilot-instructions.md` file — any skill in this directory can be used as the content of that file.

## How It Works

When Copilot detects `.github/copilot-instructions.md` in a repository, it applies those instructions to all Copilot interactions in that repo. The file is plain markdown — no frontmatter required.

## Installation

```bash
mkdir -p .github
cp copilot/<skill-name>/<skill-name>.md .github/copilot-instructions.md
```

Then commit the file to your repository so all contributors benefit from the same instructions:

```bash
git add .github/copilot-instructions.md
git commit -m "Add Copilot instructions"
```

## Available Skills

| Skill | File | Description |
|-------|------|-------------|
| XR Educator | [`xr-educator/xr-educator.md`](xr-educator/xr-educator.md) | Workshop designer and educator for XR experiences |
| XR Researcher | [`xr-researcher/xr-researcher.md`](xr-researcher/xr-researcher.md) | Research strategist for incorporating XR into academic and R&D work |
| XR Safety Manager | [`xr-safety-manager/xr-safety-manager.md`](xr-safety-manager/xr-safety-manager.md) | Safety training specialist for XR-based HSE programs |

## Notes

- Only one `copilot-instructions.md` file is active per repository.
- Instructions apply to Copilot Chat, inline suggestions, and Copilot in the GitHub.com UI.
- Keep the file focused — instructions that are too broad or too long reduce Copilot's effectiveness.
- Copilot custom instructions require a Copilot Business or Enterprise plan, or a Copilot Individual plan with the feature enabled in VS Code settings (`github.copilot.chat.codeGeneration.useInstructionFiles`).
