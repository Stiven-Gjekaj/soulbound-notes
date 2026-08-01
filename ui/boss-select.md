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
  replayable. She does not move.
- **She still counts toward completion.** The relabel changes her label and nothing else.
- **One screen holds seven bosses, and a screen is a batch.** The roster grows by screens.
- **Nothing explains the lock.** The player works out that clearing the first one opens the
  rest.
- **The screen says nothing about checkpoints.**

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

## A screen is a batch, and a batch is seven

The roster grows a screen at a time. Seven slots to a screen, one screen to a batch, and a new
batch is a new screen rather than a longer list.

This is the answer to what a live-service roster does to a fixed layout, and it is a better one
than scrolling. Seven entries can be laid out once and never rearranged, a batch has a natural
shape the player can see the whole of, and arrivals never disturb what is already there. It
also means the capstone fight that ends each batch has an obvious home: the last slot on its
own screen.

The first screen is Illia and six others. All six are unmade, so the near-term state of the
screen is one playable entry and six that are not yet anything, which is the same visual
treatment as locked and for a different reason. That is fine while there is one screen and
worth watching when there are two, because "locked until you clear something" and "not built
yet" should probably not look identical to a player who has paid.

## Nothing explains the lock

The player works it out. On a fresh save one entry is available and six are not, and clearing
the available one opens them.

That is the right amount of explanation for a screen with seven things on it, one of which is
obviously the way in. A line of text saying so would be telling the player something the layout
already said.

## Open questions

- **Does a locked entry and an unbuilt entry look the same?** They do at the moment, because
  both are just not available. Once a second batch is announced but not shipped, the difference
  between "you have not earned this" and "this does not exist yet" starts to matter.
- **What happens to completion when a screen is added?** A finished game becomes unfinished, and
  the count the player was reading changes underneath them. See
  [the Challenger](../general/the-challenger.md).
- **Do cleared screens stay reachable?** Seven per screen is clean until there are five screens
  and the player wants the boss on the second one.
