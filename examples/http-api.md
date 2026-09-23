# 样例 · HTTP API（极简词表包）

> 用途：展示 Vocabulary-First 填完长什么样。领域可换成任意新学科，结构保持不变。

## seed terms（入口）

| 词 | 白话 | 通常激活什么 |
|---|---|---|
| request / response | 一次往来：问与答 | 客户端 ↔ 服务端 |
| header / body | 信封与信纸 | HTTP 报文结构 |
| status code | 结果编号 | 成功 / 客户端错 / 服务端错 |
| method | 打算对资源做什么 | GET / POST / PUT / PATCH / DELETE |
| endpoint / route | 资源地址与入口 | URL 设计 |
| JSON | 常见正文格式 | API 载荷 |
| auth | 你是谁、能不能做 | token / session / API key |
| rate limit | 单位时间能打多少次 | 限流与配额 |

## core lexicon（骨架，摘录）

| 词 | 白话 | 备注 |
|---|---|---|
| idempotent | 同一请求重复执行，效果应与一次相同 | PUT / DELETE 常被拿来讨论 |
| safe method | 不应改变服务端状态 | 多为 GET / HEAD |
| content negotiation | 双方协商表示形式 | Accept / Content-Type |
| pagination | 大列表分段取回 | cursor / offset |
| webhook | 服务端主动回调通知 | 事件驱动集成 |
| CORS | 浏览器跨源访问策略 | 前端联调常见坑 |
| contract / OpenAPI | 接口契约与可机读描述 | 协作与代码生成 |
| latency / throughput | 慢与量 | 性能对话的基本坐标 |

## shibboleths（高信号）

| 词 | 何时出现 | 易与谁混淆 |
|---|---|---|
| REST vs RPC | 争论接口风格时 | 「RESTful」口头禅 vs 真正的资源约束 |
| at-least-once / exactly-once | 谈投递语义时 | 消息队列语境，不只是 HTTP |
| backpressure | 下游吃不下时 | 流式系统 / 网关 |
| idempotency-key | 支付与下单防重 | 与「幂等方法」相关但更具体 |
| 12-factor（配置外置等） | 部署与十二要素应用 | 偏运维 / 平台，邻域是云原生 |

## threshold concepts（学通会开窍）

1. **资源与表示分离**：同一个订单，可以是 HTML 页，也可以是 JSON。  
2. **失败也是契约的一部分**：4xx / 5xx 不是「程序坏了」的同义词。  
3. **幂等改变重试策略**：是否敢自动重试，往往取决于这一点。

## entry vocabulary（外行 → 标准名）

| 外行说法 | preferred term |
|---|---|
| 网址后面那串 | path / route / endpoint |
| 返回码 | status code |
| 登录票据 | access token / session |
| 接口文档 | API contract / OpenAPI spec |
| 被限流了 | rate limited |

## concept map（边，摘录）

```text
client —发出→ request
request —含有→ header, body, method
response —带回→ status code, header, body
endpoint —受→ auth, rate limit 约束
OpenAPI —描述→ contract
idempotent —影响→ retry 策略
```

用这份表提问时，可直接说：*沿用上面 glossary，当作语义约定；任务是……*
