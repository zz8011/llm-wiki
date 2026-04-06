---
type: concept
tags: [AI, Agent, 工程, 知识管理]
created: 2026-04-06
sources: [jason-zuo-gstack-compound-engineering]
---

# Compound Engineering

用知识积累实现 self-improving agent 的工程方法。

## 核心理念

每次工作的产出不只是代码，还有下次能复用的知识。用得越久，agent 越懂你的项目。

## 核心命令

| 命令 | 功能 |
|------|------|
| `/ce:plan` | 并行 spawn research agent，搜历史经验、扫 codebase pattern、读 git history |
| `/ce:work` | 按 plan 增量执行 |
| `/ce:compound` | 并行 spawn 3 个 agent 记录知识到 docs/solutions/ |

## compound 流程

1. **Context Analyzer** - 回溯 session 对话，提取问题类型、涉及组件、症状
2. **Solution Extractor** - 提取：什么没用、什么管用、root cause、怎么预防
3. **Related Docs Finder** - 搜已有 docs/solutions/ 查重
4. **Orchestrator** - 汇总写成结构化文档

## 文档结构

```yaml
---
category: [分类]
---
## Problem
问题描述

## What Didn't Work
排查过程中试了什么没用

## Solution
最终解法和代码

## Prevention
以后怎么避免
```

## 与 Anthropic Harness 对比

| | Anthropic progress file | CE docs/solutions/ |
|--|--|--|
| **性质** | 备忘录 | 知识库 |
| **传递** | 线性（相邻 session） | 指数（所有未来 session） |

## 价值

- **备忘录解决连续性**
- **知识库解决积累性**
- 一个线性，一个指数

## "永续" Agent

> 核心不是 24/7 不停工作，而是 self-improving，避免重复错误。

## 相关来源

- [[jason-zuo-gstack-compound-engineering]]

## 相关工具

- [[gstack]] - 配合使用
- [[Superpowers]] - 对比方案
