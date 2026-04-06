# LLM Wiki Maintenance Guide

这是一个基于 Karpathy llm-wiki 思路构建的个人知识库。

## 目录结构

```
llm-wiki/
├── raw/                  # 原始来源（不可变）
│   └── sources/          # 收集的文档、文章、笔记
├── wiki/                 # LLM 生成的 Wiki（由 AI 维护）
│   ├── entities/         # 实体页面（人物、项目、概念）
│   ├── concepts/         # 概念页面
│   ├── sources/          # 来源摘要页面
│   └── syntheses/       # 综合分析页面
├── index.md             # Wiki 内容目录
├── log.md               # 操作日志
└── CLAUDE.md           # 本文件
```

## 核心原则

1. **raw/ 是只读的** - AI 只读取，不修改原始来源
2. **Wiki 是 AI 的作品** - AI 负责创建、更新、维护所有 wiki 页面
3. **人类负责方向** - 你负责筛选来源、提问、指引分析方向

## 操作规范

### Ingest（新来源）

当你有了新来源（文章、笔记、文档）：

1. 将来源放入 `raw/sources/`
2. 读取来源，提取关键信息
3. 在 `wiki/sources/` 创建来源摘要页
4. 更新 `index.md` 添加新页面
5. 更新相关实体/概念页面（可能需要修改 10-15 个页面）
6. 在 `log.md` 记录 ingest 操作

### Query（提问）

1. 先读取 `index.md` 了解 Wiki 结构
2. 搜索相关页面
3. 综合答案，如有价值可存为新 wiki 页面

### Lint（健康检查）

定期检查：
- 页面间矛盾
- 过时内容
- 孤立页面（无 inbound links）
- 重要概念但无独立页面
- 缺失跨引用

## 页面格式

### 实体页面 (entities/)

```markdown
---
type: entity
tags: [人物, AI]
created: 2026-04-06
sources: []
---

# 实体名称

## 概述
简要说明。

## 关键信息
- 属性1
- 属性2

## 相关页面
- [[相关页面1]]
- [[相关页面2]]

## 来源
- 来源摘要页
```

### 来源页面 (sources/)

```markdown
---
type: source
title: 原始标题
url: 来源链接
date: 2026-04-06
tags: []
---

## 摘要
来源的主要内容摘要

## 关键要点
1. 要点1
2. 要点2

## 与 Wiki 的关联
- [[实体页面]]
- [[概念页面]]
```

## index.md 格式

```markdown
# Wiki Index

## 实体 (entities/)
- [[实体名]] - 一句话描述

## 概念 (concepts/)
- [[概念名]] - 一句话描述

## 来源 (sources/)
- [[来源标题]] - 日期 - 一句话描述

最后更新: 2026-04-06
```

## log.md 格式

```markdown
# Wiki Log

## [2026-04-06] ingest | 来源标题
- 处理了来源
- 创建了 3 个新页面
- 更新了 5 个现有页面

## [2026-04-06] query | 问题摘要
- 回答了关于 xxx 的问题
- 建议进一步研究 yyy
```

## 工具使用

- Obsidian Web Clipper: 采集网页文章
- Ctrl+Shift+D: 下载图片到本地
- Obsidian Git: 版本控制
- Graph View: 查看 Wiki 结构

## 目标

构建一个持久、可复合的个人知识库。
知识越积越厚，AI 越了解你。
