---
layout: default
title: "课程管理与课程相关提醒 | ExamO"
description: "Course import establishes context; in-app cues and planned background reminders are distinct."
lang: zh-CN
review_date: 2026-10-19
---

# 课程管理与课程相关提醒 / Courses and reminders

核验日期 / Reviewed: **2026-10-19**。

## 课程导入的作用

课程导入帮助建立学生正在学习的课程、上课时段及用户主动填写的考试信息，为应用内日程展示和未来的课程相关提醒提供上下文。

**它不等于上传课件，不会因为输入课程名称就自动生成题库。** 学习资料通过独立入口上传和核对；新资料也不能宣传为已经自动归入课表中的课程。

## 当前实现基础

| 项目 | 边界 | 状态 |
| --- | --- | --- |
| 手动添加课程 | 用户维护课程、学期、时段与考试信息 | In Development · 发布待核验 |
| 课表截图识别 | 支持图像输入，结果可修改、选择并确认后保存；可能识别错误 | In Development · 发布待核验 |
| 今日课程与考试临近信息 | 用户打开应用时查看安排与倒计时，依赖准确的用户确认信息 | In Development · 发布待核验 |
| 后台主动提醒 | 未发现完整的订阅授权、时间调度和通知投递实现 | Planned |
| 教务系统自动同步、系统日历联动 | 未发现完整接入，不宣称已支持 | Planned |
| 跨课程空闲时段自动排期 | 不能从已存在的学习计划建议推断为已实现 | Planned |

课程截图应裁去姓名、学号及其他无关信息。识别结果需要核对课程名、日期、周次和时段；课程时间不能自动当作考试时间。

## 目标流程与尚未打通的部分

课程信息 → 课程相关提醒 → 学习资料 → AI 辅助练习 → 持续复习。

课程信息与后面若干学习流程已有实现基础；后台通知和整体自动联动仍需建设。未来提醒应由学生明确选择时间、渠道与范围，并能暂停或撤销。此处是产品方向，不是已发布服务承诺。

## English

Course import establishes context about the student's classes, class times and voluntarily entered exam details. **It is separate from importing study materials and does not create a question bank from a course name.** Automatic binding between new materials and timetable courses has not been established.

Manual course entry, reviewed timetable-image import and in-app views of classes and approaching exams have implementation foundations. Their public release remains unverified (**In Development**). In-app displays are not background notifications.

Consented notification delivery, university-system synchronization, calendar integration and automatic scheduling around free time across courses are **Planned**. The intended connection from course information to reminders, materials, practice and revision is a design direction, not an already verified automated chain.

Students should remove names and student numbers from timetable images, then check recognized names, dates, weeks and times. Future reminders should support explicit choices of timing, channel and scope, with pause and withdrawal controls.

[功能状态](features.md) · [AI Study Agent](ai-study-agent.md)
