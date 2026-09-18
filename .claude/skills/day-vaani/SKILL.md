---
name: day-vaani
description: Write day N of the Vaani curriculum — the hub, the two independent folders parts/01-speaking/ and parts/02-writing/, the lab scaffold and the checklist — against the depth contract in docs/00_MASTER_PLAN.md §11. Use when asked to write, generate, draft or continue a day of this curriculum, or when the user types a bare day number.
argument-hint: "[day-number]"
---

# Write day $ARGUMENTS of Vaani

> **Read `docs/00_MASTER_PLAN.md` §11 in full before writing a single line.** It is the depth
> contract this skill implements. This file is the *procedure*; §11 is the *standard*, and the
> standard wins wherever the two seem to disagree.

## The commitments this course adds (plan §2, Principles 13–16)

1. **Every part ends in the learner's own English.** Recorder on, or pen moving. A part that only
   explains has failed.
2. **The two folders never lean on each other.** `01-speaking/` and `02-writing/` are separate
   courses. No cross-links, no "as you practised", no shared prerequisite. Different story
   families are fine and usual.
3. **Rule, then rep.** Every part carries the rule in plain words and then makes the learner use
   it in a sentence of their own.
4. **Never solve the reps.** Model lines show the shape; the learner's line is about the learner's
   own life, and it is left as `TODO(me)`.

And the three granth commitments (§11.1): **one idea per document · no clocks · zero to real life
in one document.**

---

## Step 1 — gather

1. Run `python granth.py brief $ARGUMENTS`. **If it exits non-zero, stop and report why.** Do not
   argue with the order guard: skipping, merging or reordering a day needs an ADR, written first.
2. Read the plan: **§2** (the principles, especially 13–16), **§4** (the constraints: a phone, a
   notebook, a mirror, nothing bought, no code), **§8** (the day map — the two IDs for day
   $ARGUMENTS, speaking first, writing second), **§11** (the depth contract), **§12** (the style
   guide).
3. Read `docs/GLOSSARY.md`. Any term already defined there is **linked, not redefined**. Grammar
   words count.
4. Read the last twenty rows of `docs/ERRORS.md`. The learner's own caught mistakes are the best
   material for today's deliberate-failure parts, if they fit the day's rule.
5. Read the previous day's `LESSON.md` and `CHECKLIST.md`. If the checklist has unticked boxes,
   say so and ask before proceeding. Build on what the same folder taught on earlier days; never
   duplicate it and never rewrite it.

## Step 2 — verify reality before you write (Principle 6)

6. **Never invent a rule.** For every grammar rule, spelling, or pronunciation the day states,
   open a live reference page and note the URL and the date. The part names the page checked, and
   the hub's §8 tabulates them. If the live reference disagrees with the plan's day title, **stop
   and propose an amendment** — do not silently adapt.
7. **Never invent a wrong version.** The deliberate-failure part shows what a beginner *actually*
   says or writes. If you are not confident a real beginner makes this exact mistake, say so in
   the part and choose one you are confident of.
8. **Never invent a citation.** This course rarely cites anything. If a day does, open the record
   live, copy the title from it, and add a dated row to `docs/SOURCES.md`. Cite by **title and
   identifier, never by author**.

## Step 3 — plan the split (before writing any prose)

9. The day has **exactly two sections**: `01-speaking/` for the `SND` or `SPK` ID and
   `02-writing/` for the `GRM` or `WRT` ID. A third section is an ADR, not a choice.
10. The default shape of each folder is three parts — **the rule** (`foundation`), **the rep**
    (`working`), **the deliberate failure** (`production`, `failure: true`). Split further by
    **idea boundary, never by length** (§11.7): a sound day may need a fourth part for a second
    mouth position; a letter-writing day may need one per section of the letter. Never fewer than
    three.
11. Apply the **one-idea test**, the **standalone test** (prerequisites inside the same folder
    only, or the same folder on an earlier day) and the **no-shortcut test** to every planned part.
12. **Choose one story family per folder.** The two folders may differ. Grep the folder's other
    parts before choosing.
13. **Print the planned part list for both folders before writing.** If it looks thin, the user
    will say so, and that conversation is cheap now and expensive after six documents exist.

## Step 4 — write the parts

Path: `days/day-NN-<day-slug>/parts/01-speaking/1.T-<slug>.md` and
`days/day-NN-<day-slug>/parts/02-writing/2.T-<slug>.md`

14. **Name the day folder `day-NN-<slug>`** — the number zero-padded, then a kebab-case slug of
    1–4 words from the *speaking* half of the plan's title, articles dropped.
