# mcQ9PXGt38g semantic review: draft rows 1-35

Reviewed each of draft rows 1-35 against the corresponding source transcript segments. This is a manual semantic review, not proof of complete source-segment coverage.

## Source-backed edits made
- Row 1: corrected the unsupported reinterpretation "has crabs" to the literal source phrase "the hat crabs"; retained the repeated "Hey".
- Row 21: restored the omitted utterances "Oh, jeez. Oh, back." in actually.
- Row 19: moved to LOW because "big bow" may be a name or ASR error and cannot be resolved from transcript text alone.
- Row 25: moved to LOW; "perhaps diagonal" was an unsupported completion of an incomplete phrase.
- Row 32: moved to LOW; "pay" may be "paint" in the game context, but transcript-only evidence is insufficient to silently correct it.
- Row 35: moved to LOW because the middle phrase "she's a blog" is unclear and the current actually omitted material.

## Other observations
- Row 15 and row 16 remain LOW; the source fragments do not support a reliable reconstruction.
- Row 10 retains the meaningful repeated "first time" in raw; actually may normalize the repetition.
- Row 22 preserves the short repeated wait sequence in raw; actually may compress it without changing the urgency.
- Rows 28-30 retain the paint/brush discussion without guessing at game mechanics.
- No short utterance was deduplicated. Repeated source speech is not treated as subtitle-system duplication without timestamp evidence.

## Status
- Draft rows reviewed: 1-35.
- SFT candidates corrected in-place only where supported.
- Ambiguous rows are marked LOW and must not enter clean.
- Next semantic review range: 36-320.
- Formal clean creation and original-file archival remain blocked until all review and source-coverage reconciliation are complete.


## 后续校正（2026-11-03）

在复核后续上下文及源字幕话轮边界后，修正了早期初审中的两项保守处理：
- 第19行不再整体视为LOW；将可确认的 `Roblox` 和重复问句 `Are we starting?` 拆为SFT，仅将无法确认的 `big bow` 保留为LOW。
- 第25行保留为有上下文支撑的省略表达 `Like a diagonal.`，不再标为LOW，也不改写为推测性的 `Perhaps diagonal.`。

第32行 `how do you pay` 仍为LOW；第35行中的 `oh she's a blog` 仍为LOW。
