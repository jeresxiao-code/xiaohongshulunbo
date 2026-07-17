---
name: xhs-orange-tech-carousel
description: Create bright orange-white-pale-blue Chinese Xiaohongshu promotional covers and coherent 3:4 infographic carousel series. Use when the user asks to turn AI tools, productivity methods, tutorials, prompt collections, workflows, checklists, product features, or knowledge content into high-readability Xiaohongshu images matching the established orange technology card style, including requests such as “按上面的风格做图”, “做成一套轮播”, “每个要点一张图”, or “延续这套橙白科技风”.
---

# 小红书橙白科技轮播

将长内容提炼为适合手机阅读的 3:4 中文信息图，并生成统一系列。使用内置图片生成工具；不要用 HTML、SVG 或占位图代替最终图片。

## 工作流程

1. 读取用户提供的文案、图片和既有成品。
2. 判断交付类型：
   - 单一主题：生成 1 张主封面。
   - 多个编号要点：默认每个要点 1 张内容页；用户已有主封面时不要重复生成。
   - 用户要求完整图文：生成主封面 + 内容页；数量由内容决定。
3. 提炼每页信息，只保留：页码、主标题、1 句价值说明、输入/条件、输出/收益、底部行动句。
4. 读取 [references/style-spec.md](references/style-spec.md) 并锁定视觉规范。
5. 读取 [references/prompt-patterns.md](references/prompt-patterns.md)，为每一张图写独立生成提示词。
6. 优先把 [assets/style-cover.png](assets/style-cover.png) 用作主封面风格参考，把 [assets/style-content-page.png](assets/style-content-page.png) 用作内容页风格参考。参考图只用于色彩、卡片、图标、字阶与系列一致性，不要求复制内容。
7. 多张图必须分别调用一次图片生成工具；不要用一次调用的多个随机变体代替不同页面。
8. 出图后逐张复核并保存到项目目录；采用 `01-topic.png`、`02-topic.png` 的编号命名。

## 内容提炼规则

- 主标题控制在 4–12 个汉字；保留用户关键名词。
- 副标题控制在 12–24 个汉字，讲清结果或变化。
- 每页优先使用 3–7 个短标签；单个标签尽量不超过 8 个汉字。
- 不把完整长提示词塞进图片。图片负责解释结构，完整提示词留在帖子正文。
- 用户要求“保留内容中心”时，保留原主题、数量、核心用途和关键输出；允许压缩连接词和重复表述。
- 不虚构价格、效果、数据、品牌背书或用户未提供的功能。
- 默认使用中文；仅保留 Claude、Notion、AI、CEO、OS 等必要专名。

## 系列一致性

- 所有页面使用相同背景、橙色强调、深色标题、圆角卡片和薄线图标。
- 页码放在左上橙色胶囊内；内容页保持同一位置与大小。
- 每页只更换主题图标与信息结构，不能每张换一套艺术风格。
- 主标题始终是第一视觉层级；人物不是该风格的默认元素。
- 每页底部使用橙色圆角行动条，文字为一句简洁结论或行动号召。

## 生成与复核

- 明确写入“精确 3:4 竖版小红书图片”。
- 检查中文主标题、页码、短标签是否准确、可读、无重复。
- 检查所有重要文字均在安全区，卡片不贴边，字号适合手机阅读。
- 检查颜色与参考图一致，避免深色赛博朋克、荧光光效和密集小字。
- 如果生成器输出 2:3，但内容完整且留有安全边距，可扩展左右浅蓝白画布到精确 3:4；禁止裁掉文字或直接拉伸。
- 若主标题错字、文字遮挡、信息缺失或布局明显失衡，重新生成该页。
- 最终报告所有文件路径、尺寸和使用的提示词框架。

## 默认交付

- PNG 格式。
- 单张或每页精确 3:4。
- 保存在当前项目的 `assets/` 下；系列图放入独立子目录。
- 在最终回复中展示成品，并提供可点击文件或目录链接。
