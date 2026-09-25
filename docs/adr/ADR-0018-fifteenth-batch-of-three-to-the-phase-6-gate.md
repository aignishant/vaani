# ADR-0018 — A fifteenth batch of three, days 118–120, ending on the phase 6 gate as a rehearsal

- **Date:** 2026-09-25
- **Day:** between days 1 and 2 (days 2–117 written, none done)
- **Phase:** 6
- **Status:** accepted
- **Amends:** v1.15.0 → v1.16.0, §9 (the writing-ahead rule), §13
- **Related:** ADR-0003, ADR-0004, ADR-0005, ADR-0006, ADR-0007, ADR-0013, ADR-0015, ADR-0017

## Context

ADR-0017 authorised days 116–117 and closed with two sentences that bind this one:

> Day 118 onward needs either a closed day 6 in `docs/PROGRESS.md` or a further ADR, and the
> question is asked out loud again first. **Three days after this batch is the gate.** A batch from
> day 118 that runs to day 120 has to write the gate day inside it, as a rehearsal, under §9's gate
> rule.

The learner asked for "next 10 days doc". Five facts were true at that moment.

**Only three days are left.** The plan is 120 days. Days 2–117 were written. A batch of ten is not
possible; the most any batch can now be is days 118–120.

**The ledger has not moved.** `docs/PROGRESS.md` still holds one row, day 1.
`python granth.py brief 116` exited non-zero with "day 2 is next".

**The fourteenth batch was whole but not committed.** On 2026-09-25, `python granth.py depth 116`
and `python granth.py depth 117` passed. `python granth.py check` failed only because the generated
indexes were stale; after `python granth.py index` it passed.

**The question was asked first.** The §9 question was put to the learner in the words §9 requires,
before anything was written: *is anybody doing the days?* It said that the course ends at day 120,
so only days 118–120 remain; that `PROGRESS.md` holds only day 1; that days 116–117 were
uncommitted; and that day 120 is the phase 6 gate and would be written as a rehearsal. It came with
three options: commit days 116–117 and write nothing new (recommended); commit and then write days
118–120; or leave everything as it is. **The learner chose to commit and then write days 118–120.**
Days 116–117 were committed (`33149e6`) before anything in this batch was written.

**Earlier days already teach part of what this batch names.** Day 99 teaches the shape of a full
talk. Day 101 teaches speaking from English you own and the drawn topic. Days 115–116 teach the
long conversation. Day 113 teaches the proofreading checklist. Days 115–116 teach the first and
second drafts. Day 117 teaches the portfolio retake and the assembled index. The days in this batch
build on those and link back to them. They don't teach them again.

## Decision

**A fifteenth batch of three days, 118–120, is written ahead from the last written day.** It is
under the cap of ten. It ends on the phase 6 gate, and so on the last day of the course.

- **Days 118 and 119 are concept days.** Each closes two IDs and teaches a rule.
- **Day 120 is the phase 6 gate, written ahead as a rehearsal** under §9's gate rule (ADR-0005). It
  teaches no new rule. It points at the gate wording in §7 and never restates it more kindly. Its hub
  and `CHECKLIST.md` carry the mandatory, tickable re-read of `docs/ERRORS.md` for days 101 to 119.
  Until that box is ticked, it is a rehearsal and says so.
- **Day 120 reviews pieces made earlier; it never makes them late.** The phase 6 gate names a
  recorded conversation and a proofread essay. Day 119 makes both. If either is missing when day 120
  is reached, the learner goes back to day 119 rather than making it on day 120 and calling it a
  gate piece. Day 120 records the unscripted talk itself.
- **"Both portfolios indexed in full" is checked in both folders, each for its own portfolio.** The
  speaking folder checks `docs/RECORDINGS.md`; the writing folder checks `docs/WRITINGS.md`. Neither
  folder mentions the other (Principle 14).

Every condition set by ADR-0004 to ADR-0017 still applies.

**What is kept:**

- **A batch starts from a clean tree** (ADR-0015). This one did.
- **Every written-ahead part says, in the part, that its wrong version is a common beginner error
  and not this learner's.**
- **Every written-ahead day's hub and `CHECKLIST.md` carry the tickable `ERRORS.md` re-read**
  before `done N`.
- **Old portfolio pieces are never edited or deleted.** A retake or a rewrite is a new file with its
  own row.

**What is new:** the plan is now written to its last day. There is no day 121 and no next batch.
Any further writing is an amendment to a day already written, under Principle 8, never a new day.

## Options considered

| Option | Why not |
| --- | --- |
| **Commit days 116–117 and write nothing new** | Offered as recommended, and declined. It is still the option that would let the gate day be shaped by the learner's real mistakes rather than by generic ones. |
| **Write ten days by adding days 121–127** | Not possible without changing the plan's length, which the learner did not ask for. The course is 120 days; ADR-0001 fixes it. |
| **Write days 118–119 and stop before the gate** | Not offered by name, and not asked for. §9 allows a gate day to be written ahead as a rehearsal, and leaving the last day alone unwritten would gain nothing the re-read box does not already give. |
| **Loosen the order guard in `granth.py`** | Same answer as ADR-0003 to ADR-0017. The guard is right for *doing*. |

## Consequences

- **Better:** the whole course exists on paper. The learner can see day 120 from day 2.
- **Worse:** the last gate of the course is written with one day of real errors behind it. Its check
  lists are generic until the re-read box is ticked, and the re-read covers nineteen days that have
  not happened yet.
- **Unchanged:** `python granth.py done N` refuses out of order and refuses an unticked checklist.
  A day with no `PROGRESS.md` row is not finished, however complete its folder looks. Phase 6 is
  green only when every condition of §9 holds.
