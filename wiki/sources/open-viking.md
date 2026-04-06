---
type: source
title: "OpenViking - Context Database for AI Agents"
author: volcengine
url: https://github.com/volcengine/OpenViking
date: 2026-04-06
tags: [AI, Context, 记忆系统, 火山引擎]
sources: []
---

# OpenViking - 来源摘要

## 项目概述

火山引擎开源的 Context Database for AI Agents，21.2k stars。

## 解决的问题

| 问题 | 传统方案 | OpenViking 方案 |
|------|----------|----------------|
| 碎片化上下文 | 向量存储分散 | 文件系统范式统一 |
| Token 消耗 | 简单截断 | L0/L1/L2 分层加载 |
| 检索效果 | 平面存储 | 目录递归检索 |
| 可观测性 | 黑盒 | 可视化检索轨迹 |
| 记忆积累 | 交互记录 | 自动提取长期记忆 |

## 架构特点

- **文件系统范式** → 统一上下文管理
- **分层加载** → 显著节省成本
- **目录检索** → 递归精确获取
- **自动压缩** → Agent 越用越聪明

## 相关概念

- [[记忆系统]]
- [[上下文管理]]

## 来源

- https://github.com/volcengine/OpenViking
