---
name: vocab-card
description: 生成英语单词学习卡片。Use when user asks for "单词卡片", "英语卡片", "生词卡", "词汇卡片", "vocab card", "vocabulary card", "flashcard" or wants to create English word learning cards.
tags:
  - Skill
  - Card
  - Education
---

# 英语单词卡片生成器

生成精美的英语单词学习卡片，支持音标、释义、例句，可导出 PNG。

## When to Use

- 用户说"单词卡片"、"生词卡"、"英语卡片"
- 用户想要制作单词学习素材
- 用户提到"vocab card"、"flashcard"、"vocabulary card"
- 用户有一批生词需要做成卡片

## Workflow

### Step 1: 收集内容

向用户确认以下信息：

| 字段 | 必填 | 说明 |
|------|------|------|
| 英文单词 | 是 | 单词本身 |
| 音标 | 否 | 如 /fəˈnetɪk/ |
| 英英释义 | 否 | 单词的英文定义 |
| 例句 | 否 | 展示用法的例句 |

支持批量生成——用户可提供多个单词，逐一生成卡片。

### Step 2: 读取模板

读取模板文件：
```
E:/AI/AAA我自己的小工具/卡片生成器/英语单词卡/generator.html
```

### Step 3: 填充内容并输出

在模板中替换默认值：

1. 单词输入框的 `placeholder` 或 `value`（约第 220 行的 `<input>`）
2. 音标输入框（约第 221 行）
3. 释义输入框（约第 222 行的 `<textarea>`）
4. 例句输入框（约第 223 行的 `<textarea>`）

将修改后的 HTML 写入用户指定路径（默认：`vocab-card.html`）。

### Step 4: 提示用户

告知用户：
1. 双击打开 HTML 文件
2. 选择卡片主题色（经典白底 / 深蓝金字 / 复古棕黄 / 薄荷炭黑）
3. 可选择卡片比例：横版（4:3，适合电脑）或竖版（9:16，适合手机）
4. 点击"生成卡片"预览，再点击"下载卡片"导出 PNG

## Validation Checklist

- [ ] 单词内容已填充
- [ ] HTML 文件已成功写入
- [ ] 告知用户需点击"生成卡片"按钮才能预览

## Common Pitfalls

### WRONG
跳过"生成卡片"按钮，以为打开就能看到卡片

### CORRECT
告知用户：打开 HTML 后需要点击"生成卡片"按钮，然后才能下载
