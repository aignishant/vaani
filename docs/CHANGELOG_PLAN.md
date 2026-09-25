# Plan changelog — Vaani

Principle 8: *if reality changes, the plan is amended first.* Every amendment lands here **before**
any day or any work changes. **Append-only. Newest last.**

An entry answers three questions in this order: **what moved in the world**, **what this plan now
says instead**, and **what that costs** — which days are affected, which IDs move, what has to be
rewritten. An entry that names the change but not its cost is a note, not an amendment.

Anything structural — a change to the day format, the ID scheme, the phase boundaries, the
toolchain — also gets an ADR in `docs/adr/`, and the entry here links it.

---

- 2026-09-18 — Plan adopted at v1.0.0. See `docs/adr/ADR-0001-the-plan-as-adopted.md`.
- 2026-09-22 — **What moved:** the learner finished day 1 and asked for the next five days at
  once, in simpler English, with a genuine free web page to check every sound against. **What the
  plan now says (v1.1.0):** (1) §9 gains an exception: days may be *written* ahead in batches of
  up to five, but are still *done* one at a time, in order — `docs/adr/ADR-0003-days-written-ahead-in-batches.md`.
  (2) §12 gains §12.8 **The language ladder**: the English a day is written in grows with the
  learner, by phase, and phase 1 is written in the simplest English the rule allows, with a short
  *Words to know* list in every part. (3) §12 gains §12.9 **Sound links**: every part that teaches
  a sound links a genuine, free, live-checked page with audio for each target word, and the free
  sound-video series, so the learner can hear a model and not only read a symbol. **Cost:** day 1
  already meets §12.9 and mostly meets §12.8; no rewrite. Days 2–6 are written under the new
  rules. `plan_version` in `granth.toml` and in every hub moves to v1.1.0. No IDs move.
- 2026-09-22 — **What moved:** with days 2–6 written and only day 1 done, the learner asked for
  days 7–16 in one sitting, because their access to the tool that writes the days is on a budget
  they may not be able to renew. **What the plan now says (v1.2.0):** §9's writing-ahead rule
  gains a second case: when the learner's access to the writing tool is not guaranteed, a batch
  may be up to ten days and may start from the last *written* day, provided every day in between
  is fully written and passes `depth`. Days are still done one at a time, in order, and
  `docs/ERRORS.md` is read before each `done N` — `docs/adr/ADR-0004-batch-of-ten-from-the-last-written-day.md`.
  **Cost:** days 7–16 are written with only day 1's real errors in the ledger; their failure parts
  are generic by construction and say so. Day 17 onward needs a closed day 6 or a new ADR. The
  day 20 gate is not written ahead. `plan_version` in `granth.toml` and in every hub moves to
  v1.2.0. No IDs move.
- 2026-09-22 — **What moved:** ADR-0004's batch closed at day 16 by its own terms, the ledger
  still has one row, and the learner asked for the next ten days, 17–26. The reason is the one
  named in ADR-0004 and it has not changed: access to the tool that writes these days is on a
  budget that may not be renewed. Day 20 is the phase 1 gate, and §9 said a gate day is never
  written ahead — a rule whose consequence, if the tool goes away, is not a better gate but no
  gate and an unclosable phase. **What the plan now says (v1.3.0):** §9's writing-ahead rule is
  amended twice. (1) A second batch of up to ten days, 17–26, may be written ahead from the last
  written day, on every condition ADR-0004 already set. (2) A phase gate day **may** be written
  ahead, but only as a rehearsal: it teaches no new rule, it points at §7 for the pass condition
  and never restates it more kindly, and its hub and checklist carry a mandatory, tickable
  re-read of `docs/ERRORS.md` for the whole phase before `done N`, at which point its generic
  check lists are replaced by this learner's real recurring mistakes —
  `docs/adr/ADR-0005-second-batch-of-ten-and-the-gate-day.md`. **Cost:** days 17–26 are written
  with only day 1's real errors in the ledger; every failure part in the batch is generic by
  construction and says so, and day 26 is written twenty-five learning days before it is read.
  The day 20 gate is a rehearsal until its re-read step is done. Day 27 onward needs a closed
  day 6 or a further ADR; a third widening without a closed day in between should be read as the
  order rule having been abandoned, and faced directly. `plan_version` in `granth.toml` and in
  every hub moves to v1.3.0. No IDs move.
