# Vaani

**Speaking and writing English from zero, one hour a day, with a recording and a written piece
every day** — 120 days, 6 phases, 240 concepts, two portfolios.

Vaani (वाणी) means *speech, the voice*. This is a practice-first English course for a complete
beginner. Every day has two folders that stand alone from each other: a **speaking** folder that
ends with your phone's voice recorder on and you saying something that is yours, and a
**writing** folder that ends with your pen on the page. Each folder is three short documents: the
rule, the rep, and a deliberate mistake you make on purpose so you can hear or see what goes
wrong. By day 120 you have a Speaking Portfolio ending in an unscripted talk and a recorded
conversation, and a Writing Portfolio ending in a full essay.

## Where to start

| You want | Open |
| --- | --- |
| The contract everything obeys | [`docs/00_MASTER_PLAN.md`](docs/00_MASTER_PLAN.md) |
| Where the work actually is | [`docs/PROGRESS.md`](docs/PROGRESS.md) — the last row |
| What each day teaches | [`docs/WIKI.md`](docs/WIKI.md) |
| Where a concept is taught | [`docs/CURRICULUM_INDEX.md`](docs/CURRICULUM_INDEX.md) |
| What is written and what is not | [`docs/TRACKER.md`](docs/TRACKER.md) |
| Your own mistakes, dated | [`docs/ERRORS.md`](docs/ERRORS.md) |
| The two portfolios | [`docs/RECORDINGS.md`](docs/RECORDINGS.md) · [`docs/WRITINGS.md`](docs/WRITINGS.md) |
| Why something is the way it is | [`docs/adr/`](docs/adr/) |

## The commands

```bash
python granth.py status        # how many days are complete, and what is next
python granth.py brief N       # what day N must cover, and whether N is allowed yet
python granth.py start N       # open day N in reading order
python granth.py depth N       # check day N against the depth contract
python granth.py check         # the whole-repository gate
python granth.py done N        # finish a day: refuses on an unticked checklist, then commits
python granth.py doctor        # is this repository wired correctly?
```

## How a day is written

A day is a **hub plus one document per subtopic**, never one long page. Every subtopic document
opens where a reader who has never met the rule can stand and ends in real life: what a fluent
speaker does instead, what a native listener notices, what a formal reader forgives and what they
do not.

Three rules make that more than an aspiration:

- **No clocks.** No document carries a duration, an estimate or a pace. The one-hour budget lives
  in the plan's §4 and nowhere else. An explanation is never trimmed because a day is running
  long — the day gets another part instead.
- **Never invent a fact.** Rules, spellings and citations are checked live on the day they are
  used, with a dated ledger row. A failed lookup leaves the exact reference to check, never a
  guess.
- **Every day ends with a check that can go RED**, and every folder has a part that is a deliberate
  failure: say it wrong, hear it, fix it; write it wrong, see it, fix it.

The full contract is [§11 of the plan](docs/00_MASTER_PLAN.md), and `python granth.py depth`
enforces the half of it a script can check.

## Layout

```text
docs/       the plan, the ledgers, the ADRs, the generated indexes
days/       the teaching — one folder per day, two folders inside each
granth.py   the whole toolchain, one file, stdlib only
granth.toml this repository's identity and the contract's knobs
```

---

Scaffolded with [granth](https://github.com/aignishant/granth-skill).
