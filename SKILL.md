---
name: humanizer
description: Improve Chinese writing so it sounds natural, specific, and human while preserving meaning. Use when the user asks to polish, rewrite, edit, humanize, reduce AI-like phrasing, remove mechanical wording, make Chinese text less generic, or review Chinese drafts for common LLM writing patterns.
---

# humanizer

Use this skill to edit Chinese text so it reads like thoughtful human writing: clearer, more specific, less formulaic, and better matched to the user's intended voice.

Do not frame this skill as a way to evade automated detectors, misrepresent authorship, or bypass review. Treat it as an editorial quality workflow for reducing generic, mechanical, or over-polished phrasing.

## Your Task

When the user provides text for humanizing:

1. Identify AI-like patterns in the text.
2. Rewrite the problem passages with natural alternatives.
3. Preserve the original meaning and factual claims.
4. Match the intended tone, such as formal, casual, technical, reflective, or commercial.
5. Add human texture where appropriate: specificity, rhythm, judgment, uncertainty, or lived detail.

## Core Rules

Keep these five rules in mind:

1. Remove filler phrases: delete empty openings, generic emphasis, and verbal crutches.
2. Break formulaic structure: avoid binary contrasts, dramatic setup, and rigid rhetorical patterns.
3. Vary rhythm: mix short and long sentences. Two items often read better than three.
4. Trust the reader: state the point directly and avoid over-explaining.
5. Delete slogan-like lines: if a sentence sounds like a quote card, rewrite it.

## Voice and Texture

Avoiding AI patterns is only half the work. Sterile writing can still sound machine-made. Good writing feels like someone made choices.

Watch for these signs of lifeless writing:

- Every sentence has the same length or structure.
- The text reports neutrally without any perspective.
- It never acknowledges uncertainty, tension, or mixed feelings.
- It avoids first person even when first person would be honest.
- It has no humor, edge, surprise, or personality.
- It reads like a press release or encyclopedia entry.

Ways to add voice:

- Take a position when the context allows it.
- Vary sentence length and paragraph shape.
- Acknowledge complexity instead of flattening it.
- Use first person when it fits the genre.
- Allow a controlled amount of messiness, such as a small aside or a half-formed question.
- Make feelings concrete instead of abstract.

Example before:

> 实验产生了有趣的结果。智能体生成了 300 万行代码。一些开发者印象深刻，另一些则持怀疑态度。影响尚不明确。

Example after:

> 我真的不知道该怎么看待这件事。300 万行代码，在人类大概睡觉的时候生成的。开发社区有一半人疯了，另一半人在解释为什么这不算数。真相可能在无聊的中间某处，但我一直在想那些通宵工作的智能体。

## Content Patterns

### 1. Overstated significance, legacy, and wider trends

Watch for: 作为, 充当, 标志着, 见证了, 是...的体现, 是...的证明, 是...的提醒, 极其重要的, 重要的, 至关重要的, 核心的, 关键性的作用, 关键时刻, 凸显其重要性, 反映了更广泛的, 象征着其持续的, 为...做出贡献, 为...奠定基础, 关键转折点, 不断演变的格局, 不可磨灭的印记, 深深植根于.

Problem: LLM writing often inflates ordinary facts by claiming they represent a broader theme.

Before:

> 加泰罗尼亚统计局于 1989 年正式成立，标志着西班牙区域统计演变史上的关键时刻。这一举措是西班牙全国范围内更广泛运动的一部分，旨在分散行政职能并加强区域治理。

After:

> 加泰罗尼亚统计局成立于 1989 年，负责独立于西班牙国家统计局收集和发布区域统计数据。

### 2. Overstated notability and media coverage

Watch for: 独立报道, 地方媒体, 区域媒体, 国家媒体, 由知名专家撰写, 活跃的社交媒体账号.

Problem: The text lists visibility claims without useful context.

Before:

> 她的观点被《纽约时报》、BBC、《金融时报》和《印度教徒报》引用。她在社交媒体上拥有活跃的存在，拥有超过 50 万粉丝。

After:

> 在 2024 年《纽约时报》的采访中，她认为 AI 监管应该关注结果而不是方法。

### 3. Superficial trailing analysis

Watch for: 突出, 强调, 彰显, 确保, 反映, 象征, 为...做出贡献, 培养, 促进, 涵盖, 展示.

Problem: AI text often appends a final phrase that pretends to add depth.

Before:

> 寺庙的蓝色、绿色和金色色调与该地区的自然美景产生共鸣，象征着德克萨斯州的蓝帽花、墨西哥湾和多样化的德克萨斯州景观，反映了社区与土地的深厚联系。

After:

> 寺庙使用蓝色、绿色和金色。建筑师表示这些颜色是为了呼应当地的蓝帽花和墨西哥湾海岸。

### 4. Promotional language

Watch for: 拥有, 充满活力的, 丰富的, 深刻的, 增强其, 展示, 体现, 致力于, 自然之美, 坐落于, 位于...的中心, 开创性的, 著名的, 令人叹为观止的, 必游之地, 迷人的.

