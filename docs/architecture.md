---
layout: default
title: "技术架构概览 | ExamO"
---

# 技术架构 / Architecture overview

[返回首页](index.html)

| 层级 / Layer | 职责 / Responsibility | 技术概览 / Stack |
| --- | --- | --- |
| 学习入口 / Client | 课程、练习、复习和讲解交互 | WeChat Mini Program |
| 应用服务 / Application | 身份校验与学习流程协调 | Node.js · Express |
| 资料与智能能力 / Capabilities | 文档解析、练习反馈与 AI 伴学 | Document parsing · AI integration |
| 持久化 / Persistence | 结构化学习记录与资料关联 | SQLite |

**学习流程：资料 → 练习 → 反馈 → 复习 → 讲解。**

The client uses application services for study workflows. Document parsing and AI capabilities are accessed behind server-side boundaries. Persistent storage supports learning records. Credentials are server-side configuration, never mini-program secrets.

此处只描述产品技术分层，不发布供应商账户、云环境标识、服务器地址、数据库位置、内部接口或部署拓扑。源码仓库单独授权访问。
