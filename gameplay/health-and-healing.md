# Health and healing

How much health the player has, how much an item gives back, and why both of those are
proportions rather than fixed numbers.

Related: [gameplay](gameplay.md), [progression](progression.md),
[Illia](../bosses/illia.md) where the items are first taught.

## Settled

- **Healing items restore a percentage of max HP**, not a flat amount.
- **Max HP ramps up across the roster**, alongside difficulty.

## Why percentages

A flat heal only works against one health total. The first version of the tutorial items was
20, 30 and 60 flat, against the engine's inherited max HP of 20, which made every one of them a
full heal and the three of them the same item.

A percentage never has that problem. A stim is worth the same fraction of the bar in the first
fight and the last one, so the items stay relevant without ever becoming mandatory, and nobody
has to retune the inventory every time a boss changes the numbers.

The three tutorial items read across directly, since the numbers already had the right shape:

| Item | Heals | At 20 max HP | At 100 max HP |
| ---- | ----- | ------------ | ------------- |
| Stim | 20% | 4 | 20 |
| Bandage | 30% | 6 | 30 |
| Med kit | 60% | 12 | 60 |

That is a reading of "make them percentages" rather than a separately chosen set, and it is
worth confirming before anyone builds it.

Percentages need a rounding rule, since HP is a whole number. Rounding up is the friendlier
default and it matters most at small totals, where the difference between 4 and 5 is a whole
extra hit.

## What percentages do not fix

Healing scales itself now. Damage does not, and damage is the number that actually decides how
hard a fight is.

What matters to a player is how many hits the bar is worth:

- 20 max HP against 3 damage a hit is about seven hits.
- 60 max HP against 3 damage a hit is twenty hits.
- 60 max HP against 9 damage a hit is seven hits again.

So raising max HP on its own makes the later fights **easier**, which is backwards. If max HP
ramps, damage has to ramp with it, or the ramp is undoing the difficulty curve it was meant to
support.

Which means the honest reason to raise max HP is not survivability, it is **resolution**. At 20
HP there are only a few meaningfully different damage values. At 100 there is room to say that
a graze costs 4 and a direct hit costs 20, and for the player to feel the difference. That is a
good reason. It is just a different reason from the one it looks like.

## Where max HP is set

The reading here is that **each boss sets the player's max HP for its own fight**, rather than
the player carrying a growing total between fights.

That is the only version that survives free boss selection. Once
[Illia](../bosses/illia.md) is cleared the rest unlock together, so if max HP grew with clears
then fighting a boss first and fighting it last would be different fights, the order would
have an optimal solution, and a best time would depend on when in the run it was set. Setting
it per fight keeps every boss the same every time it is played, which is what the records
assume.

It also puts the whole difficulty of a fight in one place: the boss decides how much health the
player brings, how much damage it deals, and therefore how many mistakes it forgives.

## Open questions

- **Are the percentages 20, 30 and 60?** They are read straight across from the flat numbers.
  Confirming is cheap and building on a guess is not.
- **Does damage ramp with max HP?** If it does not, the ramp makes the game easier the further
  in the player gets. This is the question that decides whether the ramp works at all.
- **Is max HP per fight or carried between fights?** Per fight is assumed above, for the
  reasons given, and it has not actually been decided.
- **Does the player see the percentage or the number?** The health bar shows a number today. An
  item that says it heals 30% is honest about the system, and one that says it heals 6 is
  honest about the fight.
- **Do the items round up or down?** Up is assumed. At small health totals it is the difference
  between an item being worth an extra hit or not.
