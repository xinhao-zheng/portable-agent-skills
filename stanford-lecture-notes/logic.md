# Note Skeleton · 笔记推进骨架

The advance order for course lesson notes and higher-level syntheses. Repositories
name and store units differently; source roles and gates remain stable.
本文件给出课程单课笔记与高层综合的推进顺序。仓库对单元的命名与存放各异；来源角色与
闸门保持稳定。

---

## Stanford reference profile + portable fallback | Stanford 参照 profile＋可迁移回退

Activate the **Stanford reference profile** only when the live repository matches
the source workflow's note-artifact pattern; Stanford identity alone is
insufficient. A credible match joins paired lecture `.py` files and `.txt`
transcripts to the live `_0_Digital Lecture Notes` / `_1_Module Summaries`
convention or a completed note anchor. One institution name or filename does not
establish the profile. When matched, derive the course code and unit vocabulary
from metadata, treat `.py` as skeleton and `.txt` as instructor voice, read `.py`
before `.txt`, and reuse only the paths and conventions that actually exist.
只有真实仓库匹配源工作流的笔记工件模式时，才启用 **Stanford 参照 profile**；仅有 Stanford
机构身份并不足够。可信匹配须把成对的讲义 `.py` 与转录稿 `.txt`，同真实存在的
`_0_Digital Lecture Notes` / `_1_Module Summaries` 约定或已完成笔记锚点连接起来；单个
机构名或文件名不能确立 profile。匹配后，从元数据推导课程代码与单元词汇，以 `.py` 作骨架、
`.txt` 作教师声音，先读 `.py`，并只沿用真实存在的路径与约定。

Every nonmatching repository — including another Stanford course — retains the
same causal job: source closure, skeleton before voice, traceable quotations,
child-note synthesis, and assessment mapping. Derive unit names, formats, paths,
and output conventions locally.
任何不匹配的仓库——包括另一门 Stanford 课程——都保留同一因果任务：来源闭合、先骨架
后声音、引文可追溯、子笔记综合与考核映射；单元名、格式、路径与输出约定从本地推导。

---

## Order of advance | 推进顺序（默认骨架）

1. **Close course scope** — inspect the repository before naming the unit.
   Resolve the course title, unit vocabulary (`lecture`, `week`, `part`, `module`,
   `chapter`, or local equivalent), requested granularity, canonical title,
   assessment relation, and live output path. List the complete candidate source
   set. If the Stanford reference profile matches, apply its directories and vocabulary;
   otherwise discover the local equivalent rather than imitate it.
   **闭合课程范围**——命名单元前先检查仓库。解析课程名、单元词汇（`lecture`、`week`、
   `part`、`module`、`chapter` 或本地等价物）、请求粒度、规范标题、考核关系与真实输出
   路径。列出完整候选来源集。命中 Stanford 参照 profile 时应用其目录与词汇；否则发现本地
   等价物，不照搬其外形。

2. **Choose one mode** — a leaf/lesson note reads primary course sources; a
   parent/unit synthesis requires all constituent child notes and reads those
   notes as its corpus. If the repository has only one level, use lesson mode.
   A one-child parent needs no duplicate synthesis unless explicitly requested.
   **选择单一模式**——叶级/单课笔记读课程一手来源；父级/单元综合要求全部子笔记齐备，
   并以它们为语料。仓库只有一层时使用单课模式。单子项父级默认不重复综合，除非明确要求。
   - Gate: missing required child notes block parent synthesis; name the gap. |
     闸门：缺必要子笔记即阻断父级综合；点名缺件。

3. **Classify and read sources by role** — first read structured primary
   materials completely: instructor notes, slides, Markdown, notebooks, code,
   rendered PDFs, or equivalent. Then read transcripts/captions completely.
   Finally, when one exists, read an existing output as a format anchor. The first pass builds
   the concept outline; the speech pass adds explanations, analogies, emphasis,
   and cautions. If no transcript exists, proceed from primary sources and state
   the narrower source scope; do not manufacture instructor voice.
   **按角色分类并阅读来源**——先完整读结构化一手材料：教师讲义、幻灯片、Markdown、
   Notebook、代码、渲染 PDF 或等价物；再完整读转录稿/字幕；若存在，最后读一份既有产物
   作格式锚。
   第一遍建概念骨架，口语遍补解释、类比、强调与警告。无转录稿时可依一手材料继续，但须
   声明来源范围较窄；不得制造教师声音。

4. **Build the source-role join** — use this internal ledger. The `Status` set is
   fixed: `joined`, `primary-only`, `voice-only`, `conflicted`, `missing`.
   **建立来源角色合流表**——使用下列内部台账。`Status` 固定为：`joined`、
   `primary-only`、`voice-only`、`conflicted`、`missing`。

   | Concept · 概念 | Primary mechanism/claim · 一手机制/主张 | Instructor contribution · 教师增量 | Exact address(es) · 精确地址 | Status · 状态 |
   |---|---|---|---|---|
   | one concept · 一个概念 | load-bearing source statement · 承重来源陈述 | explanation/example/caution, if present · 可用解释/例子/警告 | file + local locator · 文件＋局部定位 | fixed set only · 仅用固定词面 |

   Retain spoken insights only when they add to the primary source. A `voice-only`
   item may be attributed as instructor commentary; it cannot silently replace a
   missing primary mechanism. Repetition may support editorial synthesis but may
   not be stitched into a quotation.
   只有口语确有增量时才保留。`voice-only` 项可归因为教师评论，不得悄悄替代缺失的一手机制。
   重复可支撑编辑性综合，不得拼成引文。

