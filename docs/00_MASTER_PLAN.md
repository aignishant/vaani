---
plan: vaani
version: "v1.3.0"
topic: "Speaking and writing English from zero, one hour a day, with a recording and a written piece every day"
tracks: 4
ids: 240
days: 120
phases: 6
doc_architecture: "hub + parts/ (see §11)"
amended: "2026-09-22"
---

# MASTER PLAN v1.3.0 — Vaani

## Speaking and writing English from zero, one hour a day, with a recording and a written piece every day

> **Vaani** — वाणी, *speech, the voice, the spoken word*. The course is named for the half that
> is hardest to practise alone. Writing you can do in a notebook; speaking needs a recorder, a
> mirror, and the nerve to hear yourself back.
>
> **Purpose: this is the single source of truth.** Every other document in this repository points
> back here. When a day document and this plan disagree, this plan is right and the day is a bug.
> When *reality* and this plan disagree, the plan is amended first (Principle 8) — never patched
> around in silence.

---

## Table of contents

| § | Section |
| --- | --- |
| 1 | The vision — what exists at the end |
| 2 | Core principles — the rules that are never broken |
| 3 | The artifact — what actually gets built |
| 4 | Constraints & budget |
| 5 | The baseline — what this plan is pinned to, and how it is verified |
| 6 | The tracks and the ID scheme |
| 7 | The phases |
| 8 | The day map — day to IDs closed |
| 9 | Phase gates and the freshness check |
| 10 | Ledgers and traceability |
| **11** | **The depth contract — how a day is written** |
| 12 | The style guide |
| 13 | Amendment record |

---

## 1 · The vision — what exists at the end

By day 120 you will have **two portfolios — a Speaking Portfolio of dated voice recordings ending
in an unscripted talk and a recorded interview, and a Writing Portfolio of dated written pieces
ending in a full essay — every piece made by you, in English, on the day the plan says**, and you
will be able to defend every decision inside it.

The measure is not how many days were finished. It is whether, handed the finished thing and a
sceptical reviewer, you can explain each part, say what it costs, name what breaks it, and show
the check that catches the breakage. For a language course that reviewer is a stranger who speaks
English and does not know you: can they follow the recording, and can they read the page?

Three things this plan is trying to prevent:

1. **The tutorial ceiling.** Following steps produces something that runs and understanding that
   evaporates the moment the inputs change. Every subtopic here therefore ends at the real-system
   version, not the toy one (Principle 10). In this course the "real system" is a real
   conversation with a real person, and a real page a real person reads.
2. **The forgotten middle.** In a curriculum this long, day 3 is forgotten by day 66. Every term
   is defined on first use, *including terms from earlier days, with a link back*, and the
   glossary is a ledger rather than an afterthought.
3. **The unverifiable claim.** Notes written from memory rot silently. Every rule, example and
   citation is checked on the day it is used, and the document names what was checked
   (Principle 6).

### 1.1 Stated non-goals

These are decisions, not blind spots. Writing them down stops each of them being re-litigated on
a day when the real subject is something else.

- **Not an exam course.** No IELTS, TOEFL or any test format is taught. The gates are recordings
  and pages a stranger can follow, not band scores.
- **Not a grammar reference.** Grammar appears only where a speaking or writing rep needs it that
  day, taught as a rule with an audible or visible consequence. Nothing is taught "for
  completeness".
- **Not a listening or reading course.** Both happen as a side effect of the reps, but no day is
  about them. The learner records and writes; that is the whole loop.

---

## 2 · Core principles — the rules that are never broken

<!-- granth:principles:start -->

1. **Doc-first.** The day document is written before the work; the work follows the document. A
   thing built first and explained afterwards gets explained in the shape it happened to take,
   which is not the same as the shape it should have.
2. **One day, one commit.** Append-only, traceable history. The repository is the memory.
3. **Build first, compare after.** Hand-roll the mechanism once, then adopt the tool that does it
   for you — so the tool is a convenience and never a mystery. A tool adopted before the
   mechanism is understood becomes a thing you cannot debug.
4. **Every concept is load-bearing.** If removing it would not change the artifact, it does not
   get a day. Coverage is not the goal; a working understanding is.
5. **Depth over density.** A day is a hub plus one document per subtopic, never one long page. If
   a subtopic cannot be read on its own, understood without scrolling past a different subtopic,
   and explained back out loud, it has not been split finely enough. A wall of text is not depth —
   it is depth's disguise. The full contract is §11.
6. **Never invent a fact.** A version, an interface, a limit, a citation: look it up **live on the
   day it is used**, or leave a `TODO` containing **the exact lookup command**. The document names
   what was checked and when. A guess that happens to be right is still a guess, and the next
   reader cannot tell which kind they are holding.
7. **Fail honestly.** Errors surface, escalate and are logged. Nothing fabricates a result to
   cover an error — and this applies to the writer as much as to anything that is built. An
   unrun command's output is a `TODO`, never a plausible transcript.
8. **If reality changes, the plan is amended first.** A moved specification, a renamed interface,
   a changed limit: amend via `docs/CHANGELOG_PLAN.md` and, for anything structural, an ADR —
   *then* continue. Days are never silently patched. Stop and say so.
9. **Every day ends with a check that can go RED.** A check that cannot fail has verified nothing.
   At least one per day, and at least one day per phase whose subject is a deliberate failure.
10. **Assume no prior knowledge, finish at production.** Every subtopic opens where a reader who
    has never met the idea can stand, defines its jargon on first use — including jargon from
    earlier days, with a link back — and does not stop at the toy example. It ends with how the
    idea is used in a real system: what a professional does instead of the teaching version, what
    breaks at scale or under pressure, the review comment, the interview question. Strong basics
    and advanced technique are the same document, in that order.
11. **A day is a unit of subject, not a unit of time.** No document carries a time estimate, a
    duration, an "estimated hours" field or a suggested pace — not in frontmatter, not in prose,
    not in a checklist. A topic is finished when it is understood, in one sitting or in five.
    **Nothing is ever trimmed to fit a clock**; a day that runs long gets another part, not a
    shorter explanation.
12. **Blast radius before capability.** Every new power arrives together with its containment
    story: what it can reach, what stops it, and what the blast looks like when the stop fails.
13. **Every part ends in the learner's own English.** A speaking part ends with the recorder on
    and the learner saying something that is theirs, not the model line. A writing part ends with
    the learner's pen on the page. A part that only explains has failed the contract, however
    good the explanation.
14. **Speaking and writing never lean on each other.** The two folders in a day are written so
    that either can be done alone, in any order, on its own topic. A speaking part never says
    "as you wrote this morning"; a writing part never says "as you said". The learner asked for
    two separate courses in one repository, and that is what this is.
15. **Rule, then rep, in every part.** A rule with no rep is reading. A rep with no rule is
    guessing. Every part carries the rule in plain words and then makes the learner use it, out
    loud or on paper, in a sentence of their own.
16. **Never solve the learner's reps.** A prompt is a prompt. If the document writes the answer,
    the learner reads instead of speaks. Model lines show the *shape*; the learner's line is
    always about the learner's own life.

<!-- granth:principles:end -->

