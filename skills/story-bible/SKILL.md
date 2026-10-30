---
name: story-bible
description: Creates and maintains a story bible, the single canonical source of truth for a novel or series. Use when a writer says "make a story bible", "series bible", "canon doc", "track my characters", "build my timeline", "keep my facts straight", "I keep contradicting myself", "what color were her eyes again", "set up a source of truth for my book", or is starting or resuming a novel and needs one home for names, ages, timeline, world rules, glossary, motif budgets, voice rules and open threads. Also use before a continuity check (the bible is what continuity-guard checks against), before planning a sequel, and when extracting canon from an existing draft. Produces a structured, maintainable bible from the included template, plus a list of open canon questions for the writer.
version: 1.0.0
tags: [fiction, novel-writing, story-bible, worldbuilding, continuity, series]
---

# Story Bible

A story bible is the contract a book keeps with itself. Its value comes from being
the one place each fact lives, updated the moment that fact becomes true, so that
three chapters (or three books) later nothing quietly contradicts it. Build it early,
keep it current, and every other skill in this pack gets more accurate.

The template lives at `assets/bible_template.md`. Save the working copy next to the
manuscript as `story-bible.md` so the other skills can find it.

## Method

### 1. Choose the mode
- **From scratch** (no pages yet): interview the writer section by section, fill what
  they know, and leave the rest as scaffolding. An empty section is a to-do, not a
  failure.
- **From a draft** (pages exist): read the draft and record what is already on the
  page. Do not invent. This is the more valuable mode, because the draft has already
  made promises the writer may not remember making.
- **Update** (bible exists): read the new or revised chapter, add new facts, and log
  every change in the continuity log with its chapter.

### 2. Extract canon (draft mode)
Read in order and capture, with the chapter where each fact first appears:
1. Every proper noun with its exact spelling, including nicknames, titles and
   honorifics. Note variants already present in the draft as questions, not as canon.
2. Every dated or datable event (explicit dates, "three winters later", "the night of
   the harvest fair"), plus durations and travel times.
3. Physical facts readers track: eye and hair color, scars, height, handedness, who
   wears glasses, who cannot swim.
4. Relationships and how characters address each other.
5. World rules: magic costs, technology limits, laws, what the town has and lacks.
6. Invented or foreign terms and how the book glosses them.
7. Repeated words, objects or rituals that carry deliberate weight (motifs).
8. Setups: anything introduced with a promise attached (a locked drawer, a debt, a
   rumor, a threat).

### 3. Anchor the timeline
List events by in-world date, not by chapter order. Give every major character a
birthdate (or an age at a fixed anchor event) and compute their age at each dated
scene. Age drift, a child who has not aged "two years later", is one of the
easiest canon breaks to make and one of the hardest to see in your own draft. If the book is non-linear, keep a second column for
the order the reader learns each event.

### 4. Set the motif budgets
If a word, object or ritual carries countable weight, record its budget and what each
use means. Example: a nickname the narrator uses exactly three times, once in
affection, once in anger, once at the graveside. Budgets become machine-checkable by
continuity-guard (`scan.py --bible` reads this table directly) and by
manuscript-builder's integrity check (copy the same numbers into
`book.config.json` under `motif_budgets`).

### 5. Record voice and style rules
Narrator, POV, tense and narrative distance per strand; formatting conventions
(italics for thoughts? scene-break symbol? how texts or letters are set); words and
tics the book has decided to avoid. Point to the writer's voiceprint file rather
than copying it.

### 6. Raise open questions
End every build or update with a short numbered list of canon questions the draft
leaves ambiguous ("Ch. 4 says the mill burned in spring; Ch. 11 says autumn. Which
is canon?"). Each question names both locations and offers a recommended answer.

### 7. Log as you go
Every new fact gets a continuity-log entry with its chapter. This is what makes the
bible trustworthy later and is the first place a sequel planner looks.

## Rules that keep a bible honest
- **One fact, one home.** If a detail lives in two places it will drift. Link, do not
  copy.
- **Record when the reader learned it.** The first-appearance chapter shows whether a
  reveal has already been spent and what a new reader of book two does not know.
- **Descriptive, not aspirational.** The bible records what is on the page. Planned
  changes go in a clearly marked "Pending revisions" note until the prose catches up.
  If prose and bible disagree, decide which is right and fix the other the same day.
- **Spell it once, spell it right.** The exact-spelling field is the one continuity
  tools match against. Accepted variants (a nickname, a formal title) must be listed,
  or the scan will flag them.
- **Scale with the book.** A tight thriller may need two pages; an epic fantasy may
  split the bible into separate files (characters, world, timeline) with this file as
  the index.

## Output format
1. The completed or updated `story-bible.md` (from the template).
2. **Changes this session**: bullet list of facts added or revised, each with its
   chapter.
3. **Open canon questions**: numbered, each with locations and a recommended answer.

Pairs with: **character-depth-pass** (fills the want/need/fear/wound engine and voice
tags), **continuity-guard** (checks chapters against this file), **series-planner**
(reads this file for canon locks), **write-in-your-voice** and
**story-architecture-pass** (draft and plan inside it), and **manuscript-builder**
(enforces motif budgets at build time).
