# Language: Skill Doc + Visual Output · 语言风格：Skill 文档 + 视觉输出

Use the austere voice for instructions and a concrete instructional language for
the images. The visual deliverable is not prose, but it still makes an argument.
规则文档使用冷峻体；图片使用具象教学语言。视觉工件不是散文，但仍须完成论证。

---

## Voice A — Skill documentation | Voice A——Skill 文档

The package voice is fixed: zero filler; load-bearing verbs; em-dash
qualification; a short sentence to land the stress; honesty over rhetoric.
包内声音固定：零套话；承重动词；破折号用于限定；短句落重音；诚实压过修辞。

1. **Zero filler.** Cut “beautiful / premium / highly intuitive”. Name the
   object, transformation, gate, or failure.
   **零套话。** 删“漂亮／高级／非常直观”。写对象、变化、闸门或失败。
2. **Concrete verbs.** Filter, mask, expand, prune, update, reveal — not “show
   the relationship”. | **具象动词。** 过滤、遮罩、扩展、剪枝、更新、显露——不用“展示关系”。
3. **A contrast must be visible.** “Before/after” earns space only when an object
   actually changes. | **对照必须可见。** 只有对象真实变化时，Before/After 才值得占空间。
4. **Inspection over intent.** Describe the rendered defect, not the prompt's
   good intention. | **检查压过意图。** 描述渲染缺陷，不赞美提示词意图。

---

## Voice B — Visual language | Voice B——视觉语言

Never name a skill, prompt, or internal production rule in image text, metadata,
or filenames.
图片文字、元数据与文件名中不得点名 skill、提示词或内部生产规则。

### One image, one mechanism | 一图一机制

1. **The main object dominates.** At least half the information weight belongs
   to the object or scene that changes; labels and cards support it.
   **主对象占主导。** 至少一半信息重量属于发生变化的对象或场景；标签与卡片只作支撑。
2. **Use spatial causality.** Left-to-right or top-to-bottom change must match the
   teaching sequence. Do not use decorative arrows.
   **用空间承载因果。** 左→右或上→下须匹配教学顺序；不用装饰箭头。
3. **Label actions, not categories.** “剪掉高代价分支” beats a bare “pruning”.
   Put the technical term beside the plain action, not instead of it.
   **标动作，不只标类别。** “剪掉高代价分支”优于只写“pruning”。术语放在白话动作旁，
   不替代白话。

### Teaching before decoration | 教学先于装饰

4. **One plain teaching sentence.** It states what problem the mechanism solves.
   Keep it short enough to render at a large size.
   **一句教学白话。** 说明机制解决什么问题；短到可以大字号清晰呈现。
5. **Three to five takeaways by default.** Each maps to a visible feature. Adapt
   the count only when the repository's visual convention clearly differs.
   **默认三至五条要点。** 每条映射可见部位。只有仓库视觉约定明显不同才调整数量。
6. **Formulae and quotations are subordinate.** Use a symbol, short expression,
   or brief quote only where it labels an operation or evidence. No derivation in
   the image.
   **公式与引文从属。** 只在标记操作或证据处使用符号、短式或短引；图中不做推导。

### One inherited system | 一个继承的视觉系统

7. **Identity comes first.** Under the Stanford reference profile, derive the
   work label and use `Stanford <course-code> <work-label>` when a verified code
   exists; otherwise use `<verified Stanford course title> · <work-label>`.
   Outside the profile, course display name, work-item label, logo, and language
   come from source metadata, user instruction, or a verified existing asset;
   never export Stanford identity.
   **身份先行。** Stanford 参照 profile 先推导工作项标签；有经验证代码时使用
   `Stanford <course-code> <work-label>`，否则使用
   `<经验证 Stanford 课程全名> · <work-label>`。profile 外的课程展示名、工作项标签、
   Logo 与语言来自来源元数据、用户要求或已验证既有工件；不得外送 Stanford 身份。
8. **Inherit before inventing.** Use one priority: coherent live target-course
   set → matched Stanford reference anchor → declared defaults. Reuse aspect ratio,
   palette, type hierarchy, line weight, framing, and naming as a single system.
   **先继承，后发明。** 只用一条优先级：目标课程一致的真实视觉组 → 匹配的 Stanford 参照锚
   → 已声明默认。画幅、配色、字阶、线重、构图与命名须作为一个系统复用。
9. **One primary accent, at most one auxiliary semantic color.** The auxiliary
   color keeps one meaning across the set — risk, evidence, action, or result.
   **一个主强调色，至多一个语义辅助色。** 辅助色全组只承担一种含义——风险、证据、动作或结果。