> Principles 5, 10 and 11 are made concrete by **§11, the depth contract**, and are enforced
> mechanically by `granth.py` (`python granth.py depth N`) — and, for everything a script
> cannot judge, by reading.

---

## 3 · The artifact — what actually gets built

Two portfolios, built one piece a day, kept in each day's `lab/` folder and indexed in
`docs/RECORDINGS.md` and `docs/WRITINGS.md`.

**The Speaking Portfolio** is a folder of voice recordings made on your phone. Every day of the
course ends with the recorder on: the learner says something that is theirs — their own name,
their own street, their own bad day at work — using that day's rule. Most recordings are short.
Six of them are gate recordings, one at the end of each phase, and those are longer and are made
to be listened to by someone else: a self-introduction, a shop role-play, a story from your life,
an opinion with reasons, an interview role-play, and finally an unscripted talk plus a recorded
conversation. The portfolio grows from "I can say my name" on day 1 to "I can hold a
conversation on a topic I did not choose" on day 120.

**The Writing Portfolio** is a folder of written pieces — on paper photographed, or typed, the
learner's choice. Every day ends with the learner's pen on the page: five sentences about
themselves, a note for the fridge, a message to a friend, a memory, an opinion, a complaint
letter, a cover letter, a full essay. Six of them are gate pieces, one per phase. The portfolio
grows from "I can write my name and address" to "I can write a page a stranger can follow
without asking me what I meant".

**How they grow across the phases.** Phase 1 builds the raw material: the sounds a listener
needs to hear, and the sentence a reader needs to see. Phase 2 puts both into daily life — shops,
messages, phones, notes. Phase 3 adds the past, which is where stories live. Phase 4 adds
opinion, plans and explanation. Phase 5 goes formal: work, letters, complaints, interviews. Phase
6 is fluency and the portfolio itself: rehearsals, retakes, and the final pieces.

**Why two, and why separate.** The learner asked for speaking and writing as two separate courses
inside one repository, with nothing in one depending on the other. The two tracks share a phase
theme so the repository reads as one course, but every speaking part stands alone from every
writing part on the same day, on its own topic, with its own rule and its own rep.

The artifact is what makes Principle 4 checkable. "Is this concept load-bearing?" has a mechanical
answer: delete it and see whether the artifact still works. Nothing here is learned in the
abstract and hoped to be useful later.

---

## 4 · Constraints & budget

**The session.** One hour a day, and this section is the only place in the repository that says
so. The hour is split in half by default: speaking first, then writing, or the other way round on
the days the learner prefers. **No day document carries a clock.** The plan's job is to make each
half fit an ordinary sitting by the size of its subject, never by telling the learner to hurry.
If a day does not fit, the fix is to split the day (an ADR), not to trim the parts.

**The learner.** A complete beginner. Every day assumes nothing that an earlier day did not
teach, and every earlier term is linked back on reuse. Model lines are short. Instructions are
in the plainest English the rule allows, with the learner's own language allowed for the
*thinking*, never for the rep.

**Tools.** A phone with a voice recorder. A notebook and a pen, or a plain text editor. A mirror.
Nothing else, and nothing that costs money. "Your phone's voice recorder" is the phrase, never a
product name.

**The recordings.** They stay on the learner's phone and in each day's `lab/` folder. Audio files
are gitignored; the written pieces in `lab/` are committed, because a portfolio that is not
versioned is a folder of drafts.

**No code.** This curriculum has no toolchain beyond `granth.py`, which checks documents. No day
contains a script, a snippet or a command the learner runs, other than the `granth.py` ritual
that closes the day.

**Size, not time, as the measure.** Where a gate needs a length, it is given in words for a
written piece and in spoken words or turns for a recording. A stranger can count words; nobody
should be watching a clock.

A constraint written down is a curriculum. A constraint discovered on day 40 is a rewrite.

---

## 5 · The baseline — what this plan is pinned to, and how it is verified

| What | Pinned to | Verified how | Re-checked |
| --- | --- | --- | --- |
| The toolchain | `granth.py`, stdlib only, Python 3.11 or newer; observed 3.12.10 on 2026-09-18 | `python --version` | every phase gate |
| The English taught | Standard everyday British/international English: full sentences, contractions allowed in speech and informal writing, none in formal writing. No dialect is taught as "correct" over another; the day names the choice where it matters | by reading, on every part; any published rule a part cites gets a dated row in `docs/SOURCES.md` | every phase gate |

**The verification rule (Principle 6), in three faces:**

- **Versions.** Read the version live before pinning it. Record package, version, the date it was
  observed, the day that added it and why, in `docs/PINS.md`. A failed lookup leaves
  `TODO(<the exact command>)`, never a guess. In this course the only version is Python's.
- **Interfaces.** Every rule a day states is checked against a published grammar or pronunciation
  reference **on the day it is used**, and the document names the page checked. If the live
  reference disagrees with this plan, **stop and propose an amendment** — do not adapt silently.
- **Citations.** Every source a day teaches or cites is opened live and its title copied from the
  record, never from memory, with a dated row in `docs/SOURCES.md`. This is the strictest of the
  three, because it fails the most quietly: a wrong version pin breaks the next install, while a
  plausible identifier attached to the wrong title survives for years. **Cite by title and
  identifier, never by author** (§12.5).

---

## 6 · The tracks and the ID scheme

Every concept in this plan has an ID. A day **closes** an ID when the concept is built into the
artifact — or demonstrably exercised against it — and the day's gates are green.
`docs/TRACEABILITY.md` is regenerated from the day hubs; **an open ID from a completed phase is a
bug**, not a backlog item.

Two tracks belong to the speaking folder and two to the writing folder. **Every day closes
exactly two IDs: one from `SND` or `SPK`, and one from `GRM` or `WRT`.** That is Principle 14 as
arithmetic.

<!-- granth:tracks:start -->

| Track | Prefix | Count | What runs through it |
| --- | --- | --- | --- |
| Sounds and rhythm | `SND` | 24 | The speaking folder's mechanics: the sounds a listener needs to hear, word stress, sentence rhythm, linking, intonation, pace, and the connected speech real people use. |
| Speaking | `SPK` | 96 | The speaking folder's substance: what to say and how to hold a turn — greetings to interviews, small talk to debate, always with the recorder on. |
| Grammar for writing | `GRM` | 47 | The writing folder's rules: the sentence, tenses, articles, plurals, questions, linking words, conditionals, the passive, punctuation — each taught the day a written piece needs it. |
| Writing | `WRT` | 73 | The writing folder's craft: from the alphabet and your name, through notes, messages, paragraphs and letters, to reports, reviews and a full essay. |

<!-- granth:tracks:end -->

**Total: 240 concept IDs.**

> Some IDs are **parked** — awareness-level, deliberately not built. You learn the map, you do not
> build the thing. A parked ID is marked in its day document and still closes normally. Parking is
> a decision recorded in the open, which is the opposite of a gap.

The authoritative statement of what an ID *means* is the row that assigns it in §8. This section
gives the shape; §8 gives the contract.

---

## 7 · The phases

A phase is a run of days that share one theme and end at one gate. The gate is the point: it is
where the work stops being a set of documents and has to behave.

<!-- granth:phases:start -->

