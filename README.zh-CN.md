# yuque-skills

> [语雀](https://www.yuque.com) Agent Skills — 让 AI 助手更好地使用语雀

[English](./README.md)

## 这是什么？

本仓库提供了一组面向语雀的 [Agent Skills](https://agentskills.io)。Agent Skills 是 Anthropic 发布的开放标准，被 Claude Code、Cursor、Gemini CLI 等主流 AI 工具支持。

每个 Skill 教会 AI 助手如何完成一个具体的语雀工作流：搜索文档、写会议纪要、生成报告等。

## 前置条件

- 运行中的 [yuque-mcp](https://github.com/chen201724/yuque-mcp) 服务，已连接你的语雀账号
- 支持 Agent Skills 的 AI 工具（Claude Code、Cursor 等）

## Skills 列表

| Skill | 描述 | 适用场景 |
|-------|------|----------|
| [smart-search](./skills/smart-search/) | 用自然语言搜索语雀文档并总结要点 | 需要在语雀知识库中查找信息 |
| [meeting-notes](./skills/meeting-notes/) | 整理会议内容为标准格式并归档到语雀 | 会议结束后，需要结构化的会议纪要 |
| [weekly-report](./skills/weekly-report/) | 基于语雀活动数据生成团队周报 | 每周末，需要团队文档活动总结 |
| [tech-design](./skills/tech-design/) | 按标准模板撰写技术方案文档 | 新功能/项目需要技术方案 |
| [onboarding-guide](./skills/onboarding-guide/) | 自动整理团队核心文档生成入职阅读指南 | 新人入职，需要定制阅读清单 |
| [knowledge-report](./skills/knowledge-report/) | 全面分析团队知识管理数据并生成月报 | 每月回顾团队知识库健康度和活跃度 |

## 安装使用

### Claude Code

```bash
# 方式 1：注册为插件市场，然后浏览安装
/plugin marketplace add chen201724/yuque-skills

# 方式 2：克隆到本地直接使用
git clone https://github.com/chen201724/yuque-skills.git
# Claude Code 会自动发现项目中的 SKILL.md 文件
```

### Cursor / 其他工具

参考你所用工具的文档安装 Agent Skills。每个 skill 都是标准的目录结构，包含 `SKILL.md` 文件。

## 相关项目

- [yuque-mcp](https://github.com/chen201724/yuque-mcp) — 语雀 MCP 服务
- [yuque-ecosystem](https://github.com/chen201724/yuque-ecosystem) — 语雀工具生态汇总

## 许可证

Apache-2.0
