# ADR-0015 — A twelfth batch of two, days 112–113, inside phase 6 and crossing no gate

- **Date:** 2026-09-24
- **Day:** between days 1 and 2 (days 2–111 written, none done)
- **Phase:** 6
- **Status:** accepted
- **Amends:** v1.12.0 → v1.13.0, §9 (the writing-ahead rule), §13
- **Related:** ADR-0003, ADR-0004, ADR-0009, ADR-0013, ADR-0014

## Context

ADR-0014 authorised days 102–111 and closed with a sentence that binds this one:

> Day 112 onward needs either a closed day 6 in `docs/PROGRESS.md` or a further ADR, and the
> question is asked out loud again first.

The learner asked for "next 2 days doc". Five facts were true at that moment.

**The ledger has not moved.** `docs/PROGRESS.md` still holds one row, day 1.
`python granth.py brief 102` exits non-zero with "day 2 is next".

**The eleventh batch was whole but not committed.** On 2026-09-24, `python granth.py depth N`
passed for each of days 102–111 and `python granth.py check` passed. Days 102–111 and the v1.12.0
amendment were on disk but uncommitted. That breaks the clean-tree condition every earlier batch
met.

**The question was asked first.** The §9 question was put to the learner in the words §9 requires,
before anything was written: *is anybody doing the days?* It said that only day 1 is closed, that
days 2–111 are written but not done, that day 101 alone has twenty unticked boxes, and that days
102–111 were uncommitted. It named days 112 and 113, said they cross no gate, and said the next
gate is day 120. It came with three options: write nothing and close days; commit days 102–111 and
then write days 112–113; or write days 112–113 on an uncommitted tree, not recommended. **The
learner chose to commit days 102–111 first, then write days 112–113.** Days 102–111 were committed
before anything in this batch was written.

**Two days from day 112 cross no gate.** The phase 6 gate is day 120. Day 113 writes the
proofreading checklist that the day 120 gate names. That makes day 113 something the gate needs,
not part of the gate.

**Earlier days already teach part of what this batch names.** Day 37 teaches asking someone to say
something again. Day 59 teaches talking about a mistake you made. Day 85 teaches sounding
confident. Day 101 teaches building from English you own. Days 102–111 teach the essay parts that
day 113's checklist checks. The days in this batch build on those and link back to them. They
don't teach them again.

## Decision

**A twelfth batch of two days, 112–113, is written ahead from the last written day.** It's under
the cap of ten. It crosses no gate and no phase boundary.

Every condition set by ADR-0004 to ADR-0014 still applies. Every day between the last closed day
and the last written day is fully written and passes `depth`. Days are still *done* one at a time,
in order, each with its own `done N` and its own commit. `docs/ERRORS.md` is read before each
`done N`, and a day whose failure parts miss the real pattern is amended first.

**What is kept:**

- **The batch closes at its last day.** Day 114 onward needs either a closed day 6 in
  `docs/PROGRESS.md` or a further ADR, and the question is asked out loud again first.
- **Every written-ahead part says, in the part, that its wrong version is a common beginner error
  and not this learner's.**
- **Every written-ahead day's hub and `CHECKLIST.md` carry the tickable `ERRORS.md` re-read**
  before `done N`.
- **The formal-writing choice from ADR-0011 stands.** Essays, reviews and reports leave out
  contractions as this course's choice, and say so where it matters.

**What is new:**

- **A batch starts from a clean tree.** The previous batch is committed before the next one is
  written. This was always true in practice. The eleventh batch broke it, so it is now written
  down.

## Options considered

| Option | Why not |
| --- | --- |
| **Write nothing new; close days** | Offered, and declined. It is still the option that protects the curriculum from being shaped by errors that have not happened. |
| **Write days 112–113 on the uncommitted tree** | Offered as not recommended. Declined. Two batches in one uncommitted diff can't be told apart or reverted one at a time. |
| **Loosen the order guard in `granth.py`** | Same answer as ADR-0003 to ADR-0014. The guard is right for *doing*. |

## Consequences

- **Better:** the checklist that the day 120 gate proofreads against exists before the gate is
  written.
- **Worse:** two more days of deliberate-failure parts rest on common beginner errors. Day 113 is
  written a hundred and twelve learning days before it is read.
- **Unchanged:** `python granth.py done N` refuses out of order and refuses an unticked checklist.
  A day with no `PROGRESS.md` row is not finished, however complete its folder looks.
