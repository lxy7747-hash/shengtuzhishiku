# AGENTS.md — LLM Wiki 第二大脑操作架构

本 vault 是一个由 LLM 代理维护的持久 Markdown Wiki。Obsidian 是 IDE；LLM 是维护者；Wiki 是持续演化的知识代码库。

## 0. 核心原则

1. **Raw sources 不可变**：`raw/` 是事实来源。LLM 可以读取、引用、补充新来源，但不得修改已有原始来源内容；如需修正，新增一个更正来源或在 wiki 层注明。
2. **Wiki 可演化**：`wiki/` 由 LLM 维护。可以创建、更新、重构页面，但必须保留来源引用与变更脉络。
3. **先理解，后编辑**：任何非平凡操作前，先读取 `index.md`、相关 wiki 页面、相关 raw 来源，再做最小必要修改。
4. **持久积累**：聊天里的有价值结论、比较、分析、问题答案，应尽可能沉淀进 `wiki/`，而不是只留在对话中。
5. **显式引用**：所有事实性主张应尽量链接到来源摘要页或 raw source。无法确认的内容标注为“待验证”。
6. **矛盾优先暴露**：新来源与旧结论冲突时，不要偷偷覆盖；在相关页面加入“矛盾 / 更新”小节，并记录到 `log.md`。
7. **Obsidian 原生**：内部链接使用 `[[...]]`；图片使用 `![[...]]`；页面以 Markdown + YAML frontmatter 组织。

## 1. 目录结构

```text
raw/                         # 原始来源，原则上不可修改
  sources/                   # 文章、剪藏、论文、访谈、章节等 markdown/text/pdf 说明
  assets/                    # 本地图片、附件、截图
wiki/                        # LLM 维护的知识层
  sources/                   # 每个来源的结构化摘要页
  concepts/                  # 概念页、主题页、方法论页
  entities/                  # 人物、组织、项目、工具等实体页
  workflows/                 # 可重复执行的工作流
  questions/                 # 由问题沉淀出的分析页、比较页、答案页
  synthesis/                 # 跨来源综合、当前观点、演化中的 thesis
  maps/                      # 导航图、MOC、领域地图
outputs/                     # 可交付物：slide、chart、html、报告等
tools/                       # 可选脚本和本地工具
index.md                     # 内容目录：当前 wiki 的地图
log.md                       # 时间日志：append-only
AGENTS.md                    # 本文件：LLM 操作架构
```

## 2. 页面类型与 frontmatter

所有 LLM 创建的 wiki 页面建议包含 frontmatter：

```yaml
---
type: source-summary | concept | entity | workflow | question | synthesis | map
status: seed | active | stable | deprecated | needs-review
created: YYYY-MM-DD
updated: YYYY-MM-DD
tags: []
sources: []
---
```

## 3. 三个核心操作

### 3.1 Ingest：导入新来源

触发语示例：“导入这个来源”、“ingest @raw/sources/xxx.md”、“把这篇文章纳入 wiki”。

流程：

1. 读取 `index.md`，了解现有结构。
2. 读取待导入来源；若来源包含本地图片，必要时查看图片。
3. 提取：一句话摘要、核心论点、关键事实、概念、实体、待验证点。
4. 在 `wiki/sources/` 创建或更新来源摘要页。
5. 更新相关 `wiki/concepts/`、`wiki/entities/`、`wiki/workflows/`、`wiki/synthesis/` 页面。
6. 在相关页面加交叉链接，避免孤岛。
7. 更新 `index.md` 的内容目录。
8. 追加 `log.md` 条目。
9. 向用户报告：变更文件、关键结论、验证结果、待确认问题。

### 3.2 Query：基于 wiki 回答问题

流程：先读 `index.md`；读取相关 wiki 页面；必要时回看 raw 来源；回答时使用 `[[页面]]` 引用；若答案有长期价值，创建 `wiki/questions/` 或更新 `wiki/synthesis/`；更新 `index.md` 与 `log.md`。

### 3.3 Lint：健康检查

检查孤立页面、缺失页面、旧结论、矛盾、坏链接、index drift、source coverage。输出可写入 `wiki/synthesis/Wiki 健康检查.md`，并追加 `log.md`。

## 4. `index.md` 维护规则

