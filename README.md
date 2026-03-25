# rainman-card

English | [中文](README.zh.md)

Claude Code Skill by Rainman. Forked from [ljg-card](https://github.com/lijigang/ljg-skills) by [@lijigang](https://github.com/lijigang).

Content in, PNG out. Six molds, one command.

## Molds

| Flag | Mold | Size | Description |
|---|---|---|---|
| `-l` (default) | Long card | 1080 x auto | Single reading card, auto-height |
| `-i` | Infograph | 1080 x auto | Content-driven adaptive visual layout |
| `-m` | Multi-card | 1080 x 1440 | Auto-split into multiple reading cards |
| `-v` | Sketchnote | 1080 x auto | Hand-drawn style visual note |
| `-c` | Comic | 1080 x auto | Manga-style B&W comic |
| `-w` | Whiteboard | 1080 x auto | Marker-style board layout |

## Installation

### Option 1: Manual

```bash
git clone https://github.com/deusyu/rainman-card.git
cp -r rainman-card ~/.claude/skills/rainman-card
cd ~/.claude/skills/rainman-card && npm install playwright && npx playwright install chromium
```

### Option 2: Symlink

```bash
git clone https://github.com/deusyu/rainman-card.git ~/path/to/rainman-card
ln -s ~/path/to/rainman-card ~/.claude/skills/rainman-card
cd ~/.claude/skills/rainman-card && npm install playwright && npx playwright install chromium
```

Restart Claude Code after installation.

## Usage

```
/rainman-card -i 这段内容做成信息图
```
```
/rainman-card -l 这篇文章做成长图
```
```
/rainman-card -v 这个概念做成视觉笔记
```
```
/rainman-card -c 这个故事画成漫画
```

You can also paste text, provide a URL, or give a file path — the skill will fetch and process the content automatically.

## Output

All cards are saved to `~/Downloads/` as PNG files.

## Design Philosophy

Every card follows a strict anti-AI-slop taste guideline:

- No Inter font
- No pure black (`#000000`)
- No three-equal-column cards
- No centered hero layouts
- No AI buzzwords ("empower", "seamless", "unleash")
- No fake data (`99.99%`, `John Doe`)
- Color-matched shadows, not grey defaults
- Max/min element ratio ≥ 10:1
- Mobile-readable: body ≥ 36px, annotations ≥ 24px

## What Changed from ljg-card

- Logo/avatar: replaced with Rainman's
- Default signature: `Rainman @deusyu`
- All template paths updated to `~/.claude/skills/rainman-card/`
- Everything else preserved — same molds, same taste guidelines, same quality

## Credits

Original skill by [@lijigang](https://github.com/lijigang). The design system, taste guidelines, and six-mold architecture are entirely his work. This fork only changes branding and paths.

## License

[MIT](./LICENSE)
