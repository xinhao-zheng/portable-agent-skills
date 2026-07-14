# portable-agent-skills

A portable library of Agent Skills for evidence-bearing writing, research,
coursework, and production. Each skill binds one task contract to two internal
layers — **logic** (how the work advances) and **style** (how the result reads) —
then exposes the same `SKILL.md` to Cursor, Codex, and Claude Code. Hosts differ;
the method does not.
面向写作、研究、课程与生产任务的可迁移 Agent Skills 库。每个 skill 把一项任务契约绑定到
两个内部层——**逻辑**（工作如何推进）与**语言**（结果如何读起来）——再以同一份
`SKILL.md` 供 Cursor、Codex 与 Claude Code 加载。宿主不同；方法不变。

---

## Skills | 技能

| Skill | Purpose | Status |
|---|---|---|
| [`austere-analytical-prose`](austere-analytical-prose/SKILL.md) | Austere analytical prose for papers and technical arguments · 论文与技术论证的冷峻思辨文体 | active · 已发布 |
| [`citation-integrity-audit`](citation-integrity-audit/SKILL.md) | Re-checkable citation provenance for a paper · 论文引用的可复核溯源台账 | active · 已发布 |
| [`structured-plain-expression`](structured-plain-expression/SKILL.md) | One dataset or study → structured plain-language research post · 单一数据或研究 → 结构化白话研究帖 | active · 已发布 |
| [`reframing-research-post`](reframing-research-post/SKILL.md) | Heterogeneous evidence → earned thesis and calibrated judgment · 异质证据 → 经证据赢得的论题与校准判断 | active · 已发布 |
| [`vd-report-ingest`](vd-report-ingest/SKILL.md) | New PDF/Markdown/image → bilingual transcript + summary · 新研报 → 双语文稿与摘要 | active · 已发布 |
| [`vd-synthesis-refresh`](vd-synthesis-refresh/SKILL.md) | Summaries → index, conflict audit, or rolling synthesis · 摘要 → 索引、冲突审计或滚动综合 | active · 已发布 |
| [`vd-essay-distill`](vd-essay-distill/SKILL.md) | Chosen synthesis scope → public research essay · 指定综合范围 → 对外研究文稿 | active · 已发布 |
| [`vd-latex-render`](vd-latex-render/SKILL.md) | Finished document → brand LaTeX + PDF · 定稿文档 → 品牌 LaTeX 与 PDF | active · 已发布 |
| [`stanford-lecture-notes`](stanford-lecture-notes/SKILL.md) | Structured course sources → traceable notes or unit synthesis · 课程来源 → 可追溯笔记或单元综合 | active · 已发布 |
| [`stanford-assignment-guides`](stanford-assignment-guides/SKILL.md) | Assignment sources → bilingual view, overview, and action guide · 作业来源 → 双语题面、概述与行动 Guide | active · 已发布 |
| [`stanford-assignment-analysis`](stanford-assignment-analysis/SKILL.md) | Completed coursework → evidence-linked analysis · 已完成作业 → 证据可追溯分析 | active · 已发布 |
| [`stanford-assignment-visuals`](stanford-assignment-visuals/SKILL.md) | Validated course content → instructional bitmap set · 已验证课程内容 → 教学位图组 | active · 已发布 |

The catalog is flat: one skill, one sibling folder. No skill requires another
skill to be loaded. External tools remain explicit runtime prerequisites, never
hidden sibling dependencies.
目录保持扁平：一个 skill，一个同级文件夹。任何 skill 都不要求同时加载另一个 skill；
外部工具属于显式运行前提，不伪装成隐藏的同级依赖。

---

## Contract | 契约

The portability claim is narrow: any host implementing the Agent Skills format
can load the same task logic and output rules. It does not claim that every host
ships the same tools, permissions, or renderers. Format travels. Capability must
still be present.
可迁移主张刻意收窄：任何实现 Agent Skills 格式的宿主，都能加载同一套任务逻辑与输出规则；
这不意味着每个宿主自带相同工具、权限或渲染器。格式可以迁移；能力仍须真实存在。

