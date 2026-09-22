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
