# Boss select

The screen the game opens on and returns to. It lists the bosses, shows what the player has
done against each one, and is the only place progression is visible.

Related: [ui](ui.md), [progression](../gameplay/progression.md) for the rules it displays,
[bosses](../bosses/bosses.md) for what it lists.

## Settled

- **A locked boss shows as greyed out, with its name, a silhouette and a question mark.** It is
  present rather than hidden, so the player can see how much game is waiting.
- **[Illia](../bosses/illia.md) is the only entry unlocked on a fresh save.** Clearing her
  unlocks the rest.
- **Once cleared she is relabelled the tutorial boss** rather than boss one, and stays
  replayable.
- **She still counts toward completion.** The relabel changes her label and nothing else.

## What the locked state is made of

Three elements were chosen together and they are not doing the same job, so it is worth being
clear which is which when the screen gets laid out:

- **Greyed out** says the entry is not available.
- **Its name** says the game is not hiding anything.
- **A silhouette** stands in for whatever art the boss has, so the slot has the same shape
  locked as unlocked and the layout does not jump when it changes.
- **A question mark** stands in for the records, which are the part that genuinely has no value
  yet.

Exactly how they sit together is a layout job, but the split above is the reasoning: the name
and the shape are known, the art and the records are not.

## What the screen has to show

Per boss, once unlocked: attempts, clears, deaths, best time, and whether it has been cleared
without taking a hit. All of it already exists in the save.

**Every boss's numbers are presented the same way.** No asterisks, no per-boss footnotes, and
no special case for the tutorial.

That was decided against the obvious objection. [Illia](../bosses/illia.md) revives the player
without limit and still records each death, so her count runs higher than anyone's, and the
reflex is to mark it out as a different kind of number. It is not one. Dying to the boss who
gives you the turn back is worse than dying to the boss who sends you to the start of the
fight, because the forgiving fight is the one you had every chance to survive. A high number
against her is accurate rather than misleading, and a second reading convention for one row
would cost the screen more than it explains.

Best time is not settled the same way, and the screen is where that shows. Whether a death is
charged to the clock is a per-boss checkpoint setting, and only Illia's is decided: hers runs,
which is the only reason her unloseable fight has a skill ceiling at all. Until the rest are
set, the best time column can quietly mean two different things depending on which row is being
read. See [progression](../gameplay/progression.md).

## Open questions

- **Does the relabel change her position in the list?** A tutorial boss sitting in the first
  slot forever is one reading. Moving her out of the numbered run is another.
- **Is the lock state visible before it matters?** On a fresh save every entry but one is
  greyed out, which is clear. What is less clear is whether the player is told why, or left to
  work out that clearing the first one is the key.
- **Does the screen say anything about checkpoints?** Each boss sets how far back a death sends
  the player, and the player currently has no way to learn that except by dying. See
  [progression](../gameplay/progression.md).
