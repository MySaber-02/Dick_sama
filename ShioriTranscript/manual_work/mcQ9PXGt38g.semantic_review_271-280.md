# mcQ9PXGt38g: source-backed semantic review, draft rows 271-280

Compared original draft rows 271-280 to raw JSON transcript segments **1938-2005** on 2026-11-04. This is a partial source-backed review, **not** a proof of full 3061-segment coverage.

## Decisions

- Row 270: source segment 1936 displays a profanity mask `[ __ ]`. Reverted the unsupported expansion `oh shit` to `oh [__]` in the draft and staged raw.
- Rows 271-272: segment 1947 ends `10 9 8` and segment 1948 begins `seven six`. Corrected the cross-row contamination of actually and split the fused staged record. Recovered the missing countdown, `check from angle`, `three`, `uh`, and `okay`. Segment 1954 `it I'm so` remains LOW; its earlier source_draft_row=251 was incorrect and is now **272**.
- Row 273: restored `You better hope`, both `One second` utterances, `Down` and `I think you can`. Moved the uncertain `this color was it` from SFT to LOW.
- Row 274: rescued the color and cooking dialogue from segments 1960-1968. `so once again` and `time for that` remain LOW.
- Row 275: changed `nag` to source-supported `neg` without guessing a proper name. `neg`, `naggie`, and `fight` (which might have been `find`) remain LOW. Preserved the ensuing `I'd be happy / No, I would feel bad for her` self-correction.
- Row 276: recovered the comments, reactions, and repeated `Uh-oh` from segments 1974-1981. Ambiguous `wish we would hide` remains LOW.
- Row 277: recovered the separate `Welcome to Osaka`, `Hi`, `Uh, yeah`, `Yes. Yes.` and the qualification `a little`. The unclear source `Osaka got to be more` stays LOW.
- Row 278: kept the preface `Um` and `You know, if you hear the phrase order...` source text without substituting an unsupported Osaka expression.
- Row 279: salvaged the assessment, headband explanation and `Yes`; retained three ambiguous or incomplete portions in LOW.
- Row 280: saved repeated `I get it`, the distinct `I understand / I understood` correction, and the assignment comment. The missing-subject tour-guide utterance remains LOW.

## Resulting staging

- Added **26** source-backed SFT utterances, allowing identical raw utterances only when they are distinct real occurrences (e.g. `Yes.`).
- Evaluated **13** LOW decisions: **12** new LOW records and **1** reassigned existing record (`it I'm so`).
- Staging: **1646** SFT candidates, **209** LOW records, **552** supplement ledger rows (431 SFT and 121 LOW).
- SFT schema: every record contains only nonempty `raw`/`actually`; exact SFT/LOW raw overlap: **0**. Exact duplicate SFT raw occurrence count: **51**, preserved pending source review.

## Remaining

- The 2026-11-04 commit for original draft rows **251-270** only edited draft actually values; it did not complete SFT/LOW source-ledger reconciliation.
- Next draft range: **281-320**, followed by **321-393**.
- Full 3061-source-segment reconciliation, formal clean creation and source TXT/JSON archival **remain pending**.
