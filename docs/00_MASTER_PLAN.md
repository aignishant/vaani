# Vaani — Master Plan

`plan_version: v1.0.0`

**वाणी** — speech, the voice as it is actually used. Not the language on paper.

---

## 1 · Vision

Seventy-two days that end with you holding a ten-minute unscripted conversation in English
with a stranger, on a topic you did not prepare, without freezing, without translating in your
head, and without apologising for your English.

This is not a grammar course. It is not a vocabulary course. Grammar and vocabulary appear only
where they block the mouth. Every day ends with your own voice recorded.

---

## 2 · The artifact

Everything in this curriculum is tested against one artifact:

> **The Speaking Portfolio** — sixteen recordings, made by you, at fixed points in the plan.
> It opens with your Day 1 baseline and closes with a ten-minute unscripted interview on Day 72.
> Between them sit fourteen rehearsal recordings, each a situation you will actually be in.

The test for whether a concept earns a day is mechanical: **if removing it would not change a
recording in the portfolio, it does not get a day.** That is why there is no day on the past
perfect continuous and there is a day on how to say "sorry, I mean —" without stopping.

---

## 3 · Scope and shape

| Decision | Value |
| --- | --- |
| Days | 72 |
| Rhythm | six days on, one day off — twelve weeks |
| Documents per day | one hub + one part. Rehearsal days: one hub + two parts. **Ceiling, not a target.** |
| Session budget | one sitting, roughly half an hour — see §4 |
| Code | none, anywhere |
| Cost | none — a phone voice recorder and a wall are the whole toolchain |
| Partner required | no. Every rep has a solo form and a partner form. |

**Why 72 and not 100.** Eighty concepts, one or two per day, with fourteen days reserved for
rehearsal and three for gates. A hundred-day plan for eighty concepts produces padding, and
padding is what kills these projects in week three.

---

## 4 · The session rig

Every day is the same five blocks in the same order. This is the **only** place in this
curriculum where duration appears. No day document carries a clock, a pace, or an estimate — see
`docs/adr/0002-fixed-session-rig.md` for why.

| Block | What happens | Rough share |
| --- | --- | --- |
| **Warm-up** | Shadow yesterday's model audio. Mouth first, brain second. | ~5 min |
| **Study** | Read the day's one part document. Once, out loud. | ~7 min |
| **Drill** | The scripted reps in that document. Repeat until smooth. | ~8 min |
| **Free rep** | The unscripted rep. **Recorded, always.** | ~8 min |
| **Log** | One row in `PROGRESS.md`. One line in `ERRORS.md` if you caught yourself. | ~2 min |

If a day runs long, it runs long. Nothing is ever cut to fit the rig. If a day is consistently
running double, the day is too fat and gets split — that is an amendment, not a rushed session.

**The rig is the practice.** The reading is the smallest block on purpose. A day where you read
well and spoke little is a failed day even if you understood everything.

---

## 5 · Principles

**Your mouth is a muscle, not a database.** Knowing a phrase and being able to say it at speed
under mild social pressure are different skills. This plan trains only the second. Every part
document ends in your voice, not in your understanding.

**Record or it did not happen.** The free rep is recorded every single day. Not for anyone else.
Recording is the only way you hear the gap between the sentence you meant and the sentence you
made — and that gap is the entire curriculum.

**Errors are the asset.** `docs/ERRORS.md` is append-only and is the most valuable file here.
By Day 67 you will read it and find that four errors account for most of what goes wrong. Those
four get their own days at the end, chosen by the evidence rather than by a syllabus.

**Chunks, not words.** English is spoken in prefabricated blocks. "To be honest with you", "the
thing is", "I was just about to —". A speaker with three hundred chunks outruns a speaker with
three thousand isolated words, every time.

**Fluency before accuracy, then accuracy on top.** Phases 1 and 2 forgive errors and punish
silence. Phase 3 starts repairing. Phase 4 polishes. Reversing this order produces a person who
speaks correctly and rarely.

**One deliberate failure a day.** Every day contains a rep designed to break — speak too fast,
attempt the sound you cannot make, answer the question you have no answer to. A skill nobody has
watched fail has not been located yet.

**No streaks, no shame.** Miss a day and nothing happens. There is no counter. Day 34 is still
next.

---

## 6 · Tracks

