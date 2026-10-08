# Log — 第二大脑操作日志

> 本文件是 append-only 时间线。内容目录请看 [[index.md]]；操作规则请看 [[AGENTS.md]]。

## [2026-06-21] ingest | LLM 维护持久 Wiki / 第二大脑模式

- 输入：用户在聊天中提供的想法文本；已整理为 [[raw/sources/2026-06-21 - LLM维护持久Wiki第二大脑模式.md]]。
- 变更：[[AGENTS.md]], [[index.md]], [[log.md]], [[wiki/sources/2026-06-21 - LLM维护持久Wiki第二大脑模式.md]], [[wiki/concepts/持久 Wiki.md]], [[wiki/concepts/RAG 与持久 Wiki 的区别.md]], [[wiki/concepts/LLM Wiki Schema.md]], [[wiki/concepts/原始来源.md]], [[wiki/concepts/知识编译层.md]], [[wiki/concepts/知识复利.md]], [[wiki/workflows/Ingest 工作流.md]], [[wiki/synthesis/第二大脑初始综合.md]]。
- 摘要：初始化第二大脑架构，把“LLM 持久维护 Obsidian Wiki”模式落地为目录、规则、索引、日志与首批概念页。
- 待办：确认本 vault 是否以 AI 生图知识为主领域，并决定是否创建专门 taxonomy。

## [2026-06-21] maintenance | 确立 AI 生图知识库主领域

- 输入：用户确认“是，继续吧”，表示本 vault 以 AI 生图知识库为主领域继续建设。
- 变更：[[AGENTS.md]], [[index.md]], [[wiki/maps/AI 生图知识库地图.md]], [[wiki/concepts/AI 生图 Taxonomy.md]], [[wiki/concepts/提示词工程.md]], [[wiki/concepts/人物 DNA.md]], [[wiki/concepts/风格与质感.md]], [[wiki/concepts/生图工作流.md]], [[wiki/entities/GPT Image.md]], [[wiki/workflows/AI 生图资料 Ingest 工作流.md]], [[wiki/synthesis/第二大脑初始综合.md]]。
- 摘要：建立 AI 生图领域地图、taxonomy、核心概念页和专用 ingest 工作流，并把既有 `提示词/` 目录作为后续逐篇导入的资料入口。
- 待办：选择下一批 ingest 对象：GPT Image 模板、人物 DNA、提示词优化或临时收集。

## [2026-09-16] maintenance | 增加手机遮挡脸部构图提示词

- 输入：用户提供的“下半脸遮挡为强制构图要求”提示词。
- 变更：[[提示词/02-提示词模板/GPT Image提示词模板/手机遮挡脸部.md]], [[提示词/00-首页/AI生图知识库首页.md]], [[wiki/maps/AI 生图知识库地图.md]], [[wiki/concepts/提示词工程.md]]。
- 摘要：新增可直接复制的手机遮挡脸部模板，保留用户原文，并补充分类与导航入口。

## [2026-09-16] maintenance | 增加遮脸构图的眼神控制

- 输入：用户提供的手机屏幕注视、看镜中自己、接近直视观众三种视线规则。
- 变更：[[提示词/02-提示词模板/GPT Image提示词模板/手机遮挡脸部.md]]。
- 摘要：将手机屏幕注视作为默认推荐，并加入两眼焦点一致、避免冲突视线指令的约束与备用变体。

## [2026-09-16] lint | 全库健康检查

- 输入：用户提问“这个知识库的内容怎么样”。
- 变更：[[wiki/synthesis/Wiki 健康检查.md]]（新建）, [[index.md]]。
- 摘要：全量扫描 37 个 md 与 6 张图片、解析 211 条 wikilink，结论为「元层 A 级、内容层 D 级」；记录 8 个导航死链、6 个概念页来源引用不实、`提示词/` 全部无 frontmatter、5 张图未引用、Taxonomy 中 3 类待创建，并给出 P0–P3 改进优先级。
- 待办：P0 修正来源引用与死链、合并双首页；P1 提炼 GPT Image 结构化提示词 schema 与反推工作流。本次仅落报告，未改动既有内容与链接。

## [2026-09-16] maintenance | 处理健康检查所列问题（P0–P3）

- 输入：用户指令「处理列出的问题吧」；依据 [[wiki/synthesis/Wiki 健康检查.md]] 的问题清单。
- 新增页面：[[wiki/sources/GPT Image 提示词模板集.md]], [[wiki/sources/人物 DNA 笔记集.md]], [[wiki/sources/提示词方法笔记.md]], [[wiki/sources/2026-05-16 - 角色三视图与图片资产.md]], [[wiki/concepts/GPT Image 结构化提示词 schema.md]], [[wiki/concepts/人物身材基线.md]], [[wiki/concepts/场景与构图.md]], [[wiki/concepts/评估标准.md]], [[wiki/workflows/反推工作流.md]], [[提示词/02-提示词模板/GPT Image提示词模板/GPT Image提示词模板.md]]。
- 更新页面：[[index.md]], [[wiki/concepts/AI 生图 Taxonomy.md]], [[wiki/concepts/提示词工程.md]], [[wiki/concepts/人物 DNA.md]], [[wiki/concepts/生图工作流.md]], [[wiki/entities/GPT Image.md]], [[wiki/maps/AI 生图知识库地图.md]], [[wiki/synthesis/Wiki 健康检查.md]], [[提示词/00-首页/AI生图知识库首页.md]], [[提示词/人物DNA总表.md]]。
- 摘要：修复全部 8 个导航死链；为 6 个概念／实体页改正来源引用（原均误指第二大脑模式来源）；建立 3 份来源摘要页把 `提示词/` 的 16 份既有资料纳入 wiki 层；提炼出结构化提示词 schema 与反推工作流两个可复用资产；统一入口为 [[index.md]]；补齐「场景与构图」「评估标准」「案例库」三个此前标注待创建的分类；5 张未引用图像改为资产登记并被引用。
- 未执行：`提示词/` 下文件未加 frontmatter，也未物理移动 `手绘创作指南.md`。原因：这些文件是可直接复制粘贴的提示词载体，加 frontmatter 会污染复制内容；移动文件受 [[AGENTS.md]] 11.3 约束。两者均改为在 wiki 层与模板目录页处理，待用户明确授权后可改。
- 待办：确认 5 张图像的画面内容；补全人物 DNA 的脸型／五官／发型维度与 [[提示词/人物DNA总表.md]] 空字段；为 [[wiki/concepts/评估标准.md]] 确认是否设通过线。

## [2026-09-20] maintenance | 录入核心模特赵凤丽身材 DNA 与基线设定

