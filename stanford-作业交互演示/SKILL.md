---
name: stanford-assignment-demos
description: >-
  Build an offline HTML walkthrough of a Stanford problem set with complete
  English–Chinese questions and an experiment for each part. 用于双语读题、逐问推导与交互演示。
---

# Stanford Assignment Demos · Stanford 作业交互演示

## Source | 题面

Use the assigned edition. Reproduce every English question and subquestion, pairing each paragraph with its Chinese translation. Give the common setup once before its parts. Keep the original numbering, points, assumptions, formulas, figures, tables, captions, footnotes, data splits, code identifiers and required outputs. Cite the source page.

按本期题册完整收录每道大题和子问，英文原文与中文译文逐段对应。共用题干置于各子问之前。保留题号、分值、假设、公式、图表、图注、脚注、数据划分、代码标识和作答要求，标明原题页码。

## Interaction | 演示

Frame each part around a testable question. Explain new quantities in plain Chinese. Tell the reader which input to change, where to look on the plot and which value will change. Identify the dataset and split, or state the assumptions of the example. For iterative methods, show the initial state, update, stopping condition and loss history. Provide step, run and reset controls.

每个子问给读者一个能动手检验的问题。用白话解释新出现的量，说明改哪个输入、看图的哪里、哪个读数会变。注明课程数据与划分，或写清教学示例的设定。迭代题可单步、连跑和复位，显示初值、更新规则、停止条件与损失轨迹。

Keep essential conditions in the claim and its title. For a proof, connect the example to the general argument and identify the step that uses each assumption. Give one input and an expected result for self-check.

写明结论成立的条件，影响含义的限定词也要写进标题。证明题从例子回到一般推导，指出哪一步用到了题设。自检给出具体输入和可核对的结果。

## Delivery | 交付

Deliver one offline HTML per assignment. Embed scripts, figures and data. Link each question and its experiment in both directions. Align paragraphs side by side on wide screens. On narrow screens, place each English paragraph above its translation. Label axes and units, include a legend and allow dense plots to be enlarged. Archive the question and lesson sources, calculation code, any data preparation scripts and the build command.

每份作业交付一个离线 HTML，内嵌脚本、图形和数据。题面与本问演示双向直达。宽屏按段并排，窄屏每段先英文、后中文。图上标明坐标、单位和图例，密集图表可放大。归档题面与讲解源稿、计算代码、用到的数据准备脚本和重建命令。

Set Chinese titles in a Song-style serif at 28–40 px, body text in a sans serif at 16–17 px, and English question text in Georgia or Cambria. Set charcoal text (`#252925`) on warm white (`#F8F7F4`). Reserve teal (`#16675F`) for actions and current values, and ochre (`#A94B31`) for comparisons. Pair color with marker or line style.

中文标题用 28–40 px 宋体类字体，正文用 16–17 px 无衬线字体，英文题面用 Georgia 或 Cambria 衬线体。暖白底 `#F8F7F4` 配炭灰字 `#252925`。青绿 `#16675F` 仅标示操作和当前数值，赭色 `#A94B31` 标示对照数值。图中的数据系列同时用点形或线型区分。

## Verification | 验收

Compare the bilingual questions with the source, including page breaks, figures and footnotes. Open the HTML offline, follow each question–experiment link in both directions and exercise every part. Check the result against a boundary case or a hand calculation and test keyboard navigation, reading order and formulas on a narrow screen.

对照原题核查双语题面，留意跨页题干、图表和脚注。断网打开 HTML，逐问往返题面与演示并操作控件，用边界值或手算样例核对结果。检查键盘导航、窄屏阅读顺序和公式排版。
