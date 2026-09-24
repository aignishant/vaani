# Architecture Decision Records — Vaani

One file per structural decision: `ADR-NNNN-<kebab-slug>.md`, numbered from `0001`, **never
renumbered and never rewritten**. A decision that turns out wrong is **superseded** by a later ADR
that says so; the original stays exactly as it was written.

That rule is the whole value. An ADR set you can edit is a set that always looks like it was right
from the start, which teaches nothing. An ADR set you cannot edit records what was known at the
time, which is the only thing that makes the next decision easier.

## When an ADR is required

Write one for anything **structural** — a change to the shape of the work rather than to its
content:

- the day format, the ID scheme, the phase boundaries, the numbering rule
- skipping, merging, reordering or inserting a day (the plan forbids doing this without one)
- adopting, replacing or dropping a tool the whole project depends on
- a change in scope: something the plan promised and no longer will, or the reverse
- a constraint that turned out to be wrong

Do **not** write one for: a version bump (that is `PINS.md`), a wording change (that is
`CHANGELOG_PLAN.md`), or a decision inside a single day (that belongs in the day).

Rule of thumb: **if someone six months from now would ask "why on earth is it like this?", it
needs an ADR.** If they would not notice, it does not.

## The relationship to the changelog

`CHANGELOG_PLAN.md` records **what the plan now says**. An ADR records **why, and what else was
considered**. A structural change gets both, and the changelog entry links the ADR.

## The template

Copy `ADR-0000-template.md`. Every section is required; an ADR with no *Options considered* is a
justification written after the fact, not a decision record.

| # | Title | Date | Status |
| --- | --- | --- | --- |
| [0001](ADR-0001-the-plan-as-adopted.md) | The plan as adopted | 2026-09-18 | accepted |
| [0002](ADR-0002-two-folders-per-day.md) | Every day has two independent folders: speaking and writing | 2026-09-18 | accepted |
| [0003](ADR-0003-days-written-ahead-in-batches.md) | Days are written ahead in batches of up to five, and done one at a time, in order | 2026-09-22 | accepted |
| [0004](ADR-0004-batch-of-ten-from-the-last-written-day.md) | A batch of ten, written from the last written day | 2026-09-22 | accepted |
| [0005](ADR-0005-second-batch-of-ten-and-the-gate-day.md) | A second batch of ten, and how a gate day is written ahead | 2026-09-22 | accepted |
| [0006](ADR-0006-third-batch-and-the-order-rule-faced-directly.md) | A third batch of ten, and the order rule named for what it has become | 2026-09-22 | accepted |
| [0007](ADR-0007-fourth-batch-the-gate-day-and-the-phase-boundary.md) | A fourth batch of ten, carrying the phase 2 gate and crossing into phase 3 | 2026-09-23 | accepted |
| [0008](ADR-0008-fifth-batch-and-the-unfinished-day.md) | A fifth batch of ten, days 47–56, after finishing the day the fourth batch left half-written | 2026-09-23 | accepted |
| [0009](ADR-0009-sixth-batch-of-fourteen-across-the-phase-3-gate.md) | A sixth batch of fourteen, days 57–70, carrying the phase 3 gate and widening the cap once | 2026-09-23 | accepted |
| [0010](ADR-0010-seventh-batch-of-ten-to-the-phase-4-gate.md) | A seventh batch of ten, days 71–80, back at the cap and ending on the phase 4 gate | 2026-09-23 | accepted |
| [0011](ADR-0011-eighth-batch-of-four-opening-phase-5.md) | An eighth batch of four, days 81–84, opening phase 5 | 2026-09-23 | accepted |
| [0012](ADR-0012-ninth-batch-of-seven-after-finishing-the-eighth.md) | Days 82–84 finished under ADR-0011, then a ninth batch of seven, days 85–91 | 2026-09-24 | accepted |
| [0013](ADR-0013-tenth-batch-of-ten-across-the-phase-5-gate.md) | A tenth batch of ten, days 92–101, carrying the phase 5 gate as a rehearsal and opening phase 6 | 2026-09-24 | accepted |
| [0014](ADR-0014-eleventh-batch-of-ten-inside-phase-6.md) | An eleventh batch of ten, days 102–111, inside phase 6 and crossing no gate | 2026-09-24 | accepted |
| [0015](ADR-0015-twelfth-batch-of-two-to-the-proofreading-checklist.md) | A twelfth batch of two, days 112–113, inside phase 6 and crossing no gate | 2026-09-24 | accepted |
