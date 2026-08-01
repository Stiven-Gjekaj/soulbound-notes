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

## What it solves

Playing as a canon character means every fight has to fit that character's story: when it
happened, whether they would have been there, what it costs them, and what it means that they
lost or won. A boss rush cannot pay that bill. It has no room for it and it does not want it.

An outsider owes nothing to anybody's timeline. The Challenger can meet a character at any
point in that character's life without contradicting it, can lose without it meaning anything
canonical, and can fight somebody who would never have met them. The continuity problem does
not get solved so much as it stops being a problem, and it stops being one for every character
added from here on.

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

Worth stating positively: growth in this game is the player getting better. The numbers are the
fight describing itself, not a score of how far the Challenger has come.

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

**"The villain at the end" and "a new threat per batch" are different structures.** One is a
story with an ending. The other is a series of eras, each with its own antagonist, where the
ending keeps moving. Seasonal games mostly do the second and describe it as the first. Both
work, they need different writing, and it is much cheaper to know which one this is before the
first threat is written than after.

**Completion counting stops being a fixed number.** The tutorial boss counts toward completion,
which was decided when the roster was a known size. A growing roster turns "four of seven" into
a figure that changes under the player, and a completed game into one that becomes incomplete
when a batch lands. See [boss select](../ui/boss-select.md), which is where a player would
notice.

**v1.0 stops meaning finished.** The game repository's milestones run to v1.0 as though it were
the end of the work. Under a live-service plan it is the start of the part that lasts longest.
Those two readings of the same number should be made to agree.

## Open questions

- **One villain, or one per batch?** See above. It is the difference between a story and a
  season.
- **Does the Challenger get stronger between batches?** Per-fight max HP means growth is not
  carried, which the time travel explains neatly for a fixed roster. A live-service ladder of
  escalating threats is a stronger pull toward real progression, and the two would then have to
  be reconciled again.
- **Is the Challenger ever seen?** The player is a SOUL in the arena. Whether there is a body
  attached, in dialogue portraits, on the select screen, or at all, has not been decided, and
  it is the difference between an original character and an implied one. A
  [graphics](../graphics/graphics.md) question as much as a writing one.
- **Does the Challenger speak?** A silent protagonist keeps them yours. One with lines makes
  them somebody. Both work and they are not the same game.
- **Where do the bosses come from?** "Time and space" is broad enough to mean one universe's
  history or all of them. The answer sets what the roster can ever contain.
- **What do the bosses know?** Whether an opponent understands what the Challenger is, or
  simply finds a stranger in front of them, changes every first line in the game.
