# Autonomous AI Research: A Deep Dive into autoresearch

An interactive single-page course on **autonomous AI research** — how an LLM-driven research loop is actually built, file by file. Self-contained HTML, no framework, no build pipeline beyond `cat`.

Four modules, from the big-picture vision down to the experiment loop:

| # | Module | Topic |
|---|---|---|
| 01 | The Big Picture: AI as Researcher | The big-picture vision of LLMs as researchers |
| 02 | Three-File Architecture | The three-file architecture |
| 03 | Anatomy of a Modern GPT | Anatomy of a modern GPT |
| 04 | Experiment Loop and Scaling Out | Experiment loop and scaling out |

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
