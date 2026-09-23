# 03 · 双向用法与可复制 Prompt

## 闭环

```text
[反向] 用总称要词表
        ↓
   消化 / 收藏 / 微调 glossary
        ↓
[正向] 粘贴 glossary，要解释 / 对比 / 方案 / 代码
        ↓
   卡住？多半是缺词 → 补词再继续
        ↓
   回流进词表与 skill
```

原则：**命名精度预测协作速度。** 会叫名字，模型才进得对知识区；只会形容感觉，就容易猜谜和返工。

---

## 方向 A · 反向（生成词表 / 建地图）

### A1 · 日常三件套

```text
我在学「_____」领域。
请给我三层词，不要长篇解释：
1) seed terms：8–12 个入口词（一说就定位到这个领域）
2) core lexicon：30–50 个骨架术语（terms of art）
3) shibboleths：10 个圈内高信号黑话（注明何时用、易与哪个邻域混淆）
每词一行：词 | 一句话白话 | 它通常激活什么语境
```

### A2 · 扩充版（Vocabulary-First + Semantic Anchors）

```text
领域：_____
请按 Vocabulary-First + Semantic Anchors 输出：
1) semantic anchors（8）：一说就能激活整套方法/流派的短标签
2) seed terms（12）
3) core lexicon（40，terms of art）
4) shibboleths（10）+ 易混邻域
5) threshold concepts（5）：学通了会「开窍」的
6) entry vocabulary：外行说法 → 标准名（10 对）
7) concept map：用「A —关系→ B」列 15 条边
格式尽量表格；少散文。
```

### A3 · 缺词急救（Vocabulary Gap Detection）

```text
我知道我想要什么，但叫不出名字。
我描述的是：_____
这个在「_____」领域的标准术语是什么？
给 3 个候选，说明差别，并标出 preferred term。
```

---

## 方向 B · 正向（用词表要细节 / 派活）

```text
沿用下面 glossary（以此为准，有歧义先问我）：
[粘贴词表]

Treat the glossary as a semantic contract.
Prefer preferred terms; if I use an alias, map it;
if ambiguous, ask before acting.

任务：_____
输出要求：_____
```

### B 的变体

| 目的 | 加一句 |
|---|---|
| 学习 | 按 threshold concepts 优先讲解；每词给「直觉 → 正式定义 → 反例」 |
| 对比 | 只比较 glossary 内概念；表格式：维度 / A / B |
| 设计/代码 | 实现选项必须能回溯到 glossary 中的术语；禁用模糊词（快、好、优雅）除非先定义 |
| 教学 skill | 先抽测 5 个词是否同义；再展开 |

---

## 和常见 prompt 手法怎么拼

- **Meta-prompting**：先让 AI 写「下一问该用哪些总称」  
- **Prompt chaining**：词表 → 概念图 → 任务 分步跑  
- **Role + register**：指定学术 / 工程 / 运维黑话登记  
- **Few-shot**：示例里坚持 preferred terms  
- **Output contract**：回复必须使用词表标准名  

这些不是替代词表，而是词表对齐之后的放大器。
