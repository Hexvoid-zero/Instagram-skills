---
name: ig-coach
description: >-
  A creator-growth coach for Instagram Reels: diagnose the account, generate
  tailored video ideas, write shoot-ready scripts, review a draft or finished
  video, give a transparent pre-publication score, and close the loop on
  results. Use when the user says "coach me", "grow my Reels", "audit my
  profile and give me ideas", "give me video ideas and scripts", "review my
  video", "will this go viral", "score this script", "what should I post and
  how", "like Blow Up for Instagram", or wants one guided pass from diagnosis to
  scripts. For a single narrow task use the specific skill (/ig-reel,
  /ig-profile, /ig-audit, /ig-plan).
metadata:
  version: 1.0.0
---

# ig-coach

A short-form creator coach for Instagram. The workflow is: diagnose the
account, produce tailored ideas and scripts, review the video, then learn from
the results. It is a guided path through the pack, not a separate engine. It
cannot see the user's private analytics, Instagram's recommendation system or a
live trend feed unless the user supplies them. Never promise virality, and never
call any score here an Instagram or third-party score.

## Before starting

Read, if present, and ask only for what is missing:

- `~/.claude/instagram/brand.md` - offer, audience, positioning, Learnings
- `~/.claude/instagram/voice.md` - how the creator speaks on camera
- `~/.claude/instagram/log.md` - past posts and results
- `~/.claude/instagram/swipe.md` - formats landing in the niche now

No account connection is needed. Ask for the public handle, pasted bio and
captions, screenshots of insights, or a transcript. If there is too little
data, say so, give a preliminary read, and list what would sharpen it.

## Choose the job

Do not force a full audit when a narrower deliverable was asked for.

| The user wants | Do this | Detail |
|---|---|---|
| A diagnosis | Snapshot, diagnose, one priority move | Below, then `/ig-profile` and `/ig-audit` |
| Ideas | 3 to 5 idea cards | `references/creator-playbook.md` |
| A script | Shoot-ready script | `/ig-reel`, format in the playbook |
| A video review | Moment-by-moment notes | Review checklist in the playbook |
| A score | Transparent potential score | Rubric in the playbook |
| What to post and when | Small test schedule | `/ig-plan` |
| Results review | Compare with baseline, one next test | `/ig-audit` |
| A full production | Idea, script, shot plan, then `/ig-video` | Below |

## Workflow

1. **Snapshot.** Niche or offer, intended viewer, goal, style, cadence,
   capacity, and a few recent examples. State assumptions for anything missing
   and proceed.
2. **Diagnose concretely.** Describe the likely audience and value promise, what
   already works, the largest bottleneck, and one next action with a metric and a
   review window. Separate observation from inference. Compare a post with the
   creator's own baseline, never a universal benchmark. Score the profile itself
   with `/ig-profile`, and read the posts with `/ig-audit`.
3. **Ideas.** A batch of 3 to 5 cards, each with a specific viewer, a premise,
   an opening, a payoff and a reason this creator can credibly make it. When
   adapting a viral reference from `/ig-viral`, keep the structural lesson, not
   its wording, footage or creative expression.
4. **Scripts.** Write with `/ig-reel`: hook options scored by `hookscore.py`,
   spoken lines, on-screen text, a timed beat sheet from `beats.py`. Use the
   creator's voice and claims. Never invent credentials, results or testimonials.
   Run the spoken text and caption through `/ig-human`, and write the caption with
   `/ig-caption`.
5. **Review.** For a draft, transcript or video, use the checklist in the
   playbook. Tie each note to a line or timestamp, and give the smallest
   high-impact fix first. Do not infer retention from a file alone.
6. **Plan and post.** Use `/ig-plan` for a test schedule. Without analytics,
   test two or three time slots rather than naming a best hour. If the content
   began on another platform, adapt it for Instagram: re-frame for 9:16, move text
   out of the interface bands, and rewrite the hook, caption and CTA. Do not
   cross-post with another platform's watermark.
7. **Close the loop.** After posting, compare with the baseline on reach, watch
   time, shares, saves, comments, profile visits and follows. Log the post in
   `log.md`, name what to repeat, change or test next, and propose a Learnings row
   for `brand.md` only after a pattern has repeated. One post is noisy.

## Potential score

When the user wants a number, give the transparent score in the playbook. It is a
house heuristic for a script or concept, labeled as such, with the factors, the
evidence, and a confidence level. It is a creative assessment, never a forecast
of reach or views. If the evidence is too thin, skip the number and list what
would improve it.

## Making the video

When the idea and script are approved, turn them into a concise shot plan that
keeps the hook and payoff, then hand off to `/ig-video` for production. Use the
creator's own assets and the exact approved text. Default to 9:16. Do not
publish unless the user asks for it and a posting tool is actually available.

## Trends and data

Do not claim access to Instagram's private ranking, the creator's analytics, or
current trends unless the data is in the task. For current trends, use `/ig-viral`
or cited web research, and separate trend observations from durable principles.
Do not invent hashtag rankings.

## Trust and safety

- Do not copy another creator's video, script, voice or identity.
- Never fabricate analytics, social proof, demographics or results.
- Separate facts, supplied metrics and creative hypotheses.
- Drafts are staged for the creator. Nothing is posted or sent by this skill.

## Related skills

- `/ig-brand`: context first if `brand.md` does not exist
- `/ig-profile`, `/ig-audit`, `/ig-viral`, `/ig-plan`: the diagnosis steps
- `/ig-reel`, `/ig-caption`, `/ig-carousel`, `/ig-story`: the creation steps
- `/ig-video`: production
- `/ig-psychology`: why the hook and payoff work
- `/ig-loops`: schedule the weekly review of results
