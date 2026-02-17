# yuque-skills

> Agent Skills for [Yuque (语雀)](https://www.yuque.com) — Let AI assistants work better with Yuque.

[中文文档](./README.zh-CN.md)

## What is this?

This repository provides a collection of [Agent Skills](https://agentskills.io) for Yuque — the popular Chinese knowledge management platform. Agent Skills is an open standard by Anthropic, supported by Claude Code, Cursor, Gemini CLI, and other AI tools.

Each skill teaches an AI assistant how to perform a specific Yuque workflow: searching docs, writing meeting notes, generating reports, and more.

## Prerequisites

- A running [yuque-mcp](https://github.com/chen201724/yuque-mcp) server connected to your Yuque account
- An AI tool that supports Agent Skills (Claude Code, Cursor, etc.)

## Skills

| Skill | Description | Use When |
|-------|-------------|----------|
| [smart-search](./skills/smart-search/) | Search Yuque docs with natural language and get summarized answers | You need to find information across your Yuque knowledge base |
| [meeting-notes](./skills/meeting-notes/) | Format and archive meeting notes to Yuque | After a meeting, you want structured notes saved to Yuque |
| [weekly-report](./skills/weekly-report/) | Generate team weekly reports from Yuque activity data | End of week, need a summary of team documentation activity |
| [tech-design](./skills/tech-design/) | Write technical design docs using a standard template | Starting a new feature/project that needs a design document |
| [onboarding-guide](./skills/onboarding-guide/) | Generate onboarding reading guides from team knowledge bases | A new team member joins and needs a curated reading list |
| [knowledge-report](./skills/knowledge-report/) | Generate monthly knowledge management reports | Monthly review of team knowledge base health and activity |

## Installation

### Claude Code

```bash
# Option 1: Register as a plugin marketplace, then browse and install
/plugin marketplace add chen201724/yuque-skills

# Option 2: Clone locally and use directly
git clone https://github.com/chen201724/yuque-skills.git
# Skills will be auto-discovered from SKILL.md files in your project
```

### Cursor / Other Tools

Follow your tool's documentation for installing Agent Skills. The skills are standard `.skill` directories with `SKILL.md` files.

## Related Projects

- [yuque-mcp](https://github.com/chen201724/yuque-mcp) — MCP server for Yuque API
- [yuque-ecosystem](https://github.com/chen201724/yuque-ecosystem) — Curated list of Yuque tools and integrations

## License

Apache-2.0
