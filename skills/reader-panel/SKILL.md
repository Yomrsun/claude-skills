---
name: reader-panel
description: Critiques a scene, chapter, opening pages or whole manuscript through a panel of distinct reader types, each scoring it 1-10 with specific notes, then reports the aggregate, the shape of the score, where the panel splits and what would raise it, separating fixable problems from genuine trade-offs. Use when a writer says "what would readers think", "give me honest feedback", "score this chapter", "reader panel", "rate my opening", "would this work for romance/thriller/fantasy readers", "critique this scene", "what's my weak spot", "is this ready for beta readers", "is this ready to query", or "how do I get this to a 10". Uses six fixed lenses plus genre-adaptive swaps (fair-play mystery reader, romance HEA reader, SFF worldbuilding reader, YA reader, authenticity reader and others). Simulated readers, not a substitute for real ones; good for a first pass before beta readers or querying.
version: 1.0.0
tags: [fiction, novel-writing, critique, feedback, editing, beta-reading]
---

# Reader Panel

One reader's opinion is noise. A panel of clearly defined reader types is signal,
because each type is tuned to a different failure mode. This skill runs a piece past
several lenses at once, scores it honestly, describes the shape of the response and
tells the writer exactly what would raise the score, and which improvements would
cost something the book's best readers love.

These are simulated readers. Use the panel before beta readers to fix what is
obviously fixable, so real readers spend their attention on what only humans can tell
you.

## Inputs
- The text (scene, chapter, first pages, synopsis plus chapters, or full manuscript).
- Genre, shelf and intended audience. If not given, infer them, state the inference,
  and proceed.
- Optional: the story bible, the writer's goals for the piece, specific worries.

## Step 1: Seat the panel
### Six fixed lenses (always seated)
1. **The genre superfan.** Knows the conventions cold. Rewards delivering on the
   premise's promise; punishes cliches, missed obligatory scenes and unearned beats.
2. **The craft reader.** Prose, structure, subtext, control of distance. Rewards
   precision and restraint; punishes overwriting and on-the-nose narration.
3. **The outsider.** Does not usually read this genre. Rewards universal hooks and
   clarity; punishes in-group assumptions, jargon and slow entry.
4. **The character reader.** Here for the people. Rewards feeling known and moved;
   punishes flat or interchangeable characters and feeling that is announced
   instead of earned.
5. **The adaptation scout.** Sees it as screen. Rewards visual moments, momentum and
   castable distinct characters; punishes interiority with no exterior action.
6. **The gatekeeper (agent or acquiring editor).** Thinks market. Rewards a clear
   hook, a confident voice in the first page and a reason to turn it; punishes a soft
   opening, a muddy premise and a manuscript that does not know its shelf.

### Genre-adaptive swaps (seat one or two; replace the adaptation scout first if the panel gets too large)
| Genre or need | Seat this reader | Tuned to |
|---|---|---|
| Mystery, crime | Fair-play mystery reader | Clues visible before the reveal; no cheating; solvable but not obvious |
| Thriller | Pace reader | Stakes per chapter, ticking clock, chapter-end pull, plausibility of action |
| Romance | HEA/HFN reader | Chemistry on the page, credible obstacle, emotional beats, the promised ending |
| Fantasy, SF | Worldbuilding reader | Rules with costs, exposition delivered through action, internal consistency |
| Horror | Dread reader | Escalation, restraint, what is withheld, the rules of the threat |
| YA, middle grade | Age-band reader | Authentic teen or child interiority, agency, voice that does not condescend |
| Literary, book club | Discussion reader | Ambiguity worth arguing about, thematic depth without stated theme |
| Historical | Period reader | Era-accurate detail, mindset of the time, anachronism in dialogue |
| Lived experience outside the writer's own | Authenticity reader | Specificity versus stereotype, insider texture, harm the writer may not see |
| Series book | Series reader | Recap load, payoff of earlier books, works for a new reader |

## Step 2: Read and annotate
Read the full text before scoring. For each panelist write 3-6 notes in that
reader's priorities. Every note must point at something specific: quote a line, name
a beat, cite a page or paragraph. "The prose is strong" is not a note. "The second
paragraph's list of three adjectives slows the entrance" is.

