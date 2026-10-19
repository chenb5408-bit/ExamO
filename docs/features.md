---
layout: default
title: "功能与可用性 | ExamO"
description: "Implemented foundations, release evidence and planned capabilities."
lang: zh-CN
review_date: 2026-10-19
---

# 功能与可用性 / Features and availability

核验日期 / Reviewed: **2026-10-19**。本页区分实现证据、对外开放和规划；代码存在、配置默认值与生产发布是不同结论。

## 状态约定 / Status definitions

| 状态 | 中文 | English |
| --- | --- | --- |
| Available | 已有日期、版本和体验证据支持对外提供使用 | Verified as offered to users, with release or experience evidence |
| In Development | 有实现或集成基础，但配置、生效范围或发布验收尚未核实 | Implementation or integration exists; enablement or release acceptance remains unverified |
| Planned | 未发现完整闭环，只能作为发展方向 | No complete implementation was found; a direction, not a shipping commitment |

公开仓库和产品资料官网可访问。**本轮没有核实具体业务功能已上线，不把它们列为 Available。** This review verified public documentation, not a live release of the study service.

## 已实现基础 / Implementation found

| 功能 / Capability | 能做什么 / Scope | 当前限制 / Boundary | 状态 |
| --- | --- | --- | --- |
| 资料上传与识别 / Materials | 输入文件、图片或文字，识别后核对 / File, image or text input followed by review | 格式与解析能力受运行依赖影响，不保证任意资料都能准确识别 / Parsing depends on supported formats and runtime dependencies | In Development |
| 原题练习 / Original questions | 使用资料中解析出的原题 / Work with questions extracted from uploaded papers | AI 补充答案应与原始答案区分，并由用户核对 / AI-suggested answers are not original answer keys | In Development |
| AI 辅助练习 / Generated practice | 学习资料进入练习生成与反馈 / Generate practice from study material | 不把原卷任意改写成新题；生成内容可能有误 / Generation is distinct from original-paper practice and may contain errors | In Development |
| 错题与闪卡 / Review | 记录、回忆、自评与讲解反馈 / Records, recall, self-assessment and feedback | 失败处理与同步范围有边界；不宣称经过验证的个人遗忘曲线 / No claim of seamless synchronization or a validated personal forgetting curve | In Development |
| 讲题与费曼练习 / Explanations | 题目解释、讲解、追问、总结与用户选择的巩固练习 / Explanations, learner-led discussion and optional consolidation | 录音后的转写不等于实时语音理解；部分保存只在本机 / Post-recording transcription is not real-time voice understanding; some saved content is device-local | In Development |
| 课程与考试信息 / Courses | 课表图核对导入、手动录入、考试信息与应用内展示 / Reviewed timetable import, manual entry and in-app views | 不自动同步教务，也不把课程导入当作资料导入 / No claim of automatic university-system synchronization | In Development |
| 学习记录与偏好 / Records | 历史、趋势、薄弱点和可调整偏好 / History, trends, weak areas and preferences | 不构成成绩预测、能力认证或学习效果的因果证明 / Not a grade prediction, certification or causal efficacy claim | In Development |
| 个性化复习与学习建议 / Suggestions | 规则建议、复习安排和备考任务建议的实现基础 / Foundations for revision and task suggestions | 部分能力需要相应配置与验收，不代表完整课表避让排程 / Some functions are gated; no claim of complete timetable-aware scheduling | In Development |

## 尚待建设 / Planned capabilities

- 后台课程/考试提醒的授权、调度、投递、撤销和失败处理 / Consented background reminders with delivery and cancellation.
- 统一的 Agent 目标、计划、工具权限和执行记录 / Unified Agent goals, plans, tool permissions and execution traces.
- 模型自主选择工具、多步骤执行与可控恢复 / Model-directed tool use and multi-step execution with bounded recovery.
- 基于完整课程安排的跨课程自动排期 / Cross-course scheduling using complete course schedules.

## 如何升级为 Available / Moving a feature to Available

确认版本与开放范围、记录用户路径和验收日期、检查必要授权与失败分支，再同步更新中英文资料。没有这些证据时，维持当前状态，不用截图或历史测试数量代替发布证明。

Record a release and access scope, verify the user journey and failure paths, and update both languages together. Screenshots or historical test counts are not release evidence.

[课程管理](course-management.md) · [智能体状态](ai-study-agent.md) · [路线图](roadmap.md)
