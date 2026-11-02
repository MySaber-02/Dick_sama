> 当前范围已更新：请先读取 ShioriTranscript/manual_work/A处理范围.md。用户要求本窗口处理除B组外的全部剩余文件；下方为旧批次历史记录。

# A 组：当前窗口

2026-10-27 重新分配。本窗口分配的 8 个文件均已完成并归档；当前无待办，完成后停止。

## 最后完成的文件

- `C9EK1QSnCos`：已完成 985 条配对并归档；识别残缺上下文另存 manual_work/C9EK1QSnCos.low_confidence.jsonl，其中可确认的子句已单独提取。原始 TXT、JSON 已移动到 raw，完整性核验通过。

`5yLDmZ-Faow`、`4Him-dPaGe4` 已移交 B 组，本窗口不再处理。

## 已完成

- `F2H1iN6hv58`：已完成并归档
- `9WCnRRYFwps`：已完成并归档
- `LHOtqIOLczE`：已完成并归档
- `oEopA7l-q_k`：已完成并归档
- `6nLajpUHa3w`：已完成并归档
- `BJYiTgM7Gy8`：已完成并归档
- `9g4wXCkMn1o`：已完成并归档

## 处理要求

- 先读项目的“一号标准.md”。逐个文件通读，人工逐句处理；不使用自动语言清洗代码或助手分工替代人工判断。
- raw 只修正明确错别字和可靠识别错误，连接不合理的字幕碎片。保留真实重复、迟疑、填充词、改口、语法错误、脏话和原有遮蔽标记，不凭空添加停顿。
- actually 以单句为主、真实邻句上下文辅助，保留原意、指代、说话意图、否定和不确定性。无法可靠理解的片段另存低置信度待核文件，不编造中性表达；能可靠理解的子句可单独人工提取。
- 每条只含 raw、actually 两个字段，JSONL 格式。人工核对结果先存 manual_work/<ID>.reviewed.jsonl。
- 来源为 crawler_en/<ID>.txt 及同名 JSON。完成全文核对后，原始 TXT、JSON 移动到 raw，保持原始字节不变；结果存 clean。

## 并行归档

- 两个窗口必须使用已有归档工具：`python3 ShioriTranscript/manual_work/archive_continuation_reviewed.py <ID>`。
- 工具仅做格式、遮蔽标记、完整性检查、移动和登记，不能代替人工语言处理。已有跨进程文件锁，等待即可，不绕开。
- 不手工修改 manual_continuation_progress.json，不直接移动原件或调用其他归档脚本。
- 只处理本组待办，不操作另一组文件和中间结果，完成后停止。实时状态以中央进度和实际归档文件为准。

## 后续领取提醒

2026-10-27 已另给 B 窗口分配 100 份，见 manual_work/batch100_B_20261027/manifest.json。A 当前没有新任务；以后领取必须排除中央进度中已登记和当前任务分配.json 中预留的文件。
