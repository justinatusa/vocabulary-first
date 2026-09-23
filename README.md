<p align="center">
  <img src="assets/banner.svg" alt="Vocabulary-First" width="920"/>
</p>

<p align="center">
  <em>「先对齐名字，再进入领域。」</em>
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-c9a86c?style=flat-square&labelColor=161c24" alt="MIT"/></a>
  <a href="docs/01-problem.md"><img src="https://img.shields.io/badge/Docs-中文主文档-e8d5a3?style=flat-square&labelColor=161c24" alt="Docs"/></a>
  <a href="docs/03-bidirectional-usage.md"><img src="https://img.shields.io/badge/Prompts-可复制-blueviolet?style=flat-square&labelColor=161c24" alt="Prompts"/></a>
  <a href="examples/http-api.md"><img src="https://img.shields.io/badge/Example-HTTP%20API-2ea44f?style=flat-square&labelColor=161c24" alt="Example"/></a>
  <img src="https://img.shields.io/badge/For-人类%20%7C%20模型-6e7781?style=flat-square&labelColor=161c24" alt="Audience"/>
</p>

<p align="center">
  <strong>领域词表 = 人与模型之间的接口。</strong><br/>
  本仓库整理一套可复用的学习与协作方法：先拿到高密度术语，再据此提问、讲解、派活，并逐步收成 skill。
</p>

<p align="center">
  <a href="#一句话">一句话</a> ·
  <a href="#它解决什么">它解决什么</a> ·
  <a href="#结论">结论</a> ·
  <a href="#文档地图">文档地图</a> ·
  <a href="#三分钟样例">样例</a> ·
  <a href="#给模型读">给模型读</a>
</p>

---

## 一句话

几个词一出现，双方就站到同一张领域地图上。  
`header` / `body` 不必先声明「我在谈 HTTP」；「反代」在特定圈子里，会自动带上网关、上游、token 整条链路。

那不是装腔，而是**入口词 + 骨架词 + 圈内高信号暗号**。本仓库要找的，是这类现象的**可写入提示的总称**，以及一套双向用法。

---

## 它解决什么

| 常见卡点 | 实际发生了什么 |
|---|---|
| 叫不出名字 | 心里有画面，口头只有白话，模型只好猜 |
| 学新领域慢 | 材料很多，却抓不住骨架 |
| 每次说法都飘 | 同一需求换一套形容，答复就滑到邻域 |
| 方法停在聊天里 | 无法回流成可复用的教学 / 协作流程 |

---

## 结论

**没有唯一官方词。** 对外可统称：

> **Vocabulary-First** / **Glossary-First**

日常三件套：

| 名称 | 作用 |
|---|---|
| **seed terms** | 很少的入口种子，一说就定位 |
| **core lexicon / glossary** | 骨架术语，撑起地图 |
| **shibboleths**（或 high-signal jargon） | 圈内高信号暗号 |

写进提示时也很贴的叫法：**anchor terms / semantic anchors**、**trigger terms**、**threshold concepts**、**concept map**、**entry vocabulary**。

闭环很短：

```text
反向要词表 → 消化 / 收藏
正向用词表要细节或派活
卡住就先补词，再继续
回流进词表与 skill
```

网上已有同思路实践，例如 [Vocabulary-First Onboarding](https://forge.itsbroken.ai/techniques/fg-0108.html)、[Glossary-First Prompt](https://dev.to/novaelvaris/the-glossary-first-prompt-align-on-terms-before-you-ask-for-code-dbn)、[Semantic Anchors](https://github.com/LLM-Coding/Semantic-Anchors)。

---

## 文档地图

| 文件 | 读什么 |
|---|---|
| [docs/01-problem.md](docs/01-problem.md) | 疑惑从哪来、要达成什么 |
| [docs/02-vocabulary-family.md](docs/02-vocabulary-family.md) | 词表家族与取舍 |
| [docs/03-bidirectional-usage.md](docs/03-bidirectional-usage.md) | 反向 / 正向，可复制提示 |
| [docs/04-evidence-and-links.md](docs/04-evidence-and-links.md) | 外部证据与链接 |
| [docs/05-skill-seeds.md](docs/05-skill-seeds.md) | 压缩成 skill 的种子 |
| [examples/http-api.md](examples/http-api.md) | 一份填好的小样 |

---

## 三分钟样例

完整小表见 [examples/http-api.md](examples/http-api.md)。摘三行感受密度：

| 层 | 词 | 一句话 |
|---|---|---|
| seed | `status code` | 响应结果的编号语言 |
| core | `idempotent` | 同一请求做多次，效果应与一次相同 |
| shibboleth | `REST vs RPC` | 一开口就暴露接口风格立场 |

要整包时，直接用 [docs/03-bidirectional-usage.md](docs/03-bidirectional-usage.md) 里的 A1 / A2 提示即可。

---

## 给模型读

若任务是「读完本仓库，协助写成 skill」：

1. 先读本页结论与 [01](docs/01-problem.md)、[02](docs/02-vocabulary-family.md)  
2. 再读 [05](docs/05-skill-seeds.md)，按其中的输入槽位与输出 schema 压缩  
3. **不要**把全文塞进 skill；skill 是可执行协议，不是第二份散文  
4. 高信号关键词：`Vocabulary-First`, `seed terms`, `core lexicon`, `glossary`, `shibboleths`, `semantic anchors`, `trigger terms`

---

## 写作约定

- 中文叙述为主，英文术语保留（便于检索与写入提示）  
- 第三人称直叙；少黑话，多白话  
- 方法优先于对话年表：足够理解即可，不必复现私人聊天  

---

## 许可

[MIT](LICENSE)。分享的是方法与公开链接，不含私人数据。

---

<p align="center">
  <sub>命名精度，预测协作速度。</sub><br/>
  <sub><em>Name things first. Then ask for depth.</em></sub>
</p>