5. **Compose the mode-specific irreversible artifact** — adapt labels to the
   course while preserving the relevant inferential order.
   **写成模式专属的不可调换工件**——标题词汇适配课程，同时保留相应推断顺序。

   Lesson note · 单课笔记：
   `Contents → Overview → Core Concepts → Technical/Method Detail → Instructor Insights (if evidenced) → Course & Assessment Path`
   `目录 → 概览 → 核心概念 → 技术/方法细节 → 教师洞见（有证据时）→ 课程与考核脉络`

   Parent synthesis · 父级综合：
   `3–5 sentence overview → Cross-unit chain → Each child distilled as connected narrative → Cross-unit insights → Course & Assessment Path`
   `三至五句概览 → 跨单元主线 → 各子单元连贯浓缩 → 跨单元洞见 → 课程与考核脉络`

   In lesson mode, concepts define, detail explains mechanism, instructor
   insights carry non-duplicated evidence, and the final path connects
   prerequisites, later units, and assessments. A parent synthesis is the
   first-open, standalone review artifact: distill each child unit's load-bearing
   concepts, formulae/code, and conclusion; select representative quotations
   from the child notes; then derive patterns visible only across children. Its
   length follows aggregate coverage and will usually exceed one child note.
   If sections can swap without loss, the artifact is still a pile.
   单课模式中，概念负责定义，细节解释机制，教师洞见承载未重复证据，末尾脉络连接前置、
   后续单元与考核。父级综合是复习时首先打开、可独立使用的工件：浓缩每个子单元的承重
   概念、公式/代码与结论，从子笔记精选代表性引文，再推出只有跨子单元才可见的规律。
   篇幅服从总覆盖量，通常应超过一份子笔记。若章节可无损互换，工件仍是材料堆。

6. **Protect source integrity** — search every quotation against one source;
   preserve wording and local context. Keep years, parameters, amounts, names,
   notation, negation, comparison, causal direction, and certainty exact. When
   the source is not Chinese, translate the quotation immediately below; when it
   is Chinese, preserve it once. Add outside knowledge only when the user requests
   enrichment, and label it apart from course evidence.
   **保护来源完整性**——每条引文须能在单一来源中检索；保留措辞与局部语境。年份、参数、
   金额、人名、记号、否定、比较、因果方向与确定程度必须准确。来源非中文时，引文下一行
   立即给中文翻译；来源为中文时只保留一次。只有用户要求扩展时才加外部知识，并与课程证据
   分开标注。

7. **Bind the repository convention** — discover naming, metadata, Sources,
   Related/Assessment, separators, tables, quotation form, diagrams, footer, and
   destination from completed artifacts. In the live metadata form, enumerate
   every actual input; when `Sources` and `Related` exist, list all input files
   under the former and only verified assessment relations under the latter. If
   no convention exists, use a minimal stable one derived from the course
   hierarchy. Generate multiple units serially so each verified artifact can
   anchor the next.
   **绑定仓库约定**——从既有产物发现命名、元数据、Sources、Related/Assessment、分隔线、
   表格、引文、示意图、footer 与目标目录。按真实元数据形式枚举每个实际输入；存在
   `Sources` 与 `Related` 时，前者列全输入文件，后者只列经验证的考核关联。没有既有约定时，
   从课程层级建立最小稳定约定。多单元串行生成，使每个已验证工件成为下一工件的锚。

8. **Audit and release** — compare the concept list against all sources; verify
   every quotation by search; scan numbers, notation, and proper nouns; confirm
   course identity, assessment mapping, output path, and a complete input ledger.
   Long inputs may be read or written in chunks; the final artifact may not be
   truncated.
   **审计并发布**——以全部来源反查概念清单；逐条搜索引文；扫描数字、记号与专名；确认
   课程身份、考核映射、输出路径与完整输入台账。长输入可分批读写；最终工件不得截断。

---

## Stop conditions | 停止条件

- Missing primary material blocks a lesson note; missing child notes block a
  parent synthesis. | 缺一手材料阻断单课笔记；缺子笔记阻断父级综合。
- A missing transcript narrows attribution; it does not justify invented teacher
  insight. | 缺转录稿会收窄归因范围；不构成虚构教师洞见的理由。
- Conflicting facts remain explicit until resolved; never average or silently
  choose. | 事实冲突在解决前保持显式；不取平均、不暗选。
- Logistics, repeated transitions, and oral filler stay out unless they alter an
  assessment requirement. | 后勤、重复过渡与口语填充不入笔记；除非它们改变考核要求。

---

## Self-check | 自检清单

- [ ] Was the repository's own course/unit vocabulary discovered rather than imposed? |
      是否发现而非强加仓库自身的课程/单元词汇？
- [ ] Is the output mode leaf note or parent synthesis, with prerequisites closed? |
      输出是叶级笔记还是父级综合，前置是否闭合？
- [ ] Were structured primary sources read before transcripts? |
      是否先读结构化一手来源，再读转录稿？
- [ ] Where a real instructor contribution exists, is it bound to the primary
      claim; otherwise is `primary-only` explicit? | 存在真实教师增量时，是否已与一手主张
      绑定；不存在时，是否明确标为 `primary-only`？
- [ ] Can every quotation be found verbatim in one source? |
      每条引文是否可在单一来源逐字找到？
- [ ] Are causal direction, certainty, notation, numbers, and names exact? |
      因果方向、确定程度、记号、数字与专名是否准确？
- [ ] Does the artifact follow the live repository convention and course identity? |
      工件是否服从真实仓库约定与课程身份？
- [ ] Is the final file complete, with every actual input enumerated and every
      assessment relation verified? | 最终文件是否完整、实际输入是否列全、考核关联是否经核验？