- 输入：用户提供的模特基础身份与体态数据（赵凤丽，168cm 65kg 丰满型沙漏身材，自然适中C杯不过于丰满，自然饱满健康有张力的臀部，大腿匀称肉感，腰部相对紧实平坦）。
- 变更：[[提示词/人物DNA总表.md]], [[wiki/concepts/人物身材基线.md]], [[wiki/concepts/人物 DNA.md]], [[wiki/sources/人物 DNA 笔记集.md]], [[index.md]], [[log.md]]。
- 摘要：将核心模特「赵凤丽」的姓名、数值参数（168cm/65kg）与丰满沙漏型身材锚点完整落盘，打通提示词总表与 Wiki 概念基线层。
- 待办：确认赵凤丽的面部特征（脸型/五官）、发型发色、年龄区间与核心气质标签。

## [2026-09-20] ingest | 引入并挂载 dual-reference-mirror-selfie 与 objective-image-prompt 两个生图 Skill

- 输入：`C:\Users\m1860\.codex\skills\dual-reference-mirror-selfie`、`C:\Users\m1860\.codex\skills\objective-image-prompt`。
- 变更：`.agents/skills/`（新增 2 个工作区 Skill）、`C:\Users\m1860\.gemini\config\skills/`（新增全局配置）、[[wiki/workflows/双图镜自拍复刻工作流.md]]（新建）、[[wiki/workflows/客观反推工作流.md]]（新建）、[[index.md]], [[log.md]]。
- 摘要：完成 Antigravity 工作区与全局配置的双层挂载，使 Agent 具备基于双图机制与赵凤丽身材母版的镜自拍复刻能力，以及人物身份/身材解耦的客观图像反推能力；同步在 Wiki 知识层沉淀为 2 个可执行工作流。
- 待办：可在后续生图或反推任务中直接调用这两项技能。

## [2026-09-20] ingest | 引入并挂载 realistic-phone-photo-prompts 真实手机摄影 Skill

- 输入：`C:\Users\m1860\.codex\skills\realistic-phone-photo-prompts`。
- 变更：`.agents/skills/realistic-phone-photo-prompts`（工作区 Skill）、`C:\Users\m1860\.gemini\config\skills/realistic-phone-photo-prompts`（全局配置）、[[wiki/workflows/真实手机摄影提示词工作流.md]]（新建）、[[wiki/concepts/风格与质感.md]]（大幅扩充物理与成像维度）、[[index.md]], [[log.md]]。
- 摘要：完成 `realistic-phone-photo-prompts` 的双层挂载与知识编译，确立去 AI 感的核心物理法则（皮肤自然毛孔与色差、丝袜与织物拉伸透肤、接触阴影防悬空、24-28mm手机原相机成像与克制微不对称）；大幅充实此前偏薄的「风格与质感」概念页。
- 待办：在后续提示词编写与去 AI 感微调中深度应用该物理真实感规范。

## [2026-09-20] ingest | 创建并挂载 outfit-prompt-generator 穿搭分析与生成 Skill

- 输入：用户提供的穿搭分析与提示词生成器完整规范指令。
- 变更：`.agents/skills/outfit-prompt-generator`（工作区 Skill）、`C:\Users\m1860\.gemini\config\skills/outfit-prompt-generator`（全局配置）、`C:\Users\m1860\.codex\skills/outfit-prompt-generator`（Codex 配置）、[[wiki/workflows/穿搭分析与提示词生成工作流.md]]（新建）、[[index.md]], [[log.md]]。
- 摘要：创建包含 8 维穿搭前置诊断、默认 5 大风格体系（精准还原/日常/约会/轻熟性感/多巴胺，每类 5 套）、高跟鞋标准约束（尖头细跟 7-9cm 拒绝防水台粗跟）与整段高精度复制格式的专属穿搭生成 Skill，同步在 Wiki 知识层沉淀为可复用工作流。
- 待办：在后续穿搭生图、风格延展任务中随时调用。

## [2026-09-20] maintenance | 构建 PromptStudio AI Web 端项目 (H:\Project\aiProject)

- 输入：用户要求合并方向一（正向拼装）与方向二（双图反推），采用 Dribbble 视觉风格，并指定 Web 项目根目录为 `H:\Project\aiProject`。
- 变更：`H:\Project\aiProject`（完整 Next.js 15 全栈项目落地并启动）、[[log.md]]。
- 摘要：完成 PromptStudio AI Web 应用程序的工程化构建。界面参考 Dribbble 设计规范（药丸导航、4:3 卡片流、#ea4c89 主色）；深度整合赵凤丽身材母版（168cm/65kg C杯沙漏）、六层提示词 Schema、双图反推 9 段式复刻与 5 大穿搭风格矩阵；通过 `pnpm build` 验证并成功启动本地服务 `http://localhost:3001`。
- 待办：体验 Web 界面并根据实战出图反馈持续微调。

## [2026-09-20] refactor | 拼装台「丝袜 / 腿部质感」支持自定义输入与灵感词填入

- 输入：用户反馈「丝袜 / 腿部质感 这块加个自定义得」。
- 变更：`H:\Project\aiProject\src\lib\prompt-schemas.ts`（新增 HOSIERY_QUICK_TAGS 与 SHOE_QUICK_TAGS）、`H:\Project\aiProject\src\components\PromptStudio.tsx`（重构丝袜与鞋履控制块，支持预设/自定义双模、多行自由编辑与快速填入词）、[[log.md]]。
- 摘要：为正向拼装台的「丝袜 / 腿部质感」引入自由自定义能力，提供预设与自定义双向无缝联动、实时可编辑文本域、状态指示角标（✨ 自定义 / 标准预设），并内置「光腿神器、法式波点、浓郁摩卡、中筒小腿袜」等快速填入词；同步对齐鞋履标准的视觉高度与快捷质感，Next.js 构建与热更新验证通过。
- 待办：无。

## [2026-09-21] ingest | 同步生图配方「秋日咖啡厅羊毛高领与20D微透黑丝」至第二大脑

- 输入：[[PromptStudio AI]] 结构化拼装台
- 变更：[[outputs/recipes/2026-09-21 - 秋日咖啡厅羊毛高领与20D微透黑丝.md]], [[index.md]], [[log.md]]
- 摘要：将模特 赵凤丽 的生图配方「秋日咖啡厅羊毛高领与20D微透黑丝」及中英双语 Prompt 自动归档落盘至知识库 outputs 目录。
- 待办：可在实战生图中调用该配方验证出图效果。

## [2026-09-21] ingest | 编译 E:\ai\发图 实战素材与手机双摄防畸变规范