| Phase | Days | Theme | The gate |
| --- | --- | --- | --- |
| 1 | 1–20 | Foundations: sounds and first sentences; letters and the sentence | Speaking: a recorded self-introduction of at least ten sentences that a stranger can follow. Writing: a ten-sentence page about yourself with a capital letter and a full stop on every sentence. |
| 2 | 21–40 | Everyday life: shops, phones, plans; notes, messages, short emails | Speaking: a recorded shop or café role-play, both voices yours, at least twelve turns. Writing: a hundred-word note that asks for something, thanks someone and gives a direction. |
| 3 | 41–60 | Telling what happened: the past, stories, comparing; paragraphs that hold together | Speaking: a recorded story from your life with a beginning, middle and end, at least two hundred spoken words. Writing: a one-page story in the past, in paragraphs, with speech marks used once. |
| 4 | 61–80 | Opinions, plans and explaining; arguing on the page | Speaking: a recorded opinion with three reasons and one counter-argument answered. Writing: a two-paragraph argument, one for and one against, with a topic sentence in each. |
| 5 | 81–100 | Formal and at work: interviews, meetings, complaints; formal letters and emails | Speaking: a recorded interview role-play answering five standard questions in full sentences. Writing: a formal email and a cover letter, both with the correct greeting, sign-off and no contractions. |
| 6 | 101–120 | Fluency and the portfolio: long turns, essays, rehearsals, retakes | Speaking: an unscripted talk of at least four hundred spoken words on a topic drawn at random, plus a recorded conversation. Writing: a five-paragraph essay of at least three hundred words, proofread against the day 113 checklist. Both portfolios indexed in full. |

<!-- granth:phases:end -->

Every phase gate also includes the freshness check (§9).

---

## 8 · The day map — day to IDs closed

> **The authoritative day-to-ID assignment.** A day document closes **exactly** these IDs — no
> more, no fewer. A day that wants to close a different ID is asking for a plan amendment, and the
> amendment is written before the day is.
>
> The table below is read by `granth.py` as well as by people, which is why it sits between
> markers. Keep the three columns and keep one row per day; everything else about it is free.
>
> **Reading a title.** Every title is two halves joined by ` · `: the speaking folder's subject,
> then the writing folder's subject. The folder slug is taken from the first half. The first ID is
> always the speaking one, the second always the writing one.

<!-- granth:day-map:start -->

### Phase 1 — Foundations: sounds and first sentences; letters and the sentence (days 1–20)

| Day | Title | IDs closed |
| --- | --- | --- |
| 1 | Short vowels: bit, bet, bat, but — saying your name aloud · The alphabet: capital and small letters, and your name on paper | SND-01, WRT-01 |
| 2 | Long vowels: beat, boot, bought — stretching the sound · Your address, your phone number and numbers as words | SND-02, WRT-02 |
| 3 | The two th sounds: think and this · The sentence: one capital letter, one full stop | SND-03, GRM-01 |
| 4 | V and W: very, wet — teeth on the lip or not · One and many: the plural -s and the ones that break it | SND-04, GRM-02 |
| 5 | R and L: rice, lice — where the tongue goes · A, an, the: which one and when none | SND-05, GRM-03 |
| 6 | Final consonants: bad, bat, back — finishing the word · I am, you are, he is: the verb be | SND-06, GRM-04 |
| 7 | Word stress: PHOto, phoTOgrapher — the loud syllable · Five sentences about yourself, each one true | SND-07, WRT-03 |
| 8 | Greetings and goodbyes: hello to see you later · This, that, these, those: pointing on paper | SPK-01, GRM-05 |
| 9 | Introducing yourself in five spoken sentences · Have and has: what you own and what you are like | SPK-02, GRM-06 |
| 10 | Numbers, times and dates out loud · Writing the date, the time and a one-line diary entry | SPK-03, WRT-04 |
| 11 | Asking what, where, who · Questions with be and do: the word order | SPK-04, GRM-07 |
| 12 | Yes/no questions and short answers · Not: making a sentence negative | SPK-05, GRM-08 |
| 13 | Sentence rhythm: the stressed words and the weak ones · Describing a person in one paragraph | SND-08, WRT-05 |
| 14 | Talking about your family · My, your, his, her, and the apostrophe s | SPK-06, GRM-09 |
| 15 | Talking about your daily routine · Present simple: the -s and always, usually, never | SPK-07, GRM-10 |
| 16 | Likes and dislikes: I love, I can't stand · A short "my day" paragraph in order | SPK-08, WRT-06 |
| 17 | Linking words together: an apple, not an-apple · Prepositions of place: in, on, under, next to | SND-09, GRM-11 |
| 18 | Describing where things are in your room · Describing your room on paper | SPK-09, WRT-07 |
| 19 | Can and can't: ability and permission aloud · Can and can't on paper, and the question form | SPK-10, GRM-12 |
| 20 | Gate: the recorded self-introduction · Gate: a ten-sentence page about you | SPK-11, WRT-08 |

### Phase 2 — Everyday life: shops, phones, plans; notes, messages, short emails (days 21–40)

| Day | Title | IDs closed |
| --- | --- | --- |
| 21 | At the shop: asking for things politely · A shopping list and a note for the fridge | SPK-12, WRT-09 |
| 22 | Ordering food and drink · Countable and uncountable: some, any, a piece of | SPK-13, GRM-13 |
| 23 | Asking for and understanding directions · Writing directions someone can follow | SPK-14, WRT-10 |
| 24 | Intonation: the voice going up and going down · Much, many, a lot of, a few, a little | SND-10, GRM-14 |
| 25 | Talking on the phone: opening, holding, closing · A text message and a short reply | SPK-15, WRT-11 |
| 26 | Making plans: shall we, let's, how about · Present continuous: what is happening now | SPK-16, GRM-15 |
| 27 | Saying what is happening around you right now · Describing a picture in a paragraph | SPK-17, WRT-12 |
| 28 | At the doctor: saying how you feel and where it hurts · Adjectives and their order: a small red car | SPK-18, GRM-16 |
| 29 | The weather and small talk with a stranger · A short email to a friend | SPK-19, WRT-13 |
| 30 | The schwa: the most common sound in English · There is, there are, there isn't | SND-11, GRM-17 |
| 31 | Asking for help and asking someone to repeat · Asking a question in writing, politely | SPK-20, WRT-14 |
| 32 | Giving instructions aloud: how to make tea · Imperatives and first, next, then, finally | SPK-21, GRM-18 |
| 33 | Talking about your job or your studies · A paragraph about your work or study | SPK-22, WRT-15 |
| 34 | Money, prices and asking for a better price · How much and how many questions | SPK-23, GRM-19 |
| 35 | Contractions aloud: I'm, don't, it's, we've · Contractions on paper and the apostrophe | SND-12, GRM-20 |
| 36 | Apologising and thanking, and answering both · A thank-you note and an apology note | SPK-24, WRT-16 |
| 37 | Saying you don't understand without stopping the talk · Object pronouns: me, him, her, them | SPK-25, GRM-21 |
| 38 | Talking about your hobbies and free time · A paragraph about what you enjoy and why | SPK-26, WRT-17 |
| 39 | Speaking at a steady pace, not fast · And, but, because, so: joining two sentences | SND-13, GRM-22 |
| 40 | Gate: the recorded shop or café role-play · Gate: a hundred-word note that does three things | SPK-27, WRT-18 |