Each panelist covers: what lands, what costs points, and the single change that would
most raise their score.

## Step 3: Score honestly
Each panelist gives a 1-10 score with a one-line rationale. Use this scale and hold
to it:

| Score | Meaning |
|---|---|
| 9-10 | Exceptional; this reader would press it on friends. Rare. |
| 7-8 | Strong; publishable with targeted work. |
| 5-6 | Promising; a clear problem keeps it from working for this reader. |
| 3-4 | Not working for this reader; structural issue. |
| 1-2 | This reader would stop reading. |

Panelists should disagree; that is the point. If every score lands within one point
of the others, check whether you really applied each lens.

## Step 4: Aggregate and read the shape
1. **Mean and range.** Report both. A 7.0 with a 6-8 range and a 7.0 with a 4-10
   range are different books.
2. **Weighted score.** Weight the panelists who represent the target shelf (normally
   genre superfan and gatekeeper, plus any genre swap) double. Show the weights.
3. **Shape read.** Name the profile in plain words. Common shapes:
   - *High ceiling, narrow floor:* adored by its core readers, bounces others. Fine
     for a niche book; a risk for a book pitched broad.
   - *Broad and shallow:* nobody dislikes it, nobody loves it. Usually the most urgent
     to fix, because word of mouth needs someone to love it.
   - *Front-loaded / back-loaded:* the opening outscores the rest, or the reverse.
   - *Split by lens:* craft readers high, genre readers low (or reverse); the book
     may be on the wrong shelf.
4. **Where the panel splits.** A scene that scores 9 for the superfan and 4 for the
   outsider tells you exactly who it is failing. Say whether that reader matters for
   this book.

## Step 5: Fixable versus trade-off
Sort every improvement into one of two lists:
- **Fixable:** a change that raises some scores without lowering others (a confusing
  opening paragraph, a missing beat, an unclear stake, a flat secondary character).
- **Trade-off:** a change that would raise one reader's score by lowering another's
  (more worldbuilding explanation helps the outsider and bores the superfan; a
  faster pace helps the scout and costs the craft reader's texture).

For trade-offs, recommend which reader to serve based on the target shelf, and say
what the book would lose. Chasing every 10 flattens the work.

## Output format
```
## Reader Panel - [title of piece]
Shelf: [genre / category / audience]   Scope: [scene / chapter / manuscript]
Panel: [the six fixed lenses + swaps seated, and why]

### [Panelist name] - [score]/10
- What lands: ...
- What costs points: ...
- What would raise it: ...
- Verdict: one line in this reader's voice
(repeat per panelist)

### Aggregate
Mean X.X (range A-B)   Weighted X.X (weights: ...)
Shape: [shape read, two to four sentences]

### Where the panel splits
...

### Top 3 fixes (ranked by impact x effort)
1. [Fix] - which scores it moves - where in the text
2. ...
3. ...

### Trade-offs (decide, do not chase)
- [Change] helps [reader] / costs [reader]. Recommendation: ...

### What would get this to a 9 or 10
- Concrete changes aimed at the lowest target-shelf scores.
```

## Principles
- **Specific beats vague.** Every note is usable or it is cut.
- **Score honestly.** Inflation makes the panel worthless. Let the harsh panelist be
  harsh, and let a 9 be rare enough to mean something.
- **Judge the piece in front of you.** Score a first chapter as a first chapter, not
  as a finished novel, and say what it cannot yet be judged on.
- **End actionable.** The writer should leave knowing the two or three changes to
  make next.
- **Protect the core.** Never recommend a fix that betrays what the highest-scoring
  target readers love most.

Pairs with: **character-depth-pass** (fix thin characters the panel flags),
**story-architecture-pass** (structural problems), **deslop-pass** (prose-level
notes), **human-read-audit** (when the craft reader says it reads generic),
**beta-feedback-synthesizer** (compare the panel to what real readers said), and
**pitch-and-synopsis** (the gatekeeper's notes on hook and shelf feed the pitch).
