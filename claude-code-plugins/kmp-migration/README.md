# KMP Migration Plugin

Specialized agents for migrating Android projects to Kotlin Multiplatform (KMP).

Version: `0.1.2`

## Agents

### `android-project-analyst`
Deeply analyzes existing Android projects to understand UI (XML/Compose), control logic, data flow, and architecture. Produces SPEC documentation (PRD, DESIGN, PLAN).

### `android-to-kmp-migrator`
Plans and executes full or explicitly scoped Android-to-KMP migration. Produces runnable KMP code for UI, business logic, data layers, navigation, theming, and related Android components, then requires compile, preview, and use-case validation.

### `kmp-test-validator`
Validates the KMP implementation against the original Android source. Performs a high-fidelity audit to ensure the KMP version matches the Android behavior exactly.

### `memory-curator`
Audits and optimizes agent memory stores. Recommends which memories to retain, archive, or delete, and records resumable agent state for recovery.

### `skill-maintenance-advisor`
Reviews conversation context at regular turn intervals and recommends creating or updating reusable skills when useful patterns appear.

## Usage

After installation, the agents will be available in your Claude Code environment. You can trigger them by name or by describing the task (e.g., "Analyze this Android project for KMP migration").

## Structure

- `agents/`: Subagent definitions.
- `commands/`: Reserved for future custom slash commands.
- `skills/`: Reserved for future Claude Code skills.
- `hooks/`: Reserved for future tool-layer enforcement.
- `templates/`: Reserved for future migration templates.
