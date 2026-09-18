---
day: NN
phase: P
phase_name: "<the phase theme, from the plan's §7>"
title: "<speaking subject> · <writing subject>"
ids: [SPK-00, WRT-00]
kind: concept            # concept | mechanism | gate
plan_version: "v1.0.0"
parts: 0                 # must equal the number of documents in parts/ — usually 6
generated: "YYYY-MM-DD"
status: draft            # draft | written | complete
commit: ""               # filled in by the ledger row, after the commit exists
---

<!--
  THE HUB ORIENTS AND ASSEMBLES. IT NEVER TEACHES.

  No rule is explained in this file. No duration, estimate or pace anywhere. The two folders are
  separate courses: this hub introduces both, and never says one depends on the other.

  Eleven numbered sections, in order. Delete every one of these comments before finishing.
-->

> **Yesterday:** <what day N-1 left you holding — one clause for speaking, one for writing.>
> **Today:** <the one sentence version of this day.>
> **Tomorrow:** <what this unlocks.>

## §1 Where we are

<!-- A scene and an analogy. Plain language, NO JARGON. The only place in the day that is allowed
     to be purely orienting. One short paragraph for the speaking folder, one for the writing
     folder. They may use different scenes. -->

## §2 The map

<!-- Two tables. One line above each saying what that folder is about today. No minutes column,
     ever. -->

### Speaking — `parts/01-speaking/`

<!-- one line: what the speaking folder teaches today, and the ID it closes -->

| Part | Title | What it answers | Level |
| --- | --- | --- | --- |
| [1.1](parts/01-speaking/1.1-<slug>.md) | <the rule> | <the question> | foundation |
| [1.2](parts/01-speaking/1.2-<slug>.md) | <the rep> | <the question> | working |
| [1.3](parts/01-speaking/1.3-<slug>.md) | <the deliberate failure> | <the question> | production |

### Writing — `parts/02-writing/`

<!-- one line: what the writing folder teaches today, and the ID it closes -->

| Part | Title | What it answers | Level |
| --- | --- | --- | --- |
| [2.1](parts/02-writing/2.1-<slug>.md) | <the rule> | <the question> | foundation |
| [2.2](parts/02-writing/2.2-<slug>.md) | <the rep> | <the question> | working |
| [2.3](parts/02-writing/2.3-<slug>.md) | <the deliberate failure> | <the question> | production |

<!-- If the day has sources/ (rare), add this table and mark it read-after-the-parts. -->

## §3 Setup

<!-- What to have ready. Your phone's voice recorder. A notebook and a pen, or a text editor. A
     mirror for the sound days. And the one thing this day needs: a photo, a menu, a bill. -->

## §4 Build brief

<!-- The two reps of the day. Leave every `TODO(me)` UNSOLVED — teach, do not do the reps. -->

| Folder | What you make | Where it goes |
| --- | --- | --- |
| Speaking | `TODO(me)`: <the recording — what you say, about your own life> | `lab/speaking/day-NN.<ext>` |
| Writing | `TODO(me)`: <the page — what you write, about your own life> | `lab/writing/day-NN.md` |

## §5 The check that must be able to fail

<!-- Listen back once. Read back once. The one thing a stranger would catch. State how to make it
     go red on purpose — say the wrong version, write the wrong version, and confirm you can hear
     or see the difference. -->

## §6 Budget

<!-- What this day spends against the plan's §4. Usually: one recording, one page, nothing
     bought. State it. -->

## §7 Traps

<!-- The mistakes that eat an evening: the sound your first language does not have, the rule that
     is backwards from your language, the spelling that lies about the sound. -->

## §8 Verify before you build

<!-- The reference pages actually opened TODAY, and what each one confirmed. Never from memory. -->

| What | Where it was checked | Date | What it confirmed |
| --- | --- | --- | --- |

## §9 Say it out loud

<!-- One paragraph, spoken voice — what you would tell a friend who asked what you learned today
     and why it matters. -->

## §10 Done when

See [`CHECKLIST.md`](CHECKLIST.md). Defined by a recording that exists and a page that exists,
never by effort spent.

## §11 Ledger & commit

<!-- The verbatim rows to paste, and the commit message. The hub ends here. -->

**`docs/PROGRESS.md`:**

```text
| NN | YYYY-MM-DD | SPK-00, WRT-00 | 6 | <hash> | yes |
```

**`docs/GLOSSARY.md`** — one row per term this day defined for the first time:

```text
| <term> | <plain-language definition> | day NN part S.T | <also called> |
```

**`docs/ERRORS.md`** — one row per mistake caught on listening back or reading back:

```text
| NN | speaking | <what you said> | <what it should have been> | listen-back |
| NN | writing | <what you wrote> | <what it should have been> | read-back |
```

<!-- On a gate day, add the RECORDINGS.md and WRITINGS.md rows here. -->

**Commit:**

```text
day NN: <title> — closes SPK-00, WRT-00
```
