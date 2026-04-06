---
type: source
title: "Stitch Agent Skills"
author: google-labs-code
url: https://github.com/google-labs-code/stitch-skills
date: 2026-04-06
tags: [AI, 设计, Google, Stitch, MCP, Agent]
---

# Stitch Agent Skills

**GitHub**: https://github.com/google-labs-code/stitch-skills
**Stars**: 3.9k | **Forks**: 438

## 项目概述

Google Labs 提供的 Stitch Agent Skills 库，用于与 Stitch MCP server 配合工作。

## 可用 Skills

| Skill | 用途 |
|-------|------|
| stitch-design | 统一设计入口，处理提示词增强和设计系统合成 |
| stitch-loop | 从单一提示词生成完整多页网站 |
| design-md | 分析 Stitch 项目生成 DESIGN.md 设计文档 |
| enhance-prompt | 将模糊 UI 想法转化为精炼的 Stitch 提示词 |
| react-components | 将 Stitch 屏幕转换为 React 组件系统 |
| remot | 使用 Remotion 生成演示视频 |

## 安装

```bash
# 列出所有可用 skills
px skills add google-labs-code/stitch-skills --list

# 安装特定 skill
px skills add google-labs-code/stitch-skills --skill stitch-design --global
```

## 核心价值

- DESIGN.md 文件统一全局设计系统
- Claude Code + Stitch + design.md = 设计到代码的完整流程
