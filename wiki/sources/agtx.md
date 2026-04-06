---
type: source
title: "AGTX - AI agent that manages other coding agents"
author: fynnfluegge
url: https://github.com/fynnfluegge/agtx
date: 2026-04-06
tags: [AI, Agent, 开源, Rust, 多智能体]
sources: []
---

# AGTX - 来源摘要

## 项目概述

AGTX 是一个用 Rust 编写的开源项目，实现了"管理其他 AI 编程代理"的终端看板工具。

## 核心功能

1. **Orchestrator Agent** - AI 代理自动管理看板，通过 MCP 协调其他编码代理
2. **多代理协作** - 不同阶段配置不同代理（Gemini→研究 / Claude→实现 / Codex→审查）
3. **并行执行** - 每个任务有独立的 git worktree 和 tmux 窗口
4. **自动合并冲突解决** - 检测并自动处理合并冲突

## 工作流程

```
Planning → Running → Review → Merged
```

## 支持的 AI 代理

Claude Code | Codex | Gemini CLI | OpenCode | Cursor Agent | Copilot

## 安装方式

```bash
curl -fsSL https://raw.githubusercontent.com/fynnfluegge/agtx/main/install.sh | bash
```

## 优缺点

**优点**：安装简单，TMUX 多看板协作

**缺点**：过于复杂，依赖 Cloud Code（易封号、成本高、数量有限）

## 相关概念

- [[多智能体协作]]
- [[AI-Agent]]

## 来源

- https://github.com/fynnfluegge/agtx