| Layer | Role | Invariant |
|---|---|---|
| `name` + `description` | Discovery · 发现 | concise scope, real triggers, no platform lock-in · 范围简洁、触发真实、不锁平台 |
| `SKILL.md` | Task contract · 任务契约 | inputs, outputs, gates, and use path · 输入、输出、闸门与使用路径 |
| `logic.md` | Reasoning layer · 逻辑层 | causal order, evidence boundary, QA · 因果顺序、证据边界与 QA |
| `style.md` | Language layer · 语言层 | documentation voice + artifact-specific output voice · 文档声线＋产物专属声线 |
| Runtime | Host capability · 宿主能力 | tools are checked before the stage that needs them · 工具在对应阶段开始前检查 |

All skill documentation follows the `austere-analytical-prose` discipline:
narrow claim → causal advance → evidence → limitation → earned coda. The
deliverable voice is task-specific. Shared authorship does not mean identical
outputs; it means the same evidentiary discipline survives every task.
全部 skill 文档遵循 `austere-analytical-prose` 的纪律：收窄主张 → 因果推进 → 证据 →
边界 → 经论证赢得的收束。实际交付物使用任务专属声线。同一作者并不意味着产物同腔；
它意味着同一套证据纪律穿过每项任务而不变。

---

## Families | 技能族

| Family | Chain | Boundary |
|---|---|---|
| General writing & research · 通用写作与研究 | prose discipline; citation audit; one-study explanation; heterogeneous-evidence reframing · 文体纪律；引用审计；单一研究解释；异质证据重构 | method-neutral; source claims remain answerable · 方法中立；来源主张可追问 |
| Vertex Dimension · 维度研报 | ingest → synthesis → essay → LaTeX/PDF · 入库 → 综合 → 文稿 → 排版 | project identity and local scripts remain explicit · 项目身份与本地脚本保持显式 |
| Stanford-derived course work · Stanford 衍生课程工作流 | lecture sources → notes; assignment sources → guides; completed work → analysis; validated content → visuals · 讲义 → 笔记；题面 → Guide；完成工件 → 分析；已验证内容 → 配图 | Stanford is a verified reference profile, not an applicability boundary · Stanford 是经验证参照 profile，不是适用边界 |

`structured-plain-expression` and `reframing-research-post` share plain delivery
but solve different inference jobs. The first explains one dataset, experiment,
or investigation figure by figure. The second lets competing explanations fight
across a heterogeneous corpus and earns one conditional judgment.
`structured-plain-expression` 与 `reframing-research-post` 共用白话表达，却承担不同推断
任务：前者逐图解释一份数据、实验或调查；后者让异质材料中的竞争解释交锋，并赢得一项
有条件的判断。

---

## Stanford reference route | Stanford 参照路径

When a live Stanford repository matches the verified artifact pattern, the four
skills preserve its source hierarchy, paths, naming, and quality gates. Every
nonmatching repository — including another Stanford course — derives those
choices locally.
当真实 Stanford 仓库命中经验证工件模式时，四个 skill 保留其来源层级、路径、命名与质量
闸门；任何不匹配仓库——包括另一门 Stanford 课程——都从本地重新推导这些选择。

| Skill | Reads · 读取内容 | Produces · 主要输出 |
|---|---|---|
| [`stanford-lecture-notes`](stanford-lecture-notes/SKILL.md) | Structured lecture sources and transcripts under `_0_Digital Lecture Notes`; completed child notes for parent synthesis · `_0_Digital Lecture Notes` 中的结构化讲义、转录稿与已完成子笔记 | Lesson/Part notes or Unit/Module syntheses under `_1_Module Summaries` · `_1_Module Summaries` 中的单课/Part 笔记或 Unit/Module 综合 |
| [`stanford-assignment-guides`](stanford-assignment-guides/SKILL.md) | Authoritative prompt graph, scoring/metadata, submission rules, starter interfaces · 权威题面图、计分/元数据、提交规则与 starter 接口 | Three verified views under `_2_Assignment Guides` · `_2_Assignment Guides` 下三份经验证视图 |
| [`stanford-assignment-analysis`](stanford-assignment-analysis/SKILL.md) | Verified guide/rubric plus completed code, notebook, written, experiment, or report artifacts · 已验证 Guide/rubric 加真实完成工件 | Evidence-linked analysis under `_3_Assignment analysis (课程详解CN帖子用)` · `_3_Assignment analysis (课程详解CN帖子用)` 下的证据分析 |
| [`stanford-assignment-visuals`](stanford-assignment-visuals/SKILL.md) | Analysis + matching Overview/Summary · Analysis 加匹配的 Overview/Summary | Overview and teaching-section PNGs beside the analysis · 分析目录内的总览与分章 PNG |

