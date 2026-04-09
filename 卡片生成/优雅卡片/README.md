# 优雅卡片生成器

生成精美的双语（中英）金句/引言卡片。

**直接打开 [index.html](index.html) 即可使用，也可作为 [Claude Code](https://claude.ai/code) Skill 使用。**

## 功能

- 双语（中英）引言卡片
- 多种中英文字体可选（汇文明朝体、思源宋体、马善政行草等）
- 自定义文字颜色、背景颜色、字体大小
- 4 种预设配色模板（深蓝金、黑米色、深靛蓝、皇家紫）
- 导出 PNG / SVG
- 导出/导入 JSON 配置

## 使用方式

### 直接打开 HTML

1. 打开 `index.html`
2. 在右侧设置面板编辑内容（中文引言、英文翻译、署名等）
3. 调整字体、配色、大小
4. 点击「保存为 PNG」或「保存为 SVG」导出

### 作为 Claude Code Skill

1. 将本目录下的 `SKILL.md` 复制到 `~/.claude/skills/elegant-card/SKILL.md`
2. 修改 `SKILL.md` 中的模板路径为你实际的 `index.html` 存放位置
3. 在 Claude Code 中输入 `/优雅卡片`，提供引言内容，Claude 会自动生成 HTML 文件

## 字体说明

默认使用**汇文明朝体**（Huiwen-mincho），通过 CDN 自动加载。
- 首次加载需要几秒钟，加载期间显示回退字体（思源宋体）
- 如需本地安装：[GitHub 下载](https://github.com/bosswnx/huiwenmincho-improved)
- 字体授权：免费可商用
