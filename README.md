# disk-scanner

Windows 磁盘空间扫描 **Agent 技能**：文件夹大小分析、文件类型分布、大文件定位、游戏/清理扫描。

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