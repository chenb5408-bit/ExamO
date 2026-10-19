---
layout: default
title: "ExamO 系统架构"
description: "ExamO 系统架构 / ExamO product documentation"
lang: zh-CN
review_date: 2026-10-20
---

# ExamO 系统架构 / System architecture

核验日期 / Reviewed: 2026-10-20。此处是高层产品架构，不是内部接口或部署手册。

![学习系统与反馈](diagrams/learning-system.svg)

## 技术分层

| 层级 | 职责 / Responsibility |
| --- | --- |
| 原生微信小程序 / Native WeChat Mini Program | 用户输入、识别核对、任务选择、作答和复习交互 |
| Node.js + Express | 身份校验、资料与学习流程协调、权限边界 |
| 文档与 OCR 组件 / Document and OCR components | 文件、图像与文本解析；包含 Python 处理组件 |
| SQLite | 保存资料状态与用户学习记录；运行时使用 Node.js 内置 SQLite |
| 学习决策服务 / Learning decision services | 知识状态、优先级、学习时间预算、练习建议与复习间隔 |
| 服务端模型接入 / Server-side model integrations | 包含 DeepSeek；辅助生成、解释、识别和反馈，具体调用依配置而定 |

## 数据与任务边界

用户确认资料 → 课程和知识上下文 → 用户选择学习任务 → 学习反馈 → 更新记录 → 下次请求重新计算建议。

原试卷/题库与生成练习使用不同路径。原题不得为迎合生成流程而被重写。学习计划与自适应模块有配置前提；不能把源码中存在的实现视为已经在生产开启。

资料解析有排队、运行、成功和失败状态及超时处理；生成任务也有状态记录。这些是应用任务生命周期，不代表模型具备自主编排能力。失败处理包括明确报错、部分降级和由用户重新发起；未核实任意任务的通用自动恢复或跨进程无损续跑。

学习记录按用户和课程上下文使用。个性化依赖设置、数据量与有效反馈；不披露具体数据结构、计算权重、提示词或商业策略。

## 智能体边界

当前可以描述为模型辅助与规则编排结合的学习系统。没有发现完整的模型自主工具调度器；课程提醒、费曼和闪卡也不能据此推断已经组成同一个全自主系统。详见 [AGENT.md](ai-study-agent.md)。

## English

The reviewed system uses a native WeChat Mini Program, Node.js/Express application services, document and OCR components including Python, SQLite through Node.js's built-in interface, study-decision services and server-side model integrations including DeepSeek.

Confirmed materials feed course and knowledge context. Students choose study actions; eligible feedback updates records that later requests use to recalculate recommendations. Original-question and generated-practice paths stay separate. Planning and adaptive modules require configuration and production acceptance.

Parse and generation jobs have lifecycle states and error handling. This is application workflow management, not evidence of autonomous agent orchestration or universal resumability. No internal endpoints, deployment topology, database schema, prompts or commercial decision parameters are published.

[功能 / Features](features.md) · [智能体 / Agent](ai-study-agent.md) · [安全 / Security](security.md)
