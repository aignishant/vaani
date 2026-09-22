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
