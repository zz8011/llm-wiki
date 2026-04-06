---
type: concept
tags: [AI, Agent, gstack]
created: 2026-04-06
sources: [jason-zuo-gstack-compound-engineering]
---

# gstack

YC CEO Garry Tan 的 Claude Code skills 集合，一个人模拟整支团队。

## 核心命令

| 命令 | 功能 |
|------|------|
| `/plan-ceo-review` | CEO 视角审查，产品视角砍需求 |
| `/plan-eng-review` | 架构视角审查，锁方向 |
| `/qa` | 打开浏览器跑 staging URL，像真实用户一样测试 |

## 定位

**Planner + 浏览器 Evaluator**

- 覆盖决策层和测试层
- "Boil the Lake" 哲学：AI 时代做完整的事边际成本趋近于零

## 与 CE 配合

gstack + Compound Engineering = 完整 harness

- 决策层：gstack
- 规划层：CE
- 执行层：CE
- 审查层：gstack QA + CE reviewer

## 相关来源

- [[jason-zuo-gstack-compound-engineering]]
