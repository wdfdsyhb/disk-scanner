# disk-scanner · Windows 磁盘空间侦探

[![CI](https://github.com/wdfdsyhb/disk-scanner/actions/workflows/lint.yml/badge.svg)](https://github.com/wdfdsyhb/disk-scanner/actions/workflows/lint.yml) [![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE) ![ZCode Skill](https://img.shields.io/badge/AI-ZCode_Skill-purple)

> 对 agent 说一句「扫描C盘」，它跑 4 个脚本回你：顶层目录大小排名、垃圾文件候选（Temp/缓存/安装残留）、游戏占用定位，最后按白名单安全清理。
>
> English: Ask once and the agent maps your disk — top folder sizes, junk candidates, game installs — then cleans with a whitelist.

## 安装

把 `SKILL.md` 和 `scripts/` 放进你的 AI 编码工具技能目录：

```
~/.zcode/skills/disk-scanner/     # ZCode
```

触发词：`扫描C盘` / `磁盘扫描` / `清理磁盘`

## 能力

| 脚本 | 干什么 |
|---|---|
| `disk_scan` | 顶层目录大小排名，找空间黑洞 |
| `clean_scan` | 垃圾文件候选：Temp、缓存、安装残留 |
| `game_scan` | 游戏目录占用定位 |
| `safe_clean` | 白名单安全清理 |

## 已知限制

NTFS junction 会被 `os.walk` 跟随（`followlinks=False` 挡不住 Windows junction），个别目录计数可能偏高——识别 junction 后手动排除。

## License

MIT

---

## English

Full English documentation: [README_EN.md](README_EN.md)
