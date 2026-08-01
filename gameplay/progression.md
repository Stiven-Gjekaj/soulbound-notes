# Progression and retries

What is locked, what unlocks it, and what changes the second time the player fights something.
These are rules the whole game obeys, decided while designing
[Illia](../bosses/illia.md) but not specific to her.

Related: [gameplay](gameplay.md), [ui](../ui/ui.md) for how the boss select shows any of this.

## Settled

- **Every other boss is locked until Illia is cleared.** She is the tutorial, and a boss rush
  with a free select screen would otherwise let a first-time player open with boss three and
  meet none of it.
- **Once cleared, she stays on the select screen as the tutorial boss** rather than as boss
  number one. Her slot is relabelled, not removed. She stays replayable.
- **Dialogue is unskippable on the first run and skippable on every run after it.** The writing
  gets heard once, and after that it never stands between the player and a retry.

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

## Open questions

- **What does a locked boss look like on the select screen?** Greyed out with its name showing,
  a silhouette, a question mark, or absent entirely. Each one tells the player a different
  amount about how much game is waiting. This is a [ui](../ui/ui.md) decision.
- **What does skipping actually do?** Jump the whole dialogue block, fast-forward it while a
  key is held, or step it line by line faster than normal. The first is what a player retrying
  for the sixth time wants, and the third is what someone who half-remembers it wants.
- **Does the tutorial boss count toward completion?** If the game ever says "four of seven
  bosses cleared", relabelling her raises the question of whether she is one of the seven.
- **What does dying cost anywhere other than the tutorial?** Illia revives the player at the
  turn before, which is hers and which makes her fight nearly unloseable. Every other boss is
  currently assumed to be a normal death and a retry from the start, but that is an assumption
  nobody has made on purpose. See [Illia](../bosses/illia.md).
