---
layout: default
title: "ExamO 已实现功能与使用边界"
description: "ExamO 已实现功能与使用边界 / ExamO product documentation"
lang: zh-CN
review_date: 2026-10-20
---

# ExamO 已实现功能 / Implemented features

核验日期 / Reviewed: **2026-10-20**。依据两个私有源码仓库当前默认分支，只读核对实现与调用关系；未运行生产验收。表中“已实现 / Implemented”不等于“已上线 / Live”。

| 功能 / Feature | 状态 / Status | 条件与边界 / Conditions |
| --- | --- | --- |
| 文档、图片和粘贴文本解析 / Material parsing | 已实现 / Implemented | 格式、OCR 与服务可用性影响结果；核对后确认 |
| 资料类型与学科上下文 / Classification and subject context | 已实现 / Implemented | AI 可出错，不保证自动识别全部学科 |
| 知识点、资料证据和重要度 / Concepts and importance | 已实现 / Implemented | 考试相关重要度需启用；来源于资料，不是押题 |
| 资料生成练习 / Material-based question generation | 已实现 / Implemented | 基于复习材料；依赖模型配置与输出核对 |
| 上传原题作答 / Original-question practice | 已实现 / Implemented | 保留原题，不将原卷改写为新生成题 |
| 个性化组卷与模拟考试 / Personalized practice and mock exams | 已实现，部分需启用 / Implemented, partly configuration-dependent | 依赖可用资料、知识点与考试设置 |
| 智能批改、解释与错题分析 / Marking and mistake analysis | 已实现 / Implemented | 主观题可能使用模型；不可靠结果不等同有效学习证据 |
| 掌握度与薄弱点 / Mastery and weak points | 已实现 / Implemented | 根据记录估计，非权威评分或成绩预测 |
| 学习时间预算与任务计划 / Study budgets and planning | 已实现，需启用 / Implemented, configuration-dependent | 输入考试时间、可用时间与学习状态；由用户选择执行 |
| 自适应难度和训练顺序 / Adaptive difficulty and priorities | 已实现，部分需启用 / Implemented, partly configuration-dependent | 基于历史证据重新计算，非持续自主运行 |
| 复习间隔与学习偏好 / Review intervals and preferences | 已实现，部分需启用 / Implemented, partly configuration-dependent | 数据量、用户设置影响个性化 |
| 错题与闪卡复习 / Mistakes and flashcards | 已实现 / Implemented | 主动回忆、自评和反馈；不将单次自评当作已掌握证明 |
| AI 讲题与费曼学习 / Explanations and Feynman practice | 已实现 / Implemented | 用户触发；有追问和评价，不宣称实时语音语义理解 |
| 课程与课表管理 / Course and timetable management | 已实现 / Implemented | 截图需核对，课程导入与学习资料导入独立 |
| 应用内课程和考试提示 / In-app class and exam cues | 已实现 / Implemented | 用户打开应用查看，不是后台通知 |
| 学习记录、偏好与训练状态 / Records, preferences and task state | 已实现 / Implemented | 分用户上下文，配置和有效反馈决定可用范围 |

## 仍在验收或规划 / Validation and planning

- **待验收 / Validation required**：生产发布版本、公开体验范围、实际启用配置、跨入口一致性和全流程运行证据。
- **规划 / Planned**：模型自主多工具编排、持续跨任务执行、后台通知、通用自动重规划和任意任务恢复。

This list records implementation findings rather than production availability. Configuration-dependent planning and adaptive features must be enabled and validated. An implemented learning module does not establish an autonomous agent.

[智能体边界 / Agent boundaries](ai-study-agent.md) · [路线图 / Roadmap](roadmap.md)