- 输入：`E:\ai\发图\`（0915 运动系及膝袜、0917 居家日常自拍三部曲、手机双摄描述.txt）
- 变更：`H:\Project\aiProject\public\shots\`（导入 4 张高清实拍封面）、`H:\Project\aiProject\src\lib\mock-shots.ts`（置顶 4 套真实实战卡片）、`H:\Project\aiProject\src\components\PromptStudio.tsx`（新增手机双摄防畸变开关）、`E:\obsidian\Warehouse\AI生图知识库\wiki\sources\2026-09-21 - 实战生图素材与手机双摄规范.md`、`E:\obsidian\Warehouse\AI生图知识库\wiki\concepts\手机镜自拍与遮挡技巧.md`、[[index.md]], [[log.md]]。
- 摘要：将实战生图出图案例、局部动作微调链（浅插裤袋/整理碎发）与手机双摄防畸变黄金指令完整编译进知识库概念层，并深度挂载至 Web 端灵感流与拼装台。
- 待办：无。

## [2026-09-22] maintenance | 落地 Phase 1 真实在线生图闭环与 Phase 2 多引擎画幅格式适配器

- 输入：用户指令「依次进行推进吧」推进全生命周期缺失环节。
- 变更：
  - `H:\Project\aiProject\src\lib\prompt-formatter.ts`（新建，定义 4 种黄金画幅比例与 3 大引擎参数转换规则）
  - `H:\Project\aiProject\src\app\api\generate-image\route.ts`（新建，服务端安全生图代理，适配 OpenAI DALL-E 与 SiliconFlow FLUX 协议）
  - `H:\Project\aiProject\src\components\GenerateImageModal.tsx`（新建，Dribbble 风格实时出图与预览弹窗）
  - `H:\Project\aiProject\src\components\SettingsModal.tsx`（扩充生图模型 imageModel 自定义配置项）
  - `H:\Project\aiProject\src\components\PromptStudio.tsx`（集成画幅比例芯片、引擎切换标签与一键在线出图按钮）
  - `H:\Project\aiProject\src\components\ObjectiveLab.tsx`（反推结果区直通在线出图模态框）
  - `H:\Project\aiProject\src\components\DualRefLab.tsx`（双图复刻结果区直通在线出图模态框）
  - `E:\obsidian\Warehouse\AI生图知识库\wiki\workflows\真实在线生图与多引擎适配工作流.md`（新建工作流文档）
  - [[index.md]], [[log.md]]
- 摘要：彻底打通从提示词设计/反推到大模型在线生图的最后一公里。支持 9:16、3:4、1:1、16:9 画幅比例快速切换与 GPT Image、Midjourney、Flux/SD 参数自动装配，本地代理路由通过 `pnpm build` 与 `pnpm dev` 校验并在 3001 端口就绪。
## [2026-09-22] maintenance | 落地 Phase 3 成品质检与瑕疵挑刺体检台 (Quality Auditor & Fixer)

- 输入：用户指令「推进下一步计划」。
- 变更：
  - `H:\Project\aiProject\src\lib\audit-engine.ts`（新建，构建 6 维法医级质检体系、VLM 视觉体检与逆向局部修复指令生成）
  - `H:\Project\aiProject\src\components\QualityAuditor.tsx`（新建，Dribbble 风格成品质检看板，含雷达扫描、0-100评级、瑕疵挑刺清单与一键重新出图）
  - `H:\Project\aiProject\src\types\index.ts`（扩充 TabType 包含 `audit`）
  - `H:\Project\aiProject\src\components\Header.tsx`（新增导航栏第 6 个常驻药丸标签 `成品质检`）
  - `H:\Project\aiProject\src\components\GenerateImageModal.tsx`（出图后支持一键「送入质检挑刺」直通传输）
  - `H:\Project\aiProject\src\components\ShotsFeed.tsx`（样张卡片悬停增加「送入质检」快捷入口）
  - `H:\Project\aiProject\src\app\page.tsx`（集成 QualityAuditor 与修复重绘自动拉起模态框）
  - `E:\obsidian\Warehouse\AI生图知识库\wiki\workflows\成品质检与瑕疵挑刺工作流.md`（新建工作流文档）
  - [[index.md]], [[log.md]]
- 摘要：完成生图生命周期中关键的成品质检与挑刺修复环节。对照赵凤丽 168cm/65kg 沙漏身材、8cm 尖头细高跟接触硬阴影、斜对角双摄（禁三摄）及去磨皮真实度输出 0-100 健康评分并自动生成 Inpainting 修复提示词，支持一键携带修复词重新出图。
- 待办：无。

## [2026-09-22] maintenance | 落地 Phase 4 角色一致性矩阵看板 (Consistency Matrix)

- 输入：用户指令「继续」。
- 变更：
  - `H:\Project\aiProject\src\lib\consistency-engine.ts`（新建，多图 VLM 交叉比对引擎、五维一致性评分标准、特征漂移警示与防漂移黄金锚定锁词生成）
  - `H:\Project\aiProject\src\components\ConsistencyMatrix.tsx`（新建，Dribbble 风格 2~4 栏多视角对比网格、预设组秒级载入、放大预览与锚点导入）
  - `H:\Project\aiProject\src\types\index.ts`（扩充 TabType 包含 `consistency`）
  - `H:\Project\aiProject\src\components\Header.tsx`（新增导航栏第 7 个常驻药丸标签 `一致性`）
  - `H:\Project\aiProject\src\app\page.tsx`（集成 ConsistencyMatrix，打通拼装台与在线出图）
  - `E:\obsidian\Warehouse\AI生图知识库\wiki\workflows\角色一致性矩阵与防漂移工作流.md`（新建工作流文档）
  - [[index.md]], [[log.md]]
- 摘要：实现跨姿态、跨穿搭、跨场景的角色一致性审查系统。支持 2~4 幅图像并排交叉比对，输出五维雷达体检、标出微小特征漂移警示，并提炼黄金防漂移锚定锁词，支持一键注入拼装台或一键生图验证。
## [2026-09-22] maintenance | 落地 Phase 5 生图历史与实战配方相册 (History Gallery & Recipe Vault) 达成全闭环

- 输入：用户指令「完成最后一个闭环环节」。
- 变更：
  - `H:\Project\aiProject\src\lib\history-storage.ts`（新建，本地持久化配方仓储、CRUD、星标收藏与样张种子）
  - `H:\Project\aiProject\src\components\HistoryGallery.tsx`（新建，Dribbble 风格生图历史相册、画幅过滤、全文搜索、大图灯箱、一键回溯拼装台、直通成品质检与 Obsidian 一键同步）
  - `H:\Project\aiProject\src\types\index.ts`（TabType 扩充 `history`）
  - `H:\Project\aiProject\src\components\Header.tsx`（导航栏新增第 8 个常驻药丸标签 `历史相册`）
  - `H:\Project\aiProject\src\components\GenerateImageModal.tsx`（自动接入 saveHistoryRecord，在线出图成功即静默持久化入库）
  - `H:\Project\aiProject\src\components\PromptStudio.tsx`（出图时打包并传递拼装台穿搭蓝图参数）
  - `H:\Project\aiProject\src\app\page.tsx`（挂载 HistoryGallery 视图，打通回溯拼装台与质检跨模块流转）
  - `E:\obsidian\Warehouse\AI生图知识库\wiki\workflows\生图历史与配方相册工作流.md`（新建工作流文档）
  - [[index.md]], [[log.md]]
- 摘要：完成 AI 生图全生命周期治理体系最后闭环。生成出的每张作品与参数均自动入库，支持画幅比例筛选与星标精选，支持一键参数回溯至拼装台二次重构、一键送入挑刺质检雷达，并支持一键通过 API 归档至 Obsidian 第二大脑 outputs/recipes，真正实现创意、出图、质检、沉淀的全流程可循环复利。
- 待办：AI 生图全生命周期 5 大闭环环节已全部圆满交付完成！

## [2026-09-22] refactor | 质检台升级智能画幅识别与截幅鞋跟受力审查豁免

- 输入：用户反馈「图中没有高跟鞋，鞋跟受力与接触阴影这一条就不成立啊，智能一点」。
- 变更：`H:\Project\aiProject\src\lib\audit-engine.ts`（新增 detectImageFraming 构图识别、FramingMode、VLM 截幅审查规则与半身兜底分流）、`H:\Project\aiProject\src\components\QualityAuditor.tsx`（新增智能自动/半身豁免/全身审查 3 档画幅切换器，半身照鞋履维度标记为画外豁免 N/A 且不扣分）、[[log.md]]。
- 摘要：彻底根治非全身截幅图中对脚部与鞋履的幻觉挑刺问题。自动识别半身/腰腹/特写照片，对画面外未露出的鞋跟受力执行「画外豁免 (N/A)」，赋予 100 分满分且权重归零（不扣除总分），同时过滤出图瑕疵列表中的虚构鞋履项；提供 3 档画幅交互按钮供用户随时自由覆盖，Next.js 生产构建并通过编译验证。
- 待办：无。

## [2026-09-24] refactor | 支持从微信直接拖入照片与 Ctrl+V 剪贴板快速粘贴

- 输入：用户反馈「单图反推模块，从微信拖入照片时候无反应」及启动项目指令。
- 变更：
  - `H:\Project\aiProject\src\lib\image-utils.ts`（新增 `detectImageMimeType` 二进制魔数解析、`parseImageFromDataTransfer` 多源拖拽解析器、`parseImageFromClipboard` 剪贴板解析器，自动修复微信临时文件缺失 MIME 类型问题）
  - `H:\Project\aiProject\src\components\ObjectiveLab.tsx`（补全 `onDragEnter/Over/Leave/Drop` 事件，接入微信拖拽与全局 `Ctrl+V` 粘贴监听，增强高亮拖拽视觉反馈）
  - `H:\Project\aiProject\src\components\DualRefLab.tsx`（双图复刻插槽全面接入微信拖拽解析与状态高亮）
  - `H:\Project\aiProject\src\components\QualityAuditor.tsx`（成品质检台全面接入微信拖拽解析与 `Ctrl+V` 粘贴）
  - [[log.md]]
- 摘要：彻底解决从微信电脑版聊天窗口拖放图片无响应的问题。适配微信拖拽时的无类型临时文件、HTML 格式与 URI 链路，支持全局 Ctrl+V 直接粘贴微信图片/截图，全模块生产构建通过并启动于端口 3001。
## [2026-09-24] refactor | 单图反推实验室新增「自定义聚焦反推」功能

- 输入：用户反馈「单图反推我想加个自定义反推，比如我给你一张图，然后只让你反推图中人物得穿搭以及动作，其他不反推」。
- 变更：
  - `H:\Project\aiProject\src\components\ObjectiveLab.tsx`（新增 ExtractionScopeMode 四档聚焦模式：`👗 仅穿搭与动作`、`🔬 全量法医级`、`🛋️ 仅场景与光影`、`✍️ 自由自定义`；提供自定义指令文本域与快捷填入标签；在 AI 多模态 Prompt 中注入排他聚焦铁律，自动将未要求的杂乱背景置换为极简纯净室内环境；同步强化离线兜底规则与过滤）
  - [[log.md]]
- 摘要：为单图反推实验室引入定向反推聚焦体系。用户可一键锁定「仅反推人物穿搭与动作」，精准剥离原图杂乱房间背景，自动生成干净通用的极简摄影环境；亦可自由输入任何微观指定提示词（如仅提取上装或鞋袜），生产构建 Exit Code 0，服务在 3001 端口就绪。
- 待办：无。

## [2026-09-24] refactor | 全链路全面切换为真实大模型（彻底剔除离线假数据 Mock）

- 输入：用户指令「直接都走大模型吧」。
- 变更：
  - `H:\Project\aiProject\src\app\api\ai\route.ts`（支持服务端环境变量 `AI_API_KEY`、`AI_BASE_URL`、`AI_MODEL`，未配置时明确返回 401 提示与友好引导，视觉请求超时延长至 90 秒）
  - `H:\Project\aiProject\src\app\api\generate-image\route.ts`（增加服务端环境变量兜底支持，未配置时明确返回 401 提示）
  - `H:\Project\aiProject\src\lib\ai-client.ts`（安全传参，确保无本地配置时能无缝穿透至服务端环境）
  - `H:\Project\aiProject\src\components\ObjectiveLab.tsx`（彻底移除 offline setTimeout mock 与降级替换逻辑，完全由多模态 VLM 反推，真实报错上报并联动弹出 API 配置）
  - `H:\Project\aiProject\src\components\DualRefLab.tsx`（彻底移除 offline 模板降级，只走真实大模型视觉复刻，透明展示模型调用状态与错误）
  - `H:\Project\aiProject\src\lib\audit-engine.ts` 与 `src\components\QualityAuditor.tsx`（成品质检强制走多模态视觉大模型，彻底杜绝虚假打分与离线假数据）
  - `H:\Project\aiProject\src\lib\consistency-engine.ts` 与 `src\components\ConsistencyMatrix.tsx`（多图角色一致性体检强制走多模态大模型真实比对）
  - [[log.md]]
- 摘要：响应用户「直接都走大模型吧」要求，全系统全量拔除过去用于离线兜底的静默 Mock 模板与延时假逻辑。所有视觉反推、双图解耦、成品质检、多图一致性检测均直连真实多模态大模型 API（如 Qwen2.5-VL、GPT-4o、FLUX），未配置 Key 或接口异常时透明诚实上报真实报错并引导一键配置，`pnpm build` 与本地 3001 端口联调全部通过。
- 待办：无。

## [2026-09-24] fix | 修复反推提示词强制篡改鞋袜（白袜变黑丝、平底变高跟）问题

- 输入：用户反馈「为什么反推图片明明是白袜子，反推出来的提示词是黑袜子，还有鞋子平底鞋为什么提示词写高跟鞋？」。
- 根因定位：
  - 视觉大模型已成功识别出原图连衣裙细节（蓝白格纹、双层白蕾丝刺绣花边内衬等）；
  - 但此前在 `ObjectiveLab.tsx` 与 `DualRefLab.tsx` 的 System Prompt 中硬编码了【鞋袜强制标准：高跟鞋锁定8cm尖头细高跟、丝袜锁定20D黑色微透哑光丝袜】，导致大模型误将该条规则作为不可违抗的硬约束，强行覆盖了原图实际呈现的白色连裤袜与平底玛丽珍鞋。
- 变更：
  - `H:\Project\aiProject\src\components\ObjectiveLab.tsx`（重构 System Prompt、Scope 指令与 User 提示词：明确确立【服饰鞋袜 100% 忠实原图证据原则】，白袜/白丝必须如实反推白袜白丝，平底鞋/玛丽珍必须如实反推具体平底鞋型，严禁脑补改色改款；仅将面部与身材套用母版）
  - `H:\Project\aiProject\src\components\DualRefLab.tsx`（同步修正双图解耦指令中的鞋袜客观性，移除对 8cm 细高跟与黑丝的硬性锁定）
  - `H:\Project\aiProject\src\lib\prompt-translator.ts`（词典新增白色连裤袜、白丝、白棉袜、玛丽珍平底单鞋、运动鞋、乐福鞋中英映射，将地面接触阴影从“细高跟”改为通用“鞋底受力接触硬阴影”，移除 Negative Prompt 中对粗跟/厚底的误伤负向词）
  - [[log.md]]
- 摘要：彻底解除反推模型对黑丝与细高跟的误判锁定，严格遵循 objective-image-prompt 规范中“参考图 100% 提供服饰鞋袜发型配饰，母版仅锁定身材比例与身份”的核心原则。重新编译验证通过（Exit Code 0），服务在 3001 端口正常运行。
- 待办：无。

## [2026-09-24] fix | 修复提示词框无法复制单段与局部划选文字问题

- 输入：用户反馈「提示词框里为什么不能只复制一段」。
- 根因定位：
  - 前端各提示词容器普遍应用了 Tailwind CSS 类名 `select-all`（对应原生 CSS 的 `user-select: all;`）；
  - 根据 W3C CSS 规范，`user-select: all` 属于原子级选择（atomic selection），用户鼠标在框内任意处点击或拖拽时，浏览器均会强制选中整个容器内的所有文本，从而完全阻断了用户按需划选单词、单句或单个段落的交互能力；
  - 同时，界面缺乏分段粒度的复制按键，用户如果只需要穿搭或动作提示词，必须复制全篇后在外部编辑器手动裁切。
- 变更：
  - `H:\Project\aiProject\src\components\ObjectiveLab.tsx`：
    - 移除 `select-all`，替换为 `select-text cursor-text selection:bg-pink-100 selection:text-pink-900`，恢复原生自由划选；
    - 新增鼠标划选监听与浮动操作胶囊：在文本框内划选任意字符即弹出「📋 复制选中文字 (X字)」浮条，点击一键复制；
    - 顶栏新增「📑 分段卡片 (独立复制)」视图：自动根据标题（如【核心任务】、【服饰工艺】、【构图动态】、【负面约束】等）拆解为独立卡片，每卡片配备专属「📋 复制此段」按钮；
    - 「要素拆解卡片」标签页为 5 项微观物理要素（上装、下装、丝袜、鞋履、场景）分别增加独立复制按钮。
  - `H:\Project\aiProject\src\components\DualRefLab.tsx`、`PromptStudio.tsx`、`QualityAuditor.tsx`、`ConsistencyMatrix.tsx`、`GenerateImageModal.tsx`：
    - 全面移除 `select-all`，统一启用 `select-text cursor-text selection:bg-pink-100 selection:text-pink-900`，支持全站任意提示词框随意划词、划句、划段复制。
  - [[log.md]]
- 摘要：彻底根除 `select-all` 导致的全局强制全选问题，恢复各组件提示词的原生任意划选与右键/快捷键复制能力；并在单图客观反推模块增加「分段卡片独立复制」、「鼠标划词浮动复制」与「要素单项复制」三层高阶便捷操作。Next.js 编译验证通过（Exit Code 0）。
- 待办：无。

## [2026-09-27] feature | 落地外部本地素材库 (E:\ai\发图) 主动扫描与增量同步系统

- 输入：用户反馈「有没有主动同步的这个功能，比如我往E:\ai\发图里面添加新素材了，项目却不知道」。
- 变更：
  - `H:\Project\aiProject\src\app\api\sync-local-shots\route.ts`（新建，核心同步后端 API：递归扫描 `E:\ai\发图\` 下的所有子目录如 0915/0917/0926，自动智能配对图片与动作/提示词 `.txt`，增量同步至 Web 静态托管目录 `public/shots/synced/`，并在发现新目录时自动生成 Obsidian 来源笔记）
  - `H:\Project\aiProject\src\lib\history-storage.ts`（新增 `syncLocalShots()` 客户端增量同步逻辑，将外部素材无缝合并至用户本地配方相册，支持本地优先与去重）
  - `H:\Project\aiProject\src\components\HistoryGallery.tsx`（新增「🔄 同步本地素材 (E:\ai\发图)」常驻同步按钮、挂载时静默后台侦测新素材与自动入库 Toast 提醒、新增「📁 本地实战素材」专属分类筛选药丸）
  - `E:\obsidian\Warehouse\AI生图知识库\wiki\sources\2026-09-26 - 实战素材与动作链 (0926).md`（自动同步生成 0926 实战出图与交叉站姿说明来源笔记）
  - [[index.md]], [[log.md]]
- 摘要：打通外部目录 `E:\ai\发图\` 与 Web 应用的自动化同步管道。用户在本地任何时候往该目录添加新照片和 txt 动作描述，进入历史相册时系统均会自动静默侦测并增量同步，亦支持一键手动刷新；同步后的素材可直接回填拼装台、一键出图或直通质检，实现无感扩充实战样张库。
- 待办：无。

## [2026-09-27] feature | 历史相册升级为文件夹相册集结构（封面默认首张素材）

- 输入：用户需求「历史相册按文件夹来分吧，封面用默认用文件夹下的第一张」。
- 变更：
  - `H:\Project\aiProject\src\components\HistoryGallery.tsx`：
    - 重构数据聚合层：新增 `resolveRecordFolder` 与 `albums` 响应式计算，按 `0926`、`0917`、`0915`、`在线出图库` 自动归类分组；
    - **封面规则落地**：严格将每个文件夹内的第一张图片（`sorted[0].imageUrl`）作为相册卡片的封面；
    - 新增**「文件夹相册集视图」**（Folder Albums View）：Dribbble/iOS 照片层叠质感卡片，包含封面大图、`📌 首张默认封面` 标签、文件夹素材数计数、最新更新时间与一键进入交互；
    - 文件夹顶部导航：新增面包屑返回导航 `[ ← 返回全部文件夹 ]`，文件夹内首张照片自动标注 `📌 默认封面` 徽章；
    - 支持「文件夹相册卡片」与「平铺展开全部」双视图一键无缝切换。
  - [[log.md]]
- 摘要：完成历史相册的文件夹化体系重构。各类实战素材（0926 交叉站姿、0917 居家日常、0915 健身房等）均拥有独立相册，并严格以该文件夹下的第一张实战图作为默认封面，极大提升了素材查找效率与视觉审美体验。Next.js 编译验证通过（Exit Code 0）。
## [2026-09-27] ingest | 纳入 E:\ai\发图\素材 厚黑美学策划与分镜例图库

- 输入：`E:\ai\发图\素材\` 目录下新增的 4 组厚黑美学高价值策划图与分镜例图。
- 深度提取与转译：
  - `e34e...`：厚黑美学拍照策划（总纲、造型方案、5大构图法则、4大光影设计）；
  - `a5d9...`：拍摄分镜规划与注意事项（15 大分镜头脚本：全景4/中景7/近景4，及避坑注意事项）；
  - `5ad9...`：厚黑美学参考例图A（六大复古建筑、清水混凝土、红墙与石阶坐蹲构图）；
  - `b18d...`：厚黑美学参考例图B（六大巨石前景、水泥柱框架、中式廊亭、白色箭头引导线与落地窗格构图）。
- 变更：
  - `E:\ai\发图\素材\`（为 4 张例图分别编写并补齐同名精准配对说明 `.txt` 文本）；
  - `H:\Project\aiProject\src\app\api\sync-local-shots\route.ts`（支持从提示词首行标题提取人类可读展示名、优化厚黑美学 5 维预设解析、修复非 4 位数文件夹日期与笔记命名）；
  - `H:\Project\aiProject\public\shots\synced\`（自动增量同步生成 4 张 Web 访问资源）；
  - `E:\obsidian\Warehouse\AI生图知识库\wiki\sources\2026-09-27 - 厚黑美学拍摄策划与分镜例图 (素材).md`（自动编译来源摘要笔记）；
  - `E:\obsidian\Warehouse\AI生图知识库\wiki\concepts\厚黑美学摄影与构图.md`（新建核心概念页：系统梳理造型系统、5大构图几何、4大光影设计与分镜表格）；
  - `E:\obsidian\Warehouse\AI生图知识库\wiki\concepts\场景与构图.md`（增补外景与几何构图高阶延伸章节并建立回链）；
  - `index.md`, `log.md`。
- 摘要：完成对 `E:\ai\发图\素材` 的全流程知识编译与自动入库。不仅 Web 项目历史相册中自动新增了名为「素材」的专属独立相册集（默认首张为封面，并具备清晰分镜说明与穿搭预设），更在 Obsidian 第二大脑中沉淀出「厚黑美学摄影与构图」的全新方法论体系。
- 待办：无。

## [2026-09-27] fix | 修复成品质检体检台送检本地素材时调用模型报错问题

- 输入：用户反馈「成品质检与瑕疵挑刺体检台 调用模型失败」。
- 根因定位：
  - 从后台服务日志捕获到确切的上游拒绝信息：`[AI Proxy Upstream Error] 400: Unsupported file URI type: /shots/synced/0927-3.png`；
  - 用户从【历史相册】或实战素材库点击「送往质检」时，传入的是静态相对路径（如 `/shots/synced/0927-3.png`）；
  - `QualityAuditor.tsx` 与 `audit-engine.ts` 此前直接将相对路径打包到 `image_url` 中发送给大模型；多模态大模型服务商无法访问客户端本地私有相对路径，直接拒收并返回 400 Bad Request。
- 变更：
  - `H:\Project\aiProject\src\app\api\ai\route.ts`（服务端核心兜底：递归扫描 `messages` 中的所有 `image_url`，若检测到以 `/` 或 `http://localhost:` 开头的本地图片路径，自动从项目 `public/` 目录读取并转译为标准 Base64 Data URL 后再请求上游）；
  - `H:\Project\aiProject\src\components\QualityAuditor.tsx`（在 `initialImage` 接收与 `handleRunAudit` 点击触发前，增加前端异步转码与 Base64 格式守卫）；
  - `H:\Project\aiProject\src\lib\audit-engine.ts`（在 `auditGeneratedImage` 入口处增加自动格式检测与 Base64 转换）；
  - [[log.md]]。
