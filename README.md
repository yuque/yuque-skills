# Yuque Skills

[Agent Skills](https://agentskills.io) for [Yuque (语雀)](https://www.yuque.com) — give AI assistants the ability to work with your Yuque knowledge base.

[中文文档](./README.zh-CN.md)

## Prerequisites

- [yuque-mcp](https://github.com/chen201724/yuque-mcp-server) server connected to your Yuque account

## Skills

| Skill | Description |
|-------|-------------|
| [smart-search](skills/smart-search/) | Search Yuque docs with natural language and get summarized answers |
| [meeting-notes](skills/meeting-notes/) | Format and archive meeting notes to Yuque |
| [weekly-report](skills/weekly-report/) | Generate team weekly reports from Yuque activity data |
| [tech-design](skills/tech-design/) | Write technical design docs using a standard template |
| [onboarding-guide](skills/onboarding-guide/) | Generate onboarding reading guides for new team members |
| [knowledge-report](skills/knowledge-report/) | Generate monthly knowledge management reports |

## Install

Each skill is a standalone folder with a `SKILL.md` file.

### Claude Code

```bash
# Download a single skill
curl -sL https://raw.githubusercontent.com/chen201724/yuque-skills/main/skills/smart-search/SKILL.md \
  -o .claude/skills/smart-search.md
```

### Cursor

```bash
curl -sL https://raw.githubusercontent.com/chen201724/yuque-skills/main/skills/smart-search/SKILL.md \
  -o .cursor/skills/smart-search.md
```

### Other tools

```bash
# Clone and copy the skill you need
git clone https://github.com/chen201724/yuque-skills.git
cp -r yuque-skills/skills/smart-search /path/to/your/skills/
```

Replace `smart-search` with any skill name from the table above.

## Related

- [Yuque AI Ecosystem](https://chen201724.github.io/yuque-ecosystem/) — Website
- [yuque-mcp](https://github.com/chen201724/yuque-mcp-server) — MCP server for Yuque

## License

Apache-2.0
