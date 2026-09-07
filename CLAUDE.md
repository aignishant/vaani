# CLAUDE.md — operating rules for Vaani

Read this before touching anything. Then read `docs/00_MASTER_PLAN.md`.

---

## What this repository is

A 72-day English **speaking** curriculum. Practice-first. The learner records their voice every
single day. The output is a Speaking Portfolio of sixteen recordings, ending in a ten-minute
unscripted interview.

**This is not a coding project.** There is no source code, no toolchain, no tests, no scripts.
If you find yourself about to write a script, a checker, or a snippet in any language — stop.
That is ADR-0001 and it is not negotiable.

---

## The hard rules

1. **No code.** Not in day documents, not as a helper, not "just a small script".
2. **One part document per day.** Two on rehearsal days. **Never three.** This ceiling is the
   reason the learner chose this format over a hundred-day plan with twenty documents a day.
   Violating it is the worst thing you can do here.
3. **No clocks.** No "5 minutes", no "this should take", no pace, no estimate — anywhere in
   `days/`. §4 of the plan carries the only session budget in the whole repository.
4. **Every part ends in the learner's voice.** A `Say it yours` rep with the recorder on. A part
   that only explains has failed the contract.
5. **Every day has one deliberate failure** — a rep built to break.
6. **No person names, no brand names.** Say "your phone's voice recorder", not a product.
7. **Never invent a fact.** If you cite anything external, look it up live and append a dated
   row to `docs/SOURCES.md`. A failed lookup leaves a `TODO`, never a guess.
8. **Ledgers are append-only.** Never edit or delete a row in `docs/PROGRESS.md`,
   `docs/ERRORS.md`, `docs/CHUNKS.md`, `docs/RECORDINGS.md`, `docs/SOURCES.md`,
   `docs/CHANGELOG_PLAN.md`, or anything in `docs/adr/`. The bad rows stay.
9. **Never solve the learner's reps.** Prompts are prompts. If you write the answer, they read
   instead of speak.
10. **Days go in order.** Before writing day N, check that days up to N−1 have rows in
    `PROGRESS.md`. If they do not, say so and stop. Skipping needs an ADR.

---

## The daily loop

The learner does this. You do step 2 and help with step 5.

1. **Brief** — read `docs/00_MASTER_PLAN.md` §8 for day N's title and IDs, and the last row of
   `docs/PROGRESS.md` to confirm N is next.
2. **Write the day** — `/day-speak N`. See `.claude/skills/day-speak/SKILL.md`.
3. **Do the work** — the five blocks of the session rig. Recorder on for the free rep.
4. **Listen back** — one pass. Append anything caught to `docs/ERRORS.md`.
5. **Close** — tick `CHECKLIST.md`, append the `PROGRESS.md` row, append new chunks to
   `CHUNKS.md`. If a rehearsal day, append to `RECORDINGS.md`.

**Closing a day is refused** if the checklist is unticked, the recording does not exist, or the
new chunks are not in `CHUNKS.md`. Refusing is the point — it is the only thing between the
learner and a repository of days that look finished.

---

## Writing style

Write as speech, not as reference. Contractions. Short sentences. Second person. One metaphor
family per day. Model lines are blockquotes, never code blocks. Full style guide: plan §12.

**Never write a rule the learner cannot hear.** If a rule has no audible consequence, it does
not belong here.

---

## Repository map

```
CLAUDE.md                     this file
README.md
docs/00_MASTER_PLAN.md        THE CONTRACT — day map §8, depth contract §11, style §12
docs/PROGRESS.md              append-only · one row per completed day
docs/ERRORS.md                append-only · the most valuable file here
docs/CHUNKS.md                append-only · every phrase, taught once
docs/RECORDINGS.md            append-only · the portfolio index
docs/SOURCES.md               append-only · anything cited, with the date checked
docs/CHANGELOG_PLAN.md        append-only · every amendment
docs/adr/                     one file per structural decision, never rewritten
days/_TEMPLATES/              blank hub, checklist, part
days/day-NN-<slug>/           the days
.claude/skills/day-speak/     the day-writing skill
```

---

## When the learner is stuck

Reasonable and expected. The three fixes, in order:

1. **A day feels too hard** → it is probably two days. Split it, write the ADR, amend the plan.
2. **A gate fails** → that is the gate working. Name two or three days to re-run. Re-runs get
   their own `PROGRESS.md` rows.
3. **Days were missed** → nothing happens. There are no streaks and no counters. The next day
   is still the next day.

Never suggest they "catch up" by doubling. Two days in one sitting is one day of speaking and
one day of reading.
