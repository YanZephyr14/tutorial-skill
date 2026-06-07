# tutorial-skill

一个 Claude Code skill，用于为零基础用户生成高质量的中文技术教程或讲义。

## 功能

- **概念理解型（讲义）**：如"理解 AI Agent"、"理解 Docker"
- **工具使用型（教程）**：如"Superpowers 使用教程"、"Git 入门指南"
- **混合型**：既讲原理又教操作

## 依赖

本 skill 在写作前会联网调研最新资料，需要以下 MCP 工具支持：

| 工具 | 用途 | 必需？ |
|------|------|--------|
| [Tavily MCP Server](https://github.com/tavily-ai/tavily-mcp) | 搜索最新信息（首选） | 推荐 |
| WebFetch | 抓取官方文档 | 内置 |
| Context7 | 查询编程库/框架文档 | 可选 |

**安装 Tavily MCP Server：**

```bash
claude mcp add --transport http tavily "https://mcp.tavily.com/mcp/?tavilyApiKey=你的API_KEY"
```

API Key 在 [tavily.com](https://tavily.com) 注册获取（有免费额度）。

> 如果没有 Tavily，skill 会降级使用 WebFetch 和 Context7，但搜索效果会打折扣。

## 安装

将 `SKILL.md` 放到项目的 `.claude/skills/tutorial/` 目录下：

```bash
mkdir -p .claude/skills/tutorial
cp SKILL.md .claude/skills/tutorial/
```

## 使用

当你说以下关键词时会自动触发：

- "写教程"、"写讲义"
- "零基础"、"入门指南"
- "使用教程"、"新手教程"
- "从零开始学"、"通俗易懂"

## 核心理念

1. **类比优先** — 每个概念都用生活中的事物类比
2. **需求驱动** — 先讲"为什么需要"，再讲"这是什么"
3. **真实案例** — 用读者正在接触的真实场景举例

## 工作流程

```
明确范围 → 联网调研 → 设计大纲（用户确认）→ 生成内容 → 自查 → 修复 → 保存 .md
```

## License

MIT
