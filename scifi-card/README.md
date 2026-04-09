# 科幻词卡生成器

生成赛博朋克风格的引言/金句卡片。

**直接打开 [index.html](index.html) 即可使用，也可作为 [Claude Code](https://claude.ai/code) Skill 使用。**

## 功能

- 赛博朋克暗色主题
- 双语（中英）引言展示
- 自定义背景色、边框色、文字色、边框宽度
- 多种英文字体可选
- 导出 PNG / SVG
- JSON 导入/导出

## 使用方式

### 直接打开 HTML

1. 打开 `index.html`
2. 在设置面板编辑引言内容、角色名、出处、签名
3. 调整背景色、边框、文字颜色等样式
4. 点击「导出 PNG」或「导出 SVG」

### 作为 Claude Code Skill

1. 将本目录下的 `SKILL.md` 复制到 `~/.claude/skills/scifi-card/SKILL.md`
2. 修改 `SKILL.md` 中的模板路径为你实际的 `index.html` 存放位置
3. 在 Claude Code 中输入 `/科幻词卡`，提供引言内容，Claude 会自动生成 HTML 文件
