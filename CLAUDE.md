# Fjellferdigheter - Claude Plugin Marketplace

This repository is a **company-wide Claude plugin marketplace** for Fjellvarden. It contains multiple skills, commands, plugins, and tools designed to be installed and used across the organization via Claude Code's plugin system.

## Repository Structure

- `.claude-plugin/marketplace.json` — Marketplace configuration (owner: Fjellvarden, hei@fjellvarden.no)
- `.ai/` — Internal documentation and process descriptions (e.g., `tjeneste.md` for service page workflows)
- `skills/` — Individual skill definitions, each with a `SKILL.md` file containing YAML frontmatter and instructions

## How It Works

Skills are registered in the marketplace and can be installed via:
```
/plugin marketplace add fjellvarden/fjellferdigheter
```

Each skill is a folder under `skills/` with a `SKILL.md` file following the standard format:
```markdown
---
name: skill-name
description: What the skill does and when to trigger it
---
Instructions for Claude...
```

## Language

The primary working language is **Norwegian (Bokmål)**. Documentation and customer-facing content should be in Norwegian unless otherwise specified. Internal technical docs and skill definitions may use English.
