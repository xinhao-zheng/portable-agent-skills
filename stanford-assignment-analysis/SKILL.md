---
name: stanford-assignment-analysis
description: >-
  Apply the Stanford-derived post-assignment method to turn completed coursework
  into a forum-ready analysis: close graded-unit coverage, inspect the student's
  real code/notebook/written/report artifacts, reorganize them into a knowledge
  chain, show derivation or evidence paths, map artifacts to mechanisms, and earn
  cross-task insights. Never invent experience, reveal private tests, or answer
  personal prompts for the student. The original Stanford source workflow is the
  reference profile; it activates only on an artifact-pattern match. Every
  nonmatching repository — including another Stanford course — reuses the
  evidence-to-explanation chain through local artifact discovery. 采用源自 Stanford
  的作业后分析方法，把已完成课程作业转为可发布分析：闭合计分单元覆盖，检查学生真实的
  代码/Notebook/书面稿/报告工件，重组为知识链，展示推导或证据路径，把工件映射到机制，并
  赢得跨题洞见。不虚构经历、不泄露私有测试、不代答个人题。原 Stanford 源工作流只在工件
  模式匹配时启用参照 profile；任何不匹配的仓库——包括另一门 Stanford 课程——均通过本地
  工件发现复用证据—解释链。Use when 作业分析/复盘,
  公式与代码解释, 研究纪要,
  课程详解帖, or completed-coursework tutorial posts.
---

# Stanford Assignment Analysis · Stanford 作业分析

## What this is | 这是什么

In one line: **a post-assignment reconstruction that turns finished answers into
an irreversible learning chain — motivation before derivation, mechanism before
implementation, evidence before reflection.**
一句话：**一种做完作业后的重建：把完成的答案写成不可调换的学习链——推导之前先有
动机，实现之前先有机制，反思之前先有证据。**

Its opposite is an answer dump wearing explanatory headings: equations jump to
results, implementation is pasted whole, and “I learned” appears without an
observable change in method. That preserves the submission. It loses the learning.
它的反面是披着解释标题的答案堆：公式跳到结果，实现整段粘贴，“我学到”却没有可观察的
方法变化。它保存了提交。学习丢了。

---

## Style fingerprint | 风格指纹（八项，与 logic.md 八步一一对应）

1. **Completion gate** — no definitive analysis until authoritative prompts and
   the relevant completed submission artifacts are inspectable.
   **完成闸门**——权威题面与相关已完成提交工件不可检查时，不写确定性分析。
2. **Closed coverage** — map every graded unit; mark open-ended personal prompts
   and hidden tests as bounded exclusions, not silent omissions.
   **覆盖闭合**——映射每个计分单元；开放个人题与 hidden test 作为显式边界，不静默遗漏。
3. **Knowledge order over question order** — derive a theme chain whose sections
   cannot swap without breaking the explanation.
   **知识顺序高于题号顺序**——推出不可随意调换的主题链。
4. **Four anchors per section** — prerequisite and purpose open the section;
   earned takeaway and next use close it. Evidence sits between them.
   **每节四锚**——前置知识与学习目的开篇；经证据赢得的小结与下一用途收尾。证据居中。
5. **Derivation without jumps** — motivation → premises → transformation →
   result → intuition → failure mode.
   **推导不跳步**——动机 → 前提 → 变换 → 结果 → 直觉 → 易错点。
6. **Implementation as mechanism** — strategy before excerpt; each key element
   maps to the formula, invariant, state transition, or rubric requirement it realizes.
   **实现即机制**——片段前先讲策略；关键元素映射到其实现的公式、不变量、状态转移或 rubric 要求。
7. **Earned cross-insight** — connect multiple tasks only when a shared structure
   survives comparison; reflect on method without inventing biography.
   **赢得跨题洞见**——只有共同结构经比较成立才连接多题；反思方法，但不虚构个人经历。
8. **Portable release gate** — ordinary Markdown, repository-appropriate math,
   nearby source addresses, no hidden-test leakage, and a full beginner audit.
   **可移植发布闸门**——普通 Markdown、适合仓库的数学表达、近端来源地址、无 hidden-test
   泄露，并通过完整小白审计。

---

## How to use | 怎么用

**Writing fresh** — read [logic.md](logic.md) to discover the submission form,
close prerequisites, and build the knowledge chain; then write per
[style.md](style.md): package docs in the austere voice, the post in the embedded
analytical-teaching voice.
**新写分析**——先读 [logic.md](logic.md) 发现提交形式、闭合前置并建立知识链，再按
[style.md](style.md) 落笔：包内文档用冷峻体；帖子使用其中内嵌的分析教学体。

**Revising an existing post** — repair factual coverage and evidence-to-analysis
mapping first, then clean narrative, headings, mathematical form, and section
anchors. Do not preserve a stylish sentence that the artifacts cannot support.
**修订旧帖**——先修事实覆盖与证据—分析映射，再清理叙事、标题、数学形式与四锚。工件
不支持的漂亮句子，不保留。

| File | Role |
|------|------|
| [logic.md](logic.md) | Prerequisites, analysis chain, safety gates · 前置、分析链、安全闸门 |
| [style.md](style.md) | Skill-doc voice + analysis-post voice · Skill 文档体 + 分析帖文体 |

---

## One contrast | 一个最小对照

> Before (answer dump) — *The gradient is `Aᵀ(Aw-b)`. The code returns it.*
> 原做法（答案堆）：梯度是 `Aᵀ(Aw-b)`。代码返回它。

> After (this skill) — *Name the need first: optimization requires the direction
> in which residual error grows. Expand the quadratic, derive each term, show why
> `Aᵀ` returns sample-space error to parameter space, then point to the exact
> implementation element. Formula and implementation become one mechanism.*
> 改后（本 skill）：先点明需要——优化须知道残差增长的方向；再展开二次式，逐项推导，
> 解释 `Aᵀ` 如何把样本空间误差带回参数空间，最后指向实际实现元素。公式与实现成为同一机制。

The difference is entirely: an answer states what passed; an analysis preserves
why it had to be produced that way.
差别全在：答案陈述什么通过了；分析保存为何必须这样完成。
