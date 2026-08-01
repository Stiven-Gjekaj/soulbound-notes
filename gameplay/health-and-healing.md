# Health and healing

How much health the player has, how much an item gives back, and why both of those are
proportions rather than fixed numbers.

Related: [gameplay](gameplay.md), [progression](progression.md),
[Illia](../bosses/illia.md) where the items are first taught.

## Settled

- **Healing items restore a percentage of max HP**, not a flat amount.
- **Four healing items**, at 15, 40, 65 and 100 percent: stim, bandage, med kit and lifeline.
- **The player carries two, two, one and one of them**, weakest to strongest. Six items.
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
| Stim | 15% | 2 | 3 | 0.30 |
| Bandage | 40% | 2 | 8 | 0.80 |
| Med kit | 65% | 1 | 13 | 0.65 |
| Lifeline | 100% | 1 | 20 | 1.00 |
| **Total** | | **6** | | **2.75** |

Three properties of that spread are worth naming, because they are what make the ladder teach
something rather than just exist.

**The count runs inverse to the strength.** Two of the weakest, one of the strongest. Nobody
has to be told to save the lifeline, and nobody has to be told a stim is spendable. The
inventory explains its own economy by its shape, before a single description is read, which is
exactly what an inventory in a tutorial should do.

**The gaps are even, 25 points each, up to the lifeline.** No two of the first three are close
enough to be interchangeable at any health total. A stim is a top-up, a bandage is a recovery,
a med kit is an emergency. The fourth breaks the pattern by being the only one that finishes
the job, which is the right way for the rarest item to be different.

**Only the lifeline is a full heal.** The other three leave the player short no matter when
they are used, so topping the bar off costs either two turns or the one item there is no second
of.

## Why lifeline

The other three are objects: a chemical, a dressing, a box of supplies. The fourth is the only
one the player gets one of and the only one that finishes the job, so it should not read as a
bigger box. Lifeline names what it does rather than what it is, which is what separates it from
the ladder underneath it.

It also stays legible in a two column menu at 640x480, where "med kit" and any variation on
"trauma kit" or "medical kit" would be a glance apart from each other. Transfusion and panacea
were the other two considered: the first is long and the second belongs to a different register
than stim and bandage.

## Six items does not fit on one page

Worth being exact about, because the count was chosen partly to avoid paging and it does not.

The battle menu lays selections out in `mainTextManager.columnNumber` columns, which is 2 in
`TextManager.cs` and 2 on every text object in `Battle.unity`. `UIController.GetInventoryPage`
computes `itemsPerPage = 2 * columns`, so the ITEM menu shows **four items per page** and puts
a PAGE marker in the last cell when there are more. Six items is two pages. The engine's hard
cap, `Inventory.inventorySize`, is 8, so six is legal, just not one screen.

Three ways out, and the choice has not been made:

- **Four items total.** One of each, or two stims and one of the rest, fits a page exactly.
- **Accept two pages.** Six items with a PAGE marker, which the engine already handles.
- **Raise `columnNumber` to 3.** That yields six items per page, and also changes ACT to nine
  per page and reshapes every other selection menu in the game. The text box is 320 pixels
  wide, so three columns gives each name about a third of a line.

## What the smaller bag did to the FIGHT streak

Using an item costs the turn, and [Illia's](../bosses/illia.md) harder ultimate is triggered by
spending more than half the turns on FIGHT, so the two compete for the same resource. At ten
items that produced a real safety valve: a player committed enough to trigger the harder
ultimate had at most five spare turns and so reached it with at least five items unused.

At six items it barely holds. Five spare turns against six items means the same player can
arrive with one item left rather than five. The harder ending is still met with a slightly
fuller bag than the cautious player has, but "slightly" is the whole of it now, and the
compensation that used to be worth protecting is mostly gone.

That is not automatically wrong. The harder ultimate is a consequence and consequences are
allowed to cost something. It is only worth knowing that the cushion was removed by a change
that was about menu paging.

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

- **Four items on one page, six across two, or a three column menu?** See above. All three are
  workable and they are different amounts of work.
- **Do the counts hold for every boss, or only the tutorial?** Six uses and 2.75 bars of healing
  against a thirteen turn fight is forgiving. That is right for a tutorial and probably wrong
  for the fights behind it.
- **The engine already has something called Bandage.** `PlayerCharacter.cs` sets the default
  armour to `"Bandage"` and the default weapon to `"Stick"`, both inherited from upstream, and
  nothing in the Soulbound mod overrides either. As it stands the player would be wearing a
  bandage while carrying two more in the bag. One of the two names has to move.
- **Are the item names final?** Stim, bandage and med kit were placeholders and lifeline was
  chosen against them. If any of the first three change, the fourth should be re-checked
  against whatever replaces them, since its job is to sit outside their pattern.
