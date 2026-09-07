# ADR-0001 — No code, and no toolchain

**Status:** accepted · **Date:** 2026-09-07

## Context

The parent skill this repository is shaped after emits a Python toolchain that mechanically
enforces the depth contract, plus a config file the toolchain reads. It also assumes the subject
may involve code, and offers switches to turn linting and tests off.

The learner's requirement was explicit: no coding anywhere in this project. Not as subject
matter, and not as machinery.

## Decision

No code in this repository. No toolchain file, no config file, no scripts, no lint, no tests.
The depth contract in plan §11 is enforced by reading — by the learner against `CHECKLIST.md`,
and by the day skill, which is instructed to walk all twelve rules and refuse to close a day
that fails one.

## Consequences

**Lost.** The mechanical guarantees. Nothing exits non-zero. A day written out of order, a
smuggled-in duration, a missing section — all of these now depend on someone noticing.

**Gained.** The learner can run this entire curriculum from a phone and a text editor, with no
runtime installed and nothing to break. For a speaking course, that is the correct trade: the
barrier to a daily habit should be a recorder and nothing else.

**Mitigation.** The depth contract compensates by being short — twelve rules, all checkable by
eye in under a minute — and by putting the four that actually matter first: the part ceiling,
the recording, the deliberate failure, and no clocks.
