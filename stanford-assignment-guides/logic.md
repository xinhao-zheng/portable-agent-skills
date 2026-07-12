# Guide Skeleton · 指南推进骨架

The advance order for course assignment guide artifacts. Source formats vary;
the truth model and no-solution boundary do not.
本文件给出课程作业指南工件的推进顺序。来源格式会变；事实模型与无答案边界不变。

---

## Stanford reference profile + portable fallback | Stanford 参照 profile＋可迁移回退

Activate the **Stanford reference profile** only when the live repository matches
the source workflow's guide-artifact constellation; Stanford identity alone is
insufficient. A credible match links an assignment root and authoritative prompt
dependency graph to scoring/metadata interfaces and the live
`_2_Assignment Guides` convention or a completed `A1_...` anchor. One path or
filename does not establish the profile. When matched, derive the course code;
close `tex/main.tex` and every real `.tex/.pytex` dependency when present; bind
the live `points.json`, `meta.json`, `README.md`, submission/grader interfaces,
and rendered PDF by role. Preserve the detected `A{N}_Assignment_...` three-file
pattern under `_2_Assignment Guides`, using A1 as the format anchor when present.
只有真实仓库匹配源工作流的 Guide 工件组合时，才启用 **Stanford 参照 profile**；仅有
Stanford 机构身份并不足够。可信匹配须把作业根与权威题面依赖图，同计分/元数据接口及真实的
`_2_Assignment Guides` 约定或已完成 `A1_...` 锚点连接起来；单个路径或文件名不能确立
profile。匹配后，推导课程代码；存在 LaTeX 时闭合 `tex/main.tex` 与全部真实
`.tex/.pytex` 依赖；按角色绑定真实 `points.json`、`meta.json`、`README.md`、提交/grader
接口与渲染 PDF。保留 `_2_Assignment Guides` 下检测到的
`A{N}_Assignment_...` 三件套模式；存在 A1 工件时以其作格式锚。

Every nonmatching repository — including another Stanford course — preserves the
same truth-model and three-projection task, but derives authoritative sources,
graded units, filenames, and output paths locally.
任何不匹配的仓库——包括另一门 Stanford 课程——都保留同一事实模型与三投影任务，但从
本地推导权威来源、计分单元、文件名与输出路径。

---

## Artifact modes | 工件模式

| Mode · 模式 | Default output concept · 默认产物概念 | Primary question · 核心问题 |
|---|---|---|
| Bilingual source view · 双语来源视图 | Complete source + Chinese when distinct · 完整原题＋非中文时的中文翻译 | What exactly does the source say? · 原题究竟说什么？ |
| Overview · 知识概述 | Capability and concept map · 能力与知识地图 | What does it test? · 它考什么？ |
| Chinese action guide · 中文行动指南 | Graded-unit checklist · 计分单元速查 | What must I do, submit, and respect? · 我须做什么、交什么、遵守什么？ |

Use the repository's existing filenames. If none exist, derive stable names from
course identity and assignment ID; do not impose an `AN_...` pattern universally.
沿用仓库既有文件名。若无先例，则从课程身份与作业 ID 推出稳定命名；不把 `AN_...` 模式
强加给所有课程。

---

## Order of advance | 推进顺序（默认骨架）

1. **Resolve canonical identity** — discover course title/code, assignment ID
   and title, live root, authoritative rendered artifact, due-date source,
   scoring source, code/template root, and output directory. The source may be
   PDF, HTML/LMS export, Markdown, DOCX, LaTeX, notebook, or a combination.
   A provided path becomes the starting root, not proof that it is the only source.
   **解析规范身份**——发现课程名/代码、作业 ID 与标题、真实根目录、权威渲染工件、截止日期
   来源、计分来源、代码/模板根与输出目录。来源可以是 PDF、HTML/LMS 导出、Markdown、
   DOCX、LaTeX、Notebook 或组合。用户提供的路径是起点，不证明它是唯一来源。

