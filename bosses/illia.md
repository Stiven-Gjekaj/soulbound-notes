# Illia

The first boss, and the one the Discord voted for. She paints, and the arena is her canvas. She
carries the tutorial for the whole game, because a boss rush has nowhere else to put one.

Related: [bosses](bosses.md), [gameplay](../gameplay/gameplay.md) for the rules she teaches,
[progression](../gameplay/progression.md) for the lock she sits behind,
[graphics](../graphics/graphics.md) for how she looks.

Because she is the tutorial, every other boss is locked until she is cleared, and she is
relabelled the tutorial boss on the select screen afterwards. Her dialogue is unskippable on the
first run and skippable on every run after. Those are game-wide rules and they live in
[progression](../gameplay/progression.md).

## Settled

- **Three phases**, each one carrying tutorial weight.
- **Three attacks: brush, bucket, splodge.** Every phase uses all three, in a different form
  each time.
- **Phase 1** introduces movement and the FIGHT, ACT, ITEM and MERCY menu, with the simplest
  form of each attack.
- **Phase 2** repeats the same three attacks in a different manner. Worked example: phase 1's
  bucket fills the arena from the bottom and the player climbs above the rising paint, phase
  2's bucket is thrown into the arena and the player dodges the droplets it throws off.
- **Phase 3** is a full mini boss fight, an exam on whether the player got the gist. Brush and
  bucket incorporate both of their earlier forms and alternate between them. Splodge escalates
  instead, to three marks and more.
- **She is in full colour.** Not desaturated.
- **She can change the arena, but nothing persists between waves.** A canvas that fills up is
  a canvas nobody can fight in.
- **The player cannot paint back.** It is not one of her attacks.
- **Two to four minutes of wave time**, dialogue not counted.
- **She ends the fight herself**, once the player survives her final ultimate attack. The
  ultimate is a long string of attacks run back to back. Her HP reaching zero is not the
  ending.
- **FIGHT is taught by her and never lands.** She prompts the player to use it and then blocks
  the attack, which is how the verb gets explained. The player may keep attacking. She keeps
  blocking, and she gets irritated, and the irritation makes the final ultimate harder.
- **Dying does not end the run.** Illia brings the player back to life at the turn before the
  one they died on. This is hers, not a game-wide rule, because she is testing rather than
  killing.
- **The player carries basic healing only.** A stem, a med kit, a bandage. They are there so
  the player learns what ITEM does, not so they can out-heal a wave.

## What lost

- **A desaturated Illia with saturated paint.** The idea was to make colour scarce so that
  every new colour read as an event, doubling as the tutorial beat for each new bullet type.
  Rejected: she is a painter, and a colourless painter is a worse character than a legible
  one. The readability problem it was solving is handled by the box instead, below.
- **Paint that persists across waves.** A cumulative canvas would have made the fight build on
  itself, and would have left a finished painting on screen at the end as the spare beat.
  Rejected: the arena clogs, and it becomes unplayable well before it becomes pretty.
- **An ACT that lets the player paint back.** It would have made the fight a conversation in
  paint rather than a test. Rejected: it is not one of her attacks, and it was the most
  expensive item on the list by a distance.
- **Overlapping telegraphs in phase 3.** Two paintings in progress at once, so that reading one
  was no longer enough. Rejected in favour of alternating the two forms of each attack, which
  tests recognition instead of parallel attention, is cheaper to author, and is far less likely
  to produce a wave that is unfair by accident.
- **FIGHT changing the ending's text.** A proposal for keeping FIGHT meaningful once damage
  stopped deciding the fight: attacking her would have swapped in a different block of end
  dialogue. Superseded by the block and irritation, which is better, because it makes the
  choice cost something the player feels rather than something they read about afterwards.

## The three attacks are three reading skills

This is why there are exactly three and why they do not blur into each other. Each one asks the
player to read the arena a different way:

| Attack | Shape | What the player reads |
| ------ | ----- | --------------------- |
| Brush | A line, drawn | Direction. Where the stroke is heading. |
| Bucket | Volume, poured | Area. Which part of the box is not paint. |
| Splodge | Impact, from a point | Radius. How far from the point is far enough. |

Direction, area, radius. A player who can read all three can read any combination of them,
which is what phase 3 asks for.

## The brush is the telegraph

She paints the attack before it fires, and the act of painting is the warning. This costs
nothing in characterisation, because a painter who is not moving a brush is not painting.

It also gives the fight one difficulty knob: **brush speed**. How fast she draws is how much
warning the player gets. It tightens across the three phases without a single wave script
changing, and it is the first thing to reach for if the fight tests too easy or too hard.

## Colour discipline lives in the box, not on her

