---
layout: default
title: "ExamO 路线图 | Roadmap"
description: "Directions and evidence required before release claims."
lang: zh-CN
review_date: 2026-10-19
---

# 路线图 / Roadmap

审查日期 / Reviewed: **2026-10-19**。以下为产品方向与拟议验收条件，没有发布日期或交付时限承诺，也不表示本轮已开发这些能力。

## 当前基础

代码已覆盖课程信息、资料识别核对、练习、闪卡、讲解与学习记录等流程。公开资料页面可访问；具体业务功能的生产版本、开放范围和端到端体验尚待发布证据确认。部分个性化与备考规划能力有配置条件。

## 按证据推进

| 阶段 | 方向 | 状态 | 达到下一阶段前需要的证据 |
| --- | --- | --- | --- |
| 公开资料 | 中英文统一定位、功能状态和可引用专题 | Available · 公开产品资料 | 维护者批准的资料通过 PR 发布；页面与链接需持续维护 |
| 核心体验 | 核实已有学习流程的实际开放范围 | In Development | 可识别的发布版本、体验路径、验收日期与失败边界 |
| 课程相关支持 | 明确应用内提示，评估后台提醒 | In Development · 通知投递 Planned | 用户授权、时间校验、取消、投递结果与失败处理 |
| 个性化复习 | 核实学习记录与偏好如何影响建议 | In Development | 配置核验、建议依据可解释、关闭后行为明确 |
| 学习任务协助 | 连接课程与学习任务的建议和确认 | In Development · 自主执行 Planned | 任务可检查、可修改、可停止，不能自行扩大权限 |
| AI Study Agent | 用户授权下的模型工具选择与多步执行 | Planned | 权限边界、动作确认、状态轨迹、重复防护与有界恢复 |

## 明确不承诺

不承诺自动完成作业、预测考试分数、保证提分、自动接管课表、任意失败自愈或所有学校教务同步。课程导入与学习资料导入保持独立；需要连接时应明确说明依据和用户控制。

## English

This roadmap sets out directions and proposed acceptance criteria, not release dates or delivery promises. This documentation task does not implement the proposed features.

The code contains course, material-review, practice, flashcard, explanation and record workflows. The public documentation site is reachable; the production release and access scope of business features remain unverified. Some personalization and planning capabilities are configuration-dependent.

Priorities are to maintain consistent documentation; verify existing user journeys with release evidence; distinguish in-app cues from planned background notifications; make personalization and opt-out behavior clear; and assess user-controlled task assistance. Autonomous model-directed tools and multi-step execution remain **Planned** and require scoped permissions, action confirmation, state traces, duplicate prevention and bounded recovery.

No grade guarantees, autonomous homework completion, universal university integration or unrestricted recovery are promised.

[功能](features.md) · [AI Study Agent](ai-study-agent.md)
