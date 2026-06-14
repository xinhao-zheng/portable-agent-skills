# cursor-skills

A collection of Cursor Agent Skills, centered on writing. Each skill is a
self-contained folder defined by two things — its **argument logic** (how the
reasoning advances) and its **language style** (how each sentence reads); Cursor
loads it only when the skill's `description` matches the task. The repository is
flat: skills are added as sibling folders, not nested.
Cursor Agent Skills 集合，以写作为主。每个 skill 由两件事定义——**论证逻辑**
（论证如何推进）与**语言风格**（每句如何读起来）；仅当 skill 的 `description`
命中任务时，Cursor 才加载它。仓库保持扁平：skill 以同级文件夹新增，不嵌套。

Single author · Xinhao Zheng (Independent Researcher).
单一作者；郑鑫豪（独立研究者）。

---

## Skills | 技能


| Skill                                                         | Purpose                                                                          | Status       |
| ------------------------------------------------------------- | -------------------------------------------------------------------------------- | ------------ |
| `[austere-analytical-prose](austere-analytical-prose/)`       | An austere, analytical voice for papers and technical arguments · 论文与技术论证的冷峻思辨文体 | active · 已发布 |
| `[structured-plain-expression](structured-plain-expression/)` | A structured, plain-language voice for long-form documents · 长文档的结构化白话文体         | active · 已发布 |


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

This is a documentation format, not a prose style — each skill defines its own
voice (austere, plain, or otherwise).
这是文档格式，不是行文风格——每个 skill 自定义其声音（冷峻、白话或其他）。

---

## Encoding | 编码

UTF-8, no BOM. · UTF-8，无 BOM。

---

## Note | 说明

Each skill is a distilled style guide — a voice encoded as rules, with
domain-neutral examples — not a content generator. It shapes how your own
material reads; it does not supply the material.
每个 skill 是一份蒸馏出的风格指南——把一种声音编码为规则、配以领域中性的范例
——而非内容生成器。它只塑造你自己素材的"读法"，不替你提供素材。