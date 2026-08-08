# AI Ignore Templates

Templates for configuring which files AI coding tools should ignore when building project context.

The templates are consumed by [okram.dev](https://okram.dev) from the `main` branch. The repository currently includes OpenCode and Codex templates for JavaScript / TypeScript, Java, and Python.

OpenCode templates use `.ignore`, which is respected by the ripgrep-based `glob` and `grep` tools without changing the project's `.gitignore`.

Codex templates generate a project-named permission profile for `~/.codex/config.toml`. After adding the profile, use `/permissions` in Codex to select it.

The profile name is replaced by okram.dev when the template is generated.

Claude Code templates generate `.claude/settings.json` with project-level `permissions.deny` rules.

Pi templates generate `AGENTS.md` project instructions. Pi loads `AGENTS.md` from the project directory and uses it as context guidance.