10. **Hierarchy stays stable.** A useful default is title → central object →
    aligned takeaways. Avoid dense dashboards, sticker clusters, mascots,
    gratuitous gradients, and marketing polish unless the course brand requires them.
    **层级保持稳定。** 可用默认是标题 → 中央对象 → 对应要点。避免密集 dashboard、贴纸簇、
    吉祥物、无意义渐变与营销光泽；课程品牌明确要求时除外。

### Stanford reference defaults | Stanford 参照默认

When the Stanford reference profile is active and no stronger coherent visual
anchor exists, hold the original system: horizontal 16:9;
warm off-white `#F5F4F0`; dark navy `#1e293b`; royal blue `#1d4ed8`; light gray
`#e2e8f0`; at most one additional shared semantic color; title bar →
central main visual → 3–5 aligned takeaways.
Use Chinese-first labels and retain English only for necessary terms. These
defaults are profile-bound, not universal.
启用 Stanford 参照 profile 且无更强的一致视觉锚时，保持原系统：横版 16:9；暖灰白
`#F5F4F0`；深蓝 `#1e293b`；皇家蓝 `#1d4ed8`；浅灰 `#e2e8f0`；至多再加一种全组共用
语义色；顶栏标题 → 中央主视觉 → 三至五条对应要点。标签中文为主，只保留必要英文术语。
这些默认只绑定该 profile，不是通用规则。

Reference-profile filenames follow the asset ledger and the single naming
contract in [logic.md](logic.md) under “Stanford reference profile + portable
fallback.” Reuse those tokens verbatim; do not restate or fork the pattern here.
参照 profile 的文件名服从资产台账，以及 [logic.md](logic.md)“Stanford 参照 profile＋
可迁移回退”中的唯一命名契约。逐字复用其中 token；本文件不重述、也不分叉该模式。

### Text legibility | 文字可读性

11. **Short labels, large type.** Prefer verbs and noun phrases; split one long
    sentence into title + one plain line. Match the target language and script.
    Use no emoji, meme labels, or joke captions.
    **短标签，大字号。** 优先动词与名词短语；长句拆成标题＋一句白话。匹配目标语言与文字系统。
    不用 emoji、网络梗标签或玩笑式说明。
12. **Meaning survives text loss.** If all labels vanished, the object and
    transformation should still suggest the mechanism.
    **文字消失，意思仍在。** 即使标签全去，主对象与变化仍应暗示机制。
13. **No overlap or edge pressure.** Titles, subtitles, identity marks, section
    labels, and takeaways must clear one another and the crop.
    **不遮挡、不压边。** 标题、副标题、身份标、章名与要点须彼此避让并远离裁切边。

### Inspection language | 检查语言

14. **Pass/fail is concrete.** Pass: readable text, correct order, correct
    identity, visible object, causal action, section match, no private or answer
    leakage. Fail: name the exact malformed string, overlap, wrong label, missing
    stage, empty metaphor, hidden-test detail, answer, or code dump.
    **通过/失败须具体。** 通过：文字可读、顺序正确、身份正确、对象可见、动作有因果、章节
    匹配且无私有/答案泄露。失败：点名具体乱码、遮挡、错标签、缺阶段、空隐喻、hidden-test
    细节、答案或代码堆。
15. **Repair upstream first.** Wrong identity → metadata; wrong concept → content
    map; wrong metaphor → storyboard; clutter → composition; blurred text → reduce
    and regenerate.
    **先修上游。** 身份错回元数据；概念错回内容图；隐喻错回分镜；拥挤修构图；文字糊先减字重生。

---

## One-pass clean | 一键清洗流程

1. Reject and repair or regenerate any asset whose main field is headings, boxes,
   or formulae; never reduce ledger coverage to hide the failure. |
   主场由标题、方框或公式占据的工件须拒收并修复或重生；不得靠减少台账覆盖掩盖失败。
2. Rewrite every essential arrow as a concrete action. |
   把每根必要箭头改为具象动作。
3. Derive identity again from source/user; remove unsupported institutional assumptions. |
   从来源/用户重新推导身份；删除无依据的机构假设。
4. Reduce and enlarge labels until the target script is readable. |
   减少并放大标签，直到目标文字可读。
5. View actual assets at normal size; repair every overlap, crop, malformed
   string, and factual mismatch. | 以正常尺寸查看实际工件；修复全部遮挡、裁切、乱码与事实错配。
6. Compare the set side by side: identity, system, hierarchy, object scale, and
   label density must read as one author. | 并排比较整组：身份、系统、层级、对象尺度与标签密度
   须如一人之手。
7. Scan every asset for private tests, answers, code dumps, emoji, memes, and
   internal production language; report every released absolute save path. |
   扫描每张图中的私有测试、答案、代码堆、emoji、网络梗与内部生产语言；返回全部发布工件的
   绝对保存路径。
