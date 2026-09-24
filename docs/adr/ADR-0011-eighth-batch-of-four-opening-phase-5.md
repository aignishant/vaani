# ADR-0011 — An eighth batch of four, days 81–84, opening phase 5

- **Date:** 2026-09-23
- **Day:** between days 1 and 2 (days 2–80 written, none done)
- **Phase:** 5
- **Status:** accepted
- **Amends:** v1.8.0 → v1.9.0, §9 (the writing-ahead rule), §13
- **Related:** ADR-0003, ADR-0004, ADR-0005, ADR-0006, ADR-0007, ADR-0008, ADR-0009, ADR-0010

## Context

ADR-0010 authorised days 71–80 and closed with a sentence that binds this one:

> Day 81 onward needs either a closed day 6 in `docs/PROGRESS.md` or a further ADR, and the
> question is asked out loud again first. Day 81 opens phase 5.

The learner asked to "complete next 4 days doc". Three facts were true at that moment.

**The ledger has not moved.** `docs/PROGRESS.md` still holds one row, day 1, and
`python granth.py brief 81` exits non-zero with "day 2 is next". So the §9 question was put to the
learner before anything was written, in the words §9 requires: *is anybody doing the days?* It
came with three options: write nothing and close days, write days 81–84 as asked, or write days
81–90 at the cap of ten. The question also said that day 84 would be written eighty-three learning
days before it is read, and that phase 5 would open with no real errors behind it. **The learner
chose four, days 81–84.**

**The seventh batch is whole.** Days 71–80 are fully written. On 2026-09-23, before anything in
this batch was written, `python granth.py check` was green on all 80 written days, and
`python granth.py depth N` passed for each of days 71 to 80. The §9 rule that *a batch is only
started when the batch before it is whole* holds. One thing is recorded because it is true: at that
moment days 71–80 were in the working tree and not yet in a commit. Whole means written and
passing `depth`, not committed, so the rule holds. The commit is still owed.

**Four days from day 81 crosses no gate.** The phase 5 gate is day 100. Days 81–84 open the
phase: formal and informal, introducing yourself at work and the formal email, the interview's
first question and the CV, the standard interview questions and the cover letter.

## Decision

**An eighth batch of four days, 81–84, is written ahead from the last written day.** It is under
the cap of ten. Every condition set by ADR-0004 to ADR-0010 still applies. Every day between the
last closed day and the last written day is fully written and passes `depth`. Days are still
*done* one at a time, in order, each with its own `done N` and its own commit. `docs/ERRORS.md`
is read before each `done N`, and a day whose failure parts miss the real pattern is amended
first.

**A batch smaller than the cap is a batch like any other.** It gets its own ADR and the question
asked first, exactly as a batch of ten does. Four is not a reason to skip the question.

**What is kept, because it is the part still doing the work:**

- **The batch closes at its last day.** Day 85 onward needs either a closed day 6 in
  `docs/PROGRESS.md` or a further ADR, and the question is asked out loud again first.
- **Every written-ahead part says, in the part, that its wrong version is a common beginner error
  and not this learner's.**
- **Every written-ahead day's hub and `CHECKLIST.md` carry the tickable `ERRORS.md` re-read**
  before `done N`.

**One choice the phase 5 days name out loud.** The plan's §5 pins formal writing as having no
contractions, and the phase 5 gate asks for "no contractions". The reference pages opened on
2026-09-23 do not all agree. One academic-writing guide says to avoid contractions because "they
are too informal". One learner's page on an email cover letter offers a model sentence that
begins *I'm writing*. The writing parts of days 81, 82 and 84 say plainly that leaving
contractions out of formal writing is this course's choice, which is always safe and which the
gate asks for. They do not pretend every formal writer everywhere agrees. The plan is not
amended for this. §5 already says the day names the choice where it matters.

## Options considered

| Option | Why not |
| --- | --- |
| **Write nothing new; close days** | Offered, and declined by the learner. It is still the option that protects the curriculum from being shaped by errors that have not happened. |
| **Write 81–90, ten, at the cap** | Offered, and declined. It would have written more ahead than the learner asked for. |
| **Write 81–84 without the question, because four is small** | Not allowed. §9 asks the question before any batch on an unmoved ledger, whatever its size. |
| **Loosen the order guard in `granth.py`** | Same answer as ADR-0003 to ADR-0010. The guard is right for *doing*. |

## Consequences

- **Better:** phase 5 has its first four days, including the formal email, the CV and the cover
  letter the phase 5 gate needs.
- **Better:** the batch asks for no more than the learner asked for, and it steps over no gate.
- **Worse:** four more days of deliberate-failure parts rest on common beginner errors. Day 84 is
  written eighty-three learning days before it is read.
- **Worse:** days 81–84 assume three gates passed (phases 2, 3 and 4) that nobody has attempted.
  If any earlier gate fails when reached, days 41–84 are re-read before they are used.
- **Unchanged:** `python granth.py done N` refuses out of order and refuses an unticked checklist.
  A day with no `PROGRESS.md` row is not finished, however complete its folder looks.
