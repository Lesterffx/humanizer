# humanizer

`humanizer` is a Codex Skill for improving Chinese writing so it sounds natural, specific, and human while preserving the original meaning.

This repository is a Codex-oriented adaptation of [op7418/Humanizer-zh](https://github.com/op7418/Humanizer-zh), which was originally packaged as a Claude Code Skill. The content is optimized here for Codex Skill structure, invocation, and public reuse.

## What It Does

Use `humanizer` when Chinese text feels too generic, mechanical, inflated, or template-like.

It helps with:

- polishing AI-assisted Chinese drafts
- reducing empty phrases, promotional tone, and formulaic structures
- making course notes, knowledge-base pages, chapter drafts, and documentation more readable
- preserving meaning while improving rhythm, specificity, and voice
- reviewing drafts for common LLM writing patterns

It is not intended for evading detectors, misrepresenting authorship, or bypassing review. Treat it as an editorial quality tool.

## Repository Structure

```text
humanizer/
├── SKILL.md
├── LICENSE
├── README.md
└── agents/
    └── openai.yaml
```

- `SKILL.md` contains the Codex Skill instructions and trigger metadata.
- `agents/openai.yaml` contains Codex UI metadata.
- `README.md` explains how to install and use the Skill.
- `LICENSE` preserves the upstream MIT license notice.

## Install

Copy this repository into your global Codex skills directory:

```text
<Codex home>/skills/humanizer
```

After installation, restart Codex so it can discover the new Skill.

The final folder should contain `SKILL.md` at the skill root:

```text
<Codex home>/skills/humanizer/SKILL.md
```

## Usage

### Explicit Invocation

```text
$humanizer 请把下面这段话改得更自然，保留原意，减少 AI 味：

[粘贴你的文本]
```

### Natural Language Invocation

```text
请用 humanizer 帮我润色这段中文，让它更像真人写的，并指出主要改动：

[粘贴你的文本]
```

### File Review Scenario

```text
请用 humanizer 审阅这个 Markdown 文件，把表达机械的段落改自然，但不要改标题结构：

[path/to/article.md]
```

When asking Codex to work on files, state whether it should edit the file directly or only provide suggestions.

## Examples

### Marketing Copy

Input:

```text
$humanizer

坐落在风景如画的杭州市中心，这家咖啡馆拥有丰富的文化底蕴和令人叹为观止的装饰。它作为城市咖啡文化的焦点，为顾客提供无缝、直观和充满活力的体验。
```

Possible output:

```text
这家咖啡馆在杭州市中心开了三年，以手冲咖啡和老建筑改造的空间出名。店里不大，靠窗的位置最受欢迎，周末通常要等位。
```

### Course Notes or Knowledge Pages

Input:

```text
请用 humanizer 改写这段知识库内容，让它更像课程笔记，不要太像宣传稿：

本方法论作为高阶建模能力的重要体现，展示了学习者在不断演变的知识格局中形成系统性认知的关键路径。
```

Possible output:

```text
这套方法主要训练一件事：把零散经验整理成可复用的模型。学习者不是多记几个概念，而是要能看出问题背后的结构。
```

### Formal Documentation

Input:

```text
请用 humanizer 帮我润色这段章节草稿。要求保留正式语气，但减少套话：

此外，该流程对于内容生产效率的提升具有至关重要的意义，并为后续自动化运营体系的构建奠定了坚实基础。
```

Possible output:

```text
这个流程可以减少重复沟通和返工，让选题、脚本、发布和复盘之间更容易衔接。后续如果要做自动化，也能直接沿用这些步骤。
```

## Output Modes

You can ask Codex to adjust how much explanation it provides:

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

## Difference From the Claude Code Version

This Codex version:

- uses `name: humanizer` in `SKILL.md`
- uses Codex-compatible frontmatter
- includes `agents/openai.yaml` for Codex UI metadata
- uses `$humanizer` or natural language prompts for invocation
- removes Claude Code specific installation and command examples
- keeps the original Chinese editing heuristics while adapting the packaging for Codex

## Credits

Adapted from [op7418/Humanizer-zh](https://github.com/op7418/Humanizer-zh), which translates and adapts ideas from [blader/humanizer](https://github.com/blader/humanizer) and references Wikipedia's "Signs of AI writing" guidance.

Practical checklist ideas also draw inspiration from [hardikpandya/stop-slop](https://github.com/hardikpandya/stop-slop).

## License

MIT. See `LICENSE`.
