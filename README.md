# portable-agent-skills

Bilingual Agent Skills for writing, research, coursework, and media production. Choose a task from the table and open its `SKILL.md`. Each skill can be used on its own.

这是一组中英文技能，涵盖写作、研究、课程学习和音视频制作。按任务查下表，打开对应的 `SKILL.md` 即可。每项技能都可以单独使用。

---

## Skills | 技能

| Skill | Purpose · 用途 |
|---|---|
| [`austere-analytical-prose`](austere-analytical-prose/SKILL.md) | Refine the thesis, reasoning, and prose of a paper or technical report · 聚焦论文或技术报告的论点，理清论证，精简文字 |
| [`citation-integrity-audit`](citation-integrity-audit/SKILL.md) | Trace each citation to its source and check what it supports · 逐条核对引用原文，检查它是否支持正文的说法 |
| [`structured-plain-expression`](structured-plain-expression/SKILL.md) | Explain one study or dataset figure by figure · 用白话逐图讲清一项研究或一组数据 |
| [`reframing-research-post`](reframing-research-post/SKILL.md) | Compare explanations across sources and write a research post · 对照多份材料，比较不同解释，写成研究文章 |
| [`vd-report-ingest`](vd-report-ingest/SKILL.md) | Turn a research report into a bilingual transcript and summary · 将研报整理成双语文稿和单篇摘要 |
| [`vd-synthesis-refresh`](vd-synthesis-refresh/SKILL.md) | Update the report index, review conflicting findings, or synthesize recent reports · 更新研报索引、核查报告间的分歧，或综合近期研报 |
| [`vd-essay-distill`](vd-essay-distill/SKILL.md) | Turn an existing synthesis into a public research essay · 从已有的综合分析中提炼论点，写成公开研究文章 |
| [`vd-evidence-led-research-brief`](vd-evidence-led-research-brief/SKILL.md) | Investigate a specific question and write a brief with verifiable sources · 围绕一个问题核实材料，写成附有出处的研究简报 |
| [`vd-latex-render`](vd-latex-render/SKILL.md) | Typeset a finished document in LaTeX and compile the PDF · 按项目版式排版，生成 LaTeX 源文件和 PDF |
| [`stanford-lecture-notes`](stanford-lecture-notes/SKILL.md) | Write lecture notes or module summaries from course materials · 根据课程材料整理课堂笔记或模块总结 |
| [`stanford-assignment-guides`](stanford-assignment-guides/SKILL.md) | Prepare bilingual questions, a topic overview, and a guide to each part · 整理双语题面、知识概览和分题作业指南 |
| [`stanford-assignment-analysis`](stanford-assignment-analysis/SKILL.md) | Review completed work against the student's code, written answers, and results · 依据代码、书面答案和结果复盘已完成的作业 |
| [`stanford-assignment-visuals`](stanford-assignment-visuals/SKILL.md) | Create and inspect teaching illustrations for a course or assignment · 为课程或作业制作教学配图，逐张核对 |
| [`stanford-作业交互演示`](stanford-作业交互演示/SKILL.md) | Build an interactive HTML guide with bilingual questions and plain Chinese explanations · 将整份作业做成交互式 HTML，附双语题面和中文白话讲解 |
| [`stanford-课程资料中文版`](stanford-课程资料中文版/SKILL.md) | Translate course materials into Simplified Chinese in their original formats · 将课程资料完整译为简体中文，保留原文件格式 |
| [`stanford-课程视频字幕与配音`](stanford-课程视频字幕与配音/SKILL.md) | Transcribe lectures, add bilingual captions, and optionally dub them in Mandarin · 转录课程录像，制作双语字幕，可按需配普通话音轨 |

The `vd-` skills come from the Vertex Dimension research workflow. The `stanford-` skills were developed for Stanford coursework and can be used with other courses.

`vd-` 系列来自 Vertex Dimension 的研报工作。`stanford-` 系列源于 Stanford 课程，也可用于其他课程。

---

## Layout | 目录

```text
portable-agent-skills/
├── README.md
├── LICENSE
└── <skill>/
    ├── SKILL.md
    ├── logic.md
    └── style.md
```

Start with `SKILL.md` for the inputs, steps, and expected output. Larger skills describe the workflow in `logic.md` and the writing or presentation rules in `style.md`. Lightweight skills keep everything in `SKILL.md`.

