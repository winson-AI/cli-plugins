# Multi-CLI Plugins Ecosystem

A collection of specialized, high-performance plugins and agents designed for AI-powered CLI environments. These tools are built to be cross-compatible, supporting **Claude Code**, **Gemini CLI**, **Codex**, and other open-source AI agent frameworks.

## 🚀 Key Features

- **Cross-CLI Support**: Standardized structures for Claude Code, Gemini extensions, and Codex plugins.
- **Zero-Install Principle**: Designed to be portable and dependency-free.
- **High Fidelity**: Specialized agents for complex workflows like Android-to-KMP migration.

## 📦 Available Plugins & Extensions

| Plugin | Description | Claude Code | Gemini CLI | Codex |
|--------|-------------|-------------|------------|-------|
| **[kmp-migration](claude-code-plugins/kmp-migration/)** | Toolkit for Android-to-KMP migration (Analysis, Migration, Validation). | 0.1.1 | 0.1.1 | 0.1.1 |

---

## 🛠 Install Guidance

### 1. Clone This Repository
```bash
git clone https://github.com/winson/cli-plugins.git
```

### 2. Add the Marketplace for Each CLI
From the relevant plugin or extension folder, run the CLI marketplace add command with the current directory (`.`).

```bash
# Claude Code
case one: start claude with plugin path
claude --plugin-dir cli-plugins/claude-code-plugins/kmp-migration

case two: afer start claude
/plugin marketplace add cli-plugins/claude-code-plugins
/plugin install kmp-migration

# Codex
step one: cd codex-plugins
step two: codex plugin marketplace add .
step three: codex -> /plugins switch to market and install

# Gemini CLI
step one: cd gemini-extensions/kmp-migration
step two: gemini extensions install .
step three: gemini extensions list -> gemini -> /extensions
```

General form:

```bash
cli-name plugin marketplace add .
```

## 🛠 Usage Instructions

### 1. Claude Code
This repository follows the Claude Code plugin marketplace structure.
```bash
# Add the marketplace
/plugin marketplace add https://github.com/winson/cli-plugins

# Install the kmp-migration toolkit
/plugin install kmp-migration
```

### 2. Gemini CLI
To use these agents within the Gemini CLI environment:
1. Copy the relevant plugin folder from `gemini-extensions/` to your local extensions directory.
2. Link the extension for testing: `gemini extensions link .`
3. Invoke agents directly: `invoke_agent("android-to-kmp-migrator", "Convert this module")`.

### 3. Codex
For Codex integration:
- Point your Codex configuration to the `codex-plugins/` directory.
- The manifest (`plugin.json`) and skill definitions will be automatically detected.

---

## 📂 Project Structure

```
cli-plugins/
├── claude-code-plugins/    # Plugins for Claude Code
├── gemini-extensions/      # Extensions for Gemini CLI
├── codex-plugins/          # Plugins for Codex
├── CONTRIBUTING.md         # Guidelines for contributions
└── README.md               # This file
```

## 🤝 Contributing

We welcome contributions. Please refer to [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines on the project structure and design principles.

## 📄 License

MIT
