# Writing notes

How to name a note, how to shape it, and how to link it so the vault stays navigable as it
grows.

The other rules: [Scope](scope.md), [House style](style.md). Back to the
[README](../README.md).

---

## One subject per note

A note covers one thing. One boss, one attack, one screen, one argument.

If a note needs a table of contents to be usable, it is two notes. If you cannot name it
without the word "and", it is two notes. Splitting is cheap here because the link between the
halves survives the split and shows up in the graph.

## Naming

Filenames are lowercase, hyphenated, and end in `.md`.

```
opening-attack-pacing.md
boss-two-silhouette.md
why-the-timer-is-optional.md
```

Name a note after its subject, not after the day it was written and not after who wrote it.
Dates belong in the text if they matter, and git already knows who wrote what and when.

## The first lines

Every note opens with a single `#` heading matching its subject, then one or two lines saying
what the note is about, then the links to whatever it relates to. Somebody arriving from the
graph should know within five seconds whether they are in the right place.

The [README](../README.md) is the exception. It is the vault's front page rather than a note,
and it is titled by the repository it sits in.

If the note has been settled, the decision goes immediately under the heading, in a sentence.
Nobody should have to read an argument to the end to find out how it came out.

## Linking

Use ordinary Markdown links with a relative path:

```markdown
[the opening attack](opening-attack-pacing.md)
[the scope rules](../rules/scope.md)
```

Not `[[wikilinks]]`. Obsidian resolves both and draws both in the graph, but GitHub renders
only the first, and a good half of the reading here happens in a browser.

Two conditions on every note:

- It links out to at least one other note.
- At least one other note links to it.

The second one is the one people forget. When you add a note, add the link to it from wherever
somebody would go looking, in the same commit. A note nothing points at is invisible in the
graph and will be rewritten from scratch by somebody in three months.

The [README](../README.md) is the hub. Anything that does not obviously hang off an existing
note hangs off that.

## Folders

Every note lives in a topic folder. There are eight, and each one has a README saying exactly
what it takes and what it does not:

| Folder | Takes |
| ------ | ----- |
| [general](../general/README.md) | The project as a whole, and anything with no better home |
| [gameplay](../gameplay/README.md) | Mechanics, difficulty, pacing |
| [bosses](../bosses/README.md) | One note per boss: attacks, phases, the shape of the fight |
| [ui](../ui/README.md) | Screens, menus, the HUD, and the information they carry |
| [graphics](../graphics/README.md) | Art direction, sprites, effects |
| [writing](../writing/README.md) | Dialogue, names, flavour text, tone |
| [sound-design](../sound-design/README.md) | Music, sound effects, audio tells |
| [testing](../testing/README.md) | Playtest reports and impressions of a build |

Pick the folder by what the note is mostly about, then link to the others instead of
duplicating them. A note about how a boss's second phase sounds is a `bosses` note linking to
`sound-design`, not two half-notes that each cover a bit of it.

If a note truly fits nowhere, it goes in `general`. When `general` grows three notes about the
same new thing, that cluster becomes the ninth folder.

Folders do not affect the graph. Links do. Moving a note between folders is safe as long as
the links pointing at it move too, which Obsidian handles when you rename from inside the app.

## Images

Screenshots and reference art go in `attachments/`, named after what they show rather than
what the camera called them:

```
attachments/boss-two-phase-change.png
```

Not `Screenshot 2026-08-01 at 14.22.13.png`. Point at the image from the note that discusses
it. An image with no note around it explains nothing six months later.

Keep them reasonable in size. This is a vault people clone on laptops, not an asset store.

## Open questions

A note with unresolved parts ends with an `## Open questions` heading and a list of them.

That heading is doing real work. It marks the difference between an argument that finished and
an argument that stopped, and it gives the next person a way in that is not rereading
everything above it.

## Changing somebody else's note

Edit it. This is not a review process and nothing here needs approval.

The two things to avoid: deleting a position because you disagree with it, and rewriting a
settled decision without saying what changed. Add your disagreement underneath, sign it if the
note is a back-and-forth, and let git hold the history.
