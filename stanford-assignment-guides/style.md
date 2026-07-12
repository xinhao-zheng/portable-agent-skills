# Language: Skill Doc + Guide Outputs · 语言风格：Skill 文档 + Guide 输出

Use one austere documentation voice and three deliberately different output
registers. Their facts are shared; their compression differs.
使用一种冷峻文档体与三种刻意区分的输出声线。事实共用；压缩程度不同。

---

## Voice A — Skill documentation | Voice A——Skill 文档

The package voice is fixed: zero filler; load-bearing verbs; em-dash
qualification; a short sentence to land the stress; honesty over rhetoric.
包内声音固定：零套话；承重动词；破折号用于限定；短句落重音；诚实压过修辞。

1. **Use load-bearing verbs:** resolve, recurse, bind, project, reconcile. |
   **使用承重动词：** 解析、递归、绑定、投影、对账。
2. **Replace praise with consequence.** Not “PDF checking is important”, but
   “without the PDF pass, visible order remains unverified”. |
   **用后果替代赞美。** 不写“核对 PDF 很重要”，写“无 PDF 核对则可见顺序未经验证”。
3. **Use the em dash for a real boundary.** `Complete, not solved — every
   requirement appears; no answer does.` | **破折号只承载真实边界。** “完整，但不解题——
   每条要求都出现；答案一条不出现。”

---

## Voice B1 — Bilingual problem document | Voice B1——双语题面

1. **Source language is evidence.** Preserve it verbatim; do not modernize
   punctuation, simplify instructions, or repair meaning silently.
   **源语言即证据。** 逐字保留；不现代化标点、不简化要求、不静默修义。
2. **Translate semantic blocks when needed.** For a non-Chinese source, present
   the full source-language block, then one Chinese blockquote. For a Chinese
   source, preserve the block once. Do not alternate sentence by sentence unless
   the source itself is a list of independent items.
   **需要时按语义块翻译。** 非中文来源先完整呈现源语言块，再给一个中文 blockquote；中文
   来源只保留一次。除非来源本身是独立列表项，不逐句交替。
3. **Chinese is precise, not chatty.** Keep source-language professional terms
   where useful; preserve formulae, code, commands, paths, names, and references.
   **中文精确，不闲聊。** 必要专业术语保留源语言；公式、代码、命令、路径、专名与引用不改。
4. **Hierarchy follows the source.** Do not invent heading levels absent from
   the live artifact convention.
   **层级服从来源。** 不发明当前工件约定中不存在的标题层级。

---

## Voice B2 — Assignment Overview | Voice B2——知识概述

5. **Open on capability.** State what the assignment makes the student able to
   model, derive, implement, or evaluate — not “covers many important topics”.
   **以能力开篇。** 说明作业使学生能够建模、推导、实现或评估什么——不用“涵盖很多重要知识”。
6. **Define, then map.** A concept table gives one precise definition; a second
   table maps every subproblem to its role. Tables expose structure, not decoration.
   **先定义，再映射。** 概念表给精准定义；题目表把每小题映射到角色。表格暴露结构，不作装饰。
7. **Course relation is causal.** Show which earlier unit supplies the
   prerequisite and what later work reuses it. Do not merely list unit labels.
   **课程关系须有因果。** 说明哪个前序单元提供前置、后续工作如何复用；不只列单元标签。

---

## Voice B3 — Chinese action guide | Voice B3——中文行动指南

8. **Orient the parent problem.** Before its first subproblem card, use 2–4
   sentences to state the shared setting, capability target, and division of work.
   **先定位大题。** 第一张小题卡片前，用二至四句说明共同情境、目标能力与各小题分工。
9. **Use a fixed subproblem card.** `来源 ID / 分值 / 类型 → 题意 → 你需要做什么 →
   提交物/期望输出 → 限制/注意 → 一句话提示`. Omit only a truly empty constraint field.
   **小题卡片固定。** `来源 ID / 分值 / 类型 → 题意 → 你需要做什么 → 提交物/期望输出 →
   限制/注意 → 一句话提示`。只有确无约束时才省该栏。
10. **Compress background, never obligations.** Prompt Templates, Examples, and
   References may be described by function, but every requirement affecting the
   answer remains explicit.
   **压背景，不压义务。** Prompt Template、Example、References 可按用途压缩；凡影响作答
   的要求必须显式保留。
11. **Warnings protect boundaries.** Good: “return shape is `(batch, classes)`”.
    Bad: “compute it by applying softmax, then…”.
    **提醒守边界。** 可写“返回形状为 `(batch, classes)`”；不可写“先做 softmax，然后……”。

---

## Shared artifact form | 共用工件形式

- **Stanford reference profile:** preserve the matched source workflow's metadata,
  ToC, heading, separator, point-summary, and footer conventions; use A1 as the
  format anchor when live. | **Stanford 参照 profile：** 保留所匹配源工作流的元数据、目录、
  标题、分隔线、分值汇总与 footer 约定；A1 工件存在时以其作格式锚。
- Use metadata conventions already live in the repository; include course,
  deadline, scoring, sources, and relations where the artifact requires them. |
  沿用仓库现存元数据约定；按工件需要写课程、截止日期、计分、来源与关联。
- Use Markdown tables for mappings and point summaries; follow them with a plain
  reconciliation sentence. | 映射与分值汇总用 Markdown 表格；表后接一句白话对账结论。
- End with a factual generated-from footer and the real update date. |
  以事实性来源 footer 与真实更新日期收尾。
- Never mention a skill or internal production rule in the deliverable. |
  交付物中不得点名 skill 或内部生产规则。

---

## One-pass clean | 一键清洗流程

1. Compare all headings and subproblem IDs with the closed source model. |
   以闭合来源模型核对标题与小题 ID。
2. Search for any changed source-language sentence; restore it. |
   搜索被改写的源语言原句并恢复。
3. Recompute points by the grading schema's canonical unit ID; use `question_id`
   only when that is the live key. Compare totals across all artifacts. |
   按计分 schema 的规范单元 ID 重算分值；只有真实键为 `question_id` 时才使用它。比较总分并
   跨工件对账。
4. Remove background compression that accidentally deleted an obligation. |
   修复因压缩背景而误删的作答义务。
5. Remove every agent-generated answer, pseudocode step, derivation, and
   implementation hint. Preserve source-authored examples required by the
   bilingual source view. | 删除所有新增答案、伪代码步骤、推导与实现提示；保留双语来源
   视图必须呈现的来源自带示例。
6. Read the CN Guide alone: each subproblem must reveal do, submit, and boundary. |
   单读 CN Guide：每小题须显出做什么、交什么、边界是什么。
