# House style

How a note should read, how code is quoted inside one, and how commits are written.

The other rules: [Scope](scope.md), [Writing notes](notes.md). Back to the
[README](../README.md).

---

## Plain prose

Write the way you would explain it to somebody sitting next to you. Short paragraphs, present
tense, ordinary words.

Nobody here is being sold anything. A note does not need to open by establishing that its
subject is important, and it does not need to close by summarising itself. Say the thing.

## Two things never appear

**No em-dashes.** A comma, a colon, a full stop or a pair of brackets covers every case one
would have covered. This holds in notes, in headings, in image captions and in commit
messages.

**No emoji.** Not in headings, not as list markers, not as a status indicator. A word says the
same thing and survives being pasted somewhere else.

## Claims carry their source

If you write a number, say where it came from. Measured in a build, counted in the code, read
off a screenshot, or guessed. All four are fine. Which one it is changes what the next person
should do with it.

"The wave is too long" is an opinion and is welcome. "The wave is 4 seconds" is a fact and
needs a source. "The wave is 4 seconds and that is too long" is both, and the source belongs
on the first half.

## Name things the way the game names them

The SOUL, the arena, a wave, a turn, a boss, an encounter. Those words already mean specific
things in the engine, and using them loosely costs somebody an hour later.

The engine's [documentation](https://github.com/Stiven-Gjekaj/soulbound/tree/main/docs) has the
definitions. If you need a word the game does not have, invent one, then say what it means the
first time you use it.

## Code in a note

Code here is an illustration and never a source file. Fence it, label the language, keep it
short, and say what it is showing:

````markdown
Right now the wave gets four seconds regardless of how many bullets are on screen:

```lua
wavetimer = 4.0
```

Which means the crowded ones are the short ones, in practice.
````

Quote the smallest piece that makes the point. A whole file pasted into a note is a file
somebody will read as current, and it will not be current for long. Link to it in the game
repository instead, which stays right by itself.

## Disagreement stays visible

Two people who disagree write both positions down. Do not average them into a sentence that
neither of them would have written, and do not quietly drop the one that lost when the
argument ends. [Scope](scope.md) covers what happens to the losing option: it stays.

A note that reads as though everybody always agreed is a note that has thrown away its most
useful part.

## Commits

Same voice, same two prohibitions, and a subject stamped with this repository's own version:

```
[v4 - 2026-08-01] add the house style rules
```

The number goes up by one on every commit and never resets. The date is the day the commit was
made, written as `YYYY-MM-DD`. One stamp per subject, at the front.

This is not the game's scheme and does not track it. Soulbound stamps commits `v0.X.N`, where
`X` is a milestone and `N` counts commits inside it, because a milestone is a real thing there
with a start, an end, and a release at the end of it. This vault has no milestones and ships
nothing. Its numbers count writing, and the date is the part that tells you whether a note is
recent.

Small commits. One note, or one coherent change to one note, each time.

No trailers of any kind: no co-authors, no tooling footers, no links back to wherever the text
was written. The subject and the diff are the whole record.