The order is strict: source → verified intermediate artifact → downstream
artifact. A downstream file never repairs an upstream omission by invention.
顺序固定：来源 → 经验证中间工件 → 下游工件。下游文件不得用臆造修补上游缺口。

---

## Platform compatibility | 平台兼容

The skills follow the open [Agent Skills specification](https://agentskills.io/specification).
Install the same folder at the host's discovery path; only the path and explicit
invocation syntax change.
本库遵循开放的 [Agent Skills 规范](https://agentskills.io/specification)。把同一个文件夹
放入宿主发现路径即可；变化的只是路径与显式调用语法。

| Host | Project scope | User scope | Explicit invocation |
|---|---|---|---|
| [Cursor](https://cursor.com/docs/skills) | `.cursor/skills/<skill>/` or `.agents/skills/<skill>/` | `~/.cursor/skills/<skill>/` or `~/.agents/skills/<skill>/` | `/skill-name` |
| [Codex](https://learn.chatgpt.com/docs/build-skills.md) | `.agents/skills/<skill>/` | `~/.agents/skills/<skill>/` | `$skill-name` |
| [Claude Code](https://code.claude.com/docs/en/slash-commands) | `.claude/skills/<skill>/` | `~/.claude/skills/<skill>/` | `/skill-name` |

Automatic activation is governed by `description`; explicit invocation remains
the deterministic path when several skills are plausible.
自动触发由 `description` 控制；多个 skill 都可能命中时，显式调用仍是确定路径。

---

## Runtime requirements | 运行要求

| Scope | Required capability |
|---|---|
| Core writing, audit, notes, guides, analysis · 核心写作、审计、笔记、Guide、分析 | read and write Markdown; inspect the supplied repository and source files · 读写 Markdown；检查用户提供的仓库与来源 |
| `vd-report-ingest` | PDF/image reading; project workflow may use Python 3.11+ and PyMuPDF · PDF/图片读取；项目工作流可能需要 Python 3.11+ 与 PyMuPDF |
| `stanford-assignment-visuals` | raster image generation plus actual image inspection · 位图生成能力与实际图片检查能力 |
| `vd-latex-render` | project `scripts/render_pdf.py`, pandoc 3.x, TeX Live, XeLaTeX, `ctexart` · 项目脚本、pandoc 3.x、TeX Live、XeLaTeX、`ctexart` |
| Other project-bound stages · 其他项目绑定阶段 | the local scripts and artifact paths named by that skill · 对应 skill 点名的本地脚本与工件路径 |

A missing capability blocks the stage that needs it. It does not authorize a
silent substitute that changes the artifact contract.
能力缺失会阻断需要它的阶段；这不授权悄悄换用会改变产物契约的替代方案。

---

## Layout | 目录

```text
portable-agent-skills/
├── README.md
├── LICENSE
└── <skill>/
    ├── SKILL.md   # discovery metadata + task contract · 发现元数据＋任务契约
    ├── logic.md   # causal workflow + evidence gates · 因果流程＋证据闸门
    └── style.md   # documentation + output voices · 文档与输出声线
```

`logic.md` and `style.md` are this catalog's authoring convention, not a limit of
the Agent Skills format. A future skill may add `scripts/`, `references/`, or
`assets/` inside its own folder when the task requires them.
`logic.md` 与 `style.md` 是本目录的作者约定，不是 Agent Skills 格式边界。未来 skill 可在
任务确有需要时，于自身目录加入 `scripts/`、`references/` 或 `assets/`。

---

## Install | 安装

Copy one complete skill folder; do not copy `SKILL.md` alone.
复制完整 skill 文件夹；不要只复制 `SKILL.md`。

```bash
# Cursor · project scope
cp -r austere-analytical-prose <project>/.cursor/skills/

# Codex · repository scope
cp -r austere-analytical-prose <project>/.agents/skills/

# Claude Code · project scope
cp -r austere-analytical-prose <project>/.claude/skills/
```

The folder name must match the `name` field. Relative links inside the skill must
remain intact.
文件夹名必须与 `name` 一致；skill 内部相对链接必须保持完整。

---

## Verify | 验证

Validate structure with the Agent Skills reference validator, then test routing
and one realistic task on every host you claim to support.
先用 Agent Skills 参考校验器验证结构，再在每个声称支持的宿主上测试触发与一项真实任务。

```bash
skills-ref validate ./<skill>
```

| Gate | Required result |
|---|---|
| Shape · 形状 | one folder; `SKILL.md` present; referenced files resolve · 单一文件夹；`SKILL.md` 存在；引用文件可解析 |
| Metadata · 元数据 | `name` matches folder; `description` is 1–1024 characters and states what + when · `name` 匹配目录；`description` 为 1–1024 字符并说明做什么＋何时用 |
| Routing · 触发 | positive prompts activate; adjacent tasks do not collide · 正例触发；相邻任务不误撞 |
| Forward test · 前向测试 | a fresh agent completes one raw task without leaked conclusions · 新 Agent 在无结论泄漏下完成原始任务 |
| Runtime · 运行 | required tools exist; produced artifacts pass the skill's own QA · 所需工具存在；产物通过 skill 自身 QA |

Validation proves the package is well formed. It does not prove an unsupported
claim or a missing tool into existence.
校验证明包的形状成立；它不会把无证据主张或缺失工具变成现实。

---

## Authoring | 新增 skill

1. Add one lowercase, hyphenated sibling folder. · 新增一个小写、连字符命名的同级目录。
2. Write `SKILL.md` with `name` and a concise `description` stating what the skill does and when it triggers. · 写入 `name` 与简洁的“做什么＋何时触发”说明。
3. Keep the task contract concise; place causal detail in `logic.md` and language rules in `style.md`. · 任务契约从简；因果细节进 `logic.md`，语言规则进 `style.md`。
4. Declare real runtime dependencies; do not encode one host's tool name as a universal capability. · 声明真实运行依赖；不把单一宿主工具名写成通用能力。
5. Validate, forward-test, then add one row to [Skills](#skills--技能). · 校验、前向测试，再向技能表加一行。

---

## Documentation law | 文档约定

Every root README, `SKILL.md`, `logic.md`, and `style.md` follows one visible
documentation law:
每份根 README、`SKILL.md`、`logic.md` 与 `style.md` 共用一套可见文档纪律：

1. Bilingual, English first, paired passage by passage. · 双语、英文在前、逐段配对。
2. Bilingual section headings: `## English | 中文`. · 双语小节标题。
3. Tables map; code blocks show literal trees or commands; prose explains consequence. · 表格映射；代码块展示真实目录或命令；正文解释后果。
4. `---` separates major sections. · `---` 分隔主要章节。
5. Paths, fields, and fixed lexical sets remain literal; no emoji or per-row improvisation. · 路径、字段与固定词面保持字面一致；不用 emoji，不逐行起意。
6. Documentation uses the austere voice; deliverables use the voice their task requires. · 文档使用冷峻体；交付物使用任务真正需要的声线。

This is one authorship system, not one repeated paragraph. Logic stays common;
specialization remains real.
这是一套作者系统，不是一段模板反复复制。逻辑保持同源；特化保持真实。

---

## Limits | 边界

- Portability covers the skill format and method, not identical host tooling. · 可迁移性覆盖格式与方法，不保证宿主工具完全相同。
- Institutional or brand reference profiles activate only on verified provenance or explicit user direction. · 机构或品牌参照 profile 只在来源经验证或用户明确指定时启用。
- A skill may transform evidence; it may not fabricate evidence, quotations, sources, or certainty. · Skill 可以转换证据，不得捏造证据、引文、来源或确定性。
- Third-party names identify compatibility or method provenance; they do not imply endorsement. · 第三方名称只标识兼容性或方法来源，不表示背书。

These are boundaries, not omissions.
这些是边界，不是遗漏。

---

## Encoding | 编码

UTF-8, no BOM. · UTF-8，无 BOM。

---

## License | 许可

Repository-authored skill instructions and documentation are MIT (see
`LICENSE`). Referenced source materials and third-party marks remain with their
respective owners.
本仓库原创的 skill 指令与文档采用 MIT（见 `LICENSE`）；被引用的来源材料与第三方标识仍归
各自权利人所有。

---

*One method, many hosts. The host supplies tools; the skill supplies the standard. · 一套方法，多种宿主。宿主提供工具；Skill 守住标准。*
