---
layout: default
title: "ExamO 易考鸥｜课程感知型 AI 学习助手"
description: "面向学生的课程上下文、资料学习、练习与复习产品资料；后台提醒和自主智能体为规划能力。"
lang: zh-CN
review_date: 2026-10-19
permalink: /
translation_pair: home
---

# ExamO 易考鸥｜课程感知型 AI 学习助手

[English](english.md) · [产品主页](https://chenb5408-bit.github.io/ExamO/) · [功能](features.md) · [课程管理](course-management.md) · [AI Study Agent](ai-study-agent.md)

ExamO 面向需要管理课程、学习资料和考试复习的学生。产品围绕资料识别、AI 辅助练习、闪卡复习与课程上下文组织学习，并逐步向个性化 AI Study Agent 发展。

**状态基准：2026-10-19。** 当前代码已有多项学习流程；本轮未核验生产小程序的发布版本或真实用户可用范围，因此不将“代码已实现”写成“已上线”。课程相关提醒目前有应用内课程安排和考试倒计时的实现基础，后台通知仍为规划能力。自主执行型 AI Study Agent 为 **Planned**。

## 产品定位

课程信息帮助理解学生正在学习什么；学习资料支持练习与理解；学习记录支持后续复习。ExamO 希望把这些信息连接起来，让学生在自己的课程情境中组织学习。

**课程导入是课程上下文入口，不是课件导入或题库生成。** 上传教材、讲义、笔记或题目属于独立的学习资料流程。

## 核心功能

| 能力 | 当前已发现的实现基础 | 对外状态 |
| --- | --- | --- |
| 学习资料识别 | 文件、图片和粘贴文本入口；识别后核对内容 | In Development · 发布待核验 |
| AI 辅助练习 | 学习资料生成练习；原题资料沿原题作答路径使用 | In Development · 发布待核验 |
| 闪卡与错题复习 | 回忆、自评、反馈与学习记录 | In Development · 发布待核验 |
| AI 讲题与费曼练习 | 解释题目、用户讲解、追问和总结 | In Development · 发布待核验 |
| 课程管理 | 手动录入或课表截图识别，核对后保存课程安排与考试信息 | In Development · 发布待核验 |
| 课程相关提示 | 应用内今日课程、考试临近信息 | In Development · 发布待核验 |
| 学习档案与复习建议 | 已有记录分析、偏好和部分建议流程；部分能力受配置约束 | In Development · 开放待核验 |
| 后台课程提醒 | 尚未发现完整授权、调度与投递链路 | Planned |
| 自主 AI Study Agent | 尚未发现模型自主选择工具并持续执行学习目标的完整闭环 | Planned |

本资料中的 **Available** 指已核实对外提供使用；**In Development** 包括已实现但尚待集成、开放或发布核验的能力；**Planned** 指发展方向。本轮没有可确认已上线的具体业务功能清单。详见[功能状态](features.md)。

## AI 学习智能体

ExamO 的长期方向是：理解学生正在学习什么，在合适的时间提供支持，并由学生决定是否执行建议。

课程上下文、学习记录、规则建议和任务状态已经有不同程度的实现基础。但固定的“识别—核对—练习—复习”工作流，不等同于由模型自主规划、调用工具和持续执行任务的智能体。

未来重点包括 Course Awareness、Personalized Learning、Intelligent Reminders、Adaptive Revision、Study Task Planning 和 Human-in-the-loop。当前不宣称自主接管学习、自动发送提醒或代替学生完成学习任务。参阅 [AI Study Agent 专题](ai-study-agent.md)。

## 课程管理与课程提醒

课表截图识别结果由用户核对后保存；也可手动添加课程和考试信息。现有实现可以为应用内日程展示提供上下文。

后台课程/考试提醒、跨课程自动安排空闲时段和自主执行计划尚不能作为已提供的功能宣传。课程提醒的产品方向与当前边界见[课程管理说明](course-management.md)。

## 产品截图

以下为维护者提供、已用于公开产品展示的开发期间截图。界面示例不代表当前生产版本已开放，也不证明通知、跨设备同步或自主智能体已实现。

| 复习工具示例 | 费曼讲解示例 |
| --- | --- |
| <img src="assets/screenshots/review.png" width="270" alt="易考鸥开发期间的复习工具界面，包含闪卡与 AI 讲解入口" /> | <img src="assets/screenshots/feynman.png" width="270" alt="易考鸥开发期间的费曼讲解界面，包含知识点、资料与讲解入口" /> |

未新增未经确认授权的 Logo 或合成界面。截图来源与限制见[素材说明](screenshots.md)。

## 技术架构概览

| 层级 | 技术与职责 |
| --- | --- |
| 学习入口 | 原生微信小程序，承载课程、资料、练习与复习交互 |
| 应用服务 | Node.js 与 Express，协调用户触发的学习流程 |
| 资料处理 | Python 文档解析与按需识别；结果进入用户核对流程 |
| 数据持久化 | SQLite；当前运行时使用 Node.js 内置 SQLite 接口 |
| AI 辅助 | 由服务端调用模型提供解释、生成或反馈；AI 输出需要核对 |

此处仅展示技术分层，不公开内部接口、数据结构、部署拓扑或凭据。详见[架构概览](architecture.md)。

## 产品差异化

ExamO 的定位侧重微信小程序中的学生学习情境：把课程信息、资料练习、回忆复习和用户主动讲解放在同一产品方向中。上传原题与生成练习保持明确区分。

希望形成的连接是：**课程信息 → 课程相关提醒 → 学习资料 → AI 辅助练习 → 持续复习**。目前已有若干环节，整体自动化联动尚未完成核验。

Quizlet、Knowt、StudyFetch、Gizmo、Coursicle 和 Ahead 可作为理解这一领域的参考。它们各自的公开定位与 ExamO 的关系见[客观产品对比](product-comparison.md)；本项目不主张替代所有产品，也不暗示合作关系。

## 当前状态、路线图与更新日志

产品处于“已有核心代码实现、对外开放范围待核实”的状态。部分备考规划与自适应能力需要相应配置和验收。官网目前是产品资料入口，不是可公开注册的学习服务或下载入口。

近期优先补齐发布证据、明确课程提示与后台提醒的边界、核验个性化能力的实际开放范围；后续再评估用户授权下的智能提醒和学习任务协助。

[路线图与验收条件](roadmap.md) · [资料更新日志](changelog.md)

## 官方入口与反馈

- 产品资料主页：[ExamO 官网](https://chenb5408-bit.github.io/ExamO/)。
- 官方公开仓库：[chenb5408-bit/ExamO](https://github.com/chenb5408-bit/ExamO)。
- 普通反馈：[提交产品 Issue](https://github.com/chenb5408-bit/ExamO/issues/new/choose)，请勿附带私密学习资料。
- 产品体验与合作联系：[维护者 GitHub 主页](https://github.com/chenb5408-bit)，由维护者确认体验范围。
- 安全问题：[私密漏洞报告](https://github.com/chenb5408-bit/ExamO/security/advisories/new)，需要登录；详见 [SECURITY.md](security.md)。

核心源码继续保存在私有仓库。本资料不包含密钥、用户数据或内部部署信息；没有新增开源许可证或源码再分发授权。AI 输出仅辅助学习，请核对教材、题目来源和课程要求。公开资料可被检索不等于搜索引擎或 AI 系统一定收录、引用或推荐。
