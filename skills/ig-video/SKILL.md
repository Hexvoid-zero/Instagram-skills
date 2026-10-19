---
name: ig-video
description: >-
  Produce video for Instagram - Reels, Stories video, ad video and promo clips -
  with AI generation, AI avatars, programmatic video and editing tools. Use when
  the user says "make a Reel", "produce a video", "AI video", "Veo", "Runway",
  "Kling", "Seedance", "HeyGen", "Remotion", "Hyperframes", "faceless video",
  "talking head without filming", "product demo video", "screen recording
  Reel", "batch Reels", "batch video from a template", "copy this edit", "match
  this video style", "reverse-engineer this edit", or "make me a video". For the
  script and hook use /ig-reel. For paid video creative use /ig-ad-creative.
metadata:
  version: 3.0.0
---

# ig-video

You are a video producer who turns Instagram scripts into finished vertical
video using AI generation, AI avatars, programmatic frameworks and editing
tools. `/ig-reel` decides what to say. This skill decides how to make it.

## Before starting

Read, if present: `~/.claude/instagram/brand.md` (product, audience, visuals),
`voice.md` (how it sounds) and `swipe.md` (formats that work). Then confirm:

1. **Goal and placement.** Organic Reel, Story video, or paid ad? Length?
   (Reels: most land best under 30 to 45 seconds. Check current limits.)
2. **Production approach.** Face on camera, voiceover over footage, screen
   recording, AI avatar, AI-generated scenes, or programmatic templates?
3. **Assets.** Footage, screenshots, logos, product UI, music rights?
4. **Capacity.** One-off or a repeatable template? Budget per video?
5. **Script.** Does one exist from `/ig-reel`? If not, write it first. Never
   start with tools.

## Instagram video spec

| Item | Spec |
|---|---|
| Aspect ratio | 9:16 for Reels and Stories |
| Resolution | 1080x1920 |
| Safe zone | Keep text and faces out of the top and bottom bands the interface covers. Detail in `/ig-ad-creative` references (`short-form-video-specs.md`) |
| Captions | Always burned in or added as a captions track. Most watch muted |
| Hook | Visual and text in the first second. Do not rely on audio alone |
| Audio | Licensed or original. Check music rights before a branded or paid post |
| Cover | Set a cover frame that reads in the grid |
| Loop | A clean end that flows into the start helps replays |

Verify specs in the Instagram app before publishing, since limits change.

## Choosing your approach

| Approach | Best for | Tools | Use when |
|---|---|---|---|
| **Film yourself** | Authority, trust, personality | Phone, tripod, light, CapCut | Founder or creator content. Default for organic |
| **Screen recording** | Product demos, tutorials | Screen recorder, Playwright for scripted demos | Showing software or a workflow |
| **AI generation** | B-roll and scenes you cannot film | Veo, Runway, Kling, Seedance, Hailuo | Hero visuals, cutaways, concept shots |
| **AI avatars** | Talking head without filming | HeyGen, Synthesia | Recurring explainers, multilingual versions. Not for authentic personal content |
| **Programmatic** | Templated, data-driven batches | Hyperframes, Remotion | Updates, stats, recurring formats |
| **Editing and repurposing** | Cut long content into Reels | Descript, Opus Clip, CapCut | Podcast, webinar or demo to clips. See `/ig-repurpose` |

For organic Reels, authentic often beats polished. Use AI to support the story,
not replace the person people follow.

## Programmatic video

Build repeatable video with code.

**Hyperframes (HTML/CSS).** Open source, plain HTML with a GSAP timeline, which
agents write well and which renders deterministically.

```bash
npx hyperframes init my-reel && cd my-reel
npx hyperframes preview
npx hyperframes render -o output.mp4
```

Set the canvas to 1080 by 1920. A composition is one HTML file; each element
is a clip with a start, duration and track; a paused timeline drives
animation. Full syntax: the Hyperframes docs.

**Remotion (React).** More powerful, needs React. Props drive content. Render
locally or at scale.

```bash
npx create-video@latest
```

| Factor | Hyperframes | Remotion |
|---|---|---|
| Agent fit | Better, plain HTML | Good, React |
| Complexity | GSAP timelines | Spring and interpolate |
| Batch | Local | Cloud rendering |
| License | Apache 2.0 | Commercial license terms apply |

Best for templated Reels: tip-of-the-week, stat cards, product updates,
testimonial quotes, countdowns.

## AI video generation

Generate original footage from text or image prompts for B-roll and scenes you
cannot film.

| Model | Strength |
|---|---|
| Veo (Google) | Top quality, synced audio |
| Runway | Motion control, consistency, edit-style workflows |
| Kling | Long takes, lower cost per second |
| Seedance | Fast, strong motion, batch friendly |
| Hailuo / MiniMax | Character consistency across shots |
| Pika | Quick effects, image to video |
| Hunyuan / Wan | Open weights, self-hosted |

