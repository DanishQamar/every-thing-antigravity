# AntiGravity Hooks Guide

In 'Everything Claude Code', hooks are used to automate actions like pre-commit checks or formatting.

In **AntiGravity**, while there isn't a direct `hooks.json` equivalent exposed yet, you can achieve similar results by incorporating these checks into your workflows or manual routines.

## Recommended "Hooks"

### Pre-Commit Review
Before running `git push`, manually verify:
- [ ] No `console.log` statements left.
- [ ] Code is formatted (e.g., `prettier --write .`).
- [ ] Tests pass (e.g., `npm test`).

### Auto-Format
When editing files, you can ask AntiGravity to "format this file" or include formatting steps in your workflows.

### Safety Checks
The `security-review` workflow acts as a comprehensive "hook" that you should run proactively before major releases.
