# Yuque Skills

面向[语雀](https://www.yuque.com)的 [Agent Skills](https://agentskills.io) — 让 AI 助手更好地使用你的语雀知识库。

[English](./README.md)

## 前置条件

- 运行中的 [yuque-mcp](https://github.com/chen201724/yuque-mcp-server) 服务，已连接你的语雀账号

## Skills 列表

| Skill | 描述 |
|-------|------|
| [smart-search](skills/smart-search/) | 用自然语言搜索语雀文档并总结要点 |
| [meeting-notes](skills/meeting-notes/) | 整理会议内容为标准格式并归档到语雀 |
| [weekly-report](skills/weekly-report/) | 基于语雀活动数据生成团队周报 |
| [tech-design](skills/tech-design/) | 按标准模板撰写技术方案文档 |
| [onboarding-guide](skills/onboarding-guide/) | 自动整理团队核心文档生成入职阅读指南 |
| [knowledge-report](skills/knowledge-report/) | 全面分析团队知识管理数据并生成月报 |

## 安装

每个 Skill 是一个独立的文件夹，包含 `SKILL.md` 文件。

### Claude Code

```bash
# 下载单个 skill
curl -sL https://raw.githubusercontent.com/chen201724/yuque-skills/main/skills/smart-search/SKILL.md \
  -o .claude/skills/smart-search.md
```

### Cursor

```bash
curl -sL https://raw.githubusercontent.com/chen201724/yuque-skills/main/skills/smart-search/SKILL.md \
  -o .cursor/skills/smart-search.md
```

### 其他工具

```bash
# 克隆仓库，复制需要的 skill
git clone https://github.com/chen201724/yuque-skills.git
cp -r yuque-skills/skills/smart-search /path/to/your/skills/
```

将 `smart-search` 替换为上表中任意 skill 名称。

## 相关项目

- [语雀 AI 生态官网](https://chen201724.github.io/yuque-ecosystem/) — 官网
- [yuque-mcp](https://github.com/chen201724/yuque-mcp-server) — 语雀 MCP 服务

## 许可证

Apache-2.0
