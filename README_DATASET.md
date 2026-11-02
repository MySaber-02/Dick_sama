# Shiori 字幕风格迁移数据集

本仓库仅同步数据集及人工处理交接资料，不包含训练代码、模型、训练输出或虚拟环境。

- `ShioriTranscript/crawler_en/`：待处理的原始字幕与元数据。
- `ShioriTranscript/raw/`：完成处理后归档的原始文件，保持字节不变。
- `ShioriTranscript/clean/`：正式清洗结果，JSONL，每条仅含 `raw` 和 `actually`。
- `ShioriTranscript/manual_work/`：草稿、低置信度片段、任务清单、人工审核决定和进度记录。该目录不是正式训练集。
- `ShioriTranscript/一号标准.md`：必须遵守的清洗与中性化标准。

训练映射为 `actually → raw`。raw 保留口语语法、真实重复、迟疑、改口、填充词、脏话和人物表达习惯；actually 中性化表达但不改变原意与说话意图。

## 交接状态（2026-11-02）

接手范围包含原 A、B 两组的所有剩余文件，原分组排他限制已取消。任务清单用于查询历史进度，不再划分当前权限。

已归档的数据不要重复处理。当前 `s7C9J7guXaI` 共257条草稿，逐条语义审核决定已覆盖至257；完整审核决定见 `manual_work/s7C9J7guXaI.review_decisions.json`。目前第1–20条已人工切分为66条中间配对，保存在 `manual_work/s7C9J7guXaI.segmented.part01.jsonl`，该文件不是正式训练集。第21–257条仍待切分与终审；LOW及未核实草稿不能进入正式训练集。原始 TXT/JSON 尚未移动。`3JBmOdbzIt4` 尚未开始。

Python处理辅助脚本不在本次上传范围；尚未完成的人工决定已另存为JSON。交接仅记录当前进度，不表示所有历史样本均已按最新标准复核。
