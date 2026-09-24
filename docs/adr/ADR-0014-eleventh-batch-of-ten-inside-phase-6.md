# ADR-0014 — An eleventh batch of ten, days 102–111, inside phase 6 and crossing no gate

- **Date:** 2026-09-24
- **Day:** between days 1 and 2 (days 2–101 written, none done)
- **Phase:** 6
- **Status:** accepted
- **Amends:** v1.11.0 → v1.12.0, §9 (the writing-ahead rule), §13
- **Related:** ADR-0003, ADR-0004, ADR-0005, ADR-0006, ADR-0007, ADR-0008, ADR-0009, ADR-0010, ADR-0011, ADR-0012, ADR-0013

## Context

ADR-0013 authorised days 92–101 and closed with a sentence that binds this one:

> Day 102 onward needs either a closed day 6 in `docs/PROGRESS.md` or a further ADR, and the
> question is asked out loud again first.

The learner asked for "next 10 days doc". Five facts were true at that moment.

**The ledger has not moved.** `docs/PROGRESS.md` still holds one row, day 1.
`python granth.py brief 102` exits non-zero with "day 2 is next".

**The tenth batch is whole.** On 2026-09-24, before anything was written, `python granth.py depth N`
passed for each of days 92–101. The working tree was clean, and days 92–101 were committed.

**The question was asked first.** The §9 question was put to the learner in the words §9 requires,
before anything was written: *is anybody doing the days?* It said that the ledger shows only day 1
closed, that days 2–101 are written but not done, and that day 101 alone has twenty unticked boxes. It
said that no gate falls inside days 102–111, and that the next gate is day 120. It came with four
options: write nothing and close days; days 102–106, the original cap of five; days 102–111, ten as
asked; or days 102–112, eleven, over the cap and not recommended. **The learner chose 102–111.**

**Ten days from day 102 cross no gate.** The phase 6 gate is day 120. The batch stays inside phase 6.

**Earlier days already teach part of what this batch names.** Day 17 teaches linking one word into
the next. Day 35 teaches contractions aloud. Day 39 teaches joining two sentences with *and*, *but*,
*because* and *so*. Day 43 teaches a story with a beginning, a middle and an end. Day 47 teaches the
topic sentence, and day 57 teaches one idea per paragraph. Day 50 teaches *bored* and *boring*. Day 62
teaches disagreeing without offending. Days 67 and 71 teach the first and second conditionals. Day 73
teaches for and against in two paragraphs. Day 77 teaches summarising a conversation. Day 89 teaches
*however* and *therefore*. The days in this batch build on those and link back to them. They don't
teach them again. That's a writing choice, not a change to any ID, and it's recorded here so nobody
reads days 102, 104, 105, 106, 107, 108 and 110 as repeats.

## Decision

**An eleventh batch of ten days, 102–111, is written ahead from the last written day.** It's at the
cap. It crosses no gate and no phase boundary.

Every condition set by ADR-0004 to ADR-0013 still applies. Every day between the last closed day and
the last written day is fully written and passes `depth`. Days are still *done* one at a time, in
order, each with its own `done N` and its own commit. `docs/ERRORS.md` is read before each `done N`,
and a day whose failure parts miss the real pattern is amended first.

**What is kept, because it is the part still doing the work:**

- **The batch closes at its last day.** Day 112 onward needs either a closed day 6 in
  `docs/PROGRESS.md` or a further ADR, and the question is asked out loud again first.
- **Every written-ahead part says, in the part, that its wrong version is a common beginner error
  and not this learner's.**
- **Every written-ahead day's hub and `CHECKLIST.md` carry the tickable `ERRORS.md` re-read**
  before `done N`.
- **The formal-writing choice from ADR-0011 stands.** Essays, summaries and reports in this batch
  leave out contractions as this course's choice, and say so where it matters.

## Options considered

| Option | Why not |
| --- | --- |
| **Write nothing new; close days** | Offered, and declined. It is still the option that protects the curriculum from being shaped by errors that have not happened. |
| **Days 102–106, the original cap of five** | Offered, and declined. Less than the learner asked for. |
| **Days 102–112, eleven** | Offered as over the cap and not recommended. Declined. The cap stays ten (ADR-0009). |
| **Loosen the order guard in `granth.py`** | Same answer as ADR-0003 to ADR-0013. The guard is right for *doing*. |

## Consequences

- **Better:** the essay sequence of phase 6 — introduction, body paragraph, conclusion, then the
  argumentative, descriptive and narrative essays and the report — is written as one run.
- **Worse:** ten more days of deliberate-failure parts rest on common beginner errors. Day 111 is
  written a hundred and ten learning days before it is read.
- **Worse:** days 102–111 assume four gates passed (phases 2, 3, 4 and 5) that nobody has attempted.
  If any earlier gate fails when reached, the days after it are re-read before they are used.
- **Unchanged:** `python granth.py done N` refuses out of order and refuses an unticked checklist.
  A day with no `PROGRESS.md` row is not finished, however complete its folder looks.