### Phase 3 — Telling what happened: the past, stories, comparing; paragraphs that hold together (days 41–60)

| Day | Title | IDs closed |
| --- | --- | --- |
| 41 | What you did yesterday · Past simple: the regular -ed | SPK-28, GRM-23 |
| 42 | The three sounds of -ed: walked, played, wanted · Past simple: the irregular verbs you cannot avoid | SND-14, GRM-24 |
| 43 | A short story with a beginning, a middle and an end · A story in six sentences | SPK-29, WRT-19 |
| 44 | Time words aloud: first, then, after that, in the end · Past questions and negatives: did, didn't | SPK-30, GRM-25 |
| 45 | Talking about your childhood · A memory in one paragraph | SPK-31, WRT-20 |
| 46 | Describing a trip you took · Was, were, there was, there were | SPK-32, GRM-26 |
| 47 | Stress for emphasis: I said TUESday · The topic sentence: the first line says what the paragraph is about | SND-15, WRT-21 |
| 48 | A problem story: what went wrong and what you did · Past continuous: I was cooking when | SPK-33, GRM-27 |
| 49 | Saying what someone said to you · Writing a conversation with speech marks | SPK-34, WRT-22 |
| 50 | Talking about a film, a show or a book · Adjectives ending -ed and -ing: bored and boring | SPK-35, GRM-28 |
| 51 | Describing people: looks and character · Describing a person you know well | SPK-36, WRT-23 |
| 52 | Question intonation against statement intonation · Comparatives: -er and more | SND-16, GRM-29 |
| 53 | Comparing two things you know · Superlatives: the -est and the most | SPK-37, GRM-30 |
| 54 | Talking about your town or village · A paragraph about your town | SPK-38, WRT-24 |
| 55 | Did you hear about: passing on news · A short news report in the past | SPK-39, WRT-25 |
| 56 | Explaining why: because, so, that's why · When, while, after, before: joining past events | SPK-40, GRM-31 |
| 57 | Pausing in the right place · One idea per paragraph, and where the paragraph breaks | SND-17, WRT-26 |
| 58 | Retelling a story you heard · Retelling a story in your own words | SPK-41, WRT-27 |
| 59 | Talking about a mistake you made · Used to: things that were true and are not now | SPK-42, GRM-32 |
| 60 | Gate: the recorded story from your life · Gate: a one-page story in the past | SPK-43, WRT-28 |

### Phase 4 — Opinions, plans and explaining; arguing on the page (days 61–80)

| Day | Title | IDs closed |
| --- | --- | --- |
| 61 | Giving an opinion: I think, in my view, to be honest · Going to and will: plans and promises | SPK-44, GRM-33 |
| 62 | Agreeing and disagreeing without offending · An opinion paragraph with a reason | SPK-45, WRT-29 |
| 63 | Plans for the weekend and plans for the year · Present perfect: have you ever | SPK-46, GRM-34 |
| 64 | Have you ever: talking about experiences · A paragraph about things you have done | SPK-47, WRT-30 |
| 65 | Polite intonation: sounding kind, not cold · Should, must, have to: advice and rules on paper | SND-18, GRM-35 |
| 66 | Giving advice to a friend · A reply to a friend's problem | SPK-48, WRT-31 |
| 67 | Making suggestions and choosing between them · First conditional: if it rains, we'll stay in | SPK-49, GRM-36 |
| 68 | Talking about what might happen · Writing a plan step by step | SPK-50, WRT-32 |
| 69 | Describing a process aloud · The passive: it is made, it was built | SPK-51, GRM-37 |
| 70 | Explaining how something works to someone who doesn't know · Explaining a process in writing | SPK-52, WRT-33 |
| 71 | Holding a long turn: well, so, the thing is · Second conditional: if I were you | SND-19, GRM-38 |
| 72 | Dreams and wishes: if I could · A wish paragraph | SPK-53, WRT-34 |
| 73 | Reasons for and reasons against · For and against in two paragraphs | SPK-54, WRT-35 |
| 74 | Problems in your city and what should change · Relative clauses: who, which, that | SPK-55, GRM-39 |
| 75 | Describing a thing when you don't know its name · Defining and describing things on paper | SPK-56, WRT-36 |
| 76 | Speaking clearly on a bad line · Reported speech: she said that she was | SND-20, GRM-40 |
| 77 | Reporting what people said · Summarising a conversation in writing | SPK-57, WRT-37 |
| 78 | Interrupting politely and getting back on track · Editing your own writing: the second read | SPK-58, WRT-38 |
| 79 | A long turn on any topic · A hundred-and-fifty-word opinion piece | SPK-59, WRT-39 |
| 80 | Gate: the recorded opinion with reasons · Gate: the two-paragraph argument | SPK-60, WRT-40 |

### Phase 5 — Formal and at work: interviews, meetings, complaints; formal letters and emails (days 81–100)

| Day | Title | IDs closed |
| --- | --- | --- |
| 81 | Formal and informal: the same request said two ways · Formal and informal on paper: the same message written two ways | SPK-61, WRT-41 |
| 82 | Introducing yourself at work · A formal email: subject line, greeting, sign-off | SPK-62, WRT-42 |
| 83 | The job interview: tell me about yourself · A CV in plain sentences | SPK-63, WRT-43 |
| 84 | Answering the standard interview questions · A cover letter | SPK-64, WRT-44 |
| 85 | Sounding confident: volume, pace and the pause · Present perfect against past simple: which one on paper | SND-21, GRM-41 |
| 86 | Making a complaint politely and firmly · A complaint letter | SPK-65, WRT-45 |
| 87 | In a meeting: agreeing, asking, summarising · Meeting notes someone else can use | SPK-66, WRT-46 |
| 88 | Giving a short update on your work · A status update email | SPK-67, WRT-47 |
| 89 | Presenting: opening lines and closing lines · However, therefore, although: formal linking words | SPK-68, GRM-42 |
| 90 | Presenting: explaining a chart or a picture · Describing numbers and trends in words | SPK-69, WRT-48 |
| 91 | Stress in long words: PHOtograph, phoTOgraphy, photoGRAPHic · The passive in formal writing | SND-22, GRM-43 |
| 92 | Negotiating and asking for a better deal · A request email that gets a yes | SPK-70, WRT-49 |
| 93 | Saying no politely · Declining in writing | SPK-71, WRT-50 |
| 94 | Talking to a landlord, a bank or an office · Filling in forms and applications | SPK-72, WRT-51 |
| 95 | Dealing with an angry customer · Replying to a complaint | SPK-73, WRT-52 |
| 96 | Talking about health, safety and rules · Modals of obligation in written rules | SPK-74, GRM-44 |
| 97 | Numbers, dates and reference codes said clearly · Instructions and rules on paper | SND-23, WRT-53 |
| 98 | Explaining a technical thing to a beginner · Explaining a technical thing in writing | SPK-75, WRT-54 |
| 99 | A full talk with a structure: opening, three points, close · An essay plan | SPK-76, WRT-55 |
| 100 | Gate: the recorded interview role-play · Gate: a formal email and a cover letter | SPK-77, WRT-56 |

