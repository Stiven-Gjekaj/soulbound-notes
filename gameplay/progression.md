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
- **Death sends the player to their last checkpoint, and each boss sets where that is and
  whether the clock keeps running.** Both are per-boss dials rather than global rules.
  [Illia](../bosses/illia.md) sets one turn, unlimited retries, and a clock that never stops.
- **A checkpoint restores state and not just position.** Health, inventory and turn all go back
  to what they were when it was reached. See
  [health and healing](health-and-healing.md).
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

## Checkpoints are a per-boss dial, with two settings

A checkpoint is not one number. Each boss sets both:

- **How far back a death sends the player.** Illia sets one turn. The default for everyone else
  is the start of the fight until somebody argues otherwise.
- **Whether the clock keeps running through the death.** Illia's does, which is what gives her
  otherwise unloseable fight a skill ceiling. This is hers rather than a game-wide rule.

So "how forgiving is this fight" is a property of the fight rather than of the game, and the
two settings can be mixed. A boss with a generous checkpoint and a running clock is testing
speed. One with a harsh checkpoint and a paused clock is testing survival and nothing else.
That is a genuinely useful pair of dials, and it is worth using deliberately rather than
setting both to the same thing everywhere.

The pair does have a cost worth naming. Death counts are presented identically for every boss,
on the argument that a death is a death and the forgiving fight is the one you had every chance
to survive. Best time does not get that treatment automatically: if one boss charges its deaths
to the clock and the next does not, the column means two different things. The two records are
being held to different standards, and that is a choice rather than an oversight only if it is
made on purpose.

Worth being deliberate about, because it is the difference between a boss rush that is a series
of tests and one that is a series of gauntlets, and the answer can differ per boss without the
game feeling inconsistent. What it cannot do is vary without the player being able to tell. If
one boss rewinds a turn and the next restarts the fight, the player finds that out by dying,
and they should find it out some other way first.

## Checkpoints announce themselves

Reaching a checkpoint shows a notification in the top left of the screen. That is how the
player learns the rule: not from a tooltip and not from dying, but from the game telling them
the moment it becomes true.

It is the right corner for it. The arena is centre-low, the boss sits above it, and the top
left is the one part of a battle screen nothing else is using, so a notification there is
visible without competing with anything the player has to read to survive.

It does mean the notification carries the whole feature. A player who misses it has no other
way to find out, and a fight whose checkpoint is the start of the battle presumably never shows
one, so its absence has to be as legible as its presence. Whether "no notification" reads as
"no checkpoints here" or as "you missed it" is a [ui](../ui/ui.md) problem.

Whether a given boss charges deaths to its clock is deliberately not surfaced. It is a
per-boss setting, and it was decided that the resulting inconsistency between best times does
not matter enough to design around.

## Open questions

- **Where is each boss's checkpoint?** Illia's is one turn. The rest get decided with the boss
  they belong to rather than up front.
- **What does the notification say, and how long does it stay?** It is the only place this
  system is explained, so it is carrying more than a notification usually does.
