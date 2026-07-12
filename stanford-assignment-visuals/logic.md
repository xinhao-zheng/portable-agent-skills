# Visual Skeleton · 配图推进骨架

The advance order for course instructional visuals. Generation begins only
after the storyboard can state the transformation in one sentence.
本文件给出课程教学配图的推进顺序。只有 storyboard 能用一句话说明变化时，才开始生成。

---

## Stanford reference profile + portable fallback | Stanford 参照 profile＋可迁移回退

Activate the **Stanford reference profile** only when both conditions hold:
Stanford provenance is verified from repository metadata or the user explicitly
requests this profile; and the live repository matches the source workflow's
relevant analysis-plus-companion artifact pattern. Identity alone is insufficient.
Structure alone is insufficient. A completed visual is an optional style anchor,
never an activation prerequisite.
只有两个条件同时成立，才启用 **Stanford 参照 profile**：仓库元数据已验证 Stanford 来源，
或用户明确指定该 profile；并且真实仓库匹配源工作流相应的“Analysis＋配套工件”模式。只有
身份不够。只有结构也不够。已完成配图只是可选风格锚，绝不是首次激活的前置。

Resolve the work item before display or naming:
展示与命名前，先解析工作项：

| Work type · 工作类型 | Required source-workflow pair · 源工作流必需组合 | Work ID · 工作项 ID | Work label · 展示标签 |
|---|---|---|---|
| assignment · 作业 | Assignment Analysis + Assignment Overview | `A{N}` | `Assignment {N}` |
| unit · 课程单元 | Unit/Module Analysis + matching Unit/Module Summary or Overview · Unit/Module Analysis＋匹配的 Unit/Module Summary 或 Overview | `M{N}` or verified local ID · `M{N}` 或经验证本地 ID | verified local vocabulary + number · 经验证本地单元词汇＋编号 |

Derive course code, course title, work type, ID, and local unit vocabulary from
metadata. With a verified code, display `Stanford <course-code> <work-label>`;
without one, display `<verified Stanford course title> · <work-label>`. Labels are
Chinese-first, with English retained only for necessary terms.
从元数据推导课程代码、课程名、工作类型、ID 与本地单元词汇。有经验证代码时展示
`Stanford <course-code> <work-label>`；无代码时展示
`<经验证 Stanford 课程全名> · <work-label>`。标签中文为主，只保留必要英文术语。

When the profile is active, apply the inheritance priority in step 5. Only when
neither a coherent live target-course set nor a completed reference anchor exists,
apply the reference defaults: horizontal 16:9; warm off-white `#F5F4F0`; dark navy
`#1e293b`; royal blue `#1d4ed8`; light gray `#e2e8f0`; at most one additional
shared semantic color. Save under the matching live `_3_...` subfolder using the
detected source-workflow pattern and these defined tokens:
profile 启用时执行第 5 步的继承优先级。只有既无目标课程一致的真实视觉组，也无已完成参照
锚点时，才采用参照默认：横版 16:9；暖灰白 `#F5F4F0`；深蓝 `#1e293b`；皇家蓝
`#1d4ed8`；浅灰 `#e2e8f0`；至多再加一种全组共用语义色。保存到匹配的真实 `_3_...`
子目录，沿用检测到的源工作流模式与下列 token：

| Token · 记号 | Meaning · 含义 |
|---|---|
| `<work-id>` | verified `A{N}`, `M{N}`, or local equivalent · 经验证的 `A{N}`、`M{N}` 或本地等价 ID |
| `M{NN}` | `M` + two-digit teaching-section sequence · `M`＋两位教学章节序号 |
| `<slug>` | stable lowercase section slug · 稳定小写章节 slug |
| `<course-key>` | verified course code; otherwise stable course slug · 经验证课程代码；否则稳定课程 slug |

`<work-id>_overview_full_<course-key>_visual.png`
`<work-id>_M{NN}_<slug>_<course-key>_visual.png`

