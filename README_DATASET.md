# Shiori 字幕风格迁移数据集

本仓库仅同步数据集及人工处理交接资料，不包含训练代码、模型、训练输出或虚拟环境。

- `ShioriTranscript/crawler_en/`：待处理的原始字幕与元数据。
- `ShioriTranscript/raw/`：完成处理后归档的原始文件，保持字节不变。
- `ShioriTranscript/clean/`：正式清洗结果，JSONL，每条仅含 `raw` 和 `actually`。
- `ShioriTranscript/manual_work/`：草稿、低置信度片段、任务清单、人工审核决定和进度记录。该目录不是正式训练集。
- `ShioriTranscript/一号标准.md`：必须遵守的清洗与中性化标准。

训练映射为 `actually → raw`。raw 保留口语语法、真实重复、迟疑、改口、填充词、脏话和人物表达习惯；actually 中性化表达但不改变原意与说话意图。

## 交接状态（2026-11-02）

接手范围包含原 A、B 两组的所有剩余文件，原分组排他限制已取消。任务清单用于查询历史进度，不再划分当前权限。已归档文件不得重复处理。

### 已完成：`s7C9J7guXaI`

- 257 条草稿均已完成逐条语义决定。
- `clean/s7C9J7guXaI.jsonl`：991 条人工整理配对；每条只有 `raw` 和 `actually` 两个字段，JSONL 结构校验通过。
- `manual_work/s7C9J7guXaI.low_confidence.jsonl`：151 条含低置信度残余的源草稿行，作为人工复核上下文，不进入 SFT。
- 原始 TXT 和 JSON 已从 `crawler_en` 移动至 `raw`。归档前后 Git blob SHA 完全一致，原始字节未变。
- 2484 个原始字幕片段已覆盖；未能可靠恢复的片段没有被编入 clean。

### 下一批：接下来 20 个文件

当前队列从 `3JBmOdbzIt4` 开始。接下来 20 个文件为：

1. `3JBmOdbzIt4`
2. `EN3vJ4WlFww`
3. `7seUd8nr6-8`
4. `mcQ9PXGt38g`
5. `YZYnMPyJDtQ`
6. `Y-_3O6wZI_U`
7. `0XPeLT3nfy0`
8. `Z-VzJibKJqQ`
9. `RyelZGrCxWY`
10. `O7Gg2_1AsPU`
11. `ehbTci8o8NA`
12. `3mMbyik-hho`
13. `cZcDQqw3WO4`
14. `4g9JyWS9YAQ`
15. `E7sBKou_yMA`
16. `h3-50N7Q-rE`
17. `6BfzpTaUfT8`
18. `KdKyQ-JCBac`
19. `lNpOfFG4HlQ`
20. `9zTF9XRtmLU`

这些文件均已核实仍在 `crawler_en`，尚未在 `raw` 或 `clean` 中归档。按顺序逐个处理，单个文件完成语义审核、切分、结构校验和原始文件归档后，才更新为完成。

当前首个文件 `3JBmOdbzIt4` 已完成全文阅读：原始字幕共2428个片段，已整理成133条中间草稿记录，合并文件为 `manual_work/3JBmOdbzIt4.draft.jsonl`。目前已完成第1–80条草稿的人工语义复核和单句切分，暂存320条中间配对；第81–133条仍待处理。未创建 clean，也未移动原始文件。

Python处理辅助脚本不在本次上传范围；不使用自动语言清洗脚本、规则批量改写或外部模型代替人工语义判断。
