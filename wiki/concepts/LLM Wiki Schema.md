---
type: concept
status: active
created: 2026-06-21
updated: 2026-06-21
tags: [schema, agents]
sources:
  - [[wiki/sources/2026-06-21 - LLM维护持久Wiki第二大脑模式.md]]
---

# LLM Wiki Schema

## 定义

LLM Wiki Schema 是一份操作规范文件，在本 vault 中体现为 [[AGENTS.md]]。它定义目录结构、页面格式、导入流程、查询流程、健康检查规则、引用规范和协作边界。

## 为什么重要

没有 schema，LLM 容易像通用聊天机器人一样临场发挥；有 schema，LLM 会像维护代码库一样维护 Wiki：先读索引，按规则编辑，更新日志，验证链接。

## 当前实现

- 控制文件：[[AGENTS.md]]
- 内容目录：[[index.md]]
- 时间日志：[[log.md]]
- 核心工作流：[[wiki/workflows/Ingest 工作流.md]]