2. **Close the source graph** — follow the format actually present. For LaTeX,
   recurse from the main file through every real `input/include`; for Markdown,
   notebooks, or HTML, follow linked/included files and section order; for DOCX/PDF,
   inspect the full rendered structure. Bind available scoring/metadata files,
   README/submission policy, starter code interfaces, grader instructions, and
   the final rendered order. Under a matching Stanford reference profile, `tex/main.tex`,
   `points.json`, `meta.json`, and `submission.py` have the roles defined above;
   outside it, none is universally required.
   **闭合来源图**——服从实际格式。LaTeX 从主文件递归真实 `input/include`；Markdown、
   Notebook、HTML 跟随链接/引用与章节顺序；DOCX/PDF 检查完整渲染结构。绑定可用计分/元数据、
   README/提交政策、starter code 接口、grader 说明与最终渲染顺序。Stanford 参照 profile 下，
   `tex/main.tex`、`points.json`、`meta.json`、`submission.py` 承担上文规定角色；
   离开该 profile 后，它们不是普遍必需件。

3. **Build one assignment truth model** — record every visible and operative
   block in order: guidelines, submission and integrity rules, environment/test
   instructions, problem introductions, every graded unit, prompt templates,
   source-authored examples/sample solutions, references when present, and
   expected-output clauses. Preserve source-authored examples because they are
   evidence; never extend them into a new solution. Bind each graded unit to its
   source ID, type, points/weight, interface,
   input/output form, deliverable, and constraints. Derive totals from the actual
   scoring model; never confuse test case IDs with question IDs.
   **建立单一作业事实模型**——按顺序记录所有可见且有效区块：Guidelines、提交与诚信规则、
   环境/测试说明、题目引言、每个计分单元、Prompt Template、来源自带的示例/示例答案、
   真实存在的 References、预期输出条款。来源自带示例属于证据，须保留；不得据此续写新答案。
   每个计分单元绑定来源 ID、类型、分值/权重、接口、输入输出形式、交付物与限制。从真实计分
   模型推出总分；不得把测试 ID 混作题目 ID。

4. **Project the bilingual source view** — preserve the source-language text
   unchanged. When the source is not Chinese, translate by semantic block: a
   complete introduction or graded unit first, then one Chinese blockquote. When
   the source is Chinese, preserve it once; do not fabricate a duplicate
   translation layer. Keep formulae, code, commands, paths,
   names, and notation unchanged. Preserve conditions, parallel relations,
   contrast, causality, and certainty. Cover every learner-visible, operative block
   in the authoritative assignment; invent none. Private grader and hidden-test
   artifacts may reconcile the truth model internally, but they never enter the
   source view.
   **投影双语来源视图**——源语言文本不改。源语言非中文时，按语义块翻译：先完整呈现引言
   或计分单元，再给一个中文 blockquote；源语言已是中文时只保留一次，不虚构重复翻译层。
   公式、代码、命令、路径、专名与记号原样保留。条件、并列、转折、
   因果与确定程度保持一致。覆盖权威作业中一切学习者可见且有效的区块；不虚构任何区块。
   私有 grader 与 hidden-test 工件只可在内部对账，绝不进入来源视图。

5. **Derive the Overview** — only after the truth model closes. Write:
   assignment capability in 3–5 sentences → concept-definition mapping →
   graded-unit-to-concept mapping → course/unit/assessment relation. Explain what
   the assignment trains; do not restate the entire prompt or solve it.
   **推出 Overview**——仅在事实模型闭合后生成。结构为：三至五句能力概述 → 概念定义映射 →
   计分单元—知识点映射 → 课程/单元/考核关系。说明作业训练什么；不复述完整题面，不解题。