| ID | Track | What it covers |
| --- | --- | --- |
| `PR` | Pronunciation & Prosody | Vowels, consonants, stress, rhythm, linking, intonation |
| `FL` | Fluency & Flow | Speed, pausing, chunking, not stopping, escape hatches |
| `FN` | Functions & Formulas | The phrase sets for real situations |
| `IN` | Interaction | Turn-taking, listening, repair, group dynamics |
| `CF` | Confidence & Correction | Recording, transcript review, nerves, self-monitoring |

Every concept has exactly one ID and is taught on exactly one day. Later days cite it; no day
teaches it twice.

---

## 7 · Phases and gates

A phase gate is a recording. You do not proceed on a calendar; you proceed on a gate.

| Phase | Days | Name | Gate |
| --- | --- | --- | --- |
| 1 | 1–18 | **Unblocking** | A 90-second unscripted monologue with no more than three freezes |
| 2 | 19–36 | **The Toolkit** | Six everyday situations, unscripted, back to back |
| 3 | 37–54 | **Interaction** | An eight-minute unscripted two-way conversation |
| 4 | 55–72 | **Performance** | A ten-minute unscripted interview, plus the assembled portfolio |

**A failed gate is not a restart.** It names the two or three days to re-run, and those re-runs
go in `PROGRESS.md` as their own rows. A gate you passed on the second attempt is a better
record than one you passed on the first.

---

## 8 · The day map

<!-- granth:day-map:start -->

### Phase 1 — Unblocking (Days 1–18)

*Goal: the silence breaks. Accuracy is explicitly not the target.*

| Day | Title | IDs | Track |
| --- | --- | --- | --- |
| 1 | Baseline, the recorder, and the log | CF-01, CF-02 | CF |
| 2 | The short vowels, and why they collide | PR-01 | PR |
| 3 | Shadowing: speaking before understanding | PR-02, FL-01 | PR/FL |
| 4 | Chunks, not words | FL-02 | FL |
| 5 | The 4/3/2 rep: the same story, faster | FL-03 | FL |
| 6 | **Rehearsal** — sixty seconds about yourself | CF-03 | CF |
| 7 | Long vowels and the length contrast | PR-03 | PR |
| 8 | Word stress: the one syllable that carries the word | PR-04 | PR |
| 9 | Buying time: hesitation that sounds fluent | FL-04, FN-01 | FL/FN |
| 10 | Your routine, out loud, without notes | FN-02 | FN |
| 11 | Consonant clusters, and the vowel you sneak in | PR-05 | PR |
| 12 | **Rehearsal** — ninety seconds: a day in your life | CF-04 | CF |
| 13 | Sentence stress: which words get hit | PR-06 | PR |
| 14 | Telling what happened, and the -ed trap | PR-07, FN-03 | PR/FN |
| 15 | Linking: where one word runs into the next | PR-08 | PR |
| 16 | Asking out loud: the six question shapes | IN-01 | IN |
| 17 | Correcting yourself without stopping | CF-05, FL-05 | CF/FL |
| 18 | **Gate 1** — ninety seconds unscripted, against the baseline | CF-06 | CF |

### Phase 2 — The Toolkit (Days 19–36)

*Goal: the phrase for the situation arrives before you have to think about it.*

| Day | Title | IDs | Track |
| --- | --- | --- | --- |
| 19 | Ordering, buying, asking for things | FN-04 | FN |
| 20 | The schwa: the sound that does most of the work | PR-09 | PR |
| 21 | Directions and describing a place | FN-05 | FN |
| 22 | Weak forms and contractions: gonna, wanna, 'ave | PR-10 | PR |
| 23 | Describing people and things at speed | FN-06 | FN |
| 24 | **Rehearsal** — three counter-service roleplays | CF-07 | CF |
| 25 | Plans, intentions, and decisions made just now | FN-07 | FN |
| 26 | Intonation 1: the fall, the rise, and the question that isn't | PR-11 | PR |
| 27 | Saying what you think, and softening it | FN-08 | FN |
| 28 | Agreeing, half-agreeing, disagreeing | FN-09, IN-02 | FN/IN |
| 29 | The sounds your first language did not give you | PR-12 | PR |
| 30 | **Rehearsal** — a three-minute opinion exchange | CF-08 | CF |
| 31 | Requests, and saying no without damage | FN-10 | FN |
| 32 | Small talk: opener, bridge, exit | IN-03 | IN |
| 33 | Comparing, choosing, recommending | FN-11 | FN |
| 34 | The phrasal verbs you cannot avoid | FN-12 | FN |
| 35 | The two-minute anecdote with a point | FN-13 | FN |
| 36 | **Gate 2** — six situations, unscripted, back to back | CF-09 | CF |