- 摘要：完成质检台本地图片多模态链路闭环。无论是从历史相册一键送检的实战素材、拖入的图片还是剪贴板粘贴的图片，系统均能无感完成 Base64 序列化并送达大模型，顺利生成法医级质检体检报告与局部重绘指令。服务已在 3001 端口稳定就绪。
- 待办：无。

## [2026-09-27] fix | 修复在线生图使用文本推理模型导致服务商拒收报错问题

- 输入：用户反馈「开始在线生图报错 生成出错： model 'gemini-3.8-flash-high' is not supported; supported image models: gpt-image-2, grok-imagine-image-quality, grok-imagine-image, grok-imagine-image-pro, grok-imagine-1.0, grok-imagine-1.0-edit, gemini-3.1-flash-image」。
- 根因定位：
  - 用户配置的本地 Gemini 网关服务商将「文本/多模态推理模型（`gemini-3.8-flash-high`）」与「专用生图模型（`gemini-3.1-flash-image`、`grok-imagine-image`、`gpt-image-2`）」严格区隔；
  - 用户此前在生图模型项中沿用了 `gemini-3.8-flash-high`，导致上游生图端点 (`/images/generations`) 拒绝处理并报错。
- 变更：
  - `H:\Project\aiProject\src\app\api\generate-image\route.ts`（服务端智能映射：若检测到传入的 `model` 是文本/推理模型如 `gemini-3.8-flash-high`，自动映射为对应代理支持的 `gemini-3.1-flash-image`；同时兼容 SiliconFlow FLUX.1 与 OpenAI DALL-E 3）；
  - `H:\Project\aiProject\src\components\GenerateImageModal.tsx`（新增「生图模型选择器」交互卡片，支持一键切换 `gemini-3.1-flash-image`、`gpt-image-2`、`grok-imagine-image`、`FLUX.1-schnell`、`dall-e-3` 或自定义输入；报错时提供一键修复按钮）；
  - `H:\Project\aiProject\src\lib\ai-client.ts`（在 `PROVIDER_PRESETS` 中官方新增「Gemini / 本地反代 (3180)」渠道预设）；
  - [[log.md]]。
