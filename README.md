# 自主 AI 研究：autoresearch 深度解析

An interactive single-page course on **autonomous AI research** — how an LLM-driven research loop is actually built, file by file. Self-contained HTML, no framework, no build pipeline beyond `cat`.

中文教程，4 章，从大局观到实验循环：

| # | Module | Topic |
|---|---|---|
| 01 | 大局观：AI 当研究员 | The big-picture vision of LLMs as researchers |
| 02 | 三文件架构 | The three-file architecture |
| 03 | 现代 GPT 解剖 | Anatomy of a modern GPT |
| 04 | 实验循环与扩展 | Experiment loop and scaling out |

## Build

```bash
bash build.sh
```

The script concatenates `_base.html + modules/*.html + _footer.html` into `index.html`. Open `index.html` in any browser.

## Structure

```
_base.html        Shell, nav, fonts, accent variables
_footer.html      Closing tags
modules/*.html    Chapter content, assembled in numeric order
main.js           Scroll progress, nav-dot active states
styles.css        Layout, typography, animations
build.sh          One-line concat
```

Styling: purple accent (`#6D4FC2`), Bricolage Grotesque + DM Sans + JetBrains Mono via [loli.net](https://fonts.loli.net) mirror.

## Deploy

Static. Drop the directory on any host — GitHub Pages, Vercel, S3, anywhere that serves HTML.