### Phase 3 — Interaction (Days 37–54)

*Goal: another person is talking, and that stops being an emergency.*

| Day | Title | IDs | Track |
| --- | --- | --- | --- |
| 37 | Listening for the gist while your reply is loading | IN-04 | IN |
| 38 | Taking the floor, and holding it | IN-05 | IN |
| 39 | Repair: "sorry, I mean —" and asking for a repeat | IN-06 | IN |
| 40 | Interrupting, and being interrupted | IN-07 | IN |
| 41 | Intonation 2: interest, doubt, surprise, sarcasm | PR-13 | PR |
| 42 | **Rehearsal** — a five-minute two-way conversation | CF-10 | CF |
| 43 | Follow-up questions that keep it alive | IN-08 | IN |
| 44 | Saying it a second way when the first way failed | FL-06 | FL |
| 45 | Pausing on purpose, and the myth of speed | PR-14, FL-07 | PR/FL |
| 46 | Phone calls and voice notes: no face to read | IN-09 | IN |
| 47 | Explaining something complicated, simply | FN-14 | FN |
| 48 | **Rehearsal** — explain your work to a stranger | CF-11 | CF |
| 49 | When they misunderstood you, and when you misunderstood them | IN-10 | IN |
| 50 | Story shape: setup, turn, point | FN-15 | FN |
| 51 | Register: the same sentence, casual and formal | IN-11 | IN |
| 52 | The escape hatch: when the word will not come | FL-08 | FL |
| 53 | Three or more voices: getting in and staying in | IN-12 | IN |
| 54 | **Gate 3** — an eight-minute unscripted conversation | CF-12 | CF |

### Phase 4 — Performance (Days 55–72)

*Goal: it holds up when it matters and someone is judging.*

| Day | Title | IDs | Track |
| --- | --- | --- | --- |
| 55 | Meetings: the update, the blocker, the ask | FN-16 | FN |
| 56 | Disagreeing in a room without burning it | IN-13 | IN |
| 57 | Presenting 1: structure and signposting | FN-17 | FN |
| 58 | Presenting 2: pace, volume, and the eyes | PR-15 | PR |
| 59 | The question you cannot answer | IN-14 | IN |
| 60 | **Rehearsal** — a four-minute presentation | CF-13 | CF |
| 61 | Interview English: the answer with a shape | FN-18 | FN |
| 62 | Interview English: yourself, without a script | FN-19 | FN |
| 63 | Pushing back and negotiating | IN-15 | IN |
| 64 | Under pressure: what breaks first, and bracing it | PR-16, FL-09 | PR/FL |
| 65 | Accent: what to change, what to keep, what not to chase | PR-17 | PR |
| 66 | **Rehearsal** — a mock interview | CF-14 | CF |
| 67 | Reading your own error ledger: the top four | CF-15 | CF |
| 68 | Killing your top four, out loud | CF-16 | CF |
| 69 | Tired, nervous, bad connection: speaking anyway | FL-10 | FL |
| 70 | The maintenance routine after Day 72 | CF-17 | CF |
| 71 | Portfolio assembly: Day 1 against today | CF-18 | CF |
| 72 | **Gate 4** — ten-minute unscripted interview, and the retrospective | CF-19 | CF |

<!-- granth:day-map:end -->

---

## 9 · Traceability

Eighty concept IDs across five tracks, each assigned to exactly one day above. Two IDs on the
same day is fine; the same ID on two days is a planning bug and gets an amendment.

- `PR-01` … `PR-17` — seventeen
- `FL-01` … `FL-10` — ten
- `FN-01` … `FN-19` — nineteen
- `IN-01` … `IN-15` — fifteen
- `CF-01` … `CF-19` — nineteen

---

## 10 · Anatomy of a day

```
days/day-14-what-happened-and-the-ed-trap/
├── LESSON.md      the hub — orients, assembles, holds the build brief. It never teaches.
├── CHECKLIST.md   the definition of done
├── parts/
│   └── 01-the-ed-trap.md            THE TEACHING — one idea, one document
└── audio/         your recordings — gitignored, they are yours
```

**Rehearsal days carry two part documents.** Every other day carries one. This ceiling is not
advisory; a day that needs three parts is two days.

