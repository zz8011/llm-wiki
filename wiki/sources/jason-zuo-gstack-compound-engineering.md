---
type: source
title: "gstack + Compound Engineering 完整分析"
author: Jason Zuo @xxxjzuo
url: https://x.com/xxx111god/status/2038086450013495554
date: 2026-04-06
tags: [AI, 工程, gstack, Agent, Compound Engineering]
sources: []
---

# Jason Zuo-gstack-Compound Engineering - 来源摘要

## 概述

Jason Zuo 详细对比了 gstack、Superpowers 和 Compound Engineering，解释了为什么他认为 CE 是更好的选择。

## Anthropic 的 Harness 架构

核心四个角色：
| 角色 | 功能 |
|------|------|
| Planner agent | 把大任务拆成 feature list |
| Coding agent | 每次只做一个 feature，留结构化笔记 |
| Evaluator agent | 独立审查（不让 builder 评价自己的工作） |
| 跨 session 桥接 | 用 progress file 传递上下文 |

**关键洞见**：Generator-evaluator 分离效果显著提升。Anthropics 用这套架构让 agent 自主开发了完整的 claude.ai 克隆，200+ 可验证 feature。

## 三者对比

### gstack = Planner + 浏览器 Evaluator
- 覆盖决策层和测试层
- `/plan-ceo-review` + `/plan-eng-review` 对应 Planner
- `/qa` 打开浏览器跑 staging URL，像真实用户一样测试
- **优点**：Planning + QA 是最好的
- **缺点**：没有结构化增量执行 workflow，也没有知识积累机制

### Superpowers (120k stars) = 流程有了，深度不够
- brainstorm → plan → execute → review
- 实现了 generator-evaluator 分离
- **缺点**：
  - Plan 基于当前 context，没有历史知识
  - 没有知识积累机制

### Compound Engineering (CE) = 解决知识积累
- `/ce:plan` 并行 spawn research agent 搜历史经验、扫 codebase pattern、读 git history
- `/ce:compound` 并行 spawn 3 个 agent 记录知识：
  - **Context Analyzer**：回溯整个 session 对话，提取问题类型、涉及组件、症状
  - **Solution Extractor**：从 debug 过程提取：什么没用、什么管用、root cause、怎么预防
  - **Related Docs Finder**：搜已有的 docs/solutions/ 查重
- 输出到 `docs/solutions/`，结构化文档

## 关键区别

| | Anthropic progress file | CE docs/solutions/ |
|--|--|--|
| **性质** | 备忘录 | 知识库 |
| **传递** | 线性（相邻 session） | 指数（所有未来 session） |
| **效果** | 连续性 | 积累性 |

## "永续" Agent 的关键

> 核心不是 24/7 不停工作，而是通过持续工作做到 **self-improving**，避免重复错误。

## gstack + CE = 完整 harness

- 决策层：gstack `/plan-ceo-review`、`/plan-eng-review`
- 规划层：CE `/ce:plan`
- 执行层：CE `/ce:work`
- 审查层：gstack QA + CE 并行 reviewer

## 相关概念

- [[gstack]]
- [[Compound Engineering]]

## 来源

- https://x.com/xxx111god/status/2038086450013495554
