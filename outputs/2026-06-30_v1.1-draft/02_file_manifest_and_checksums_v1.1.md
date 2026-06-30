# 文件清单与校验记录 V1.1

| 项目 | 内容 |
|---|---|
| 文档包 | `outputs/2026-06-30_v1.1-draft` |
| 校验日期 | 2026-06-30 |
| 校验算法 | SHA256 |
| 用途 | 判断文件是否被改动，支持版本基线和回退 |

## 1. 文件校验清单

| 文件 | 行数 | 字节数 | SHA256 |
|---|---:|---:|---|
| `00_revision-notes_v1.1.md` | 46 | 2234 | `78D35DF0409391DD8560A2201F4C0C4AD13B6CA63201201D7FBB09CF03716EB6` |
| `01_hardware_rd_design_spec_outline_v1.1.md` | 680 | 26926 | `62C35C2E000207127DB1B0D7A2DBB28869BF9925C89238E4AC659580945216AF` |
| `_source_reference/01_hardware_rd_design_spec_outline_v1.0.reference.md` | 408 | 12779 | `36499B2D137E0EF81BB2D6D48536707303A276C6D5CD8EB10DA35BFAFA5C8E1A` |

## 2. 校验方法

在 PowerShell 中可执行：

```powershell
Get-FileHash -LiteralPath ".\outputs\2026-06-30_v1.1-draft\01_hardware_rd_design_spec_outline_v1.1.md" -Algorithm SHA256
```

如果输出的哈希值与本清单一致，表示文件内容与 V1.1 草案基线一致。

## 3. 回退说明

- 如需回退到 V1.0，可使用 `_source_reference/01_hardware_rd_design_spec_outline_v1.0.reference.md`。
- 如需继续修订，建议新建 `v1.2-draft` 或 `v1.1.1-draft`，不要覆盖本版本。

