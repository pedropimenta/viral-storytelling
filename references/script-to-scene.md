# Script-to-scene contract

## Anchors

An anchor is a unique id written in braces right before the word where something must happen on screen:

```
"The {pulley}drive pulley grips the cables. When it turns, the {car}car rises while the {counterweight}counterweight goes down."
```

- Unique per script; never reuse an id or match by word prefix.
- If you rename a word, keep the anchor; if you remove an anchor, remove its direction row and timeline cue together.
- The narration audio produces word timings; the anchor's time is the timestamp of the word right after it.
- `{start}` on the first beat and `{end}` on the last are reserved.

## Direction table

One row per anchor (`templates/direction.json`):

| Field | Meaning |
|---|---|
| `anchor` | `b1:failure`, `b2:fix` … or the anchor id |
| `line` | the exact text excerpt from the script |
| `shows` | the visible action (verb + object) |
| `zoom` | which part and which detail fills the frame |
| `text` | on-screen text, or `none` |
| `sound` | effect or ambience, or `none` |

A row whose `shows` is empty or abstract ("concept of energy") is a defect.

## Camera grammar

- Continuous camera that travels to the part named in the line; arrive *before* the word, act *on* the word.
- Close-up for actions, wide for recaps and for "the whole path".
- The retest uses the same framing as the failure so the difference reads instantly.
- One focus per frame; darken, blur or freeze the rest (staging).
- Respect screen direction across cuts (180° rule).

## On-screen text and labels

- Subtitles always at the bottom, rendered into the scene.
- Other text: short, one item at a time, never competing with the subtitle.
- Labels only for parts that are visible and already installed; parts not yet built stay invisible; installed parts stay in place.

## Hard cuts inside a scene

When a 10 s scene needs two or three images, split it into segments (e.g. 0–5 s / 5–10 s or 0–4 / 4–7 / 7–10), each starting from its own reference frame. Use a hard cut when the label says "CUT", when the camera move implies a new place, or when a continuous move would make the model invent people or objects between the two frames.

## Generation hygiene (AI video)

- State in every prompt that it is a staged reconstruction with actors and makeup; nobody is hurt.
- Replace violent words with neutral ones; imply injuries, never show wounds.
- If the model keeps inventing a person from an object at the frame edge, crop the reference or use a slow zoom on the still instead of rerolling.
- Check a contact sheet (3 frames per scene) of every batch before moving on.
