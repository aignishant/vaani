# ADR-0010 — A seventh batch of ten, days 71–80, back at the cap and ending on the phase 4 gate

- **Date:** 2026-09-23
- **Day:** between days 1 and 2 (days 2–70 written, none done)
- **Phase:** 4
- **Status:** accepted
- **Amends:** v1.7.0 → v1.8.0, §9 (the writing-ahead rule), §13
- **Related:** ADR-0003, ADR-0004, ADR-0005, ADR-0006, ADR-0007, ADR-0008, ADR-0009

## Context

ADR-0009 authorised days 57–70 and closed with a sentence that binds this one:

> Day 71 onward needs either a closed day 6 in `docs/PROGRESS.md` or a further ADR, and the
> question is asked out loud again first.

The learner asked for "the next 14 days". Three facts were true at that moment.

**The ledger has not moved.** `docs/PROGRESS.md` still holds one row, day 1. So the §9 question was
put to the learner before anything was written, in the words §9 requires: *is anybody doing the
days?* It came with three options: write days 71–80 (ten, at the cap), write days 71–84 (fourteen,
past the cap a second time), or write nothing and close days instead. The question also stated the
cap, and said that ADR-0009's fourteen was a named exception that no later batch could use as a
precedent. **The learner chose ten, days 71–80.**

**The sixth batch is whole.** Days 57–70 are fully written. On 2026-09-23, before anything in this
batch was written, `python granth.py check` was green on all 70 written days, with the depth
contract met for every one. The §9 rule that *a batch is only started when the batch before it is
whole* holds.

**Ten days from day 71 ends exactly on the phase 4 gate.** Day 80 is the gate: a recorded opinion
with three reasons and one counter-argument answered, and a two-paragraph argument, one for and one
against, with a topic sentence in each.

## Decision

**A seventh batch of ten days, 71–80, is written ahead from the last written day, at the cap.**
Every condition set by ADR-0004 to ADR-0009 still applies. Every day between the last closed day
and the last written day is fully written and passes `depth`. Days are still *done* one at a time,
in order, each with its own `done N` and its own commit. `docs/ERRORS.md` is read before each
`done N`, and a day whose failure parts miss the real pattern is amended first.

**The cap is ten, and this batch keeps to it.** ADR-0009's exception stays one exception. The
learner was offered fourteen again and chose ten.

**The phase 4 gate, day 80, is written inside the batch as a rehearsal.** A batch never jumps a gate
it does not write. Day 80 is a rehearsal of the gate under ADR-0005. It teaches no new rule and
quotes §7 without softening it. Its hub and checklist carry the mandatory re-read of
`docs/ERRORS.md` for days 61 to 79.

**What is kept, because it is the part still doing the work:**

- **The batch closes at its last day.** Day 81 onward needs either a closed day 6 in
  `docs/PROGRESS.md` or a further ADR, and the question is asked out loud again first. Day 81 opens
  phase 5.
- **Every written-ahead part says, in the part, that its wrong version is a common beginner error
  and not this learner's.**
- **Every written-ahead day's hub and `CHECKLIST.md` carry the tickable `ERRORS.md` re-read**
  before `done N`.

## Options considered

| Option | Why not |
| --- | --- |
| **Write nothing new; close days** | Offered, and declined by the learner. It is still the option that protects the curriculum from being shaped by errors that have not happened. |
| **Write 71–84, fourteen, as asked** | Offered with the cap stated, and declined. It would have made ADR-0009's one-time exception into a habit, and stepped over the day 80 gate four days into phase 5. |
| **Write 71–84 silently, quoting ADR-0009** | Not allowed. §9 names that exception as no precedent. |
| **Write 71–79 and leave the gate** | Not asked for, and it would leave a gate unwritten one day beyond the batch. A gate doesn't need to end a batch, but here it falls exactly on the tenth day. |
| **Loosen the order guard in `granth.py`** | Same answer as ADR-0003 to ADR-0009. The guard is right for *doing*. |

## Consequences

- **Better:** phase 4 is written to its gate. Eighty days of curriculum survive the writing access
  ending, and the batch ends on a phase boundary, so the next batch starts a phase cleanly.
- **Better:** the cap is back at ten, and the learner chose it with fourteen on offer. An exception
  followed by a return to the rule is still an exception.
- **Worse:** ten more days of deliberate-failure parts rest on common beginner errors. Day 80 is
  written seventy-nine learning days before it is read, and the `ERRORS.md` re-read before each
  `done N` now covers seventy-nine days of repair work.
- **Worse:** days 71–80 assume two gates passed (phase 2, phase 3) that nobody has attempted, and
  day 80 rehearses a third. If any earlier gate fails when reached, days 41–80 are re-read before
  they are used.
- **Unchanged:** `python granth.py done N` refuses out of order and refuses an unticked checklist.
  A day with no `PROGRESS.md` row is not finished, however complete its folder looks.