Every repository outside this two-part match — including another Stanford course
with a different workflow — preserves the same content, storyboard, generation,
inspection, and repair gates. Inherit its identity and visual system; do not
export Stanford branding or legacy filenames.
任何不满足这两个条件的仓库——包括工作流不同的另一门 Stanford 课程——都保留同一内容、
分镜、生成、检查与修复闸门；继承自身身份与视觉系统，不外送 Stanford 品牌或旧命名。

---

## Modes | 模式

| Mode · 模式 | Asset · 工件 | Use · 用途 |
|---|---|---|
| Overview · 总览 | One full learning map · 一张全景学习图 | Cover, opening, whole chain · 封面、开篇、完整链条 |
| Section set · 分章组 | One image per teaching section · 每教学章节一图 | Section anchors, mechanism explanation · 正文锚点、机制解释 |
| Both · 两者 | Overview plus section set · 总览加分章组 | Default for “整套/按章节全做” · “整套/按章节全做”的默认 |

If the user explicitly requests one mode, obey it. If the user asks for a full
set or clearly requests work-item visuals without specifying, default to Both.
用户明确指定则服从；用户要求整套，或明确要某个工作项配图但未指定时，默认两者都做。

---

## Order of advance | 推进顺序（默认骨架）

1. **Fix scope and ledger** — resolve course identity, work type (`assignment` or
   `unit`), work ID/title, live content artifacts, output directory, requested mode, and existing visual
   convention. For a section set, list real teaching sections in the ledger below.
   The `Status` set is fixed: `planned`, `generated`, `passed`, `repair`, `blocked`.
   Preface, Knowledge Map, symbol lookup, Cross-Task Insights, Methodological Gains,
   and appendix do not become separate images unless they carry an independent
   mechanism.
   **固定范围与台账**——解析课程身份、工作类型（`assignment` 或 `unit`）、工作项 ID/标题、
   真实内容工件、输出目录、请求模式与
   既有视觉约定。分章组在下表列出真实教学章节。`Status` 固定为：`planned`、`generated`、
   `passed`、`repair`、`blocked`。前言、知识地图、符号速查、跨题洞见、方法论收获与附录
   默认不单独成图，除非它们承载独立机制。

   | Asset ID · 工件 ID | Mode · 模式 | Source section · 来源章节 | Main object · 主对象 | Visible transformation · 可见变化 | Filename · 文件名 | Status · 状态 |
   |---|---|---|---|---|---|---|
   | stable local ID · 稳定本地 ID | overview/section · 总览/分章 | exact heading or whole chain · 精确标题或完整链 | one object/scene · 一个对象/场景 | before → action → after · 之前→动作→之后 | deterministic local name · 确定性本地名 | fixed set only · 仅用固定词面 |

2. **Close the content map** — under the Stanford reference profile, require the
   source pair defined for the resolved work type: Assignment Analysis + Assignment
   Overview for an assignment; Unit/Module Analysis + its matching Unit/Module
   Summary or Overview for a course unit. Read Analysis first: it controls the
   organizing question, chapter names, order, boundaries, and learning chain. Read
   the companion second: it verifies concepts, course relations, and work-item
   position. Course notes and completed submissions are secondary; they may verify
   terminology or implementation, not redefine section boundaries. A missing
   required artifact blocks generation; a conflict remains named.
   **闭合内容图**——Stanford 参照 profile 下，须按已解析工作类型闭合源组合：作业要求
   Assignment Analysis＋Assignment Overview；课程单元要求 Unit/Module Analysis＋匹配的
   Unit/Module Summary 或 Overview。先读 Analysis：它控制组织问题、章名、顺序、边界与学习
   链；再读配套工件：它核对概念、课程关系与工作项定位。课程笔记与完成提交是次级来源，只可
   核验术语或实现，不得重定章节边界。缺必需工件则阻断生成；冲突保持具名。

   Outside that profile, prefer an equivalent validated analysis + companion chain.
   If none exists, build an explicit map from the authoritative assignment/unit
   source, course notes, and rubric before drawing. In every case, read the title,
   organizing question, knowledge chain, and all teaching sections. Private grader
   content, hidden tests, solution details, and large code excerpts may verify a
   boundary internally; they never enter the publishable content map.
   profile 外优先使用等价的已验证 Analysis＋配套工件链。若不存在，则从权威作业/单元来源、
   课程笔记与 rubric 先建立显式内容图，再绘制。任何情况下都须读取标题、组织问题、知识链与
   全部教学章节。私有 grader 内容、hidden test、答案细节与大段代码只可在内部核验边界，
   绝不进入可发布内容图。

