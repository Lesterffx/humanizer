# humanizer

`humanizer` 是一个面向 Codex 的中文写作润色 Skill，用于在保留原意和事实信息的前提下，让文本更自然、更具体、更像真人写作。

本仓库是基于 [op7418/Humanizer-zh](https://github.com/op7418/Humanizer-zh) 改造的 Codex 版适配。原项目是 Claude Code Skill 版；本仓库针对 Codex 的 Skill 结构、触发方式和公开复用场景进行了整理。

## 功能说明

当中文文本显得过于空泛、机械、夸张或模板化时，可以使用 `humanizer` 进行编辑。

它适合处理：

- AI 辅助生成后的中文草稿润色
- 章节草稿、课程笔记、知识库页面和说明文档优化
- 营销文案、正式说明、项目介绍中的套话压缩
- 宣传腔、三段式排比、模糊归因、过度强调意义等常见模式修正
- 在保留原意的同时，改善句子节奏、细节密度和表达语气

它不是用来规避检测、伪造作者身份或绕过审核的工具。更合适的定位是：一个帮助中文文本减少模板味、提升编辑质量的 Codex Skill。

## 仓库结构

```text
humanizer/
├── SKILL.md
├── LICENSE
├── README.md
└── agents/
    └── openai.yaml
```

文件说明：

- `SKILL.md`：Codex 真正读取的 Skill 指令和触发元数据。
- `agents/openai.yaml`：Codex UI 展示信息。
- `README.md`：给用户看的安装和使用说明。
- `LICENSE`：MIT License。

## 安装方式

将本仓库复制到你的 Codex 全局 Skills 目录中：

```text
<Codex home>/skills/humanizer
```

安装完成后，目录中应包含：

```text
<Codex home>/skills/humanizer/SKILL.md
```

然后重启 Codex，让 Codex 重新发现这个 Skill。

## 使用方式

### 显式调用

```text
$humanizer 请把下面这段话改得更自然，保留原意，减少 AI 味：

[粘贴你的文本]
```

### 自然语言调用

```text
请用 humanizer 帮我润色这段中文，让它更像真人写的，并指出主要改动：

[粘贴你的文本]
```

### 文件审阅场景

```text
请用 humanizer 审阅这个 Markdown 文件，把表达机械的段落改自然，但不要改标题结构：

[path/to/article.md]
```

如果让 Codex 处理文件，建议同时说明：

- 是否允许直接修改文件
- 是否只需要给出改写建议
- 是否需要保留标题、列表、引用、表格等结构
- 是否需要输出修改摘要或评分

## 示例

### 示例 1：营销文案

输入：

```text
$humanizer

坐落在风景如画的杭州市中心，这家咖啡馆拥有丰富的文化底蕴和令人叹为观止的装饰。它作为城市咖啡文化的焦点，为顾客提供无缝、直观和充满活力的体验。
```

可能输出：

```text
这家咖啡馆在杭州市中心开了三年，以手冲咖啡和老建筑改造的空间出名。店里不大，靠窗的位置最受欢迎，周末通常要等位。
```

### 示例 2：课程笔记或知识库页面

输入：

```text
请用 humanizer 改写这段知识库内容，让它更像课程笔记，不要太像宣传稿：

本方法论作为高阶建模能力的重要体现，展示了学习者在不断演变的知识格局中形成系统性认知的关键路径。
```

可能输出：

```text
这套方法主要训练一件事：把零散经验整理成可复用的模型。学习者不是多记几个概念，而是要能看出问题背后的结构。
```

### 示例 3：正式说明或章节草稿

输入：

```text
请用 humanizer 帮我润色这段章节草稿。要求保留正式语气，但减少套话：

此外，该流程对于内容生产效率的提升具有至关重要的意义，并为后续自动化运营体系的构建奠定了坚实基础。
```

可能输出：

```text
这个流程可以减少重复沟通和返工，让选题、脚本、发布和复盘之间更容易衔接。后续如果要做自动化，也能直接沿用这些步骤。
```

## 输出模式

你可以要求 Codex 控制解释的详细程度：

```text
只给我改写后的正文，不要解释。
```

```text
请先列出 AI 味最重的 5 个问题，再给改写版。
```

```text
请给出改写版，并用 3 条说明你改了什么。
```

```text
请按 humanizer 的 50 分评分表评估这段文字，并给出修改建议。
```

## 与 Claude Code 版的区别

这个 Codex 版做了以下适配：

- `SKILL.md` 中使用 `name: humanizer`。
- 使用 Codex 兼容的 frontmatter。
- 增加 `agents/openai.yaml`，用于 Codex UI 展示。
- 使用 `$humanizer` 或自然语言请求触发。
- 移除了 Claude Code 专用的安装说明和命令示例。
- 保留原中文编辑启发式规则，但将打包方式改为 Codex Skill。

## 来源与致谢

本仓库改造自 [op7418/Humanizer-zh](https://github.com/op7418/Humanizer-zh)。该项目翻译和整理了 [blader/humanizer](https://github.com/blader/humanizer) 的思路，并参考了 Wikipedia 的 "Signs of AI writing" 指南。

实用检查清单的思路也参考了 [hardikpandya/stop-slop](https://github.com/hardikpandya/stop-slop)。

## 许可证

本项目使用 MIT License，见 `LICENSE`。
