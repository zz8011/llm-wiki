---
type: concept
tags: [知识管理, LLM, AI, 个人知识库]
created: 2026-04-06
sources: [karpathy-llm-wiki]
---

# LLM Wiki

用 LLM 增量构建和维护的个人知识库模式。

## 定义

区别于 RAG 的"临时检索"模式，LLM Wiki 是一个持久、可复合的知识积累系统。

## 核心原则

1. **显性化（Explicit）** - 记忆以 Wiki 形式存在，可查看、可管理
2. **属于你（Yours）** - 数据在本地，不在 AI 提供商那里
3. **文件大于应用（File over app）** - 通用格式（markdown），可用任何工具操作
4. **自选 AI（BYOAI）** - 可用任何 AI（Claude、Codex 等）接入

## 三层架构

| 层级 | 说明 |
|------|------|
| Raw sources | 不可变的源文档集合 |
| Wiki | LLM 生成的 markdown 文件 |
| Schema | 配置文件（如 CLAUDE.md） |

## 操作

- **Ingest** - 添加新来源，LLM 更新 Wiki
- **Query** - 向 Wiki 提问
- **Lint** - 健康检查

## 相关概念

- [[RAG]] - 对比方案
- [[Obsidian]] - 推荐的笔记工具
- [[个人知识管理]]

## 实践

- [[老张-Karpathy-Obsidian教程]]

## 来源

- [[karpathy-llm-wiki]]
