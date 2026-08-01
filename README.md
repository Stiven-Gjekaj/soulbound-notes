<div align="center">

# Soulbound Notes

### The discussion vault behind Soulbound

_Design notes, arguments, and the decisions they produced. Made by PaperTrail._

<p align="center">
  <a href="#what-this-is"><b>What This Is</b></a> |
  <a href="#what-goes-here"><b>What Goes Here</b></a> |
  <a href="#the-rules"><b>Rules</b></a> |
  <a href="#opening-the-vault"><b>Obsidian</b></a> |
  <a href="#how-notes-connect"><b>Linking</b></a> |
  <a href="#related"><b>Related</b></a>
</p>

</div>

---

## What this is

**Soulbound Notes** is the writing space for
[Soulbound](https://github.com/Stiven-Gjekaj/soulbound), a boss rush running on its own
Undertale-style battle engine. Developers, artists and testers all read and write here, in
the same files.

Nothing in this repository runs. There is no project to open, no build to produce, and no
file the engine loads. A note can contain code, and often should, but only as something to
point at while explaining an idea:

```lua
-- a wave's pacing, sketched in a note so it can be argued with
wavetimer = 4.0
arenasize = { 155, 130 }
```

That block is an illustration. It is not a file the game reads, and nobody can break a build
by editing it. Keeping the discussion out of the game repository is what makes that true, and
it is the rule everything else here follows from.

---

## What goes here

- Boss ideas: attacks, patterns, phases, and how a fight is meant to feel
- Arguments about difficulty and pacing, and what the player is being asked to learn
- Art direction: what a boss looks like, what a screen looks like, what the game reads as
- Decisions, written down with the reasoning behind them and the options that lost
- Open questions nobody has answered yet, which are worth writing down before they are

What does not:

- Working code, Lua or C#. That belongs in the game repository, where it is built and checked.
- Assets the game ships. Sprites, music and shaders belong beside the build that loads them.
- Bugs and tasks. Those are issues on the game repository, next to the code that has to change.

Nothing written here is load-bearing on its own. It becomes load-bearing only when somebody
acts on it, and the acting happens elsewhere.

---

## The rules

Three short pages, and they are the only rules this vault has.

| Page | What it settles |
| ---- | --------------- |
| [Scope](rules/scope.md) | What belongs here, what belongs with the code, and what happens to a discussion once it is settled |
| [Writing notes](rules/notes.md) | Naming, one subject per note, and the linking that keeps the graph worth looking at |
| [House style](rules/style.md) | How a note reads, how code is quoted inside one, and how commits are written |

---

## Opening the vault

The repository is an [Obsidian](https://obsidian.md) vault. Clone it, open Obsidian, choose
**Open folder as vault**, and point it at the clone. There are no plugins to install and no
settings to change.

Obsidian's own `.obsidian/` folder is not committed. It holds one person's window layout and
pane positions, which is not something to resolve conflicts over.

Every page is also readable on GitHub, in a browser, with no vault at all. That is deliberate,
and it is why notes link the way they do.

---

## How notes connect

Notes link to each other with ordinary Markdown links, `[text](rules/notes.md)`, rather than
Obsidian's `[[wikilink]]` syntax. Obsidian's graph counts both. GitHub renders only the first.
Ordinary links are the ones that work in both places at once.

This README is the hub. Every note is reachable from it and reaches back to it, directly or
through another note. A note nothing links to sits alone in the graph and will not be found
again, which is a slower way of not writing it.

```
README.md           this page, and the way in
rules/              how the vault works
  scope.md            what belongs here
  notes.md            how to write and connect a note
  style.md            how a note should read
```

Topic folders appear as they fill. A new note can sit at the root until there are three of its
kind, and then they get a folder together. [Writing notes](rules/notes.md) has the details.

---

## Related

[Soulbound](https://github.com/Stiven-Gjekaj/soulbound) is the game and the engine underneath
it. Its [README](https://github.com/Stiven-Gjekaj/soulbound#readme) covers what the game is,
its [changelog](https://github.com/Stiven-Gjekaj/soulbound/blob/main/CHANGELOG.md) covers what
changed, and its
[milestones](https://github.com/Stiven-Gjekaj/soulbound/blob/main/docs/project/milestones.md)
cover what is coming.

That repository answers what and when. This one answers why.

<div align="center">
<sub>Start with the <a href="rules/scope.md">rules</a>.</sub>
</div>
