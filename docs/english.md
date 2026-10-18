---
layout: default
title: "ExamO | AI Study Assistant for Exam Preparation"
lang: en
---

# ExamO — AI Study Assistant

[中文介绍](index.html) · [Product website](https://chenb5408-bit.github.io/ExamO/) · [Security](security.html)

ExamO (易考鸥) is an enterprise project for AI-assisted learning and exam preparation on WeChat. It connects course materials, practice, review and explanation so learners can study with clearer structure and more useful feedback.

## Product capabilities

- Organize course materials and study tasks.
- Parse learning materials and prepare practice; uploaded question papers follow the original-question workflow.
- Answer questions and review feedback and weak areas.
- Reinforce understanding through error review, flashcards and self-assessment.
- Explain concepts in plain language with Feynman-style practice and AI follow-up questions.
- Use learning records to inform subsequent review.

## Sample screens

These are screenshots from product development, provided as illustrative references rather than a guarantee of the current interface. No real user account, private learning record or uploaded document is shown.

<img src="assets/screenshots/review.png" width="260" alt="ExamO review tools" /> <img src="assets/screenshots/feynman.png" width="260" alt="ExamO Feynman explanation practice" />

## Architecture

WeChat Mini Program → application services → learning and practice capabilities → persistent storage. The high-level stack includes Node.js, Express, SQLite, document parsing and AI service integration. Provider credentials remain on the server. See [architecture](architecture.html); no infrastructure identifiers or production endpoints are published.

## Status and access

The maintainer reports development complete as of 19 October 2026. The project is in maintenance and product-presentation phase. This repository does not claim public registration availability, certification or service-level guarantees.

- [Product website](https://chenb5408-bit.github.io/ExamO/)
- [Product questions and feedback](https://github.com/chenb5408-bit/ExamO/issues/new/choose)
- [Maintainer and cooperation inquiries](https://github.com/chenb5408-bit); no dedicated business email is currently published.
- Authorized source access: [mini-program](https://github.com/chenb5408-bit/examo-miniapp), [backend](https://github.com/chenb5408-bit/examo-backend). Private repositories normally return 404 for unauthorized visitors.
- Mini-program access is supplied by the maintainer; no public release link or QR code is invented here.

## Repository boundaries

This public repository contains reviewed product documentation and screenshots only. Application source, secrets, user data, databases and internal deployment details are excluded. No open-source license is added. Access to source code or permission to reuse product assets must be obtained separately.

AI-generated content is a study aid and should be checked against authoritative course materials. For sensitive reports use [private vulnerability reporting](https://github.com/chenb5408-bit/ExamO/security/advisories/new), not public issues.

Keywords: ExamO, WeChat Mini Program, AI education, exam preparation, study assistant, miniprogram, flashcard review, Feynman learning.
