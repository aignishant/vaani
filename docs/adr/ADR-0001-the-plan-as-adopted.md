# ADR-0001 — The plan as adopted

- **Date:** 2026-09-18
- **Day:** before day 1
- **Phase:** —
- **Status:** accepted
- **Amends:** nothing — this is the founding record
- **Related:** `docs/00_MASTER_PLAN.md` v1.0.0, ADR-0002

## Context

This repository teaches **speaking and writing English from zero, one hour a day, with a
recording and a written piece every day** over 120 days, and it exists because the obvious
alternatives do not work:

- **Following a course** produces something that runs and understanding that evaporates the moment
  the inputs change. There is no artifact to defend and no record of why anything is as it is.
  For a language, "runs" means the learner can repeat the model line and cannot say their own.
- **Reading a grammar book** covers the surface in the order the book was written, which is the
  grammarian's order and not a speaker's. Nothing forces the learner to open their mouth.
- **Practising with no plan** teaches whatever came up, leaves the gaps invisible, and cannot
  tell a sound the learner has mastered from one they have never tried.

The plan answers all three: a fixed day-to-concept map, so gaps are visible; two artifacts, so
every concept is load-bearing; and a depth contract, so a subject is either covered properly or
mechanically flagged as not covered at all.

The learner is a complete beginner with one hour a day, and asked for the speaking and writing
halves to be separate courses inside one repository. That last request is structural and gets its
own record, ADR-0002.

The decisions below were taken at the start, together, because each is expensive to change once
days exist.

## Decision

**v1.0.0 of `docs/00_MASTER_PLAN.md` is adopted as the single source of truth.** In particular:

| Decision | As adopted | Why this and not the alternative |
| --- | --- | --- |
| **Scope** | 120 days, 6 phases, 240 concept IDs across 4 tracks | A beginner reaching a held conversation and a full essay needs the past, the future, opinion, formal register and fluency work, each of which is a phase of its own. Sixty days would drop formal English or fluency; ninety would drop one of the two. Every day closes exactly two IDs, one per folder, so 240 is 120 speaking-side and 120 writing-side concepts, not padding. |
| **The artifact** | A Speaking Portfolio of dated recordings ending in an unscripted talk and a recorded conversation, and a Writing Portfolio of dated pieces ending in a full essay | One artifact per folder makes Principle 4 checkable in each: delete a concept and see whether the gate piece still works. |
| **Day format** | A hub plus one document per subtopic (plan §11), with exactly two sections per day: `01-speaking/` and `02-writing/` | A single-file day silently becomes a wall of text under one heading. A reader cannot revisit one idea without re-reading four, and nothing distinguishes a thin subtopic from a missing one. The two-section rule is ADR-0002. |
| **No clocks** | No duration, estimate or pace in any document (Principle 11); the one-hour budget lives in plan §4 only | A duration field silently authorises the worst edit in technical writing: cutting an explanation because the day is running long. |
| **Verification** | Rules and citations looked up live, with dated ledger rows (Principle 6); `require_sources` is off because the course teaches rules, not documents | Notes written from memory rot silently. A citation written from memory rots most silently of all. |
| **Constraints** | A phone recorder, a notebook, a mirror; nothing bought; no code; audio gitignored, writing committed | A constraint written down is a curriculum. A constraint discovered on day 40 is a rewrite. |
| **Numbering** | Days start at 1 | There is no setup day. Day 1 records a sound and writes a name; a setup day that closed no IDs would make every later count wrong for nothing. |

## Options considered

| Option | Why not |
| --- | --- |
| **No plan — practise and see what comes up** | Teaches whatever the day happened to need. Gaps stay invisible, and there is no way to tell a sound covered thinly from one skipped entirely. |
| **A topic list instead of a day map** | A list has no order and no gate, so nothing ever has to work. The day map is what makes "am I allowed to start day 27?" a mechanical question. |
| **One file per day** | The format this plan explicitly replaces — see the day-format row above. |
| **A shorter curriculum** | Fewer days helps only if the subject is smaller. Trimming days without trimming scope is Principle 11's failure mode with extra steps. |
| **A test-prep course** | The gates would become band scores, which a stranger cannot check by listening or reading. Rejected as a stated non-goal (plan §1.1). |

## Consequences

- **Better:** every concept has exactly one address; a thin day is visible from the tracker alone;
  the repository can be picked up after three weeks away, because the last ledger row says where
  we are.
- **Worse:** the format has real overhead. Eleven sections per part, six parts per day, is a lot
  of structure, and some days will be slower to write than the subject strictly requires.
- **New failure mode:** the generated indexes can go stale and start disagreeing with the days.
  Caught by `python granth.py check`, which fails if any generated document is out of date.
- **Revisit if:** the eleven-section contract starts producing padding — sections filled to satisfy
  the checker rather than the reader. That is a signal the contract is wrong for this subject, and
  it gets its own ADR rather than a quiet exception.
