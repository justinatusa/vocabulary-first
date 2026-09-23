# Vocabulary-First

> 领域词表 = 你和 AI 之间的 API。先对齐叫法，再学习 / 提问 / 干活。

中文主文档，英文术语保留。本仓库沉淀的是一次真实疑惑及其答案：当我说不清自己在找什么词时，如何找到能「一说就激活整片领域」的那类总称，并把它变成可迭代的学习方法。

---

## 这篇文档面向谁

1. **未来的你**：消化后可改成 skill / 工作流  
2. **其他 AI**：读完应能理解问题、词表家族、双向用法，并协助写成 skill  
3. **协作者**：想用「词表优先」跟 LLM 学新领域的人

---

## 结论（先看这个）

**没有唯一官方词。** 你要的是一簇近亲概念，对外最好叫：

- **Vocabulary-First / Glossary-First**（用法层总称）
- 写进 prompt 很贴的叫法：**anchor terms / semantic anchors**、**seed terms**、**glossary**
- 日常三件套：**seed terms** + **core lexicon / glossary** + **shibboleths**（或 high-signal jargon）
- 进阶可加：**trigger terms**、**controlled vocabulary**、**threshold concepts**、**concept map**、**entry vocabulary**、**jargon map**
- 慎用/别混：**tacit knowledge**（指隐性知识本身，不是那些词）；RAG 的 **chunk** ≠ 认知组块

闭环：

```text
反向：要词表（建地图）
  → 消化 / 收藏高密度术语
正向：用词表提问或派活（要细节、要产出）
  → 卡住时先补词，再继续
  → 回流进词表与 skill
```

网上已有同思路的命名实践，例如 [Vocabulary-First Onboarding (FG-0108)](https://forge.itsbroken.ai/techniques/fg-0108.html)、[Glossary-First Prompt](https://dev.to/novaelvaris/the-glossary-first-prompt-align-on-terms-before-you-ask-for-code-dbn)、[Semantic Anchors](https://github.com/LLM-Coding/Semantic-Anchors)。

---

## 文档地图

| 文件 | 内容 |
|---|---|
| [docs/01-problem.md](docs/01-problem.md) | 原始疑惑、要解决什么、对话里怎么被钉准 |
| [docs/02-vocabulary-family.md](docs/02-vocabulary-family.md) | 词表家族总览（总称 → 侧重点） |
| [docs/03-bidirectional-usage.md](docs/03-bidirectional-usage.md) | 反向生成词表 / 正向用词表；可复制 prompt |
| [docs/04-evidence-and-links.md](docs/04-evidence-and-links.md) | 外部文章、项目、相关说法证据 |
| [docs/05-skill-seeds.md](docs/05-skill-seeds.md) | 给其他 AI 改写成 skill 的种子与建议 |

---

## 30 秒版

你曾经模糊地叫它 leading words / keywords：几个词一出现，对方（人或模型）就知道你在哪个领域的哪张地图上。例如 header + body → HTTP API；「反代」在特定语境下会拉起大模型网关/token 链路。

这不只是「黑话」，而是：

- **入口词**：定位场景  
- **骨架词**：撑起领域地图  
- **高信号暗号（shibboleths）**：圈内一听就懂  

拿去问 AI 时，用**总称**（seed terms、core lexicon…）比用比喻「锚点」更稳；AI 更清楚你要的是词表，不是散文。

---

## 许可

MIT（见 [LICENSE](LICENSE)）。讨论来自私人对话整理，对外分享的是方法与公开链接，不是私人数据。
