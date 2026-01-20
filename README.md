# Everything AntiGravity

**The ultimate configuration collection for AntiGravity (Gemini), combining [Everything Claude Code](https://github.com/affaan-m/everything-claude-code), [AntiGravity Awesome Skills](https://github.com/sickn33/antigravity-awesome-skills), and [Gemini Superpowers](https://github.com/anthonylee991/gemini-superpowers-antigravity).**

This repository transforms your AntiGravity agent into an expert engineer, security researcher, and product manager.

## 🚀 Features

### 🧠 Extensive Skill Library (`.agent/skills/`)
Over 50+ domain-specific skills including:
- **Engineering**: `backend-dev-guidelines`, `frontend-patterns`, `tdd`, `react-ui-patterns`
- **Security**: `pentest-checklist`, `aws-penetration-testing`, `owasp-top-10`, `api-fuzzing`
- **Product**: `product-manager-toolkit`, `pricing-strategy`, `launch-strategy`
- **Design**: `ui-ux-pro-max`, `frontend-design`, `mobile-design`
- **Marketing**: `copywriting`, `seo-audit`, `social-content`

### ⚡ Superpowered Workflows (`.agent/workflows/`)
Automated processes to guide complex tasks:
- **`/superpowers-plan`**: Create detailed implementation plans with verification steps.
- **`/superpowers-review`**: Automated code review with severity levels.
- **`/superpowers-tdd`**: Guided Test-Driven Development sessions.
- **`/security-review`**: Comprehensive security auditing.
- **`/architect-review`**: High-level system architecture analysis.

### 🛡️ Unbreakable Rules (`.agent/rules/`)
- **`coding-style.md`**: Enforces type safety, error handling, and immutability.
- **`security.md`**: Prevents common vulnerabilities like SQLi and hardcoded secrets.
- **`superpowers.md`**: Activates advanced reasoning and verify-before-commit behaviors.

## 🛠️ Installation

Simply copy the `.agent` directory to your project root.

```bash
cp -r /path/to/every-thing-antigravity/.agent /your/project/root/
```

## 📖 Usage

### Using Skills
AntiGravity effectively "knows" these skills. You can ask it to:
- "Audit this file for security vulnerabilities" (Trigger: `security-scanning`)
- "Help me design a pricing page" (Trigger: `pricing-strategy`)
- "Write a marketing email for this feature" (Trigger: `email-systems`)

### Using Workflows
Type the workflow name / slash command in the chat:
- "Run a security review" or `/security-review`
- "Plan the new feature" or `/superpowers-plan`

##  CREDITS

Aggregated and adapted from:
- [affaan-m/everything-claude-code](https://github.com/affaan-m/everything-claude-code)
- [sickn33/antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills)
- [anthonylee991/gemini-superpowers-antigravity](https://github.com/anthonylee991/gemini-superpowers-antigravity)
