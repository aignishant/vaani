# `days/` — the teaching

One folder per day, `day-NN-<slug>/`. The number is the identity; the slug is a label on it, so a
folder can be renamed to a better slug at any time and nothing downstream notices.

```text
days/day-NN-<day-slug>/
├── LESSON.md      # the hub — orients and assembles; it never teaches
├── CHECKLIST.md   # the definition of done
├── parts/
│   ├── 01-speaking/   # THE SPEAKING FOLDER — the rule, the rep, the deliberate failure
│   └── 02-writing/    # THE WRITING FOLDER  — the rule, the rep, the deliberate failure
├── sources/       # one document per primary source (rare in this course)
└── lab/
    ├── speaking/  # your recording for the day — stays on your phone and here, not in git
    └── writing/   # your page for the day — committed; this is the Writing Portfolio
```

**The two folders are separate courses.** Do the speaking folder, or the writing folder, or both,
in either order. Nothing in one needs the other.

**Read a folder in this order:** the hub's §1 and its map for that folder, then the parts in
number order — the rule, then the rep with the recorder on or the pen moving, then the deliberate
failure. If the day has `sources/`, read those last.

**Write a day** with `/day-vaani N`, or scaffold an empty one with `python granth.py new N <slug>`.
The standard every day is held to is the plan's §11.

`_TEMPLATES/` holds the blank documents `python granth.py new` copies from. It is not a day and no
tool treats it as one.