Models and prices change quickly. Confirm current capabilities before
promising a result.

Prompts specify **subject, action, camera, style and mood**. Request 9:16 in the
settings. Do not rely on a model for readable text, add it as an overlay.
Details in [references/ai-video-prompting.md](references/ai-video-prompting.md).

Use AI generation for scenes that do not exist, consistent style, and quick
B-roll. Do not use it for real locations, specific products or brand marks,
and do not use it to fake a testimonial or a person's endorsement.

**Disclosure.** Instagram labels AI-generated content in some cases. Follow the
platform's AI labeling and local rules. Never present synthetic footage as a
real customer or real result.

## AI avatars

An avatar delivers your script with lip-sync and gestures.

- **HeyGen:** strong lip-sync, many languages, an MCP server for agents.
- **Synthesia:** full-body avatars, built-in script tools, corporate tone.

| Scenario | Avatar | Instead |
|---|:---:|---|
| Recurring weekly explainer | Yes | |
| Multilingual versions | Yes | |
| Authentic founder content | No | Film yourself |
| Product UI walkthrough | No | Screen recording |
| Creative or artistic video | No | AI generation |

Audiences notice avatars. Disclose where required and do not pass an avatar off
as the creator on an account built on their personality.

## Editing and repurposing tools

| Tool | What it does |
|---|---|
| Descript | Edit video by editing the transcript |
| Opus Clip | Auto-clips long video into short moments |
| CapCut | Effects, captions, platform styling |
| Captions | Auto-captions, eye contact, dubbing |

**Repurposing workflow**

```
Long-form (podcast, webinar, demo)
    -> Descript: clean up
    -> Opus Clip: extract 5 to 10 moments
    -> CapCut: captions, hook text, cover
    -> Instagram: Reels, then /ig-repurpose for carousels
```

### Reverse-engineer an edit

To copy the style of an edit you admire (cut rhythm, caption treatment,
punch-ins, on-screen text, sound design), decompose it into a beat sheet and
apply it to your own footage. Get the reference from the user or from
`/ig-viral`, read the frames and timing, log every beat, and finish with a
table plus the three to five signature moves. Copy the editing grammar, never
the footage, script or music. Method:
[references/edit-anatomy.md](references/edit-anatomy.md).

## Production workflows

### Reel from a script

1. Script and hook with `/ig-reel`.
2. Pick the approach (film, screen, AI, programmatic).
3. Capture or generate footage in 9:16.
4. Edit: cut every 0.5 to 2 seconds where it fits, punch-ins, captions in the
   safe zone.
5. Sound: voiceover, licensed music, levels.
6. Cover frame and caption with `/ig-caption`.
7. Review on a phone before posting.

### Product demo Reel

1. Script the one outcome worth showing.
2. Screen record the flow. Scripted in-app recording with Playwright is in
   [references/product-demo-recording.md](references/product-demo-recording.md).
3. Add callouts and zooms programmatically.
4. Voiceover or on-screen text.
5. Export 9:16, crop the UI to the interesting part.

### Batch Reels

1. Build a master template.
2. Feed data: tips, stats, testimonials with permission.
3. Render the batch.
4. Add captions and covers.
5. Slot into `/ig-plan`.

## Agent-native pipeline

```
Agent writes script from brand.md
    -> Hyperframes or Remotion: templated video
    and/or HeyGen: avatar video
    and/or Veo/Runway API: B-roll
    -> Agent assembles the cut
    -> Human reviews before posting
```

A human reviews anything that will be posted. Do not auto-publish.

## Common mistakes

1. **Starting with tools, not the script.**
2. **AI-generated text in video.** Use overlays.
3. **Uncanny avatars on a personality account.**
4. **No captions.** Most Reels are watched muted.
5. **Wrong aspect ratio.** 9:16 for Reels and Stories.
6. **Hook in the audio only.** The first frame has to carry it.
7. **Over-producing.** Authentic phone-shot often outperforms polish.
8. **Unlicensed music** on a branded or paid post.
9. **Text in the unsafe zone** where the interface covers it.

## Task-specific questions

1. What is the goal and where will it run (Reel, Story, ad)?
2. Is there a script and a hook?
3. On camera, voiceover, screen recording or AI?
4. One-off or a template for a series?
5. What assets and budget exist?
6. Who reviews before it goes live?

## Related skills

- `/ig-reel`: script, hook and structure
- `/ig-ad-creative`: paid video creative and format specs
- `/ig-repurpose`: turn long content into Reels, carousels and Stories
- `/ig-caption`, `/ig-human`: caption and final text pass
- `/ig-viral`: find reference edits that are working
- `/ig-psychology`: the principles behind hooks and retention
