# ADR-0005 — A second batch of ten, days 17–26, and the phase gate day may be written ahead

- **Date:** 2026-09-22
- **Day:** between days 1 and 2 (days 2–16 written, not done)
- **Phase:** 1, crossing into 2
- **Status:** accepted
- **Amends:** v1.2.0 → v1.3.0, §9 (the writing-ahead rule, both sentences)
- **Related:** ADR-0001, ADR-0003, ADR-0004

## Context

ADR-0004 allowed one batch of ten, days 7–16, and closed itself deliberately: *"day 17 onward
needs either a closed day 6 or a new ADR."* That sentence was written so that the next batch
would have to be argued for again rather than drifting into a habit. This is that argument.

Two facts stand today, 2026-09-22.

**The ledger has one row.** `docs/PROGRESS.md` records day 1 and nothing else. Days 2–16 are
written, pass `python granth.py depth`, and are not done. Under §9 as it stands, nothing further
can be written until day 6 is closed.

**The reason for writing ahead has not changed.** The learner's access to the tool that writes
these documents is on a budget they may not be able to renew. A day not written today may never
be written. Ten more days written now is ten more days of curriculum that survive the
subscription ending.

Against that stands the cost, which grows with every batch and is now large enough to state
plainly: **days 17–26 are written with only day 1's real errors in `docs/ERRORS.md`.** Day 26 is
written twenty-five learning days before it is read. Every deliberate-failure part in the batch
rests on what beginners commonly do, not on what this learner did.

**And one rule is directly in the way.** §9 ends the ADR-0004 paragraph with: *"The phase gate
day is never written ahead."* Day 20 is the phase 1 gate. The rule is a good one and its reason
is real: a gate is an assessment of a phase, and an assessment written before the phase happened
cannot be shaped by the phase. The gate day's parts should be able to say "you have been getting
the -s wrong since day 15, so watch it here", and a gate written now cannot say that.

But the rule assumes the writer will still be there when day 20 arrives. If that assumption
fails, the consequence of the rule is not a better gate; it is **no gate at all**, an unclosable
phase, and a portfolio with a hole where its first piece should be. A rule that protects quality
by risking existence is the wrong rule for this particular risk.

## Decision

**A second batch of up to ten days, 17–26, may be written ahead from the last written day.**
Days are still *done* one at a time, in order, each with its own `python granth.py done N` and
its own commit. Every condition of ADR-0004 carries over unchanged.

**And: a phase gate day may be written ahead, but only as a rehearsal of a gate, never as the
gate's final wording.** Concretely, for day 20 and any gate day written under this ADR:

- The gate day is written to the same depth contract as any other day — hub, two folders, three
  parts each, a deliberate failure in each folder.
- Its parts teach **how to assemble and check a long piece from what the phase already taught**.
  They do not introduce a new rule, because a gate that teaches something new is not a gate.
- **The gate day's hub and checklist carry a mandatory re-read step before `done N`:** the
  learner or the writer reads `docs/ERRORS.md` for every day of the phase and amends the gate
  day's check lists to name this learner's actual recurring mistakes. This step is not optional
  and is a ticked box on `CHECKLIST.md`, not a suggestion in prose.
- The gate's **pass condition is never weakened** by having been written early. Plan §7 carries
  the gate wording; the day document points at it and does not restate it more kindly.

**This ADR closes at day 26.** Day 27 onward needs either a closed day 6 or a further ADR. The
cap is kept deliberately: it is the only thing that makes each batch a decision instead of a
default.

## Options considered

| Option | Why not |
| --- | --- |
| **Write only days 17–19 and stop at the gate** | Honours §9 exactly, and is the safest reading. It delivers three days instead of ten, and leaves the phase 1 gate — the day that produces the first portfolio piece — as the single day most likely never to be written. It protects the gate's wording at the cost of the gate. |
| **Write 17–19 and 21–26, leaving a hole at day 20** | Keeps the letter of the gate rule, but a numbered gap in `days/` is exactly what §11.3 forbids inside a day and what the order rule forbids across days. It also hides the decision: nothing in the repository would say why 20 is missing. |
| **Write the gate day but let it introduce new material** | Then it is day 21 wearing day 20's number. A gate that teaches is not a gate, and the phase would end without ever being measured. |
| **Drop the cap and write the rest of phase 2 while the tool exists** | The cost already named — failure parts written blind — scales with the batch, and past ten days it stops being amendable and starts being a second curriculum written over the first. Ten is the run ADR-0004 argued for; this ADR does not get to quietly raise it. |
| **Loosen the order guard in `granth.py`** | Same answer as ADR-0003 and ADR-0004. The guard is right for *doing*. The exception is for *writing*, and it belongs in an ADR, not in the toolchain. |

## Consequences

- **Better:** days 17–26 exist, and phase 1 can be closed even if the writing tool goes away
  tomorrow. The phase 1 gate has a document.
- **Worse:** ten days of deliberate-failure parts rest on common beginner errors rather than this
  learner's ledger, and say so in every part. The day 20 gate is a rehearsal until its re-read
  step is done; until then, its check lists are generic.
- **Worse:** this is the second ADR in a row to widen the same rule. If a third is written
  without a closed day in between, the honest reading is that the order rule has been abandoned
  in practice, and that should be faced directly rather than by a fourth exception.
- **Unchanged:** `python granth.py done N` still refuses out of order and still refuses an
  unticked checklist. A day with no `PROGRESS.md` row is still not finished, however complete
  its folder looks.
