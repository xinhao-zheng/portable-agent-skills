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

Give the reader a way into the question before the worked example. Say in plain Chinese what the quantities stand for and what a satisfactory answer would show. Read the unfamiliar notation aloud in words, unpack the operations in order, and substitute small numbers where useful. For a coding task, trace one input to its expected output. Place this help beside the question or link to it directly from the top.

先让读者读懂题目。用白话说明题里的量各指什么、最后要算出或说明什么。把陌生符号念成一句话，按实际计算顺序拆开，必要时用小数值代入。代码题用一组输入说明预期输出。读题引导紧邻原题，或由页首直接进入。

Start the example with one step a beginner can check by hand. Explain why each later step follows. Ask the reader to predict a change, use a named control and find the result on the graph. For a proof, return from the example to the general argument and its assumptions. Identify course data and splits. For iterative methods, show the initial state, updates, stopping condition and loss history, with step, run and reset controls.

例子从初学者能手算核对的一步开始，逐步说明为什么这样做。让读者先预测，再操作指定控件，在图上找到对应的变化。证明题从例子回到一般推导，指出用到的假设。注明课程数据及划分。迭代题可单步、连跑和复位，显示初值、更新规则、停止条件与损失轨迹。

## Delivery | 交付

Deliver one offline HTML per assignment. Embed scripts, figures and data. Link each question and its experiment in both directions. Align paragraphs side by side on wide screens. On narrow screens, place each English paragraph above its translation. Label axes and units, include a legend and allow dense plots to be enlarged. Archive the question and lesson sources, calculation code, any data preparation scripts and the build command.

每份作业交付一个离线 HTML，内嵌脚本、图形和数据。题面与本问演示双向直达。宽屏按段并排，窄屏每段先英文、后中文。图上标明坐标、单位和图例，密集图表可放大。归档题面与讲解源稿、计算代码、用到的数据准备脚本和重建命令。

Set Chinese titles in a Song-style serif at 28–40 px, body text in a sans serif at 16–17 px, and English question text in Georgia or Cambria. Set charcoal text (`#252925`) on warm white (`#F8F7F4`). Reserve teal (`#16675F`) for actions and current values, and ochre (`#A94B31`) for comparisons. Pair color with marker or line style.

中文标题用 28–40 px 宋体类字体，正文用 16–17 px 无衬线字体，英文题面用 Georgia 或 Cambria 衬线体。暖白底 `#F8F7F4` 配炭灰字 `#252925`。青绿 `#16675F` 仅标示操作和当前数值，赭色 `#A94B31` 标示对照数值。图中的数据系列同时用点形或线型区分。

## Verification | 验收

Compare each walkthrough's bilingual text with the source, including nested parts, page breaks, figures and footnotes. Open a part directly offline and read it from the beginning. Follow the worked example with the controls, check a hand calculation or boundary case, and test links, keyboard navigation and narrow-screen reading order.

逐页对照原题，核查嵌套子问、跨页题干、图表和脚注。断网直接打开任一子问，从头读题，照例子操作并核对手算结果或边界值。检查链接、键盘导航、窄屏阅读顺序和公式排版。
