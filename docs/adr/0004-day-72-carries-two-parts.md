# ADR-0004 — Day 72 carries two parts, under the rehearsal-day allowance

**Status:** accepted · **Date:** 2026-09-07

## Context

`CLAUDE.md` rule 2 and ADR-0003 set the ceiling: one part document per day, two on rehearsal days,
never three. The three earlier gates — Days 18, 36 and 54 — each carry one part and produce one
portfolio recording, so the question never came up before.

Day 72 is different, and the plan says so in two places written before any day was drafted. §7
names the Phase 4 gate as "a ten-minute unscripted interview, **plus the assembled portfolio**",
and `docs/RECORDINGS.md` allocates two of the sixteen recordings to Day 72: row 15, the gate, and
row 16, the retrospective.

Two recordings cannot live in one part. A part has seven fixed sections with exactly one **Say it
yours** in it, and rule 4 of the depth contract requires that rep to name its own file. Putting a
second recorded rep inside one part would break the section contract — which is the shape every
other day in the repository is held to — in order to protect a document count.

The two recordings are also genuinely sequential rather than two halves of one thing. The
retrospective is made of the gate's counts, so it cannot be recorded until the gate exists.

## Decision

**Day 72 carries two part documents**, treated as a rehearsal-class day under the existing
allowance rather than as an exception to it:

- `parts/01-ten-minutes-and-nobody-helping.md` → `audio/d72-gate.m4a` (recording 15)
- `parts/02-the-retrospective.md` → `audio/d72-retrospective.m4a` (recording 16)

The ceiling itself is untouched: two, never three. Day 72's hub states the reason, exactly as the
rehearsal-day hubs do.

Part 01 teaches no new phrases, following the gate convention set by Days 18, 36 and 54 — a gate
reminds, it does not teach. Part 02 carries the day's only phrase bank.

## Consequences

**No amendment to `00_MASTER_PLAN.md`**, and therefore no row in `docs/CHANGELOG_PLAN.md`. The day
map, the concept IDs and the sixteen-recording portfolio are unchanged; this ADR records how an
already-written requirement is met, not a change to it.

**The rule now has a second reading available to a future writer**: "a day that produces two
portfolio recordings carries two parts". That reading is narrow and evidence-bound — the portfolio
has sixteen recordings across seventy-two days and only Day 72 has two — but it is a crack in the
most load-bearing rule in the repository, and ADR-0003 predicted exactly this pressure. Anyone
reaching for this precedent on a day that produces one recording is reaching wrong.