15. **Links are relative to the part's own folder**: a sibling is `1.2-<slug>.md`, the hub is
    `../../LESSON.md`, the same folder on an earlier day is
    `../../../day-MM-<slug>/parts/01-speaking/1.1-<slug>.md`. **Never `../02-writing/` from a
    speaking part, never `../01-speaking/` from a writing part.**
16. Every part carries **all eleven sections of §11.4, in order**, with this course's headings:
    *One-line answer · The story · The idea in plain language · Why Vaani needs it · [The source
    behind it] · The rule · When it breaks · In real life · Check yourself*. Start from
    `days/_TEMPLATES/PART.md`. There are no code blocks, so no *Line by line*.
17. **Model lines are blockquotes.** Never code blocks. Never more than three in a row. Short.
18. **The story is the section that gets written badly.** A scene the reader has plausibly lived —
    a shop counter, a landlord on the phone, a form at the bank, a neighbour at the door. Simple
    words. Load-bearing: the scene contains the actual misunderstanding. One family per folder.
19. **The rule must be audible or visible.** If saying it wrong sounds the same and writing it
    wrong looks the same, it is not a rule for this course (§11.8, failure 9). Say where the
    tongue goes, where the capital goes, what the listener hears.
20. **`When it breaks` carries the real wrong version**, written as it comes out of a beginner's
    mouth or pen, and what the listener or reader gets instead. Then the smallest fix.
21. **`In real life` is not optional.** What a fluent speaker does instead · what goes wrong under
    pressure · what a native listener notices and forgives · what a formal reader does not.
22. **`Check yourself` is the rep.** One thing to record or write now, about the learner's own
    life, as a `TODO(me)` prompt — **never the answer** — and one question to answer out loud.
23. A diagram whenever the rule is spatial: the mouth, the page, the shape of a letter.

## Step 5 — sources, if any

24. Almost never. If the day genuinely leans on a citable document, follow §11.4.2: one document
    in `sources/`, from `days/_TEMPLATES/SOURCE.md`, read after the parts, taught once in the
    whole curriculum, with the claim shown on and off. Check `docs/wiki/ENTITIES.md` first.

## Step 6 — write the hub

25. `days/day-NN-<slug>/LESSON.md`, from `days/_TEMPLATES/LESSON.md`. **The hub never teaches.**
    Eleven numbered sections in order (§11.5). §2 is two tables, one per folder. §4 names two
    reps: the recording and the page, both `TODO(me)`. §11 ends with the verbatim ledger rows and
    the commit message.
26. `frontmatter.parts` must equal the number of documents actually in `parts/`. The checker
    compares them. `frontmatter.ids` carries exactly the two IDs from §8.

## Step 7 — write the checklist and the lab

27. `days/day-NN-<slug>/CHECKLIST.md`, from `days/_TEMPLATES/CHECKLIST.md`: one box per part in
    each folder, the recording-exists and page-exists boxes, the listen-back and read-back boxes,
    **at least one "break it, watch it go red, fix it"**, the ledger rows, and the commit box.
28. Create `lab/speaking/` and `lab/writing/` as empty folders with a one-line `README.md` in each
    saying what goes there. The learner fills them.

## Step 8 — verify

29. Run `python granth.py depth $ARGUMENTS`. **Fix every failure; never hand-wave past one.**
30. Run `python granth.py index`, then `python granth.py check`.
31. **Read both folders once more for a cross-folder lean.** The checker cannot catch it. If either
    folder mentions the other, fix it.
32. Finish by printing: the two IDs closed, the part count per folder, the two reps, the budget,
    and the reference pages you actually opened.

---

## Always

- Honour `CLAUDE.md`: doc-first · never invent a fact · at least one check that can go red ·
  every instruction inside the plan's §4 constraints.
- **Write for a beginner in the language you are writing.** Short sentences. Common words.
  Contractions. Second person. If a twelve-year-old could not follow the first sentence, rewrite
  it.
- **Grammar and punctuation are part of the deliverable, in every section.** In a language course
  they are the subject.
- **Do not solve the `TODO(me)` reps.** Teach; do not do the reps for the learner.
- **Never name a person, instructor, author, channel, app, academy or training company.** "Your
  phone's voice recorder". Names inside model lines are the learner's characters and are fine.
- **No clocks.** Not in frontmatter, not in prose, not in the checklist. Lengths are in words or
  turns, never in minutes.
- The failure modes this format exists to prevent (§11.8): splitting without deepening · summary
  in place of explanation · **stopping at the model line** · assuming the previous day · a rule
  without failure · **trimming to fit** · solved reps · a carried-over clock · **a rule the
  learner cannot hear or see** · **a cross-folder lean**. If a part gained no story, no rule, no
  real wrong version and no real-life section, it is not done.
