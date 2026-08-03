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
- **Nineteen years old**, five foot eight and lean. The height is canon.
- **Brown hair**, with some of it showing past the beanie.
- **Blue overalls**, over basic clothes.
- **Five wind-up poses**, one per attack form.
- **The beanie is its own sprite**, layered over the body rather than drawn into each pose.

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

**The shirt is functionally the sleeve.** Almost all of it sits behind the overall bib, so the
only part of it anyone sees is the upper arm, which is the top half of every gesture. That
makes its value a readability decision rather than a wardrobe one: a dark sleeve leaves only
the forearm visible against black and the telegraph reads from the elbow down, which is half
the arc. Something light or mid keeps the whole arm in play, and the sleeve edge then gives the
gesture a natural articulation point partway along it.

## Lean, and not trying to be imposing

Five foot eight and lean means she is not a physically threatening shape, and she should not be
drawn as one. Everything dangerous about this fight is in the arena, not in her posture. That
matches a boss who is testing rather than killing, and it is why the brush hierarchy works: the
loudest thing about her is the tool, which is exactly the right reading for someone who thinks
of this as work.

Loose overalls on a lean frame also give a useful silhouette: a narrow body inside fabric that
does not fit closely. It reads as working clothes rather than a costume, and it keeps the boxy
middle the outline needs without making her bulky.

One knock-on for [boss select](../ui/boss-select.md): she is a tall, narrow sprite, roughly
three times as high as she is wide. Seven entries share a screen, and the slot proportions
should suit that rather than fighting it.

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

The overalls are blue. Brown hair against tan canvas would have put two low-saturation browns
at head and torso, and at this resolution they merge into one mass with a beanie floating on
top. Denim separates them.

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

## The beanie is a separate sprite

Six body states and three hat positions, nine assets, eighteen readable combinations. The hat
tell works in every pose rather than only in an idle, and tuning it later costs three small
sprites instead of nine redraws.

This is the engine's own documented pattern rather than a trick.
`docs/api/sprites-and-animation.md` uses a multi-part character as its worked example,
building one out of separate torso, legs and head sprites joined with `SetParent`, with each
part's position relative to its parent. Illia is that with two parts instead of three.

Two things follow, and both land on whoever draws her rather than on whoever scripts it.

**Her head does not move between poses.** A parented sprite sits at a fixed offset from its
parent, so if her head shifts as she winds up an arm, the beanie drifts off it. Keeping the
head at a constant position across all six body states makes the offset a single number that is
right everywhere. This costs nothing, because every gesture in the fight is in the arm.

**The body sprite carries a full head of hair.** The beanie is drawn on top and the three
positions cover different amounts of the crown, so the pushed-back state exposes hair that the
tugged-down state hides. If the body is drawn assuming a hat, the tell reveals a bald patch the
first time she pushes it back.

## She is nineteen

Worth stating because it reaches past the art. Farm overalls, a beanie and a braid on a
nineteen year old reads as somebody who works rather than somebody with a title, which is the
right register for a boss who is testing you rather than trying to kill you.

It also sets the voice. Her seven responses to being attacked run down toward irritation, and a
nineteen year old runs out of patience differently from a master with a grievance: shorter,
blunter, more bored than wounded. See [writing](../writing/writing.md).

## Silhouette

Rounded top, boxy middle, heavy feet. Beanie, overall bib and boots give her an outline that
survives with no interior detail at all.

That used to matter because the [boss select](../ui/boss-select.md) drew locked entries as
silhouettes and hers was the reference for that treatment. It no longer does: locked entries
now show the boss's own icon under a padlock. The requirement survives the change anyway, for a
different reason. Her icon sits on a turning wheel at whatever size the arc gives it, five
entries on screen with the two at the ends scaled down and fading, so it has to stay
identifiable small and dim. An outline that reads with no interior detail is what does that.

The braid is what makes it hers rather than generic. It is a small asymmetric notch at head
height, and it tells you which way she faces with no other information present. So it never
flips sides, in any pose or any frame.

**One consequence of the two sides chosen.** Her right hand is the viewer's left, and the braid
is also on the viewer's left, so both of her distinguishing features sit on the same side. That
is a strong, unmistakable read, and it makes the braid the one element with a real chance of
competing with the brush for the eye. Keep it low contrast. It is a silhouette marker, not a
focal point.

## Open questions

- **How light is the sleeve?** The only decision left that the fight actually depends on, for
  the reason above. Everything else here can be adjusted after the first generation; this one
  changes how much of the telegraph the player can see.
- **Which paint colours are hers?** The brush tip takes the colour of the attack it is about to
  make, so brush, bucket and splodge each need one, distinct from each other and from the blue
  of the overalls.