Undertale-style layout already separates her from her bullets: she sits above the arena, the
bullets are inside it. Her being in full colour costs the player nothing, because her colours
are never competing for attention with the thing that can kill them.

What does have to stay disciplined is the inside of the box. The working rule:

> Anything with colour inside the arena is dangerous.

Which means no decorative paint inside the box. If the floor of the arena is painted for mood
rather than for damage, it is a flat neutral tone, or it is not there. Every bullet type also
needs its own shape and not only its own colour, because the screen is 640x480 and because
colour alone shuts colourblind players out of the one system the entire fight is built on.

## The canvas resets, so alterations pay off inside their own wave

With no persistence, every arena change she makes has to matter in the wave that made it. The
phase 1 bucket already works this way: the paint rises during the wave, the player climbs, the
wave ends, the paint drains. Nothing carries over and nothing accumulates.

That is a constraint worth stating positively. It means every wave can be tested on its own,
in any order, without a setup wave before it.

## The time budget

Two to four minutes of wave time, against three phases of three attacks.

At a comfortable 12 to 15 seconds per wave, that range is 9 to 18 waves. Three phases times
three attacks is exactly 9. So:

- **Two minutes is the minimum viable fight**: the 3x3 grid, nothing repeated, no wave doing
  double duty.
- **Four minutes is roughly double that**, and phases 1 and 2 should not absorb it. They are
  three waves each and they are teaching, so they end when the lesson lands.
- **Phase 3 is the variable.** It is the only phase that grows.

Four minutes does not mean longer waves. A 24 second wave is exhausting rather than hard. It
means more waves, and they belong in phase 3.

## The attack grid

| Attack | Phase 1 | Phase 2 | Phase 3 |
| ------ | ------- | ------- | ------- |
| Brush | A single swipe across one part of the arena, left or right | Strikes down in sections across the arena, one after another, in the manner of Asgore's trident | Alternates the two |
| Bucket | Fills the arena from the bottom, the player climbs above the rising paint | Thrown into the arena, the player dodges the droplets it throws off | Alternates the two |
| Splodge | One mark | Two marks | Three marks, and more |

Every form escalates along its own attack's axis rather than borrowing another's. The sectioned
brush is still a direction read, just several of them in sequence. Two marks is still a radius
read, just twice. Nothing has drifted into being a different attack, which is what keeps the
vocabulary at three.

## Splodge is a dial, and the other two are switches

Worth naming, because it changes what phase 3 is doing.

Brush and bucket each have two genuinely different forms. A swipe and a sectioned strike are
not the same attack at different volumes, and neither are a rising fill and a thrown bucket.
Phase 3 can alternate them because there is something to alternate.

Splodge does not work that way. One mark, two marks, three marks and more is a single form with
a number attached. There is nothing to alternate, so its phase 3 is a straight escalation.

That is a feature rather than a gap. It gives the three attacks three different escalation
shapes: two that transform and one that simply intensifies. It also means the recognition test
in phase 3 is carried by brush and bucket, while splodge is the attack that applies pressure
underneath it. Splodge is exempt from the opening-gesture constraint below, because there is
no wrong answer to guess at: more marks is more marks.

One thing left hanging by "three marks, and more": whether the count climbs during phase 3, so
that the last splodge wave is denser than the first, or whether it sits at a fixed number
above three. The ultimate presumably has the most of all.

## Phase 3 is a recognition test, and that sets a hard art constraint

Alternating the two forms turns phase 3 into something the first two phases cannot be: the
player no longer knows which version is coming. Seeing the telegraph is no longer enough,
because the telegraph now has to be identified before it can be answered.

That is a better exam than running two attacks at once, and it comes with a constraint that
has to hold or the phase is unfair:

> The two forms of brush, and the two forms of bucket, must be tellable apart from the first
> moment of the brushstroke.

If the rising bucket and the thrown bucket look identical for their first second, phase 3 asks
the player to guess. Both pairs need a distinct opening gesture, and this is a requirement on
the animation rather than a nice-to-have, so it belongs in the brief before anyone draws her.
See [graphics](../graphics/graphics.md).

Splodge is outside this. It has one form and a count, so there is nothing to identify.

## Wave count, and what "alternates" decides

Whether the alternation happens inside a wave or between waves is the difference between two
quite different fights, and the wave maths settles it either way:

- **Between waves.** Phase 3 runs six waves, one per form. Total is 3 + 3 + 6 plus the
  ultimate, about 13 waves, landing near three and a half minutes. Gentler, and closer to a
  playlist than an exam.
- **Within a wave.** Phase 3 runs three waves, one per attack, each switching forms as it
  goes. Total is 3 + 3 + 3 plus the ultimate, about 10 waves, landing near two and a half
  minutes. This is the version that actually tests recognition, and it is the shorter fight.

