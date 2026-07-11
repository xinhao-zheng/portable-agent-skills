# cursor-skills

A collection of Cursor Agent Skills, centered on writing. Each skill is a
self-contained folder defined by two things — its **argument logic** (how the
reasoning advances) and its **language style** (how each sentence reads); Cursor
loads it only when the skill's `description` matches the task. The repository is
flat: skills are added as sibling folders, not nested.
Cursor Agent Skills 集合，以写作为主。每个 skill 由两件事定义——**论证逻辑**
（论证如何推进）与**语言风格**（每句如何读起来）；仅当 skill 的 `description`
命中任务时，Cursor 才加载它。仓库保持扁平：skill 以同级文件夹新增，不嵌套。

---

## Skills | 技能


| Skill                                                         | Purpose                                                                          | Status       |
| ------------------------------------------------------------- | -------------------------------------------------------------------------------- | ------------ |
| [`austere-analytical-prose`](austere-analytical-prose/SKILL.md)       | An austere, analytical voice for papers and technical arguments · 论文与技术论证的冷峻思辨文体 | active · 已发布 |
| [`citation-integrity-audit`](citation-integrity-audit/SKILL.md)       | A re-checkable provenance ledger for a paper's citations · 论文引用的可复核溯源台账         | active · 已发布 |
| [`structured-plain-expression`](structured-plain-expression/SKILL.md) | A structured plain-language research post from one dataset/study — finding-first, evidence as a chain, sourced numbers · 把一份数据/研究写成结构化白话研究帖：结论先行、证据成链、数字带出处 | active · 已发布 |
| [`reframing-research-post`](reframing-research-post/SKILL.md) | An earned thesis from heterogeneous evidence — competing frames, independent triangulation, causal tests, hidden bills, and calibrated judgments · 从异质材料中赢得论题：框架竞争、独立三角验证、因果检验、隐藏账单与校准判断 | active · 已发布 |
| [`vd-report-ingest`](vd-report-ingest/SKILL.md) | Ingest new PDF/MD/image → bilingual transcript + summary · 新研报入库：提取、双语、摘要 | active · 已发布 |
| [`vd-synthesis-refresh`](vd-synthesis-refresh/SKILL.md) | Rebuild index, cross-report audit, or rolling window · 刷新索引、冲突审计或滚动窗口 | active · 已发布 |
| [`vd-essay-distill`](vd-essay-distill/SKILL.md) | Distill a chosen synthesis scope into a public-account essay · 综合研判转公众号文稿 | active · 已发布 |
| [`vd-latex-render`](vd-latex-render/SKILL.md) | Typeset a chosen document into brand LaTeX + PDF · 把文稿排成品牌 LaTeX + PDF | active · 已发布 |

Each of the eight skills is **self-contained**: its `SKILL.md`, `logic.md`, and `style.md`
carry every rule needed to execute that task. No other skill file need be loaded.
Every skill's documentation is written in one voice — the austere-analytical-prose
discipline (narrow claim → causal advance → evidence → falsifiability → aphoristic
coda; each skill's fingerprints mapped one-to-one onto its logic steps), so the whole
folder reads as one author; only the task differs.
八个 skill 均**自洽**：其 `SKILL.md`、`logic.md`、`style.md` 含执行该任务所需的全部规则，
无需加载其他 skill 文件。每个 skill 的文档共用一种声音——冷峻思辨学术体的纪律（收窄主张 →
因果推进 → 证据 → 可证伪 → 格言收束；每个 skill 的指纹与其 logic 步一一对应），故整座文件夹
读如一人之手；只是任务不同。

The two general research-post skills divide the reasoning job deliberately.
`structured-plain-expression` turns **one dataset, experiment, or investigation**
into a figure-by-figure evidence chain. `reframing-research-post` works across a
**heterogeneous corpus** — primarily for company and industry research, with the
same neutral method portable to other fields — when the task is to let competing
explanations fight, derive an insight no single source states, and land in a
calibrated conditional judgment. They share plain delivery and evidence discipline;
their primary inference jobs differ.
两个通用研究帖 skill 刻意拆开推理任务。`structured-plain-expression` 把**一份数据、实验
或调查**写成逐图推进的证据链；`reframing-research-post` 面向**异质材料集合**——以公司和
产业研究为主，同一中性方法可迁移到其他领域——让竞争解释交锋，推出没有单一来源直接说出
的洞见，并落到校准后的条件判断。二者共用白话表达与证据纪律；主要推断任务不同。

The four `vd-*` skills are **Vertex Dimension's research workflow** (ingest →
synthesis → essay → render). They embed two voices in `style.md` — **Voice A**
(austere, for the skill docs) and **Voice B** (the deliverable: structured plain for
`report-summaries/` and `synthesis/`, the austere-but-public, brand-aligned essay
voice for `public-essays/`, and the austere monochrome typesetting voice for the
`latex/` PDF) — and carry the brand ethos consistently (*traceable text*; *let the
better answer win, not the louder one*; restraint as premium), without naming
sibling skills in deliverable files.
四个 `vd-*` skill 是 **Vertex Dimension 的研报工作流**（入库 → 综合研判 → 文稿 → 排版）。
它们在 `style.md` 内嵌两种声音——**Voice A**（冷峻，用于 skill 文档）与 **Voice B**（交付物：
`report-summaries/`、`synthesis/` 用结构化白话，`public-essays/` 用冷峻但面向公众、契合
品牌的文稿体，`latex/` PDF 用冷峻纯黑白的排版体）——并一致承载品牌内核（*可追溯的文本*；
*让更好的答案胜出、而非更响的那个*；克制即高级），且交付物中不点名 sibling skill。


