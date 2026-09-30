---
type: concept
status: active
created: 2026-06-21
updated: 2026-06-21
tags: [second-brain, knowledge-management]
sources:
  - [[wiki/sources/2026-06-21 - LLM维护持久Wiki第二大脑模式.md]]
---

# 持久 Wiki

## 定义

持久 Wiki 是位于原始来源与用户问题之间的结构化 Markdown 知识层。它不是临时查询结果，而是由 LLM 持续维护、可积累、可链接、可审计的知识 artifact。

## 为什么重要

传统 RAG 在每次提问时重新检索片段并拼接答案；持久 Wiki 则把已读来源中的知识编译一次，并在后续导入中持续更新。

## 关键组成

- [[wiki/concepts/原始来源.md]]：不可变事实来源。
- Wiki 页面：概念、实体、来源摘要、问题答案、综合页。
- [[wiki/concepts/LLM Wiki Schema.md]]：规定代理如何维护 Wiki。
- [[index.md]]：内容导航。
- [[log.md]]：时间线和审计记录。

## 相关概念

- [[wiki/concepts/RAG 与持久 Wiki 的区别.md]]
- [[wiki/concepts/知识编译层.md]]
- [[wiki/concepts/知识复利.md]]
