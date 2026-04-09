---
name: elegant-card
description: 生成优雅的双语金句/引言卡片。Use when user asks for "生成卡片", "金句卡片", "引言卡片", "优雅卡片", "quote card", "elegant card" or wants to create a beautiful bilingual quote image.
tags:
  - Skill
  - Card
  - Design
---

# 优雅卡片生成器

生成精美的双语金句/引言卡片，支持自定义字体、配色、导出 PNG/SVG。

## When to Use

- 用户说"生成卡片"、"做一张金句卡片"、"引言卡片"
- 用户想要把一段话做成漂亮的图片
- 用户提到"优雅卡片"、"elegant card"
- 用户需要双语（中英）引言卡片

## Workflow

### Step 1: 收集内容

向用户确认以下信息（可一次性询问，也可根据上下文推断）：

| 字段 | 必填 | 说明 |
|------|------|------|
| 中文引言 | 是 | 卡片主体中文内容 |
| 英文翻译 | 否 | 对应的英文翻译 |
| 署名 | 否 | 出处，如"——荣格《红书》" |
| 底部签名 | 否 | 右下角的小签名，如"Tanch" |

### Step 2: 读取模板

读取模板文件：
```
E:/AI/AAA我自己的小工具/卡片生成器/优雅卡片/generator.html
```

### Step 3: 填充内容并输出

在模板中定位以下默认值，替换为用户提供的内容：

- `chineseText` 的默认值 → 用户的中文引言
- `englishText` 的默认值 → 用户的英文翻译
- `signatureText` 的默认值 → 用户的署名
- `footerSignatureText` 的默认值 → 用户的签名

具体修改位置（在 `<script>` 标签内）：

1. 中文文本输入框的 `value` 属性（约第 247 行的 `<textarea>`）
2. 英文文本输入框的 `value` 属性（约第 256 行的 `<textarea>`）
3. 署名输入框的 `value` 属性（约第 261 行的 `<input>`）
4. 底部签名输入框的 `value` 属性（约第 267 行的 `<input>`）
5. 卡片预览区中的默认文本（约第 203-216 行的 `<div>` 内容）

将修改后的 HTML 写入用户指定路径（默认：当前目录下 `elegant-card.html`）。

### Step 4: 提示用户

告知用户：
1. 双击打开生成的 HTML 文件
2. 在浏览器中可继续调整样式（字体、颜色、大小等）
3. 可切换卡片比例：横版（4:3，适合电脑/横屏）或竖版（9:16，适合手机/竖屏）
4. 点击"保存为PNG"或"保存为SVG"导出图片

## Validation Checklist

- [ ] 中文引言内容已填充
- [ ] HTML 文件已成功写入
- [ ] 告知用户打开方式

## Common Pitfalls

### WRONG
直接创建新 HTML 而不基于模板
```

### CORRECT
基于 generator.html 模板修改内容值
```
