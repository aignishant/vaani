# ADR-0013 — A tenth batch of ten, days 92–101, carrying the phase 5 gate as a rehearsal and opening phase 6

- **Date:** 2026-09-24
- **Day:** between days 1 and 2 (days 2–91 written, none done)
- **Phase:** 5 → 6
- **Status:** accepted
- **Amends:** v1.10.0 → v1.11.0, §9 (the writing-ahead rule), §13
- **Related:** ADR-0003, ADR-0004, ADR-0005, ADR-0006, ADR-0007, ADR-0008, ADR-0009, ADR-0010, ADR-0011, ADR-0012

## Context

ADR-0012 authorised days 85–91 and closed with a sentence that binds this one:

> Day 92 onward needs either a closed day 6 in `docs/PROGRESS.md` or a further ADR, and the
> question is asked out loud again first.

The learner asked for "next 10 days doc". Five facts were true at that moment.

**The ledger has not moved.** `docs/PROGRESS.md` still holds one row, day 1.
`python granth.py brief 92` exits non-zero with "day 2 is next".

**The ninth batch is whole.** On 2026-09-24, before anything was written, `python granth.py depth N`
passed for each of days 85–91. The working tree was clean. The commit ADR-0011 and ADR-0012 said was
owed, covering days 71–91, has been made.

**The question was asked first.** The §9 question was put to the learner in the words §9 requires,
before anything was written: *is anybody doing the days?* It said that the ledger shows only day 1
closed and that days 2–91 are written but not done. It named the phase 5 gate, day 100, and the
phase boundary at day 101. It came with four options: write nothing and close days; days 92–96, the
original cap of five; days 92–100, ending on the gate; or days 92–101, ten as asked. **The learner
chose 92–101.**

**Ten days from day 92 cross a gate.** The phase 5 gate is day 100. §9 says a batch may cross a phase
boundary but never jump a gate it does not write. This batch writes day 100 inside it, as a rehearsal
under the gate rule, so day 101 is allowed.

**Earlier days already teach part of what this batch names.** Day 10 teaches numbers one to a
hundred, times and dates out loud. Day 34 teaches asking for a better price at a stall. Day 65
teaches *should*, *must* and *have to* on paper. Day 70 teaches explaining how something works.
Day 75 teaches describing a thing when you don't know its name. Day 76 teaches chunking, spelling
with letter words and read-back on a bad line. The days in this batch build on those and link back
to them. They don't teach them again. That's a writing choice, not a change to any ID, and it's
recorded here so nobody reads days 92, 96, 97, 98 and 101 as repeats.

## Decision

**A tenth batch of ten days, 92–101, is written ahead from the last written day.** It's at the cap.
It carries **day 100, the phase 5 gate, as a rehearsal** under the §9 gate rule. The gate teaches no
new rule, points at the §7 wording without softening it, and carries a mandatory, tickable
`docs/ERRORS.md` re-read for days 81 to 99 before `done 100`. Day 101 opens phase 6.

Every condition set by ADR-0004 to ADR-0012 still applies. Every day between the last closed day and
the last written day is fully written and passes `depth`. Days are still *done* one at a time, in
order, each with its own `done N` and its own commit. `docs/ERRORS.md` is read before each `done N`,
and a day whose failure parts miss the real pattern is amended first.

**What is kept, because it is the part still doing the work:**

- **The batch closes at its last day.** Day 102 onward needs either a closed day 6 in
  `docs/PROGRESS.md` or a further ADR, and the question is asked out loud again first.
- **Every written-ahead part says, in the part, that its wrong version is a common beginner error
  and not this learner's.**
- **Every written-ahead day's hub and `CHECKLIST.md` carry the tickable `ERRORS.md` re-read**
  before `done N`.
- **The formal-writing choice from ADR-0011 stands.** Formal pages in this batch leave out
  contractions as this course's choice, and say so where it matters. The gate page on day 100
  needs no contractions because the §7 wording says so.

## Options considered

| Option | Why not |
| --- | --- |
| **Write nothing new; close days** | Offered, and declined. It is still the option that protects the curriculum from being shaped by errors that have not happened. |
| **Days 92–96, the original cap of five** | Offered, and declined. Less than the learner asked for, and it leaves the gate unwritten. |
| **Days 92–100, ending on the gate** | Offered, and declined. A clean stop at the phase boundary, but one day fewer than asked. |
| **Days 92–101 without writing the gate** | Not allowed. §9: a batch that steps over an unwritten gate into the next phase is refused. |
| **Loosen the order guard in `granth.py`** | Same answer as ADR-0003 to ADR-0012. The guard is right for *doing*. |

## Consequences

- **Better:** phase 5 is fully written, gate included, and phase 6 has its first day.
- **Worse:** ten more days of deliberate-failure parts rest on common beginner errors. Day 101 is
  written a hundred learning days before it is read.
- **Worse:** the day 100 gate is written with nothing from days 81 to 99 in the error ledger. Its
  check lists are generic until the re-read is ticked. Until then it's a rehearsal, and it says so.
- **Worse:** days 92–101 assume four gates passed (phases 2, 3, 4 and 5) that nobody has attempted.
  If any earlier gate fails when reached, the days after it are re-read before they are used.
- **Unchanged:** `python granth.py done N` refuses out of order and refuses an unticked checklist.
  A day with no `PROGRESS.md` row is not finished, however complete its folder looks.
