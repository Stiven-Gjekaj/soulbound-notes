# The Challenger

Who the player is. Not a character from anybody's story, but an original one who arrives from
outside it.

Related: [general](general.md), [bosses](../bosses/bosses.md) for who they fight,
[health and healing](../gameplay/health-and-healing.md) for what they bring,
[writing](../writing/writing.md) for how they are addressed.

## Settled

- **The player is the Challenger**, an original character rather than anyone from the source
  material.
- **The player names them.** The name entry screen the game already has is where that happens.
- **They exist outside the universe** the bosses belong to, and travel through time and space
  to reach them.
- **They fight powerful characters to grow stronger**, working toward being able to beat the
  villain at the end of it.
- **They are never seen.** No portrait, no sprite, no body. The player is a SOUL.
- **They never speak.** Silent throughout.
- **The bosses are from Soultale**, the original story this game is based on.
- **The bosses do not know what the Challenger is.** They meet a stranger, not a traveller.

## What it solves

Playing as a canon character means every fight has to fit that character's story: when it
happened, whether they would have been there, what it costs them, and what it means that they
lost or won. A boss rush cannot pay that bill. It has no room for it and it does not want it.

An outsider owes nothing to the timeline. The Challenger can meet a character at any point in
that character's life without contradicting it, can lose without it meaning anything canonical,
and can fight somebody who would never have met them. The continuity problem does not get
solved so much as it stops being a problem, and it stops being one for every character added
from here on.

The timeline in question is Soultale's, which is this project's own story rather than somebody
else's. That does not make the problem smaller, it makes it worse: a canon you wrote is one you
are still writing, and a game that fixes a character's fate is a game that has quietly decided
something the story had not. The Challenger keeps the two separate. Nothing that happens in a
fight is something that happened in Soultale.

## Nobody home

Not seen, and does not speak. No portrait, no sprite, no lines. The player is a SOUL in a box
and that is the entire visible character.

This is the strongest version of the idea rather than a shortcut past drawing one. A named,
silent, invisible protagonist is a space the player occupies rather than a person they watch.
The name they typed is theirs and nothing overwrites it with somebody else's face or somebody
else's opinion.

It is also why the bosses carry every scene. There is no reaction shot and no reply, so
whatever a fight means has to be in what the boss says and what the boss does. That is a real
constraint on [writing](../writing/writing.md), and it is the same constraint Undertale-style
battles already work under.

**The bosses do not know what the Challenger is.** They meet a stranger who turned up to fight
them. No opponent gets to explain the premise, because no opponent has it. The player is the
only one holding the whole picture, and the fiction never has to be delivered as exposition by
somebody who should not know it.

## It fits what was already built

The premise arrived after most of the mechanics, so it is worth noting how little of it has to
be argued for. Nearly everything decided so far reads as though it was designed for this.

- **The player names their character.** That was a v0.5 feature and a UI decision. It is now
  the premise: the Challenger is yours, so you name them.
- **The boss select lets you pick anybody in any order.** Someone travelling through time and
  space does not have a correct order to do it in.
- **Each fight sets the player's max HP.** See below, this is the one that needed the premise
  most.
- **Illia tests rather than kills, and revives the player.** An outsider who turned up to be
  measured against her is exactly who she would be gentle with.
- **Bosses can come from anywhere.** Nothing in the fiction limits the roster, which is the
  whole point of the live-service plan.

## Growth, and the one thing that had to be reconciled

The fiction says the Challenger grows stronger. The mechanics say each boss sets the player's
max HP for its own fight and nothing carries between fights. Read plainly, those contradict:
if nothing carries, the Challenger never actually grows.

Time travel resolves it, and does so better than a compromise would. **The Challenger who
faces a given opponent is the version of themselves who was ready for that opponent.** Their
fights are not a sequence in one life. Each is a separate crossing, and each crossing lands
them at the strength that meeting requires.

So a player who opens with a late boss is not fighting it underpowered, and one who saves an
early boss for last is not trivialising it. Both meet the version of the Challenger that fight
is for. The per-fight max HP stops being a records-keeping concession and becomes the plainest
possible statement of the premise, and free boss selection stops needing an excuse.

Worth stating positively: the Challenger's stat line is the fight describing itself, not a
score of how far they have come. The growth happens somewhere else.

## Growth is unlocks, not numbers

**The Challenger gets stronger through item and perk unlocks.** Not through a rising stat line.

That is a better fit than a level would have been, and it resolves the tension above properly
rather than explaining it away. Max HP belongs to the fight, so the fight stays the same
difficulty every time it is played. The kit belongs to the player, so it carries. Progression
is real, persistent and visible, and none of it touches the numbers that make records
comparable.

Perks also become the place every future "what if the player could" goes. The healing item
counts, for instance, are fixed for every boss **unless a perk changes them**, which is what
lets the inventory be a designed constant and still be something the player can affect.

Two perks deep this needs its own note. At two facts it does not, so it lives here until there
is a third.

### It does bring back a problem per-fight max HP was avoiding

If perks are persistent and can be brought into any fight, then a boss fought with a full perk
loadout and the same boss fought bare are different fights. That is exactly the order
dependence that setting max HP per fight was chosen to avoid, arriving through a different
door.