3. **Assign one main object** — for each asset, choose a concrete object or scene
   that can carry the concept: tensor block, masked grid, loss surface, search
   frontier, state map, game tree, evidence filter, count machine, feedback loop,
   laboratory setup, historical timeline, argument scale, or domain equivalent.
   Write: “The image shows [object] changing from [before] to [after].” If the
   sentence is abstract or lists headings, redesign.
   **分配一个主对象**——每个工件选择可承载概念的具象对象或场景：张量块、遮罩网格、损失
   曲面、搜索前沿、状态地图、博弈树、证据滤镜、计数机器、反馈回路、实验装置、历史时间线、
   论证天平或领域等价物。写：“图展示[对象]从[之前]变成[之后]。”若仍抽象或只是标题列表，重做。

4. **Write the causal storyboard** — answer who changes, why, and what it
   becomes. Prefer `Before → Mechanism → After` or `Problem → Intervention →
   Result`. Give each essential arrow an action verb. Prepare one plain teaching
   sentence and 3–5 short labels mapped directly to visible objects. Formulae and
   quotations remain local annotations, never the main field.
   **写因果分镜**——回答谁在变、为何变、变成什么。优先 `Before → Mechanism → After`
   或 `Problem → Intervention → Result`。必要箭头带动作词。准备一句教学白话与三至五个
   直接映射可见对象的短标签。公式与引文只作局部注释，不占主场。

5. **Inherit or declare the visual system** — use one priority order. First,
   inherit a coherent live visual set from the target course. If none exists and
   the Stanford reference profile matches, inherit its completed reference anchor;
   if no such anchor exists, use the declared reference defaults. Outside that
   profile, declare once: wide instructional canvas (16:9 by default), quiet light
   background, dark text, one primary accent, at most one auxiliary semantic color,
   title bar + central object + aligned takeaways. In every branch, derive display
   name, logo/brand constraints, and language from source metadata or user
   instruction. Never mix branches.
   **继承或声明视觉系统**——只用一条优先级。先继承目标课程真实且一致的既有视觉组；若无，
   且 Stanford 参照 profile 匹配，则继承其已完成参照锚；仍无锚点，才采用已声明的参照默认。
   profile 外一次声明：默认宽幅教学画布（16:9）、安静浅底、深色文字、一个主强调色、至多
   一个语义辅助色、顶栏标题＋中央对象＋对应要点。所有分支的展示名、Logo/品牌限制与语言
   均来自来源元数据或用户要求。分支不得混用。

6. **Generate the asset** — for raster instructional illustrations, default to
   AI image generation with an explicit concrete object, causal change, readable
   target language, and prohibitions against formula walls, flowchart walls, and
   marketing posters. Do not default to Python/PIL, HTML/CSS, slides, or diagrams.
   Programmatic composition is allowed when the user requests editable/vector
   output, the repository convention requires it, or repeated text failure needs
   a clean overlay; preserve the instructional main visual. Exclude private or
   hidden tests, answer details, large code excerpts, emoji, memes, and internal
   production language from prompts and images.
   **生成工件**——位图教学插图默认 AI 生图，提示词明确具象对象、因果变化、目标语言可读，
   并禁止公式墙、流程图墙与营销海报。不得默认使用 Python/PIL、HTML/CSS、幻灯片或图表。
   用户要求可编辑/矢量、仓库约定需要，或文字多次失败需清晰叠字时，可程序化合成；仍须保留
   教学主视觉。提示词与图片均排除私有或 hidden test、答案细节、大段代码、emoji、网络梗
   与内部生产语言。