Both sit inside the two to four minute budget. The within-a-wave version is the one that makes
phase 3 an exam rather than a recap.

## What FIGHT is for

She asks for it. Somewhere in phase 1 she tells the player to attack her, they do, and she
blocks it. That is the lesson: this is the button, this is what pressing it looks like, and
this is what happens when you press it on me.

The player can keep attacking after that. She keeps blocking, she never takes damage, and what
accumulates instead is her irritation, which makes the final ultimate harder. FIGHT is
therefore a real verb with a real consequence, which is exactly what a tutorial needs, and the
consequence lands at the end rather than immediately.

Two things have to hold or it turns on the player:

**The FIGHT she asks for cannot count.** She instructed it, and a tutorial that punishes the
player for following its own instruction is worse than one that teaches nothing. The counter
starts on the second attack, the first one the player chose for themselves.

**The irritation has to be visible.** If she gets angrier and the only place it shows is the
difficulty of a wave three minutes later, the player experiences an unexplained spike rather
than a consequence. Whatever the state is, it needs a tell in her dialogue, her expression or
her painting, and it needs one on every step rather than only at the end. See
[graphics](../graphics/graphics.md) and [writing](../writing/writing.md).

## The ultimate

The fight ends when the player survives it, so it is the only wave in the game so far whose
failure condition and success condition are the same event. Three things follow.

It earns its length in a way no other wave does. A long single wave is exhausting in the middle
of a fight and correct at the end of one, and this is the one place where thirty to sixty
seconds is right rather than indulgent.

It has to be survivable without knowing it in advance, because the first time anyone sees it is
the run where it decides the fight. Whatever it does, it is built from the three attacks the
player has spent two phases learning, and it introduces nothing new. The novelty is the length
and the density, not the vocabulary.

And the thing that would normally make it cruel is already solved. A long final wave is usually
the most expensive failure a fight can hand out, because dying at the end means replaying all
of it. Here she revives the player at the turn before, so the ultimate can be attempted again
immediately. It can be as demanding as it needs to be without the walk back being the real
punishment.

## Dying is a rewind

She brings the player back at the turn before the one they died on. It fits her, since she is
running a test rather than a fight, and it makes the tutorial nearly impossible to fail out of.

Two consequences worth being deliberate about. The ultimate becomes retryable in place, which
is what lets it be genuinely hard rather than hard-with-an-asterisk. And the fight stops being
balanced around healing: with a rewind on death and only basic items, the difficulty valve is
brush speed and the irritation state, not how many bandages the player brought.

The rewind is Illia's. Nothing yet says any other boss does this, and the assumption is that
none of them do, which makes her the one fight the player can be careless in. See
[progression](../gameplay/progression.md).

## Open questions

- **Is irritation binary or scaled?** Either she is annoyed or she is not, and the ultimate has
  two versions, or every extra attack turns the dial and the ultimate has many. Binary is one
  flag and one alternative wave. Scaled is a difficulty curve authored by the player without
  their knowing it, which is more interesting and much harder to balance.
- **Does irritation survive a death?** If she revives the player, is she still as annoyed as she
  was, and does dying reset the counter or add to it.
- **Is the rewind unlimited?** Nothing caps it at the moment, which makes the tutorial
  unloseable. That is defensible for a tutorial and it should be a choice rather than an
  oversight.
- **Do rewound deaths count as deaths?** The boss select records deaths per boss. If Illia
  revives the player twelve times, the select screen either says twelve deaths on a fight
  nobody can lose, or it says none and quietly means something different for her than for
  everyone else.
- **Are the item names final?** Stem, med kit and bandage are what they are called at the
  moment. Naming is a [writing](../writing/writing.md) job and these read as placeholders.
- **Do the three heal differently, or are they one item with three names?** Three items that
  all restore the same amount teach the player nothing about ITEM except which button it is
  under. Three that differ, a small instant one and a large slow one for instance, teach a
  choice.
- **Does phase 3 alternate inside a wave or between waves?** Inside is the recognition test and
  the shorter fight, between is the recap and the longer one. The section above has the maths.
- **Does the splodge count climb inside phase 3, or sit fixed above three?** "Three marks, and
  more" leaves it open. Climbing gives the phase its own curve, fixed makes it easier to tune
  against the ultimate.
- **What separates the thrown bucket from a splodge?** The phase 2 bucket is thrown and throws
  off droplets, which is impact spreading from a point, which is the splodge's own job. This is
  the one pair in the grid that could collapse into a single attack in practice, and it needs
  watching once both exist.
- **Does the phase 1 brush swipe always come from the same edge?** Left or right is settled.
  Whether it enters from the side it lands on, or is drawn across from the opposite one, is the
  difference between a direction read and a pure position read.
