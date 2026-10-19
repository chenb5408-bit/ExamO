---
layout: default
title: "ExamO 技术架构概览 | Architecture"
description: "WeChat Mini Program, Node.js, Express, SQLite and document processing."
lang: zh-CN
review_date: 2026-10-19
---

# 技术架构概览 / Architecture overview

核验日期 / Reviewed: **2026-10-19**。只描述公开技术分层，不披露私有实现或部署细节。

| 层级 / Layer | 作用 / Responsibility |
| --- | --- |
| 原生微信小程序 / Native WeChat Mini Program | 课程、资料、练习、复习与用户确认 / Study interfaces and user control |
| Node.js + Express | 组织用户触发的学习流程与权限边界 / Coordinate user-triggered workflows and access boundaries |
| Python 文档处理 / Document processing | 文本、布局与按需识别，处理结果交给用户核对 / Parsing and recognition followed by user review |
| SQLite | 保存结构化学习与任务信息；当前运行时使用 Node 内置 SQLite 接口 / Persistence through Node's built-in SQLite interface |
| 服务端模型集成 / Server-side model integration | 解释、生成与反馈；由应用控制调用流程 / Explanations, generation and feedback through application-controlled calls |

多步骤处理和持久化任务不构成完整自主 Agent 的证据。此处不公布模型账户、服务地址、云环境、私有接口、数据表、内部提示词或业务算法。

Multi-step processing and stored tasks are not evidence of a complete autonomous Agent. Provider accounts, infrastructure, private endpoints, data structures, internal prompts and business algorithms remain outside this public overview.
