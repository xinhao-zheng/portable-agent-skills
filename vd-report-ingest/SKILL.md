---
name: vd-report-ingest
description: >-
  Ingest a new equity-research PDF, markdown, or image into the vd-research
  pipeline — extract pages, build bilingual transcript, agent-authored
  retranslation, and per-report summary. Self-contained: carries its own skill-doc
  voice rules and summary-output rules; no other skill need be loaded. 将新 PDF、
  Markdown 或图片研报入库：分页提取、生成双语文稿、由 agent 对照来源重译、单篇白话摘要。
  自洽完整：内含 skill 文档文体与摘要输出文体；无需加载其他 skill。Use when the
  user drops a new report file, asks to 入库/提取/翻译/摘要 a new PDF or image, or
  says "new report arrived" for this research project.
---

# Research Report Ingest · 研报入库

## What this is | 这是什么

In one line: **a fixed causal chain that turns an opaque PDF or image into a
traceable bilingual transcript and a falsifiable summary — each stage producing
a named artifact before the next runs, so downstream work can point to page N
without trusting memory.**
一句话：**一条固定因果链，把不透明 PDF 或图片变为可追溯的双语文稿与可证伪摘要——
每一阶段产出具名工件后才进入下一步，使下游工作可指向第 N 页而无需采信记忆。**

Its opposite is ad-hoc extraction: translate first, structure later, summarize
from a single read-through. That severs the audit chain — synthesis cannot
re-check a claim the transcript never anchored.
它的反面是临时提取：先译后结构、读一遍就写摘要。审计链由此切断——综合研判无法
复核一份从未锚定的主张。

In Vertex Dimension's terms: before the firm can *model, price, and allocate*, the
raw report must first become **traceable text** — making the substrate clean is
this stage's only job.
用 Vertex Dimension 的话说：在能*建模、定价、配置*之前，原始研报须先变成**可追溯的
文本**——把基底做干净，是本阶段唯一的任务。

---

## Style fingerprint | 风格指纹（九项，与 logic.md 九步一一对应）

1. **Closed intake set** — one source file maps to one slug carrying the full
   title (strip only the real extension, never split on an interior dot); a slug
   collapsed to `YYYYMMDD_<n>` or duplicated across `bilingual-transcripts/` /
   `report-summaries/` is a defect found before extraction opens.
   **闭合入库集**——一个源文件对应一个承载完整标题的 slug（只去真实扩展名、
   绝不在内部点号处截断）；被压成 `YYYYMMDD_<n>` 或在 `bilingual-transcripts/`/
   `report-summaries/` 中重复的 slug，是开提之前就能发现的缺陷。
2. **Gap first: opaque substrate** — the problem is not a missing summary but a
   wrong substrate: binary layout, no page index, language split; extraction
   supplies structure, never judgment.
   **缺口先行：不透明基底**——问题不是"缺摘要"，而是"基底错误"：版式封闭、
   无页码、语种割裂；提取供给结构，不供给判断。
3. **Verbatim first, page-marker gate** — extract page text before any
   translation, every body page carrying `<!-- PDF Page N -->`; translation
   fills empty language blocks, never replaces the extract pass, and a summary
   claim with no mappable page fails the gate.
   **先逐字提取、页标记闸门**——任何翻译之前先提取分页文本，每个正文页带
   `<!-- PDF Page N -->`；翻译填充空语言块、不替代提取步骤，无法映射页码的
   摘要主张判失败。
4. **Artifact-vs-opinion spine** — named files (evidence) vs claims in the
   agent's head (non-evidence); no `-Summary.md` until the `*-Bilingual.md`
   body pages are populated — no summary-from-PDF shortcut.
   **工件 vs 观点脊柱**——具名文件（证据）vs 代理记忆中的主张（非证据）；
   `*-Bilingual.md` 正文页未填齐之前不写 `-Summary.md`——禁止从 PDF 直写
   摘要的捷径。