It lands on records. A best time against a boss now depends on which perks the player had when
they set it, so the number is not comparable with their own earlier run, let alone anyone
else's. Three ways out, none of them chosen:

- **Accept it.** Most games with builds do. The record measures the player's best, whatever
  they brought.
- **Record the loadout with the time**, so a run is comparable with the runs it should be
  compared with.
- **Keep perks out of the timed record**, which makes the record clean and makes the perks feel
  like they do not count.

## What they carry

Nothing that came from anywhere. The Challenger arrives with themselves and what they were
wearing, which is why the starting gear is worth nothing and why getting stronger has to be
earned in the fights rather than brought to them.

- **Weapon: fists.** They brought no weapon, because they are not from anywhere that would have
  given them one. It is also the plainest statement the game can make about the premise: the
  Challenger fights to grow stronger, and starts with only themselves to fight with.
- **Armour: worn coat.** Travel-worn clothing rather than protection. Whatever they had on when
  they crossed.

Both replace names inherited from upstream, `"Stick"` and `"Bandage"`, which were placeholders
from a different game and one of which collided with the healing item of the same name. The
collision is what prompted the rename. The premise is what decided it.

Two alternates were weighed and are worth keeping on the shelf: **resolve** and **drifter's
coat**, which say the same things less literally. Fists and worn coat won on being immediately
legible on a stats line at 640x480.

### These were not cosmetic

The names feed real numbers. `FightUIController.cs` computes damage dealt from `WeaponATK`,
and `PlayerController.cs` reduces damage taken by `floor((DEF + ArmorDEF) / 5)`, so five points
of armour is one point of damage prevented. Both values come from looking the equipment name up
in the item pools.

They are also the engine's fallback state: whenever a mod removes the currently equipped item
from the library, `Inventory.cs` reverts the player to those two names. So the defaults and the
fallbacks had to move together, and the equipment pools had to learn the new names, or the
lookup would have resolved to zero by failing rather than by design.

Both now sit in the weapon and armor pools at 0, which is what the old defaults should always
have been: neither Stick nor Bandage was in either pool, so the engine looking up its own
starting gear used to warn that it did not exist. Stick and Bandage stay in the library as
ordinary items, which is what leaves Bandage free to be a healing item.

This is done, on the game repository, as `v0.6.3`.

## Being addressed by a title

Having a title as well as a name is quietly useful for [writing](../writing/writing.md). A boss
can call the player "Challenger" and never need their name, which matters because the engine
caps names at nine characters, in `PlayerCharacter.cs`, and because dialogue built around
interpolating a player-chosen name reads badly however careful it is.

The name is for the player. The title is for everybody else in the game.

## The live-service plan

The original intent is for the roster to keep growing, with each batch of characters bringing a
new major threat, so that the Challenger always has a bigger reason to keep fighting.

The premise is what makes that possible. A roster of canon characters runs out at the edge of
one story. A Challenger from outside has no such edge, so adding a character never needs a
justification beyond somebody wanting to fight them. That is the strongest single argument for
the whole idea and it should be the thing that survives if anything else about it changes.

Three consequences, all of which touch decisions already made.

**One villain, and one big fight to close each batch.** Not a new antagonist per batch. The
villain at the end stays the villain at the end, and every batch finishes on a boss large
enough to feel like an ending without being the ending.

That is the structure that keeps a live-service game from spending its own premise. A new
villain each season means the last one stopped mattering, and after two of those the player
learns that whoever is at the end this time is temporary. Here the destination never moves. The
capstone fights are stages of getting there, so each batch can land hard without cashing in the
thing the whole game is pointed at.

It does put weight on the capstone fights. Each one has to be a real event rather than the
seventh boss of seven, and each one has to leave the villain further away than the player
hoped, or the pattern becomes a countdown with a known length.

**Completion counting stops being a fixed number.** The tutorial boss counts toward completion,
which was decided when the roster was a known size. A growing roster turns "four of seven" into
a figure that changes under the player, and a completed game into one that becomes incomplete
when a batch lands. See [boss select](../ui/boss-select.md), which is where a player would
notice.

**v1.0 stops meaning finished.** The game repository's milestones run to v1.0 as though it were
the end of the work. Under a live-service plan it is the start of the part that lasts longest.
Those two readings of the same number should be made to agree.

## Open questions

- **How do perks interact with the records?** See above. Three options, none picked, and it
  gets harder to change once times are being recorded.
- **Where do perks come from?** Clearing bosses, clearing them a particular way, no-hit runs,
  best times, or something else entirely. Whatever it is becomes what the game is actually
  asking the player to do.
- **Can a perk be brought into the tutorial?** Illia is the first fight and the fight the
  numbers are taught in. A player replaying her with a loadout is playing a different tutorial
  from the one that was designed.
- **Does the player ever learn the premise?** Nobody in the game knows it and the Challenger
  does not speak, so there is currently no one who can say any of it out loud. Either it lives
  entirely outside the fiction, in a title screen or a store page, or something in the game has
  to carry it without a character to carry it.
- **How does a Soultale reader meet this?** Somebody who knows the story arrives already
  attached to these characters and expecting things of them. Somebody who does not arrives with
  a boss rush. The first fight is the same for both and it cannot be written for both by
  accident.
