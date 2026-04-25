# Contributing a Plugin

Each plugin in this marketplace is a self-contained Claude Code plugin inside its own directory.

## Plugin directory structure

```
my-plugin/
├── .claude-plugin/
│   └── plugin.json               # Required — plugin manifest
├── skills/                       # Optional — auto-invoked skills
│   └── <skill-name>/
│       └── SKILL.md
├── commands/                     # Optional — slash commands
│   └── <command-name>.md
├── agents/                       # Optional — subagents
│   └── <agent-name>.md
├── hooks/                        # Optional — enforcement hooks
│   ├── hooks.json
│   └── <hook-script>.sh
├── templates/                    # Optional — files dropped during init
├── README.md                     # Required — plugin docs
└── ...
```

## Minimal plugin.json

```json
{
  "name": "my-plugin",
  "version": "0.1.0",
  "description": "One sentence — what it does.",
  "author": { "name": "Your Name" },
  "license": "MIT"
}
```

## Steps to add a plugin

1. **Create the directory** at the repo root: `my-plugin/`
2. **Add `.claude-plugin/plugin.json`** with at least `name` and `version`
3. **Add your components** — skills, commands, agents, hooks, templates
4. **Write a README.md** inside the plugin directory
5. **Register in `marketplace.json`** — add an entry to the `plugins` array:

   ```json
   {
     "name": "my-plugin",
     "source": "./my-plugin",
     "description": "One sentence.",
     "version": "0.1.0"
   }
   ```

6. **Update the root README.md** — add a row to the Available Plugins table
7. **Test locally**:

   ```bash
   claude --plugin-dir ./my-plugin
   ```

## Design principles

- **Zero install beyond Claude Code.** No pip, no brew, no npm.
- **Enforcement, not suggestion.** Use hooks for invariants.
- **One domain, done well.** Each plugin solves one workflow problem.
- **Native first.** Prefer Claude's built-in capabilities.
