# mcQ9PXGt38g semantic review: original draft rows 151-190

This pass compared every original draft row 151-190 with the corresponding source TXT dialogue. Each edit was applied by the exact original draft row and a checked raw-text prefix to avoid the cross-row `actually` alignment error discovered in the preceding pass. The original source TXT and JSON were not modified.

## Main source-backed decisions

- Rows 151-152: retained the game's virus/cactus discussion as spoken rather than inventing the explanation for the odd ASR phrase; restored "Sounds good", "I can do this", and the tentative "Maybe you are around here" statement.
- Row 153: preserved the questions, the whistle instruction, the competing self-criticisms, and "that's my contribution". "No, you thought secretary" remains LOW because its words cannot be reliably resolved.
- Rows 154-155: preserved the uncertainty about whether a target was dead and whether to shoot again; restored the repeated reassurance and "Wow" rather than compressing different speakers' reactions.
- Row 156: recovered the separate encouragement, "I got Boo", and "Killer Queen" dialogue. The cut-off "they sound so close but I am so" remains LOW.
- Rows 157-158: retained "Those are not the lyrics" and the question about possible shapes. Crucially, the source TXT has "Not on the walls, I don't think. You can fly." The pre-existing staged record had incorrectly fused it as "I don't think you can fly". The staged raw and actually were split to preserve the opposite truth values of the statements.
- Rows 159-161: retained the uncertainty and reactions around finding Giggles; retained the speaker's correction from "starting soon area" to "starting area". "Someone H was just random" remains LOW.
- Rows 162-165: the old staged SFT had skipped this dialogue. Recovered the countdown, inability to hear/see, attempts to locate players, and comments about shooting toilet paper; left "I had one in me", "oh the person this thing", and "you found be at least" in LOW because their referents or ASR words remain uncertain.
- Rows 166-170: recovered the end of the search round and the new Infection-mode explanation, including the conditional "when you die, you become a hunter". The "oh when you" fragment is LOW; the proposed timer is left as a question, not asserted as an agreed setting.
- Rows 171-174: retained both speakers' constraints about revealing locations, switching points of view, seeing other players, and leaving voice chat. The cut-off "your spot knowledge takes anymore" remains LOW. "In fact, you can't see each other" is not rewritten to claim the opposite.
- Rows 175-176: preserved the hunter instruction, the painting questions, the explicit question about repeated shooting, and the judgment that the camouflage is too obvious. The truncated "oh god what a" and "where should I" remain LOW.
- Row 177: salvaged the definite "you got to make that yourself" statement. Kept uncertain ASR phrases involving "Emones", "moved out", and "how do you put... picture on" in LOW; did not guess a name or role from the game mode.
- Rows 178-180: kept the artist/painting conversation, disagreement, win/loss uncertainty, remaining time, and the "sunk cost fallacy" reference without inventing motives.
- Rows 181-186: preserved the Ctrl+Z request, contrast between frustration and hope, self-corrections, and color-picker trouble. The broken "I got to go within" and "it's not do space bar and then" commands remain LOW.
- Rows 187-190: preserved the transition to hunting and the panic reactions. The incomplete "should I get", ambiguous "move coals or" and "move calls", and unexplained "never move over" are LOW rather than fabricated instructions.

## Staging and provenance updates

- Original draft rows reviewed in this pass: 151-190 (40 rows). Original raw fields were preserved; only the corresponding actually values were edited.
- Corrected 36 existing SFT staged records; resegmented three SFT raw entries to restore source-supported speaker boundaries; removed the staged entry containing the unresolved "never move over" phrase.
- Added 58 source-backed SFT entries for dialogue formerly omitted from rows 162-180.
- Added 7 newly identified LOW fragments; corrected 8 existing LOW records whose source_draft_row/draft_row metadata pointed to the wrong draft line.
- Added 58 SFT and 11 LOW coverage-ledger entries (the LOW additions include 4 previously existing LOW records that lacked ledger coverage).
- Current staging after this pass: 1,455 SFT candidates; 175 LOW entries; 254 coverage-ledger records (194 SFT and 60 LOW).
- The staged SFT has 24 exact duplicate raw occurrences retained as potentially genuine repeated speech; no automatic deduplication. No exact SFT/LOW raw overlap, no empty SFT fields or SFT schema errors. Some legacy LOW entries have older optional source-row metadata; they were not assigned invented positions.

## Status

- Completed semantic review: original draft rows 1-190 out of 393.
- Next review range: 191-320.
- All 3,061 source subtitle segments have been read, but complete source-to-SFT/LOW reconciliation is not yet established.
- No final `clean` was created, and no original TXT/JSON was moved from `crawler_en`.
