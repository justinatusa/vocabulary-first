# 04 · 证据与链接

> 链接以整理当日可访问来源为准；若失效，用标题关键词检索同名概念即可。

## 与「词表优先」几乎同构的实践

### Vocabulary-First Onboarding（FG-0108）

- 链接：[FG-0108 Vocabulary-First Onboarding](https://forge.itsbroken.ai/techniques/fg-0108.html)
- 要点：领域词表是人与模型之间的接口；先握 20–30 个从业者用词；卡住时先诊断是否「缺词」而非「缺能力」。
- 子方法：Domain Vocabulary Bootstrap / Concept-Level Sufficiency（会叫名即可协作）/ Vocabulary Gap Detection。

### Glossary-First Prompt

- 链接：[The Glossary-First Prompt（DEV）](https://dev.to/novaelvaris/the-glossary-first-prompt-align-on-terms-before-you-ask-for-code-dbn)
- 要点：写代码前先对齐 8–15 个会改变实现选择的词；多义词必须先提问；减少返工。

### Semantic Anchors

- 链接：[LLM-Coding/Semantic-Anchors](https://github.com/LLM-Coding/Semantic-Anchors)
- 要点：短标签激活大块共享知识（如 `TDD, London School`、`arc42`）；压缩提示、提高一致性。
- 延伸：[Spec-Driven Development with Semantic Anchors](https://llm-coding.github.io/Semantic-Anchors/spec-driven-development)

### Domain-specific prompts / 术语进提示

- 例：[Crafting Domain-Specific Prompts](https://www.refontelearning.com/blog/crafting-domain-specific-prompts-for-better-llm-outputs)
- 要点：主动使用领域术语，有助于模型进入正确知识区；可维护领域 glossary。

### 提示用词与领域知识（研究向）

- 例：[Prompt Engineering: How Prompt Vocabulary affects Domain Knowledge](https://arxiv.org/html/2505.17037v1)
- 要点：提示用词选择会影响领域知识激活与表现（学术证据向，方法仍在发展）。

## 学习科学近亲

| 概念 | 参考入口 |
|---|---|
| Concept map | [Wikipedia: Concept map](https://en.wikipedia.org/wiki/Concept_map) |
| Advance organizer | Ausubel；常与 concept map 一起出现在教学设计里 |
| Threshold concepts | Meyer & Land；医学 / 科学教育中大量案例 |
| Concept inventory | 学科概念测查工具（如各学科 Concept Inventory） |

## 知识组织近亲

| 概念 | 参考入口 |
|---|---|
| Controlled vocabulary | 图书馆学受控词表（优选词、参照、消歧） |
| SKOS / taxonomy | 用层次与 `broader/narrower` 管术语 |
| Shared glossary / termbase | 组织级人机共用词表（企业术语库、AI-ready termbase） |

## 提示工程词表（元层）

学「如何跟模型说话」本身也有一套 seed terms，例如：

- NYIT LibGuide：[Prompt Engineering Key Terms](https://libguides.nyit.edu/promptengineering/key-terms)（含 Seed Words、few-shot、CoT 等）
- 各类 technique map：zero-shot / few-shot / chaining / meta-prompting / RAG …

这是「第二层词表」：先有协作手法的名，再有领域的名。

## 本仓库的几条判断

1. 要找的不是单一英文词，而是 **可写入提示的总称簇**。  
2. 比喻「锚点」有直觉，但 **seed / lexicon / shibboleth / glossary-first** 更可执行。  
3. 学习时词表齐了就能推进；不必先有完美 ontology。

---

## 补充检索（第二轮）

### Anchor / Semantic Anchors

- [LLM-Coding/Semantic-Anchors](https://github.com/LLM-Coding/Semantic-Anchors)：专名激活方法知识；强调 Names beat descriptions。
- [Augmented Coding Patterns · Semantic Anchors](https://lexler.github.io/augmented-coding-patterns/patterns/semantic-anchors/)：有对照实验叙述（点名 vs 只描述）。
- [Promptwatch · Anchor Terms](https://promptwatch.com/glossary/anchor-terms)：偏 GEO / 品牌归因的「锚术语」——**相近但不是同一问题**；本仓库主推的是提示侧 semantic anchors，不把 GEO 义项当主定义。

### Glossary as trigger / 懒加载

- [Agent Glossary 思路（Medium）](https://ronie.medium.com/agent-glossary-teaching-agents-our-shared-language-93bae9674b02)：共享短柄；出现术语再注入定义。
- [ruliana/pi-glossary](https://github.com/ruliana/pi-glossary)：用 term/alias/regex 作 **trigger**，懒加载 glossary。
- 实践笔记：[Three weeks using glossaries for agents](https://ronie.medium.com/three-weeks-using-glossaries-for-agents-4f3c85b49cb5)

### 压缩与领域词表

- Domain glossary 常被写成「上下文压缩 / 命名一致性」手段（多见于 agent 工程笔记）。
- 「具名概念当 pointer」与 anchor terms 同构；检索系统里的 semantic **chunking** 是另一回事，勿混进「认知组块」讨论。

### 取舍摘要

收入主叙事：**anchor terms / semantic anchors**、**trigger terms**（机制）、**glossary**、**jargon map**（近亲）。  
降级：**domain shorthand**。  
原理向备注：**chunk（认知）**。  
显式排除当「那些词」用：**tacit knowledge**、**indexical term**。
