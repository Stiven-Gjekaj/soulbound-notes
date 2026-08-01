# Progression and retries

What is locked, what unlocks it, and what changes the second time the player fights something.
These are rules the whole game obeys, decided while designing
[Illia](../bosses/illia.md) but not specific to her.

Related: [gameplay](gameplay.md), [boss select](../ui/boss-select.md) for the screen that shows
all of this, [ui](../ui/ui.md) for the rest of the screens.

## Settled

- **Every other boss is locked until Illia is cleared.** She is the tutorial, and a boss rush
  with a free select screen would otherwise let a first-time player open with boss three and
  meet none of it.
- **Once cleared, she stays on the select screen as the tutorial boss** rather than as boss
  number one. Her slot is relabelled, not removed. She stays replayable.
- **Dialogue is unskippable on the first run and skippable on every run after it.** Skipping
  jumps the whole dialogue block rather than speeding it up. The writing gets heard once, and
  after that it never stands between the player and a retry.
- **Death sends the player to their last checkpoint, and each boss sets where that is.** It is
  a per-boss dial rather than one global rule. [Illia](../bosses/illia.md) sets hers to one
  turn, the shortest possible, because she is the tutorial.
- **She counts toward completion.** Being relabelled the tutorial boss changes her label on the
  select screen and nothing else. If the game says four bosses cleared, she is one of the ones
  it is counting.

## Why the lock is the right shape

The alternative was to take the tutorial out of Illia and put it somewhere the player passes
through regardless. That would have kept the select screen free from the first launch, at the
cost of a separate tutorial to build and a first boss with nothing to teach.

Locking is cheaper and it costs the player almost nothing, because the thing behind the lock is
one two to four minute fight and clearing it is the intended first act anyway. The lock is only
ever felt by a returning player on a fresh save, and relabelling her afterwards is what stops
her looking like a boss they have to keep counting.

## What the game has to remember

Three pieces of state, all per save rather than per session:

- Whether Illia has been cleared, which drives the lock and the relabel.
- Whether the player has seen a given boss's dialogue, which drives the skip. Per boss, so the
  rule generalises to every boss added later without further thought.
- Everything already recorded per boss: attempts, clears, deaths, best time, no-hit.

The first two are new. Neither is expensive, and deciding them now means the boss select and
the save format get built once rather than retrofitted at boss four.

## Checkpoints are a per-boss dial

Every boss decides how far back a death sends the player, so "how forgiving is this fight"
becomes a property of the fight rather than of the game. Illia sets it to one turn and lifts
the limit on retries, which is what a tutorial should do. Nothing says any other boss is that
generous, and the sensible default for the rest is the start of the fight until somebody argues
otherwise.

Worth being deliberate about, because it is the difference between a boss rush that is a series
of tests and one that is a series of gauntlets, and the answer can differ per boss without the
game feeling inconsistent. What it cannot do is vary without the player being able to tell. If
one boss rewinds a turn and the next restarts the fight, the player finds that out by dying,
and they should find it out some other way first.

## Open questions

- **Where is each boss's checkpoint?** Illia's is decided. The rest are unset, and the default
  in everyone's head is currently "start of the fight" without that having been chosen.
- **How does the player know where the checkpoint is before they die?** A per-boss dial the
  player cannot see is a surprise rather than a rule.
- **Does the clock keep running through a death?** Records include a best time per boss, and a
  checkpoint that costs no time makes those times mean something different. See
  [Illia](../bosses/illia.md), whose unlimited rewind is the extreme case.
