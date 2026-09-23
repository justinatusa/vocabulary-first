# 05 · Skill 种子（给其他 AI / 未来的你）

## 给其他 AI 的阅读说明（请先读）

你正在阅读的仓库，记录的是用户的真实目标：

> 用「领域高密度术语总称」驱动与 LLM 的学习与协作：先反向要词表，再正向用词表要细节或派活，并迭代成可复用 skill。

若用户要求你「据此写成 skill」，请输出：

1. 短 system/指令（≤40 行）  
2. 固定输入槽位（领域、目标、已有词表、输出格式）  
3. 固定输出 schema（表格字段不可随意改名）  
4. 失败模式（缺词、邻域混淆、假懂）与追问策略  
5. 不要把本 README 全文塞进 skill；要**压缩成可执行协议**

高信号关键词（便于你定位意图）：
`Vocabulary-First`, `Glossary-First`, `anchor terms`, `semantic anchors`, `seed terms`, `core lexicon`, `glossary`, `shibboleths`, `trigger terms`, `jargon map`, `controlled vocabulary`, `threshold concepts`, `concept map`, `entry vocabulary`, `terms of art`, `ubiquitous language`

---

## 建议拆成的 skill 粒度（推荐）

| Skill 名（建议） | 只做一件事 |
|---|---|
| `vocab.bootstrap` | 给定领域 → 输出 A2 扩充词表包 |
| `vocab.gap` | 白话描述 → preferred term 候选 |
| `vocab.teach` | 给定 glossary → 按 threshold 教学 |
| `vocab.task` | 给定 glossary + 任务 → 受语义契约约束的产出 |
| `vocab.refine` | 旧词表 + 新对话 → 增量合并与消歧 |

先做前两个，通常就够回流；teach/task 第二批再做。

---

## Skill 草稿：`vocab.bootstrap`

```yaml
name: vocab.bootstrap
purpose: Bootstrap a Vocabulary-First pack for a domain
inputs:
  domain: string
  locale: "zh-CN" | "en" | "bilingual"
  depth: "trio" | "full"   # trio=A1, full=A2
output_schema:
  - section: semantic_anchors|seed_terms|core_lexicon|shibboleths|threshold_concepts|entry_vocabulary|concept_map_edges
  - fields: [term, gloss, activates, notes]
rules:
  - Prefer tables; minimize prose
  - Mark lookalike neighbor domains for shibboleths
  - Prefer terms of art over metaphors
  - If domain is ambiguous, ask 1 clarifying question then stop
```

## Skill 草稿：`vocab.task`

```yaml
name: vocab.task
purpose: Execute a task under a semantic contract glossary
inputs:
  glossary: table
  task: string
  deliverable: string
rules:
  - Glossary is a semantic contract
  - Map aliases to preferred terms silently
  - On ambiguity, ask before acting
  - Ban undefined evaluative adjectives (fast/good/elegant) unless defined
  - Every major design choice must cite a glossary term
```

---

## 对人的使用建议

1. **先消化文档，再写 skill**——skill 是压缩，不是另一份散文。  
2. **词表文件化**（如 `glossaries/<domain>.md`），skill 只引用路径。  
3. **教领域时**：bootstrap → teach → 小测验（concept inventory 风格）→ 再 task。  
4. **别神化词表**：词会过时；保留 aliases/deprecated，定期 refine。  
5. **评价标准**：协作是否更少来回、是否更少邻域跑偏，而不是词表有多长。

---

## 一句话总纲（可当 skill 开头）

> Domain vocabulary is the API between the learner and the model. Name things first; then ask for depth or work.
