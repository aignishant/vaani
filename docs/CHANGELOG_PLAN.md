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
