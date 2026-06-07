# tutorial-skill

一个 AI skill，让你的 AI 自动生成**零基础也能看懂**的中文技术教程或讲义。

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

## 前置条件

- 支持 skill 的 AI 编程工具（Claude Code、Cursor 等）
- 联网搜索工具（推荐 Tavily，见下方）

## 联网搜索工具

本 skill 在写作前会联网调研最新资料，需要以下工具支持：

| 工具 | 用途 | 项目地址 |
|------|------|---------|
| **Tavily**（推荐） | 搜索最新信息，效果最好 | [github.com/tavily-ai/tavily-mcp](https://github.com/tavily-ai/tavily-mcp) |
| **Context7**（可选） | 查询编程库/框架最新文档 | [github.com/upstash/context7](https://github.com/upstash/context7) |

> 如果没有这些工具，可以在 SKILL.md 中替换成你有的搜索工具，见下方「自定义」章节。

## 安装

### 方法一：命令行安装

```bash
mkdir -p .claude/skills/tutorial
curl -o .claude/skills/tutorial/SKILL.md https://raw.githubusercontent.com/YanZephyr14/tutorial-skill/main/SKILL.md
```

### 方法二：手动安装

1. 下载本仓库的 `SKILL.md` 文件
2. 在你的项目中创建 `.claude/skills/tutorial/` 目录
3. 将 `SKILL.md` 放入该目录

```
你的项目/
└── .claude/
    └── skills/
        └── tutorial/
            └── SKILL.md
```

## 使用

用自然语言触发：

```
帮我写一个 Docker 零基础入门教程
```

```
我想做一个 Python for AI Agent 的讲义，面向没学过 Python 的人
```

```
帮我写一个 VS Code 使用教程，保存到 ./docs/
```

**触发关键词：** "写教程"、"写讲义"、"零基础"、"入门指南"、"使用教程"、"新手教程"、"从零开始学"、"通俗易懂"

**输出：** 固定为 `.md` 文件，保存到你指定的目录。

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

## 自定义

### 替换搜索工具

SKILL.md 中的调研方式可以替换成你有的工具。打开 SKILL.md，找到这段：

```markdown
**调研方式：**
- 用 Tavily 搜索最新信息（首选）
- 用 WebFetch 抓取官方文档
- 用 Context7 查询编程库文档
```

改成你有的工具即可，比如：

```markdown
**调研方式：**
- 用 WebFetch 抓取官方文档
- 用 WebSearch 搜索最新信息
```

### 修改写作风格

编辑 SKILL.md 末尾的「写作要点」部分即可。

## 设计理念

- **类比优先** — 每个概念都用生活中的事物类比（API = 餐厅点餐，循环 = 闹钟）
- **需求驱动** — 先讲"为什么需要"，再讲"这是什么"
- **真实案例** — 用读者正在接触的场景举例

## License

MIT