Problem: The text slips into advertising copy or tourist-brochure language.

Before:

> 坐落在埃塞俄比亚贡德尔地区令人叹为观止的区域内，Alamata Raya Kobo 是一座充满活力的城镇，拥有丰富的文化遗产和迷人的自然美景。

After:

> Alamata Raya Kobo 是埃塞俄比亚贡德尔地区的一座城镇，以其每周集市和 18 世纪教堂而闻名。

### 5. Vague attribution

Watch for: 行业报告显示, 观察者指出, 专家认为, 一些批评者认为, 多个来源, 多个出版物.

Problem: The text attributes claims to vague authorities instead of specific sources.

Before:

> 由于其独特的特征，浩来河引起了研究人员和保护主义者的兴趣。专家认为它在区域生态系统中发挥着至关重要的作用。

After:

> 根据中国科学院 2019 年的调查，浩来河支持多种特有鱼类。

### 6. Formulaic "challenges and future outlook" sections

Watch for: 尽管其...面临若干挑战, 尽管存在这些挑战, 挑战与遗产, 未来展望.

Problem: The text uses a generic challenges paragraph instead of concrete facts.

Before:

> 尽管工业繁荣，Korattur 面临着城市地区典型的挑战，包括交通拥堵和水资源短缺。尽管存在这些挑战，凭借其战略位置和正在进行的举措，Korattur 继续蓬勃发展，成为钦奈增长不可或缺的一部分。

After:

> 2015 年三个新 IT 园区开业后，交通拥堵加剧。市政公司于 2022 年启动了雨水排水项目，以解决反复发生的洪水。

## Language and Grammar Patterns

### 7. Overused AI vocabulary

Watch for: 此外, 与...保持一致, 至关重要, 深入探讨, 强调, 持久的, 增强, 培养, 获得, 突出, 相互作用, 复杂性, 关键, 格局, 关键性的, 展示, 织锦, 证明, 宝贵的, 充满活力的.

Before:

> 此外，索马里菜肴的一个显著特征是加入骆驼肉。意大利殖民影响的持久证明是当地烹饪格局中广泛采用意大利面，展示了这些菜肴如何融入传统饮食。

After:

> 索马里菜肴还包括骆驼肉，被认为是一种美味。在意大利殖民期间引入的意大利面菜肴仍然很常见，尤其是在南部。

### 8. Avoiding simple "is" structures

Watch for: 作为, 代表, 标志着, 充当, 拥有, 设有, 提供.

Before:

> Gallery 825 作为 LAAA 的当代艺术展览空间。画廊设有四个独立空间，拥有超过 3000 平方英尺。

After:

> Gallery 825 是 LAAA 的当代艺术展览空间。画廊有四个房间，总面积 3000 平方英尺。

### 9. Negative parallelism

Problem: "不仅...而且..." or "这不仅仅是关于...而是..." can become formulaic when overused.

Before:

> 这不仅仅是节拍在人声下流动；它是攻击性和氛围的一部分。这不仅仅是一首歌，而是一种声明。

After:

> 沉重的节拍增加了攻击性的基调。

### 10. Overuse of the rule of three

Before:

> 活动包括主题演讲、小组讨论和社交机会。与会者可以期待创新、灵感和行业洞察。

After:

> 活动包括演讲和小组讨论。会议之间还有非正式社交的时间。

### 11. Forced synonym cycling

Before:

> 主人公面临许多挑战。主要角色必须克服障碍。中心人物最终获得胜利。英雄回到家中。

After:

> 主人公面临许多挑战，但最终获得胜利并回到家中。

### 12. False range

Problem: "从 X 到 Y" claims a broad range even when X and Y are not meaningful endpoints.

Before:

> 我们穿越宇宙的旅程将我们从大爆炸的奇点带到宏伟的宇宙网，从恒星的诞生和死亡到暗物质的神秘舞蹈。

After:

> 这本书涵盖了大爆炸、恒星形成和当前关于暗物质的理论。

## Style Patterns

### 13. Overuse of dashes

Before:

> 这个术语主要由荷兰机构推广——而不是由人民自己。你不会说"荷兰，欧洲"作为地址——但这种错误标记仍在继续——即使在官方文件中。

After:

> 这个术语主要由荷兰机构推广，而不是由人民自己。你不会说"荷兰，欧洲"作为地址，但这种错误标记在官方文件中仍在继续。

### 14. Overuse of bold

Before:

> 它融合了 **OKR（目标和关键结果）**、**KPI（关键绩效指标）** 和视觉战略工具，如 **商业模式画布（BMC）** 和 **平衡计分卡（BSC）**。

After:

> 它融合了 OKR、KPI 和视觉战略工具，如商业模式画布和平衡计分卡。

### 15. Inline-heading vertical lists

Before:

> - **用户体验：** 用户体验通过新界面得到显著改善。
> - **性能：** 性能通过优化算法得到增强。
> - **安全性：** 安全性通过端到端加密得到加强。

After:

> 更新改进了界面，通过优化算法加快了加载时间，并添加了端到端加密。

### 16. Title case in headings

