# Health and healing

How much health the player has, how much an item gives back, and why both of those are
proportions rather than fixed numbers.

Related: [gameplay](gameplay.md), [progression](progression.md),
[Illia](../bosses/illia.md) where the items are first taught.

## Settled

- **Healing items restore a percentage of max HP**, not a flat amount.
- **The three basic items heal 15, 40 and 65 percent**, being stim, bandage and med kit.
- **Fractions round up** to the nearest whole HP.
- **The player is shown the percentage** when they use an item, not the HP figure.
- **Max HP ramps up across the roster**, alongside difficulty.
- **Each boss sets the player's max HP for its own fight.** The player does not carry a growing
  total between fights.
- **Damage ramps with it.** How much, and per boss, is deferred to the fights that need it.

## Why percentages

A flat heal only works against one health total. The first version of the tutorial items was
20, 30 and 60 flat, against the engine's inherited max HP of 20, which made every one of them a
full heal and the three of them the same item.

A percentage never has that problem. A stim is worth the same fraction of the bar in the first
fight and the last one, so the items stay relevant without ever becoming mandatory, and nobody
has to retune the inventory every time a boss changes the numbers.

## The three items

| Item | Heals | At 20 max HP | At 60 max HP | At 100 max HP |
| ---- | ----- | ------------ | ------------ | ------------- |
| Stim | 15% | 3 | 9 | 15 |
| Bandage | 40% | 8 | 24 | 40 |
| Med kit | 65% | 13 | 39 | 65 |

Two properties of that spread are worth naming, because they are what make the ladder teach
something rather than just exist.

**The gaps are even, 25 points each.** The three are equally far apart, so no two of them are
close enough to be interchangeable at any health total. A stim is a top-up, a bandage is a
recovery, a med kit is an emergency, and the player can tell which is which without reading a
number.

**None of them is a full heal.** The largest is 65%, so no single item ever restores the bar
from empty. There is no "and now I am fine" button, only degrees of less bad, and a player who
wants to be topped up spends two turns on it. That does more to teach what ITEM costs than any
description would.

## Rounding

Fractions round up. 15% of 25 max HP is 3.75, which heals 4.

Rounding up is the friendlier direction and it does two useful things. It matters most at low
health totals, where the difference between 3 and 4 can be a whole extra hit survived, and it
guarantees every item always heals at least 1 HP, so no item can ever be a wasted turn no
matter how small the player's maximum gets.

## The player sees the percentage

Using an item reports what it healed as a percentage rather than as an HP figure.

That is the right way round, because the percentage is the part that stays true. The bandage
heals 40% in the first fight and the last one, so it is a fact the player learns once. The HP
figure it corresponds to changes with every boss, so quoting it would teach a number that stops
being true as soon as they move on. The health bar is already there for anyone who wants to
know where they actually stand. See [ui](../ui/ui.md).

## Max HP is set by the fight, and damage rises with it

Each boss sets the player's max HP for its own fight. Nothing is carried between fights.

That is the only version that survives free boss selection. Once
[Illia](../bosses/illia.md) is cleared the rest unlock together, so if max HP grew with clears
then fighting a boss first and fighting it last would be different fights, the order would have
an optimal solution, and a best time would depend on when in the run it was set. Setting it per
fight keeps every boss the same every time it is played, which is what the records assume.

It also puts the whole difficulty of a fight in one place. A boss decides how much health the
player brings, how much damage it deals, and therefore how many mistakes it forgives, and none
of those three can be tuned from outside the fight by accident.

Damage ramps alongside max HP, which is what stops the ramp from working backwards. The number
that matters to a player is how many hits the bar is worth:

- 20 max HP against 3 damage a hit is about seven hits.
- 60 max HP against 3 damage a hit is twenty hits.
- 60 max HP against 9 damage a hit is seven hits again.

Raising max HP alone would have made the later fights easier. Raising both keeps the count of
survivable mistakes under the boss's control, which is where it belongs.

So the reason to raise max HP is not survivability, it is **resolution**. At 20 HP there are
only a handful of meaningfully different damage values. At 100 there is room to say a graze
costs 4 and a direct hit costs 20, and for the player to feel the gap between them. The exact
numbers per boss are deferred to the fights that need them.

## Open questions

- **How many of each does the player carry?** The counts are unset. Against
  [Illia](../bosses/illia.md) it barely matters, since the rewind is unlimited and healing is
  not what decides her fight, but it is where the player learns that items run out, so the
  number is teaching something whether it was chosen or not.
- **What does Illia's fight set max HP to?** Every fight sets its own, and hers is the one the
  player meets first, so it is the total every percentage in the game gets read against on the
  first encounter.
- **Do items heal on the same turn they are used, or the next one?** A 65% heal that lands
  immediately and one that lands after the wave are different items with the same number.
