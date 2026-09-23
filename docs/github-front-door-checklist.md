# GitHub 仓库门面清单（可复用）

> 给其他 AI / 未来开新仓用：把「方法仓库」做成对外可分享、同事会 wow、又不喧闹的样子。  
> 徽章只是可选零件之一，**不必每项都上**；按仓库类型取舍。

## 目标

正式、干净、有品味；实质内容优先。  
要学的是 skills / 方法 / 中转站类仓的 taste，不是 Redis / transformers 那种纯工程素页，也不是营销刷屏页。

## 必做（门面骨架）

1. **一句主张**：仓库是什么（可用一个隐喻，如「X 是 Y 的接口」）。
2. **一句金句**（可选但很加分）：短、居中、有立场；不要功能列表当开头。
3. **结论前置**：访客 30 秒知道「没有唯一官方名 / 怎么用 / 去哪读」。
4. **清晰文档地图**：`docs/` 分篇 + 仓库根 README 当目录与摘要。
5. **一份看得见的样例**：`examples/` 里填好一张小表，比纯方法论更能 wow。
6. **About 侧栏**  
   - Description：哲学半句 + 动作半句  
   - Topics：发现用词，约 6–10 个，不刷虚词  
   - Homepage：有独立站再填，否则留空  
   - Wiki / Projects：有 `docs/` 就关掉，减少侧栏噪音
7. **许可**：MIT（或你真实使用的许可）放根目录并在 README 链出去。

## 加分（按需）

| 项 | 何时用 | 注意 |
|---|---|---|
| Banner 图（SVG/PNG） | 方法/作品向仓 | 一张够；墨金/深色克制配色优于彩虹 |
| Social preview PNG 1280×640 | 要丢链接到聊天/推特 | 与 README 内嵌图不是同一槽；在 Settings → Social preview 上传 |
| 徽章 | 需要快速信号时 | **≤3**：License / Docs / Example；不要 stars/Trendshift/赞助墙 |
| 锚点小目录 | README 超过一屏 | `这是什么 · 结论 · 怎么用 · 文档 · 样例` |
| 收尾对句 | 想留余味 | 中英各一行即可，勿 CTA 按钮墙 |
| `npx skills add …` | 真是可安装 skill | 方法论文档仓可不写 |

## 不要做（anti-pattern）

- Happy to announce / 空 Star History / 「请点 star」
- 徽章墙、赞助商表压过正文
- 0 星时还挂 Trending / Trendshift
- 为「正式」而空开 Releases、Actions（无版本产物、无 CI 交付就不必）
- 把聊天记录当文档；第一人称对 AI 喊话味
- Wiki/Projects 空壳开着

## 类型对照（怎么选强度）

| 仓库类型 | 视觉强度 | 参考气质 |
|---|---|---|
| 纯库 / 协议 | 极克制，可无 banner | anthropics/skills、vercel-labs/agent-skills |
| 方法论文档（本仓这类） | 金句 + 一张图 + 少徽章 | vocabulary-first、ponytail 气质 |
| 可安装 Skill 产品 | 可有 demo GIF + 一行安装 | nuwa、huashu-design、mattpocock/skills |
| Awesome / Hub | 分类清单为主，头图可选 | 有品味的 awesome；避开社交墙 |

## 开新仓时对 AI 的最短指令（可复制）

```text
把这个仓库的 GitHub 门面做成「正式、干净、可分享给同事」：
- 实质内容不动或只做必要压缩
- README：居中主张/金句、结论前置、文档地图、一份小样例、克制收尾
- 徽章可选且 ≤3；不要 Star History / 赞助墙 / 求星
- About：description=隐喻+动作；topics 精选；wiki/projects 关掉（若已有 docs/）
- 无版本产物则不要 Releases/Actions
- 另产一张 1280×640 social preview PNG，说明需在 Settings 上传
- 参考气质：有品味的 skills/方法仓，不是纯工程素仓，也不是营销页
```

## 本仓已落地项（vocabulary-first）

- [x] 金句 + banner.svg  
- [x] ≤3 徽章  
- [x] 结论 / 三件套 / 文档地图 / HTTP 样例  
- [x] About description + topics；wiki/projects 关  
- [x] 无 Releases / Actions  
- [x] `assets/social-preview.png`（1280×640，供 Settings 上传）  
