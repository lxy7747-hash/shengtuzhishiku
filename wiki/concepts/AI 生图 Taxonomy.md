---
type: concept
status: active
created: 2026-06-21
updated: 2026-09-16
tags: [ai-image, taxonomy]
sources:
  - [[AGENTS.md]]
  - [[wiki/sources/2026-06-21 - LLM维护持久Wiki第二大脑模式.md]]
---

# AI 生图 Taxonomy

## 定义

AI 生图 Taxonomy 是本 vault 对 AI 图像生成知识的分类法。它决定新来源、提示词、案例和经验应该被拆解到哪些页面中。

## 一级分类

| 类别 | 用途 | 典型页面 |
|---|---|---|
| 模型 / 工具 | 记录不同生成工具的能力、限制、参数和经验 | [[wiki/entities/GPT Image.md]] |
| 提示词工程 | 管理提示词结构、优化方法、反推和模板 | [[wiki/concepts/提示词工程.md]]、[[wiki/concepts/GPT Image 结构化提示词 schema.md]] |
| 人物 DNA | 管理角色一致性、外貌、身材、服饰、身份设定 | [[wiki/concepts/人物 DNA.md]]、[[wiki/concepts/人物身材基线.md]] |
| 风格与质感 | 管理视觉风格、摄影感、材质、光影、色彩 | [[wiki/concepts/风格与质感.md]] |
| 场景与构图 | 管理空间、镜头、景别、角度、背景细节 | [[wiki/concepts/场景与构图.md]] |
| 工作流 | 管理从需求到成品的可重复步骤 | [[wiki/concepts/生图工作流.md]]、[[wiki/workflows/反推工作流.md]] |
| 案例库 | 记录一次具体生成任务的输入、输出和复盘 | [[wiki/sources/2026-05-16 - 角色三视图与图片资产.md]]（首个资产登记，内容待用户补全） |
| 评估标准 | 定义好图、坏图、可用图的判断标准 | [[wiki/concepts/评估标准.md]]（六维度框架已定，通过线待定） |

> **结构说明**：本库不为「案例库」另建目录，案例按 [[AGENTS.md]] 的前缀分型落在 `wiki/sources/`（图像资产、生成复盘）或 `wiki/questions/`（一次具体问题的分析）。见 [[wiki/synthesis/Wiki 健康检查.md]] 中关于目录结构的说明。
>
> **空分类已清零**：2026-09-16 之前「场景与构图」「案例库」「评估标准」三类均标注「待创建」，现已各自有页面。其中「案例库」仅有资产登记、尚无完整案例，是最薄的一类。

## AI 生图来源的拆解字段

导入资料时优先提取：

- 目标效果：想生成什么。
- 适用工具：哪个模型或平台。
- 提示词结构：主体、场景、风格、镜头、光线、材质、动作、情绪、参数。
- 可复用变量：可替换的角色、地点、服饰、镜头、风格词。
- 失败模式：常见问题、负面提示、需要避免的表达。
- 示例证据：图片、生成结果、参数截图、对比图。
- 复用方式：适合沉淀为模板、工作流、案例还是概念。

## 相关页面

- [[wiki/maps/AI 生图知识库地图.md]]
- [[wiki/workflows/AI 生图资料 Ingest 工作流.md]]
- [[wiki/concepts/提示词工程.md]]
- [[wiki/concepts/GPT Image 结构化提示词 schema.md]]
- [[wiki/concepts/人物 DNA.md]]
- [[wiki/concepts/人物身材基线.md]]
- [[wiki/concepts/风格与质感.md]]
- [[wiki/concepts/场景与构图.md]]
- [[wiki/concepts/评估标准.md]]
- [[wiki/concepts/生图工作流.md]]
- [[wiki/workflows/反推工作流.md]]
