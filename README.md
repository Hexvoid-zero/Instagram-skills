<div align="center">


# Instagram plugin for Claude

A Claude and Codex plugin with 24 skills for running an Instagram account: strategy,
content, engagement, paid ads, PR and video. Version 0.3.0.

<a href="https://www.instagram.com/hexvoid-zero"><img src="https://img.shields.io/badge/Instagram-E4405F?style=flat&logo=instagram&logoColor=white" alt="Follow on Instagram" /></a>

<div align="left">  

## Install

Download or clone this repo, zip the contents of the repo root as
`instagram.plugin` (the `.claude-plugin/` folder and `skills/` must be at the
top level of the zip), and add it to Claude as a plugin:

```bash
git clone <your-repo-url> instagram-plugin
cd instagram-plugin
zip -r ../instagram.plugin . -x '.git/*'
```

## Layout

```
.claude-plugin/plugin.json   plugin manifest
skills/<skill>/SKILL.md      one folder per skill, with references/ and scripts
README.md
```

## What is in it

Twenty-four skills that cover the full Instagram loop: strategy, creation,
engagement, paid, and the context that ties them together.

| Stage | Skills |
|---|---|
| Context | `ig-brand` (writes `brand.md`, the file every other skill reads) |
| Strategy | `ig-coach` (guided diagnosis, ideas, scripts and review), `ig-growth-plan`, `ig-plan`, `ig-profile`, `ig-audit`, `ig-viral`, `ig-ideas`, `ig-council`, `ig-psychology` |
| Create | `ig-reel`, `ig-carousel`, `ig-story`, `ig-caption`, `ig-repurpose`, `ig-video` |
| Engage | `ig-comment`, `ig-reply`, `ig-dm` |
| Paid | `ig-ads`, `ig-ad-creative` |
| Systems | `ig-loops` (recurring workflows) |
| Reputation | `ig-pr` (press, creator collabs, crisis response) |
| Polish | `ig-human` (de-slop and AI-detection score) |

## Start here

1. Run `/ig-brand` to capture offer, audience, positioning and voice. It writes
   `~/.claude/instagram/brand.md`, which the other skills read first.
2. Run `/ig-growth-plan` for the quarter, then `/ig-plan` for the week.
3. Create with `/ig-reel`, `/ig-carousel` and friends. Every draft goes through
   `/ig-human` before you post.
4. Review with `/ig-audit`, and set up recurring routines with `/ig-loops`.

## Shared files

Everything lives in `~/.claude/instagram/` so it survives plugin updates:

| File | Written by | Read by |
|---|---|---|
| `brand.md` | `ig-brand` | most skills (offer, audience, Learnings, paid settings) |
| `voice.md` | `ig-brand`, `ig-reel` | all drafting skills |
| `swipe.md` | `ig-viral` | `ig-reel`, `ig-ads`, `ig-ad-creative`, `ig-plan` |
| `log.md` | you | `ig-audit`, `ig-plan`, `ig-ideas`, `ig-loops` |
| `plan.md` | `ig-plan` | `ig-loops`, `ig-council` |
| `plans/<slug>/` | `ig-growth-plan` | `ig-plan` |
| `loops/` | `ig-loops` | `ig-loops` |
| `advisors/` | `ig-council` | `ig-council` (custom advisors) |

## Scripts and data

Python 3, standard library only: `caption.py`, `hookscore.py`, `beats.py`,
`humanize.py`, `detect.py`, `swipe.py`. Call them by bare name from the skill's
own folder; the skills tell you when. Data files: `ig-reel/hooks.json` (26 hook
formulas), `ig-human/slop.json`, `ig-profile/rubric.json`.

## Notes

- **No automation of engagement.** Skills draft replies, DMs and posts. A person
  sends them. Spend, publishing and outreach are always gated. See
  `ig-loops/references/loop-guardrails.md`.
- **Paid ads cover Instagram placements bought through Meta.** Google,
  LinkedIn, B2B/ABM and search-ad material from the source packs was left out.
- **`ig-council` is a persona simulation** built from advisors' published
  frameworks. It is not the real people.
- **Ad-creative and video references** were adapted from public marketing-skills
  material. External tools (HeyGen, Veo, Runway, Remotion and similar) change
  quickly, so confirm current features and pricing before relying on them.
