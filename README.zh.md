# rainman-card

[English](README.md) | 中文

Rainman 的 Claude Code Skill。Fork 自 [@lijigang](https://github.com/lijigang) 的 [ljg-card](https://github.com/lijigang/ljg-skills)。

内容进去，PNG 出来。六种模具，一条命令。

## 模具

| 参数 | 模具 | 尺寸 | 说明 |
|---|---|---|---|
| `-l`（默认） | 长图 | 1080 x auto | 单张阅读卡，内容自动撑高 |
| `-i` | 信息图 | 1080 x auto | 内容驱动的自适应视觉布局 |
| `-m` | 多卡 | 1080 x 1440 | 自动切分为多张阅读卡片 |
| `-v` | 视觉笔记 | 1080 x auto | 手绘风格 sketchnote |
| `-c` | 漫画 | 1080 x auto | 日式黑白漫画 |
| `-w` | 白板 | 1080 x auto | 白板马克笔风格 |

## 安装

```bash
git clone https://github.com/deusyu/rainman-card.git
cp -r rainman-card ~/.claude/skills/rainman-card
cd ~/.claude/skills/rainman-card && npm install playwright && npx playwright install chromium
```

重启 Claude Code 生效。

## 使用

```
/rainman-card -i 这段内容做成信息图
```
```
/rainman-card -l 这篇文章做成长图
```

支持粘贴文本、URL、文件路径，自动获取内容。

## 产出

所有卡片保存至 `~/Downloads/`，PNG 格式。

## 与 ljg-card 的区别

仅改了品牌相关内容：头像、默认署名（`Rainman @deusyu`）、模板路径。六种模具、品味准则、设计体系完全保留原版。

## 致谢

原版 skill 由 [@lijigang](https://github.com/lijigang) 设计和开发。设计体系、品味准则和六模具架构均为其原创。本 fork 仅修改了品牌和路径。

## 许可

[MIT](./LICENSE)