- 2026-09-22 — **What moved:** ADR-0005's batch closed at day 26 by its own terms and left a
  warning: a third widening without a closed day in between means the order rule has been
  abandoned in practice and should be faced directly. The learner asked for days 27–36 with the
  ledger still holding one row, so the warning applies. **What the plan now says (v1.4.0):** §9's
  writing-ahead rule gains the third batch, days 27–36, on every condition ADR-0004 and ADR-0005
  already set — and stops calling writing ahead exceptional. The rule is split into the two rules
  it always was: *doing* days in order is the hard rule, never broken, enforced by
  `python granth.py done N`; *writing* ahead is the normal mode of this repository while access to
  the writing tool is not guaranteed, capped at ten days per batch and argued for in its own ADR
  each time. The cost is paid in the open: every written-ahead part says in the part that its
  wrong version is a common beginner error and not this learner's, and every such day's hub and
  checklist carry a tickable `docs/ERRORS.md` re-read before `done N` —
  `docs/adr/ADR-0006-third-batch-and-the-order-rule-faced-directly.md`. **Cost:** days 27–36 are
  written with one day of real errors behind them; day 36 is written thirty-five learning days
  before it is read. The `ERRORS.md` re-read now carries thirty-five days of repair work and is a
  checkbox, not a guarantee. Day 37 onward needs a closed day 6 or a further ADR, and the phase 2
  gate, day 40, is deliberately left out of the batch. `plan_version` in `granth.toml` and in
  every hub moves to v1.4.0. No IDs move.
- 2026-09-23 — **What moved:** ADR-0006's batch closed at day 36 and left a question rather than a
  warning: if a fourth batch were asked for with the ledger still holding one row, the question is
  "is anybody doing the days?", and it belongs to the learner. A fourth batch was asked for. The
  question was put to the learner in those words, with the option of writing nothing and closing
  days instead, and the learner chose to write days 37–46 anyway. **What the plan now says
  (v1.5.0):** §9's writing-ahead rule gains the fourth batch, days 37–46, on every condition
  ADR-0004, ADR-0005 and ADR-0006 already set; it gains a rule that a batch **may cross a phase
  boundary but never jump a gate it does not write** — a gate inside the batch's span is written
  inside the batch, as a rehearsal; and it gains the requirement that when no day has been closed
  since the previous batch, the "is anybody doing the days?" question is **asked out loud before
  anything is written** and the answer recorded in the batch's ADR —
  `docs/adr/ADR-0007-fourth-batch-the-gate-day-and-the-phase-boundary.md`. **Cost:** days 37–46
  are written with one day of real errors behind them; day 46 is written forty-five learning days
  before it is read. The phase 2 gate, day 40, is now written, by a repository that has watched
  the learner do one day; it is a rehearsal until its `docs/ERRORS.md` re-read is ticked, and its
  hub and checklist say so. Days 41–46 assume a learner who has passed a gate nobody has
  attempted; if that gate is failed, they are re-read before they are used. Day 47 onward needs a
  closed day 6 or a further ADR. `plan_version` in `granth.toml` and in every hub moves to v1.5.0.
  No IDs move.
- 2026-09-23 — **What moved:** ADR-0007's batch was found unfinished: day 46 had four of its six
  parts and no hub, checklist or lab, so §9's condition that every day up to the last written day
  passes `depth` was false. A fifth batch was asked for with the ledger still holding one row, so
  the question "is anybody doing the days?" was put to the learner in those words before anything
  was written, with the option of writing nothing new. The learner chose to finish day 46 and then
  write days 47–56. **What the plan now says (v1.6.0):** §9's writing-ahead rule gains the fifth
  batch, days 47–56, on every condition ADR-0004 to ADR-0007 set, and gains the rule that **a
  batch is only started when the batch before it is whole** — an earlier batch's unfinished day
  is finished under its own ADR first and never counts toward the new ten —
  `docs/adr/ADR-0008-fifth-batch-and-the-unfinished-day.md`. §13 gains the v1.5.0 row it was
  missing and the v1.6.0 row. **Cost:** days 47–56 are written with one day of real errors behind
  them; day 56 is written fifty-five learning days before it is read. The phase 3 gate, day 60,
  stays outside the batch. Day 57 onward needs a closed day 6 or a further ADR, with the question
  asked again first. `plan_version` in `granth.toml` and in every hub moves to v1.6.0. No IDs move.
