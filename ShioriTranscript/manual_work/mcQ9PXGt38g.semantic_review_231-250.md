# mcQ9PXGt38g semantic review: draft rows 231-250

Compared original draft rows 231-250 with the source TXT. Updated all 20 corresponding `actually` fields and repaired the SFT/LOW segmentation and coverage ledger.

## Main corrections

- Row 231: restored the repeated "Who says?" question and the short "Yeah" / "Wait, hold on" turns. Kept the unclear "level two little bed" and the cut-off "Did I" in LOW.
- Row 232: recovered "Indo Country", the repeated "Okay", and "I promise you". Kept "herself as a jor" and "going to promise" unresolved rather than guessing the name or missing subject.
- Row 233: separated "It's my turn", the repeated "Meadows", "Let's go", and "Hide". Kept "It's my..." and "Want to be a hidden..." in LOW.
- Row 234: restored "That looks funny", "Your time", and the one-legged-thing question. Kept the truncated "That looks..." and unclear "doesn't feel like... with that" phrase in LOW.
- Row 235: restored both repetitions of "Give up on this idea", "You're not doing it", and the omitted "We have a lot of time" reaction. Kept "Get out of here spot" unresolved.
- Row 236: restored "It's nice during hiding time" and "Nope"; retained the incomplete "You could become a little..." and "Not that other..." in LOW.
- Row 237: restored "Please" and the repeated "How do I..." question. Kept "I'm going to..." in LOW.
- Row 238: preserved "Do you think I could be good like this?", "It could be", and the incomplete "I'm just not the right..." without inventing "position".
- Row 239: retained "I know" before "That's too metallic". The fragments "I'm trying to..." and "then believe" remain LOW.
- Rows 240-241: added previously missing reactions, including "I'm boring", the repeated "No", the angle discussion, "One second", "Hold on", and "Use little details". The unfinished "Spin your..." remains LOW.
- Row 242: preserved both "I so cooked" and "I'm so cooked" separately; the malformed first phrase and unfinished "I mean it seems like it already..." remain LOW.
- Rows 243-244: restored both "Spin around" repetitions, the repeated "Why am I..." question, and all three front-view instructions. The final "So..." remains LOW.
- Rows 245-247: restored repeated "Don't try anything funny", both camera warnings, the repeated "Keep busing" phrase in LOW, the repeated "It's whatever", and the repeated "Closer" instructions.
- Row 248: restored "I really don't know how", both "Why?" reactions, and "Give me the lighter color".
- Row 249: restored the repeated pleas, "There we go", both "No" reactions, and all four "Stay away" utterances.
- Row 250: restored "There's a lot of... a lot of hunters" and retained the term "ruffies" without changing it to a guessed name. The trailing "there's really just a lot of..." and "But..." remain LOW.

## Staging changes

- Reviewed draft rows 231-250 and updated 20 `actually` fields.
- Replaced 46 previously staged records for rows 231-239 with 138 source-aligned sentence-level SFT records for rows 231-250.
- Added 15 LOW fragments; corrected earlier LOW source-row metadata and removed "indo country" from LOW after recovering it as SFT.
- Reconciled SFT and LOW coverage-ledger entries for rows 191-250.
- Current staging: 1620 SFT, 197 LOW, 513 coverage-ledger entries (405 SFT / 108 LOW). No exact SFT/LOW raw overlap; SFT schema checks pass.

## Status

- Original draft rows reviewed: 1-250 of 393.
- Next review range: 251-320.
- Full reconciliation of all 3,061 source subtitle segments remains pending.
- No formal clean was created; original TXT/JSON remain in `crawler_en`.
