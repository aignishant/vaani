# ADR-0012 — Days 82–84 are finished under ADR-0011, then a ninth batch of seven, days 85–91

- **Date:** 2026-09-24
- **Day:** between days 1 and 2 (days 2–81 written, none done)
- **Phase:** 5
- **Status:** accepted
- **Amends:** v1.9.0 → v1.10.0, §9 (the writing-ahead rule), §13
- **Related:** ADR-0003, ADR-0004, ADR-0005, ADR-0006, ADR-0007, ADR-0008, ADR-0009, ADR-0010, ADR-0011

## Context

ADR-0011 authorised days 81–84 and closed with a sentence that binds this one:

> Day 85 onward needs either a closed day 6 in `docs/PROGRESS.md` or a further ADR, and the
> question is asked out loud again first.

The learner asked for "next 10 days doc". Four facts were true at that moment.

**The ledger has not moved.** `docs/PROGRESS.md` still holds one row, day 1.
`python granth.py brief 72` exits non-zero with "day 2 is next".

**The eighth batch is not whole.** Day 81 is fully written and passes `depth`. Days 82, 83 and 84
have their folders but not a single file. On 2026-09-24, before anything was written,
`python granth.py check` passed the depth contract on all 81 written days. It failed only because
the generated indexes were stale, and `python granth.py index` fixes that. §9 says that *a batch is
only started when the batch before it is whole*, and that an unfinished day from an earlier batch
is finished first, under that batch's ADR, and never counts toward the new batch (ADR-0008). So
days 82–84 are ADR-0011's to finish, not this ADR's.

**The question was asked first.** The §9 question was put to the learner before anything was
written, in the words §9 requires: *is anybody doing the days?* It said that days 82–84 are
unfinished and come first. It came with four options: write nothing and close days; finish only
82–84; finish 82–84 and write 85–91, ten day documents in all; or finish 82–84 and write 85–94,
a new batch at the cap of ten. **The learner chose 82–91: ten day documents in all.**

**Seven days from day 85 crosses no gate.** The phase 5 gate is day 100. Days 85–91 are the
middle of phase 5: sounding confident, the complaint, the meeting, the status update, the opening
and closing of a talk, explaining a chart, and stress in long words with the passive.

One more thing is recorded because it is true. Days 71–81 are in the working tree and not in a
commit. ADR-0011 already said the commit was owed. It is still owed, and it now covers days 71–91.

## Decision

**Days 82–84 are finished under ADR-0011, exactly as it authorised them.** They don't count toward
this batch.

**A ninth batch of seven days, 85–91, is written ahead from the last written day**, once day 84 is
whole. It is under the cap of ten. The learner's count of ten is the number of day documents
written in this sitting, not the size of the batch. That keeps the ADR-0008 rule intact: a batch
never absorbs another batch's unfinished days.

Every condition set by ADR-0004 to ADR-0011 still applies. Every day between the last closed day
and the last written day is fully written and passes `depth`. Days are still *done* one at a time,
in order, each with its own `done N` and its own commit. `docs/ERRORS.md` is read before each
`done N`, and a day whose failure parts miss the real pattern is amended first.

**What is kept, because it is the part still doing the work:**

- **The batch closes at its last day.** Day 92 onward needs either a closed day 6 in
  `docs/PROGRESS.md` or a further ADR, and the question is asked out loud again first.
- **Every written-ahead part says, in the part, that its wrong version is a common beginner error
  and not this learner's.**
- **Every written-ahead day's hub and `CHECKLIST.md` carry the tickable `ERRORS.md` re-read**
  before `done N`.
- **The formal-writing choice from ADR-0011 stands.** Formal pages in days 86, 88 and 91 leave out
  contractions as this course's choice and say so where it matters.

## Options considered

| Option | Why not |
| --- | --- |
| **Write nothing new; close days** | Offered, and declined. It is still the option that protects the curriculum from being shaped by errors that have not happened. |
| **Finish only 82–84** | Offered, and declined. It would have written less than the learner asked for. |
| **Finish 82–84 and write 85–94, a batch of ten** | Offered, and declined. Thirteen day documents, more than the learner asked for. |
| **Count 82–91 as one batch of ten** | Not allowed. ADR-0008: an earlier batch's unfinished days are finished under that batch's ADR and never count toward a new one. |
| **Loosen the order guard in `granth.py`** | Same answer as ADR-0003 to ADR-0011. The guard is right for *doing*. |

## Consequences

- **Better:** the eighth batch becomes whole, and phase 5 gets its middle: the complaint, the
  meeting, the update, the talk and the chart that the phase 5 gate stands on.
- **Worse:** ten more days of deliberate-failure parts rest on common beginner errors. Day 91 is
  written ninety learning days before it is read.
- **Worse:** days 82–91 assume three gates passed (phases 2, 3 and 4) that nobody has attempted.
  If any earlier gate fails when reached, days 41–91 are re-read before they are used.
- **Worse:** the uncommitted working tree grows to days 71–91. One unlucky reset loses eleven
  written days. The commit is owed, and it is named here so it is not forgotten.
- **Unchanged:** `python granth.py done N` refuses out of order and refuses an unticked checklist.
  A day with no `PROGRESS.md` row is not finished, however complete its folder looks.
