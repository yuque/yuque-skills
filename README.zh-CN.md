# Yuque Skills

面向[语雀](https://www.yuque.com)的 [Agent Skills](https://agentskills.io) — 让 AI 助手更好地使用你的语雀知识库。

[English](./README.md)

## 前置条件

- 运行中的 [yuque-mcp](https://github.com/yuque/yuque-mcp-server) 服务，已连接你的语雀账号

## Token 类型说明

Yuque Skills 按**个人**和**团队**场景拆分，分别需要不同的 Token：

| Token 类型 | 作用范围 | 使用场景 |
|-----------|---------|---------|
| 个人 Token | 你自己的知识库 | 搜索、写入、管理个人文档 |
| 团队 Token | 团队/组织知识库 | 访问团队知识库、成员统计、团队分析。需要团队级别权限。 |

> 💡 个人系列 Skills 只需个人 Token。团队系列 Skills 需要团队 Token 并配置相应权限（如报表类需要 `statistic:read` 权限）。

## Skills 列表

### 🧑 个人 Skills

面向个人使用 — 操作你的个人语雀知识库。

| Skill | 描述 |
|-------|------|
| [personal-search](skills/personal-search/) | 用自然语言搜索个人语雀文档并总结要点 |
| [personal-meeting-notes](skills/personal-meeting-notes/) | 整理会议内容为标准格式并归档到个人语雀 |
| [personal-weekly](skills/personal-weekly/) | 基于个人文档活动数据生成个人周报 |
| [personal-tech-design](skills/personal-tech-design/) | 按标准模板撰写技术方案文档并存到个人知识库 |

### 👥 团队 Skills

面向团队使用 — 操作团队/组织语雀知识库。需要团队 Token。

| Skill | 描述 |
|-------|------|
| [team-search](skills/team-search/) | 用自然语言搜索团队语雀文档并总结要点 |
| [team-meeting-notes](skills/team-meeting-notes/) | 整理会议内容为标准格式并归档到团队语雀 |
| [team-weekly](skills/team-weekly/) | 基于语雀团队活动数据和成员贡献生成团队周报 |
| [team-tech-design](skills/team-tech-design/) | 按标准模板撰写技术方案文档并存到团队知识库（含评审流程） |
| [team-onboarding](skills/team-onboarding/) | 自动整理团队核心文档生成新人入职阅读指南 |
| [team-knowledge-report](skills/team-knowledge-report/) | 全面分析团队知识管理数据并生成月报 |

## 安装

每个 Skill 是一个独立的文件夹，包含 `SKILL.md` 文件。

### Claude Code

```bash
# 下载单个 skill
curl -sL https://raw.githubusercontent.com/yuque/yuque-skills/main/skills/personal-search/SKILL.md \
  -o .claude/skills/personal-search.md
```

### Cursor

```bash
curl -sL https://raw.githubusercontent.com/yuque/yuque-skills/main/skills/personal-search/SKILL.md \
  -o .cursor/skills/personal-search.md
```

### 其他工具

```bash
# 克隆仓库，复制需要的 skill
git clone https://github.com/yuque/yuque-skills.git
cp -r yuque-skills/skills/personal-search /path/to/your/skills/
```

将 `personal-search` 替换为上表中任意 skill 名称。

## 相关项目

- [语雀 AI 生态官网](https://yuque.github.io/yuque-ecosystem/) — 官网
- [yuque-mcp](https://github.com/yuque/yuque-mcp-server) — 语雀 MCP 服务

## 许可证

Apache-2.0