### Phase 6 — Fluency and the portfolio: long turns, essays, rehearsals, retakes (days 101–120)

| Day | Title | IDs closed |
| --- | --- | --- |
| 101 | Fluency: speaking without translating in your head · The essay introduction | SPK-78, WRT-57 |
| 102 | Idioms you actually hear, and the ones to leave alone · The body paragraph | SPK-79, WRT-58 |
| 103 | Telling a joke or an anecdote · The conclusion | SPK-80, WRT-59 |
| 104 | Connected speech: gonna, wanna, dunno — hearing it and choosing it · Third and mixed conditionals: if I had known | SND-24, GRM-45 |
| 105 | Debating: making a point and answering one · An argumentative essay | SPK-81, WRT-60 |
| 106 | Discussing the news and current topics · A summary of an article | SPK-82, WRT-61 |
| 107 | Describing feelings precisely · A descriptive essay | SPK-83, WRT-62 |
| 108 | Storytelling with suspense · A narrative essay | SPK-84, WRT-63 |
| 109 | Phrasal verbs in speech: put off, get over, run out of · Phrasal verbs in writing, and when to avoid them | SPK-85, GRM-46 |
| 110 | Hedging: sort of, I suppose, it depends · Punctuation: commas, colons, semicolons | SPK-86, GRM-47 |
| 111 | Talking about your own field at length · A report | SPK-87, WRT-64 |
| 112 | Answering hard questions on the spot · A review | SPK-88, WRT-65 |
| 113 | Self-correction while speaking · The proofreading checklist | SPK-89, WRT-66 |
| 114 | Listening back and fixing your own recording · Rewriting your day 20 page | SPK-90, WRT-67 |
| 115 | The long conversation: first rehearsal · The essay: first draft | SPK-91, WRT-68 |
| 116 | The long conversation: second rehearsal · The essay: second draft | SPK-92, WRT-69 |
| 117 | Recording the portfolio: retake the weakest piece · Assembling the writing portfolio | SPK-93, WRT-70 |
| 118 | The unscripted talk, no notes · The one-sitting page: write without stopping | SPK-94, WRT-71 |
| 119 | The final recorded conversation · The final essay | SPK-95, WRT-72 |
| 120 | Gate: the speaking portfolio review · Gate: the writing portfolio review | SPK-96, WRT-73 |

<!-- granth:day-map:end -->

---

## 9 · Phase gates and the freshness check

A phase is **green** only when all six hold:

1. Every day in the phase has its row in `docs/PROGRESS.md`, with gates green.
2. `docs/TRACEABILITY.md` shows **no open IDs** from this or any earlier phase.
3. `python granth.py check` passes on the whole repository — the depth contract for every written
   day, and the generated documents being current.
4. Every day in the phase has a `parts/` directory. A day with no `parts/` is not written (§11.2),
   so a phase containing one cannot be green.
5. The **freshness check** passes:
   - The gate recording exists on the phone and in the day's `lab/`, and has a row in
     `docs/RECORDINGS.md`. The gate page exists in `lab/` and has a row in `docs/WRITINGS.md`.
   - Every rule cited in the phase was checked against a live reference page on the day it was
     written; any that has since moved is re-checked.
   - Anything this plan pinned in §5 is re-read at its source. Moved? Amend first (Principle 8).
6. Every deviation is recorded: an ADR for anything structural, `docs/CHANGELOG_PLAN.md` for plan
   text. A deviation that is written down is a decision; one that is not is a defect.

**Never** skip a day, merge two days, or reorder days without an ADR.

**Writing ahead.** Days may be *written* ahead in batches of up to five, from the last closed day
forward with no gap. They are still *done* one at a time, in order, each with its own
`python granth.py done N` and its own commit, and a written-ahead day's failure parts say plainly
that they rest on common beginner errors rather than on this learner's ledger. See
`docs/adr/ADR-0003-days-written-ahead-in-batches.md`.

When the learner's access to the writing tool is not guaranteed, a batch may be up to **ten**
days and may start from the last *written* day, provided every day between the last closed day
and the last written day is fully written and passes `python granth.py depth N`. `docs/ERRORS.md`
is read before each `done N`, and a day whose failure parts miss the real pattern is amended
first. See `docs/adr/ADR-0004-batch-of-ten-from-the-last-written-day.md`.

Each such batch closes at its last day and the next one is argued for again, in its own ADR, so
that writing ahead stays a decision and never becomes the default. The second batch is days
17–26. See `docs/adr/ADR-0005-second-batch-of-ten-and-the-gate-day.md`.

**The phase gate day.** A gate day may be written ahead, but only as a **rehearsal of a gate**.
It teaches no new rule — a gate that teaches is not a gate. It points at the gate wording in §7
and never restates it more kindly, because a gate written early is not a gate made easier. And
its hub and its `CHECKLIST.md` carry a **mandatory, tickable re-read** of `docs/ERRORS.md` for
every day of the phase before `done N`, at which point its generic check lists are replaced by
this learner's real recurring mistakes. Until that box is ticked, a written-ahead gate day is a
rehearsal and says so (ADR-0005).

> A gate is never passed because time ran out (Principle 11). `python granth.py done N` is gated on
> a ticked checklist, a ledger row and green checks, and on nothing else.

**When a gate fails.** That is the gate working. Name two or three days from the phase to re-run;
re-runs get their own `PROGRESS.md` rows with a note. Never "catch up" by doubling: two days in one
sitting is one day of speaking and one day of reading.

---

## 10 · Ledgers and traceability

All ledgers live in `docs/`.

| File | Nature | The rule |
| --- | --- | --- |
| `docs/PROGRESS.md` | append-only | One row per completed day. **The last row is where we actually are.** |
| `docs/PINS.md` | append-only | Every version, tool or limit this project depends on: what, which value, the date observed, the day that added it, why. No invented values (Principle 6). |
| `docs/SOURCES.md` | append-only | Every source a document teaches or cites: exact title, identifier, year, URL, the date the record was checked, and which documents cite it. |
| `docs/GLOSSARY.md` | append-only | Every term, defined once, with the part that introduced it. This is what stops day 66 redefining a day 3 word slightly differently. |
| `docs/PROVENANCE.md` | append-only | Every third-party thing this project runs or vendors: source, licence, version, who audited it and when, and what it is permitted to touch — recorded **before** it first runs (Principle 12). |
| `docs/ERRORS.md` | append-only | Every mistake the learner caught on listening back or re-reading: the day, what was said or written, what it should have been. **The most valuable file here.** |
| `docs/RECORDINGS.md` | append-only | The Speaking Portfolio index: one row per gate recording and per retake. |
| `docs/WRITINGS.md` | append-only | The Writing Portfolio index: one row per gate piece and per rewrite. |
| `docs/CHANGELOG_PLAN.md` | append-only | Every amendment to this plan (Principle 8). Newest last. |
| `docs/adr/` | append-only | One file per structural decision, numbered, never rewritten. Superseded, not deleted. |
| `docs/TRACEABILITY.md` | **generated** | Every ID, its planned day, whether it is closed. |
| `docs/CURRICULUM_INDEX.md` | **generated** | The reverse lookup: where do I learn `SPK-14`? |
| `docs/TRACKER.md` | **generated** | What is written, how thick each day is, what is pending. |
| `docs/WIKI.md` + `docs/wiki/` | **generated** | One row per day, one page per day, plus the entity index. |

