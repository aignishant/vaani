# ADR-0017 — A fourteenth batch of two, days 116–117, inside phase 6 and crossing no gate

- **Date:** 2026-09-24
- **Day:** between days 1 and 2 (days 2–115 written, none done)
- **Phase:** 6
- **Status:** accepted
- **Amends:** v1.14.0 → v1.15.0, §9 (the writing-ahead rule), §13
- **Related:** ADR-0003, ADR-0004, ADR-0006, ADR-0007, ADR-0015, ADR-0016

## Context

ADR-0016 authorised days 114–115 and closed with a sentence that binds this one:

> Day 116 onward needs either a closed day 6 in `docs/PROGRESS.md` or a further ADR, and the
> question is asked out loud again first.

The learner asked for "next 2 days doc" again. Four facts were true at that moment.

**The ledger has not moved.** `docs/PROGRESS.md` still holds one row, day 1.

**The thirteenth batch was whole.** On 2026-09-24 `python granth.py depth 114`,
`python granth.py depth 115` and `python granth.py check` passed. When the question was asked,
days 114–115 looked uncommitted. By the time the answer came, the learner had committed them
themselves (`fa805fe`), so the tree was already clean and nothing more was committed before this
batch.

**The question was asked first.** The §9 question was put to the learner in the words §9 requires,
before anything was written: *is anybody doing the days?* It said that `PROGRESS.md` holds only
day 1, that days 2–115 are written and not done, and that days 114–115 needed committing first. It
named days 116 and 117 and said neither crosses a gate; the gate is day 120. It came with three
options: commit days 114–115 and write nothing new (recommended); commit and then write days
116–117; or leave everything uncommitted. **The learner chose to commit and then write days
116–117.**

**Earlier days already teach part of what this batch names.** Day 25 teaches holding a phone
call. Day 78 teaches the second read of a page. Day 113 teaches the proofreading checklist. Day 114
teaches listening back to a recording and one fix per retake. Day 115 teaches follow-up questions
and the first draft. The days in this batch build on those and link back to them. They don't teach
them again.

## Decision

**A fourteenth batch of two days, 116–117, is written ahead from the last written day.** It is
under the cap of ten. It crosses no gate and no phase boundary. Day 116 is called a *rehearsal* and
day 117 names the portfolio, but both are concept days that close two IDs and teach a rule. Neither
is a gate day, and neither restates the gate. Day 117's writing folder assembles the portfolio index
that the gate names, and points at the gate wording in §7 rather than repeating it.

Every condition set by ADR-0004 to ADR-0016 still applies.

**What is kept:**

- **The batch closes at its last day.** Day 118 onward needs either a closed day 6 in
  `docs/PROGRESS.md` or a further ADR, and the question is asked out loud again first. **Three
  days after this batch is the gate.** A batch from day 118 that runs to day 120 has to write the
  gate day inside it, as a rehearsal, under §9's gate rule.
- **A batch starts from a clean tree** (ADR-0015).
- **Every written-ahead part says, in the part, that its wrong version is a common beginner error
  and not this learner's.**
- **Every written-ahead day's hub and `CHECKLIST.md` carry the tickable `ERRORS.md` re-read**
  before `done N`.
- **Old portfolio pieces are never edited or deleted.** A retake or a rewrite is a new file with its
  own row (§3; the ledgers' own headers).

**What is new:** nothing structural.

## Options considered

| Option | Why not |
| --- | --- |
| **Commit days 114–115 and write nothing new** | Offered as recommended, and declined. It is still the option that protects the curriculum from being shaped by errors that have not happened. |
| **Leave everything uncommitted** | Offered, and declined. |
| **Write days 116–120 to the gate** | Not asked for. It would pull the gate day into a batch because it was next, which §9 forbids. |
| **Loosen the order guard in `granth.py`** | Same answer as ADR-0003 to ADR-0016. The guard is right for *doing*. |

## Consequences

- **Better:** the second rehearsal, the second draft, the portfolio retake and the assembled index
  exist before the last three days are written.
- **Worse:** day 117 asks the learner to choose the weakest of five gate recordings and to index
  six gate pieces, none of which exist yet.
- **Unchanged:** `python granth.py done N` refuses out of order and refuses an unticked checklist.
  A day with no `PROGRESS.md` row is not finished, however complete its folder looks.