- 2026-09-23 — **What moved:** a sixth batch was asked for ("the next 14 days") with the ledger
  still holding one row. The fifth batch was whole: days 43–56 passed `depth` and `check` was
  green. The question "is anybody doing the days?" was put to the learner in those words before
  anything was written. The options were: write nothing and close days, write days 57–66 at the
  cap of ten, or write days 57–70 past the cap. The learner chose fourteen, days 57–70, with the
  cap stated. **What the plan now says (v1.7.0):** §9's writing-ahead rule gains the sixth batch,
  days 57–70, on every condition ADR-0004 to ADR-0008 set. It is named as a **one-time exception
  to the cap of ten**, chosen by the learner with the cap in front of them. The cap stays ten, and
  any batch over ten needs its own ADR and its own choice.
  `docs/adr/ADR-0009-sixth-batch-of-fourteen-across-the-phase-3-gate.md`. §13 gains the v1.7.0
  row. **Cost:** days 57–70 are written with one day of real errors behind them. The phase 3
  gate, day 60, is written inside the batch as a rehearsal, with a mandatory `ERRORS.md` re-read
  for days 41–59. Days 61–70 open phase 4 and assume two gates nobody has attempted. Day 70 is
  written sixty-nine learning days before it is read. Day 71 onward needs a closed day 6 or a
  further ADR, with the question asked again first. `plan_version` in `granth.toml` and in every
  hub moves to v1.7.0. No IDs move.
- 2026-09-23 — **What moved:** a seventh batch was asked for ("the next 14 days") with the ledger
  still holding one row. The sixth batch was whole: `check` was green on all 70 written days. The
  question "is anybody doing the days?" was put to the learner in those words before anything was
  written, with the cap of ten stated and ADR-0009's fourteen named as no precedent. The options
  were: write nothing and close days, write days 71–80 at the cap, or write days 71–84 past it. The
  learner chose ten, days 71–80. **What the plan now says (v1.8.0):** §9's writing-ahead rule gains
  the seventh batch, days 71–80, on every condition ADR-0004 to ADR-0009 set, at the cap of ten —
  `docs/adr/ADR-0010-seventh-batch-of-ten-to-the-phase-4-gate.md`. §13 gains the v1.8.0 row.
  **Cost:** days 71–80 are written with one day of real errors behind them. The phase 4 gate, day
  80, is written inside the batch as a rehearsal, with a mandatory `ERRORS.md` re-read for days
  61–79. Day 80 is written seventy-nine learning days before it is read. Day 81 onward needs a
  closed day 6 or a further ADR, with the question asked again first. `plan_version` in
  `granth.toml` and in every hub moves to v1.8.0. No IDs move.
- 2026-09-23 — **What moved:** an eighth batch was asked for ("complete next 4 days doc") with the
  ledger still holding one row. The seventh batch was whole: `check` was green on all 80 written
  days and `depth` passed for each of days 71–80, which were in the working tree and not yet
  committed. The question "is anybody doing the days?" was put to the learner in those words
  before anything was written. The options were: write nothing and close days, write days 81–84
  as asked, or write days 81–90 at the cap. The learner chose four, days 81–84. **What the plan
  now says (v1.9.0):** §9's writing-ahead rule gains the eighth batch, days 81–84, on every
  condition ADR-0004 to ADR-0010 set, and says that a batch under the cap still gets its own ADR
  and the question first — `docs/adr/ADR-0011-eighth-batch-of-four-opening-phase-5.md`. §13 gains
  the v1.9.0 row. **Cost:** days 81–84 are written with one day of real errors behind them. Day 84
  is written eighty-three learning days before it is read. The batch crosses no gate; the phase 5
  gate, day 100, is not written. Day 85 onward needs a closed day 6 or a further ADR, with the
  question asked again first. `plan_version` in `granth.toml` and in every hub moves to v1.9.0.
  No IDs move.
