# ADR-0006 — A third batch of ten, days 27–36, and the order rule named for what it has become

- **Date:** 2026-09-22
- **Day:** between days 1 and 2 (days 2–26 written, not done)
- **Phase:** 2
- **Status:** accepted
- **Amends:** v1.3.0 → v1.4.0, §9 (the writing-ahead rule)
- **Related:** ADR-0001, ADR-0003, ADR-0004, ADR-0005

## Context

ADR-0005 closed itself at day 26 and left this sentence behind:

> If a third is written without a closed day in between, the honest reading is that the order rule
> has been abandoned in practice, and that should be faced directly rather than by a fourth
> exception.

This is that third ADR, and no day has been closed in between. `docs/PROGRESS.md` still has one
row: day 1. Days 2–26 are written and not done. So the sentence applies, and this ADR does not get
to pretend otherwise by arguing the same budget argument a third time.

**So face it.** The order rule, as written, is two rules wearing one name:

1. **Days are *done* in order.** Day N is practised only after day N−1 was practised. This rule
   has never been broken. `python granth.py done N` still refuses out of order, and one row in
   `PROGRESS.md` is the proof that it refuses.
2. **Days are *written* close to where the learner is.** This rule has been widened three times
   and is, in practice, gone. Twenty-five days are written ahead of a learner standing on day 1.

Rule 1 is the one that protects the learning. Rule 2 protected something real but smaller: that a
day is shaped by the errors of the days before it. Pretending rule 2 still holds is now the
dishonest option, and the repository's whole point is that a deviation written down is a decision
and one that is not is a defect.

The cost is therefore restated plainly, and it is larger than in ADR-0005: **days 27–36 are
written with one day of real errors behind them.** Every deliberate-failure part in this batch
rests on errors beginners commonly make, not on errors this learner has made. Day 36 is written
thirty-five learning days before it is read. No amount of care in the writing changes that, and
the only thing that repairs it is the `docs/ERRORS.md` re-read before each `done N`, which is
already a ticked box on every checklist in the batch.

The reason for writing ahead is unchanged and is still real: the learner's access to the tool that
writes these documents is on a budget they may not be able to renew. A day not written today may
never be written. Phase 2 runs to day 40; this batch takes it to 36.

## Decision

**A third batch of up to ten days, 27–36, may be written ahead from the last written day**, on
every condition ADR-0004 and ADR-0005 already set: every day between the last closed day and the
last written day is fully written and passes `python granth.py depth N`; days are still *done* one
at a time, in order, each with its own `done N` and its own commit; `docs/ERRORS.md` is read before
each `done N` and a day whose failure parts miss the real pattern is amended first.

**And the plan stops claiming that writing ahead is exceptional.** §9 is rewritten to say what is
true: *doing* days in order is the hard rule and is enforced by the toolchain; *writing* ahead is
allowed in batches of up to ten from the last written day while the learner's access to the
writing tool is not guaranteed, and every such batch carries the generic-failure cost in writing,
in every part it produces.

**What is kept, because it is the part that was doing the work:**

- **Each batch is still capped at ten and still closes at its last day.** Day 37 onward needs
  either a closed day 6 or a further ADR. The cap is the only thing that keeps each batch a
  decision.
- **Every written-ahead part says, in the part, that its wrong version is a common beginner error
  and not this learner's.** A reader must not be able to mistake a generic failure for a
  diagnosed one.
- **Every written-ahead day's hub and `CHECKLIST.md` carry the tickable `ERRORS.md` re-read**
  before `done N`.
- **Gate days are still rehearsals when written ahead** (ADR-0005), and day 40 — the phase 2 gate
  — is *not* in this batch. The batch stops at 36, four days short of it, so the gate can still be
  written with more of the phase's errors in hand if the tool survives that long.

## Options considered

| Option | Why not |
| --- | --- |
| **Refuse, and write nothing until day 6 is closed** | The honest reading of ADR-0005's warning, taken literally. It protects a rule that is already gone in practice, and its cost is falling on the wrong side of the risk: if the tool goes away, the learner has 26 days of curriculum instead of 36, and nothing about days 2–26 gets better for the refusal. |
| **Write the batch and say nothing about the warning** | The cheapest and the worst. The repository's only real asset is that it records its own deviations. An unrecorded third widening turns every earlier ADR into decoration. |
| **Write all of phase 2, days 27–40, in one batch** | Drops the cap, which is the last thing keeping this a decision, and pulls the phase 2 gate into a batch written with one day of errors behind it. ADR-0005 wrote the gate exception for a gate that would otherwise never exist; day 40 is not in that position yet. |
| **Keep the ten-day cap but delete the "exceptional" framing entirely** | Close to what is decided here, but going further — dropping the per-batch ADR — would remove the argument step. The point of the cap is that somebody has to write down why, each time. |
| **Loosen the order guard in `granth.py`** | Same answer as ADR-0003, ADR-0004 and ADR-0005. The guard is right for *doing*. The exception is for *writing*, and it belongs in an ADR. |

## Consequences

- **Better:** days 27–36 exist. Phase 2 is written as far as day 36 and survives the subscription
  ending. The plan's §9 now describes what actually happens instead of an exception that has
  swallowed its rule.
- **Worse:** ten more days of deliberate-failure parts rest on common beginner errors. The
  `ERRORS.md` re-read before each `done N` is now carrying thirty-five days of repair work, and it
  is a checkbox, not a guarantee.
- **Worse:** writing ahead is now the normal mode of this repository, and this ADR says so. If a
  fourth batch is asked for before a single day is closed, the question to ask is no longer "may
  we write ahead?" but "is anybody doing the days?" — and that question belongs to the learner,
  not to another ADR.
- **Unchanged:** `python granth.py done N` refuses out of order and refuses an unticked checklist.
  A day with no `PROGRESS.md` row is not finished, however complete its folder looks. The phase 2
  gate, day 40, is still unwritten.