### The seven sections of a part

In this fixed order, every time:

1. **The one-line answer** — what this is, in a sentence, before any explanation.
2. **The model** — what a fluent speaker actually does. Written as speech, not as a rule.
   Includes the phrase bank for the day, six to ten chunks, no more.
3. **Say it now** — the scripted drill. Fixed sentences, repeated. This is where the mouth
   learns the shape.
4. **Say it yours** — the unscripted rep. A prompt, no script, recorder on. **Every part has
   one.**
5. **The deliberate failure** — the rep built to break, and what breaking sounds like.
6. **When it breaks in the wild** — the real situation where this collapses, and the repair.
7. **Check yourself** — the recorded proof. A specific, listenable pass condition. Never
   "do you feel more confident?"

### The hub

`LESSON.md` orients and assembles. It carries: the day number and IDs, one sentence on why the
day exists, the part list in reading order, the build brief (today's portfolio contribution, if
any), and the `PROGRESS.md` row to paste. **The hub never teaches.** If a hub explains something,
that explanation belongs in a part.

---

## 11 · The depth contract

A day is not finished because it exists. It is finished when it passes all of these. There is no
script to run — this is read and ticked by hand, and the day skill in `.claude/skills/day-speak/`
refuses to close a day without it.

| # | The rule | Why it is here |
| --- | --- | --- |
| 1 | Folder shape and numbering correct, no gaps | A missing part number means a part was planned and dropped |
| 2 | One part document. Two on rehearsal days. Never three. | The stated reason this course exists |
| 3 | All seven sections present, in order | Sections get dropped in exactly the order they are useful |
| 4 | A **Say it yours** rep exists and names a recording file | A day with no recording is reading, not speaking |
| 5 | A **deliberate failure** rep exists | See §5 |
| 6 | Every chunk in the phrase bank is appended to `CHUNKS.md` | Otherwise the same phrase gets taught three times |
| 7 | No clock, no pace, no duration anywhere in the day folder | §4 holds the only budget; a clock in a day licenses cutting the explanation |
| 8 | The hub assembles; it does not teach | A teaching hub means the part is thin |
| 9 | The hub's IDs match §8 of this plan exactly | The only defence against a quietly skipped concept |
| 10 | `Check yourself` is listenable, not felt | "Do you feel confident?" passes on any day, so it checks nothing |
| 11 | No person names, no brand names | Tool categories are fine: "your phone's recorder", not a product |
| 12 | No code, in any document | ADR-0001 |

---

## 12 · Style guide

**Write it as speech.** This curriculum is about the mouth. A part document that reads like a
grammar reference has already lost. Contractions everywhere. Short sentences.

**Model lines are marked and are meant to be said aloud**, formatted as blockquotes, never as
code blocks — there is no code here and a code block invites the eye to skim.

**No jargon without a plain gloss on first use.** "Schwa" is fine once you have said "the lazy
uh sound in the second half of *doctor*."

**One metaphor family per day.** Do not open with a muscle metaphor and close with a software
metaphor.

**Second person, always.** "You" say it. Not "the learner" or "one".

**Never write a rule you cannot hear.** If a rule has no audible consequence, it belongs in a
grammar book, not here.

---

## 13 · Ledgers

All append-only. Nothing in them is ever edited or deleted, including the bad rows.

| File | One row per |
| --- | --- |
| `docs/PROGRESS.md` | completed day — what you did, how the recording sounded, what went wrong |
| `docs/ERRORS.md` | error caught in your own recording, with the date and the day |
| `docs/CHUNKS.md` | phrase taught, defined once, with the day that taught it |
| `docs/RECORDINGS.md` | portfolio recording, with the date and what it was |
| `docs/SOURCES.md` | any external source used, with the date checked |
| `docs/CHANGELOG_PLAN.md` | amendment to this plan |
| `docs/adr/` | structural decision, never rewritten |

`ERRORS.md` is the one that earns its keep. Days 67 and 68 are written from it and cannot be
written without it.

---

## 14 · Amending this plan

Reality moves — you discover the sound you cannot make is not the one you expected, or a phase
takes longer. The order is fixed:

**Verify what actually changed → state the cost → write an ADR if the day map shifts → edit this
plan and bump `plan_version` → append to `CHANGELOG_PLAN.md` → only then touch days.**

Adding days at the end is cheap. Inserting a day in the middle renumbers everything after it,
which is exactly why it needs a written decision first.
