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
- **Irritation is binary, and it takes a perfect streak.** It triggers only if the player uses
  FIGHT on every single turn after she teaches it. The turn she asks for does not count, and
  one turn spent on anything else clears it. There are two ultimates, not a curve.
- **Dying does not end the run.** Illia brings the player back to life at the turn before the
  one they died on, without limit. Her checkpoint is one turn, which is the most generous
  setting of a rule every boss has. See [progression](../gameplay/progression.md).
- **Rewound deaths still count** in her record on the boss select.
- **The player carries basic healing only.** Stim, bandage and med kit, healing least to most
  in that order. They exist so the player learns what ITEM does, not so they can out-heal a
  wave. The names are placeholders.

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
  was no longer enough. Not rejected so much as moved: phase 3 keeps one idea per wave, and the
  overlapping happens in the ultimate instead, where it is the climax rather than a difficulty
  spike three waves from the end.
- **Alternating forms inside a single phase 3 wave.** It would have made phase 3 a recognition
  test, where the player has to identify which version is coming before answering it. Rejected
  in favour of one form per wave, which keeps every wave in the fight a single clean idea. That
  is the right property for the fight that teaches the game, and it costs phase 3 its sharpest
  possible version.
- **FIGHT changing the ending's text.** A proposal for keeping FIGHT meaningful once damage
  stopped deciding the fight: attacking her would have swapped in a different block of end
  dialogue. Superseded by the block and irritation, which is better, because it makes the
  choice cost something the player feels rather than something they read about afterwards.

## The three attacks are three reading skills

This is why there are exactly three and why they do not blur into each other. Each asks the
player to read the arena a different way, and each one has a different relationship to time:

| Attack | Shape | What the player reads | Moves? |
| ------ | ----- | --------------------- | ------ |
| Brush | A region swept | Which part of the arena is about to be covered. She points at it by swiping at it. | The sweep does |
| Bucket | Paint in bulk | Where the gap is, in a mass that is rising or a shower that is coming down | Yes, constantly |
| Splodge | A marked area, fixed | How much safe floor is left, and where it is | No |

Region denial, threading a moving field, and standing somewhere that is not marked. A player
who can do all three can handle any arrangement of them, which is what phase 3 asks for.

The bucket and the splodge are the pair most at risk of collapsing into each other, since both
are paint arriving in quantity, and the thing that keeps them apart is motion. A bucket is
individual projectiles the player threads between while they travel. A splodge is a fixed
region that is simply dangerous, and adding marks does not add things to dodge, it removes
floor to stand on. If a splodge ever starts moving, or a bucket ever resolves into a static
zone, they have become the same attack.

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
| Brush | A single swipe covering one side of the arena, left or right | Strikes down in sections across the arena, one after another, in the manner of Asgore's trident | Alternates the two |
| Bucket | Fills the arena from the bottom, the player climbs above the rising paint | Thrown in, arriving as a shower of small projectiles | Alternates the two |
| Splodge | One marked area | Two marked areas | Three, and more, at a random count |

The brush points at itself. She swipes right from the player's view and the right side of the
arena is what gets covered, so the gesture and the danger are the same direction. That is the
simplest possible telegraph and it is why the brush is the right attack to open on: the answer
to phase 1's brush is "be on the other side", which is one decision with two options.

Every form escalates along its own attack's axis rather than borrowing another's. The sectioned
brush is still a direction read, just several of them in sequence. Two marks is still a radius
read, just twice. Nothing has drifted into being a different attack, which is what keeps the
vocabulary at three.

## Splodge is a dial, and the other two are switches

Worth naming, because it changes what phase 3 is doing.

Brush and bucket each have two genuinely different forms. A swipe and a sectioned strike are
not the same attack at different volumes, and neither are a rising fill and a thrown bucket.
Phase 3 can alternate them because there is something to alternate.

Splodge does not work that way. One area, two areas, three and more is a single form with a
number attached. There is nothing to alternate, so its phase 3 is a straight escalation, and in
phase 3 the count is random rather than fixed.

That is a feature rather than a gap. It gives the three attacks three different escalation
shapes: two that transform and one that simply intensifies. It also means the recognition test
in phase 3 is carried by brush and bucket, while splodge is the attack that applies pressure
underneath it. Splodge is exempt from the opening-gesture constraint below, because there is no
wrong answer to guess at: more marked floor is more marked floor.

The random count needs a floor and a ceiling. Splodge is the one attack whose difficulty is a
single number, so an unbounded roll is the one place in the fight where a run can be
meaningfully harder than another run for no reason the player caused. Since the boss select
keeps a best time per boss, that variance shows up directly in a record people will compare.
Three to five is a range that stays unpredictable without any roll being unfair. Bounding it is
the point, not the specific numbers.

## The ultimate is where everything overlaps

Phase 3 keeps its forms in separate waves. The ultimate does not: it throws all of them into a
single wave, back to back and on top of each other.

That is what makes it the climax rather than a longer phase 3, and it is the one place in the
fight where the player has to read two things at once. It also means the ultimate is the only
wave with a genuinely new demand, while still introducing no new attack, which is the property
the exam needed.

It puts a constraint on the animation that the rest of the fight does not:

> When two of her attacks are being painted at the same time, both telegraphs have to stay
> readable.

Two brushstrokes in flight cannot occupy the same visual language, or the player sees one
smear and guesses. That is a requirement on how she is drawn rather than a nice-to-have, and it
belongs in the brief before anyone animates her. See [graphics](../graphics/graphics.md).

## Wave count