- 摘要：彻底厘清视觉推理模型与图像生成模型的渠道映射。服务端已实现对 Gemini 代理生图模型的自适应纠错，前端亦提供可视化的生图引擎一键切换与修复体验。
- 待办：无。

## [2026-09-27] refactor | 移除生图弹窗冗余设置框，回归全局API设置并适配Gemini图像网关

- 输入：用户反馈「不需要图中的设置了，直接使用全局API设置」。
- 变更：
  - `H:\Project\aiProject\src\components\GenerateImageModal.tsx`（彻底移除弹窗内的局部模型选择与输入模块，恢复极简沉浸式出图界面；生图模型完全由右上角全局【API 设置】驱动）；
  - `H:\Project\aiProject\src\app\api\generate-image\route.ts`（适配本地反代 Gemini 图像网关的协议细节：自动剔除 OpenAI 样式的 `size` 字段，彻底避免网关将其误转为内部未定义字段 `_imageSize` 导致 Google API 抛出 `INVALID_ARGUMENT` 报错；同时服务端自动保障将 `gemini-3.8-flash` 文本模型平滑转译为真实的 `gemini-3.1-flash-image` 生图模型）；
  - [[log.md]]。
- 摘要：生图弹窗界面恢复极简清爽，完全继承右上角全局 API 设置；服务端完成针对 Gemini 图像生成协议（免传 size 字段与模型自适应）的无感兼容。服务在 3001 端口实时就绪。
- 待办：无。

