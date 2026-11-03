# mcQ9PXGt38g semantic review: draft rows 191-230

Rows 191-230 were compared with the original source TXT. The corresponding draft `actually` fields were reviewed and updated by original row number; source TXT and JSON were left unchanged.

## Decisions
- Restored repeated questions, repeated evaluations, acknowledgements, and speaker reactions that earlier segmentation had compressed.
- Preserved uncertainty, questions, conditions, and self-corrections rather than turning them into confident statements.
- Split recoverable utterances from incomplete ASR fragments and retained unresolved phrases in LOW where their meaning could not be verified.
- Corrected the repeated negative response count in row 222 to match the source.
- Recovered omitted sentence-level SFT material from rows 203-215 and 217-230.
- Kept unclear name/location phrases and incomplete UI/gameplay instructions unresolved; no unsupported names, locations, or actions were inferred.

## Staging snapshot
- Draft rows reviewed: 191-230.
- Segmented SFT: 1,528 records.
- LOW: 183 records.
- Coverage ledger: 342 records (267 SFT, 75 LOW).
- Exact repeated raw occurrences in SFT: 26; no automatic deduplication.
- No exact SFT/LOW raw overlap; SFT schema validation passes.
- Every SFT coverage-ledger pair matches a staged SFT record. Four LOW ledger records still have reason-text mismatches, and some LOW entries from this range are not yet represented in the supplement ledger.

## Status
- Original draft rows reviewed: 1-230 of 393.
- Next review range: 231-320.
- Full source-to-SFT/LOW reconciliation remains pending.
- No formal clean was created; original TXT/JSON remain in `crawler_en`.
