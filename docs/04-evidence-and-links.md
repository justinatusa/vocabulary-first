# 04 · 证据与链接

> 说明：链接以整理当日可访问来源为准；若失效，用标题关键词检索同名概念即可。

## 与「词表优先」几乎同构的实践

### Vocabulary-First Onboarding（FG-0108）

- 链接：[FG-0108 Vocabulary-First Onboarding](https://forge.itsbroken.ai/techniques/fg-0108.html)
- 要点：领域词表是人与 AI 之间的 API；先握 20–30 个从业者用词；卡住时先诊断是否「缺词」而非「缺能力」。
- 子方法：Domain Vocabulary Bootstrap / Concept-Level Sufficiency（会叫名即可协作）/ Vocabulary Gap Detection。

### Glossary-First Prompt

- 链接：[The Glossary-First Prompt（DEV）](https://dev.to/novaelvaris/the-glossary-first-prompt-align-on-terms-before-you-ask-for-code-dbn)
- 要点：写代码前先对齐 8–15 个会改变实现选择的词；多义词必须先提问；减少返工。

### Semantic Anchors

- 链接：[LLM-Coding/Semantic-Anchors](https://github.com/LLM-Coding/Semantic-Anchors)
- 要点：短标签激活大块共享知识（如 `TDD, London School`、`arc42`）；压缩 prompt、提高一致性。
- 延伸：[Spec-Driven Development with Semantic Anchors](https://llm-coding.github.io/Semantic-Anchors/spec-driven-development)

### Domain-specific prompts / 术语进 prompt

- 例：[Crafting Domain-Specific Prompts](https://www.refontelearning.com/blog/crafting-domain-specific-prompts-for-better-llm-outputs)
- 要点：主动使用领域术语，有助于模型进入正确知识区；可维护领域 glossary。

### Prompt 词汇与领域知识（研究向）

- 例：[Prompt Engineering: How Prompt Vocabulary affects Domain Knowledge](https://arxiv.org/html/2505.17037v1)
- 要点：prompt 用词选择会影响领域知识激活与表现（学术证据向，方法仍在发展）。

## 学习科学近亲

| 概念 | 参考入口 |
|---|---|
| Concept map | [Wikipedia: Concept map](https://en.wikipedia.org/wiki/Concept_map) |
| Advance organizer | Ausubel；常与 concept map 一起出现在教学设计里 |
| Threshold concepts | Meyer & Land；医学/科学教育中大量案例 |
| Concept inventory | 学科概念测查工具（如各学科 Concept Inventory） |

## 知识组织近亲

| 概念 | 参考入口 |
|---|---|
| Controlled vocabulary | 图书馆学受控词表（优选词、参照、消歧） |
| SKOS / taxonomy | 用层次与 `broader/narrower` 管术语；有人用 ChatGPT 辅助从扁平词表生成层级 |
| Shared glossary / termbase | 组织级人机共用词表（企业术语库、AI-ready termbase） |

## Prompt 工程词表（元层）

学「如何跟 AI 说话」本身也有一套 seed terms，例如：

- NYIT LibGuide：[Prompt Engineering Key Terms](https://libguides.nyit.edu/promptengineering/key-terms)（含 Seed Words、few-shot、CoT 等）
- 各类 technique map：zero-shot / few-shot / chaining / meta-prompting / RAG …

这是「第二层词表」：先有协作手法的名，再有领域的名。

## 对话中形成的判断（非外部文献，但是仓库结论）

1. 用户要找的不是单一英文词，而是 **可写入 prompt 的总称簇**。  
2. 比喻「锚点」有直觉，但 **seed / lexicon / shibboleth / glossary-first** 更可执行。  
3. **文件级一致**（会跑）与 **流水线文件**（会发版）可分离——同理，学习时词表齐了就能学，不必先有完美 ontology。  
