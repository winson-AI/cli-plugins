# KMP Migration Toolkit for Claude Code

A collection of specialized agents for knowledge workers migrating Android projects to Kotlin Multiplatform (KMP). Part of the `cli-plugins` ecosystem.

## Install

```bash
# Add the marketplace (one-time)
/plugin marketplace add <repository-url>

# Install the plugin
/plugin install kmp-migration
```

Or load the plugin directly for development:

```bash
claude --plugin-dir ./claude-code-plugins/kmp-migration
```

## Available Plugins

| Plugin | Description | Version |
|--------|-------------|---------|
| [kmp-migration](kmp-migration/) | End-to-end Android to KMP migration toolkit. Includes specialized agents for project analysis, source-to-source migration, fidelity-first test validation, memory curation, and skill maintenance. | 0.1.2 |

### kmp-migration

**What it ships:**
- 5 specialized agents:
  - `android-project-analyst`: Deep Android architecture, UI, data/control flow analysis, and SPEC generation.
  - `android-to-kmp-migrator`: Runnable Android-to-KMP migration with mandatory compile, preview, and use-case validation.
  - `kmp-test-validator`: High-fidelity validation against Android behavior and provided test cases.
  - `memory-curator`: Agent memory audit, cleanup recommendations, and recovery state records.
  - `skill-maintenance-advisor`: Periodic advice for creating or updating reusable skills from conversation context.
- Standard placeholder structure for commands, skills, hooks, and templates.

Full docs: [kmp-migration/README.md](kmp-migration/README.md)

## Repository Structure

```
claude-code-plugins/
├── .claude-plugin/
│   └── marketplace.json          # Plugin registry — lists all available plugins
├── kmp-migration/                # Plugin: KMP Migration Toolkit
│   ├── .claude-plugin/
│   │   └── plugin.json           # Plugin manifest
│   ├── skills/                   # Auto-invoked skills
│   ├── commands/                 # Slash commands
│   ├── agents/                   # Specialized subagents
│   ├── hooks/                    # Tool-layer enforcement
│   ├── templates/                # Migration templates
│   └── README.md                 # Plugin-specific docs
├── CONTRIBUTING.md               # How to add a plugin
├── CLAUDE.md                     # Repository instructions for Claude
└── README.md                     # This file
```

## License

MIT