`index.md` 是内容地图，不是时间线。每个页面使用一行：

```markdown
- [[wiki/concepts/概念名.md]] — 一句话说明。
```

每次新增、重命名、删除 wiki 页面，都更新 `index.md`。

## 5. `log.md` 维护规则

`log.md` 是 append-only 时间线。不要重写历史条目，除非用户明确要求。

条目格式：

```markdown
## [YYYY-MM-DD] ingest | 标题

- 输入：[[raw/sources/xxx.md]]
- 变更：[[wiki/sources/xxx.md]], [[wiki/concepts/yyy.md]]
- 摘要：一句话说明本次做了什么。
- 待办：可选。
```

操作类型建议：`ingest`、`query`、`lint`、`refactor`、`maintenance`。

## 6. 命名规范

- 中文页面优先使用中文标题。
- 文件名避免特殊符号：`<>:"/\|?*`。
- 来源摘要：`YYYY-MM-DD - 标题.md`。
- 概念、实体、工作流：直接用清晰名称，如 `持久 Wiki.md`。
- 页面链接优先写完整相对路径：`[[wiki/concepts/持久 Wiki.md]]`。

## 7. 引用与证据规则

- 来源摘要页必须链接 raw source。
- 概念页的关键定义至少链接一个来源摘要页。
- 综合页必须区分：事实、解释、推测、待验证。
- 网络检索所得信息需要记录访问日期与 URL；若来源会变化，优先保存到 `raw/sources/`。

## 8. 与用户协作规则

LLM 默认可以执行：新建 wiki 页面；更新相关交叉链接；更新 `index.md` 与 `log.md`；对明显的格式和链接问题做小修。

LLM 应先询问用户：删除页面或大规模重命名；改变目录结构；批量导入大量来源；对存在争议的 synthesis 做强结论改写。

每次完成后简要报告：结果、变更文件、验证方式、待确认 / 后续建议。

## 9. 默认启动例程

每个新会话中，如果用户要求维护第二大脑：读取 `AGENTS.md`；读取 `index.md` 和最近 5 条 `log.md`；根据任务读取相关页面；按 Ingest / Query / Lint / Maintenance 流程执行。

## 10. 当前第二大脑的初始主题

本 vault 的主领域是：**AI 生图知识库**。

元主题是：**LLM 代理维护的持久个人 Wiki / 第二大脑**。

初始目标：把原始来源编译为可演化的 Obsidian Wiki；让知识通过 ingest、query、lint 持续复利；用 `AGENTS.md` 保持代理行为稳定。

## 11. AI 生图领域规范

当用户要求整理、导入、分析 AI 生图相关内容时，默认按 [[wiki/maps/AI 生图知识库地图.md]] 与 [[wiki/concepts/AI 生图 Taxonomy.md]] 归档。

### 11.1 主要知识类别

- **模型 / 工具**：GPT Image、Midjourney、Stable Diffusion、Flux、ComfyUI、LoRA、ControlNet 等。
- **提示词工程**：提示词模板、正向提示词、负向提示词、提示词优化、反推。
- **人物 DNA**：角色一致性、脸型、身材、发型、服饰、姿态、身份设定。
- **风格与质感**：真人感、摄影感、胶片感、动漫风、材质、光影、色彩。
- **场景与构图**：地点、镜头、景别、角度、空间关系、背景细节。
- **工作流**：从构思、生成、反推、迭代、修复、放大、归档到复用的流程。
- **案例库**：一次生成任务的输入、输出、参数、失败点、可复用经验。
- **评估标准**：一致性、真实感、清晰度、审美、可控性、商用风险。

### 11.2 AI 生图来源导入规则

导入 AI 生图来源时，除通用 ingest 字段外，优先提取：

- 适用模型 / 工具。
- 目标效果。
- 可复用提示词结构。
- 关键变量：主体、场景、风格、镜头、光线、材质、动作、情绪、参数。
- 负面约束或常见失败点。
- 示例图片与本地附件。
- 可沉淀为模板、工作流或案例的部分。

### 11.3 既有资料处理

当前 `提示词/` 目录视为用户已有工作资料。LLM 不主动搬动或重命名其中内容；需要纳入第二大脑时，应逐篇读取并在 `wiki/` 中创建摘要、概念、模板或案例页，再建立回链。