**Nine are written by hand and five are generated — do not confuse them.** Editing a generated
file only means the next `python granth.py index` silently overwrites you. The generated files are
an index *over* the days; every line in them is copied from a day document, and nothing in them is
written by a model. **If an index ever disagrees with the day it indexes, the day is right and the
index is stale** — regenerate it.

The append-only ledgers are written by the day you are finishing. Every hub ends with the exact
rows to paste (§11.5, section 11).

---

## 11 · The depth contract — how a day is written

> **Read this section in full before writing a single line of any day.** It carries the judgement
> no checker can make for you: the one-idea test, the standalone test, and whether a story is one
> the reader has plausibly lived.

### 11.1 The three commitments

Everything below follows from three sentences.

**One idea per document.** A subtopic that cannot be read alone, understood without scrolling past
a different subtopic, and explained back out loud is not one subtopic — it is several, badly
stacked. If a document needs the word "also" to introduce its second half, it is two documents.

**No clocks.** Nothing in a day folder carries a time estimate, a duration, an "estimated hours"
field or a pace. A reader may spend five sittings on one part. An explanation is **never** trimmed
because a day is getting long; the day gets another part instead.

**Zero to production, in one document.** Each part opens where a reader who has never heard of the
idea can stand, and ends where a professional stands: the real-system version, what breaks at
scale or under pressure, what a senior reviewer says, what an interviewer probes. In this course
"production" is *real life*: the real conversation, the real reader, the real consequence of
getting it wrong.

### 11.2 The folder shape

```text
days/day-NN-<day-slug>/
├── LESSON.md      # the hub: story · part map · setup · build brief · check · budget · ledger
├── CHECKLIST.md   # the definition of done; `python granth.py done N` refuses until it is ticked
├── parts/         # THE TEACHING — one document per subtopic, numbered <section>.<subtopic>
│   ├── 01-speaking/           # THE SPEAKING FOLDER — stands alone
│   │   ├── 1.1-<slug>.md
│   │   ├── 1.2-<slug>.md
│   │   └── 1.3-<slug>.md
│   └── 02-writing/            # THE WRITING FOLDER — stands alone
│       ├── 2.1-<slug>.md
│       ├── 2.2-<slug>.md
│       └── 2.3-<slug>.md
├── sources/       # one document per primary source (rare in this course — see §11.4.2)
└── lab/           # the learner's own work: the day's recording and the day's page
    ├── speaking/  # audio files — gitignored
    └── writing/   # the written piece — committed
```

**Line by line:**

- `days/day-NN-<day-slug>/` — the number zero-padded, then a kebab-case slug of **1–4 words** taken
  from the hub's `title` with articles dropped. A number alone is an address, not an answer, and
  120 of them are indistinguishable in a file tree, a tab strip or a `git log --stat`.
- `LESSON.md` — the hub. It orients and assembles; **it never teaches** (§11.5).
- `CHECKLIST.md` — the definition of done. Without it a day has no way to be finished.
- `parts/` — **mandatory**. A day without it is not written, and a phase containing such a day
  cannot be green.
- `parts/01-speaking/` — **always section 1, always this name.** Every part in it is about the
  day's `SND` or `SPK` ID and nothing else. It never links into `02-writing/`.
- `parts/02-writing/` — **always section 2, always this name.** Every part in it is about the
  day's `GRM` or `WRT` ID and nothing else. It never links into `01-speaking/`.
- `sources/` — beside `parts/`, never inside it. Present only on days whose ideas come from a
  citable primary document, which in this course is almost never.
- `lab/` — the learner's own work. Audio is gitignored; writing is committed, because the Writing
  Portfolio is the artifact.

**The number is the identity; the slug is a label on it.** Every tool resolves a day by number and
accepts any slug, so a folder can be renamed to a better slug at any time with a `git mv` and
nothing downstream notices. Part *filenames* never change — they already carry a full slug, and
renaming them would break every cross-part link for no gain.

### 11.3 The numbering rule — what `1.1` and `2.3` mean

A part filename is `<section>.<subtopic>-<kebab-slug>.md`.

- The **section** number is the folder: `1` is speaking, `2` is writing. **Every day has exactly
  these two sections.** A third section is a plan amendment.
- The **subtopic** number is reading order inside that folder. The default shape of each folder is
  three parts — **the rule, the rep, the deliberate failure** — but a folder gets as many parts as
  its idea needs (§11.7).
- Subtopics run `1..N` with no gaps inside each section. A gap means a document was deleted or
  never written, and nothing else in the repository would say so.
- The section folder's number and the number before the dot must agree.
- **Every part lives in its section's folder.** Never loose in `parts/`.
- **Links between parts are relative to the part's own folder**: a sibling is `1.2-<slug>.md`,
  the hub is `../../LESSON.md`. **A part never links across to the other folder** (Principle 14).

### 11.4 What a part document must contain

Eleven sections, **in this order**. Three are conditional — each is required exactly when its
trigger is present, and never asked for otherwise. Two headings are reworded for this course's
voice (the slot is the same; `granth.toml` carries the pattern): *The mechanism* is written as
**The rule**, and *In production* is written as **In real life**.

| # | Section | Required | What it is |
| --- | --- | --- | --- |
| 0 | **frontmatter** | always | `day`, `part`, `title`, `ids`, `level`, `prerequisites`, `prev`, `next`. Optionally `sources`, and `failure: true` on the day's deliberate-failure part. **No duration field of any kind.** |
| 1 | **One-line answer** | always | The rule in one sentence, before anything else. A reader who stops here has still learned something true. |
| 2 | **The story** | always | A concrete scene first: a person, a shop, a phone call, a misunderstanding. **No jargon at all.** Four rules — see §12.2. |
| 3 | **The idea in plain language** | always | The rule assuming zero prior knowledge; every term defined on first use, *including terms from earlier days*, with a link to the part that introduced them. No model lines yet. |
| 4 | **Why Vaani needs it** | always | The concrete later day, or the concrete gate recording or page, that breaks without this. Never "this is important". |
| 5 | **The source behind it** | when `sources:` is declared | An **address, not an explanation**: the citation block (exact title · identifier · year · URL, **no authors**), **one sentence** of the claim, and a **link to the source document that teaches it**. Nothing more. |
| 6 | **The rule** | always | How it actually works: the pattern, the model lines as blockquotes, the mouth position or the page layout, the diagram if it is spatial. Nothing skipped as "obvious". |
| 7 | **Line by line** | when the part carries a code block | Not expected in this course. A part with no fenced code block does not carry this section. |
| 8 | **The source in one demo** | source documents only | See §11.4.2. |
| 9 | **When it breaks** | always | The **real** wrong version: what a beginner actually says or writes, written out as it sounds or as it looks, what a listener or reader hears instead, and the smallest fix. |
| 10 | **In real life** | always | What a fluent speaker or writer does instead of the teaching version, what goes wrong under pressure — a fast speaker, an angry customer, a formal reader — and what a native listener notices. **Not optional.** |
| 11 | **Check yourself** | always | One thing to **record** or **write** now, in the learner's own words, and one question to answer out loud. This is where Principle 13 lives: the recorder is on, or the pen is moving. |

