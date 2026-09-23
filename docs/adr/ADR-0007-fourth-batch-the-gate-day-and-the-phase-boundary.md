# ADR-0007 — A fourth batch of ten, days 37–46, carrying the phase 2 gate and crossing into phase 3

- **Date:** 2026-09-23
- **Day:** between days 1 and 2 (days 2–36 written, not done)
- **Phase:** 2 into 3
- **Status:** accepted
- **Amends:** v1.4.0 → v1.5.0, §9 (the writing-ahead rule)
- **Related:** ADR-0001, ADR-0003, ADR-0004, ADR-0005, ADR-0006

## Context

ADR-0006 closed itself at day 36 and left a sentence that is not about writing ahead at all:

> If a fourth batch is asked for before a single day is closed, the question to ask is no longer
> "may we write ahead?" but "is anybody doing the days?" — and that question belongs to the
> learner, not to another ADR.

A fourth batch was asked for, and `docs/PROGRESS.md` still holds one row: day 1. So the question
was put to the learner before anything was written, in those words, with the option of writing
nothing new and closing days instead. **The learner answered: write days 37–46 anyway.** The
reason is the one every batch has had, and it is about the tool and not about the learning — the
access that writes these documents is on a budget that may not be renewed, and a day not written
now may never be written at all.

That answer settles the question this ADR is not allowed to settle for itself. It does not settle
the cost, so the cost is restated, larger again: **days 37–46 are written with one day of real
errors behind them.** Day 46 is written forty-five learning days before it is read. Every
deliberate-failure part in this batch rests on errors beginners commonly make, not on errors this
learner has made, and says so inside the part.

Two things are new in this batch, and neither was true of the three before it.

**The phase 2 gate, day 40, is inside it.** ADR-0006 kept day 40 out deliberately, four days short,
"so the gate can still be written with more of the phase's errors in hand if the tool survives
that long". The tool survived four days and no more errors arrived, because no day has been done.
Waiting again would buy nothing — there is no mechanism by which errors appear while the ledger is
still. The gate is therefore written, and it is written as a **rehearsal** under the rule ADR-0005
already set: it teaches no new rule, it points at the plan's §7 wording and never restates it more
kindly, and it does not become a gate until its `docs/ERRORS.md` re-read is ticked.

**The batch crosses a phase boundary.** Days 37–40 finish phase 2; days 41–46 open phase 3, whose
theme is the past and telling what happened. Writing across a gate is a further loosening: phase 3
days are written before the phase 2 gate has been attempted, so they assume a learner who can do
something nobody has watched them do. That is named here rather than discovered later.

## Decision

**A fourth batch of ten days, 37–46, is written ahead from the last written day**, on every
condition ADR-0004, ADR-0005 and ADR-0006 already set: every day between the last closed day and
the last written day is fully written and passes `python granth.py depth N`; days are still *done*
one at a time, in order, each with its own `done N` and its own commit; `docs/ERRORS.md` is read
before each `done N`, and a day whose failure parts miss the real pattern is amended first.

**Day 40, the phase 2 gate, is written as a rehearsal**, under the ADR-0005 gate rule in full. It
teaches no new rule. It quotes the gate wording from §7 and adds nothing to it. Its hub and its
`CHECKLIST.md` carry a mandatory, tickable re-read of `docs/ERRORS.md` for every day of phase 2
before `done 40`, at which point its generic check lists are replaced by this learner's real
recurring mistakes. Until that box is ticked it is a rehearsal and says so on its own first page.

**A batch may cross a phase boundary**, and the plan's §9 now says so rather than leaving it to be
inferred. The condition is that the gate day between the two phases is itself in the batch and
written as a rehearsal: a batch may not jump a gate it does not write.

**What is kept, because it is the part still doing the work:**

- **The cap is ten and the batch closes at its last day.** Day 47 onward needs either a closed day
  6 in `docs/PROGRESS.md` or a further ADR.
- **Every written-ahead part says, in the part, that its wrong version is a common beginner error
  and not this learner's.**
- **Every written-ahead day's hub and `CHECKLIST.md` carry the tickable `ERRORS.md` re-read**
  before `done N`.
- **The question ADR-0006 raised is the learner's and is asked, not assumed.** It was asked before
  this batch and answered. It is asked again before a fifth.

## Options considered

| Option | Why not |
| --- | --- |
| **Write nothing until a day is closed** | The option the learner was offered first, in those words, and declined. Declining it is theirs to do: the risk it protects against — a curriculum shaped by errors that have not happened — is already thirty-five days old, and the risk it accepts is that the writing access ends with ten fewer days on disk. |
| **Write 37–39 and stop before the gate** | Offered, and declined. It keeps day 40 unwritten for the same reason ADR-0006 gave, but that reason has now failed its own test: four days passed and no error rows appeared, because the ledger only moves when a day is *done*. Stopping short a second time protects nothing and leaves the phase without its gate. |
| **Write 37–46 and treat day 40 as an ordinary day** | The worst of the three. A gate that is written like a lesson stops being a gate, and the phase 2 check becomes a document the learner reads rather than a thing they have to pass. ADR-0005 wrote the rehearsal rule for exactly this. |
| **Write 37–40 only, stopping at the phase boundary** | Tidier, and it avoids writing phase 3 before phase 2 has been attempted. But it spends a whole ADR on four days, and the cap exists to make each batch a decision, not to make the decisions small. The phase crossing is a real cost and is written down instead of avoided. |
| **Drop the per-batch ADR now that writing ahead is normal** | The argument step is the only thing left. ADR-0006 made writing ahead the normal mode; the ADR is what stops it becoming invisible. |
| **Loosen the order guard in `granth.py`** | Same answer as ADR-0003 through ADR-0006. The guard is right for *doing*. The exception is for *writing*, and it belongs here. |

## Consequences

- **Better:** days 37–46 exist. Phase 2 is complete, gate included, and phase 3 is open to day 46.
  Forty-six days of curriculum survive the writing access ending.
- **Worse:** ten more days of deliberate-failure parts rest on common beginner errors, and the
  `ERRORS.md` re-read before each `done N` now carries forty-five days of repair work.
- **Worse:** the phase 2 gate is written by a repository that has watched the learner do one day.
  Its check lists are generic until the re-read replaces them, and a gate with generic checks is a
  rehearsal wearing a gate's name. It says so, in the hub and on the checklist.
- **Worse:** phase 3 days assume a learner who has passed a gate nobody has attempted. If the gate
  is failed when it is reached, days 41–46 are re-read before they are used, and the phase 2 days
  named in the failure are re-run first, with their own `PROGRESS.md` rows.
- **Unchanged:** `python granth.py done N` refuses out of order and refuses an unticked checklist.
  A day with no `PROGRESS.md` row is not finished, however complete its folder looks.
