# Scope

What belongs in this vault, what belongs with the code, and what happens to a discussion once
it has been settled.

The other rules: [Writing notes](notes.md), [House style](style.md). Back to the
[README](../README.md).

---

## The one rule

Nothing here runs.

This vault holds writing about the game. The game itself, the engine underneath it, its assets
and its issue tracker all live in
[the game repository](https://github.com/Stiven-Gjekaj/soulbound). Two repositories, and the
line between them is whether a thing is executed.

Code is welcome in a note as an illustration. Quote a function to explain what it currently
does. Sketch a wave to show the pattern you are describing. Paste an error to ask why it
happens. What you cannot do is treat this vault as a place where a change is made. A note is
never the version of record for anything that ships.

## Why the split

The game repository is built by CI on every push, released from tags, and read by anyone who
downloads a build. Everything in it is either shipped or checked, which is a useful property
and an expensive one to keep. Discussion does not survive that setting: half-formed ideas,
rejected options and open arguments would each have to pass a review whose whole purpose is to
protect a build.

Here none of that applies. A note can be wrong. Two notes can contradict each other. A note
can stop mid-argument because whoever was writing it ran out of certainty. That freedom is the
reason this repository exists separately, and it stops being free the moment something here
can break something there.

## What belongs here

- Boss design: attacks, patterns, phases, the shape of a fight, the order things are taught in
- Difficulty and pacing, including the parts that are only a feeling until somebody writes them down
- Art direction: silhouettes, palettes, what a screen looks like, what the game reads as
- Player experience: what is confusing, what is unfair, what is unfair in a good way
- Decisions and the reasoning that produced them
- Open questions, which are worth a note before they have an answer rather than after

## What belongs with the code

- Lua and C# that the game actually loads
- Sprites, music, shaders and fonts that ship in a build
- Bug reports, tasks and anything with a definition of done
- Engine documentation, which is reference material rather than discussion

A note that would break something if it were wrong is in the wrong repository.

## Who writes here

Developers, artists and testers, in the same files, with no separate track for any of them.

You do not need to read C# or Lua to write here, and a note is not better for containing
either. "The second phase feels unfair because you cannot see the next attack coming" is a
complete and useful note. Working out which line causes that is a different job, done
somewhere else, by whoever picks up the issue.

## From a discussion to a decision

A discussion is finished when somebody can act on it. At that point:

1. The note states what was decided, in a sentence, near the top.
2. It keeps the options that lost and why they lost. That record is the reason any of it was
   worth writing.
3. The work moves to the game repository as an issue, and the issue links back to the note.

The note stays where it is. Six months later somebody asks again why the boss opens with the
slow pattern instead of the fast one, and the answer is either written down here or gone.

## Nothing is deleted

An idea that lost is the reason the current one won. Mark the note settled, link to whatever
replaced it, and leave it in place.

The exception is a file that was never about the game: scratch text, a duplicate, something
created by accident. Those can go.