## [2026-09-27] fix | 修复质检台重新出图只下发局部修图补丁导致生图提示词缺失问题

- 输入：用户反馈「图中发给生图引擎的提示词完全不对啊」（展开后仅见 159 字符的局部微调补丁片段，丢失人物母版、穿搭、场景与负面约束）。
- 根因定位：
  - 此前【成品质检台】的 `report.fixPrompt` 主要面向局部重绘笔刷（Inpainting Patch，如手部噪点、皮带褶皱、去磨皮滤镜）；
  - 点击「携带此修复指令直接重新出图」时，旧代码直接将这一段仅 100 多字符的局部微调补丁当成了全部 Prompt 喂给文生图引擎；
  - 导致生图大模型（FLUX/DALL-E/Gemini）缺失主体（赵凤丽 168cm/65kg C杯沙漏身材）、服饰穿搭、镜自拍构图与生活光影，引发误出图。
- 变更：
  - `H:\Project\aiProject\src\lib\audit-engine.ts`：
    - 多模态 VLM 新增 `fullReGenPrompt` 产出字段，并在 fallback 与解析层新增核心引擎函数 `buildCompleteReGenPrompt`；
    - 智能融合模特赵凤丽黄金 DNA 基准、服饰穿搭、景别构图（半身/全身自适应）、本次质检发现的专属物理修复项以及全局负面约束，合成完整的文生图指令；
  - `H:\Project\aiProject\src\components\QualityAuditor.tsx`：
    - 修复指令 Tab 新增「🎨 完整重构生图词 (Full Prompt)」与「🔧 局部重绘补丁 (Inpaint)」双视图与针对性复制能力；
    - 点击「携带完整修复指令直接重新出图」时，自动打包下发完整重构提示词，彻底告别单薄补丁；
  - `H:\Project\aiProject\src\components\GenerateImageModal.tsx`：
    - 将底部 Prompt 展示区升级为可直接微调编辑的交互文本框，支持出图前自由调整细节，并提供一键「恢复原始 Prompt」；
  - [[log.md]]。
