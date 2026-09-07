---
name: day-speak
description: Write one day of the Vaani English speaking curriculum. Use when the learner asks to write, generate, or start day N, or invokes /day-speak N. Produces a hub, one part document (two on rehearsal days), and a checklist, all conforming to the depth contract in docs/00_MASTER_PLAN.md §11.
---

# day-speak — write one day of Vaani

## Before anything

1. Read `CLAUDE.md`. The ten hard rules apply to everything below.
2. Read `docs/00_MASTER_PLAN.md` §8 and find day N's row: its title, its concept IDs, its track.
3. Read the last row of `docs/PROGRESS.md`. **If day N−1 has no row, stop.** Say which day is
   actually next. Do not write ahead.
4. Read `docs/CHUNKS.md`. Any phrase already there **is not taught again** — cite the day that
   taught it and move on.
5. If day N ≥ 37, skim `docs/ERRORS.md`. Where the learner's own recurring errors touch today's
   concept, the `When it breaks in the wild` section addresses theirs, not a generic one.

## Announce before you write

Print the planned part list — the part title and its four to six chunk phrases — and wait.

> Day 26 · `PR-11` · Intonation 1: the fall, the rise, and the question that isn't
> Part 01 — *Where your voice goes at the end*
> Chunks: rising tag · falling statement · the checking rise · "…right?" · "…isn't it?"

If it looks thin, the learner says so now. That conversation costs one message here and a
rewritten day later.

## What you write

```
days/day-NN-<slug>/
├── LESSON.md
├── CHECKLIST.md
├── parts/
│   └── 01-<slug>.md        one. two only on a rehearsal day. never three.
└── audio/.gitkeep
```

Slug: lowercase, hyphens, from the plan title. `day-26-intonation-the-fall-and-the-rise`.

### The hub — `LESSON.md`

Copy `days/_TEMPLATES/LESSON.md`. It carries:

- day number, title, concept IDs, phase — **IDs verbatim from plan §8**
- one sentence on why this day exists, in terms of the portfolio
- the part list, in reading order, as links
- the build brief: what today contributes to the portfolio, or "no portfolio contribution today"
- the `PROGRESS.md` row, pre-filled except for the outcome

**The hub never teaches.** If you catch yourself explaining in it, that paragraph belongs in the
part.

### The part — `parts/01-<slug>.md`

Copy `days/_TEMPLATES/PART.md`. Seven sections, this order, no exceptions:

| Section | What goes in it |
| --- | --- |
| **The one-line answer** | One sentence. Before any explanation. |
| **The model** | What a fluent speaker actually does. Model lines as blockquotes. The phrase bank: six to ten chunks, no more. |
| **Say it now** | The scripted drill. Fixed lines, repeated. |
| **Say it yours** | The unscripted rep. A prompt, no script, recorder on, named audio file. |
| **The deliberate failure** | The rep built to break, and what breaking sounds like. |
| **When it breaks in the wild** | The real situation where this collapses, and the repair line. |
| **Check yourself** | Listenable pass condition against the recording. |

**`Say it yours` is never optional and is never a written exercise.** It names its own file:
`audio/dNN-free.m4a`. If a day has no recording, that day did not happen.

**`Check yourself` must be checkable by listening.** Good: "Play it back — did every 'the' in
front of a consonant come out as *thuh*, not *thee*?" Bad: "Do you feel more natural?"

### The checklist — `CHECKLIST.md`

Copy `days/_TEMPLATES/CHECKLIST.md`, then add one line per rep in the part. Every box must be
tickable by the learner alone, from evidence.

## Never

- Write three part documents. **This is the failure the whole format exists to prevent.**
- Put a duration, pace, or "should take" anywhere in `days/`.
- Write code, in any language, for any reason.
- Answer a `Say it yours` prompt. It is theirs.
- Teach a chunk already in `CHUNKS.md`.
- Name a person or a brand.
- Invent a fact, a source, or a statistic. Look it up live, log it in `SOURCES.md` with today's
  date, or leave a `TODO` with the exact thing to check.

## After writing — the depth pass

Walk plan §11, all twelve rules, out loud, and say which pass and which do not. Then fix the
failures before showing anything. **Never present a day and its failures together** — fix first.

The commonest three failures, in order: a `Check yourself` that is a feeling rather than a sound;
a missing deliberate failure; a hub that started teaching.

## Closing a day

The learner closes it, not you. Refuse if:

- `CHECKLIST.md` has an unticked box, or
- the free-rep recording does not exist, or
- the day's new chunks are not appended to `CHUNKS.md`.

State which one, and stop. Then append: the `PROGRESS.md` row, the new `CHUNKS.md` rows, any
`ERRORS.md` rows from the playback, and — on a rehearsal or gate day — the `RECORDINGS.md` row.
