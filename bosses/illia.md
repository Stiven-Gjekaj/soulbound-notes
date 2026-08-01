# Illia

The first boss, and the one the Discord voted for. She paints, and the arena is her canvas. She
carries the tutorial for the whole game, because a boss rush has nowhere else to put one.

Related: [bosses](bosses.md), [gameplay](../gameplay/gameplay.md) for the rules she teaches,
[graphics](../graphics/graphics.md) for how she looks.

## Settled

- **Three phases**, each one carrying tutorial weight.
- **Three attacks: brush, bucket, splodge.** Every phase uses all three, in a different form
  each time.
- **Phase 1** introduces movement and the FIGHT, ACT, ITEM and MERCY menu, with the simplest
  form of each attack.
- **Phase 2** repeats the same three attacks in a different manner. Worked example: phase 1's
  bucket fills the arena from the bottom and the player climbs above the rising paint, phase
  2's bucket is thrown into the arena and the player dodges the droplets it throws off.
- **Phase 3** is a full mini boss fight, an exam on whether the player got the gist.
- **She is in full colour.** Not desaturated.
- **She can change the arena, but nothing persists between waves.** A canvas that fills up is
  a canvas nobody can fight in.
- **The player cannot paint back.** It is not one of her attacks.
- **Two to four minutes of wave time**, dialogue not counted.
- **She ends the fight herself**, once the player survives her final ultimate attack. The
  ultimate is a long string of attacks run back to back. Her HP reaching zero is not the
  ending.

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

## Phase 3 gets one new thing, and it is not a fourth attack

Adding a fourth attack in the exam would undercut the point of an exam. The escalation should
come from the three the player already knows.

The proposal: **in phase 3 the telegraphs overlap.** Two paintings in progress at once, so
reading one is no longer enough and the player has to decide which brush matters first. It
costs no new art and no new attack, it is the exam the first two phases were revising for, and
it is the only moment where her adaptive improviser characterisation arrives at full strength.

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

And it is where the retry cost lands. Dying to the last twenty seconds of a three minute fight
is the most expensive failure the game can hand out, so what the retry costs is a real
decision, not a detail. See [progression](../gameplay/progression.md).

## Open questions

- **What is FIGHT for?** It is taught in phase 1, so it works, but damage no longer ends the
  fight. A tutorial that teaches a button and then reveals the button never mattered has
  taught the player something false. The cheapest honest fix is that FIGHT does not shorten
  the fight but does change how it ends, which keeps the verb real and costs one flag and one
  alternative block of end text. That is a proposal, not a decision.
- **What does dying in the ultimate cost?** Retrying from the start of the fight is the boss
  rush default and it is a three minute walk back. Worth deciding deliberately rather than
  inheriting.
- **How much healing does the player carry?** ITEM is taught in phase 1, so items exist. How
  many the player brings into the ultimate is the difficulty valve for the whole fight, and it
  is currently unset.
- **What separates the bucket from the splodge in practice?** Phase 2's thrown bucket throws
  off droplets, and phase 2's splodge is two or three splatters at once. Those are close
  enough that they could read as the same attack. The split on paper is volume against impact,
  and it needs to survive contact with the actual waves.