- 摘要：彻底厘清「局部 Inpainting 补丁」与「文生图完整 Re-Gen Prompt」的职责边界。重新出图现已完整携带赵凤丽模特母版与全部场景穿搭细节，支持所见即所得的微调出图。
- 待办：无。

## [2026-09-27] maintenance | 停止本地开发服务，完成阶段性交付

- 输入：用户指令「关闭项目吧」。
- 变更：[[log.md]]。
- 摘要：已安全停止运行在 3001 端口的 Next.js 服务进程并释放端口。本阶段全部功能改造与代码构建验证已顺利落盘交付。
- 待办：下次需要使用时直接运行 `pnpm dev --port 3001` 或通知启动即可。

## [2026-09-29] refactor | PromptStudio AI 全面架构优化与鲁棒性加固

- 输入：用户反馈《PromptStudio AI 项目改进意见（细化版）》（涵盖高优先级：状态管理重构、全局错误边界、技能引擎拆分；中优先级：API 错误脱敏、模特数据持久化解耦、API Key 体验优化）。
- 变更：
  - `H:\Project\aiProject\src\store\useAppStore.ts`（新建：引入轻量级 Zustand 全局状态仓库，收拢 Tab、Model、StudioPreset、AuditTransfer、Toast 等 10+ 项状态，下沉业务交互函数，彻底消除组件 Props 深度层层透传）；
  - `H:\Project\aiProject\src\app\page.tsx`（重构：大幅精简并接入 `useAppStore`，组件与业务逻辑高度解耦）；
  - `H:\Project\aiProject\src\components\ErrorBoundary.tsx`（新建：实现法医级安全隔离与友好异常恢复 UI，支持一键重试、复制错误日志与返回主页）；
  - `H:\Project\aiProject\src\app\layout.tsx`（接入 `ErrorBoundary` 包裹全站根节点，杜绝任何未知报错导致页面白屏）；
  - `H:\Project\aiProject\src\lib\skills-engine.ts`（重构：拆解 260+ 行的单体函数，提取 `buildBodyDescription`、`buildOutfitDescription`、`buildSceneDescription`、`buildPhysicsItems` 与 `buildNegativeConstraints` 模块化纯函数）；
  - `H:\Project\aiProject\src\app\api\ai\route.ts` & `src/app/api/generate-image/route.ts`（重构：对客户端错误返回实施脱敏与分类指导，隐去内部接口端点与底层栈，提供 `isRetryable` 标志区分致命配置错误与临时可重试错误，服务端完整保留诊断日志）；
  - `H:\Project\aiProject\src\lib\model-storage.ts`（新建：实现模特数据从硬编码向 LocalStorage 动态持久化迁移，支持新增、编辑、删除与重置官方出厂模特）；
  - `H:\Project\aiProject\src\components\ModelModal.tsx`（升级：支持在 UI 界面交互式录入新模特身材参数 DNA，并提供自定义模特删除与出厂重置能力）；
  - `H:\Project\aiProject\src\components\SettingsModal.tsx`（升级：API Key 支持掩码预览 `sk-xxxx••••••••xxxx`、一键复制密钥、安全存储说明以及强化连通性测试体验）；
  - [[log.md]]。
