---
name: viral-storytelling
description: Storytelling method for animated or AI-generated videos, from 60-second vertical shorts to 8–12 minute long-form stories. Use when writing or revising a video script, a hook, a narration, a beat sheet, a storyboard or a scene-by-scene direction table; when adapting a story between short and long format; or when reviewing whether each spoken line is backed by a visible action on screen. Covers explainer shorts (how a mechanism works) and true-story narratives (survival, history, mystery).
---

# Viral storytelling

A script is a promise that the picture keeps. Every method in this skill serves one rule:

> **The image explains the sentence at the moment it is spoken.**

If a line has no visible action, it is either cut or the scene is built for it. A new line of narration never creates a new scene by itself.

## Pick the format first

| | Short | Long-form |
|---|---|---|
| Length | 45–100 s, vertical 9:16 | 8–12 min, horizontal 16:9 |
| Unit | 4–6 beats of 1–3 sentences | 10–12 blocks of 30–90 s, cut into 10 s scenes |
| Hook | first 1–3 s, picture + line | first 20–30 s, cold open in the middle of the action |
| Arc | one question, one answer | several open loops, each paid off later |
| Detail | `references/short-form.md` | `references/long-form.md` |

Both formats share the beat engine (`references/beats.md`), the script-to-scene contract (`references/script-to-scene.md`) and the fact check (`references/facts.md`).

## Workflow

1. **Brief.** Write down: audience, topic, format, and *one sentence the viewer must understand by the end*. If that sentence is missing, stop and ask.
2. **Facts before words.** Research primary sources and fill `templates/facts.md`: every claim in the narration gets a source, a strength (strong/medium/weak) and the limit of what the picture may show. Weak claims are rewritten or dropped. Fiction, jokes and dramatizations are listed as such.
3. **Beat sheet.** Build the skeleton with the beat engine: *hook → first event → failure → fix → retest → limits/close* for explainers; *cold open → setup → rising danger → turn → struggle → rescue/answer → echo* for true stories. One beat = one idea.
4. **Script with anchors.** Write the narration in `templates/script.json`. Mark the exact word where each visual action lands with a unique anchor: `{valve}valve`. Never use vague anchors or word prefixes.
5. **Direction table.** For each anchor fill `templates/direction.json`: line, what is shown, framing/zoom, on-screen text, sound. One visible action per line. No action → rewrite the line or build the scene.
6. **Storyboard** (long-form or AI-generated video). Cut the timeline into 10 s scenes with a first and last frame each (`templates/storyboard-scene.md`). Write continuity rules (character marks, props, screen direction) *before* generating any image.
7. **Read-aloud pass.** Read the script out loud at the target pace (~150 words/min for long-form conversational, ~160–170 for shorts). Cut any sentence you cannot say in one breath.
8. **Review.** Run `references/review-checklist.md` against the preview: compare each sentence with the frame at its anchor, list concrete defects with timestamp, sentence and fix. Distinguish what was measured from editorial judgment; list what still needs a human listen.

## Non-negotiables

- **Hook = picture + line together.** The first frame already shows the strongest image; the first line poses the question or states the impossible fact.
- **Failure before fix, fix before retest.** An explainer shows the problem and its consequence, then the fix *installed with real support*, then the *same* test again in a comparable frame.
- **Plant and pay off.** Every object, fact or phrase that matters at the end appears earlier. Nothing important arrives from nowhere.
- **Anticipation before impact.** A pause, silence or still frame precedes every strong moment.
- **One focus per frame.** Little text, one item at a time, at the bottom. Labels point only to parts that are visible and already in place.
- **Recognizable scale.** Hands are anatomical and age-correct; objects keep real proportions.
- **Honest close.** State what the model simplifies or what the sources dispute. Never invent sources, testimonials, audience numbers or results.
- **Sensitive real stories.** Dramatize without gore: injuries are implied, never shown. Call reconstructions "reconstruction" and AI imagery "AI-generated".
- **Voice change = new timing.** Timings from a silent or old draft do not prove sync with a new narration. Re-time after every new voice take; keep approved audio when only visuals change.

## Files

- `references/beats.md` — the beat engine, hooks, open loops, sentence rules
- `references/short-form.md` — 60–100 s structure, timing table, examples
- `references/long-form.md` — block map, rhythm per block, mid-roll CTA, extra case, closing question
- `references/script-to-scene.md` — anchors, direction table, camera grammar, continuity, documentary vs. explainer looks
- `references/facts.md` — sourcing rules and limits of representation
- `references/review-checklist.md` — what to check before delivery
- `templates/` — `script.json`, `direction.json`, `facts.md`, `storyboard-scene.md`, `brief.md`
- `examples/` — `mechanism-short.md` (explainer), `true-story-long.md` (10-minute survival story)