7. **Inspect the rendered asset** — view every actual image at normal and readable
   scale. Check target-language text, overlap, crop, contrast, course/work-item
   identity, section title, stage order, main object, causal transformation,
   factual fidelity, whether each takeaway points to something visible, and whether
   any private-test, answer, code-dump, or internal-rule content leaked through.
   Prompt intent is not evidence of output quality.
   **检查实际渲染工件**——以正常与可读比例查看每张图。检查目标语言、遮挡、裁切、对比度、
   课程/工作项身份、章名、阶段顺序、主对象、因果变化、事实忠实、每条要点是否指向可见对象，
   以及是否泄露私有测试、答案、代码堆或内部规则。提示词意图不是输出质量证据。

8. **Repair, save, reconcile** — repair content/metaphor failure upstream;
   repair text first by reducing labels, shortening sentences, and regenerating.
   Overlay only when allowed. Follow the repository's filename and directory
   convention; if none exists, use stable course/work-item/section slugs.
   Verify count, names, geometry, visual consistency, and one-to-one coverage.
   Re-scan every asset for private tests, answers, and code dumps. Return the
   complete absolute save path for every released asset.
   **修复、保存、对账**——内容/隐喻失败回上游修；文字失败先减标签、缩短句、重生；允许时
   才叠字。沿用仓库文件名与目录约定；若无先例，使用稳定课程/工作项/章节 slug。核验数量、
   命名、几何、视觉一致性与一一覆盖；再次扫描私有测试、答案与代码堆。交付时返回每个发布
   工件的完整绝对保存路径。

---

## Failure taxonomy | 失败分类

| Failure · 失败 | Repair · 修复 |
|---|---|
| Content wrong · 内容错 | Re-read authoritative artifacts; rebuild map · 回读权威工件，重建内容图 |
| Identity wrong · 身份错 | Re-resolve course metadata; regenerate labels · 重解课程元数据并重生标签 |
| Metaphor empty · 隐喻空 | Replace boxes with one object undergoing change · 用一个变化对象替代方框 |
| Flowchart/formula wall · 流程/公式墙 | Reduce stages; restore concrete scene · 减阶段，恢复具象场景 |
| Text illegible · 文字糊 | Shorten/reduce/regenerate; overlay only as fallback · 减字重生；叠字仅兜底 |
| Private/answer leakage · 私有/答案泄露 | Remove from content map and prompt; regenerate; reinspect · 从内容图与提示词删除，重生并复检 |
| Set inconsistent · 整组不一 | Reapply shared identity, system, and hierarchy · 重施身份、系统与层级 |

---

## Self-check | 自检清单

- [ ] Are work type, work ID, and requested mode fixed, with a complete asset ledger? |
      是否已固定工作类型、工作项 ID 与请求模式，并列全资产台账？
- [ ] Do section assets map one-to-one to real teaching sections? |
      分章工件是否与真实教学章节一一对应？
- [ ] Does every image have one concrete main object and visible transformation? |
      每图是否有一个具象主对象与可见变化？
- [ ] Was identity derived from source/user, with the Stanford reference profile
      activated only on the two-part match? | 身份是否来自来源/用户，且 Stanford 参照 profile
      只在双条件匹配时启用？
- [ ] Is one visual system held across the set? |
      整组是否服从一个视觉系统？
- [ ] Was every actual asset inspected for text, crop, identity, facts, and causality? |
      每张实际工件是否检查文字、裁切、身份、事实与因果？
- [ ] Were failed assets repaired rather than delivered with caveats? |
      不合格工件是否已修复，而非带免责声明交付？
- [ ] Are private tests, answer details, code dumps, emoji, memes, and internal
      rules absent? | 私有测试、答案细节、代码堆、emoji、网络梗与内部规则是否均未出现？
- [ ] Do names, counts, and section coverage reconcile before release? |
      发布前命名、数量与章节覆盖是否对账？
- [ ] Was every released asset reported with its complete absolute save path? |
      是否返回了每个发布工件的完整绝对保存路径？