- 摘要：按计划完整交付 6 大优化项。全局构建验证通过（`exit code 0`），代码架构模块度、系统容错性与交互体验大幅跃升。
- 待办：无。

## [2026-09-29] refactor | PromptStudio AI 第二轮架构细化与体验加固落地

- 输入：用户反馈《PromptStudio AI 项目改进意见（细化版）》第二轮建议：
  - 中优先级：模特数据持久化、Store 规模控制切片化、ErrorBoundary 功能加强；
  - 低优先级：类型定义收紧与 JSDoc 标注、SettingsModal 补充显式「测试连接」功能。
- 变更：
  - `H:\Project\aiProject\src\lib\model-storage.ts`（规范模特持久化仓储为全站单一事实来源，支持 LocalStorage CRUD、激活模特状态持久化与出厂重置）；
  - `H:\Project\aiProject\src\lib\character-dna.ts`（重命名默认硬编码模特为 `SEED_DEFAULT_MODEL_ZHAO` 与 `SEED_AVAILABLE_MODELS`，明确标记为出厂种子数据，保留向后兼容别名）；
  - `H:\Project\aiProject\src\store\slices\`（新建：按领域拆分为 `tabSlice.ts`、`modelSlice.ts`、`studioSlice.ts`、`auditSlice.ts` 与 `uiSlice.ts`，彻底防止单 Store 膨胀）；
  - `H:\Project\aiProject\src\store\useAppStore.ts`（重构：通过 Zustand `StateCreator` 模式组合各子切片，同时导出轻量化领域专精选择器 Hooks 如 `useTabStore`、`useModelStore`、`useStudioStore` 等）；
  - `H:\Project\aiProject\src\components\ErrorBoundary.tsx`（强化：新增软状态重置恢复按钮 `handleSoftReset`、智能错误分类 `deduceErrorCategory`、开发环境折叠诊断堆栈 `<details>` 与安全硬刷新）；
  - `H:\Project\aiProject\src\types\index.ts`（收紧：新增独立 `StudioPreset` 穿搭与场景预设接口，替换匿名内联类型；新增并严格标注 `StudioOptions` 的 12 项字段与 JSDoc 用途说明）；
  - `H:\Project\aiProject\src\lib\skills-engine.ts`（重构：从 `@/types` 导入并重导出 `StudioOptions`，规范模块化类型出口）；
  - `H:\Project\aiProject\src\lib\ai-client.ts`（升级：`CallAIOptions` 增加 `overrideConfig` 接口，支持临时测试连接时免写入 LocalStorage 的无副作用轻量握手）；
  - `H:\Project\aiProject\src\components\SettingsModal.tsx`（强化：API Key 区域增加快速测试按键与环境变量 Key 状态提示，设置页主体新增醒目的「API 连通性测试与诊断」交互卡片，支持毫秒延迟测速与详细报错排查指引）；
  - [[log.md]]。
- 摘要：圆满完成第二轮 5 项细化改进。通过 Zustand Slice 模式实现了清晰的状态分治，巩固了模特数据单一事实来源，完善了错误边界的软恢复与诊断展开，收紧了核心提示词接口类型规范，并在设置中提供了直观、无副作用的 API Key 连通性测试与毫秒级延迟反馈。生产环境构建通过，服务在 3001 端口稳定就绪。
- 待办：无。






## [2026-10-08] ingest | 建立0915、0917、0926、0927实战案例检索与复用导航

- 输入：提交 [102f70e](https://github.com/lxy7747-hash/shengtuzhishiku/commit/102f70e68e4668eee80fb4075a1539aaa8cc2bbb) 中 `提示词/06-案例复盘/0915、0917、0926、0927`；11份文本与11张配图。
- 变更：[[wiki/sources/2026-09-30 - 0915运动穿搭案例.md]]、[[wiki/sources/2026-09-30 - 0917居家镜自拍动作案例.md]]、[[wiki/sources/2026-09-26 - 实战素材与动作链 (0926).md]]、[[wiki/sources/2026-09-30 - 0927俯拍与试衣镜自拍案例.md]]、[[wiki/maps/生图实战案例目录.md]]、[[wiki/concepts/实战案例提示词片段库.md]]、[[wiki/sources/2026-09-21 - 实战生图素材与手机双摄规范.md]]、[[wiki/concepts/手机镜自拍与遮挡技巧.md]]、[[wiki/maps/AI 生图知识库地图.md]]、[[wiki/concepts/AI 生图 Taxonomy.md]]、[[index.md]]、[[log.md]]。
- 摘要：按摄影视角、人物动作、遮挡方式、服装材质、适用场景登记11条图片案例，提炼11段候选复用片段，补齐全部原始文件回链及index与主地图入口；原始资料保持不变。
- 证据更新：保留历史“突破”“实现了”“卓越表现”表述并显式限定其未附验证证据；当前已知效果仅指配图可见元素，生成复现与用户验收仍待验证。0926的白色手机目标与浅蓝色配图有差异；0927的白色丝袜效果、俯拍图EXIF方向待核验，3.png无同名提示词，未自动沿用2.txt。
- 验证：已逐份读取文本、查看全部配图；核对原始文件覆盖、内部页面与章节链接、新页frontmatter及导航，确认只变更wiki、index与追加log。
- 待办：补实际底图及输入输出角色、工具版本与参数、未配对图片提示词、逐项复现与验收记录；不从文件名推断生成工具、迭代顺序或有效性。
