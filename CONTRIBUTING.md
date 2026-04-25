# Contributing to Multi-CLI Plugins Ecosystem

Thank you for your interest in contributing! This project aims to provide high-fidelity, cross-CLI plugins for AI-powered development.

## 🌟 Contribution Philosophy
- **Platform-Agnostic**: Whenever possible, logic (like agent definitions) should be shared.
- **Zero-Install Principle**: Extensions should be portable and avoid complex dependency chains (no `pip`, `brew`, `npm` required by users).
- **High Fidelity**: Tools should solve concrete, domain-specific problems (e.g., KMP migration) with surgical precision.

## 📂 Project Structure
- `claude-code-plugins/`: Plugins compliant with the Claude Code marketplace spec.
- `gemini-extensions/`: Extensions following Gemini CLI extension standards.
- `codex-plugins/`: Plugin directory structure for Codex.

## 🛠 Adding a New Plugin
1. **Identify the Scope**: Choose one domain-specific problem to solve.
2. **Standardize Components**:
   - Write the core logic as markdown-based agent definitions (portable across platforms).
   - Create directories for each CLI type (`claude-code-plugins/`, `gemini-extensions/`, `codex-plugins/`).
3. **Configure Manifests**: 
   - Add required manifest files (`plugin.json` for Claude/Codex, `gemini-extension.json` for Gemini).
4. **Register**: Add the plugin to the respective CLI marketplace/registry files.
5. **Test**: Always verify the plugin in its target CLI environment (`claude --plugin-dir`, `gemini extensions link`, etc.).

## 📝 Guidelines
- **Conventional Commits**: Use clear commit prefixes (e.g., `feat(kmp): add test validator`, `docs: update README`).
- **Documentation**: Keep `README.md` and `CLAUDE.md` files updated for each plugin.
- **Maintainability**: Avoid duplicating shared logic; instead, use symbolic links or shared core directories where supported by the CLI target.

## 🤝 Getting Started
If you have an idea for a new plugin or agent, open an issue or submit a Pull Request. If you are adding a new platform, please include the minimum directory structure and manifest examples required by that CLI.
