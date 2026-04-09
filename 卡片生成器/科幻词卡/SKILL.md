---
name: scifi-card
description: 生成赛博朋克/科幻风格的引言卡片。Use when user asks for "科幻卡片", "赛博朋克卡片", "词卡", "scifi card", "cyberpunk card", "引用卡片" or wants to create a futuristic quote card.
tags:
  - Skill
  - Card
  - Design
---

# 科幻词卡生成器

生成赛博朋克风格的引言/金句卡片，支持自定义配色、边框、导出 PNG/SVG。

## When to Use

- 用户说"科幻卡片"、"赛博朋克卡片"、"词卡"
- 用户想要制作有科技感的引言图片
- 用户提到"scifi card"、"cyberpunk card"
- 用户想要暗色主题的引用卡片

## Workflow

### Step 1: 收集内容

向用户确认以下信息：

| 字段 | 必填 | 说明 |
|------|------|------|
| 中文引言 | 是 | 卡片主体中文内容 |
| 英文翻译 | 否 | 对应的英文翻译 |
| 角色名 | 否 | 说出这句话的角色，如"Morpheus" |
| 出处 | 否 | 来源信息，如"《黑客帝国》The Matrix, 1999" |
| 签名 | 否 | 右下角花体签名 |

### Step 2: 读取模板

读取模板文件：
```
E:/AI/AAA我自己的小工具/卡片生成器/科幻词卡/generator.html
```

### Step 3: 填充内容并输出

在模板中替换以下默认值：

1. 中文引用输入框的 `value`（约第 264 行的 `<textarea>`）
2. 英文引用输入框的 `value`（约第 267 行的 `<textarea>`）
3. 角色名输入框的 `value`（约第 286 行的 `<input>`）
4. 出处输入框的 `value`（约第 291 行的 `<input>`）
5. 签名输入框的 `value`（约第 296 行的 `<input>`）
6. 卡片预览区的默认文本（约第 202-221 行）

同时更新 `quoteCardData` 对象中的默认值（约第 348-367 行）。

将修改后的 HTML 写入用户指定路径（默认：`scifi-card.html`）。

### Step 4: 提示用户

告知用户：
1. 双击打开生成的 HTML 文件
2. 可调整背景色、边框色、文字色、边框宽度
3. 可切换卡片比例：横版（4:3，适合电脑/横屏）或竖版（9:16，适合手机/竖屏）
4. 点击"导出 PNG"或"导出 SVG"

## Validation Checklist

- [ ] 中文引言内容已填充
- [ ] HTML 文件已成功写入
- [ ] 告知用户打开方式

## Common Pitfalls

### WRONG
修改卡片样式代码结构

### CORRECT
只修改内容值和 quoteCardData 对象中的文本字段
