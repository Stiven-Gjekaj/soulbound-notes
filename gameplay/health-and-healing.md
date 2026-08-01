# Health and healing

How much health the player has, how much an item gives back, and why both of those are
proportions rather than fixed numbers.

Related: [gameplay](gameplay.md), [progression](progression.md),
[Illia](../bosses/illia.md) where the items are first taught.

## Settled

- **Healing items restore a percentage of max HP**, not a flat amount.
- **Four healing items**, at 15, 40, 65 and 100 percent: stim, bandage, med kit and hope.
- **The player carries two, two, one and one of them**, weakest to strongest. Six items, and
  the same six for every boss unless a perk says otherwise.
- **Fractions round up** to the nearest whole HP.
- **An item heals on the turn it is used**, before the wave rather than after it.
- **The inventory is restored by the checkpoint**, to whatever it held when the checkpoint was
  reached. A checkpoint at the start of a battle therefore refills it.
- **The player is shown the percentage** when they use an item, not the HP figure.
- **Six items across two menu pages**, ordered weakest to strongest. The ITEM menu holds four,
  and paging is accepted rather than designed around.
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
| Hope | 100% | 1 | 20 | 1.00 |
| **Total** | | **6** | | **2.75** |

Three properties of that spread are worth naming, because they are what make the ladder teach
something rather than just exist.

**The count runs inverse to the strength.** Two of the weakest, one of the strongest. Nobody
has to be told to save the hope, and nobody has to be told a stim is spendable. The
inventory explains its own economy by its shape, before a single description is read, which is
exactly what an inventory in a tutorial should do.

**The gaps are even, 25 points each, up to the hope.** No two of the first three are close
enough to be interchangeable at any health total. A stim is a top-up, a bandage is a recovery,
a med kit is an emergency. The fourth breaks the pattern by being the only one that finishes
the job, which is the right way for the rarest item to be different.

**Only the hope is a full heal.** The other three leave the player short no matter when
they are used, so topping the bar off costs either two turns or the one item there is no second
of.

## Why hope

The other three are objects: a chemical, a dressing, a box of supplies. The fourth is the only
one the player gets one of and the only one that finishes the job, so it should not read as a
bigger box.

Hope is not an object at all. It is not even a thing that does something, the way a lifeline or
a transfusion would be. It leaves the ladder rather than topping it, and that break is doing
the work: the item that is different in every mechanical way is also the only one whose name
belongs to a different kind of word. A player reading the list knows which one matters before
they know what any of them heal.

It fits the game it is in, too. Soulbound is a game about souls, and a full restore called Hope
is the sort of thing this game gets to mean. The other three could belong to anything.

It is also four characters long, which quietly removes it from the menu width problem below.

**What lost:** lifeline, transfusion and panacea. Lifeline named the function rather than the
object, which was the right instinct and half the distance. Transfusion was long for a two
column menu. Panacea was the closest, and lost on sounding like it came from a different game
than the one with a stim and a bandage in it.

## Six items does not fit on one page

Worth being exact about, because the count was chosen partly to avoid paging and it does not.

The battle menu lays selections out in `mainTextManager.columnNumber` columns, which is 2 in
`TextManager.cs` and 2 on every text object in `Battle.unity`. `UIController.GetInventoryPage`
computes `itemsPerPage = 2 * columns`, so the ITEM menu shows **four items per page** and puts
a PAGE marker in the last cell when there are more. Six items is two pages. The engine's hard
cap, `Inventory.inventorySize`, is 8, so six is legal, just not one screen.

### Three columns would not fix it on its own

Raising `columnNumber` to 3 gives six items a page arithmetically, and breaks the layout.

The menu does not compute column positions. `SelectMessage` builds the row by inserting tab
characters, and `TextManager` renders a tab as `currentX = ++tabCount * columnShift`, where
`columnShift` is a separate serialised field sitting at **265**. So columns land at x = 0, 265
and 530, and the engine's own width calculation in `UnitaleUtil` is
`columnShift * columns`, which for three columns is **795 pixels on a 640 pixel screen**. The
third column renders off the right edge. `SetPlayerOnSelection` uses the same figure to place
the SOUL, so the cursor would follow it off the screen.

The menu *logic* generalises fine. `GetInventoryPage` is written as `2 * columns`, `GetActPage`
as `3 * columns`, the PAGE marker as `3 * columns - 1`, and `SelectionChoice` takes rows and
columns as arguments. Nothing assumes two except the pixels.

So three columns costs a `columnShift` change as well, down to about 176 to fit three columns
in the span two currently occupy. That is a third less width per name in every selection menu
in the game, and it also turns ACT into nine options a page and reshapes MERCY and enemy
select, because all four menus read the same two fields.

### Two pages, accepted

Six items across two pages. The engine already handles the paging and the PAGE marker, nothing
is rebuilt, and no item comes out of the bag to make a layout fit.

What lost: cutting to four items, which would have bought a single page at the cost of two
items, and the three column rebuild, which is the right change only if the item roster grows
enough to need it. Neither is closed off. Both stay available if the second page turns out to
cost more in play than it does on paper.

### The order stays weakest to strongest

Stim, stim, bandage, bandage on page one; med kit and hope on page two.

The obvious objection is that this buries the two emergency items behind a page turn, and that
the menu makes it worse by resetting: `UIController` sets `selectedItem = 0` and calls
`GetInventoryPage(0, ...)` every time the ITEM menu opens, so the player never resumes where
they left off and pays the page turn on every use.

The objection does not survive contact with the turn structure. **Nothing is timed while the
menu is open.** The wave timer belongs to DEFENDING, and selection has no clock at all, so a
player choosing an item has as long as they want. There is no panic to design around, only two
extra keypresses in a state where keypresses cost nothing.

Which leaves the reading order as the only thing the sequence has to get right, and weakest to
strongest is the order the items were designed in and the order they teach themselves in. Page
one is what you spend, page two is what you save. The paging is doing the sorting for free.

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

## The inventory is part of the checkpoint

Dying restores the bag to what it held at the checkpoint. If the checkpoint is the start of the
battle the player gets everything back, and if it is somewhere later they get back exactly what
they were carrying when they reached it.

Those are the same rule rather than two, which is the useful part. The checkpoint restores
state, not position: health, inventory, turn, and anything else the fight was tracking. "Refill
at the start of a battle" is that rule applied to a checkpoint that happens to sit at turn
zero. Nothing special-cases the tutorial.

It also means an item spent on the turn the player died is refunded, since the checkpoint
predates it. Combined with a running clock, death against
[Illia](../bosses/illia.md) costs exactly one thing and it is time. Not progress, not
resources, not the turn's item. That is a clean, single-currency failure and it is worth
keeping single.

See [progression](progression.md) for where each boss's checkpoint sits.

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

- **Which perks touch the inventory, and how far?** The counts hold for every boss unless a perk
  changes them, which makes the perk system the only thing that can move a number the fights
  are otherwise balanced against. See
  [the Challenger](../general/the-challenger.md).
- **Are the item names final?** Stim, bandage and med kit were placeholders and hope was
  chosen against them. If any of the first three change, the fourth should be re-checked
  against whatever replaces them, since its job is to sit outside their pattern.

The engine used to call the default armour "Bandage", which collided with the healing item.
The equipment was renamed rather than the item: the Challenger now starts with fists and a worn
coat. See [the Challenger](../general/the-challenger.md).
