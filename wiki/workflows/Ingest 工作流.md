---
type: workflow
status: active
created: 2026-06-21
updated: 2026-06-21
tags: [workflow, ingest]
sources:
  - [[wiki/sources/2026-06-21 - LLM维护持久Wiki第二大脑模式.md]]
---

# Ingest 工作流

## 目的

把一个新来源从 `raw/` 编译进 `wiki/`，让它产生持久、可链接、可复用的知识增量。

## 触发条件

用户说：“导入这个来源”、“ingest @文件名”、“把这篇文章纳入 wiki”。

## 输入

- 一个或多个 raw source。
- 用户对重点、领域、输出形式的偏好。

## 步骤

1. 读取 [[AGENTS.md]]、[[index.md]] 和最近的 [[log.md]] 条目。
2. 读取待导入来源，必要时查看附件图片。
3. 提取摘要、论点、事实、概念、实体、矛盾、后续问题。
4. 创建或更新 `wiki/sources/` 来源摘要页。
5. 更新相关 `wiki/concepts/`、`wiki/entities/`、`wiki/synthesis/` 页面。
6. 增加双向语义链接。
7. 更新 [[index.md]]。
8. 追加 [[log.md]]。
9. 报告变更与验证。

## 验证清单

- [ ] 来源摘要页链接到 raw source。
- [ ] 新增页面已出现在 [[index.md]]。
- [ ] `log.md` 有 append-only 记录。
- [ ] 关键概念至少有一个交叉链接。
- [ ] 矛盾和待验证点没有被隐藏。