5. **Proposition-shaped summary** — the one-line conclusion is checkable (*who
   wins, through which mechanism, on what horizon*); `stance` follows the causal
   chain in the body, not the headline mood-word alone.
   **摘要命题化**——一句话结论可检验（*谁因何机制在何窗口受益*）；`stance`
   跟随正文因果链，不单跟标题情绪词。
6. **Evidence by stage** — one table maps each stage to its named artifact and
   gate. Published bilingual MD retains the legacy compatibility value
   `translation: professional human-quality retranslation`; it marks the
   agent-authored retranslation stage, not human authorship, human review, or an
   independently measured quality result. Raw MT is not a shippable final state.
   **分阶段证据对照**——一张表把每步映射到具名工件与闸门。发布的双语 MD 保留兼容性
   状态值 `translation: professional human-quality retranslation`；它只标记 agent
   重译阶段，不证明人工撰写、人工审校或经独立测量的翻译质量。机器直译不是可交付终态。
7. **Named falsifiers** — each summary closes with one observable that would
   break its one-line conclusion; a thin OCR/scan extraction carries an explicit
   confidence caveat.
   **具名证伪条件**——每份摘要以一条可观察项收束，说明何种情形将推翻一句话
   结论；OCR/扫描提取稀薄时写明置信度局限。
8. **Index coda, timestamp fresh** — ingest ends at `scripts/index.py`;
   `synthesis/all-reports-index.md` must carry a new `generated_at` UTC —
   cross-report synthesis is a separate task.
   **索引收束、时间戳刷新**——入库止于 `scripts/index.py`；
   `all-reports-index.md` 须带新的 `generated_at` UTC——跨报告综合是独立任务。
9. **Agent token for interpretive output** — retranslation and `-Summary.md`
   are agent-authored from `*-Bilingual.md`; free Google MT or a third-party OCR
   plugin is not a shippable final state (see [logic.md](logic.md) step 9).
   **解读产出用 agent token**——重译与摘要由 agent 对照双语稿撰写；免费 Google
   机翻或第三方 OCR 插件不是可交付终态（见 [logic.md](logic.md) 第 9 步）。

---

## How to use | 怎么用

**Ingesting fresh** — first read [logic.md](logic.md) for the advance order
(intake → extract → retranslate → summarize with its falsifier → index), then
execute per [style.md](style.md): skill docs in the austere voice; summary files
in the embedded plain-output voice (Voice B in that file).
**新入库**——先读 [logic.md](logic.md) 定推进顺序（接收 → 提取 → 重译 → 摘要并
点名证伪 → 索引），再依 [style.md](style.md) 执行：skill 文档用冷峻体；摘要文件
用该文件内嵌的白话输出体（Voice B）。

**Repairing a broken chain** — first locate which artifact is missing or thin
(bilingual empty? summary ahead of transcript?), fix upstream per [logic.md](logic.md),
then re-run downstream only.
**修复断裂链**——先定位缺失或稀薄的工件（双语空？摘要早于文稿？），按 [logic.md](logic.md)
修上游，再仅重跑下游。

| File | Role |
|------|------|
| [logic.md](logic.md) | Advance order, gates, paths · 推进顺序、闸门、路径 |
| [style.md](style.md) | Skill-doc voice + summary output voice · skill 文档体 + 摘要输出体 |

---

## One contrast | 一个最小对照

> Before (ad-hoc) — *"I read the PDF and wrote a bullish summary."*
> 原做法——*"我读了一遍 PDF，写了一份看多摘要。"*

> After (this skill) — *Extract → `*-Bilingual.md` → retranslate → `*-Summary.md`
> → index row. Each file is evidence for the next; page N is the address of every
> claim.*
> 改后（本 skill）——*提取 → `*-Bilingual.md` → 重译 → `*-Summary.md` → 索引行。
> 每个文件都是下一步的证据；第 N 页是每条主张的地址。*

The difference is entirely: opinion deferred until the transcript exists; the
chain, not the reader's memory, carries the proof.
差别全在：观点延至文稿存在之后；链条——而非读者记忆——承载证据。
