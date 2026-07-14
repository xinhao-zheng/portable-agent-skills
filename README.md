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

| Skill | Purpose |
|---|---|
| [`austere-analytical-prose`](austere-analytical-prose/SKILL.md) | Austere analytical prose for papers and technical arguments · 论文与技术论证的冷峻思辨文体 |
| [`citation-integrity-audit`](citation-integrity-audit/SKILL.md) | Re-checkable citation provenance for a paper · 论文引用的可复核溯源台账 |
| [`structured-plain-expression`](structured-plain-expression/SKILL.md) | One dataset or study → structured plain-language research post · 单一数据或研究 → 结构化白话研究帖 |
| [`reframing-research-post`](reframing-research-post/SKILL.md) | Heterogeneous evidence → earned thesis and calibrated judgment · 异质证据 → 经证据赢得的论题与校准判断 |
| [`vd-report-ingest`](vd-report-ingest/SKILL.md) | New PDF/Markdown/image → bilingual transcript + summary · 新研报 → 双语文稿与摘要 |
| [`vd-synthesis-refresh`](vd-synthesis-refresh/SKILL.md) | Summaries → index, conflict audit, or rolling synthesis · 摘要 → 索引、冲突审计或滚动综合 |
| [`vd-essay-distill`](vd-essay-distill/SKILL.md) | Chosen synthesis scope → public research essay · 指定综合范围 → 对外研究文稿 |
| [`vd-latex-render`](vd-latex-render/SKILL.md) | Finished document → brand LaTeX + PDF · 定稿文档 → 品牌 LaTeX 与 PDF |
| [`stanford-lecture-notes`](stanford-lecture-notes/SKILL.md) | Structured course sources → traceable notes or unit synthesis · 课程来源 → 可追溯笔记或单元综合 |
| [`stanford-assignment-guides`](stanford-assignment-guides/SKILL.md) | Assignment sources → bilingual view, overview, and action guide · 作业来源 → 双语题面、概述与行动 Guide |
| [`stanford-assignment-analysis`](stanford-assignment-analysis/SKILL.md) | Completed coursework → evidence-linked analysis · 已完成作业 → 证据可追溯分析 |
| [`stanford-assignment-visuals`](stanford-assignment-visuals/SKILL.md) | Validated course content → instructional bitmap set · 已验证课程内容 → 教学位图组 |

The catalog is flat: one skill, one sibling folder. No skill requires another
skill to be loaded. External tools remain explicit runtime prerequisites, never
hidden sibling dependencies.
目录保持扁平：一个 skill，一个同级文件夹。任何 skill 都不要求同时加载另一个 skill；
外部工具属于显式运行前提，不伪装成隐藏的同级依赖。

---

## Contract | 契约

A compliant host can load the same task logic and output rules; tools,
permissions, and renderers remain host capabilities. Format travels. Capability
must still be present.
合规宿主可以加载同一套任务逻辑与输出规则；工具、权限与渲染器仍属宿主能力。格式可以
迁移；能力必须真实存在。

| Layer | Role | Invariant |
|---|---|---|
| `name` + `description` | Discovery · 发现 | concise scope, real triggers, no platform lock-in · 范围简洁、触发真实、不锁平台 |
| `SKILL.md` | Task contract · 任务契约 | inputs, outputs, gates, and use path · 输入、输出、闸门与使用路径 |
| `logic.md` | Reasoning layer · 逻辑层 | advance order, evidence boundary, QA · 推进顺序、证据边界与 QA |
| `style.md` | Language layer · 语言层 | documentation voice + artifact-specific output voice · 文档声线＋产物专属声线 |
| Runtime | Host capability · 宿主能力 | tools are checked before the stage that needs them · 工具在对应阶段开始前检查 |

All skill documentation inherits the `austere-analytical-prose` discipline:
narrow scope → load-bearing advance → evidence → honest limit → earned close.
Argumentative tasks use causality; audit, build, and visual tasks translate it
into provenance, dependency, or rendered evidence. Deliverables stay task-specific.
全部 skill 文档继承 `austere-analytical-prose` 的纪律：收窄范围 → 承重推进 → 证据 →
诚实边界 → 经论证赢得的收束。论说任务使用因果；审计、构建与视觉任务则转译为溯源、
依赖或可见证据。交付物保持任务特化。

### Families | 技能族

| Family | Chain | Boundary |
|---|---|---|
| General writing & research · 通用写作与研究 | prose discipline; citation audit; one-study explanation; heterogeneous-evidence reframing · 文体纪律；引用审计；单一研究解释；异质证据重构 | method-neutral; source claims remain answerable · 方法中立；来源主张可追问 |
| Vertex Dimension · 维度研报 | ingest → synthesis → essay → LaTeX/PDF · 入库 → 综合 → 文稿 → 排版 | project identity and local scripts remain explicit · 项目身份与本地脚本保持显式 |
| Stanford-derived course work · Stanford 衍生课程工作流 | lecture sources → notes; assignment sources → guides; completed work → analysis; validated content → visuals · 讲义 → 笔记；题面 → Guide；完成工件 → 分析；已验证内容 → 配图 | Stanford is a verified reference profile, not an applicability boundary · Stanford 是经验证参照 profile，不是适用边界 |

### Stanford reference profile | Stanford 参照 profile

Stanford is a verified reference profile, not an applicability boundary. On an
artifact-pattern match, the four course skills preserve its hierarchy, naming,
paths, and gates; otherwise they derive them locally. The order remains source →
verified intermediate artifact → downstream artifact.
Stanford 是经验证参照 profile，不是适用边界。工件模式命中时，四个课程 skill 保留其
层级、命名、路径与闸门；否则均从本地推导。顺序始终是来源 → 经验证中间工件 → 下游工件。

---

## Compatibility and install | 兼容与安装

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

The folder name must match the `name` field, and relative links must remain
intact.
文件夹名必须与 `name` 字段一致，内部相对链接必须保持完整。

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

New skills preserve one authorship system without repeating one template:
documentation keeps the austere discipline; deliverables keep the voice their
task requires.
新增 skill 延续同一作者系统，而非复刻同一模板：文档守住冷峻纪律；交付物保留任务真正
需要的声线。

1. Add one lowercase, hyphenated sibling folder. · 新增一个小写、连字符命名的同级目录。
2. Write `SKILL.md` with `name` and a concise `description` stating what the skill does and when it triggers. · 写入 `name` 与简洁的“做什么＋何时触发”说明。
3. Keep the contract concise; put causal detail in `logic.md` and language rules in `style.md`. · 契约从简；因果细节进 `logic.md`，语言规则进 `style.md`。
4. Write bilingually, English first; use bilingual headings, mapping tables, literal code blocks, and fixed paths or fields. · 双语、英文在前；使用双语标题、映射表、字面代码块及固定路径或字段。
5. Declare real runtime dependencies; never treat one host's tool name as a universal capability. · 声明真实运行依赖；不把单一宿主工具名当成通用能力。
6. Validate, forward-test, then add one row to [Skills](#skills--技能). · 校验、前向测试，再向技能表加一行。

---

## Limits | 边界

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
