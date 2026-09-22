# ADR-0003 — Days are written ahead in batches of up to five, and are still done one at a time, in order

- **Date:** 2026-09-22
- **Day:** between days 1 and 2
- **Phase:** 1
- **Status:** accepted
- **Amends:** v1.0.0 → v1.1.0, §9 (the order rule) and §12 (two new subsections, see `docs/CHANGELOG_PLAN.md`)
- **Related:** ADR-0001, ADR-0002

## Context

The plan's §9 and `CLAUDE.md` say a day is written only when every earlier day has a row in
`docs/PROGRESS.md`. `python granth.py brief N` enforces it: it exits non-zero when day N−1 is not
in the ledger. The rule exists so that day N is written with day N−1's real errors in front of
the writer — the last twenty rows of `docs/ERRORS.md` are meant to shape the next day's
deliberate-failure parts.

On 2026-09-22 the learner finished day 1 and asked for the next five days in one go. The reason is
practical: the learner wants to open the repository each morning and find the day already there,
without a writing session standing between them and the recorder. Writing one day at a time means
a writing turn every single day, and a day with nobody to write it is a day not done.

The cost of writing ahead is real and should be named: days 3–6 are written without seeing the
learner's actual day 2–5 errors, so their deliberate-failure parts rest on what beginners commonly
do, not on what this beginner did.

## Decision

**Days may be written ahead in batches of up to five. They are still done one at a time, in
order, and each is closed with its own `python granth.py done N` and its own commit.**

- A batch is written only from the last closed day forward, with no gap: if day N is the last
  row in `PROGRESS.md`, the batch is N+1 … N+5 at most.
- `brief` is run for the first day of the batch only; for the rest, the writer reads the plan's
  §8 row directly and says so in the hub's §8.
- A batch-written day's deliberate-failure parts say plainly that they rest on common beginner
  errors, not on this learner's ledger. When the learner's `ERRORS.md` rows for the earlier days
  exist and disagree, the day is amended before it is done, not after.
- Written-ahead days carry `status: written` until their own `done N`. The order guard on `done`
  is untouched: day 4 cannot be closed before day 3 has its row.
- The `PROGRESS.md` rule is unchanged: a day with no row is not finished, however complete its
  folder looks.

The load-bearing half is *done in order, one commit each*. Writing ahead changes when the
documents exist; it changes nothing about when a day counts.

## Options considered

| Option | Why not |
| --- | --- |
| **Keep writing one day at a time (the status quo)** | Correct in principle, but it makes every morning depend on a writing turn. Days not written are days not done, and the learner asked for the opposite. |
| **Write the whole phase (20 days) ahead** | Day 20 written on day 1 would ignore nineteen days of real errors. Five is the longest run that can be amended cheaply when the ledger disagrees with it. |
| **Loosen `brief`'s order guard in `granth.py`** | Touches the toolchain for a workflow choice. The guard is right for *doing*; the exception is for *writing*, and it is recorded here instead. |
| **Merge five days into one document set** | Forbidden outright by §9 and §11: a day is a unit of subject, and merging is what the day format exists to prevent. |

## Consequences

- **Better:** the next day always exists. The learner never waits.
- **Worse:** days 3–6 are written blind to days 2–5's real errors. Their failure parts are
  generic by construction, and each says so.
- **New failure mode:** a written-ahead day drifts from what the learner actually needs, and
  nobody re-reads it before it is done. What catches it: the rule above that `ERRORS.md` rows
  from the earlier days are read before each `done N`, and the day is amended first if they
  disagree.
- **Revisit if:** the learner's ledger shows the generic failure parts missing their real
  mistakes two days running. Then the batch shrinks to two, or to one.
