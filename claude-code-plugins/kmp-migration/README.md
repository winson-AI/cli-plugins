# KMP Migration Plugin

Specialized agents for migrating Android projects to Kotlin Multiplatform (KMP).

## Agents

### `android-project-analyst`
Deeply analyzes existing Android projects to understand UI (XML/Compose), control logic, data flow, and architecture. Produces SPEC documentation (PRD, DESIGN, PLAN).

### `android-to-kmp-migrator`
Plans and executes the migration of Android components to KMP. Handles source code transformation and architectural mapping.

### `kmp-test-validator`
Validates the KMP implementation against the original Android source. Performs a high-fidelity audit to ensure the KMP version matches the Android behavior exactly.

## Usage

After installation, the agents will be available in your Claude Code environment. You can trigger them by name or by describing the task (e.g., "Analyze this Android project for KMP migration").

## Structure

- `agents/`: Subagent definitions.
- `commands/`: Custom slash commands (Placeholder).
- `skills/`: Automated skills (Placeholder).
- `hooks/`: Tool-layer enforcement (Placeholder).
- `templates/`: Migration templates (Placeholder).
