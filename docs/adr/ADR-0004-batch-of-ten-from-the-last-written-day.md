# ADR-0004 — A batch may be up to ten days and may start from the last written day, when the learner's access to the writing tool is not guaranteed

- **Date:** 2026-09-22
- **Day:** between days 1 and 2 (days 2–6 written, not done)
- **Phase:** 1
- **Status:** accepted
- **Amends:** v1.1.0 → v1.2.0, §9 (the writing-ahead rule)
- **Related:** ADR-0001, ADR-0003

## Context

ADR-0003 allows days to be *written* ahead in batches of up to five, counted from the last day
closed in `docs/PROGRESS.md`. Under it, days 2–6 were written on 2026-09-22. None is done yet:
the ledger has one row, day 1.

On the same date the learner asked for the next ten days, 7–16, in one sitting. The reason is
not convenience. The learner's account with the tool that writes these documents is on a budget
they may not be able to renew, so a day not written today may not get written at all. Under
ADR-0003 as it stands, nothing can be written until day 6 is done, and by then the tool may be
gone. A curriculum whose next day depends on a subscription is a curriculum that stops when the
subscription does.

The cost named in ADR-0003 grows with the batch and should be named again: days 7–16 are written
with only day 1's real errors in `docs/ERRORS.md`. Their deliberate-failure parts rest on what
beginners commonly do, not on what this learner did on days 2–15. Day 16 is written fifteen
learning days before it is read.

## Decision

**When the learner's access to the writing tool is not guaranteed, a batch may be up to ten
days and may start from the last *written* day rather than the last *closed* day, provided every
day between the last closed day and the last written day is fully written and passes
`python granth.py depth N`.** Days are still *done* one at a time, in order, each with its own
`python granth.py done N` and its own commit.

- The batch under this ADR is days 7–16. It closes at day 16; day 17 onward needs either a
  closed day 6 or a new ADR.
- `brief` is run for the first day of the batch; it exits non-zero, as designed, and the writer
  records the stop in the hub's §8 and proceeds under this ADR. For the rest, the writer reads
  the plan's §8 row directly and says so in the hub.
- Every hub in the batch says in §8 that it was written under ADR-0004, ahead of its turn, and
  every deliberate-failure part says its wrong version rests on common beginner errors.
- **Before each `done N`, the learner or the writer reads the `docs/ERRORS.md` rows from days
  2 to N−1.** If a day's failure parts miss the real pattern, the day is amended first and done
  second. This is the rule that makes the batch safe, and it is unchanged from ADR-0003.
- The `PROGRESS.md` rule is unchanged: a day with no row is not finished, however complete its
  folder looks. The order guard on `done` is untouched.

The load-bearing half is still *done in order, one commit each*, plus the read of `ERRORS.md`
before each `done`. Writing ahead changes when the documents exist; it changes nothing about
when a day counts.

## Options considered

| Option | Why not |
| --- | --- |
| **Keep ADR-0003 as it stands (batches of five from the last closed day)** | Correct when the writer is always available. Here the writer may not be, and a rule that produces zero days when it is most needed has failed at its one job. |
| **Write only days 7–11 (another five) from the last written day** | Halves the exposure to blind failure parts, but leaves the learner with an eleven-day buffer that ends mid-phase, with the tool possibly gone. Ten is what the learner asked for, knowing the cost, and stops short of the gate. |
| **Write the whole phase (days 7–20)** | Day 20 is the phase gate. A gate written before any of the phase's real errors exist would test what the writer guessed, not what the learner did. The gate stays unwritten until day 19 is done. |
| **Loosen `brief`'s order guard in `granth.py`** | Touches the toolchain for a workflow choice. The guard is right for *doing*; the exception is for *writing*, and it is recorded here instead. |

## Consequences

- **Better:** days 7–16 exist today. The learner can do one day each morning for the next fifteen
  days without a writing turn standing between them and the recorder, whether or not the tool is
  still available.
- **Worse:** ten days of failure parts written blind. Each says so. Some will miss this learner's
  real mistakes.
- **New failure mode:** a written-ahead day drifts from what the learner needs and nobody re-reads
  it before it is done. What catches it: the `ERRORS.md` read before each `done N`, above. If the
  tool is gone, the learner does the read themselves and writes a note under the day's
  `PROGRESS.md` row saying what the failure part missed.
- **Revisit if:** the learner's ledger shows the generic failure parts missing their real
  mistakes two days running; or the account is renewed, in which case day 17 onward returns to
  ADR-0003's batch of five from the last closed day.