**Section 10 is the one that gets dropped, and dropping it halves the document.** A part that
shows the rule working on one model line and never says what happens in a real conversation has
taught half the subject.

#### 11.4.1 Five additional rules on every part

1. **Name what you checked.** The reference page, the dictionary entry, the pronunciation guide —
   with the date. "Verified" without an address is not verified.
2. **State the version, or leave the lookup command.** Never a remembered number (Principle 6).
3. **Respect the constraints in §4** in every instruction a reader is given: a phone, a notebook,
   a mirror, and nothing that costs money.
4. **Name the trap.** If the part touches a rule beginners commonly get backwards, a sound that
   the learner's first language does not have, or a word English spells one way and says another,
   say so where the reader would otherwise take the wrong turn.
5. **Never invent a citation.** Look the record up live, copy the title from the record and not
   from memory, and add a dated row to `docs/SOURCES.md`. Cite by **title and identifier, never by
   author** (§12.5).

#### 11.4.2 Source documents — one per primary source

This course teaches rules, not documents. Almost no day will carry a `sources/` folder. The rule
is kept for the rare case — a day that leans on a published pronunciation standard or a named
style guide — and it is the standard granth rule, unchanged:

When a day's ideas come from public primary documents, the day gets **one document per source**,
in `days/day-NN-<slug>/sources/`, **beside `parts/` and not inside it**, named `NN-<source-slug>.md`
and numbered from `01` in reading order. A source document is written to the same eleven-section
contract as any other part, with a part's frontmatter **minus `part`** and **plus `source:`**
(singular). Its *The source in one demo* section shows the source's claim on one model line with
the claim switched on and off — the ablation — with both versions written out. **A source is
taught once in the whole curriculum.** Two documents declaring the same identifier is a checker
failure.

### 11.5 What the hub (`LESSON.md`) must contain

The hub orients and assembles. **It never teaches** — no rule is explained here.

| # | Section | What it carries |
| --- | --- | --- |
| 0 | frontmatter | `day`, `phase`, `title`, `ids`, `kind`, `plan_version`, `parts`, `generated`, `status`, and whatever else the project tracks. No duration field. |
| 0 | blockquote | Yesterday / today / tomorrow, in three lines. No time estimate. |
| §1 | **Where we are** | A scene and an analogy. Plain language, no jargon. |
| §2 | **The map** | Two tables — **Speaking** and **Writing** — each with every part: number, linked title, what it answers, `level`. One line above each table saying what that folder is about today. **No minutes column, ever.** |
| §3 | **Setup** | What to have ready: the recorder, the notebook, the mirror, and the one thing this day needs (a photo to describe, a menu, a bill). |
| §4 | **Build brief** | The two reps of the day — the recording and the page — with `TODO(me)` markers left **unsolved**. |
| §5 | **The check that must be able to fail** | Listen back / read back: the one thing a stranger would catch. State how to make it go red on purpose. |
| §6 | **Budget** | What the day spends against §4: usually "one recording, one page, nothing bought". |
| §7 | **Traps** | The mistakes that eat an evening: the sound the learner's first language lacks, the rule that is backwards from their language, the spelling that lies. |
| §8 | **Verify before you build** | The reference pages actually opened today, with what each confirmed. |
| §9 | **Say it out loud** | One paragraph, spoken voice — the answer you would give a friend who asked what you learned today and why it matters. |
| §10 | **Done when** | A pointer to `CHECKLIST.md`. Defined by a recording that exists and a page that exists, never by elapsed effort. |
| §11 | **Ledger & commit** | The verbatim `PROGRESS.md` row, any `GLOSSARY.md` / `ERRORS.md` / `RECORDINGS.md` / `WRITINGS.md` rows, and the commit message. **The hub ends here.** |

The ritual in §11 is the point: the repository is the memory, and a memory that depends on
remembering to write it down is not one.

### 11.6 The `level` field — how a day climbs

Every part declares one:

| Level | The reader afterwards |
| --- | --- |
| `foundation` | knows what the rule is and can hear or see it |
| `working` | can use it in a sentence of their own, unaided |
| `production` | knows what changes in a real conversation or for a real reader, and what breaks |

**Each folder climbs.** A folder that is all `foundation` is a lecture. A folder that opens at
`production` has skipped the reader. The default three-part shape — rule (`foundation`), rep
(`working`), deliberate failure (`production`) — climbs by construction.

### 11.7 How finely to split

Split by **idea boundary, never by length or pace**. There is no target part count: three parts if
the folder needs three, seven if it needs seven.

Three tests, applied *before* writing:

- **The one-idea test.** If the part needs "also" to introduce its second half, it is two parts.
- **The standalone test.** A part must be readable cold. Name and link its prerequisite part —
  **inside the same folder, or on an earlier day's same folder**. Never across.
- **The no-shortcut test.** "For now, just accept that" is banned unless it links forward to the
  part that explains it. A deferred explanation must have an address.

The default shape of each folder:

| Part | Subject | Level |
| --- | --- | --- |
| `N.1` | the rule — what it is, how it sounds or looks, the model lines | `foundation` |
| `N.2` | the rep — the learner uses it on their own life, recorder on or pen moving | `working` |
| `N.3` | the deliberate failure — the wrong version, on purpose, heard or seen, then fixed | `production` |

**Every day carries at least one part whose subject is a deliberate failure** — say it wrong on
purpose, hear what a listener hears, fix it; or write it wrong on purpose, read what a reader
reads, fix it. That part declares `failure: true` in its frontmatter. The default is one in each
folder.

### 11.8 What "in depth" is not

The eight failure modes this format exists to prevent. If a part shows one, it is not done.

1. **Splitting without deepening** — the same wall of text, now in six files.
2. **Summary in place of explanation** — a description of the rule instead of the rule.
3. **Stopping at the toy example** — no `In real life`, so the reader learned a model line.
4. **Assuming the previous day** — an undefined term from day 12 used on day 51.
5. **A rule without failure** — a happy path with no wrong version anywhere.
6. **Trimming to fit** — an explanation cut because the day was getting long. Add a part instead.
7. **Solved reps** — the `TODO(me)` prompts answered for the reader, who then does none.
8. **A carried-over clock** — a duration field copied from an older draft.

And two that are this course's own:

9. **A rule the learner cannot hear or see** — a grammar point with no audible or visible
   consequence. If saying it wrong sounds the same and writing it wrong looks the same, it is not
   a rule for this course.
10. **A cross-folder lean** — "as you practised in the writing part". Principle 14: the folders
    never touch.

### 11.9 Enforcement

Run `python granth.py depth N` after writing a day. It fails on: a missing or misordered section, a
numbering gap, a bare numeric folder, a part loose in `parts/`, a malformed citation, a source
taught twice, a smuggled-in clock, a missing deliberate-failure part, a hub that carries teaching,
and a hub whose IDs disagree with §8.

**Never hand-wave past a `depth` failure.** The checker only knows the things a script can know;
everything it cannot check — whether the story is lived, whether the rule is audible, whether
`In real life` is true, whether the folders lean on each other — is checked by reading, and a
repository that argues with its own checker will not survive the reading either.

