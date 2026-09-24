# ADR-0016 — A thirteenth batch of two, days 114–115, inside phase 6 and crossing no gate

- **Date:** 2026-09-24
- **Day:** between days 1 and 2 (days 2–113 written, none done)
- **Phase:** 6
- **Status:** accepted
- **Amends:** v1.13.0 → v1.14.0, §9 (the writing-ahead rule), §13
- **Related:** ADR-0003, ADR-0004, ADR-0006, ADR-0007, ADR-0015

## Context

ADR-0015 authorised days 112–113 and closed with a sentence that binds this one:

> Day 114 onward needs either a closed day 6 in `docs/PROGRESS.md` or a further ADR, and the
> question is asked out loud again first.

The learner asked for "next 2 days doc". Four facts were true at that moment.

**The ledger has not moved.** `docs/PROGRESS.md` still holds one row, day 1.
`python granth.py brief 112` exited non-zero with "day 2 is next".

**The twelfth batch was whole but not committed.** On 2026-09-24, `python granth.py depth 112`,
`python granth.py depth 113` and `python granth.py check` all passed, but days 112–113 and the
v1.13.0 amendment were on disk uncommitted. ADR-0015 wrote down that a batch starts from a clean
tree.

**The question was asked first.** The §9 question was put to the learner in the words §9 requires,
before anything was written: *is anybody doing the days?* It said that `PROGRESS.md` holds only
day 1, that days 2–113 are written and not done, that day 111 alone has twenty unticked boxes, and
that days 112–113 were uncommitted. It named days 114 and 115 and said neither crosses a gate; the
next gate is day 120. It came with three options: commit days 112–113 and write nothing new
(recommended); commit days 112–113 and then write days 114–115; or leave everything uncommitted.
**The learner chose to commit days 112–113, then write days 114–115.** Days 112–113 were committed
before anything in this batch was written.

**Earlier days already teach part of what this batch names.** Day 20 teaches the one-go take and
retaking only for a reason you can name. Day 29 teaches agreeing and adding one thing. Day 33
teaches follow-up questions from the answering side. Day 38 teaches asking back. Day 78 teaches the
second read. Day 99 teaches the essay plan, and days 101–103 its introduction, body paragraph and
conclusion. The days in this batch build on those and link back to them. They don't teach them
again.

## Decision

**A thirteenth batch of two days, 114–115, is written ahead from the last written day.** It is
under the cap of ten. It crosses no gate and no phase boundary. Day 115 is called a *rehearsal* in
the plan's §8 title, but it is a concept day that closes SPK-91 and WRT-68 and teaches a rule. It
is not a gate day, and the gate rule of §9 does not apply to it.

Every condition set by ADR-0004 to ADR-0015 still applies. Every day between the last closed day
and the last written day is fully written and passes `depth`. Days are still *done* one at a time,
in order, each with its own `done N` and its own commit. `docs/ERRORS.md` is read before each
`done N`, and a day whose failure parts miss the real pattern is amended first.

**What is kept:**

- **The batch closes at its last day.** Day 116 onward needs either a closed day 6 in
  `docs/PROGRESS.md` or a further ADR, and the question is asked out loud again first.
- **A batch starts from a clean tree** (ADR-0015). This batch did.
- **Every written-ahead part says, in the part, that its wrong version is a common beginner error
  and not this learner's.**
- **Every written-ahead day's hub and `CHECKLIST.md` carry the tickable `ERRORS.md` re-read**
  before `done N`.
- **The formal-writing choice from ADR-0011 stands.** The essay leaves out contractions as this
  course's choice.

**What is new:** nothing structural. One point is named rather than hidden: day 114's writing
folder rewrites the day 20 gate page. The day 20 page is **never edited**; the rewrite is a new
file with its own `docs/WRITINGS.md` row, as §3 and that ledger's own header already say.

## Options considered

| Option | Why not |
| --- | --- |
| **Commit days 112–113 and write nothing new** | Offered as recommended, and declined. It is still the option that protects the curriculum from being shaped by errors that have not happened. |
| **Leave everything uncommitted** | Offered, and declined. |
| **Write days 114–120 to the gate** | Not asked for. Six days past this batch include the gate day, which would have to be written inside the batch as a rehearsal; that is a larger decision and gets its own question. |
| **Loosen the order guard in `granth.py`** | Same answer as ADR-0003 to ADR-0015. The guard is right for *doing*. |

## Consequences

- **Better:** the first rehearsal and the first draft exist before the second ones (day 116) are
  written, so the phase 6 run-in reads in order.
- **Worse:** two more days of deliberate-failure parts rest on common beginner errors. Day 114
  asks the learner to listen back to a recording and rewrite a page that do not exist yet.
- **Unchanged:** `python granth.py done N` refuses out of order and refuses an unticked checklist.
  A day with no `PROGRESS.md` row is not finished, however complete its folder looks.
