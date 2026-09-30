---
type: workflow
status: active
created: 2026-06-21
updated: 2026-06-21
tags: [ai-image, workflow, ingest]
sources:
  - [[wiki/sources/2026-06-21 - LLM维护持久Wiki第二大脑模式.md]]
---

# AI 生图资料 Ingest 工作流

## 目的

把 AI 生图相关资料导入第二大脑，并拆解为可复用的提示词结构、工具经验、人物 DNA、风格质感、工作流或案例。

## 输入

- `raw/sources/` 中的新来源。
- `提示词/` 中的既有笔记。
- 用户粘贴的提示词、案例、图片说明或生成复盘。

## 步骤

1. 读取 [[AGENTS.md]]、[[index.md]]、[[wiki/maps/AI 生图知识库地图.md]] 和 [[wiki/concepts/AI 生图 Taxonomy.md]]。
2. 判断资料类型：模板、案例、工具说明、技巧、人物设定、风格词、工作流、问题复盘。
3. 提取 AI 生图字段：
   - 目标效果
   - 适用工具 / 模型
   - 提示词结构
   - 可替换变量
   - 失败模式与负面约束
   - 图片证据或附件
   - 可复用结论
4. 创建或更新来源摘要页。
5. 更新相关概念页：[[wiki/concepts/提示词工程.md]]、[[wiki/concepts/人物 DNA.md]]、[[wiki/concepts/风格与质感.md]]、[[wiki/concepts/生图工作流.md]]。
6. 如果涉及具体工具，更新实体页，例如 [[wiki/entities/GPT Image.md]]。
7. 如果是可复用模板，后续可创建模板页或问题页。
8. 更新 [[index.md]] 和 [[log.md]]。

## 输出格式建议

导入一篇 AI 生图资料时，来源摘要页应包含：

```markdown
## 一句话摘要
## 适用工具
## 目标效果
## 提示词结构
## 可复用变量
## 失败模式 / 负面约束
## 示例与证据
## 可沉淀为
## 相关页面
## 后续问题
```

## 验证清单

- [ ] 是否链接原始资料或既有笔记。
- [ ] 是否归入 [[wiki/concepts/AI 生图 Taxonomy.md]] 的至少一个类别。
- [ ] 是否更新相关工具 / 概念页。
- [ ] 是否记录可复用模板或失败模式。
- [ ] 是否更新 [[index.md]] 和 [[log.md]]。
