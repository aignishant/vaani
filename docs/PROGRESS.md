# Progress ledger — Vaani

Append-only. **The last row is where we actually are.** One row per *completed* day, pasted from
that day's hub §11 before `python granth.py done N` will commit. A day with no row here is not
finished, whatever the folder looks like.

Nothing is ever deleted from this table. A day that went wrong gets a note under it saying what
went wrong — a ledger that only records successes is a ledger nobody can learn from.

| Day | Date | IDs closed | Parts | Commit | Gates green? |
| --- | ---- | ---------- | ----- | ------ | ------------ |
| 1 | 2026-09-22 | SND-01, WRT-01 | 6 | the `done 1` commit of 2026-09-22 | yes |
