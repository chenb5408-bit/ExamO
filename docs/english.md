---
layout: default
title: "ExamO — Course-Aware AI Study Assistant"
description: "Course context, document-based learning, practice and revision for students. Background reminders and autonomous execution are planned."
lang: en
review_date: 2026-10-19
translation_pair: home
---

# ExamO — Course-Aware AI Study Assistant

[中文](index.md) · [Product website](https://chenb5408-bit.github.io/ExamO/) · [Features](features.md) · [Course management](course-management.md) · [AI Study Agent](ai-study-agent.md)

ExamO (易考鸥) is for students organizing courses, study materials and exam revision. Its product direction brings together document-based learning, AI-assisted practice, flashcard review and course context, with a vision to evolve into a personalized AI Study Agent.

**Status reviewed: 19 October 2026.** The code contains several study workflows, but this review did not verify a production mini-program release or which features are available to users. Course-related support currently has implementation for in-app schedules and exam countdowns; background notifications remain planned. An autonomous AI Study Agent is **Planned**.

## Positioning

Course information provides context about what a student is studying. Materials support practice and understanding. Learning records inform subsequent revision. ExamO aims to connect these parts around the student's actual courses.

**Importing courses establishes course context; it does not import lecture materials or create a question bank.** Uploading textbooks, slides, notes or questions is a separate study-material workflow.

## Core capabilities

| Capability | Implementation found in the review | Public status |
| --- | --- | --- |
| Material recognition | File, image and pasted-text inputs, followed by content review | In Development · release unverified |
| AI-assisted practice | Practice from study materials; uploaded questions follow an original-question workflow | In Development · release unverified |
| Flashcards and error review | Recall, self-assessment, feedback and study records | In Development · release unverified |
| AI explanations and Feynman practice | Question explanations, learner-led explanation, follow-up questions and summaries | In Development · release unverified |
| Course management | Manual entry or timetable-image recognition, with review before saving course and exam information | In Development · release unverified |
| Course-related cues | In-app views of today's classes and approaching exams | In Development · release unverified |
| Learning profiles and revision suggestions | Record analysis, preferences and some suggestion workflows; some capabilities are configuration-dependent | In Development · availability unverified |
| Background course reminders | No complete consent, scheduling and delivery workflow was found | Planned |
| Autonomous AI Study Agent | No complete model-directed tool-selection and goal-execution loop was found | Planned |

Here, **Available** means verified as offered to users. **In Development** also covers implemented capabilities awaiting integration, enablement or release verification. **Planned** describes a direction, not a shipping commitment. This review confirmed no specific business feature as live. See the [feature status reference](features.md).

## AI Study Agent

The long-term aim is to understand what a student is studying, offer support at useful moments, and leave decisions with the student.

Course context, learning records, rule-based suggestions and task states provide parts of that foundation. A fixed sequence such as recognition, review, practice and revision does not by itself establish an Agent that independently plans, selects tools and executes goals.

The proposed direction covers Course Awareness, Personalized Learning, Intelligent Reminders, Adaptive Revision, Study Task Planning and Human-in-the-loop. ExamO does not currently claim to take over study decisions, send proactive reminders or autonomously complete learning tasks. Read the [AI Study Agent brief](ai-study-agent.md).

## Courses and reminders

Students review recognized timetable information before saving it, or enter courses and exam details manually. This information supports in-app schedule displays.

Background notifications, automatic planning around free time across all courses, and autonomous plan execution are not claimed as available. The [course-management guide](course-management.md) separates existing implementation from future reminder capabilities.

## Product screens

These maintainer-supplied screens were previously used in the public showcase. They illustrate development-stage interfaces, not a verified production release or evidence of notification delivery, cross-device synchronization or autonomous Agent execution.

| Review tools | Feynman explanation practice |
| --- | --- |
| <img src="assets/screenshots/review.png" width="270" alt="ExamO development-stage review tools with flashcard and AI explanation entry points" /> | <img src="assets/screenshots/feynman.png" width="270" alt="ExamO development-stage Feynman practice with topic, material and explanation inputs" /> |

No new logo or synthetic interface is introduced. See [asset provenance](screenshots.md).

## Architecture overview

| Layer | Technology and responsibility |
| --- | --- |
| Study interface | Native WeChat Mini Program for courses, materials, practice and revision |
| Application services | Node.js and Express coordinate user-triggered workflows |
| Material processing | Python document parsing and recognition where needed, followed by user review |
| Persistence | SQLite, accessed through Node.js's built-in SQLite interface in the reviewed runtime |
| AI assistance | Server-side model calls for explanations, generation and feedback; outputs require review |

This is a high-level description. Internal endpoints, data structures, infrastructure and credentials remain private. See [architecture](architecture.md).

## What distinguishes the direction

ExamO focuses on students' course context within a WeChat Mini Program, bringing material-based practice, recall and learner-led explanation into one product direction. It explicitly distinguishes uploaded original questions from generated practice.

The intended connection is **course information → course-related reminders → study materials → AI-assisted practice → continued revision**. Several parts have implementation; an integrated automated workflow has not been verified.

Quizlet, Knowt, StudyFetch, Gizmo, Coursicle and Ahead provide useful context for this category. The [product comparison](product-comparison.md) summarizes their published positioning without asserting superiority or a partnership.

## Status, roadmap and updates

Core workflows have code implementations; the scope of a public release remains unverified. Some planning and adaptive-learning capabilities depend on configuration and acceptance checks. The website is a product-information site, not a public registration or download service.

Near-term priorities are release evidence, clear distinctions between in-app cues and background reminders, and verification of personalization availability. User-authorized reminders and learning-task assistance are later directions.

[Roadmap and acceptance criteria](roadmap.md) · [Documentation changelog](changelog.md)

## Official links and feedback

- [Product website](https://chenb5408-bit.github.io/ExamO/)
- [Official public repository](https://github.com/chenb5408-bit/ExamO)
- [Product feedback](https://github.com/chenb5408-bit/ExamO/issues/new/choose); do not attach private study materials.
- [Maintainer contact](https://github.com/chenb5408-bit) for experience access and cooperation inquiries.
- [Private security reports](https://github.com/chenb5408-bit/ExamO/security/advisories/new), requiring sign-in; see [SECURITY.md](security.md).

Core source repositories remain private. This documentation contains no credentials, user records or internal deployment information. No open-source license or source-redistribution permission is added. AI output is a study aid: check it against course materials and question sources. Public visibility does not guarantee indexing, citation or recommendation by any search engine or AI system.
