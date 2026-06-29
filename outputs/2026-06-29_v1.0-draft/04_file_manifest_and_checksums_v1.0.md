# 文件清单与校验记录 V1.0

| 项目 | 内容 |
|---|---|
| 文档包 | `outputs/2026-06-29_v1.0-draft` |
| 校验日期 | 2026-06-29 |
| 校验算法 | SHA256 |
| 用途 | 判断文件是否被改动，支持版本基线和回退 |

## 1. 文件校验清单

| 文件 | 行数 | 字节数 | SHA256 |
|---|---:|---:|---|
| `00_version-control-and-rollback.md` | 156 | 5650 | `7E1B4422E49F40883827B82D8C2214027D4B8BB00B057F06DA55D2AFE218306C` |
| `01_hardware_rd_design_spec_outline_v1.0.md` | 408 | 12779 | `36499B2D137E0EF81BB2D6D48536707303A276C6D5CD8EB10DA35BFAFA5C8E1A` |
| `02_ipd_stage_input_output_matrix_v1.0.md` | 162 | 15040 | `4F3CD36E5989D812A0DEEDDC9CAC849F2B8CB40EBD7664CCF8348CC766F9A37A` |
| `03_hardware_rd_review_gates_and_exit_criteria_v1.0.md` | 410 | 15370 | `177BB5EE0D5BCCC824A91F5CB89E45E485B4DBF653683085A033CF77DEE95DA1` |
| `_source_snapshot/hardware-rd-design-spec-communication.filled.2026-06-29.md` | 505 | 14083 | `FA32300F159ED0FDC27A34B052FE0B458D0E0284F4E003A5E47B543E9718A818` |

## 2. 校验方法

在 PowerShell 中可执行：

```powershell
Get-FileHash -LiteralPath ".\outputs\2026-06-29_v1.0-draft\01_hardware_rd_design_spec_outline_v1.0.md" -Algorithm SHA256
```

如果输出的哈希值与本清单一致，表示文件内容与 V1.0 草案基线一致。

## 3. 变更后的处理规则

- 如果需要修改文件，建议复制当前目录为新版本目录后修改。
- 如果只做小范围修订，可生成 `v1.0.1` 版本并更新本清单。
- 如果哈希不一致但未记录变更，应先确认是否存在人工修改，再决定保留、回退或形成新版本。

