# disk-scanner · Windows Disk Space Detective

[![CI](https://github.com/wdfdsyhb/disk-scanner/actions/workflows/lint.yml/badge.svg)](https://github.com/wdfdsyhb/disk-scanner/actions/workflows/lint.yml) [![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE) ![ZCode Skill](https://img.shields.io/badge/AI-ZCode_Skill-purple)

> Ask once and the agent maps your disk — top folder sizes, junk candidates, game installs — then cleans with a whitelist.

## Installation

Put `SKILL.md` and `scripts/` into your AI coding tool's skills directory:

```
~/.zcode/skills/disk-scanner/     # ZCode
```

Trigger words: `扫描C盘` (scan C drive) / `磁盘扫描` (disk scan) / `清理磁盘` (clean disk)

## Capabilities

| Script | What it does |
|---|---|
| `disk_scan` | Ranks top-level folder sizes to find space hogs |
| `clean_scan` | Junk file candidates: Temp, caches, leftover installers |
| `game_scan` | Locates game directory usage |
| `safe_clean` | Whitelist-based safe cleanup |

## Known Limitations

NTFS junctions are followed by `os.walk` (`followlinks=False` does not stop Windows junctions), so a few directory counts may run high — identify junctions and exclude them manually.

## License

MIT

> 🇨🇳 中文文档: [README.md](README.md)