- 2026-09-24 — **What moved:** "next 10 days doc" was asked for with the ledger still holding one
  row. The eighth batch was not whole: day 81 was written and passed `depth`, and days 82–84 had
  empty folders. `check` passed the depth contract on all 81 written days, and failed only on
  stale generated indexes. The question "is anybody doing the days?" was put to the learner in
  those words before anything was written. It said that 82–84 were unfinished and came first. The
  options were: write nothing and close days, finish only 82–84, finish 82–84 and write 85–91 (ten
  day documents), or finish 82–84 and write 85–94 (a new batch at the cap). The learner chose
  82–91. **What the plan now says (v1.10.0):** §9's writing-ahead rule records that days 82–84 are
  finished under ADR-0011 and that the ninth batch is days 85–91, on every condition ADR-0004 to
  ADR-0011 set — `docs/adr/ADR-0012-ninth-batch-of-seven-after-finishing-the-eighth.md`. §13 gains
  the v1.10.0 row. **Cost:** days 82–91 are written with one day of real errors behind them. Day
  91 is written ninety learning days before it is read. The batch crosses no gate; the phase 5
  gate, day 100, is not written. Day 92 onward needs a closed day 6 or a further ADR, with the
  question asked again first. Days 71–91 are still uncommitted. `plan_version` in `granth.toml`
  and in every hub moves to v1.10.0. No IDs move.
- 2026-09-24 — **What moved:** "next 10 days doc" was asked for with the ledger still holding one
  row. The ninth batch was whole: `depth` passed for each of days 85–91, and the working tree was
  clean, with days 71–91 committed. The question "is anybody doing the days?" was put to the
  learner in those words before anything was written. It named the phase 5 gate at day 100 and the
  phase boundary at day 101. The options were: write nothing and close days, write days 92–96,
  write days 92–100 ending on the gate, or write days 92–101 as asked. The learner chose 92–101.
  **What the plan now says (v1.11.0):** §9's writing-ahead rule gains the tenth batch, days
  92–101, at the cap of ten, carrying the phase 5 gate as a rehearsal and opening phase 6, on every
  condition ADR-0004 to ADR-0012 set —
  `docs/adr/ADR-0013-tenth-batch-of-ten-across-the-phase-5-gate.md`. §13 gains the v1.11.0 row.
  **Cost:** days 92–101 are written with one day of real errors behind them. Day 101 is written a
  hundred learning days before it is read. The day 100 gate is a rehearsal until its `ERRORS.md`
  re-read for days 81–99 is ticked. Day 102 onward needs a closed day 6 or a further ADR, with the
  question asked again first. `plan_version` in `granth.toml` and in every hub moves to v1.11.0.
  No IDs move.
- 2026-09-24 — **What moved:** "next 10 days doc" was asked for with the ledger still holding one
  row. The tenth batch was whole: `depth` passed for each of days 92–101, and the working tree was
  clean, with days 92–101 committed. The question "is anybody doing the days?" was put to the
  learner in those words before anything was written. It said that days 2–101 are written and not
  done, that day 101 alone has twenty unticked boxes, and that no gate falls inside days 102–111.
  The options were: write nothing and close days, write days 102–106, write days 102–111 as asked,
  or write days 102–112, over the cap and not recommended. The learner chose 102–111. **What the
  plan now says (v1.12.0):** §9's writing-ahead rule gains the eleventh batch, days 102–111, at the
  cap of ten, inside phase 6 and crossing no gate, on every condition ADR-0004 to ADR-0013 set —
  `docs/adr/ADR-0014-eleventh-batch-of-ten-inside-phase-6.md`. §13 gains the v1.12.0 row.
  **Cost:** days 102–111 are written with one day of real errors behind them. Day 111 is written a
  hundred and ten learning days before it is read. Day 112 onward needs a closed day 6 or a further
  ADR, with the question asked again first. `plan_version` in `granth.toml` and in every hub moves
  to v1.12.0. No IDs move.
- 2026-09-24 — **What moved:** "next 2 days doc" was asked for with the ledger still holding one
  row. The eleventh batch passed `depth` for each of days 102–111 and `check` passed, but it was on
  disk uncommitted. The question "is anybody doing the days?" was put to the learner in those words
  before anything was written. It said that days 2–111 are written and not done, that day 101 alone
  has twenty unticked boxes, that days 102–111 were uncommitted, and that no gate falls inside days
  112–113. The options were: write nothing and close days, commit days 102–111 and then write days
  112–113, or write days 112–113 on the uncommitted tree, not recommended. The learner chose to
  commit first, and days 102–111 were committed before this batch was written. **What the plan now
  says (v1.13.0):** §9's writing-ahead rule gains the twelfth batch, days 112–113, inside phase 6
  and crossing no gate, on every condition ADR-0004 to ADR-0014 set, plus a new one written down:
  a batch starts from a clean tree —
  `docs/adr/ADR-0015-twelfth-batch-of-two-to-the-proofreading-checklist.md`. §13 gains the v1.13.0
  row. **Cost:** days 112–113 are written with one day of real errors behind them. Day 114 onward
  needs a closed day 6 or a further ADR, with the question asked again first. `plan_version` in
  `granth.toml` and in every hub moves to v1.13.0. No IDs move.
