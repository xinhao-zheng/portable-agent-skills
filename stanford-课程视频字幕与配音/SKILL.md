---
name: stanford-captioned-videos
description: >-
  Burn Chinese–English captions into Stanford course recordings and produce
  Mandarin-dubbed editions when requested. Align captions to each edition’s audio. 用于课程录像的双语字幕烧录、普通话配音和音轨对齐。
---

# Stanford Captioned Videos · Stanford 课程视频字幕与配音

## Source | 来源

Identify the recording and requested editions. Use the destination and course numbering supplied for the task. Retain the original frame size, duration and chapters. Use verified captions or transcribe the source audio with timestamps. Check names, symbols and technical terms against the slides or handouts before translating each sentence.

核对原片及所需版本，采用本次任务指定的交付位置和课程编号。保留原画幅、时长和章节。沿用核实过的字幕，缺字幕时按原声转写并保留时间码。对照课件或讲义校正专名、符号和术语，再逐句翻译。

## Captions | 字幕

Burn Chinese above English on the original picture. At a frame height of 1080 pixels, use Microsoft YaHei 49 for Chinese and Segoe UI Semibold 39 for English. Leave at least 168 pixels below the subtitles. Scale both font sizes and the margin with frame height. Use light text, a thin dark outline, a soft shadow and a transparent background. Break lines at phrase boundaries and display each cue during its spoken passage.

在原画面烧录双语字幕，中文在上，英文在下。以画高 1080 像素为基准，中文用微软雅黑 49，英文用 Segoe UI Semibold 39，字幕下缘距底边至少 168 像素。字号和底边距随画高等比缩放。用浅色字、细深色描边、轻阴影和透明背景。按意群断行，每条字幕随对应台词显示。

## Audio | 音轨

Keep the original audio in the English edition and time both subtitle lines to it. For a Mandarin edition, use Qwen3-TTS-12Hz-1.7B-Base with `audio/reference.wav` and its verbatim transcript, `audio/reference.txt`, from the Nihilux repository or a supplied copy. Break the Mandarin script into phrases that follow natural spoken word order. Preserve speaker turns, technical terms, numbers and natural pitch. Fit speech into nearby pauses before increasing speed, up to 1.10×. Give each Chinese cue and its English counterpart the same start and end times on the final Mandarin track. Keep the reference package read-only and write synthesis files in the task workspace.

英语版保留原声，中英两行字幕按原声定时。制作中文版时，用 Qwen3-TTS-12Hz-1.7B-Base 合成普通话。从虚照参考库或调用方提供的副本读取 `audio/reference.wav` 和与录音逐字对应的 `audio/reference.txt`。口播按自然语序断句，保留发言轮次、术语、数字和自然音高。先利用相邻停顿，确需加速时上限为 1.10 倍。以最终普通话音轨为准，为每条中文字幕和对应英文标定相同的起止时间。参考包只读，合成文件写入本次任务工作区。[Nihilux voice reference](https://github.com/xinhao-zheng/nihilux-voice-reference)

## Verification | 验收

Play the opening, a dense passage and the ending of each edition. Check cue timing, terminology, line breaks and legibility on light and dark frames with the player controls open. Use the course numbering and naming rules. Export the requested MP4 editions, matching timed SRTs and bilingual Markdown transcripts as specified.

回放各版片头、密集讲解和片尾，核对字幕起止、术语和断行。在亮暗画面及播放器控件展开时检查可读性。沿用课程编号与命名，按任务交付成片、与音轨对应的 SRT 和双语 Markdown 逐字稿。
