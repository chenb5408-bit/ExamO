---
layout: default
title: "ExamO AI Study Agent | 课程感知型学习智能体方向"
description: "A planned Agent direction, with an eight-criteria review and user-control boundaries."
lang: zh-CN
review_date: 2026-10-19
---

# ExamO AI Study Agent

**课程感知型 AI 学习智能体 · Course-aware learning-agent direction**

核验日期 / Reviewed: **2026-10-19**。当前对外定位是 **课程感知型 AI 学习助手 / Course-Aware AI Study Assistant**。本专题中的自主执行型 AI Study Agent 是 **Planned**，不是已经上线的产品能力。

## 产品理念

ExamO 不只是希望回答学习问题，还希望理解学生正在学习什么，并在合适的时间提供学习支持。学生应理解建议依据、决定是否行动，并保有修改与停止的控制权。

当前证据支持若干用户触发的学习工作流。调用大模型、拥有多个处理步骤或保存任务状态，都不足以单独证明已经具备自主智能体。

## 六个设计方向

| 方向 | 当前基础 | 仍需建立 | 状态 |
| --- | --- | --- | --- |
| Course Awareness · 课程感知 | 用户确认的课程、课表与考试上下文 | 持续可靠的跨课程上下文与明确关联，不虚构教学进度 | In Development |
| Personalized Learning · 个性化学习 | 学习记录、趋势、偏好及部分规则建议 | 验证开放范围、建议依据和用户调整后的效果边界 | In Development |
| Intelligent Reminders · 智能提醒 | 应用内课程与考试信息展示 | 用户授权、调度、投递、撤销与失败处理 | Planned |
| Adaptive Revision · 自适应复习 | 回忆自评、记录与部分复习排期基础 | 验证配置、生效与可解释性，不夸大科学有效性 | In Development |
| Study Task Planning · 学习任务规划 | 部分备考建议和任务安排已有实现，受配置限制 | 与真实课程安排衔接，核验可用性；自主执行单独评估 | In Development |
| Human-in-the-loop · 用户确认与控制 | 上传选择、识别核对、保存确认和个性化开关 | Agent 专用动作预览、权限范围、逐项批准、暂停和撤销 | In Development · Agent 控制层 Planned |

**本轮没有具体智能体能力可标记 Available。** 状态含义与发布要求见[功能状态](features.md)。

## 八项能力审查

| 标准 | 审查结论 | 不能据此宣传的能力 |
| --- | --- | --- |
| 课程上下文感知 | 部分实现，来源于用户输入/确认 | 自动掌握全部学期进度、教务实时同步 |
| 学习记录分析 | 有统计与分析基础，部分能力受配置影响 | 成绩预测、因果学习效果证明 |
| 个性化学习建议 | 有规则建议与偏好基础 | 完全自主的个人学习策略 |
| 工具调用 | 现有调用路径由应用代码和用户操作决定 | 模型自主选择和组合学习工具 |
| 多步骤任务执行 | 有固定学习业务流程 | 模型自主拆解目标并连续完成任务 |
| 用户授权机制 | 有具体流程的确认与用户边界 | 完整的 Agent 工具授权与撤销机制 |
| 任务状态管理 | 有具体任务的排队、处理和结果状态 | 统一的 Agent 目标、计划和执行轨迹 |
| 错误恢复 | 有特定流程的重试、降级和用户恢复入口 | 任意任务自动自愈或保证最终完成 |

## 未来执行边界

未来若建设自主工具使用，至少应先验证：行动范围可见、重要动作需确认、权限可撤销、失败次数有界、执行状态可追踪、重复动作可避免，以及用户能停止任务。学习建议应保留不确定性，不替代学生判断或教师要求。

这些是拟议验收条件，不表示已有通用执行器、后台 Agent 或外部系统权限。本次资料建设不会开发智能体。

## English

**ExamO AI Study Agent is a planned direction, not a released autonomous capability.** The current positioning is a Course-Aware AI Study Assistant.

The aim is to understand what a student is studying, offer help at useful moments, and leave decisions and control with the student. Model API calls, fixed processing steps and stored task states do not by themselves establish autonomous agency.

| Direction | Present foundation | Remaining work | Status |
| --- | --- | --- | --- |
| Course Awareness | User-reviewed course, timetable and exam context | Reliable cross-course context and explicit associations | In Development |
| Personalized Learning | Records, trends, preferences and some rule-based suggestions | Verify availability, rationale and user control | In Development |
| Intelligent Reminders | In-app course and exam displays | Consent, scheduling, delivery, withdrawal and failure handling | Planned |
| Adaptive Revision | Recall feedback, records and some scheduling foundations | Verify enablement and explainability without efficacy claims | In Development |
| Study Task Planning | Some gated planning and task suggestions | Course-schedule integration and release verification; execution assessed separately | In Development |
| Human-in-the-loop | Input selection, content review, confirmation and personalization controls | Agent-specific action previews, scoped approvals, pause and revocation | In Development · Agent controls Planned |

The eight-criteria review found partial course awareness, records analysis and suggestions; application-controlled API calls; fixed multi-step workflows; action-specific confirmations; feature-specific task states; and bounded recovery in some flows. It did **not** establish model-selected tools, autonomous goal execution or a unified Agent permission and execution system. No specific Agent capability is classified as **Available** by this review.

Future autonomous features should require visible action scope, explicit approval for consequential actions, revocable permissions, bounded retries, traceable state, duplicate-action prevention and a stop control. These are proposed acceptance criteria, not existing capabilities or implementation commitments.

[课程管理](course-management.md) · [路线图](roadmap.md)