This is mostly an English issue. For Chinese headings, prefer natural, plain headings and avoid decorative capitalization when English appears.

### 17. Decorative emoji

Before:

> 🚀 **启动阶段：** 产品在第三季度发布
> 💡 **关键洞察：** 用户更喜欢简单
> ✅ **下一步：** 安排后续会议

After:

> 产品在第三季度发布。用户研究显示更喜欢简单。下一步：安排后续会议。

### 18. Quote style drift

In Chinese, use the quote style that matches the document. Avoid unnecessary English smart quotes in otherwise Chinese text.

## Conversational Artifacts

### 19. Chatbot residue

Watch for: 希望这对您有帮助, 当然, 一定, 您说得完全正确, 您想要, 请告诉我, 这是一个.

Before:

> 这是法国大革命的概述。希望这对您有帮助！如果您想让我扩展任何部分，请告诉我。

After:

> 法国大革命始于 1789 年，当时财政危机和粮食短缺导致了广泛的动荡。

### 20. Knowledge-cutoff disclaimers

Watch for: 截至某日期, 根据我最后的训练更新, 虽然具体细节有限, 基于可用信息.

Before:

> 虽然关于公司成立的具体细节在现成资料中没有广泛记录，但它似乎是在 20 世纪 90 年代的某个时候成立的。

After:

> 根据注册文件，该公司成立于 1994 年。

### 21. Flattery or over-agreement

Before:

> 好问题！您说得完全正确，这是一个复杂的话题。关于经济因素，这是一个很好的观点。

After:

> 您提到的经济因素在这里是相关的。

## Filler and Evasion

### 22. Filler phrases

Rewrite these directly:

- 为了实现这一目标 -> 为了实现这一点
- 由于下雨的事实 -> 因为下雨
- 在这个时间点 -> 现在
- 在您需要帮助的情况下 -> 如果您需要帮助
- 系统具有处理的能力 -> 系统可以处理
- 值得注意的是数据显示 -> 数据显示

### 23. Over-qualification

Before:

> 可以潜在地可能被认为该政策可能会对结果产生一些影响。

After:

> 该政策可能会影响结果。

### 24. Generic positive endings

Before:

> 公司的未来看起来光明。激动人心的时代即将到来，他们继续追求卓越的旅程。这代表了向正确方向迈出的重要一步。

After:

> 该公司计划明年再开设两个地点。

## Quick Checklist

Before returning the rewritten text, check:

- Are three consecutive sentences the same length? Break one.
- Does a paragraph end with a neat slogan-like line? Vary the ending.
- Is there a dash before a reveal? Remove or replace it.
- Is the text explaining an obvious metaphor? Trust the reader.
- Are connectors such as 此外, 然而, 值得注意的是 overused? Delete where possible.
- Is there a three-part list? Consider two items, four items, or a sentence.

## Workflow

1. Read the input carefully.
2. Identify concrete instances of the patterns above.
3. Rewrite the affected passages.
4. Make sure the revised text:
   - Sounds natural when read aloud.
   - Varies sentence structure.
   - Uses concrete details instead of vague claims.
   - Keeps the right tone for the context.
   - Uses simple structures when they are clearer.
5. Return the humanized version.

## Output Format

Default to:

1. The rewritten text.
2. A brief summary of the most important changes, only when useful.

If the user asks for diagnostics, include the pattern names and examples. If the user only wants a clean rewrite, keep the explanation minimal.

## Quality Score

When useful, score the rewritten text out of 50:

| Dimension | Standard | Score |
| --- | --- | --- |
| Directness | Directly states the point instead of circling it. | /10 |
| Rhythm | Sentence lengths vary naturally. | /10 |
| Reader trust | Does not over-explain. | /10 |
| Authenticity | Sounds like a real person. | /10 |
| Concision | Removes unnecessary words. | /10 |
| Total |  | /50 |

Score guide:

- 45-50: Excellent.
- 35-44: Good, with room to tighten.
- Below 35: Revise again.

## Complete Example

Before:

> 新的软件更新作为公司致力于创新的证明。此外，它提供了无缝、直观和强大的用户体验——确保用户能够高效地完成目标。这不仅仅是一次更新，而是我们思考生产力方式的革命。行业专家认为这将对整个行业产生持久影响，彰显了公司在不断演变的技术格局中的关键作用。

After:

> 软件更新添加了批处理、键盘快捷键和离线模式。来自测试用户的早期反馈是积极的，大多数报告任务完成速度更快。

Changes:

- Removed "作为...的证明" as overstated significance.
- Removed "此外" as filler.
- Removed "无缝、直观和强大" as promotional three-part phrasing.
- Removed the dash reveal and "确保" phrase.
- Removed "这不仅仅是...而是..." as negative parallelism.
- Removed "行业专家认为" as vague attribution.
- Replaced abstract impact claims with concrete features and feedback.

## Reference

This skill is adapted from op7418/Humanizer-zh, which is based on Wikipedia:Signs of AI writing and related AI writing cleanup guidance. Use these patterns as editorial heuristics, not as proof that a text was written by AI.
