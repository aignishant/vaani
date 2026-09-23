# ADR-0008 — A fifth batch of ten, days 47–56, after finishing the day the fourth batch left half-written

- **Date:** 2026-09-23
- **Day:** between days 1 and 2 (days 2–45 written, day 46 half-written, none done)
- **Phase:** 3
- **Status:** accepted
- **Amends:** v1.5.0 → v1.6.0, §9 (the writing-ahead rule)
- **Related:** ADR-0003, ADR-0004, ADR-0005, ADR-0006, ADR-0007

## Context

ADR-0007 authorised days 37–46 and closed itself with two sentences that bind this one:

> Day 47 onward needs either a closed day 6 in `docs/PROGRESS.md` or a further ADR.

> The question ADR-0006 raised is the learner's and is asked, not assumed. It was asked before
> this batch and answered. It is asked again before a fifth.

Two facts were true when the fifth batch was asked for ("complete 10 next days doc").

**The ledger has not moved.** `docs/PROGRESS.md` still holds one row, day 1. No day has been
closed since ADR-0003. So the question was put to the learner before anything was written, in the
words §9 requires — *is anybody doing the days?* — with the option of writing nothing new and
closing days instead. **The learner answered: finish day 46, then write days 47–56.** The option
"finish 46 only, then close days" was offered and declined, and so was counting day 46 as the
first of the ten.

**The fourth batch was not finished.** Day 46 had four of its six parts on disk and no hub, no
checklist and no lab. It passed no `depth` check, because a day with no hub cannot. The §9 rule
that every batch rests on — *every day between the last closed day and the last written day is
fully written and passes `python granth.py depth N`* — was therefore false at the moment the fifth
batch was asked for. A batch written on top of a half-written day would have broken that rule in
the first line.

## Decision

**Day 46 is finished first, under ADR-0007**, which already authorised it. Its missing parts 2.2
and 2.3, its hub, its checklist and its lab are written, and `python granth.py depth 46` passes
before any day of this batch is started. Finishing a day an earlier batch authorised is not
new writing ahead and does not count toward this batch's ten.

**A fifth batch of ten days, 47–56, is written ahead from the last written day**, on every
condition ADR-0004 to ADR-0007 already set: every day between the last closed day and the last
written day is fully written and passes `depth`; days are still *done* one at a time, in order,
each with its own `done N` and its own commit; `docs/ERRORS.md` is read before each `done N`, and
a day whose failure parts miss the real pattern is amended first.

**The phase 3 gate, day 60, is outside this batch** and is not pulled in because it is near. The
batch crosses no gate, so the rule that a batch may not jump a gate it does not write is not
engaged.

**A batch is only started when the batch before it is whole.** This is new, and it is the lesson
of day 46: §9 now says so, so that the next batch cannot be asked for on top of a half-written
day either.

**What is kept, because it is the part still doing the work:**

- **The cap is ten and the batch closes at its last day.** Day 57 onward needs either a closed
  day 6 in `docs/PROGRESS.md` or a further ADR, and the question is asked out loud again first.
- **Every written-ahead part says, in the part, that its wrong version is a common beginner error
  and not this learner's.**
- **Every written-ahead day's hub and `CHECKLIST.md` carry the tickable `ERRORS.md` re-read**
  before `done N`.

## Options considered

| Option | Why not |
| --- | --- |
| **Finish day 46 and write nothing new** | Offered first, and declined by the learner. It is the option that protects the curriculum from being shaped by errors that have not happened, and that risk is already forty-five days old. |
| **Write 46–55, counting day 46 as the first of the ten** | Offered, and declined. It would also blur the rule: day 46 belongs to the fourth batch, and letting a new batch absorb an old batch's unfinished day makes "the batch closes at its last day" untrue. |
| **Write 47–56 and leave day 46 as it was** | The worst option. A half-written day sitting inside the written range makes the §9 condition false, and it would be read by the learner before any day of the new batch. |
| **Write 47–60, reaching the phase 3 gate** | Fourteen days, past the cap of ten. The cap is never widened (ADR-0006), and a gate is never pulled into a batch because it is next. |
| **Drop the per-batch ADR** | Same answer as ADR-0007. The ADR is what stops writing ahead from becoming invisible. |
| **Loosen the order guard in `granth.py`** | Same answer as ADR-0003 to ADR-0007. The guard is right for *doing*. |

## Consequences

- **Better:** day 46 is whole, and days 47–56 exist. Phase 3 is written to day 56, four days short
  of its gate. Fifty-six days of curriculum survive the writing access ending.
- **Worse:** ten more days of deliberate-failure parts rest on common beginner errors. Day 56 is
  written fifty-five learning days before it is read, and the `ERRORS.md` re-read before each
  `done N` now carries fifty-five days of repair work.
- **Worse:** days 47–56, like 41–46, assume a learner who has passed a phase 2 gate nobody has
  attempted. If that gate fails when it is reached, days 41–56 are re-read before they are used.
- **Unchanged:** `python granth.py done N` refuses out of order and refuses an unticked checklist.
  A day with no `PROGRESS.md` row is not finished, however complete its folder looks.