---

## Layout | 目录

Every skill folder has the same shape:
每个 skill 文件夹同构：

```
<skill>/
├── SKILL.md   # entry: name + description + overview · 入口
├── logic.md   # the logic layer — argument / structure · 逻辑层（论证／结构）
└── style.md   # the language layer · 语言层
```


| Path               | Role                                                                                       |
| ------------------ | ------------------------------------------------------------------------------------------ |
| `<skill>/SKILL.md` | Entry Cursor loads; carries `name` + `description` · Cursor 加载的入口；含 `name` 与 `description` |
| `<skill>/*.md`     | Optional detail, read on demand · 可选细节，按需读取                                                |


---

## Usage | 使用

A skill is active when its folder sits under a `skills/` directory Cursor reads.
Copy the folder you need:
将某个 skill 的文件夹放入 Cursor 读取的 `skills/` 目录，即生效。复制所需文件夹：

```bash
# project scope · 项目级（仅当前仓库）
cp -r austere-analytical-prose <project>/.cursor/skills/

# personal scope · 个人级（所有项目）
cp -r austere-analytical-prose ~/.cursor/skills/
```

Cursor then applies the skill automatically when a task matches its
`description`, or when you name it explicitly.
随后 Cursor 会在任务命中其 `description` 时自动应用，或在你显式指名时应用。

---

## Authoring | 新增 skill

Add one folder with a `SKILL.md` whose front matter carries `name` (lowercase,
hyphenated) and a `description` stating what the skill does and when to use it;
keep the body concise and move detail into side files; then add one row to
[Skills](#skills--技能).
新增一个文件夹，内含 `SKILL.md`，其 front matter 含 `name`（小写、连字符）与
`description`（说明做什么、何时用）；正文从简，细节移入子文件；然后在
[技能索引](#skills--技能)加一行。

---

## Documentation convention | 文档约定

Every README and `SKILL.md` here shares one documentation format:
本仓库每个 README 与 `SKILL.md` 共用一套文档格式：

1. Bilingual, English first, paired line by line. · 双语、英文在前、逐句配对。
2. Bilingual section headers `## English | 中文`. · 双语小节标题。
3. Tables or code blocks for any index, mapping, or layout. · 索引、映射、目录用表格或代码块。
4. `---` between sections. · `---` 分节。
5. Fixed lexical sets for graded table columns — declared once at the top, bare
   words only, never emoji, never per-row improvisation. · 表格定级列用固定词面集——
   表首声明一次，裸词承载，不用 emoji，不逐行起意。

This is a documentation format, not a prose style — each skill defines its own
voice (austere, plain, or otherwise).
这是文档格式，不是行文风格——每个 skill 自定义其声音（冷峻、白话或其他）。

---

## Encoding | 编码

UTF-8, no BOM. · UTF-8，无 BOM。

---

## Note | 说明

Each skill is a distilled method — a task protocol plus output rules, with
portable examples — not a substitute for evidence. It works from material you
provide or sources it can verify; it never fabricates evidence, quotations,
sources, or certainty.
每个 skill 是一套蒸馏后的方法——任务协议加输出规则，并配以可迁移范例——而非证据的
替代品。它处理你提供或其能核验的材料；绝不捏造证据、引文、来源或确定性。