先读 `SKILL.md`，了解要提供什么材料、怎么做、最后交付什么。较复杂的技能用 `logic.md` 说明步骤，用 `style.md` 说明写法或版式。轻量技能只需一份 `SKILL.md`。

---

## Compatibility and install | 兼容与安装

Copy the whole skill folder to a location below. Use the `name` from `SKILL.md` for the installed folder name and for direct invocation. The tool uses `description` to match a skill to a request. See the [Agent Skills specification](https://agentskills.io/specification).

将所需技能的整个文件夹复制到下表中的位置。安装目录名和直接调用时的名称均取自 `SKILL.md` 的 `name`。工具根据 `description` 判断何时使用该技能。

| Tool · 工具 | Project · 项目 | User · 用户 | Invoke · 调用 |
|---|---|---|---|
| [Cursor](https://cursor.com/docs/skills) | `.cursor/skills/<skill>/` or `.agents/skills/<skill>/` | `~/.cursor/skills/<skill>/` or `~/.agents/skills/<skill>/` | `/skill-name` |
| [Codex](https://learn.chatgpt.com/docs/build-skills) | `.agents/skills/<skill>/` | `~/.agents/skills/<skill>/` | `$skill-name` |
| [Claude Code](https://code.claude.com/docs/en/skills) | `.claude/skills/<skill>/` | `~/.claude/skills/<skill>/` | `/skill-name` |

From the repository root, set `PROJECT_DIR` to your project, create the destination directory, and run the command for your tool.

在本仓库根目录执行。先将 `PROJECT_DIR` 设为项目路径，建好目标技能目录，再选用对应命令。

```bash
# Cursor
cp -r austere-analytical-prose "${PROJECT_DIR:?}/.cursor/skills/"

# Codex
cp -r austere-analytical-prose "${PROJECT_DIR:?}/.agents/skills/"

# Claude Code
cp -r austere-analytical-prose "${PROJECT_DIR:?}/.claude/skills/"
```

---

## Runtime requirements | 运行要求

Each skill lists the tools its task needs. For example, `vd-report-ingest` needs to read the source PDF or images. `stanford-assignment-visuals` needs image generation and inspection. `vd-latex-render` uses the project's `scripts/render_pdf.py`, Pandoc 3.x, and XeLaTeX with `ctexart` from TeX Live.

具体工具见各技能说明。例如，研报入库需要读取原始 PDF 或图片，教学配图需要生成并检查图像。LaTeX 排版使用项目中的 `scripts/render_pdf.py`、Pandoc 3.x，以及 TeX Live 中的 XeLaTeX 和 `ctexart`。

---

## Verify | 验证

Run the reference validator on the installed folder. Then give a fresh session a representative task and its source files. Check that the intended skill is selected and the result meets the requirements in `SKILL.md`. Repeat on each tool you claim to support.

用参考校验工具检查安装目录。再开一个新会话，提供实际任务和原始材料，核对工具选中的技能，并按 `SKILL.md` 检查结果。对声明支持的每种工具各测一次。

```bash
skills-ref validate ./austere-analytical-prose
```

---

## Authoring | 新增技能

1. Give each skill its own folder. In `SKILL.md`, set a lowercase, hyphenated `name` and describe when to use it. · 每项技能单设目录。在 `SKILL.md` 中用小写字母和连字符填写 `name`，并在 `description` 中写明适用任务。
2. Write in English and Chinese, English first. Keep paths, commands, and field names as written. · 中英文对照，英文在前。路径、命令和字段名保留原样。
3. Name the source material, tools, deliverable, and checks. Write instructions concisely and choose the language of the output for its readers. · 写清所需材料、工具、交付物和检查方法。指令从简，成品的写法由读者和用途决定。
4. Test the skill on a real task, then add one row to the [catalog](#skills--技能). · 用实际任务验证后，在技能表中补一行。

---

## Limits | 使用范围

Use an institution's or brand's conventions when the source material or the user calls for them. Third-party names identify the origin of a method or a compatible tool. Trace quotations and factual claims to their sources, and state what the evidence leaves open.

材料来源或用户要求明确时，才采用相应机构或品牌的规范。第三方名称仅用于说明方法来源或工具兼容性。引文和事实须有出处，证据不足之处应写明。

## Encoding | 编码

UTF-8 without BOM. · UTF-8，无 BOM。

## License | 许可

The repository's instructions and documentation use the [MIT License](LICENSE). Referenced materials and third-party marks belong to their respective owners.

本仓库的技能指令与文档采用 MIT 许可。引用材料与第三方标识归各自权利人所有。
