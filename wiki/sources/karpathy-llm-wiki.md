---
type: source
title: LLM Wiki
author: Andrej Karpathy
url: https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f
date: 2026-04-05
tags: [AI, 知识管理, LLM, 个人知识库]
sources: []
---

# LLM Wiki - 来源摘要

## 核心思想

Karpathy 提出用 LLM 增量构建和维护一个持久化的 Wiki，区别于 RAG 的"每次从零开始检索"。

## 关键要点

1. **持久积累** - Wiki 是可复合的产物，跨引用已建立，矛盾已标记
2. **三层架构** - Raw sources / Wiki / Schema (CLAUDE.md)
3. **操作流程** - Ingest / Query / Lint
4. **AI 负责维护** - 人类负责选素材、提问、思考

## 工具栈

- Obsidian Web Clipper（采集）
- Obsidian Git（版本控制）
- qmd（本地搜索）
- Marp（幻灯片）
- Dataview（数据库查询）

## 延伸阅读

- [[老张-Karpathy-Obsidian教程]] - 落地实践

## 来源

- 原始：https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f
