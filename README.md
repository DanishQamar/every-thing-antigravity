# Everything AntiGravity

**A comprehensive configuration collection for AntiGravity (Gemini), inspired by [Everything Claude Code](https://github.com/affaan-m/everything-claude-code).**

This repository contains battle-tested configurations to supercharge your AntiGravity coding agent with specialized rules, skills, and workflows.

## Process

We researched the original `affaan-m/everything-claude-code` repository, analyzed its structure (Agents, Skills, Rules, Commands), and ported the best components to AntiGravity's native format.

## What's Inside

### `.agent/rules/`
Global behavioral guidelines that AntiGravity will always follow.
- **`coding-style.md`**: Best practices for cleaner, safer code (Immutability, Error Handling).
- **`security.md`**: Mandatory security checks (No hardcoded secrets, SQLi prevention).

### `.agent/skills/`
Domain-specific knowledge packages that AntiGravity leverages for specific tasks.
- **`backend/`**: Patterns for REST APIs, Database transactions, Caching, etc.
- **`coding-standards/`**: Universal naming conventions and React best practices.
- **`tdd/`**: The Test-Driven Development "Red-Green-Refactor" cycle.

### `.agent/workflows/`
Automated processes (replacing "Agents" and "Commands").
- **`architect-review`**: High-level system design analysis.
- **`security-review`**: Deep-dive vulnerability assessment.
- **`tdd`**: Step-by-step TDD session guide.
- **`plan`**: Create robust implementation plans.
- **`code-review`**: Automated code quality checks.

### Other
- **`mcp-servers.json`**: Reference configuration for Model Context Protocol servers (GitHub, Supabase, etc.).
- **`docs/hooks.md`**: Guide on how to implement "hooks" in AntiGravity.

## Quick Start

1. **Verify Installation**: Ensure this repository is checked out or the `.agent` folder is copied to your project root.
2. **Trigger a Workflow**:
   - "Start a security review" -> Triggers `security-review`
   - "Help me plan this feature" -> Triggers `plan`
   - "Let's do TDD for this function" -> Triggers `tdd`
3. **Benefit from Rules**: AntiGravity will automatically apply `coding-style` and `security` guidelines to its output.

## Credits

Heavily inspired by and adapted from [affaan-m/everything-claude-code](https://github.com/affaan-m/everything-claude-code).
