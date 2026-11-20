---
name: stanford-assignment-demos
description: >-
  Build an offline HTML walkthrough of a Stanford problem set with complete
  English–Chinese questions and an experiment for each part. 用于双语读题、逐问推导与交互演示。
---

# Stanford Assignment Demos · Stanford 作业交互演示

## Source | 题面

Use the assigned edition. Open each walkthrough with the parent question and the current part in English and Chinese, paired paragraph by paragraph and visible on the same page. Include shared definitions and any intermediate setup the part relies on. Preserve numbering, points, assumptions, formulas, figures, tables, captions, footnotes, data splits, code identifiers and required outputs. Cite the source page.

每个演示页开头直接列出本期大题和当前子问的完整英中题面，原文译文逐段对应，默认展开。补齐本问沿用的条件、定义及中间层题干。保留题号、分值、假设、公式、图表、图注、脚注、数据划分、代码标识和作答要求，标明原题页码。

## Interaction | 演示

Teach each part to a first-time reader. Say what is given and what to find. Work through a small example in plain Chinese, explaining each new symbol and why each step follows. Show intermediate values or states. Ask the reader to predict a change, try a named control and compare the result with the example. Then return to the original question and its assumptions.

把每个子问讲给第一次接触它的人。先说已知什么、要求什么，再带读者算一个小例子。符号一出现就用白话解释，写出中间数值或状态，讲清每一步为什么这样做。让读者先猜，再操作指定控件，到图上或读数里核对。最后带着例子回到原题，说明哪些条件起了作用。

Distinguish teaching examples from course data and identify the split. For a proof, show how the reasoning extends beyond the example. For an iterative method, show the initial state, an update, the stopping condition and loss history, with step, run and reset controls. Give one input and an expected result for self-check.

区分教学例子和课程数据，注明数据划分。证明题说明怎样从具体例子推到一般情形。迭代题可单步、连跑和复位，显示初值、更新规则、停止条件与损失轨迹。自检给出具体输入和可核对的结果。

## Delivery | 交付

Deliver one offline HTML per assignment. Embed scripts, figures and data. Link each question and its experiment in both directions. Align paragraphs side by side on wide screens. On narrow screens, place each English paragraph above its translation. Label axes and units, include a legend and allow dense plots to be enlarged. Archive the question and lesson sources, calculation code, any data preparation scripts and the build command.

每份作业交付一个离线 HTML，内嵌脚本、图形和数据。题面与本问演示双向直达。宽屏按段并排，窄屏每段先英文、后中文。图上标明坐标、单位和图例，密集图表可放大。归档题面与讲解源稿、计算代码、用到的数据准备脚本和重建命令。

Set Chinese titles in a Song-style serif at 28–40 px, body text in a sans serif at 16–17 px, and English question text in Georgia or Cambria. Set charcoal text (`#252925`) on warm white (`#F8F7F4`). Reserve teal (`#16675F`) for actions and current values, and ochre (`#A94B31`) for comparisons. Pair color with marker or line style.

中文标题用 28–40 px 宋体类字体，正文用 16–17 px 无衬线字体，英文题面用 Georgia 或 Cambria 衬线体。暖白底 `#F8F7F4` 配炭灰字 `#252925`。青绿 `#16675F` 仅标示操作和当前数值，赭色 `#A94B31` 标示对照数值。图中的数据系列同时用点形或线型区分。

## Verification | 验收

Compare each walkthrough's bilingual text with the source, including nested parts, page breaks, figures and footnotes. Open a part directly offline and read it from the beginning. Follow the worked example with the controls, check a hand calculation or boundary case, and test links, keyboard navigation and narrow-screen reading order.

逐页对照原题，核查嵌套子问、跨页题干、图表和脚注。断网直接打开任一子问，从头读题，照例子操作并核对手算结果或边界值。检查链接、键盘导航、窄屏阅读顺序和公式排版。
