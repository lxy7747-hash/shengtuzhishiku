---
type: concept
status: active
created: 2026-06-21
updated: 2026-06-21
tags: [rag, second-brain]
sources:
  - [[wiki/sources/2026-06-21 - LLM维护持久Wiki第二大脑模式.md]]
---

# RAG 与持久 Wiki 的区别

## 定义

RAG 通常在查询时从原始文件中检索相关片段，再由 LLM 生成答案。持久 Wiki 则让 LLM 预先并持续地把来源整合为结构化知识层。

## 核心区别

| 维度 | 传统 RAG | 持久 Wiki |
|---|---|---|
| 知识形态 | 原始 chunk + 临时答案 | 持久 Markdown 页面 |
| 积累方式 | 每次查询重新拼接 | 每次导入与提问都沉淀 |
| 矛盾处理 | 常在查询时临时发现 | 预先标记并持续更新 |
| 用户角色 | 上传文件、提问 | 策展来源、指导探索 |
| LLM 角色 | 检索与回答 | Wiki 维护者与知识编译器 |

## 相关页面

- [[wiki/concepts/持久 Wiki.md]]
- [[wiki/concepts/知识编译层.md]]
