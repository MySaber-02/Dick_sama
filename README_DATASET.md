# Shiori 字幕风格迁移数据集

本仓库仅同步数据集及人工处理交接资料，不包含训练代码、模型、训练输出或虚拟环境。

- `ShioriTranscript/crawler_en/`：待处理的原始字幕与元数据。
- `ShioriTranscript/raw/`：完成处理后归档的原始文件，保持字节不变。
- `ShioriTranscript/clean/`：正式清洗结果，JSONL，每条仅含 `raw` 和 `actually`。
- `ShioriTranscript/manual_work/`：草稿、低置信度片段、任务清单、人工审核决定和进度记录。该目录不是正式训练集。
- `ShioriTranscript/一号标准.md`：必须遵守的清洗与中性化标准。

训练映射为 `actually → raw`。raw 保留口语语法、真实重复、迟疑、改口、填充词、脏话和人物表达习惯；actually 中性化表达但不改变原意与说话意图。

## 交接状态（2026-11-03）

接手范围包含原 A、B 两组的所有剩余文件，原分组排他限制已取消。任务清单用于查询历史进度，不再划分当前权限。已归档文件不得重复处理。

### 已完成：`s7C9J7guXaI`

- 257 条草稿均已完成逐条语义决定。
- `clean/s7C9J7guXaI.jsonl`：991 条人工整理配对；每条只有 `raw` 和 `actually` 两个字段，JSONL 结构校验通过。
- `manual_work/s7C9J7guXaI.low_confidence.jsonl`：151 条含低置信度残余的源草稿行，作为人工复核上下文，不进入 SFT。
- 原始 TXT 和 JSON 已从 `crawler_en` 移动至 `raw`。归档前后 Git blob SHA 完全一致，原始字节未变。
- 2484 个原始字幕片段已覆盖；未能可靠恢复的片段没有被编入 clean。

### 已完成：`3JBmOdbzIt4`

- 原始字幕全文共2428个片段，已阅读；133条草稿均已完成语义复核与切分。
- `clean/3JBmOdbzIt4.jsonl`：1220条人工整理配对；每条仅含 `raw` 和 `actually`，JSONL结构校验通过，完全相同的raw重复数为0。
- `manual_work/3JBmOdbzIt4.low_confidence.jsonl`：90条低置信度片段，单独保留，不进入SFT。
- 原始TXT/JSON已从 `crawler_en` 移动至 `raw`；归档前后Git blob SHA完全一致，原始字节未变。
- 全文已阅读、133条草稿覆盖已核对；但未建立2428个ASR片段逐一映射至clean/LOW记录的机器可验证索引，因此不宣称逐片段覆盖证明。

### 下一批：接下来 20 个文件

当前队列从 `EN3vJ4WlFww` 开始。接下来20个文件为：

1. `EN3vJ4WlFww`
2. `7seUd8nr6-8`
3. `mcQ9PXGt38g`
4. `YZYnMPyJDtQ`
5. `Y-_3O6wZI_U`
6. `0XPeLT3nfy0`
7. `Z-VzJibKJqQ`
8. `RyelZGrCxWY`
9. `O7Gg2_1AsPU`
10. `ehbTci8o8NA`
11. `3mMbyik-hho`
12. `cZcDQqw3WO4`
13. `4g9JyWS9YAQ`
14. `E7sBKou_yMA`
15. `h3-50N7Q-rE`
16. `6BfzpTaUfT8`
17. `KdKyQ-JCBac`
18. `lNpOfFG4HlQ`
19. `9zTF9XRtmLU`
20. `5HJGBZ8OxzA`

以下列表记录本批次处理顺序，实时状态以 `ShioriTranscript/manual_work/batch_10.checkpoint.json` 为准。单个文件完成语义审核、切分、结构校验和原始文件归档后，才更新为完成。

### 当前处理：`mcQ9PXGt38g`（2026-11-03）

- 原始字幕共3061个片段，全文已阅读；完整来源到SFT/LOW的逐段核对仍未完成。
- 原始草稿393条；第1～190条已完成人工语义复核。草稿文件另含13条来源覆盖补充记录。
- `manual_work/mcQ9PXGt38g.segmented.jsonl`：1455条SFT候选，结构校验通过。
- `manual_work/mcQ9PXGt38g.low_confidence.jsonl`：175条LOW记录，不进入SFT。
- `manual_work/mcQ9PXGt38g.coverage_supplements.jsonl`：254条覆盖记录，其中194条SFT、60条LOW。
- 保留24处完全相同的raw重复出现，不自动去重；草稿另有1处完全相同raw重复，也暂时保留。SFT与LOW之间无完全相同raw重叠。
- 第151～190条已经重新逐行对照源字幕复核，纠正了此前的错行风险，并恢复162～180行遗漏的58条句子级SFT候选；复核记录见 `manual_work/mcQ9PXGt38g.semantic_review_151-190.md`。
- 下一步从原始草稿第191条继续复核。尚未创建clean，原始TXT/JSON仍在`crawler_en`，未归档。

Python处理辅助脚本不在本次上传范围；不使用自动语言清洗脚本、规则批量改写或外部模型代替人工语义判断。
