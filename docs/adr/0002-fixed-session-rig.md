# ADR-0002 — A fixed session rig instead of clocks in days

**Status:** accepted · **Date:** 2026-09-07

## Context

Two requirements collide.

The inherited contract forbids durations anywhere in a day document, for a good reason: a
duration field silently authorises cutting an explanation because the day is running long.
Remove the field and that edit loses its justification.

But the learner has a real constraint — roughly half an hour a day, and a course that has to fit
inside two to three months. A curriculum that ignores that produces days that cannot be done and
a plan abandoned in week three.

## Decision

The budget lives in exactly one place: §4 of the master plan, as a **fixed five-block rig** —
warm-up, study, drill, free rep, log — with a rough share against each block. It is the same
every day.

`days/` stays completely clock-free. No day document carries a duration, a pace, or an estimate,
and the day skill and the depth contract both check for it.

## Consequences

A day is still a unit of subject, not of time. If a day runs long, it runs long, and nothing is
cut. But the learner knows the shape of every session before opening it, and can tell after two
weeks whether the days are correctly sized.

**The pressure valve is the day map, not the day.** If sessions consistently run to double, the
fix is to split the day and amend the plan — never to skip the free rep. The free rep is the
last block, which makes it the one under pressure; the depth contract makes it non-optional
precisely for that reason.
