---
name: stanford-lecture-notes
description: >-
  Apply the Stanford-derived note method to structured course materials and
  transcripts, producing traceable Chinese-first lesson notes or unit syntheses:
  primary materials fix the skeleton; instructor speech adds explanation; quotes
  stay verbatim and become bilingual when translation is needed. The original
  Stanford source workflow is the reference profile; it activates only on an
  artifact-pattern match. Every
  nonmatching repository — including another Stanford course — reuses the
  protocol through local source discovery. 采用源自 Stanford 的笔记方法处理结构化课程材料与
  转录稿，生成可追溯、中文优先的单课笔记或单元综合：一手材料钉住骨架，教师口语补解释；
  引文保持逐字，需翻译时双语并列。原 Stanford 源工作流只在工件模式匹配时启用参照
  profile；任何不匹配的仓库——包括另一门 Stanford 课程——均通过本地来源发现复用该协议。
  Use when 生成课程笔记, 总结
  lecture/week/unit/module/chapter, 制作 Summary/Overview, or 提炼讲义与转录稿.
---

# Stanford Lecture Notes · Stanford 课程笔记

## What this is | 这是什么

In one line: **a source-closed method for turning structured instruction and
spoken explanation into one review artifact — the primary material fixes the
skeleton, instructor speech adds judgment, and no sentence loses its address.**
一句话：**一种先闭合来源、再生成复习工件的方法——主讲义钉住骨架，教师口语补判断；
成稿中没有一句失去地址。**

Its opposite is compression by impression: skim the slides, quote from memory,
then arrange familiar terms under headings. That yields a plausible note whose
strongest sentences cannot be re-checked. Plausibility is not provenance.
它的反面是凭印象压缩：略读幻灯片、凭记忆引语，再把熟悉术语排进标题。所得笔记或许
顺眼，最承重的句子却无法复核。像真的，不等于可追溯。

---

## Style fingerprint | 风格指纹（八项，与 logic.md 八步一一对应）

1. **Closed course scope** — resolve the repository's own unit vocabulary and
   the requested granularity before reading.
   **课程范围闭合**——阅读前解析仓库自身的单元词汇与请求粒度。
2. **Mode gate** — a lesson note reads primary materials; a unit synthesis reads
   completed child notes. The two modes do not blur.
   **模式闸门**——单课笔记读一手材料；高层综合读已完成子笔记。两种模式不混写。
3. **Skeleton before voice** — read structured sources before transcripts; the
   conceptual order exists before speech adds intuition.
   **先骨架，后声音**——先读结构化来源，再读转录稿；概念顺序先成立，口语再补直觉。
4. **Source-role join** — each major concept binds its primary mechanism to an
   instructor explanation, example, caution, or repeated emphasis when available.
   **来源角色合流**——每个主要概念把一手机制与可用的教师解释、例子、警告或重复强调绑定。
5. **Mode-specific irreversible structure** — lesson notes advance from overview
   to mechanism; parent syntheses advance from child-unit distillation to a
   cross-unit insight. Neither may collapse into headings.
   **模式专属的不可调换结构**——单课笔记从概览推进到机制；父级综合从子单元浓缩推进到
   跨单元洞见。二者都不得塌成标题清单。
6. **Verbatim integrity** — quotations stay single-source and exact; numbers,
   names, causal relations, and uncertainty retain their original force.
   **逐字完整性**——引文保持单源且准确；数字、人名、因果与不确定性保留原始力度。
7. **Repository convention as anchor** — discover live paths, naming, metadata,
   tables, quotation form, and footer; never impose one example repository.
   **仓库约定作锚**——发现真实路径、命名、元数据、表格、引文与尾注；不强加示例仓库布局。
8. **Audit before release** — coverage, quotation search, factual checks, and
   cross-unit coherence pass before completion.
   **发布前审计**——覆盖、引文检索、事实核对与跨单元连贯性全部通过，才算完成。

---

## How to use | 怎么用

**Writing a lesson note** — read [logic.md](logic.md) to classify sources and
close the source set, then write per [style.md](style.md): skill docs in the
austere voice; the note in the embedded Chinese-first review voice.
**生成单课笔记**——先读 [logic.md](logic.md) 分类来源并闭合来源集，再按
[style.md](style.md) 落笔：Skill 文档用冷峻体；笔记使用其中内嵌的中文复习体。

**Writing a unit synthesis** — confirm every child note exists, read those notes
as the closed corpus, and derive the cross-unit chain. Do not silently replace a
missing child with raw sources.
**生成高层综合**——先确认全部子笔记存在，以这些笔记构成闭合语料，再推出跨单元链。
不得用原始来源悄悄替代缺失子笔记。

| File | Role |
|------|------|
| [logic.md](logic.md) | Scope, source roles, composition gates · 范围、来源角色、生成闸门 |
| [style.md](style.md) | Skill-doc voice + note-output voice · Skill 文档体 + 笔记输出体 |

---

## One contrast | 一个最小对照

> Before (topic list) — *Gradient descent: definition, formula, applications.*
> 原做法（术语清单）：梯度下降：定义、公式、应用。

> After (this skill) — *The primary lecture fixes the update rule; the transcript
> explains why the learning rate is the control surface; the note joins them,
> quotes the caution exactly, and shows which assessment reuses it.*
> 改后（本 skill）：主讲义钉住更新规则；转录稿解释为何学习率才是控制面；笔记把两者
> 合流，逐字保留警告，并指出哪项考核会复用它。

The difference is entirely: a list remembers topics; a traceable note preserves
the reasoning that made the topics matter.
差别全在：清单记住题目；可追溯笔记保住题目为何成立的推理。
