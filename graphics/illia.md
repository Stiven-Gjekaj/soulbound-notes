# Illia's look

What she wears, what reads at 640x480, and the one hierarchy the fight cannot survive losing.

Related: [graphics](graphics.md), [Illia](../bosses/illia.md) for the fight this serves,
[writing](../writing/writing.md) for the tell her dialogue shares.

## Settled

- **Beanie.**
- **A small braid** at the side of her face, on the viewer's left.
- **Farm overalls and boots.**
- **Paint-stained.**
- **Bare forearms.**
- **Brush in her right hand**, which is the viewer's left when she faces the player.
- **Nineteen years old**, with brown hair.
- **Five wind-up poses**, one per attack form.

## The one rule

> The brush tip is the brightest, highest-contrast point on her. Nothing she wears beats it.

Everything below is downstream of that. The brush carries every telegraph in the fight: the
player reads the stroke, not her face, to know what is coming. If the brush disappears into
her, the fight stops being legible and no amount of good art fixes it.

She stays in full colour. The rule is not about desaturating her, it is about one point winning.

## The overalls are what make paint-stained work

Splatter on a busy surface is noise. Splatter on one large flat mid-tone reads as splatter.
Overalls are exactly that surface, denim or canvas, so the stains land as texture rather than
as competing detail. This is the reason the paint-stained direction survives contact with the
rule above, and it would not have on a more decorated costume.

**The stains run away from her hands.** Filthiest at the boots and the overall legs, less on
the bib, less again up the forearms, and her hands and face nearly clean. That is what a person
who wipes their hands and never wipes their boots actually looks like, and it keeps the paint
off the six inches of sprite nearest the brush tip, which is the one place it cannot go.

## Bare forearms are the gesture

Four of her five wind-ups are told apart by how she moves the brush, so the arm has to be
readable in motion against a dark background. Bare skin is a mid-value shape that holds its
edge; a long dark sleeve swallows the same motion and takes the fight's readability with it.

The forearm and the brush are not competing. The arm is the vector and the tip is the point it
aims: together they read as one gesture, which is what a telegraph needs to be.

## The beanie carries the run-down

Her irritation is a count of seven with no meter, so her dialogue and her face are the only
signal it exists. A face at this resolution cannot hold seven readable expressions. A hat can.

Pushed back, then straightened, then tugged down over the eyes as she stops having anything
left to say. A player reads hat position without being told to, it costs one sprite element
instead of seven faces, and it lands the tell in the same place the last written line does.
Whether the hat carries part of the tell or all of it is a question for
[writing](../writing/writing.md).

## The brush tip is the colour of what is coming

The tip is already the loudest point by rule, so give it the colour of the paint she is about
to use. The telegraph then says which attack is coming as well as that one is, at no cost, on
the one element that is allowed to shout.

This is also where the earliest idea in this project's art direction finally landed. It started
as "each new bullet type is a new colour she has just discovered", which needed her to be
colourless for it to read. She is not colourless, so it lives in the tip instead, which is a
smaller home and a better one.

## Palette, by consequence

The rule and the costume decide most of it. Overalls low-saturation mid-tone. Boots and stains
lower still. **The beanie is the one safe place for a saturated signature colour**, since it
sits about as far from the brush hand as anything on her does, and a boss select entry wants a
colour you recognise from across the screen.

Brown hair narrows the overalls. Brown hair against tan canvas puts two low-saturation browns
next to each other at head and torso, and at this resolution they merge into one mass with a
beanie floating on top. **Denim blue separates them and canvas does not**, so unless the beanie
is carrying an unusual amount of contrast on its own, the overalls want to be blue.

It also means the hair is not a recognition cue. Brown is the least distinctive colour a
character can have, which is fine here because it puts all of that work on the beanie, where
the rule already wanted it.

## Five poses is exactly the minimum, so nothing is spare

Five wind-ups covers one per attack form: two brush, two bucket, one splodge. There is no
redundancy in that, which has two consequences worth building around.

**The two pairs need the most separation and get the least help.** Brush against brush and
bucket against bucket are the recognition test, and
[Illia](../bosses/illia.md) requires each pair to be tellable apart from the first moment of the
stroke. Splodge has no partner, so its pose is free to be the most distinct of the five and
should be, since it costs nothing.

**Five wind-ups is not five sprites.** She is on screen during every dialogue turn, so she also
needs an idle, and the beanie tell needs a pushed-back, a straightened and a tugged-down.
Counted naively that is nine poses rather than five.

It does not have to be. **Draw the beanie as its own element layered over the body.** Three hat
positions across six body states gives eighteen readable combinations out of nine assets, the
hat tell becomes available in every pose rather than only in an idle, and adjusting the tell
later costs three small sprites instead of a redraw. The engine loads sprites individually, so
layering is a scripting question rather than an art one.

## She is nineteen

Worth stating because it reaches past the art. Farm overalls, a beanie and a braid on a
nineteen year old reads as somebody who works rather than somebody with a title, which is the
right register for a boss who is testing you rather than trying to kill you.

It also sets the voice. Her seven responses to being attacked run down toward irritation, and a
nineteen year old runs out of patience differently from a master with a grievance: shorter,
blunter, more bored than wounded. See [writing](../writing/writing.md).

## Silhouette

Rounded top, boxy middle, heavy feet. Beanie, overall bib and boots give her an outline that
survives with no interior detail at all, which matters because her select entry sits beside six
locked ones rendered as silhouettes and hers is the reference for that treatment. See
[boss select](../ui/boss-select.md).

The braid is what makes it hers rather than generic. It is a small asymmetric notch at head
height, and it tells you which way she faces with no other information present. So it never
flips sides, in any pose or any frame.

**One consequence of the two sides chosen.** Her right hand is the viewer's left, and the braid
is also on the viewer's left, so both of her distinguishing features sit on the same side. That
is a strong, unmistakable read, and it makes the braid the one element with a real chance of
competing with the brush for the eye. Keep it low contrast. It is a silhouette marker, not a
focal point.

## Open questions

- **What is under the overalls?** Bare forearms are settled, the shoulders are not, and the
  shirt decides whether her upper arm reads as part of the gesture or as part of the torso.
- **How much hair shows under the beanie**, beyond the braid. It is the difference between the
  beanie being a hat she wears and the beanie being her head shape.
- **Are the overalls blue?** See the palette note. Brown hair makes it close to a decision
  rather than a preference.
- **Is the beanie a separate sprite?** If the hat tell is layered rather than drawn into each
  pose, the asset count roughly halves and the tell works in every pose. Worth deciding before
  anything is drawn rather than after.
- **Anything else Soultale fixes about her.** Age and hair are answered. Build, height and
  whatever else the story has already committed to are not, and this page is what the fight
  requires of her rather than who she is.
