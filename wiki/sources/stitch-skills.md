---
type: source
title: "Stitch Agent Skills"
author: google-labs-code
url: https://github.com/google-labs-code/stitch-skills
date: 2026-04-06
tags: [AI, 设计, Google, Stitch, MCP, Agent]
sources: []
---

# Stitch Agent Skills - 来源摘要

## 项目概述

Google Labs 提供的 Stitch Agent Skills 库，3.9k stars，用于与 Stitch MCP server 配合工作。

## 核心价值

- DESIGN.md 文件统一全局设计系统
- 以前请设计师要花几千美金等几周，现在一个人一个下午搞定

## 可用 Skills

| Skill | 用途 |
|-------|------|
| stitch-design | 统一设计入口，处理提示词增强和设计系统合成 |
| stitch-loop | 从单一提示词生成完整多页网站 |
| design-md | 分析 Stitch 项目生成 DESIGN.md 设计文档 |
| enhance-prompt | 将模糊 UI 想法转化为精炼的 Stitch 提示词 |
| react-components | 将 Stitch 屏幕转换为 React 组件系统 |

## 工作流

```
Stitch 出设计 → design.md 统一设计系统 → Claude Code 写代码
```

## 安装

```bash
px skills add google-labs-code/stitch-skills --skill stitch-design --global
```

## 相关概念

- [[Google Stitch]]
- [[Claude Code]]

## 来源

- https://github.com/google-labs-code/stitch-skills