Phase 3 alternates between waves rather than inside them. One wave per form, six waves, each
one a single known thing at higher pressure.

| Phase | Waves | Roughly |
| ----- | ----- | ------- |
| 1 | 3, one per attack | 40 seconds |
| 2 | 3, one per attack | 40 seconds |
| 3 | 6, one per form | 80 seconds |
| Ultimate | 1 | 30 to 60 seconds |
| **Total** | **13** | **about three and a half minutes** |

That sits in the upper half of the two to four minute budget with the ultimate at its longer
end, and it leaves room to cut a phase 3 wave if the fight tests long.

The tradeoff is worth naming. Between-waves alternation means phase 3 never asks the player to
identify which form is coming mid-wave, so it is a pressure test rather than a recognition
test. What it gains is that every wave in the fight is one clean idea, which is the right
property for the fight that teaches the game.

## What FIGHT is for

She asks for it. Somewhere in phase 1 she tells the player to attack her, they do, and she
blocks it. That is the lesson: this is the button, this is what pressing it looks like, and
this is what happens when you press it on me.

The player can keep attacking after that. She keeps blocking, she never takes damage, and what
accumulates instead is her irritation, which makes the final ultimate harder. FIGHT is
therefore a real verb with a real consequence, which is exactly what a tutorial needs, and the
consequence lands at the end rather than immediately.

**The FIGHT she asks for does not count.** She instructed it, and a tutorial that punishes the
player for following its own instruction is worse than one that teaches nothing. The count
starts on the next turn, the first attack the player chose for themselves.

### Irritation is a streak, not a tally

It is binary. There are two ultimates, a normal one and a harder one, and no curve between
them. What selects the harder one is not how many times the player attacked but whether they
attacked **every turn** after the lesson, without a single exception.

That is a generous rule and a pointed one. Attacking out of curiosity costs nothing, because
one turn spent on ACT or ITEM or MERCY clears it. The harder ultimate is reserved for a player
who decided that attacking her was the answer and never revisited it. She is not punishing
violence, she is answering commitment.

It is also one flag rather than a counter, and the flag only ever moves one way: it starts set
after the lesson and is cleared the first time a turn goes elsewhere. That has a consequence
worth being deliberate about. A player who breaks the streak on turn two and then attacks for
the rest of the fight gets the normal ultimate, and she has no mechanical reason to react to
those attacks at all. Whether she still comments on them is a [writing](../writing/writing.md)
question, but she should, or the back half of the fight goes quiet on a player who is still
swinging.

### It has to be visible

If the only place her state shows is the difficulty of a wave three minutes later, the player
experiences an unexplained spike rather than a consequence they caused. She needs a tell, in
her dialogue, her expression or her painting, on each turn the streak is still alive. The tell
is also what tells the player they can stop. See [graphics](../graphics/graphics.md) and
[writing](../writing/writing.md).

### It survives death

The streak is not reset by dying. Since she rewinds the player to the turn before, that turn
gets replayed, and the replay is what counts: if the player attacked on the first attempt and
used an item on the second, the streak is broken. The state follows the timeline she rewound
to, not the one she erased.

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

She brings the player back at the turn before the one they died on, as many times as it takes.
It fits her, since she is running a test rather than a fight, and it makes the tutorial
effectively impossible to fail out of.

She is not an exception to a rule. Death sends the player to their last checkpoint, and each
boss sets how far back that is. Illia sets it one turn, which is the shortest possible walk
back and the reason her fight can afford to be forgiving while the ones behind her are not.

Two consequences worth being deliberate about. The ultimate becomes retryable in place, which
is what lets it be genuinely demanding rather than demanding-with-an-asterisk. And the fight
stops being balanced around healing: with an unlimited rewind and only basic items, the
difficulty valve is brush speed and the irritation flag, not how many bandages the player
brought.

Deaths still count in her record even though they cost nothing. That is the consistent choice,
and it does mean her death count is not comparable with any other boss's: a careless player
can rack up a dozen against Illia and none anywhere else, having played worse everywhere else.
Anything that ever compares death counts across bosses needs to know that.

## Open questions

- **Does she keep reacting to FIGHT after the streak is broken?** Mechanically nothing is
  happening any more, but a player can still be attacking every turn, and silence would read as
  the fight having stopped noticing them.
- **Is her fight timed across a rewind?** Records include a best time per boss. If the clock
  keeps running through a death and a revive, an unlimited rewind means her best time is still
  a real number. If it does not, her times are not comparable with anyone's, including her own.
- **What are the three actually called?** Stim, bandage and med kit are placeholders and the
  real names are a [writing](../writing/writing.md) job. Worth doing early, since the tutorial
  is where the player learns the game's vocabulary and placeholder names get into screenshots.
- **Does the ladder differ by more than amount?** Three items that differ only in how much they
  heal teach one lesson: bigger is better, always use the biggest. Giving them a second axis,
  a cheap one that heals instantly against a large one that costs the rest of the turn, is what
  turns ITEM from a button into a choice. Not required for a tutorial, but it is the cheapest
  place to add depth.
- **What is the range on the random splodge count?** Random is settled, the bounds are not, and
  splodge is the one attack whose whole difficulty is a single number.
- **What is in the ultimate, in what order?** Everything, in one wave, is the shape. Which
  forms, how many passes, and how long it runs is the last piece of the fight that is still
  entirely open, and it is the piece the whole thing ends on.
- **What order do the six phase 3 waves come in?** Six waves of one known thing each is a
  sequence, and the sequence is the difficulty curve. Alternating attack by attack reads
  differently from grouping both forms of each attack together.
