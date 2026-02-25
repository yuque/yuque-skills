# Yuque Skills

[Agent Skills](https://agentskills.io) for [Yuque (语雀)](https://www.yuque.com) — give AI assistants the ability to work with your Yuque knowledge base.

[中文文档](./README.zh-CN.md)

## Prerequisites

- [yuque-mcp](https://github.com/yuque/yuque-mcp-server) server connected to your Yuque account

## Token Types

Yuque Skills are split into **Personal** and **Team** scenarios, each requiring a different Token:

| Token Type | Scope | Use Case |
|------------|-------|----------|
| Personal Token | Your own knowledge bases | Search, write, and manage your personal docs |
| Team Token | Team/group knowledge bases | Access team repos, member stats, group analytics. Requires group-level permissions. |

> 💡 Personal skills only need a personal Token. Team skills require a team Token with appropriate permissions (e.g., `statistic:read` for reports).

## Skills

### 🧑 Personal Skills

For individual use — works with your personal Yuque knowledge bases.

| Skill | Description |
|-------|-------------|
| [personal-search](skills/personal-search/) | Search your personal Yuque docs with natural language and get summarized answers |
| [personal-meeting-notes](skills/personal-meeting-notes/) | Format and archive meeting notes to your personal Yuque |
| [personal-weekly](skills/personal-weekly/) | Generate personal weekly reports from your documentation activity |
| [personal-tech-design](skills/personal-tech-design/) | Write technical design docs and save to your personal repo |

### 👥 Team Skills

For team use — works with team/group Yuque knowledge bases. Requires team Token.

| Skill | Description |
|-------|-------------|
| [team-search](skills/team-search/) | Search team Yuque docs with natural language and get summarized answers |
| [team-meeting-notes](skills/team-meeting-notes/) | Format and archive meeting notes to team Yuque |
| [team-weekly](skills/team-weekly/) | Generate team weekly reports from Yuque activity data and member contributions |
| [team-tech-design](skills/team-tech-design/) | Write technical design docs and save to team repo with review workflow |
| [team-onboarding](skills/team-onboarding/) | Generate onboarding reading guides for new team members |
| [team-knowledge-report](skills/team-knowledge-report/) | Generate monthly knowledge management reports with team analytics |

## Install

Each skill is a standalone folder with a `SKILL.md` file.

### Claude Code

```bash
# Download a single skill
curl -sL https://raw.githubusercontent.com/yuque/yuque-skills/main/skills/personal-search/SKILL.md \
  -o .claude/skills/personal-search.md
```

### Cursor

```bash
curl -sL https://raw.githubusercontent.com/yuque/yuque-skills/main/skills/personal-search/SKILL.md \
  -o .cursor/skills/personal-search.md
```

### Other tools

```bash
# Clone and copy the skill you need
git clone https://github.com/yuque/yuque-skills.git
cp -r yuque-skills/skills/personal-search /path/to/your/skills/
```

Replace `personal-search` with any skill name from the tables above.

## Related

- [Yuque AI Ecosystem](https://yuque.github.io/yuque-ecosystem/) — Website
- [yuque-mcp](https://github.com/yuque/yuque-mcp-server) — MCP server for Yuque

## License

Apache-2.0
