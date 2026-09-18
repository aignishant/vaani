# ADR-0002 — Every day has two independent folders: speaking and writing

- **Date:** 2026-09-18
- **Day:** before day 1
- **Phase:** —
- **Status:** accepted
- **Amends:** nothing — adopted together with v1.0.0
- **Related:** ADR-0001; plan §6, §11.2, §11.3, Principle 14

## Context

The learner asked for two things that pull against each other. One: a single course, one hour a
day, that teaches both speaking and writing. Two: the speaking and writing halves kept fully
separate — "separate learning, not related to each other" — so that either can be done on its own.

The granth day format is a hub plus `parts/` with numbered sections. Nothing in it says how many
sections a day has or what they are called. Left open, a writer would sometimes make three
sections, sometimes one, and would sooner or later write "as you practised this morning" from a
writing part into a speaking part, because it is the natural thing to do. Once that happens the
two halves are one course again, and the learner cannot skip the writing on a day with no pen.

## Decision

**Every day has exactly two sections, always named `01-speaking/` and `02-writing/`, and neither
links into the other.**

- Section 1 closes the day's `SND` or `SPK` ID and nothing else. Section 2 closes the day's `GRM`
  or `WRT` ID and nothing else. Every day closes exactly two IDs, one per folder (plan §6).
- The day title is two halves joined by ` · `; the folder slug comes from the speaking half.
- A part's `prerequisites`, `prev` and `next` point only inside its own folder, or to the same
  folder on an earlier day. Never across.
- The hub's map is two tables, one per folder, and the build brief names two reps: a recording and
  a page.
- The two folders may use different story families on the same day (§12.2 rule 4). They are
  separate courses; a shared metaphor would be a lean.
- A third section is a plan amendment, not a writer's choice.

The load-bearing half is the *no cross-link* rule. It is what makes "do the speaking folder today
and the writing folder tomorrow" a valid way to use the course, and it is checked by reading,
because no script can tell a helpful back-reference from a lean.

## Options considered

| Option | Why not |
| --- | --- |
| **Leave the section count open** | The status quo of the granth format. Works for a single-subject curriculum; here it would let the two halves merge one back-reference at a time. |
| **Two separate repositories** | Cleanest separation, but two `PROGRESS.md` files, two plans, two rituals, for one learner with one hour. The learner asked for one course. |
| **Alternate days: speaking on odd days, writing on even** | Halves the practice frequency of each skill. Speaking every other day is not speaking every day, and the portfolio would have half the recordings. |
| **Top-level `speaking/` and `writing/` folders inside the day, outside `parts/`** | Bypasses the depth checker entirely; the eleven-section contract would be unenforced on every part. |

## Consequences

- **Better:** the learner can do either folder alone, in any order, on any day. Traceability is
  exact: the speaking IDs and the writing IDs are different prefixes and can be reported apart.
- **Worse:** some rules — contractions, question word order — are genuinely both spoken and
  written, and will be taught twice, once per folder, with different reps. That is a cost paid on
  purpose; the second teaching is a second rep, not a duplicate. The glossary defines the term
  once and both parts link it.
- **New failure mode:** a writer leans across folders without noticing. The checker cannot catch
  it. The day-writing skill's checklist asks for it explicitly, and the audit reads for it first.
- **Revisit if:** the learner finds the two halves so unrelated that the shared phase theme is a
  fiction, or so related that the no-cross-link rule is fighting the subject. Either is a signal
  for a new ADR, not a quiet exception.