6. **Derive the Chinese action guide** — require the bilingual view and Overview
   or their freshly validated in-memory equivalents. Open every parent problem
   with a 2–4 sentence orientation: shared setting, target capability, and how
   its subproblems divide the work. Then give every smallest graded unit its own
   entry: source ID, score/type, prompt meaning, what to do, expected deliverable,
   operative constraints, and one warning. Compress background, never obligations.
   The warning may flag format, boundary, or omission; it may not supply an
   answer, derivation, pseudocode, or implementation strategy.
   **推出中文行动 Guide**——要求双语视图与 Overview 已存在，或本次已验证的等价内存模型。
   每道大题先用二至四句定位共同情境、目标能力及各小题分工；再为每个最小计分单元建立独立
   条目：来源 ID、分值/类型、题意、做什么、预期交付物、有效限制、一句提醒。可压背景，不压
   义务。提醒可指出格式、边界或遗漏；不得给答案、推导、伪代码或实现策略。

7. **Bind the serial chain** — generate only requested modes while satisfying
   their upstream gates. For a bundle: bilingual view → Overview → action guide,
   auditing each before the next. Align metadata, contents, separators, headings,
   tables, and footer with the nearest completed artifact. If none exists, define
   one minimal convention and hold it across the set.
   **绑定串行链**——只生成所请求模式，同时满足上游闸门。整套按双语视图 → Overview → 行动
   Guide，逐件审计后继续。元数据、目录、分隔线、标题、表格与 footer 对齐最近完成工件；
   若无先例，定义一个最小约定并贯穿整套。

8. **Reconcile and release** — compare every artifact against the truth model:
   course/assignment identity, date, score/weight, type, terminology translation,
   visible order, graded-unit count, expected outputs, references, filenames, and
   absence of agent-generated solutions. Source-authored sample solutions remain
   only where the authoritative source view requires them.
   Record the authority rule used when sources disagree. Long files may be written
   in chunks; final files may not be shortened or truncated.
   **对账并发布**——用事实模型反查每份工件：课程/作业身份、日期、分值/权重、类型、术语
   译法、可见顺序、计分单元数、预期输出、References、文件名与“不新增答案”边界。来源自带
   示例答案只在权威来源视图要求处保留。来源冲突时记录采用的权威规则。
   长文件可分批写；最终文件不得缩写或截断。

---

## Authority policy | 权威策略

Infer authority from the repository and state it before resolving conflicts.
A common pattern is: source document controls wording; scoring system controls
points; metadata/LMS controls deadlines; rendered artifact controls visible order;
starter code controls interfaces. This is a default hypothesis, not a universal law.
从仓库推断权威层级，并在解决冲突前写明。常见模式是：源文档控制措辞；计分系统控制分值；
元数据/LMS 控制截止日期；渲染工件控制可见顺序；starter code 控制接口。这是默认假设，
不是普遍定律。

- If an existing guide conflicts with authority, repair the guide. |
  既有 Guide 与权威来源冲突时，修 Guide。
- If authority remains ambiguous and changes the deliverable materially, name
  the conflict and request direction. | 权威仍不明确且会实质改变交付物时，点名冲突并请求方向。
- A missing standard template placeholder is non-blocking only after comparison
  shows it carries no real content. | 标准模板占位缺失只有在对比确认无真实内容后才不阻塞。

---

## Self-check | 自检清单

- [ ] Were course identity, assignment identity, and source authority discovered? |
      是否发现课程身份、作业身份与来源权威？
- [ ] Is the actual dependency graph complete for the formats present? |
      对实际存在的格式，依赖图是否完整？
- [ ] Are all visible and operative blocks represented, with no invented section? |
      所有可见有效区块是否覆盖，且无虚构章节？
- [ ] Are scores/weights derived from the real grading model and reconciled? |
      分值/权重是否来自真实计分模型并完成对账？
- [ ] Is original-language text unchanged and translation faithful? |
      原语言文本是否未改、翻译是否忠实？
- [ ] Does the Overview map every graded unit to a real concept? |
      Overview 是否把每个计分单元映射到真实概念？
- [ ] Does the action guide preserve obligations while adding no solution? |
      行动 Guide 是否保留义务且未新增答案？
- [ ] Do all requested artifacts agree on identity, scoring, terminology, order,
      and naming? | 所有请求工件是否在身份、计分、术语、顺序与命名上完全一致？
