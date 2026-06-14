# Document Architecture · 文档架构

The build order of structured plain expression. The illustrations are
domain-neutral; the architecture is field-independent — it holds for a spec, a
guide, a research note, or a blueprint alike.
本文件给出"结构化白话"的搭建顺序。范例均为领域中性；架构与具体领域无关——无论
技术规范、指南、研究纪要还是蓝图皆适用。

---

## Order of build | 搭建顺序（默认骨架）

1. **Overview first** — the first screen is a map: a diagram, a big table, or a
   one-minute lookup, placed within the opening 200 words, so a reader who stops
   after the first screen still leaves with 80%.
   **概览先行**——第一屏是一张地图：图、大表或一分钟速查，落在开头 200 字内；
   读者即使只读第一屏也带走八成。
   - e.g. open with a "30-second lookup" section before any detail.
     范例：在任何细节之前，先放一节"30 秒速查"。

2. **Three layers, disclosed in order** — overview → detailed body → appendix;
   each layer stands on its own, and the reader descends only as far as the need.
   **三层，按序披露**——概览 → 详细主体 → 附录；每层自足，读者按需下探。
   - Overview = the map; body = the argument and examples; appendix = lookup
     tables, numbering, references.
     概览＝地图；主体＝论证与例子；附录＝映射表、编号、引用。

3. **Form follows relation** — pick the form from the information relation, not
   from habit.
   **形式随关系**——按信息关系选形式，而非按习惯。
   - parallel / contrast / classification / mapping → a table; sequence → a
     numbered list or flow; a single thread → short prose.
     并列／对比／分类／映射 → 表格；时序 → 编号列表或流程；单一叙事 → 短段。

4. **Every unit is four-part** — a task, step, or experiment runs: why (its role
   in the whole) → how (input / action / output) → how to judge (continue / redo
   / stop) → expected (a number or a shape).
   **每个单元四件套**——任务／步骤／实验走：为什么（在整体中的角色）→ 怎么做
   （输入／操作／输出）→ 怎么判断（继续／回炉／停手）→ 预期（一个数字或形态）。

5. **Anticipate the objection** — after "the conclusion is X", ask "how would a
   reviewer rebut X?" and answer it, rather than leaving the reader to.
   **预判反对**——给出"结论是 X"后，先问"审稿人会怎么反驳 X？"并作答，而非留给
   读者去问。
   - e.g. *"X. One will ask: only on your data? — reproduced on three public
     sets, all above baseline (see §6)."*
     范例："X。有人会问：只在你的数据上成立？——已在三个公开集复现，均高于基线
     （见 §6）。"

6. **Cross-reference by address** — point to a specific section or file; never
   "see above" or "as mentioned".
   **按地址交叉引用**——指向具体小节或文件；不用"见上文""如前所述"。
   - ✓ "as in §2.3" / "see `guide.md` §4" — ✗ "as mentioned earlier".
     ✓ "如 §2.3" / "见 `guide.md` §4" — ✗ "如前所述"。

7. **Close with a self-check** — end the document with a short checklist (5–8
   boxes) that restates its own standards.
   **以自检收尾**——文末放一张简短清单（5–8 条），复述本文档自己的标准。

---

## Self-check | 自检清单

- [ ] Does the first screen convey 80% in 30 seconds? |
      第一屏是否 30 秒传达八成？
- [ ] Are the three layers (overview / body / appendix) each complete? |
      三层（概览／主体／附录）是否各自自足？
- [ ] Is each information relation in its right form (table / list / prose)? |
      每种信息关系是否用了对的形式（表格／列表／散文）？
- [ ] Does every task or step run the four parts (why → how → judge → expected)? |
      每个任务／步骤是否走了四件套（为什么 → 怎么做 → 怎么判断 → 预期）？
- [ ] Is each persuasive claim met with its own rebuttal-and-answer? |
      每个说服性结论是否自带反驳与回答？
- [ ] Are all cross-references specific (section / file), never "see above"? |
      所有交叉引用是否具体（小节／文件），无"见上文"？
- [ ] Does the document end on a self-check checklist? |
      文档是否以自检清单收尾？
