# 02 · 词表家族（Vocabulary Family）

> 用法层总称：**Vocabulary-First** / **Glossary-First**。  
> 下面是可写进 prompt 的零件词；按需组合，不必一次全要。

## 核心三件套（日常够用）

| 总称 | 侧重点 | 典型用途 |
|---|---|---|
| **seed terms / seed words** | 很少的入口种子 | 先定位，再展开 |
| **core lexicon / domain vocabulary / glossary** | 骨架词表、专名清单 | 建地图、统一叫法 |
| **shibboleths** | 圈内高信号暗号 | 一听就定位场景 / 是否自己人 |

相近写法：`terms of art`（正经专名）、`high-signal jargon`（高密度行话）。

## AI 协作向（几乎就是本仓库主题）

| 总称 | 一句话 |
|---|---|
| **Semantic Anchors（语义锚）** | 极短专名激活模型里一整块方法/流派知识（如 `TDD, London School`） |
| **Vocabulary-First Onboarding** | 进新领域前先握 20–30 个从业者用词 |
| **Glossary-First Prompt** | 先对齐术语再写代码/方案 |
| **Ubiquitous Language（DDD）** | 业务侧共同语言 |
| **Nomenclature / terminology alignment** | 显式统一命名 |
| **Declaration layer / termbase** | 先声明「以谁为准」，再读内容/执行 |
| **Vocabulary governance** | 首选词、别名、禁用词的治理 |

## 学习科学 / 认知向

| 总称 | 一句话 |
|---|---|
| **Advance organizer（先行组织者）** | 学新知前先给框架，后面有处可挂 |
| **Concept map（概念图）** | 词 + 关系，不只是扁平清单 |
| **Concept inventory** | 用核心概念测是否真懂 |
| **Threshold concepts** | 跨过才开窍的门槛概念 |
| **Schema activation（图式激活）** | 线索唤醒整套认知图式（header/body → HTTP 很像这个） |
| **Lexical priming（词汇启动）** | 先出现的词拉高相关理解 |
| **Scaffolding** | 术语支架撑起后续学习 |
| **Mental model / shared mental model** | 脑中可运行的领域模型；共同语言是入口 |

## 知识组织 / 检索向

| 总称 | 一句话 |
|---|---|
| **Controlled vocabulary** | 受控词表：一词一义、有关系 |
| **Thesaurus / taxonomy / ontology** | 同义词表 → 分类树 → 概念网 |
| **Entry vocabulary** | 外行说法 → 专家标准词的桥 |
| **Preferred term / alias / deprecated** | 标准名、别名、废弃名 |
| **Index terms** | 高信号主题词/标签 |
| **Facet vocabulary** | 按维度切词（对象/动作/约束/指标…） |

## 怎么选（速查）

| 你想要的效果 | 优先喊 |
|---|---|
| 几个词定位领域 | shibboleths / semantic anchors / high-signal jargon |
| 可学的骨架地图 | core lexicon / concept map / advance organizer |
| 跟 AI 对齐、少返工 | glossary-first / controlled vocabulary / ubiquitous language |
| 学通会开窍 | threshold concepts |
| 外行话换圈内话 | entry vocabulary；aliases → preferred terms |
| 反向建表再正向干活 | Vocabulary-First 全套 |

## 中文可用说法

种子词、核心词表、专名、圈内暗号、受控词表、术语表、门槛概念、概念图、语义锚、词表优先 / 术语表优先。

---

## 候选词取舍表（补充检索后的合并结论）

来源：对话中的自搜 + 二次补搜。只保留对「写 prompt / 学领域 / 变 skill」真有用的；不合适的明确剔除或降级。

| 名词 | 适用场景 | 能否写进 prompt 描述需求 | 本仓库态度 |
|---|---|---|---|
| **Anchor terms / Semantic anchors** | Prompt 工程；短名激活大块训练知识 | ✅ 强烈推荐 | **首选之一**（与 seed/glossary 并列） |
| **Trigger terms / context trigger words** | 知识唤起；glossary 懒加载匹配 | ✅ 可用 | 推荐作「机制说明」：词出现 → 注入定义 |
| **Glossary** | 人机共享术语表 | ✅ 推荐 | 已是主干（Glossary-First） |
| **Jargon / domain jargon** | 通用行话 | ✅ 可用但偏宽 | 保留；写 prompt 时最好收窄成 high-signal jargon |
| **Jargon map** | 行话 → 含义/关系的地图 | ✅ 可用 | 作 concept map 的口语近亲 |
| **Domain shorthand** | 工程口语速记 | ✅ 可用 | 降级为 seed/shibboleth 的别称，不单列为主概念 |
| **Chunk（认知组块）** | 认知心理学：一次握住的信息块 | ⚠️ 解释原理可用 | **可写在说明里**；勿与 RAG text chunking 混淆 |
| **Tacit knowledge（默会知识）** | 指背后那套不会说的知 | ❌ 不是那些关键词 | **保留为反例**：别用它指「要的那串词」 |
| **Indexical term（索引词）** | 语言学冷门 | ❌ 工程对话少用 | **不收入主词表** |

### 补搜后额外值得挂上的

| 名词 | 为什么有价值 |
|---|---|
| **Semantic Anchors**（方法名目录） | 有公开目录与实验：专名比长段释义更能稳定激活方法知识 |
| **Agent Glossary + trigger 懒加载** | 词作 trigger，命中才注入定义；词表可很大、上下文仍瘦 |
| **Domain glossary = context compression** | 规范词把多句解释压成短柄，命名一致性上升 |
| **Semantic compression（具名指针）** | 「用标准名当 pointer，别重讲模型已知的常识」——与 anchor 同构 |

### 写 prompt 时的优先顺序（实操）

1. 要入口/骨架清单 → `seed terms` + `core lexicon` / `glossary`  
2. 要「一说就激活方法」→ `anchor terms` / `semantic anchors`  
3. 要圈内定位/防邻域跑偏 → `shibboleths` / `high-signal jargon`  
4. 要外行话换标准名 → `entry vocabulary`  
5. 要关系图 → `concept map` 或口语 `jargon map`  
