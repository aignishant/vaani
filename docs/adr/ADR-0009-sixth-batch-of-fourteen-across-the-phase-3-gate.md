# ADR-0009 — A sixth batch of fourteen, days 57–70, carrying the phase 3 gate and widening the cap once

- **Date:** 2026-09-23
- **Day:** between days 1 and 2 (days 2–56 written, none done)
- **Phase:** 3, crossing into 4
- **Status:** accepted
- **Amends:** v1.6.0 → v1.7.0, §9 (the writing-ahead rule)
- **Related:** ADR-0003, ADR-0004, ADR-0005, ADR-0006, ADR-0007, ADR-0008

## Context

ADR-0008 authorised days 47–56 and closed itself with a sentence that binds this one:

> Day 57 onward needs either a closed day 6 in `docs/PROGRESS.md` or a further ADR, and the
> question is asked out loud again first.

The learner asked for "the next 14 days". Three facts were true at that moment.

**The ledger has not moved.** `docs/PROGRESS.md` still holds one row, day 1. So the §9 question was
put to the learner before anything was written, in the words §9 requires — *is anybody doing the
days?* — with three options: write days 57–66 (ten, at the cap), write days 57–70 (fourteen, past
the cap), or write nothing and close days instead. **The learner chose fourteen, days 57–70.**

**The fifth batch is whole.** Days 43–56 are fully written, and on 2026-09-23 `python granth.py
depth` passed for each of them and `python granth.py check` was green on all 56 written days. The
§9 rule that *a batch is only started when the batch before it is whole* holds.

**Fourteen is past the cap.** §9 says a batch is never widened past ten, and ADR-0006 said the
cap is never widened. ADR-0008 listed fourteen days (47–60) as an option and turned it down for
exactly that reason. This time the learner was told about the cap in the question itself, was
offered the ten-day batch first, and chose fourteen anyway.

## Decision

**A sixth batch of fourteen days, 57–70, is written ahead from the last written day.** Every
condition ADR-0004 to ADR-0008 set still applies. Every day between the last closed day and the
last written day is fully written and passes `depth`. Days are still *done* one at a time, in
order, each with its own `done N` and its own commit. `docs/ERRORS.md` is read before each
`done N`, and a day whose failure parts miss the real pattern is amended first.

**The cap is widened once, for this batch, by name.** The cap stays ten. This batch is a
recorded exception because the learner chose it with the cap in front of them. §9 names it as an
exception, so the next batch cannot quote it as a precedent. A batch of more than ten needs its
own ADR, and the learner has to choose it with the cap stated.

**The phase 3 gate, day 60, is written inside the batch as a rehearsal.** The batch crosses it, so
the rule that a batch never jumps a gate it does not write applies. Day 60 is a rehearsal of the
gate under ADR-0005. It teaches no new rule and quotes §7 without softening it. Its hub and
checklist carry the mandatory re-read of `docs/ERRORS.md` for days 41 to 59.

**Days 61–70 open phase 4** and assume a learner who has passed a phase 3 gate nobody has
attempted.

**What is kept, because it is the part still doing the work:**

- **The batch closes at its last day.** Day 71 onward needs either a closed day 6 in
  `docs/PROGRESS.md` or a further ADR, and the question is asked out loud again first.
- **Every written-ahead part says, in the part, that its wrong version is a common beginner error
  and not this learner's.**
- **Every written-ahead day's hub and `CHECKLIST.md` carry the tickable `ERRORS.md` re-read**
  before `done N`.

## Options considered

| Option | Why not |
| --- | --- |
| **Write nothing new; close days** | Offered, and declined by the learner. It is still the option that protects the curriculum from being shaped by errors that have not happened. |
| **Write 57–66, at the cap of ten** | Offered first, and declined. It would have kept the cap intact and stopped six days into phase 4. |
| **Write 57–70 silently, as if ten were still the cap** | The worst option. A cap that is broken without a record is not a cap any more. |
| **Raise the cap to fourteen for every batch** | Not asked for. One learner's choice of one batch is an exception, not a new rule. |
| **Stop at 60, the gate** | Four days. Not what was asked for, and the gate does not need to end a batch. It needs to be written inside one. |
| **Loosen the order guard in `granth.py`** | Same answer as ADR-0003 to ADR-0008. The guard is right for *doing*. |

## Consequences

- **Better:** phase 3 is written to its gate, and phase 4 is written to day 70. Seventy days of
  curriculum survive the writing access ending.
- **Worse:** fourteen more days of deliberate-failure parts rest on common beginner errors. Day 70
  is written sixty-nine learning days before it is read, and the `ERRORS.md` re-read before each
  `done N` now covers sixty-nine days of repair work.
- **Worse:** the cap has now been widened once. A cap that has been widened is easier to widen
  again. That is why the exception is named in §9 and needs a fresh ADR and a fresh choice.
- **Worse:** days 61–70 assume two gates passed (phase 2, phase 3) that nobody has attempted. If
  either fails when reached, days 41–70 are re-read before they are used.
- **Unchanged:** `python granth.py done N` refuses out of order and refuses an unticked checklist.
  A day with no `PROGRESS.md` row is not finished, however complete its folder looks.
