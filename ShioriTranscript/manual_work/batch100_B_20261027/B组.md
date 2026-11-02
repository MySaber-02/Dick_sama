# B 组新任务：100 个文件

分配日期：2026-10-27。任务编号：B100-20261027。负责窗口：B。

已排除已完成、已登记、其他批次预留及已有中间结果的文件。原件未复制、未移动，仍在 crawler_en。

共 100 份，分为 10 个小批次，每批 10 份；TXT 合计 6,656,598 字节。以下是分配时的清单，实时状态以中央进度为准。

## 工作标准

- 先读 ShioriTranscript/一号标准.md；本任务是人工逐句清洗和中性配对，不是启动模型训练。
- 逐个文件阅读全文并处理，不用自动语言清洗代码替代人工判断，不启用助手分工。
- raw 只修正明确错别字、可靠的 ASR 错误和文本格式，连接不合理的字幕碎片。保留真实重复、迟疑、填充词、改口、语法错误、脏话及原有遮蔽标记；不凭空添加停顿，不做语言润色。
- actually 单句为主、真实上下文辅助。只改变风格，准确保留意思、说话意图、指代、否定和不确定性；不能把疑问、反问、命令等一律改成陈述，不按外部事实或完整故事改写原意。
- 无法可靠理解的残片保留至 manual_work/<ID>.low_confidence.jsonl 待核，不编造 actually；可靠子句可单独人工提取并记录其来源。待核数量与排除的完整句子数量不要混淆。
- 每条配对只有 raw、actually 两个字段，JSONL 格式；先写 manual_work/<ID>.reviewed.jsonl，再人工核对全文覆盖及语义对应。

## 归档与进度

- 源文件仍在 crawler_en/<ID>.txt、crawler_en/<ID>.json。全部处理并核对后才移动到 raw，原始字节不变；正式配对存 clean。
- 本批已由分配工具登记到 manual_continuation_progress.json，无需再次添加文件。只读中央进度判断是否完成，不能按本清单的初始状态重复处理。
- 统一使用已有归档工具：`python3 ShioriTranscript/manual_work/archive_continuation_reviewed.py <ID>`。工具只做检查、文件操作和登记，不能代替人工语言处理。
- 若确有含原始脏话遮蔽的残片被排除且保留完整原文至待核文件，可使用 `--include-pending-censors`，核对全部原始遮蔽标记在正式配对和待核原文中的总数；不能删除遮蔽或猜写其中内容。
- 归档工具有跨进程锁，等待即可；不绕开锁，不手工改中央进度，不直接移动原件。
- 按 B01—B10 顺序处理，每 10 份是一个进度检查点，不把部分处理或仅通读标记为完成。只处理本批 100 份，完成后停止，不自行领取 A 组或其他文件。
- 只做本窗口所属文件，不覆盖其他窗口的中间结果。历史 batch20_groups 是已完成的旧批次，本批以本目录 manifest.json 为准。

## B01：第 1—10 份

| 顺序 | 文件 ID | TXT 大小（字节） |
| --- | --- | ---: |
| 1 | `BCwy8TXOXjs` | 57,787 |
| 2 | `zhuoz3lrzAA` | 58,186 |
| 3 | `LdIZ6BiQgQE` | 58,478 |
| 4 | `zABLEHgW6mg` | 58,606 |
| 5 | `4aPCtvK_HgI` | 58,634 |
| 6 | `r5LVDqGMum8` | 58,922 |
| 7 | `JIBkEfvDVRo` | 58,960 |
| 8 | `3flK5EtKenk` | 59,085 |
| 9 | `_poW1Y2EWd8` | 59,498 |
| 10 | `xN4ScQHRuCs` | 59,783 |

## B02：第 11—20 份

| 顺序 | 文件 ID | TXT 大小（字节） |
| --- | --- | ---: |
| 11 | `7AQX14oEFK0` | 59,879 |
| 12 | `n3ErwVlICrU` | 60,178 |
| 13 | `o-vPa42nYuY` | 60,435 |
| 14 | `XlHYRrUIIDA` | 60,823 |
| 15 | `e1K6PON6n_E` | 61,025 |
| 16 | `wz26Uwd2xjI` | 61,202 |
| 17 | `LB2__anNj5o` | 61,758 |
| 18 | `LpeIJ5UC9h0` | 61,829 |
| 19 | `L4ACXBql3No` | 62,052 |
| 20 | `UzsoRrmg6Mw` | 62,107 |

## B03：第 21—30 份

| 顺序 | 文件 ID | TXT 大小（字节） |
| --- | --- | ---: |
| 21 | `k-wgzIL9348` | 62,134 |
| 22 | `aM7ysu2s7X0` | 62,262 |
| 23 | `kZE2IcVGRAQ` | 62,313 |
| 24 | `CVrQI_-wnRc` | 62,758 |
| 25 | `MDr4eV4ii2g` | 62,770 |
| 26 | `dTf0g5tqzBU` | 62,797 |
| 27 | `_2wLwo7OXsY` | 62,948 |
| 28 | `h9Ng8PeQ-Qg` | 62,960 |
| 29 | `vG9vdfJJiyY` | 63,005 |
| 30 | `iycEkuK8mjE` | 63,099 |

## B04：第 31—40 份

