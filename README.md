# Handy Tools

一些好用的小工具，直接浏览器打开即用，无需安装。

## 工具分类

### [卡片生成](卡片生成/)

各类卡片/图片生成工具。

| 工具 | 说明 |
|------|------|
| [优雅卡片](卡片生成/优雅卡片/) | 双语金句/引言卡片，多种字体和配色 |
| [科幻词卡](卡片生成/科幻词卡/) | 赛博朋克风格引言卡片 |
| [英语单词卡](卡片生成/英语单词卡/) | 英语单词学习卡片 |

## 使用方式

### 方式一：直接打开 HTML

所有工具都是单个 HTML 文件，双击即可在浏览器中打开使用。
无需安装任何依赖，无需服务器，无需注册账号。

### 方式二：Claude Code Skill

每个工具都附带 `SKILL.md`，可以作为 [Claude Code](https://claude.ai/code) 的 Skill 使用，让 AI 帮你填充内容并生成 HTML 文件。

**安装方法：**

将对应工具目录下的 `SKILL.md` 复制到你的 Claude Code skills 目录：

```
~/.claude/skills/elegant-card/SKILL.md
~/.claude/skills/scifi-card/SKILL.md
~/.claude/skills/vocab-card/SKILL.md
```

**使用方法：**

在 Claude Code 中输入 `/优雅卡片`、`/科幻词卡` 或 `/英语单词卡`，然后提供你想做成卡片的内容，Claude 会自动生成 HTML 文件。

> **注意：** Skill 中的模板路径需要根据你的实际存放位置修改 `SKILL.md` 中的路径引用。

## 技术栈

- 纯前端 HTML/CSS/JavaScript
- [Tailwind CSS](https://tailwindcss.com/)（CDN）
- [html2canvas](https://html2canvas.hertzen.com/)（导出 PNG）
- [Google Fonts](https://fonts.google.com/)（在线字体）

## License

MIT
