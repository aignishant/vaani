# Day NN — definition of done

`python granth.py done NN` refuses to commit while any box below is unticked. That refusal is the
point: a day is finished when the recording exists, the page exists, and the checks are green —
and by nothing else.

No box here carries a time estimate, and none ever will.

## Speaking folder

<!-- One box per part. Reading it is not enough — the recorder was on. -->

- [ ] `parts/01-speaking/1.1-<slug>.md` — read · said the model lines aloud · answered its question out loud
- [ ] `parts/01-speaking/1.2-<slug>.md` — did the rep with the recorder on, about my own life
- [ ] `parts/01-speaking/1.3-<slug>.md` — said the wrong version on purpose · heard the difference · said it right
- [ ] The recording exists: `lab/speaking/day-NN.<ext>`
- [ ] Listened back once; anything caught is in `docs/ERRORS.md`

## Writing folder

- [ ] `parts/02-writing/2.1-<slug>.md` — read · copied the model lines by hand · answered its question out loud
- [ ] `parts/02-writing/2.2-<slug>.md` — did the rep with the pen moving, about my own life
- [ ] `parts/02-writing/2.3-<slug>.md` — wrote the wrong version on purpose · saw the difference · wrote it right
- [ ] The page exists: `lab/writing/day-NN.md`
- [ ] Read back once; anything caught is in `docs/ERRORS.md`

## Check

- [ ] **Break it on purpose, watch it go red, fix it.** <what to say or write wrong>
- [ ] `python granth.py depth NN` — green
- [ ] `python granth.py check` — green across the whole repository

## Record

- [ ] Every term defined for the first time today has a row in `docs/GLOSSARY.md`
- [ ] Every reference page opened today is in the hub's §8
- [ ] Every source cited today has a dated row in `docs/SOURCES.md`
- [ ] On a gate day: the `docs/RECORDINGS.md` and `docs/WRITINGS.md` rows are pasted
- [ ] The `docs/PROGRESS.md` row is pasted from the hub's §11
- [ ] Committed with the message from the hub's §11
