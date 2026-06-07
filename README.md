# tutorial-skill

一个 Claude Code skill，让你的 AI 自动生成**零基础也能看懂**的中文技术教程或讲义。

你只需要说一句话，比如"帮我写一个 Docker 入门教程"，它就会自动调研最新资料、设计大纲、生成完整内容、自查质量，最后保存为 `.md` 文件。

## 它能做什么？

| 类型 | 适合场景 | 例子 |
|------|---------|------|
| **概念理解型（讲义）** | 想让读者"理解原理" | Python for AI Agent、理解区块链 |
| **工具使用型（教程）** | 想让读者"学会操作" | Superpowers 使用教程、Git 入门 |
| **混合型** | 既讲原理又教操作 | Claude Code 完全指南 |

## 效果示例

用本 skill 生成的教程，每个概念都有生活类比、代码逐行注释、练习+答案：

```markdown
## 第2章 数据：Agent 的语言

### 🎯 为什么需要学这个？
Agent 之间传递信息需要一种统一格式。就像人类用中文交流，Agent 用 JSON 交流。

### 💡 一个类比
- 变量 = 快递柜（给包裹起个编号，存起来）
- 字典 = 快递单（收件人、地址、电话 —— 键值对）
- JSON = 快递单的标准格式（所有快递公司都认）

### ✏️ 小练习
1. 这条消息的"角色"是什么？
2. 大模型决定调用哪个工具？

<details>
<summary>📝 参考答案</summary>
...
</details>
```

完整示例：[python-for-ai-agent.md](https://github.com/YanZephyr14/tutorial-skill/blob/main/examples/python-for-ai-agent.md)

## 前置条件

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code/overview) 已安装
- [Tavily API Key](https://tavily.com)（免费注册，用于联网搜索最新资料）

## 安装

### 第 1 步：安装 Tavily MCP Server（推荐）

Tavily 让 skill 能联网搜索最新资料，确保内容准确。没有它也能用，但搜索效果会差很多。

```bash
# 注册 https://tavily.com 获取 API Key，然后运行：
claude mcp add --transport http tavily "https://mcp.tavily.com/mcp/?tavilyApiKey=你的API_KEY"
```

### 第 2 步：安装 skill

```bash
# 在你的项目目录下运行
mkdir -p .claude/skills/tutorial
curl -o .claude/skills/tutorial/SKILL.md https://raw.githubusercontent.com/YanZephyr14/tutorial-skill/main/SKILL.md
```

## 使用

在 Claude Code 中，用自然语言触发：

```
帮我写一个 Docker 零基础入门教程
```

```
我想做一个 Python for AI Agent 的讲义，面向没学过 Python 的人
```

```
帮我写一个 VS Code 使用教程，保存到 ./docs/
```

### 触发关键词

"写教程"、"写讲义"、"零基础"、"入门指南"、"使用教程"、"新手教程"、"从零开始学"、"通俗易懂"

### 输出

- 固定输出为 `.md` 文件
- 保存到你指定的目录
- 如果没指定路径，会询问你

## 工作流程

```
明确范围 → 联网调研 → 设计大纲（等你确认）→ 生成内容 → 自查 → 修复 → 保存 .md
```

1. **明确范围** — 从你的话中推断主题和类型，尽量不问问题
2. **联网调研** — 用 Tavily 搜索最新资料，确保信息准确
3. **设计大纲** — 生成大纲给你确认，确认后才开始写
4. **生成内容** — 一次性写完，包含练习和答案
5. **自查** — 检查正确性、结构、完整性
6. **修复** — 发现问题自动修复，直到自查通过
7. **保存** — 写入 `.md` 文件

## 设计理念

- **类比优先** — 每个概念都用生活中的事物类比（API = 餐厅点餐，循环 = 闹钟）
- **需求驱动** — 先讲"为什么需要"，再讲"这是什么"
- **真实案例** — 用读者正在接触的场景举例

## License

MIT