- 2026-09-24 — **What moved:** "next 2 days doc" was asked for again with the ledger still holding
  one row. Days 112–113 passed `depth` and `check` but were on disk uncommitted. The question "is
  anybody doing the days?" was put to the learner in those words before anything was written. It
  said that days 2–113 are written and not done, that day 111 alone has twenty unticked boxes, that
  days 112–113 were uncommitted, and that no gate falls inside days 114–115. The options were:
  commit days 112–113 and write nothing new (recommended), commit and then write days 114–115, or
  leave everything uncommitted. The learner chose to commit and then write, and days 112–113 were
  committed before this batch was written. **What the plan now says (v1.14.0):** §9's
  writing-ahead rule gains the thirteenth batch, days 114–115, inside phase 6 and crossing no gate,
  on every condition ADR-0004 to ADR-0015 set —
  `docs/adr/ADR-0016-thirteenth-batch-of-two-first-rehearsal-and-draft.md`. §13 gains the v1.14.0
  row. **Cost:** days 114–115 are written with one day of real errors behind them, and day 114
  works on a recording and a page that do not exist yet. Day 116 onward needs a closed day 6 or a
  further ADR, with the question asked again first. `plan_version` in `granth.toml` and in every
  hub moves to v1.14.0. No IDs move.
- 2026-09-24 — **What moved:** "next 2 days doc" was asked for again with the ledger still holding
  one row. Days 114–115 passed `depth` and `check`. The question "is anybody doing the days?" was
  put to the learner in those words before anything was written, with three options: commit days
  114–115 and write nothing new (recommended), commit and then write days 116–117, or leave
  everything uncommitted. The learner chose to commit and then write; they had already committed
  days 114–115 themselves (`fa805fe`), so the tree was clean. **What the plan now says
  (v1.15.0):** §9's writing-ahead rule gains the fourteenth batch, days 116–117, inside phase 6 and
  crossing no gate, on every condition ADR-0004 to ADR-0016 set —
  `docs/adr/ADR-0017-fourteenth-batch-of-two-second-rehearsal-and-portfolio.md`. §13 gains the
  v1.15.0 row. **Cost:** day 117 works on five gate recordings and six gate pieces that do not
  exist yet. Day 118 onward needs a closed day 6 or a further ADR, with the question asked again
  first, and any batch reaching day 120 writes the gate day inside it as a rehearsal.
  `plan_version` in `granth.toml` and in every hub moves to v1.15.0. No IDs move.
- 2026-09-25 — **What moved:** "next 10 days doc" was asked for with the ledger still holding one
  row and only three days left in the plan. Days 116–117 passed `depth`; `check` passed once the
  indexes were regenerated; the tree was not clean. The question "is anybody doing the days?" was
  put to the learner in those words before anything was written. It said that the course ends at
  day 120, so only days 118–120 remain, that days 2–117 are written and not done, that days 116–117
  were uncommitted, and that day 120 is the phase 6 gate and would be written as a rehearsal. The
  options were: commit days 116–117 and write nothing new (recommended), commit and then write days
  118–120, or leave everything as it is. The learner chose to commit and then write, and days
  116–117 were committed (`33149e6`) before this batch was written. **What the plan now says
  (v1.16.0):** §9's writing-ahead rule gains the fifteenth and last batch, days 118–120, ending on
  the phase 6 gate as a rehearsal, on every condition ADR-0004 to ADR-0017 set —
  `docs/adr/ADR-0018-fifteenth-batch-of-three-to-the-phase-6-gate.md`. §13 gains the v1.16.0 row.
  **Cost:** the last gate of the course is written with one day of real errors behind it; its check
  lists stay generic until its `ERRORS.md` re-read is ticked. Day 120 reviews the conversation and
  the essay that day 119 makes, and never makes them late. The plan is now written to its last day;
  any further change is an amendment to a written day, not a new batch. `plan_version` in
  `granth.toml` and in every hub moves to v1.16.0. No IDs move.
