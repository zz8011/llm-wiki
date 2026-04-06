---
type: source
title: "OpenViking - Context Database for AI Agents"
author: volcengine
url: https://github.com/volcengine/OpenViking
date: 2026-04-06
tags: [AI, Context, 记忆系统, 火山引擎, 开源]
---

# OpenViking

**GitHub**: https://github.com/volcengine/OpenViking
**Stars**: 21.2k | **Forks**: 1.5k

## 项目概述

"OpenViking: The Context Database for AI Agents"

解决 AI Agent 开发中的上下文管理问题。

## 核心问题

- **碎片化上下文**：记忆在代码中、资源在向量数据库中、Skills 分散
- **上下文需求激增**：长任务产生大量上下文，简单截断会丢失信息
- **检索效果差**：传统 RAG 平面存储，缺乏全局视图
- **不可观测**：隐式检索链像黑盒
- **记忆迭代差**：只是交互记录，缺乏 Agent 相关任务记忆

## 核心特性

| 特性 | 说明 |
|------|------|
| 文件系统范式 | 统一管理 memories、resources、skills |
| 分层上下文加载 | L0/L1/L2 三层，按需加载，节省 token |
| 目录递归检索 | 结合目录定位和语义搜索 |
| 可视化检索轨迹 | 可观测的检索链 |
| 自动 Session 管理 | 自动压缩对话，提取长期记忆 |

## 安装

```bash
pip install openviking --upgrade --force-reinstall
```