| 顺序 | 文件 ID | TXT 大小（字节） |
| --- | --- | ---: |
| 31 | `mx35HHWpUjs` | 63,106 |
| 32 | `GzHU0hbbwYY` | 63,554 |
| 33 | `1wCgmK-D04M` | 63,628 |
| 34 | `Y9F_JJiBUZ8` | 63,782 |
| 35 | `y2xUvultGOE` | 64,042 |
| 36 | `lheeLniAvLI` | 64,161 |
| 37 | `v20tKX4gLIg` | 64,208 |
| 38 | `VbUImtn3sLs` | 64,242 |
| 39 | `NZcLZj7sty4` | 64,333 |
| 40 | `yrGLY0yxA0s` | 64,634 |

## B05：第 41—50 份

| 顺序 | 文件 ID | TXT 大小（字节） |
| --- | --- | ---: |
| 41 | `HNpT88tiKLM` | 64,647 |
| 42 | `lc411r2fo-c` | 64,733 |
| 43 | `m73wkwQNl2I` | 65,043 |
| 44 | `EowJuA2nT5o` | 65,486 |
| 45 | `21eDvOhRZ3o` | 65,743 |
| 46 | `wujF26r0KFU` | 65,828 |
| 47 | `9YOmY5bJalM` | 65,870 |
| 48 | `JnRJ0ine5KU` | 65,899 |
| 49 | `sEu1Yj-cICI` | 66,000 |
| 50 | `_PkbayGWyQo` | 66,326 |

## B06：第 51—60 份

| 顺序 | 文件 ID | TXT 大小（字节） |
| --- | --- | ---: |
| 51 | `2pVr-HeNIxc` | 66,477 |
| 52 | `iKTFRrKwFDM` | 66,546 |
| 53 | `wJoJznX5GuU` | 66,588 |
| 54 | `5EdPS2SeIRs` | 66,662 |
| 55 | `MosGttRX15Q` | 66,714 |
| 56 | `vgMkbCbwltc` | 66,820 |
| 57 | `UTbHC4u5XBU` | 67,117 |
| 58 | `UJKvVAMMXEw` | 67,182 |
| 59 | `SkN_v9losxU` | 67,469 |
| 60 | `fLVJWc6jlUY` | 67,485 |

## B07：第 61—70 份

| 顺序 | 文件 ID | TXT 大小（字节） |
| --- | --- | ---: |
| 61 | `HOUkMMMzNZQ` | 67,923 |
| 62 | `fwrMjZF-5Gs` | 68,113 |
| 63 | `R350tbrRFAc` | 68,401 |
| 64 | `3xOyrgufb0M` | 68,443 |
| 65 | `EzP8PoJDKDo` | 68,550 |
| 66 | `7H3S3pyL92o` | 68,754 |
| 67 | `Q32Om1RAa1c` | 68,935 |
| 68 | `dvOBSw4e-No` | 69,221 |
| 69 | `pMiDV5XOrSo` | 69,524 |
| 70 | `GOcKPl4t9mk` | 69,548 |

## B08：第 71—80 份

| 顺序 | 文件 ID | TXT 大小（字节） |
| --- | --- | ---: |
| 71 | `ogkjSMyssbs` | 69,587 |
| 72 | `KSaC99K4IF8` | 70,009 |
| 73 | `plU_vIIQV0M` | 70,525 |
| 74 | `-pwzzYrR4us` | 70,645 |
| 75 | `26-4XEQa5Jk` | 70,696 |
| 76 | `bIldpIXptuQ` | 70,708 |
| 77 | `8Q2A02tRvhM` | 71,419 |
| 78 | `_6wUT7s4668` | 71,656 |
| 79 | `SjpQBxwrME0` | 71,699 |
| 80 | `lR1aOrIrOII` | 71,822 |

## B09：第 81—90 份

| 顺序 | 文件 ID | TXT 大小（字节） |
| --- | --- | ---: |
| 81 | `pBJFZ0QrvvU` | 72,163 |
| 82 | `WoczqZ351oM` | 72,243 |
| 83 | `AbnVeOh24QI` | 72,434 |
| 84 | `zsUX_k9_Baw` | 72,572 |
| 85 | `rDOg_TMxfAg` | 72,973 |
| 86 | `YQaj9oQOfzw` | 72,986 |
| 87 | `_V-F99hL9Zg` | 73,013 |
| 88 | `nFm3B-nurb8` | 73,299 |
| 89 | `52HmisUYz_I` | 73,411 |
| 90 | `NziJqMVv4c0` | 73,458 |

## B10：第 91—100 份

| 顺序 | 文件 ID | TXT 大小（字节） |
| --- | --- | ---: |
| 91 | `DQU38bTURjg` | 73,635 |
| 92 | `IhCq_BlUpII` | 73,716 |
| 93 | `JC65GxRRSto` | 73,722 |
| 94 | `IT1W5ZzuA1I` | 73,824 |
| 95 | `96wFsPtaaIo` | 74,006 |
| 96 | `_PvxTDguq0w` | 74,286 |
| 97 | `9g1UpAQqjg4` | 74,292 |
| 98 | `bgVgVBcsd-U` | 74,389 |
| 99 | `k3rGI1jg9J4` | 74,389 |
| 100 | `ZfYHI3Fy_1Q` | 75,011 |
