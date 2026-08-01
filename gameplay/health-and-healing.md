# Health and healing

How much health the player has, how much an item gives back, and why both of those are
proportions rather than fixed numbers.

Related: [gameplay](gameplay.md), [progression](progression.md),
[Illia](../bosses/illia.md) where the items are first taught.

## Settled

- **Healing items restore a percentage of max HP**, not a flat amount.
- **Four healing items**, at 15, 40, 65 and 100 percent. The first three are stim, bandage and
  med kit. The fourth has no name yet.
- **The player carries four, three, two and one of them**, weakest to strongest.
- **Fractions round up** to the nearest whole HP.
- **An item heals on the turn it is used**, before the wave rather than after it.
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

## The four items

| Item | Heals | Carried | At 20 max HP | Whole bars carried |
| ---- | ----- | ------- | ------------ | ------------------ |
| Stim | 15% | 4 | 3 | 0.60 |
| Bandage | 40% | 3 | 8 | 1.20 |
| Med kit | 65% | 2 | 13 | 1.30 |
| The full heal | 100% | 1 | 20 | 1.00 |
| **Total** | | **10** | | **4.10** |

Three properties of that spread are worth naming, because they are what make the ladder teach
something rather than just exist.

**The count runs inverse to the strength.** Four of the weakest, one of the strongest. Nobody
has to be told to save the full heal, and nobody has to be told a stim is spendable. The
inventory explains its own economy by its shape, before a single description is read, which is
exactly what an inventory in a tutorial should do.

**The gaps are even, 25 points each, up to the full heal.** No two of the first three are close
enough to be interchangeable at any health total. A stim is a top-up, a bandage is a recovery,
a med kit is an emergency. The fourth breaks the pattern by being the only one that finishes
the job, which is the right way for the rarest item to be different.

**Only the fourth is a full heal.** The other three leave the player short no matter when they
are used, so topping the bar off costs either two turns or the one item there is no second of.

## The FIGHT streak pays for itself

An interaction worth being aware of, since it falls out of decisions already made rather than
being designed.

Using an item costs the turn, and [Illia's](../bosses/illia.md) harder ultimate is triggered by
spending more than half the turns on FIGHT. Those two compete for the same resource. Against
her thirteen turns, a player committed enough to trigger the harder ultimate has spent seven or
more turns attacking, leaving at most five for anything else, so they reach it having used at
most half their inventory.

The result is self-balancing without anybody balancing it. The harder ultimate is always faced
with the fuller bag, and the player who healed their way through the fight faces the easier one
with less left. That is worth protecting if the turn count or the threshold ever moves.

## Rounding

Fractions round up. 15% of 25 max HP is 3.75, which heals 4.

Rounding up is the friendlier direction and it does two useful things. It matters most at low
health totals, where the difference between 3 and 4 can be a whole extra hit survived, and it
guarantees every item always heals at least 1 HP, so no item can ever be a wasted turn no
matter how small the player's maximum gets.

## Healing lands on the turn it is spent

An item takes effect immediately, before the wave that turn produces, rather than resolving
afterwards.

That makes ITEM a reactive option rather than only a pre-emptive one. A player who came out of
the last wave on two HP can fix it before the next one starts, instead of having to have
predicted it a turn early. It is the difference between an inventory that rewards foresight and
one that punishes its absence, and for the fight that teaches the menu it should be the former.

The cost is the turn. Using an item is a turn not spent on anything else, which is the whole
price and is enough of one.

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

- **What is the fourth item called?** It is the only one without even a placeholder, and it is
  the one the player will remember, since it is the one they get exactly one of. A
  [writing](../writing/writing.md) job.
- **Do the counts hold for every boss, or only the tutorial?** Four, three, two and one is
  generous: ten uses and four full bars of healing against a thirteen turn fight. That is right
  for a tutorial and almost certainly wrong for the fights behind it.
- **Does the inventory refill between attempts?** With an unlimited rewind, a bag that does not
  refill turns into the real failure state of a fight that has no other one.
