---
layout: default
title: "ExamO AI Study Agent｜智能体机制与边界"
description: "ExamO AI Study Agent｜智能体机制与边界 / ExamO product documentation"
lang: zh-CN
review_date: 2026-10-20
---

# ExamO AI Study Agent

**课程感知型学习智能体项目 / A course-aware learning agent project**

核验日期 / Reviewed: 2026-10-20。

## 目标与当前实现

支持大学生用自己的课程、考试目标与学习资料开展练习和持续复习。当前实现结合用户控制、模型辅助与规则决策；“学习智能体”是项目方向，不代表已实现模型自主多工具调度。

| 环节 | 当前实现 | 边界 |
| --- | --- | --- |
| 感知 / Perception | 文件、图片和文本解析，课程与考试上下文，知识点与资料证据 | 用户核对；内容质量影响识别和推断 |
| 规划 / Planning | 时间预算、考试优先级、任务队列与学习计划 | 已实现，需启用；规则和数据计算，非模型自主拆解任意目标 |
| 执行 / Execution | 应用调用解析、生成练习、批改、错题、闪卡与费曼等能力 | 用户触发；不是统一自主工具调用器 |
| 评估 / Evaluation | 答题记录、掌握度、薄弱点、验证与复习反馈 | 辅助指标；不预测成绩，不将不可靠批改直接当作学习证据 |
| 调整 / Adjustment | 基于记录重新计算优先级、难度与复习建议 | 部分需启用；下次请求重新计算，不表示持续后台自运行 |

## 能力与工具

资料解析/OCR、知识整理、原题练习、AI 生成练习、模拟考试、批改与解释、错题分析、自适应训练、闪卡复习、费曼讲解均有实现入口。它们由应用流程按用户动作调用，不能把“存在这些能力”宣传为“模型可自主选用所有工具”。

## 记忆与上下文

已有课程、知识点、答题表现、掌握状态、训练/复习记录与学习偏好的实现。个性化取决于数据、配置和用户设置。这里的“记忆”指应用记录与统计，不代表无限保存、跨平台数据融合或模型永久记住用户。

## 执行流程

用户选择课程和目标 → 上传并核对资料 → 整理知识证据 → 在启用后计算计划 → 用户选择学习能力 → 作答或主动回忆/讲解 → 记录符合条件的反馈 → 更新状态 → 下次请求重算建议。

这条路径已有多个相互连接的实现，但没有证据证明所有输入、工具和复习方式都受同一自主控制器统一编排。不会把课程截图导入当作课件导入或自动出题。

## 用户控制、安全与恢复

- 资料核对、任务启动和偏好设置保留用户控制；后台通知应另行取得用户授权。
- 服务端身份和归属校验限制数据访问；模型输出仍需核对。本页不构成安全认证或合规结论。
- 已有部分任务状态、超时、错误和降级处理；没有核实通用自主重规划与任意任务自动恢复。
- 不代替学生作出考试成绩保证，不把资料重要度当成真实考试概率。
- 本仓库不公开提示词、核心算法参数、模型凭据、学习原件和个人记录。

## 状态 / Status

**已实现 / Implemented**：课程和资料上下文、用户触发的多步骤学习流程、学习记录与部分规则建议。

**已实现但需配置及验收 / Implemented, configuration and acceptance required**：学习任务规划、考试专项训练、部分动态难度与复习策略。

**规划 / Planned**：模型自主选工具、跨任务长期执行、统一调度闪卡/费曼/提醒、授权后的后台通知与自动失败重规划。

## English

ExamO is an AI Study Agent project for university exam preparation. Its present implementation is a user-controlled study system combining model assistance with rule-based orchestration.

Perception includes reviewed materials, course context and concept evidence. Planning services calculate time budgets, priorities and task suggestions when enabled. Execution invokes study capabilities through application workflows. Evaluation records eligible performance and recall feedback. Adjustment recalculates subsequent recommendations, difficulty and revision timing from updated state.

Memory means application records and learning preferences, not unlimited retention or permanent model memory. Tool availability does not establish autonomous tool selection. Job states and timeouts do not establish general autonomous recovery.

Implemented foundations include context, records and user-triggered multi-step workflows. Planning and some adaptive features require configuration and acceptance. Autonomous model-directed tool selection, sustained cross-task execution, a unified flashcard/Feynman/reminder controller and autonomous error replanning remain **Planned**. Background notifications also require explicit consent and a complete delivery implementation.

This is an education-agent and exam-preparation-agent project description, not a claim of a fully autonomous Agentic Learning System. See [FEATURES.md](features.md) and [ROADMAP.md](roadmap.md).
