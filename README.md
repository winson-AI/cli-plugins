# Multi-CLI Plugins Ecosystem

A collection of specialized, high-performance plugins and agents designed for AI-powered CLI environments. These tools are built to be cross-compatible, supporting **Claude Code**, **Gemini CLI**, **Codex**, and other open-source AI agent frameworks.

## 🚀 Key Features

- **Cross-CLI Support**: Standardized markdown-based agent definitions that work seamlessly across different AI environments.
- **Zero-Install Principle**: Designed to be portable and dependency-free, allowing for instant usage.
- **High Fidelity**: Specialized agents for complex workflows like Android-to-KMP migration.

## 📦 Available Plugins

| Plugin | Description | Supported CLIs |
|--------|-------------|----------------|
| **[kmp-migration](claude-code-plugins/kmp-migration/)** | A complete toolkit for migrating Android projects to Kotlin Multiplatform (KMP). Includes analysis, migration, and validation agents. | Claude Code, Gemini, Codex |

---

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
To utilize these specialized agents in Gemini:
1. Locate the agent definitions in `claude-code-plugins/kmp-migration/agents/`.
2. Reference or import these `.md` files into your Gemini project configuration.
3. Invoke directly: `invoke_agent("android-to-kmp-migrator", "Convert this module")`.

### 3. Codex & Open Source Repos
For Codex or custom implementations:
- Point your agent configuration to the `agents/` directory of the desired plugin.
- The YAML frontmatter in each `.md` file defines the tools, model, and triggers required for the agent to operate.

---

## 📂 Project Structure

```
cli-plugins/
├── claude-code-plugins/          # Central directory for all plugin packages
│   ├── .claude-plugin/           # Marketplace registry
│   └── kmp-migration/            # KMP Migration Toolkit
│       ├── agents/               # Multi-platform agent definitions (.md)
│       ├── skills/               # Automated capabilities
│       ├── commands/             # Slash commands
│       └── README.md             # Plugin documentation
├── CONTRIBUTING.md               # How to contribute new plugins or agents
└── README.md                     # This file
```

## 🤝 Contributing

We welcome contributions of new plugins or improvements to existing agents. Please refer to [CONTRIBUTING.md](claude-code-plugins/CONTRIBUTING.md) for detailed guidelines on the plugin structure and design principles.

## 📄 License

MIT
