# How to Use Everything AntiGravity in a New Project

This guide explains how to install and leverage the "Everything AntiGravity" configurations in your own projects.

## Installation

### Option 1: Copy to Project (Per-Project Config)

The most robust way to use these configurations is to copy the `.agent` directory into the root of your project.

1.  **Navigate to your new project root:**
    ```bash
    cd path/to/my-new-project
    ```

2.  **Copy the `.agent` folder:**
    Assuming you have `everything-antigravity` cloned locally:
    ```bash
    cp -r path/to/everything-antigravity/.agent .
    ```

    Your project structure should look like this:
    ```
    my-new-project/
    ├── .agent/
    │   ├── rules/
    │   ├── skills/
    │   └── workflows/
    ├── src/
    └── ...
    ```

### Option 2: Global Configuration (If supported)

If AntiGravity supports a global configuration directory (e.g., `~/.antigravity` or `~/.gemini`), you can copy the contents there. *Note: Check your specific AntiGravity version documentation for global support.*

## Configuration

### MCP Servers

If you need external tool access (GitHub, Database, etc.), configure your MCP servers.

1.  **Locate the reference config:**
    Open `mcp-servers.json` in the `everything-antigravity` repository.

2.  **Add to your Global Config:**
    Copy the relevant server configurations to your global AntiGravity config file (usually `~/.gemini/config.json` or `~/.claude.json` pending specific implementation details).

    *Example:*
    ```json
    {
      "mcpServers": {
        "github": {
          "command": "npx",
          "args": ["-y", "@modelcontextprotocol/server-github"],
          "env": { "GITHUB_PERSONAL_ACCESS_TOKEN": "..." }
        }
      }
    }
    ```

## Usage Examples

Once installed, AntiGravity will automatically ingest the Rules and Skills. You can trigger Workflows using natural language.

### 1. Starting a New Feature
**Prompt:**
> "I want to add a new user profile page. Help me plan this."

**What happens:**
- AntiGravity detects the intent and triggers the **Plan** workflow.
- It will ask you for goal descriptions, breaking changes, etc.
- It will generate an `implementation_plan.md`.

### 2. Developing with TDD
**Prompt:**
> "Let's implement the `calculateTax` function using TDD."

**What happens:**
- AntiGravity triggers the **TDD** workflow.
- It will guide you: *Define Interface* -> *Red (Fail)* -> *Green (Pass)* -> *Refactor*.

### 3. Security Check
**Prompt:**
> "Review `auth.ts` for security issues."

**What happens:**
- AntiGravity triggers the **Security Review** workflow.
- It checks for secrets, input validation, and OWASP vulnerabilities based on `.agent/rules/security.md`.

### 4. Code Quality
**Prompt:**
> "Review my changes."

**What happens:**
- AntiGravity applies the **Coding Style** rules and **Code Review** workflow.
- It checks for immutability, naming conventions, and error handling.

## Troubleshooting

- **Agent ignores rules:**
  - Verify that the `.agent` folder is in the root of your workspace.
  - Explicitly reference the rule: *"Critique this code based on the coding-style rule."*

- **Workflows don't trigger:**
  - Ensure `.agent/workflows/*.md` files exist.
  - Try using the exact workflow name: *"Run the security-review workflow."*
