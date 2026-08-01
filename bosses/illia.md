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
- **Irritation is binary, and it takes a majority.** It triggers when the player uses FIGHT on
  more than half the turns after she teaches it, which is the same moment she runs out of
  written responses to being attacked. There are two ultimates, not a curve. The count is
  invisible: her dialogue is the only signal it exists.
- **Dying does not end the run.** Illia brings the player back to life at the turn before the
  one they died on, without limit. Her checkpoint is one turn, which is the most generous
  setting of a rule every boss has. See [progression](../gameplay/progression.md).
- **Rewound deaths still count** in her record on the boss select, presented the same way as
  every other boss's.
- **The clock keeps running through a death and a revive.** The rewind costs time, not
  progress.
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
| Splodge | One marked area | Two marked areas | Three or four, chosen at random |

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

Splodge does not work that way. One area, two areas, three or four is a single form with a
number attached. There is nothing to alternate, so its phase 3 is a straight escalation, and
from phase 3 onward the count is rolled rather than fixed.

That is a feature rather than a gap. It gives the three attacks three different escalation
shapes: two that transform and one that simply intensifies. It also means the recognition test
in phase 3 is carried by brush and bucket, while splodge is the attack that applies pressure
underneath it. Splodge is exempt from the opening-gesture constraint below, because there is no
wrong answer to guess at: more marked floor is more marked floor.

The roll is **three or four**, in phase 3 and in the ultimate alike. A two-value range is about
as tight as random can be while still being random, which is the right amount here: splodge is
the one attack whose entire difficulty is a single number, and the boss select keeps a best
time per boss, so any variance lands directly in a record people compare. Three against four
changes how much floor is left without any roll being one the player can blame a loss on.

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

### Irritation is a majority, and her dialogue sets the number

It is binary. There are two ultimates, a normal one and a harder one, with no curve between
them. What selects the harder one is the player using FIGHT on **more than half** the turns.
The attacks do not have to be consecutive, and the turn she asks for does not count toward
either side of the fraction.

The threshold is not a tuning number picked in isolation. She has a set of written responses to
being attacked, one for each attack, and the harder ultimate is what happens when she reaches
the end of them. Running out of things to say **is** the irritation. So the size of the
dialogue pool is the balance number, which means writing decides it rather than tuning.

That couples two things that are usually independent, and it is worth stating plainly: **the
number of FIGHT responses she has is a gameplay number.** Adding a line moves the threshold.
Cutting one moves it the other way. They cannot be edited separately.

Against the current 13 wave structure, that is thirteen turns, one of which is the lesson, so
more than half of the remaining twelve is seven. **She needs seven distinct responses to
FIGHT.** If the wave count changes, that number changes with it.

### The count is invisible, so the dialogue is the whole tell

There is no meter, no counter and no icon. Nothing on screen says how close the player is, and
that is deliberate.

Which puts the entire mechanic on seven lines of dialogue. A rule that only shows up as a
harder wave three minutes later would read as an unexplained spike rather than as a consequence
the player caused, and her lines are the only thing standing between this rule and being
exactly that.

So they cannot be a bag of interchangeable barks. They have to be an ordered run-down: shorter,
or sharper, or more tired, in a direction a player can feel without being told there is a
direction. Her seventh line is the warning, and it has to land as one while there is still time
to stop. That is a harder writing job than seven reactions to being hit, and it is load-bearing
in a way dialogue usually is not. See [writing](../writing/writing.md), and
[graphics](../graphics/graphics.md) if her expression carries part of it.

### It survives death

Dying does not reset the count. Since she rewinds the player to the turn before, that turn gets
replayed, and the timeline that stands is the one that counts: an attack made on an attempt she
erased is not counted twice, and if the player attacked on the first attempt and used an item
on the replay, the replay is what the count sees. The same applies to the denominator, since a
rewound turn is one turn rather than two.

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

### The rewind costs time, not progress

The clock does not stop for a death. It runs through dying, through her reviving the player,
and into the replayed turn, so a death is free in progress and expensive in the only currency
the records keep.

That is what stops the tutorial being a fight with no skill ceiling. It cannot be lost, so
clearing it says nothing, but clearing it quickly says everything, and the gap between a player
who dodged the ultimate and one who was revived through it four times is visible on the boss
select without either of them having failed. An unloseable fight with a real best time is a
better first boss than a loseable one, because it puts the pressure on the player who wants it
and takes it off the player who does not.

It also means her best time is a real number rather than a special case, comparable with her
own earlier runs and sitting in the same column as everyone else's on the same terms.

Deaths still count in her record even though they cost nothing, and the boss select shows them
exactly the way it shows everybody else's. There is no asterisk and no separate presentation.

The argument for marking them out was that a cheap death is not the same event as an expensive
one, so her column would run high and mislead. The argument against is better: dying to the
boss who revives you is worse than dying to the boss who sends you back to the start. One of
those fights hands you the turn back and asks you to try the same twenty seconds again. Failing
that is a plainer statement about the run than failing a fight that costs three minutes to
re-enter. Her number running high is the number being right.

## Open questions

- **What does she say on the attack after the last one?** The pool is seven deep and the fight
  has more turns than that, so a committed player will attack again with nothing left in the
  bank. A repeated final line, a silence that is deliberately a silence, or something that only
  exists past the threshold. Whichever it is, it is the first thing the player hears after the
  fight has already been decided.
- **Does the clock run through her revive dialogue too?** It runs through the death, which is
  settled. Whether it runs while she is saying something about it is a smaller question with a
  real answer, because on a first run that dialogue cannot be skipped.
- **What are the three actually called?** Stim, bandage and med kit are placeholders and the
  real names are a [writing](../writing/writing.md) job. Worth doing early, since the tutorial
  is where the player learns the game's vocabulary and placeholder names get into screenshots.
- **Does the ladder differ by more than amount?** Three items that differ only in how much they
  heal teach one lesson: bigger is better, always use the biggest. Giving them a second axis,
  a cheap one that heals instantly against a large one that costs the rest of the turn, is what
  turns ITEM from a button into a choice. Not required for a tutorial, but it is the cheapest
  place to add depth.
- **What is in the ultimate, in what order?** Everything, in one wave, is the shape. Which
  forms, how many passes, and how long it runs is the last piece of the fight that is still
  entirely open, and it is the piece the whole thing ends on.
- **What order do the six phase 3 waves come in?** Six waves of one known thing each is a
  sequence, and the sequence is the difficulty curve. Alternating attack by attack reads
  differently from grouping both forms of each attack together.
