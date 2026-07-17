# 图片生成提示词模板

## 主封面

```text
Use case: ads-marketing
Asset type: exact 3:4 vertical Xiaohongshu promotional cover
Primary request: 为[主题]制作高点击中文主封面。
Style: bright warm-white to pale sky-blue enterprise AI infographic, vivid coral-orange key panels, graphite bold Chinese text, cyan glass cards, mint-green checks, subtle grid, clean and professional.
Composition: 顶部小标签；上中部超大主标题；中央橙色圆角主题图标；周围放置[数量]个短标签卡片；底部橙色行动条。
Text (verbatim): “[主标题]” “[核心卖点]” “[标签1]” “[标签2]” … “[行动句]”
Constraints: exact 3:4 portrait, mobile readable Chinese, safe margins, no people, no watermark, no extra English, no tiny paragraphs, no misspellings, no duplicated labels, no dark cyberpunk.
```

## 内容页

```text
Use case: ads-marketing
Asset type: one coherent page in an exact 3:4 Xiaohongshu infographic carousel
Input image: use the supplied style-content reference only for palette, typography, rounded cards, icons, spacing and hierarchy.
Series style: bright warm-white to pale sky-blue background, coral-orange key panels, graphite bold Chinese text, cyan glass cards, mint-green checks, subtle grid and line icons, no people.
Composition: 左上页码；顶部超大标题；一句价值说明；中央橙色主题图标；“你需要填写/输入”与“AI 会输出/你将获得”两个区域；底部橙色行动条。
Text (verbatim): “[页码]” “[主标题]” “[副标题]” “[输入标签1]” … “[输出标签1]” … “[行动句]”
Visual metaphor: [与该页主题对应的中心图标、流程或结构]
Constraints: exact 3:4 portrait, all Chinese text accurate and legible, safe margins, no extra English, no watermark, no tiny paragraphs, no duplicated labels, visually match the reference.
```

## 提示词编写要求

- 每张图只写本页需要出现的文字，并标记 `Text (verbatim)`。
- 为每页指定一个具体视觉隐喻，避免泛化为“科技感背景”。
- 系列页面重复完整风格规范，不能假设生成器记得上一张。
- 若用户已提供满意成品，把该图作为 `referenced_image_paths` 的风格参考。