---

## 12 · The style guide

### 12.1 The register

**Storytelling is the default.** A scene before a rule, every time. The reader is learning this in
order to talk to real people and write to real people, so no rule stops at the model line.

**Simple language first.** The reader is a beginner in the language the document is written in.
Short sentences. Common words. Contractions. Second person: *you say*, *you write*. If a
twelve-year-old could not follow the first sentence, rewrite the first sentence.

**Model lines are blockquotes, never code blocks.** A code block is for code, and this course has
none. A model line looks like this:

> Hi, I'm Priya. I'm from Pune. Nice to meet you.

**Define every term on first use, including terms from earlier days**, with a link back to the
part that introduced them, and a row in `docs/GLOSSARY.md`. 120 days is long enough that day 3 is
forgotten by day 66. Grammar words — *noun*, *verb*, *tense* — are terms and get defined like any
other; a beginner does not know them.

**Grammar and punctuation are part of the deliverable**, in every section of every document.
Correct full stops and commas, no run-on sentences, and no long chain of dashes where two ordinary
sentences would read better. A sentence the reader has to parse twice has failed. In a language
course this is not style; it is the subject.

### 12.2 The story rules

The story is the hook the rule hangs on, not decoration. Four rules, and the first is the one
that gets broken:

1. **A scene the reader has plausibly lived.** A shop counter. A phone call to a landlord. A form
   at a bank. An auto-rickshaw and a wrong turn. A doctor's waiting room. A neighbour at the
   door. **Not** a boardroom in a film, a courtroom, a spaceship. Test: *could the reader have
   been standing in this scene themselves?* If they must first be told what the setting **is**,
   the analogy is carrying the explanation instead of hooking it.
2. **Simple words.** Short sentences beat clever ones here.
3. **Realistic and load-bearing.** The scene must contain the actual misunderstanding or decision
   the part teaches, not a pretty image the part then abandons. Every later section that reaches
   back for the scene must still fit it.
4. **One metaphor family per day.** Before choosing, grep the day's other parts and the hub's §1.
   Two parts reaching for the same family — two shops, two phone calls — read as one idea
   repeated. **The speaking folder and the writing folder may use different families;** they are
   separate courses.

### 12.3 The scene format

For failures and motivations, four beats:

> **The scene** — what someone was doing.
> **The naive fix** — what they reached for first, and why it was reasonable.
> **Why it fails** — the real failure, with what the listener or reader actually got.
> **The insight** — the thing that actually solves it.

### 12.4 Model lines and reps

- **Model lines are blockquotes.** Never code blocks. Never more than three in a row.
- **Every rule has a matching "When it breaks"** with the **real wrong version** written out as
  a beginner actually produces it, and what the listener or reader gets instead.
- **A diagram whenever the rule is spatial** — where the tongue goes, where the capital letter
  goes, the shape of a formal letter on the page.
- **Tables for enumerable facts, prose for reasoning.** Never a table of one row.
- **Leave `TODO(me)` reps unsolved.** Teach; do not do the reps for the reader. A rep is always
  about the learner's own life — their own street, their own family, their own bad day.
- **The rep is spoken or written, never read.** "Say it three times" is a rep. "Read the model
  line" is not.

### 12.5 Facts

- Never invent a rule, a spelling, a pronunciation or a citation (Principle 6).
- **Cite by title and identifier, never by author** — `spec:<name>-<revision>` for a named style
  guide or standard, `doi:` for a published paper. The identifier resolves to exactly one
  document, and it is what a reader types.
- A rule stated from memory is a `TODO` naming the reference page to check. **Never a plausible
  guess.**

### 12.6 The two things that are never written

1. **No clocks.** No duration, no "estimated hours", no "this should take about", no pace —
   anywhere, in any document, in any field (Principle 11). A recording's length is given in
   spoken words or turns, a page's in words.
2. **No person names, no course or creator brand names.** This curriculum is self-contained and
   promotes nobody: never name an instructor, author, channel, academy, app or training company —
   in a lesson, a checklist or a commit message. "Your phone's voice recorder", never a product.
   Names *inside model lines* — the Priya in a greeting — are fine; they are the learner's
   characters, not endorsements.

### 12.7 The ritual

Every day ends the same way: the recording exists, the page exists, paste the ledger rows, tick
the checklist, run the gate, commit. Not because ritual is virtuous, but because a repository that
records itself is a repository you can return to after three weeks away and still trust.

### 12.8 The language ladder

The learner is learning the language the documents are written in. So the English of the
*explanation* — not of the model lines, which are always real English — climbs with the learner,
phase by phase. A day is written at its phase's rung, never above it.

| Phase | Days | The English the explanation is written in |
| --- | --- | --- |
| 1 | 1–20 | The simplest the rule allows. Sentences of about ten words. The most common words only. One idea per sentence. Every hard word gets a plain meaning the first time it appears. |
| 2 | 21–40 | Still simple. Sentences may join with *and*, *but*, *because*. New words are still explained where they appear. |
| 3–4 | 41–80 | Ordinary plain English. Longer sentences are allowed when they read once. Hard words are still defined on first use. |
| 5–6 | 81–120 | Natural English, as a fluent colleague would write it. Terms are still defined and linked. |

Two rules hold on every rung. **Every part in phases 1–2 opens its *The idea in plain language*
section with a short *Words to know* list**: the three to six words in the part that a beginner
may not know, each with a plain meaning. And the register climbs only when the plan says; a day
that reads harder than its rung is a bug, and the fix is to rewrite the sentence, never to skip
the idea.

### 12.9 Sound links

A sound the learner cannot hear a model of is a sound they will copy from the page, which is not
a sound at all. So **every part that teaches a sound links, for each target word, a genuine,
free, live-checked reference page that carries a pronunciation button** — a learner's dictionary
entry — and names the free sound-video series where the learner can watch the mouth. The link is
opened on the day the part is written, the date is written beside it, and it gets a row in
`docs/SOURCES.md`. A part never links a page it did not open, and never claims a page carries a
sound it could not confirm. The learner's instruction is always the same: *listen, then say it
with the recorder on, then play both back*.

---

## 13 · Amendment record

This plan is amended, never quietly edited. Every amendment lands in `docs/CHANGELOG_PLAN.md`
before any day or any code changes, and anything structural gets an ADR in `docs/adr/`.

| Version | Date | What changed |
| --- | --- | --- |
| v1.0.0 | 2026-09-18 | Plan adopted. See `docs/adr/ADR-0001-the-plan-as-adopted.md`. |
| v1.1.0 | 2026-09-22 | §9: days may be written ahead in batches of five, done in order (ADR-0003). §12.8 the language ladder; §12.9 sound links. See `docs/CHANGELOG_PLAN.md`. |
| v1.2.0 | 2026-09-22 | §9: a batch may be up to ten days from the last written day when the writing tool's availability is not guaranteed (ADR-0004). See `docs/CHANGELOG_PLAN.md`. |
| v1.3.0 | 2026-09-22 | §9: a second batch of ten, days 17–26, and a phase gate day may be written ahead as a rehearsal, with a mandatory `ERRORS.md` re-read before `done N` (ADR-0005). See `docs/CHANGELOG_PLAN.md`. |
